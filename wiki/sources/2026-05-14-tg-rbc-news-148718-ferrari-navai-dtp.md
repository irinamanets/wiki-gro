---
id: mkt:sources/2026-05-14-tg-rbc-news-148718-ferrari-navai-dtp
title: "Telegram: @rbc_news/148718 — видео ДТП Ferrari (рэпер Navai), Зубовский бульвар (off-domain, triaged out)"
type: source
layer: volatile
theme: raw-notes
tags: [news-tracking, russia, rbc, telegram, video, off-domain]
confidence: low
created: 2026-05-14
updated: 2026-05-14
original: raw/processed/video/tg_rbc_news_148718.mp4
namespace: mkt
---

# Telegram: @rbc_news/148718 — видео ДТП Ferrari (рэпер Navai)

Стендалоун-видео из канала [@rbc_news](https://t.me/rbc_news) (id 148718, добавлено backfill-задачей «РБК» 2026-05-14). Новостной сюжет о ДТП: водителю спорткара Ferrari с рэпером Navai, попавшего в аварию на Зубовском бульваре в Москве, может грозить лишение водительских прав (авто без номеров, повреждена городская инфраструктура → обращение в суд о возмещении ущерба). Источник: [rbc.ru/rbcfreenews](https://www.rbc.ru/rbcfreenews/69fa3da69a7947bffb0482bf), пресс-служба депатранса Москвы.

## Метаданные
- **Тип:** video (mp4, ~2,6 МБ), Telegram-пост
- **Источник:** tg:rbc_news/148718 (https://t.me/rbc_news/148718)
- **Дата добавления:** 2026-05-14 07:29 UTC (backfill, scheduled task «РБК»)
- **Автор / источник:** РБК (деловое/общее СМИ)
- **Экспертность автора:** н/п — новостной incident-сюжет, не экспертное мнение по маркетингу/рынку.
- **Sidecar note:** был — generic backfill-контекст («трекинг новостей и трендов, вычленять релевантные инсайты, если есть»). Caption поста сохранён в `.note.md`.
- **Транскрипт:** `.transcript.md` — VAD не обнаружил речи (ratio 0,0%), whisper пропущен. Содержательного аудио нет; единственный текстовый сигнал — caption поста (см. выше).
- **Sensitive flag:** нет.

## Релевантность

**No relevant extractions.** Off-domain incident/celebrity news: ДТП спорткара с участием публичной персоны (рэпер Navai) и перспектива лишения прав. Нет рыночной, продуктовой, аудиторной или маркетинговой связки с ГРО. По рубрике `wiki/rules.md` («Релевантность сырых источников» → нерелевантно: «офтоп, не касающийся продукта / рынка / аудитории / маркетинга») — в слои не выносится.

Видео без речи (VAD 0,0%) — дополнительный извлекаемый контент отсутствует. Caption-фактура — чистый news-incident без бизнес-нарратива.

Источник обработан как audit-запись, файл уходит в `raw/processed/` (не `failed/` — нерелевантность не ошибка парсинга).

## Связанные страницы
- [[rules]] — рубрика релевантности (off-domain news)
</content>
