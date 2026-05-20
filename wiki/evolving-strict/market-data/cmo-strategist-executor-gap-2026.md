---
id: mkt:evolving-strict/market-data/cmo-strategist-executor-gap-2026
title: "CMO 2026: разрыв ожиданий стратег vs исполнитель (84% / 64%)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [cmo, marketing-leadership, hr, organizational-design, b2b, research-data]
confidence: low
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-pressfeed-prdoctor-marketing-pr-sales-conflict.md]
namespace: mkt
---

# CMO 2026: разрыв ожиданий стратег vs исполнитель

**Тезис.** Существует **системный разрыв** между тем, что работодатели говорят, что ждут от директора по маркетингу (CMO), и тем, как они его на самом деле нанимают и оценивают. Конфликт желания и исполнения создаёт хрестоматийную ситуацию: бизнес на словах хочет стратега, отвечающего за деньги и рост, но нанимает и оценивает его как тактика-исполнителя.

## Ключевые цифры

- 84% работодателей ждут от CMO **роста выручки или прибыли** `[conf:low, src:2026-05-18]`
- 64% директоров по маркетингу уверены, что работодатели **ищут не стратегов**, а «маркетологов с руками», которые будут напрямую приводить клиентов `[conf:low, src:2026-05-18]`

**Разрыв 84/64** — численная иллюстрация **системного несовпадения**: работодатели **просят** стратегического результата, но **нанимают и оценивают** по тактическим метрикам.

## Атрибуция и confidence

**Источник:** статья PR DOCTOR на Pressfeed ([[sources/2026-05-19-pressfeed-prdoctor-marketing-pr-sales-conflict]]) `[conf:low, src:2026-05-18]`.

**Первоисточник самого исследования в статье не назван** — формулировка автора: «недавно опубликованное исследование, проведённое среди директоров по маркетингу». **Confidence: low** именно из-за невозможности атрибутировать первоисточник:

- Не указаны: издание, методология, выборка, география, период
- Не указано, опрашивали ли только CMO или и работодателей (для второй цифры нужны обе стороны)
- Не указано, RU-data или глобальный mix

**Action:** при использовании этих цифр в content/SEO — **обязательно** указывать «по данным, цитируемым PR DOCTOR в Pressfeed, 2026-05» и **не использовать как первичный источник для quantitative claims**. Уровень — illustrative, не bookable.

## Почему gap существует (интерпретация PR DOCTOR)

Параллельно с PR/маркетинг/sales-конфликтом (см. [[canon/marketing-frameworks/three-dept-conflict-prdoctor]]) у CMO своя версия того же дисфункционального паттерна:

- **Объявленная роль:** стратег, отвечающий за рост выручки → требует системного мышления, межфункциональной координации, long-term horizon
- **Реальные KPI и ожидания:** «приведи мне 100 квалифицированных лидов в этом месяце» → тактика, короткий горизонт
- **Следствие:** CMO либо уходит в тактику и теряет стратегическую функцию, либо упирается в недовольство работодателя «где результат на выручке?»

Это **изоморфно** причине-3 («неправильная KPI-структура») из 3-dept рамки, только применено к одному человеку, а не к отделам.

## Связь с другими сигналами в вики

### Параллельные данные о маркетинг-лидерах
- [[canon-strict/historical-campaigns/tbank-tinvest-tolk-pro-2026-04|TINKOFF/Т-Инвестиции]] и другие brand-кампании — кейсы где CMO играет стратегическую роль (имея autonomy и стратегический KPI)
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]] — расширение skill-set CMO в сторону AI-native, что **усиливает** требование стратегии

### Operational consequences
- [[canon/marketing-frameworks/marketing-sales-alignment-framework]] — Shared KPIs как технический фикс для CMO-сегмента gap (если работодатель и CMO оба измеряют выручку → tactic-strategy gap снимается)
- [[canon/marketing-frameworks/three-dept-conflict-prdoctor]] — переход к Revenue KPIs снимает CMO-парадокс на системном уровне
- [[canon/marketing-frameworks/brand-manager-core-competencies]] — что должен уметь сильный маркетинг-лидер (баланс стратегии и тактики)

### Adjacent — HR/recruiting сигналы
- [[evolving/industry-trends/ru-hr-tech-ai-landscape-2026]] — состояние RU HR-tech рынка, в котором происходит наём CMO
- [[evolving-strict/market-data/ru-it-labor-market-salaries-2026|RU IT labor market]] — для бенчмарков по компенсациям marketing-leadership

## Что делать с этим сигналом

**Для GRO:**
- При найме маркетинг-лидера — **на старте письменно зафиксировать** Revenue KPI (выручка, retention, LTV, MRR-рост) **до** обсуждения tactic-задач. Это снимает gap **превентивно** (см. [[canon/marketing-frameworks/gtm-shared-understanding-anchor|GTM anchor]] как родственный pattern для продукта).
- Не нанимать «стратега» без бюджета и autonomy на стратегию — лучше нанять senior performance-маркетолога с понятной tactic-зоной.

**Для content/SEO:**
- Цифры использовать **с атрибуцией и caveat**: «по данным, цитируемым PR DOCTOR в Pressfeed»
- **Не использовать** в high-stakes-публикациях без верификации первоисточника
- Можно использовать как hook для статей про **CMO compensation structure**, **marketing organization design**, **revenue accountability**

## TTL и re-verification

`evolving-strict/market-data` → 180 дней soft re-verify.

**Action 2026-11-19:**
- Найти первоисточник исследования (поиск по терминам про CMO-survey c фокусом на разрыв revenue-expectations vs tactic-execution; «директора по маркетингу исследование стратеги исполнители»)
- Если нашёлся → обновить `confidence` (medium/high) и заменить src на оригинал
- Если не нашёлся через 6 месяцев → пометить `stale: true` и перенести в `volatile-strict` либо удалить с пометкой «не подтверждено»

## Anti-patterns при использовании этих цифр

- ❌ **Цитировать как «исследование показало»** без оговорки про невыявленный первоисточник
- ❌ **Делать high-stakes-выводы** (стратегические решения, презентации инвесторам) на основе single-source unverified data
- ❌ **Игнорировать gap-сигнал** только потому что primary-source не подтверждён — pattern существует, изоморфен другим параллельным данным в вики (см. 3-dept рамку)

## Связанные страницы

- [[canon/marketing-frameworks/three-dept-conflict-prdoctor]]
- [[canon/marketing-frameworks/marketing-sales-alignment-framework]]
- [[canon/marketing-frameworks/brand-manager-core-competencies]]
- [[canon/marketing-frameworks/gtm-shared-understanding-anchor]]
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]]
- [[evolving/industry-trends/ru-hr-tech-ai-landscape-2026]]
- [[sources/2026-05-19-pressfeed-prdoctor-marketing-pr-sales-conflict]]
