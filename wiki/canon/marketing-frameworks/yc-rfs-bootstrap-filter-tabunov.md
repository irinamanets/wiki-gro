---
id: mkt:canon/marketing-frameworks/yc-rfs-bootstrap-filter-tabunov
title: "YC RFS bootstrap-filter — методика разбора Request for Startups для соло-фаундера (Табунов)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [y-combinator, rfs, bootstrap, idea-filtering, founder-mindset, solopreneurship, awareness]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-your-pet-project-may-20-25-2026.md]
namespace: mkt
---

# YC RFS bootstrap-filter

Reusable рамка для **разбора любого Request for Startups** (YC, A16z, Sequoia, Hustle Fund, или внутренний listing) с точки зрения **bootstrapped solo-фаундера**. Канонически зафиксирована Михаилом Табуновым в разборе YC Summer 2026 RFS ([[sources/2026-05-26-tg-your-pet-project-may-20-25-2026]] пост 635, 2026-05-21): из 15 YC-идей прошли фильтр **4 (≈27%)**, остальные 11 идей — VC-приемлемые, но **operationally unsuitable** для bootstrap.

`confidence: medium`: эксперт-inferred (Табунов как founder Baza Education, 2 года public-content про solopreneur paths). Методика — операционально-применима к любому RFS, не только к YC. Списочный анализ конкретных 15 YC-идей и distinction «горизонт 2030 (VC) vs горизонт сегодня (bootstrap)» — субъективные founder-voice оценки, переносимы на другие RFS с adaptation.

## Главный тезис

> «YC инвестирует на десять лет вперёд. Они могут вложиться во что-то, что залетит в 2030. А нам-то нужно что-то, где **платят уже сегодня**.»

VC-RFS оптимизирован под идеи с **большим TAM в горизонте 5-10 лет** и **высоким технологическим barrier-to-entry** (защита моата). Bootstrap-фаундер оптимизирован под идеи с **немедленным спросом** и **низким технологическим barrier-to-entry** (быстрый запуск). **Эти оптимизации почти ортогональны** → ≈70-80% VC-RFS идей не подходят bootstrap-фаундеру.

## Методика фильтрации (4 операционных критерия)

Применяется к каждому пункту RFS:

| # | Критерий | Что отсекает | Конкретный пример из YC SU26 |
|---|---|---|---|
| 1 | **Спрос есть прямо сейчас?** | Идеи, рассчитанные на «созревание рынка» через 3-5+ лет | Dynamic Software Interfaces — «платить будут через пару лет» |
| 2 | **Нет ли тяжёлых капитальных вложений?** | R&D-heavy, hardware, infrastructure, regulatory | Electronics in Space, Inference Chips for Agent Workflows, Supply Chain 2.0 for Semiconductors |
| 3 | **Не требует ли регуляторных согласований до первой продажи?** | Healthcare/finance/defense | AI Personalized Medicine (FDA), Counter-Swarm Defense |
| 4 | **Можно ли продавать SMB / индивидам, а не F100?** | Enterprise-sales-only идеи | Startups That Sell to Huge Companies, SaaS Challengers (ERP, чип-софт) |

**Disqualifier-логика:** если идея **проваливает хотя бы один** критерий → она не для bootstrap-фаундера. YC может в неё инвестировать, но соло-фаундер с подпиской на Claude и парой выходных её не запустит.

**Negative space-проверка:** если осталось >50% идей — критерии **слишком мягкие**, нужно ужесточить. У Табунова на YC SU26 прошли 4/15 ≈ 27% — это **здоровый** filtering ratio для VC-RFS.

## Анатомия проходящих идей (паттерн)

4 идеи, прошедшие фильтр Табунова, объединяет общий паттерн:

**Все 4 = AI-агентская инфраструктура для одной из ролей:**

| Идея YC SU26 | Кто платит сегодня | Bootstrap-механика |
|---|---|---|
| AI-Native Service Companies | Малый/средний бизнес | Один фаундер с подпиской на Claude = маркетинговое агентство |
| Software for Agents | Solo-разработчики агентов | MCP-обёртки, инструменты на $100-300/мес каждый |
| Company Brain | Любая компания с >5 сотрудниками | AI-first knowledge management |
| The AI Operating System for Companies | Те же | «Аналог Notion навайбкодить может любой» |

