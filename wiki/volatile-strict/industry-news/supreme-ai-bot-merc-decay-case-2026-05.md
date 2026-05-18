---
id: mkt:volatile-strict/industry-news/supreme-ai-bot-merc-decay-case-2026-05
title: "@supreme_ai_bot (НейроБот) — Mercedes-наклейка кейс провала (800 → 330 юзеров)"
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [telegram-bot, gpt-wrapper, marketing-fail, organic-traffic-decay, case-study, founder-observation, awareness]
confidence: medium
stale: false
created: 2026-05-18
updated: 2026-05-18
sources: [sources/2026-05-13-tg-your-pet-project-may-6-13-2026.md]
namespace: mkt
---

# @supreme_ai_bot (НейроБот) — Mercedes-наклейка кейс провала

Real-life наблюдаемый кейс провала маркетинговой стратегии «наклейка на стекле собственного автомобиля» — описан Михаилом Табуновым ([[sources/2026-05-13-tg-your-pet-project-may-6-13-2026]] пост 621, 2026-05-06) с приложенным фото. **Используется как exemplary case для [[canon/marketing-frameworks/build-in-public-as-paid-traffic-anti-pattern|build-in-public-anti-pattern framework]]**.

`confidence: medium`: метрики (800 → 330 пользователей) self-reported Табуновым через наблюдение, не верифицированы через analytics-доступ к боту. Но **факт публикации** в Mercedes-наклейку и **снижение** между двумя точками наблюдения (~3-5 недель) — high-confidence через прямое фото.

## Хронология

- **(до 2026-04-XX)** — владелец **@supreme_ai_bot** ("НейроБот") клеит большую наклейку с QR-кодом, ником, и **промокодом MERCEDES на 20.000 бесплатных токенов** на заднее стекло собственного `Mercedes-Benz GLK 250 4MATIC`.
- **(2026-04-XX)** — Михаил Табунов фотографирует машину в пробке. На момент фото **800 пользователей** в боте `[conf:medium, src:2026-05-06]`.
- **2026-05-06** — Табунов публикует пост 621. На момент публикации **~330 пользователей** в боте `[conf:medium, src:2026-05-06]`. Минус **470 пользователей** за период наблюдения.

## Продукт-описание

**@supreme_ai_bot ("НейроБот")** — Telegram-бот, обёртка над ChatGPT API. Заявленные функции:

- **ИИ Ассистент** (chat-mode).
- **Генерация видео** (вероятно проксирование через 3rd-party AI-video API типа Runway или Pika).
- **Генерация фото** (DALL-E / Midjourney proxy).
- **Генерация песен** (Suno / Udio proxy).

Onboarding-incentive: **20.000 бесплатных токенов по промокоду MERCEDES**.

## Маркетинговый канал владельца

- **Канал привлечения:** наклейка на заднем стекле личного автомобиля Mercedes-Benz GLK 250 (4MATIC).
- **Аудитория канала:** **случайные водители в пробках** — нулевая ICP-фильтрация, нулевой targeting.
- **Скорость доставки:** пешеходная (зависит от пробок + угла обзора пассажира).
- **Конверсия:** требует от смотрящего: (а) увидеть наклейку, (б) запомнить ник / достать телефон / отсканировать QR на ходу или в пробке, (в) перейти в Telegram, (г) запустить бот, (д) ввести промокод. **Цепочка из 5 шагов**.

## Implied метрики (расчёт от ratio)

| Параметр | Значение |
|---|---|
| Пик пользователей | 800 |
| Текущий | ~330 |
| Decay | −59% за период наблюдения (≈ 3-5 нед) | [conf:low, src:2026-05-18]
| Implied weekly churn rate | ~15-20% | [conf:low, src:2026-05-18]

**Implication:** **15-20% weekly churn** для consumer GPT-wrapper — это **catastrophic level**. Industry benchmark для подписочных мобильных приложений (см. [[canon/marketing-frameworks/retention-benchmarks-b2c]]): D30 retention 5-15% для massmarket, weekly churn после первой недели — 5-10% максимум. [conf:low, src:2026-05-18]

## Editorial-skepticism caveat

