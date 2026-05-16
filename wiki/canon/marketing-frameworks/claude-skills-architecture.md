---
id: mkt:canon/marketing-frameworks/claude-skills-architecture
title: "Claude Skills — командный artifact для повторяемых маркетинговых задач"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai, claude-code, claude-skills, prompt, vibecoding, agents, marketing-ops, knowledge-management]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-14  # +self-calibration pattern from Annakov's slide-inspector — skill analyses user's past sessions to auto-extend with their "house rules"
sources: [sources/2026-05-05-tg-solokumi-redump-dec25-apr26.md, sources/2026-04-14-tg-solokumi-nov2025-apr2026.md, sources/2026-05-14-tg-products-and-startups-may-2026.md]
namespace: mkt
---

# Claude Skills — упаковка проверенных промптов в командный artifact

**Claude Skill** — `.md`-файл, который Claude Code (или Claude.ai) автоматически активирует, когда задача попадает под его область применения. По сути это **банк проверенных промптов**: вы описываете один раз, как должен решаться повторяющийся класс задач, и потом просто запускаете задачу — скилл срабатывает автоматически, без явного его упоминания в промпте.

Это canon: сама архитектура «скилл = модульный артефакт со срабатыванием по контексту» — стабильная инженерная рекомендация на эпоху IDE-агентов. Конкретные библиотеки скиллов (Superpowers, Marketing Skills, Claude SEO, Frontend-design, Composio и т.д.) — дрейфующий слой, живёт в [[evolving/content-trends/claude-code-skills-bank-2026]].

Источник: Р. Кумар Виас, [[sources/2026-05-05-tg-solokumi-redump-dec25-apr26|@solokumi]] пост 384 (2026-03-13) — главный гайд по skills lifecycle, плюс пост 388 (2026-03-23) — публичный релиз ZIP-архива со скиллами для генерации статических баннеров через Higgsfield + Nano Banana, и пост 402 (2026-04-30) — банк маст-хэв скиллов.

## Зачем это маркетологу

Маркетинговая работа — это **много повторяющихся задач**: разбивка креатива конкурентов на параметры, генерация промптов для Nano Banana, аудит вебинарной воронки, генерация еженедельных отчётов по кампаниям, написание поста в TOV бренда, разбор звонка отдела продаж. Без скиллов вы каждый раз заново даёте Claude всю инструкцию по пять-десять минут «вспомни наш TOV», «вот критерии», «вот шаблон отчёта». Со скиллами — один раз настроили, дальше срабатывает автоматически.

Это **тот же паттерн, что используется при инженерной работе**: harness для повторяемости (см. [[canon/marketing-frameworks/harness-engineering-for-ai-agents]]). Claude Skill — единица harness'а для маркетолога.

## Канонические правила skill design

### Правило 1 — 1 скилл = 1 узкая задача

Не пихайте в один скилл цепочку «спарсь конкурентов → проанализируй → сгенерируй идеи → напиши копи → визуализируй». Это превращается в монолит, который агент плохо соблюдает. Разбивайте сложную задачу на цепочку специализированных скиллов:

- **Creatives Ideas Generator** — просит аналитику по лучшим креосам и генерирует идеи
- **Creatives Copy Generator** — пишет копирайт креатива на основе идей
- **Visualizer** — придумывает визуальную идею и сразу присылает промпты для Nano Banana

В одном треде Claude активирует их **последовательно**, передавая контекст между ними.

### Правило 2 — REFERENCE.md для часто-подгружаемых данных

