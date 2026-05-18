---
id: mkt:canon/marketing-frameworks/cpa-calculator-pre-launch-roi
title: "Pre-launch ROI калькулятор: считай выплату за лид до запуска кампании"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [framework, performance, roi, paid-ads, calculation]
confidence: medium
stale: false
created: 2026-04-14
updated: 2026-05-19
sources: [sources/2026-04-14-tg-petrochenkow-mar-apr-2026.md, sources/2026-05-19-pressfeed-chatbot-roi-framework-evseeva.md]
namespace: mkt
---

# Pre-launch ROI калькулятор

**Тезис.** В России есть массовое поверие, что «реклама — это лотерея»: запустим, посмотрим, как пойдёт. Из этого тезиса вытекает порядок действий: сначала собираем 10 000 ключевых слов, потом пишем тексты, ставим ставку «от балды» и ждём чуда.

Профессиональные арбитражники, у которых медиа-бюджет = их деньги, делают **наоборот**: сначала считают конечный результат, потом запускают **только по выгодным комбинациям**. Для них реклама — это покер, а не лотерея: играют только по потенциально интересным комбинациям.

## Что нужно посчитать до запуска

### 1. Примерные показатели рекламы
- **CTR** — кликабельность, исходя из площадки и креативов
- **CPM** — стоимость 1000 показов
- **CPC** — стоимость клика (= CPM / CTR / 1000)
- **Желаемое число кликов** — какой объём трафика нужен для теста гипотезы

### 2. Показатели воронки сайта
- **Коэффициент конверсии** (визит → лид)
- **Коэффициент качества заявки** (apriv — % подтверждённых лидов после квалификации)
- **Выплата за лид** (см. ниже — ключевой и часто неправильно считаемый показатель)

### 3. Формула выплаты за лид

> **Выплата за лид = Маржа × CR (лид → покупка)**

**Пример Petrochenkov:** маржа на iPhone 5000 ₽, из 10 заказов 8 выкупаются (CR покупки = 0,8). Тогда выплата за лид = 5000 × 0,8 = **4000 ₽**.

Эта величина — не доход, не ARPU, не средний чек. Это «сколько я могу позволить себе платить за лид, чтобы оставаться в плюсе». Если CPL > этой величины — кампания убыточна, **независимо от того, как красивы отчёты**.

## Готовый калькулятор

