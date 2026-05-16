---
id: mkt:canon/marketing-frameworks/erp-vs-crm-smb-distinction
title: "ERP vs CRM — операциональная distinction для SMB-контента"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [framework, smb, sales, operations, crm, erp, jtbd, content-hook, ru]
confidence: medium
stale: false
created: 2026-05-06
updated: 2026-05-06
sources: [sources/2026-05-05-yt-predprinimatel-dela-vasilyev-erp-google-sheets.md]
namespace: mkt
---

# ERP vs CRM — операциональная distinction для SMB-контента

**ERP vs CRM** — операциональная рамка различения двух классов бизнес-систем, **которые большинство SMB-владельцев путают или схлопывают в одну**. Различение ценно как **diagnostic content-hook** для SMB-контента: именно здесь сидит массовый паттерн «у меня есть Bitrix24 = у меня есть система», игнорирующий весь пост-продажный fulfillment-слой.

Канонический RU-источник для формулировки — Сергей Васильев (инженер-системотехник, 5+ лет в нише Google Sheets ERP для мебельной индустрии) на «Слёте героев в Сочи», см. [[sources/2026-05-05-yt-predprinimatel-dela-vasilyev-erp-google-sheets|YouTube «Предприниматель ДЕла» #2/4]].

## Сама distinction

| Параметр | CRM | ERP |
|---|---|---|
| **Что делает** | Собирает контакты лидов, помогает менеджеру довести лид до оплачивающего клиента | Принимает оплачивающего клиента и доводит заказ до **fulfillment** (производство → доставка → установка → подписанные акты) |
| **Stage в lifecycle сделки** | Pre-sale + sale | Post-sale + delivery + post-delivery |
| **Главные пользователи** | Продавец, маркетолог, sales-менеджер, РОП | Производственный начальник, кладовщик, снабженец, сервис-инженер, бухгалтер |
| **Главные данные** | Lead, contact, deal, pipeline-stage, source, owner | Заказ, спецификация, поставщик, склад, производственный участок, статус fulfillment'а |
| **Метрика успеха** | Conversion-rate воронки, CAC, sales velocity | On-time delivery rate, доля брака, return-rate, cycle-time от оплаты до акта |
| **RU-канонические продукты** | Bitrix24, AmoCRM, RetailCRM | 1С:ERP, 1С:УПП, SAP S/4HANA, MS Dynamics, кастомные Google Sheets / Notion стеки |

## Прямая формулировка от Васильева

> «CRM-система занимается именно сбором таких контактов и затем помогает менеджеру превратить лида в реального клиента. Всё, далее должна вступать в дело ERP-система, то есть она помогает весь процесс создания мебели для этого заказчика автоматизировать, через ERP-систему можно выстроить логистику, провести все по этапам производства, ну и соответственно выяснить, что у нас по финансам, сколько мы затратили, сколько планировали затратить и так далее.» `[conf:medium, src:2026-05-05]`

И ключевой operational-anti-pattern, на который Васильев указывает:

> «Очень много сил обычно вкладывается именно в процесс продажи мебели, а затем почему-то собственники бизнесов думают, ну производство само всё сделает, но вот это очень большая ошибка.»

## Почему RU-SMB схлопывают эти системы

В русскоязычном SMB-пространстве массово встречается паттерн:

1. **«У меня есть CRM, значит у меня есть учёт»** — Bitrix24 / AmoCRM воспринимается как «система», но фактически ведёт только sales до момента «деньги пришли».
2. **«Производство = операционка, а не система»** — поскольку CRM-системы маркетируются «для всего бизнеса», а ERP-системы (1С) ассоциируются с гигантскими корпоративными внедрениями за миллионы рублей, средний SMB отказывается от ERP-слоя как «слишком сложно для нас».
3. **«Excel-файлы у нескольких сотрудников = у нас всё под контролем»** — пост-продажный процесс трекается в десятках разрозненных Excel-таблиц без единой системы, что приводит к hidden-failure-mode «заказ потерян», «спецификация не передана производству», «клиент не получил акт».

Этот паттерн — **diagnostic-маркер** founder-owner-seller сегмента ([[canon/target-audience/ru-smb-founder-owner-seller]]) и узкоспециализированных production-businesses (мебель, металлообработка, строительство, ремонт).

## Где distinction работает как content-hook

### 1. Hook для founder-owner-seller (cross-sales-content)

«Если у вас Битрикс24 и больше ничего, у вас не "система", у вас половина системы». Ставит зеркало перед фаундером, кто гордится наличием CRM, и опровергает self-perception «у меня всё под контролем». Strong для top-of-funnel awareness-контента.

### 2. Hook для контента про automation / tooling

«CRM продаёт за вас, ERP исполняет за вас. Оба нужны.» Снимает ложное противопоставление CRM ↔ ERP (как будто это альтернативы) и переводит в «комплементарный stack».

### 3. Hook для SMB-категорий с production / fulfillment слоем

В мебели, ремонте, строительстве, custom-manufacturing — где производство значимое и неавтоматизированное — ERP-vs-CRM frame **прямо применим**. В SaaS / digital products / pure-services рамка деформируется (нет production-слоя в физическом смысле), но всё равно полезна как разделение sales-stages vs post-sale-customer-success-stages.

### 4. Hook для «дешёвая ERP без 1С»

Васильев explicitly строит свою сцену вокруг этого: 1С коробочное ERP «от 500 000 ₽ + внедрение + обучение + очередь к программистам», против которого он предлагает Google Sheets + свой курс ~100 000 ₽. Это **content-pattern «доступная альтернатива тяжёлому корпоративному ПО для SMB»**, переиспользуемый в контенте для SMB-сегмента. См. [[evolving/competitor-positioning/tablichnyj-biatlon-niche-vertical-edu-product]] для конкретной реализации.

## Применимость к GRO

GRO **не является** ни CRM, ни ERP — продукт находится в категории **«ежедневная тренировка предпринимателя через AI-coaching»**, ортогональной обоим системам. Но distinction полезна как **frame-builder для контента**:

### Где GRO позиционируется

GRO closes **другой gap** — gap между «у меня есть инструменты» и «я как founder работаю эффективно с инструментами». Можно использовать в content:

> «CRM делает за вас sales, ERP делает за вас fulfillment. А кто делает за вас **founder-операционку** — приоритеты, фокус, daily plan, ретроспективу? Это GRO.»

Это позиционирование GRO как **третьего слоя** в SMB-tooling-stack: **sales (CRM) + fulfillment (ERP) + founder-личная-эффективность (GRO)**. Ставит GRO в комплементарную, а не конкурентную, позицию по отношению к existing tooling-investments ЦА.

### Где GRO **не** должен использовать distinction

- **Не позиционируйте GRO как замену CRM или ERP** — это путает аудиторию. GRO работает с **владельцем как пользователем**, а не с продавцом / производственником.
- **Не используйте distinction в B2C-контенте** — для частных лиц / freelancers / соло-фрилансеров CRM/ERP терминология чуждая, использование рамки выглядит как «надавливание корпоративной терминологией».

## Почему distinction нужна как **canonical** framework

ERP vs CRM — **стабильная** категориальная рамка, которая не дрейфует с месячной скоростью. Сама структура «системы для pre-sale» vs «системы для post-sale» — это структурный факт business-architecture, не текущий тренд. По operational-тесту [[rules]]: «если я не трону эту страницу полгода — её содержимое ещё будет истинным?» — да, будет. Поэтому `canon/marketing-frameworks/`, не `evolving/`.

Конкретные tooling-альтернативы (1С vs Sheets vs Notion-stacks) — **дрейфуют**, и именно эти конкретные сравнения уйдут в [[evolving/competitor-positioning/tablichnyj-biatlon-niche-vertical-edu-product]] и аналогичные дочерние страницы по конкретным альтернативам.

## Связанные страницы

- [[canon/marketing-frameworks/sales-crm-minimum-fieldset]] — minimum-viable CRM-конфигурация, наполняет «CRM»-сторону distinction (5 документов + 11 полей)
- [[canon/target-audience/ru-smb-founder-owner-seller]] — основная ЦА, где distinction работает как diagnostic-hook
- [[canon/target-audience/automation-eager-knowledge-worker-ru]] — adjacent-аудитория, для которой distinction может оформляться через self-serve automation tools (Zapier-аналоги, Notion-stacks)
- [[evolving/competitor-positioning/tablichnyj-biatlon-niche-vertical-edu-product]] — конкретная реализация «дешёвой ERP без 1С» через Google Sheets-стек для мебельной индустрии
- [[canon/marketing-frameworks/cost-leader-premium-quality-positioning]] — adjacent-фрейм: распространение «дешёво по цене, премиум по качеству» с продукта на инструмент управления бизнесом (Sheets-as-ERP vs 1С)
- [[canon/marketing-frameworks/marketing-as-product-bobkov]] — комплементарный взгляд на маркетинг как «продукт внутри организации», параллель к ERP/CRM как тоже «продуктам внутри»
- [[sources/2026-05-05-yt-predprinimatel-dela-vasilyev-erp-google-sheets]] — первоисточник formulation от Васильева

## Caveat

- `confidence: medium` — distinction формализована **на основе одного first-hand RU-выступления** (Васильев на Слёте героев), но **сама концепция ERP vs CRM** в индустрии устоявшаяся, не зависит от этого источника. Источник используется для конкретных RU-формулировок и operational-тезисов, не для самой distinction.
- В US/global business-discourse distinction между ERP и CRM известна десятилетиями (ERP — 1990s, CRM — 1995+). Уникальность RU-формулировки — в **операциональном пафосе** «собственники путают» и в **cost-positioning** «1С-vs-Sheets» (~500K vs ~100K), который специфичен для RU-SMB-рынка.
- При расширении формулы на не-production бизнесы (SaaS, digital agency, content) рамка должна быть переинтерпретирована: ERP-слой = customer-success / fulfillment-operations / project-management, не «производственный цех». Эта адаптация **должна быть прописана** при появлении соответствующих RU-кейсов.

## Backlinks

_7 pages link to this one._

- [[canon/target-audience/ru-smb-founder-owner-seller]]
- [[evolving/competitor-positioning/predprinimatel-dela-channel-pattern]]
- [[evolving/competitor-positioning/tablichnyj-biatlon-niche-vertical-edu-product]]
- [[evolving/content-trends/factory-tour-pro-day-event-format]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-yt-predprinimatel-dela-vasilyev-erp-google-sheets]]