Если у вас есть файлы, которые вы постоянно подгружаете как контекст — анализ ЦА, AJTBD-интервью, JTBD-карты, выписки звонков, ToV-документы, бренд-гайдлайны — они не должны жить в самом `SKILL.md`. Они засоряют контекстное окно и нарушают правило 200 строк (см. [[canon/marketing-frameworks/claude-md-structure-marketing#жёсткий-лимит]]).

Правильно:
- Отдельный `REFERENCE.md` или папка `references/` внутри директории скилла
- В `SKILL.md` только указание: «когда нужно идти в [файл] за [контекстом]»

Это разделяет **что делать** (skill) от **на каких данных** (reference). Reference обновляется отдельно и независимо.

### Правило 3 — MCP-интеграция как «руки» скилла

Skill можно связать с внешними сервисами через MCP-серверы (Model Context Protocol):

- **Notion / Linear / Jira** — скилл сам ходит в базу знаний и ищет нужный контекст
- **Google Drive / Slack / GitHub** — скилл сам берёт данные оттуда
- **Figma / Excalidraw** — скилл рисует диаграммы
- **Telegram / Email / CRM** — скилл сам отправляет результат
- **Composio** — meta-MCP: 500+ внешних сервисов через единый интерфейс (см. [[evolving/content-trends/claude-code-skills-bank-2026#composio]])

Без MCP скилл — это «мозг без рук»: даёт идеи, пишет тексты, но не выполняет действия в ваших системах. С MCP — полноценный исполнитель.

### Правило 3a — Self-calibration step (Аннаков, slide-inspector pattern)

Update 2026-05-14 ([[sources/2026-05-14-tg-products-and-startups-may-2026]] пост 1747): Байрам Аннаков добавил в свой open-source skill `slide-inspector` ([github.com/BayramAnnakov/ai-personal-os-skills/tree/main/skills/slide-inspector](https://github.com/BayramAnnakov/ai-personal-os-skills/tree/main/skills/slide-inspector)) **шаг калибровки** — переиспользуемый архитектурный паттерн для skill design.

**Что делает шаг калибровки:**

1. Skill при инициализации анализирует **прошлые Claude Code сессии пользователя** на предмет правок выходов того класса задач, который скилл обслуживает (для slide-inspector — pptx-исправлений)
2. Из этих правок извлекает **«фирменные» правила пользователя** (типичные исправления, которые он делает руками)
3. Расширяет себя этими правилами — то есть на следующем запуске skill уже знает о specific-styles пользователя

**Почему этот паттерн важен:**

- **Solves cold-start problem of generic skills:** общий skill не знает о ваших правилах оформления. Self-calibration делает его персонализированным с нулевой ручной настройкой.
- **Reusable architecture:** применимо к **любому** skill, который ассистирует на структурируемом выводе (writeups, slides, code, документы). Skill обнаруживает паттерн «исправление» (diff между его выходом и финальной версией) и инкорпорирует.
- **Reduces feedback loop drift:** правки, сделанные пользователем, не теряются между сессиями. Skill становится **noticeable** лучше через 2-3 calibration-цикла.

**Когда применять:**

- Skill производит **структурируемый артефакт** (slide, lengthy document, code section)
- Пользователь регулярно делает правки **одного типа** (форматирование, тон, специфика данных)
- Существует **diff-detection** для нужного типа артефакта (для pptx — структура файла; для текста — line-diff; для кода — AST)

**Когда не работает:**

- Skill решает **одноразовые** задачи (генерация ad-hoc мемов)
- Артефакт не структурируем (свободный творческий текст с непредсказуемой структурой)
- Прошлых сессий нет (cold start absolute)

### Правило 4 — Skills bank как методология команды

Если убрать весь хайп с агентов и разложить его на 2 составляющие:

1. **Обычная автоматизация только с участием LLM**
2. **Методология, с помощью которой вы решаете задачу**

Второе сильно важнее первого. Автоматизировать процесс с понятной последовательностью действий и логикой — просто. Вся суть — в правильности логики.

Поэтому **командное правило**, рекомендуемое Kumar & Solo: при решении задачи **всегда сохранять и прикладывать использованные промпты к решению**. Это собирается в банк знаний, который потом легко превращается в скиллы.

Skills bank = живой методологический справочник команды, а не хобби одного гика.

## Реальные используемые скиллы Kumar & Solo

Эти примеры — от Виаса в посте 384, как иллюстрация:

- **TOV** — чтобы Claude всегда писал контент в стиле бренда (Tone of Voice)
- **Webinar funnel audit** — чеклист для проверки воронки вебинара
- **Reporting skill** — автоматическая генерация еженедельных отчётов по кампаниям

Плюс ZIP-архив, опубликованный публично 2026-03-23 (пост 388) — фреймворк генерации статических баннеров через Higgsfield + Nano Banana, на вход — описание персон, AJTBD-интервью, инфа о клиентах. Артефакт лежит в [[sources/2026-04-14-tg-solokumi-nov2025-apr2026|первом дампе]] как `raw/processed/documents/tg_solokumi_388.zip`.

## Anti-patterns

- **Mega-skill на 500 строк** — после ~200 строк Claude перестаёт его соблюдать (тот же лимит, что у [[canon/marketing-frameworks/claude-md-structure-marketing|CLAUDE.md]]). Разбивайте на узкоспециализированные скиллы.
- **Skill без self-calibration на structured-выводе** — упускаете 2-3-цикл'овую возможность сделать skill заметно лучше под пользователя без ручной правки.
- **50 одновременно активных скиллов** — агент путается в инструкциях, результат хуже чем без скиллов. Собирайте маленький стек под повторяющиеся процессы.
- **Skill без REFERENCE.md** — если каждый раз вручную подгружаете один и тот же контекст, это сигнал, что нужен reference-файл.
- **Skill без MCP** — мозг без рук, ограничивает полезность.
- **Использовать только чужие скиллы из маркетплейса** — лучший скилл, который у вас будет, тот, что вы напишете сами под свой процесс.

## Где брать готовые скиллы

- **SkillHub** — маркетплейс с 7 000+ скиллов и one-click install (пост 402, 2026-04-30)
- **Built-in marketplace** в Claude Code
- **GitHub-репозитории** конкретных коллекций — список и обзоры в [[evolving/content-trends/claude-code-skills-bank-2026]]

## Связь с другими страницами

- [[canon/marketing-frameworks/claude-md-structure-marketing]] — `CLAUDE.md` как корневой брифинг проекта; скилл — модульная инструкция под конкретную задачу
- [[canon/marketing-frameworks/multi-agent-marketing-org-principles]] — где скиллы выступают «должностными инструкциями» для AI-сотрудников
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — общая концепция harness; skill — частный случай
- [[evolving/content-trends/claude-code-skills-bank-2026]] — дрейфующий каталог конкретных скиллов 2026 (Superpowers, GSD, Marketing Skills, Claude SEO и т.д.)
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]] — экосистема, в которой скиллы живут
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]] — навык «уметь паковать процесс в скилл» как часть профиля 2026

## Backlinks

_9 pages link to this one._

- [[canon/marketing-frameworks/claude-md-structure-marketing]]
- [[canon/marketing-frameworks/landing-15min-figma-cursor]]
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]]
- [[evolving/content-trends/ai-tools-self-hosting-arbitrage]]
- [[evolving/content-trends/claude-code-skills-bank-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-solokumi-redump-dec25-apr26]]
- [[volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1]]
