---
id: mkt:evolving/content-trends/geo-playbook-2026-q2
title: "GEO-плейбук Q2 2026 — 6 практических механик попадания в AI-выдачу"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [geo, aeo, llm-search, chatgpt, perplexity, faq-schema, llms-txt, robots-txt, reddit, wikipedia, content, generative-engine-optimization, json-ld, monitoring, kravchenko]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-05-19  # +Кравченко (Insight Analytics) механика VI → GEO-monitoring discipline + Faire +40% AI-Overviews case; +Pressfeed «GEO иллюзия позиций»: 5-шаговый практикумный чек-лист
sources: [sources/2026-05-14-tg-solokumi-may-2026.md, sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data.md, sources/2026-05-18-pressfeed-geo-illusion-stability-measure.md]
namespace: mkt
---

# GEO-плейбук Q2 2026 — 6 практических механик

Дрейфующий operational-плейбук для **Generative Engine Optimization** на состояние 2026-05. Если [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] и [[evolving/industry-trends/ai-search-aeo-geo-2026]] фиксируют **тренд и его рамку**, то этот плейбук — **что делать в пятницу утром**: конкретные техники с метриками, чек-листы и инструменты мониторинга.

Это `evolving`, не `canon`: метрики (%-цитат, CTR, доля Reddit/Wikipedia в LLM-источниках) меняются по мере того, как LLM-провайдеры обновляют retrieval-стек. Каждые 3 месяца требует re-verify.

