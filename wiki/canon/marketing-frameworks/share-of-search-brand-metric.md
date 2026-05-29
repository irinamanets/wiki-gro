---
id: mkt:canon/marketing-frameworks/share-of-search-brand-metric
title: "Share of Search — опережающий индикатор бренда (через Wordstat / Google Trends)"
type: page
subtype: metric
layer: canon
theme: marketing-frameworks
tags: [framework, metric, brand-marketing, kpi, share-of-search, leading-indicator, wordstat, google-trends, cmo, cfo-language]
confidence: medium
stale: false
created: 2026-05-27
updated: 2026-05-27
sources: [sources/2026-05-27-dzen-delovoymir-pervukhin-brand-vs-performance.md]
namespace: mkt
---

# Share of Search — опережающий индикатор бренда

**Share of Search (SoS)** — доля брендовых поисковых запросов компании относительно конкурентов в категории. Используется как **опережающий индикатор**: рост Share of Search **предшествует росту выручки примерно на 2–3 месяца** `[conf:medium, src:2026-05-27]`. Канонизация: Артем Первухин, продакшен-директор KINETICA, статья на Деловом мире / Дзен ([[sources/2026-05-27-dzen-delovoymir-pervukhin-brand-vs-performance]]).

Метрика — основной KPI **инвестиционного трека** в [[canon/marketing-frameworks/brand-vs-performance-two-track-strategy-pervukhin|two-track стратегии]] и встаёт рядом с [[canon/marketing-frameworks/brand-lift-measurement-by-platform]] как пара «количественный + качественный» брендовых KPI.

## Определение

> «Доля брендовых поисковых запросов компании относительно конкурентов в категории. Отслеживается через Wordstat и Google Trends в динамике, еженедельно.» `[conf:medium, src:2026-05-27]`

**Формула (concept):**
```
SoS = (запросы по моему бренду + категория) / (Σ запросов по всем брендам категории)
```

Период замера — **еженедельно**. Не разовый замер, а **динамика**.

## Ключевые свойства

> «Это опережающий индикатор: рост Share of Search предшествует росту выручки примерно на 2–3 месяца. Ключевое свойство — его невозможно накрутить внутри рекламного кабинета.» `[conf:medium, src:2026-05-27]`

3 свойства, делающих SoS уникальным KPI:

1. **Опережающий** — реагирует за 2–3 месяца до изменения выручки `[conf:medium, src:2026-05-27]`. Это позволяет **раньше реагировать**: оптимизировать охватную кампанию по сигналу SoS, не дожидаясь подтверждения через продажи.
2. **Невозможно накрутить из рекламного кабинета** — это **внешний рыночный замер** (Wordstat — данные поисковых систем). В отличие от показов/охватов внутри Директа/myTarget, которые формально «закрашены» бюджетом, SoS отражает реальный спрос.
3. **Сравнительный** — относительная метрика к конкурентам, а не абсолютная. Это автоматически нормализует на сезонность и общий рост категории.

## Инструменты замера

| Источник | Что даёт | Ограничения |
|---|---|---|
| **Wordstat (Яндекс)** | Месячная история запросов по любым ключевым словам, регионам, устройствам. Бесплатно. | Гранулярность месяц; для еженедельной динамики — собственный сбор/парсинг. |
| **Google Trends** | Относительная динамика (0–100) по запросам, регионам, периодам. Бесплатно. | Не абсолютные числа; нужны бренды для сравнения; шум на низкочастотных запросах. |
| **Платные SEO-tools** (Keys.so, Bukvarix, Serpstat и т.д.) | Точнее, можно делать конкурентные срезы. | Платно; точность зависит от sample. |

**Минимальный setup (free)**: Wordstat + Google Trends + еженедельный ручной (или скриптом) snapshot конкурентов в Google Sheets.

## Как считать «бренд в категории»

Для корректного SoS нужен **bounded list конкурентов**. Например:
- **Категория «фитнес-приложения»:** GRO + FitOn + Sweat + Nike Training Club + Fitstars + СилаVoli + ...
- **SoS GRO =** (запросы «ГРО» + «GROapp» + «гро приложение» + ...) / (Σ запросов по всем брендам категории).

**Anti-pattern:** считать SoS «в вакууме» (только свои запросы без знаменателя) — это не Share of Search, это **brand search volume**, который мало отличается от обычного organic-трафика по бренду.

## Соответствие инвестиционному треку

SoS — главная **leading metric** инвестиционного трека [[canon/marketing-frameworks/brand-vs-performance-two-track-strategy-pervukhin|two-track стратегии]]:

| Этап после старта охватной кампании | Что должен показывать SoS |
|---|---|
| Неделя 1–3 | Без значимых изменений (шум) |
| **Неделя 4–6** | **Начинает реагировать** — первый измеримый сигнал `[conf:medium, src:2026-05-27]` (см. [[evolving-strict/campaign-metrics/brand-investment-timeline-benchmarks]]) |
| Месяц 2–3 | Виден устойчивый рост SoS у компании при стабильных значениях у конкурентов |
| Месяц 4–6 | Подтверждение через рост выручки (с lag 2–3 мес) |

