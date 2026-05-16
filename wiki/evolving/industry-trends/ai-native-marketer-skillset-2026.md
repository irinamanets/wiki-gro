---
id: mkt:evolving/industry-trends/ai-native-marketer-skillset-2026
title: "AI-native маркетолог 2026 — профиль навыков и роли"
type: page
subtype: trend
layer: evolving
theme: industry-trends
tags: [ai, marketing, skillset, role, career, future-of-work]
confidence: high
stale: false
created: 2026-04-14
updated: 2026-05-14  # +параллель из engineering recruiting (Volkov через @ai_newz 4568) — adoption AI упирается в команду, не в бюджет/стратегию; AI-native skills gap как индустриальный bottleneck
sources: [sources/2026-04-14-tg-solokumi-nov2025-apr2026.md, sources/2026-05-05-tg-products-and-startups-mar-may-2026.md, sources/2026-05-14-tg-ai-newz-may-2026.md]
namespace: mkt
---

# AI-native маркетолог 2026 — профиль навыков

Как изменилась роль маркетолога за последний год и что должен уметь человек, работающий в маркетинге в 2026, чтобы не оказаться в поиске работы к концу года. Синтез практического наблюдения Р. Кумара Виаса, [[sources/2026-04-14-tg-solokumi-nov2025-apr2026|@solokumi]] посты 357 (2025-12-16) и 377 (2026-02-16), с cross-check'ом к [[evolving/industry-trends/ai-native-company-architecture-2026]] и [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]].

Это evolving: конкретный список инструментов дрейфует 2–4 месяца, но **структурные изменения роли** устойчивы на 1–2 года. TTL soft 180 дней, hard — при смене поколения моделей или рекламных платформ.

## Главный сдвиг

Техническая настройка рекламных кабинетов — **уходит в прошлое**. После [[canon/marketing-frameworks/andromeda-creative-framework-2026|Andromeda]] и аналогичных AI-систем в TikTok/Яндексе рычаг оптимизации смещается с «правильной настройки таргета» на «системного производства разнообразия креативов». Всё решает **креативный процесс**, а не пальцы на ползунках.

Маркетолог 2026 — это **не «человек, который настраивает рекламный кабинет»**. Это **оркестратор контентного конвейера**, подкреплённого системой AI-агентов, с навыком вайбкодинга и методологической глубиной в JTBD/AJTBD.

## Что должен уметь: 6 устойчивых навыков

### 1. Построить креативный процесс на основе данных

Не «сочинять креативы из головы», а забирать вход из:
- [[canon/marketing-frameworks/ai-video-production-pipeline|Трендвотчинга]] (системный анализ работающих крео своих и конкурентов)
- **JTBD / AJTBD** (методология Вани Замесина, ядро выявления болей)
- **Анализа звонков сейлзов** (ИИ-ОКК, 40–50 параметров оценки, cross-extract инсайтов для маркетинга)
- **Анализа CTR / CVR предыдущих креативов** по параметрам

См. [[evolving/content-trends/ai-static-creative-templates-2026]] и [[canon/marketing-frameworks/ai-video-production-pipeline]] для практики.

### 2. Системно анализировать крео конкурентов через ИИ-тулы

Meta Ad Library, Google Ads Transparency Center, TikTok Creative Center, LinkedIn Ad Library, VK Реклама + скрипты парсинга через Apify/Firecrawl/Exa.ai + агенты, которые автоматически собирают данные в таблицу с параметрами (тип хука, локация, актёр, формат, длительность открута).

См. [[evolving/industry-trends/agent-first-world-openclaw-2026]] как общее направление «парсить всё через агентов».

### 3. Быстро и дёшево запускать **сотни разных креативов**

- Производственная ёмкость — **десятки креативов в неделю**, не 3–5
- Параметризация результатов (каждый креатив разбит на измеримые характеристики)
- Масштабирование наиболее эффективных связок в парадигме Andromeda
- Стоимость видео-креатива — **$7–15** при полном AI-production цикле (см. [[canon/marketing-frameworks/ai-video-production-pipeline]])

