---
id: mkt:volatile-strict/competitor-news/seedance-2-1-pricing-2026-05
title: "Seedance 2.1 и 2.0 Mini — анонс upcoming релизов (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [seedance, bytedance, ai-video, pricing, model-release]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-cgevent-may19-25-2026.md]
namespace: mkt
---

# Seedance 2.1 и 2.0 Mini — upcoming релиз

**Дата сигнала:** 2026-05-19 (пост 15700 в [[sources/2026-05-26-tg-cgevent-may19-25-2026|@cgevent]]). `[conf:medium, src:2026-05-19]`

## Что анонсировано

| Модель | Что изменится | Ожидаемая цена | Source |
|---|---|---|---|
| **Seedance 2.1** | Качество генерации **+~20%** vs Seedance 2.0 | Не объявлено | `[conf:low, src:2026-05-19]` |
| **Seedance 2.0 Mini** | Облегчённая версия, **работает лучше, чем Seedance 2.0 Fast** | **~$0.073 / сек** | `[conf:medium, src:2026-05-19]` |

Текущая Seedance 2.0 — **$0.03 / сек** (см. [[evolving/content-trends/ai-video-tools-stack-2026|AI-video-tools stack]]) `[conf:medium, src:2026-04-03]`. То есть Mini-версия дороже базовой, но позиционируется как «лучше чем Fast» — видимо, новое промежуточное звено в линейке.

## Почему это важно

### 1. Seedance продолжает удерживать ценовое лидерство

Даже Mini за $0.073/сек = **в ~3× дешевле Runway Gen-4.5** при средне-сопоставимом качестве `[conf:medium, src:2026-04-03]`. Бюджетный AI-video pipeline (Kumar & Solo paradigm) сохраняет Seedance как умолчание.

### 2. Линейка дробится — но не в counter-направлении Google

Google консолидируется (Gemini Omni поглощает Veo) `[conf:high, src:2026-05-20]` — см. [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]]. ByteDance/Seedance — наоборот **дробит линейку** (2.0 → 2.0 Fast → 2.0 Mini → 2.1) под разные tier'ы цены/качества. Это два противоположных bet'a на структуру рынка:

- **Google bet:** одна большая модель, разные планы по compute
- **ByteDance bet:** много специализированных моделей под разные ценовые точки

Параллель с OpenAI (GPT-5/Sora/GPT Image 2 — отдельные продукты, см. [[volatile-strict/competitor-news/openai-gpt55-launch-2026-04]]).

### 3. Frontier shifts — но не обязательно перепозиционирование стека

+20% качества Seedance 2.0 → 2.1 — это incremental, не breakthrough. Не похоже на смену лидера рынка по качеству; Seedance остаётся **бюджетным выбором с @-системой и `[cut]` фичей** (см. [[evolving/content-trends/ai-video-tools-stack-2026]]). [conf:low, src:2026-05-26]

## Контекст рынка

Параллельные релизы той же недели:
- **20 мая:** [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05|Gemini Omni Flash]] (Google I/O) — multimodal-layering edit
- **22 мая:** [[volatile-strict/competitor-news/runway-aleph-2-video-2026-05|Runway Aleph 2]] — frame-edit propagation
- **25 мая:** [[volatile-strict/competitor-news/bytedance-vcube-video-upscaler-2026-05|ByteDance vCube upscaler]] — параллельный продукт от ByteDance

ByteDance, по-видимому, отвечает на конкурентное давление двумя ходами: **upscaler как дополнение** к Seedance (доводит 480p/720p/1080p выход модели до 2K/4K) + **новые tier'ы цены/качества** через Seedance 2.1 / 2.0 Mini.

## Почему это важно для GRO

1. **Обновление [[evolving/content-trends/ai-video-tools-stack-2026|AI-video-tools stack]]** — добавить Seedance 2.0 Mini как промежуточный tier между Fast и Pro.
2. **Hook для контент-команды:** *«Битва за tier-2 AI-видео: кому достанется $0.07/сек ниша между бюджетной Hailuo и premium Seedance 2.0»* — narrative-frame для разбора стека.
3. **Recurring-hook про Seedance.** Канал [[sources/2026-04-14-tg-solokumi-nov2025-apr2026|@solokumi]] (Kumar & Solo) — ключевой voice по Seedance в RU-комьюнити. Стоит мониторить их пост-релизные обзоры.

## Связанные страницы

- [[evolving/content-trends/ai-video-tools-stack-2026]] — AI-video-tools stack (нужен update Seedance 2.0 Mini)
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] — параллельный релиз Google
- [[volatile-strict/competitor-news/runway-aleph-2-video-2026-05]] — параллельный релиз Runway
- [[volatile-strict/competitor-news/bytedance-vcube-video-upscaler-2026-05]] — параллельный продукт ByteDance
- [[sources/2026-05-26-tg-cgevent-may19-25-2026]] — первоисточник
