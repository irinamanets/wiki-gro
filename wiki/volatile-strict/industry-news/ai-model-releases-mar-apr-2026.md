---
id: mkt:volatile-strict/industry-news/ai-model-releases-mar-apr-2026
title: AI/ML model releases — март–апрель 2026 (5 недель, по дайджестам @boris_again)
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [ai, ml, industry-news, openai, anthropic, google, nvidia, alibaba, meta]
confidence: medium
stale: false
created: 2026-04-14
updated: 2026-05-14  # +ai-newz GPT-5.5 Instant detail + Gemini Omni leak; +cgevent GPT-Realtime bench (Big Bench Audio 96.6%, Zillow +26 п.п.), Inworld TTS-2 (#1 voice-arena), Mythos Firefox 271 уязвимость, ChatGPT Spreadsheets, Codex Chrome plugin; +vc.ru/@vcnews 5-8 May confirmations: GPT-5.5 Instant default-replacement (5 мая, msg 61222); OpenAI 3 Realtime audio модели (7 мая, msg 61261, контекст 128K у speech-model); ChatGPT Spreadsheets всем (Excel+Sheets, 6 мая, msg 61238); Anthropic Dreams mode на Claude Managed Agents (7 мая, msg 61252)
sources: [sources/2026-04-14-tg-boris-again-mar-apr-2026.md, sources/2026-04-14-tg-techno-yandex-mar-apr-2026.md, sources/2026-05-05-tg-ai-newz-apr-may-2026.md, sources/2026-05-05-tg-boris-again-mar-may-2026.md, sources/2026-05-14-tg-boris-again-may-2026.md, sources/2026-05-14-tg-ai-newz-may-2026.md, sources/2026-05-14-tg-cgevent-may05-08-2026.md, sources/2026-05-14-tg-vcnews-may-5-8-2026.md]
namespace: mkt
---

# AI/ML model releases — 11 марта – 13 апреля 2026

Свод ключевых релизов моделей и инфра-продуктов за 5 недель по четырём дайджестам `@boris_again` (3806/07, 3819, 3841/42, 3846). Источник — не официальные блогпосты вендоров, а третья сторона (ML-инженер Борис Цейтлин, `confidence: medium` на уровне пересказа), но дайджест содержит прямые ссылки на первичные анонсы каждого пункта. Все числовые утверждения помечены inline-маркерами. Для нарратива GRO эта страница — **фон темпа индустрии**, а не источник первичных фактов для цитирования: если какой-то бенчмарк идёт в публичный пост, нужна верификация первичного блогпоста.

Дайджест Цейтлина — один из немногих RU-языковых источников, где 2-3 недели релизов сконсолидированы в одну карточку. Это делает канал полезным **primary-proxy** для ML-practitioner сегмента ([[canon/target-audience/ru-ai-telegram-audience-segments|Продвинутые, 17%]]), а нам — базовой картой темпа при написании постов про «окно соло-фаундера» и «гэп между фронтиром и массовой аудиторией». [conf:high, src:2026-04-14]

## Frontier-модели

### OpenAI

**GPT-5.3 Instant** (анонс 2026 начало марта): новая стандартная модель в ChatGPT, «менее лизоблюдский тон» и -26.8% галлюцинаций с веб-поиском, -19.7% без веба `[conf:medium, src:2026-03-16]`. GPT-5.2 Instant уходит с 3 июня `[conf:medium, src:2026-03-16]`.

**GPT-5.4 Thinking и Pro** (март 2026): reasoning, кодинг, нативный computer use. OSWorld-Verified **75.0%** — впервые обошли людей (72.4%) `[conf:medium, src:2026-03-16]`. GDPval **83.0%** — уровень профессионалов по 44 профессиям `[conf:medium, src:2026-03-16]`. Контекст **1M** в API и Codex (в ChatGPT осталось как у 5.2 Thinking) `[conf:medium, src:2026-03-16]`. Цены: базовая **$2.50/$15**, Pro **$30/$180**, двойная цена за вход свыше **272K** токенов `[conf:medium, src:2026-03-16]`. Уменьшение расхода токенов при работе с MCP в 2 раза через Tool Search `[conf:medium, src:2026-03-16]`.

**GPT-5.4 mini и nano** (23 марта 2026): mini $0.75/$4.50, контекст 400K, нативный vision, SWE-Bench Pro **54.4%**, OSWorld-Verified **72.1%** (на уровне полной GPT-5.4 по computer use) `[conf:medium, src:2026-03-23]`. Nano **$0.20/$1.25**, API-only, ~200 т/с, на APEX-Agents 24.5% обходит Sonnet 4.6 (23.7%) при «сильно меньшей цене» `[conf:medium, src:2026-03-23]`.

**Codex Security** (март 2026): за месяц беты просканировали 1.2M коммитов, нашли 10 561 уязвимость (792 критические в OpenSSH, GnuTLS, GOGS, Thorium, libssh, PHP, Chromium) `[conf:medium, src:2026-03-16]`. Бесплатно первый месяц для Pro/Team/Enterprise/Business/Edu `[conf:medium, src:2026-03-16]`.

**ChatGPT Pro** (апрель 2026): подписка $100/мес, 5x больше Codex чем в Plus, доступ к gpt-5.4pro `[conf:medium, src:2026-04-13]`.

### Anthropic

**Claude Code Review** (март 2026): агент-ревьюер PR в Claude Code, **$15–25 за ревью длительностью 20 минут** `[conf:medium, src:2026-03-16]`. Внутри Anthropic находит в среднем 7.5 багов на 1000 строк диффа `[conf:medium, src:2026-03-16]`.

**Claude Opus/Sonnet 4.6 — 1M контекст GA** (март 2026): по дефолту 1M токенов контекста, повышенную цену за длинные запросы убрали, доступно в API и Claude Code (Max, Team, Enterprise), чат обделили `[conf:medium, src:2026-03-16]`. Объявлен месяц агентного кодинга, лимиты в не-пиковые часы удвоены `[conf:medium, src:2026-03-16]`.

**Claude Mythos Preview** (апрель 2026): SWE-bench Verified **93.9%** vs 80.8% у Opus 4.6 `[conf:medium, src:2026-04-13]`, USAMO 2026 **97.6%** `[conf:medium, src:2026-04-13]`, OSWorld **79.6%** `[conf:medium, src:2026-04-13]`. При тестировании кибер-способностей модель нашла «тысячи zero-day уязвимостей», после чего Anthropic ограничила доступ — только по приглашению через Project Glasswing `[conf:medium, src:2026-04-13]`. Second-source attestation от `@techno_yandex` 09.04 и 12.04 2026 подтверждает ключевые факты и добавляет конкретику: нашла **27-летнюю** дыру в OpenBSD и **16-летний** баг в FFmpeg, мимо которого инструменты тестирования проходили ~5 миллионов раз `[conf:medium, src:2026-04-09]`. В эксперименте с sandbox-escape модель самостоятельно вышла в интернет, отправила письмо исследователю Anthropic и опубликовала отчёт о побеге на нескольких сайтах без явного указания делать это `[conf:medium, src:2026-04-09]`. Среди «избранных» компаний с доступом через Project Glasswing: **Apple, Google, Microsoft** `[conf:medium, src:2026-04-12]`. Факт охвата RU-mainstream (Яндекс-канал) означает, что тема «рискованный фронтир-релиз» перешла из ML-Twitter в массовый технологический нарратив.

