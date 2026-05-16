---
id: mkt:evolving/industry-trends/ai-agent-marketplace-project-deal-2026
title: "AI-to-AI marketplace — Anthropic Project Deal 2026"
type: page
subtype: insight
layer: evolving
theme: industry-trends
tags: [ai-agents, agent-economy, marketplace, content, awareness, project-deal]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-products-and-startups-mar-may-2026.md]
namespace: mkt
---

# AI-to-AI marketplace — Anthropic Project Deal 2026

**Первый публично документированный масштабный эксперимент**, в котором AI-агенты автономно проводили переговоры и совершали покупки/продажи на маркетплейсе **без участия людей в самом процессе**. Источник: [Anthropic Project Deal](https://www.anthropic.com/features/project-deal), пересказ Байрама Аннакова в [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] пост 1728 (2026-04-27).

Это `evolving`-страница, потому что наблюдаемый pattern (a) ещё в фазе ранней экспериментации, (b) метрики неравенства между моделями будут пересматриваться по мере появления новых релизов, (c) GTM-импликации формируются live в апреле–июне 2026.

## Что это было

**Set up:** 69 сотрудников Anthropic. Каждому AI-агент проводил **intake interview**:
- Что продаёшь?
- Что хочешь купить?
- Инструкции по стилю торга (пример из поста: «когда торгуешься, говори в стиле уставшего ковбоя, у которого жизнь не задалась»)

**Mechanism:** Slack-канал, в котором агенты могли предлагать товары, вести переговоры, заключать сделки. **Все переговоры и решения принимались агентами автономно.**

**Результаты:** `[conf:high, src:2026-04-27]`
- **186 сделок** на **$4 000** общего объёма
- Средний чек ~$21,5 (личные вещи сотрудников)
- После завершения — люди приходили получать и отдавать товары физически

После того, как все сделки были заключены, люди приходили получать и отдавать товары физически `[conf:high, src:2026-04-27]`.

## Ключевая находка — ресурсное неравенство между моделями

`[conf:high, src:2026-04-27]` Эксперимент эмпирически зафиксировал то, что Бай гипотетизировал в посте 1439 ранее («AI агенты у богатых будут иметь больше compute и доступа к информации, будут умнее вести переговоры и несправедливо распределять ресурсы»):

| Транзакция | Opus-агент продал | Haiku-агент продал | Дельта |
|---|---|---|---|
| Сломанный складной велик | $65 | $38 | **+$27 (+71%)** `[conf:high, src:2026-04-27]` |
| Средний spread по продажам | базовая цена + ~$3 | базовая цена | **+$3** `[conf:high, src:2026-04-27]` |
| Средний spread по покупкам | -$3 от запрошенной | базовая | **-$3 в пользу Opus** `[conf:high, src:2026-04-27]` |

То есть **на одной и той же сделке Opus-side получал ~$6 преимущества по сравнению с Haiku-side**. На объёмах единиц это незаметно, на масштабах — структурное неравенство, которое **scale-ит** по мере роста agent-volume.

## Импликации для agent-economy

### 1. Эмпирическое подтверждение compute-as-leverage гипотезы

До Project Deal тезис «более мощные модели будут лучше торговаться» был дедуктивным. Теперь — **измеренный эффект** на 186 сделках. Это меняет ставки в дискуссиях о regulatory framework, fairness, ресурсном equality в agent-mediated commerce.

### 2. Готовая proof-point для AI-divide narrative

Маркетинг-имплицации:
- Для b2c-аудитории: «у тех, кто платит за Opus, будут лучшие сделки в b2b-маркетплейсах будущего» — narrative-ladder для премиум-инструментов
- Для b2b-аудитории: «не упускайте 7-15% margin на model choice, когда compute уже не главная стоимость» (см. [[evolving-strict/market-data/ai-coding-tools-cost-explosion-2026]] — токены > зарплаты сотрудников)
- Для founder-аудитории: «agent-economy = сложноструктурированная игра, выигрывает не лучший продукт, а лучший harness × лучшая модель»

### 3. GTM-сигнал для категории «agent-native services»

Из обсуждения Бая в посте 1694 (предыдущий дамп): открытые вопросы для marketplace-architecture, теперь частично закрытые:

| Вопрос (1694) | Ответ Project Deal (1728) |
|---|---|
| Top grossing для агентов | Личные вещи! По крайней мере в pilot-эксперименте — secondary marketplace доминирует |
| Репутационная система | Не формализована — за один эксперимент агенты не успели накопить репутацию |
| Стиль негоциации | **Customizable per-агент** через intake interview («уставший ковбой») — это **новый GTM-вектор**: персонализация поведения агента под бренд клиента |
| Open b2b-контракт через агентов | **Открытый вопрос** Бая: через сколько месяцев первый b2b-контракт будет полностью заключён между двумя агентами без человека? |

## Связь с marketing GRO

Это **не direct fit для GRO как продукта**, но даёт два косвенных вектора:

### Контент-нарратив про fairness-в-эпоху-агентов

Hook-семейство, которое pierces «AI-везде-всем-помогает» оптимистичного нарратива:
- «Opus-агент продал велик за $65, Haiku — за $38. Один и тот же велик. Когда агенты будут торговаться за вашу зарплату — у кого будет премиум?»
- Сегмент: AI-аудитория, переход awareness → consideration. См. [[evolving/content-trends/ai-product-engineer-content-hooks]] для интеграции.

### Anchor-кейс «AI-в-real-world-not-just-chat»

Project Deal — это **не demo и не benchmark**. Это **operationalized agent commerce внутри реальной компании**. Для контента, объясняющего «AI-уже-делает-X-в-реальности», это самый чистый proof-point на дату 2026-05-05. Использовать как референс при cross-link с [[evolving/industry-trends/ai-agent-economy-2026]] и [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]].

