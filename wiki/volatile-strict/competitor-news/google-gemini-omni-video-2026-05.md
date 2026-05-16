---
id: mkt:volatile-strict/competitor-news/google-gemini-omni-video-2026-05
title: "Google тестит Gemini Omni — конец Veo как отдельной линейки (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [google, gemini, veo, video-generation, multimodal, ai-platform-wars]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-ai-newz-may-2026.md]
namespace: mkt
---

# Google тестит Gemini Omni — конец Veo как отдельной линейки (май 2026)

**Дата сигнала:** 2026-05-11 (пост 4564 в [[sources/2026-05-14-tg-ai-newz-may-2026|@ai_newz]]) `[conf:medium, src:2026-05-11]`.

## Что произошло

Согласно пересказу `@ai_newz`, Google тестирует **Gemini Omni** — апдейт основной модели Gemini, который добавляет **видеогенерацию** к уже существующим выходам (текст, изображения, аудио) `[conf:medium, src:2026-05-11]`. Источник: leak/insider-watch, не официальный анонс.

**Структурное следствие:** **линейке Veo как отдельной линейке моделей пришёл конец** `[conf:medium, src:2026-05-11]`. Veo консолидируется внутрь Gemini.

**Ожидаемая презентация:** на **Google I/O** (предполагаемо в следующую неделю после поста, то есть конец мая 2026) `[conf:medium, src:2026-05-11]`.

## Контекст — unified multimodal foundation

До Gemini Omni у Google была мульти-линейка `[conf:high, src:2026-04-06]`:

- **Gemini** — основной LLM (текст, картинки, аудио на выход)
- **Veo** — отдельная видео-модель (Veo 3.1 Lite, Veo 3.1 Fast — см. [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|model releases timeline]])
- **Lyria** — отдельная аудио-модель (Lyria 3 Pro)

Логика консолидации `@ai_newz` `[conf:medium, src:2026-05-11]`: Gemini уже может выдавать **аудио** и **картинки** как выходные модальности, добавление **видео** — финальный шаг unified multimodal foundation. После этого Veo как самостоятельный продукт теряет смысл — пользователь получает единый запрос «сгенерируй видео» внутри Gemini.

## Стратегические импликации

### 1. End of multi-product-line strategy у Google

Это **противоположная стратегия OpenAI и Anthropic**, которые держат раздельные продукты `[conf:high, src:2026-04-26]`:

- OpenAI: GPT-5.5 (LLM) vs Sora 2 (видео) vs GPT Image 2 (картинки) vs Whisper (audio) — отдельные модели, отдельные API
- Anthropic: Claude (LLM) vs Claude Design (UI/презентации) — даже Claude Design это отдельный inference layer

Google делает **обратный bet**: одна модель — все модальности. Этот выбор предполагает, что **multimodal cross-attention внутри одной модели даёт качественный edge** vs специализированные модели.

### 2. End-state Web 4.0 multimodal interaction

Если bet работает, Gemini Omni задаёт **прецедент unified multimodal** для всей индустрии. OpenAI и Anthropic будут вынуждены реагировать либо подражанием (multi-modal monolith), либо двойным контр-нарративом «специализация даёт качество».

### 3. Compute-impact

Унифицированная модель = одна тренировка вместо трёх. Это **снимает дублирование compute** в сравнении с раздельной линейкой. Параллель с [[volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05|Anthropic compute crunch]] — Google решает ту же compute-задачу через архитектуру, а не через capex.

## Почему это важно для marketing-memory GRO

1. **Готовый hook про «свернуть стек».** Hook-формулировка: *«Через год вместо подписки на ChatGPT + Veo + Sora + Lyria — одна подписка на Gemini, и в ней всё. Бизнес-урок: если ваш продукт это конкуренция с одной фичей внутри гиганта — окно закрывается»*. Связь с [[evolving/industry-trends/software-moat-erosion-2026|эрозией moat]].
2. **Параллель «специализация vs unified» в любой категории.** Это reusable рамка для контента: *«Что лучше — vertical-инструмент или multimodal-комбайн?»* Прямая параллель с positioning GRO как **vertical product** (self-management для предпринимателей) против horizontal AI-комбайнов.
3. **I/O как анкер-событие.** Google I/O 2026 будет основным AI-новостным якорем в конце мая — стоит подготовить пакет постов **в день I/O** (Tier A в [[volatile/weekly-digest/ai-industry-news-w15-w18-2026]] обновить после факта).

## Связанные страницы

- [[sources/2026-05-14-tg-ai-newz-may-2026]] — первоисточник
- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — model releases timeline (Veo 3.1 Lite, Lyria 3 Pro контекст)
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — макро-нарратив гонки
- [[evolving/industry-trends/software-moat-erosion-2026]] — эрозия moat
- [[volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05]] — параллель compute crunch (Anthropic закрывает свою сторону)
- [[volatile-strict/competitor-news/anthropic-third-party-credits-2026-06]] — параллельный ход Anthropic в ecosystem-распределение

## Caveat

`@ai_newz` — vторичный пересказ leak/insider-watch, без официального источника. **Не использовать для пресс-цитат** до анонса на I/O. Это — early signal для tracking трендов, не canonical fact для публикации.