### 4. Быстро тестировать разные воронки — от VSL до квизов — с помощью ноукод-тулов

- **VSL-воронка** (Video Sales Letter) — упомянута @solokumi как «самая трендовая и конверсионная последних месяцев»
- **Квиз-воронка** — для B2C, особенно Fitness & Health
- **Вебинарная воронка** — классика для B2B и дорогих продуктов
- **ManyChat welcome-цепочка** — новая фича с октября 2025, дала +50% к объёму лидов в кейсе Refocus DE
- **Bothelp / Salebot** — для Telegram-специфичных воронок
- **Lovable / Base44** — для быстрого сбора лендинга под новую гипотезу (см. [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]])

Полный инвентарь воронок — в [[canon/marketing-frameworks/funnel-simplicity-principle]] и связанных страницах.

### 5. Автоматизировать аналитику до уровня «отчёт сразу с рекомендациями в Telegram»

- Агент на **n8n** (или Claude Code), который:
  - собирает метрики из Meta/Google/TikTok Ads через API
  - считает бенчмарки (средний CPL, ROAS, CVR)
  - прогоняет через LLM (Gemini, Claude) с ролью Senior Media Buyer
  - категоризирует креативы (HELL YES / YES / MAYBE / NOT REALLY / WE WASTED MONEY / INSUFFICIENT DATA)
  - пишет результаты в Google Sheets + отправляет отчёт в Telegram
- Конкретный рабочий пример (@solokumi пост 375, 2026-02-09) — [готовый workflow](https://n8n.io/workflows/10427-analyze-facebook-ads-and-send-insights-to-google-sheets-with-gemini-ai/)
- Ключевая черта: **не «аналитика», а «аналитика → действия»**. Отчёт бесполезен, пока не сопровождается actionable recommendations

### 6. Вайбкодить: Nano Banana, Midjourney, VEO3, Sora, Higgsfield, Cursor, Claude Code, Base44

- **Генерация визуала:** Nano Banana (default), Midjourney (стиль/бренд), Flux (текст на изображении), DALL-E 3 (прототипы)
- **Генерация видео:** VEO3/Higgsfield (default), Seedance 2.0 (массовые микро-истории), Runway (кино-камера), Kling 3.0 (face consistency), Sora 2 (диалоги + физика)
- **Агенты-парсеры:** Cursor + Claude Code + MCP Apify / Firecrawl / Exa.ai
- **Лендинги за 15 минут:** Base44, Lovable, Cursor + Claude Code (см. [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]])
- **Ассистенты:** Manus.ai для оркестрации задач

## Must-have агенты в команде маркетинга 2026

По опыту Kumar & Solo (@solokumi пост 357), минимальный набор агентов, который должен быть в любом AI-native маркетинге:

| Агент | Функция | Слой ([[canon/marketing-frameworks/multi-agent-marketing-org-principles\|принципы оркестрации]]) |
|---|---|---|
| **Агент анализа конкурентов** | Парсит сайты + креативы + лендинги конкурентов | Сенсор → Аналитик |
| **Агент-трендвотчер** | Парсит виральные видео, извлекает параметры, собирает тренды | Сенсор |
| **Агент генерации виральных видео** | Берёт тренды + продукт → готовый сценарий + промпты для VEO3/Higgsfield | Исполнитель (L2) |
| **База знаний о компании с внешним интерфейсом (через Cursor)** | Хранит JTBD, ICP, TOV, положения бренда, legal claims | Инфраструктура |
| **Агент-анализатор звонков** | 40–50 параметров оценки, инсайты для креосов | Сенсор → Аналитик |
| **Агент-аналитик кабинетов** | Ежедневный дайджест по рекламе + рекомендации | Аналитик → Исполнитель (L1) |
| **ИИ-ОКК (контроль качества сейлзов)** | Оценка звонков + динамика по менеджерам | Сенсор → Аналитик |
| **ИИ-тренер сейлзов** | Персонализированные ролевки | Исполнитель (L2) |
| **Manychat welcome-бот** | Квалификация каждого нового подписчика, посадка в CRM | Исполнитель (L0) |

