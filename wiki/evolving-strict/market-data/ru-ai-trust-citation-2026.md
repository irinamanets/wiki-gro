---
id: mkt:evolving-strict/market-data/ru-ai-trust-citation-2026
title: "RU-доверие к AI-поиску + AI-ответы без ссылок: 28% / 87% (Pressfeed, май 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ai-search, llm-citation, trust, user-behavior, ru-market, source-attribution, brand-risk, information-laundering]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-18-pressfeed-geo-illusion-stability-measure.md]
namespace: mkt
---

# Trust к AI-поиску и отсутствие ссылок — RU-сигнал 2026

## TL;DR

В Pressfeed мая 2026 (отраслевые опросы) зафиксированы две **пересекающиеся метрики**, описывающие risk-сигнал AI-поиска для брендов в РФ:

- **28% россиян доверяют тому, что говорит ИИ в поиске** `[conf:medium, src:2026-05-18]`
- **В 87% AI-ответов, где была бы уместна ссылка, она отсутствует** `[conf:medium, src:2026-05-18]`

Это создаёт **«legally-permitted information laundering»**: ~1 из 3 потенциальных клиентов в RU воспримет AI-ответ как факт, при этом 87% таких ответов **не позволят верифицировать источник**. `[conf:medium, src:2026-05-18]`

## Метрики

### 1. Доверие RU-аудитории ИИ-поиску

| Метрика | Значение | Период | Источник | Confidence | Marker |
|---|---|---|---|---|---|
| Доля россиян, доверяющих информации от ИИ в поиске | **28%** | 2026 (по отраслевым опросам, цитируемым Pressfeed) | [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]] | medium | `[conf:medium, src:2026-05-18]` |

**Интерпретация:** ~1 из 3 потенциальных клиентов в RU **примет AI-ответ как факт** без верификации. Это **достаточно высокий уровень**, чтобы AI-выдача стала **first-touchpoint** для большой части воронки. Сравнение с глобальными метриками не приведено в источнике; нужен cross-check с RU-замерами типа ВЦИОМ / Mediascope.

### 2. AI-ответы без ссылок

| Метрика | Значение | Период | Источник | Confidence | Marker |
|---|---|---|---|---|---|
| Доля AI-ответов, где уместна ссылка, но её нет | **87%** | 2026 (по отраслевым опросам, цитируемым Pressfeed) | [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]] | medium | `[conf:medium, src:2026-05-18]` |

**Интерпретация:** **9 из 10** AI-ответов в RU-выдаче, которые **должны** были бы дать ссылку на источник, её **не дают**. Пользователь видит готовый ответ **без оговорок**, без возможности верифицировать. Это **системная уязвимость LLM**: модели достраивают картину там, где данных не хватает, делают это уверенно, и пользователь не понимает, что ответ может быть фабрикован/неточен.

## Confidence обоснование

`confidence: medium` — единичный источник (Pressfeed). Указаны как «отраслевые опросы» без названия исследовательского агентства / выборки / методологии. Перед использованием в маркетинговых материалах GRO:

1. Найти первичный источник опроса (возможно — Mediascope, ВЦИОМ, NAFI, OWI)
2. Сравнить с замерами доверия к AI в US (Pew Research, Edelman Trust Barometer)
3. Если в течение 3 месяцев не появится подтверждение из независимого источника → понизить до `confidence: low`

## Combined Risk Surface

Сочетание 28% × 87% создаёт **измеримый бизнес-риск** для брендов: `[conf:medium, src:2026-05-18]`

| Риск | Механизм | Вероятность | Impact |
|---|---|---|---|
| AI называет цену ниже реальной | Модель цитирует устаревшие данные | Высокая | Клиенты с другим бюджетом, потеря выручки |
| AI описывает B2B-продукт как бюджетный | Mismatch ценовой категории | Средняя | Отсев целевых клиентов |
| AI путает компанию с другой (похожее название) | Entity disambiguation failure | Низкая, но критичная | Претензии за чужие ошибки, репутационный ущерб |
| Information primacy theft (см. ниже) | LLM цитирует pre-trained text без source | Высокая | Конкуренты «съедают» оригинальное authorship |

## Information laundering: legal × technical × behavioral

Системный provo:

1. **Legal layer** — [[volatile-strict/industry-news/ru-ai-law-march-2026|закон РФ март 2026]] делает training на опубликованных текстах без согласия **допустимым** (если пользователь не видит исходника).
2. **Technical layer** — 87% AI-ответов без ссылок = технически **исключено** атрибутирование источника пользователю. `[conf:medium, src:2026-05-18]`
3. **Behavioral layer** — 28% RU-аудитории доверяет AI-ответам = **критическая масса** пользователей, принимающих unverified information как факт. `[conf:medium, src:2026-05-18]`

**Combined:** **legal-permitted, technically-invisible, behaviorally-trusted** dissemination информации без credit оригинальному автору. Это **legal information laundering** — статус-кво, не bug.

**Что это значит для бренда:**

- Оригинальный авторский контент монетизирован конкурентами (через ту же информацию, рекомендованную AI к их домену), без юридической защиты, без видимости пользователю
- Маркетинговые claims о брендах **не контролируются** брендами: AI может транслировать любые tier/price/positioning-signals без verification
- Brand-monitoring в AI-выдаче (см. [[canon/marketing-frameworks/geo-monitoring-discipline-2026]]) — **операционная необходимость**, не оптимизация

## Импликации для GRO

### Operational

1. **GEO-monitoring обязателен** — нужно **знать**, что AI говорит о GRO (правильная цена / правильная категория / правильный JTBD). См. [[canon/marketing-frameworks/geo-monitoring-discipline-2026]].
2. **Citation quality check** — отдельная subметрика в GEO-monitoring: цитирует ли AI GRO **корректно** (методология «4 шага», правильная подписка 2 490 ₽/мес, правильная категория «тренировка предпринимательского мышления») или **неверно** (старая цена / не та категория / другой бренд). `[conf:medium, src:2026-05-18]`
3. **Brand entity disambiguation** — есть ли в категории конкурент с похожим названием? Если да — **расширенная Schema** + явные differentiation-signals на сайте, чтобы AI не путал.

### Content-стратегия

1. **Использовать 28% trust как hook** для маркетинговых материалов: «1 из 3 ваших клиентов уже принимает решения через AI — что они слышат о вас?» `[conf:medium, src:2026-05-18]`
2. **Использовать 87% no-citation как provocation**: «Когда AI рекомендует GRO, вы видите это? Никто не видит — без GEO-monitoring вы слепы.» `[conf:medium, src:2026-05-18]`
3. **Не использовать confidence: low** signals в материалах без проверки — `confidence: medium` пока ограничивает.

## Сравнение с глобальным trend'ом

Метрики **не нормированы** между странами; нужны независимые замеры. Дополнительные RU-сигналы:

- Brand Analytics: **-33-38% органического трафика RU за 2025** ([[evolving/industry-trends/ai-search-aeo-geo-2026]]) — корреляция со sдвигом к AI-поиску `[conf:medium, src:2026-05-18]`
- 13 RU-практиков (Pressfeed май 2026): 30-40% падения за 2025 ([[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026]]) `[conf:medium, src:2026-05-18]`
- DiaClass: **10% трафика из ChatGPT/Perplexity** ([[evolving-strict/market-data/ru-ai-search-traffic-share-2026]]) `[conf:medium, src:2026-05-18]`

Все три сигнала складываются: **RU-аудитория уже частично в AI-выдаче, доверяет ей, но не видит ссылок** — это **зрелый рынок** для GEO-инвестиций (а не «emerging»).

## Re-verify

`evolving-strict` → re-verify **каждые 6 месяцев**:
- Q4 2026 / Q1 2027: новые отраслевые опросы trust-метрик
- Особое внимание: если 28% растёт быстро (50%+), GEO становится **must-have**, не optional `[conf:medium, src:2026-05-18]`
- Если 87% no-citation падает (как платформы добавляют source-attribution фичи), risk landscape меняется `[conf:medium, src:2026-05-18]`

## Связанные страницы

- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — родительский тренд (decision-layer, RU specifics)
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — operational playbook
- [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] — почему trust+87% делают monitoring обязательным `[conf:medium, src:2026-05-18]`
- [[canon/marketing-frameworks/stochastic-llm-ranking-sparktoro]] — почему даже корректная цитата нестабильна
- [[canon/marketing-frameworks/geo-platform-segmentation-yandex-chatgpt-perplexity]] — где этот risk применим (RU-платформы)
- [[volatile-strict/industry-news/ru-ai-law-march-2026]] — legal layer (закон не защищает от пересказа)
- [[evolving-strict/market-data/ru-ai-search-traffic-share-2026]] — связанные RU-метрики AI-трафика
- [[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026]] — RU practitioner consensus, который подтверждает зрелость рынка
- [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]] — первоисточник метрик
