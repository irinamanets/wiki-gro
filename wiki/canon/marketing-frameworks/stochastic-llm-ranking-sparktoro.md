---
id: mkt:canon/marketing-frameworks/stochastic-llm-ranking-sparktoro
title: "Стохастичность LLM-выдачи: probabilistic-метрики вместо «позиций» (SparkToro 2961 prompts)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [seo, aeo, geo, ai-search, llm-citation, share-of-voice, stochastic-ranking, sparktoro, measurement, geo-monitoring, brand-visibility]
confidence: high
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-18-pressfeed-geo-illusion-stability-measure.md]
namespace: mkt
---

# Стохастичность LLM-выдачи как фундаментальная природа AI-поиска

## TL;DR

LLM-нейровыдача — **стохастична** по своей архитектуре, не детерминированна. **Понятие «позиции» здесь не работает**. Бренд либо имеет **высокую вероятность** появления при серийных прогонах (стабильный сигнал), либо — **низкую** (случайный шум). GEO-стратегия должна оптимизировать **вероятность**, а не «позицию», и измерять её через **серийные прогоны**, не одиночные.

> «В нейровыдаче нет позиций, есть только вероятность. Именно её надо научиться измерять.»
>
> — Pressfeed, май 2026 ([[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]])

## Почему `canon`

Это **архитектурный факт об LLM-выдаче**, не trend и не tool. Стохастичность retrieval+generation остаётся стабильной между поколениями моделей: при любых улучшениях RLHF и search-augmentation модель **продолжает sample-ить из распределения**, а не возвращать фиксированный rank. Пока LLM-генерация остаётся probabilistic (для всех моделей на горизонте 5+ лет), эта рамка применима без изменений. Конкретные **измеряющие инструменты** меняются — но **сам факт стохастичности** не уйдёт.

## SparkToro benchmark (январь 2026)

Первый широкоизвестный публичный эксперимент по количественному измерению стохастичности:

- **600 участников**
- **2961 идентичный prompt-прогон** через ChatGPT, Claude, Google AI Overviews
- **Вероятность идентичного brand-set при повторе запроса: < 1%** `[conf:high, src:2026-05-18]`
- **При 5 прогонах одного prompt'а: ≈ 20% брендов появляются стабильно** `[conf:high, src:2026-05-18]`
- **Identical sequence of brands — практически невозможна** `[conf:high, src:2026-05-18]`

**Главный SparkToro-вывод:** частота попадания бренда в ответ **определяется не реальным весом бренда на рынке, а насыщенностью тематического кластера** — то есть retrieval-корпус и его структура важнее brand-equity. Это **операционное основание** тезиса Шевченко («попадание в трастовый корпус») и Кравченко («object-oriented retrieval»).

## Главная импликация: единичные прогоны бесполезны

| Что нельзя измерять | Почему |
|---|---|
| «Нас упомянули 20 раз за месяц» | Нет шкалы стабильности; 20 = noise или signal? |
| «AI поставила нас первыми» | Один раз — почти всегда случайность |
| Single-shot prompt run | Любой результат — шум |

| Что нужно измерять | Зачем |
|---|---|
| **Доля релевантных запросов с упоминанием бренда** | Inclusion rate в retrieval-pool |
| **Стабильность при серийных прогонах** (5–10 раз) | Probability density, не moment |
| **Контекст упоминания** (ниша, ценовой сегмент, преимущества) | Качество цитирования, а не только факт |
| **Co-mention pattern** (какие бренды рядом с нашим) | Семантическая категория, в которой AI разместила бренд |

## Operational test

Для каждого ключевого запроса GEO-monitoring:

1. **Запустить 5 прогонов** через каждую целевую платформу (Яндекс Нейро / ChatGPT / Perplexity / Алиса AI / Gemini)
2. **Зафиксировать**: появился ли бренд хоть раз? В скольких из 5? На какой позиции (если упомянут)? В каком контексте?
3. **Рассчитать**:
   - **Probability of inclusion** = (прогонов с упоминанием) / (всего прогонов) × 100%
   - **Citation stability score** — насколько одинаков контекст между прогонами (нужны качественные tags)
4. **Сравнить** с benchmark'ом 20% (SparkToro): бренд в **«стабильном top-20%»** — устойчивое присутствие; меньше — random noise.

