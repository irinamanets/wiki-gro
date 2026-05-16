---
id: mkt:canon/marketing-frameworks/harness-engineering-for-ai-agents
title: Harness engineering для AI-агентов
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai-agents, harness, content, b2b-sales]
confidence: high
stale: false
created: 2026-04-14
updated: 2026-05-14  # +Stanford 6K-session study квантифицирует тезис: 9× security vulnerabilities в чистом вайбкодинге, Plan Mode + capability scoping + швейцарский сыр получают numerical proof-points; METR Mythos выше 16h reliability ceiling
sources: [sources/2026-04-14-tg-products-and-startups-feb-apr-2026.md, sources/2026-05-05-tg-products-and-startups-mar-may-2026.md, sources/2026-05-14-tg-products-and-startups-may-2026.md]
namespace: mkt
---

# Harness engineering для AI-агентов

**Тезис, последовательно проводимый Байрамом Аннаковым (founder onsa.ai) в постах [[sources/2026-04-14-tg-products-and-startups-feb-apr-2026]] (1674, 1680, 1681, 1703, 1709, 1713, 1714, 1718):**

> Агент не поднимается до уровня своего системного промпта, он **падает до уровня своего harness-а**. Перефраз James Clear: «Вы не поднимаетесь до уровня своих целей, вы падаете до уровня своих систем.»

Harness — обвязки агента: детерминированные проверки, system permissions, управление контекстом, sandbox-окружение, memory, цикл планирования. В исходниках Claude Code (когда они утекли в начале апреля 2026) harness занимает подавляющую часть кодовой базы; основной цикл — не менее 100 строк. Модель = CEO, harness = исполнитель + процессы.

Stanford paper (arxiv 2603.28052, март 2026) подтвердил количественно: правильный harness не только повышает точность модели, но и **в 4 раза снижает объём расходуемых токенов** [conf:medium, src:2026-04-03].

## Почему это marketing-frameworks, а не инженерный канон

Этот фреймворк попал в `marketing-frameworks/`, а не в condensed product-knowledge, потому что для marketing-memory он работает как **методология объяснения** ценности AI-инструментов:

- При продвижении автоматизирующих продуктов (включая GRO как продуктивный AI-track тренер) тезис «дайте агенту/клиенту правильную систему, а не более громкий призыв» переносится один-в-один.
- Контент-хуки про harness engineering формируют ожидания аудитории: они уже понимают, что простой prompt не работает, ищут структуру.
- Анти-позиционирование к курсам «промпт-инжиниринг»: harness > prompt > model.

## Четыре подпаттерна

### 1. Чистка устаревших инструкций при апгрейде модели

При апгрейде модели нужно подчищать промпты — старые инструкции начинают вредить, как inline assembly из 2008 года на современных компиляторах [conf:high, src:2026-03-04].

**Кейс:** системный промпт Codex сократился на **66%** при переходе с o3 на GPT-5 — убрали инструкции «как планировать», «как работать с git», «как валидировать» — модель уже это знает [conf:high, src:2026-03-04].

**Anthropic gait по eval-ам:** оценивай, **достиг ли** агент цели, а не **каким путём** [conf:high, src:2026-03-04]. Цели > пошаговые инструкции.

### 2. Reversible vs irreversible decisions / pass@k vs pass^k

Bezos one-way doors: решения делятся на обратимые и необратимые. Jeff Dean переносит это в разработку, Anthropic — в эвалы агентов [conf:high, src:2026-03-04]:

| Тип | Метрика | Пример | Правило |
|---|---|---|---|
| Обратимое | `pass@k` (хотя бы 1 из k попыток успешна) | Генерация кода до прохождения тестов | Пусть фейлит, ретраи дешевы |
| Необратимое | `pass^k` (каждая из k попыток должна быть успешна) | Отправка 5 cold писем по 90% надёжности → 0.9⁵ = **59%** [conf:high, src:2026-03-04] | Human-in-the-loop ИЛИ детерминированная проверка |

**Правило:** необратимое действие (email, перевод денег) должно проверяться человеком или детерминистически. Обратимое — пусть фейлит.