## Update may 2026 — Andrew Ng про сжатие engineer:PM ratio

В апреле 2026 Бай Аннаков ([[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] пост 1723) пересказал лекцию Andrew Ng (осень 2025, Стэнфорд), где Ng зафиксировал **структурный сдвиг в org-design** AI-native команд:

> «**Соотношение инженеров к продактам сдвигается от классических 7:1 к 1:1, а может и даже перевернётся**».
>
> «Take the engineer, take the PM, and collapse them into a single human. Those engineers are the fastest moving people I'm seeing in Silicon Valley today».

Это applies к marketing-функции на следующем слое: **сжатие** marketer ↔ analyst ↔ AI-engineer ↔ producer в одного оператора. AI-native маркетолог 2026 = **полный operator**: JTBD-методолог + аналитик + content-producer + code-shipper (через vibecoding) + agent-orchestrator.

**Косвенное следствие для команды (по Robin-кейсу onsa).** Один из 7-1 ролей, который **точно не collapses в человеческого operator'а** — это **memory/context-keeper**. Onsa это решили через AI Chief of Staff (Robin, см. [[evolving/competitor-positioning/onsa-robin-ai-chief-of-staff]]): Robin копит team-context, достаёт когда нужно. Это **новая обязательная позиция в AI-native маркетинге 2026** — не «marketer», не «analyst», а **AI Chief of Staff команды**.

Дополнено в must-have таблицу выше:

| Агент | Функция | Обоснование добавления |
|---|---|---|
| **AI Chief of Staff (Robin-style)** | Утренний бриф + 2nd opinion на дизайн/аналитику + re-onboarding после отпуска + meeting notes с собственным мнением | Onsa подтвердили: **главное — что AI помнит**, не делает. Команда живёт в потоке, через неделю не помнят почему решили X. AI Chief of Staff копит контекст и достаёт |

Cross-link с [[canon/marketing-frameworks/multi-agent-marketing-org-principles]] и [[evolving/industry-trends/ai-native-company-architecture-2026]].

## Что происходит с рабочим местом человека

Повторяющиеся исполнительские задачи (настройка кабинетов, ручная оптимизация ставок, клепание отчётов в Excel, ответы в комментах) — **автоматизируются агентами уровней 0–1**. Человек остаётся как:

- **Оркестратор** (задающий цели, проверяющий confidence-scores)
- **Стратег** (определяющий воронку, выбирающий тестируемые гипотезы)
- **Методолог JTBD** (единственный источник правды о клиенте, который не галлюцинирует)
- **Ревьюер креативов** (red team, финальный human-in-the-loop)
- **Connectivity layer** (общение с людьми внутри компании, межкомандные согласования)

**Задачи уходят, навыки остаются** — но веса между ними перераспределяются. «Знать Facebook Ads Manager наизусть» теряет ценность, «уметь написать хороший CLAUDE.md» её приобретает.

## Параллель из engineering recruiting (май 2026)

[[sources/2026-05-14-tg-ai-newz-may-2026|@ai_newz пост 4568 (нативная реклама за рекрутинг-партнёра Mike Volkov)]] формулирует **зеркальный тезис для инженерии**, который один-в-один переносится на маркетинг:

> «Для кучи компаний это реальный блокер: AI adoption упирается **не в бюджеты и не в стратегию** — а в то, что текущая команда просто не умеет работать с агентным стеком на том уровне, который уже существует. Обычная реальность, про которую не принято говорить вслух.»

**Структурный сигнал для marketing-memory:**

1. **AI adoption bottleneck — это команда, не tech.** Это **независимое подтверждение** главного тезиса страницы: дефицит не в инструментах, не в моделях, не в бюджетах — а в **людях, умеющих оркестрировать стек на продакшен-уровне**.
2. **Делитель рынка.** Volkov эксплицитно делит candidates на две группы:
   - **«AI» в резюме = поставил Copilot и пишу промпты в ChatGPT»** — масса рынка
   - **Инженер со spec-driven pipeline, принудительным TDD через агентов, MCP-серверами, скиллами и автоматизацией** — единицы
   - **Пропасть между ними — структурная**, а не градуальная
3. **То же самое в маркетинге.** Маркетолог, поставивший ChatGPT и пишущий промпты, vs маркетолог с собственным `CLAUDE.md`, multi-agent pipeline, [[canon/marketing-frameworks/ai-video-production-pipeline|массовым креатив-производством]], spec-driven content workflow — это **разные категории работников**, не разные уровни одной шкалы.
4. **Hiring-pattern для маркетинга.** Если паттерн «специализированный рекрутер AI-native инженеров» становится отдельной нишей (Volkov), это **proof-point будущего тренда** — появятся специализированные AI-native маркетинг-рекрутеры. Это **новая HR-tech категория** для marketing-memory tracking.

**Готовый hook для GRO-контента:**

*«Когда-то ты выбирал маркетолога по знанию Facebook Ads. Сегодня — по тому, есть ли у него собственный CLAUDE.md в репозитории. Пропасть между двумя категориями — больше, чем кажется»*.

**Caveat:** этот пост — `#промо` native-ad, поэтому используется как **proof-point индустриального паттерна**, не как primary source для метрик. Сам факт того, что появилась специализированная рекрутинговая ниша, важнее конкретного кейса Volkov.

## Связь с другими страницами

- [[canon/marketing-frameworks/andromeda-creative-framework-2026]] — рамка, внутри которой живёт этот профиль навыков
- [[canon/marketing-frameworks/multi-agent-marketing-org-principles]] — архитектура многоагентных систем, которыми управляет этот маркетолог
- [[canon/marketing-frameworks/claude-md-structure-marketing]] — базовый инструмент воспроизводимой работы с Claude Code
- [[canon/marketing-frameworks/ai-video-production-pipeline]] — практика массового производства креативов
- [[evolving/content-trends/ai-video-tools-stack-2026]] — дрейфующий инструментальный стек
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]] — vibecoding-стек, в котором работает такой маркетолог
- [[evolving/industry-trends/ai-native-company-architecture-2026]] — более широкий взгляд на уровне всей компании
- [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]] — общий тренд смещения knowledge work к AI-native ролям
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — крайний вариант: тот же скиллсет, но в соло-режиме без команды
- [[sources/2026-05-14-tg-ai-newz-may-2026]] — независимое подтверждение тезиса из инженерии (Mike Volkov #промо 4568)
- [[evolving/competitor-positioning/onsa-robin-ai-chief-of-staff]] — Robin как референсный кейс AI Chief of Staff в команде
- [[canon/marketing-frameworks/karpathy-software-3-agentic-engineering]] — Software 3.0 как framework, под который сжимаются роли
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] — Andrew Ng 7:1 → 1:1 + Robin кейс

