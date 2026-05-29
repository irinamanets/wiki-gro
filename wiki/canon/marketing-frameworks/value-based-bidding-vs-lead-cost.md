---
id: mkt:canon/marketing-frameworks/value-based-bidding-vs-lead-cost
title: "Value-based bidding vs CPL: передача офлайн-конверсий как сдвиг performance-метрики"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [performance-marketing, paid-ads, yandex-direct, smart-bidding, crm, attribution, ltv, framework]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-dzen-delovoymir-pervukhin-funnel-5-leaks.md]
namespace: mkt
---

# Value-based bidding vs CPL: сдвиг performance-метрики 2026

Устойчивый методологический сдвиг performance-маркетинга: оптимизация по **факту заявки (CPL)** уступает место оптимизации по **ценности конверсии, выручке, ROI и прибыли**. Достигается передачей офлайн-конверсий из CRM в рекламную систему. Сформулирован Артемом Первухиным (KINETICA) в [[sources/2026-05-26-dzen-delovoymir-pervukhin-funnel-5-leaks]] как Утечка #2 в [[canon/marketing-frameworks/pervukhin-funnel-5-leaks-diagnostic]].

## Главный тезис

> «Логика performance-маркетинга смещается от "дешёвый лид любой ценой" к прибыльности и LTV. Вопрос меняется: не "как получить заявку дешевле", а "какие заявки реально окупаются".» `[conf:medium, src:2026-05-26]`

## Почему CPL ломается как единственная метрика

CPL (cost per lead) — удобная, но **слепая** метрика:

- Фиксирует событие на сайте, но **не знает, чем закончилась сделка** `[conf:medium, src:2026-05-26]`.
- Канал с высоким числом лидов может генерировать **низкую выручку** — и наоборот.
- Для B2B, недвижимости, медицины и любых длинных воронок **разрыв между заявкой и оплатой — недели** `[conf:medium, src:2026-05-26]`.

Симптом: CPA держится, лиды идут — но «денег в компании не прибавляется». Это опаснее очевидного провала, потому что на поверхности всё нормально.

## Решение: value-based bidding

Алгоритмы Яндекс Директа давно умеют оптимизироваться по:
- **Ценности конверсии** (передаётся вес каждой конверсии);
- **Выручке** (передаётся сумма сделки);
- **ROI и прибыли** (передаётся профит-маржа).

Большинство рекламодателей по-прежнему передают только **факт заявки** — и теряют этот рычаг `[conf:medium, src:2026-05-26]`.

**Что нужно:**
1. **Сквозная аналитика** — Яндекс Метрика + CRM + коллтрекинг в связке.
2. **Передача офлайн-конверсий** в Директ из CRM: статусы сделок, суммы оплат, оплаты вне сайта.
3. **Смотреть на окупаемость через CRM**, а не только через счётчик.

## Особый случай — широкий ассортимент

Для интернет-магазинов с широким ассортиментом одинаковый CPO ломает экономику:
> Одинаковый CPO в 2 500 ₽ для расходника за 400 ₽ и техники за 400 000 ₽ — **это не одно и то же** `[conf:medium, src:2026-05-26]`.

Корректный подход:
- Для расходника: проверять, **берут ли его в комплекте** с более дорогими позициями (cross-sell-метрика).
- Для дорогой техники: проверять, **что произойдёт с выручкой, если поднять целевой CPA на 20–30%** (масштабирование).

**Кейс KINETICA.** Крупный казахстанский магазин техники: изменили подход к сегментации и пересмотрели список продвигаемых товаров. За месяц **ДРР снизился с 11% до 3%** при росте CPO на 67% — за счёт роста среднего чека и конверсии `[conf:medium, src:2026-05-26]`. Если бы фокус оставался на удержании CPO, масштабирования не случилось бы. Полный кейс: [[evolving-strict/campaign-metrics/kinetica-funnel-optimization-cases-2025]].

## Operational-протокол перехода с CPL на value-based

1. **Аудит инфраструктуры.** Есть ли CRM с фиксацией статусов сделок и сумм оплат? Связан ли коллтрекинг с CRM?
2. **Маппинг событий.** Какие события надо передавать: «заявка» → «квалифицированный лид» → «КП» → «оплата». Каждое — с весом или суммой.
3. **Интеграция.** Стандартная схема: CRM → API Яндекс Директа (Offline Conversion API). Для типовых CRM (Bitrix24, amoCRM) — готовые коннекторы.
4. **Период обучения.** Алгоритму нужен **минимум 10 событий «оплата» в неделю** (см. [[canon/marketing-frameworks/algorithm-training-conversion-action-selection]]). На длинном цикле — обучаться на промежуточном событии («квалифицированный лид»), коррелирующем с покупкой.
5. **Метрика успеха.** Не CPA, а **ROAS / ДРР / профит по кампании**. Динамика во времени, не точечный snapshot.

