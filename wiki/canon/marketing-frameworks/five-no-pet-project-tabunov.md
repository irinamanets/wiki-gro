---
id: mkt:canon/marketing-frameworks/five-no-pet-project-tabunov
title: 5 НЕТ для пет-проекта (Табунов) — operational-чек-лист bootstrap-парадигмы
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [pet-project, bootstrap, anti-pattern, founder-mindset, mvp, solopreneurship, operational-checklist]
confidence: medium
stale: false
created: 2026-05-18
updated: 2026-05-18
sources: [sources/2026-05-13-tg-your-pet-project-may-6-13-2026.md]
namespace: mkt
---

# 5 НЕТ для пет-проекта (Табунов)

Operational-чек-лист от Михаила Табунова ([[sources/2026-05-13-tg-your-pet-project-may-6-13-2026]] пост 622, 2026-05-07): пять explicit disqualifier-критериев, который превращают pet-проект в **мини-бизнес**. Прямое расширение [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov|Bootstrap vs Startup]]-рамки — пять конкретных операционных правил, отделяющих bootstrap-паттерн от стартап-anti-pattern.

`confidence: medium`: эксперт-inferred (founder Baza Education, два года public content на эту тему), framework предельно лаконичен, но каждое правило пересекается с устоявшимися anti-pattern наблюдениями indie-hacker community.

## Главный тезис

> «Чтобы твой проект превратился в мини-бизнес, нужно сказать пять НЕТ.»
>
> «Ведь самое главное — иметь достаточно простой проект, чтобы тупо доделать его до конца. **Сложности и так будут.**»

## Пять НЕТ

### 1. НЕТ идеям, которые не объяснить ребёнку

**Что это исключает:** деривативные идеи в духе «AI-powered SaaS for cross-platform B2B SEO content automation pipeline». Если ребёнку 8 лет нельзя объяснить за 30 секунд **что продукт делает**, то ни в твиттере, ни на лендинге, ни в TikTok-преролле — никто не поймёт.

**Анти-пример:** «платформа для умного управления контентом в эпоху AI».
**Pro-пример:** «приложение, которое будит тебя только когда выполнил задание». (см. [[evolving-strict/competitor-metrics/yp-may-2026-50k-mrr-app-cluster|Wayk]] кейс)

**Connection:** прямо ложится на [[canon/marketing-frameworks/definition-of-done-product-positioning|DoD framework]] поста 610 предыдущего ingest'a — «лендинг = заявленный конкретный результат за конкретное время».

### 2. НЕТ идеям, за которые не платят

**Что это исключает:** идеи, **уже работающие** только потому, что «никто не сделал хороший продукт». Если в нише ноль конкурентов с платным предложением — это сигнал отсутствия рынка, не его открытия.

**Anti-pattern:** «я делаю это потому что мне самому надо». Если ты сам не готов заплатить за это $20-50/мес — никто не готов.

**Pro-pattern:** «иду туда, где люди уже платят» (см. [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] — bootstrap-cэлл «куда уже платят»).

**Connection:** структурно эквивалентно [[canon/marketing-frameworks/blue-ocean-strategy-anti-pattern]] — «нет конкурентов = нет рынка».

### 3. НЕТ исследованиям, касдевам и опросам

**Что это исключает:** custdev-исследования, опросы потенциальных клиентов, focus groups. Они **не дают**:
- Реальной готовности платить (interviewees переоценивают свой будущий willingness).
- Реальной частоты использования (overestimate).
- Реальной приоритезации фич (anchoring on most-recently-mentioned).

**Pro-pattern:** Прямая продажа в качестве validation. **«Валидация только через прямую продажу»** (см. [[evolving/content-trends/your-pet-project-channel-hooks]] launch mythology hooks).

**Connection:** структурно эквивалентно [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev|MVP-launch anti-perfectionism]] и [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] «продают раньше, чем построили».

### 4. НЕТ продуктам, которые не запилить на коленке за две недели

**Что это исключает:**
- Продукты с тяжёлым backend-инфраструктурным компонентом.
- Микросервисные архитектуры на старте.
- Продукты, требующие compliance / regulatory approval до первой продажи.
- ML-pipelines, которые требуют training data до запуска.

**Implication:** на 2026 году с AI-tools (Claude Code, Cursor, Bubble) **«две недели»** = **MVP лендинг + Stripe-checkout + Telegram-бот / простой web-app / wrapper над OpenAI API**. См. [[canon/marketing-frameworks/landing-15min-figma-cursor]].

