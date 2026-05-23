---
id: mkt:evolving-strict/competitor-metrics/llm-rewrite-quality-benchmark-2026
title: "Бенчмарк качества рерайта: штампы и галлюцинации по 7 сервисам (Pressfeed-тест, 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [ai, llm, rewrite, benchmark, content-quality, claude, gpt, deepseek, yandexgpt, market-data]
confidence: medium
stale: false
created: 2026-05-18
updated: 2026-05-18
sources: [sources/2026-05-18-pressfeed-rerajt-tools-2026-landscape.md]
namespace: mkt
---

# Бенчмарк качества рерайта: штампы и галлюцинации по 7 сервисам

Числовой результат **single-source single-test** замера от автора [[sources/2026-05-18-pressfeed-rerajt-tools-2026-landscape|статьи Pressfeed (2026-05-18)]]. Методология: одна короткая агентская новость РИА (1500 знаков, март 2026), прогнана через 7 сервисов **без кастомного промпта** (инструкция «перепиши своими словами»); подсчитаны штампы и галлюцинации, выставлена субъективная оценка.

**Почему `evolving-strict`:** конкретные числа с привязкой к датам и моделям, обновляются с release-cycle (~3-6 мес), inline-маркеры обязательны. **Caveat по достоверности:** один тест, один автор, один промпт-режим («голый»), субъективные оценки. Это **directional signal, не authority-бенчмарк** — для high-confidence нужны независимые повторы. `confidence: medium`.

## Результаты теста (1500 знаков, без кастомного промпта)

| Сервис | Категория | Штампы (на 1000 знаков) | Галлюцинации | Субъективная оценка | Source |
|---|---|---|---|---|---|
| Claude Sonnet 4.6 | голый LLM | 1 | 0 | 7,5 / 10 | `[conf:medium, src:2026-05-18]` |
| GPT-5 | голый LLM | 2 | н/у | 7 / 10 | `[conf:medium, src:2026-05-18]` |
| DeepSeek V3 | голый LLM | 2 | 1 (вставила левую цифру) | 6,5 / 10 | `[conf:medium, src:2026-05-18]` |
| YandexGPT | голый LLM (РФ) | 3 | н/у | 5 / 10 | `[conf:medium, src:2026-05-18]` |
| PR-CY | обёртка | 3 | н/у | 5 / 10 | `[conf:medium, src:2026-05-18]` |
| Raskruty | SEO-синонимайзер | 4 | н/у | 2 / 10 | `[conf:medium, src:2026-05-18]` |

(«н/у» — галлюцинации в источнике явно не названы для этого сервиса; явно зафиксированы только у Claude — 0 и у DeepSeek — 1.)

## Производные наблюдения

- **Лидер по качеству в тесте — Claude Sonnet 4.6**: минимум штампов (1 на 1000 знаков) и ноль галлюцинаций. `[conf:medium, src:2026-05-18]`
- **Разрыв синонимайзер → LLM**: Raskruty дал 4 штампа и оценку 2/10, любой голый LLM — ≥5/10. `[conf:medium, src:2026-05-18]`
- **Обёртка не лучше голого LLM**: PR-CY (обёртка, 5/10) уступает Claude/GPT/DeepSeek (голые LLM, 6,5-7,5/10). `[conf:medium, src:2026-05-18]`
- **DeepSeek V3 — лучшая цена/качество** при оговорке про галлюцинацию: 6,5/10 при стоимости в 5-10× ниже GPT. `[conf:medium, src:2026-05-18]`

## Сопутствующие ценовые / цензурные факты

- DeepSeek V3 — в **5-10× дешевле GPT**. `[conf:medium, src:2026-05-18]` Согласуется с дефляцией токенов — [[evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026]].
- Обёртки накручивают до **+300%** к стоимости той же модели напрямую. `[conf:medium, src:2026-05-18]`
- Классический SEO-рерайт у бирж — **~30 ₽ за 1000 знаков**. `[conf:low, src:2026-05-18]`
- Автор разобрала суммарно **24 инструмента** (в таблицу теста попали 7). `[conf:medium, src:2026-05-18]`

## Главный методологический вывод первоисточника

Тест проводился **без кастомного промпта** — это и есть baseline «голой» работы. Вывод автора: без нормального промпта **любая** LLM работает посредственно; качество начинается с процесса вокруг модели (стилевой профиль, фактчек, критика, правка). То есть таблица фиксирует **нижнюю границу** возможностей каждого сервиса, а не потолок. См. рамку [[canon/marketing-frameworks/rewrite-task-tool-matching-2026]].

## TTL и план верификации

- TTL: 90 дней soft — числа быстро устаревают с релизами моделей (Sonnet 5 / GPT-5.5 / Gemini 3.x).
- Что отслеживать: появление независимых RU-бенчмарков рерайта (для повышения confidence до high); смена «кто внутри обёрток».
- Контр-сигнал: независимый тест с противоположным ранжированием → пометить страницу `confidence: low` и зафиксировать противоречие.

## Связанные страницы
- [[sources/2026-05-18-pressfeed-rerajt-tools-2026-landscape]] — первоисточник теста
- [[evolving/competitor-positioning/ai-rewriter-tool-landscape-5-tiers-2026]] — качественная карта тех же сервисов
- [[canon/marketing-frameworks/rewrite-task-tool-matching-2026]] — почему baseline «голой» работы — нижняя граница
- [[evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026]] — ценовой контекст (DeepSeek в 5-10× дешевле)
- [[evolving/content-trends/ai-text-detection-landscape-2026]] — почему % уникальности от детектора не метрика качества
</content>