- Возможно, что владелец **не пытался удержать пользователей** — наклейка могла быть **тестом креатива** или **виральным жестом** без серьёзных намерений монетизации.
- Возможно, метрика 800 → 330 — **активные** пользователи, а кумулятивный count (total subscribers) выше. Telegram-боты не показывают total публично.
- Табунов как наблюдатель — **не клиент бота**, не имеет analytics-доступа. Метрики через **«окошко количества участников»** в Telegram-боте (видимо публично при попытке start).

## Что это иллюстрирует

**Тезис Табунова:** наклейка на стекле = build-in-public:

1. **Channel mismatch:** автомобиль в пробке (физическое пространство, случайные водители) — не соответствует ICP «AI-tools enthusiasts in Telegram-comfortable demographic».
2. **Невозможность атрибуции:** owner не может оптимизировать creative / targeting / messaging — нет feedback loop.
3. **Невозможность масштабирования:** «купить 100 машин» — нелогично; «купить ad-spot в Meta» — логично.
4. **Конкурирующие продукты в нише** (ChatGPT-wrappers in Telegram) **с 200K+ пользователями и $X MRR** существуют и достигают этого через **paid-traffic в крупнейшие рекламные системы**. Они не клеят наклейки.

## Параллели в литературе

Этот кейс — **российский 2026-equivalent** классических provincial bootstrap failures, описанных:

- [[canon/marketing-frameworks/bavarian-backyard-self-employment-trap]] — «баварский дворик» паттерн: продукт сделан, но рынок неправильно классифицирован.
- [[canon/marketing-frameworks/blue-ocean-strategy-anti-pattern]] — «нет конкурентов = нет рынка». Здесь конкуренты есть, но они **в правильных рекламных системах**, не в физическом пространстве.
- [[canon/marketing-frameworks/external-validation-trap]] — паттерн «делаю что вижу, не что работает» (наклейка как mimicry «как делают рекламу»).

## Применение к GRO content

**Готовый hook-кейс:**

| Стадия воронки | Hook | Какому сегменту |
|---|---|---|
| Awareness | «Чувак клеит рекламу своего AI-бота на Mercedes. На фото — 800 юзеров. Сейчас — 330.» | Все сегменты как анти-pattern story |
| Awareness | «Что общего у наклейки на Мерсе и build-in-public в Твиттере?» (с answer = ничего не масштабируется) | Vibecoders + предприниматели |
| Consideration | «$20 в Meta достанет твоего реального пользователя. Наклейка достанет случайного водителя в пробке.» | Предприниматели |
| Anti-pattern | «Не клей наклейку на свой Мерс. Учись paid-traffic.» | Предприниматели на пороге выбора канала |

## TTL и stale-логика

Этот кейс — **volatile-strict** потому что:
- Single moment in time observation (May 2026).
- Через 3-6 месяцев бот может либо **окончательно умереть** (0 пользователей), либо **внезапно вырасти** (если владелец сменит канал), либо **остаться в этом состоянии** (zombie-status).
- Метрики живут только **до следующего наблюдения** от Табунова или другого источника.

**TTL: 14 дней** (re-verify в next ingest канала Табунова, или через прямой grep `@supreme_ai_bot` в новых источниках). После 90 дней — переоценить confidence на low и пометить stale.

## Связанные страницы

- [[canon/marketing-frameworks/build-in-public-as-paid-traffic-anti-pattern]] — главный framework, который этот кейс иллюстрирует
- [[canon/marketing-frameworks/bavarian-backyard-self-employment-trap]] — параллель anti-pattern
- [[canon/marketing-frameworks/blue-ocean-strategy-anti-pattern]] — параллель в логике "нет конкурентов = нет рынка"
- [[canon/marketing-frameworks/external-validation-trap]] — параллель в "делаю что вижу, не что работает"
- [[canon/marketing-frameworks/retention-benchmarks-b2c]] — benchmarks для weekly churn в B2C consumer apps
- [[evolving-strict/competitor-metrics/yp-may-2026-50k-mrr-app-cluster]] — пять кейсов, **которые сделали правильно** (paid-traffic) против этого кейса
- [[evolving/content-trends/your-pet-project-channel-hooks]] — host-страница hooks канала, содержит этот кейс
- [[sources/2026-05-13-tg-your-pet-project-may-6-13-2026]] — источник
