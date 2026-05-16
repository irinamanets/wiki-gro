---
id: mkt:sources/2026-04-27-tg-startupoftheday-apr-15-27-2026
title: "Telegram @startupoftheday (Александр Горный) — дамп 15-27 апр 2026"
type: source
layer: evolving
theme: content-trends
tags: [telegram, startupoftheday, gorny, daily-digest, venture, ai-content-hooks, candidate-side-ai, autonomous-delivery, cbinsights, invisible-ai-paradox]
confidence: medium
created: 2026-04-27
updated: 2026-04-27
original: raw/processed/articles/tg_startupoftheday_20260427-152915.md
bundle_primary: raw/processed/articles/tg_startupoftheday_20260427-152915.md
bundle_children:
  - raw/processed/media/tg_startupoftheday_5018.jpg
  - raw/processed/media/tg_startupoftheday_5022.jpg
  - raw/processed/media/tg_startupoftheday_5026.jpg
namespace: mkt
---

# Telegram @startupoftheday — дамп 22 постов (2026-04-15 → 2026-04-27)

Второй ingest канала Александра Горного. Покрывает 13 дней (ids 5014..5036) и продолжает наблюдение, начатое в [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]] (дамп 23 марта – 14 апреля). Тот же author voice, тот же содержательный паттерн (ежедневный «стартап дня» + субботние ретроспективы + нерегулярные #простомысли + нативные рекламы).

## Метаданные

- **Тип:** Telegram-канал dump (text + 3 image children в bundle)
- **Канал:** [@startupoftheday](https://t.me/startupoftheday) — «Стартап дня» Александра Горного
- **Период:** 2026-04-15 (пост 5014) → 2026-04-27 (пост 5036), 22 сообщения
- **Дата добавления:** 2026-04-27 (backfill scheduled task «Стартап дня (Александр Горный)»)
- **Автор:** Александр Горный — ex-директор по стратегии Mail.ru Group, основатель ShareAI клуба, ежедневный VC/startup-обозреватель. Полный bio см. в [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]].
- **Экспертность автора:** inferred (см. предыдущий ingest), `confidence: medium` для его аналитических тезисов, `confidence: low` для ремарок-наблюдений.
- **Sidecar note:** был — пользователь маркирует канал как «временный контекст для трекинга новостей и трендов. Релевантные инсайты можно вычленить». Это явный signal: volatile-first обработка, извлекать только высокосигнальные hooks/frameworks, остальное в audit.
- **Sensitive flag:** none — публичный канал, PII отсутствует.

## Медиа-вложения

3 children в bundle. Captions полностью присутствуют в primary тексте (sidecars дублируют caption + source URL). Изображения в основном иллюстративные.

| ID | Тип | Пост | Содержимое | Релевантность |
|---|---|---|---|---|
| 5018 | jpg | Just AI Agent Platform Cloud (advertorial) | Креатив advertorial: «Agent Platform», pink-pastel ткань фон, бейдж «CLOUD», CTA «Зарегистрируйтесь и запустите первого агента сегодня» + 3 буллета фич | Низкая — типичный advertorial-креатив для уже задокументированной платформы (см. [[evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026]]). OCR ниже. |
| 5022 | jpg | ALSO электро-cargo-bike | Фото устройства: четырёхколёсный электробайк-телега бежевого цвета с большим грузовым отсеком, watercolor-инсталляция Bay Bridge на стенде сзади, лого ALSO на покрышке | Средняя — визуально подтверждает «странность» формы (телега ≠ велосипед), используется в [[volatile-strict/industry-news/also-electric-bike-delivery-2026-04]] |
| 5026 | jpg | YouTube thumbnail «RUNET совсем не работает» | YouTube-обложка выпуска Горного: левая половина — портрет ведущего (предположительно сам Горный или соведущий) в синей рубашке; правая — крупная типографика «RUNET / СОВСЕМ НЕ РАБОТАЕТ» + кусачки, перекусывающие синий ethernet-кабель. Бейдж «НОВОСТИ» внизу-слева. | Средняя — content-format reference для weekly news-roundup рубрики Горного (TOC из 20 пунктов) |

OCR/описание изображений см. ниже в `## Распознанный текст`.

## Транскрипты медиа

В этом bundle нет audio/video children. Все 3 attachments — статичные изображения.

## Релевантность

**Релевантно (извлечено в слои):**

1. **Candidate-side AI-сервисы (пост 5014)** — Горный артикулирует уже формирующуюся категорию: AI-tutor для соискателя, который пишет резюме, рассылает отклики, ведёт переписку с рекрутерами, готовит к интервью. Pricing 10% годового дохода. Российский pioneer существует (4+ года, anonymous). Это **новый жанр** в карьерной сегмент-карте — не ATS-оптимизация резюме, а полная аутсорс-замена соискателя ботом. → новая страница `evolving/industry-trends/candidate-side-ai-services-2026` + enrich [[evolving/content-trends/career-audience-hooks-2026]] hook 13.

2. **FirmPilot — vertical AI-marketing-as-a-service для юристов (пост 5017)** — $22M Round недавно, $4-9k/мес pricing, AI-AI-AI как primary value-prop (vs обычное низкомаржинальное full-service агентство). Горный явно артикулирует тезис: «один и тот же продукт у венчурного стартапа с инвестициями vs обычного агентства = разные оценки рынка». Это первый в нашей вики case-pin AI-marketing-агентства как venture-категории + готовый материал для [[evolving/competitor-positioning/firmpilot-ai-marketing-vertical-2026]] (новая страница) + сигнал для [[evolving/industry-trends/ai-vertical-services-vc-uplift-2026]] (новая страница, обобщение).

3. **Just AI Agent Platform Cloud (пост 5018, рекламный)** — advertorial с erid 2VtzquZcCs9, ИНН Маинд Крафт. Уже задокументирован в [[evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026]] как один из 5 RU no-code AI-agent платформ. Новая фактура в этом посте: cloud-вариант (не on-prem), drag-and-drop конструктор, готовые коннекторы к CRM/CMS/телефонии, бесплатный план + переход к платным тарифам. Также — это **второй advertorial Just AI** в @startupoftheday (signal частоты: повторяется как маркетинговый канал в «стартапах дня» Горного, а не разовая интеграция). → enrich `ru-nocode-ai-agent-platforms-2026` секцией с конкретикой по Cloud-варианту + reference на advertorial-format.

4. **ALSO электро-cargo-bike (посты 5022, 5029)** — $200M раунд, контракт с Doordash, регуляторная стратегия «прикинемся велосипедом» (педали-генератор электричества, не привод). Whoosh-параллель упомянута. → новая страница `volatile-strict/industry-news/also-electric-bike-delivery-2026-04` (news event с inline-маркерами) + новая страница `evolving/industry-trends/autonomous-delivery-vehicle-classification-2026` (regulatory-arbitrage таксономия, применимая к любому подобному сегменту).

5. **CBInsights unicorn breakdown 2026 (пост 5030)** — 43 новых unicorn YTD в 2026: 11 GenAI-applications, 5 AI-чипы, 5 робототехника+автопилоты, 2 foundation models, 2 боевых дрона, 2 нейроинтерфейса, 1 GLP-1 service, 15 «legacy» (финтех/медтех/крипта). Горный thesis: «к 2028 у legacy будет 10%, а не 35%». → новая страница `evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-yt-d` (4 числа = 4 inline-маркера обязательны).

6. **«Невидимый ИИ» — author thesis (пост 5035, verified expert, signal post)** — Горный объясняет MIT-парадокс «AI есть, ВВП не растёт» через простую ментальную модель: единственная быстрая feedback loop — продажи (только near-customer оптимизация даёт быстрый макроэффект). Backoffice-оптимизация → zero-sum конкурентная игра + удар по покупательной способности через увольнения = чистый минус для макро-выручки. Контейнерная аналогия. → новая страница `evolving/content-trends/invisible-ai-paradox-gorny-hook` (готовый content-hook + layer narrative) + enrich [[evolving/industry-trends/ai-productivity-j-curve-2026]] (новый 5-й data-point — Горный thesis).

7. **saas-rating.ru обновился до 2025 года (пост 5032)** — ежегодный рейтинг RU SaaS по налоговым данным, собирает Аскар Рахимбердиев (founder МойСклад). Это методологически **«самый честный рейтинг»** — не самоотчёт, а налоговая. → новая страница `evolving-strict/market-data/ru-saas-rating-2025` (resource-pin + методология).

8. **Weekly news-roundup YouTube format (пост 5026)** — Горный публикует TOC выпуска недели: 20 заголовков (политика, AI-сделки, тех-новости, регуляторика, забавное). Это формат-аномалия в @startupoftheday: 1 пост = вся неделя в одном TOC + push к YouTube. Использует thumbnail с типографикой и метафорой (RUNET / кусачки). → новая страница `evolving/content-trends/weekly-news-roundup-yt-format-gorny` (content-format reference).

9. **Webpagebot — Telegram URL-preview refresh (пост 5027)** — Горный обращает внимание на полезный, но скрытый бот @Webpagebot (30K MAU vs PremiumBot 13M). Полезно для маркетеров, кто работает с TG (после публикации сайт меняется → preview тоже надо обновить). → enrich [[evolving/content-trends/telegram-native-formats]] секцией про operational hint + cross-reference.

10. **Telegram comment-spam девушки-боты (пост 5023)** — наблюдение Горного: спам-боты-«красивые девушки» лайкают всё подряд → юзер заходит в профиль → реклама. Конверсия маленькая, но не ноль. Решение Горного: отключить лайки в комментариях. → новая страница `evolving/content-trends/tg-comment-spam-defense-2026` (anti-pattern + operational decision).

11. **Author opinion (пост 5021)**: Горный фиксирует marketplace-парадокс — в большинстве отраслей маркетплейсы выигрывают, но **биржи блогеров для рекламных интеграций** — устойчивое исключение, никто не понимает почему. Слабый, но любопытный сигнал для marketing-frameworks темы. → лёгкая enrich-запись в новой странице `evolving/industry-trends/influencer-marketplace-failure-paradox` (короткая страница-якорь под будущее накопление сигналов; сейчас 1 expert-opinion data-point с conf:low по фактике).

**Нерелевантно (только в audit):**

- **Пост 5016** — выдуманный мысленный эксперимент про «онлайн-компанию, которая не возвращается на рекламные кабинеты РФ» (без рыночного применения, личное наблюдение).
- **Пост 5019** — заметка про мероприятия (#личное).
- **Пост 5020** — Flowrite #субботнийповтор: ретроспектива закрывшегося стартапа из 2022 (пред-ChatGPT этап AI-копирайтинга, продукт мёртв). Не относится к 2026 и не даёт инсайтов.
- **Пост 5025** — про детей и тренеров (#личное).
- **Пост 5028** — author opinion про управление числами в больших компаниях. Слабая связка с маркетингом GRO; не извлекаем (можно вернуться, если повторится в трёх и более источниках).
- **Пост 5031** — короткая цитата «Выгорать дорого». Не достаточно фактуры.
- **Пост 5033** — Stilt #субботнийповтор: ретроспектива провалившегося финтех-API-стартапа из 2022. Не относится к 2026.
- **Пост 5034** — про лайк гадости друзьями (#личное).
- **Пост 5036** — TopHub advertorial (рекламная интеграция канала по менеджменту, без инсайтов).

## Распознанный текст

### tg_startupoftheday_5018.jpg (Just AI advertorial креатив)

Стилистика: pink-pastel шёлковая ткань с переливами как фон. Композиция:
- Верхний бейдж: круглая форма с белым текстом «CLOUD» на ярко-розовом фоне
- Главный текст: крупная типографика «**Agent Platform**» в светлом скруглённом боксе
- Нижний блок: иконка робота слева + «Зарегистрируйтесь и запустите первого агента сегодня» как заголовок CTA
- Три буллета на белом фоне:
  - «No-code для старта, Pro-code когда нужна кастомизация»
  - «Любая LLM на выбор: OpenAI, GigaChat, YandexGPT и другие»
  - «Один агент или целая мультиагентная система»

Композиционно — **типичный SaaS-креатив 2026** для advertorial-постов в TG: pastel-фон, читаемая типографика, 3 ключевые value-prop точки, CTA на регистрацию. Совпадает с advertorial-паттерном тех же advertorials, что Горный публиковал в первом ingest'е (Лавка, Сбер тендеры, Т-Банк), но визуально мягче — соответствует tech-аудитории канала.

### tg_startupoftheday_5022.jpg (ALSO электро-cargo-bike)

Фото устройства на стенде:
- Бежево-кремовый кузов с длинным горизонтальным грузовым отсеком сзади
- Четыре чёрных колеса с фиолетовой накладкой по центру (брендинг ALSO)
- На передней колесной декорации — лого «ALSO»
- В передней части — рулевая колонка с мотоциклетного типа рулём, седло
- Пурпурный/фиолетовый акцент на боковой панели передней секции
- Фон: масштабная фотография Bay Bridge (Сан-Франциско) с контейнеровозом → намёк на location презентации (Bay Area)

Визуально устройство **сильнее похоже на cargo-телегу или гольф-карт**, чем на велосипед. Подтверждает наблюдение Горного из caption: «Выглядит устройство на мой вкус скорее как телега, но компания предпочитает название "велосипед"». Регуляторная стратегия (педали-как-генератор) — это языковая arbitrage поверх явно automotive form-factor.

### tg_startupoftheday_5026.jpg (YouTube thumbnail «RUNET»)

Композиция YouTube-обложки в RU-news-roundup стиле:
- Левая треть: портрет мужчины (тёмные волосы, синяя рубашка, взгляд в камеру) на белом фоне — соведущий или сам Горный
- Правая две трети: типографика-апокалипсис «**RUNET** / **СОВСЕМ НЕ РАБОТАЕТ**» белыми буквами на красном «брызг»-фоне (имитация краски-кляксы)
- Иллюстрация под текстом: синий ethernet-кабель (RJ-45 разъём слева), зажатый профессиональными синими кусачками — момент перерезания
- Слева внизу: красный бейдж «**НОВОСТИ**» белыми буквами

Метафора прямая и провокационная: рунет «отключают» физически. Это reference на регуляторные RU-новости недели (см. также [[volatile-strict/industry-news/ru-vpn-telegram-restrictions-2026-04]] и [[volatile-strict/industry-news/ru-vpn-metering-proposal-2026-04]]).

## Связанные страницы

### Создаются этим ingest'ом

- [[evolving/industry-trends/candidate-side-ai-services-2026]]
- [[evolving/competitor-positioning/firmpilot-ai-marketing-vertical-2026]]
- [[evolving/industry-trends/ai-vertical-services-vc-uplift-2026]]
- [[volatile-strict/industry-news/also-electric-bike-delivery-2026-04]]
- [[evolving/industry-trends/autonomous-delivery-vehicle-classification-2026]]
- [[evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd]]
- [[evolving/content-trends/invisible-ai-paradox-gorny-hook]]
- [[evolving-strict/market-data/ru-saas-rating-2025]]
- [[evolving/content-trends/weekly-news-roundup-yt-format-gorny]]
- [[evolving/content-trends/tg-comment-spam-defense-2026]]
- [[evolving/industry-trends/influencer-marketplace-failure-paradox]]

### Обновляются

- [[evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026]] — Just AI Cloud-вариант + advertorial frequency signal
- [[evolving/content-trends/career-audience-hooks-2026]] — новый Hook 13 (candidate-side AI-аутсорс)
- [[evolving/industry-trends/ai-productivity-j-curve-2026]] — Горный thesis как 5-й data-point
- [[evolving/content-trends/telegram-native-formats]] — Webpagebot operational hint
- [[volatile/weekly-digest/startupoftheday-mar-apr-2026]] — расширение даты (или, опционально, новый weekly-digest для apr 15-27)

### Контекст

- [[sources/2026-04-14-tg-startupoftheday-mar-apr-2026]] — предыдущий dump того же канала
- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] — base framework для FirmPilot pricing-разбора
- [[evolving/industry-trends/software-moat-erosion-2026]] — context для «AI-AI-AI vs обычное агентство» Горного
