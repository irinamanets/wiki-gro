---
id: mkt:evolving-strict/competitor-metrics/llm-web-traffic-2026-04
title: "LLM web-traffic снимок апрель 2026 — ChatGPT, Gemini, Claude, Grok, DeepSeek"
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [llm, ai, openai, anthropic, google, deepseek, xai, web-traffic, audience, similarweb]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-14  # +market-share по визитам OpenAI 77%→56% (@bezsmuzi 15870), Gemini 25%, Claude ~6% — independent cross-check via Кульгин
sources: [sources/2026-05-05-tg-bossofyourboss-apr-may-2026.md, sources/2026-05-14-tg-bossofyourboss-may-12-13-2026.md, sources/2026-05-14-tg-neuraldvig-may-5-12-2026.md, sources/2026-05-14-tg-bezsmuzi-may-5-7.md]
namespace: mkt
---

# LLM web-traffic снимок апрель 2026 (visits + DAU)

Срез аудитории пяти крупнейших публичных LLM-чатов по визитам web-доменов на апрель 2026, с year-over-year сравнением. Источник — пост 1193 канала [[sources/2026-05-05-tg-bossofyourboss-apr-may-2026|@bossofyourboss]] (Михаил Табунов, founder-наблюдатель, expert-inferred). Числа — публичные visit-count'ы (вероятный pipeline источника — SimilarWeb или Ahrefs traffic estimates, явно не указан в посте; `confidence: medium`).

Эта страница — точка истины для текущих audience-чисел LLM при сравнении игроков и обсуждении дрейфа рынка в контенте GRO.

## Сводная таблица — апрель 2026 vs апрель 2025

| Платформа | Визиты апр 2026 | Визиты апр 2025 | YoY-динамика | Source |
|---|---|---|---|---|
| ChatGPT | 5,7 млрд | 5,1 млрд | +12% | `[conf:medium, src:2026-05-05]` |
| Gemini (Google) | 2,5 млрд | 0,4 млрд | ×6,25 | `[conf:medium, src:2026-05-05]` |
| Claude | 0,6 млрд | 0,1 млрд | ×6,0 | `[conf:medium, src:2026-05-05]` |
| Grok | 0,35 млрд | 0,2 млрд | ×1,75 | `[conf:medium, src:2026-05-05]` |
| DeepSeek | 0,35 млрд | 0,48 млрд | −27% | `[conf:medium, src:2026-05-05]` |

## Market-share по визитам — independent cross-check (Кульгин 2026-05-06)

Третий срез — **доля рынка по визитам** среди тройки лидеров, через @bezsmuzi пост 15870 (2026-05-06). Кульгин ретранслирует без указания методологического источника, но цифры **когерентны с table выше** и приходят с другого канала (Tabunov / @bossofyourboss → SimilarWeb visits; Кульгин → market-share %). См. [[sources/2026-05-14-tg-bezsmuzi-may-5-7]].

| Платформа | Доля визитов (год назад) | Доля визитов (май 2026) | Дельта | Source |
|---|---|---|---|---|
| ChatGPT (OpenAI) | 77% | 56% | −21 п.п. | `[conf:medium, src:2026-05-06]` |
| Gemini (Google) | — | 25% | growth | `[conf:medium, src:2026-05-06]` |
| Claude (Anthropic) | — | ~6% | growth | `[conf:medium, src:2026-05-06]` |

**Cohereнтность:** 56% + 25% + 6% = 87% от total — оставшиеся ~13% делят DeepSeek, Grok, и другие. Это **согласовано** с absolute visits таблицей выше: ChatGPT 5,7 млрд / total ~10,2 млрд = ~56%. `[conf:medium, src:2026-05-06]`

**Интерпретация:** не падение ChatGPT в абсолюте (5,1 → 5,7 млрд = +12%), а **mature plateau лидера** на фоне быстрого роста челленджеров. **OpenAI потерял 21 п.п. share за год** при том, что **сохранил абсолютный рост**. `[conf:medium, src:2026-05-06]`

**Кульгинский прогноз:** «Я ставлю на Gemini, т.к. за ними Google» — совпадает с прогнозом Tabunov'а из 1193.

### Дополнительные апрель-май 2026 model releases

Кульгин дамп 5–7 мая фиксирует три параллельных release-сигнала, которые формируют contextual ground для traffic-метрик выше:

