---
id: mkt:volatile-strict/competitor-news/google-gemini-3-5-flash-2026-05
title: "Google Gemini 3.5 Flash — релиз, +3× pricing, агентность (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [ai, google, gemini, model-release, pricing, agentic, competitor-news]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-06-01  # +vcnews 18-20 мая: second-source attestation I/O 2026 day-1 (vc.ru/ai/2938255, 61451) + Gemini Omni Flash multimodal-video (61452) + day-1 recap AI Ultra/Spark/Pics (61455) + Gemini Omni как «лучшая для редактирования видео» (61466)
sources: [sources/2026-05-26-tg-ai-newz-may-19-25-2026.md, sources/2026-06-01-tg-vcnews-may-18-20-2026.md]
namespace: mkt
---

# Google Gemini 3.5 Flash — релиз и pricing-сдвиг (19 мая 2026)

**Дата сигнала:** 2026-05-19 (пост 4583 в [[sources/2026-05-26-tg-ai-newz-may-19-25-2026|@ai_newz]] + официальная бенчмарк-таблица DeepMind в media 4583) `[conf:high, src:2026-05-19]`.

## Что произошло

Google DeepMind выпустил **Gemini 3.5 Flash** — апдейт «дешёвой» Flash-линейки `[conf:high, src:2026-05-19]`. По пересказу @ai_newz, модель «**заметно сильнее, чем Gemini 3.1 Pro**», но с **удвоением-утроением цены за токены** `[conf:high, src:2026-05-19]`.

## Pricing-сдвиг

| Модель | Input | Output | Δ vs prev |
|---|---|---|---|
| Gemini 3 Flash (старая) | $0.50/1M | $3.00/1M | baseline `[conf:high, src:2026-05-19]` |
| **Gemini 3.5 Flash (новая)** | **$1.50/1M** | **$9.00/1M** | **+200%** input, **+200%** output `[conf:high, src:2026-05-19]` |
| Gemini 3.1 Pro (для сравнения, <200k context) | $2.00/1M | $12.00/1M | reference `[conf:medium, src:2026-05-19]` |

**Read of shift:**

1. **Flash больше не «дешёвая модель»** — Flash-3.5 теперь стоит **в 3 раза больше, чем Flash-3**, и почти **75% от цены Pro** ($1.5 vs $2 input). [conf:low, src:2026-05-26]
2. **«Дешёвый» сегмент сжимается** — на рынке остаются два полюса: фронтир (Claude Opus 4.7, GPT-5.5, Gemini 3.1 Pro по $2-3/$15-30) и open-weight (DeepSeek V4 $0.14-1.74/$0.28-3.48, Kimi K2.6 $0.95/$4). **Middle vanishing**: Flash была middle, теперь сместилась к frontier по цене. [conf:low, src:2026-05-26]
3. **Real cost per task** — открытый вопрос: автор @ai_newz отмечает «насколько реально выросла стоимость за задачу по сравнению с прошлой Flash мы узнаем только с тестами» `[conf:high, src:2026-05-19]`. Если 3.5 Flash в 3× умнее на токен → effective cost сравним. Если только в 1.5× умнее → реальное удорожание ×2.

## Технические возможности

**Главный focus** — agentic capabilities. Google «серьёзно отнёсся к проблемам в агентности и особенно прокачал модель в этом» `[conf:high, src:2026-05-19]`.

**Showcase use-case:** Gemini 3.5 Flash **за 12 часов написала небольшую операционную систему, которая может запустить Doom** `[conf:high, src:2026-05-19]`. Это **демо-формула**: «model + 12h continuous run → working software product» — следующая ступень после «Claude переписывает Bun с Zig на Rust за 10 дней» (см. [[volatile-strict/industry-news/anthropic-bun-rust-rewrite-2026-05]]).

**Pro модель** существует, но в публичном доступе пока нет — обещают «в следующем месяце» (≈ июнь 2026) `[conf:medium, src:2026-05-19]`. Цена Pro **прогнозируется как ещё более agressive** (по author-suggestion @ai_newz).

## Benchmarks (картинка 4583 — официальная таблица DeepMind)

