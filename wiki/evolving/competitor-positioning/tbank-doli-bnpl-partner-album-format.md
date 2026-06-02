---
id: mkt:evolving/competitor-positioning/tbank-doli-bnpl-partner-album-format
title: "T-Bank «Доли» — Partner-Album creative template для BNPL-офферов"
type: page
subtype: competitor
layer: evolving
theme: competitor-positioning
tags: [competitor, t-bank, doli, bnpl, creative-template, partnerships, album-format, fashion]
confidence: high
stale: false
created: 2026-04-17
updated: 2026-06-01
sources: [sources/2026-04-14-tg-tinkoffbank-10558-doli-fashion-album.md, sources/2026-06-01-tg-tinkoffbank-may-26-30-2026.md]
namespace: mkt
---

# T-Bank «Доли» — Partner-Album creative template

Воспроизводимый креатив-шаблон, используемый sub-брендом Т-Банка **«Доли»** (buy-now-pay-later — BNPL) для мульти-партнёрских акций: **1 cover-креатив + N brand-cards** с унифицированным logo-lockup'ом и split-payment-UI. Документирую на base-кейсе fashion-album весны 2026 (5 партнёров, 15 продуктов).

Base-case: [[sources/2026-04-14-tg-tinkoffbank-10558-doli-fashion-album]] — TG-альбом @tinkoffbank/10558–10563 (5 карт + 1 cover).

## Анатомия шаблона

### Cover-креатив (1 шт.)
- **Фон:** lavender/светло-сиреневый (sub-brand palette Доли, см. [[evolving/competitor-positioning/tbank-doli-bnpl-sub-brand-palette-lavender]]).
- **Headline:** seasonal-framing, agnostic к конкретному партнёру: «Обновляем гардероб к весне с Долями». Позволяет одной cover-креативу работать на всех N партнёров сразу.
- **Highlight:** название sub-бренда («Долями») выделено tinted-accent-background'ом.
- **Hero:** один-два visual-elements (модель, product-hero) — not product-specific.
- **Disclaimer footer:** мелкий серый текст с лицензией ЦБ РФ в нижнем правом/левом углу.

### Brand-card (×N, одна на партнёра)
- **Top-lockup:** `[логотип партнёра]  |  [лого Доли]` — **pipe-separator co-brand-formula**.
  - Пример: `NIKIFILINI | IIII ДОЛЯМИ`, `POISON DROP | IIII ДОЛЯМИ`.
  - Единая высота логотипов, визуальный parity (партнёр ≡ Доли по weight).
- **Product grid:** 3 продукта от партнёра, разложенных на lavender-фоне как **flat-lay или cutout-stack**.
- **Price-label под каждым продуктом** в двухуровневом формате:

  ```
  [Название продукта]
  [Полная цена] ₽ ([split-сумма] ₽ × 4)
  ```

  Пример: `Свитшот Nikifilini / 10 000 ₽ (2 500 ₽ × 4)`.
- **Нет hero-CTA** внутри brand-card — все CTA инкапсулированы в caption TG-поста (landing-URL для каждого партнёра через `u.tbank.ru/<partner>`).

## Масштабируемость на вертикали

Шаблон partner-agnostic и может переноситься на не-fashion вертикали с минимальной переработкой:

| Вертикаль | Потенциальные партнёры (гипотеза) | Seasonal hook |
|---|---|---|
| Fashion (base-case) | Randewoo, Poison Drop, Nikifilini, Ushatava, Maneken Brand | «Обновляем гардероб к весне» |
| Electronics | re:Store, Ситилинк, DNS, М.Видео, Эльдорадо | «Обновляем технику на новый сезон» |
| Beauty | Golden Apple, Randewoo, Рив Гош, Л'Этуаль | «Готовимся к летнему уходу» |
| Travel | Яндекс.Путешествия, Tutu, Aviasales | «Собираемся в отпуск с Долями» |
| Books/Education | Read Rate, Литрес, Skyeng | «Инвестируем в развитие» |
| Home & Furniture | Hoff, Askona, Belmebel | «Обновляем интерьер» |

