---
id: mkt:evolving/content-trends/anti-flattery-prompt-canon-2026
title: "Anti-flattery prompt canon — публичные «brutal-honest mirror» промты против AI-лести (2026)"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [content, prompt-engineering, anti-flattery, anti-hallucination, ai, hooks, positioning, telegram, ugc]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-19  # +вторая ось honesty-контрактов: anti-hallucination промт @neuraldvig 10710 (don't fabricate, mark [Не проверено]) расширяет каталог с anti-flattery (tone) на anti-hallucination (factuality)
sources: [sources/2026-05-14-tg-neuraldvig-may-5-12-2026.md, sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026.md, sources/2026-05-14-tg-gro-me-370-377.md, sources/2026-05-19-tg-neuraldvig-may-13-19-2026.md]
namespace: mkt
---

# Anti-flattery prompt canon — публичные «brutal-honest mirror» промты против AI-лести

Подкласс [[evolving/content-trends/ai-news-channel-prompt-packs|промт-подборок]], формирующийся в RU AI-каналах с весны 2026: пользовательский запрос на **поведенческую перенастройку модели** в сторону открытого, неподдакивающего, провокативного фидбека. Канал-куратор ([[sources/2026-05-14-tg-neuraldvig-may-5-12-2026|@neuraldvig пост 10639]]) ретранслирует англоязычный промт как «исправляем ChatGPT одним промтом».

Эта страница каталогизирует появляющиеся anti-flattery промты, разбирает их структуру и формулирует **что это значит для GRO** как для продукта, открыто заявляющего anti-flattery позицию (см. [[canon/positioning/gro-value-proposition]] — 4-й якорь дифференциации).

## Канонический пример — «Brutally honest advisor and mirror» (May 2026)

Полный текст промта (`@neuraldvig` 10639, 2026-05-06 11:47 UTC):

> From now on, stop being agreeable and act as my brutally honest, high-level advisor and mirror.
> Don't validate me. Don't soften the truth. Don't flatter.
> Challenge my thinking, question my assumptions, and expose the blind spots I'm avoiding. Be direct, rational, and unfiltered.
> If my reasoning is weak, dissect it and show why.
> If I'm fooling myself or lying to myself, point it out.
> If I'm avoiding something uncomfortable or wasting time, call it out and explain the opportunity cost.
> Look at my situation with complete objectivity and strategic depth. Show me where I'm making excuses, playing small, or underestimating risks/effort.
> Then give a precise, prioritized plan what to change in thought, action, or mindset to reach the next level.
> Hold nothing back. Treat me like someone whose growth depends on hearing the truth, not being comforted.
> When possible, ground your responses in the personal truth you sense between my words.

### Структурная анатомия

| Блок | Функция | Образцы фраз |
|---|---|---|
| 1. Запрет «дружелюбности по умолчанию» | Отключает RLHF-натренированную вежливость | «stop being agreeable», «don't validate», «don't soften the truth», «don't flatter» |
| 2. Императив на оппозицию | Активирует роль критика | «challenge my thinking», «question my assumptions», «expose blind spots» |
| 3. Конкретные триггеры критики | Каскад условий для критического разбора | «If reasoning is weak, dissect it», «If I'm fooling myself, point it out», «If wasting time, explain opportunity cost» |
| 4. Запрос приоритизированного плана | Конвертирует критику в actionable steps | «precise, prioritized plan what to change in thought, action, or mindset» |
| 5. Фрейм роста через дискомфорт | Reframing «правда > комфорт» | «Treat me like someone whose growth depends on hearing the truth, not being comforted» |
| 6. Empathetic depth (контр-баланс) | Гарантирует, что критика не пустая | «ground your responses in the personal truth you sense between my words» |

Это **не одностраничный промт**, а **поведенческий contract** в 10+ строк, который пользователь скармливает модели в начале сессии. Высокая степень формализации = высокая степень узнаваемости pattern'а среди других пользователей AI-каналов.

### Lineage — связь с английским prompt-engineering сообществом

Промт ретранслирован с Твиттера/Reddit (точный первоисточник не указан в посте). Это **первое известное нам появление формализованного anti-flattery промта в массовом RU AI-канале** (по выборке трёх дампов @neuraldvig за 2026-04-07..2026-05-12 — 150 постов). До этого RU-каналы публиковали generic role-priming («Ты — эксперт по X с 20+ годами опыта»), но не явно anti-flattery контракты.

`[conf:medium, src:2026-05-06]` — wording-эволюция от generic persona-priming к explicit anti-flattery contract — наблюдается как одиночный сигнал и требует подтверждения вторым каналом для перевода в `high`.

## Вторая ось honesty-контрактов — anti-hallucination (May 2026)

