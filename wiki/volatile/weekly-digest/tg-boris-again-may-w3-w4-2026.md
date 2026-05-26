---
id: mkt:volatile/weekly-digest/tg-boris-again-may-w3-w4-2026
title: "@boris_again дайджест AI/ML — недели 11–17 и 18–24 мая 2026 (Google I/O + китайский frontier + AI cyber + слоп-юмор)"
type: page
subtype: notes
layer: volatile
theme: weekly-digest
tags: [telegram, ai, ml, weekly-digest, google-io, gemini, qwen, cohere, deepseek, anthropic, ai-cyber, slop, content-pool]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-boris-again-may-19-24-2026.md]
namespace: mkt
---

# @boris_again дайджест AI/ML — недели 11–17 и 18–24 мая 2026

Сводка по двум weekly-дайджестам [@boris_again](https://t.me/boris_again) (посты 3916 и 3918) из [[sources/2026-05-26-tg-boris-again-may-19-24-2026]]. Цель страницы — **content-sourcing pool** для блога / соцсетей GRO. TTL: ~6 недель, потом устойчивые паттерны переезжают в `evolving*` слои, остальное архивируется.

Это **продолжение** [[volatile/weekly-digest/ai-industry-news-w15-w18-2026]] (13 апреля — 4 мая 2026 по `@ai_newz`). По хронологии оба source pool'а покрывают одну общую неделю 11–17 мая, что **усиливает confidence** на пересечениях.

## Tier A — потенциальные hook'ы для GRO-контента

### 1. METR self-vs-measured productivity gap (11 мая)

**Сильнейший contrarian hook 2026.** Разработчики считают себя 3x продуктивнее с агентами, объективные замеры — **1.4–2x**. METR сами **подозревают**, что методология **завышает**. Полная страница: [[evolving-strict/market-data/metr-ai-productivity-self-vs-measured-2026-05]].

**Почему релевантно GRO:** прямой counter-evangelism content. Готовый блог-пост *«AI не делает вас 10x. Делает в 1.4х. И вы себя обманываете»* — CFO-friendly хук с конкретной цифрой `[conf:high, src:2026-05-11]`.

**Action item:** топ приоритет для контент-плана, использовать в комбо с TPS slop ([[evolving/content-trends/tps-slop-tech-metric-template-2026]]).

---

### 2. Google I/O 2026 — двойной анонс (19–20 мая)

**Gemini 3.5 Flash** + **Gemini Omni** — две модели на одной keynote `[conf:high, src:2026-05-19]`. Это **самое значимое событие индустрии за май**. Полные страницы:
- [[volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05]] — 3.5 Flash + Gemini Spark
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] (обновлённая) — Omni официальный анонс с pricing

**Почему релевантно GRO:**
1. **Mid-tier цены сжаты** — Flash $1.50/$9 «сильно дешевле Sonnet» => GRO может опционально мигрировать часть pipeline.
2. **Gemini Spark = клон OpenClaw** — Google входит в agent-first гонку. Прямой контент-hook: «3 вендора, 3 personal agent'а — какой выбрать».
3. **Omni закрывает Veo как отдельную линейку** — confirmed prediction от 11 мая.

**Action item:** связать с [[evolving/industry-trends/agent-first-world-openclaw-2026]] и [[evolving/industry-trends/ai-corporate-race-mar-may-2026]].

---

### 3. Китайский frontier wave (21–24 мая)

**Три китайских релиза за неделю**:
- **Alibaba Qwen 3.7-Max** — frontier для agentic, SWE-bench Pro 60.6, Terminal-Bench 69.7 (лидер), 1M контекст, 35 часов автономной работы. [[volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05]]
- **DeepSeek V4-Pro** — цены в 4 раза вниз навсегда ($0.435/$0.87). [[volatile-strict/competitor-news/deepseek-v4-pro-price-cut-2026-05]]
- **ByteDance Lance** — open multimodal с video-edit. [[volatile-strict/competitor-news/bytedance-lance-open-multimodal-2026-05]]

Контр-нарратив «китайские модели = research-only» **больше не работает** `[conf:high, src:2026-05-24]`.

**Почему релевантно GRO:** **vendor diversification стала технически реальной**. Контент-формат: *«Можно ли построить marketing-stack на Qwen + DeepSeek в 2026?»*

**Action item:** добавить vendor-diversification как **новый под-нарратив** в [[evolving/industry-trends/china-ai-manufacturing-momentum-2026]].

