---
id: mkt:sources/2026-05-24-condense-zhazhda-biz-25-articles
title: "Condensed: zhazhda.biz base/ (25 статей) — sales-planning + KPI-мотивация"
type: source
layer: canon
theme: marketing-frameworks
tags: [framework, sales, kpi, motivation, sales-management]
confidence: medium
created: 2026-05-24
updated: 2026-05-24
original: raw/processed/articles/_condense_zhazhda_chunk2_2026-05-24.md
namespace: mkt
---

# Condensed: zhazhda.biz base/ (25 статей)

Машинно-сжатая выжимка из 25 справочных статей раздела `zhazhda.biz/base/` (сделана `wiki-condense` агентом, 2026-05-24). Каждый факт атрибутирован inline-маркером `[src: filename, date]`.

## Метаданные
- **Тип:** condensed-выжимка (web, articles)
- **Дата добавления:** 2026-05-24
- **Автор / источник:** zhazhda.biz/base/ — справочный раздел (преимущественно бухгалтерия/налоги/кадровое делопроизводство)
- **Экспертность автора:** inferred — справочный портал для МСБ; квалификация авторов не указана, но материал по sales-management/KPI содержит проверяемые operational-рамки → `confidence: medium` для содержания фреймворков
- **Sidecar note:** был — подтверждает, что 23 из 25 статей нерелевантны (бухгалтерия/налоги/кадры), извлечены только 2 (причины невыполнения плана продаж + система мотивации на основе KPI)
- **Sensitive flag:** не обнаружено

## Релевантность

Релевантно домену (извлечено в `canon/marketing-frameworks`):
- **Факторная модель причин невыполнения плана продаж** (внешние vs внутренние факторы, пессимистичное планирование, «план после анализа») — reusable sales-management методология.
- **Мотивация продающего персонала** (на достижение vs на избежание, материальная vs нематериальная, 3 правила мотивации) — reusable рамка.
- **Система мотивации на основе KPI** (4-этапная методология разработки, 3 уровня KPI-показателей, формула «оклад + премия», пример колл-центра) — reusable operational-фреймворк.

Отфильтровано (нерелевантно — только бухгалтерия/налоги/кадровое делопроизводство, out-of-domain): 23 статьи (КНД 1151111, страховые взносы ИП/КФХ, СЗВ-М, 2-НДФЛ, онлайн-касса, ОКВЭД, штатное расписание, регистрация/смена адреса ООО, субординация, патент, земельный налог и пр.). Зафиксированы в source-manifest ниже как audit trail; в слои не уносятся.

## Ключевые идеи
- План продаж составляется только **после анализа продаж**; без анализа результата «скорее всего не будет».
- Факторы невыполнения плана делятся на внешние (сезонность, география, конкуренция — не контролируются) и внутренние (ресурсы, прогнозы, персонал, мотивация — контролируются).
- Планировать стоит **пессимистичный вариант** — минимальный объём, при котором не нужно сокращать затраты, плюс план действий при падении ниже минимума.
- Мотивация двунаправленна: на достижение (позитивная атмосфера) + на избежание (контроль); рекомендуется совмещение.
- Нематериальные факторы (атмосфера, отношения с руководством) мотивируют сильнее, чем кажется; «умение мотивировать схоже с продажами».
- KPI-мотивация связывает результативность с вознаграждением напрямую, исключая формальный подход; прозрачность расчёта премии включает самомотивацию.

## Факты и цифры
- 4 этапа разработки KPI-системы: (1) анализ положения + цели в показателях; (2) бюджет на персонал + деление на эффективный/вспомогательный/руководящий; (3) разработка под отдел + фиксация в трудовых договорах; (4) контроль эффективности (кратко- и долгосрочные показатели). `[src: web_zhazhda.biz_base_sistema-motivacii-na-osnove-kpi, 2026-05-19]`
- 3 уровня KPI: 1-й (компания целиком — объём производства/продаж, рентабельность, чистая прибыль; для АУП); 2-й (производство/сбыт — склад, маркетинг, продажи; объём продаж + дебиторка); 3-й (вспомогательные — бухгалтерия, юристы, ИТ, кадры, безопасность; качество и своевременность задач). `[src: web_zhazhda.biz_base_sistema-motivacii-na-osnove-kpi, 2026-05-19]`
- Формула оплаты: фиксированная часть оклада + премиальная часть; вес показателя = его значимость. `[src: web_zhazhda.biz_base_sistema-motivacii-na-osnove-kpi, 2026-05-19]`

## Связанные страницы
- [[canon/marketing-frameworks/sales-plan-failure-factor-model]]
- [[canon/marketing-frameworks/sales-staff-motivation-achievement-avoidance]]
- [[canon/marketing-frameworks/kpi-motivation-system-4-stages]]

