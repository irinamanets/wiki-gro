---
id: mkt:sources/2026-05-26-tg-startupoftheday-may-20-26-2026
title: "Telegram @startupoftheday (Александр Горный) — 12 постов 20–26 мая 2026 (5076–5087)"
type: source
layer: evolving
theme: content-trends
tags: [telegram, startupoftheday, gorny, daily-digest, venture, spacex-ipo, featherless, squaremind, avanpost, tbank, sponsored-ad]
confidence: medium
created: 2026-05-26
updated: 2026-05-26
original: raw/processed/articles/tg_startupoftheday_20260526-101001.md
bundle_primary: raw/processed/articles/tg_startupoftheday_20260526-101001.md
bundle_children:
  - raw/processed/media/tg_startupoftheday_5078.jpg
  - raw/processed/media/tg_startupoftheday_5079.jpg
  - raw/processed/media/tg_startupoftheday_5083.jpg
  - raw/processed/media/tg_startupoftheday_5084.jpg
  - raw/processed/media/tg_startupoftheday_5086.jpg
namespace: mkt
---

# Telegram @startupoftheday — 12 постов (2026-05-20 → 2026-05-26)

Шестой ingest канала Александра Горного. Дамп охватывает ids 5076..5087 (12 сообщений, из них 2 рекламные интеграции от Т-Бизнес и Avanpost, 1 личный анонс «не я в этой группе», 1 #субботнийповтор 2022 года, 1 #личное про обман инвесторов). 5 медиа-вложений (jpg) → bundle ingest.

Это **delta-ingest** — нет overlap с предыдущими пятью ingest'ами канала: [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]] 4961–5013, [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] 5014–5036, [[sources/2026-05-05-tg-startupoftheday-apr-may-2026]] 4999–5052, [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]] 5053–5067, [[sources/2026-05-22-tg-startupoftheday-may-14-19-2026]] 5068–5075.

## Метаданные

- **Тип:** Telegram-канал dump (text + 5 image attachments → bundle)
- **Канал:** [@startupoftheday](https://t.me/startupoftheday) — «Стартап дня» Александра Горного
- **Период:** 2026-05-20 (пост 5076) → 2026-05-26 (пост 5087), 12 сообщений
- **Дата добавления:** 2026-05-26 (backfill scheduled task)
- **Автор:** Александр Горный — ex-директор по стратегии Mail.ru Group, founder ShareAI закрытого клуба, ежедневный VC/startup-обозреватель. Полное bio — см. [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]].
- **Экспертность автора:** inferred (15+ лет VC/startup-аналитики, ex-Mail.ru Group strategy). `confidence: medium` для аналитических тезисов; `confidence: low` для разовых ремарок.
- **Sidecar note:** был — пользователь маркирует канал как «источник новостей по тематике Бизнес/Предпринимательство, ежедневный разбор стартапа. Используем для написания постов/новостей в блоге; релевантные инсайты в другие категории — вычленять. Временный контекст для трекинга». Volatile-first обработка с extraction высокосигнальных hooks/frameworks.
- **Triage:** verdict `relevant` (Haiku, 2026-05-26) — SpaceX IPO разбор оценки, Featherless API-by-subscription модель, SquareMind 7-летняя commercialization-lag, две sponsored интеграции (Т-Бизнес дизайнерская карта + Avanpost Identity Cloud).
- **Sensitive flag:** none — публичный канал, PII отсутствует. На скриншотах 5083/5084 видны имена/аватарки участников TG-группы — это публичные TG-профили, не приватная PII.

## Релевантность

Извлечения по 12 постам:

| ID | Дата | Тип | Содержание | Релевантно? |
|---|---|---|---|---|
| 5076 | 05-20 | foreign startup + thesis | **SquareMind** (FR/US дермато-робот) — 7 лет разработки, FDA+EU сертификация, $18M раунд, ноль продаж. Тезис «сертификация ≠ commercialization» | **high** — competitor metric + medtech commercialization-lag pattern |
| 5077 | 05-22 | foreign startup + framework | **Featherless** (US AI infra) — 30K моделей под одним API, **API по подписке** ($10/мес, no token billing). $20M раунд. Тезис «API-as-subscription выгоднее metered» | **high** — pricing-model framework + competitor metric |
| 5078 | 05-22 | sponsored ad + image | **Т-Бизнес дизайнерская карта Саша Тито** — лимитированная коллаб, «founder как художник» позиционирование. Маркировка «Реклама. АО ТБанк» | **high** — competitor positioning + sponsored ad format |
| 5079 | 05-22 | sponsored ad + image | (продолжение 5078) фото открытого чемодана с картой | high — часть 5078 паттерна |
| 5080 | 05-24 | RU startup #субботнийповтор 2022 | **Hungry Teams** — RU startup-investor matchmaker, проект умер. Тезис «технология без монетизации = ноль» | **medium** — marketplace failure case (2022 throwback) |
| 5081 | 05-25 | foreign startup + valuation framework | **SpaceX IPO проспект**: $18,5B выручка 2025, $4B opex loss, $20B capex, $80B raise, потенциальная оценка $1-2T. Тезис «покупают не лидера а мечту: Amazon/NVidia было — Uber/Airbnb/Stripe нет». Конгломерат-критика. | **very high** — canon valuation framework + SpaceX competitor metrics + Musk strategy counterpoint |
| 5082 | 05-25 | own-brand warning | Анонс «мошенники сделали группу в мою честь, это не я, жалуйтесь» | **medium** — founder-impersonation defense template |
| 5083 | 05-25 | image | Скриншот TG-группы-импостера «Стартап дня. Александр» с 11260 участниками | **medium** — proof artifact для founder-impersonation pattern |
| 5084 | 05-25 | image | Скриншот профиля fake-группы (Виктор/Akafatalerror/Timur/Gregory Shevchenko с AI-меткой и др.) | medium — proof artifact |
| 5086 | 05-25 | sponsored ad + image | **Avanpost Identity Cloud** — облачная IAM (MFA/SSO/device control), архитектура tenant-isolation, free до 1 сентября. Маркировка «Реклама. ООО Аванпост» | **high** — competitor positioning RU cybersec + sponsored ad format |
| 5087 | 05-26 | #личное | Founder-отрезвление: пять историй когда автор был «обманут» (тестовая трата $250 на исчезнувший сервис, друзья-займы, exit-trick стартапера, начальник, бывшая) | medium — founder-experience hook (без маркетинговой фактуры по сути), audit only |

**Релевантно (извлечено в слои):** 5076, 5077, 5078+5079, 5081, 5082+5083+5084, 5086.

**Нерелевантно (audit only):** 5080 (Hungry Teams — мёртвый 2022 throwback, фактура устарела, тезис «технология ≠ монетизация» уже зафиксирован в canon-фреймах), 5087 (#личное про обманы — не маркетинговая фактура, founder-mindset hook возможен но не уникален).

## Ключевые идеи

### 1. SpaceX IPO — «покупают мечту, а не лидера» (пост 5081)

Самый длинный и сильный аналитический пост дампа. Горный читал проспект SpaceX и выделил пять связанных тезисов:

**(a) Конгломерат-структура.** SpaceX — это **три разные компании** с разной динамикой/рынками/технологиями: Starlink (прибыльный, быстрорастущий, самый большой), xAI = Twitter+AI (чистый стартап), собственно ракетные запуски (стабильно, ~ноль). Слиты только «финансовым гением Маска».

**(b) Опасения комментаторов про убытки переоценены.** $4B операционных потерь + $20B capex за 2025 = огромные деньги (сопоставимы с ВВП Монголии или бюджетом Хорватии), но при привлечении $80B этого хватит на 2-3 года. «Совершенно адекватная ситуация, столько и надо тратить».

**(c) Числовой парадокс.** Выручка SpaceX за 2025 — **$18,5 млрд**. Google делает столько за две недели. Потенциальную оценку триллион-два математикой обосновать **«нельзя никак, совсем никак»**.

**(d) Multiples reference set (canon-вытяжка):** компания должна стоить **порядка 50-100 годовых выручек**. Сравнительные multiples (P/S):
- Историческое среднее NASDAQ — ~3
- Сейчас NASDAQ — ~7
- Google — 11
- Tesla — 16
- Anthropic — ~20
- SpaceX (целевое) — ~100

Это не «много» и даже не «очень много», нужно другое слово.

**(e) Pattern «покупают мечту»:** SpaceX выходит на биржу будучи **чистым стартапом** — обещания (датацентры в космосе, AI-бизнес, Starlink как стандарт связи), не результат. Инвесторы покупают мечту, как было с **Amazon и NVidia**. Так **не было** с Uber/Airbnb. Так **не планируется** со Stripe. → канонический фрейм оценки IPO «дотащить-до-мечты vs. ленивый-кэшфлоу».

**(f) Волатильность post-IPO.** Поскольку математического обоснования нет, всё определяется верой → «лёгкий ветерок сможет в два раза в любую сторону сдвинуть».

Полные framework в [[canon/marketing-frameworks/dream-vs-numbers-valuation-thesis-gorny-spacex]]. Числовые метрики SpaceX в [[evolving-strict/competitor-metrics/spacex-ipo-financials-2025-2026]]. Counterpoint к Маск-vertical-integration в [[canon/marketing-frameworks/dream-to-strategy-musk-vertical-integration]].

### 2. Featherless — API по подписке против metered pricing (пост 5077)

Featherless крутит **30 000 нейросетей** на своих серверах (HuggingFace catalog далеко не весь, но шаг туда), все под одним API-ключом. Цена — **подписка от $10/мес, токены бесплатно**. Защита от злоупотреблений — лимит параллельных запросов. В недавнем раунде привлёк **$20 млн**.

Горный формулирует более широкий тезис, чем просто Featherless как стартап:

> «API по подписке — интересная концепция, может быть, так и надо. В мире вайбкодеров появится много продуктов со смешной нагрузкой, и **$10 в месяц брать с них выгоднее, чем 5 центов за потребление**. Клиент при этом не страдает: он, во-первых, избыточно оптимистичен о перспективах роста своего проекта, а во-вторых, что такое десять долларов, вообще ж не жалко.»

Это компактная теория **pricing-психологии для AI-инфраструктуры vibecoder-эпохи**:

1. **Реальная нагрузка vibecoder-проектов низкая** (большинство умирает на pre-traction стадии).
2. **Анчоринг psychology** — $10/мес «не жалко», даже если по metered получилось бы $0,80.
3. **Founder-optimism premium** — покупатель закладывает рост, который не состоится.
4. **Operational simplicity** — нет квот, нет surprise bills, нет cost-monitoring.

Полный фрейм в [[canon/marketing-frameworks/api-subscription-vs-metered-pricing-featherless-gorny]]. Метрики Featherless в [[evolving-strict/competitor-metrics/featherless-funding-2026]].

### 3. SquareMind — 7-летняя commercialization-lag (пост 5076)

SquareMind — франко-американский медтех-стартап, «фотобудка с роборукой» для скрининга рака кожи. AI составляет body-map по родинкам, врач смотрит готовый результат. Экономика на одной приём в США — экономия **~$100** (высокие зарплаты дерматологов). Если робот стоит $500K (вероятно меньше), окупаемость 2 года.

**Аномалия:** 7 лет разработки, FDA и EU сертификация получены, **ноль продаж**. Свежий раунд $18M — «возможно, убедили фонды что скоро начнут».

Это **второй случай в марте-мае 2026 в этом канале**, когда регуляторно-сертифицированный медтех не продаётся: первый — отдельные кейсы AI-radiology с подтверждённой точностью без adoption. Это становится **observable pattern**: «sertification ≠ commercialization» в медтехе.

Pattern зафиксирован в [[evolving/industry-trends/medtech-commercialization-lag-pattern-2026]]. Метрики SquareMind в [[evolving-strict/competitor-metrics/squaremind-funding-2026]].

### 4. Т-Бизнес лимитированная дизайнерская карта Саши Тито (посты 5078–5079)

**Sponsored ad с маркировкой** (erid: 2SDnjct7bQE, ИНН 7710140679 — АО «ТБанк»). Структура:

1. **Артефакт-hook:** «прислали в очень большом чемодане» — фото алюминиевого premium-кейса с лого «Т-Бизнес» на матовом фоне (dark wood interior).
2. **Reframing «карта = подпись»:** «Кусок пластика — как татуировка, просто знак авторства. Как у художника под картиной, так и у предпринимателя — своя карта».
3. **Founder-pain hook:** «я сам как предприниматель знаю, как рутина выжимает всё вдохновение... Путь к ним лежит только через творчество и развитие».
4. **Solution:** «Занимайтесь тем, что вас захватывает, рутину доверьте Т-Бизнесу».
5. **CTA:** оформить limited business-card с дизайном **Саши Тито** (художник, photo-floral принт), «успейте — тираж ограничен».

Pattern — **founder-as-artist + product-as-signature**, физический premium-артефакт (метал-чемодан) как unboxing-теаsер, артист-collaboration вместо стандартной карты. Реализует **«доверь рутину»** мессадж Т-Банка через эстетический контекст. Это новый sub-pattern T-Bank competitor positioning — `card-as-art-collab`, отличается от T-Premium (sub-brand palette), Доли (BNPL), Дофамин-банкинг (consumer-emotional). Это **B2B (Т-Бизнес)** сегмент, premium-positioning для SMB-founder'ов.

Подробно в [[evolving/competitor-positioning/tbank-business-card-sasha-tito-2026]]. Cross-link в [[evolving/content-trends/founder-channel-sponsored-ad-formats-2026]] как Pattern 5: «artifact-first founder-as-artist sponsored integration».

### 5. Avanpost Identity Cloud — RU Identity-as-a-Service positioning (пост 5086)

**Sponsored ad с маркировкой** (erid: 2VtzqxgN33E, ИНН 7722778473 — ООО «Аванпост»). Целевая аудитория — «компании с высоким риском атак», message-проблема — «80% случаев хакеры обходят базовую двухфакторку (Verizon DBIR)».

**Product positioning:**
- **Avanpost Identity Cloud** — облачный IAM для «безопасного доступа сотрудников и подрядчиков».
- Архитектура: **per-tenant изоляция** (отдельный контур, отдельная БД, отдельные политики), «сравнимая с выделенным on-premise решением, но без затрат на инфраструктуру». Это ключевая дифференциация vs. shared multitenant SaaS-IAM.
- **Access Bridge** — защищённая интеграция с корп-системами с сохранением контроля периметра.
- **Отказоустойчивость** через независимые ЦОД.
- **Офлайн-аутентификация без деградации второго фактора** (roadmap Q3 2026).

**Acquisition tactic:** «до 1 сентября бесплатно для любого числа пользователей, далее тарификация по пользователю, а не блоком». Это **free-trial с deadline + per-user pricing** против корпоративного per-seat-pack — апеллирует к SMB-сегменту.

**Креатив (5086.jpg):** темно-синий gradient + дог-робот на облачках (white BoltAI-like robot dog), «MFA, SSO и контроль устройств в безопасном облаке», orange chip «Тестирование бесплатно до 1 сентября», лого Avanpost × Identity Cloud lockup. Образный tonality — playful (робот-собачка), не industrial-cybersec strict.

Подробно в [[evolving/competitor-positioning/avanpost-identity-cloud-2026]]. Cross-link в [[evolving/content-trends/founder-channel-sponsored-ad-formats-2026]] как Pattern 6: «security-vendor через fear-stat + free-until-deadline».

### 6. Founder-impersonation scam-defense template (посты 5082–5084)

Два поста + два скриншота составляют **готовый micro-format для собственников каналов**:

**Структура (3 элемента):**
1. **Disclosure trigger:** «Пишут, что мошенники сделали новую группу в мою честь. Видимо, скоро будут деньги просить.»
2. **Disclaim ownership:** «Это не я :)»
3. **Defense CTA:** «Нажимайте на спам и жалобу, если вас туда добавили».
4. **Proof artifacts:** два скриншота — (а) общий вид группы «Стартап дня. Александр» с 11 260 участниками и chat-message Александра Горного («Hungry Teams через 4 года» — копипаст текста из самого Горного, замаскированный под оригинал!), (б) профиль группы с participants list.

Замечательный нюанс: **импостер вообще скопировал тот же текст**, который Горный публиковал в собственный канал тем же утром (#субботнийповтор 2022). Это превращает скам-предупреждение в самореферентный proof-of-impersonation.

Pattern в [[evolving/content-trends/founder-impersonation-scam-defense-gorny-2026]]. Применимо в GRO/groapp для @gro_me официальных каналов и личных аккаунтов фаундеров.

## Связанные страницы

**Новые (создаются этим ingest'ом):**
- [[canon/marketing-frameworks/api-subscription-vs-metered-pricing-featherless-gorny]]
- [[canon/marketing-frameworks/dream-vs-numbers-valuation-thesis-gorny-spacex]]
- [[evolving-strict/competitor-metrics/spacex-ipo-financials-2025-2026]]
- [[evolving-strict/competitor-metrics/squaremind-funding-2026]]
- [[evolving-strict/competitor-metrics/featherless-funding-2026]]
- [[evolving/industry-trends/medtech-commercialization-lag-pattern-2026]]
- [[evolving/content-trends/founder-impersonation-scam-defense-gorny-2026]]
- [[evolving/competitor-positioning/tbank-business-card-sasha-tito-2026]]
- [[evolving/competitor-positioning/avanpost-identity-cloud-2026]]

**Обновляются:**
- [[canon/marketing-frameworks/dream-to-strategy-musk-vertical-integration]] — добавлен counterpoint Горного («конгломерат 3 разных компаний, не интегральная стратегия») + SpaceX IPO numbers
- [[evolving/content-trends/founder-channel-sponsored-ad-formats-2026]] — добавлены Pattern 5 (Т-Бизнес artifact-first founder-as-artist) и Pattern 6 (Avanpost fear-stat + free-until-deadline)

**Контекст других Gorny-ingest'ов:**
- [[sources/2026-05-22-tg-startupoftheday-may-14-19-2026]] — предыдущий срез (Mavrck pyramid, Omni semantic-layer, Descript replacement, Ikigai vibecoding)
- [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]]
- [[sources/2026-05-05-tg-startupoftheday-apr-may-2026]]
- [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]]
- [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]]

