---
id: mkt:canon/marketing-frameworks/ai-productivity-3-levers-typical
title: "Три рычага AI-операционки — Remove / Compress / Rebuild (TYPICAL, 2026)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai, productivity, automation, framework, operations, self-serve, decision-logs, content-hook]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-typicalcompany-may-6-12-2026.md]
namespace: mkt
---

# Три рычага AI-операционки — Remove / Compress / Rebuild

Операционная рамка из TYPICAL Telegram-поста 1332 (`2026-05-08`), описывающая, **как руководителю внедрить AI в команду сегодня**, чтобы повысить выработку (revenue/employee). Атрибуция: [[evolving/competitor-positioning/typical-company]] (consulting/edu-бизнес TYPICAL, ведущая канала, экспертность `inferred medium`). `confidence: medium` — авторская рамка, продолжение структурной [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]] (пост 1330 от того же канала).

**Operational counterpart к 3-shifts (структурной рамке).** Где 3 сдвига объясняют, **почему** product-economics меняется, 3 рычага — **что делать с этим внутри команды на этой неделе**.

Мы храним в `canon/marketing-frameworks`, потому что:
- рамка **архитектурно стабильна** (3 рычага описывают общие классы изменений, не конкретные tools / vendors),
- не требует numeric strict-citation — это reusable conceptual framework,
- конкретные numeric anchors (revenue/empl., productivity-multiplier) живут в `evolving-strict/*` и [[evolving/industry-trends/ai-for-managers-2025-2026]].

## Рамка целиком

Перед перечислением: TYPICAL framing — «**если ваша прибыль на сотрудника не растёт, проверьте 3 рычага**».

### Рычаг 1. **Remove** — убрать лишнюю человеческую работу

TYPICAL formulation:

> «Созвоны-уточнения, ручные отчёты, повторяющиеся объяснения, онбординг через людей вместо системы. Большая часть этого уже автоматизируется.»

**Что значит на практике:**

- **Созвоны-уточнения** — встречи, где обсуждают, что было решено или что нужно сделать. Решаются: decision logs (рычаг 3 use-case), асинхронные writeup'ы, AI-резюме встреч.
- **Ручные отчёты** — собрать данные из 5 источников и записать в 6-й. Решается: BI-инструменты + LLM-saммари + auto-report генераторы.
- **Повторяющиеся объяснения** — onboarding, ответы на одни и те же вопросы клиентов/команды. Решается: документация + AI-поиск + first-line auto-answer.
- **Онбординг через людей вместо системы** — каждый новичок отнимает 20+ часов senior'а на «введение в курс». Решается: structured docs + AI-tutoring + self-paced playbook.

**Diagnostic question:** «Какие задачи у меня есть **только потому, что их раньше можно было сделать только так**?»

### Рычаг 2. **Compress** — сжать цикл, сократить время итерации

TYPICAL formulation:

> «Прототипирование, вариации, саммари переговоров, автоматические выводы вместо ручной аналитики. Чем быстрее цикл, тем выше выработка на сотрудника.»

**Что значит на практике:**

- **Прототипирование.** Не «3-недельная разработка прототипа», а «3 дня от идеи до first prototype» через no-code AI tools (Lovable, Cursor, Bolt). См. [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]].
- **Вариации.** Не «один креатив на тестирование», а 10-20 вариаций через AI на pre-test. См. [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] для examples в content domain.
- **Саммари переговоров.** Granola, Otter, Fireflies — AI-cаммари с decision-points + action items. Уже стандарт.
- **Автоматические выводы вместо ручной аналитики.** Не «дашборд + ручной insight», а LLM-ассистент, который читает дашборд и пишет краткий выводный текст «что произошло за неделю».

**Diagnostic question:** «Где **между шагами** у меня самая длинная пауза (waiting time)? Что можно сжать?»

### Рычаг 3. **Rebuild** — пересобрать процесс

TYPICAL formulation:

> «Если бы вы строили этот процесс сегодня с AI, он вообще выглядел бы так же? Часто оказывается, что ускорять нечего — процесс просто устарел.»

