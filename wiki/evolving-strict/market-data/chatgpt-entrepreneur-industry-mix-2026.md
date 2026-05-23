---
id: mkt:evolving-strict/market-data/chatgpt-entrepreneur-industry-mix-2026
title: Industry-mix предпринимателей в ChatGPT — a16z / OpenAI, март 2026
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ai, market-data, target-audience, awareness, content]
confidence: high
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-temno-moreynis-may-14-19-2026.md]
namespace: mkt
---

# Industry-mix предпринимателей в ChatGPT (a16z / OpenAI, март 2026)

Численный срез того, **предприниматели каких индустрий чаще всего используют ChatGPT** для предпринимательских задач. Данные a16z, построенные на отчёте OpenAI «How People Use ChatGPT» (March 2026). В marketing-memory попали через [[sources/2026-05-19-tg-temno-moreynis-may-14-19-2026|дайджест @temno]] (Морейнис встроил a16z-карточку в пост 7834). Страница в `evolving-strict/market-data`, потому что это **датированный численный замер**, который устаревает с выходом новых отчётов OpenAI/a16z (TTL 180 дней) и требует audit-trail на каждое число.

## Базовые цифры

- Выборка: **~4 млн** US-пользователей ChatGPT, отправляющих entrepreneurial-сообщения (анонимный сэмпл Free/Plus/Pro/Go). `[conf:high, src:2026-05-14]`
- **Active-когорта: 71%** (≈2,84 млн человек). `[conf:high, src:2026-05-14]`
- **Prospective-когорта: 29%** (≈1,16 млн человек). `[conf:high, src:2026-05-14]`

Active = уже ведут деятельность; Prospective = присматриваются/планируют. Каждый прямоугольник на исходной marimekko сайзится по доле в своей когорте.

## Industry-mix по когортам

Доли когорт: Active 71%, Prospective 29% (см. «Базовые цифры» выше). `[conf:high, src:2026-05-14]`

| Индустрия | Active-доля | Prospective-доля | Source |
|---|---|---|---|
| Professional & agency services (консалтинг, бухгалтерия, агентства) | 22% | 20% | `[conf:high, src:2026-05-14]` |
| Retail / ecommerce brand | 21% | 27% | `[conf:high, src:2026-05-14]` |
| Home / trade services (ремонт, обслуживание оборудования) | 18% | 12% | `[conf:high, src:2026-05-14]` |
| Health / beauty practice | 11% | 6% | `[conf:high, src:2026-05-14]` |
| Other | 10% | 8% | `[conf:high, src:2026-05-14]` |
| Food / hospitality | 8% | 9% | `[conf:high, src:2026-05-14]` |
| Tech startup | 5% | 13% | `[conf:high, src:2026-05-14]` |
| Property | 5% | 5% | `[conf:high, src:2026-05-14]` |

## Главный сигнал для маркетинга

**Tech-предприниматели — меньшинство среди тех, кто задаёт ИИ предпринимательские вопросы.** В Active-когорте tech startup = 5%, тогда как professional services + retail/ecommerce = 43% (×8,6 от tech). Морейнис формулирует это как «опережают в 4 раза с лишним» по числу задающих предпринимательские вопросы. `[conf:medium, src:2026-05-14]` — это retell-формулировка автора, точная база сравнения не специфицирована; верифицированные доли в таблице выше точнее.

**Интерпретация Морейниса (мнение, не данные):** tech-предприниматели задают ИИ технические, но не предпринимательские вопросы — либо считают техническую часть важнее, либо ищут «сложных людей со сложными ответами». `[conf:low, src:2026-05-14]` — субъективная гипотеза автора.

**Prospective → Active дрейф.** Tech startup проседает с 13% (Prospective) до 5% (Active) — самый сильный отток когорты. `[conf:high, src:2026-05-14]` Retail/ecommerce наоборот лидирует среди Prospective (27%). `[conf:high, src:2026-05-14]` Это сигнал, что **non-tech предприниматели лучше конвертируются из «присматриваются» в «уже делают»** с ИИ — практический довод для vertical-niche позиционирования (см. ниже).

## Маркетинговые выводы

1. **Data-anchor для vertical-niche тезиса.** Цифры — эмпирическое подтверждение [[canon/marketing-frameworks/sell-the-answer-not-platform-moreynis|тезиса «продавай ответ на проф. вопрос»]]: массовый ИИ-предприниматель — это бухгалтер, ритейлер, мастер-ремонтник, бьюти-мастер, а не tech-founder. Продукт «для всех» промахивается по реальному составу аудитории.
2. **Сегментация ЦА GRO.** Если GRO таргетирует предпринимателей (см. [[canon/target-audience/gro-segments]]), реальный профиль — non-tech SMB-владелец сервисной/розничной ниши, а не «техностартапер». Подтверждает [[canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis|правило 5 (SMB lifestyle)]].
3. **Готовый content-anchor.** Конкретная инфографика a16z с источником OpenAI — сильный proof-point для постов GRO про «кто реально использует ИИ в бизнесе» (awareness-контент).

## TTL и supersession watch

- `evolving-strict`, TTL 180 дней. Перепроверить осенью 2026 — OpenAI/a16z выпускают usage-отчёты регулярно, доли сместятся.
- При появлении RU-эквивалента (Яндекс/GigaChat usage по индустриям) — добавить как отдельный замер и кросс-сравнить (US-mix не переносится на РФ напрямую).

## Cross-links
- [[canon/marketing-frameworks/sell-the-answer-not-platform-moreynis]] — vertical-niche positioning, для которого это data-anchor
- [[canon/target-audience/gro-segments]] — сегменты ЦА GRO, которые этот замер уточняет
- [[canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis]] — правило 5 (SMB), подтверждаемое составом аудитории
- [[evolving/industry-trends/ru-vertical-ai-signals-2026]] — RU-вертикальные ИИ-сигналы (контраст US-mix)
- [[sources/2026-05-19-tg-temno-moreynis-may-14-19-2026]] — источник (пост 7834)
