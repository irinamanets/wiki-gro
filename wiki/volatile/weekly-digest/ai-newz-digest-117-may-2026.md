---
id: mkt:volatile/weekly-digest/ai-newz-digest-117-may-2026
title: "@ai_newz Нейродайджест #117 (4-24 мая 2026) — мета-карта 3 недель AI"
type: page
subtype: notes
layer: volatile
theme: weekly-digest
tags: [ai, digest, telegram, ai-newz, llm, generative, anthropic, openai, claude, codex]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-ai-newz-may-19-25-2026.md]
namespace: mkt
---

# Нейродайджест #117 — мета-карта 3 недель AI (4-24 мая 2026)

**Источник:** пост 4590 в [[sources/2026-05-26-tg-ai-newz-may-19-25-2026|@ai_newz]] от 25.05.2026. **Жанр:** мета-дайджест автора канала. **Уникальная характеристика этого выпуска:** автор перечёркивает «**неделю**» → пишет «**3 недели**» — сигнал, что **темп индустрии превышает скорость недельных дайджестов**, форматы переходят на 2-3-недельные циклы. `[conf:high, src:2026-05-25]`

**TTL:** 14 дней после `created` → `stale: true` 2026-06-09. После — записи, подтверждённые первичными источниками, мигрируют в `evolving-strict/*` или удаляются.

## Структура дайджеста

27 пунктов в 4 секциях:
- **LLM** (9 пунктов)
- **Генеративные модели** (1 пункт)
- **Прочее** (6 пунктов)
- **Личное** (2 пункта)

Каждая запись содержит ссылку на оригинальный пост канала (формат `t.me/ai_newz/<id>`). Большинство уже зафиксировано как отдельные страницы в `volatile-strict/*` — это **second-source attestation для already-tracked сигналов**.

## Уже зафиксированные (re-attestation)

### LLM
- **GPT Instant 5.5 (4560)** → [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|ai-model-releases-mar-apr-2026.md]] раздел Update 2026-05-14. Подтверждение: «Модель поумнела, а в ChatGPT обновили интерфейс памяти, чтобы было понятно, на что опирается ответ».
- **Mythos порвал разработчиков Firefox (4562)** → [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]] + [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|main page Mythos Firefox section]]. Подтверждение: «Модель Mythos от Anthropic за месяц нашла 271 уязвимость (включая критические), обойдя результаты людей за полтора года».
- **Управление роем агентов и режим /goal (4569)** → новый сигнал, см. ниже.
- **Бесплатные API-кредиты для сторонних приложений (4571)** → [[volatile-strict/competitor-news/anthropic-third-party-credits-2026-06]]. Подтверждение: «Anthropic будет насыпать подписчикам токены (до $200) для использования в сторонних тулах на базе Agent SDK».
- **Приговор для TurboQuant на серверах (4574)** → нерелевантно для marketing-memory (deep ML-infra), audit-only.
- **Первая модель из датацентров SpaceX (4580)** → [[volatile-strict/competitor-news/cursor-composer-2-5-2026-05]]. Подтверждение: «Cursor выпустили Composer 2.5 на базе K2.5. Модель стала умнее, но стоимость fast-режима выросла вдвое (до уровня Sonnet)».
- **Gemini 3.5 Flash написала свою ОС за 12 часов (4583)** → [[volatile-strict/competitor-news/google-gemini-3-5-flash-2026-05]]. Подтверждение: «Вышла Gemini 3.5 Flash с сильным упором на агентность. Модель заметно умнее, но цены выросли в 3 раза по сравнению с прошлой версией».
- **Тысяча токенов в секунду на триллионнике (4587)** → [[volatile-strict/competitor-news/cerebras-kimi-k26-1000tps-2026-05]]. Подтверждение: «Cerebras (которые только что вышли на IPO) запустили Kimi K2.6 с безумной скоростью, пока только для энтерпрайз-клиентов».
- **Ремонт кэша и тизер новых фич (4588)** → [[volatile-strict/competitor-news/openai-codex-cache-fix-slow-mode-2026-05]]. Подтверждение: «OpenAI пофиксили баг с выжиранием лимитов в Codex и тизерят режим /slow для объёмных несрочных задач».

### Генеративные модели
- **Смерть линейки Veo (4564)** → [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]]. Подтверждение: «Google выпустила Gemini Omni. Модель теперь сама умеет в видеогенерацию».

### Прочее
- **Маск и Anthropic теперь партнеры (4561)** → [[volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05]]. Подтверждение: «Anthropic арендует датацентр Colossus у SpaceX. В ответ Клоду вдвое подняли лимиты для подписчиков».
- **Настоящая меха за $650k (4566)** → нерелевантно для marketing-memory (robotics demo).
- **Анекдот про обезьяну и скейлинг лоуз (4567)** → нерелевантно (юмор).
- **Миграция с Zig на Rust за 10 дней (4572)** → [[volatile-strict/industry-news/anthropic-bun-rust-rewrite-2026-05]]. Подтверждение: «Лид-разработчик Bun полностью переписал рантайм при помощи Claude. Новая версия стабильнее и быстрее».
- **Счёт за токены на $1.3 млн в месяц (4576)** → существующий fix (см. предыдущий дамп этого канала, [[sources/2026-05-19-tg-ai-newz-may-14-19-2026]]).
- **Арендовать H100 почти нереально (4579)** → [[volatile-strict/industry-news/gpu-scarcity-neocloud-anthropic-2026-05]]. Подтверждение: «В мире заканчиваются GPU. Старые A100 стоят дороже, чем два года назад, а неоклауды отдают всё крупным игрокам».
- **Андрей Карпатый вышел с вольных хлебов (4582)** → [[volatile-strict/competitor-news/anthropic-karpathy-join-2026-05]]. Подтверждение: «Легендарный ресерчер поддался FOMO и официально присоединился к Anthropic».

