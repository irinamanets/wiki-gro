---
id: mkt:evolving/industry-trends/code-with-claude-2026-frameworks
title: "Code w/ Claude 2026 — дистилляция конференции: узкое место сдвигается в инфраструктуру вокруг модели"
type: page
subtype: insight
layer: evolving
theme: industry-trends
tags: [ai-agents, harness-engineering, agent-memory, claude-code, anthropic, content, awareness, consideration]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-products-and-startups-may-15-19-2026.md]
namespace: mkt
---

# Code w/ Claude 2026 — дистилляция конференции

**Источник:** Байрам Аннаков, пост 1752 «7 идей с конфы Code w/ Claude» + OCR его персонального mini-сайта (attached 1753/1754/1755) ([[sources/2026-05-19-tg-products-and-startups-may-15-19-2026]]). Конференция: **19 докладов, 8.5 часов** `[conf:high, src:2026-05-18]`, [плейлист на YouTube](https://www.youtube.com/watch?v=GMIWm5y90xA&list=PLmWCw1CzcFim2obQ-w3ohbULOfwp5lApR). Эксперт verified; синтез — `confidence: medium`.

> ⚠ Видео-нарезка докладов (attached 1752, 504MB) транскрипт получить не удалось (whisper quota 429). Контент полностью покрыт авторской дистилляцией + OCR mini-сайта.

## Центральная тема всех докладов

> **Узкое место сдвигается в инфраструктуру вокруг модели** — harness, системы обратной связи, системы верификации, контекст и память, безопасная работа агентов, эвалы. — Аннаков, обобщая все токи

Это прямой резонанс с [[evolving/industry-trends/ai-value-migration-2026]] (ценность уплывает от моделей) и с [[canon/marketing-frameworks/harness-engineering-for-ai-agents]]. Та же мысль, что в [[evolving/industry-trends/ai-accountability-premium-2026]]: модель-«делание» обнуляется, ценность мигрирует к слоям вокруг неё.

## 7 топ-идей (по Аннакову)

1. **Haiku берёт Opus в эдвайзеры (Advisor pattern).** Агент на слабой модели (Haiku) получает эдвайзера на сильной (Opus) и обращается к ней простым tool call. Near-Opus intelligence при Haiku-цене. CPO GitHub. Детальнее: [Advisor strategy blog](https://claude.com/blog/the-advisor-strategy), [docs](https://platform.claude.com/docs/en/agents-and-tools/tool-use/advisor-tool).
2. **Время полураспада агента (Half-Life Rule).** Код, компенсирующий непредсказуемость агента, имеет half-life **6–12 месяцев** `[conf:medium, src:2026-05-18]` → лабы реализуют это как встроенную возможность модели/API. А код, «подключающий» агента к вашему **уникальному миру** (контекст, авторизация, внешние системы) — реально уникален, **компаундится**, туда и надо вкладываться.
3. **Как работает Claude Code-команда.** Отказ от долгосрочных роадмапов (JIT planning); технические дебаты решаются 2-3 альтернативными pull-реквестами, а не whiteboarding; узкое место смещается на проверку и безопасность.
4. **Дайте каждому агенту свой компьютер с теми же тулами и «глазами», что у вас.** Онбординг агента ≈ онбординг сотрудника + computer use + self-improvement loop (агент репортит затруднения → люди+агенты решают → рой агентов тестит).
5. **Оценивайте новую версию модели по тому, помогает ли она удалить код.** Лучший сигнал на апгрейд — что вы теперь можете удалить код / сократить промпт.
6. **3 аспекта памяти агента: хранение, структура, процесс.** Где хранится память; структура (.md-файлы для памяти, скиллы как «процессная» память); процесс (что триггерит обновление, как оно происходит). Резонирует с [[canon/marketing-frameworks/claude-skills-architecture]].
7. **Закон Amdahl как бизнес-стратегия (Bottleneck Migration).** Ускорил один этап в **3–5×** `[conf:medium, src:2026-05-18]` → остальные становятся узким местом. Задача CEO/продакта — те самые медленные стадии; причём перепроектировать **сразу**, а не после. Следующие юникорны — там, где кто-то построит инфраструктуру верификации/оценки аутпута модели, которой нет у других.

## Framework Library — словарь именованных mental models (OCR 1754)

Аннаков собрал **24 именованных mental model** из 19 докладов как «словарь для постов, слайдов курса и архитектурных ревью». Наиболее ценные для маркетинга/позиционирования:

| Mental model | Суть | Маркетинговое применение |
|---|---|---|
| **Advisor pattern** | Дешёвый executor + дорогой on-demand консультант (Haiku-junior, Opus-senior) | hook «семь раз Haiku, один раз Opus» — экономия |
| **Half-Life Rule** | Scaffolding вокруг слабостей модели — распадается; tools/data/auth к вашему миру — компаундятся | где строить moat |
| **Agent Front Door** | Уникальные API/тулы/контекст, которые экспонирует только ваш продукт — **новый moat** | прямой positioning-язык |
| **Effort Dial** | Заменяет бинарный thinking-toggle: управляет тем, **как сильно** работает модель, не «работает ли» | UX-нарратив |
| **Three-Layer Memory** | Short / Medium / Long память + «dreaming pass» между сессиями | контент про память агентов |
| **JIT Planning · Code Wins** | Технические дебаты решать генерацией 2-3 PR параллельно, не whiteboarding | process-инсайт |
| **Manager-as-IC** | Плоская оргструктура, каждый менеджер шипит код (дефолт команды Claude Code) | org-design нарратив |
| **Bottleneck Migration** | Ускорил этап в 3-5× → остальное узкое место. Amdahl's Law как product strategy | стратегический hook |
| **Dark Factory** | Агенты работают ночью без человека в петле (credit: Simon Willison) | provocative-hook |
| **Country of Geniuses in a Data Center** | North star Дарио (Anthropic): достигается иерархическим multi-agent | визионерский нарратив |
| **Saturation Curve of Form Factors** | Чатботы насыщены; coding/agentic формы ещё растут — изобретай следующую | продуктовый инсайт |
| **Hold Light and Shade** | Принцип релиза Anthropic: шипить агрессивно **И** ответственно. Оба, каждый релиз | мост к [[canon/marketing-frameworks/ai-agent-architectural-guardrails-2026]] |

Полный список из 24 — в OCR-разделе «Распознанный текст → 1754» source-страницы [[sources/2026-05-19-tg-products-and-startups-may-15-19-2026]].

## Что нового анонсировано (из OCR 1755 — keynote tags)

Opening Keynote (47 мин) анонсировал: **routines, dreaming, mythos, /ultrareview**, task-horizon, async-engineering. «What's new in Claude Code» (25 мин): **Auto Mode, Work Trees, Auto Memory, Routines**. Live-coding с Boris Cherny & Jarred Sumner: Robobun-агент контрибьютит в Bun больше PR, чем сам Jarred. Это volatile-news-материал — фиксируем как контекст, отдельную news-страницу не создаём (нет верификации первоисточников из видео).

## Применение для контента GRO

1. **Готовый словарь mental models.** Framework Library — 24 узнаваемых термина для постов про AI-агентов; повышает «экспертность» контента ГРО без необходимости самим придумывать рамки.
2. **«Узкое место в инфраструктуре» как сквозной нарратив.** Подкрепляет позиционирование: ценность не в самой модели, а в том, что вокруг неё (контекст, верификация, навыки человека) — bridge к [[canon/positioning/gro-value-proposition]].
3. **Amdahl-as-strategy + Bottleneck Migration** — готовая рамка для постов про продуктивность/процессы для founder-аудитории.
4. **Half-Life Rule** — мощный hook: «не строй то, что лаба встроит через полгода; строй то, что подключает AI к твоему уникальному миру».

## Hooks

- «Узкое место больше не в коде. Оно в том, что вокруг модели: память, верификация, контекст.»
- «Half-Life Rule: если код компенсирует тупость модели — он умрёт через полгода. Если подключает к твоему миру — компаундится.» `[conf:medium, src:2026-05-18]`
- «Семь раз Haiku, один раз Opus: дешёвый агент с дорогим советником в кармане.»
- «Amdahl как стратегия: ускорил один этап в 5× — остальные стали бутылочным горлышком. Это и есть задача CEO.» `[conf:medium, src:2026-05-18]`

## Caveat'ы и TTL

- Дистилляция конференции автором (verified, priority-1), `confidence: medium`. Конкретные числа (94-96% cache, 6-12 мес, 3-5×) — из докладов через OCR, `medium`, воспроизводить как «по материалам Code w/ Claude 2026».
- `evolving`, TTL soft 180 дней. Re-verify к 2026-11: какие из анонсов (routines, dreaming, mythos) реально вышли; устарели ли mental models с новыми релизами.

## Связанные страницы

- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — инфраструктура надёжности агентов (центральная тема конференции)
- [[evolving/industry-trends/ai-value-migration-2026]] — «ценность уплывает от моделей» — макро-рамка той же мысли
- [[evolving/industry-trends/ai-accountability-premium-2026]] — узкое место → верификация → ответственность
- [[canon/marketing-frameworks/ai-agent-architectural-guardrails-2026]] — «Hold Light and Shade» / безопасность как часть релиза
- [[canon/marketing-frameworks/claude-skills-architecture]] — скиллы как «процессная» память (идея 6)
- [[canon/marketing-frameworks/generative-ui-design-system-inference]] — generative-UI / визуализация аутпута (пост 1753)
- [[sources/2026-05-19-tg-products-and-startups-may-15-19-2026]] — источник (посты 1752–1755)

## Источники

- [[sources/2026-05-19-tg-products-and-startups-may-15-19-2026]] — посты 1752–1755
- [Code w/ Claude 2026 playlist](https://www.youtube.com/watch?v=GMIWm5y90xA&list=PLmWCw1CzcFim2obQ-w3ohbULOfwp5lApR)
- [Advisor strategy (Claude blog)](https://claude.com/blog/the-advisor-strategy)
