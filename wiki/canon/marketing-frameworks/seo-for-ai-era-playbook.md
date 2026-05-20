---
id: mkt:canon/marketing-frameworks/seo-for-ai-era-playbook
title: "SEO для AI-эпохи: практический плейбук"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [seo, ai, content, pr, geo, aeo, faq-schema, llms-txt, robots-txt, e-e-a-t, entity, vector-search, json-ld, kravchenko]
confidence: medium
stale: false
created: 2026-04-16
updated: 2026-05-19  # +Pressfeed/Kovpak: local-media publications as SEO long-tail assets (городские порталы как domain-authority boost + индексация локальных запросов 6+ мес)
sources: [sources/2026-04-16-condense-pressfeed-35-articles.md, sources/2026-05-14-tg-solokumi-may-2026.md, sources/2026-05-18-pressfeed-13-cases-ai-search-adaptation.md, sources/2026-05-18-pressfeed-pragmatix-ai-data-over-landing.md, sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data.md, sources/2026-05-18-pressfeed-geo-illusion-stability-measure.md, sources/2026-05-19-pressfeed-kovpak-local-media-sales-funnel.md]
namespace: mkt
---

# SEO для AI-эпохи: практический плейбук

Reusable методология оптимизации контента под нейроответы поисковых систем (AEO/GEO). Стабильные рекомендации, не привязанные к конкретной платформе.

## Наиболее эффективные форматы для попадания в нейроответы

1. **Гайды и инструкции** -- пошаговые how-to с чёткой структурой
2. **Обзоры и сравнения** -- структурированные таблицы, списки «за/против»
3. **Кейсы и разборы** -- конкретные примеры с числами и результатами
4. **FAQ** -- прямые вопросы и ответы

## Принцип «Answer first» (перевёрнутая пирамида)

Статья в начале даёт краткий ответ на главный вопрос, затем раскрывает подробности. AI-системы выдёргивают первые абзацы как сниппет -- именно там должен быть ответ.

## Кластерный подход

Кластеры контента по смежным вопросам повышают доверие нейросетей к источнику как экспертному. Одна страница -- один вопрос, но множество связанных страниц формируют «экспертный профиль домена».

## Микроразметка

Schema.org / JSON-LD с тегами:
- `FAQPage` -- для FAQ-страниц
- `HowTo` -- для инструкций
- `NewsArticle` -- для новостных материалов
- `Review` -- для обзоров
- `Product` / `Offer` / `Brand` -- для коммерческих сущностей (Кравченко, Insight Analytics, май 2026 — Faire case +40% упоминаний в AI-Overviews после расширения этой группы)
- `Person` -- для профилей экспертов (E-E-A-T)

Помогает ботам парсить контент и корректно цитировать.

### JSON-LD как преимущественный формат

По [[sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data|Кравченко (Insight Analytics, май 2026)]]:

> «JSON-LD остаётся самым удобным способом передачи структурированных данных. Он не перегружает HTML и позволяет передавать сложные иерархии. В условиях динамических AI-обзоров скорость и чистота передачи данных становятся конкурентным фактором.»

Operational guideline:

| Формат | AI-retrieval приоритет | Когда выбирать |
|---|---|---|
| **JSON-LD в `<head>`** | **высший** | По умолчанию для всех новых сайтов и при рефакторинге |
| Microdata (HTML inline) | средний | Legacy-страницы, где JSON-LD сразу не внедрить |
| RDFa | низкий | Редко используется, не оптимален для AI |
| Open Graph | вспомогательный | Дополнение к JSON-LD для соцсетей |

Динамические AI-обзоры (Google AI Overviews, ChatGPT search, Алиса AI) делают real-time запросы к продуктовым страницам в момент формирования ответа — чем чище и быстрее парсится разметка, тем выше шанс попадания в ответ.

### Архитектурный, не точечный апгрейд

> «Компании нужен не точечный апгрейд, а перестройка инфраструктуры сайта. Генеративный поиск требует машиночитаемой модели данных — на уровне архитектуры, а не отдельных страниц.»
>
> — Кравченко, Insight Analytics

