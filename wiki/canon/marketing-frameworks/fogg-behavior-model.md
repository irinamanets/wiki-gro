---
id: mkt:canon/marketing-frameworks/fogg-behavior-model
title: "Fogg Behavior Model (B=MAT) — поведение как пересечение мотивации, способности и триггера"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [behavioral-design, habit, conversion, ux, onboarding, friction, product-management]
confidence: high
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-dzen-delovoymir-habit-product-hook-model.md]
namespace: mkt
---

# Fogg Behavior Model (B = M × A × T)

Reusable поведенческая модель Би Джея Фогга (BJ Fogg, Стэнфорд): **поведение случается, когда мотивация, способность и триггер встречаются в одной точке**. Устоявшийся индустриальный фреймворк; в marketing-memory зафиксирован как canon-константа, потому что это правило проектирования любого «момента действия» — онбординга, CTA, первого шага в продукте.

Источник синтеза — [[sources/2026-05-19-dzen-delovoymir-habit-product-hook-model]] (Деловой мир / Дзен). Модель сама по себе общеиндустриальная (`confidence: high`); атрибуция пересказа — `medium`.

## Формула

> Behavior = Motivation × Ability × Trigger

Все три фактора должны быть достаточны **одновременно**:

- **Motivation (мотивация)** — насколько человек хочет совершить действие. Ресурс ненадёжный: то есть, то нет.
- **Ability (способность)** — насколько действие легко совершить. Управляется уровнем friction.
- **Trigger (триггер)** — стимул, который запускает действие в нужный момент (см. внешние/внутренние триггеры в [[canon/marketing-frameworks/hook-model-habit-loop]]).

## Главное практическое следствие: проектируй ability, а не motivation

> Если способность низкая — нужно очень много мотивации, чтобы человек что-то сделал. А мотивация — ресурс ненадёжный.

Поэтому **не пытайся накачать мотивацию — уменьшай размер действия**, пока его не станет невозможно не сделать. Это самый дешёвый и надёжный рычаг, потому что не зависит от настроения пользователя.

**Примеры low-friction first action:**

- TikTok открывается **сразу на видео** — не нужно ничего искать. `[conf:high, src:2026-05-19]`
- Duolingo предлагает урок на **3 минуты**, а не на 30. `[conf:high, src:2026-05-19]`
- Headspace начинает с медитации на **1 минуту**. `[conf:high, src:2026-05-19]`

Если первое действие требует думать, выбирать, регистрироваться, заполнять профиль — петля рвётся ещё до старта. **Каждый дополнительный шаг до момента ценности — минус к вероятности возврата.**

## Связь с другими фреймворками

- **Hook Model.** Fogg описывает элемент «действие» в петле [[canon/marketing-frameworks/hook-model-habit-loop|Hook Model]]: триггер запускает, ability определяет, состоится ли действие.
- **Funnel simplicity.** Минимизация ability-барьеров — это [[canon/marketing-frameworks/funnel-simplicity-principle|принцип простоты воронки]] на уровне отдельного шага.
- **Онбординг Табунова.** «Уменьшай размер действия» = операционный двигатель правила [[canon/marketing-frameworks/tabunov-onboarding-principles|«даём попользоваться» за 25 секунд]]: первая ценность должна достигаться одним минимальным действием.
- **Retention.** Снижение friction в первом действии напрямую улучшает Time-to-habit и активацию (см. [[canon/marketing-frameworks/habit-retention-diagnostics]]).

## Применение к GRO

GRO обещает «маленькие шаги вместо мотивации» (см. [[canon/product-knowledge/gro-app-overview]] и [[canon/positioning/gro-value-proposition]]) — это буквально Fogg-модель в позиционировании: продукт строит привычку не через накачку мотивации, а через минимальное ежедневное действие (короткая тренировка до 20 минут, в идеале первое действие — ещё короче).

Операционные следствия для GRO:
- Первая тренировка в онбординге — минимально возможная (one-tap старт, без предварительной регистрации/профиля до ценности).
- Триггер целить во внутреннее состояние (тревога о невыполненной цели), а не только в push в фиксированное время.
- Не повышать ability-барьер «обучающими» экранами и видео (anti-pattern из онбординга Табунова).

## Связанные страницы
- [[canon/marketing-frameworks/hook-model-habit-loop]]
- [[canon/marketing-frameworks/habit-retention-diagnostics]]
- [[canon/marketing-frameworks/funnel-simplicity-principle]]
- [[canon/marketing-frameworks/tabunov-onboarding-principles]]
- [[canon/product-knowledge/gro-app-overview]]
- [[canon/positioning/gro-value-proposition]]
- [[sources/2026-05-19-dzen-delovoymir-habit-product-hook-model]]
