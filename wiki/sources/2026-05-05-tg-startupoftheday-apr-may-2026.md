---
id: mkt:sources/2026-05-05-tg-startupoftheday-apr-may-2026
title: "Telegram @startupoftheday (Александр Горный) — re-dump 50 постов apr 6 — may 5 2026"
type: source
layer: evolving
theme: content-trends
tags: [telegram, startupoftheday, gorny, daily-digest, venture, ai-energy, ai-token-deflation, claude-course, ai-tutor]
confidence: medium
created: 2026-05-05
updated: 2026-05-05
original: raw/processed/articles/tg_startupoftheday_20260505-131619.md
bundle_children:
  - raw/processed/media/tg_startupoftheday_5041.jpg
  - raw/processed/media/tg_startupoftheday_5042.jpg
  - raw/processed/media/tg_startupoftheday_5003.jpg
  - raw/processed/media/tg_startupoftheday_5007.jpg
  - raw/processed/media/tg_startupoftheday_5018.jpg
  - raw/processed/media/tg_startupoftheday_5022.jpg
  - raw/processed/media/tg_startupoftheday_5026.jpg
bundle_primary: raw/processed/articles/tg_startupoftheday_20260505-131619.md
namespace: mkt
---

# Telegram @startupoftheday — re-dump 50 постов (2026-04-06 → 2026-05-05)

Третий ingest канала Александра Горного. Дамп охватывает ids 4999..5052, **существенный overlap** с двумя предыдущими ingests:

- **Overlap с [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]]:** ids 4999..5013 (14 постов, apr 6 — apr 14) — уже обработаны полностью.
- **Overlap с [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]]:** ids 5014..5036 (22 поста, apr 15 — apr 27) — уже обработаны полностью.
- **DELTA (новые посты):** ids 5037..5052 (16 постов, apr 28 — may 5 2026). Этот ingest обрабатывает **только дельту**.

Содержательно — третий backfill scheduled task'а «Стартап дня (Александр Горный)». Тот же author voice, та же композиция (1 «стартап дня» / день + субботние ретроспективы + #простомысли + advertorials), что и в первых двух ingests.

## Метаданные

- **Тип:** Telegram-канал re-dump (text + 7 image children в bundle, из них 5 уже в `raw/processed/` от предыдущих ingests, 2 новых — `5041.jpg`, `5042.jpg`)
- **Канал:** [@startupoftheday](https://t.me/startupoftheday) — «Стартап дня» Александра Горного
- **Период:** 2026-04-06 (пост 4999) → 2026-05-05 (пост 5052), 50 сообщений; **delta-период (новые):** 2026-04-28 (пост 5037) → 2026-05-05 (пост 5052), 16 сообщений
- **Дата добавления:** 2026-05-05 (backfill scheduled task)
- **Автор:** Александр Горный — ex-директор по стратегии Mail.ru Group, founder ShareAI клуба, ежедневный VC/startup-обозреватель. Полное bio см. в [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]].
- **Экспертность автора:** inferred (15+ лет VC-аналитики, ex-Mail.ru Group strategy director). `confidence: medium` для аналитических тезисов, `confidence: low` для разовых ремарок-наблюдений.
- **Sidecar note:** был — пользователь маркирует канал как «временный контекст для трекинга новостей и трендов. Если есть какие-то релевантные инсайты в другие категории — можно их вычленить». Volatile-first обработка.
- **Sensitive flag:** none — публичный канал, PII отсутствует.

## Делта-постов: 16 новых сообщений (5037..5052)