**Pro-pattern:** обёртки над GPT/Claude/Gemini (см. [[evolving-strict/competitor-metrics/yp-may-2026-50k-mrr-app-cluster|LiveTranslator, IQ Boost cases]] — это именно такие обёртки), no-code-MVP, single-feature-product.

**Connection:** прямо ложится на [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] — agent-обёртки на $99/мес, не enterprise-SaaS.

### 5. НЕТ выходу из найма и привлечению инвестиций

**Что это исключает:**
- Уход из работы до достижения unit-economy-валидации.
- Раунды pre-seed / seed на pet-проект.
- Friends & Family investment.
- Аксесераторы и инкубаторы.

**Pro-pattern:** «Час в день + $200-300 трафика/мес → $5K MRR за полгода» (см. [[evolving/content-trends/your-pet-project-channel-hooks]] из поста 600). Найм даёт **финансовую подушку** для **итераций** — преждевременный уход из работы создаёт давление «надо срочно зарабатывать» = плохие решения.

**Connection:**
- [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] — основная рамка (стартапер живёт на деньги инвестора, бутстреппер — на свои + клиента).
- [[canon/marketing-frameworks/blank-when-to-raise-investment]] — каноническая Blank-рамка про когда раунд оправдан.

## Operational-таблица

Сводная таблица для быстрой self-диагностики:

| # | Запрет | Симптом anti-pattern | Pro-pattern |
|---|---|---|---|
| 1 | Идея, которую не объяснить ребёнку | «AI-powered SaaS for…» | One-sentence value prop, понятный 8-летнему |
| 2 | Идея, за которую не платят | «Никто не делает, потому что неоткрытый рынок» | «Куда уже платят» |
| 3 | Исследования / касдевы / опросы | Месяц на «валидацию идеи без денег» | Прямая продажа MVP |
| 4 | Продукт >2 недель разработки | Микросервисы / ML-pipelines / regulatory | Обёртка над AI API / no-code / single-feature |
| 5 | Уход из найма + инвестиции | «Уволюсь и буду фокусироваться» | Час в день + $200-300 трафика |

## Применение к GRO content

5 НЕТ — это **готовый contrarian hook-format** для контента GRO:

- Каждое НЕТ — отдельный пост с deep-dive в anti-pattern.
- Структура поста: НЕТ → почему 80% фаундеров делают это → конкретный пример провала → pro-pattern.
- Соответствие сегментам [[canon/target-audience/gro-segments]]:
  - **Предприниматели на пороге первого pet-проекта** — основной адресат.
  - **Карьеристы с side-project дилеммой** — НЕТ #5 (уход из найма) прямо для них.
  - **Фрилансеры с pet-product дилеммой** — НЕТ #4 (за 2 недели) прямо для них.

## Hooks для GRO content

| Стадия воронки | Hook | Какому сегменту |
|---|---|---|
| Awareness | «5 НЕТ, без которых твой пет-проект не станет бизнесом.» | Все три сегмента |
| Awareness | «НЕТ исследованиям и касдевам. Валидация только через прямую продажу.» | Предприниматели |
| Consideration | «НЕТ выходу из найма. Час в день и $200/мес трафика → $5K MRR за полгода.» | Карьеристы + предприниматели |
| Decision | «Сложности и так будут. Главное — простой проект, чтобы тупо доделать до конца.» | Все сегменты на пороге запуска |

## Связанные страницы

- [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] — основная рамка, в которую вписан 5-НЕТ-чеклист
- [[canon/marketing-frameworks/zero-to-one-vs-scale-tabunov]] — параллельная рамка отделения задач до и после PMF
- [[canon/marketing-frameworks/blue-ocean-strategy-anti-pattern]] — fundament для НЕТ #2 («куда платят»)
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] — fundament для НЕТ #3
- [[canon/marketing-frameworks/landing-15min-figma-cursor]] — fundament для НЕТ #4
- [[canon/marketing-frameworks/blank-when-to-raise-investment]] — fundament для НЕТ #5
- [[canon/marketing-frameworks/definition-of-done-product-positioning]] — fundament для НЕТ #1
- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] — операционный pattern wrapper-stack под НЕТ #4
- [[evolving/content-trends/your-pet-project-channel-hooks]] — host-страница hooks канала (содержит этот чеклист как hook)
- [[evolving-strict/competitor-metrics/yp-may-2026-50k-mrr-app-cluster]] — кейсы реализаций 5 НЕТ
- [[canon/target-audience/gro-segments]] — кому адресовать
- [[sources/2026-05-13-tg-your-pet-project-may-6-13-2026]] — источник
