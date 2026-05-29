---
id: mkt:evolving/content-trends/forbes-russia-native-ad-pattern-2026
title: Шаблон нативной рекламы Forbes Russia (spetsproekt + erid + image-hook)
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [native-advertising, forbes, russia, content-pattern, spetsproekt, erid, b2b-marketing]
confidence: medium
stale: false
created: 2026-04-14
updated: 2026-05-28  # +4-й замер (8-11 мая): MTS Optimus blogs (с brand-mark — отступление от классического pattern), Forbes Club event-promo, Forbes×Серебряный дождь FM-cross-media, FOMOиYOLO 6-platform podcast. +cross-link на forbes-200-richest-russia-content-franchise (третий устойчивый Forbes editorial archetype — wealth-listicle content-asset). Prior: +cross-link на forbes-30-under-30-content-franchise; +4 кейса 7-8 мая (Кронунг blogs, PropTech Яндекс blogs, Alfa-Bank brandvoice, форум «Движение» spetsproekt+erid).
sources: [sources/2026-04-14-tg-forbesrussia-apr-13-14.md, sources/2026-04-10-piarhub-research-native-pr-2026.md, sources/2026-05-05-tg-forbesrussia-may-4-5-2026.md, sources/2026-05-19-tg-forbesrussia-20260519-104004.md, sources/2026-05-26-forbes-tegi-30-under-30.md, sources/2026-05-26-forbes-tegi-200-bogateyshih-biznesmenov.md, sources/2026-05-26-tg-forbesrussia-may-8-11-2026.md]
namespace: mkt
---

# Шаблон нативной рекламы Forbes Russia

В Telegram-канале @forbesrussia 13–14 апреля 2026 одновременно прошли два нативных размещения с **идентичной структурой** — EMC (Европейский медицинский центр) и ВТБ Мои Инвестиции. Совпадение шаблона позволяет описать его как **наблюдаемый pattern Forbes-нативки 2026**, а не одиночный кейс. Бенчмарк-источник для шаблона — [[sources/2026-04-14-tg-forbesrussia-apr-13-14]].

## Анатомия шаблона

| Элемент | EMC (94821) | ВТБ Интеллект (94859) |
|---|---|---|
| URL-площадка | `forbes.ru/spetsproekt/...` | `forbes.ru/special/...` |
| erid в URL | `?erid=F7NfYUJCUneTVTcSKRK3` | `?erid=F7NfYUJCUneTVTGkjwoG` |
| Длина TG-поста | 2 коротких абзаца | 3 коротких абзаца |
| Заголовок-крючок в посте | «как врачи EMC помогают бороться с главной болезнью XXI века» | «Как работает новое решение от ВТБ Мои Инвестиции» |
| Изображение | Стоковая мед.сцена + крупный текстовый оверлей-крючок | 3D-рендер премиум-объекта (бриллиант) + крупный текстовый оверлей |
| Brand-mark на изображении | нет | нет |
| Disclaimer в подвале поста | `__*Реклама, АО Европейский Медицинский Центр__` | `__*Реклама, Банк ВТБ (ПАО), 18+__` |
| CTA | «рассказываем в нашем материале» | «рассказываем в нашем материале» |

## Шаблон нормализован

1. **Ссылка с `erid` обязательна.** Это не вкус Forbes, это требование закона о маркировке (см. [[canon-strict/legal-claims/ad-marking-russia-2026]]). Шаблон не рискует, прячет erid в query-параметре.
2. **URL-сегмент `/spetsproekt/` или `/special/`.** Это семантический сигнал «это партнёрский материал», читатель привычен.
3. **Изображение без brand-mark.** Принципиальное отличие от классического ad-баннера: бренд **не на картинке**, бренд — в подвале поста. Это «доверие к редакции > узнаваемость рекламодателя» подход. У читателя нет реакции «мне щас впарят», есть реакция «Forbes сделал материал на тему».
4. **Текстовый оверлей в стиле editorial cover.** Заголовок-крючок размещён прямо на изображении в верстке Forbes-cover-стиля — это позволяет посту работать как «обложка статьи», не как «баннер с CTA».
5. **Disclaimer курсивом в подвале + полное юр.лицо.** Минимально необходимый текст по закону, без эскалации (нет «ВНИМАНИЕ! РЕКЛАМА!»).
6. **CTA — мягкий: «рассказываем в нашем материале».** Не «купите», не «получите», не «узнайте сейчас». Editorial-тон сохраняется до финального байта.

## Почему это работает (гипотеза)

