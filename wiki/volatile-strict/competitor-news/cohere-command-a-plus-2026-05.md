---
id: mkt:volatile-strict/competitor-news/cohere-command-a-plus-2026-05
title: "Cohere Command A+ — первый открытый фронтир Cohere с нативными source-citations (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [cohere, command-a-plus, moe, open-weights, multilingual, rag, source-citations, hugging-face]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-boris-again-may-19-24-2026.md]
namespace: mkt
---

# Cohere Command A+ — первый открытый фронтир Cohere (май 2026)

**Дата события:** ~2026-05-22 (попал в weekly digest 24 мая) `[conf:high, src:2026-05-24]`. Зафиксировано в [[sources/2026-05-26-tg-boris-again-may-19-24-2026|@boris_again, пост 3918]].

## Что вышло

Cohere выпустила **Command A+** — первая **открытая** фронтирная модель компании `[conf:high, src:2026-05-24]`.

| Параметр | Значение |
|---|---|
| Архитектура | **218B MoE (25B активных)** `[conf:high, src:2026-05-24]` |
| Языки | **48** `[conf:high, src:2026-05-24]` |
| Объединяет | Command A / Reasoning / Vision / Translate (4 прежние модели) `[conf:high, src:2026-05-24]` |
| Особенность | **Нативные ссылки на источники в ответах** `[conf:high, src:2026-05-24]` |
| Веса | **Открытые** (HuggingFace, w4a4 quantization) `[conf:high, src:2026-05-24]` |
| Лицензия | (не уточнена в дайджесте) |

## Что отличает Command A+ от других open-source frontier-моделей

### 1. Native source-citations — built-in RAG primitive

Самый важный архитектурный выбор Cohere — **модель умеет цитировать источники нативно**, без post-hoc citation-injection в промпте. Это значит:
- Меньше hallucinations на RAG-задачах (caveat: precision не публикована)
- Структурный output для downstream-обработки (citation = first-class output token, не free-text reference)
- **Прямой match с регуляторными требованиями ЕС** (EU AI Act провенанс) и потребностями enterprise-RAG

Это **дифференциация на product-design уровне**, не на benchmark'ах. Cohere позиционирует себя как «open frontier model для enterprise RAG», в отличие от Qwen («open frontier для agentic», см. [[volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05]]) или DeepSeek («open frontier для cost-efficiency»).

### 2. MoE 218B → 25B активных

Это **«сжатый Mistral Large» подход**: общая капасити большая, но активная часть умеренная, что снижает inference cost. Сравнение:
- Mixtral 8x22B: 141B total, 39B active
- DeepSeek V3-Pro: 671B total, 37B active
- Cohere Command A+: 218B total, 25B active
- Qwen3.7-Max: closed weights (для контекста)

Command A+ — **самая «эффективная»** на оси active/total ratio среди open MoE (≈11.5%). Это даёт хороший inference на single high-end GPU. [conf:low, src:2026-05-26]

### 3. 48 языков — multilingual-first

Cohere исторически фокусируется на enterprise + non-English markets (acquired by Oracle's RAG pipeline). 48 языков — это **stronger multilingual coverage чем Qwen (30+) и DeepSeek (20+)**. Релевантно для **российского рынка**: если поддержка русского качественная, это open-source альтернатива закрытым моделям для GRO-content генерации.

## Что значит для рынка

### 1. Cohere возвращается в публичное обсуждение

После hype 2023 года вокруг Cohere (когда они были фронтиром в enterprise-RAG) компания **тихо ушла с радара публичного AI-discourse** — фокус сместился на B2B-контракты. Command A+ — это **попытка вернуться в open-source discourse**, чтобы перехватить mindshare developers, которые сегодня делятся между Qwen / DeepSeek / Mistral.

### 2. «Open frontier» становится фрагментированным

К маю 2026 у нас **четыре отчётливо позиционированных open frontier игрока**:

| Игрок | Дифференциация |
|---|---|
| DeepSeek V4-Pro | cost-efficiency (см. [[volatile-strict/competitor-news/deepseek-v4-pro-price-cut-2026-05]]) |
| Qwen 3.7-Max (Plus версия позже) | agentic / Terminal-Bench |
| Cohere Command A+ | RAG / source-citations / multilingual |
| Mistral Large 3+ (анонсирован, не вышел) | EU-compliance / sovereign AI |

То есть open frontier **больше не пытается обыграть closed на общих benchmarks** — каждый берёт свою product-niche. Это **зрелость рынка**.

### 3. Source-citations как новая architectural feature

После Command A+ ожидаем, что **другие игроки тоже сделают citations нативно** (Anthropic уже делает в Claude через `<citation>` tags, но не на модельном уровне). Это **тренд года** — структурный output становится first-class.

## Почему это важно для GRO

1. **Открытый RAG-стек для content-team**. Если GRO делает блог-контент через AI с цитированием источников, Command A+ — это **продакшен-готовая open модель** с правильным architectural fit. Особенно интересен 48 языков (русский должен работать качественно).
2. **Контент-hook**: *«Cohere вернулась с открытым фронтиром — что значит native source-citations для AI-контента в RAG-эпоху»*.
3. **Связь с GEO/AEO**: native citations в ответе модели = **прямой match с GEO-инфраструктурой** (которую LLM сами всё чаще цитируют). См. [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]].

## Связанные страницы

- [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — первоисточник (пост 3918)
- [[volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05]] — параллельный закрытый китайский frontier
- [[volatile-strict/competitor-news/deepseek-v4-pro-price-cut-2026-05]] — другой open-источник той же недели
- [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]] — закрытый mid-tier с похожей ценой
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — native citations и GEO-инфраструктура
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий нарратив гонки
