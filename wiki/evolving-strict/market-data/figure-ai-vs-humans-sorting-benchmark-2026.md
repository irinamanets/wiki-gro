---
id: mkt:evolving-strict/market-data/figure-ai-vs-humans-sorting-benchmark-2026
title: "Figure AI vs люди — бенчмарк сортировки посылок (май 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [robotics, humanoid, figure-ai, market-data, automation, ai]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-breakingtrends-may14-19.md]
namespace: mkt
---

# Figure AI vs люди — бенчмарк сортировки посылок (май 2026)

Прямой head-to-head тест человекоподобных роботов Figure AI против людей на реальной линии сортировки посылок. Опубликован через @breakingtrends 2026-05-18 ([[sources/2026-05-19-tg-breakingtrends-may14-19]] пост #16762). Confidence `medium` — через посредника, без указания независимого первоисточника.

## Условия теста

- Команда стажёров + **3 человекоподобных робота** Figure AI `[conf:medium, src:2026-05-18]`
- **10 часов** работы на линии сортировки в условиях, максимально приближённых к реальным `[conf:medium, src:2026-05-18]`
- Люди работали с обычными перерывами: **30 минут на обед + 2 короткие паузы** `[conf:medium, src:2026-05-18]`
- Роботы работали **без остановки** всё это время `[conf:medium, src:2026-05-18]`

## Результаты

| Участник | Обработано посылок | Скорость | Source |
|---|---|---|---|
| Люди | **12 926** | **2,79 сек/коробка** | `[conf:medium, src:2026-05-18]` |
| Роботы Figure AI | **12 757** | **2,83 сек/коробка** | `[conf:medium, src:2026-05-18]` |

**Итог:** люди **выиграли** — обработали на **169 посылок больше** и были на **0,04 сек/коробку быстрее** `[conf:medium, src:2026-05-18]`, несмотря на перерывы. Роботы при этом работали без отдыха.

## Интерпретация

1. **Productivity-robot reality check.** Даже в простой, повторяемой, предсказуемой задаче (сортировка) топовый humanoid-робот пока **проигрывает** людям по throughput `[conf:medium, src:2026-05-18]` — хоть и с минимальным отрывом. Это сильный counter-signal к мейнстрим-нарративу «роботы заменят рабочих завтра».
2. **Отрыв минимален → траектория ясна.** Разрыв в 1,3% по объёму и 1,4% по скорости — настолько мал, что при текущей скорости улучшения железа/софта роботы догонят людей в обозримом будущем. То есть тест читается двояко: «люди пока лучше» И «роботы почти сравнялись». Оба прочтения валидны как контент-углы. [conf:low, src:2026-05-19]
3. **Экономика, а не только скорость.** Роботы работают без перерывов, отпусков, больничных — даже при равном throughput unit-economics могут склониться в их пользу. Связка с [[evolving-strict/market-data/humanoid-robot-unit-economics-2024-2050]].

## Импликации для маркетинга GRO

- **Content-hook (контр-нарратив):** «Роботы Figure AI 10 часов работали без перерыва — и всё равно проиграли людям с обедом. Что это говорит о реальной готовности AI заменить нас?» Сбалансированный, не алармистский хук про AI-замещение.
- **Connect к augmentation-нарративу GRO:** тест — иллюстрация тезиса «AI/роботы пока augment, а не replace». GRO позиционируется как augmentation-tool (делает человека сильнее, не заменяет) — этот datapoint поддерживает нарратив. См. [[canon/positioning/gro-value-proposition]].
- **Anti-pattern:** не использовать как «роботы провалились / AI-пузырь». Сильная интерпретация — «разрыв уже 1%, и он схлопывается»; слабая — «роботы бесполезны». [conf:low, src:2026-05-19]

## TTL и план верификации

- **TTL: 90 дней (до 2026-08-17)** — точечный benchmark, быстро устаревает с новыми поколениями роботов.
- **Re-verify:** при следующем публичном head-to-head тесте Figure/Optimus/Boston Dynamics или при появлении независимого первоисточника этого теста.

## Связанные страницы
- [[evolving/industry-trends/humanoid-robot-narrative-shift-2026]] — productivity-вертикаль humanoid-нарратива (Figure как один из игроков)
- [[evolving-strict/market-data/humanoid-robot-unit-economics-2024-2050]] — unit-economics роботов (окупаемость, $/час)
- [[evolving/industry-trends/ai-replacing-jobs-global-2026]] — нарратив AI-замещения труда
- [[evolving-strict/market-data/ru-retail-robotization-metrics-2025-2026]] — RU-срез роботизации
- [[canon/positioning/gro-value-proposition]] — augmentation, а не replacement
- [[sources/2026-05-19-tg-breakingtrends-may14-19]] — источник (пост #16762)
