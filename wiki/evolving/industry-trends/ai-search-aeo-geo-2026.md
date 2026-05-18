---
id: mkt:evolving/industry-trends/ai-search-aeo-geo-2026
title: "AI трансформирует поиск: эпоха AEO и GEO (2026)"
type: page
subtype: trend
layer: evolving
theme: industry-trends
tags: [seo, ai, content, search, decision-layer, infrastructure]
confidence: medium
stale: false
created: 2026-04-16
updated: 2026-05-18  # +Pressfeed «13 кейсов» (май 2026): RU practitioner-консенсус — PR замещает SEO как primary для инфо-запросов, B2B AI-трафик 0.36%/3.4% (qtickets), DiaClass 10%, 30-40% падения органики, 20-25% инфо-трафика, LLM-friendly видео-транскрипция
sources: [sources/2026-04-16-condense-pressfeed-35-articles.md, sources/2026-05-14-tg-techsparks-may-2026.md, sources/2026-05-14-tg-solokumi-may-2026.md, sources/2026-05-14-tg-cossaru-may-5-14-2026.md, sources/2026-05-14-tg-temno-moreynis-may-5-14-2026.md, sources/2026-05-18-pressfeed-13-cases-ai-search-adaptation.md]
namespace: mkt
---

# AI трансформирует поиск: эпоха AEO и GEO (2026)

Zero-click поиск растёт: пользователи получают ответ прямо в поисковой выдаче через нейроответы, без перехода на сайты. Это системный сдвиг, порождающий два новых подхода к оптимизации: AEO (Answer Engine Optimization) и GEO (Generative Engine Optimization).

## Определения

- **AEO** (Answer Engine Optimization) -- оптимизация контента, чтобы поисковые AI-системы (Яндекс с Алисой, Google AI Overviews, Perplexity) цитировали его в сниппетах и ответах
- **GEO** (Generative Engine Optimization) -- более широкое понятие: оптимизация под любые генеративные модели, включая ChatGPT, Claude, Gemini как «новые поисковые движки»

## Ключевые тезисы

- SEO постепенно становится частью контент-маркетинга, а не отдельной технической функцией
- PR и контент-маркетинг теперь неотделимы от SEO-стратегии: алгоритмы воспринимают регулярные упоминания бренда как сигнал авторитетности
- Появился термин **AI SEO** -- оптимизация контента под ответы нейросетей; некоторые медиа уже предлагают специальные форматы статей для попадания в ответы ИИ

## Инструменты мониторинга видимости в AI-ответах

- Пиксель Тулс (RU)
- Gptfox
- Ahrefs Brand Radar
- Llmspot

## Связь с GRO

Для маркетинга GRO это означает:
- Контент блога/медиа должен быть оптимизирован не только под классический SEO, но и под AEO/GEO
- Публикации в СМИ с высоким трастом дают двойной эффект: классический SEO + попадание в нейроответы
- Собственный экспертный контент-кластер повышает вероятность цитирования AI-системами

## Update 2026-05-14 — Decision-layer рамка (Technology Magazine через Себрант 5590)

