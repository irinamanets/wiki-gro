---
id: mkt:canon/marketing-frameworks/three-question-product-test-moreynis
title: 3-вопросный product test (retell Морейниса)
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [product-management, mvp, decision, framework, startup]
confidence: low
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-temno-moreynis-may-5-14-2026.md]
namespace: mkt
---

# 3-вопросный product test

Лёгкий фреймворк product management для оценки идеи продукта на самой ранней стадии. Пересказан **Аркадием Морейнисом** ([@temno](https://t.me/temno), [пост 7830 от 2026-05-12](https://t.me/temno/7830)) со ссылкой на неназванный американский стартап (оценка $11.5B `[conf:low, src:2026-05-12]`).

`confidence: low` — потому что Морейнис не указывает первичный источник (имя стартапа / автора). Сам фреймворк звучит как **conventional wisdom** (Y Combinator-style), сшитая в трёх-вопросный формат.

## Три вопроса

> Принципы продуктового менеджмента одного американского стартапа, который сейчас оценивается в 11.5 миллиардов долларов, основан на трёх вопросах. — Морейнис, [[sources/2026-05-14-tg-temno-moreynis-may-5-14-2026|пост 7830, 2026-05-12]]

### Вопрос 1: Value at launch — может ли продукт иметь ценность сразу после запуска?

> Может ли продукт иметь ценность сразу после запуска? Если нет — то нет времени тратить на это время.

**Mechanism:** если продукт требует «накопления данных», «сети пользователей», «обучения модели», чтобы давать ценность — это **kill criterion** на раннем этапе. Стартап с финансами runaway < 12 месяцев не может позволить «long ramp to value».

**Anti-pattern:** «через 6 месяцев у нас будет N пользователей и тогда продукт начнёт работать». Это **chicken-egg**, который убивает большинство мar/keтplace стартапов на раннем этапе.

**Каноническое следствие:** строй продукты с **immediate value на первого пользователя**, network effect — bonus, не requirement.

### Вопрос 2: Building block — может ли продукт быть кирпичиком для следующих?

> Может ли этот продукт быть кирпичиком для следующих продуктов? Если нет — не делаем, потому что это тупиковая ветвь развития.

**Mechanism:** ранний стартап делает не «один продукт», а **первую stepping stone в продуктовой стратегии**. Если продукт A не открывает дверей к продукту B → стартап ограничен потолком A.

**Examples:**
- Stripe начинал с payment API → стал инфра-стэком (Atlas, Connect, Climate, Issuing) — каждая «новая фича» — следующий продукт.
- Notion начинал с note-taking → стал database / collaboration / AI workspace — каждый этап раздвигает рынок.
- Anti-pattern: одно-функциональные tools без roadmap (URL shorteners, single-purpose Chrome extensions).

**Каноническое следствие:** при выборе MVP смотри не на «что нужно сейчас», а на «что станет возможным после, если это построено». Продукт-фундамент > продукт-результат.

### Вопрос 3: Minimum testable — можно ли проверить гипотезу на минимальном числе пользователей?

> Можно ли проверить гипотезу ценности на минимальном количестве пользователей? Если да — делаем и быстро проверяем. Если не работает — быстро выкидываем. Если работает — начинаем делать то, для чего этот продукт является кирпичиком.

**Mechanism:** ключ — **минимальное N пользователей**, чтобы гипотеза была validated. Если для proof нужны 1000 пользователей — это не testable hypothesis, это full launch. Если хватает 10-50 пользователей и binary outcome (работает / не работает) — это правильно сформулированная гипотеза.

**Anti-pattern:** «нам нужно 6 месяцев публичной beta, чтобы понять, есть ли market». Скорее всего, неправильно сформулирована гипотеза.

**Каноническое следствие:** scope MVP по «minimum sample for validation», не по «full feature set».

## Как работает все три вопроса вместе

Это **AND-gate** — все 3 должны быть «да», чтобы продукт прошёл:

```
Идея → Q1 (immediate value) → Q2 (building block) → Q3 (testable on minimum N) → Решение делать
              ↓ нет                  ↓ нет                  ↓ нет
              KILL                   KILL                   KILL
```

Если хотя бы один — «нет», идея либо переформулируется, либо killed.

## Связь с другими product-test фреймовкками

### Vs [[canon/marketing-frameworks/demand-first-mvp-castdev|Demand-first MVP]]

Demand-first MVP: проверь спрос перед сборкой. 3-question test: оцени стратегическую жизнеспособность перед запуском demand-test. Они **complementary** — 3-question test — pre-test, demand-first MVP — post-test.

### Vs [[canon/marketing-frameworks/mvp-definition-gorny|MVP по Горному]]

Горный: MVP — это минимальное, что отвечает на гипотезу. 3-question Q3 — это **operationalization** этого правила («минимальное число пользователей для validation»).

### Vs [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev|Anti-perfectionism MVP-launch]]

Anti-perfectionism: выпусти MVP «недоделанным». 3-question test даёт **критерий**, когда «недоделанность» оправдана (Q3 — если minimal users достаточно для validation, дальше дотачивать не нужно до запуска).

### Vs [[canon/marketing-frameworks/disproportionality-hypothesis-moreynis|Disproportionality hypothesis]]

Disproportionality — критерий **стратегической вирабильности** идеи (рычаг, неравенство). 3-question test — **тактический pre-launch test**. Они работают на разных уровнях: disproportionality — на уровне всей стратегии, 3-question test — на уровне каждого нового продукта внутри стратегии.

## Anti-patterns 3-question test

1. **Reframing «нет» в «да».** Founder любит свой продукт → переформулирует «продукт не имеет value at launch» в «продукт имеет потенциальную value». **Q1 — binary**, не «потенциал».
2. **Использование как stage-gate в больших корпорациях.** В корпоративном контексте 3-question test может стать политическим оружием: «отвергнем продукт через Q2 (это не кирпичик)». Использование без понимания контекста — anti-pattern.
3. **Игнорирование Q2 на раннем этапе.** «Мы пока не знаем, что построим дальше — поэтому скипнем Q2». Это даёт permission to build one-offs.
4. **Q3 без binary outcome.** Если «проверяем» через метрики «retention 30%», но не определено, что «успех = 30%», а «провал = 15%» — Q3 не работает.

## Operational-применение для GRO

Для каждой новой фичи / продуктовой линии GRO:

| Вопрос | Применение |
|---|---|
| Q1: value at launch? | Должна ли фича работать на первом пользователе без сообщества / накопленных данных? |
| Q2: building block? | Открывает ли эта фича дорогу к следующим (например, accountability → cohort → marketplace экспертов)? |
| Q3: minimum testable? | Сколько пользователей нужно, чтобы понять, работает фича или нет? Если >100 — переформулируйте. |

**Hook для блога:** «3 вопроса перед каждой новой фичей — фреймовка $11.5B стартапа» (с caveat retell Морейниса).

## Cross-links

- [[canon/marketing-frameworks/demand-first-mvp-castdev]] — complementary post-test
- [[canon/marketing-frameworks/mvp-definition-gorny]] — определение MVP
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] — позволение запускать «недоделанное»
- [[canon/marketing-frameworks/disproportionality-hypothesis-moreynis]] — стратегический pre-test
- [[canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis]] — playbook от того же автора
- [[canon/marketing-frameworks/latent-demand-ai-startup-search-moreynis]] — стратегическая рамка для Q1 (где value at launch достижима)
- [[canon/marketing-frameworks/bubble-chart-prioritization]] — альтернативный prioritization-инструмент
- [[sources/2026-05-14-tg-temno-moreynis-may-5-14-2026]] — источник
