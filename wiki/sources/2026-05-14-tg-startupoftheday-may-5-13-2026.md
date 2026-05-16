---
id: mkt:sources/2026-05-14-tg-startupoftheday-may-5-13-2026
title: "Telegram @startupoftheday (Александр Горный) — 15 постов 5–13 мая 2026 (5053–5067)"
type: source
layer: evolving
theme: content-trends
tags: [telegram, startupoftheday, gorny, daily-digest, venture, b2b-sales, llm-bots, fake-reviews, dadata, ai-matchmaking, kelluu, neato, ilant]
confidence: medium
created: 2026-05-14
updated: 2026-05-14
original: raw/processed/articles/tg_startupoftheday_20260514-071623.md
bundle_primary: raw/processed/articles/tg_startupoftheday_20260514-071623.md
bundle_children:
  - raw/processed/video/tg_startupoftheday_5062.mp4
  - raw/processed/media/tg_startupoftheday_5064.jpg
  - raw/processed/media/tg_startupoftheday_5065.jpg
namespace: mkt
---

# Telegram @startupoftheday — 15 постов (2026-05-05 → 2026-05-13)

Четвёртый ingest канала Александра Горного. Дамп охватывает ids 5053..5067 (15 сообщений; пост 5062 — короткое мотивационное видео, поэтому в нумерации 15 ids, а в content-факте 14 текстовых + 1 видео + 2 image-attached).

