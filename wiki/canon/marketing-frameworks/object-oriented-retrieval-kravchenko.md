---
id: mkt:canon/marketing-frameworks/object-oriented-retrieval-kravchenko
title: "Object-oriented retrieval: LLM ищет не текст, а объекты (Кравченко)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [geo, aeo, ai-search, structured-data, schema-org, json-ld, retrieval, ontology, insight-analytics, kravchenko, inventory-accuracy]
confidence: medium
stale: false
created: 2026-05-18
updated: 2026-05-18
sources: [sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data.md]
namespace: mkt
---

# Object-oriented retrieval: модель ищет объекты, а не текст

Концептуальная рамка, артикулированная Владимиром Кравченко (управляющий партнёр Insight Analytics) в Pressfeed «.Журнал» (май 2026), и операционная производная для маркетинговой работы: продукт без атрибутной структуры — это **узел в графе без связей**, для retrieval-стека LLM он **не существует**.

## Главный тезис

> «Генеративная модель ищет не текст, а объекты: товар, услугу, бренд, локацию. Если продукт не размечен как сущность с атрибутами — ценой, наличием, характеристиками, условиями доставки — для алгоритма он практически не существует.»
>
> — В. Кравченко, Insight Analytics, Pressfeed май 2026

## Почему `canon`

Сама **онтология retrieval'а** (LLM работает с графом сущностей, а не с потоком текста) — это стабильное архитектурное свойство современных LLM-стеков и retrieval-augmented generation (RAG) пайплайнов. Конкретные доли AI-трафика, числа цитируемости и платформенные механизмы — `evolving*` (см. [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]]); сам **принцип, что объект > текст** — concept-уровень.

Связь с [[canon/marketing-frameworks/product-data-as-architecture-pragmatix|product-data-as-architecture]] (Kevin Indig): тот говорит «маркетинг = архитектура данных» — концепт операционного сдвига. Эта страница артикулирует **онтологическое объяснение**, **почему** это так: потому что retrieval-стек видит сущности с атрибутами, а не нарративы.

## Граф сущностей: что нужно прописать

Минимальный объектный профиль продукта для AI-retrieval:

| Сущность | Обязательные атрибуты | Schema.org-якорь |
|---|---|---|
| **Продукт / услуга** | название, описание, категория, цена, наличие, рейтинг | `Product` / `Service` |
| **Бренд** | название, легитимность, связи с продуктами | `Brand` (через `Product/brand`) |
| **Локация** (если релевантно) | адрес, координаты, регион охвата | `Place`, `Organization/address` |
| **Условия предложения** | цена, валюта, доставка, гарантия, возврат | `Offer`, `OfferShippingDetails`, `MerchantReturnPolicy` |
| **Характеристики** | состав, размеры, страна происхождения, сертификаты | `additionalProperty`, `material`, `countryOfOrigin` |
| **Социальный proof** | количество отзывов, средний рейтинг, дата последнего отзыва | `AggregateRating`, `Review` |

**Принцип graph completeness:** продукт = узел; каждый атрибут = ребро. Чем больше валидных рёбер — тем выше шанс попадания в AI-ответ. Узел без рёбер невидим, узел со многими рёбрами **доминирует** в выдаче.

## JSON-LD как преимущественный формат

> «JSON-LD остаётся самым удобным способом передачи структурированных данных. Он не перегружает HTML и позволяет передавать сложные иерархии. В условиях динамических AI-обзоров скорость и чистота передачи данных становятся конкурентным фактором.»

Operational приоритизация по форматам разметки:

| Формат | AI-retrieval приоритет | Когда выбирать |
|---|---|---|
| **JSON-LD в `<head>`** | **высший** | По умолчанию для всех новых сайтов и при рефакторинге |
| Microdata (HTML inline) | средний | Legacy-страницы, где JSON-LD сразу не внедрить |
| RDFa | низкий | Редко используется, не оптимален для AI |
| Open Graph | вспомогательный | Дополнение к JSON-LD для соцсетей |

Speed/cleanliness considerations: динамические AI-обзоры (Google AI Overviews, ChatGPT search, Алиса AI) делают **real-time запросы** к продуктовым страницам в момент формирования ответа. Чем чище и быстрее парсится разметка — тем выше шанс быть включённым в ответ.