## Медиа-вложения

| ID | Тип | Назначение | Описание |
|---|---|---|---|
| 5078 | media (jpg, 960×720) | Sponsored ad cover (T-Бизнес) | Алюминиевый premium-кейс с лого «Т Бизнес» на матовой грани, тёмное wood-panel interior, конференц-зал. Маркировка `Реклама. АО «ТБанк». ИНН 7710140679 erid: 2SDnjct7bQE` нижней строкой. |
| 5079 | media (jpg, 720×960) | Sponsored ad reveal | Рука держит дизайнерскую карту с floral-print (Саша Тито) над открытым chemodan-кейсом; внутри ещё carbon-чёрная карта с подписью художника и брошюра. |
| 5083 | media (jpg, 591×1280) | Scam proof artifact #1 | TG-screenshot fake-группы «Стартап дня. Александр» (11 260 участников, 251 онлайн). Видна копия chat-сообщения, мимикрия под оригинал автора. |
| 5084 | media (jpg, 591×1280) | Scam proof artifact #2 | TG-screenshot профиля группы (Чат/Звук/Покинуть кнопки), participant list (Viktor, Akafatalerror, Timur, Виталий Приходько, Anton Rosenberg, Gregory Shevchenko с AI-badge, Александр Буртовой). |
| 5086 | media (jpg, 960×960) | Sponsored ad creative (Avanpost) | Dark-blue gradient sky+clouds фон, white robot-dog character (BoltAI-like, glowing chest accent), header «MFA, SSO и контроль устройств в безопасном облаке», orange chip «Тестирование бесплатно до 1 сентября», лого Avanpost × Identity Cloud. Маркировка `Реклама. ООО «Аванпост» ИНН: 7722778473`. |

## Распознанный текст

OCR/описание включён непосредственно в таблицу «Медиа-вложения» выше; нет отдельных невидимых текстов.
