---
id: mkt:sources/2026-05-05-tg-wtf-hr-redump
title: WTF_HR — Telegram-канал HR-аналитики, повторный дамп (50 сообщений ids 2176..2228, идентичен дампу 2026-04-14)
type: source
layer: evolving
theme: industry-trends
tags: [hr, labor-market, ai-adoption, ai-skepticism, corporate-ai, russia, usa, telegram, redump, no-delta]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-05
original: raw/processed/articles/tg_wtf_hr_20260505-130713.md
bundle_primary: raw/processed/articles/tg_wtf_hr_20260505-130713.md
bundle_children:
  - raw/processed/media/tg_wtf_hr_2177.jpg
  - raw/processed/media/tg_wtf_hr_2178.jpg
  - raw/processed/media/tg_wtf_hr_2181.jpg
  - raw/processed/media/tg_wtf_hr_2182.jpg
  - raw/processed/media/tg_wtf_hr_2183.jpg
  - raw/processed/media/tg_wtf_hr_2184.jpg
  - raw/processed/media/tg_wtf_hr_2185.jpg
  - raw/processed/media/tg_wtf_hr_2186.jpg
  - raw/processed/media/tg_wtf_hr_2187.jpg
  - raw/processed/media/tg_wtf_hr_2188.jpg
  - raw/processed/media/tg_wtf_hr_2189.jpg
  - raw/processed/media/tg_wtf_hr_2190.jpg
  - raw/processed/media/tg_wtf_hr_2191.jpg
  - raw/processed/media/tg_wtf_hr_2192.jpg
  - raw/processed/media/tg_wtf_hr_2198.jpg
  - raw/processed/media/tg_wtf_hr_2201.jpg
  - raw/processed/media/tg_wtf_hr_2203.jpg
  - raw/processed/media/tg_wtf_hr_2204.jpg
  - raw/processed/media/tg_wtf_hr_2207.jpg
  - raw/processed/media/tg_wtf_hr_2209.jpg
  - raw/processed/media/tg_wtf_hr_2213.jpg
  - raw/processed/media/tg_wtf_hr_2219.jpg
  - raw/processed/media/tg_wtf_hr_2221.jpg
namespace: mkt
---

# WTF_HR — повторный дамп 2026-05-05 (нет нового контента)

## Метаданные
- **Тип:** Telegram-канал дамп (50 сообщений, ids 2176..2228), бандл с 23 картинками
- **Источник:** https://t.me/wtf_hr
- **Дата дампа:** 2026-05-05 13:07 UTC
- **Автор / источник:** Анонимный коллектив авторов канала WTF_HR
- **Экспертность автора:** inferred (medium) для labour-market и корпоративной динамики; low для технических тезисов про ИИ. Подробности — на [[sources/2026-04-14-tg-wtf-hr-nov24-oct25|первичной source-странице 2026-04-14]].
- **Sidecar note:** был. Пользователь подтверждает временный характер источника: «глобально это временный контекст для трекинга новостей и трендов». Это второй такой дамп подряд — тот же channel, тот же диапазон id'ов, та же выборка.
- **Sensitive flag:** none — всё публично из открытого Telegram-канала.

## Релевантность

**Verdict: no relevant NEW extractions.** Этот дамп — побайтовый повтор контента, уже обработанного 2026-04-14: тот же диапазон id'ов 2176..2228 с теми же временными метками от 2024-11-12 до 2025-10-17, теми же 24 attached-вложениями (включая ту же missing PDF 2211).

Канал явно на паузе с октября 2025 — пост 2218 (2025-09-23) прямо декларирует: **«Регулярного постинга несколько раз в неделю больше не будет. ... Изменится и формат»**. Затем за 24 дня (до конца октября) выходят 4 заключительных поста цикла «Смелые прогнозы / Что уже происходит / Сокращения из-за ИИ». После 2228 (2025-10-17) — тишина 6+ месяцев на момент этого re-dump.