Это **delta-ingest** (нет overlap с предыдущими тремя ingest'ами того же канала: [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]] 4961–5013, [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] 5014–5036, [[sources/2026-05-05-tg-startupoftheday-apr-may-2026]] 4999–5052).

## Метаданные

- **Тип:** Telegram-канал dump (text + 3 media children в bundle: 1 video + 2 jpg)
- **Канал:** [@startupoftheday](https://t.me/startupoftheday) — «Стартап дня» Александра Горного
- **Период:** 2026-05-05 (пост 5053) → 2026-05-13 (пост 5067), 15 сообщений
- **Дата добавления:** 2026-05-14 (backfill scheduled task)
- **Автор:** Александр Горный — ex-директор по стратегии Mail.ru Group, founder ShareAI закрытого клуба, ежедневный VC/startup-обозреватель. Полное bio — см. [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]].
- **Экспертность автора:** inferred (15+ лет VC/startup-аналитики, ex-Mail.ru Group strategy). `confidence: medium` для аналитических тезисов; `confidence: low` для разовых ремарок.
- **Sidecar note:** был — пользователь маркирует канал как «временный контекст для трекинга новостей и трендов. Если есть какие-то релевантные инсайты в другие категории — можно их вычленить». Volatile-first обработка с extraction высокосигнальных hooks/frameworks.
- **Sensitive flag:** none — публичный канал, PII отсутствует.

## Релевантность

Извлечения по 15 постам:

| ID | Дата | Тип | Содержание | Релевантно? |
|---|---|---|---|---|
| 5053 | 05-05 | mmorpg-аудитория quip | «Мужчина 26-40 лет играет в MMORPG ВСЕГО 2-3 часа в день» — Горный ремарка про free-time-asymmetry | low — off-topic, audit only |
| 5054 | 05-06 | foreign startup | Kelluu (Финляндия) — беспилотные дирижабли с водородом для разведки/мониторинга, €15M раунд | low — foreign defense/hardware, weak signal |
| 5055 | 05-06 | author thesis (high) | **LLM-бот в подкаст-студии**: «как клиент я предпочёл бы человека, но меня довели до конца, деньги приняли — а владелец сэкономил зарплату оператора» — фрейм human-vs-LLM-tradeoff для SMB | **high** — готовый thesis для GRO про AI-replacement в SMB |
| 5056 | 05-07 | author thesis (high) | **«Чёрное зеркало» — LLM-агенты усилят самоцензуру**: при выдаче виз/приёме на работу можно прочесть весь архив человека в интернете → люди начнут «осторожнее себя вести в сети» | **medium-high** — готовый contrarian content hook для эпохи AI-агентов |
| 5057 | 05-08 | foreign+RU startup | **Agentsbar** — RU AI-стартап, агенты ищут партнёрства за пользователя; параллель с Wise (genesis на вечеринке → $15B) | **medium-high** — vertical signal: AI agent для networking/matchmaking + готовая Wise-аналогия |
| 5058 | 05-08 | own promo | Курс Claude Code — описание группы участников (100 чел: основатели, директора по развитию, Head of Product) | **medium** — enrich aiacademy page с composition аудитории |
| 5059 | 05-09 | RU startup retro | **QComment** — биржа фейковых отзывов в РФ, 66M «работ», 3–50₽ за отзыв; #субботнийповтор из 2022 | **medium-high** — competitor-news (всё ещё работает после смены домена), data anchor для fake-review-рынка |
| 5060 | 05-10 | author thesis (high) | **«Сравнивать ВВП и капитализацию — признак некомпетентности»** — нельзя складывать flow ($/год) и stock ($) | **high** — каноничная экспертная фрейм-фикс для контента ГРО |
| 5061 | 05-11 | foreign startup (high) | **Neato** — возрождает классический дистрибьюторский слой на Amazon, выкупает у брендов оптом, $25M раунд | **high** — каноничный business-model фреймворк (marketplace-distributor revival) |
| 5062 | 05-12 | video (short) | Видео-мотивашка: «живём не для работы и стартапов» (8 секунд) | irrelevant — мотивационный moment, audit only |
| 5063 | 05-12 | author thesis (high) | **«Холодные рассылки — платить адресату за демо»** — counter-thesis к 1.1% conversion: если платить 500$ за demo-час, voronka улучшится с 10:1 до 30:1, но всё равно окупится | **high** — готовый contrarian B2B-sales content hook |
| 5064 | 05-12 | author thesis + image | **Bubble-chart concentration thesis**: BofA chart «Big Tech 40% S&P 500» как сигнал пузыря — Горный rebuke: «концентрация ложный сигнал кризиса, мир стал монопольнее, и на бирже это нормально» | **medium-high** — counter-bubble thesis + готовый image-anchor (BofA «Peak concentration levels of major bubbles >40%») |
| 5065 | 05-12 | advertorial | **DaData «Бренд по ИНН»** — RU B2B-сервис автоматического enrichment лидов: ИНН → коммерческое название, описание бизнеса (нейросеть), сайт, лого; используется как fuel для AI-сегментации лидов | **medium-high** — RU B2B-sales-data signal + companion для FETE-фреймворка |
| 5066 | 05-13 | foreign startup (low) | **Asto CT** — КТ-сканер для лошадей без наркоза, $27M раунд (270K$ за спасённую лошадь по расчёту Горного) | low — foreign vet/hardware niche, weak signal; audit only |
| 5067 | 05-13 | own promo | Курс Claude Code — старт в субботу 16 мая, 3 блока программы (установка → продвинутые → личная эффективность) | **medium** — enrich aiacademy page программой курса |

**Релевантно (извлечено в слои):**

1. **Горный thesis «LLM-бот в подкаст-студии» (пост 5055)** — фрейм human-vs-LLM tradeoff: «как клиент я предпочёл бы человека, но довели до конца + сэкономили зарплату». Это **готовый контентный insight** для SMB-сегмента: AI-replacement в operations работает даже когда «качество ниже», потому что compensated скоростью/ценой/24/7. → новая страница `canon/marketing-frameworks/llm-bot-customer-tolerance-gorny-frame` (canon, методология выбора между AI и human для SMB).

2. **Горный thesis «Чёрное зеркало — LLM усилит самоцензуру» (пост 5056)** — counter-narrative для AI-эпохи: раньше «компромат теоретически есть, практически никто не пролистает архив», LLM-агенты сделают это рутиной → люди начнут заметно осторожнее себя вести. → новая страница `evolving/content-trends/llm-self-censorship-hook-gorny-2026` (готовый contrarian hook для контента).

3. **Agentsbar (пост 5057)** — RU AI-стартап в категории «AI agent matchmaking для бизнес-партнёрств». 30 активных агентов, без монетизации, ранняя стадия. Параллель с Wise (genesis вечеринки → IPO). → новая страница `volatile-strict/competitor-news/agentsbar-ai-partnership-matchmaking-2026-05` (single sample, но vertical-сигнал).

4. **QComment retro (пост 5059)** — биржа фейковых отзывов в РФ, 66M опубликованных работ, цены 3–50₽ за отзыв, теперь .com домен и крипта-выплаты. Это **RU-specific бенчмарк** на рынке фейк-отзывов, важный для понимания landscape «отзывы как источник доверия». → новая страница `volatile-strict/competitor-news/qcomment-fake-review-market-ru-2026` (vol-strict — с числами + датой источника).

5. **Горный thesis «ВВП vs капитализация» (пост 5060)** — каноничная фрейм-фикс: «ВВП — flow ($/год), капитализация — stock ($); сравнивать как самолёт vs расстояние от Москвы до Питера». → новая страница `canon/marketing-frameworks/gdp-vs-marketcap-flow-stock-distinction-gorny` (canon — стабильная экспертная methodology).

6. **Neato (пост 5061)** — marketplace-distributor revival model. Дистрибьюторы возрождаются как layer **between brand and marketplace**: выкупают у бренда оптом, сами управляют рекламой/ценами на Amazon, выкидывают серых селлеров. $25M раунд → category-validated bet. → новая страница `canon/marketing-frameworks/marketplace-distributor-revival-model-neato` (canon — business-model фреймворк, переносимый на RU-маркетплейсы).

7. **Горный thesis «Платный demo» (пост 5063)** — counter-thesis к стандартному B2B-outbound: вместо «бесплатное demo за 500 баксов от халявщиков» предлагает «платить 500$ адресату за час demo», воронка ухудшится 10:1→30:1, но качество leads резко вырастет. → новая страница `canon/marketing-frameworks/paid-demo-cold-outreach-thesis-gorny` (canon — counterintuitive B2B-методология).

8. **Горный thesis «Концентрация = пузырь» rebuke (пост 5064, изображение BofA chart)** — counter-narrative к bubble-fearmongering на основе «Big Tech 40% S&P»: «мир стал монопольным, концентрация естественна, это не сигнал кризиса». → новая страница `evolving/industry-trends/big-tech-concentration-not-bubble-gorny-2026` (counter-anchor для bubble-discourse).

9. **DaData «Бренд по ИНН» (пост 5065)** — RU B2B sales-enrichment продукт, RU-аналог Clay-стека внутри FETE-фреймворка. → новая страница `evolving/competitor-positioning/dadata-brand-by-inn-ru-sales-enrichment-2026` (RU vertical в B2B-sales-data).

**Updates существующих страниц:**

- [[evolving/competitor-positioning/aiacademy-claude-code-course-gorny-shevchenko-2026]] — finalization-сигналы: composition аудитории (100 чел: founders, директора по развитию, Head of Product), программа из 3 блоков, формат (записанные видео + вебинары), позиционирование «не для вайбкодинга, не для оптимизации промышленного программирования».
- [[canon/marketing-frameworks/fete-outreach-framework-clay]] — добавить DaData «Бренд по ИНН» как RU-локальный инструмент F-этапа (Find/Enrich).

**Нерелевантно (только в audit):**

- **5053 (MMORPG ЦА quip)** — off-topic, авторская шутка про free-time-asymmetry.
- **5054 (Kelluu, дирижабли)** — foreign defense/hardware, без связи с GRO/маркетингом/AI.
- **5062 (видео-мотивашка)** — 8-сек personal moment, без фактуры.
- **5066 (Asto CT, КТ для лошадей)** — foreign vet/hardware niche, single sample, weak signal.

## Медиа-вложения

| ID | Тип | Пост | Содержимое | Релевантность |
|---|---|---|---|---|
| 5062 | mp4 (8 сек) | personal note | Видео: «В начале рабочей недели напоминаю, что живем мы не для работы и даже не для стартапов, есть много других куда более важных дел» | irrelevant |
| 5064 | jpg | Bubble-chart thesis | **BofA chart «Peak concentration levels of major bubbles >40%»** — historic concentrations 1840 Railroads 63%, 1965 Nifty Fifty 40%, 1989 Japan 44%, 2000 Tech & Telecom 41%, 2025 AI Big 10 40% — все «пиковые пузыри» по концентрации. Источник: BofA Global Investment Strategy / Bloomberg. | medium-high — image-anchor для bubble-discussion |
| 5065 | jpg | DaData advertorial | Корпоративная реклама DaData: тёмно-синий фон, лого DaData, заголовок «Сервис "Бренд по ИНН" находит сведения о лидах для B2B-продаж», пример карточки на «HFLabs — российская IT-компания, разрабатывающая решения для повышения качества клиентских данных и master data management с 2005 года» (ИНН 7707545900); легальный disclaimer внизу (ИНН 7721581040, erid 2Vtzqwut8XZ) | medium — companion image для DaData competitor-positioning |

## Транскрипты медиа

### tg_startupoftheday_5062.mp4 (8 сек, мотивашка)

> «В начале рабочей недели напоминаю, что живем мы не для работы и даже не для стартапов, есть много других куда более важных дел.»

Автор: Александр Горный (моноглавая голосовая нота с phone-camera-видео; не извлекается в слои — personal moment).

## Распознанный текст

### tg_startupoftheday_5064.jpg (BofA chart)

**Title:** Chart 13: Peak concentration levels of major bubbles… >40%
**Subtitle:** Concentration in historic bubbles

**Легенда:**
- Railroads, % US stock market (1835–1910)
- Japan, % MSCI ACWI (1981–1994)
- AI Big 10*, % S&P 500 (2019–2025) — выделена голубым highlight
- Nifty Fifty, % S&P 500 (1965–1981)
- Tech & telecom, % S&P 500 (1988–2006)

**Помеченные пики:**
- 63% — Railroads, ~1875
- 40% — Nifty Fifty, ~1972
- 44% — Japan, ~1989
- 41% — Tech & telecom, ~2000
- 40% — AI Big 10, ~2025

**Footer:** Source: BofA Global Investment Strategy, Bloomberg. * AI Big Ten = Magnificent 7 + AVGO, MU, AMD. BofA GLOBAL RESEARCH.

**Содержательно:** chart показывает, что AI-концентрация в S&P 500 уже на уровне исторических «пузырных» пиков (40%, как Tech & telecom 2000 или Nifty Fifty 1972). Используется bubble-believers как сигнал «AI-пузырь готов лопнуть». Горный rebuke (пост 5064): концентрация — естественное следствие монополизации экономики (Walmart 2% → 8% retail US), не сигнал кризиса.

### tg_startupoftheday_5065.jpg (DaData «Бренд по ИНН»)

**Композиция:** корпоративная вертикальная реклама на тёмно-синем (DaData брендовый цвет).

- **Сверху справа:** disclaimer «Реклама. ООО «Дейта Кью», ИНН 7721581040, erid: 2Vtzqwut8XZ»
- **Слева сверху:** красный лейбл «DaData»
- **Заголовок крупно белым:** «Сервис "Бренд по ИНН" находит сведения о лидах для B2B-продаж»
- **Иллюстрация ниже:** карточка-mockup product-page DaData:
  - Слева — вертикальная зелёная плашка: «ИНН 7707545900»
  - Справа — описание: «**HFLabs** — российская IT-компания, разрабатывающая решения для повышения качества клиентских данных и master data management с 2005 года. Основные продукты включают системы для нормализации, обогащения, объединения…» (cut-off в карточке)
- **Стилистика:** B2B SaaS reference-design (corporate blue, white text, screenshot-illustration, ИНН-anchor для credibility). Близко к [[evolving/content-trends/forbes-russia-native-ad-pattern-2026]] и [[evolving/content-trends/vcru-top10-advertorial-pattern-2026]].

## Ключевые идеи

### 1. Горный thesis «LLM-бот в подкаст-студии» (пост 5055)

Реальный кейс автора: бронировал запись через Telegram, «менеджер» оказался LLM-ботом на старой модели, «тупил». **Outcome для бизнеса:** Горный довёл бронь до конца, заплатил, запись сделана; «владелец зарплату оператора экономит, может и конечную стоимость услуги снизил».

**Тезис Горного:**
> «И это в подкаст-студии, не в IT-стартапе каком-то. В интересное время живем.»

Это фрейм **human-vs-LLM tolerance tradeoff**:

- **Customer side:** LLM-бот раздражает («тупил»), но компенсируется (а) мгновенным ответом, (б) **довёл до конца** (key — completion compensates frustration).
- **Owner side:** экономия зарплаты оператора, возможно — снижение конечной цены.
- **Result:** для **operations-задач с low-stakes endpoint** (бронь/билет/выписка) LLM-бот выигрывает у человека по unit-economics, даже если customer experience «ниже».

Это **готовый пост для GRO** про AI-replacement в SMB-operations: «вы беспокоитесь, что AI заменит человеческий сервис. Уже заменил — в подкаст-студиях, парикмахерских, такси. Главное, чтобы доводил клиента до конца».

### 2. Горный thesis «Чёрное зеркало — LLM усилит самоцензуру» (пост 5056)

> «Раньше было так: написал крамольный комментарий, два друга лайкнули, и он навеки потерялся. <…> LLM лениться не будет. При самых рутинных проверках типа выдачи визы или приема на работу можно зарядить агента прочесть всё, что человек в интернете оставил.»

**Тезис Горного:** через пару лет это станет mainstream → люди начнут «заметно осторожнее себя вести в сети».

**Content hook для GRO:** counter-narrative к AI-democratization-tropes («AI даёт каждому суперспособности»). Альтернативный thesis: «AI-агенты дают каждому суперспособность копать чужой архив. И это меняет поведение всех, кто в сети». Готовая площадка для контента про **defensive-posture в AI-эпохе** (без панических интонаций).

### 3. Agentsbar — AI agent matchmaking + Wise-аналогия (пост 5057)

**Agentsbar (RU):**
- AI-агенты ищут партнёрства от имени пользователя в назначенное время
- 30 активных агентов, без монетизации, ранняя стадия
- Основной фокус — co-founder matching для стартаперов
- URL: https://agentsbar.com/

**Wise-аналогия (Горный):**
> «у Wise тоже 14 лет между знакомством на вечеринке и IPO прошло»

Это **counter-anchor к "AI agent matchmaking — слабая монетизация"**: «слабая» monetization при ранней стадии — нормально для networking-продуктов (Wise сейчас 15B$, не сразу). Готовая cross-link для valuations-discussions в AI-vertical.

### 4. QComment — биржа фейковых отзывов RU (пост 5059, #субботнийповтор)

- **66 миллионов «работ»** (опубликованных отзывов) — anchor RU-рынка
- **3₽ за 75 символов** минимум, до 50₽ в сложных случаях
- Заказывать можно ТОЛЬКО комментарии на самого себя, конкурентов поливать грязью запрещено (видимо risk anti-defamation lawsuits)
- **Не работает с Tripadvisor** (лучшая модерация по словам QComment)
- Сменил домен с .ru на .com, ООО продолжает сдавать отчётность; выплаты исполнителям только через крипту

**Контекст:** «трудности с государством» Горный называет, но не uniquely в России — паттерн «fake-review-биржа уходит в .com + крипту-only» характерен для аналогов в US (Fiverr-tier gigs тоже теневые). 66M отзывов = «явно меньше, чем объём честных отзывов в Рунете, но всё же заметная часть массы».

### 5. Горный thesis «ВВП vs капитализация» (пост 5060)

> «Хороший признак некомпетентности — прямое сравнение ВВП и капитализации.»

**Технический разбор:**
- **ВВП = flow:** $/год, $/квартал, $/месяц — все одна и та же величина (скорость производства)
- **Капитализация = stock:** $ (статичная)
- **Можно делить:** capitalization/GDP_ratio имеет смысл (Buffett ratio)
- **Нельзя складывать/вычитать:** «как самолёт быстрее, чем расстояние от Москвы до Питера»

Это **basic финансово-аналитическая дисциплина** + **готовый content-фильтр**: если автор сравнивает A/B-капитализации с C/D-ВВП, он не понимает темы. Применимо к media-criticism и к фактчекингу для GRO-контента.

### 6. Neato — возрождение дистрибьюторов в эпоху маркетплейсов (пост 5061)

**Бизнес-модель Neato:**
- Выкупает товар у бренда оптом (классическая дистрибьюция)
- Сам управляет ценами, рекламой, скидками на Amazon
- Сам выкидывает серых селлеров (если нарушают правила)
- Маржа — традиционная wholesale → retail спред

**Сегмент:** бытовые товары, корма, кухонная утварь, бакалея, косметика, БАДы.

**Сегмент пользователя:** **brand с brand-recognition**, но без отдельного «отдела по Amazon» или с предпочтением подрядчика своим сотрудникам.

**Раунд:** $25M (Series B) — мало для бизнес-модели с heavy inventory, Горный отмечает, что про кредиты на закупку скорее всего не рассказывают прессе.

**Тезис:** **возрождение классической дистрибьюторской модели** на маркетплейсах. Это **canon-уровневый фреймворк** для понимания эволюции ритейла — параллельно к [[canon/marketing-frameworks/grebenyuk-jv-distribution-model]] (RU JV-дистрибьюция). RU-аналоги: пока нет явных, но потенциальная категория для Ozon/Wildberries.

### 7. Горный thesis «Платный demo» для холодного аутрича (пост 5063)

**Базовая воронка холодных рассылок:**
- 500 получателей → 10 demo → 1 контракт → 1M LTV
- Conversion to demo ~2%, to contract ~10% from demo

**Горный counter-thesis:**
> «А вот если бы они предлагали заплатить 500 баксов за участие в демо?»

Для ЛПР в стартапе или VP в корпорации $500 — приятные деньги. Воронка ухудшится с 10:1 до 30:1 (3x регрессия), но **окупится** — конкретно за счёт качества leads (отсев халявщиков).

**Открытый вопрос Горного:** «Почему так никто не делает? Или делает кто-то уже? Или никто не умеет рассылки таргетировать?»

**Это контентный hook для B2B-сегмента**: counter-thesis к 1.1% conversion на cold outbound (см. [[canon/marketing-frameworks/fete-outreach-framework-clay]]). Готовая контр-тема для дискуссии в B2B-Sales-сегменте.

### 8. Горный thesis «Концентрация ≠ пузырь» (пост 5064, BofA chart)

**Bubble-believer thesis:** «Big Tech 40% S&P 500» = повторение Nifty Fifty 1972 (40%), Japan 1989 (44%), Tech&Telecom 2000 (41%) → AI bubble сейчас на peak, готов лопнуть.

**Горный rebuke в 2 шагах:**

1. **Циклически кризиса давно не было** — пора бы, но и перед COVID было пора, и прошло 10 лет без серьёзного кризиса.

2. **Соображения концентрации — ложные.** Мир действительно стал монопольнее:
   - Walmart (крупнейший US retail): 2% доли в 70-х → **8% сейчас**
   - Банки US: ещё сильнее консолидация
   - Естественно, что **на бирже это отражается** — гиганты в реальной экономике становятся гигантами на бирже.

> «Так и должно быть.»

**Это counter-anchor для GRO-content:** альтернативный фрейм к «AI bubble готов лопнуть». Готовое сочетание с [[evolving/industry-trends/ai-energy-bottleneck-debunked-gorny-2026]] — тот же автор, та же логика «counter-FUD-anchor».

### 9. DaData «Бренд по ИНН» — RU B2B sales-enrichment (пост 5065)

**Продукт:**
- Вход — ИНН организации/ИП
- Выход:
  - **Коммерческое название** (например, «Ozon» вместо «ООО „Интернет Решения"»)
  - **Описание бизнеса** (выжимка с сайта, через нейросеть, не ОКВЭД)
  - **Сайт и лого**

**Use cases:**
1. **Sales enrichment:** API-pipeline → CRM автоматически
2. **AI segmentation fuel:** описания компаний используются для обучения нейросетей сегментации лидов и генерации персонализированных писем

**Pricing:** бесплатно для первых 50 юрлиц (lead-magnet).

**Это RU-аналог Apollo/Clearbit для лидов**, специально под российский регистрационный landscape (ИНН-anchor). Прямо вписывается в **F-этап (Find/Enrich)** [[canon/marketing-frameworks/fete-outreach-framework-clay|FETE-фреймворка]].

## Факты и цифры

- **Kelluu (Finland):** €15M раунд, беспилотные дирижабли с водородным двигателем, до 12 ч полёта `[conf:high, src:2026-05-06]`
- **Agentsbar (RU, агенты для networking):** 30 активных агентов, без монетизации `[conf:medium, src:2026-05-08]`
- **Wise (origin):** 14 лет между знакомством на вечеринке и IPO, текущая капитализация $15B `[conf:medium, src:2026-05-08]`
- **QComment:** 66M опубликованных «работ», 3₽–50₽ за отзыв, сменил .ru → .com `[conf:medium, src:2026-05-09]`
- **Курс Claude Code (Горный + Шевченко):** под 100 человек в группе, профиль (основатели, директора, Head of Product) `[conf:medium, src:2026-05-08]`
- **Walmart concentration:** 2% (1970-е) → 8% (2025) US retail market `[conf:medium, src:2026-05-12]`
- **BofA chart peak concentrations:** AI Big 10 — 40% S&P 500 (2025), Railroads — 63% (1875), Nifty Fifty — 40% (1972), Japan — 44% (1989), Tech&Telecom — 41% (2000) `[conf:high, src:2026-05-12]` (источник: BofA Global Investment Strategy / Bloomberg)
- **Neato:** $25M раунд, бизнес-модель — дистрибьютор-resurrection на Amazon `[conf:high, src:2026-05-11]`
- **Asto CT:** $27M раунд, КТ-сканер для лошадей без наркоза, 10K «пациентов» за 11 лет (~270K$ инвестиций за каждую спасённую жизнь) `[conf:medium, src:2026-05-13]`
- **DaData:** бесплатные 50 юрлиц для теста, ООО «Дейта Кью» ИНН 7721581040 `[conf:high, src:2026-05-12]`
- **Cold-outreach voronka anchor:** Горный — 500 → 10 demo → 1 контракт → 1M LTV (baseline для B2B) `[conf:low, src:2026-05-12]`
- **Paid-demo воронка (Горный гипотеза):** регрессия 10:1 → 30:1 при 500$ за час demo `[conf:low, src:2026-05-12]`

## Связанные страницы

### Создаются этим ingest'ом

- [[canon/marketing-frameworks/llm-bot-customer-tolerance-gorny-frame]]
- [[evolving/content-trends/llm-self-censorship-hook-gorny-2026]]
- [[volatile-strict/competitor-news/agentsbar-ai-partnership-matchmaking-2026-05]]
- [[volatile-strict/competitor-news/qcomment-fake-review-market-ru-2026]]
- [[canon/marketing-frameworks/gdp-vs-marketcap-flow-stock-distinction-gorny]]
- [[canon/marketing-frameworks/marketplace-distributor-revival-model-neato]]
- [[canon/marketing-frameworks/paid-demo-cold-outreach-thesis-gorny]]
- [[evolving/industry-trends/big-tech-concentration-not-bubble-gorny-2026]]
- [[evolving/competitor-positioning/dadata-brand-by-inn-ru-sales-enrichment-2026]]

### Обновляются

- [[evolving/competitor-positioning/aiacademy-claude-code-course-gorny-shevchenko-2026]] — composition аудитории, программа 3 блоков, формат
- [[canon/marketing-frameworks/fete-outreach-framework-clay]] — добавить DaData как RU-tool на F-этапе

### Контекст

- [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]] — первый ingest канала
- [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] — второй ingest
- [[sources/2026-05-05-tg-startupoftheday-apr-may-2026]] — третий ingest (overlap-период)
- [[canon/marketing-frameworks/mvp-definition-gorny]] — другой Горный-thesis (canon)
- [[evolving/industry-trends/ai-energy-bottleneck-debunked-gorny-2026]] — паттерн Горный counter-FUD-anchor
- [[evolving/content-trends/invisible-ai-paradox-gorny-hook]] — связанный thesis (Горный, май 2026)
- [[canon/marketing-frameworks/grebenyuk-jv-distribution-model]] — RU параллель Neato-модели (JV-дистрибьюция)
