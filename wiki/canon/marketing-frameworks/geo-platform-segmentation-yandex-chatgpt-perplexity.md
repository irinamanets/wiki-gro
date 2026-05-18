---
id: mkt:canon/marketing-frameworks/geo-platform-segmentation-yandex-chatgpt-perplexity
title: "GEO-сегментация платформ: 3 разные retrieval-инфраструктуры (Яндекс Нейро / ChatGPT / Perplexity)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [seo, aeo, geo, ai-search, yandex-neuro, chatgpt, perplexity, retrieval-corpus, content-strategy, platform-strategy, ru-marketing]
confidence: high
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-18-pressfeed-geo-illusion-stability-measure.md]
namespace: mkt
---

# GEO-сегментация платформ: 3 разные retrieval-инфраструктуры

## TL;DR

Типичная ошибка маркетолога — действовать «универсально» в Яндекс Нейро, ChatGPT и Perplexity. У каждой системы — **своя retrieval-база и своя аудитория**. Контент-стратегия определяется **после** выбора аудитории, не до.

**Принципиальное правило:**

1. Сначала — **какая аудитория мне нужна?**
2. Потом — **в какой платформе/платформах эта аудитория?**
3. Только потом — **под какую retrieval-инфраструктуру строить контент?**

## Почему `canon`

