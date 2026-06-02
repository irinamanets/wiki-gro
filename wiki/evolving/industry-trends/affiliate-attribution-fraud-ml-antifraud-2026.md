---
id: mkt:evolving/industry-trends/affiliate-attribution-fraud-ml-antifraud-2026
title: "Affiliate-фрод и сдвиг к ML-антифроду — кейс cookie-stuffing eBay (Geo Visitors)"
type: page
subtype: insight
layer: evolving
theme: industry-trends
tags: [industry-trends, affiliate, attribution, fraud, antifraud, cookie-stuffing, ml, ai-agents, ebay, performance-marketing]
confidence: medium
stale: false
created: 2026-06-01
updated: 2026-06-01
sources: [sources/2026-06-01-tsifrovoy-robin-gud-obman-ebay.md]
namespace: mkt
---

# Affiliate-фрод и сдвиг к ML-антифроду

Кейс-разбор классического affiliate-фрода (cookie stuffing) и вывод о том, почему атрибуция по последнему клику структурно уязвима — и куда движется антифрод площадок. Источник — vc.ru story «Цифровой Робин Гуд: обман eBay» ([[sources/2026-06-01-tsifrovoy-robin-gud-obman-ebay]]). Релевантно для performance-маркетинга: показывает предел last-click-атрибуции и обостряющуюся проблему в эпоху AI-агентов.

## Кейс Geo Visitors (Шон Хоган, 2004–2006)

- Бесплатный виджет-карта посетителей сайта **скрыто ставил партнёрскую куку eBay** при загрузке `[conf:medium, src:2026-05-30]`.
- К 2006 схема хранила **650 000 активных кук** и забирала **~15% всего партнёрского бюджета eBay** `[conf:medium, src:2026-05-30]`.
- Всего выплачено партнёру **~$28 млн** до раскрытия `[conf:medium, src:2026-05-30]`.

Это classic **cookie stuffing**: партнёрская кука ставится без реального перехода пользователя по партнёрской ссылке, и любая последующая покупка ложно атрибутируется фроду.

## Антифрод eBay «Trip Wire»

- Невидимый пиксель на главной странице фиксировал **факт реального визита** пользователя `[conf:medium, src:2026-05-30]`.
- Сверка показала: **~99% «рефералов» Хогана** реальными переходами не подтверждались `[conf:medium, src:2026-05-30]`.

Механика обнаружения: сопоставить «заявленный реферал» с «зафиксированным фактом визита». Расхождение → фрод.

## Инсайт автора (атрибуция мнения)

По мнению автора материала `[conf:low, src:2026-05-30]` (эксперт не верифицирован — см. source-страницу):

- Любая **атрибуция по последнему клику без проверки факта визита** уязвима для фрода.
- Современный антифрод площадок строится на **графах связей аккаунтов** и **моделях обнаружения аномалий в кликах** (ML-антифрод), а не на простой last-click-логике.
- Проблема **обостряется в эпоху AI-агентов**, которые сами кликают по ссылкам и совершают покупки — граница «человек vs автоматический клик» размывается, last-click становится ещё менее достоверным.

## Что это значит для маркетинга

- **Last-click-атрибуция — не источник истины.** Performance-кампании с CPA-моделью партнёрам требуют independent visit-verification (пиксель факта визита, как Trip Wire), иначе бюджет утекает в фрод.
- **ML-антифрод — новая базовая линия.** Графы связей + аномалии кликов — стандарт для площадок с партнёрским бюджетом. Малому бренду — закладывать verification в условия affiliate-программы.
- **AI-агенты ломают атрибуцию.** Рост агентского трафика (AI кликает и покупает) — структурный вызов для всей performance-attribution. Связь с трендом удешевления AI-агентов: [[evolving/industry-trends/ru-recruitment-fraud-patterns-2026]] (смежный fraud-эволюционный паттерн).

## Caveats

- Цифры ($28 млн, 650 000 кук, ~15% бюджета, ~99%) — из ретроспективного материала, первичные судебные документы eBay vs Hogan не сверялись. `confidence: medium` на фактах кейса, `low` на интерпретации автора.
- Тренд `evolving` — антифрод-методы и AI-агентский трафик быстро дрейфуют, re-verify в пределах 6 месяцев.

## Связанные страницы

- [[evolving/industry-trends/ru-recruitment-fraud-patterns-2026]] — смежные fraud-паттерны РФ 2026
- [[evolving-strict/campaign-metrics/tbank-antifraud-service-metrics]] — антифрод как security-as-marketing (банковский кейс)
- [[evolving-strict/market-data/ru-mfo-microloan-market-2026]] — смежный fintech-рынок с SEO/affiliate-обзорами
- [[canon/marketing-frameworks/scammer-manipulation-8-techniques]] — потребительская сторона фрода
- [[sources/2026-06-01-tsifrovoy-robin-gud-obman-ebay]] — источник
