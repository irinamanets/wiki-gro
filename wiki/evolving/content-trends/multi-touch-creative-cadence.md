---
id: mkt:evolving/content-trends/multi-touch-creative-cadence
title: "Multi-touch creative cadence — two-wave strategy для running campaigns в TG"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [content, telegram, creative-reference, campaign-cadence, t-bank, multi-touch, reminder-creative]
confidence: medium
stale: false
created: 2026-04-17
updated: 2026-04-17  # +immediate-stacking pattern: #10545 video-teaser → #10546 thumbnail как back-to-back touch pair внутри одного episode-launch'а (branded-show Star-vs-Fraud). Отличается от spaced-repetition — complementary tactic
sources: [sources/2026-04-14-tg-tinkoffbank-10557-daily-cashback-streak.md, sources/2026-04-14-tg-tinkoffbank-10572-cashback-100-typographic.md, sources/2026-04-17-tg-tinkoffbank-10545-satir-meter-scam-teaser.md, sources/2026-04-14-tg-tinkoffbank-10546-stars-vs-fraudsters.md]
namespace: mkt
---

# Multi-touch creative cadence

Наблюдаемый паттерн: одна running-кампания получает **несколько разнородных креативов** в Telegram-канале бренда, растянутых во времени. Не reposting одного creative'а, а **fresh creative-formats для одного offer'а** с разной сложностью: первая волна — detailed (учит механику), последующие волны — compressed (напоминают).

Base-кейс — Т-Банк «Кэшбэк 100% каждый день» (апрель 2026): **#10557 detailed phone-hero + #10572 typographic-hero** в одной campaign window до 15 апреля, с gap ~5 постов между creative'ами ([[sources/2026-04-14-tg-tinkoffbank-10557-daily-cashback-streak]], [[sources/2026-04-14-tg-tinkoffbank-10572-cashback-100-typographic]]). `[conf:high, src:2026-04-14]`

## Анатомия паттерна

**Структурные требования:**

1. **Running campaign с deadline** — кампания работает через window (до X даты), а не one-shot event.
2. **Fresh creative-formats** — не reposting одного image, а новый дизайн в рамках brand-consistency.
3. **Spacing между креативами** — 3–7 постов gap (в TG feed это ~1–3 дня). Обеспечивает **non-overload** user'а, но reminder функционирует.
4. **Visual-continuity markers** — общий элемент в креативах (иконка, палитра, gradient), чтобы user подсознательно связывал creative'ы как one-campaign.
5. **Декрещивание сложности от wave к wave** — first wave детальная (ML/explain), subsequent — compressed (remind/trigger).

**Отсутствующие в paradigm'е:**
- Не требуются одинаковые landing-ссылки (могут быть разные UTM для attribution, но **endpoint одинаковый**).
- Не требуются одинаковые captions (caption может варьироваться — humor style в one caption, pragmatic в другой).

## Почему это работает в TG

