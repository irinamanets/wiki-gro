---
id: mkt:evolving-strict/market-data/ai-vendor-revenue-per-employee-2026
title: "Revenue per employee — fastest-growing AI vendors (Feb 2026, Startup Riders × Ramp Economics Lab)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ai, anthropic, openai, cursor, replit, vercel, supabase, elevenlabs, lovable, productivity, revenue-per-employee, benchmark]
confidence: medium
stale: false
created: 2026-05-06
updated: 2026-05-14  # +Hyperliquid outlier ($102.4M/employee, 11 people) — выше AI-leaders на порядок
sources: [sources/2026-05-05-tg-typicalcompany-may-2026-redump.md, sources/2026-05-14-vcru-spiridonov-id79772-condensed.md]
namespace: mkt
---

# Revenue per employee — fastest-growing AI vendors

Числовой срез на февраль 2026 по выручке/сотрудник у самых быстрорастущих AI-вендоров (foundation models, vibe coding, voice AI, dev tools, BaaS) на основе **публичной инфографики Startup Riders × Ramp Economics Lab** (опубликована Feb 2026, data verified 2026-02-18). Источник попал в наш контекст через TYPICAL Telegram пост 1330 от 2026-05-04 (`[conf:medium, src:2026-05-04]` для самого факта re-share'а), но первичная атрибуция метрик — Ramp Economics Lab. `[conf:medium, src:2026-02-18]`

Расположена в `evolving-strict/market-data`, потому что: (а) revenue/empl. — численная метрика, дрейфующая по мере найма и роста выручки; (б) каждое число требует inline-маркера source-даты; (в) на момент **2026-05-06 это актуальный baseline** для AI-productivity-нарратива в маркетинге GRO. Перепроверка через 6 месяцев hard-required (см. supersession watch ниже).

## Сводная таблица — AI-вендоры

| Компания | Категория | Команда (~) | Revenue / employee | Source |
|---|---|---|---|---|
| Anthropic | Foundation Model | 2 500 | **$5,6 млн** | `[conf:medium, src:2026-02-18]` |
| OpenAI | Foundation Model | 4 000 | **$5,0 млн** | `[conf:medium, src:2026-02-18]` |
| Cursor | AI Code Editor | 300 | **$3,3 млн** | `[conf:medium, src:2026-02-18]` |
| Replit | AI Dev Tools | 110 | **$2,2 млн** | `[conf:medium, src:2026-02-18]` |
| Lovable | Vibe Coding | 150 | **$1,3 млн** | `[conf:medium, src:2026-02-18]` |
| ElevenLabs | Voice AI | 400 | **$825 тыс.** | `[conf:medium, src:2026-02-18]` |
| Supabase | Backend-as-a-Service | 150 | **$467 тыс.** | `[conf:medium, src:2026-02-18]` |
| Vercel | Web Dev / AI Cloud | 600 | **$333 тыс.** | `[conf:medium, src:2026-02-18]` |
| Granola | AI Meeting Notes | 40 | not disclosed | `[conf:medium, src:2026-02-18]` |
| xAI | Foundation Model | 1 200+ | not disclosed | `[conf:medium, src:2026-02-18]` |

**Контрольная линия от Ramp:** «$250K **"good" benchmark** for pre-IPO SaaS» `[conf:medium, src:2026-02-18]`. Это эталон, относительно которого читаются остальные числа.

**Non-AI outlier для перспективы (Спиридонов, vc.ru):**

| Компания | Категория | Команда | Revenue / employee | Source |
|---|---|---|---|---|
| Hyperliquid | Крипто-DEX | **11** | **$102,4 млн** (мировой рекорд) | `[conf:high, src:2026-05-14]` |
| Tether | Crypto stablecoin | н/д | **$93 млн** | `[conf:high, src:2026-05-14]` |

Hyperliquid превышает Anthropic в **18,3 раза** `[conf:high, src:2026-05-14]`. Важная оговорка: Hyperliquid — криптобиржа с сетевыми эффектами и нулевым маркетинг-бюджетом, это **не репрезентативный бенчмарк для SaaS/AI**. Включён как **экстремальная anchor-точка** для диапазона: $250K (good pre-IPO SaaS) → $5,6M (Anthropic) → $102,4M (Hyperliquid). Подробнее: [[evolving-strict/market-data/hyperliquid-microteam-benchmark-2026]].

## Сравнение с Mag 7 (FY 2024)

| Компания | Команда | Revenue / employee | Source |
|---|---|---|---|
| Apple | 164 000 | $2,4 млн | `[conf:medium, src:2026-02-18]` |
| Meta | 73 000 | $2,2 млн | `[conf:medium, src:2026-02-18]` |
| Microsoft | 228 000 | $1,0 млн | `[conf:medium, src:2026-02-18]` |

## Ключевые наблюдения

### 1. Топ-4 AI-вендоров уже опередили Mag 7 по revenue/empl.

Anthropic ($5,6 млн), OpenAI ($5,0 млн), Cursor ($3,3 млн), Replit ($2,2 млн) — все четыре превышают Apple ($2,4 млн), которая была эталонным ориентиром «безумно эффективной» компании последние ~10 лет. `[conf:medium, src:2026-02-18]`. Cursor с командой 300 человек делает revenue/empl. в **1,4 раза больше, чем Apple с 164 000 человек** `[conf:medium, src:2026-02-18]`.

### 2. Маленькие команды — структурно эффективнее

Связь размера команды и revenue/empl. **обратная**: чем меньше команда, тем выше показатель. Replit (110 чел.) делает $2,2M на человека `[conf:medium, src:2026-02-18]`, Cursor (300 чел.) — $3,3M `[conf:medium, src:2026-02-18]`. Это **не linear correlation** на всём списке (Anthropic 2 500 чел. при $5,6M переворачивает naive-нарратив «маленькие = эффективные»), но в категориях ниже foundation-model уровня правило держится.

### 3. 22-кратный gap к pre-IPO SaaS бенчмарку

Anthropic ($5,6 млн) превосходит «good» benchmark Ramp для pre-IPO SaaS ($250 тыс.) **в 22,4 раза** `[conf:medium, src:2026-02-18]`. Это не в категории «лучше среднего», это **другой режим экономики**, в котором software-производство переразвернулось в сторону high-leverage few-people-teams.

### 4. Категориальный разнос внутри AI

«AI-вендоры» — не однородный класс. Foundation models (Anthropic, OpenAI) — топ. Code editors (Cursor) — следующий tier. Vibe coding / agent platforms (Replit, Lovable) — средний tier. Voice AI / BaaS / Web dev (ElevenLabs, Supabase, Vercel) — нижний AI-tier, всё ещё **выше pre-IPO SaaS бенчмарка** ($250K), но уже сравнимо с traditional SaaS.

## Что это значит для маркетинга GRO

### Content-hook level

1. **Topic-anchor для AI-productivity нарратива.** Заголовочный hook **«Anthropic с командой 2 500 человек делает $5,6 млн выручки на сотрудника — это в 2,3 раза больше, чем Apple» `[conf:medium, src:2026-02-18]`** работает как attention-opener для top-of-funnel поста о том, что AI меняет product-economics. Должен цитироваться с атрибуцией Ramp Economics Lab / Startup Riders, не как наша оценка.

2. **Counter-anchor против скепсиса.** Часть аудитории GRO (карьеристы из non-tech фона) не верит, что AI реально меняет productivity. Числа $5,6 млн / $5,0 млн / $3,3 млн — это не abstract claim, это **измеренная revenue** компаний в открытых источниках. Цифры нивелируют эпистемологический разрыв.

3. **Permission to compare.** Иллюстрирует, что разница между «AI-native» и «AI-adjacent» бизнесом — **порядок величины на person-level KPI**, а не плюс-десять-процентов эффективности `[conf:medium, src:2026-02-18]`. Для GRO content это лицензирует крупный CTA: «не "встрой AI в один процесс"», а «**пересоберись вокруг AI**». Связь с [[evolving/industry-trends/ai-native-company-architecture-2026]] (если страница есть; иначе — с [[evolving/industry-trends/ai-native-marketer-skillset-2026]]).

### Funnel level

- **Top-of-funnel awareness post**: статичный creative с топ-4 AI-вендорами + «vs Apple» — для Reels / TikTok / vk.video / vk.shorts. Hook: **«Anthropic делает $5,6M на человека. Apple — $2,4M.»** `[conf:medium, src:2026-02-18]` Подпись: «Дело не в маржинальности — а в том, что AI-компании сами работают с AI».
- **Mid-funnel argument**: ссылка на эту страницу как evidence-строку в lead-magnet'е («Чек-лист: 7 признаков AI-native команды»).
- **Founder-segment specific**: для [[canon/target-audience/ru-smb-founder-owner-seller]] — рамка «**раньше команда 10 человек делала $1M, теперь команда 1 человек делает $1M**». Это resonant с pain-point этого сегмента (он уже единственный, кто реально продаёт — и теперь ему нужно убрать команду из-под себя, не расширять её).

### Anti-pattern (что не делать)

- **Не подменять оценкой revenue прибылью.** TYPICAL в посте 1330 называет это «прибылью на сотрудника», но это **выручка** (revenue per employee). Различие критично — Anthropic с большой долей COGS (compute) может иметь revenue/empl. $5,6M, но profit/empl. ниже на порядок. См. supersession watch ниже.
- **Не экстраполировать на не-AI-стартапы.** Ramp benchmark $250K для pre-IPO SaaS — это для «нормальных» SaaS, не для AI-нативных. AI-leaders далеко за пределами normal-SaaS-распределения по структурным причинам (capex, маржа, AI-leverage).

## Risks и оговорки

- **Размер команды — приблизительный.** «~2 500», «~4 000» — это публичные оценки, не точная HR-цифра. Колебания ±10% не меняют интерпретацию, но могут смещать ранжирование рядом стоящих компаний `[conf:medium, src:2026-02-18]`.
- **Revenue numbers — Ramp Economics Lab по corporate spend на ramp.com (платёжная платформа для бизнеса).** Это **proxy для контрактной выручки**, а не GAAP-выручка. Для foundation models это близко к реальной B2B-выручке (они продают через ramp-clients). Для consumer-led (Replit, Cursor) часть выручки идёт через app-stores / direct, и Ramp может её не видеть. → реальный revenue **может быть выше**, чем на инфографике.
- **Snapshot Feb 2026.** Числа — на момент верификации 2026-02-18. К маю 2026 (3 месяца спустя) Anthropic и OpenAI выросли по выручке (см. [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] — раунды и оценки), но команды тоже расширились. Net effect на revenue/empl. неизвестен без обновления Ramp.
- **«Не disclosed» — это не «zero»,** это **намеренно скрытая публичная информация**. Granola и xAI могут быть как сильно выше, так и сильно ниже среднего по списку.

## Supersession watch

- **Через 6 месяцев (~ноябрь 2026):** перепроверить через Ramp Economics Lab или альтернативные источники (Startup Riders, Ben Thompson Stratechery, The Information). Hard-стейл: если за 6 месяцев Anthropic нанял ещё 1 000 человек без пропорционального роста выручки — revenue/empl. может упасть, и нарратив «AI-leaders обгоняют Mag 7» нужно будет скорректировать.
- **При появлении первичных GAAP-данных (10-K Apple FY2025, 10-K Meta FY2025, IPO-проспекты Anthropic / OpenAI / Cursor)** — supersede эти числа на официальные с inline `[conf:high, src:<filing-date>]`.
- **При появлении Q2/Q3 2026 Ramp обновлений** — добавить параллельную колонку, не заменяя (для контроля рост-trajectory).

## Связанные страницы

- [[sources/2026-05-05-tg-typicalcompany-may-2026-redump]] — источник этого ingest'а (через re-share TYPICAL)
- [[evolving-strict/market-data/hyperliquid-microteam-benchmark-2026]] — Hyperliquid как мировой рекорд $102,4M/employee (non-AI outlier)
- [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] — оценки и финансирование AI-лидеров на Q2 2026 (валюация, не revenue/empl.)
- [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]] — связанный тренд: AI замещает middle-skill knowledge workers, 75% Google-кода через AI `[conf:medium, src:2026-04-22]`
- [[evolving/industry-trends/ai-productivity-j-curve-2026]] — productivity J-curve — почему даже в этих компаниях разрыв между AI-power-users и средним пользователем огромный
- [[evolving/industry-trends/ai-for-managers-2025-2026]] — связанный тренд AI-pressure на руководителей; добавлена 4-я data-точка из этого же поста 1330
- [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]] — TYPICAL framework о трёх сдвигах в product-economics, привязанный к этим метрикам
- [[evolving-strict/market-data/ru-economy-profit-per-employee-2024]] — параллельная страница с РФ profit-per-employee benchmark'ом (для контраста: РФ обрабатывающая промышленность 1,0 млн ₽ ≈ $11 тыс. — на 3 порядка ниже AI-leaders)

## Backlinks

_6 pages link to this one._

- [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]]
- [[evolving/industry-trends/ai-for-managers-2025-2026]]
- [[evolving/industry-trends/ai-knowledge-worker-climb-2025-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-typicalcompany-may-2026-redump]]
