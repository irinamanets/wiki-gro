---
id: mkt:volatile-strict/competitor-news/tbank-unionpay-global-61-countries-2026-05
title: "T-Bank запустил переводы на UnionPay Global карты в 61 страну (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [competitor, t-bank, cross-border, unionpay, payment-infrastructure, sanctions, fintech, news]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-tinkoffbank-may-19-26-2026.md]
namespace: mkt
---

# T-Bank запустил переводы на UnionPay Global карты в 61 страну (май 2026)

Т-Банк объявил расширение международных переводов: со счёта в Т-Банке теперь можно отправлять деньги на карты **UnionPay Global** в **61 страну**. `[conf:high, src:2026-05-21]` Раньше переводы были доступны только на карты UnionPay, выпущенные в Китае. Перевод по номеру карты + ФИО получателя на латинице. Зачисление моментально. `[conf:high, src:2026-05-21]`

## Параметры запуска

| Параметр | Значение | Source |
|---|---|---|
| **Дата объявления** | 21 мая 2026 (пост @tinkoffbank/10736) | `[conf:high, src:2026-05-21]` |
| **Охват стран** | **61 страна** (включая Китай, Узбекистан, Вьетнам, Филиппины, Сингапур, Францию, Германию, Испанию, Бельгию) | `[conf:high, src:2026-05-21]` |
| **Тип карт получателя** | UnionPay Global (любых стран эмиссии, не только Китай) | `[conf:high, src:2026-05-21]` |
| **Способ перевода** | По номеру карты + ФИО латиницей | `[conf:high, src:2026-05-21]` |
| **Время зачисления** | Моментально | `[conf:high, src:2026-05-21]` |
| **Лимит без комиссии** | До **100 000 ₽/мес** (зависит от подписки Pro и сервиса Premium) | `[conf:high, src:2026-05-21]` |
| **UI-вход** | «Платежи» → «В другую страну» → выбрать страну → «По номеру карты» → номер + ФИО + сумма → «Перевести» | `[conf:high, src:2026-05-21]` |

Полные условия — на странице tbank.ru/bank/help/cross-border/outgoing-terms/ `[conf:high, src:2026-05-21]`.

## Стратегический контекст

После санкционных ограничений на SWIFT для RU-банков (2022), доступность международных переводов для физических лиц **существенно сузилась**. Большинство RU-банков смогли восстановить только узкий perimeter (внутри-ЕАЭС, или **через UnionPay только в Китай**).

Т-Банк теперь имеет **значительно более широкий международный охват**, чем typical RU-bank, благодаря UnionPay Global infrastructure:

- **Узбекистан, Вьетнам, Филиппины, Сингапур** — азиатские направления, где UnionPay имеет penetration
- **Франция, Германия, Испания, Бельгия** — европейские направления, где UnionPay Global cards держат немногие, но они **существуют** (через эмиттентов UnionPay Europe)

61 страна — это **не 61 country с UnionPay-native эмиссиями**, а **61 country, где UnionPay Global cards могут быть выпущены или приняты** через интернациональные эмитенты.

## Конкурентный landscape (cross-border переводы для физлиц)

| Игрок | Международный охват для P2P-переводов из РФ |
|---|---|
| **Т-Банк** | **61 страна** через UnionPay Global + дополнительные channels |
| **Сбер** | ЕАЭС + ограниченный non-CIS через SWIFT-replacement (СБП cross-border) |
| **ВТБ** | Ограниченно non-CIS, в основном корпоративные |
| **Газпромбанк** | Корпоративные переводы, ограниченно P2P |
| **Yandex Pay / СБП** | СБП cross-border — узкий, тестовые направления (Узбекистан, Беларусь, Казахстан) |
| **Контур.Финансы** | Cross-border для МСП, узкий охват |

**Т-Банк лидирует** по country-count и frictionless-flow для P2P-переводов.

## Маркетинговый сигнал

1. **Infrastructure-flex.** «61 страна» — это **scale claim**, понятный mass-audience. Не требует понимания UnionPay-механики.
2. **Customer-segment locking.** Бизнес-путешественники, owners cross-border бизнесов, RU-граждане за границей — эти сегменты **в Т-Банке remain**, потому что у других банков нет такого охвата.
3. **Cross-border = differentiation moat.** В RU-банковском конкуренте «cashback» и «обслуживание» — commoditized. **International-payments** — это remaining differentiator, где Т-Банк explicitly строит лидерство.
4. **Anchor-frame:** «По номеру карты. Моментально» — это **anti-friction message**. Стандартная боль cross-border переводов = долго (SWIFT 3–5 дней) и сложно (IBAN, BIC, address). Т-Банк snimaет эти болy.

## Регуляторный/операционный контекст

- Перевод **облагается лимитом 100 000 ₽/мес без комиссии**, дальше — стандартные комиссии Т-Банка. [conf:low, src:2026-05-26]
- Pro-подписка и Premium-сервис могут расширять лимит. Это создаёт **upsell-bridge** между cross-border сервисом и premium-tier.
- Зачисление «моментально» — возможно только потому что **UnionPay clearing infrastructure** имеет realtime-капабилити. Это отличие от SWIFT (1–3 рабочих дня).

## Для GRO — что унести

Не applicable напрямую (GRO не финансовый продукт), но **наблюдаемый pattern**: **infrastructure-claim как scale-сигнал**. «Доступно в N странах», «Подключено N интеграций», «Поддерживаем N форматов» — это reусableusable для любого SaaS / digital-продукта. Numerical scope = simpler comprehension чем benefit-list.

## Связанные страницы
- [[sources/2026-05-26-tg-tinkoffbank-may-19-26-2026]] — primary-источник (#10736)
- [[evolving/industry-trends/tbank-corporate-platform-stack-2026]] — ecosystem-strategy контекст
- [[evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay]] — canonical yellow-block использованный в creative
- [[evolving-strict/competitor-metrics/tbank-historical-metrics-2019-2024]] — historical metrics
