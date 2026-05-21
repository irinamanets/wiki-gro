---
id: mkt:evolving-strict/market-data/comscore-ai-search-adoption-2026-05
title: "Comscore AI Intelligence Report: 34,9% Google-поисков с AI-обзором (конец 2025)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ai-search, seo, comscore, google, bing, ai-overviews, copilot, organic-traffic, benchmark, search]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-cossaru-may-14-19-2026.md]
namespace: mkt
---

# Comscore AI Intelligence Report — adoption AI-обзоров в поиске (конец 2025)

Comscore [опубликовал отчёт](https://www.comscore.com/Insights/Presentations-and-Whitepapers/2025/AI-Intelligence-Report), официально подтверждающий, что AI-обзоры в поисковой выдаче — больше не эксперимент, а массовое явление. Данные процитированы в [[sources/2026-05-19-tg-cossaru-may-14-19-2026|Cossa @cossaru пост 23157]] (2026-05-18). Это **первый известный нам публичный benchmark доли AI-обзоров в Google по итогам года**, дополняющий RU-практик-замеры из [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]] и [[evolving-strict/market-data/ru-ai-search-traffic-share-2026]].

## Adoption AI-обзоров

| Метрика | Значение | Контекст | Source |
|---|---|---|---|
| Google-запросы с AI-обзором | **34,9%** | конец 2025 (IV квартал) | `[conf:high, src:2026-05-18]` |
| Google-запросы с AI-обзором | **25,9%** | июнь 2025 (baseline) | `[conf:high, src:2026-05-18]` |
| Bing-запросы с Copilot | **15,7%** | декабрь 2025 | `[conf:medium, src:2026-05-18]` |
| Bing-запросы с Copilot | **13,7%** | ноябрь 2025 | `[conf:medium, src:2026-05-18]` |
| Bing-запросы с Copilot | **11,7%** | октябрь 2025 | `[conf:medium, src:2026-05-18]` |

**Динамика Google:** рост с 25,9% (июнь) до 34,9% (конец года) — почти +9 п.п. за полгода `[conf:high, src:2026-05-18]`. Основной скачок пришёлся на IV квартал 2025. Bing рос медленнее (около полугода держался у 11%, затем октябрь→декабрь поднялся с 11,7% до 15,7%) `[conf:medium, src:2026-05-18]`.

## Замедление роста поисковой активности

| Метрика | Значение | Контекст | Source |
|---|---|---|---|
| Рост поисков в США (YoY) | **+3%** | IV квартал 2025 | `[conf:high, src:2026-05-18]` |
| Рост поисков в США (YoY) | **+12%** | IV квартал 2024 | `[conf:high, src:2026-05-18]` |
| Общий объём поисков | 77 млрд → 78 млрд | I кв. → IV кв. 2025 (почти неизменно) | `[conf:high, src:2026-05-18]` |

**Интерпретация:** темпы роста числа поисков резко упали (с +12% до +3% YoY) при практически неизменном абсолютном объёме (77→78 млрд) `[conf:high, src:2026-05-18]`. Полной остановки поиска не произошло, но **классический поиск вышел на плато** — пользователи всё чаще получают готовый ответ в AI-обзоре, не переходя по ссылкам. Это zero-click-сдвиг, измеренный на уровне поисковой платформы, а не отдельных сайтов.

## Прогноз

| Прогноз | Горизонт | Source |
|---|---|---|
| AI-поиск обгонит традиционный по объёму привлекаемого трафика | **2028** | `[conf:medium, src:2026-05-18]` |

Прогноз согласуется с ранее зафиксированными сигналами: Gartner −25% органики к концу 2026 ([[evolving/industry-trends/ai-search-aeo-geo-2026|Кумар Виас update]]), McKinsey $3–5 трлн agentic commerce к 2030 ([[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]]), Brand Analytics −33–38% RU-органики за 2025 `[conf:low, src:2026-05-18]`.

## Импликация для GRO

- Comscore даёт **global/US-замер платформенного уровня** (доля запросов с AI-обзором), тогда как ранее в вики были преимущественно **outcome-замеры на уровне сайтов** (Duda +320% трафика `[conf:low, src:2026-05-18]`, RU practitioner доли AI-трафика). Эти два слоя данных комплементарны: Comscore показывает **охват canvas'а**, site-level замеры — **дельту для тех, кто попал в ответ**.
- Если треть Google-поисков уже содержит AI-обзор, то отсутствие GRO-контента в retrieval-корпусе означает потерю видимости в трети поисковых сессий. Это количественное обоснование GEO/AEO-приоритета.
- **Caveat:** замер Google/Bing — это US-рынок. Для RU-аудитории GRO приоритетен Яндекс/Алиса (см. [[evolving/industry-trends/ai-search-aeo-geo-2026|RU-специфика decision-layer]]); RU-доли AI-обзоров отдельно — в [[evolving-strict/market-data/ru-ai-search-traffic-share-2026]] и [[evolving-strict/market-data/ru-ai-search-interest-2025-2026]].

## Caveats

1. **Pass-through через Cossa:** цифры процитированы из поста Cossa, цитирующего отчёт Comscore, без прямого доступа к самому отчёту. Перед использованием в маркетинговых материалах GRO — достать оригинал Comscore AI Intelligence Report 2025 и переподтвердить методологию (что именно считается «запросом с AI-обзором», география выборки).
2. **«Доля запросов с AI-обзором» ≠ доля кликов/трафика.** AI-обзор может показываться, но пользователь всё равно может перейти по ссылке. Это метрика **присутствия AI-блока**, не conversion / click-share.
3. **Bing-данные помесячные, Google — полугодовые** — методологии замера могут отличаться, прямое сравнение Google vs Bing процентов делать осторожно.

## Contradictions

_Противоречий с другими страницами вики нет. Цифры согласуются с RU practitioner-сигналами (30–40% падения органики `[conf:low, src:2026-05-18]`), Gartner-прогнозом и Brand Analytics-замером._

## Связанные страницы
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — родительский тренд (decision-layer, AEO/GEO)
- [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]] — Adobe / McKinsey / Gartner / Brand Analytics бенчмарки
- [[evolving-strict/market-data/ru-ai-search-traffic-share-2026]] — RU доли AI-трафика B2B/B2C
- [[evolving-strict/market-data/ru-ai-search-interest-2025-2026]] — RU интерес к AI-поиску (Яндекс/Алиса)
- [[sources/2026-05-19-tg-cossaru-may-14-19-2026]] — первоисточник (Cossa @cossaru пост 23157)

## Backlinks

_To be populated by wiki-lint._
