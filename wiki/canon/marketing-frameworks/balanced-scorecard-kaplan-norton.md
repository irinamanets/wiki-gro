---
id: mkt:canon/marketing-frameworks/balanced-scorecard-kaplan-norton
title: "Balanced Scorecard (Kaplan/Norton) — 4 направления, 3 базовые стратегии"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [strategy, kpi, performance-management, alignment, decision]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources:
  - sources/2026-05-14-condense-e-xecutive-ru-34-articles.md
  - sources/2026-05-14-exec-339160-bsc-v-deistvii.md
  - sources/2026-05-14-exec-339174-bsc-novoe-zaklinanie.md
namespace: mkt
---

# Balanced Scorecard (Kaplan/Norton) — фреймворк управления через 4 направления

Reusable framework, введённый Robert S. Kaplan и David P. Norton в книге «The Balanced Scorecard: Translating Strategy into Action» (Harvard Business School Press, 1996). Вариант для постсоветских рынков — материалы e-xecutive.ru ~2003 («BSc в действии», «BSc: новое заклинание или стратегия»).

**Vintage warning:** конкретные кейсы (AT&T Canada +32%, Compaq vs Dell, AT&T vs ICQ) — иллюстративные, не данные для современных бенчмарков. Концептуальная структура (4 направления + 3 стратегии + anti-pattern «теста для дрессировщика») — устойчива.

## 4 направления развития (классическая структура BSc)

Каскадная логика: каждое предыдущее направление является **средством** для последующего, последующее — **целью** для предыдущего. Снизу вверх:

1. **Инновации / Обучение / Инфраструктура** — нематериальные активы, фундамент
   - Компетенции сотрудников
   - Информационные системы
   - Культура и мотивация
2. **Внутренние процессы** — что улучшить, чтобы реализовать конкурентную стратегию
   - Operational excellence
   - Управление клиентскими отношениями
   - Инновационный процесс
3. **Клиенты** — продуктово-маркетинговая стратегия + конкурентная стратегия
   - Customer satisfaction, retention, acquisition
   - Доля рынка в целевом сегменте
   - Доходность клиента
4. **Финансы** — отдача акционеру
   - ROE, ROIC
   - Выручка, EBITDA
   - Денежный поток

> **Кейс-логика:** чтобы дать акционеру отдачу (4), нужно завоевать клиента (3); чтобы завоевать клиента, нужно настроить процессы (2); чтобы настроить процессы, нужны люди, ИТ и культура (1).

## 3 базовые конкурентные стратегии

Какую логику BSc применить — зависит от выбранной стратегии (Treacy/Wiersema 1995):

| Стратегия | Logic | Pricing | Quality |
|---|---|---|---|
| **Лидерство по издержкам** | Минимальная цена | Lowest | Average / acceptable |
| **Лидерство товара** | Наилучшие показатели по отрасли | Premium | Highest |
| **Близость к потребителю** | Дополнительные сервисные услуги для узкого сегмента | Premium | Tailored |

BSc для каждой стратегии нагружает разные направления:
- Лидер издержек → сильный акцент на «процессы» (efficiency, cost reduction)
- Лидер товара → акцент на «инновации/обучение» (R&D, product excellence)
- Близость к потребителю → акцент на «клиентов» (deep relationship, customization)

## Эмпирика причины неудач стратегий

> **До 70% неудачных реализаций связаны не с качеством стратегии, а с плохой реализацией** `[conf:medium, src:~2003]`

US data, переупаковано в BSc-методике как обоснование появления BSc (стратегия без operational layer = bumbling). Современные оценки (Kotter, HBR Strategy Execution Research) дают близкую цифру (~60-70% strategies fail to execute).

## Доля нефинансовых KPI

> По данным, **35% от всех используемых компаниями ключевых показателей**, на основе которых принимаются управленческие решения, являются нефинансовыми `[conf:low, src:~2003]` (US data ранее 2003)

Тренд с тех пор продолжился: современные scorecard'ы у tech-компаний имеют 50%+ нефинансовых KPI (NPS, retention, engagement, employee satisfaction, time-to-value, qualitative product signals).

## Кейс AT&T Canada после внедрения BSc

> Темпы роста составили **32% за 3 года**, в то время как рынок в целом вырос всего на **4%**, а среднерыночные тарифы значительно снизились. `[conf:medium, src:~2003]`

Vintage иллюстрация — не данные. Polmer для BSc-методологии.

## Anti-pattern «теста для дрессировщика»

> Бизнесмен должен точно знать, **почему он потерпел неудачу или достиг успеха**, а традиционные финансовые показатели не дают этого знания — финдиректор «спросит коммерческого, тот — главного инженера, можно устраивать бесчисленные совещания, но так и не добраться до истины». `[conf:medium, src:~2003]`

Финансовый показатель — это **результат**, не **причина**. Чтобы понять причину, нужны opera- и leading-KPIs из направлений 1-3.

**Operational consequence:** топ-менеджмент не должен принимать решения, опираясь только на финансовый dashboard. Каждый финансовый показатель должен быть «подвешен» к одному или нескольким нефинансовым leading-индикаторам.

## Anti-pattern: AT&T vs ICQ — структурная слепота

