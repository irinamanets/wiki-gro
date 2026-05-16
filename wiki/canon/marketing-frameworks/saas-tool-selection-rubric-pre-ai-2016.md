---
id: mkt:canon/marketing-frameworks/saas-tool-selection-rubric-pre-ai-2016
title: "Pre-AI SaaS-tool selection rubric (2016) — 6-критериев baseline для contrast с AI-эры rubric'ой"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [marketing-frameworks, smb, ru, saas, pre-ai-era, historical-baseline, tool-selection, productivity, rubric]
confidence: medium
stale: false
created: 2026-05-16
updated: 2026-05-16
sources: [sources/2026-05-16-zhazhda-task-manager-business-evergreen-2016.md]
namespace: mkt
---

# Pre-AI SaaS-tool selection rubric (2016)

**Что это:** канонизированная 6-критериев rubric для выбора SMB-SaaS-tool, сформулированная редакцией Жажды в листикле «Выбираем планировщик задач для предпринимателя» (~2016, см. [[sources/2026-05-16-zhazhda-task-manager-business-evergreen-2016]]). Сохраняется как **canon** (стабильна) — это исторический артефакт **pre-AI эпохи**, который не «устареет» в смысле supersession (он уже устарел тематически, но **фиксирует frame 2016 года** как контрастный baseline для AI-эры rubric'и 2026).

`confidence: medium` — rubric сформулирована одним источником, но **5 из 6 критериев совпадают** с типичными SMB-SaaS-selection-criteria 2014-2018 эпохи (по аналогам в [[evolving/content-trends/zhazhda-biz-evergreen-listicle-genre]] и параллельным жанрам hr-portal, vc.ru ranking-статей), что повышает доверие к rubric'е как репрезентативной.

## 6 критериев pre-AI rubric

Прямые формулировки из листикла Жажды (intro секция «Вот критерии, которым он должен соответствовать обязательно»):

### 1. Кроссплатформенность

> «Работает на iOS, Android, macOS, Windows и в браузерах. Утром занес задачи на ноутбуке под "Виндой", днем открыл приложение с Айфона – все работает.»

В 2016 это **главный differentiator** — категория ещё фрагментирована по платформам (Things только macOS, Wunderlist везде, You Doo только Windows). В 2026 это **дефолт** — никто не покупает single-platform productivity-tool.

**К 2026 этот критерий мутировал в:**
- Mobile-first design (web — secondary)
- Telegram / WhatsApp / Slack как «дополнительная платформа» (messenger-bot интерфейс)
- iPad / tablet-optimized version (не просто responsive)

### 2. Расширенный функционал (CRUD-задач)

> «Созданием простого списка задач никого не удивишь. Сервис должен уметь расставлять приоритеты, делать заметки, прикреплять файлы и сортировать задачи по группам.»

Базовый CRUD-функционал «приоритеты + заметки + attachments + сортировка» — в 2026 это **commodity**, минимум для входа в категорию. **Не differentiator.**

**К 2026 этот критерий мутировал в:**
- AI-prompted task creation (LLM понимает «забронируй эту встречу» и создаёт задачу + календарь-event)
- Smart-prioritization (Motion, Reclaim — AI решает что делать в каком порядке)
- Auto-summary, auto-categorization

### 3. Облако + офлайн

> «Работает онлайн и офлайн, а все данные хранятся в "облаке".»

В 2016 это **острый вопрос** — облачная архитектура только утвердилась как стандарт, и офлайн-mode был сложной inженерной задачей. В 2026 — **дефолт**.

**К 2026 этот критерий мутировал в:**
- Real-time sync между устройствами (мгновенная sync, не «через 5 минут»)
- E2E-шифрование (Signal-style end-to-end)
- Cloud-agnostic / self-host опции для privacy-conscious пользователей

### 4. Бесплатная пробная версия

> «За хорошие программы нужно платить – факт. Но бесплатная пробная версия должна быть обязательно. Это позволить оценить продукт и принять окончательное решение.»

В 2016 **обязательный** компонент SaaS-pricing-модели. В 2026 — **частично деградировал** (некоторые AI-tools предлагают per-credit pay-as-you-go без trial, потому что compute-stoимость не позволяет щедрых trial-periods; например, ранний Cursor / Cline).

**К 2026 этот критерий мутировал в:**
- Freemium с щедрым free tier (Notion, Linear, ClickUp)
- Pay-as-you-go credits (Cursor, ChatGPT API) — не trial, а **усыпление barrier через micro-payments**
- 14-day money-back guarantee (для AI-tools)

### 5. Русификация

> «Никому не хочется разбираться в интерфейсе на английском. Поэтому наличие русского языка – приоритетный критерий выбора.»

В 2016 RU-локализация была **must-have для SMB**. В 2026 этот критерий **частично деградировал**:

- LLM-эра сделала **on-the-fly translation** доступной (любой английский UI можно перевести через расширение браузера или AI-tool)
- Молодое SMB-поколение (founders 25-35 лет) **comfortable с английским** — особенно в IT/SaaS-нише
- **Однако:** для mainstream SMB (бьюти, общепит, авто-сервис) RU-локализация **всё ещё обязательна** — это сегмент-зависимое требование, не universal

**К 2026 этот критерий мутировал в:**
- RU-native AI/LLM (YandexGPT, GigaChat) для SMB не-IT-сегмента
- Voice-interface на русском (важно для не-power-users)
- Cyrillic-friendly typography / search

### 6. Простой / интуитивный UI

> «Простой и интуитивный интерфейс, с которым можно подружиться за несколько минут.»

В 2016 это **проблема** — категория была заполнена over-engineered tools (Microsoft Project, корпоративные TaskFlow-системы), и SMB нуждался в «consumer-grade simple» tools. В 2026 **остаётся актуальным**, но **значимо мутировал**.

**К 2026 этот критерий мутировал в:**
- Conversational UI (chat-based, не form-based) — Motion, Notion AI, ChatGPT-Tasks
- Voice-first interface для не-text-friendly юзеров
- AI-onboarding (LLM объясняет фичи пользователю на естественном языке, не tutorial-overlay'ami)

## Что отсутствует в pre-AI rubric (появилось в 2026)

Критерии, **отсутствующие в 2016 rubric** Жажды, но **обязательные в 2026 SaaS-selection-rubric**:

### A. AI-функции

- Smart-prioritization (AI решает что важнее)
- LLM-prompted task creation
- Voice-to-task с LLM (не просто Siri-style speech-to-text)
- AI-summary, AI-categorization
- Agentic-execution (AI сам выполняет часть задач: бронирует, отправляет email, и т.д.)

В 2016 ни один из этих критериев **даже не был на радаре** — LLM (transformer-architecture) появилась в 2017, ChatGPT — в 2022, mainstream AI productivity-tools — 2024-2025.

### B. Messenger-интеграция

- Telegram-bot (RU-критично)
- Slack-bot (для team-collaboration)
- WhatsApp / Viber-bot (для не-IT SMB)
- Email-to-task (forward email → создаётся задача с контекстом)

В 2016 messenger-категория была **silo'ed**: Telegram только-только запустился (2013), мессенджеры **не были** integration-target'ами для productivity-tools. К 2026 это **дефолтная интеграционная точка**.

### C. API / automation

- Zapier / Make.com / n8n
- Public API
- Webhooks

В 2016 эти инструменты существовали (Zapier с 2011), но **не были mainstream-требованием SMB** — только power-users. К 2026 **expected feature**.

### D. Privacy / E2E

- E2E-шифрование
- GDPR / 152-ФЗ compliance
- On-premise / self-host вариант
- Data residency (где физически хранятся данные)

В 2016 SMB **не задумывался** о privacy SaaS-tools (только enterprise). К 2026 — **post-Snowden / post-2022 privacy-awareness** среди RU-SMB значимо выросла.

### E. Mobile-first

В 2016 **«работает на мобильном» был критерий**. В 2026 **«mobile-first дизайн, а web — secondary»** — стандарт. Любой productivity-tool, у которого desktop primary, mobile secondary — считается legacy.

## Применение rubric'и: как читать GRO content про productivity-tools

GRO как habit-tracker **не конкурирует напрямую** с task-managers, но **смежная категория**. При написании contenta про productivity (статьи, посты), GRO может:

### 1. Использовать pre-AI rubric как baseline для contrast

В content типа «5 productivity-tools 2026 для предпринимателя» GRO может **явно сравнить** 6-критериев rubric Жажды (2016) с 11-критериев AI-эры rubric (5 mутированных + 6 новых). Это **показывает экспертизу** в эволюции категории и **позиционирует AI-эру как новую эру**, не incremental update.

### 2. Использовать как mental model для собственного продукта

При product-marketing GRO можно явно показать, что GRO соответствует **всем 11 критериям 2026**:

- Кроссплатформенность → iOS, Android, web
- Расширенный функционал → AI smart-prioritization (если есть)
- Облако + офлайн → есть
- Бесплатная пробная версия → 14-дневный free trial
- Русификация → нативная RU
- Простой UI → habit-tracker focus, не «for everything»
- AI-функции → smart suggestions, voice-input (если есть)
- Messenger-интеграция → Telegram-bot (если есть)
- API / automation → public API (если есть)
- Privacy → 152-ФЗ compliance, RU data residency
- Mobile-first → primary platform

### 3. Использовать как textbook reference в editorial / SEO-content

Pre-AI rubric Жажды — **готовый scaffold для SEO-арбитража**: GRO может написать «6 критериев выбора productivity-tool в 2016 и почему сейчас их уже 11» — это **evergreen content** с double-edged value (SEO traffic + позиционирование экспертизы).

## Связанные страницы

- [[sources/2026-05-16-zhazhda-task-manager-business-evergreen-2016]] — якорь-источник (pre-AI rubric)
- [[evolving/content-trends/ru-task-manager-listicle-baseline-2016]] — landscape-страница 2016, контекст rubric'и
- [[evolving/content-trends/zhazhda-biz-evergreen-listicle-genre]] — жанр, в котором rubric была сформулирована
- [[canon/target-audience/ru-smb-founder-owner-seller]] — целевая аудитория rubric'и (SMB-founder 2016 → 2026)
- [[evolving/industry-trends/ai-productivity-j-curve-2026]] — современная industry-trend, отвечающая на 2016-rubric AI-эра ответом
- [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]] — TYPICAL 3-сдвига AI-productivity, объясняющие почему 2016-rubric устарела
