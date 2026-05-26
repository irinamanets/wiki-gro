---
id: mkt:canon/marketing-frameworks/dbs-fulfillment-marketplace-exit-step
title: "DBS (Delivered by Seller): операционный half-exit с маркетплейсов без полной логистики"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [marketplace, dbs, fulfillment, fbo, fbs, exit-strategy, ru-smb, sellers, sdek, logistics, operations]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-bezsmuzi-may-8-11-2026.md]
namespace: mkt
---

# DBS (Delivered by Seller) — half-exit с маркетплейсов без полной логистики

DBS — операционный fulfillment-режим маркетплейса, где **МП выступает только витриной**, а **доставку селлер организует силами транспортной компании** (СДЭК, Деловые Линии, Boxberry и т.д.). Зафиксировано в [[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026|посте 15976 Максима Кульгина]] от 2026-05-10 как цитата опытного селлера.

`confidence: medium` — практика широко известна и операционально verifiable у крупных МП (Ozon DBS, Yandex Market DBS). Цитата в посте 15976 — operational testimony от практикующего селлера, передана Кульгиным без коррекций.

## Три fulfillment-модели маркетплейсов

| Модель | Кто хранит товар | Кто доставляет | Маржинальность для селлера | Cost базы |
|---|---|---|---|---|
| **FBO** (Fulfillment by Operator) | МП-склад | МП | Низкая (комиссии + storage) | Хранение / возвраты |
| **FBS** (Fulfillment by Seller, классический) | Склад селлера | МП-сеть | Средняя | Логистика МП |
| **DBS** (Delivered by Seller) | Склад селлера | **Транспортная компания селлера** | **Высокая** (МП = только витрина) | Tariff TK + outsource ops |

DBS — это **maximal-cost-control модель** для селлера, при которой МП теряет влияние на доставку и не получает logistics-margin.

## Точная operational цитата (пост 15976)

> «Для селлеров МП сейчас многими ТК предусмотрена **более простая схема работы с меньшим количеством затрат**. Называется **DBS** — режим доставки, когда МП выступает исключительно витриной, а доставка осуществляется посредством ТК. Это **дешевле на длинной дистанции**, есть возможность подключения доп.услуг — по типу примерки на дому, возврата до и после выкупа после одобрения селлера. Также **многие компании предлагают скидки или персональные тарифы**, если работа налажена, и выручка стабильно высокая. Тот же СДЭК предлагает уйму вариантов оптимизации работы, чтобы у селлера было больше времени на фокусное развитие своего дела, без оглядки на муторную операционку.»

## Почему DBS — это half-exit, а не «остаться на МП»

В контексте [[evolving/industry-trends/ru-marketplace-seller-squeeze-2026|сжатия селлеров маркетплейсами]] селлеры обсуждают **3 опции** ([[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026|пост 15990]]):

1. **Остаться на FBO/FBS** — терпеть сжатие маржи (take rate >50%, контрафакт, штрафы)
2. **Построить собственную логистику** — full exit с МП, но капекс на склад + ИТ + персонал = barrier для small/median sellers
3. **DBS** — **third way**: МП-витрина (трафик, доверие) + outsourced транспорт (СДЭК, ...) + контроль над cost-structure доставки

DBS особенно подходит:
- Селлерам с **уникальным товаром** — не страдают от контрафакта внутри МП.
- Селлерам со **стабильной выручкой** — получают **персональные тарифы** ТК.
- Селлерам с **дальней географией доставки** — long-distance economics ТК часто лучше внутренней логистики МП.

## Дополнительные advantages по цитате

1. **Доп. услуги ТК:** примерка на дому, возврат до и после выкупа **только после одобрения селлера**. Это даёт селлеру **возможность отказа в возврате** в случае подмены товара — то, что не работает в FBO/FBS-режиме, где МП решает unilaterally.
2. **Personal тарифы / скидки** — ТК конкурируют между собой и предоставляют volume-discount, в отличие от МП, у которого фиксированная комиссия.
3. **Outsourced operations** — селлер не отвлекается на упаковку/маркировку/возвраты, ТК делает full-cycle логистику. «Фокус на развитии своего дела, без оглядки на муторную операционку.»

## Когда DBS не работает

- **Категории с high-frequency low-AOV** (низкий чек) — фиксированная стоимость отправки ТК делает unit-economics нерентабельной.
- **Категории с быстрой доставкой** (готовая еда, продукты) — ТК не предоставляют next-day-1-час доставку, а FBO предоставляет.
- **Категории под МП-private-label** — если МП **планирует** запустить свой analog (см. [[evolving/industry-trends/ru-marketplace-seller-squeeze-2026|механика data leverage]]) — никакая логистика не спасёт.

## Связь с другими рамками

1. **[[evolving/industry-trends/ru-marketplace-seller-squeeze-2026]]** — DBS как **defensive response** на take-rate >50% и data leverage.
2. **[[canon/marketing-frameworks/marketplace-distribution-diversification-5-channels]]** (Т-Банк / Кретов) — DBS укладывается в широкую логику diversification: не уходить с МП полностью, а **минимизировать dependency**.
3. **[[evolving/industry-trends/freelance-platform-dependency|Платформенная зависимость]]** — параллель из freelance-мира: DBS = технический способ снизить platform-dependency, не теряя platform-traffic.
4. **[[canon/marketing-frameworks/typical-productized-services-pivot|Productized services pivot]]** — DBS отдаёт логистику как «productized service» ТК, освобождая селлера для focus на product/marketing.

## Application для GRO

GRO как продукт **не операционно затрагивает** маркетплейсы. Но **content GRO** для founder/SMB-аудитории, часть которой = МП-селлеры, должен включать DBS как **actionable framework**:

- **Hook про DBS как half-exit** — для тех, кто слышал «бросай маркетплейсы», но не может (или не хочет).
- **Education content** — explanatory материал о трёх fulfillment-моделях и когда какая работает.
- **Founder-content angle** — «как фокусироваться на продукте, отдав operations внешнему партнёру» — переходит от MP-кейса к broader productivity-фрейму.

## Hooks для контента GRO

1. «DBS — это не уйти с маркетплейса. Это **снизить его влияние без капекса на склад**.»
2. «Витрина — МП. Доставка — СДЭК. **Контроль — селлер**. Это работает.»
3. «Полная экспансия в свою логистику = годовой капекс. **DBS** = три месяца на переход.»

## Caveat'ы

- DBS **не везде доступен** — Ozon и Yandex Market предоставляют активно, WB — частично/в выбранных категориях.
- **Логистические расходы** через ТК **выше unit-стоимости** МП-операций (если объёмы средние) — экономия идёт через **избежание take rate и комиссии**, не через прямую цену доставки.
- **Time-to-customer** через ТК обычно **дольше**, чем через МП-сеть, что снижает конверсию в impulse-категориях.
- DBS требует **operational capacity** у селлера (упаковка, маркировка, передача в ТК) — не подходит зеро-time founders.

## Связанные страницы

- [[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026]] — источник-якорь
- [[evolving/industry-trends/ru-marketplace-seller-squeeze-2026]] — контекст squeeze, defensive response
- [[canon/marketing-frameworks/marketplace-distribution-diversification-5-channels]] — broader diversification рамка
- [[evolving/industry-trends/freelance-platform-dependency]] — параллель из freelance
- [[canon/marketing-frameworks/typical-productized-services-pivot]] — outsourced services pattern
