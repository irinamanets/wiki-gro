---
id: mkt:evolving/content-trends/expert-pair-webinar-leadmagnet-pattern-krylov
title: "Expert-pair webinar lead-magnet funnel — 4-touch pattern (Krylov × Мерзликин Sleeptery)"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [content, telegram, author-channel, webinar, lead-magnet, funnel, co-host, distribution, notebooklm, krylov]
confidence: medium
stale: false
created: 2026-05-28
updated: 2026-05-28
sources: [sources/2026-05-26-tg-howtomake10x-may-20-26-2026.md]
namespace: mkt
---

# Expert-pair webinar lead-magnet funnel — 4-touch pattern

**Тезис.** Author-канал (Krylov-type, founder-led) + adjacent-founder-эксперт (Мерзликин/Sleeptery-type) запускают **совместный live-эфир** через **4-touch lead-magnet funnel** в канале: D-1 teaser → D-0 live → D+1 recap + памятка. Это **reusable distribution-template** для author-каналов с consulting/community-монетизацией и для founder'ов SaaS-продуктов в той же ICP.

**Зафиксировано на:** Krylov × Мерзликин (Sleeptery) эфире 21 мая 2026, посты 1573–1576 на @howtomake10x. См. [[sources/2026-05-26-tg-howtomake10x-may-20-26-2026]].

**Почему `evolving/content-trends`:** это **наблюдаемый контент-паттерн** RU-2026, не canonical webinar-methodology. Дрейфует с эволюцией channel-funnel-практик и AI-tooling'а (NotebookLM как recap-генератор — 2026-specific tool). Подтверждается на этом срезе; нужен 2-3 проверочных observation на других author-каналах для upgrade в `canon`.

## Полная архитектура funnel'а

```
                                          ←—— ASSETS PASSED OVER ——→
                                          
D-1 (2026-05-20):     [Teaser]          ← обложка-пара + bio + CTA
            ↓                              "Регистрируемся" → бот
            
D-0 (2026-05-21):     [Live launch]     ← video-привет (mp4)
            ↓                              + reminder скрин с live-link
            
D-0 (2026-05-21):     [Live reminder]   ← скрин live-комнаты + прямая ссылка
            ↓                              vitalykrylov.com/efir (last-mile)
            
D+1 (2026-05-22):     [Recap+памятка]   ← обложка "СОН: ПЕРЕСБОРКА"
                                          + CTA на бот для записи+памятки
                                          (NotebookLM-generated)
```

## Detailed breakdown по touch'ам

### Touch 1: D-1 Teaser (пост 1573, 2026-05-20 10:04 UTC)

**Контент-компоненты:**
- **Header-обложка** (1280×720, dark theme) — два говорящих лица крупным планом (founder продукта + co-host), стилизованный мобильный девайс в фоне, заголовок «**СОЗВОНЫ**», bio спикера, value-line, дата+время. Образец промо-обложки для co-host эфира.
- **Текстовый payload** — раскрытие bio спикера + value-proposition:
  ```
  Александр — предприниматель с 8-летним стажем, фаундер Sleeptery
  и человек, который продал SaaS-платформу «Таксиагрегатор» за 700 млн рублей
  платёжной системе QIWI.

  Но поговорим не про сделки. Поговорим про сон.
  ```
- **Bridge от topic к pain (через первое лицо хоста):**
  ```
  Когда ты постоянно нанимаешь людей, оцениваешь риски и принимаешь решения
  в неопределённости — даже лёгкий недосып начинает бить по качеству мышления.
  ```
- **Reframe / new-frame:** «Сон — это не отдых. Это качество твоих решений.»
- **Operational-promise:** «можно научиться — маленькими шагами, триггеры, привычки.»
- **CTA с urgency:** «Завтра, 17:00. Ставьте напоминание 🔥»
- **Lead-capture URL:** `t.me/howtomake_10x_bot?start=sozvon_tg` — link с UTM-параметром в start-payload.

**Mechanic:**
- **Founder-pair credibility** — оба персонажа имеют exit-track-record, audience доверяет.
- **Specific date + specific value** — снижает «может посмотрю запись» процент.
- **Bot-funnel вместо просто-comment** — все registrations capt'ятся в lead-database Krylov'а.

### Touch 2: D-0 Live launch (пост 1574, 2026-05-21 12:16 UTC)

**Контент:** короткий video (mp4, 4.4 MB) — судя по контексту, video-привет накануне эфира («Стартуем эфир!»).

**Mechanic:**
- Reminder для registered audience (FOMO-trigger «эфир скоро начинается»).
- Reminder для new readers, пропустивших D-1 teaser.
- Video format раскрывает «человеческий» face — увеличивает trust и conversion.

(В нашем срезе video находится в `raw/failed/video/` — транскрипция провалилась; контент-восстановить можно только по контексту.)