## Inventory accuracy как relevance criterion

> «ИИ генерирует ответы на основе доступной информации «здесь и сейчас». Если на сайте указано наличие товара, которого уже нет, модель фиксирует недостоверность. Актуальность данных становится новым критерием релевантности.»

Новая операционная цепочка (в отличие от классического SEO, где «404» — просто исчезновение из индекса):

1. **Real-time inventory sync** между CMS / ERP / e-commerce backend и JSON-LD-разметкой на странице
2. **AI-агент читает inconsistency**: «in-stock» в Schema vs «sold-out» на странице чекаута
3. **AI помечает домен как недостоверный** для будущих запросов (degradation signal)
4. **Downgrade ranking** не только этой страницы, но **домена целиком** для категории

Это **антифрагильное обоснование** для real-time data pipeline: один незакрытый недоступный товар деградирует видимость **всех** товаров домена. Inventory drift — не операционная мелочь, а **репутационная угроза** в AI-эпохе.

**Practical checklist:**

- [ ] Inventory webhook → JSON-LD regeneration latency < 5 минут
- [ ] Stale-asset detection: ежедневный аудит расхождений Schema vs page state
- [ ] Soft-fallback: при out-of-stock — обновление Schema (`availability: OutOfStock`) до удаления страницы
- [ ] Monitoring: алерт на расхождения наличия между фидом, разметкой и checkout-API

## Архитектурный, не точечный апгрейд

> «Компании нужен не точечный апгрейд, а перестройка инфраструктуры сайта. Генеративный поиск требует машиночитаемой модели данных — на уровне архитектуры, а не отдельных страниц.»

Менеджерская рамка приоритизации:

| Категория работы | Кто отвечает | Бюджетная категория |
|---|---|---|
| **Добавить FAQ-блок в существующий лендинг** | Content / SEO-team | opex (точечный) |
| **Перестроить data-pipeline (CMS → API → JSON-LD endpoint)** | Product / Engineering / Data | **capex** (архитектурный) |
| **Обеспечить inventory real-time sync** | Engineering + DevOps | **capex** (инфраструктура) |
| **Внедрить мониторинг видимости в AI** | Marketing analytics + Data | opex (новый функционал) |

**Operational consequence:** при планировании бюджета GEO/AEO рассматривать в первую очередь как **инфраструктурный проект**, не как content-инициативу. Без архитектурного слоя точечные content-улучшения не дают полного uplift'а (упрётся в неполные данные).

## Кейс-валидация: Faire (платформа B2B-shopping)

**Контекст:** Faire — платформа, соединяющая бренды и независимые магазины (US/EU).

**Что было:** Высокие позиции в обычной выдаче Google, но предложения **не попадали в Google AI Overviews**.

**Аудит выявил:** разметка сайта недостаточно детализирована для генеративного поиска. То, что работает для классического SEO (страничные H-теги, alt-теги, базовый title/meta), не достаточно для AI-retrieval.

**Что сделали:**
- Расширили атрибуты Schema.org (добавили полную онтологию `Product` / `Offer` / `Brand`)
- Перешли на передачу данных **через JSON-LD в режиме реального времени** (не статическая разметка при деплое, а dynamic-endpoint)

**Результат:** **+40% упоминаний Faire в AI-обзорах по коммерческим запросам** `[conf:medium, src:2026-05-18]`.

Это **первая опубликованная цифра uplift'а от структурированных данных на AI-Overviews** в нашей вики. Согласуется с тезисом Шевченко о механизме (3) fine-tuning + search ([[evolving/content-trends/aeo-geo-llm-search-optimization-2026]]) и тезисом PRAGMATIX «продукт с полными данными попадает в рекомендации AI чаще» ([[canon/marketing-frameworks/product-data-as-architecture-pragmatix]]).

## Booking-case (travel vertical, анонимизированный)

**Контекст:** Travel-сегмент (предположительно туристический сервис, по контексту «бронирование»).

**Что сделали:** Адаптация контента + структурирование данных (детали не раскрыты Кравченко).

**Результаты:**
- **+15% конверсии в бронирование** из каналов ИИ-ассистентов `[conf:medium, src:2026-05-18]`
- **+30% цитируемости бренда** в ответах моделей `[conf:medium, src:2026-05-18]`

