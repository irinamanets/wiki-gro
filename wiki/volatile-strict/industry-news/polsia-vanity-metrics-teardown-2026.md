---
id: mkt:volatile-strict/industry-news/polsia-vanity-metrics-teardown-2026
title: Polsia — $30M раунд при разоблачённых vanity-метриках (Табунов / NotOnKetamine, май 2026)
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [ai, vanity-metrics, vc-narrative, ai-wrapper, solopreneurship, churn, arr, case-study, news]
confidence: medium
stale: false
created: 2026-05-30
updated: 2026-05-30
sources: [sources/2026-05-30-tg-your-pet-project-may-27-29-2026.md]
namespace: mkt
---

# Polsia — $30M раунд при разоблачённых vanity-метриках

Кейс-разбор от Михаила Табунова ([[sources/2026-05-30-tg-your-pet-project-may-27-29-2026|@your_pet_project пост 640, 2026-05-29]]) с цитированием публичного teardown'а исследователя под ником NotOnKetamine. Это **cautionary-tale** про разрыв между заявленными метриками AI-стартапа и реальной unit-экономикой — и про то, что VC всё равно дали раунд.

**Почему `volatile-strict`.** Кейс свежий, метрики оспариваемые, исход (выживет ли база при churn 48%/мес) станет ясен только через год — рынок одиночных AI-компаний меняется еженедельно. TTL 14–90 дней: после лета 2026 кейс надо либо перепроверить, либо мигрировать в evolving как закрытую историю. Inline-маркеры на всех числах; источник чисел — пересказ Табунова и публикация NotOnKetamine, не first-party отчётность Polsia, отсюда `confidence: medium`. [conf:low, src:2026-05-30]

## Заявленные метрики (Polsia / фаундер Бен Сера)

| Метрика | Значение | Источник |
|---|---|---|
| Возраст проекта | ~6 месяцев на момент раунда | `[conf:medium, src:2026-05-29]` |
| Заявленный ARR | $10M | `[conf:medium, src:2026-05-29]` |
| «Созданных компаний» на платформе | 120 000+ (точно 118 683) | `[conf:medium, src:2026-05-29]` |
| Привлечённый раунд | $30M | `[conf:high, src:2026-05-29]` |
| Оценка | $250M | `[conf:high, src:2026-05-29]` |
| Подписка | $50/мес + 20% с выручки сгенерённых компаний + 20% с рекламного бюджета | `[conf:medium, src:2026-05-29]` |
| Инвесторы | Sound Ventures (фонд Эштона Кутчера), True Ventures, ангелы | `[conf:high, src:2026-05-29]` |

Позиционирование: «AI, который запускает компанию под ключ», «оркестр AI-агентов, который ведёт твой бизнес 24/7». Раунд [реально состоялся](https://www.trueventures.com/blog/polsia-one-person-company-no-longer-a-metaphor) `[conf:high, src:2026-05-29]`.

## Разоблачение (NotOnKetamine teardown)

| Что разоблачено | Цифра | Источник |
|---|---|---|
| Реальная подписочная выручка из заявленных $10M ARR | $4.6M (остальное — разовые покупки + прогон рекламного бюджета юзеров; месячный кешфлоу × 12) | `[conf:medium, src:2026-05-29]` |
| Месячный churn | 48% | `[conf:medium, src:2026-05-29]` |
| Остаток платящей базы через год при таком churn | 0.04% | `[conf:medium, src:2026-05-29]` |
| Живых «компаний» из 118 683 | 7 437 (6.3%; остальные 94% — брошенные пустышки) | `[conf:medium, src:2026-05-29]` |
| Доля выручки от подписок, уходящая на compute (Claude через AWS Bedrock) | 57% (продукт убыточен ещё до зарплат) | `[conf:medium, src:2026-05-29]` |
| «Флагманские» компании с витрины, показывающие выручку | 16 из 16 показывают $0.00; у свежесозданных нет формы оплаты (ни Stripe, ни checkout) | `[conf:medium, src:2026-05-29]` |
| Природа «автономного AI» | обёртка над Claude; в коде найдена админка с живыми операторами, вручную оценивающими работу агентов | `[conf:medium, src:2026-05-29]` |

**Вишенка:** Polsia задом наперёд читается как AISLOP (AI Slop, «ИИ-помои») `[conf:high, src:2026-05-29]`.

## Три объяснения (Табунов)

1. **Перформанс / арт.** Стартап как акт современного искусства; название не случайно, фаундер открыто говорит, что большая часть выхлопа — мусор.
2. **Чистый хайп на VC.** «Венчуры не покупают unit-экономику, они покупают нарратив. "Первая полностью автономная AI-компания" — топовый нарратив 2026 года.»
3. **Эпоха.** «Можно собрать обёртку над Claude, прикрутить хайповый лендинг, нагнать псевдо-ARR через подписки и ad pass-through, и поднять $30M. Сильный продукт не нужен.»

Куда пойдут деньги (по заявлению фаундера): офис, зарплата основателю, compute, маркетинг; плюс намерение выделить 10% акций самому AI, нанять команду, а потом заменить и её на AI `[conf:low, src:2026-05-29]`.

Финальный вердикт Табунова: «Скам это или гениальный маркетинг — покажет churn. Через год база схлопнется. Возможно, главный кейс 2026 года про то, как реально работает рынок.»

## Лендинг (визуал)

Обложка лендинга (см. [[sources/2026-05-30-tg-your-pet-project-may-27-29-2026|source, OCR media 640]]): ч/б корпоративный офис с кубиклами, заголовок «Polsia», слоган **«AI That Runs Your Company While You Sleep»**, CTA «GET STARTED». Хайповый лендинг — ровно тот «прикрученный лендинг» из объяснения №3.

## Связь с метриками и трендами

- **Псевдо-ARR через ad pass-through** — тот же приём «месячный кешфлоу × 12», что и в разборе Den's case в [[volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026]] (revenue vs profit разрыв). Прямой контраст к bootstrap-кейсам с честной unit-экономикой (Wave AI, Medvi).
- **Compute > 50% выручки** — повторяет паттерн «маржа = 43%, 57% токены» из Wave AI ([[volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026]]): AI-обёртки структурно упираются в compute-косты. [conf:low, src:2026-05-30]
- **Обёртка над Claude + живые операторы в админке** — то же разоблачение «автономности», что и тезис Табунова про OpenClaw (вирусность = дистрибуция, не автономность) и про неработающие юзкейсы автономных агентов — см. [[evolving/industry-trends/agent-first-world-openclaw-2026]].
- **VC покупают нарратив, не unit-экономику** — anti-pattern к [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov|bootstrap-парадигме]] и к [[canon/marketing-frameworks/zero-to-one-vs-scale-tabunov|Fab.com cautionary]].

## Позиция GRO

**Cautionary tale, не позитивный пример.** GRO как продукт про дисциплину и измеримую продуктивность не может ассоциироваться с псевдо-ARR и «обёртками без продукта». Использовать только как editorial-skepticism awareness-контент: «учитесь отличать нарратив от unit-экономики». Готовые anti-hooks — в [[evolving/content-trends/your-pet-project-channel-hooks]].

## Связанные страницы
- [[sources/2026-05-30-tg-your-pet-project-may-27-29-2026]]
- [[volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026]]
- [[evolving/industry-trends/agent-first-world-openclaw-2026]]
- [[evolving/industry-trends/ai-agent-marketing-capability-boundary-2026]]
- [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]]
- [[canon/marketing-frameworks/zero-to-one-vs-scale-tabunov]]
- [[evolving/content-trends/your-pet-project-channel-hooks]]
</content>