### Touch 3: D-0 Live reminder (пост 1575, 2026-05-21 13:57 UTC, 1ч 41мин после launch'а)

**Контент:** screenshot live-комнаты с двумя видео-окнами:
- Top-right: Krylov (с заметным «Vitaly Krylov» подписью) — в машине, кудри
- Main frame: Мерзликин в жёлтой футболке-поло на фоне tropical-фона (виртуальный)
- Подпись «Александр Мерзликин»

**Текстовое тело:** «Стартуем эфир про сон и восстановление! Вот прямая ссылка для подключения: vitalykrylov.com/efir»

**Mechanic — last-mile conversion из «зарегистрировались» в «реально подключились»:**
- Visual proof, что эфир реально идёт сейчас (видны живые faces).
- Прямая ссылка `vitalykrylov.com/efir` (не Yet-Another-Bot) — обходит дополнительный click из бота для нерегистрированных late-comers.
- 1ч 41мин запас — last-second подключения возможны.

### Touch 4: D+1 Recap+памятка (пост 1576, 2026-05-22 14:10 UTC)

**Контент-компоненты:**
- **Recap-обложка** «**СОН: ПЕРЕСБОРКА. Практическая памятка**» — line-art «биомеханическая схема» мозга с подписями (BIOLOGICAL PROCESSOR, NEURAL PATHWAYS, OSCILLATOR UNIT, CIRCADIAN RHYTHM MODULATOR, ENERGY RECOVERY SYSTEM, SINE WAVE GENERATOR — стиль научно-технического чертежа). В правом нижнем углу — **лого NotebookLM** (Google's AI notebook).
- **Текстовое тело:**
  ```
  Друзья, всем добрый вечер!
  Вчера был совершенно бомбовый СОЗВОН про сон и энергию!
  Мы вдохновились и собрали по итогам целую ПАМЯТКУ, про то, как правильно спать
  чтобы максимально восстанавливаться!
  По вот этой ссылке вы сможете получить запись СОЗВОНА и саму памятку!
  Добрых снов!
  PS: киньте огня 🔥 если пойдете забирать материалы)
  ```
- **CTA с double-asset offer:** `t.me/howtomake_10x_bot?start=sozvon_mtrls` — запись (retention asset) + памятка (distributable asset)

**Mechanic — двойной актив:**
- **Запись (retention asset)** — для тех, кто пропустил live или хочет пересмотреть. Lead-magnet с low-touch consumption.
- **Памятка (distributable asset)** — это **AI-generated через NotebookLM** артефакт, который **можно forward'нуть** другому founder'у с тем же pain'ом. **Это inadvertent referral mechanic** — каждый получивший памятку становится potential distribution channel.
- **Engagement-validation:** «киньте огня 🔥» — collect качественную проксу engagement'а + сигнал для алгоритма Telegram.

## NotebookLM как content-tooling: AI-приём в production marketing

В углу обложки памятки (пост 1576) явно видно лого **NotebookLM** — Google's AI notebook product, который позволяет загрузить материалы (в т.ч. транскрипт webinar'а) и сгенерировать summary / artifacts.

Это **proof-point RU-adoption Western AI-tooling'а в production marketing'е**. Krylov / его команда:
1. Записали webinar (T-0 live, 21 мая)
2. Извлекли transcript (через whisper / Yandex SpeechKit / другой STT)
3. Загрузили в NotebookLM
4. Получили structured summary "Памятка"
5. Дизайнили obloжку через AI-image-generation или Canva
6. Опубликовали как T+1 recap

**Cycle time:** D-0 live (17:00 МСК 21 мая) → D+1 recap (14:10 UTC 22 мая) = ~21 час. Это **production-ready cycle** даже с AI-tooling'ом.

Cross-link: [[evolving/industry-trends/ru-geo-aeo-practitioner-playbook-2026]] — про RU AI-toolchain в SMM/PR/контент-маркетинге. NotebookLM здесь — **новый specific tool** для post-webinar artifact'а.

## Funnel-метрики (estimated, not measured)

Реальные числа не публиковались. На основе typical author-channel benchmarks:

| Touch | Expected drop-off | Reasoning |
|---|---|---|
| D-1 teaser views | 100% (baseline = views на posts of @howtomake10x) | Inevitable channel-reach |
| D-1 teaser → бот регистрация | ~3-7% | Standard channel-to-bot conversion |
| Бот registration → D-0 live attendance | ~30-50% | Standard event RSVP-to-show rate |
| D-0 live attendance → D-0 last-mile late-join (через 1575) | +5-15% baseline | Last-minute discovery |
| D+1 recap views | 80-100% baseline | Channel-reach + topic-stickiness |
| D+1 recap → бот «sozvon_mtrls» request | 3-8% | Lead-magnet conversion |
| Total funnel «teaser view → material acquirer» | ~5-15% | Stack-conversion |

