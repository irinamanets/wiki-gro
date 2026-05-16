---
id: mkt:volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026
title: AI-solopreneur case studies — янв–апр 2026 (Табунов digest)
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [ai, solopreneurship, case-studies, agent, saas, mrr, arr, consideration, news]
confidence: medium
stale: false
created: 2026-04-14
updated: 2026-05-06
sources: [sources/2026-04-14-tg-your-pet-project-jan-apr2026.md, sources/2026-05-05-tg-your-pet-project-feb-may-2026.md]
namespace: mkt
---

# AI-solopreneur case studies — январь–апрель 2026

Дайджест 10 публичных кейсов AI-solopreneur-запусков, разобранных Михаилом Табуновым в канале [[sources/2026-04-14-tg-your-pet-project-jan-apr2026|@your_pet_project]] за период январь–апрель 2026. Все цифры — из ретро-разборов автора, не из first-party отчётности компаний; где возможно, Табунов ссылается на публичные источники (NYT для Medvi, GitHub для OpenClaw, Twitter/LinkedIn-посты фаундеров). Этот digest — **не** страница про тренд (тот живёт в [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]) и **не** про content-hooks (те — в [[evolving/content-trends/your-pet-project-channel-hooks]]); он — про operational-цифры конкретных запусков, которые можно использовать как референсы и бенчмарки при позиционировании GRO.

**Почему `volatile-strict`.** Каждая цифра здесь имеет дату поста, и рынок соло-AI-агентов меняется еженедельно (OpenAI покупает OpenClaw, Lovable переходит $200M ARR за полгода, Medvi упирается в NYT + FDA warnings). TTL 14–90 дней — после середины лета 2026 эти кейсы надо либо перепроверять, либо мигрировать в evolving. Inline-маркеры `[conf:*, src:*]` на всех ключевых числах.

## Кейсы (в хронологии постов)

### Lancer — Upwork bidding-agent

- Продукт: AI-агент, который 24/7 мониторит Upwork, фильтрует подходящие заказы, пишет персонализированные отклики и отправляет в первые 10 минут после публикации заказа. `[conf:medium, src:2026-01-16]`
- Фаундер: Иван, владелец агентства MVP Masters, 5 лет заказной разработки. В 2024 году вложил $800 в Upwork → 3 контракта → $240K за 12 месяцев. `[conf:medium, src:2026-01-16]`
- MRR: $10K через 3 месяца после запуска, средний чек $300/мес, 2 фаундера, 0 сотрудников, 0$ на рекламу. `[conf:medium, src:2026-01-16]`
- GTM: беты на друзей → LinkedIn post → партнёрство с «Upwork-экспертами» (которые раньше продавали «аутсорс биддинга») → сам Lancer продавал Lancer через Upwork-профиль «Upwork Bidding». `[conf:medium, src:2026-01-16]`
- Офферы на покупку: $100K–$150K диапазон. `[conf:low, src:2026-01-16]`
- **Killer-механика:** отклик в первые 10 минут vs отклик через 3 часа — «небо и земля» по конверсии.
- Референс для GRO: пример **агента, который конкурирует с фрилансером, не с SaaS-инструментом** — канонический иллюстратор тезиса [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]].

### Phoebe — AI-координатор смен для eldercare