## Что не вошло в публичный отчёт

- **Distributions** реальных моделей (сколько % сотрудников использовали Opus vs Haiku) — Anthropic не раскрыла. Это влияет на интерпретацию +$3 spread.
- **Selection bias.** 69 сотрудников — добровольцы, тип-A AI-natives. Не репрезентативно для general population.
- **Регуляторные импликации.** SEC/CFTC/EU не упоминались в публикации — но при scale-up такие эксперименты войдут в regulatory radar.

`confidence: high` на самом факте эксперимента и опубликованных цифрах (Anthropic — first-source). `confidence: medium` на интерпретации $3 spread как структурного, не stochastic.

## TTL и evolution

Страница `evolving`, ожидаемая полу-жизнь оценки **6 месяцев**: при выходе следующего поколения моделей (Opus 5? Sonnet 5?) или повторного эксперимента с другой стороной (OpenAI «AI commerce» pilot, Google Cloud b2b-agents) метрики неравенства надо переоценить.

Trigger для re-verify:
- Anthropic выпустит follow-up paper c numerical breakdown
- OpenAI/Google проведут аналогичный эксперимент → можно сравнить cross-vendor spread
- Появится первый публичный b2b-контракт, заключённый между агентами без человека (Бай задал вопрос «через сколько месяцев?»)

## Связанные страницы

- [[evolving/industry-trends/ai-agent-economy-2026]] — мета-страница про agent-инфраструктуру; Project Deal — её latest data-point
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — почему harness × model вместе определяют performance; Project Deal измеряет model-component
- [[evolving-strict/market-data/ai-coding-tools-cost-explosion-2026]] — Cost-сторона того же тренда: токены > зарплаты, model choice = страт. решение
- [[evolving/content-trends/ai-product-engineer-content-hooks]] — hook-bank, в который добавляется Project Deal hook
- [[volatile-strict/competitor-news/anthropic-claude-managed-agents-2026-04]] — параллельный launch Anthropic в managed agent-инфраструктуре
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] — первоисточник (пост 1728)

## Backlinks

_5 pages link to this one._

- [[evolving/content-trends/ai-product-engineer-content-hooks]]
- [[evolving/industry-trends/ai-agent-economy-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]]