Petrochenkov ссылается на простой публичный инструмент: **cpa.rip/roi/** (упомянут в посте 1199, 2026-03-11).

## Алгоритм работы с калькулятором

1. Заливаешь кампании с **тестовым бюджетом 3 000 – 15 000 ₽**.
2. Снимаешь реальные показатели рекламы (CTR, CPC, реальную конверсию сайта).
3. Заносишь данные в файл вместе с показателями воронки (apriv, CR покупки, маржа).
4. Получаешь **готовый медиаплан** с прогнозом, сколько лидов / клиентов / выручки даст каждый рубль трафика.

## Когда применять

- Перед запуском **любой** платной кампании, даже если бюджет «всего» 50 000 ₽.
- При смене канала / креатива / посадочной — пересчитывать заново, не использовать прошлые цифры.
- При презентации бюджета руководству — это превращает «рекламу-лотерею» в управляемый расчёт.
- **Для стартапов и MVP** — этот же расчёт выявляет, есть ли вообще unit-экономика, прежде чем тратить деньги.

## Ограничения

- Тестовый бюджет 3-15 тыс ₽ даёт высокую погрешность оценки CR. Полагаться на цифры, снятые с 200 кликов, — самообман. Для надёжной оценки нужно ≥1000 кликов на гипотезу.
- Маржа должна учитывать **операционные расходы**, не только себестоимость товара. Иначе «выплата за лид» завышена и при масштабировании кампания убыточна.
- CR покупки нужно считать **на той же ЦА**, на которую рекламируешься. Среднее по компании может вводить в заблуждение, если кампания таргетируется на холодную аудиторию, а CR компании посчитан на тёплой.
- Не учитывает LTV. Для подписочных продуктов и продуктов с repeat purchase ROI на первой покупке может быть отрицательным, а кампания при этом — выгодной (см. ниже).

## LTV-расширение

Для подписочных продуктов (как GRO) формулу нужно расширить:

> **Выплата за лид = (Маржа × CR покупки) + (LTV × CR retention) − Operational cost**

Если первый платёж даёт минус, но средний клиент остаётся 6 месяцев, реальная выплата за лид считается на горизонте 6 месяцев. Это та же логика, по которой работает Front-End стратегия [[canon/marketing-frameworks/marketing-audit-protocol]] (пост 1217 — рекомендация Petrochenkov на 2026: создавать FE-продукты по 10-20% цены основного, чтобы LTV закрыл CAC).

## Cross-domain parallel: Pre-launch ROI и для automation

Тот же принцип «сначала считай, потом запускай» работает не только в paid-ads, но и во **внутренней автоматизации**. Юлия Евсеева в колонке Pressfeed (2026-05-19) — см. [[canon/marketing-frameworks/chatbot-roi-4-economic-effects]] и [[sources/2026-05-19-pressfeed-chatbot-roi-framework-evseeva]] — даёт параллельную рамку для решения о внедрении чат-бота: 4 узла экономического эффекта (восстановление лидов, LTV, FTE-экономия, off-hours) + ROI-гейт. Принцип идентичен Петроченкову: «главная ошибка — внедрять, а потом пытаться оценить результат. Правильная логика обратная: сначала расчёт, потом запуск.» Если в формулу нельзя подставить хотя бы половину показателей — внедрение преждевременно.

Это формирует **canonical RU-narrative о rational marketing/automation 2026**:

| Контекст | Pre-launch ROI рамка |
|---|---|
| Paid-ads (внешний траффик) | Петроченков: CPL ≤ Маржа × CR покупки |
| Чат-бот / automation (внутренние процессы) | Евсеева: ROI = (Доп. прибыль + Экономия − Стоимость проекта) / Стоимость проекта |
| Любая automation в SMB | Григорьев ([[canon/marketing-frameworks/ai-smb-pilot-three-traps]]): без цели, без MVP, без buy-in — Klarna $15M вам ждёт |

## Связь с другими фреймворками

- [[canon/marketing-frameworks/marketing-audit-protocol]] — диагностика того, понимает ли команда unit-экономику.
- [[canon/marketing-frameworks/refused-customer-interview]] — улучшает CR покупки через понимание барьеров.
- [[canon/marketing-frameworks/qualitative-adjectives-ad-copy]] — улучшает CTR (и тем самым CPC) на этапе креатива.
- [[canon/marketing-frameworks/chatbot-roi-4-economic-effects]] — pre-launch ROI для automation (Евсеева).
- [[canon/marketing-frameworks/ai-smb-pilot-three-traps]] — anti-pattern AI-внедрения (Григорьев).
- [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] — бенчмарки CPV/CPM по каналам РФ.

## См. также

- [[sources/2026-04-14-tg-petrochenkow-mar-apr-2026]] — первоисточник (пост 1199, 2026-03-11)
- [[sources/2026-05-19-pressfeed-chatbot-roi-framework-evseeva]] — параллельная рамка для automation

## Backlinks

_13 pages link to this one._

- [[canon/marketing-frameworks/andromeda-creative-framework-2026]]
- [[canon/marketing-frameworks/business-metrics-for-owners]]
- [[canon/marketing-frameworks/hyperseg-funnel-replication]]
- [[canon/marketing-frameworks/marketer-hiring-questions]]
- [[canon/marketing-frameworks/marketer-task-typing-fomichev]]
- [[canon/marketing-frameworks/mvp-definition-gorny]]
- [[canon/marketing-frameworks/petscom-unit-economics-failure]]
- [[canon/marketing-frameworks/qualitative-adjectives-ad-copy]]
- [[canon/marketing-frameworks/sales-crm-minimum-fieldset]]
- [[evolving-strict/market-data/deloitte-marketing-trends-2026]]
- [[evolving/content-trends/price-anchor-demping-content-format]]
- [[index]]
- [[sources/2026-04-14-tg-petrochenkow-mar-apr-2026]]
