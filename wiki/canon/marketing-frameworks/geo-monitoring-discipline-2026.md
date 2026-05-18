---
id: mkt:canon/marketing-frameworks/geo-monitoring-discipline-2026
title: "GEO-мониторинг: дисциплина измерения видимости в AI-выдаче"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [geo, aeo, ai-search, monitoring, analytics, brand-visibility, kravchenko, share-of-voice, llm-citation]
confidence: medium
stale: false
created: 2026-05-18
updated: 2026-05-18
sources: [sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data.md, sources/2026-05-14-tg-solokumi-may-2026.md]
namespace: mkt
---

# GEO-мониторинг как отдельная маркетинговая дисциплина

В классическом SEO-периоде измерение видимости = позиция в Google/Yandex SERP. В AI-эпохе это **уже не отражает реальную видимость**: пользователь получает ответ от AI, и попадание на первое место в классической выдаче ничего не значит, если бренда нет в **пуле источников, которые цитирует модель**.

> «Традиционный SERP больше не отражает реальную видимость. Бизнесу необходимо внедрять GEO-мониторинг: отслеживать, входит ли бренд в пул источников для целевых запросов и как именно его цитирует модель. Если компания не попадает в ответ ИИ, первое место в классическом поиске не имеет значения.»
>
> — В. Кравченко, Insight Analytics, Pressfeed май 2026

## Почему `canon`

Дисциплина «измерять видимость в AI-ответах» — это **стабильная функция маркетинга** в AI-эпохе, аналогичная классическим SEO-tracking-практикам. Конкретные **инструменты** меняются (Llmspot, GEO Tracker AI, audit.algomizer.com — могут устареть за год), **операционная дисциплина измерения** — нет. Связка с tooling-уровнем — через [[evolving/content-trends/geo-playbook-2026-q2|механику VI Кумар Виас]] (там список конкретных tools).

## Что отслеживать (фреймворк измерения)

GEO-мониторинг измеряет **четыре независимых измерения** видимости бренда в AI-ответах:

| Измерение | Вопрос | Метрика | Частота |
|---|---|---|---|
| **1. Inclusion** | Входит ли бренд в pool источников для целевых запросов? | Share-of-voice (доля упоминаний из общего числа AI-ответов на список запросов) | weekly |
| **2. Citation quality** | Как именно цитирует модель — точно, в нужном контексте, без искажения? | Manual review citation samples (5–10/запрос) | monthly |
| **3. Competitive parity** | Кого ещё цитирует AI по тем же запросам? Какова доля голоса конкурентов? | Competitive share-of-voice analysis | monthly |
| **4. Trend over time** | Растёт или падает наша доля? Появляются новые конкуренты? | Time-series по share-of-voice | monthly + alerts |

### Inclusion: контрольный список запросов

Для каждого продукта/бренда сформировать **контрольный список 15-30 целевых запросов**, по которым нужно появляться в AI-выдаче. Для GRO примеры:

- _«Приложение для тренировки предпринимательских навыков»_
- _«Как тренировать переговоры без тренера»_
- _«Альтернатива курсам по soft skills в 2026»_
- _«Методика ежедневной рефлексии для фаундера»_
- _«AI-приложение для развития мышления»_
- _«Как развить менеджерские навыки самостоятельно»_

(см. [[canon/positioning/gro-value-proposition]] для полного списка)

Запускать каждый запрос **через 4-6 AI-платформ** еженедельно:
- ChatGPT (с/без search)
- Claude
- Gemini
- Perplexity
- Алиса AI (Yandex)
- Google AI Overviews

Логировать в spreadsheet:
- Дата
- Платформа
- Запрос
- Упомянут ли бренд? (Y/N)
- Позиция в списке упоминаний (1, 2, 3+)
- Контекст цитирования (positive, neutral, negative)
- Конкуренты в том же ответе

### Citation quality: что мониторить

Не каждое упоминание — хорошее упоминание. Citation quality оценивается по 4 осям:

1. **Точность** — модель цитирует факты о продукте корректно (цена правильная, фичи правильные)
2. **Контекст** — упоминание соответствует JTBD пользователя, а не «случайный пример»
3. **Авторитетность** — модель ссылается на корпоративный источник vs. третий обзорщик
4. **Recency** — модель цитирует актуальные данные vs. устаревшие (старая цена, удалённая фича)

**Negative findings — типичные**: устаревшая цена, исчезнувшая фича указана как актуальная, конкурент упомянут в более позитивном свете, бренд упомянут только в негативном кейсе.

### Competitive parity: share-of-voice

Для каждого целевого запроса считать **долю упоминаний бренда среди всех упоминаний** в AI-ответах.

| Метрика | Формула |
|---|---|
| Share-of-voice (SoV) | `(упоминания бренда) / (общее число упоминаний всех брендов) × 100%` |
| First-mention rate | `(запросы где бренд упомянут первым) / (всего запросов) × 100%` |
| Co-mention pattern | Список брендов, которые AI **регулярно упоминает рядом** с нашим |

Co-mention pattern — особенно важная метрика: если AI регулярно упоминает GRO рядом с курсами Skillbox/Нетологии — это бенчмарк, относительно которого AI «понимает» GRO. Если рядом с медитационными приложениями — это **репозиционирование**, нужно корректировать content/data.

### Trend over time: alerts

Настроить алёрты на:
- Падение SoV > 20% week-over-week
- Появление нового конкурента в топ-5 co-mentions
- Изменение citation quality (например, начали цитировать негативно)
- Исчезновение из ответа по запросам, где бренд был стабильным top-3

## Tooling (инструментальный слой)

Конкретные инструменты — это **evolving**-уровень (меняются с темпом 6-12 месяцев). Подробный обзор tools — в [[evolving/content-trends/geo-playbook-2026-q2|плейбуке Q2 2026]] механика VI. Краткая таблица для контекста:

