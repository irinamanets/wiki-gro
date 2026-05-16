---
id: mkt:evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026
title: LLM token-pricing deflation 2025–2026 — anchor-точки от Горного
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [ai, llm, pricing, deflation, openai, deepseek, market-data, awareness]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-14  # +Grok 4.3 ($1.25/$2.50) от Кульгина @bezsmuzi 15860 — заполняет mid-tier pricing point ($2.50/M output)
sources: [sources/2026-05-05-tg-startupoftheday-apr-may-2026.md, sources/2026-05-14-tg-bezsmuzi-may-5-7.md]
namespace: mkt
---

# LLM token-pricing deflation — anchor-точки 2025–2026

Числовая страница с конкретными anchor-кейсами **снижения цены LLM-токенов** между 2025 и 2026. Артикулирована Александром Горным в посте 5052 (2026-05-05) — см. [[sources/2026-05-05-tg-startupoftheday-apr-may-2026]].

**Почему `evolving-strict`:** числа конкретные с привязкой к датам, обновляются с release-cycle моделей (~3-6 месяцев), inline-маркеры обязательны. Через 6 месяцев anchor-точки могут устареть и потребовать ре-верификации.

## Тезис Горного

> «Точно такая же фигня происходит и с AI. Мы злимся на появление лимитов и ограничений там, где их не было. Мы воспринимаем как должное появление дешевых моделей, которые обыгрывают прошлогодние топовые.»

Горный использует **аналогию с такси Москвы** для иллюстрации:

| Параметр | Такси 2009 | Такси 2026 | Дельта |
|---|---|---|---|
| Цена в рублях | 400 ₽ | 868 ₽ | +117% (рост) `[conf:medium, src:2026-05-05]` |
| Цена в долларах | $13 | $11.5 | −11% (падение) `[conf:medium, src:2026-05-05]` |
| Цена в минимальных зарплатах | 1/10 МРОТ | 1/30 МРОТ | −67% (падение) `[conf:medium, src:2026-05-05]` |
| Цена в реальных рублях 2009 | 400 ₽ | 277 ₽ | −31% (падение) `[conf:medium, src:2026-05-05]` |
| Цена в реальных рублях 2026 | 1252 ₽ | 868 ₽ | −31% (падение) `[conf:medium, src:2026-05-05]` |
| **Качество** | Без страхования, старые машины, без приложения | Страхование, новые машины, удобное приложение | Резко выше `[conf:high, src:2026-05-05]` |

> «На самом деле объективно цена упала. При том, что поездки застрахованы, машины более-менее новые, государство начало брать какие-то налоги, с приложением стало удобнее — т.е. качество-то за это время выросло.»

**Аналогия с AI:** так же. Видим **лимиты и ограничения** (что воспринимается как «дорожает»), не видим **снижение effective price per quality unit**.

## Anchor-кейсы по моделям LLM

### GPT-4o (OpenAI, baseline 2025)

**Цена за 1M исходящих токенов:** **$10** `[conf:medium, src:2026-05-05]` (Горный референсная точка для baseline 2025)

Контекст: GPT-4o был **лучшей доступной моделью** на конец 2025 — массовый default для production-задач middle-complexity.

### GPT 5.4-mini (OpenAI, 2026)

**Качество:** «сильнее» GPT-4o (по мнению Горного) `[conf:medium, src:2026-05-05]`

**Цена:** **в 2.5 раза дешевле** GPT-4o → **~$4 за 1M исходящих токенов** `[conf:medium, src:2026-05-05]`

**Дельта:** за **1 год** между топ-моделью 2025 и mini-моделью 2026 — **−60% цены при +N% качества**. `[conf:medium, src:2026-05-05]`

### Deepseek V4 Flash (DeepSeek, 2026)

**Качество:** для большинства задач сопоставимо с GPT-4o (по мнению Горного), Deepseek V4 — frontier китайская модель.

**Цена:** **в 40 раз дешевле** GPT-4o → **~$0.25 за 1M исходящих токенов** `[conf:medium, src:2026-05-05]`

**Дельта:** между OpenAI premium-tier 2025 и open-weight Asian frontier-model — **−97.5% цены при сопоставимом качестве**. `[conf:medium, src:2026-05-05]`

> «Если не гнаться за брендом, то Deepseek V4 Flash дешевле, чем 4o в 40 (сорок) раз.»

## Сводная таблица anchor-точек deflation

| Модель | Год | $/1M output tokens | Quality vs GPT-4o (оценка Горного) | Δ к GPT-4o | Source |
|---|---|---|---|---|---|
| GPT-4o (OpenAI) | 2025 (baseline) | $10 | (baseline) | — | `[conf:medium, src:2026-05-05]` |
| GPT 5.4-mini (OpenAI) | 2026 | ~$4 | сильнее | −60% | `[conf:medium, src:2026-05-05]` |
| Grok 4.3 (xAI) | 2026 (май) | $2.50 (input $1.25/M) | «бенчмарки лучше многих» (Кульгин ретранслирует, без конкретики) | −75% | `[conf:medium, src:2026-05-05]` |
| Deepseek V4 Flash | 2026 | ~$0.25 | сопоставимо для большинства задач | −97.5% | `[conf:medium, src:2026-05-05]` |

