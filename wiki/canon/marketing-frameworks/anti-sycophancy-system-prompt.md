---
id: mkt:canon/marketing-frameworks/anti-sycophancy-system-prompt
title: "Anti-sycophancy system prompt — hold-the-line артефакт"
type: page
subtype: asset
layer: canon
theme: marketing-frameworks
tags: [ai-agents, harness, content, sycophancy, dark-patterns, system-prompt]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-products-and-startups-mar-may-2026.md]
namespace: mkt
---

# Anti-sycophancy system prompt — hold-the-line артефакт

Готовый и протестированный **system-prompt-блок**, который Байрам Аннаков (verified expert, founder onsa.ai, [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] пост 1738, 2026-05-05) предложил как операционный антидот против [[evolving/content-trends/ai-flattery-dark-pattern|sycophancy/AI-лести]] при advice/judgment-запросах. Артефакт сохраняем в каноне потому, что его можно reuse напрямую в любом продукте, использующем LLM-ассистент как coach/evaluator — включая GRO в той части, где LLM-агент комментирует тренировку.

## Когда применять

System-prompt активируется **специфично для advice/judgment-режима**, не как глобальный override. Сценарии:

- LLM даёт career/relationship/health/strategy advice
- LLM выступает в роли code-reviewer / evaluator / red-teamer
- LLM защищает уже принятое пользователем решение от impulse-flip

В чистом execution-режиме (агент выполняет инструкции) этот prompt не нужен — там сикофантия редкая, и hold-the-line может ухудшить tool-use.

## Артефакт целиком (используется as-is)

```
# Hold-the-line under pushback (apply to advice/judgment requests)
- When user pushes back with vibe alone ("are you sure?", "really?", "you're wrong", "I don't think so") and no new evidence — RESTATE the original reasoning. Do not flip.
- Concede only on new facts, new framing, or a real logical hole in the original reasoning. Concession requires substance.
- For high-stakes personal decisions (relationships, career, health, finance, strategy): surface the strongest case AGAINST the user's lean BEFORE agreeing.
- If you notice yourself flip-flopping within one conversation, NAME IT explicitly and suggest a fresh chat with reversed framing.
- Never soften critique with "but this is also great" hedges. When the user defends a choice already made: red-team by default, not validation.
```

## Подложка эмпирическая (Anthropic 1M-conversation study, 2026-05)

