---
id: mkt:evolving/content-trends/ai-video-tools-stack-2026
title: "AI video generation tools stack — апрель 2026"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [creative, video, ai, tools, seedance, runway, higgsfield, veo3, sora, kling]
confidence: high
stale: false
created: 2026-04-14
updated: 2026-05-19  # +cgevent дамп 8-19 мая: HiDream-O1 (=Peanut раскрыт, vivago.ai, 8B pixel-space no-VAE), Krea K-2 (всем + безлимит неделю), AsymFLUX.2 Klein (+40% скорости pixel-space), Starchild-1 (Odyssey world model realtime 20FPS), HY-World-2.0/Pixal3D (Tencent опенсорс), Viggle P.I.N.O.C (нейромокап), Video2Video нейрорендер, LTX Director (Comfy timeline). Peanut раскрыт → теперь HiDream-O1. Prior: +cross-link на RU-parallel snapshot
sources: [sources/2026-04-14-tg-solokumi-nov2025-apr2026.md, sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026.md, sources/2026-05-14-tg-cgevent-may05-08-2026.md, sources/2026-05-19-pressfeed-ai-tools-for-online-courses-15.md, sources/2026-05-19-tg-cgevent-may08-19-2026.md]
namespace: mkt
---

# AI video generation tools — стек начала 2026

Дрейфующий снимок набора моделей, используемых для AI-production видеокреативов на апрель 2026. Это evolving-страница: сами модели сменяются каждые 2–4 месяца, позиции в рейтингах смещаются. TTL soft 180 дней, дата проверки пересечения с новыми исследованиями — каждые 2 месяца.

Стек описан с позиции маркетолога-практика, который оценивает инструменты по: качеству финального видео, стоимости за секунду, скорости генерации, способности держать консистентного персонажа, жёсткости цензуры. Источник: Р. Кумар Виас / Kumar & Solo, [[sources/2026-04-14-tg-solokumi-nov2025-apr2026|@solokumi]], посты 349, 354, 379, 382, 387, 390, 392.

Каноническая **механика** производства (как этими инструментами пользоваться в 5-этапном pipeline) — в [[canon/marketing-frameworks/ai-video-production-pipeline]]. Здесь — только дрейфующая часть «какая модель что умеет прямо сейчас».

## Основные модели (апрель 2026)

### Seedance 2.0

- **Стоимость:** ~$0.03 за секунду видео — **в 9× дешевле Runway** по оценке @solokumi (пост 392, 2026-04-03)
- **Суперсила:** **@-система** — загрузка до 12 референсных файлов с ролями. Примеры ролей: `@Image1` — лицо персонажа, `@Image2` — стиль освещения, `@Video1` — характер движения камеры, `@Audio1` — ритм и темп. Модель держит всё одновременно и собирает видео, в котором персонаж не мутирует, свет не скачет, динамика синхронизирована с музыкой.
- **По многим рейтингам — #1 среди видеомоделей на начало 2026**, опережает Sora 2 и Veo 3 (по оценке @solokumi, независимо не подтверждено)
- **Минусы:**
  - Генерация занимает до ~30 минут на видео (изматывает при массовом производстве)
  - Цензура — жёсткая, экспрессия и нестандартные углы ловят бан аккаунта
