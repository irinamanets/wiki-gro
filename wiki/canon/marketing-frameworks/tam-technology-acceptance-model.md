---
id: mkt:canon/marketing-frameworks/tam-technology-acceptance-model
title: TAM — Technology Acceptance Model
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [framework, adoption, barriers, tam, methodology]
confidence: high
stale: false
created: 2026-04-13
updated: 2026-04-13
sources: [sources/2026-04-13-subbotin-ru-ai-telegram-audience.md]
namespace: mkt
---

# Technology Acceptance Model (TAM)

Классическая модель принятия технологии, предложенная Fred D. Davis (1989). TAM объясняет, почему пользователи принимают или отвергают технологию, через два основных фактора: **Perceived Usefulness** (воспринимаемая полезность) и **Perceived Ease of Use** (воспринимаемая простота). Эти два фактора определяют намерение использовать технологию, которое, в свою очередь, предсказывает фактическое использование.

Для `marketing-memory` TAM — это каноничный инструмент для классификации маркетинговых барьеров: когда мы анализируем, почему какая-то аудитория не использует GRO или ИИ-инструменты в целом, мы раскладываем возражения на «не понимаю пользы» vs «кажется сложным», а не валим всё в одну кучу «не нравится продукт».

## Классические факторы TAM

1. **Perceived Usefulness (PU).** Насколько пользователь считает, что технология улучшит его работу / жизнь. В маркетинговых терминах — это value proposition и JTBD. Если PU низкий, даже идеально простой продукт не будет использоваться.
2. **Perceived Ease of Use (PEOU).** Насколько пользователь считает, что технология будет простой в освоении. Влияет и на PU (сложное кажется менее полезным), и напрямую на намерение использовать.
3. **Behavioral Intention to Use.** Намерение использовать — мост между восприятием и реальным действием.
4. **Actual System Use.** Фактическое поведение.

## Расширение TAM для рынков с ограниченным доступом

[[sources/2026-04-13-subbotin-ru-ai-telegram-audience|Исследование Субботина (n=632)]] обнаружило, что для русскоязычного ИИ-рынка классическая TAM недостаточна: 25% аудитории сталкиваются с инфраструктурными ограничениями доступа к ИИ-сервисам, и этот фактор **не описывается** ни PU, ни PEOU. Автор предлагает добавить третий фактор — **Infrastructure Access** — как модифицирующую переменную для рынков с ограниченным доступом к технологиям.

Для marketing-memory это означает: при анализе барьеров GRO или конкурентов на российском рынке нельзя ограничиваться только восприятием полезности и простоты — нужно явно выделять inфраструктурные барьеры (платёжные ограничения, доступ к frontier-моделям, региональная блокировка) как отдельный класс, с отдельной стратегией (альтернативные провайдеры, локальные модели, обход ограничений).

## Как использовать TAM в marketing-memory

- **При анализе отзывов и объекций** ([[evolving/customer-feedback/gro-app-store-reviews]] и подобные) — классифицировать каждую объекцию как «PU-проблема» (не понимаю зачем), «PEOU-проблема» (слишком сложно) или «Infra-проблема» (не могу воспользоваться технически).
- **При проектировании контента** — если PU низкий, контент должен отвечать на «зачем», а не «как». Если PEOU низкий — наоборот.
- **При анализе конкурентов** — раскладывать их value proposition и onboarding через те же оси.
- **При работе с «заблокированной» аудиторией** — не игнорировать её как «небрендовую», а выделять в отдельный сегмент с отдельной стратегией (см. [[canon/target-audience/ru-ai-telegram-audience-segments|сегмент C «Заблокированные»]]).

## Эмпирическое применение на русскоязычной ИИ-аудитории

Исследование Субботина применило TAM к аудитории авторского ТГ-канала об ИИ и обнаружило:

- **PEOU низкий.** 45.6% аудитории указали «нехватку знаний» как главный барьер, три четверти не проходили никакого обучения. Это не технологический, а когнитивный барьер простоты использования.
- **PU средняя, но абстрактная.** 41% хотят агентов и автоматизацию, но не могут артикулировать конкретные задачи. Пользователи понимают, что ИИ может быть полезен, но не видят собственный ROI. 32.1% указали «нехватку времени» — они не инвестируют, пока не уверены в полезности.
- **Infrastructure Access — отдельная ось.** 25% сталкиваются с проблемами доступа к ИИ-сервисам. Эта переменная отсутствует в классической TAM и должна рассматриваться как добавочный фактор для рынков типа РФ.

Подробная раскладка барьеров по сегментам — в [[canon/target-audience/ru-ai-telegram-audience-segments]] и [[evolving/industry-trends/ru-ai-audience-gap-2026]].

## Связанные материалы

- [[canon/marketing-frameworks/rogers-diffusion-of-innovations]] — диффузия инноваций, complement к TAM (TAM — почему принимают, Роджерс — в каком темпе аудитория принимает)
- [[canon/marketing-frameworks/native-advertising]] — нативная реклама как один из каналов преодоления низкого PEOU через демонстрацию
- [[canon/target-audience/ru-ai-telegram-audience-segments]] — пример сегментации, построенной на TAM-осях
- [[sources/2026-04-13-subbotin-ru-ai-telegram-audience]] — эмпирическое применение и предложенное расширение TAM

## Backlinks

_13 pages link to this one._

- [[canon/marketing-frameworks/ankusheva-ai-implementation-triad]]
- [[canon/marketing-frameworks/demin-international-expansion-5-pillars]]
- [[canon/marketing-frameworks/narrative-as-brand-currency]]
- [[canon/marketing-frameworks/organize-to-value-mckinsey]]
- [[canon/marketing-frameworks/petscom-unit-economics-failure]]
- [[canon/marketing-frameworks/rogers-diffusion-of-innovations]]
- [[canon/target-audience/ru-ai-telegram-audience-segments]]
- [[evolving-strict/market-data/ru-ai-telegram-audience-2026]]
- [[evolving/industry-trends/future-of-work-trends-2026]]
- [[evolving/industry-trends/ru-ai-audience-gap-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-04-13-subbotin-ru-ai-telegram-audience]]
