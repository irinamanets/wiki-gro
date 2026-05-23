---
id: mkt:canon/marketing-frameworks/habit-retention-diagnostics
title: "Habit-retention диагностики — частота, Time to habit, Habit moment, DAU/MAU"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [retention, habit, metrics, product-management, dau-mau, cohort-analysis, pmf]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-dzen-delovoymir-habit-product-hook-model.md]
namespace: mkt
---

# Habit-retention диагностики

Reusable набор метрик для ответа на вопрос **«формируется ли у пользователя привычка к продукту»**, который стандартный retention D1/D7/D30 не закрывает. Зафиксирован как canon-константа: это правила интерпретации, по которым мы смотрим на любые retention-данные (свои и конкурентов), а не текущие числа GRO (те — в [[evolving-strict/product-metrics/gro-store-installs]]).

Источник синтеза — [[sources/2026-05-19-dzen-delovoymir-habit-product-hook-model]] (Деловой мир / Дзен), `confidence: medium` по атрибуции; пороги пересекаются с общеиндустриальными бенчмарками (Lenny's Newsletter, Reforge, классическая статья Brian Balfour про DAU/MAU).

## Зачем нужны метрики глубже D1/D7/D30

Стандартный retention D1/D7/D30 показывает **факт** возврата, но не его **природу**. Он не отличает «пользователь вернулся, потому что мы его задолбали пушами и скидками» от «пользователь вернулся, потому что продукт стал привычкой». Чтобы понять, замыкается ли поведенческая петля (см. [[canon/marketing-frameworks/hook-model-habit-loop]]), нужно смотреть глубже.

## Четыре диагностики

### 1. Частота сессий

Сколько раз в неделю активный пользователь открывает продукт. **Если число растёт со временем когорты — петля работает.** Падает — привычка не сформировалась, retention держится на внешних стимулах.

### 2. Time to habit

Сколько дней с момента регистрации проходит до момента, когда пользователь начинает возвращаться **стабильно**. У сильных продуктов есть «магическое число» — порог, после которого вероятность удержания резко растёт.

- Канонический исторический пример: Facebook* — «**7 друзей за 10 дней**». `[conf:medium, src:2026-05-19]`

(*деятельность Meta признана экстремистской и запрещена в РФ)

Доводить новых пользователей до этой точки — отдельная продуктовая задача и зона активации. Связана с [[canon/marketing-frameworks/tabunov-onboarding-principles|онбордингом]] и [[canon/marketing-frameworks/fogg-behavior-model|снижением friction первого действия]].

### 3. Habit moment

Конкретное действие, которое **отличает привычного пользователя от случайного**: создание первого плейлиста, streak длиннее 7 дней, заполненный профиль. `[conf:medium, src:2026-05-19]`

> Найти своё habit moment и оптимизировать продукт под доведение до него — самая высокоокупаемая работа в retention.

Habit moment часто совпадает с элементом «инвестиция» из [[canon/marketing-frameworks/hook-model-habit-loop|Hook Model]] — действием, повышающим switching cost.

### 4. DAU/MAU — отношение дневной аудитории к месячной

«Stickiness» продукта — главный сводный индикатор привычности:

| DAU/MAU | Трактовка | Source |
|---|---|---|
| < 20% | Продукт используется эпизодически | `[conf:medium, src:2026-05-19]` |
| 20–50% | Промежуточная зона | `[conf:medium, src:2026-05-19]` |
| > 50% | Продукт стал частью ежедневной рутины | `[conf:medium, src:2026-05-19]` |

Ключевой динамический сигнал: **у habit-продуктов DAU/MAU растёт со временем когорты, а не падает.** `[conf:medium, src:2026-05-19]` Если падает — продукт держится на acquisition, не на привычке.

## Как это сочетается с другими retention-метриками

- [[canon/marketing-frameworks/retention-benchmarks-b2c]] — пороги «качества ведра» (Day-30 ≥20%, subscription retention ≥75%). Эти диагностики **дополняют** их: бенчмарки говорят «дырявое ли ведро», habit-метрики — «по какой причине пользователь возвращается».
- DAU/MAU > 50% и растущая частота сессий — это и есть «золотой продукт» Табунова, наблюдаемый с другого ракурса.

## Применение к GRO

GRO — daily-habit-продукт, поэтому именно эти метрики, а не только Day-30, должны быть в его retention-дашборде:

- **Частота сессий:** целевой паттерн — рост числа тренировок в неделю по мере взросления когорты.
- **Time to habit:** GRO нужно определить своё «магическое число» (например, «N тренировок за первые 7 дней» или «первый завершённый недельный план») и оптимизировать онбординг под доведение до него.
- **Habit moment:** кандидаты — первая завершённая тренировка, первый недельный streak, первый персональный план. Эти же действия — «инвестиция» в петле.
- **DAU/MAU:** для habit-продукта целевая зона > 50% (ежедневная рутина); < 20% означало бы, что GRO используется эпизодически, а не как привычка — что противоречит value proposition «расти каждый день» (см. [[canon/positioning/gro-value-proposition]]).

Текущие operational-числа GRO — в [[evolving-strict/product-metrics/gro-store-installs]]; эта страница — шаблон их интерпретации.

## Связанные страницы
- [[canon/marketing-frameworks/hook-model-habit-loop]]
- [[canon/marketing-frameworks/fogg-behavior-model]]
- [[canon/marketing-frameworks/retention-benchmarks-b2c]]
- [[canon/marketing-frameworks/tabunov-onboarding-principles]]
- [[evolving/industry-trends/whoop-retention-case-2026]]
- [[evolving-strict/product-metrics/gro-store-installs]]
- [[canon/product-knowledge/gro-app-overview]]
- [[canon/positioning/gro-value-proposition]]
- [[sources/2026-05-19-dzen-delovoymir-habit-product-hook-model]]
