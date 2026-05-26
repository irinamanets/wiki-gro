---
id: mkt:evolving-strict/market-data/stack-overflow-ai-displacement-2026
title: "Stack Overflow: −78% вопросов за год (3,8k vs 200k+ в мес) — proof-point AI-замены developer-search"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [stack-overflow, developer-tools, ai-displacement, search-shift, metric, dec-2025, llm-displacement]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-bezsmuzi-may-8-11-2026.md]
namespace: mkt
---

# Stack Overflow коллапс: −78% за год как proof-point AI-замены поиска [conf:low, src:2026-05-26]

Символический proof-point AI-displacement в developer-tools: культовая платформа для Q&A разработчиков **откатилась на уровень 2009 года** по объёму вопросов. Зафиксировано через [[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026|пост 15982 Максима Кульгина]] от 2026-05-10 с прикреплённым chart-скриншотом (img 15982).

`confidence: medium` — retold через TG-канал, первичная источника (Stack Overflow data dashboard / annual report) не указана в дампе. Сама цифра проверяется по публичному dashboard SO; тренд хорошо задокументирован в developer-community discourse с 2024.

## Ключевые цифры

| Метрика | Декабрь 2025 | Пик 2014 | Изменение | Source |
|---|---|---|---|---|
| Вопросов в месяц | **3 862** | **>200 000** | **−98% от пика** | `[conf:medium, src:2026-05-10]` |
| YoY (vs декабрь 2024) | 3 862 | ~17 000 | **−78%** | `[conf:medium, src:2026-05-10]` |
| Эквивалент уровня | — | — | Откат к **2009** году | `[conf:medium, src:2026-05-10]` |

Дельта 2014 → 2025: платформа теряет **~98% объёма** относительно пика. YoY −78% — это **ускорение коллапса**, а не плавная эрозия. Источник коллапса — **массовое замещение поиска ответов на LLM-чатах**. [conf:low, src:2026-05-26]

## Что говорит сам Кульгин

> «Я сам ловлю себя на том, что **не гуглю ничего уже полгода**. Сразу иду в ИИ.»

Это **personal proof-point** от operational founder'а, который сам построил несколько IT-бизнесов (clickfraud.ru, xmldatafeed.com, notissimus.com) — не theoretical-наблюдатель, а user-replacing-search-with-LLM на конкретных операционных задачах.

## Почему это важно для маркетинга

### 1. Strongest single-symbol для AI-displacement narrative

Stack Overflow в discourse — это **synecdoche developer-knowledge**. Когда «Stack Overflow откатился на уровень 2009» — это легко понимаемая метрика, которая работает в hook'ах и заголовках. Сравните:

- ❌ «LLM-системы вытесняют поисковые запросы технических Q&A» — концептуально, низкая retention.
- ✅ «**Stack Overflow откатился на уровень 2009 — все ушли в ChatGPT**» — конкретно, проверяемо, эмоционально.

### 2. Часть более широкого SEO-to-LLM shift

Связано с двумя соседними страницами:
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — общий сдвиг поискового слоя.
- [[evolving/content-trends/ai-text-detection-landscape-2026]] — AI-текст обнаружение.
- [[volatile/raw-notes/ru-platform-access-april-2026]] — RU-специфическая динамика доступа.

SEO-команды читают эту метрику как **«AEO/GEO — must, не optional»**: developer-аудитория **уже** ушла, обычные пользователи следуют.

### 3. Proof-point per-seat SaaS displacement

Связь с [[evolving/industry-trends/ai-agents-saas-seat-compression-2026|сжатием per-seat SaaS]]: Stack Overflow Teams (платный B2B-продукт SO) ровно та категория, которая страдает первой. **Платформа, чья value-prop = "developer-search", лишилась 98% search-объёма** — это структурный коллапс business-rationale, не циклическое падение. [conf:low, src:2026-05-26]

## Контент-применение

Hook-семейство для блога GRO / постов в TG:

1. «Stack Overflow откатился на уровень 2009 года. Не 2019, не 2015 — 2009. До того, как о нём узнали.»
2. «3 862 вопроса в декабре 2025. На пике 2014 было больше **200 000 в месяц**. Минус 98%.» [conf:low, src:2026-05-26]
3. «−78% за год — это не плавная эрозия, это коллапс. Поищите аналог в истории технологических платформ.» [conf:low, src:2026-05-26]
4. «Я не гуглю уже полгода. Сразу в ИИ.» — voice operational founder'а.

## Caveat'ы и оговоры

- Цифры **retold через TG-канал** — первичный источник (SO public data API / annual report / Stack Overflow blog) не указан Кульгиным. Перед strict-использованием в публикации — проверить через [data.stackexchange.com](https://data.stackexchange.com/) или [SO public dashboard](https://stackoverflow.com/).
- Декабрь — сезонно слабый месяц для SO; YoY сравнение валидно (декабрь к декабрю), но абсолютная цифра 3 862 может быть немного занижена сезонно.
- Тренд **может ускоряться** к 2026 (Cursor/Claude Code/Copilot extension всё больше). Re-verify в Q3 2026 — если будут <1 000 вопросов/мес, это перейдёт на уровень terminal-decline.
- TTL **90 дней** (evolving-strict). Re-verify не позднее **2026-08-25** с актуальными числами.

## Hooks для контента

- «−98% от пика. **Stack Overflow откатился на уровень 2009 — до того, как о нём узнали.**» `[conf:medium, src:2026-05-10]`
- «3 862 вопроса в декабре 2025 — против >200 тысяч на пике 2014.» `[conf:medium, src:2026-05-10]`
- «Если developer не пользуется SO — он не пользуется и поиском. Кто следующий?» `[conf:medium, src:2026-05-10]`

## Связанные страницы

- [[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026]] — источник-якорь
- [[evolving/industry-trends/ai-agents-saas-seat-compression-2026]] — родственный per-seat SaaS displacement
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — общий поисковый сдвиг
- [[evolving/industry-trends/ai-replacing-jobs-global-2026]] — родственный displacement-нарратив (jobs side)
- [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] — теоретическая рамка retrieval-сдвига