- Продукт: AI-координатор смен для агентств по уходу за пожилыми. Когда сиделка отменяет смену, Phoebe параллельно обзванивает и SMS-ит всех доступных (до 50+ одновременно), находит замену, синхронизирует с системами агентства. Сиделкам не нужно регистрироваться — Phoebe звонит как обычный координатор. `[conf:medium, src:2026-01-30]`
- Фаундеры: Джастин и Дэйв — оба с успешными exits (Justin продал SaaS для Airtable, Dave — healthcare бизнес). `[conf:medium, src:2026-01-30]`
- ARR: $1M за 3.5 месяца, сравнимо с Cursor и Lovable по темпу. Подписано несколько десятков клиентов, высокий чек. `[conf:medium, src:2026-01-30]`
- GTM: outreach на агентства + LinkedIn + YouTube-созвоны с владельцами агентств как референсы. Онбординг вручную, допиливание под пожелания клиентов. `[conf:medium, src:2026-01-30]`
- **Тезис фаундера:** «В эпоху LLM чистый софт — красный океан. Реальная возможность — software-driven services.» `[conf:medium, src:2026-01-30]`
- Референс для GRO: кейс «продукт = рабочий бизнес-процесс, не инструмент» — полностью на стороне agent-vs-saas arbitrage.

### OpenClaw — Personal AI Assistant

- Продукт: AI-ассистент, работающий через уже-установленные мессенджеры (WhatsApp, Telegram, Slack, Discord, iMessage и т.д.), говорит/слушает на macOS/iOS/Android, рендерит интерактивный Canvas. Open source, MIT. `[conf:high, src:2026-02-20]`
- Фаундер: Peter, Австрия, iOS-разработчик. В 2011 сделал PSPDFKit (opensource PDF SDK для iOS/Android), продал в 2021 за $100M+. После выхода на пенсию — выгорание и экзистенциальный кризис. `[conf:medium, src:2026-02-20]`
- Рост: прототип за час → ноябрь 2025 релиз на GitHub → 24 января 2026 = 7800 ⭐ → 26 января = 39800 ⭐ → февраль 200k+ ⭐. 60 дней от анонса до 200k звёзд. `[conf:high, src:2026-02-20]`
- История имени: Anthropic прислал претензию на «Clawd» (слишком похоже на Claude) → ребрендинг в Moltbot → крипто-скамеры захватили освободившийся GitHub-name в 10-секундное окно и запустили фейковый токен $CLAWD с кап $16M → финальное имя OpenClaw. `[conf:high, src:2026-02-20]`
- Exit: офферы от Meta (Цукерберг) + Microsoft (Nadella), финальный оффер от OpenAI принят. `[conf:medium, src:2026-02-20]`
- **Тезис Табунова про причину вирусности (важное наблюдение):** реальные юзкейсы OpenClaw работают плохо (контент = нейрослоп, project management хуже живого PM, обзвоны по базе — очевидно робот с первой фразы). Единственная причина вирусности — интеграция в WhatsApp/Telegram, т.е. **решён вопрос дистрибуции**. `[conf:medium, src:2026-02-20]`
- Референс для GRO: OCR обложки репо (см. source-страницу) подтверждает позиционирование «встроиться туда, где пользователь уже сидит» — применимо к стратегии native-forms [[evolving/content-trends/telegram-native-formats]].
- **Cross-link:** обновляется страница [[evolving/industry-trends/agent-first-world-openclaw-2026]] с этим narrative-fix'ом.

### Lovable — vibecoding full-stack generator (апдейт существующего кейса)

- Фаундер: Antón Osika, Швеция. KTH инженерная физика + прикладная математика → CERN → стартапы → основал Depict.ai (AI-рекомендации для e-commerce). `[conf:high, src:2026-02-27]`
- Путь продукта: вдохновился ChatGPT 4 (2023) → за выходные собрал opensource «GPT Engineer App» → за 2 месяца 50k ⭐ на GitHub → ноябрь 2023 ушёл из Depict → Product Hunt запуск провалился (название «GPT Engineer» = «обёртка над ChatGPT» в восприятии) → переосмысление: интеграция с Supabase (backend одной кнопкой), деплой, auth → ребрендинг в Lovable (от «Minimum Lovable Product» Осики вместо MVP) → перезапуск декабрь 2024. `[conf:high, src:2026-02-27]`
- Revenue timeline (Табунов цитирует):
  - Ноябрь 2024: $100K MRR `[conf:medium, src:2026-02-27]`
  - Декабрь 2024: $350K MRR `[conf:medium, src:2026-02-27]`
  - Февраль 2025: $1M MRR `[conf:medium, src:2026-02-27]`
  - Июль 2025: $10M+ MRR `[conf:medium, src:2026-02-27]`
  - Ноябрь 2025: $20M+ MRR / $200M ARR `[conf:medium, src:2026-02-27]`
