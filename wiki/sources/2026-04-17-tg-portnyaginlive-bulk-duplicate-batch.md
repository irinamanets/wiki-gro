---
id: mkt:sources/2026-04-17-tg-portnyaginlive-bulk-duplicate-batch
title: "Telegram @portnyaginlive — bulk-дубль 13 постов (10 фото + 3 видео, audit-only)"
type: source
layer: evolving
theme: content-trends
tags: [telegram, author-blogger, portnyagin, duplicate, audit-only, bulk-audit]
confidence: low
created: 2026-04-17
updated: 2026-04-17
original: raw/links.md#bulk-batch-2026-04-17
namespace: mkt
---

# Telegram @portnyaginlive — bulk-аудит 13 дубликатов (29 файлов)

## Метаданные

- **Тип:** консолидированный bulk-audit; 13 primaries (10 JPG + 3 MP4) + 16 bundle-children + sidecars = 29 физических файлов из того же backfill-дропа.
- **Канал:** [@portnyaginlive](https://t.me/portnyaginlive) — авторский канал Дмитрия Портнягина.
- **Дата повторного добавления:** 2026-04-14 12:54–12:55 UTC (автоматическая backfill-задача «Дмитрий Портнягин»).
- **Sidecar notes:** все 29 файлов имеют одинаковую пользовательскую заметку — «Телеграм — Авторские», трекинг новостей и трендов. Caption-поле заполнено только у primaries (10 постов), у bundle-children сохранён тот же шаблонный sidecar без caption.
- **Sensitive flag:** none — публичный канал, PII отсутствует.

## Статус — bulk MD5-идентичный дубль уже обработанного bundle-дампа

Все 13 primaries и все 16 bundle-children — **MD5-идентичные дубли** файлов, уже находящихся в `raw/processed/` и являющихся bundle-детьми канального дампа [[sources/2026-04-14-tg-portnyaginlive-mar-apr-2026]]. Новый drop отличается только отсутствием суффикса ` (1)` в имени файла.

Файлы попали повторно в `raw/pending/` через автоматическую backfill-задачу «Дмитрий Портнягин» 2026-04-14 12:54–12:55 UTC. Фактического нового контента не вносят. Для видео (11167, 11168, 11169 + 11170/11171/11172) транскрипты (whisper-1) уже были учтены в enrich-pass родителя 2026-04-15 — см. `## Транскрипты медиа` в родительском bundle-source.

**Решение о консолидации.** После пяти индивидуальных duplicate-audit страниц ([[sources/2026-04-17-tg-portnyaginlive-11128-duplicate]], [[sources/2026-04-17-tg-portnyaginlive-11131-duplicate]], [[sources/2026-04-17-tg-portnyaginlive-11132-duplicate]], [[sources/2026-04-17-tg-portnyaginlive-11158-11161-duplicate]], [[sources/2026-04-17-tg-portnyaginlive-11166-duplicate]]) паттерн стабилизирован: каждый файл этого backfill-дропа — MD5-дубль, весь контент уже ingested родителем, никаких новых слой-правок. Оставшиеся 13 primaries сливаем в один audit-источник, чтобы не засорять `wiki/sources/` одинаковыми one-liner'ами.

## Релевантность

**No relevant extractions across all 13 primaries + 16 children.** Весь маркетингово-релевантный контент уже извлечён при первичном ingest'е родительского bundle-дампа и зафиксирован в [[evolving/content-trends/portnyagin-founder-channel-patterns]]. Повторный прогон тех же MD5 не даёт нового signal'а. В слои не пишется ничего.

## Таблица дубликатов (13 primaries)

Все MD5 — pending == processed (проверено перед переносом). Caption взят из `.note.md` sidecar.

### Фото (10 primaries)

| # | Пост | MD5 | Bundle | Caption (короткий тег) |
|---|---|---|---|---|
| 1 | 11127 | `b6af31422e92fcd0f50152a2f1fbf09e` | orphan | _(caption отсутствует в sidecar — только стандартный блок «Телеграм — Авторские»)_ |
| 2 | 11133 | `10784cd03a625af8479316ac45c9dbfc` | orphan | «Сегодня Siberia — 4 года» (4-year-anniversary post, founder-retrospective на открытие первого банного комплекса в Москве, COVID-start/СВО-open) |
| 3 | 11135 | `bcfd4847bd9e00b8ce719888a992cedf` | orphan | «Ключевая ставка» (прогноз снижения ставки ЦБ 20 марта до 15%, 7-е снижение подряд, caveat про бюджетную неопределённость) |
| 4 | 11136 | `55cd11756cdcb53422fce892d1c48b82` | orphan | «Кладбище стартапов: Pets.com» (unit-economics разбор на примере dot-com crash — CAC $400, маржа 2–4%, losses 88M зрителей Super Bowl, IPO→shutdown за 9 мес; Chewy-sequel $10-11B cap) |
| 5 | 11137 | `fa04d9d32c66a1212ab48a54c4d96f8e` | 11137+11138+11139+11140+11141 | «Дофаминовое меню: где брать гормоны счастья» (шпаргалка по 5 нейромедиаторам — дофамин/эндорфины/мелатонин/серотонин/окситоцин) |
| 6 | 11145 | `f9e7299fe7e8deb913ea13de7e5325ec` | 11145+11146…+11153 | «Плато Путорана с Димой Портнягиным» (промо-пост гастроэкспедиции Neverend+Siberia, 30 июля–3 августа, Норильск, 1.39 млн ₽, 9 bullets программы: вертолёты, каякинг, WHERETOEAT-шефы, баня, DJ-сеты) |
| 7 | 11155 | `84255ef65b358ee4bc588248d0763cf6` | 11155+11156 | «У нас есть преимущество перед зумерами — мы умеем пользоваться ими профессионально» (founder-retrospective mini: первый офис Димы в Благовещенске, 2008) |
| 8 | 11157 | `37d69235ee62de2a371e9f0b6bfe031f` | orphan | «Бизнес-события апреля» (editorial-подборка ~18 мероприятий по Москве — ТОЛК Форум, Дата-саммит, Скольково, Genesis, Finnext, Data Fusion, AI Future/Blockchain, ExpoElectronica, GAME & LEARN и др.) |
| 9 | 11164 | `71e6936f01c645cae779c5ee53ef827b` | orphan | «ВРЕМЯ НЕТВОРКИНГА» (editorial-рубрика нетворкинга в комментариях, 5-пунктовый формат представления, модерационные правила) |
| 10 | 11165 | `4e8b869496e6e843381839eb2eceede6` | orphan | «В России могут ввести плату за VPN-трафик» (Минцифры — квота 15 ГБ/мес, ₽150/доп. ГБ; опасения по YouTube/Instagram) |

### Видео (3 primaries)

| # | Пост | MD5 | Bundle | Caption (короткий тег) |
|---|---|---|---|---|
| 11 | 11167 | `32f83ed271940043dcc4d0cbafc7b81f` | orphan | «Меньше месяца осталось до открытия нового банного комплекса Siberia» (анонс Siberia Москва, метро Бауманская) |
| 12 | 11168 | `9ee4217210b23e811c0710bbac0769ef` | orphan | «Думаем наперед, товарищи / Think about it» (founder-short, идея-тизер без фактуры) |
| 13 | 11169 | `93c88c6737573f65efbf1badbe97add2` | 11169+11170+11171+11172 | «Новости из мира ИИ за неделю» (AI-weekly digest: 10 пунктов — китайские гуманоиды, Figure 03 у Меланьи Трамп, Midjourney Pretext, Claude Code autonomy, Figma AI agents, Anthropic computer use, ByteDance Deerflow 2.0, Salesforce логистика, Meta* TRIBE v2, OpenAI закрывает Sora) |

### Bundle children (16 файлов, все MD5-verified дубли)

- **Bundle 11137** (post «Дофаминовое меню»): 11138, 11139, 11140, 11141 (4 карточки — визуализация гормонов).
- **Bundle 11145** (post «Плато Путорана»): 11146, 11147, 11148, 11149, 11150, 11151, 11152, 11153 (8 фото экспедиции — природа/активности).
- **Bundle 11155** (post «Преимущество перед зумерами»): 11156 (1 фото первого офиса).
- **Bundle 11169** (post «Новости из мира ИИ»): 11170, 11171, 11172 (3 видео-иллюстрации AI-новостей с предсохранёнными `.transcript.md`).

Все 16 children имеют sidecar `.note.md` с таким же шаблонным блоком «Телеграм — Авторские», но без caption-поля (caption принадлежит primary'ю поста).

## Связанные страницы

- [[sources/2026-04-14-tg-portnyaginlive-mar-apr-2026]] — канальный bundle-дамп, где все 13 постов уже учтены как bundle-дети или отдельные факты и где транскрипты 11167/11168/11169+children были добавлены в enrich-pass 2026-04-15
- [[evolving/content-trends/portnyagin-founder-channel-patterns]] — страница паттернов формата founder-channel @portnyaginlive (AI-digest, editorial-calendar, founder-retrospective, promo-post, news-digest — все эти форматы уже на ней)
- [[sources/2026-04-17-tg-portnyaginlive-11128-duplicate]] — индивидуальный audit того же backfill-дропа (прецедент паттерна)
- [[sources/2026-04-17-tg-portnyaginlive-11131-duplicate]] — индивидуальный audit того же backfill-дропа
- [[sources/2026-04-17-tg-portnyaginlive-11132-duplicate]] — индивидуальный audit того же backfill-дропа
- [[sources/2026-04-17-tg-portnyaginlive-11158-11161-duplicate]] — bundle-audit того же backfill-дропа (4 видео «Люди Siberia»)
- [[sources/2026-04-17-tg-portnyaginlive-11166-duplicate]] — индивидуальный audit того же backfill-дропа (видео «Конец пищевой цепочки»)
