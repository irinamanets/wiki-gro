---
id: mkt:evolving/content-trends/claude-code-skills-bank-2026
title: "Claude Code Skills Bank — must-have набор скиллов для маркетолога (апрель 2026)"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [claude-code, claude-skills, vibecoding, marketing-ops, superpowers, get-shit-done, marketing-skills, claude-seo, composio, deep-research, loki-mode, typefully, remotion, gstack, ui-ux-pro-max, frontend-slides, nuwa-skill]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-14
sources: [sources/2026-05-05-tg-solokumi-redump-dec25-apr26.md, sources/2026-05-14-tg-solokumi-may-2026.md]
namespace: mkt
---

# Claude Code Skills Bank — апрель 2026 (must-have)

Дрейфующий каталог конкретных скиллов Claude Code, которые на конец апреля 2026 рекомендованы как маст-хэв для маркетолога-практика. Каноническая **архитектура** скилла («1 скилл = 1 задача», REFERENCE.md, MCP) — стабильна и живёт в [[canon/marketing-frameworks/claude-skills-architecture]]. Здесь — **что именно поставить прямо сейчас**.

Это evolving: каталог обновляется быстрее, чем за полгода. Новые скиллы появляются еженедельно, старые устаревают или мерджатся в новые версии. TTL — 90 дней soft re-verify.

