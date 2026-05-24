---
id: mkt:evolving-strict/market-data/ru-bnpl-aov-uplift-2023
title: "BNPL в РФ — AOV uplift и осведомлённость рынка (2023, Долями × Рив Гош)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [bnpl, market-data, retail, e-commerce, payments, aov, doly, tinkoff, t-bank, russia]
confidence: high
stale: false
created: 2026-05-15
updated: 2026-05-24  # +forward-link на follow-up business-turnover study 2024 (×3 оборота, кейс Mollis) из chunk6 condensed
sources: [sources/2026-05-14-condense-web-vc-ru-tbank-27.md, sources/2026-05-24-condense-vc-ru-tbank-chunk6-30.md]
namespace: mkt
---

# BNPL в РФ — AOV uplift и осведомлённость рынка (2023)

Опубликованные Т-Банком цифры из кейса **Долями × Рив Гош (2023)** дают anchor-точку по двум вертикальным метрикам российского BNPL-рынка: (1) **uplift среднего чека** при использовании BNPL и (2) **осведомлённость / использование** BNPL у потребителей.

## Ключевые цифры

### AOV uplift (кейс Рив Гош)

| Метрика | Без BNPL | С BNPL (Долями) | Uplift | Source |
|---|---|---|---|---|
| Средний чек | 5 500 ₽ | 7 000 ₽ | **+26%** | `[conf:high, src:2023-01-01]` |

### Оборотные эффекты Рив Гош

| Метрика | Значение | Source |
|---|---|---|
| Оборот от Долями YoY | **+26%** | `[conf:high, src:2023-01-01]` |
| E-com Рив Гош total YoY | **+37%** | `[conf:high, src:2023-01-01]` |
| Tinkoff Shopping (vendor platform) | **×7 рост** за год до публикации (2022→2023) | `[conf:medium, src:2023-01-01]` |

### Rynок BNPL РФ (2023)

| Метрика | Значение | Source |
|---|---|---|
| Осведомлённость потребителей о BNPL | **93%** | `[conf:high, src:2023-01-01]` |
| Фактическое использование BNPL | **40%** | `[conf:high, src:2023-01-01]` |

## Интерпретация

### AOV +26% — что это значит `[conf:high, src:2023-01-01]`

BNPL-механика добавляет в чек **~1 500 ₽** среднего uplift'а — это **разница «купил vs купил больше»**. Когда оплата разбивается на 4 части, психологический порог покупки снижается: пользователь добавляет 1–2 дополнительные позиции, которые «не вошли бы» в чек при полной оплате сразу. `[conf:high, src:2023-01-01]`

Эффект подтверждается **двойным сигналом**:
- AOV +26% (рост среднего чека) `[conf:high, src:2023-01-01]`
- Оборот от Долями +26% YoY (рост total volume через канал) `[conf:high, src:2023-01-01]`

Эти числа двинулись **синхронно**, что означает: рост идёт не из roof-attraction новых клиентов (тогда оборот вырос бы быстрее AOV), а из **changing behavior существующих клиентов** в сторону больших корзин.

### Tinkoff Shopping ×7 — что это значит

Платформа Tinkoff Shopping (агрегатор предложений ритейлеров внутри банковского приложения) выросла в 7 раз за год. Это **косвенный сигнал** о том, что российские потребители 2023 рассматривают банковское приложение как **e-commerce surface**, не только как расчётный инструмент. Параллельно с этим — открытие Tinkoff Выгода и Клубы лояльности (см. [[canon-strict/historical-campaigns/tbank-loyalty-clubs-pilot-2024]]).

### 93% осведомлённость / 40% использование — gap `[conf:high, src:2023-01-01]`

**53 п.п. разрыв** между «знаю про BNPL» и «использую BNPL» — это **head room** для роста. Каждый процент конверсии из «знаю» в «использую» = миллионы новых транзакций. Это объясняет агрессивную экспансию Долями / Яндекс Сплит / Ozon Installment в 2023–2024.

## Связь с современным BNPL-пейзажем

