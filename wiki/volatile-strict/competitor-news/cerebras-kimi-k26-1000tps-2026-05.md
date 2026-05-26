---
id: mkt:volatile-strict/competitor-news/cerebras-kimi-k26-1000tps-2026-05
title: "Cerebras × Kimi K2.6 — триллион параметров на 981 t/s (22 мая 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [ai, cerebras, kimi, k26, moonshot, hardware, inference, competitor-news, enterprise]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-ai-newz-may-19-25-2026.md]
namespace: mkt
---

# Cerebras × Kimi K2.6 — триллион параметров на 981 t/s (22 мая 2026)

**Дата сигнала:** 2026-05-22 (пост 4587 в [[sources/2026-05-26-tg-ai-newz-may-19-25-2026|@ai_newz]] + Artificial Analysis диаграмма в media 4587) `[conf:high, src:2026-05-22]`.

## Что произошло

Cerebras запустила **Moonshot Kimi K2.6** (1T параметров) на скорости **981 токенов в секунду** `[conf:high, src:2026-05-22]`. Это **первый случай**, когда триллион-параметровая модель работает на такой скорости — раньше **самой большой моделью у Cerebras был GLM 4.7 на 358B** `[conf:high, src:2026-05-22]`.

**Доступ:** только **энтерпрайз-клиентам** Cerebras Cloud `[conf:high, src:2026-05-22]`. **Не для retail/individual developers** — это **B2B-вертикаль**.

## Бенчмарк-таблица (Artificial Analysis, 10 000 input tokens)

| Provider | Output Tokens / Second | Δ vs Cerebras | Source |
|---|---|---|---|
| **Cerebras** | **981** | baseline (leader) | `[conf:high, src:2026-05-22]` |
| Clarifai | 147 | 6.7× slower | `[conf:high, src:2026-05-22]` |
| Azure | 75 | 13.1× slower | `[conf:high, src:2026-05-22]` |
| Fireworks | 75 | 13.1× slower | `[conf:high, src:2026-05-22]` |
| Cloudflare | 75 | 13.1× slower | `[conf:high, src:2026-05-22]` |
| Weights & Biases | 74 | 13.3× slower | `[conf:high, src:2026-05-22]` |
| Novita | 42 | 23.4× slower | `[conf:high, src:2026-05-22]` |
| SiliconFlow (FP8) | 31 | 31.6× slower | `[conf:high, src:2026-05-22]` |
| Kimi (native) | 31 | 31.6× slower | `[conf:high, src:2026-05-22]` |

**Главный визуальный нарратив диаграммы (media 4587):** **6,7× разрыв Cerebras vs второго места (Clarifai)** — single dominant столбик vs остальные малые столбики.

## Cerebras IPO update (тот же пост)

В том же посте @ai_newz упоминает **post-IPO update**: компания **«вышла на IPO на прошлой неделе, привлекла $5.5 миллиардов и теперь стоит $56 миллиардов»** `[conf:high, src:2026-05-22]`.

**Reconcile с предыдущим фиксацией:** [[volatile-strict/industry-news/cerebras-ipo-2026-05|cerebras-ipo-2026-05]] зафиксировала на 14 мая cap **$40 млрд** (с опционами/варрантами **$49 млрд**). На 22 мая (8 дней после IPO open) cap = **$56 млрд** — **рост $16 млрд (+40%) за неделю**. Это **typical post-IPO float-rally** для hot AI-hardware ticker. **Supersession флоу:** см. секцию ниже + изменения в [[volatile-strict/industry-news/cerebras-ipo-2026-05]]. [conf:low, src:2026-05-26]

## Что значит «1000 t/s на 1T параметров»

**Технически:** для триллион-параметровой модели **981 t/s** — это **рекорд** среди публично доступных провайдеров `[conf:high, src:2026-05-22]`. Для сравнения:
- Kimi native = 31 t/s (то есть **в 31.6× медленнее**, чем на Cerebras).
- Microsoft Azure = 75 t/s.
- Cloudflare AI = 75 t/s.

