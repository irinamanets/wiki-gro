---
id: mkt:volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05
title: "Google Gemini 3.5 Flash launch + Gemini Spark — Google I/O 2026"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [google, gemini, gemini-spark, agent, ai-platform-wars, google-io, pricing]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-boris-again-may-19-24-2026.md]
namespace: mkt
---

# Google Gemini 3.5 Flash launch + Gemini Spark — Google I/O 2026

**Дата события:** 2026-05-19 (анонс перед I/O), 2026-05-20 (I/O keynote — см. также [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]]) `[conf:high, src:2026-05-19]`. Зафиксировано в [[sources/2026-05-26-tg-boris-again-may-19-24-2026|@boris_again, посты 3912 и 3918]].

## Что вышло

Google выпустил **Gemini 3.5 Flash** — mid-tier «рабочую лошадку», которая обходит прежний флагман Gemini 3.1 Pro на агентных и кодинг-задачах `[conf:high, src:2026-05-19]`.

**Ключевые цифры:**

| Параметр | Значение | Source |
|---|---|---|
| Скорость | ~280 т/с (4× быстрее 3.1 Pro) | `[conf:high, src:2026-05-19]` |
| Качество | уровень Gemini 3.1 Pro на сложных задачах | `[conf:high, src:2026-05-19]` |
| Цена input | $1.50 / 1M токенов | `[conf:high, src:2026-05-24]` |
| Цена output | $9 / 1M токенов | `[conf:high, src:2026-05-24]` |
| Слоган | «Frontier intelligence with action» | `[conf:high, src:2026-05-19]` |

**Pricing-фрейминг по словам автора дайджеста:** «сильно дороже чем раньше, но сильно дешевле, чем Sonnet» `[conf:high, src:2026-05-24]`. То есть Google **поднял** Flash-цены, но **остался дешевле Anthropic mid-tier'а** — и это позиционирующее решение, а не побочный эффект.

## Gemini Spark — Google клонирует OpenClaw

**Gemini Spark** — персональный AI-агент Google на 3.5 Flash, представлен в анонсе как **«runs 24/7, helping you navigate your digital life, taking action on your behalf while under your direction»** `[conf:high, src:2026-05-19]`. По автору источника — **«собственный клон OpenClaw»** (см. [[volatile-strict/competitor-news/openclaw-anthropic-agent-2026]] для контекста OpenClaw как agent-first end-state).

**Структурное наблюдение:** Google не пытается изобретать новый формат — он берёт паттерн Anthropic OpenClaw / Comet (background agent в браузере) и **доставляет его внутрь экосистемы Google-аккаунта**, где у него уже есть дистрибуция (Workspace + Android + Chrome). Это **distribution play**, а не technology play.

## Что значит для рынка

### 1. Mid-tier ценовая революция

До Gemini 3.5 Flash mid-tier-рынок был фрагментирован: Claude Haiku, GPT-4o-mini, Gemini Flash 2.0, Qwen — каждый со своим pricing-кластером. **Gemini 3.5 Flash $1.50/$9 + frontier-уровень + 280 т/с** = новый референс. Все остальные mid-tier модели теперь вынуждены либо догонять качество, либо опускать цены.

Прямая параллель — DeepSeek сделал [параллельный ход в этой же неделе](#) (см. [[volatile-strict/competitor-news/deepseek-v4-pro-price-cut-2026-05]]): V4-Pro подешевела в 4 раза до $0.435/$0.87 `[conf:high, src:2026-05-24]`. То есть **в одну неделю мы наблюдаем ценовое сжатие mid-tier с двух сторон** — frontier-вверх (Gemini поднимает Flash до качества Pro и ставит цену ниже Sonnet) и open-source-снизу (DeepSeek режет цены в 4×).

### 2. Agent-first stack как новая поверхность конкуренции

Gemini Spark + 3.5 Flash + 280 т/с + ~$1.50/$9 = **готовая инфраструктура для агентного workload'а**. Высокая скорость особенно важна, потому что агентные пайплайны бегают цикл «думать → действовать → проверить → думать дальше» — каждый цикл — ~5–10 токенов с overhead'ом, latency накапливается.

Связь с [[evolving/industry-trends/agent-first-world-openclaw-2026]]: теперь у **трёх** игроков (Anthropic OpenClaw, OpenAI Codex, Google Spark) есть собственные «персональные агенты», и они начнут конкурировать **на уровне дистрибуции в OS / браузере**, а не на уровне качества модели.

### 3. Speed gap как новая ось конкуренции

280 т/с против ~50–60 т/с у Claude Sonnet 4.7 — это **5× speed advantage**. В практических agentic-задачах это превращается в **5× больше итераций за то же время** или **5× меньше latency** для коротких ответов. Для GRO как vertical-продукта это означает: **Google становится естественным выбором для real-time use-case'ов** (live ассистенты, customer support, in-app suggestions). Для long-running agentic tasks Claude по-прежнему выигрывает (см. [[evolving-strict/competitor-metrics/artificial-analysis-coding-agent-index-2026-05]] — Claude Code 66 vs Gemini CLI 43).

## Почему это важно для GRO

1. **Возможность снизить cost-per-action в продакшене**. Если GRO использует AI для генерации саджестов / редактуры / классификации, переключение mid-tier на Gemini 3.5 Flash даёт 5× speed + ~30–40% cost reduction vs Haiku/Sonnet-baseline. Стоит проэкспериментировать в production-A/B на одной фиче. [conf:low, src:2026-05-26]
2. **Готовый «Google vs Anthropic vs OpenAI» контент-hook**. Pricing-сравнение трёх mid-tier'ов с реальными цифрами — это сильнейший CFO-friendly контент для блога GRO. Заголовок: *«В мае 2026 mid-tier AI стал в 3 раза дешевле — что это значит для вашего AI-стека»*.
3. **Положение Anthropic как «premium-only»** усиливается. Если Gemini закрывает mid-tier и DeepSeek закрывает open-source-низ, Anthropic вынужденно остаётся в премиум-сегменте (Sonnet/Opus/Mythos), что **поляризует рынок**. Это связано с [[volatile-strict/competitor-news/anthropic-third-party-credits-2026-06]] (Anthropic уже движется в «нам нужны деньги где угодно»).

## Связанные страницы

- [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — первоисточник (посты 3912, 3918)
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] — параллельный анонс Gemini Omni на том же I/O
- [[volatile-strict/competitor-news/deepseek-v4-pro-price-cut-2026-05]] — ценовое сжатие снизу (DeepSeek V4-Pro в 4× дешевле)
- [[volatile-strict/competitor-news/alibaba-qwen-3-7-max-2026-05]] — китайский frontier agentic-конкурент
- [[evolving/industry-trends/agent-first-world-openclaw-2026]] — Gemini Spark как часть agent-first нарратива
- [[evolving-strict/competitor-metrics/artificial-analysis-coding-agent-index-2026-05]] — Coding Agent Index, где Gemini CLI пока 43 vs Claude Code 66
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий нарратив гонки