Источник: Р. Кумар Виас, [[sources/2026-05-05-tg-solokumi-redump-dec25-apr26|@solokumi]] пост 402 (2026-04-30) — публикация Виаса с annotated списком; пост 390 (2026-03-31) — упоминание [`everything-claude-code`](https://github.com/affaan-m/everything-claude-code) (27 агентов / 64 скилла / 33 команды) как эталонная подборка.

## Цена ошибки

> Если врубить сразу 50 скиллов, результат ухудшится, потому что агент начинает путаться в инструкциях.
>
> — @solokumi пост 402, 2026-04-30

Поэтому **собирайте маленький стек под повторяющиеся процессы**, а не «всё подряд». Ниже — список тех, что Виас рекомендует как маст-хэв; для маркетолога это ~5-7 одновременных скиллов.

## Маст-хэв скиллы (апрель 2026)

### 1. Superpowers — обязательный first install

Топовый скилл с **150 000 stars на GitHub** `[conf:high, src:2026-04-30]` от obra (см. [github.com/obra/superpowers](https://github.com/obra/superpowers)). Превращает агента из «неструктурированного активного джуна во вдумчивого структурного синиора».

Команды:
- `/brainstorm` — агент задаёт набор вопросов **до** старта, прежде чем что-то фигачить
- `/write-plan` — разбивает задачу на шаги и показывает план перед началом, можно внести правки до реализации
- `/execute-plan` — запускает несколько суб-агентов одновременно + чекает результат в конце

Это базовый productivity-усилитель для любой нетривиальной задачи. Должен ставиться первым.

### 2. Get Shit Done (GSD) — менеджер проектов внутри Клода

Решает проблему context-degradation при длительной работе: после нескольких часов работы Claude может начать забывать, что он делал. GSD разбивает проект на **3 изолированные фазы** — план / выполнение / ревью. Каждый агент стартует с **чистым контекстом 200 000 токенов** `[conf:high, src:2026-04-30]` и передаёт состояние следующему через файлы на диске.

Репозиторий: [github.com/gsd-build/get-shit-done](https://github.com/gsd-build/get-shit-done).

### 3. Frontend-design — официальный плагин Anthropic

До написания любого кода заставляет агента принять чёткое design-решение (брутально минималистичное, редакторское, ретрофутуристичное и т.д.) и раскатывать именно его. Решает паттерн «слопные ИИ-сайты» с однотипным дизайном.

Если делаешь сайт или приложение — ставится первым после Superpowers. Репозиторий: [github.com/anthropics/claude-code/tree/main/plugins/frontend-design](https://github.com/anthropics/claude-code/tree/main/plugins/frontend-design).

### 4. Marketing Skills — пак для маркетолога

Коллекция скиллов: CRO, копирайтинг, SEO, аналитика, стратегии роста — в одном комплекте. Один раз настраиваешь под себя (TOV, ЦА, продукт) и дальше не объясняешь агенту каждый раз.

Репозиторий: [github.com/coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills).

### 5. Claude SEO — полная SEO-система с суб-агентами

**19 sub-skills + 12 sub-агентов** `[conf:high, src:2026-04-30]`: технический SEO, E-E-A-T анализ, schema-разметка, исследование ключей, аудит конкурентов, бэклинки, локальный SEO, Google API и отчёты в PDF / Excel.

Закрывает почти весь цикл важных SEO-задач, если делаешь руками. Репозиторий: [github.com/AgriciDaniel/claude-seo](https://github.com/AgriciDaniel/claude-seo).

### 6. Composio — MCP-доступ к 500+ внешним сервисам

Не скилл, а **MCP-интеграция** (протокол MCP — Model Context Protocol — даёт Claude прямой доступ к внешним сервисам). Через одну подписку Composio получаешь Gmail, Slack, GitHub, Notion, Telegram, Figma и **ещё 500+ приложений** `[conf:high, src:2026-04-30]`. Claude напрямую выполняет действия в этих сервисах, управляет авторизацией и автоматизирует воркфлоу через несколько инструментов сразу.

Сайт: [composio.dev/toolkits/composio/framework/claude-code](https://composio.dev/toolkits/composio/framework/claude-code).

### 7. Deep Research — нормальный ресёч с источниками

**8-фазный pipeline** `[conf:high, src:2026-04-30]` с оценкой достоверности источников и автовалидацией. Работает для анализа рынка, подготовки к запуску на новом рынке — везде, где нужен структурированный ресёч с проверяемыми ссылками.

Репозиторий: [github.com/199-biotechnologies/claude-deep-research-skill](https://github.com/199-biotechnologies/claude-deep-research-skill).

### 8. Code Simplifier — официальный clean-up

Официальный плагин от Anthropic, которым команда Claude Code чистит свой собственный код. Сканирует проект, убирает мусор, **снижает расход токенов** при дальнейшей работе. Ссылка: [claude.com/plugins/code-simplifier](https://claude.com/plugins/code-simplifier).

### 9. Superflow — проектирование сложных задач

«Любимый скилл Виаса» — позволяет делать сложные задачи через project-flow. Особенно полезен, когда задача нелинейная и состоит из нескольких связанных подзадач, которые нужно спланировать как граф.

Репозиторий: [github.com/egerev/superflow](https://github.com/egerev/superflow).

## Volume 2 — апдейт от 2026-05-12 (ещё 7 скиллов)

12 мая 2026 Виас публикует [[sources/2026-05-14-tg-solokumi-may-2026|вторую партию из 7 скиллов]] (карусель 408–415). Базовая партия (предыдущий пост vol. 1) была репостнута почти 1500 раз `[conf:medium, src:2026-05-12]` — это сигнал работающего формата. Новая партия добавляет: **рой агентов / мульти-агентная оркестрация, постинг, видео-генерация, дизайн-машина, презентации, виртуальные клоны экспертов**.

### 10. loki-mode — оркестратор роя из 37 субагентов

Запускает и оркеструет **рой 37 субагентов в 6 свормах параллельно** `[conf:high, src:2026-05-12]`, каждый со своей ролью и контекстом. Работают автономно над разными кусками задачи (от плана до деплоя и маркетинга), потом сводят результат.

> «Фактически это как нанять команду джунов и синьоров на свой проект, только бесплатно и без джиры и созвонов.»
>
> — карточка скилла, @solokumi 409, 2026-05-12

Архитектурно похоже на [[canon/marketing-frameworks/multi-agent-marketing-org-principles]] — но в одном скилле, готовом из коробки. Альтернатива GSD (см. #2 в первой партии) с акцентом не на context-degradation, а на parallelism.

Репозиторий: [github.com/asklokesh/claudeskill-loki-mode](https://github.com/asklokesh/claudeskill-loki-mode).

### 11. Typefully — постинг в соцсети из Claude

Написал пост или тред в Claude → **одной командой** кидаешь его в очередь на релиз сразу в несколько соцсетей через Typefully. Поддерживает **X (Twitter), LinkedIn, Threads**. Удобно для контент-завода (когда заранее сгенерил пачку постов, нужно разлить по каналам).

Это MCP-интеграция, документация: [typefully.com/?settings=integrations-claude](https://typefully.com/?settings=integrations-claude) ([Support article](https://support.typefully.com/en/articles/13128440-typefully-mcp-server)).

### 12. Remotion — видео из текста одним кликом

«After Effects, где вместо мышки на таймлайне ты пишешь словами»: пишешь сценарий типа «в первую секунду появись логотип слева, во вторую секунду выскочи текст справа, в третью покажи график», Remotion читает это и собирает готовый видеофайл, готовый под постинг в соцсети.

Заменяет full-stack video pipeline (After Effects + Premier + дизайнер) на текстовый интерфейс. Доки: [remotion.dev/docs/ai/skills](https://remotion.dev/docs/ai/skills).

### 13. GStack (Garry Tan, президент YCombinator) — инженерная команда из 23 инструментов

Сборка от **Garry Tan, президента YCombinator** `[conf:high, src:2026-05-12]`. Превращает Claude в инженерную команду из **23 инструментов под разные роли** `[conf:high, src:2026-05-12]`:

| Роль | Что делает |
|---|---|
| CEO | развивает продукт |
| Eng Manager | выстраивает архитектуру |
| Designer | ловит AI-слоп (анти-паттерн-фильтр) |
| Reviewer | ищет баги |
| QA | открывает реальный браузер для тестов |
| Release Engineer | релизит готовый продукт |

Это **полная инженерная org structure** в одной сборке. Аналог GSD по идее, но на 4x более глубокую глубину ролей. Репозиторий: [github.com/garrytan/gstack](https://github.com/garrytan/gstack).

### 14. UI-UX Pro Max — дизайн-интеллект под капотом Claude

«Прокачанная версия скилла frontend-design» (см. #3 в первой партии). Внутри собрано **67 UI-стилей, 161 палитра, 57 пар шрифтов, 99 UX-правил, 25 типов графиков, поддержка 16 стеков** `[conf:high, src:2026-05-12]`. Подбирает дизайн **под продукт и аудиторию** вместо генерации шаблонов.

Важно отличить от frontend-design: тот заставляет принять design-решение и держаться его (борьба со «слопным AI-сайтом»); ui-ux-pro-max — это **library + опционная логика подбора**. Используются вместе.

Репозиторий: [github.com/nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill).

### 15. frontend-slides — презентации одним кликом

Быстро генерит презентацию из материалов в **одном из 10 встроенных стилей** `[conf:high, src:2026-05-12]`. Конвертирует PPT в нужный формат, сохраняя картинки и анимации. Когда нужно собрать pitch-deck для встречи через 30 минут — самое то.

Репозиторий: [github.com/zarazhangrui/frontend-slides](https://github.com/zarazhangrui/frontend-slides).

### 16. nuwa-skill — виртуальные клоны экспертов

Даёшь имя любого человека → **Nuwa спавнит 6 research-агентов** `[conf:high, src:2026-05-12]`, которые роются в его книгах, подкастах и соцсетях. На выходе — готовый скилл «думать как X» с его ментальными моделями, методами принятия решений и паттернами речи.

**В репо уже лежат готовые шаблоны**: Стив Джобс, Илон Маск, Чарли Мангер, Ричард Фейнман, Навал Равикант, Нассим Талеб, Андрей Карпатый `[conf:high, src:2026-05-12]`.

Маркетинговый use-case: «mental model brainstorm» — приводишь к проблеме виртуального Фейнмана и виртуального Мангера, получаешь два разных угла без созыва живых экспертов. Тоже архетип «множество ролей в одном агенте», но в отличие от GStack — это не операционная команда, а **корпус мыслителей**.

Репозиторий: [github.com/alchaincyf/nuwa-skill](https://github.com/alchaincyf/nuwa-skill).

## Маркетплейсы скиллов

- **SkillHub** — [skillhub.club](https://www.skillhub.club/), **7 000+ скиллов с one-click install** `[conf:high, src:2026-04-30]`
- **Built-in marketplace** в самом Claude Code (через CLI)
- **`everything-claude-code`** на GitHub ([affaan-m/everything-claude-code](https://github.com/affaan-m/everything-claude-code)) — фантастическая подборка, **27 агентов / 64 скилла / 33 команды** `[conf:high, src:2026-03-31]` (пост 390)

## Лайфхаки от Виаса

- **`/loop` для ночного выполнения** — крутит итерации локально, пока ноутбук включён (см. [[canon/marketing-frameworks/claude-md-structure-marketing#claude-code-расширенные-возможности]])
- **Remote Tasks в Claude.ai → Projects → Scheduled Tasks** — выполняется на серверах Anthropic без включённого ноутбука
- **HANDOFF.md** — внешняя память агента между сессиями: «после каждых 10 действий обновляй HANDOFF.md». Утром открыл один файл — за 2 минуты понял всё, что произошло за ночь
- **Haiku вместо Opus для мониторинга и сбора данных** — кратно дешевле, справляется не хуже на простых задачах
- **MCP Excalidraw skill** — превращает любой процесс в диаграмму прямо в рабочем пространстве. Полезно для визуализации архитектуры мульти-агентных систем
- **Лучший скилл — тот, что напишешь сам** под свой процесс. Маркетплейс — стартовая точка, не финал

## Anti-patterns

- **Установить 50 скиллов одновременно** — деградация результата
- **Использовать только готовые скиллы из маркетплейсов** — никогда не дойдёшь до собственного качества
- **Ставить Marketing Skills без настройки под TOV / ЦА / продукт** — генерирует общий generic-маркетинг
- **Игнорировать MCP** — скилл без MCP остаётся на уровне brainstorm-партнёра, не исполнителя
- **Не использовать Code Simplifier** на больших проектах — расход токенов растёт нелинейно

## Связь с другими страницами

- [[canon/marketing-frameworks/claude-skills-architecture]] — каноническая архитектура скилла
- [[canon/marketing-frameworks/claude-md-structure-marketing]] — `CLAUDE.md` как корневой брифинг, на котором живут скиллы
- [[canon/marketing-frameworks/multi-agent-marketing-org-principles]] — где скиллы выступают должностными инструкциями AI-сотрудников
- [[evolving/content-trends/ai-tools-self-hosting-arbitrage]] — связка in-house агентов и self-hosted infra
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]] — экосистема Cursor / Claude Code / Codex
- [[evolving/content-trends/sales-ops-ai-tooling-stack-2026]] — соседний стек инструментов (Clay, Gumloop, ElevenLabs, etc.) для sales-ops, дополняющий skills bank

## Backlinks

_9 pages link to this one._

- [[canon/marketing-frameworks/claude-md-structure-marketing]]
- [[canon/marketing-frameworks/claude-skills-architecture]]
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]]
- [[evolving/content-trends/ai-tools-self-hosting-arbitrage]]
- [[evolving/content-trends/sales-ops-ai-tooling-stack-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-solokumi-redump-dec25-apr26]]
- [[volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1]]
