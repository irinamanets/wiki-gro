---
id: mkt:evolving/competitor-positioning/zakryvatel-sdelok-ai-agent
title: "«Закрыватель сделок» — productized AI-агент по методологии Шевелева"
type: page
subtype: competitor
layer: evolving
theme: competitor-positioning
tags: [ai, sales, agent, smb, productized-methodology, russia, competitor]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-14
sources: [sources/2026-05-05-tg-olegcloser-mar-may-2026.md, sources/2026-05-14-tg-olegcloser-may-7-13-2026.md]
namespace: mkt
---

# «Закрыватель сделок» — productized AI-агент по методологии Шевелева

Narrow AI-agent в нише sales-closing, разработанный **Олегом Шевелевым** (см. [[sources/2026-05-05-tg-olegcloser-mar-may-2026]]) и обученный его собственной методологии — **формуле 100% закрытия сделки** (см. [[canon/marketing-frameworks/sales-100-formula-shevelev]]). Запущен в апреле 2026 как часть курса «ПРОКАЧКА продаж с ИИ»; **отдельно НЕ продаётся** (явное заявление автора в посте 2256).

`confidence: medium` — единственный источник, нет независимой верификации, но автор демонстрирует работу агента публично в реалити «Рекордный апрель».

## Позиционирование

В пространстве sales-AI агентов «Закрыватель сделок» занимает **уникальный угол**:

| Сегмент рынка | Примеры | Что делает | Чем отличается «Закрыватель» |
|---|---|---|---|
| Generic sales-AI (CRM-coupled) | Salesforce Einstein, HubSpot AI | Score лидов, suggested actions на основе аггрегированной data | Заточен под одну методологию автора, не под data-driven scoring |
| Воронкочные AI-помощники | Just AI Agent Platform, generic GPT-coach | Открытый агент с подмешанной кастомной инструкцией | Closed methodology + verified expert behind it |
| Industry-vertical sales AI (USA) | Gong.io, Chorus | Анализ записей звонков для coaching менеджеров | Targeted на closing зависших сделок, не на coaching |
| **«Закрыватель сделок»** | — | **Применение конкретного экспертного фреймворка к индивидуальной зависшей сделке** | Productized expert methodology, bundled в обучающий курс |

**Главный differentiator** — это не «AI с фичами», а **methodology-as-a-service**: продукт продаёт **методологию автора**, а агент — это interface к ней.

## Алгоритм работы (по описанию автора)

Из поста 2256 (2026-04-21):

1. Пользователь даёт **описание сделки** (контекст: что продаёт, с кем общается, на каком этапе)
2. Пользователь прикрепляет **переписку и/или транскрипт звонка** с клиентом
3. Агент проверяет, на какой стадии сделка относительно **формулы 100% закрытия** (ФВ × ОП × Д × ЛПР × ЗС — **canonical расшифровки**: Финансовая Возможность × Осознанная Потребность × Доверие × Лицо Принимающее Решение × Здесь и Сейчас, см. [[canon/marketing-frameworks/sales-100-formula-shevelev]]; по карусели Шевелев × Т-Бизнес секреты 2026-05-07, [[sources/2026-05-14-tg-olegcloser-may-7-13-2026]] карточки 2284-2293)
4. **Critical step:** для каждого из 5 критериев агент **находит цитаты в переписке** как обоснование оценки
5. Если цитата не находится — критерий = 0
6. Агент выдаёт **готовую цепочку касаний** для прокачки слабых критериев:
   - Текст сообщения для отправки клиенту
   - Сценарий звонка
   - Текст голосового сообщения
   - Сценарий video-кружка

**Ключевая фраза** из поста 2256: «Агент сам проверяет точность оценки» — то есть он работает **против wishful thinking продавца**, а не вместе с ним.

## Бизнес-модель и distribution

- **Pricing model:** **bundled-only** — отдельной цены нет
- **Условия доступа:** «Решил дать доступ первым 50, кто зайдёт в ближайшую ПРОКАЧКУ» (пост 2256)
- **Anchoring продажи:** AI-агент работает как **bonus-trigger** для покупки основного курса, а не как самостоятельный SaaS
- **Pre-launch механика:** доступ к агенту открывается **до старта основного потока**, чтобы участники начали получать результат сразу — это ускоряет CTA «купить курс» до того, как человек дойдёт до основной программы
- **Demo-evidence:** показано в реалити «Рекордный апрель» — 5 участникам дан доступ к агенту, для проработки сотен зависших сделок (пост 2255). Это work как proof-by-demonstration см. [[canon/marketing-frameworks/business-reality-show-format]]

## Сильные стороны (для конкурентного анализа)

