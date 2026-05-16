---
id: mkt:evolving-strict/market-data/ru-labor-market-stagnation-q1-2026
title: "Стагнация найма РФ Q1 2026: hh.индекс, вакансии, конкуренция по секторам"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [labor-market, hiring, hh-index]
confidence: medium
stale: false
created: 2026-04-16
updated: 2026-05-05  # +Batyrev/SuperJob triangulation: −20% вакансий, +33% резюме, 2,2% безработица, 30/28/25 days closure, only 2% планируют массовые сокращения
sources: [sources/2026-04-16-vcru-hr-condensed-37-articles.md, sources/2026-05-05-vc-ru-condensed.md, sources/2026-05-05-yt-batyrev-management-news-mar16-31.md]
namespace: mkt
---

# Стагнация найма РФ Q1 2026

Количественный срез стагнации рынка труда РФ в первом квартале 2026. Данные из vc.ru/hr (публикация stagnatziya-nayma), cross-reference с hh.ru официальными метриками.

## Ключевые метрики

### hh.индекс (резюме на вакансию)
- Январь 2026: 9.6 `[conf:medium, src:2026-04-16]`
- Февраль 2026: 9.8 (РФ) `[conf:medium, src:2026-04-16]`; **independent confirm 9,8 РФ февраль 2026** `[conf:high, src:2026-05-05]`
- Март 2026 (Москва): **10** `[conf:high, src:2026-05-05]` — **independent confirm**
- Март 2026: 11.4 (РФ) `[conf:medium, src:2026-04-16]`
- Март 2025: 5.9 `[conf:medium, src:2026-04-16]`
- Сравнительная база: **в начале 2025 hh.индекс был 3,4–4,8** `[conf:high, src:2026-05-05]` — **двойной рост за год**
- Интерпретация: hh.индекс >8.0 = разворот рынка в сторону работодателя `[conf:medium, src:2026-04-16]`

### Динамика февраль 2026 (м/м и г/г, enrich 2026-05-05)
- Количество **вакансий выросло на 12% м/м**, резюме — на **15% м/м** `[conf:high, src:2026-05-05]`
- Г/г: **вакансий на 27% меньше**, активных резюме на **42% больше** `[conf:high, src:2026-05-05]`

### Зарплата (enrich 2026-05-05)
- Медианная предлагаемая зарплата (РФ, февраль 2026): **84 600 ₽** vs **81 300 ₽ в январе** `[conf:high, src:2026-05-05]`

### Дефицит кадров (enrich 2026-05-05)
- Минтруд: **>2,4 млн человек** общий дефицит `[conf:medium, src:2026-05-05]`
- IT: **>1 млн человек** `[conf:medium, src:2026-05-05]`

### Вакансии и резюме (г/г)
- Активные вакансии: -27-30% г/г `[conf:medium, src:2026-04-16]`
- Число резюме: +39-42% г/г `[conf:medium, src:2026-04-16]`

### Секторный breakdown

| Сектор | Вакансии (г/г) | Резюме (г/г) | hh.индекс Q1 2026 | hh.индекс Q1 2025 | Source |
|---|---|---|---|---|---|
| IT | -36-39% | — | 19.6-21.3 | 9.6-11.3 | `[conf:medium, src:2026-04-16]` |
| Маркетинг | -27-30% | +23-24% | 23-27 | — | `[conf:medium, src:2026-04-16]` |
| Продажи | -28-29% | +41-42% | 7.6-8.1 | 3.8-4.6 | `[conf:medium, src:2026-04-16]` |

Маркетинг -- самая перегретая сфера с 23-27 резюме на вакансию. `[conf:medium, src:2026-04-16]`

## Импликации для GRO

Двукратный рост конкуренции в IT за год и перегрев маркетинга усиливают спрос на самостоятельный карьерный рост (Сегмент 1 GRO -- карьеристы). Content-hook: «23 резюме на одну маркетинговую вакансию -- стандартный подход больше не работает».

## Triangulation от SuperJob (Batyrev, март 2026)

Через [[sources/2026-05-05-yt-batyrev-management-news-mar16-31]] — Батырев цитирует CNews со ссылкой на исследование SuperJob по Q1 2026. **Третий независимый источник** по стагнации (после vc.ru и hh.ru), цифры близки по знаку и порядку:

| Метрика | SuperJob (Батырев) | vc.ru (на этой странице) | Source |
|---|---|---|---|
| Вакансии г/г | **−20%** | −27-30% | `[conf:high, src:2026-03-25]` |
| Резюме г/г | **+33%** | +39-42% | `[conf:high, src:2026-03-25]` |
| Безработица январь 2026 | **2,2%** | — | `[conf:high, src:2026-03-25]` |
| Доля компаний, планирующих массовые сокращения | **2%** | — | `[conf:high, src:2026-03-25]` |
| Закрытие управленческой позиции | **30 дней** | — | `[conf:high, src:2026-03-25]` |
| Закрытие квалифицированного рабочего | **28 дней** | — | `[conf:high, src:2026-03-25]` |
| Закрытие линейного специалиста | **25 дней** | — | `[conf:high, src:2026-03-25]` |

