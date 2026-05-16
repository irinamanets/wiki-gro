---
id: mkt:canon/product-knowledge/gro-app-store-listing
title: GRO — листинг в App Store (iOS, RU)
type: page
subtype: asset
layer: canon
theme: product-knowledge
tags: [product, app-store, ios, distribution, pricing]
confidence: high
stale: false
created: 2026-04-10
updated: 2026-04-10  # third ingest same day (RuStore cross-link)
sources: [sources/2026-04-10-gro-appstore-listing.md, sources/2026-04-10-gro-googleplay-listing.md, sources/2026-04-10-gro-rustore-listing.md]
namespace: mkt
---

# GRO — листинг в App Store (iOS, RU)

Каноническая справка о том, как GRO выглядит в Apple App Store (российская витрина) на 2026-04-10. Это одна из трёх ingested точек дистрибуции продукта; параллельные Android-стороны задокументированы в [[canon/product-knowledge/gro-google-play-listing|Google Play]] и [[canon/product-knowledge/gro-rustore-listing|RuStore]]. Веб-кабинет появится после соответствующего ingest-а.

Задача этой страницы — быть reference-точкой для контент-команды: какая сейчас версия, какой минимум iOS, какие IAP, как продукт там позиционируется и чем подача в App Store отличается от подачи на [[sources/2026-04-10-groapp-landing|лендинге]].

## Техническая конфигурация

- **Bundle ID:** `pro.gro` — единый для всех трёх платформ ([[canon/product-knowledge/gro-google-play-listing|Google Play]] и [[canon/product-knowledge/gro-rustore-listing|RuStore]] используют тот же идентификатор, теперь подтверждено прямым ingest-ом всех трёх сторов).
- **Текущая версия:** **1.6.14** (релиз 2026-03-31).
- **Минимум iOS:** iOS 15.1.
- **Поддерживаемые устройства:** iPhone, iPod touch. Отдельной iPad-оптимизации в листинге нет.
- **Размер установки:** 77,6 МБ (для сравнения, в [[canon/product-knowledge/gro-rustore-listing|RuStore]] APK-сборка весит 49,1 МБ — разница объясняется форматом дистрибутива, не продуктом).
- **Категория в App Store:** Бизнес. Триангуляция по трём сторам: **App Store — Бизнес, Google Play — Стиль жизни / LIFESTYLE, RuStore — Бизнес-сервисы**. Два из трёх стора (Apple и RuStore) выбрали business-вертикаль; только Google Play — lifestyle. Это не противоречие, а реальная разница в том, как команда выбрала категорию в разных сторах. Открытый вопрос к продукт-команде: осознан ли lifestyle-выбор в Google Play? См. [[canon/product-knowledge/gro-rustore-listing]].
- **Языки интерфейса:** русский и английский.
- **Возрастной рейтинг:** 16+.

На контент-уровне это даёт две зацепки:
1. **iOS 15.1+** — устройства 2015 года и новее, покрытие всей активной iOS-базы. В креативах и CPA-кампаниях не нужно оговаривать «требуется свежий iPhone».
2. **Английский в интерфейсе** — уже есть, хотя основной канон продукта (лендинг, testimonials, описание) — русский. Это потенциальный рычаг для глобального outreach'а, но пока без подтверждённого английского позиционирования.

## Провайдер и юрлицо

- **Publisher в App Store:** Romsfort East Advisory Management consultancies LLC.
- **Copyright в карточке:** © ООО "ГРО".

Расхождение между App Store publisher и держателем copyright в РФ — это особенность международной дистрибуции Apple (для RU storefront публикуют через нерезидентное юрлицо). После ingest-а [[canon/product-knowledge/gro-rustore-listing|RuStore]] картина corporate-структуры стала полнее: в RuStore publisher — **непосредственно ООО ГРО**, без посредника, потому что политика VK-стора требует российское юрлицо. То есть команда держит **две параллельные ветки дистрибуции** — Romsfort East (Dubai) под Apple/Google и ООО ГРО под RuStore. Маркетингового смысла по-прежнему не несёт, в контенте эти юрлица не цитировать. Важно помнить при любых упоминаниях «кто стоит за продуктом»: команда и бренд — это [[canon/product-knowledge/gro-team|основатели ГРО]], а не `Romsfort East Advisory` и не абстрактное «ООО ГРО».

## Позиционирование в листинге

App Store-описание даёт **альтернативную рамку** к лендинговой:

- **Лендинг:** GRO = «тренажёр», ежедневные 15–20-минутные тренировки на реальных примерах из ниши.
- **App Store:** GRO = «помощник в принятии решений», помогает «структурировать мысли, увидеть варианты, последствия и выбрать сильный следующий шаг».

Anti-positioning один и тот же: **«это не курсы и не советы»**. Обе рамки непротиворечивы — decision-support можно описать как «тренировка в микро-формате, где упражнение — это реальная твоя ситуация». Но контент-команда должна сознательно выбирать, какую рамку разворачивать в каждом конкретном канале: performance-креативы и пост для предпринимателя лучше работают через «помощник в решениях», а retention-контент и storytelling — через «ежедневный тренажёр». См. также [[canon/positioning/gro-value-proposition]].

