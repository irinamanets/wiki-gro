---
id: mkt:sources/2026-05-23-tg-recruiter-live-may-19-22-2026
title: "Telegram @recruiter_live — дамп 6 постов (ids 4476..4482, 19–22 мая 2026)"
type: source
layer: evolving
theme: industry-trends
tags: [career, content, awareness, labor-market, legal, nda, ecommerce]
confidence: medium
created: 2026-05-23
updated: 2026-05-23
original: raw/processed/articles/tg_recruiter_live_20260523-091000.md
bundle_primary: raw/processed/articles/tg_recruiter_live_20260523-091000.md
bundle_children:
  - raw/processed/media/tg_recruiter_live_4477.jpg
  - raw/processed/media/tg_recruiter_live_4478.jpg
  - raw/processed/media/tg_recruiter_live_4481.jpg
namespace: mkt
---

# Telegram @recruiter_live — дамп 19–22 мая 2026

## Метаданные

- **Тип:** Telegram-канал (авторский, тренер по рекрутменту), дамп 6 постов + 3 медиа-вложения
- **Канал:** `t.me/recruiter_live`, автор @tihragency Татьяна (агентство TIHR), практикующий карьерный консультант/рекрутер
- **Период:** 2026-05-19 14:01 → 2026-05-22 20:47 UTC (messages 4476..4482). **Пятый по счёту дамп** этого канала после [[sources/2026-04-14-tg-recruiter-live-career-digest]], [[sources/2026-05-05-tg-recruiter-live-apr-may-2026]], [[sources/2026-05-14-tg-recruiter-live-may-2026]] и [[sources/2026-05-19-tg-recruiter-live-may-18-19-2026]]. Перекрытий по ids нет (предыдущий заканчивался 4475).
- **Автор / источник:** Татьяна, @tihragency — практикующий карьерный консультант. Посты 4476, 4482 — пересылки/обзоры стороннего контента (Ведомости, LinkedIn-посты Aliya Janabilova и Kirill Pudrikov); 4477–4478 — личные репосты AI-инфографики с рыночными долями (off-topic для маркетинга); 4479 — личное наблюдение автора + LinkedIn-пересылка; 4481 — `#fun` мем.
- **Экспертность автора:** inferred (`confidence: medium`) — практикующий рекрутер с коммерческой практикой; для пересылаемых сторонних постов confidence наследуется от первоисточника. NDA-разбор (4482) — это пересылка авторского LinkedIn-поста Kirill Pudrikov с детальной legal-аргументацией со ссылками на конкретные ФЗ/статьи; контент верифицируем по тексту закона, не зависит от персоны.
- **Sidecar note:** был — пользователь явно назначает канал «временным контекстом для трекинга новостей и трендов по тематике Карьера и рекрутмент». Используется для написания блог-постов и новостей сервиса; разрешено вычленять инсайты в другие категории при наличии.
- **Bundle membership:** 1 primary (.md) + 3 children (3 jpg, все lightweight media → свёрнуты в эту source-страницу, отдельных source-страниц не создавалось). `.bundle.json` отсутствовал — children резолвились через `_(attached: ...)_` маркеры, все 3 найдены в `media/`. `.description.md` сайдкаров не было, vision-описание делалось в момент ingest'а.
- **Triage verdict:** `relevant` (Haiku, 2026-05-23) — канал эксперта по рекрутменту, тренды рынка труда, интервьюирование, HR-практики как контекст для ЦА ГРО.
- **Sensitive flag:** нет. Мем 4481 содержит замазанные ники (редактура на стороне источника), PII не извлекается.

## Релевантность

Дамп — пятый re-dump того же канала за ~6 недель. Из 6 постов 3 несут новый релевантный сигнал, 2 — off-topic репосты AI-инфографики (audit-only OCR ниже), 1 — `#fun` мем (audit-only). Большая часть narrative-рамок канала (response rate, ATS-коллапс, сломанная коммуникация) уже зафиксирована — новые extracts ниже.

**Высокорелевантно (новое):**