В контексте RU 2026, где **53% аудитории заявляет о баннерной слепоте** (см. [[evolving-strict/market-data/wciom-ad-perception-russia-2026]]) и **46% владельцев Telegram-каналов отказываются от размещения «рекламы MAX» как табу-категории** (см. [[evolving/content-trends/telegram-native-formats]]), шаблон Forbes-нативки эксплуатирует **последний оставшийся слой доверия** — авторитет деловой редакции. Бренд платит **за отсутствие visible brand'а на креативе**, потому что visible brand = триггер баннерной слепоты. Это инверсия классической рекламной логики «больше brand, лучше recall».

## Кому это нужно использовать

| Тип бренда | Стоит ли копировать шаблон |
|---|---|
| Premium B2B услуги (медицина, фин.услуги, юр.услуги) | ✅ Да — целевая аудитория Forbes сама по себе сегмент |
| AI-продукты для бизнеса | ✅ Да — высокий information-density формат подходит для сложного продукта |
| B2C consumer (FMCG, мода, развлечения) | ❌ Нет — не та аудитория |
| GRO (B2C+B2SMB AI-продукт) | ◯ Условно — Forbes spetsproekt дорог; шаблон можно переиспользовать на Forbes-tier-2 (РБК, Коммерсантъ, Cossa) или на собственном лендинге |

## Что GRO может перенять без покупки Forbes

Форма шаблона воспроизводима и без federal-tier площадки:

1. **Image cover в editorial-стиле**, не баннер. Текст-крючок на картинке — да, лого бренда — нет (или маленькое в углу).
2. **CTA-формулировка «рассказываем в нашем материале»**, а не «купите/попробуйте». Тестировать в A/B.
3. **Long-form landing вместо product page**. Шаблон Forbes ведёт на статью, а не на checkout. Для GRO это `groapp.ru/blog/<slug>` или `lk.groapp.ru/onboarding-stories`, не на paywall.

## Подтверждение шаблона на 4 свежих кейсах (май 2026)

Через [[sources/2026-05-05-tg-forbesrussia-may-4-5-2026|@forbesrussia 4–5 мая 2026]] поступили **4 новых нативных размещения за 2 дня** — что **подтверждает шаблон как production-устойчивый** (это не одиночный сезонный пик, а постоянный поток).

| Кейс | ID | Disclaimer | URL-сегмент | Изображение | Тип |
|---|---|---|---|---|---|
| Go Invest «Время для венчура» (Хуторов) | 95605 | `__*Информационная поддержка__` | `blogs.forbes.ru/2026/04/23/...` | editorial-cover Forbes spetsproekt | колонка эксперта |
| HUTTON НАОС промпарк | 95615 | `__* Реклама ООО «АНГАРА»__` | `forbes.ru/spetsproekt/...?erid=` | industrial-park рендер | spetsproekt |
| Будь Здоров / Ингосстрах медфраншизы | 95636 | `__* Информационная поддержка__` | `forbes.ru/brandvoice/...` | editorial-cover | brandvoice |
| Go Invest «Снижение ставки» (Григорьев) | 95650 | `__*Информационная поддержка__` | `blogs.forbes.ru/2026/04/29/...` | editorial-cover | колонка эксперта |

### Sub-pattern 1: «Информационная поддержка» disclaimer

**3 из 4 свежих кейсов** используют формулировку **«Информационная поддержка»** вместо «Реклама» в качестве disclaimer. `[conf:high, src:2026-05-04]` Это **более мягкий регистр** — формально не «реклама», а «информационное сотрудничество», с нюансами:

- **Юридически:** «Информационная поддержка» означает **не платное размещение**, а партнёрский материал (например, бесплатное информационное сопровождение клиентского события). Erid в URL отсутствует, но есть полный disclaimer внизу. `[conf:medium, src:2026-05-05]`
- **С маркетинговой точки зрения:** disclaimer мягче → читатель не reactiveн → доверие выше. **Но**: при росте FAS-проверок может стать рискованным шаблоном — формальной маркировки нет.
- **Кому подходит:** долгие партнёры Forbes (Go Invest как пример — несколько колонок за месяц), некоммерческие/PR-инициативы, эксперты из bench-pool редакции.

### Sub-pattern 2: «Колонка эксперта» как формат

Go Invest использует **колонки на blogs.forbes.ru** (а не статьи на forbes.ru/spetsproekt) — это **отдельная под-площадка** Forbes для авторских мнений. Преимущества:

- **Editorial-credibility** — даже сильнее, чем spetsproekt: автор с именем, должностью (директор по развитию внебиржевых продуктов), персональная подпись.
- **CTA через имя автора**: «в своей колонке рассказал Андрей Хуторов» — читатель идёт за конкретным экспертом, не за брендом.
- **Серийная природа**: Go Invest публикуется регулярно (3 разных автора за 2 недели) — это **PR-стратегия типа content drumbeat**, а не одиночное размещение.

