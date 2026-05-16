---
id: mkt:evolving/content-trends/ru-personal-finance-listicle-baseline-2016
title: "RU SMB personal-finance tooling — historical content-baseline ~2016 (Жажда листикл)"
type: page
subtype: insight
layer: evolving
theme: content-trends
tags: [content-trends, historical-baseline, smb, ru, fintech, budgeting, listicle, pre-ai-era, zhazhda]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-zhazhda-budget-apps-evergreen-2016.md]
namespace: mkt
---

# RU SMB personal-finance tooling — historical content-baseline ~2016

**Что это:** snapshot редакционно-нормативного среза RU SMB-personal-finance-tooling-landscape образца ~2016 года, зафиксированный в анонимном evergreen-листикле Жажды «Программы и сервисы для ведения бюджета» ([[sources/2026-05-14-zhazhda-budget-apps-evergreen-2016]]). Hand-pick'нутые редакцией 10 продуктов отражают, **как тогдашний издатель для SMB-аудитории представлял себе нормативный tool-stack**, и служит pre-AI baseline для рассуждений о том, **как эволюционировал tooling и контент про tooling за 10 лет к 2026**.

`confidence: medium` — наблюдения опираются на один источник, но категория `historical baseline` именно про **снимок прошлого**, а не про currentтрy, поэтому single-source приемлемо: мы не утверждаем «такой landscape сейчас», утверждаем «такой landscape представляла Жажда в 2016».

## Зачем эта страница

Этот landscape **не современный** — почти все конкретные факты (цены, user-counts, банк-партнёры) устарели на 10 лет. Но **сам срез** ценен как:

1. **Pre-AI baseline для рассуждений о SMB-tool-эволюции.** Чтобы построить контент 2026 года «как изменилось/что осталось», нужен фиксированный baseline из прошлого. Этот листикл — готовый baseline.
2. **Эталонная структура tool-категорий.** В 2016 редакция Жажды делила SMB-finance-tooling на 4 категории: (a) специализированные финтрекеры с SMS-парсингом, (b) бесплатное open-source ПО, (c) методология-based приложения, (d) general-purpose таблицы. Эта таксономия **частично переносится на 2026** (см. ниже).
3. **Reference для дифференциации GRO-контента от legacy-листиклов.** Если GRO пишет «5 AI-инструментов предпринимателя 2026», знание, чем выглядел жанровый предшественник, помогает не повторить структурные ошибки (анонимность, отсутствие дат, format-fill до круглого числа).

## Срез: что входило в категорию «программа для бюджета SMB» по версии Жажды ~2016

10 продуктов, упорядоченные по объёму внимания в листикле:

| # | Продукт | Категория | Что декларируется |
|---|---|---|---|
| 1 | **Дзен-мани** (Антон Федосин, march 2015) | SMS-парсер для личных финансов | Мобильный + веб, распознавание SMS от ~200 банков, импорт из электронных кошельков, multi-user, plan-fact-анализ |
| 2 | **Дребеденьги** | SMS-парсер, аналог Дзен-мани | SMS-tracking, multi-user, экспорт в Excel, weekly email-бэкапы, self-hosted-вариант (до 30 пользователей) |
| 3 | **Семейный бюджет / ExpertPro** | Десктопный финтрекер | Платный с ограниченной бесплатной версией, годовая подписка — упомянуто как «недорого» |
| 4 | **HomeBank** | Бесплатный open-source-десктоп | Linux/Windows, разбивка операций, лимиты по категориям, динамические отчёты, интеграция с Quicken/MS Money/QIF/OFX/CSV |
| 5 | **You Need a Budget (YNAB)** | Методология-based приложение | OS X/iOS/Android/Windows, мульти-бюджеты, planning-first методология, integration с банкингом, $50 десктопная версия |
| 6 | **EasyFinance** | Облачный сервис с банк-API | 3-tier (Light/Medium/Full Pro), интеграция «банк-клиент» с named-партнёрами, мобильные клиенты |
| 7 | **Excel (Microsoft 2016)** | General-purpose таблицы | 400+ формул, .xls как indstandard, сводные таблицы, недостаток автоматизации и multi-user |
| 8 | **LibreOffice Calc** | General-purpose таблицы, бесплатный | Кросс-платформенный open-source, аналог Excel с худшими диаграммами |
| 9 | **Google Таблицы / Формы** | Cloud-native таблицы | Изначальная мобильность, multi-user real-time, интеграция в Google-стек |
| 10 | **«Бюджет» + «Кошелёк»** | Минималистические мобильные приложения | «Не дать выйти за рамки» / «ничего лишнего» — лёгкие consumer-приложения |

