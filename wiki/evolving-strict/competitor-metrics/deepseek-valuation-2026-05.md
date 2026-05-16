---
id: mkt:evolving-strict/competitor-metrics/deepseek-valuation-2026-05
title: "DeepSeek валюация — $10B → $50B (Reuters supersede FT-leak $45B, 6 мая 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [ai, deepseek, china, valuation, funding, reuters, ft, state-fund]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14  # +Reuters supersede 6 мая: $50B (up from FT-leak $45B) + сумма раунда $3-4B (vs $300M первого FT-черновика). Cumulative escalation timeline: $10B → $20B → $45B → $50B за 2 недели.
sources: [sources/2026-05-14-tg-vcnews-may-5-8-2026.md, sources/2026-05-14-tg-theedinorog-may-2026.md]
namespace: mkt
---

# DeepSeek валюация — $10B → $50B (Reuters 6 мая 2026)

В ходе переговоров о привлечении **первых для компании внешних инвестиций** оценка **DeepSeek** значительно выросла. `[conf:medium, src:2026-05-06]`

## Цифры (актуальные — Reuters supersede 2026-05-06)

| Метрика | Значение | Source |
|---|---|---|
| Оценка до раунда | $10 млрд | `[conf:medium, src:2026-05-06]` |
| Оценка раунда | **$50 млрд** (Reuters supersede $45B FT-leak) | `[conf:medium, src:2026-05-06]` |
| Сумма раунда | **$3–4 млрд** (вместо первоначально упомянутых $300M в апреле) | `[conf:medium, src:2026-05-06]` |
| Мультипликатор роста | ×5.0 (за 2 недели от первого FT-leak в апреле) | `[conf:medium, src:2026-05-06]` |
| Тип раунда | Первые внешние инвестиции | `[conf:medium, src:2026-05-06]` |
| Лид-инвестор | **Китайский национальный AI-фонд** (создан в январе 2026) | `[conf:medium, src:2026-05-06]` |

Источник на 2026-05-06: **Reuters**, [reuters.com/world/asia-pacific/deepseek-nears-45-billion-valuation](https://www.reuters.com/world/asia-pacific/deepseek-nears-45-billion-valuation-chinas-big-fund-leads-investment-talks-ft-2026-05-06/) — через Edinorog 7929 ([[sources/2026-05-14-tg-theedinorog-may-2026]]). Reuters ссылается на FT-leak от 6 мая 2026, но добавляет деталь $50B (не $45B). `[conf:medium, src:2026-05-06]`

<!-- superseded 2026-05-14 by [[sources/2026-05-14-tg-theedinorog-may-2026]] (Reuters 6 мая 2026): было «Оценка раунда $45 млрд / Мультипликатор ×4.5 / Сумма не указана / лид «крупнейший госфонд КНР»» — теперь $50B, ×5.0, $3-4B сумма, лид «китайский национальный AI-фонд» (январь 2026). Reuters добавил детали к FT-leak. -->

**Confidence: medium** — FT-leak + Reuters до закрытия раунда; цифра $50B = leaked target valuation, не подтверждённое closing.

## Escalation timeline

В одном новостном цикле (конец апреля → 6 мая 2026):

| Дата | Оценка | Source |
|---|---|---|
| 2026-04 (начало) | $10 млрд (target round) | `[conf:medium, src:2026-04]` (Edinorog 7867) |
| 2026-04 (после недели) | $20 млрд (leak) | `[conf:medium, src:2026-04]` |
| 2026-05-06 (FT) | $45 млрд (FT-leak) | `[conf:medium, src:2026-05-06]` |
| 2026-05-06 (Reuters) | **$50 млрд** (актуальный) | `[conf:medium, src:2026-05-06]` |

Это **escalation × 5 за 2 недели** на стадии переговоров. Характеристика стиля китайских AI-pre-IPO-раундов 2026 года.

## Маркетинговое значение

### 1. **Китайская AI-капитальная гонка официально открыта**

До этого DeepSeek был известен как **bootstrap-стартап Liang Wenfeng без внешних инвестиций**. Компания получила глобальную известность в январе 2025 после релиза DeepSeek-V3 и R1 — frontier-модели, тренируемые **в 10× меньшим compute-бюджетом**, чем у конкурентов. Это **подрывной шок** для US-валуаций OpenAI/Anthropic (TCO-снижение в 10× = revaluation всей отрасли).

**Майский раунд 2026:** DeepSeek **признаёт необходимость капитала** для следующих стадий. Госфонд КНР как лид означает:

- **Китайское государство активно вкладывает** в frontier-AI (раньше это были private deep tech VC).
- **DeepSeek будет масштабироваться** за счёт государственного capital, не commercial — это новый паттерн вертикали «AI-as-state-strategy».
- **Не выйдет на западные биржи** в обозримое время (государственная связь = compliance issues).

### 2. Сравнение с US-моделью капитализации frontier-AI

| Вендор | Последняя валюация | Capital model |
|---|---|---|
| OpenAI | ~$500B (Nov 2025, see [[volatile-strict/industry-news/openai-852b-valuation-doubt-2026]]) | Microsoft + VCs |
| Anthropic | ~$200B (April 2026, see [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]]) | Amazon + Blackstone-PE |
| xAI/SpaceXAI | ~$200B (private, через SpaceX cap-stack) | Musk capital pool |
| **DeepSeek** | **$50B** (Reuters 2026-05-06) | **China state fund** |
| Moonshot (Kimi) | $20B (May 2026) | Pre-IPO Hong Kong |