| ID | Дата | Тип | Содержание | Релевантно? |
|---|---|---|---|---|
| 5037 | 04-28 | foreign startup | Lumia Health — умная серёжка для головной боли, $17M раунд, без FDA | low — foreign hardware-AI, weak signal |
| 5039 | 04-28 | job posting | Поиск CMO-сооснователя для CLAV (Berlin BAД, ~€2M ARR) | irrelevant — конкретная вакансия, без рыночного инсайта |
| 5040 | 04-29 | author note | Две загадки про спам в Telegram | irrelevant — открытые вопросы без фактуры |
| 5041 | 04-29 | advertorial | Avito Работа promo: 20M соискателей/месяц + 500 бонусов за вакансию | medium — RU labor-market metric anchor |
| 5042 | 04-30 | weekly TOC | Новости недели на YouTube (TOC из 19 пунктов) | low — re-confirmation формата, новый thumbnail |
| 5043 | 04-30 | foreign startup (signal) | **Ilant Health** — 3-уровневая терапия ожирения для корпораций (psy → Ozempic → хирургия), risk-sharing pricing, $22M раунд | medium-high — corporate-wellness vertical AI |
| 5044 | 04-30 | **own promo (signal)** | **Курс «Claude Code для предпринимателя»** с Григорием Шевченко, старт 2026-05-16 | high — Горный запускает свой обучающий продукт |
| 5045 | 05-01 | personal | Шоколад 100→80г | irrelevant |
| 5046 | 05-01 | personal | Le Sallay banking — рефлексия про потери разных типов | low — личная философия без рыночного контекста |
| 5047 | 05-02 | retro | Instoried 4 года назад #субботнийповтор (закрылся pre-ChatGPT) | irrelevant — historical, продукт мёртв |
| 5048 | 05-02 | own promo (signal) | **Ответ на «зачем курс если всё бесплатно есть» — фильтр-thesis** | medium — content-hook о ценности курсов |
| 5049 | 05-03 | **author thesis (signal)** | **«Дефицит электростанций»** — расчёт что AI-энергозатрат 0.1% ВВП планеты | high — counter-anchor против AI-energy panic |
| 5050 | 05-04 | foreign startup | Agriodor — феромоны вместо пестицидов, €15M, France | low — foreign agritech, weak signal |
| 5051 | 05-04 | own promo (signal) | Курс Claude Code — для офлайн-бизнеса (positioning Q&A) | medium — расширение target audience |
| 5052 | 05-05 | **author thesis (signal)** | **«О дорогих токенах»** — token-pricing decline thesis с конкретными числами | high — token-deflation rebuke + concrete pricing |

## Медиа-вложения (delta — только новые children)

Из 7 image-attached в bundle манифесте 5 уже в `raw/processed/` (5003, 5007, 5018, 5022, 5026 — обработаны в предыдущих ingests). 2 новых (5041, 5042) обработаны здесь.

| ID | Тип | Пост | Содержимое | Релевантность |
|---|---|---|---|---|
| 5041 | jpg | Avito Работа advertorial | Креатив advertorial: тёмно-фиолетовый фон, лого Avito Работа сверху, заголовок «Получайте бонусы за вакансии», иллюстрация — карточка «Вакансия размещена» с зелёной галкой + три цилиндрические монеты-бонусы синих/фиолетовых; «+500» бейдж снизу слева; ИНН 7710668349 ООО «КЕХ еКоммерц», erid 2VTzqWJMHzz | Низкая — типичный SaaS-рекламный креатив с focus на точечный stimulus («бонусы»). OCR ниже. |
| 5042 | jpg | YouTube thumbnail «Где польза от AI?!» | YouTube-обложка weekly news-roundup. Левая половина — портрет ведущего (тёмно-русые волосы, серая футболка, нахмуренный взгляд) на тёмно-городском фоне со «зданием с экранами». Правая половина — крупная типографика «Где / польза / от AI?!» белыми буквами + красная стрелка-«crash» вниз; верх — красный график-провал; нижний правый — газета «AI productivity study» с red-bar charts | Средняя — content-format reference, **новый thumbnail variant** для weekly-roundup-формата ([[evolving/content-trends/weekly-news-roundup-yt-format-gorny]]) — alarmism-метафора снова, но теперь про AI-productivity ('Где польза от AI?!'). Метафора повторяет паттерн apr 21 thumbnail (RUNET / кусачки) — типография + alarming framing + red-bar/crash visual. |

## Транскрипты медиа

В этом bundle нет audio/video children — только 2 новых статичных изображения.

## Релевантность

**Релевантно (извлечено в слои):**