**Marginal cost of adding partner = 1 brand-card**. Cover-креатив, caption-template, CTA-workflow переиспользуются. Это делает partner-album **самой экономной мульти-партнёрской механикой** в арсенале Т-Банка (в отличие от indivudual-launch'а типа [[sources/2026-04-14-tg-tinkoffbank-10547-gac-tpremium-partnership|T-Premium × GAC S7]], где один партнёр = весь креативный budget).

## Почему это работает

1. **Scale через lockup-consistency.** Все 5 brand-cards выглядят одинаково (один layout, один фон, одна типографика) — это позволяет **mental batching**: читатель видит это как «Доли предлагают 5 вариантов», а не как 5 отдельных ads.
2. **Price-split UI снимает sticker-shock.** Цена 35 900 ₽ воспринимается как барьер, **8 975 ₽/месяц × 4** — как affordable. Это psycho-financial перфрейминг стандартного BNPL, но **стандартизованный в UI**, что делает его мгновенно читаемым.
3. **Partner logo в lockup = social proof.** Присутствие D2C-premium брендов (Ushatava, Poison Drop, Nikifilini) рядом с Доли сигнализирует: «Доли используются premium-brands, а не только масс-маркетом». Это **up-market positioning** через co-brand association.
4. **Landing-URL через `u.tbank.ru/<partner>` = ecosystem-attribution.** Каждый клик из TG → ecosystem-контролируемая landing-URL, которая позволяет:
   - Attribute conversions на уровне партнёра;
   - Контролировать creative-flow (страница может показывать другие Доли-офферы);
   - Retarget'ить пользователя через Т-Банк-рекламные сети.
5. **Cover seasonal-frame = переиспользуемая креативная единица.** «Обновляем гардероб к весне» работает для всех 5 fashion-партнёров одновременно, и cover можно **re-use в следующем сезоне** с минимальным re-draft'ом («к лету», «к осени»).

## Партнёры base-case (fashion spring 2026)

| Партнёр | Категория | Представление в альбоме | Landing |
|---|---|---|---|
| **Randewoo** | парфюмерия и косметика mid-premium | 3 парфюма (Juliette Has A Gun, Montale, Rabanne) | u.tbank.ru/randewooo |
| **Poison Drop** | ювелирный дизайнер-маркетплейс | 3 украшения (Tannum серьги, 78Glass кольцо, Poison Drop Lab колье) | u.tbank.ru/poisondropp |
| **Nikifilini** | streetwear-premium D2C | 3 item'а одежды (джинсы, свитшот, футболка) | u.tbank.ru/nikifilini |
| **Ushatava** | women's designer-apparel | 3 женских item'а (олимпийка, корсет, юбка) | u.tbank.ru/ushatava |
| **Maneken Brand** | made-in-Moscow casual-oversize | 3 item'а (футболка, бомбер, костюм) | u.tbank.ru/manekenbrand |

**ICP диагностика:** все 5 — **D2C RU-brands в mid-premium сегменте**, не масс-маркет (как Zara/H&M) и не luxury (как Dior/Gucci). Ценовой диапазон 4–35k ₽, мода 10–15k ₽ (см. [[sources/2026-04-14-tg-tinkoffbank-10558-doli-fashion-album]] таблица). Это **consumer-audience, готовый к impulse-purchase**, но нуждающийся в psycho-finance-снижении барьера (split на 4 ×).

## Применение для GRO

1. **Partner-album-шаблон как альтернатива single-partner-кампаниям.** Если GRO планирует мульти-партнёрские акции (cross-promote с fitness-apps, wellness-brands, productivity-tools) — использовать album-format: 1 cover + N cards снижает cost per partner, но требует **унифицированного logo-lockup** и **seasonal-agnostic headline**.
2. **Split-payment UI как коммуникация subscription.** GRO — subscription-продукт (см. [[canon/product-knowledge/gro-pricing-model]]). Применимо: вместо «2 490 ₽/месяц» — «2 490 ₽/мес (82 ₽/день)» или «29 880 ₽/год (2 490 ₽/мес × 12)». Двухуровневое отображение снимает sticker-shock на annual-checkout.
3. **Pipe-separator co-brand lockup `[GRO] | [партнёр]`.** Если GRO co-brand'ит с партнёром (fitness-клуб, бренд одежды, nutrition-brand) — использовать parity-стиль, не sub-logo. Это signal'ит equal-partnership, а не sponsorship.
4. **Landing через свой redirect.** Для attribution — редирект типа `app.gro.run/partner/<name>` позволяет трекать CTR, конверсию и lifetime от каждого партнёра.

## Ограничения шаблона

- **Требует 3+ партнёров за cycle** для оправдания cover-креатива. С 1–2 партнёрами — выгоднее single-launch (типа T-Premium × GAC).
- ~~**Требует category-homogeneity партнёров.** Нельзя смешать fashion-бренд и electronics в одном album'е — читатель теряет контекст.~~ <!-- superseded 2026-06-01 by [[sources/2026-06-01-tg-tinkoffbank-may-26-30-2026]] : майский album смешал мебель/электронику/гардероб/спорт в одном альбоме — homogeneity нужна по occasion/сезону, не по категории товара --> **Уточнено (2026-06-01):** требуется homogeneity не по категории товара, а по **поводу/сезону** (объединяющая occasion-рамка). Майский album смешал 5 разных категорий под рамкой «лето: гардероб и дом» без потери контекста.
- **Seasonal frame требует reset каждый сезон.** Frame «к весне» перестаёт работать к июню. Нужно **календарь партнёрских cycle'ов**, привязанный к fashion/retail seasonality.
- **Price-split UI работает только при BNPL/installment-offer'е.** Для cash-discount или loyalty-rewards — не применимо (UI будет misleading).

## Observed exemplars

| Дата | Партнёры | Категория | Источник | Сезон |
|---|---|---|---|---|
| 2026-04 (spring) | Randewoo, Poison Drop, Nikifilini, Ushatava, Maneken Brand | Fashion & Beauty | [[sources/2026-04-14-tg-tinkoffbank-10558-doli-fashion-album]] | Spring 2026 |
| 2026-05 (summer) | divan.ru, Технопарк, zolla, 12 Storeez, Спортмастер | **Mixed: мебель + электроника + гардероб + спорт** | [[sources/2026-06-01-tg-tinkoffbank-may-26-30-2026]] | Summer 2026 |

(Страница обновляется по мере накопления примеров. REFLECT должен периодически проверять @tinkoffbank и @tinkoffdoli на новые альбомы в других вертикалях для подтверждения/refinement шаблона.)

### Майский album (2026-05) — что подтвердил и что уточнил

Второй наблюдаемый album (@tinkoffbank/10758–10763, «Обновляем летний гардероб и дом с Долями») **подтверждает partner-agnostic-гипотезу** и одновременно опровергает одно из «Ограничений шаблона» ниже:

- **Шаблон сохранён 1-в-1.** Cover seasonal-agnostic («гардероб и дом»), pink/lavender-фон, «Долями» в tinted-accent; на каждой brand-card pipe-separator lockup `[партнёр] | IIII ДОЛЯМИ`; двухуровневый прайс `[полная] ₽ ([split] ₽ × 4)`. То есть креативная единица переиспользована без переработки — ровно как описывает «marginal cost = 1 brand-card».
- **Category-homogeneity НЕ обязательна.** Майский album смешал **мебель (divan.ru), электронику (Технопарк/проигрыватель + проектор), масс-маркет-гардероб (zolla), mid-premium-гардероб (12 Storeez) и спорт/outdoor (Спортмастер)** в одном альбоме. Это прямо опровергает прежнее ограничение «нельзя смешать fashion и electronics — читатель теряет контекст». Объединяющая рамка тут не категория, а **seasonal-occasion** («лето: обновляем гардероб и дом») — занятие, а не товарная группа. Вывод: homogeneity нужна по **поводу/сезону**, не по категории товара.
- **Ценовой диапазон расширен вниз и вверх:** 2 999 ₽ (рубашка zolla, split 750 ₽) … 22 000 ₽ (босоножки 12 Storeez, split 5 500 ₽). split-сумма опустилась до **750 ₽/мес × 4** — Доли давят на ощущение «почти бесплатно» на нижнем сегменте.
- **ICP сместился с premium-D2C на mass-to-mid mix.** Апрельский album был D2C mid-premium (Ushatava, Poison Drop). Майский добавил масс-ритейл (Спортмастер, zolla, Технопарк) — то есть Доли используют один шаблон для двух разных up-market/mass-аудиторий, меняя только набор партнёров.

## Contradictions

- **[2026-06-01]** Ограничение «требует category-homogeneity партнёров» опровергнуто майским album'ом ([[sources/2026-06-01-tg-tinkoffbank-may-26-30-2026]]), где в одном альбоме смешаны мебель, электроника, гардероб и спорт. Резолюция (свежий первичный first-party источник > прежняя гипотеза): homogeneity требуется по **поводу/сезону**, не по товарной категории. Старая формулировка обёрнута в HTML-комментарий в разделе «Ограничения шаблона».

## Связанные страницы

- [[sources/2026-04-14-tg-tinkoffbank-10558-doli-fashion-album]] — primary-источник (fashion album)
- [[sources/2026-06-01-tg-tinkoffbank-may-26-30-2026]] — summer mixed-vertical album (подтверждение scalability)
- [[evolving/competitor-positioning/tbank-doli-bnpl-sub-brand-palette-lavender]] — визуальная палитра Доли
- [[evolving/competitor-positioning/tbank-premium-sub-brand-palette]] — матрица 5 sub-brands T-Bank
- [[evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay]] — consumer-жёлтый (контраст с Доли lavender)
- [[canon/marketing-frameworks/partnerships-growth-multiplier]] — partnerships как рост-мультипликатор
- [[evolving/content-trends/telegram-native-formats]] — формат TG-альбомов

## Backlinks

_5 pages link to this one._

- [[canon/marketing-frameworks/partnerships-growth-multiplier]]
- [[evolving/competitor-positioning/tbank-doli-bnpl-sub-brand-palette-lavender]]
- [[evolving/industry-trends/tbank-corporate-platform-stack-2026]]
- [[index]]
- [[sources/2026-04-14-tg-tinkoffbank-10558-doli-fashion-album]]
