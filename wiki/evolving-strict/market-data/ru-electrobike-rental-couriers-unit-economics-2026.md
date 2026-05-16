---
id: mkt:evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026
title: "Электробайк-rental для курьеров — RU unit-economics март 2026 (бенчмарки)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [smb, ru, courier-rental, ebike, unit-economics, dds, b2c, b2b, fleet, sezon]
confidence: low
stale: false
created: 2026-05-06
updated: 2026-05-06  # +month-1 partial DDS из выпуска #5/5 финала (OFJAPdavM3s, дата съёмки 2026-03-19): выручка 675 800 ₽ (581 500 аренда + 89 000 продажа тук-тук + 4 800 сервис + 1 000 запчасти), расходы 360 530 ₽, прибыль 315 269 ₽, ZP 4000/смена piece-rate × 39 смен = 158 000 ₽ ФОТ, marketing 42 000 ₽ (vs 25 126 ₽ в month-3 — explained как winter-warming), patent 50 000 ₽/год. Trajectory month-1 → month-3: +32% ЧДП, +31,6% ФОТ. B2C tariff 4 000 ₽/нед в кадре (vs 6 000 ₽/нед в #1/#4) — добавлено в Contradictions. 2 «трупа» из 47 в первой партии (контроллер + курьер сжёг) → defect/incident rate 2/45 = ~4,4%. Damage cost-share 50/50 для unclear-fault инцидентов, курьер платит 500 ₽/нед в рассрочку
sources: [sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc.md, sources/2026-05-06-yt-biznes-s-nulya-electrobike-prequel-decision-procurement.md, sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet.md]
namespace: mkt
---

# Электробайк-rental для курьеров — RU unit-economics март 2026

Бенчмарки по категории **"prokat электровелосипедов для курьеров доставки в РФ, ранний-стадии SMB"**, single-source из founder-DIY эпизода Муратаева ([[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]]). Confidence: **low** — это **один founder-кейс одного месяца**, не отраслевая выборка. Используется как **сетевая точка** для сравнения с будущими ingest'ами этой же или соседних категорий.

**Caveat от founder'а:** «Пока это не говорит вам цифры, сколько мы действительно заработали за март, мы сведём АПУ» — `[conf:low, src:2026-05-05]`. То есть founder сам пометил: ДДС ≠ прибыль. Амортизация (3,5%/мес × парк) пока не вычтена.

## Investment + revenue baseline

| Параметр | Значение | Source-marker |
|---|---|---|
| Total investment (4 мес) | 4 800 000 ₽ | `[conf:low, src:2026-05-05]` |
| Monthly rental revenue (март) | 959 200 ₽ | `[conf:low, src:2026-05-05]` |
| Repair-side revenue | 25 520 ₽ | `[conf:low, src:2026-05-05]` |
| Parts-sale revenue | 300 ₽ (маргинальный) | `[conf:low, src:2026-05-05]` |
| Total inflows | ~1 198 000 ₽ | `[conf:low, src:2026-05-05]` |
| Total outflows | 781 000 ₽ | `[conf:low, src:2026-05-05]` |
| Net cash flow (NCFO) | 417 000 ₽ | `[conf:low, src:2026-05-05]` |
| Cash balance end-of-period | 765 000 ₽ | `[conf:low, src:2026-05-05]` |
| Bike fleet size | 47 байков | `[conf:low, src:2026-05-05]` |
| Founder's break-even ETA | 10+ месяцев | `[conf:low, src:2026-05-05]` |

**Разрыв revenue:** 916 000 ₽ vs 959 200 ₽ упомянуты в разных частях эпизода — расхождение в пределах 5%, скорее всего one округлённое vs другое детализированное. `[conf:low, src:2026-05-05]`

## Tariff structure (B2C vs B2B)

| Сегмент | Цена/байк/мес | Рекуррентность | Маржа vs reference |
|---|---|---|---|
| B2C (частный курьер) | 24 000 ₽/мес = 6 000 ₽/нед × 4 | По неделе, средний срок 1-4 нед | Reference (100%) `[conf:low, src:2026-05-05]` |
| B2B (курьерская компания, anchor: Важная Рыба) | 16 000 ₽/мес × 7 байков, **год вперёд** | Recurring × 12 мес | **−33% per bike** vs B2C, но **+12 мес commitment** `[conf:low, src:2026-05-05]` |