## Треки в App Store

Явно перечислены шесть тем, на которых построены «треки и сценарии роста»:

- карьера
- деньги
- коммуникации
- мышление
- фокус
- продуктивность

**Это не тот же набор, что на лендинге.** На groapp.ru заявлены: продажи, маркетинг, коммуникации, цели, мышление, мотивация. Пересечение — только «коммуникации» и «мышление». Разнобой зафиксирован в `## Contradictions` на странице [[canon/product-knowledge/gro-app-overview]]; контент-команда должна проверить, какой список канонический в продукте сейчас (через веб-кабинет или query к команде).

## In-app purchases

В листинге явно показаны две позиции:

| SKU | Цена | Source |
|---|---|---|
| Подписка (1 месяц) | 2 490 ₽ | `[conf:high, src:2026-04-10]` |
| «100% Энергии» | 2 990 ₽ | `[conf:high, src:2026-04-10]` |

Подробный комментарий и связь с лендинговой ценой — в [[canon/product-knowledge/gro-pricing]]. Здесь достаточно знать, что App Store **подтверждает** месячную подписку как 2 490 ₽ (что совпадает с лендинговыми 83 ₽ × 30 дней) и **добавляет** новый SKU «100% Энергии» за 2 990 ₽, которого на лендинге не было.

## Ratings

Числовые данные (средний, распределение) живут в дрейфующей метрике [[evolving-strict/product-metrics/gro-store-ratings]] — там inline-маркеры и правила supersession. На момент последнего ingest-а App Store показывал малую bimodal-базу: большинство пятёрок и небольшой негативный хвост из 1★–2★, реагирующих на paywall. Качественный синтез того, **что** люди пишут — в [[evolving/customer-feedback/gro-app-store-reviews]].

**Правило цитирования в контенте.** Никогда не цитировать рейтинг без контекста размера выборки — это риск недобросовестной рекламы. Пока база <50 оценок, использовать дословные отзывы, а не агрегат.

## What's new — продуктовый сигнал

Release notes версии 1.6.14 (2026-03-31):

> Теперь подборки тренажеров подобраны индивидуально для твоего роста!

Это прямое усиление 4-го шага «адаптация» из [[canon/product-knowledge/gro-app-overview|механики продукта]] — продукт двигается в сторону персонализации. Готовый hook для release-post'а или post'а про обновления, если такой формат появится в контент-плане.

## Что НЕ выносить в контент

- Фразу «Romsfort East Advisory Management consultancies LLC» — это служебное publisher-юрлицо, не бренд.
- Рейтинг «4,0» без пояснения «11 оценок» — создаёт впечатление большей выборки, чем есть.
- «100% Энергии — 2 990 ₽» как известный оффер: природа SKU не подтверждена, сначала нужна верификация продуктом.

## Связанные страницы

- [[canon/product-knowledge/gro-google-play-listing]] — параллельный Android-листинг Google Play (та же версия, та же рамка, другая категория)
- [[canon/product-knowledge/gro-rustore-listing]] — параллельный Android-листинг RuStore (та же версия, та же рамка, другой publisher — ООО ГРО)
- [[canon/product-knowledge/gro-app-overview]] — механика продукта, 4 шага, треки (с contradictions-блоком про разнобой треков)
- [[canon/product-knowledge/gro-pricing]] — цена и IAP (обновлено по App Store данным)
- [[evolving/customer-feedback/gro-app-store-reviews]] — синтез пользовательских отзывов
- [[canon/product-knowledge/gro-team]] — реальная команда за продуктом (не App Store publisher)
- [[canon/positioning/gro-value-proposition]] — позиционирование продукта
- [[sources/2026-04-10-gro-appstore-listing]]

## Backlinks

_21 pages link to this one._

- [[canon/marketing-frameworks/tabunov-landing-anatomy]]
- [[canon/marketing-frameworks/visual-content-design-for-conversion]]
- [[canon/product-knowledge/gro-app-overview]]
- [[canon/product-knowledge/gro-google-play-listing]]
- [[canon/product-knowledge/gro-pricing]]
- [[canon/product-knowledge/gro-rustore-listing]]
- [[canon/product-knowledge/gro-team]]
- [[canon/product-knowledge/gro-web-app]]
- [[evolving-strict/market-data/app-store-slop-2026]]
- [[evolving-strict/market-data/ru-beauty-health-ecommerce-q1-2026]]
- [[evolving-strict/market-data/ru-business-ai-adoption-2026]]
- [[evolving-strict/product-metrics/gro-store-installs]]
- [[evolving-strict/product-metrics/gro-store-ratings]]
- [[evolving/customer-feedback/gro-app-store-reviews]]
- [[index]]
- [[overview]]
- [[sources/2026-04-10-gro-appstore-listing]]
- [[sources/2026-04-10-gro-googleplay-listing]]
- [[sources/2026-04-10-gro-lk-auth]]
- [[sources/2026-04-10-gro-rustore-listing]]
- [[sources/2026-04-16-hh-employer-branding-vacancies]]
