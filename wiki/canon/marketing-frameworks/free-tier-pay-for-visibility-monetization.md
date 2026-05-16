---
id: mkt:canon/marketing-frameworks/free-tier-pay-for-visibility-monetization
title: "Free-tier + pay-for-visibility — pre-freemium consumer marketplace monetization"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [frameworks, freemium, monetization, consumer-internet, marketplace, two-sided, founder-mental-model, business-model]
confidence: medium
stale: false
created: 2026-05-06
updated: 2026-05-06
sources: [sources/2026-05-05-yt-ilya-solovey-andreev-mamba-badoo-bumble.md]
namespace: mkt
---

# Free-tier + pay-for-visibility monetization

Бизнес-модель **двух-уровневой монетизации consumer-marketplace'a**, в которой:

1. **Базовый функционал бесплатен** для всех пользователей (регистрация, listing, базовый matching).
2. **Платная функция — видимость** (показ в топе, выделение анкеты, приоритет в выдаче, boost'ы).
3. **Монетизация на правой стороне асимметрии**: пользователь платит не за «доступ», а за **выделиться среди других пользователей**.

Канонический исторический case-study — **Мамба (2003)** Андрея Андреева ([[canon-strict/historical-campaigns/andreev-mamba-badoo-bumble-empire-1999-2019|см. полную хронологию]]). Pattern сформирован **до того, как термин «freemium» был популяризован** Wilson'ом в 2006 — это первая RU-реализация и одна из первых глобальных реализаций модели.

`confidence: medium` — pattern сформулирован по одному case-study (Мамба) из вторичного источника ([[sources/2026-05-05-yt-ilya-solovey-andreev-mamba-badoo-bumble|разбор Соловья]]). Структурно перекликается с публично описанными моделями (LinkedIn Premium 2008, Tinder Boost 2015, Avito VIP 2010-х, OnlyFans 2016, Hh.ru paid resume highlight) но не верифицирован против академической литературы по multi-sided platform pricing.

## Pre-condition (когда применим)

Pattern работает когда **на marketplace выполнены ВСЕ три условия**:

1. **Двусторонний рынок с асимметрией внимания**: на одной стороне — много supply (анкеты, объявления, профили, кандидаты), на другой стороне — sparse attention (ограниченное количество ищущих с временем на просмотр). Дейтинг, job-marketplace, classifieds, content platforms.
2. **Self-serve discovery flow**: пользователь сам ищет/просматривает supply (через поиск, swipe, scroll-feed). Это отличается от **algorithmic matching service** (где платформа сама подбирает) — там visibility-purchase ломает trust в алгоритме.
3. **Status-anxiety или urgency на supply-стороне**: пользователь supply-стороны переживает «я один из миллионов» (на дейтинге — про не выделиться; на job-сайтах — про затеряться среди резюме; в classifieds — про не быть найденным). **Visibility-purchase решает status-anxiety**, а не функциональную проблему.

Если хоть одно условие не выполнено — pattern деградирует:

- Без двусторонней асимметрии — visibility-purchase не имеет смысла (некому смотреть).
- При algorithmic matching — visibility-purchase подрывает trust («алгоритм продаётся»).
- Без status-anxiety — supply-сторона не готова платить за visibility (нет внутреннего мотива).

## Шесть структурных характеристик

### 1. Free-tier должен покрывать «полный путь к минимальной победе»

Бесплатный пользователь должен иметь возможность пройти всю воронку до первого «успеха» (на дейтинге — первый match и переписка; на job-сайте — первая отправка резюме). Если free-tier обрезает путь до победы — **conversion на paid не растёт, а decline'ится** (пользователь уходит к конкуренту с полным free-tier).

Андреев в Мамбе: бесплатная регистрация + полная анонимность + поиск + переписка. **SMS-плата только за «топ-видимость» — ОДНА фича**. Остальное free.

### 2. Paid-tier должен решать **status**, не **функциональность**

Если paid-tier разблокирует **функцию** — это уже classic premium model (LinkedIn Pro, Spotify Premium). Это работает, но имеет другие экономики (более низкий conversion, более высокий churn).

Pay-for-visibility model работает на **внутреннем motiv'е status'a**: «я хочу выделиться». Это не функция — это позиция. Микроплатёж ($1-5) приемлем, потому что не это «купить функцию», а **«заявить о себе»**.

### 3. Visibility должна быть **временной**, не permanent

Если купленная visibility — permanent, marketplace заполняется paid'ами навсегда, и `новые` paid'ы перестают видеть upside. Если visibility — на 24h / 1 неделя / pre-event — рынок **обновляется**, и старые paid'ы возвращаются за новой подпиской. Recurring revenue.

Андреев в Мамбе: SMS-платёж = временная видимость на главной. **Каждый раз нужно заново.** Это создаёт **recurring micro-payment loop** ещё до subscription-эры.

### 4. Цена paid-tier — **импульсная**, не размышляемая

SMS-платёж в нулевых = $0.50–$2. Современный аналог — micro-purchase в app store ($0.99–$4.99). **Размер цены — ниже психологического trigger'a «надо подумать»**. Если пользователь начинает считать ROI («стоит ли мне платить $20 за неделю топа?»), conversion падает.

Pattern: **импульс vs размышление**. Visibility — импульс-покупка ("вижу красивую анкету → быстро в топ → она увидит меня").

### 5. Marketplace должен иметь **достаточно critical mass** на supply-стороне

Без critical mass'а supply-стороны нечем выделяться — все анкеты видны и так. Pattern активируется когда:

- На дейтинге — десятки тысяч анкет в каждом городе.
- В job-marketplace — сотни кандидатов на каждую вакансию.
- В classifieds — десятки тысяч объявлений в категории.

Андреев запускал Мамбу на **уже** существующем «деморализованном» рынке RU-дейтинга (там были игроки с paid-моделью), и его free-tier немедленно accumulated 4.5M анкет за 2 года — visibility-моделя стала monetizable, потому что critical mass был.

### 6. Demand-сторона — бесплатно, но **только через time investment**

Demand-сторона (тот, кто ищет) — бесплатно для платформы, потому что это **они сами находятся в позиции «быть найденным»** на следующей итерации (на дейтинге — они тоже хотят быть в топе; на job-сайтах — они тоже хотят выделиться).

Demand-сторона **косвенно платит вниманием** — они тратят время на просмотр paid-выделенного supply'a. Это и есть тот самый **attention asymmetry**, которую monetize'ит Pattern.

## Как Андреев реализовал в Мамбе и Баду

| Аспект | Мамба (2003-2005) | Баду (2006-2014) |
|---|---|---|
| Free-tier | Регистрация, анонимность, поиск, переписка | + соцсеть-механики, постинг, friends |
| Paid-tier | SMS-платёж за «топ» на главной | Credits для boost'ов, видимости в search'е, отправки сообщений нон-friends |
| Цена paid | $0.50-$2 (SMS) | $1-$5 (credits package) |
| Длительность paid | Сессионная (на час-день) | На X показов, expire после use'а |
| Supply critical mass | 4.5M анкет к 2005 | 12M к 2007, 80M к 2010 |
| Recurring loop | Да (новый SMS = новый top) | Да (credits expire → нужны новые) |
| Status-anxiety target | «я не один из миллионов» | «привлекательная анкета в потоке» |

## Pattern в industries за пределами Мамбы

| Industry / Product | Free-tier | Paid-visibility | Год | Pattern fit |
|---|---|---|---|---|
| **Avito (RU classifieds)** | Бесплатное размещение | VIP-объявления, выделение | 2010-е | ✅ canonical |
| **HH.ru (RU job-marketplace)** | Бесплатное резюме | Highlight, поднятие, премиум | 2010-е | ✅ canonical |
| **LinkedIn Premium** | Бесплатный профиль | InMail, Premium badge | 2008+ | ⚠ partial — больше про функцию |
| **Tinder Boost** (post-2015) | Free swipes (limited) | Boost (10× visibility 30 min) | 2015+ | ✅ canonical, прямой потомок Мамбы |
| **OnlyFans Tips** | Free profile | Featured creators, promotional spots | 2016+ | ⚠ adjacent — больше про supply-payout |
| **Etsy Promoted Listings** | Free shop | Pay-per-click promotion | 2010+ | ✅ canonical |
| **Yandex.Direct contextual** | Free search visibility | Paid bid for ad position | 2001+ | ✅ B2B, но та же mechanics |

**Insight**: pattern почти универсален для двусторонних marketplace'ов с supply-attention asymmetry. Tinder Boost — прямой потомок Mамба-механики, проданной 12 лет позже под premium-брендом.

## Anti-patterns

1. **Pay-to-play в 1-stage funnel'e** — если paid-visibility разблокирует функцию (не статус), это deteriorate'ит trust (пример: Tinder Gold/Platinum воспринимается как «pay-to-win», что вызывает backlash в community).
2. **Permanent visibility-purchase** — заполняет marketplace навсегда без recurring revenue. Pattern: всегда временная visibility.
3. **Visibility без critical mass** — на новом рынке без supply нечем выделяться. Pattern неприменим в early-stage marketplace; нужно сначала набрать supply через free-tier.
4. **Высокая цена paid-tier** — выходит из «импульсной» зоны в «размышляемую», conversion падает. Pattern: micro-payments, не subscription'ы.
5. **Algorithmic-matching + visibility-purchase** — пользователь подозревает «алгоритм продаётся», падает trust в core experience. Pattern incompatible с recommendation engine'ами.

## Применимость к GRO

GRO — health/fitness consumer app, не marketplace. Прямой pattern fit ограничен (нет supply-attention asymmetry в health domain'е), но **отдельные принципы переносимы**:

- **Free-tier должен покрывать полный путь к минимальной победе**. У GRO 14-day free trial — это не free-tier, это trial. Если бы был перманентный free-tier (e.g., бесплатный 1 минимальная тренировка/день), pattern Мамбы был бы более релевантен. Question для product team: что такое «free tier с минимальной победой» в health-контексте?
- **Paid-tier через status, не функциональность** — для health app statusный motiv может быть «streak-достижения», «leaderboards», «public profile с прогрессом». GRO такого не делает (community/social — отсутствует), что отличает его от **gamified consumer fitness** apps (Strava, Whoop, Nike Run).
- **Pattern наиболее применим если GRO добавит community/social модуль** — там pay-for-visibility может стать живой моделью (highlight'ы прогресса, badges, premium leaderboard placement). См. [[evolving/industry-trends/whoop-retention-case-2026|Whoop retention case]] как adjacent reference.

Pattern не догма для GRO — больше **референс на adjacent monetization-architectures**, чем prescriptive guideline.

## Связанные страницы

- [[canon-strict/historical-campaigns/andreev-mamba-badoo-bumble-empire-1999-2019]] — canonical case (Мамба 2003)
- [[canon/marketing-frameworks/mentality-driven-localization-andreev]] — соседний pattern из той же истории
- [[canon/marketing-frameworks/distressed-asset-consolidation-playbook]] — соседний RU founder-playbook (industrial vs consumer)
- [[canon-strict/historical-campaigns/samwer-rocket-internet-fast-follower]] — соседний consumer-internet pattern из 2000-х
- [[canon/positioning/gro-value-proposition]] — GRO позиционирование
- [[evolving/industry-trends/whoop-retention-case-2026]] — adjacent consumer-fitness retention reference
- [[sources/2026-05-05-yt-ilya-solovey-andreev-mamba-badoo-bumble]] — первоисточник
