---
id: mkt:volatile-strict/competitor-news/qcomment-fake-review-market-ru-2026
title: "QComment — RU биржа фейковых отзывов (re-emerged 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [ru-startup, fake-reviews, reputation, marketplaces, otzovik, yandex-market, content-trust]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-startupoftheday-may-5-13-2026.md]
namespace: mkt
---

# QComment — RU биржа фейковых отзывов (re-emerged 2026)

Российская биржа фейковых отзывов: заказчик описывает где, что и как писать, исполнители публикуют отзывы о товарах, которыми никогда не пользовались. Освещена Александром Горным в #субботнийповтор посте 5059 (2026-05-09) — оригинальный пост 2022 года, апдейт о текущем статусе — см. [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]].

## Базовые факты

- **Название:** QComment `[conf:high, src:2026-05-09]`
- **Сегмент:** биржа фейковых отзывов (RU + adjacent) `[conf:high, src:2026-05-09]`
- **Опубликовано «работ» (отзывов):** **66 миллионов** `[conf:medium, src:2026-05-09]` (по данным сайта QComment, по словам Горного — verified самим стартапом)
- **Площадки:** Отзовик, Яндекс.Маркет, YouTube, безымянные локальные форумы `[conf:high, src:2026-05-09]`
- **Цены за отзыв:** от **3₽** (75 символов без регистрации) до **50₽** (сложные случаи) `[conf:high, src:2026-05-09]`
- **Изначальный домен:** .ru (2022 год, время первой публикации Горного) `[conf:high, src:2026-05-09]`
- **Текущий домен:** .com `[conf:high, src:2026-05-09]`
- **ООО:** продолжает сдавать отчётность `[conf:medium, src:2026-05-09]`
- **Способ выплат:** теперь только через крипту (по жалобам исполнителей) `[conf:low, src:2026-05-09]`
- **Прим. от Горного:** «якобы возникли сложности с государством» `[conf:low, src:2026-05-09]`

## Ограничения сервиса (по словам Горного)

1. **Только positive on self:** заказывать можно ТОЛЬКО комментарии на самого себя. Обливать грязью конкурентов **запрещено**. Возможно — risk попадания под уголовку за клевету.
2. **Не работает с Tripadvisor:** скорее всего, лучшая модерация (по словам самой QComment).

## Сигнал-уровень

**Несмотря на #субботнийповтор формат**, эта запись — **активный сигнал** в 2026:

- Платформа **жива** (домен переехал, ООО сдаёт отчётность)
- Способ оплаты ушёл в **тень** (только крипта для исполнителей)
- Прием платежей с заказчиков **открытыми картами**
- **Размер рынка:** 66M «работ» = заметная часть RU-отзывного объёма

**Контекст:** это **classic shadow-economy pattern** для RU-fake-review-сервиса. Не уникально для России — аналогичные сервисы в US (e.g. AppSally) тоже периодически уходят в .com + crypto-only.

## Что это значит для GRO

GRO — фитнес-приложение, **не отзовик**. Но **отзывы — основной маркетинговый инструмент product-page на App Store / Play / RuStore** (см. [[evolving-strict/product-metrics|product-metrics]]).

### 1. Landscape «как формируется средний рейтинг RU-app»

Существование 66M «работ» = заметная часть отзывного объёма Рунета. Это означает:

- **Средний рейтинг RU-апп не отражает реальное user-satisfaction** в чистом виде
- **Defensive стратегия:** GRO должна **активно собирать честные отзывы** (review-prompts в продукте, NPS-кампании), а не полагаться на органику. См. [[canon/marketing-frameworks/employer-branding-review-funnel]] — паттерн «выстраиваем funnel честных отзывов» (transferable от employer-branding).

### 2. Defensive PR-сценарий

Если GRO попадает в коммерчески неудобную ситуацию с конкурентом, который **через QComment-подобный сервис** заполняет product-page или sentiment-monitoring отрицательными отзывами — нужен ready PR-playbook (см. [[canon/marketing-frameworks/crisis-pr-principles]]).

**Signal: QComment не разрешает «лить грязь на конкурентов»** — uncertainty уровня, действительно ли competitors могут так атаковать GRO. Но рынок shadow-сервисов есть, и не QComment — единственный.

### 3. AI-content-creation как «новая фейк-фабрика»

В 2026 значение QComment **подрывает AI-content-generation**: создать 66M уникальных текстовых отзывов **дешевле через LLM**, чем нанимать людей по 3-50₽ за штуку. Это **structural disruption** для всего fake-review-сегмента. [conf:low, src:2026-05-14]

**Implication для GRO:** мониторинг **AI-сгенерированных отзывов** на product-pages должен включать **detection-pattern** (homogeneity, lack of specific product-feature mentions, generic phrasing). См. [[canon/marketing-frameworks/ai-text-markers-checklist]] — paralel pattern для текста AI-generated.

## TTL и retest

`volatile-strict` — через **90 дней** (2026-08-14) проверить:
- Жив ли QComment.com?
- Появились ли case-studies детекции его отзывов (антифрод сервисы как Otzovik/Яндекс.Маркет)?
- Каков **AI-фактор** в RU-fake-review-индустрии? LLM-generated отзывы дешевле, появились ли «AI-биржи отзывов»?

## Связанные страницы

- [[canon/marketing-frameworks/employer-branding-review-funnel]] — паттерн сбора честных отзывов (employer-branding, transferable)
- [[canon/marketing-frameworks/crisis-pr-principles]] — playbook на случай атаки фейк-отзывами
- [[canon/marketing-frameworks/ai-text-markers-checklist]] — detection AI-generated текста
- [[evolving/content-trends/competitor-data-poisoning-defense-pattern]] — adjacent: defense pattern против data-poisoning
- [[evolving/content-trends/ai-screenshot-trust-crisis-2026]] — adjacent (trust crisis в AI-эпохе)
- [[sources/2026-05-14-tg-startupoftheday-may-5-13-2026]] — оригинал (пост 5059)
