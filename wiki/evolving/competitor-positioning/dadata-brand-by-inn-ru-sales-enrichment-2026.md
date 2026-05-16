---
id: mkt:evolving/competitor-positioning/dadata-brand-by-inn-ru-sales-enrichment-2026
title: "DaData «Бренд по ИНН» — RU B2B sales-enrichment (2026)"
type: page
subtype: competitor
layer: evolving
theme: competitor-positioning
tags: [ru-saas, b2b-sales, lead-enrichment, crm, ai-fueled, inn-database, dadata, fete-framework]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-startupoftheday-may-5-13-2026.md]
namespace: mkt
---

# DaData «Бренд по ИНН» — RU B2B sales-enrichment

Российский B2B-сервис автоматического enrichment лидов: вход — ИНН организации/ИП, выход — коммерческое название, описание бизнеса (нейросеть), сайт, лого. Запущен компанией HFLabs (бренд DaData), показан в advertorial-формате через @startupoftheday (пост 5065, 2026-05-12) — см. [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]].

## Базовые факты

- **Продукт:** «Бренд по ИНН» — суб-продукт платформы DaData (https://dadata.ru/product/find-brand/) `[conf:high, src:2026-05-12]`
- **Компания-производитель:** HFLabs (ИНН 7707545900, основана 2005 — IT-компания, специализируется на data quality и MDM) `[conf:high, src:2026-05-12]`
- **Юр.лицо рекламы:** ООО «Дейта Кью» (ИНН 7721581040, erid 2Vtzqwut8XZ) `[conf:high, src:2026-05-12]`
- **Pricing:** бесплатно для первых 50 юрлиц (lead-magnet) `[conf:high, src:2026-05-12]`
- **Канал promo:** advertorial в @startupoftheday (TG-канал ~50K+ подписчиков, Александр Горный) `[conf:medium, src:2026-05-12]`

## Что делает сервис

### Вход

Список ИНН организаций или ИП (батч-загрузка возможна по API)

### Выход — три ключевых поля для каждого ИНН

1. **Коммерческое название.** «Ozon» вместо «ООО „Интернет Решения"»; «Альфа-Банк» вместо «АО „Альфа-Банк"»
2. **Описание бизнеса.** Выжимка с **сайта компании, через нейросеть**. НЕ формальный код ОКВЭД, а **semantic-описание** того, чем компания реально занимается.
3. **Сайт и лого.** Adjacent visual identity для дальнейшего использования

## Use-cases (по позиционированию продукта)

### Use case 1: Sales-enrichment в CRM

> «Списки контрагентов по API пропускают через сервис, получают подробности и автоматически записывают в CRM. Больше не нужно работать руками: гуглить сайты, копаться в поисковой выдаче, читать и копипастить разделы «О компании».»

**Это direct замена manual research-этапа** в B2B sales-операциях. Sales-rep economy: каждый pre-call research занимает 5–20 минут на один лид; DaData делает это **за ~1 минуту через API**.

### Use case 2: AI-сегментация и персонализация писем (fuel)

> «А еще сервис используют, чтобы обучать нейросетки. Моделям выдают описания компаний из «Бренда по ИНН» — подробности о том, чем занимается бизнес, насколько он крупный, в каких регионах работает. В итоге нейросети точнее сегментируют лидов и составляют персонализированные письма.»

**Это connect-point с [[canon/marketing-frameworks/fete-outreach-framework-clay|FETE-фреймворком]]:**

- **F — Find:** список ИНН из любого источника (Apollo альтернатива, парсинг открытых баз ЕГРЮЛ)
- **E — Enrich:** **здесь DaData встаёт как RU-tool** на этапе AI-enrichment. Аналог Clay (US/EU) для RU-рынка.
- **T — Transform:** LLM-агент использует DaData-описания как **input для персонализации writing**
- **E — Export:** результат в CRM (HubSpot, Salesforce, AmoCRM, Bitrix24)

## Сегмент рынка — где DaData сидит

| Сегмент | Глобальные аналоги | RU-position DaData |
|---|---|---|
| **Company-level intelligence** | Apollo, Clearbit, ZoomInfo | **DaData = lead** (для RU-компаний) |
| **People-level intelligence** | LinkedIn Sales Navigator, Apollo | DaData не покрывает (нет contact-data) |
| **Pure data normalization** | Various (no clear global leader) | DaData — historic core competency (с 2005) |
| **AI-enrichment workflow** | Clay (multi-tool aggregator) | **DaData = component**, не workflow-platform |

**Differentiation:** DaData покрывает **company-level RU-specific data** (на основе официальных ИНН-registry + AI-обогащения). Это **локальный moat**, который global-конкуренты (Apollo) не имеют — они не покрывают RU rich enough.

## Что это значит для GRO

GRO — **consumer fitness app**, не B2B SaaS-сервис. **Прямое product-relevance отсутствует.** Но фрейм работает в:

### Use case 1: corporate-wellness sales (если GRO когда-либо вакантна)

Если GRO будет продавать **corporate-wellness contracts** для HR-отделов крупных компаний, нужно:
- Список потенциальных corporate buyers (ИНН крупных компаний)
- **DaData может дать GRO sales-team:** имена брендов, описание HR-фокуса, размер компании (для приоритизации)

**Conversion projection:** GRO sales-rep тратит 15-20 минут на pre-call research per lead → с DaData = 2-3 минуты. **Productivity 5-8x** на etape enrichment.

### Use case 2: paid-vs-free freemium funnel — паттерн

DaData использует **«бесплатно для первых 50 юрлиц»** — classic paid SaaS free-tier playbook. **Threshold 50 юрлиц** — это:
- Слишком много для one-off testing (forces actual integration)
- Слишком мало для serious sales-operation (creates upgrade-pressure)

Это **smart freemium hook**. GRO как consumer-app использует «14 дней триал». В **B2B-line** GRO (если запустят), DaData-pattern переносим: «бесплатно для первых 50 employees».

### Use case 3: советская «ИНН-anchor» как trust signal

Композиция DaData advertorial (см. распознанный текст в [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]]) использует **ИНН-anchor визуально** как credibility-signal:

