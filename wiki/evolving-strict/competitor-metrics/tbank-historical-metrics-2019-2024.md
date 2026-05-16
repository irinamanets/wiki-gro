---
id: mkt:evolving-strict/competitor-metrics/tbank-historical-metrics-2019-2024
title: "Т-Банк — исторические метрики 2019–2024: voice AI, ecosystem scale, VoiceKit, AI-matching"
type: page
subtype: competitor
layer: evolving-strict
theme: competitor-metrics
tags: [t-bank, tinkoff, competitor, historical, metrics, voice-ai, ecosystem, ai-matching, voicekit]
confidence: high
stale: false
created: 2026-05-15
updated: 2026-05-15
sources: [sources/2026-05-14-condense-web-vc-ru-tbank-27.md]
namespace: mkt
---

# Т-Банк — исторические метрики 2019–2024

Сводка ключевых публично заявленных метрик Т-Банка по периоду 2019–2024, извлечённых из корпоративного блога на vc.ru. Эти цифры — историческая опорная база для понимания траектории Т-Банка как ecosystem-игрока. Современные (2026) метрики и продуктовая карта — в [[evolving/industry-trends/tbank-corporate-platform-stack-2026]].

## Сводная таблица

| Категория | Метрика | Значение | Период | Source |
|---|---|---|---|---|
| Аудитория app | Активные клиенты | 40 млн | 2024 | `[conf:high, src:2024-01-01]` |
| Экосистема | Клиенты T-Bank group | 50M+ | 2023 | `[conf:high, src:2023-01-01]` |
| Premium brokerage | Клиенты / менеджеры | 1M / 1500 | 2023 | `[conf:high, src:2023-01-01]` |
| Voice AI (Олег) | Запуск | декабрь 2019 | 2019 | `[conf:high, src:2019-01-01]` |
| Voice AI (Олег) | Автоматизация звонков | 80% | конец 2020 | `[conf:high, src:2020-01-01]` |
| Voice AI (Олег) | Сценарии обработки | 60 | 2020 | `[conf:high, src:2020-01-01]` |
| Voice AI (Олег) | Пиковая нагрузка | 5000 одновременных звонков | 2020 | `[conf:high, src:2020-01-01]` |
| VoiceKit | Точность ASR | 95% | 2021 | `[conf:high, src:2021-01-01]` |
| VoiceKit | Calibration data | 100–150 звонков на модель | 2021 | `[conf:high, src:2021-01-01]` |
| VoiceKit | Цена B2B | ~10 000 ₽/мес | 2021 | `[conf:medium, src:2021-01-01]` |
| VoiceKit | Конкурент-бенчмарк | ~40 000 ₽/мес (ручная разметка) | 2021 | `[conf:medium, src:2021-01-01]` |
| LADA-дилер кейс | Uplift продаж | +12% | 2021 | `[conf:medium, src:2021-01-01]` |

## Voice AI стек — голосовой робот Олег

**Запуск:** декабрь 2019 `[conf:high, src:2019-01-01]`. К концу 2020 года Олег автоматизировал **80% входящих звонков** в банк `[conf:high, src:2020-01-01]` через **60 сценариев** обработки с пиковой нагрузкой **5000 одновременных звонков** `[conf:high, src:2020-01-01]`. Технология построена на собственном NLP+ASR стеке (не лицензированный сторонний движок) `[conf:high, src:2020-01-01]`.

**Значение для рынка:** Олег стал первым публично заявленным production-уровнем voice-AI в российском банковском секторе. Метрика «80% автоматизации» — это, по сути, deflation labor cost'а call-center'а в ~5x за 12 месяцев. `[conf:high, src:2023-01-01]`

## VoiceKit — продажа voice-AI как B2B-продукт

В 2021 году Т-Банк начал продавать собственные voice-технологии как B2B-сервис **Tinkoff VoiceKit**:

- Точность распознавания речи: **95%** `[conf:high, src:2021-01-01]` — достигается после **100–150 звонков** для калибровки на конкретный domain клиента `[conf:high, src:2021-01-01]`.
- Цена: **~10 000 ₽/мес** vs **~40 000 ₽/мес** для ручной разметки `[conf:medium, src:2021-01-01]` — то есть **4× cheaper**, что делало продукт конкурентоспособным даже без масштабных продаж.
- Кейс-применение: LADA-дилер получил **+12% к продажам** после внедрения через Calltouch Predict + VoiceKit `[conf:medium, src:2021-01-01]`.

