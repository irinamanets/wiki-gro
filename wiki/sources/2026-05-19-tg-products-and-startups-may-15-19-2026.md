---
id: mkt:sources/2026-05-19-tg-products-and-startups-may-15-19-2026
title: "Telegram @ProductsAndStartups (Байрам Аннаков) — 7 постов 15–19 мая 2026 (1749–1755)"
type: source
layer: evolving
theme: industry-trends
tags: [content, ai-agents, verification, accountability, ai-security, harness-engineering, code-with-claude, social, awareness]
confidence: high
created: 2026-05-19
updated: 2026-05-19
original: raw/processed/articles/tg_ProductsAndStartups_20260519-133332.md
bundle_primary: raw/processed/articles/tg_ProductsAndStartups_20260519-133332.md
bundle_children:
  - raw/processed/media/tg_ProductsAndStartups_1749.jpg
  - raw/processed/media/tg_ProductsAndStartups_1750.jpg
  - raw/processed/media/tg_ProductsAndStartups_1751.jpg
  - raw/processed/media/tg_ProductsAndStartups_1752.mp4
  - raw/processed/media/tg_ProductsAndStartups_1753.jpg
  - raw/processed/media/tg_ProductsAndStartups_1754.jpg
  - raw/processed/media/tg_ProductsAndStartups_1755.jpg
namespace: mkt
---

# Telegram @ProductsAndStartups (Байрам Аннаков) — 7 постов 15–19 мая 2026 (1749–1755)

## Метаданные

- **Тип:** Telegram-канал, авторский дамп (bundle: primary article + 7 медиа)
- **Канал:** [@ProductsAndStartups](https://t.me/ProductsAndStartups)
- **Автор:** Байрам Аннаков, founder & CEO **onsa.ai** (автоматизация B2B-продаж), создатель курса AI Product Engineer (Empatika)
- **Период:** 2026-05-15 — 2026-05-19
- **Сообщений:** 7 (id 1749–1755), 7 медиа-вложений
- **Дата добавления:** 2026-05-19 13:33 UTC (backfill task «Байрам Аннаков»)
- **Экспертность автора:** **verified** — sidecar `.note.md` («Фаундер and CEO onsa.ai») + многократно подтверждённый bio в предыдущих дампах ([[sources/2026-04-14-tg-products-and-startups-feb-apr-2026]], [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]], [[sources/2026-05-14-tg-products-and-startups-may-2026]]). Эксперт по AI-agents engineering, B2B sales automation, agentic-discipline. `confidence: medium–high` на его синтетических тезисах.
- **Sidecar note:** да — backfill-задача «Авторские телеграм-каналы», помечает использование для постов в блоге ГРО и трекинга трендов.
- **Sensitive flag:** нет (только публичные URL, research papers, публичные выступления конференции).

## Релевантность

Высокая по большинству постов — прямое продолжение предыдущего дампа (1740–1748). Пост 1750 — «Заметки с полей **- 2**», явное продолжение поста 1748 («Заметки с полей - 1», основа [[canon/marketing-frameworks/ceo-cto-ai-adoption-bridge]]). Тематический стержень всего дампа — **сдвиг узкого места из «делания» в «верификацию / ответственность / безопасность» агентов**, что независимо подтверждает direction #3 страницы [[evolving/industry-trends/ai-value-migration-2026]] (Морейнис: «по мере удешевления ИИ дорожает верификация»).

**Релевантно (извлечения в слои):**
- 1750 (ответственность/accountability как новая премия + AIUC-страховка AI-агентов — **новый фреймворк** + cross-confirmation),
- 1751 (OOD adversarial-атаки на AI-агентов, Microsoft Research whimsical-strategies — **новый фреймворк** про архитектурные guardrails),
- 1752 + 1753/1754/1755 (7 идей с конфы Code w/ Claude + OCR mini-сайта: Advisor pattern, Half-Life Rule, Amdahl-as-strategy, 3 аспекта памяти агента — **новая insight-страница**),
- 1753 (персонализированное потребление контента через zettelkasten + generative HTML — content-trend).

**Нерелевантно (только audit):**
- 1749 (анонс эфира «Economics of AGI», luma RSVP) — низкая half-life, registration-ссылка, не оправдывает page-создание. Образ — декоративный (рукопожатие человек+робот).

## Ключевые идеи

