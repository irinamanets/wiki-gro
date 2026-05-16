---
id: mkt:sources/2026-05-05-hr-portal-ru-article-trebovaniya-k-menedzheru-po-podboru-personala
title: "Требования к менеджеру по подбору персонала"
type: source
layer: sources
theme: sources
tags: [hr, recruitment, evergreen-filler]
confidence: low
stale: false
created: 2026-05-05
updated: 2026-05-05
original: raw/processed/articles/web_hr-portal.ru_article_trebovaniya-k-menedzheru-po-podboru-personala_9bc38270.md
namespace: mkt
triaged: irrelevant-after-review
---

# Требования к менеджеру по подбору персонала

## Метаданные
- **Тип:** article (web, hr-portal.ru)
- **URL:** https://hr-portal.ru/article/trebovaniya-k-menedzheru-po-podboru-personala
- **Дата добавления:** 2026-05-05 (backfill scheduled task "hr-portal.ru")
- **Автор / источник:** анонимный (hr-portal.ru, без подписи и даты публикации)
- **Экспертность автора:** не верифицирован (анонимный SEO-материал, без bio, без даты)
- **Sidecar note:** был — backfill-источник по теме «HR / Управление персоналом», временный контекст для трекинга трендов рынка труда
- **Triage verdict:** relevant (автоматический, claude-haiku-4-5; topics: target-audience, industry-trends, market-data)

## Релевантность

**После ручной ревизии — no relevant extractions.**

Triage пометил источник как `relevant` (target-audience / industry-trends / market-data), но при применении доменного rubric (см. `wiki/rules.md` → «Релевантность сырых источников») контент не проходит:

- **Нет метрик, дат, бенчмарков** — текст не содержит ни одного числового показателя, ни одной ссылки на исследование, ни одной даты.
- **Нет эксперта** — материал анонимный, без подписи и квалификации автора (приоритет источника сигнала №3 → `confidence: low` + «автор не верифицирован»).
- **Нет тренда / кейса / новости** — это evergreen-SEO про общие обязанности HR-менеджера: набор кадров, обучение, управление, оценка качества.
- **Не добавляет к существующим страницам ЦА** — портрет HRD/HR-функции уже покрыт богаче в [[canon/target-audience/hrd-portrait-2025-2026]] (датированный источник hh.ru с разбивкой на 7 блоков компетенций, hard/soft skills, data-driven акценты). Добавление generic-боилерплейта только разбавит синтез.
- **Не имеет связки с продуктом ГРО** — нет use-case, нет JTBD, нет позиционных хуков.

Файл уходит в `raw/processed/` как audit-запись (паттерн повторяет ~40+ ранее обработанных hr-portal источников с `triaged: irrelevant`/`triaged-out`).

## Связанные страницы (контекст, не извлечение)

- [[canon/target-audience/hrd-portrait-2025-2026]] — датированная HR-аудитория для ГРО (B2B-угол)
- [[canon/target-audience/gro-segments]] — общая сегментация ЦА
- [[evolving/industry-trends/ai-replacing-jobs-global-2026]] — реальный HR/labor-market трекинг
