---
id: mkt:evolving-strict/competitor-metrics/squaremind-funding-2026
title: SquareMind — финансовые метрики и commercialization-lag (май 2026)
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [squaremind, medtech, dermatology, ai-imaging, funding, fda, ce-mark, commercialization-lag, france, usa]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-startupoftheday-may-20-26-2026.md]
namespace: mkt
---

# SquareMind — финансовые метрики (май 2026)

Франко-американский медтех-стартап, AI-робот для скрининга рака кожи. Извлечено из поста 5076 [@startupoftheday](https://t.me/startupoftheday) от 2026-05-20 (см. [[sources/2026-05-26-tg-startupoftheday-may-20-26-2026]]).

Сайт: [squaremind.com](https://www.squaremind.com/).

## Продукт

«Фотобудка с роборукой»:
- Пациент раздевается, заходит в установку
- За несколько минут робот делает снимки всего тела
- AI склеивает снимки в body-map, подсвечивает подозрительные родинки
- Живой дерматолог смотрит готовый результат вместо лазания с лупой

## Целевая экономика клиента

| Показатель | Значение | Source |
|---|---|---|
| Экономия зарплаты врача за приём (США) | ~$100 | `[conf:medium, src:2026-05-20]` |
| Ориентировочная цена робота | до $500 000 (вероятно, в разы меньше) | `[conf:low, src:2026-05-20]` |
| Теоретическая окупаемость | ~2 года | `[conf:medium, src:2026-05-20]` |

## Funding и регуляторика

| Показатель | Значение | Source |
|---|---|---|
| Время разработки (на момент мая 2026) | 7 лет | `[conf:high, src:2026-05-20]` |
| FDA сертификация (США) | получена | `[conf:high, src:2026-05-20]` |
| EU сертификация (CE Mark) | получена | `[conf:high, src:2026-05-20]` |
| Объём последнего раунда (май 2026) | $18 млн | `[conf:high, src:2026-05-20]` |
| Проданных установок (на момент привлечения) | 0 | `[conf:medium, src:2026-05-20]` |

## Commercialization-lag pattern

SquareMind иллюстрирует наблюдаемый паттерн «**регуляторика ≠ продажи**» в медтехе:

1. **7 лет разработки** — медицинский R&D-цикл с регуляторными gates обычно занимает 5-10 лет, не аномалия.
2. **FDA + EU сертификация** получены — формально продукт можно продавать на двух крупнейших рынках мира.
3. **Ноль продаж** — продукт не покупается, несмотря на сертификацию.
4. **$18M раунд** — фонды поверили обещанию «вот-вот начнут продавать», но это **bet на будущую коммерциализацию**, не на текущий traction.

Это второй случай в @startupoftheday канале с похожей структурой за весну 2026 — pattern зафиксирован в [[evolving/industry-trends/medtech-commercialization-lag-pattern-2026]].

### Гипотезы о причинах lag'а

(не подтверждены в источнике, маркетинговые гипотезы для собственного использования):

1. **Procurement-cycle больниц** длиннее, чем cycle SaaS-продаж (12-36 месяцев discovery → trial → contract).
2. **Compliance внутри больницы** (HIPAA training, integration с EMR) добавляет 6-12 месяцев после подписания контракта.
3. **Reimbursement-coding** (CPT codes для нового типа диагностики) требует отдельной работы с страховщиками.
4. **Education-need** дерматологического сообщества — врачей нужно учить интерпретации AI-вывода.
5. **Capital-cost barrier** — даже $500K оборудование за капекс сложно подписать без 2-3 лет doable-pipeline.

## Маркетинговая интерпретация для GRO-контекста

GRO **не работает** в медтехе, но **observable pattern** «certification без commercialization» применим к любому продукту, где регуляторика/сертификация воспринимается как proxy traction:

- **AI-инструменты с certification badges** (SOC2, ISO27001, FedRAMP) — это **не traction**, а access-control.
- **GRO в B2B-канале (Интенсив)** при работе с корпоративными клиентами столкнётся с похожим procurement-cycle latency.

Это уроки про **не путать compliance-readiness с product-market-fit**.

## Связанные страницы

- [[evolving/industry-trends/medtech-commercialization-lag-pattern-2026]] — pattern, к которому SquareMind — proof-point
- [[canon/marketing-frameworks/dream-vs-numbers-valuation-thesis-gorny-spacex]] — Архетип A («покупают мечту»): $18M на 0-revenue стартап
- [[sources/2026-05-26-tg-startupoftheday-may-20-26-2026]]

## Источник

Александр Горный, пост 5076 [@startupoftheday](https://t.me/startupoftheday) от 2026-05-20 `[conf:high, src:2026-05-20]`.