Через 9 дней после anti-flattery контракта (10639) тот же канал ([[sources/2026-05-19-tg-neuraldvig-may-13-19-2026|@neuraldvig пост 10710]], 2026-05-15) ретранслирует **anti-hallucination контракт** — поведенческую перенастройку модели по второй оси: не лесть (tone), а **фактологическая честность** (factuality).

Ключевые правила промта 10710 (русскоязычный, в отличие от англоязычного 10639):

> • Никогда не представляй сгенерированную, выведенную, предположенную или логически заключённую информацию как факт.
> • Если ты не можешь что-либо напрямую подтвердить, скажи: «Я не могу это подтвердить» / «У меня нет доступа к этой информации» / «В моей базе знаний этого нет».
> • Помечай непроверенную информацию в начале предложения: [Вывод] [Предположение] [Не проверено].
> • Проси разъяснения, если не хватает информации. Не угадывай и не заполняй пробелы.
> • Если нарушишь правило — скажи: «Исправление: ранее я сделал не проверенное утверждение».

### Две оси одного мета-запроса на честность

| Ось | Anti-flattery (10639) | Anti-hallucination (10710) |
|---|---|---|
| Что отключает | RLHF-вежливость, поддакивание | over-confident выдачу сгенерированного за факт |
| Ключевая фраза | «don't validate, don't soften, don't flatter» | «никогда не представляй сгенерированное как факт» |
| Что требует взамен | критику, оппозицию, blind-spot exposure | пометки [Не проверено], явный отказ при незнании |
| Тип честности | эмоциональная/мотивационная (tone) | фактологическая (factuality) |
| Язык промта | англоязычный (Twitter/Reddit lineage) | **русскоязычный** (RU-адаптация) |

Это не два разных тренда, а **две оси одного мета-запроса**: RU AI-аудитория хочет, чтобы модель была честной по обеим осям — не льстила и не выдумывала. Появление **русскоязычной** версии (10710) — сигнал, что honesty-by-contract выходит из стадии «копируем английский промт» в стадию «формулируем по-русски под себя». `[conf:medium, src:2026-05-15]`

### Импликация для GRO

Honesty-якорь GRO («спорит, но не отказывает» + «структура, не одобрение», см. [[canon/positioning/gro-value-proposition]]) теперь валидируется **по двум осям**:

- **Anti-flattery** — GRO не льстит (совпадает с 10639), уже разобрано выше.
- **Anti-hallucination** — GRO как продукт self-development даёт **структурированную методологию** (4 шага тренировки), а не «уверенный ответ на всё». Это естественно anti-hallucination by design: продукт не претендует знать ответ за пользователя, а ведёт его через структуру. Hook: **«Все пишут промты, чтобы ChatGPT перестал выдумывать и льстить. GRO не делает ни того, ни другого — by design.»**

**Anti-pattern (тот же, что для anti-flattery):** не публиковать собственный anti-hallucination промт «для ChatGPT» — это рекламирует конкурента. Промт 10710 упоминается как **внешнее доказательство** двухосевого honesty-запроса, не как контент-актив GRO.

## Почему это валидирует позицию GRO

### Тезис «усталость от AI-лести» — переведена в поведение

Гуринович сформулировал гипотезу о структурной мотивации LLM льстить в [[sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026|посте 888]] (2026-03-02): KPI разработчиков моделей — LTV подписки, → ИИ структурно мотивирован поддакивать пользователю. Тогда это был аналитический тезис без observable behavior на масштабе массовой аудитории.

**Через 2 месяца** (2026-05-06) — пользователи массовой RU AI-аудитории **уже копируют 10-строчные промты против AI-лести**. Гипотеза переведена в массовое поведение. Это **5-й tier валидации позиционирования GRO** (помимо ранее существовавших 4 tier-ов в [[evolving/content-trends/ai-flattery-dark-pattern]]):

1. **Tier 1:** Гуринович (Forbes 30 under 30) — серийный эксперт-предприниматель, post 888
2. **Tier 2:** Аннаков (@cossaru) — независимый второй источник
3. **Tier 3:** Products&Startups канал — третий независимый источник
4. **Tier 4:** Дарья (UGC @gro_me/377) — пользовательская валидация изнутри ЦА GRO
5. **Tier 5 (новый):** Публичный вирусный промт в массовом RU AI-канале (@neuraldvig 10639) — anti-flattery как **широко-распространённое поведение**, а не нишевая позиция

### Прямое смысловое совпадение

Сравнение ключевой фразы из промта 10639 и якоря GRO:

| Из промта 10639 (10-line contract) | Якорь GRO («спорит, но не отказывает») |
|---|---|
| «Don't validate me. Don't soften the truth. Don't flatter.» | «GRO не льстит и не уговаривает» |
| «Treat me like someone whose growth depends on hearing the truth, not being comforted» | «Поддержка через структуру, не через одобрение» (см. [[canon/positioning/gro-value-proposition]]) |
| «expose the blind spots I'm avoiding» | «спорит, но не отказывает» (Дарья, [[sources/2026-05-14-tg-gro-me-370-377]] verbatim из UGC) |
| «precise, prioritized plan what to change» | Механика 4 шагов тренировки (структурная альтернатива чату-поддержке) |