**Наблюдения по таксономии:**

- **4 структурных типа:** (а) SMS-парсеры, (б) методология-based, (в) open-source-десктоп, (г) general-purpose-таблицы — это **операциональная классификация finance-tooling 2016**, эта таксономия частично выжила в 2026.
- **Excel/Sheets/Calc — 30% листикла** — фактически 3 из 10 позиций отдано general-purpose-таблицам. Это **сильный editorial signal** о том, что в 2016 редактор RU-SMB-журнала считал Excel-стек **первой линией обороны** для финансового трекинга SMB. Этот тезис **переживает до 2026** (см. [[canon/marketing-frameworks/erp-vs-crm-smb-distinction]] и [[canon/marketing-frameworks/business-metrics-for-owners]]).
- **Все продукты ориентированы на single-user или small-team** — нет ни одного enterprise-продукта, ни одного integration-hub'a. Это **подтверждает SMB-первокатегорию** журнала.

## Что переносится на 2026 (durable observations)

### 1. Excel/Sheets как первая линия SMB-financial-tracking

Тезис «у тебя есть Office → у тебя есть программа для бюджета» **актуален в 2026**. Эволюционировал только context:

- **2016:** Excel desktop + LibreOffice Calc как бесплатная альтернатива + Google Sheets как cloud-альтернатива.
- **2026:** Google Sheets / Excel 365 / Notion-таблицы / Airtable — горизонтальное расширение. Notion и Airtable **отсутствуют в листикле 2016** (Notion основан 2016, Airtable 2012, но массовость RU-аудитории пришла позже).
- **Дрейф:** AI-сторонние и automation layer (Zapier-аналоги, OpenAI Code Interpreter, Claude Sheets-handling) преобразуют Excel-стек **из ручного в semi-automated** к 2026. Это и есть основной differentiator pre-AI vs AI-era.

### 2. SMS-парсинг как «фишка» SMB-личных-финансов — обрушился

Дзен-мани и Дребеденьги в 2016 строили UVP на «знаем 200 банков, автопарсим SMS». К 2026 эта категория **схлопнулась**:

- **Banking API** (Open Banking, банк-партнёрства T-Pay/СБП/QR) сделали SMS-парсинг архаичным.
- **Сами банк-приложения** научились категоризации и виджетам — нативная функция выместила сторонний tracker.
- **СБП и QR-pay** убрали SMS-уведомления как первичный канал → SMS-парсинг потерял data-source.

Это **disruption-кейс**: целая категория «sms-finance-tracker» исчезла за 10 лет. Полезно как **наводящий пример** для контента «какие SMB-tool-категории умрут к 2030».

### 3. Methodology-based приложения остались — теперь в AI-форме

YNAB-формат «продукт + методология учёта» (planning-first, envelope budgeting) в 2026 **жив**:

- YNAB сам **существует и растёт в US-market** (web subscription model).
- Methodology-based подход переехал в **AI-coaching products** — где AI прокачивает не tool-mastery, а **change-of-behavior** (планирование, ретроспектива, accountability). GRO попадает в эту категорию methodology-based-AI.

Это связка: **YNAB ~ методология для денег. GRO ~ методология для предпринимательского времени.** Структурно одна и та же позиция в product-space, но разные axises.

### 4. Анонимный editorial-обзор — формат деградировал

В 2016 анонимный листикл «10 программ для бюджета» — нормальный editorial-формат для RU-SMB-журнала. В 2026:

- **Анонимность теряет SEO-вес** (Google E-E-A-T 2022+: expertise/experience/authority/trust);
- **AEO/GEO эра** (AI-search-engines) требует verifiable attribution для попадания в AI-ответы (см. [[evolving/industry-trends/ai-search-aeo-geo-2026]]);
- **Listicle-формат отдельно от автора** проигрывает personality-driven контенту (см. [[evolving/content-trends/business-publication-ceo-listicle-pattern-2026]] — Деловой мир сохранил формат, но добавил guest experts).

Это указывает на **direction для GRO-контента**: листикл-формат всё ещё рабочий, но **обязательно с authorship + датой + конкретной критериологией**.

## Где использовать в GRO-контенте

### 1. Эпохальная компарация «как вели бюджет 10 лет назад vs сейчас»

Готовый hook: «В 2016 редакция Жажды считала вершиной финансового трекинга для предпринимателя — SMS-парсер. В 2026 SMS-парсера больше нет, потому что [реальный AI-инструмент сегодня]». Дёшево написать, читается легко, демонстрирует tooling-эволюцию.

### 2. Категоризация current GRO-content stack по 2016-таксономии

Применить 4-категорийную таксономию из 2016 (SMS-парсеры / методология-based / open-source / general-purpose) к 2026-AI-стеку:

| Категория 2016 | Что было | Аналог 2026 |
|---|---|---|
| SMS-парсеры | Дзен-мани, Дребеденьги | СБП-виджеты внутри банк-приложений (T-Pay, Сбер-Pay) |
| Методология-based | YNAB | GRO, Atomic Habits app, Sunsama, любые AI-coaches |
| Open-source десктоп | HomeBank, LibreOffice Calc | Notion-templates, Obsidian-vaults, n8n self-hosted |
| General-purpose | Excel, Google Sheets | + Notion + Airtable + Claude/ChatGPT-as-spreadsheet-interpreter |

Получается готовая структура для статьи «4 категории SMB-tooling — что изменилось за 10 лет».

### 3. Negative example для GRO-методологии content

Использовать **жанровые анти-паттерны** zhazhda-листикла как «как НЕ писать о GRO-инструментах»:

- ❌ Анонимный редакционный обзор → ✅ автор-эксперт с bio.
- ❌ Отсутствие даты → ✅ «На май 2026» в подзаголовке.
- ❌ Format-fill до круглого N → ✅ глубокая 5-6 инструментов с реальным сравнением.
- ❌ Эвристика «по download'ам/массовости» → ✅ критериология «протестировано 90 дней с N-founder'ов».

## Caveat

- **Не цитировать конкретные числа из этой страницы** как «факты 2016». Все числа в листикле Жажды — без attribution к первоисточнику и без датировки фактов. Использовать их как **редакционное мнение Жажды**, не как market data.
- **Не утверждать «landscape был такой»** — утверждать «landscape представляла Жажда такой». Это editorial bias, не market reality. В 2016 на RU-рынке были и другие категории (1С:Бухгалтерия, корпоративные ERP-системы), не попавшие в листикл потому, что выходят за SMB-personal-finance.
- **Дрейф через 5+ лет.** При появлении 2030-материала, который будет ссылаться на эту страницу как «pre-AI baseline», обновить параллель — возможно, появится 2026-листикл, который займёт промежуточное звено.

## Связанные страницы

- [[sources/2026-05-14-zhazhda-budget-apps-evergreen-2016]] — первоисточник
- [[evolving/content-trends/zhazhda-biz-evergreen-listicle-genre]] — жанровая parent-страница (6 образцов жанра, эта — об одном из 6)
- [[canon/marketing-frameworks/erp-vs-crm-smb-distinction]] — где Excel-как-hidden-failure-mode и Sheets-as-ERP уже зафиксированы (durable наблюдения)
- [[canon/marketing-frameworks/business-metrics-for-owners]] — где Excel-как-первый-ДДС-отчёт founder'а уже зафиксирован
- [[canon/target-audience/ru-smb-founder-owner-seller]] — целевая аудитория, к которой адресован и landscape 2016, и GRO-контент 2026
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — почему анонимный формат деградировал к 2026 (Google E-E-A-T + AI-search)
- [[evolving/content-trends/business-publication-ceo-listicle-pattern-2026]] — параллельный эволюционировавший листикл-формат (Деловой Мир сохранил структуру + добавил гостевых экспертов)
