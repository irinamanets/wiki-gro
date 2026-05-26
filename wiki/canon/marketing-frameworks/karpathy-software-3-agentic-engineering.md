---
id: mkt:canon/marketing-frameworks/karpathy-software-3-agentic-engineering
title: "Software 3.0 + agentic engineering — Karpathy AI Ascent 2026"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai-agents, content, awareness, software-3, agentic-engineering, vibecoding]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-26  # +Karpathy → Anthropic (19 мая 2026) — автор фрейма теперь в Anthropic, что меняет sponsor-вес концепта
sources: [sources/2026-05-05-tg-products-and-startups-mar-may-2026.md, sources/2026-05-26-tg-ai-newz-may-19-25-2026.md]
namespace: mkt
---

# Software 3.0 + agentic engineering

**Эволюционная рамка от Andrey Karpathy** (выступление на AI Ascent 2026 от Sequoia, [запись](https://www.youtube.com/watch?v=96jN2OCOfLs)), пересказ + интерпретация Байрама Аннакова в [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] пост 1737. Зафиксировано в `canon/marketing-frameworks/`, потому что это **концептуальное переименование того, чем занимаются разработчики и AI-builder'ы** — устойчиво, переносится на любой пресет, и определяет язык сегмента ЦА, к которому маркетинг GRO обращается.

## Тезис в одном абзаце

**Software 3.0 = новая поверхность программирования, где первичный артефакт — контекст, а не код.** Поверх 1.0 (классический код) и 2.0 (нейросети как функция) появился слой, где разработчик собирает **контекст**, а LLM выполняет вычисление. Логичное следствие: **agentic engineering > vibecoding** — научиться вайбкодить не сложно, поддерживать качество традиционного софта при этом — альфа.

## Определения

| Уровень | Что программируется | Артефакт | Кто умеет |
|---|---|---|---|
| Software 1.0 | Логика напрямую | Код (Python/Go/JS) | Классические инженеры |
| Software 2.0 | Веса нейросети | Датасеты + архитектура | ML-инженеры |
| Software 3.0 | Контекст для LLM | Промпт + skill + harness + memory | AI-product engineer |

Software 3.0 не отменяет 1.0 и 2.0 — оно поверх них. То, что Карпатый прогал «вчера» (MenuGen в YC Summer School — сайт, где LLM генерит меню) теперь делается **одним промптом в Gemini**. Поверхность программирования сдвигается вверх по абстракции.

## Четыре scoping-тезиса Karpathy

### 1. Неоднородность интеллекта моделей

Модели иногда «жутко тупят» на простейших вопросах (Karpathy пример: «я в 50 м от автомойки, ехать или дойти пешком?» → LLM: «дойти, всё равно помоют»), при этом могут [написать C-компилятор с нуля](https://www.anthropic.com/engineering/building-c-compiler) (показательный кейс Anthropic, март 2026). По Karpathy, дело в трёх факторах:

1. **Верифицируема ли задача** — есть ли deterministic ground truth
2. **Достаточно ли данных для тренировки** — collected vs synthetic
3. **Приоритеты ведущих лабораторий** — что они оптимизируют

«Incentives matter» — это явно тот же принцип, что в [[canon/marketing-frameworks/harness-engineering-for-ai-agents|harness engineering]] про Bezos one-way doors и **«агент падает до уровня harness'а»**. Лаборатории оптимизируют под свои eval'ы → модели сильны там, где лаборатория собрала данные и придумала evaluation.

### 2. Agentic engineering > vibecoding

**Vibecoding** = попросить LLM собрать MVP и принять то, что получилось. **Agentic engineering** = построить harness вокруг LLM (см. [[canon/marketing-frameworks/harness-engineering-for-ai-agents]]) так, чтобы автономный агент **поддерживал тот же уровень качества, что и традиционный софт** — детерминированные проверки, sandbox, memory, self-review, retryable vs non-retryable шаги, pass@k vs pass^k разделение.

«Любой традиционный софт сейчас можно завайбкодить. Но ключевая сложность — как при этом поддержать тот же уровень качества. Именно здесь и альфа для билдеров.»

### 3. Какие скиллы людей останутся

Три устойчивых скилла, по Karpathy:

- **Планирование и контроль** — где должен оказаться продукт, где remember'ить ограничения
- **Вкус** — что хорошо, что плохо. Этот скилл — главный фильтр между vibecoded MVP и продакшен-качеством
- **Понимание** — глубинное знание задачи, не делегируемое модели

> **«You can outsource your thinking, but you cannot outsource your understanding»** — ключевая цитата Карпатого, которую он часто переиспользует в последние недели. Перекликается с [[evolving/content-trends/ai-product-engineer-content-hooks|hook-семейством]] «Граф 3023 заметок» (пост 1711) и [[evolving/industry-trends/ai-cognitive-atrophy-identity-2026|cognitive atrophy]] аргументом.

### 4. Совет фаундерам — «слепые зоны лабораторий»

«В принципе, любая область может быть описана как верифицируемая в той или иной степени, вопрос лишь в том, насколько сложно собрать данные и построить тренинг для них и приоритетов лабораторий. Поэтому **"слепые зоны" лабораторий (в части данных и инсентивов) — первые кандидаты**».

Это операционный фрейм: **где нужны данные, которые лабы не собирают, и нет инсентива оптимизировать?** Эти ниши — кандидаты для startup. Связь с [[evolving/industry-trends/ai-vertical-services-vc-uplift-2026|vertical AI services]]: vertical-vendor собирает доменные данные, лаба не собирает.

## Эволюция нарратива Karpathy за 2 года (2024 → 2026)

Из ретроспективы Бая (пост 1737):

| Тезис | AI Ascent 2024 | AI Ascent 2026 | Что изменилось |
|---|---|---|---|
| Скорость эволюции моделей | «не предполагалась» | реально каждые 3-6 мес фаворит меняется | Modus operandi → moving target |
| LLM as OS | сильная идея | ещё жива, теперь говорит «модель как компьютер» | Конкретизировалось до Software 3.0 |
| Open-source и экосистема | один из главных тезисов | **почти исчезли** упоминания | Сдвиг к managed-stack (Anthropic, OpenAI) |
| Поверхность программирования | код, агенты как assistant | **контекст**, agentic engineering > vibecoding | Software 3.0 явно артикулирован |

«Open-source vs proprietary» disappearance — наблюдение Karpathy, не прогноз. Это сигнал, что для индустрии вокруг Anthropic/OpenAI managed-стек сейчас доминирующий нарратив; ByteDance Deerflow 2.0 (см. [[evolving/industry-trends/ai-agent-economy-2026]] §8) — контр-сигнал, но в Sequoia-нарративе пока не звучит.

## Связь с marketing-strategy GRO

GRO работает с сегментом, для которого язык «Software 3.0» — родной. Соответственно:

1. **Tone-of-voice signal:** говорить о продукте в категориях «контекста, а не функционала» — резонирует с этой ЦА. См. [[evolving/content-trends/ai-product-engineer-content-hooks]] hook «Granular harness > generic motivation».
2. **Anti-positioning to курсы prompt-инжиниринга:** их обещание = vibecoding. GRO-аналог — **agentic engineering for self**: построить harness для тренировок, а не «пробудить мотивацию». Связь с [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] и [[evolving/content-trends/ai-flattery-dark-pattern]].
3. **Понимание > мышление:** core skill «вкус» переносится в content GRO как «способность отличить эффективную тренировку от пустой». GRO даёт harness, но **вкус остаётся за пользователем** — и это нормально, мы не хотим заменять его суждение, мы хотим освободить energy для него.
4. **Слепая зона лабораторий = vertical health.** Лабораторные foundation models не оптимизируются под персональную fitness-данных. Vertical-vendors (включая GRO) — natural fit для совета Karpathy.

## Граница применимости

- **Не используется как hype-rhetoric.** «Software 3.0» — это технический концепт; подавать в GRO-контенте как мем-фразу — обесценить. Лучше использовать рамку, не термин.
- **Karpathy — авторитетный, но не последняя инстанция.** Альтернативные рамки (LangChain «agentic systems», Anthropic «harness engineering» как product term, Microsoft «agent-first») сосуществуют — Karpathy просто наиболее визуальная подача.
- **`confidence: high`** на наблюдениях (видео фиксированное, цитата дословная), `medium` на интерпретации Бая (как и любая интерпретация выступления).

## Update 2026-05-26 — Karpathy → Anthropic меняет sponsor-вес фрейма

19 мая 2026 Andrej Karpathy [официально присоединился к Anthropic](https://twitter.com/karpathy/status/...) (см. [[volatile-strict/competitor-news/anthropic-karpathy-join-2026-05]] + [[sources/2026-05-26-tg-ai-newz-may-19-25-2026|@ai_newz post 4582]]). Это **меняет статус автора фрейма** и косвенно sponsor-вес концепта:

- **До:** Karpathy = ex-OpenAI/Tesla, founder Eureka Labs (образовательный стартап), freelance researcher. Software 3.0 — собственный фрейм без affiliation.
- **После:** Karpathy = Anthropic researcher. **Software 3.0 фрейм имплицитно связан с Anthropic-stack** (Claude Code, harness engineering, Claude Design, Managed Agents).

**Импликация для GRO-контента:**

1. При использовании фрейма в постах — упоминать Anthropic-context факультативно, но **исторический trace важен** (Karpathy ходил по нескольким лабам). Не подавать как «Anthropic концепт».
2. **Возможная coming evolution фрейма:** Karpathy теперь имеет инсайдер-доступ к Anthropic frontier работе — следующие его публичные выступления / посты могут добавить layer Software 3.5 или operational-фрейм поверх 3.0. Следить за каналом.
3. **Связь с [[canon/marketing-frameworks/frontier-lab-vs-startup-career-tradeoff]]**: Karpathy сам — case **iteration** (freelance ↔ frontier-lab) в этом career-tradeoff'е. Его возвращение во frontier-lab показывает, что **freelance/startup-фаза не closes door обратно**.

## Связанные страницы

- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]] — operational layer Software 3.0 (как именно строить контекст-harness)
- [[canon/marketing-frameworks/karpathy-ai-60s-mainframe-analogy]] — соседняя Karpathy-рамка (макро-уровень: где мы в индустриальной волне)
- [[evolving/industry-trends/ai-cognitive-atrophy-identity-2026]] — «outsource thinking но не understanding» как философская подложка
- [[evolving/content-trends/ai-product-engineer-content-hooks]] — content-hooks bank, использующий эту рамку
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]] — vibecoding как baseline, agentic engineering как уровень выше
- [[evolving/industry-trends/ai-vertical-services-vc-uplift-2026]] — «слепые зоны лабораторий» как стратегический совет
- [[canon/marketing-frameworks/frontier-lab-vs-startup-career-tradeoff]] — Karpathy как case-iteration в этом фрейме
- [[volatile-strict/competitor-news/anthropic-karpathy-join-2026-05]] — Karpathy → Anthropic анонс
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]] — первоисточник Software 3.0 (AI Ascent 2026)
- [[sources/2026-05-26-tg-ai-newz-may-19-25-2026]] — Karpathy → Anthropic update

## Backlinks

_10 pages link to this one._

- [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]]
- [[canon/marketing-frameworks/anti-sycophancy-system-prompt]]
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]]
- [[canon/marketing-frameworks/karpathy-ai-60s-mainframe-analogy]]
- [[evolving/content-trends/ai-product-engineer-content-hooks]]
- [[evolving/industry-trends/ai-cognitive-atrophy-identity-2026]]
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-products-and-startups-mar-may-2026]]
