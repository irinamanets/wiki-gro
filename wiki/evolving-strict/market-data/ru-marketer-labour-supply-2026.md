---
id: mkt:evolving-strict/market-data/ru-marketer-labour-supply-2026
title: "Рынок труда маркетологов РФ 2026 — overflow и compression"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [market-data, labor-market, marketing-jobs, ru, hr, ai-replacement]
confidence: medium
stale: false
created: 2026-05-06
updated: 2026-05-06
sources: [sources/2026-05-05-tg-petrochenkow-apr-may-2026.md]
namespace: mkt
---

# Рынок труда маркетологов РФ 2026 — overflow и compression

Срез сигналов о состоянии рынка труда маркетологов в РФ на апрель 2026: переход от острого дефицита (2021) к острому overflow (2026), причины и implications.

## Ключевая метрика

| Показатель | Значение | Контекст | Source |
|---|---|---|---|
| Кандидатов на 1 вакансию маркетолога РФ 2026 | **12** | RBC «Продавцы воздуха» | `[conf:medium, src:2026-04-24]` |
| Кандидатов на 1 вакансию маркетолога РФ 2021 | востребованы наравне с опытными программистами (точные числа в RBC не приведены) | до сжатия | `[conf:medium, src:2026-04-24]` |

`[conf:medium, src:2026-04-24]` — RBC агрегирует данные с HH.ru / других job-площадок, не первичный recruitment-data, через перепост в TG-канале Petrochenkov.

## Заголовок RBC (2026-04-24)

> **Продавцы воздуха. Почему спрос на маркетологов в России рекордно упал.**
>
> Маркетолог — одна из самых пострадавших за последние годы профессий. В 2021 году они были востребованы наравне с опытными программистами, **а теперь на каждую вакансию претендуют 12 человек**. Почему модные специалисты вдруг оказались не нужны?

