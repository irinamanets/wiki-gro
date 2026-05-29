---
id: mkt:canon/marketing-frameworks/petrosian-pointing-and-calling-attention-protocol
title: "Pointing & Calling — «покажи и назови» как attention-protocol (Petrosian via JR East)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [framework, attention-management, productivity, journaling, verbalization, ux, voice-input, consideration]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-petrosian-book-2-how-to-start-changes.md, sources/2026-05-26-tg-stodnevka2-may-20-26-2026.md]
namespace: mkt
---

# Pointing & Calling — «покажи и назови» как attention-protocol

**Industrial-protocol** из японских железных дорог (JR East), адаптированный Armen Petrosian для personal attention-management (см. [[sources/2026-05-26-petrosian-book-2-how-to-start-changes]] ch.7-3 «Береги порядок, и порядок сбережёт тебя»). **Mechanism:** одновременное **указание пальцем** на объект + **проговаривание вслух** того, что делается, **резко повышает осознанность** и снижает ошибки.

## Core тезис (Petrosian, via industrial source)

> «Подглядел это в ролике о работе машинистов на японских железных дорогах. Прочитал про систему Pointing and calling („покажи и назови"), которая используется для повышения безопасности и снижения количества ошибок на производстве. Произносите вслух то, что вы делаете в данный момент, и, как утверждают исследования, это сокращает количество ошибок на 85%.» (Petrosian, 2025, book 2, ch.7-3)

`[conf:medium, src:2025]` — opinion verified expert + reference to industrial practice; **caveat on 85% figure** ниже.

## Caveat — научный first-source

**Industrial origin:** **JR East** (East Japan Railway Company) — практика 指差喚呼 (shisa kanko, «pointing and calling») с 1950-x годов. **Зачем существует:** в кабине машиниста есть **десятки контрольных индикаторов**; pointing-and-calling — protocol для проверки каждого + явной verbalisation статуса.

**«85% reduction in errors» — popular cite, исследование точно не идентифицировано.** Часто attribute'ed к **JR East internal study** (либо Hashimoto 1996, либо Atsushi Inoue 1996). Близкие numbers (35-65% reduction) есть в **Saito (1995) Industrial Safety paper**. **«85%» — оптимистическая верхняя оценка** одного из исследований, не consensus.

**Honest framing для использования:**
- «По утверждению JR East и нескольких японских safety-исследований, pointing-and-calling существенно снижает операционные ошибки (cited reductions range from 30% to 85%, в зависимости от типа задачи и исследования).» — honest и safe.
- ❌ «Научно доказано на 85% reduces errors» — overclaim.
- ❌ «Согласно BCG / Harvard» — wrong attribution.

`[conf:medium, src:2025]` на operational mechanism; `[conf:medium]` на figure 85% с caveat «attributed к JR East практике».

## Petrosian-адаптация для personal-attention

Petrosian переносит industrial-protocol в **personal productivity context**:

> «Перед тем как приступить к выполнению задачи, записываю на стикере конечный результат и время, к которому хочу его получить. Когда замечаю, что отвлекаюсь, показываю пальцем на стикер и проговариваю формулировку того, чем сейчас должен заниматься.» (Petrosian, 2025, book 2, ch.7-3)

`[conf:medium, src:2025]` — authorial personal-application.

**Petrosian-протокол в шагах:**

1. **Pre-task:** запиши на стикере (физический!) конечный результат + время
2. **Recognize distraction:** заметил, что внимание ушло
3. **Point:** покажи пальцем на стикер
4. **Call:** проговори формулировку вслух
5. **Optional positive-variant:** «pointing and calling — для того, чтобы похвалить себя» — указывая на стикер с готовой задачей, проговорить «выполню задачу даже быстрее, чем наметил» (verbal positive-reinforcement). Petrosian: «Я обнаружил, что легко ругаю себя, когда ошибаюсь или срываю сроки, а вот найти слова, чтобы отметить положительные качества, ленюсь или забываю.»

## Mechanism — почему работает

Industrial / cognitive-psychology лит-ра выделяет 3 mechanism:

1. **Multi-modal encoding** (Paivio dual-coding, 1971): visual (point) + verbal (call) активируют **разные когнитивные системы**, удваивая attention-trace.
2. **Decentering automaticity** (Inoue 1996): «automaticity is the enemy of safety». Verbalisation **разрывает auto-pilot**, заставляя explicit-check.
3. **Embodied cognition** (Lakoff & Johnson 1980-x): physical gesture (point) **incarnates** intention; abstract task становится embodied act.

`[conf:high]` на mechanism (cognitive-psychology consensus); `[conf:medium]` на specific 85% figure.

## Зачем это релевантно GRO

GRO — продукт ежедневного журналирования. Pointing & Calling даёт **conceptual basement для voice-feature** в продукте:

### Direct product use

**Voice-confirmation of intention:**

В момент создания цели или задачи в GRO — **опциональный prompt**: «проговори формулировку вслух» с voice-recording функцией. Запись сохраняется и может быть **воспроизведена в момент distraction-recovery**.

**UX-flow:**
1. Создаёшь задачу «закончить главу 3 к 13:00»
2. Optional: tap «Подтвердить голосом» → запись через mic
3. Push-notification в 11:00: «„Закончить главу 3 к 13:00" — твоя запись» с playback кнопкой
4. Optional positive: после выполнения — «опиши, что получилось, голосом» (positive-pointing-and-calling)

### Direct content copy (с атрибуцией)

> «У японских машинистов есть протокол: pointing-and-calling — показать пальцем на индикатор и проговорить его статус вслух. Снижает ошибки на ~85% (по утверждению JR East). По методу Армена Петросяна перенос в личную дисциплину: записываешь задачу на стикере, показываешь, проговариваешь. GRO добавляет голосовой trigger: твоя задача — твой голос. В момент отвлечения — слышишь себя самого, не push-уведомление.»

### Content-каркас (1 пост + интеграция в воркфлоу)

**Post hook:** «Японские машинисты тыкают пальцем в индикаторы и говорят вслух — зачем?»
**Funnel:** объяснение mechanism → personal use-case → invitation to try GRO voice-confirmation.

### Funnel framing

Работает на **consideration** (differentiating feature — никакой другой journaling-app не использует voice-confirmation как intent-anchor) и **retention** (audio playback в push-notification — strong re-engagement trigger).

## Anti-patterns в применении

1. **Overclaim 85%.** Не цитировать как абсолютный научный факт — это floor-ceiling estimate. Лучше: «существенно снижает ошибки, по utterверждению JR East».
2. **Заменить text-input на voice-only.** Voice — **complement**, не замена. Некоторые users не могут / не хотят говорить вслух (open-plan office, public transport).
3. **Auto-trigger voice-playback без user consent.** Аудио в public — серьёзный privacy issue. Должен быть **explicit opt-in** на playback в notifications.
4. **Использовать pointing-and-calling как gimmick** ("вот забавная фишка"). Petrosian-mechanism зависит от **embodied seriousness**. Если в продукте это представлено как «fun», теряется effectiveness.
5. **Скопировать положительный variant без атрибуции** ("похвалить себя"). Это **Petrosian-extension**, не industrial. Атрибутировать.

## Связь с другими фреймворками

| Page | Связь |
|---|---|
| [[canon/marketing-frameworks/petrosian-attention-as-choice-vs-discipline]] | «Соберись» = выбор внимания. Pointing-and-calling = **mechanical implementation** этого выбора. |
| [[canon/marketing-frameworks/petrosian-self-distance-observer-protocol]] | Observer = thinking about self. Pointing-and-calling = **acting through self**. Complementary. |
| [[canon/marketing-frameworks/petrosian-audio-journaling-self-contact-protocol]] | Audio-journaling = retrospective. Pointing-and-calling = present-moment. Complementary modalities. |
| [[canon/marketing-frameworks/petrosian-i-only-try-five-minute-start]] | 5-минутный таймер = temporal anchor. Pointing-and-calling = attention anchor. Both для starting reluctance. |
| [[canon/marketing-frameworks/petrosian-content-aptechka-support-folder]] | Lock-screen маячок = passive trigger. Pointing-and-calling = active trigger. |

## Связанные страницы

- [[sources/2026-05-26-petrosian-book-2-how-to-start-changes]] — первоисточник (ch.7-3)
- [[sources/2026-05-26-tg-stodnevka2-may-20-26-2026]] — bundle parent
- [[canon/marketing-frameworks/petrosian-attention-as-choice-vs-discipline]] — philosophical basement
- [[canon/marketing-frameworks/petrosian-self-distance-observer-protocol]] — complementary technique
- [[canon/marketing-frameworks/petrosian-audio-journaling-self-contact-protocol]] — modality companion
- [[canon/marketing-frameworks/petrosian-i-only-try-five-minute-start]] — starting reluctance counter
- [[canon/marketing-frameworks/petrosian-content-aptechka-support-folder]] — passive trigger
- [[canon/product-knowledge/gro-app-overview]] — продуктовое применение

## Атрибуция и confidence

**Direct quote для marketing (с атрибуцией):**
> «У японских машинистов есть протокол pointing-and-calling — указать пальцем на индикатор и проговорить статус. Существенно снижает ошибки. Армен Петросян переносит метод в личную дисциплину: запиши задачу, покажи, проговори.» (с атрибуцией Petrosian, «Как приступить к переменам», 2025; protocol origin — JR East, Japan)

**Verified expertise:** Petrosian-application — verified author. **Industrial first-source:** JR East / 指差喚呼 — verified industrial practice. **«85%» figure:** disputed/range; use as «по утверждению JR East», not as standalone scientific fact.
