---
id: mkt:evolving-strict/competitor-metrics/claude-opus-4-6-release-benchmarks-2026
title: Claude Opus 4.6 — релизные бенчмарки и фичи (май 2026)
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [ai, claude, llm, benchmarks, anthropic]
confidence: medium
stale: false
created: 2026-06-01
updated: 2026-06-01
sources: [sources/2026-06-01-condense-vcru-molyanov-may-2026.md, sources/2026-06-01-vc-ru-molyanov-2723945-novaya-versiya-claude-opus-4-6-uluchsheniya.md, sources/2026-06-01-vc-ru-molyanov-2723951-chatgpt-5-3-codex-protiv-opus.md]
namespace: mkt
---

# Claude Opus 4.6 — релизные бенчмарки и фичи (май 2026)

Срез характеристик Claude Opus 4.6 и сравнение с ChatGPT 5.3 Codex, как их описал Павел Молянов (verified expert) в своём блоге. Нужен marketing-memory как ориентир по возможностям LLM-инструментов, которыми располагают маркетологи и контент-команды — особенно для контента GRO про AI-практики. Strict-слой: все числа с inline-маркерами. Источник один (self-reported retelling релиза) → `confidence: medium`.

## Бенчмарки и характеристики Opus 4.6

| Параметр | Значение | Source |
|---|---|---|
| Контекстное окно | 1 млн токенов (было 250к) | `[conf:medium, src:2026-05-01]` |
| Максимальный вывод | до 128к токенов | `[conf:medium, src:2026-05-01]` |
| Long-context retrieval @256к | 93% (у Sonnet 4.5 было 11%) | `[conf:medium, src:2026-05-01]` |
| Long-context retrieval @1млн | 75% (у Sonnet 4.5 было 19%) | `[conf:medium, src:2026-05-01]` |
| SWE Bench Verified | на долю процента ХУЖЕ устаревшего Opus 4.5 | `[conf:medium, src:2026-05-01]` |

**Прочтение:** скачок retrieval (11%→93% на 256к) — главный практический выигрыш для длинных документов/баз знаний; регресс на SWE Bench против 4.5 показывает, что версии не монотонно улучшаются по всем осям `[conf:medium, src:2026-05-01]`.

## Новые фичи

- **Adaptive thinking** — 4 уровня размышлений: low / medium / high / max (раньше только вкл/выкл) `[conf:medium, src:2026-05-01]`.
- **Compaction по API** — модель сама сжимает контекст и делает саммари диалога; можно прописать правила суммаризации `[conf:medium, src:2026-05-01]`.
- **Agent Team в Claude Code** — субагенты внутри пачки общаются между собой и проверяют друг друга (раньше отчёты обрабатывал только основной агент) `[conf:medium, src:2026-05-01]`.
- **Delegate mode (Shift+Tab)** — основной агент не редактирует файлы / не пишет код / не выполняет команды, только создаёт субагентов `[conf:medium, src:2026-05-01]`.

## Сравнение с ChatGPT 5.3 Codex

- ChatGPT 5.3 Codex вышел следом за новым Opus и по бенчмаркам «ещё лучше» нового Opus `[conf:medium, src:2026-05-01]`.
- В своём боте Молянов проверял паттерны Claude Code на Claude Opus 4.8 (упоминание ещё более актуальной версии) `[conf:low, src:2026-05-01]`.

## Маркетинговые выводы

- Рост контекста до 1М + Agent Team напрямую усиливают агент-связки в контент-продакшене (см. [[evolving/content-trends/molyanov-ai-content-automation-patterns]]) — длинные ТЗ и базы знаний помещаются в один проход.
- Версии LLM меняются ежемесячно и не строго вверх — для контента GRO это аргумент против «вечных» сравнений моделей; данные стареют за недели (потому evolving-strict, не canon).

## Связанные страницы
- [[sources/2026-06-01-condense-vcru-molyanov-may-2026]]
- [[evolving/content-trends/molyanov-ai-content-automation-patterns]]
- [[canon/marketing-frameworks/llm-task-spec-decomposition-molyanov]]
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]]
- [[evolving-strict/competitor-metrics/artificial-analysis-coding-agent-index-2026-05]]
