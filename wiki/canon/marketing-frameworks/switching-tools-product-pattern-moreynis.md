---
id: mkt:canon/marketing-frameworks/switching-tools-product-pattern-moreynis
title: Switching tools — продуктовый паттерн B2B (Морейнис)
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [b2b, product-pattern, growth-hacking, decision, competition]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-temno-moreynis-may-5-14-2026.md]
namespace: mkt
---

# Switching tools — продуктовый паттерн B2B

Продуктовый паттерн обратной парадигмы, сформулированный **Аркадием Морейнисом** ([@temno](https://t.me/temno), [пост 7827 от 2026-05-11](https://t.me/temno/7827)). Размещается в `canon/marketing-frameworks` как стабильный B2B-паттерн, не привязанный к конкретной волне.

## Центральная формулировка

> Если на рынке творится бардак... не нужно ему противостоять, лучше его возглавить. Не нужно мешать конкурентам — нужно начать им помогать. — Морейнис, [[sources/2026-05-14-tg-temno-moreynis-may-5-14-2026|пост 7827, 2026-05-11]]

Морейнис формулирует **«обратную парадигму»** для B2B-стартапов: вместо строить retention-инструменты для удержания пользователей от перехода на конкурентов (стандартное правило), строить **switching tools** — инструменты, помогающие пользователям мигрировать с одного сервиса на другой. И продавать эти инструменты **конкурентам**, а не пользователям.

## Mechanism

Структурная логика паттерна:

1. **В насыщенном рынке** (где аналогов много, конкуренция высокая) переключение между сервисами — больной болт. Пользователь хочет перейти, но не может (data migration, learning curve, история).
2. **Стандартный паттерн:** каждый сервис добавляет «лояльность» (data lock-in, бонусы за стаж, integrations) → застой рынка.
3. **Switching tool** обнуляет migration friction: автоматический экспорт из старого, автоматический импорт в новый, перенос истории.
4. **Бизнес-модель:** не платит **пользователь** (зачем платить за переход), платит **новый сервис** (тот, который получает пользователя). Это **CAC reduction tool** для нового сервиса.

## Proof-points

Морейнис ссылается на существующий стартап (без названия) — switching tool, который уже хорошо взлетает. `[conf:low, src:2026-05-11]`

Канонические исторические примеры:

- **Email portability tools** — позволяют перенести email-историю с Gmail в ProtonMail (или наоборот). Продаются end-user'у, но реально работают как CAC reduction для receiving service.
- **CRM migration tools** (Salesforce ↔ HubSpot, etc.) — стандартный enterprise-pattern. Продаются partner'ом receiving CRM, а не self-service.
- **Music playlist migration** (Spotify ↔ Apple Music ↔ YouTube Music) — стороннее приложение (типа FreeYourMusic / SongShift) фактически продаётся receiving-сервису как часть его growth budget.
- **WordPress migration plugins** (типа All-in-One WP Migration) — продаются hosting providers, которые хотят забрать сайты у конкурентов.

## Operational-применение

**Признаки рынка, где switching tool сработает:**

| Признак | Объяснение |
|---|---|
| Аналогов много, dominance низкая | Если 80% рынка у одного игрока — он не платит за миграцию (зачем), а у конкурентов нет бюджета. |
| Migration friction высокая (data, history, integrations) | Если миграция и так easy — switching tool не нужен. |
| Switching cost ≤ N-month подписки на новый сервис | Если switching tool дороже стоимости первых N месяцев в новом — clients не используют. |
| Новый сервис достаточно зрелый (deserves migration) | Сlients не мигрируют ради ради переключения; должна быть value в новом. |

**Признаки рынка, где не сработает:**

- Монопольный или дуопольный рынок (нет конкурентов с deep pockets).
- Network effect — пользователь не уходит без сети друзей (соцсети).
- Высокий sunk cost в нематериальном (репутация, рейтинг профиля).
- Бесплатные продукты без коммерческой модели (нет budget).

## Бизнес-модель switching tool

Три типичных схемы:

1. **Per-migration fee** — receiving сервис платит фиксированную сумму ($50-500) за каждого мигранта.
2. **Revenue share** — receiving сервис делится % от revenue первых N месяцев мигранта.
3. **Tiered subscription** — receiving сервис покупает подписку на N миграций / месяц.

Модель 1 — наиболее популярная, но даёт неровный cash flow для switching tool startup. Модель 2 — даёт recurring revenue, но требует tight integration с receiving billing. Модель 3 — даёт predictable revenue, но требует enterprise-sales-цикл.

## Связь с другими паттернами

### Vs [[canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis|правило 1]] (не софт, а результат)

Switching tool — extreme-форма правила 1: продаётся **не код**, а **операционный результат миграции** (вот N конкретных пользователей с их данными мигрировали к вам). Receiving сервис платит за **outcome**, не за toolset.

### Vs [[canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis|правило 2]] (кого похвалят за покупку)

В receiving сервисе за покупку switching tool хвалят **growth-команду / маркетинг**. Это понятный buyer: CMO / VP Growth. Они меряются по CAC, и switching tool — это **самый дешёвый CAC** на рынке (конкурент сам платит за их customer transition).

### Vs [[evolving/industry-trends/ai-value-migration-2026|AI value migration]]

ИИ радикально снижает стоимость switching tools — раньше каждый switching tool требовал custom integration с API source и destination сервисов, теперь LLM-агент может **на лету парсить любой data export** и **на лету генерировать import script**. → Switching tools становятся **universal commodity** + переходят в self-service ИИ-инструменты.

## Anti-patterns

1. **Продавать switching tool пользователям.** Пользователь не хочет платить за переход, он хочет иметь его бесплатно. Прежде чем switching tool станет коммерчески viable — он должен быть free для end-user'а. Source revenue: receiving сервис.
2. **Делать switching tool как «фичу» внутри своего продукта.** Если рекламируешь «легко мигрировать из X в нас», но интегрировано внутри своего сервиса — у тебя feature, не switching tool. Switching tool как standalone product продаётся **любому** receiving сервису, не только тебе.
3. **Игнорировать legal/data ownership.** В EU и РФ data portability — это правовое право пользователя (GDPR Article 20, ФЗ-152). Не нужно «изобретать» switching tool как «грязный hack» — это правовая infrastructure, на которой можно строить продукт.
4. **Конкуренция со source сервисом.** Source-сервис (с которого мигрируют) будет всячески ломать switching tool. Лучшая стратегия — building tool через **публичные API source сервиса** (которые он не может закрыть) или через **legal data portability** (которую он не может отказать).

## Operational-применение для GRO

GRO работает в нише personal development / habit tracking, где есть существующие игроки (Headway, Headspace, Atomic Habits app, Notion habit-templates):

**Гипотетический GRO switching tool:**
- Парсит экспорт пользователя из Headway / Atomic Habits / Notion / Habitica.
- Переносит привычки, треки, цели в GRO с сохранением streaks.
- Продаётся **GRO** (себе) как CAC reduction tool — переключение пользователя с конкурента в GRO с минимальным friction.

**Альтернатива:** GRO не делает switching tool сам, но **поддерживает import** от конкурентов как обязательную фичу (low effort engineering, big growth lever).

**Hook для блога:** «Конкуренты усложняют миграцию между сервисами — а должны делать наоборот. Почему switching tools — это будущее B2C-маркетинга» — readable статья.

## Cross-links

- [[canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis]] — общий B2B-playbook (правила 1, 2)
- [[canon/marketing-frameworks/latent-demand-ai-startup-search-moreynis]] — switching tool как обнуление barrier «data migration»
- [[evolving/industry-trends/ai-value-migration-2026]] — ИИ радикально снижает стоимость switching tools
- [[canon/marketing-frameworks/breakage-business-model-fitness]] — диагностика рынков, на которых switching tools sup-востребованы
- [[evolving/competitor-positioning/avito-smb-analytical-content-play]] — пример индустрии с high-migration friction
- [[canon/positioning/gro-value-proposition]] — GRO позиционирование с учётом migration paths
- [[sources/2026-05-14-tg-temno-moreynis-may-5-14-2026]] — источник