- Команда: $10M ARR = 15 чел; $100M ARR = 45 чел; сейчас = 500 чел. Быстрее, чем OpenAI, Cursor и любая другая софтверная компания. `[conf:medium, src:2026-02-27]`
- Юзербейс: 100k+ новых проектов создаётся в день, 25M проектов за первый год. `[conf:medium, src:2026-02-27]`
- Инвестиции: ~$550M привлечено, последний раунд по оценке $6.6B. Прибыли до сих пор нет (всё на токены и зарплаты). `[conf:medium, src:2026-02-27]`
- Pricing: $20–$100/мес + кредиты за AI-генерацию, публикация приложения $20–$50. `[conf:medium, src:2026-02-27]`
- **Важный caveat Табунова:** Lovable — «говногенератор», максимально прячет техническую реализацию. Работает хорошо на простых прототипах, плохо — когда таблиц >3 или внешние API. Пример: Lovable не смог сделать работающий парсер Twitter, потому что не знал, что в бесплатном API нет поиска, хотя сам выбрал этот путь. `[conf:medium, src:2026-02-27]`
- **Тезис:** «Можно быть топовым стартапом, при этом быть плохим бизнесом» — оценка и раунды ≠ прибыль.
- Референс для GRO: anti-pattern для позиционирования («не копируй hype-first модель, копируй unit-economy»).

### Wave AI — оффлайн-транскрибация встреч

- Продукт: приложение для транскрибации и суммаризации аудио, фокус на **оффлайн-встречах** (очные, у врача, интервью, лекции, голосовые заметки) — в противовес конкурентам (Otter, Fireflies, Fathom), которые делали ботов для Zoom. `[conf:medium, src:2026-03-06]`
- Фаундер: Joe (Josh) Morer, ex-глава NY-подразделения Uber. `[conf:medium, src:2026-03-06]`
- Финансы: ARR $7M, 22K платящих, маржа 43% (57% = токены). Команда — 1 человек, 0 инвестиций. `[conf:medium, src:2026-03-06]`
- Timeline: февраль 2024 $100K ARR → август 2024 $2M → конец 2024 $5M → 2026-03 $7M (рост прекратился, рынок перегрелся). `[conf:medium, src:2026-03-06]`
- Траф: Meta Ads + Apple Search Ads. 23 активных креатива на момент поста, >100 за прошлый год. `[conf:medium, src:2026-03-06]`
- **Операционный тезис фаундера:** «Каждый доллар рекламы должен отбиваться. Иначе никак. Начал с маленьких бюджетов, на них всё окупалось, поднимал дальше.» `[conf:medium, src:2026-03-06]`
- **Самоидентификация:** «Это не технологический стартап, это как продуктовый магазин на углу. Просто магазин живёт в интернете.» `[conf:medium, src:2026-03-06]`
- Референс для GRO: **bootstrap-mindset reference** — каждый доллар окупается, один фаундер, только «скучные» каналы трафика. Идеально для objection-handling «у меня нет инвестиций».

### Kleo — AI-автор постов для LinkedIn

