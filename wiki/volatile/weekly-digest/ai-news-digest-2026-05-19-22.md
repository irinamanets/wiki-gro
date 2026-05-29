---
id: mkt:volatile/weekly-digest/ai-news-digest-2026-05-19-22
title: "AI-новости 2026-05-19..22 из @neuraldvig — Google I/O + RU AI-summit week"
type: page
subtype: news
layer: volatile
theme: weekly-digest
tags: [content, telegram, ai, news-digest, google-io, gemini-omni, sber, t-bank, yandex, tilda, runway]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-neuraldvig-may-19-22-2026.md]
namespace: mkt
---

# AI-новости 2026-05-19..22 из @neuraldvig

TTL **14 дней** — после 9 июня 2026 эта страница перейдёт в `stale`. Содержательно — сводка `[[sources/2026-05-26-tg-neuraldvig-may-19-22-2026|пятого среза канала @neuraldvig]]` (50 постов, 3,5 дня).

## Главные события недели (Tier A)

### Google I/O 2026 — 7 параллельных анонсов

Google провёл свой keynote 20 мая 2026. Канал neuraldvig сделал 7 постов подряд (10740–10748) на тему. **Краткий список анонсов:**

1. **Gemini Omni** — multimodal foundation; видео-генерация добавлена; **Veo как линейка закрыта** [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05|подробнее]]
2. **Gemini 3.5 Flash** — лидер на бенчмарках, **бесплатно** для всех в Gemini App [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05|подробнее]]
3. **Gemini 3.5 Pro** — обещают через месяц
4. **Gemini Spark** — Google клон OpenClaw, 24/7 background agent в Gmail/Calendar/Docs/сторонние приложения
5. **Умные очки от Google** — партнёрство с Gentle Monster, Wabby Parker, Samsung; Nano Banana, переводчик с копированием тона голоса, фоновые задачи (заказ еды)
6. **Google Pics** — ИИ-фотошоп на Nano Banana, сегментация объектов
7. **Multi-agent search** — мониторинг акций/блогов/релизов/цен/дропов несколькими параллельными агентами
8. **Подписка Ultra** — новая Ultra $100/мес; старая Ultra $250 → $200

### RU AI-summit week (ЦИПР 2026)

Параллельно с I/O Россия выкатила **6 крупных AI-анонсов** на одной неделе вокруг ЦИПРа:

| Анонс | Игрок | Сегмент | Страница |
|---|---|---|---|
| ERP на ГигаЧат, январь 2027 (замена SAP) | Sber + СберМаркетинг | enterprise resource planning | [[volatile-strict/competitor-news/sber-erp-gigachat-2027]] |
| Sage Observability AI Agent + Anomaly Analyzer | T-Bank | SRE / observability | [[volatile-strict/competitor-news/tbank-sage-observability-ai-agent-2026-05]] |
| AI-помощник Маркус для внутренних маркетологов | Sber + СберМаркетинг | marketing intelligence | [[volatile-strict/competitor-news/sber-marcus-marketing-ai-2026-05]] |
| Alice AI ART — улучшенный русский текст в картинках | Yandex AI Studio | image generation | [[volatile-strict/competitor-news/yandex-alice-ai-art-russian-text-2026-05]] |
| Image Generation Tool (DeepSeek V3.2 incl.) | Yandex AI Studio | agent platform | [[volatile-strict/competitor-news/yandex-alice-ai-art-russian-text-2026-05]] |
| Drinkit нейробариста | Yandex B2B Tech × Drinkit | B2C AI-customization | [[volatile-strict/competitor-news/yandex-drinkit-ai-barista-2026-05]] |
| 12 млн ₽ кибериспытания | T-Bank (CISO Гадарь) | bug bounty / employer-brand | (заметка в [[sources/2026-05-26-tg-neuraldvig-may-19-22-2026]]) |
| AI-сервис для борщевика — Зелёная Цифра премия | Yandex | green tech / computer vision | (заметка) |
| Бакалавриат AI360 Сбер+Яндекс | Sber + Yandex + 5 вузов | AI education | (заметка) |

