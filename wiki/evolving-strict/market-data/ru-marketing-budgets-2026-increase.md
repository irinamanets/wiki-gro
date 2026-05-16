---
id: mkt:evolving-strict/market-data/ru-marketing-budgets-2026-increase
title: "RU маркетинг-бюджеты 2026 — 63% компаний планируют увеличение"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [market-data, russia, marketing-budgets, 2026, smb, q2-2026]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-moibiz-apr-21-may-05.md]
namespace: mkt
---

# RU маркетинг-бюджеты 2026 — 63% компаний планируют увеличение `[conf:medium, src:2026-04-28]`

Сводный single-data-point: по данным, упомянутым в дайджесте @moibiz за 28 апреля 2026 (пост 7459, [[sources/2026-05-05-tg-moibiz-apr-21-may-05|source]]), **63% компаний в России планируют увеличить бюджеты на маркетинг в 2026 году** `[conf:medium, src:2026-04-28]`. Первоисточник в посте не раскрыт (vk.cc-ссылка, перепечатка из отраслевого медиа).

## Метрика

| Показатель | Значение | Период | Source |
|---|---|---|---|
| Доля российских компаний, увеличивающих бюджет на маркетинг в 2026 | 63% | планы на 2026 | `[conf:medium, src:2026-04-28]` |

`[conf:medium, src:2026-04-28]` — потому что:
- Источник вторичный (дайджест @moibiz пересказывает отраслевую публикацию)
- Первичная методология не раскрыта (sample size, distribution by industry, by size, методика опроса)
- Упоминается без конкретного контекста (общая формулировка из дайджеста)

**Перед использованием в публичных GRO-материалах** — найти первоисточник, проверить методику, проверить sample.

## Контекст и интерпретация

Эта метрика — **прямое противоречие** narrative «сжимающегося спроса» Q1 2026 (см. [[evolving/industry-trends/ru-smb-sales-q1-2026]] и [[evolving-strict/market-data/ru-business-q1-2026-survey]]). 37,6% компаний жалуются на падение потребительского спроса в Q1 2026 `[conf:medium, src:2026-05-04]`, и при этом 63% планируют **увеличивать** маркетинговые бюджеты `[conf:medium, src:2026-04-28]`.

Это **не парадокс**, а **сигнал бифуркации рынка**:

- **Те, у кого есть запас прочности** (большие компании, крепкие SMB, новые технологические бизнесы) — **увеличивают** маркетинг, чтобы захватить долю выходящих из рынка игроков. Падение спроса означает дешёвые лиды для тех, кто остаётся.
- **Те, у кого нет запаса** (struggling SMB, описанные в [[evolving/industry-trends/ru-smb-sales-q1-2026]]) — режут маркетинг и попадают в нисходящую спираль (см. [[evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026]]).

Это типовой консолидационный паттерн в downturn: рынок переcortines, оставшиеся игроки укрупняются.

## Релевантность для GRO

**Для маркетинга GRO как продукта:**

- **Hook:** «63% российских компаний увеличат бюджет на маркетинг в 2026. Если вы среди них — каждый рубль сейчас на счёт. GRO помогает не выгореть, тратя бюджет на запуск кампаний.» `[conf:medium, src:2026-04-28]` (мостик к продуктовому value-proposition GRO как «личной устойчивости фаундера»).
- **Macro-якорь:** в любых внутренних обоснованиях «маркетинг сейчас актуален» эта цифра — точка опоры. **Но**: 63% `[conf:medium, src:2026-04-28]` **планируют** увеличить — это не **уже увеличили**. Реальные post-action data появятся в H2 2026.
- **Аудитория-фильтр:** 63% `[conf:medium, src:2026-04-28]` — это среднее по большинству секторов. Для b2c-розницы / общепита картина может быть прямо противоположной (см. [[evolving-strict/market-data/ru-business-q1-2026-survey]]). Для GRO ICP (соло-фаундеры, продуктовые предприниматели) — ближе к среднему 63% `[conf:medium, src:2026-04-28]`, чем к минимуму.

**Для контента GRO:**

- Использовать в нарративе «несмотря на сжимающийся спрос Q1 2026, маркетинг не умер — он перераспределяется».
- Combinable с другими бенчмарк-цифрами: см. [[evolving-strict/market-data/ru-smb-digital-ad-spend-2026]] (operational digital ad spend SMB), [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] (общий рынок РФ).
- **Не использовать как «факт о всём рынке»** — это plan-data, не actual-data.

## Caveat'ы и TTL

- **Plan vs actual:** опросы планов часто overestimate реальные изменения. Реальные H1 2026 данные могут показать lower delivery vs plan.
- **Источник не верифицирован:** до выяснения первоисточника `confidence` зафиксирован `medium`. Если первоисточник окажется методологически слабым (n=200 case-by-case, без weighing) — confidence пересматривается до `low`.
- **TTL:** 180 дней (evolving-strict). Re-verify не позднее 2026-10. Replace fact с actual-data, как только она появится.
- **Сравнить с другими источниками** при ingest [[evolving-strict/market-data/deloitte-marketing-trends-2026]], [[evolving-strict/market-data/global-marketing-outlook-2026]] — нет ли парных глобальных метрик.

## Связанные страницы

- [[evolving-strict/market-data/ru-smb-digital-ad-spend-2026]] — operational digital ad spend
- [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] — общий рекламный рынок РФ
- [[evolving-strict/market-data/ru-business-q1-2026-survey]] — Q1-кризис спроса (контр-сигнал)
- [[evolving/industry-trends/ru-smb-sales-q1-2026]] — нарратив Q1-кризиса
- [[evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026]] — другая сторона бифуркации
- [[evolving-strict/market-data/deloitte-marketing-trends-2026]] — глобальный benchmark
- [[sources/2026-05-05-tg-moibiz-apr-21-may-05]] — источник