- Продукт: парсит LinkedIn-профиль, учит стиль, генерит идеи для контента, заголовки, пишет посты «как ты, а не как ChatGPT», + инфографика. `[conf:medium, src:2026-03-13]`
- Команда: 3 партнёра. Лара (маркетолог, своё агентство + коучинг, 300K+ LinkedIn подписчиков). Джейк (маркетолог, 180K LinkedIn). Кэмерон (CTO, пилит продукт). `[conf:medium, src:2026-03-13]`
- История: Kleo 1.0 — бесплатное Chrome-расширение для анализа чужого LinkedIn-контента, 60K юзеров → LinkedIn прислал cease-and-desist за скрейпинг → расширение удалили → перепилили тех же юзеров в Kleo 2.0 SaaS. `[conf:medium, src:2026-03-13]`
- Launch playbook:
  1. Waitlist (простой ленд).
  2. Прогрев почтой (10+ писем за 4 недели до запуска, писали про решаемую проблему — «почему AI-контент пахнет дерьмом»).
  3. Вебинар на 40 минут в день запуска.
  4. Онбординг вручную, Джейк раздал личный номер юзерам.
- Финансы: $30K MRR за первые 4 дня → $62K MRR за 2 месяца → $150K общей выручки → 1000+ активных подписок. Цель 2026 = $300K MRR + exit. `[conf:medium, src:2026-03-13]`
- Pricing: $100/мес или $999/год. `[conf:medium, src:2026-03-13]`
- **Тезис:** «Повторить этот кейс 1-в-1 нельзя (сотня тысяч подписчиков в LinkedIn нужна). Но собирать базу вокруг одной проблемы — да.»
- Референс для GRO: **content-first GTM reference** — кейс «база подписчиков × waitlist → revenue». Прямо поддерживает нарратив [[canon/marketing-frameworks/retention-benchmarks-b2c|retention-first growth]].

### Sleek.design — AI-дизайнер мобильных UI

- Продукт: описание приложения → AI генерит мокапы экранов за секунды → редактирование через промпт → экспорт в Figma/код. `[conf:medium, src:2026-03-20]`
- Фаундер: Mattia, Full Stack JS-разраб, предыдущие проекты — Reweb (конструктор сайтов), Supadash, Buildshare. Распаковал Reweb под mobile design за 3 недели. `[conf:medium, src:2026-03-20]`
- Финансы: $10K MRR за 6 недель, 0 paid traffic. Тарифы $25 / $50 / $70, жёсткий push на годовую оплату. `[conf:medium, src:2026-03-20]`
- Стек: Next.js, Supabase, Vercel, Stripe, PostHog. `[conf:medium, src:2026-03-20]`
- GTM: Twitter на 8K подписчиков → один пост «We built the fastest way to vibe design mobile apps. From idea to screen designs in under 2 minutes. Export to code or @figma. Comment "sleek" for early access.» → 871k просмотров. Дальше: ежедневные посты, бесплатные генерации для комментаторов, дизайны в сервисе без упоминания инструмента, Instagram-блогеры подхватили бесплатно. `[conf:medium, src:2026-03-20]`
- **Урок о фокусе:** Reweb не рос, потому что «был ок для многих, но не идеален ни для кого» (индихакеры + стартапы + дизайнеры + PMs + агентства). Sleek — узкий аватар = «авторы мобильных приложений без команды». `[conf:medium, src:2026-03-20]`
- **Caveat (важен как cautionary):** дизайн — разовая история, высокий churn, плохо подходит для платного трафа. Плюс Google выкатил аналог на той же неделе. `[conf:medium, src:2026-03-20]`
- Референс для GRO: **focused audience reference** — точечная иллюстрация тезиса «чем уже сегмент, тем легче запуск».

### Youform — Typeform-клон после миграции тарифов

