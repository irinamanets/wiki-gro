---
id: mkt:sources/2026-04-14-tg-boris-again-mar-apr-2026
title: Telegram @boris_again — дамп 50 постов 11 марта – 14 апреля 2026 (Борис Цейтлин, ML-инженер / SaaS-фаундер)
type: source
layer: evolving
theme: content-trends
tags: [telegram, ai, ml, vibecoding, claude-code, industry-news, content, post]
confidence: medium
created: 2026-04-14
updated: 2026-04-14
original: raw/processed/articles/tg_boris_again_20260414-142514.md
namespace: mkt
---

# Telegram @boris_again — дамп 50 постов 11 марта – 14 апреля 2026

## Метаданные
- **Тип:** Telegram channel dump (Markdown + 36 JPG + 2 MP4, bundle ingest)
- **Канал:** [@boris_again](https://t.me/boris_again)
- **Автор:** Борис Цейтлин (`@btseytlin`, упоминается в посте 3816). ML-инженер, автор книги про ML, строит собственный SaaS (TapAgent — агент тестирования мобильных игр), участник Kaggle-коммьюнити, параллельно мейнтейнит pet-проекты (hr-breaker, any2json), выступает на open-mic.
- **Даты постов:** 2026-03-11 22:48 UTC … 2026-04-14 11:00 UTC
- **Охват:** 50 сообщений, ids 3798..3847, 36 медиа-вложений, 2 видео
- **Дата добавления:** 2026-04-14 14:25 UTC (scheduled backfill «Борис опять»)
- **Экспертность автора:** **inferred (из метаданных источника)**. Автор регулярно публикует технические обзоры AI-моделей, ведёт собственный SaaS-продукт на Claude Code, публикуется на Habr (две статьи за период: Talk2Data self-service, AGC 2026 RAG), участвовал как бета-тестер ATS МТС. Это не верифицированный индустриальный эксперт масштаба Карпатого, но **ML-practitioner с доказуемым practical output** → мнения по AI-tooling и AI-рынку сохраняем как `confidence: medium` с атрибуцией «по мнению Бориса Цейтлина».
- **Sidecar note:** был — boilerplate от backfill-задачи «Борис опять», обозначает канал как источник новостей/трендов для генерации собственных постов в блог GRO. Не даёт специфичной классификации, но подтверждает намерение пользователя использовать канал как content-pipeline.
- **Sensitive flag:** none — публичный канал, PII/credentials отсутствуют.

## Релевантность

Применён рубрик rules.md раздел «Релевантность сырых источников». Из 50 постов **релевантно ~12** (AI/ML дайджесты как industry-news, мета-наблюдения про вайбкодинг как content-hooks, наблюдение о retention short-form video, 3 RU-вертикальных AI-кейса). Остальные **38 нерелевантны** для marketing-memory:

- **Нерелевантны** (идут только в audit log): мемы про AI (3798, 3802, 3813, 3815, 3820, 3829, 3830, 3832, 3839, 3844), нейроплатформа MIT про бэкпроп у мышей (3805), DataChannel-туннель через ВК-звонки (3810–3812, политически-техническое обход блокировок), Kaggle Leonardo дрон-эмика (3817/18), статья на Хабре про HyperAgents Татьяны Шавриной (3821–3824, академический ML-paper), статья про RAG-челлендж (3826, niche dev-audience), supply chain attack на LiteLLM (3825, infosec), claw-code Python port Claude Code (3831), GitHub приватные репо и обучение (3827), платная статья на RBC (3828), Google Colab в VS Code (3836), Gemma 4 анонс (3838 — дубль в дайджесте 3841), Artemis II (3834–35, 3840), Omni-модели объяснение (3843), Data Fest 2026 CFS (3847), hr-breaker v0.2.0 + MTC ATS validation (3804, 3809 — niche HR).
- **Дубли и self-promo**: 3799 (self-promo Habr Talk2Data), 3845 (вопрос в пустоту).

**Релевантные извлечения** (идут в layer-страницы):

| Пост | Дата | Содержание | Layer / Theme |
|---|---|---|---|
| 3800 | 2026-03-12 | Мета-рефлексия Цейтлина: Claude Code на Opus 4.6 — «качественный скачок», перешёл к «программированию промптами в трёх вкладках терминала», Cursor для диффов, сам код практически не пишет. Конкретные кейсы: iGPU-драйверы на Hetzner за 4 часа vs «раньше неделю», формулы в книге, hr-breaker, pycocotools, 500 символов в Forbes 30U30. Объекции: «нет инженерного вкуса», нужно «следить за разделением ответственности», диффы просматривать «стараюсь». | `evolving/content-trends` (hooks для GRO нарратива AI-solopreneurship + объекции) |
| 3814 | 2026-03-21 | Мета-рефлексия Цейтлина, тёмная сторона вайбкодинга: frontier AI сам себе галлюцинировал результаты, перепутал порядок аргументов функции; «проще всё сжечь» — состояние вайбкод-проекта когда становишься несчастным мейнтейнером легаси. Главный вывод: **«чтобы хорошо вайбкодилось, надо читать код»**. Lightweight-версия для тех, кто читать не умеет: спрашивать Клода «объясни мне по шагам как работает фича X». | `evolving/content-trends` (объекции к нарративу) |
| 3816 | 2026-03-21 | **Наблюдение о retention short-form video**: стендап 4-минутный формат — «плохое удержание в тиктоке/инсте, алгоритмы не подхватывают», поэтому в лентах видно много видосов с разговорами с аудиторией — там виральность выше, хотя шутки могут быть хуже. | `evolving/content-trends` (новое, важно для GRO TikTok/Reels-стратегии) |
| 3806, 3807 | 2026-03-16 | AI/ML дайджест 2–16 марта: GPT-5.3 Instant (-26.8% галлюцинаций с веб-поиском), GPT-5.4 Thinking/Pro ($2.50/$15 и $30/$180, OSWorld 75.0% впервые обошли людей, GDPval 83.0%, 1M контекст в API), OpenAI Codex Security (1.2M коммитов, 10 561 уязвимостей), Claude Code Review ($15–25 за ревью), Gemini 3.1 Flash-Lite ($0.25/$1.50), Gemini Embedding 2, Luma Uni-1, ChatGPT for Excel, LTX-2.3, Grok 4.20 (2M контекст, $2/$6), Nemotron 3 Super. | `volatile-strict/industry-news` |
| 3819 | 2026-03-23 | AI/ML дайджест 16–22 марта: Nvidia GTC week (Groq 3 LPX, DLSS 5, GWM-1, Nemotron-Cascade 2 — IMO gold 79.3%), GPT-5.4 mini/nano, Cursor Composer 2 (бьёт Opus 4.6 на Terminal-Bench 2.0, оказался пост-трейном Kimi 2.5), MiniMax M2.7, Xiaomi MiMo-V2-Pro (1T params, 1M контекст), Microsoft MAI-Image-2, Mistral Leanstral + Forge, Naver Seoul World Model. | `volatile-strict/industry-news` |
| 3841, 3842 | 2026-04-06 | AI/ML дайджест 23 марта – 5 апреля: **Google Gemma 4** (Apache 2.0, 4 размера включая E2B/E4B для мобилок, 31B Dense — AIME 2026 89.2%, LCB 80.0%, Arena Elo 1452 — 3-е место, 140 языков, мультимодальность), Veo 3.1 Lite, Microsoft MAI-Transcribe-1 (WER 3.8% FLEURS, обогнал Whisper Large v3, $0.36/час), GLM-5V-Turbo, Wan2.7-Image, Harrier-OSS-v1 (SOTA Multilingual MTEB 74.3), Matrix-Game 3.0, Lyria 3 Pro ($0.08/трек), Gemini 3.1 Flash Live, Suno 5.5, Runway Multi-Shot, Seedance 2.0 в CapCut (Pro), Cohere Transcribe (open-source 2B ASR, WER 5.42%), Теренс Тао доказал теорему с ChatGPT. | `volatile-strict/industry-news` |
| 3846 | 2026-04-13 | AI/ML дайджест 6–12 апреля: **Meta Muse Spark** (первый результат MSL, не оупенсорс), **Claude Mythos Preview** (SWE-bench Verified 93.9% vs 80.8% у Opus 4.6, USAMO 97.6%, по приглашению через Project Glasswing), Alibaba HappyHorse 1.0 (#1 Video Arena Elo 1333 T2V / 1392 I2V, 40L unified Transformer), Netflix VOID (удаление объектов из видео с физикой, 64.8% vs Runway 18.4%), Alibaba VimRAG (+12.5пп vs vanilla RAG), Runway Characters, FLUX.2 Small Decoder, sync-3 (16B, 95+ языков), MemPalace (LongMemEval 96.6%), VoxCPM2, FLUX-style робот, NVIDIA NTC, Qwen HopChain, MiniMax Music 2.6, World Labs Marble 1.1, MiniMax M2.7 веса выложены, ChatGPT Pro за $100/мес. | `volatile-strict/industry-news` |
| 3837 | 2026-04-02 | **IQDOC AI** — RAG-ассистент для врачей на клинических рекомендациях Минздрава РФ. «Тысячи врачей» пользуются, проанализировали 25 тыс. запросов, публикации в Медвестнике и Коммерсанте. Пример российского vertical-AI продукта, вышедшего на рынок. Необъяснимо: врачи из Челябинска чаще задают вопросы про рак лёгкого. | `evolving/industry-trends` (RU vertical AI market signals) |
| 3808 | 2026-03-17 | **@coreinfra** — DeepTech стартап на стыке AI-кодогенерации и формальной верификации. Ведут канал публично, chaos_theory (Rust property-based тесты) в опенсорсе. Founders с прошлым в ВКонтакте/Яндексе/Транзасе. RU vertical deeptech signal. | `evolving/industry-trends` (дополнительный сигнал к IQDOC) |
| 3833 | 2026-04-01 | Цитата Вячеслава Цыганова (исполнительный директор Т-Технологий): «Мы смотрим через призму: если наука не превращается в продукт, значит, инвестиция не завершена — надо продолжать инвестировать». Сигнал: на фоне общего снижения инвестиций в AI крупный российский IT-холдинг публично подтверждает продолжение фундаментальных вложений. | `evolving/industry-trends` (дополнительный сигнал) |

## Ключевые идеи

1. **Вайбкодинг зрелее, но не магия (Март 2026).** Выход Opus 4.6 + Claude Code превратил AI-ассистирование кода из «приятное дополнение» в **базовый способ работы с LLM**. Для ML-инженера уровня Цейтлина это уже не tool, а operating mode. Но автор сам же показывает тёмную сторону: без чтения кода возникает «слой слоп-костылей», агент сам себе галлюцинирует результаты вызова функций. **Для нарратива GRO это важный balancing point**: вайбкодинг = аргумент для hook «соло-фаундер может больше», но «надо читать код» = аргумент для objection «нужен навык, а не просто подписка на модель».

2. **Retention short-form video зависит от формата, а не только от контента.** Цейтлин эмпирически подтверждает, что static-camera стендап (даже с качественными шутками) не подхватывается алгоритмами TikTok/Reels — лучше работают разговоры с аудиторией (viral video format with engagement). Прямое практическое наблюдение для медиа-стратегии GRO.

3. **Темп AI-релизов зашкаливает.** За 5 недель (11 марта – 14 апреля 2026) вышли: GPT-5.3/5.4/5.4 mini/nano, Gemini 3.1 (Flash-Lite, Flash Live, Embedding 2), Gemma 4 (3-е место в Arena), Claude Mythos Preview (SWE-bench 93.9%), Cursor Composer 2, Nemotron-Cascade 2 (IOI/IMO gold), Grok 4.20, MiniMax M2.7, Xiaomi MiMo-V2-Pro (1T), Meta Muse Spark, Alibaba HappyHorse (видео #1), Netflix VOID, Runway GWM-1/Characters. Это плотность, которую GRO-контенту **невозможно догнать напрямую** (дайджест Цейтлина уже закрывает эту нишу лучше). Но это прекрасный **первоисточник темпа** для постов про «окно соло-фаундера» ([[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]) и для иллюстрации гэпа между фронтиром и массовой ИИ-аудиторией ([[evolving/industry-trends/ru-ai-audience-gap-2026]]).

4. **RU vertical AI живёт:** три независимых сигнала за 5 недель — IQDOC AI для врачей (реальная метрика: тысячи пользователей, 25К запросов, публикации в Медвестнике/Коммерсанте), CoreInfra (DeepTech AI + formal verification, опенсорс), Т-Технологии публичное подтверждение продолжения R&D инвестиций. Это **контр-сигнал к доминирующему нарративу** «русский рынок ИИ отстаёт и сворачивается».

## Факты и цифры

<!-- Числа с inline-маркерами — страница sources/ это evolving-layer audit, числовой синтез идёт в volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md -->

**Самые цитируемые бенчмарки периода:**
- Claude Mythos Preview: SWE-bench Verified 93.9% vs 80.8% у Opus 4.6, USAMO 2026 97.6%, OSWorld 79.6% `[conf:medium, src:2026-04-13]`
- GPT-5.4 Thinking: OSWorld-Verified 75.0% (впервые обошли людей 72.4%), GDPval 83.0% `[conf:medium, src:2026-03-16]`
- Gemma 4 31B: Arena Elo 1452 (3-е место), AIME 2026 89.2%, LiveCodeBench 80.0% `[conf:medium, src:2026-04-06]`
- Cursor Composer 2 vs Opus 4.6 на Terminal-Bench 2.0: 61.7 vs 58.0 `[conf:medium, src:2026-03-23]`

**Самые цитируемые цены:**
- GPT-5.4 Thinking: $2.50/$15 (базовая), Pro $30/$180, двойная цена >272K токенов `[conf:medium, src:2026-03-16]`
- GPT-5.4 mini: $0.75/$4.50, nano $0.20/$1.25 `[conf:medium, src:2026-03-23]`
- Gemini 3.1 Flash-Lite: $0.25/$1.50 за 1M токенов `[conf:medium, src:2026-03-16]`
- Cursor Composer 2: $0.5/$2.5 (fast $1.5/$7.5), «в 7 раз дешевле Opus» `[conf:medium, src:2026-03-23]`
- Microsoft MAI-Transcribe-1: $0.36 за час аудио `[conf:medium, src:2026-04-06]`

## Связанные страницы

- [[evolving/content-trends/ai-solopreneur-narrative-hooks]] — расширение hooks/objections на базе постов 3800 и 3814 Цейтлина
- [[evolving/content-trends/short-form-video-algo-retention-2026]] — новое наблюдение из поста 3816
- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — агрегат дайджестов 3806/07/19/41/42/46
- [[evolving/industry-trends/ru-vertical-ai-signals-2026]] — IQDOC + CoreInfra + Т-Технологии
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — усилен мета-рефлексией Цейтлина про Claude Code как новый operating mode
- [[canon/target-audience/ru-ai-telegram-audience-segments]] — Цейтлин как пример «Продвинутого» сегмента (17%), канал как медиа этого сегмента