1. **Горный thesis «Дефицит электростанций» (пост 5049)** — counter-anchor против AI-energy doom narrative. Расчёт на пальцах: для гарантированной экономической катастрофы (увольнение 50% white-collar в США) AI-выручка нужна 25% × 50% × 25% от ВВП = ~3%, при стоимости электричества 10% от цены токена → **0.1% ВВП планеты**. Существующей энергетике нужно прирасти на **3% доп. от обычного роста**. → новая страница `evolving/industry-trends/ai-energy-bottleneck-debunked-gorny-2026` (counter-narrative).

2. **Горный thesis «О дорогих токенах» (пост 5052)** — token-pricing deflation thesis с такси-аналогией (2009 vs 2026 в долларах, минимальных зарплатах, реальных рублях — реально дешевле, при том что качество выросло). Конкретные anchor-числа: GPT-4o $10/M token (2025), GPT 5.4-mini сильнее в 2.5 раза дешевле (за год), Deepseek V4 Flash в **40 раз** дешевле GPT-4o. Тезис: «AI дорожает» — это иллюзия фокусировки на лимитах, а не на эффективной стоимости качества. → новая страница `evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026` (strict — числа с inline-маркерами + cross-link с [[canon/marketing-frameworks/token-economics-cost-vs-value-amodei]]).

