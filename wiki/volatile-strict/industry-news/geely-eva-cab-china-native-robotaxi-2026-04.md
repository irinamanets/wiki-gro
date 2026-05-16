---
id: mkt:volatile-strict/industry-news/geely-eva-cab-china-native-robotaxi-2026-04
title: "Geely Eva Cab — первый native robotaxi Китая (Beijing Auto Show, 24 апр 2026)"
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [geely, china, robotaxi, autonomous-vehicles, ai, beijing-auto-show, native-av]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-techsparks-apr-may-2026.md]
namespace: mkt
---

# Geely Eva Cab — China-native robotaxi

## Базовый факт

- **24 апреля 2026:** Geely на **Beijing Auto Show 2026** представила **Eva Cab** — позиционируется как **первый в Китае native robotaxi**, спроектированный **с нуля под автономные перевозки** `[conf:high, src:2026-04-24]`
- **Native-design маркер:** руль и привычные органы управления, рассчитанные на «белкового водителя», **отсутствуют** `[conf:high, src:2026-04-24]`
- **Mass production / коммерческая эксплуатация:** запланированы на **2027** `[conf:high, src:2026-04-24]`

Источник: carnewschina.com. Зафиксировано в [[sources/2026-05-05-tg-techsparks-apr-may-2026|@techsparks]] пост 5571.

## Технические характеристики (раскрытые)

«Не обвес для придания автономности обычным существующим моделям, а с нуля спроектированная под автономные перевозки машина». Spec-карточка нетипична для классического авто — начинается **не с мощности двигателя**, а с AI-стека `[conf:high, src:2026-04-24]`:

| Компонент | Значение | Source |
|---|---|---|
| AI-модель | World Action Model (WAM), Step 3.5 | `[conf:high, src:2026-04-24]` |
| Параметры модели | **196 млрд параметров** | `[conf:high, src:2026-04-24]` |
| Аппаратная платформа | **H9** | `[conf:high, src:2026-04-24]` |
| Производительность | **1 400 TOPS** | `[conf:high, src:2026-04-24]` |
| Mass production target | **2027** | `[conf:high, src:2026-04-24]` |

## Стратегическая значимость

### 1. Конвенция категории — native-AV без атавизмов

«Без руля и педалей» — это **намеренный design-сигнал**, а не упущение. Tesla Cybercab (anonsовалось ранее, в plan capex 2026 — см. [[volatile-strict/competitor-news/tesla-capex-25b-2026|Tesla $25B capex]]) идёт по тому же дизайн-вектору. Это **emerging-конвенция категории**: **AV-машина высшего уровня автономии — не «обычный автомобиль с автопилотом»**, а new-form-factor транспорт без legacy-controls.

Это конвергенция, которой раньше не было: **Geely (Китай) и Tesla (США) синхронно выпускают native-AV без legacy-controls в один и тот же квартал**. Это сильный сигнал того, что категория «full self-driving with steering wheel» переходит в **разряд устаревших** — даже если регуляторы пока требуют законодательно педаль/руль.

### 2. Подтверждение [[evolving/industry-trends/china-ai-manufacturing-momentum-2026|материального слоя AI Китая]]

Geely Eva Cab — **4-й сигнал материального слоя AI в Китае** (после AgiBot 10K humanoid units, BCI Госплана 2030, Honor Lightning humanoid марафон 2026-04-19):

| # | Сигнал | Дата | Тип |
|---|---|---|---|
| 1 | AgiBot 10K humanoid units shipped | 2026-03 | manufacturing |
| 2 | BCI Госплан Китая (7 министерств) | 2026-03 | regulatory/strategic |
| 3 | Honor Lightning marathon (50:26 vs human 57:20) | 2026-04-19 | capability ramp-up |
| 4 | **Geely Eva Cab native robotaxi (196B params, 1400 TOPS)** | **2026-04-24** | **production-grade AV** |

Pattern: **Китай систематически строит physical-layer AI** (роботы / BCI / AV), параллельно к software-фронт-доминированию США (OpenAI / Anthropic / Microsoft).

### 3. Спецификация AI как product-marketing-первое

Раскрытие **196B параметров и 1400 TOPS** в product-marketing-материалах автомобиля — **новая конвенция AV-маркетинга**. Раньше клиент принимал решение по mph/мили-на-литре, теперь — по характеристикам vision/reasoning-стека. Это **прямой product-marketing pattern для AI-driven hardware**: AI как **первая spec в spec-листе**, а не **последняя**.

Сигнал для marketing-memory: на vertical AI-products (industrial / autonomous / consumer) **transparent disclosure AI-стека становится нормой**. Это перекликается с тезисом [[evolving/industry-trends/industrial-ai-measurable-roi-2026|industrial AI raised the bar for ROI-disclosure]] — там бизнес раскрывает экономику, здесь — технические параметры.

## Что не известно из поста (gaps)

- **Compute envelope** vs Tesla FSD-стека (HW4? HW5?)
- **Reference cities** для пилотов
- **Retail-цена** (если Geely планирует consumer-sales или only-fleet)
- **Конкуренты в Китае:** XPeng / Pony.ai / Baidu Apollo native-AV сравнения

Эти gaps можно закрыть в Q3-Q4 2026, когда Geely выпустит pre-production tease.

## Импликации для marketing-memory GRO

GRO — self-management product, не AV-relevant. Но переносимые сигналы:

1. **Native-design narrative.** «Не обвес поверх старого, а с нуля под новую парадигму» — готовая риторическая рамка для content GRO о том, как **вертикальные AI-продукты дизайнятся под новую парадигму, а не старую** (классический пример: Atomic Habits как старая parametрizация vs GRO как AI-native scaffold).

2. **Cross-Pacific synchronicity hook.** Tesla Cybercab + Geely Eva Cab + Uber $10B fleet — **три параллельных AV-сигнала за две недели апреля 2026**. Подходит для weekly-digest content в [[evolving/content-trends/short-form-video-algo-retention-2026|short-form video формате]] для сегмента «карьеристы».

3. **AI-spec-as-marketing template.** Geely product-marketing раскрывает 196B / 1400 TOPS в первой строке. Если GRO когда-нибудь будет публиковать AI-обогащённые changelog'и — этот template (AI capabilities как первая spec, до feature-listа) — применим.

## Связанные страницы

- [[evolving/industry-trends/china-ai-manufacturing-momentum-2026]] — 4-й сигнал материального слоя AI в Китае
- [[volatile-strict/competitor-news/tesla-capex-25b-2026]] — параллельный Cybercab native-AV в US
- [[volatile-strict/competitor-news/uber-10b-robotaxi-investment-2026-04]] — параллельная robotaxi-инвестиция Uber
- [[evolving/industry-trends/autonomous-delivery-vehicle-classification-2026]] — regulatory-arbitrage рамка для AV
- [[volatile-strict/industry-news/honor-lightning-humanoid-marathon-2026-04]] — 3-й китайский сигнал той же недели
- [[sources/2026-05-05-tg-techsparks-apr-may-2026]] — источник (пост 5571)

## Backlinks

_7 pages link to this one._

- [[evolving/industry-trends/china-ai-manufacturing-momentum-2026]]
- [[index]]
- [[sources/2026-05-05-tg-techsparks-apr-may-2026]]
- [[volatile-strict/competitor-news/tesla-capex-25b-2026]]
- [[volatile-strict/competitor-news/uber-10b-robotaxi-investment-2026-04]]
- [[volatile-strict/competitor-news/uber-autonomous-strategy-pivot-2026]]
- [[volatile-strict/industry-news/honor-lightning-humanoid-marathon-2026-04]]
