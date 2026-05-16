---
id: mkt:evolving-strict/campaign-metrics/cross-promo-speaker-swap-benchmark-2026
title: "Cross-promo speaker-swap benchmark — Telegram-конференция Воронина (14 мая 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: campaign-metrics
tags: [telegram, cross-promo, webinar, partnerships, community, benchmark, russia]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-community-tech-voronin-may-2026.md]
namespace: mkt
---

# Cross-promo speaker-swap benchmark — Telegram-конференция Воронина (14 мая 2026)

## Краткое summary

Реальные оперативные цифры **cross-promo экономики бесплатной онлайн-конференции в Telegram** в РФ-сегменте mid-May 2026. Источник — скриншот таблицы аналитики, опубликованный Михаилом Ворониным в его авторском канале @community_tech (пост 989, image 989) за несколько часов до начала конференции «Время сильных 2026» 14 мая. См. [[sources/2026-05-14-tg-community-tech-voronin-may-2026]] для контекста и OCR-данных.

**Confidence: medium** — один публичный snapshot, без независимой верификации, без указания методики подсчёта «вошедших» (видимо — uniques через регистрационного бота за timeframe промо-кампании). Атрибуция: «по опубликованной таблице Михаила Воронина, src:t.me/community_tech/989, 2026-05-14».

## Модель «cross-promo speaker-swap»

Воронин формулирует экономику в посте 989 дословно:

> «Плата спикеров за эту конференцию — обмен подписчиками».

Это операционная схема:
1. Организатор собирает **8 топ-спикеров** (бизнес-инфлюенсеры с собственной Telegram-аудиторией). `[conf:high, src:2026-05-14]`
2. Каждый спикер постит у себя анонс с реферальной ссылкой на регистрационный бот Воронина.
3. Регистрационный бот трекает source-ссылку — кто пришёл от какого спикера.
4. Подписки на канал Воронина (через `/start <ref>` параметр) учитываются как «оплата» спикера за участие.
5. Спикер получает доступ к собранной cross-аудитории (агрегированный охват) + brand exposure.

Cost-zero для организатора (нет paid-traffic), стимулы выровнены: чем «лучше» спикер привёл/удержал, тем выше его reputation среди peer-каналов.

## Benchmark-таблица (snapshot 14 мая 2026, перед началом)

Источник — image 989, скриншот excel-таблицы:

| Спикер | Вошло в бот | Подписалось (+) | Отписалось (–) | Заблокировали бота | Конверсия (вход → подписчик), % | Source |
|---|---|---|---|---|---|---|
| Дмитрий Бескромный | 310 | 127 | 156 | 58 | 40.97% | `[conf:medium, src:2026-05-14]` |
| Михаил Дашкиев | 217 | 137 | 78 | 12 | 63.13% | `[conf:medium, src:2026-05-14]` |
| Роман Кумар | 133 | 66 | 60 | 17 | 49.62% | `[conf:medium, src:2026-05-14]` |
| Денис Амирханян | 127 | 76 | 49 | 7 | 59.84% | `[conf:medium, src:2026-05-14]` |
| Михаил Воронин (host) | 72 | 42 | 28 | 4 | 58.33% | `[conf:medium, src:2026-05-14]` |
| Максим Спиридонов | 74 | 36 | 35 | 12 | 48.65% | `[conf:medium, src:2026-05-14]` |
| Вита Носова | 43 | 23 | 19 | 5 | 53.49% | `[conf:medium, src:2026-05-14]` |
| Сергей Иванов | 176 | 98 | 85 | 13 | 55.68% | `[conf:medium, src:2026-05-14]` |
| **ИТОГО (8 спикеров)** | **1152** | **605** | **510** | **128** | **53.72%** | `[conf:medium, src:2026-05-14]` |

## Ключевые метрики

- **Общий cross-promo охват за timeframe (несколько дней до 14 мая):** 1152 уникальных входов в регистрационный бот. `[conf:medium, src:2026-05-14]`
- **Средняя «брутто-конверсия в подписчика»:** 53.72% (от вошедших). `[conf:medium, src:2026-05-14]`
- **Bot-block rate (cold-traffic):** 11.1% (128 из 1152). `[conf:medium, src:2026-05-14]` — это baseline для «отказа сразу же» в Telegram-funnels на cold-traffic.
- **Разброс конверсии между спикерами:** 40.97% (Бескромный) — 63.13% (Дашкиев), коэффициент ×1.54. `[conf:medium, src:2026-05-14]`
- **Разброс «силы трафика»:** ×7.2 (Бескромный 310 vs Носова 43). `[conf:medium, src:2026-05-14]`

## Insight: «качество > размер аудитории»

Корреляция между **трафиком** (вошло) и **конверсией** (подписалось/вошло) **слабая или обратная**:

- Дашкиев привёл 217 человек с конверсией 63.13% (137 подписчиков чистыми) `[conf:medium, src:2026-05-14]`
- Бескромный привёл 310 человек с конверсией 40.97% (127 подписчиков чистыми) `[conf:medium, src:2026-05-14]`
- При вдвое большем чистом результате (217 vs 310) у Дашкиева получилось **больше подписчиков** (137 vs 127). `[conf:medium, src:2026-05-14]`

**Гипотеза:** аудитория Бескромного «холоднее» или менее заинтересована в business-developer контенте конференции. Аудитория Дашкиева (БМ alumni) — более warm и self-selected.

**Operational follow-up:** при выборе cross-promo спикеров не оптимизировать по размеру их аудитории, а по **fit аудитории с твоим продуктом / темой**. См. также [[canon/marketing-frameworks/voronin-preventive-social-capital|preventive social capital framework]] — отношения со спикерами надо строить заранее, чтобы иметь выбор по fit'у, а не по «кто соглашается».

## Insight: bot-block rate как leading-indicator качества трафика

- У Бескромного 58 заблокировали бота из 310 = 18.7% bot-block rate `[conf:medium, src:2026-05-14]`
- У Воронина (хост) 4 из 72 = 5.6% bot-block rate `[conf:medium, src:2026-05-14]`
- У Амирханяна 7 из 127 = 5.5% `[conf:medium, src:2026-05-14]`

Bot-block rate коррелирует с **«насколько аудитория ожидала именно этого предложения»**. Высокий bot-block → click-фроод или mismatched expectation (пришли по другому ожиданию, увидели лиd-magnet bot — заблокировали). Низкий bot-block → аудитория «understood the deal» до клика. `[conf:medium, src:2026-05-14]`

Это **раннее качество трафика signal** до того, как смотреть на retention и revenue.

## Сравнение с другими бенчмарками

| Канал | Benchmark | Source |
|---|---|---|
| Cross-promo speaker-swap (this page) | 53.72% mean конверсия, 11.1% bot-block | `[conf:medium, src:2026-05-14]` |
| Telegram Ads (этот пресет) | См. [[evolving-strict/campaign-metrics/telegram-ads-benchmarks-2026]] | — |
| hh.ru × Вкусно — и точка (брендированные vacancy pages) | ×27.3 откликов, ×98 просмотров | См. [[canon-strict/historical-campaigns/hh-ru-brand-center-cases-2025-2026]] |
| UGC CPV | См. [[evolving-strict/campaign-metrics/ugc-cpv-benchmarks-2026]] | — |

Cross-promo speaker-swap **не сравним напрямую с paid channels** по unit economics, потому что cost-zero. Сравним по quality: 53.72% конверсия — выше типичной для cold paid-traffic в Telegram (обычно 15–30% по нашему ad-benchmark-стеку) `[conf:medium, src:2026-05-14]`, но это объясняется warm-nature peer-promo (доверие спикеру передаётся на аудиторию).

## Caveats

- **Один snapshot, один организатор.** Не репрезентативно для всего РФ-сегмента 2026 — масштаб 1152 человек, но всего 8 спикеров одной cohort'ы (Атланты-circle). Воспроизводимость на других cohorts (например, IT-сегмент) не верифицирована.
- **Методика не раскрыта.** «Вошло в бот» — uniques или sessions? Timeframe замера? Включает ли pre-event push или только cold-traffic? Без методички цифры — directional, не precise.
- **Конверсия = подписался на канал Воронина**, не = посмотрел конференцию. Real attendance rate отдельно (обычно для free-webinar'ов 25–40% от регистраций) `[conf:low, src:2026-05-14]`.
- **Self-reported данные** организатора. Может быть оптимистичное rounding или selective disclosure (плохие cohorts не показаны).
- **Snapshot за несколько часов до конференции** — после конференции цифры могут сильно поменяться (массовый block-после-получения-материалов).

## Re-verify

TTL для evolving-strict — soft 180 дней. Re-verify: 2026-11-14. Если появятся аналогичные snapshot'ы от других организаторов RU-Telegram-конференций — переоценить medians и canonical-ranges.

## Связанные страницы

- [[canon/marketing-frameworks/voronin-preventive-social-capital]] — preconditions для speaker-swap (как собирать peer-network до event'а)
- [[evolving-strict/campaign-metrics/telegram-ads-benchmarks-2026]] — сравнение с paid Telegram
- [[evolving-strict/campaign-metrics/ugc-cpv-benchmarks-2026]] — альтернативный organic-канал
- [[evolving/content-trends/branded-media-tg-cross-channel-pattern]] — другой cross-channel-pattern в Telegram
- [[volatile/weekly-digest/voronin-community-tech-feb-apr-2026]] — апрельский Атланты Сити event-marketing микс
- [[sources/2026-05-14-tg-community-tech-voronin-may-2026]]
- [[canon/marketing-frameworks/partnerships-growth-multiplier]]
