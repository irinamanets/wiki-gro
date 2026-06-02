---
id: mkt:evolving/industry-trends/agentic-commerce-stripe-2026
title: Agentic Commerce — Stripe 5-level framework, ACP, инфраструктура 2026
type: page
subtype: trend
layer: evolving
theme: industry-trends
tags: [agentic-commerce, stripe, acp, stablecoin, api, b2b, payments, ycp, alice, sap, joule, openai, chatgpt-checkout]
confidence: medium
stale: false
created: 2026-04-14
updated: 2026-05-30  # +@techno_yandex (май 2026): «Торговец» как маркетинговый персонаж Алисы «Найти дешевле» / Perplexity Shopping — consumer-facing промо L2-агента
sources:
  - sources/2026-04-14-peregudov-telegram-dec25-apr26.md
  - sources/2026-05-18-pressfeed-pragmatix-ai-data-over-landing.md
  - sources/2026-05-30-tg-techno-yandex-may-26-30-2026.md
namespace: mkt
---

# Agentic Commerce — Stripe framework и инфраструктура 2026

Stripe в марте 2026 выпустила отчёт с концептуальной рамкой и инфраструктурным стеком для **эпохи покупок через AI-агентов**. Рамка и цифры пересказаны в [[sources/2026-04-14-peregudov-telegram-dec25-apr26]] (пост 411, 2026-04-07). Первичный отчёт Stripe в source не цитируется дословно и на него не ссылается ссылка — фиксируем как пересказ практикующего founder-а; `confidence: medium` до первичной верификации отчёта.

**Почему `evolving`, а не `evolving-strict`:** цифры приведены с округлениями и без привязки к конкретным страницам первичного отчёта. Если понадобится цитировать эти цифры как metric, нужно верифицировать по оригиналу Stripe и перенести metric-блок в `evolving-strict/market-data`.

## 5-уровневая лестница Agentic Commerce

Это **описательный** framework — не оценочный. Каждый следующий уровень не лучше предыдущего, а даёт больше полномочий агенту.

| Уровень | Название | Что делает агент | Что решает человек | Состояние апр.2026 |
|---|---|---|---|---|
| **L1** | Заполнение форм | Человек сам решает, что купить. Агент заполняет платёжные/доставочные данные и жмёт «купить» | Всё — выбор товара, момент покупки, подтверждение | **Mainstream**. ChatGPT с payment integrations, extensions браузера |
| **L2** | Описательный поиск | Человек описывает ситуацию («Школьная форма для третьеклассницы, любит Лабубу и теннис»). Агент предлагает товары | Выбор конкретного варианта из предложенного, подтверждение покупки | **Emerging**. Частично покрыт ChatGPT Shopping, Perplexity Shopping |
| **L3** | Память | Агент помнит предпочтения из прошлых разговоров и покупок. «Найди пару базовых образов на лето» — агент делает подборку под запрос, бюджет, особенности фигуры, прошлые покупки | Решение о покупке остаётся за человеком | **Research phase**. Появляются первые прототипы в Claude Code / OpenAI Memory |
| **L4** | Делегирование | Человек доверяет агенту сам выбор и покупку: «Купи мне одежду, $400» | Делегированный бюджет и намерение | **Далеко**. Blocked инфраструктурой (auth, payment safety) |
| **L5** | Предсказание | Промпта вообще нет. Агент знает календарь, предпочтения и бюджет. Человек получает уведомление: «Вот список — всё уже куплено» | Post-hoc approval, возврат при несогласии | **Далёкое будущее**. Применимо только к повторяющимся покупкам |

**Stripe сравнивает текущий момент с серединой 90-х** — когда интернет уже был, но никто не понимал, как его использовать.

**Прогноз «через год» (т.е. апрель 2027, по Перегудову с опорой на Stripe)**:
- L2 уйдёт в широкие массы (как сейчас ChatGPT).
- L3 будет активно развиваться (как сейчас Claude Code).

## Инфраструктурный стек Stripe под Agentic Commerce

| Компонент | Назначение |
|---|---|
| **Agentic Commerce Protocol (ACP)** | Открытый протокол, через который агенты находят продавцов и делают заказы. Параллель: как Stripe-ACH для платежей, только для agent-to-merchant commerce |
| **Shared Payment Tokens (SPT)** | Агенты смогут делать платежи, **не раскрывая реальных карточных данных**. Решает ключевую safety-проблему L4/L5 — делегирование бюджета без риска unbounded spend |
| **Agentic Commerce Suite** | Low-code решение для бизнесов — одна интеграция, продаёшь через множество AI-агентов одновременно. Снимает необходимость интегрироваться отдельно с ChatGPT, Claude, Gemini и т.д. |

## Числовые маркеры из отчёта Stripe 2025

