---
id: mkt:evolving-strict/competitor-metrics/featherless-funding-2026
title: Featherless — финансовые метрики (май 2026)
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [featherless, ai-infrastructure, llm-api, subscription-pricing, huggingface, funding, openrouter-alternative, usa]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-startupoftheday-may-20-26-2026.md]
namespace: mkt
---

# Featherless — финансовые метрики (май 2026)

Американский AI-инфраструктурный стартап, AI-API gateway по подписке. Извлечено из поста 5077 [@startupoftheday](https://t.me/startupoftheday) от 2026-05-22 (см. [[sources/2026-05-26-tg-startupoftheday-may-20-26-2026]]).

Сайт: [featherless.ai](https://featherless.ai/).

## Продукт и pricing

| Показатель | Значение | Source |
|---|---|---|
| Каталог моделей (на момент мая 2026) | 30 000 нейросетей | `[conf:high, src:2026-05-22]` |
| Тип pricing | Подписка (subscription), а не metered | `[conf:high, src:2026-05-22]` |
| Минимальный тариф | $10 / месяц | `[conf:high, src:2026-05-22]` |
| Цена за токены сверх лимита | $0 (бесплатно в рамках подписки) | `[conf:high, src:2026-05-22]` |
| Anti-abuse механизм | Лимит параллельных запросов | `[conf:high, src:2026-05-22]` |
| Включает популярные модели | Deepseek, Qwen (явно упомянуты Горным) | `[conf:high, src:2026-05-22]` |

Сравнение с конкурентами (контекстуальное, не из источника):
- OpenRouter — metered pricing, **dollarized per-token**
- Together / Replicate — metered + reserved capacity
- HuggingFace Inference Endpoints — metered (на дед-капасити)

Featherless — **первый mainstream AI-API gateway с flat subscription** в массовом сегменте `[conf:medium, src:2026-05-22]`.

## Funding

| Показатель | Значение | Source |
|---|---|---|
| Объём последнего раунда (май 2026) | $20 млн | `[conf:high, src:2026-05-22]` |
| Стадия | Не указана прямо (контекстно — Series A/B) | `[conf:low, src:2026-05-22]` |
| Локация | США | `[conf:high, src:2026-05-22]` |

## Market signal — раунд как валидация модели

$20M на subscription-AI-API-инфраструктуру в мае 2026 — это **сигнал инвестиционного признания pricing-модели**. Раньше venture-доминировала metered-модель (OpenRouter, Together), сейчас фонды дают капитал на flat-subscription альтернативу.

Это **early-stage market validation** концепции «**API по подписке выгоднее metered для vibecoder-сегмента**» — см. [[canon/marketing-frameworks/api-subscription-vs-metered-pricing-featherless-gorny]].

## Маркетинговая интерпретация

### 1. Pricing-anchor для AI-SaaS

$10/мес становится **psychological anchor** для AI-API подписок на 2026-2027 годы. Любой новый player в сегменте «AI-инфраструктура для SMB» будет calibrate'ить свой entry-level tier к этой точке:

- **Ниже $10/мес** — freemium-стратегия (бесплатно + paid features)
- **$10-30/мес** — мейнстрим individual / SMB tier
- **$50-150/мес** — pro tier с премиум-фичами
- **$500+/мес** — team / SMB business tier
- **Enterprise** — custom (metered + commit)

### 2. OpenRouter блокировка RU-доступа делает RU-альтернативу заметнее

В контексте упомянутого в [[sources/2026-05-19-tg-neuraldvig-may-13-19-2026]] факта, что OpenRouter блокирует RU-доступ к американским LLM-API, рынок открыт для **аналога Featherless с RU-friendly access**. Это competitive opportunity для российских AI-инфра-стартапов (GigaChat, YandexGPT, Cloud.ru/Selectel inference) — но требует **именно подписочной модели**, не metered.

### 3. Урок для GRO subscription positioning

Хотя GRO не AI-API gateway, **pricing-психология subscription** валидируется featherless-метриками: clients принимают subscription охотнее, чем metered, если стоимость подписки попадает в «фоновую трату» psychological zone. GRO с тарифом 2 490 ₽/мес попадает в этот «не считаемый» диапазон для **большинства целевых сегментов** (вершиной customer trust survey будет, что 2 490 ₽ не воспринимается как «крупная покупка»). [conf:low, src:2026-05-26]

## Связанные страницы

- [[canon/marketing-frameworks/api-subscription-vs-metered-pricing-featherless-gorny]] — фреймворк, который опирается на эти метрики
- [[evolving/industry-trends/ai-marketing-limits-2026]] — общий AI-фон
- [[sources/2026-05-19-tg-neuraldvig-may-13-19-2026]] — OpenRouter RU-блок context
- [[evolving-strict/competitor-metrics/anthropic-spacex-colossus-rental-2026-05]] — соседний AI-инфра сигнал
- [[sources/2026-05-26-tg-startupoftheday-may-20-26-2026]]

## Источник

Александр Горный, пост 5077 [@startupoftheday](https://t.me/startupoftheday) от 2026-05-22 `[conf:high, src:2026-05-22]`.