| Инструмент | Что делает | Cost (Q2 2026) | Best for |
|---|---|---|---|
| GEO Tracker AI | Tracking упоминаний в ChatGPT/Perplexity | $$ | Регулярный mass-monitoring |
| audit.algomizer.com | One-shot аудит видимости | free | Baseline / sanity-check |
| Llmspot | Глобальный AI visibility tracker | $$ | Multi-platform consolidated view |
| Ahrefs Brand Radar | Module к Ahrefs для AI | $$$ | Если уже на Ahrefs |
| Пиксель Тулс (RU) | Алиса + RU AI-поисковики | $$ | RU-фокус (важно для GRO) |
| Custom prompt-runner | Скрипт, гоняющий список запросов через API | low | Cost-conscious / кастомные метрики |

Для GRO рекомендуется combo: **Пиксель Тулс** (RU coverage с Алисой) + **GEO Tracker AI** (ChatGPT/Perplexity для cross-border аудитории) + **custom prompt-runner** для еженедельной автоматизации.

## Operational playbook (минимальный first-pass)

Минимальный GEO-monitoring проект для команды маркетинга — **2 недели на запуск**:

| Шаг | Артефакт | Время |
|---|---|---|
| 1. Сформировать контрольный список 15–30 запросов | Spreadsheet с targeting list | 4 ч |
| 2. Запустить baseline через audit.algomizer.com (free) | Текущий snapshot видимости | 30 мин |
| 3. Запустить ручной прогон через 4-6 AI-платформ | Baseline spreadsheet | 4 ч |
| 4. Настроить weekly cadence в календаре + ответственный | Process doc | 1 ч |
| 5. Настроить tool (GEO Tracker AI или Пиксель Тулс) | Account + integration | 4 ч |
| 6. Настроить алёрты на падение SoV | Threshold definitions | 2 ч |
| 7. Первый weekly review через 2 недели | Trend snapshot | 2 ч |

**Минимальный team setup:** один marketing analyst как owner процесса, content/SEO-lead на еженедельный review.

## Связь с другими дисциплинами маркетинга

| Дисциплина | Что даёт GEO-monitoring | Что забирает у GEO-monitoring |
|---|---|---|
| **Content marketing** | Свежий список тем (запросы, по которым AI ищет, но GRO не упоминают) | Идеи под seeding на трастовые ресурсы |
| **PR** | Цели for seeding (Reddit, Habr, vc.ru, профильные СМИ) | Метрики эффективности PR-программы за пределами media-mentions |
| **Product** | Сигналы об упоминании устаревших фич / неточных параметров | Приоритизация product-data updates |
| **Analytics** | Новый канал attribution: «откуда узнали о бренде» | Воронка от AI-mention к регистрации |
| **Sales** | Customer feedback: какой контекст AI даёт о бренде первым клиентам | Talking points для скрипта |

## Anti-patterns

1. **Мониторить только positive citations.** Negative и neutral citations — тоже сигнал; нужно оценивать все.
2. **Использовать только один tool.** Каждый tool покрывает свой набор моделей; multi-tool combo даёт полную картину.
3. **Запускать раз в месяц.** AI-retrieval быстро меняется; weekly cadence — минимум для актуальной картины.
4. **Не логировать конкурентов.** Без competitive parity нельзя оценить, плохо ли бренду или плохо всей категории.
5. **Игнорировать citation quality.** «Упоминается» ≠ «упоминается хорошо». 100% inclusion с негативным контекстом хуже 50% inclusion с положительным.
6. **Делать без действия.** Мониторинг без operational loop (что мы делаем при падении SoV?) — пустая трата ресурса. Нужна связка с content/PR/product action items.

## Связь с GRO

Для GRO как продукта раннего этапа AI-visibility критична:

1. **Baseline-аудит:** какие из 20+ продуктовых запросов GRO уже упоминается AI? Скорее всего, < 20% (большинство платформ ещё не индексировали или не цитируют активно).
2. **Competitive landscape:** кого AI рекомендует **вместо** GRO по запросам про «развитие мышления»? Это бенчмарк для content/PR-программы.
3. **Citation quality:** если AI упоминает GRO, какой контекст даёт? Тренировка для предпринимателей vs. soft skills vs. медитация — это разные позиционирования.
4. **Trend tracking:** месячный track, как меняется SoV после каждой content/PR-инициативы — единственная объективная метрика эффективности GEO-инвестиций.
5. **Связь с [[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026|RU practitioner playbook]]:** DiaClass отчитывался о 10% трафика из ChatGPT/Perplexity — это **достижимый бенчмарк** для нишевого SaaS, если запустить GEO-monitoring и operational loop.

## Связанные страницы

- [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] — концептуальная пара (что оптимизировать в данных)
- [[canon/marketing-frameworks/product-data-as-architecture-pragmatix]] — связанная рамка (Indig: «маркетинг = архитектура данных»)
- [[canon/marketing-frameworks/seo-for-ai-era-playbook]] — общий playbook
- [[evolving/content-trends/geo-playbook-2026-q2]] — детальный tools-уровень (механика VI)
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — родительский content-trend
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — родительский AEO/GEO-тренд
- [[evolving/industry-trends/ai-search-product-discovery-layer-2026]] — decision-layer контекст
- [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]] — benchmarks (Faire +40%, booking +15%/+30%)
- [[canon/positioning/gro-value-proposition]] — список запросов для GRO-мониторинга
- [[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026]] — RU practitioner-консенсус с примерами
- [[sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data]] — первоисточник тезиса
- [[sources/2026-05-14-tg-solokumi-may-2026]] — Кумар Виас, дополнительные инструменты
