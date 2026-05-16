---
id: mkt:canon/marketing-frameworks/gdp-vs-marketcap-flow-stock-distinction-gorny
title: "ВВП vs капитализация — flow/stock дисциплина (Горный)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [analytics, finance, fact-check, content-discipline, economic-literacy, gorny]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-startupoftheday-may-5-13-2026.md]
namespace: mkt
---

# ВВП vs капитализация — flow vs stock дисциплина

Каноничный фактологический фильтр для маркетингового и аналитического контента. Зафиксирован Александром Горным в посте 5060 (2026-05-10) — см. [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]].

## Тезис

> «Хороший признак некомпетентности — прямое сравнение ВВП и капитализации. "Стоимость компании A обогнала ВВП страны X" и подобное. Если автор такое пишет — он не понимает, о чем пишет.»
> — Александр Горный, пост 5060 (2026-05-10) `[conf:high, src:2026-05-10]`

Это **basic financial-literacy дисциплина**, но регулярно нарушается в массовом media-контенте, включая авторский (бизнес-блогеры, новостные аккаунты, telegram-каналы).

## Технический разбор

### ВВП — это **flow**

- **Единица:** деньги в единицу времени ($/год, $/квартал, $/месяц)
- **Значение:** скорость производства товаров и услуг
- **Пример:** US GDP = $27T/год (2024)
- **Свойство:** 120 в год = 30 в квартал = 10 в месяц = 12000 в век — **одно и то же**

### Капитализация — это **stock**

- **Единица:** деньги (статично, $)
- **Значение:** оценка совокупной стоимости акций компании в моменте
- **Пример:** Apple market cap = $3.5T (точка во времени)
- **Свойство:** 100 — это 100, не «100/год»

### Правило операций

| Операция | Можно? | Пример |
|---|---|---|
| **Делить** stock на flow | ✅ Да | Capitalization / Annual GDP = «Buffett ratio»; имеет интерпретацию `years_of_economy` |
| **Складывать** stock + flow | ❌ Нет | $3.5T + $27T/year = бессмысленно |
| **Вычитать** stock − flow | ❌ Нет | «Apple capitalization обогнала ВВП Швейцарии» = категориальная ошибка |
| **Сравнивать ">"** stock vs flow | ❌ Нет | «X > Y» бессмысленно, как «самолёт быстрее, чем расстояние» |
| **Делить** stock на stock | ✅ Да | Apple cap / Microsoft cap = relative valuation |
| **Делить** flow на flow | ✅ Да | US GDP / China GDP = relative production |

## Аналогия Горного

> «Сравнивать их между собой это как "самолет быстрее, чем расстояние от Москвы до Питера". Нет, даже свет не быстрее, а улитка не медленнее.»

Это **canonical false-comparison test**: если сравнение двух величин разной размерности **не имеет интерпретации**, то и числа не имеют смысла.

## Применение в content-стратегии GRO

GRO — фитнес-приложение, **не финансовый сервис**. Прямой content-relevance к финансово-аналитическим темам отсутствует. Но фрейм применим **уровнем выше — как дисциплина создания корректного контента**.

### Use case 1: фактчек собственного контента

Перед публикацией поста или статьи проверять:
- **Каждая числовая comparison** = same dimension? (flow vs flow, stock vs stock, ratio vs ratio)
- **Числовое утверждение** = с источником? с датой? с пометкой `[conf:*]`?
- **Категоризация** = stable (canon) vs evolving vs volatile?

Это **basic дисциплина-чеклист**, который должен предшествовать публикации.

### Use case 2: content-filter для внешних источников

Если в source-tg/article видим «Apple capitalization обогнала ВВП страны X» — это **trigger** на:
- Понизить confidence до `low` для всего источника
- Воспринимать аналитику как narrative, не данные
- Cross-check ключевые тезисы через другой source

### Use case 3: counter-content hook

Hook-pattern для intermediate GRO-аудитории (interested in fitness + business):

> «"Уолл-стрит-капитализация GRO достигла $X миллионов — это больше, чем годовой бюджет на спорт в стране Y". Если такое читаете — закрывайте статью. Автор не понимает разницу между скоростью и расстоянием.»

Это **сильное opener** для постов про **факт-чек в эпоху AI-контента**, where GRO позиционируется как «продукт с дисциплиной фактов».

## Cross-domain transferability

Распространённые ошибки той же категории (flow vs stock) в маркетинге:

| Ошибочная metric | Тип ошибки | Корректное сравнение |
|---|---|---|
| «Чистый retention 90% (за квартал)» vs «Чистый retention 80% (за год)» | flow vs flow разной длины окна | Анализируется только при equal-period normalization |
| «MRR $1M» vs «ACV $1M» | flow vs ratio (расчётное) | MRR × 12 = ARR (правильная норма) |
| «CPL $20» vs «CAC $50» | acquisition-cost vs lifetime-cost | Совершенно разные понятия, не сравниваются напрямую |
| «10M MAU» vs «50K paying customers» | active users vs paying = ratio | Conversion = 0.5%, это **derived ratio** |
| «5K новых клиентов/месяц» vs «100K customers in total» | flow vs stock | Сравнивается только через growth rate (5%/month) |

Это **переносимый фрейм** для проверки маркетинговых metrics-claims.

## Anti-pattern — где НЕ применять (контекст важен)

- **Casual storytelling.** Если post — про вдохновение, а не про факт-анализ, дисциплина flow/stock может быть **смягчена с явным маркером «оценочно»**. Например: «Apple — больше, чем половина ВВП РФ» — corrigible если за этим стоит rough order-of-magnitude intuition, не precise claim.
- **Контент для широкой аудитории** — если читатель не знает, что такое ВВП, дисциплина становится pedantic. Адаптируй под аудиторию.

## Связанные страницы

- [[canon/marketing-frameworks/ai-text-markers-checklist]] — adjacent (fact-discipline для AI-generated content)
- [[canon/marketing-frameworks/mvp-definition-gorny]] — другой фрейм Горного (terminology discipline)
- [[canon/marketing-frameworks/business-metrics-for-owners]] — adjacent (metric-literacy для предпринимателей)
- [[canon/marketing-frameworks/business-valuation-methods-smb]] — adjacent (правильные методы valuation)
- [[evolving-strict/market-data/llm-token-pricing-deflation-2025-2026]] — пример strict-применения дисциплины (нумерические сравнения с inline-маркерами)
- [[evolving/industry-trends/big-tech-concentration-not-bubble-gorny-2026]] — паттерн Горный «counter-anchor через корректный фрейм»
- [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]] — оригинал (пост 5060)