Эти цифры — **пересказ Перегудова, не прямая цитата из отчёта**. Для использования в маркетинговом контенте GRO требуется доставать первичный Stripe Outlook 2026 и проверять.

- **$2 трлн** платежей обработано Stripe за 2025 — _«это равно 2% мирового ВВП или, например, ВВП России»_ `[conf:medium, src:2026-04-07]` (pass-through через Перегудова).
- **Объём крипто-платежей (стейблкоины) через Stripe** вырос за 2025 в **2×** до **$400 млрд**, **60% B2B** `[conf:medium, src:2026-04-07]`. Перегудов комментирует: _«А вы говорите, крипта сдулась.»_
- **Число компаний, достигших $10M ARR за 3 месяца с запуска, удвоилось** за 2025 `[conf:medium, src:2026-04-07]`. Интерпретация: если идея попала — масштабирование идёт быстрее, чем в дотвайбкодинговую эру.

## Импликации для маркетинга GRO

1. **GRO как объект agentic commerce** — через 12–24 месяца пользователь сможет сказать своему LLM: «Подбери мне приложение для тренировки когнитивных навыков под мои цели, подпиши на 3 месяца». Это L3–L4 сценарий. Следствие: **листинги в магазинах должны быть машиночитаемыми** (богатые метаданные, clean schema.org, описание через L2-дружественные use-cases). См. параллель с тем, как уже устроен ghost в JSON-LD Google Play ([[canon/product-knowledge/gro-google-play-listing]]).
2. **SPT и legal/trust-барьер**. Пока агенты не платят, но скоро смогут. Для GRO это значит, что paywall-эксперименты (триал на 1 ₽ за 14 дней, см. [[canon/product-knowledge/gro-pricing]]) должны быть машинно-проверяемыми и с явными conditions — иначе агент откажется подписать пользователя.
3. **L2-hook для контента**. Прямой content-slot: обучающие посты «как правильно описать задачу агенту, чтобы он подобрал тебе инструмент» — и в примере фигурирует GRO. Это одновременно educational и product placement.
4. **B2B-ветка**. Если $10M ARR за 3 месяца удваивается, то GRO в B2B-раскатке (корпоративы, HR-партнёрства) может двигаться быстрее, чем планировалось в 2025-м. Это аргумент за агрессивный outbound в ближайшие 6 месяцев.

## Update 2026-05-18 — Pressfeed/PRAGMATIX: первые публичные agent-чекауты и B2B-сдвиг

[[sources/2026-05-18-pressfeed-pragmatix-ai-data-over-landing|PRAGMATIX/Pressfeed]] (май 2026) фиксирует, что L2 уровень лестницы перешёл из «emerging» в **operational** на нескольких рынках одновременно:

### Глобально: OpenAI × Stripe ChatGPT checkout

> «Крупные американские магазины и технологические компании уже разрабатывают единые стандарты, чтобы AI могли работать с их каталогами напрямую. OpenAI и платежный сервис Stripe запустили первый такой чекаут в ChatGPT. Искусственный интеллект помогает пользователю выбрать товар и оформить заказ прямо в чате, а человек подтверждает покупку одним нажатием, без перехода на сайт.»

Это **первое production-grade воплощение L2** через инфраструктуру Stripe ACP. См. [[volatile-strict/industry-news/openai-stripe-chatgpt-checkout-2026-05]].

### RU: Алиса AI «Найти дешевле» + YCP

Параллельно Яндекс запустил аналог в Алисе AI: агент **«Найти дешевле»** + протокол **Yandex Commerce Protocol (YCP)** — RU-аналог ACP. Магазины подключаются через YCP, чтобы их каталог попадал в подборки агента. См. [[volatile-strict/industry-news/yandex-alice-find-cheaper-agent-2026-05]].

**Это означает:** L2-L3 лестницы уже стали reality в **двух крупнейших AI-экосистемах** — глобальной (OpenAI) и российской (Яндекс) — одновременно в Q1-Q2 2026. Прогноз «L2 — массовый через год» (апрель 2027) подтверждается, но **опережает на ~6 месяцев**.

### B2B: SAP Joule Tender Analysis Agent

В B2B-сегменте сдвиг идёт быстрее розницы. SAP интегрировала Joule с **Tender Analysis Agent** — автоматический разбор тендерных предложений (требования, сравнение поставщиков по цене, срокам, SLA, рискам) с рекомендацией. См. [[volatile-strict/industry-news/sap-joule-tender-analysis-agent-2026]].

**Что значит для B2B-продавца:**

> «Оценивается только то, что можно прочитать и сравнить: надежность поставок, SLA поддержки, совокупная стоимость владения, соответствие стандартам. Все это должно быть в данных, а не в PDF с коммерческим предложением.»

Это операционная валидация рамки [[canon/marketing-frameworks/product-data-as-architecture-pragmatix|«маркетинг = архитектура данных»]] на B2B-сегменте.

