---
id: mkt:canon/marketing-frameworks/profit-share-service-revenue-smb
title: "Profit-share на service revenue для удержания переманенного персонала (SMB-rental)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [smb, hr, retention, partnership, fleet-rental, comp-design, founder-playbook]
confidence: medium
stale: false
created: 2026-05-06
updated: 2026-05-06
sources: [sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet.md]
namespace: mkt
---

# Profit-share на service revenue для удержания переманенного персонала

Operational HR-pattern для **fleet-rental SMB**, в котором переманенные технические специалисты получают **piece-rate ZP** по основному business core (аренда), но **отдельный profit-share по «вторичному» revenue stream (сервис сторонних)**. Pattern впервые зафиксирован в финальном выпуске электробайк-серии Муратаева (#5/5, [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]]).

## Структура (на примере «Дай газу» / Муратаев)

| Revenue stream | Compensation |
|---|---|
| **Аренда company-owned байков** (core revenue, B2C/B2B) | ZP/смена 4 000 ₽ piece-rate per механик; не зависит от выручки этой смены |
| **Сервис сторонних байков** (новый стрим, не было в month-0) | **33% / 33% / 33%** (Ахмат / Андрей / компания) |

Founder (Кирилл): «деньги за работу пилится между компанией и между сервисами. Это нормальная история во всех сервисах. И то же самое во всех сверх услуги, как и маникюры, так далее. Все работают вздельно, получают 40 или 50 процентов».

## Почему это работает structurally

### Mitigates fold-failure mode конкурента

Андрей (новый механик) в кадре explains, **почему ушёл с предыдущего места**:

> «По факту была обговоренность, что вот 4 тысячи фикса, все, что по ремонтам сверху, оно идет сверху. В итоге произошло так, что компании стало невыгодно мне платить. И они сделали как? 4 тысячи у меня есть фиксы, и все, что по сервисам в день, если оно перебивает эти 4 тысячи, то мне платят вверх. То есть, допустим, я целый день очень сильно уматываюсь, а у меня выходит там 4 200, потому что на 200 рублей больше вышло сервиса».

Это classic **fold-into-fixed antipattern**: компания, увидев «sweet spot» где variable-comp пересекает fixed-comp, schiefстеллt formulу так, чтобы variable работал как **floor**, а не как **upside**. Для механика это значит: **work harder = same money**, мотивация исчезает.

**Profit-share pattern избегает fold'а** структурно:
- ZP/смена = **piece-rate per shift, not per revenue per shift**. Не зависит от выручки этой смены. Механик получает 4 000 ₽ независимо от того, было обслужено 1 байк или 5.
- Profit-share по сервису = **отдельный pool**, который **не уменьшается** при росте core-выручки.
- Compagnia не имеет механизма «fold» — она физически не может перевести profit-share в фикс, потому что это разные revenue streams.

### Фиксирует «новые-vs-старые-деньги» mental model для founder'а

Founder explicitly explains в кадре: «4 тысячи рублей человеку выплачивается только тогда, когда он там выполняет какую-то работу, связанную с нашими байками, в которой мы получаем деньги только с аренды. С новых денег, которые заходят в компанию».

Это **clear separation between asset-revenue (аренда core) и service-revenue (cross-customer ремонт)**. Founder сохраняет ZP-cost predictable (фиксирован per-shift), а profit-share становится **alignment-инструмент** на growth secondary stream.

## Когда применять

**Условия применимости:**

1. **Multi-revenue-stream SMB** — есть основной (как rental) + secondary (как сервис, retail, partнёрство), и secondary можно attribute к специфическому персоналу.
2. **Skilled labor** — техническая компетенция, которую трудно нанять с рынка (electromobility specialist, hairstylist, IT-специалист). Для commodity labor (cashier, packer) profit-share не нужен.
3. **Переманенный персонал** — когда конкретный персонал имеет alternative path (свой бизнес, другой работодатель). Profit-share = retention-механизм против реверс-переманивания.
4. **Visible secondary-stream growth potential** — если secondary < 5% от main, profit-share = noise. В кейсе Муратаева секондарный сервис 4 800 / 581 500 = 0,8% в month-1, но **trajectory** — 25 520 / 916 000 = 2,8% в month-3 (×3,5 рост за 2 мес). Founder фиксирует структуру **до того, как стрим вырастет**, чтобы при scale alignment был уже встроен.

**Условия НЕприменимости:**

- Single-revenue-stream бизнес (только аренда без сервиса) — нечего share'ить.
- Founder hates partial ownership of revenue → нет structural shift.
- Налоговая структура не позволяет (если patent-based как у Муратаева — вне dispute, всё в кэше).

## Соотношения

Founder upper-cap: «у сервисменов это условно 40 или 50 процентов» — то есть **40-50% от service-revenue идёт мастеру**. В кейсе Муратаева пошёл 33%/33% × 2 мастера = **66% к мастерам, 33% к компании**.

| % мастеру | Применимо когда | Source |
|---|---|---|
| 40-50% (industry-standard, по словам founder'а) | Маникюр, parikmaher-сервисы, body-care, hair-salon | folk wisdom (founder claims, not validated) |
| 33% × 2 мастера = 66% (split-share) | Multiple-mechanic shop с парным staffing | [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]] |
| 25-30% | Mass-volume, low-skill | hypothesis, не зафиксировано |

## Cross-применимость к не-rental SMB

Pattern обобщается за пределы fleet-rental:

- **Гимнастический / спортивный клуб + доп-услуги (массаж, training)**: ZP/смена для тренеров на базовых группах, profit-share на personal-training (см. parallel в [[evolving-strict/market-data/ru-fitness-club-unit-economics-2026]] — фитнес-клуб Ильи использует **другую модель** «брожение через breakage», но **тот же принцип отделения core-cohort revenue от individual revenue**)
- **Маркетплейс-агентство + custom-projects**: ZP за стандартные операции, profit-share за custom-projects per менеджеру
- **Service-software (consultant + billable hours)**: salary за base + bonus за billable hours overflow

## Связанные страницы

- [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]] — anchor-источник pattern'а
- [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]] — где Сервис-revenue scale'ится до 25 520 ₽/мес-3 (vs 4 800 ₽/мес-1) — confirmation that secondary-stream грeve grows
- [[evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026]] — числовая основа: ФОТ 158 000 → 208 000 (mo1→mo3), service-revenue 4 800 → 25 520
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] — operational philosophy founder'а, под которую этот pattern fits (piece-rate vs fixed = anti-overspend на launch)
- [[canon/target-audience/ru-smb-founder-owner-seller]] — ICP-сегмент, для которого этот pattern actionable
- [[canon/marketing-frameworks/breakage-business-model-fitness]] — cross-vertical alternative (фитнес-Ilya) для multi-revenue-stream SMB
- [[canon/marketing-frameworks/three-partner-majority-rule-smb]] — соседняя governance-page, прихваченная в том же эпизоде

## Backlinks

_6 pages link to this one._

- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]]
- [[canon/marketing-frameworks/three-partner-majority-rule-smb]]
- [[evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026]]
- [[evolving/content-trends/biznes-s-nulya-founder-diy-format-2026]]
- [[index]]
- [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]]
