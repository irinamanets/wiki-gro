---
id: mkt:sources/2026-05-05-tg-gurinovich-shares-may-2026-duplicate
title: Telegram @gurinovich_shares — backfill дамп 50 постов 22 янв – 20 апр 2026 (bundle-дубль апрельского ingest + 1 новый пост 911)
type: source
layer: evolving
theme: content-trends
tags: [telegram, post, duplicate-bundle, audit-only, gurinovich]
confidence: medium
created: 2026-05-05
updated: 2026-05-05
original: raw/processed/articles/tg_gurinovich_shares_20260505-133859.md
bundle_primary: raw/processed/articles/tg_gurinovich_shares_20260505-133859.md
bundle_children:
  - raw/processed/media/tg_gurinovich_shares_862.jpg
  - raw/processed/media/tg_gurinovich_shares_864.jpg
  - raw/processed/media/tg_gurinovich_shares_866.jpg
  - raw/processed/media/tg_gurinovich_shares_869.jpg
  - raw/processed/media/tg_gurinovich_shares_871.jpg
  - raw/processed/media/tg_gurinovich_shares_875.jpg
  - raw/processed/media/tg_gurinovich_shares_877.jpg
  - raw/processed/media/tg_gurinovich_shares_879.jpg
  - raw/processed/media/tg_gurinovich_shares_882.jpg
  - raw/processed/media/tg_gurinovich_shares_884.jpg
  - raw/processed/media/tg_gurinovich_shares_885.jpg
  - raw/processed/media/tg_gurinovich_shares_886.jpg
  - raw/processed/media/tg_gurinovich_shares_887.jpg
  - raw/processed/media/tg_gurinovich_shares_890.jpg
  - raw/processed/media/tg_gurinovich_shares_895.jpg
  - raw/processed/media/tg_gurinovich_shares_897.jpg
  - raw/processed/media/tg_gurinovich_shares_898.jpg
  - raw/processed/media/tg_gurinovich_shares_899.jpg
  - raw/processed/media/tg_gurinovich_shares_900.jpg
  - raw/processed/media/tg_gurinovich_shares_901.jpg
  - raw/processed/media/tg_gurinovich_shares_902.jpg
  - raw/processed/media/tg_gurinovich_shares_903.jpg
  - raw/processed/media/tg_gurinovich_shares_905.jpg
  - raw/processed/media/tg_gurinovich_shares_909.jpg
  - raw/processed/video/tg_gurinovich_shares_870.mp4
  - raw/processed/video/tg_gurinovich_shares_896.mp4
namespace: mkt
---

# Telegram @gurinovich_shares — backfill дамп 2026-05-05 (bundle-дубль)

## Метаданные
- **Тип:** Telegram channel dump (Markdown + 24 jpg + 2 mp4, bundle ingest)
- **Канал:** [@gurinovich_shares](https://t.me/gurinovich_shares) — «Гуринович делится!»
- **Автор:** Эдуард Гуринович — серийный предприниматель, Forbes 30 under 30, основатель CarPrice, соучредитель медиа-холдинга «Основатели». См. полный профиль автора в родительском source [[sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026]].
- **Даты постов:** 2026-01-22 18:56 UTC … 2026-04-20 08:48 UTC (50 постов, ids 862–911)
- **Дата добавления:** 2026-05-05 13:38 UTC (scheduled backfill task «Эдуард Гуринович»)
- **Sidecar note:** был. Цитата: «Это источник новостей по тематике "Телеграм — Авторские". Серийный предприниматель, Forbes 30 under 30. Эти данные ... используем для написания своих постов и новостей в блоге нашего сервиса.» — идентичен sidecar родительского ingest, content-pipeline для блога GRO.
- **Sensitive flag:** none — публичный канал, PII/credentials отсутствуют.

## Статус — bundle-дубль уже обработанного канального дампа

Этот дамп почти полностью совпадает с уже обработанным канальным bundle-source [[sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026]] (50 постов, ids 861–910).

**Перекрытие:** 49 постов (862..910) — идентичный текст, идентичная семантика. Все 7 релевантных извлечений из родительского ingest (861/874/869/875/876/888/904) уже синтезированы в layer-страницы:

- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] (пост 861/874)
- [[evolving/content-trends/ai-solopreneur-narrative-hooks]] (пост 861/874/869)
- [[evolving/content-trends/ai-flattery-dark-pattern]] (пост 888)
- [[evolving/content-trends/ru-business-tg-content-drift-2026]] (пост 904)
- [[evolving/content-trends/ai-agents-demand-hooks-2026]] (пост 869/876/888)
- [[evolving/content-trends/telegram-native-formats]] (пост 875)

**Различия:**

1. **Пост 861** (контекстный пост «вайб-кодинг как подростковый секс») в этом дампе **отсутствует** — родительский дамп начинался с 861, текущий — с 862. Содержательной потери нет: пост 874 в текущем дампе ссылается на пост 861 по якорю, и сам тезис «инфляция навыка вайбкодинга» уже зафиксирован.
2. **Пост 911** (2026-04-20 08:48 UTC) — НОВЫЙ, в родительском дампе отсутствовал. Личный пост о дне рождения автора («В свои 35 лет ... продолжаю оставаться оптимистом и стараюсь не терять энергию»). См. раздел «Релевантность» ниже.
3. **Файлы 862.jpg и 871.jpg** — в текущем дампе физически новые (нет MD5-совпадения в `raw/processed/media/`). В родительском bundle для этих постов сохранены `.mp4` варианты (cover/превью видео). Это означает, что Telegram-экспортёр в этот раз сохранил статичные обложки вместо видео-вариантов — то же самое содержимое поста, разные форматы attachment. Vision-описания не делаем, потому что эти посты (862 — Березовский / docu-промо, 871 — Ракета-промо) уже классифицированы как **нерелевантные** в родительском source (self-promo/personal). Превью-кадр из `.mp4` ничем содержательно не дополняет уже зафиксированное.
4. **24 остальных media + 2 видео** — MD5-идентичные дубли уже обработанных файлов (см. таблицу проверки ниже).