1. **Grok 4.3** (2026-05-05, @bezsmuzi 15860) — релиз на OpenRouter, pricing $1.25/$2.50 за 1M токенов. См. [[volatile-strict/competitor-news/xai-grok-4-3-release-2026-05]].
2. **GPT-5.5** — обзор Every (3 недели тестов, 2026-05-06, @bezsmuzi 15874): 62 vs 33 на Senior Engineer бенчмарке против Opus 4.7. См. [[volatile-strict/competitor-news/openai-gpt-5-5-every-review-2026-05]]. `[conf:medium, src:2026-05-06]`
3. **TRELLIS.2 Microsoft** (2026-05-06, @bezsmuzi 15892) — open-source 4B Image-to-3D. См. [[volatile-strict/competitor-news/microsoft-trellis-2-image-to-3d-2026-05]].

GPT-5.5 — **product-катализатор**, который потенциально может остановить дрейф OpenAI traffic share. Re-verify через 90 дней (август 2026) — обновился ли market-share после GPT-5.5 adoption.

## DAU Similarweb (iOS + Android, мобайл — Worldwide, май 2026 backfill)

Второй среза — **Daily Active Users** мобильных приложений (iOS + Android) от Similarweb, опубликован Tabunov'ым 2026-05-12 ([[sources/2026-05-14-tg-bossofyourboss-may-12-13-2026|@bossofyourboss посты 1197+1198]]). Это дополняет визиты web-домена выше: мобайл DAU — параллельный канал adoption, который visits-метрика упускает.

### Claude DAU — hockey-stick за 2025–2026 (чарт 1197)

| Период | Claude DAU | Source |
|---|---|---|
| Январь 2025 – август 2025 | ~1,5 млн (плато) | `[conf:medium, src:2026-05-12]` |
| Ноябрь 2025 | ~5 млн | `[conf:medium, src:2026-05-12]` |
| Февраль 2026 | ~11,2 млн (резкий взлёт) | `[conf:medium, src:2026-05-12]` |
| Конец апреля 2026 | ~25–26 млн | `[conf:medium, src:2026-05-12]` |

**Совокупный рост от плато до пика: ~×17 за 8 месяцев** (1,5 → 25 млн) `[conf:medium, src:2026-05-12]`. Это **классический hockey-stick** в смысле [[canon/marketing-frameworks/hockey-stick-adoption-curve]]: длинный плоский базовый период → плавный устойчивый рост → инфлексионная точка (декабрь 2025 – январь 2026) → вертикальный взлёт.

### Сравнительный DAU Claude vs DeepSeek vs Grok — Q1-Q2 2026 (чарт 1198)

| Платформа | DAU начало января 2026 | DAU конец апреля 2026 | Динамика | Source |
|---|---|---|---|---|
| Claude | ~3 млн | ~25–26 млн | ×8 за 4 месяца | `[conf:medium, src:2026-05-12]` |
| DeepSeek | ~11 млн | ~15 млн | +36% (с локальным пиком ~16 млн в марте) | `[conf:medium, src:2026-05-12]` |
| Grok | ~13 млн | ~10 млн | −23% | `[conf:medium, src:2026-05-12]` |

**Точка пересечения** (когда Claude обогнал и DeepSeek и Grok): середина марта 2026, в зоне ~14 млн DAU `[conf:medium, src:2026-05-12]`. До этого Claude был **третьим по DAU** среди этой тройки.

### Что DAU добавляет к visits-картине

- **Подтверждает прогноз Tabunov'а из 1193:** «Claude станет дефолтом для работы» — DAU-инфлексия материально подтверждает это в ~25 млн ежедневной активной аудитории к концу апреля 2026.
- **Объясняет рост визитов ×6 YoY у Claude (0,1 → 0,6 млрд):** не равномерный рост, а **сжатый в Q1-Q2 2026** взрыв (DAU выросла с 1,5M до 25M в основном за декабрь 2025 — апрель 2026).
- **DeepSeek slowdown подтверждается на двух осях:** visits −27% YoY + DAU дрейф в плато `[conf:medium, src:2026-05-12]`. Виральность Q1 2025 не конвертировалась в устойчивую активную базу.
- **Grok отрицательный DAU-трек.** Из всех трёх — единственный с YoY-снижением мобильных DAU за квартал. При этом visits +75% YoY `[conf:medium, src:2026-05-12]` — расхождение объясняется тем, что Grok-визиты идут в основном через X-веб (встроенный доступ), а mobile-app не приживается.

### Caveat — Similarweb mobile DAU