- Продукт: конструктор форм и опросов, позиционируется как «The most affordable Typeform alternative». `[conf:medium, src:2026-03-27]`
- Фаундер: Abhishek, Индия, начал как разработчик в Accenture → стартап → фриланс → параллельно сайд-проекты. До Youform был Botflow (no-code чатботы), продал на Acquire.com за $10K, когда понял что пользователи ищут не чатботы, а замену Typeform. `[conf:medium, src:2026-03-27]`
- Контекст запуска: в сент 2024 Typeform принудительно мигрировал всех на новые тарифы (базовый $29 → 750 ответов → 100; бесплатный 100 → 10; капча от $199). На HN 7+ постов «Typeform was too expensive, so I built my own». `[conf:high, src:2026-03-27]`
- MVP: запустил за неделю. `[conf:medium, src:2026-03-27]`
- Первые 200 юзеров: **вручную через X и Reddit** — вбивал «Typeform», читал жалобы, писал в личку «Слышал, ты на Typeform. Попробуешь мою штуку? То же самое, но дешевле.» `[conf:medium, src:2026-03-27]`
- Партнёрство: Davis, 20K Twitter подписчиков, стал co-founder-amplifier. `[conf:medium, src:2026-03-27]`
- Монетизация timeline: первые 40 дней = lifetime deals ($299 → $399) = $35K за 40 дней → переключение на subscription $29/мес с unlimited tier. `[conf:medium, src:2026-03-27]`
- Product Hunt: #4 продукт дня, 682 апвоута. Комментарий: «Перешли с Typeform и сэкономили $24,000 в год БЕЗ потери эффективности». `[conf:medium, src:2026-03-27]`
- Финансы: 80K зарегистрированных, $18K MRR, 1% конверсия в платящих. `[conf:medium, src:2026-03-27]`
- **Тезис Табунова:** «Продавать то же самое, но дешевле и проще — это лучше, чем выдумывать гениальную идею без конкурентов.»
- Референс для GRO: **price-arbitrage GTM reference** — кейс, иллюстрирующий миф #1 из [[canon/marketing-frameworks/tabunov-landing-anatomy|launch myths]]: «нет конкурентов = нет рынка».

### BeFactor (RU) — накрутка поведенческих факторов в Яндексе

- Продукт: ставишь на комп, софт других участников автоматически ищут твой сайт в Яндексе, заходят, листают страницы, кликают — имитируют живого посетителя. Обменная модель (твоя машина делает то же для других). Всё в обычном Chrome. `[conf:medium, src:2026-04-03]`
- Фаундер: Алексей Блинов, 44 года, Fullstack-разработчик (основная работа — тяжёлые корпоративные системы), образование — защита информации. `[conf:medium, src:2026-04-03]`
- История: с 2011 ковырял Яндекс.Метрику → первый проект RateMeUp (сервис накрутки счётчиков, работает до сих пор) → проекты для YouTube и Instagram → усиление антифрода → BeFactor. Идея пришла после конференции Baltic Digital Days (эксперимент по ручной накрутке ПФ). `[conf:medium, src:2026-04-03]`
- Launch: по базе RateMeUp (150+ человек, каждый третий заинтересовался). `[conf:medium, src:2026-04-03]`
- GTM: пробовали ссылочные биржи, форумы, email, Директ и AdSense — объявления не проходили модерацию. **Главный канал оказался ироничным: сервис раскрутил сам себя в Яндексе**. `[conf:medium, src:2026-04-03]`
- Финансы: 100+ платящих в год, MRR $2–5K. `[conf:medium, src:2026-04-03]`
- Команда: Алексей соло + фрилансеры на разовые задачи. `[conf:medium, src:2026-04-03]`
- **Важно про RU-контекст:** единственный российский кейс в дайджесте. GTM через Директ/AdSense не работает (модерация), через email/форумы — тоже не работает. Осталось: существующая лояльная база + self-promo через собственный же продукт.
- Референс для GRO: **RU-domain bootstrap reference** — RU-solopreneur-кейс, где западные playbook'и не работают из-за регуляторной среды. Полезен как counter-example к «просто залей траф в Meta» (см. пост 585 и [[evolving/industry-trends/ru-telegram-blocking-max-migration-2026]]).

### Medvi — telehealth GLP-1 витрина ($401M solopreneur)

