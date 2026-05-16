---
id: mkt:canon/marketing-frameworks/sales-crm-minimum-fieldset
title: "Минимальный CRM для sales: 5 документов + 11 полей"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [sales, crm, operations, tooling, b2b]
confidence: low
stale: false
created: 2026-05-05
updated: 2026-05-05
sources:
  - sources/2026-05-05-e-xecutive-ru-condensed.md
  - sources/2026-05-05-exec-upravlenie-prodazhami.md
namespace: mkt
---

# Минимальный CRM для sales: 5 документов + 11 полей

Минимально жизнеспособная конфигурация sales-tooling: 5 операционных документов и 11 полей в клиентской БД. Намеренно skeletal — компания может расширять под свои use-cases, но без этих базовых элементов sales-команда не управляется. Применимо к любому B2B-каналу с активными sales (где есть менеджер, ведущий клиента).

## 5 операционных документов на sales-rep

| # | Документ | Что содержит | Частота update |
|---|---|---|---|
| 1 | **Профиль клиента** | Company info, контакты ЛПР, decision-process, существующие потребности, почему сейчас, размер сделки | По мере обновления |
| 2 | **Рабочий лист менеджера** | Текущие задачи, follow-ups, приоритеты на сегодня | Ежедневно |
| 3 | **Отчёт за день** | Что сделано (звонки, встречи, движение по deals), что планируется на завтра | Ежедневно |
| 4 | **Отчёт за месяц** | Pipeline, closed deals, conversions, summary by stage | Ежемесячно |
| 5 | **Структурированная клиентская БД** | Все клиенты (включая потенциальных) с 11 полями (ниже) + история взаимодействий | Постоянно |

И **план продаж на месяц** — формально 6-й артефакт, но он входит в управленческий цикл (sales manager + rep ставят план), не в инструменты rep'а.

## 11 минимальных полей клиентской БД

| # | Поле | Описание |
|---|---|---|
| 1 | **Статус** | Текущая стадия pipeline (Lead / MQL / SQL / Opportunity / Closed Won / Closed Lost / Dormant) |
| 2 | **Название** | Название компании (или ФИО для физлица) |
| 3 | **Источник** | Где появился лид (paid search, referral, конференция, cold outreach, ...) |
| 4 | **Ведущий менеджер** | Кто из sales-команды ведёт |
| 5 | **Регион** | Географический market |
| 6 | **Контакт (ФИО, должность)** | Главный контакт; для крупных deals — multiple |
| 7 | **Категория** | Сегмент клиента (size, vertical, type) |
| 8 | **Специализация** | Чем клиент занимается (для context при общении) |
| 9 | **Ценовая категория** | Tier по price (наш типичный размер сделки для этого клиента) |
| 10 | **Особые условия** | Скидки, отсрочки, нестандартные термы (например, контрактный SLA) |
| 11 | **Примечание** | Свободный текст для rep'а |

## Почему именно 11 (не 5 и не 30)

**5 полей** недостаточно: нельзя сегментировать pipeline (нужен Source, Регион, Категория для аналитики).

**30 полей** избыточно: rep тратит время на заполнение вместо общения с клиентом, поля не заполняются регулярно, БД становится «грязной» и теряет аналитическую ценность.

11 полей — sweet spot: хватает для базовой сегментации pipeline и reporting, мало настолько что rep'ы реально заполняют.

## Что критично, но **не** в минимальном наборе

Расширения, которые добавляются по мере зрелости sales-org:
- **Activity log** (звонки, встречи, emails) — критично для pipeline transparency, но автоматизируется через интеграцию с email/телефонией, не ручным вводом
- **Lead score** — вычисляемое поле (на основе activity и demographic), не вводится rep'ом
- **Forecast confidence** — для каждой opportunity, %вероятность закрытия
- **Custom fields под индустрию** — например, для SaaS добавляется ARR / contract length / renewal date

## Применимость к GRO

- **При запуске sales-функции с нуля:** начать с 11 полей, не строить «идеальный CRM с 50 полями». Расширять только когда обнаруживается аналитический gap.
- **При migration в новый CRM:** 11 минимальных полей мигрируются обязательно, остальное — на основе usage analytics в старой системе (что реально использовалось).
- **При найме sales-rep'а:** обучение минимальному набору + правилам обновления (отчёт за день обязателен) — в первый день.
- **Anti-pattern:** «давайте добавим поле X, всем rep'ам надо обновлять» — без проверки что новое поле даёт аналитическую ценность. Растёт data debt и uncompleted записи.

## Связанные страницы

- [[canon/marketing-frameworks/management-pyramid-sales]] — иерархическая модель управления, в рамках которой работает CRM
- [[canon/marketing-frameworks/defector-loyalty-crm-analysis]] — расширение на retention / churn analysis
- [[canon/marketing-frameworks/cpa-calculator-pre-launch-roi]] — связка CRM с unit-econ при оценке кампаний
- [[canon/marketing-frameworks/marketing-audit-protocol]] — место CRM-аудита в общем audit-протоколе
- [[canon/marketing-frameworks/business-metrics-for-owners]] — какие метрики из CRM поднимаются на owner-level

## Caveat

Skeletal-набор устойчив с начала 2000-х. Конкретный source 2001 без независимой верификации использования. Для современных Sales-Tech (HubSpot, Salesforce, Pipedrive, AmoCRM, Bitrix24) эти 11 полей входят в базовую конфигурацию из коробки. `conf:low` для атрибуции, сам набор очевидно устоявшийся.

## Backlinks

_7 pages link to this one._

- [[canon/marketing-frameworks/erp-vs-crm-smb-distinction]]
- [[canon/marketing-frameworks/krylov-sales-imitator-3-markers]]
- [[canon/marketing-frameworks/management-pyramid-sales]]
- [[canon/marketing-frameworks/sales-100-formula-shevelev]]
- [[canon/marketing-frameworks/sales-quality-vs-quantity-vyakuba-kpi]]
- [[index]]
- [[sources/2026-05-05-e-xecutive-ru-condensed]]