| BNPL-провайдер | Parent ecosystem | Sub-brand | Палитра | Reference |
|---|---|---|---|---|
| **Долями** | T-Bank | Доли | Lavender | [[evolving/competitor-positioning/tbank-doli-bnpl-sub-brand-palette-lavender]] |
| Яндекс Сплит | Яндекс | inherited | Yandex red/yellow | adjacent |
| Ozon Installment | Ozon | inherited | Ozon blue | adjacent |
| Yoomoney Installment | Yoomoney | inherited | Yoomoney purple | adjacent |

К 2026 году Долями стал **5-м sub-brand** в T-Bank group с distinct lavender-palette (см. [[evolving/competitor-positioning/tbank-doli-bnpl-sub-brand-palette-lavender]]) — это **визуальная капитализация BNPL-успеха 2023**. Метрики 2023 года + операционный track-record на 2 года → инвестиция в отдельную brand-identity была обоснована.

**Follow-up (2024):** AOV-эффект 2023 (+26% на чеке) развёрнут Т-Банком в **бизнес-уровневый turnover-эффект** — бизнес с рассрочкой в среднем ×3 оборота (медуслуги ×5, образование ×4), кейс Mollis +53% средний чек. Детали — [[evolving-strict/market-data/ru-bnpl-business-turnover-effect-2024]]. [conf:low, src:2026-05-24]

## Применение для GRO

1. **«Подписка в рассрочку» как conversion-lever.** Если GRO добавит pay-later для годовой подписки (12 × месячный платёж становится 4 × квартальный платёж), AOV-логика +26% переносится: пользователь, который не покупает annual из-за **psychological barrier**, конвертируется на pay-later структуре. `[conf:high, src:2023-01-01]`
2. **Партнёрство с BNPL-провайдером (Долями / Яндекс Сплит).** Для физических товаров от GRO (тренажёры, спортпит) — direct integration с одним из BNPL-провайдеров. Метрика AOV +26% — solid ROI argument для merchant'а. `[conf:high, src:2023-01-01]`
3. **Awareness-gap в фитнес-вертикали.** 93% знают про BNPL, но только 40% используют — те же 53 п.п. разрыва скорее всего работают и в нишевых вертикалях. Контент-маркетинг GRO может использовать «как платить за подписку частями» как **education-driven funnel**. `[conf:high, src:2023-01-01]`
4. **Anti-pattern: не использовать BNPL для импульсивных мелких сумм.** AOV-эффект работает на **среднем чеке** ~5–7K. Для GRO-цен 2.5K в месяц BNPL не даст того же uplift'а — структура не соответствует threshold'у, где BNPL даёт значимый decision-shift.

## Contradictions / supersession риски

- Метрики 2023 могут **дрейфовать с обновлением рынка**: следующий публичный data-release Долями (если случится) — supersession этих чисел.
- BNPL осведомлённость **может расти** к 2026 (более насыщенный рынок) → 93%/40% gap сужается, и AOV-эффект меняется. `[conf:high, src:2023-01-01]`
- Tinkoff Shopping ×7 — `conf:medium` потому что точная база (что было 1× год назад) не раскрыта.

TTL: 180 дней (`evolving-strict` default), но первая re-verification — при появлении любого нового Долями-relate публичного исследования.

## Связанные страницы

- [[canon-strict/historical-campaigns/tbank-loyalty-clubs-pilot-2024]] — Клубы лояльности (другая B2B2C-механика T-Bank)
- [[evolving-strict/competitor-metrics/tbank-historical-metrics-2019-2024]] — общий контекст метрик T-Bank
- [[evolving/competitor-positioning/tbank-doli-bnpl-sub-brand-palette-lavender]] — Доли sub-brand в 2026
- [[evolving/competitor-positioning/tbank-doli-bnpl-partner-album-format]] — BNPL partner-album формат
- [[evolving-strict/market-data/ru-payment-conversion-2022]] — параллельная payment-метрика
- [[evolving/industry-trends/tbank-corporate-platform-stack-2026]] — современный T-Bank контекст
- [[evolving-strict/market-data/ru-bnpl-business-turnover-effect-2024]] — follow-up: BNPL-эффект на обороты бизнеса (×3) + кейс Mollis
- [[evolving-strict/market-data/ru-consumer-services-research-pr-2024-2025]] — рассрочка на доп.образование (родители)
- [[sources/2026-05-14-condense-web-vc-ru-tbank-27]] — источник
- [[sources/2026-05-14-web-vc-ru-tbank-2066920]] — детальный stub Рив Гош кейса
