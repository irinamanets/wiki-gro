---
id: mkt:evolving/competitor-positioning/neurofond-positioning-2026-05
title: Нейрофонд — positioning AI-агрегатора без VPN и с RU-картами (multi-model, founder-Egoshin, май 2026)
type: page
subtype: competitor
layer: evolving
theme: competitor-positioning
tags: [b2b, b2c, ai, content, social, paid-ads, awareness, consideration]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-egoshin-kedprof-may-5-12-2026.md, sources/2026-04-14-tg-egoshin-kedprof.md, sources/2026-05-05-tg-egoshin-kedprof-may-2026.md]
namespace: mkt
---

# Нейрофонд — positioning AI-агрегатора без VPN и с RU-картами

**Нейрофонд** — флагманский продукт «Кеды профессора» (founder Константин Егошин, также co-founder GRO). Это **sibling-product GRO от той же команды**: разные product-spaces (Нейрофонд = AI-агрегатор/utility, GRO = behavior-change через AI-тренажёры), но overlap в team, audience, distribution-tactics.

Страница расположена в `evolving/competitor-positioning`, потому что: (а) positioning лендинга и стек моделей дрейфуют с месячной скоростью (новые модели интегрируются, формулировки кейсов меняются); (б) это не наш конкурент в строгом смысле (разные problem-spaces), но это **adjacent vendor в той же экосистеме**, чьё позиционирование нужно знать для (i) cross-channel промо через Егошина, (ii) anti-positioning против AI-агрегатор аудитории, которую могут перепутать с GRO.

## Базовое позиционирование (2026-05-08)

Из [[sources/2026-05-14-tg-egoshin-kedprof-may-5-12-2026|TG-поста 569]] и скриншота лендинга `promo.neurofond.ru`:

| Элемент | Значение |
|---|---|
| **Headline** | «Нейрофонд — единый доступ к лучшим нейросетям мира» |
| **Sub-headline** | «Легко. Доступно. Быстро» |
| **CTA** | «Начать бесплатно (карта не требуется)» |
| **Trust-якоря (две иконки рядом с CTA)** | «Без VPN», «Оплата российскими картами» |
| **Multi-model стек (видимый на 2026-05-12)** | Claude Opus / Claude Sonnet, GPT-4o, **Gemini 3.1 Pro** (плюс другие модели; точный список не считан) `[conf:high, src:2026-05-12]` |
| **Доменная архитектура** | `promo.neurofond.ru` — маркетинговый лендинг; `neurofond.ru` — продуктовое приложение; `neurofond.ru/shared/*` — публичные кейсы клиентов |

## Промокод-механика

**Egoshin использует личный публичный промокод EGOSHIN800** в постах канала, где упомянут продукт `[conf:high, src:2026-05-08]`. Это **founder-as-affiliate pattern**: персональный код, а не event-specific (как KEDPROF / RIF90GUEST из апрельско-майских дампов — те привязаны к конкретным выступлениям и конференциям).

Цитата из поста 569:

> «Можете мой промокод активировать в настройках, чтобы попробовать продукт: `EGOSHIN800`»

Это паттерн, который встречается у других RU-founder'ов (Гребенюк, Высоцкий — см. [[evolving/content-trends/ai-translator-curator-channel-pattern-egoshin]] секция Brand-anchor лекций) и подтверждает, что **founder-personal-promocode** — стандарт в RU AI/EdTech-продуктах 2026.

