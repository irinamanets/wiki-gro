---
id: mkt:evolving/content-trends/sales-ops-ai-tooling-stack-2026
title: "Sales-ops AI tooling stack — апрель 2026 (Clay / Gumloop / ElevenLabs / Gamma / Granola / NotebookLM)"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [sales-ops, ai, tooling, lead-generation, voice-agents, presentations, transcription, rag, claygent, gumloop, elevenlabs, gamma, granola, notebooklm, fete-framework, dadata, kontur-focus, sbis, n8n, unisender]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-14
sources: [sources/2026-05-05-tg-solokumi-redump-dec25-apr26.md, sources/2026-05-14-tg-solokumi-may-2026.md]
namespace: mkt
---

# Sales-ops AI tooling stack — апрель 2026

Дрейфующий каталог точечных AI-инструментов для sales-ops и marketing-ops, рекомендованных Kumar & Solo в посте 401 «Банк AI инструментов для решения конкретных задач (Часть 2)». Связан с [[evolving/content-trends/claude-code-skills-bank-2026]] (Claude Code skills bank) как **дополняющий слой**: skills-bank — это in-house агенты на инструментальном уровне, а этот стек — узкоспециализированные SaaS, которые дешевле/быстрее купить, чем строить.

Это evolving: каждый элемент стека дрейфует с появлением аналогов, изменением цен и расширением фич. TTL 90 дней soft re-verify.

Источник: Р. Кумар Виас, [[sources/2026-05-05-tg-solokumi-redump-dec25-apr26|@solokumi]] пост 401 (2026-04-27). Часть 1 банка инструментов — в первом дампе (пост 367 Manus, пост 366 vibecoding tier).

## Контекст

«Бизнес сейчас выигрывает не у того, кто лучше настраивает кампании, а у того, кто быстрее и дешевле крутит креативный конвейер» (пост 389) — но это **только маркетинг**. Параллельно идёт sales-конвейер с своими bottleneck'ами: лидген, voice-agents, презентации, фиксация договорённостей со звонков. Ниже — что Виас рекомендует ставить под каждый bottleneck.

## Лидген и outbound

### Clay + Claygent — лидген на стероидах

