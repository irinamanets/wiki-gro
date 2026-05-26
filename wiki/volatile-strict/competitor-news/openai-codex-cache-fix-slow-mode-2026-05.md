---
id: mkt:volatile-strict/competitor-news/openai-codex-cache-fix-slow-mode-2026-05
title: "OpenAI Codex — cache bug fix + reset limits + /slow mode teaser (24 мая 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [ai, openai, codex, operations, ai-coding, competitor-news]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-ai-newz-may-19-25-2026.md]
namespace: mkt
---

# OpenAI Codex — cache bug fix + limits reset + /slow tease (24 мая 2026)

**Дата сигнала:** 2026-05-24 (пост 4588 в [[sources/2026-05-26-tg-ai-newz-may-19-25-2026|@ai_newz]], со скриншотом твита **Tibo Sottiaux** [@thsottiaux] от 23-24 мая) `[conf:high, src:2026-05-24]`.

## Что произошло

OpenAI пофиксил **баг с кэшем в Codex**, из-за которого «**быстро выжирались лимиты**» подписчиков `[conf:high, src:2026-05-24]`. Tibo Sottiaux (OpenAI Codex team) объяснил root cause:

> «Some of you noticed limits drained faster in Codex, we root caused it to an **optimization that we rolled back** that had an impact on cache hit rates when compacting across long running sessions. We fixed this and have now **reset usage limits for all accounts**. Enjoy the weekend.» — @thsottiaux `[conf:high, src:2026-05-24]`

**Действия OpenAI:**

1. **Rolled back** свежую оптимизацию, которая ломала cache hit rates во время компакции долгоживущих сессий `[conf:high, src:2026-05-24]`.
2. **Reset usage limits** для **всех аккаунтов** `[conf:high, src:2026-05-24]` — это **не credit/refund**, а сброс счётчика usage. Хороший UX-pattern: вместо аудита/возмещения, чистый wipe.
3. **Teaser**: `/slow` режим для **несрочных объёмных тасков** `[conf:high, src:2026-05-24]`. По интерпретации @ai_newz, это **direct counter-feature** к Claude Code /goal mode (мульти-агентность + non-stop until goal).

## Авторский комментарий @ai_newz

«Из-за него быстро выжирались лимиты, поэтому их снова ресетнули, **Anthropic тут стоит поучиться**. А ещё Тибо тизерит /slow режим для Codex, что было бы очень круто для несрочных объёмных тасков.» `[conf:medium, src:2026-05-24]`

Это **имплицитная критика Anthropic**. Контекст:
- Claude Pro / Max подписчики неоднократно сообщали о drop'е лимитов при обновлениях Claude Code (см. [[volatile-strict/industry-news/anthropic-bun-rust-rewrite-2026-05]] + general AI-newz threads).
- Anthropic исторически compensates via **token credit increases** (см. [[volatile-strict/competitor-news/anthropic-third-party-credits-2026-06|Anthropic third-party credits до $200]]) — **не reset'ом**, а expansion'ом scope'а.
- OpenAI здесь демонстрирует **alternative operations pattern**: rollback → public transparency → reset → next-feature teaser. Эта последовательность короче (за <72ч) и более прозрачна.

## /slow mode — что это значит

Не задеплоено, но контекст:

- **Codex /slow vs Claude /goal** — обе фичи направлены на **«не блокировать UI, дай модели больше времени»**, но с разным emphasis:
  - **Claude /goal** (см. [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|mar-apr digest]]) — мульти-агентность Claude Code, модель **не останавливается до достижения цели**.
  - **OpenAI /slow** — судя по тизеру, **batch-mode оптимизация**: «возьми эту задачу, у меня нет дедлайна, выполни когда есть свободные ресурсы». Похоже на **OpenAI Batch API** (50% скидка за 24h latency), но интегрировано в Codex UI. [conf:low, src:2026-05-26]
- **Use-case:** мега-рефакторинги, code-review больших codebases, dependency-updates, security-audits — задачи, где «через час или через 6 часов всё равно».

**Маркетинговая релевантность:** continuation [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|Codex vs Claude Code arms-race]]: OpenAI **продолжает расширять Codex** после Chrome plugin (8 мая), Spreadsheets (6 мая), reset-сcss и /slow teaser. **Каждые 2-3 недели — новая Codex-фича**.

## Operational PR-pattern: rollback + transparency + reset

**Эта тройка действий — образцовый ops PR-pattern для AI-vendor'ов в 2026 году.** Compare:

| Действие | Что говорит публике | Risk |
|---|---|---|
| **1. Rollback** | «Мы знаем root cause, не игнорируем» | Признание ошибки |
| **2. Public transparency** (твит, не only support tickets) | «Не прячемся за support» | Может усилить недовольство |
| **3. Reset limits** | «Компенсируем потерю, не вопросы» | Прецедент для будущих ситуаций |
| **4. Tease next feature** (/slow) | «Не просто фиксим, движемся вперёд» | Бесполезно, если feature не выйдет |

**Marketing значение для GRO:** этот pattern переносим. Если GRO-продукт когда-нибудь столкнётся с user-facing глюком (cache bug, training-pipeline downtime), tested template — **rollback → transparency → reset → tease**. Не «извинения + промокод», а **проактивные операционные действия**.

## Связь с трендом «AI coding tooling consolidation»

См. [[volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1]]. Codex + Claude Code занимают всё больше mind-share в developer-segment'е (см. также [[volatile-strict/competitor-news/cursor-composer-2-5-2026-05]] — Cursor пытается удержать позиции через SpaceXAI compute). 

**Сигнал из 4588:** «Codex limits drain faster» означает, что **usage** Codex реально велик — пользователи **долго работают в long-running sessions**, которые ломают cache. Это **косвенно подтверждает growing share** Codex в coding-assistant рынке.

## Маркетинговое значение для GRO

**Для контент-команды:**
- **Hook «Anthropic тут стоит поучиться»** — useful angle для постов про **«как AI-вендоры коммуницируют с пользователями»**. Сравнение OpenAI vs Anthropic ops-style — content-вилка про **transparency в AI**.
- **Anchor-cost-of-use story:** «Limits drain faster, потом reset, потом /slow mode» — visceral нарратив про **«стоимость AI-подписки = volatile, а не fixed»**, который перекликается с [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|tokenizer-overhead caveat Opus 4.7]] (1.0-1.35× больше токенов после tokenizer update).
- **/slow mode как product-design lesson:** «Не каждая задача нужна за 5 секунд. Иногда оптимальный UX — это `я займусь этим, возвращайся завтра`». **Применимо для GRO-копирайтинга**: AI-обучение тоже не должно быть instant, есть value в `slow learning`.

**Для нарратива рынка:**
- Параллельно с GPU scarcity (см. [[volatile-strict/industry-news/gpu-scarcity-neocloud-anthropic-2026-05]]) — **OpenAI compute optimization** становится виден через operational artifacts (cache-bug, /slow mode batch'инг). Это **показатель compute-tightness рынка**: вендоры экономят на каждом cache-hit.

## Связанные страницы

- [[sources/2026-05-26-tg-ai-newz-may-19-25-2026]] — первоисточник
- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — Codex + Claude Code arms race
- [[volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1]] — coding tools macrotrend
- [[volatile-strict/competitor-news/cursor-composer-2-5-2026-05]] — третий игрок (Cursor)
- [[volatile-strict/competitor-news/anthropic-third-party-credits-2026-06]] — Anthropic compensation pattern (контраст)
- [[volatile-strict/industry-news/gpu-scarcity-neocloud-anthropic-2026-05]] — compute-tightness фон
