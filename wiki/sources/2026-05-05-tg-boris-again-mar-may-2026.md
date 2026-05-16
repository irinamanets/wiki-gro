---
id: mkt:sources/2026-05-05-tg-boris-again-mar-may-2026
title: Telegram @boris_again — re-export 50 постов 21 марта – 5 мая 2026 (overlap 3814–3847 с предыдущим дампом + новые 3848–3863)
type: source
layer: evolving
theme: content-trends
tags: [telegram, ai, ml, vibecoding, claude-code, industry-news, content, post]
confidence: medium
created: 2026-05-05
updated: 2026-05-05
original: raw/processed/articles/tg_boris_again_20260505-140114.md
bundle_children:
  - raw/processed/media/tg_boris_again_3814.jpg
  - raw/processed/video/tg_boris_again_3816.mp4
  - raw/processed/media/tg_boris_again_3817.jpg
  - raw/processed/media/tg_boris_again_3818.jpg
  - raw/processed/media/tg_boris_again_3820.jpg
  - raw/processed/media/tg_boris_again_3821.jpg
  - raw/processed/media/tg_boris_again_3822.jpg
  - raw/processed/media/tg_boris_again_3823.jpg
  - raw/processed/media/tg_boris_again_3824.jpg
  - raw/processed/media/tg_boris_again_3825.jpg
  - raw/processed/media/tg_boris_again_3826.jpg
  - raw/processed/media/tg_boris_again_3827.jpg
  - raw/processed/media/tg_boris_again_3828.jpg
  - raw/processed/media/tg_boris_again_3829.jpg
  - raw/processed/media/tg_boris_again_3830.jpg
  - raw/processed/media/tg_boris_again_3831.jpg
  - raw/processed/media/tg_boris_again_3832.jpg
  - raw/processed/media/tg_boris_again_3833.jpg
  - raw/processed/media/tg_boris_again_3834.jpg
  - raw/processed/media/tg_boris_again_3835.jpg
  - raw/processed/media/tg_boris_again_3836.jpg
  - raw/processed/media/tg_boris_again_3838.jpg
  - raw/processed/media/tg_boris_again_3839.jpg
  - raw/processed/media/tg_boris_again_3840.jpg
  - raw/processed/media/tg_boris_again_3841.jpg
  - raw/processed/media/tg_boris_again_3845.jpg
  - raw/processed/media/tg_boris_again_3846.jpg
  - raw/processed/media/tg_boris_again_3847.jpg
  - raw/processed/media/tg_boris_again_3848.jpg
  - raw/processed/media/tg_boris_again_3850.jpg
  - raw/processed/media/tg_boris_again_3851.jpg
  - raw/processed/media/tg_boris_again_3852.jpg
  - raw/processed/media/tg_boris_again_3853.jpg
  - raw/processed/media/tg_boris_again_3861.jpg
namespace: mkt
---

# Telegram @boris_again — дамп 50 постов 21 марта – 5 мая 2026 (re-export + 16 новых)

