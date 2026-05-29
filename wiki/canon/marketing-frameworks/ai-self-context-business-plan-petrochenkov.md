---
id: mkt:canon/marketing-frameworks/ai-self-context-business-plan-petrochenkov
title: "AI self-context business-plan: загрузи весь контекст → получи полный Playbook (Петроченков)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [framework, petrochenkov, ai, llm, business-plan, playbook, claude-project, chatgpt-project, founder-tools, prompt-engineering, ai-as-strategy-pilot]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-petrochenkow-20260526-112500.md]
namespace: mkt
---

# AI self-context business-plan (Петроченков)

Operational методология: **загрузить в LLM-проект весь контекст о себе и своём бизнесе** (telegram-канал, продукт, рынок, клиентские кейсы, **полный ОПиУ**), задать **founder-level задачу с конкретным числом и сроком** — получить **полный Playbook нового продукта** (а не гипотезы). По Антону Петроченкову ([[sources/2026-05-26-tg-petrochenkow-20260526-112500|пост 1306, 2026-05-25]]):

> «Сижу, пялюсь в экран и думаю: "А че, так можно было?". В общем, неожиданно для себя я, вместо разбиения очередного мифа, получил вполне себе реалистичный план действий с уникальным для рынка продуктом» `[conf:medium, src:2026-05-25]`.

`confidence: medium` — inferred-эксперт (Petrochenkov как founder performance-агентства, **5-й independent operational пост про AI** за 2 месяца — устойчивый knowledge-asset), но **single-shot observation** без cross-author triangulation. Применимость к чужим founder-сетапам **не верифицирована** (зависит от качества входного контекста).

## TL;DR

> ИИ как «второй пилот опытного маркетолога» (см. [[evolving/industry-trends/ai-marketing-limits-2026]]) — это **performance-level применение**. Этот фрейм — **strategy-level extension**: LLM с **полным self-context** генерирует не гипотезы, а **полный operational playbook нового продукта** включая P&L, скрипты, календарь, юр-предупреждение. Конверсия гипотез в playbook происходит **на стороне модели**, не на стороне founder'а. Условие: **качество загруженного контекста** + **правильно сформулированный вопрос с числом и сроком**.

## 4-шаговая методология

### Шаг 1 — создать **проект** (workspace)

Используется **проект** LLM-сервиса (Claude Project или ChatGPT Project на момент 2026):
- Persistent file storage (загруженные документы сохраняются между сессиями).
- Custom instructions / system prompt уровня проекта.
- Чаты в проекте имеют доступ ко всем загруженным файлам.

> Petrochenkov не называет конкретный сервис в посте — формулирует как обобщённый «проект» с возможностью загрузки нескольких документов и совместной работы. По состоянию на май 2026 пригодны: Claude Projects, ChatGPT Projects, Notion AI Workspace, Gemini Gem.

### Шаг 2 — загрузить **весь self-context**

По Petrochenkov-эксперименту (буквальный список):

1. **Весь telegram-канал автора** (export как набор постов или транскрипт через бот) — content-stylа voice, экспертные тезисы, audience signals.
2. **Кейсы клиентов** (cases, успехи, провалы, конкретные цифры результатов).
3. **Полное описание продукта** (что продаём, кому, как доставляем).
4. **Исследование рынка** (TAM/SAM, конкурентный ландшафт, тренды).
5. **Весь ОПиУ (отчёт о прибылях и убытках)** — **финансовая прозрачность критична**, потому что без неё P&L нового продукта будет hallucinated.

**Принцип:** «всё, что ты знаешь о себе и своём бизнесе — скорми». **Не пытаться курировать «что важно»** — это делает selection bias, который ломает контекст.

### Шаг 3 — сформулировать founder-level задачу

Формулировка Петроченкова (paraphrase):

> «Создать план заработка **XXX евро чистыми** на **абсолютно новом продукте** за **7 дней**».

**Структурные элементы хорошей founder-задачи:**

1. **Конкретное число** (XXX евро / млн ₽) — не «увеличить выручку», а измеримое целевое значение.
2. **Чистое значение** (после costs / refunds / комиссий) — это форсит модель посчитать P&L реально, а не gross.
3. **Абсолютно новый продукт** — снимает inertia, не даёт модели взять «упростить существующий». Это **creative-forcing constraint**.
4. **Конкретный срок** (7 дней) — short timeframe форсит scrappy-execution playbook (без квартала бренд-кампании, без агентств), что подходит founder'у.
5. **Режим совместной работы** — модель не выдаёт готовое решение, а спрашивает уточнения и строит план итеративно.

**Anti-pattern формулировок** (которые ломают результат):
- «Помоги мне с маркетингом» — слишком абстрактно
- «Сделай контент-план» — слишком узко (исключает offer, P&L, scripts)
- «Создай 10 идей бизнеса» — модель уходит в hypothesis-generation вместо operational planning
- «Без конкретных цифр» — модель не считает P&L, выдаёт качественный нарратив

