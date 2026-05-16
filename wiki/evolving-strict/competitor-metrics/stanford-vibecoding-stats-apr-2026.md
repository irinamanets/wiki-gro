---
id: mkt:evolving-strict/competitor-metrics/stanford-vibecoding-stats-apr-2026
title: "Stanford vibecoding-study — численные метрики (янв–апр 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [ai-agents, vibecoding, security, benchmarks, claude-code]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-products-and-startups-may-2026.md]
namespace: mkt
---

# Stanford vibecoding-study — численные метрики (янв–апр 2026)

Канонические числа из Stanford-исследования вайбкодинга (`arxiv 2604.20779`), пересказанные Байрамом Аннаковым ([[sources/2026-05-14-tg-products-and-startups-may-2026]] пост 1740, attached/1740 — TL;DR slide). Методологический контекст и интерпретация — в [[canon/marketing-frameworks/vibecoding-stanford-study-2026]].

Это `evolving-strict` потому, что цифры — конкретные snapshot-метрики янв–апр 2026, которые будут пересматриваться при следующих пейперах того же типа (Stanford, BigCode, Anthropic own studies, и т.д.). Каждая метрика — с inline `[conf:*, src:*]`.

## Параметры датасета

- Сессий: **6 000** `[conf:high, src:2026-05-06]`
- Промптов: **63 000** `[conf:high, src:2026-05-06]`
- Тулколлов: **355 000** `[conf:high, src:2026-05-06]`
- Период сбора: январь–апрель 2026 `[conf:high, src:2026-05-06]`
- Источники сессий: Claude Code (большинство, Opus 4.6), OpenCode, Gemini, Factory `[conf:high, src:2026-05-06]`

## Распределение use cases (RQ1, Sec. 3.1)

| Use case | Доля | Source |
|---|---|---|
| Code understanding | 19% | `[conf:high, src:2026-05-06]` |
| Git operations | 14% | `[conf:high, src:2026-05-06]` |
| Create new code | 13% | `[conf:high, src:2026-05-06]` |
| Debug | 13% | `[conf:high, src:2026-05-06]` |
| Refactor | 9% | `[conf:high, src:2026-05-06]` |
| Other | 32% | `[conf:high, src:2026-05-06]` |

**Tool calls breakdown:**
- bash — **33%** `[conf:high, src:2026-05-06]`
- read/edit/search files — **48%** `[conf:high, src:2026-05-06]`
- остальное — ~19% `[conf:high, src:2026-05-06]`

## Vibecoding distribution (RQ1, Sec. 3.2)

| Режим работы | Доля сессий | Source |
|---|---|---|
| Чистый вайбкодинг (агент пишет >99% кода) | **41%** | `[conf:high, src:2026-05-06]` |
| Чистый human | **23%** | `[conf:high, src:2026-05-06]` |
| Hybrid | ~36% | `[conf:high, src:2026-05-06]` |

## AI-code survival rate (RQ2, Sec. 4.2)

| Режим | Survival до коммита | Source |
|---|---|---|
| Коллаборация | **44%** | `[conf:high, src:2026-05-06]` |
| Чистый вайбкодинг | **59%** | `[conf:high, src:2026-05-06]` |

**Code waste decomposition** (для коллаборации):
- ~**10%** агент сам же переписывает `[conf:high, src:2026-05-06]`
- ~**46%** юзер удаляет/переписывает руками `[conf:high, src:2026-05-06]`

## Vulnerability rate (RQ2, Sec. 4.3) — главная метрика

На 1 000 строк введённого кода:

| Режим | Vulnerabilities / 1K LOC | Кратность | Source |
|---|---|---|---|
| Человек ручками | **0.08** | 1× (baseline) | `[conf:high, src:2026-05-06]` |
| Человек + агент в коллабе | **0.14** | ~1.8× | `[conf:high, src:2026-05-06]` |
| Чистый вайбкодинг | **0.76** | **~9.5×** | `[conf:high, src:2026-05-06]` |

Конкретный пример уязвимости из пейпера: `subprocess.run(cmd, shell=True)` — **CWE-78** (command injection) `[conf:high, src:2026-05-06]`.

**Caveat:** Stanford использовал Semgrep — pattern-based, может давать false positives `[conf:high, src:2026-05-06]`. Бай: «9× надо читать как грубый порядок, направление и величина — реальные».

## Pricing (RQ2, Sec. 4.3)

Median $ / 100 committed lines:

| Режим | $/100 LOC | Source |
|---|---|---|
| Human-only | **$0.07** | `[conf:high, src:2026-05-06]` |
| Collaborative | **$0.05** | `[conf:high, src:2026-05-06]` |
| Vibe coding | **$0.13** | `[conf:high, src:2026-05-06]` |

Vibe coding **в 2.6× дороже коллаборации** `[conf:high, src:2026-05-06]`.

## Session success and failure (RQ2, Sec. 4.1)

- Average session success rate: **82%** `[conf:high, src:2026-05-06]`
- Fail-сценарии: юзер прерывает; системная ошибка блокирует агента `[conf:high, src:2026-05-06]`

## User behavior (RQ1, Sec. 3.3)

| Тип юзера | Доля | Source |
|---|---|---|
| Expert Nitpicker | **40%** | `[conf:high, src:2026-05-06]` |
| Vague Requester | **33%** | `[conf:high, src:2026-05-06]` |
| Other | **20%** | `[conf:high, src:2026-05-06]` |
| Mind Changer | **7%** | `[conf:high, src:2026-05-06]` |

## Agent stop / interruption / pushback (RQ2, Sec. 4.4)

Per turn:

| Событие | Доля turns | Source |
|---|---|---|
| Agent stop (агент сам остановился задать вопрос) | **1%** | `[conf:high, src:2026-05-06]` |
| User interruption | **5%** | `[conf:high, src:2026-05-06]` |
| User pushback | **41%** | `[conf:high, src:2026-05-06]` |

## Связь с другими страницами

- [[canon/marketing-frameworks/vibecoding-stanford-study-2026]] — методологическая рамка, интерпретация
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — Stanford-цифры как proof-point раздела про швейцарский сыр и Plan Mode
- [[evolving-strict/competitor-metrics/zapier-automation-bench-2026]] — соседний benchmark (другой класс задач, но та же логика «AI лучше людей не везде»)
- [[evolving-strict/market-data/ai-coding-tools-cost-explosion-2026]] — связанные cost-данные
- [[evolving/content-trends/ai-product-engineer-content-hooks]] — где эти цифры превращаются в контент-хуки

## Источники

- [[sources/2026-05-14-tg-products-and-startups-may-2026]] — пост 1740, attached/1740 TL;DR slide
- arxiv.org/abs/2604.20779 — оригинальный пейпер