1. **Verified expert behind it.** Шевелев — кандидат наук, автор бестселлера на 5 retail-площадках. Это сильнее, чем «универсальный sales-bot».
2. **Тренировка на собственных кейсах.** Автор «много лет внедряет это у клиентов от Сбера до малого бизнеса» (пост 2256) — большой proprietary dataset для fine-tuning.
3. **Vertical narrowness.** Агент не пытается решить «всё про продажи» — только **closing зависших сделок**. Узкий scope = высокое качество выхода.
4. **Cite-evidence guard rail.** Критерии оцениваются только при наличии цитат. Это снижает hallucination'ы и заставляет пользователя признавать слабость своей сделки.
5. **Universal applicability claim.** «На реалити участники от медоборудования до обработки копыт — формула у всех одна» (пост 2256) — широкая декларируемая применимость в B2B.

## Слабые стороны / риски

1. **Ограничен одной методологией.** Если методология Шевелева не подходит конкретному бизнесу (например, transactional SaaS-продажи, где сделка закрывается через self-checkout), агент бесполезен.
2. **Bundled-only distribution = high entry cost.** Чтобы получить агента, нужно купить курс. Для предпринимателя «попробовать» — не вариант.
3. **Vendor lock-in на Шевелева.** Нет открытого API, нет кастомизации под другие методологии. Если автор уйдёт в другой проект, агент устареет вместе с курсом.
4. **No public benchmark.** Нет независимых отчётов о точности или conversion-uplift'е. Все evidence — anecdotal от участников курса.
5. **Тренировочные данные — закрытые.** Если данные тренировки агента — это переписки клиентов автора, **возможны вопросы по конфиденциальности** (хотя сейчас публично об этом не говорится).

## Применимость в маркетинге GRO

GRO **не конкурирует прямо** с «Закрывателем сделок» (разные ниши: closing B2B-сделок vs personal productivity), но **методологический pattern переносим**:

1. **Productized methodology pattern.** GRO может упаковать собственную методологию (например, «методика 4 шагов тренировки») в narrow AI-agent'а внутри приложения — это паттерн дифференциации от generic productivity GPT-обёрток.

2. **Cite-evidence guard rail.** Аналог в GRO: AI-агент в приложении должен искать **конкретные паттерны в данных пользователя** (история тренировок, время на телефон, окошки энергии), а не давать абстрактные советы. «Я вижу, что ты три раза подряд начинал тренировку в 8 утра и сдавался к 8:15 — давай попробуем 7:45».

3. **Bundled-only vs separate distribution.** Шевелев показывает, что **bundled** (агент включён в основной продукт) работает как retention trigger. Для GRO: если делать AI-coach как отдельный paid-tier — высокий entry cost снижает adoption. Лучше встроить в core subscription.

4. **Reality show as demo-vehicle.** Шевелев продемонстрировал агент **в реалити шоу**, а не в маркетинг-материалах. Параллель для GRO — см. [[canon/marketing-frameworks/business-reality-show-format]] для облегчённой адаптации.

## Сегмент конкурентного давления

В русском sales-AI пространстве «Закрыватель сделок» соседствует с:

- **Just AI Agent Platform Cloud** — generic platform для построения собственных агентов (см. [[evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026]]). Шевелев, скорее всего, использует её как backend (или OpenAI Assistants API).
- **Generic ChatGPT/Claude** — конкуренты «снизу» (бесплатные альтернативы для самостоятельной настройки)
- **Sales-vendor specific AI** (Bitrix24 AI, AmoCRM AI) — конкуренты «сверху» (заточены на CRM users, но не на методологию закрытия)

`Закрыватель сделок` занимает специфическую нишу: **methodology-vertical AI** — узкий, дорогой через bundle, с anchoring на личность эксперта.

## Связанные страницы

- [[sources/2026-05-05-tg-olegcloser-mar-may-2026]] — источник-якорь
- [[canon/marketing-frameworks/sales-100-formula-shevelev]] — методология, на которой обучен агент
- [[canon/marketing-frameworks/business-reality-show-format]] — demo-vehicle для агента
- [[canon/target-audience/ru-smb-founder-owner-seller]] — целевая аудитория агента
- [[evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026]] — backend-провайдеры (вероятный технический base)
- [[evolving/industry-trends/ai-agent-economy-2026]] — макро-контекст AI-агентов
- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] — pricing-аналитика для AI-агентов
- [[canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis]] — параллельный playbook для продажи AI-агентов в B2B

## Backlinks

_9 pages link to this one._

- [[canon/marketing-frameworks/business-reality-show-format]]
- [[canon/marketing-frameworks/objection-after-holidays-vrkr]]
- [[canon/marketing-frameworks/sales-100-formula-shevelev]]
- [[canon/target-audience/ru-smb-founder-owner-seller]]
- [[evolving/content-trends/mystery-shopper-content-format]]
- [[evolving/content-trends/sales-ai-narrative-hooks-2026]]
- [[evolving/industry-trends/ru-smb-sales-q1-2026]]
- [[index]]
- [[sources/2026-05-05-tg-olegcloser-mar-may-2026]]
