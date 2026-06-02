---
id: mkt:evolving-strict/campaign-metrics/telegram-ads-benchmarks-2026
title: Telegram Ads -- CPL бенчмарки 2026
type: page
subtype: metric
layer: evolving-strict
theme: campaign-metrics
tags: [paid-ads, telegram, benchmarks, cpl]
confidence: medium
stale: false
created: 2026-04-16
updated: 2026-06-01  # +Нейроцех CPS-замеры с новым подрядчиком (€0,88 avg / €0,53 best, 2366 подписчиков; €1 Нейроцех / €1,16 личный канал; до этого 300–400₽ у других подрядчиков; Яндекс.Директ 70→250₽ exhaustion) из condensed-дайджеста Молянова мая 2026 → confidence low→medium (несколько независимых замеров)
sources: [sources/2026-04-16-vcru-blogs-molyanov-spiridonov-gorny.md, sources/2026-05-18-pressfeed-telegram-updates-2025-2026.md, sources/2026-06-01-condense-vcru-molyanov-may-2026.md, sources/2026-06-01-vc-ru-molyanov-2756355-reklama-v-telegram.md]
namespace: mkt
---

# Telegram Ads -- CPL бенчмарки 2026

Сборная страница бенчмарков стоимости подписчика в Telegram Ads. Evolving-strict: каждая ставка с inline-маркером.

## Data points

| Источник | Канал | Ниша | CPL | Метод | Source |
|---|---|---|---|---|---|
| Молянов (self-reported) | Telegram Ads (криптокабинет) | AI-креаторы (вакансии) | ~2 руб./подписчик | Crypto-cabinet Telegram Ads | `[conf:low, src:2026-04-16]` |
| Молянов / Нейроцех (новый подрядчик) | Telegram Ads | ИИ-клуб (образование) | €0,88 средн., €0,53 в лучшие периоды | 2366 подписчиков за кампанию | `[conf:medium, src:2026-05-01]` |
| Молянов / Нейроцех (новый подрядчик) | Telegram Ads | ИИ-клуб (образование) | €1 / подписчик | добили канал до 10к | `[conf:medium, src:2026-05-01]` |
| Молянов / личный канал (новый подрядчик) | Telegram Ads | авторский блог | €1,16 / подписчик | self-reported | `[conf:medium, src:2026-05-01]` |
| Молянов / Нейроцех (старые подрядчики) | Telegram Ads | ИИ-клуб | 300--400 ₽ и выше / подписчик | self-reported (раньше) | `[conf:medium, src:2026-05-01]` |
| Молянов / Нейроцех (Яндекс.Директ) | Яндекс.Директ | ИИ-клуб | вырос с 70 до 250 ₽ (канал перестал расти, исчерпание) | self-reported | `[conf:medium, src:2026-05-01]` |
| Петроченков (Convert Monster) | MAX | Performance/education | 80--150 руб./подписчик | MAX CPL | `[conf:medium, src:2026-04-14]` |

**Разброс:** от ~2 ₽ (криптокабинет, AI-ниша) до 150 ₽ (MAX performance) отражает разницу ниш, кабинетов и целевых действий. Несколько независимых замеров Молянова с **новым подрядчиком** (@hotheads_band) сходятся около **€0,5–1,2/подписчик** на тематической AI-аудитории `[conf:medium, src:2026-05-01]` — это заметно дешевле прежних 300–400 ₽ у других подрядчиков и исчерпавшегося Яндекс.Директа (70→250 ₽). Появление нескольких сходящихся замеров — основание поднять confidence страницы low→medium.

<!-- superseded 2026-06-01 by [[sources/2026-06-01-vc-ru-molyanov-2756355-reklama-v-telegram]] : ранее единственным замером Молянова был ~2₽ криптокабинет (conf:low); новые замеры дают €0,5–1,2 на официальном кабинете через @hotheads_band и контекст исчерпания Яндекс.Директа. Строка ~2₽ оставлена как валидный отдельный кейс (криптокабинет, другая ниша), но больше не единственная точка. --> [conf:low, src:2026-06-01]

**Подрядчик, рекомендованный Моляновым** (не только Telegram Ads): @hotheads_band `[conf:medium, src:2026-05-01]`.

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
- [[sources/2026-06-01-condense-vcru-molyanov-may-2026]] -- condensed-дайджест Молянова мая 2026 (Нейроцех CPS-замеры)
- [[evolving-strict/campaign-metrics/site-conversion-telegram-chat-case-2026]] -- сопряжённый CRO-кейс Молянова
