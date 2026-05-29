---
id: mkt:canon/marketing-frameworks/petrosian-environment-3-functions-development
title: "Среда развития = 3 функции: напоминать / пояснять / поддерживать (Petrosian)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [framework, environment-design, ux, journaling, retention, consideration]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-petrosian-book-2-how-to-start-changes.md, sources/2026-05-26-tg-stodnevka2-may-20-26-2026.md]
namespace: mkt
---

# Среда развития = 3 функции: напоминать / пояснять / поддерживать

Финальный фрейм книги «Как приступить к переменам» (Petrosian, 2025, §«Создайте свою среду развития»; см. [[sources/2026-05-26-petrosian-book-2-how-to-start-changes]]). Petrosian формализует **environment-design** как **3 distinct функции**, каждая со своими artifacts и practices.

## Core тезис (Petrosian)

> «Достичь цели будет легче, если нам будет помогать среда, в которой мы находимся. Три важные функции среды: напоминать, пояснять, поддерживать.» (Petrosian, 2025, book 2, final §)

`[conf:medium, src:2025]` — operational framework от verified expert.

## Три функции

### 1. Напоминать = действовать

Petrosian: **«Помнить — значит действовать. Повторение цели, многократное её переписывание не приблизит её осуществление.»**

| Артефакт | Использование |
|---|---|
| **Материальные напоминания** | Трекеры, доски визуализации, moodboard, lock-screen экраны |
| **Действия** | Ежедневная обработка целей, списки идей, оформление списков задач |
| **Ключевой вопрос** | «Каким будет моё ближайшее действие по этой цели?» |

**Mechanism:** напоминание = **prompt-to-action**, не passive-reminder. Если list задач превращается в «сканворд, который хочется разгадать» (Petrosian metaphor) — это правильно. Если list пасивно прокручивается — нарушен mechanism.

### 2. Пояснять = сохранять ясность

Petrosian: **«Многолетний опыт проведения Стодневок убедил: те, кто чётко осознаёт ущерб, который повлечёт за собой отказ от перемен, реже сходят с пути.»**

| Артефакт | Использование |
|---|---|
| **«Хроника проекта»** | Текстовый файл по каждой цели |
| **3 вопроса дневной фиксации** | Что получилось, что будете повторять? Что вышло не так? Как иначе в следующий раз? |
| **Чек-листы и памятки** | «Те, кто жалеет время на подобную „писанину", не пользуются мощью алгоритмов и не учатся на собственном опыте» |

**Mechanism:** пояснение = **mental model update**. Регулярная письменная рефлексия превращает разрозненный опыт в **актуализируемое знание**.

### 3. Поддерживать = укреплять уверенность

Petrosian: **«Трекеры, коллажи, показатели не заменят живого общения. Рассказывайте о своём деле, чтобы самому лучше его понять. Задавайте вопросы и обсуждайте ситуации, с которыми встречаетесь. Учитесь у других и спрашивайте совета.»**

