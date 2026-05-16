---
id: mkt:evolving-strict/market-data/app-store-slop-2026
title: App Store slop — эффект vibe-coding на входящий поток заявок (Q1 2026)
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [app-store, market-data, vibe-coding, ai-tooling, discovery, ios, submissions]
confidence: medium
stale: false
created: 2026-04-14
updated: 2026-04-14
sources: [sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026.md]
namespace: mkt
---

# App Store slop от vibe-coding — количественный срез Q1 2026

Количественное наблюдение: поток заявок в Apple App Store ускорился в 2025–2026 из-за снижения порога разработки через vibe-coding (Claude Code, ChatGPT Codex и аналоги), что смещает узкое место со стадии production в стадию **discovery** магазина.

Источник первичного факта — пост 1187 канала [[sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026|@bossofyourboss]], который ссылается на первичный материал (Apple, через медиа-канал `bit.ly/4dDlL5d`). `confidence: medium` — числа транслированы из первичного медиа-канала через вторичный комментарий founder-автора, без прямой проверки пресс-релиза Apple на момент записи.

## Ключевые числа Q1 2026

| Метрика | Значение | Источник |
|---|---|---|
| Заявок в App Store за Q1 2026 | 235 800 | `[conf:medium, src:2026-04-09]` |
| Рост год к году Q1 | +84% | `[conf:medium, src:2026-04-09]` |
| Всего заявок за 2025 | ~600 000 | `[conf:medium, src:2026-04-09]` |
| Рост 2025 к 2024 | +30% | `[conf:medium, src:2026-04-09]` |
| Максимум годовых заявок с какого года | с 2016 | `[conf:medium, src:2026-04-09]` |
| Доля заявок, обрабатываемых за 48 часов | 90% | `[conf:medium, src:2026-04-09]` |
| Среднее время ревью Apple | 1,5 дня | `[conf:medium, src:2026-04-09]` |

Все числа — состояние на 2026-04-09 (дата публикации поста).

## Нарратив

1. **Причина всплеска — vibe-coding.** Инструменты типа Claude Code и ChatGPT Codex снизили порог разработки до такого уровня, что приложения теперь создают люди без опыта в программировании. Это прямо признаёт Apple в комментариях к своей статистике `[conf:medium, src:2026-04-09]`.

2. **Apple ревью масштабировано такими же AI-инструментами.** Девелоперы жаловались на очереди, но Apple отчиталась, что 90% заявок обрабатываются за 48 часов (среднее — 1,5 дня) `[conf:medium, src:2026-04-09]`. Механика: сами ревьюеры теперь работают с AI-ассистентами.

3. **Реальная проблема — не ревью, а discovery.** Табунов формулирует это так:

   > Реальная проблема не в ревью — Apple его масштабировала теми же инструментами, что создали волну. Проблема в discovery: когда Store заполняется тысячами посредственных аппок, найти нормальное становится всё труднее. Демократизация создания не решает распределение — узкое место просто смещается.

   Это встраивается в более общее наблюдение: масштабирование одного звена воронки **не решает** пропускную способность всей цепочки.

4. **Bonus-наблюдение поста 1188.** Автор отмечает отдельный паттерн: «в 2026 в апсторе новая тема — сначала жмут реджект по рандомной причине, потом разбираются». Это не число, но это operational-сигнал, что AI-ревью делает false-positive rejects чаще, и это создаёт побочный failure-mode для новых заявок `[conf:low, src:2026-04-09]`.

## Cross-факт: Amazon downtime от vibe-coding (пост 1170)

Отдельный эпизод, подтверждающий тезис «AI-код снижает порог, но повышает риск» с другой стороны рынка:

- За март 2026 AWS лежал 6+ часов `[conf:medium, src:2026-03-11]`.
- В декабре 2025 — 13+ часов даунтайма `[conf:medium, src:2026-03-11]`.
- Amazon связал даунтаймы с vibe-coding `[conf:medium, src:2026-03-11]`.
- Решение Amazon: все изменения от AI coding assistants должны проходить ревью сеньоров `[conf:medium, src:2026-03-11]`.
- Прогноз автора (не факт): в критичных сервисах AI-разработку запретят. `[conf:low, src:2026-03-11]`

Первоисточник, на который ссылается пост — Ars Technica `arstechnica.com/ai/2026/03/after-outages-amazon-to-make-senior-engineers-sign-off-on-ai-assisted-changes/`.
 [conf:medium, src:2026-04-14]
## Применение к GRO

- **GRO конкурирует в продуктивности-нише**, где порог входа после vibe-coding максимально низкий. Это означает: через 12 месяцев на рынке будут десятки слабых клонов GRO, сделанных вайбкодерами. Дифференциация — не «фичи», а [[canon/marketing-frameworks/retention-benchmarks-b2c|retention]] и brand-voice ([[canon/brand-guidelines/gro-typography]] + будущий brand manual).
- **ASO и discovery в App Store становятся сильнее**, чем просто маркетинговый бюджет. Это повод инвестировать в [[canon/product-knowledge/gro-app-store-listing]] как в asset.
- **False-positive rejects Apple AI-ревью** — риск для любого релиза GRO. Нужно иметь готовый playbook «что делаем, если получаем необоснованный reject».
- **Параллельно с iOS growth, Android slop растёт** (отдельно не квантифицировано, но Google Play исторически менее селективен). Это повышает ценность RuStore-версии ([[canon/product-knowledge/gro-rustore-listing]]) в российском контексте.

## TTL и supersession

Это evolving-strict метрика с жёстким TTL 180 дней. Пересматривать не позднее **2026-10-14**:
- Q2 2026 число заявок.
- Изменился ли процент AI-ревью.
- Появились ли пресс-релизы Apple/Google о discovery-изменениях.

Если Apple публикует официальную статистику 2025 позже (annual report), значения «~600K» и «+30%» нужно заменять на точные и оборачивать старые значения в HTML-комментарий. [conf:medium, src:2026-04-14]

## Связанные страницы
- [[canon/marketing-frameworks/retention-benchmarks-b2c]]
- [[canon/marketing-frameworks/funnel-simplicity-principle]]
- [[canon/product-knowledge/gro-app-store-listing]]
- [[canon/product-knowledge/gro-google-play-listing]]
- [[canon/product-knowledge/gro-rustore-listing]]
- [[volatile-strict/industry-news/ai-tooling-market-news-2026-q1]]
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]
- [[sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026]]
