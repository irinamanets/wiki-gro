---
id: mkt:evolving-strict/market-data/ai-personalization-benchmarks-2026
title: "Бенчмарки эффекта AI-персонализации (Persado, Movable Ink, Klarna, Shopify, Bank of America) 2024–2026"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ai, personalization, benchmarks, e-commerce, email, sms, push, klarna, shopify, persado]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-dzen-inc-personalization-vs-manipulation.md, sources/2026-05-05-dzen-ru-condensed.md]
namespace: mkt
---

# Бенчмарки AI-персонализации 2024–2026

Сводка публичных кейсов с числами, демонстрирующих качественный эффект AI-персонализации. Источник — long-form Inc. Russia 5 мая 2026 (Григорий Щеглов, эксперт Дмитрий Юдин, Cloud.ru / НИУ ВШЭ). Большая часть кейсов — отчёты вендоров (Persado, Movable Ink, Klarna), confidence: medium при использовании в маркетинговом контенте.

## Сводная таблица

| Компания / кейс | Метрика | Значение | Период | Source |
|---|---|---|---|---|
| Carrefour × Persado | Рост конверсии в SMS и push | **+42%** | до 2026 | `[conf:medium, src:2026-05-05]` |
| Ballard Designs × Movable Ink | Рост выручки с одной email-рассылки | **×25** | до 2026 | `[conf:medium, src:2026-05-05]` |
| Shopify (внутренняя статистика) | Рост трафика из ИИ-поиска за год | **×8** | 2025 → 2026 | `[conf:medium, src:2026-05-05]` |
| Shopify (внутренняя статистика) | Рост заказов из ИИ-источников за год | **×15** | 2025 → 2026 | `[conf:medium, src:2026-05-05]` |
| E-commerce (общий бенчмарк) | Прирост выручки от ИИ-персонализации | **+5–15%** | 2024–2026 | `[conf:medium, src:2026-05-05]` |
| E-commerce (smart рекомендации) | Доля выручки страницы товара через «умный» блок | **до 31%** | 2024–2026 | `[conf:medium, src:2026-05-05]` |
| E-commerce (адаптивная лента) | Превышение конверсии над static-лентой | **×4,5** | 2024–2026 | `[conf:medium, src:2026-05-05]` |
| Bank of America Erica | Совокупное число взаимодействий | **3 млрд** | 2018–2025 | `[conf:medium, src:2026-05-05]` |
| Bank of America Erica | Из них проактивных | **1,7 млрд** | 2018–2025 | `[conf:medium, src:2026-05-05]` |
| Bank of America (контекстные предложения) | Рост выручки через Erica | **+19%** | 2018–2025 | `[conf:medium, src:2026-05-05]` |
| Klarna AI-ассистент | Диалогов в первый месяц после запуска | **2,3 млн** | февраль 2024 | `[conf:high, src:2026-05-05]` |
| Klarna AI-ассистент | Доля от всех клиентских обращений | **2/3** | февраль 2024 | `[conf:high, src:2026-05-05]` |
| Klarna (среднее время решения обращения) | До запуска ассистента | **11 минут** | до фев 2024 | `[conf:high, src:2026-05-05]` |
| Klarna (среднее время решения обращения) | После запуска ассистента | **<2 минут** | с фев 2024 | `[conf:high, src:2026-05-05]` |

## Технический бенчмарк (latency)

- Между открытием страницы и финальным контентом — **~8 вызовов к разным моделям** `[conf:medium, src:2026-05-05]`
- Полный цикл (сбор сигналов → contextual bandits → финальный контент) — **<200мс** `[conf:medium, src:2026-05-05]`

## Caveats при использовании этих чисел

1. **Бенчмарки от вендоров.** Persado, Movable Ink — это вендоры персонализации; кейсы Carrefour и Ballard приводятся в маркетинговых материалах самих вендоров. Числа +42% / ×25 — peak-кейсы, а не median. При цитировании в контенте указывать «по данным вендора». `[conf:medium, src:2026-05-05]`
2. **«Прирост выручки 5–15%»** — общий разброс по индустрии, не конкретный замер. Это полезно как conservative anchor («даже на нижней границе значительный эффект»). `[conf:medium, src:2026-05-05]`
3. **Klarna 2/3 обращений** — относится к customer support, не к маркетинг-обращениям.
4. **Контекст применимости** — эти числа показывают, что **в 2026 году AI-персонализация уже доказала измеряемый эффект**, а не остаётся «гипотезой». Это анти-фрейм для скептиков.

## Связанные страницы

- [[evolving/industry-trends/ai-personalization-industrial-shift-2026]] — качественный нарратив тренда
- [[canon/marketing-frameworks/ai-personalization-4-layer-architecture]] — техническая разборка
- [[canon/marketing-frameworks/yudin-personalization-vs-manipulation-test]] — этический тест
- [[canon/marketing-frameworks/real-time-personalization-cvm-mechanics]] — каноническая CVM-архитектура
- [[sources/2026-05-05-dzen-inc-personalization-vs-manipulation]]

## Backlinks

_10 pages link to this one._

- [[canon/marketing-frameworks/ai-personalization-4-layer-architecture]]
- [[canon/marketing-frameworks/real-time-personalization-cvm-mechanics]]
- [[canon/marketing-frameworks/yudin-personalization-vs-manipulation-test]]
- [[evolving-strict/market-data/meta-ads-experiment-2026]]
- [[evolving-strict/product-metrics/vk-video-recommendation-uplift-2026]]
- [[evolving/industry-trends/ai-personalization-industrial-shift-2026]]
- [[evolving/industry-trends/t1-forum-6-it-trends-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-dzen-ru-condensed]]