`[conf:medium, src:2026-04-24]` (RBC через перепост Petrochenkov #1267)

## Причины overflow (combined evidence)

### Cause 1. AI-частичная замена

Petrochenkov ([[evolving/industry-trends/ai-marketing-limits-2026]]): ИИ-агенты неплохо делают **парсинг и работа с базами лидов, первичную квалификацию, структурирование рекламы, работу с семантикой, анализ резюме, контент-идеи, BI-дашборды**. Это **junior/middle-маркетолог tasks**.

Если 60% задач middle-маркетолога автоматизируется → одной senior-командой и парой джунов компании справляются с тем, на что раньше уходило 5-7 маркетологов. Рынок всасывает в overflow всех, кого «потеряли» компании. `[conf:low, src:2026-04-24]` (estimate, не measured)

### Cause 2. Регуляторное давление на digital-каналы

[[evolving/industry-trends/ru-digital-regulatory-squeeze-2026]] — ad-блокировки + ФЗ-168 + white-list-угрозы — заставляют SMB сокращать маркетинговые бюджеты. **Меньше бюджет → меньше команда → больше уволенных в overflow.**

### Cause 3. Демпинг от инфо-курсов

[[evolving/industry-trends/ai-marketing-limits-2026]] + Petrochenkov-formulation: «ИИ-маркетолог = газонокосилка для лохов». Тысячи курсов «как стать маркетологом за 2 месяца» (2020-2024) выпустили **большой пул junior-кандидатов** без production-опыта. Они в overflow в первую очередь.

### Cause 4. Падение покупательской активности

[[evolving/industry-trends/ru-smb-sales-q1-2026]] + boli-карта собственников ([[evolving/customer-feedback/ru-smb-owner-pains-2026]]) — SMB-собственники в режиме «сохранить то, что есть» (4-я боль), не «нанять новых маркетологов».

### Cause 5. AI-cheating discount

[[evolving/industry-trends/ai-cheat-interview-pattern-2026]] — массовый AI-cheating на интервью **обесценивает** значимую часть кандидатов. Работодатели разочаровываются, расширяют requirements, что снижает скорость найма и копит overflow.

## Implications для маркетингового сектора

### Для собственника / hiring manager

- **Filter discipline.** При 12 кандидатах на вакансию можно (и нужно) фильтровать жёстко. Petrochenkov-метод (3 диагностических вопроса + AI-cheating защита) — relevant больше чем когда-либо. См. [[canon/marketing-frameworks/marketer-hiring-questions]] + [[evolving/industry-trends/ai-cheat-interview-pattern-2026]].
- **Зарплатное снижение.** При overflow зарплаты middle-маркетолога должны снизиться. Но: senior-маркетологи (с production-опытом, AI-augmented) **остаются дефицитными** — bipolar рынок.
- **AI-augmentation strategy.** Нанимать одного senior + AI-tools вместо команды из 5 middle. Это эффективнее в overflow-режиме.

### Для кандидата

- **Junior-уровень — критически overcrowded.** Прорыв через сертификаты «прошёл курс маркетинга» больше не работает.
- **Production-portfolio решает.** Реальные кейсы с цифрами (CR из X в Y, бюджет такой-то, ROI такой-то) — единственный отличающий фактор.
- **AI-augmented profile.** Не «знаю Я.Директ», а «использую Notebook LM + Gemini + n8n для оптимизации Я.Директ в production». Двукратная компетенция.
- **Niche-специализация.** Generalist-маркетолог — массовая категория overflow. Niche (B2B-промышленность, медицина, EdTech) — меньше overflow.

### Для маркетингового продукта (B2B SaaS типа GRO)

- **Customer-base shifts.** SMB-маркетологи в overflow становятся фрилансерами, ищут tools. Средний LTV-pattern клиента изменяется.
- **Tone of voice.** «Замени отдел маркетинга AI» — не работает в 2026, потому что overflow + 5 болей собственника не про **замену**, а про **доверие**. AI-co-pilot framing работает.
- **Pricing.** При боли «сохранить то, что есть» (#4) и «не на кого положиться» (#2) — premium-tier плохо продаётся, low-cost-tier хорошо. Но не «бесплатно» (Petrochenkov: 1500₽/мес как референс качественной курса). `[conf:low, src:2026-04-30]`

## Контекст vs. соседние источники

- **HH.ru data.** Conventional unemployment data РФ — overflow на маркетинг был фиксируется и в данных HH.ru (см. [[evolving-strict/market-data/ru-hiring-cost-benchmarks-2026]] и [[evolving-strict/market-data/hh-automation-survey-2026]]).
- **Anthropic data.** Глобальные данные [[evolving-strict/market-data/ai-labor-market-anthropic-2026]] показывают **AI как knowledge-worker pacer**, что correlates с RU-картиной.
- **Convert Monster source.** Petrochenkov по своим клиентам видит то же самое: SMB-собственники не ищут «нового маркетолога», ищут **«как обойтись текущим»**.

## Что НЕ известно (gaps)

- **Точные зарплатные benchmarks** middle vs. senior маркетолога РФ 2026 — RBC и Petrochenkov не приводят.
- **Региональная разбивка.** Москва/Питер/regions — разные картины.
- **Sub-категории маркетинга.** Performance-marketers vs. brand-marketers vs. content-marketers могут иметь разные overflow-rates.
- **Trajectory.** При AI-tools зрелости в 2027-2028 — overflow углубится или скомпенсируется новыми ролями (AI-marketing-engineer)?

## Связь с другими страницами

- [[evolving/industry-trends/ru-marketing-digital-paralysis-mar2026]] — широкая картина digital-проблем 2026 в РФ.
- [[evolving/industry-trends/ai-marketing-limits-2026]] — что AI делает / не делает в маркетинге → causes overflow.
- [[evolving/industry-trends/ai-cheat-interview-pattern-2026]] — AI-cheating усугубляет overflow-discount.
- [[evolving/customer-feedback/ru-smb-owner-pains-2026]] — собственники не нанимают, потому что 5 других болей.
- [[evolving/industry-trends/hiring-trends-russia-2026]] — общая RU-recruitment картина.
- [[canon/marketing-frameworks/marketer-hiring-questions]] — defense-protocol для собственника при overflow.

## См. также

- [[sources/2026-05-05-tg-petrochenkow-apr-may-2026]] — первоисточник (пост 1267, скриншот RBC, 2026-04-24)

## Backlinks

_8 pages link to this one._

- [[canon/marketing-frameworks/marketer-hiring-questions]]
- [[evolving-strict/market-data/ru-self-employed-2025]]
- [[evolving/industry-trends/ai-cheat-interview-pattern-2026]]
- [[evolving/industry-trends/ai-marketing-limits-2026]]
- [[evolving/industry-trends/ru-marketing-digital-paralysis-mar2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-petrochenkow-apr-may-2026]]