### Sub-pattern 3: «Brandvoice» зона Forbes

«Будь Здоров / Ингосстрах» (95636) опубликовался в URL-сегменте `forbes.ru/brandvoice/...` — это **третья выделенная зона Forbes** для нативных публикаций (помимо spetsproekt и blogs):

- **Brandvoice** = бренд-журнал Forbes (англ-аналог: forbes.com/brandvoice/)
- Автор материала: **«рассказывает Родион Ступин, генеральный директор сети клиник “Будь Здоров”»** — то есть формат «бренд-герой расскрывает экспертизу».
- Tone: editorial, без CTA-баннеров, fact-base (отраслевые исследования). 

**Итог по sub-patterns:** Forbes-нативка 2026 — **не один шаблон, а 3-уровневое меню**:
1. **Spetsproekt** (формальная реклама с erid, disclaimer «* Реклама ООО ...») — для разовых размещений с регуляторной прозрачностью.
2. **Blogs (колонка эксперта)** — для drumbeat-партнёров, мягкий disclaimer «Информационная поддержка», editorial-credibility.
3. **Brandvoice** — для бренд-журнал материалов, autorship от CEO/директоров, образовательный формат.

GRO-маркетинг при будущем рассмотрении Forbes-площадки должен **выбирать формат под цель**: trial-размещение → spetsproekt; long-term presence → blogs (колонка от Кости Егошина или другого эксперта); thought leadership → brandvoice (через интервью с фаундером).

## Третье подтверждение шаблона (4 кейса 7–8 мая 2026)

Через [[sources/2026-05-19-tg-forbesrussia-20260519-104004|@forbesrussia 7–8 мая 2026]] поступили **ещё 4 нативных размещения за 2 дня**. Это **третий замер** (после 13-14 апреля и 4-5 мая) — шаблон окончательно подтверждён как production-устойчивый постоянный поток, а не сезонная аномалия.

| Кейс | ID | Disclaimer | Зона / URL-сегмент | Текст-оверлей на обложке | Тип |
|---|---|---|---|---|---|
| Кронунг «Обратная диджитализация» (Филипп Шраге) | 95707 | `__*Информационная поддержка__` | `blogs.forbes.ru/2026/05/07/...` | без жирного оверлея | колонка эксперта |
| PropTech Яндекса «УК 2.0» (Дарья Воронова) | 95724 | `__*Информационная поддержка__` | `blogs.forbes.ru/2026/04/28/...` | «**УК 2.0:** почему ИИ становится главным драйвером эффективности УК» | колонка эксперта |
| Alfa-Bank «Сложнее теста Тьюринга» (методика оценки ИИ-агентов) | 95740 | `__*Информационная поддержка__` | `forbes.ru/brandvoice/...` | «**KPI найдутся для каждого:** в Альфа-Банке внедрили новую методику оценки ИИ-агентов» | brandvoice |
| Форум недвижимости «Движение» (Сочи 16-19 июня) | 95749 | `__*Реклама, ООО "Форум недвижимости Движение. Москва"__` | `dvizhenie.ru/forum?...&erid=2SDnjcjAcUS` | event-промо | spetsproekt/event (erid) |

### Что подтверждают эти кейсы

1. **«Информационная поддержка» закрепилась как доминирующий disclaimer** для editorial-форматов: **3 из 4** новых кейсов (Кронунг, PropTech, Alfa-Bank). Совпадает с замером 4-5 мая (тоже 3 из 4). Это устойчивый sub-pattern, не разовый. `[conf:high, src:2026-05-08]`
2. **Brandvoice расширяется на AI-тематику.** Alfa-Bank (95740) — кейс brandvoice про методику оценки ИИ-агентов: бренд-герой (Станислав Милых, руководитель дирекции ботов и ассистентов Альфа-Банка) раскрывает экспертизу через образовательный формат «может задать отраслевой стандарт». Это **AI-продукт в формате brandvoice** — прямой референс для будущих GRO-размещений.
3. **Editorial-cover с жирным текст-оверлеем слева** — устойчивый визуальный код: «**УК 2.0:**» (95724), «**KPI найдутся для каждого:**» (95740). Двоеточие после жирного хука + продолжение обычным шрифтом. Brand-mark отсутствует на обоих. Это та же верстка, что у апрельских EMC/ВТБ.
4. **Event-промо использует полноценную «Реклама»+erid** (95749, форум «Движение») — для коммерческих событий с конкретным CTA сохраняется формальная маркировка, в отличие от editorial-колонок. Подтверждает выбор формата под цель.