Интерпретация: 30% — это **awareness/visibility uplift** (модель чаще включает бренд в ответы), 15% — **conversion uplift внутри AI-канала** (после адаптации vs. до). Это **разные метрики**, обе важны: visibility = воронка-вход, conversion = качество landing-experience после клика.

Согласуется с **+38% Adobe Analytics** ([[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]]) — AI-канал даёт более qualified трафик, потому что пользователь уже принял решение после AI-сравнения.

## Связь с GRO

GRO — SaaS-продукт, и большая часть retrieval-объектов для него — это **листинги в App Store / Google Play / RuStore + groapp.ru**:

1. **Объектный профиль приложения:**
   - `Product` = «GRO — приложение для тренировки предпринимательских навыков»
   - `Offer` = subscription model (2 490 ₽/мес, 14-дневный триал) — см. [[canon/product-knowledge/gro-pricing]]
   - `Brand` = GRO
   - `AggregateRating` — текущий рейтинг store'а
   - `additionalProperty` — фичи (4 шага тренировки, мобильное приложение, web, AI-кэйсы)
2. **Inventory accuracy для SaaS:** не «in-stock», но **availability** функций (что включено в Free vs Pro). Если на лендинге одна tier-таблица, а в Schema другая — degradation signal.
3. **JSON-LD на groapp.ru:** проверить наличие `Product/SoftwareApplication` markup с полным набором атрибутов
4. **Architectural play:** связать продуктовую CMS (что обновляется при выпуске нового набора кейсов) с JSON-LD-разметкой → автоматическое обновление атрибутов без ручного редактирования
5. **GRO Intensive (B2B-трек, [[canon/product-knowledge/gro-intensive]]):** B2B-сегмент особенно чувствителен (Gartner 90% к 2028 — см. [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]]). Schema-разметка для cohort-формата: SLA на поддержку, формат интенсива, продолжительность, gar результат / возврат.

## Связь с GEO-monitoring

Object-oriented retrieval **требует** GEO-мониторинга для проверки попадания: классический SERP-rank не отражает, **появляется ли продукт в AI-ответах**. См. [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] — отдельная операционная дисциплина, без которой инвестиции в object-data не измеримы.

## Anti-patterns

1. **Только title + meta-description.** Это уровень SEO 2010-х, в AI-retrieval — невидим (нет графа атрибутов).
2. **Один общий FAQ-блок.** AI-retrieval нужны атрибутные структуры на уровне сущности, не нарратив на уровне страницы. FAQ помогает, но не заменяет product-schema.
3. **Статический JSON-LD при деплое.** Не отражает inventory accuracy. Нужен dynamic endpoint, который генерируется в момент запроса.
4. **Заполнение атрибутов «для галочки» без consistency.** AI читает inconsistency между data sources и downgrade'ит. Лучше меньше атрибутов, но **точных и согласованных**.
5. **Premium-нарратив без machine-readable claims.** «Лучший в категории» без `AggregateRating` или сертификата = пустой signal для AI. Подробнее — [[canon/marketing-frameworks/product-data-as-architecture-pragmatix|premium-pattern]].

## Связанные страницы

- [[canon/marketing-frameworks/product-data-as-architecture-pragmatix]] — концептуальный сосед (Indig: «маркетинг = архитектура данных»); эта страница объясняет **почему** через онтологию retrieval'а
- [[canon/marketing-frameworks/seo-for-ai-era-playbook]] — общий playbook AEO/GEO; здесь — концептуальное обоснование data-приоритета
- [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] — операционная дисциплина измерения видимости в AI-ответах
- [[evolving/industry-trends/ai-search-product-discovery-layer-2026]] — родительский тренд (decision-layer)
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — родительский AEO/GEO-тренд
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — content-playbook AEO/GEO
- [[evolving/content-trends/geo-playbook-2026-q2]] — 6 операционных механик Кумар Виас
- [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]] — Faire +40%, booking +15%/+30% и другие бенчмарки
- [[canon/product-knowledge/gro-app-overview]] — продуктовый обзор GRO (где применять схему)
- [[canon/product-knowledge/gro-pricing]] — ценовая модель GRO (атрибут Offer)
- [[sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data]] — первоисточник
