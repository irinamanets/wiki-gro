---
id: mkt:volatile-strict/competitor-news/cursor-composer-2-5-2026-05
title: "Cursor Composer 2.5 — релиз, удвоение цены fast mode, тренинг в SpaceXAI (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [ai, cursor, composer, spacexai, coding, pricing, competitor]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-ai-newz-may-14-19-2026.md]
namespace: mkt
---

# Cursor Composer 2.5 — релиз и pricing-сдвиг (19 мая 2026)

**Дата сигнала:** 2026-05-19 (пост 4580 в [[sources/2026-05-19-tg-ai-newz-may-14-19-2026|@ai_newz]], со ссылкой на блогпост cursor.com/blog/composer-2-5) `[conf:medium, src:2026-05-19]`.

## Что произошло

Cursor выпустил **Composer 2.5** — coding-модель на той же базе **K2.5**, что и предыдущая версия `[conf:medium, src:2026-05-19]`.

- Количество синтетических тренировочных тасков увеличили **в 25×** `[conf:medium, src:2026-05-19]`.
- Это **первая модель Cursor, натренированная в датацентрах SpaceXAI** `[conf:medium, src:2026-05-19]`.
- Cursor и SpaceXAI уже **совместно тренируют заметно большую модель**, используя **в 10× больше компьюта** `[conf:medium, src:2026-05-19]`.
- По пересказу @ai_newz, от результатов этой большой модели **зависит, выкупит ли SpaceX компанию Cursor** `[conf:low, src:2026-05-19]` (авторская трактовка, не verified).

## Pricing-сдвиг

- **Fast mode** (включён по умолчанию) подорожал **в 2×** — теперь **$3 / $15 за миллион токенов** (input/output), что равно стоимости Sonnet `[conf:medium, src:2026-05-19]`.
- **Обычный режим** не изменился — **$0,5 / $2,5 за миллион токенов** `[conf:medium, src:2026-05-19]`.

## Бенчмарки (из media 4580)

| Bench | Composer 2.5 | Opus 4.7 | GPT-5.5 | Composer 2 | Source |
|---|---|---|---|---|---|
| Terminal-Bench 2.0 | 69,3% | 69,4% | 82,7% | 61,7% | `[conf:medium, src:2026-05-19]` |
| SWE-Bench Multilingual | 79,8% | 80,5% | 77,8% | 73,7% | `[conf:medium, src:2026-05-19]` |
| CursorBench v3.1 (harder) | 63,2% | 64,8% (max) | 64,3% (xhigh) | 52,2% | `[conf:medium, src:2026-05-19]` |

Caveat на самом слайде Cursor: Opus 4.7 и GPT-5.5 показаны по **self-reported scores** для public evals `[conf:medium, src:2026-05-19]`. Composer 2.5 заметно прибавил относительно Composer 2 (например, CursorBench 52,2% → 63,2%), но на Terminal-Bench/SWE-Bench идёт вровень с Opus 4.7 и отстаёт от GPT-5.5 на Terminal-Bench `[conf:medium, src:2026-05-19]`.

## Стратегический контекст

### 1. SpaceXAI-тренинг закрывает апрельскую сделку Cursor

В апреле 2026 уже было раскрыто, что xAI начала сдавать Colossus в аренду, и **Cursor — первый клиент**, тренировавший Composer 2.5 (см. [[volatile-strict/competitor-news/spacexai-rename-2026-05|rebrand xAI → SpaceXAI]] и опцию выкупа Cursor за $60 млрд). Composer 2.5 — **первый публичный продукт, прямо подтверждающий**, что этот compute-deal реализован, не остался на бумаге `[conf:medium, src:2026-05-19]`.

### 2. Pricing вверх на фоне cost-explosion

Удвоение fast-mode (дефолтного) режима — встраивается в нарратив [[evolving-strict/market-data/ai-coding-tools-cost-explosion-2026|токены дороже зарплат]]. Coding-вендоры **поднимают цены**, потому что compute дорожает (см. [[volatile-strict/industry-news/gpu-scarcity-neocloud-anthropic-2026-05|GPU-дефицит]]). Параллель: Anthropic убирал тиры и резал лимиты весной 2026 — Cursor вместо этого **поднял цену дефолтного режима**.

### 3. Compute как фактор M&A

Тезис «от результата большой модели зависит выкуп Cursor» (даже если это авторская трактовка) согласуется с уже зафиксированным паттерном: Маск **готов делать опцион на чужой coding-продукт**, лишь бы загрузить Colossus и продвинуть Grok-в-кодинге `[conf:low, src:2026-05-19]`.

## Почему это важно для GRO

1. **Конкурентный мониторинг AI-tooling.** Cursor — частый референс в нашем трекинге AI-coding-рынка ([[volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1|консолидация]]). Composer 2.5 фиксирует, что Cursor движется от «обёртки над чужими моделями» к **собственной модели на собственном (арендованном) компьюте**.
2. **Pricing-сигнал для контента про экономику AI.** «Дефолтный режим coding-инструмента подорожал в 2× до уровня Sonnet» — конкретный anchor для постов про то, что **дешёвый AI-tooling заканчивается** (контр-нарратив hype).
3. **Не для прямого позиционирования GRO** — это dev-tooling, далёкая от B2C-продуктивности вертикаль. Использовать как **макро-фон темпа индустрии**, не как прямой hook.

## Связанные страницы

- [[volatile-strict/competitor-news/spacexai-rename-2026-05]] — SpaceXAI-rebrand и compute-deal с Cursor
- [[volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05]] — Anthropic как второй клиент Colossus
- [[evolving-strict/market-data/ai-coding-tools-cost-explosion-2026]] — нарратив роста стоимости AI-tooling
- [[volatile-strict/industry-news/gpu-scarcity-neocloud-anthropic-2026-05]] — GPU-дефицит как драйвер pricing
- [[volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05]] — динамика coding-вендоров
- [[sources/2026-05-19-tg-ai-newz-may-14-19-2026]] — первоисточник

## Caveat

@ai_newz — вторичный пересказ блогпоста Cursor; авторская трактовка про M&A-зависимость не подтверждена. Не использовать для пресс-цитат до сверки с cursor.com/blog. Это operational-сигнал для трекинга, не canonical fact.
