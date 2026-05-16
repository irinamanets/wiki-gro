---
id: mkt:evolving/content-trends/llm-sentiment-tracking-pattern-2026
title: "Паттерн автоматического трекинга sentiment LLM по HN — hnup.date (май 2026)"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [content, sentiment, llm, competitor-intelligence, automation, hackernews, pattern]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-cgevent-may05-08-2026.md]
namespace: mkt
---

# Паттерн автоматического трекинга sentiment LLM по HN — hnup.date

## Что это

[hnup.date/hn-sota](https://hnup.date/hn-sota) — публично доступный дашборд, который **ежедневно** скрейпит Hacker News, прогоняет LLM через комментарии и считает **sentiment в отношении конкретных моделей** (Claude, GPT, Gemini, Llama, …). Сигнал, найденный в @cgevent 2026-05-05 (#15599) — **первое публичное автоматизированное LLM-sentiment-tracking** для AI-моделей.

## Архитектура пайплайна (по описанию автора)

Каждый день автоматически `[conf:medium, src:2026-05-05]`:

1. **Получает 200 самых популярных постов за 24 часа на Hacker News**
2. **Через LLM выбирает посты, заголовки которых посвящены LLM или программированию в целом (максимум 50)**
3. **Для каждого поста отправляет заголовок и комментарии в Gemini** — он определяет упомянутые модели из списка и оценивает sentiment

## Что показывает дашборд (на 5 мая 2026)

- **Claude по-прежнему обсуждают/упоминают больше всех**, но **смешанная реакция** (одни хвалят, другие критикуют)
- **GPT обсуждается немного меньше, но получает гораздо меньше негатива**
- Visual: гистограмма по модели × sentiment-bucket, обновляется ежедневно

## Структурное значение

### Технический паттерн универсален

Эта архитектура — **переиспользуемый шаблон** для любого продукта, который хочет автоматически отслеживать sentiment про себя и конкурентов:

```
Источник комментариев (HN / Reddit / Twitter / Telegram channels / VC)
   ↓
LLM-фильтр (отобрать релевантные посты по теме)
   ↓
LLM-классификатор (sentiment + упомянутые продукты/модели)
   ↓
Аггрегация (storage: bucketed by date × product × sentiment)
   ↓
Публичный или внутренний дашборд
```

### Стоимость низкая, выгода высокая

Автор @cgevent отмечает:

> *«На HN выборка достаточно маленькая, поэтому делать далекоидущие выводы не получится. Хотелось бы увидеть такое для Reddit или даже Twitter, но там за API дерут много $.»*

То есть **economic constraint** — это **доступ к API источника**, не cost LLM-классификации. Для HN — free, для Reddit/Twitter — paid. Это **окно возможностей**: тот, кто построит дешёвый дашборд для Reddit/Twitter, получит **дифференцированный competitor intelligence** для продуктовых команд.

### Применимость для маркетинга GRO

#### Сценарий 1: трекинг sentiment GRO

GRO может построить **внутренний** аналог hnup.date для самого себя:
- Источники: Telegram-каналы (RU-AI комьюнити), VC.ru, Habr-комменты, App Store reviews
- Фильтр: посты, упоминающие «GRO» / «коучинг» / «goal-setting» / «трекер целей»
- Классификатор: positive / mixed / negative
- Дашборд: внутренний eng-tracking

**Зачем:** **ранний сигнал церебрального negative-sentiment** до того, как он перерастёт в кризисный PR. Также — материал для **content-team** про **«что пользователи хвалят / критикуют именно сейчас»**.

#### Сценарий 2: трекинг sentiment конкурентов

Аналогичный пайплайн для **карты конкурентного нарратива**:
- Источники: те же
- Фильтр: посты, упоминающие конкурентов GRO (Tilda Education, БизнесМолодость, Open Talks, Synergy, Skypro, ...)
- Классификатор: sentiment per конкурент
- Дашборд: **internal competitive landscape map**

**Зачем:** **сигналить content-team про окно возможностей** — «такой-то конкурент собрал negative волну → можно публиковать сравнительный контент» или **«такой-то конкурент собрал positive волну → стоит изучить, что они сделали»**.

#### Сценарий 3: контент-материал «AI-sentiment dashboards»

GRO-блог может опубликовать **статью-разбор** «как построить sentiment-tracking для своего продукта» — это **гарантированно работающий evergreen-контент** для b2b SaaS-аудитории GRO, потому что:
- Тема актуальная (LLM-инструменты для product analytics растут)
- Аудитория релевантная (предприниматели, маркетологи, продакты)
- Низкий competition: пока **никто в РФ публично не пишет про автоматизированный sentiment-tracking** на LLM-комментариях
- Естественно встаёт CTA на GRO («когда вы трекаете sentiment — куда вы записываете insights? в GRO как goal-tracking pattern»)

## Параллельные паттерны в индустрии

| Сервис | Что отслеживает | Метод | Public/Private |
|---|---|---|---|
| hnup.date/hn-sota | Sentiment LLM-моделей на HN | LLM (Gemini) + scraper | Public |
| HackerNews TOP-200 sort | Просто популярность | Heuristic | Public |
| AppFigures / SensorTower (GRO already uses) | App Store reviews | Rule-based + manual review | Paid |
| Brand24 / Mention.com | Brand mentions | Rule-based scraping | Paid SaaS |
| Pulse / Glean (внутр.) | Внутрисервисные ключевые слова | LLM (private) | Internal |

**Дифференциация hnup.date pattern:** **LLM-классификация sentiment** в одном пайплайне (а не отдельный manual-step). Это **низшая стоимость на один classified item** среди приведённых аналогов.

## Применение для GRO-контента (recap)

### Hook'и

1. **«Sentiment-tracking перестал быть enterprise-фичей»**. Один человек на ChatGPT API сегодня делает то, что 5 лет назад делала команда из 3 NLP-инженеров в SaaS-стартапе. Анчер контента про **AI-democratization of competitive intelligence**.

2. **«Claude обсуждают больше, но GPT любят больше»**. **Конкретная инсайт-цифра** для контента про **«популярность ≠ любовь»**, применима для **«брендинг ≠ user-experience»** нарратива.

3. **«Стоимость API источника = constraint роста»**. Анчер для контента про **«free-tier данных как конкурентное преимущество»** — кто умеет получать качественные данные без оплаты $, тот выигрывает на маржинальности.

### Anti-patterns

- **Не публиковать как «вот вам ready-to-use инструмент»** — hnup.date это **PoC-проект одного человека**, не enterprise-tool. Использовать как **шаблон**, не как **продукт**.
- **Не цитировать конкретные sentiment-числа как авторитетные** — выборка маленькая, методология не открыта, repeatability не гарантирована. Использовать как **directional signal**, не как **fact**.
- **Не строить sentiment-track против конкурентов без правовой консультации** — особенно в РФ, где **законодательство о персональных данных** покрывает многие виды публичного сбора отзывов. Сначала юрист, потом scraping.

## Связь с другими страницами

- [[evolving/competitor-positioning/]] — этот паттерн = инструмент для построения и обновления конкурентной карты
- [[evolving/content-trends/ai-news-channel-prompt-packs]] — параллельный паттерн «contentful prompts» (тут — analytics prompts)
- [[evolving/customer-feedback/gro-app-store-reviews]] — существующая ручная страница, для которой sentiment-tracking может быть автоматизирован
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]] — automated sentiment-tracking как часть нового скилл-сета маркетолога
- [[evolving/content-trends/competitor-data-poisoning-defense-pattern]] — обратная сторона: если кто-то трекает наш sentiment, мы можем влиять на него (через user-driven publishing)