## Backlinks

_21 pages link to this one._

- [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]]
- [[canon/marketing-frameworks/andromeda-creative-framework-2026]]
- [[canon/marketing-frameworks/claude-md-structure-marketing]]
- [[canon/marketing-frameworks/claude-skills-architecture]]
- [[canon/marketing-frameworks/multi-agent-marketing-org-principles]]
- [[evolving-strict/market-data/ai-vendor-revenue-per-employee-2026]]
- [[evolving-strict/market-data/sourcecraft-developer-ai-shift-2026]]
- [[evolving-strict/product-metrics/refocus-germany-2026-growth]]
- [[evolving/competitor-positioning/claude-design-2026]]
- [[evolving/competitor-positioning/onsa-robin-ai-chief-of-staff]]
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]]
- [[evolving/content-trends/ai-content-production-multiagent-2026]]
- [[evolving/content-trends/ai-tools-self-hosting-arbitrage]]
- [[evolving/content-trends/ai-video-tools-stack-2026]]
- [[evolving/content-trends/sales-ops-ai-tooling-stack-2026]]
- [[evolving/content-trends/telegram-native-formats]]
- [[index]]
- [[sources/2026-04-14-tg-solokumi-nov2025-apr2026]]
- [[sources/2026-05-05-tg-cossaru-apr-24-may-5-2026]]
- [[sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026]]
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]]
