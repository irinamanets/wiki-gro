---
id: mkt:canon/marketing-frameworks/gtm-shared-understanding-anchor
title: "GTM shared-understanding anchor: зафиксировать понимание продукта письменно до запуска"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [marketing-frameworks, gtm, go-to-market, product-positioning, b2b, organizational-design, anti-pattern]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-pressfeed-prdoctor-marketing-pr-sales-conflict.md]
namespace: mkt
---

# GTM shared-understanding anchor

**Тезис.** Прежде чем запускать go-to-market работу — позиционирование, ключевые сообщения, контент-планы, каналы продвижения — нужно **письменно зафиксировать совместное понимание команды о том, что такое продукт и какую ценность он несёт клиенту**. Иначе «все согласовывают» на промежуточных этапах → а на финальной презентации директору выясняется, что фундаментальное допущение неверно → бюджет и месяцы работы уходят в песок.

Сформулирован совладельцем PR-агентства PR DOCTOR на основе реального case ([[sources/2026-05-19-pressfeed-prdoctor-marketing-pr-sales-conflict]]). `confidence: medium` — inferred expert single-source, но pattern совпадает с lean-startup доктриной «assumptions test first».

## Кейс PR DOCTOR (2 месяца GTM сгорели)

**Сценарий:**

1. Заказчик — IT-компания с новым решением
2. PR DOCTOR готовил GTM-стратегию **2 месяца**
3. Что было сделано: позиционирование, ключевые сообщения, контент-планы, каналы продвижения
4. **На каждом этапе** руководитель проекта и продакт-оунеры всё согласовывали, вносили предложения и двигались вместе с агентством
5. Несколько предварительных встреч и совещаний, согласованы презентации отдельных разделов и ключевые гипотезы
6. **На финальной презентации директору выяснилось:**
   - Продукт **вообще не предназначен для внешнего рынка**
   - Его название **чисто техническое, для внутреннего использования**
7. → Оперативно переключились на другое решение
8. → **2 месяца совместной работы и солидный кусок бюджета ушли в песок**

**Ключевой вывод автора:**

> «Если вы уверены, что все в команде одинаково понимают продукт и его ценность для клиента, лучше лишний раз перепроверьте и зафиксируйте это понимание в письменном виде.»

## Почему рушится «согласование по этапам»

Согласование промежуточных этапов **не ловит ошибки в фундаментальных допущениях**, потому что:

- Каждый этап обсуждает **тактику**, а не базовое предположение
- Product-owner-ы могут не иметь полной картины (директор не пришёл на промежуточные встречи)
- «Все согласовали» = политическое согласие, не verified understanding
- Письменная фиксация **с конкретными формулировками** ловит расхождения, которые проскальзывают через verbal-agreement

Это родственно principle [[canon/marketing-frameworks/definition-of-done-product-positioning|Definition-of-Done для позиционирования]] и lean «riskiest assumption test».

## Anchor-документ: что фиксируется до GTM-работы

**Минимальный shared-understanding документ:**

| Поле | Кто заполняет | Кто approve |
|---|---|---|
| Целевой рынок (внутренний / внешний / оба) | Product-owner | CEO / Founder |
| Целевой сегмент (B2B / B2C / hybrid; SMB / Mid / Enterprise) | Маркетинг + product | CEO / Founder |
| Название продукта (внутреннее vs внешнее) | Product + маркетинг | CEO + legal |
| Value proposition (1-предложение, для какой роли, какую проблему решает) | Маркетинг | CEO + product |
| Cycle sales (длина, кто покупатель, кто плательщик) | Sales + product | CEO |
| Pricing model (subscription / one-time / freemium / usage-based) | Product + finance | CEO |
| Conflict-with-other-products в портфеле (если есть) | Product | CEO |
| **Approval signature от CEO/Founder** | — | CEO |

**Принцип:** **минимум, без которого GTM-работа бессмысленна**. Не «полное ТЗ», а anchor, на который опирается вся последующая работа.