Платформенная сегментация ландшафта AI-поиска — **архитектурный факт** в 2026 году. Конкретные доли долей платформ меняются (метрики живут в `evolving-strict/market-data`), **сам принцип «разные базы → разные стратегии»** стабилен. Мог бы измениться при глобальной конвергенции LLM-провайдеров на единую retrieval-инфраструктуру, но это пока невидно на горизонте 2–3 лет (Яндекс, Google, OpenAI, Anthropic, Perplexity — все строят независимые corpus'ы).

## Три платформы — три инфраструктуры

### 1. Яндекс Нейро / Алиса AI

| Параметр | Значение |
|---|---|
| **Retrieval-corpus** | Поисковая выдача Яндекса + Карты + Яндекс Бизнес + Дзен + региональные/новостные ресурсы + справочники организаций |
| **Аудитория** | Русскоязычная, российский контекст |
| **Что делает relevant** | Актуальная карточка в Я.Бизнесе, живые отзывы, локальные упоминания, присутствие в RU-СМИ и Дзен |
| **Слабые места** | Англоязычный контент эффекта не даёт; зарубежные ресурсы — почти невидимы |
| **Когда приоритет** | RU-аудитория (90%+ пользователей B2C, региональный B2B, локальный сервис) |

**RU-структурный приоритет**: Яндекс — единственный российский владелец всего decision-layer (retrieval + ranking + synthesis на [[evolving/industry-trends/ai-search-aeo-geo-2026|decision-layer-рамке]]). Для GRO как RU-приоритетного продукта — **№1 платформа**.

### 2. ChatGPT (с/без search)

| Параметр | Значение |
|---|---|
| **Retrieval-corpus** | Широкий public web: статьи, техническая документация, профессиональные медиа, тематические блоги (англоязычный массив > русскоязычного) |
| **Аудитория** | Глобальная (US/EU/global tech-community) |
| **Что делает relevant** | Системное присутствие в экспертном поле: исследования, методические материалы, ссылки от источников с репутацией (Medium, профильные tech-блоги, Wikipedia) |
| **Слабые места** | Русскоязычная статья здесь **эффекта не даёт** напрямую (только если переведена/охвачена англоязычным retrieval) |
| **Когда приоритет** | Глобальная B2B-аудитория, cross-border SaaS, tech-community, founder-positioning |

**Wikipedia как 47.9% источников ChatGPT** ([[evolving/content-trends/aeo-geo-llm-search-optimization-2026|Кумар Виас]]) — отдельный лever для ChatGPT-стратегии.

### 3. Perplexity (live web search)

| Параметр | Значение |
|---|---|
| **Retrieval-corpus** | **Живой web-поиск** при каждом запросе — выбирает из актуальных страниц, не из заранее обученной модели |
| **Аудитория** | Глобальная + RU (растущая prosumer-tier для research-задач) |
| **Что делает relevant** | **Свежесть** + **фактурность** материала; конкретные цифры, чёткие утверждения, проверяемые данные. Накопленный авторитет домена менее важен. |
| **Слабые места** | Long-term seeding-стратегия (как для ChatGPT) даёт меньше отдачи; нужна **content-recency**. Один устаревший пост может «стереть» бренд из ответа. |
| **Когда приоритет** | Research-heavy B2B, аналитика, fact-checking, специализированные категории, где «свежесть данных» = competitive moat |

**Reddit как 46.7% источников Perplexity** ([[evolving/content-trends/aeo-geo-llm-search-optimization-2026|Кумар Виас]]) — отдельный lever для Perplexity-стратегии.

## Compare matrix

| Критерий | Яндекс Нейро | ChatGPT | Perplexity |
|---|---|---|---|
| Аудитория | RU | Global | Global + research-prosumer |
| Корпус | Я.Бизнес + Дзен + СМИ + Карты | Public web (en-heavy) | Live web (recency-bias) |
| Содержание лучших постов | Локальное, фактурное, отзывы | Экспертно-методическое, кейсы | Свежее, числовое, аргументированное |
| Authority | Высокий | Высокий | Низкий (recency > authority) |
| Recency | Средний | Низкий (training cutoff) | **Высокий** |
| Long-term seeding | Эффективно | **Очень эффективно** | Меньше (старый контент не цитируется) |
| Канонический seeding-mix | Я.Бизнес + Дзен + RU-СМИ + Карты | Medium + Reddit + Wikipedia + vc.ru/Habr | Reddit + recent published articles + news |

## Operational playbook — 3 параллельных track

### Yandex Track (RU-приоритет)

- **Я.Бизнес** — карточка организации, регулярные обновления, ответы на отзывы
- **Дзен** — экспертные статьи команды, регулярная публикация (1–2/мес)
- **RU-СМИ** — выходы на vc.ru, Habr, профильные отраслевые издания
- **Pressfeed/Hara-Kiri** — PR-targeted seeding в журналистский pool (см. [[canon/marketing-frameworks/performance-pr-framework]])
- **Карты** — синхронизация с Я.Картами для local SEO

### ChatGPT Track (Global, long-term)

- **Medium** — authored-посты founders на английском (1–2/мес)
- **Reddit** — нативные комментарии в r/selfimprovement, r/productivity, r/Entrepreneur (для GRO)
- **Wikipedia presence** — для зрелого бренда долгосрочная цель: попасть в Wikipedia как notable entity в категории
- **Profession-aligned tech blogs** — гостевые статьи в нишевых медиа
- **Long-form research** — белые бумаги, отчёты — попадают в pre-training через years

### Perplexity Track (Recency-focused)

- **Recent published articles** — новости/обновления продукта в news-формате, чтобы попадали в свежий web
- **Reddit** — те же subs, но с фокусом на **свежие** треды
- **News/PR с конкретикой** — числа, бенчмарки, проверяемые факты в анонсах
- **Frequent content cadence** — нельзя сделать раз и забыть; нужна непрерывная content-стрелка

## Anti-patterns

1. **Универсальная content-стратегия для всех 3 платформ** — главная типичная ошибка. Один и тот же материал работает по-разному в трёх корпусах.
2. **Английский Medium-пост в надежде попасть в Яндекс Нейро** — ChatGPT-канал, не Яндекс. Языковой mismatch критичен.
3. **Russian-only-стратегия для глобальной B2B-аудитории** — теряете ChatGPT/Perplexity/Gemini для tech-decision-makers и cross-border SaaS-категорий.
4. **Long-form seeding в Perplexity** — Perplexity берёт live web, не накопленный корпус. Нужна **recency-стратегия**, не authority.
5. **Игнорировать Карты/Я.Бизнес для local-business** — для медицины, услуг, retail — это **главный** канал в Яндекс Нейро.

## Связь с GRO

GRO — **RU-приоритетный продукт с глобальными перспективами для tech-/founder-аудитории**. Соответственно:

1. **Priority 1: Yandex Track** — Я.Бизнес + Дзен + RU-СМИ (vc.ru, Habr) + Pressfeed-seeding. Это **core** канал для большинства потенциальных клиентов GRO в 2026.
2. **Priority 2: ChatGPT Track** — Medium founders + Reddit r/selfimprovement/Entrepreneur, для долгосрочной cross-border позиции в категории «продукты для развития мышления». Slower, but compounds.
3. **Priority 3: Perplexity Track** — recurring news про продукт (release notes, исследования внутри GRO-команды, метрики использования), на vc.ru и Habr с recency-focus. Менее приоритет, но недорого.

Connected пейджи:
- [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] — для каждого из 3 track'ов нужен **отдельный** контрольный список запросов и monitoring loop
- [[canon/marketing-frameworks/stochastic-llm-ranking-sparktoro]] — внутри **каждой** платформы probability работает независимо; высокое присутствие в Яндексе ≠ высокое в ChatGPT
- [[canon/positioning/gro-value-proposition]] — value-prop переупаковывается под каждый track

## Связанные страницы

- [[canon/marketing-frameworks/stochastic-llm-ranking-sparktoro]] — стохастичность как foundation измерения по каждой платформе
- [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] — операционный monitoring (запросы × платформы)
- [[canon/marketing-frameworks/seo-for-ai-era-playbook]] — общий playbook AI-эпохи
- [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] — онтологическая рамка retrieval'а
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — родительский content-trend (Шевченко 3 механизма + Кумар Виас доли)
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — родительский industry-trend (decision-layer)
- [[evolving/content-trends/geo-playbook-2026-q2]] — operational playbook Кумар Виас
- [[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026]] — RU practitioner consensus
- [[evolving-strict/market-data/alice-ai-usage-breakdown-2026]] — RU-метрики использования Алисы
- [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]] — первоисточник 3-платформенной сегментации
