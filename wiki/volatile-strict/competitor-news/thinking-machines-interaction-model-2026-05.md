---
id: mkt:volatile-strict/competitor-news/thinking-machines-interaction-model-2026-05
title: "Thinking Machines (Мира Мурати) — interaction model без external scaffolding (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [thinking-machines, murati, ai, voice, multimodal, interaction, sebrant]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-19  # +fourth-source @vcnews 61327 (12 мая): RU-mainstream фиксация первой ПУБЛИЧНОЙ демо TML-Interaction (с видео) — переход в product-rollout phase подтверждён. Prior: +third-source @cgevent (12 мая, пост 15664) архитектура + hard-числа 276B MoE/12B активных, FD-bench v1.5 77.8 vs 46-54, turn-taking 400мс. Prior: +second-source Edinorog 7944
sources: [sources/2026-05-14-tg-techsparks-may-2026.md, sources/2026-05-14-tg-theedinorog-may-2026.md, sources/2026-05-19-tg-cgevent-may08-19-2026.md, sources/2026-05-19-tg-vcnews-may-12-14-2026.md]
namespace: mkt
---

# Thinking Machines — interaction model без external scaffolding

**Дата сигнала:** 2026-05-13 (пост 5596 в [[sources/2026-05-14-tg-techsparks-may-2026|@techsparks]]) `[conf:medium, src:2026-05-13]`.