3. **Курс Claude Code от Горного × Шевченко (посты 5044, 5048, 5051)** — Горный + Григорий Шевченко (CEO агентства ~30 человек, опыт внедрения Claude Code в бизнес-процессы) запускают курс **«Claude Code для предпринимателя»** на платформе [claude.aiacademy.me](https://claude.aiacademy.me/), старт **2026-05-16**. Целевая аудитория — владельцы бизнеса и руководители (не программисты). Скидка до 3 мая. Positioning-тезисы: (а) курс не за «секретные знания», а за **фильтр** («автор выбрал важные темы из 1000»), (б) полезен для офлайн-бизнеса если есть «пара часов работы за компьютером в день или материальные расходы на компьютерных сотрудников». → новая страница `evolving/competitor-positioning/aiacademy-claude-code-course-gorny-shevchenko-2026` (новая категория конкурентов на RU AI-tutor рынке).

4. **Ilant Health — corporate-wellness vertical AI (пост 5043)** — 3-уровневая терапия ожирения для корпораций (психолог → Оземпик/GLP-1 → хирургическое уменьшение желудка), $22M раунд, ранее обещали **risk-sharing pricing** (плата как процент от фактической экономии); сейчас обещание со страницы исчезло. Обобщает тренд: corporate wellness ← vertical AI consulting → cost-of-employees attack vector. → enrich [[evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd]] (GLP-1 segment) + enrich [[evolving/industry-trends/ai-vertical-services-vc-uplift-2026]] (corporate wellness vertical).

5. **Avito Работа RU labor-market anchor (пост 5041)** — advertorial числа: **20 миллионов соискателей в месяц** на платформе Avito Работа (Горный ремарка: «о смене работы примерно столько россиян и думает»). Это **direct alternative** к hh.ru (см. [[evolving/competitor-positioning/hh-ru-career-marketplace]] / [[evolving/competitor-positioning/hh-ru-hrtech-platform]]) на RU-рынке найма. → enrich [[evolving/industry-trends/ru-labor-market-employer-turn-2026]] количественной точкой + новая competitor-страница `evolving/competitor-positioning/avito-rabota-job-platform-2026` (категория competitor-positioning, не маркетплейс).

6. **Lumia Health — foreign hardware-wellness (пост 5037)** — слабый сигнал, добавляется в общую таксономию через cross-link с CBInsights GLP-1 / здоровье-сегментом. Без отдельной страницы.

7. **Weekly news-roundup formats — новый thumbnail variant (пост 5042)** — подтверждение pattern и **expansion** thumbnail-метафор. Apr 21 thumbnail был «RUNET / кусачки» (RU-news alarmism). Apr 30 thumbnail — «Где польза от AI?!» (alarmism об AI-productivity, согласуется с тезисом 5035 «Невидимый ИИ» от того же автора). Оба используют alarming-question + red visual + газетный layout. → enrich [[evolving/content-trends/weekly-news-roundup-yt-format-gorny]] секцией про второй thumbnail-вариант.

**Нерелевантно (только в audit):**

- **Пост 5037 (Lumia Health)** — foreign медицинский hardware без direct relevance к GRO; просто упомянут в нашей таксономии. Без отдельной страницы.
- **Пост 5039 (CLAV CMO job)** — конкретная вакансия Berlin BAД, не маркетинговый инсайт.
- **Пост 5040 (загадки про спам)** — открытые вопросы автора без фактуры.
- **Пост 5045 (шоколад 80г)** — чисто off-topic.
- **Пост 5046 (Le Sallay)** — личная рефлексия о банкротстве школы, без рыночного контекста.
- **Пост 5047 (Instoried retro)** — рекап продукта 2022 года, мёртв в 2023 после ChatGPT.
- **Пост 5050 (Agriodor)** — foreign agritech (феромоны вместо пестицидов), €15M, не релевантно к GRO/AI/маркетингу. Хорошая иллюстрация alternative-to-pesticide бизнес-модели, но категория для GRO далёкая.

## Ключевые идеи

### 1. Горный thesis «AI-energy-bottleneck — миф» (пост 5049)

Базовый расчёт **на пальцах** (Горный делает в 5 шагов):

1. Зарплата всех белых воротничков в США ≈ **25% американского ВВП** (предположение)
2. Если AI уволит 50% — экономическая катастрофа (anchor)
3. Чтобы такая катастрофа стала реальностью, AI-стартапы должны иметь выручку **меньше 50%** от уволенных зарплат (никто не платит больше, чем экономит). Целевой estimate Горного: **25%**.
4. Отсюда AI-выручка = 50% × 25% × 25% = **3% ВВП**.
5. Стоимость электричества = **10%** от цены токена (estimate Горного, оверzhirованно).

**Финальный расчёт:** на «AI-революцию» нужна энергия = 0.1 × 0.3 × 0.25 × 0.5 × 0.25 = **0.1% ВВП планеты**. Существующей энергетике надо прирасти на **3% дополнительно от обычного роста**.

Вывод Горного: «По масштабам консервативной отрасли — много, но даже с дивана видно, что это возможно». Грандиозные запросы AI-компаний (миллиарды на gigawatts) — «примерно треть от моих расчётов».

**Тип Горный-сигнала:** counter-anchor против hype-discussions «AI остановит scaling из-за электричества». Тезис **доступен для контента GRO** как rebuttal-материал на тему «AI-революция отменяется».

### 2. Горный thesis «Токены дешевеют» (пост 5052)

Аналогия с такси:
- Такси Москва 2009 (тариф «дорогу покажешь», маршрут от Белорусской до юго-запада) — **400₽** = **$13** = **1/10 минимальной зарплаты**
- Такси Москва 2026 (эконом, тот же маршрут) — **868₽** = **$11.5** = **1/30 минимальной зарплаты** = **277₽ в рублях 2009** (с поправкой на инфляцию)

В абсолютных рублях такси «подорожало в 2 раза», но **в реальных деньгах подешевело**, при росте качества (страховка, новые машины, удобное приложение).

Аналогия с AI:
- GPT-4o (лучшая модель 2025), $10 за 1M исходящих токенов
- GPT 5.4-mini (через год, 2026) — **сильнее, в 2.5 раза дешевле**
- Deepseek V4 Flash (2026) — **в 40 раз дешевле** GPT-4o при сопоставимом качестве для большинства задач

**Тип Горный-сигнала:** counter-anchor против discussion «AI дорожает, лимиты ужесточаются». Готовая аналогия для контента (taxi-like commodity inflation reality).

### 3. Образовательный продукт от Горного × Шевченко

Горный + Григорий Шевченко (CEO агентства ~30 чел) запускают курс **«Claude Code для предпринимателя»** ([claude.aiacademy.me](https://claude.aiacademy.me/)). Старт **2026-05-16**, стартовая скидка до 3 мая.

Positioning через 3 поста (5044, 5048, 5051):
- **5044 (запуск)**: «Claude Code, или Codex, или Cursor — штуки, без которых уже нельзя». Аудитория — **владельцы бизнеса и руководители**, НЕ программисты. Опыт Шевченко: внедрение Claude Code в агентство 30 человек.
- **5048 (объекция «всё бесплатно есть»)**: «Ценность любого курса не в "секретных знаниях", а в **отборе полезного**. В фильтре, а не в количестве материалов». Если время бесконечно, денег мало → самому. Иначе → курс.
- **5051 (расширение target)**: для офлайн-бизнеса (например, владелец ресторана) полезен если «есть хотя бы пара часов работы за компьютером в день, или расходы на "компьютерных" сотрудников материальны».

**Это новая категория конкурентов** в RU AI-tutor сегменте: **founder-led practical course** (vs академические курсы AiAcademy.me доступа к моделям, vs no-code платформы типа [[evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026]]). Сегментация — entrepreneurs/owners, не разработчики.

### 4. Ilant Health и corporate-wellness vertical AI

3-уровневая терапия ожирения для корпораций (психолог → Оземпик → хирургия), $22M раунд. Уникальный pricing-механизм (теперь убран с сайта): **% от фактической экономии**, а не фиксированная плата. Это **risk-sharing model** — стартап разделяет с клиентом downside.

GLP-1 unicorn в [[evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd]] = 1 (2.3% доли). Ilant Health не unicorn, но **второй sample вокруг GLP-1 corporate-wellness категории** (уже подсегмент формируется: фарма-доступ + хирургия + employer-pay).

### 5. Avito Работа как RU-labor anchor

20M соискателей/месяц на Avito Работе. Для сравнения:
- hh.ru: ~10M MAU (см. [[evolving/competitor-positioning/hh-ru-career-marketplace]])
- Население РФ ≈ 144M, экономически активное ≈ 75M, white-collar ≈ ?

**20M = ~27% экономически активного населения РФ** (из comment'а Горного «о смене работы примерно столько россиян и думает»).

Это **dual-channel** RU labor market: hh.ru классифайд + Avito Работа classifeds-style на крупной горизонтальной площадке.

### 6. Weekly news-roundup thumbnail variants

| Дата | Метафора | Visual | Topic |
|---|---|---|---|
| 2026-04-21 | RUNET совсем не работает | Кусачки + ethernet кабель | Регуляторика РФ |
| 2026-04-30 | Где польза от AI?! | Crash-график + portrait + газета «AI productivity study» | AI-productivity (alarmism) |

Оба используют: alarming-вопрос/восклицание, red visual element, портрет ведущего слева, типографика справа. **Pattern сохраняется через 9 дней** = format уже стабильный, не разовый.

## Факты и цифры (delta)

- **Avito Работа:** 20 миллионов соискателей/месяц [Пост 5041]
- **Avito Работа:** 500 бонусов за каждую вакансию (промо акция) [Пост 5041]
- **Lumia Health:** $17M раунд [Пост 5037]
- **Ilant Health:** $22M раунд [Пост 5043]
- **GPT-4o (2025):** $10 за 1M исходящих токенов [Пост 5052]
- **GPT 5.4-mini (2026, по Горному):** в 2.5 раза дешевле GPT-4o при превосходстве [Пост 5052]
- **Deepseek V4 Flash (2026, по Горному):** в 40 раз дешевле GPT-4o [Пост 5052]
- **Энергозатраты AI-революции (Горный расчёт):** 0.1% ВВП планеты [Пост 5049]
- **Прирост энергетики необходимый:** 3% дополнительно к обычному росту [Пост 5049]
- **AI-выручка для катастрофы (Горный):** ~3% мирового ВВП = ~$1 трлн [Пост 5049]
- **Курс Claude Code (Горный + Шевченко):** старт 2026-05-16, скидка до 2026-05-03, агентство Шевченко ~30 человек [Посты 5044, 5051]
- **Agriodor:** €15M раунд, France, феромоны вместо пестицидов [Пост 5050]
- **Allbirds (упомянут в 5026 — overlap):** обувной бренд продал производство, купил GPU для нейросетей — pivot AI [уже covered в [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]]]

## Распознанный текст

### tg_startupoftheday_5041.jpg (Avito Работа advertorial)

Композиция:
- Тёмно-фиолетовый/индиго фон
- Сверху по центру: лого «Avito Работа» (мульти-цветная плойка-иконка слева + чёрный/тёмный текст)
- Заголовок крупно белым: «**Получайте / бонусы / за вакансии**» (с подчёркиванием слова «бонусы»)
- Иллюстрация в нижней половине:
  - Слева: телефон-карточка с зелёной галкой (✓) и подписью «Вакансия размещена»
  - Справа: две-три цилиндрические монеты-плитки в синих/фиолетовых тонах (символика Avito Кошелька)
- Снизу слева: фиолетовая plate-«+500» с пурпурной звездой-иконкой (бонус-валюта)
- Низ изображения: легальный disclaimer «**РЕКЛАМА. ООО "КЕХ ЕКОММЕРЦ". ИНН: 7710668349. ERID: 2VTZQWJMHZZ**»

Стилистика — типичный **SaaS rewards-promo креатив** с акцентом на single-stimulus (бонусы) + product-screenshot (vacancy подтверждена). Размещён в premium TG-канале (@startupoftheday) как advertorial.

### tg_startupoftheday_5042.jpg (YouTube thumbnail «Где польза от AI?!»)

Композиция YouTube-обложки:
- Левая треть: портрет мужчины (русые/тёмно-русые волосы, борода, серая футболка, чуть нахмуренный, серьёзный взгляд в камеру) на размытом тёмно-городском фоне (city skyline ночью с экранами)
- Сверху над портретом: красный crash-график ↘ (резкое падение)
- Правая две трети: типография крупно белыми буквами на тёмном **«Где / польза / от AI?!»** + красная стрелка-падение справа от «AI?!»
- Внизу справа: газета развёрнутая «**AI productivity study**» с красными bar-charts падения
- Композиционно — **alarmism-thumbnail** в стиле alarming question + red visual + portrait left
- Брендинг канала Горного — отсутствует видимый watermark/иконка

Метафора: AI-productivity «не работает», статистика падает, red-bar charts фиксируют crash. Это **content reference на пост 5035 «Невидимый ИИ»** того же канала (см. [[evolving/content-trends/invisible-ai-paradox-gorny-hook]]).

## Связанные страницы

### Создаются этим ingest'ом

- [[evolving/industry-trends/ai-energy-bottleneck-debunked-gorny-2026]]
- [[evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026]]
- [[evolving/competitor-positioning/aiacademy-claude-code-course-gorny-shevchenko-2026]]
- [[evolving/competitor-positioning/avito-rabota-job-platform-2026]]

### Обновляются

- [[evolving/content-trends/weekly-news-roundup-yt-format-gorny]] — новый thumbnail-вариант (Apr 30 «Где польза от AI?!»)
- [[evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd]] — Ilant Health как 2-й sample в GLP-1 corporate-wellness вертикали
- [[evolving/industry-trends/ai-vertical-services-vc-uplift-2026]] — Ilant Health corporate-wellness sub-segment
- [[evolving/industry-trends/ru-labor-market-employer-turn-2026]] — Avito Работа 20M MAU как 2-я anchor-точка (после hh.ru)
- [[evolving/content-trends/invisible-ai-paradox-gorny-hook]] — пост 5042 thumbnail как visual reference на тот же thesis

### Контекст

- [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]] — первый ingest того же канала (4961..5013)
- [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] — второй ingest того же канала (5014..5036)
- [[canon/marketing-frameworks/token-economics-cost-vs-value-amodei]] — Amodei thesis, complementary к Горному thesis
- [[evolving-strict/market-data/ai-coding-tools-cost-explosion-2026]] — opposite-side anchor (cost-overrun): Горный говорит о deflation на consumer pricing, эта страница — о explosion на enterprise high-volume