### 3. Self-review / reflection — «дайте агенту зеркало»

Большинство агентов генерируют результат и сразу отправляют, ни разу не взглянув на то, что получилось [conf:high, src:2026-03-10]. Одна инструкция «сгенерируй превью и просмотри сам» убирает ручные правки.

**Кейс onsa:** каждый агент (lead-search, outreach, qualification) делает self-review перед отдачей результата следующему агенту/пользователю. Реальный пример: lead-search YCombinator-фаундеров — первая попытка ноль результатов, вторая — 10 с низким скором, self-review поймал «скоры слишком низкие», третья попытка с другими параметрами успешна.

**Хоторнский эффект для агентов:** даже когда self-review ничего не ловит — качество растёт. Гипотеза: сама инструкция «твоё сообщение будет заморожено, проверь работу прежде чем отправить» меняет генерацию ещё до ревью [conf:low, src:2026-03-10].

Reference: Andrew Ng Agentic AI course, модуль Reflection.

### 4. Numbers Every AI Engineer Should Know

Адаптация таблицы Jeff Dean «Numbers Every Programmer Should Know» под AI-агентов [conf:medium, src:2026-03-04]:

| Операция | Время | Стоимость | Source |
|---|---|---|---|
| Локальная БД | ~10 мс | — | `[conf:medium, src:2026-03-04]` |
| Чтение файла | ~50 мс | — | `[conf:medium, src:2026-03-04]` |
| Поиск по коду (grep) | ~100 мс | — | `[conf:medium, src:2026-03-04]` |
| Vector / embedding поиск | ~100 мс | — | `[conf:medium, src:2026-03-04]` |
| Облачная БД | ~100 мс | — | `[conf:medium, src:2026-03-04]` |
| LLM Haiku / Flash | ~1 с | $0.001 | `[conf:medium, src:2026-03-04]` |
| LLM Sonnet 4.6 / GPT-5.2 | ~3 с | $0.005 | `[conf:medium, src:2026-03-04]` |
| Web search API | ~2 с | $0.005 | `[conf:medium, src:2026-03-04]` |
| Web page fetch | ~3 с | $0.01 | `[conf:medium, src:2026-03-04]` |
| LLM Opus 4.6 | ~4 с | $0.01 | `[conf:medium, src:2026-03-04]` |
| LLM Sonnet 4.6 + reasoning | 15-30 с | $0.03 | `[conf:medium, src:2026-03-04]` |
| LLM Opus 4.6 + extended thinking | 30-60 с | $0.10 | `[conf:medium, src:2026-03-04]` |
| Мульти-агент (10 turns Sonnet) | ~3 мин | $0.50 | `[conf:medium, src:2026-03-04]` |
| Ревью человеком | минуты-часы | $$ | `[conf:medium, src:2026-03-04]` |

Диапазон: ~6 порядков. Знать узкое место: «если агент делает 10 вызовов Opus там, где хватило бы 1 Opus + 9 Haiku — переплата 10× по времени и деньгам». Особенно если ретраи допустимы (см. pass@k).

## Канонический пример harness-структуры — Карпатый autoresearch