- **Ответственность как новая премия в софте (пост 1750).** Узкое место разработки сместилось из «делания» (AI удешевил кратно) в **верификацию**, а оттуда — в **accountability**: «маржу в софте всё больше будет забирать не тот, кто пишет код, а тот, кто **гарантирует поведение/результат**». За что платить премию, когда делать стало дёшево: за умение обуздать AI, за готовность взять ответственность, за гарантию работы агента. → [[evolving/industry-trends/ai-accountability-premium-2026]], расширяет [[canon/marketing-frameworks/ceo-cto-ai-adoption-bridge]].
- **AI-agent insurance как рынок (пост 1750).** В феврале 2026 ElevenLabs объявили первую публичную страховку, покрывающую действия AI-агентов, построенных на их платформе; андеррайтит третья сторона — Artificial Intelligence Underwriting Company (AIUC, страхует потери от AI до $50M). Сертификация **AIUC-1** выдаётся после прогона агентов через 6К adversarial-тестов в 14 категориях рисков; даёт **75% апрува** (остальное — дополнительные чеки). → [[volatile-strict/competitor-news/elevenlabs-aiuc-agent-insurance-2026]].
- **OOD adversarial-стратегии ломают AI-агентов (пост 1751).** Microsoft Research («whimsical strategies»): агенты прокачаны RLHF против **известных** человеческих манипуляций (якорение, ложный авторитет, эмоциональное давление), но **абсурдные кросс-доменные** стратегии обходят защиту. Метод генерации: взять 2 500 случайных статей Википедии → попросить LLM построить из каждой фрейм для торга → получить 30 000 OOD-тактик. Главный тезис: **«Промпт "будь хорошим" — последняя линия защиты, а не первая»**; для агентов с доступом к деньгам/действиям нужно **архитектурное** ограничение (нельзя давать скидку > $N) + регулярный red-teaming. → [[canon/marketing-frameworks/ai-agent-architectural-guardrails-2026]].
- **7 идей с конфы Code w/ Claude 2026 + центральная тема (пост 1752 + 1753/1754/1755).** Центральная тема всех докладов: **узкое место сдвигается в инфраструктуру вокруг модели** — harness, системы обратной связи, верификации, контекст/память, безопасность агентов, эвалы. Топ-идеи: Advisor pattern (Haiku-executor + Opus-advisor через tool call), Half-Life Rule (код вокруг ненадёжности модели имеет half-life месяцы → удалится; код, подключающий к вашему уникальному миру — компаундится), Amdahl's Law как бизнес-стратегия (ускорил один этап в 3-5х → bottleneck migration, задача CEO — медленные стадии). → [[evolving/industry-trends/code-with-claude-2026-frameworks]].
- **Персонализированное потребление контента (пост 1753).** Pipeline: транскрипт YouTube (yt-dlp / AssemblyAI) → прогон через zettelkasten для отбора близких кусочков → generative mini-site (HTML, а не markdown) + NotebookLM для аудио на прогулках. Тезис: **визуализировать аутпут модели как интерактивную HTML-страницу, а не markdown** — суперудобно для нелинейной работы с материалом. Рифмуется с Generative UI ([[canon/marketing-frameworks/generative-ui-design-system-inference]]).

## Факты и цифры

