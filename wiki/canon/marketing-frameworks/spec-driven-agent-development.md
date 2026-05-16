---
id: mkt:canon/marketing-frameworks/spec-driven-agent-development
title: Spec-driven agent development -- методология Молянова
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai, methodology, agent, vibe-coding, content]
confidence: medium
stale: false
created: 2026-04-16
updated: 2026-04-16
sources: [sources/2026-04-16-vcru-blogs-molyanov-spiridonov-gorny.md]
namespace: mkt
---

# Spec-driven agent development -- методология Молянова

Публичная методология работы с AI-агентами, задокументированная Павлом Моляновым (founder Сделаем + Нейроцех, verified expert) в открытом репо и блог-постах на vc.ru. Устойчивая концепция (не зависит от конкретной модели), поэтому canon.

## Этапы

1. **user-spec-planning** -- интервью: агент расспрашивает человека о бизнес-задаче, фиксирует требования
2. **tech-spec-planning** -- перевод требований в техническую спецификацию
3. **task-decomposition** -- разбивка на автономные мелкие задачи с инструкциями
4. **do-task / do-feature** -- агент исполняет, субагенты проверяют после каждого этапа

## Ключевые принципы

По мнению Молянова:

- Разбивка на маленькие шаги с инструкциями (не один большой prompt)
- Проверка субагентами после каждого этапа (quality gate)
- Новая задача = новый чат (изоляция контекста)
- Интервью перед началом работы (discovery phase)
- «Работа с нейронками мало отличается от работы с людьми. Надо их обучать, продумывать бизнес-процессы, писать регламенты»

## Прикладные кейсы из Нейроцеха

- **Тендер через Claude Code:** резидент Нейроцеха рассказал, как его Claude Code агент самостоятельно выиграл тендер на разработку бренда -- «Я не глядя пишу своему AI-агенту: Разберись и подготовь КП. Агент пошел смотреть КП. Посчитано четко.»
- **Агент-copilot в продажах:** обработка итогов созвонов, оценка по технике, формирование КП на основе прайсов и болей клиента, обратная связь по созвону

## Маркетинговое значение

Методология -- reusable фреймворк для content-маркетинга GRO: объясняет «как работать с ИИ системно» аудитории, которая уже прошла стадию «попробовать ChatGPT». Совместима с messaging [[canon/positioning/gro-value-proposition]] про системность и рефлексию.

## Связанные страницы

- [[sources/2026-04-16-vcru-blogs-molyanov-spiridonov-gorny]] -- первоисточник
- [[evolving/competitor-positioning/neyrotsekh-molyanov]] -- кто стоит за методологией
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] -- рыночный контекст для агентов
- [[evolving/content-trends/ai-solopreneur-narrative-hooks]] -- как упаковать это в hooks

## Backlinks

_10 pages link to this one._

- [[canon/marketing-frameworks/peregudov-vibecoding-founder-playbook-2026]]
- [[canon/marketing-frameworks/rag-first-ai-implementation-melkozerov]]
- [[evolving/content-trends/ai-solopreneur-narrative-hooks]]
- [[evolving/content-trends/tg-posts-seo-repurposing]]
- [[evolving/content-trends/vibe-coding-curse-content-hooks-2026]]
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]
- [[index]]
- [[overview]]
- [[sources/2026-04-16-vcru-blogs-molyanov-spiridonov-gorny]]
- [[sources/2026-05-05-tg-peregudov-jan-may-2026]]