Источник: пост 405 (2026-05-07) канала [@solokumi](https://t.me/solokumi) — Р. Кумар Виас фиксирует 6 механик с цифрами, которые активно цитируются в практическом GEO-сообществе.

## Почему именно сейчас открыто окно возможностей

> «Большинство компаний ещё не начали с этим работать — окно возможностей открыто прямо сейчас.»
>
> — Р. Кумар Виас, @solokumi пост 405, 2026-05-07

**Метрики сдвига**: ChatGPT обслуживает 900 млн пользователей в неделю, Perplexity — 1+ млрд запросов в месяц `[conf:high, src:2026-05-07]`. Параллельно позиция #1 в Google теряет CTR — **на 38% меньше, чем год назад** `[conf:high, src:2026-05-07]`. **Gartner прогнозирует -25% органического трафика к концу 2026** `[conf:medium, src:2026-05-07]`. Можно стать первым в Google и при этом проигрывать тем, кто работает с AI-поиском.

И ключевое: **трафик из AI конвертится в 4+ раз лучше органики**, регистрации приходят в **10 раз чаще** `[conf:medium, src:2026-05-07]` — это не догоняющий канал, это next-best-channel прямо сейчас.

## Механика I — Правило первых 50 слов

**Цифра**: 44.2% всех AI-цитат приходятся на первые 30% текста страницы `[conf:high, src:2026-05-07]`.

**Что делать**: давать прямой ответ на главный вопрос пользователя в первых 50 словах. Потом детали. Это даёт **+40% к цитируемости ИИ** `[conf:high, src:2026-05-07]`.

**Быстрая win-операция**: возьмите 5 самых посещаемых страниц сайта, перепишите первый абзац каждой. **2 часа работы, результат виден через 3–4 недели** `[conf:medium, src:2026-05-07]`.

**Связь с smart-SEO**: это и есть «answer-first»-структура из [[canon/marketing-frameworks/seo-for-ai-era-playbook]] — перевёрнутая пирамида. Просто теперь измерено в долях AI-цитат.

## Механика II — FAQPage schema

**Что**: разместить специальный JSON-LD-блок в `<head>` страницы. Это прямой путь к попаданию в Google AI Overviews и к тому, как LLM понимают структуру вашего текста.

**Template**:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "Ваш главный вопрос?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "Прямой ответ 50 слов без воды."
    }
  }]
}
</script>
```

Детали schema — [schema.org/FAQPage](http://schema.org/FAQPage).

**Почему это работает**: формат «вопрос → ответ» **буквально совпадает** с тем, на чём обучаются LLM на стадии RLHF. Из [[evolving/industry-trends/ai-search-aeo-geo-2026]] (Шевченко / humanswith.ai): пары Q&A — это RLHF-friendly формат, оценщики предпочитают такие ответы и модель усиливает их вес.

## Механика III — llms.txt и robots.txt

**llms.txt** — новый файл, который кладётся в корне сайта и **объясняет AI-краулерам структуру вашего контента**. Аналогия с `robots.txt`, но для LLM-ботов.

**Генератор**: [llmstxt.firecrawl.dev](https://llmstxt.firecrawl.dev/) — генерирует базовый llms.txt по сайту.

**robots.txt — проверка чек-лист**: GPTBot, ClaudeBot, PerplexityBot **не должны быть заблокированы**. Иначе ни одна LLM вас не процитирует. Это технический must-check для всех бизнесов, работающих с GEO.

```
# robots.txt — must-allow для GEO 2026
User-agent: GPTBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: CCBot
Allow: /
```

## Механика IV — Off-domain placement (85% AI-цитат не у вас)

**Главная цифра**: 85% ссылок в ответах AI идут с доменов, **которыми вы не владеете** `[conf:high, src:2026-05-07]`. **53% всех AI-цитат** — из отзовиков и списков типа «Топ-10 для…» `[conf:high, src:2026-05-07]`.

**Это переворачивает SEO-логику**: оптимизировать собственный сайт уже **недостаточно**. Нужно попасть в:

1. **Актуальные списки и подборки**: «Топ-10 CRM для SMB», «5 лучших SaaS-аналитик» и т.п. Это и есть основной механизм попадания в AI-выдачу.
2. **Подкасты и медиа** — упоминания в подкастах и журналистских материалах **влияют на AI-ответы сильнее обычных бэклинков**.
3. **Reddit / Quora развёрнутые ответы по вашей теме** (см. механику V).

Это то, что Шевченко в [[evolving/industry-trends/ai-search-aeo-geo-2026]] называет **targeted seeding контента в retrieval-corpus LLM** — теперь с цифрой «85% off-domain».

**Бесплатный аудит** того, как вас сейчас видят AI-модели — [audit.algomizer.com](https://audit.algomizer.com/).

## Механика V — Reddit / Wikipedia как primary corpus

**Доли источников у LLM**:

- **46.7% источников Perplexity — Reddit** `[conf:high, src:2026-05-07]`
- **47.9% источников ChatGPT — Wikipedia** `[conf:high, src:2026-05-07]`

**Можно зафигачить идеальный сайт и не попасть в AI-ответы**, просто потому что вас там нет.

**RU-аналоги** для русскоязычного рынка (Reddit/Wikipedia слабо представлены в RU-выдаче): **vc.ru**, **Habr**, **крупные telegram-каналы**.

**Чек-лист быстрого старта по Reddit**:

| Параметр | Значение |
|---|---|
| Один развёрнутый ответ | На основной вопрос вашей ниши |
| Объём | 400–600 слов |
| Тон | Полезный, **не** продающий |
| Обновление | Раз в квартал |
| B2B-альтернатива | LinkedIn-пост в том же формате |
| Source | `[conf:medium, src:2026-05-07]` |

**Чек-лист по Wikipedia**: есть ли статья по вашей теме? Если есть — **проверить, что там есть ссылка на первоисточник с вашего домена**. Это легитимная low-cost точка входа в ChatGPT-retrieval corpus.

## Механика VI — Мониторинг позиций в AI-поиске

В классическом SEO всё понятно — Ahrefs, Semrush, Serpstat. В GEO **другой стек инструментов**:

| Инструмент | Что делает | Cost |
|---|---|---|
| [GEO Tracker AI](https://geotrackerai.com/) | Отслеживает упоминания бренда в ChatGPT и Perplexity, показывает, по каким промптам вас цитируют, сравнивает с конкурентами | $$ |
| [audit.algomizer.com](https://audit.algomizer.com/) | Бесплатный one-shot аудит видимости бренда в AI-моделях | free |
| Пиксель Тулс (RU) | RU-мониторинг видимости в Алисе и российских AI-поисковиках | $$ |
| Ahrefs Brand Radar | Дополнительный модуль Ahrefs для AI-мониторинга | $$$ |
| Llmspot | Глобальный AI-визибилити-tracker | $$ |

Список четырёх последних — из [[evolving/industry-trends/ai-search-aeo-geo-2026]]; GEO Tracker AI добавляет Виас в посте 405 как **новый специализированный инструмент** для ChatGPT+Perplexity-комбо.

## Sanity-check: куда уходят регистрации

Финальная цифра, ради которой всё это делается:

| Канал | Конверсия в регистрацию | Source |
|---|---|---|
| Органический поиск | baseline | `[conf:medium, src:2026-05-07]` |
| AI-поиск (ChatGPT / Perplexity / Claude) | в **10 раз чаще** | `[conf:medium, src:2026-05-07]` |

**Интерпретация**: пользователь, который пришёл через AI, **уже принял решение**, что вы — релевантный ответ на его вопрос. Это другой уровень намерения, и поэтому регистрация в 10x.

## Update 2026-05-18 — Кравченко (Insight Analytics): дополнения к механикам

[[sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data|Кравченко в Pressfeed «.Журнал» (май 2026)]] добавляет операционное расширение к двум механикам:

### Механика II расширяется: Faire case +40% AI-Overviews

Кравченко описывает operational case: платформа Faire имела высокие позиции в обычной выдаче Google, но **не попадала в Google AI Overviews**. После расширения атрибутов **Schema.org Product/Offer/Brand** + переход на **JSON-LD в режиме реального времени**: **+40% упоминаний в AI-обзорах по коммерческим запросам** `[conf:medium, src:2026-05-18]`.

Это **первый публичный benchmark uplift'а** от структурированных данных на Google AI Overviews. Дополняет цифру «+40% к цитируемости от первых 50 слов» (механика I) — это работает на **отдельном уровне** (объектные атрибуты, не текст).

**Operational consequence для механики II:** не ограничиваться `FAQPage` schema. Для коммерческих сущностей добавлять полную онтологию `Product` / `Offer` / `Brand` / `AggregateRating` (для e-commerce) или `SoftwareApplication` (для SaaS). Полная рамка — [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]].

### Механика VI расширяется: GEO-мониторинг как отдельная дисциплина

Кравченко артикулирует то, что в этой странице фигурирует как **набор инструментов** (GEO Tracker AI, audit.algomizer.com, Llmspot, Ahrefs Brand Radar, Пиксель Тулс), как **отдельную операционную дисциплину** с собственным фреймворком измерения:

- **Inclusion** — входит ли бренд в pool источников по контрольному списку запросов?
- **Citation quality** — как именно цитирует модель (точно/искажение, контекст, авторитетность)
- **Competitive parity** — share-of-voice относительно конкурентов
- **Trend over time** — динамика по этим трём осям

Полный playbook дисциплины (что отслеживать, weekly cadence, operational loop, alerts) — [[canon/marketing-frameworks/geo-monitoring-discipline-2026]]. Инструменты остаются те же, что в этой механике; разница — в **дисциплине измерения**, не в tooling.

### Дополнительный operational signal: inventory accuracy

Из материала Кравченко:

> «ИИ генерирует ответы на основе доступной информации «здесь и сейчас». Если на сайте указано наличие товара, которого уже нет, модель фиксирует недостоверность. Актуальность данных становится новым критерием релевантности.»

Это **новая операционная цепочка**: stale data → AI помечает домен как недостоверный → downgrade ranking **всего домена**. Один незакрытый недоступный товар деградирует видимость **всех** товаров. См. [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] раздел «Inventory accuracy».

Для e-commerce и B2B-SaaS — обязательная инфраструктурная компонента (real-time sync между inventory/feature-set и JSON-LD-разметкой), не операционная мелочь.

## Полный чек-лист для команды

Минимальный first-pass GEO-проект (1 спринт, 2 недели):

- [ ] **Контент**: переписать первые 50 слов на 5 топовых страницах (Mech I, 2 ч работы)
- [ ] **Schema**: вставить FAQPage JSON-LD в 5 топовых страниц (Mech II, 1 ч)
- [ ] **Crawl**: проверить, что GPTBot/ClaudeBot/PerplexityBot **не заблокированы** в robots.txt (Mech III, 15 мин)
- [ ] **llms.txt**: сгенерировать через llmstxt.firecrawl.dev, выложить в корне сайта (Mech III, 30 мин)
- [ ] **Off-domain**: найти 3 актуальных списка «Топ-10 для X», попасть в них (Mech IV, 1–2 недели outreach)
- [ ] **Reddit**: один пост 400–600 слов в /r/<ниша>, полезный, без продажи (Mech V, 2 ч)
- [ ] **Wikipedia**: проверить наличие статьи по теме, бэклинк с вашего сайта (Mech V, 1 ч)
- [ ] **Мониторинг**: запустить GEO Tracker AI + audit.algomizer.com для baseline (Mech VI, 30 мин)
- [ ] **Product Schema**: расширить разметку коммерческих страниц до `Product` / `Offer` / `Brand` / `AggregateRating` + переход на JSON-LD в `<head>` (если ещё Microdata) — Faire case +40% AI-Overviews (Кравченко, 2026-05-18, 2-4 ч)
- [ ] **Inventory sync**: проверить, что `availability` в Schema обновляется при изменении состояния (latency < 5 мин). При out-of-stock — обновление Schema, не удаление страницы. (Engineering, 4-8 ч)

**Результат**: через 3–4 недели — измеряемый рост AI-цитируемости (`+40%` теоретический потолок от Mech I в одиночку; +40% и в Faire case от Schema-расширения — это **независимые** uplifts по разным механизмам).

## Связанные страницы

- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] — базовый тренд AEO/GEO, теоретическая рамка
- [[evolving/industry-trends/ai-search-aeo-geo-2026]] — макро-уровень тренда + decision-layer рамка
- [[canon/marketing-frameworks/seo-for-ai-era-playbook]] — стабильная рамка (форматы, кластеры, schema)
- [[canon/marketing-frameworks/fete-outreach-framework-clay]] — параллельная operational-механика (но для outbound, не для inbound)
- [[canon/marketing-frameworks/object-oriented-retrieval-kravchenko]] — онтологическая рамка retrieval'а LLM через объекты, Faire +40% case, inventory accuracy
- [[canon/marketing-frameworks/geo-monitoring-discipline-2026]] — GEO-мониторинг как отдельная операционная дисциплина (4-осевая рамка измерения)
- [[sources/2026-04-16-pressfeed-geo-vmesto-seo]] — Шевченко / humanswith.ai про три механизма попадания в LLM
- [[sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data]] — Кравченко: object-oriented retrieval, Faire case, architectural shift

## Update 2026-05-19 — Pressfeed 5-шаговый практикумный чек-лист (extension)

[[sources/2026-05-18-pressfeed-geo-illusion-stability-measure|Pressfeed «GEO иллюзия позиций»]] (май 2026) даёт **5-шаговый operational чек-лист** как extension к 6 механикам Кумар Виас выше. Шаги ориентированы на **первое полугодие GEO-программы** (когда базовая инфраструктура запущена, но ещё не понятна реальная видимость):

### Шаг 1. Проверьте, что о вас знают

Прогон **нескольких запросов в разных формулировках** через **Яндекс Нейро + ChatGPT** (минимум 2 платформы; полная сегментация — [[canon/marketing-frameworks/geo-platform-segmentation-yandex-chatgpt-perplexity|platform segmentation]]).

**Зафиксировать:**
- Где бренда **нет**
- Где бренд **есть**
- Где AI говорит о бренде **что-то не то** (старая цена, путаница с конкурентом, неверная категория)

Это **важнее любого контент-плана** — без baseline-аудита остальное теряет смысл. Это input для GEO-monitoring loop ([[canon/marketing-frameworks/geo-monitoring-discipline-2026|GEO-monitoring discipline]]).

### Шаг 2. Разделите экосистемы

Не действовать «универсально» по 3 платформам. Определить **где сосредоточена ваша аудитория**, направить усилия туда. Для каждой экосистемы — **отдельная инфраструктура** (см. platform-segmentation таблицу).

### Шаг 3. Закрепите авторство

- Новые материалы — **сначала на своих площадках**, потом на внешних
- **Никаких эксклюзивов** чужим доменам, если они главные для категории
- Партнёрские версии — **специально неполноценны** без вашего бренда

Это защита от [[evolving/content-trends/aeo-geo-llm-search-optimization-2026|information primacy theft]] — LLM выбирает не первоисточник, а более trusted/recent домен. Legal protection ([[volatile-strict/industry-news/ru-ai-law-march-2026|RU AI-закон март 2026]]) **отсутствует** в РФ; единственная защита — content-структурная.

### Шаг 4. Считайте правильные метрики

**Не:** «нас упомянули 20 раз за месяц»

**А:**

- В какой **доле релевантных запросов** мы появляемся?
- В каком **контексте**?
- Насколько **стабильно** при повторных прогонах? (SparkToro benchmark: 20% брендов появляются стабильно при 5 прогонах — see [[canon/marketing-frameworks/stochastic-llm-ranking-sparktoro|stochastic-llm-ranking]])

Это **операционная импликация стохастичности** AI-выдачи. Подробная рамка metric'ов — [[canon/marketing-frameworks/geo-monitoring-discipline-2026|GEO-monitoring discipline]].

### Шаг 5. Честно оцените перспективы

GEO — **инвестиция в среду, которая может измениться в любой момент**:

- Алгоритмы обновляются без расписания и предупреждения
- Год работы может быть **обнулён** одним обновлением модели
- В классическом SEO накопленные ссылки/история работают месяцами; в GEO такой стабильности нет

**Дисквалификаторы** (когда GEO не оправдан):
- Нет чёткого отличия от конкурентов (commodity-сегмент → AI выдаёт общий список или отправляет на маркетплейс)
- Нет готовности работать **минимум год**
- Клиент в категории выбирает **по цене** → AI пойдёт по price-comparison

Полный disqualification-фреймворк → [[evolving/content-trends/geo-when-not-worth-investing-2026]].

## Sources

- [[sources/2026-05-14-tg-solokumi-may-2026]] — пост 405 от 2026-05-07 (6 механик с метриками)
- [[sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data]] — Кравченко (Insight Analytics): Faire +40% case + дополнения к механикам II и VI
- [[sources/2026-05-18-pressfeed-geo-illusion-stability-measure]] — 5-шаговый practitioner чек-лист (extension)
