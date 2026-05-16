---
id: mkt:evolving-strict/product-metrics/gro-store-ratings
title: GRO — рейтинги в магазинах приложений
type: page
subtype: metric
layer: evolving-strict
theme: product-metrics
tags: [product, ratings, app-store, google-play, rustore, social-proof]
confidence: high
stale: false
created: 2026-04-10
updated: 2026-04-10
sources:
  - sources/2026-04-10-gro-appstore-listing.md
  - sources/2026-04-10-gro-googleplay-listing.md
  - sources/2026-04-10-gro-rustore-listing.md
namespace: mkt
---

# GRO — рейтинги в магазинах приложений

Числовые рейтинги и распределение оценок GRO в трёх ingested точках мобильной дистрибуции по состоянию на 2026-04-10. Это **evolving-strict**-страница: данные дрейфуют с каждой новой оценкой, каждое число обязано нести inline-маркер `[conf:*, src:*]`, при любом пересборе — supersession через HTML-комментарий. TTL 180 дней; после — re-verify повторным ingest-ом страниц листингов.

Качественный синтез того, **что** люди пишут в отзывах, и выводы для контента — в `[[evolving/customer-feedback/gro-app-store-reviews]]`. Эта страница — только цифры.

## Сводная таблица

| Стор | Средний рейтинг | Всего оценок | Source |
|---|---|---|---|
| App Store iOS (RU) | 4,0 / 5 | 11 | `[conf:high, src:2026-04-10]` |
| Google Play | — (скрыт) | 0 видимых | `[conf:high, src:2026-04-10]` |
| RuStore | 0,0 «Нет оценок» | 0 | `[conf:high, src:2026-04-10]` |

**Интерпретация:** по сути, рейтинг как маркетинговый сигнал существует только в App Store, и даже там база слишком мала, чтобы оперировать им как claim'ом. Google Play скрывает агрегат при малой базе отзывов. RuStore показывает явный 0,0 «Нет оценок» — хуже всего для CPA-кампаний.

## App Store iOS — распределение

- Средний: **4,0 / 5** `[conf:high, src:2026-04-10]`
- Всего оценок: **11** `[conf:high, src:2026-04-10]`
- Распределение: **7 × 5★, 1 × 4★, 0 × 3★, 2 × 2★, 1 × 1★** `[conf:high, src:2026-04-10]`
- Доля пятёрок: **72,7%** `[conf:high, src:2026-04-10]`
- Доля 1★–2★: **27,3%** `[conf:high, src:2026-04-10]`

**Bimodal без «серединки»** — оба полюса, судя по контенту отзывов, реагируют на одно и то же (paywall). Синтез содержимого — в [[evolving/customer-feedback/gro-app-store-reviews]].

**11 оценок — пока слишком малая база**, чтобы оперировать рейтингом как маркетинговым claim'ом в креативе. Риск недобросовестной рекламы: «4,0 в App Store» без контекста «11 оценок» создаст ложное впечатление масштаба. До 50+ оценок лучше использовать конкретные дословные отзывы.

## Google Play — рейтинг скрыт

- Средний рейтинг: **не отображается** `[conf:high, src:2026-04-10]`
- Причина скрытия: Google Play автоматически скрывает агрегат при слишком малой базе отзывов.
- Видимых пользовательских отзывов: **0** `[conf:high, src:2026-04-10]`

Google Play-канал — **без социального доказательства внутри стора**. Рекомендация (см. [[canon/product-knowledge/gro-google-play-listing]]): не запускать масштабные CPA-кампании под Android, пока листинг пустой; приоритет — собрать первые 20–50 оценок органикой или in-app review prompt.

## RuStore — рейтинг отсутствует

- Средний рейтинг: **0,0** `[conf:high, src:2026-04-10]`
- Подпись: **«Нет оценок»** `[conf:high, src:2026-04-10]`
- Видимых пользовательских отзывов: **0** `[conf:high, src:2026-04-10]`

RuStore **ещё более пустой, чем Google Play**: там хотя бы bucket «100+» установок намекает на какую-то базу, здесь — ни рейтинга, ни отзывов. Это критично, потому что RuStore — обязательный канал для части российских Android-устройств (без Google Services). Рекомендация — любой CPA-креатив, ведущий в RuStore, должен нести собственный proof из-за пустого листинга.

## Что НЕ выносить в контент

- **«Рейтинг GRO в магазинах»** как усреднённая фраза — работает только iOS (4,0 при 11 оценках, с обязательной оговоркой про размер выборки). В Google Play и RuStore рейтинга нет.
- **«4,0» без «11 оценок»** — всегда указывать базу, иначе недобросовестная реклама.
- **Выдумывать рейтинг** там, где его нет (Google Play, RuStore) — нельзя.

## Условия пересборки

Эта страница помечена `evolving-strict` — ожидается regular re-verify. Триггеры для re-ingest:

- Накопление новых оценок в любом из сторов (проверять раз в 4–6 недель).
- Появление видимого рейтинга в Google Play (скрывается при <5–10 оценок — порог точно не документирован).
- Появление первой оценки в RuStore.
- Любой маркетинговый спор, где число рейтинга нужно процитировать в креативе — обязательно refetch.

При любой пересборке старые числа обязаны уйти в HTML-комментарий формата `<!-- superseded YYYY-MM-DD by new-source : было 4,0/11 -->`, а не быть перезаписаны.

## Связанные страницы

- [[evolving/customer-feedback/gro-app-store-reviews]] — качественный синтез содержимого отзывов
- [[evolving-strict/product-metrics/gro-store-installs]] — числа по установкам (параллельная метрика)
- [[canon/product-knowledge/gro-app-store-listing]] — iOS-листинг (reference)
- [[canon/product-knowledge/gro-google-play-listing]] — Google Play-листинг
- [[canon/product-knowledge/gro-rustore-listing]] — RuStore-листинг
- [[sources/2026-04-10-gro-appstore-listing]]
- [[sources/2026-04-10-gro-googleplay-listing]]
- [[sources/2026-04-10-gro-rustore-listing]]

## Backlinks

_9 pages link to this one._

- [[canon/marketing-frameworks/external-validation-trap]]
- [[canon/marketing-frameworks/retention-benchmarks-b2c]]
- [[canon/product-knowledge/gro-app-store-listing]]
- [[canon/product-knowledge/gro-google-play-listing]]
- [[canon/product-knowledge/gro-rustore-listing]]
- [[evolving-strict/product-metrics/gro-store-installs]]
- [[evolving/content-trends/ru-business-tg-content-drift-2026]]
- [[index]]
- [[overview]]