- **Key trick:** `[cut]` в промпте — можно писать **один промпт с несколькими сценами через `[cut]`**, модель сама делает монтаж. Недооценённая функция: одна генерация = готовая мини-история
- **Гайд по @-системе:** [magichour.ai/blog/how-to-use-seedance-20](https://magichour.ai/blog/how-to-use-seedance-20)
- **Репозиторий 500+ промптов и результатов:** [github.com/YouMind-OpenLab/awesome-seedance-2-prompts](https://github.com/YouMind-OpenLab/awesome-seedance-2-prompts)

### Runway Gen-4.5

- **Стоимость:** ~в 9× дороже Seedance. В 2026 цена на промпте Kumar & Solo — не основной минус, ключевой минус — ограничение входа
- **Суперсила:** **лучший кинематографический язык**. Понимает термины оператора: dolly zoom, orbit shot, pedestal up, tracking shot, crane up. Одно изображение + описание движения камеры → киношная картинка с детализацией
- **Скорость:** **менее 6 минут на клип** (в 5 раз быстрее Seedance при массовом производстве)
- **Цензура:** мягче, чем у Seedance
- **Суперсила 2:** можно прописать **несколько сцен в одном промпте без ручного сшивания** в CapCut
- **Главное ограничение:** **только одно референсное фото максимум**. Поменял угол камеры — персонаж начинает мутировать. Поэтому Runway — для сцен, где важна картинка на одной локации, а не история с одним героем через несколько сцен
- **Стратегия применения:** планировать сценарий **кусками по 5–6 секунд**. Попытка описать 15 секунд одним промптом → дрифт персонажа к середине клипа
- **Официальный гайд по камерным терминам:** [help.runwayml.com/hc/en-us/articles/46749315925395](https://help.runwayml.com/hc/en-us/articles/46749315925395-Camera-Terms-Prompts-Examples)

### Kling 3.0

- **Суперсила:** **лучший face consistency между сценами** из всех моделей на рынке. Единственный правильный выбор, когда в креативе **реальный человек** и нужно несколько сцен с ним
- **Эксклюзивная фича — Motion Control:** загрузить **референс движения** (видео из TikTok/фильма с нужным танцем/движением) + стартовый фрейм персонажа → модель применяет движение к персонажу, держит лицо
- **Motion Control рекомендации:**
  - Чистый кадр, один объект, средний план, тело видно 80% времени, однотонный фон
  - Стабильная камера, штатив, без дрожания
  - Руки не должны закрывать лицо (иначе деформация)
  - Длительность референса: 3–6 секунд
  - Персонаж на входе — минимум 2K, лучше 4K разрешение, нейтральный фон
  - Поза персонажа должна примерно сочетаться с движением (не брать сидящего для бега)
- **Юз-кейсы:** копирование танцевальных трендов TikTok с брендовым персонажем; воспроизведение сцен из фильмов с подменой актёра

### VEO3 / VEO 3.1 (Google)

- **Суперсила:** прекрасное качество, справляется со сложными движениями и разговорами, встроенное генерирование аудио
- **Стоимость в Higgsfield:** ~58 кредитов / видео
- **Где используется:** default-инструмент Kumar & Solo для регулярной генерации видеокреативов по 5-этапному pipeline
- **Фича:** «Enhance ON» — Higgsfield сам улучшает промпт (подробнее описывает сцену, добавляет тегирование текста для говорящих персонажей)

### Sora 2 (OpenAI)

- **Суперсила:** видео со **звуком, диалогами, нормальной физикой** которая не ломается в середине сцены
- **Cameos:** загружаешь лицо → вставляешь в любые сцены с **передачей внешности и голоса**
- **Доступ:** требует подписки OpenAI; на начало 2026 — частично платный, частично по ожиданию
- **Не работает через Higgsfield-интерфейс**, только через OpenAI напрямую
- **Где используется:** street-interview формат и других типах, требующих реалистичной физики + диалогов

### Higgsfield

- **Не отдельная модель**, а **мета-интерфейс** над несколькими моделями (VEO3, Minimax Hailuo, Seedance, иногда Kling)
- **Ключевая ценность:** UGC Builder — аватары, 40+ готовых пресетов для сценариев (тестимониалы, распаковки, демо продуктов), шаблоны эффектов (зум, битвы персонажей, зоомы)
- **Подход:** «не-prompt-focused» — вместо написания промптов выбираешь пресет, результат собирается из готовых блоков
- **Ingredients:** добавление конкретных объектов в видео (загружаешь фотку автобуса или кружки — модель вставляет именно её)
- **Используется для:** быстрых UGC-видео, генерации хуков, регулярной фабрики контента без сложных промптов

### PrunaAI p-video-avatar

- **Платформа:** Replicate ([replicate.com/prunaai/p-video-avatar](https://replicate.com/prunaai/p-video-avatar)) `[conf:medium, src:2026-04-30]`
- **Вход:** фото + аудио (или текстовое описание); поддержка русского языка `[conf:medium, src:2026-04-30]`
- **Выход:** видео с аватаром
- **Самопозиционирование:** «P-Video is the fastest video model on Earth» — без независимой верификации `[conf:low, src:2026-04-30]`
- **Бизнес-модель:** при запуске в апреле 2026 был **free trial period** через Replicate `[conf:medium, src:2026-04-30]`
- **Юз-кейсы:** UGC-аватары, talking-head контент, короткие промо-видео с поддержкой РУ-голоса (это редкость — большинство видео-моделей плохо озвучивают русский)
- **Когда брать:** быстрая talking-head генерация (фото + audio → видео), когда нужна РУ-озвучка, и когда не нужна полная сцена (модель — про аватар, не про среду)
- **Источник наблюдения:** [@neuraldvig](https://t.me/neuraldvig) пост 10617 от 2026-04-30 ([[sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026]])

### Bach.Art (Video Rebirth, май 2026)

- **Платформа:** [bach.art](https://www.bach.art/), стартап Video Rebirth `[conf:high, src:2026-05-08]`
- **Качество:** по оценке @cgevent — уровень Kling 3, не Seedance 2.0 `[conf:medium, src:2026-05-08]`
- **Стоимость:** $0.019 / кредит (через $15 за 800 кредитов, кредиты не сгорают); **6 сек 720p = 24 кредита ≈ $0.45/видео или $0.075/сек** `[conf:high, src:2026-05-08]`
- **Free plan:** 60 кредитов при логине Google + 60 ежедневно `[conf:high, src:2026-05-08]`
- **Суперсила 1:** **Multi-Shot Montage до 30 сек** — 5 клипов × 6 сек + 4 склейки в одном промпте, модель сама собирает раскадровку `[conf:high, src:2026-05-08]`
- **Суперсила 2:** **отсутствие face-fence** — Tom Cruise, Brad Pitt и другие селебы доступны для генерации `[conf:medium, src:2026-05-08]`. **Этически рискованное позиционирование** — для коммерческого продакшна требует юридической оценки.
- **Reference-to-Video:** **до 8 reference картинок** на входе (сравнимо с @-системой Seedance 2.0) `[conf:high, src:2026-05-08]`
- **Звук:** липсинк, войсовер встроены `[conf:high, src:2026-05-08]`
- **Когда брать:** parody-content, character-driven длинные сцены без сшивания, low-budget индивидуальные эксперименты с celebrity-faces
- **Когда НЕ брать:** коммерческий проект без явного consent на face — регуляторный риск
- **Подробный разбор:** [[volatile-strict/competitor-news/bach-art-video-gen-2026-05]]

### HiDream-O1-Image (8B) — раскрытый Peanut (опенсорс выпущен)

<!-- superseded 2026-05-10 by [[sources/2026-05-19-tg-cgevent-may08-19-2026]] : раньше эта модель была загадочным «Peanut (Open Weights Coming Soon)» на text-to-image арене, статус open weights — анонсированы но не выпущены. Теперь раскрыта личность и веса выложены. -->

- **Идентичность:** «загадочный Peanut» с арены оказался **HiDream-O1-Image (8B) от vivago.ai** `[conf:high, src:2026-05-10]`
- **Прежняя позиция на арене:** 8-е место, перед ним только закрытые модели (выше Z-Image Turbo, Qwen-Image, FLUX.2 [dev]) `[conf:medium, src:2026-05-06]`
- **Архитектура:** **pixel-space, без VAE, без text-encoder** — «pixels in, pixels out», без latent compression и decoder-артефактов `[conf:medium, src:2026-05-10]`. Внутри — рассуждающий prompt-агент (типа gpt-image-2 и Nano Banana)
- **Версии:** dev (28 шагов инференса) / standard (50 шагов); разрешение до 2048; есть режим редактирования `[conf:medium, src:2026-05-10]`
- **Выложено:** дистиллированный + недистиллированный варианты + Reasoning-Driven Prompt Agent; код с WebUI; FP8-версии для 16GB/10GB VRAM; Pinokio Launcher; раскатано на Fal и других агрегаторах
- **Рассуждающий агент:** локальная Gemma-4-31B-it или любой OpenAI-compatible endpoint
- **Оценка:** Ostriss (AI Toolkit) — «самая крутая модель, которую я видел… суперэффективное использование пиксельного пространства, обучается очень быстро, изменит всю отрасль». Caveat @cgevent: дистиллят пока «мылит картинку, с кожей не очень», проблемы с анатомией и лицами `[conf:medium, src:2026-05-10]`
- **Когда брать:** опенсорс-эксперименты с pixel-space подходом; LoRA-обучение (Ostriss отмечает быстрое обучение); ждать нативной поддержки в ComfyUI (кастом-ноды уже есть)

### Krea K-2 — собственная модель Krea (художественные стили)

- **Платформа:** [krea.ai/krea-2](https://www.krea.ai/krea-2) `[conf:high, src:2026-05-12]`
- **Архитектура:** тренирована **с нуля**, заточена на разные художественные стили — «креатив в духе Midjourney», не фоторил/рендеринг текста `[conf:high, src:2026-05-12]`
- **Доступ:** на старте (12 мая) только Max/Business; **19 мая раскатили всем подписчикам + безлимитные генерации без кредитов на неделю** для всех тарифов (Basic/Pro/Max/Business) `[conf:high, src:2026-05-19]`
- **Key trick (гайд Олега, тестил 2 недели до релиза):** **первое слово промпта = тег жанра/стиля** (фото / иллюстрация / коллаж / мурал) — управляет рендером ещё до того, как модель узнаёт, что рисовать. Без жанрового тега скатывается в дефолтный сглаженный реализм `[conf:medium, src:2026-05-13]`
- **Принцип:** не зажимать длинными промптами
- **Когда брать:** художественный/иллюстративный контент, сюрреализм, коллажи; неделя безлимита — окно для массового теста без затрат
- **Гайд:** [olegpars.com/k2guide](https://olegpars.com/k2guide/read/#ru)

### AsymFLUX.2 Klein — pixel-space, +40% скорости

- **Платформа:** [hanshengchen.com/asymflow](https://hanshengchen.com/asymflow/), есть код + быстрое демо, поддержка ComfyUI на днях `[conf:high, src:2026-05-15]`
- **Архитектура:** работает напрямую в пиксельном пространстве, **No VAE** `[conf:high, src:2026-05-15]`
- **Главная фишка:** **на 40% быстрее**, меньше мыла `[conf:medium, src:2026-05-15]`
- **Caveat @cgevent:** понимание промпта — типичный Flux, «чуда нет»; слово `poster` в промпте заставляет рисовать буквы (убирать) `[conf:medium, src:2026-05-15]`
- **Когда брать:** быстрая локальная генерация, когда нужна скорость и приемлемое качество Flux-уровня

### Starchild-1 (Odyssey) — multimodal world model

- **Платформа:** [odyssey.ml/introducing-starchild-1](https://odyssey.ml/introducing-starchild-1); демо пока нет, только техрепорт `[conf:medium, src:2026-05-18]`
- **Тип:** интерактивный генератор сцен между «генераторами миров» и «генераторами видео» (преемник Odyssey 2)
- **Суперсила:** **реалтайм 20 FPS**, редактирование и стриминг видео в реальном времени, упор на звук и полную мультимодальность; управление генерацией в реальном времени, **в т.ч. голосом** `[conf:medium, src:2026-05-18]`
- **Позиционирование:** «обучение на основе богатого мультимодального взаимодействия с миром» vs только визуального наблюдения. @cgevent: «если размотать вперёд — это реально матрица»
- **Когда брать:** не сейчас (демо нет) — **сигнал для трекинга** реалтайм-интерактивной генерации

### Tencent: HY-World-2.0 + Pixal3D (3D / world, опенсорс)

- **HY-World-2.0** — опенсорсный генератор миров (аналог Marble), код и веса выложены ([github.com/Tencent-Hunyuan/HY-World-2.0](https://github.com/Tencent-Hunyuan/HY-World-2.0)); есть и web-демо с китайским логином `[conf:high, src:2026-05-18]`
- **Pixal3D** — 3D-генератор, под капотом **Trellis.2**, pixel back-projection в 3D-feature-volume для direct pixel-to-3D соответствия; веса + код + демо ([ldyang694.github.io/projects/pixal3d](https://ldyang694.github.io/projects/pixal3d/)) `[conf:medium, src:2026-05-12]`
- **Когда брать:** 3D-ассеты и сцены для опенсорс-пайплайнов; альтернатива Trellis/Hunyuan

### Viggle.ai P.I.N.O.C — нейромокап (видео → fbx/glb)

- **Платформа:** [viggle.ai/3d-studio](https://viggle.ai/3d-studio/landing) — pivot из мемных видео в нейромокап `[conf:medium, src:2026-05-13]`
- **Вход → выход:** видео персонажа → **скелет с анимацией в fbx/glb** для импорта в Blender/Maya; либо фото персонажа → превью анимации в гауссианах
- **Доступ:** «вроде как бесплатно», есть login as guest
- **Когда брать:** перенос движения из видео в 3D-пайплайн; мост между AI-генерацией и классическим CG

### Video2Video / обобщённый нейрорендер

- **Подход:** снимаешь себя реальной камерой → нейрорендеришь через video2video (проще, чем раскадровки + промпты), но надо понимать, что и как снимать/монтировать `[conf:medium, src:2026-05-18]`
- **Замена персонажа (Seedance мультиреференс):** на вход анимация + картинка нового персонажа + промпт `change the girl in the video (@video) to the man in the image (@image)` `[conf:medium, src:2026-05-18]`
- **Импликация (@cgevent):** для каждой страны в прокате/стриминге можно подменять персонажей; «выбор персонажа на стартовом экране Нетфликса»
- **Когда брать:** локализация контента под аудитории, замена актёров без пересъёмки

### LTX Director — All-in-One Timeline в ComfyUI

- **Платформа:** [github.com/WhatDreamsCost/WhatDreamsCost-ComfyUI](https://github.com/WhatDreamsCost/WhatDreamsCost-ComfyUI) `[conf:high, src:2026-05-15]`
- **Что это:** таймлайн и монтаж прямо в ComfyUI — I2V, T2V, FLFF, Prompt Relay, Custom Audio
- **Позиционирование:** «никаких агентов и токенов» — **контр-тренд к agentic-продуктам** (Higgsfield Super Computer), full control в Comfy
- **Когда брать:** Comfy power-users, которым нужен таймлайн без переключения на агентов и без сжигания кредитов

### Ideogram Background Remover (май 2026)

- **Платформа:** [ideogram.ai/features/background-remover](https://ideogram.ai/features/background-remover/)
- **Архитектура:** **отдельная модель** (не работа основной модели), натренирована с нуля на собственных датасетах `[conf:medium, src:2026-05-08]`
- **Качество:** не ломается на прозрачных объектах, **чистая альфа** `[conf:medium, src:2026-05-08]`
- **Доступ:** включая бесплатный план `[conf:high, src:2026-05-08]`
- **Сигнал:** Ideogram движется в сторону **слоёв и композа** — потенциально превращается из text-to-image в **slice-based composition tool**
- **Когда брать:** массовый продакшн ассетов с альфой (постеры, превью, прозрачные UI-элементы)

### LTX2.3 All-in-One workflow (опенсорс)

- **Платформа:** ComfyUI workflow на [civitai.com/models/2553704](https://civitai.com/models/2553704/ltx23-all-in-one-prompt-relay-id-lora-controlnet-detailer-upscaler-custom-audio-keyframes) `[conf:high, src:2026-05-08]`
- **Архитектура:** объединяет в одном пайплайне:
  - LoRA-based character/style conditioning
  - **Voice identity transfer (ID LoRA)** — единое лицо + голос в нескольких клипах
  - Custom или сгенерированный audio
  - ControlNet-guided animation по reference-видео
  - Keyframe images для structured motion control
- **Когда брать:** опенсорс-power-users (только Comfy, только hardcore), которые хотят полный контроль workflow без переключения между сервисами
- **Caveat:** только для технически подготовленных пользователей — Comfy не для beginner'ов
- **Разбор:** [reddit.com/r/StableDiffusion/s/mnanyCoOtH](https://www.reddit.com/r/StableDiffusion/s/mnanyCoOtH)

### Minimax Hailuo 2.3

- **Стоимость в Higgsfield:** ~6 кредитов / видео (дешёвая)
- **Суперсила:** хорошо держит **лицо персонажа** при статичных сценах
- **Когда брать:** персонажи почти не двигаются, движения минимальны. Для экономии кредитов на «говорящей голове»-жанре

## Сводная таблица

| Модель | Стоимость | Скорость | Face consistency | Key feature | Source |
|---|---|---|---|---|---|
| Seedance 2.0 | $0.03/сек | ~30 мин | Высокая (если @Image1 хорош) | @-система, `[cut]` | `[conf:medium, src:2026-04-03]` |
| Runway Gen-4.5 | ~9× Seedance | <6 мин | Среднее (дрифт >5 сек) | Кинематографичный язык камер | `[conf:medium, src:2026-04-03]` |
| Kling 3.0 | Средняя | Средняя | **Лучшая в классе** | Motion Control | `[conf:medium, src:2026-03-06]` |
| VEO3 (Higgsfield) | 58 кредитов | Средняя | Хорошая | Встроенное аудио, Enhance | `[conf:medium, src:2025-12-12]` |
| Sora 2 | Подписка OpenAI | Средняя | Высокая | Cameos (подмена лица) | `[conf:medium, src:2025-12-03]` |
| Minimax Hailuo 2.3 | 6 кредитов | Быстрая | Средняя (только статика) | Дешёвая для говорящих голов | `[conf:medium, src:2025-12-12]` |
| Midjourney (static-only) | Подписка MJ | Быстрая | — | Художественный бренд-стиль, персонажи, мудборды | `[conf:high, src:2025-12-03]` |
| Nano Banana | Подписка / Google Ads | Быстрая | Высокая | Консистентный персонаж, работает с текстом | `[conf:high, src:2025-12-03]` |
| PrunaAI p-video-avatar | Free trial / Replicate-rate | Быстрая (self-claim) | Хорошая (talking-head) | РУ-голос, фото+аудио → аватар | `[conf:medium, src:2026-04-30]` |
| Bach.Art | $0.45 / 6 сек видео | Средняя | Декларируется как ключевая фича | **Multi-Shot Montage 30 сек, no face-fence** | `[conf:medium, src:2026-05-08]` |
| HiDream-O1 (8B, =Peanut) | Опенсорс (compute сам) | dev 28 / std 50 шагов | TBD (дистиллят слабый) | Pixel-space, no VAE, reasoning prompt-agent | `[conf:medium, src:2026-05-10]` |
| Krea K-2 | Безлимит/неделя, далее тариф | Быстрая | — (художественные стили, не фоторил) | Тег жанра первым словом промпта | `[conf:high, src:2026-05-19]` |
| AsymFLUX.2 Klein | Опенсорс (compute сам) | +40% vs Flux | — | Pixel-space, no VAE, скорость | `[conf:medium, src:2026-05-15]` |
| Starchild-1 (Odyssey) | Демо нет (техрепорт) | Realtime 20 FPS | TBD | World model, управление голосом в realtime | `[conf:medium, src:2026-05-18]` |
| Ideogram bg-remover | Free / Ideogram tier | Быстрая | — | Отдельная модель для альфы | `[conf:medium, src:2026-05-08]` |
| LTX2.3 All-in-One workflow | Опенсорс (compute сам) | Variable | Высокая через ID LoRA | Full Comfy pipeline single-workflow | `[conf:high, src:2026-05-08]` |
| LTX Director | Опенсорс (Comfy) | Variable | — | Таймлайн+монтаж в Comfy, без агентов/токенов | `[conf:high, src:2026-05-15]` |

Все оценки — **self-reported** практикой Kumar & Solo. Независимых бенчмарков (например, Arena-style) в статьях нет, поэтому `confidence: medium` везде. Для более строгих оценок нужны независимые замеры.

## Рекомендованные связки

- **Фабрика контента по 5-stage pipeline ([[canon/marketing-frameworks/ai-video-production-pipeline]]):** Sora (если доступ) + VEO3 + Higgsfield — для аватаров, Midjourney для стиля, Nano Banana для массовой генерации стартовых фреймов и SMM-креативов
- **Один человек в нескольких сценах (реальный актёр в UGC):** Kling 3.0 по умолчанию, fallback на Sora 2 с Cameos
- **Красивая одна сцена с киношной камерой:** Runway Gen-4.5, но с планированием на 5–6-секундные куски
- **Массовая генерация коротких сцен через один промпт (микро-истории):** Seedance 2.0 с `[cut]`
- **Минимальные движения персонажа (говорящая голова, тестимониал):** Minimax Hailuo 2.3 для экономии

## Как этот стек меняется

На момент написания (апрель 2026) уже идут переговоры и анонсы новых моделей — см. [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]]. Эта страница будет обновляться/заменяться каждые 2–3 месяца. Главный инвариант, переживающий смену моделей: **5-этапный pipeline** в [[canon/marketing-frameworks/ai-video-production-pipeline]] остаётся прежним, меняются только конкретные модели, выполняющие этап IV.

## Anti-patterns

- **Ставить Runway по умолчанию, а не Seedance** — если не нужны дорогие киношные камеры, это в 9× дороже без соответствующего ROI
- **Генерировать в Sora/Seedance эмоционально-экспрессивные креативы без учёта жёсткой цензуры** → bans + перекресталённая себестоимость
- **Использовать одну модель для всего ролика, когда нужна смена контекста** — ломается консистентность. Правильно — Kling для консистентных сцен + Seedance для сложных движений, сшивка в CapCut
- **Планировать один Runway-клип на 15 секунд** — персонаж уплывёт к середине. Только куски по 5–6 секунд, сшивка потом

## Связь с другими страницами

- [[canon/marketing-frameworks/ai-video-production-pipeline]] — механика 5 этапов, внутри которой эти модели выполняют этап IV
- [[canon/marketing-frameworks/andromeda-creative-framework-2026]] — почему нужно так много креативов, что окупается массовое производство
- [[evolving/content-trends/ai-static-creative-templates-2026]] — параллельный стек для статических креативов (Nano Banana, Midjourney, Flux, DALL-E 3)
- [[evolving/content-trends/ru-ai-course-production-stack-2026]] — RU-parallel snapshot (Kandinsky Video, Шедеврум) для course production без VPN; качественно отстаёт от global stack, но достаточен для фонового видео в обучающих курсах
- [[canon/marketing-frameworks/ai-course-production-conveyor-7-stages]] — 7-этапный pipeline production курса; эта страница покрывает sub-этап 6.1 (фоновое видео) глобальным стеком
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]] — навык «промптить Nano Banana, VEO3, Higgsfield» как часть профиля
- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — свежие релизы, которые могут вытеснить текущих лидеров
- [[volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1]] — параллельная консолидация вайбкодинг-tooling'а
- [[volatile-strict/competitor-news/higgsfield-super-computer-agent-2026-05]] — agentic-надстройка над этим стеком (агент сам выбирает модель)
- [[volatile/weekly-digest/tg-cgevent-may-w3-2026]] — дайджест дампа, откуда пришли HiDream-O1 / Krea K-2 / AsymFLUX
- [[sources/2026-05-19-tg-cgevent-may08-19-2026]] — source-дамп 8-19 мая (новые модели)

## Backlinks

_14 pages link to this one._

- [[canon/marketing-frameworks/ai-video-production-pipeline]]
- [[canon/marketing-frameworks/andromeda-creative-framework-2026]]
- [[evolving-strict/market-data/appmagic-mobile-landscape-2026]]
- [[evolving-strict/market-data/specialized-video-finetune-cost-anchor-2026-05]]
- [[evolving/content-trends/ai-serial-content-format-2026]]
- [[evolving/content-trends/ai-static-creative-templates-2026]]
- [[evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format]]
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]]
- [[index]]
- [[sources/2026-04-14-tg-solokumi-nov2025-apr2026]]
- [[sources/2026-05-05-tg-cossaru-apr-24-may-5-2026]]
- [[sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026]]
- [[volatile-strict/competitor-news/elevenmusic-platform-launch-2026-05]]
- [[volatile-strict/competitor-news/grok-imagine-agents-2026-05]]