**Расхождение в digit-точности** (SuperJob −20%/+33% vs vc.ru −27-30%/+39-42%) `[conf:high, src:2026-03-25]` объясняется методологиями: разные отрасли в выборках, разные периоды агрегации, разные определения «вакансии»/«резюме» (с фильтром или без). **Содержательно полностью сходится:** оба источника фиксируют одно и то же — двукратный разворот «вакансий меньше, резюме больше», порядок −20-30% / +30-40%.

### Качественная интерпретация Батырева (важно для контента)

- «Это **не про то, что работодатель теперь может выбирать из бесконечного количества резюме**, кандидатов, волшебных матросов. Это про то, что рынок стал **осторожнее**. Цена ошибки в найме выросла, рисковать деньгами никто не хочет».
- «Резюме стало больше — но это не означает, что **качество выросло**».
- «Вакансий стало меньше — но управленческая позиция всё равно закрывается ~30 дней».
- «Компании всё реже набирают новых сотрудников **не потому, что работа стала меньше**, а потому, что **бизнес пересобирает себя**: пытается выжать результаты из тех ресурсов, которые уже есть».

Это интегрирует canon-рамку [[canon/marketing-frameworks/work-recomposition-batyrev]] (пересборка труда) и [[canon/marketing-frameworks/four-baskets-of-roles-batyrev]] (4 корзины) как **прямые ответы на стагнацию**.

### Hook для контента

«В РФ Q1 2026: вакансий −20%, резюме +33%, безработица 2,2%, только 2% компаний планируют массовые сокращения, управленец закрывается 30 дней. `[conf:high, src:2026-03-25]` Это **не "ад на рынке труда"**, это **разворот к работодателю + пересборка системы**. Рефлекс "открыть ещё одну вакансию" больше не работает — нужно сначала пересобрать роль» — anchor-hook для founder-аудитории Сегмента 2.

## Дополнительные структурные сигналы (enrich 2026-05-05)

- ФАС изучает «**зарплатный картель**»: неформальные соглашения работодателей не «хантить» друг у друга и не повышать зарплаты дефицитным специалистам в условиях кадрового дефицита 2026 `[conf:medium, src:2026-05-05]`. Если подтвердится — серьёзный structural-сигнал, что top-50 employer в РФ ведут coordinated wage suppression.
- **Modis (одежда)** подала заявление о банкротстве; за 2 года число магазинов сократилось со **121 до 31** `[conf:medium, src:2026-05-05]`. Это иллюстрация банкротств МСБ под давлением **повышения НДС с 20% до 22% + понижения порога** `[conf:medium, src:2026-05-05]` — структурно высвобождает кадры для других секторов.
- Динамика инвестиций РФ: с **+8,7% в начале 2025 до −3,1% к концу 2025** `[conf:medium, src:2026-05-05]` — макро-фон стагнации.

## Связанные страницы
- [[evolving-strict/market-data/ru-labor-market-q1-2026]] -- более ранний срез (ЦБ + hh)
- [[evolving-strict/market-data/ru-labor-market-hh-2026]] -- hh исследование (n=2683/1314)
- [[evolving/industry-trends/ru-labor-market-employer-turn-2026]] -- качественный анализ разворота
- [[evolving/industry-trends/hiring-trends-russia-2026]] -- 6 трендов найма
- [[evolving-strict/market-data/ru-hr-tech-market-size-2026]] -- объём рынка HR Tech
- [[evolving-strict/market-data/employee-engagement-quiet-quitting-2026]] -- состояние оставшегося штата
- [[evolving/industry-trends/gen-z-workforce-shift-2026]] -- поколенческий контекст
- [[sources/2026-05-05-vc-ru-condensed]] -- vc.ru condensed (46 articles)
- [[sources/2026-05-05-yt-batyrev-management-news-mar16-31]] -- Batyrev/SuperJob 3-й независимый источник стагнации Q1 2026 + качественная интерпретация
- [[canon/marketing-frameworks/work-recomposition-batyrev]] -- canon-рамка «пересборки труда» как ответ на стагнацию
- [[canon/marketing-frameworks/four-baskets-of-roles-batyrev]] -- operational-инструмент пересборки роли

## Backlinks

_17 pages link to this one._

- [[canon/marketing-frameworks/four-baskets-of-roles-batyrev]]
- [[canon/marketing-frameworks/work-recomposition-batyrev]]
- [[canon/target-audience/ru-smb-founder-owner-seller]]
- [[canon/target-audience/senior-employees-50plus-ru-2026]]
- [[evolving-strict/market-data/ru-hiring-cost-benchmarks-2026]]
- [[evolving-strict/market-data/ru-self-employed-2025]]
- [[evolving-strict/market-data/ru-vvp-investment-cooling-2026]]
- [[evolving-strict/market-data/wgsn-future-consumer-2027]]
- [[evolving/industry-trends/gen-z-workforce-shift-2026]]
- [[evolving/industry-trends/return-to-office-global-2026]]
- [[evolving/industry-trends/ru-labor-market-employer-turn-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-04-16-vcru-hr-condensed-37-articles]]
- [[sources/2026-05-05-vc-ru-condensed]]
- [[sources/2026-05-05-yt-batyrev-management-news-mar16-31]]
- [[sources/2026-05-06-yt-rybakov-vvp-trump-oil]]
