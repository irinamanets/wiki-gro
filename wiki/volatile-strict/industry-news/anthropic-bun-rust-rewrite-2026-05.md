---
id: mkt:volatile-strict/industry-news/anthropic-bun-rust-rewrite-2026-05
title: "Bun переписан с Zig на Rust за 10 дней с Claude — proof-point AI-assisted разработки (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [ai, anthropic, claude, bun, rust, ai-assisted-dev, proof-point]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-ai-newz-may-14-19-2026.md]
namespace: mkt
---

# Bun: Zig → Rust за 10 дней с Claude (май 2026)

**Дата сигнала:** 2026-05-14 (пост 4572 в [[sources/2026-05-19-tg-ai-newz-may-14-19-2026|@ai_newz]], со ссылкой на GitHub PR #30412) `[conf:medium, src:2026-05-14]`.

## Что произошло

JavaScript-рантайм **Bun** (компанию-разработчика oven-sh в конце 2025 купил Anthropic) **переписали с языка Zig на Rust** `[conf:medium, src:2026-05-14]`. У лид-разработчика (Jarred Sumner), при помощи **Claude** (вероятно модель Mythos), на это ушло **10 дней с первого коммита** `[conf:medium, src:2026-05-14]`.

Структура кода осталась той же — по сути это **тот же код на другом языке** (механический, но огромный по объёму порт). Скрин PR (media 4572): «Rewrite Bun in Rust #30412» **Merged**, **6755 коммитов** в `main` из ветки `claude/phase-a-po...` `[conf:medium, src:2026-05-14]` — префикс ветки `claude/` прямо указывает на AI-assisted процесс.

## Динамика (за процессом наблюдали публично)

- Первый коммит попал на главную **Hacker News** `[conf:medium, src:2026-05-14]`.
- Изначально разработчик написал, что ветка **экспериментальная**, а Rust-код, вероятно, выкинут `[conf:medium, src:2026-05-14]`.
- Через **пару дней** Rust-версия проходила **99,8% тестов** Bun `[conf:medium, src:2026-05-14]` — и «на помойку» отправилась уже **оригинальная Zig-версия**.
- Статус Rust-версии — **Canary**, заменит Zig в следующем релизе `[conf:medium, src:2026-05-14]`.
- Причина миграции — **нестабильность Bun**, в т.ч. баги с памятью. У Rust-версии **нет регрессий по скорости**, местами даже быстрее `[conf:medium, src:2026-05-14]`.

## Почему это важно для GRO

Не как технический факт (язык рантайма далёк от маркетинга), а как **proof-point зрелости AI-assisted разработки** — конкретный, верифицируемый, публичный кейс:

1. **Anchor «AI делает то, что раньше = месяцы команды».** Полный порт production-рантайма за 10 дней силами одного человека + Claude — это сильная иллюстрация скачка производительности `[conf:medium, src:2026-05-14]`. Применимо в контенте про [[evolving/industry-trends/ai-productivity-j-curve-2026|AI-производительность]] и [[evolving/industry-trends/ai-solopreneurship-window-2026-2029|окно соло-фаундера]].
2. **Contrast-hook к «нейрослоп».** Распространённый контр-аргумент «AI генерит мусор» (см. [[evolving/content-trends/plastic-ai-content-pushback-hook]]) уравновешивается тем, что в structured-задачах (механический порт со 100% тестовым покрытием) AI выдаёт production-результат. Полезно как **balanced framing**: AI силён там, где есть чёткий критерий проверки. [conf:low, src:2026-05-19]
3. **Anthropic-as-actor.** Anthropic не только продаёт Claude, но и **использует его на собственном dogfood-продукте** (Bun) — это messaging-паттерн «вендор ест свою еду», который стоит распознавать у конкурентов.
4. **Не для прямого позиционирования GRO** — dev-tooling-вертикаль. Использовать как **proof-point в постах про AI-производительность**, не как продуктовый hook.

## Связанные страницы

- [[evolving/industry-trends/ai-productivity-j-curve-2026]] — скачок производительности (Bun-порт = anchor-кейс)
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — один человек + AI делает работу команды
- [[evolving/content-trends/plastic-ai-content-pushback-hook]] — контр-нарратив «нейрослоп», который этот кейс балансирует
- [[evolving-strict/market-data/ai-coding-tools-cost-explosion-2026]] — экономика AI-coding (обратная сторона: дорого)
- [[volatile-strict/competitor-news/cursor-composer-2-5-2026-05]] — параллельная динамика coding-моделей
- [[sources/2026-05-19-tg-ai-newz-may-14-19-2026]] — первоисточник

## Caveat

@ai_newz — вторичный пересказ; «вероятно Mythos» — догадка автора о модели, не факт. PR-факты (99,8% тестов, 10 дней, 6755 коммитов) верифицируемы по github.com/oven-sh/bun/pull/30412 — при использовании в контенте сослаться на PR напрямую. Operational-сигнал для трекинга, не canonical fact до сверки. [conf:low, src:2026-05-19]

## TTL

**TTL: 90 дней (до 2026-08-17)** — переоценить, вышла ли Rust-версия в стабильный релиз и закрепился ли AI-assisted-порт как репрезентативный кейс производительности.