Это **новый рекорд RU-AI-corporate-доли** в одной feed-неделе (~14% feed-а neuraldvig). См. также [[evolving/industry-trends/industrial-ai-measurable-roi-2026|индустриальный AI в РФ выходит в production phase]].

## Frontier models (Tier A)

- [[volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05|Qwen 3.7-Max]] — третье подтверждение (10770-10772). 35 часов autonomous-demo, 1158+ tool calls, CUDA-оптимизация ×10
- [[volatile-strict/competitor-news/deepseek-v4-pro-price-cut-2026-05|DeepSeek -75%]] — третье подтверждение цены $0.435/$0.8. neuraldvig прямо сравнивает с Gemini 3.5 Flash ($1.5/$9)
- [[volatile-strict/competitor-news/runway-aleph-2-video-2026-05|Runway Aleph 2.0]] — **новый release** через 2 дня после Gemini Omni. Frame-edit propagation механика.

## RU SaaS adopting AI (Tier B)

- [[volatile-strict/competitor-news/tilda-vibe-block-2026-05|Tilda Vibe Block]] (10768) — vibe-coding внутри RU mainstream-конструктора. **Первый RU mainstream-SaaS, принявший vibe-coding-парадигму** в no-code.

## Sceptical voices / balance (Tier B)

- **Bjarne Stroustrup + Linus Torvalds против vibecode** (10734) — создатели C++ и Linux раскритиковали AI-сгенерированный код за баги, безопасность, нечитаемость. Готовый balance-content для блога GRO.

- **Science deepfake-detection guide** (10765-10767) — обновлённые 7 признаков AI-генерации (геометрия, свет, шумы, мимика, речь, контекст). Эксперты советуют **доверять интуиции** + использовать другой AI для проверки.

## AI-tooling сигналы (Tier B)

- **Audiblez** (10733, GitHub) — EPUB → audiobook через Kokoro модель, open-source
- **Studio Moises** (10739) — audio2audio AI для музыкантов: stem-генерация, mastering, lyrics. Free тариф
- **prompt1.ru** (10760) — RU-prompts library, разбито по категориям
- **aiengineeringfromscratch.com** (10761) — free AI-engineering course, 412 уроков / 20 этапов
- **GigaAI SeeLight S1** (10776) — китайский humanoid-робот для пожилых, бесплатные тестовые партии 2027

## Промт-подборки в feed-е (Tier B)

3 промт-поста (10757, 10769, 10780) = 6% feed-а за 3,5 дня. Нормализованно ~12% для 7-дневного среза — в норме для канала. См. [[evolving/content-trends/ai-news-channel-prompt-packs]].

**Новый формат: Reverse Brainstorming** (10780) — двухходовый промт, сначала генерация anti-ideas, потом разворот. Reusable для GRO prompt-bank сегмента 2 (предприниматели).

## Actionable hooks для GRO

1. **«У Сбера маркетологи получают AI-коллегу. Что мешает каждому получить AI-наставника в кармане?»** — прямой positioning hook против Sber Маркус
2. **«Кофейня нашла способ давать каждому свой напиток. Что мешает вашему продукту?»** — для сегмента 2 ЦА (предприниматели)
3. **«Создатели Linux и C++ говорят: AI код пишет хуже джуна»** — balance-content
4. **«Как распознать AI-генерацию: 7 признаков от Science»** — SEO/GEO-hook
5. **«Tilda учит конструктор сайтов понимать промты. Что когда твоя CRM тоже это сделает?»** — для founder-сегмента
6. **«Runway убил Gemini Omni через 2 дня. Что это значит для AI-video стека»** — quick-take для технической аудитории

## Connections

- [[sources/2026-05-26-tg-neuraldvig-may-19-22-2026]] — первоисточник дайджеста
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — макро-нарратив гонки
- [[evolving/industry-trends/industrial-ai-measurable-roi-2026]] — RU AI в production phase
- [[evolving/content-trends/ai-news-channel-prompt-packs]] — формат канала
- [[volatile/weekly-digest/ai-news-digest-2026-05-13-19]] — предыдущая weekly-сводка
- [[volatile/weekly-digest/ai-news-digest-2026-04-07-14]] — первая weekly-сводка
