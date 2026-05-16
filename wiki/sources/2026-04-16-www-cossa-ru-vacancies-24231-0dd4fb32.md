---
id: mkt:sources/2026-04-16-www-cossa-ru-vacancies-24231-0dd4fb32
title: "Cossa vacancy 24231: Internet Buyer (РИМ) — scrape: mostly boilerplate"
type: source
layer: sources
theme: sources
tags: [empty-scrape, vacancy, cossa]
confidence: low
stale: false
created: 2026-04-16
updated: 2026-04-16
original: raw/processed/articles/web_www.cossa.ru_vacancies_24231_0dd4fb32.md
namespace: mkt
triaged: relevant
---

# Cossa vacancy 24231: Internet Buyer (РИМ) — scrape: mostly boilerplate

## Метаданные
- **Тип:** article (URL scrape)
- **Источник:** https://www.cossa.ru/vacancies/24231/
- **Файл:** `web_www.cossa.ru_vacancies_24231_0dd4fb32.md`
- **Sidecar note:** был — backfill из scheduled task `cossa.ru`, маркетинг/digital/SMM источник для трекинга новостей и трендов
- **Triage:** relevant (gpt-4o-mini) — но по факту triage среагировал на заголовки 3 новостных ссылок в шапке Cossa, а не на тело вакансии

## Релевантность

**No relevant extractions.** Скрейпер получил почти пустой ответ. В файле:
- фрагмент вакансии в 2 строки («Digital агентство ищет специалиста по закупке РИМ в сети Интернет; желателен опыт с Web Index, Adriver.ru, DoubleClick, Google Analytics») — без названия агентства, условий, дат; устаревший стек медиа-баинга (Adriver, DoubleClick)
- дублированное приглашение «встретиться с авторами Cossa»
- 3 не связанные ссылки на текущие новости Cossa в шапке (VK Видео ускоряет старт видео в 6 раз; «Медиатренды 2025–2026: стирание границ между устройствами, субботний прайм и нишевые темы»; «Объём рекламных услуг Х5 в I квартале 2026 года составил 7,7 млрд рублей») — это заголовки-teaser, полных текстов нет
- cookies-уведомление и копирайт

Вакансия сама по себе нерелевантна (контекст найма, не маркетинга продукта); фактура из вакансии (Adriver/DoubleClick как желательный опыт) — исторический стек медиа-баинга, а не современный сигнал. Link-titles — потенциально интересные сигналы (X5 7,7 млрд ₽ Q1 2026, медиатренды 2025–2026, VK Video), но только заголовки без тел — недостаточно для фактической страницы в слое.

Исходная страница (`cossa.ru/vacancies/24231/`), видимо, вернула старую неполную вакансию, либо контент рендерится JS, которого скрейпер не исполнил. Повторный fetch не делаем — это функция scheduled task `cossa.ru`, а не ingest.

Файл фиксируется как audit-лог обработки; в слои ничего не уходит.

## Связанные страницы
- [[sources/2026-04-16-www-cossa-ru-vacancies-23613-878daf9a]] — аналогичный случай пустой вакансии Cossa
- [[sources/2026-04-16-www-cossa-ru-vacancies-102519-a2ae26c1]] — ещё один scrape-irrelevant Cossa-vacancy
- [[sources/2026-04-14-tg-cossaru-apr-3-14]] — канонический ingest Cossa-контента (telegram, с полным телом постов)
