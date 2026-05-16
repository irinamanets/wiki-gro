---
id: mkt:evolving-strict/product-metrics/gro-store-installs
title: GRO — установки в магазинах приложений
type: page
subtype: metric
layer: evolving-strict
theme: product-metrics
tags: [product, installs, app-store, google-play, rustore, distribution]
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

# GRO — установки в магазинах приложений

Числовые показатели установок GRO в трёх ingested точках мобильной дистрибуции по состоянию на 2026-04-10. **evolving-strict**: числа обязаны нести inline `[conf:*, src:*]`, любые обновления идут через supersession. TTL 180 дней.

Рейтинги как параллельная метрика — в [[evolving-strict/product-metrics/gro-store-ratings]]. Качественные выводы о том, как эти числа влияют на distribution-стратегию — в соответствующих листинг-страницах.

## Сводная таблица

| Стор | Публичный показатель | Internal (если есть) | Source |
|---|---|---|---|
| App Store iOS | не раскрывается | — | `[conf:high, src:2026-04-10]` |
| Google Play | 100+ (bucket) | 448 точно (из data-blob) | `[conf:high, src:2026-04-10]` |
| RuStore | «до 1 тыс» (bucket) | — | `[conf:high, src:2026-04-10]` |

## App Store iOS

Apple **не показывает** число установок на публичной странице приложения. Единственный косвенный сигнал — 11 пользовательских оценок (см. [[evolving-strict/product-metrics/gro-store-ratings]]), но это не база установок.

Без внешних инструментов (App Annie, Sensor Tower) или внутренних App Store Connect-данных точное число недоступно. Если такие данные появятся — ingested сюда отдельным полем.

## Google Play

- **Публичный bucket:** **100+** `[conf:high, src:2026-04-10]`. Google Play округляет до bucket'ов; 100+ — первый публичный порог выше 50+.
- **Внутреннее точное значение (из data-blob страницы):** **448 установок** `[conf:high, src:2026-04-10]`.

**Правила цитирования:**

- Публично (в контенте, CPA-креативах, постах): только **«100+»** или вообще без числа.
- **Точное «448» — internal-only.** Цитирование точного числа в публичном контенте выглядит как внутренняя утечка, Google Play сам такое число не раскрывает.
- В overview/tracking-документах и для внутренних решений — можно и нужно использовать точное 448, это полезный signal для distribution-планирования.

**Вывод для distribution-стратегии.** Текущее internal-значение Google Play (см. таблицу выше) описывает **почти незадействованный канал**. Для сравнения (не прямого, базы разные): App Store показывает порядка десятка оценок, что при нормальной конверсии оценок в единицы процентов даёт грубо сопоставимую базу установок на iOS. То есть GRO сейчас распределён между iOS и Google Play примерно поровну на уровне сотен установок каждый — вывод устойчивый, конкретные числа обновляются по таблице в начале страницы.

## RuStore

- **Публичный bucket:** **«до 1 тыс»** `[conf:high, src:2026-04-10]`. Это **первый** bucket RuStore, ниже него bucket'а нет (ни «до 500», ни «до 100»).
- **Точное число:** **не раскрывается** ни в UI, ни в HTML страницы (в отличие от Google Play, где точное значение есть в data-blob).

Важно: bucket «до 1 тыс» не означает, что у GRO близко к тысяче установок в RuStore. Это означает только, что число **меньше тысячи** — может быть 10, 50, 200. Без более точных данных использовать его как маркетинговый сигнал нельзя.

## Интерпретация — total reach

Публичные числа дают только нижнюю границу:
- Google Play: **≥100** установок `[conf:high, src:2026-04-10]`
- RuStore: **<1000** установок `[conf:high, src:2026-04-10]`
- App Store: **неизвестно** публично

**Internal total** (с учётом точного Google Play 448 и консервативной оценки): вероятнее всего в диапазоне **нескольких сотен** установок на каждой платформе, общий total — в **низких тысячах** `[conf:medium, src:2026-04-10]`. Это грубая оценка, не число для маркетинга.

**Маркетинговый вывод.** GRO находится на фазе **до product-market-fit-масштабирования** по дистрибуции. Любые CPA-кампании сейчас — про обучение аудитории и сбор первых отзывов, а не про масштабный growth. Performance-бюджеты должны рассматриваться как research-бюджеты, не как acquisition-скейл.

## Что НЕ выносить в контент

- **Точное «448»** — internal-only. В публичном контенте — только «100+».
- **«До 1 тыс»** как positive framing — это предел bucket'а снизу, а не достижение сверху.
- **Суммирование установок между сторами** в публичных числах — ни один стор не раскрывает точных чисел, сумма всегда будет недобросовестной оценкой.

## Условия пересборки

- Переход Google Play в следующий bucket (500+, 1K+, 5K+) — обязательный re-ingest.
- Появление в RuStore bucket'а за пределами «до 1 тыс» — обязательный re-ingest.
- Любая внутренняя данная по App Store (если команда поделится) — отдельным update.
- Плановый re-verify — каждые 180 дней (TTL evolving-strict).

## Связанные страницы

- [[evolving-strict/product-metrics/gro-store-ratings]] — параллельная метрика (рейтинги)
- [[canon/product-knowledge/gro-app-store-listing]] — iOS-листинг
- [[canon/product-knowledge/gro-google-play-listing]] — Google Play-листинг
- [[canon/product-knowledge/gro-rustore-listing]] — RuStore-листинг
- [[sources/2026-04-10-gro-appstore-listing]]
- [[sources/2026-04-10-gro-googleplay-listing]]
- [[sources/2026-04-10-gro-rustore-listing]]

## Backlinks

_9 pages link to this one._

- [[canon/marketing-frameworks/narrative-as-brand-currency]]
- [[canon/marketing-frameworks/retention-benchmarks-b2c]]
- [[canon/product-knowledge/gro-google-play-listing]]
- [[canon/product-knowledge/gro-rustore-listing]]
- [[evolving-strict/market-data/ru-psychology-services-2025-2026]]
- [[evolving-strict/product-metrics/gro-store-ratings]]
- [[evolving/content-trends/ru-business-tg-content-drift-2026]]
- [[index]]
- [[overview]]