- **Пост 4482 (#полезное #NDA) — границы коммерческой тайны и неисполнимость штрафных NDA в РФ.** Пересылка детального LinkedIn-поста Kirill Pudrikov. Содержательный legal-разбор со ссылками на ФЗ «О коммерческой тайне» №98-ФЗ, ТК РФ (ст. 192 закрытый перечень взысканий, ст. 238 — только прямой действительный ущерб) и судебную практику. Тезис: запрет в NDA указывать **название компании / должность / круг обязанностей** под штраф 5–10 млн ₽ — юридически уязвим, потому что (а) название компании публично (учредительные документы + госреестры), (б) ТК не предусматривает денежных штрафов для работников, (в) суды отказывают во взыскании несоразмерных штрафов без доказанного ущерба. → **новая страница** [[canon-strict/legal-claims/ru-nda-confidentiality-limits-2026]] + cross-ref в [[evolving/industry-trends/ru-job-seeker-experience-2026]].

- **Пост 4476 (репост Ведомости) — Wildberries запускает B2B-экспорт российских товаров в Китай.** Анонс на конференции Wildberries Ecomday 2026 в Ханчжоу. Китайские компании смогут оформлять B2B-заказы российских товаров оптом онлайн, получать закрывающие документы, пользоваться инфраструктурой WB для логистики и таможенного сопровождения. Первоисточник — [Ведомости](https://www.vedomosti.ru/business/news/2026/05/19/1198217-wildberries-kitai), дата 2026-05-19. → **новая страница** [[volatile-strict/industry-news/wb-china-b2b-export-2026-05]] + cross-ref в [[evolving/industry-trends/ru-marketplace-seller-squeeze-2026]] и [[evolving/industry-trends/ru-china-trade-q1-2026]].

- **Пост 4479 (#интервью) — подготовка к интервью «думать изнутри компании».** Личное наблюдение Татьяны (кандидат открыл файл с деталями вакансии прямо на интервью, файл подвис) + пересылка LinkedIn-поста Aliya Janabilova. Тезис: до встречи разобраться — чем занимается компания, какой продукт/услуга, кто клиенты, как зарабатывает; на интервью не уходить в классическую самопрезентацию (где работал/учился), а сразу связывать свой опыт с задачами компании («у вас фокус на X — у меня был похожий кейс…»). Сильный кандидат «перестаёт быть просто кандидатом» и становится человеком, который «думает изнутри». → новый Hook 35 в [[evolving/content-trends/career-audience-hooks-2026]] + десятый голос в [[evolving/industry-trends/ru-job-seeker-experience-2026]].

**Нерелевантно для слоёв (только audit-only, OCR ниже):**

- **Пост 4477 + медиа 4477.jpg — глобальные доли рынка кормов для животных (Pet Food).** AI-сгенерированная инфографика Pristine Market Insights с долями выручки 2024. Off-topic: не про ГРО, не про рекрутмент/HR/маркетинг. Автор сам помечает `#рыноктруда` и просит «поправить», но содержание — рынок pet food, к marketing-memory не относится.
- **Пост 4478 + медиа 4478.jpg — мировые игроки рынка гидроизоляционных мембран.** Аналогичная off-topic инфографика. Автор сомневается в точности AI-данных. К домену не относится.
- **Пост 4481 + медиа 4481.jpg — `#fun` мем** (Threads-скрин про «съесть деревянную дверь за 5 дней → отдал бы бобрам на аутсорс»). Юмор, к домену не относится.

## Распознанный текст (OCR медиа-вложений, audit-only)

### Медиа 4477.jpg — «Pet Food» (Pristine Market Insights, Global Pet Food Market Revenue Share % 2024)

Off-topic для маркетинга ГРО; сохраняется только как audit обработанного вложения.

- **Key players:** Nestlé 23,63%; MARS 6,26%; fressnapf 4,96%; heristo 3,60%; General Mills 3,49%; HARRISON 3,39%; Felderzeugnisse 2,82%; Herrmann's Manufaktur 2,51%; YARRAH 2,17%; the honest kitchen 2,15%.
- **Rising players:** almo nature 1,48%; Agrolimen 1,27%; PRIMAL 1,15%; WELLNESS 1,01%; Vafo 0,88%; PetCo 0,85%; BIOPUR 0,79%; PETGUARD 0,75%; GrandFood 0,68%; rpf (Real Pet Food) 0,61%.
- Подпись: «Market Share Analysis of 50+ Companies is Available in Full Report. © Pristine Market Insights 2026.»
- Caption автора: «Лидеры рынка кормов для животных. В России точно есть Марс и Нестле. Сам сегмент в России растёт несколько лет подряд.» (заметим: инфографика глобальная, не РФ; российских игроков на ней нет).

### Медиа 4478.jpg — «Global Market Players in Waterproofing Membranes Market»

Off-topic; audit-only.

1. SIKA AG (Switzerland); 2. Tremco Incorporated (US); 3. GCP Applied Technologies (US); 4. CARLISLE Companies (US); 5. SOPREMA Group (France); 6. Johns Manville (US); 7. BASF (Germany); 8. RENOLIT (Germany); 9. FOSROC (UK); 10. MAPEI (Italy).
- Caption автора: упоминает Sika, BASF, RENOLIT, MAPEI; сомневается в присутствии немцев в РФ.

### Медиа 4481.jpg — `#fun` мем (Threads)

Off-topic; audit-only. Скрин Threads-треда: «Представьте, что у вас собеседование на новую работу. Вам задают вопрос: "Если бы у вас было пять дней, чтобы съесть обычную деревянную дверь, как бы вы это сделали?"» → ответ «Отдал бы бобрам на аутсорс» (1,6 тыс. ❤). Ники замазаны на стороне источника.

## Связанные страницы

- [[canon-strict/legal-claims/ru-nda-confidentiality-limits-2026]] — новая страница (NDA, пост 4482)
- [[volatile-strict/industry-news/wb-china-b2b-export-2026-05]] — новая страница (WB→Китай, пост 4476)
- [[evolving/content-trends/career-audience-hooks-2026]] — Hook 35 (подготовка к интервью, пост 4479)
- [[evolving/industry-trends/ru-job-seeker-experience-2026]] — десятый голос (пост 4479)
- [[evolving/industry-trends/ru-marketplace-seller-squeeze-2026]] — cross-ref WB B2B-экспорт
- [[sources/2026-05-19-tg-recruiter-live-may-18-19-2026]] — предыдущий (четвёртый) дамп канала
- [[canon/target-audience/gro-segments]] — карьерная и предпринимательская аудитория канала
