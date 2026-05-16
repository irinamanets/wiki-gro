---
id: mkt:evolving-strict/market-data/specialized-video-finetune-cost-anchor-2026-05
title: "Стоимость специализированного видео-финетюна — anchor 2026 (Sulphur-2 Base)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ai, finetune, video-models, cost-benchmark, ltx, anchor]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-cgevent-apr30-may05-2026.md]
namespace: mkt
---

# Specialized video-finetune cost anchor — май 2026

**Sulphur-2 Base** — публичный full-finetune (не lora) **LTX 2.3** с раскрытием бюджета. Используется как **cost anchor** для понимания «сколько стоит сделать специализированный видео-финетюн в 2026».

## Sulphur-2 Base — архитектура и бюджет

Authors: Sulphur AI (Pony-for-SDXL аналогия). Цель — снять цензуру и обучить LTX 2.3 на NSFW-контенте `[conf:high, src:2026-05-05]`.

### Датасет

- **125 000 видеороликов** `[conf:high, src:2026-05-05]`
- Каждый ролик **10 секунд** при **24 fps** `[conf:high, src:2026-05-05]`
- Источник — мульти-источниковый, без аниме/2D (это ухудшает результат) `[conf:high, src:2026-05-05]`

### Стоимость

- **Разметка датасета: $700** `[conf:high, src:2026-05-05]`
- **GPU-аренда (training): $8 000** `[conf:high, src:2026-05-05]`
- **Итого raw direct cost: ~$8 700** (разметка + GPU)
- **Общая стоимость проекта выше** из-за «других расходов» (не раскрыты) `[conf:high, src:2026-05-05]`

### Технический результат

- LTX 2.3 после finetune **умеет в NSFW «гораздо лучше**, чем lora к WAN» `[conf:medium, src:2026-05-05]` (subjective оценка авторов)
- Авторы решили **не делать finetune WAN** (дорого), но планируют **Sulphur-3** `[conf:high, src:2026-05-05]`

Источники:
- [civitai.red/models/2594061/sulphur-2-base](https://civitai.red/models/2594061/sulphur-2-base)
- [huggingface.co/SulphurAI/Sulphur-2-base](https://huggingface.co/SulphurAI/Sulphur-2-base/tree/main)
- [reddit r/StableDiffusion — Sulphur 2 released](https://www.reddit.com/r/StableDiffusion/comments/1t2c9qg/sulphur_2_released/)

## Cost anchor как market-data signal

Это **первый публичный** disclosure full-finetune budget на видео-модели в 2026. Применимость как cost anchor:

| Аспект | Цифра | Source |
|---|---|---|
| Размер датасета | 125 000 × 10 сек × 24 fps | `[conf:high, src:2026-05-05]` |
| Total frames | ~30 млн frames (приблизительно) | derived |
| Разметка | $700 | `[conf:high, src:2026-05-05]` |
| GPU-аренда | $8 000 | `[conf:high, src:2026-05-05]` |
| Direct cost | ~$8 700 | derived |
| Эффективная стоимость per second | ~$0.007 / сек видео | derived |

## Применимость для GRO marketing-нарратива

### Не для прямого маркетинга

Sulphur-2 — NSFW-финетюн, не релевантен GRO для прямого использования или цитирования.

### Релевантно как **disclosure-paradigm** anchor

Этот публичный disclosure — пример **транспарентности cost-budgets**, который перекликается с уже зафиксированной в [[evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format|Нейропрожаркой]] **«культурой раскрытия production-данных»** в русскоязычном AI-сообществе.

Sulphur-2 говорит: «вот наш датасет, вот наши деньги, вот наш результат». Авторы Нейропрожарки говорят: «вот наш бюджет $16, вот ~37 часов работы, вот workflow». **Тот же transparency-паттерн, разные масштабы**.

Применимость для блог-постов GRO `[conf:medium, src:2026-05-05]`: **transparency-контент работает в этой аудитории лучше, чем aspirational** (см. также anti-pattern в neuroprozharka-ai-indie-filmmaking-format).

### Hook для контента

«В 2023 натренировать видео-модель стоило миллионы и команды учёных. В 2026: $700 на разметку + $8 000 на GPU = $8 700, всё. Это меняет game для специализированных вертикалей. И это **вторая часть solo-founder window** ([[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]) — не только использование AI-моделей, но и **их создание под конкретный use-case**». `[conf:high, src:2026-05-05]`

## Связь с другими wiki-страницами

- [[evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format]] — параллельная transparency-культура
- [[evolving/content-trends/ai-video-tools-stack-2026]] — стек, в котором LTX 2.3 — один из компонентов
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — окно, теперь включающее «делать модели», не только «использовать»
- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — общий tracker модель-релизов
- [[sources/2026-05-05-tg-cgevent-apr30-may05-2026]] — источник