Менеджерская рамка приоритизации бюджета:

| Категория работы | Кто отвечает | Бюджетная категория |
|---|---|---|
| Добавить FAQ-блок в существующий лендинг | Content / SEO-team | opex (точечный) |
| Перестроить data-pipeline (CMS → API → JSON-LD endpoint) | Product / Engineering / Data | **capex** (архитектурный) |
| Обеспечить inventory real-time sync | Engineering + DevOps | **capex** (инфраструктура) |
| Внедрить мониторинг видимости в AI | Marketing analytics + Data | opex (новый функционал) |

Без capex-слоя точечные content-улучшения упираются в потолок неполных данных. Полная рамка — [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]].

### Inventory accuracy как relevance criterion

Если на сайте указано наличие товара, которого уже нет, AI фиксирует недостоверность и помечает домен как устаревший источник для категории — downgrade ranking **всего домена**, не только страницы. Real-time inventory sync с JSON-LD-разметкой — обязательная инфраструктурная компонента. Подробнее — [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] раздел «Inventory accuracy».

## Технические настройки

- Добавить сайт в Яндекс.Вебмастер, Google Search Console и Bing Webmaster Tools
- В `robots.txt` снять ограничения для: `ChatGPT-User`, `PerplexityBot`, `YandexBot`, **`GPTBot`**, **`ClaudeBot`** (обязательный must-allow чек по солокуми 405)
- **`llms.txt`** в корне сайта — новый файл, объясняющий AI-краулерам структуру контента. Генератор: [llmstxt.firecrawl.dev](https://llmstxt.firecrawl.dev/) (см. [[evolving/content-trends/geo-playbook-2026-q2]] механика III)
- Убедиться, что AI-боты могут индексировать контент (не блокированы WAF/CDN)

## Калибровка «answer-first» через измеренные доли цитирования

Принцип «answer first» становится квантифицируемым: **44.2% всех AI-цитат — из первых 30% страницы; ответ в первых 50 словах даёт +40% к цитируемости** (см. [[evolving/content-trends/geo-playbook-2026-q2]]). Это не оценка, а measured доля распределения. Поэтому правило формализуется так:

- **Первые 50 слов** — прямой ответ на главный вопрос юзера, без воды
- **Следующие 30% страницы** — самая ценная плотность фактов и ссылок
- **Остаток (70%)** — расширения, кейсы, FAQ, технические детали

## E-E-A-T через профили экспертов с верифицированными материалами

Дополнение из [[sources/2026-05-18-pressfeed-13-cases-ai-search-adaptation|Pressfeed 13 кейсов]] (май 2026, туроператорский маркетплейс):

> «Параллельно мы усилили E-E-A-T, создавая профили экспертов с привязкой к верифицированным материалам, чтобы на нас ссылались внешние медиа и отраслевые авторы.»

**Шаблон E-E-A-T-якоря на сайте:**

Создать отдельные страницы-профили для каждого ключевого эксперта компании:

- Биография (с релевантными деталями, не "20 лет в digital")
- Список публикаций с обратными ссылками на оригиналы
- Спикерские выступления (видео + транскрипция, см. ниже про видео-механику)
- Сертификаты / профессиональная экспертиза
- Авторские страницы / колонки на корпоративном сайте

Это **не** футер «команда». Это полноценные lifelong-страницы, которые могут цитироваться внешними медиа. Дополнительно — Schema.org `Person` markup для каждого профиля.

## ENTITY и векторная близость как новый слой семантики

> «Сюда можно добавить столь нашумевшие термины, как ENTITY (сущности) и векторную близость. И это действительно работает. И классический поиск, и нейросети воспринимают контент более комплексно.»

Это **сдвиг** от keyword-research к **семантическим полям**: вместо «20 ключей по объёму» — карта 200+ связанных сущностей и фраз вокруг основной темы. Каждая страница покрывает не одну фразу, а **поле связанных сущностей**.

**Инструменты RU-практиков** (на май 2026):
- Собственные NLP-сервисы для подбора сущностей (упоминается агентство с заявкой +3× к цитируемости `[conf:low, src:2026-05-18]`)
- Wordstat + Google Trends для широких ключей (RU практик из Pressfeed: добавляет ключи через эти 2 инструмента + пересматривает структуру под «плюсы и минусы», «отзывы», «рекомендации»)
- Прямая работа с эмбеддингами для проверки векторной близости

## LLM-friendly HTML для видеоконтента

Отдельная техника, описана в [[canon/marketing-frameworks/llm-friendly-video-transcription]]. Главное: встраивать **скрытую** HTML-транскрипцию видео в код страницы, чтобы AI-краулеры могли индексировать содержание ролика как текст.

## SEO для внешних публикаций в СМИ

- Основной источник трафика для не-новостных медиа -- органический поиск
- СМИ имеют высокий траст у поисковиков: статья на таком ресурсе попадает в топ быстрее, чем на корпоративном блоге
- SEO-оптимизация внешних публикаций привлекает в разы больше читателей, чем неоптимизированные
- Стратегия «поисковое продвижение на внешних площадках»: статьи на VC.ru, E-xecutive, Biz360 попадают в топ быстрее корпоративного блога (подтверждено кейсом THERMAGENT)

### Локальные городские порталы как domain-authority boost (Ковпак, 2026)

Расширение «внешних публикаций» на **локальный** уровень — крупные городские порталы РФ (Fontanka.ru СПб, E1.ru Екатеринбург, 74.ru Челябинск, сетка Shkulev Media + независимые) — это **отдельный класс external-площадок** с собственной экономикой:

- **Доменный траст** для локальной поисковой выдачи (Google + Яндекс) — выше, чем у tier-1 национальных СМИ для запросов с city-specific intent (например, «ремонт в Самаре» → локальный портал ранжируется выше федерального)
- **SEO long-tail эффект:** одна публикация даёт **+50 органических лидов через 6 мес** после первичных 12k просмотров `[conf:medium, src:2026-05-19]` — то есть инвестиция работает как накопительный asset, а не разовая реклама
- **Цена входа** 25-150k₽ за лонгрид — ниже чем tier-1 СМИ, но получаемый локальный SEO-сигнал часто **переоценён** в общем восприятии маркетологов
- **Связка с GEO/AEO:** локальные публикации тоже попадают в retrieval-корпус LLM для locally-grounded запросов, особенно для RU AI-поиска (см. [[evolving-strict/market-data/ru-ai-search-traffic-share-2026]])

Подробная methodology — [[canon/marketing-frameworks/local-media-sales-funnel-kovpak]]. Practical anti-pattern: пытаться оптимизировать публикацию под VC.ru/Дзен без 90/10 пропорции — модерация удалит, SEO-asset не создастся (см. [[canon/marketing-frameworks/native-90-10-ratio-moderated-platforms]]).

## Двухуровневая декомпозиция эпохи AI-поиска

Этот playbook покрывает **контентный слой** (как попасть в retrieval-корпус, который читают LLM). Это **необходимое, но недостаточное** условие для рекомендации AI пользователю.

После попадания в корпус наступает **selection-фаза**: AI делает финальный выбор по структурированным данным о продукте (цена, гарантия, состав, сертификаты, TCO, SLA). Маркетинговые формулировки и сторителлинг на этом уровне игнорируются.

Для полного покрытия используй обе страницы:

- **Этот playbook (content-side)** — FAQ, Schema.org, llms.txt, E-E-A-T, ENTITY, seeding в трастовые сайты
- **Product Data рамка (data-side):** [[canon/marketing-frameworks/product-data-as-architecture-pragmatix]] — machine-readable product attributes, premium claims pattern, race-to-bottom anti-pattern

Industry-trend контекст обеих рамок — [[evolving/industry-trends/ai-search-product-discovery-layer-2026]].

## Foundation frameworks (architectural prerequisites)

Этот playbook **операционализирует** три более фундаментальных canon-фреймворка. Без понимания их основополагающих тезисов playbook действует «механически» и упирается в потолок sameness:

1. **[[canon/marketing-frameworks/stochastic-llm-ranking-sparktoro]]** — почему «позиции» в нейровыдаче не существует, нужна **probabilistic-метрика**. Foundation: SparkToro 2961-prompt benchmark Jan 2026 (<1% identical brand-set, ~20% stable brands at 5 runs).
2. **[[canon/marketing-frameworks/geo-platform-segmentation-yandex-chatgpt-perplexity]]** — почему Яндекс Нейро / ChatGPT / Perplexity нельзя оптимизировать одинаково. Foundation: 3 разные retrieval-инфраструктуры, content-стратегия выбирается **после** выбора аудитории.
3. **[[canon/marketing-frameworks/geo-monitoring-discipline-2026]]** — как измерять успех (4-осевая рамка: inclusion / citation quality / competitive parity / trend).

**Disqualification check** перед бюджетом → [[evolving/content-trends/geo-when-not-worth-investing-2026]] (3 кейса + sameness anti-pattern).

## Связанные страницы
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] -- тренд AEO/GEO
- [[canon/marketing-frameworks/product-data-as-architecture-pragmatix]] -- data-side: продуктовый фид как новая поверхность маркетинга
- [[evolving/industry-trends/ai-search-product-discovery-layer-2026]] -- AI как product decision-layer
- [[evolving-strict/market-data/ai-search-commerce-benchmarks-2026]] -- benchmarks 2025-2026
- [[canon/marketing-frameworks/native-advertising]] -- нативные публикации как SEO-инструмент
- [[evolving/content-trends/ai-in-pr-workflows-2026]] -- AI-инструменты в PR
- [[evolving-strict/campaign-metrics/pressfeed-pr-cases-2026]] -- кейс THERMAGENT с SEO на внешних площадках
- [[canon/marketing-frameworks/llm-friendly-video-transcription]] -- видео-механика
- [[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026]] -- RU practitioner-консенсус
- [[evolving/industry-trends/seo-to-pr-substitution-2026]] -- сдвиг SEO→PR в эру нейропоиска
- [[sources/2026-05-18-pressfeed-13-cases-ai-search-adaptation]] -- источник 13 RU-кейсов май 2026
- [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] -- онтологическая рамка retrieval'а + Faire +40% case + inventory accuracy
- [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] -- GEO-мониторинг как отдельная операционная дисциплина (foundation)
- [[sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data]] -- источник тезисов про JSON-LD приоритет и архитектурный сдвиг
- [[canon/marketing-frameworks/stochastic-llm-ranking-sparktoro]] -- foundation: стохастичность retrieval'а
- [[canon/marketing-frameworks/geo-platform-segmentation-yandex-chatgpt-perplexity]] -- foundation: 3 retrieval-инфраструктуры
- [[evolving/content-trends/geo-when-not-worth-investing-2026]] -- disqualification framework
- [[volatile-strict/industry-news/ru-ai-law-march-2026]] -- legal context (RU март 2026)
- [[evolving-strict/market-data/ru-ai-trust-citation-2026]] -- 28% trust / 87% no-citation RU
- [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]] -- источник foundation-расширения
- [[canon/marketing-frameworks/seo-search-intent-content-method-stadley]] -- content-side фундамент (метод поискового интента); без него технические механики не дают ROI
- [[canon/marketing-frameworks/expert-trust-platforms-leverage-method]] -- expert-уровень distribution: trust-площадки для не-СМИ-вертикалей (psychology, healthcare, law)
- [[canon/marketing-frameworks/seo-article-as-digital-asset-stadley]] -- CapEx-рамка SEO-актива vs. OpEx других форматов

## Backlinks

_7 pages link to this one._

- [[canon/marketing-frameworks/native-advertising]]
- [[canon/marketing-frameworks/performance-pr-framework]]
- [[evolving-strict/campaign-metrics/pressfeed-pr-cases-2026]]
- [[evolving/industry-trends/ai-search-aeo-geo-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-04-16-condense-pressfeed-35-articles]]
