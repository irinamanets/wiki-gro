---
id: mkt:evolving-strict/product-metrics/vk-video-recommendation-uplift-2026
title: VK Видео Discovery — +10% времени просмотра «Смотрите также» через AI face-recognition (май 2026)
type: page
subtype: metric
layer: evolving-strict
theme: product-metrics
tags: [ai, vk, recommendation, face-recognition, ru-market, consumer-media, retention, personalization]
confidence: high
stale: false
created: 2026-05-06
updated: 2026-05-06
sources: [sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026.md]
namespace: mkt
---

# VK Видео Discovery — +10% времени просмотра через AI face-recognition [conf:medium, src:2026-05-05]

## Ключевые числа

- **+10%** время просмотра контента «с любимыми героями» из раздела **«Смотрите также»** (после внедрения AI-системы) `[conf:high, src:2026-05-05]`
- **1 кадр/секунда** — частота анализа видеоряда первой моделью каскада `[conf:high, src:2026-05-05]`
- **2 модели машинного обучения** в каскаде (detection → recognition) `[conf:high, src:2026-05-05]`

## Источник и контекст

- **Изначальная публикация:** [habr.com/ru/news/1031600](https://habr.com/ru/news/1031600) (2026-05-05) `[src:2026-05-05]`
- **Ретрансляция:** Telegram @neuraldvig пост 10631 от 2026-05-05 ([[sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026]])
- **Команда-разработчик:** AI VK (внутреннее ML-подразделение VK).

`confidence: high` — это **публичное PR-сообщение крупной RU-корпорации с конкретной цифрой и архитектурной деталью**, опубликованное на Habr (RU IT-медиа с редактурой). Цифра 10% — **самостоятельно раскрытая VK**; она может быть подобрана для красивости (cherry-picked window or segment), но это не выдумка третьей стороны [conf:medium, src:2026-05-05].

## Архитектура AI-решения

Two-stage detection-recognition pipeline:

### Stage 1 — Detection (поиск популярных персон в видеоряде)

- Анализирует видеоряд **с частотой 1 кадр / секунда** `[conf:high, src:2026-05-05]`
- Цель: найти кадры, где присутствует «популярная персона» — без идентификации кто именно
- Это classic person-detection задача, упрощение по сравнению с face-recognition (recall важнее precision на этом этапе)

### Stage 2 — Recognition (распознавание конкретных персон)

- Работает **только на кадрах**, прошедших фильтр Stage 1 `[conf:high, src:2026-05-05]`
- Цель: определить, **кто именно** из «популярных персон» в кадре
- Это сужает compute-нагрузку: дорогую face-recognition прогоняют не на всём видео, а только на отобранных Stage 1 кадрах. Production cost-optimization паттерн.

## Бизнес-метрика

> «Время просмотра контента с любимыми героями **из раздела "Смотрите также"** выросло на **10%**, и лента стала заметно релевантнее.» `[conf:high, src:2026-05-05]`

**Что это конкретно означает (литералистский разбор):**

- **«Время просмотра»** — суммарная watch-time метрика. Не views, не impressions, не CTR. Это интеграл взаимодействия (релевантность × длительность × глубина).
- **«Контента с любимыми героями»** — подмножество контента, в котором AI-система определила «популярных персон»; не весь катало
- **«Из раздела "Смотрите также"»** — конкретный recommendation-surface (после-роликовая полоса). Не весь VK Видео, не главная лента, а **именно "Смотрите также"**.
- **«+10%»** — относительный uplift над baseline (предположительно — версия рекомендаций без face-recognition; A/B-test или pre/post-deployment) [conf:medium, src:2026-05-05].

**Что не раскрыто (caveats):**

- Какой baseline использовался (предыдущая система рекомендаций без face-recognition или без любого AI)
- Сегмент пользователей (все? только те, у кого есть «любимые герои»? новые vs старые?)
- Период измерения (1 неделя? 1 месяц?)
- Was the +10% measured at session-level, user-level, or platform-level [conf:medium, src:2026-05-05]

## Сравнение с глобальными бенчмарками

Глобальные публичные данные о AI-personalization uplift в видео-стриминге:

| Платформа | Метрика | Uplift | Год | Источник |
|---|---|---|---|---|
| Netflix Personalized Recs | Watch time, total | +20–30% [conf:medium, src:2026-05-05] | 2015 | Netflix Tech Blog (publicly known) |
| YouTube Deep Learning Recs | Total viewing time | +20% [conf:medium, src:2026-05-05] | 2016 | Covington et al., RecSys'16 |
| TikTok For You Page | Session length | +35% (estimated) [conf:medium, src:2026-05-05] | 2019–2020 | Industry estimate, не raw publication |
| **VK Видео Discovery (face-recog)** | **Watch time в "Смотрите также"** | **+10%** | **2026-05** | `[conf:high, src:2026-05-05]` |

**Кросс-чтение:** +10% от VK Видео — **скромнее глобальных топ-кейсов**, но это и узкая метрика (один surface — "Смотрите также"), и узкая фича (только face-recognition, не общая ML-personalization). Если интерпретировать +10% как **incremental gain поверх уже работающей общей рекомендательной системы**, то это значимый delta — каскадные улучшения в зрелых системах редко дают >10% [conf:medium, src:2026-05-05].

## Что значит для маркетинга РФ-контентных продуктов

1. **Production-grade AI personalization в RU consumer-media — это реальность 2026.** До VK Видео публичных RU-кейсов с раскрытой ML-архитектурой и конкретной uplift-цифрой не было. Это benchmark для всех новых RU-консьюмерных AI-кейсов.
2. **Face-recognition как specific feature** — не «AI вообще», а конкретная technical capability. Это маркетинговый паттерн «AI = разные специализированные модели в каскаде», а не «волшебная коробочка». Полезно для GRO-контента: не «GRO использует AI», а «GRO использует X для Y, Z для W».
3. **Корпоративный transparency-нарратив.** Раскрыть архитектурный детал (1 кадр/сек, две модели в каскаде) — это **редкий PR-ход для RU big tech**. Совпадает с паттерном из сигнала 10 ([[evolving/industry-trends/ru-vertical-ai-signals-2026]] — Sber GigaChain «open community»). Возможно, RU big tech начинает использовать «технический transparency» как differentiation в B2C-сегменте.

## Что значит для GRO

- **Бенчмарк AI-uplift** — если GRO внедрит AI-personalization для ленты упражнений / рекомендаций тренировок, +10% — это **минимально достижимый ориентир**, ниже которого результат будет «не стоило внедрять». Цифра пригодна как KPI-якорь [conf:medium, src:2026-05-05].
- **Контент-hook** — «как работает AI-рекомендация в RU-сервисах: VK Видео раскрыл architecture» — образовательный пост для сегмента «Продвинутых» ([[canon/target-audience/ru-ai-telegram-audience-segments]]). Дополняет соседние посты про Sber/Yandex/MWS.
- **Anti-pattern messaging** — не делать сравнения «GRO даст +50% retention через AI» без конкретной архитектурной детали и метода измерения. VK Видео даёт +10% и при этом раскрывает что-как — это правильный нарратив [conf:medium, src:2026-05-05].

## Связанные страницы

- [[evolving/industry-trends/ru-vertical-ai-signals-2026]] — VK Видео как сигнал 11
- [[evolving/industry-trends/ai-personalization-industrial-shift-2026]] — глобальный фон сдвига AI-personalization из top-of-funnel в production-grade
- [[evolving-strict/market-data/ai-personalization-benchmarks-2026]] — соседняя страница с другими бенчмарками AI-personalization
- [[canon/marketing-frameworks/ai-personalization-4-layer-architecture]] — фреймворк для понимания «какой слой AI-personalization работает»
- [[sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026]] — оригинальный источник (ретрансляция Habr)

## Backlinks

_5 pages link to this one._

- [[evolving/industry-trends/ai-personalization-industrial-shift-2026]]
- [[evolving/industry-trends/ru-vertical-ai-signals-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026]]
