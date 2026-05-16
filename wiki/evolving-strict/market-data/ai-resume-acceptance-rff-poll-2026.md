---
id: mkt:evolving-strict/market-data/ai-resume-acceptance-rff-poll-2026
title: "AI-резюме acceptance — sentiment HR/recruiters (RFF poll, 543 голоса, апрель 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [market-data, ai, hr, resume, sentiment, russia, poll]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-rff-channel-redump-mar-may-2026.md]
namespace: mkt
---

# AI-резюме acceptance — sentiment HR/recruiters (RFF poll, апрель 2026)

Самый детализированный публичный замер sentiment по AI-edited резюме среди RU HR-сообщества на 2026-04-27 `[conf:high, src:2026-04-27]`. Опрос проведён внутри Telegram-канала [@rff_channel](https://t.me/rff_channel) (Recruitment for Friends, аудитория 50K+ HR/рекрутеров), 543 голоса. Самозаявленный sample, не репрезентативный по всему рынку, но HR-аудитория сама по себе является **decision-maker'ом** в воронке найма — то есть это срез именно по тем, кто реально читает AI-edited резюме.

## Распределение ответов

| Ответ | % | N | Source |
|---|---|---|---|
| «Если видно, что применяли ИИ, но аккуратно — норм» | 39% | 213 | `[conf:high, src:2026-04-27]` |
| «Прекрасно, тоже пользуюсь» | 35% | 195 | `[conf:high, src:2026-04-27]` |
| «Нейтрально» | 16% | 88 | `[conf:high, src:2026-04-27]` |
| «Просмотреть ответы коллег» (passive) | 11% | 64 | `[conf:high, src:2026-04-27]` |
| «Пролистываю сразу если вижу — ←→↑↓~» | 6% | 36 | `[conf:high, src:2026-04-27]` |
| «Почти не сталкиваюсь» | 2% | 16 | `[conf:high, src:2026-04-27]` |
| «Нет мнения» | 2% | 15 | `[conf:high, src:2026-04-27]` |
| «Что такое ИИ?» | 1% | 6 | `[conf:high, src:2026-04-27]` |
| «Свой вариант в комментариях» | 0% | 1 | `[conf:high, src:2026-04-27]` |

(Сумма не равна точно 100% из-за округлений и passive-опции «посмотреть ответы коллег».) `[conf:high, src:2026-04-27]`

## Ключевые числовые выводы [conf:high, src:2026-04-27]

- **Strong positive (sam использую) — 35%** `[conf:high, src:2026-04-27]`
- **Conditional positive (норм если аккуратно) — 39%** `[conf:high, src:2026-04-27]`
- **Strong+conditional positive = 74%** `[conf:high, src:2026-04-27]` — большинство HR-аудитории RFF принимает AI-edited резюме
- **Strong rejection (пролистываю сразу) — 6%** `[conf:high, src:2026-04-27]` — strong AI-stigma остаётся узкой нишей
- **Neutral / no opinion — 16% + 2% + 2% + 1% = 21%** `[conf:high, src:2026-04-27]`

## Что триггерит rejection (по мнению автора RFF, [src:2026-04-27])

«Триггерит не ИИ, а:
- **Шаблонность**
- **Странный язык**
- **Перегруженные формулировки**
- **"Креатив" со спецсимволами** (`—`, `←`, `→`, `↑`, `↓`, `~`)»

То есть rejection-trigger — **не сам факт использования AI, а низкое качество финального текста.** Это conceptually совпадает с outputs [[canon/marketing-frameworks/ai-text-markers-checklist|AI-text-markers checklist]] (Pressfeed): те же 12 маркеров AI-текста, которые HR замечают и квалифицируют как «шаблонность».

## Связь с academic preprint (Hook 14, self-preference bias) [conf:medium, src:2026-05-02]

Параллельно RFF-опросу академическое исследование `arxiv.org/abs/2509.00462` (см. [[volatile-strict/industry-news/llm-self-preference-resume-bias-2026]]) показало, что когда **оценщик-LLM и автор резюме на одной модели**, кандидат проходит шортлист на **20–60% чаще** при идентичном содержании `[conf:medium, src:2026-05-02]`. Это **self-preference bias** на side LLM-оценщиков.

**RFF-опрос дополняет картину со стороны human-оценщиков:** 74% human HR ок с AI-резюме (RFF, 543 votes, 2026-04-27) `[conf:high, src:2026-04-27]`, self-preference bias эффект 20–60% на LLM-оценщиков (academic preprint, 2026-05-02) `[conf:medium, src:2026-05-02]`. **Двусторонняя картина:** ни human, ни LLM-оценщики не отвергают AI-резюме как класс — они оценивают качество финального текста (human) или совпадение «диалекта» (LLM).

## Импликации для GRO-маркетинга [conf:medium, src:2026-05-05]

1. **Узкая ниша «AI-stigma» (6% strong rejection)** — это **меньшинство**, опасения «если использую AI — меня не позовут» сильно завышены `[conf:high, src:2026-04-27]`. Counter-narrative для GRO: «AI — инструмент, а не риск» — но c caveat: качество ≠ инструмент.
2. **Триггеры rejection — не AI, а шаблонность.** Это **прямой канон** для positioning [[canon/marketing-frameworks/ai-resume-prompting-checklist-rff]]: использование AI окей, но **за финальный результат отвечает человек**.
3. **Sample limitation.** Это HR-сторона, не candidate-сторона. Данные про то, как HR относится к AI-резюме; не про то, сколько кандидатов реально использует AI. Cross-link с [[evolving/industry-trends/candidate-side-ai-services-2026]] для **candidate-side adoption rate** (full-outsource через бот за десять процентов годового дохода). `[conf:medium, src:2026-05-05]`
4. **Time-to-stale.** RFF-опрос — апрель 2026. Sentiment к AI-резюме **дрейфует месяцами**. Re-verify через шесть месяцев (октябрь 2026) — если шесть процентов strong rejection вырастет до пятнадцати-двадцати процентов, это сигнал саттурации/контр-волны (HR начинают активно фильтровать AI-output из-за perceived качества). `[conf:medium, src:2026-05-05]`

## Использование в content hooks GRO

Прямая cross-link с **Hook 22** в [[evolving/content-trends/career-audience-hooks-2026]] — «AI экологично, не шаблонно».

Hook-формулировки:

> «74% HR в апреле 2026 спокойно относятся к резюме, написанному с AI. Только 6% триггерятся. Триггерит не AI — триггерит шаблонность. Что значит: ваше AI-резюме плохо не потому, что вы использовали AI, а потому что отдали финал AI-у целиком». `[conf:high, src:2026-04-27]`

> «Самый большой миф 2026 года: "если HR увидит, что я использовал AI — не позовёт". Реальность: 39% HR прямо говорят "если аккуратно — норм", и ещё 35% "сам пользуюсь". Под удар попадает не AI, а финальное качество текста». `[conf:high, src:2026-04-27]`

## Caveats [conf:medium, src:2026-05-05]

- **Self-selected sample** аудитории RFF (HR/рекрутеры активно следящие за HR-Telegram-контентом). Не общий рынок труда; не candidate-side. `[conf:medium, src:2026-04-27]`
- **n = 543** — sample размер достаточный для grouping, но недостаточный для подсегментации (по индустрии / возрасту / стажу).
- **Self-reported sentiment**, не observed behavior. HR может говорить «норм если аккуратно», но в реальной воронке отсеивать кандидата за perceived AI-стиль. Cross-validation через behavioral A/B (пары identical-content резюме «human-style» vs «AI-default-style») в RU-контексте на 2026-05 не проводилась.
- **Not stratified** по seniority уровня роли, industry, размеру компании. HR в IT-компании может отвечать иначе, чем HR в production-сегменте.
- **Single-source observation.** Cross-validation: hh.ru-бренд аналогичных опросов на 2026-05 не публиковал. Ждём вторую точку для триангуляции.

## Связанные страницы

- [[sources/2026-05-05-tg-rff-channel-redump-mar-may-2026]] — основной источник
- [[canon/marketing-frameworks/ai-resume-prompting-checklist-rff]] — 5 принципов экологичного AI-prompting (прескрипция RFF после интерпретации опроса)
- [[evolving/content-trends/career-audience-hooks-2026]] — Hook 22 строится на этих числах
- [[volatile-strict/industry-news/llm-self-preference-resume-bias-2026]] — academic preprint про LLM-side bias (cross-validation)
- [[canon/marketing-frameworks/ai-text-markers-checklist]] — 12 маркеров AI-текста, которые HR воспринимают как «шаблонность»
- [[evolving/industry-trends/candidate-side-ai-services-2026]] — candidate-сторона adoption (Hook 13)
- [[evolving/content-trends/ai-text-detection-landscape-2026]] — двусторонняя детекция AI-текста
- [[evolving-strict/market-data/ru-labor-market-q1-2026]] — макроконтекст рынка труда

## Backlinks

_7 pages link to this one._

- [[canon/marketing-frameworks/ai-resume-prompting-checklist-rff]]
- [[evolving-strict/market-data/ru-labor-market-q1-2026]]
- [[evolving/content-trends/career-audience-hooks-2026]]
- [[evolving/content-trends/telegram-native-formats]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-rff-channel-redump-mar-may-2026]]
