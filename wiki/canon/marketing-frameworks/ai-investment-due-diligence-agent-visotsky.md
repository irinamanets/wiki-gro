---
id: mkt:canon/marketing-frameworks/ai-investment-due-diligence-agent-visotsky
title: AI investment-due-diligence agent — 4-стадийный пайплайн (Высоцкий, Claude)
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai, agent, due-diligence, automation, claude, owner-self-management, workflow]
confidence: medium
stale: false
created: 2026-05-31
updated: 2026-05-31
sources: [sources/2026-05-31-tg-alexander-visotsky-may-27-30-2026.md]
namespace: mkt
---

# AI investment-due-diligence agent — 4-стадийный пайплайн (Высоцкий)

Reusable AI-workflow-паттерн от Александра Высоцкого (founder [[evolving/competitor-positioning/business-booster-visotsky|Business Booster]]), описанный в Telegram-канале [@alexander_visotsky](https://t.me/alexander_visotsky) пост 3845 (2026-05-27), см. [[sources/2026-05-31-tg-alexander-visotsky-may-27-30-2026|source-дамп]]. Это **4-й публичный operational AI-case** канона Высоцкого (после Claude Cowork-страховки, инвест-дека и личного CFO — см. [[evolving/content-trends/visotsky-ai-personal-assistant-narratives]]).

Качественно отличается от предыдущих кейсов: это не one-off operation и не personal-finance-роль, а **autonomous agentic due-diligence pipeline** — агент, настроенный на постоянную задачу (анализ входящих инвест-предложений) с правом самостоятельно вести переписку с внешними людьми.

Экспертность: **inferred** (публичный founder-инвестор) → `confidence: medium`, атрибуция к автору. Self-reported reliability («на грубых ошибках ни разу не ловил») → `[conf:low]`, не верифицировано.

## Контекст агента
Агент в Claude знает интересы владельца, его подходы, чем он занимается и какую ценность может дать проектам. На входе — инвестиционные презентации (питч-деки), приходящие Высоцкому как потенциальному инвестору / эдвайзеру. Цель — автономно отфильтровать поток и выдать решение, экономя время основателя на первичном анализе.

## 4 стадии пайплайна

| Стадия | Что делает | Тип проверки |
|---|---|---|
| **1. Поиск противоречий** | Оценивает внутреннюю логичность презентации: есть ли нестыковки, бьются ли цифры между собой | Internal consistency check |
| **2. Agentic outreach** | Если что-то не сходится — **сам ведёт переписку с фаундерами**, задаёт уточняющие вопросы, добывает недостающие данные | Autonomous external data-gathering |
| **3. Внешняя сверка** | Сверяет заявления с рыночными показателями и реальной бизнес-практикой | External world-grounding |
| **4. Вердикт** | Выдаёт решение: инвестировать / стать эдвайзером / не подходить к проекту | Decision output |

**Side-output (не стадия, но заявленная фича):** агент всегда даёт качественную обратную связь отправителю — «что подкрутить, что улучшить, чтобы проект полетел». Это превращает фильтрацию входящих в **goodwill-генератор**: даже отказ оставляет ценность у автора питча.

## Почему это значимый паттерн

1. **Agentic, не assistive.** Ключевое отличие от кейсов #1–#3 Высоцкого — стадия 2: агент **сам инициирует внешнюю коммуникацию** с третьими лицами (фаундерами), а не только обрабатывает данные владельца. Это переход от «AI как ассистент» к «AI как делегированный аналитик с правом действия». Перекликается с [[canon/marketing-frameworks/harness-engineering-for-ai-agents|harness-engineering]]: агент работает в выстроенном пайплайне, а не на одном промпте.
2. **Structured judgment, не суммаризация.** Большинство AI-due-diligence-демо 2026 = «загрузи дек → получи summary». Этот пайплайн добавляет **multi-stage reasoning с действием**: consistency → gather → ground → decide. Это ближе к [[canon/marketing-frameworks/multi-agent-marketing-org-principles|triangulation-валидации]] (внутренняя логика + внешняя сверка + добор данных).
3. **Human-in-the-loop на вердикте, не на процессе.** Владелец делает финальное решение и даёт экспертизу, но «первичный анализ и оценку делает ИИ». Это **operational threshold** делегирования: человек оставляет за собой judgment, отдаёт AI рутину фильтрации.

## Связь с инвест-фреймворками канона

- **[[canon/marketing-frameworks/blank-when-to-raise-investment|Правило Бланка — когда привлекать инвестора]]** — обратная сторона того же стола: Бланк про критерии фаундера, этот пайплайн про критерии инвестора.
- **[[canon/marketing-frameworks/shaq-investment-principles|Принципы инвестиций Шакила О’Нила]]** — human-judgment-критерии («верю + пользуюсь лично»), которые на стадии 4 остаются за человеком, не за AI.
- **[[canon/marketing-frameworks/agalarov-tangibility-investment-test|Тест осязаемости Агаларова]]** — ещё один human-judgment-критерий инвестрешения, комплементарный AI-pre-screening'у.

## Адаптация для GRO-контента

GRO — не AI-инструмент и не инвест-продукт, но паттерн переносим как **content-asset** и как **format**:

- **Content-hook**: «как я делегировал AI рутину, оставив за собой только решение» — узнаваемая [[evolving/content-trends/visotsky-ai-personal-assistant-narratives|first-person operational AI-case]]-структура. Для GRO эквивалент — «AI берёт трекинг состояния, я оставляю за собой только выбор практики».
- **4-stage template** как reusable narrative-скелет для любого «как я автоматизировал X»-поста: проверка логики → добор данных → сверка с реальностью → решение. Применимо к разбору любого decision-workflow.
- **Anti-pattern**: не позиционировать GRO как «AI-агента» (misleading), не цитировать Высоцкого дословно.

Валидирует [[evolving/industry-trends/agent-first-world-openclaw-2026|agent-first-world сигнал]]: публичный founder из non-AI-вертикали (бизнес-консалтинг) строит и публично показывает **multi-stage agentic workflow** с правом действия, не просто чат-ассистента.

## Связанные страницы
- [[evolving/content-trends/visotsky-ai-personal-assistant-narratives]] — 4-й operational AI-case в серии автора
- [[evolving/competitor-positioning/business-booster-visotsky]] — профиль автора / контекст канала
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — harness-pattern для agentic workflow
- [[canon/marketing-frameworks/blank-when-to-raise-investment]] — комплементарный инвест-фреймворк
- [[canon/marketing-frameworks/shaq-investment-principles]] — human-judgment-критерии (стадия 4)
- [[evolving/industry-trends/agent-first-world-openclaw-2026]] — agent-first-world контекст
- [[sources/2026-05-31-tg-alexander-visotsky-may-27-30-2026]] — source (пост 3845)
