---
id: mkt:volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05
title: "OpenAI Codex vs Claude Code: разворот загрузок 27.04–03.05.2026"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [openai, codex, anthropic, claude-code, ai-agents, dev-tools]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-14  # +ai-newz 4569-4570: Anthropic ответ на /goal (клонировано из Codex) + multi-agent management в Claude Code → product parity restored; +compute resolution через Colossus deal (4561)
sources: [sources/2026-05-05-vc-ru-condensed.md, sources/2026-05-05-vcru-ai-2910896-zagruzki-codex-ot-openai-prevysili-skachivaniya-c.md, sources/2026-05-05-tg-ai-newz-apr-may-2026.md, sources/2026-05-05-tg-vcnews-may-2-5-2026.md, sources/2026-05-14-tg-ai-newz-may-2026.md]
namespace: mkt
---

# OpenAI Codex vs Claude Code: разворот загрузок (27.04–03.05.2026)

За **5 дней** (27 апреля – 3 мая 2026) Codex от OpenAI обошёл Claude Code от Anthropic по числу ежедневных загрузок npm-пакета. По данным **TickerTrends** (через vc.ru):

| Инструмент | 27.04.2026 | 03.05.2026 | Δ за 5 дней |
|---|---|---|---|
| Codex (OpenAI) | 5 млн | **86,1 млн** | **+1397%** `[conf:high, src:2026-05-05]` |
| Claude Code (Anthropic) | 11,8 млн | **7,2 млн** | **−39%** `[conf:high, src:2026-05-05]` |

## Caveat по методологии

**TickerTrends измеряет скачивания npm-пакетов, не уникальных пользователей** `[conf:high, src:2026-05-05]`. Это критическое уточнение:

- npm-загрузка может происходить при каждой CI-сборке, при каждой переустановке dependency у нового разработчика, при автоматических обновлениях.
- Резкий рост за 5 дней может означать, что один крупный enterprise начал использовать Codex в CI/CD pipeline (умножая загрузки на N сборок/день), а не кратное увеличение пользовательской базы. `[conf:high, src:2026-05-05]`
- Цифру **нельзя** использовать как «X пользователей перешли с Claude на Codex».

## Что реально произошло (продуктовые сигналы)

OpenAI выкатила в этот же период три апдейта Codex:

- **16 апреля 2026** — добавлен автономный агент, поддержка GPT-Image 1.5, **>90 интеграций со сторонними сервисами**. Это — главный продуктовый драйвер.
- **30 апреля 2026** — команда `/goal` (планирование многоэтапных задач, аналог плагина в Claude Code).
- **1 мая 2026** — «питомцы» — тамагочи-индикатор активности AI-агента (UX-feature, gamification).

Параллельно Anthropic столкнулась с операционными проблемами:

- В конце марта / начале апреля 2026 пользователи Claude **жалуются на блокировки даже платных аккаунтов** `[conf:medium, src:2026-05-05]`. Причины (по vc.ru): подключение OpenClaw, регистрация из неподдерживаемых регионов.
- Это **не** falling-rocket-сценарий: в марте 2026 Bloomberg сообщал, что Anthropic **удвоила выручку** благодаря спросу на Claude Code, клиенты переходили на сервис летом 2025 `[conf:medium, src:2026-05-05]`.

## Интерпретация

1. **OpenAI выровняла feature-gap.** В марте–начале апреля 2026 Claude Code был очевидным премьером для serious dev-tools (Code agents, multi-step tasks, integrations) `[conf:medium, src:2026-05-05]`. К концу апреля Codex сравнялся: автономный агент, более 90 интеграций, `/goal`. После этого уже rational для команд переключаться обратно на Codex (особенно если они уже на ChatGPT Enterprise).
2. **Anthropic operational hits.** Блокировки платных аккаунтов в апреле — серьёзный signal об операционной перегрузке `[conf:medium, src:2026-05-05]`. Это, скорее всего, и есть структурная причина падения npm-загрузок Claude Code в этот период.
3. **Преувеличенный signal-character.** Реальная **доля рынка** dev-tools так быстро не сдвигается `[conf:medium, src:2026-05-05]`. Цифра npm-загрузок отражает либо измеренческий артефакт (npm-каскад), либо действительно резкий enterprise-rollout. Без независимых данных (DAU, paid customers) интерпретация ограничена.

## Анти-pattern для контента

- **Не** писать «Codex заменил Claude Code» / «Anthropic проиграл». 5-дневный срез + npm-каскад — слабая основа для нарратива.
- **Можно** писать «гонка обостряется», «OpenAI выровнял продукт», «Anthropic столкнулся с блокировками» — это поддерживается данными.

## Связь с broader narrative

Этот спайк — часть [[evolving/industry-trends/ai-corporate-race-mar-may-2026|гонки корпоративных AI-решений Q2 2026]]. Codex развивается агрессивно в тот же квартал, когда OpenAI запускает The Deployment Company и нанимает 3500 человек. Anthropic параллельно делает Claude Mythos и работает над enterprise-сегментом — оба идут в одну сторону, но через разные продукты.

## Update 2026-05-05 — Anthropic Claude Code postmortem (24 апреля 2026)