**Threshold-интерпретация (рабочая):**

| Probability | Интерпретация |
|---|---|
| ≥ 80% | Стабильное dominant-присутствие в категории |
| 40–80% | Регулярное упоминание; работа GEO даёт effect |
| 20–40% | Появление в «стабильных 20%» SparkToro; работаем дальше |
| < 20% | Random noise; нет реального GEO-присутствия |

## Связь с существующими GEO-страницами

### `geo-monitoring-discipline-2026` (Кравченко)

В [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] **операционная рамка** GEO-monitoring (inclusion / citation quality / competitive parity / trend) — но без **теоретического обоснования**, почему вообще нужно измерять «долю», а не «позицию». SparkToro даёт это обоснование: стохастичность ≡ нет позиций.

**Точка интеграции:** Кравченко-фреймворк операционализирует **что** измерять, SparkToro/эта страница объясняет **почему** именно так.

### `aeo-geo-llm-search-optimization-2026` (Шевченко + Виас + RU practitioners)

В [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] **3 механизма retrieval** (pre-training / RLHF / fine-tuning+search) и **operational playbook** (Кумар Виас). SparkToro добавляет **measurement-сторону**: даже идеально оптимизированный контент даст probability < 100%; нужно измерять distribution, не успех/провал.

### `seo-for-ai-era-playbook` (общий playbook)

В [[canon/marketing-frameworks/seo-for-ai-era-playbook]] — стратегические рекомендации для AI-эпохи. SparkToro/стохастичность — **фундамент** этих рекомендаций (без него план «попасть в топ» невыполним по определению).

## Anti-patterns

1. **Ставить KPI «появиться в первой пятёрке»** — позиции не существует; KPI должен быть probability + inclusion rate.
2. **Удовлетворяться одиночным прогоном** — даже три прогона недостаточно; SparkToro показала, что **≥ 5 прогонов** — минимум.
3. **Сравнивать с конкурентом по одиночному ответу** — конкурент мог быть «верхним 20%» в шумовом распределении, мы — нет; нужны серийные прогоны.
4. **Игнорировать вариативность контекста** — бренд может появляться стабильно, но в неправильной категории (медитационные приложения вместо тренировки бизнес-навыков); это **сигнал репозиционирования AI**, не «успех».
5. **Trust «AI сказала про нас один раз»** — это шум, не сигнал.

## Связь с GRO

Для GRO как продукта раннего этапа AI-visibility:

1. **Baseline GEO-аудит** обязательно с **5+ прогонами на запрос** через 4–6 платформ. Без этого — невозможно отличить «GRO ещё не в retrieval-pool» от «GRO случайно появилась раз».
2. **Реалистичные ожидания**: даже после полноценной GEO-программы probability ≈ 40–60% — нормальный target для нишевого SaaS (на base SparkToro 20% — стабильность для случайного бренда; целенаправленная работа должна дать 2× — но не 100%).
3. **Бюджетная импликация**: GEO — **долгосрочная инвестиция в распределение вероятностей**, а не «попадание в топ» как фиксированный milestone. Quarterly review trend, не binary success/failure check.
4. **Competitive parity baseline** в категории «тренировки мышления / soft skills для предпринимателей» — какова probability у Skillbox / Нетологии / альтернативных приложений? Это бенчмарк, не наш absolute number.

## Связанные страницы

- [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] — операционная рамка измерения (4-осевая)
- [[canon/marketing-frameworks/seo-for-ai-era-playbook]] — общий playbook AI-эпохи
- [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] — онтологическая рамка retrieval (что в графе сущностей)
- [[canon/marketing-frameworks/geo-platform-segmentation-yandex-chatgpt-perplexity]] — три разных retrieval-инфраструктуры (parallel к стохастичности — разные дистрибуции по платформам)
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — родительский content-trend
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — родительский industry-trend
- [[evolving/content-trends/geo-playbook-2026-q2]] — operational playbook Q2 2026 (Кумар Виас механики)
- [[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026]] — RU practitioner consensus
- [[evolving/content-trends/geo-when-not-worth-investing-2026]] — обратная сторона: когда стохастичность не даёт окупаемости
- [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]] — первоисточник тезиса (Pressfeed, май 2026)