Поскольку **дельта = ∅**, никаких новых страниц в слоях не создаётся, и существующие страницы не обновляются. Этот audit-файл фиксирует факт повторной обработки и подтверждает, что ingest-pipeline корректно классифицирует «канал не двинулся» как success → `processed/` (не failure → `failed/`), в соответствии с правилами `wiki/rules.md` секция «Релевантность сырых источников».

## Что уже синтезировано (по предыдущему дампу)

Все ниже перечисленное было создано/обновлено в ingest-сессии **2026-04-14** на основании identical-выборки. Для маркетинга GRO эти страницы остаются актуальными и единственным «выходом» канала WTF_HR в слои:

- [[sources/2026-04-14-tg-wtf-hr-nov24-oct25]] — полная source-страница с 7 тематическими кластерами, OCR-описаниями всех 24 вложений и разбором PDF affidavit 2211
- [[evolving/content-trends/wtf-hr-ai-skeptic-hooks]] — bank из 5 hook-семейств для contrarian-балансира GRO-контента
- [[canon/marketing-frameworks/karpathy-ai-60s-mainframe-analogy]] — фреймворк «AI ≈ mainframes 60-х»
- [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]] — ссылается на этот источник как на 4-й голос про судьбу джунов и apprenticeship-revival
- [[evolving/industry-trends/ai-productivity-j-curve-2026]] — эмпирическая база hook'ов «SalesForce +4%», «Klarna reversal»
- [[evolving/industry-trends/future-of-work-trends-2026]] — рамка «две касты работников будущего» (пост 2228)
- [[evolving/industry-trends/return-to-office-global-2026]] — комментарий WTF_HR про корпоративный тренд RTO (пост 2221)
- [[evolving/industry-trends/ai-replacing-jobs-global-2026]] — критическая рамка «сокращают не из-за ИИ, а под бюджет ИИ-гонки» (пост 2225)

Ни одно из этих утверждений не получает нового подтверждения от данного re-dump'а: контент идентичен, дополнительных постов нет, дополнительной фактуры нет, авторская позиция не пересмотрена (потому что новых постов нет).

## Сравнение child-sets между дампом 2026-04-14 и 2026-05-05

В обеих выборках присутствуют ровно одни и те же 23 attached-картинки (2177, 2178, 2181..2192, 2198, 2201, 2203, 2204, 2207, 2209, 2213, 2219, 2221) и одна missing PDF (2211). В первом дампе была дополнительно картинка 2202.jpg, которая в текущем дампе не зафиксирована (бандл-резолвер не нашёл `_(attached: ...)_`-маркера в посте 2202 — возможно, telegram-экспортер на этот раз пропустил картинку, либо она удалена в канале; на содержательность это не влияет, поскольку пост 2202 «Развилка на дороге» был и тогда отнесён к нерелевантным).

OCR-описания всех 23 child-картинок полностью совпадают с уже задокументированными в [[sources/2026-04-14-tg-wtf-hr-nov24-oct25#медиа-вложения]] — повторно их здесь не дублируем, чтобы не создавать дрейфа между двумя audit-файлами.

## Операционный вывод

Канал @wtf_hr — **stale-источник** с октября 2025. Включать его в scheduled-задачу «Телеграм — HR / Найм / Карьера» в текущем виде не имеет смысла до тех пор, пока канал не возобновит постинг или не появится сигнал о новом эпизодическом посте. Альтернативы для трекинга RU-HR-нарративов и labour-market трендов в оставшихся в активе авторов — см. [[evolving/industry-trends/hiring-trends-russia-2026]], [[evolving/industry-trends/ru-labor-market-shift-2026]], [[evolving/industry-trends/ru-hr-tech-ai-landscape-2026]].

## Связанные страницы

- [[sources/2026-04-14-tg-wtf-hr-nov24-oct25]] — первичный дамп тех же 50 постов (содержательная база)
- [[evolving/content-trends/wtf-hr-ai-skeptic-hooks]] — bank контр-нарративов из этого канала
- [[canon/marketing-frameworks/karpathy-ai-60s-mainframe-analogy]] — Karpathy-аналогия
- [[evolving/industry-trends/future-of-work-trends-2026]] — две касты будущего работника
