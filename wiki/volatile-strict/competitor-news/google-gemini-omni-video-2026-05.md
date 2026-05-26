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
updated: 2026-05-26  # +third-source attest @boris_again (пост 3914 от 2026-05-20): official I/O announcement превратил leak в подтверждённое событие; +pricing AI Plus $20/мес, AI Ultra $100/мес, Vertex AI «в ближайшие недели», SynthID watermark, C2PA Content Credentials, AI Content Detection API — confidence поднята с medium до high
sources: [sources/2026-05-14-tg-ai-newz-may-2026.md, sources/2026-05-19-tg-cgevent-may08-19-2026.md, sources/2026-05-26-tg-boris-again-may-19-24-2026.md]
namespace: mkt
---

# Google Gemini Omni — официальный анонс на Google I/O (май 2026)

**Дата leak'а:** 2026-05-11 (пост 4564 в [[sources/2026-05-14-tg-ai-newz-may-2026|@ai_newz]]) `[conf:medium, src:2026-05-11]`.
**Дата официального анонса:** 2026-05-20 (Google I/O 2026, [boris_again пост 3914](https://t.me/boris_again/3914)) — leak подтверждён, переведён в `[conf:high, src:2026-05-20]`.

## Что произошло

Согласно пересказу `@ai_newz`, Google тестирует **Gemini Omni** — апдейт основной модели Gemini, который добавляет **видеогенерацию** к уже существующим выходам (текст, изображения, аудио) `[conf:high, src:2026-05-20]`. <!-- superseded 2026-05-26 by [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] : confidence medium → high, источник leak → официальный анонс на I/O -->

**Структурное следствие:** **линейке Veo как отдельной линейке моделей пришёл конец** `[conf:high, src:2026-05-20]`. Veo консолидируется внутрь Gemini.

**Дата официальной презентации:** **2026-05-20 на Google I/O 2026** `[conf:high, src:2026-05-20]` (leak от 11 мая прогноз подтвердился — окно «в следующую неделю» точно совпало).

## Официальный анонс — что добавил I/O

Прямая цитата из поста [@boris_again 3914](https://t.me/boris_again/3914) (2026-05-20 10:37 UTC):

> «Google собрал весь мультимодальный стек в одну модель: текст, изображение, аудио, видео на вход — видео на выход. Первая модель семейства, **Gemini Omni Flash**, уже доступна подписчикам.»

**Pricing:**
- **AI Plus** — от **$20/мес** `[conf:high, src:2026-05-20]`
- **AI Ultra** — от **$100/мес** с приоритетом `[conf:high, src:2026-05-20]`
- **Vertex AI API** — «в ближайшие недели» `[conf:high, src:2026-05-20]`
- **SLA:** нет (на момент анонса) `[conf:high, src:2026-05-20]`

**Безопасность и provenance:**
- Каждый сгенерированный ролик маркируется **невидимым водяным знаком SynthID** `[conf:high, src:2026-05-20]`
- Google расширяет **C2PA Content Credentials** `[conf:high, src:2026-05-20]`
- Запускается **AI Content Detection API** для распознавания сгенерированного контента `[conf:high, src:2026-05-20]`

**Капабилити:**
- Multimodal layering — каждая инструкция наслаивается на предыдущую («замени скульптуру на мыльные пузыри», «когда рука касается зеркала — зеркало плывёт») `[conf:high, src:2026-05-20]`
- Модель **помнит контекст и сохраняет персонажей сквозь правки** `[conf:high, src:2026-05-20]`
- Физика улучшена: **гравитация, кинетика, динамика жидкости** `[conf:high, src:2026-05-20]`

## Second-source attestation: @cgevent (11–12 мая)

[[sources/2026-05-19-tg-cgevent-may08-19-2026|@cgevent]] независимо подтверждает сигнал (посты 15656/15661/15662, 11–12 мая):

- У части пользователей приложения Gemini появилось приглашение **«Meet our new video model. Remix your videos, edit directly in chat, try a template, and more»** `[conf:medium, src:2026-05-11]`
- На Reddit: качество следования промпту отличное, генерация звука «улучшена в разы» `[conf:low, src:2026-05-11]`
- Контекстное окно **>12 млн токенов**, агентные рабочие процессы (модель сама выбирает формат/модель под задачу) `[conf:low, src:2026-05-11]`
- Прямое сравнение с Seedance (пост 15662): на одном промпте в **математике и тексте Gemini Omni «явно получше»** (наследие Flash + Nanobanana), в остальном нужны расширенные тесты `[conf:medium, src:2026-05-12]`
- **Сильно цензурирована** — Will Smith не пропускает (генерит только обобщённого «mature African-American man») `[conf:medium, src:2026-05-11]`
- Google пересматривает систему лимитов токенов (вкладка usage limits) — новая модель «жрёт токены ещё интенсивнее»

Это укрепляет confidence сигнала с одного второисточника (@ai_newz) до **двух независимых** — но оба остаются leak/insider-watch до официального анонса на I/O.

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

## Caveat (исторический — пред-анонсный период)

<!-- superseded 2026-05-26 by [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] : leak подтверждён на I/O, caveat больше не релевантен. Сохранено как audit trail. -->

(До 20 мая 2026) `@ai_newz` — вторичный пересказ leak/insider-watch, без официального источника. **Не использовать для пресс-цитат** до анонса на I/O. Это — early signal для tracking трендов, не canonical fact для публикации.

**После 20 мая 2026:** официальный Google анонс на I/O, факт canonical, можно цитировать.

## Contradictions

- **[2026-05-26]** Конфликт между `confidence: medium` (leak от 11 мая) и `confidence: high` (официальный анонс 20 мая) разрешён в пользу свежего/первичного. Старая формулировка обёрнута в HTML-комментарий, новая стала visible. Источник: [[sources/2026-05-26-tg-boris-again-may-19-24-2026]].

## Связанные страницы (обновлено)

- [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — official-anouncement source (boris_again пост 3914)
- [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]] — parallel I/O анонс (Gemini 3.5 Flash + Spark)
