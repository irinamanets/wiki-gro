---
id: mkt:evolving-strict/competitor-metrics/nebius-arr-2025-2026
title: "Nebius (Волож) — ARR и динамика 2025–2026"
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [nebius, volozh, ai-infrastructure, arr, neocloud, eigen-ai]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-14  # +Q1 2026 actuals: выручка $399M (+684% YoY), капекс $2.5B, кап $52.6B, акции +16% на отчёте (Edinorog 7948 от 14 мая)
sources: [sources/2026-05-05-dzen-nebius-eigen-acquisition.md, sources/2026-05-05-dzen-ru-condensed.md, sources/2026-05-14-tg-theedinorog-may-2026.md]
namespace: mkt
---

# Nebius (Волож) — ARR и сделки 2025–2026

Контрольный срез ARR-метрик и публичных сделок Nebius Group, актуально на май 2026.

## ARR прогресс

| Период | ARR | Source |
|---|---|---|
| Конец 2025 | **$1,25 млрд** | `[conf:high, src:2026-05-05]` |
| Прогноз конец 2026 | **$7–9 млрд** | `[conf:high, src:2026-05-05]` |
| Рост за год (центральная оценка $8 млрд) | **×6,4** | `[conf:high, src:2026-05-05]` |
| Диапазон роста | **×5,6–7,2** | `[conf:high, src:2026-05-05]` |

## Сделка Eigen AI (май 2026)

| Параметр | Значение | Source |
|---|---|---|
| Сумма сделки | **$643 млн** | `[conf:high, src:2026-05-05]` |
| Acquired company | Eigen AI (inference + post-training алгоритмы) | `[conf:high, src:2026-05-05]` |
| Интеграция | Nebius Token Factory | `[conf:high, src:2026-05-05]` |
| Реакция акций | **+14,2%** до **$176,42** | `[conf:high, src:2026-05-05]` |

## Связанные публичные числа Q4 2025 (с других ингестов)

Из [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] (более ранний срез того же объекта):

| Метрика | Значение | Период | Source |
|---|---|---|---|
| Выручка Q4 2025 | **$227,7 млн** (+547% г/г) | Q4 2025 | `[conf:high, src:2026-05-05]` |
| Годовая выручка 2025 | **$529,8 млн** (+479% г/г) | 2025 | `[conf:high, src:2026-05-05]` |
| Caveat (промах от консенсуса) | Ниже ожиданий аналитиков ($246,1 млн консенсус Q4) | Q4 2025 | `[conf:high, src:2026-05-05]` |

## Q1 2026 — официальный отчёт (13 мая 2026)

Через VC и Edinorog 7948 (14 мая) — [[sources/2026-05-14-tg-theedinorog-may-2026]]:

| Метрика | Значение | Source |
|---|---|---|
| Выручка Q1 2026 | **$399 млн (+684% YoY)** | `[conf:high, src:2026-05-13]` |
| Капекс Q1 2026 | **$2,5 млрд** (расширение дата-центров, чипы, оборудование) | `[conf:high, src:2026-05-13]` |
| Капитализация (после отчёта) | **$52,6 млрд** | `[conf:high, src:2026-05-13]` |
| Реакция акций | **+16% за день** на отчёте | `[conf:high, src:2026-05-13]` |

**Аналитический комментарий:** $399M Q1 vs $227.7M Q4 2025 = **+75% QoQ** — ускорение роста `[conf:high, src:2026-05-13]`. ARR-следствие (annualized run rate из Q1 2026 × 4): **$1.6 млрд** на 31 марта 2026 vs **$1.25 млрд** end-2025 (×1.28 за квартал) `[conf:medium, src:2026-05-13]`. Если темп сохранится — fits to upper-bound guidance $7–9B end-2026 `[conf:medium, src:2026-05-13]`.

**Капекс vs выручка:** $2.5B за квартал vs $399M выручки = capital intensity ratio **6.3×**. Это характерно для neocloud-стадии «build-out before scale» — Nebius сейчас не оптимизирует прибыль, а **захватывает compute-инфраструктуру** как long-term moat.

## Caveats

1. **ARR vs выручка.** Числа $1,25 млрд (ARR end-2025) и $529,8 млн (выручка 2025) — разные метрики:
   - ARR = annualized run rate, рассчитанный из последнего квартала × 4
   - Annual revenue = фактический оборот за календарный год
   ARR обычно выше revenue в быстрорастущих компаниях. Нельзя складывать или сравнивать напрямую.
2. **Прогноз $7–9 млрд ARR end-2026** — guidance менеджмента, не консенсус аналитиков. Используется в маркетинге Nebius как target. Confidence: high (источник — официальные коммуникации Nebius), но фактическое исполнение остаётся открытым риском.
3. **Eigen AI** — не публично торгуемая компания, оценка $643 млн = сумма сделки, не market cap.

## Что это значит — для контента

1. **«Бывший CEO Yandex строит AI-инфраструктурную компанию с прогнозируемым ×6 ростом за год»** — сильный нарратив для русскоязычной аудитории, ищущей роле-моделей в мировом AI.
2. **Контент-возможность.** Разобрать differentiation Nebius vs CoreWeave, Crusoe, Lambda — какие architecture-выборы определяют growth-trajectory.
3. **Anti-pattern.** Не использовать Nebius как пример «обычного AI-стартапа» — это не стартап, а scale-up в публичном поле с прозрачной финансовой отчётностью. Это другой класс кейса.

## Связанные страницы

- [[volatile-strict/competitor-news/nebius-eigen-acquisition-2026-05]] — детали сделки
- [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] — broader контекст AI-валюаций
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий AI-race нарратив
- [[sources/2026-05-05-dzen-nebius-eigen-acquisition]]

## Backlinks

_6 pages link to this one._

- [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]]
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-dzen-ru-condensed]]
- [[volatile-strict/competitor-news/nebius-eigen-acquisition-2026-05]]