## Source manifest

| # | File | Title | Status |
|---|---|---|---|
| 1 | web_zhazhda.biz_base_poryadok-zapolneniya-formy-knd-1151111_8dd3dd99.md | Порядок заполнения формы КНД 1151111 | no_extractions |
| 2 | web_zhazhda.biz_base_predelnaya-baza-strahovyh-vznosov-v-2018-godu_ffb1d7b9.md | Предельная база страховых взносов в 2018 году | no_extractions |
| 3 | web_zhazhda.biz_base_prichiny-nevypolneniya-plana-prodazh_45b3cf66.md | Причины невыполнения плана продаж | extracted (marketing-frameworks) |
| 4 | web_zhazhda.biz_base_proverki-ip-posle-zakrytiya_25ed14e5.md | Проверки, которые ждут ИП после закрытия | no_extractions |
| 5 | web_zhazhda.biz_base_raschet-indeksacii-zarabotnoj-platy_4cc5d7ef.md | Расчет индексации заработной платы | no_extractions |
| 6 | web_zhazhda.biz_base_registratsiya-ooo-v-drugom-regione-ili-gorode_a1bf3603.md | Регистрация ООО в другом регионе или городе | no_extractions |
| 7 | web_zhazhda.biz_base_shtrafy-gosudarstvennoj-inspekcii-truda_23c1091b.md | Штрафы Государственной инспекции труда | no_extractions |
| 8 | web_zhazhda.biz_base_sistema-motivacii-na-osnove-kpi_c55f33a2.md | Система мотивации на основе KPI | extracted (marketing-frameworks) |
| 9 | web_zhazhda.biz_base_sluzhebnoe-zadanie-na-komandirovku_d8310073.md | Служебное задание на командировку | no_extractions |
| 10 | web_zhazhda.biz_base_smena-yuridicheskogo-adresa-ooo_57a10ff9.md | Смена юридического адреса ООО в 2017 | no_extractions |
| 11 | web_zhazhda.biz_base_sotrudnik-propal-bez-vesti_fbad20bb.md | Работник пропал: действия работодателя | no_extractions |
| 12 | web_zhazhda.biz_base_srok-sdachi-otcheta-2-ndfl_929d4f01.md | Срок сдачи отчета 2-НДФЛ | no_extractions |
| 13 | web_zhazhda.biz_base_sroki-sdachi-szv-m-v-2018-godu_a849dcd5.md | Сроки сдачи СЗВ-М в 2018 году | no_extractions |
| 14 | web_zhazhda.biz_base_strahovye-vznosy-ip-na-envd_c54f074d.md | Страховые взносы ИП на ЕНВД | no_extractions |
| 15 | web_zhazhda.biz_base_strahovye-vznosy-ip-s-dohodom-svyshe-300000-rub_58cde921.md | Страховые взносы ИП при доходе свыше 300000 рублей | no_extractions |
| 16 | web_zhazhda.biz_base_strahovye-vznosy-ip_3a6a3ceb.md | Страховые взносы ИП в ПФР в 2017 | no_extractions |
| 17 | web_zhazhda.biz_base_strahovye-vznosy-kfh_4e222499.md | Страховые взносы КФХ в 2018 году | no_extractions |
| 18 | web_zhazhda.biz_base_subordinaciya-na-rabote_4021e8dc.md | Субординация на работе | no_extractions |
| 19 | web_zhazhda.biz_base_trebovaniya-k-cheku-onlajn-kassy_b8f9d6d0.md | Требования к чеку онлайн-кассы | no_extractions |
| 20 | web_zhazhda.biz_base_uchet-ip-pri-patente_056d2c99.md | Как вести учет ИП на патенте | no_extractions |
| 21 | web_zhazhda.biz_base_uchet-vozvrata-tovara_8a823578.md | Учет возврата товара | no_extractions |
| 22 | web_zhazhda.biz_base_vnesenie-izmenenij-kody-okved_14203f9c.md | Внесение изменений в коды ОКВЭД в 2017 году | no_extractions |
| 23 | web_zhazhda.biz_base_vnesenie-izmenenij-v-shtatnoe-raspisanie_6266ff97.md | Внесение изменений в штатное расписание | no_extractions |
| 24 | web_zhazhda.biz_base_vyplata-zarplaty-v-ooo_a47c042f.md | Выплата зарплаты в ООО | no_extractions |
| 25 | web_zhazhda.biz_base_zemelnyj-nalog-ip-usn_2e16a3e2.md | Земельный налог ИП на УСН | no_extractions |
</content>