- **Источник цифр — Similarweb publicly-reported chart** (видимый watermark в обоих изображениях). Tabunov цитирует чарт, не сам source-data — это retransmission.
- **DAU охватывает только официальные мобильные приложения**, не учитывает desktop-веб через chat.* домены, API-трафик, и Claude Code как CLI-инструмент.
- **Округление до миллиона.** Cifры считаны с графика визуально; точность ±0,5M в пиковой зоне.

### Vendor-side enforcement как фактор RU-DAU

**Сигнал 2026-05-08 ([[sources/2026-05-14-tg-neuraldvig-may-5-12-2026|@neuraldvig 10650]] со ссылкой на Baza):** Claude начал **массово банить RU-пользователей за регистрацию через VPN**. По данным Baza — **сотни аккаунтов** уже потеряли доступ; деньги за подписку возвращают, но чаты/проекты/код теряются `[conf:medium, src:2026-05-08]`. Эксперты связывают волну с новыми проверками по паттернам частого переподключения VPN и смены региона.

**Что это значит для RU-сегмента DAU-метрик:**

- **Российская часть Claude DAU из чарта 1198 (~25 млн в апреле 2026)** содержала significant долю серых VPN-регистраций из РФ. Точная цифра не публична, но по [[sources/2026-05-14-tg-bossofyourboss-may-12-13-2026|@bossofyourboss посту 1199]] Tabunov явно использует Claude через VPN-инфраструктуру в команде.
- **К июню 2026** ожидается **видимая просадка Claude DAU в RU-сегменте** при условии что волна банов продолжается systematically, а не как разовый cleanup. TTL: 30 дней re-verify.
- **Структурный фактор для прогноза Tabunov'а «Claude станет дефолтом для работы»**: для RU-аудитории прогноз получает значимый regulatory headwind. Если volumes продолжатся — RU-developers могут массово мигрировать на (а) российские альтернативы (GigaChain, Yandex AI Studio, MWS GPT Model Hub), (б) более устойчивые к VPN-fingerprint вендоры (DeepSeek, Qwen, open-source). См. [[evolving/industry-trends/ru-ai-aggregator-platforms-2026|MWS GPT Model Hub]] как один из таких вариантов.
- **Cross-link** на 15-й вектор [[evolving/industry-trends/ru-digital-regulatory-squeeze-2026]] — vendor-side suspension как новый regulatory squeeze axis.

Эта заметка **не меняет численные данные** в DAU-таблицах выше (они отражают апрель 2026 — до волны банов), но **flag**-ует, что **май-июнь 2026 DAU-чарты в RU-разрезе могут показать материальное снижение Claude**, не связанное с product-fundamentals.

## Ключевые наблюдения

- **ChatGPT удержал лидерство, но рост схлопнулся.** Прирост +12% год-к-году (5,1→5,7 млрд) на фоне ×6 у Gemini и Claude `[conf:medium, src:2026-05-05]`. Это не падение, но и не растущий лидер — фаза «mature plateau».
- **Gemini — главный gainer года.** Рост в 6,25× (0,4→2,5 млрд визитов) сделал его второй платформой по визитам, опередив Claude и Grok вместе взятых `[conf:medium, src:2026-05-05]`. Драйвер — интеграция в Google Search и default-bundling в Workspace.
- **Claude — растёт пропорционально, остаётся нишевым.** Тот же ×6 рост, что у Gemini, но с гораздо меньшей базы (0,1→0,6 млрд) `[conf:medium, src:2026-05-05]`. Audience остаётся профессиональной (developers, knowledge-workers).
- **DeepSeek провалился.** Единственный игрок с YoY-падением: −27% (0,48→0,35 млрд) `[conf:medium, src:2026-05-05]`. Виральность Q1 2025 («китайская GPT-4 за копейки») не конвертировалась в устойчивую аудиторию.
- **Grok ищет нишу.** Скромный рост ×1,75 (0,2→0,35 млрд) `[conf:medium, src:2026-05-05]`, при том что встроен в X/Twitter с гарантированным trafficом — слабый сигнал для модели Маска.

## Прогноз Табунова (subjective, expert-inferred)

Из поста 1193 (`confidence: medium`):

