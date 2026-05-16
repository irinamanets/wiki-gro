---
id: mkt:canon/marketing-frameworks/business-metrics-for-owners
title: "Ключевые бизнес-метрики для владельцев: воронка и маркетинг"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [content, retention, decision]
confidence: medium
stale: false
created: 2026-04-16
updated: 2026-05-06  # +applied case: ДДС vs АПУ vs амортизация на примере rental-бизнеса Муратаева (выпуск #4 велобайк-серии); founder-explainer как content-pattern для воспитания founder-аудитории
sources: [sources/2026-04-16-condense-pressfeed-35-articles.md, sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc.md]
namespace: mkt
---

# Ключевые бизнес-метрики для владельцев: воронка и маркетинг

Минимальный набор метрик, которые владелец бизнеса должен контролировать -- от маржинальности до LTV. Подходит как контент-рамка для GRO Сегмента 2 (предприниматели).

## Воронка владельца

Приоритет сверху вниз:
1. **Маржинальность** -- сколько остаётся после переменных расходов
2. **Рентабельность** -- сколько остаётся после всех расходов
3. **Постоянные / переменные расходы** -- понимание структуры затрат
4. **Точка безубыточности** -- минимум выручки для нуля

## Маркетинговые метрики для контроля

- **CPL** (Cost Per Lead) -- стоимость лида
- **CAC** (Customer Acquisition Cost) -- стоимость клиента
- **ROMI** (Return on Marketing Investment) -- окупаемость маркетинга
- **LTV** (Lifetime Value) -- пожизненная ценность клиента

По мнению маркетолога Михаила Ветренко: «Увеличив LTV всего на 10-20%, можно удвоить прибыль без увеличения бюджета на привлечение.»

## Связь с GRO

GRO как подписочный продукт -- метрики LTV и retention критичны. Владельцы из Сегмента 2 оперируют именно этими понятиями -- контент GRO может использовать эту рамку для образовательных постов.

## Applied case: ДДС vs АПУ vs амортизация (rental-бизнес, выпуск #4 Муратаева 2026-05-05)

Из источника [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]] — applied illustration trio метрик в живом SMB-кейсе:

### ДДС (Движение Денежных Средств) — что Муратаев показывает в кадре

| Категория | Сумма (март 2026) |
|---|---|
| Поступления | ~1 198 000 ₽ (rental + ремонт + продажи + возврат залога) |
| Выплаты | 781 000 ₽ (ФОТ + оборудование + аренда + маркетинг + расходники) |
| **ЧДП** (чистый денежный поток) | **417 000 ₽** |
| Остаток на конец периода | 765 000 ₽ |

ДДС = **только cash in/out, без bookkeeping concepts**. Это **первый отчёт**, который владелец SMB реально может построить в Excel. Founder-friendly. Но **не показывает прибыль** — потому что игнорирует амортизацию.

### АПУ (Альтернативный отчёт о Прибылях и Убытках) — что Муратаев откладывает на следующий выпуск

> «Для меня лично интереснее больше АПУшка, но АПУшка будет в следующей серии.» — Муратаев

АПУ = **profit-and-loss** с учётом всех **non-cash adjustments**:
- Амортизация активов
- Кредиторская задолженность (что должны мы)
- Дебиторская задолженность (что должны нам)
- Обороты vs payments timing

Различие критично: **ЧДП может быть положительным** (cash flowing), **а АПУ при этом может быть отрицательным** (бизнес фактически убыточен, потому что активы изнашиваются быстрее).

### Амортизация — связующий концепт

Муратаев в эпизоде #4 объясняет:

> «Мы исходим из того, что байк проживёт у нас полтора года, и делим сумму закупки на эти восемнадцать месяцев, и получаем, что у нас амортизация 3,5% в месяц.»

При парке 47 байков × 75 000 ₽ × 3,5% = **~123 000 ₽/мес «бумажной» амортизации**, не отображаемой в ДДС. Это **−30% от ЧДП 417 000 ₽** → реальная прибыль ~294 000 ₽/мес → break-even 16-17 мес вместо 10.

**Operational rule для founder'а**: при subscription / rental-бизнесах **always считать амортизацию отдельно от cash-flow** — иначе неправильный break-even, неправильный horizon investment.

### Founder-explainer как content-pattern

Что Муратаев делает в кадре — это **публично-педагогический момент** для founder-аудитории, которая часто **путает ДДС и прибыль**. Это reusable content-template для GRO:

1. Показать конкретные numbers (как Муратаев — ДДС March)
2. Признать caveat (как Муратаев — «АПУ в следующей серии»)
3. Ввести разъяснение non-cash-конструкции (амортизация)
4. Показать impact на break-even

Это **founder-content для founder-audience**, который **повышает trust** через demonstrated finance-numeracy.

## Связанные страницы
- [[canon/marketing-frameworks/cpa-calculator-pre-launch-roi]] -- калькулятор ROI
- [[canon/marketing-frameworks/retention-benchmarks-b2c]] -- retention-бенчмарки
- [[canon/target-audience/gro-segments]] -- сегменты ЦА (Сегмент 2)
- [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]] — applied case ДДС/АПУ/амортизация
- [[evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026]] — конкретные numbers из applied case
- [[canon/marketing-frameworks/breakage-business-model-fitness]] — соседняя metric-rich модель (renewal % как key health indicator)
- [[canon/marketing-frameworks/b2b-pivot-anchor-customer-smb]] — pattern, влияющий на recurring-revenue структуру метрик

## Backlinks

_11 pages link to this one._

- [[canon/marketing-frameworks/b2b-pivot-anchor-customer-smb]]
- [[canon/marketing-frameworks/breakage-business-model-fitness]]
- [[canon/marketing-frameworks/kpmg-5-stage-restructuring]]
- [[canon/marketing-frameworks/plant-to-company-transition]]
- [[canon/marketing-frameworks/portnyagin-7-decision-questions]]
- [[canon/marketing-frameworks/sales-crm-minimum-fieldset]]
- [[canon/marketing-frameworks/seissembai-algorithm-ratchet-vicious-circle]]
- [[canon/marketing-frameworks/trainer-rental-marketplace-model]]
- [[evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026]]
- [[index]]
- [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]]
