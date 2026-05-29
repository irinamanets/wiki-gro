---
id: mkt:volatile-strict/competitor-news/bytedance-vcube-video-upscaler-2026-05
title: "ByteDance vCube — video upscaler (480p/720p/1080p → 2K/4K, 60fps), май 2026"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [bytedance, vcube, video-upscaler, ai-video, seedance, fal-ai, replicate]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-cgevent-may19-25-2026.md]
namespace: mkt
---

# ByteDance vCube — video upscaler

**Дата сигнала:** 2026-05-25 (пост 15746 в [[sources/2026-05-26-tg-cgevent-may19-25-2026|@cgevent]]). `[conf:high, src:2026-05-25]`

## Что вышло

ByteDance выпустил **vCube** — AI video upscaler. **Никакого опенсорса, только API.** `[conf:high, src:2026-05-25]`

| Параметр | Значение | Source |
|---|---|---|
| Вход | 480p / 720p / 1080p | `[conf:high, src:2026-05-25]` |
| Выход | до **2K** или **4K** | `[conf:high, src:2026-05-25]` |
| Частота кадров | до **60 кадров/сек** | `[conf:high, src:2026-05-25]` |
| Позиционирование | «Идеальное дополнение для Seedance» (от ByteDance) | `[conf:high, src:2026-05-25]` |
| Доступ | API через [Fal.ai](https://fal.ai/models/fal-ai/bytedance-upscaler/upscale/video) или [Replicate](https://replicate.com/bytedance/video-upscaler) | `[conf:high, src:2026-05-25]` |
| Pro mode | **×10 от обычной цены** | `[conf:high, src:2026-05-25]` |

## Pricing (Fal.ai, 30fps)

| Разрешение | Standard ($/сек) | PRO ($/сек) | 60fps Standard | 60fps PRO | Source |
|---|---|---|---|---|---|
| 1080p | $0.0072 | $0.072 | $0.0144 | $0.144 | `[conf:high, src:2026-05-25]` |
| 2K | $0.0144 | $0.144 | $0.0288 | $0.288 | `[conf:high, src:2026-05-25]` |
| 4K | $0.0288 | $0.288 | $0.0576 | $0.576 | `[conf:high, src:2026-05-25]` |

**60fps удваивает цену для любого разрешения. PRO mode в 10 раз дороже обычного.** `[conf:high, src:2026-05-25]`

Есть **пресеты для описания сцены** для более точного попадания в upscale (предположительно, схожий механизм с Krea / Topaz scene-aware upscaling).

На Replicate цены **расписаны более понятно** (по оценке Цыпцына).

## Зачем ByteDance это сделал

vCube — это **дополнение к Seedance**, а не самостоятельный продукт. Логика:

- Seedance 2.0 генерит видео в 720p/1080p, но **не до 4K**
- Для коммерческого/широкоэкранного использования нужен апскейл
- Раньше пайплайн был Seedance → Topaz через Krea ($35/мес) — внешняя зависимость от not-ByteDance тулзы

Теперь **полный pipeline остаётся внутри ByteDance** (Seedance генерация → vCube upscale), плюс монетизация per-second.

Параллельно ByteDance продвигает **новые tier'ы Seedance**: 2.1 (+20% качества), 2.0 Mini ($0.073/сек) — см. [[volatile-strict/competitor-news/seedance-2-1-pricing-2026-05]]. [conf:low, src:2026-05-26]

## Конкурентный ландшафт

| Upscaler | Цена / 1080p | Цена / 4K | Источник | Source |
|---|---|---|---|---|
| **vCube (Standard)** | $0.0072/сек | $0.0288/сек | ByteDance API | `[conf:high, src:2026-05-25]` |
| **Topaz Video через Krea** | $35/мес unlimited | $35/мес unlimited | Krea подписка | `[conf:medium, src:2026-04-14]` |
| **Topaz desktop** | Single-purchase | Single-purchase | Лицензия Topaz | `[conf:medium, src:2026-04-14]` |

vCube — **per-second pricing**, Topaz — **flat-rate subscription**. Break-even для контент-фабрики: при >>$35/мес на vCube (≈4900 сек 1080p = 81 минута материала) Topaz становится выгоднее. Для разовых задач vCube выгоднее.

## Почему это важно для GRO

1. **Tier-3 / Premium pipeline пост-обработка.** Если контент-команда GRO будет делать **высокобюджетные** ролики на YouTube/презентации — vCube заходит как дешёвый per-job апскейлер без подписки на Topaz.
2. **Обновление [[evolving/content-trends/ai-video-tools-stack-2026|AI-video-tools stack]]** — добавить vCube в раздел post-processing, рядом с Topaz Video.
3. **Reusable рамка для контента:** *«AI-video pipeline 2026: 4 уровня инструментов от генерации до апскейла — сколько стоит производить 4K-ролик»* — практичный how-to для блог-поста с конкретными расчётами.

## Связанные страницы

- [[evolving/content-trends/ai-video-tools-stack-2026]] — AI-video-tools stack (добавить vCube в раздел post-processing)
- [[volatile-strict/competitor-news/seedance-2-1-pricing-2026-05]] — параллельный анонс Seedance 2.1 / 2.0 Mini
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] — главный конкурент в video AI
- [[sources/2026-05-26-tg-cgevent-may19-25-2026]] — первоисточник
