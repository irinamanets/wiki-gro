---
id: mkt:evolving-strict/competitor-metrics/artificial-analysis-coding-agent-index-2026-05
title: "Artificial Analysis Coding Agent Index — лидерборд агентных систем (май 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [artificial-analysis, leaderboard, claude-code, codex, cursor, gemini-cli, agentic-systems, benchmark]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-boris-again-may-19-24-2026.md]
namespace: mkt
---

# Artificial Analysis Coding Agent Index — лидерборд агентных систем (май 2026)

**Дата публикации:** ~2026-05-23 (запуск Артифика в weekly digest 24 мая) `[conf:high, src:2026-05-23]`. Зафиксировано в [[sources/2026-05-26-tg-boris-again-may-19-24-2026|@boris_again, пост 3918]]. URL: [artificialanalysis.ai/agents/coding-agents](https://artificialanalysis.ai/agents/coding-agents).

## Что вышло

[Artificial Analysis](https://artificialanalysis.ai) — независимый бенчмарк-провайдер для LLM (de-facto «Speedtest для AI») — запустил **новый лидерборд для агентных систем** (не моделей, а целых систем «модель + инструменты + scaffolding») `[conf:high, src:2026-05-23]`.

## Стартовые цифры

| Система | Score (Coding Agent Index) | Source |
|---|---|---|
| Claude Code | **66** | `[conf:high, src:2026-05-23]` |
| OpenAI Codex | **65** | `[conf:high, src:2026-05-23]` |
| Cursor Composer 2.5 | **62** | `[conf:high, src:2026-05-23]` |
| Gemini CLI | **43** | `[conf:high, src:2026-05-23]` |

## Что значит «индекс агентных систем» vs модельные бенчмарки

Это **категориальный shift** в индустриальной оценке:

- **Старая логика (до 2026):** бенчмаркали отдельные модели на отдельных задачах (SWE-bench, HumanEval, MBPP). Это давало рейтинги моделей: Claude Opus 4.7, GPT-5, Gemini 3 Pro и т. п.
- **Новая логика (AA Coding Agent Index):** бенчмаркаются **системы из связки модели + scaffolding + memory + tool-calling pattern**. Claude Code != Claude Opus — это **обвязка** вокруг модели с системными промптами, retrieval, code-execution, persistence.

То есть AA-index измеряет **продуктовую систему целиком**, не модель. Это критически важно: разработчики выбирают **систему**, не модель.

## Распределение результатов

- **Claude Code 66 / Codex 65 / Cursor 62** — кластер около верха, всё в пределах 6%. Различение между ними **не статистически значимо** на этом уровне точности — в практике все три «одинаково хорошие». [conf:low, src:2026-05-26]
- **Gemini CLI 43** — заметно отстаёт (на 33% слабее Claude Code). Это **серьёзный негативный знак** для Google Spark/Gemini agent stack'а, который только-только выпустили (см. [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]]). [conf:low, src:2026-05-26]

## Что значит для рынка

### 1. «Coding agent» = устаканившаяся product category

Запуск отдельного benchmark'а — это **подтверждение категории**. До 2026 года «AI coding assistant» был размыт между Copilot, ChatGPT, Cursor, Tabnine. После AA-index есть **чёткие 4 контендера** в категории «autonomous coding agent» (не «autocomplete»).

### 2. Claude Code лидирует по чуть-чуть, но **лидирует**

Anthropic с Claude Code захватывает leader-status в новой категории. Параллельно с тем, что Anthropic режет ресурсы Claude Code из-за compute crunch'а (см. [[evolving/industry-trends/ai-marketing-limits-2026]]) — то есть **спрос обгоняет supply**. Это **«hot product»** ситуация.

### 3. Gemini CLI отстаёт — Google нужен ответ

Gemini Spark (см. [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]]) — это попытка Google построить **competing agent stack**. AA-index показывает, что **Gemini CLI пока не дотягивает**, а Spark ориентирован на consumer, не coding. **Стратегический gap у Google**.

### 4. Cursor Composer 2.5 — **выживший indie**

Cursor — единственный из топ-3, кто **не принадлежит frontier-лабе** (Anthropic / OpenAI). Composer 2.5 на 62 — это сильное достижение для **standalone-IDE команды**. Cursor доказывает, что **product-design layer выше модели** даёт competitive advantage. Это **прямой пример для GRO** — vertical-сервис на чужой модели может конкурировать с native-сервисами вендоров.

## Что значит для GRO как content-сервиса

### 1. GRO content-team-stack пересматривается

Если GRO использует AI для редактуры / генерации / транскрипции, то **Claude Code и Codex** — это **верхний tier для coding-task'ов** (хотя GRO не пишет код напрямую, многие операции близки к code-like — структурирование данных, генерация JSON-схем, etc.). **Cursor Composer** как third option — для команды, которая хочет один tool на разработку и контент-операции.

### 2. AA-index как готовый контент-формат

Periodical-обновление AA Coding Agent Index — это **отличный контент-формат для GRO блога**: «Что изменилось в Q3 2026?», «Кто обогнал кого?», «Что значит для вашей команды?». **Готовый serial-content** по образцу «AI рейтингов» в IT-блогах.

### 3. Связь с METR survey

Combined с [[evolving-strict/market-data/metr-ai-productivity-self-vs-measured-2026-05]] получается **двусторонняя картина**:
- AA-index говорит: **какой agent сильнее** (объективно)
- METR survey говорит: **насколько использование agent'а помогает** (объективно vs perceived)

Это **готовый контент-блок «Реалистичная оценка AI coding tools на май 2026»** для CFO/CTO-аудитории GRO-блога.

## Почему это важно для GRO

1. **Решение про content-team AI-stack** теперь основано на benchmark'е, не на vendor-marketing'е. Claude Code / Codex — рекомендуемые. Gemini CLI — рано.
2. **Готовый контент-format** для блога: AA-index как «periodic чекпоинт» индустрии.
3. **Cursor success story** для GRO positioning: «vertical-команда на чужой модели может побеждать native-сервисы вендора» — прямой кейс для GRO как **vertical productivity-stack'а** vs Google Workspace / Microsoft 365.

## Связанные страницы

- [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — первоисточник (пост 3918)
- [[evolving-strict/market-data/metr-ai-productivity-self-vs-measured-2026-05]] — productivity reality-check (как использовать эти agents'ы конвертируется в реальный gain)
- [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]] — Gemini Spark/CLI как response Google
- [[volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05]] — Qwen 3.7-Max ожидаемо войдёт в следующий update
- [[evolving/industry-trends/ai-marketing-limits-2026]] — связанный нарратив про границы AI-маркетинга
- [[evolving/competitor-positioning/openclaw-vs-hermes-agent-tools-2026]] — продуктовая категория «autonomous agent»
- [[evolving/industry-trends/agent-first-world-openclaw-2026]] — общий нарратив agent-first world
