---
id: mkt:canon/marketing-frameworks/international-launch-monetization-checklist
title: "Pre-launch checklist для международной монетизации (6 уровней подготовки)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [international-expansion, monetization, checklist, localization, payments, jurisdiction, online-business]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-dzen-delovoymir-online-business-monetization-international.md]
namespace: mkt
---

# Pre-launch checklist для международной монетизации

Operational checklist того, **что нужно подготовить до запуска монетизации на международном рынке**. Дополняет стратегический фрейм [[canon/marketing-frameworks/demin-international-expansion-5-pillars|5 основ Демина]] — там «зачем и как мыслить», здесь — «что физически сделать».

**Принцип:** для монетизации за рубежом **недостаточно выбрать модель дохода** (см. [[canon/marketing-frameworks/online-business-monetization-models-taxonomy|таксономию 11 моделей]]). Нужно построить полный operational stack: локализация → продвижение → поддержка → compliance → платежи → логистика. Пропуск любого уровня = блокировка revenue или churn.

**Источник** — редакционная статья «Журнала Деловой мир» (см. [[sources/2026-05-26-dzen-delovoymir-online-business-monetization-international]]), `confidence: medium`. Чеклист — стандартная operational baseline индустрии онлайн-бизнеса (соответствует Stripe Atlas guides, Localization Industry Standards Association, etc.); используется как практический справочник, не как novel insight.

## 6 уровней подготовки

### 1. Локализация сайта и продукта

- **Не перевод, а локализация.** Перевод текста — необходимое, но недостаточное условие. Нужна культурная адаптация: формат дат, валют, единиц измерения, обращения (formal vs informal), визуальные референсы, цветовые ассоциации.
- **Right-to-left языки** (арабский, иврит) требуют redesign UI, не только перевода.
- **CJK-языки** (китайский, японский, корейский) требуют другой типографики, размеров шрифтов, проверки на поддержку всех символов.

См. также [[canon/marketing-frameworks/mentality-driven-localization-andreev|mentality-driven localization (Андреев, Mamba/Badoo)]] — почему дейтинг-сервис в каждой стране должен «играть на местных стереотипах ухаживания», а не быть унифицированным.

### 2. Адаптация продвижения под географию

- **Каналы.** В каждой географии — свой dominant social: VK/Telegram в RU, WhatsApp/Instagram в LatAm/MENA, WeChat/Douyin в China, Line в Japan, KakaoTalk в Korea.
- **SEO-стратегия.** Google в большинстве стран; Yandex в RU; Baidu в China; Naver в Korea; Yahoo в Japan. **Search behavior** различается (длина запроса, intent split).
- **Paid-ads инфраструктура.** Доступ к Meta Ads / Google Ads / TikTok Ads из RU может требовать иностранного юрлица — см. уровень #4.

### 3. Поддержка на других языках

- **Native-speaker support** — не машинный перевод. Churn в первые 30 дней часто driven by «не понимаю, что мне ответили в саппорте».
- **Time-zone coverage.** Если запускаешь на US — нужен support в их рабочее время.
- **Self-service knowledge base** на local-языке снижает нагрузку и улучшает retention.

### 4. Требования зарубежных платформ и юрисдикция

- **App Store / Play Store / RuStore** — каждый имеет свои compliance requirements (privacy policy, age rating, content guidelines, payment processing rules).
- **GDPR / CCPA / China PIPL** — privacy regulations, обязательные при работе с EU/US/China клиентами. Нарушение → штрафы, deplatforming.
- **Регистрация иностранного юрлица** часто требуется для: подключения местных рекламных площадок, открытия Stripe/PayPal, заключения партнёрских договоров, выставления invoices без VAT-проблем. Популярные юрисдикции (со стороны RU-предпринимателей): США (Delaware LLC), Великобритания, Гонконг, Сербия, Китай, ОАЭ.

### 5. Платёжная инфраструктура

- **Эквайринги:** Stripe (US/EU/UK по умолчанию, нужно юрлицо в supported countries), PayPal (исторически универсальнее, но с ограничениями для high-risk verticals), Adyen, Square, локальные acquirers.
- **Мульти-валютные счета:** Wise (бывший TransferWise), Payoneer — для приёма платежей в местной валюте и avoidance forex-потерь.
- **Local payment methods.** В Нидерландах — iDEAL, в Германии — Sofort/Giropay, в Бразилии — Pix/Boleto, в Индии — UPI, в Китае — Alipay/WeChat Pay. Без local methods conversion может упасть в разы.
- **Subscription billing:** Stripe Billing, Chargebee, Recurly — для подписочной модели монетизации (см. модель #2 в [[canon/marketing-frameworks/online-business-monetization-models-taxonomy|таксономии]]).

### 6. Логистика (только для физических товаров)

- Не применимо к ГРО (цифровой продукт), но обязательно для FMCG / D2C / merch.
- Включает: international shipping carriers, customs brokerage, warehousing (3PL), returns processing, fulfillment SLA per geo.

## Связь с моделями монетизации

Каждая модель из [[canon/marketing-frameworks/online-business-monetization-models-taxonomy|таксономии 11 моделей]] имеет свои критические уровни этого чеклиста:

| Модель | Критические уровни checklist'а |
|---|---|
| Subscription (#2) | #1 локализация UI/onboarding, #4 эквайринг с recurring-support, #5 multi-currency billing |
| Freemium (#3) | #1 локализация free-tier, #5 frictionless payment upgrade |
| In-app purchases (#5) | #4 App Store / Play compliance, #5 platform-mandated billing |
| Комиссионная (#6) | #4 KYC/AML compliance в каждой юрисдикции, #5 split-payment infrastructure |
| Рекламная (#7) | #2 ad-network access, #4 GDPR cookie consent |
| Affiliate / CPA (#8/#9) | #4 партнёрские договоры по местному праву, #5 payout infrastructure |

## Связь с другими страницами вики

- [[canon/marketing-frameworks/demin-international-expansion-5-pillars]] — стратегический фрейм международной экспансии (mindset, не operations)
- [[canon/marketing-frameworks/mentality-driven-localization-andreev]] — почему локализация — не перевод (#1)
- [[canon/marketing-frameworks/online-business-monetization-models-taxonomy]] — какую модель монетизировать (этот чеклист — про **как** запустить)
- [[canon/marketing-frameworks/regional-first-retail-expansion-eldorado]] — regional-first как альтернативная стратегия (сначала укрепиться в макрорегионе, потом международная экспансия)
- [[sources/2026-05-26-dzen-delovoymir-online-business-monetization-international]] — source-страница с PR-блоком про Easy Payments как пример сервиса, закрывающего уровни #4 и #5

## Применимость для ГРО

ГРО — цифровое приложение, физическая логистика (#6) не нужна. Критичны:

- **#1 локализация:** при выходе на англоязычный рынок — не только перевод UI, но и культурная адаптация tone-of-voice (RU «дружелюбный эксперт» → EN может потребовать другой регистр) и метафор тренировок.
- **#2 каналы продвижения:** для англоязычного рынка — Meta Ads / Google Ads / Reddit / TikTok / Apple Search Ads вместо VK / Yandex.
- **#4 юрлицо:** регистрация US LLC или UK Ltd для доступа к Apple Developer / Google Play / Stripe без RU-ограничений.
- **#5 платежи:** Stripe + Apple/Google in-app billing (по их правилам — не обходить).

**Order of operations:** обычно #4 (юрлицо) — критический prerequisite для #2 (ads platforms) и #5 (payment processors). Без него остальные уровни блокированы.
