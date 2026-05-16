---
id: mkt:volatile-strict/competitor-news/openai-gpt-5-5-every-review-2026-05
title: "GPT-5.5 — Every review (3 недели тестов): первая модель OpenAI за год, на которую переходят с Claude"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [openai, anthropic, gpt-5-5, claude, opus-4-7, llm, developer-tools, codex, every-review]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14  # +Yandex @techno_yandex 5212 (2026-05-11) institutional second-source attestation GPT-5.5 Instant как default ChatGPT для всех
sources: [sources/2026-05-14-tg-bezsmuzi-may-5-7.md, sources/2026-05-14-tg-techno-yandex-may-6-13-2026.md]
namespace: mkt
---

# GPT-5.5 — Every review (3 недели тестов)

[Every](https://every.to/) опубликовал sustained-review GPT-5.5 после 3 недель использования, сравнивая с Anthropic Opus 4.7 на собственном Senior Engineer бенчмарке. Кульгин ретранслировал review в @bezsmuzi пост 15874 (2026-05-06) — см. [[sources/2026-05-14-tg-bezsmuzi-may-5-7]]. Это первая модель OpenAI за год, ради которой команда писателей Every **переключилась с Claude**.

**Yandex @techno_yandex (2026-05-11, пост 5212)** ретранслировал OpenAI-анонс GPT-5.5 **Instant** как «обновление основной нейросети в ChatGPT, доступной всем пользователям»; описал её как «заметно быстрее, лучше работает с фотографиями, точнее решает когда идти в поиск, реже галлюцинирует, даёт лаконичные ответы без эмодзи, лучше учитывает контекст прошлых бесед». Это second-source attestation институциональной редактуры — см. [[sources/2026-05-14-tg-techno-yandex-may-6-13-2026]]. `[conf:medium, src:2026-05-11]`

**Почему `volatile-strict`:** оценки cap-моделей актуальны 30-90 дней (новый релиз перетасует расклад), numeric anchors требуют inline-маркеров. TTL 90 дней.

## Структурный сигнал

Это **второй раз** за апрель–май 2026 (после Anthropic Dreams Mode и openai-codex-vs-claude-code), когда:

1. Профессиональная writer/developer-команда **публично декларирует переход с Claude на ChatGPT**.
2. Базис сравнения — **3 недели регулярного использования**, а не one-shot бенчмарк.

Сигнал смены **default mind-share** в writer/developer use-case, где Claude доминировал последний год.

## Цифры — Every Senior Engineer benchmark

| Модель | Senior Engineer score | Период теста | Объём тестирования | Source |
|---|---|---|---|---|
| GPT-5.5 | 62 из 100 | 3 недели | 900+ млн токенов | `[conf:medium, src:2026-05-06]` |
| Opus 4.7 | 33 из 100 | 3 недели | 900+ млн токенов | `[conf:medium, src:2026-05-06]` |

**Caveat:** Every не публикует методологию бенчмарка публично (внутренний test-suite). `confidence: medium` для chisel-сравнения. Но 3-недельный sustained-test с 900M токенов — структурно сильнее одиночных benchmark-прогона. `[conf:medium, src:2026-05-06]`

## Качественные оценки Every

**Что Every понравилось в GPT-5.5:**

- **Скачок в кодинге + приятно работать.** «Быстрая, дружелюбная, сразу стала основной. Но при этом мощная в коде — редкое сочетание». `[conf:medium, src:2026-05-06]`
- **Серьёзная концептуальная ясность.** «Держит сложный план в голове часами, не отвлекаясь на существующий код. Первая модель, которая справляется со сложными рефакторингами, где нужно удалить и переосмыслить большую часть кодовой базы.» `[conf:medium, src:2026-05-06]`
- **Хорошо пишет тексты.** «Первая модель OpenAI за год, из-за которой писатели Every перешли с Claude. Текст ощущается органичнее, лучше копирует стиль, не перебарщивая.» `[conf:medium, src:2026-05-06]`
- **Агентская работа.** «Первая модель OpenAI, которая одновременно и сильный инженер, и умеет всё: от таблиц до ресерча.» `[conf:medium, src:2026-05-06]`
- **Codex desktop.** «Безумно быстрая, потрясающе работает в десктопном Codex — часть команды пересела с Claude Code и Cowork на время тестирования.» `[conf:medium, src:2026-05-06]`

**Что осталось за Opus 4.7:**

- **Планы лучше.** «Планы 5.5 очень читаемые, но у Opus внимательнее к деталям и острее инсайты.» `[conf:medium, src:2026-05-06]`
- **Фронтенд + фулстек.** «Opus чуть лучше во фронтенде и фулстек-продуктовой работе, когда нужно фулстек-мышление и дизайн, и не очень хорошо пишет на Ruby.» `[conf:medium, src:2026-05-06]`
- **Underspecified задачи.** «5.5 отличный вайб-кодер, но без плана хуже Opus — Opus лучше читает между строк в недоспецифицированных задачах.» `[conf:medium, src:2026-05-06]`

**Интересный pattern:** GPT-5.5 «лучше всего работает по плану, составленному Opus 4.7» — гибридный workflow.

## Контекст — Кульгинский комментарий

Кульгин в пост-репосте **не использует GPT-5.5 сам**: «То что вижу, наши ребята задействуют Gemini 3.1 Pro + DeepSeek». То есть его команда оптимизирует по cost не по quality. Это **отдельный сигнал** — для RU-SMB сегмента (Кульгин типичный representative) выбор LLM идёт не «лидеры рынка», а **price-performance** (китайские + Google).

## Связь с другими сигналами

- **DAU Claude инфлексия (1,5M → 25M)** в [[evolving-strict/competitor-metrics/llm-web-traffic-2026-04]] — Anthropic ещё **на пиковом adoption**. GPT-5.5 не делает Claude меньше популярным, но **перетягивает на маржу** новых high-intent профессиональных пользователей.
- **OpenAI market share визитов −21 п.п. за год** (с 77% до 56%, [[evolving-strict/competitor-metrics/llm-web-traffic-2026-04]]) — GPT-5.5 как product может остановить дрейф или даже его обернуть. Re-verify через 90 дней. [conf:low, src:2026-05-14]
- **Codex vs Claude Code** ([[volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05]]) — параллельный сигнал; Every подтверждает, что Codex desktop становится конкурентным с Claude Code.

## Маркетинговые выводы для GRO

1. **Tech-stack ratification.** Если GRO использует Claude для product-research / writing / code — этот review — **сигнал переоценить**. Не один-в-один заменять, а параллельный тест GPT-5.5 на собственных задачах (3 недели — методика валидна).
2. **Контент-хук:** «Every опубликовал 3-недельный обзор GPT-5.5 — впервые за год их писатели перешли с Claude на ChatGPT. 62 vs 33 на Senior Engineer бенчмарке. Что это значит для твоего стека?» — open-ended question для аудитории founders / developers.
3. **Caveat для контента:** 62 vs 33 — внутренний бенчмарк Every, **не публичный**. Цитировать с явной атрибуцией «по бенчмарку Every», не как «GPT-5.5 в 2 раза лучше Opus».

## TTL и план верификации

- **TTL: 90 дней** (до 2026-08-14). Re-verify: появятся ли новые публичные бенчмарки (SWE-bench, HumanEval, MMLU обновления), confirm/refute эти оценки.
- **Контр-сигнал:** если Anthropic выкатывает Claude 5 / Opus 5 в ближайшие 60 дней — текущий review устаревает, нужен новый раунд сравнения.

## Связанные страницы

- [[evolving-strict/competitor-metrics/llm-web-traffic-2026-04]] — апрель 2026 web-traffic + DAU
- [[evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026]] — pricing-перспектива
- [[volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05]] — параллельный сигнал
- [[volatile-strict/competitor-news/anthropic-claude-dreams-mode-2026-05]] — Anthropic counter-move
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — нарратив рынка
- [[sources/2026-05-14-tg-bezsmuzi-may-5-7]] — первоисточник, пост 15874
