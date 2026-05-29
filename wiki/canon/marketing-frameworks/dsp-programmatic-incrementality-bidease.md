---
id: mkt:canon/marketing-frameworks/dsp-programmatic-incrementality-bidease
title: "DSP-программатик как инкрементальный канал (рамка Bidease)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [dsp, programmatic, incrementality, mobile, bidease, channel-strategy, cpa, scaling]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-cossaru-may-19-25-2026.md]
namespace: mkt
---

# DSP-программатик как инкрементальный канал — рамка Bidease

Reusable рамка для оценки, **когда и почему** включать программатик-DSP в маркетинговый mix. Сформулирована командой «Бидиз» (Bidease) в карусели на канале Cossa в мае 2026. Bidease — игрок RU mobile-программатика, поэтому framing partial-PR, но сам концепт-сдвиг от «DSP как ещё один канал» к «DSP как инкремент к остальным» — переносим.

## Почему canon

Концепт инкрементальности канала — стабильная методологическая рамка, применимая к любому маркетинг-миксу. Конкретные DSP-провайдеры, ставки, бенчмарки → `evolving*`. Концепт переносим за пределы mobile (хотя Bidease формулирует для mobile).

## Главный тезис

«DSP — не "ещё один канал закупки". На практике именно он часто даёт **инкремент**, когда классические соцсети и поиск уже **упёрлись в потолок по CPA и охватам**.»

Это означает: DSP **не заменяет** Telegram Ads / Я Директ / VK Реклама / Mintegral, а **расширяет** общий охват и снижает marginal CPA — там, где основные каналы уже масштабированы максимально.

## 4 опорных вопроса рамки

Bidease задаёт 4 структурных вопроса для оценки DSP:

| # | Вопрос | Что проверяется |
|---|---|---|
| 1 | **Почему DSP помогает масштабироваться?** | Структурная причина: где DSP-inventory не пересекается с уже-закупленным в основных каналах |
| 2 | **Откуда берётся дополнительный трафик?** | Конкретные источники: какие сайты/приложения в DSP-сети не индексируются Я Директом и VK Рекламой |
| 3 | **Как проверять инкрементальность источника?** | A/B-тесты (control group без DSP-impression vs. exposed), incrementality lift |
| 4 | **Почему не каждая DSP действительно даёт рост?** | Качество inventory, fraud-фильтры, реальное пересечение с основными каналами |

Точные ответы (cossa.ru карусель к посту 23168) — в первоисточнике Bidease; здесь — рамка.

## Когда DSP-инкремент работает

DSP даёт инкрементальный охват **при условии**, что:

1. **Основные каналы насыщены.** Если Я Директ ещё не докручен по охвату (например, бренд тратит <50% доступного бюджета по auction), сначала там добирать охват.
2. **Аудитория **раздроблена** по сайтам/приложениям.** DSP силён там, где целевая аудитория проводит время в нишевых местах, недоступных через mainstream-каналы (специализированные mobile-apps, отраслевые сайты, in-app inventory).
3. **CPM в основных каналах **перегрет**.** Когда auction Я Директа толкает CPM выше эконом-границы — DSP открывает доступ к более дешёвому inventory вне основной аукционной перегрузки.
4. **Можно измерить incrementality.** Без A/B-теста против control group **нельзя сказать**, дала ли DSP реальный рост или просто «переломила» уже-готовых к покупке пользователей (cannibalization).

## Когда DSP не работает

- **На раннем этапе бренда.** Если ещё нет насыщения в Я Директ / VK, DSP — преждевременная диверсификация.
- **Маленький бюджет.** DSP-кампания меньше 300–500 тыс. ₽ часто не даёт статистически значимых результатов (auction-cost начальной фазы съедает бюджет).
- **Без proper attribution stack.** Без MMM или хотя бы post-impression conversion tracking — невозможно оценить incrementality.
- **С низкокачественным inventory.** «Дешёвая DSP» с fraud-наполненным inventory может **снизить общий ROAS**, потому что показы не достигают реальных людей.

## Operational-применение: 3-step pre-DSP-checklist

Перед запуском DSP-кампании задать 3 вопроса:

1. **Достигнут ли auction-ceiling в основных каналах?** Если бюджет в Я Директ / VK не выкручен по охвату — сначала туда.
2. **Готова ли система измерения incrementality?** A/B control group, holdout, attribution stack. Без этого DSP — «надежда», не measurement.
3. **Какая конкретно DSP подходит для моей вертикали?** Не «программатик вообще», а «именно эта DSP с этим inventory mix». Mobile vs. desktop, gaming vs. e-commerce, prog OOH vs. CTV — разные DSP.

## Импликация для GRO

GRO как mobile-app продукт с **долгой воронкой** (install → onboarding → habit → conversion) — потенциальный кандидат на DSP **позже**, когда:

- Я Директ и mobile UA-каналы (Mintegral, AppLovin) выкручены по охвату до auction-ceiling.
- Есть proper attribution stack (incrementality measurement через тесты или MMM).
- Бюджет позволяет осмысленный DSP-test (500K+ ₽).

**Сейчас (Q2 2026)** для GRO **рано**: бренд не выкручен в основных каналах, а DSP без incrementality measurement = дорогая «надежда». Hook для блога: «Когда программатик-DSP — это не пятая нога, а реальный рост: рамка Bidease». Применимо для аудитории GRO Сегмента 2 (предприниматели), которые часто **прыгают** в DSP без структурной оценки.

## Caveats

- **Bidease — заинтересованная сторона.** Партнёрский пост с framing «DSP даёт инкремент» — это в т. ч. PR. Сам concept-сдвиг валиден (incrementality — мейнстримная концепция в indust), но конкретные числа от Bidease нужно проверять.
- **Mobile-focus.** Bidease — mobile DSP. Рамка применима шире (web, CTV, prog OOH), но операционные детали будут отличаться.
- **Confidence: medium** — это качественная рамка, не measurement. Поднимется до `high` при появлении опубликованных incrementality-исследований с конкретными цифрами по RU-рынку.

## Связанные страницы

- [[evolving-strict/market-data/apptica-ru-mobile-creatives-q1-2026]] — параллельный замер от Bidease/Apptica про структурный сдвиг RU mobile
- [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] — общий контекст замедления рынка и перегретого аукциона
- [[canon/marketing-frameworks/clickless-channel-incrementality-stable-id]] — параллельная рамка incrementality для clickless-каналов
- [[evolving-strict/market-data/digital-ad-cpm-shifts-q1-2026]] — почему «auction-ceiling» в Я Директ — реальная проблема в 2026
- [[canon/marketing-frameworks/pervukhin-funnel-5-leaks-diagnostic]] — KINETICA-фреймворк диагностики перегретого аукциона (другой ответ на тот же вопрос)
- [[evolving/industry-trends/digital-indoor-retail-media-ru-2026]] — другая категория inventory, для другого вида incrementality
- [[canon/marketing-frameworks/marketplace-distribution-diversification-5-channels]] — общая стратегия диверсификации каналов
- [[sources/2026-05-26-tg-cossaru-may-19-25-2026]]
