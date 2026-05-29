---
id: mkt:volatile/weekly-digest/tg-cgevent-may-w4-2026
title: "Дайджест @cgevent — 19–25 мая 2026 (Tier A/B/C)"
type: page
subtype: notes
layer: volatile
theme: weekly-digest
tags: [content, telegram, ai, cg, video-generation, gemini, seedance, runway, capcut, digest]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-cgevent-may19-25-2026.md]
namespace: mkt
---

# Дайджест @cgevent — 19–25 мая 2026

Конденсированная карта для быстрого скана content-team. Полная карта релевантности и фактологии — в [[sources/2026-05-26-tg-cgevent-may19-25-2026]]. Предыдущий дайджест канала — [[volatile/weekly-digest/tg-cgevent-may-w3-2026]] (8–19 мая).

Главная нить недели — **Google I/O 2026** (20 мая) и его эхо-волна (Aleph 2 через 2 дня, CapCut партнёрство через 2 дня, Seedance 2.1 анонс предшествующий). Цыпцын постит **5 длинных постов про Gemini Omni** (capabilities, World Knowledge, Avatar, Editing, What's Next) — это самый детальный разбор Omni в RU-комьюнити на сегодня.

## Tier A — главные индустриальные события

### A.1. Gemini Omni — официально на I/O, 5-th independent attest

Через 9 дней после leak'а @ai_newz Google официально анонсировал Gemini Omni на Google I/O 2026 (20 мая). Цыпцын расширяет картину пятью постами с тестами:
- **Генерация** (15710): «вялая динамика и физика», переключения камеры «своеобразны», по сравнению с Seedance заторможенно.
- **Редактирование** (15711, 15712, 15714): «совершенно огненное», можно загружать свои видео, не только генерации. Работает с реальными youtube-видео.
- **World Knowledge** (15713, 15743): не нужны детальные промпты — Omni понимает мир из LLM-контекста. Сильно подходит для образования/иллюстрации.
- **Avatar/Cameo** (15716, 15717): принимает фото человека → встраивает в видео. Внутри строит 3D-модель лица (фотограмметрия). Будущая фича — KYC-like video-референс лица.
- **What's Next** (15722): подкаст разработчиков обещает длительность до 30 сек, дополнительные tooling-инструменты, video-референс для лица. Это «HeyGen поперхнулся» — Google идёт прямо в digital-avatar.

Также vision-confirmed pricing: **Omni Flash 30 cr/video / Veo 3.1 Lite 10 / Veo 3.1 Fast 20** в Google Flow (15708).

→ обновление [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] (5-th attest).

### A.2. Google I/O 2026 — полная карта анонсов

Vision-confirmed (карточка 15709): **Gemini Omni / Gemini 3.5 Flash / Gemini Spark (background agent) / Antigravity (agent-first dev) / умные очки / Google Pics (Nano Banana под капотом)** — 6 главных продуктов.

Также: **TPU v8i** (800-1500 ток/сек, в Antigravity ×12 быстрее прошлой Pro), **Gemini Pro 4.0** обещают «в следующем месяце».

### A.3. Runway Aleph 2 — через 2 дня после I/O

Цыпцын ретранслирует анонс (1080p, 30 сек, доступ от Standard, промокод `RUNWAY50`) и тестирует на промпте про ниндзя. Цитата: «Выглядит как ответ редактирующим возможностям Gemini Omni.» — это **2-nd independent attest** Aleph 2 (первый был от @neuraldvig).

→ обновление [[volatile-strict/competitor-news/runway-aleph-2-video-2026-05]].

### A.4. Seedance 2.1 + 2.0 Mini — upcoming

@cgevent: Seedance 2.1 даст +20% качества к 2.0; Seedance 2.0 Mini лучше Fast при $0.073/сек. ByteDance дробит линейку под разные tier'ы (anti-pattern Google консолидации).

→ NEW [[volatile-strict/competitor-news/seedance-2-1-pricing-2026-05]].

### A.5. ByteDance vCube — video upscaler

API-only (Fal.ai + Replicate). Pricing: 1080p $0.0072/sec / 2K $0.0144 / 4K $0.0288. PRO mode ×10. ByteDance официально позиционирует как «дополнение к Seedance».

→ NEW [[volatile-strict/competitor-news/bytedance-vcube-video-upscaler-2026-05]].

### A.6. CapCut × Gemini — таймлайн внутри Gemini app

CapCut публично парнерится с Google Gemini. **В Gemini App приедет таймлайн для монтажа** через CapCut. Параллельно у Google — Flow (видео), Pics (картинки), теперь Gemini app (LLM + монтаж).

→ NEW [[volatile-strict/competitor-news/capcut-gemini-partnership-2026-05]].

### A.7. Sam Altman × YC — $2M в OpenAI токенах за equity

Vision-confirmed (15715): Tyler Bosmeny твит, 1.2M views. Distribution play против Claude Code на фоне блокировок Anthropic. Asymmetric trade: токены сейчас vs equity через 5+ лет.

→ NEW [[volatile-strict/competitor-news/openai-yc-2m-tokens-equity-2026-05]].

### A.8. Rodin 2.5 — 10M полигонов + organic anatomy

3D-AI выходит на органику (брови, волосы, вены). Extreme High mode + Thinking Mode. Use-case в основном 3D-печать (полигонаж избыточен для realtime).

→ NEW [[volatile-strict/competitor-news/rodin-2-5-3d-generator-2026-05]].

## Tier B — значимые тренды

### B.1. «Нейропрожарка» — 3 новых breakdown'а

- **«Новая жизнь» (Курмаев, 15719):** Higgsfield-only stack, ~10 ч / 2200-2400 ₽. Стилистика Аркейн/Spider-Verse. Главный pain — консистентность через fixed frame + Elements в Kling.
- **Союзмультфильм «Винни-Пух» (Голубь, 15729):** 50 ч / 2 недели / ~$210. Полный 6-этапный workflow с моделями (NanoBanana Pro для интерьеров/шотов, Kling 3.0 для анимации, Topaz через Krea для апскейла до 30fps, Suno 5.5 для музыки, Premiere). Конкурс «Ну ИИ погоди» к 90-летию студии.
- **Stasy Smith ЖБИ-рекламный ролик (15745):** Серия рекламных роликов для производителя ЖБИ, маскот «Олег» (железобетонный блок), 4 серии за месяц. Стек NanoBanana + GPT-Image + Kling/Grok/Sora + Seedance с 3-го ролика + ElevenLabs/Suno.

→ обновление [[evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format]].

### B.2. World Knowledge — главный edge Omni vs Seedance

Цыпцын настаивает: **главная ценность Gemini Omni не генерация, а понимание мира из LLM**. Применение в **образовании, иллюстрации, презентациях** — там, где детализация мира важнее динамики. Пример (15743): достаточно сформулировать концепцию ролика, Omni сама находит теорию, описания объектов, визуализирует.

→ добавить к [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] разделом про edu use-case.

### B.3. Frame-edit propagation vs prompt-edit — расхождение UX

Два подхода к video editing AI:
- **Prompt-natural-language** (Gemini Omni): описываешь словами «сделай всех фламинго»
- **Frame-direct propagation** (Runway Aleph 2): меняешь один кадр, AI разносит на весь ролик

Это **разделение рынка video AI** на два UX-русла. Параллельно — agentic подход Higgsfield, где монтаж происходит во время генерации.

→ reusable рамка для блог-поста *«Три UX-парадигмы AI-видео-редактирования 2026»*.

### B.4. PanoWorld — Qwen-Edit для риелторов

PanoWorld: 2D-планы этажей → виртуальные туры по дому. Под капотом — Qwen-Edit + гауссианы. **Use-case: недвига и риелторы** (виртуальный тур по дому, которого ещё нет).

### B.5. Krea K-2 — анонс опенсорс

Разработчик Krea.ai (sleenyre) в Twitter: планы выпустить **открытую версию модели K-2 + техрепорт + возможно специальная аниме-модель**. Цитата: «Теперь, когда мы заслужили право обучать более амбициозные модели, нужно сначала научиться ходить, прежде чем начинать бегать.» Интригующее намёк на крупную модель.

## Tier C — операционные сигналы

### C.1. AI-tooling сигналы

- **Apple ml-lito** — опенсорс 3D-генератор по картинке (github.com/apple/ml-lito); упор на освещение с разных ракурсов. Оценка @cgevent — отстаёт от Hunyuan.
- **WavFlow (Meta)** — Foley в waveform space, без VAE. Применение: переозвучка видео.
- **Black Forest Lab — erase-tool** вместо ожидаемого Flux.3. Flux Erase под капотом Flux.2 Klein 9B, требует ручной маски, веса не обновлены с февраля. **Сигнал отставания BFL**.
- **text-to-CAD (cadskills.xyz)** — опенсорс набор скиллов для Codex/Claude Code для CAD-генерации в цикле.

### C.2. RU enterprise-AI

- **Сбер собственная ERP-платформа** (15701) — релиз 2027, ИИ-агенты на ГигаЧат, scale сравним с SAP. Альтернатива импортозамещению. **Не AI-tooling**, но релевантно для трекинга RU enterprise AI direction.

### C.3. Робототехника

- **Unitree G1** (15702) — голосовое управление действиями в realtime. «Сначала думает, потом превращает в последовательность движений». Команды на китайском.

### C.4. AI-маркетинговый хайп (anti-pattern)

- **PettiChat ошейник-переводчик** (15749) — китайский Meng Xiaoyi за $118, заявлена точность 95% (vision 94.6%/1.2 сек), 10K+ предзаказов до релиза. **Скептик-пост Цыпцына**: «ДЕВЯНОСТО ПЯТЬ, КАРЛ!». Reusable hook про AI-хайп-ловушки в маркетинге.

### C.5. Реклама / job postings

- **Mira AI-агент в Telegram** (15723) — реклама конкурента Higgsfield (саб-агенты, 1000+ MCP, работа в групповых чатах).
- **ProMediaFlow вакансии** (15730) — CSM / Content&SMM / Partnerships. От $2000/мес.

## Главные актуализации (вики-actions)

| Action | Файл |
|---|---|
| Update (5-th attest) | [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] |
| Update (2-nd attest) | [[volatile-strict/competitor-news/runway-aleph-2-video-2026-05]] |
| Update (Seedance Mini, Aleph 2 30sec/1080p, Rodin 2.5, vCube) | [[evolving/content-trends/ai-video-tools-stack-2026]] |
| Update (+3 нейропрожарки) | [[evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format]] |
| NEW | [[volatile-strict/competitor-news/seedance-2-1-pricing-2026-05]] |
| NEW | [[volatile-strict/competitor-news/bytedance-vcube-video-upscaler-2026-05]] |
| NEW | [[volatile-strict/competitor-news/capcut-gemini-partnership-2026-05]] |
| NEW | [[volatile-strict/competitor-news/openai-yc-2m-tokens-equity-2026-05]] |
| NEW | [[volatile-strict/competitor-news/rodin-2-5-3d-generator-2026-05]] |
| Source | [[sources/2026-05-26-tg-cgevent-may19-25-2026]] |

## Связь с другими дайджестами

- **Предыдущий дамп канала:** [[volatile/weekly-digest/tg-cgevent-may-w3-2026]] (8–19 мая) — overlap по 19 мая
- **Параллельные дайджесты той же недели:**
  - [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — Цейтлин ретранслирует Google I/O
  - [[sources/2026-05-26-tg-neuraldvig-may-19-22-2026]] — neuraldvig про Aleph 2 (first mention)

## Связанные страницы

- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — макро-нарратив AI-гонки
- [[evolving/industry-trends/software-moat-erosion-2026]] — moat-erosion (CapCut в Gemini ускоряет)
- [[volatile-strict/competitor-news/higgsfield-super-computer-agent-2026-05]] — параллельный agentic подход
- [[sources/2026-05-26-tg-cgevent-may19-25-2026]] — первоисточник полного дампа
