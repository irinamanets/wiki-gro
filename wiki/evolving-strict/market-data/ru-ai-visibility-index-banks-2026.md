---
id: mkt:evolving-strict/market-data/ru-ai-visibility-index-banks-2026
title: "RU-индекс «ИИ-видимости» брендов — первый публичный (AIMonitor.pro, май 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [geo, aeo, ai-search, ru-market, brand-visibility, share-of-voice, banks, llm-citation, brightedge]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-incrussiamedia-may-11-17-2026.md]
namespace: mkt
---

# RU-индекс «ИИ-видимости» брендов — первый публичный (AIMonitor.pro)

Май 2026: в России появился **первый публичный индекс «ИИ-видимости» брендов** — метрика того, как часто и в каком контексте нейросети упоминают компанию в ответах. Составлен профильной платформой **AIMonitor.pro**, передан Inc. Russia ([[sources/2026-05-19-tg-incrussiamedia-may-11-17-2026|пост 36801, 2026-05-15]]). Это первый RU-датапоинт, операционализирующий теоретическую рамку GEO-мониторинга на конкретной вертикали (банки).

## Почему `evolving-strict`

Числовой срез share-of-voice брендов в AI-выдаче — это **метрика с дрейфом**: индекс пересчитывается по мере того, как банки наращивают GEO-присутствие и retrieval-базы моделей обновляются. Каждое число с inline-маркером, hard re-verify каждые 3–6 месяцев. Концептуальная (стабильная) рамка измерения — в [[canon/marketing-frameworks/geo-monitoring-discipline-2026]]; этот срез — её первый публичный RU-инстанс.

## Методология индекса

- Платформа: **AIMonitor.pro** (профильный RU-сервис измерения ИИ-видимости) `[conf:medium, src:2026-05-15]`
- Охват: проанализировано **более 40 тыс. запросов** `[conf:medium, src:2026-05-15]`
- Модели в выборке: **ChatGPT, DeepSeek, Perplexity, «Алиса AI»** `[conf:medium, src:2026-05-15]`
- Метрика: индекс «ИИ-видимости» (доля/частота упоминания бренда в ответах моделей по релевантным запросам), выражен в % `[conf:medium, src:2026-05-15]`

`confidence: medium` — методология индекса (нормировка %, веса платформ, формула композиции) в посте не раскрыта; цифры публикует сам вендор-платформа через деловое медиа. Для критических решений требуется верификация на первоисточнике AIMonitor.pro.

## Топ-5 RU-банков по ИИ-видимости (май 2026)

| Место | Банк | ИИ-видимость | Source |
|---|---|---|---|
| 1 | «Сбер» | 26,7% | `[conf:medium, src:2026-05-15]` |
| 2 | Т-Банк | 19,1% | `[conf:medium, src:2026-05-15]` |
| 3 | ВТБ | 17,9% | `[conf:medium, src:2026-05-15]` |
| 4 | Альфа-Банк | 14,8% | `[conf:medium, src:2026-05-15]` |
| 5 | «Открытие» | 5,4% | `[conf:medium, src:2026-05-15]` |

**Наблюдение:** топ-5 покрывает **84,9%** совокупной видимости категории `[conf:medium, src:2026-05-15]` — сильная концентрация. Разрыв лидера (Сбер 26,7%) и пятого места («Открытие» 5,4%) — почти **×5** `[conf:medium, src:2026-05-15]`. Это commerce-аналог классического SERP-доминирования: в нейровыдаче, как и в Google, видимость распределена по power-law, а не равномерно.

## Глобальный контекст (BrightEdge)

Пост приводит два глобальных бенчмарка от BrightEdge как обоснование, зачем индекс вообще нужен:

- **68% маркетологов** уже адаптируют стратегии под ИИ-поиск `[conf:medium, src:2026-05-15]`
- Трафик из генеративных систем вырос на **180% за 2025 год** `[conf:medium, src:2026-05-15]`

Оба числа согласуются с уже зафиксированным в вики паттерном ускорения AI-search (см. [[evolving-strict/market-data/comscore-ai-search-adoption-2026-05]] и [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]]) — глобальный рост AI-трафика на сотни процентов при падении классической органики.

## Что это значит для маркетинга GRO

1. **Появился измеримый инструмент GEO-мониторинга в RU** — то, что [[canon/marketing-frameworks/geo-monitoring-discipline-2026|дисциплина GEO-мониторинга]] описывает как «контрольный список запросов + share-of-voice», теперь существует как готовый сервис (AIMonitor.pro) для RU-рынка. Для GRO это снижает порог входа в baseline-аудит ИИ-видимости.
2. **Бенчмарк концентрации** — power-law (топ-5 = ~85% видимости) означает, что в нейровыдаче «нет середняков»: либо ты в топе категории, либо тебя AI не цитирует вовсе. Для нишевого SaaS (профиль GRO) это аргумент за раннее GEO-инвестирование, пока категория «приложения для тренировки мышления» не консолидировалась вокруг 2–3 имён. [conf:low, src:2026-05-19]
3. **Банки как leading indicator** — финсектор первым получил публичный индекс, потому что там высокая частота AI-запросов и большие GEO-бюджеты. Edtech / self-improvement (где играет GRO) пойдёт следом; стоит заранее войти в retrieval-корпус, чтобы попасть в первый же индекс категории с ненулевой долей.
4. **Метрика для борда** — индекс в % даёт нефинансовый, но объективный KPI эффективности content/PR-программы, который можно показывать инвесторам как «share of AI voice растёт».

## Contradictions

_Пока нет._

## Связанные страницы

- [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] — концептуальная рамка измерения, которую этот индекс инстанцирует
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — родительский content-trend (AEO/GEO playbook)
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — родительский industry-trend
- [[evolving-strict/market-data/ru-ai-search-traffic-share-2026]] — RU-метрики долей AI-трафика по проектам
- [[evolving-strict/market-data/ru-ai-trust-citation-2026]] — RU trust/citation сигналы (28% доверяют ИИ / 87% без ссылки) [conf:low, src:2026-05-19]
- [[evolving-strict/market-data/comscore-ai-search-adoption-2026-05]] — глобальный AI-search adoption бенчмарк
- [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]] — commerce-бенчмарки AI-выдачи
- [[canon/positioning/gro-value-proposition]] — список целевых запросов GRO для замера видимости
- [[sources/2026-05-19-tg-incrussiamedia-may-11-17-2026]] — первоисточник (Inc. Russia, AIMonitor.pro index)