**Sample**: anchor B2B-customer = 7 байков × 16 000 ₽/мес = **112 000 ₽/мес recurring** = **1 344 000 ₽/год** на одном контракте. `[conf:low, src:2026-05-05]`

**Trade-off framework:** founder сознательно соглашается на **−33% маржу за байк** в обмен на: `[conf:low, src:2026-05-05]`
- Year-ahead commitment (12 × cash flow visibility)
- Customer-acquisition cost = 0 (через personal network)
- One-touch operations (не reprocess договор каждую неделю)

Подробнее в [[canon/marketing-frameworks/b2b-pivot-anchor-customer-smb]].

## OPEX breakdown (март 2026)

| Категория | Сумма (₽) | % от total OPEX | Source-marker |
|---|---|---|---|
| ФОТ | 208 000 | 26,6% | `[conf:low, src:2026-05-05]` |
| Капитальные вложения / активы | 143 000 | 18,3% | `[conf:low, src:2026-05-05]` |
| Закупка байков (новая партия) | 80 000 | 10,2% | `[conf:low, src:2026-05-05]` |
| Покупка У-велосипедов (доплата при замене парка) | 70 000 | 9,0% | `[conf:low, src:2026-05-05]` |
| Офис и склад (всего) | 73 000 | 9,4% | `[conf:low, src:2026-05-05]` |
| — Аренда помещений | 32 750 | 4,2% | `[conf:low, src:2026-05-05]` |
| — Установка камер | 31 000 | 4,0% | `[conf:low, src:2026-05-05]` |
| — Офисные расходы | 9 869 | 1,3% | `[conf:low, src:2026-05-05]` |
| Покупка оборудования (инструмент) | 67 000 | 8,6% | `[conf:low, src:2026-05-05]` |
| **Маркетинг (всего)** | **58 956** | **7,5%** | `[conf:low, src:2026-05-05]` |
| — Авито | 25 126 | 3,2% | `[conf:low, src:2026-05-05]` |
| — Брендинг (типография + наклейки) | 32 000 | 4,1% | `[conf:low, src:2026-05-05]` |
| — Реферальная программа курьерам | 1 500 | 0,2% | `[conf:low, src:2026-05-05]` |
| Закупка расходников | 31 312 | 4,0% | `[conf:low, src:2026-05-05]` |
| Прочие расходы | 9 810 | 1,3% | `[conf:low, src:2026-05-05]` |
| **Total** | **781 000** | 100% | `[conf:low, src:2026-05-05]` |

**Marketing-specific бенчмарк**: **7,5% от monthly OPEX уходит на маркетинг** в этом case'е. Это **низкий процент** для consumer-бизнеса (типичный B2C SMB в РФ — 10-20%), что косвенно подтверждает founder'скую тезис «маркетинг работает через сарафан + наклейки + геолокация рядом с дарксторами, не через paid». `[conf:low, src:2026-05-05]`

**FOT-distribution внутри 208 000 ₽/мес ФОТ:** `[conf:low, src:2026-05-05]`
- Ахмат (главный технарь, переманенный) — 150 115 ₽/мес `[conf:low, src:2026-05-05]`
- Андрей (operations co-founder) — 48 000 ₽/мес (не с самого начала) `[conf:low, src:2026-05-05]`
- Аутсорс (бухгалтер + юрист + ассистент) — 10 000 ₽/мес `[conf:low, src:2026-05-05]`

Это **операционно интересный signal**: главный технарь зарабатывает **в 3 раза больше operations-партнёра**. Объясняется тем, что Ахмат был переманен с Yandex.Лавка ПВЗ с прибылью 70-80 тыс ₽/мес, поэтому **floor для retention** = существенно выше market rate. Это applied case [[canon/marketing-frameworks/employee-retention-cost-bredova]].

## Unit pricing (BIKE assets)

