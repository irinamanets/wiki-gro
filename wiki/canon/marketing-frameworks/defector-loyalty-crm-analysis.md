---
id: mkt:canon/marketing-frameworks/defector-loyalty-crm-analysis
title: "Defector + Loyalty Analysis: CRM-фреймворк управления текучестью"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [retention, churn, crm, customer-research]
confidence: low
stale: false
created: 2026-05-05
updated: 2026-05-05
sources:
  - sources/2026-05-05-e-xecutive-ru-condensed.md
  - sources/2026-05-05-exec-mobilnaya-svyaz-crm.md
namespace: mkt
---

# Defector + Loyalty Analysis: CRM-фреймворк управления текучестью

Парный CRM-фреймворк управления оттоком (churn): **Defector Analysis** работает с уходящими клиентами и выявляет реальные причины ухода (а не первый озвученный «цена»), **Loyalty Analysis** работает с остающимися и выявляет реальные удерживающие факторы. Использование без пары даёт перекошенную картину.

## Базовая формула

> **Ценность = полезность / цена**

Если полезность падает при стабильной цене → ценность падает в восприятии клиента → клиент уходит, обосновывая это «ценой». Снижение цены при той же низкой полезности проблему не решает: ценность остаётся низкой (числитель и знаменатель падают вместе).

## Defector Analysis (анализ ушедших)

**Метод:** серия итеративных вопросов «почему?» к ушедшему клиенту. После 3-5 итераций «цена» уходит, проявляются реальные факторы:

```
«Почему ушли?» → «Дорого»
«Почему стало дорого?» → «Стало дороже чем у конкурента»
«Почему перешли к конкуренту?» → «У них качество сети лучше»
«В чём именно лучше?» → «У меня перестали обрываться разговоры в офисе»
       ↓
   реальная причина = качество в конкретной геолокации
```

**Что даёт:** список реальных driver'ов оттока, ранжированный по частоте упоминаний. Используется для приоритизации продуктовых и сервисных улучшений.

**Anti-pattern:** принимать «цена» за реальный фактор и снижать цену. Это лечит симптом, не причину. Расходы растут, отток продолжается.

## Loyalty Analysis (анализ остающихся)

**Метод:** интервью с лояльными клиентами (>2 лет, NPS ≥ 8) о том, **почему они продолжают покупать** и какие у нас сильные стороны с их точки зрения.

**Что даёт:**
- Список удерживающих факторов (фичи, сервис, личные отношения с менеджером, привычки)
- Понимание чем мы реально отличаемся (по версии клиента, не маркетолога)
- Hooks для мессаджинга при привлечении похожих клиентов

**Зачем дополняет Defector Analysis:**
- Defector показывает что нас выдаёт (negative signals)
- Loyalty показывает что нас удерживает (positive signals)
- Только их пересечение даёт полную картину value proposition

## Microniche marketing как развитие

После Defector + Loyalty часто всплывают микросегменты с уникальными причинами оставаться/уходить. Под них можно делать **специальные сервис-пакеты** (см. [[canon/marketing-frameworks/microniche-marketing-packages]]).

## Иллюстративные кейсы (historic, conf:low)

- **Cellnet × BarclayCard** — телефоны клиентам банка с возможностью просмотра банковских счетов и электронных платежей. Отток в этом сегменте стал 5% против 20% средних по индустрии мобильной связи Великобритании (historic исторические цифры, иллюстрируют механику пакета под микросегмент)
- **British Airways NY-London** — вместо снижения цен ввели лежачие места, ванные, свежие газеты, завтрак, пижамы → выросла прибыль на маршруте на 25%. Иллюстрирует «увеличение полезности» при стабильной цене → рост ценности → снижение оттока

## Применимость к GRO

- При первом всплеске churn — НЕ принимать «цена» за причину. Запускать defector-интервью.
- Минимально жизнеспособный defector pipeline: 5-минутный exit-interview через бот при отмене подписки + квартальные глубинные с 5-10 ушедшими (когортой).
- Минимально жизнеспособный loyalty pipeline: ежеквартальные интервью с 5-10 лояльными (NPS ≥ 8, >2 цикла) — те же вопросы про jobs-to-be-done.
- Из обоих — input в roadmap и в content marketing (loyalty findings = социальное доказательство, defector findings = снимаются страхи у новых клиентов).

## Связанные страницы

- [[canon/marketing-frameworks/value-for-customer-concept]] — определение ценности, на котором построена формула полезность/цена
- [[canon/marketing-frameworks/microniche-marketing-packages]] — как развивать defector findings в продуктовые пакеты
- [[canon/marketing-frameworks/refused-customer-interview]] — техника интервью с отказавшимся / ушедшим клиентом
- [[canon/marketing-frameworks/retention-benchmarks-b2c]] — actionable retention бенчмарки (свежие, не historic)
- [[canon/marketing-frameworks/nps-three-tier-customer-and-employee]] — лёгкая NPS-петля как entry-point: критики (0–5) = defector-сигналы для итеративного «почему», промоутеры (9–10) = loyalty-сигналы (упрощённая версия пары defector/loyalty)

## Caveat

Фреймворк timeless и применяется в современном CRM/CX. Иллюстративные цифры (Cellnet 5%/20%, BA +25%) — historic 2001-2002, без независимой верификации; служат иллюстрацией механики, не source-of-truth для свежих расчётов. `conf:low`.

## Backlinks

_7 pages link to this one._

- [[canon/marketing-frameworks/breakage-business-model-fitness]]
- [[canon/marketing-frameworks/microniche-marketing-packages]]
- [[canon/marketing-frameworks/patagonia-refusal-as-asset]]
- [[canon/marketing-frameworks/sales-crm-minimum-fieldset]]
- [[canon/marketing-frameworks/value-for-customer-concept]]
- [[index]]
- [[sources/2026-05-05-e-xecutive-ru-condensed]]