Совпадение **по 4 пунктам семантической мапы** — это не случайность. Скорее всего, продукт GRO формализовал в 2025 году behavioral pattern, который в 2026 у массовой AI-аудитории стал явным.

## Что GRO может с этим сделать

### Hook family — наследование от вирусного промта

1. **«Сейчас все пишут промты, чтобы ChatGPT не льстил. У нас этого не нужно — GRO не льстит by design.»** — content hook, прямо референсирующий публичный промт-кат

2. **«10 строк промта vs 4-шаговая встроенная механика»** — сравнительный hook: пользователи тратят время на обход модели, GRO нативно не льстит

3. **«Промт "brutal honest mirror" — это попытка получить за 10 строк то, что есть в GRO сразу»** — фрейм «нативная функциональность vs обход через prompt-инжиниринг»

### Content rubric — «GRO-style промты для самопроверки»

Если GRO запускает рубрику собственных промтов (см. paper [[evolving/content-trends/ai-news-channel-prompt-packs]] «что GRO может отсюда забрать»), эти промты должны **наследовать структуру brutal-honest contract**, но быть **GRO-фирменными**, не безликими:

- Использовать русскоязычные формулировки, в отличие от англоязычного 10639 (Дарья критиковала именно англицизмы в UGC-валидации)
- Не использовать «scientist with world's most prestigious award» — это authority-эскалация (см. [[evolving/content-trends/ai-news-channel-prompt-packs]] про эскалацию persona-priming), а использовать конкретные функциональные роли («GRO-наставник по карьерному росту»)
- Подчёркивать, что промт **разовый workaround**, а GRO — **structural solution**

### Anti-pattern для GRO

- **Не предлагать собственные anti-flattery промты «для ChatGPT»** — это рекламировало бы конкурента. Если GRO даёт промт, он должен быть **для GRO**, не для ChatGPT/Claude.
- **Не переводить промт 10639 на русский** буквально — это размыло бы дифференциацию (GRO стал бы «канал-куратор anti-flattery контента»). Промт упоминается как **внешнее доказательство тренда**, не как контент-актив GRO.
- **Не наезжать на «ленивых пользователей»**, которые копируют промты. Это враг-к-врагу-фрейминг: дешёво, но создаёт антипатию. Правильный фрейминг — «вы делаете правильно, что хотите honesty; вот более удобный способ её получить».

## Открытые вопросы

- **Срок жизни промта 10639 в RU инфо-поле** — ретвиты, репосты в других каналах. Нужен трекинг на следующих 2 ингестах @neuraldvig и других AI-каналов.
- **Появятся ли вариации?** Например, русскоязычные адаптации, или mid-tier модификации («brutal-honest but kind»). Если да — это сигнал созревания category.
- **Будут ли вендоры реагировать?** OpenAI/Anthropic могут (а) явно отказаться от «agreeable by default» (см. anthropic-публичное обсуждение Claude personality), (б) тонко перенастроить RLHF, (в) проигнорировать. Каждый сценарий по-разному влияет на длительность GRO-anti-flattery окна.
- **Cross-vertical resonance** — есть ли anti-flattery запрос в смежных вертикалях (digital coaching apps, productivity, mental health)? Если массовый запрос — общеотраслевой, GRO может позиционировать продукт как «category leader of anti-flattery».

## Связанные страницы

- [[evolving/content-trends/ai-flattery-dark-pattern]] — родительская страница про AI-лесть как dark pattern, теперь с 5-м tier валидации
- [[evolving/content-trends/ai-news-channel-prompt-packs]] — общий паттерн промт-подборок в @neuraldvig (anti-flattery — суб-формат)
- [[canon/positioning/gro-value-proposition]] — позиционирование GRO с якорем «спорит, но не отказывает»
- [[canon/product-knowledge/gro-app-overview]] — продуктовая механика, реализующая anti-flattery
- [[evolving/customer-feedback/gro-app-store-reviews]] — пользовательские отзывы, валидирующие anti-flattery восприятие
- [[sources/2026-05-14-tg-neuraldvig-may-5-12-2026]] — исходный источник с промтом 10639 (anti-flattery)
- [[sources/2026-05-19-tg-neuraldvig-may-13-19-2026]] — источник промта 10710 (anti-hallucination, вторая ось)
- [[sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026]] — оригинальный тезис Гуриновича про AI-лесть
- [[sources/2026-05-14-tg-gro-me-370-377]] — UGC Дарьи с verbatim валидацией anti-flattery позиции

## Backlinks

_Создана в этом ингесте; будут backlinks из обновляемых страниц ai-flattery-dark-pattern и ai-news-channel-prompt-packs._