---

### 4. Cohere Command A+ — нативные source-citations (22–24 мая)

Первая открытая фронтир Cohere, 218B MoE (25B активных), 48 языков, **citations как first-class output** `[conf:high, src:2026-05-24]`. [[volatile-strict/competitor-news/cohere-command-a-plus-2026-05]].

**Почему релевантно GRO:** RAG / GEO / AEO продукты ждали нативный citation primitive. Сильный архитектурный signal для contentteam-pipelines.

**Action item:** связать с [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]].

---

### 5. AI cyber 0-day wave (11–15 мая)

Четыре события в одну неделю:
- **Google GTIG**: первая реальная AI 0-day-атака в проде `[conf:high, src:2026-05-17]`
- **Microsoft MDASH**: 100+ агентов нашли «кучу критических уязвимостей» `[conf:high, src:2026-05-12]`
- **UK AISI «Cooling Tower»**: Claude Mythos прошёл симулятор ICS-атаки 3/10 `[conf:medium, src:2026-05-15]`
- **ExploitBench**: Mythos довёл 18/41 уязвимостей до эксплойта, остальные модели — 0 `[conf:medium, src:2026-05-15]`

Полная страница: [[volatile-strict/industry-news/ai-cyber-0day-wave-may-2026]].

**Почему релевантно GRO:** **AI cyber-security = новая product category** с готовым PR-нарративом «defense at AI speed». Можно расширить блог в эту тему как side-cluster.

**Action item:** связать с [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]] (обновляется с production attestation).

---

### 6. GPT-4.5 прошёл Тьюринга (22 мая)

73% участников приняли GPT-4.5 за человека — больше, чем настоящих людей. Первая статистически значимая работа UCSD `[conf:high, src:2026-05-22]`. [[volatile-strict/industry-news/gpt-4-5-statistically-significant-turing-2026-05]].

**Почему релевантно GRO:** прямой удар по AI-detection-tool рынку, прямой стимул к authenticity-positioning. Готовый CTR-хук «AI впервые официально прошёл тест Тьюринга».

**Action item:** связать с [[evolving/content-trends/ai-text-detection-landscape-2026]] и [[evolving/content-trends/anti-ai-positioning-as-brand-asset-2026]].

---

### 7. Artificial Analysis Coding Agent Index запущен (23 мая)

Claude Code 66, Codex 65, Cursor Composer 2.5 62, Gemini CLI 43. Новая категория benchmark'ов: **«агентная система целиком»**, не модель. [[evolving-strict/competitor-metrics/artificial-analysis-coding-agent-index-2026-05]].

**Почему релевантно GRO:** GRO content-team stack-решение пересматривается на основе benchmark'а. Готовый serial-content «AA-index update Q3 2026».

**Action item:** добавить в content-pool как periodic-update формат.

---

### 8. Anthropic Project Glasswing follow-up (21 мая)

Anthropic выпустила отчёт по раздаче Mythos Preview. Нашли **«гору критичных багов, оупенсорс просит котелочек не варить, не успевают латать дыры»** `[conf:medium, src:2026-05-21]`. Это **production-time attestation** Glasswing-инициативы. Backfill: [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]].

**Почему релевантно GRO:** усиливает Anthropic-positioning «Mythos = security frontier model, отдельно от Claude».

---

### 9. Слоп-сатира как канон (24 мая)

Два мема в один день:
- **TPS = Tokens Per Slop** — шаблон tech-метрики + slop-каламбур. [[evolving/content-trends/tps-slop-tech-metric-template-2026]]
- **«нихуя себе / срочно напишите новость»** — мем-template для AI-news flooding. [[evolving/content-trends/ai-news-flooding-meme-template-2026]]

**Почему релевантно GRO:** **готовые шаблоны самосаркастичного контента**, которые сразу можно адаптировать под маркетинговые / HR-метрики.

**Action item:** включить в content-pool как **regular self-aware humor** формат раз в 1–2 недели.

---

## Tier B — backfill в существующие страницы

### B1. ApexGO (UPenn антибиотики) — 14 мая

Байесовская оптимизация молекул антибиотиков, **эффективные на мышах** (Nature) `[conf:high, src:2026-05-14]`. **Биотех + AI** — категория-обещание. Backfill в [[evolving/industry-trends/consumer-biotech-anti-aging-trend-2026]] как «применение AI к открытию лекарств».

### B2. SenseTime SenseNova-U1 — 15 мая