`[conf:medium, src:2026-05-06]` для всех (см. [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] для полной таблицы и method).

**DeepSeek = 4-я нога capital-race** (см. [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] для общей карты ног). Раньше его не было в counting — теперь явно входит.

### 3. **Структурный сигнал для RU-AI**

Российский AI-сектор (Yandex, T1, Sber, MTS) **не имеет аналога $45B оценки**. Это значит:

- RU-AI-вендоры **на 1-2 ордера** меньше китайских по capital, что даёт **меньшую compute-капасити**.
- В RU-content нарративе DeepSeek упоминается как «китайский DeepSeek = доступная альтернатива OpenAI» — теперь меняется акцент: «китайский DeepSeek = $50B-вендор с госфондом за спиной, не маленький стартап».

### 4. Контент-hook для GRO-блога

> «DeepSeek поднял оценку с $10B до $45B за раунд. Что это говорит о структуре AI-рынка-2026: Россия как третий полюс или его уже нет?»

Cross-link на [[evolving/industry-trends/ru-vertical-ai-signals-2026]] (если такая есть, иначе создавать).

## Маркетинговое следствие для GRO

- **Анализ конкурентов в content-плане GRO:** DeepSeek — не локальный, а глобальный AI-конкурент за mindshare пользователей и инвестиций. В content-плане упоминается **в категории «новый capital-расклад»** и в нарративе **«не только OpenAI = AI»**.
- **Технологический контекст:** DeepSeek-модели обходятся **дешевле** в API. Для small SaaS-сервисов типа GRO это привлекательный backend-выбор (если будет официальная RU-доступность через aggregator).

## Что мониторить

- **Закрытие раунда** — подтверждение $45B оценки официально.
- **Использование госфонд-капитала** — DeepSeek сделает следующий релиз модели уровня GPT-5? Когда?
- **Регуляторные риски** — US sanctions могут ужесточиться против DeepSeek после государственной связки.
- **Аналогичные раунды у других китайских AI** — Moonshot ($20B), Zhipu, Baichuan.

## Связанные страницы

- [[evolving-strict/competitor-metrics/moonshot-kimi-arr-2026-05]] — параллельный китайский раунд (тот же дайджест)
- [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] — общая таблица AI-валуаций
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий капитал-расклад
- [[evolving/industry-trends/china-ai-manufacturing-momentum-2026]] — китайский AI-momentum
- [[sources/2026-05-14-tg-vcnews-may-5-8-2026]] — первичный сигнал (FT-leak)
- [[sources/2026-05-14-tg-theedinorog-may-2026]] — Reuters supersede $50B (6 мая)

## Contradictions

- **[2026-05-14]** По [[sources/2026-05-14-tg-theedinorog-may-2026]], Reuters $50B (6 мая) supersede FT-leak $45B из [[sources/2026-05-14-tg-vcnews-may-5-8-2026]]. Reuters имеет приоритет как глобальный wire-сервис с deeper sourcing. Resolved.

## TTL

**TTL: 180 дней (до 2026-11-10)** — валюация частной компании, обновляется на следующем раунде или IPO. После Q3 — переоценить, появилась ли публичная цифра.