**Grok 4.3** заполняет **mid-tier nicheing pricing point** между GPT 5.4-mini и DeepSeek V4 Flash. Доступ через OpenRouter, что сигнализирует, что xAI начинает биться **на developer/aggregator-сегмент** через мульти-моделевые workflow. См. [[volatile-strict/competitor-news/xai-grok-4-3-release-2026-05]] для контекста релиза. `[conf:medium, src:2026-05-05]`

**Вывод Горного:** «Но, конечно, дорожает. И лимиты ух какие злые стали.»

То есть consumer-perception («AI стал дороже из-за лимитов») и market-reality (effective price per quality dropped 60-97%) **расходятся в противоположные стороны**. `[conf:medium, src:2026-05-05]`

## Применение в маркетинге GRO

### Hook variant A: «AI стал дешевле в 40 раз. Это та самая картинка, которая не транслируется в нарратив»

Аудитория — предприниматели и founders. Сильный counter-anchor для тех, кто **не использует AI потому что "дорого"**.

> «Считаешь, что AI неоправданно дорог? Топ-модель 2025 года стоила $10 за миллион токенов. Сегодня DeepSeek-V4 Flash делает то же самое за **25 центов** `[conf:medium, src:2026-05-05]`. Это 40-кратное снижение цены **за один год**. Если ты ждёшь, что станет ещё дешевле прежде, чем начнёшь — ты опоздаешь к мощности.»

### Hook variant B: «Лимиты — это не подорожание»

Аудитория — power-users (карьеристы, vibe-coders), кто столкнулся с лимитами на consumer-tier'е.

> «Anthropic ввёл лимиты на Claude Pro. OpenAI понизил квоты на ChatGPT Plus. Кажется, что AI стал дороже. Но реальная цена 1M токенов упала с $10 до $4 (OpenAI) и до **25 центов** (DeepSeek) `[conf:medium, src:2026-05-05]`. Лимиты — это **rationing**, не **inflation**. Это разные вещи.»

### Hook variant C: «Тачка-аналогия Горного для контента»

Готовая визуальная аналогия для постов: «такси 2009 vs такси 2026 в реальных деньгах vs восприятие».

Аудитория — широкая, требуется работа с реальными vs номинальными ценами. Подходит для образовательного контента про economics.

## Рамки и оговорки

- **Цены — оценка Горного, не verified pricing list.** OpenAI / DeepSeek официальные pricing-страницы могут давать другие цифры в каждый момент. Использовать с атрибуцией «по оценке Горного» или «по cross-reference с MWS Model Hub». Не цитировать как «официальный price-table».
- **Качественное сравнение не строго.** «GPT 5.4-mini сильнее GPT-4o» и «Deepseek V4 Flash сопоставим» — это **subjective expert assessment** Горного, не результат бенчмарка. Не использовать как absolute claim.
- **40x deflation за год** — релевантно для специфической кросс-vendor сравнений (OpenAI top vs DeepSeek frontier) `[conf:medium, src:2026-05-05]`. Внутри одного vendor (OpenAI 4o → 5.4-mini) deflation = 60% `[conf:medium, src:2026-05-05]`, что **высоко, но не экстремально**. В контенте важно не путать эти два случая.
- **Direction stable, magnitude noisy.** Гарантированно цены **продолжат падать** при exponential model-progress. Конкретные коэффициенты будут двигаться, но pattern (2-10x deflation/year на consumer pricing) — стабильный `[conf:low, src:2026-05-05]`.

## Связанные страницы

- [[canon/marketing-frameworks/token-economics-cost-vs-value-amodei]] — структурная рамка: cost равен, value на порядки разный (Amodei × Горный complementary)
- [[evolving-strict/market-data/ai-coding-tools-cost-explosion-2026]] — opposite anchor: enterprise high-volume cost explosion. Парадокс: consumer pricing deflates, enterprise OPEX explodes.
- [[evolving/industry-trends/ai-energy-bottleneck-debunked-gorny-2026]] — связанный counter-FUD thesis от того же автора
- [[evolving/industry-trends/ru-ai-aggregator-platforms-2026]] — MWS Model Hub: -95% input promo, -80% output promo (RU аналог DeepSeek deflation на cost-conscious сегменте) `[conf:high, src:2026-04-29]`
- [[evolving/industry-trends/software-moat-erosion-2026]] — moat-эрозия от dropping cost
- [[evolving/competitor-positioning/aiacademy-claude-code-course-gorny-shevchenko-2026]] — соавтор Горный коммерциализирует свой анализ через course
- [[sources/2026-05-05-tg-startupoftheday-apr-may-2026]] — оригинал
- [[sources/2026-05-14-tg-bezsmuzi-may-5-7]] — Grok 4.3 release с pricing $1.25/$2.50
- [[volatile-strict/competitor-news/xai-grok-4-3-release-2026-05]] — контекст релиза Grok 4.3

## TTL и ре-верификация

`evolving-strict` — через **90 дней** (2026-08-05) snap текущие pricing GPT-5.4-mini, DeepSeek V4 Flash, добавить ряды для GPT-5.5 / Claude 4 / Gemini 3 если выйдут. Если deflation rate останется 2x/year — pattern становится stable, кандидат на переход в `canon/marketing-frameworks` как универсальный price-trajectory anchor.

## Backlinks

_5 pages link to this one._

- [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]]
- [[evolving/industry-trends/ai-energy-bottleneck-debunked-gorny-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-startupoftheday-apr-may-2026]]