[Technology Magazine](https://technologymagazine.com/articles/ai-rewriting-decision-layer) (статья **«AI Rewriting Decision Layer»**) переформулирует тезис: **«ИИ не убивает поисковые системы, он переписывает процесс принятия решений»**. Пересказ Себрантом в [@techsparks 5590](https://t.me/techsparks) от **7 мая 2026**.

### Главный структурный тезис

Подход «AI vs поисковики как соперники» — **ошибочен и неполноценен**. На рынке происходит **структурная конвергенция**: AI и поисковики объединяются в **единую систему** decision-layer'а, которая извлекает информацию, принимает решения и синтезирует ответ.

> «Поисковики долгие годы были основным интерфейсом интернета. ИИ меняет этот интерфейс, но не саму потребность в нем. Зависимость от релевантных данных и ранжирования осталась.»

Без качественных базовых функций retrieval+ranking качество AI-ответа снижается.

### Три уровня контроля (controllers)

Для создания **комплексного AI** нужен контроль на **3 уровнях**:

1. **Извлечение данных** (retrieval) — индексирование интернета, crawl, datasets
2. **Ранжирование и персонализация** (ranking) — алгоритмическое определение релевантности
3. **Синтез** (synthesis) — генерация финального ответа из retrieved data

**Лишь несколько компаний работают по всему циклу:**

| Компания | Retrieval | Ranking | Synthesis | Сегмент |
|---|---|---|---|---|
| **Google** | ✓ (search index) | ✓ (PageRank+Gemini) | ✓ (AI Overviews, Gemini) | General-purpose web |
| **Microsoft** | ✓ (Bing index) | ✓ (Bing algo + Copilot) | ✓ (Copilot, GPT через OpenAI) | General + enterprise |
| **Baidu** | ✓ (Chinese web index) | ✓ | ✓ (Ernie) | China-локальный |
| **Яндекс** | ✓ (RU web index) | ✓ | ✓ (Алиса, YandexGPT) | RU-локальный |
| **Amazon** | ✓ (product index) | ✓ | ✓ (Rufus) | **E-commerce-вертикаль** |

**Все пять компаний дают доступ к части инфраструктуры по API** — это **новая распределённая инфраструктурная модель**.

### Что это меняет для AEO/GEO стратегии

Раньше **AEO/GEO** воспринимался как **внешняя оптимизация** под уже сформированный AI-ответ. Decision-layer рамка показывает: **AI-ответ формируется на трёх уровнях**, и **influencing** возможен на каждом:

- **На уровне retrieval** — попасть в crawl-индекс (классический SEO + structured data + APIs)
- **На уровне ranking** — добиться высокой релевантности (классический SEO + brand authority + E-A-T)
- **На уровне synthesis** — попасть в **prompt-context** AI-модели (промт-инжектируемый контент: высокотрастовые цитаты, обзорные статьи, специальные «AI-friendly» форматы)

**Структурная импликация:** SEO-аудит и AI-аудит — **разные слои контроля, разные инструменты**. Содержательно: «AI optimization» — это не более тонкая SEO, а **отдельная дисциплина** с собственной мета-моделью.

### RU-специфика

**Яндекс — единственный RU-владелец всех 3 уровней.** Это **сильный structural advantage** для русскоязычной аудитории (Алиса даёт интегрированный decision-layer в RU-вебе). Для GRO-аудитории (RU + СНГ) **Яндекс — главный приоритет AEO/GEO**, не Google (хотя и Google AI Overviews работает в RU-выдаче).

**Лидеры по внедрению AI** (в decision-layer): «Среди лидеров по внедрению ИИ: Google, Microsoft, Baidu и Яндекс» — то есть Яндекс входит в top-4 globally, что валидирует его как обязательный канал для GRO-контента.

### Анти-pattern

- **Не путать decision-layer с AI-features в обычном Search** — это **архитектурный сдвиг**, не feature-добавка. Если контент-стратегия в 2026 ориентируется на «выходить в TOP-10», она уже не покрывает decision-layer (запросы пересобираются на 3 уровнях).
- **Не воспринимать «5 компаний контролируют» как монополию** — это **необходимая структура** для AI-search, не bad-acting. Каждый из 5 даёт API-доступ к части infrastructure → builders строят third-party AI-приложения поверх.

## Update 2026-05-14 — Кумар Виас квантификация скейла и Gartner-прогноз

[[sources/2026-05-14-tg-solokumi-may-2026|Solokumi пост 405]] (2026-05-07) добавляет цифры скейла:

- ChatGPT — 900 млн пользователей в неделю `[conf:high, src:2026-05-07]`
- Perplexity — 1+ млрд запросов в месяц `[conf:high, src:2026-05-07]`
- Позиция #1 в Google: CTR на 38% меньше, чем год назад `[conf:high, src:2026-05-07]`
- **Gartner-прогноз: -25% органического трафика к концу 2026** `[conf:medium, src:2026-05-07]`

Эти цифры **валидируют** decision-layer-рамку из апдейта 2026-05-14 (Себрант/Technology Magazine): сдвиг происходит на структурном уровне, поисковики и AI-стек реально объединяются, **и пользователи это уже сделали** (1+ млрд запросов/мес у Perplexity — это не нишевый продукт). Окно для GEO-стратегии открыто, но Gartner прогнозирует измеряемое сокращение классического канала к концу года.

Конверсионный сигнал (`confidence: medium`): AI-трафик конвертится в 4+ раза лучше органики, регистрации приходят в 10 раз чаще `[conf:medium, src:2026-05-07]` — не догоняющий канал, а new-best для тех, кто опередил рынок.

Детальный operational playbook → [[evolving/content-trends/geo-playbook-2026-q2]].

## Update 2026-05-15 — Алла Рауд: measurable vs dark-zone (Cossa)

**Алла Рауд** (founder «Киберкошка», ASO в IT-Agency) в [Cossa 23121](https://t.me/cossaru/23121) от 2026-05-12 артикулирует операционную рамку: разделить **измеримое** в AI-search от **«тёмной зоны»**.

**Измеримо уже сейчас:** видимость бренда, роль в ответе (центральная/вспомогательная/фоновая), тональность упоминания, устойчивость формулировок, сравнение с конкурентами.

**В «тёмной зоне»:** точные конверсии из AI-поиска в покупку, полная атрибуция PR-активностей, ROI на конкретные технические изменения сайта.

Это даёт **методологический разграничитель**: AI-search measurement — отдельная дисциплина, не подмена SEO. Полный фреймворк см. [[canon/marketing-frameworks/ai-search-measurable-vs-dark-zone]].

## Update 2026-05-15 — Duda study: масштабный signal для AEO (Cossa)

[Duda](https://tech.yahoo.com/ai/deals/articles/want-320-more-traffic-2-131000677.html) проанализировала **850 000 сайтов и 69 млн визитов AI-краулеров** ([Cossa 23137](https://t.me/cossaru/23137) от 2026-05-13). Главное:

- AI-видимые сайты получают **+320% живого трафика** vs AI-игнорируемые
- ×2,7 форм, ×2,5 звонков
- Microsoft Clarity: AI-трафик конвертируется в **3× лучше** обычного
- Google AI Overviews показываются в **68% локальных запросов**

**Дихотомия рынка**: сайты в AI-ответе → +320%; вне AI-ответа → −20–90% (см. [[evolving-strict/market-data/digital-ad-cpm-shifts-q1-2026]]). Это **«победитель забирает всё»** для AI-видимости — больше нет средней нормы.

5 must-have для попадания в AI-ответ (active blog, Local Schema, GBP sync, динамические страницы, **больше страниц как ключевой пункт**) детализированы в [[evolving/content-trends/ai-aeo-must-haves-2026]]. Полные метрики — [[evolving-strict/market-data/duda-ai-traffic-conversion-2026]].

## Update 2026-05-16 — Морейнис: marketing tools for humans устаревают (RU-голос для AEO/GEO)

> Большинство маркетинговых инструментов, которые ты использовал для продвижения своего программного продукта, скоро станут неактуальными. Потому что они рассчитаны на людей. — Морейнис, [[sources/2026-05-14-tg-temno-moreynis-may-5-14-2026|пост 7833, 2026-05-14]]

Морейнис добавляет **RU-голос** к global AEO/GEO нарративу через формулировку **«маркетинг для агентов вместо для людей»**. Тезис идёт в три уровня:

1. **Видимый сдвиг:** ИИ-агенты становятся новыми «потребителями» продуктов (особенно SaaS / API-first сервисов).
2. **Что у тебя не работает:** видеоролики, провокационные посты, эмоциональный сторителлинг, бренд-сторителлинг — всё, что рассчитано на эмоциональный отклик человека.
3. **Что начнёт работать:** structured machine-readable docs, API-first content, decision logic в open data, schema.org markup, citation в structured databases.

**Связь с Алла Рауд (cossa, 14 мая 2026):** Рауд формулирует это как **dark-zone** — место, где AI-агенты делают выбор без видимости для marketers. Морейнис добавляет **operational consequence** — нужны **два parallel content tracks** (для людей + для агентов).

**Связь с Duda study:** Duda измерила **outcome** (видимые в AI-ответах сайты получают +320% трафика). Морейнис даёт **причину** (стек маркетинговых сигналов для людей перестаёт работать в agent-first сегменте).

**RU-content opportunity:** Морейнис — публичный голос в русскоязычном Telegram, поэтому его формулировка тренда становится **referral anchor** для marketing-content GRO и индустриальных постов на vc.ru / Habr. Стандартный hook:

```
Аркадий Морейнис (fastfounder.ru): ваши видеоролики не нужны ИИ-агентам.
60% знаниевых запросов уже идёт через ChatGPT (не Google). К 2027 — 50%
доли поиска в США (Gartner). Что ты делаешь, чтобы попасть в machine-readable
маркетинг?
[open question]
```

Подробный разбор Морейниса-формата маркетинговых hooks для агентов — в [[evolving/content-trends/marketing-for-ai-agents-content-hooks]].

## Update 2026-05-18 — Pressfeed: 13 RU-кейсов адаптации с количественными сигналами

[[sources/2026-05-18-pressfeed-13-cases-ai-search-adaptation|Pressfeed «13 историй»]] (май 2026) даёт **первый известный нам публичный RU-замер** долей AI-трафика на конкретных проектах и **practitioner-консенсус** из 13 экспертных комментариев. Это валидация decision-layer-рамки на местных проектах.

### Главное

1. **PR замещает SEO как primary-канал для информационных запросов** — это отдельный системный сдвиг, отражённый в новой странице [[evolving/industry-trends/seo-to-pr-substitution-2026]]. SEO становится фундаментом (technical base + брендовые запросы), PR — primary driver для попадания в нейроответы.
2. **B2B vs B2C разница в 45×**: qtickets B2B (qtickets.ru) — 0.36% AI-трафика от визитов и 3.4% от органики; qtickets B2C (qtickets.events) — 0.008% `[conf:medium, src:2026-05-18]`. См. полный разбор [[evolving-strict/market-data/ru-ai-search-traffic-share-2026]].
3. **Нишевые инструмент-search SaaS — самая высокая доля** (DiaClass: 10% трафика из ChatGPT/Perplexity) `[conf:medium, src:2026-05-18]`. GRO ближе к этому профилю.
4. **Падение органики 30-40% за 2025**, при этом **20-25% — именно информационный трафик**, коммерческий стабилен `[conf:high, src:2026-05-18]`. Это **валидация Gartner-прогноза** «-25% к концу 2026» — тренд уже реализуется.
5. **Триггер RU-рынка — май 2025**: Яндекс и Google синхронно запустили AI-блоки. **Декабрь 2025** — массовый запуск GEO/AEO как платных услуг RU-агентствами `[conf:high, src:2026-05-18]`. **Январь 2026** — первый клиент через ChatGPT-рекомендацию + первое приглашение в тендер по AEO `[conf:medium, src:2026-05-18]`.
6. **Яндекс.Метрика измеряет AI-трафик с 2024H2** `[conf:high, src:2026-05-18]`.

### Новые operational механики из 13 кейсов

- **E-E-A-T через профили экспертов**: отдельные страницы с верифицированными ссылками на публикации (туроператорский маркетплейс) — детализировано в [[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026]].
- **SSR-страницы по узким сущностям**: для туроператоров, для каждой темы, для каждого пользовательского сценария — long-tail генерация как стандартный пункт.
- **ENTITY + векторная близость**: NLP-инструменты для подбора связанных сущностей; единичный заявленный кейс +3× к цитируемости `[conf:low, src:2026-05-18]`, но **множественное упоминание** этого как priority-инструмента у RU-практиков валидирует тренд.
- **LLM-friendly HTML для видео**: встраивание скрытой транскрипции в HTML для AI-индексации видеоконтента — новая страница [[canon/marketing-frameworks/llm-friendly-video-transcription]].
- **PR-эксперимент «несуществующий бизнес»**: RU-агентство заставило ИИ рекомендовать несуществующий бренд только за счёт активной PR-работы. **Proof-of-concept** того, что PR-присутствие в retrieval-корпусе достаточно для AI-цитирования.

### Анти-pattern «промпт-магия» подтверждён ещё раз

Все 13 практиков сошлись: попытки прямой инъекции в ChatGPT через диалоги — не работают. Системный подход через SEO-фундамент + targeted seeding на трастовые площадки — единственное, что работает. Это **тройное подтверждение** anti-pattern'а из [[evolving/content-trends/aeo-geo-llm-search-optimization-2026|Pressfeed апрель]] и Перегудов/Шевченко (апрель).

### Связь с decision-layer и Морейнис

RU-практики неявно работают на трёх уровнях decision-layer:
- **Retrieval**: SSR-страницы + Schema.org + llms.txt + LLM-friendly видео = присутствие в crawl-индексе
- **Ranking**: E-E-A-T + длинный список internal-сущностей = высокая релевантность
- **Synthesis**: PR-targeted seeding на трастовые площадки = попадание в prompt-context

Это **операционное приземление** decision-layer-рамки Себранта на RU-рынке. И «PR-эксперимент с несуществующим бизнесом» — наиболее яркое подтверждение Морейнис-тезиса «маркетинг для агентов»: AI делает выбор по retrieval-корпусу, а не по эмоциям пользователя.

## Связанные страницы
- [[canon/marketing-frameworks/seo-for-ai-era-playbook]] -- практические рекомендации по AI-оптимизации
- [[canon/marketing-frameworks/ai-search-measurable-vs-dark-zone]] -- Алла Рауд measurable vs dark-zone
- [[evolving/content-trends/ai-aeo-must-haves-2026]] -- 5 must-have Duda (operational)
- [[evolving-strict/market-data/duda-ai-traffic-conversion-2026]] -- метрики Duda study
- [[evolving-strict/market-data/digital-ad-cpm-shifts-q1-2026]] -- обратная сторона: каннибализация трафика без AI-видимости
- [[evolving/content-trends/smm-strategy-trends-2026]] -- Social SEO как часть SMM-стратегии 2026
- [[evolving/content-trends/ai-in-pr-workflows-2026]] -- Яндекс легитимизирует GEO как PR-дисциплину
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] -- макро-карта controllers (5 узлов decision-layer пересекаются с capital-узлами гонки)
- [[evolving/content-trends/aeo-geo-llm-search-optimization-2026]] -- практический playbook AEO/GEO
- [[evolving/content-trends/geo-playbook-2026-q2]] -- operational плейбук Q2 2026 с 6 механиками
- [[sources/2026-05-14-tg-techsparks-may-2026]] -- источник пересказа Technology Magazine
- [[sources/2026-05-14-tg-solokumi-may-2026]] -- источник цифр скейла и Gartner-прогноза
- [[sources/2026-05-14-tg-cossaru-may-5-14-2026]] -- источник Аллы Рауд и Duda study
- [[evolving/content-trends/marketing-for-ai-agents-content-hooks]] -- content-side derivative тренда (hooks для marketing-for-agents)
- [[evolving/industry-trends/agent-first-world-openclaw-2026]] -- родительский тренд (агенты как новые пользователи)
- [[sources/2026-05-14-tg-temno-moreynis-may-5-14-2026]] -- источник Морейнис «marketing tools for humans устаревают» (пост 7833)
- [[sources/2026-05-18-pressfeed-13-cases-ai-search-adaptation]] -- источник 13 RU-кейсов (май 2026)
- [[evolving/industry-trends/seo-to-pr-substitution-2026]] -- сдвиг SEO→PR (deriv этого тренда)
- [[evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026]] -- RU practitioner-консенсус 13 кейсов
- [[evolving-strict/market-data/ru-ai-search-traffic-share-2026]] -- RU метрики долей AI-трафика B2B/B2C
- [[canon/marketing-frameworks/llm-friendly-video-transcription]] -- LLM-friendly видео-механика