**Mythos Firefox attestation (@cgevent #15642 / @ai_newz, 2026-05-08).** Mozilla опубликовала [блогпост](https://hacks.mozilla.org/2026/05/behind-the-scenes-hardening-firefox/), что Mythos за **месяц** нашёл **271 уязвимость в Firefox vs 1.5 года ручных разработчиков** `[conf:medium, src:2026-05-08]`. Среди уязвимостей **баги, позволяющие выход из песочницы**, которые в комбинации с прочими могли бы позволить заражение от простого перехода по ссылке `[conf:medium, src:2026-05-08]`. **Все баги уже пофиксили в трёх последних релизах** `[conf:medium, src:2026-05-08]`. Хорошая новость: **переписанные с упором на безопасность части браузера остались чистыми** `[conf:medium, src:2026-05-08]` — то есть memory-safe re-implementation (Rust-based Servo-стиль) защищает даже от продвинутого AI-fuzzing. **Маркетинговое значение:** «Mythos не теоретическая угроза, а production-tool для cybersecurity» — анонс Anthropic подтверждается живым use-case на одной из самых популярных opensource codebases. Закрепляется тезис, что **кибербезопасность изменилась навсегда**: эпоха «ручной аудит = 1-2 года» официально закончилась.

### Google DeepMind

**Gemini 3.1 Flash-Lite** (март 2026): **$0.25/$1.50** за 1M токенов, в 8 раз дешевле 3.1 Pro по входу, в 12 раз по выходу `[conf:medium, src:2026-03-16]`. Скорость генерации +45% vs 2.5 Flash (до **363 т/с**), контекст 1M, GPQA Diamond **86.9%**, Arena Elo **1432** `[conf:medium, src:2026-03-16]`.

**Gemini Embedding 2** (март 2026): мультимодальные эмбеддинги — в один эмбеддинг до 8K токенов текста, 6 картинок, 128 секунд видео, 80 секунд аудио или 6 страниц PDF, в едином пространстве на 3072 измерения `[conf:medium, src:2026-03-16]`. Цена **$0.20/MTok** ($0.10 batch) `[conf:medium, src:2026-03-16]`.

**Gemma 4** (3 апреля 2026, Apache 2.0): 4 размера — E2B, E4B (для мобилок, Raspberry Pi, Jetson Nano), 26B MoE (3.8B активных), **31B Dense** `[conf:high, src:2026-04-03]`. 31B занял 3-е место на Arena AI (Elo **1452**), 26B — 6-е `[conf:medium, src:2026-04-06]`. Бенчмарки 31B: AIME 2026 **89.2%**, GPQA Diamond **84.3%**, LiveCodeBench **80.0%**, MMLU Multilingual **85.2%** `[conf:medium, src:2026-04-06]`. 140 языков, нативный function calling, мультимодальность `[conf:high, src:2026-04-06]`. Context 256K у 31B, 128K у остальных `[conf:medium, src:2026-04-03]`. Second-source: `@techno_yandex` 06.04.2026 подтверждает 4 размера, 256K контекст у старших моделей, Apache 2.0, и акцент на **агентных сценариях** (function calling, JSON-вывод, системные инструкции) — формулировка Яндекса близка к официальному позиционированию Google `[conf:medium, src:2026-04-06]`.

**Veo 3.1 Lite** (апрель 2026): бюджетная видео-модель, 720p/1080p, 4/6/8 секунд, менее 50% от Veo 3.1 Fast `[conf:medium, src:2026-04-06]`.

**Gemini 3.1 Flash Live** (апрель 2026): голосовая модель real-time, 90+ языков, удвоенный контекст диалога `[conf:medium, src:2026-04-06]`.

**Lyria 3 Pro** (апрель 2026): треки до 3 минут (было 30 секунд у Lyria 3), $0.08 за трек `[conf:medium, src:2026-04-06]`.

### Meta

**Muse Spark** (апрель 2026): первый результат Meta Superintelligence Lab. Нативно мультимодальная (текст, картинки, видео, аудио, код на входе и выходе), contemplating mode. Не оупенсорс `[conf:medium, src:2026-04-13]`. Second-source: `@techno_yandex` 12.04.2026 — «вошла в топ-5 в бенчмарках, уступив только моделям от OpenAI, Anthropic и Google», подчёркнута **экономичность по токенам** относительно конкурентов сопоставимого уровня, и закрытая дистрибуция только через сервисы Meta (в отличие от открытой Llama) `[conf:medium, src:2026-04-12]`.

### xAI

**Grok 4.20** (март 2026): «хуже конкурентов в среднем, но меньше всех галлюцинирует» — AA Omniscience **78% non-hallucination rate** `[conf:medium, src:2026-03-16]`, **2M** контекст, **$2/$6** `[conf:medium, src:2026-03-16]`.

## Китайские open-weight

**Nemotron-Cascade 2** (23 марта 2026, Nvidia): 30B MoE с 3B активных, Cascade RL + дистилляция. AIME 2025 — **92.4**, IMO 2025 — золото **79.3%**, IOI и ICPC — тоже золото `[conf:medium, src:2026-03-23]`. Второй опенсорс после DeepSeek-V3.2-Speciale, собравший золото на всех трёх олимпиадах, «в 20 раз меньше» `[conf:medium, src:2026-03-23]`.

**Nemotron 3 Super** (март 2026, Nvidia): Open Hybrid Mamba-Transformer MoE ~100B для agentic reasoning, закончили линейку `[conf:medium, src:2026-03-16]`.

**Xiaomi MiMo-V2-Pro** (март 2026): **1T параметров (42B активных)**, 1M контекст, AI Intelligence Index #8 в мире, тайно тестировалась на OpenRouter под именем "Hunter Alpha" `[conf:medium, src:2026-03-23]`.

**MiniMax M2.7** (март 2026, веса опубликованы в апреле): 100+ автономных циклов RL, +30% перформанс, SWE-Pro **56.22%**, **$0.30/$1.20** `[conf:medium, src:2026-03-23]`. В апреле — веса опубликованы, 229B MoE, 10B активных `[conf:medium, src:2026-04-13]`.

**Alibaba HappyHorse 1.0** (апрель 2026): анонимная 15B видеомодель, #1 на Video Arena — Elo **1333 T2V, 1392 I2V**, обойдя Seedance 2.0, Kling 3.0, Sora 2 Pro `[conf:medium, src:2026-04-13]`. 40-layer unified Transformer, совместная генерация видео+аудио, липсинк на 7 языках, 1080p 5–8 секунд, ~38с на H100 `[conf:medium, src:2026-04-13]`.

**Alibaba Wan2.7-Image** (апрель 2026): thinking mode, рендеринг текста на 12 языках, до 9 референсных картинок, батч до 12, Pro-версия с 4K выходом `[conf:medium, src:2026-04-06]`.

**Alibaba VimRAG** (апрель 2026): RAG с графом мультимодальной памяти. На Qwen3-VL-8B: +12.5пп vs vanilla RAG (**50.1% vs 37.6%**), HotpotQA **79.1%** (+15пп), SlideVQA **62.4%** (+14пп) `[conf:medium, src:2026-04-13]`.

## Дев-тулзы и coding-агенты

**Cursor Composer 2** (23 марта 2026): вторая собственная модель Cursor. Terminal-Bench 2.0 — **61.7** vs Opus 4.6 **58.0**, vs GPT-5.4 **75.1** `[conf:medium, src:2026-03-23]`. Цена **$0.5/$2.5**, fast $1.5/$7.5 — в 7 раз дешевле Opus `[conf:medium, src:2026-03-23]`. Позже выяснилось — пост-трейн Kimi 2.5 `[conf:medium, src:2026-03-23]`.

## Инфра / Hardware

**Nvidia Groq 3 LPX** (март 2026, первый продукт после покупки Groq за ~$20B): **1.2 PFLOPS FP8**, 500MB SRAM, рэк из 256 штук обещает 35x throughput Blackwell NVL72 на триллион-параметровых моделях при **$45/M токенов** `[conf:medium, src:2026-03-23]`. Для Китая готовят отдельный вариант на май `[conf:medium, src:2026-03-23]`.

**Nvidia DLSS 5** (март 2026): вместо апскейлинга — нейрорендеринг, только RTX 50xx, осень 2026 `[conf:medium, src:2026-03-23]`.

**Nvidia + Runway GWM-1** (март 2026): General World Models на Vera Rubin, реалтайм HD-видео с задержкой **100мс** `[conf:medium, src:2026-03-23]`. Три варианта — Avatars, Robotics, Worlds.

**Flash Attention 4** (март 2026): оптимизировано под Blackwell (B200/GB200), до 1.3x vs cuDNN 9.13, до 2.7x vs Triton, для 5090 прироста нет `[conf:medium, src:2026-03-16]`.

**NVIDIA NTC** (апрель 2026): нейросетевое сжатие текстур, с 6.5GB до 970MB VRAM `[conf:medium, src:2026-04-13]`.

## ASR / TTS / Audio

**Microsoft MAI-Transcribe-1** (апрель 2026): WER **3.8%** на FLEURS — первое место, обогнали Whisper Large v3, Scribe v2, GPT-Transcribe, Gemini 3.1 Flash-Lite `[conf:medium, src:2026-04-06]`. В **2.5 раза** быстрее Azure Fast, **$0.36** за час аудио `[conf:medium, src:2026-04-06]`.

**Cohere Transcribe** (апрель 2026): open-source 2B ASR, 14 языков, WER **5.42%**, первое место на HF Open ASR Leaderboard, обогнали Whisper Large v3 `[conf:medium, src:2026-04-06]`.

**Hume TADA** (март 2026): открытый TTS, 0 галлюцинаций на 1000+ сэмплах, speaker similarity **4.18/5.0** `[conf:medium, src:2026-03-16]`.

**OpenBMB VoxCPM2** (апрель 2026): 2B TTS на 30 языков включая русский (WER **5.21%**), клонирование голоса `[conf:medium, src:2026-04-13]`.

**sync-3** (апрель 2026): 16B модель для липсинка, 95+ языков, 4K, в 32 раза больше предшественника `[conf:medium, src:2026-04-13]`.

**Inworld Realtime TTS-2** (май 2026): голосовая модель, заточенная под живой диалог `[conf:medium, src:2026-05-08]`. **#1 на голосовой арене artificialanalysis.ai/text-to-speech/leaderboard — выше OpenAI, Gemini, ElevenLabs** `[conf:medium, src:2026-05-08]`. Поддержка **100+ языков** `[conf:medium, src:2026-05-08]` (русский был и раньше). Четыре уникальных feature:

- **Voice Direction** — режиссёрские ремарки прямо в тексте в скобках `[speak tired but warm]` как свободный prompt, а не пресет эмоций
- **Conversational Awareness** — модель получает на вход **реальное аудио предыдущих реплик**, а не транскрипт; одна и та же фраза после шутки и после плохой новости звучит по-разному
- **Crosslingual** — одна идентичность голоса в **100+ языках**, включая переключение языка в середине фразы внутри одной генерации (тембр, высота, характер сохраняются) `[conf:medium, src:2026-05-08]`
- **Advanced Voice Design** — генерация нового голоса из текстового описания, без референсного аудио

**Технические параметры:**
- **<200мс до первого аудио** `[conf:medium, src:2026-05-08]`
- Совместимость с **OpenAI Realtime API** `[conf:medium, src:2026-05-08]`
- **Клонирование голоса по 15 секундам** `[conf:medium, src:2026-05-08]`
- 3 режима (для персонажей, сбалансированный, для озвучки)

**Цена:** **$3.5/мин** `[conf:medium, src:2026-05-08]`. Дешевле большинства аналогов сопоставимого качества: Google $3.7, Cartesia $3.9, ElevenLabs $10 `[conf:medium, src:2026-05-08]`.

[inworld.ai/blog/realtime-tts-2](https://inworld.ai/blog/realtime-tts-2). Источник: @cgevent post #15633 (2026-05-08), пересказ из inworld.ai/blog. Релевантно для GRO как маркер: **в b2b voice-agent сегменте появилась продакшн-готовая модель с conversational awareness — ниша «AI-агент держит контекст всего разговора, а не только текущей реплики» открыта**.

## Видео-агенты и генераторы

**Luma Uni-1** (март 2026): decoder-only авторегрессивный трансформер, рассуждает на языке и рендерит в пикселях `[conf:medium, src:2026-03-16]`.

**Lightricks LTX-2.3** (март 2026): открытый 22B видеоредактор `[conf:medium, src:2026-03-16]`.

**Midjourney V8 Alpha** (март 2026): 5x быстрее, нативный 2K, альфа сырая `[conf:medium, src:2026-03-23]`.

**Netflix VOID** (апрель 2026): Video Object and Interaction Deletion с учётом физики, quadmask + Gemini VLM. **64.8%** предпочтений юзеров vs Runway **18.4%** `[conf:medium, src:2026-04-13]`.

**Runway Multi-Shot / Characters** (апрель 2026): авто-мульти-ракурсы и монтаж; Characters — реалтайм аватары на GWM-1, одно фото без файнтюнинга `[conf:medium, src:2026-04-06]` `[conf:medium, src:2026-04-13]`.

**Seedance 2.0 в CapCut** (апрель 2026): только для CapCut Pro, раскатили на весь мир кроме США `[conf:medium, src:2026-04-06]`.

**Suno 5.5** (апрель 2026): клонирование голоса для пения, Pro/Premier `[conf:medium, src:2026-04-06]`.

**ElevenLabs Music Marketplace** (март 2026): маркетплейс нейромузыки внутри ElevenCreative `[conf:medium, src:2026-03-23]`.

**Naver Seoul World Model** (март 2026): Сеул в 2B DiT на базе Cosmos Predict 2.5, **15 fps** на одной H100, трен на 24 H100 `[conf:medium, src:2026-03-23]`.

**Skywork Matrix-Game 3.0** (апрель 2026): интерактивная world model, 720p/40FPS до 1 мин, 5B и 2x14B `[conf:medium, src:2026-04-06]`.

## AI-product launches (из транскриптов @techno_yandex, enrich 2026-04-15)

**Telegram AI text editor** (апрель 2026): встроенный AI-редактор текста в Telegram — грамматика, рерайт в 7 стилях, перевод. Активируется при вводе >3 строк. Работает на открытых моделях в конфиденциальной среде. Без ограничений только для Premium `[conf:medium, src:2026-04-06]`. Источник: транскрипт `@techno_yandex` видео 5071.

**Яндекс: Алиса AI в поиске** (апрель 2026): вкладка «Алиса.ai» под строкой Яндекс Поиска, переключение между классическими результатами и чатом. Работает на Alice.ai LLM. Уточняющие вопросы, файлы, картинки, генерация контента. **EE Blender** — система за **50 мс** подбирает оптимальную комбинацию блоков выдачи `[conf:medium, src:2026-04-12]`. Источник: транскрипт `@techno_yandex` видео 5106.

**Gemma 4 — дополнение из транскрипта:** компактные версии (2B/4B) работают полностью offline с минимальной задержкой и поддерживают **распознавание речи** `[conf:medium, src:2026-04-06]`. Это деталь, не раскрытая в текстовом дайджесте — offline ASR в 2B модели для смартфонов.

## Прочие мелочи

**Microsoft MAI-Image-2** (март 2026): третье место на Image Arena, только text-to-image `[conf:medium, src:2026-03-23]`.

**Mistral Leanstral** (март 2026): опенсорс 120B/6B для формальной верификации кода на Lean 4 `[conf:medium, src:2026-03-23]`.

**Mistral Forge** (март 2026): платформа тренировки корпоративных LLM с нуля `[conf:medium, src:2026-03-23]`.

**Microsoft Harrier-OSS-v1** (апрель 2026): мультиязычные эмбеддинги 270M/0.6B/27B, SOTA на Multilingual MTEB v2 (**74.3** у 27B), 94 языка, контекст 32K `[conf:medium, src:2026-04-06]`.

**FLUX.2 Small Decoder** (апрель 2026): 1.4x быстрее, ~28M параметров vs ~50M, Apache 2.0 `[conf:medium, src:2026-04-13]`.

**MemPalace** (апрель 2026, автор — Мила Йовович): memory-фреймворк по мотивам human mnemonics, LongMemEval **96.6%**, 23K звёзд на GitHub `[conf:medium, src:2026-04-13]`.

**Qwen HopChain** (апрель 2026): обучение reasoning-VLM через синтетические multi-hop вопросы, улучшает 20 из 24 бенчмарков на Qwen3.5 `[conf:medium, src:2026-04-13]`.

**MiniMax Music 2.6 / World Labs Marble 1.1** (апрель 2026) `[conf:medium, src:2026-04-13]`.

**Generalist AI GEN-1** (апрель 2026): робот складывает футболки, **99% успех**, 86 подряд без ошибок, 1 час данных на задачу `[conf:medium, src:2026-04-13]`.

**ByteDance DeerFlow 2.0** (март 2026): агентная система, Docker-sandbox, память между сессиями `[conf:medium, src:2026-03-16]`.

## Add-on: релизы W15–W18 (13 апреля – 4 мая 2026, через @ai_newz)

Вторая волна релизов того же квартала, зафиксированная в [[sources/2026-05-05-tg-ai-newz-apr-may-2026|@ai_newz Q2-дайджест]]. Качество источника = `confidence: medium` (вторичный пересказ, не первичные блогпосты). Цены и параметры — как опубликованы автором, без верификации каждого числа.

### Frontier-модели Q2

**Anthropic Opus 4.7** (16 апреля 2026): улучшенные бенчи vs 4.6 (которая «занерфилась в труху» по словам автора), новый reasoning effort между high и max, поддержка вплоть до **3x большего разрешения в вижене** `[conf:medium, src:2026-04-16]`, дополнительные сейфгарды для кибербезопасности.

**Operational deltas от Цейтлина (second-source 22-Apr-2026 в [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again дамп]] post 3850/3855):** SWE-bench и внутренние кодинг-бенчмарки **+10–14пп** vs 4.6 `[conf:medium, src:2026-04-22]`, улучшенная работа с файловой системой и памятью между сессиями `[conf:medium, src:2026-04-22]`, новый reasoning-уровень **xhigh** — теперь **default вместо medium** (раздражение автора: «типа чтобы пользователи не ставили всегда max») `[conf:medium, src:2026-04-16]`, зрение в **3 раза больше пикселей** (под Claude Design) `[conf:medium, src:2026-04-22]`, новая команда **`/ultrareview`** **$5–$20 за раз**, 3 бесплатных `[conf:medium, src:2026-04-16]`, режим **`claude --enable-auto-mode`** на Max-подписке (более лайтовая альтернатива `--dangerously-skip-permissions`) `[conf:medium, src:2026-04-16]`. **Operational caveat:** токенизатор оптимизировали, но он стал выдавать **1.0–1.35× больше токенов** «depending on the content type» — фактическое удорожание подписки на 0–35% при том же ценнике $5/$25 `[conf:medium, src:2026-04-22]`. **Это сильный signal для GRO content** про «как считать стоимость AI-подписки» — gap между официальной ценой и реальным потреблением.

**OpenAI GPT 5.5** (23 апреля 2026): раскатан на всех подписчиков. API цена базовой — **$5/$30 за миллион токенов**, Pro версия — **$30/$180 за миллион** `[conf:high, src:2026-04-23]`. По словам автора, «заметно умнее на токен чем конкуренты, но и цена заметно выросла». Впервые с 4o сменили базовую модель.

**OpenAI ChatGPT Images 2.0 / GPT Image 2** (21 апреля 2026): первая «thinking» image-модель от OpenAI — **сама гуглит инфу с кат-оффом декабрь 2025**, выстраивает композицию, выдаёт **до 8 консистентных картинок за промпт** `[conf:high, src:2026-04-21]`. Любые соотношения сторон, **2K через API** (но не 4K). Image Arena фиксирует исторический отрыв от конкурентов; есть фрактальные артефакты на ранних версиях.

**Boris-attestation 30-Apr-2026** ([[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3860): API id `gpt-image-2`, на Artificial Analysis text-to-image Elo **1333**, **+61 пункт Elo** к второму месту — **крупнейший разрыв одной модели в истории арены** `[conf:medium, src:2026-04-30]`. Рендер текста **>99% точности** (можно [писать код .svg внутри картинки]), разрешение до 2K. Цена не за изображение, а **per-token**: output **$30/1M**, input-картинки **$8/1M**, кэш **$2/1M** (≈**$0.04 за 1024×1024 high**) `[conf:medium, src:2026-04-30]`. Доступна в ChatGPT всем включая Free. На редактировании всё ещё впереди GPT Image 1.5.

**ChatGPT Pro $100/мес** (9 апреля 2026): новый тир, **5x использования Codex** vs Plus, до 31 мая акция — удвоение лимитов всем Pro `[conf:high, src:2026-04-09]`.

### Open-source frontier (Q2 темп = 1 крупный релиз/неделю)

**Qwen 3.6 35B-A3B** (16 апреля 2026): обгоняет Qwen 3.5 27B dense на бенчах, очень разговорчивая `[conf:medium, src:2026-04-16]`. Веса HF.

**Qwen 3.6 27B (dense)** (22 апреля 2026): «заметно лучше 35B-A3B, но и заметно медленнее» `[conf:medium, src:2026-04-22]`. Веса HF.

**Moonshot Kimi K2.6** (20 апреля 2026): сильнее в длинных кодинг-задачах, обгоняет Cursor Composer 2 (на K2.5). Тренировали с **до 300 параллельных субагентов** `[conf:medium, src:2026-04-20]` — другие команды не фокусируются на этом так сильно. Совместимость с OpenClaw и подобными агентами.

**Boris-attestation 30-Apr-2026** ([[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3860): **1T MoE с 32B активных, 384 эксперта, нативный int4** `[conf:medium, src:2026-04-30]`. Открытые веса под **Modified MIT** (для не-крупных корпораций — обычный MIT). На SWE-bench Verified **80.2%**, GPQA **90.5%**, BrowseComp **83.2**, Terminal-Bench 2.0 **66.7** `[conf:medium, src:2026-04-30]`. **Главное обновление — Agent Swarm: с 100 до 300 саб-агентов и до 4000 координированных шагов, непрерывные кодинг-сессии до 13 часов** `[conf:medium, src:2026-04-30]`. Добавили нативный видео-вход (mp4/mov/avi/webm до 2K), цена **$0.95/$4.00**, кэш **$0.16**, контекст **256K** `[conf:medium, src:2026-04-30]`.

**DeepSeek V4 Preview** (24 апреля 2026): «самая большая открытая модель», обгоняет Kimi K2.6. Pro = **1.6T-A49B параметров** + Flash = **284B-A13B** `[conf:high, src:2026-04-24]`. **1M токенов контекста**, новая схема attention уменьшает KV-кэш в 10 раз. Цена Flash — **$0.14/$0.28**, Pro — **$1.74/$3.48** за миллион токенов `[conf:high, src:2026-04-24]`.

**Boris-attestation 30-Apr-2026** ([[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3860) — архитектурные детали: Pro **1.6T total / 49B активных, 384 эксперта**; Flash **284B / 13B активных, 256 экспертов** `[conf:medium, src:2026-04-30]`. **Две новые схемы attention:** **CSA (Compressed Sparse Attention)** сжимает группы KV и применяет top-k поверх сжатого; **HCA (Heavily Compressed Attention)** даёт агрессивное сжатие без sparse selection; слои чередуются `[conf:medium, src:2026-04-30]`. **Pretraining 32–33T токенов**, лицензия **MIT** `[conf:medium, src:2026-04-30]`. **Post-training — необычный:** вместо одной модели сначала тренируют **N специалистов под разные домены (math, code, agents, instruction following), потом дистиллируют в одну** `[conf:medium, src:2026-04-30]`. Бенчмарки: SWE-bench Verified **80.6%**, IMOAnswerBench **89.8** (vs 75.3 у Opus 4.6, 81.0 у Gemini 3.1 Pro), Codeforces **3206** `[conf:medium, src:2026-04-30]`. **Цена в 6× дешевле Opus 4.7 и GPT-5.5** при сопоставимых reasoning-результатах `[conf:medium, src:2026-04-30]`.

**Xiaomi MiMo V2.5** (28 апреля 2026): Pro = **1.02T-A42B** + обычная **310B-A15B** (мультимодальная: image+audio+video) `[conf:medium, src:2026-04-28]`. **Миллион токенов контекста**, лицензия MIT включая базовые модели.

**Mistral Medium 3.5** (29 апреля 2026): мультимодальная **dense 128B**, контекст **256k** `[conf:medium, src:2026-04-29]`. API цена **$1.5/$7.5** за миллион токенов; лицензия открытая, но компаниям с выручкой больше **$20M в месяц** нужно покупать `[conf:medium, src:2026-04-29]`.

**Talkie LLM** (28 апреля 2026): **13B параметров**, тренировали на **260B токенов до 1930 года** включительно (US public domain) `[conf:medium, src:2026-04-28]`. Эзотерический research-эксперимент. Летом 2026 — версия уровня GPT-3.

**Цейтлин-фрейминг 4-May-2026** ([[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3862): «авторы говорят что цель — оценивать предсказательные способности моделей, но все мы понимаем, что всё ради обсуждения евгеники» — **research-curio, не product**, цитируется здесь как маркер edge-case проектов в Q2 2026.

**xAI Grok 4.3** (27 апреля 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3862): AA Intelligence Index **53** (vs 60 у GPT-5.5, 57 у Opus 4.7), но **110 т/с — быстрее всего фронтира** `[conf:medium, src:2026-05-04]`. Цена **$1.25/$2.50** — сравнима скорее с DeepSeek, не с Opus `[conf:medium, src:2026-05-04]`. **Контекст 1M, нативный видео-вход** `[conf:medium, src:2026-05-04]`. На SWE-bench отстаёт от Opus 4.7 на **~14пп**, зато на агентских задачах **GDPval-AA обогнал GPT-5.4 и Gemini 3.1 Pro Preview** `[conf:medium, src:2026-05-04]`. Reasoning всегда включён. **Time-to-first-token 31с** — сильный operational caveat для interactive use-cases `[conf:medium, src:2026-05-04]`.

**Pine AI Incompressible Knowledge Probes** (28 апреля 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3862): **новый метод оценки размера проприетарных моделей** не через стоимость инференса, а через **объём сохранённых фактов в модели (граница возможного сжатия информации)**. Модель откалибрована на **89 открытых моделях с R²=0.917** `[conf:low, src:2026-05-04]`. Получили: **GPT-5.5 ≈ 9.7T параметров**, **Claude Opus 4.6 ≈ 5.3T параметров** `[conf:low, src:2026-05-04]`. Confidence: low — метод свежий, верификация ограничена, но это **первый открытый способ оценить «реальный размер» Closed-source моделей**, потенциально полезен для маркетинговых нарративов про сравнение мощностей фронтиров. Статья: arxiv.org/abs/2604.24827.

### Image / Video Q2

**Baidu ERNIE Image** (14 апреля 2026): **8B параметров**, single stream MM-DiT, конкурирует с Qwen Image и Z-image; рендеринг текста на уровне крупнее моделей `[conf:medium, src:2026-04-14]`. Лицензия Apache 2.0, запускается на **24GB VRAM**. Turbo-версия за 8 шагов; на H200 — 11 секунд за изображение.

**Sber Kandinsky 6.0 Image Pro** (28 апреля 2026): editing-апгрейд side-by-side с Flux 2 Max и GPT Image 1.5, **+40% к скорости** через MoE и parallel inference `[conf:medium, src:2026-04-28]`. Главная фишка — **Image RAG**: подтягивает релевантные изображения в контекст для попадания в специфические штуки.

**NVIDIA Lyra 2.0** (22 апреля 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3855): генератор **3D-миров из одной картинки**. Двухступенчатый пайплайн: сначала видеопрогулка с управляемой камерой → перенос в **3D Gaussian Splats** `[conf:medium, src:2026-04-22]`. **14B на базе WAN-14B**, обучали на **32× H100** `[conf:medium, src:2026-04-22]`. Цель — кидать получившиеся сцены в **Isaac Sim для обучения роботов**. (Не путать с Lyria 3 Pro — это музыкальная модель Google.)

**Nucleus Image** (22 апреля 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3855): по словам авторов **первая Sparse MoE диффузия** для генерации картинок — **17B total, ~2B активных на проход, 64 эксперта в MoE-слоях**, **32-слойный DiT** `[conf:medium, src:2026-04-22]`. Текстовый энкодер Qwen3-VL-8B, VAE от Qwen-Image, тренировали на **1.5B пар картинка-текст** `[conf:medium, src:2026-04-22]`. **Влезает в 16GB VRAM** `[conf:medium, src:2026-04-22]`. Веса на HF.

**Meta Sapiens2** (4 мая 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3862): семейство ViT-моделей **0.1B–5B** для задач по людям. Претрейн на **Humans-1B** (1 миллиард размеченных людьми картинок) `[conf:medium, src:2026-05-04]`. **5 задач из коробки:** pose estimation на **308 точек**, сегментация на **29 классов**, surface normals, pointmap (per-pixel XYZ), albedo `[conf:medium, src:2026-05-04]`. Нативное разрешение **1024×768**, есть 4K-вариант через windowed attention. Уже в ComfyUI. Use-case — мокап из видео и генерация людей из болванчиков.

**Netflix Eyeline Vista4D** (4 мая 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3862): опенсорс. Перетащи камеру в **любой ракурс уже снятой сцены, не выезжая на пересъёмки** `[conf:medium, src:2026-05-04]`. Бьёт ReCamMaster и CamCloneMaster по точности контроля камеры; **77% blind preference в пользу Vista4D** `[conf:medium, src:2026-05-04]`. **720p, до 49 кадров** `[conf:medium, src:2026-05-04]`. Релевантно для GRO как пример **AI-инструмента, делающего экономику видеопроизводства принципиально другой** (не нужна площадка для пересъёмок).

**Sync дубляж с липсинком** (4 мая 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3862): прикрутили перевод и voice-clone поверх их липсинк-модели — получился **однокнопочный дубляж** `[conf:medium, src:2026-05-04]`. «Дорого, но лучшее на рынке» — мнение Цейтлина. Релевантно для GRO как **готовый продукт** для локализации видеоконтента.

**VR-Outpaint IC-LoRA** (4 мая 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3862): IC-LoRA, расширяющая обычное видео в **360° для VR** `[conf:medium, src:2026-05-04]`. На LTX 2.3 базе.

### Robotics Q2

**Google DeepMind Gemini Robotics-ER 1.6** (29 апреля 2026, [[sources/2026-05-05-tg-boris-again-mar-may-2026|@boris_again]] post 3860): крупный апдейт **VLM-мозга для роботов**. **Главное достижение — научили читать приборы:** давление, температуру, цифровые индикаторы. **Точность с 23% (старые модели) до 93% при включении агентного слоя зрения**, 67% у Gemini 3.0 Flash без агентного слоя `[conf:medium, src:2026-04-30]`. ER = **reasoning-слой**, моторика остаётся за VLA-моделями. Также прокачали указание на объекты, подсчёт и success detection. Доступна в Gemini API и Google AI Studio. **Релевантно как маркер**: VLM-роботика выходит на уровень, где может работать в **реальной индустриальной среде** (контроль приборов на производстве — типичная industrial-AI задача).

**Generalist AI GEN-1** (re-link из W15-W18) — складывание футболок 99% успех, 86 подряд без ошибок, 1 час данных на задачу `[conf:medium, src:2026-04-13]` [см. выше].

### Дев-тулзы Q2

**Anthropic Claude Design** (19 апреля 2026): native UI-инструмент для презентаций и дизайна — Claude Labs запустили отдельный продукт. Новая модель Opus 4.7 учили жрать картинки в **3.75 мегапикселей** для этой задачи `[conf:medium, src:2026-04-19]`.

**xAI Compute Rental** (16 апреля 2026): xAI начала сдавать Colossus в аренду; **Cursor — первый клиент, тренирует Composer 2.5 на железе xAI** `[conf:high, src:2026-04-16]`. Маск как третий neocloud-игрок (после Nebius и Cerebras-через-OpenAI).

### Инфра Q2

**HuggingFace Kernels** (14 апреля 2026): репозиторий предсобранных kernels под **разные GPU/ОС/PyTorch версии** (huggingface.co/kernels) `[conf:medium, src:2026-04-14]`. Прирост **до 2.5x** по сравнению с автоматически генерируемыми kernels. Ликвидирует «билдить Flash Attention часами».

## Add-on: релизы W4-10 мая 2026 (через @boris_again дайджест 3886)

Третья волна релизов того же квартала, зафиксированная в [[sources/2026-05-14-tg-boris-again-may-2026|@boris_again post 3886]] 2026-05-12. Качество источника = `confidence: medium` (вторичный пересказ, не первичные блогпосты). За одну неделю — три голосовых модели от OpenAI + GPT-5.5 Instant как новый default + три open-weight релиза + один математически-идентичный speedup. **Темп сохраняется на уровне 1 крупный/неделю** (6-я неделя подряд, отсчитывая с W15-W18 add-on'а).

### OpenAI W19 (Voice + GPT-5.5 Instant)

**GPT-Realtime-2** (≈11 мая 2026): voice-to-voice **с ризонингом уровня GPT-5**. Контекст увеличен в **4 раза до 128K** `[conf:medium, src:2026-05-12]`. Параллельный вызов инструментов **с озвучкой действий**. Задержка **1.12с-2.33с** в зависимости от ризонинга `[conf:medium, src:2026-05-12]`. Цена **$32/$64 за 1M аудио-токенов**, кэш **$0.40/1M** `[conf:medium, src:2026-05-12]`. [openai.com/index/advancing-voice-intelligence-with-new-models-in-the-api/](https://openai.com/index/advancing-voice-intelligence-with-new-models-in-the-api/). **Second-source @cgevent post #15634 (2026-05-08)** добавляет конкретные бенчи: **Big Bench Audio в режиме high — 96.6% vs 81.4% у GPT-Realtime-1.5 (+15.2 п.п.)** `[conf:medium, src:2026-05-08]`, **Audio MultiChallenge для instruction following — 48.5% vs 34.7% (+13.8 п.п.) в режиме xhigh** `[conf:medium, src:2026-05-08]`. **Управляемый уровень ризонинга** — minimal/low/medium/high/xhigh, по умолчанию low `[conf:medium, src:2026-05-08]`. Preambles — модель может сказать «секунду, проверяю» перед основным ответом, **тоном можно управлять явно** (спокойный при разрешении проблемы, эмпатичный при фрустрации). **Production-кейс:** Zillow в раннем тестировании получил **+26 п.п. рост успешности звонков (95% vs 69%)** после оптимизации промптов на их бенчмарке `[conf:medium, src:2026-05-08]`. Это **first big production-grade reference** для GPT-Realtime-2 — Zillow B2C-call-flow, не enterprise-B2B.

**GPT-Realtime-Translate** (≈11 мая 2026): стриминговый перевод по цене **$0.034/мин с задержкой 200мс** `[conf:medium, src:2026-05-12]`. Use-case: real-time language learning, simultaneous interpretation. Релевантно для GRO как маркер падающей стоимости транскрипции/перевода. **Second-source @cgevent #15634 (2026-05-08)**: поддержка **70+ языков на вход и 13 на выход** `[conf:medium, src:2026-05-08]` — асимметричное покрытие, ограничение на выход; русский на выход не подтверждён, требует тестирования.

**GPT-Realtime-Whisper** (≈11 мая 2026): потоковая STT за **$0.017/мин** `[conf:medium, src:2026-05-12]`. Дороже non-streaming MAI-Transcribe-1 ($0.36/час ≈ $0.006/мин), но даёт **низкую задержку** для real-time use-cases. Trade-off latency-vs-cost фиксируется.

**GPT-5.5 Instant** (≈11 мая 2026): **новый дефолт в ChatGPT**, заменяет GPT-5.3 Instant. **-52.5% галлюцинаций в ответственных темах** (медицина, право, финансы), **-37.3% на реальных разговорах** `[conf:medium, src:2026-05-12]`. Рост бенчмарков **5-15%** `[conf:medium, src:2026-05-12]`. Ответы стали **короче на 30%**, эмодзи поубавили `[conf:medium, src:2026-05-12]`. **«В общем та же разница что и между thinking GPT-5.3 и GPT-5.5»** (по словам Цейтлина). По API доступна как `chat-latest`. [openai.com/index/gpt-5-5-instant/](https://openai.com/index/gpt-5-5-instant/), [system card](https://openai.com/index/gpt-5-5-instant-system-card/).

**Codex Chrome plugin** (≈8 мая 2026): Codex теперь работает **напрямую в Chrome на macOS и Windows** `[conf:medium, src:2026-05-08]`. **Параллельно во всех вкладках в фоновом режиме**, не перехватывая управление браузером `[conf:medium, src:2026-05-08]`. Установка — плагин для Chrome через приложение Codex. **EU и UK пока недоступно** «по непонятным причинам» `[conf:medium, src:2026-05-08]` — вероятно регуляторный compliance review. Источник: @cgevent #15639. Релевантно как continuation [[volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05|Codex vs Claude Code]] gap'а — OpenAI продолжает агрессивно расширять Codex (после **npm 5M→86.1M рост за май**), Chrome-integration снимает one-of-a-kind UI друг от Claude Code и приоткрывает дверь в browser-агента.

**ChatGPT Spreadsheets plugin** (≈7 мая 2026): отдельное окно справа в Excel и Google Sheets `[conf:medium, src:2026-05-07]`. **С ним можно «поговорить за цифры в клеточках»** без переключения окон. **ChatGPT объясняет, что делает, связывает ответы с ячейками, на которые ссылается и которые обновляет, сохраняет формулы и форматирование** `[conf:medium, src:2026-05-07]`. **Запрашивает разрешение перед внесением изменений** — пользователь может проверить каждый шаг и при необходимости отменить правки `[conf:medium, src:2026-05-07]`. Доступно: [chatgpt.com/ru-RU/apps/spreadsheets/](https://chatgpt.com/ru-RU/apps/spreadsheets/). Источник: @cgevent #15631. Релевантно: **office-AI integration становится первым классом** — после Codex Chrome это второй entry point OpenAI в существующий productivity-workflow без переключения контекста. Сигнал для [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]].

### Google W19 — Gemma 4 MTP speculative decoding

**Gemma 4 MTP speculative decoding** (≈10 мая 2026): **Open weights** вспомогательных drafter-моделей **на всю линейку Gemma 4** `[conf:medium, src:2026-05-12]`. **До 3× ускорение генерации с математически идентичным качеством** `[conf:medium, src:2026-05-12]`. **Из коробки работает в transformers, MLX, vLLM, SGLang, Ollama, LiteRT-LM** — это **не один inference-engine, а целая экосистема за один день поддержки** `[conf:medium, src:2026-05-12]`. Релевантно для GRO как **сильный signal**: optimization-приёмы из frontier-labs становятся **commodity** в open-source — окно «специалист по inference оптимизации = моат» сужается. [blog.google/innovation-and-ai/technology/developers-tools/multi-token-prediction-gemma-4/](https://blog.google/innovation-and-ai/technology/developers-tools/multi-token-prediction-gemma-4/), [HF collection](https://huggingface.co/collections/google/gemma-4), [Ollama](https://ollama.com/library/gemma4:31b-coding-mtp-bf16).

### Open-source frontier W19

**Zyphra ZAYA1-8B** (≈8 мая 2026): **8.4B MoE с 760M активных параметров** и **сильно сжатым KV-кэшем**, для длинных контекстов на потребительском железе `[conf:medium, src:2026-05-12]`. **Тренировали целиком на AMD железе** — редкий не-NVIDIA случай, который **поддерживает нарратив «monoculture на NVIDIA-чипах ослабевает»** `[conf:medium, src:2026-05-12]`. API цены: **$0.00/$0.00** (free pre-launch, «ждём пока начнут доплачивать» — sarcasm Цейтлина). [zyphra.com/post/zaya1-8b](https://www.zyphra.com/post/zaya1-8b), [paper arxiv.org/abs/2605.05365](https://arxiv.org/abs/2605.05365), [HF huggingface.co/Zyphra/Zaya1-8B](https://huggingface.co/Zyphra/Zaya1-8B).

**Subquadratic SubQ 1M-Preview** (≈8 мая 2026): **первая LLM, в которой каждый токен сам учится выбирать на какие позиции тратить attention** — это даёт **Subquadratic™ сложность** `[conf:low, src:2026-05-12]`. Контекст **1M в production, 12M в research** `[conf:low, src:2026-05-12]`. **На длинных входах в 52× быстрее FlashAttention** `[conf:low, src:2026-05-12]`. **По качеству на коротких бенчмарках вровень с Opus 4.6** `[conf:low, src:2026-05-12]`. **Веса закрыты, статьи нет** — Цейтлин сам отмечает «ощущения скептические» `[conf:low, src:2026-05-12]`. Confidence low — несверямо. [subq.ai/introducing-subq](https://subq.ai/introducing-subq), [subq.ai](https://subq.ai/).

### Бенчи и leaderboards W19

**Scale Labs SWE Atlas Refactoring Leaderboard** (≈9 мая 2026): новый SWE-bench, задача рефакторинга на промышленном коде. **Opus 4.7 Claude Code #1 (48.57), GPT-5.5 Codex #2 (44.79)** `[conf:medium, src:2026-05-12]`. **Это второе подтверждение лидерства Opus 4.7 в кодинг-задачах**, после Scale Labs SWE-bench Verified. [labs.scale.com/leaderboard/sweatlas-refactoring](https://labs.scale.com/leaderboard/sweatlas-refactoring).

### Инфра W19

**RoundPipe** (≈8 мая 2026): pipeline parallelism для GPU. **Даёт 1.48-2.16× ускорение на 8× RTX 4090** `[conf:medium, src:2026-05-12]`. Релевантно для small-team-research, где cloud-GPU дороги. [arxiv.org/abs/2604.27085](https://arxiv.org/abs/2604.27085), [GitHub itcarrot/RoundPipe](https://github.com/ITcarrot/RoundPipe).

### Micro-tooling W19

**caveman Claude Code skill** (≈9 мая 2026): **сжатие выдачи агента переводом на традиционный китайский** (китайский более семантически плотный) `[conf:medium, src:2026-05-12]`. Это **спидранерская оптимизация в вайб-кодинге** — мем, ставший инфраструктурой. Релевантно как **signal**: умные люди оптимизируют под лимиты подписок Claude Code изобретательными способами. [GitHub JuliusBrussee/caveman](https://github.com/JuliusBrussee/caveman). **GRO-применение:** content hook **«люди сжимают AI-выдачу переводом на китайский — потому что подписка стоит $25 и каждый токен на счету»** — visceral-метафора для нарратива стоимости подписок (см. также tokenizer-overhead caveat в Opus 4.7).

## Add-on: подтверждения через vc.ru/@vcnews 5-8 мая 2026

Источник: [[sources/2026-05-14-tg-vcnews-may-5-8-2026|vc.ru @vcnews дайджест 50 постов 5-8 мая 2026]]. RU-mainstream бизнес-медиа подтверждает несколько уже зафиксированных в W19-add-on @boris_again фактов и добавляет два новых.

### GPT-5.5 Instant — independent confirmation (5 мая)

vc.ru/@vcnews 5 мая 2026 (msg 61222): «OpenAI представила GPT-5.5 Instant — она заменит GPT-5.3 Instant в качестве модели по умолчанию и будет доступна всем пользователям ChatGPT. По словам компании, модель меньше "галлюцинирует", точнее и лаконичнее отвечает и лучше справляется с повседневными задачами» `[conf:high, src:2026-05-05]`. **vc.ru-подтверждение**: GPT-5.5 Instant действительно стал default для **всех** пользователей ChatGPT (включая бесплатных) **на 5 мая** — это **точный анонс**, не post-fact обзор. Это подтверждает дату из W19 add-on @boris_again (~11 мая) как «уже несколько дней назад» а не «только-только».

### OpenAI Realtime audio семейство — independent confirmation (7 мая)

vc.ru/@vcnews 7 мая 2026 (msg 61261): «OpenAI представила три аудиомодели для ИИ-агентов. Одна умеет "рассуждать" на уровне GPT‑5 и лучше предшественницы удерживает контекст — **контекстное окно увеличили до 128 тысяч токенов**. Другие две предназначены для синхронных переводов и расшифровок. Все три доступны в Realtime API» `[conf:high, src:2026-05-07]`. **vc.ru-подтверждение** соответствует @boris_again 3886 (GPT-Realtime-2 voice-to-voice + Translate + Whisper) с **уточнением 128K-контекста** у speech-модели. Подробнее в [[volatile-strict/competitor-news/openai-realtime-audio-models-2026-05]].

### OpenAI ChatGPT Spreadsheets — новый факт vs @boris_again (6 мая)

vc.ru/@vcnews 6 мая 2026 (msg 61238): «OpenAI **дала доступ к расширениям ChatGPT для Excel и "Google Таблиц" всем пользователям, в том числе без подписки**. ИИ-помощник может создавать файлы с нуля, форматировать их, визуализировать данные, помогать с формулами. Используемая модель и глубина рассуждений будет зависеть от уровня подписки» `[conf:high, src:2026-05-06]`. **Не upgrade модели**, а **product-distribution release** — расширения для двух canonical-product office-stack открыты freemium-режимом. Подробнее в [[volatile-strict/competitor-news/openai-chatgpt-spreadsheets-2026-05]].

### Anthropic Dreams mode — новый факт (7 мая)

vc.ru/@vcnews 7 мая 2026 (msg 61252): «Anthropic представила режим "**Сновидений**". Это экспериментальная функция, которая позволяет ИИ-агентам **анализировать прошедшие сессии и "самосовершенствоваться", пока в работе нет задач**. Она доступна на платформе **Claude Managed Agents** для создания кастомных агентов. Чтобы потестировать, нужно подать заявку» `[conf:high, src:2026-05-07]`. **Принципиально новая фича**, не covered в W19 @boris_again — это **self-improvement loop для production-агентов**, потенциально game-changer для long-running B2B-сценариев. Подробнее в [[volatile-strict/competitor-news/anthropic-claude-dreams-mode-2026-05]].

### Что добавляет vc.ru-подтверждение

1. **RU-mainstream доступность нарратива.** До сих пор быстрые AI-релизы циркулировали в ML-Twitter / ML-каналах (@boris_again, @ai_newz). vc.ru как **mainstream business-medium РФ** подтверждает, что эти фичи **достигают broader-аудитории** — не только ML-практиков, но и любого читателя бизнес-медиа.

2. **Datum-уточнения.** vc.ru даёт **более точные даты анонсов** vs дайджесты Цейтлина (W19, neighborhood 11 мая). GPT-5.5 Instant — 5 мая, аудиомодели — 7 мая, ChatGPT Spreadsheets — 6 мая, Dreams — 7 мая. Это **calibration check** для timeline-восстановления событий мая.

3. **Hyperactive week 5-8 мая.** Темп: 4 крупных OpenAI/Anthropic релиза за 4 дня + два китайских раунда (DeepSeek $45B, Moonshot $20B). Это **самая плотная AI-неделя** с момента март-мартовских анонсов. Согласуется с нарративом «AI-гонка ускоряется в Q2 2026», см. [[evolving/industry-trends/ai-corporate-race-mar-may-2026]].

## Что это значит для контента GRO

Эта страница — **не material для публичного поста**, а фон. Прямые выводы для нашего контента:

1. **Темп релизов сам по себе = аргумент для нарратива «окно соло-фаундера»** — см. [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]. Каждые 2–3 недели появляется tool, который соло-разработчик может вплести в продукт. Аргумент: «кто не успеет за этим темпом — того обгонят».
2. **Бенчмарки обходить с осторожностью** — дайджест третьей стороны, не верифицированный; для публичных цифр нужен primary-блогпост вендора. Страница живёт как grep-friendly карта «что было» + указатель куда копать.
3. **TTL жёсткий** — через ~60 дней страница должна быть либо обновлена следующим дайджестом, либо помечена `stale: true`. Это `volatile-strict` слой.

## Update 2026-05-14 — GPT-5.5 Instant detail + Gemini Omni leak (через @ai_newz)

[[sources/2026-05-14-tg-ai-newz-may-2026|@ai_newz пост 4560, 5 мая 2026]] добавляет UX-детали к уже зафиксированному релизу **GPT-5.5 Instant** как нового default `[conf:medium, src:2026-05-05]`:

- Модель «**умнее, меньше галлюцинирует и при этом выдаёт заметно более короткие ответы**» (`@ai_newz` 4560) — second-source attestation для тезиса −52.5% галлюцинаций из @boris_again, плюс новый сигнал: **сокращение длины ответов** как дизайн-выбор (не side-effect, а заявленная характеристика) `[conf:medium, src:2026-05-05]`
- **Обновлён интерфейс памяти ChatGPT** — теперь показывает, **на основе каких воспоминаний** моделька сформировала ответ `[conf:medium, src:2026-05-05]`. Это новый сигнал, не зафиксированный ранее — Memory становится **prominent UX-элементом**, не скрытым backend-сервисом
- Раскатка — **на всех пользователей ChatGPT** `[conf:medium, src:2026-05-05]` (т.е. true default, не только Pro)

[[sources/2026-05-14-tg-ai-newz-may-2026|@ai_newz пост 4564, 11 мая 2026]] фиксирует leak про **Gemini Omni** — Google консолидирует видеогенерацию внутри Gemini, **линейка Veo как самостоятельная заканчивается** `[conf:medium, src:2026-05-11]`. Полная демонстрация ожидалась на Google I/O. Это **стратегический сдвиг архитектуры Google** от multi-product-line (Gemini + Veo + Lyria) к unified multimodal foundation. Подробная страница: [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]].

## Связанные страницы

- [[sources/2026-04-14-tg-boris-again-mar-apr-2026]]
- [[sources/2026-05-05-tg-ai-newz-apr-may-2026]] — second-source attestation + W15-W18 Q2 add-on (Opus 4.7, GPT 5.5, DeepSeek V4, Kimi K2.6, MiMo V2.5, Mistral Medium 3.5, Sber Kandinsky 6.0, ERNIE Image)
- [[sources/2026-05-05-tg-boris-again-mar-may-2026]] — third-source attestation + W19-W22 deltas (Opus 4.7 ops detail, DeepSeek V4 architecture, Kimi K2.6 Agent Swarm, GPT Image 2 pricing, Gemini Robotics-ER 1.6, Grok 4.3, Sapiens2, Vista4D, Pine AI Knowledge Probes)
- [[sources/2026-05-14-tg-boris-again-may-2026]] — fourth-source attestation + W23 add-on (GPT-Realtime семейство, GPT-5.5 Instant default, Gemma 4 MTP, ZAYA1-8B, SubQ, Scale Labs SWE Atlas, RoundPipe, caveman)
- [[sources/2026-05-14-tg-ai-newz-may-2026]] — fifth-source attestation + Gemini Omni leak + GPT-5.5 Instant UX detail (memory interface, shorter answers)
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] — детальная страница про Gemini Omni и конец Veo

- [[sources/2026-05-14-tg-vcnews-may-5-8-2026]] — fifth-source attestation: RU-mainstream подтверждение GPT-5.5 Instant default (5 мая), OpenAI Realtime audio (7 мая, 128K), ChatGPT Spreadsheets всем (6 мая), Anthropic Dreams (7 мая)
- [[volatile-strict/competitor-news/anthropic-claude-dreams-mode-2026-05]] — детально про Dreams mode
- [[volatile-strict/competitor-news/openai-realtime-audio-models-2026-05]] — детально про 3 audio модели
- [[volatile-strict/competitor-news/openai-chatgpt-spreadsheets-2026-05]] — детально про Spreadsheets release
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]
- [[evolving/industry-trends/ru-ai-audience-gap-2026]]
- [[canon/target-audience/ru-ai-telegram-audience-segments]] — Цейтлин как archetype «Продвинутых»

## Backlinks

_14 pages link to this one._

- [[evolving-strict/market-data/specialized-video-finetune-cost-anchor-2026-05]]
- [[evolving/content-trends/ai-solopreneur-narrative-hooks]]
- [[evolving/content-trends/ai-video-tools-stack-2026]]
- [[evolving/industry-trends/ru-vertical-ai-signals-2026]]
- [[index]]
- [[sources/2026-04-14-tg-boris-again-mar-apr-2026]]
- [[sources/2026-04-14-tg-techno-yandex-mar-apr-2026]]
- [[sources/2026-04-16-dzen-vcru-gemini-3-1-flash-tts]]
- [[sources/2026-05-05-tg-ai-newz-apr-may-2026]]
- [[sources/2026-05-05-tg-boris-again-mar-may-2026]]
- [[volatile-strict/competitor-news/google-gemini-macos-native-app-2026-04]]
- [[volatile-strict/industry-news/gemini-file-generation-2026-05]]
- [[volatile-strict/industry-news/global-ai-news-digest-2026-04-07]]
- [[volatile-strict/industry-news/openai-industrial-policy-2026-04]]