## Релевантность

**No relevant extractions.** Bundle audit-only.

- 49 перекрывающихся постов уже извлечены в родительском ingest. Дублировать факты в layer-страницы запрещено (нарушение supersession-инвариантов и DRY).
- 1 новый пост (911) — личный («день рождения, 35 лет, оптимизм»), без marketing/industry/product-сигнала. Per `wiki/rules.md` → раздел «Релевантность сырых источников» → «Personal/off-topic», «Мотивационная "вода"» — нерелевантно. В layer не идёт.
- 2 новых физических файла (862.jpg, 871.jpg) принадлежат уже-классифицированным как нерелевантным постам (Березовский docu-промо / Ракета-промо). Vision-проход не выполняется (как и в родителе).

## Проверка дублирования (MD5-сравнение pending vs processed)

| Файл | Статус | Действие |
|---|---|---|
| tg_gurinovich_shares_862.jpg | NEW (no processed counterpart, родитель сохранил `.mp4`) | move to processed (no vision — irrelevant post) |
| tg_gurinovich_shares_871.jpg | NEW (no processed counterpart, родитель сохранил `.mp4`) | move to processed (no vision — irrelevant post) |
| tg_gurinovich_shares_864.jpg | DUP (MD5-совпадение) | move to processed (overwrites identical) |
| tg_gurinovich_shares_866.jpg | DUP | move to processed |
| tg_gurinovich_shares_869.jpg | DUP | move to processed |
| tg_gurinovich_shares_875.jpg | DUP | move to processed |
| tg_gurinovich_shares_877.jpg | DUP | move to processed |
| tg_gurinovich_shares_879.jpg | DUP | move to processed |
| tg_gurinovich_shares_882.jpg | DUP | move to processed |
| tg_gurinovich_shares_884.jpg | DUP | move to processed |
| tg_gurinovich_shares_885.jpg | DUP | move to processed |
| tg_gurinovich_shares_886.jpg | DUP | move to processed |
| tg_gurinovich_shares_887.jpg | DUP | move to processed |
| tg_gurinovich_shares_890.jpg | DUP | move to processed |
| tg_gurinovich_shares_895.jpg | DUP | move to processed |
| tg_gurinovich_shares_897.jpg | DUP | move to processed |
| tg_gurinovich_shares_898.jpg | DUP | move to processed |
| tg_gurinovich_shares_899.jpg | DUP | move to processed |
| tg_gurinovich_shares_900.jpg | DUP | move to processed |
| tg_gurinovich_shares_901.jpg | DUP | move to processed |
| tg_gurinovich_shares_902.jpg | DUP | move to processed |
| tg_gurinovich_shares_903.jpg | DUP | move to processed |
| tg_gurinovich_shares_905.jpg | DUP | move to processed |
| tg_gurinovich_shares_909.jpg | DUP | move to processed |
| tg_gurinovich_shares_870.mp4 | DUP | move to processed |
| tg_gurinovich_shares_896.mp4 | DUP | move to processed |

24 DUP + 2 NEW (но irrelevant) = 26 children, 1 primary article. Audit-фиксация без новых синтезированных страниц.

## Содержание (для audit)

Полный текст постов 862–911 — в `raw/processed/articles/tg_gurinovich_shares_20260505-133859.md`. Резюме семантики уже зафиксировано в [[sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026]] для постов 862–910.

**Пост 911 — единственный новый (audit-фиксация, в layer не идёт):**

> «Пройдя земную жизнь до половины, я очутился в сумрачном лесу (с) — В свои 35 лет я себя ощущаю намного взрослее, опытнее, прохожу сложные уровни испытаний, но продолжаю оставаться оптимистом и стараюсь не терять энергию! Вторая "половина" жизни будет точно интереснее, так что не переключаемся, полный вперед!»
>
> Хэштеги: #деньрождения #мудрость
>
> Дата: 2026-04-20 08:48 UTC

Классификация: personal/off-topic, motivational. Без marketing/product/audience-сигнала. Per `wiki/rules.md` секция «Нерелевантно».

## Транскрипты медиа

Дубли уже-обработанных файлов 870.mp4 и 896.mp4. Их транскрипты зафиксированы в родительском bundle-source [[sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026]] секция «Транскрипты медиа»:

- 870.mp4 — VAD: no speech detected (видео без речи, demonstration of the device).
- 896.mp4 — 12 сек, рус., «До откуда взялась печаль?» — личный комментарий.

Оба нерелевантны.

## Связанные страницы

- [[sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026]] — родительский канальный bundle-дамп, где все семантически совпадающие посты (862–910) уже извлечены и синтезированы
- [[evolving/content-trends/ai-flattery-dark-pattern]] — GRO-релевантная страница, построенная на посте 888 родителя (повторно не обновляется)
- [[evolving/content-trends/ru-business-tg-content-drift-2026]] — построена на посте 904 родителя (повторно не обновляется)
