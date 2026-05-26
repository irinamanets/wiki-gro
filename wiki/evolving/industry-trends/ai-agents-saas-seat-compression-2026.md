---
id: mkt:evolving/industry-trends/ai-agents-saas-seat-compression-2026
title: "Сжатие per-seat SaaS под AI-агентами: −$285 млрд капитализации Q1 2026"
type: page
subtype: trend
layer: evolving
theme: industry-trends
tags: [ai-agents, saas, per-seat, agent-economy, capitalization, software-market, displacement, business-model]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-bezsmuzi-may-8-11-2026.md]
namespace: mkt
---

# Сжатие per-seat SaaS под AI-агентами: −$285 млрд капитализации Q1 2026

Структурный сдвиг 2026: **AI-агенты атакуют не должности, а business model SaaS** — per-seat-pricing разрывается, когда один агент делает работу за «пять подписок». Зафиксирован через цитирование Forbes Максимом Кульгиным ([[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026|пост 15968 от 2026-05-10]]).

`confidence: medium` — первичный источник (Forbes) указан опосредованно, retold one-voice. Цифры **очень характерные** (худший квартал со времён 2008), что повышает значимость, но требует первичной верификации перед использованием в strict-контенте.

## Тезис

Forbes (через Кульгина): **AI-агенты за квартал стерли ~$285 млрд капитализации SaaS-компаний** — «**худший квартал у софтверных акций со времён кризиса 2008 года**». `[conf:medium, src:2026-05-10]`

При этом **общие расходы бизнеса на софт не упали — выросли +15% до $1,4 трлн в 2026**. `[conf:medium, src:2026-05-10]` Деньги в индустрии есть; они перетекают **с per-seat SaaS на agent-tooling**.

Кульгин-формулировка (как operational tested-by-buying SMB-предпринимателя):

> «Если агент сам делает работу, за которую раньше сидели **пять человек с подписками**, то платить за пять мест уже странно. **Модель оплаты за каждого сотрудника начинает скрипеть.**»

## Структурная механика

| Старая модель (per-seat SaaS) | Новая модель (agent-priced) |
|---|---|
| Цена ∝ числу сотрудников | Цена ∝ outcome (задачи / транзакции / API-calls) |
| Apex: 5 сотрудников × $50/mo = $250/mo | 1 agent делает работу 5: $50–$200/mo за outcome |
| Vendor revenue растёт от роста штата клиента | Vendor revenue растёт от value, не от headcount |
| Защитный barrier: workflow lock-in | Защитный barrier: integration depth + data |
| Кризис 2026: −$285 млрд capitalization | Бенефициары: agent-platforms, vertical-AI |

## Связь с другими трендами

1. **[[evolving/industry-trends/open-extensible-saas-shift-2026|Сдвиг к открытому/расширяемому SaaS]]** (Морейнис 2026-05-18). Морейнис предлагает **defense**: закрытый SaaS умирает, расширяемый — выживает. Кульгин/Forbes фиксируют **симптом**: $285 млрд капитализации стёрты. Две стороны одной монеты.
2. **[[evolving/industry-trends/ai-agent-economy-2026|Экономика AI-агентов 2026]]** — agent-pricing infrastructure (Stripe MPP, webmcp) — то, **куда** перетекают $1,4 трлн расходов на софт.
3. **[[evolving/industry-trends/ai-replacing-jobs-global-2026|AI замещает позиции]]** — раньше это был job-replacement-нарратив. Теперь он расширяется до **SaaS-vendor replacement**: не «AI заменяет работника», а «agent заменяет 5 SaaS-подписок».
4. **[[evolving-strict/market-data/stack-overflow-ai-displacement-2026|Stack Overflow коллапс −78%]]** — micro-кейс той же логики на категории developer-tools.

## Per-seat пример: ChatGPT в Excel/Google Sheets

Пост 15971 (Кульгин): OpenAI встроил **GPT-5.5 в Excel и Google Sheets** через [chatgpt.com/ru-RU/apps/spreadsheets/](https://chatgpt.com/ru-RU/apps/spreadsheets/) — анализ неструктурированных данных, финансовые модели, генерация формул, обновление таблиц, трекеры расходов. Кульгин: «Аналитики рады или нет, ведь их нужно меньше теперь.»

**Per-seat последствие:** компания, у которой раньше было **5 аналитиков × $30 BI-подписка = $150/mo**, теперь может оставить 1 аналитика + ChatGPT-spreadsheet интеграцию, и аналитическая mощность растёт, а seat-revenue BI-вендора падает. См. также [[volatile-strict/competitor-news/chatgpt-in-spreadsheets-2026-05]].

## Что мониторить

- **Quarterly earnings calls** SaaS-вендоров (Salesforce, Workday, ServiceNow, Atlassian) — упоминания agent-erosion / pricing-model-shift.
- **Pricing announcements vendors**: переход от per-seat к outcome-based / usage-based.
- **Russian Tier-2 SaaS** (Bitrix24, amoCRM, Mango Office, Контур): когда они начнут anti-agent позиционирование или, наоборот, agent-bundle.
- **Re-verify Forbes-цифру** $285 млрд через первичный отчёт (Bloomberg / FT / market-cap baseline).

## Hooks для контента GRO

1. «$285 млрд capitalization стёрло за квартал — худший квартал SaaS со времён 2008.»
2. «Если агент делает работу пятерых, платить за пять seat-подписок — странно.»
3. «Бизнес тратит +15% на софт ($1,4 трлн), но **деньги текут не туда, куда раньше**.»
4. «Per-seat — это headcount-tax. Outcome-pricing — это value-tax. Угадайте, что выживет.»
5. «Аналитики теперь не нужны в количестве пяти — нужен один с ChatGPT в Excel.»

## Caveat'ы

- $285 млрд — retold через TG-канал, не verified от первичной Forbes-публикации (требует cross-check).
- «Худший квартал со времён 2008» — характеризация Forbes, не независимая аналитика.
- Тренд **молодой** (только Q1 2026), масштаб может измениться по мере того, как SaaS-вендоры переходят на hybrid-pricing.
- TTL 90 дней (volatile-strict pricing-сигнал внутри evolving-рамки). Re-verify не позднее 2026-08-25.

## Связанные страницы

- [[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026]] — источник-якорь
- [[evolving/industry-trends/ai-agent-economy-2026]] — куда текут деньги
- [[evolving/industry-trends/open-extensible-saas-shift-2026]] — defensive-сдвиг Морейниса
- [[evolving/industry-trends/ai-replacing-jobs-global-2026]] — родственный displacement-нарратив (jobs side)
- [[evolving-strict/market-data/stack-overflow-ai-displacement-2026]] — micro-proof-point на developer-tools
- [[volatile-strict/competitor-news/chatgpt-in-spreadsheets-2026-05]] — конкретный SaaS-erosion-кейс (BI/spreadsheet)
