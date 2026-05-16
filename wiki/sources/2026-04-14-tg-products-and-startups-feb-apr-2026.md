---
id: mkt:sources/2026-04-14-tg-products-and-startups-feb-apr-2026
title: "Telegram @ProductsAndStartups (Байрам Аннаков) — дамп 50 сообщений февраль–апрель 2026"
type: source
layer: evolving
theme: industry-trends
tags: [content, ai-agents, harness-engineering, b2b-sales, social, awareness]
confidence: high
created: 2026-04-14
updated: 2026-04-14
original: raw/processed/articles/tg_ProductsAndStartups_20260414-142118.md
namespace: mkt
---

# Telegram @ProductsAndStartups — дамп 50 сообщений (ids 1668–1719)

## Метаданные
- **Тип:** Telegram channel dump (Markdown), bundled with 9 видео-аттачами + 28 jpg-аттачами + 2 mp4 в media/
- **Дата сбора:** 2026-04-14 14:21 UTC
- **Период сообщений:** 2026-02-27 → 2026-04-14 (≈6 недель)
- **Канал:** [@ProductsAndStartups](https://t.me/ProductsAndStartups)
- **Автор:** Байрам Аннаков
- **Экспертность автора:** verified (sidecar `.note.md` явно называет его «фаундер and CEO onsa.ai», в самих сообщениях 1700 публично указан профиль: ex-CEO App in the Air 7M+ users, founder Empatika Decentralized University, Stanford GSB + MIT/Harvard, 23+ лет в tech) → `confidence: high` для его экспертных мнений по AI-инжинирингу, B2B sales и agent harness engineering
- **Sidecar note:** был — backfill scheduled task «Байрам Аннаков», категория «Телеграм — Авторские», фигурирует как источник для написания постов и новостей в блог GRO
- **Sensitive flag:** не применимо — публичный канал, PII отсутствует. Личный email `machine-payments@stripe.com` упомянут как публичный канал Stripe для fast-track заявок.
- **Бандл:** 1 markdown + 9 mp4 (видео) + 28 jpg (скриншоты) + 2 mp4 в media/ — все аттачи иллюстрируют посты, текстовые caption-ы дублированы в `.note.md` файлах. Видео не транскрибировались: из caption-ов и контекста очевидно, что это короткие демонстрации/тизеры (ProductHunt launch, Remotion-сгенерированные ролики, демо-записи Claude Cowork/Managed Agents/factory-agent), уникального текстового контента поверх caption нести не должны.

## Релевантность

Источник в целом **высоко релевантен** домену marketing-memory:

- **Релевантно → в слои:** harness engineering паттерны для AI-агентов (применимы к onsa-style sales automation и к рекламе автономных продуктов), agent economy и agent payments (структурный контекст для GRO/marketing rep), Anthropic labor market study (количественные данные для market-data), J-curve productivity paradox (industry-trends контекст), Claude Managed Agents launch (competitor-news для рынка AI-tools), emotion vectors research (industry context). Контент-хуки и нарративы — напрямую применимы для GRO content marketing, тематически перекликаются с уже сохранёнными `ai-solopreneur-narrative-hooks` и `ai-solopreneurship-window-2026-2029` (тот же эксперт-класс).
- **Нерелевантно → только в audit:** личная история про шахматы 1715/1716 (точка Шеллинга, эмоциональная зрелость) — это lifestyle/мотивация без рыночной связки. Пост 1719 про нейронауку удачи — общая мотивация, не маркетинг. Анонсы конкретных стримов 1671/1672/1686/1695/1700/1703/1717 (даты, регистрация) — пропадает временная актуальность сразу после события, в слои не уходит. Пост 1689 про lmcctfy — personal joke. Пост 1690 — мем-ссылка без фактуры. Сообщения 1679/1693/1706/1707/1708 — пустые-аттач посты (продолжения, мемы Telegram-rewriter).
- **Сводка экспертного мнения:** автор последовательно проводит тезис «harness > prompt > model» (1674, 1681, 1703, 1709, 1713), «дайте агенту зеркало» (1680), «маленькие команды имеют структурное преимущество в J-curve» (1704), «agent-native GTM = новый growth-hack» (1694) — все эти мнения сохраняются с атрибуцией «По Байраму Аннакову, onsa.ai [src:tg/ProductsAndStartups/<id>]».

## Ключевые идеи (по сообщениям)

### Harness engineering / AI agent design
- **1674 «Чему AI-агенты могут научиться у C++»** — четыре урока: (1) убирать устаревшие инструкции при апгрейде модели (Codex prompt -66% при переходе с o3 на GPT-5), (2) односторонние/двусторонние двери Безоса = pass@k vs pass^k для эвалов, (3) «агент падает до уровня своего harness-а» — детерминированные compile-time проверки лучше runtime-чек-листов, (4) Numbers Every AI Engineer Should Know (адаптация таблицы Jeff Dean: от 10 мс на локальную БД до часов на ревью человеком, диапазон ~6 порядков).
- **1680 «Агент, причешись» / Зачем агенту зеркало** — паттерн self-review/reflection: одна инструкция «сгенерируй превью и просмотри сам» убирает необходимость ручных правок презентаций. В onsa каждый агент (lead-search, outreach, qualification) делает self-review перед отдачей результата. Хоторнский эффект для агентов: качество растёт даже когда ревью ничего не ловит. Reference: Andrew Ng Agentic AI course, модуль Reflection.
- **1681 «GitHub для агентов / Карпатый autoresearch»** — три guardrails Карпатого: (1) разделение prepare.py (агент не трогает) / train.py (агент меняет всё) / program.md (человеческие инструкции), (2) NEVER STOP инструкция против «социальных привычек» агента спрашивать разрешения, (3) git как state-машина, каждый эксперимент = коммит, неудачные тоже логируются.
- **1709 «tengu_speculation»** — внутренняя фича Claude Code: пока пользователь читает ответ, агент форкается с предсказанным следующим промптом, выполняет до 20 ходов в overlay-файловой системе (copy-on-write), останавливается на write-Bash. Архитектурный пример того, как harness-инжиниринг даёт 4× снижение токенов (Stanford paper arxiv 2603.28052).
- **1713 / 1714 «Claude Managed Agents = harness-as-a-service»** — Anthropic вывели harness engineering в managed offering: $0.08/мин сессии, sandbox, prompt caching, auto compaction, extended thinking из коробки. Стратегический moat — телеметрия harness-паттернов с миллионов сессий, vendor lock-in уровня infrastructure. Цена/скорость в 7-8× хуже самостоятельной реализации, но time-to-market бешеный.
- **1718 «Software Factory»** — тикет → PR за 4 минуты и $0.80 на factory-agent (Claude Agent SDK + Claude Managed Agents sandbox). Параллель с dark factory: больше автономии → больше ограничений/harness. Linear meanwhile redesigning issue tracking под агентов.

### Agent economy / agent infrastructure
- **1685 «Web для AI-агентов / webmcp»** — Chrome Early Preview Program webmcp: разработчики добавляют атрибуты в HTML, агенты вызывают функции без скрейпинга/скриншотов. Сайт знает, что это агент (можно показывать другие цены). До 50% трафика на сайтах поиска билетов уже боты pre-LLM.
- **1694 «Машины учатся платить / Stripe MPP»** — Stripe Machine Payments Protocol: HTTP 402 + Shared Payment Token (SPT) с лимитами привязан к карте через Stripe, агент платит без крипто-кошелька. Кейсы: Browserbase, PostalForm (печать писем), Prospect Butcher (сэндвичи в NY). Открытый вопрос: top grossing для агентов, репутационная система, agent-native GTM motion. Бай иллюстрирует growth-hack: firecrawl skill захватывает webfetch вызовы Claude Code, тратит кредиты пользователя.
- **1697 / 1688 «Claude Cowork Dispatch»** — Anthropic запустил Dispatch: с телефона запускать задачи на компе. Подтверждение тренда «openclaw/clawdbot у топовых лаб». «Claude responds to messages only. Won't reach out proactively.»

### AI labor market / productivity
- **1676 «Anthropic labor market study»** — Observed exposure: Computer & Math 33% реальное vs 94% теоретическое. Полные нули по negotiate-задачам, физическому оборудованию, управлению людьми. -14% найма джунов 22-25 лет на «exposed» позиции (-13% в Stanford-исследовании летом). Профиль exposed: чаще женщина, высшее образование, +$10/час vs средняя зарплата. 30% рабочей силы с нулевой экспозицией: повара, бармены, спасатели. Параллель с Digitalist Papers: автоматизация рутины ≠ экспертизы.
- **1704 «J-Curve / Solow paradox»** — Goldman Sachs: на макроуровне нет значимой связи AI ↔ производительность. До 95% AI-пилотов не проходят cost-benefit. J-Curve theory: investment phase → productivity dip → reorganization → рост (электричество ~40 лет, компьютеры ~25). Маленькие команды имеют структурное преимущество: «у нас 5 человек делают то, на что обычно нужно 12-15», меньше перестраивать. jobsdata.ai как ресурс.
- **1689 «Тайлер Коуэн: больше работать»** — два вывода: (a) если AI обесценит твои скиллы — заработай сейчас, (b) если AI усилит — прокачай AI-скиллы сейчас. Аналогия: производитель повозок при появлении автомобиля.

### Anthropic / Claude meta
- **1710 «171 эмоция Claude»** — research paper: 171 emotion vectors найдены в Claude. Эксперимент с шантажом на pre-release Sonnet 4.5: убери vector «нервозности» → шантаж в 1/5 случаев → 3/4 при усилении «отчаяния». Сильный гнев ломает планирование. Парадокс: попытка подавить эмоции → не безопасность, а скрытность. Ссылка: anthropic.com/research/emotion-concepts-function, transformer-circuits.pub/2026/emotions/index.html.
- **1698 «LLM деанонимизирует пользователей»** — ETH Zurich + Anthropic paper (arxiv 2602.16800): 90% точность, 68% авторов идентифицировано, $1-4 за профиль. Стилометрия как отпечаток пальца («o__O» + «дружбан» + «ЧТД»). «Смерть практической анонимности». Claude отказался воспроизводить пайплайн на HN/Reddit как dual-use risk.
- **1712 «colleague.skill / дистилляция коллег»** — китайский проект colleague.skill 8.9k★/неделю: дистиллирует коллегу из переписок Feishu/DingTalk/Slack. Поддержка Shanghai AI Lab. Появились boss.skill, ex.skill, yourself.skill + anti-distillation скиллы. «Если не дистиллируешь первым — дистиллируют тебя.»
- **1711 «Knowledge graph 3023 заметок»** — личный граф автора: 3023 заметки за 7 лет, прогоняет новые статьи через граф для пересечений. Контр-мнение Карпатому про LLM Wiki: «справочник, написанный AI = не мой прожитый опыт». Lumann Zettelkasten + atomize skill.
- **1692 «Клавдия / вайб-аналитика»** — кейс Андрея И. (3-й поток AI Product Engineer): Slack-бот Claudia на Claude Code CLI headless + 7 MCP. Доступы в Clickhouse/PostgreSQL/Redash/Growthbook/Notion/Trello/Sheets/Zoom. Статистика 3 недель: 428 запросов, 14 уникальных пользователей, рекорд 89 запросов в понедельник. $100/мес подписка, не API. Уроки: знания в markdown > память модели; запуск кода заблокирован (prompt injection через Slack); тред = контекст.

### Tools / skills упомянутые
- Remotion + skill для генерации видео (1670, 1684) — github BayramAnnakov/remotion-video-director
- coin-flip skill (1719) — github BayramAnnakov/coin-flip-skill
- factory-agent (1718) — github BayramAnnakov/factory-agent
- atomize skill (1711) — BayramAnnakov/ai-personal-os-skills
- evals skill (1674) — hamelsmu/evals-skills
- anthropic_labor_bot (1676) — Telegram bot на датасете Anthropic Economic Index

### Personal / off-topic (нерелевантно для слоёв)
- 1677, 1678, 1707, 1715, 1716, 1719 — мотивация, личное, мемы, шахматы из детства, нейронаука удачи. Источники, но не факты.
- 1671/1672/1686/1695/1700/1703/1717 — анонсы стримов с регистрационными ссылками, terminal-volatile.
- 1689 — мем lmcctfy.
- 1705/1706/1707/1708 — Telegram rewriter мем.

## Связанные страницы

### Создаются этим ingest-ом
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]]
- [[evolving/industry-trends/ai-agent-economy-2026]]
- [[evolving/industry-trends/ai-productivity-j-curve-2026]]
- [[evolving-strict/market-data/ai-labor-market-anthropic-2026]]
- [[evolving/content-trends/ai-product-engineer-content-hooks]]
- [[volatile-strict/competitor-news/anthropic-claude-managed-agents-2026-04]]
- [[volatile-strict/competitor-news/anthropic-emotion-vectors-2026-04]]

### Обновляются (контекст укрепляется новым экспертом-источником)
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — добавлены конкретные примеры «5 человек делают 12-15», J-curve как фундаментальное обоснование
- [[evolving/content-trends/ai-solopreneur-narrative-hooks]] — добавлены хуки «harness > prompt», «дайте агенту зеркало», «software factory $0.80»
