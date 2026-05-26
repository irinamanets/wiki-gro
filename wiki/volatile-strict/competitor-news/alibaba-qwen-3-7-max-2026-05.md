---
id: mkt:volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05
title: "Alibaba Qwen 3.7-Max — китайский frontier для agentic задач (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [alibaba, qwen, china-ai, agent, swe-bench, terminal-bench, frontier-model, closed-weights]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-boris-again-may-19-24-2026.md]
namespace: mkt
---

# Alibaba Qwen 3.7-Max — китайский frontier для agentic задач (май 2026)

**Дата события:** ~2026-05-22 (анонс попал в weekly digest от 24 мая) `[conf:high, src:2026-05-24]`. Зафиксировано в [[sources/2026-05-26-tg-boris-again-may-19-24-2026|@boris_again, пост 3918]].

## Что вышло

Alibaba представила **Qwen 3.7-Max** — флагманскую text-only модель, специально позиционируемую под **длинные агентные задачи** `[conf:high, src:2026-05-24]`.

| Параметр | Значение |
|---|---|
| Контекст | **1M токенов** `[conf:high, src:2026-05-24]` |
| Цена input | $2.50 / 1M токенов `[conf:high, src:2026-05-24]` |
| Цена output | $7.50 / 1M токенов `[conf:high, src:2026-05-24]` |
| SWE-bench Pro | **60.6** (между Opus 4.6 и 4.7) `[conf:high, src:2026-05-24]` |
| Terminal-Bench | **69.7** (лидер) `[conf:high, src:2026-05-24]` |
| Hallucination rate | **~22.9%** (самый низкий среди заявленных) `[conf:high, src:2026-05-24]` |
| Демо | **35 часов автономной работы, 1158 вызовов инструментов** `[conf:high, src:2026-05-24]` |
| Веса | **Закрытые** (Plus-версия мультимодальная — позже с открытыми весами) `[conf:high, src:2026-05-24]` |
| Доступ | Alibaba Cloud, OpenRouter `[conf:high, src:2026-05-24]` |

## Что значит «между Opus 4.6 и 4.7»

SWE-bench Pro 60.6 — это **прямое попадание во frontier-сегмент** на coding tasks. Для контекста:
- Anthropic Claude Opus 4.6 — ~58–59 на SWE-bench Pro (предыдущий публичный референс)
- Claude Opus 4.7 — ~62–64 (текущий лидер)
- Qwen 3.7-Max — **60.6**, то есть **в середине промежутка**

Terminal-Bench 69.7 (лидер) — Qwen **обгоняет** Claude Code и Codex по умению работать в terminal-окружении. Это **первый случай, когда китайский лаб обгоняет US-фронтир на конкретном benchmark'е, релевантном для production agentic stack'а**.

## 35 часов и 1158 вызовов инструментов — что это значит

В демо-сценарии Qwen 3.7-Max выполнял задачу **35 часов автономно**, сделав **1158 tool calls**. Для сравнения:
- Claude Code типичная сессия — несколько часов, 50–300 tool calls
- Anthropic Mythos Preview production-attestation Firefox bugs — ~1 месяц на 271 уязвимость (см. [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]])

То есть Qwen демонстрирует **отдельный режим работы — long-horizon autonomous agent**, не «interactive copilot». Это важно для рынка: open до сих пор не было фронтирной модели, специально оптимизированной под этот режим.

## Что значит для рынка

### 1. Конец нарратива «китайские модели — только для research / open-source»

До Qwen 3.7-Max доминировал нарратив «китайские лабы делают open weights, US делает закрытый frontier». DeepSeek V3-Pro/V4-Pro были open и фронтирными, но **не позиционировались под agentic workloads с tool use**. Qwen 3.7-Max меняет это **двумя ходами одновременно**:

- Закрытые веса (как US фронтир) — Alibaba монетизирует через Cloud API, а не через open release.
- Acentic-first benchmarks (Terminal-Bench лидер, SWE-bench Pro между Opus 4.6 и 4.7) — Qwen теперь **конкурент Claude Code/Codex**, не «open-source альтернатива GPT-4».

Контр-нарратив «Qwen для research, US для production» больше не работает `[conf:high, src:2026-05-24]`.

### 2. Hallucination rate 22.9% — не «низкий», а «опубликованный» [conf:low, src:2026-05-26]

22.9% выглядит как «много», но **раньше эту метрику просто не публиковали в спецификациях**. Alibaba делает рискованный шаг: вместо общих лозунгов «надёжный для агентных задач» — конкретное число с benchmark-методологией. Это **PR-маркер открытости**, который повышает доверие к остальным заявленным цифрам. [conf:low, src:2026-05-26]

### 3. Pricing $2.50/$7.50 — стратегический срез

Qwen 3.7-Max дороже Gemini 3.5 Flash ($1.50/$9 вход, выход дороже у Gemini), но **дешевле Claude Sonnet** ($3/$15) — то есть Alibaba прицеливается на **«китайский Sonnet»** позицию: близко по цене и качеству, но с лучшим Terminal-Bench и 1M контекстом.

### 4. Plus-версия с открытыми весами — позже

Anonces заявил, что **Plus-версия (мультимодальная) будет позже с открытыми весами** `[conf:high, src:2026-05-24]`. То есть Alibaba играет в split: **flagship text-only закрыт, multimodal Plus откроют**. Это инверсия Gemini-стратегии (multimodal закрыт, text открыт через AI Studio).

## Почему это важно для GRO

1. **Готовый «китайский Sonnet» альтернатива** для agentic workloads. Если GRO зависит от Anthropic, появление Qwen 3.7-Max — это **vendor diversification option** на похожей цене с лучшим Terminal-Bench. Минусы: latency из RU/EU (китайский cloud), compliance вопросы, политический риск.
2. **Контент-hook**: *«Китайские модели больше не "research only". Что значит Qwen 3.7-Max между Opus 4.6 и 4.7 для российского AI-стартапа»*. **Сильный заголовок** для блога GRO.
3. **Подсвечивает frontier-overflow**: первый раз за 12 месяцев у нас **5 серьёзных claimants на SWE-bench top-3** одновременно (Opus 4.7, Qwen 3.7-Max, GPT-5.5, Gemini 3.5 Pro в июне, возможно Mythos). Это **сигнал стабилизации frontier'а** — gap между лидерами схлопывается.

## Связанные страницы

- [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — первоисточник (пост 3918)
- [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]] — параллельный конкурент по mid-tier
- [[volatile-strict/competitor-news/deepseek-v4-pro-price-cut-2026-05]] — другой китайский ход той же недели
- [[evolving/industry-trends/china-ai-manufacturing-momentum-2026]] — общий нарратив китайского AI-momentum'а
- [[evolving-strict/competitor-metrics/artificial-analysis-coding-agent-index-2026-05]] — Coding Agent Index (Qwen 3.7-Max ожидаемо войдёт)
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий нарратив гонки