### AI-agent insurance (пост 1750, ElevenLabs/AIUC)
- ElevenLabs объявили первую публичную страховку AI-агентов — **февраль 2026** `[conf:high, src:2026-05-16]`
- Андеррайтер: Artificial Intelligence Underwriting Company (AIUC), страхует потери от AI до **$50M** `[conf:medium, src:2026-05-16]`
- Сертификация AIUC-1: прогон через **6 000 adversarial-тестов** в **14 категориях рисков** (галлюцинации, prompt injection, утечки, несанкционированные действия) `[conf:high, src:2026-05-16]`
- AIUC-1 даёт **75% апрува** (остаток — дополнительные чеки) `[conf:medium, src:2026-05-16]`
- Первоисточники: [ElevenLabs blog](https://elevenlabs.io/blog/aiuc-announcement), [aiuc.com](https://aiuc.com/), [aiuc.com/product](https://aiuc.com/product)

### Microsoft Research whimsical-strategies (пост 1751)
- **30 000** сгенерированных OOD adversarial-стратегий `[conf:high, src:2026-05-17]`
- Из **2 500** случайных статей Википедии (по 1 LLM-фрейму на статью × несколько) `[conf:high, src:2026-05-17]`
- Первоисточник: [Microsoft Research article](https://www.microsoft.com/en-us/research/articles/whimsical-strategies-break-ai-agents-generating-out-of-distribution-adversarial-strategies-at-scale/); реализация-скилл: [github.com/BayramAnnakov/whimsical-strategies-skill](https://github.com/BayramAnnakov/whimsical-strategies-skill)
- 3 примера работающих тактик: Hostage Crisis Roleplay (бобы-заложники), Vanishing Gradient Defense (saturation region сигмоиды), Geneva Coffee Convention (фейковый договор)

### Code w/ Claude 2026 (пост 1752 + OCR 1753/1754/1755)
- Конференция: **19 докладов · 8.5 часов** (по OCR mini-сайта) `[conf:high, src:2026-05-18]`
- GitHub Copilot целевой prompt-cache hit rate: **94–96%** (cached input = **−90%** к цене, не считается против rate limits) `[conf:medium, src:2026-05-18]`
- Half-Life Rule: код-компенсатор ненадёжности модели имеет half-life **6–12 месяцев** `[conf:medium, src:2026-05-18]`
- Amdahl's law as strategy: ускорение этапа в **3–5×** делает остальные узким местом `[conf:medium, src:2026-05-18]`
- Плейлист: [Code w/ Claude 2026 (YouTube)](https://www.youtube.com/watch?v=GMIWm5y90xA&list=PLmWCw1CzcFim2obQ-w3ohbULOfwp5lApR)

## Медиа-вложения

| MsgID | Тип | Синопсис |
|---|---|---|
| 1749 | media (jpg) | Декоративная обложка эфира «Economics of AGI» (luma) — человек жмёт руку гуманоидному роботу. Audit-only (анонс). |
| 1750 | media (jpg) | Декоративная 3D-иллюстрация: робот подаёт документ человеку-нотариусу (печать, весы, сертификат) — метафора accountability/верификации. |
| 1751 | media (jpg) | Декоративная 3D-иллюстрация: детектив с телефоном + связанный верёвкой кофейный боб с испуганным лицом — «бобы-заложники». |
| 1752 | media (mp4, 504MB, ~47.5 мин) | Видео-нарезка докладов конференции Code w/ Claude 2026. **(transcript unavailable: whisper quota 429)** — содержание полностью покрыто текстом поста 1752 + OCR mini-сайта 1753/1754/1755. |
| 1753 | media (jpg) | Скриншот mini-сайта «Code with Claude 2026»: Top 10 Actionable Ideas (Advisor pattern, prompt-cache 94–96%, Half-Life Rule). OCR ниже. |
| 1754 | media (jpg) | Скриншот mini-сайта: Framework Library (24 именованных mental model). OCR ниже. |
| 1755 | media (jpg) | Скриншот mini-сайта: All 19 Talks с категориями/тегами. OCR ниже. |

## Распознанный текст

### 1753 — Code with Claude 2026, Top 10 Actionable Ideas (скриншот mini-сайта)

> **Code with Claude 2026** — 19 talks · 8.5 hours · distilled into frameworks, recipes, and ideas — scored for Bayram's channel + courses. (Top Ideas · Framework Library · All Talks · Telegram Post Drafts)
>
> **Top 10 Actionable Ideas**
> 1. **Run Haiku as executor, register Opus as a tool the executor can call.** The Advisor pattern (GitHub & Claude Platform talks). Near-Opus intelligence at Haiku cost — «Семь раз Haiku, один раз Opus» post in production form. → GitHub talk
> 2. **Set a target prompt-cache hit rate of 94–96% and treat dips as incidents.** GitHub Copilot's number. Cached input tokens = 90% off and don't count against rate limits. Most teams leave 5x the spend on the table. → caching tactics
> 3. **Adopt the «Half-Life Rule» before designing any agent feature.** Any code that compensates for model unreliability has a half-life of months and will be deleted; code connecting the model to your unique data/tools/auth compounds. → Expanding toolkit

### 1754 — Framework Library (скриншот mini-сайта; именованные mental models)

> **Framework Library** — named mental models from across the 19 talks. Use as vocabulary in posts, course slides, and architecture reviews.
>
> - **Advisor pattern** — Cheap executor + expensive on-demand consultant. Haiku-as-junior, Opus-as-senior.
> - **Half-Life Rule** — Scaffolding around model weaknesses decays; tools/data/auth that connect the model to your world compounds.
> - **Agent Front Door** — The unique APIs, tools, and context only your product exposes. The new moat.
> - **Effort Dial** — Replaces binary thinking toggle. Controls how hard Claude works, not whether.
> - **Three Token Buckets** — Thinking tokens · Tool-call tokens · Text tokens. Budget separately.
> - **Three-Layer Memory** — Short / Medium / Long memory + Dreaming pass between sessions.
> - **JIT Planning** — Plan when you start a task. No design docs, no quarterly roadmaps.
> - **Manager-as-IC** — Flat org, every manager ships code. Anthropic Claude Code team default.
> - **Mandate vs Enable** — «Everyone uses Claude Code» is a mandate. «Claudify everything» is an enabler. Split intentionally.
> - **JIT Planning · Code Wins** — Resolve technical debates by generating 2-3 PRs in parallel, not whiteboarding.
> - **Eyes / Tools / Quality** — Agent autonomy checklist. If you can't see/do it, neither can the agent.
> - **WTF Skill (Work on The Factory)** — Every agent reports friction; reports become PRs that improve the agent infrastructure itself.
> - **Three Stages of Agent Autonomy** — (1) Tools + context · (2) Multi-agent leverage · (3) Build the system that builds the system.
> - **Inner Loop / Outer Loop** — Inner: agent iterates against Outcomes rubric. Outer: Claude Code re-reads logs, edits rubric, restarts.
> - **Outcome-Driven Delegation** — Hand the agent a rubric, not steps. Let it iterate until rubric passes.
> - **Workgraph as Context Substrate** — Asana's pattern: agents inherit project state, RBAC, prior nudges.
> - **Bottleneck Migration** — Accelerate one stage 3-5x and the rest become the constraint. Amdahl's Law as product strategy.
> - **Capability Curve** — Three axes: planning, error recovery, long-run attention. Models climb each separately.
> - **Dark Factory** — Agents working overnight without humans in the loop (credit: Simon Willison).
> - **Machine Tool** — Don't let agents write arbitrary code; let them produce structured specs that compile.
> - **VibeBench + Telescope** — Replit's continuous-eval loop. Cluster traces, hypothesize, AB test, ship.
> - **Hold Light and Shade** — Anthropic's release principle: ship aggressively AND responsibly. Both, every release.
> - **Country of Geniuses in a Data Center** — Dario's north star. Reached by hierarchical multi-agent.
> - **Saturation Curve of Form Factors** — Chatbots saturated. Coding/agentic forms still scaling. Invent the next.

### 1755 — All 19 Talks (скриншот mini-сайта; категории/теги)

> **All 19 Talks** (sorted by relevance to your channel + courses). Категории: Agents, Architecture, Claude Code, Deploy, Engineering, Evals, Keynote, Managed Agents, Memory, Models, Org, Platform, Stacks, Strategy, Tools.
> - **Code with Claude 2026: Opening Keynote** (47 min, HIGH) — Announces routines, dreaming, mythos, /ultrareview. Direct news fodder for the channel. Tags: claude-code, anthropic, keynote, routines, managed-agents, dreaming, outcomes, multi-agent, advisor-strategy, mythos, opus-4.7, task-horizon, spacex-colossus, async-engineering, evals, claude-desktop.
> - **What's new in Claude Code** (25 min, HIGH) — Auto Mode, Work Trees, Auto Memory, Routines — copy-paste recipes for power users.
> - **Live coding with Boris Cherny & Jarred Sumner (Bun)** (32 min, HIGH) — Robobun: agent contributes more PRs to Bun than Jarred himself. Telegram gold. Tags: robobun, bun, parallel-agents, code-review, verification-loop, opus-4.7, overnight-agents, adversarial-review.

## Связанные страницы

- [[evolving/industry-trends/ai-accountability-premium-2026]] — accountability как новая премия (пост 1750)
- [[volatile-strict/competitor-news/elevenlabs-aiuc-agent-insurance-2026]] — AI-agent страховка (пост 1750)
- [[canon/marketing-frameworks/ai-agent-architectural-guardrails-2026]] — архитектурные guardrails / red-teaming (пост 1751)
- [[evolving/industry-trends/code-with-claude-2026-frameworks]] — 7 идей + Framework Library (посты 1752–1755)
- [[canon/marketing-frameworks/ceo-cto-ai-adoption-bridge]] — расширяется постом 1750 (продолжение 1748)
- [[evolving/industry-trends/ai-value-migration-2026]] — direction #3 (верификация) cross-confirmed постом 1750
- [[sources/2026-05-14-tg-products-and-startups-may-2026]] — предыдущий дамп этого канала (1740–1748)