### Новые количественные сигналы (отдельная страница)

[[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]] фиксирует:

- **Adobe Black Friday 2025 (US):** +805% YoY AI-search traffic, +38% conversion `[conf:high, src:2026-05-18]`
- **McKinsey 2030:** $3–5 трлн agentic commerce / год `[conf:medium, src:2026-05-18]`
- **Gartner B2B 2028:** 90% сделок с AI на >$15 трлн `[conf:medium, src:2026-05-18]`
- **Brand Analytics RU 2025:** российские компании потеряли 33-38% органики `[conf:high, src:2026-05-18]`

McKinsey-цифра ($3-5T/год к 2030) дополняет цифру Stripe-2025 ($2T обработано, $400 млрд стейблкоинами) **prognoz-trajectory'ей** — Stripe сейчас уже больше 50% McKinsey-target минимума ($3T).

### Update 2026-05-30 — consumer-facing промо L2-агента (@techno_yandex)

@techno_yandex (карусель «В мире агентов», пост 5276, 2026-05-27) показывает, что Яндекс **маркетит L2-shopping-агента широкой аудитории как персонажа**: архетип «Торговец» (маскот-куница с QR-кодами и посылками), чьи «известные подвиды» — **«Найти дешевле» в Алисе AI и Perplexity Shopping**. Это сигнал, что L2-агенты вышли из «emerging» в потребительский маркетинг — бренд продвигает их как понятную «личность», а не функцию. Контент-приём разобран в [[evolving/content-trends/ai-agent-persona-mascot-design-2026]].

**Следствие для GRO:** если L2-агенты теперь рекламируются как персонажи массовой аудитории, осведомлённость пользователей о «спроси агента, что купить» растёт быстрее ожиданий → машиночитаемость листингов GRO становится приоритетом раньше, чем по прогнозу апрель-2027.

### Связь с продуктовым data-сдвигом

PRAGMATIX/Pressfeed артикулирует **новый структурный слой** в agentic commerce: после видимости (GEO/AEO) идёт **отбор по structured data**. Это разобрано в [[evolving/industry-trends/ai-search-product-discovery-layer-2026]] и [[canon/marketing-frameworks/product-data-as-architecture-pragmatix]].

Связь с лестницей: уровни L1-L5 описывают **degree of agent autonomy**, продуктовый data-сдвиг описывает **fuel** — какую информацию агент использует для решения. Без качественного structured data даже на L2 агент рекомендует не вас, а конкурента с лучшими данными.

## Связанные

- [[evolving/industry-trends/software-moat-erosion-2026]] — комплементарный тезис: «80% потребности в интерфейсах пропадёт, агенты общаются через API». ACP и SPT — инфраструктурный ответ на этот сдвиг.
- [[evolving/industry-trends/ai-native-company-architecture-2026]] — внутри компании агенты тоже общаются через стандартизированные API-контракты, это параллель.
- [[evolving/industry-trends/ai-search-product-discovery-layer-2026]] — параллельный тренд: AI как decision-layer для product selection через structured data
- [[canon/marketing-frameworks/product-data-as-architecture-pragmatix]] — концептуальная рамка «маркетинг = архитектура данных»
- [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]] — все benchmark-метрики 2025-2026
- [[volatile-strict/industry-news/openai-stripe-chatgpt-checkout-2026-05]] — L2 в production (global)
- [[volatile-strict/industry-news/yandex-alice-find-cheaper-agent-2026-05]] — L2 в production (RU) + YCP протокол
- [[volatile-strict/industry-news/sap-joule-tender-analysis-agent-2026]] — B2B agent в production
- [[evolving/content-trends/ai-agent-persona-mascot-design-2026]] — «Торговец» как маркетинговый персонаж L2-агента
- [[sources/2026-04-14-peregudov-telegram-dec25-apr26]] — первоисточник (пересказ Перегудова).
- [[sources/2026-05-18-pressfeed-pragmatix-ai-data-over-landing]] — Pressfeed/PRAGMATIX май 2026 (данные > лендинг)
- [[sources/2026-05-30-tg-techno-yandex-may-26-30-2026]] — @techno_yandex (consumer-facing промо L2-агента)

## Contradictions

Нет в рамках wiki. **Caveat**: все цифры здесь — pass-through через Перегудова из отчёта Stripe. Первичный отчёт не верифицирован. При первой же верификации оригинала нужно (a) проверить цифры, (b) обновить `confidence:` до `high`, если совпало, либо применить supersession, если цифра не совпала.

## Backlinks

_7 pages link to this one._

- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]]
- [[evolving/industry-trends/software-moat-erosion-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-04-14-peregudov-telegram-dec25-apr26]]
- [[sources/2026-05-05-tg-peregudov-jan-may-2026]]
- [[volatile-strict/competitor-news/replit-stripe-3digit-growth-2026-05]]