Команда **Миры Мурати** (Thinking Machines, основана ex-OpenAI-CTO в 2024) опубликовала технический пост [thinkingmachines.ai/blog/interaction-models/](https://thinkingmachines.ai/blog/interaction-models/) с описанием нового подхода к interactive AI-моделям.

## Что произошло

Thinking Machines обнародовали **interaction model** — модель, **с нуля спроектированную и обученную** для **реактивного multimodal-взаимодействия** с человеком, без необходимости внешнего scaffolding (Eleven Labs для голоса + ChatGPT-stack + дополнительные слои оркестрации).

**Цитата команды:**

> «Interactivity should scale alongside intelligence; the way we work with AI should not be treated as an afterthought.»

## Контекст — проблема external scaffolding

Себрант приводит **собственный кейс**: на конференции YAC/e команда Яндекса делала живой разговор людей с «Клаусом» (AI-помощник для студентов на семинарах). **«Намучились, чтобы всё было живо и быстро, безо всяких пауз»** `[conf:medium, src:2026-05-13]`. То есть **скорость реакции и multimodal-готовность** — реальная боль production-применений LLM в живом взаимодействии.

**Стандартный pipeline** до этого был:
1. ASR (Whisper / Eleven Labs / ...) — голос → текст
2. LLM (ChatGPT / Claude / ...) — текст → текст
3. TTS (Eleven Labs / Polly / ...) — текст → голос
4. Optional: vision module для видеоввода + custom оркестратор

Каждый слой добавляет latency. Каждое отдельное API — дополнительная стоимость и зависимость.

## Что обещает Thinking Machines

По их декларации `[conf:medium, src:2026-05-13]`:

- **С нуля обученная под interaction** (не post-hoc мультимодальный layer на LLM)
- **Действительно чутко реагирует на любое вмешательство** человека в процессе совместной работы
- **Мультимодальное вмешательство:** мгновенная реакция голосом на появление человека в кадре (если есть доступ к камере)
- **Реакция голосом по запросу** (не only текст)

Себрант: «**От демки по ссылке слюнки текут**, быстрей бы дали пощупать и вообще хорошо бы, чтоб такие интерфейсы поскорей стали всеобщей нормой».

## Стратегические импликации

### 1. Удар по middleware-economy

Если interaction-model выходит в production, это **угроза для middleware-vendors**:
- **Eleven Labs** — TTS-вендор, доход которого построен на bridge между LLM и voice
- **AssemblyAI / Deepgram** — ASR-вендоры
- **LangChain / LlamaIndex** — orchestration-слои

Параллель — [[volatile-strict/competitor-news/anthropic-claude-managed-agents-2026-04|Anthropic Managed Agents]]: frontier-провайдеры **поглощают функциональность ecosystem-vendors** внутрь basic offering, выдавливая ecosystem-players вверх по value-chain. Thinking Machines делает то же самое для voice/multimodal.

### 2. Новый игрок в гонке

[[evolving/industry-trends/ai-corporate-race-mar-may-2026|Гонка корпоративных AI-решений]] до сих пор была 6–7 капитал-узлов: OpenAI, Anthropic, xAI, Nebius, Tesla, Meta, Google. Thinking Machines с interaction-моделью может стать **8-м узлом**, **специализированным на UX-уровне**, не на frontier-моделях.

Это структурно отличается от других узлов:
- Не конкурирует с OpenAI/Anthropic на reasoning benchmark'ах
- Конкурирует на **«как ощущается работа с AI»**
- Может стать platform-of-choice для **enterprise voice/multimodal** use-cases (call centers, voice assistants, educational, healthcare)

### 3. Мира Мурати — verified founder

Мурати — ex-CTO OpenAI (до запуска Thinking Machines в 2024), верифицированный AI-founder. Этот сигнал — **первый крупный публичный technical milestone Thinking Machines** с момента основания. До этого компания делала **раунды без громких релизов** — теперь начинается **product-rollout phase**.

## Third-source attestation: @cgevent (12 мая) — архитектура и числа

[[sources/2026-05-19-tg-cgevent-may08-19-2026|@cgevent пост 15664 (12 мая 2026)]] добавляет **техническую конкретику**, которой не было в пересказах @techsparks/@theedinorog:

**Архитектура (как работает):**
- **Реалтайм микрокусочками по 200 мс**, где аудио + видео + текст идут **параллельными потоками** `[conf:medium, src:2026-05-12]`
- **Асинхронное мышление по ходу диалога**: длинные цепочки рассуждений, инструменты, поиск не блокируют основной поток
- **Фоновая модель** докидывает результаты в живой разговор в подходящий момент → задержка не-thinking модели + интеллект thinking модели
- Прямая формулировка проблемы: «пока ты говоришь — модель глухая; пока модель отвечает — она слепая» (текущие VAD+TTS+dialogue-logic подпорки)

**Конкретные новые возможности:**
- Перебивать пользователя, когда тот говорит чушь
- Говорить одновременно с тобой — синхронный перевод, лайв-комментарий
- Реагировать на визуальные триггеры: «скажи, когда подниму палец», «посчитай мои отжимания»
- Держать чувство времени: «напоминай дышать каждые 4 секунды»
- Вызывать инструменты и искать в вебе параллельно с разговором

**Hard-числа (self-reported бенчмарки):**
- **276B MoE / 12B активных** параметров `[conf:medium, src:2026-05-12]`
- **FD-bench v1.5** (качество интеракции): **77.8 vs 46–54** у GPT-Realtime и Gemini-Live `[conf:medium, src:2026-05-12]`
- **Turn-taking latency 400 мс** — лучшая в категории `[conf:medium, src:2026-05-12]`
- На новых бенчах проактивной речи (TimeSpeak, CueSpeak) и визуальных триггеров (RepCount, Charades) конкуренты дают «ноль или единицы процентов» `[conf:low, src:2026-05-12]`
- Research preview закрытый, доступ «в ближайшие месяцы»

**Релевантность визуальных триггеров для GRO:** возможности «посчитай отжимания» / «напоминай дышать каждые 4 секунды» — ровно тот тип проактивного wellness/coaching-присутствия, который GRO мог бы дать в голосовом интерфейсе. Tracking-релевантно для product-стороны.

## Fourth-source attestation: @vcnews (12 мая) — публичная демо, mainstream-RU фиксация

[[sources/2026-05-19-tg-vcnews-may-12-14-2026|@vcnews пост 61327 (12 мая 2026, с видео)]] переводит сигнал из «техпост/анонс» в **первую публичную демонстрацию** через RU-mainstream бизнес-медиа `[conf:medium, src:2026-05-12]`:

> «Стартап Thinking Machines Lab бывшего техдиректора OpenAI Миры Мурати **впервые показал** свою разработку **TML-Interaction**. Это "модель взаимодействия", которая должна приблизить общение с ИИ-моделями к человеческому. Нейросеть одновременно обрабатывает аудио и видео и "обдумывает" ответ, быстро реагирует на перебивания и **может перебить сама**, параллельно ищет в интернете и визуализирует данные.»

**Что это меняет:**
- **Подтверждение product-rollout phase.** Предыдущие источники (@techsparks, @theedinorog, @cgevent) описывали blog-пост / research-preview. vc.ru фиксирует **публичный показ** — компания вышла из «раунды без релизов» в публичную демонстрацию.
- **Mainstream-RU coverage.** До этого Thinking Machines был сигналом для AI-tracking-каналов; теперь попал в крупнейшее RU-бизнес-медиа — расширение awareness за пределы технической аудитории.
- **Reconcile названия.** vc.ru использует имя **TML-Interaction** для продукта (раньше в вики фигурировало просто «interaction model» по blog-посту thinkingmachines.ai). Использовать **TML-Interaction** как product-name.
- **Capabilities совпали** с @cgevent-описанием (перебивания, аудио+видео параллельно, параллельный поиск/визуализация) — четвёртый источник без противоречий усиливает confidence в фактуре, но остаётся medium (демо ≠ GA-доступ).

## Применимость для marketing-memory GRO

### Hook-возможности

1. **«Interactivity should scale alongside intelligence»** — готовая цитата Thinking Machines для **content про UX AI-инструментов**. Применима для GRO как продукта, у которого UX (timing, тон, ritual) — core differentiator, не optional layer.
2. **«AI как afterthought interaction — закончилось»** — формулировка для постов про **product-philosophy в AI-эпохе**. GRO имеет аналогичную позицию: ритуал постановки целей **не доделка** к AI, а первичная функциональность.
3. **«Бесшовное multimodal-AI приходит. Eleven Labs уже не панацея»** — для **tech-аудитории**, знакомой с middleware-стеком.

### Anti-pattern

- **Не использовать пока interaction model не вышла в публичный доступ** — пост 5596 — **анонс**, не release. Использовать как **future-tense сигнал**, не как «уже работает».
- **Не приписывать Thinking Machines конкретный feature**, не подтверждённый их blog'ом — Себрант пересказывает, наш пересказ Себранта — третий уровень. Для финального контента — **читать оригинал** на thinkingmachines.ai.

## Связь с другими страницами

- [[sources/2026-05-14-tg-techsparks-may-2026]] — первоисточник пересказа
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — макро-гонка, в которой Thinking Machines может стать 8-м узлом
- [[evolving/content-trends/sebrant-cognitive-exoskeleton-hooks]] — Hook 1 (когнитивный экзоскелет) — родственная рамка про AI-teammate; interaction model = операционная реализация
- [[canon/marketing-frameworks/anthropic-constitutional-reasoning-paper-2026]] — параллельный technical milestone в AI-design
- [[volatile-strict/competitor-news/anthropic-claude-managed-agents-2026-04]] — структурная параллель (frontier-vendor поглощает middleware)
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] — Google делает аналогичный bet через unified multimodal
- [[canon/positioning/gro-value-proposition]] — UX как core differentiator (параллель Thinking Machines product-philosophy)

## Источник

- [[sources/2026-05-14-tg-techsparks-may-2026]] — пост 5596 (13 мая 2026, 18:12 UTC)
- Оригинал поста Thinking Machines: [thinkingmachines.ai/blog/interaction-models/](https://thinkingmachines.ai/blog/interaction-models/)

## Caveat

`@techsparks` — vторичный пересказ blog-поста. **Не использовать для пресс-цитат** без чтения оригинала. Это — **operational signal для tracking трендов**, не canonical fact для публикации. Confidence: medium. При подготовке финального контента — проверить, что Thinking Machines не изменил формулировки или not рассинхронизировался с маркетинговой документацией.