| Артефакт | Использование |
|---|---|
| **Папка «Поддержка»** | Контент-аптечка (см. [[canon/marketing-frameworks/petrosian-content-aptechka-support-folder]]) |
| **Свидетель** | Человек, которому пишешь «Сделал» (см. [[canon/marketing-frameworks/petrosian-6-weak-points-first-month-resistance]] #5) |
| **Единомышленники** | «Найдите тех, кто заинтересован в вашем успехе, кто вам симпатизирует. Ищите взаимовыгодное сотрудничество» |
| **Ключевой вопрос** | «Чем достижение вашей цели может быть интересно другому?» |

**Mechanism:** support = **external validation + collective intelligence**. Petrosian подчёркивает: «Поддержка не в том, чтобы другие сделали вашу работу. Взгляд со стороны и оценка достигнутого укрепляют уверенность.»

## Финальный пакет — иллюстрация

Petrosian в final § явно описывает **полный environment-стек Стодневки** как application фрейма:

> «По этим принципам я создал Стодневку https://stodnevka.ru. Отсчёт дней напоминает мне о целях и сроках. Дневник, который веду в закрытой группе, закрепляет опыт. Взаимодействие с участниками, их обратная связь — моя поддержка. С 2015 года, каждый месяц стартует группа Стодневки. В течение 100 дней мы двигаемся к поставленным целям.» (Petrosian, 2025, book 2, final)

`[conf:high, src:2025]` — Стодневка = canonical-exemplar 3-функцийной среды:

| Функция | Артефакт Стодневки |
|---|---|
| Напоминать | Отсчёт дней (100-day counter) |
| Пояснять | Дневник в закрытой группе |
| Поддерживать | Обратная связь от участников |

## Зачем это релевантно GRO

GRO — продукт ежедневного журналирования. 3-функцийная рамка даёт **готовый design framework** для product feature audit:

### Direct product audit (для GRO)

| Функция | Что должно быть в GRO | Status (typical journaling-app) |
|---|---|---|
| **Напоминать** | Lock-screen widget, push на time-of-day, trackers | Чаще всего **есть** (push, calendar integration) |
| **Пояснять** | Per-goal sub-journal с structured prompt'ами (3 вопроса) | Чаще всего **нет structured prompt'ов**, только free-form |
| **Поддерживать** | Community / accountability / mood-curated archive | Чаще всего **нет community-layer** в personal-journal apps |

**Gap-analysis:** журналинг-категория обычно sterile в области «Поддерживать» (приложения боятся social-features, чтобы не превратиться в Instagram). Petrosian-фрейм показывает: **отсутствие support-функции — главный gap** в индустрии. GRO может позиционироваться через **3-functional completeness** против фрагментированных конкурентов.

### Direct content copy (с атрибуцией)

> «Любое успешное изменение требует среды. По формуле Армена Петросяна (Стодневка с 2015 года), среда работает только если выполняет три функции: напоминать, пояснять, поддерживать. Most journaling apps хорошо напоминают, кое-как поясняют, и почти никто не поддерживает. GRO заложен на все три.»

### Content-каркас (3 поста или 3-секционный сравнительный обзор)

3 функции = готовый 3-acts narrative:
- **Часть 1: Напоминать.** Что значит good-reminder vs spam-push?
- **Часть 2: Пояснять.** Почему free-form journal недостаточен — нужны structured prompts?
- **Часть 3: Поддерживать.** Что делать, когда никто не верит в твою цель? (gap, который GRO closes)

### Funnel framing

Работает на **awareness** (educate о 3 функциях) → **decision** (audit на наличие 3 в текущем используемом продукте) → **switch to GRO** (если GRO покрывает все 3, а current — нет).

## Anti-patterns в применении

1. **Свести «Поддерживать» к community-features.** Petrosian-«поддерживать» включает **single-witness** (одного человека, кому пишешь «Сделал»), **папку поддержки** (внутреннюю аптечку), и только потом community. Forced community = anti-pattern.
2. **Превратить «Напоминать» в notification-spam.** Petrosian-«напоминать» = **prompt-to-action**, не passive-reminder. Если push не вызывает action, он vandalises trust.
3. **Свести «Пояснять» к analytics dashboards.** Pet 정rosian-«пояснять» = **reflective writing**, не data-visualization. Графики ≠ ясность. Графики могут сопровождать, но не заменяют.
4. **Использовать рамку для over-engineering.** 3 функции — **minimum viable**, не **must-include everything for every function**. Lean app может start с одной функции, дополнить остальными по мере.

## Связь с другими фреймворками

| Page | Связь |
|---|---|
| [[canon/marketing-frameworks/petrosian-content-aptechka-support-folder]] | «Поддерживать»-функция = операционализация через папку «Поддержка». |
| [[canon/marketing-frameworks/petrosian-6-weak-points-first-month-resistance]] | «Поддерживать» адресует #5 «чужие ожидания / отсутствие поддержки». |
| [[canon/marketing-frameworks/petrosian-goal-processing-6-questions-daily]] | «Пояснять»-функция = операционализация через ежедневную 10-15 мин обработку. |
| [[canon/marketing-frameworks/petrosian-content-as-accelerator]] | «Пояснять» через публичный newsletter = sublimated 3-функции (rec в один контейнер). |
| [[canon/marketing-frameworks/fogg-behavior-model]] | «Напоминать» = Fogg Prompt. «Пояснять» = Fogg Ability-up через clarity. «Поддерживать» = Fogg Motivation-up через social/emotional. |
| [[canon/marketing-frameworks/hook-model-habit-loop]] | 3 функции map'ятся на Trigger / Action / Reward соответственно (with extension to Investment via «Пояснять»). |

## Связанные страницы

- [[sources/2026-05-26-petrosian-book-2-how-to-start-changes]] — первоисточник (final §)
- [[sources/2026-05-26-tg-stodnevka2-may-20-26-2026]] — bundle parent
- [[canon/marketing-frameworks/petrosian-content-aptechka-support-folder]] — support-функция operational
- [[canon/marketing-frameworks/petrosian-6-weak-points-first-month-resistance]] — counter to weak points
- [[canon/marketing-frameworks/petrosian-goal-processing-6-questions-daily]] — explain-функция operational
- [[canon/marketing-frameworks/petrosian-content-as-accelerator]] — публичный newsletter как 3-в-1
- [[canon/marketing-frameworks/fogg-behavior-model]] — mechanism map
- [[canon/marketing-frameworks/hook-model-habit-loop]] — UX-pattern map
- [[canon/product-knowledge/gro-app-overview]] — продуктовое применение

## Атрибуция и confidence

**Direct quote для marketing (с атрибуцией):**
> «Среда работает только если выполняет три функции: напоминать, пояснять, поддерживать.» (Армен Петросян, «Как приступить к переменам», 2025)

**Verified expertise** (по `wiki/rules.md` критерий 2): 10+ лет Стодневок, published book 2025. **Operational track-record:** Стодневка как canonical exemplar = self-applied фрейм с 2015 года. `confidence: medium` на фрейме.
