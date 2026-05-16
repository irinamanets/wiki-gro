---
id: mkt:sources/2026-04-16-www-cossa-ru-vacancies-23613-878daf9a
title: "Cossa vacancy 23613: Директор по маркетингу (scrape: empty body)"
type: source
layer: sources
theme: sources
tags: [empty-scrape, vacancy, cossa]
confidence: low
stale: false
created: 2026-04-16
updated: 2026-04-16
original: raw/processed/articles/web_www.cossa.ru_vacancies_23613_878daf9a.md
namespace: mkt
triaged: relevant
---

# Cossa vacancy 23613: Директор по маркетингу (scrape: empty body)

## Метаданные
- **Тип:** article (URL scrape)
- **Источник:** https://www.cossa.ru/vacancies/23613/
- **Файл:** `web_www.cossa.ru_vacancies_23613_878daf9a.md`
- **Sidecar note:** был — backfill из scheduled task `cossa.ru`, маркетинг/digital/SMM источник для трекинга новостей и трендов
- **Triage:** relevant (gpt-4o-mini) — но по факту скрейпер не получил тело вакансии

## Релевантность

**No relevant extractions.** Тело вакансии «Директор по маркетингу» не было получено скрейпером — в файле присутствует только boilerplate:
- стандартное приглашение к встрече с авторами Cossa (дублированное)
- 3 не связанные ссылки на текущие новости Cossa в шапке (VK Видео, Медиатренды 2025–2026, реклама Х5 — эти страницы ingested как отдельные источники)
- cookies-уведомление и копирайт

Исходная страница (`cossa.ru/vacancies/23613/`), видимо, вернула 404/архив/требует авторизации, либо контент вакансии рендерится JS, которого скрейпер не исполнил. Повторный fetch не делаем — это функция scheduled task `cossa.ru`, а не ingest.

Файл фиксируется как audit-лог обработки; в слои ничего не уходит.

## Связанные страницы
- [[sources/2026-04-16-www-cossa-ru-vacancies-102519-a2ae26c1]] — аналогичный случай пустой вакансии Cossa
- [[sources/2026-04-14-tg-cossaru-apr-3-14]] — канонический ingest Cossa-контента
