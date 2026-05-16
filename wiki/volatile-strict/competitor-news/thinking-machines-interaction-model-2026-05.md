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
updated: 2026-05-14  # +second-source attest Edinorog 7944 (vc.ru 12 мая) — TML-Interaction наименование уточнено, Мурати единственная из 5 cofounders осталась после февраля 2026
sources: [sources/2026-05-14-tg-techsparks-may-2026.md, sources/2026-05-14-tg-theedinorog-may-2026.md]
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
