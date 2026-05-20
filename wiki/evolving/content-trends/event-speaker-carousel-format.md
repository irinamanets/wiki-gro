---
id: mkt:evolving/content-trends/event-speaker-carousel-format
title: "Event-speaker carousel — формат «hero-коллаж + индивидуальные speaker cards»"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [content, events, awareness, consideration, creative-reference, telegram, vk, carousel]
confidence: medium
stale: false
created: 2026-04-17
updated: 2026-05-19  # +cross-link to Cherednichenko/LZ.Media speaker operational layer (4 страницы)
sources:
  - sources/2026-04-17-tg-tinkoffbank-10539-tolk-pro-speakers.md
  - sources/2026-05-19-pressfeed-lz-media-speaker-first-event-prep.md
namespace: mkt
---

# Event-speaker carousel — формат «hero-коллаж + индивидуальные speaker cards»

Воспроизводимая структура event-анонса с множеством докладчиков: **1 hero-коллаж собирает всех вместе** + **N индивидуальных карточек по одной на спикера**. Наблюдается у крупных RU-игроков для премиум-событий с звёздным кастом (3–6 спикеров).

## Структура carousel'а

| Позиция | Тип | Функция | Что содержит |
|---|---|---|---|
| 1 (hero) | групповой коллаж | attention-grab в ленте, передача общей идеи | все N спикеров на одном изображении + название события + 1–2 строки слогана + логотип |
| 2..N+1 | speaker card | credibility per-speaker | имя + формат (online/offline) + портрет + 1-строчные регалии |

Всё оформление — **единая палитра, единая типографика, единый логотип** на hero. Speaker cards — строго один portrait + text, ничего лишнего: взгляд скользит сверху вниз без competing-элементов.

## Почему формат работает

1. **Hero делает стоп-функцию в ленте** — лицо(а) + крупный текст + бренд-лого ловят внимание в 0,5–1 сек скроллинга.
2. **Speaker cards создают dwell-time** — заинтересованный пользователь листает carousel, алгоритм видит высокий engagement.
3. **Self-segmentation аудитории** — те, кто досмотрел до последней карточки, — самые горячие лиды. Можно retargetить по этому событию.
4. **Social proof стековано** — каждая speaker card добавляет регалию, к концу carousel пользователь накопил 4–6 уровней credibility.

## Критические design-решения

1. **Offline/online-статус в заголовке карточки**, не в отдельной легенде. Одно поле после имени («Джек Швагер (онлайн)», «Янис Варуфакис (офлайн)») — и hybrid-формат мгновенно понятен без дополнительных пояснений. Это решает самую частую UX-проблему анонсов hybrid-конференций.
2. **Один format для всех speaker cards** — не соблазняйтесь выделить звёздного спикера «особенной карточкой». Равномерность держит карусель в ритме: одно портретное поле + один заголовок + одна строка регалий × N. Различие — только в содержимом текста, не в композиции.
3. **Hero — групповой коллаж, не individual star**. Даже если среди спикеров есть суперзвезда — на hero все они стоят вместе. Это сигнал «событие больше, чем один спикер».
4. **Темный драматический фон** — реально помогает лицам и тексту «выйти» из ленты. Тёмно-фиолетовый (Т-Инвестиции), тёмно-синий (конференции Тинькофф Бизнеса), чёрный (event-форумы premium-брендов) — воспроизводимый палитрный подход.

## Hook-формула для caption под каждым спикером

Вместо простой подписи «CEO XYZ Inc.» используется **stacking экспертных регалий по 3 уровням**:

```
🟡 [Имя], [культовая культурная вещь автор/создал]
   [Трек-рекорд в должности: 2–3 конкретные работы, цифры где возможно]
   [Что конкретно разберёт на событии: конкретное обещание]
```

Пример (Т-Инвестиции ТОЛК.PRO):

> 🟡 **Джек Швагер** — автор культовой серии «Маги рынка», признанный инсайдер Уолл-стрит. Его экспертиза сформирована годами работы директором по исследованиям в Prudential Securities и Smith Barney, а также опытом управляющего портфелями в хедж-фондах (The Fortune Group). Спикер подключится онлайн и проведёт структурный разбор, какие три системные ошибки уничтожают капитал 95% трейдеров и какие алгоритмы позволяют оставшимся 5% стабильно обыгрывать рынок на институциональном уровне.

Три уровня credibility читаются последовательно: культура → трек-рекорд → обещание. Каждый закрывает свой тип скептицизма:
- «Кто это вообще?» → культовая вещь
- «Это просто bullshit или реально эксперт?» → конкретный трек-рекорд
- «Зачем мне покупать билет?» → конкретное обещание разобрать X

## Наблюдаемые кейсы

| Кейс | Год/дата | Платформа | Примечания |
|---|---|---|---|
| Т-Инвестиции ТОЛК.PRO (4 апр 2026) | 2026-04 | @tinkoffbank TG | 4 спикера, hero + 4 cards, промокод MART -30%. См. [[canon-strict/historical-campaigns/tbank-tinvest-tolk-pro-2026-04]] |

_Раздел будет дополняться по мере появления новых observed-кейсов через ingest._

## Application для GRO

- **Прямое применение** для hypothesized event'а GRO: если GRO собирает fitness-founder сессию (Лапшина + Егошин + 2 coach-партнёра), этот carousel переносится 1-в-1 — 1 hero + 4 speaker cards.
- **Адаптация для live-stream / webinar**: если event полностью онлайн, формат всё равно работает — просто у всех карточек (онлайн) tag.
- **Перенос на content-series**: carousel можно использовать не только под event, но и под **серию экспертных интервью** в блоге. Hero = «7 голосов о fitness в 2026» + 7 cards, каждая со спикером и 1-строчной цитатой.

## Связанные страницы

- [[canon/marketing-frameworks/speaking-as-marketing-channel]] — спикерство как маркетинговый канал (теория ROI)
- [[canon/marketing-frameworks/speaker-event-type-selection-cherednichenko]] — типология площадок (когда group-collage carousel оправдан для peer-event vs target-audience event)
- [[canon/marketing-frameworks/speaker-marketing-kit-structure-cherednichenko]] — спикерский маркетинг-кит (carousel — публичная демонстрация кита event-организатором)
- [[canon-strict/historical-campaigns/tbank-tinvest-tolk-pro-2026-04]] — базовый наблюдаемый кейс для этого паттерна
- [[evolving/content-trends/telegram-native-formats]] — нативные форматы TG, в т.ч. carousel
- [[evolving/content-trends/sweepstake-promocode-combo-mechanics]] — альтернативная промо-формула (сопоставление: event vs sweepstakes)
- [[evolving/competitor-positioning/tbank-tinvest-premium-positioning]] — как формат поддерживает premium-позиционирование
- [[canon-strict/historical-campaigns/tbank-t-insurance-poleteli-vzr-q1-2026]] — другая кампания того же бренд-дома для contrast (не event, carousel из 2 креативов)

## Backlinks

_6 pages link to this one._

- [[canon-strict/historical-campaigns/tbank-tinvest-tolk-pro-2026-04]]
- [[evolving/competitor-positioning/tbank-tinvest-premium-positioning]]
- [[evolving/content-trends/book-recommendation-carousel-tg]]
- [[evolving/content-trends/factory-tour-pro-day-event-format]]
- [[index]]
- [[sources/2026-04-17-tg-tinkoffbank-10539-tolk-pro-speakers]]
