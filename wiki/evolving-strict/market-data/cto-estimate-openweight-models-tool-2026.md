---
id: mkt:evolving-strict/market-data/cto-estimate-openweight-models-tool-2026
title: "CTO-estimate — агрегатор open-weight моделей и снимок рейтинга (май 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ai, open-weight, llm, benchmarks, tools, self-hosting]
confidence: medium
stale: false
created: 2026-05-30
updated: 2026-05-30
sources: [sources/2026-05-30-tg-cgevent-may-25-29-2026.md]
namespace: mkt
---

# CTO-estimate — агрегатор open-weight моделей (май 2026)

Бесплатный инструмент [cto-estimate.openweights.space](https://cto-estimate.openweights.space/), сделанный подписчиком @cgevent (Алексей). Зафиксировано через [@cgevent](https://t.me/cgevent) пост 15785, 2026-05-29.

## Что это

Агрегатор данных по open-weight моделям в одном месте: бенчмарки **Artificial Analysis** + конфиги моделей с **Hugging Face**. Назначение — для тех, кто работает с локальными LLM или следит за open-weight ландшафтом.

**Функциональность:**
- Каталог open-weight моделей
- Фильтры: размер, модальность, context length, reasoning, лицензия
- Рейтинги на основе бенчмарков
- Сравнение моделей бок о бок
- Детали архитектуры и параметров
- Ежедневные обновления списка
- Практический раздел: первичная оценка требований к GPU и экономики собственного сервера (Self-hosted LLM / GPU Calculator / Server ROI Calculator)

## Снимок рейтинга Intelligence (composite Artificial Analysis), 2026-05-29

Топ open-weight моделей по composite Intelligence-score (vision-снято из UI-вложения 15785):

| Модель | Intelligence | Source |
|---|---|---|
| Kimi K2.6 (Moonshot, 1600B) | 54 | `[conf:medium, src:2026-05-29]` |
| MiMo-V2.5-Pro (Xiaomi) | 54 | `[conf:medium, src:2026-05-29]` |
| DeepSeek V4 Pro (Reasoning) | 52 | `[conf:medium, src:2026-05-29]` |
| GLM-5.1 (Reasoning, Zhipu) | 51 | `[conf:medium, src:2026-05-29]` |
| GLM-5 (Reasoning) | 50 | `[conf:medium, src:2026-05-29]` |
| MiniMax-M2.7 | 50 | `[conf:medium, src:2026-05-29]` |
| MiMo-V2.5 | 49 | `[conf:medium, src:2026-05-29]` |
| Kimi K2.5 | 47 | `[conf:medium, src:2026-05-29]` |
| DeepSeek V4 FL | 47 | `[conf:medium, src:2026-05-29]` |

**Карточка DeepSeek V4 Pro (Reasoning, Max Effort)** `[conf:medium, src:2026-05-29]`:
- Параметры: **1600B total / 49B active (MoE)** `[conf:medium, src:2026-05-29]`
- Context: **1M** `[conf:medium, src:2026-05-29]`
- Speed: **30 t/s** `[conf:medium, src:2026-05-29]`
- GPQA **89.0%**, SciCode **50.0%**, IFBench **76.0%**, Omniscience **43.0%** `[conf:medium, src:2026-05-29]`

Все числа — из UI агрегатора (вторичные данные Artificial Analysis), не независимый замер → `confidence: medium`.

## Релевантность для marketing-memory

- **Сигнал зрелости open-weight ландшафта.** Топ open-weight моделей — **китайские** (Kimi/Moonshot, MiMo/Xiaomi, DeepSeek, GLM/Zhipu, MiniMax) `[conf:medium, src:2026-05-29]`. Подтверждает [[evolving/industry-trends/ai-corporate-race-mar-may-2026|тренд агентного китайского frontier]] на open-weight стороне.
- **Self-hosting экономика выходит в инструментальный слой.** Появление GPU/ROI-калькулятора как продукта — сигнал, что **локальный запуск LLM становится массовой практической задачей**, а не нишей. Связано с [[evolving/industry-trends/on-device-ai-quantization-2026]] и [[evolving/content-trends/ai-tools-self-hosting-arbitrage]].
- **Content-hook:** «топ-10 опенсорс-моделей — все китайские, и их можно крутить локально» — узнаваемый hook про доступность/независимость стека.

## TTL и checkpoint
Evolving-strict TTL 180 дней (hard re-verify), но данные дрейфуют **ежедневно** (инструмент обновляется каждый день) — рейтинг устаревает быстрее формального TTL. Перепроверять при следующем @cgevent/AI-дампе.

## Связанные страницы
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — китайский frontier и гонка моделей
- [[evolving/industry-trends/on-device-ai-quantization-2026]] — локальный запуск и квантизация
- [[evolving/content-trends/ai-video-tools-stack-2026]] — параллельный open-weight image/video стек