### Шаг 4 — получить **полный Playbook** (не гипотезы)

Результат Petrochenkov-эксперимента — 11 deliverables:

1. **Ядро оффера** (centralcore value proposition в одной формуле)
2. **Подробное описание продукта** (как доставляется, сроки, формат)
3. **JTBD** (для кого, в какой ситуации, какой Job)
4. **Сравнение с конкурентами** (с матрицей)
5. **PNL** (P&L расчёт — выручка, costs, margin, breakeven, timing)
6. **Скрипт эфира** (для live launch / запуск через стрим)
7. **Планы постов в соцсетях** (по каналам, по фазам)
8. **Скрипты дожима** (sales-followup сценарии для не-купивших)
9. **Расчёт затраты личных нормочасов** (founder time budget)
10. **Календарь** (по дням × шагам — что когда делать)
11. **Чек-лист запуска** (операционный freshman checklist)

**+ Автоматическое предупреждение о юридических рисках** (даже не запрошенное — модель сама указала, что некоторые механики рискованны с т.з. ФЗ).

Эта **полнота** — то, что вызвало у Петроченкова реакцию «А че, так можно было?». Это **strategy-level competence** LLM при условии достаточного контекста.

## Метаправило: «правильный вопрос — это 50% правильного ответа»

Petrochenkov-meta-formulation:

> «Это высокоуровневая галлюцинация ИИ? Или очередное подтверждение правила: правильно заданный вопрос — это 50% правильного ответа?» `[conf:medium, src:2026-05-25]`

**Petrochenkov-гипотеза:** результат — **не галлюцинация**, а **операционно валидный playbook**, потому что:

1. **Контекст был полный** (см. Шаг 2) — модель не выдумывала факты, она компоновала из загруженных.
2. **Задача была чётко формулирована** (см. Шаг 3) — не abstract, а с числом и сроком.
3. **Founder с production-опытом** (Petrochenkov) **может оценить операционную валидность** результата (от opинеnя «галлюцинация» до «реалистичный план»).

Это **пересекается с другими canon-фреймами** про prompt-quality:
- [[evolving/content-trends/anti-flattery-prompt-canon-2026]] — anti-pattern user-промтов, портящих результат
- [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] — структурированный input как leverage над LLM-выводом

## Что отличает этот фрейм от обычного «AI помощник»

| Параметр | Обычное использование LLM | Self-context business-plan фрейм |
|---|---|---|
| Контекст | Только текст промта (1-2 абзаца) | **Весь founder-knowledge** (мегабайты загруженных данных) |
| Цель | Гипотезы, идеи, варианты | **Готовый operational playbook** |
| Уровень | Tactical (контент, идея заголовка) | **Strategy + tactical вместе** (от ядра оффера до календаря) |
| P&L | Не считается | **Calculated с реальными costs founder'а** |
| Юр-риски | Не учитываются | **Surface'аются автоматически** |
| Время на input | 5-30 минут (написание промта) | **2-5 часов** (сбор и загрузка контекста) + 30 минут на правильный вопрос |
| Time on output | Минуты | **Минуты** (после загрузки) — leverage огромный |
| Replicability | Per-conversation | **Per-project** (один раз настроил → переиспользуется для новых продуктов) |

**Asymmetric ROI:** инвестировал 4 часа в сбор и загрузку контекста + 30 минут на правильный вопрос → получил playbook нового продукта стоимостью **бизнес-консалтинговой работы 50-200 часов**. Это **leverage ~100×**.

## Operational эвристики (практическое применение)

### Для founder'а с устоявшимся бизнесом:

1. **Один раз настроить self-context project** в LLM-сервисе. Это **infrastructure investment**, не одноразовая трата.
2. **Регулярно обновлять контекст** — добавлять новые посты канала, новые кейсы, новые P&L периоды. Контекст «стареет» с каждой неделей.
3. **Запросы формулировать как founder-задачу с числом + сроком** (см. Шаг 3).
4. **Не пропускать ОПиУ** — без P&L модель будет hallucination'ить unit economics нового продукта.
5. **Использовать как стратегический спарринг-партнёр**, не как замену собственного thinking.

### Для GRO-команды:

Это **applicable как операционный инструмент** для:
- Анализа new-product hypothesis (если рассматриваем расширение в Тариф2 / Интенсив-расширение)
- Quarterly strategy planning (после обновления project с Q-результатами)
- Pricing experiments (с подачей контекста customer feedback + competitor data)

Caveat: **не использовать для продаваемого контента без редактуры** — даже валидный playbook требует human-edit под voice бренда + проверки конкретных claims.

## Limits и failure modes

### Где этот фрейм НЕ работает:

1. **Founder без production-опыта** — не сможет оценить операционную валидность. Модель выдаст красивый playbook, который **выглядит реалистично, но не работает на рынке**. Нет внутреннего bullshit-detector → результат: «инфобиз-фишка с AI».
2. **Не полный контекст** — если ОПиУ не загружен или customer-кейсы абстрактны, модель **заполняет пробелы средним по индустрии** = playbook бесполезен для конкретного бизнеса.
3. **Старый контекст** — если данные в проекте старше 6 месяцев, выводы могут быть на устаревшем foundation (market data, конкуренты, регуляторика).
4. **Регулируемые ниши без юр-консультации** — модель выдаёт юр-warning, но **юристом не заменяет**. Финансовый, медицинский, образовательный сектора требуют post-AI юр-review.
5. **Sensitive PII в контексте** — нельзя загружать personal data клиентов, переписки сотрудников, contracts с counterparty-NDAs (см. `wiki/rules.md` про sensitive content).

### Risk-of-overconfidence ↔ rule «правильный вопрос — 50% ответа»

Этот фрейм работает **именно потому**, что founder ставит правильный вопрос и **может оценить ответ**. Если оба условия не выполнены — фрейм становится **classic инфобиз-trap** (Petrochenkov явно отделяет свой эксперимент от «инфобизовой фишки» через результат-проверку):

> «Решил проверить в реальности одну из самых распространённых инфобизовых фишек на рынке — реальный заработок денег на искусственном интеллекте» → результат: **playbook реалистичен, но Petrochenkov может его оценить как opытный founder**.

→ **Метаусловие фрейма: founder с операционной экспертизой, способный оценить валидность output'a**. Без этого условия фрейм неотличим от того, что критикует [[canon/marketing-frameworks/respectable-infobiz-rybakov|респектабельный инфобиз]].

## Связь с другими canon-фреймами

- [[evolving/industry-trends/ai-marketing-limits-2026]] — sibling рамка performance-уровня (этот фрейм — её strategy-extension). Petrochenkov consistent в обоих: AI = leverage опытного, multiplier ошибок слабого.
- [[canon/marketing-frameworks/ai-content-marketing-delegation-frame-lz-media]] — параллель в content-marketing зоне (LZ.Media-формула): AI ≠ замена редактора, AI = инструмент опытного.
- [[canon/marketing-frameworks/ai-persona-usability-test-petrochenkov]] — соседний AI-tool того же автора: synthetic-persona-usability test, тоже tactical (не strategy), но того же founder-tooling-семейства.
- [[canon/marketing-frameworks/cpa-calculator-pre-launch-roi]] — pre-launch ROI calc Петроченкова, который этот playbook автоматизирует / расширяет.
- [[canon/marketing-frameworks/respectable-infobiz-rybakov]] — anti-pattern: инфобиз-обещание «AI заработает за тебя». Различие — в наличии founder-экспертизы для оценки результата.
- [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] — структурный input как leverage над LLM-выводом (как self-context project укладывается в onto-retrieval framework).

## Caveats

- **Single-author observation.** Только один эксперимент Petrochenkov без cross-author triangulation. Нужна верификация: повторят ли другие founders RU performance-сообщества с тем же качеством результата.
- **«Полный Playbook» — Petrochenkov-категоризация.** Объективно мы не видели сам output (closed proprietary content); только список 11 deliverables по Petrochenkov-описанию. Реальное качество каждого deliverable нужно verify на cases других founders.
- **«XXX евро» намеренно занумерован.** Конкретное целевое число Petrochenkov убрал из публикации. Это норма для founder content, но для оценки feasibility playbook'а — слепое пятно (€10K и €1M — разные playbook).
- **Time-to-execute не указан.** Petrochenkov не пишет, исполнил ли он сам этот playbook за 7 дней. Возможно, playbook остаётся как hypothetical reference — это снижает «доказанность» рамки.
- **TTL — calibrate за 6 мес.** Frontier LLM models (Claude 4.x, GPT-5.x) меняются каждые 3-6 месяцев. Качество self-context-playbook'а **будет расти**, а не падать. Через 6 мес calibrate, насколько threshold founder-экспертизы снизился.

## Связанные страницы

- [[evolving/industry-trends/ai-marketing-limits-2026]] — sibling performance-фрейм того же автора
- [[canon/marketing-frameworks/ai-persona-usability-test-petrochenkov]] — соседний tactical AI-tool того же автора
- [[canon/marketing-frameworks/ai-content-marketing-delegation-frame-lz-media]] — параллель в content-marketing
- [[canon/marketing-frameworks/respectable-infobiz-rybakov]] — anti-pattern фрейма
- [[canon/marketing-frameworks/cpa-calculator-pre-launch-roi]] — pre-launch ROI rationale, который playbook автоматизирует
- [[sources/2026-05-26-tg-petrochenkow-20260526-112500]] — первоисточник