> «Share of search растёт вместе с охватами — конкуренты остаются на месте.» `[conf:medium, src:2026-05-27]`

Это **диагностический сигнал**: если охватная кампания идёт 6 недель, а SoS не двинулся — креатив/канал/сегмент не работают, нужна спринтовая корректировка (см. [[canon/marketing-frameworks/brand-sprint-testing-quarterly-three-iterations]]).

## Anti-patterns

1. **Абсолютные числа без bounded list конкурентов** — это brand search volume, не SoS.
2. **Месячный замер вместо еженедельного** — теряется leading-индикаторная функция (lag в 4 недели = вся ценность опережения сожжена).
3. **Игнорирование сезонности** — частично нормализуется через сравнительный знаменатель, но в категориях с очень разной сезонностью (например, ёлки) сравнение не работает.
4. **Использование как стандалон-метрики** — SoS работает в системе с [[canon/marketing-frameworks/brand-lift-measurement-by-platform|Brand Lift]] и [[canon/marketing-frameworks/assisted-conversions-attribution-3-models|ассоциированными конверсиями]]. По отдельности теряет 50%+ ценности.
5. **Реакция CFO «верю/не верю»** — нужно с самого старта объяснить методологию и горизонт (4–6 недель до первого сигнала), иначе после двух «пустых» недель SoS будет признан «не работающим».

## Применение к GRO

GRO как B2C subscription с **формирующимся брендом** в категории «фитнес-приложения/программа тренировок». Operational-протокол:

### 1. Baseline (T0)
- Bounded list: GRO + FitOn + Sweat + Fitstars + Силаvoli + Nike Training Club + 3–5 RU-конкурентов.
- Query-список: «гро», «groapp», «ГРО приложение», «ГРО фитнес», «ГРО тренировки» (и аналоги у конкурентов).
- Замер через Wordstat месячный + Google Trends weekly за последние 12 месяцев.

### 2. Регулярный замер
- **Еженедельный snapshot** в Google Sheets/Notion.
- **Месячный визуал** (line chart SoS GRO vs топ-3 конкурента).
- Метрика встаёт в investment-dashboard CMO.

### 3. Использование при защите бюджета
- В operational-отчёте: CPA installs, retention D7/D14/D30, активация подписки.
- В **investment-отчёте** (новый!): **SoS GRO X% → Y%** за период; динамика CPC по бренду в Яндексе; ассоциированные конверсии охватных каналов в перформанс.

### 4. Триггеры действий
- Падение SoS 2 недели подряд без роста конкурентов → срочный аудит охватных каналов.
- Рост SoS при росте CPI install → охват разогрел нерелевантную аудиторию, нужна корректировка таргетинга.
- Рост SoS + снижение CPC по бренду → охватная инвестиция работает, можно масштабировать.

## Hooks для контента GRO/маркетологов

| Стадия | Hook | Сегмент |
|---|---|---|
| Awareness | «Share of Search опережает выручку на 2–3 месяца. Единственная брендовая метрика, которую невозможно накрутить из рекламного кабинета.» `[conf:medium, src:2026-05-27]` | Маркетологи, founders |
| Awareness | «Бренд можно измерить. Если ваш Share of Search не растёт — конкурент выкупает спрос, который должен был быть вашим.» | CMO, маркетинг-директора |
| Consideration | «3 простых инструмента для замера SoS: Wordstat (бесплатно), Google Trends (бесплатно), Google Sheets (бесплатно). Никакой "сложной аналитики" не нужно.» | Маркетологи, SMB |
| Decision | «Перед защитой бренд-бюджета подготовьте динамику Share of Search за 6 месяцев. Это перевод разговора с "верьте нам" на "смотрите на данные".» | CMO, B2B |

## Связанные страницы

- [[canon/marketing-frameworks/brand-vs-performance-two-track-strategy-pervukhin]] — родительская two-track стратегия (SoS — её главный investment-KPI)
- [[canon/marketing-frameworks/brand-lift-measurement-by-platform]] — парная метрика (количественный SoS + качественный Brand Lift)
- [[canon/marketing-frameworks/assisted-conversions-attribution-3-models]] — третья метрика бренда (мост к перформансу через атрибуцию)
- [[canon/marketing-frameworks/brand-sprint-testing-quarterly-three-iterations]] — спринтовая модель тестирования с SoS как чек-поинтом
- [[evolving-strict/campaign-metrics/brand-investment-timeline-benchmarks]] — 4–6 недель до первого сигнала SoS
- [[canon/marketing-frameworks/pervukhin-funnel-5-leaks-diagnostic]] — Утечка #1 (ориентир не тот) — SoS даёт корректный ориентир «динамика ниши»
- [[canon/marketing-frameworks/niche-dynamics-vs-self-comparison-benchmark]] — сравнение CPA с динамикой ниши, smежная methodology
- [[sources/2026-05-27-dzen-delovoymir-pervukhin-brand-vs-performance]] — первоисточник
