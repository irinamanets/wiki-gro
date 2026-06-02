---
id: mkt:evolving-strict/market-data/anti-ai-search-backlash-2026
title: Anti-AI-search backlash — рост DuckDuckGo после Google I/O 26 (май 2026)
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [seo, search, duckduckgo, google, ai-search, market-data, awareness]
confidence: medium
stale: false
created: 2026-05-30
updated: 2026-05-30
sources: [sources/2026-05-30-tg-neuraldvig-may-22-30-2026.md]
namespace: mkt
---

# Anti-AI-search backlash — измеримый отток от AI-выдачи (май 2026)

После Google I/O 26 (20 мая 2026), где Google усилил AI-ответы и AI-изображения в выдаче по умолчанию, зафиксирован **измеримый встречный спрос на поиск без ИИ**. Канал @neuraldvig (10801) ретранслирует данные [TechCrunch](https://techcrunch.com/2026/05/26/duckduckgo-installs-are-up-30-as-users-reject-being-force-fed-googles-ai-search/).

## Цифры

| Метрика | Значение | Период | Source |
|---|---|---|---|
| DuckDuckGo installs (общий рост) | +18% | после Google I/O 26 | `[conf:medium, src:2026-05-26]` |
| DuckDuckGo installs среди iPhone-пользователей (пик) | +69,9% | пиковый момент | `[conf:medium, src:2026-05-26]` |
| Трафик noai.duckduckgo.com (страница без ИИ-выдачи) | +22,7% | после Google I/O 26 | `[conf:medium, src:2026-05-26]` |

**Caveat по `confidence`:** числа приходят вторичной ретрансляцией Telegram-канала со ссылкой на TechCrunch; первоисточник TechCrunch — журналистская сводка app-store-данных, не аудированный отчёт. Заголовок TechCrunch упоминает +30% (URL), пересказ канала — +18%; расхождение не разрешено, поэтому `confidence: medium`. Для пресс-цитат нужна прямая верификация по первоисточнику `[conf:low, src:2026-05-26]`.

## Что это значит — структурный сигнал

Это первый **количественный** маркер тренда, который раньше фиксировался качественно: часть аудитории воспринимает форсированную AI-выдачу как ухудшение UX и **активно мигрирует** к alternativ-ам, рекламирующим «поиск без ИИ» как фичу. `noai.duckduckgo.com` — это позиционирование «anti-AI as a feature», и оно конвертит трафик `[conf:medium, src:2026-05-26]`.

Параллель с уже зафиксированным паттерном **anti-AI-позиционирования как бренд-актива** ([[evolving/content-trends/anti-ai-positioning-as-brand-asset-2026]]): здесь тот же механизм работает на уровне **search-инфраструктуры**, а не контента — пользователь голосует установкой приложения.

## Почему это важно для marketing-memory GRO

1. **Контент-хук «AI-fatigue».** Готовая фактура для поста/статьи: *«Пока все встраивают ИИ, +18% аудитории устанавливают браузер ради поиска БЕЗ ИИ. Урок: насильно навязанный ИИ — это анти-фича»* `[conf:medium, src:2026-05-26]`. Связь с [[evolving/content-trends/dead-internet-theory-counter-trend-2026]] и [[evolving/industry-trends/ai-accountability-premium-2026]].
2. **AEO/GEO-осторожность.** Если измеримая доля аудитории отключает AI-выдачу, то ставка только на AEO/GEO ([[evolving/content-trends/aeo-geo-llm-search-optimization-2026]]) недо-покрывает сегмент anti-AI-пользователей. Классический органический поиск и прямые каналы сохраняют ценность для этого сегмента.
3. **Сегментный сигнал.** Anti-AI-аудитория — потенциальный under-served сегмент для позиционирования «человеческого» продукта. Для GRO (self-development) это рифмуется с нарративом «инструмент усиливает человека, а не заменяет его».

## Связанные страницы
- [[evolving/content-trends/anti-ai-positioning-as-brand-asset-2026]] — anti-AI как бренд-актив (контентный уровень того же тренда)
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — AEO/GEO-оптимизация (контр-сила: ставка на AI-выдачу)
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — макро-тренд AI-поиска
- [[evolving/industry-trends/ai-accountability-premium-2026]] — премия за «честный»/anti-AI продукт
- [[sources/2026-05-30-tg-neuraldvig-may-22-30-2026]] — источник
