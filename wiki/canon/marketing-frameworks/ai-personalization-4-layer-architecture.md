---
id: mkt:canon/marketing-frameworks/ai-personalization-4-layer-architecture
title: "AI-персонализация: 4-слойная архитектура (signals → features → bandits → generation)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai, personalization, architecture, contextual-bandits, gen-ai, real-time, decisioning]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-dzen-inc-personalization-vs-manipulation.md, sources/2026-05-05-dzen-ru-condensed.md]
namespace: mkt
---

# AI-персонализация: 4-слойная архитектура

Универсальный паттерн любой современной системы AI-персонализации в момент контакта с пользователем. Зафиксирован в 2026 году как стабильный, переносимый между индустриями шаблон. Применяется в e-commerce, в рекламных сетях (Google Ads, «VK Реклама», «Яндекс Реклама»), в банкинге (Bank of America Erica), в email-маркетинге (Movable Ink).

## Зачем эта рамка

Понятная архитектурная карта помогает:
- **Вендорам** — объяснить разницу между «у нас есть AI» и реальной полной системой.
- **Покупателям** — оценить, что именно из 4 слоёв есть у вендора, а что — bolt-on или маркетинговый wrapper.
- **Маркетинговому контенту** — структурировать рассказ о технологии без скатывания в hype или undersell.

## Четыре слоя

### Слой 1 — Сбор сигналов (input)

Источники сигнала о клиенте, собираемые **в момент события**, не батчами:

- Клик
- Скролл
- Паузы (где задержался, сколько времени)
- Время суток
- Устройство
- Контекст сессии (откуда пришёл, что искал)

Все эти сигналы стекаются в **поток событий** → объединяются с историческими данными о пользователе → формируют единый профиль.

Критическое требование — sub-секундная латентность передачи события в следующий слой. Батч-обработка убивает главную ценность системы.

### Слой 2 — Вычисление признаков (features)

Из сырых событий вычисляются **производные числовые признаки** для модели:
- «Число сессий за последние 7 дней»
- «Средний чек за последние 90 дней»
- «Вектор принадлежности к категории» (embedding)
- «Время с последней покупки»
- Сегментные принадлежности (high-LTV, churn-risk и т.д.)

Этот слой — feature store, либо рассчитываемый on-the-fly из event-stream, либо предвычисленный батчами с realtime-обновлениями.

### Слой 3 — Contextual bandits (decisioning)

Алгоритм выбора, **что показать пользователю прямо сейчас**.

Bandit'ы — класс алгоритмов из reinforcement learning. Главное отличие от обычного A/B теста:
- A/B показывает фиксированную пропорцию вариантов всем пользователям одинаково
- Bandit подстраивает выбор варианта под features конкретного пользователя

Contextual bandits решают: «при этих признаках пользователя — какой из доступных контентов / офферов / форматов даст наилучший expected outcome?»

Альтернативные имена: real-time decisioning engine, decision-as-a-service, next best action engine.

### Слой 4 — Генерация финального контента (<200мс)

Bandits решают «что показать», но не «как именно показать». Если контент полностью предзаготовлен (10 готовых баннеров, выбираем 1) — генерация не нужна. Если контент динамический — этот слой генерирует:

- Заголовок (LLM)
- Изображение (generative image model)
- CTA-формулировку
- Layout / порядок элементов

**Критический бенчмарк:** полный цикл от события до показа — **<200мс** `[conf:medium, src:2026-05-05]`. За это время происходит **~8 вызовов разных моделей** `[conf:medium, src:2026-05-05]`.

## Пример полного потока

Пользователь открыл product page.

1. **Слой 1:** event «page_view» с device, time, referrer, session_id → event bus
2. **Слой 2:** features компьютер: «N сессий за неделю», «склонность к категории X», «последний клик 12 минут назад» → feature store
3. **Слой 3:** contextual bandit получает features → выбирает «формат: video review, не текстовый», «emphasis: цена», «recommendation block: 5 близких товаров»
4. **Слой 4:** LLM генерирует динамический заголовок, image model генерирует hero, layout engine собирает блок → возвращается в браузер

Всё за <200мс `[conf:medium, src:2026-05-05]`.

## Какие компании работают с какими слоями

| Слой | Pure-play вендоры | Часть platform |
|---|---|---|
| 1: signals | Segment, Snowplow, RudderStack | Any martech-suite |
| 2: features | Tecton, Feast | Databricks, Snowflake |
| 3: bandits | Pega, Oracle Siebel RTD, Adobe Target | Klaviyo, MoEngage (light) |
| 4: generation | Persado, Movable Ink, Jasper | OpenAI / Anthropic API + RAG |

В РФ-телекоме полную CVM-стек реализуют МегаФон MegaRITM (см. [[canon/marketing-frameworks/real-time-personalization-cvm-mechanics]]) и аналогичные in-house платформы у крупных банков.

## Связь с predictive intent modeling

В 2026 году к 4-слойной архитектуре начинает добавляться **5-й слой** — predictive intent modeling. Он работает не «реактивно» (на текущий event), а **проактивно** — предсказывает, что пользователю понадобится через 1–2 шага в его сценарии.

В B2B серийно (см. enterprise-кейсы Salesforce, HubSpot). В B2C только единицы вендоров. Это следующая волна персонализации.

## Связанные страницы

- [[evolving/industry-trends/ai-personalization-industrial-shift-2026]] — индустриальный нарратив
- [[canon/marketing-frameworks/yudin-personalization-vs-manipulation-test]] — этический тест
- [[evolving-strict/market-data/ai-personalization-benchmarks-2026]] — числа эффекта
- [[canon/marketing-frameworks/real-time-personalization-cvm-mechanics]] — параллельная CVM-рамка (полностью совместима, эту страницу можно считать generalized-версией)
- [[sources/2026-05-05-dzen-inc-personalization-vs-manipulation]]

## Backlinks

_10 pages link to this one._

- [[canon/marketing-frameworks/rag-first-ai-implementation-melkozerov]]
- [[canon/marketing-frameworks/real-time-personalization-cvm-mechanics]]
- [[canon/marketing-frameworks/yudin-personalization-vs-manipulation-test]]
- [[evolving-strict/market-data/ai-personalization-benchmarks-2026]]
- [[evolving-strict/market-data/appmagic-mobile-landscape-2026]]
- [[evolving-strict/product-metrics/vk-video-recommendation-uplift-2026]]
- [[evolving/industry-trends/ai-personalization-industrial-shift-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-dzen-ru-condensed]]
