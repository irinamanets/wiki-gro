---
id: mkt:evolving-strict/competitor-metrics/prodamus-paytech-metrics-2026
title: "Продамус (Prodamus) — операционные метрики PayTech-платформы, 2026"
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [competitor, paytech, online-payments, b2b-platform, ru-saas, founder-metrics, prodamus, mamutkin]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-fomichevkirill-may-6-14-2026.md]
namespace: mkt
---

# Продамус (Prodamus) — операционные метрики, 2026

Снимок операционных метрик PayTech-платформы [Продамус](https://prodamus.ru/) — одной из заметных RU-инфраструктурных платформ для онлайн-школ, экспертов и цифрового бизнеса. Цифры **self-reported founder'ом Романом Мамуткиным** в гостевом профиле рубрики «Коннект» Кирилла Фомичёва (пост [@fomichevkirill/2415](https://t.me/fomichevkirill/2415) от 2026-05-12). См. [[sources/2026-05-14-tg-fomichevkirill-may-6-14-2026|первичный источник]].

`confidence: medium` — single source, founder self-claim, **без независимой верификации** через 1C-отчётность, аудит или регистрационные данные. Контекст для оценки: Мамуткин публиковал эти цифры в продуктовом профиле для networking-сообщества, где founder'у нет смысла занижать оборот, но завышение могло бы привлечь регуляторное внимание — это создаёт moderate floor of accuracy. Цифры воспроизводятся как atributable data point с явной пометкой источника.

## Authority chain

- **Автор данных:** Роман Мамуткин, founder Продамус. Преподаёт в школе бизнеса «Горки» (упомянуто в источнике, без верификации). Статьи на РБК (companies.rbc.ru):
  - «5 этапов роста бизнеса: какие органы формировать на каждом шаге»
  - «Заблуждение о найме CEO: почему собственники ищут не там»
- **Метод получения:** founder self-claim в публичном profile-посте `[conf:medium, src:2026-05-12]`.
- **Транслятор:** Кирилл Фомичёв (@fomichevkirill) в рубрике «Коннект».

## Операционные метрики (self-reported)

| Метрика | Значение | Период | Source |
|---|---|---|---|
| Транзакции (сделки) | 760 000 | в месяц | `[conf:medium, src:2026-05-12]` |
| Оборот (GMV) | 33 млрд ₽ | в год | `[conf:medium, src:2026-05-12]` |
| Выручка платформы | 2,5 млрд ₽ | в год | `[conf:medium, src:2026-05-12]` |

### Derived ratios (вычислимые из self-reported)

| Производная метрика | Значение | Расчёт | Source |
|---|---|---|---|
| Средний чек транзакции | ~3 619 ₽ | 33 млрд ₽ / (760K × 12) = 33 000 000 000 / 9 120 000 = ~3 619 ₽ | `[conf:medium, src:2026-05-12]` |
| Take rate (комиссия платформы) | ~7,6% | 2,5 млрд ₽ / 33 млрд ₽ = 0,0758 | `[conf:medium, src:2026-05-12]` |
| Транзакции в год | 9,12 млн | 760K × 12 | `[conf:medium, src:2026-05-12]` |

**Каверзы интерпретации:**

- **Take rate 7,6%** — высокая для PayTech-aggregator'а (для сравнения: Stripe ~2,9–3,4%, Сбер ПлатиКонтр ~2,5%, ЮКасса ~2,4–3,5%) `[conf:low, src:2026-05-14]`. Это объясняется тем, что Продамус — **не чистый payment processor**, а **payment + sales-infrastructure-platform** для онлайн-школ (продающие лендинги, рекуррентные платежи, рассрочки, маркетплейс-функционал, налоговые отчёты для самозанятых/ИП). Бóльшая часть «выручки» — это не комиссия за payment, а пакеты subscription для эксперт-сегмента (inferred-from-positioning).
- **Средний чек ~3,6K ₽** соответствует typical инфо-продукт сегменту: онлайн-курсы для физлиц (3–10K ₽), мини-курсы (500–3K ₽), expert-консультации с малой группой (1,5–5K ₽).
- **Compoundirovanниый scale-up paint:** **760K сделок/мес** — это **~25K сделок в день** или **~17 сделок в минуту 24/7**. Уровень нагрузки, требующий продакшн-grade payment-infrastructure (не «WordPress + плагин Робокассы»).

## Strategy thesis от Мамуткина — multi-vertical scaling roadmap

В том же посте 2415 Мамуткин формализует **3-точечный roadmap** масштабирования Продамус как ecosystem:

> «Точка А — развиваю PayTech (системы оплат). Точка Б — SalesTech (системы продаж для селлеров и малого бизнеса). Точка С — CyberTech (Кибер-Агроном, Кибер-Бухгалтер, Кибер-Логист…)».
>
> — @fomichevkirill/2415, 2026-05-12 `[conf:medium, src:2026-05-12]`

### CyberTech thesis

Развёрнуто Мамуткиным в том же посте:

> «В обеих сферах есть узкое горлышко — люди. В агро это агроном, в логистике экспедитор. И задача с помощью технологий это узкое горлышко убрать. Например, человек без агрономического образования может выходить в поле, а центр управления будет направлять его действия. Получается такой кибер-агроном. В логистике кибер-экспедитор: обычный человек, усиленный системой, способен выполнять работу уровня специалиста с многолетним опытом».
>
> — @fomichevkirill/2415, 2026-05-12 `[conf:medium, src:2026-05-12]`

Это **human-amplifier thesis**: вместо replacement-AI (замена специалиста алгоритмом) — augmentation-AI (низко-skilled оператор + AI-управление = выходной результат уровня senior-специалиста). Семантически близко к [[evolving/content-trends/ai-agents-demand-hooks-2026|content hook'у про AI как амплификатор]] и к концепции [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026|AI-knowledge-worker climb]].

### Activeные partnership requests

Из того же поста — **6 категорий партнёрств**, которые Мамуткин активно ищет `[conf:medium, src:2026-05-12]`:

1. Партнёрства в развитии PayTech
2. Создание новой e-com платформы / маркетплейса нового типа
3. Сильный логистический партнёр по РФ
4. Инвесторы в крупные объекты недвижимости
5. Предприниматели с воображением и амбициями в команду
6. (Implicit) технологические партнёры для CyberTech-вертикалей

Это сигнал, что Продамус в Q2 2026 находится в **expansion-phase**, выходящей за пределы основного PayTech-домена.

## Сравнение с другими RU-PayTech / SaaS

| Платформа | Транзакции/мес | Оборот/год | Выручка/год | Take rate | Source |
|---|---|---|---|---|---|
| Продамус | 760K | 33 млрд ₽ | 2,5 млрд ₽ | ~7,6% | `[conf:medium, src:2026-05-12]` |
| ЮКасса (Сбер) | — | — | — | 2,4–3,5% | public pricing `[conf:high, src:2026-05-14]` |
| Robokassa | — | — | — | 2,5–4% | public pricing `[conf:high, src:2026-05-14]` |
| Tinkoff Payments | — | — | — | 2–2,8% | public pricing `[conf:high, src:2026-05-14]` |

**Insight:** позиционирование Продамус — не «дешёвый payment-processor», а **vertical-SaaS для инфо-бизнес/expert-сегмента с тарифом по принципу «всё включено»**. Это сегмент-defensible: классические payment-aggregators (ЮКасса, Robokassa) не покрывают функционал лендингов, рассрочек, рекурренции и налоговой автоматизации.

## Связь с другими страницами вики

- [[evolving-strict/competitor-metrics/ru-saas-revenue-rating-2025]] — Продамус не входил в опубликованный рейтинг (нужно проверить — самостоятельная классификация, не SaaS в чистом виде, а transaction-revenue mix).
- [[evolving/content-trends/founder-channel-sponsored-ad-formats-2026]] — гостевой профиль в рубрике «Коннект» как format продвижения PayTech-платформы среди founder-аудитории.
- [[canon/marketing-frameworks/marketing-as-product-bobkov]] — Продамус продаёт «marketing-as-product» (готовая sales-infrastructure для эксперт-сегмента).
- [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]] — CyberTech-thesis Мамуткина концептуально близка.
- [[evolving/industry-trends/ai-vertical-services-vc-uplift-2026]] — vertical-SaaS-thesis как стратегический playbook.

## Stale-check / re-verification

- **Soft re-verify через 180 дней (≤ 2026-11-14):** проверить, обновил ли Мамуткин публичные цифры (новые intervals в рубриках @fomichevkirill, @mamutkins).
- **Hard re-verify через год:** запросить через [companies.rbc.ru](https://companies.rbc.ru) официальную выручку ООО, к которому привязан Продамус (отчётность 2025–2026 годов).

## Caveats

- **Self-reported.** Цифры опубликованы в продуктовом профиле, не в отчётности. Возможны округления вверх для маркетингового эффекта.
- **Take rate 7,6% derived** — корректность derived ratio зависит от точности обеих метрик (оборота и выручки) `[conf:medium, src:2026-05-12]`. Если одна из них округлена в большую сторону, take rate смещается.
- **Не уточнён legal-entity scope.** «Продамус» — это бренд, под которым может работать несколько юр.лиц. Оборот может быть consolidated (включая partner-flow), может быть только direct.
- **CyberTech-projection.** «Точка С» — стратегический roadmap, не операционная метрика. На май 2026 нет публичных свидетельств реального запуска Кибер-Агронома или Кибер-Логиста как продуктов.

## Связанные источники

- [[sources/2026-05-14-tg-fomichevkirill-may-6-14-2026]] — первичный источник self-claim'а
