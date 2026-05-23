---
id: mkt:evolving-strict/campaign-metrics/telegram-ads-benchmarks-2026
title: Telegram Ads -- CPL бенчмарки 2026
type: page
subtype: metric
layer: evolving-strict
theme: campaign-metrics
tags: [paid-ads, telegram, benchmarks, cpl]
confidence: low
stale: false
created: 2026-04-16
updated: 2026-05-18  # +расширение рекламного инвентаря Telegram Ads 2025–2026 (Banner in Video, реклама в ботах от 1000 польз., поиск по ключевым словам, Pixel Tag, снижение порога входа) из обзора Pressfeed
sources: [sources/2026-04-16-vcru-blogs-molyanov-spiridonov-gorny.md, sources/2026-05-18-pressfeed-telegram-updates-2025-2026.md]
namespace: mkt
---

# Telegram Ads -- CPL бенчмарки 2026

Сборная страница бенчмарков стоимости подписчика в Telegram Ads. Evolving-strict: каждая ставка с inline-маркером.

## Data points

| Источник | Канал | Ниша | CPL | Метод | Source |
|---|---|---|---|---|---|
| Молянов (self-reported) | Telegram Ads (криптокабинет) | AI-креаторы (вакансии) | ~2 руб./подписчик | Crypto-cabinet Telegram Ads | `[conf:low, src:2026-04-16]` |
| Петроченков (Convert Monster) | MAX | Performance/education | 80--150 руб./подписчик | MAX CPL | `[conf:medium, src:2026-04-14]` |

**Разброс:** от 2 до 150 руб. отражает разницу ниш, кабинетов (крипто vs официальный) и целевых действий. Молянов не уточняет sample size и длительность кампании, поэтому conf:low.

## Контекст

- Медиаинфляция в digital замедляется (E-Promo Group, 2026), но CAC в перенасыщенных аукционах продолжает расти `[conf:medium, src:2026-04-16]`
- Рынок digital-рекламы РФ за 24 месяца прошёл структурный сдвиг: «то, что в 2023 году считалось рабочей схемой, сегодня даёт отрицательную маржу» -- по мнению Молянова `[conf:medium, src:2026-04-16]`

См. макро-контекст: [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]].

## Расширение рекламного инвентаря Telegram Ads (2025–2026)

По обзору Pressfeed [[sources/2026-05-18-pressfeed-telegram-updates-2025-2026]] — платформа за 2025 — начало 2026 расширила форматы и точки контакта (имена экспертов в источнике не названы → conf:medium):

- **Снижен финансовый порог входа** на платформу — точная цена зависит от выбора реселлера `[conf:medium, src:2026-05-18]`.
- **Banner in Video** — текстовые объявления в видеоплеере `[conf:medium, src:2026-05-18]`.
- **Реклама в ботах** — доступна для ботов от **1000 пользователей** `[conf:medium, src:2026-05-18]`.
- **Реклама в поиске по ключевым словам** — новый формат размещения `[conf:medium, src:2026-05-18]`.
- **Pixel Tag** — инструмент трекинга действий пользователя после перехода на сайт из объявления; ускоряет управление кампанией и расчёт эффективности `[conf:medium, src:2026-05-18]`.

**Прочтение:** расширение инвентаря даёт брендам больше точек контакта и доступ к аудитории, не сталкивавшейся с рекламой в классических форматах; снижение порога входа открывает Telegram Ads для меньших бюджетов. Pixel Tag закрывает часть attribution-пробела, но не решает проблему пер-постовой атрибуции подписок (см. [[evolving/content-trends/telegram-platform-capabilities-2026]] раздел «Чего платформе не хватает»). Stars используются как валюта запуска рекламы — см. [[evolving/content-trends/telegram-stars-gifts-creator-monetization-2026]].

## Связанные страницы

- [[sources/2026-04-16-vcru-blogs-molyanov-spiridonov-gorny]] -- первоисточник Молянова
- [[sources/2026-05-18-pressfeed-telegram-updates-2025-2026]] -- расширение рекламного инвентаря 2025–2026
- [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] -- объём рынка и тренды
- [[canon/marketing-frameworks/native-advertising]] -- натив как альтернатива paid в условиях высокого CAC
- [[evolving/content-trends/telegram-native-formats]] -- organic-альтернатива Telegram Ads
- [[evolving/content-trends/telegram-platform-capabilities-2026]] -- общая карта возможностей платформы
- [[evolving/content-trends/telegram-stars-gifts-creator-monetization-2026]] -- Stars как валюта Telegram Ads