**Значение для рынка:** VoiceKit — пример **monetization of internal capability**. Voice-AI был построен для собственных потребностей Т-Банка (Олег), но затем превратился в B2B-продукт. Этот паттерн «build-internal-then-sell» часто появляется в зрелых tech-компаниях.

## Ecosystem scale

- **Приложение Тинькофф (2024): 40M клиентов** `[conf:high, src:2024-01-01]` — упоминается как охват для партнёрских программ (Клубы лояльности и Tinkoff Выгода).
- **Т-Банк group (2023): 50M+ клиентов** `[conf:high, src:2023-01-01]` — в контексте Долями/BNPL-дистрибуции.

Цифры отличаются, потому что 40M = только пользователи мобильного приложения, 50M+ = total group exposure (включая держателей карт, B2B-клиентов, страховых клиентов, инвестиционных клиентов).

## Premium brokerage и AI-matching

- **Личное брокерское обслуживание:** **1M клиентов** при **1500 персональных менеджерах** `[conf:high, src:2023-01-01]`.
- **Алгоритм подбора:** работает «как Tinder» — multi-criteria scoring по доходности, продуктовому профилю, истории обращений, стилю коммуникации `[conf:high, src:2023-01-01]`.
- **Платформа:** TWork (внутренняя HR-платформа Т-Банка, расширена на manager-matching) `[conf:high, src:2023-01-01]`.

Это **~667 клиентов на менеджера** — невозможный соотношение без алгоритмического matching'а. Подробный фреймворк-анализ — в [[canon/marketing-frameworks/ai-matching-at-scale-tinder-pattern]].

## Связь с современностью (2026)

Историческая база 2019–2024 → сегодняшний ecosystem-стек (banking → Time → Селлер AI → Сделка → Т-Бизнес → Доли → Т-Образование → Т-Путешествия → Город / Топливо). Подробная карта 2026 — в [[evolving/industry-trends/tbank-corporate-platform-stack-2026]].

**Ключевая эволюционная стрелка:** в 2019–2024 Т-Банк создавал **отдельные продуктовые activations** (Олег, VoiceKit, Долями, Клубы лояльности). В 2025–2026 эти activations превратились в **sub-brand'ы с distinct visual identity** (Доли lavender, Т-Бизнес beige, T-Premium navy, Т-Инвестиции deep-violet, consumer-yellow для дочерних edtech/travel). Это переход от **monolithic-brand-with-products** к **portfolio-of-positioned-sub-brands**.

## TTL и обновление

Страница `evolving-strict` с TTL ~180 дней. Метрики 2019–2024 относительно стабильны (это исторические факты, не текущие KPI), но **сводки нужно re-verify при появлении новых данных Т-Банка** на vc.ru:
- Если будет обновлённая 2025+ цифра аудитории — supersession через `## Contradictions`.
- Если VoiceKit цена изменится (2026 cost базы) — то же.
- Если matching-ratio 1M/1500 пересмотрится — пометить как stale.

## Связанные страницы

- [[canon-strict/historical-campaigns/tbank-vselennaya-tinkoff-viral-2020]] — viral campaign 2020 на этой же ecosystem-базе
- [[canon-strict/historical-campaigns/tbank-loyalty-clubs-pilot-2024]] — клубы лояльности pilot 2024
- [[canon/marketing-frameworks/ai-matching-at-scale-tinder-pattern]] — фреймворк AI-matching 1M/1500
- [[canon/marketing-frameworks/data-driven-viral-campaign-framework]] — фреймворк viral-из-данных
- [[evolving-strict/market-data/ru-bnpl-aov-uplift-2023]] — BNPL метрики (Долями × Рив Гош)
- [[evolving-strict/market-data/ru-payment-conversion-2022]] — Tinkoff Pay conversion benchmarks
- [[evolving/content-trends/tbank-vc-ru-content-mix-2019-2024]] — публикационная стратегия за тот же период
- [[evolving/industry-trends/tbank-corporate-platform-stack-2026]] — современная карта ecosystem
- [[evolving/competitor-positioning/tbank-tinvest-premium-positioning]] — Т-Инвестиции positioning
- [[sources/2026-05-14-condense-web-vc-ru-tbank-27]] — источник