> AT&T потребовалось **75 лет**, чтобы подключить 50 млн пользователей телефонной сети. ICQ набрала 50 млн пользователей систем интерактивного общения (чатов) всего за **2,5 года**. `[conf:medium, src:~2003]`

Vintage пример с очевидным сегодня выводом (network effects + zero marginal cost). Применение для BSc: traditional industries имели **другую структуру KPI** (рост абонентской базы лимитирован capacity infrastructure'а), новые industries оперируют **виртуальной capacity**. Нельзя слепо переносить KPI старой индустрии на новую.

## Anti-pattern: Compaq vs Dell — разные бизнес-модели

> Compaq девятикратно обновляет товарные запасы в год, Dell — более 25 раз. **Не значит, что Dell управляет запасами лучше** — это следствие разных бизнес-моделей: Compaq производит по прогнозу, Dell — на заказ. `[conf:medium, src:~2003]`

**Урок:** набор показателей всегда характерен для конкретной компании и стратегии, **нельзя слепо переносить отраслевые бенчмарки**. Бенчмарк имеет смысл только в рамках одной бизнес-модели.

Применение в маркетинге: CAC «как у Stripe» не имеет смысла для B2C-приложения. CR воронки «как у Shopify» не имеет смысла для enterprise SaaS. Каждый бенчмарк должен сопровождаться quality-параметром «совпадает ли наша бизнес-модель».

## Применение к GRO

### Структура BSc для GRO

**Финансы (горизонт 1):** MRR, churn rate, CAC payback, gross margin

**Клиенты (продуктово-маркетинговая стратегия):**
- Конверсия trial → paid
- D30 retention
- Daily active users / Monthly active users (см. [[evolving-strict/product-metrics/gro-store-ratings]] и [[evolving-strict/product-metrics/gro-store-installs]])
- NPS / Customer Satisfaction

**Внутренние процессы:**
- Time-to-value (от регистрации до первой завершённой задачи)
- Скорость релизного цикла
- Стоимость поддержки клиента
- Скорость закрытия багов

**Инновации / Обучение / Инфраструктура:**
- Velocity AI-фичи в продукте
- Скорость освоения новых каналов командой
- HR-метрики (eNPS, retention)
- Документированность процессов (см. [[canon/marketing-frameworks/claude-md-structure-marketing]])

### Какая стратегия у GRO?

GRO **не лидер по издержкам** (premium subscription) и **не лидер товара** (Notion / Things функционально шире). GRO = **близость к потребителю**: узкий сегмент (российские разработчики с pet-project'ом + owner-seller SMB), tailored UX, страновая локализация, premium-tier pricing допустим. См. [[canon/positioning/gro-value-proposition]] / [[canon/target-audience/gro-segments]].

**Следствие:** BSc для GRO должен нагружать направление «клиенты» (NPS, retention, deep customer-data) сильнее, чем «процессы» (operational excellence). Это противоречит «оптимизируем всё» — стратегический выбор делает фокус.

### Anti-patterns для GRO

- **Принимать решения только по MRR.** «Тест для дрессировщика» — почему MRR упал, без leading-indicators не понять.
- **Сравнивать CAC с benchmarks из других категорий** — Notion B2B-CAC не релевантен GRO B2C-CAC.
- **Копировать KPI-структуру Notion / Todoist.** У них другая стратегия (лидер товара).

## Связь с другими фреймворками

- **OKR vs BSc** — OKR (Doerr) можно рассматривать как simplified BSc (без жёсткой attribution к 4 направлениям). См. [[canon/marketing-frameworks/mbo-smart-cascade]] (MBO как предтеча OKR).
- **North Star Metric** (современный SaaS) — одна метрика, которая концентрирует business value. Часто живёт в направлении «клиенты» BSc.
- **AARRR / pirate metrics** (Dave McClure) — funnel-структурированный subset BSc для consumer products.
- **Customer Health Score** (B2B SaaS) — operational индикатор, который ввести в направление «клиенты».

## Anti-pattern hooks для контента

- **«MRR не объясняет, почему MRR падает. Нужна leading-индикация»** — diagnostic hook
- **«CAC как у Stripe = бессмысленный бенчмарк, если ваша модель — не Stripe»** — predictive hook
- **«70% стратегий не падают на execution, а проваливаются от отсутствия структурированных KPI»** `[conf:medium, src:~2003]` — content hook
- **«AT&T 75 лет vs ICQ 2,5 года: одна метрика, две индустрии»** — vintage-illustration hook

## Связанные страницы
- [[canon/marketing-frameworks/mbo-smart-cascade]]
- [[canon/marketing-frameworks/kpi-parallel-hypothesis-petrochenkov]]
- [[canon/marketing-frameworks/business-metrics-for-owners]]
- [[canon/marketing-frameworks/mckinsey-three-horizons-of-growth]]
- [[canon/marketing-frameworks/sales-quality-vs-quantity-vyakuba-kpi]]
- [[canon/marketing-frameworks/marketing-audit-protocol]]
- [[canon/positioning/gro-value-proposition]]
- [[sources/2026-05-14-condense-e-xecutive-ru-34-articles]]