## SLA: когда нужна письменная фиксация

- ✅ Новый продукт (любого масштаба)
- ✅ Существенная смена позиционирования
- ✅ Выход на новый сегмент
- ✅ Pivot из B2C в B2B (или обратно)
- ✅ Запуск GTM работы агентством / новой командой
- ⚠️ Минор-релиз существующего продукта — можно ограничиться обновлением одного-двух полей
- ❌ Тактические campaigns в рамках уже зафиксированного позиционирования — не нужно

## Применение к GRO

GRO имеет **два продукта**: подписка на приложение (B2C, 2 490 ₽/мес) и Интенсив (B2B/cohort, high-ticket). Для каждого должен быть свой shared-understanding anchor:

- **Приложение:** B2C, retention-driven, paid-ads + контент, subscription, цена стабильна → anchor зафиксирован в [[canon/product-knowledge/gro-product-overview]] (если существует)
- **Интенсив:** B2B/групповой формат, sales-cycle 1-3 месяца, ROI-первое сообщение L&D → anchor зафиксирован в [[canon/product-knowledge/gro-intensive]]

При запуске любой новой GTM-кампании (например, выход в новый сегмент HR-tech или коллаборации с EdTech-партнёром) — **сначала обновить или подтвердить anchor**, потом начинать работу. Иначе PR DOCTOR-case повторится в нашем масштабе.

## Связь с другими фреймворками

### Upstream
- [[canon/marketing-frameworks/three-dept-conflict-prdoctor]] — общая рамка «зафиксировать роли и понимание письменно»; GTM-anchor — конкретный case
- [[canon/marketing-frameworks/definition-of-done-product-positioning]] — определение готовности позиционирования к запуску
- [[canon/marketing-frameworks/refused-customer-interview]] — параллельная доктрина «assumptions test first» через интервью с отказниками

### Downstream
- [[canon/marketing-frameworks/marketing-sales-alignment-framework]] — Lead Definition SLA становится осмысленным только после shared-understanding anchor
- [[canon/marketing-frameworks/b2b-pr-influence-shift-2026]] — смысловая архитектура PR (рычаг 1 оттуда) требует anchor как input
- [[canon/marketing-frameworks/event-coordination-checklist-prdoctor]] — единые pitch-скрипты на мероприятиях требуют anchor

### Adjacent — antidote-доктрины из существующей вики
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] — counter-balance: anchor не значит «всё идеально продумано до запуска»; это минимум фундаментальных допущений, а MVP-итерации проверяют остальное

## Anti-patterns

- ❌ **«Все согласовали на промежуточных встречах»** — verbal-agreement не ловит расхождения в фундаментальных допущениях
- ❌ **«Анкер — это полное ТЗ на 50 страниц»** — нет, минимум, без которого GTM бессмысленна. Перегружать — никто не прочитает
- ❌ **«CEO одобрит на финальной презентации»** — поздно. Anchor должен иметь CEO-signature **до** работы над тактикой
- ❌ **«Промежуточный продакт-оунер заменяет CEO в approval»** — нет, anchor требует executive-уровня approve, потому что туда входят strategic-вопросы (целевой рынок, pricing, конфликты в портфеле)
- ❌ **«Каждый кампания требует нового anchor»** — нет, anchor стабилен пока продукт/позиционирование стабильны; тактические кампании работают в рамках одного anchor

## Связанные страницы

- [[canon/marketing-frameworks/three-dept-conflict-prdoctor]]
- [[canon/marketing-frameworks/marketing-sales-alignment-framework]]
- [[canon/marketing-frameworks/definition-of-done-product-positioning]]
- [[canon/marketing-frameworks/refused-customer-interview]]
- [[canon/marketing-frameworks/event-coordination-checklist-prdoctor]]
- [[canon/marketing-frameworks/b2b-pr-influence-shift-2026]]
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]]
- [[canon/product-knowledge/gro-intensive]]
- [[sources/2026-05-19-pressfeed-prdoctor-marketing-pr-sales-conflict]]
