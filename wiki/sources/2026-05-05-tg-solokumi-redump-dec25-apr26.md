---
id: mkt:sources/2026-05-05-tg-solokumi-redump-dec25-apr26
title: "Telegram @solokumi — повторный дамп декабрь 2025 – апрель 2026 (50 постов 348..402)"
type: source
layer: evolving
theme: content-trends
tags: [ai, marketing, content, vibecoding, claude-code, claude-skills, claude-design, refocus, kumar-solo, telegram, author-channel, redump]
confidence: high
created: 2026-05-05
updated: 2026-05-05
original: raw/processed/articles/tg_solokumi_20260505-134644.md
namespace: mkt
bundle_primary: raw/processed/articles/tg_solokumi_20260505-134644.md
bundle_children:
  - raw/processed/media/tg_solokumi_380.jpg
  - raw/processed/media/tg_solokumi_391.jpg
  - raw/processed/media/tg_solokumi_396.jpg
  - raw/processed/media/tg_solokumi_398.jpg
---

# Telegram @solokumi — повторный дамп (id 348..402, дек 2025 – апр 2026)

Второй backfill-дамп авторского канала [@solokumi](https://t.me/solokumi) (Роман Кумар Виас + Саша Соловьёв, Kumar & Solo). 50 постов id 348..402, частично перекрывает [[sources/2026-04-14-tg-solokumi-nov2025-apr2026|первый дамп]] (id 343..397) — пересечение 348..397, добавляет 5 новых постов 398, 399, 400, 401, 402 и более полный текст по ряду уже виденных постов.

## Метаданные

- **Тип:** Telegram-канал (экспорт текстов + 4 изображения)
- **Период:** 2025-12-01 – 2026-04-30 (5 месяцев, 50 постов)
- **Канал:** https://t.me/solokumi
- **Авторы:** Роман Кумар Виас + Саша Соловьёв (Kumar & Solo)
- **Экспертность автора:** verified — детали в [[sources/2026-04-14-tg-solokumi-nov2025-apr2026|первом дампе]]. Без изменений: серийный предприниматель в EdTech/маркетинге (Refocus, Qmarketing Academy), верифицирован.
- **Sidecar note:** был. Backfill scheduled task «Роман Кумар Виас и Саша Соловьев», категория «Телеграм — Авторские», использовать для контента блога GRO + извлекать релевантные инсайты в другие категории.
- **Sensitive flag:** none — публичный канал.
- **Bundle:** primary + 4 image children (380, 391, 396, 398). Один child (`tg_solokumi_388.zip`) числится как **missing** в `.bundle.json` — он был обработан в первом дампе и переехал в `raw/processed/documents/`, что объясняет «отсутствие» относительно второго bundle-resolution. Не считаем это потерей.
- **Child notes (media):** к каждому из 4 image children приложен `.note.md` с captionом поста.

## Релевантность

Источник высокорелевантен `marketing-memory`. Из 50 постов:

- **~20 постов** — пересекаются с первым дампом, без новой фактуры в большинстве случаев. Не дублируем извлечения, а проверяем через supersession-механику, нет ли уточнений (в этом дампе уточнения в постах 397, 400 — см. ниже).
- **8 постов** — **net new** содержание, не покрытое первым дампом: 384 (Claude Skills lifecycle), 386 (self-hosted SaaS), 395 (5 advanced Claude Code features), 397 (расширенный гайд по /loop / Remote Tasks / HANDOFF.md), 399 (Claude Design release), 400 (sales department AI overhaul с количественными апдейтами), 401 (Bank of AI tools part 2), 402 (Claude Code skills bank).
- **~10 постов** — анонсы эфиров/курсов (как в первом дампе, audit-only).
- **2 поста** — личные / духовные практики Виаса (376 музыкальный альбом, 398 практика медитации). 376 — личное, не выносим. 398 содержит operationalised hooks про «состояние предпринимателя как ROI-инструмент» — релевантно [[evolving/content-trends/owner-escape-operations-hooks]] / [[evolving/content-trends/founder-mental-health-format-2026]] как exemplar founder-mental-health поста, но базовая страница уже есть, добавляем backlink.

## Ключевые идеи (только net-new vs первый дамп)

- **Claude Skills как унифицированный паттерн рабочих промптов.** Skill = `.md`-файл, который активируется автоматически в зависимости от задачи. Правила: 1 скилл = 1 узкая задача, REFERENCE.md для часто-подгружаемых данных, MCP-интеграция = «руки» агента. Это упаковка повторяющихся промптов в командный artifact, который собирается в банк скиллов команды.
- **Self-hosting как inflation hedge.** SaaS-подписки могут съедать 10–15% от расходов компании; n8n / Supabase / Cal.com / Plausible имеют open-source аналоги, разворачиваемые на Oracle Cloud Free Tier (4 vCPU / 24GB RAM / 200GB) или AWS Free Tier бесплатно. Цена входа — 1–2 часа настройки, $50 на Upwork-ера если не девелопер. Это **системный механизм downgrade SaaS-подписок** до in-house-агентов на Claude Code (продолжение тезиса из первого дампа).
- **5 продвинутых фишек Claude Code (пост 395).** MCP-серверы (Figma, Calendar, GitHub, Notion и др.), параллельный запуск дочерних агентов, hooks (скрипты в ответ на действия Клода), `/init` команда для генерации `CLAUDE.md` с нуля, `/think` режим расширенного мышления.
- **/loop + Remote Tasks + HANDOFF.md (пост 397).** Полная схема ночного расписания: `/loop` крутит итерации локально пока комп включён; Remote Tasks выполняется на серверах Anthropic без включённого ноутбука; HANDOFF.md — внешняя память агента между сессиями (промпт «после каждых 10 действий обновляй HANDOFF.md»). Пример ночного расписания: 23:00 — оценка качества звонков; 01:00 — мониторинг кабинетов через 3 роли; 03:00 — конкурентная разведка через Firecrawl; 06:30 — финальный брифинг в Telegram. Для дешёвых задач — Haiku вместо Opus.
- **Claude Design (пост 399, 2026-04-20).** Anthropic выпустил Claude Design на Claude Opus 4.7 — самой мощной визуальной модели. Доступно в Pro / Max / Team / Enterprise планах. Акции Figma -8% после анонса 17 апреля, несколько дизайн-студий начали сокращения. Возможности: слайды/презентации, one-pagers и лендинги, wireframe → high-fidelity, email-шаблоны, связка Design → Code (handoff bundle в Claude Code). Совет: настроить дизайн-систему перед первым использованием (цвета, шрифты, компоненты).
- **Sales department AI overhaul (пост 400, 2026-04-22).** Конкретные количественные данные о трансформации отдела продаж Refocus DE: $35k/мес → <$1k/мес стоимость QA звонков, при переходе с 10% покрытия людьми на 100% покрытия LLM. 55 параметров скоринга на каждый звонок. Связка ИИ контроль качества + ИИ-тренер = собственная разработка Kumar & Solo. Лайфхак — не анализировать звонки <3 мин для экономии токенов. РОПы сами вайбкодят через Cursor + API CRM. Бесплатные транскрибаторы — Fathom (полностью бесплатный), Granola, Fireflies.
- **Bank of AI tools part 2 (пост 401).** Сервисы по узким задачам:
  - **Clay + Claygent** — лидген, 150+ источников, AI-агент сам пишет персональные сообщения и экономит кредиты при поиске контактов
  - **Gumloop** — Zapier с LLM, без кода, используют Webflow/Shopify/Instacart
  - **ElevenLabs** — клонирование голоса + Voice Agents (sub-second response)
  - **Gamma** — слайды из текста, 70M пользователей и $100M ARR к концу 2025; хак — отдать транскрипт созвона → получить КП в слайдах
  - **Granola** — локальный noteтейкер (не объявляет о присутствии в звонке как Fireflies/Fathom), Spaces для шаринга контекста на команду
  - **NotebookLM** — RAG по своим докам, Audio Overview генерирует подкаст-обсуждение документа двумя ведущими
- **Claude Code skills bank (пост 402, 2026-04-30).** Маст-хэв набор:
  - **Superpowers** (150к stars на GitHub) — `/brainstorm`, `/write-plan`, `/execute-plan`
  - **Get Shit Done** — 3 изолированные фазы (план / выполнение / ревью), каждый агент стартует с чистым контекстом 200k токенов, передаёт состояние через файлы
  - **Frontend-design** — заставляет агента принять design-решение до кода (минималистичное / редакторское / ретрофутуристичное)
  - **Marketing Skills** — пак скиллов CRO / копирайтинг / SEO / аналитика / стратегии роста
  - **Claude SEO** — 19 sub-skills + 12 sub-агентов: технический SEO, E-E-A-T, schema, ключевые запросы, бэклинки, локальный SEO, Google API, отчёты PDF/Excel
  - **Composio** — MCP-интеграция к 500+ внешним сервисам
  - **Deep Research** — 8-фазный pipeline с оценкой достоверности источников
  - **Code Simplifier** — официальный плагин Anthropic, чистит мусор и снижает расход токенов
  - **Superflow** — проектирование сложных задач через project-flow
  - **SkillHub** — маркетплейс с 7000+ скиллов, one-click install
- **«Креатив = таргетинг» (пост 387, 2026-03-20) — кристаллизация в одну фразу.** Это не фигура речи, а лучшее определение того, как работают рекламные системы в 2026: что Meta, что TikTok и Яндекс сводят все к «запусти максимально широкий таргетинг и ничего не трогай», дальше именно креатив определяет аудиторию и цену. Стоимость UGC-ролика упала с $200–250 до $5–20 (формализуется в [[canon/marketing-frameworks/andromeda-creative-framework-2026]]).
- **Atria (пост 394, 2026-04-08) — конкурентный шпион в коробке.** Apка для отслеживания креативов и лендингов конкурентов. Подписка → видишь все активные креативы; clone-add → получаешь готовый адаптированный креатив; A+/iteration potential/underperforming оценка собственных креативов. Триггер для того, чтобы Виас написал «жестко подгорело» — Kumar & Solo пилили эту автоматизацию месяц.
- **Landing за 15 минут через Figma → Cursor (пост 358, 2025-12-23).** 8-шаговый процесс: html.to.design plugin → Copy as → CSS → Cursor проект → Claude Code (Pro) → промпт → генерация → итерация → публикация (GitHub / Figma / Tilda). Канонический pattern для маркетолога без дизайнера/разработчика.
- **AI мультики как формат (пост 379).** Pixar / Disney / 2D-comic / semi-realistic 3D / cartoon 2D — стили с готовыми промптами. 3-фазный pipeline: сценарий через Claude → стартовые фреймы (Midjourney / Nano Banana с референсом персонажа) → анимация в Higgsfield/VEO3 → монтаж в CapCut.

## Факты и цифры (net new vs первый дамп)

- **$35,000/мес → <$1,000/мес** стоимость QA звонков отдела продаж в Refocus, при переходе с 10% покрытия людьми на 100% покрытия LLM (пост 400, 2026-04-22)
- **55 параметров** скоринга каждого звонка отдела продаж в текущей системе Refocus DE (пост 400, 2026-04-22) — supersedes исходный «50 параметров» из поста 377 первого дампа
- **Figma -8%** в день 17 апреля 2026 после анонса Claude Design (пост 399, 2026-04-20)
- **Gamma — 70M пользователей и $100M ARR к концу 2025** (пост 401, 2026-04-27) — третья сторона, expert claim
- **Superpowers — 150k звёзд на GitHub** (пост 402, 2026-04-30)
- **SkillHub — 7000+ скиллов** в маркетплейсе (пост 402, 2026-04-30)
- **Claude SEO — 19 sub-skills + 12 sub-агентов** (пост 402, 2026-04-30)
- **Composio — 500+ внешних сервисов** через MCP (пост 402, 2026-04-30)
- **Deep Research — 8-фазный pipeline** оценки источников (пост 402, 2026-04-30)
- **Refocus QA cost ratio:** покрытие выросло **в 10× (10% → 100%)** при снижении стоимости **в ~35× ($35k → <$1k)** — комбинированный эффект **~350×** на $/звонок (пост 400)
- **80% маркетинговых SaaS-подписок реально запилить in-house за полторы недели** на Claude Code (пост 390, 2026-03-31) — expert claim founder
- **Anthropic /loop команда выкачена в марте 2026** (пост 397, 2026-04-14) — фактическая дата релиза
- **47% брендов используют AI в рекламе сейчас, 90% будет в 2026** (пост 349, 2025-12-03) — expert claim founder, без независимого подтверждения
- **Кампания Чувствует Refocus DE: маржа 2.5× выше СНГ, $2M ARR за 10 мес, цель $18M к декабрю** — без изменений vs первый дамп
- **Stripe — Voice Agents с sub-second response** (пост 401, через ElevenLabs)
- **Параллельный запуск агентов в Claude Code увеличивает скорость в 3×, токены тоже в 3×** (пост 395, 2026-04-10) — expert claim

## Медиа-вложения

### tg_solokumi_380.jpg — график выручки Refocus DE (повтор из первого дампа)

Тот же image, что в первом дампе. Данные не изменились. См. [[evolving-strict/product-metrics/refocus-germany-2026-growth]] и audit в [[sources/2026-04-14-tg-solokumi-nov2025-apr2026]].

### tg_solokumi_391.jpg — VIBECON постер (повтор)

Тот же image. См. описание в первом дампе. Используется как сигнал консолидации vibecoding-категории.

### tg_solokumi_396.jpg — конференция «фокус/состояние фаундера» (повтор)

Тот же image. См. описание в первом дампе.

### tg_solokumi_398.jpg — медитация как ROI-инструмент

Новое изображение в этом дампе (пост 398, 2026-04-17). По caption — заглавная картинка к лонгриду «Почему медитация — один из главных ROI-инструментов в моей жизни как предпринимателя». Не описание поста — сама статика к посту, а текст лонгрида содержит operational-фреймворк (Анапана 20–30 мин ежедневно; випассана 2× в год; дыхание 4-7-8 для острых ситуаций). Связано с [[evolving/content-trends/founder-mental-health-format-2026]] и [[evolving/content-trends/owner-escape-operations-hooks]] как exemplar founder-mental-health поста с конкретным operational-выходом, а не motivational fluff.

## Распознанный текст

Не применимо: image-children — captionable visuals (графики/постеры), их fact-content включён в caption, отдельной OCR-секции не требуется.

## Связанные страницы

Net-new страницы, созданные из этого источника:

- [[canon/marketing-frameworks/claude-skills-architecture]] — Claude Skills как командный artifact: 1 скилл = 1 задача, REFERENCE.md, MCP-интеграция
- [[canon/marketing-frameworks/landing-15min-figma-cursor]] — 8-шаговый процесс «лендинг за 15 минут» через Figma html.to.design + Cursor + Claude Code
- [[evolving/content-trends/ai-tools-self-hosting-arbitrage]] — self-hosting open-source альтернатив SaaS на Free Tiers как inflation hedge
- [[evolving/content-trends/claude-code-skills-bank-2026]] — банк маст-хэв скиллов Claude Code (Superpowers, GSD, Frontend-design, Marketing Skills, Claude SEO, Composio, Deep Research, Code Simplifier, Superflow)
- [[evolving/content-trends/sales-ops-ai-tooling-stack-2026]] — ops-стек продажника-2026 (Clay+Claygent, Gumloop, ElevenLabs, Gamma, Granola, NotebookLM, Fathom)
- [[evolving/competitor-positioning/claude-design-2026]] — Claude Design как конкурент Figma и шаг Anthropic в visual-дизайн
- [[volatile-strict/competitor-news/anthropic-claude-design-launch-2026-04]] — анонс Claude Design 2026-04-17, Figma -8%

Страницы, обновлённые backlink + новой фактурой:

- [[canon/marketing-frameworks/claude-md-structure-marketing]] — добавлены 5 advanced features (MCP, parallel agents, hooks, /init, /think) и /loop + Remote Tasks + HANDOFF.md
- [[evolving-strict/product-metrics/refocus-germany-2026-growth]] — supersession 50→55 params; новый факт $35k → <$1k QA cost
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]] — Atria и Claude Design как новые элементы стека
- [[volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1]] — Atria, Claude Design, Skills Bank, /loop+Remote Tasks как новые consolidation-сигналы

## Contradictions

- **«50 параметров» (пост 377, дамп 1, 2026-02-16) vs «55 параметров» (пост 400, дамп 2, 2026-04-22)** — сейлз-QA параметризация. Разрешение: новое значение более свежее, supersede на странице [[evolving-strict/product-metrics/refocus-germany-2026-growth]]; старое оборачиваем в HTML-коммент.