## Связь с pre-launch ROI Petrochenkov

Petrochenkov в [[canon/marketing-frameworks/cpa-calculator-pre-launch-roi]] даёт **формулу до запуска**:
> Выплата за лид = Маржа × CR (лид → покупка)

Pervukhin даёт **operational-цикл после запуска**: чтобы CR (лид → покупка) можно было считать в реальном времени и **отдавать алгоритму**, а не только использовать как pre-launch проверку.

Вместе формируют **полную рамку value-based performance 2026**:
1. До запуска: Petrochenkov pre-launch ROI → есть ли вообще unit-экономика.
2. На запуске: Pervukhin value-based bidding → передавать выручку/прибыль алгоритму, не CPL.
3. После запуска: Pervukhin 5-leaks → если value-based не работает, искать утечку по 5-leaks рамке.

## LTV-расширение для подписочных продуктов (как GRO)

Для subscription-моделей формула расширяется:
> Выплата за лид = (Маржа × CR покупки) + (LTV × CR retention) − Operational cost

Это та же логика, что в Petrochenkov LTV-extension и Front-End стратегии. Для GRO: ценность установки приложения **зависит от вероятности дойти до платной подписки** (D7/D14 retention → activation), а не от факта установки.

В Директ передаётся не «установка», а **«активация подписки»** или **«D14 retention»** — событие, которое **реально предсказывает LTV**.

## Anti-pattern: оптимизация по случайным микроконверсиям

> «Не использовать случайные микроконверсии — скролл или клик по баннеру сигналом не являются.» `[conf:medium, src:2026-05-26]`

Передача в Директ микроконверсий, **не коррелирующих с покупкой** (скроллы, hover'ы, добавление в избранное без покупки), → алгоритм оптимизируется под трафик, **который не покупает**. См. подробнее: [[canon/marketing-frameworks/algorithm-training-conversion-action-selection]].

## Применение

**Кому критично:**
- E-commerce с широким ассортиментом и разными ценовыми сегментами.
- B2B-услуги с длинным циклом сделки.
- Подписочные продукты с retention-кривой (GRO).
- Любому бизнесу, где CPA «держится», а выручка не растёт.

**С чем сочетается:**
- [[canon/marketing-frameworks/cpa-calculator-pre-launch-roi]] — pre-launch ROI рамка-предшественник.
- [[canon/marketing-frameworks/algorithm-training-conversion-action-selection]] — какой именно сигнал передавать алгоритму.
- [[canon/marketing-frameworks/sales-crm-minimum-fieldset]] — минимальный fieldset CRM для атрибуции.
- [[canon/marketing-frameworks/hot-lead-share-kpi-vtochku]] — доля горячих лидов как качественный KPI.

## Hooks для контента GRO

| Стадия | Hook | Сегмент |
|---|---|---|
| Awareness | «Большинство рекламодателей до сих пор оптимизируют Директ по факту заявки. И теряют десятки процентов выручки.» | Founders, маркетологи |
| Consideration | «Одинаковый CPO в 2500 ₽ для расходника за 400 ₽ и техники за 400 000 ₽ — это не одно и то же.» | E-commerce |
| Consideration | «"Дешёвый лид любой ценой" — мёртвая метрика 2026. Живая — какие заявки реально окупаются.» | Performance-маркетологи |
| Decision | «Передача офлайн-конверсий в Директ — самый быстрый способ масштабировать прибыльные сегменты и срезать убыточные.» | Заказчики performance |

## Связанные страницы

- [[canon/marketing-frameworks/pervukhin-funnel-5-leaks-diagnostic]] — родительский framework
- [[canon/marketing-frameworks/cpa-calculator-pre-launch-roi]] — pre-launch ROI рамка-предшественник
- [[canon/marketing-frameworks/algorithm-training-conversion-action-selection]] — выбор обучающего события
- [[canon/marketing-frameworks/niche-dynamics-vs-self-comparison-benchmark]] — корректный ориентир CPA
- [[canon/marketing-frameworks/sales-crm-minimum-fieldset]] — минимальный fieldset CRM
- [[canon/marketing-frameworks/hot-lead-share-kpi-vtochku]] — доля горячих лидов как KPI
- [[evolving-strict/campaign-metrics/kinetica-funnel-optimization-cases-2025]] — кейс KZ-техники
- [[sources/2026-05-26-dzen-delovoymir-pervukhin-funnel-5-leaks]] — первоисточник
