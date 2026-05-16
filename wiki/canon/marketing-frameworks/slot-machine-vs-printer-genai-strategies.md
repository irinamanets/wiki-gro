---
id: mkt:canon/marketing-frameworks/slot-machine-vs-printer-genai-strategies
title: "Слот-машина vs принтер — две стратегии GenAI-продуктов и метафора cost per task"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai-agents, positioning, b2b-sales, content, awareness]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-products-and-startups-may-2026.md]
namespace: mkt
---

# Слот-машина vs принтер — две стратегии GenAI-продуктов

**Источник:** Байрам Аннаков, пост 1745 ([[sources/2026-05-14-tg-products-and-startups-may-2026]]). Развитие метафоры одного из клиентов onsa («Я в Лас-Вегасе», после $150 слитых на генерацию промо-ролика через HeyGen) в полноценный позиционный фреймворк для GenAI-продуктов.

## Базовая метафора

> «Я сижу в казино, дёргаю слот: иногда сходится, эйфория, как бы победа — а в следующий раз всё ломается заново. Слил уже $150 и так и не получилось.» — клиент onsa, после неудачных попыток сгенерировать промо-видео в HeyGen.

GenAI-продукт, который ставит юзера в положение «крути ручку, пока не получится» — слот-машина. GenAI-продукт, который выдаёт результат с первого раза — принтер. Между ними **транзакционная экономика** (рента, заработанная на самой случайности модели), переходящая в **отток**, когда модели становятся детерминированнее.

## Цитата Kitze (talk)

> «My favorite [analogy] is a comparison to a casino. So in casino you buy chips. Here you buy tokens. You spin the slots or you press generate. You might hit the jackpot or nothing. You get a functional full stack app or garbage. Flashing lights, active animation. "You're absolutely right." "Great idea." "I've got my own strategy. I'm a prompt engineer."»

Это **подтверждение** метафоры из независимого источника: значит, паттерн уже узнаваем рынком, не уникальное наблюдение Бая.

## Loss Disguised as a Win (Rachel Thomas, fast.ai)