Общий характеристический шаблон:
- **Платит — другой solopreneur или маленькая команда** (peer-bootstrap economy, не enterprise).
- **Решение — обёртка над существующим foundation model** (Claude / GPT / Gemini), не fundamental innovation.
- **Запуск — 1-2 уикэнда** (см. [[canon/marketing-frameworks/five-no-pet-project-tabunov]] правило #4).
- **Цена — $99-300/мес** (см. [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] — попадает в agent-pricing коридор, не enterprise).

## Стратегическое наблюдение: VC-bootstrap arbitrage

Существование такого filtering-pattern'а — само по себе **рыночный сигнал**: **VC и solopreneur-сообщества оптимизируются в разных направлениях**, и пересечение между ними становится тоньше.

**Operational implication:** для bootstrap-фаундера **YC RFS = полезный inventory сигналов будущего спроса**, но **не roadmap для запуска**. Использовать как «список тем, которые будут на гребне в 2028-2030, чтобы решить, какую упрощённую SMB-версию запустить сегодня».

**Пример reasoning:**
- YC: «AI Personalized Medicine» (большой долгий рынок)
- Bootstrap: «AI-ассистент для нутрициологов-фрилансеров» (та же тема, но SMB-аватар, без FDA, $99/мес)

## Применение к GRO

GRO **не пишет RFS**, но 4 YC-категории, прошедшие фильтр Табунова, **прямо относятся к ЦА GRO**:

- **AI-Native Service Companies** = под-аудитория [[canon/target-audience/gro-segments|Сегмента 3 «фрилансеры»]] — solopreneur'ы, выходящие на «маркетинговое агентство из одного человека». GRO релевантен как **slой системности над хаосом операционки** (см. content-angle «хаос в операционке» в Сегменте 2).
- **Software for Agents** = под-аудитория [[canon/target-audience/gro-segments|Сегмента 2 «предприниматели в росте»]] и Сегмента 3, кто строит свои AI-агенты. GRO релевантен как **дисциплина пет-проекта** на фоне их основного направления.
- **Company Brain / AI OS for Companies** = смежные ниши, в которых GRO может **позиционироваться через partnerships** (например, GRO как «knowledge layer» внутри AI-OS-проектов от bootstrap-фаундеров).

## Hooks для контента GRO

| Стадия воронки | Hook | Сегмент |
|---|---|---|
| Awareness | «YC инвестирует на 10 лет вперёд. Тебе нужно, чтобы платили сегодня.» | Предприниматели, фрилансеры |
| Awareness | «Из 15 YC-идей для bootstrap-фаундера годится 4. Остальные — для тех, кто умеет питчить инвесторов.» | Предприниматели |
| Consideration | «Космос, регуляторика, F100-клиенты, hardware — это не для пет-проекта по выходным.» | Карьеристы с side-project дилеммой |
| Consideration | «AI-агентство из одного человека. Software for agents. Company Brain. AI OS для компаний. 4 категории, где платят сегодня.» | Предприниматели на пред-запуске |
| Decision | «Пока стартаперы 2 года питчат убыточный проект, ты за выходные навайбкодишь простой инструмент в одной из этих ниш. И начнёшь получать оплаты через пару месяцев.» | Предприниматели + фрилансеры |

## Anti-pattern: «фильтрация для оправдания»

Главная ловушка применения рамки: использовать фильтр **не для отбора**, а для **оправдания нежелания запускать вообще**. Симптомы:

- Прогоняешь RFS через фильтр → ни одна идея не подходит → «значит, рынок сейчас не для меня» → откладываешь запуск.
- Применяешь фильтр **слишком жёстко** (5-6 критериев вместо 4) → отсев 100% → паралич.

**Контр-мера:** фильтр — это **отсев заведомо неподходящего**, а не **поиск идеального**. Если ≥3 идей прошли фильтр → выбирай самую близкую к твоей экспертизе и запускайся. Не пытайся найти «ту самую» — иначе попадёшь в anti-pattern из [[canon/marketing-frameworks/founder-vs-passerby-mindset-tabunov]] («прохожий ищет ту самую идею, фаундер запускает что есть»).

## Связанные страницы

- [[canon/marketing-frameworks/founder-vs-passerby-mindset-tabunov]] — анти-pattern «прохожий ищет ту самую идею» — родственная рамка
- [[canon/marketing-frameworks/five-no-pet-project-tabunov]] — operational disqualifiers, дополнительный фильтр на отобранные идеи
- [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] — корневая парадигма: bootstrap живёт на деньги клиента, VC — на деньги инвестора, разные timelines
- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] — все 4 прошедшие идеи попадают в agent-pricing коридор $99-300/мес
- [[canon/marketing-frameworks/zero-to-one-vs-scale-tabunov]] — bootstrap-фаундер работает в zero-to-one, не имеет ресурсов на капитальный scale
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — все 4 прошедшие идеи — про AI-агентскую инфраструктуру, что укладывается в макро-тренд
- [[evolving/industry-trends/agent-first-world-openclaw-2026]] — параллельный сигнал про инфраструктурный gap для agent-builder'ов (OpenClaw как пример)
- [[canon/target-audience/gro-segments]] — соответствие YC-категорий сегментам GRO ЦА
- [[evolving/content-trends/your-pet-project-channel-hooks]] — host для hook'ов
- [[sources/2026-05-26-tg-your-pet-project-may-20-25-2026]] — первоисточник (пост 635)