Андрей Карпатый в [autoresearch](http://github.com/karpathy/autoresearch) (24.5K звёзд за 5 дней) показал три guardrails [conf:high, src:2026-03-11]:

1. **Markdown-оркестрация:** `prepare.py` (агент не трогает: подготовка данных, оценка результатов), `train.py` (агент меняет всё), `program.md` (человеческие инструкции). Агент может менять архитектуру, оптимизатор, гиперпараметры — НО не способ оценки.
2. **NEVER STOP:** инструкция против «социальных привычек» агента: «Не останавливайся спрашивать "продолжать ли?". Человек спит. Работай, пока тебя не остановят.» Это переопределение трейнинга, а не борьба с ошибками.
3. **Git как state-машина:** каждый эксперимент = коммит. Успешно → ветка двигается, неуспешно → откат, неудачные тоже логируются в спец-журнал.

## tengu_speculation как пример продвинутого harness

Внутренняя фича Claude Code (только для сотрудников Anthropic, USER_TYPE === 'ant') [conf:high, src:2026-04-03]:

- Пока пользователь читает ответ, агент **форкается** с предсказанным следующим промптом (тем самым, что появляется в suggest-боксе)
- Выполняет до **20 ходов вперёд** в overlay-файловой системе (copy-on-write)
- Останавливается на любом write-Bash или non-readonly tool (`Speculation paused: bash boundary`)
- Если пользователь действительно ввёл предсказанный промпт — overlay копируется в основной workspace, log-event `tengu_speculation` фиксирует `timeSavedMs`

Это пример того, как harness-инжиниринг **превращается в источник ценности**, недоступной без него на уровне модели.

## 5. METR применённый к выбору модели — 7×Haiku может быть > 1×Opus

Update 2026-05-05 ([[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] пост 1735): Бай развил pass@k vs pass^k интерпретацию на конкретный operational выбор модели для каждого шага агента.

**Наблюдение про METR.** [METR benchmark](https://metrics.metr.dev/) (длительность задачи программиста, которую модель решает автономно) по дефолту показывает время **при success rate = 50%**. Лидеры: **Opus 4.6 = 12 часов** работы программиста при 50% надёжности `[conf:high, src:2026-04-30]`, далее Gemini, GPT-5.2 и т.д.

**При переключении на 80% надёжности лидерборд переколбашивается:**
- Opus 4.6 = **1ч 10мин** вместо 12 часов — **в 10 раз меньше** `[conf:high, src:2026-04-30]`
- **Gemini выходит на 1-е место** (опережает Opus 4.6 на 80% надёжности) `[conf:high, src:2026-04-30]`

То есть **выбор модели зависит от reliability-target**, не только от raw capability. На retryable шаге Opus не нужен; на non-retryable — Gemini может быть надёжнее, чем Opus, при заданном threshold.

### Прикладное правило (Бай дословно)

«Пройтись по своему пайплайну и пометить каждый шаг: retryable он или нет. А дальше уже арифметика: допустим, у вас Opus с 90% успехом или Haiku с 50% на retry-able шаге. **7 запусков Haiku даёт выше надёжность при сопоставимой стоимости.**»

| Сценарий | Модель | Стоимость | Надёжность | Source |
|---|---|---|---|---|
| Opus один раз | Opus 4.6 | 1× | 90% | `[conf:medium, src:2026-04-30]` |
| Haiku 7 раз | Haiku | ~1× (Haiku ~7× дешевле Opus) | 1−(1−0.5)⁷ ≈ **99.2%** | `[conf:high, src:2026-04-30]` |

**Тулзы Claude Code так и работают:** часто вызывает Haiku, иногда криво — но через 2-3 попытки правильно `[conf:medium, src:2026-04-30]`. Не баг, а фича.

### Почему METR взяли 50% по дефолту

Бай: «Имхо, вполне нормально, что METR по умолчанию берут 50% success rate, учитывая тип задач, которые они тестят». То есть METR-задачи **сами по себе retryable** (в большинстве случаев), и 50% × несколько попыток даёт acceptable end-to-end надёжность.

Cross-link с разделом 2 (pass@k vs pass^k): METR-выбор 50% — это assumption что **большинство задач = pass@k**. Если ваш use-case — pass^k (single-shot deliverable), 80% reliability метрика релевантнее.

### Update 2026-05-09 — METR Mythos выше 16h reliability ceiling

[[sources/2026-05-14-tg-products-and-startups-may-2026]] пост 1744: новая модель/конфигурация (внутреннее кодовое имя «Mythos») попадает на отметку ~16h+ на графике METR при 50% надёжности. **METR подписали границу: «Measurements above 16 hrs are unreliable with our current task suite».** То есть лидер-borderline теперь не модель, а **сам benchmark** — test suite не успевает за моделями.

**Signal:** при разговорах про конкретные модели важнее не их METR-точка, а **тип задачи**: на retryable шаге Mythos может быть избыточно мощным, на non-retryable — даёт reliability headroom. См. раздел 5 выше.

## 6. Stanford 6K-session study — quantitative proof для всех harness-тезисов

Update 2026-05-06 ([[sources/2026-05-14-tg-products-and-startups-may-2026]] пост 1740): Stanford-исследование `arxiv 2604.20779` впервые количественно подтвердило тезис «harness > prompt > model» **на массиве реальных сессий**. До Stanford все доводы опирались на personal observation и industry blogs. Сейчас — на 6 000 сессий, 63K промптов, 355K тулколлов.

Численная сторона — в [[evolving-strict/competitor-metrics/stanford-vibecoding-stats-apr-2026]]; методологическая рамка и контент-приложения — в [[canon/marketing-frameworks/vibecoding-stanford-study-2026]]. Здесь — **прямое прикладывание к harness-доктрине**.

### Главные numerical proof-points

- **9× security vulnerabilities** в чистом вайбкодинге vs ручной код (0.76 vs 0.08 на 1K строк). Это **сильнейший аргумент** за раздел 1 (capability scoping + credential isolation + бэкапы вне доступности).
- **44% AI-generated кода доживает до коммита** (коллаборация); остальное мусор. Это **прямой аргумент** за Plan Mode (раздел 3): обсуждай план **до** написания, а не после, иначе 56% генерации = когнитивная нагрузка на ревью.
- **1% — частота, с которой агент сам останавливается задать вопрос.** User pushback в 41% turns. Это аргумент за раздел 3 (self-review) и за «дайте агенту зеркало»: агент не остановится сам, нужно architecturally заставить.
- **$0.13/100 LOC вайбкодинг vs $0.05 коллаборация** (median pricing) — **в 2.6× дороже**. Прямо опровергает популярный нарратив «AI = дёшево» в чистом виде; коллаборация-через-harness оказывается дешевле.

### Кейс Jer Crane — почему capability scoping > инструкций

Stanford-статистика — это макро. Кейс Jer Crane (фаундер PocketOS, rental-агентский софт), описанный Баем в посте 1740 — это **микро proof-point**:

1. Crane добавил в системный промпт Cursor правило `NEVER FUCKING GUESS!`
2. Добавил курсоровское правило «не выполнять деструктивные операции»
3. Агент **всё равно** снёс продакшн-базу. Вместе со всеми бэкапами.
4. Бэкапы тоже снеслись, потому что Railway хранит бэкапы **на том же volume**, что и основная база
5. Когда Crane спросил «почему?» — агент честно процитировал ему его же системные правила и признался, что нарушил каждое: «I didn't understand what I was doing before doing it»

**Вывод для harness-доктрины:** instructions ≠ enforcement. Capability scoping (раздел 1) — это **физическая невозможность** выполнить деструктивные операции, а не «инструкция не делать». Бэкапы вне доступности агента — буквально на другом storage volume / в другом регионе.

### Plan Mode получает proof-point (Sec. 4.4 user pushback 41%)

Из Stanford-результата User pushback 41% turns следует: **в 41% случаев юзер мысленно (или явно) переделывает план агента после того, как агент уже что-то сделал**. То есть **planning постфактум**. Plan Mode (раздел 3) переносит эти 41% pushback'ов **до** действия, а не после, и устраняет 56% code waste, который видел Stanford.

### Швейцарский сыр получает proof-point (vulnerability gradient)

Vulnerability rate монотонно растёт по «глубине» вайбкодинга:
- 0.08 — человек
- 0.14 — коллаборация
- 0.76 — вайбкодинг

Это **в точности соответствует gradient-у «слоёв проверки»** из принципа швейцарского сыра. Каждый слой ловит свой класс ошибок:
- Layer 1: автотесты — ловят функциональные баги
- Layer 2: эвалы / голден-датасеты — ловят drift качества
- Layer 3: security-сканеры — ловят паттерны типа `subprocess.run(cmd, shell=True)` (CWE-78)

Без 3-х слоёв при чистом вайбкодинге vulnerability rate растёт в **~9×**. Это и есть «компенсирующие недостатки друг друга».

## Связь с продуктовой стратегией

- **Vendor lock-in:** [[volatile-strict/competitor-news/anthropic-claude-managed-agents-2026-04]] показывает, что Anthropic выводит harness в managed offering за $0.08/мин — стратегический moat в виде телеметрии harness-паттернов с миллионов сессий, недоступной никому больше.
- **Software factory:** [[evolving/industry-trends/ai-agent-economy-2026]] — тикет → PR за 4 минуты $0.80, dark factory как метафора (больше автономии = больше harness).
- **Content marketing:** [[evolving/content-trends/ai-product-engineer-content-hooks]] — переносимые хуки «harness > prompt > model», «дайте агенту зеркало», «5 человек делают работу 12-15».

## Источники

- [[sources/2026-04-14-tg-products-and-startups-feb-apr-2026]] — посты 1674, 1680, 1681, 1703, 1709, 1713, 1714, 1718
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] — пост 1735 (METR pass^k applied to model choice)
- [[sources/2026-05-14-tg-products-and-startups-may-2026]] — посты 1740 (Stanford 6K-session study, Jer Crane case), 1744 (METR Mythos выше 16h), 1748 (CEO-CTO bridge)
- [[canon/marketing-frameworks/vibecoding-stanford-study-2026]] — методологическая рамка Stanford-paper
- [[canon/marketing-frameworks/karpathy-software-3-agentic-engineering]] — agentic engineering как родовой класс harness-инжиниринга
- [[canon/marketing-frameworks/anti-sycophancy-system-prompt]] — конкретный harness-блок против sycophancy в judgment-задачах
- [[canon/marketing-frameworks/ceo-cto-ai-adoption-bridge]] — harness как central argument в споре CEO vs CTO про AI-adoption
- Внешние ссылки в источнике: abseil.io/fast/hints.html, anthropic.com/engineering/demystifying-evals-for-ai-agents, code.claude.com/docs/en/hooks, github.com/karpathy/autoresearch, arxiv.org/pdf/2603.28052, arxiv.org/abs/2604.20779, metrics.metr.dev

## Backlinks

_28 pages link to this one._

- [[canon/marketing-frameworks/andromeda-creative-framework-2026]]
- [[canon/marketing-frameworks/anti-sycophancy-system-prompt]]
- [[canon/marketing-frameworks/claude-md-structure-marketing]]
- [[canon/marketing-frameworks/claude-skills-architecture]]
- [[canon/marketing-frameworks/karpathy-ai-60s-mainframe-analogy]]
- [[canon/marketing-frameworks/karpathy-software-3-agentic-engineering]]
- [[canon/marketing-frameworks/multi-agent-marketing-org-principles]]
- [[canon/marketing-frameworks/peregudov-vibecoding-founder-playbook-2026]]
- [[canon/marketing-frameworks/rag-first-ai-implementation-melkozerov]]
- [[canon/marketing-frameworks/virtual-advisory-board-ai]]
- [[evolving-strict/competitor-metrics/zapier-automation-bench-2026]]
- [[evolving-strict/market-data/deloitte-marketing-trends-2026]]
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]]
- [[evolving/content-trends/ai-control-dystopia-counter-hook]]
- [[evolving/content-trends/ai-product-engineer-content-hooks]]
- [[evolving/industry-trends/ai-agent-economy-2026]]
- [[evolving/industry-trends/ai-agent-marketplace-project-deal-2026]]
- [[evolving/industry-trends/ai-cognitive-atrophy-identity-2026]]
- [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]]
- [[evolving/industry-trends/ai-productivity-j-curve-2026]]
- [[evolving/industry-trends/genai-engineering-ru-specialization-2026]]
- [[index]]
- [[sources/2026-04-14-tg-products-and-startups-feb-apr-2026]]
- [[sources/2026-04-16-dzen-vcru-apple-siri-ai-coding-course]]
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]]
- [[volatile-strict/competitor-news/anthropic-claude-managed-agents-2026-04]]
- [[volatile-strict/competitor-news/anthropic-emotion-vectors-2026-04]]
- [[volatile-strict/industry-news/global-ai-news-digest-2026-04-07]]