**Содержательные сигналы этих размещений** разнесены в отдельные слои: PropTech-кейс → [[evolving/industry-trends/proptech-ai-housing-management-ru-2026]], Alfa-Bank AI-агенты → контекст [[evolving/industry-trends/industrial-ai-measurable-roi-2026]].

## Четвёртое подтверждение шаблона (8-11 мая 2026) + расширение в franchise-территорию

Через [[sources/2026-05-26-tg-forbesrussia-may-8-11-2026|@forbesrussia 8-11 мая 2026]] поступили **2 новых native-ad кейса** (95757 MTS Optimus, 95759 Forbes Club event-promo) **плюс 2 кейса editorial-franchise-уровня** (95789 Forbes×Серебряный дождь, 95802 FOMOиYOLO 6-platform). Это **четвёртый замер**: pattern окончательно canon, плюс появляется **adjacent-territory** — editorial-franchise за пределами рекламной нативки.

### Native-ad кейсы 8-11 мая

| Кейс | ID | Disclaimer | Зона / URL-сегмент | Текст-оверлей | Тип | Brand-mark? |
|---|---|---|---|---|---|---|
| MTS Optimus «Что предприниматели недооценивают» (Бутковская) | 95757 | `__*Информационная поддержка__` | `blogs.forbes.ru/2026/05/04/...` | дублирует заголовок поста | колонка эксперта | **есть (логотип MTS Optimus в углу)** |
| Forbes Club бизнес-завтрак (Гук, ОБИТ) | 95759 | — (no disclaimer, чисто промо клуба) | `clubforbes.ru/` | event-cover | внутренний event-промо | — |

### Ключевое наблюдение: первое отступление от brand-mark-less канона

