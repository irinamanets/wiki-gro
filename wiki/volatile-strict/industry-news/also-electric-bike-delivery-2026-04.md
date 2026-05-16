---
id: mkt:volatile-strict/industry-news/also-electric-bike-delivery-2026-04
title: "ALSO привлёк $200M на беспилотный электро-cargo-bike (контракт с Doordash)"
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [autonomous-delivery, robotics, also, doordash, hardware, mega-round, awareness]
confidence: medium
stale: false
created: 2026-04-27
updated: 2026-04-27
sources: [sources/2026-04-27-tg-startupoftheday-apr-15-27-2026.md]
namespace: mkt
---

# ALSO — $200M раунд + Doordash контракт + новый класс беспилотного курьера

К концу апреля 2026 в США оформился новый формат беспилотной last-mile-доставки: **электро-cargo-bike** от стартапа [ALSO](https://ridealso.com/). По наблюдению Александра Горного ([[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] посты 5022, 5029).

## Факты

- **Раунд:** $200M `[conf:medium, src:2026-04-20]`. Часть пойдёт на cargo-bike (one-of-multiple продукт ALSO).
- **Партнёрство:** контракт с **Doordash** (крупнейший US-доставщик еды) уже подписан `[conf:medium, src:2026-04-20]`.
- **Status доставок:** «первый заказ ещё не доставил» (на 2026-04-20) — то есть pre-revenue в этой вертикали `[conf:medium, src:2026-04-20]`.
- **Form-factor:** четырёхколёсное cargo-устройство с большим грузовым отсеком, большие колёса, мощная батарея, далёкие маршруты. Визуально ближе к «телеге» чем к велосипеду (см. [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] раздел про распознанный текст 5022.jpg).
- **Регуляторная стратегия (важно):** педали есть, но **не приводят колёса напрямую — только генерируют электричество для батареи**. Цель — формально классифицироваться как велосипед, чтобы получить право на велодорожки/тротуары. См. [[evolving/industry-trends/autonomous-delivery-vehicle-classification-2026]].

## Почему это сигнал, а не просто новость

Существующий стандарт беспилотного курьера в мегаполисах — **приземистые роверы, имитирующие пешехода** (small, slow, short-range) `[conf:high, src:2026-04-20]`. По мнению Горного, эта форма-фактор **structurally плохой**:
- Маленькая грузоподъёмность → мало заказов на маршрут
- Медленный → еда стынет
- Короткий радиус → негодная экономика для доставки за пределы 1-2 км
- Имитирует пешехода в категории, где живые люди работают **на велосипедах**

ALSO — **первая попытка скопировать живого курьера, а не пешехода**. Это **категориальный сдвиг**, не просто очередной игрок.

## Author opinion (verified-as-VC-observer)

Горный фиксирует регуляторный аспект:
> «ей хочется, чтобы им было можно ездить по велодорожкам и, видимо, даже по тротуарам. Это и безопаснее для доставщика, и автопилот проще запрограммировать, если не надо думать о больших скоростях окружающих. Обычным людям такое соседство скорее всего не понравится, да. Впрочем, им и живые курьеры на байках не нравятся, радикально хуже не станет.»

Эта observation = ядро для [[evolving/industry-trends/autonomous-delivery-vehicle-classification-2026]] (regulatory-arbitrage taxonomy).

## Russian-параллель: Whoosh

Горный сам напоминает про российский **Whoosh**, который аргументировал, что его электросамокаты — «не совсем самоходные» (требуют толкания ногой при старте), чтобы избежать категоризации как мопедов `[conf:medium, src:2026-04-23]`. Через 2-3 года та же риторическая стратегия повторяется ALSO в другой юрисдикции — это **structural pattern**, не case-noise.

## Что это значит для маркетинга GRO

GRO — фитнес-приложение. Прямого функционального пересечения с автономной доставкой нет. Но как **content/cultural reference** случай ALSO попадает в три ниши:

1. **«Ходи пешком vs. поезжай на электротранспорте» — текущий cultural reframe** — все больше городских жителей по умолчанию находятся на pedal-assisted, кикшеринге, такси. Активная физическая активность становится **выбором, а не дефолтом**. Это касается positioning [[canon/product-knowledge/gro-team]] — фитнес-приложение продаёт **выбор активности**, против тренда «всё за тебя».
2. **AI/automation-narrative-якорь** — ALSO как один из 5 «робототехника+автопилоты» unicorn-ов 2026 YTD ([[evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd]]). Для content-постов про «AI заменяет всё» — конкретный данные-point.
3. **Регуляторная мысль-формат** — «как одна product-decision (педали-генератор vs. педали-привод) перевернёт legal-категорию» — переносимый mental model для маркетеров про packaging product narrative. См. [[evolving/industry-trends/autonomous-delivery-vehicle-classification-2026]].

## TTL

`volatile-strict` — через 90 дней (≈2026-07-26) проверить:
- Запустил ли ALSO реальные доставки с Doordash?
- Выиграл ли регуляторный спор «велосипед vs. транспорт» в каком-либо штате?
- Появились ли копии этого формата от других стартапов?

Если ни одно — пометить `stale: true` и оставить как историю **первой попытки** этого формата.

## Связанные страницы

- [[evolving/industry-trends/autonomous-delivery-vehicle-classification-2026]] — regulatory-arbitrage таксономия (педали-as-genre marker)
- [[evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd]] — ALSO в составе 5 «robotics + autopilots» unicorn-ов 2026 YTD
- [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] — оригинал ingest
