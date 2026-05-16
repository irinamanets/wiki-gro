---
id: mkt:canon/marketing-frameworks/retention-benchmarks-b2c
title: Retention-бенчмарки B2C-продуктов (Day-30, subscription retention)
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [retention, b2c, pmf, metrics, benchmarks, subscription, saas]
confidence: medium
stale: false
created: 2026-04-14
updated: 2026-04-14  # +второй Табунов-источник (@your_pet_project пост 575): subscription retention >90% как «bar of excellence»
sources: [sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026.md, sources/2026-04-14-tg-your-pet-project-jan-apr2026.md]
namespace: mkt
---

# Retention-бенчмарки B2C-продуктов

Reusable референс для оценки качества B2C-продукта (включая GRO) по двум retention-метрикам: **Day-30 retention cohort** и **subscription retention** (для подписочных продуктов). Thresholds зафиксированы как framework-константа в canon-слое, потому что описывают не конкретные текущие данные GRO (те живут в [[evolving-strict/product-metrics/gro-store-installs]]), а **правила интерпретации**, по которым мы смотрим на любые retention-числа — свои или конкурентов.

Источник thresholds — founder-voice Михаила Табунова ([[sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026]], посты 1154, 1163, 1185). Эксперт-inferred, `confidence: medium`. Пересекается с публичными бенчмарками индустрии (Appfigures, Mobbin, Lenny's Newsletter).

## Day-30 retention (M1) — B2C SAAS

| M1 retention | Трактовка | Что делать |
|---|---|---|
| <10% | «Всё плохо» — дырявое ведро | Не вливать paid traffic, переделывать продукт / value proposition |
| 10–20% | «Надо выживать» | Искать PMF, оптимизировать core loop, не масштабировать |
| 20%+ | «Золотой продукт» | Можно лить traffic, оптимизировать CAC/LTV, масштабировать |

Источник: [[sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026]] пост 1185.

**Операционный тест «дырявого ведра»** (пост 1163): если воронка выглядит как Day-1 40% → Day-7 15% → Month-1 3%, то **никакой трафик не поможет расти**. «Можно лить в него сколько угодно трафика, но расти всё равно не будет». Рост = retention, не acquisition.

## Subscription retention — подписочные B2C

| Subscription retention | Трактовка |
|---|---|
| <45% | Смерть продукта — «херовый продукт», подписочная модель не держится |
| 45–75% | Выживание |
| 75%+ | Ценный продукт — пользователи реально продлевают |

Дополнительно, порог «совсем плохо»: ниже **60%** subscription retention уже считается слабым продуктом, а не нормальной зоной выживания (пост 1154, на примере двух AI-ботов в Telegram).

**Второй Табунов-источник — «bar of excellence» порог 90%+.** В [[sources/2026-04-14-tg-your-pet-project-jan-apr2026|канале @your_pet_project пост 575]] («Просто – Сложно – Реально сложно») Табунов подымает планку для «реально сложного» до **>90% месяц-к-месяцу** и одновременно подтверждает Day-30 retention >20% как зону жизнеспособности:

| Retention-уровень | Табунов (пост 575) | Контекст |
|---|---|---|
| Day-30 retention >20% | «Если это так, то скорее всего продукт будет жить долго» | Та же граница, что в посте 1185 из @bossofyourboss — consistency между двумя источниками |
| Subscription retention >90% m/m | «Продукт создаёт реальную ценность» | Stricter чем >75% в посте 1185; трактуется как «bar of excellence», не новый baseline |

Это не противоречие и не supersession — `>75%` и `>90%` отражают разные зоны одной и той же шкалы: 75% = «ценный продукт, жить можно», 90% = «реально сложная цель, за которой гоняются инвесторы». Canon-порог остаётся 75% (общий baseline); 90% — aspirational target для «вершина кривой».

## Почему retention важнее acquisition

Универсальный принцип (Табунов, пост 1185):

> Если люди не возвращаются в продукт — никакой маркетинг не поможет. А если возвращаются — то он не особо и нужен.

Три следствия:
1. **Проблемы acquisition решаются деньгами** (больше paid traffic, больше каналов).
2. **Монетизацию можно подтюнить** (pricing, IAP, paywalls).
3. **А retention — это про то, полезен ли твой продукт на самом деле** (это сигнал PMF, не tuning).

## Связь с Product-Market Fit

Retention — количественный proxy для PMF в B2C-SAAS:

- **Актуальность проблемы.** Если люди не возвращаются, проблема либо не реальна, либо редкая (разовая).
- **Разовые проблемы vs постоянные.** Поиск работы, переезд, обучение навыку — плохая основа для стабильного B2C-бизнеса, потому что после решения пользователь уходит. Нужна проблема, **которую надо решать каждый день** (пост 1185, тезис 5).
- **Organic vs paid retention.** Органические пользователи обычно retention выше, чем paid. По retention среза «органика / paid» видно качество paid-канала (пост 1185, тезис 6).

## Как не надо накручивать retention

- **Уведомления в лицо.** Завалить пользователя пушами и рассылками даёт короткий всплеск активности, потом отписка и отток (пост 1185, тезис 7).
- **Косметические A/B-тесты без изменения value prop.** «В два раза поднять retention не получится» только за счёт интерфейсных правок (пост 1185, тезис 3).
- **Смотреть только acquisition-метрики.** Пример из поста 1163: 50 000 установок, install $0.50, conv 8%, ROMI 300%, рейтинг 4.7 — и всё это при M1 3%. «Дырявое ведро» на зелёных acquisition-метриках — частый кейс.

## Как правильно растить retention

**Положительный кейс Whoop** (см. отдельную страницу [[evolving/industry-trends/whoop-retention-case-2026]]):

- Delayed gratification: ключевые метрики разблокируются не сразу (Recovery через 4 дня, биологический возраст через 21 день).
- Streak-механика и push-дискотека при снятии браслета.
- Community-компонент как дополнительный retention-hook.

**Отрицательный кейс «дырявого ведра»** (пост 1163): все paid-метрики зелёные, но retention провален — лить трафик в такое = сжигать деньги.

**Параноик-мониторинг как условие выживания** (пост 1154): два AI-бота в Telegram с одинаковым трафиком и продуктом. У первого владельца M1 retention 30%, он думает это норма. У второго LTV x2 больше: он каждый день в логах, ловит все ошибки API, промпты, timeout'ы, саппорт-жалобы. Разницу retention сделало не рынок, а дисциплина мониторинга.

## Применение к GRO

- GRO — B2C-SAAS с подпиской (см. [[canon/product-knowledge/gro-pricing]]), поэтому обе шкалы применимы:
  - Целевая зона Day-30 retention: 20%+ (иначе PMF под вопросом).
  - Целевая зона subscription retention: 75%+ (ниже 45% — продукт надо переделывать, не маркетинг).
- Текущие operational числа GRO живут в [[evolving-strict/product-metrics/gro-store-installs]] и [[evolving-strict/product-metrics/gro-store-ratings]]; эти thresholds — шаблон их интерпретации.
- Важно: GRO как **привычка/дисциплина** (4 шага продуктивности) концептуально ближе к «повторяющейся каждодневной проблеме», чем к «разовой» (поиск работы, покупка) — это правильная категория для стабильного B2C-бизнеса по Табунову (пост 1185, тезис 5). Этот тезис переиспользуется в позиционировании [[canon/positioning/gro-value-proposition]].

## Связанные страницы
- [[canon/positioning/gro-value-proposition]]
- [[canon/product-knowledge/gro-app-overview]]
- [[evolving/industry-trends/whoop-retention-case-2026]]
- [[evolving-strict/product-metrics/gro-store-installs]]
- [[sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026]]
- [[sources/2026-04-14-tg-your-pet-project-jan-apr2026]]
- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]]
- [[canon/marketing-frameworks/tabunov-landing-anatomy]]
- [[canon/marketing-frameworks/tabunov-onboarding-principles]]