**MTS Optimus (95757)** — это **первый зафиксированный случай**, когда в blogs/«Информационная поддержка» кейсе на обложке **есть видимый brand-mark** (логотип MTS Optimus в углу). `[conf:high, src:2026-05-08]` Это отступление от классического принципа Forbes-нативки «бренд **не на картинке**, бренд — в подвале поста» (см. шаблон выше, sub-pattern #3).

**Возможные интерпретации:**

1. **Договор с крупным брендом**: MTS — это не одиночный кейс, а **корпорация уровня top-3 в РФ** ("трудно спрятать" brand в editorial-обложке). Forbes может торговать brand-mark-allowance под конкретного клиента.
2. **Эрозия канона**: со временем шаблон может смещаться к «editorial-cover + small brand-mark» — как способ повысить ad recall без уровня агрессии классического баннера. Нужны последующие замеры, чтобы понять, аномалия это или начало drift'а.
3. **Особая зона MTS Optimus**: возможно, MTS Optimus имеет более тесное партнёрство с Forbes (как Go Invest), и для них доступен расширенный набор форматов.

**Следующий замер должен проверить, есть ли brand-mark в новых blogs-кейсах от других брендов**. Если 2-3 кейса подряд с brand-mark — это смена шаблона, нужен update основной таблицы. Пока что **canonical pattern остаётся «без brand-mark»**, MTS — задокументированное исключение.

### Содержательный сигнал MTS Optimus кейса

Сам кейс — глубинные интервью с владельцами SMB про **«разрушение бизнеса изнутри»** — содержательно релевантен для marketing-memory GRO и разнесён в [[canon/target-audience/ru-smb-founder-owner-seller]] (founder-owner-seller подтверждение). См. также [[evolving-strict/market-data/ifors-smb-anxiety-2026]] — независимое quantitative подтверждение того же sentiment'а (IFORS 63%).

### Editorial-franchise расширение (95789, 95802)

Параллельно нативно-рекламному pattern'у в этом дампе видны **2 устойчивых editorial-franchise шаблона** Forbes-редакции, расширяющих бренд в смежные каналы:

- **Forbes×Серебряный дождь (95789)** — еженедельная FM-программа «Набутов здесь. Forbes», конвертация эфира в подкаст. Это **co-branded editorial product**, не нативка.
- **FOMOиYOLO (95802)** — 6-platform cross-stream подкаст-дистрибуция Forbes Young (forbes.ru сайт, Apple Podcasts, Яндекс Музыка, Telegram bot, Spotify, mave.digital).

Оба — **editorial-franchise**, не платная нативка: в них **нет erid**, **нет «Информационная поддержка»**, **нет рекламодателя**. Forbes использует свой бренд для расширения в смежные каналы (радио, multi-platform подкастинг). Это **другой контент-юнит** и заслуживает отдельной страницы — см. [[evolving/content-trends/forbes-radio-cross-media-franchise]].

**Важно для GRO**: Forbes-аудитория сейчас потребляет контент в **3 параллельных контурах**:
1. Web/Telegram editorial (основной поток)
2. Native-ad материалы (3-tier меню: spetsproekt/blogs/brandvoice)
3. Editorial-franchise (radio program + multi-platform podcast)

Реклама GRO в любом контуре требует **разной упаковки** и разной экономики.

## Сиблинг-шаблон на другой площадке

Forbes-формат — не единственный устойчивый RU-native-шаблон 2026. Параллельно на vc.ru/<B2B-categories> закрепился другой паттерн — **«Топ-N ИИ-инструментов» advertorial с 🥇-медалью на одном инструменте**. Разбор и сравнение двух шаблонов — в [[evolving/content-trends/vcru-top10-advertorial-pattern-2026]]. Ключевые различия: Forbes прячет бренд под editorial-обложкой (1 бренд, editorial-материал, erid в URL), vc.ru прячет бренд за «объективностью рейтинга» (8–12 брендов, честная критика 9 конкурентов валидирует #1, часто без явной erid-маркировки).

Оба шаблона — производные общего принципа «commercial-intent-skepticism bypass», описанного в [[canon/marketing-frameworks/native-advertising]] через Nutella-кейс, но адаптированного под разные сегменты (B2C premium vs B2B SaaS).

## Связанные страницы

- [[canon/marketing-frameworks/native-advertising]]
- [[canon-strict/legal-claims/ad-marking-russia-2026]]
- [[evolving/industry-trends/native-pr-russia-2026]]
- [[evolving/content-trends/telegram-native-formats]]
- [[evolving/content-trends/vcru-top10-advertorial-pattern-2026]] — сиблинг-паттерн B2B SaaS
- [[evolving-strict/market-data/wciom-ad-perception-russia-2026]]
- [[volatile-strict/industry-news/vtb-intellect-ai-investing-2026]]
- [[sources/2026-04-14-tg-forbesrussia-apr-13-14]]
- [[sources/2026-04-10-piarhub-research-native-pr-2026]]
- [[sources/2026-05-05-tg-forbesrussia-may-4-5-2026]] — 4 свежих кейса май 2026 + sub-patterns
- [[sources/2026-05-19-tg-forbesrussia-20260519-104004]] — третье подтверждение, 4 кейса 7-8 мая 2026
- [[evolving/industry-trends/proptech-ai-housing-management-ru-2026]] — содержательный сигнал кейса 95724
- [[evolving/industry-trends/industrial-ai-measurable-roi-2026]] — контекст Alfa-Bank AI-агенты кейса 95740
- [[evolving/content-trends/forbes-30-under-30-content-franchise]] — другой устойчивый Forbes editorial pattern (multi-edition контент-актив, founder-listicle архетип)
- [[evolving/content-trends/forbes-200-richest-russia-content-franchise]] — третий устойчивый Forbes editorial pattern (wealth-listicle архетип, sibling 30 Under 30)
- [[sources/2026-05-26-forbes-tegi-200-bogateyshih-biznesmenov]] — sibling tag-page Forbes-франшизы wealth-listicle
- [[sources/2026-05-26-tg-forbesrussia-may-8-11-2026]] — 4-й замер pattern'а: 2 native-ad кейса (MTS Optimus с brand-mark — первое отступление; Forbes Club event-promo) + 2 editorial-franchise (Серебряный дождь, FOMOиYOLO)
- [[evolving/content-trends/forbes-radio-cross-media-franchise]] — adjacent-territory: Forbes×Серебряный дождь FM + FOMOиYOLO 6-platform podcast cross-stream

## Backlinks

_12 pages link to this one._

- [[evolving/content-trends/dzen-republication-preview-pattern-2026]]
- [[evolving/content-trends/hh-ru-blog-content-patterns]]
- [[evolving/content-trends/inc-russia-longform-pattern-2026]]
- [[evolving/content-trends/ru-sales-infobiz-content-patterns]]
- [[evolving/content-trends/vcru-top10-advertorial-pattern-2026]]
- [[index]]
- [[sources/2026-04-14-tg-forbesrussia-apr-13-14]]
- [[sources/2026-04-14-vcru-garmony-top10-hr-ai-advertorial]]
- [[sources/2026-05-05-tg-forbesrussia-may-4-5-2026]]
- [[sources/2026-05-05-tg-mspiridonov-apr-may-2026]]
- [[sources/2026-05-05-tg-vyakuba-apr-may-2026]]
- [[volatile-strict/industry-news/vtb-intellect-ai-investing-2026]]
