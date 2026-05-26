---
id: mkt:volatile-strict/competitor-news/deepseek-v4-pro-price-cut-2026-05
title: "DeepSeek V4-Pro подешевела в 4 раза навсегда (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [deepseek, v4-pro, china-ai, pricing, open-weights, cost-efficiency]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-boris-again-may-19-24-2026.md]
namespace: mkt
---

# DeepSeek V4-Pro подешевела в 4 раза навсегда (май 2026)

**Дата события:** ~2026-05-22 (попал в weekly digest 24 мая) `[conf:high, src:2026-05-24]`. Зафиксировано в [[sources/2026-05-26-tg-boris-again-may-19-24-2026|@boris_again, пост 3918]].

## Что произошло

DeepSeek **резко снизила цены** на V4-Pro **навсегда**:

| Параметр | Старая цена | Новая цена | Изменение |
|---|---|---|---|
| Input / 1M токенов | ~$1.74 | **$0.435** | **−75%** `[conf:high, src:2026-05-24]` |
| Output / 1M токенов | ~$3.48 | **$0.87** | **−75%** `[conf:high, src:2026-05-24]` |

То есть API стал в **4 раза дешевле**, и это **постоянная цена** (не временная промо-акция) `[conf:high, src:2026-05-24]`.

## Что это значит

### 1. Самая дешёвая frontier модель на рынке

При $0.435/$0.87 DeepSeek V4-Pro **дешевле всех актуальных mid-tier**:
- Gemini 3.5 Flash — $1.50/$9 (см. [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]])
- Qwen 3.7-Max — $2.50/$7.50 (см. [[volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05]])
- Claude Haiku — ~$1/$5
- GPT-4o-mini — ~$0.15/$0.60 (близко на input, но output дороже)

DeepSeek V4-Pro теперь — **самый дешёвый «frontier-class» API на рынке**.

### 2. Ценовое сжатие mid-tier с двух сторон в одну неделю

В неделю 18–24 мая мы наблюдали:
- **Сверху**: Gemini 3.5 Flash «спустил» frontier-качество в mid-tier за $1.50/$9
- **Снизу**: DeepSeek режет цены в 4× до $0.435/$0.87

Это **двусторонний squeeze** для всех остальных mid-tier игроков (GPT-4o-mini, Claude Haiku, Mistral, Gemini Flash 2.x). В течение 6–12 месяцев ждём ответных ценовых ходов от OpenAI и Anthropic.

### 3. «Навсегда» как маркетинговый ход

Слово **«навсегда»** в анонсе — это сильный позиционирующий signal. Обычно AI-компании режут цены временно (price-war промо), потому что compute capex меняется. DeepSeek заявляет permanent reduction → демонстрирует **уверенность в собственной cost structure** (использует домашние GPU + дешёвую инференс-инфру в Китае).

### 4. Стратегический контекст

DeepSeek позиционирует себя как **«AWS S3» из мира моделей** — дешевизна как product-feature, а не price-promo. Это **отличается от Qwen** (frontier-positioning) и **от Anthropic** (premium-positioning). Триполярный рынок:

| Позиция | Игрок | Тезис |
|---|---|---|
| Premium | Anthropic (Sonnet/Opus/Mythos) | «лучшее качество, цена не первое» |
| Frontier-open | Qwen 3.7-Max, Cohere Command A+ | «фронтир + специализация (agentic / RAG)» |
| Cost-floor | DeepSeek V4-Pro | «самое дешёвое frontier-API на рынке» |

## Почему это важно для GRO

1. **Bulk content generation становится в 4 раза дешевле**. Для GRO как content-сервиса это **прямой cost-impact** — если переключить часть pipeline (синонимы, regenerate variants, классификация) на V4-Pro, мощность остаётся frontier-уровневой, а cost падает в 3–10× vs Sonnet baseline.
2. **Контент-hook**: *«AI стал в 4 раза дешевле за одну неделю — что делать со старыми OPEX-моделями content-team»*. Готовый CFO-friendly блог-пост.
3. **Подсвечивает «AI как commoditizing infrastructure»**. Если frontier-quality можно получить за $0.435/1M токенов, тогда **разница между AI-сервисами больше не в качестве модели, а в продуктовой обвязке** — UX, домен-специфика, integration. Это **прямой usaged GRO positioning** как vertical-инструмент (а не «AI обёртка»).

## Связанные страницы

- [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — первоисточник (пост 3918)
- [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]] — параллельный mid-tier ход той же недели
- [[volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05]] — frontier-open позиция
- [[volatile-strict/competitor-news/cohere-command-a-plus-2026-05]] — frontier-open RAG-позиция
- [[evolving/industry-trends/china-ai-manufacturing-momentum-2026]] — общий китайский нарратив
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий нарратив гонки
