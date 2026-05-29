---
id: mkt:sources/2026-05-26-forbes-tegi-5-let-forbes-woman
title: "Forbes.ru тег '5-let-forbes-woman' (triaged-out)"
type: source
layer: sources
theme: sources
tags: [triaged-out, forbes-tag-stub]
confidence: low
created: 2026-05-26
updated: 2026-05-26
original: raw/processed/articles/web_www.forbes.ru_tegi_5-let-forbes-woman_1debeed4.md
namespace: mkt
triage_verdict: uncertain
triage_reason: "Источник из авторитетного издания Forbes Russia с релевантной тематикой (женщины в бизнесе), но файл содержит только заголовок и ссылку без внутреннего контента — низкая плотность фактов."
---

# Forbes.ru тег '5-let-forbes-woman' (triaged-out)

## Метаданные

- **Тип:** URL fetch-stub (тег-лендинг Forbes.ru)
- **URL:** https://www.forbes.ru/tegi/5-let-forbes-woman
- **Дата fetch:** 2026-05-26 14:35 UTC
- **Дата добавления:** 2026-05-26 (backfill scheduled task "forbes.ru")
- **Автор / источник:** Forbes Russia
- **Экспертность автора:** N/A (тег-лендинг, не статья)
- **Sidecar note:** был — общий контекст backfill-задачи по forbes.ru как источнику новостей бизнеса/финансов.
- **Sensitive flag:** none

## Triage

**Verdict:** `uncertain` → applied as `irrelevant` (нет извлекаемых фактов).

Триаж-резон: «Источник из авторитетного издания Forbes Russia с релевантной тематикой (женщины в бизнесе), но файл содержит только заголовок и ссылку без внутреннего контента — низкая плотность фактов.»

Triaged via `wiki-triage` agent (`claude-haiku-4-5`) at `2026-05-26T20:47:33Z`.

## Релевантность

**No relevant extractions.** Страница представляет собой тег-лендинг Forbes.ru с одним заголовком «5 лет Forbes Woman» и единственной исходящей ссылкой на спецпроект (`/forbes-woman/zhenshchiny-v-biznese/267499-spetsproekt-5-let-forbes-woman`). Нет ни сводки выпусков, ни тезисов, ни данных о ЦА, ни цитат — fetch вернул только meta-обёртку тега, а не контент целевой статьи.

Чтобы извлечь маркетинговый сигнал по теме «женщины в бизнесе / 5-летие Forbes Woman», нужно отдельно ingest'ить целевой URL спецпроекта (`267499-spetsproekt-5-let-forbes-woman`). Здесь — только audit-запись о попытке обработки тег-страницы.

## Содержание (для аудита)

Полный текст файла:

```
# 5 лет Forbes Woman – новости и статьи по тегу | Forbes.ru

Source: https://www.forbes.ru/tegi/5-let-forbes-woman
Fetched: 2026-05-26 14:35 UTC

[ Лучшие материалы и главные события за 5 лет журнала Forbes Woman ](https://www.forbes.ru/forbes-woman/zhenshchiny-v-biznese/267499-spetsproekt-5-let-forbes-woman)
```

## Связанные страницы

Связанных layer-страниц нет (no extractable signal). Семейство Forbes-тег-stub'ов — см. сводный паттерн в [[sources/2026-05-26-forbes-tegi-10-let-forbes]] и аналогичные `triaged-out` source-пейджи с tag `forbes-tag-stub`.
