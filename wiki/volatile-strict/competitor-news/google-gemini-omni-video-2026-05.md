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
updated: 2026-05-30  # +8-th source @neuraldvig (10783 lego-ремикс первого фильма про поезд + маппеты; 10796 перевод видео на другой язык с липсинком и адаптацией лица) — RU-meme-демки capability «translation + lip-sync + face-adaptation», корроборация dubbing-функции. Prior: +7-th source @techno_yandex 5271 (технодайджест недели, 2026-05-24) — RU научпоп-пересказ: «семейство Gemini Omni; первая, Omni Flash, умеет генерировать видео по запросам с текстом, картинками, видео и аудио одновременно». Подтверждает unified-multimodal формулировку для широкой RU-аудитории. Prior: +6-th source @solokumi (Кумар Виас, пост 419 от 2026-05-22) — маркетинговый ракурс reuse-first: 5 use-case промптов + prompt-формула. Рекомендация маркетологам — НЕ генерировать с нуля, а пересобирать существующий контент. Подробный operational playbook см. [[evolving/content-trends/gemini-omni-marketer-playbook-2026]]. Prior: +5-th source @cgevent (15707-15722, 15735, 15743) — детальный capability-разбор Цыпцына, vision-confirmed pricing в Google Flow, Avatar/Cameo механика 3D-фотограмметрии лица.
sources: [sources/2026-05-14-tg-ai-newz-may-2026.md, sources/2026-05-19-tg-cgevent-may08-19-2026.md, sources/2026-05-26-tg-boris-again-may-19-24-2026.md, sources/2026-05-26-tg-neuraldvig-may-19-22-2026.md, sources/2026-05-26-tg-cgevent-may19-25-2026.md, sources/2026-05-26-tg-solokumi-may-20-22-2026.md, sources/2026-05-26-tg-techno-yandex-may-20-25-2026.md, sources/2026-05-30-tg-neuraldvig-may-22-30-2026.md]
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
- [[sources/2026-05-26-tg-neuraldvig-may-19-22-2026]] — **4-th source attest** (10740-10750 в день I/O + 10758 post-launch observation): добавляет описания I/O-фич + умные очки + Google Pics + Multi-agent search
- [[sources/2026-05-26-tg-cgevent-may19-25-2026]] — **5-th source attest** (15707-15722, 15735, 15743): детальный capability-разбор Цыпцына, 5 длинных постов с тестами + vision-confirmed pricing в Google Flow + Avatar/Cameo механика 3D-фотограмметрии лица + плановая video-референс-фича
- [[sources/2026-05-26-tg-solokumi-may-20-22-2026]] — **6-th source attest** (Кумар Виас @solokumi пост 419, 2026-05-22): **маркетинговый ракурс** — позиционирование Omni как **видеоредактора, а не очередного генератора** + 5 готовых use-case промптов для маркетинга + **prompt-формула** (`Use this as the base / Keep / Change / Add / Output as / Do not add`) + рекомендация reuse > generate
- [[sources/2026-05-26-tg-techno-yandex-may-20-25-2026]] — **7-th source attest** (технодайджест 5271, 2026-05-24): RU научпоп-формулировка для широкой аудитории — «семейство Gemini Omni; первая, Omni Flash, умеет генерировать видео по запросам с текстом, картинками, видео и аудио одновременно» (mainstream-перевод unified-multimodal тезиса)
- [[sources/2026-05-30-tg-neuraldvig-may-22-30-2026]] — **8-th source attest** (10783, 10796): meme-демки capability'ей — lego/маппет-ремикс первого в истории фильма про поезд (multimodal layering на реальном архивном видео) + **перевод видео на другой язык с липсинком и адаптацией лица актрисы** (`@neuraldvig`: «нейронка подтягивает липсинк и даже может адаптировать лицо»). Корроборирует dubbing/translation-функцию `[conf:low, src:2026-05-26]` — meme-канал, не первоисточник. Параллель с **ElevenLabs Dubbing 2** (10811 в том же дампе — улучшенное сохранение эмоций/тембра/голоса при переводе, ср. [[evolving/content-trends/ai-video-tools-stack-2026]]): video-translation/dubbing сегмент обостряется с двух сторон.
- [[evolving/content-trends/gemini-omni-marketer-playbook-2026]] — operational playbook для маркетинга, синтезирующий маркетинговый ракурс Кумара Виаса
- [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]] — parallel I/O анонс (Gemini 3.5 Flash + Spark)
- [[volatile-strict/competitor-news/runway-aleph-2-video-2026-05]] — Runway ответ через 2 дня (frame-edit propagation)
- [[volatile-strict/competitor-news/capcut-gemini-partnership-2026-05]] — CapCut партнёрство через 2 дня