## Backlinks

_24 pages link to this one._

- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]]
- [[canon/marketing-frameworks/business-metrics-for-owners]]
- [[canon/marketing-frameworks/defector-loyalty-crm-analysis]]
- [[canon/marketing-frameworks/definition-of-done-product-positioning]]
- [[canon/marketing-frameworks/employee-retention-cost-bredova]]
- [[canon/marketing-frameworks/funnel-simplicity-principle]]
- [[canon/marketing-frameworks/grebenyuk-4x-markup-rule]]
- [[canon/marketing-frameworks/marketer-task-typing-fomichev]]
- [[canon/marketing-frameworks/petscom-unit-economics-failure]]
- [[canon/marketing-frameworks/tabunov-onboarding-principles]]
- [[evolving-strict/market-data/app-store-slop-2026]]
- [[evolving/content-trends/daily-streak-gamification-in-finance]]
- [[evolving/content-trends/entertainment-over-pain-framing]]
- [[evolving/content-trends/methodology-vs-execution-anti-hook]]
- [[evolving/content-trends/tabunov-founder-growth-hooks]]
- [[evolving/content-trends/your-pet-project-channel-hooks]]
- [[evolving/industry-trends/whoop-retention-case-2026]]
- [[index]]
- [[sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026]]
- [[sources/2026-04-14-tg-tinkoffbank-10557-daily-cashback-streak]]
- [[sources/2026-04-14-tg-your-pet-project-jan-apr2026]]
- [[sources/2026-05-05-tg-bossofyourboss-apr-may-2026]]
- [[volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026]]
- [[volatile-strict/industry-news/ru-subscription-autocharge-law-2026-03]]