- Продукт: витрина продажи препаратов для похудения (GLP-1, Ozempic-аналоги, в 7 раз дешевле). Вся медицина/врачи/аптеки/доставка/комплаенс переданы CareValidate и OpenLoop Health. Фаундер делает одну вещь — льёт трафик. `[conf:high, src:2026-04-10]`
- Фаундер: Matthew Gallagher, 41 год, вырос в трейлер-парке. В 12 лет начал делать сайты на GeoCities. Первый бизнес — Watch Gang (подписка на часы, $11M выручки за год, 60 сотрудников, не вышла в прибыль). Вынес урок: больше людей = больше костов и медленнее решения. `[conf:high, src:2026-04-10]`
- Запуск Medvi: сентябрь 2024, $20K стартового капитала, 2 месяца на сборку. `[conf:high, src:2026-04-10]`
- Финансы:
  - Месяц 1: 300 клиентов `[conf:medium, src:2026-04-10]`
  - Месяц 2: 1300 клиентов `[conf:medium, src:2026-04-10]`
  - 2025 год: $401M выручки, 250K клиентов, 16.2% прибыли (~$65M) `[conf:high, src:2026-04-10]`
  - План 2026: $1.8B выручки, 15% маржа `[conf:medium, src:2026-04-10]`
- Команда: 2 сотрудника (он и брат). `[conf:high, src:2026-04-10]`
- Сравнение: Hims & Hers (ближайший конкурент) — $2.4B при 2442 сотрудниках, маржа 5.5%. Medvi — 3x маржа при 1200x меньшей команде. `[conf:high, src:2026-04-10]`
- GTM: Meta + Google paid traffic, простые мессаджи «получи рецепт за 5 минут», «одобрение 99%». Широкий аватар (10M американцев уже на GLP-1), высокий чек $179–299/мес. `[conf:medium, src:2026-04-10]`
- Масштаб рекламы: 5K одновременных кампаний в Meta на пике. `[conf:high, src:2026-04-10]`
- AI-стек маркетинга: ChatGPT + Claude + Grok для кода/текстов/лендов, NanoBanana для картинок, Runway для видеокреативов, ElevenLabs для голоса, AI-чатбот на саппорте. `[conf:high, src:2026-04-10]`
- **Dark side (раскопано NYT после публикации):**
  - 1000+ фейковых врачебных аккаунтов в Meta с именами типа «Dr. Tuckr Carlzyn», «Professor Albust Dongledore» `[conf:high, src:2026-04-10]`
  - Фото до/после — deepfake (одно «до» взято из статьи про бросивших пить, с подменённым лицом) `[conf:high, src:2026-04-10]`
  - FDA warning за 6 недель до публикации NYT `[conf:high, src:2026-04-10]`
  - Коллективный иск за спам-рассылки `[conf:high, src:2026-04-10]`
  - Утечка данных OpenLoop Health: 1.6M пациентских записей `[conf:high, src:2026-04-10]`
- Trustpilot: 4.4 из 5 на 11K отзывов. `[conf:medium, src:2026-04-10]`
- Обложка NYT (см. source-страницу): «How A.I. Helped One Man (and His Brother) Build a $1.8 Billion Company. Who needs more than two employees when artificial intelligence can do so many corporate tasks? It's super efficient — and a little bit lonely.»
- **Позиция GRO (важно):** кейс одновременно подтверждает тезис «solopreneur window» и служит **cautionary tale** для positioning GRO. GRO как продукт про **дисциплину и продуктивность** не может ассоциироваться с фейковыми докторами и deepfake-маркетингом. Использовать можно только nuanced hooks: «AI-solopreneur scale возможен, но обратная сторона — компромиссы по качеству и этике» (см. [[evolving/content-trends/your-pet-project-channel-hooks|anti-hooks]]).
- **Cross-link:** обновляется [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] с этим counter-weight.

### Den (RU) — TG-бот для генерации картинок (выпускник практикума Baza)