Rachel Thomas в посте на [fast.ai от 2026-01-28](https://www.fast.ai/posts/2026-01-28-dark-flow/) приводит понятие из мира gambling:

> На мультилайн-слотах можно поставить 20 центов и получить 15 кредитов обратно с разными «свистелками-перделками». Мы реагируем на это как на выигрыш, хотя по факту в минусе на 5.

**Применение к GenAI:** скорость, количество сгенерированного кода, «собрал прототип за час» ощущаются как победа. Через неделю выясняется, что **в 9 раз больше уязвимостей** (см. [[canon/marketing-frameworks/vibecoding-stanford-study-2026]]). Это и есть Loss Disguised as a Win — проигрыш закамуфлированный под выигрыш.

## Почему диффузионные модели — главные слот-машины

Гипотеза Бая: чем больше степеней свободы у выхода модели, тем сильнее слот-эффект.

- LLM-текст: десятки тысяч токенов на выходе, но валидируется человеком быстро (1-2 минуты прочесть)
- Картинка: миллионы пикселей, валидация — глаз/час
- Видео: миллионы пикселей × время, валидация дольше

→ Видео и картинки — самые сильные слот-машины. Диффузионные модели «генерят из шума», ощущение «ну вот почти круто, но вот немножечко тут подкрутим» = слот-аппарат, в котором почти выпало 777.

## Связь с tokenmaxxing (SemiAnalysis)

SemiAnalysis ввели термин **tokenmaxxing** в своём newsletter «The Coding Assistant Breakdown»: одна и та же задача потребляет всё больше токенов, потому что ради повышения качества бросаем на неё больше попыток / больше reasoning'a.

**Cost dynamics на 2026:**
- Цена за токен стремительно падает (commodity)
- НО объём токенов на задачу растёт быстрее
- ⇒ **cost per task растёт**, а cost per token падает
- Соотношение Input:Output в Claude Code = **100:1** — то есть основная нагрузка на context-window, а не на генерацию

**Главное операционное правило Бая:**

> Важнее следить не за cost per token, а за **cost per task**. И постоянно чекать: а действительно ли улучшается качество с ростом этого индикатора?

## Две стратегии для builder'ов

Бай выделяет два архетипа GenAI-продуктов:

### Slot-machine-стратегия

- **Юнит-экономика:** N попыток на одну удачу, где N>1
- **Выручка:** растёт пропорционально N (больше пуллов = больше дохода)
- **Психология:** допамин-фидбэк на «почти выиграл», dark flow
- **Транзакционная рента:** работает, пока модели плохо детерминированы
- **Зависимость от лабораторий:** обратная — улучшение моделей **снижает** выручку
- **Пример:** HeyGen, многие AI-video продукты с прямым consumer-flow

### Printer-стратегия

- **Юнит-экономика:** ≤1 попытка на результат
- **Выручка:** ниже на сессию, но retention выше
- **Психология:** «спокойная экспертность», доверие
- **Долгосрочная позиция:** усиливается с улучшением моделей
- **Зависимость от лабораторий:** прямая — улучшение моделей **повышает** ценность
- **Пример:** onsa (B2B sales automation с детерминированными промежуточными шагами), Robin AI Chief of Staff (помнит, не делает — см. [[evolving/competitor-positioning/onsa-robin-ai-chief-of-staff]])

## Transitional rent — почему slot-machine не вечна

Бай вводит понятие **transitional rent** (временная рента): доход, который существует **только пока** есть market gap. Slot-machine GenAI продукты живут transitional rent на недетерминированности диффузии и LLM.

«Если ваша юнит-экономика завязана на N>1 попыток — вы зависите от **темпов улучшения моделей** в части детерминированности. Чем быстрее лаборатории решат `mechanistic interpretability` ([[sources/2026-05-14-tg-products-and-startups-may-2026]] ссылка из 1745 на пост 1260) — тем быстрее ваш бизнес обнулится.»

**Сигналы исхода transitional rent:**
- Лидирующие лаборатории публикуют работы по mech-interp
- Запуск reproducible inference modes (deterministic-сэмплирование)
- Появление контр-стартапов с «принтер-режимом» в том же сегменте

## Применение к GRO-позиционированию

**Готовая антипозиция против слот-машинных конкурентов:**

> «GRO не заставляет вас крутить барабан. Каждая тренировка — это результат с первого раза, а не "попробуй ещё разок"».

Целевые конкуренты для этой антипозиции:
- AI-fitness стартапы, генерирующие план каждый раз заново при минимальном изменении запроса
- Generic AI-coaching продукты с «сгенерируй мне рутину» ➝ результат каждый раз другой
- ChatGPT-обвязки без памяти и без harness

**Контент-хуки** (см. [[evolving/content-trends/ai-product-engineer-content-hooks]] update «Я в Вегасе»):
- «Сколько $ вы уже слили на GenAI, который "почти получился"?»
- «Slot vs printer» — explainer-пост про две стратегии AI-продуктов
- «Cost per task, не cost per token» — методологический пост для founder-аудитории

## Гипотезы для проверки

Бай предлагает два направления исследования:

1. **Статистика распределения токенов по типам задач:** если slot-machine-свойство реально, то для image/video задач **уходит больше токенов** и **вариабельность выше** (то all-shot работает, то нужно бесконечно крутить).

2. **Correlation between determinism and retention:** retention выше у продуктов с меньшим N. Гипотеза измеримая, если вытянуть статистику churn'a из открытых AI-продуктов.

## Anti-patterns

- **Маркетировать улучшение моделей как "теперь крутить надо меньше"** — это сигнал юзеру, что раньше он переплачивал. Лучше fold improvement в новый pricing tier.
- **Hide cost per task за метрикой "tokens consumed"** — слот-машина-маскировка. Юзеру нужна метрика «сколько попыток в среднем», не «сколько токенов».
- **Игнорировать transitional rent в долгосрочной стратегии** — даже если сейчас 2x rev на slot-mode, через 12-18 месяцев это исчезнет.

## Связь с другими страницами

- [[canon/marketing-frameworks/vibecoding-stanford-study-2026]] — численная основа метафоры (Loss Disguised as a Win = 9× уязвимостей через неделю)
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — printer-стратегия = harness-инжиниринг применённый к продуктовому UX
- [[evolving/competitor-positioning/onsa-robin-ai-chief-of-staff]] — пример printer-стратегии в B2B продукте
- [[evolving/content-trends/ai-product-engineer-content-hooks]] — готовые хуки на основе этой метафоры
- [[evolving/industry-trends/ai-cognitive-atrophy-identity-2026]] — связь dark flow / dopamine loop с long-term cognitive cost
- [[canon/positioning/gro-value-proposition]] — printer-стратегия применима к GRO

## Источники

- [[sources/2026-05-14-tg-products-and-startups-may-2026]] — пост 1745, attached/1745 (slot-machine + printer illustration)
- youtube.com/watch?v=JV-wY5pxXLo — Kitze talk с casino-метафорой
- fast.ai/posts/2026-01-28-dark-flow — Rachel Thomas про Loss Disguised as a Win
- newsletter.semianalysis.com/p/the-coding-assistant-breakdown-more — SemiAnalysis tokenmaxxing
