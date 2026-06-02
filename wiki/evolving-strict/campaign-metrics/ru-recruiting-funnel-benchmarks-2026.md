---
id: mkt:evolving-strict/campaign-metrics/ru-recruiting-funnel-benchmarks-2026
title: "Бенчмарки рекрутинговой воронки РФ 2026: response-time, salary-transparency, персонализация"
type: page
subtype: metric
layer: evolving-strict
theme: campaign-metrics
tags: [recruiting, hiring, conversion, benchmarks, funnel, response-time]
confidence: low
stale: false
created: 2026-06-01
updated: 2026-06-01
sources: [sources/2026-06-01-condense-vcru-hr-51-articles.md]
namespace: mkt
---

# Бенчмарки рекрутинговой воронки РФ 2026

Числовые ориентиры **конверсии рекрутинговой воронки** (response-time, salary-transparency, персонализация, source-of-hire vs quality), извлечённые из 6-го батча vc.ru/hr ([[sources/2026-06-01-condense-vcru-hr-51-articles]]).

**Caveat по confidence.** Большинство этих чисел приходят из **native-ad статей Garmony AI** и подобных вендоров — это **vendor-sourced PR-метрики без раскрытой методологии**, повторяемые через десятки advertorial-лонгридов. `confidence: low` по умолчанию. Полезны как **content-anchors** (data-hooks для постов про найм и про скорость процесса), а не как верифицированный рыночный факт. Где найм-стоимостные бенчмарки (CPH/TTH/QoH) — см. соседнюю [[evolving-strict/market-data/ru-hiring-cost-benchmarks-2026]]; эта страница — про **конверсию воронки**, не про стоимость.

## Response-time как конверсионный рычаг

| Метрика | Значение | Source |
|---|---|---|
| Снижение time-to-first-response с 72 ч до 2 ч → рост конверсии в оффер | +35–40% | `[conf:low, src:2026-05-30]` |
| Доля кандидатов, отказывающихся продолжать без ответа в течение 3 дней | 78% | `[conf:low, src:2026-05-30]` |
| Короткое видео (60 сек) от будущего руководителя в описании вакансии → рост конверсии в отклик | +35–40% | `[conf:low, src:2026-05-30]` |

Скорость реакции в 2026 подаётся как конкурентное преимущество, **сопоставимое с уровнем зарплаты** (qualitative-нарратив, [[evolving/industry-trends/ru-hr-tech-ai-landscape-2026]]). Это прямой proof-point для AI-рекрутинг-вендоров: «автокоммуникация = первый ответ за 2 ч».

## Salary-transparency

| Метрика | Значение | Source |
|---|---|---|
| Доля сильных кандидатов, не откликающихся на вакансии без зарплатной вилки | 50% | `[conf:low, src:2026-05-30]` |
| Доля кандидатов, готовых отказаться при полностью автоматизированной коммуникации | 76% | `[conf:low, src:2026-05-30]` |

Salary-transparency-сигнал согласуется с «vacancy-as-ad» рамкой ([[canon/marketing-frameworks/vacancy-as-marketing-material]]): «прозрачные деньги» — один из четырёх обязательных элементов конвертирующей вакансии.

## Персонализация аутрича

| Метрика | Значение | Source |
|---|---|---|
| Конверсия персонализированного сообщения (LinkedIn/TenChat) — доля ответов | 10–15% | `[conf:low, src:2026-05-30]` |
| Конверсия массовой рассылки — доля ответов | 1–2% | `[conf:low, src:2026-05-30]` |

Разрыв ~7-10× между персонализированным и массовым аутричем — переносимый бенчмарк и за пределы рекрутинга (B2B-outreach в целом).

## Source-of-hire vs quality-of-hire (иллюстративные native-ad числа)

| Канал | Доля откликов | Quality / конверсия | Source |
|---|---|---|---|
| hh.ru | ~60–80% | 5–15% quality | `[conf:low, src:2026-05-30]` |
| Реферальная программа | ~5–15% | 45–52% quality/конверсии | `[conf:low, src:2026-05-30]` |
| Хабр Карьера | ~12–20% | 35–38% конверсии | `[conf:low, src:2026-05-30]` |

Инверсия «много откликов ≠ много качества»: широкие агрегаторы дают объём при низком quality, рефералы — обратное. Согласуется с реферальными числами в [[evolving-strict/market-data/ru-hiring-cost-benchmarks-2026]] (реферал даёт 25-35% наймов с максимальным QoH). [conf:low, src:2026-06-01]

## Дополнительные воронко-релевантные anchors

| Метрика | Значение | Source |
|---|---|---|
| Контр-оффер от текущего работодателя (IT/маркетинг/финансы) | 60–70% случаев | `[conf:low, src:2026-05-30]` |
| Ручной скрининг: время на вакансию (3–5 мин × 200–500 резюме) | 15–40 ч | `[conf:low, src:2026-05-30]` |
| Стоимость скрининга одной вакансии (при ЗП рекрутера 150к ₽/мес ≈ 937 ₽/ч) | 14–16 тыс. ₽ | `[conf:low, src:2026-05-30]` |
| HR-специалисты, тратящие до 80% времени на задачи без человеческого суждения | 67% | `[conf:low, src:2026-05-30]` |
| 83% оптимизируют резюме через ChatGPT → реально подходящих в потоке | 8–15% | `[conf:low, src:2026-05-30]` |

Последняя строка — двусторонний сигнал: AI-инфляция откликов снижает signal-to-noise воронки, что усиливает спрос на NLP-скрининг (vendor-нарратив Garmony) и на candidate-side AI ([[evolving/industry-trends/candidate-side-ai-services-2026]]).

## Content-hooks для GRO

- «78% кандидатов уходят, если вы не ответили за 3 дня. Скорость — это новая зарплата» — hook для Сегмента 2 (работодатели). `[conf:low, src:2026-05-30]`
- «Персонализированное сообщение конвертит в 7-10 раз лучше массовой рассылки» — переносимый outreach-anchor. `[conf:low, src:2026-05-30]`
- «83% кандидатов пишут резюме через ChatGPT, реально подходят 8-15%» — anxiety/абсурд-hook про слом скрининга. `[conf:low, src:2026-05-30]`

## Связанные страницы
- [[evolving-strict/market-data/ru-hiring-cost-benchmarks-2026]] — стоимостные бенчмарки найма (CPH/TTH/QoH), комплементарны
- [[canon/marketing-frameworks/vacancy-as-marketing-material]] — vacancy-as-ad (salary-transparency как элемент конверсии)
- [[evolving/industry-trends/candidate-side-ai-services-2026]] — AI-инфляция откликов на стороне кандидата
- [[evolving/industry-trends/ru-hr-tech-ai-landscape-2026]] — vendor-контекст (Garmony как источник чисел)
- [[evolving/industry-trends/ai-recruiting-humanity-countertrend-2026]] — 76% против полностью автоматизированной коммуникации [conf:low, src:2026-06-01]
- [[sources/2026-06-01-condense-vcru-hr-51-articles]] — первоисточник (6-й батч)