| Параметр | Значение | Source-marker |
|---|---|---|
| Полный байк (U5) | ~75 000 ₽ | `[conf:low, src:2026-05-05]` |
| Аккумулятор (большой) | ~55 000 ₽ | `[conf:low, src:2026-05-05]` |
| Корпус-без-аккумулятора | ~20 000 ₽ | `[conf:low, src:2026-05-05]` |
| **% аккумулятора в цене байка** | **~73%** | `[conf:low, src:2026-05-05]` |

**Implication**: при операционной модели «менять аккумулятор как самый часто-failing компонент» — exposure на **главную capital-cost component** через standardization. `[conf:low, src:2026-05-05]`

## Amortization assumption

- **Founder's assumption**: байк проживёт **18 месяцев** в активной аренде (пессимистичнее официальной гарантии **36 мес** от поставщика)
- **Monthly amortization rate** = 1 / 18 = **5,55%** (founder округляет до **3,5%**) `[conf:low, src:2026-05-05]`

Note: расхождение между 5,55% (теоретический рассчёт) и 3,5% (озвученной founder'ом) скорее всего объясняется тем, что founder вычитает амортизацию **только для активной части парка**, а не от всего investment-base. Точная формула не обсуждается в эпизоде. `[conf:low, src:2026-05-05]`

При monthly amortization 3,5% × 47 байков × 75 000 ₽ ≈ **123 000 ₽/мес «бумажной» амортизации** — что **−30% от ЧДП 417 000 ₽**. Это reduces real-profit с 417 → ~294 тыс ₽/мес и **меняет break-even ETA с 10 мес на ≈16 мес** — founder признаёт это implicitly: «минимальная окупаемость 10 месяцев, а то и больше». `[conf:low, src:2026-05-05]`

## Payment fees (SBP vs Card)

| Метод | Комиссия | Использование в кейсе |
|---|---|---|
| QR-код / SBP | **0,7%** | Default по политике founder'а | `[conf:low, src:2026-05-05]` |
| Карта (физическая) | **2,2-2,6%** (varies by bank) | Avoid where possible | `[conf:low, src:2026-05-05]` |
| Удалённая ссылка-онлайн | **0,7%** (тоже SBP) | Для продления без визита | `[conf:low, src:2026-05-05]` |

**Operational impact**: при monthly inflows 1 198 000 ₽, разница 1,5 п.п. = **~18 000 ₽/мес сэкономленных** на одном выборе payment-method. `[conf:low, src:2026-05-05]`

## Default + collection metrics

| Параметр | Значение | Source-marker |
|---|---|---|
| Active rentals (март, оценка) | ~50 байков | `[conf:low, src:2026-05-05]` |
| Default cases (просрочка >5 дней) | 1 кейс | `[conf:low, src:2026-05-05]` |
| Default rate (раннняя выборка) | ~2% | `[conf:low, src:2026-05-05]` |
| Soft-collection метод | Блокировка ручки газа дистанционно (telematics) | `[conf:low, src:2026-05-05]` |
| Hard-collection метод | Бумажка-объявление на байк, потом изъятие | `[conf:low, src:2026-05-05]` |

**Telematics requirement** (operational must-have): без kill-switch'а unit-economics rental-бизнеса не работает — default rate 2% при **неконтролируемом активе** = unacceptable risk. `[conf:low, src:2026-05-05]`

## Залоговая механика

| Параметр | Значение | Source-marker |
|---|---|---|
| Возврат залога март (out) | 28 200 ₽ | `[conf:low, src:2026-05-05]` |
| Сумма залогов на момент эпизода | «намного больше», не указано | — |
| Удержание за зеркало | ~700 ₽ | `[conf:low, src:2026-05-05]` |
| Стоимость наклеек (для удержания если сняли) | ~450 ₽ | `[conf:low, src:2026-05-05]` |
| Plan: future штраф за снятие наклейки | 3 000 ₽ (anchor, обсуждается) | `[conf:low, src:2026-05-05]` |

## Sezon-pattern (counter-intuitive)

Quoted finding from founder: **зима = main season, лето = низкий сезон** для food-delivery courier rentals в РФ. `[conf:medium, src:2026-05-05]`

**Driver**: behaviour конечного потребителя (заказывает доставку зимой, гуляет летом) → spike в food-delivery courier demand зимой → bike-rental demand зимой → **opposite of naive bike-rental seasonality** (где сезон = летние месяцы для прогулочной аренды). `[conf:medium, src:2026-05-05]`

**Marketing-implication**: AOV / fleet-utilization будет иметь **зимний пик**, и paid-marketing нужно усиливать **октябрь-ноябрь**, не март-май. `[conf:medium, src:2026-05-05]`

## Acquisition channels (бенчмарки внутри 25 126 ₽ Авито-spend) `[conf:low, src:2026-05-05]`

- **Авито-share от total marketing**: 25 126 / 58 956 = **42,6% маркетинг-бюджета** идёт на единственный paid-канал. `[conf:low, src:2026-05-05]`
- **Реферальная economics**: 500 ₽ × 3 курьера = 1 500 ₽ за приведённых трёх клиентов → **CPA = 500 ₽** (incidental, не scaled). `[conf:low, src:2026-05-05]`
- **Founder's note: «Звонки подсбавились»** на Авито к концу марта → ranky platform plateau effect, supply-side saturation в этой нише на этом канале. `[conf:low, src:2026-05-05]`

**Implication**: paid-acquisition в этой нише в 2026 имеет **низкий ceiling** — после ~25 000 ₽/мес на Авито дальше масштабировать тяжело. Sequential channel rollout (Yandex.Pro, парки) рассматривается founder'ом, но **только когда парк байков увеличится** (т.е. supply должен расти быстрее, чем acquisition spend). `[conf:low, src:2026-05-05]`

## Supplier-side benchmarks

| Параметр | Значение | Source-marker |
|---|---|---|
| Gold standard supplier defect rate (DC-зарядка) | 1 / 47 байков = ~2% | `[conf:low, src:2026-05-05]` |
| Lag для появления запчастей на новой модели | ~1 год от выхода | `[conf:low, src:2026-05-05]` |
| Гарантия от поставщика | 36 месяцев | `[conf:low, src:2026-05-05]` |
| ТО-cycle | Раз в 3 недели летом, чаще зимой | `[conf:medium, src:2026-05-05]` |

## Day-0 procurement breakdown (prequel-эпизод, ~декабрь 2025 / январь 2026)

Из chronologically-предшествующего эпизода ([[sources/2026-05-06-yt-biznes-s-nulya-electrobike-prequel-decision-procurement]] — момент закупки до запуска проекта в Парнасе) зафиксирован **per-supplier basket** на старте, который не показан в #4 (там — agregate за 4 месяца).

| Параметр | Значение | Source-marker |
|---|---|---|
| Procurement basket (Day-0) | 4 043 372 ₽ | `[conf:medium, src:2026-05-06]` |
| — у Анатолия (Москва, дистрибьютор китайского завода, бренд H/U) | 2 919 250 ₽ | `[conf:medium, src:2026-05-06]` |
| — у второго поставщика (название не озвучено) | 820 000 ₽ | `[conf:medium, src:2026-05-06]` |
| — мелкие расходники | 100 000 ₽ | `[conf:medium, src:2026-05-06]` |
| Доставка байков из Москвы в СПб | 82 350 ₽ | `[conf:medium, src:2026-05-06]` |
| **Total Day-0 capital outflow на байки + доставку** | **4 125 722 ₽** | `[conf:medium, src:2026-05-06]` |
| Bike fleet at procurement | 45 байков (план), смесь U5 / H10 / U2 | `[conf:medium, src:2026-05-06]` |
| Founder's pre-trip plan (озвучено в pitch) | ~4,5 млн ₽ | `[conf:medium, src:2026-05-06]` |

**Implication для break-even ETA:** Day-0 procurement = 4,1 млн ₽ vs total 4-month investment 4,8 млн ₽ (#4) → **за 4 месяца founder доинвестировал ~700 тыс ₽** (новые модели, инструменты, инфраструктура). Это ~23% от Day-0 в follow-on capex — **стандартный pattern для capital-intensive rental businesses**: значительная часть ongoing capex на 1-й год обновления парка. `[conf:medium, src:2026-05-06]`

### Per-model unit prices (Day-0 supplier-quotes, на запись телефонного разговора)

| Модель | Цена за байк | Поставщик | Notes |
|---|---|---|---|
| U5 | 74 000 ₽ | Анатолий | Базовая модель парка | `[conf:medium, src:2026-05-06]` |
| H10 | 85 000 ₽ | Анатолий | Премиум-модель, на момент звонка осталось 5–10 шт | `[conf:medium, src:2026-05-06]` |
| U2 | 85 000 ₽ | Анатолий | Документально >250 кВт → требует прав от курьера, 70 А·ч | `[conf:medium, src:2026-05-06]` |
| Венбокс У3 (с малым аккумулятором) | 45 000–50 000 ₽ | Второй поставщик | 5–6 ч работы | `[conf:medium, src:2026-05-06]` |
| Венбокс с большим аккумулятором | 65 000–75 000 ₽ | Второй поставщик | 10–12 ч работы | `[conf:medium, src:2026-05-06]` |

**Confirmation для тезиса «аккумулятор = 50%+ стоимости байка»:** Венбокс с small battery 45–50 тыс vs same bike с large battery 65–75 тыс → **delta аккумулятор = 20–25 тыс ₽ = ~30% разницы цены**, что согласуется с #4-baseline «аккумулятор ~55K из 75K = ~73%». `[conf:medium, src:2026-05-06]`

### Supplier landscape (РФ 2026)

| Бренд | Repute (по Муратаеву) | Запчасти в РФ |
|---|---|---|
| H8/H10/U2/U5 (Анатолий, Москва) | Founder выбрал → закупка | В наличии у поставщика | `[conf:medium, src:2026-05-06]` |
| Венбокс | «очень крутые» | Доступны на рынке | `[conf:medium, src:2026-05-06]` |
| Майколин | «новый, не ломаются» | Доступны | `[conf:medium, src:2026-05-06]` |
| Куга | «классные велики» | **Запчасти нигде нет — ни на рынках, ни на Авито, ни у поставщиков** → deal-breaker | `[conf:medium, src:2026-05-06]` |

**Operational rule from supplier-research** (founder выводит на запись): **«запчасти всегда появляются примерно через несколько сезонов, как вышла модель»** = **lag запчастей ≈ 1 год** от выхода новой модели. Согласуется с supplier landscape benchmark из #4 (отсутствие запчастей U5 в начале 2026). `[conf:medium, src:2026-05-06]`

### Pre-launch competitor-pricing intelligence (mystery-shopping)

Founder снимает на запись 3 phone calls — **исследование рынка до закупки**:

| Параметр | Конкурент (mystery-shopped как доставка суши) |
|---|---|
| Конкурент monthly tariff | 15 800 ₽/мес `[conf:medium, src:2026-05-06]` |
| Конкурент weekly tariff | 3 950 ₽/нед = ≈15 800 ₽/мес × 4 нед `[conf:medium, src:2026-05-06]` |
| Модель | Monstr Tracks с **2** аккумуляторами `[conf:medium, src:2026-05-06]` |
| Один аккум хватает на | 5–6 часов (зимой 5 ч из-за холода) `[conf:medium, src:2026-05-06]` |
| Заявленный велопарк конкурента | «более 200 байков» (founder discounts as overstated) `[conf:low, src:2026-05-06]` |
| Свободных в один день | 20 байков (по словам конкурента) `[conf:low, src:2026-05-06]` |
| Service-bezopasnosti фильтр | Судимость / кредитная история / криминал `[conf:medium, src:2026-05-06]` |

**Implication для tariff-strategy:** founder выходит на рынок **выше конкурента**: его B2C 6 000 ₽/нед vs конкурент 3 950 ₽/нед = **+52% premium**. Trade-off — **сервис на месте + новые байки + open-doors**. К месяцу #4 это работает (см. #4 baseline 24 000 ₽/мес vs 15 800 ₽/мес у конкурента, **52% premium retained**), но требует supplementary value (сервис как retention-asset). `[conf:medium, src:2026-05-06]`

### Авито-density конкурентов на момент geo-выбора (Day-0)

| Локация | Объявлений на Авито (на момент анализа founder'а) | Курьерский спрос (qualitative) |
|---|---|---|
| Кудрово | 28 | высокий | `[conf:medium, src:2026-05-06]` |
| Мурино | 32 | высокий | `[conf:medium, src:2026-05-06]` |
| Парнас / Парголово | **2** | высокий (даркстор Самокат + Яндекс.Лавка) | `[conf:medium, src:2026-05-06]` |

**Decision criterion:** **inverse-конкурентность × ICP-density** = best location. Founder выбрал Парнас по этому правилу. К месяцу #4 (~3 мес после) данное решение **подтвердилось через результат** (см. #4: «здесь базируется самокат и здесь базируется Яндекс.Лавка», «огромный плюс — мы можем запуститься без рекламы»). `[conf:medium, src:2026-05-06]`

**Reusable benchmark для location-based SMB:** при разнице **2 vs 28 listings** конкурентов (≈14× разница в supply) и **сопоставимой density спроса** — выбор низко-конкурентной локации даёт **near-zero paid acquisition** в первые месяцы (что согласуется с #4 marketing 7,5% от OPEX, и founder говорит «мы можем запуститься без рекламы»).

## Month-1 partial DDS (20 февраля — 19 марта 2026, выпуск #5/5)

Из финального выпуска серии ([[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]]) зафиксирован **первый месячный baseline** проекта — chronologically более ранний, чем DDS из #4. Founder показывает в кадре table в Excel, читает каждую цифру out loud. Это даёт **trajectory** month-1 → month-3 для anchor-категории.

| Параметр | Month-1 (20.02–19.03) | Month-3 (полный март) | Δ MoM |
|---|---|---|---|
| Bike fleet | 47 заказано (43 ключа + 4 готовы); 2 «трупа» = 1 контроллер брак + 1 курьер сжёг | 47 байков (~5-7 в B2B, остальное B2C) | стабильно |
| Total inflows | 675 800 ₽ `[conf:medium, src:2026-03-19]` | ~1 198 000 ₽ `[conf:low, src:2026-05-05]` | +77% |
| — Аренда | 581 500 ₽ `[conf:medium, src:2026-03-19]` | 959 200 ₽ `[conf:low, src:2026-05-05]` | +65% |
| — Сервис сторонних | 4 800 ₽ `[conf:medium, src:2026-03-19]` | 25 520 ₽ `[conf:low, src:2026-05-05]` | **+432%** |
| — Запчасти | 1 000 ₽ `[conf:medium, src:2026-03-19]` | 300 ₽ `[conf:low, src:2026-05-05]` | -70% |
| — Прочее (продажа тук-тук как излишек) | 89 000 ₽ (one-off) `[conf:medium, src:2026-03-19]` | продажа U-байков (величина не named) `[conf:low, src:2026-05-05]` | n/a |
| Total OPEX | 360 530 ₽ `[conf:medium, src:2026-03-19]` | 781 000 ₽ `[conf:low, src:2026-05-05]` | +117% |
| ФОТ | 158 000 ₽ (39 смен × ~4 000 ₽) `[conf:medium, src:2026-03-19]` | 208 000 ₽ `[conf:low, src:2026-05-05]` | +31,6% |
| Маркетинг (всего) | 42 000 ₽ `[conf:medium, src:2026-03-19]` | 58 956 ₽ `[conf:low, src:2026-05-05]` | +40% |
| Аренда помещения | 35 000 ₽ (50% from 110 000 + free first month) `[conf:medium, src:2026-03-19]` | 32 750 ₽ `[conf:low, src:2026-05-05]` | стабильно |
| **NCFO (профит)** | **315 269 ₽** `[conf:medium, src:2026-03-19]` | **417 000 ₽** `[conf:low, src:2026-05-05]` | **+32%** |

**Caveat (founder в кадре):** «промежуточные цифры, потому что более детальные хотим дать уже когда март закончится». То есть месяц-1 = **partial period (20.02–19.03 = ~28 дней)**, не календарный март. `[conf:medium, src:2026-03-19]`

### ФОТ структура месяц-1 (piece-rate)

ZP/смена = **4 000 ₽** piece-rate. **39 рабочих смен** в month-1 = ~156 000 ₽ + small adjust = **158 000 ₽**. `[conf:medium, src:2026-03-19]`

В month-3 ФОТ распределён уже: Ахмат 150 115 + Андрей 48 000 + аутсорс 10 000 = 208 000 ₽. То есть **за 2 месяца появился второй механик-Андрей** (в month-1 был только Ахмат + Андрюха-co-founder, см. [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]]). `[conf:low, src:2026-05-05]`

### Marketing-spend pattern (winter-warming → seasonality scaling-down)

В month-1 marketing **42 000 ₽**, в month-3 **25 126 ₽** Авито (+ 32 000 брендинг = 58 956 ₽ всего, but pure Авито-spend ниже). Founder в кадре explains:

> «Мы запустились в феврале при морозах, и спрос на них был маленький, и Андрей каждый день покупал продвижение на сервисе, и они не очень хорошо сдавались. Но как сразу погода наладилась, потеплело, и там просто по 20-30 звонков люди звонят, бронируют, поэтому сейчас уже мы там вкладываем 500 рублей в день, это, наверное, максимум».

**Implication:** **paid acquisition как bridging-traffic в seasonal launch lag** — больше paid в холодные месяцы, меньше когда сарафан + walking-in курьеры через Авито-органику начинают доминировать. Это **opposite** typical retail seasonality (где paid usually scales-up в peak-season). Для bike-rental в РФ — **counter-cyclical paid pattern**: larger paid в low-demand season для bridging cash-flow до warm-pickup. `[conf:medium, src:2026-03-19]`

### Defect rate из новой партии (расширение баselin)

В month-1 founder показывает **2 «трупа» из 45 рабочих байков** (47 заказано, 2 не доехали как working): `[conf:medium, src:2026-03-19]`

- **1 контроллер-брак**: «нажимаем ручку газа, он рывками. Это нужно диагностировать»
- **1 контроллер сожжён курьером**: за **0,5 дня катания** новый байк, поехал в сугробы, забуксовал, mosfet'ы сгорели

**Operational rule founder'а** для unclear-fault инцидентов: **50/50 cost-share** (компания + курьер), курьер платит **500 ₽/нед в рассрочку** поверх обычной аренды. `[conf:medium, src:2026-03-19]`

**Расширенный benchmark defect/incident rate:**

| Источник | Defect/incident | Rate | Period |
|---|---|---|---|
| Month-1 (#5/5) | 1 контроллер-брак + 1 курьер сжёг (50/50 split) | 2/45 = ~4,4% | за первые 4 нед | `[conf:medium, src:2026-03-19]` |
| Month-3 (#4) | 1 DC-зарядка брак | 1/47 = ~2,1% | за месяц-3 | `[conf:low, src:2026-05-05]` |

Combined: **first-batch defect rate ~4-5%** в первые 4 нед (frontload'ed), **stabilized rate ~2%** после. Это **intuitive pattern** для capital assets с supplier-side defects, но **впервые quantified** для bike-rental в РФ. `[conf:medium, src:2026-03-19]`

### Patent налог (специфика SMB-rental)

Founder explicitly: **система патент = 50 000 ₽/год** = ~4 167 ₽/мес. `[conf:medium, src:2026-03-19]`

«Когда вы занимаетесь таким бизнесом, у вас может быть патент. Поэтому очень удобно. Просто вы платите 50 тысяч рублей в год».

**Implication для break-even:** patent как fixed-cost не масштабируется с парком (один патент покрывает unlimited fleet под ту же activity classification) → **economy-of-scale на налоговой стороне** для fleet-rental. `[conf:medium, src:2026-03-19]`

### Inbound-call volume (month-1 raw demand signal)

Founder проговаривает в кадре: `[conf:medium, src:2026-03-19]`

- **Normal day**: 50-60 звонков
- **Peak day**: 100 звонков (рекорд)

**Implication для funnel-conversion**: 50-60 calls/day × 30 = 1 500-1 800 calls/мес в normal-режиме. Из этого ~21 байк сдан в #1 за 2 нед = ~3 байка/день intake. **Conversion рейт inbound-call → bike-rental = 3/55 ≈ 5,5%**. Низкая (но **lead-volume высокий**), что объясняет, почему founder активно нанимает менеджера в #4: «надо это всё свешивать на менеджера». `[conf:medium, src:2026-03-19]`

## Contradictions — B2C tariff range

| Источник | B2C tariff | Notes |
|---|---|---|
| #1 ([[sources/2026-05-05-yt-biznes-s-nulya-electrobike-rental-couriers]]) | 6 000 ₽/нед = 24 000 ₽/мес | implicit baseline `[conf:low, src:2026-05-05]` |
| #4 ([[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]]) | 24 000 ₽/мес | confirmed `[conf:low, src:2026-05-05]` |
| **#5 (этот, дата съёмки 2026-03-19)** | **4 000 ₽/нед** (озвучено в кадре через звонок клиенту) | `[conf:medium, src:2026-03-19]` |
| Prequel ([[sources/2026-05-06-yt-biznes-s-nulya-electrobike-prequel-decision-procurement]]) | 4 000–6 000 ₽/нед как **range у конкурентов** до запуска | `[conf:medium, src:2026-05-06]` |

**Возможные объяснения** (нерезолвенные на момент ingest'а #5/5):

1. **Скидка на запуск** — 4 000 ₽/нед в марте, scale-up до 6 000 ₽/нед к маю
2. **Multiple-tier pricing** — 4 000 ₽/нед на старшую модель U5, 6 000 ₽/нед на премиум-модель (founder в звонке упоминает «несколько моделей»)
3. **Ошибочный recall founder'а** в #1/#4 при озвучивании tariff round to «6 000 ₽» в narrative-context

**Мapping range для marketing-planning:** **B2C tariff = 4 000 — 6 000 ₽/нед** (range), не fixed; зависит от model + period. `[conf:low, src:2026-03-19, src:2026-05-05]`

## Limitations and re-verify triggers

**Single-source caveat:** все numbers выше — из одного эпизода одного founder'а одного месяца (март 2026). Confidence = **low** в плоскости отрасли, **medium** в плоскости конкретного кейса.

**Re-verify triggers** (180 дней TTL):
- Появление выпуска #5 этой серии → April baseline → можно сравнить month-over-month и calibrate
- Independent ingest другой courier-rental компании → validate / contrast benchmarks
- Запуск public benchmark от платформы (Авито Бизнес, OZON, etc.) по **rental-бизнесам в РФ**
- Появление winter-баланса (ноябрь-февраль) → подтверждение / опровержение sezon-pattern

**Не использовать как single-truth для:**
- Investor pitch GRO (обращение к single founder-case без validation)
- Public marketing material (low-confidence numbers с inline-маркерами не годятся)
- Strategic decision-making без cross-reference

**Можно использовать как:**
- Точку отсчёта для discussion в narrative content («вот пример как один SMB-founder делает 416K чистого денежного потока в месяц»)
- Anchor для conversation с rental-business founder'ами
- Frame для понимания, **из чего состоит** OPEX rental-бизнеса (что упускают / что переоценивают новички)

## Связанные страницы

- [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]] — anchor-источник (#4 эпизод, март-baseline = month-3)
- [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-prequel-decision-procurement]] — Day-0 procurement breakdown (chronologically первый эпизод серии)
- [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-rental-couriers]] — выпуск #1 серии (стартап-стадия данные)
- [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]] — выпуск #5/5 финал (month-1 partial DDS 20.02–19.03, defect rate 4,4%, ZP 4000/смена, courier-blogger UGC)
- [[canon/marketing-frameworks/profit-share-service-revenue-smb]] — operational pattern, объясняющий ФОТ-структуру (piece-rate + 33/33/33 на сервис)
- [[canon/marketing-frameworks/business-metrics-for-owners]] — рамка для метрик владельца, applied к этому кейсу
- [[canon/marketing-frameworks/breakage-business-model-fitness]] — соседняя rental-категория (фитнес vs bike) — для contrast
- [[evolving-strict/market-data/ru-fitness-club-unit-economics-2026]] — соседняя rental-юнит-экономика (другая вертикаль)
- [[canon/marketing-frameworks/b2b-pivot-anchor-customer-smb]] — pattern B2B-anchor pivot (производный от этого кейса)
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] — operational philosophy того же founder'а
- [[evolving/content-trends/biznes-s-nulya-founder-diy-format-2026]] — content-формат, через который собираются такие baseline'ы
- [[canon/target-audience/ru-smb-founder-owner-seller]] — ICP-сегмент founder'а этого кейса