### Личное
- **Голосовухи от рекрутеров в LinkedIn (4577)** → нерелевантно (anecdotal).
- **Как попасть в топовую AI-лабу или стартап (4585)** → [[canon/marketing-frameworks/frontier-lab-vs-startup-career-tradeoff]]. Подтверждение: «Мои мысли о карьерном пути в frontier-лабы и почему стартапы (как наш) часто дают больше ownership и пространства для быстрого роста».

## Новый сигнал — Claude Code /goal mode (post 4569)

В дайджесте упоминается **пост 4569**, который **не входил в текущий дамп** (4581-4590), но trackается через дайджест-резюме:

**«Управление роем агентов и режим /goal — В Claude Code завезли мульти-агентный режим и слизали фичу Codex, где модель не останавливается до достижения цели.»** `[conf:medium, src:2026-05-25]`

**Что это значит:**

1. **Anthropic /goal copies OpenAI Codex /slow-style continuous-mode** — то есть **обе coding-platforms нацелены на «не останавливайся пока не достигнешь цели»**. Это **convergent feature war** между Codex и Claude Code.
2. **Мульти-агентность в Claude Code** — Claude Code теперь поддерживает **рой агентов** (multiple agents в одной сессии, координированных). Похоже на **внутреннюю реализацию Multi-Agent Pattern** (см. [[volatile-strict/competitor-news/anthropic-claude-managed-agents-2026-04|Claude Managed Agents]]) на client-уровне.
3. **Конкурентная динамика** (Claude vs Codex):
   - **Codex /slow** (24 мая, tease) — batch-mode «возьми задачу когда есть ресурсы».
   - **Claude /goal** (≈ start мая) — continuous-until-done.
   - Они **не идентичны**, но обе под одной зонтичной идеей **«AI-coder работает дольше человеческого attention span»**.

**Сигнал для GRO нарратива:** **рой агентов** становится **client-side feature**, не enterprise-API. То есть **individual developers получают доступ к agent-swarm**, который раньше требовал custom-build. Это **сильный signal** для нарратива «AI tooling commoditizes capabilities, которые год назад были enterprise-only».

## Что значит дайджест целиком (мета-уровень)

**1. Темп = 3 недели как «новая неделя».**

Автор перечёркивает «неделю» → «3 недели». **Сигнал**: темп индустрии превышает скорость недельных дайджестов, контент-форматы переходят на 2-3-недельные циклы. Сравнить с [[sources/2026-05-19-tg-ai-newz-may-14-19-2026|предыдущим дампом ai_newz]] (14-19 мая, недельный) и **этим дампом** (19-25 мая + дайджест #117 за 4-24 мая) — **новые дайджесты охватывают всё более длинные окна**.

**Маркетинговая релевантность для GRO:** content-стратегия должна **переориентироваться с weekly на bi-weekly или tri-weekly cycle'ы**. Newsletter-формат «раз в неделю» в AI-доменах перестаёт работать — слишком много событий между выпусками. **Подтверждение тренда** из [[evolving/content-trends/community-monthly-recap-digest-format-2026|community-monthly-recap-digest формата]] — там же доминирование месячных recap'ов как форматов.

**2. Anthropic-doмiнирование в LLM-секции.**

Из 9 LLM-пунктов:
- **6 про Anthropic-stack** (Mythos, Claude Code /goal, third-party credits, Karpathy join, GPU scarcity backdrop с Anthropic-anchor'ом, Bun Rust rewrite).
- **2 про OpenAI** (GPT-5.5 Instant memory UX, Codex cache fix + /slow tease).
- **1 про Google** (Gemini 3.5 Flash).

**Маркетинговая интерпретация:** в восприятии ML-twitter (proxy для AI-aud сегмента) **Anthropic является main story** мая 2026. Это **anchor для positioning** при выборе frontiers для контент-нарратива GRO.

**3. Generative модели — только Google.**

Единственный пункт в секции «Генеративные модели» — про Gemini Omni / смерть Veo. **Это значит**: остальные generative-фронты (image, video, voice, music) либо в paused-state, либо вне фокуса ML-канала @ai_newz. Сравнить с [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|releases-mar-apr]] добавлением W19 — там OpenAI выпустил 3 voice-модели, но в digest #117 это не попало.

**Это означает:** **digest каналов селективен** — нельзя использовать как полный proxy для индустрии, но можно как **proxy для viral attention внутри ML-community**.

## Связанные страницы

- [[sources/2026-05-26-tg-ai-newz-may-19-25-2026]] — первоисточник
- [[volatile-strict/competitor-news/anthropic-karpathy-join-2026-05]]
- [[volatile-strict/competitor-news/google-gemini-3-5-flash-2026-05]]
- [[volatile-strict/competitor-news/openai-codex-cache-fix-slow-mode-2026-05]]
- [[volatile-strict/competitor-news/cerebras-kimi-k26-1000tps-2026-05]]
- [[volatile-strict/industry-news/cerebras-ipo-2026-05]]
- [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]]
- [[volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05]]
- [[volatile-strict/competitor-news/anthropic-third-party-credits-2026-06]]
- [[volatile-strict/competitor-news/cursor-composer-2-5-2026-05]]
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]]
- [[volatile-strict/industry-news/anthropic-bun-rust-rewrite-2026-05]]
- [[volatile-strict/industry-news/gpu-scarcity-neocloud-anthropic-2026-05]]
- [[canon/marketing-frameworks/frontier-lab-vs-startup-career-tradeoff]]
- [[evolving/content-trends/community-monthly-recap-digest-format-2026]]
- [[sources/2026-05-19-tg-ai-newz-may-14-19-2026]] — предыдущий дамп этого же канала