- Зелёная плашка с ИНН на каждой mock-карточке («ИНН 7707545900»)
- Это **RU-specific дизайн-pattern** для B2B-product-pages
- Создаёт **ощущение officiality**, что важно для compliance-sensitive industries

GRO не B2B по умолчанию, но если когда-либо будет — **ИНН-anchor визуальный паттерн** в advertorials = ready-to-use.

## Сигнал-уровень

**Single sample**, но **strong signal**:
- HFLabs — established RU IT-компания с 2005 (не fly-by-night)
- Канал promo (@startupoftheday) подтверждает **active marketing push** в B2B-segment Q2 2026
- Vertical (B2B sales-data) — **активно растущая** глобально (Apollo $1B+ ARR, ZoomInfo $1B+ revenue) → RU-equivalent имеет место

**Что мониторить дальше:**
- Conversion на «50 юрлиц free trial» → paid?
- Корпоративные кастомеры?
- Появятся ли direct competitors (HHRetail, OpenCorporates RU, etc.)?

## TTL и retest

`evolving` — через **120 дней** (2026-09-14) проверить:
1. Каковы customer-numbers?
2. Появилась ли direct competition в RU?
3. Удержал ли HFLabs lead-position?
4. Если категория быстро становится crowded → проброс в `evolving/industry-trends/ru-b2b-sales-data-landscape-2026`

## Связанные страницы

- [[canon/marketing-frameworks/fete-outreach-framework-clay]] — companion канон-фрейм (DaData = E-этап RU-tool)
- [[canon/marketing-frameworks/paid-demo-cold-outreach-thesis-gorny]] — companion B2B-sales фрейм (Горный)
- [[canon/marketing-frameworks/sales-crm-minimum-fieldset]] — adjacent (CRM-discipline)
- [[evolving/competitor-positioning/avito-rabota-job-platform-2026]] — adjacent (RU B2B-recruitment platform)
- [[evolving/industry-trends/ai-vertical-services-vc-uplift-2026]] — adjacent (vertical AI services trend)
- [[evolving/content-trends/forbes-russia-native-ad-pattern-2026]] — companion advertorial-pattern (visual design)
- [[evolving/content-trends/vcru-top10-advertorial-pattern-2026]] — companion advertorial-pattern
- [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]] — оригинал (пост 5065 + advertorial image)