1. **Channel-feed-фатиг.** TG-user скроллит много channels, и **repost того же креатива** вызывает «blindness» через 24 часа. Fresh creative в рамках одной кампании **повторно привлекает внимание** — это ещё одно ad-slot, но с **same offer payoff**.
2. **Дифференциация по audience-segments.** Detailed creative (#10557) убеждает users, **кто ещё не знает о фиче**. Compressed creative (#10572) триггерит users, **кто уже понял механику, но ещё не активировал**. Разные copies для разных stages funnel'а внутри одного campaign'а.
3. **Campaign-runway optimization.** Дедлайн «до 15 апреля» = ~2 недели running window. Одно creative per campaign — недоиспользование окна. Две-три creative-waves позволяют **fill up runway** без увеличения bet (single-creative assumption loses 50% impressions в день запуска).
4. **Testing без explicit A/B.** De-facto #10557 vs #10572 — это **natural A/B**: сравнение CTR показывает, detailed vs compressed работает лучше. Internal analytics могут использовать это для future-optimization.

## Observed cadence в T-Bank ingest'ах

Из наблюдаемой подборки (10537–10583) вырисовывается implicit-pattern:

| Гипотеза | Признак | Данные |
|---|---|---|
| **Major launches** получают **1 detailed creative** | Сделка (#10544), ВЗР POLETELI (#10537) | Пока видно только first-wave. Later-wave может ещё появиться. |
| **Running offers с deadline** получают **multi-touch** | Кэшбэк 100% (#10557 + #10572) | 2 creative'а в 1 campaign window `[conf:high, src:2026-04-14]` — подтверждено |
| **Brand-awareness content** (speaker lineup, Tolk.PRO) не получает multi-touch | Tolk.PRO (#10539–10543) | Единая creative-серия в карусели |
| **Cross-promo / партнёрства** получают **1 detailed** | GAC×T-Premium (#10547), Utair×Т-Путешествия (#10567) | Single creative per partnership-drop |

**Tentative inference:** T-Bank reserves multi-touch-cadence **specifically для running offers** (cashback-акции, window-deadline промо). Brand-content и partnerships — single-wave. Это **discipline**, не randomness: campaign-тип → creative-pattern.

## Сравнение first wave vs second wave

Разборка #10557 vs #10572:

| Характеристика | #10557 (first wave) | #10572 (second wave) |
|---|---|---|
| **Hero-object** | 3D-смартфон с mini-calendar UI | Нет product-object; 3D «100%» типографика |
| **Visual complexity** | Высокая (phone + calendar-strip + crown + 5 day-tiles) | Низкая (только headline + цифра + crown) |
| **Educational content** | Явное: mini-calendar показывает механику streak | Отсутствует: assumed-knowledge |
| **Brand-anchor (crown)** | Embedded в calendar (одна из иконок) | Hero-feature (отдельный medallion) |
| **Subhead-fokus** | «До 15 апреля» (urgency) | «В разделе „Кэшбэк дня"» (action) |
| **Caption-tone** | Explanatory (safety-board meme «0 дней без X») | Word-play («вероятность 100% равна 100%») |
| **Assumed user-state** | «Не знает о фиче» | «Слышал, не активировал» |

Это **textbook first-wave vs reminder-wave** diff: explain vs trigger.

## Ограничения

1. **Требует creative-production bandwidth.** Два creative'а = два дизайна. Не все бренды имеют in-house-studio для этого. Т-Банк имеет.
2. **Short campaign windows** менее подходят — если window 3 дня, second-wave overlap'нет first-wave. Нужен минимум ~10 дней для двух волн.
3. **Regulatory-re-compliance.** Каждый new creative для financial-продукта должен проходить ЦБ РФ approval. Scaling multi-touch увеличивает compliance-overhead. Т-Банк имеет internal-compliance-flow, но smaller banks — не всегда.
4. **Brand-consistency риск.** Второе creative может drift-нуть от brand-language, вызывая «неуверенность» у user'а («тот ли это банк?»). Решение: **visual-anchor** (в T-Bank это iridescent crown + yellow-fon).

## Переносимость на GRO

1. **GRO seasonal campaigns** (new-year challenge, summer-body, quarterly-streak). Running window 2–4 недели — подходит для multi-touch cadence.
2. **Feature-launch → reminder-iteration** — first-wave educational (показ UI-demo), second-wave assumed-knowledge (minimal visual, CTA-focused). Типичный product-marketing paradigm.
3. **Visual-anchor discipline.** GRO должно определить **устойчивый brand-anchor** (иконку, декоративный element), который переносится через все creative-iteration'ы кампании. У T-Bank это iridescent crown. У GRO — может быть streak-symbol, achievement-badge, lifecycle-icon.
4. **Cadence-spacing calibration.** TG-channel T-Банка публикует ~2–3 поста/день → gap в 5 постов = ~2 дня. Для GRO с другой post-frequency нужно калибровать spacing пропорционально (в channel'е с 1 постом/3 дня — gap ~15 дней, что может слишком долго).

## Immediate-stacking tactic — complementary pattern (branded-show launch)

Помимо **spaced-repetition** (running campaign с gap 5–7 постов между creative-waves, кейс Кэшбэк 100%), обнаружена **immediate-stacking** tactic — два разнородных creative-touch'а публикуются **back-to-back** в рамках одного episode-launch'а, без gap'а.

Base-кейс — branded-show «Звёзды против мошенников», episode 1 (Сатир):

| Touch | Тип | Функция | Caption-тон |
|---|---|---|---|
| [#10545](https://t.me/tinkoffbank/10545) | 42-сек **video-клип** из эпизода (peak emotional moment, Сатир в reenactment «пломба-скама») | Эмоциональный prime, cliffhanger **без CTA** | Genre-parody listicle «Как довести Илью Сатира до слёз» |
| [#10546](https://t.me/tinkoffbank/10546) | Static **thumbnail image** + полный caption с up-sell lattice | Логистика просмотра, CTA-stack (YT/VK → T-Refund → Защита близких → sweepstake) | Explanatory + conversion-focused |

Посты идут **consecutive** в нумерации канала ([[sources/2026-04-17-tg-tinkoffbank-10545-satir-meter-scam-teaser]], [[sources/2026-04-14-tg-tinkoffbank-10546-stars-vs-fraudsters]]). `[conf:high, src:2026-04-14]`

**Отличие от spaced-repetition:**

| Характеристика | Spaced-repetition (Кэшбэк 100%) | Immediate-stacking (Satir teaser) |
|---|---|---|
| **Gap между touch'ами** | 5–7 постов (~2 дня) | 0–1 пост (minuts/часы) |
| **Тип campaign'а** | Running offer с window-deadline (2 недели) | Episode-launch (one-off для одного эпизода) |
| **Роль первого touch'а** | Educational (explain механику) | Emotional prime (без CTA) |
| **Роль второго touch'а** | Compressed reminder (активирует уже понявших) | Logistics + conversion (CTA-stack) |
| **User-journey** | Одиночный user может видеть только один touch → каждый must stand alone | User видит оба back-to-back → они **work as pair** |

Immediate-stacking обеспечивает **priming-эффект**: user, который посмотрел tease video, приходит к thumbnail'у **уже с emotional stake'ом**, что повышает CTR thumbnail'а. Spaced-repetition же рассчитан на **разные user-state'ы** (незнающие и знающие уже узнали).

**Tentative-inference:** оба паттерна — формы multi-touch. Выбор между ними зависит от:
- **Single-episode** / **recurring offer** → immediate / spaced.
- **Pull-hook через emotion** / **push-CTA через urgency** → immediate / spaced.
- **Short-form video доступен** / **только static creative** → immediate выигрывает, когда есть video-content.

Полный анализ teaser-pattern'а — [[evolving/content-trends/short-form-teaser-for-branded-show]].

## Gap и неизвестные

- **Third-wave?** Не наблюдалось в подборке. Возможно, T-Bank практикует two-wave (not three) для 2-недельного window. Для 3–4-недельного window возможно третья компрессия.
- **Conversion-analytics** между first и second wave не публична. Нет data о том, какая wave реально драйвит large-share activations.
- **Как decide'ить creative-format first vs second?** Detailed phone-hero vs typographic-only — **T-Bank-specific выбор**. Другие бренды могут сделать inverted (typography first, product later). Что лучше — needs testing.
- **Third-party campaigns получают multi-touch?** Не ясно. #10547 GAC×T-Premium — пока single-wave. Возможно, partnership-deadlines structurally shorter → не подходят для multi-touch.

## Связанные страницы

- [[sources/2026-04-14-tg-tinkoffbank-10557-daily-cashback-streak]] — first-wave detailed creative (spaced-repetition pattern)
- [[sources/2026-04-14-tg-tinkoffbank-10572-cashback-100-typographic]] — second-wave compressed creative (spaced-repetition pattern)
- [[sources/2026-04-17-tg-tinkoffbank-10545-satir-meter-scam-teaser]] — video-тизер (immediate-stacking pattern, part 1)
- [[sources/2026-04-14-tg-tinkoffbank-10546-stars-vs-fraudsters]] — main thumbnail (immediate-stacking pattern, part 2)
- [[evolving/content-trends/short-form-teaser-for-branded-show]] — launch-tactic для serialized branded-show (pair teaser + thumbnail)
- [[evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay]] — визуальный протокол, из которого две волны берут свои варианты
- [[evolving/content-trends/daily-streak-gamification-in-finance]] — gamification паттерн, продвигаемый этой многотачевой кампанией
- [[evolving/content-trends/telegram-native-formats]] — общий контекст TG-форматов
- [[evolving/content-trends/urgency-window-launch-playbook]] — другой паттерн cadence (launch-window, 5 фаз)
- [[evolving/content-trends/safety-board-meme-inversion-hook]] — caption-формат в first-wave

## Backlinks

_8 pages link to this one._

- [[canon/marketing-frameworks/multichannel-cumulative-effect]]
- [[evolving/content-trends/daily-streak-gamification-in-finance]]
- [[evolving/content-trends/short-form-teaser-for-branded-show]]
- [[index]]
- [[sources/2026-04-14-tg-tinkoffbank-10557-daily-cashback-streak]]
- [[sources/2026-04-14-tg-tinkoffbank-10572-cashback-100-typographic]]
- [[sources/2026-04-14-tg-tinkoffbank-10575-egg-cashback-olive]]
- [[sources/2026-04-17-tg-tinkoffbank-10545-satir-meter-scam-teaser]]
