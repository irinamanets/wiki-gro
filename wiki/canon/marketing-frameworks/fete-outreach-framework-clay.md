---
id: mkt:canon/marketing-frameworks/fete-outreach-framework-clay
title: "FETE-фреймворк: Find → Enrich → Transform → Export (AI-персонализированный outbound)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [sales-ops, ai, outreach, lead-generation, clay, claygent, fete-framework, b2b, cold-email, personalization]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-solokumi-may-2026.md, sources/2026-05-14-tg-startupoftheday-may-5-13-2026.md]
namespace: mkt
---

# FETE-фреймворк — Find → Enrich → Transform → Export

Каноническая четырёхшаговая методология построения AI-персонализированного outbound-процесса. Зафиксирована Романом Кумар Виасом ([@solokumi](https://t.me/solokumi)) на основе практики использования платформы Clay в Refocus и других проектах. Применима к любому B2B-сегменту: SaaS-продажи, корп-аутрич, агентский outreach, продажа консалтинга.

**Почему canon** — это **процессный фреймворк** (как AIDA или JTBD), а не конкретный инструмент. Стек инструментов под FETE дрейфует (Clay сегодня, что-то другое завтра — отдельные тулзы трекаются в [[evolving/content-trends/sales-ops-ai-tooling-stack-2026]]). Сам же четырёхшаговый паттерн стабилен.

## Контекст проблемы

Большинство фаундеров и маркетологов запускают outbound в лоб:

1. Выгружают базу откуда-нибудь / парсят LinkedIn
2. Добавляют `{First_Name}` в начало письма
3. Нажимают «Отправить»

Результат — **1.1% response rate**, демотивация, забрасывают канал. FETE — это **системная замена** этому паттерну, дающая **рост до 4%+** за счёт AI-агентов, которые делают per-lead research, который раньше требовал человека-аналитика.

## Четыре шага FETE

### F — Find

Загрузка списка лидов из любого источника:

- **Apollo / LinkedIn Sales Navigator** — основные источники для глобал-аутрича
- **Hunter** — email-лукапы
- **CSV-табличка** — если уже есть готовый список
- **Outbound-парсер** — собственный краулер LinkedIn / sales nav

На этом шаге собирается «сырой» список лидов с минимальными полями (имя, компания, должность). Никакой персонализации пока — просто база.

### E — Enrich

По каждому лиду одновременно запрашиваются данные из нескольких баз:

- **Должность и история** — из LinkedIn
- **Email** — из Hunter / Apollo
- **Стек технологий компании** — из BuiltWith / Wappalyzer
- **Свежие новости о компании** — из Google News
- **Финансовая информация** — из Crunchbase / PitchBook (для US/EU) или Контур.Фокус / Dadata (для RU)
- **Найм-сигналы** — из открытых job-постов компании

Цель этого шага — **уплотнить контекст** перед тем, как агент будет писать сообщение. Чем больше сигналов, тем точнее персонализация.

### T — Transform

Здесь подключается **AI-агент с веб-браузером** (Claygent в Clay, аналоги — собственная связка n8n + Browse-Use / Browser MCP / Playwright + LLM). Задаётся **один промпт**, агент сам ходит по сайтам каждого лида и пишет персонализацию.

**Базовый промпт «свежий контент»**:

```
Visit {company_website}. Find the most recent blog post, case study,
or news from the last 90 days. Write one sentence (max 20 words)
to use as an opening line in a cold email referencing this specific content.
Write in English.
```

**Усиленный промпт «найди боль клиентов»** (даёт ещё более точный заход):

```
Search for recent reviews of {company_name} on G2 or Trustpilot.
Find 1-2 specific pain points mentioned by their customers.
Write one sentence referencing this pain and connecting it to a solution.
Max 20 words.
```

На выходе — **N разных хуков** для N лидов. Это и есть рост с 1.1% до 4%+ — каждое письмо реально про получателя, а не про массив.

### E — Export

Готовый список с персонализацией отправляется в инструмент рассылки:

- **Instantly / Smartlead / Lemlist** — outbound-платформы с дроп-лимитами и тротлингом
- **CRM напрямую** (HubSpot, Pipedrive, AmoCRM) — если SDR будет писать вручную
- **Unisender / SendGrid** — для российского контура

После Export процесс зацикливается: replies → CRM → next touch с новой персонализацией.

## Ключевые метрики

- **Шаблонный outreach**: 1.1% response rate `[conf:high, src:2026-05-05]`
- **FETE через Clay/Claygent**: 4%+ response rate `[conf:high, src:2026-05-05]`
- **Время первой настройки полного флоу**: 3–4 часа `[conf:medium, src:2026-05-05]`
- **Clay интеграции для Enrich-шага**: 150+ источников данных `[conf:high, src:2026-05-05]`

## Где это ломается

> «AI-outreach распознаётся всё лучше, если промптец слабый — письмо получается слоповым, и получатель это чувствует.»
>
> — Р. Кумар Виас, @solokumi пост 403, 2026-05-05

Ограничения FETE:

1. **Слабый промпт = AI-слоп**. Если промпт generic — получатели за версту видят шаблонный AI-выход и игнорируют. Промпты на Transform-шаге требуют итерации.
2. **Анти-bot защита**. G2 / Trustpilot и часть сайтов уже ставят CAPTCHA на агентов. Claygent обходит часть, но не всё.
3. **Per-token cost не нулевой**. На 10К лидов Transform-шаг может стоить сотни долларов. Оптимизация — фильтровать лиды перед Transform (только ICP, не «всё подряд»).
4. **Регуляторика**. GDPR / CCPA / 152-ФЗ требуют согласия для холодных рассылок в части юрисдикций — FETE не освобождает от правового слоя.

## Анти-паттерн: full-automation

Виас явно предупреждает: **полностью автоматизировать FETE — рискованно**. Работает **комбинированный** подход:

- **AI — на массовых задачах**: Enrich, валидация, первичная персонализация (Transform-prompt в один проход).
- **Человек — на контроле и решениях**: финальный отбор лидов (top-priority), ручные письма под топ-аккаунты, ответы на replies.

Эта рамка перекликается с [[canon/marketing-frameworks/ai-personalization-4-layer-architecture]] — оба фреймворка отказываются от утопии «full agentic loop» и фиксируют human-on-the-loop как permanent invariant.

## Альтернативный стек для русскоязычного рынка

Clay стоит дорого и оптимизирован под глобальный рынок. Виас приводит **функциональный эквивалент** для RU-сегмента, в 5–10 раз дешевле `[conf:medium, src:2026-05-05]`:

| Шаг FETE | Clay (глобал) | Российский стек |
|---|---|---|
| Find | Apollo / LinkedIn Sales Nav | Dadata (реквизиты и выручка по ИНН, 10К запросов/день бесплатно) |
| Enrich | Hunter / BuiltWith / Google News | Контур.Фокус API (финансы + связи юрлиц), СБИС (контакты юрлиц), **DaData «Бренд по ИНН»** (AI-описание бизнеса по ИНН) |
| Transform | Claygent | n8n + Claude / GPT через API (промпт-агент пишет письмо) |
| Export | Instantly / Smartlead / Lemlist | Unisender / SendPulse |

**Trade-off**: 5–10x дешевле, но нужен **интегратор** (n8n flow, API-ключи, prompt engineering). Это не plug-and-play — это сборка под себя на 1–2 недели работы.

### Update 2026-05-14: DaData «Бренд по ИНН» как RU E-tool

К существующему RU-стеку Enrich-этапа добавлен **DaData «Бренд по ИНН»** (https://dadata.ru/product/find-brand/) — суб-продукт HFLabs/DaData, который **специально под FETE-сценарий**:

- **Вход:** ИНН организации (batch через API)
- **Выход:** коммерческое название («Ozon» вместо «ООО „Интернет Решения"»), AI-описание бизнеса (выжимка с сайта компании через нейросеть, не ОКВЭД), сайт, лого
- **Pricing:** бесплатно для первых 50 юрлиц (lead-magnet)
- **Контекст использования:** прямо подтверждает FETE-workflow — описания бизнеса используются для **обучения нейросеток сегментации лидов и составления персонализированных писем** (Transform-этап получает rich input)

См. [[evolving/competitor-positioning/dadata-brand-by-inn-ru-sales-enrichment-2026]] для подробного разбора продукта и сегмента.

Это **important addition к RU-стеку**: DaData не заменяет Контур.Фокус / СБИС (они дают финансы и связи юрлиц), а **дополняет** их AI-обогащённым описанием бизнеса — то, что в Clay делает Claygent через web-scraping, в RU-стеке делает DaData нативно через ИНН-anchor.

## Связь с другими фреймворками

- [[evolving/content-trends/sales-ops-ai-tooling-stack-2026]] — дрейфующий каталог конкретных тулз для каждого шага FETE
- [[canon/marketing-frameworks/ai-personalization-4-layer-architecture]] — упорная человеко-AI композиция как принцип (FETE — частный случай для outbound)
- [[canon/marketing-frameworks/multi-agent-marketing-org-principles]] — FETE — пример operating model с AI-агентами на operational-слое и людьми на стратегическом
- [[canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis]] — соседний B2B-фреймворк, у Морейниса акцент на discovery-call, у FETE — на pre-call outbound
- [[canon/marketing-frameworks/paid-demo-cold-outreach-thesis-gorny]] — companion counter-thesis (Горный): «платить адресату за demo, отсекая халявщиков»
- [[evolving/competitor-positioning/dadata-brand-by-inn-ru-sales-enrichment-2026]] — RU E-tool, добавленный в стек 2026-05-14

## Sources

- [[sources/2026-05-14-tg-solokumi-may-2026]] — пост 403 от 2026-05-05 (изначальная формулировка FETE Виасом)
- [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]] — DaData «Бренд по ИНН» как RU E-tool (пост 5065)