**Что значит на практике:** **самый важный из трёх** — не «как сделать существующий процесс быстрее», а **«нужен ли вообще этот процесс»**. Часто после реальной попытки автоматизировать процесс выясняется:
- Процесс существует, потому что когда-то не было AI для его частей. С появлением AI часть из шагов **не имеет смысла**.
- Например: «3-уровневая модерация контента» — придумано для случая, когда нет автоматических AI-фильтров. С AI-фильтром нужен 1-уровень + AI-review, а не 3 человеческих уровня.

**Diagnostic question:** «Если бы я начинал команду с нуля сегодня, я бы вообще придумал этот процесс?»

**TYPICAL-pattern сила:** Rebuild **не дешевле и не быстрее, чем Compress**. Это организационно труднее (нужно перестроить организацию, заново обучать), но *структурно* самое мощное — потому что Remove и Compress оптимизируют существующее, Rebuild **заменяет** на что-то качественно другое.

## Self-serve как естественное следствие 3 рычагов

> «Так часть функций естественно уходит в self-serve — когда сотрудник закрывает задачу без вовлечения коллег.»

**Self-serve** — не отдельный рычаг, а **результат**, к которому ведут все 3:
- Remove → убираем coordinator-роль из workflow
- Compress → сотрудник не ждёт ответа коллеги, потому что цикл сжат
- Rebuild → workflow построен на single-actor + AI ассистент, без cross-team-handoff

Это меняет **org-design** команды: меньше координаторов, больше single-actor specialists с AI-amplification. См. [[canon/marketing-frameworks/ai-amplifier-fragmented-vs-modular-jobs]].

## Эвристика 3+ повторений — TYPICAL canonical decision rule

Главное actionable правило поста 1332:

> Если один и тот же запрос повторяется **3+ раза**, это кандидат на автоматизацию.

**Почему 3+, а не 2+ или 5+?** Это TYPICAL pattern, не теоретический optimum, но он балансирует:
- **2+ слишком рано** — false positive автоматизаций, которые потом не используются
- **5+ слишком поздно** — упускаешь окно, когда автоматизация ещё ROI-positive
- **3+ как threshold** — даёт сигнал «это не one-off, это паттерн», но ещё не успел стать pain

**Как использовать в team-workflow:**
- Маркер «3rd time today this question came up» в чате/тикетах → ticket «explore automation candidate»
- В weekly retro команды: каждый отвечает «какой запрос я ответил 3+ раз на этой неделе?»

Эта эвристика **закрепляется как самостоятельный pattern** в `canon/marketing-frameworks` — короткий, actionable, reusable.

## 6 use-cases AI для усиления процессов (TYPICAL checklist)

Из того же поста 1332 — конкретные точки, где AI работает «out of the box» в management-контексте:

| # | Use-case | Tool/Pattern | Связь с рычагами |
|---|---|---|---|
| 1 | Резюме встреч для принятия решений | Granola, Otter | Compress |
| 2 | Ведение журнала решений (decision logs) | Notion + AI, Linear, custom GPTs | Compress + Rebuild |
| 3 | Первый уровень общения с клиентом | Chatbot, AI-помощник | Remove |
| 4 | Авторевью контента и документов | LLM + Notion AI, Cursor | Compress |
| 5 | Поиск по базе знаний вместо обращений к коллегам | RAG, AI-поиск | Remove |
| 6 | Генерация обучающих материалов из реальных процессов | Loom + GPT, structured docs | Remove |

**6 use-cases** не претендуют на исчерпываемость — это **starter pack**, который TYPICAL рекомендует «попробовать на этой неделе». Это **explicit lowest-friction onboarding-path для AI** в команду. Совпадает с тезисом TYPICAL поста 1303 о том, что **«управление информацией и коммуникацией — главный AI rapid-win»** ([[evolving/industry-trends/ai-for-managers-2025-2026]] data-point 3).

## Связь с другими TYPICAL рамками