**Что неизвестно (carve-out для будущих ingest'ов):**

- Размер скидки / триал-период по EGOSHIN800 — пост не раскрывает (требует посещения лендинга или активации).
- Структура revenue-sharing (если есть) между Егошиным и Нейрофондом.
- Действует ли EGOSHIN800 на годовую подписку и на upgrade-tier'ы.

## Стек моделей и multi-model positioning

Из скриншотов 569 и 570:

- **GPT-4o** — виден как одна из доступных моделей на UI-скриншоте лендинга (правая карточка превью, диалог с HR-вакансией) `[conf:high, src:2026-05-08]`
- **Claude Opus, Claude Sonnet** — упомянуты в тексте поста 569 («Opus или Sonnet вам нужны, приходите к нам в Нейрофонд, там всё работает») `[conf:high, src:2026-05-08]`
- **Gemini 3.1 Pro** — виден как активная модель в скриншоте поста 570 (мобильный UI `neurofond.ru`, dropdown селектор модели в шапке диалога) `[conf:high, src:2026-05-12]`

**Положение в taxonomy AI-агрегаторов 2026:**

- Нейрофонд — **multi-model aggregator класса «3+ вендора в одном UI»** (GPT + Claude + Gemini), а не «обёртка над одной моделью» (как, например, Bothub был раньше с GPT-only).
- Конкурентная позиция: **аналог Poe / OpenRouter в US-сцене, но RU-нативный с RU-payment-rails и без VPN-требования**.
- Vendor-risk управляется: блокировка Claude Anthropic'ом → пользователи Нейрофонда продолжают работать на других моделях. Это конкретный operational moat в условиях [[evolving/industry-trends/ru-digital-regulatory-squeeze-2026|RU regulatory squeeze]].

## Opportunistic positioning vs vendor-side blocks

Из поста 569 (2026-05-08):

> «С утра все новости о том, что Антропик блокирует учетки российских пользователей в Claude. Печально. Если вас заблокировали, а Opus или Sonnet вам нужны, приходите к нам в Нейрофонд, там всё работает: promo.neurofond.ru/»

Это **opportunistic positioning playbook**:

1. **Trigger** — публичная новость о vendor-блокировке (Anthropic banned RU accounts, см. [[volatile-strict/industry-news/anthropic-ru-block-egoshin-vendor-confirmation-2026-05]]).
2. **Move** — короткий пост в тот же день («с утра все новости...») с эмпатией («Печально») + явным CTA («приходите к нам, там всё работает»).
3. **Constraints** — нет морализаторства против Anthropic, нет атаки на конкурента, нет detailed-сравнения. Просто facts + solution.
4. **Mechanism** — promocode EGOSHIN800 как trial-incentive (снимает friction «попробовать»).

**Что это означает для GRO** (если volume Claude-блокировок продолжит расти):

- GRO ≠ AI-агрегатор, поэтому **Claude-блокировка напрямую не релевантна GRO-аудитории**.
- Но **vendor-trust-shift** общий тренд: RU-нативные продукты получают +reliability-points против западных вендоров. Это **косвенный tailwind** для всех RU-AI продуктов, включая GRO.
- Playbook «оперативно реагировать на vendor-новости» применим к GRO, если: (а) США-блокирует app-store для RU-приложений; (б) появится volatile-новость про AI-обучающие продукты, конкурентов GRO.

## Аудитория и overlap с GRO

| Атрибут | Нейрофонд | GRO |
|---|---|---|
| **Problem-space** | AI utility / агрегатор моделей для повседневных задач | Behavior change / личностный рост через AI-тренажёры |
| **Use-case** | «Напиши текст / суммаризируй / сгенерируй» | «Развей привычку / преодолей выгорание / поставь цель» |
| **Frequency-of-use** | Daily (workflow tool) | 3-5×/week (habit tool) |
| **Primary buyer** | Карьерист / предприниматель / маркетолог | Карьерист / предприниматель (overlap!) + lifestyle audience |
| **Pricing** | Freemium → paid tier (детали неизвестны, требуют ingest лендинга) | Freemium → paid subscription |
| **Distribution** | Personal-channel founder Егошин + paid ads + B2B sales | App stores + content marketing + Telegram channels of founders |
| **Brand-trust-якорь** | «Без VPN / RU-картами» | Лапшина-Соколов Okko-якорь + ИИ-тренажёры |

**Overlap-зона:** карьеристы и предприниматели в RU TG, использующие AI ежедневно. Эти люди — **потенциально и пользователи Нейрофонда, и пользователи GRO**. Каннибализация **низкая** (разные moments-of-use: Нейрофонд для work-tasks, GRO для personal-growth), но **cross-promo-возможность высокая**.

## Cross-promo-вектор Егошина

Поскольку **Егошин = co-founder GRO + founder Нейрофонд**, естественно возникает вопрос: как Егошин балансирует продвижение Нейрофонда (на его личном канале) и продвижение GRO (на канале Лапшиной @eklapshinaofficial + общий GRO-канал)?

Из текущих и предыдущих дампов:

- **На @egoshin_kedprof Нейрофонд продвигается активно** (промокод EGOSHIN800 в каждом релевантном посте, скриншоты UI как иллюстрация бытовых вопросов, прямые CTA «приходите к нам»).
- **GRO упоминается реже** — преимущественно в брендингах выступлений и в постах-визитках (2026-03-15 пост 532, см. [[sources/2026-04-14-tg-egoshin-kedprof|апрельский дамп]]).
- **Audience split:** канал Егошина больше resonate с work-productivity и AI-developer аудиторией (продакт-задачи, переводы AI-лидеров), а Лапшина — с lifestyle / personal-growth / founder-wife аудиторией.

**Гипотеза для CMO GRO:** Нейрофонд-промо на канале Егошина не конкурирует с GRO-промо, потому что **разные moments-of-attention** аудитории. Канал Егошина — это рабочий-режим, канал Лапшиной — это lifestyle-режим. Cross-promo между двумя продуктами **возможен в обе стороны**, но обычно делается через **shared-content** (Лапшина упоминает Нейрофонд как тулзу в bts-постах, Егошин упоминает GRO как brand при выступлениях), а не через прямые CTA.

## Anti-positioning для GRO

GRO **не позиционируется как AI-агрегатор** ни в каком контенте. Это важный invariant: если GRO-content начнёт хвастаться «у нас доступ к GPT/Claude/Gemini», аудитория будет читать GRO как **похожий-на-Нейрофонд продукт** (а это означает каннибализацию двух sibling-продуктов одной команды).

Правильное GRO-позиционирование (anti-Нейрофонд):

- **«AI-тренажёры для развития привычек»**, а не «доступ к AI-моделям»
- **«Behavior change через AI»**, а не «AI для productivity»
- **«4-шаговая тренировка»** (canon-структура продукта), а не «выбор модели»
- В контентах GRO **не упоминать модели по именам** (Claude, GPT, Gemini) — это позиционирует GRO как технический wrapper, а не как behavior-change-tool

## Что эта страница НЕ описывает

- **Юр-структуру Нейрофонда** (ООО, бенефициары, доли) — не входит в маркетинговый scope.
- **Финансовые метрики Нейрофонда** (MRR, install-count, retention) — не раскрыты в источниках, отсутствуют в публичном поле.
- **Точные тарифы Нейрофонда** — требуют отдельного ingest лендинга `promo.neurofond.ru` или активации EGOSHIN800.
- **Roadmap Нейрофонда по моделям** — что планируется интегрировать дальше (Claude 4.7? GPT-5? и т.д.) — не озвучено.

## Cross-links

- [[canon/product-knowledge/gro-team]] — Егошин как founder Нейрофонда и co-founder GRO; родительская team-страница
- [[evolving/industry-trends/ru-digital-regulatory-squeeze-2026]] — 15-й вектор vendor-side suspension, на который Нейрофонд оперативно реагирует
- [[volatile-strict/industry-news/anthropic-ru-block-egoshin-vendor-confirmation-2026-05]] — second-source vendor-confirmation Claude RU-блока
- [[evolving/content-trends/ai-translator-curator-channel-pattern-egoshin]] — channel-pattern, через который Нейрофонд продвигается
- [[canon/marketing-frameworks/egoshin-ai-adoption-ladder]] — лестница AI-адаптации, концептуальный контекст
- [[canon/positioning/gro-value-proposition]] — anti-positioning reference для GRO
- [[sources/2026-05-14-tg-egoshin-kedprof-may-5-12-2026]] — основной первоисточник
- [[sources/2026-04-14-tg-egoshin-kedprof]] — апрельский baseline
- [[sources/2026-05-05-tg-egoshin-kedprof-may-2026]] — майский refresh