Источник: [deepmind.google/models/evals-methodology/gemini-3-5-flash](https://deepmind.google/models/evals-methodology/gemini-3-5-flash/) (привязка по URL в нижней части картинки). Сравниваются **6 моделей в 14 бенчмарках**.

### Сравнительная таблица (выборочно)

| Бенчмарк | Gemini 3.5 Flash | Gemini 3 Flash | Gemini 3.1 Pro | Claude Sonnet 4.6 | Claude Opus 4.7 | GPT-5.5 | Source |
|---|---|---|---|---|---|---|---|
| Terminal-bench 2.1 | 76.2% | 58.0% | 70.3% | — | 66.1% | **78.2%** | `[conf:high, src:2026-05-19]` |
| SWE-Bench Pro Public | 55.1% | 49.6% | 54.2% | — | **64.3%** | 58.6% | `[conf:high, src:2026-05-19]` |
| MCP Atlas | **83.6%** | 62.0% | 78.2% | 69.5% | 79.1% | 75.3% | `[conf:high, src:2026-05-19]` |
| Toolathlon | **56.5%** | 49.4% | — | — | — | 55.6% | `[conf:high, src:2026-05-19]` |
| OSWorld-Verified | 78.4% | 65.1% | 76.2% | 72.5% | 78.0% | **78.7%** | `[conf:high, src:2026-05-19]` |
| Finance Agent v2 | **57.9%** | 42.6% | 43.0% | 51.0% | 51.5% | 51.8% | `[conf:high, src:2026-05-19]` |
| GDPval-AA (Elo) | 1656 | 1204 | 1314 | 1676 | 1753 | **1769** | `[conf:high, src:2026-05-19]` |
| CharXiv Reasoning | **84.2%** | 80.3% | 83.3% | 72.4% | 82.1% | 84.1% | `[conf:high, src:2026-05-19]` |
| MMMU-Pro | **83.6%** | 81.2% | 80.5% | 74.5% | 75.2% | 81.2% | `[conf:high, src:2026-05-19]` |
| Blueprint-Bench 2 | 33.6% | 0.0% | 26.5% | 6.7% | 24.5% | **36.2%** | `[conf:high, src:2026-05-19]` |
| MRCR v2 8-needle (128k avg) | 77.3% | 67.2% | 84.9% | 84.9% | 59.3% | **94.8%** | `[conf:high, src:2026-05-19]` |
| MRCR v2 1M pointwise | **26.6%** | 22.1% | 26.3% | — | — | — | `[conf:high, src:2026-05-19]` |
| Humanity's Last Exam | 40.2% | 33.7% | 44.4% | 33.2% | **46.9%** | 41.4% | `[conf:high, src:2026-05-19]` |
| ARC-AGI-2 | 72.1% | 33.6% | 77.1% | 58.3% | 75.8% | **84.6%** | `[conf:high, src:2026-05-19]` |

**Где Gemini 3.5 Flash лидер (5 из 14):** MCP Atlas, Toolathlon, Finance Agent v2, CharXiv Reasoning, MMMU-Pro, MRCR v2 1M pointwise. **Сильные стороны: agentic workflows + multimodal + long-context (но только 1M pointwise; в short-context retrieval уступает GPT-5.5)**.

**Где Gemini 3.5 Flash отстаёт:** Reasoning (Humanity's Last Exam уступает Opus 4.7 на 6.7 п.п.), Coding (SWE-Bench Pro уступает Opus 4.7 на 9.2 п.п.), Long-context 128k retrieval (уступает GPT-5.5 на 17.5 п.п.).

### Маркетинговая интерпретация таблицы (Google angle)

**Google положительно позиционирует 3.5 Flash именно против Opus 4.7 и GPT-5.5** — то есть **через лидерство в 5 бенчмарках Google продаёт идею «дешёвая модель = frontier-equivalent для agentic-tasks»**. Это **oправдывает +3× pricing**: «вы платите за **frontier-уровень в agentic**, не за **базовую модель**».

**Counter-arguments конкурентов:** Reasoning + coding (Opus 4.7 лидер), agentic spatial (GPT-5.5 лидер), short-context retrieval (GPT-5.5 +17.5 п.п.). Поэтому в **B2B-сегментах с reasoning-emphasis** (юриспруденция, finance, медицина, deep code-review) **Opus 4.7 остаётся выбором**, а Gemini 3.5 Flash оптимальна для **agentic workflows + multimodal**.

## Что это значит для рынка

**1. Pricing-trend reversal.** Период «модели дешевеют каждый квартал» (LLM-token-pricing-deflation, см. [[evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026]]) **прерывается на Gemini 3.5 Flash**. Это **первый крупный релиз 2026 года, в котором цена выросла, а не упала**.

**2. Vendor-сегментация по use-case.**
- Gemini 3.5 Flash → **agentic workflows** (MCP, tools, finance-agents), **multimodal-heavy** контент.
- Claude Opus 4.7 → **deep reasoning**, **coding** (SWE-Bench Pro), **academic** (Humanity's Last Exam).
- GPT-5.5 → **long-context retrieval** (MRCR 128k), **abstract reasoning** (ARC-AGI-2), **UI control** (OSWorld).

**3. Demo-формула.** Релиз 3.5 Flash подкреплён «модель собирает ОС за 12 часов» — это **новый стандарт agentic-anchor demo**. Ожидание: Pro релиз будет с ещё более экстремальным demo (full-game за 24ч? full-app suite?).

## Маркетинговое значение для GRO

**Для контент-команды:**
- **Hook «Gemini Flash подорожала в 3 раза»** — viral-friendly заголовок для постов про «эра дешёвых моделей закончилась» / «AI-инструменты больше не lite-utility, а frontier-grade». Связка с тезисом из [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|mar-apr digest]] про «token-cost деленные надвое каждые 6 мес» — Gemini 3.5 Flash как **anti-trend signal**.
- **Сравнение «MCP Atlas 83.6%» как frontier-показатель** для постов про AI-агенты в B2B-маркетинге. Если GRO позиционируется как AI-обучение для команд, новый стандарт «83% MCP success» — relevant benchmark. [conf:low, src:2026-05-26]
- **Demo «ОС за 12 часов» — copy-template hook**: «За 12 часов команда из 1 AI собрала продукт, на который раньше уходил квартал». Visceral для маркетинговой воронки про productivity-gains.

**Для нарратива рынка:**
- Связка с [[evolving/industry-trends/ai-corporate-race-mar-may-2026]]: каждый вендор движется к unified-multimodal-frontier. Gemini Omni (см. [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]]) → теперь 3.5 Flash как ranged-multimodal-baseline (CharXiv 84.2%, MMMU-Pro 83.6%). **Google консолидирует визуальную модель Gemini под одним брендом**. [conf:low, src:2026-05-26]

## Второй source-attestation — vc.ru I/O 2026 day-1 (61451/61452/61455/61466)

[[sources/2026-06-01-tg-vcnews-may-18-20-2026|@vcnews 18–20 мая]] фиксирует официальные I/O-анонсы Google из mainstream-источника `[conf:high, src:2026-05-19]`:

- **Gemini 3.5 Flash** (пост 61451, vc.ru/ai/2938255) — Google называет её «самой мощной моделью для агентов и кодирования», уже доступна всем пользователям; **Gemini 3.5 Pro** тестируют внутри, релиз планируют на **июнь 2026** `[conf:high, src:2026-05-19]`. Подтверждает focus на agentic + сроки Pro, ранее зафиксированные через @ai_newz.
- **Gemini Omni Flash** (пост 61452) — мультимодальная модель для генерации видео из любых данных (картинки, аудио, схемы, ролики), создание аватара по фото+голосу; доступна по подписке в Gemini и Flow `[conf:high, src:2026-05-19]`.
- **I/O day-1 recap** (пост 61455, vc.ru/ai/2938226) — главные анонсы: обновлённая подписка **AI Ultra**, модели **Gemini Omni** и **Gemini 3.5 Flash**, персональный ИИ-агент **Gemini Spark**, обновление поиска, инструмент **Google Pics** `[conf:high, src:2026-05-19]`.
- **Gemini Omni для видео** (пост 61466) — в соцсетях названа «лучшей моделью для редактирования видео» (спецэффекты, смена погоды/антуража), «работает как Nano Banana, но с роликами» `[conf:medium, src:2026-05-20]`.

**Что добавляет:** vc.ru — независимое подтверждение официального I/O 2026, плюс Gemini Spark (24/7 personal agent) и Google Pics — анонсы, дополняющие 3.5 Flash в общей I/O-волне. Усиливает тезис «Google закрывает agent-gap» из [[evolving/industry-trends/ai-corporate-race-mar-may-2026]].

## Связанные страницы

- [[sources/2026-05-26-tg-ai-newz-may-19-25-2026]] — первоисточник
- [[sources/2026-06-01-tg-vcnews-may-18-20-2026]] — второй source-attestation I/O 2026 (vc.ru, посты 61451/61452/61455/61466)
- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — main release-tracker, добавлен add-on про 3.5 Flash
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] — параллельный Google-anchor (Gemini Omni unified)
- [[evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026]] — pricing trend (anti-signal)
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — макротренд гонки
- [[volatile-strict/competitor-news/cursor-composer-2-5-2026-05]] — параллельный pricing-up (Composer fast mode ×2)