- **Gemini станет дефолтной моделью для повседневных задач** `[conf:medium, src:2026-05-05]` — поведенческий аргумент: Google ecosystem (Search, Workspace, Android) сделает Gemini «out-of-the-box» для масс-аудитории.
- **Claude станет дефолтом для работы** `[conf:medium, src:2026-05-05]` — закрепится в developer/knowledge-worker сегменте через Claude Code, MCP-стандарт ([[evolving/industry-trends/anthropic-creative-tools-mcp-2026]]) и enterprise-JV ([[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]]).
- **ChatGPT помрёт под тяжестью инвестиций** `[conf:low, src:2026-05-05]` — спорный тезис; контр-аргумент в [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] о том, что OpenAI делает enterprise-pivot через The Deployment Company.
- **Grok останется нишевым «весёлым непонятно что»** `[conf:medium, src:2026-05-05]` — поддерживается треком Grok image-generation backlash (декабрь 2025 — апрель 2026, см. предыдущий дамп пост 1189).

## Динамика прошлого года — что Табунов писал в 2025

Tabunov сделал это **3-й «частью»** серии «Битва LLM» (2 года подряд, кадэнс ~12 мес). В 2025 (1-я часть, год назад):

- **Прогноз №1: «Я ставлю на Google»** `[conf:medium, src:2026-05-05]` — реализовался: Gemini ×6,25.
- **Прогноз №2: «Claude — мой помощник на каждый день»** `[conf:medium, src:2026-05-05]` — частично реализовался для personal-use, но Claude остался more developer-skewed.

Это даёт Tabunov-прогнозу некоторую calibration-track: 2/2 для крупных трендов, поэтому apr-2026 forecast стоит читать с `confidence: medium`, а не `low`.

## Caveat по методологии

- **Visits ≠ MAU.** Визиты web-домена не равны активным пользователям; не учитывают мобильные приложения и API-трафик. Например, Claude Code как CLI-инструмент даёт нулевой visit-count при том, что это ключевая часть adoption Claude.
- **API-traffic не виден в visit-count'ах.** OpenAI и Anthropic зарабатывают значительную долю выручки на API, который не отражается в web-визитах. Отсюда возможный bias: visit-count недооценивает реальную долю Claude в developer-сегменте.
- **Источник методологии не указан.** Tabunov-пост не цитирует SimilarWeb, Ahrefs или другой провайдер; числа могут быть округлёнными или агрегированными по разным источникам — отсюда `confidence: medium`, а не `high`.

## Применимость для GRO

1. **Контент-хук «битва LLM»** — благодаря cadence Tabunov ~12 мес, можно делать собственный годовой LLM-обзор для GRO как [[evolving/content-trends/tabunov-founder-growth-hooks|founder-voice serial]] формат с метриками `[conf:medium, src:2026-05-05]`.
2. **Default-страх для пользователей.** Если Gemini действительно станет default, GRO как productivity-app должен заранее обеспечить интеграцию с Gemini API (через MCP) на ровне с Claude/ChatGPT, чтобы не отвалиться от mass-market workflow `[conf:medium, src:2026-05-05]`.
3. **Контент-нарратив «Claude → работа, Gemini → жизнь».** Сегментация рынка по use-case даёт чистый messaging-фреймворк: для GRO как «дисциплина продуктивности» Claude-аудитория ближе по психотипу (knowledge-workers с дисциплиной).

## Связанные страницы
- [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] — финансовая сторона того же рынка
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — нарратив того же рынка
- [[evolving/industry-trends/anthropic-creative-tools-mcp-2026]] — Anthropic creative-tools push
- [[evolving/content-trends/tabunov-founder-growth-hooks]] — Tabunov-формат «годовая битва LLM»
- [[canon/marketing-frameworks/hockey-stick-adoption-curve]] — общая рамка инфлексии (Claude DAU как эмпирический якорь)
- [[sources/2026-05-05-tg-bossofyourboss-apr-may-2026]]
- [[sources/2026-05-14-tg-bossofyourboss-may-12-13-2026]] — Similarweb DAU чарты Claude/DeepSeek/Grok
- [[sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026]] — Tabunov 2-я «часть» (год назад)
- [[sources/2026-05-14-tg-bezsmuzi-may-5-7]] — Кульгинский market-share cross-check + Grok 4.3 / GPT-5.5 / TRELLIS.2 release context
- [[volatile-strict/competitor-news/openai-gpt-5-5-every-review-2026-05]] — связанный product-релиз
- [[volatile-strict/competitor-news/xai-grok-4-3-release-2026-05]] — связанный product-релиз

## Backlinks

_5 pages link to this one._

- [[evolving/content-trends/tabunov-founder-growth-hooks]]
- [[evolving/industry-trends/anthropic-creative-tools-mcp-2026]]
- [[index]]
- [[sources/2026-05-05-tg-bossofyourboss-apr-may-2026]]
- [[volatile-strict/industry-news/mts-adtech-mta-launch-2026]]