3 рычага вместе с 3 сдвигами составляют **тематическую дилогию TYPICAL** про AI:

```
[3 сдвига — structural]                  [3 рычага — operational]
1. Productivity per person ↑       →     1. Remove
2. Function boundaries dissolve    →     2. Compress
3. Bottleneck → distribution        →     3. Rebuild
```

Не **строгое 1-to-1** соответствие, скорее: **3 сдвига объясняют, почему рамка нужна; 3 рычага — как её приложить на этой неделе**.

Для **content marketing GRO:** оба используются вместе. 3 сдвига — opening hook (зачем тебе это надо), 3 рычага — body (что конкретно делать).

## Использование в content GRO

### Длинная форма (статья / лендинг)

**«Три рычага AI для руководителя в 2026»** — готовый skeleton long-read'а:
- Hook — «прибыль на сотрудника AI-компаний vs Apple» (anchor к [[evolving-strict/market-data/ai-vendor-revenue-per-employee-2026]])
- 1) Remove — что в команде делается, только потому что иначе раньше было нельзя
- 2) Compress — где между шагами waiting time
- 3) Rebuild — что бы вы вообще не строили сейчас с нуля
- Эвристика 3+ повторений
- 6 use-cases starter pack
- Tie-back: GRO для self-management — личный аналог 3 рычагов на уровне одного человека

Атрибуция: «по operational-рамке TYPICAL» с `[conf:medium]`. Не подменять авторской.

### Короткая форма (TG / Reels)

**3-card carousel:**
- Слайд 1 — «3 вопроса руководителю на этой неделе»
- Слайд 2 — Что я делаю **только** потому что иначе раньше было нельзя? (Remove)
- Слайд 3 — Где между шагами waiting? (Compress)
- Слайд 4 — Что бы я не делал сейчас с нуля? (Rebuild)
- CTA — GRO Productivity для индивидуального применения

### Hooks (готовые формулировки)

- «3 повторения = кандидат на автоматизацию. Простая эвристика, которую может ввести любой руководитель сегодня.»
- «Не "как сделать процесс быстрее". А "нужен ли он вообще". Это rebuild.»
- «Самая мощная экономия времени — не оптимизация существующего workflow, а его удаление.»

## Anti-patterns при использовании

- **Не цитировать как «по TYPICAL» 6 use-cases без атрибуции.** Use-cases — handpicked TYPICAL'ом из общедоступного AI-tooling каталога. Атрибуция: «по operational-чек-листу TYPICAL».
- **Не превращать в waterfall.** «Сначала Remove, потом Compress, потом Rebuild» — неверно. 3 рычага **параллельны**, не последовательны. Команда может делать Rebuild на одном процессе и Compress на другом одновременно.
- **Не путать с replacement.** «Remove человеческой работы» **не означает** замену людей AI. Это убирание **типа задач**, который раньше требовал человеческого вовлечения. Освободившееся время команды направляется на distribution / trust / packaging (Сдвиг 3 из [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]]).

## Связанные страницы

- [[sources/2026-05-14-tg-typicalcompany-may-6-12-2026]] — источник рамки (TYPICAL пост 1332)
- [[evolving/competitor-positioning/typical-company]] — автор рамки
- [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]] — структурный counterpart (3 сдвига объясняют, почему 3 рычага нужны)
- [[canon/marketing-frameworks/ai-amplifier-fragmented-vs-modular-jobs]] — org-design следствие self-serve паттерна
- [[evolving/industry-trends/ai-for-managers-2025-2026]] — это пост = 6-я data-точка в общем тренде
- [[evolving/industry-trends/ai-productivity-j-curve-2026]] — productivity gap внутри команды между AI-power-users и средним пользователем
- [[evolving-strict/market-data/ai-vendor-revenue-per-employee-2026]] — numeric anchors для opening hook
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]] — Rycag 2 (Compress) практические tools
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — Rycag 2 в content domain
- [[canon/marketing-frameworks/typical-productized-services-pivot]] — другая рамка из того же ingest