[Clay](https://clay.com/) — топ-инструмент, который мало кто из русскоязычной аудитории реально щупал. Собирает данные о лиде из **150+ источников** `[conf:high, src:2026-04-27]` в одну таблицу: LinkedIn, стек технологий на сайте, новостной фон, последние найм-активности.

**Claygent** — AI-агент внутри Clay. Сам заходит на сайт компании, читает страницы и пишет первое сообщение под конкретного человека, которое звучит так, будто вы час сидели и собирали данные вручную.

**Лайфхак на токены:** агент проверяет базы данных одну за другой (Apollo, Hunter и ещё десяток других) и **останавливается, как только нашёл нужные контакты** `[conf:high, src:2026-04-27]` — не тратит кредиты на все источники сразу.

### Gumloop — Zapier с LLM, без кода

[Gumloop](https://gumloop.com/) — строит процесс из блоков, без кода, как Zapier, но с LLM встроенным:

- лид падает в форму → Gumloop обогащает через Clay → квалифицирует контакты через GPT/Opus → менеджер получает уже разобранный список

**Стоит дешевле большинства аналогов** `[conf:medium, src:2026-04-27]`, на нём сидят команды Webflow, Shopify, Instacart и других топ-компаний.

## Голос

### ElevenLabs — клонирование голоса + Voice Agents

[ElevenLabs](https://elevenlabs.io/): клонируете голос за минуту и дальше озвучиваете любые тексты с сохранением тембра.

**Voice Agents** — AI-бот разговаривает голосом с клиентом по телефону или в поддержке в реальном времени, **скорость отклика — менее секунды** `[conf:high, src:2026-04-27]`. Несколько знакомых Виаса убрали часть колл-центра и поставили это.

В Refocus DE на ElevenLabs работает их собственный AI-тренер продажников; отдельные участки sales-flow тоже автоматизируются.

## Презентации

### Gamma — слайды из текста

[Gamma](https://gamma.app/): скидываешь заметки, брифинг или рандомный текст и получаешь красивый дек с визуалами. **70 миллионов пользователей и $100M ARR к концу 2025** `[conf:medium, src:2026-04-27]` — третья сторона, expert claim founder без независимого подтверждения.

**Killer-хак:** отдаёшь Gamma транскрипт созвона с клиентом → через полминуты получаешь КП в слайдах.

С появлением Claude Design (см. [[evolving/competitor-positioning/claude-design-2026]]) актуальность Gamma снизилась, **но по cost'ам Гамма всё ещё топчик** на конец апреля 2026 `[conf:medium, src:2026-04-27]`.

## Созвоны и заметки

### Granola — локальный noteтейкер без объявления

[Granola](https://granola.ai/): работает **локально на вашем компьютере**, в звонок не заходит и собеседников не пугает. После встречи выдаёт транскрипт с action items.

**Уникальная фича:** единственный noteтейкер, который **не объявляет о своём присутствии**, как это делают Fireflies, Fathom и другие `[conf:high, src:2026-04-27]`. Это критично, когда ваш собеседник параноит или просто не любит ботов на встречах.

Недавно добавили **Spaces** — общий контекст встреч, который шарится на команду.

### Fathom — бесплатный транскрибатор для всех звонков

[Fathom](https://fathom.video/) — упомянут в посте 400 как часть стека Refocus DE для транскрибации 100% звонков отдела продаж. **Полностью бесплатный** `[conf:high, src:2026-04-22]`, что и позволило Refocus уронить стоимость QA с **$35,000/мес → <$1,000/мес** при 10× расширении покрытия (см. [[evolving-strict/product-metrics/refocus-germany-2026-growth#стоимость-qa-звонков]]).

Альтернативы: Granola (локальный, для приватных), Fireflies (облачный с объявлением).

## Ресёрч по своим документам

### NotebookLM — RAG без галлюцинаций

[NotebookLM](https://notebooklm.google.com/): загружаешь свои доки, транскрипты, статьи, задаёшь вопросы и получаешь ответы **строго по ним без выдумок** `[conf:high, src:2026-04-27]`.

**Audio Overview** — фича, которая загружает документ и выдаёт **подкаст с двумя AI-ведущими, которые его обсуждают** `[conf:high, src:2026-04-27]`. Можно слушать во время прогулки вместо чтения 40-страничного отчёта.

Для подключения Claude Code к NotebookLM через API есть [notebooklm-py](https://github.com/teng-lin/notebooklm-py).

В Refocus DE NotebookLM используется как ИИ-симулятор для обучения языку — со студентами, геймификацией и лидербордом (пост 377 первого дампа).

## Сводная таблица — bottleneck → tool

| Bottleneck в sales-ops | Рекомендуемый tool 2026 | Альтернативы | Source |
|---|---|---|---|
| Лидген + персонализация outbound | Clay + Claygent | Apollo + GPT, Lemlist | `[conf:high, src:2026-04-27]` |
| Workflow-автоматизация без кода | Gumloop | n8n self-hosted (см. [[evolving/content-trends/ai-tools-self-hosting-arbitrage]]), Zapier+OpenAI | `[conf:high, src:2026-04-27]` |
| Голосовой AI-агент | ElevenLabs Voice Agents | Bland.ai, Vapi.ai | `[conf:high, src:2026-04-27]` |
| Презентации из текста | Gamma | Claude Design (свежий), Tome | `[conf:medium, src:2026-04-27]` |
| Транскрипт созвонов (приватный) | Granola | Fathom (бесплатный), Otter | `[conf:high, src:2026-04-27]` |
| Транскрипт всех звонков (массовый) | Fathom | Granola Spaces, Fireflies | `[conf:high, src:2026-04-22]` |
| RAG по своим документам | NotebookLM | Custom Claude Code + MCP, Glean | `[conf:high, src:2026-04-27]` |

## Anti-patterns

- **Купить весь стек сразу** — это $200–500/мес и большая часть инструментов не используется. Ставить под конкретный bottleneck.
- **Использовать ElevenLabs Voice Agent для high-touch B2B продаж** — результат рассказчиков смешанный. Подходит для cold-screening, не для closing.
- **Заменить Granola на Fathom без learning** — Fathom объявляет о присутствии, может изменить динамику звонка.
- **Доверять Gamma 70M users / $100M ARR** как факту индустрии — это expert claim founder Виаса, без независимого подтверждения. Использовать как сигнал «инструмент работает», не как точную метрику.

## Update 2026-05-14 — FETE-фреймворк и RU-стек как альтернатива

[[sources/2026-05-14-tg-solokumi-may-2026|Solokumi пост 403]] (2026-05-05) фиксирует **процессный фреймворк** поверх Clay-стека — **FETE: Find → Enrich → Transform → Export**. Это полная operating model для outbound, теперь канонизирована как [[canon/marketing-frameworks/fete-outreach-framework-clay|отдельная страница в canon/marketing-frameworks]]. Каталог инструментов на этой странице — **тактическая реализация** FETE.

**Метрика эффекта FETE**: шаблонный outreach даёт **1.1% response rate**, FETE через Clay/Claygent — **4%+** `[conf:high, src:2026-05-05]`. Это ~4x улучшение, при том что время первой настройки — 3–4 часа `[conf:medium, src:2026-05-05]`.

**Двойной промпт-паттерн Transform-шага** (Виас публикует прямо в посте):

1. **Свежий контент**: «Visit {company_website}. Find the most recent blog post / case study / news from the last 90 days. Write one sentence (max 20 words) opening line referencing it».
2. **Реальные боли клиентов**: «Search for recent reviews of {company_name} on G2 or Trustpilot. Find 1-2 specific pain points. Write one sentence referencing this pain and connecting it to a solution. Max 20 words».

Второй промпт даёт ещё больший uplift — но сложнее обходит anti-bot на G2/Trustpilot.

### RU-стек как 5–10x дешевле Clay

Для русскоязычного рынка Clay избыточен (оптимизирован под US/EU данные). Виас приводит функциональный эквивалент `[conf:medium, src:2026-05-05]`:

| Шаг FETE | Clay (глобал) | RU-стек |
|---|---|---|
| Find | Apollo / LinkedIn Sales Navigator | **Dadata** (реквизиты и выручка по ИНН, 10К запросов/день бесплатно) |
| Enrich | Hunter / BuiltWith / Google News | **Контур.Фокус API** (финансы + связи юрлиц), **СБИС** (контакты юрлиц) |
| Transform | Claygent | **n8n** + Claude / GPT через API |
| Export | Instantly / Smartlead / Lemlist | **Unisender** / SendPulse |

Trade-off: 5–10x дешевле, но нужен интегратор (n8n flow, API-ключи, prompt engineering) — 1–2 недели сборки.

## Когда страница должна быть обновлена

- Появятся независимые подтверждения метрик Gamma — снять caveat
- Voice Agents выйдут на 1-second responses или ниже на массовом рынке — обновить рекомендации
- Появятся local-only альтернативы NotebookLM — добавить в таблицу
- Granola добавит критичные фичи (или потеряет) — пересмотреть рекомендацию
- FETE response rate (1.1% → 4%) перепроверить через 3 мес — anti-bot защита может снизить эффективность Transform-шага

## Связь с другими страницами

- [[evolving/content-trends/claude-code-skills-bank-2026]] — параллельный стек in-house на Claude Code
- [[evolving/content-trends/ai-tools-self-hosting-arbitrage]] — self-host альтернативы (n8n vs Gumloop, Plausible vs GA)
- [[canon/marketing-frameworks/multi-agent-marketing-org-principles]] — где эти tools выступают исполнителями в слое 3
- [[evolving-strict/product-metrics/refocus-germany-2026-growth]] — case-study, на которой эти инструменты собраны
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]] — навык «знать tooling под каждый bottleneck» как часть профиля 2026

## Backlinks

_8 pages link to this one._

- [[evolving-strict/product-metrics/refocus-germany-2026-growth]]
- [[evolving/competitor-positioning/claude-design-2026]]
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]]
- [[evolving/content-trends/claude-code-skills-bank-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-solokumi-redump-dec25-apr26]]
- [[volatile-strict/competitor-news/anthropic-claude-design-launch-2026-04]]