Добавлено [delta] из второго дампа [[sources/2026-05-05-tg-your-pet-project-feb-may-2026|пост 611, 2026-04-24]]. Это **второй RU-solopreneur кейс** в дайджесте после BeFactor, и **первый RU-кейс с прозрачной paid-traffic экономикой**.

- Продукт: Telegram-бот, генерирует картинки по текстовому описанию. AI-обёртка над нейронкой. `[conf:medium, src:2026-04-24]`
- Фаундер: Ден, Fullstack-разработчик на Ruby on Rails, выпускник практикума Baza Education. До этого — три-четыре запуска (преимущественно B2B SAAS), не окупались / тонули в долгом цикле сделок. `[conf:medium, src:2026-04-24]`
- Финансы (за 2 месяца ноябрь 2025 — февраль 2026):
  - Залито в трафик: $3 000 `[conf:medium, src:2026-04-24]`
  - Выручка: $9 200 `[conf:medium, src:2026-04-24]`
  - Окупаемость трафика: ×3 без учёта токенов `[conf:medium, src:2026-04-24]`
  - Стоимость платящего пользователя: 490 ₽ `[conf:medium, src:2026-04-24]`
  - Пользователи в боте за первый месяц: 32 000 `[conf:medium, src:2026-04-24]`
- Развитие: только на собственно заработанные деньги (zero outside investment). `[conf:medium, src:2026-04-24]`
- Цикл оплаты: 5 минут от входа в бот до конверсии («Зашёл → написал "кот в космосе на скейтборде" → получил картинку → захотел ещё → купил кредитов»). `[conf:medium, src:2026-04-24]`
- Канал трафика: Telegram (через посевы / Telegram Ads). `[conf:medium, src:2026-04-24]`
- **Дисрапция канала:** в феврале 2026 начались массовые блокировки Telegram в РФ → пришлось остановить трафик и переделывать (см. [[evolving/industry-trends/ru-telegram-blocking-max-migration-2026]]). `[conf:medium, src:2026-04-24]`
- **Publisher pivot:** в апреле 2026 команда Baza Education взяла проект на паблишинг — Ден остался на разработке, инвестируют деньги Baza. `[conf:medium, src:2026-04-24]`
- **Параллельный сигнал из image_611** (скриншот ТГ-сообщения от Дена в чате практикума, 2026-02-15): «Я тут на трекинге уже год. Сделал где-то 5 запусков `[conf:high, src:2026-02-15]`. Последний запуск 1 ноября `[conf:high, src:2026-02-15]`. Генератор картинок (ссылку не дам), за последние 30 дней чууть до 1k usd `[conf:high, src:2026-02-15]` не дотянула прибыль.» Реакции: 🔥25 👍8 ❤️3 `[conf:high, src:2026-02-15]`. Это даёт **profit-vs-revenue** контраст: $9.2K revenue / 2 мес = ~$4.6K/мес revenue `[conf:high, src:2026-02-15]`, но «чуть до $1K не дотянула прибыль» за один из тех месяцев → margin ~20% `[conf:medium, src:2026-02-15]`. Соответствует AI-обёртке (50-70% маржа теоретически `[conf:low, src:2026-02-15]`, но за вычетом трафика, эквайринга, комиссий — 20% реально `[conf:low, src:2026-02-15]`).

**Тезис Табунова про Den's case:**
- «Простой бот-обёртка над нейронкой. Идея, которую ты уже видел. Разработка — пару недель. Запуск — ещё пара-тройка недель на калибровку трафика.» `[conf:medium, src:2026-04-24]`
- «Не гениальная идея. Не прорыв. Не стартап-мечта. Просто человек, который взял понятный продукт на растущем рынке и научился покупать трафик.» `[conf:medium, src:2026-04-24]`
- «Это не удача и случайность, а последовательная работа.» — четвёртый запуск удачный после трёх неудачных. Отлично резонирует с paths/learn-loops нарративом GRO. `[conf:medium, src:2026-04-24]`

