---
id: mkt:evolving-strict/market-data/ru-saas-rating-2025
title: "Saas-rating.ru — обновление 2025 года (выручка/прибыль RU SaaS по налоговой)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ru-saas, market-data, financials, moysklad, rating, awareness]
confidence: high
stale: false
created: 2026-04-27
updated: 2026-04-27
sources: [sources/2026-04-27-tg-startupoftheday-apr-15-27-2026.md]
namespace: mkt
---

# Saas-rating.ru — обновление 2025 года

[saas-rating.ru](https://saas-rating.ru/) — ежегодный рейтинг крупных RU SaaS-компаний, который раз в год собирает Аскар Рахимбердиев (founder МойСклад) с командой по **открытым данным налоговой**. На 2026-04-25 опубликован срез **за 2025 год** `[conf:high, src:2026-04-25]`.

## Методология (важна для confidence)

Источник данных — **открытые данные налоговой РФ**, не самоотчёт компаний. Это делает рейтинг методологически устойчивым:
- Нет risk'а под-/переоценки выручки самими компаниями
- Сопоставимая база между всеми участниками
- Точно идентифицирует growth/decline через год-к-году

Сам куратор называет его **«самым честным рейтингом RU SaaS»** `[conf:medium, src:2026-04-25]`. По наблюдению Александра Горного ([[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] пост 5032) — за methodological neutrality рейтинг используется как reference в RU venture- и SaaS-discussions годами.

## Срез 2025 года

Конкретные позиции и числа в нашей вики **не зафиксированы** на этой итерации — поверхностный анонс Горного передаёт только факт обновления. Если требуется конкретная статистика (топ-10, динамика, медианы) — обращаться к [saas-rating.ru](https://saas-rating.ru/) напрямую и зафиксировать здесь как отдельный data-pull.

**Что это значит для маркетинга GRO:**

GRO — мобильное B2C-приложение, не B2B SaaS (см. [[canon/product-knowledge/gro-team]]). Прямой попадки в этот рейтинг нет. Но **резерв полезности**:

1. **TAM-калибровка для конкурентов** — все B2B SaaS, которых GRO встречает в нативной рекламе или контентном пересечении (СберМегаплан, AmoCRM, hh.ru, и т.д.) присутствуют в этом рейтинге. Можно проверять ARR-порядки, не полагаясь на пресс-релизы.
2. **Сигнал зрелости рынка** — если медианная выручка топ-50 SaaS растёт год-к-году с замедлением, это **признак SaaS-плато в РФ** — что согласуется с тезисами [[evolving/industry-trends/software-moat-erosion-2026]] и [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]].
3. **Independent reference** для любых утверждений «рынок RU SaaS такой-то размером» — saas-rating + ЦБ+hh-сводка [[evolving-strict/market-data/ru-labor-market-hh-2026]] + [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] триангулируют картину RU digital-economy 2025-2026.

См. также [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] для price-структуры RU SaaS.

## Куратор: Аскар Рахимбердиев

- Founder и CEO **МойСклад** — один из старейших RU SaaS (с 2007 года) `[conf:medium, src:2026-04-25]`, лидер сегмента торгового учёта для SMB
- Активный публичный комментатор RU SaaS-рынка
- Делает saas-rating.ru как **общественную инициативу** (не коммерческий продукт), что снижает мотив к bias

`confidence: medium` для этих биографических деталей (взяты из публичных источников + анонсы Горного), `high` для самого факта существования рейтинга.

## Связанные страницы

- [[evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd]] — параллельный rating, но global+venture-оценочный (не выручка)
- [[evolving-strict/market-data/ru-smb-ecosystem-scale-2025]] — для cross-reference RU SMB-метрик
- [[evolving/industry-trends/software-moat-erosion-2026]] — context: почему SaaS-метрики становятся всё менее предсказуемыми
- [[sources/2026-04-27-tg-startupoftheday-apr-15-27-2026]] — first-mention в нашей вики

## Ре-верификация

Следующий срез saas-rating.ru обещан через год (≈2027-04). Если ingest-овать его — обновить эту страницу, добавить blocks year-over-year compare.