8B мультимодальная модель **без VAE и vision-encoder** на одной RTX 5090 `[conf:medium, src:2026-05-15]`. Архитектурный signal — **архитектурная инновация может ослабить scaling-only нарратив**.

### B3. OpenAI опроверг гипотезу Эрдёша — 22 мая

Внутренней моделью; Гауэрс назвал работу Annals of Mathematics-уровня `[conf:medium, src:2026-05-22]`. **Math research → AI** как новый PR-нарратив OpenAI. Backfill в [[evolving/industry-trends/ai-corporate-race-mar-may-2026]].

### B4. xAI Grok Build — 11–17 мая

**«Очередной Claude Code, но от xAI»** для SuperGrok Heavy `[conf:medium, src:2026-05-17]`. Пятый contender в coding-agent рынке (после Claude Code / Codex / Cursor / Gemini CLI). Скорее всего войдёт в следующий AA-index update.

### B5. SOOHAK math benchmark — 12 мая

439 research-уровень задач, **1 место Gemini-3-Pro 30.4%** `[conf:medium, src:2026-05-12]`. Math-benchmark, добавить в pool benchmarks-page (если создаётся).

### B6. Vercel Zero — agent-native programming language — 17 мая

Experimental язык, **structured JSON-диагностика вместо текстовых ошибок**, **typed repair metadata**, **встроенный toolchain как Agent Skills** (Claude Code / Cursor / Codex). Компилятор self-hosting. **Контент-hook: «эра agent-native languages»**. Связать с [[evolving/industry-trends/agent-first-world-openclaw-2026]].

### B7. AI-pointer (DeepMind) — UX-концепт — 17 мая

Курсор мыши на Gemini, который **понимает на что показывает и зачем**. UX-concept-watch — потенциальный sample для GRO UX-исследований.

### B8. Datadog Toto 2.0 — TSFM — 22 мая

Time series foundation models, 4M–2.5B. **Главный посыл — scaling law работает для time series**. Backfill в [[evolving/industry-trends/ai-personalization-industrial-shift-2026]].

### B9. EVA-Bench, OmniGUI, CHI-Bench, Spreadsheet-RL, OpenComputer

Бенчмарки следующих 3 месяцев. Для каждого — отдельное upcoming событие. Не создаём страницы сейчас, **fold обратно в очередное Tier B**, если в дайджестах появятся implementations.

---

## Tier C — нерелевантно / слабый сигнал

- **3919 NN-мем «этот канал»** — релевантно как content-pattern (Tier A), но фактического content'а нет.
- **3920 TPS slop** — релевантно как content-pattern (Tier A), факт-ноль.
- **MinT (LoRA-постинг)** — узкая research-инфра, не релевантна marketing-audience.
- **Visual Aesthetic Benchmark** — meta-research, не actionable.
- **Anthropic emotion vectors** (не в этом дайджесте, но контекст из [[volatile-strict/competitor-news/anthropic-emotion-vectors-2026-04]]) — research-уровень.

---

## Outgoing content-pipeline (TODO)

| Hook | Format | Channel | Priority |
|---|---|---|---|
| METR self-vs-measured | блог-пост / Twitter thread | groapp.ru/blog + LinkedIn | **высший** |
| Google I/O двойной анонс (Flash+Omni+Spark) | блог-пост + Telegram | groapp.ru/blog + Telegram | высший |
| Китайский frontier wave (Qwen+DeepSeek+ByteDance) | блог-пост | groapp.ru/blog | средний |
| AA Coding Agent Index | serial-content | блог + Telegram | средний |
| TPS slop tech-metric template | self-aware-humor пост | Telegram + Instagram | средний |
| GPT-4.5 Turing | один пост (high-CTR) | LinkedIn + Telegram | высший |
| AI cyber 0-day wave | блог-пост + Twitter | groapp.ru/blog | низкий-средний |
| Cohere Command A+ citations | блог-пост для RAG-аудитории | groapp.ru/blog | низкий |

## Связанные страницы

- [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — primary source
- [[volatile/weekly-digest/ai-industry-news-w15-w18-2026]] — предыдущий pool (`@ai_newz`)
- [[volatile/weekly-digest/ai-news-digest-2026-05-13-19]] — ещё один pool
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий нарратив гонки
- [[evolving/industry-trends/agent-first-world-openclaw-2026]] — agent-first нарратив
- [[evolving/industry-trends/china-ai-manufacturing-momentum-2026]] — китайский momentum
