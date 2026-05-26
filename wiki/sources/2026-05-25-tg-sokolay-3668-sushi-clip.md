---
id: mkt:sources/2026-05-25-tg-sokolay-3668-sushi-clip
title: "Telegram @sokolay #3668 — видео-клип «It's sushi time» (lifestyle, без речи)"
type: source
layer: sources
theme: sources
tags: [content, telegram, author-blogger, video, lifestyle]
confidence: low
stale: false
created: 2026-05-25
updated: 2026-05-25
original: raw/processed/video/tg_sokolay_3668.mp4
namespace: mkt
---

# Telegram @sokolay #3668 — видео «It's sushi time 🍣»

## Метаданные
- **Тип:** видео (mp4, ~5.8 МБ), отдельное сообщение Telegram-канала
- **Дата добавления:** 2026-05-14 (backfill scheduled task «Александр Соколовский»)
- **Канал:** [@sokolay](https://t.me/sokolay) (Александр Соколовский) — сообщение [#3668](https://t.me/sokolay/3668)
- **Caption:** «It's sushi time 🍣»
- **Автор / источник:** Александр Соколовский — медиа-предприниматель, ведущий подкаста «Соколовский»
- **Экспертность автора:** inferred (для author-channel паттернов; см. [[sources/2026-04-14-tg-sokolay-mar-apr-2026]]). К данному клипу неприменимо — контента для оценки нет.
- **Sidecar note:** был. Контекст от пользователя: «источник новостей по тематике Телеграм — Авторские, временный контекст для трекинга новостей/трендов; релевантные инсайты в другие категории вычленять».
- **VAD / транскрипт:** речь не обнаружена (VAD ratio = 0.0%), whisper пропущен (ниже порога). Клип без голосового контента — фоновое видео еды.
- **Sensitive flag:** none. Публичное сообщение, PII/кредов нет.

## Релевантность

**Решение: no relevant extractions в слои.** Причина: одиночный lifestyle-клип без речевого и текстового контента (VAD = 0.0%), caption — «It's sushi time 🍣». Чистый food/lifestyle-«наполнитель» feed'а, без сигнала про продукт ГРО, конкурентов, рынок, ЦА, контент-формат или метрики.

Разбор по рубрике `rules.md` («Релевантность сырых источников»):

- **Продукт-сигналов нет** — клип не про ГРО-подобный продукт.
- **Конкурент-сигналов нет** — нет позиционирования, мессаджинга, метрик, анонсов.
- **Контент-формат** — формально это «lifestyle-видео автора», но он уже зафиксирован как количественный паттерн в [[sources/2026-04-14-tg-sokolay-mar-apr-2026]] (личный/лайфстайл-контент как credibility-фундамент author-канала). Один новый food-клип не добавляет сигнала сверх уже извлечённого; отдельную страницу в `evolving/content-trends` не спавнит.
- **Метрик нет** — `evolving-strict/*` не затрагивается.
- **ЦА / тренды / методологии** — отсутствуют.

Соответствует ранее зафиксированной в бандле @sokolay категории out-of-scope lifestyle-заливки (Dubai-фото, тренировки, медитация — все помечены как чистый lifestyle, в слои не извлекались). Файл уходит в `raw/processed/` как обработанный (не `failed/` — это нерелевантность, не ошибка парсинга).

## Ключевые идеи

Отсутствуют — клип без речи и без содержательного текста (только caption «It's sushi time 🍣»).

## Факты и цифры

Отсутствуют.

## Связанные страницы

- [[sources/2026-04-14-tg-sokolay-mar-apr-2026]] — основной бандл-дамп канала @sokolay, где lifestyle-контент автора разобран как credibility-паттерн author-канала
- [[evolving/content-trends/podcast-driven-author-channel-patterns]] — подкаст-driven author-канал @sokolay как exemplar; lifestyle-клипы — часть его контент-микса
- [[evolving/content-trends/telegram-author-channel-patterns]] — общий паттерн Telegram author-каналов, к которому относится @sokolay
