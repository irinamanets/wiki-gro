---
id: mkt:sources/2026-04-14-tg-bezsmuzi-apr-12-14
title: "Telegram @bezsmuzi (Максим Кульгин) — дамп 50 постов, 12–14 апреля 2026"
type: source
layer: volatile
theme: raw-notes
tags: [source, telegram, news, ai-trends, ru-platform-access, kulgin]
confidence: medium
created: 2026-04-14
updated: 2026-04-14
original: raw/processed/articles/tg_bezsmuzi_20260414-140242.md
namespace: mkt
---

# Telegram @bezsmuzi — дамп 50 постов (12–14 апреля 2026)

## Метаданные

- **Тип:** Telegram channel dump (Markdown + 49 медиафайлов: 42 изображения + 7 видео)
- **Источник:** https://t.me/bezsmuzi
- **Автор:** Максим Кульгин — предприниматель, основатель clickfraud.ru, poisk.im, xmldatafeed.com (Санкт-Петербург). Упоминает эти проекты в постах 15254, 15263, 15284, 15285, 15286.
- **Экспертность автора:** inferred (medium) — self-described как действующий IT-предприниматель с несколькими коммерческими продуктами (parsing, защита от кликфрода, товарный поиск). Канал = ежедневные личные заметки про IT/AI/рынок РФ, не первоисточник новостей.
- **Дата сбора:** 2026-04-14 14:02 UTC
- **Диапазон постов:** id 15237–15286 (50 сообщений) за 2026-04-12 — 2026-04-14
- **Sidecar note:** был — «источник новостей по тематике Телеграм-Авторские, для написания своих постов и новостей в блоге нашего сервиса; временный контекст для трекинга трендов». Classification-guide: извлекаем только то, что можно переиспользовать как сырьё для контента.
- **Sensitive flag:** none

## Релевантность

Большая часть постов — личные наблюдения и мемные заметки без фактуры, которые не создают новых страниц в слоях. В `volatile/` уходят:

1. **AI-model news кластер** (15240 DeepSeek V4, 15243 Qwen 3.6-Plus, 15260 AI pricing, 15261 Software Meltdown, 15269 ChatGPT-6 «Spud», 15275 MiniMax M2.7, 15278 Dreamina/Seedance 2.0) — это secondary-retelling свежих релизов, confidence: low-medium, homes в `volatile/weekly-digest`.

