---
id: mkt:volatile-strict/industry-news/ru-ai-law-march-2026
title: "Законопроект РФ о регулировании ИИ (март 2026): обучение на опубликованных текстах без согласия — допустимо"
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [legal, ai-regulation, copyright, ru-market, gosduma, training-data, llm-policy, ip-law]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-18-pressfeed-geo-illusion-stability-measure.md]
namespace: mkt
---

# Закон РФ о регулировании ИИ (март 2026) — legal framework для GEO/AI-эпохи

## Факты

В марте 2026 года в Госдуму внесён законопроект о регулировании ИИ `[conf:medium, src:2026-05-18]`. Ключевые положения по упоминанию в Pressfeed:

1. **Обучение моделей на опубликованных авторских текстах без согласия правообладателя признаётся допустимым**, если **пользователь не видит исходника** `[conf:medium, src:2026-05-18]`.
2. **Авторство результата** (AI-generated output) **закрепляется за тем, кто составил промпт и внёс творческий вклад** `[conf:medium, src:2026-05-18]`.

**Что закон не регулирует:**

- Что делать, если нейросеть **воспроизводит пересказ статьи без упоминания автора** — закон **не отвечает** `[conf:medium, src:2026-05-18]`. Эта серая зона остаётся открытой.

## Confidence обоснование

`confidence: medium` — единичный источник (Pressfeed, май 2026), без прямой ссылки на номер законопроекта или текст. Pressfeed указывает «внесли в марте 2026». Прежде чем использовать в legal-материалах GRO, необходимо:

1. Найти конкретный законопроект на duma.gov.ru с номером и текстом
2. Проверить, прошёл ли он первое чтение / в какой стадии находится
3. Сравнить с пунктами Pressfeed на возможную интерпретацию

## Импликации для маркетинга GRO

### Information primacy theft — нет защиты

Сценарий, который описан в [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure|первоисточнике]]: GRO публикует уникальную методику; крупные ресурсы выпускают обзоры с тезисами GRO; AI цитирует **обзоры**, не GRO.

**Legal protection в РФ:** **нет** на 2026-05-18. Согласно закону, training на этих обзорах **допустимо без согласия автора оригинальной статьи** (GRO), пока пользователь не видит дословный исходник. Защита GRO — только **через content-структуру**:

1. Публикация **первой** на собственных площадках
2. Партнёрские версии **специально неполноценны без бренда GRO**
3. Выход на **нескольких авторитетных площадках одновременно** до подхвата темы конкурентами
4. Данные, которые **трудно пересказать**: собственные исследования, первичная аналитика, кейсы с конкретными цифрами

(Подробно — [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] раздел «Information primacy theft»)

### Authorship результата принадлежит prompter

Это **юридически значимое решение** для AI-tools-as-product:

- Если GRO встроит AI-фичу (например, «AI-помощник тренировки» в приложении), **юридически авторство результата** принадлежит пользователю — это устраняет один из юридических рисков AI-фич в продукте
- В обратную сторону: AI-generated marketing-материалы для GRO юридически — авторство менеджера, **писавшего промпт**, не модели

### Cross-border риск

Глобальные модели (ChatGPT, Claude, Gemini) тренируются на данных по своим правилам (Berne Convention, EU AI Act, US case law). RU-закон актуален для **Алисы AI / Яндекс GPT / других RU-моделей**, не для глобальных. Это **усиливает значимость [[canon/marketing-frameworks/geo-platform-segmentation-yandex-chatgpt-perplexity|platform segmentation]]** — разные legal-режимы по платформам.

## Связь с trust-signal

В той же Pressfeed-статье: **28% россиян доверяют тому, что говорит ИИ в поиске**, **в 87% AI-ответов ссылка отсутствует**. Сочетание: `[conf:medium, src:2026-05-18]`

- AI цитирует без ссылки (87%) `[conf:medium, src:2026-05-18]`
- Закон не защищает от пересказа без упоминания
- Пользователь доверяет AI (28%) `[conf:medium, src:2026-05-18]`

= **legally-permitted information laundering**: оригинальный автор не получает credit, не получает trust, не получает traffic. Подробно — [[evolving-strict/market-data/ru-ai-trust-citation-2026]].

## Anti-pattern

1. **Не рассчитывать на legal protection** оригинального автора при information primacy theft в RU-ландшафте.
2. **Не использовать AI-generated тексты с предположением «это не повлияет на authorship»** — авторство закреплено за prompter'ом, но **возможный risk** того, что output воспроизводит обучающие данные — открыт.
3. **Не игнорировать legal-tracking** — это **first-draft** legislation, который может измениться при втором чтении.

## Связанные страницы

- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — content-trend, где information primacy theft разобран operational
- [[evolving/content-trends/geo-when-not-worth-investing-2026]] — disqualification framework для GEO
- [[canon/marketing-frameworks/stochastic-llm-ranking-sparktoro]] — стохастичность как architectural-факт, который усугубляет правовую двусмысленность
- [[evolving-strict/market-data/ru-ai-trust-citation-2026]] — trust-метрики RU-аудитории к AI
- [[canon/marketing-frameworks/geo-platform-segmentation-yandex-chatgpt-perplexity]] — почему RU-закон применим только к RU-моделям
- [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]] — первоисточник упоминания закона
