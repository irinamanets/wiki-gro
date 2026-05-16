---
id: mkt:sources/2026-04-16-www-cossa-ru-vacancies-20343-7764a36b
title: "Digital-дизайнер (вакансия Cossa)"
type: source
layer: sources
theme: sources
tags: [no-extractions, thin-fetch]
confidence: low
stale: false
created: 2026-04-16
updated: 2026-04-16
original: raw/processed/articles/web_www.cossa.ru_vacancies_20343_7764a36b.md
namespace: mkt
---

# Digital-дизайнер (вакансия Cossa)

## Метаданные
- **Тип:** web-страница (вакансия)
- **URL:** https://www.cossa.ru/vacancies/20343/
- **Источник:** www.cossa.ru (раздел /vacancies/)
- **Дата fetch:** 2026-04-16 10:48 UTC
- **Файл:** `web_www.cossa.ru_vacancies_20343_7764a36b.md`
- **Автор / источник:** Cossa (аггрегатор digital-вакансий РФ)
- **Экспертность автора:** не применимо (вакансия без авторства)
- **Sidecar note:** был — backfill scheduled task «cossa.ru» для трекинга маркетинг/digital новостей; потенциально polezny для контекста трендов/форматов

## Релевантность
**No relevant extractions.**

Фетч страницы вакансии фактически провалился по содержательной части: в markdown попал только шаблон сайта (две строки CTA «встретиться и пообщаться лично с авторами Cossa»), три ссылки сайдбара на несвязанные новости VK Видео / медиатренды / X5, cookie-notice и копирайт-футер. Описание самой вакансии (title «Digital-дизайнер», требования, задачи, вилка, работодатель) в fetch-выдаче отсутствует — вероятно, основной блок рендерится JS или требует авторизации.

Что могло бы быть релевантно, если бы контент был: структура вакансии как индикатор `industry-trends` по ролям/скиллам в digital-агентствах — но извлекать не из чего. Триаж-вердикт `relevant` от gpt-4o-mini был основан на шаблонных словах «Cossa / digital» без анализа того, что реальной фактуры нет.

Pattern: такой же тонкий фетч характерен для всех ранее обработанных `/vacancies/*` страниц Cossa (см. уже processed source-страницы той же даты `2026-04-16-www-cossa-ru-vacancies-*`) — все они triaged-out или fetch-empty.

В слои ничего не уходит. Source-страница оставлена как audit-лог факта обработки + сигнал про fetch-стратегию (crawler backfill'а cossa.ru/vacancies/ даёт пустые страницы).

## Связанные страницы
- [[sources/2026-04-16-www-cossa-ru-vacancies-20345-3b05c515]] — той же датой обработан «Технический дизайнер», triaged-out
- [[sources/2026-04-16-www-cossa-ru-vacancies-20347-01e4a2af]] — «Графический дизайнер», triaged-out
- [[sources/2026-04-14-tg-cossaru-apr-3-14]] — Cossa как источник новостей/трендов, где контент был релевантен