## Метаданные
- **Тип:** Telegram channel dump (Markdown + 33 JPG + 1 MP4, bundle ingest)
- **Канал:** [@boris_again](https://t.me/boris_again)
- **Автор:** Борис Цейтлин (`@btseytlin`). ML-инженер, автор книги про ML, строит TapAgent (агент тестирования мобильных игр), участник Kaggle-коммьюнити, мейнтейнит pet-проекты (hr-breaker, ultrapack, MatrixGame WASM port). Полный профиль — в [[sources/2026-04-14-tg-boris-again-mar-apr-2026]].
- **Даты постов:** 2026-03-21 10:14 UTC … 2026-05-05 10:26 UTC
- **Охват:** 50 сообщений, ids 3814..3863, 33 медиа, 1 видео.
- **Дата добавления:** 2026-05-05 14:01 UTC (scheduled backfill «Борис опять»).
- **Экспертность автора:** **inferred (из метаданных источника)** — атрибуция, верификация и обоснование `confidence: medium` см. в [[sources/2026-04-14-tg-boris-again-mar-apr-2026]].
- **Sidecar note:** был — boilerplate от backfill-задачи «Борис опять», обозначает канал как источник трендов для блога GRO.
- **Sensitive flag:** none — публичный канал, PII/credentials отсутствуют.

## Релевантность

**Структура дампа: 34 поста — повторное скачивание (3814–3847), 16 — новые (3848–3863).** Backfill-планировщик не помнит, какой high-watermark был у предыдущего ingest-а, и переэкспортирует сообщения после последнего отрезка пагинации; это объясняет, почему в дампе появились посты, уже обработанные в [[sources/2026-04-14-tg-boris-again-mar-apr-2026]] (там был охват 3798..3847).

Из 50 постов:
- **34 — full duplicate** контента предыдущего ingest-а (3814–3847). Все факты, классификации, layer-роутинг, supersession-решения, уже зафиксированы в `2026-04-14-tg-boris-again-mar-apr-2026`. **Здесь повторно не извлекаются** — это re-read без изменений (паттерн «GRO landing refresh»).
- **16 — новые** (3848–3863), из них релевантно ~9, нерелевантно ~7.

**Релевантные новые извлечения** (3848–3863):

| Пост | Дата | Содержание | Layer / Theme |
|---|---|---|---|
| 3849 | 2026-04-16 | Logical Intelligence — стартап на energy-based models (EBM): Founding Chair Ян ЛеКун, главный математик Майкл Фридман (Филдсовская медаль), 10 PhD + 6 ICPC-медалистов. EBM минимизирует функцию энергии в латентном пространстве вместо токен-генерации. Sudoku 96% (LLMs ~2%), PutnamBench 99.4% formal verification (исправили 15 ошибок в заданиях). Открытая позиция AI Researcher $225K-$350K + equity, San-Francisco, O-1 виза. **Не-LLM AI-architecture как альтернативный нарратив фронтиру** — слабый сигнал, but worth tracking. | **Не идёт в слой** — единичный сигнал на новую категорию (non-LLM reasoning AI). Audit-log only. Если появится 2-й независимый сигнал об EBM или альт-архитектурах reasoning AI — создать `evolving/industry-trends/non-llm-reasoning-architectures-2026.md`. |
| 3850 + 3855 | 2026-04-16 + 2026-04-22 | **Anthropic Opus 4.7** (16-Apr release): улучшенное распознавание картинок (>3x разрешение), новая команда `/ultrareview` ($5–$20 за раз, 3 бесплатных), reasoning-уровень **xhigh** (между high и max, теперь default вместо medium), токенизатор оптимизирован но выдаёт **1.0–1.35× больше токенов** в зависимости от content type, режим `claude --enable-auto-mode` на Max-подписке. Боря — independent second-source attestation к [[sources/2026-05-05-tg-ai-newz-apr-may-2026|@ai_newz Q2 add-on]] плюс новые ops-детали (xhigh default, tokenizer overhead, /ultrareview ценник, auto-mode CLI flag). | `volatile-strict/industry-news/ai-model-releases-mar-apr-2026` (extend Opus 4.7 entry с Боря-deltas). Tokenizer 1.0–1.35× — сильный operational caveat для подписочной экономики. |
| 3851 | 2026-04-17 | **ULTRAPACK** ([github.com/btseytlin/ultrapack](https://github.com/btseytlin/ultrapack), 27 ⭐ / 5 forks на момент скриншота) — собственный пак Claude Code-скилов Цейтлина: `/up:make <feature>` создаёт `docs/tasks/<feature>.md` и проводит через дизайн → планирование → исполнение → верификацию → ревью → доку, фокус на **инвариантах**, **принципах**, и **мануальном тестировании** (агент сам «протыкивает» свои изменения). Hands-off режим документирует решения, принятые без пользователя. Сравнивает себя с **feature-dev** (официальный, мало мануальных тестов), **Superpowers** («перегружен и уничтожает лимиты, пишет в планы какой код будет писать, дублируя работу, пихает TDD куда не надо»), **Personal AI Infrastructure** Миссии («перегружен какой-то шизофренией»). Hook: «Пет проекты в 2026 би лайк: 5 маркдаун файлов.» | `evolving/content-trends/ai-solopreneur-narrative-hooks` (добавляется hook **"5 маркдаун файлов = пет-проект 2026"** + кейс founder-as-tooling-author). Также cross-link в [[evolving/content-trends/your-pet-project-channel-hooks|Табунов]] как пример РУ-аналога паттерна «founder публикует свой dev-stack как контент». |
| 3853 | 2026-04-21 | **Boris Cosmic Rangers 2 → Rust WASM port** ([ilyagusev.dev/matrixgame](https://ilyagusev.dev/matrixgame/), [github.com/IlyaGusev/MatrixGame](https://github.com/IlyaGusev/MatrixGame)) — Цейтлин переписывает планетарные бои Космических Рейнджеров 2 (открытый C++ DirectX 9) на Rust WASM с помощью Claude Code + Codex. Делается для теста способностей текущих LLM. **Killer-quote:** «Я не знаю Rust, но знаю плюсы, поэтому могу читать оригинал». **Я не бог линала и с 3D графикой плотно до этого не работал**. Уже работает: загрузка ресурсов, ландшафт, текстуры, вода, небо, статические/анимированные объекты. **«В одиночку они не вытягивают»** — Claude Code + Codex обязательны вместе. | `evolving/content-trends/ai-solopreneur-narrative-hooks` (добавляется hook **«я не знаю X, но знаю Y, поэтому могу читать»** — мостовой паттерн для языковых barrier'ов через AI). |
| 3855 | 2026-04-22 | AI/ML дайджест W13–19 апр (продолжение). **NEW не-в-existing-page:** **NVIDIA Lyra 2.0** — генератор 3D-миров из одной картинки, видеопрогулка → 3D Gaussian Splats, 14B на базе WAN-14B, 32x H100 трен, цель — Isaac Sim для роботов; **Nucleus Image** — sparse MoE диффузия (первая по словам авторов), **17B total / ~2B active, 64 эксперта** в MoE-слоях, 32-layer DiT, текстовый энкодер Qwen3-VL-8B, VAE от Qwen-Image, 1.5B пар картинка-текст, влезет в 16GB VRAM. | `volatile-strict/industry-news/ai-model-releases-mar-apr-2026` (extend Q2 add-on с Lyra 2.0 + Nucleus Image). |
| 3860 | 2026-04-30 | AI/ML дайджест W20–26 апр (NEW deltas). **GPT Image 2:** API id `gpt-image-2`, +**61 пунктов Elo** к второму месту (исторический отрыв на Image Arena), output **$30/1M токенов**, input-картинки **$8/1M**, кэш **$2/1M** (≈$0.04 за 1024×1024 high). **DeepSeek V4** архитектурные детали: **CSA (Compressed Sparse Attention)** + **HCA (Heavily Compressed Attention)** в чередующихся слоях, **pretraining 32–33T токенов**, post-train method **«N специалистов под домены (math/code/agents/IF) → distill в одну»**, IMOAnswerBench **89.8** (vs 75.3 у Opus 4.6, 81.0 у Gemini 3.1 Pro), Codeforces **3206**. **Kimi K2.6** новые детали: нативный **int4**, открытые веса под Modified MIT (для не-крупных корпораций — обычный MIT), GPQA **90.5%**, BrowseComp **83.2**, Terminal-Bench 2.0 **66.7**, **Agent Swarm 100→300 саб-агентов и до 4000 координированных шагов, кодинг-сессии до 13 часов**, нативный видео-вход (mp4/mov/avi/webm до 2K), $0.95/$4.00, кэш $0.16, 256K контекст. **Google DeepMind Gemini Robotics-ER 1.6** — VLM-мозг для роботов, **точность чтения приборов выросла с 23% (старые) до 93% при включении агентного слоя зрения** (давление, температура, цифровые индикаторы); 67% у Gemini 3.0 Flash без агентного слоя. ER = reasoning-слой, моторика — у VLA-моделей. | `volatile-strict/industry-news/ai-model-releases-mar-apr-2026` (extend Q2 add-on с DeepSeek V4 architecture detail, Kimi K2.6 agent swarm specs, GPT Image 2 pricing, Gemini Robotics-ER 1.6). |
| 3862 | 2026-05-04 | AI/ML дайджест W27–04 мая. **xAI Grok 4.3:** AAII **53** (vs 60 GPT-5.5, 57 Opus 4.7), **110 t/s** (быстрее всего фронтира), **$1.25/$2.50** (≈DeepSeek tier, не Opus), **1M контекст**, нативный видео-вход, на SWE-bench отстаёт от Opus 4.7 ~14пп, на агентских задачах (GDPval-AA) обогнал GPT-5.4 + Gemini 3.1 Pro Preview, reasoning всегда вкл, **TTFT 31с**. **Meta Sapiens2** — семейство ViT 0.1B–5B на **Humans-1B** (1 млрд размеченных людей), 5 задач: pose **308 точек**, сегментация **29 классов**, surface normals, pointmap, albedo. Нативное **1024×768**, 4K через windowed attention, уже в ComfyUI. **Netflix Eyeline Vista4D** — перетащи камеру в любой ракурс уже снятой сцены без пересъёмок, **77% blind preference vs ReCamMaster/CamCloneMaster**, **720p, 49 кадров**. **Talkie 1930** — 13B модель, **260B токенов до 1930 года** (US public domain). К лету обещают уровень GPT-3. **Pine AI Incompressible Knowledge Probes** — метод оценки размера проприетарных моделей через объём сохранённых фактов (граница сжатия информации), калибровка на 89 открытых моделях с **R²=0.917**. Получили: GPT-5.5 ≈ **9.7T параметров**, Claude Opus 4.6 ≈ **5.3T параметров**. **VR-Outpaint LoRA** — расширяет видео в 360° для VR. **Sync дубляж** = их липсинк + перевод + voice-clone в однокнопочный пайплайн. | `volatile-strict/industry-news/ai-model-releases-mar-apr-2026` (extend Q2 add-on с Grok 4.3 detail, Sapiens2, Vista4D, Talkie 1930 как research-curio, Pine AI Probes как новый model-sizing метод, VR-Outpaint, Sync dubbing). |
| 3852 | 2026-04-20 | CayleyPy серия Kaggle-челленджей по сборке Мегаминкса/кубика 3×3×3/4×4×4 (научный проект МФТИ + Илья Осокин). Призовой фонд > 100K ₽, NIPS spotlight за CayleyPy. **Не идёт в слой** — академический ML-кейс, низкая marketing-релевантность. Audit-log only. | — |
| 3854 | 2026-04-21 | Нео-банк PLATA — Series C, оценка **$5B**, активные найм. ML/AI-роли: Senior DS Risk (кредитный скоринг, GNN в проде), ML Engineer Middle+/Senior (ASR, TTS, OCR, DL-зоопарк), AI Engineer Middle+/Senior (LLM-агенты, RAG, A/B). Вилки от **$6K/мес gross**. Локации: Мексика, Сербия, Казахстан, Барселона, Кипр, Remote. **Слабая marketing-релевантность** — рынок hiring AI-talent с RU-локацией, бенчмарк зарплат, но не наша ЦА (DS-инженеры — не GRO-сегмент). Audit-log only. | — |

**Нерелевантные новые посты** (только в audit log):
- 3848 KillBench whitecircle.ai — политический мем про bias моделей (тут Grok ненавидит китайцев, etc.). Off-topic для marketing.
- 3856 «Кто плохо кодит — переродится в Opus 4.7 и будет строить килотонны бесполезного софта» — AI-мем.
- 3857 «Мы русские, с нами клод» — мем.
- 3858 «С LLM: не доверяй, но проверять лень» — AI-цитата, но не уникальная (общеизвестный риторический паттерн).
- 3859 «Не попал в Forbes 30U30 — придётся найти свой путь в тюрьму самостоятельно» — комедия.
- 3861 PyTorch Lightning supply chain attack — infosec.
- 3863 «Не стоило добавлять фейри в борщ» — мем.

## Ключевые идеи

1. **Q2 темп фронтир-релизов = 1 крупный/неделю.** За 6 недель (16 апр – 4 мая) Боря зафиксировал: Opus 4.7, Qwen 3.6 35B, Grok 4.3, GPT-5.5, GPT Image 2, DeepSeek V4 (Pro 1.6T + Flash 284B), Kimi K2.6, Gemini Robotics-ER 1.6, Meta Sapiens2, Netflix Vista4D. Это полностью консистентно с фоном из [[sources/2026-05-05-tg-ai-newz-apr-may-2026|@ai_newz]] и второй атестацией укрепляет [[evolving/industry-trends/ai-solopreneurship-window-2026-2029|нарратив окна соло-фаундера]] — каждые 2–3 недели появляется новый базовый блок.

2. **Anthropic Opus 4.7 token-overhead caveat.** Цейтлин — единственный из ингестируемых каналов, кто явно обращает внимание на нюанс **«токенизатор оптимизирован, но выдаёт 1.0–1.35× больше токенов в зависимости от content type»**. Это сильный operational signal для подписочной экономики Claude — реальное удорожание подписки на 0–35% при том же ценнике. **Применимо для постов GRO** про «как считать стоимость AI-подписки» / «гэп между ценой и реальным потреблением». `[conf:medium, src:2026-04-16]`

3. **Founder dev-tooling pet projects = новый формат контента.** Цейтлин публично выкатывает **ULTRAPACK** (Claude Code skill pack, 27 ⭐, чистый README в стиле «5 маркдаун файлов = пет-проект 2026») и параллельно ведёт **MatrixGame WASM port** (Cosmic Rangers 2 на Rust WASM, тест способностей LLM). Оба — не продукты, а **публичные dev-журналы**, которые Цейтлин использует как контент-актив для канала. Это — новый паттерн для GRO content-trends: founder публикует свой dev-stack как content (в дополнение к существующему [[evolving/content-trends/your-pet-project-channel-hooks|Табунов-формату]] case-study).

4. **Pine AI Knowledge Probes — новый метод оценки размера проприетарных моделей.** Не через benchmarks или цену, а через **«потолок сжатия знаний»**: моделей оценивают по объёму памятных фактов (R²=0.917 на 89 открытых моделях). Полезно для маркетинговых нарративов, где нужно сослаться на «реальный размер» Closed-source моделей: GPT-5.5 ≈ 9.7T, Claude Opus 4.6 ≈ 5.3T `[conf:low, src:2026-05-04]` (метод новый, верификация ограничена).

5. **Re-export overhead = рабочая операционная характеристика backfill-планировщика.** Этот ingest показал, что 68% дампа (34 из 50) — overlap с предыдущим ingest-ом за 3 недели до. Это известный side-effect TG-export-инструмента — он не помнит high-watermark предыдущего пробега и пагинирует от текущего момента назад до фиксированного лимита. Для очереди ingest-а это означает: **бóльшая часть бюджета ingest-сессии тратится на de-duplication, а не на новые факты**. Возможный architectural-fix — wiki-prepare-уровневая дедупликация по message-id'ам (вне scope этого ingest-а, фиксируется как наблюдение).

## Факты и цифры

<!-- Числа с inline-маркерами — страница sources/ это evolving-layer audit, числовой синтез идёт в `volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md` -->

**Самые цитируемые бенчмарки нового периода:**
- **DeepSeek V4 Pro:** 1.6T total / 49B active, 384 экспертов, IMOAnswerBench **89.8** (vs 75.3 Opus 4.6, 81.0 Gemini 3.1 Pro), Codeforces **3206**, $1.74/$3.48 за 1M токенов `[conf:medium, src:2026-04-30]`
- **Kimi K2.6:** 1T MoE, 32B active, 384 экспертов, Agent Swarm **100→300 саб-агентов**, до **4000 координированных шагов**, кодинг-сессии до **13 часов**, $0.95/$4.00 `[conf:medium, src:2026-04-30]`
- **GPT Image 2:** Image Arena Elo 1333, **+61 пункт Elo** к второму месту (рекорд отрыва) `[conf:medium, src:2026-04-30]`
- **Gemini Robotics-ER 1.6:** чтение приборов **23%→93%** с агентным слоем зрения, 67% у Gemini 3.0 Flash без него `[conf:medium, src:2026-04-30]`
- **Grok 4.3:** AAII 53, **110 t/s**, **$1.25/$2.50**, TTFT **31с**, на агентских задачах GDPval-AA обогнал GPT-5.4 + Gemini 3.1 Pro `[conf:medium, src:2026-05-04]`
- **Pine AI Knowledge Probes:** R²=**0.917** на 89 открытых моделях; GPT-5.5 ≈ **9.7T**, Opus 4.6 ≈ **5.3T** `[conf:low, src:2026-05-04]`

**Anthropic Opus 4.7 — operational deltas:**
- Image res >3× для Claude Design `[conf:medium, src:2026-04-16]`
- `/ultrareview` $5–$20 за раз, 3 бесплатных `[conf:medium, src:2026-04-16]`
- Tokenizer 1.0–1.35× больше токенов на тот же контент `[conf:medium, src:2026-04-16]`
- xhigh уровень — теперь default вместо medium `[conf:medium, src:2026-04-16]`

## Распознанный текст

OCR относится только к новой доли вложений (3848–3863). Большинство — заглушки header-картинок (Anthropic, Google, etc.) или мемы; OCR-ценность низкая. Содержательные:

- **3833 (re-export, уже OCR'или в предыдущем дампе) — но добавляется новая деталь.** Подпись на ТАСС-картинке: «Т-технологии ежегодно инвестируют **до 700 млн рублей** в прикладные исследования» — ранее в `2026-04-14-tg-boris-again-mar-apr-2026` была отмечена цитата Цыганова без числа. Уточнение из OCR заголовка картинки → добавляется в [[evolving/industry-trends/ru-vertical-ai-signals-2026|Сигнал 3]] supersession-update.
- **3850 — Claude Code v2.1.111 / Opus 4.7 (1M context) with xhigh / D:\\git\\lingtrain / Welcome to Opus 4.7 xhigh!** Скриншот терминала после установки модели. Подтверждает версию (4.7 + xhigh + 1M context default) и формальную доступность.
- **3851 — github.com/btseytlin/ultrapack:** 2 Contributors, 0 Issues, **27 ⭐**, **5 forks**. Сорсный snapshot для метрики «founder dev-pet-project уровня viral».
- Остальные новые медиа (3848 killbench-скриншот, 3852 промо CayleyPy/RYBE/BLASTIM, 3853 MatrixGame screenshot, 3861 PyTorch-Lightning supply-chain-картинка) — низкая marketing-ценность.

## Связанные страницы

- [[sources/2026-04-14-tg-boris-again-mar-apr-2026]] — предыдущий boris_again дамп (3798–3847), частично перекрывает этот (3814–3847 = 100% дубль)
- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — основное место для дайджестных извлечений (3855/3860/3862 → Q2 add-on extension)
- [[sources/2026-05-05-tg-ai-newz-apr-may-2026]] — параллельный AI-новостной канал, second-source attestation для Q2-релизов
- [[evolving/content-trends/ai-solopreneur-narrative-hooks]] — расширяется hook-ами 3851 ULTRAPACK и 3853 MatrixGame
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — Q2 темп релизов = непрерывный фон тренда
- [[evolving/industry-trends/ru-vertical-ai-signals-2026]] — Сигнал 3 (Т-Технологии) уточняется числом 700 млн ₽/год через OCR ТАСС-картинки 3833
- [[canon/target-audience/ru-ai-telegram-audience-segments]] — Цейтлин как archetype «Продвинутых», `@boris_again` как медиа этого сегмента