`[conf:low, src:2026-05-22]` — все цифры — extrapolation, не measured. Krylov audience size конкретно не публикуется (~50-100k likely range для author-канала ex-CEO Gett).

## Reusable funnel-template для GRO

### Direct application

GRO может реплицировать pattern с founder Лапшиной/Егошиным × adjacent-эксперт:

| Touch | GRO-application |
|---|---|
| **D-1 teaser** | Founder GRO × peer-founder (e.g. founder другого RU productivity SaaS / consultant): обложка-пара + bio + topic + дата + CTA на свой бот |
| **D-0 live launch** | Video-привет в @gro_me с face-time founder'а |
| **D-0 live reminder** | Screenshot live-room с прямой ссылкой на webinar-platform |
| **D+1 recap+памятка** | NotebookLM-generated «Практическая памятка [тема]» + CTA на бот для записи |

### Topic-кандидаты для GRO co-host webinar'ов

1. **GRO × Sleeptery** (если bilateral interest) — direct topic «sleep + journaling = founder decision-quality» — natural complement.
2. **GRO × Markup AI** ([[canon/marketing-frameworks/virtual-advisory-board-ai]]) — «личный advisory board + daily reflection».
3. **GRO × any peer-founder** — «founder routines: 7 утренних, 7 вечерних».
4. **GRO × ex-CEO большого бренда** — «как founder больших бизнесов структурируют свой день».

## Anti-patterns

1. **Без credibility-anchor co-host'а.** Если adjacent-эксперт не имеет own audience и own track-record — funnel не работает (только Krylov-audience напряжена «kто этот человек?»).
2. **D+1 без памятки (только recap-запись).** Без distributable asset funnel не получает inadvertent referrals. **Памятка — must-have**, не nice-to-have.
3. **Bot без deep-link payload'а.** Если CTA — `t.me/bot` без `?start=sozvon_xxx` — нельзя tracking'овать source/touch. Krylov явно использует `?start=sozvon_tg` (D-1) и `?start=sozvon_mtrls` (D+1) — это **operational rigour**.
4. **Live на own-platform без backup ссылки.** Если live идёт только на vitalykrylov.com — late-comers могут не подключиться. Backup ссылка на YouTube Live / Zoom — рекомендуется. (В этом случае Krylov использует свой own-domain landing, что — risk-prone.)
5. **Recap-памятка без NotebookLM-class quality.** Простой text-summary в боте не работает. Нужен **дизайн-обёрнутый artifact**, который не стыдно forward'нуть.
6. **No reactivation reinforcement.** Krylov-pattern не показывает D+7 / D+30 reactivation. Это **gap** — материалы стареют, можно дополнительно репостить через 1-2 недели для new-arrivals аудитории.

## Cross-channel pattern observation

Pattern «co-host webinar + 4-touch funnel» — не уникальный для Krylov, но **operational rigour** (бот с UTM, NotebookLM-памятка, prepared обложки) — образцовый. Параллели:

- **Воронин (Атланты)** — много co-host events, но they go offline-first (см. [[evolving/competitor-positioning/atlanty-business-club-positioning-2026]])
- **Фомичёв (Точно)** — мощная sponsored-content стратегия, но соло-формат (см. [[evolving/content-trends/sponsored-author-channel-monetization-fomichev]])
- **Pressfeed-CEO** — webinar'ы 4D-формата (см. [[sources/2026-05-19-pressfeed-lz-media-speaker-first-event-prep]] и связанные) — но больше B2B-tech-сегмент

Krylov-Мерзликин — **первый замеченный нами кейс полного 4-touch funnel'а с AI-recap-памяткой** в RU author-channel сегменте за май 2026.

## Связанные страницы

- [[sources/2026-05-26-tg-howtomake10x-may-20-26-2026]] — первичный источник (посты 1573–1576)
- [[canon/marketing-frameworks/sleep-as-decision-quality-merzlikin]] — content-payload эфира
- [[evolving/competitor-positioning/sleeptery-sleep-saas-2026]] — adjacent-founder продукт
- [[evolving/content-trends/sponsored-author-channel-monetization-fomichev]] — parallel monetization pattern на author-каналах
- [[evolving/content-trends/telegram-author-channel-patterns]] — broader author-канал-tax
- [[canon/marketing-frameworks/llm-friendly-video-transcription]] — STT-side AI-toolchain
- [[evolving/industry-trends/ru-geo-aeo-practitioner-playbook-2026]] — broader RU AI-toolchain context
- [[canon/marketing-frameworks/ai-text-markers-checklist]] — quality control AI-generated artifacts
- [[canon/target-audience/ru-smb-founder-owner-seller]] — target audience funnel'а
- [[canon/marketing-frameworks/native-advertising]] — related pattern (sponsored content)
