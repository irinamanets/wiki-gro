---
id: mkt:volatile-strict/competitor-news/xai-grok-4-3-release-2026-05
title: "xAI Grok 4.3 — релиз и OpenRouter pricing $1.25/$2.50 (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [xai, grok, llm, openrouter, pricing, deflation, awareness]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-bezsmuzi-may-5-7.md]
namespace: mkt
---

# xAI Grok 4.3 — релиз на OpenRouter (май 2026)

Кульгин в @bezsmuzi пост 15860 (2026-05-05) сообщает о выходе Grok 4.3. Модель доступна на OpenRouter, цены: **$1.25 за 1M input токенов, $2.50 за 1M output**. «Бенчмарки лучше многих» (без конкретных чисел). См. [[sources/2026-05-14-tg-bezsmuzi-may-5-7]].

**Почему `volatile-strict`:** релиз новой модели — discrete news event, pricing — точная цифра, requires inline-маркеров.

## Pricing snapshot

| Модель | Input ($/1M) | Output ($/1M) | Платформа | Source |
|---|---|---|---|---|
| Grok 4.3 | $1.25 | $2.50 | OpenRouter | `[conf:medium, src:2026-05-05]` |

OpenRouter URL: https://openrouter.ai/x-ai/grok-4.3

## Контекст — где это в pricing-кривой

Сопоставим с anchor-точками из [[evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026|Горный deflation table]]:

| Модель | $/1M output | Position |
|---|---|---|
| GPT-4o (baseline 2025) | $10 | premium-tier 2025 |
| GPT 5.4-mini | ~$4 | mid-tier 2026 |
| **Grok 4.3** | **$2.50** | **mid-tier 2026** |
| Deepseek V4 Flash | ~$0.25 | low-cost frontier 2026 |

Grok 4.3 встаёт **между GPT 5.4-mini и DeepSeek** — это **mid-cost / frontier-quality** позиционирование. Для xAI это **первая модель** с агрессивно-низким OpenRouter pricing (предыдущие Grok'и были в premium-tier).

## Сигнал для рынка

- **xAI ценовая дисциплина** — раньше Grok был «забавная игрушка для X-юзеров», сейчас xAI начинает биться **на developer-сегмент** через OpenRouter и pricing. `[conf:medium, src:2026-05-05]`
- **OpenRouter как primary distribution** — xAI **не** мажет цены на собственном API endpoint, а пушит через aggregator. Это сигнализирует, что Grok ищет нишу в **multi-model workflow** (когда developer переключается между моделями по задаче).
- **«Бенчмарки лучше многих»** — без конкретики, Кульгин не приводит цифры. `confidence: low` для quality claims, `medium` для pricing facts.

## Связь с предыдущими signals

- **Grok DAU −23% Q1 2026** ([[evolving-strict/competitor-metrics/llm-web-traffic-2026-04]]) — Grok падает на mobile, но визиты +75% YoY за счёт X-веб. 4.3 — потенциальный try-to-revert. [conf:low, src:2026-05-14]
- **OpenAI market share visits 77% → 56%** ([[sources/2026-05-14-tg-bezsmuzi-may-5-7]]) — рынок открывается для челленджеров; Grok 4.3 — один из них. [conf:low, src:2026-05-14]

## Маркетинговые выводы для GRO

1. **Если в стеке используется multi-model gateway** — добавить Grok 4.3 в test-pool для price-performance comparison. $2.50/M output — competitive с GPT-5.4-mini.
2. **Контент-хук:** «Grok 4.3 вышел — за полцены от Opus, и доступен через OpenRouter. Это четвёртый игрок в `mid-cost frontier` нише за квартал. Что это значит для economics стартапа?»

## TTL и план верификации

- **TTL: 90 дней** (до 2026-08-14). Pricing моделей переписывается каждые 60-90 дней, через квартал — re-verify через OpenRouter / xAI публичный pricing.
- **Контр-сигнал:** если xAI вводит rate-limits или поднимает цены — записать supersession.

## Связанные страницы

- [[evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026]] — общая кривая pricing deflation
- [[evolving-strict/competitor-metrics/llm-web-traffic-2026-04]] — позиция Grok в audience-метриках
- [[volatile-strict/competitor-news/openai-gpt-5-5-every-review-2026-05]] — конкурент в mid-tier
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — рамка рынка
- [[sources/2026-05-14-tg-bezsmuzi-may-5-7]] — первоисточник, пост 15860
