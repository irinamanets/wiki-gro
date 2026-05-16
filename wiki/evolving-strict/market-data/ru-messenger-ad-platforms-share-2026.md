---
id: mkt:evolving-strict/market-data/ru-messenger-ad-platforms-share-2026
title: "Mессенджер-реклама в РФ — доли рекламодателей Q2 2026 (TG 67% / VK 65% / MAX 56%)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [market-data, advertising, telegram, vk, max, russia, paid-ads, platform-mix]
confidence: medium
stale: false
created: 2026-05-16
updated: 2026-05-16
sources: [sources/2026-05-14-tg-rb-ru-may-5-13-2026.md]
namespace: mkt
---

# Mессенджер-реклама в РФ — доли рекламодателей Q2 2026

Числовая фиксация **трёх mass-messenger платформ** в РФ как paid-каналы рекламодателей на февраль–апрель 2026. Через @rb_ru post 46210 (13 мая 2026) — пересказ исследования (источник без атрибуции в посте; типичный «по данным рынка» формат @rb_ru, поэтому conf:medium для всех значений).

**Важно:** это **первая числовая фиксация MAX-доли в рекламодательском mix** в marketing-memory. Предыдущие сигналы про MAX касались **аудитории канала** (cohort growth +60% YoY), не **доли рекламодателей**. [conf:low, src:2026-05-16]

## Доли рекламодателей (Q2 2026)

| Платформа | % рекламодателей с активным бюджетом | Источник | Source |
|---|---|---|---|
| Telegram | **67%** | rb_ru агрегация | `[conf:medium, src:2026-05-13]` |
| VK | **65%** | rb_ru агрегация | `[conf:medium, src:2026-05-13]` |
| MAX | **56%** | rb_ru агрегация — **первая фиксация** | `[conf:medium, src:2026-05-13]` |

**Интерпретация:** Telegram ещё лидирует, но **MAX уже на расстоянии 11 п.п.** Это значит — большинство рекламодателей **multi-platform**, не «или TG или VK». Структурная гипотеза подтверждена: «диверсификация по платформам» = **новая база** для RU advertising 2026, не «выбрать одну».

## Динамика стоимости в Telegram (фев → апр 2026)

| Метрика | Изменение | Source |
|---|---|---|
| Стоимость рекламных постов в TG | **−17%** | `[conf:medium, src:2026-05-13]` |
| Цена клика в TG | **−10%** | `[conf:medium, src:2026-05-13]` |
| Рост бюджетов маркетплейсов в TG | **+150%** (×2,5) | `[conf:medium, src:2026-05-13]` |
| Рост бюджетов финансовых компаний в TG | **+70%** | `[conf:medium, src:2026-05-13]` |

**Интерпретация:** **цены снижаются**, но **маркетплейсы (×2,5) и финансы (+70%) ужесточают конкуренцию** в TG. Это значит: [conf:low, src:2026-05-16]
- Для **большинства** advertisers TG **дешевеет** — снижение CPM
- Для **performance-категорий** (маркетплейсы, кредиты) TG **дорожает** через bid-pressure в auctions

Это классическая **competitive bifurcation** платформы: повышенный buyer competition выгоняет low-value advertisers, но performance-categories продолжают bid up.

## Cross-link с предыдущими benchmark'ами

- [[evolving-strict/campaign-metrics/telegram-ads-benchmarks-2026]] — CPL бенчмарки (Молянов криптокабинет ~2 ₽, MAX ~80-150 ₽). **Новый context**: общая стоимость в TG -17% к началу 2026, но **performance verticals** держат уровень или растут. [conf:low, src:2026-05-16]
- [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] — макро-объём рынка 470 млрд ₽ 2026 (прогноз), темп +10%. [conf:low, src:2026-05-16]
- [[evolving-strict/market-data/ru-smb-digital-ad-spend-2026]] — SMB-сегмент расходов.

## Маркетинговые следствия для GRO

1. **Multi-platform-планирование становится дефолтом, не премиумом.** Если у advertisers 67% TG / 65% VK / 56% MAX — это **тройное покрытие**. GRO-кампании в paid-ads должны планироваться сразу на **минимум 2 платформы** (TG обязательно + одна из VK/MAX). `[conf:medium, src:2026-05-13]`
2. **TG снижает CPM = окно возможностей для тестов**. Не-performance advertisers получают **лучшие** ставки в TG, чем 6 месяцев назад. GRO-brand-content (не performance, не direct response) получает **больше impressions за тот же бюджет**. `[conf:medium, src:2026-05-13]`
3. **MAX = новый «второй tier» канал**. **56% advertiser-priority** + предыдущий сигнал [[evolving-strict/market-data/ru-ai-tg-audience-segments-2026|MAX audience growth +60% YoY]] = pattern «MAX становится mainstream». Стоит **планировать тест GRO на MAX до конца Q3 2026**. [conf:low, src:2026-05-16]
4. **Performance-категории дорожают в TG**. Если GRO планирует performance-кампании (direct-response, app-install, subscribe) — closer внимание к bid-pressure от маркетплейсов в TG. Альтернатива: VK Ads или MAX (где пока меньше performance-конкуренция).
5. **«Платформенный портфель» — новый KPI** для CMO. Compliance с тройным mix не означает 33/33/33; означает **наличие данных** по effective CPC/CPM в каждой из трёх.

## TTL и обновления

- **TTL: 90 дней** (evolving-strict). К августу 2026 — обновить:
  - Сдвинулся ли MAX выше 60% (catching up to VK)? [conf:low, src:2026-05-16]
  - Стабилизировалась ли цена клика в TG после -10%? [conf:low, src:2026-05-16]
  - Появились ли новые большие vertical-конкуренты (e-commerce, edu)?
- **Watch list:**
  - Официальный AKAR / AdIndex Q2 2026 отчёт по разделу messenger ads
  - Реакция Mail.ru / VK на growth MAX — увеличат ли промо-предложения для миграции к VK?
  - Появление **TG Stars** или **TG Premium ad-units** — новый разрыв в pricing

## Связанные страницы

- [[sources/2026-05-14-tg-rb-ru-may-5-13-2026]] — первоисточник (@rb_ru post 46210)
- [[evolving-strict/campaign-metrics/telegram-ads-benchmarks-2026]] — CPL бенчмарки Telegram Ads
- [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] — макро-объём рынка
- [[evolving-strict/market-data/ru-smb-digital-ad-spend-2026]] — SMB digital ad spend
- [[evolving/competitor-positioning/max-messenger]] — MAX как платформа
- [[evolving/content-trends/telegram-native-formats]] — organic-альтернатива
- [[evolving-strict/market-data/digital-ad-cpm-shifts-q1-2026]] — Q1 CPM движение