## Capability-разбор от @cgevent (детально)

5-th attest [[sources/2026-05-26-tg-cgevent-may19-25-2026|@cgevent дамп 19-25 мая]] добавляет детализацию по capability'ям Omni Flash через серию из 5 длинных постов Цыпцына:

### Генерация (пост 15710)
По сравнению с Seedance: **«вялая динамика и физика»**, **«переключения камеры своеобразны»**, общее впечатление **«заторможенно и искусственно»** `[conf:medium, src:2026-05-20]`. 10-секундное ограничение — пока узкое место для динамичных сцен.

### Редактирование (посты 15711-15714)
**«Совершенно огненное»** `[conf:medium, src:2026-05-20]`. Ключевые наблюдения:
- Можно **загружать свои видео**, не только генерации
- Пример промпта `«Make everyone in this shot flamingos. Wearing the same outfit.»` — работает
- Пример от [fofr](https://x.com/fofrAI): «сделай её невидимой, надень перчатки», «когда она говорит, подходят двое мужчин и уносят фотографию в рамке», «поменяй её одежду»
- Работает на **реальном youtube-видео** (Цыпцын редактировал Gemini Omni Release Notes видео)
- **Понимание происходящего в кадре «потрясающее»** — точка дифференциации vs prompt-only генераторов

### World Knowledge (пост 15713, 15743)
Omni **тащит весь LLM-контекст Gemini** `[conf:medium, src:2026-05-20]`. Импликации:
- **Не нужны детальные промпты** — модель строит детали из понимания мира
- Главное применение — **образование, иллюстрация, презентации**: достаточно сформулировать концепцию ролика, Omni сама находит теорию, описания объектов, визуализирует с текстом
- Цыпцын: **«Режиссура образовательных роликов — это сторителлинг другого рода. Драки и погони не нужны. Нужны концепции.»**

### Avatar/Cameo (посты 15716-15717, 15722)
Omni принимает фото человека → встраивает в видео `[conf:medium, src:2026-05-20]`:
- Цыпцын взял свою старую фотку с CG EVENT 2015 → промпт «жидкий терминатор» → «скушал и не поперхнулся»
- **Технология под капотом:** «модель строит что-то типа 3D-модели (как при фотограмметрии), чтобы сохранять консистентность при повороте головы»
- **Practical-tip:** «Больше фоток на входе — лучше». Чем больше ракурсов, тем точнее 3D-реконструкция
- **Caveat:** детали скачут (очки пропадают, борода меняется) — особенно на нестандартных формах
- **Будущая фича:** video-референс лица (ставите камеру → крутите лицом как при KYC → модель строит лицевую модель). По наблюдению Цыпцына — *«HeyGen поперхнулся»* (прямая конкуренция с digital-avatar-стартапами)

### What's Next (пост 15722)
По подкасту `Introducing Gemini Omni`:
- **Длительность будет увеличена** — несколько раз звучала **цифра 30 сек** как ориентир
- **Уже сейчас можно продолжать клипы** — Omni держит в памяти полный референс, должна попадать в консистентность
- **Больше tooling-а** — инструменты, унаследованные от Gemini (поиск в интернете, работа с данными — как в Nanobanana 2)
- **Цифровая копия пользователя** — KYC-style face+voice scan → ваш аватар → используется в генерациях
- Tools для **сторителлинга** — будут развивать Flow в этом направлении (Цыпцын: но что с интерфейсом Flow при появлении CapCut в Gemini App?)

### Pipeline-prescription Цыпцына

Главный вывод [[sources/2026-05-26-tg-cgevent-may19-25-2026|@cgevent]]: **«генерация в Сиденс, редактирование в Омни»** `[conf:medium, src:2026-05-20]`. То есть Omni не вытесняет Seedance, а образует с ней **двухступенчатый pipeline:**

1. **Stage 1 (Seedance 2.0):** генерация базовой сцены — лучшая динамика, физика, скорость
2. **Stage 2 (Gemini Omni):** правки и кросс-сцены — лучшее понимание мира + редактирование

**Минус pipeline'a:** «дороговато получается». Две подписки (Sora-конкурент + Google Flow Pro) суммарно $50-80/мес для серьёзного контент-production.

## Vision-confirmed pricing в Google Flow

Скриншот UI приложения Google Flow (15708, vision-confirmed) показывает три варианта в выборе модели:
- **Omni Flash** — **30 credits / video** (отмечен как «selected» в скриншоте) `[conf:high, src:2026-05-20]`
- **Veo 3.1 Lite** — 10 credits / video `[conf:high, src:2026-05-20]`
- **Veo 3.1 Fast** — 20 credits / video `[conf:high, src:2026-05-20]`

**Расчёт ROI на плане Google Pro** (1000 кредитов/мес):
- Omni Flash: **33 видео/месяц** (10 сек каждое) `[conf:high, src:2026-05-20]`
- Veo 3.1 Quality (если был бы доступен в Flow): **100 кр/видео = 10 видео/мес** `[conf:high, src:2026-05-20]` — по умолчанию через AI Plus

Для сравнения с конкурентами: на тех же $20/мес AI Plus (≈Google Pro) **Sora 2 даёт 25-30 видео/мес** `[conf:medium, src:2026-04-26]`; **Seedance 2.0 @ $0.03/сек = ~$0.18/видео = ~110 видео за $20** (см. [[evolving/content-trends/ai-video-tools-stack-2026]]). То есть **Seedance остаётся бюджетным выбором даже после Omni** — Google не атакует ценовой сегмент.

## Маркетинговый ракурс — Кумар Виас (6-th source, 22 мая)

Роман Кумар Виас ([[sources/2026-05-26-tg-solokumi-may-20-22-2026|@solokumi пост 419]], 2026-05-22) даёт **первый практический ракурс с прицелом на маркетолога**, ортогональный capability-разбору Цыпцына (который смотрит из CG-производства):

**Главный фрейм:** Omni — это **не видеогенератор**, а **видеоредактор**. Кумар Виас рекомендует маркетологам **тестировать не генерацию с нуля, а пересборку существующих ассетов** (фото продукта, горизонтальные ролики, скриншоты UI, маршруты, фото founder'а):

> «Маркетосам нужно первым делом тестировать не генерацию с нуля, а реюзать старые фото продукта и горизонтальные ролики. Omni интересен не как десятый генератор слоповых видосов, а как **флоу переработки того, что уже есть**. Для статичных креосов **ресайз и адаптация — это вообще один из главных юзкейсов AI**.»

**Что Кумар Виас вынес в публичные actionable** (см. [[evolving/content-trends/gemini-omni-marketer-playbook-2026|operational playbook]]):

1. **5 use-case промптов** для маркетинга — публично цитируемые рекомендации:
   - Шортс из 8-10 случайных фото галереи за минуту
   - 5 вариантов рекламы из одного фото продукта
   - Старый горизонтальный ролик → вертикальный Shorts
   - Скрин Google Maps маршрута → travel POV видео
   - AI-аватар себя в студийной интро-сцене (фреймит как **killing-feature**, обещает тестирование на Refocus)

2. **Prompt-формула** — операционный handbook:
   ```
   Use this as the base [вводные] → Keep [что нельзя менять] → Change [что нужно менять] → Add [стиль/движение] → Output as [формат] → Do not add [что не нужно]
   ```
   Формула содержит **4 defensive слота** (Keep / Do not add задают anti-hallucination guards) и **2 generative слота** (Change / Add). Подробный разбор формулы — в [[evolving/content-trends/gemini-omni-marketer-playbook-2026]].

3. **Доступ stack** для маркетинга:
   - **Gemini app** — быстрые правки в чате (A/B тесты креативов)
   - **Google Flow** — полноценный продакшн (бренд-ролики, multi-shot)
   - **YouTube Shorts** — публикация одной кнопкой

**Дифференциация от cgevent-ракурса:** Цыпцын оценивает Omni через CG-производственные критерии (физика, ракурсы камеры, Avatar/Cameo для character-driven контента) и приходит к выводу «pipeline Seedance + Omni». Кумар Виас оценивает через **маркетинговое ROI** (CPM креатива, скорость A/B-тестов, переработка mertвого backlog'а ассетов) и приходит к выводу **«Omni как self-sufficient tool для reuse-сценария»** — без Seedance, без двойной подписки. Это два legitимных use-case с разными economic-показателями.