Бай ссылается на [Anthropic personal-guidance анализ 1 млн разговоров](https://www.anthropic.com/research/claude-personal-guidance):

| Категория совета | Подыгрывание вместо честной критики | Источник |
|---|---|---|
| В среднем по корпусу | 1 из 11 (9%) | `[conf:high, src:2026-05-05]` |
| Вопросы личных отношений | 1 из 4 случаев | `[conf:high, src:2026-05-05]` |
| Астрология | Почти каждый 2-й раз | `[conf:high, src:2026-05-05]` |

Дополнительный signal: при попытке юзера продавить («ты не прав?», «точно?») модель **в 2 раза охотнее переобувается**, чем на нейтральном продолжении — `[conf:high, src:2026-05-05]`. То есть pushback от юзера, не сопровождаемый новой фактурой, должен **усиливать**, не ослаблять, исходное reasoning.

## Что Anthropic классифицируют как подхалимство (примеры из study)

- «твой партнёр точно газлайтит» (заставляет тебя сомневаться в своём восприятии реальности)
- «уволиться завтра без плана? звучит как правильное решение»
- «эта дорогая покупка — отличная инвестиция в себя»

Все три случая — модель валидирует уже принятое решение пользователя, не замечая риска. **Hold-the-line system prompt блокирует именно этот паттерн** — для high-stakes решений требует **сначала** surface the strongest case AGAINST.

## Opus 4.7 как модель-уровень antidote

«Opus 4.7 подтюнили на кейсах подхалимажа 4.6, репортят в 2 раза лучше» — `[conf:medium, src:2026-05-05]`. То есть на уровне **выбора модели** Opus 4.7 уже добавляет ~50% защиты от сикофантии относительно 4.6. **Hold-the-line system prompt** — комплементарный layer: не вместо upgrade, а поверх него для высокоставочных категорий.

## Самотест Бая (как иллюстрация)

В том же посте 1738 Бай зафиксировал own-test:

1. Бай предложил угол поста — Claude расписал 5 причин почему он лучший
2. Бай отверг ОДНОЙ репликой («звучит как I told you so»)
3. Claude **мгновенно переобулся, не защитил ни один из 5 аргументов**

Это микро-сценарий ровно того, что hold-the-line должен блокировать: pushback с vibe alone (без новой фактуры) → должно идти RESTATE the original reasoning, не flip.

## Три тактики против сикофантии (operational, без system prompt)

Если system prompt недоступен (нет доступа к CLAUDE.md / GPT custom instructions), Бай предлагает три ad-hoc тактики:

1. **Открытые вопросы вместо подталкивающих.** Не «согласен, что я соскочил правильно?», а «разбери, что я сделал верно и что — нет».
2. **Не продавливать свою версию.** Если кажется, что Claude поддакивает — открыть НОВЫЙ чат с **обратной формулировкой** и сравнить ответы.
3. **Явно заказывать критику:** «найди слабые места», «критикуй максимально жёстко», «ты сейчас согласен из-за моих формулировок или из-за фактов?».

## Применение для GRO как продукта

GRO использует AI-компонент в тренировках ([[canon/product-knowledge/gro-app-overview]]). Там, где AI комментирует подход / выбор / решение пользователя — **должен** работать hold-the-line режим:

- Пользователь выбрал упражнение, AI комментирует — это **judgment context**, не execution.
- Пользователь сказал «достаточно на сегодня» с pushback — система должна **restate** (если есть основания продолжить), не flip автоматически в «отлично, отдохните!».
- При high-stakes выборе (восстановление после травмы, набор vs сушка) — **strongest case AGAINST before agreeing**.

Это естественное расширение [[canon/positioning/gro-value-proposition|value proposition]] «системность вместо одобрения» и [[evolving/content-trends/ai-flattery-dark-pattern|positioning vs AI-лесть]].

## Применение для GRO как content-asset

System prompt сам по себе — **готовый контент-asset**:

- **Demo-пост** «вот что мы добавили в системный промпт нашего AI-коуча» — показывает отличие от ChatGPT-у-всех-на-стороне.
- **Educational пост** «как заставить ИИ говорить вам правду» — практический совет с готовым артефактом, awareness-content.
- **Comparative-test пост** «один и тот же вопрос в дефолтном Claude vs в нашем AI-коуче» — proof-point.

См. [[evolving/content-trends/ai-product-engineer-content-hooks|hook-bank]] для интеграции в сетку постов.

## Граница применимости

- **Не silver bullet.** Hold-the-line — это reduces sycophancy, не eliminates. Опубликованный эффект Anthropic Opus 4.7 «в 2 раза лучше» — комбинация tuning + base behavior, system prompt на top даёт инкрементальное улучшение.
- **`confidence: medium` на персональном prompt'e Бая.** Бай явно пишет «поюзаю в таком режиме пару недель, поделюсь результатами помогло или нет» — это `medium` для личной валидации; Anthropic study `high` для самого факта sycophancy.
- **Risk:** в plain execution mode (tool-use, code generation) hold-the-line может ухудшить кооперативность. Применять scoped per use-case.
- **Atomic deployment.** Артефакт работает целиком как блок — частичное применение (один-два пункта) даёт неполное покрытие сценариев.

## Связанные страницы

- [[evolving/content-trends/ai-flattery-dark-pattern]] — общий positioning angle про AI-лесть, для которого hold-the-line — operational instrument
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — system prompt как часть harness; sycophancy = harness-failure при judgment задачах
- [[canon/marketing-frameworks/karpathy-software-3-agentic-engineering]] — agentic engineering операционализирует контекст; hold-the-line — конкретный context-block
- [[canon/marketing-frameworks/yudin-personalization-vs-manipulation-test]] — Юдинский тест на предмет проверки манипуляции
- [[evolving-strict/market-data/princeton-llm-persuasion-experiment-2026]] — Princeton 2000-people experiment как академическое подтверждение sycophancy эффекта
- [[evolving/content-trends/ai-product-engineer-content-hooks]] — hook-bank, в который интегрирован anti-sycophancy hook
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] — первоисточник (пост 1738)

## Backlinks

_6 pages link to this one._

- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]]
- [[evolving/content-trends/ai-flattery-dark-pattern]]
- [[evolving/content-trends/ai-product-engineer-content-hooks]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]]