**Маркетинговая интерпретация:** Cerebras Wafer-Scale Engine (WSE) реально работает как **prime-rate inference accelerator** для frontier-моделей. Раньше CS-3 чипы тестировались только на средних моделях; теперь — на triллион-параметровом классе. Это **сильный proof-point** для нарратива «Cerebras — реальная альтернатива Nvidia для inference».

**Operational caveat:** только enterprise. Retail/dev-доступа нет. Это **typical Cerebras GTM**: они продают direct'ом крупным клиентам, не open-API'я. **Это ограничивает relevance** для GRO-сегмента (мы — не enterprise AI-hardware customer), но повышает relevance для нарратива **«AI-стек дифференцируется по тиерам»**.

## Связь с OpenAI коллаборацией

@ai_newz упоминает: «**жду чего-то большего чем Codex Spark из их коллаборации с OpenAI**» `[conf:medium, src:2026-05-22]`. 

Контекст:
- Cerebras анонсировала партнёрство с OpenAI ранее в 2026 году.
- **Codex Spark** — какой-то совместный продукт (детали пока не зафиксированы в marketing-memory; уточним при следующем источнике).
- Author-suggestion: следующий milestone — **более серьёзный совместный продукт OpenAI × Cerebras** beyond Codex Spark. Это **anchor для следующей волны Cerebras news**.

## Маркетинговое значение для GRO

**Низкая прямая релевантность** (GRO — продукт обучения, не AI-hardware customer), но **средняя контекстуальная**:

**Для контент-команды:**
- **Hook «триллион параметров на 1000 t/s»** — visceral числа для постов про **«AI-инфраструктура догоняет амбиции моделей»**. Сравнение «Kimi native 31 t/s vs Cerebras 981 t/s» — **31×** разрыв — даёт мощный visceral для постов про **«разница между фронтиром и commodity inference»**.
- **Story про «эра скорости начинается»:** если frontier-модели теперь работают на 1000 t/s, AI-приложения с **real-time inference** (voice agents, screen-readers, real-time copilots) становятся product-feasible. **Связь с [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026|Inworld Realtime TTS-2 <200ms]] и GPT-Realtime-2.**
- **Cerebras IPO как business-story hook:** [[volatile-strict/industry-news/cerebras-ipo-2026-05|cap $40B → $56B за неделю]] — это **+40% post-IPO float-rally**, отличный анкер для постов про **«AI-hardware рынок капитализируется быстрее, чем экспектации»**. [conf:low, src:2026-05-26]

**Для нарратива рынка:**
- Параллельно с GPU scarcity (см. [[volatile-strict/industry-news/gpu-scarcity-neocloud-anthropic-2026-05]]) — **Cerebras продаёт alternative-инфраструктуру** B2B-сегменту. Это **двойной сигнал**: GPU кончились → enterprise клиенты ищут не-Nvidia options → Cerebras + Groq + другие WSE/LPU-vendor'ы получают spotlight. Cerebras IPO + Kimi K2.6 milestone — **proof-of-traction** этого тренда.
- **Anti-Nvidia позиционирование жизнеспособно.** Cerebras собрала $5.5B в IPO именно на этом нарративе, а теперь технически демонстрирует «6.7× быстрее ближайшего GPU-cloud provider». Это **investment-thesis-validation**.

## Supersession для cerebras-ipo-2026-05

См. [[volatile-strict/industry-news/cerebras-ipo-2026-05]] — обновлено cap $40 млрд → **$56 млрд на 22 мая 2026** (post-IPO 8 дней). Старое cap-значение wrapped в HTML-комментарий с audit-trail; новая запись в `## Contradictions` блоке.

## Связанные страницы

- [[sources/2026-05-26-tg-ai-newz-may-19-25-2026]] — первоисточник
- [[volatile-strict/industry-news/cerebras-ipo-2026-05]] — IPO + supersession cap value
- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — Kimi K2.6 spec context (1T MoE 32B active)
- [[volatile-strict/industry-news/gpu-scarcity-neocloud-anthropic-2026-05]] — compute-tightness backdrop
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — макротренд AI-гонки
- [[volatile-strict/industry-news/openai-852b-valuation-doubt-2026]] — параллельная AI-капитализация
