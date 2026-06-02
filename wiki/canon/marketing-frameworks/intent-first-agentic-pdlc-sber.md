---
id: mkt:canon/marketing-frameworks/intent-first-agentic-pdlc-sber
title: Intent-first agentic PDLC — «от кода к намерению» (whitepaper Сбера AI-Disrupt)
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai, methodology, agentic-development, autonomy-ladder, intent-first, sber, content]
confidence: medium
stale: false
created: 2026-05-30
updated: 2026-05-30
sources: [sources/2026-05-30-tg-ai-newz-may-26-28-2026.md]
namespace: mkt
---

# Intent-first agentic PDLC — «от кода к намерению»

Методологический каркас перехода к агентной разработке, формализованный во **внутреннем whitepaper Сбера «AI-Disrupt PDLC»** (337 тыс. знаков, разбор на [Хабре](https://habr.com/ru/companies/oleg-bunin/articles/1038588/) через @ai_newz). Концепция стабильна между моделями и инструментами (описывает **парадигму**, а не конкретный продукт), поэтому `canon`. Конкретные числовые телеметрия-маркеры Сбера вынесены отдельно в [[evolving-strict/market-data/sber-agentic-dev-telemetry-2026]].

## Центральный сдвиг парадигмы

**От написания кода → к формированию намерения.** Спецификация первична, код становится **вторичным артефактом**. Операционное следствие, сформулированное в источнике: «сломался код? чиним не код, а спецификацию». Это переносит точку приложения человеческого усилия с реализации на постановку.

Рифмуется с уже зафиксированными в вики методологиями:
- [[canon/marketing-frameworks/spec-driven-agent-development|Spec-driven agent development Молянова]] (user-spec → tech-spec → decomposition → do-task) — Сбер даёт enterprise-формализацию того же принципа.
- [[canon/marketing-frameworks/karpathy-software-3-agentic-engineering|Karpathy Software 3.0]] — контекст/спецификация как новая поверхность программирования.

## Двухпетлевая модель IDP (Integrated Development Platform)

| Петля | Актор | Такт | Содержание |
|---|---|---|---|
| **Intent Loop** (петля намерения) | человек | дни | пишет спецификацию, проверяет результат, принимает архитектурные/продуктовые решения |
| **Implementation Loop** (петля реализации) | агенты | минуты | разработка по спецификации, прогон автотестов, мульти-агентная сборка |

**Жёсткое правило разделения труда:** функция человека — **намерение**, функция агента — **исполнение**. Архитектурные и продуктовые решения человек **не делегирует** — это граница автономии.

## Discovery Gap

Ключевая концепция whitepaper: **простая адаптация старого конвейера под новые инструменты даёт линейный потолок прироста (11–25%)**. Чтобы выйти за него, нужна перестройка самого процесса (две петли выше), а не «прикрутить ИИ к существующему pipeline». Это прямой аналог reframe «масштабирование ≠ PoC» из [[evolving/industry-trends/ai-agent-economy-2026|экономики AI-агентов]] (§15 Альфа-Банк).

## Адаптивная лестница автономии R0–R5

Вместо бинарного Human-in-the-loop (которое де-факто не работает — телеметрия показывает 93% авто-аппрува, разбор в [[evolving-strict/market-data/sber-agentic-dev-telemetry-2026]]) предлагается **градуированная автономия**:
- **Пакетные одобрения** (batch approvals) вместо подтверждения каждого действия.
- **Trust windows** — окна доверия, внутри которых агент действует без подтверждения.
- **Лестница R0–R5** — адаптивный уровень автономии под класс задачи и зрелость процесса.

Это перекликается с 3-step taxonomy Сбера из [[evolving/industry-trends/sber-gigaagent-ai-agents-narrative-2026|GigaAgent-нарратива]] (prompt → agent → autonomous entity) — обе рамки от одной компании, описывают спектр автономии.

## FinOps-предохранители

Мультиагентные архитектуры потребляют **~×15 токенов** vs классический чат-режим → whitepaper требует **Cost circuit breakers** (предохранители от зацикливания) как обязательный элемент. Cost-as-managed-variable рифмуется с cost-routing слоем ([[evolving/industry-trends/ai-agent-economy-2026]] §14 ClawRouters).

## «Окружение агента важнее модели»

Один из 5 поворотов whitepaper. Усиливает [[canon/marketing-frameworks/harness-engineering-for-ai-agents|harness-инженерию]]: качество результата определяется обвязкой (контекст, инструменты, guardrails, skills), а не выбором конкретной LLM. Это устойчивый принцип, переносимый на любой стек.

## Маркетинговое значение для GRO

- **Готовый anti-hype нарратив с enterprise-весом.** Сбер — mainstream-авторитет; «от кода к намерению» и «Discovery Gap» — это формулировки, которые можно использовать в контенте про системное (а не наивное) внедрение AI. Усиливает позиционирование GRO про системность и рефлексию ([[canon/positioning/gro-value-proposition]]).
- **«Парадокс джунов» как культурный hook.** Whitepaper фиксирует культурную побочку: новички вынуждены ревьюить сложный код, который пока не могут написать сами; сеньоры теряют «дофамин от самостоятельного решения». Это перенос на любую профессию, где агенты забирают core-работу — content-anchor про изменение роли специалиста (см. [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]]).
- **Intent-first как messaging-каркас.** «Учись формулировать намерение, а не исполнять» — прямой мостик к GRO-нарративу о развитии мышления, а не механического навыка.

## Атрибуция

Whitepaper внутренний (Сбер), разбор сделан ИИ-энтузиастом на Хабре, ретранслирован @ai_newz. `confidence: medium` — концепции согласованы с независимыми методологиями (Молянов, Карпатый), но первоисточник — корпоративный документ в пересказе, не peer-reviewed.

## Связанные страницы
- [[sources/2026-05-30-tg-ai-newz-may-26-28-2026]] — первоисточник
- [[canon/marketing-frameworks/spec-driven-agent-development]] — тот же intent-first принцип (Молянов)
- [[canon/marketing-frameworks/karpathy-software-3-agentic-engineering]] — контекст как поверхность программирования
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — «окружение агента важнее модели»
- [[evolving-strict/market-data/sber-agentic-dev-telemetry-2026]] — числовые маркеры зрелости
- [[evolving/industry-trends/sber-gigaagent-ai-agents-narrative-2026]] — продуктовая сторона Сбер-агентов
- [[evolving/industry-trends/ai-agent-economy-2026]] — макро-контекст agent-economy