[[sources/2026-05-05-tg-ai-newz-apr-may-2026|@ai_newz пост 4550]] зафиксировал [официальный постмортем Anthropic](https://www.anthropic.com/engineering/april-23-postmortem) о деградациях Claude Code за весну 2026. Anthropic признала **три проблемы**, влиявшие на качество кода:

1. **Дефолтный reasoning effort незаметно сменили high → medium** на месяц `[conf:high, src:2026-04-24]`. Это объясняет subjective-жалобы пользователей на «Claude поглупел» — критическое cost-optimization-решение, которое прямо ударило по качеству output.
2. **Баг резал thinking из истории сессий >1ч**: размышления модели после каждого сообщения удалялись если сессия простаивала больше часа `[conf:high, src:2026-04-24]`. Пофиксили за две недели.
3. **Системный промпт просил генерить меньше токенов** `[conf:high, src:2026-04-24]`. Прямой cost-cut, ухудшавший reasoning-выход.

Anthropic ресетнула лимиты всем пользователям Claude Code и пообещала чаще использовать публичные версии Claude Code внутри компании, тестировать все изменения промпта.

**Интерпретация для гонки:** постмортем — это **операционный context для падения npm-загрузок Claude Code в апреле**. То, что выглядело как «pure product win OpenAI» (Codex рост загрузок), частично объясняется параллельной операционной перегрузкой Anthropic (cost-cut → деградация → пользователи переключаются). В дайджесте #116 (4 мая) автор @ai_newz явно фиксирует **выручка Codex выросла в два раза за неделю** `[conf:high, src:2026-05-04]`.

**Питомцы как gamification feature** (1 мая, [[sources/2026-05-05-tg-ai-newz-apr-may-2026|пост 4557]]): OpenAI добавили в Codex AI-питомцев («можно сделать гоблином»). Контраст из автора: «Из Claude Code тамагочи вырезали через неделю после добавления». Сигнал — **OpenAI инвестирует в UX/gamification**, Anthropic инвестирует в core capability и сейфгарды (Mythos, identity verification, compute-rationing) — стратегические priorities двух команд расходятся.

## Update 2026-05-14 — product parity restored + compute resolution

Два сигнала из [[sources/2026-05-14-tg-ai-newz-may-2026|@ai_newz май 2026]] меняют trajectory гонки:

**1. Anthropic клонировала /goal-режим из Codex** (пост 4569, 13 мая) `[conf:medium, src:2026-05-13]`. В Claude Code появился режим, в котором модель **не останавливается, пока не достигнет цели** — прямой клон `/goal` команды Codex от 30 апреля. Это **закрывает feature-gap**, который OpenAI создала за две недели до этого.

**2. Multi-agent management в Claude Code** (4569) `[conf:medium, src:2026-05-13]`. Claude Code заводит режим управления несколькими агентами сразу — число открытых терминалов уменьшится в разы. `@ai_newz` комментирует: «разработчики оркестраторов поверх клод кода напряглись» — то есть Anthropic поглощает функциональность third-party multi-agent оркестраторов внутрь самого Claude Code. Это **жёсткий ход против ecosystem-players**, которые строились на gap «нужно много терминалов».

**3. Compute crunch resolved.** Параллельно (6 мая) Anthropic подписала аренду Colossus у SpaceX — 200K GPU, лимиты Pro ×2, API лимиты «в разы» (см. [[volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05]]). Это **снимает операционную constraint**, объяснявшую падение npm-загрузок Claude Code в апреле через cost-rationing.

**Стратегический update нарратива:**

Картина «OpenAI выиграл, Anthropic проигрывает» из апреля **уже не точная**. К середине мая 2026:

- Anthropic закрыла compute crunch (Colossus deal)
- Anthropic закрыла feature-gap (multi-agent + /goal)
- Anthropic запустила revenue layer для third-party apps (см. [[volatile-strict/competitor-news/anthropic-third-party-credits-2026-06|кредиты с 15 июня]])

OpenAI в это время:
- Сохраняет лидерство по абсолютным npm-загрузкам
- Имеет AI-питомцев (UX gamification)
- Идёт в B2B через TPG/Brookfield/Bain joint venture

Это не **«один выиграл»** — это **two-front race с разными стратегиями**: OpenAI делает scale + UX, Anthropic делает feature-parity + ecosystem distribution. Контент для GRO должен отражать **обе ноги гонки**, а не one-sided narrative.

**Стилистическая ремарка автора** (пост 4569): *«Я не знаю кто в Антропике делает эти видео с анонсами, но они до боли хорошие»* — это **сигнал о качестве маркетинговой ассеты** Anthropic. Готовый hook: «качественные launch-видео — это сегодня differentiator на frontier-AI-рынке. Anthropic один из немногих, кто это понимает». См. [[evolving/content-trends/contrarian-framing-expert-telegram]] для CTA-формата.

## Связанные страницы

- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — макро-нарратив гонки
- [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] — финансовая сторона гонки
- [[volatile-strict/competitor-news/anthropic-800b-identity-verification-2026-04]] — Anthropic параллельно
- [[volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05]] — Colossus deal как compute resolution
- [[volatile-strict/competitor-news/anthropic-third-party-credits-2026-06]] — Anthropic ecosystem credits с 15 июня
- [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]] — flagship-продукт Anthropic
- [[volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1]] — рынок AI-coding в первом квартале
- [[sources/2026-05-05-vc-ru-condensed]] — источник
- [[sources/2026-05-05-tg-ai-newz-apr-may-2026]] — Anthropic Claude Code postmortem + Codex pets + выручка ×2 за неделю (W15–W18 ai-newz)
- [[sources/2026-05-14-tg-ai-newz-may-2026]] — May 2026 update: Anthropic ответ через /goal + multi-agent + compute resolution

## Backlinks

_8 pages link to this one._

- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-ai-newz-apr-may-2026]]
- [[sources/2026-05-05-tg-vcnews-may-2-5-2026]]
- [[sources/2026-05-05-vc-ru-condensed]]
- [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]]
- [[volatile/weekly-digest/ai-industry-news-w15-w18-2026]]
