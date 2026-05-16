---
id: mkt:canon/marketing-frameworks/data-driven-viral-campaign-framework
title: "Data-driven viral campaign — фреймворк превращения owned-data в виральный контент"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [framework, viral, data-driven, content, owned-data, social-graph, marketing]
confidence: high
stale: false
created: 2026-05-15
updated: 2026-05-15
sources: [sources/2026-05-14-condense-web-vc-ru-tbank-27.md]
namespace: mkt
---

# Data-driven viral campaign — фреймворк

Переносимая методология превращения **накопленных собственных данных** (transactional, behavioral, social) в **персонализированный shareable-контент**, который пользователь публикует в соцсетях. Архетип — «Вселенная Тинькофф» 2020 ([[canon-strict/historical-campaigns/tbank-vselennaya-tinkoff-viral-2020]]), но фреймворк domain-neutral: применим к банкам, e-commerce, fitness/lifestyle-app, edutech и любому digital-продукту с накопленной user-base.

## Четыре шага фреймворка

### 1. Агрегация: данные → структура

Превратить «служебные» данные в **смысловую структуру**, доступную для отображения:
- Транзакции → социальный граф (кто кому платит / кому продают одни и те же ритейлеры)
- Покупки → персональные категориальные паттерны («что вы покупаете чаще, чем 80% похожих клиентов»)
- Действия в app → trajectory относительно cohort'а (рейтинги, leaderboard'ы, прогресс-карты)
- История поиска → персональная карта интересов

**Принцип:** данные, которые компания считает «infrastructure-only», часто становятся продуктовым контентом. Это не PII-нарушение, если показывается только агрегированно и относительно пользователя.

### 2. Персонализация: пользователь видит себя

Каждый user должен получить **уникальный артефакт**, привязанный к его собственному ID/аккаунту:
- «Ты в 3 рукопожатиях от X»
- «Твой top-5 категорий за год»
- «Среди 12M клиентов ты — 1247-й по…»

Психологический crank: **self-reflection > information**. Когда видишь себя в данных, хочется опубликовать.

### 3. Public anchors: celebrity-distance / leaderboard / relativity

Привязать персональный артефакт к **публично узнаваемым якорям**:
- Известные люди в графе («сколько узлов до Варламова»)
- Топ-перцентили («ты в 5% самых активных»)
- Сравнение с публичными бренчами («ты используешь продукт чаще, чем 90% когорты»)

Social-proof эффект: shareable hook должен показывать status (relative position), не просто факт.

### 4. Share-as-meaning + referral incentive

Шеринг должен быть **встроен в смысл просмотра**, не «опция в конце»:
- Shareable-карточка — единственный способ показать результат друзьям
- Referral-механика с призовым фондом за охват (не за конверсию в продукт напрямую)
- Visual format подходит под основные соц-сети (Stories aspect ratio, square card, OG-meta)

«Вселенная Тинькофф» использовала призовой фонд **1 000 000 ₽**, награждавший **активный шеринг**, а не покупку банковского продукта — это критично: incentive должен направлять виральность, не loss-leader продажу.

## Условия применимости

Фреймворк работает, когда выполнены **все три** условия:

1. **Data-moat.** Накопленные user-data, которые конкурент не может быстро повторить (transactional history, social graph, behavioral data). Для GRO — это user-progress, тренировочные паттерны, потребительские circulation в продукте.
2. **Critical mass.** Минимум ~100K active users для статистически значимой персонализации. Меньше — артефакт получится «пустым» или «один и тот же у всех».
3. **Privacy-safe aggregation.** Юридический + этический фильтр: показывать только то, что пользователь сам про себя может узнать (свои данные, не чужие). Публичные anchors — только согласованные / уже публичные персоны.

## Anti-patterns (когда не работает)

- **Просто красивый dashboard.** Если у пользователя нет персонального хука и нет share-мотивации — это analytics, не viral.
- **Слишком много данных.** Если артефакт показывает 20 метрик — он не shareable. Хорошие data-viral-кампании показывают **одну сильную метрику** на one-page.
- **Привязка к продуктовому upsell.** Если в конце «купи Premium чтобы увидеть полную картину» — virality убивается. Полный артефакт должен быть free; upsell — отдельный layer.
- **Манипулятивные сравнения.** «Ты хуже 90% когорты» — генерирует shame, не sharing. Сравнения работают, когда показывают **status uplift** или **achievement**, не failure.

## Бенчмарки и валидация

| Кампания | Год | Domain | Data-источник | Outcome |
|---|---|---|---|---|
| Вселенная Тинькофф | 2020 | banking | 2 ТБ transactional + social graph 12M | viral, hyped в отраслевых медиа `[conf:high, src:2020]` |
| Spotify Wrapped | annual | music streaming | listening history → annual recap | global viral standard, ~60% MAU участвуют |
| Strava Year in Sport | annual | fitness | training data → personalized recap | strong viral momentum в fitness-cohort |
| Apple Music Replay | annual | music streaming | playback data | weaker viral than Wrapped из-за post-experience timing |

«Вселенная Тинькофф» — российский archetype data-driven viral; Spotify Wrapped — international gold standard, на который ссылаются почти все imitators.

## Применение для GRO

1. **GRO Year in Movement.** Ежегодная персонализированная карта тренировок: топ-5 типов активности, total минут, percentile relative к когорте, «дни прорыва» (биографические нарративы из streak-данных).
2. **Match Map / Fitness Graph.** Если у GRO появится social-layer (друзья тренируются вместе) — граф «через сколько шагов ты связан с конкретным тренером/амбассадором». Это direct-копия Вселенной с переносом банковского графа на fitness-граф.
3. **Streak Constellation.** Визуализация streak-данных как «созвездия» — каждая тренировка узел, цепочки = streaks. Похоже на data-art больше, чем на dashboard.
4. **Public-anchor hook.** Включить в визуализацию **известных fitness-blogger'ов / спортсменов** — пользователь видит, насколько он «близок» к их режиму. Не для платного endorsement'а, а для status-proof в shareable-карточке.

## Связанные страницы

- [[canon-strict/historical-campaigns/tbank-vselennaya-tinkoff-viral-2020]] — archetypal источник
- [[canon/marketing-frameworks/narrative-as-brand-currency]] — нарратив-валюта (смежная рамка)
- [[canon/marketing-frameworks/ugc-and-microinfluencers]] — UGC mechanism (data-viral как форма UGC где user шарит свою data-карточку)
- [[canon/marketing-frameworks/mrbeast-data-beats-ego-retention-graphs]] — data-driven decision-making (adjacent paradigm)
- [[canon/marketing-frameworks/peregudov-vibecoding-founder-playbook-2026]] — современные tools (можно собрать prototype Year-in-Sport за вечер на vibecoding-стеке)
- [[evolving/content-trends/tbank-vc-ru-content-mix-2019-2024]] — T-Bank контент-стратегия как контекст
- [[sources/2026-05-14-condense-web-vc-ru-tbank-27]] — источник