**Референс для GRO:** **четвёртый запуск как успех после трёх неудач** — резонансный hook для GRO-аудитории «целеустремлённые, готовые к продолжительной работе». Прямо ложится в [[canon/target-audience/ru-smb-founder-owner-seller]] и [[evolving/content-trends/your-pet-project-channel-hooks]] (новый под-секция «multi-launch persistence»).

## Агрегированные выводы

### Общие паттерны всех 10 кейсов

1. **Высокий чек или высокий объём.** Минимум $29/мес (Youform), максимум $179–299/мес (Medvi). Все, кто ниже $20, — кейс LLM-обёрток (Telegram bots), где объём компенсирует низкий чек.
2. **Узкий сегмент / широкий аватар.** Работают обе стратегии, но в разных условиях:
   - Узкий сегмент: Sleek (авторы мобильных приложений), Phoebe (eldercare agencies), Lancer (Upwork-фрилансеры), Kleo (LinkedIn-блогеры).
   - Широкий аватар: Medvi (10M GLP-1 юзеров), Lovable (vibecoding для всех).
3. **Manual first 100.** Везде первые юзеры получены вручную — Twitter-DM (Youform), email-рассылка по waitlist (Kleo), существующая база (BeFactor), bounce через audience founder'а (Lovable/Sleek/Wave AI).
4. **Traffic > product.** Wave AI и Medvi прямо говорят: «Делаю одну вещь — лью траф». Команда ≤2, 80% времени в маркетинге. `[conf:medium, src:2026-04-14]`
5. **Exit через content, не через PR-события.** Никто не ждал Product Hunt, никто не ходил в VC (кроме Lovable, и это привело к $550M инвестиций при нулевой прибыли — хорошо для хайпа, плохо для бизнеса).

### Cross-refs

- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — большой тренд, куда этот digest добавляет quantitative anchors.
- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] — framework, который эти кейсы иллюстрируют.
- [[canon/marketing-frameworks/tabunov-landing-anatomy]] — большинство кейсов прошли через этот ленд-паттерн.
- [[canon/marketing-frameworks/retention-benchmarks-b2c]] — все успешные кейсы имеют retention выше canon-порогов.
- [[evolving/content-trends/your-pet-project-channel-hooks]] — сестринская hooks-страница из того же источника.
- [[evolving/industry-trends/agent-first-world-openclaw-2026]] — OpenClaw detail-addendum с Табуновской narrative-коррекцией.

## Связанные страницы
- [[sources/2026-04-14-tg-your-pet-project-jan-apr2026]]
- [[canon/positioning/gro-value-proposition]]
- [[canon/target-audience/gro-segments]]
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]
- [[evolving/industry-trends/agent-first-world-openclaw-2026]]
- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]]
- [[canon/marketing-frameworks/retention-benchmarks-b2c]]
- [[evolving/content-trends/your-pet-project-channel-hooks]]

## Backlinks

_16 pages link to this one._

- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]]
- [[canon/marketing-frameworks/blue-ocean-strategy-anti-pattern]]
- [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]]
- [[canon/marketing-frameworks/tabunov-landing-anatomy]]
- [[canon/marketing-frameworks/zero-to-one-vs-scale-tabunov]]
- [[evolving-strict/competitor-metrics/glority-global-paint-by-numbers-publisher]]
- [[evolving-strict/market-data/solopreneur-boom-indicators-2026-q2]]
- [[evolving/content-trends/career-audience-hooks-2026]]
- [[evolving/content-trends/visotsky-ai-personal-assistant-narratives]]
- [[evolving/content-trends/your-pet-project-channel-hooks]]
- [[evolving/industry-trends/agent-first-world-openclaw-2026]]
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]
- [[index]]
- [[sources/2026-04-14-tg-your-pet-project-jan-apr2026]]
- [[sources/2026-05-05-tg-alexander-visotsky-apr-may-2026]]
- [[sources/2026-05-05-tg-your-pet-project-feb-may-2026]]