2. **RU platform-access кластер** (15242 top downloads RU — 9 VPN + MAX #10, 15248 VPS цены +500–700%, 15262 WB/Сбер сбои, 15268/15273/15282/15283 блокировки Telegram и миграция в MAX) — темпоральный сигнал про доступность каналов, home в `volatile/raw-notes`.

3. **Content-trend reinforcement** (15256 — «куда делись продавцы курсов WB? стали ИИ-коучами и владельцами контент-заводов») — слабое, но именованное подтверждение нарратива про смену инфобиз-фронтира; добавляется как cross-signal в `evolving/content-trends/ai-solopreneur-narrative-hooks`.

4. **MAX reinforcement** (15242 — MAX на 10 месте в топ загрузок РФ при 9 VPN впереди; 15282 — Кульгин запустил Telegram→MAX бота, отмечает что «часть аудитории перейдёт в MAX, вопрос времени») — уточняет профиль MAX в `evolving/competitor-positioning/max-messenger`.

Нерелевантные посты (audit only, в слои не уходят): 15237 (мем ZeroGPT), 15238 (udemy downloader), 15239 (Perplexity Pro личный вопрос), 15241 (ВПН-граффити), 15244 (поздравительная открытка), 15245–15247 (без фактуры), 15249 (цветы), 15250 (эйджизм), 15251 (заградительные цены), 15252 (гуманоид Unitree — физика, не рынок), 15253 (курятина в Саратове), 15254 (use-case Qwen для NDA — приватный кейс), 15255 (paid promo «Миллиарды по приколу»), 15257 (ставки депозитов юрлиц), 15258 (my-translator OSS), 15259 (SIM-спам), 15263 (poisk.im + Я.Маркет affiliate — приватный кейс), 15264 (paid promo block.talk), 15265–15267 (офтоп), 15270 (курс рубля), 15271 (рынок IT в РФ — мнение без данных), 15272 (иллюстраторы), 15274 (безработица гуманоидов), 15276–15277 (мемы), 15279 (paid promo VK Tech вебинар), 15280 (HR в РФ — мнение), 15281 (HR-тест на северокорейцев), 15284–15286 (приватные кейсы автора).

## Ключевые идеи

- **Weekly AI-model drop** (12–14 апреля): сразу 4 заметных анонса (DeepSeek V4, Qwen 3.6-Plus, ChatGPT-6 «Spud», MiniMax M2.7) + видео-модели (Dreamina/Seedance 2.0). Плотность релизов за 3 дня — сигнал «горячей» недели.
- **RU platform-access turbulence:** 9 из топ-10 загрузок приложений в РФ — VPN-сервисы, MAX на 10 месте. Параллельно VPS-цены под VPN взлетели в 5–7x. Это маркетинговый сигнал о том, **где** пользователи сейчас концентрируются и **через что** они туда попадают.
- **Telegram blocking рабочая гипотеза:** блокировки Telegram в РФ стали предметным событием (упоминания 15262, 15268, 15273, 15282, 15283), и авторы (включая самого Кульгина, см. [[sources/2026-04-14-tg-founderwoman-feb-apr-2026]]) массово готовят Telegram→MAX мосты. Кульгин лично запустил такой бот для своего канала.
- **Software Meltdown нарратив** (15261): автор пересказывает чужой тезис, что SaaS за 5–50к ₽/мес теряет ценность из-за AI; остаются free-софт и enterprise. Сам автор не соглашается — это не утверждение, а маркер того, что дискурс в маркет-комьюнити активный.
- **«Куда делись инфобизнесмены WB»** (15256): народное объяснение — стали ИИ-коучами и владельцами контент-заводов. Это ложится поверх существующего тренда [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]].

## Факты и цифры

Все цифры — **retold** через канал Кульгина, не первоисточник. В `volatile/` уходят без inline-маркеров (loose layer), но с датой источника в тексте.

- Топ загрузок РФ 2026-04-12: позиции 1–9 — VPN-сервисы, позиция 10 — MAX (15242)
- VPS под VPN 2/2 и 2/4: 4–5к ₽/мес; 8/12: 10к+ ₽/мес, рост 500–700% с начала 2026 (15248)
- DeepSeek V4: релиз конца апреля 2026, многоуровневый режим (15240)
- Qwen 3.6-Plus: #1 в Daily/Weekly/Trending OpenRouter одновременно, доступна на OpenRouter/Fireworks/Alibaba Cloud Model Studio/Qwen Cloud (15243)
- ChatGPT-6 «Spud»: релиз 2026-04-14, автономные агенты, контекст 2 млн токенов (со слов Альтмана, retold) (15269)
- MiniMax M2.7: opensource, SWE-Pro 56.22%, Terminal Bench 2 57.0%, non-commercial лицензия (15275)
- Dreamina by ByteDance на базе Seedance 2.0 — видео-модель (15278)
- Цена AI-токенов: $150 за 1 млн output токенов (15260, модель не названа — вероятно Claude Opus или GPT-4 Turbo класса)
- Unitree гуманоид: 10 м/с vs Усейн Болт пиковые 12,4 м/с (15252)
- Курс USD/RUB 2026-04-13: <76 ₽, минимум с весны 2023 (15270)

## Связанные страницы

- [[volatile/weekly-digest/ai-model-releases-2026-w15]] — AI релизы недели 12–14 апреля (выжимка из 7 постов)
- [[volatile/raw-notes/ru-platform-access-april-2026]] — RU-turbulence вокруг Telegram/MAX/VPN (выжимка из 6 постов)
- [[evolving/competitor-positioning/max-messenger]] — обновлён с top-downloads сигналом и telega.fm бот-мостом
- [[evolving/content-trends/ai-solopreneur-narrative-hooks]] — обновлён с «WB-курсы → ИИ-коучи» cross-signal
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — контекстно связана через 15256
