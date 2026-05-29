---
id: mkt:evolving-strict/campaign-metrics/diksi-bilayn-smart-tv-incrementality-2026
title: "Smart TV → офлайн-продажи: бенчмарки инкрементальности (Дикси × Билайн Adtech, дек 2025 — янв 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: campaign-metrics
tags: [campaign-metrics, advertising, ctv, smart-tv, retail-media, attribution, paid-ads, ru, case-study]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-26  # +cross-ref на сиблинг-кейс «Купер» × Билайн Adtech (media-mix)
sources: [sources/2026-05-19-dzen-diksi-bilayn-smart-tv-offline-sales-case.md]
namespace: mkt
---

# Smart TV → офлайн-продажи: бенчмарки инкрементальности (Дикси × Билайн Adtech)

Числовые результаты тест-контрольного измерения вклада рекламы на Билайн Смарт ТВ в офлайн-продажи сети «Дикси». Кейс операторов кампании («Дикси», РОССТ, Билайн Adtech) — **self-reported, без независимой валидации**, поэтому `confidence: medium`. Методология — см. [[canon/marketing-frameworks/clickless-channel-incrementality-stable-id]].

**Главный результат:** инкрементальный эффект Smart-TV-кампании сверх сезонности — **+23,4 п.п.** роста конверсии в покупку. `[conf:medium, src:2026-05-19]`

## Параметры кампании

| Параметр | Значение | Source |
|---|---|---|
| Канал | Билайн Смарт ТВ (CTV, без клика) | `[conf:medium, src:2026-05-19]` |
| Период | декабрь 2025 — январь 2026 (предновогодний пик) | `[conf:medium, src:2026-05-19]` |
| Выборка | 3,9 млн пользователей | `[conf:medium, src:2026-05-19]` |
| Атрибуция | Stable ID (обезличенный, по согласию) → офлайн-покупки в «Дикси» | `[conf:medium, src:2026-05-19]` |

## Инкрементальный lift (тест vs контроль)

| Метрика | Тест | Контроль | Дельта (инкремент) | Source |
|---|---|---|---|---|
| CR в целевые действия (рост в тесте) | +62,4% | — | — | `[conf:medium, src:2026-05-19]` |
| Конверсия в покупку (главный итог) | — | — | +23,4 п.п. | `[conf:medium, src:2026-05-19]` |
| CR у покупателей | +49,8% | +33,6% | +16,2 п.п. | `[conf:medium, src:2026-05-19]` |
| Средний чек | +22% | +17% | +5 п.п. | `[conf:medium, src:2026-05-19]` |

Обе группы росли на фоне предновогоднего спроса, но тестовая стабильно опережала контрольную — это и позволило отделить эффект сезона от эффекта рекламы. `[conf:medium, src:2026-05-19]`

## Региональный разрез

- В отдельных регионах дельта достигала **+54 п.п.** `[conf:medium, src:2026-05-19]`
- Эффект в регионах превышал столичный **более чем в 2 раза** `[conf:medium, src:2026-05-19]`
- Интерпретация операторов: высокая восприимчивость региональной аудитории к Smart-TV-рекламе (меньше рекламного шума, выше доля ТВ-смотрения). `[conf:low, src:2026-05-19]`

## Что показывают цифры (выводы)

- **Smart TV измеримо влияет на офлайн-выручку** даже без кликов — фиксируется эффект и на целевые действия, и на чек. `[conf:medium, src:2026-05-19]`
- **Эффект отделим от сезонности** — тест стабильно выше контроля при общем росте. `[conf:medium, src:2026-05-19]`
- **Рост комплексный**: канал двигает сразу привлечение, частоту/конверсию и средний чек, а не только верх воронки. `[conf:medium, src:2026-05-19]`
- **Регионы — приоритет для охватного CTV-бюджета** при таком разрыве дельты со столицей. `[conf:low, src:2026-05-19]`

## Caveat

Данные предоставлены операторами кампании (вендорский кейс). Не раскрыты: размер каждой группы, attribution window, способ построения «потенциального контакта» с рекламой, репрезентативность контроля. Для переноса бенчмарков на собственные кампании см. ограничения во [[canon/marketing-frameworks/clickless-channel-incrementality-stable-id]].

## Связанные страницы

- [[canon/marketing-frameworks/clickless-channel-incrementality-stable-id]] — методология измерения click-less каналов
- [[evolving-strict/campaign-metrics/kuper-bilayn-cross-channel-incrementality-2026]] — сиблинг-кейс того же провайдера (Билайн Adtech), но media-mix из 4 каналов + синергия
- [[canon/marketing-frameworks/channel-role-funnel-mapping-media-mix]] — роль-декомпозиция каналов + синергия (надстройка над этим кейсом)
- [[evolving/industry-trends/digital-indoor-retail-media-ru-2026]] — Билайн Adtech как игрок retail-media
- [[evolving-strict/market-data/digital-ad-cpm-shifts-q1-2026]] — сдвиг бюджетов на CTV/DOOH (макро-контекст)
- [[evolving-strict/campaign-metrics/ugc-cpv-benchmarks-2026]] — смежные канальные бенчмарки RU-рынка
- [[sources/2026-05-19-dzen-diksi-bilayn-smart-tv-offline-sales-case]] — первоисточник
