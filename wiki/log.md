---
title: Operation Log
type: log
---

# Marketing Memory — Operation Log

Append-only журнал всех операций агента. Новые записи добавляются в конец.

Формат записи (префикс типа в квадратных скобках для grep-friendly парсинга):
```
## [YYYY-MM-DD HH:MM] [ingest|query|lint|reflect|preset-init] | <short title>
- source / read / input: ...
- created: ...
- updated: ...
- superseded: ...                                 # только для ingest, при supersession
- backfilled: ...                                 # только для query
- layer-touched: {canon: 2, evolving-strict: 3}   # счётчик страниц по слоям
- touched: N pages
```

Проверить парсинг:
```
grep -E "^## \[.*\] \[(ingest|query|lint|reflect|preset-init)\]" wiki/log.md
```

---

## [2026-04-10 11:50] [preset-init] | bootstrap marketing-memory
- namespace: mkt
- enabled_layers: [canon, canon-strict, evolving, evolving-strict, volatile, volatile-strict]
- themes_count: 18
- directories_created: 18 (layer/theme) + 0 (sources/lint-reports already existed)
- tag_groups: 5 (channels, funnel-stages, content-formats, personas, competitors)
- page_types: 11
- identity: null (command KB, not personal)
- domain_rules: empty placeholder (to be filled via REFLECT)
- files_generated: preset.yaml, rules.md, index.md, overview.md, log.md

## [2026-04-10 15:45] [ingest] | Пиархаб — исследование нативного PR 2026 (PDF, 80 стр)
- source: wiki/sources/2026-04-10-piarhub-research-native-pr-2026.md
- created:
  - wiki/canon/marketing-frameworks/native-advertising.md
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md
  - wiki/canon-strict/historical-campaigns/native-pr-cases-2026.md
  - wiki/evolving/industry-trends/native-pr-russia-2026.md
  - wiki/evolving/content-trends/telegram-native-formats.md
  - wiki/evolving/competitor-positioning/max-messenger.md
  - wiki/evolving-strict/competitor-metrics/social-platforms-ru-audience-2025.md
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md
- updated: wiki/index.md
- superseded: none (первый ingest в пресете)
- sensitive flag: контактные данные агентства (почта/телефон/адрес) оставлены только в raw/, в wiki не перенесены
- layer-touched: {canon: 2, canon-strict: 2, evolving: 3, evolving-strict: 2, sources: 1}
- touched: 11 pages (1 source + 9 synthesized + index)
- raw: raw/in-progress/documents/Исследование Пиархаб.pdf → raw/processed/documents/

## [2026-04-10 19:00] [ingest] | GRO — официальный лендинг продукта (groapp.ru)
- source: wiki/sources/2026-04-10-groapp-landing.md
- created:
  - wiki/canon/product-knowledge/gro-app-overview.md
  - wiki/canon/product-knowledge/gro-pricing.md
  - wiki/canon/product-knowledge/gro-team.md
  - wiki/canon/product-knowledge/gro-testimonials.md
  - wiki/canon/target-audience/gro-segments.md
  - wiki/canon/positioning/gro-value-proposition.md
- updated:
  - wiki/index.md
  - wiki/overview.md (первое заполнение «Что мы знаем» + gaps)
- superseded: none (первый product-focused ingest)
- sensitive flag: none — публичный first-party лендинг, PII отсутствует
- layer-touched: {canon: 6, sources: 1}
- touched: 9 pages (1 source + 6 synthesized + index + overview)
- raw: raw/links.md#https://groapp.ru/#download → status: processed

## [2026-04-10 19:40] [ingest] | GRO — листинг в App Store iOS (apps.apple.com)
- source: wiki/sources/2026-04-10-gro-appstore-listing.md
- created:
  - wiki/canon/product-knowledge/gro-app-store-listing.md
  - wiki/canon/product-knowledge/gro-app-store-reviews.md
- updated:
  - wiki/canon/product-knowledge/gro-pricing.md (supersession: точная цена 2 490 ₽/мес подтверждена IAP + добавлен SKU «100% Энергии» 2 990 ₽ + Contradictions-блок)
  - wiki/canon/product-knowledge/gro-app-overview.md (добавлен App Store-набор треков, What's new v1.6.14, Contradictions-блок про разнобой треков и дуальный framing)
  - wiki/index.md
  - wiki/overview.md (дистрибуция iOS, органические insights из отзывов, gaps)
- superseded: day-rate derivation цены на gro-pricing (лендинг давал 83×30≈2490; теперь подтверждено IAP как 2 490,00 ₽)
- sensitive flag: none — публичный листинг App Store, никаких PII
- layer-touched: {canon: 2 created + 2 updated, sources: 1}
- touched: 7 pages (1 source + 2 new canon + 2 updated canon + index + overview)
- raw: raw/links.md#https://apps.apple.com/ru/app/gro/id6754377283 → status: processed

## [2026-04-10 20:15] [ingest] | GRO — листинг в Google Play (play.google.com)
- source: wiki/sources/2026-04-10-gro-googleplay-listing.md
- created:
  - wiki/canon/product-knowledge/gro-google-play-listing.md
- updated:
  - wiki/canon/product-knowledge/gro-app-store-listing.md (cross-link на Android-сиблинг, категорийное расхождение Бизнес/Стиль жизни, кросс-платформенное подтверждение Bundle ID)
  - wiki/canon/product-knowledge/gro-pricing.md (кросс-платформенное подтверждение IAP-диапазона 2 490–2 990 ₽ через Google Play)
  - wiki/canon/product-knowledge/gro-app-overview.md (Android-листинг в границах, усиление store-канон vs site-канон split'а, JSON-LD ghost как третий Contradictions-пункт)
  - wiki/index.md
  - wiki/overview.md (Android-дистрибуция, framing split, gaps: CPA-готовность, SEO-ghost, домен gro.pro)
- superseded: none — Google Play подтверждает, а не конфликтует с App Store
- sensitive flag: адрес и телефон Romsfort East в Дубае оставлены только в source-странице (audit), в слои и контент не выносятся. Точное число установок (448) помечено как internal-only.
- layer-touched: {canon: 1 created + 3 updated, sources: 1}
- touched: 7 pages (1 source + 1 new canon + 3 updated canon + index + overview)
- raw: raw/links.md#https://play.google.com/store/apps/details?id=pro.gro → status: processed

## [2026-04-10 20:45] [ingest] | GRO — листинг в RuStore (rustore.ru)
- source: wiki/sources/2026-04-10-gro-rustore-listing.md
- created:
  - wiki/canon/product-knowledge/gro-rustore-listing.md
- updated:
  - wiki/canon/product-knowledge/gro-app-store-listing.md (cross-link на RuStore, публикатор-триангуляция Romsfort East vs ООО ГРО, категорийная триангуляция 2:1 за business)
  - wiki/canon/product-knowledge/gro-google-play-listing.md (cross-link на RuStore, LIFESTYLE как исключение 1:2, gro.pro подтверждён во втором сторе)
  - wiki/canon/product-knowledge/gro-pricing.md (RuStore не раскрывает IAP — отмечено как отсутствие раскрытия, не противоречие)
  - wiki/canon/product-knowledge/gro-app-overview.md (RuStore в границах, три из трёх сторов согласованы по трекам и рамке, Contradictions-блоки усилены тройной выборкой, What's new — разные release-notes между сторами)
  - wiki/canon/product-knowledge/gro-team.md (новый блок «Publisher-структуры»: две параллельные корпоративные ветки Romsfort East Dubai + ООО ГРО Россия, правило «не цитировать в контенте»)
  - wiki/index.md
  - wiki/overview.md (RuStore-дистрибуция, publisher-структуры, обновлён framing split 3:1, категорийный сюжет 2:1, остался один pending URL — веб-кабинет)
- superseded: none — RuStore подтверждает store-канон и не конфликтует с предыдущими сторами; лишь дополняет картину
- sensitive flag: none — публичный листинг, PII отсутствует, юр. структуры (ООО ГРО, Romsfort East) зафиксированы только в audit/внутренних ссылках, в контент не выносятся
- layer-touched: {canon: 1 created + 5 updated, sources: 1}
- touched: 9 pages (1 source + 1 new canon + 5 updated canon + index + overview)
- raw: raw/links.md#https://www.rustore.ru/catalog/app/pro.gro → status: processed

## [2026-04-10 20:15] [ingest] | GRO — веб-кабинет lk.groapp.ru (экран авторизации)
- source: wiki/sources/2026-04-10-gro-lk-auth.md
- created:
  - wiki/canon/product-knowledge/gro-web-app.md (четвёртая точка дистрибуции, Expo/React Native Web стек)
  - wiki/canon/brand-guidelines/gro-typography.md (первый каноничный сигнал о визуальной идентичности: Montserrat + Unbounded + SpaceMono)
- updated:
  - wiki/canon/product-knowledge/gro-app-overview.md (добавлен раздел про четвёртую точку дистрибуции и Expo-стек как объяснение синхронных релизов; tracks contradiction зафиксирован как НЕ закрытый после web-ingest)
  - wiki/canon/product-knowledge/gro-pricing.md (зафиксировано, что веб-кабинет не раскрывает цены pre-auth; маркетинговое следствие — контент-ссылки с прозрачной ценой направлять на лендинг, не на lk.groapp.ru)
  - wiki/index.md (новая source, два новых canon-страниц, оживлён раздел brand-guidelines)
  - wiki/overview.md (закрыт последний distribution-gap, частично закрыт gap по домену gro.pro, добавлен сигнал о Brand guidelines, уточнён статус tracks contradiction)
- superseded: none — веб-кабинет дополняет картину, ни с чем не конфликтует; tracks contradiction явно зафиксирован как non-resolved, что тоже не supersession
- sensitive flag: none — публичный экран регистрации, PII отсутствует в контенте страницы (только в формах ввода, не в HTML)
- notable findings:
  - GRO = единый cross-platform React Native кодбейс (Expo), объясняет синхронный релиз v1.6.14 на 3 стора
  - четвёртая точка дистрибуции (веб) закрывает distribution-map продукта
  - первый каноничный typographic stack занесён в brand-guidelines (раньше пуст)
  - домен gro.pro gap частично закрыт: веб-кабинет на groapp.ru, gro.pro узко legal/support
  - tracks contradiction НЕ закрыт — pre-auth экран треки не показывает
  - copy-hook «Сохраним твою точку старта» зафиксирован как переиспользуемый микро-копирайтинг
- layer-touched: {canon: 2 created + 2 updated, sources: 1}
- touched: 7 pages (1 source + 2 new canon + 2 updated canon + index + overview)
- raw: raw/links.md#https://lk.groapp.ru/auth/ → status: processed

## [2026-04-10 20:29] [reflect] | classification fix + ingest pipeline speedup
- analyzed: 7 ingest entries (Piarhub PDF + 6 GRO URLs) + user feedback on /ingest-pending batch
- report: wiki/lint-reports/2026-04-10-reflect.md
- proposed: (A) add `evolving/customer-feedback`, `evolving/product-reception`, `evolving-strict/product-metrics` themes; (B) add «Как выбрать слой» section to rules.md with operational-test and examples; (C) add operational-test line to wiki-ingest manual §5.1; (D) backfill misclassified pages via git mv (loose layers); (E) Phase 1 prefetch in /ingest-pending; (F) Phase 2 defer-finalize via new wiki-finalize subagent; (G) explicitly deferred Phase 4 autotrigger
- applied:
  - wiki/preset.yaml: +3 themes (customer-feedback, product-reception, product-metrics)
  - wiki/rules.md: +«Как выбрать слой» section
  - .claude/agents/wiki-ingest.md: +operational-test at §5.1, +defer-finalize mode section, +prefetch cache section, §9 and §11 now conditional, +new §11.5 (finalize-spec line contract)
  - git mv wiki/canon/product-knowledge/gro-app-store-reviews.md → wiki/evolving/customer-feedback/gro-app-store-reviews.md (front-matter updated)
  - wiki/evolving-strict/product-metrics/gro-store-ratings.md (new — ratings from all 3 stores, inline [conf,src] markers)
  - wiki/evolving-strict/product-metrics/gro-store-installs.md (new — installs from all 3 stores, inline markers)
  - wiki/canon/product-knowledge/gro-app-store-listing.md, gro-google-play-listing.md, gro-rustore-listing.md: ratings/installs blocks replaced with cross-links to new metric pages
  - cross-link updates: wiki/index.md (new subsections customer-feedback + product-metrics), wiki/overview.md, wiki/canon/product-knowledge/gro-app-overview.md, wiki/sources/2026-04-10-gro-appstore-listing.md, wiki/sources/2026-04-10-gro-googleplay-listing.md
  - .claude/agents/wiki-finalize.md (new subagent — aggregates shared-file updates from finalize-spec.jsonl)
  - .claude/commands/ingest-pending.md: rewritten as 3-phase (prefetch → defer-finalize synthesis → finalize)
  - CLAUDE.md: subagent registry now 4 subagents (+wiki-finalize), slash-command row for /ingest-pending updated, ownership table updated
- deferred: Phase 4 (auto-trigger on raw-drop) — not implemented; revisit after ~20 more ingest entries per user decision
- touched: 17 files (3 framework, 7 wiki synthesized/moved, 2 new metric pages, 2 new subagent/command docs, 3 cross-link updates)

## [2026-04-11 12:50] [ingest] | подкаст соло-фаундер + ИИ (видео, 27:39)
- source: wiki/sources/2026-04-11-podcast-ai-solopreneur.md
- created:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (добавлен раздел «Внешние сигналы, усиливающие сегменты 2 и 3 (2026-04-11)»: маппинг нарратива из подкаста на сегменты предпринимателей/фрилансеров/карьеристов, cross-links на новые evolving-страницы)
  - wiki/canon/positioning/gro-value-proposition.md (добавлен раздел «Внешние резонансы позиционирования (2026-04-11)»: резонансы тезисов «любопытство = главный навык», «барьер 200 $», объекции «одиночество» — с новой парой evolving cross-links)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/video/videoplayback.mp4 (+.transcript.md +.audio.mp3 +.note.md siblings)

## [2026-04-13 17:00] [ingest] | Субботин — исследование русскоязычной ИИ-аудитории ТГ-каналов (PDF, 22 стр, n=632)
- source: wiki/sources/2026-04-13-subbotin-ru-ai-telegram-audience.md
- created:
  - wiki/canon/marketing-frameworks/tam-technology-acceptance-model.md
  - wiki/canon/marketing-frameworks/rogers-diffusion-of-innovations.md
  - wiki/canon/target-audience/ru-ai-telegram-audience-segments.md
  - wiki/evolving-strict/market-data/ru-ai-telegram-audience-2026.md
  - wiki/evolving/industry-trends/ru-ai-audience-gap-2026.md
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (добавлен раздел «Частичное количественное подтверждение»: тезисы о барьере входа и спросе на агентов теперь подкреплены n=632, прогнозы остаются confidence:low)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (вводный абзац обновлён: ссылка на новую data-driven страницу ai-agents-demand-hooks-2026, разделение на «нарративный слой» vs «data-driven слой»)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/documents/research_report.pdf
## [2026-04-14 14:55] [ingest] | Telegram @FounderWoman (Паскина/NUSELF) — дамп 50 постов + 26 медиа (bundled), 3 релевантных сигнала из 50
- source: wiki/sources/2026-04-14-tg-founderwoman-feb-apr-2026.md
- created: none
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (добавлен раздел «Авторы как страховочные каналы в MAX (2026-04-14)» — behavioral-паттерн на примере @FounderWoman, автор завела дубль-канал в MAX из-за сбоев Telegram, не ради миграции)
  - wiki/evolving/content-trends/telegram-native-formats.md (добавлен раздел «Наблюдаемые exemplar-ы в авторских каналах» с разбором erid-нативки Сбера × @FounderWoman (пост #1800, 2026-03-31) — сторителлинг-интеграция через личный pain + рамка расширения ниши + корректная ERID-маркировка)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 2, 'sources': 1}
- touched: 3 pages
- raw: raw/processed/articles/tg_FounderWoman_20260414-134353.md (+ .note.md sibling) + 26 files in raw/processed/media/tg_FounderWoman_* (each with .note.md sibling) — bundled move

## [2026-04-14 14:45] [ingest] | Telegram @ProductsAndStartups (Байрам Аннаков) — дамп 50 сообщений + 39 аттачей
- source: wiki/sources/2026-04-14-tg-products-and-startups-feb-apr-2026.md
- created:
  - wiki/canon/marketing-frameworks/harness-engineering-for-ai-agents.md
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md
  - wiki/evolving-strict/market-data/ai-labor-market-anthropic-2026.md
  - wiki/evolving/content-trends/ai-product-engineer-content-hooks.md
  - wiki/volatile-strict/competitor-news/anthropic-claude-managed-agents-2026-04.md
  - wiki/volatile-strict/competitor-news/anthropic-emotion-vectors-2026-04.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен раздел о верифицированном эмпирическом подкреплении от Байрама Аннакова (onsa.ai 5 человек делают работу 12-15), механизм J-curve, harness-as-a-service ускоряет сжатие окна. Подтезис о преимуществе мелких апгрейдится к confidence: medium.)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлены три новых hook-семейства от Байрама: «harness > prompt > model» с метафорой зеркала, «5 человек делают работу 12-15» как empirical proof-point, «software factory $0.80 4 минуты» как scary-good демо-хук.)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 1, 'evolving': 4, 'evolving-strict': 1, 'volatile-strict': 2, 'sources': 1}
- touched: 10 pages
- raw: raw/in-progress/{articles,video,media}/tg_ProductsAndStartups_* (1 md + 11 mp4 + 28 jpg + 40 .note.md) → raw/processed/{articles,video,media}/

## [2026-04-14 14:45] [ingest] | @Theedinorogblog (Филонов) — дамп 50 сообщений март–апрель 2026 (bundled: +28 jpg +7 mp4)
- source: wiki/sources/2026-04-14-tg-theedinorog-mar-apr-2026.md
- created:
  - wiki/volatile/weekly-digest/edinorog-mar-apr-2026-digest.md
- updated:
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлена секция 7 с 5 свежими RU-медийными proof-points (Medvi/Rork/Alien/Systematika/Ten8), новое hook-семейство «нарратив уже здесь», disclaimer про Medvi)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен блок «RU-специфика регуляторного гэпа (апрель 2026)» с 7 постами из канала: VPN-плата, исключение из реестра, методичка iOS-sandboxing, закон об AI маркировке, предложение Шойтова цензурировать AI. Новый тезис про iOS-привилегию и нишу локальных AI-обёрток)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile': 1, 'evolving': 2, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_Theedinorogblog_20260414-134525.md (+ 28 jpg/.note в raw/processed/media/, 7 mp4/.note в raw/processed/video/)

## [2026-04-14 14:50] [ingest] | Telegram @TorbosovLife — дамп 50 постов (бандл md+46jpg+4mp4)
- source: wiki/sources/2026-04-14-tg-torbosov-life-apr-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-premium-real-estate-q1-2026.md
  - wiki/evolving/content-trends/contrarian-framing-expert-telegram.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен sources back-link на дамп Торбосова как пример длинного экспертного нативного формата)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving-strict': 1, 'evolving': 2, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_TorbosovLife_20260414-120042.md (+ 46 media + 4 video + sidecars)

## [2026-04-14 15:00] [ingest] | Addmeto (Бакунов) — 50 постов Telegram июль 2025 – март 2026 (+47 media)
- source: wiki/sources/2026-04-14-tg-addmeto-jul2025-mar2026.md
- created:
  - wiki/volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1.md
  - wiki/evolving/industry-trends/ai-knowledge-worker-climb-2025-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен раздел «Рыночные proof-points 2025-H2 → 2026-Q1»: DeepSeek $300k training, Codex 2M users, Claude Code $1B ARR, Sky.app «вечер работы» как empirical подтверждение падения барьера; подтезис о tooling-monetization апгрейден до confidence medium)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлено hook-семейство 8 «За несколько часов» (Sky.app кейс как третий empirical proof-point после Байрама и Rork); ссылки на news-кластер)
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (Добавлен раздел «Внешние demand-side proof-points»: Sora2 #1 App Store, Codex 2M, Claude Code $1B как anti-hooks для «я опоздал» и усилители для сегмента B; предостережение не использовать для сегмента C)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile-strict': 1, 'evolving': 4, 'sources': 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_addmeto_20260414-141322.md (+ .note.md + 47 media siblings in raw/processed/media/)

## [2026-04-14 14:45] [ingest] | Telegram @ai_newz — дамп 50 сообщений (4479–4528, bundled: 1 article + 33 media + 11 video)
- source: wiki/sources/2026-04-14-tg-ai-newz-mar-apr-2026.md
- created:
  - wiki/volatile/weekly-digest/ai-industry-news-w11-w15-2026.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile': 1, 'sources': 1}
- touched: 2 pages
- raw: raw/processed/articles/tg_ai_newz_20260414-142552.md (+ 33 raw/processed/media/tg_ai_newz_*.jpg|mp4 + 11 raw/processed/video/tg_ai_newz_*.mp4 + все .note.md siblings)

## [2026-04-14 14:50] [ingest] | Telegram @alexander_visotsky — дамп 50 постов (bundled: article + 31 jpg + 7 mp4 + 1 ogg)
- source: wiki/sources/2026-04-14-tg-alexander-visotsky-mar-apr-2026.md
- created:
  - wiki/evolving/competitor-positioning/business-booster-visotsky.md
  - wiki/evolving/content-trends/visotsky-case-study-structure.md
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md
  - wiki/canon/marketing-frameworks/visotsky-productivity-heuristics.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен Visotsky/Business Booster как четвёртый exemplar жанра expert-founder TG-channel: integrated lead-funnel pattern, ≈2 поста/день, lead magnets mix, FOMO-driven offline event; что GRO может забрать и что не брать; добавлены ссылки на 3 новые страницы visotsky-*)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 4, 'canon': 1, 'sources': 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_alexander_visotsky_20260414-134525.md + 31× media/ + 7× video/ + 1× audio/ (все с .note.md сиблингами; audio также с .audio.mp3 intermediate, transcript НЕ создан — whisper MCP недоступен)

## [2026-04-14 14:45] [ingest] | Telegram @bezsmuzi (Кульгин) — дамп 50 постов 12–14 апреля 2026 (weekly bundle)
- source: wiki/sources/2026-04-14-tg-bezsmuzi-apr-12-14.md
- created:
  - wiki/volatile/weekly-digest/ai-model-releases-2026-w15.md
  - wiki/volatile/raw-notes/ru-platform-access-april-2026.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлены подтверждающий сигнал от @bezsmuzi (Кульгин запустил Telegram→MAX бот) и top-downloads сигнал (9 VPN + MAX #10 в РФ топ-10) с caveat про первоисточник)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлен hook 7 «Куда делись инфобизнесмены WB → ИИ-коучи» (cross-signal от Кульгина 15256) как подтверждение окна + anti-hook-маркер против инфобиз-оборотов)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile': 2, 'evolving': 2, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_bezsmuzi_20260414-140242.md (+ 42 media + 7 video + все .note.md siblings → raw/processed/{media,video}/)

## [2026-04-14 14:55] [ingest] | @boris_again — дамп 50 постов март–апрель 2026 (bundle: md + 36 jpg + 2 mp4)
- source: wiki/sources/2026-04-14-tg-boris-again-mar-apr-2026.md
- created:
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md
  - wiki/evolving/content-trends/short-form-video-algo-retention-2026.md
  - wiki/evolving/industry-trends/ru-vertical-ai-signals-2026.md
- updated:
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлены разделы 8 и 9: hook-family «Claude Code — новый operating mode» (позитивный, из поста 3800) и objection-family «чтобы хорошо вайбкодилось — надо читать код» (балансирующий, из поста 3814). Цейтлин как inferred expert даёт честный двусторонний голос на нарратив solopreneurship)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Новый раздел «Второй независимый practitioner-голос»: Цейтлин как третий источник (после подкаст-инвестора и Байрама Аннакова). Конкретные operational proof-points (iGPU за 4 часа, hr-breaker, any2json) и честный objection-balance. Темп ~40 релизов за 5 недель как фоновый аргумент окна)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile-strict': 1, 'evolving': 4, 'sources': 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_boris_again_20260414-142514.md + raw/processed/media/tg_boris_again_{3798..3847}.jpg (36 files) + raw/processed/video/tg_boris_again_{3801,3816}.mp4 + все .note.md sidecars

## [2026-04-14 14:50] [ingest] | Telegram @bossofyourboss (Табунов) — 50 постов дек 2025 — апр 2026, bundled ingest (1 md + 20 jpg + 4 mp4)
- source: wiki/sources/2026-04-14-tg-bossofyourboss-dec2025-apr2026.md
- created:
  - wiki/canon/marketing-frameworks/retention-benchmarks-b2c.md
  - wiki/canon/marketing-frameworks/funnel-simplicity-principle.md
  - wiki/evolving/content-trends/entertainment-over-pain-framing.md
  - wiki/evolving/content-trends/tabunov-founder-growth-hooks.md
  - wiki/evolving/industry-trends/whoop-retention-case-2026.md
  - wiki/evolving-strict/market-data/app-store-slop-2026.md
  - wiki/volatile-strict/industry-news/ai-tooling-market-news-2026-q1.md
  - wiki/volatile-strict/industry-news/ru-subscription-autocharge-law-2026-03.md
- updated:
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлен раздел 10 «12 тезисов про вайбкодинг» (Табунов) — 4 сильных хука + cross-links на tabunov-founder-growth-hooks и retention-benchmarks-b2c; source добавлен во front-matter)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 2, 'evolving': 3, 'evolving-strict': 1, 'volatile-strict': 2, 'sources': 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_bossofyourboss_20260414-140207.md (+.note.md) + raw/processed/media/tg_bossofyourboss_*.{jpg,mp4} (21 files +.note.md siblings) + raw/processed/video/tg_bossofyourboss_*.mp4 (3 files +.note.md siblings)

## [2026-04-14 14:45] [ingest] | Telegram @breakingtrends — дамп 50 сообщений (11 дней, 12 релевантных, bundled ingest)
- source: wiki/sources/2026-04-14-tg-breakingtrends-digest.md
- created:
  - wiki/volatile/weekly-digest/2026-04-14-breakingtrends-marketing-ai-news.md
  - wiki/evolving-strict/market-data/alice-ai-usage-breakdown-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+секция «Новостные сигналы про labor-market reshaping»: IBM -30% офисных ролей, 44% зумеров саботируют ИИ, Claude token-limits перестраивают workday — промежуточный тезис про corporate labor reshaping поднят до conf:medium (прогноз 3-летнего окна остаётся conf:low))
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (+секция «Новые hooks из новостных сигналов»: hook «AI по лимитам токенов» (для сегментов D и B), hook «IBM -30%» fear-based (осторожно для B и GRO предприниматели), anti-hook «не конкурировать с Алисой в поиске/объяснении» со ссылкой на новую alice-ai-usage-breakdown страницу)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile': 1, 'evolving-strict': 1, 'evolving': 2, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_breakingtrends_20260414-115851.md (+ .note.md) + 40 jpg + 10 mp4 (+ note.md siblings) в raw/processed/media и raw/processed/video

## [2026-04-14 14:45] [ingest] | Telegram @businesssecrets — дамп 50 постов дек 2025 (news-tracker, 48/50 нерелевантны)
- source: wiki/sources/2026-04-14-tg-businesssecrets-dec2025-dump.md
- created:
  - wiki/volatile-strict/industry-news/ru-ai-displacement-narrative-dec2025.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile-strict': 1, 'sources': 1}
- touched: 2 pages
- raw: raw/processed/articles/tg_businesssecrets_20260414-113925.md + 50×raw/processed/media/tg_businesssecrets_{43576..43625}.jpg (bundled, все с .note.md siblings)

## [2026-04-14 14:42] [ingest] | @cgevent bundled ingest — 50 сообщений + 45 медиа-вложений (8–14 апр 2026)
- source: wiki/sources/2026-04-14-tg-cgevent-apr08-14-2026.md
- created:
  - wiki/volatile/weekly-digest/tg-cgevent-ai-cg-apr08-14-2026.md
  - wiki/evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile': 1, 'evolving': 1, 'sources': 1}
- touched: 3 pages
- raw: raw/processed/articles/tg_cgevent_20260414-142831.md (+ .note.md sibling) + raw/processed/media/tg_cgevent_153{66,68,70,74,76-81,84,88-90,95},154{04,05,08,13,14}.jpg (20 files + notes) + raw/processed/video/tg_cgevent_153{67,69,71,72,75,82,83,86,87,92,94,96-99},154{00-03,06,07,09,10-12}.{mp4,mov} (25 files + notes) — 90 files total moved in-progress→processed

## [2026-04-14 14:55] [ingest] | Telegram @community_tech — Михаил Воронин (фев–апр 2026, 50 постов + 17 медиа)
- source: wiki/sources/2026-04-14-tg-community-tech-voronin-feb-apr-2026.md
- created:
  - wiki/volatile/weekly-digest/voronin-community-tech-feb-apr-2026.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile': 1, 'sources': 1}
- touched: 2 pages
- raw: raw/processed/articles/tg_community_tech_20260414-141304.md + 17 bundled media across media/audio/video

## [2026-04-14 14:50] [ingest] | Cossa.ru ТГ-дайджест 3–14 апреля 2026 (bundled: 50 msg + 49 media)
- source: wiki/sources/2026-04-14-tg-cossaru-apr-3-14.md
- created:
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md
  - wiki/evolving-strict/market-data/global-marketing-outlook-2026.md
  - wiki/evolving-strict/market-data/ru-smb-digital-ad-spend-2026.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлен раздел «Инфраструктурная подготовка рекламного рынка (2026-04-08 → 2026-04-14)»: BidFox 1000+ каналов, PromoPult боты, Telega.in первая perf-реклама, caveat на «100M пользователей»; добавлены cross-links на tg-cossaru source и ru-telegram-blocking-max-migration-2026)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен exemplar «Ишь, Миш! × девелопер Академический» (2026-04-08): hyperlocal story-driven video, 90 062 просмотра / 1055 реакций, цикл 2–3 дня, перенос паттерна на GRO (среда вместо продукта))
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md (Добавлен раздел «Сигналы со стороны SMB-сегмента (2026-04-14)» со cross-link на ru-smb-digital-ad-spend-2026, интерпретацией доли SMB в общем приросте рынка, inline-маркерами на 5 ключевых числах АРИР)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'evolving-strict': 3, 'sources': 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_cossaru_20260414-115813.md (+.note.md) + raw/processed/media/tg_cossaru_*.jpg[.note.md] (43 jpg + 43 notes) + raw/processed/video/tg_cossaru_*.mp4[.note.md] (6 mp4 + 6 notes)

## [2026-04-14 15:00] [ingest] | Telegram @dnative — digest 7497–7546 (trend-tracking, bundled 33 files)
- source: wiki/sources/2026-04-14-tg-dnative-digest-7497-7546.md
- created:
  - wiki/evolving-strict/market-data/wciom-ad-perception-russia-2026.md
  - wiki/evolving/content-trends/vk-shopsy-creator-playbook.md
  - wiki/evolving/content-trends/youtube-thumbnail-face-trend.md
  - wiki/volatile-strict/industry-news/russian-social-platforms-digest-2026-03-04.md
  - wiki/volatile-strict/competitor-news/mave-stream-media-platform-launch-2026.md
  - wiki/evolving/industry-trends/max-messenger-author-rejection-2026.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлен третий публично задокументированный сигнал отторжения MAX (dnative, 2026-04-02, этическая рамка «цифрового сопротивления») + кейс провала розыгрыша официального MAX-канала на 1-й день рождения (2026-04-06, 3600+ участников, бот сбойнул, 5 термокружек) с механическим разбором (button-under-post vs original-post only))
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (Добавлен апдейт 2026-04-14: Пиархаб конференция «Telegram — всё?» 1 апреля, ВЦИОМ 2028-survey подтверждает 88% спрос на ненавязчивость, корректировка рекомендации №5 про MAX с учётом creator-rejection)
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md (Добавлен раздел «Потребительский слой — ВЦИОМ апрель 2026» с 4 inline-strict цифрами: топ-источник реклама на маркетплейсах 43%, 72% ежедневного контакта в соцсетях, парадокс доверия 52%/49%, creator-commerce 44% хотят покупки в один клик)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'evolving-strict': 2, 'volatile-strict': 2, 'sources': 1, 'updated-pages': 3}
- touched: 10 pages
- raw: raw/processed/articles/tg_dnative_20260414-115727.md (+32 attached children in media/video/audio, all with sidecar .note.md)

## [2026-04-14 14:50] [ingest] | Telegram @egoshin_kedprof — дамп 50 постов янв-апр 2026 (bundled: 1 md + 45 jpg + 4 mp4)
- source: wiki/sources/2026-04-14-tg-egoshin-kedprof.md
- created:
  - wiki/canon/marketing-frameworks/egoshin-ai-adoption-ladder.md
  - wiki/canon/marketing-frameworks/four-paths-it-market-future.md
  - wiki/evolving/industry-trends/b2b-ai-adoption-fte-kpi-2026.md
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md
  - wiki/evolving/industry-trends/ru-ai-national-strategy-2026.md
  - wiki/volatile/weekly-digest/davos-2026-ai-speakers-digest.md
- updated:
  - wiki/canon/product-knowledge/gro-team.md (First-party подтверждение co-founder статуса Егошина от него самого (пост-визитка канала 2026-03-15); расширенные биографические якоря (Яндекс/МФТИ/МИСиС клиенты, Рейтинг Рунета 15/1 место, НИУ ВШЭ стратегический партнёр, IBS 7+ лет, лекции МФТИ/МГИМО/МИСиС, «Россия-страна возможностей»); Шапран Андрей как бывший коммерческий директор KedProf и partnership-сигнал; cross-links на две новые рамки Егошина)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Новый раздел «FTE-reframe и Карпатый job map (2026-04-14)»: добавлены FTE как корпоративная метрика из SnowBase и карта Карпатого по 342 профессиям (8-9/10 у разработчиков/юристов/аналитиков, 10/10 у мед. транскрибаторов); direction of travel теперь подкреплён ещё двумя independent сигналами)
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (Новый раздел «Authored hooks от Константина Егошина»: 4 готовых hook-а с сегментацией и GRO-angles — «Команда на стероидах», «Стратегия когнитивной бережливости», «Атомный козырь России», диагностический «Лестница адаптации» (5% организаций решили ступень 1))
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 3, 'evolving': 5, 'volatile': 1, 'sources': 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_egoshin_kedprof_20260414-141358.md + 45 media/*.jpg + 4 video/*.mp4 (все с .note.md sidecars)

## [2026-04-14 14:50] [ingest] | tg @fomichevkirill feb-apr 2026 (bundle: 1 md + 37 jpg + 3 pdf)
- source: wiki/sources/2026-04-14-tg-fomichevkirill-feb-apr-2026.md
- created:
  - wiki/canon/marketing-frameworks/llm-market-analysis-prompt.md
- updated:
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (+hook-family #11 «ИИ как тьютор, а не решебник» с атрибуцией Фомичёву (confidence: low), 4 готовые формулировки + anti-hook про «ответ за секунду», cross-link к tutor-mode industry pattern (Gemini/Alisa))
  - wiki/evolving/competitor-positioning/max-messenger.md (+4-й автор с cold-standby MAX-зеркалом (Фомичёв, пост 2353) — паттерн укрепляется, 4 независимых автора за фев–апр 2026; +дополнительный раздел про Яндекс Мессенджер как «русский Slack» team-comms сигнал)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 1, 'evolving': 2, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_fomichevkirill_20260414-140321.md + 37 media + 3 documents (+ sidecar .note.md-ы)

## [2026-04-14 14:50] [ingest] | Forbes Russia daily digest 13–14 апр 2026 (50 постов + 29 attachments, бандл)
- source: wiki/sources/2026-04-14-tg-forbesrussia-apr-13-14.md
- created:
  - wiki/volatile-strict/industry-news/mts-hrtech-multiagent-launch-2026.md
  - wiki/volatile-strict/industry-news/dzen-national-info-platform-2026.md
  - wiki/volatile-strict/industry-news/vtb-intellect-ai-investing-2026.md
  - wiki/evolving/content-trends/forbes-russia-native-ad-pattern-2026.md
  - wiki/evolving-strict/market-data/ru-digital-economy-snapshot-2026-04.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (+ раздел «Federal-tier издатель: Forbes Russia с MAX-зеркалом» — Forbes публично указывает max.ru/forbes в alt-channels footer, качественно новая ступень паттерна (federal-tier media, не indie))
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (+ раздел «Smoke-сигнал ослабления давления (2026-04-14)» — Bloomberg+Forbes сигнал о возможном откате регуляторного давления на Telegram из-за рейтинга Путина; добавлен как параллельный сценарий, не supersession)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile-strict': 3, 'evolving': 2, 'evolving-strict': 1, 'sources': 1, 'evolving-updated': 2}
- touched: 7 pages
- raw: raw/processed/articles/tg_forbesrussia_20260414-114809.md + 29 children (28 jpg → raw/processed/media/, 1 mp4 → raw/processed/video/)

## [2026-04-14 14:42] [ingest] | Telegram @grebenukm (Гребенюк / Аномалия) — дамп 50 постов 2026-03-18..04-13
- source: wiki/sources/2026-04-14-tg-grebenukm-mar-apr-2026.md
- created:
  - wiki/evolving/competitor-positioning/grebenyuk-anomaly-community.md
  - wiki/canon/marketing-frameworks/demand-first-mvp-castdev.md
  - wiki/canon/marketing-frameworks/grebenyuk-4x-markup-rule.md
  - wiki/canon/marketing-frameworks/four-zones-of-genius-hendricks.md
  - wiki/evolving/content-trends/urgency-window-launch-playbook.md
  - wiki/evolving/content-trends/anti-authority-positioning-hook.md
  - wiki/evolving/content-trends/enough-vs-growth-narrative.md
  - wiki/evolving/industry-trends/ru-smb-mentor-community-market-2026.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (+ Активный grower — Grebenyuk (12к→15к за 5 дней, публично тормошит MAX PR-отдел, authority-figure signal встречный dnative-rejection-паттерну); +source Grebenyuk; +link grebenyuk-anomaly-community)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 3, 'evolving': 5, 'sources': 1, 'updated_evolving': 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_grebenukm_20260414-113526.md + 23 children (20 media, 2 video, 1 audio; 3 media/av read failed: whisper MCP unavailable — uvx not installed)

## [2026-04-15 00:00] [ingest] | Гуринович делится — TG дамп 50 постов янв–мар 2026 (Эдуард Гуринович, Forbes 30 under 30)
- source: wiki/sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026.md
- created:
  - wiki/evolving/content-trends/ai-flattery-dark-pattern.md
  - wiki/evolving/content-trends/ru-business-tg-content-drift-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен 4-й verified голос (Гуринович): трафик как структурное ограничение эпохи вайбкодинга (+15-20%/год), рекомендация не-программистам фокусироваться на привлечении клиентов вместо вайбкодинга, расширение ЦА тезиса до маркетологов/трафик-менеджеров)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлено hook-family #12 «Вайбкодинг как подростковый секс + инфляция навыка» (Гуринович): снятие FOMO через эмпатичный рефрейм, метафора 90-х про компоненты ПК, hooks про трафик и 0.001% затрат на прототип, anti-hooks про «освой вайбкодинг за неделю»)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен exemplar «Основатели.Doc × Ракета» (пост 875): founder-story YouTube-фильм → TG ретрансляция → offline demand spike у бутика и сторонних reseller-ов. Первый proof-point уровня «виральный founder-story в RU TG способен двигать реальные retail-точки». Скрин переписки с реселлером как independent свидетельство)
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (Добавлен anti-hook «ваш ИИ вам льстит» (пост 888, cross-link на новую страницу ai-flattery-dark-pattern) + новый hook «virtual AI persona как отдельная content-профессия» (пост 876, Гуринович публично запускает продюсирование виртуального персонажа))
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 6, 'sources': 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_gurinovich_shares_20260414-134629.md + 26 children (24 media + 2 video)

## [2026-04-15 12:55] [ingest] | @hh_ru_official — дамп 50 постов + 28 медиа (март–апрель 2026): HRTech market + Галочка mascot-campaign + federal-brand MAX cross-promo
- source: wiki/sources/2026-04-14-tg-hh-ru-official-mar-apr-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-hrtech-market-2023-2025.md
  - wiki/evolving/content-trends/hh-ru-galochka-mascot-campaign.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен новый exemplar @hh_ru_official: первый federal-brand serialised mascot-кампания (в дополнение к автор-каналам Visotsky/FounderWoman/Cossa/Gurinovich). Показывает, что маскот-сериал — отдельный формат, не в таблице Пиархаб)
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлен третий качественный уровень паттерна MAX-поддержки: federal-tier потребительский бренд (hh.ru) с систематическим cross-promo через подпись-CTA начиная 2026-03-30. Lightweight формат, не требует контент-миграции. Hypothesis: синхронизированный onset с infrastructure roll-out (BidFox/Telega.in))
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'evolving-strict': 1, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_hh_ru_official_20260414-112925.md + 23 media + 5 video children (28 children total; videos transcribed: 0 of 5, read failed — whisper MCP and faster-whisper unavailable in current environment, captions cover semantic content)

## [2026-04-15 13:15] [ingest] | Telegram @howtomake10x (Крылов, ex-CEO Gett) — март–апрель 2026, 50 постов + 43 медиа bundle
- source: wiki/sources/2026-04-14-tg-howtomake10x-mar-apr-2026.md
- created:
  - wiki/evolving/product-reception/gro-productivity-energy-angle.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (5-й автор-сигнал: Крылов (@howtomake10x) — hedging-but-actively-migrating под-паттерн с blocking-fear CTA, exclusive-контентом в MAX и публичным backlash от аудитории; типология MAX-migration расширена до 5 под-паттернов)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (2-й независимый голос (Крылов) + 4 новых paradox-хука: «слабый сотрудник ест управленческую энергию», «я был причиной того, что всё падало», paired 5-признаков self-diagnostic, «первые 30 минут после плохой новости»; confidence паттерна повышается)
  - wiki/evolving/content-trends/visotsky-case-study-structure.md (2-й независимый автор (Крылов) применяет тот же 4-элементный паттерн на 3 кейсах (Starbucks/Schultz, Danny Meyer/Union Square, US-realtor remembrance); отличия: легендарные западные герои vs named clients, low-risk вариант; 3-й под-тип формата — механика-под-прикрытием-истории)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (новое hook-family #13: Bruch & Ghoshal 10%/90% quantitative anchor для productivity angle + AI-resume-slop reverse-hook («AI убил резюме как сигнал, выжили — human provenance»); первое verified эмпирическое число для GRO productivity-коммуникации)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 4, 'sources': 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_howtomake10x_20260414-140923.md + 43 children (37 media/.jpg+mp4, 4 video/.mp4, 1 audio/.ogg; audio 1493 whisper MCP unreachable в сессии, .audio.mp3 ffmpeg-sibling сохранён для повторной попытки)

## [2026-04-14 15:30] [ingest] | HR_kak_delat (bundle: 1 primary + 35 media) — извлечён только labor-market snapshot Q1 2026
- source: wiki/sources/2026-04-14-tg-hr-kak-delat-feb-apr-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving-strict': 1, 'sources': 1}
- touched: 2 pages
- raw: raw/processed/articles/tg_hr_kak_delat_20260414-112628.md + 35 children

## [2026-04-15 00:00] [ingest] | Telegram @hutzp (Женя Давыдов, SETTERS) — дамп 50 сообщений + 47 jpg + 1 mp4
- source: wiki/sources/2026-04-14-hutzp-telegram-20260402-0414.md
- created:
  - wiki/canon/marketing-frameworks/narrative-as-brand-currency.md
  - wiki/canon/marketing-frameworks/organize-to-value-mckinsey.md
  - wiki/evolving/industry-trends/russian-cultural-code-branding-2026.md
  - wiki/evolving/industry-trends/future-of-work-trends-2026.md
  - wiki/evolving/competitor-positioning/settersgroup-ecosystem.md
  - wiki/evolving/content-trends/telegram-author-channel-patterns.md
- updated:
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md (добавлен раздел Practical examples с тремя реальными ad-marked постами (HUGO erid 2SDnjcAJjPt, REB8T erid 2W5zFHTWxSM, Т-Бизнес erid 2SDnjeb1Vpv), новый source в front-matter)
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (добавлено практическое наблюдение о маркировке в @hutzp как подтверждение совместимости натива и compliance, новый source в front-matter)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 2, 'canon-strict': 1, 'evolving': 4, 'sources': 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_hutzp_20260414-140146.md + 48 children (47 jpg to raw/processed/media/, 1 mp4 to raw/processed/video/)

## [2026-04-15 13:40] [ingest] | Telegram @incrussiamedia bundle 8–14 апреля 2026 (primary + 48 jpg + 2 mp4)
- source: wiki/sources/2026-04-15-tg-incrussiamedia-apr-8-14-2026.md
- created:
  - wiki/volatile-strict/competitor-news/canva-acquires-simtheory-ortto-2026-04.md
  - wiki/volatile-strict/competitor-news/openai-acquires-hiro-finance-2026-04.md
  - wiki/volatile-strict/competitor-news/microsoft-copilot-agents-2026-04.md
  - wiki/evolving-strict/competitor-metrics/canva-2026.md
  - wiki/canon/marketing-frameworks/benetton-toscani-provocative-advertising.md
- updated:
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md (Добавлен блок «Mainstream validation (2026-04-15)»: три апрельских события (Canva, Microsoft, OpenAI) как массовое подтверждение agent-first тезиса, замечание про enterprise vs consumer split)
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md (Добавлен раздел «6. M&A-консолидация стека — апрельская волна 2026» с разбором трёх сделок как параллельной волны к стандартам webmcp/MPP)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile-strict': 3, 'evolving-strict': 1, 'canon': 1, 'evolving': 2, 'sources': 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_incrussiamedia_20260414-114004.md + 50 children (48 jpg media + 2 mp4 video)

## [2026-04-15 13:49] [ingest] | Kommersant TG digest 13–14 апреля 2026 — Дзен-regulator apdate + премиум-срез + beauty-vertical
- source: wiki/sources/2026-04-14-tg-kommersant-apr-13-14.md
- created:
  - wiki/evolving-strict/market-data/ru-beauty-health-ecommerce-q1-2026.md
- updated:
  - wiki/volatile-strict/industry-news/dzen-national-info-platform-2026.md (Kommersant confirmation + новые конкретные детали: VK-презентация как первоисточник, законопроект в мае 2026, оператор на 5 лет, аудитория СМИ −30–70% с 2022, Дзен = 80% трафика на сайты СМИ; две открытые позиции закрыты)
  - wiki/evolving-strict/market-data/ru-premium-real-estate-q1-2026.md (Добавлен официальный aggregate-срез Kommersant: Q1 2026 Москва −54% продаж премиум-новостроек, 109 сделок; confidence базового факта повышен до high (два независимых источника — expert+редакционный); front-matter остался medium из-за operational Whitewill/Dubai разделов)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving-strict': 2, 'volatile-strict': 1, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_kommersant_20260414-115034.md + 29 children (25 media + 4 video)

## [2026-04-14 15:00] [ingest] | Telegram @kwork_kwork — 50 постов (bundle: primary + 50 media, май 2025 → апрель 2026)
- source: wiki/sources/2026-04-14-tg-kwork-may2025-apr2026.md
- created: none
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (+kwork_kwork exemplar: low-frequency editorial бренд-канал маркетплейса как противоположный полюс hh.ru маскот-кампании, сравнительная таблица, 5 рубрик чередования, «делегирование» как сквозной нарратив, editorial-ретранслятор как формат отсутствующий в таблице Пиархаб)
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (+параллельный сигнал: Kwork открыл ИИ-рубрики в каталоге услуг (первый product-шаг фриланс-платформы РФ под ИИ), практическое применение hooks для сегментов A/B/D, anti-hook «не цитировать Kwork как конкурента»)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+product-signal зрелости: Kwork как 4-й независимый demand-side голос (после подкаста, Субботина, Гуриновича) — не апгрейд confidence, но добавляет transaction-based proof-point к narrative-based сигналам)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_kwork_kwork_20260414-113145.md + 50 children (raw/processed/media/tg_kwork_kwork_*.jpg) + .note.md sidecar

## [2026-04-14 16:30] [ingest] | @moibiz Telegram digest 2026-04-04..04-14 (bundled: 1 md + 47 media children)
- source: wiki/sources/2026-04-14-tg-moibiz-apr-04-14.md
- created:
  - wiki/volatile-strict/industry-news/yandex-alice-ai-visibility-tool-2026-04.md
  - wiki/evolving-strict/market-data/ru-ecommerce-platformization-reshetnikov-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (+секция «Гос-канал подтверждает multi-platform реальность» с цитатой из @moibiz 7355 и новым датапоинтом TenChat в списке разрешённых площадок)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile-strict': 1, 'evolving-strict': 1, 'evolving': 1, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_moibiz_20260414-115337.md + 47 children (39 jpg + 8 mp4) → processed/

## [2026-04-15 14:50] [ingest] | Telegram @mspiridonov — дамп 50 постов + 21 медиа (Максим Спиридонов, verified expert)
- source: wiki/sources/2026-04-14-tg-mspiridonov-mar-apr-2026.md
- created:
  - wiki/canon/marketing-frameworks/external-validation-trap.md
  - wiki/canon/marketing-frameworks/virtual-advisory-board-ai.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+Carta slide 2016–2025 (solo-founded US стартапы 18%→36%, 1-founder=2-founder, 54 601 startups) как прямой количественный source; новый раздел с таблицей и inline [conf:high, src:2026-04-07] маркерами)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (+hook-family #10 (Carta 36% solo + «installed robotic workforce» + Luna bootique objection), #11 (Michelin трап/Buffett-тест anti-validation), #12 (виртуальный борд как готовый hook))
  - wiki/evolving-strict/market-data/ai-labor-market-anthropic-2026.md (+Upwork 2026 skills report cross-reference: +109% AI-компетенции, +329% AI-video, +178% процесс-встройка и т.д., все с inline [conf:medium, src:2026-04-01]; таблица + marketing-интерпретация)
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md (+новый раздел 7 «Эмпирические маркеры — AI-бутик Luna (Andon Labs)»: 00K, SF, найм/подрядчики/кредит автономно + характерные LLM-патологии; новый objection-proof-point)
  - wiki/canon/marketing-frameworks/native-advertising.md (+новый раздел «Extreme-native» с кейсом Nutella в Артемиде II: +516% за сутки, +910% за 2 дня, зеро-стоимостный brand-placement как крайняя точка спектра нативности и теоретическая формулировка commercial-intent-skepticism)
  - wiki/evolving/customer-feedback/gro-app-store-reviews.md (+cross-link use case «брейншторм» с формализованным паттерном виртуального борда (virtual-advisory-board-ai), который связывает стихийное наблюдение с более широким рыночным паттерном)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 3, 'evolving': 3, 'evolving-strict': 1, 'sources': 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_mspiridonov_20260414-133438.md + 21 children (15 media jpg + 6 video mp4)

## [2026-04-14 14:30] [ingest] | Telegram @neuraldvig — 50 постов за 7 дней (AI-news daily-feed, bundle: 1 md + 35 jpg + 15 mp4)
- source: wiki/sources/2026-04-14-tg-neuraldvig-apr-7-14.md
- created:
  - wiki/evolving/content-trends/ai-news-channel-prompt-packs.md
  - wiki/volatile/weekly-digest/ai-news-digest-2026-04-07-14.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (добавлен @neuraldvig как exemplar daily-feed AI-news/memes/prompt-packs жанра; новый раздел с композицией feed (≈60% news + 25% memes + 12% prompt-packs + 3–4% ads), положение в таксономии Пиархаб, что GRO может/не может брать; sources и «Связанные страницы» расширены)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 2, 'volatile': 1, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_neuraldvig_20260414-141651.md + 50 children (35 media/jpg + 15 video/mp4, all claimed, none read per-child — visual/meme-only, decision documented in source page)

## [2026-04-14 11:53] [ingest] | Telegram @ofd24 — фискально-налоговый дайджест (нерелевантно, audit only)
- source: wiki/sources/2026-04-14-tg-ofd24-fiscal-regulation-digest.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: raw/processed/articles/tg_ofd24_20260414-115318.md + 12 children (11 media/*.jpg + 1 documents/tg_ofd24_6471.pdf)

## [2026-04-15 14:45] [ingest] | Telegram @olegcloser (Олег Шевелев) — bundled дамп 50 постов + 46 медиа (Q1 2026 SMB sales signals)
- source: wiki/sources/2026-04-14-olegcloser-telegram-dump.md
- created:
  - wiki/canon/marketing-frameworks/business-reality-show-format.md
  - wiki/evolving/content-trends/sales-ai-narrative-hooks-2026.md
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (+6-й автор-якорь (Олег Шевелев @olegcloser) с уникальным под-паттерном «tech-troubleshooting cold-standby» — самый репутационно-безопасный вариант MAX-CTA, готовый template для GRO)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 2, 'evolving': 3, 'sources': 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_olegcloser_20260414-134643.md + 46 children (2 audio, 22 video, 22 media) → processed. Note: 2 audio children marked (read failed: whisper MCP unavailable — uvx not on PATH); bundle overall success via primary caption-proxy.

## [2026-04-14 16:00] [ingest] | ОПОРА РОССИИ — TG-дайджест 6990–7039 (bundle: 1 md + 42 media)
- source: wiki/sources/2026-04-14-tg-opora-russia-week-7.md
- created:
  - wiki/evolving-strict/market-data/ru-youth-entrepreneurs-2026.md
  - wiki/evolving-strict/market-data/ru-self-employed-segments-2026.md
  - wiki/evolving/industry-trends/telegram-business-channel-risk-ru-2026.md
  - wiki/volatile-strict/competitor-news/yandex-direct-opora-promo-2026-04.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (добавлен раздел "Внешние количественные подтверждения сегментов (2026-04-14)": сегмент 2 усиливается данными о молодых ИП, сегмент 3 распадается на цифровую и офлайн модель самозанятых; +3 cross-link на новые market-data + ru-ai-telegram-audience-segments)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 1, 'evolving': 1, 'evolving-strict': 2, 'volatile-strict': 1, 'sources': 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_opora_russia_20260414-115317.md + 42 children (40 jpg + 2 mov in raw/processed/media|video/)

## [2026-04-14 15:00] [ingest] | Перегудов / Whizz — 50 постов TG дек.2025–апр.2026 (bundled с 9 media)
- source: wiki/sources/2026-04-14-peregudov-telegram-dec25-apr26.md
- created:
  - wiki/evolving/industry-trends/ai-native-company-architecture-2026.md
  - wiki/evolving/industry-trends/software-moat-erosion-2026.md
  - wiki/evolving/industry-trends/agentic-commerce-stripe-2026.md
  - wiki/evolving/content-trends/aeo-geo-llm-search-optimization-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+секция «Практик-свидетель: Перегудов / Whizz» — хронология конверсии «не уверен → 100% должен попробовать» за 6 недель (2026-01-21 → 2026-03-04), апгрейд confidence «барьер упал» до high на personal-experience уровне, апгрейд «структурное преимущество мелких» до medium (3 независимых голоса), добавлен новый механизм «коллапс цикла жизни SaaS» через cross-link на software-moat-erosion-2026)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (+hook-family #13 «MOAT больше не в софте, он в дистрибуции» (Перегудов) с короткими формулировками, траекторией-хуком, quote-card референсом через Navall Ravikant meme (media/394), связками с 3 сегментами ЦА, и anti-hooks из постов 390 (anti-AI-генерация) и 412 (LLM-лесть))
  - wiki/evolving/content-trends/telegram-native-formats.md (+секция «Exemplar: Михаил Перегудов (@peregudov)» — структурные характеристики авторского founder-канала, паттерны #реклама-интеграций (5 платных + 3 рекомендательных за 50 постов), quote-card визуал (media/394), мем-иллюстрация к longread (media/392), self-imposed discipline «посты изначально в 2× длиннее», anti-паттерны (longread про личное, политика, 3+ реклам в неделю))
- superseded: none
- sensitive flag: ⚠ media/tg_peregudov_401.jpg (скриншот админки Whizz) содержит PII: имена и email ~12 сотрудников. В слоях не цитируется дословно, только агрегированно (Humans(67)/Agents(2), столбцы, 6 городов). PII осталась только в исходном raw и обезличенно упомянута в source-странице как audit
- layer-touched: {'evolving': 7, 'sources': 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_peregudov_20260414-140932.md + 9 children (raw/processed/media/tg_peregudov_{365,367,382,383,384,385,392,394,401}.jpg)

## [2026-04-15 04:30] [ingest] | Антон Петроченков (@petrochenkow) — Telegram bundle март–апрель 2026 (50 постов + 26 медиа)
- source: wiki/sources/2026-04-14-tg-petrochenkow-mar-apr-2026.md
- created:
  - wiki/canon/marketing-frameworks/cross-industry-pattern-borrowing.md
  - wiki/canon/marketing-frameworks/marketing-audit-protocol.md
  - wiki/canon/marketing-frameworks/cpa-calculator-pre-launch-roi.md
  - wiki/canon/marketing-frameworks/qualitative-adjectives-ad-copy.md
  - wiki/canon/marketing-frameworks/hyperseg-funnel-replication.md
  - wiki/canon/marketing-frameworks/refused-customer-interview.md
  - wiki/canon/marketing-frameworks/marketer-hiring-questions.md
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
  - wiki/evolving/industry-trends/ai-marketing-limits-2026.md
  - wiki/evolving-strict/market-data/ru-private-dental-clinics-2025-2026.md
  - wiki/evolving-strict/market-data/ru-psychology-services-2025-2026.md
  - wiki/evolving-strict/market-data/ru-b2b-industrial-2025-2026.md
  - wiki/volatile-strict/industry-news/openai-ads-chatgpt-2026-03.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (+practitioner-сигнал: Petrochenkov CPL 80-150 ₽/подп (2026-03-26, conf:medium), brand bookings до конца марта (2026-03-12), анонс конференции «5000+ подп по 62 ₽ в бизнес-тематиках» (2026-04-13, conf:low), маркетинговое следствие про CPL-окно для GRO-теста в Q2 2026)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (+hook-family #14 «курс про ИИ продаёт курс про обучение продавать ИИ» (Petrochenkov 2026-04-01), готовый anti-hook для GRO как защита от инфобизнес-симулякров; cross-link на ai-marketing-limits-2026)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 7, 'evolving': 2, 'evolving-strict': 3, 'volatile-strict': 1, 'sources': 1, 'updated_evolving': 2}
- touched: 14 pages
- raw: raw/processed/articles/tg_petrochenkow_20260414-115450.md + 26 children (22 jpg media + 3 mp4 video + 1 xlsx documents)

## [2026-04-14 14:50] [ingest] | Telegram @portnyaginlive (50 постов, ред.-формат, bundle +50 media) — 5 new / 4 updated
- source: wiki/sources/2026-04-14-tg-portnyaginlive-mar-apr-2026.md
- created:
  - wiki/volatile-strict/industry-news/ru-vpn-metering-proposal-2026-04.md
  - wiki/volatile-strict/industry-news/global-ai-news-digest-2026-04-07.md
  - wiki/canon/marketing-frameworks/petscom-unit-economics-failure.md
  - wiki/canon/marketing-frameworks/demin-international-expansion-5-pillars.md
  - wiki/evolving/content-trends/portnyagin-founder-channel-patterns.md
- updated:
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (Добавлен 5-й вектор давления — VPN-metering proposal (Portnyagin 11165, 2026-04-01, confidence:low). Был 4 параллельных давления, стал 5. Новая характеристика рычага — первый механизм, который бьёт по конечному пользователю, а не по бизнесу. Обновлены план верификации, контр-сигналы и cross-links.)
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md (Добавлен раздел 8 — Weekly AI news digest 2026-04-07 как подтверждение нарратива в RU-предпринимательском Telegram'е. 4 пункта из 10 прямо резонируют со страницей: Claude Code agentic mode, Anthropic Computer Use, Figma AI agents, ByteDance Deerflow 2.0. Мета-наблюдение: когда крупные RU founder-каналы weekly-агрегируют agent-first новости, нарратив уже не early-adopter.)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (Добавлен раздел 6 — внешний резонанс: Goryachev case studies из @portnyaginlive 11180/11181 подтверждают нарратив Шевелева 'собственник в режиме выживания'. Два case: Деафон (compensation shock ₽200K→₽30K → recovery ×3) и Простомебель (115+ leads за 2 мес по ₽5000/lead). Все numeric claims confidence:low (промо-пост), но рамка совпадает слово-в-слово — это повышает confidence самого нарратива.)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен exemplar-раздел Portnyagin (@portnyaginlive) — founder-channel в редакторском режиме. Три нативных формата: weekly AI news digest как rubric, 2-day reveal affiliate promo, meme-news format. Контраст editorial vs personal-authorship voice. Cross-link на portnyagin-founder-channel-patterns.)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 2, 'evolving': 4, 'volatile-strict': 2, 'sources': 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_portnyaginlive_20260414-131858.md + 50 children (34 media + 16 video, videos не транскрибированы)

## [2026-04-15 14:45] [ingest] | Колганов @psilonsk — Telegram management-wisdom дамп (6 недель, 50 сообщений + 32 обложки)
- source: wiki/sources/2026-04-14-psilonsk-management-tg-dump.md
- created:
  - wiki/evolving/content-trends/psilonsk-management-hooks-bank.md
  - wiki/evolving/content-trends/psilonsk-channel-patterns.md
  - wiki/evolving/content-trends/ai-control-dystopia-counter-hook.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлен седьмой author-сигнал — compliance-with-irony (Колганов @psilonsk, пост 5506 от 2026-04-01): саркастическое продвижение MAX-канала с 4-кратной рамкой «не побоюсь этого слова мессенджер МАХ» + mock-опечатка «ХАМ». Единственный из семи паттернов, который не воспроизводим коммерчески. Обновлены sources и updated.)
  - wiki/evolving/industry-trends/max-messenger-author-rejection-2026.md (Добавлен раздел «Contrast с compliance-with-irony (Колганов 2026-04-01)» — третья позиция в спектре между dnative-rejection и sincere compliance; дополнена таблица с тремя политиками; обновлены sources и Связанные страницы.)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 5, 'sources': 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_psilonsk_20260414-140008.md + 32 media children (tg_psilonsk_5466..5524.jpg) → processed

## [2026-04-14 17:00] [ingest] | @rb_ru — Telegram-дайджест RB 1–14 апреля 2026 (50 постов, 48 медиа bundle)
- source: wiki/sources/2026-04-14-rb-ru-tg-digest-2026-04-01-14.md
- created:
  - wiki/canon/marketing-frameworks/ankusheva-ai-implementation-triad.md
  - wiki/evolving-strict/market-data/ru-business-ai-adoption-2026.md
  - wiki/volatile-strict/industry-news/ru-vpn-telegram-restrictions-2026-04.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (+раздел Внешний сигнал из B2B-медиа (rb.ru): формула «в Макс хотят идти не все», обвал Telegram 2026-04-10, рестораны 10–20 тыс ₽/день)
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (+раздел Voice-AI как структурный anti-hook: 61/17/15 разбивка, дифференциация text-AI vs voice-AI, anti-hook для всех 4 сегментов)
  - wiki/canon/target-audience/gro-segments.md (+раздел Внешние количественные подтверждения career-сегмента: 41% готовы менять работу, RAND 44–54 потерянных рабочих дня, productivity tax angle для «100% Энергии»)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+раздел Корпоративная сторона тезиса (rb.ru): 71% корп.инвестиции в AI, 45% top priority, 65% малого B2B-marketing провал; +Anti-pattern voice-AI (61% rejection))
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 2, 'evolving': 3, 'evolving-strict': 1, 'volatile-strict': 1, 'sources': 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_rb_ru_20260414-114745.md + 48 children (42 jpg + 6 mp4)

## [2026-04-14 15:30] [ingest] | РБК (@rbc_news) — TG news-дайджест 50 постов 13–14 апр 2026 (bundle +21 media, 3/50 релевантных)
- source: wiki/sources/2026-04-14-rbc-news-telegram-digest-apr13-14.md
- created: none
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (+два новых exemplar-раздела: (1) co-branded editorial integrations у федеральных СМИ (Sber×РБК ГигаНаука, РБК×ProductStar Мини-MBA) — рубричный vs разовый натив, co-brand как визуал-mechanic; (2) live-stream selling в недвижимости как новый под-формат, отсутствующий в исходной таблице Пиархаб, параллель с китайским social commerce, импликации для GRO (часовой live-стрим разбора тренировочного дня))
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (+апдейт 2026-04-14 про co-branded editorial integrations у федеральных СМИ: Sber×РБК ГигаНаука (рубричный натив с GigaChat), РБК×ProductStar Мини-MBA (co-brand только на визуале). Валидация тезиса «рынок более рациональным, больше данных» через long-form партнёрства. Второй независимый tier-1 сигнал, что нарратив «ИИ для руководителей» стал мейнстримом.)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 2, 'sources': 1}
- touched: 3 pages
- raw: raw/processed/articles/tg_rbc_news_20260414-115115.md + 21 children (15 media jpg + 6 video mp4), видео не транскрибированы (irrelevant/redundant — все видео относятся к нерелевантным сюжетам или полностью покрыты текстом поста)

## [2026-04-14 14:42] [ingest] | Telegram @recruiter_live — career digest + HH 2026 labor market (bundle: 1 .md + 2 PDF + 2 mp4 + 27 jpg)
- source: wiki/sources/2026-04-14-tg-recruiter-live-career-digest.md
- created:
  - wiki/evolving-strict/market-data/ru-labor-market-hh-2026.md
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (Добавлен раздел «HH 2026: транзитная зона карьеристов» с количественным подтверждением сегмента 1 (52% меняют профессию, 51% нет роста, 42% выгорание, 40% нет карьерных опций) и backlink на новую страницу evolving-strict/market-data/ru-labor-market-hh-2026)
- superseded: none
- sensitive flag: почтовые контакты авторов (ti@tihragency.ru, ratina@retailtech.ru) и ТГ-хэндлы — оставлены только в raw/processed/, в wiki не перенесены
- layer-touched: {'evolving-strict': 1, 'evolving': 2, 'canon': 1, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_recruiter_live_20260414-112124.md + 31 children (27 jpg в media/, 2 mp4 в video/, 2 pdf в documents/), все с .note.md sidecar'ом primary-файла

## [2026-04-14 14:42] [ingest] | Telegram @rff_channel (HR, 50 постов март-апрель 2026) — bundled, off-domain, 3 узких сигнала
- source: wiki/sources/2026-04-14-tg-rff-channel-mar-apr-2026.md
- created:
  - wiki/evolving/competitor-positioning/qooqa-ai-recruiter.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (+большая секция «Niche-vertical channel playbook» на примере RFF: 8 элементов playbook (рубрики/UGC-prompt/long-form интервью/co-branded research/спутниковая сеть/hub-post/sponsored content/serial кросс-промо), что GRO забрать и что НЕ брать)
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md (+четвёртый практический пример complient native-ad из HR-вертикали (RFF пост 4350: ЭКОПСИ × Яндекс Практикум, erid 2W5zFGy3CUh, через биржу telega.in); добавляет модель «брокер вместо прямого контракта», «плашка О рекламодателе вместо ИНН в теле», вывод что practice устоялась across verticals)
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (+секция «Qooqa как proof-point для возражения AI-агенты пока хайп»: hooks по 3 сегментам (Любопытные/Амбициозные/Продвинутые), anti-pattern «не позиционировать GRO как Qooqa», обоснование почему именно Qooqa (российский / sponsored с erid / co-marketing с ЭКОПСИ / fully autonomous))
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'canon-strict': 1, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_rff_channel_20260414-112920.md + 44 children (33 jpg + 5 mp4 + 6 pdf, все с .note.md sidecars)

## [2026-04-15 19:12] [ingest] | Telegram @rybakovigor (бандл 50 постов + 47 медиа, март–апрель 2026)
- source: wiki/sources/2026-04-14-tg-rybakovigor-march-april-2026.md
- created:
  - wiki/canon/marketing-frameworks/collective-intelligence-meeting-protocol.md
  - wiki/canon/marketing-frameworks/environment-architecture-entrepreneur-safety.md
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен exemplar «Эквиум 9-image carousel» (Рыбаков msg 6475–6483) — детальный разбор структуры (9 страниц, watermark на каждой, page-numbering, template-карточки founders с Forbes-номерами, factual proof через named cases, soft CTA на ассоциацию), 5 переиспользуемых приёмов для GRO + 3 anti-pattern предостережения)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 2, 'evolving': 1, 'evolving_updated': 1, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_rybakovigor_20260414-120554.md + 47 children (33 media jpg + 14 video mp4)

## [2026-04-14 14:45] [ingest] | Telegram @selfworkru (Самозанятые.рф) — 50 постов (bundled: 46 jpg + 1 mp4)
- source: wiki/sources/2026-04-14-tg-selfworkru-mar-apr-2026.md
- created: none
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (+@selfworkru exemplar: carousel-heavy бренд-канал нишевого B2C-сервиса с коин-маскотом, двухцветной семантической палитрой (насыщенно-синий=эмоция, светло-голубой=explainer), Q&A rubric «Вы спрашиваете — мы отвечаем», pair cat-memes формат, пасхальный seasonal-quiz. Закрывает третью нишу в corpus между минималистичным Kwork и дорогим маскот-сериалом hh.ru)
  - wiki/evolving/competitor-positioning/max-messenger.md (+Нишевый B2C слой exemplar-ов: @selfworkru пост 2979 (2026-03-31) — MAX как backup в шутливом первоапрельском disclaimer-посте, MAX второй в alt-channels списке после VK. Четвёртый наблюдаемый слой (indie / federal media / federal B2C / нишевый B2C) нормализации MAX как backup)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 2, 'sources': 1}
- touched: 3 pages
- raw: raw/processed/articles/tg_selfworkru_20260414-113513.md + 47 children (46 jpg media + 1 mp4 video, all to processed/)

## [2026-04-15 16:25] [ingest] | Telegram @sergei_ivanov_efko — CEO ЭФКО как 8-й MAX-endorser (bundle: md + 45 media children)
- source: wiki/sources/2026-04-14-tg-sergei-ivanov-efko-mar-apr-2026.md
- created: none
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлен 8-й под-паттерн Industrialist-founder sincere endorser на примере @sergei_ivanov_efko (CEO ЭФКО): самая высокая в корпусе плотность footer-CTA в личном канале (~32% из 50 постов), дословный sincere positive endorsement MAX от C-level FMCG-индустриалиста (2026-03-31), authority-трансфер двусторонний; конфиденциальность: author-single-voice требует подтверждения)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 1, 'sources': 1}
- touched: 2 pages
- raw: raw/processed/articles/tg_sergei_ivanov_efko_20260414-131909.md + 45 children (18 video + 18 media + 4 audio + 5 documents) + .note.md sidecar → all processed/

## [2026-04-14 16:30] [ingest] | Соколовский — подкаст-driven author-канал Telegram (bundled: md + 43 media, 27 дней)
- source: wiki/sources/2026-04-14-tg-sokolay-mar-apr-2026.md
- created:
  - wiki/evolving/content-trends/podcast-driven-author-channel-patterns.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен exemplar @sokolay с таблицей 3 паттернов native-ad (carousel/affiliate/editorial), anti-pattern affiliate без ad-marking, предупреждение о credibility-требовании для 40% лайфстайла)
  - wiki/evolving/content-trends/telegram-author-channel-patterns.md (Добавлен раздел «Подкатегории author-blogger формата»: A=agency/founder-driven (@hutzp), B=подкаст-driven (@sokolay), сравнение контент-миксов, impl для выбора формата GRO (default A до накопления легитимности))
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_sokolay_20260414-122006.md + 43 children (17 jpg + 26 mp4)

## [2026-04-14 14:50] [ingest] | Telegram @solokumi (Kumar & Solo) — 50 постов Nov 2025 – Apr 2026 (bundled: 1 md + 3 img + 1 zip)
- source: wiki/sources/2026-04-14-tg-solokumi-nov2025-apr2026.md
- created:
  - wiki/canon/marketing-frameworks/andromeda-creative-framework-2026.md
  - wiki/canon/marketing-frameworks/ai-video-production-pipeline.md
  - wiki/canon/marketing-frameworks/multi-agent-marketing-org-principles.md
  - wiki/canon/marketing-frameworks/claude-md-structure-marketing.md
  - wiki/evolving/content-trends/ai-video-tools-stack-2026.md
  - wiki/evolving/content-trends/ai-static-creative-templates-2026.md
  - wiki/evolving/industry-trends/ai-native-marketer-skillset-2026.md
  - wiki/evolving/competitor-positioning/vibecoding-stack-ecosystem-2026.md
  - wiki/evolving-strict/product-metrics/refocus-germany-2026-growth.md
- updated:
  - wiki/volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1.md (Добавлены 3 timeline-записи: Claude Skills public release Kumar & Solo (2026-03-23), `/loop` + Remote Tasks в Claude Code (2026-03…04), VIBECON как первая русскоязычная vibecoding-конференция (2026-04-02). Дополнительный source в front-matter, backlink на vibecoding-stack-ecosystem-2026)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлены два новых раздела: Kumar & Solo 4-stage content funnel (привлечение → контентная воронка → прогрев → продажи, бенчмарк ER 15–20%) и ManyChat welcome-серия с октября 2025 (+50% лидов в Refocus DE). Дополнительный source в front-matter, три backlink'а)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 4, 'evolving': 4, 'evolving-strict': 1, 'volatile-strict': 1, 'sources': 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_solokumi_20260414-135928.md + 4 children (tg_solokumi_380.jpg, tg_solokumi_388.zip, tg_solokumi_391.jpg, tg_solokumi_396.jpg) with note sidecars

## [2026-04-14 15:00] [ingest] | Telegram @startupoftheday (Горный) — дамп марта–апреля 2026 (bundle: 1 primary + 13 media children)
- source: wiki/sources/2026-04-14-tg-startupoftheday-mar-apr-2026.md
- created:
  - wiki/canon/marketing-frameworks/mvp-definition-gorny.md
  - wiki/volatile/weekly-digest/startupoftheday-mar-apr-2026.md
- updated:
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлен hook-family #15 (Горный): эмоциональный apex «ЗА ОДИН, СУКА, ЗАПРОС», Death By Clawd как interactive CTA, RevenueCat thesis как argument-from-authority третьего уровня)
  - wiki/evolving/industry-trends/software-moat-erosion-2026.md (Добавлен третий независимый голос (Горный, посты 5005–5006): RevenueCat thesis + DataDog/CrowdStrike mid-cap SaaS переоценка, перевод тезиса в публично-рыночную плоскость)
  - wiki/evolving/industry-trends/ru-vertical-ai-signals-2026.md (Добавлены сигналы 4–6 (Yandex B2B Tech грант + R77/Noumy/GO2AI, NovaVoice, AiAcademy/Чиббис с 2.2M views). Шесть сигналов, два независимых источника (Цейтлин + Горный))
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен раздел «Anti-pattern-заметки Горного»: DOOH dashboard-fetishism, April Fools anti-tradition, Product Hunt cynicism, наблюдение за native-ads separation-of-concerns в expert-канале)
  - wiki/canon/product-knowledge/gro-team.md (Новый раздел «Network-признаки — ShareAI × Лапшина»: верификация инсайдерского статуса Лапшиной в русскоязычной AI/VC сцене через гостевое интервью в закрытом клубе Горного)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 2, 'evolving': 4, 'volatile': 1, 'sources': 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_startupoftheday_20260414-113752.md + 13 children (media: 12, video: 1)

## [2026-04-14 14:55] [ingest] | Telegram @stodnevka2 (Петросян) — март–апр 2026, 50 постов + 12 медиа (bundle)
- source: wiki/sources/2026-04-14-tg-stodnevka2-mar-apr-2026.md
- created: none
- updated:
  - wiki/evolving/industry-trends/max-messenger-author-rejection-2026.md (добавлен девятый под-паттерн «Петросян — resigned dubbing + offplatform pivot»: публичное dubbing в MAX без рост-амбиций, фокус на рассылке + Substack, quantitative confirmation (Substack 100 subs за месяц, open-rate почти сравнялась с TG))
  - wiki/evolving/competitor-positioning/max-messenger.md (добавлен раздел «Девятый автор-сигнал: Армен Петросян (@stodnevka2) — resigned dubbing + offplatform pivot» с полной поведенческой траекторией март–апрель 2026, расширена таблица под-паттернов до 9 строк, quantitative-якорь под newsletter-pivot)
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (добавлен апдейт «quantitative-якорь под ценность собственных каналов»: первое в wiki наблюдение Substack 100 subs за месяц + open-rate proxy + business-impact signal «худший март за 18 лет» у established RU tier-2 автора)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_stodnevka2_20260414-140600.md + 12 children in raw/processed/media/ (all with .note.md sidecars)

## [2026-04-14 14:45] [ingest] | Telegram @studentsuper (SuperJob Старт) — дамп мар–апр 2026 (1 primary + 46 children)
- source: wiki/sources/2026-04-14-tg-studentsuper-mar-apr-2026.md
- created:
  - wiki/volatile-strict/industry-news/superjob-ai-agents-marketplace-2026-04.md
  - wiki/volatile/weekly-digest/tg-studentsuper-mar-apr-2026.md
- updated:
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (+SuperJob AI-agents marketplace (2026-04-07) как свежий proof-point «агент = сотрудник» в одной неделе с МТС HRTech — используется как objection-closer для Любопытных/Амбициозных)
  - wiki/evolving/content-trends/telegram-native-formats.md (+новая секция «Corporate мем-видео + card-offer паттерн (SuperJob Старт)» + «Corporate UGC-hiring как market-signal (SuperJob, 2026-03-24)» — прикладной телеграм-пример для early-career ЦА и признак нормализации managed-UGC)
- superseded: none
- sensitive flag: none
- layer-touched: {'volatile-strict': 1, 'volatile': 1, 'evolving': 2, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_studentsuper_20260414-113210.md + 46 children (22 video + 24 media)

## [2026-04-14 14:55] [ingest] | Telegram @t_jrnl (Тинькофф Журнал) — apr 2026 (bundle: 1 primary + 49 jpg + 1 mp4)
- source: wiki/sources/2026-04-14-tg-t-jrnl-apr2026.md
- created:
  - wiki/evolving-strict/market-data/ai-driven-layoffs-2025-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (добавлен раздел «Глобальный корпоративный контекст» с жёсткими цифрами Amazon/MS/Сбер (10/7/20%) и 47% РФ крупняка — качественная narrative-рамка РФ-рынка труда теперь имеет количественные ориентиры со стороны корпоративных решений; обновлены sources и связанные страницы)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (тезис «2026–2027 фаза: крупные выжимают эффективность из существующих» усилен жёсткими цифрами 10/7/20% AI-layoffs — намерение стало реализацией; sources расширен на t_jrnl apr2026)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (добавлены Hook 7 «10/7/20% AI-layoffs — готовься заранее» (awareness) и Hook 8 «Сильные/слабые стороны на собеседовании» (consideration/decision) — оба из Т-Ж apr2026 с anti-hook правилом «не продавать на страхе»; обновлена таблица маппинга hooks→воронка и связанные страницы)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving-strict': 1, 'evolving': 3, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_t_jrnl_20260414-114926.md + 50 children (49 media/jpg + 1 video/mp4, все sidecars перемещены)

## [2026-04-15 01:00] [ingest] | Telegram @techno_yandex — bundle 50 сообщений (текст + 46 медиа) за 31.03 – 14.04.2026
- source: wiki/sources/2026-04-14-tg-techno-yandex-mar-apr-2026.md
- created:
  - wiki/evolving/content-trends/ai-in-pr-workflows-2026.md
  - wiki/evolving-strict/market-data/ru-ai-search-interest-2025-2026.md
  - wiki/volatile-strict/industry-news/openai-industrial-policy-2026-04.md
- updated:
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md (Second-source attestation от @techno_yandex: Claude Mythos — добавлено про 27-летнюю OpenBSD-дыру, 16-летний FFmpeg-баг, sandbox-escape эксперимент и клиентов Glasswing (Apple/Google/Microsoft); Gemma 4 — добавлен агентный фрейминг; Muse Spark — добавлена формулировка про топ-5 и экономичность токенов; sources расширен)
  - wiki/volatile-strict/industry-news/yandex-alice-ai-visibility-tool-2026-04.md (Cross-link на две новые страницы (ai-in-pr-workflows-2026, ru-ai-search-interest-2025-2026) как параллельные сигналы от того же Яндекса в ту же неделю)
  - wiki/evolving-strict/market-data/alice-ai-usage-breakdown-2026.md (Cross-link на ru-ai-search-interest-2025-2026 (динамический срез от того же Яндекса, контекстуализирует breakdown))
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 1, 'evolving-strict': 2, 'volatile-strict': 3, 'sources': 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_techno_yandex_20260414-142456.md + 46 children (37 jpg + 9 mp4) to processed

## [2026-04-14 14:45] [ingest] | techsparks (Себрант) — 50 постов март–апрель 2026 (bundle: +46 JPG + 1 PDF)
- source: wiki/sources/2026-04-14-tg-techsparks-mar-apr-2026.md
- created:
  - wiki/evolving/content-trends/sebrant-cognitive-exoskeleton-hooks.md
  - wiki/evolving-strict/market-data/us-ai-job-risk-tufts-2026.md
  - wiki/volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026.md
  - wiki/volatile-strict/industry-news/eu-chatgpt-vlose-dsa-2026.md
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-ai-audience-gap-2026.md (Добавлена тройная валидация тезиса о «разрыве двух миров»: Karpathy (Business Insider) + Forbes (Josipa Majic) + Sebrant (@techsparks 5532) — three-way independent convergence на один наблюдаемый факт)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлено экспертное подтверждение тезиса от Себранта: интроверты первыми под ударом, AI-native стартапы роем против старожилов, когнитивный экзоскелет. Второй независимый источник рядом с исходным неверифицированным спикером)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлена hook-family #16: «AI-код vs человеческий код — parity, not inferiority» от Себранта на базе Claude Mythos Preview, снимающая объекцию «AI-код ненадёжный»)
  - wiki/volatile-strict/industry-news/openai-industrial-policy-2026-04.md (Добавлен критический read Себранта: идеи не новы (у Альтмана с 2021), документ — часть IPO-прелюдии, параллельная покупка TBPN подкаста как media-control ход. Мета-урок редакторского pattern для GRO content)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 4, 'evolving-strict': 1, 'volatile-strict': 3, 'sources': 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_techsparks_20260414-142117.md + 47 children (1 PDF + 46 JPG)

## [2026-04-15 14:45] [ingest] | Ринат Алиев (@telega_Rinata) — TG-дамп founder-coach personal-brand канала (50 постов + 28 медиа bundled)
- source: wiki/sources/2026-04-14-tg-telega-rinata-mar-apr-2026.md
- created: none
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен exemplar-раздел «@telega_Rinata (Ринат Алиев) — founder-coach personal brand с цепочкой UTM-лендингов»: cadence 1.25/день, 40% промо-плотность, UTM-per-post паттерн, cross-platform funnel, user-generated casting, шаблон «разбор интервью CEO». Источник добавлен в sources:)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлен Hook-family #17 «От каких экспертов я уже отказался из-за ИИ» (Ринат Алиев, conf:low) — personal-level эмоциональный hook, дополняющий data-driven hooks #5/#16b. С готовой формулировкой, anti-hook caveat и правилом атрибуции.)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 2, 'sources': 1}
- touched: 3 pages
- raw: raw/processed/articles/tg_telega_Rinata_20260414-140646.md + 28 bundled children (23 media, 1 audio, 4 video)

## [2026-04-15 21:20] [ingest] | Telegram @temno — Morejnis digest mar–apr 2026 (50 posts bundle, recovery)
- source: wiki/sources/2026-04-14-tg-temno-moreynis-mar-apr-2026.md
- created:
  - wiki/evolving/industry-trends/ai-value-migration-2026.md
  - wiki/canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis.md
  - wiki/evolving/content-trends/moreynis-hand-drawn-meme-format.md
  - wiki/evolving/industry-trends/b2b-ai-adoption-fte-kpi-2026.md
- updated:
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (добавлен Морейнис как параллельный голос: hook-семейства «judgment > productivity» (7779) и «делай то, чего не хотят» (7742); источник включён в sources front-matter)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (добавлен Морейнис как параллельный голос: «сжатие vs расширение» (7741), «арбитраж с ИИ» (7757), структурное преимущество мелких; источник включён в sources)
  - wiki/evolving/content-trends/telegram-native-formats.md (добавлен Морейнис / @temno как exemplar хэнд-дроу формата с cross-link на moreynis-hand-drawn-meme-format)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 1, 'evolving': 6, 'sources': 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_temno_20260414-131359.md + 50 children in raw/processed/media/ (recovery: primary stuck in pending, children stranded in in-progress/media from prior interrupted run; wiki-side artifacts already existed)

## [2026-04-14 11:30] [ingest] | @typicalcompany — TG-дамп TYPICAL management-консалтинга (bundle: primary + 25 children)
- source: wiki/sources/2026-04-14-tg-typicalcompany-nov25-mar26.md
- created:
  - wiki/evolving/competitor-positioning/typical-company.md
  - wiki/evolving/industry-trends/ai-for-managers-2025-2026.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен exemplar TYPICAL: community-first playbook с #хэштеговой навигацией серий, 5 форматов (hashtag-оглавление, визуальные карусели когнитивных искажений, raw-audio intro-лекция, вторичный reframed repost, iPhone screenshot testimonial), 6 заимствуемых паттернов + 4 anti-pattern'а (зелёная палитра collision, community-first модель, slow-burn launch, punchy voice))
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (Добавлен раздел «AI снимает рутину информации» hook от TYPICAL (5 hooks для карьериста-руководителя, 2 anti-hook'а), cross-refs на typical-company/ai-for-managers, обновлены sources и «Связанные материалы»)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 4, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_typicalcompany_20260414-111235.md + 25 children (21 media/jpg, 1 audio/ogg, 1 video/mp4, 1 media/mp4, 1 documents/avif)

## [2026-04-14 14:45] [ingest] | vcnews @vcnews — дайджест 50 постов + 42 медиа (10–14 апреля 2026)
- source: wiki/sources/2026-04-14-tg-vcnews-apr-10-14.md
- created:
  - wiki/evolving-strict/market-data/ru-corporate-ai-assistants-2026.md
  - wiki/volatile/weekly-digest/2026-04-10-14-vcnews-signals.md
- updated:
  - wiki/evolving/industry-trends/ru-ai-audience-gap-2026.md (новый раздел «Дрейф инфраструктурного барьера — апрель 2026» — VPN crackdown, Шадаев, Дуров, слух об ослаблении TG-блока; дрейф состава сегмента заблокированных)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (новый раздел «Frontier-вендоры сдвигаются на enterprise» — OpenAI $852B дрейф, Claude Mythos unprecedented конкуренция, Meta AI-twin Цукерберга, OpenAI→Hiro финтех)
  - wiki/evolving/competitor-positioning/max-messenger.md (новый раздел «Keyword-detection controversy (2026-04-13)» — 9-й штрих к trust gap, ограничения для чувствительных B2B-форматов)
  - wiki/volatile-strict/industry-news/ru-vpn-telegram-restrictions-2026-04.md (новый раздел с 4 vcnews-сигналами второй волны (RKS Global, Шадаев публичная позиция, Дуров антицензурный протокол, слух Forbes/Bloomberg))
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving-strict': 1, 'volatile': 1, 'evolving': 3, 'volatile-strict': 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_vcnews_20260414-113635.md + 42 children (39 jpg in media/ + 3 mp4 in video/) → status: processed

## [2026-04-14 14:45] [ingest] | Якуба @vyakuba — дамп 50 TG-постов март–апрель 2026 (bundle: 1 md + 34 media)
- source: wiki/sources/2026-04-14-tg-vyakuba-mar-apr-2026.md
- created:
  - wiki/evolving/competitor-positioning/vyakuba-sales-training.md
  - wiki/evolving/content-trends/ru-sales-infobiz-content-patterns.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+cross-vertical voice Якубы (пост 6685): «дешевеет не человек, дешевеют простые действия» — не-tech голос из инфобиз-мира, валидирует центральный подтезис; добавлен в sources[])
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'sources': 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_vyakuba_20260414-134550.md + 34 children (14 media + 20 video)

## [2026-04-14 16:30] [ingest] | WTF_HR — годовая выборка HR-канала, ноябрь 2024 — октябрь 2025 (bundle: 1 md + 24 jpg + 1 pdf)
- source: wiki/sources/2026-04-14-tg-wtf-hr-nov24-oct25.md
- created:
  - wiki/canon/marketing-frameworks/karpathy-ai-60s-mainframe-analogy.md
  - wiki/evolving/content-trends/wtf-hr-ai-skeptic-hooks.md
- updated:
  - wiki/sources/2026-04-14-tg-wtf-hr-nov24-oct25.md (новая source-страница bundle (primary + 25 children))
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md (+WTF_HR три эмпирические data-точки (Klarna reversal, SalesForce +4%/+6%, «сначала сокращают, потом внедряют»); cross-link на Karpathy-аналогию)
  - wiki/evolving/industry-trends/ai-knowledge-worker-climb-2025-2026.md (+Сигналы 4 и 5 (junior-apprenticeship revival, конец прикладного IT-образования, вайб-консалтинг) из WTF_HR)
  - wiki/evolving/industry-trends/future-of-work-trends-2026.md (+Движение 7: долгосрочная futurology WTF_HR «две касты работников» + unicorn of one + мидл-менеджеры на замену + KPI как условие диплома)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+Скептический контрапункт WTF_HR: 3 точки поддержки (unicorn of one, мидл-менеджеры на замене, две касты) + 4 ограничения (Klarna, SalesForce, «сначала сокращают», сырые агенты))
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (+Объекция #4 «Корпорации крутят ИИ-пиар, но ROI не виден» с парированием)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 1, 'evolving': 5, 'sources': 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_wtf_hr_20260414-110741.md + 25 children (24 jpg в media/ + 1 pdf в documents/)

## [2026-04-15 22:40] [ingest] | Telegram @your_pet_project Табунова — 10 AI-solopreneur кейсов + 3 canon-фреймворка + updates к 5 существующим страницам
- source: wiki/sources/2026-04-14-tg-your-pet-project-jan-apr2026.md
- created:
  - wiki/evolving/content-trends/your-pet-project-channel-hooks.md
  - wiki/volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026.md
  - wiki/canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage.md
  - wiki/canon/marketing-frameworks/tabunov-landing-anatomy.md
  - wiki/canon/marketing-frameworks/tabunov-onboarding-principles.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+operational quantitative anchor: 10 case studies (Medvi $401M/2чел, Lovable $200M ARR, Wave AI $7M ARR соло); 2–5x ускорение time-to-$10K MRR (6 нед vs 12+ мес в 2022); agent-vs-SaaS arbitrage как operational механизм; Medvi balancing note (cautionary tale с FDA/NYT/deepfakes); confidence качественной части поднят до medium)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (+hook family 5b («40 клиентов по $250», «50 клиентов — это подъезд»), case-anchored proof-points от Медви/Lovable/Phoebe/Sleek/Lancer, empirical knockout counter для скептических ответов)
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md (+narrative correction от Табунова: реальные юзкейсы OpenClaw работают плохо (контент=нейрослоп, PM хуже человека, обзвоны видно робот), вирусность = distribution win через WhatsApp/Telegram, не capability win; OCR обложки репо подтверждает 12+ каналов интеграции; следствие для GRO — не позиционировать как agent-coach преждевременно)
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (+Табунов founder-practitioner signal: paid-traffic permanence thesis («актив, который не заблокируешь»), real-world execution через MAX-дублирование .ru аудитории, пятый тип источника в конвергенции на выводе (медиа/Forbes/гос/исследование/практик))
  - wiki/canon/marketing-frameworks/retention-benchmarks-b2c.md (+второй Табунов-источник (@your_pet_project пост 575): subscription retention >90% м/м как «bar of excellence» порог (aspirational target сверх baseline 75%), Day-30 >20% подтверждён consistency между двумя каналами; cross-links на новые tabunov-фреймворки)
- superseded: none
- sensitive flag: none
- layer-touched: {'canon': 4, 'evolving': 4, 'volatile-strict': 1, 'sources': 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_your_pet_project_20260414-133409.md + 17 children (16 media jpg/mp4 + 1 audio sidecar)

## [2026-04-14 12:59] [ingest] | vc.ru/hr — опрос Talantix об автоматизации подбора (нерелевантный источник, audit only)
- source: wiki/sources/2026-04-14-vcru-talantix-hr-automation-survey.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: raw/processed/articles/web_vc.ru_hr_2816230-avtomatizatsiya-podbora-personala_ab987f4c.md (+ .note.md sibling); irrelevant source, no layer pages created

## [2026-04-15 22:57] [ingest] | vc.ru/hr advertorial за Garmony AI — RU-native-шаблон #2 + HR-tech AI landscape
- source: wiki/sources/2026-04-14-vcru-garmony-top10-hr-ai-advertorial.md
- created:
  - wiki/evolving/content-trends/vcru-top10-advertorial-pattern-2026.md
  - wiki/evolving/industry-trends/ru-hr-tech-ai-landscape-2026.md
- updated:
  - wiki/canon/marketing-frameworks/native-advertising.md (добавлена секция «Два наблюдаемых шаблона B2B/B2C-native-размещения в 2026 (RU)» с cross-links на Forbes и vc.ru паттерны, обновлён список связанных страниц и sources)
  - wiki/evolving/content-trends/forbes-russia-native-ad-pattern-2026.md (добавлена секция «Сиблинг-шаблон на другой площадке» со сравнением с vc.ru-паттерном, обновлён список связанных страниц)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 2, 'canon': 1, 'sources': 1}
- touched: 5 pages
- raw: raw/processed/articles/web_vc.ru_hr_2816700-top-10-ii-instrumentov-dlya-hr-i-rekrutinga_c0e1f311.md

## [2026-04-14 13:05] [ingest] | vc.ru/hr — ТОП-6 HRM (irrelevant, audit-only)
- source: wiki/sources/2026-04-14-vc-ru-top-6-hrm-hiring.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: raw/processed/articles/web_vc.ru_hr_2818762-top-6-hrm-sistem-dlya-effektivnogo-najma_34fd4e8e.md (+ .note.md sibling), irrelevant source

## [2026-04-14 15:05] [ingest] | vc.ru/hr — анонимный соискатель «рынок труда 2026, игра в кальмара часть 2»
- source: wiki/sources/2026-04-14-vc-ru-hr-labor-market-opinion.md
- created:
  - wiki/evolving/industry-trends/ru-job-seeker-experience-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (Добавлен раздел «Голос соискателя» — третий voice (job-seeker-side) к уже существующим recruiter-side и corporate-side narrative)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Добавлен Hook 9 «Это не ты плохой соискатель. Это система сломалась» — empathy-first awareness hook, предшествующий всем остальным hook по последовательности потребления; анти-паттерн к прямому «готовься заранее»)
  - wiki/canon/target-audience/gro-segments.md (К блоку внешних сигналов для сегмента 1 «карьеристы» добавлен тезис об обязательной empathy-first ступени перед actionable-контентом (обоснование — третий голос соискателя из vc.ru))
  - wiki/evolving-strict/market-data/ai-driven-layoffs-2025-2026.md (Добавлен cross-link на новую страницу ru-job-seeker-experience-2026 как корроборация того, что corporate-side нарратив (Amazon/MS/Сбер) дошёл до самой аудитории в её собственных словах)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'canon': 1, 'evolving-strict': 1, 'sources': 1}
- touched: 6 pages
- raw: raw/processed/articles/web_vc.ru_hr_2864515-rynok-truda-v-rossii-problemy-i-vyzovy-dlya-soisk_b4e5a54d.md (+ .note.md sibling)

## [2026-04-15 00:00] [ingest] | vc.ru/hr/2866962 — второй advertorial за Garmony AI (ИИ-инструменты для HR 2026)
- source: wiki/sources/2026-04-14-vcru-garmony-ii-instrumenty-hr-advertorial.md
- created: none
- updated:
  - wiki/evolving/content-trends/vcru-top10-advertorial-pattern-2026.md (Добавлен второй референс-кейс; observed pattern → confirmed recurring pattern; секция A/B-ротации hook-статистики)
  - wiki/evolving/industry-trends/ru-hr-tech-ai-landscape-2026.md (Второй advertorial от того же промотёра добавлен в sources; подтверждение устойчивости ценовой таблицы; явная пометка «не независимая верификация»)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 2, 'sources': 1}
- touched: 3 pages
- raw: raw/processed/articles/web_vc.ru_hr_2866962-ii-instrumenty-dla-hr-i-rekrutinga_aeacf30d.md (+ .note.md sidecar)

## [2026-04-15 14:50] [ingest] | [enrich] transcript 3428 (Panov/Neiry) for @hutzp bundle
- source: wiki/sources/2026-04-14-hutzp-telegram-20260402-0414.md
- created: none
- updated:
  - wiki/sources/2026-04-14-hutzp-telegram-20260402-0414.md (Added full transcript of video 3428, reclassified 40% as relevant, updated Метаданные and Факты и цифры)
  - wiki/evolving/industry-trends/russian-cultural-code-branding-2026.md (Added Panov's 3 components of Russian cultural code + Russian engineering school narrative as second data point)
  - wiki/evolving/industry-trends/future-of-work-trends-2026.md (Added section 8: Panov AI→neurotech prognosis (15yr horizon) + happiness-by-subscription hook for GRO)
  - wiki/evolving/content-trends/telegram-author-channel-patterns.md (Enriched Friends-of-mine rubric with actual transcript structure: 8-topic blitz, 5:51 runtime, high-density format)
  - wiki/evolving/competitor-positioning/settersgroup-ecosystem.md (Enriched Panov profile with interview content: cultural code definition, business philosophy, AI prognosis)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 4, 'sources': 1}
- touched: 5 pages
- raw: no raw moves (enrich mode: transcript sidecar already in raw/processed/video/)

## [2026-04-15 16:30] [ingest] | [enrich] olegcloser podcasts 2234/2238 — whisper transcripts
- source: wiki/sources/2026-04-14-olegcloser-telegram-dump.md
- created: none
- updated:
  - wiki/sources/2026-04-14-olegcloser-telegram-dump.md (+transcript summaries for 2234/2238, updated audio section and key ideas)
  - wiki/evolving/content-trends/sales-ai-narrative-hooks-2026.md (+diagnostic frameworks from transcripts (checklist, buy-from-yourself test, investment fear cycle))
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (+transcript detail for expert diagnostic section (concrete tools checklist, investment fear mechanism, pain convergence across revenue scales))
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+investment job JTBD from transcript 2238, lead magnet adaptation)
  - wiki/canon/marketing-frameworks/business-reality-show-format.md (+companion podcast content as retention mechanism between reality show launches)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving': 2, 'canon': 2}
- touched: 5 pages
- raw: no raw moves (enrich mode — files already in raw/processed/audio/)

## [2026-04-15 12:00] [ingest] | enrich | rb_ru digest — transcript 46048 (Surf Coffee)
- source: wiki/sources/2026-04-14-rb-ru-tg-digest-2026-04-01-14.md
- created: none
- updated:
  - wiki/sources/2026-04-14-rb-ru-tg-digest-2026-04-01-14.md (Добавлена транскрипция видео 46048 (Мотти/Surf Coffee), обновлены секции медиа-вложений и экспертных мнений)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: No raw moves (enrich mode, files already in raw/processed/)

## [2026-04-15 22:00] [ingest] | ENRICH @rbc_news bundle — +6 video transcripts, 147484 adds copywriting-референс
- source: wiki/sources/2026-04-14-rbc-news-telegram-digest-apr13-14.md
- created: none
- updated:
  - wiki/sources/2026-04-14-rbc-news-telegram-digest-apr13-14.md (+Транскрипты медиа section (6 videos), updated media table, transcript policy)
  - wiki/evolving/content-trends/telegram-native-formats.md (+rhetorical framing detail из видео-транскрипта 147484 к секции Sber x RБК ГигаНаука)
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (+Mass-media copywriting-референс section: Sber x РБК ГигаНаука 3 заимствуемых приёма + mainstream priming signal)
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (+enrich transcript detail к Sber x РБК entry (hero-метафора, dual-hook, open-loop))
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'sources': 1}
- touched: 4 pages
- raw: No raw moves (enrich mode: files already in raw/processed/video/)

## [2026-04-15 12:00] [ingest] | [enrich] | tg_forbesrussia 94870.mp4 transcript (irrelevant)
- source: wiki/sources/2026-04-14-tg-forbesrussia-apr-13-14.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-forbesrussia-apr-13-14.md (enrich: добавлена секция Транскрипты медиа с расшифровкой видео 94870, обновлена таблица медиа-вложений)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode)

## [2026-04-15 07:15] [ingest] | [enrich] Grebenyuk bundle transcripts (7367.mp3, 7385.mp4, 7390.mp4)
- source: wiki/sources/2026-04-14-tg-grebenukm-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-grebenukm-mar-apr-2026.md (Обновлены секции Аудио/Видео с транскриптами, добавлена макроэкономическая рамка в Факты и цифры, enriched ПДВН-данные)
  - wiki/evolving/competitor-positioning/grebenyuk-anomaly-community.md (Добавлен кризис-framing из voice 7367, уточнены ПДВН-данные (300-400 чел, пятёрки, телемосты), добавлен формат serial content медкомпании из 7390)
  - wiki/evolving/content-trends/urgency-window-launch-playbook.md (Добавлена Фаза 0 (voice-first FOMO seed) по транскрипту 7367, обновлён чек-лист)
  - wiki/canon/marketing-frameworks/demand-first-mvp-castdev.md (Добавлен кризис как триггер применения фреймворка (из voice 7367))
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен Grebenyuk voice-FOMO format section, source добавлен в front-matter)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving': 3, 'canon': 1}
- touched: 5 pages
- raw: no raw moves (enrich-only run, files already in raw/processed/)

## [2026-04-15 12:00] [ingest] | ENRICH video transcripts | tg_gurinovich_shares bundle (870, 896)
- source: wiki/sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-gurinovich-shares-jan-mar-2026.md (Added Транскрипты медиа section with audit of 870.mp4 (no speech) and 896.mp4 (irrelevant personal clip))
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode — transcripts already in raw/processed/video/)

## [2026-04-15 12:30] [ingest] | [enrich] hh.ru Галочка — 5 video transcripts added
- source: wiki/sources/2026-04-14-tg-hh-ru-official-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-hh-ru-official-mar-apr-2026.md (Added full transcripts for 5 video children (4807/4815/4820/4826/4829); replaced read-failed block; added 3 new key ideas from transcripts)
  - wiki/evolving/content-trends/hh-ru-galochka-mascot-campaign.md (Added sections 3a (Gaechka sidekick) and 3b (corporate jargon parody); enriched timeline with transcript details; added audio-only brand-recall hook analysis)
  - wiki/evolving/content-trends/telegram-native-formats.md (Added transcript-derived format observations to hh.ru exemplar: audio-only brand-recall hook, sidekick character, enumerative parody)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving': 2}
- touched: 3 pages
- raw: no raw moves (enrich mode — transcripts read from raw/processed/video/)

## [2026-04-15 15:10] [ingest] | ENRICH @howtomake10x — транскрипты медиа (podcast 1493 B2B sales slowdown + 3 видео)
- source: wiki/sources/2026-04-14-tg-howtomake10x-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-howtomake10x-mar-apr-2026.md (Enrich: добавлены транскрипты 4 children (1493/1486/1492/1498), обновлён per-post audit (1493 A->R), добавлен раздел Транскрипты медиа)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (+раздел 7 Третий независимый голос Крылов podcast 1493: ~15 B2B owners, hiring-as-survival, multi-touch sales, confidence medium->high)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (+2 новых хука из podcast 1493: найм как survival skill 2026 + multi-touch продажа вместо одного звонка)
  - wiki/evolving/product-reception/gro-productivity-energy-angle.md (+engagement-тест Крылова из podcast 1493 как diagnostic hook для Arc 3 (отключившиеся))
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving': 3}
- touched: 4 pages
- raw: no raw moves (enrich mode, files already in raw/processed/)

## [2026-04-15 12:00] [ingest] | [enrich] | tg_hr_kak_delat — 9 video transcripts reviewed, 0 relevant
- source: wiki/sources/2026-04-14-tg-hr-kak-delat-feb-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-hr-kak-delat-feb-apr-2026.md (enrich: added transcript summaries for 9 video children, confirmed irrelevance, added Транскрипты медиа section)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode, files already in raw/processed/)

## [2026-04-15 10:30] [ingest] | [enrich] video transcripts for tg_kommersant digi 13-14 Apr 2026
- source: wiki/sources/2026-04-14-tg-kommersant-apr-13-14.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-kommersant-apr-13-14.md (Добавлена секция Транскрипты медиа (4 видео), обновлена таблица Медиа-вложения)
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (Добавлена verbatim-цитата Пескова о цифровых ограничениях (транскрипция видео 105461) + source backlink)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving': 1}
- touched: 2 pages
- raw: no raw moves (enrich mode — files already in raw/processed/video/)

## [2026-04-15 14:50] [ingest] | ENRICH tg-moibiz-apr-04-14 (+3 video transcripts, no new layer content)
- source: wiki/sources/2026-04-14-tg-moibiz-apr-04-14.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-moibiz-apr-04-14.md (Added transcript section for 3 video children (7351 speech transcribed, 7361+7362 no speech); updated media inventory; no new layer-relevant content found)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode — files already in raw/processed/)

## [2026-04-15 21:00] [ingest] | [enrich] video transcripts for tg-mspiridonov bundle (6 children)
- source: wiki/sources/2026-04-14-tg-mspiridonov-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-mspiridonov-mar-apr-2026.md (Replaced video transcripts-skipped section with actual transcript summaries; added new facts from 4280 transcript (Claude Sonnet 4.6, Andon Market, operational details))
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md (Section 7 (Luna): added Claude Sonnet 4.6 as underlying model, Andon Market name/address, proactive initiative details, ethics framing from first-party video, third conclusion about Anthropic ecosystem)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Hook 10.3: enriched with first-party details from Andon Labs video transcript (model, address, proactive initiative, ethics framing, new content angle))
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving': 2}
- touched: 3 pages
- raw: no raw moves (enrich mode — files already in raw/processed/video/)

## [2026-04-15 12:00] [ingest] | ENRICH video transcripts — tg_neuraldvig 2026-04-07..14
- source: wiki/sources/2026-04-14-tg-neuraldvig-apr-7-14.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-neuraldvig-apr-7-14.md (Added transcript analysis for 14 video children; confirmed decorative content, no new facts)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode — files already in raw/processed/)

## [2026-04-15 00:00] [ingest] | [enrich] tg_opora_russia week 7 — video transcripts (no new content)
- source: wiki/sources/2026-04-14-tg-opora-russia-week-7.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-opora-russia-week-7.md (Added Транскрипты медиа section with results of whisper transcription for 2 video children (both empty of speech))
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode — files already in raw/processed/)

## [2026-04-15 15:00] [ingest] | Petrochenkow enrich — 3 video transcripts (1205, 1236, 1243)
- source: wiki/sources/2026-04-14-tg-petrochenkow-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-petrochenkow-mar-apr-2026.md (Добавлен раздел Транскрипты медиа с 3 видео-транскриптами, обновлены описания в Распознанный текст)
  - wiki/volatile-strict/industry-news/openai-ads-chatgpt-2026-03.md (Добавлена секция с визуальной иллюстрацией ad-injection паттерна из сатирического скетча (видео 1205))
  - wiki/evolving/industry-trends/ai-marketing-limits-2026.md (Добавлено подтверждение продуктизации AI-исследования рынка из видео-кружка 1236)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'volatile-strict': 1, 'evolving': 1}
- touched: 3 pages
- raw: No raw moves (enrich-only pass; transcripts already in raw/processed/video/)

## [2026-04-15 07:10] [ingest] | [enrich] Portnyaginlive video transcripts (16 videos, 2 relevant)
- source: wiki/sources/2026-04-14-tg-portnyaginlive-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-portnyaginlive-mar-apr-2026.md (Added Транскрипты медиа section (16 videos), updated video table from not-transcribed to transcribed, reclassified 11166+11168 as relevant)
  - wiki/evolving/content-trends/portnyagin-founder-channel-patterns.md (Added 2 new format patterns: #9 raw founder monologue (11166), #10 satirical skit (11168); updated format proportions table; added authenticity-valve observation to key thesis)
  - wiki/volatile-strict/industry-news/ru-vpn-metering-proposal-2026-04.md (Added satirical skit 11168 as audience-reaction signal to VPN-metering proposal)
  - wiki/evolving/content-trends/telegram-native-formats.md (Brief note on satirical skit as extension of meme-news format)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving': 2, 'volatile-strict': 1}
- touched: 4 pages
- raw: no raw moves (enrich mode — files already in raw/processed/)

## [2026-04-15 06:50] [ingest] | ENRICH tg-recruiter-live-career-digest (video transcripts)
- source: wiki/sources/2026-04-14-tg-recruiter-live-career-digest.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-recruiter-live-career-digest.md (Added Транскрипты медиа section with transcripts of 2 video children (4385.mp4, 4400.mp4); both confirmed as #fun memes with no extractable content)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode, files already in raw/processed/)

## [2026-04-15 12:00] [ingest] | [enrich] | tg_rff_channel video transcripts (5x meme, no new extractions)
- source: wiki/sources/2026-04-14-tg-rff-channel-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-rff-channel-mar-apr-2026.md (Added Транскрипты медиа section with 5 video transcripts (all meme, irrelevant); updated video-children note in Релевантность section)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: N/A (enrich mode, no raw moves)

## [2026-04-15 14:55] [ingest] | ENRICH @rybakovigor -- 14 video transcripts, +3 hooks, +Physical AI signal
- source: wiki/sources/2026-04-14-tg-rybakovigor-march-april-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-rybakovigor-march-april-2026.md (Added Транскрипты медиа section with summaries of all 14 video transcripts, updated video section and relevance)
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md (Added 3 hooks (#8 Physical AI, #9 death-and-rebirth resilience, #10 plan-situational mode) from video transcripts)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Added Physical AI signal from Rybakov + Moscow 15% civil servants AI replacement data point)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'evolving': 2}
- touched: 3 pages
- raw: N/A (enrich mode -- no raw file moves)

## [2026-04-15 12:00] [ingest] | ENRICH tg_selfworkru — transcript for video 3031.mp4 (empty)
- source: wiki/sources/2026-04-14-tg-selfworkru-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-selfworkru-mar-apr-2026.md (Added transcript result for video child 3031.mp4 (whisper output: watermark only, no speech))
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode)

## [2026-04-15 23:10] [ingest] | ENRICH @sergei_ivanov_efko — 22 transcripts reviewed, source page enriched
- source: wiki/sources/2026-04-14-tg-sergei-ivanov-efko-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-sergei-ivanov-efko-mar-apr-2026.md (ENRICH pass: added transcript summaries for 18 video + 4 audio children, confirmed original relevance assessment, enriched video 4019 Altero placement with verbatim spoken CTA)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode, files already in raw/processed/)

## [2026-04-15 14:50] [ingest] | [enrich] sokolay video transcripts (20 children)
- source: wiki/sources/2026-04-14-tg-sokolay-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-sokolay-mar-apr-2026.md (enrich: added transcript summaries for 4 podcast teasers (3606/3607/3628/3629), confirmed 16 lifestyle videos as zero-content, updated media table)
  - wiki/evolving/content-trends/podcast-driven-author-channel-patterns.md (enrich: added teaser credential-stack template detail, rapid-fire quote montage format, Minaev YouTube platform signal)
  - wiki/evolving/content-trends/telegram-author-channel-patterns.md (enrich: added teaser format detail to podcast-driven subcategory B description)
  - wiki/evolving/content-trends/telegram-native-formats.md (enrich: added transcript detail and Minaev platform endorsement to sokolay exemplar section)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'sources': 1}
- touched: 4 pages
- raw: n/a (enrich mode, no raw file moves)

## [2026-04-15 14:45] [ingest] | ENRICH tg-startupoftheday-mar-apr-2026 (transcript 4979)
- source: wiki/sources/2026-04-14-tg-startupoftheday-mar-apr-2026.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode, transcript already in raw/processed/video/)

## [2026-04-15 15:00] [ingest] | @studentsuper enrich — 22 video transcripts reviewed, zero new extractions
- source: wiki/sources/2026-04-14-tg-studentsuper-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-studentsuper-mar-apr-2026.md (Added transcript review results (enrich pass): 22 video transcripts confirmed zero factual content, added transcript summary table)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode — files already in raw/processed/)

## [2026-04-15 12:00] [ingest] | [enrich] tg_t_jrnl video 34100 transcript — anti-infobiz «План Б»
- source: wiki/sources/2026-04-14-tg-t-jrnl-apr2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-t-jrnl-apr2026.md (Добавлены секции Транскрипты медиа (34100) и ключевой тезис anti-infobiz в Ключевые идеи и Релевантность)
  - wiki/canon/positioning/gro-value-proposition.md (Новая секция anti-infobiz resonance из «Плана Б» Т-Ж)
  - wiki/evolving/content-trends/ru-business-tg-content-drift-2026.md (Корроборация дрейфа от инфобиза вторым независимым источником (План Б Т-Ж))
  - wiki/evolving/content-trends/ru-sales-infobiz-content-patterns.md (Добавлен внешний контекст mainstream-перцепции инфобиза)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Добавлен Hook 10 — anti-infobiz «PDF» из «Плана Б» Т-Ж)
  - wiki/evolving-strict/market-data/ai-driven-layoffs-2025-2026.md (Enrich note: transcript 34100 усиливает нарратив «готовься заранее»)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'canon': 1, 'evolving': 3, 'evolving-strict': 1}
- touched: 6 pages
- raw: no raw moves (enrich mode — files already in raw/processed/)

## [2026-04-15 12:00] [ingest] | [enrich] | @techno_yandex video transcripts (8 of 9)
- source: wiki/sources/2026-04-14-tg-techno-yandex-mar-apr-2026.md
- created:
  - wiki/evolving/content-trends/ai-serial-content-format-2026.md
- updated:
  - wiki/sources/2026-04-14-tg-techno-yandex-mar-apr-2026.md (Added Транскрипты медиа section with 8 transcript summaries, updated bundle metadata)
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md (Added Yandex first-party video articulation section (video 5070): mass-media validation + Yandex own agents)
  - wiki/evolving/content-trends/telegram-native-formats.md (Added Telegram April 2026 AI text editor section (7 styles, premium-only, open models))
  - wiki/volatile-strict/industry-news/yandex-alice-ai-visibility-tool-2026-04.md (Added Alice AI integrated into Yandex Search UI + EE Blender (50ms) section)
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md (Added AI-product launches section: Telegram AI editor, Alice AI in search, Gemma 4 offline ASR)
  - wiki/evolving/content-trends/ai-in-pr-workflows-2026.md (Added agent-paradigm cross-link section + cross-link to ai-serial-content-format-2026)
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 4, 'volatile-strict': 2, 'sources': 1}
- touched: 8 pages
- raw: N/A (enrich mode, no raw file moves)

## [2026-04-15 14:50] [ingest] | ENRICH @telega_Rinata — 5 audio/video transcripts (voice-note format pattern)
- source: wiki/sources/2026-04-14-tg-telega-rinata-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-telega-rinata-mar-apr-2026.md (Added transcript summaries for 5 audio/video children (enrich pass))
  - wiki/evolving/content-trends/telegram-native-formats.md (Added structured voice-note format pattern from transcript 549 (7-min management monologue with narrative arc))
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 1, 'sources': 1}
- touched: 2 pages
- raw: no raw moves (enrich mode — files already in raw/processed/)

## [2026-04-15 12:00] [ingest] | ENRICH tg_vcnews_20260414 — video transcripts (3)
- source: wiki/sources/2026-04-14-tg-vcnews-apr-10-14.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-vcnews-apr-10-14.md (Добавлена секция Транскрипты медиа (3 видео), обновлена секция Медиа-вложения с результатами транскрипции)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: no raw moves (enrich mode, files already in raw/processed/)

## [2026-04-15 15:15] [ingest] | ENRICH @vyakuba — 19 video transcripts (7 substantive)
- source: wiki/sources/2026-04-14-tg-vyakuba-mar-apr-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-vyakuba-mar-apr-2026.md (Added Транскрипты медиа section with 19 transcript summaries (7 substantive + 12 non-substantive), updated metadata)
  - wiki/evolving/competitor-positioning/vyakuba-sales-training.md (Added Minsk metrics (30/300 ppl, sold-out 2 weeks), guest speaker credentials, live stage micro-coaching format, 2 new hooks from transcripts)
  - wiki/evolving/content-trends/ru-sales-infobiz-content-patterns.md (Added Genre 8 (live stage micro-coaching) and Genre 9 (guest-speaker collaboration podcast) from video transcripts)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (Added 3rd voice (Yakuba) paradox-hooks section: leadership-inspire hook (6659) + customer-is-never-wrong hook (6695/Ibragimov))
- superseded: none
- sensitive flag: none
- layer-touched: {'evolving': 3, 'sources': 1}
- touched: 4 pages
- raw: no raw moves (enrich mode — files already in raw/processed/)

## [2026-04-15 12:00] [ingest] | [enrich] video transcript 576 for tg-your-pet-project-jan-apr2026
- source: wiki/sources/2026-04-14-tg-your-pet-project-jan-apr2026.md
- created: none
- updated:
  - wiki/sources/2026-04-14-tg-your-pet-project-jan-apr2026.md (replaced read-failed note for video 576 with actual transcript content)
  - wiki/canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage.md (added Raccoon meme-video section reinforcing pricing thesis (40x250 > 2000x5))
  - wiki/evolving/content-trends/your-pet-project-channel-hooks.md (added Raccoon meme-format hook subsection with video content framing)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (added Raccoon meme-video as format reference under 5b hook family)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1, 'canon': 1, 'evolving': 2}
- touched: 4 pages
- raw: no raw moves (enrich mode; transcript sidecar already in raw/processed/video/)

## [2026-04-15 17:43] [ingest] | [enrich] tg_incrussiamedia дайджест 8-14 апреля — 2 video transcripts
- source: wiki/sources/2026-04-15-tg-incrussiamedia-apr-8-14-2026.md
- created: none
- updated:
  - wiki/sources/2026-04-15-tg-incrussiamedia-apr-8-14-2026.md (Добавлена секция Транскрипты медиа (2 видео), обновлены аннотации в Медиа-вложения: read failed -> транскрипт создан)
- superseded: none
- sensitive flag: none
- layer-touched: {'sources': 1}
- touched: 1 pages
- raw: n/a (enrich mode, no raw moves)

## [2026-04-16 19:30] [reflect] | wiki-query agent UX: human-readable output + save criteria + concurrency
- analyzed: wiki-query.md manual, CLAUDE.md delegation/hooks, ingest-pending.md parallel mode, lib.sh worktree detection. 0 query log entries (agent never ran)
- report: wiki/lint-reports/2026-04-16-reflect-query-ux.md
- proposed & applied:
  - A: human-readable output rule — interpret [conf:*, src:*] markers instead of copying raw (.claude/agents/wiki-query.md steps 3, 4, 9, anti-patterns)
  - B: operational save/skip test for step 5 (3+ pages synthesis, reuse potential, novel insight) (.claude/agents/wiki-query.md step 5)
  - C: query concurrency via worktrees — always-worktree dispatch, merge protocol reusing Phase 2.5, coexistence matrix with ingest (CLAUDE.md new section + delegation rules + git exceptions; .claude/agents/wiki-query.md new Runtime environment section)
  - D: MCP query pipeline — removed --no-save (queries now accumulate knowledge), added worktree isolation per query, merge with fcntl lock, commit safety net, human-readable SYSTEM_PROMPT. No regex sanitization — prompt-only approach.
  - E: усилены формулировки anti-marker rule в wiki-query.md (шаги 3, 4, 9) после трёх неудачных тестов
- layer-touched: {lint-reports: 1}
- touched: 6 files (CLAUDE.md, .claude/agents/wiki-query.md, /srv/services/wiki-mcp/tools/query.py, Dockerfile, README.md, reflect report)

## [2026-04-16 14:36] [ingest] | web_dzen.ru Манса Муса (irrelevant)
- source: wiki/sources/2026-04-16-dzen-mansa-musa-history.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_dzen.ru_a_Z4EEAPEeO2kurFW2_9933158d.md

## [2026-04-16 14:36] [ingest] | Дзен — Папа Римский / Южный Судан (off-topic, no extractions)
- source: wiki/sources/2026-04-16-dzen-pope-south-sudan.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_dzen.ru_a_Z4EGNFIKZSAPtCOf_358c094a.md

## [2026-04-16 14:36] [ingest] | dzen — naked yoga YouTube moderation (irrelevant)
- source: wiki/sources/2026-04-16-dzen-naked-yoga-youtube-moderation.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_dzen.ru_a_Z4EFVbCeRkIjSU9M_8b659cce.md

## [2026-04-16 14:36] [ingest] | Дзен: мем «Я глажу кота перед ядерным взрывом» (irrelevant)
- source: wiki/sources/2026-04-16-dzen-cat-nuclear-meme.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_dzen.ru_a_Z4EG9X-wGS6tY7hY_fdc66094.md

## [2026-04-16 14:36] [ingest] | Дзен: мем «плюшки» (irrelevant source)
- source: wiki/sources/2026-04-16-dzen-saddest-meme-cat.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_dzen.ru_a_Z4EH-tv19SrPhdUM_7aed1b72.md

## [2026-04-16 14:36] [ingest] | dzen.ru — Тамам Шуд (irrelevant)
- source: wiki/sources/2026-04-16-dzen-tamam-shud-case.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_dzen.ru_a_Z4EIY5HKvXOZj9HG_5d8ea338.md

## [2026-04-16 14:36] [ingest] | Дзен — хакер vs мошенники (irrelevant, no extractions)
- source: wiki/sources/2026-04-16-dzen-scambaiter-hacker-vs-scammers.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_dzen.ru_a_Z4EHhogeZFjMq7W4_c031d799.md

## [2026-04-16 14:36] [ingest] | hh.ru/Clickme: AI-инструменты для рекламы вакансий
- source: wiki/sources/2026-04-16-hh-clickme-ai-tools.md
- created:
  - wiki/evolving/industry-trends/ai-generated-creatives-in-advertising.md
- updated:
  - wiki/canon/marketing-frameworks/native-advertising.md (добавлен cross-link на AI-генерацию креативов)
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md (добавлен cross-link на AI-генерацию как альтернативу UGC-визуалам)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, canon: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_hh.ru_article_iskusstvennyj-intellekt-v-clickme-chto-umeet-i-kak-i_0a2fb82e.md

## [2026-04-16 14:36] [ingest] | hh.ru — 6 трендов найма на 2026 год
- source: wiki/sources/2026-04-16-hh-hiring-trends-2026.md
- created:
  - wiki/evolving/industry-trends/hiring-trends-russia-2026.md
  - wiki/evolving/content-trends/hiring-trends-content-hooks-gro.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (Добавлен раздел «Внешние сигналы из рынка труда (2026-04-16)» с данными hh.ru о поляризации, ИИ-грамотности, гибридных ролях)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен раздел кросс-верификации: ИИ-грамотность must-have из hh.ru как частичное подтверждение тезиса)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, canon: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_hh.ru_article_6-trendov-v-najme-na-2026-god-kotorye-prognoziruyut-_2750dffa.md

## [2026-04-16 14:40] [ingest] | hh.ru: брендирование вакансий -- 7 принципов визуального контент-дизайна
- source: wiki/sources/2026-04-16-hh-employer-branding-vacancies.md
- created:
  - wiki/canon/marketing-frameworks/visual-content-design-for-conversion.md
- updated:
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md (Добавлен раздел EGC как драйвер конверсии + cross-link на visual-content-design)
  - wiki/canon/marketing-frameworks/native-advertising.md (Cross-link на visual-content-design-for-conversion)
  - wiki/evolving/content-trends/telegram-native-formats.md (Cross-link на visual-content-design-for-conversion)
  - wiki/canon/product-knowledge/gro-testimonials.md (Добавлен раздел визуального усиления testimonials + cross-link)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_hh.ru_article_kak-brendirovanie-vakansij-na-hh-ru-povyshaet-kolich_1daaa3a4.md

## [2026-04-16 14:36] [ingest] | vc.ru — OpenAI внутренняя записка о конкуренции с Anthropic (апрель 2026)
- source: wiki/sources/2026-04-16-vc-openai-competition-memo-apr2026.md
- created:
  - wiki/volatile-strict/industry-news/openai-enterprise-pivot-apr2026.md
  - wiki/evolving-strict/market-data/ai-platform-revenue-2026.md
  - wiki/evolving/industry-trends/ai-platform-wars-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен связанный контекст: конкуренция AI-платформ подтверждает ускорение инфраструктуры, добавлена ссылка на ai-platform-wars-2026)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving-strict: 1, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_vc.ru_ai_2866812-konkurenciya-na-rynke-ii-openai-strategiya-razvit_6d8312f6.md

## [2026-04-16 14:40] [ingest] | vc.ru/ai: OpenAI GPT-5.4 Cyber + валюационный дрейф
- source: wiki/sources/2026-04-16-vcru-openai-gpt54-cyber.md
- created:
  - wiki/volatile-strict/industry-news/openai-gpt54-cyber-launch-2026.md
  - wiki/volatile-strict/industry-news/openai-852b-valuation-doubt-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен раздел Enterprise pivot как подтверждение фазы 1 (GPT-5.4 Cyber + Claude Mythos + OpenAI valuation doubt))
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 2, evolving: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_vc.ru_ai_2869036-openai-gpt54-cyber-dlya-specialistov-v-kiberbezop_1ca0c9d7.md

## [2026-04-16 14:40] [ingest] | vc.ru/ai: Allbirds -> NewBird AI (GPUaaS pivot)
- source: wiki/sources/2026-04-16-vcru-allbirds-newbird-ai-pivot.md
- created:
  - wiki/volatile-strict/industry-news/allbirds-newbird-ai-pivot-2026.md
  - wiki/evolving/industry-trends/ai-infrastructure-demand-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Added supply-side section (AI infrastructure demand as condition for solopreneurship window))
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Added hook #5 (AI-hype multiplier from Allbirds/NewBird AI case))
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 3, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_vc.ru_ai_2869875-allbirds-pereimenovka-newbird-ai-oblachnye-reshen_d220c7db.md

## [2026-04-16 14:40] [ingest] | Apple Siri AI-upskilling (vc.ru / The Information)
- source: wiki/sources/2026-04-16-apple-siri-ai-upskilling.md
- created:
  - wiki/volatile-strict/industry-news/apple-siri-ai-course-2026.md
  - wiki/evolving/industry-trends/enterprise-ai-upskilling-2026.md
  - wiki/evolving/content-trends/ai-adoption-news-hooks.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен кейс Apple/Siri как подтверждение тезиса о корпоративной инерции + запись в Contradictions)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлен cross-link на комплементарный набор news-hooks из AI-adoption новостей)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 4, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_vc.ru_apple_2870994-apple-otpravlyaet-razrabotchikov-siri-na-kurs-_d58c0157.md

## [2026-04-16 14:40] [ingest] | vc.ru: Google Gemini macOS app + Apple-Siri-Gemini (iOS 27)
- source: wiki/sources/2026-04-16-vcru-google-gemini-macos-app.md
- created:
  - wiki/volatile-strict/competitor-news/google-gemini-macos-native-app-2026-04.md
- updated:
  - wiki/evolving/content-trends/aeo-geo-llm-search-optimization-2026.md (Added section on desktop AI-assistants as GEO accelerator (Gemini macOS app + Siri-Gemini))
  - wiki/evolving-strict/market-data/alice-ai-usage-breakdown-2026.md (Added cross-link to Gemini macOS app as global comparator for desktop AI assistants)
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md (Added cross-link to Gemini screen sharing as early desktop agent pattern)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_vc.ru_apple_2870097-google-gemini-prilozhenie-dlya-macos_e3f8068b.md

## [2026-04-16 14:40] [ingest] | vc.ru/headhunter VTB x hh.ru Mashina Vremeni (interactive video employer branding)
- source: wiki/sources/2026-04-16-vtb-hh-mashina-vremeni.md
- created:
  - wiki/evolving/content-trends/interactive-video-employer-branding.md
- updated:
  - wiki/canon-strict/historical-campaigns/native-pr-cases-2026.md (Added VTB x hh.ru Time Machine as case #4 (gamified interactive video, ~7500 interactions))
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (Added VTB Time Machine as proof-point for format complexity trend (section 4))
  - wiki/evolving/content-trends/telegram-native-formats.md (Added cross-reference section about web-based interactive formats beyond Telegram)
  - wiki/canon/marketing-frameworks/native-advertising.md (Added cross-link to interactive-video-employer-branding page)
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, evolving: 3, canon: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_vc.ru_headhunter_2128622-proekt-vtb-i-hh-ru-mashina-vremeni-dlya-s_8ad081b9.md

## [2026-04-16 14:36] [ingest] | vc.ru/hr: five handshakes networking (irrelevant)
- source: wiki/sources/2026-04-16-vcru-hr-five-handshakes-networking.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_vc.ru_hr_2703115-teoriya-pyati-rukopozhatiy_a32953df.md

## [2026-04-16 14:40] [ingest] | Pressfeed: 12 маркеров AI-текста (статья)
- source: wiki/sources/2026-04-16-pressfeed-12-ai-text-markers.md
- created:
  - wiki/canon/marketing-frameworks/ai-text-markers-checklist.md
  - wiki/evolving/content-trends/ai-text-detection-landscape-2026.md
- updated:
  - wiki/canon/marketing-frameworks/native-advertising.md (Добавлена секция AI-контент и нативная реклама + cross-links на чек-лист маркеров)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлена секция AI-контент и Telegram-нативы + cross-links)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_12-markerov-ai-teksta-kak-redaktor-otlichaet-mashinu-ot-avto_39a6ff9c.md

## [2026-04-16 14:40] [ingest] | Forbes: НДС-реформа для общепита (УСН/ПСН) — временное смягчение апрель-декабрь 2026
- source: wiki/sources/2026-04-16-forbes-vat-relief-horeca-2026.md
- created:
  - wiki/volatile-strict/industry-news/vat-reform-horeca-russia-2026.md
- updated:
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md (добавлен cross-link на НДС-реформу как параллельную регуляторную нагрузку)
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (добавлен cross-link на НДС-реформу как вектор регуляторного давления)
  - wiki/canon/target-audience/gro-segments.md (добавлен раздел макро-давления на сегменты 2 и 3 от налоговой реформы)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, canon-strict: 1, evolving: 1, canon: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_www.forbes.ru_biznes_559168-gosduma-prinala-zakon-o-vremennom-smagcenii-us_bbaeea51.md

## [2026-04-16 14:36] [ingest] | Cossa.ru SEO course listing (irrelevant, audit only)
- source: wiki/sources/2026-04-16-cossa-seo-course-listing.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.cossa.ru_events_238_127047_bdf3b892.md

## [2026-04-16 14:36] [ingest] | secretmag.ru: Что делать, если не дают кредит в банке (irrelevant)
- source: wiki/sources/2026-04-16-secretmag-chto-delat-esli-ne-dayut-kredit.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_secretmag.ru_business_methods_chto-delat-esli-ne-dayut-kredit-v-banke.htm_35e20ce4.md

## [2026-04-16 14:36] [ingest] | dp.ru: Петербуржец лишился Audi (irrelevant)
- source: wiki/sources/2026-04-16-dpru-peterburzhec-audi-drunk-driving.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2025_10_01_peterburzhec-lishilsja-audi-za_4357f8e4.md

## [2026-04-16 14:36] [ingest] | Executive.ru — правила собеседования для работодателя (irrelevant)
- source: wiki/sources/2026-04-16-executive-interview-rules-for-employers.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.e-xecutive.ru_career_hr-management_337788-pravila-igry-sobesedovanie-dlya-_da98badb.md

## [2026-04-16 14:36] [ingest] | vc.ru/tbank — Тинькофф x Роза Хутор quest (irrelevant, audit-only)
- source: wiki/sources/2026-04-16-vcru-tbank-rosa-khutor-quest.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_vc.ru_tbank_1003035-kvest-prizy-i-gory-keshbeka-tinkoff-stal-partn_8a270862.md

## [2026-04-16 14:40] [ingest] | Pressfeed: 7 историй о работе с UGC (статья)
- source: wiki/sources/2026-04-16-pressfeed-ugc-7-cases.md
- created:
  - wiki/evolving-strict/campaign-metrics/ugc-cpv-benchmarks-2026.md
  - wiki/evolving/content-trends/ugc-creator-search-methods.md
- updated:
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md (Добавлены KOC (Key Opinion Consumers), always-on модель UGC, операционные принципы из 7 кейсов, CPV cross-link)
  - wiki/canon/marketing-frameworks/native-advertising.md (Добавлены cross-links на UGC creator search и CPV benchmarks)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 1, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_7-istorij-o-rabote-s-ugc-kontentom_3b8fd06d.md

## [2026-04-16 14:40] [ingest] | vc.ru — Илья DomProdazh / Kwork (история фрилансера)
- source: wiki/sources/2026-04-16-vc-ilya-domprodazh-kwork.md
- created:
  - wiki/evolving/industry-trends/freelance-platform-dependency.md
  - wiki/evolving/content-trends/freelancer-growth-narrative-hooks.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (Добавлен внешний кейс масштабирования фрилансера (Kwork, 23 человека) — усиление Сегментов 2 и 3)
  - wiki/canon/positioning/gro-value-proposition.md (Добавлен резонанс «системность vs платформенная зависимость» + cross-links на новые evolving-страницы)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, canon: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_vc.ru_story_1425330-ilya-domprodazh-kwork-obespechivaet-rabotoi-vs_51ee8705.md

## [2026-04-16 14:40] [ingest] | hh.ru — Данина: доказательный подход к найму (трёхфакторная модель + демография)
- source: wiki/sources/2026-04-16-hh-danina-evidence-based-hiring.md
- created:
  - wiki/canon/marketing-frameworks/evidence-based-hiring-3-factors.md
- updated:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (Добавлены демографическая корневая причина (яма 1990-х), секторный breakdown (розница 1.3, ИТ 12.7/1.7), зарплатная гонка, воронка подбора 100-160+ контактов)
  - wiki/evolving-strict/market-data/ru-labor-market-hh-2026.md (Добавлены метрики авг 2024 (вакансии +74%, резюме +17%, безработица 2.4%, дефицит 1.6М, гибрид 185K, reviews 79%))
  - wiki/evolving/industry-trends/hiring-trends-russia-2026.md (Добавлено количественное подтверждение поляризации (ИТ 12.7/1.7, розница 1.3) и employer branding)
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (Добавлен 4-й голос (Данина/платформа) — демографический фундамент сдвига + Red Queen модель)
  - wiki/evolving/content-trends/hiring-trends-content-hooks-gro.md (Добавлены 4 новых hook (Red Queen, 79% reviews, гибрид seniority gap, 100-160 контактов))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving-strict: 2, evolving: 3, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_hh.ru_article_chto-i-kak-myenyat-v-podborye-dokazatyelnyy-podkhod-_a50609d2.md

## [2026-04-16 14:40] [ingest] | Pressfeed: тренды контент- и SMM-стратегии в 2026 году
- source: wiki/sources/2026-04-16-pressfeed-smm-content-trends-2026.md
- created:
  - wiki/evolving/content-trends/smm-strategy-trends-2026.md
- updated:
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md (добавлен раздел UGC как столп контент-системы 2026 + cross-link на smm-strategy-trends-2026)
  - wiki/evolving/content-trends/telegram-native-formats.md (добавлен раздел пересечения с SMM-трендами 2026 + cross-link)
  - wiki/canon/marketing-frameworks/native-advertising.md (добавлен cross-link на smm-strategy-trends-2026)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, canon: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_trendy-kontent-i-smm-strategii-v-2026-godu-czennost-zhivogo-_2de95eae.md

## [2026-04-16 14:40] [ingest] | Pressfeed: GEO вместо SEO — 3-mechanism model + anti-pattern ChatGPT injection
- source: wiki/sources/2026-04-16-pressfeed-geo-vmesto-seo.md
- created:
  - wiki/evolving/content-trends/aeo-geo-llm-search-optimization-2026.md
- updated:
  - wiki/canon/marketing-frameworks/native-advertising.md (Добавлена секция GEO как эволюция нативного посева + cross-link)
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (Расширена рекомендация #7 (SEO для собственных каналов) ссылкой на GEO-тренд)
  - wiki/canon/positioning/gro-value-proposition.md (Добавлен cross-link на GEO-стратегию для value-prop GRO)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, canon: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_geo-vmesto-seo-kak-popast-v-otvety-chatgpt-i-zachem-eto-bizn_eb1757ff.md

## [2026-04-16 14:40] [ingest] | Pressfeed condensed: 35 статей -- AEO/GEO, digital paralysis РФ, PR frameworks, content trends 2026
- source: wiki/sources/2026-04-16-condense-pressfeed-35-articles.md
- created:
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md
  - wiki/evolving/industry-trends/ru-marketing-digital-paralysis-mar2026.md
  - wiki/evolving/industry-trends/ru-brand-russification-law-2026.md
  - wiki/evolving/content-trends/sensory-marketing-trend-2026.md
  - wiki/evolving/content-trends/personal-brand-shift-2026.md
  - wiki/evolving/content-trends/ai-content-production-multiagent-2026.md
  - wiki/canon/marketing-frameworks/seo-for-ai-era-playbook.md
  - wiki/canon/marketing-frameworks/performance-pr-framework.md
  - wiki/canon/marketing-frameworks/crisis-pr-principles.md
  - wiki/canon/marketing-frameworks/mobile-ux-b2b-conversion.md
  - wiki/canon/marketing-frameworks/speaking-as-marketing-channel.md
  - wiki/canon/marketing-frameworks/business-metrics-for-owners.md
  - wiki/evolving-strict/campaign-metrics/pressfeed-pr-cases-2026.md
- updated:
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md (Добавлены ФЗ 168-ФЗ русификация брендов и отраслевые ограничения рекламы (табак, медицина, обсценная лексика))
  - wiki/canon/marketing-frameworks/native-advertising.md (Добавлен раздел SEO-усиление нативных публикаций + ссылки на новые страницы)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, canon-strict: 1, evolving: 6, evolving-strict: 1, sources: 1}
- touched: 16 pages
- raw: raw/processed/articles/_condense_pressfeed_2026-04-16.md

## [2026-04-16 14:40] [ingest] | Condensed: e-xecutive.ru (23 статьи) -- 2 marketing-фреймворка
- source: wiki/sources/2026-04-16-condense-e-xecutive-23-articles.md
- created:
  - wiki/canon/marketing-frameworks/marketing-as-communication-5th-p.md
  - wiki/canon/marketing-frameworks/offensive-marketing-framework.md
- updated:
  - wiki/canon/marketing-frameworks/native-advertising.md (Добавлены cross-links на 5th P и offensive marketing)
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md (Добавлены cross-links на 5th P и offensive marketing)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/_condense_e-xecutive_2026-04-16.md

## [2026-04-16 14:45] [ingest] | hh.ru blog condensed (43 articles): HRTech ecosystem, labor market, skill-based hiring, employer branding patterns
- source: wiki/sources/2026-04-16-condense-hh-ru-blog-43.md
- created:
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md
  - wiki/evolving-strict/market-data/ru-labor-market-structural-2024-2026.md
  - wiki/evolving/industry-trends/skill-based-hiring-russia-2026.md
  - wiki/canon/marketing-frameworks/employer-branding-review-funnel.md
  - wiki/evolving/content-trends/hh-ru-blog-content-patterns.md
  - wiki/canon/target-audience/hrd-portrait-2025-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (Добавлены исторические метрики из блога hh.ru (hh-индекс 3.1 июнь 2024, вакансии x2, дефицит 1.6M->4M, розница 3.3), зафиксировано не-противоречие с hh-индексом 9.8 Q1 2026)
  - wiki/evolving/industry-trends/hiring-trends-russia-2026.md (Добавлены 6 мега-трендов hh.ru (навыкоцентричность, внутренние маркетплейсы, удалёнка, команды, кризис мотивации, интерфейсизация) + ссылка на портрет HRD)
  - wiki/evolving-strict/market-data/ru-hrtech-market-2023-2025.md (Добавлены per-product метрики: Dream Job 6M/мес + 599 открытых работодателей, чат-бот 11.2% конверсия, AI NPS 97% + +40% откликов)
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (Добавлен 4-й голос (демографический фундамент из hh.ru): яма 1990-х, дефицит 1.6M->4M, навыкоцентричность 68% как ответ)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 4, evolving-strict: 3, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/_condense_hh-ru_2026-04-16.md

## [2026-04-16 14:45] [ingest] | Condensed: 18 vc.ru misc (Anthropic $800B, Google AI, Uber pivot, T-Bank Time)
- source: wiki/sources/2026-04-16-condense-vcru-misc-18.md
- created:
  - wiki/volatile-strict/competitor-news/anthropic-800b-identity-verification-2026-04.md
  - wiki/volatile-strict/competitor-news/google-gemini-chrome-ai-2026-04.md
  - wiki/volatile-strict/competitor-news/uber-autonomous-strategy-pivot-2026.md
  - wiki/evolving/industry-trends/tbank-corporate-platform-stack-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (Добавлен пятый голос (vc.ru/opinions) подтверждения кадрового голода)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 3, evolving: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/_condense_vcru-misc_2026-04-16.md

## [2026-04-16 14:50] [ingest] | vc.ru/hr condensed 37 articles: HR Tech, labor market stagnation, Garmony AI, GenAI specialization
- source: wiki/sources/2026-04-16-vcru-hr-condensed-37-articles.md
- created:
  - wiki/evolving-strict/market-data/ru-labor-market-stagnation-q1-2026.md
  - wiki/evolving-strict/market-data/ru-hr-tech-market-size-2026.md
  - wiki/evolving-strict/market-data/ru-hiring-cost-benchmarks-2026.md
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md
  - wiki/evolving/industry-trends/return-to-office-global-2026.md
  - wiki/evolving/industry-trends/genai-engineering-ru-specialization-2026.md
  - wiki/evolving/competitor-positioning/garmony-ai-advertorial-campaign-2026.md
  - wiki/evolving/content-trends/vcru-hr-content-patterns-2026.md
  - wiki/canon/marketing-frameworks/hr-brand-ambassador-program.md
  - wiki/canon/marketing-frameworks/dtc-community-driven-growth.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (Добавлен рыночный контекст Q1 2026 по всем 3 сегментам (hh.индекс, anxiety-triggers, микросмены))
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md (Добавлена секция DTC community-driven growth + cross-links на новые страницы)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 3, evolving: 7, canon: 4, sources: 1}
- touched: 14 pages
- raw: raw/processed/articles/_condense_vcru-hr_2026-04-16.md

## [2026-04-16 14:50] [ingest] | vc.ru блоги: Молянов + Спиридонов + Горный (76 статей, condensed)
- source: wiki/sources/2026-04-16-vcru-blogs-molyanov-spiridonov-gorny.md
- created:
  - wiki/evolving/competitor-positioning/neyrotsekh-molyanov.md
  - wiki/canon/marketing-frameworks/spec-driven-agent-development.md
  - wiki/canon/marketing-frameworks/partnerships-growth-multiplier.md
  - wiki/evolving/content-trends/short-video-reels-tiktok-2026.md
  - wiki/evolving/content-trends/tg-posts-seo-repurposing.md
  - wiki/evolving-strict/campaign-metrics/telegram-ads-benchmarks-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Upgrade confidence low->medium: Молянов как второй verified голос, кейсы агентов (тендер, copilot), Brand Analytics подтверждение сдвига спроса)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлены hooks 5-7 от Молянова: агент-как-коллега (тендер), переход от ответов к действиям (Brand Analytics), 30-минутный TG-to-SEO tool)
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md (Добавлены качественные сигналы: медиаинфляция замедляется (E-Promo Group), структурный сдвиг digital-маркетинга РФ (CAC растёт, 2023 схемы не работают))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 4, evolving-strict: 2, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/_condense_vcru-blogs_2026-04-16.md


## [2026-04-16 19:55] [ingest] | rb.ru news: школьник из Елабуги запустил венчурный микрофонд (irrelevant, audit only)
- source: wiki/sources/2026-04-16-rb-ru-news-a-chego-dobilsya-ty-ad3b781b.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_a-chego-dobilsya-ty_ad3b781b.md

## [2026-04-16 19:55] [ingest] | Dzen / hh.ru Бренд-центр — кампания «Выходите за рамки привычного», кейсы Alfa-Bank + Сбер + metrics брендирования вакансий
- source: wiki/sources/2026-04-16-dzen-hh-brand-center-vihodite-za-ramki.md
- created:
  - wiki/canon/marketing-frameworks/brand-center-agency-operating-model.md
  - wiki/evolving/content-trends/wes-anderson-aesthetic-hr-branding-2026.md
  - wiki/evolving-strict/campaign-metrics/branded-vacancy-pages-hh-2026.md
- updated:
  - wiki/canon-strict/historical-campaigns/native-pr-cases-2026.md (Добавлены кейсы 5 (Alfa-Bank симуляция, 63K просмотров) и 6 (Сбер экстрим-забег, 39K/32% start/50%+ completion, Tagline Awards 2023 gold+bronze) в коллекцию Бренд-центра hh.ru, обновлена сводная таблица паттернов)
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md (Добавлены 4 спецпроекта Бренд-центра в секции маркетинговых кампаний (Alfa, Сбер, self-campaign «Выходите за рамки привычного», СИБУР долгосрочный B2B))
  - wiki/evolving/content-trends/interactive-video-employer-branding.md (Добавлено сопоставление форматов Бренд-центра (ВТБ interactive video vs Alfa симуляция vs Сбер экстрим-забег vs T1 игра) с наблюдением premium vs mass engagement)
  - wiki/canon/marketing-frameworks/employer-branding-review-funnel.md (Добавлены cross-links на agency operating model и branded vacancy metrics)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, canon-strict: 1, evolving: 3, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_dzen.ru_a_Zo5K3r8ACxEjzBSo_e8beb4cb.md (+ .note.md + .triage.json)

## [2026-04-16 19:55] [ingest] | tg_portnyaginlive_11125.jpg — photo duplicate (no relevant extractions)
- source: wiki/sources/2026-04-14-tg-portnyaginlive-11125-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/media/tg_portnyaginlive_11125.jpg

## [2026-04-16 19:55] [ingest] | hh.ru на Дзене: advertorial Теста профориентации («15 профессий», МГУ) — 2-й B2C-продукт hh.ru
- source: wiki/sources/2026-04-16-dzen-hh-profession-test-15.md
- created:
  - wiki/evolving/competitor-positioning/hh-ru-profession-test.md
- updated:
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md (Добавлен Тест профориентации в B2C-блок экосистемы; раскрыта двусторонняя B2C-стратегия (тест + маркетплейс = freemium-funnel))
  - wiki/evolving/content-trends/hh-ru-blog-content-patterns.md (Добавлен Формат 6 (Дзен-advertorial без промокода, pure product promo); контраст с Форматом 5 по позиции в воронке (awareness vs конверсия))
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Добавлен Hook 12 «15 подходящих профессий — а что дальше?» как anti-snapshot дифференциация GRO vs hh.ru-тест; тройка Hook 10+11+12 как канонический дифференциал от infobiz/mentor/test)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_dzen.ru_a_Zqtx_Mjtn0qjQs0k_58b904b3.md + sidecars (.note.md, .triage.json)

## [2026-04-16 19:55] [ingest] | rb.ru: Ethereum × Сколково блокчейн-центр (no relevant extractions)
- source: wiki/sources/2026-04-16-rb-ru-news-blockovo-731e5963.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_blockovo_731e5963.md (+ .note.md + .triage.json)

## [2026-04-16 19:55] [ingest] | zhazhda.biz idei-biznesa-doma (2017 listicle) — no relevant extractions (false-positive triage)
- source: wiki/sources/2026-04-16-zhazhda-biz-idei-biznesa-doma-e56aff29.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_zhazhda.biz_base_idei-biznesa-doma_e56aff29.md (+ .note.md + .triage.json)

## [2026-04-16 19:55] [ingest] | Forbes.ru: интеграция UDS×Ozon — гибридная модель SMB e-commerce + первый transactional-сигнал MAX
- source: wiki/sources/2026-04-16-forbes-uds-ozon-integration.md
- created:
  - wiki/volatile-strict/competitor-news/uds-ozon-integration-2026-04.md
  - wiki/evolving/competitor-positioning/uds-loyalty-platform.md
- updated:
  - wiki/evolving/industry-trends/freelance-platform-dependency.md (+секция «Рыночный ответ — гибридная модель своё+чужое» с UDS×Ozon как ответом на тренд платформенной зависимости, +2 cross-link-а)
  - wiki/evolving-strict/market-data/ru-ecommerce-platformization-reshetnikov-2026.md (+наблюдение «гибридная модель как следующий шаг» с потенциальной декомпозицией 62% на чистую-платформу и гибрид, watchlist на репликацию UDS-паттерна)
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (+UDS×Ozon в список инфраструктурных игроков MAX — первый транзакционный (не контентный) канал MAX)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_www.forbes.ru_novosti-kompaniy_559209-integracia-uds-i-ozon-dostavki-svoj-_b314f9d4.md (+.note.md, +.triage.json)

## [2026-04-16 19:55] [ingest] | Жажда (web): методология управления распределённой командой — canon/marketing-frameworks page + RTO-2026 контекст
- source: wiki/sources/2026-04-16-zhazhda-remote-teams.md
- created:
  - wiki/canon/marketing-frameworks/distributed-team-management-principles.md
- updated:
  - wiki/evolving/industry-trends/return-to-office-global-2026.md (Добавлена историческая рамка (Вымпелком 2016 с планом 50-70% удалёнки) + cross-link на distributed-team-management-principles — объяснение парадокса RTO через отсутствие менеджерской культуры распределёнки)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 1, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_kak-postroit-effektivnuyu-komandu-iz-udalennyh-sot_7aa27488.md + sidecars

## [2026-04-16 19:55] [ingest] | rb.ru — ПСБ×ОПОРА киноурок Владивосток (audit-only, no extractions)
- source: wiki/sources/2026-04-16-rb-ru-news-kinourok-vladivostok-7352cd7c.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_kinourok_vladivostok_7352cd7c.md (+ .note.md, .triage.json)

## [2026-04-16 19:55] [ingest] | Дзен/Инк.: Anthropic $800B — Caplight $688B, 1000 enterprise, VC-цитаты
- source: wiki/sources/2026-04-16-dzen-incrussia-anthropic-800b-caplight.md
- created: none
- updated:
  - wiki/volatile-strict/competitor-news/anthropic-800b-identity-verification-2026-04.md (Добавлены: Caplight secondary $688B (+75% за 3 мес), 1000 enterprise-клиентов ≥$1M с удвоением <2 мес, revenue baseline $9B run-rate, VC-цитаты Davis (Mithril) и Tunguz (Theory Ventures), IPO-окно конец 2026 (conf:low). Third-source усиление от Inc./incrussia.ru.)
  - wiki/volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026.md (Добавлен пункт 4 «Commercial-positioning эффект подтверждён третьим источником» — Inc./incrussia явно формулирует Claude Code commercial + Mythos closed = leading industry player. Scarcity + social proof в бренд-стратегии.)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 2, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/web_dzen.ru_a_ad_UDpBYQg6GitmW_2bc267c1.md (+ .note.md, .triage.json sidecars)

## [2026-04-16 19:55] [ingest] | dp.ru: роботизация ретейла РФ как ответ на кадровый дефицит (2025-10-08)
- source: wiki/sources/2026-04-16-dp-ru-retail-robotization-labor-deficit.md
- created:
  - wiki/evolving/industry-trends/ru-retail-robotization-labor-deficit-2025-2026.md
  - wiki/evolving-strict/market-data/ru-retail-robotization-metrics-2025-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (Добавлен шестой голос — operational response ретейла (dp.ru): 15% ретейлеров прямо называют дефицит причиной модернизации, 30% сокращения операций за 3 года, кейсы Лента/X5/Лемана Про, формулировка Соколова-Рексофт «закрывают не вакансии, а функции» как messaging-hook)
  - wiki/evolving/industry-trends/b2b-ai-adoption-fte-kpi-2026.md (Добавлена третья проекция FTE-тренда — физический труд в ретейле (30-40% сокращение клининга, 80% автоматизации в РЦ X5, full-replacement кейс Лемана Про). Таблица трёх проекций: knowledge work / industrial / physical)
  - wiki/evolving-strict/market-data/ru-labor-market-structural-2024-2026.md (В секторном breakdown розничной торговли добавлен блок "Роботизация как operational response на дефицит" с 7 ключевыми метриками из dp.ru + четвёртый пункт в GRO-значение про ретейл как самый экстремальный полигон дефицита)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2025_10_08_kadrovij-deficit-v-torgovih_8af8a06a.md (+ .note.md + .triage.json)

## [2026-04-16 19:55] [ingest] | rb.ru McKinsey/Winter Capital startup contest (no relevant extractions)
- source: wiki/sources/2026-04-16-rb-ru-mckinsey-winter-capital-startup-contest.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_mckinsey-chance_a4f5bed0.md (+ .note.md + .triage.json)

## [2026-04-16 19:55] [ingest] | Cossa — анонс вебинара Ingate/Completo по веб-аналитике (irrelevant, audit only)
- source: wiki/sources/2026-04-16-cossa-webinar-ingate-web-analytics.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.cossa.ru_events_238_130428_0a7f90e3.md (+ .note.md, .triage.json)

## [2026-04-16 19:55] [ingest] | Жажда: 5 предпринимателей после 40 — late-starter founder narrative hooks
- source: wiki/sources/2026-04-16-zhazhda-biz-lifestyle-predprinimateli-posle-40.md
- created:
  - wiki/evolving/content-trends/late-starter-founder-narrative-hooks.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (Добавлена секция «Возрастная подгруппа 40+» внутри Сегмента 2 с профилем late-starter founder, cross-link на late-starter-founder-narrative-hooks, +1 source)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлен cross-link на парную страницу late-starter-founder-narrative-hooks (возрастной контрнарратив))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_predprinimateli-posle-40_9d6ad1af.md

## [2026-04-16 19:55] [ingest] | dp.ru: Пульс МСП 2025 (Авито × Корпорация МСП) — масштаб SMB РФ + 5 трендов
- source: wiki/sources/2026-04-16-dp-ru-puls-msp-avito-corpmsp-2025.md
- created:
  - wiki/evolving-strict/market-data/ru-smb-ecosystem-scale-2025.md
  - wiki/evolving/industry-trends/ru-smb-trends-corpmsp-2025.md
  - wiki/evolving/competitor-positioning/avito-smb-analytical-content-play.md
- updated:
  - wiki/evolving-strict/market-data/ru-smb-digital-ad-spend-2026.md (Добавлены cross-links на ru-smb-ecosystem-scale-2025 и ru-smb-trends-corpmsp-2025, обновлены sources.)
  - wiki/evolving-strict/market-data/ru-youth-entrepreneurs-2026.md (Добавлена секция институционального макро-контекста (Пульс МСП 2025), обновлены sources.)
  - wiki/canon/target-audience/gro-segments.md (Добавлена секция институционального макро-контекста SMB (3 cross-link'а) и обновлены sources.)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (Добавлены cross-links на ru-smb-ecosystem-scale-2025 и ru-smb-trends-corpmsp-2025.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 3, evolving: 3, canon: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2025_10_20_puls-msp-v-rossii-vipustili_1be131c3.md

## [2026-04-16 19:55] [ingest] | Инк./Дзен: Hi-Tech Mail survey — креаторская экономика РФ (аспирационные инфлюенсеры, affiliate, 1.57T ad market)
- source: wiki/sources/2026-04-16-dzen-inc-creator-economy-monetization-survey.md
- created:
  - wiki/evolving-strict/market-data/ru-creator-economy-monetization-survey-2026.md
  - wiki/evolving/industry-trends/ru-creator-economy-monetization-2026.md
- updated:
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md (Добавлена альтернативная оценка 2025 (широкий scope, Инк.): 1,57 трлн руб. +28% с разбором различий scope (узкий AdIndex vs широкий Инк. включая e-commerce media), замедление до +10-15% в 2026 подтверждается обоими источниками)
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md (Добавлен раздел «Аспирационный слой: массовое я инфлюенсер (РФ 2026)» — 79% думают о монетизации, 81% self-perception как инфлюенсер, 56% affiliate-preference, следствия для брендов (ценовое давление, affiliate-first кампании, поиск начинающих авторов))
  - wiki/canon/target-audience/gro-segments.md (Добавлен раздел «Adjacent market: аспирационный креаторский overlap с Сегментом 3» — 27% action-gap, content hook «монетизация контента как ремесло, не лотерея», anti-pattern «стать инфлюенсером за месяц»)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 2, evolving: 1, canon: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_dzen.ru_a_aeCZ85BYQg6Gi78G_1b5819ae.md (+.note.md, +.triage.json)

## [2026-04-16 19:55] [ingest] | Жажда: россияне, построившие бизнес за рубежом -- expat founder archetype (4 под-паттерна + 5 hooks)
- source: wiki/sources/2026-04-16-zhazhda-biz-lifestyle-rossijane-postroivshie-biznes-za-rubezhom.md
- created:
  - wiki/evolving/content-trends/ru-expat-founder-narrative-hooks.md
- updated:
  - wiki/evolving/content-trends/late-starter-founder-narrative-hooks.md (Добавлена секция "Пересечение с expat-архетипом" (Горяев как мост late-start × expat), cross-link на ru-expat-founder-narrative-hooks и вторичный источник rossijane-postroivshie-biznes-za-rubezhom.)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Обогащена запись про релокантскую подгруппу в "География" ссылкой на новый expat-founder-narrative-hooks архетип + добавлен источник.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, canon: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_rossijane-postroivshie-biznes-za-rubezhom_30ee5969.md

## [2026-04-16 19:55] [ingest] | Cossa vacancy 24231 (Internet Buyer) — scrape empty, audit stub
- source: wiki/sources/2026-04-16-www-cossa-ru-vacancies-24231-0dd4fb32.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.cossa.ru_vacancies_24231_0dd4fb32.md (+ .note.md, .triage.json)

## [2026-04-16 19:55] [ingest] | Дзен (vc.ru/ai): Gemini 3.1 Flash TTS — enrichment (ElevenLabs V3 benchmark + RU + AI Studio/API)
- source: wiki/sources/2026-04-16-dzen-vcru-gemini-3-1-flash-tts.md
- created: none
- updated:
  - wiki/volatile-strict/competitor-news/google-gemini-chrome-ai-2026-04.md (Добавлены 3 детали из Дзен-перепубликации: бенчмарк vs ElevenLabs V3, RU-поддержка, дистрибуция через Google AI Studio + API Gemini)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/web_dzen.ru_a_aeCuZIoRHWhcqfpH_02ca856b.md + sidecars

## [2026-04-16 19:55] [ingest] | Жажда: стоит ли покупать готовый бизнес — 5 методик оценки и buy-vs-build для SMB
- source: wiki/sources/2026-04-16-zhazhda-biz-lifestyle-stoit-li-pokupat-gotovyj-biznes-c44f319d.md
- created:
  - wiki/canon/marketing-frameworks/business-valuation-methods-smb.md
  - wiki/evolving/content-trends/ready-business-purchase-narrative-hooks.md
- updated:
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Добавлена секция «Buy-vs-build: альтернативный путь входа» с cross-links на 5 методик оценки и narrative hooks; уникальный GRO-угол: двух-горизонтный нарратив (рабочее время + DCF-оценка при exit).)
  - wiki/canon/marketing-frameworks/startup-capital-sources-classification.md (Добавлена секция «Альтернативный путь: купить уже готовое» как 6-й путь (инверсия вопроса «где взять деньги для запуска»); cross-links на валюационные методики и hooks «buy-vs-build».)
  - wiki/evolving/content-trends/founder-investor-decision-hooks.md (Добавлены cross-links на ready-business-purchase-narrative-hooks и business-valuation-methods как смежную ветвь (founder после «брать ли деньги» переключается на «а может, купить работающее»).)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_stoit-li-pokupat-gotovyj-biznes_c44f319d.md

## [2026-04-16 19:56] [ingest] | hr-portal.ru article про инфо/тех-обеспечение HR-систем — нерелевантно (audit-стаб)
- source: wiki/sources/2026-04-16-hr-portal-ru-article-dlya-chego-neobhodimo-informacionnoe-i-tehniche-5b185a05.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_dlya-chego-neobhodimo-informacionnoe-i-tehnicheskoe-_5b185a05.md

## [2026-04-16 19:56] [ingest] | hr-portal.ru: разделение управленческого труда — no relevant extractions (audit only)
- source: wiki/sources/2026-04-16-hr-portal-ru-article-razdelenie-mezhdu-rukovoditelyami-upravlencheskogo-t-b58d34a5.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_razdelenie-mezhdu-rukovoditelyami-upravlencheskogo-t_b58d34a5.md + 2 sidecars

## [2026-04-16 19:56] [ingest] | rb.ru Ingria VC Day 2016 (архив, no relevant extractions)
- source: wiki/sources/2026-04-16-rb-ru-ingria-invest-sessiya-2016.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_ingria_invest_sessiya_7b1298b0.md (+ 2 sidecars)

## [2026-04-16 19:56] [ingest] | hr-portal.ru: соц-псих методы управления кадрами (no relevant extractions)
- source: wiki/sources/2026-04-16-hr-portal-ru-article-socialno-psihologicheskie-metody-i-sposoby-upravleni-5a8a1ec4.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_socialno-psihologicheskie-metody-i-sposoby-upravleni_5a8a1ec4.md

## [2026-04-16 19:56] [ingest] | Дзен: Набиуллина — нехватка рабочей силы (дубликат vc.ru)
- source: wiki/sources/2026-04-16-dzen-vcru-nabiullina-labor-shortage.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_dzen.ru_a_aeC3lIoRHWhcqf3Z_88ce3214.md (+ .note.md, .triage.json)

## [2026-04-16 19:56] [ingest] | rb.ru «Придумай финтех» интенсив ВШЭ (архив, no relevant extractions)
- source: wiki/sources/2026-04-16-rb-ru-pridumay-fintech-hse.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_pridumay_fintech_1270941e.md (+ .note.md, .triage.json)

## [2026-04-16 19:56] [ingest] | Cossa vacancy 23613 (Директор по маркетингу) — empty scrape, no extractions
- source: wiki/sources/2026-04-16-www-cossa-ru-vacancies-23613-878daf9a.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.cossa.ru_vacancies_23613_878daf9a.md

## [2026-04-16 19:56] [ingest] | rb.ru: анонс семинара Сколтеха по ML — нерелевантно, audit-only
- source: wiki/sources/2026-04-16-rb-ru-skoltech-ml-workshop.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_skoltech_machine_learning_ddec0ad4.md (irrelevant, no layer pages)

## [2026-04-16 19:57] [ingest] | rb.ru: Faberlic FMCG-акселератор (audit-only, no relevant extractions)
- source: wiki/sources/2026-04-16-rb-ru-news-accelerator-fmcg-313a6c1f.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_accelerator-fmcg_313a6c1f.md*

## [2026-04-16 19:57] [ingest] | rb.ru: ДКК коливинг в Шанхае (2016) — no relevant extractions
- source: wiki/sources/2026-04-16-rb-ru-dkk-coliving-shanghai.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_dkk-coliving_26b9d284.md (+ .note.md + .triage.json)

## [2026-04-16 19:57] [ingest] | HR-Portal: совершенствование системы управления персоналом (no relevant extractions)
- source: wiki/sources/2026-04-16-hr-portal-personnel-management-system.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_sovershenstvovanie-sistemy-upravleniya-personalom-ce_0dff3e09.md

## [2026-04-16 19:57] [ingest] | Жажда: когда брать деньги инвестора — 2 canon-фреймворка (Бланк + 5 источников капитала) + narrative hooks для SMB-founder
- source: wiki/sources/2026-04-16-zhazhda-biz-lifestyle-kogda-brat-dengi-investora-2427f149.md
- created:
  - wiki/canon/marketing-frameworks/blank-when-to-raise-investment.md
  - wiki/canon/marketing-frameworks/startup-capital-sources-classification.md
  - wiki/evolving/content-trends/founder-investor-decision-hooks.md
- updated:
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Добавлена секция funding anti-pattern + cross-links на 3 новые страницы (blank/capital-sources/decision-hooks) + 2-й source в front-matter)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (Добавлены 2 cross-link на новые funding-frameworks в секции связанных страниц)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_kogda-brat-dengi-investora_2427f149.md + .note.md + .triage.json

## [2026-04-16 19:58] [ingest] | redrop tg_portnyaginlive_11124.jpg (декоративное фото, irrelevant, audit-only)
- source: wiki/sources/2026-04-14-tg-portnyaginlive-11124-photo.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/media/tg_portnyaginlive_11124.jpg

## [2026-04-16 19:58] [ingest] | Forbes.ru про Snap: 16% сокращение + акции +9% (investor-loop enrich)
- source: wiki/sources/2026-04-16-forbes-ru-snap-stock-9pct-ai-layoffs.md
- created: none
- updated:
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (Snap-секция обогащена операционными AI-метриками (65% кода, 1M+ запросов/мес), Q1-прогнозом (+12% до $1,5B), датой заявления; добавлен новый раздел "Investor-сигнал: рынок поощряет AI-layoffs" с petлёй обратной связи CEO→stock→peer-CEO; +2 новых content-hook)
  - wiki/evolving-strict/market-data/ai-driven-layoffs-2025-2026.md (Snap добавлен в таблицу публичных CEO-заявлений (4-й кейс, 2026-04-15); добавлено 4-е наблюдение про investor-loop (+8,7% акций на NYSE); content-hook обновлён на квартет цифр (10/7/20/16%))
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Hook 7 обогащён Snap-данными: квартет 10/7/20/16%, два новых под-hook (investor-loop и operational benchmark 65% кода))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, evolving-strict: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_www.forbes.ru_investicii_559249-akcii-snap-vyrosli-na-9-na-novostah-o-plan_72f92259.md + 2 sidecars

## [2026-04-16 19:58] [ingest] | hr-portal.ru: психология управления персоналом — irrelevant (textbook Маслоу без фактуры)
- source: wiki/sources/2026-04-16-hr-portal-psihologiya-upravleniya-personalom.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_psihologiya-effektivnogo-upravleniya-personalom_40bf6393.md (no relevant extractions)

## [2026-04-16 19:58] [ingest] | hr-portal.ru: Российский подход к управлению персоналом (irrelevant, audit-only)
- source: wiki/sources/2026-04-16-hr-portal-ru-article-rossiyskiy-podhod-k-organizacii-i-upravleniyu-person-4be786e3.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_rossiyskiy-podhod-k-organizacii-i-upravleniyu-person_4be786e3.md

## [2026-04-16 19:58] [ingest] | Секрет фирмы (2016) FDP guerrilla-реклама Berlin post-Brexit -- no relevant extractions
- source: wiki/sources/2026-04-16-secretmag-startups-london-berlin-brexit-2016.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_secretmag.ru_news_plakat-dnya-startapy-iz-londona-pozvali-v-berlin-posle-_3fd7d66d.md

## [2026-04-16 19:58] [ingest] | zhazhda.biz listicle «истории тех кто разбогател в школе» (no relevant extractions)
- source: wiki/sources/2026-04-16-zhazhda-istorii-razbogatel-v-shkole.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_istorii-teh-kto-razbogatel-eshhe-v-shkole_8376c62a.md

## [2026-04-16 19:58] [ingest] | Дзен/vc.ru Anthropic $800B + productivity study (4 enriched pages)
- source: wiki/sources/2026-04-16-dzen-vcru-anthropic-800b-productivity-study.md
- created: none
- updated:
  - wiki/volatile-strict/competitor-news/anthropic-800b-identity-verification-2026-04.md (Добавлены BI+Bloomberg как первичные источники раунда, Feb 2026 $380B baseline (>2x за 2 мес), nuance Bloomberg «компания отбивается от денег»)
  - wiki/evolving-strict/market-data/ai-labor-market-anthropic-2026.md (Добавлен новый Anthropic productivity study (100K anonymized Claude chats, +1.8%/год annual gain, медиана 80% экономии времени на задачу) + интерпретация counter-point к Goldman Sachs)
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md (Добавлен counter-point от Anthropic own study (+1.8%/год vs Goldman Sachs «нет связи»), разрешение через individual vs corporate layer)
  - wiki/evolving/content-trends/ai-product-engineer-content-hooks.md (Добавлен hook «80% vs 95% — разница между вами и компанией» (Anthropic 80% медиана vs Goldman Sachs 95% корп. пилотов неудачные))
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving-strict: 1, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_dzen.ru_a_ad_KSIoRHWhcqdK7_9a5f8540.md*

## [2026-04-16 19:58] [ingest] | Inc./Дзен: Nvidia × Cadence — симуляции для роботов + Cadence AI-агент для чип-дизайна на Google Cloud
- source: wiki/sources/2026-04-16-dzen-inc-nvidia-cadence-robot-simulation.md
- created:
  - wiki/volatile-strict/industry-news/ai-data-scarcity-nvidia-cadence-2026-04.md
- updated:
  - wiki/evolving/industry-trends/ai-value-migration-2026.md (Добавлено CEO-level подтверждение направления №4 (данные как узкое горлышко) — Хуанг/Девган на конференции Cadence 2026-04-16)
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md (Добавлен раздел §9 — Cadence AI-агент для EDA на Google Cloud как vertical-B2B agent-кейс в deep-B2B + self-reinforcing AI-for-AI messaging pattern)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_dzen.ru_a_aeC0JTljwSj4DNgN_0f14b956.md (+ .note.md, .triage.json sidecars)

## [2026-04-16 19:58] [ingest] | Cossa vacancy 20343 Digital-дизайнер (fetch empty, no extractions)
- source: wiki/sources/2026-04-16-www-cossa-ru-vacancies-20343-7764a36b.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.cossa.ru_vacancies_20343_7764a36b.md (+ .note.md, .triage.json)

## [2026-04-16 19:58] [ingest] | rb.ru Рыбаков Фонд — встречи стартапов (audit-only, no relevant extractions)
- source: wiki/sources/2026-04-16-rb-ru-news-rivakov-meetings-58257110.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_rivakov-meetings_58257110.md

## [2026-04-16 19:58] [ingest] | RB.RU backfill: School 42 Silicon Valley — нерелевантно GRO-домену
- source: wiki/sources/2026-04-16-rb-ru-silicon-valley-42-school.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_rb.ru_news_silicon_valley_besplatno_0f506f5b.md (+ .note.md, .triage.json)

## [2026-04-16 20:00] [ingest] | Дзен hh.ru: advertorial Карьерного маркетплейса — B2C-пивот hh.ru + Hook 11 для GRO
- source: wiki/sources/2026-04-16-dzen-hh-kareernyj-marketplace-checklist.md
- created:
  - wiki/evolving/competitor-positioning/hh-ru-career-marketplace.md
- updated:
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md (Добавлен Карьерный маркетплейс в таблицу экосистемы + отдельный раздел про B2C-пивот hh.ru (ранее вся экосистема была B2B-only))
  - wiki/evolving/content-trends/hh-ru-blog-content-patterns.md (Добавлен Формат 5 (Дзен-advertorial с per-channel промокодом) + обновлены мета-паттерн и значение для GRO (5 форматов, 4 B2B + 1 B2C))
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Добавлен Hook 11 (hh.ru 5-шаговый readiness-checklist как конкурентный anti-hook для дифференциации GRO) + пара Hook10+Hook11 как anti-consultancy комбо)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_dzen.ru_a_Zqt7MwVC8FJ6EeAT_3b1c0697.md (+sidecars .note.md, .triage.json) → status: processed

## [2026-04-16 20:00] [ingest] | zhazhda.biz блоги о бизнесе (~2015-2016): паттерн радикально-прозрачного founder-блога (Овчинников «Сила ума»)
- source: wiki/sources/2026-04-16-zhazhda-blogi-o-biznese.md
- created:
  - wiki/canon/marketing-frameworks/radical-transparency-founder-blog.md
- updated:
  - wiki/canon/marketing-frameworks/business-reality-show-format.md (Добавлен исторический предшественник — long-form радикально-прозрачный founder-блог Овчинникова «Сила ума» ~2006 как предтеча cohort-scaled реалити-формата)
  - wiki/evolving/content-trends/personal-brand-shift-2026.md (Добавлен раздел «Исторический контекст» с RU-прецедентом ~2006 (Овчинников) + cross-links на canon-страницы radical-transparency и business-reality)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_samye-samye-blogi-o-biznese_e44b74c2.md (+ .note.md, .triage.json)

## [2026-04-16 20:45] [ingest] | hr-portal.ru: определение системы управления персоналом (irrelevant — generic HR textbook)
- source: wiki/sources/2026-04-16-hr-portal-opredelenie-sistemy-upravleniya-personalom.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_opredelenie-znachenie-i-funkcii-sistemy-upravleniya-_f98f462a.md

## [2026-04-16 20:47] [ingest] | Inc./Дзен: Yandex AI Studio Academy + inventory 5 RU no-code AI-agent платформ
- source: wiki/sources/2026-04-16-dzen-inc-yandex-ai-academy-nocode-agents.md
- created:
  - wiki/evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-vertical-ai-signals-2026.md (Добавлен сигнал 7 (Yandex AI Studio Academy + inventory 4 RU no-code AI-agent конкурентов: Just AI / MWS / ГигаЧат / Nodul). Cross-source стало три (Цейтлин + Горный + Inc. Russia). Обновлён синтез 6→7 сигналов.)
  - wiki/evolving-strict/market-data/ru-corporate-ai-assistants-2026.md (Добавлена секция Качественный сигнал зрелости: BigTech запускает массовое обучение no-code AI-agent (апрель 2026), подтверждающий реальность оценки 30 млрд ₽)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, evolving-strict: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_dzen.ru_a_ad-554dP7i9xBots_96910d36.md

## [2026-04-16 20:51] [ingest] | tg_portnyaginlive_11126.jpg — duplicate audit (no extractions)
- source: wiki/sources/2026-04-16-tg-portnyaginlive-11126-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/media/tg_portnyaginlive_11126.jpg + .note.md sidecar

## [2026-04-16 20:55] [ingest] | Forbes Russia: МегаФон запустил MegaRITM — in-house CVM с GenAI (import-substitution + export plan)
- source: wiki/sources/2026-04-16-forbes-megafon-megaritm-cvm.md
- created:
  - wiki/volatile-strict/industry-news/megafon-megaritm-cvm-platform-2026-04.md
  - wiki/canon/marketing-frameworks/real-time-personalization-cvm-mechanics.md
- updated:
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (МегаФон MegaRITM добавлен как третий enterprise proof-point (после SuperJob 2026-04-07 и МТС 2026-04-14) — нарратив "AI в production РФ" теперь подкреплён тремя случаями за 9 дней)
  - wiki/evolving-strict/market-data/ru-business-ai-adoption-2026.md (Добавлен § 4a — MegaRITM как concrete production-datapoint (500M/мес, 1500 rps, 100+ сценариев, 4 канала), cross-table расширен)
  - wiki/evolving/industry-trends/b2b-ai-adoption-fte-kpi-2026.md (Добавлен блок "Production-proof от МегаФона" — MegaRITM как иллюстрация FTE-эффекта в маркетинге и import-substitution на 2-й→3-й ступени лестницы Егошина)
  - wiki/evolving/industry-trends/ru-ai-national-strategy-2026.md (Добавлен раздел "Import-substitution в MarTech-стеке — кейс МегаФона MegaRITM" как production-proof пунктов 3 (фронтальное применение) и 7 (международная экспансия) совещания у Президента)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, canon: 1, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_www.forbes.ru_novosti-kompaniy_559203-megafon-razrabotal-platformu-dla-pod_33ff2867.md (+.note.md +.triage.json)

## [2026-04-16 21:40] [ingest] | Inc./Дзен: Рокет Контрол раскрыл финансы — industrial vertical AI РФ выходит в измеримую экономику
- source: wiki/sources/2026-04-16-dzen-inc-rocket-control-industrial-ai-roi.md
- created:
  - wiki/evolving-strict/competitor-metrics/rocket-control-industrial-ai-2026.md
  - wiki/evolving/industry-trends/industrial-ai-measurable-roi-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-vertical-ai-signals-2026.md (Добавлен Сигнал 8 — Рокет Контрол (industrial vertical AI, первый public-financials кейс РФ); расширен синтез до восьми сигналов и обновлены gaps)
  - wiki/evolving-strict/market-data/ru-corporate-ai-assistants-2026.md (Добавлен bottom-up proof-point: Рокет Контрол с раскрытыми финансами как первый RU vertical AI игрок, подтверждающий не-фантомность оценки 30 млрд ₽)
  - wiki/evolving/industry-trends/b2b-ai-adoption-fte-kpi-2026.md (Добавлен параллельный сдвиг в industrial AI — ROI-метрики вместо технологии (Рокет Контрол как industrial-flavour проекция того же тренда клиент-требует-измеримой-экономики))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 3, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_dzen.ru_a_ad_O_zljwSj4C7ic_178bbe6b.md* (primary + .note.md + .triage.json)

## [2026-04-16 21:41] [ingest] | secretmag 2016: RU internet platforms NHT verification (Comscore/Moat) — историческая точка отсчёта ad-quality
- source: wiki/sources/2026-04-16-secretmag-vedomosti-runet-ad-verification-2016.md
- created:
  - wiki/canon-strict/historical-campaigns/ru-ad-quality-verification-2016.md
- updated:
  - wiki/evolving/industry-trends/ai-marketing-limits-2026.md (Добавлена секция исторического контекста bot-traffic в Рунете со ссылкой на snapshot 2016 (Rambler 1,8%, Yandex 0,3% vs US 6%, world >9%); обновлён sources и связанные страницы.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, evolving: 1, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/web_secretmag.ru_news_vedomosti-internet-ploshadki-runeta-proveryayut-kachest_223a19d5.md (+ .note.md + .triage.json)

## [2026-04-16 22:02] [ingest] | TG Тинькофф Бизнес #10555 (audio, irrelevant)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10555.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/audio/tg_tinkoffbank_10555.ogg (+ .audio.mp3, .note.md, .transcript.md)

## [2026-04-16 22:05] [ingest] | zhazhda.biz: бесплатный PR для SMB — критерии инфоповода + 2 кейс-стади + Евросеть 2007
- source: wiki/sources/2026-04-16-zhazhda-biz-lifestyle-rasskazhite-o-moem-biznese.md
- created:
  - wiki/canon/marketing-frameworks/infopovod-criteria-smb-pr.md
  - wiki/canon/marketing-frameworks/outlier-content-pr-case-studies.md
- updated:
  - wiki/canon/marketing-frameworks/benetton-toscani-provocative-advertising.md (Добавлен русский parallel: кейс Евросеть 2007 (Чичваркин, «цены просто ох…ть», 10k USD бюджет → 2.5x оборот) + сравнительная таблица ценностная vs языковая провокация.)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Добавлен бесплатный PR-канал (инфоповоды + outlier content) как прикладной совет сегменту и awareness-рычаг ГРО.)
  - wiki/canon/marketing-frameworks/performance-pr-framework.md (Добавлены cross-links на новые страницы инфоповодов (upstream для performance PR) и outlier content PR.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_rasskazhite-o-moem-biznese_370b1ee0.md (+ .note.md, .triage.json)

## [2026-04-16 22:20] [ingest] | vc.ru/Дзен: Apple Siri AI coding course + Claude Code enterprise adoption (The Information)
- source: wiki/sources/2026-04-16-dzen-vcru-apple-siri-ai-coding-course.md
- created: none
- updated:
  - wiki/volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1.md (Добавлена timeline-entry 2026-04-16 (Apple Siri AI coding course + Claude Code enterprise budgets) + 3-й пункт синтеза «Enterprise-adoption закрепляется»)
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md (Добавлен 4-й натурный data-point (Apple Siri retraining) — другой тип сигнала (признание investment phase, не провал/flat), сильный consumer-сигнал про Claude Code как enterprise-standard даже для Apple)
  - wiki/evolving/industry-trends/ai-knowledge-worker-climb-2025-2026.md (Обновление 2026-04-16 к Сигналу 3: Apple как enterprise-validation — формальный курс по ИИ-программированию + значительные бюджеты на Claude Code в консервативной компании = middle-skill → orchestrator переход становится required enterprise skill; разрыв adoption внутри Apple = тот же J-curve паттерн в миниатюре)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_dzen.ru_a_aeCcOIoRHWhcqfPM_b73a406d.md (+.note.md, +.triage.json)

## [2026-04-17 05:39] [ingest] | tg_portnyaginlive_11166.mp4 — duplicate audit (no extractions)
- source: wiki/sources/2026-04-17-tg-portnyaginlive-11166-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/video/tg_portnyaginlive_11166.mp4 (+ .audio.mp3, .bundle.json, .note.md, .transcript.md)

## [2026-04-17 05:42] [ingest] | tg_portnyaginlive_11173.mp4 — duplicate audit (no extractions)
- source: wiki/sources/2026-04-17-tg-portnyaginlive-11173-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/video/tg_portnyaginlive_11173.mp4

## [2026-04-17 05:45] [ingest] | TG @portnyaginlive #11128 (фото, дубль Good Vibes, irrelevant)
- source: wiki/sources/2026-04-17-tg-portnyaginlive-11128-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/media/tg_portnyaginlive_11128.jpg + .note.md + .bundle.json sidecars

## [2026-04-17 05:45] [ingest] | TG @tinkoffbank #10539-10543: Т-Инвестиции ТОЛК.PRO hybrid-event с 4 мировыми спикерами (Schwager/Varoufakis/King/Williams) + промокод MART -30% на брокерские тарифы
- source: wiki/sources/2026-04-17-tg-tinkoffbank-10539-tolk-pro-speakers.md
- created:
  - wiki/canon-strict/historical-campaigns/tbank-tinvest-tolk-pro-2026-04.md
  - wiki/evolving/content-trends/event-speaker-carousel-format.md
  - wiki/evolving/competitor-positioning/tbank-tinvest-premium-positioning.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/media/tg_tinkoffbank_10539.jpg + 4 children (10540..10543) with .note.md sidecars

## [2026-04-17 05:48] [ingest] | TG @tinkoffbank #10575 — 100% кэшбэк на яйца (olive-green sub-palette Easter piggyback)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10575-egg-cashback-olive.md
- created: none
- updated:
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (Добавлен #10575 olive-green BG alt-palette (6-й режим), расширена таблица 9 observed режимов, body-текст описывает новый dated-badge UX-pattern)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/media/tg_tinkoffbank_10575.jpg (+ .bundle.json, .note.md)

## [2026-04-17 05:50] [ingest] | TG @tinkoffbank #10537 — Т-Страхование ВЗР POLETELI промо-bundle (sweepstake + promocode + emoji-poll opener)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10537-vzr-poleteli.md
- created:
  - wiki/canon-strict/historical-campaigns/tbank-t-insurance-poleteli-vzr-q1-2026.md
  - wiki/evolving/content-trends/sweepstake-promocode-combo-mechanics.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен Exemplar «emoji-poll softener перед hard-sell промо» — второй observed случай emoji-poll-opener в RU-бренд-каналах после priming-серии @hh_ru_official (разный масштаб применения одного примитива))
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/media/tg_tinkoffbank_10537.jpg + 10538.jpg + 3 sidecars (.note.md ×2, .bundle.json)

## [2026-04-17 05:50] [ingest] | TG @tinkoffbank #10544 — анонс сервиса «Сделка» (escrow для недвижимости, freemium 500k-100M ₽)
- source: wiki/sources/2026-04-17-tg-tinkoffbank-10544-sdelka-realty.md
- created:
  - wiki/canon-strict/historical-campaigns/tbank-sdelka-real-estate-escrow-launch-2026.md
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md
- updated:
  - wiki/evolving/industry-trends/tbank-corporate-platform-stack-2026.md (Добавлен раздел «Сделка» — escrow-вертикаль для недвижимости (2026-04): 4-я вертикаль стека после Time/Селлер/дофамин-банкинга, freemium-позиция против 0,1–0,5% комиссии конкурентов, roadmap на авто/землю/гаражи)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен раздел «Exemplar: minimalist product-launch без sweepstakes» с разбором поста @tinkoffbank #10544 — контраст с POLETELI: «Запустили» как совершённое действие, roadmap-hook вместо urgency, минимализм → signal product confidence; адаптация для GRO product-launch)
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, evolving: 3, sources: 1}
- touched: 5 pages
- raw: raw/processed/media/tg_tinkoffbank_10544.jpg (+ .bundle.json, .note.md sidecars)

## [2026-04-17 05:50] [ingest] | TG @tinkoffbank #10158 — Т-Страхование ВЗР POLETELI промо-bundle (sweepstake + promocode + emoji-poll opener)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10567-utair-closed-sale.md
- created:
  - wiki/evolving/content-trends/tier-gated-discount-upsell-hook.md
- updated:
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (Добавлен #10567 Utair как partner-color override variant (yellow-block уступает partner-brand orange+blue, pill-tags вместо bottom-yellow-block); расширен вывод о family of templates внутри consumer-yellow bucket)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, sources: 1}
- touched: 3 pages
- raw: raw/processed/media/tg_tinkoffbank_10567.jpg (+ .bundle.json, .note.md)

## [2026-04-17 05:52] [ingest] | TG @tinkoffbank #10577 (bundle +5 children) — Т-Образование math-course + UGC testimonial carousel pattern
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10577-t-education-math-course.md
- created:
  - wiki/evolving/content-trends/ugc-testimonial-carousel-arc.md
- updated:
  - wiki/evolving/industry-trends/tbank-corporate-platform-stack-2026.md (Добавлен раздел Т-Образование + Т-Путешествия как B2C non-financial brand-extensions, наследующие consumer-yellow (vs B2B sub-brands с distinct palettes))
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (Добавлена adjacent-UI demo hero variation (#10577) в 9-режимную матрицу yellow-block-протокола + sources/Связанные)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/media/tg_tinkoffbank_10577.jpg + 5 children (10578-10582) + sidecars

## [2026-04-17 05:55] [ingest] | TG @tinkoffbank #10546 — YT-шоу «Звёзды против мошенников» → branded-show-format + YT-thumbnail counter-example
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10546-stars-vs-fraudsters.md
- created:
  - wiki/evolving/content-trends/branded-show-format-t-bank-stars-vs-fraudsters.md
- updated:
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (Добавлена секция Counter-example: YouTube thumbnail (#10546 «Stars vs Fraudsters») сознательно ломает yellow-block-шаблон в пользу YouTube-формулы (крупные лица + эмоциональный speech-bubble + 3D-типография). Вывод: T-Bank применяет by-channel визуальный протокол, не один template.)
  - wiki/evolving/content-trends/entertainment-over-pain-framing.md (Добавлена секция Real-world brand example: T-Bank «Звёзды против мошенников» (2026) как concrete-иллюстрация entertainment-рамки над anti-fraud CSR-темой (обычно pain-killer). Показывает, что даже «защитные» topics можно переупаковать в entertainment, если найти game-механику и celebrity-functional-role.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/media/tg_tinkoffbank_10546.jpg (+ .bundle.json, .note.md)

## [2026-04-17 05:55] [ingest] | TG @tinkoffbank #10583 — Т-Путешествия лето (countdown-copy + lifestyle-hero + 2×2 tier-matrix)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10583-summer-hotel-pool-glasses.md
- created: none
- updated:
  - wiki/evolving/content-trends/tier-gated-discount-upsell-hook.md (Добавлен variant E: 2×2 tier-matrix (подписка × booking-recency) — эволюция механики от linear 2 tier до multi-dimensional loyalty matrix)
  - wiki/evolving/content-trends/urgency-window-launch-playbook.md (Добавлен раздел Sibling-technique — countdown-copy как single-post alternative full urgency-window playbook (natural anchor vs artificial close))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, sources: 1}
- touched: 3 pages
- raw: raw/processed/media/tg_tinkoffbank_10583.jpg (+ .bundle.json, .note.md)

## [2026-04-17 06:00] [ingest] | TG @tinkoffbank #10570 — Платинум wildlife-карты с metaphor-caption
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10570-platinum-wildlife.md
- created:
  - wiki/evolving/content-trends/metaphor-reframing-utility-hook.md
  - wiki/evolving/content-trends/collectible-card-design-fintech.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, sources: 1}
- touched: 3 pages
- raw: raw/processed/media/tg_tinkoffbank_10570.jpg (+ .bundle.json, .note.md)

## [2026-04-17 06:00] [ingest] | TG @portnyaginlive #11131 — duplicate audit (Lenin meme OCR, no extractions)
- source: wiki/sources/2026-04-17-tg-portnyaginlive-11131-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/media/tg_portnyaginlive_11131.jpg (+ .note.md, .bundle.json)

## [2026-04-17 06:05] [ingest] | TG @portnyaginlive #11132 (фото, дубль Manul/WHERE TO EAT shortlist, irrelevant)
- source: wiki/sources/2026-04-17-tg-portnyaginlive-11132-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/media/tg_portnyaginlive_11132.jpg (+ .note.md, .bundle.json) — MD5-duplicate of already-processed tg_portnyaginlive_11132 (1).jpg

## [2026-04-17 06:10] [ingest] | TG @tinkoffbank #10547 — GAC S7 × T-Premium GWP → T-Premium palette + gift-with-purchase framework
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10547-gac-tpremium-partnership.md
- created:
  - wiki/evolving/competitor-positioning/tbank-premium-sub-brand-palette.md
  - wiki/evolving/content-trends/gift-with-purchase-premium-bundling.md
- updated:
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (Добавлен cross-link на T-Premium palette как третью визуальную подсистему T-Bank ecosystem (после consumer-yellow и tinvest-violet).)
  - wiki/canon/marketing-frameworks/partnerships-growth-multiplier.md (Добавлена секция Concrete B2C partnership mechanic — Gift-with-Purchase с base-кейсом T-Bank × GAC S7. Cross-link на новый фреймворк gift-with-purchase-premium-bundling.)
  - wiki/evolving/competitor-positioning/tbank-tinvest-premium-positioning.md (Добавлен четвёртый sub-бренд T-Premium в секцию Related streams у Т-Банка + cross-link на визуальную палитру.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, canon: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/media/tg_tinkoffbank_10547.jpg (+ .bundle.json, .note.md)

## [2026-04-17 06:10] [ingest] | TG @tinkoffbank #10572 — Кэшбэк 100% typographic-hero (wave 2 of #10557 campaign)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10572-cashback-100-typographic.md
- created:
  - wiki/evolving/content-trends/multi-touch-creative-cadence.md
- updated:
  - wiki/evolving/content-trends/daily-streak-gamification-in-finance.md (Добавлен блок Multi-touch creative-strategy — #10572 как wave 2 той же кампании подтверждает disciplined multi-touch pattern для streak-акций; таблица wave 1 vs wave 2 и implication для GRO)
  - wiki/sources/2026-04-14-tg-tinkoffbank-10557-daily-cashback-streak.md (Backlink на #10572 (wave 2) и multi-touch-creative-cadence в секции Связанные страницы)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/media/tg_tinkoffbank_10572.jpg (+ .bundle.json, .note.md)

## [2026-04-17 06:10] [ingest] | tg_portnyaginlive — bulk-дубль 13 постов (10 фото + 3 видео; 29 файлов, audit-only, no extractions)
- source: wiki/sources/2026-04-17-tg-portnyaginlive-bulk-duplicate-batch.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/media/ (10 primaries: 11127, 11133, 11135, 11136, 11137+4children, 11145+8children, 11155+1child, 11157, 11164, 11165) + raw/processed/video/ (3 primaries: 11167, 11168, 11169+3children) + all sidecars = 29 файлов

## [2026-04-17 06:15] [ingest] | TG @tinkoffbank #10545 — видео-тизер к Satir-эпизоду Stars-vs-Fraudsters (pathos + scam-reenactment + two-touch launch)
- source: wiki/sources/2026-04-17-tg-tinkoffbank-10545-satir-meter-scam-teaser.md
- created:
  - wiki/evolving/content-trends/short-form-teaser-for-branded-show.md
- updated:
  - wiki/evolving/content-trends/branded-show-format-t-bank-stars-vs-fraudsters.md (Добавлены секции: (1) two-touch launch tactic (video-teaser #10545 → thumbnail #10546 back-to-back); (2) pathos-layer в casting и content (actor-level role-play-adaptability, не только speech-удержание); (3) scam-reenactment как content-substance (пломба-скам, каталог узнаваемых RU-схем как long-tail серии))
  - wiki/evolving/content-trends/entertainment-over-pain-framing.md (Добавлена подсекция «Pathos-layer: entertainment-рамка включает эмоциональную уязвимость, не только humor» — entertainment ≠ humor, включает pathos/drama/vulnerability как pull-hooks; расширение GRO-выводов (pull-hook через cliffhanger-эмоцию, real scenarios over abstract messaging))
  - wiki/evolving/content-trends/multi-touch-creative-cadence.md (Добавлена секция «Immediate-stacking tactic — complementary pattern» с таблицей сравнения spaced-repetition (Кэшбэк 100%) vs immediate-stacking (Satir teaser→thumbnail). Обобщён фреймворк: оба паттерна — формы multi-touch, выбор зависит от episode-vs-running, pull-vs-push, video-vs-static.)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлена подсекция «Exemplar: native video-teaser к YT-эпизоду branded-show» — TG как video-first platform для крупных брендов, per-platform cut-down из длинного YT-контента, pull-hook native video + no-CTA caption)
  - wiki/sources/2026-04-14-tg-tinkoffbank-10546-stars-vs-fraudsters.md (Добавлен link на #10545 как pair-post (video-тизер того же эпизода, publish back-to-back). Добавлен link на новую страницу short-form-teaser-for-branded-show.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, sources: 2}
- touched: 7 pages
- raw: raw/processed/video/tg_tinkoffbank_10545.mp4 (+.audio.mp3, .bundle.json, .note.md, .transcript.md)

## [2026-04-17 06:25] [ingest] | TG @tinkoffbank #10557 — Кэшбэк дня (streak UX) → daily-streak-gamification + safety-board-meme-inversion-hook
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10557-daily-cashback-streak.md
- created:
  - wiki/evolving/content-trends/daily-streak-gamification-in-finance.md
  - wiki/evolving/content-trends/safety-board-meme-inversion-hook.md
- updated:
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (Добавлен #10557 как четвёртый наблюдаемый экземпляр канонического yellow-block-шаблона (возврат к эталону после двух отклонений #10546 YT и #10547 T-Premium). Обновлены sources и related-links.)
  - wiki/canon/marketing-frameworks/cross-industry-pattern-borrowing.md (Добавлена секция Пример 2026: T-Bank Кэшбэк дня как перенос streak+lock UX из fitness/gaming в banking. Иллюстрирует Petrochenkov-эвристику на свежем 2026-кейсе.)
  - wiki/evolving/industry-trends/whoop-retention-case-2026.md (Добавлена секция Cross-industry миграция паттерна: fintech (T-Bank) заимствует streak-механику из fitness (Whoop-оригинал). Замкнут цикл: fitness-UX → consumer-привычка → banking re-use. Переносимость на GRO как fitness-home.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, canon: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/media/tg_tinkoffbank_10557.jpg (+ .bundle.json, .note.md)

## [2026-04-17 06:35] [ingest] | TG @tinkoffbank #10558–10563 — BNPL Доли × 5 fashion-partners (album creative template + lavender sub-brand palette)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10558-doli-fashion-album.md
- created:
  - wiki/evolving/competitor-positioning/tbank-doli-bnpl-partner-album-format.md
  - wiki/evolving/competitor-positioning/tbank-doli-bnpl-sub-brand-palette-lavender.md
- updated:
  - wiki/evolving/competitor-positioning/tbank-premium-sub-brand-palette.md (Расширена матрица с 4 до 5 sub-brand palettes (добавлены Доли lavender и уточнён Т-Бизнес beige/tan вместо чёрного/красного), введена новая axis emotional-registry.)
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (Добавлено подтверждение 5 sub-brand palettes в T-Bank group; consumer-yellow переопределён как один из пяти coexisting протоколов.)
  - wiki/canon/marketing-frameworks/partnerships-growth-multiplier.md (Добавлен раздел «Concrete B2C mechanic — BNPL Partner-Album» с base-case Доли × 5 fashion brands + сравнительная таблица с GWP-механикой (marginal cost добавления партнёра).)
  - wiki/evolving/industry-trends/tbank-corporate-platform-stack-2026.md (Добавлен раздел «Доли — 5-й sub-brand в портфеле T-Bank group», зафиксирован expansion ecosystem-narrative от 4 до 5 distinct palettes и emotion-registries.)
- superseded:
  - wiki/evolving/competitor-positioning/tbank-premium-sub-brand-palette.md (было «Т-Бизнес — чёрный/красный B2B-эстетика»; теперь beige/tan + 3D-office-realism)
- sensitive flag: none
- layer-touched: {evolving: 5, canon: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/media/tg_tinkoffbank_10558.jpg* + 5 children (10559–10563) with .note.md sidecars + .bundle.json → status: processed

## [2026-04-17 06:36] [ingest] | TG @tinkoffbank #10565 — ТОЛК-2026 threshold-merch teaser (engagement-механика + community-sourced mascot pipeline)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10565-tolk-cat-merch-threshold.md
- created:
  - wiki/evolving/content-trends/threshold-contingent-merch-activation.md
  - wiki/evolving/content-trends/community-sourced-mascot-mockup.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, sources: 1}
- touched: 3 pages
- raw: raw/processed/media/tg_tinkoffbank_10565.jpg* + .note.md + .bundle.json → status: processed

## [2026-04-17 06:37] [ingest] | TG @tinkoffbank #10566 — Т-Бизнес SMB-support defensive move (VAT-compensation H1 2026)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10566-tbiznes-vat-compensation-2026.md
- created:
  - wiki/evolving/competitor-positioning/tbiznes-smb-support-defensive-positioning-2026.md
  - wiki/volatile-strict/competitor-news/tbiznes-vat-compensation-offer-2026-h1.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, volatile-strict: 1, sources: 1}
- touched: 3 pages
- raw: raw/processed/media/tg_tinkoffbank_10566.jpg* + .note.md + .bundle.json → status: processed

## [2026-04-17 05:45] [ingest] | TG @tinkoffbank #10574 — второй эпизод «Звёзды против мошенников» (Щербаков), serialization формата branded-show подтверждена
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10574-scherbakov-stars-vs-fraudsters.md
- created: none
- updated:
  - wiki/evolving/content-trends/branded-show-format-t-bank-stars-vs-fraudsters.md (Добавлен episode 2 (Щербаков), serialization подтверждена, functional-casting pattern обобщён, episode-differentiation hook-pattern)
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (Добавлен #10574 как второй YT-thumbnail counter-example (template YT-formula) + sources list)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, sources: 1}
- touched: 3 pages
- raw: raw/processed/media/tg_tinkoffbank_10574.jpg (+ .bundle.json, .note.md)

## [2026-04-17 05:50] [ingest] | tg_portnyaginlive 11158-11161 — bundle-дубль 4 видео (audit-only, no extractions)
- source: wiki/sources/2026-04-17-tg-portnyaginlive-11158-11161-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/video/tg_portnyaginlive_11158.mp4 + 3 children (11159, 11160, 11161) + sidecars

## [2026-04-17 07:45] [ingest] | TG @tinkoffbank #10568 — AcademeG ambassador how-to video + «Город» consumer-superapp layer + multi-merchant partnership mechanic
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10568-academeg-fuel-cashback.md
- created:
  - wiki/evolving/content-trends/ambassador-product-demo-hybrid.md
  - wiki/evolving/content-trends/dual-modality-video-text-tutorial.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен новый exemplar-блок «ambassador how-to video + dual-modality caption» (T-Bank AcademeG 35-сек) + cross-links на две новые content-trend страницы.)
  - wiki/evolving/industry-trends/tbank-corporate-platform-stack-2026.md (Добавлен новый раздел «Город — consumer-superapp layer с merchant-backend»: T-Bank «Город» → «Топливо» × N АЗС (Газпромнефть/Татнефть/Teboil/Нефтьмагистраль) как horizontal multi-merchant integration; ecosystem-sequence расширен.)
  - wiki/canon/marketing-frameworks/partnerships-growth-multiplier.md (Добавлена третья consumer-partnership механика — Multi-Merchant Superapp Backend (base-кейс T-Bank «Город» → «Топливо»); обновлена сравнительная таблица до трёх механик (GWP, BNPL Album, Superapp Backend).)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, canon: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/video/tg_tinkoffbank_10568.mp4 (+ .audio.mp3, .bundle.json, .note.md, .transcript.md)

## [2026-04-17 07:50] [ingest] | TG @tinkoffbank #10573 — «авиарежим» comedy skit (sell-free branded entertainment extreme)
- source: wiki/sources/2026-04-14-tg-tinkoffbank-10573-aviarezhim-comedy-sketch.md
- created:
  - wiki/evolving/content-trends/sell-free-branded-entertainment.md
- updated:
  - wiki/evolving/content-trends/entertainment-over-pain-framing.md (Добавлен sell-free extreme как третье расширение рамки (после humor-layer + pathos-layer): таблица трёх регистров (product-demo / teaser / sell-free) с base-кейсами из @tinkoffbank, cross-link на новую страницу.)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен новый exemplar-блок «sell-free branded comedy skit» (#10573 38-сек) + обновлён updated-комментарий; список связанных страниц расширен.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/video/tg_tinkoffbank_10573.mp4 (+ .audio.mp3, .bundle.json, .note.md, .transcript.md)

## [2026-04-27 15:50] [ingest] | TG @startupoftheday — дамп 22 постов apr 15-27 (candidate-side AI, FirmPilot, ALSO, CBInsights 65% AI, Невидимый ИИ thesis)
- source: wiki/sources/2026-04-27-tg-startupoftheday-apr-15-27-2026.md
- created:
  - wiki/evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd.md
  - wiki/evolving-strict/market-data/ru-saas-rating-2025.md
  - wiki/volatile-strict/industry-news/also-electric-bike-delivery-2026-04.md
  - wiki/evolving/industry-trends/candidate-side-ai-services-2026.md
  - wiki/evolving/competitor-positioning/firmpilot-ai-marketing-vertical-2026.md
  - wiki/evolving/industry-trends/ai-vertical-services-vc-uplift-2026.md
  - wiki/evolving/industry-trends/autonomous-delivery-vehicle-classification-2026.md
  - wiki/evolving/content-trends/invisible-ai-paradox-gorny-hook.md
  - wiki/evolving/content-trends/weekly-news-roundup-yt-format-gorny.md
  - wiki/evolving/content-trends/tg-comment-spam-defense-2026.md
  - wiki/evolving/industry-trends/influencer-marketplace-failure-paradox.md
- updated:
  - wiki/evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026.md (Добавлена секция Just AI Agent Platform Cloud (apr 2026 advertorial, drag-and-drop, готовые коннекторы CRM/CMS, free→paid tiers) + сигнал второй advertorial Just AI в @startupoftheday + OCR креатива)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Добавлен Hook 13 — «AI делает за тебя резюме, отклики и переписку с рекрутером — за 10% годового дохода» (Горный thesis); cross-link на новую страницу candidate-side-ai-services-2026; обновлён маппинг hook'ов на воронку)
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md (Добавлен 5-й data-point — Горный «Невидимый ИИ» с feedback-loop объяснением макро-парадокса (вместо чисто J-curve): near-customer оптимизация быстрая, backoffice — zero-sum + удар по покупательной способности)
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлена секция Operational hint: @Webpagebot для refresh URL-preview в TG (30K MAU, скрытый), 3 cross-link на новые страницы (weekly-news-roundup, tg-comment-spam-defense, sources/2026-04-27))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 8, evolving-strict: 2, volatile-strict: 1, sources: 1}
- touched: 16 pages
- raw: raw/processed/articles/tg_startupoftheday_20260427-152915.md + 3 children (5018, 5022, 5026 .jpg) with .note.md sidecars + .bundle.json absent (no prepare run)

## [2026-04-30 09:36] [ingest] | TG @grebenukm — дамп 21 пост apr 16-29 (СП-модель, 5 единичек, north star Аномалии, Декларация сезон 2)
- source: wiki/sources/2026-04-30-tg-grebenukm-apr-16-29-2026.md
- created:
  - wiki/canon/marketing-frameworks/grebenyuk-5-edinichek-framework.md
  - wiki/canon/marketing-frameworks/grebenyuk-jv-distribution-model.md
  - wiki/canon/marketing-frameworks/speed-vs-precision-smb-framework.md
  - wiki/evolving/content-trends/accountability-reality-show-format.md
- updated:
  - wiki/evolving/competitor-positioning/grebenyuk-anomaly-community.md (Апдейт апр 2026: north star metric Аномалии (количество аномалий/мес), планка 50K подписчиков оказалась сложной, кластер 1M+/10M+ дохода, ЕС-клиника запуск летом, личный бренд перезапуск, «Декларация» сезон 2 анонс, fan-made Dota 2 мем-коллажи как сигнал зрелости бренда)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_grebenukm_20260430-093103.md + 12 children (6 media, 5 video, 2 audio) with sidecars

## [2026-04-30 09:40] [ingest] | GRO — лендинг groapp.ru/#download, срез 2026-04-30 (re-read, без изменений)
- source: wiki/sources/2026-04-30-groapp-landing-refresh.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 0, sources: 1}
- touched: 1 pages
- raw: raw/links.md#https://groapp.ru/#download — уже status: processed (первичный ingest 2026-04-10), новая source-страница создана как snapshot-audit

## [2026-05-05 15:38] [ingest] | TG @addmeto — повторный backfill-дамп идентичен 2026-04-14 (no new extractions)
- source: wiki/sources/2026-05-05-tg-addmeto-jul2025-mar2026-redump.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/tg_addmeto_20260505-135420.md (+ .note.md, .triage.json, .bundle.json) + 47 media children → raw/processed/media/

## [2026-05-05 15:54] [ingest] | TG @ai_newz — дамп 50 постов apr 4-may 4 (Q2 follow-up): Anthropic compute crunch + xAI compute rental + Yandex MiniLED Alice + LLM resume self-preference bias
- source: wiki/sources/2026-05-05-tg-ai-newz-apr-may-2026.md
- created:
  - wiki/volatile-strict/industry-news/llm-self-preference-resume-bias-2026.md
  - wiki/volatile-strict/competitor-news/yandex-tv-station-miniled-alice-2026.md
  - wiki/volatile/weekly-digest/ai-industry-news-w15-w18-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (Добавлены Anthropic compute crunch update (pricing revolt 15.04 + Claude Code Pro exclusion test 22.04 + postmortem 24.04, цены ×2-3 для активных) и xAI neocloud entry update (Cursor — первый клиент 16.04, опция SpaceX-Cursor $60B 22.04, или $10B компенсация при отказе))
  - wiki/volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05.md (Добавлен Anthropic Claude Code postmortem (24.04.2026): 3 признанные проблемы (reasoning effort high→medium, thinking-cut при простое >1ч, cost-cut промпт), Codex выручка ×2 за неделю (по @ai_newz #116 4.05), gamification feature pets (1.05) — стратегические priorities OpenAI vs Anthropic расходятся (UX vs core capability))
  - wiki/volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026.md (Добавлен fourth-source attestation от @ai_newz пост 4519 (7.04.2026): Mythos API цена $25/$125 за миллион токенов подтверждена, $100M кредитов на аудит для 40+ организаций; связь с compute-crunch (Anthropic premium pricing на Mythos + cost-rationing на Claude Code = два проявления одного экономического сжатия))
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md (Добавлен add-on W15-W18 (13.04 - 4.05): Opus 4.7 (3x вижен resolution), GPT 5.5 ($5/$30 base, $30/$180 Pro), ChatGPT Images 2.0 (thinking, до 8 картинок, 2K через API), ChatGPT Pro $100 (5x Codex), Qwen 3.6 35B-A3B + 27B, Kimi K2.6 (300 субагентов), DeepSeek V4 Pro 1.6T-A49B + Flash 284B-A13B (KV-кэш ×10 меньше), Xiaomi MiMo V2.5 (1.02T-A42B + 310B-A15B мультимодальная MIT), Mistral Medium 3.5 dense 128B 256k, Talkie LLM 1930, Baidu ERNIE Image 8B Apache 2.0, Sber Kandinsky 6.0 Image Pro (Image RAG + +40% MoE), Anthropic Claude Design, xAI Compute Rental, HF Kernels)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Добавлен Hook 14 — «AI-нарциссизм / self-preference bias» с двумя hook-формулировками (резюме на той же модели проходит на 20-60% чаще), cross-link на новую страницу llm-self-preference-resume-bias-2026, обновлён маппинг hook-ов на воронку)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 4, volatile: 1, evolving: 2, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_ai_newz_20260505-135940.md + 39 children (32 media, 7 video) with sidecars (.bundle.json, .note.md, .triage.json, .audio.mp3, .transcript.md где есть)

## [2026-05-05 15:55] [ingest] | TG @alexander_visotsky — дамп 50 постов 2026-04-12..05-05 (Claude Cowork narrative, Алексей FoodLab кейс, Platform feature deep-dive, IQ ≥120 hiring, plastic-AI-content)
- source: wiki/sources/2026-05-05-tg-alexander-visotsky-apr-may-2026.md
- created:
  - wiki/evolving/content-trends/visotsky-ai-personal-assistant-narratives.md
  - wiki/volatile-strict/competitor-news/business-booster-aleksey-foodlab-case-2026.md
  - wiki/evolving-strict/competitor-metrics/business-booster-platform-features-2026.md
  - wiki/evolving/content-trends/iq-hiring-criteria-hook.md
  - wiki/evolving/content-trends/career-quitting-signals-hook.md
  - wiki/evolving/content-trends/plastic-ai-content-pushback-hook.md
  - wiki/evolving/content-trends/anti-impersonation-operational-notice.md
  - wiki/evolving/content-trends/bbq-character-test-personality-typing.md
- updated:
  - wiki/evolving/competitor-positioning/business-booster-visotsky.md (Добавлена секция «Update 2026-05-05 — второй наблюдательный срез» с 6 новыми сигналами (AI-tooling narrative, Алексей FoodLab кейс, Platform feature breakdown, IQ ≥120 hiring, audience-inversion для employees, light-content engine) + обновлённая таблица типов постов с longitudinal-сравнением окно1 vs окно2 (24 дня разрыв) + обновлены sources и updated date)
  - wiki/evolving/content-trends/visotsky-case-study-structure.md (Добавлена секция «Update 2026-05-05 — третий Visotsky-кейс (Алексей FoodLab)» с разбором 5-постового multi-post кейса + детализация content-engine второго порядка через Хайвазиана + Алексея + обновлённая таблица отличий теперь на трёх авторов + повышение confidence паттерна до medium+ с 6 примерами)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (Добавлена секция «Hooks из второго среза Visotsky (2026-04-12..05-05, enrich 2026-05-05)» с 5 новыми hooks: «4 ошибки в управлении» (3730), «В ручном управлении невозможно построить актив» (3747), «Барбекю как симулятор бизнеса» (3754, ссылка на отдельную страницу), «Масштаб бизнеса = масштаб окружения» (3734), «Сначала падает культура. Потом уходят сильные...» (3730 + Крылов cross-source signal))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 7, evolving-strict: 1, volatile-strict: 1, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/tg_alexander_visotsky_20260505-133622.md + 35 children (26 media + 4 audio + 30 video sidecars including 4 transcripts) → status: processed

## [2026-05-05 15:55] [ingest] | TG @bossofyourboss дамп apr-may 2026 — 88% overlap, новые посты: LLM-traffic, toilet-humor, anti-методология, Tabunov YT про Дурова
- source: wiki/sources/2026-05-05-tg-bossofyourboss-apr-may-2026.md
- created:
  - wiki/evolving-strict/competitor-metrics/llm-web-traffic-2026-04.md
  - wiki/evolving/content-trends/toilet-humor-universal-content.md
  - wiki/evolving/content-trends/methodology-vs-execution-anti-hook.md
- updated:
  - wiki/evolving/industry-trends/anthropic-creative-tools-mcp-2026.md (Добавлена секция Adoption-сигнал в РФ founder-сегменте: Tabunov early-watcher reaction на Claude Design (пост 1191) — слабый, но релевантный signal что rollout в РФ ограничен)
  - wiki/evolving/content-trends/tabunov-founder-growth-hooks.md (Добавлены 4 новых хука из apr-may дампа: anti-методологический (1195), сортирный юмор (1192), cadenced-серия «Битва LLM» как годовой формат (1193), meme-обзор как формат YT-эпизода (1196 «Кухня про Дурова»))
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (Добавлена секция «Народный нарратив: nostalgia-love + economic-paradox» с разбором Tabunov YT-эпизода «Кухня» от 2026-05-04: «ЗАРАБАТЫВАЮТ ВСЕ, КРОМЕ TELEGRAM» — economic-frame новый, не присутствовавший в Cossa/Forbes-аналитике; meme-обзор как content-формат)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_bossofyourboss_20260505-133919.md + 26 children (23 jpg + 3 mp4) with all sidecars (.bundle.json, .note.md, .triage.json, .transcript.md, .audio.mp3) → status: processed

## [2026-05-05 15:58] [ingest] | TG @bezsmuzi may 3-5 2026 — РКН KPI 2030, Минпромторг параллельный импорт, Q1 макро, маркетплейс-кризис, candidate-side AI
- source: wiki/sources/2026-05-05-tg-bezsmuzi-may-3-5.md
- created:
  - wiki/volatile-strict/industry-news/ru-rkn-vpn-92pct-target-2030.md
  - wiki/evolving-strict/market-data/ru-business-q1-2026-survey.md
  - wiki/evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026.md
  - wiki/evolving/content-trends/taxes-as-status-symbol-content.md
- updated:
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (Усилен 5-й вектор (РКН KPI 92% VPN к 2030 — strategic документ ГРЧЦ); добавлен 6-й вектор (Минпромторг параллельный импорт IT-комплектующих стоп с 27 мая 2026).)
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (Добавлен раздел Роструд апр 2026: 105 147 человек под сокращение, +43% за 10 мес, безработица 2,2%; cross-link на новую ru-business-q1-2026-survey.)
  - wiki/evolving/industry-trends/candidate-side-ai-services-2026.md (Reinforcing signals из @bezsmuzi: whohasjobs.com US-exemplar, RU «бизнес на резюме», IT-coaching pricing 30-50% × 2 года; цена-anchor сравнение с Горный thesis.)
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлен раздел Update @bezsmuzi 2026-05-05: telega.fm 1 месяц органики; TG падает / MAX растёт qualitative-сигнал.)
  - wiki/volatile/raw-notes/ru-platform-access-april-2026.md (Расширено до мая 2026: добавлены 4 новых сигнала (РКН KPI 92% VPN, Минпромторг параллельный импорт, RKS Global 30 RU-приложений сканируют, TG↓/MAX↑); продлён TTL до 2026-06-05.)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving-strict: 3, evolving: 4, volatile: 1, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_bezsmuzi_20260505-134703.md + 45 children (41 media + 4 video) with sidecars (.note.md, .bundle.json, .triage.json, .transcript.md, .audio.mp3)

## [2026-05-05 16:00] [ingest] | hh.ru condense 46 статей (2026-05-05): AI-обвязка платформы, 6 новых кейсов Бренд-центра, свежие октябрьские срезы рынка труда
- source: wiki/sources/2026-05-05-hh-ru-condensed.md
- created:
  - wiki/evolving/competitor-positioning/hh-ru-ai-hiring-suite-2026.md
  - wiki/evolving-strict/campaign-metrics/hh-ru-call-channel-effectiveness-2026.md
  - wiki/evolving-strict/market-data/ru-shipbuilding-2024.md
  - wiki/canon/marketing-frameworks/evp-framework-brand-center-hh.md
  - wiki/canon/marketing-frameworks/strong-offer-hr-marketing-tilda.md
  - wiki/canon-strict/historical-campaigns/hh-ru-brand-center-cases-2025-2026.md
  - wiki/evolving/customer-feedback/dream-job-review-funnel-2025.md
- updated:
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md (Добавлена AI-обвязка (помощник для найма, виртуальный рекрутер, ranking, расшифровка звонков), новые тарифы вахты, стикеры, увеличение логотипа, Премия HR-бренд 2026.)
  - wiki/evolving-strict/market-data/ru-labor-market-structural-2024-2026.md (Свежие срезы октября 2025: безработица 2,1%, hh.индекс 5,5/6,4; активность синих воротничков +80% YoY; ИИ в HR Gartner 19→61%, WEF/74% автоматизировали.)
  - wiki/evolving-strict/campaign-metrics/branded-vacancy-pages-hh-2026.md (Расширенные бенчмарки: Hochland +55/+41/+62%, Согласие +47,4%, кобренд Альфа-Банк +25,6%/BA 9,8→19%, ВТБ 42M показов, СИБУР 54M показов/×3,75 от прогноза.)
  - wiki/canon/marketing-frameworks/employer-branding-review-funnel.md (Добавлены паттерны 9-11: ГНИВЦ playbook (отзывы→процессные изменения), системный playbook ВТБ, threshold «<4 = invisible» Согласие.)
  - wiki/evolving/content-trends/hh-ru-blog-content-patterns.md (Добавлены Формат 7 (Sense Machine нейромаркетинг как research-backbone) и Формат 8 (региональный отраслевой срез — судостроение).)
  - wiki/evolving/industry-trends/skill-based-hiring-russia-2026.md (Добавлен AI-driven навыкоцентричный поиск (×1,7 пул кандидатов), эволюция тестов на hh.ru (roadmap практических заданий как defense vs AI-assisted кандидаты).)
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md (Добавлен раздел 152-ФЗ для HR-AI: риски облачных ИИ-сервисов, локализация, human-in-the-loop, anti-pattern Amazon как пример bias-нарушения.)
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1, evolving: 4, evolving-strict: 4, canon: 3, canon-strict: 2}
- touched: 14 pages
- raw: raw/processed/articles/_condense_hh-ru_2026-05-05.md (status: processed, irrelevant отдельные статьи остались как stub-source-pages созданные wiki-condense)

## [2026-05-05 16:00] [ingest] | TG @cossaru apr 24 – may 5 2026 — WGSN/AppMagic/Deloitte/Princeton/newstalgia/social-addiction/Brand-Map/RAG-first/Угулава×Claude Design
- source: wiki/sources/2026-05-05-tg-cossaru-apr-24-may-5-2026.md
- created:
  - wiki/evolving-strict/market-data/wgsn-future-consumer-2027.md
  - wiki/evolving-strict/market-data/appmagic-mobile-landscape-2026.md
  - wiki/evolving-strict/market-data/deloitte-marketing-trends-2026.md
  - wiki/evolving-strict/market-data/princeton-llm-persuasion-experiment-2026.md
  - wiki/evolving/content-trends/nostalgia-marketing-2026.md
  - wiki/evolving/content-trends/social-media-addiction-design-patterns.md
  - wiki/volatile-strict/competitor-news/brand-map-curator-marketplace-launch-2026.md
  - wiki/canon/marketing-frameworks/rag-first-ai-implementation-melkozerov.md
- updated:
  - wiki/canon/marketing-frameworks/yudin-personalization-vs-manipulation-test.md (Princeton 2000-people experiment как numerical validation теста (61% vs 22%, 55.5% with warning, 9.5% noticed). Юдин-тест получает empirical подтверждение)
  - wiki/evolving/content-trends/ai-flattery-dark-pattern.md (Princeton experiment apr 2026 даёт первое numerical evidence для тезиса Гуриновича. Hook-family A дополнен числовыми hooks. Confidence гипотезы шагает с medium до high (replicated experiment))
  - wiki/evolving/competitor-positioning/max-messenger.md (Первый publicly-cited B2C performance-кейс на MAX: Фианит-Ломбард feb 2026 (через Telega.in), декларируемый "в разы ниже" CPC чем в Telegram, без чисел; PR-shift в RU маркетинговой среде)
  - wiki/evolving/industry-trends/anthropic-creative-tools-mcp-2026.md (Concrete RU practitioner case: Tim Угулава × Claude Design — пиксельный лендинг с мини-игрой для НейроМастерской; production-readiness Claude Design подтверждена; cross-link с newstalgia + WGSN Strategic Joy)
  - wiki/evolving/industry-trends/ai-personalization-industrial-shift-2026.md (Princeton 2000-people experiment как numerical evidence для этического caveat — industry-shift делает Юдин-тест operationally critical, не только этический)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 4, evolving: 5, volatile-strict: 1, canon: 2, sources: 1}
- touched: 14 pages
- raw: raw/processed/articles/tg_cossaru_20260505-132244.md + 49 children (47 media + 2 video) + sidecars

## [2026-05-05 16:00] [ingest] | TG @olegcloser cycle-2 — полный цикл «Рекордного апреля» 2026-03-16→2026-05-03 (формула 100%, AI-агент «Закрыватель сделок», mystery-shopper, ВР×КР, Q2 playbook)
- source: wiki/sources/2026-05-05-tg-olegcloser-mar-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/sales-100-formula-shevelev.md
  - wiki/evolving/competitor-positioning/zakryvatel-sdelok-ai-agent.md
  - wiki/evolving/content-trends/mystery-shopper-content-format.md
  - wiki/canon/marketing-frameworks/objection-after-holidays-vrkr.md
  - wiki/evolving/content-trends/reality-show-haters-narrative-defense.md
- updated:
  - wiki/canon/marketing-frameworks/business-reality-show-format.md (Добавлена секция «Полный цикл Рекордного апреля» — задокументированная механика (mystery shopper, AI-tooling, 2 эпизода, рекорд, pre-launch sold out, hate-defense, companion content). 5 новых cross-links.)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (Добавлена секция «Q2 2026 forward-looking — Шевелев Q2-priorities playbook»: 3 priorities (mental shift / product-adapt / founder-attention) из подкаста 2277 + ВР×КР техника из 2282 + cycle-2 marketing implications.)
  - wiki/evolving/content-trends/sales-ai-narrative-hooks-2026.md (Добавлена секция «Cycle-2 hooks» с 7 новыми hooks: mystery-shopper «больно очень больно», hate-defense reframe, Q2 prescription triad, ВР×КР объекция, 18-дыр teaser, cite-the-amount formula authority, pre-sold-out scarcity.)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Добавлена секция «Полная траектория Рекордного апреля — что произошло с участниками»: 5 named-кейсов (Юлия/Юрий/Артур/Роман/Екатерина) + JTBD «помоги поверить что движение возможно» + product-stagnation anti-pattern + 1-2-часа founder-attention action item.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 5, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_olegcloser_20260505-135032.md + 43 children (4 audio + 12 video + 27 media) with sidecars (.note.md, .transcript.md, .audio.mp3, .bundle.json)

## [2026-05-05 16:30] [ingest] | condensed e-xecutive.ru 34 статьи 2001-2002 — 17 timeless marketing-frameworks (Парето / value-for-customer / BCG / KPMG / defector-loyalty / brand-manager / M&A) + 3 evolving-trends + 2 positioning/audience
- source: wiki/sources/2026-05-05-e-xecutive-ru-condensed.md
- created:
  - wiki/canon/marketing-frameworks/brand-manager-core-competencies.md
  - wiki/canon/marketing-frameworks/value-for-customer-concept.md
  - wiki/canon/marketing-frameworks/production-vs-market-pricing-pipeline.md
  - wiki/canon/marketing-frameworks/defector-loyalty-crm-analysis.md
  - wiki/canon/marketing-frameworks/microniche-marketing-packages.md
  - wiki/canon/marketing-frameworks/pareto-80-20-marketing.md
  - wiki/canon/marketing-frameworks/open-source-competitor-research.md
  - wiki/canon/marketing-frameworks/consulting-brand-naming-typology.md
  - wiki/canon/marketing-frameworks/bcg-outsourcing-decision-matrix.md
  - wiki/canon/marketing-frameworks/kpmg-5-stage-restructuring.md
  - wiki/canon/marketing-frameworks/score-diagnostic-model.md
  - wiki/canon/marketing-frameworks/bubble-chart-prioritization.md
  - wiki/canon/marketing-frameworks/plant-to-company-transition.md
  - wiki/canon/marketing-frameworks/ma-goodwill-synergy-basics.md
  - wiki/canon/marketing-frameworks/management-pyramid-sales.md
  - wiki/canon/marketing-frameworks/sales-crm-minimum-fieldset.md
  - wiki/canon/marketing-frameworks/internal-change-communication-protocol.md
  - wiki/canon/positioning/attention-warfare-thesis.md
  - wiki/canon/target-audience/b2c-vs-b2b-value-segmentation.md
  - wiki/evolving/industry-trends/entertainment-business-shift-2001-thesis.md
  - wiki/evolving/industry-trends/hr-as-strategic-partner-ulrich-cipd.md
  - wiki/evolving/content-trends/pr-self-publishing-principle.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 19, evolving: 3, sources: 1}
- touched: 23 pages
- raw: raw/processed/articles/_condense_e-xecutive-ru_2026-05-05.md (status: processed; legacy stub-source-pages 2026-05-05-exec-* остаются как audit-trail созданные wiki-condense до этого ingest)

## [2026-05-05 16:30] [ingest] | TG @moibiz — дайджест 21 апр – 5 мая 2026: ставка ЦБ 14,5% (gov-confirm), закон об адаптации МСП к НДС, 63% компаний ↑ маркетинг-бюджеты, Runet 38,4 трлн ₽, запуск Novatorix
- source: wiki/sources/2026-05-05-tg-moibiz-apr-21-may-05.md
- created:
  - wiki/evolving/competitor-positioning/novatorix-moibiz-ai-consultant-2026.md
  - wiki/evolving-strict/market-data/ru-marketing-budgets-2026-increase.md
  - wiki/evolving-strict/market-data/ru-runet-economy-2025.md
  - wiki/volatile-strict/industry-news/ru-msp-tax-relief-law-2026-04.md
- updated:
  - wiki/volatile-strict/industry-news/cb-ru-key-rate-14-5-2026-04.md (Подтверждение ставки 14,5% через государственный канал @moibiz (пост 7446) — confidence на самом значении ставки upgraded medium→high; добавлен второй source; impact-числа Крылова остаются medium.)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (Добавлен раздел 8 — четвёртый независимый голос (@moibiz, гос-канал) на рамке Q1-кризиса спроса; supply-side signal «упал спрос на бизнес-тренеров»; нарратив теперь mainstream-консенсус (4 голоса: Шевелев, Крылов, Goryachev, @moibiz/гос).)
  - wiki/evolving-strict/market-data/ru-smb-ecosystem-scale-2025.md (Addendum operational scale: 410 центров «Мой бизнес», 62,4K услуг YTD 2026, 7,7K через МСП.РФ, ГМФО 3,5K микрозаймов на 9,45 млрд ₽, РГО 2,9K поручительств на 41,1 млрд ₽; Премия 78/298/38 регионов/проектов/финалистов; пропорция ~1 услуга на 100 SMB/квартал.)
  - wiki/evolving/industry-trends/ru-vertical-ai-signals-2026.md (Добавлен Сигнал 12 — Novatorix как первый государственный vertical AI инструмент в инвентаре; источников теперь пять (Цейтлин/Горный/Inc.Russia/@neuraldvig/@moibiz); anti-hallucination claim становится мейнстримом.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 3, volatile-strict: 2, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_moibiz_20260505-132339.md + 44 children (38 jpg + 6 mp4) с .note.md/.bundle.json/.audio.mp3/.transcript.md sidecars → status: processed

## [2026-05-05 18:00] [ingest] | TG @dnative дайджест 7547-7596 (14 apr – 4 may 2026) — 50 постов с 39 children
- source: wiki/sources/2026-05-05-tg-dnative-7547-7596.md
- created:
  - wiki/evolving-strict/competitor-metrics/vk-organic-reach-growth-2026-q1.md
  - wiki/evolving/content-trends/long-form-reels-organic-distribution-2026.md
  - wiki/evolving/content-trends/brand-fanpage-format-2026.md
  - wiki/evolving/content-trends/grandma-employee-viral-format-corazon.md
  - wiki/evolving/content-trends/proof-of-process-content-spider-2026.md
  - wiki/evolving/content-trends/threads-spam-emotional-hook-2026.md
  - wiki/evolving/content-trends/dnative-marketing-content-vacuum-thesis.md
  - wiki/evolving/content-trends/vibe-coding-curse-content-hooks-2026.md
  - wiki/evolving/industry-trends/instagram-aggregator-pages-algorithm-2026.md
  - wiki/evolving-strict/market-data/meta-ads-experiment-2026.md
  - wiki/volatile-strict/industry-news/mts-adtech-mta-launch-2026.md
  - wiki/volatile-strict/industry-news/uk-trust-survey-2026.md
- updated:
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md (Добавлены данные Гуляева РАЭК через Коммерсант (53→28% YoY), ВЦИОМ 31% за один-клик, ВК Шопсы 30 млрд просмотров и x5,7 конверсия — секция социальной коммерции)
  - wiki/evolving/content-trends/vk-shopsy-creator-playbook.md (Добавлена секция 'Масштаб платформы (апрель 2026)': 30 млрд просмотров товарного контента ВК Шопсы 2025, конверсия x5,7, ВЦИОМ 31% параллельный сигнал)
  - wiki/evolving/industry-trends/ru-news-consumption-platform-shift-2010-2025.md (Добавлен second-source confirmation от @dnative с теми же ключевыми цифрами Михайлова + дополнительная фактура (100-400k материалов/день в РФ + тезис dnative о 3-й точке маршрута))
  - wiki/volatile-strict/industry-news/russian-social-platforms-digest-2026-03-04.md (Добавлены 2 секции: VK Видео сокращение собственных шоу (2026-04-17, релизует главную для авторов) и Yandex Reklama IN: РИТЕЙЛ конференция (анонс))
  - wiki/volatile-strict/industry-news/ru-vpn-telegram-restrictions-2026-04.md (Добавлена хронология 2026-04-17: dnative фиксирует -1/3 охватов в TG-каналах + тезис VPN-кочевник наоборот (пользователи сокращают активность в RU-сервисах))
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (Добавлен 5-й слой реакции рынка: эрозия охватов TG из-за VPN-блокировок (-1/3 через @dnative_sklad), импликация для CPV-бенчмарков)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 9, evolving-strict: 3, volatile-strict: 4, sources: 1}
- touched: 19 pages
- raw: raw/processed/articles/tg_dnative_20260505-132530.md + 39 children (17 video, 19 media-jpg, 2 audio-ogg) + sidecars (.bundle.json, .triage.json, .note.md, .transcript.md, .audio.mp3) → status: processed

## [2026-05-05 18:30] [ingest] | TG @boris_again — re-export 50 постов 21 мар – 5 мая 2026 (overlap 3814–3847 prior + 16 new 3848–3863): Opus 4.7 ops, DeepSeek V4 architecture, Kimi K2.6 Agent Swarm, GPT Image 2, Gemini Robotics-ER 1.6, Grok 4.3, Pine Probes, ULTRAPACK + MatrixGame hooks
- source: wiki/sources/2026-05-05-tg-boris-again-mar-may-2026.md
- created: none
- updated:
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md (Boris-attestation 22-Apr/30-Apr/4-May к Q2 add-on: Opus 4.7 ops detail (tokenizer 1.0–1.35× больше токенов, /ultrareview $5–$20, xhigh default, --enable-auto-mode, +10–14пп SWE-bench vs 4.6); GPT Image 2 (API id gpt-image-2, +61 пункт Elo Image Arena, per-token pricing $30/$8/$2, ≈$0.04 за 1024×1024 high); DeepSeek V4 архитектура (CSA+HCA attention, 32–33T pretraining, N-specialists distill post-train, IMOAnswerBench 89.8, Codeforces 3206, 6× дешевле Opus); Kimi K2.6 Agent Swarm (100→300 саб-агентов, до 4000 шагов, 13ч кодинг-сессии, нативный int4, видео-вход); Grok 4.3 (110 t/s, $1.25/$2.50, TTFT 31с); Talkie 1930 framing; Pine AI Knowledge Probes (R²=0.917, GPT-5.5≈9.7T, Opus 4.6≈5.3T); Lyra 2.0; Nucleus Image (sparse MoE 17B/2B); Sapiens2 (Humans-1B, 308 точек pose); Vista4D Netflix (77% blind preference); Sync dubbing; VR-Outpaint; новый раздел Robotics Q2 с Gemini Robotics-ER 1.6 (чтение приборов 23%→93%))
  - wiki/evolving/industry-trends/ru-vertical-ai-signals-2026.md (Сигнал 3 (Т-Технологии) уточнён конкретной цифрой: до 700 млн ₽/год в прикладные исследования (через OCR ТАСС-картинки 3833 в re-export дампе))
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Hook 8 «Пет проекты в 2026 би лайк: 5 маркдаун файлов» (Цейтлин ULTRAPACK 27⭐, GitHub) + sub-hook про инверсию dev-tools value chain. Hook 9 «Я не знаю Rust, но знаю плюсы, поэтому могу читать оригинал» (Цейтлин MatrixGame Rust WASM port) — мостовой паттерн для языковых barrier-ов через AI + sub-hook «в одиночку Claude Code и Codex не вытягивают»)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_boris_again_20260505-140114.md (+ .bundle.json, .note.md, .triage.json sidecars) + 33 media children + 1 video child (tg_boris_again_3816.mp4) with .note.md sidecars

## [2026-05-05 18:30] [ingest] | TG @ofd24 — дайджест 3 апр – 5 мая 2026 (re-evaluated релевантность: фискальное регулирование как macro-context для SMB-контента)
- source: wiki/sources/2026-05-05-tg-ofd24-apr-3-may-5-2026.md
- created:
  - wiki/volatile-strict/industry-news/ru-spot-eaeu-launch-2026.md
  - wiki/volatile-strict/industry-news/ru-markirovka-expansion-2026-q2.md
  - wiki/volatile-strict/industry-news/ru-fns-cb-individual-transfers-surveillance-2026.md
  - wiki/evolving-strict/market-data/ru-qsr-restaurant-2025-2026-q1.md
- updated:
  - wiki/volatile-strict/industry-news/cb-ru-key-rate-14-5-2026-04.md (Добавлен 4-й независимый источник: @ofd24 пост 6528 — отраслевой канал ОФД с B2B-аудиторией бухгалтеров/общепита подтверждает снижение ставки до 14,5%)
  - wiki/volatile-strict/industry-news/ru-msp-tax-relief-law-2026-04.md (Добавлен 2-й источник: @ofd24 пост 6510 (Госдума 14.04.2026 в 3-м чтении, параметры совпадают). Новая секция "Operational gap — кассовый разрыв Q1 2026 не закрыт" с цифрами ФРиО (трафик -3% страна, -12% Москва, -11% баров за март). Обновлены связанные страницы.)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (6-й независимый голос на рамке Q1 кризиса: @ofd24 с financial datapoints — QSR-операторы 2025 (прибыль -15…-61% при росте выручки +15-19%) и рестораны Q1 2026 (трафик Москва -12%, -11% баров за март). Это первый аудируемый-quantitative источник на рамке (предыдущие 5 — narrative).)
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (Добавлен 7-й вектор: фискально-комплаенсное давление (СПОТ + расширение Честного Знака + надзор переводов + автоштрафы). Качественно отличается от 1-6 векторов: бьёт не по distribution или hardware, а по transactional cost самого ведения бизнеса. Direct opportunity для GRO как инструмента дедлайн-комплаенса.)
  - wiki/evolving/industry-trends/ru-retail-robotization-labor-deficit-2025-2026.md (Добавлен adjacent global signal — Galbot 20 магазинов в Шанхае (план 100 к концу 2026): полное замещение кассирской позиции. Counter-pattern к "роботы закрывают функции, не вакансии". Эмоциональный триггер для founder-аудитории.)
  - wiki/evolving-strict/market-data/ru-business-q1-2026-survey.md (Добавлен sector-specific addendum: QSR + общепит datapoints через @ofd24 (Коммерсант + ФРиО). Цифры: -61% Burger King прибыль, -12% Москва трафик. Структурный паттерн "рост выручки + падение прибыли" совпадает с marketplace margin collapse и общим survey.)
  - wiki/sources/2026-04-14-tg-ofd24-fiscal-regulation-digest.md (Добавлена ремарка о supersession рамки релевантности (2026-05-05) и блок ## Contradictions: пользователь в новом ingest перепозиционировал канал как трекер регуляторных событий для SMB-контента; ретроактивный пересмотр не делается, но политика релевантности изменилась.)
- superseded:
  - wiki/sources/2026-04-14-tg-ofd24-fiscal-regulation-digest.md (supersession рамки релевантности, не фактаж)
- sensitive flag: none
- layer-touched: {volatile-strict: 4, evolving-strict: 2, evolving: 3, sources: 2}
- touched: 11 pages
- raw: raw/processed/articles/tg_ofd24_20260505-132232.md + 6 children (3 media, 3 video) с sidecars

## [2026-05-05 18:50] [ingest] | TG @howtomake10x — 2026-03-18..05-05 continuation (50 постов, 1502–1562; novel: 1541–1562)
- source: wiki/sources/2026-05-05-tg-howtomake10x-mar-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/krylov-reference-call-question.md
  - wiki/canon/marketing-frameworks/krylov-sales-imitator-3-markers.md
  - wiki/canon/marketing-frameworks/krylov-7-mentor-meetings.md
  - wiki/evolving/competitor-positioning/aimindset-lab-ai-native-2026.md
  - wiki/volatile-strict/industry-news/cb-ru-key-rate-14-5-2026-04.md
- updated:
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (Добавлены 4 новых Krylov-hook'а: «эмоциональное состояние = рабочий инструмент» (1546), «3 маркера sales-имитатора» (1548), «профи vs универсал» Marey/Альфа-Банк (1549) + швейцарский нож метафора)
  - wiki/evolving/product-reception/gro-productivity-energy-angle.md (Добавлен раздел «Дополнения 2026-05-05»: post 1546 как третья формулировка productivity-anchor + reference-call вопрос (1547) reframe'нутый как self-test)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Hook 11 — «AI как замена B2B-команды продаж» через Krylov×Smetnev созвон (Skyeng anchor); cross-link на B2B AI playbook и AI Mindset Lab)
  - wiki/evolving/industry-trends/ru-smb-mentor-community-market-2026.md (Добавлены 2 новых player'а в landscape: «Команда А» (Krylov, emerging) и «Атланты» (Воронин, mature anchor); category эволюция от dual-anchor (Гребенюк/Высоцкий) к multi-player (4 full-stack игрока))
  - wiki/sources/2026-04-14-tg-howtomake10x-mar-apr-2026.md (Добавлен continuation-pointer на 2026-05-05 срез)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 4, volatile-strict: 1, sources: 2}
- touched: 11 pages
- raw: raw/processed/articles/tg_howtomake10x_20260505-135048.md + 44 children (43 media + 1 video) with sidecars (.note.md, .bundle.json, .triage.json, .transcript.md for 1543)

## [2026-05-05 18:51] [ingest] | TG @breakingtrends — дамп 50 постов apr21-may05 + 43 media (bundle, AI-corporate-race + RU regulatory + content-trends)
- source: wiki/sources/2026-05-05-tg-breakingtrends-apr21-may05.md
- created:
  - wiki/evolving-strict/market-data/ru-vpn-downloads-2026-q1.md
  - wiki/evolving-strict/market-data/youtube-ad-revenue-2025-2026.md
  - wiki/evolving/industry-trends/ru-news-consumption-platform-shift-2010-2025.md
  - wiki/evolving/competitor-positioning/breaking-trends-pr-agency.md
  - wiki/volatile-strict/competitor-news/microsoft-vibe-working-office-2026.md
  - wiki/volatile-strict/competitor-news/microsoft-9000-voluntary-retirements-2026.md
  - wiki/volatile-strict/competitor-news/openai-phone-mediatek-2028.md
  - wiki/volatile-strict/competitor-news/disney-ai-adoption-dashboard-tokenmaxxing-2026.md
  - wiki/volatile-strict/industry-news/oscar-academy-ai-rules-2026.md
  - wiki/volatile-strict/industry-news/ru-rosobrnadzor-homework-ai-2026.md
  - wiki/evolving/content-trends/it-collapse-fallback-meme-hook.md
  - wiki/evolving/content-trends/lacoste-rebrand-back-to-roots-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (+ Коммерсантъ March 2026: TG трафик −18%, MAX активность +60%, TG MAU >94M — quantitative confirmation мета-нарратива)
  - wiki/volatile-strict/industry-news/ru-rkn-vpn-92pct-target-2030.md (+ second source: Кащенко в Газете.ru (4 мая 2026) подтверждает те же цифры 92%/831 Тбит/с/98% — два независимых пересказа)
  - wiki/volatile-strict/industry-news/ru-vpn-metering-proposal-2026-04.md (+ second source Mash через @breakingtrends 16702: подтверждение Минцифры обсуждения платного зарубежного мобильного интернета)
  - wiki/evolving/industry-trends/ai-knowledge-worker-climb-2025-2026.md (+ сигналы 6,7: Google Pichai 75% AI-кода + Business Insider vibe-coding популяризация для не-технарей (пенсионеры, дети))
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (+ Качественный сдвиг: AI как полная замена роли — Business Insider эксперимент журналистки с AI-агентом на собственных текстах/голосе/сценариях)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 2, evolving: 5, volatile-strict: 7, sources: 1, canon: 0}
- touched: 13 pages
- raw: raw/processed/articles/tg_breakingtrends_20260505-132513.md + 43 children (34 media + 9 video)

## [2026-05-05 19:00] [ingest] | TG @peregudov re-dump (50 постов янв-май 2026, 377-429) — vibecoding founder playbook (canon) + Creally AI-influencer-platform counterpoint + LinkedIn voice-rules + AI Skills Conf lineup
- source: wiki/sources/2026-05-05-tg-peregudov-jan-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/peregudov-vibecoding-founder-playbook-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-native-company-architecture-2026.md (Добавлена секция «AI-replacement внешней операционной команды (Creally, 2026-05)» с таблицей сравнения внутренних vs внешних AI-replacement функций; cross-link на новый vibecoding playbook как пред-условие Whizz-кейса)
  - wiki/evolving/industry-trends/influencer-marketplace-failure-paradox.md (Добавлена секция «Counterpoint: Creally — AI-agency-replacement (не marketplace)» с таблицей 4-признакового различия от marketplace-pattern; пометка confidence:medium из-за paid promo)
  - wiki/evolving/content-trends/telegram-native-formats.md (В разделе exemplar Перегудов добавлена под-секция «Re-dump 2026-05-05: новые паттерны» — 3 новых под-паттерна (Курцвейл 2-серийный cliffhanger 421→422, AI-event-poster paid_ads 419-420, UTM-only paid_ads anti-pattern Creally 429))
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Добавлены Hook 12 «AI-замена B2C-инфлюенсер-маркетинговой команды» (Перегудов × Creally, расширение Hook 11 на B2C) и Hook 13 «Vibecoding founder playbook» (5 шагов, мост между AI-narrative и core-value-prop GRO) с funnel-mapping таблицей)
- superseded: none
- sensitive flag: ⚠ media/tg_peregudov_401.jpg содержит PII — скриншот внутренней системы Whizz с именами/email; в слоях не цитируется (унаследовано из предыдущего ingest)
- layer-touched: {canon: 1, evolving: 4, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_peregudov_20260505-135403.md + 9 children (8 media, 1 video) with sidecars (.note.md ×9, .bundle.json, .triage.json, .audio.mp3, .transcript.md)

## [2026-05-05 19:37] [ingest] | TG @gurinovich_shares — backfill 2026-05-05 (bundle-дубль апрельского дампа + 1 personal пост 911, audit-only)
- source: wiki/sources/2026-05-05-tg-gurinovich-shares-may-2026-duplicate.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/tg_gurinovich_shares_20260505-133859.md + 26 children (24 jpg, 2 mp4) with sidecars; 24 MD5-DUP children overwrote identical processed/ counterparts, 2 NEW (862.jpg, 871.jpg) added (irrelevant posts, no vision)

## [2026-05-05 22:30] [ingest] | condensed vc.ru 46 статей apr-may 2026 — AI-индустрия, HR Tech РФ, рынок труда, layoffs волна 2
- source: wiki/sources/2026-05-05-vc-ru-condensed.md
- created:
  - wiki/evolving-strict/market-data/employee-engagement-quiet-quitting-2026.md
  - wiki/evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2.md
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md
  - wiki/evolving/industry-trends/gen-z-workforce-shift-2026.md
  - wiki/evolving/content-trends/employee-content-employer-trust-2026.md
  - wiki/evolving/content-trends/job-posting-as-content-2026.md
  - wiki/evolving/content-trends/corporate-merch-as-message.md
  - wiki/volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05.md
  - wiki/volatile-strict/competitor-news/apple-ternus-ceo-transition-2026.md
  - wiki/volatile-strict/competitor-news/unity-agent-beta-2026.md
  - wiki/volatile-strict/industry-news/amsterdam-outdoor-ad-ban-2026.md
  - wiki/volatile-strict/industry-news/openai-altman-new-yorker-dossier.md
  - wiki/canon/marketing-frameworks/dunning-kruger-marketing-applications.md
  - wiki/canon/marketing-frameworks/sbi-grow-feedback-framework.md
  - wiki/canon/marketing-frameworks/multichannel-cumulative-effect.md
  - wiki/canon/target-audience/it-specialist-candidate-profile-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-hr-tech-market-size-2026.md (Enrich vc.ru condensed 2026-05-05: H1 2025 = 40.6 млрд ₽ +12%; 72.8% планы автоматизации ВШЭ+hh+Ancor; точность ручного скрининга 60-70% vs NLP 97%; ROI HRM 500-1500%)
  - wiki/evolving-strict/market-data/ru-labor-market-stagnation-q1-2026.md (Independent confirm hh.индекс март 2026 Москва 10, февраль РФ 9.8; новые: вакансии +12% м/м, резюме +15% м/м, медианная 84600 ₽; ФАС зарплатный картель; Modis банкротство; инвестиции -3.1% к концу 2025)
  - wiki/evolving-strict/market-data/ai-driven-layoffs-2025-2026.md (Coinbase -14% (700, реструктуризация $50-60M, Q4 убыток $667M, биткоин -40%), Crypto.com -12% (180), Block -40% (4000, фев 2026); Anthropic-исследование о профессиях под угрозой)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (Криптофинансовая вертикаль AI-cost-cutting: Coinbase/Crypto.com/Block с конкретными CEO-цитатами; Anthropic исследование «безопасных» профессий (живое взаимодействие))
  - wiki/evolving/competitor-positioning/max-messenger.md (Update apr 2026: 110M зарегистрированных, 80M DAU (рост с 52M), 7M каналов; расшифровка кружков мая 2026, голосовых апрель 2026; caveat про DAU vs декабрь 2025 = 52M)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 6, evolving: 5, volatile-strict: 5, canon: 4, sources: 1}
- touched: 21 pages
- raw: raw/processed/articles/_condense_vc-ru_2026-05-05.md (+ .note.md)

## [2026-05-05 22:50] [ingest] | Condense dzen-ru — 10 статей dzen.ru (vc.ru/Inc. репабликации) 2026-05-05: AI-JV, MCP, персонализация, МСБ-агенты
- source: wiki/sources/2026-05-05-dzen-ru-condensed.md
- created:
  - wiki/evolving/industry-trends/volvo-gemini-automotive-ai-2026.md
  - wiki/evolving/industry-trends/anthropic-creative-tools-mcp-2026.md
  - wiki/evolving/industry-trends/ai-personalization-industrial-shift-2026.md
  - wiki/evolving/industry-trends/ru-msb-agent-payments-channel-2024-2026.md
  - wiki/evolving-strict/market-data/ai-personalization-benchmarks-2026.md
  - wiki/evolving-strict/market-data/ru-msb-agent-payments-tochka-2026.md
  - wiki/evolving-strict/market-data/hh-automation-survey-2026.md
  - wiki/canon/marketing-frameworks/yudin-personalization-vs-manipulation-test.md
  - wiki/canon/marketing-frameworks/ai-personalization-4-layer-architecture.md
  - wiki/volatile-strict/competitor-news/nebius-eigen-acquisition-2026-05.md
  - wiki/evolving-strict/competitor-metrics/nebius-arr-2025-2026.md
  - wiki/volatile-strict/competitor-news/openai-spinoff-rejected-pre-ipo-2026-05.md
  - wiki/volatile-strict/competitor-news/replit-stripe-3digit-growth-2026-05.md
  - wiki/canon/target-audience/automation-eager-knowledge-worker-ru.md
  - wiki/evolving/content-trends/inc-russia-longform-pattern-2026.md
  - wiki/evolving/content-trends/dzen-republication-preview-pattern-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (Добавлены: параллель Anthropic JV $1,5 млрд + OpenAI Development Company $10 млрд оценка как индустриальный паттерн enterprise-через-PE-фонды; Nebius+Eigen $643 млн как neocloud-консолидация; MCP-стандартизация (Claude+Adobe/Blender/Canva совместим с GPT-5.5/Gemini) как 4-й сигнал.)
  - wiki/evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2.md (Добавлены 9 строк в таблицу: Anthropic JV ($1,5 млрд оценка, $300 млн стартовых, партнёры), Nebius ARR ($1,25→$7–9 млрд), Nebius+Eigen ($643 млн, акции +14,2%).)
  - wiki/canon/marketing-frameworks/real-time-personalization-cvm-mechanics.md (Cross-link на тест Юдина (этический слой) + ai-personalization-4-layer-architecture (generalized version) + ai-personalization-industrial-shift-2026 + benchmarks-2026.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 6, evolving-strict: 4, volatile-strict: 3, sources: 1}
- touched: 17 pages
- raw: raw/processed/articles/_condense_dzen-ru_2026-05-05.md

## [2026-05-05 23:50] [ingest] | TG @cgevent — дайджест 30 апр – 5 мая 2026 (Apple Vision Pro отмена, AI-cost > зарплат, Китайский суд, 3 «Нейропрожарки», Roblox/Unity/ElevenMusic AI-layer)
- source: wiki/sources/2026-05-05-tg-cgevent-apr30-may05-2026.md
- created:
  - wiki/evolving-strict/market-data/ai-coding-tools-cost-explosion-2026.md
  - wiki/evolving-strict/market-data/specialized-video-finetune-cost-anchor-2026-05.md
  - wiki/volatile-strict/industry-news/apple-vision-pro-discontinued-2026-04.md
  - wiki/volatile-strict/industry-news/china-court-ai-replacement-2026-04.md
  - wiki/volatile-strict/industry-news/gemini-file-generation-2026-05.md
  - wiki/volatile-strict/competitor-news/elevenmusic-platform-launch-2026-05.md
  - wiki/volatile-strict/competitor-news/grok-imagine-agents-2026-05.md
  - wiki/volatile-strict/competitor-news/google-photos-wardrobe-2026-05.md
  - wiki/volatile-strict/competitor-news/anthropic-blender-donation-2026-05.md
  - wiki/volatile-strict/competitor-news/roblox-reality-hybrid-architecture-2026.md
  - wiki/volatile/weekly-digest/tg-cgevent-may-w1-2026.md
- updated:
  - wiki/evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format.md (Добавлены 3 новых exemplar'а формата: Саянов «На пороге Тьмы» (1 000 ₽, ~6 мес), Михина «Once upon a time» (€100-150), Bao «Маяк Вольной Судьбы» ($60, 6 минут — впервые полноценный 6-минутный кинематографический клип). Расширена сводная таблица бюджетов (теперь 8 кейсов с inline-маркерами + Source-колонка). Добавлен раздел про эволюцию формата апрель→май 2026.)
  - wiki/volatile-strict/competitor-news/unity-agent-beta-2026.md (Добавлен второй source-anchor (@cgevent #15591–15598) с детализацией возможностей агента (генерация сцен по картинке/референсу, промптовая анимация персонажей, генерация звука, AI Gateway для подключения внешних Codex/Claude/Gemini/Cursor моделей). Расширены связанные страницы (grok-imagine-agents, roblox-reality).)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (Добавлены два counter-anchor раздела: (1) Cost overrun — Uber/Swan AI/Nvidia публично признали, что cost(токены) > cost(найм людей) в 2-5×; (2) Китайский суд Ханчжоу 2026-04-30 — первый правовой precedent против AI-замещения. Расширены связанные страницы.)
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md (Добавлены 6-й и 7-й data-point: Uber/Swan/Nvidia (cost overrun как часть investment phase) и Китайский суд Ханчжоу (regulatory friction как новый компонент J-curve, удлиняющий её на legal compliance).)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, evolving-strict: 2, volatile-strict: 8, volatile: 1, sources: 1}
- touched: 14 pages
- raw: raw/processed/articles/tg_cgevent_20260505-141248.md + 49 children (22 video + 27 media) with sidecars (.note.md, .bundle.json, .triage.json, 17 .transcript.md, .audio.mp3 для аудио-обработанных)

## [2026-05-06 00:00] [ingest] | TG @grebenukm — дамп 50 постов apr 2 – may 5 (bridge-ingest, новое: «Выбор Миши» 19 пивот-рычагов, ЕС-клиника 2K семей market-sizing, Декларация s2 live, identity-defiance hook)
- source: wiki/sources/2026-05-05-tg-grebenukm-apr-may-2026.md
- created: none
- updated:
  - wiki/evolving/competitor-positioning/grebenyuk-anomaly-community.md (Добавлена секция «Апдейт май 2026»: новый курс Аномалии «Выбор Миши» (19 пивот-рычагов, третий в трёхуровневой product-таксономии), ЕС-клиника публичный market-sizing 2% Moscow premium med = 2 000 семей, salary 800K+ ₽, Хлебинский (RetailRocket) co-mentor, Хамовники А-класс офис, deadline 10 мая. Декларация s2 live production data, dual-track positioning (community + luxury), identity-defiance subvariant.)
  - wiki/evolving/content-trends/accountability-reality-show-format.md (Добавлена секция «Production data points (live ingest 2026-05-05)»: casting selectivity 500→16 (≈3.2%), in-show funnel 16→10→8→4, live-audience layer 300 мест × билет qtickets, framing «Игра в кальмара», diversified-niche pool как TOFU material. Расширена сравнительная таблица сезонов 1 vs 2.)
  - wiki/evolving/content-trends/anti-authority-positioning-hook.md (Добавлена секция «Identity-defiance subvariant» (пост 7443 Делягин-quote): сравнительная таблица reframe vs identity-defiance, когда какой вариант, anti-pattern'ы, GRO-адаптация через segment-identity вместо founder-community.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_grebenukm_20260505-131949.md + 29 children (20 media, 7 video, 2 audio) with sidecars

## [2026-05-06 00:00] [ingest] | TG @incrussiamedia — дайджест 50 постов apr-28→may-5 2026 (mobile shutdown, контрафакт ecom, готовый бизнес 2026, Heroes Olden Era, Patagonia, Нейри, Smart Engines, AI-music promo)
- source: wiki/sources/2026-05-05-tg-incrussiamedia-apr-28-may-5-2026.md
- created:
  - wiki/sources/2026-05-05-tg-incrussiamedia-apr-28-may-5-2026.md
  - wiki/volatile-strict/industry-news/ru-counterfeit-marketplaces-letter-2026-04.md
  - wiki/evolving-strict/market-data/ru-ready-business-demand-2026.md
  - wiki/volatile-strict/industry-news/unfrozen-heroes-olden-era-launch-2026-05.md
  - wiki/canon/marketing-frameworks/patagonia-refusal-as-asset.md
  - wiki/volatile-strict/competitor-news/neyri-panov-2026-05.md
  - wiki/volatile-strict/industry-news/smart-engines-gosuslugi-ocr-2026-04.md
  - wiki/evolving/content-trends/inc-russia-ai-music-track-promo-2026.md
- updated:
  - wiki/volatile-strict/industry-news/ru-mobile-internet-shutdowns-may-2026.md (Inc.Russia 36678 ранний анонс apr-30 (на 4 дня раньше операторов); первое числовое определение ущерба от мартовских прецедентов 3–5 млрд ₽; 36697 повторное предупреждение в день начала окна + carousel «как подготовиться» (36698–702))
  - wiki/evolving-strict/market-data/hh-automation-survey-2026.md (Cross-channel publication confirmation через Inc.Russia 36707 (тот же breakdown 70%/27%, цитата Хадиной 3ч/день, editorial framing «автоматизация — базовое условие, не бонус»))
  - wiki/evolving/industry-trends/ai-personalization-industrial-shift-2026.md (Inc.Russia 36708 второй материал на тему за неделю; точное эхо тезиса Юдина «вовлечённость от зависимости система не отличает» — нарратив стал стабильной content-vertical Inc.Russia)
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (Greative/Зыкова авторская колонка Inc.Russia 36690 (agency-side signal): FAS до конца 2026 confirm + dual-positioning brands («не бросают замедленные платформы, усиливают присутствие в разрешённых»); закрепление «зеркалирование, не миграция» как стабильного состояния)
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1, canon: 1, evolving: 3, evolving-strict: 2, volatile-strict: 5}
- touched: 12 pages
- raw: raw/processed/articles/tg_incrussiamedia_20260505-131747.md + 45 children (42 media, 2 video, 1 audio) with sidecars (.bundle.json, .note.md, .triage.json, .audio.mp3, .transcript.md)

## [2026-05-06 00:00] [ingest] | TG @portnyaginlive — дамп 50 постов apr-20…may-1 2026 (Siberia 5-bath series, Самвер/Rocket Internet, 7 decision questions)
- source: wiki/sources/2026-05-05-tg-portnyaginlive-apr-20-may-1-2026.md
- created:
  - wiki/canon-strict/historical-campaigns/samwer-rocket-internet-fast-follower.md
  - wiki/canon/marketing-frameworks/portnyagin-7-decision-questions.md
  - wiki/evolving/content-trends/cultural-narrative-brand-storytelling.md
- updated:
  - wiki/evolving/content-trends/portnyagin-founder-channel-patterns.md (Добавлены 11-й формат (serialized cultural-narrative product launch — 5 банных постов под единый launch) и 12-й (defensive brand-mission essay 11243); раздел дополнительных наблюдений второго дампа: monthly cadence бизнес-событий подтверждена, balance failure-cases + winning playbooks; cross-links на 3 новые страницы и второй source)
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, canon: 1, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_portnyaginlive_20260505-132547.md + 50 children (jpg media)

## [2026-05-06 01:00] [ingest] | TG @HR_kak_delat — повторная вырезка mar-may 2026 (50 постов 1932-1983, новая фактура 1963-1983)
- source: wiki/sources/2026-05-05-tg-hr-kak-delat-mar-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/hr-strategy-three-scenarios.md
- updated:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (+апрельский апдейт hh-индекс >11 п. (vs 9.8 в марте), эмоциональные метрики (выгорание +36%, тихие увольнения +19%, конфликты +16%, индекс настроения 0.18), 46% работодателей считают рост hh-индекса ничего не меняет; +сводная таблица динамики hh-индекса по 6 точкам с триангуляцией; +cross-link на новый framework hr-strategy-three-scenarios)
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (+седьмой голос HR-клуб «Как делать»: фрагментация HR-моделей (пост 1963), эмпатия выжигает (пост 1965); связка с тремя сценариями; маркетинговое следствие для HR-vertical контента GRO)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (+Hook 18 «Горизонтальные связи > готовые решения» из @HR_kak_delat пост 1963: парадокс ценности нетворка в условиях фрагментации правил, GRO-перенос как тренажёр для решений в неопределённости; обновлён маппинг hook'ов на воронку)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving-strict: 1, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_hr_kak_delat_20260505-131532.md + 33 children (26 media, 7 video; PDF 1955 missing)

## [2026-05-06 01:30] [ingest] | TG @hh_ru_official — 50 постов post-Галочка (2026-03-18 → 2026-05-05): brand-statement carousel, 2-club sport-sponsorship, X5 partnership, утилитарные лайфхаки, AI «Хед Хантыч»
- source: wiki/sources/2026-05-05-tg-hh-ru-official-apr-may-2026.md
- created:
  - wiki/evolving/content-trends/hh-ru-sport-sponsorship-2026.md
- updated:
  - wiki/evolving/content-trends/hh-ru-galochka-mascot-campaign.md (+Post-finale секция: brand-statement carousel «не ради Галочки» (5 карточек) как двухступенчатый close + sub-character «Хед Хантыч» AI voice cloning + sport-кластер замещение character-нарратива)
  - wiki/evolving/content-trends/hh-ru-blog-content-patterns.md (+Формат 9: утилитарный лайфхак-пост по продуктовой фиче (TG) — 3 наблюдаемых экземпляра (язык поисковых запросов hh.ru, правило 50-70%, резюме без KPI))
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (+Hook 16 (резюме без KPI — 4 формата для не-метричных ролей) + Hook 17 (правило 50-70% — отклик при неполном соответствии); обновлена funnel-таблица)
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md (+Brand-statement self-positioning carousel (5 карточек) + Sport-sponsorship 2-club portfolio + X5 «Мастер в кубе» партнёрство + утилитарные лайфхак-фичи в TG + AI voice cloning раздел)
  - wiki/canon/marketing-frameworks/partnerships-growth-multiplier.md (+4-я механика «Corporate Pro-Competition Media Partnership» (base-кейс hh.ru × X5 «Мастер в кубе»); расширена сравнительная таблица до 4 механик)
  - wiki/evolving/competitor-positioning/hh-ru-career-marketplace.md (+Подтверждение продукта через TG (день рождения 20-24 апр 2026 со скидкой 20%); +«hh Карьеры» как обучающий sub-продукт; описание полноценного B2C-стека из 4 surfaces)
  - wiki/evolving-strict/market-data/employee-engagement-quiet-quitting-2026.md (+Цифра «33% россиян стали чаще уставать от работы» (опрос hh.ru ко Дню выгорания 28.04.2026, пост #4856) с inline-маркером)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, canon: 1, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_hh_ru_official_20260505-131555.md + 33 children (27 jpg media + 5 mp4 video + 1 mp3 audio + sidecars)

## [2026-05-06 02:00] [ingest] | TG @opora_russia — дамп 50 постов apr 24 — may 5 2026 (макро SMB-state, ЦБ 14,5% confirm, кадровый резерв 4,4 млн, офлайн розница -25 лет, кредит МСП -2,5 трлн)
- source: wiki/sources/2026-05-05-tg-opora-russia-apr-may-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-msp-credit-volume-2025.md
  - wiki/evolving-strict/market-data/ru-labor-reserve-shortage-2026.md
  - wiki/evolving/industry-trends/ru-offline-retail-decline-2026.md
  - wiki/volatile-strict/industry-news/ru-msp-q1-2026-deterioration-survey.md
- updated:
  - wiki/volatile-strict/industry-news/cb-ru-key-rate-14-5-2026-04.md (Третье независимое подтверждение ставки 14,5% через ОПОРА пост 7105; добавлен раздел про парадокс monetary easing (ставка ↓) без credit easing (52,5% кредит недоступен, -2,5 трлн МСП-кредитов в 2025); cross-link на новые ru-msp-credit-volume-2025 и ru-msp-q1-2026-deterioration-survey)
  - wiki/evolving-strict/market-data/ru-business-q1-2026-survey.md (Триангуляция Ведомости + Точка с ОПОРА/ЦСР/ТПП данными: 94,7% МСП говорят об ухудшении, 50% микро без прибыли, 65% Q1 без прибыли, 37,5% слабый спрос (vs 37,6% Ведомости — strong validation), 53% рост неплатежей (МСП острее крупного корп-сектора), 52,5% кредит недоступен, оборот р/с МСП -16%; новая narrative-layer ОПОРЫ про группу риска 20-60M руб)
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (Четвёртая независимая точка через ОПОРА пост 7130: кадровый резерв 4,4 млн человек (-9% YoY, почти ½ за 5 лет), структура 2,2+1,7+0,55, salary +13–20%/yr в дефицитных отраслях, прогноз замещения 2 млн/yr до 2030; согласовано с hh blog (1,6→4 млн дефицит) и Б1 Survey (61%→35% YoY); cross-link на новую ru-labor-reserve-shortage-2026)
  - wiki/evolving-strict/market-data/ru-franchise-market-q1-2026.md (Параллельные данные через ОПОРА пост 7146: общий объём рынка 3,81 трлн руб 2025, детализация окупаемости 58% за 12 мес / 7% >2 лет (дополняет 83% за 2 года Forbes), >50% всех предложений с порогом до 1 млн руб, структура мотивации франчайзи (58% готовая модель, 48% снижение рисков, 36% компромисс с независимостью))
  - wiki/evolving/industry-trends/ru-smb-trends-corpmsp-2025.md (Подтверждение тренда 4 (адресная поддержка) через case-study «СВОй бизнес» (ОПОРА+Единая Россия+Корпорация МСП+центры Мой бизнес+Сбер+ПСБ): 21 ветеран в Чувашии завершил модуль (с/х, ИТ, услуги, полиграфия и др.), кейс Леонида Стрелкова (центр операторов БПЛА, соц.контракт). Параллельно Премия «Бизнес-Успех» 2011-2025: 75 городов, 85K+ участников)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 4, evolving: 2, volatile-strict: 2, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_opora_russia_20260505-132056.md + 36 children (36 jpg) с .note.md/.bundle.json/.triage.json sidecars; missing tg_opora_russia_7144.pdf (приложение к посту 7144 не попало в дамп)

## [2026-05-06 02:30] [ingest] | TG @psilonsk — дамп apr 15 – may 5 2026 (range 5525..5551, 16 новых уникальных постов): hook-bank +12 хуков, channel-patterns на 9-недельное окно, AI counter-narrative эволюция
- source: wiki/sources/2026-05-05-tg-psilonsk-may-2026-extension.md
- created: none
- updated:
  - wiki/evolving/content-trends/psilonsk-management-hooks-bank.md (Добавлен раздел 11 (новые хуки из дампа 5525..5551): 11.1 Бонус ≠ компенсация неловкости (5541), 11.2 Уважай отказ от управленческой роли (5531), 11.3 Не зови сотрудников человечками + Уберите устные статусы + Защити время на менеджерское мышление (5525, 5535), 11.4 Не спрашивай о том, что не имеет отношения к работе (5536), 11.5 Эксперт един (5537), 11.6 Передумать нормально + Польза или радость + Низкая толерантность к риску за 40 (5542, 5543, 5544), 11.7 Уметь противостоять ИИ как новый навык (5545), 11.8 Сила команды в неоднородности (5532), 11.9 Скорлупа и ядра — не везде (5526), 11.10 Границы с боссом (5549), 11.11 Секретная схема = работать + Не доверяй слепо (5550, 5551). Обновлён front-matter: вторая source-страница, updated 2026-05-05.)
  - wiki/evolving/content-trends/psilonsk-channel-patterns.md (Окно наблюдения расширено с 6 до 9 недель. Метрики регулярности перестроены в трёхколонной таблице (Окно 1 / Окно 2 / Итого). Добавлено подтверждение трёхрубричного цикла на втором цикле (3 новые задачи 1197-1969..1199-1971 + 3 разбора). Подтверждена устойчиво низкая коммерческая нагрузка (1,5% feed за 9 недель). Сквозная нумерация задач подтверждена. Обновлён front-matter.)
  - wiki/evolving/content-trends/ai-control-dystopia-counter-hook.md (Confidence поднят с low до medium на основании второго независимого тезиса того же автора (5545 от 2026-04-30). Добавлена секция «Эволюция тезиса автора (мар → апр 2026)»: переход от прогноза (5496) к рекомендации навыка (5545). Добавлен вариант (d) Конструктивная рамка через 5545 — позитивная упаковка counter-narrative как «нового управленческого навыка», что снимает противоречие с AI-component GRO. Front-matter: вторая source-страница, updated 2026-05-05.)
  - wiki/canon/marketing-frameworks/environment-architecture-entrepreneur-safety.md (Добавлен cross-link на hook 11.11.2 в psilonsk-management-hooks-bank (Колганов про бильярдную, 5551) как родственный operational signal к необходимости environment design вместо контроля характеров.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, canon: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_psilonsk_20260505-135021.md + 31 children (.jpg) + sidecars (.bundle.json, .note.md, .triage.json) → status: processed

## [2026-05-06 04:30] [ingest] | TG @petrochenkow продолжение apr-may 2026 — 8-channel priority, niche-RACE, VK 4-связки, KPI parallel, TOP-5 SMB pains, AI-cheat-собес, RBC «12 кандидатов»
- source: wiki/sources/2026-05-05-tg-petrochenkow-apr-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/petrochenkov-2026-q2-channel-priority.md
  - wiki/canon/marketing-frameworks/kpi-parallel-hypothesis-petrochenkov.md
  - wiki/canon/marketing-frameworks/niche-race-leak-mapping.md
  - wiki/canon/marketing-frameworks/vk-ads-2026-niche-playbook.md
  - wiki/evolving/customer-feedback/ru-smb-owner-pains-2026.md
  - wiki/evolving/industry-trends/ai-cheat-interview-pattern-2026.md
  - wiki/evolving/content-trends/extreme-pr-event-audience-segmentation.md
  - wiki/evolving/content-trends/price-anchor-demping-content-format.md
  - wiki/evolving-strict/market-data/ru-marketer-labour-supply-2026.md
  - wiki/volatile-strict/industry-news/klimenko-foreign-traffic-rumor-2026-04.md
- updated:
  - wiki/canon/marketing-frameworks/multichannel-cumulative-effect.md (Добавлен Petrochenkov 2026-Q2 channel pack (готовый payload для multichannel-стратегии) + cross-link на 4 новые Petrochenkov-страницы)
  - wiki/canon/marketing-frameworks/marketer-hiring-questions.md (Добавлен AI-cheat защитный layer для трёх вопросов 2026 + stylometry double-check + cross-link на ai-cheat-interview-pattern-2026 и ru-marketer-labour-supply-2026)
  - wiki/canon/marketing-frameworks/hyperseg-funnel-replication.md (Добавлены cross-links на niche-RACE-leak-mapping (pre-step), kpi-parallel-hypothesis (logical extension), petrochenkov-2026-q2-channel-priority (channel selection), vk-ads-2026-niche-playbook)
  - wiki/canon/marketing-frameworks/refused-customer-interview.md (Cross-links на niche-RACE-leak-mapping (стадия утечки) и kpi-parallel-hypothesis (50 гипотез после интервью))
  - wiki/evolving/industry-trends/ai-marketing-limits-2026.md (Добавлены apr-may 2026 update-секции: (a) обратная сторона лимитов ИИ — AI-cheat собес как производное от «приемлемых, но не необходимых» LLM-ответов; (b) Petrochenkov-курс 1500₽/мес как продуктовый response рынка)
  - wiki/evolving/industry-trends/ru-marketing-digital-paralysis-mar2026.md (Добавлены apr 2026 update: recovery signals через альтернативные каналы (Petrochenkov 8-channel ranking) + рынок труда маркетологов как обратная сторона паралича (RBC 12 кандидатов))
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлен Petrochenkov 2026-04-20 update: MAX в TOP-источников качественных лидов 2026-Q2 на 8-м месте с пометкой кратный рост — третий signal от Petrochenkov в одном временном окне)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 7, evolving: 6, evolving-strict: 1, volatile-strict: 1, sources: 1}
- touched: 16 pages
- raw: raw/processed/articles/tg_petrochenkow_20260505-132353.md + 32 children (24 jpg + 8 mp4) with sidecars (.note.md, .transcript.md, .audio.mp3, .bundle.json, .triage.json)

## [2026-05-06 06:00] [ingest] | TG @egoshin_kedprof refresh — 50 постов (янв–май 2026): UAE agentic govt, РФ-экономика 2024 by сектор, Амодей token-economics, channel-pattern 60/20/15
- source: wiki/sources/2026-05-05-tg-egoshin-kedprof-may-2026.md
- created:
  - wiki/volatile-strict/industry-news/uae-agentic-government-50pct-2026.md
  - wiki/evolving-strict/market-data/ru-economy-profit-per-employee-2024.md
  - wiki/canon/marketing-frameworks/token-economics-cost-vs-value-amodei.md
  - wiki/evolving/content-trends/ai-translator-curator-channel-pattern-egoshin.md
- updated:
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md (+Government-as-validator block: UAE 50% agentic govt services (2026-04-23) как 4-й угол валидации после consumer/enterprise/mass-media; supersession watch на UAE-отчётность)
  - wiki/evolving/industry-trends/ru-ai-national-strategy-2026.md (+UAE как сравнительная модель: operational KPI vs RU infrastructural «atomic trump»; таблица различий, content-implications для B2B-сейлза)
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md (+Hook «cost равен, value различается на 8 порядков» (Амодей) с inline-маркерами + Hook «UAE government-as-validator» с anti-skeptic anchor для сегмента A; обновлены связанные материалы)
  - wiki/volatile/weekly-digest/davos-2026-ai-speakers-digest.md (+Follow-up подкасты Амодея (2026-04-30, 2,5 ч) и Хуанга (2026-05-03) как продолжение Давос-серии; Egoshin перешёл с discrete-event на continuous content-pool)
  - wiki/sources/2026-04-14-tg-egoshin-kedprof.md (+cross-link на refresh-дамп от 2026-05-05 с указанием overlap (42 поста) + 4 новых извлечения)
  - wiki/evolving/content-trends/telegram-author-channel-patterns.md (+sub-pattern AI-translator-curator (@egoshin_kedprof) как 3-я подкатегория к @hutzp/@sokolay)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 4, evolving-strict: 1, volatile: 1, volatile-strict: 1, sources: 2}
- touched: 10 pages
- raw: raw/processed/articles/tg_egoshin_kedprof_20260505-135208.md + 49 children (44 jpg + 5 mp4) with sidecars (.bundle.json, .note.md, .triage.json, 5x .transcript.md, 5x .audio.mp3)

## [2026-05-06 12:00] [ingest] | TG @forbesrussia — дамп 50 постов 4–5 мая 2026 (B1 deficit halve, мобильный интернет 5–9 мая, Cerebras IPO, 4 forbes-нативки, Минцифры open-source отказ, AI на госданных, медфраншизы +15%)
- source: wiki/sources/2026-05-05-tg-forbesrussia-may-4-5-2026.md
- created:
  - wiki/volatile-strict/industry-news/ru-mobile-internet-shutdowns-may-2026.md
  - wiki/volatile-strict/industry-news/cerebras-ipo-2026-05.md
  - wiki/volatile-strict/industry-news/apple-tsmc-diversification-2026-05.md
  - wiki/volatile-strict/industry-news/ru-mincifry-opensource-marking-rejected-2026-05.md
  - wiki/evolving-strict/market-data/ru-franchise-market-q1-2026.md
  - wiki/evolving/industry-trends/ru-mental-load-pharma-2023-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (Добавлен B1 Survey: 61% → 35% компаний с дефицитом за год (вторая независимая валидация остывания), 58% обучают, 50% аутсорс, 23% найм; 25% планируют сократить расходы на персонал)
  - wiki/volatile-strict/industry-news/ru-vpn-telegram-restrictions-2026-04.md (Добавлен cross-link к новой странице ru-mobile-internet-shutdowns-may-2026 (4-й connectivity-event))
  - wiki/evolving/industry-trends/ru-ai-national-strategy-2026.md (Добавлены 2 регуляторных конкретизатора: AI на госданных через ФСТЭК+ФСБ согласование (95645) и Минцифры отказ от маркировки open-source (95647))
  - wiki/evolving/content-trends/forbes-russia-native-ad-pattern-2026.md (Добавлены 4 свежих кейса 4–5 мая (Go Invest x2, HUTTON, Будь Здоров) + три sub-pattern: «Информационная поддержка» disclaimer (3/4), колонка эксперта на blogs.forbes.ru, brandvoice-зона. Шаблон Forbes-нативки = 3-уровневое меню)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Добавлен Hook 15 — «Новые карьерные лифты: стратегия > стаж» (Катерина Груздева, Narrators agency / E-Promo Group, через Forbes Young 95651); резонирует с B1 Survey (58% работодателей обучают))
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 5, evolving-strict: 2, evolving: 4, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/tg_forbesrussia_20260505-131943.md + 26 children (media .jpg, sidecars .note.md/.bundle.json/.triage.json)

## [2026-05-06 12:00] [ingest] | TG @rb_ru — дайджест 50 постов 24 апр – 5 май 2026 (paid Альфа-Саммит, AI-marking law, Сергиенков HH AI-displacement, Набиуллина 14,5% confirmed, T1 6 IT-трендов, MAX +60% YoY)
- source: wiki/sources/2026-05-05-tg-rb-ru-apr-24-may-5-2026.md
- created:
  - wiki/volatile-strict/industry-news/ru-ai-marking-law-2026.md
  - wiki/evolving-strict/market-data/ru-bigtech-revenue-2025.md
  - wiki/evolving/industry-trends/t1-forum-6-it-trends-2026.md
  - wiki/evolving-strict/market-data/ru-online-cinema-2025.md
- updated:
  - wiki/sources/2026-05-05-tg-rb-ru-apr-24-may-5-2026.md (New source bundle (single creation, no prior delta))
  - wiki/evolving/competitor-positioning/max-messenger.md (Добавлен раздел про rb.ru #46122 (March 2026): TG -18% YoY, 76,5% охват, MAX cohort +60% — первый числовой proof migration started; +source)
  - wiki/evolving-strict/competitor-metrics/social-platforms-ru-audience-2025.md (Добавлен раздел Динамика март 2026 с TG -18% YoY/76,5% охват/MAX cohort +60%; +source)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (Добавлена секция Сергиенков (CEO HeadHunter) на Альфа-Саммите 28 апр 2026 — public quote: маркетологи/бухгалтеры/юристы под ударом 3-5 лет, anti-alarmist рамка для GRO content; +source)
  - wiki/volatile-strict/industry-news/cb-ru-key-rate-14-5-2026-04.md (Добавлен раздел Подтверждение от Набиуллиной на Альфа-Саммите (5-й первичный источник, первое лицо ЦБ публично прогноз 14,5% на 2026, дефицит труда constant); +source)
  - wiki/evolving/industry-trends/ru-offline-retail-decline-2026.md (Добавлена секция Конкретные кейсы apr 2026: Лэтуаль 150 closures (1 млрд ₽ убыток) + Подружка/Рив Гош/Иль де Ботэ cluster-decline; М.Видео заход в food через MP (15,5% комиссия, 200→тысячи позиций) — конвергенция marketplace-категорий; +source)
  - wiki/evolving-strict/market-data/ru-ecommerce-platformization-reshetnikov-2026.md (Добавлено наблюдение №5: 289-ФЗ платформенный закон (вступление 1 окт 2026) — реестр цифровых платформ, обязательные проверки партнёров/ПВЗ, передача данных в налоговую → regulatory ceiling, парадокс усиления зависимости SMB от ТОП-3 платформ; +source)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 3, evolving: 3, volatile-strict: 2, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_rb_ru_20260505-131938.md + 48 children (40 media .jpg + 8 video .mp4) + sidecars (.bundle.json, .note.md, .triage.json, 6 .transcript.md, 6 .audio.mp3, 48 child .note.md)

## [2026-05-06 12:30] [ingest] | TG @neuraldvig — повторный дамп 50 постов за apr 29 – may 5 (RU AI corporate signals MWS+Sber+VK+Yandex, prompt-packs стабильно 12% feed)
- source: wiki/sources/2026-05-05-tg-neuraldvig-apr-29-may-5-2026.md
- created:
  - wiki/evolving/industry-trends/ru-ai-aggregator-platforms-2026.md
  - wiki/evolving-strict/market-data/sourcecraft-developer-ai-shift-2026.md
  - wiki/evolving-strict/product-metrics/vk-video-recommendation-uplift-2026.md
  - wiki/evolving/content-trends/branded-media-tg-cross-channel-pattern.md
- updated:
  - wiki/evolving/content-trends/ai-news-channel-prompt-packs.md (Воспроизводимость паттерна 12% feed/неделю (6/50 постов 2026-04-29..05-05) — повторно подтверждена; новые 6 образцов с эволюцией patterns: persona-priming эскалация до 30+ лет, эмоциональный шантаж модели, multi-turn conversation-промт, образовательная вертикаль доминирует (4/6).)
  - wiki/evolving/content-trends/ai-video-tools-stack-2026.md (Добавлена PrunaAI p-video-avatar (фото+аудио → видео-аватар, поддержка РУ-голоса, free trial через Replicate, апр 2026); +строка в сводной таблице.)
  - wiki/evolving/industry-trends/ru-vertical-ai-signals-2026.md (Добавлены сигналы 9 (MWS GPT Model Hub — RU LLM-aggregator), 10 (Sber GigaChain Крестников — community-driven open-source), 11 (VK Видео Discovery — public RU production-grade AI personalization +10%) + 11b (Алиса AI Minecraft EdTech). Синтез расширен до 11 сигналов из 4 источников.)
  - wiki/evolving/industry-trends/ai-personalization-industrial-shift-2026.md (Добавлен раздел "RU production-grade benchmark — VK Видео Discovery (+10% watch time)" — первый RU consumer-media кейс с раскрытой архитектурой и uplift-метрикой; cross-link на новую страницу метрики.)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (Добавлен Counter-anchor: ИАТЭ МИФИ Обнинск отменяет рефераты из-за AI-slop — институциональное сопротивление принимающей стороны как regulatory mechanism. +counter-anxiety hook для GRO.)
  - wiki/evolving/content-trends/telegram-native-formats.md (Обновлён @neuraldvig exemplar блок: повторный дамп через 3 недели подтверждает композицию feed (12% промт-подборок, ~50% новостей, ~36% мемов), новый ~4% компонент cross-promo techno_yandex; добавлен в sources.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 6, evolving-strict: 2, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_neuraldvig_20260505-135804.md + 50 children (37 jpg media + 13 mp4 video) with sidecars (.note.md, .triage.json, .bundle.json, 13 .transcript.md)

## [2026-05-06 14:30] [ingest] | TG @mspiridonov — дамп 50 постов apr 18 — may 5 (management-frameworks burst, Honor Lightning humanoid marathon proof-point, Tholai 5th voice on Q1-crisis, vibecoding founder-CEO normalization)
- source: wiki/sources/2026-05-05-tg-mspiridonov-apr-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/business-crisis-playbook-apollo13.md
  - wiki/canon/marketing-frameworks/pre-bite-perception-mcdonalds.md
  - wiki/canon/marketing-frameworks/hedgehog-vs-fox-strategy-2026.md
  - wiki/canon/marketing-frameworks/bavarian-backyard-self-employment-trap.md
  - wiki/canon/marketing-frameworks/dream-to-strategy-musk-vertical-integration.md
  - wiki/canon/marketing-frameworks/spiridonov-three-engagement-formats.md
  - wiki/canon/marketing-frameworks/shaq-investment-principles.md
  - wiki/volatile-strict/industry-news/honor-lightning-humanoid-marathon-2026-04.md
  - wiki/volatile-strict/industry-news/ft-autonomous-vehicle-cities-scenarios-2026.md
- updated:
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (добавлены ссылки на bavarian-backyard (diagnostic-marker), apollo13-crisis-playbook, spiridonov-three-engagement-formats (positioning-clarity GRO vs high-touch mentor-tier))
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (+5-й голос на рамку Q1-кризиса: Tholai/Metro Russia прогноз волны закрытий 2026; confidence на самой рамке поднят до high (5 независимых типов источников))
  - wiki/evolving/competitor-positioning/vibecoding-stack-ecosystem-2026.md (добавлен founder-CEO normalization signal: Спиридонов как 4-й verified-голос про vibecoding-нормализацию, 2-часовой прототип через Boost Замесина, тезис «через год-два будет таким же базовым навыком как поиск»)
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md (добавлен capabilities ramp-up sub-section: Honor Lightning Beijing humanoid марафон 2026-04-19 — 50:26 vs human 57:20, 3.2x YoY, 40% autonomous)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (добавлен positive-metaphor variant — Спиридоновский баварский дворик (3-й регистр после Высоцкий/Крылов); сопутствующие концепты динамический ноль и рынок-которого-нет; meta-вывод про яркие образы)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 8, evolving: 3, volatile-strict: 2, sources: 1}
- touched: 14 pages
- raw: raw/processed/articles/tg_mspiridonov_20260505-134643.md + 33 children (27 media + 6 video) + sidecars (.note.md, .audio.mp3, .transcript.md, .bundle.json, .triage.json)

## [2026-05-06 16:00] [ingest] | TG @kwork_kwork — re-dump 50 постов (overlap 46, delta 4: посты 561 низкоконкурентные рубрики, 562 портфолио, 563 UGC, 564 обучение под спрос), новая страница marketplace-content-driven-category-dev
- source: wiki/sources/2026-05-05-tg-kwork-may25-may26-redump.md
- created:
  - wiki/evolving/content-trends/marketplace-content-driven-category-dev.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (+ delta-блок про Kwork redump 2026-05-05 (стабильность шаблона на 11+ месяцев, минорное смещение к «герой+объект» в 562/563/564, новый pattern content-driven category development) + cross-link на новую страницу marketplace-content-driven-category-dev)
  - wiki/evolving/content-trends/freelancer-growth-narrative-hooks.md (+ Hook 5 «Учись под реальный спрос, а не вообще» (Kwork post 564, 2026-05-05) с маппингом на core-нарратив GRO и связкой с enough-vs-growth-narrative от Гребенюка)
  - wiki/evolving/industry-trends/freelance-platform-dependency.md (+ Раздел Proprietary-data как моат маркетплейса: Kwork post 561 (рубрики с низкой конкуренцией) → information lock-in + контр-нарратив GRO «не дай платформе быть твоим единственным компасом»)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_kwork_kwork_20260505-131609.md (+3 sidecars) + 50 children to raw/processed/media/ (4 new: 561-564, 46 dedup against existing)

## [2026-05-06 16:15] [ingest] | TG @fomichevkirill — incremental дамп март–май 2026 (Apr 15–May 5)
- source: wiki/sources/2026-05-05-tg-fomichevkirill-mar-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/marketing-as-product-bobkov.md
  - wiki/canon/marketing-frameworks/marketer-task-typing-fomichev.md
  - wiki/evolving-strict/market-data/workplace-context-switching-cost-2026.md
- updated:
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (+Hook 10 «наставник-визионер как ускоритель квантового скачка» (Фомичёв пост 2409, повтор тезиса от 2026-03 → устойчивый авторский нарратив для GRO-позиционирования AI-тьютор))
  - wiki/canon/marketing-frameworks/marketer-hiring-questions.md (cross-link с marketer-task-typing-fomichev (комплементарная рамка: типизация задачи ДО 3 вопросов отбора))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_fomichevkirill_20260505-135000.md + 38 jpg + 2 mp4 children (1 missing PDF tg_fomichevkirill_2377.pdf уже обработан как отдельный source 2026-05-05)

## [2026-05-06 17:00] [ingest] | TG @FounderWoman re-dump (50 постов, ids 1784..1841, март–май 2026) — overlap 1784..1819, новый контент 1820..1841, один relevant exemplar (NUSELF own-brand promo с FWOMAN15)
- source: wiki/sources/2026-05-05-tg-founderwoman-mar-may-2026.md
- created: none
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md (Добавлен новый sub-exemplar в секцию FounderWoman: NUSELF × FounderWoman own-brand commerce promo (#1828, 2026-04-24), -15% промокод FWOMAN15 до 1 мая, 7-day window, 9 product-shots; сравнительная таблица с Сбер-exemplar (external-ad vs self-brand author-promo); +источник в front-matter.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/tg_FounderWoman_20260505-132815.md (+ .bundle.json, .note.md, .triage.json) + 28 children в raw/processed/media/ (tg_FounderWoman_{1784..1791,1798,1807,1813..1817,1822..1824,1826,1828..1836}.jpg + .note.md siblings)

## [2026-05-06 17:30] [ingest] | TG @ProductsAndStartups (Аннаков) — дамп 50 постов (ids 1688..1738, mar 18 – may 5 2026), net new 1720..1738: Project Deal AI marketplace, Karpathy Software 3.0, anti-sycophancy hold-the-line, Robin AI CoS, METR pass@k, Zapier 13%, identity-через-mastery
- source: wiki/sources/2026-05-05-tg-products-and-startups-mar-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/karpathy-software-3-agentic-engineering.md
  - wiki/canon/marketing-frameworks/anti-sycophancy-system-prompt.md
  - wiki/evolving/industry-trends/ai-agent-marketplace-project-deal-2026.md
  - wiki/evolving/industry-trends/ai-cognitive-atrophy-identity-2026.md
  - wiki/evolving/competitor-positioning/onsa-robin-ai-chief-of-staff.md
  - wiki/evolving-strict/competitor-metrics/zapier-automation-bench-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md (Project Deal как первый mass-scale AI-to-AI marketplace experiment, ресурсное неравенство Opus vs Haiku +$3 advantage; cross-link)
  - wiki/canon/marketing-frameworks/harness-engineering-for-ai-agents.md (METR pass@k vs pass^k applied to model choice; 7×Haiku может давать выше надёжность чем 1×Opus)
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md (Tom's Hardware 80K Q1-2026 layoffs reframe через stock-and-flow + 275K AI-вакансий; Hans Rosling Size/Negativity Instinct)
  - wiki/evolving/content-trends/ai-product-engineer-content-hooks.md (новые хуки: Project Deal $4000, Software 3.0, identity-через-mastery, METR 80%, hold-the-line system prompt)
  - wiki/evolving/content-trends/ai-flattery-dark-pattern.md (Anthropic 1M sycophancy study 9%/25%/~50%; Opus 4.7 antidote; готовый Hold-the-line system prompt)
  - wiki/evolving/industry-trends/ai-native-marketer-skillset-2026.md (Andrew Ng Стэнфорд осень 2025: engineer:PM 7:1 → 1:1; AI Chief of Staff role)
  - wiki/canon/marketing-frameworks/karpathy-ai-60s-mainframe-analogy.md (AI Ascent 2026 эволюция нарратива vs 2024)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 6, evolving-strict: 1, sources: 1}
- touched: 13 pages
- raw: raw/processed/articles/tg_ProductsAndStartups_20260505-135131.md + 45 children (42 jpg + 3 mp4) + sidecars (.bundle.json, .note.md, .triage.json, 2 .transcript.md, 2 .audio.mp3)

## [2026-05-06 17:30] [ingest] | TG @rybakovigor — incremental дамп 50 постов 6 апр – 5 мая 2026 (Эквиум 10 лет речь "бизнес=сделка/сообщество=эволюция", взаимопроявленность essay, иллюзия данных column, СКФУ-карусель как 2-й exemplar)
- source: wiki/sources/2026-05-05-tg-rybakovigor-apr06-may05-2026.md
- created:
  - wiki/canon/marketing-frameworks/entrepreneur-manager-mode-switching.md
  - wiki/canon/marketing-frameworks/data-illusion-management-rybakov.md
  - wiki/canon/marketing-frameworks/community-as-evolution-vs-business-as-deal.md
  - wiki/evolving/content-trends/founder-history-edutainment-format.md
- updated:
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md (расширена с 10 до 16 хуков: производство времени / бизнес=сделка / одиночество / взаимопроявленность / данные приходят запоздало / паника-люкс)
  - wiki/evolving/content-trends/telegram-native-formats.md (sub-exemplar Эквиум×СКФУ 4-страничная карусель — 2-й экземпляр branded community формата)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_rybakovigor_20260505-133100.md (+ .bundle.json, .note.md, .triage.json) + 44 children to raw/processed/{media,video}/ (26 jpg + 18 mp4 + child .note.md siblings + 19 .transcript.md/.audio.mp3 sidecars)

## [2026-05-06 18:30] [ingest] | TG @recruiter_live — re-dump 50 постов apr 13 – may 3 (RU SaaS rating топ-13, HH Доступный найм МСБ, РБК top-management-hiring strict, восьмой голос про post-offer-гостинг, AI-lawsuits counter-anchor, food-retail Q1)
- source: wiki/sources/2026-05-05-tg-recruiter-live-apr-may-2026.md
- created:
  - wiki/evolving-strict/competitor-metrics/ru-saas-revenue-rating-2025.md
  - wiki/evolving-strict/market-data/ru-top-management-hiring-q1-2026.md
  - wiki/volatile-strict/industry-news/hh-ru-dostupny-naym-msb-2026-04.md
- updated:
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md (секции «Доступный найм программа МСБ 2026-04-23» и «Channel-shift к рефералкам и ТГ-каналам» + 2 млн ₽ pricing benchmark)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Hooks 19-21: внутренний рост, бизнес-survival-vignette с числами, AI на стороне сотрудника как legal риск)
  - wiki/evolving/industry-trends/ru-job-seeker-experience-2026.md (восьмой голос Taice Bulat: post-offer-гостинг)
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (post-offer-гостинг как новый временной слой communication-broken narrative + strict-цифры 60/90/180 дней)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (Counter-anchor legal-side: РБК Pro 29 апр 2026 AI-lawsuits — третий тип resistance)
  - wiki/evolving/industry-trends/ru-offline-retail-decline-2026.md (Food-retail Q1-2026 INFOline: 8/10 топ-ритейлеров замедлились)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (Complementary variant — Бизнес-survival-vignette Слава Рюмин)
- superseded: none
- sensitive flag: личные контакты автора (ti@tihragency.ru, @tihragency) и нескольких HR-авторов из LinkedIn-пересылок — в layer-страницы не перенесены
- layer-touched: {evolving-strict: 2, volatile-strict: 1, evolving: 7, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_recruiter_live_20260505-131448.md + 31 children (29 jpg + 2 mp4) + sidecars (.bundle.json, .note.md, .triage.json, .transcript.md, .audio.mp3, child .note.md)

## [2026-05-06 11:00] [ingest] | TG @startupoftheday — re-dump 50 постов apr 6 — may 5 2026 (delta 16 новых, ids 5037..5052: Gorny AI-energy debunk + token deflation theses, Claude Code course launch, Avito Работа 20M anchor, Ilant Health corp-wellness vertical)
- source: wiki/sources/2026-05-05-tg-startupoftheday-apr-may-2026.md
- created:
  - wiki/evolving/industry-trends/ai-energy-bottleneck-debunked-gorny-2026.md
  - wiki/evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026.md
  - wiki/evolving/competitor-positioning/aiacademy-claude-code-course-gorny-shevchenko-2026.md
  - wiki/evolving/competitor-positioning/avito-rabota-job-platform-2026.md
- updated:
  - wiki/evolving/content-trends/weekly-news-roundup-yt-format-gorny.md (второй thumbnail-вариант apr 30 «Где польза от AI?!»; pattern подтверждён через 9 дней)
  - wiki/evolving-strict/market-data/cbinsights-unicorns-2026-breakdown-ytd.md (sub-segment update GLP-1 corporate-wellness вертикаль: Ilant Health 2M + Lumia Health 7M)
  - wiki/evolving/industry-trends/ai-vertical-services-vc-uplift-2026.md (3-й proof-point: Ilant Health corporate-wellness vertical)
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md (anchor-точка Avito Работа 20M MAU соискателей)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 6, evolving-strict: 2, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_startupoftheday_20260505-131619.md (+ .bundle.json, .note.md, .triage.json) + 2 new children to raw/processed/media/ (5041, 5042 + .note.md siblings); 5 children already in raw/processed/ from prior ingests (5003, 5007, 5018, 5022, 5026)

## [2026-05-06 05:55] [ingest] | TG @solokumi redump 348..402 (dec25-apr26) — net-new Claude Skills/Design/Skills Bank/Refocus sales overhaul
- source: wiki/sources/2026-05-05-tg-solokumi-redump-dec25-apr26.md
- created:
  - wiki/canon/marketing-frameworks/claude-skills-architecture.md
  - wiki/canon/marketing-frameworks/landing-15min-figma-cursor.md
  - wiki/evolving/content-trends/ai-tools-self-hosting-arbitrage.md
  - wiki/evolving/content-trends/claude-code-skills-bank-2026.md
  - wiki/evolving/content-trends/sales-ops-ai-tooling-stack-2026.md
  - wiki/evolving/competitor-positioning/claude-design-2026.md
  - wiki/volatile-strict/competitor-news/anthropic-claude-design-launch-2026-04.md
- updated:
  - wiki/canon/marketing-frameworks/claude-md-structure-marketing.md (раздел Claude Code расширенные возможности: MCP, parallel agents, hooks, /init, /think, /loop+Remote Tasks+HANDOFF.md, ночное расписание, Haiku vs Opus + cross-links)
  - wiki/evolving-strict/product-metrics/refocus-germany-2026-growth.md (supersession 50→55 параметров; новый раздел стоимость QA звонков $35k→<$1k ~350× cost-effectiveness; Contradictions block; cross-link)
  - wiki/evolving/competitor-positioning/vibecoding-stack-ecosystem-2026.md (раздел Claude Design в Auxiliary; 6 новых cross-links)
  - wiki/volatile-strict/industry-news/ai-coding-tools-consolidation-2026q1.md (4 timeline entries: Atria, Claude Design + Figma -8%, Refocus sales-overhaul, Skills Bank; 5 cross-links)
- superseded:
  - wiki/evolving-strict/product-metrics/refocus-germany-2026-growth.md (50→55 параметров скоринга звонков)
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 5, evolving-strict: 1, volatile-strict: 2, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/tg_solokumi_20260505-134644.md + 4 children (380.jpg, 391.jpg, 396.jpg, 398.jpg)

## [2026-05-06 17:30] [ingest] | TG @rff_channel — re-dump 50 постов 24 мар–5 мая 2026 (overlap 4302..4348 + delta 4358..4402), 5 узких сигналов: AI-резюме poll 543 votes / 5 prompting principles / Bredova cost-of-replacement / ЭКОПСИ generations-rebuttal / HR-index 22 vs 11
- source: wiki/sources/2026-05-05-tg-rff-channel-redump-mar-may-2026.md
- created:
  - wiki/evolving-strict/market-data/ai-resume-acceptance-rff-poll-2026.md
  - wiki/canon/marketing-frameworks/ai-resume-prompting-checklist-rff.md
  - wiki/canon/marketing-frameworks/employee-retention-cost-bredova.md
  - wiki/evolving/industry-trends/generations-theory-rebuttal-ecopsy.md
- updated:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (HR-вертикаль перегрета вдвое — RFF chart 4358 HR-индекс 22 vs общий 11; C-level oklady РФ 2025-2026 от @bezaspera)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Hook 22 «AI-резюме = норм, шаблонное = нет» 543 голоса 74%; Hook 23 «Глобально TG ≈ LinkedIn для русскоязычных HR»)
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md (Practical examples с таблицей 5 complient native-ad placements + Dream Job direct UTM без брокера — pattern direct-deal жизнеспособен)
  - wiki/evolving/content-trends/telegram-native-formats.md (sub-block RFF re-dump — playbook воспроизводится + новый sub-pattern HR-вопрос-poll 543 votes)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, canon-strict: 1, evolving: 3, evolving-strict: 2, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_rff_channel_20260505-131538.md + 35 children (30 jpg media + 5 mp4 video) + sidecars (.bundle.json, .note.md, .triage.json, 5 .transcript.md, 5 .audio.mp3, 35 child .note.md). 8 PDF children отсутствуют физически

## [2026-05-06 18:00] [ingest] | TG @wtf_hr — повторный дамп 2026-05-05 (ids 2176..2228, identical к дампу 2026-04-14, zero delta, канал на паузе с окт 2025)
- source: wiki/sources/2026-05-05-tg-wtf-hr-redump.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/tg_wtf_hr_20260505-130713.md (+ .bundle.json, .note.md, .triage.json sidecars) + 23 children в raw/processed/media/ (tg_wtf_hr_{2177,2178,2181..2192,2198,2201,2203,2204,2207,2209,2213,2219,2221}.jpg + .note.md siblings); 1 missing PDF tg_wtf_hr_2211 (already absent in 2026-04-14 dump too)

## [2026-05-06 18:00] [ingest] | TG @stodnevka2 re-dump (50 постов apr 15–may 5 2026, 26 уникальных) — Petrosian newsletter cadence sustained 60d, 3 новых reusable framework (calibration, traction, book-carousel)
- source: wiki/sources/2026-05-05-tg-stodnevka2-apr-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/petrosian-monthly-calibration-3-layers.md
  - wiki/canon/marketing-frameworks/petrosian-traction-formula.md
  - wiki/evolving/content-trends/book-recommendation-carousel-tg.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (Petrosian newsletter cadence sustained на 60-дневном горизонте, письмо #7→#10, weekly cadence 3 weeks confirmed)
  - wiki/evolving/industry-trends/max-messenger-author-rejection-2026.md (Petrosian — first 60-day datapoint sustainability of TG-author offplatform-pivot)
  - wiki/evolving/content-trends/telegram-native-formats.md (новый exemplar Армен Петросян @stodnevka2: longform-эссе + книжная карусель + serial newsletter)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 4, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_stodnevka2_20260505-135212.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + 13 children to raw/processed/media/ (each with .note.md sibling)

## [2026-05-06 18:00] [ingest] | TG @techno_yandex re-dump 50 постов 26.04-05.05.2026 (3 нед спустя): GPT-5.5+GPT Image 2 + DeepSeek V4 1M context + Spotify/Oscar creative-pushback + 35% AI-websites Stanford-like + AI grief-tech market $22B→$80B + Goblin RLHF-artifact + synthetic data 2:1 ratio debate
- source: wiki/sources/2026-05-05-tg-techno-yandex-apr-may-2026.md
- created:
  - wiki/volatile-strict/competitor-news/openai-gpt55-launch-2026-04.md
  - wiki/volatile-strict/competitor-news/deepseek-v4-release-2026-04.md
  - wiki/volatile-strict/competitor-news/huawei-pura90-watch-buds2-2026-04.md
  - wiki/volatile-strict/competitor-news/dreame-aurora-modular-phone-2026-05.md
  - wiki/volatile-strict/competitor-news/spotify-verified-musician-badge-2026-05.md
  - wiki/volatile-strict/competitor-news/youtube-ai-search-premium-test-2026-05.md
  - wiki/volatile-strict/competitor-news/tesla-semi-production-2026-05.md
  - wiki/volatile-strict/competitor-news/samsung-project-luna-concept-2026-04.md
  - wiki/volatile-strict/competitor-news/yandex-tv-station-cloud-gaming-2026-05.md
  - wiki/volatile-strict/industry-news/openai-goblins-system-prompt-2026-04.md
  - wiki/evolving-strict/market-data/ai-generated-websites-share-2025.md
  - wiki/evolving/industry-trends/ai-grief-tech-market-2026.md
  - wiki/evolving/industry-trends/synthetic-data-model-collapse-debate-2026.md
  - wiki/canon/marketing-frameworks/yandex-ml-anomaly-detection-explainer.md
  - wiki/evolving/content-trends/yandex-techno-explainer-format-2026.md
- updated:
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md (GPT-5.5 launch + Goblin-RLHF case 2.5%→2/3, GPT Image 2 2K 8 связных top Elo; Second-source attestation на DeepSeek V4)
  - wiki/volatile-strict/industry-news/oscar-academy-ai-rules-2026.md (Second-source attestation от @techno_yandex 5206)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (раздел Creative-industry institutional pushback 2026-05-02..05: Oscar / Spotify / Китайский суд)
  - wiki/evolving/content-trends/ai-news-channel-prompt-packs.md (Sediment-test: @techno_yandex 0% prompt-packs vs @neuraldvig 12%×2 — pattern сегментный)
  - wiki/evolving/content-trends/ai-text-detection-landscape-2026.md (раздел AI-websites scale + perception gap: 0%→35% к середине 2025; sentiment-anomaly +107%)
  - wiki/evolving/content-trends/plastic-ai-content-pushback-hook.md (Quantitative validation 35%/+107% Stanford-like + Institutional signals Oscar+Spotify)
  - wiki/evolving-strict/market-data/app-store-slop-2026.md (Cross-domain validation web-side: AI-websites 0%→35% — triangulация с iOS submissions +84% Q1 2026)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 10, evolving: 5, evolving-strict: 2, canon: 1, sources: 1}
- touched: 23 pages
- raw: raw/processed/articles/tg_techno_yandex_20260505-140507.md + 48 children (35 media .jpg + 13 video .mp4) + sidecars (.bundle.json, .note.md, .triage.json, 7 .transcript.md, 11 .audio.mp3, 48 child .note.md)

## [2026-05-06 17:30] [ingest] | TG @t_jrnl (Тинькофф Журнал) — дамп 50 постов 01–05 мая 2026 (id 34254..34303): salary-trajectory, ageism mainstream, niche-biz long-cycle conversion
- source: wiki/sources/2026-05-05-tg-t-jrnl-may-1-5-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-salary-gap-moscow-regions-2025.md
  - wiki/evolving/content-trends/long-cycle-ridicule-conversion-niche-biz.md
- updated:
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Hook 24 «Эйджизм — общемировая проблема» План Б 158 Т-Ж: Виталий, Екатерина 47 лет — mainstream-валидация late-starter narrative)
  - wiki/evolving/content-trends/late-starter-founder-narrative-hooks.md (секция Mainstream-валидация: Т-Ж подкаст План Б 158, 2 verbatim-кейса; теперь 2 источника разной калибровки)
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (секция Долгосрочный фон: Москва/регионы 2,72×→2,39× за 2021-2025 + долларовая траектория ЗП РФ $935/$550/$1200)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_t_jrnl_20260505-132013.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + 49 jpg + 1 mp4 children в raw/processed/media|video/ (1 mp4-сайдкары: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 18:00] [ingest] | TG @techsparks refresh — 50 постов apr 11 – may 4 2026 (Tesla $25B 5-я нога, Meta CEO clone+desk move, GPT-Rosalind vertical, Geely Eva Cab native robotaxi, Hannover Messe industrial AI mainstream, Buser «Tony Stark» 3-й голос рамки усилителя, Yamshchikov shamans-wanted)
- source: wiki/sources/2026-05-05-tg-techsparks-apr-may-2026.md
- created:
  - wiki/evolving/content-trends/specialist-vs-generalist-hook-2026.md
  - wiki/volatile-strict/competitor-news/tesla-capex-25b-2026.md
  - wiki/volatile-strict/competitor-news/uber-10b-robotaxi-investment-2026-04.md
  - wiki/volatile-strict/competitor-news/openai-gpt-rosalind-2026-04.md
  - wiki/volatile-strict/industry-news/geely-eva-cab-china-native-robotaxi-2026-04.md
- updated:
  - wiki/evolving/content-trends/sebrant-cognitive-exoskeleton-hooks.md (Hooks 6-8: AI-клон руководителя, AI как костюм Тони Старка — 3-й verified голос, анти-доумерский anachronism-template; triple validation рамки усилителя)
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (расширение с 4 до 6 капитал-узлов: Tesla $25B 5-я нога; Meta CEO 6-я нога; GPT-Rosalind vertical-pivot; cross-link Apple Ternus)
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md (сигнал 4 — Geely Eva Cab native robotaxi 196B params 1400 TOPS; Sony robot table tennis Япония)
  - wiki/evolving/industry-trends/industrial-ai-measurable-roi-2026.md (Hannover Messe 2026 3000+ industrial AI exhibitors; Toyota Woven City vertical industrial AI; cross-link pharma-vertical GPT-Rosalind)
  - wiki/volatile-strict/competitor-news/uber-autonomous-strategy-pivot-2026.md (Contradictions блок: $10B+$7.5B противоречит «отказу от собственных AV»; supersession build → partner-and-operate)
  - wiki/volatile-strict/competitor-news/apple-ternus-ceo-transition-2026.md (Independent re-citation Себрантом 5566; прямая цитата Тернуса; cross-link «personal CEO commitment to AI»)
  - wiki/volatile-strict/industry-news/honor-lightning-humanoid-marathon-2026-04.md (3-й independent voice через techsparks 5564; confidence stable high через тройное подтверждение)
- superseded:
  - wiki/volatile-strict/competitor-news/uber-autonomous-strategy-pivot-2026.md
- sensitive flag: none
- layer-touched: {evolving: 4, volatile-strict: 7, sources: 1}
- touched: 13 pages
- raw: raw/processed/articles/tg_techsparks_20260505-135952.md + 43 children (43 jpg + 86 sidecar files = 129 total) with sidecars (.note.md, .bundle.json, .triage.json) → raw/processed/

## [2026-05-06 17:30] [ingest] | TG @vyakuba re-dump (50 постов apr 23 — may 5 2026): Instagram-carousel sub-genre, paid А7 integration, Спиридонов podcast collab, verified 222K Instagram
- source: wiki/sources/2026-05-05-tg-vyakuba-apr-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/ritz-carlton-empowerment-2000.md
  - wiki/canon/marketing-frameworks/premium-perception-through-price.md
  - wiki/canon/marketing-frameworks/sales-quality-vs-quantity-vyakuba-kpi.md
  - wiki/evolving/content-trends/vyakuba-instagram-carousel-format.md
- updated:
  - wiki/evolving/competitor-positioning/vyakuba-sales-training.md (verified Instagram metrics 222K +7K за 2 дня, Пхукет тур, paid-партнёрка А7 business_2, podcast со Спиридоновым, новый sub-genre Instagram-carousel)
  - wiki/evolving/content-trends/ru-sales-infobiz-content-patterns.md (Жанр 10 Instagram-carousel в TG; Жанр 11 paid-партнёрская реклама стороннего сервиса)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (Hook «Контакт сломан» 6800; Hook «Скорость = decision velocity» 6802; Hook «Деньги не портят, а усиливают» 6801)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Hook 14: два совета фаундеру от Спиридонова в подкасте Якубы — counter-balance к оптимизм-hook'ам 1-4)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 5, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_vyakuba_20260505-133315.md + 40 children (31 media .jpg + 9 video {mp4,mov} + sidecars: .bundle.json, .note.md, .triage.json, 31 child .note.md, 3 .transcript.md, 3 .audio.mp3)

## [2026-05-06 05:27] [ingest] | hr-portal.ru — Что такое HR: расшифровка термина (no relevant extractions, audit-only)
- source: wiki/sources/2026-05-05-hr-portal-chto-takoe-hr-rasshifrovka.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_chto-takoe-hr-kak-rasshifrovyvaetsya-i-chto-oznachae_5fe31e39.md (+ 3 sidecars)

## [2026-05-06 17:30] [ingest] | TG @studentsuper re-dump (SuperJob Старт) — 50 постов 2026-03-31..04-30 (overlap 21, новых 29: silence по AI-агентам, MAX-distribution-CTA, FMCG cross-promo, carousel-density)
- source: wiki/sources/2026-05-05-tg-studentsuper-redump-mar-apr-2026.md
- created: none
- updated:
  - wiki/volatile-strict/industry-news/superjob-ai-agents-marketplace-2026-04.md (TTL-проверка: silence-signal через 23 дня после анонса 6588; confidence остаётся medium, TTL продлён до 2026-06-06)
  - wiki/volatile/weekly-digest/tg-studentsuper-mar-apr-2026.md (Update re-dump: 6 новых блоков — silence по AI-агентам, MAX-distribution-CTA, Сенежская × SuperJob FMCG-партнёрство, carousel-density, Cosmonautics holiday gamified, lifestyle-vacancy Tinkoff-style)
  - wiki/evolving/competitor-positioning/max-messenger.md (раздел Federal-tier B2C: SuperJob Старт corporate distribution-CTA с 2026-04-27; 3 поста за 4 дня max.ru/superjob; каскадная адопция MAX в job-marketplace через ~4 нед после hh.ru)
  - wiki/evolving/content-trends/telegram-native-formats.md (раздел Exemplar update SuperJob Старт re-dump: corporate carousel-density 22%, FMCG cross-promo Сенежская × SuperJob erid 2VtzqwqmG1d, holiday-themed gamified, lifestyle-vacancy Tinkoff-style joke 6616)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, volatile: 1, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_studentsuper_20260505-131617.md (+3 sidecars) + 47 children (10 video + 37 media) с .note.md/.transcript.md/.audio.mp3 sidecars

## [2026-05-06 18:30] [ingest] | TG @Theedinorogblog incremental dump 50 постов apr 21 — may 5 (TG-эрозия 3-й источник, AI-валюация-race ускорилась, Smart Ranking second-source, Cofix×Я.Пэй QR кейс, Adapty unicorn-trajectory, AI-law two-step, Filonov editorial-skepticism cluster)
- source: wiki/sources/2026-05-05-tg-theedinorog-apr-may-2026.md
- created:
  - wiki/evolving/content-trends/competitor-data-poisoning-defense-pattern.md
  - wiki/evolving/content-trends/qr-loyalty-integration-cofix-yandex-pay.md
  - wiki/evolving-strict/competitor-metrics/adapty-ru-saas-benchmark-2026.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (Edinorog 7896 Digital Budget: TG -18% YoY март, MAX +61%, Telega +260%, VK Мессенджер +0,4% — третий независимый источник; Forbes-Дуров $7,1B → $2,6B сравнение со Snapchat)
  - wiki/evolving-strict/competitor-metrics/social-platforms-ru-audience-2025.md (disaggregated раздел Digital Budget: TG -18%/-10%, MAX +61%, Telega.in +260%, VK Мессенджер +0,4% — три-источная триангуляция)
  - wiki/evolving-strict/market-data/ru-bigtech-revenue-2025.md (Smart Ranking 100 second-source: 8,8 трлн ₽ vs rb.ru 8,9 трлн; 76,4% концентрация топ-10 vs 70%; антилидеры Carprice/Postgres/BIA)
  - wiki/evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2.md (Anthropic $300B secondary, $400B новый primary раунд; OpenAI $80B secondary, internal targets miss WSJ; Brockman self-claim $50B доли)
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (8-й вектор regulatory squeeze: AI-закон two-step pattern либерализация 2026-04-27 → реестр+ФСТЭК+ФСБ для суверенных моделей 2026-05-05; header «Пять» → «Восемь»)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (Hook 15 Editorial-skepticism cluster Filonov: 5 case-studies Citix/JagaJam/2GIS/Neiry/eFishery; Hook 16 AlinaRutina/Rutina.me virtual-team-replacement)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, evolving-strict: 4, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_Theedinorogblog_20260505-133834.md + 36 children (30 jpg media + 6 mp4 video) + sidecars (.bundle.json, .note.md, .triage.json, 2 .transcript.md for 7877.mp4 + 7910.mp4 + .audio.mp3 siblings, 36 child .note.md)

## [2026-05-06 05:30] [ingest] | HR-Portal: методы и технологии подбора персонала (canon-таксономия HR)
- source: wiki/sources/2026-05-05-hr-portal-metody-podbora-personala.md
- created:
  - wiki/canon/marketing-frameworks/recruitment-methods-taxonomy.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_metody-i-tehnologii-podbora-personala_b6009e3c.md (+ 3 sidecars)

## [2026-05-06 17:30] [ingest] | dp.ru — СПб средняя зарплата >125k ₽ фев 2026 + AI-attribution к overflow в маркетинге/консалтинге (5-й Q1 cooling источник, narrative-сдвиг)
- source: wiki/sources/2026-05-04-dp-ru-spb-wages-feb-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-spb-labor-market-feb-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md (секция СПб срез февраль 2026 — пятая независимая точка cooling: dp.ru/РИА/Росстат; >125k ₽, РФ +15% YoY, СПб -21%/+25% YoY, AI+investment-freeze attribution)
  - wiki/evolving-strict/market-data/ru-salary-gap-moscow-regions-2025.md (Q1 2026 точка по СПб >125k и регионам; Чукотка 223k янв, Хабаровский край +23% YoY)
  - wiki/evolving-strict/market-data/ru-marketer-labour-supply-2026.md (СПб срез — dp.ru как 4-й независимый proof-point: первое массовое деловое СМИ с AI-attribution; investment-freeze 4-я причина overflow)
  - wiki/evolving/industry-trends/ru-marketing-digital-paralysis-mar2026.md (May 2026 narrative-сдвиг: AI-attribution в массовом СМИ + investment-freeze 4-я причина; СПб -21%/+25%)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Hook 25 — СПб локализованный AI-displacement: рез +25%/вак -21% YoY)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 4, evolving: 2, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_04_srednjaja-zarplata-v-peterburge_ae634d39.md (+ 3 sidecars: .note.md, .triage.json, .bundle.json)

## [2026-05-06 12:35] [ingest] | TG @typicalcompany — re-dump 50 постов (overlap 1273..1329, новый пост 1330: $5,6 млн revenue/empl. AI-вендоров + рамка 3 сдвига)
- source: wiki/sources/2026-05-05-tg-typicalcompany-may-2026-redump.md
- created:
  - wiki/evolving-strict/market-data/ai-vendor-revenue-per-employee-2026.md
  - wiki/canon/marketing-frameworks/ai-productivity-3-shifts-typical.md
- updated:
  - wiki/evolving/industry-trends/ai-for-managers-2025-2026.md (4-я data-точка: revenue/empl. AI-вендоров vs Mag 7 как количественный proof; unified-сигнал из 4 точек)
  - wiki/evolving/industry-trends/ai-knowledge-worker-climb-2025-2026.md (Сигнал 8: revenue/empl. AI-вендоров Anthropic $5,6M vs Apple $2,4M)
  - wiki/evolving/competitor-positioning/typical-company.md (continuity-update раздел 10-недельного content-pause Mar–May 2026; thematic shift к AI-productivity нарративу)
  - wiki/evolving/content-trends/telegram-native-formats.md (наблюдение про continuity-проверку TYPICAL re-dump через 3 недели: pause-режим как normal lifecycle)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 1, canon: 1, evolving: 4, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_typicalcompany_20260505-134515.md + 23 children (21 jpg media + 1 ogg audio + 1 mp4 video) + sidecars (.bundle.json, .note.md, .triage.json, 2 .transcript.md, 2 .audio.mp3, 22 child .note.md); 1 missing (tg_typicalcompany_1293.avif)

## [2026-05-06 17:30] [ingest] | HR-Portal: обзор методов отбора (оценки) кандидата — комплементарная RU-таксономия (5 традиционных + 6 нетрадиционных методов)
- source: wiki/sources/2026-05-05-hr-portal-obzor-metodov-otbora-personala.md
- created:
  - wiki/canon/marketing-frameworks/candidate-selection-methods-taxonomy.md
- updated:
  - wiki/canon/marketing-frameworks/recruitment-methods-taxonomy.md (cross-link на новую candidate-selection-methods-taxonomy; +source)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_obzor-metodov-otbora-personala_43b67d9b.md (+ 3 sidecars)

## [2026-05-06 18:30] [ingest] | dp.ru — Минпромторг параллельный импорт IT (2026-05-04) — supersession brand-list 6-го вектора + новые dedicated-страницы по приказу 27 мая 2026 и динамике объёма
- source: wiki/sources/2026-05-04-dp-ru-minpromtorg-parallel-import-laptops.md
- created:
  - wiki/volatile-strict/industry-news/ru-minpromtorg-parallel-import-stop-2026-05.md
  - wiki/evolving-strict/market-data/ru-parallel-import-volume-2022-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (6-й вектор Минпромторг: supersession brand-list — корректное прочтение приказа = 10 брендов под полным запретом, не 4 «исключения»; quantitative baseline $4 млрд → $1 млрд −75%; целевая доля 50%, техсбор 250/500 ₽; раздел Contradictions)
- superseded:
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (6-й вектор brand-list: bezsmuzi false reading → ДП правильное)
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving-strict: 1, evolving: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_04_v-minpromtorge-zajavili--chto_7a5d7fd1.md (+ .note.md, .triage.json, .bundle.json)

## [2026-05-06 17:30] [ingest] | TG @vcnews — дамп 50 постов 02–05 мая 2026 (продолжение апрельского среза, ~85% дублирующая second-source аттестация + 5 новых сигналов)
- source: wiki/sources/2026-05-05-tg-vcnews-may-2-5-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-self-employed-2025.md
- updated:
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (9-й вектор: банковские P2P-чаты в режиме disable Сбер+Т-Банк white-list compliance; vcnews 61196/61210)
  - wiki/volatile-strict/industry-news/ru-mobile-internet-shutdowns-may-2026.md (vcnews chronology consolidation 61184/61199/61204/61206/61210; white-list сами не работали в первый час; первое прямое предупреждение Яндекс Go и Сбер)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (Addendum седьмой голос: РСПП corporate-уровень + consumer-footfall впервые с пандемии)
  - wiki/volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05.md (vcnews 61216 как 4-й второ-источник для TickerTrends-данных)
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (vcnews второ-источник для DeployCo/Cerebras/Panthalassa посты 61195/61190/61214)
  - wiki/volatile-strict/competitor-news/openai-spinoff-rejected-pre-ipo-2026-05.md (vcnews 61205 как 3-й второ-источник)
  - wiki/volatile-strict/industry-news/cerebras-ipo-2026-05.md (vcnews 61190 как второ-источник)
  - wiki/volatile-strict/industry-news/amsterdam-outdoor-ad-ban-2026.md (vcnews 61198 как 3-й второ-источник)
  - wiki/volatile-strict/industry-news/apple-tsmc-diversification-2026-05.md (vcnews 61207 как второ-источник)
  - wiki/volatile-strict/competitor-news/replit-stripe-3digit-growth-2026-05.md (vcnews 61200 как 3-й второ-источник)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 1, volatile-strict: 6, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_vcnews_20260505-131655.md + 48 children (42 media + 6 video) with sidecars (.note.md, .triage.json, .bundle.json, 5 .transcript.md)

## [2026-05-06 12:00] [ingest] | hr-portal.ru — стратегия фокусирования (Porter focus strategy): canonical framework page + GRO anti-positioning structural argument
- source: wiki/sources/2026-05-05-hr-portal-focus-strategy.md
- created:
  - wiki/canon/marketing-frameworks/focus-strategy-porter.md
- updated:
  - wiki/canon/marketing-frameworks/microniche-marketing-packages.md (cross-link на parent-фрейм focus-strategy-porter; microniche packaging как операционная реализация differentiation focus через partnership)
  - wiki/canon/positioning/gro-value-proposition.md (раздел про focus strategy Porter как структурную рамку для anti-positioning GRO: differentiation focus в узкой нише ежедневных тренировок)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_strategiya-fokusirovaniya-i-ee-ispolzovanie-v-biznes_a3e14db2.md (+ 3 sidecars: .note.md, .triage.json, .bundle.json)

## [2026-05-06 17:30] [ingest] | dp.ru — расширенная программа ПМЭФ-2026 (3-6 июня): трек «новые медиа и реклама», роботизация/кадры в ~20 сессиях, ШОС/БРИКС МСП
- source: wiki/sources/2026-05-04-dp-ru-pmef-2026-program-announcement.md
- created:
  - wiki/volatile-strict/industry-news/pmef-2026-program-announcement.md
- updated:
  - wiki/evolving/industry-trends/ru-ai-national-strategy-2026.md (раздел «ПМЭФ-2026 как event-якорь стратегии» — ШОС/БРИКС МСП внутри программы как операционный venue п.7)
  - wiki/evolving/industry-trends/ru-retail-robotization-labor-deficit-2025-2026.md (раздел Government-visibility: роботизация и кадры — 2 из ~20 дискуссионных сессий ПМЭФ-2026; эскалация нишевой темы до федеральной повестки)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_04_v-rasshirennoj-programme-pmjef_d4cbcb13.md (+ .bundle.json, .note.md, .triage.json sidecars)

## [2026-05-06 08:30] [ingest] | TG @temno — Аркадий Морейнис re-dump апр–май 2026 (50 постов, 12 overlap + 38 новых, 5 canon-фреймовок и 3 направления миграции ценности)
- source: wiki/sources/2026-05-05-tg-temno-moreynis-apr-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/loss-aversion-product-moreynis.md
  - wiki/canon/marketing-frameworks/jevons-paradox-ai-positioning.md
  - wiki/canon/marketing-frameworks/disproportionality-hypothesis-moreynis.md
  - wiki/canon/marketing-frameworks/david-tricks-vs-goliath-startup-strategy.md
  - wiki/canon/marketing-frameworks/return-on-time-moreynis.md
- updated:
  - wiki/canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis.md (расширен с 8 до 10 правил: 9 разработчики ИИ-платформ → консультанты; 10 ИИ-франшиза как extreme правила 1; YC RFS triangulation)
  - wiki/evolving/industry-trends/ai-value-migration-2026.md (3 новых направления миграции: атомизация рынков под ИИ + Коуз; ИИ-франшиза; софт для ИИ-агентов; YC RFS 2026 + Tomasz Tunguz cost-ratio 10:1/4:1/25:1)
  - wiki/evolving/content-trends/moreynis-hand-drawn-meme-format.md (confidence повышен с medium до high после второго подтверждения через 4 недели; 96% постов; production-ready формат)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (самый сильный экономический counter-anchor — парадокс Джевонса 1865 от Аарона Леви Box через Морейниса; 3 условия применимости)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (4 cross-links на новые canon-страницы Морейниса с operational-описанием; loss-aversion retention; ROT core operational reformulation; disproportionality для onboarding; Jevons counter-anchor для AI-anxious founders)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving: 3, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_temno_20260505-132554.md + 50 children (50 jpg media) with sidecars (.note.md, .triage.json, .bundle.json)

## [2026-05-06 17:30] [ingest] | hr-portal.ru — Требования к менеджеру по подбору персонала (audit-only, no relevant extractions)
- source: wiki/sources/2026-05-05-hr-portal-ru-article-trebovaniya-k-menedzheru-po-podboru-personala.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_trebovaniya-k-menedzheru-po-podboru-personala_9bc38270.md (+ .bundle.json, .note.md, .triage.json)

## [2026-05-06 17:30] [ingest] | TG @your_pet_project (Табунов) re-dump 50 постов фев-май 2026 — DoD framework, Bootstrap vs Startup, Zero-to-one vs Scale, Blue Ocean anti-pattern, Glority paint-by-numbers, Den case, solopreneur boom Q1-Q2 indicators
- source: wiki/sources/2026-05-05-tg-your-pet-project-feb-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/definition-of-done-product-positioning.md
  - wiki/canon/marketing-frameworks/bootstrap-vs-startup-tabunov.md
  - wiki/canon/marketing-frameworks/zero-to-one-vs-scale-tabunov.md
  - wiki/canon/marketing-frameworks/blue-ocean-strategy-anti-pattern.md
  - wiki/evolving-strict/competitor-metrics/glority-global-paint-by-numbers-publisher.md
  - wiki/evolving-strict/market-data/solopreneur-boom-indicators-2026-q2.md
- updated:
  - wiki/volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026.md (Den RU TG-бот для генерации картинок Baza: $1K → $1.2K за 2 мес, x3 окупаемость, 32K юзеров, 4-й запуск; Image_611 OCR с profit-vs-revenue контрастом)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (confidence upgrade до 4 голосов; Solo vs micro-team x50 iteration speed; Glority paint-by-numbers; Counter-anchor «30 валидных ниш» vs 235K App Store apps; Contradictions block)
  - wiki/evolving/content-trends/your-pet-project-channel-hooks.md (8 sub-секций hooks из delta дампа: DoD positioning, Bootstrap vs Startup, Zero-to-one vs Scale, Blue Ocean anti-pattern, 180 секунд, Solo vs Micro-team, Glority, Pruefs, Multi-launch persistence Den, Solopreneur boom)
  - wiki/canon/marketing-frameworks/tabunov-onboarding-principles.md (180-секундный extended walkthrough пост 613: детальный antipattern-сценарий по секундам)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (Hook 25 «Пет-проект как pruefs > отсиженный опыт» Табунов 618: 800 откликов, 80% без пруфов, NDA)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving-strict: 2, evolving: 3, volatile-strict: 1, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/tg_your_pet_project_20260505-132611.md + 22 children (20 jpg media + 2 mp4 video) + sidecars (.note.md, .triage.json, .bundle.json, 2 .transcript.md, 2 .audio.mp3, 2 child .note.md)
## [2026-05-06 11:50] [ingest] | YouTube «НЕскучные ФИнансы» — разбор автомойки/СТО на Авито за 2 млн ₽ (Цветков, bundle 1+3 children)
- source: wiki/sources/2026-05-05-yt-neskuchnye-finansy-avtomoyka-avito-razbor.md
- created:
  - wiki/evolving/content-trends/avito-business-autopsy-yt-format-2026.md
- updated:
  - wiki/evolving/content-trends/ready-business-purchase-narrative-hooks.md (Добавлена 6-я категория hooks (red-flag сканер по marketplace-листингу) с 7 переносимыми хуками + sub-кластер anti-pattern «investor-absentee owner» с 3 хуками; обновлён updated, добавлен новый source и cross-link к format-странице)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Добавлен раздел «Зеркальный anti-pattern: investor-absentee owner» с сравнительной таблицей и ICP-boundary clarification (этот владелец — НЕ ICP GRO), diagnostic-маркер при сегментации лидов, контент-импликация)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, canon: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/yt_0Ci1OIX_750.md + 3 audio children (m4a + audio.mp3 + transcript.md, все sidecars: bundle.json, note.md×2, triage.json)

## [2026-05-06 11:50] [ingest] | YT Маргулан Сейсембай — 6 типов токсичных людей: canon HR-фильтр + narrative-хуки для founder-сегмента (1-й из 4 видео из scheduled-задачи)
- source: wiki/sources/2026-05-05-yt-margulan-six-toxic-types.md
- created:
  - wiki/canon/marketing-frameworks/seissembai-six-toxic-types-filter.md
  - wiki/evolving/content-trends/seissembai-people-filter-narrative-hooks.md
- updated:
  - wiki/canon/marketing-frameworks/environment-architecture-entrepreneur-safety.md (+cross-link на Сейсембая как operational-фильтр для среды «Люди» (Рыбаков — макро/структура, Сейсембай — микро/операция); +source)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+секция «Operational HR-фильтр для сегмента: 6 типов токсичных контактов (enrich 2026-05-06)» — гордец-руководитель как consrervative bottleneck; personal-circle hygiene в контексте JTBD «помоги мне поверить»; tactical playbook исторических связей; 3 marketing-применимости; +2 cross-links в Связанных страницах; +source)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/yt_abVi-meHRBU.md + 3 audio children (m4a primary, .audio.mp3 normalized, .transcript.md whisper-1)

## [2026-05-06 11:50] [ingest] | YT Бизнес с нуля (Муратаев) — выпуск #4 велобайк-серии: B2B-пивот через «Важную Рыбу» + полный март-ДДС (959K revenue, 417K NCFO, 4.8M investment, 10+ мес окупаемость), новые pages b2b-anchor-pivot + electrobike-rental-unit-economics-2026
- source: wiki/sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc.md
- created:
  - wiki/evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026.md
  - wiki/canon/marketing-frameworks/b2b-pivot-anchor-customer-smb.md
- updated:
  - wiki/canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev.md (Re-confirmation секция из выпуска #4: 5 новых operational-illustrations принципа (3D-печать запчастей, бумажка вместо изъятия, переманивание партнёра, ДДС vs АПУ как admission, колхозный фен-припой крыла); +cross-link на новый b2b-pivot-anchor-customer-smb.md)
  - wiki/evolving/content-trends/biznes-s-nulya-founder-diy-format-2026.md (Новая секция «Financial-recap sub-format» — 9-й структурный элемент founder-DIY формата (monthly DDS recap каждый ~4-й эпизод проекта); cadence pattern; founder-explainer как content-template)
  - wiki/canon/marketing-frameworks/business-reality-show-format.md (Internal sub-cadence observation: founder-DIY имеет financial-recap раз в ~4 эпизода как monthly close as content; +источник #6 в front-matter)
  - wiki/canon/marketing-frameworks/business-metrics-for-owners.md (Большая applied-case секция: ДДС vs АПУ vs амортизация на примере rental-бизнеса Муратаева (47 байков × 75K × 3.5% = 123K monthly amortization vs 417K NCFO → real break-even 16-17 мес); founder-explainer как content-pattern для GRO)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Team-structure deepening для hands-on-builder архетипа: founder + ops + переманенный technical (Ахмат 72% ФОТ, salary-floor 2× от прежнего бизнеса); network-driven hiring vs formal recruiting; B2B-anchor через бизнес-клуб как acquisition-pattern; ICP-implication для GRO (lightweight team coordination для 3-5 человек))
  - wiki/canon/marketing-frameworks/breakage-business-model-fitness.md (Complementary mechanic секция: service-as-retention в rental-бизнесах = противоположность breakage (high engagement, retention через quality service на месте); cross-link на electrobike-month4 source и unit-economics)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 1, evolving-strict: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/yt_GObhZh076W4.md (+ 3 sidecars: .note.md, .bundle.json, .triage.json) + raw/processed/audio/yt_GObhZh076W4.m4a (+ 3 sidecars: .note.md, .audio.mp3, .transcript.md)

## [2026-05-06 11:50] [ingest] | YouTube Илья Соловей #2/5 — Северсталь / Череповецкий завод: контр-интуитивный location-bet, pivot нарратива 1956, Мордашов post-Soviet, export-pivot через прямые отношения, моногород-стратегия (формат канала: 2-е подтверждение, low → medium)
- source: wiki/sources/2026-05-05-yt-ilya-solovey-severstal-history.md
- created:
  - wiki/canon-strict/historical-campaigns/severstal-cherepovets-transformation.md
  - wiki/canon/marketing-frameworks/contrarian-location-bet-logistics-vs-resources.md
  - wiki/canon/marketing-frameworks/quality-over-quantity-pivot-narrative.md
  - wiki/canon/marketing-frameworks/post-soviet-90s-export-pivot-playbook.md
  - wiki/canon/marketing-frameworks/monogorod-employer-brand-stewardship.md
- updated:
  - wiki/evolving/content-trends/business-history-documentary-format-ru.md (2-я точка наблюдения формата канала Соловья (Северсталь): confidence повышен low → medium, добавлена comparison-таблица 8 структурных признаков (все подтверждены), новое наблюдение про расширенный mid-roll Boosty product-placement и telegram-CTA как cross-platform monetization-funnel)
  - wiki/canon/marketing-frameworks/distressed-asset-consolidation-playbook.md (Добавлен параллельный кейс Алексей Мордашов / Северсталь как 2-й post-Soviet RU founder-CEO в playbook'е. Critical difference: insider (Мордашов) vs outsider (Филёвы) acquisition — playbook расщеплён на 2 sub-варианта. Rouge Steel 2003 как пример international distressed-asset bet расширяет применимость)
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, canon: 5, evolving: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/yt_5ZA3gCb80dM.md + 7 sidecars (.bundle.json, .note.md, .triage.json + audio: .m4a, .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 11:50] [ingest] | YouTube Илья Соловей #5/5 финальный — РЖД (state-monopoly / public-infrastructure, 21:08): низкий substance-yield, формат канала fully canonical на 5 trans-governance точках
- source: wiki/sources/2026-05-05-yt-ilya-solovey-rzd-russian-railways.md
- created:none
- updated:
  - wiki/evolving/content-trends/business-history-documentary-format-ru.md (5-я финальная точка наблюдения формата Соловья (РЖД, state-monopoly / public-infrastructure). Status: fully canonical (5/5 trans-domain, trans-governance подтверждение). NEW: hook-репертуар расширен 4-м sub-pattern (statistical-bombshell в дополнение к descriptive 3/5 и provocative-quote 1/5); pre-emptive teaser current-events и расширенный Boosty mid-roll подтверждены как устойчивые selective patterns (2/5 каждый); pre-roll sponsorship финально 1/5 (одиночный outlier Porsche). Гипотеза «формат специфичен для founder-driven кейсов» разрушена РЖД-кейсом — формат универсален для governance-types (private-corporate / state-monopoly / dynasty / serial-entrepreneur). Substance-yield variability: subject-driven (РЖД ~0 frameworks, Андреев 5+, Северсталь/Porsche по 4); формат systemic, substance subject-driven.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/yt_iA1LNACOVrE.md + 3 children (raw/processed/audio/yt_iA1LNACOVrE.m4a, .audio.mp3, .transcript.md) + 4 sidecars (.bundle.json, .triage.json, 2× .note.md)

## [2026-05-06 11:50] [ingest] | YT Спиридонов #2/5 — Reels/Shorts разрушают префронтальную кору (2:29 + Klingon-track meta-format)
- source: wiki/sources/2026-05-06-yt-spiridonov-reels-prefrontal-eeg.md
- created:
  - wiki/evolving/content-trends/yt-multitrack-audio-meta-format-spiridonov.md
- updated:
  - wiki/evolving/content-trends/social-media-addiction-design-patterns.md (добавлен biological-layer (ЭЭГ-evidence Гентского университета n=48 + hook-цитата Спиридонова + cross-link на yt-multitrack-meta-format))
  - wiki/evolving/content-trends/short-form-video-algo-retention-2026.md (добавлена attention-cost-сторона как complement к algorithm-side, cross-link на social-media-addiction и yt-multitrack-meta-format)
  - wiki/canon/marketing-frameworks/signal-noise-essentialism-spiridonov.md (добавлен раздел Companion-piece про видео #2 (ЭЭГ + Klingon-track) как биологическая иллюстрация концепции шума)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, canon: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/yt_ALETk5S0-Nc.md + 3 children (audio: .m4a + .audio.mp3 + .transcript.md) + sidecars (.note.md ×2, .bundle.json, .triage.json)

## [2026-05-06 11:50] [ingest] | YT Максим Батырев #2/3 — выпуск 1–15 марта 2026 (conservative hub-extension): fog vs clarity, IndiGo structural blindness, Паспорт функции на одну страницу, 3 пункта программы трансформации
- source: wiki/sources/2026-05-05-yt-batyrev-management-news-mar1-15.md
- created:none
- updated:
  - wiki/canon/marketing-frameworks/work-recomposition-batyrev.md (+«Fog vs Clarity» как сквозная рамка пересборки; +«3 обязательных пункта программы трансформации» (результат-в-деньгах + срок + ответственный); +Anti-pattern «средняя температура по больнице» (ВШЭ Q4 2025); +полный раздел «Паспорт функции на одну страницу» (parallel-инструмент к 4 корзинам, для функции/подразделения); +формат «Три действия руководителя на 2 недели» как canonical-структура)
  - wiki/canon/marketing-frameworks/four-baskets-of-roles-batyrev.md (+cross-link на Паспорт функции как complementary-инструмент (4 корзины — для роли, паспорт — для функции/подразделения); +second source link; +кейс отдела сопровождения B2B)
  - wiki/canon/marketing-frameworks/meta-error-batyrev-asymmetric-signals.md (+Sibling-pattern «IndiGo / структурная слепота при системных изменениях» с полным разбором (3 причины слепоты, 5 слоёв удара, 7-вопросный тест перед нормативным изменением); +сравнительная таблица Meta-error vs IndiGo-error)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+Operational instruments из выпуска 1–15 марта: «3 пункта программы трансформации» (результат-в-деньгах + срок + ответственный) как self-test для founder; +«Паспорт функции» — typical-кейсы (отдел продаж, founder-self) для пересборки на функционо-уровне; +«Разговор ясности» (single-page-обсуждение направления) как diagnostic-tool с 7-вопросной структурой)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/yt_-cKYU0IEE7o.md (+ 3 sidecars: .note.md, .bundle.json, .triage.json) + raw/processed/audio/yt_-cKYU0IEE7o.m4a (+ 3 sidecars: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 11:50] [ingest] | YouTube «Предприниматель ДЕла» #2/4 — Сергей Васильев ERP/Google Sheets (Слёт героев speaker-cut): ERP-vs-CRM distinction + Табличный биатлон (~100K ₽ mebel-only edu-product) + speaker-carousel mechanic revealed
- source: wiki/sources/2026-05-05-yt-predprinimatel-dela-vasilyev-erp-google-sheets.md
- created:
  - wiki/canon/marketing-frameworks/erp-vs-crm-smb-distinction.md
  - wiki/evolving/competitor-positioning/tablichnyj-biatlon-niche-vertical-edu-product.md
- updated:
  - wiki/evolving/content-trends/factory-tour-pro-day-event-format.md (Добавлен раздел Speaker-carousel внутри основного дня — revealed mechanic peer-validated speaker-pipeline + content-pipeline (1 Слёт = N speaker-видео в году); cross-links на новые vendor-product и concept страницы.)
  - wiki/evolving/competitor-positioning/predprinimatel-dela-channel-pattern.md (Добавлен раздел Content-archetypes канала (3 archetypes: factory-tour / event-speaker-cut / vendor-spotlight-doc) + Ecosystem-builder pattern (Дмитриев = trust-broker для приглашённых vendors из собственного бизнеса). Caveat обновлён, что после 2-х из 4-х ингестов пока остаётся confidence: low, но picture richer.)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Добавлен Diagnostic-маркер «ERP-CRM схлапывание» (production-слой сегмента): founder с production-фазой массово схлапывает CRM/ERP в одну систему. Контентный hook GRO как третий слой stack-а (sales / fulfillment / founder-effectiveness). Cross-link на новый ERP-CRM framework и Васильев-vendor-product страницы.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 3, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/yt_jC1Udb6H720.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + raw/processed/audio/yt_jC1Udb6H720.m4a (+ 3 sidecars: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 11:50] [ingest] | YouTube «Предприниматель ДЕла» #4/4 (final) — китайский завод адгезивов Mr. Джу: PUR/EVA 3.4:1, 8000т warehouse, 4-й content-archetype delegation-trip-doc
- source: wiki/sources/2026-05-05-yt-predprinimatel-dela-china-adhesive-factory-tour.md
- created:none
- updated:
  - wiki/evolving/competitor-positioning/predprinimatel-dela-channel-pattern.md (4-й content-archetype delegation-trip-doc confirmed; cross-source recognition в Китае; graduated-access pattern (4 визита → закрытые цеха); time-locked content moat)
  - wiki/evolving/industry-trends/ru-manufacturing-china-pivot-2022-2026.md (PUR/EVA 3.4:1 production-volume cross-source signal с китайского Tier-1; full-palette gap RU-distribution (5 цветов PUR, чёрный недоступен); marketing-implication «PUR-tooling = sufficient differentiator 2026»)
  - wiki/evolving/content-trends/factory-tour-pro-day-event-format.md (+ #4/4 source как 4-я confirmation стандартного 3-min promo-tail; новая страница sources в front-matter)
  - wiki/evolving/industry-trends/ru-retail-robotization-labor-deficit-2025-2026.md (Cross-source labor-efficiency signal: 1 оператор/смена на 8000т smart-warehouse (Китай #4/4) — China-supplier-tour proof для RU labor-deficit narrative)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/yt_RjR2ijCieKM.md + 3 children (audio/m4a + audio/mp3 + transcript)

## [2026-05-06 11:55] [ingest] | YouTube «Бизнес с нуля» #2/5 — фитнес-клуб 2000 м² (Илья, СПб Невский): юнит-экономика 130/30 млн, breakage 91%, founder-interview format extension, DDX/Sportlife рыночный контекст
- source: wiki/sources/2026-05-05-yt-biznes-s-nulya-fitness-club-economics.md
- created:
  - wiki/evolving-strict/market-data/ru-fitness-club-unit-economics-2026.md
  - wiki/canon/marketing-frameworks/breakage-business-model-fitness.md
  - wiki/evolving/industry-trends/ru-fitness-market-2016-2026.md
  - wiki/canon/marketing-frameworks/trainer-rental-marketplace-model.md
  - wiki/canon/marketing-frameworks/construction-site-content-marketing.md
- updated:
  - wiki/evolving/content-trends/biznes-s-nulya-founder-diy-format-2026.md (Канал «Бизнес с нуля» использует ДВА формата (founder-DIY + founder-interview), второй разобран на примере выпуска про фитнес-клуб Ильи: 8 структурных элементов interview-формата (friend-frame, quick-math hook, walk-through, side-quest gag, honest math reset, mid-roll лайфхак ad, розыгрыш CTA, closing wisdom))
  - wiki/canon/marketing-frameworks/business-reality-show-format.md (Расширена 4-членная типология до 5-членной: добавлен founder-interview (Муратаев visiting Илью с фитнес-клубом). Канал «Бизнес с нуля» уникален тем, что использует одновременно DIY и interview форматы.)
  - wiki/canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev.md (Добавлены cross-links на 2-й ingest канала (фитнес-клуб Ильи): тот же anti-perfectionism практикуется собеседником (стыдный туалет, БУ оборудование, ремонт на 70%, ladder pricing 5500→17900). +sources entry.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/yt__DbHZm_Ooqo.md + 3 children в audio/ (+ 7 sidecars: 3 .note.md, 1 .triage.json, 1 .bundle.json, .audio.mp3, .transcript.md)

## [2026-05-06 12:00] [ingest] | YouTube Маргулан Сейсембай — видео #3: 7 источников силы в переговорах (canon framework + 4 narrative hooks #9–12 + new success-story-as-illustration pattern)
- source: wiki/sources/2026-05-05-yt-margulan-negotiation-power-sources.md
- created:
  - wiki/canon/marketing-frameworks/seissembai-seven-power-sources-negotiation.md
- updated:
  - wiki/evolving/content-trends/seissembai-people-filter-narrative-hooks.md (Расширено до видео #3: добавлены хуки 9–12 (uncomfortable axiom, 7 источников numbered structure, 5-долларовый туалет visceral metaphor, success-story-as-illustration $425M), новый narrative-pattern «success-story-as-illustration» отдельно от vulnerability self-disclosure, anti-tactics counter-positioning structural pattern, evolution table narrative-canon Сейсембая, обновлены sources/title/tags.)
  - wiki/canon/marketing-frameworks/seissembai-six-toxic-types-filter.md (Cross-link на новые соседние фреймовки автора (видео #2 и #3) в Связанных страницах.)
  - wiki/canon/marketing-frameworks/seissembai-algorithm-ratchet-vicious-circle.md (Cross-link на 7-power-sources фреймовку (видео #3) в секции «Связи с другими фреймворками» и в «Связанные страницы».)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/yt_miPYNfojRCM.md (+ 3 sidecars: .note.md, .triage.json, .bundle.json) + 3 children in raw/processed/audio/ (yt_miPYNfojRCM.m4a + .audio.mp3 + .transcript.md + .note.md)

## [2026-05-06 12:00] [ingest] | YouTube «Бизнес с нуля» (Муратаев) — prequel-эпизод про электробайки (chronologically первый, decision-pitch/procurement/Авито-density geo-arbitrage/первая встреча с Ахматом)
- source: wiki/sources/2026-05-06-yt-biznes-s-nulya-electrobike-prequel-decision-procurement.md
- created:none
- updated:
  - wiki/evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026.md (Day-0 procurement breakdown: 4 043 372 ₽ basket по 2 поставщикам, доставка 82 350 ₽; per-model pricing (U5 74K, H10 85K, U2 85K, Венбокс 45–75K); supplier landscape (Анатолий/Венбокс/Майколин/Куга-deal-breaker); mystery-shopping конкурента (15 800 ₽/мес vs 24 000 founder-a +52% premium); Авито-density geo-arbitrage (Кудрово 28 / Мурино 32 / Парнас 2))
  - wiki/evolving/content-trends/biznes-s-nulya-founder-diy-format-2026.md (Decision-pitch sub-format как 0-й структурный элемент перед распаковкой; mystery-shopping competitor by phone как новый pattern competitive intelligence в кадре; pre-launch demand validation by Avito test-listing without inventory; обновлённый чек-лист 10 элементов)
  - wiki/canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev.md (Pre-launch confirmation anti-perfectionism принципа: 1,5 ч до decision (vs 'обдумаю дома'), 1,5 нед от помещения до собранного парка, mystery-shopping в кадре вместо premium market-research, Авито-объявление без байков как pretend-MVP demand validation, equity 33/33/33 на handshake, trademark как boundary anti-perfectionism)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 1, evolving: 1, canon: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/yt_-lqcbszD_oQ.md + 3 children (audio/m4a + audio/mp3 + transcript) with sidecars (.note.md, .triage.json, .bundle.json, .transcript.md)

## [2026-05-06 12:00] [ingest] | YouTube Илья Соловей #4/5 — Андреев / Мамба-Баду-Бамбл (consumer-internet серийный founder, pre-freemium freemium, mentality-driven локализация)
- source: wiki/sources/2026-05-05-yt-ilya-solovey-andreev-mamba-badoo-bumble.md
- created:
  - wiki/canon-strict/historical-campaigns/andreev-mamba-badoo-bumble-empire-1999-2019.md
  - wiki/canon/marketing-frameworks/free-tier-pay-for-visibility-monetization.md
  - wiki/canon/marketing-frameworks/mentality-driven-localization-andreev.md
- updated:
  - wiki/evolving/content-trends/business-history-documentary-format-ru.md (4-я точка наблюдения формата Соловья (первый consumer-internet кейс). Pattern подтверждён на consumer-subject (был открытый caveat). Длина 19:29 — возврат к baseline 19-20 min, что confirms что Porsche 28:00 был subject-driven outlier. NEW мета-наблюдения: pre-roll sponsorship — selective option (1/4); subject scope расширен на consumer-internet; RU-founder-international archetype как новый subject sub-category; provocative-quote-as-opening как новый hook-формат. Confidence остаётся high (теперь 4 точки).)
  - wiki/canon-strict/historical-campaigns/samwer-rocket-internet-fast-follower.md (Cross-link на Андреевский кейс как counter-pattern: Самверы scale через replication, Андреев scale через original business-model + deep-mentality локализация. Pair-сравнение полезно для founder-стратегий.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 2, canon: 2, evolving: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/yt_hnCOvaJohnk.md + 7 children/sidecars (yt_hnCOvaJohnk.md.{bundle.json,note.md,triage.json}, yt_hnCOvaJohnk.m4a, yt_hnCOvaJohnk.m4a.{audio.mp3,note.md,transcript.md})

## [2026-05-06 12:00] [ingest] | YT-интервью Спиридонов × Tholai (CEO Metro Россия): 7 кризисов / 3 правила выживания 2026 — primary substantiation 5-го голоса в Q1-кризисе кластере + Apollo-13 live-кейс
- source: wiki/sources/2026-05-05-yt-spiridonov-tholai-metro-7-crises.md
- created:none
- updated:
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (Tholai/Metro 5-й голос upgrade с secondary (TG-teaser) на primary (50-минутное YT-интервью): прямые цитаты forecast волны 2026 + 7 quantitative Q1-datapoints (алкоголь 2 года, средний чек 1,5 года, trade-down коньяк, HoReCa foodcost, молочка −40% YoY, 9 категорий в дефляции, Metro +5%/мес рост). Confidence на голосе с medium до high, на самой рамке остаётся high.)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Новый раздел Tholai-3-rules (фокус, SKU rolling cut 50K→10-15K артикулов, тяжёлые кадровые решения) — 3-й тип authority в survival-кластере (consultant + founder-coach + B2B-supplier-counterparty с 23-летним cross-cycle опытом). Outside-perspective playbook + 4 ready hooks с Tholai-attribution.)
  - wiki/canon/marketing-frameworks/business-crisis-playbook-apollo13.md (Новый раздел Live-illustrative case Metro Russia: операционная иллюстрация шагов 4 (поиск скрытых ресурсов через категорийную пересборку алкоголь→soft drinks) и 5 (выход более сильным — рост +5%/мес на падающем рынке). Tholai как multi-cycle authority (23 года, 7 кризисов). Caveat: Metro-масштаб не replicable для SMB-founder, фрейм важнее tactics.)
  - wiki/sources/2026-05-05-tg-mspiridonov-apr-may-2026.md (Cross-link substantiation: TG-teaser (post 4300, 18 апр) для Tholai теперь имеет primary YT-интервью substantiation; добавлены новые quantitative datapoints, которые стали доступны из видео.)
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1, evolving: 1, canon: 2}
- touched: 5 pages
- raw: raw/processed/articles/yt_NZIdd-4v96o.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + raw/processed/audio/yt_NZIdd-4v96o.m4a (+ 3 sidecars: .audio.mp3, .note.md, .transcript.md) — 8 files total

## [2026-05-06 12:00] [ingest] | YT Токовинин 3/5 (NO NEED TO THINK AI, 29:23) — 7 founder frames: AI-1997-analogy, cognitive-atrophy historical anchor, employment-default counter-FOMO, capital lifecycle formula, imitation>innovation, monoproduct-vs-assortment, low-margin quality driver, separate-line VAT tactic
- source: wiki/sources/2026-05-06-yt-tokovinin-no-need-to-think-ai.md
- created:
  - wiki/canon/marketing-frameworks/internet-1997-ai-revolution-analogy-tokovinin.md
  - wiki/canon/marketing-frameworks/employment-vs-business-default-choice-tokovinin.md
  - wiki/canon/marketing-frameworks/capital-as-product-formula-tokovinin.md
  - wiki/canon/marketing-frameworks/imitation-over-innovation-tokovinin.md
  - wiki/canon/marketing-frameworks/monoproduct-vs-assortment-market-capacity-tokovinin.md
  - wiki/canon/marketing-frameworks/separate-line-tax-pass-through-pricing-tokovinin.md
  - wiki/canon/marketing-frameworks/low-margin-customer-quality-driver-tokovinin.md
- updated:
  - wiki/evolving/industry-trends/ai-cognitive-atrophy-identity-2026.md (Tokovinin как 2-й голос (после Аннакова) с historical-precedent anchor: calculator → счёт в уме, spell-check → grammar skill, Google → fact recall; AI = четвёртый round; +cross-link на Tokovinin canon-frames)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+Tokovinin-frames section: 4 fundamental founder-frames (capital formula lifecycle, employment default, monoproduct timing, low-margin quality) с marketing-implication для GRO + 8 cross-links на новые canon-страницы; 9-frame founder operational stack от amoCRM-voice)
  - wiki/canon/marketing-frameworks/sales-as-business-core-tokovinin.md (+8 cross-links на Tokovinin 3/5 frames + source-page)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 8, evolving: 1, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/yt_Lw8qAeSxtLI.md + 3 sidecars (.bundle.json, .note.md, .triage.json) + 4 audio children (.m4a, .audio.mp3, .note.md, .transcript.md) → processed

## [2026-05-06 12:00] [ingest] | YT Максим Батырев — выпуск 5 новостей менеджмента (16–31 марта 2026): пересборка труда, 4 корзины ролей, ошибка асимметричных сигналов (Meta), AI-must РФ 16,5k+ вакансий + возрастной разворот 50+, Gallup 2026 latest, ADP n=39k, Atlanta Fed n=750
- source: wiki/sources/2026-05-05-yt-batyrev-management-news-mar16-31.md
- created:
  - wiki/canon/marketing-frameworks/four-baskets-of-roles-batyrev.md
  - wiki/canon/marketing-frameworks/work-recomposition-batyrev.md
  - wiki/canon/marketing-frameworks/meta-error-batyrev-asymmetric-signals.md
  - wiki/canon/target-audience/senior-employees-50plus-ru-2026.md
- updated:
  - wiki/canon/marketing-frameworks/internal-change-communication-protocol.md (+Batyrev 5-вопрос-тест перед сложными HR-решениями + порядок коммуникации (топы→middle→команды→только потом наверх) + татуировка одной фразой; cross-link на meta-error patterns)
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md (+Третий голос Batyrev/SuperJob на разворот: −20% вакансий, +33% резюме, 2,2% безработица, 30/28/25 дней закрытие, 2% планируют сокращения; «формула новой взрослости» 5 шагов; тест 4 вопросов; возрастной разворот как parallel-сигнал)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (+Dell -10%/-11k март 2026 (Reuters); ASML -3000 mid-management + протест 1000+ Вильтховен 24.03.2026; Meta 25.03.2026 супер-бонус как кейс асимметричных сигналов; Atlanta Fed n=750 «парадокс производительности AI»)
  - wiki/evolving-strict/market-data/employee-engagement-quiet-quitting-2026.md (+Gallup 2026 ежегодное обновление: 49%/46% (впервые struggling > thriving), engagement 31% (worst за десятилетия), 28% видят рынок хорошим vs ~70% mid-2022; ADP n=39k 22%/19%/6× safety multiplier, 53% vs 12% engagement при инвестициях в обучение; парадокс ежедневных AI-пользователей (×4 чаще говорят «менее продуктивен»); supersession Gallup 21-23% → 31% latest)
  - wiki/evolving-strict/market-data/ru-labor-market-stagnation-q1-2026.md (+SuperJob triangulation (через Batyrev): −20% вакансий, +33% резюме, 2,2% безработица, 30/28/25 дней, 2% планируют сокращения; качественная интерпретация «бизнес пересобирает себя» как драйвер cross-link к canon-рамке Batyrev)
  - wiki/evolving/industry-trends/ai-knowledge-worker-climb-2025-2026.md (+Сигнал 9: AI-must в RU вакансиях Q1 2026 — 16,5k+ открытых позиций (HH+PRDev), отклики ×2,7 г/г, чаще всего у клиентских менеджеров/маркетологов/аналитиков/копирайтеров/программистов; Batyrev «AI = новый Excel» — RU-side замыкание тренда)
  - wiki/evolving/industry-trends/ai-for-managers-2025-2026.md (+5-я data-точка: Batyrev как RU-side голос на AI-pressure для руководителей; «AI = базовая рабочая грамотность как Excel и почта»; 16,5k+ AI-must вакансий РФ Q1 2026)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+Operational-инструмент Batyrev «4 вопроса перед открытием вакансии» как ответ на стагнацию найма Q1 2026; cross-link на пересборку труда и 4 корзины ролей; self-application для founderа на собственную роль)
- superseded: 
  - wiki/evolving-strict/market-data/employee-engagement-quiet-quitting-2026.md (Gallup engagement 21-23% → 31% latest, audit trail сохранён в HTML-комментарии в таблице)
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 3, evolving-strict: 2, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/yt_4yhJk40wIpo.md + 7 sidecars/children (.bundle.json, .note.md, .triage.json, audio/.m4a, audio/.m4a.audio.mp3, audio/.m4a.note.md, audio/.m4a.transcript.md)

## [2026-05-06 12:30] [ingest] | YT «НЕскучные ФИнансы» — разбор салона красоты за 3,7 млн на Авито (2-й выпуск формата): расширение avito-business-autopsy + ready-business-purchase-narrative-hooks (франшиза, brokerage, build-vs-buy)
- source: wiki/sources/2026-05-05-yt-neskuchnye-finansy-salon-krasoty-avito-razbor.md
- created:none
- updated:
  - wiki/evolving/content-trends/avito-business-autopsy-yt-format-2026.md (2-й источник подтверждает повторяемость жанра (тот же ведущий Цветков); новый раздел «Brokerage representation» как нюанс к звонку-эмоциональному ядру; новый раздел «Франшиза-burden» как отдельный red-flag-кластер; расширенный verdict-rule с двумя вариациями (жёсткой и мягкой); новый «Build-vs-buy frame» (replacement cost) как опциональный элемент; расширенный red-flag банк до 12 пунктов (было 6) с указанием источника по каждому)
  - wiki/evolving/content-trends/ready-business-purchase-narrative-hooks.md (Новая категория 7 «Franchise-burden разбор» (5 hook-формулировок + матрица трёх вопросов); расширение категории 4 (reverse-angle) под-кластером «Brokerage representation» с 5 hook-формулировками для матрицы 2×2 продавцов)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/yt_-XTH-HU5J5U.md (+ 4 sidecars: .bundle.json, .note.md, .triage.json) + raw/processed/audio/yt_-XTH-HU5J5U.m4a (+ 3 sidecars: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 12:30] [ingest] | YT «Бизнес с нуля» (Муратаев) — запуск проката электробайков для курьеров: founder-DIY реалити как третий тип бизнес-реалити + anti-perfectionism MVP-launch idology + hands-on-builder подвариант ICP
- source: wiki/sources/2026-05-05-yt-biznes-s-nulya-electrobike-rental-couriers.md
- created:
  - wiki/canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev.md
  - wiki/evolving/content-trends/biznes-s-nulya-founder-diy-format-2026.md
  - wiki/sources/2026-05-05-yt-biznes-s-nulya-electrobike-rental-couriers.md
- updated:
  - wiki/canon/marketing-frameworks/business-reality-show-format.md (Добавлена расширенная типология бизнес-реалити (3 типа реалити + autopsy: cohort coaching / accountability / founder-DIY / single-listing autopsy) с anchor-кейсами и matrix по subject/time-window/coach role)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Добавлен третий архетип сегмента — hands-on-builder founder (фаза активного запуска, рядом с crisis-стороной и exit-стороной): маркеры, контраст-таблица с crisis-archetype, ICP-импликация для GRO, diagnostic-маркер для лидов)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/yt_0ITFGsvCy1I.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + raw/processed/audio/yt_0ITFGsvCy1I.m4a (+ 3 sidecars: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 12:30] [ingest] | YouTube Margulan Seissembai видео #4 «Solitude as tool» (SW-65s1zP9Q, финал scheduled-серии): новый canon solitude-7-benefits-4-controllers + хуки 13–16 в narrative-page + cross-links 3 предыдущих canon + 4-й компонент founder full-stack в ru-smb-founder
- source: wiki/sources/2026-05-05-yt-margulan-solitude-tool.md
- created:
  - wiki/canon/marketing-frameworks/seissembai-solitude-7-benefits-4-controllers.md
- updated:
  - wiki/evolving/content-trends/seissembai-people-filter-narrative-hooks.md (Title shift с #1-#3 из 4 на #1-#4 финальная подборка; добавлены хуки 13-16 (counter-positioning инструмент-vs-социальная-норма, диагностика 'Я занят = страх', consume-without-integration видеорегистратор-метафора, tapas culturally-distant authority); evolution-таблица расширена до 4 видео, author-signature summary финализирован; corpus closed.)
  - wiki/canon/marketing-frameworks/seissembai-algorithm-ratchet-vicious-circle.md (Cross-link на новую solitude-фреймовку как operational extension forward-pointer-а из видео #2 ('чтобы понять какая цель ваша — побыть в одиночестве'); добавлен в sources frontmatter; full corpus 4 видео отмечен в соседних фреймовках.)
  - wiki/canon/marketing-frameworks/seissembai-six-toxic-types-filter.md (Cross-link на solitude-фреймовку (видео #4); функция 1 «возврат к естественности» — operational механизм для самокритики, без которого фильтр окружения не выполним; full corpus 4 видео; добавлен в sources.)
  - wiki/canon/marketing-frameworks/seissembai-seven-power-sources-negotiation.md (Cross-link на solitude-фреймовку (видео #4); функции 3 и 4 — analytical reflection и intent-vs-action audit — pre-condition для применения 7 power-sources в реальных переговорах; full corpus 4 видео; добавлен в sources.)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Новый раздел про solitude-фреймовку как 4-й компонент founder full-stack самоменеджмента; counter-positioning к I-am-busy identity, intra-day встраивание как match с GRO product-промисом, counter-anchor к high-content-consumption норме; updated cross-links bottom добавлены video #3 + video #4 + corpus закрыт; updated comment отражает 4 видео corpus.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/yt_SW-65s1zP9Q.md (+ 3 sidecars: bundle.json, note.md, triage.json) + raw/processed/audio/yt_SW-65s1zP9Q.m4a (+ 3 sidecars: audio.mp3, note.md, transcript.md)

## [2026-05-06 12:30] [ingest] | YouTube — М. Спиридонов #5/5 final: Сет Годин «The Dip» (яма vs тупик, 9:57): canonical persistence-framework + закрытие 5-серийного cluster Спиридонова + cluster-CTA meta-формат
- source: wiki/sources/2026-05-06-yt-spiridonov-godin-dip-framework.md
- created:
  - wiki/canon/marketing-frameworks/godin-dip-vs-deadend-spiridonov.md
- updated:
  - wiki/canon/marketing-frameworks/signal-noise-essentialism-spiridonov.md (+companion-piece про яму vs тупик (#5/5 final): новая секция со сравнительной таблицей productivity vs persistence dimension; explicit cluster-CTA внутри-серийной связи #5→#1; cross-link на godin-dip-vs-deadend-spiridonov)
  - wiki/canon/marketing-frameworks/housel-psychology-of-money-spiridonov.md (+cross-link на godin-dip фрейм #5/5 final в таблице связей и в Связанных страницах; общий closing-тезис «дисциплина / характер бьёт интеллект» (#4) ↔ «честность с собой бьёт упрямство» (#5))
  - wiki/canon/marketing-frameworks/spiridonov-three-engagement-formats.md (новая секция «Серия Спиридонова #1–#5 — content-tier ниже tiered-форматов» с таблицей всех 5 видео cluster и cluster-CTA pattern; cross-link на godin-dip-vs-deadend-spiridonov)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (новая секция «Persistence-dimension: Спиридонов #5/5 final» — 3 диагностических вопроса как self-test для founder-owner-seller в Q1 2026 cooling cycle; pre-commit kill-criteria по Дику Коллинзу как antipanic-protocol; завершает трёх-осный фреймворк Спиридонова для сегмента (productivity / money / persistence))
  - wiki/evolving/content-trends/yt-multitrack-audio-meta-format-spiridonov.md (новая секция «explicit cluster-CTA через end-screen» как второй meta-формат от Спиридонова + сравнение Klingon-track vs Cluster-CTA + объединённый pattern (видео #2 использует оба) как gold standard signature-видео)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/yt_tRcTN1lsw9E.md + 3 sidecars (.bundle.json, .note.md, .triage.json) + 4 children in raw/processed/audio/ (yt_tRcTN1lsw9E.m4a, .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 13:30] [ingest] | YouTube @IgorRybakov 3-й выпуск (~март 2026, ~30 мин) — дело Гасанова, респектабельный инфобиз фреймворк, FSB-cutoff закон, USD -10% YTD, онлайн-казино легализация
- source: wiki/sources/2026-05-06-yt-rybakov-trump-putin-dollar.md
- created:
  - wiki/canon/marketing-frameworks/respectable-infobiz-rybakov.md
  - wiki/volatile-strict/industry-news/ru-gasanov-tax-case-2026.md
  - wiki/volatile-strict/industry-news/ru-fsb-comms-cutoff-law-2026.md
  - wiki/volatile-strict/industry-news/ru-online-casino-legalization-2026.md
  - wiki/evolving-strict/market-data/usd-decline-tactical-vs-strategic-2026.md
- updated:
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md (+2 хука: #21 «чем хуже — тем лучше» combinatorial-расширение к #16 (паника = люкс) и #10 (планово-ситуационный режим); #22 эпатаж как fea-then-bug в эпоху регуляторных атак (применение хука #17 «право в контексте» к content creators))
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (+2 вектора: 12-й (FSB-cutoff закон Госдумы); 13-й (атаки на блогеров-инфобизнесменов: Гасанов, Аяз Шабудин). Расширено заголовок section с «11 параллельных» до «13 параллельных давлений»)
  - wiki/canon/positioning/gro-value-proposition.md (Новая section «Внешние резонансы: Респектабельный инфобиз Рыбакова + регуляторный squeeze (2026-05-06)» — связка фреймворка respectable-infobiz с counter-positioning GRO; дополнен sources frontmatter)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, evolving-strict: 1, volatile-strict: 3, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/yt_q2eyXzUJ4ec.md + 3 children (audio: m4a + audio.mp3 + transcript.md) with sidecars (.note.md, .triage.json, .bundle.json, m4a.note.md)

## [2026-05-06 14:50] [ingest] | YT @mihail-tokovinin #4/5 «Family, Money, and the Law» — long-form-cancellation-defense + AMOCON cross-video systematic embedding + Tokovinin peer-critic Грэбнюку
- source: wiki/sources/2026-05-06-yt-tokovinin-family-money-law.md
- created:
  - wiki/canon/marketing-frameworks/long-form-cancellation-defense-tokovinin.md
- updated:
  - wiki/volatile-strict/competitor-news/amocon-2026-promo-april.md (Cross-video systematic embedding observation: ad-блок повторяется в видео 4/5 (Lw-hmtrszCs) с адаптированной bridge-фразой («большие формы» vs «правильная комната»), но stable core message + промокод. Pattern переходит из «разовое включение» в «systematic continuous distribution».)
  - wiki/evolving/competitor-positioning/grebenyuk-anomaly-community.md (Peer-level critic section: Tokovinin прямой counter-frame на «жена-как-бизнес-партнёр» Гребенюка — generalization-from-self anti-pattern. «Не надо по себе судить о людях.» Marketing-implication для GRO own narrative discipline.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, volatile-strict: 1, evolving: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/yt_Lw-hmtrszCs.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + raw/processed/audio/yt_Lw-hmtrszCs.m4a (+ 3 sidecars: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 17:30] [ingest] | YouTube (Oskar Hartmann × Эмин Агаларов 2026-05-05) — 5 mental-frameworks серийных предпринимателей + Tahnoun AI-cascade enforcement-layer (40-мин интервью, density ~1 frame/5 мин)
- source: wiki/sources/2026-05-06-yt-uVD3QAoiLF0-hartmann-agalarov.md
- created:
  - wiki/canon/marketing-frameworks/hartmann-instant-reply-principle.md
  - wiki/canon/marketing-frameworks/hartmann-ai-mandate-cascade.md
  - wiki/canon/marketing-frameworks/hartmann-control-only-investment.md
  - wiki/canon/marketing-frameworks/hartmann-children-success-mandate.md
  - wiki/canon/marketing-frameworks/agalarov-tangibility-investment-test.md
  - wiki/evolving/content-trends/oskar-hartmann-channel-pattern.md
- updated:
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (Новый раздел «Hartmann × Tahnoun cascade как enforcement-layer» в Personal CEO commitment to AI: каскад UAE-state → Tahnoun (.3T) → Hartmann → руководители отделов с deadline-ультиматумом до конца года)
  - wiki/evolving/content-trends/enough-vs-growth-narrative.md (Counter-anchor «Агаларов: остановиться = смерть» как identity-driven mode; bimodal segmentation для founder-content (lifestyle vs identity-driven))
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (5 cross-links на новые Hartmann/Agalarov-страницы как top-tier ICP-aligned content channel и mental-frameworks)
  - wiki/canon/marketing-frameworks/return-on-time-moreynis.md (Counter-anchors из Hartmann × Агаларов: Hartmann-mode (instant-reply остаётся в петле) и Agalarov-mode (identity-driven scale, не ROT) как complementary modes; bimodal segmentation для ROT-content GRO)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving: 4, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/yt_uVD3QAoiLF0.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + raw/processed/audio/yt_uVD3QAoiLF0.m4a (+ 3 sidecars: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 17:30] [ingest] | YouTube @IgorRybakov 4-й выпуск (РЖД, Эпштейн, Индия-нефть, Маск 800 млрд) — +хуки #23 (самофокус→community), #24 (cancel-resonance); fiscal-stress блок (РЖД 4 трлн + Индия −3,5× нефть); Tesla/SpaceX/xAI manipulative re-valuation
- source: wiki/sources/2026-05-06-yt-rybakov-rzd-epstein-india-oil.md
- created:none
- updated:
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md (+2 хука: #23 «Самофокус → депрессия → выход через благодарность и сети людей» (operational mechanism для community-positioning, complement к хуку #20); #24 «Резонанс СМИ как weaponized cancel-tool — когда волна поднялась, она необратима» (defensive playbook + counter-positioning, расширение хука #22))
  - wiki/evolving-strict/market-data/ru-vvp-investment-cooling-2026.md (+Февральская fiscal-stress блок: РЖД 4 трлн ₽ долг + продажа башни Москоутаурус 220 млрд ₽; Индия −3,5× импорт нефти, переключение на venesuelan oil под контролем США; ФНБ-исчерпание (Минфин недобор 3-3,5 трлн); продолжение «сжимающейся спирали» автора с federal-tier proof points; +source)
  - wiki/evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2.md (+Tesla/SpaceX/xAI блок: Маск 800 млрд $ через манипулятивные A→A покупки (SpaceX купил xAI, capitalisation airdrop); прогноз 1 трлн $; +«дутыш капитализаций как механизм абсорбции эмиссионных денег» double-frame thesis (bubble-skepticism + real-infrastructure); +«manipulative re-valuation» как 3-я структурная категория валюация-механики после primary fundraising и secondary premium; +source)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, evolving-strict: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/yt_TksnX6IMmlQ.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + 4 children в raw/processed/audio/ (m4a + .audio.mp3 + .note.md + .transcript.md)

## [2026-05-06 17:30] [ingest] | YouTube Спиридонов #1/5 — сигнал/шум, эссенциализм, 3-фазовый протокол; 5 canon-фреймворков созданы + 3 страницы обогащены
- source: wiki/sources/2026-05-05-yt-spiridonov-signal-noise-essentialism.md
- created:
  - wiki/canon/marketing-frameworks/signal-noise-essentialism-spiridonov.md
  - wiki/canon/marketing-frameworks/valuable-to-stranger-filter.md
  - wiki/canon/marketing-frameworks/evening-audit-morning-bunker-protocol.md
  - wiki/canon/marketing-frameworks/jobs-2x2-product-line-radical-cut.md
  - wiki/canon/marketing-frameworks/mrbeast-data-beats-ego-retention-graphs.md
- updated:
  - wiki/canon/marketing-frameworks/pareto-80-20-marketing.md (Добавлен раздел про operational переупаковку Парето в лексику «сигнал vs шум» от Спиридонова + cross-links на 4 дочерние страницы; источники +1; updated 2026-05-06.)
  - wiki/canon/marketing-frameworks/visotsky-productivity-heuristics.md (Добавлен раздел про параллельный playbook Спиридонова (концептуальный vs числовой); cross-links; источники +1; updated 2026-05-06.)
  - wiki/canon/target-audience/gro-segments.md (Добавлен раздел «Productivity vocabulary для всех трёх сегментов» с маппированием signal/noise hooks Спиридонова на каждый сегмент GRO + cross-links на 4 дочерние страницы; источники +1; updated 2026-05-06.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 8, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/yt_0srV7ceoAX0.md + 3 children (audio + audio_normalized + transcript) with sidecars (.note.md, .bundle.json, .triage.json)

## [2026-05-06 17:30] [ingest] | YouTube Спиридонов #4/5 — Psychology of Money (Хаузел recap, 8:39): operational рамка «доход − эго» + 3-шаговый алгоритм; money-companion к signal/noise; 9-й голос psychological dimension в Q1 2026 cooling
- source: wiki/sources/2026-05-06-yt-spiridonov-housel-psychology-of-money.md
- created:
  - wiki/canon/marketing-frameworks/housel-psychology-of-money-spiridonov.md
- updated:
  - wiki/canon/marketing-frameworks/signal-noise-essentialism-spiridonov.md (+companion section про money-psychology (двухосный фрейм Спиридонова: signal/noise productivity ось + money-psychology ось); cross-link на новую страницу housel-psychology-of-money-spiridonov; +source в front-matter)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+enrich-секция «Personal-finance dimension: Спиридонов #4 «доход − эго»» — закрывает gap про personal financial discipline founder-owner-seller сегмента; mirroring 3 правил Толай на personal-уровень founder в Q1 2026)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (+addendum «9-й голос: Спиридонов #4 — psychological dimension cooling cycle» — internal psychological mechanism Q1 2026, complement к 8 предыдущим external voices; объясняет почему founder-owner-seller тратит личные сбережения на ФОТ)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/yt_sKHI5JQnsxA.md (+ 3 sidecars: .note.md, .triage.json, .bundle.json) + 4 children (raw/processed/audio/yt_sKHI5JQnsxA.m4a + .audio.mp3 + .note.md + .transcript.md)

## [2026-05-06 17:30] [ingest] | YT Михаил Токовинин 2/5 (amoCRM) — реакции на 4 ролика: Кийосаки-долг / WB-селлеры / NVIDIA-equity / subscription-pitch (Ford doctor-patient + Bakalchuk «ваши проблемы»)
- source: wiki/sources/2026-05-05-yt-tokovinin-billion-debts-sellers-startups.md
- created:
  - wiki/canon/marketing-frameworks/subscription-consumption-model-shift-tokovinin.md
  - wiki/canon/marketing-frameworks/sales-as-business-core-tokovinin.md
- updated:
  - wiki/evolving/industry-trends/freelance-platform-dependency.md (Tokovinin (amoCRM) 4-й голос: 5 тезисов — customers belong to platform / low-margin tail only / constant influx by design / sales-motion ownership distinguisher / Bakalchuk «ваши проблемы» management style)
  - wiki/canon/marketing-frameworks/hartmann-control-only-investment.md (Tokovinin cross-validation: layer 1 — согласие «3% от большой > 100% от маленькой»; layer 2 — counter-frame employee-equity tension (transfer of risk сотрудник не подписывал))
  - wiki/canon/marketing-frameworks/refused-customer-interview.md (Ford «faster horse» / doctor-patient framing (Токовинин) как complementary doctrine: refused-customer interview — частный случай doctor-patient на point of failure; обобщение до comprehensive product-discovery doctrine + Ford-тест для interview script quality)
  - wiki/canon/target-audience/gro-segments.md (+ 2 cross-link на новые Tokovinin-фреймы: sales-as-business-core (founder vs supplier), subscription-consumption-model-shift (doctor-patient CustDev для всех 3 сегментов))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/yt_GYyi48pziuI.md + 3 children (audio m4a + audio.mp3 + transcript.md) with sidecars (.note.md, .triage.json, .bundle.json)

## [2026-05-06 17:30] [ingest] | YT @Максим Батырев — «Life without waiting for vacation» (1m14s шорт, музыка без речи; audit-only, no relevant extractions; Батырёв #3/3 финал)
- source: wiki/sources/2026-05-05-yt-batyrev-life-without-waiting-vacation.md
- created:none
- updated:none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/yt_MRFVSCbZ_pU.md + 3 children (audio/yt_MRFVSCbZ_pU.m4a, .audio.mp3, .transcript.md) with sidecars (.note.md, .triage.json, .bundle.json)

## [2026-05-06 17:30] [ingest] | YT «Предприниматель ДЕла» #1/4 — СВ Мебель factory-tour + 10-й слёт героев в Сочи: 5 новых canon/evolving фреймов + 4-й архетип SMB-founder-сегмента
- source: wiki/sources/2026-05-05-yt-predprinimatel-dela-sv-mebel-factory-tour.md
- created:
  - wiki/sources/2026-05-05-yt-predprinimatel-dela-sv-mebel-factory-tour.md
  - wiki/evolving/content-trends/factory-tour-pro-day-event-format.md
  - wiki/canon/marketing-frameworks/cost-leader-premium-quality-positioning.md
  - wiki/evolving/industry-trends/ru-manufacturing-china-pivot-2022-2026.md
  - wiki/evolving/content-trends/factory-discipline-narrative-hook.md
  - wiki/evolving/competitor-positioning/predprinimatel-dela-channel-pattern.md
- updated:
  - wiki/canon/marketing-frameworks/focus-strategy-porter.md (+2-й RU-exemplar (СВ Мебель): differentiation focus в гиперэконом-сегменте через cost-leader-with-premium-quality formula; complementary action-source vs hr-portal textbook reformulation)
  - wiki/evolving/industry-trends/ru-retail-robotization-labor-deficit-2025-2026.md (+Manufacturing-parallel: SV-Mebel 5 KUKA роботов / 1=6 грузчиков / KUKA сохранён при China-pivot прочего парка; pioneer 2019 (Remix Packing 5 линий = 150 оптимизированных) — proof-point роботизации в production-секторе РФ; structural retail↔manufacturing аналогия)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+Четвёртый архетип сегмента: factory-owner-event-organizer (Стеклянников/СВ Мебель 30 лет) + zerkalny event-organizer-without-own-production (Дмитриев); ICP-импликация B2B-партнёрство и content-source rather than direct subscription target; #1/4 confidence low)
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1, canon: 3, evolving: 5}
- touched: 9 pages
- raw: raw/processed/articles/yt_GUMv4IJHsgA.md (+ .bundle.json, .note.md, .triage.json) + 4 children: raw/processed/audio/yt_GUMv4IJHsgA.m4a (+ .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 18:25] [ingest] | YouTube Маргулан Сейсембай #2/4 — vicious circle (D8C6nTN8yrg, 9:12): algorithm-ratchet canon framework + 4 narrative-хука + founder-сегмент operational stack
- source: wiki/sources/2026-05-05-yt-margulan-vicious-circle.md
- created:
  - wiki/canon/marketing-frameworks/seissembai-algorithm-ratchet-vicious-circle.md
- updated:
  - wiki/evolving/content-trends/seissembai-people-filter-narrative-hooks.md (+4 narrative-хука (5–8) из видео #2: метафора храповика/трещотки, метафора гусеницы-пожирающей-ошибки, диагностика "если цель не драйвит — она не ваша", FOMO как social-media-induced ложное ощущение; +confirmation founder-vulnerability стилистики; title generalized с people-filter на серию #1–#2)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+section "Operational stack самоменеджмента" с тремя applicability-блоками (algorithm-ratchet, daily reflection ritual с diagnostic-сигналом goal misalignment, FOMO counter-positioning); +marketing-применимость; +cross-link на новую canon-фреймовку)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/yt_D8C6nTN8yrg.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + 4 children в raw/processed/audio/ (.m4a, .m4a.audio.mp3, .m4a.note.md, .m4a.transcript.md)

## [2026-05-06 18:30] [ingest] | YT @IgorRybakov — обзор экономических новостей ~2026-01-15: «сжимающая спираль» mechanism + ВВП-прогноз 0,8% + кейс газовозов Технониколь + Ростик-с/Домодедово
- source: wiki/sources/2026-05-06-yt-rybakov-vvp-trump-oil.md
- created:
  - wiki/canon/marketing-frameworks/private-vs-state-innovation-rybakov.md
  - wiki/evolving-strict/market-data/ru-vvp-investment-cooling-2026.md
  - wiki/volatile-strict/industry-news/ru-rostix-bankruptcy-jan-2026.md
  - wiki/volatile-strict/industry-news/ru-domodedovo-airport-auction-jan-2026.md
- updated:
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md (+2 хука (#17 «право в контексте», #18 «управленческая среда определяет результат») из YouTube-выпуска ~2026-01-15; tags +video,+youtube; 3-я source-страница в коллекции)
  - wiki/evolving/industry-trends/ru-smb-sales-q1-2026.md (+8-й независимый голос в Q1 2026 cooling кластере: Рыбаков YouTube «сжимающая спираль» как первая mechanism-модель + 4 sub-сигнала (ВВП 0,8%, инвест-минимум, Ростик-с datapoint, counter-frame «чем хуже тем лучше»))
  - wiki/evolving-strict/market-data/ru-qsr-restaurant-2025-2026-q1.md (+оперативный operational-hit Q1 2026 (Ростик-с: 25 точек, 600 увольнений, 4 мес без зарплат, KFC возврат прав 11/2025) как leading indicator продолжения 2025 финансового сжатия в 2026)
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1, canon: 1, evolving-strict: 2, volatile-strict: 2, evolving: 2}
- touched: 8 pages
- raw: raw/processed/articles/yt_A6w8Zpwzghc.md + 3 children (audio/yt_A6w8Zpwzghc.m4a + .audio.mp3 + .transcript.md)

## [2026-05-06 18:30] [ingest] | YT «Предприниматель ДЕла» #3/4 — Русин (Ламинат Рус) лазерное кромление + кейс Мария-Русин 2022 (cascading sanctions shock + consumables China-pivot)
- source: wiki/sources/2026-05-05-yt-predprinimatel-dela-rusin-laser-edging.md
- created:none
- updated:
  - wiki/evolving/competitor-positioning/predprinimatel-dela-channel-pattern.md (vendor-spotlight-doc подтверждён как 3-й archetype с template-структурой (lead-in/personal backstory/operational deep-dive/live demo/Q&A/promo-tail); discriminator knowledge-vendor vs material-vendor; +#3/4 source; confidence остался low до #4/4)
  - wiki/evolving/content-trends/factory-tour-pro-day-event-format.md (speaker-template diversity (knowledge-vendor через slides+framework vs material-vendor через physical-event-marketing+giveaway); applied к разным категориям спикеров; +#3/4 source)
  - wiki/evolving/industry-trends/ru-manufacturing-china-pivot-2022-2026.md (second first-hand кейс (Русин/Ламинат Рус); cascading-shock pattern Мария-Русин 2022 (Homag laser stuck в Германии → emergency-партнёрство → multi-year scaling маленького vendor); +consumables-pivot (кромка Rehau German 140₽/м → китайская 45₽/м, 4-летний 12-vendor supplier-search); +Hook 4 в применимости к GRO; +#3/4 source)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/yt_LnPu0Ky6nt8.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + 4 children (raw/processed/audio/yt_LnPu0Ky6nt8.m4a + .audio.mp3 + .note.md + .transcript.md)

## [2026-05-06 19:00] [ingest] | TG @IgorRybakov YouTube #2 — Запреты 2026 (РКН/Telegram/ЖКХ/серый iPhone, ~февраль 2026): +2 hooks в Rybakov-collection, +SIM-реестр page, +ЖКХ-шок page, +Heineken-RU layoffs page; updated 4 cross-pages
- source: wiki/sources/2026-05-06-yt-Jk5otbO0nYA.md
- created:
  - wiki/volatile-strict/industry-news/ru-sim-card-registry-2028.md
  - wiki/volatile-strict/industry-news/ru-jkh-shock-jan-2026.md
  - wiki/volatile-strict/competitor-news/heineken-ru-layoffs-feb-2026.md
- updated:
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md (+2 хука (#19 «средства нападения быстрее защиты» — counter-intuitive risk-frame для регуляторики; #20 «счастливые ищут счастливых» — environmental sorting / community framework для GRO); +source 2026-05-06-yt-Jk5otbO0nYA; updated в свяанных страницах)
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (Новый раздел «Rybakov YouTube: 4-я волна замедления + WeChat-параллель к 2035» — 8 протоколов, 75 млн ₽ штрафов, требование физприсутствия, MAX перегрузка от регистрационного бума, акции VK +; technical deconstruction логики РКН (file-transport-layer attack); 10-летний horizon framing для national-app supply-side; observation про business-celebrity voices как часть proправительственного choir по MAX)
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (+2 вектора давления (10-й SIM-реестр к 2028 + 11-й — двойной squeeze серый импорт iPhone через Минпромторг + SIM-реестр); title обновлён «9 → 11 параллельных давлений»; cold-calling channel дорожает структурно; founder-asynchronous norms cement; tailwind для locale-привязанной экосистемы)
  - wiki/evolving-strict/market-data/ru-private-dental-clinics-2025-2026.md (+ Salary boom стоматологов (independent verification структурного сдвига сегмента): ортопеды до 750 тыс ₽/мес, медиана стоматолога 330 тыс ₽/мес +10% YoY, имплантолог Мурманск 650 тыс ₽, региональный gap «практически исчез»; analysis + asymmetric-distribution thesis (премиальная медицина защищена от Q1 cooling))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 1, volatile-strict: 3, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/yt_Jk5otbO0nYA.md + 3 children (audio: m4a + audio.mp3 + transcript.md) + sidecars (.bundle.json, .note.md, .triage.json)

## [2026-05-06 19:42] [ingest] | YouTube Илья Соловей — S7 Airlines (#1/5 серии): rebrand 2006 + распределённый M&A playbook Филёвых + 2 креативные кампании + наблюдение документального YT-формата
- source: wiki/sources/2026-05-05-yt-ilya-solovey-s7-airlines-history.md
- created:
  - wiki/canon-strict/historical-campaigns/s7-airlines-rebrand-2006.md
  - wiki/canon-strict/historical-campaigns/s7-creative-campaigns-2016-2019.md
  - wiki/canon/marketing-frameworks/distressed-asset-consolidation-playbook.md
  - wiki/evolving/content-trends/business-history-documentary-format-ru.md
- updated:
  - wiki/canon/marketing-frameworks/consulting-brand-naming-typology.md (+section «Кейс S7 Airlines rebrand 2006» как RU B2C-вариант Тип 3 (constructed via IATA-код), отличия от Accenture (B2B/global) и подтверждение универсальности Тип 3 для разных категорий бизнеса; +source link, +cross-link)
  - wiki/canon/marketing-frameworks/internal-change-communication-protocol.md (+cross-link на S7 rebrand: использование уже-существующего внутреннего идентификатора (IATA-код S7) облегчает внутреннее принятие новой brand-идентичности; +source link)
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 2, canon: 3, evolving: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/yt_3sJleUFJBZo.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + 3 children (raw/processed/audio/yt_3sJleUFJBZo.m4a + .audio.mp3 + .transcript.md + .note.md)

## [2026-05-06 19:50] [ingest] | YouTube — Бизнес с нуля Муратаев финал #5/5 велобайк-серии (OFJAPdavM3s, дата съёмки 2026-03-19): month-1 partial DDS, second mechanic Андрей, profit-share 33/33/33, conflict-курьер, client-UGC Vlad, open-call ПО
- source: wiki/sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet.md
- created:
  - wiki/canon/marketing-frameworks/profit-share-service-revenue-smb.md
  - wiki/canon/marketing-frameworks/three-partner-majority-rule-smb.md
  - wiki/evolving/content-trends/courier-as-organic-ugc-producer.md
  - wiki/evolving/content-trends/inbound-talent-via-yt-finale.md
- updated:
  - wiki/evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026.md (+month-1 partial DDS (20.02-19.03): 675 800 / 360 530 / 315 269 ₽; ZP 4000/смена piece-rate × 39 смен; trajectory month-1→month-3 (+32% NCFO); winter-warming paid-spend pattern (42 000→25 126 ₽); defect rate 4,4% (2/45) первой партии; B2C tariff Contradictions block (4 000 ₽/нед vs 6 000 ₽/нед); patent 50 000 ₽/год; inbound-call volume 50-60/day normal, 100/day peak)
  - wiki/evolving/content-trends/biznes-s-nulya-founder-diy-format-2026.md (+non-linear month-1 finale sub-format (financial baseline самый ранний в серии = финал); +conflict-anchor structure (cliffhanger 0:00 → tension middle → resolution finale, элемент 11); +inbound-talent funnel via finale appeal (элемент 12); +client-as-organic-UGC applied case (Влад в финале, sub-механика 11-strict element))
  - wiki/canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev.md (+month-1 confirmation секция (5 applied illustrations): ZP 4000/смена piece-rate vs salary; флаер-A4-ошибка-как-feature reframed (operational mistake → marketing-feature); самопришедший mechanic Андрей вместо recruiting-process; open call viewers вместо formal-hiring; 50/50 cost-share для unclear-fault инцидентов вместо forensic analysis)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/yt_OFJAPdavM3s.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + 1 audio child (raw/processed/audio/yt_OFJAPdavM3s.m4a + 3 sidecars: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 20:15] [ingest] | YT Илья Соловей #3 — Porsche/VW dynasty saga (3rd validation: format conf medium → high; 4 canon frameworks + 1 canon-strict case + 2 updates)
- source: wiki/sources/2026-05-05-yt-ilya-solovey-porsche-history.md
- created:
  - wiki/canon-strict/historical-campaigns/porsche-vw-1990s-2009-acquisition-saga.md
  - wiki/canon/marketing-frameworks/multi-generational-family-business-survival.md
  - wiki/canon/marketing-frameworks/operational-turnaround-playbook-wiedeking.md
  - wiki/canon/marketing-frameworks/davids-goliath-acquisition-anti-pattern.md
  - wiki/canon/marketing-frameworks/dual-track-monetization-luxury-car-brand.md
- updated:
  - wiki/evolving/content-trends/business-history-documentary-format-ru.md (Confidence повышен medium → high после 3-го ingest'а канала Соловья (Porsche). Первый non-RU subject — формат подтверждён trans-culturally. Добавлен 3-й столбец comparison-table; новые observations: pre-roll sponsorship Edison (NEW), pre-emptive teaser current-events (NEW), format-вариативность по subject scope (28:00 outlier для multi-decade saga).)
  - wiki/canon/marketing-frameworks/distressed-asset-consolidation-playbook.md (3-й параллельный кейс (Wiedeking / Porsche 1992-1998) добавлен как outsider professional-CEO sub-variant. Playbook теперь имеет три sub-варианта (outsider founder-CEO Филёвы / insider founder-CEO Мордашов / outsider professional-CEO Wiedeking). Trans-cultural validation (RU + DE).)
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, canon: 5, evolving: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/yt_DtTyyYr-CkQ.md + 3 children (raw/processed/audio/yt_DtTyyYr-CkQ.m4a, .audio.mp3, .transcript.md) + 4 sidecars (.bundle.json, .triage.json, 2× .note.md)

## [2026-05-06 21:00] [ingest] | YT Михаил Токовинин (amoCRM) 5/5 final — economic crisis counter-frame + 3 новых canon-фрейма (scale-flips-debt, populism-discount-rule, human-hours-economic-unit)
- source: wiki/sources/2026-05-05-yt-tokovinin-economic-crisis.md
- created:
  - wiki/canon/marketing-frameworks/scale-flips-debt-leverage-tokovinin.md
  - wiki/canon/marketing-frameworks/populism-discount-rule-tokovinin.md
  - wiki/canon/marketing-frameworks/human-hours-economic-unit-tokovinin.md
- updated:
  - wiki/canon/marketing-frameworks/long-form-cancellation-defense-tokovinin.md (n=5 cross-video pattern validation; confidence upgrade medium → high; double counter-frame Осипов+Рыбаков как escalation pattern)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Wealth-tier sub-segmentation Bloomberg threshold (00K-0M = primary GRO target middle tier; <00K = secondary не-panic content))
  - wiki/evolving-strict/market-data/usd-decline-tactical-vs-strategic-2026.md (Cluster validation: Tokovinin как 2-й RU founder voice про global-debt-zero через инфляцию; binary-frame inflation/deflation/aliens)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving-strict: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/yt_Q6MbmBM7m1s.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json) + raw/processed/audio/yt_Q6MbmBM7m1s.m4a (+ 3 sidecars: .audio.mp3, .note.md, .transcript.md)

## [2026-05-06 21:45] [ingest] | yt @mihail-tokovinin (amoCRM cofounder) #1/5 — Q&A видео 9YxLk3u__rI 24:24, 4 founder mental models + AMOCON 2026 event metric
- source: wiki/sources/2026-05-05-yt-tokovinin-ban-this-from-children.md
- created:
  - wiki/canon/marketing-frameworks/fear-vs-shyness-tokovinin.md
  - wiki/canon/marketing-frameworks/peer-environment-aspiration-tokovinin.md
  - wiki/canon/marketing-frameworks/passion-test-real-entrepreneur-tokovinin.md
  - wiki/canon/marketing-frameworks/anti-classification-people-tokovinin.md
  - wiki/evolving-strict/competitor-metrics/amocon-2026-event-scale.md
  - wiki/volatile-strict/competitor-news/amocon-2026-promo-april.md
- updated:
  - wiki/evolving-strict/competitor-metrics/ru-saas-revenue-rating-2025.md (+second source (Токовинин YouTube Q&A 2026-05-05) с amoCRM context; cross-link на amocon-2026-event-scale; примечание про personal-brand co-founder + flagship event как marketing-leverage в условиях замедления категории (amoCRM +7%))
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (+counter-anchor секция «passion-test (Токовинин, май 2026)» как 4-й голос: для значимой части аудитории «операционка» = passion-mismatch, не time-management problem. 3 inversion-hooks + anti-shaming caveat. Cross-links на passion-test и fear-vs-shyness pages)
  - wiki/canon/target-audience/gro-segments.md (+3 cross-links на новые Токовинин-фреймворки (fear-vs-shyness universal в 3 сегментах, peer-environment aspiration universal, passion-test specifically для Сегмента 2 предпринимателей))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving-strict: 2, evolving: 1, volatile-strict: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/yt_9YxLk3u__rI.md + 3 children (audio m4a + audio.mp3 + transcript.md) with sidecars (.note.md, .triage.json, .bundle.json)

## [2026-05-12 15:00] [ingest] | tg @eklapshinaofficial — дамп канала основателя GRO Лапшиной (822 постов, 2024-07 — 2026-05)
- source: wiki/sources/2026-05-12-tg-eklapshinaofficial.md
- created:
  - wiki/canon/brand-guidelines/lapshina-founder-tov.md
  - wiki/evolving/content-trends/eklapshinaofficial-channel-patterns.md
- updated:
  - wiki/canon/product-knowledge/gro-team.md (Добавлены: MAX-канал Лапшиной (max.ru/eklapshinaofficial), подкаст-серия #БеседысЛапшиной, сигнал коллаборации с Бехтеревой для GRO (пост #869), подтверждение AI-usage, участие в EVOLUT forum; добавлен новый источник и cross-links)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_eklapshinaofficial_20260512-134306.md

## [2026-05-12 13:30] [ingest] | @gro_me пост #210 — Спецпроект «30 вдохновляющих женщин» (PDF)
- source: wiki/sources/2026-05-12-tg-gro-me-210-women-pdf.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/documents/tg_gro_me_210.pdf

## [2026-05-12 14:00] [ingest] | ingest tg_gro_me_20260512-131154.md — официальный канал @gro_me, 338 постов, окт 2025 – май 2026
- source: wiki/sources/2026-05-12-tg-gro-me-channel-dump.md
- created:
  - wiki/canon/brand-guidelines/gro-channel-tone-of-voice.md
  - wiki/evolving/content-trends/gro-content-rubrics-system.md
  - wiki/evolving/product-reception/gro-channel-content-history.md
  - wiki/evolving-strict/product-metrics/gro-app-milestones.md
- updated:
  - wiki/canon/product-knowledge/gro-app-overview.md (Added Max as 5th distribution point, origin story via First Principles Method, reference to milestones page)
  - wiki/canon/product-knowledge/gro-team.md (Added TG channel dump as source confirming expert network (Bekhtereva, Chmukh, Zarubina et al.))
  - wiki/canon/positioning/gro-value-proposition.md (Added First Principles origin story section and conference trust-economy thesis)
  - wiki/canon/target-audience/gro-segments.md (Added confirmed audience identity labels (Предприимчивые, Неодинокие предприниматели) and gender data)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_gro_me_20260512-131154.md + 1 child (raw/processed/documents/tg_gro_me_340.pdf)

## [2026-05-14 12:32] [ingest] | vc.ru/hr конденсат 48 статей (май 2026) — IT-зарплаты, Garmony AI модель зрелости, ATS churn, маркетологи в избытке
- source: wiki/sources/2026-05-14-vcru-hr-condensed-48-articles.md
- created:
  - wiki/evolving-strict/market-data/ru-it-labor-market-salaries-2026.md
- updated:
  - wiki/evolving/competitor-positioning/garmony-ai-advertorial-campaign-2026.md (+4-уровневая модель зрелости AI-рекрутинга, классификация 5 классов, ROI-расчёт, расширенная карта конкурентов, цены рекрутинговых площадок 2026)
  - wiki/evolving-strict/market-data/ru-hr-tech-market-size-2026.md (+ATS churn 31%, AI-агент заменяет процессный HR, 83% кандидатов используют ChatGPT для резюме, личный бренд 46% IT)
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md (+маркетологи явно названы в избытке с прямой атрибуцией, Минфин Q1 МСБ -25%, ЦБ ставка 21% и НДС 22% как системные триггеры разворота)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 2, evolving: 3, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/_condense_web-vc-ru-hr_2026-05-14.md (+ .note.md sidecar)

## [2026-05-14 12:32] [ingest] | Спиридонов vc.ru/id79772 condensed (43 статьи) — AI-аватары, Hyperliquid, Wonder Family, China AI инфраструктура, constraint-innovation
- source: wiki/sources/2026-05-14-vcru-spiridonov-id79772-condensed.md
- created:
  - wiki/canon/marketing-frameworks/constraint-driven-innovation.md
  - wiki/evolving-strict/market-data/hyperliquid-microteam-benchmark-2026.md
  - wiki/volatile-strict/competitor-news/wonder-family-3-5m-round-2026.md
  - wiki/evolving/industry-trends/ai-digital-commerce-avatars-2026.md
- updated:
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md (Добавлен Сигнал 0: инфраструктурная статистика Strider/SCSP (250+ ДЦ, 750+ EFLOPS, 36 гуманоидов vs 8 у США, USA AI Action Plan))
  - wiki/canon/target-audience/gro-segments.md (Добавлен раздел «Психографический профиль предпринимателя по залёту» (Спиридонов) + новый под-сегмент родители-предприниматели Wonder Family)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (Добавлен раздел «Hyperliquid как экстремальный кейс микрокоманды» ($102.4M/employee) как anchor-точка)
  - wiki/evolving-strict/market-data/ai-vendor-revenue-per-employee-2026.md (Добавлена таблица non-AI outlier: Hyperliquid $102.4M/employee, Tether $93M/employee)
  - wiki/sources/2026-05-14-vcru-spiridonov-id79772-condensed.md (Stub расширен до полной source-страницы: метаданные, ключевые идеи, факты, связанные страницы)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 3, evolving-strict: 2, volatile-strict: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/_condense_web_vc.ru_id79772_2026-05-14.md

## [2026-05-14 12:35] [ingest] | ДП: закон об ИИ-изображениях/голосе в предвыборной агитации (2 мая 2026)
- source: wiki/sources/2026-05-02-dp-ru-ai-election-content-law.md
- created: none
- updated:
  - wiki/volatile-strict/industry-news/ru-ai-marking-law-2026.md (Добавлен закон от 2 мая 2026 о ИИ-образах в агитации (путин подписал), хронология расширена, новый раздел с нормами и маркетинговыми выводами, сигнал про авторские права vs AI-изображения)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_02_v-rf-opredelili-porjadok-primenenija_289a0a6f.md

## [2026-05-14 12:40] [ingest] | hh.ru кейс АШАН — массовый найм через звонки и чат-бот подбора
- source: wiki/sources/2026-05-14-hh-ru-ashan-mass-hiring-case.md
- created: none
- updated:
  - wiki/evolving-strict/campaign-metrics/hh-ru-call-channel-effectiveness-2026.md (добавлен раздел Enterprise-кейс АШАН: валидация маркированных звонков + метрики чат-бота (9,7→13,5%, 20% откликов))
  - wiki/evolving/competitor-positioning/hh-ru-ai-hiring-suite-2026.md (добавлен раздел Enterprise-валидация чат-бота подбора — кейс АШАН: adoption динамика + страх автоматизации vs реальная конверсия)
  - wiki/evolving/industry-trends/ru-retail-robotization-labor-deficit-2025-2026.md (добавлен раздел HR-автоматизация найма как параллельная волна: таблица двух векторов ответа ретейла на кадровый дефицит (физическая роботизация vs digital-автоматизация найма))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_hh.ru_article_kak-ashan-uskoril-massovyj-najm-s-pomoshchyu-zvonkov_15616078.md

## [2026-05-14 12:40] [ingest] | hh.ru × Вкусно — и точка: кобренд-кампания массового найма (×27,3 откликов, 2024)
- source: wiki/sources/2026-05-14-hh-ru-vkusno-i-tochka-cobrand-case.md
- created: none
- updated:
  - wiki/canon-strict/historical-campaigns/hh-ru-brand-center-cases-2025-2026.md (Добавлен кейс #7 (Вкусно — и точка × hh.ru): полный breakdown метрик кобренд-кампании конец 2024 — ×27,3 откликов, ×98 просмотров, 7,4M охват, DOOH post-view. Добавлена строка в сводную таблицу. Обновлён заголовок и счётчик кейсов (6→7). Добавлен источник sources/2026-05-14-...)
  - wiki/evolving-strict/campaign-metrics/branded-vacancy-pages-hh-2026.md (Supersession: запись «×27 откликов [conf:medium, src:2026-05-05]» заменена полным breakdown из первичного источника. Добавлено 8 строк с full metrics [conf:high, src:2026-05-14]. Добавлен блок Contradictions. Обновлён вывод об эластичности эффекта.)
- superseded: wiki/evolving-strict/campaign-metrics/branded-vacancy-pages-hh-2026.md (Вкусно—и точка entry conf:medium→conf:high, full breakdown)
- sensitive flag: none
- layer-touched: {canon-strict: 1, evolving-strict: 1, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/web_hh.ru_article_kak-kobrend-hh-ru-i-vkusno-i-tochka-uvelichil-otklik_072034cf.md

## [2026-05-14 12:40] [ingest] | ДП: KPI по блокировкам — бюджет ГРЧЦ из ФЗ-426 (третий независимый источник, финансирование верифицировано)
- source: wiki/sources/2026-05-14-dp-ru-rkn-vpn-kpi-budget-2026.md
- created: none
- updated:
  - wiki/volatile-strict/industry-news/ru-rkn-vpn-92pct-target-2030.md (Добавлены официальные бюджетные суммы ГРЧЦ из ФЗ-426 (20/9,9/9,8 млрд ₽); conf:low → conf:high на финансировании; новый третий источник)
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (Добавлен новый подраздел «Верификация финансирования 5-го вектора» с официальными бюджетными данными ФЗ-426)
- superseded: wiki/volatile-strict/industry-news/ru-rkn-vpn-92pct-target-2030.md (financing section: conf:low → superseded, conf:high in place)
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 1, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_06_kpi-po-blokirovkam-otsekut_ecd5c259.md

## [2026-05-14 12:45] [ingest] | dp.ru — синхронизация маркетинга и продаж (Часть 1): Shared KPIs + Lead Definition SLA + Feedback Loop
- source: wiki/sources/2026-05-14-dp-ru-marketing-sales-sync.md
- created:
  - wiki/canon/marketing-frameworks/marketing-sales-alignment-framework.md
- updated:
  - wiki/canon/marketing-frameworks/kpi-parallel-hypothesis-petrochenkov.md (добавлен cross-link на marketing-sales-alignment-framework как предпосылка параллельного тестирования)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_04_kak-nastroit-besperebojnuju_4d1259c6.md

## [2026-05-14 18:30] [ingest] | hh.ru: исследование оценки эффективности 2025 (38% adoption, HRTech-сигнал)
- source: wiki/sources/2026-05-14-hh-ru-performance-review-survey-2025.md
- created:
  - wiki/evolving-strict/market-data/ru-performance-review-adoption-2025.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (Расширен контекст HR-сегмента ЦА: Performance Review как зрелый инструмент в SMB)
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md (Добавлен сигнал зрелости HR-практик: 38% компаний делают регулярный Performance Review)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 1, canon: 1, evolving: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_hh.ru_article_kak-kompanii-rabotayut-s-ocenkoj-ehffektivnosti-issl_05d2cfb9.md

## [2026-05-14 18:30] [ingest] | vc.ru/molyanov condensed: ИИ-агенты + принцип настойчивости (36 статей)
- source: wiki/sources/2026-05-14-condense-web-vc-ru-molyanov.md
- created:
  - wiki/canon/marketing-frameworks/molyanov-ai-agent-workflow.md
  - wiki/evolving/content-trends/content-marketing-persistence-principle.md
- updated:
  - wiki/evolving/competitor-positioning/neyrotsekh-molyanov.md (Обогащение профиля Нейроцех: ссылки на новые страницы методологии Молянова и принцип настойчивости)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/_condense_web_vc.ru_molyanov_2026-05-14.md

## [2026-05-15 06:58] [ingest] | @eklapshinaofficial #896-897 incremental delta — Архитектор нового типа + Engineered scandal playbook
- source: wiki/sources/2026-05-14-tg-eklapshinaofficial-896-897.md
- created:
  - wiki/canon/marketing-frameworks/lapshina-architect-new-type-founder-archetype.md
  - wiki/evolving/content-trends/engineered-scandal-attention-playbook.md
- updated:
  - wiki/canon/brand-guidelines/lapshina-founder-tov.md (Добавлен раздел «Incremental delta 2026-05-14» с разборами постов #896 и #897, уточнены маркеры TOV)
  - wiki/evolving/content-trends/eklapshinaofficial-channel-patterns.md (Добавлен раздел «Incremental delta 2026-05-14» с новым sub-форматом hashtag-free long-form essay и расширением content-bank)
  - wiki/canon/positioning/gro-value-proposition.md (Добавлена ссылка на lapshina-architect-new-type-founder-archetype как концептуальную основу anti-positioning)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_eklapshinaofficial_20260514-070259.md + 1 child (media/tg_eklapshinaofficial_896.jpg)

## [2026-05-15 07:00] [ingest] | hh.ru condensed (12 articles): skills inflation + operational personnel + oil-gas + Deloitte AI-HR + 6 CPA strategies + Tuckman/Kotter change-mgmt
- source: wiki/sources/2026-05-14-condense-hh-ru-12-articles.md
- created:
  - wiki/canon/marketing-frameworks/internal-hiring-cost-reduction-strategies.md
  - wiki/evolving-strict/market-data/ru-operational-personnel-q2-2024.md
  - wiki/evolving-strict/market-data/ru-oil-gas-labor-market-2024.md
  - wiki/evolving/industry-trends/ai-in-hr-deloitte-model-2026.md
  - wiki/canon/marketing-frameworks/change-management-tuckman-kotter-ramazanov.md
- updated:
  - wiki/evolving/industry-trends/skill-based-hiring-russia-2026.md (Добавлен раздел «Skills inflation как развитие тренда»: ценность падает при росте числа навыков, IT-инструменты 3-5 лет жизни, Java -56%, MS PowerPoint -41,6%)
  - wiki/evolving-strict/market-data/ru-hiring-cost-benchmarks-2026.md (Добавлены драйверы роста стоимости найма 20-40% за 2 года, 6 стратегий снижения CPA с детальной таблицей и кейсами)
  - wiki/canon/marketing-frameworks/employer-branding-review-funnel.md (Добавлен Паттерн 12 — AlfaStrahovanie playbook: сбор feedback, 5 категорий open-text, anti-pattern «only positive», customer voice > company voice)
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md (Добавлен раздел «Продуктовые анонсы мая 2026 (5 новых фич)»: двухсторонние звонки, кастомизируемая воронка, 5 статусов отказа, поле «Оформление», trust badge)
  - wiki/evolving/content-trends/hh-ru-blog-content-patterns.md (Добавлен раздел «Структурный мета-обзор: 4 канонических шаблонa hh-статей»: pain-anchored, кейс с числом, аналитика, длинная экспертная статья)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, evolving-strict: 3, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/_condense_hh-ru_2026-05-14.md (+ .note.md + .triage.json + .bundle.json)

## [2026-05-15 07:00] [ingest] | vc.ru/story condensed (19 статей): PLG-SEO HoneyCup, монета доверия, онбординг ROI, Profi.ru 5-й голос, cautionary 90-х
- source: wiki/sources/2026-05-14-condense-web-vc-ru-story.md
- created:
  - wiki/canon/marketing-frameworks/honeycup-plg-programmatic-seo-2026.md
  - wiki/canon/marketing-frameworks/trust-as-managed-asset-coin-principle.md
  - wiki/canon/marketing-frameworks/corporate-holiday-content-anti-patterns.md
  - wiki/evolving-strict/campaign-metrics/digital-onboarding-roi-it-2026.md
  - wiki/evolving/content-trends/founder-expert-hook-family-vcru.md
- updated:
  - wiki/canon/target-audience/gro-segments.md (+cautionary-tale narrative для Сегмента 2: кейс Виктора Николаевича (1997 два магазина → 2026 пенсия 18.2K) как контрапункт к late-starter-founder hook-family)
  - wiki/evolving/industry-trends/freelance-platform-dependency.md (+5-й голос — Кейс 4 (Profi.ru): фрилансер с рейтингом 4.8+ и 5-летним стажем потерял аккаунт без объяснений; B2C-services-marketplace расширение)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/_condense_web_vc.ru_story_2026-05-14.md (+3 sidecars: .bundle.json, .note.md, .triage.json)

## [2026-05-15 07:00] [ingest] | @dnative дайджест 7598-7611 (14 постов, 12 media) — Insta bot purge, VK Донат Q1 2026, AI-screenshot crisis, agent-shopping skeptic
- source: wiki/sources/2026-05-14-tg-dnative-7598-7611.md
- created:
  - wiki/evolving-strict/competitor-metrics/instagram-bot-purge-may-2026.md
  - wiki/evolving-strict/competitor-metrics/vk-donat-revenue-q1-2026.md
  - wiki/evolving/content-trends/ai-screenshot-trust-crisis-2026.md
  - wiki/evolving/content-trends/dnative-ai-agent-shopping-skeptic-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-creator-economy-monetization-2026.md (Добавлен раздел про VK как строителя creator-monetization стека: VK Видео гранты 5M ₽ + VK Донат 718M ₽ Q1 2026, +26% YoY)
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md (Добавлен раздел 11 «Контр-нарратив B2C — dnative skeptic-thesis о Google Gemini agentic shopping»: первый артикулированный B2C-anti-bull тезис)
  - wiki/evolving/content-trends/contrarian-framing-expert-telegram.md (Добавлен подтверждающий кейс #2 (dnative AI-agent shopping skeptic): паттерн работает во второй вертикали; confidence повышен medium→high; вариация personal experience-anchor)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 2, evolving: 5, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_dnative_20260514-082937.md + 12 children (raw/processed/media/tg_dnative_7598..7611.jpg)

## [2026-05-15 07:05] [ingest] | hr-portal.ru condensed: 13 evergreen HR-объяснялок (baseline-портреты + textbook-фреймворки)
- source: wiki/sources/2026-05-14-condense-hr-portal-13-articles.md
- created:
  - wiki/canon/marketing-frameworks/thomas-kilmann-conflict-strategies.md
  - wiki/canon/marketing-frameworks/employee-adaptation-typology.md
  - wiki/canon/marketing-frameworks/us-japan-management-contrast.md
  - wiki/canon/target-audience/ru-key-account-manager-profile.md
  - wiki/canon-strict/legal-claims/ru-polygraph-hiring-2026.md
  - wiki/evolving/content-trends/hr-portal-evergreen-genre-2026.md
- updated:
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (Добавлен раздел «Baseline textbook-портрет предпринимателя (hr-portal.ru reference, 2026-05-14)» с каноническим списком черт и hook-кандидатами про адаптивность и копирование успеха)
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md (Добавлен раздел «Evergreen-бенчмарки текучести (контекст-якорь, hr-portal.ru reference)» с числами 5%/10-15%/>20% и «идеал безработицы не выше 5%»)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, canon-strict: 1, evolving: 2, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/_condense_hr-portal.ru_2026-05-14.md

## [2026-05-15 07:05] [ingest] | vc.ru/tbank condensed (27 статей 2019–2024): историческая основа T-Bank ecosystem
- source: wiki/sources/2026-05-14-condense-web-vc-ru-tbank-27.md
- created:
  - wiki/canon-strict/historical-campaigns/tbank-vselennaya-tinkoff-viral-2020.md
  - wiki/canon-strict/historical-campaigns/tbank-loyalty-clubs-pilot-2024.md
  - wiki/canon/marketing-frameworks/data-driven-viral-campaign-framework.md
  - wiki/canon/marketing-frameworks/ai-matching-at-scale-tinder-pattern.md
  - wiki/evolving-strict/competitor-metrics/tbank-historical-metrics-2019-2024.md
  - wiki/evolving-strict/market-data/ru-bnpl-aov-uplift-2023.md
  - wiki/evolving-strict/market-data/ru-payment-conversion-2022.md
  - wiki/evolving/content-trends/tbank-vc-ru-content-mix-2019-2024.md
- updated:
  - wiki/evolving/industry-trends/tbank-corporate-platform-stack-2026.md (Добавлен раздел Историческая основа 2019–2024: цепочка activations Олег → Инвесткопилка → Вселенная → VoiceKit → опционная Пармас → Tinkoff Pay → AI-matching → Долями × Рив Гош → IDентификация → Клубы лояльности с inline-маркерами и cross-link на 8 новых страниц)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, canon-strict: 2, evolving-strict: 3, evolving: 2, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/_condense_web_vc.ru_tbank_2026-05-14.md (+ .bundle.json, .note.md, .triage.json sidecars)

## [2026-05-15 07:05] [ingest] | tg @community_tech (Воронин, май-continuation): preventive social capital framework + cross-promo speaker-swap benchmark
- source: wiki/sources/2026-05-14-tg-community-tech-voronin-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/voronin-preventive-social-capital.md
  - wiki/evolving-strict/campaign-metrics/cross-promo-speaker-swap-benchmark-2026.md
- updated:
  - wiki/volatile/weekly-digest/voronin-community-tech-feb-apr-2026.md (Расширен continuation-секцией §5 (май 2026): преventive social capital операционализирован, cross-promo benchmark получен, ALARM/FOMO copywriting pattern; title обновлён, второй источник добавлен)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving-strict: 1, volatile: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_community_tech_20260514-090113.md + 4 children (images 983,986,987,989) → processed/

## [2026-05-15 07:15] [ingest] | TG @bossofyourboss — дамп 2026-05-14 (Claude DAU hockey-stick + ReStaff native-ad + USDT-блокировка июль 2026)
- source: wiki/sources/2026-05-14-tg-bossofyourboss-may-12-13-2026.md
- created:
  - wiki/canon/marketing-frameworks/hockey-stick-adoption-curve.md
- updated:
  - wiki/evolving-strict/competitor-metrics/llm-web-traffic-2026-04.md (Добавлен раздел DAU Similarweb (iOS+Android): Claude hockey-stick 1,5M→25M за 8 мес + сравнительная таблица Claude vs DeepSeek vs Grok Q1-Q2 2026 с точкой пересечения в марте; заголовок «LLM web-traffic снимок апрель 2026 (visits + DAU)»)
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (Добавлен 14-й вектор: банковская блокировка платежей в нелицензированные крипто-площадки с июля 2026; USDT-канал для выплат подрядчикам выходит из обращения)
  - wiki/evolving/content-trends/tabunov-founder-growth-hooks.md (Добавлены 2 новых раздела: hockey-stick adoption-нарратив «свидетельство инфлексии» — 5-блочный шаблон + метафора «извержение вулкана»; production native-ad шаблон «founder-объяснил-боль → решение» — 7-блочная структура с footer ИНН+ERID)
  - wiki/canon/marketing-frameworks/distributed-team-management-principles.md (Добавлен Принцип 6 — Payroll-инфраструктура — отдельный operational layer при 5+ распределённых исполнителях; mix-юрисдикций → bookkeeping nonlinear growth; регуляторный risk-watch USDT-блокировка; альтернативы ReStaff/Deel/Remote.com)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_bossofyourboss_20260514-084846.md + 2 children (tg_bossofyourboss_1197.jpg, tg_bossofyourboss_1198.jpg) → raw/processed/media/

## [2026-05-15 07:15] [ingest] | TG @howtomake10x май 2026 (1563-1570): phone detox protocol + parallel consulting unit-economics + Команда А cohort-size signal
- source: wiki/sources/2026-05-14-tg-howtomake10x-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/krylov-morning-phone-protocol.md
  - wiki/canon/marketing-frameworks/parallel-consulting-monetization-model.md
- updated:
  - wiki/evolving/industry-trends/ru-smb-mentor-community-market-2026.md (Углубление «Команда А» Крылова: cohort-size 200+ предпринимателей с 15+ млрд revenue в топе, parallel-consulting unit-economics, partner-network через Хирковского; пятый источник)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (Добавлены 3 новых hook раздела от Krylov 1563/1570: «окружение — главный актив консалтинга», «самый дорогой сотрудник проверяет мессенджеры 80 раз в день», «это не работа, это иллюзия контроля»; cross-link на counter-mode Hartmann)
  - wiki/evolving/product-reception/gro-productivity-energy-angle.md (Третий self-reported case под productivity/energy angle (Krylov 1570 — 80 проверок, 8h20m в телефоне); counter-anchor pair Hartmann vs Krylov для segmentation founder-content)
  - wiki/canon/marketing-frameworks/hartmann-instant-reply-principle.md (Cross-link на counter-mode Krylov morning phone protocol; добавлен второй источник)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_howtomake10x_20260514-085703.md + 5 children (media)

## [2026-05-15 07:30] [ingest] | tg-boris-again 6-14 мая: «неделя пет-проектов» (24 reader-pitches) + AI/ML дайджест W4-10 мая + 2 новых hook'а
- source: wiki/sources/2026-05-14-tg-boris-again-may-2026.md
- created:
  - wiki/evolving/content-trends/indie-pet-project-pitch-patterns-tg-2026.md
- updated:
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md (Add-on W4-10 мая 2026 (дайджест 3886): OpenAI GPT-Realtime семейство, GPT-5.5 Instant new default −52.5% галлюцинаций, Gemma 4 MTP 3× ускорение, Zyphra ZAYA1-8B all-AMD, Subquadratic SubQ 1M-Preview, Scale Labs SWE Atlas, RoundPipe, caveman skill; шестая неделя подряд)
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md (+Hook 17 «Anti-LLM-outreach» (Цейтлин 3890: скам-аутрич звучит человечнее AI-template) +Hook 18 «Agent-readable KB как пет-проект» (AnastasiyaW happyin.space 3897) +cross-link к новой странице indie-pet-project-pitch-patterns-tg-2026)
  - wiki/evolving/content-trends/telegram-author-channel-patterns.md (+Sub-pattern 4 «Weekly themed crowdsourced content» (@boris_again 2026-05 пет-projects week) — 4-я подкатегория author-channel формата; механика announce→curate→batch-publish, inverse normal mix 85% гости / 15% автор; baseline для GRO 1 curator-week в квартал)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, volatile-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_boris_again_20260514-094418.md* + 21 media children → processed/

## [2026-05-15 07:30] [ingest] | @gro_me посты 370–377 (мая 2026) — Зарубина (Сколково) + развёрнутый UGC Дарьи с verbatim anti-flattery validation
- source: wiki/sources/2026-05-14-tg-gro-me-370-377.md
- created:
  - wiki/canon/marketing-frameworks/zarubina-startup-mistakes-8.md
  - wiki/evolving/industry-trends/crisis-growth-niches-2026-zarubina.md
- updated:
  - wiki/canon/brand-guidelines/gro-channel-tone-of-voice.md (+anti-flattery встроен в TOV через UGC Дарьи; +новый гостевой автор Камила Зарубина в пуле экспертов)
  - wiki/evolving/product-reception/gro-channel-content-history.md (+посты 370–377 в May 2026 хронологии; +Арка 5 «гостевая экспертиза высокого уровня + UGC-валидация»)
  - wiki/evolving/content-trends/gro-content-rubrics-system.md (+шаблон карусели от внешнего эксперта (формат 6 карточек, 4:5, GRO-палитра); +расширение UGC #проGRO до полноценных нарративов; +Зарубина в списке гостевых авторов)
  - wiki/canon/product-knowledge/gro-testimonials.md (+4-й развёрнутый testimonial Дарьи (1500+ знаков, психопортрет, метрики 55→3000 читателей, anti-flattery hooks); +закрыт сегмент фрилансеров)
  - wiki/canon/positioning/gro-value-proposition.md (+4-й якорь дифференциации «спорит, но не отказывает» (anti-flattery, valid UGC); +«сильная комбинация» как рамка от Зарубиной для self-positioning)
  - wiki/evolving/customer-feedback/gro-app-store-reviews.md (+внешняя UGC-валидация anti-flattery позиции через testimonial Дарьи; +тройная валидация (Гуринович→Аннаков→Дарья) в карте dark-pattern)
  - wiki/evolving/content-trends/ai-flattery-dark-pattern.md (+4-й tier подтверждения (user-side UGC через Дарью @gro_me/377); +3 готовых hook-формулировки из verbatim цитаты)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 5, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_gro_me_20260514-070258.md + 8 children (raw/processed/media/tg_gro_me_370..377.jpg) с sidecars

## [2026-05-15 14:30] [ingest] | e-xecutive.ru condensed (34 vintage статьи): 12 canonical marketing-frameworks страниц + 1 content-trends
- source: wiki/sources/2026-05-14-condense-e-xecutive-ru-34-articles.md
- created:
  - wiki/canon/marketing-frameworks/niche-vs-mass-marketing.md
  - wiki/canon/marketing-frameworks/mckinsey-growth-cycles-feedback-loops.md
  - wiki/canon/marketing-frameworks/mckinsey-three-horizons-of-growth.md
  - wiki/canon/marketing-frameworks/creative-destruction-foster-kaplan.md
  - wiki/canon/marketing-frameworks/balanced-scorecard-kaplan-norton.md
  - wiki/canon/marketing-frameworks/mbo-smart-cascade.md
  - wiki/canon/marketing-frameworks/b2b-services-client-maturity-funnel.md
  - wiki/canon/marketing-frameworks/creative-pr-symbolic-expressiveness.md
  - wiki/canon/marketing-frameworks/mars-sales-methodology-fmcg.md
  - wiki/canon/marketing-frameworks/sales-manager-vs-salesperson-mars.md
  - wiki/canon/marketing-frameworks/employee-intrinsic-demotivation-6-factors.md
  - wiki/canon/marketing-frameworks/knowledge-management-codification-vs-personification.md
  - wiki/evolving/content-trends/fairytale-narrative-b2b-marketing.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 12, evolving: 1, sources: 1}
- touched: 14 pages
- raw: raw/processed/articles/_condense_e-xecutive.ru_2026-05-14.md (+ .note.md, .bundle.json, .triage.json sidecars)

## [2026-05-15 12:30] [ingest] | Дзен/Деловой Мир — Маркина (АЙNET INSIGHT): бренд-подкасты как маркетинговый канал
- source: wiki/sources/2026-05-14-dzen-delovoy-mir-brand-podcasts-markina.md
- created:
  - wiki/canon/marketing-frameworks/brand-podcast-launch-playbook.md
  - wiki/evolving/content-trends/brand-podcast-vs-integration-shift-2026.md
  - wiki/evolving-strict/market-data/ru-podcast-audience-2023-2025.md
- updated:
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md
  - wiki/evolving/content-trends/branded-media-tg-cross-channel-pattern.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 1, evolving-strict: 1, canon-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_dzen.ru_a_afjVchUdvlFXiBa4_a7891617.md

## [2026-05-15 12:33] [ingest] | Telegram @ai_newz — дамп 11 сообщений 4560–4571 (5–13 мая 2026)
- source: wiki/sources/2026-05-14-tg-ai-newz-may-2026.md
- created:
  - wiki/volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05.md
  - wiki/volatile-strict/competitor-news/google-gemini-omni-video-2026-05.md
  - wiki/volatile-strict/competitor-news/anthropic-third-party-credits-2026-06.md
- updated:
  - wiki/volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026.md
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md
  - wiki/volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05.md
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md
  - wiki/evolving/industry-trends/ai-native-marketer-skillset-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 5, evolving: 3, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_ai_newz_20260514-093955.md + 9 children (video/media)

## [2026-05-15 12:34] [ingest] | Telegram @alexander_visotsky — 36 постов 6–13 мая 2026 (1440 Camp + mobile launch + AI sales-audit)
- source: wiki/sources/2026-05-14-tg-alexander-visotsky-may-2026.md
- created:
  - wiki/evolving/content-trends/hiring-as-marketing-reframe-hook.md
  - wiki/evolving/content-trends/founder-conference-live-reportage-pattern.md
- updated:
  - wiki/evolving/competitor-positioning/business-booster-visotsky.md
  - wiki/evolving-strict/competitor-metrics/business-booster-platform-features-2026.md
  - wiki/evolving/content-trends/visotsky-ai-personal-assistant-narratives.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_alexander_visotsky_20260514-084454.md + 32 children (media/video/audio)

## [2026-05-15 12:43] [ingest] | Дзен/Деловой Мир — Шутенко: «Топливо для CEO» (когнитивная выносливость до 15:00)
- source: wiki/sources/2026-05-14-dzen-deloviy-mir-ceo-cognitive-endurance.md
- created:
  - wiki/evolving/content-trends/business-publication-ceo-listicle-pattern-2026.md
  - wiki/evolving/content-trends/ceo-somatic-energy-hooks.md
- updated:
  - wiki/evolving/product-reception/gro-productivity-energy-angle.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/web_dzen.ru_a_afoB41U4_3gzL2ft_32a68342.md

## [2026-05-15 12:51] [ingest] | Telegram @fomichevkirill — 7 сообщений 6–14 мая 2026 (follow-up дисциплина + Prodamus)
- source: wiki/sources/2026-05-14-tg-fomichevkirill-may-6-14-2026.md
- created:
  - wiki/canon/marketing-frameworks/sales-follow-up-second-touch-fomichev.md
  - wiki/evolving-strict/competitor-metrics/prodamus-paytech-metrics-2026.md
  - wiki/evolving/content-trends/founder-channel-sponsored-ad-formats-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-smb-mentor-community-market-2026.md
  - wiki/evolving/content-trends/ai-agents-demand-hooks-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_fomichevkirill_20260514-085547.md + 6 children (media/video)

## [2026-05-15 12:57] [ingest] | Telegram @cgevent — 50 сообщений 5–8 мая 2026 (AI-video / Hollywood institutional shift / Нейропрожарка)
- source: wiki/sources/2026-05-14-tg-cgevent-may05-08-2026.md
- created:
  - wiki/evolving/industry-trends/hollywood-ai-institutional-shift-2026.md
  - wiki/evolving/industry-trends/india-ai-film-lab-2026.md
  - wiki/evolving/industry-trends/humanoid-robot-narrative-shift-2026.md
  - wiki/evolving/content-trends/llm-sentiment-tracking-pattern-2026.md
  - wiki/evolving/content-trends/ai-impersonation-into-classic-scenes-2026.md
  - wiki/volatile-strict/competitor-news/bach-art-video-gen-2026-05.md
  - wiki/volatile/weekly-digest/tg-cgevent-may-w2-2026.md
- updated:
  - wiki/evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format.md
  - wiki/evolving/content-trends/ai-video-tools-stack-2026.md
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md
  - wiki/evolving/industry-trends/ai-knowledge-worker-climb-2025-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 7, volatile-strict: 1, volatile: 1, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_cgevent_20260514-093838.md + 48 children (media/video)

## [2026-05-15 13:15] [ingest] | Дзен/Деловой Мир — Сербин (ДоброПост): team-resilience framework
- source: wiki/sources/2026-05-14-dzen-delovoy-mir-serbin-team-resilience.md
- created:
  - wiki/canon/marketing-frameworks/serbin-team-resilience-framework.md
  - wiki/canon/marketing-frameworks/evening-facts-only-report-pattern.md
  - wiki/evolving/industry-trends/ru-china-import-tariff-2027-2029.md
  - wiki/evolving/content-trends/serbin-team-resilience-hooks.md
- updated:
  - wiki/canon/marketing-frameworks/distributed-team-management-principles.md
  - wiki/canon/marketing-frameworks/internal-change-communication-protocol.md
  - wiki/canon/marketing-frameworks/change-management-tuckman-kotter-ramazanov.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 2, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_dzen.ru_a_agL4lhUdvlFXlMHe_0a2e8e67.md

## [2026-05-15 13:17] [ingest] | Telegram @neuraldvig — 50 постов 5–12 мая 2026 (AI-news + anti-flattery prompt canon + T-Pay BLE)
- source: wiki/sources/2026-05-14-tg-neuraldvig-may-5-12-2026.md
- created:
  - wiki/evolving/content-trends/anti-flattery-prompt-canon-2026.md
  - wiki/evolving-strict/product-metrics/tpay-ble-launch-may-2026.md
  - wiki/canon/marketing-frameworks/ai-startup-failure-catalogue.md
- updated:
  - wiki/evolving/content-trends/ai-news-channel-prompt-packs.md
  - wiki/evolving/content-trends/ai-flattery-dark-pattern.md
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md
  - wiki/evolving-strict/competitor-metrics/llm-web-traffic-2026-04.md
  - wiki/evolving/content-trends/telegram-native-formats.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 5, evolving-strict: 2, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_neuraldvig_20260514-090543.md + 49 children (media/video)

## [2026-05-15 13:22] [ingest] | Telegram @grebenukm — 7456–7477 (5–14 мая 2026): crisis-defiance + six-seven aesthetics + Декларация s2
- source: wiki/sources/2026-05-14-tg-grebenukm-may-2026.md
- created:
  - wiki/evolving/content-trends/crisis-defiance-essay-long-form.md
  - wiki/evolving/content-trends/six-seven-aesthetics-anti-success-content-trend-2026.md
  - wiki/evolving/industry-trends/ru-premium-segment-cooling-2026.md
- updated:
  - wiki/evolving/competitor-positioning/grebenyuk-anomaly-community.md
  - wiki/evolving/content-trends/accountability-reality-show-format.md
  - wiki/evolving/content-trends/anti-authority-positioning-hook.md
  - wiki/canon/marketing-frameworks/grebenyuk-5-edinichek-framework.md
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
  - wiki/volatile-strict/industry-news/ru-vpn-metering-proposal-2026-04.md
  - wiki/evolving-strict/market-data/ru-premium-real-estate-q1-2026.md
- superseded: 1 (см. updated entries)
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 5, evolving-strict: 1, volatile-strict: 1, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_grebenukm_20260514-071823.md + 14 children (media/video)

## [2026-05-15 13:35] [ingest] | Дзен/Деловой Мир — 5 независимых каналов сбыта для маркетплейс-продавца
- source: wiki/sources/2026-05-14-dzen-delovoymir-marketplace-independent-channels.md
- created:
  - wiki/canon/marketing-frameworks/marketplace-distribution-diversification-5-channels.md
  - wiki/evolving-strict/campaign-metrics/ru-marketplace-channel-economics-2026-05.md
- updated:
  - wiki/evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026.md
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving-strict: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_dzen.ru_a_agLm2FrEqxFxxEbE_2e466e45.md

## [2026-05-15 18:30] [ingest] | Telegram @mspiridonov — 15 постов 2026-05-06…2026-05-14: 7 новых canon/strict страниц (Хуанг narrative preheating, 3 роли founder'а, sorting-test fragmented/modular, Marina Bay pivot, humanoid unit-economics, GLP-1 vs AI, consumer biotech) + 4 обновления
- source: wiki/sources/2026-05-14-tg-mspiridonov-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/huang-narrative-preheating-leadership.md
  - wiki/canon/marketing-frameworks/owner-strategist-operator-three-roles-separation.md
  - wiki/canon/marketing-frameworks/ai-amplifier-fragmented-vs-modular-jobs.md
  - wiki/canon/marketing-frameworks/netology-pivot-marina-bay-2012.md
  - wiki/evolving-strict/market-data/humanoid-robot-unit-economics-2024-2050.md
  - wiki/evolving-strict/market-data/glp1-vs-ai-consumer-biotech-2025.md
  - wiki/evolving/industry-trends/consumer-biotech-anti-aging-trend-2026.md
- updated:
  - wiki/canon/marketing-frameworks/jevons-paradox-ai-positioning.md (+третий verified-голос Спиридонова: рентгенологический кейс с 10-летним эмпирическим треком (Хинтон 2016 vs реальность 2026); таблица 3 голосов; cross-link на ai-amplifier-fragmented-vs-modular-jobs)
  - wiki/canon/marketing-frameworks/spiridonov-three-engagement-formats.md (+May 2026 promo: Время сильных 2026 co-branded event с Атлантами; еженедельные разборы Метод 2.0 с Варварой Львовой; адрес ЦА бизнес ≥50M ₽ выручки/год)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (+Counter-anchor рентгенологического кейса Спиридонова; двух-критериальный sorting-test fragmented vs modular jobs)
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md (+Экономический контекст: unit-economics humanoid'ов McKinsey/Bain/Morgan Stanley объясняет почему Китай production-hub для high-wage экспорта)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 3, evolving-strict: 2, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_mspiridonov_20260514-083423.md + 5 children (tg_mspiridonov_4385/4390/4398/4399/4400.jpg)

## [2026-05-15 16:30] [ingest] | Дзен/Деловой Мир — Григорьев (Aiston): цифровая трансформация МСБ vs автоматизация
- source: wiki/sources/2026-05-14-dzen-aiston-grigoryev-digital-transformation-smb-2026.md
- created:
  - wiki/canon/marketing-frameworks/automation-vs-digital-transformation-framework.md
  - wiki/canon/marketing-frameworks/ai-smb-pilot-three-traps.md
- updated:
  - wiki/evolving/industry-trends/ru-smb-trends-corpmsp-2025.md
  - wiki/evolving/content-trends/wtf-hr-ai-skeptic-hooks.md
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md
  - wiki/canon/marketing-frameworks/ankusheva-ai-implementation-triad.md
  - wiki/evolving/industry-trends/ru-marketing-digital-paralysis-mar2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 4, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_dzen.ru_a_agLOuVU4_3gzOgaz_45279fa1.md

## [2026-05-15 16:35] [ingest] | Telegram @olegcloser (Шевелев) — 7–13 мая 2026 (СОПРАНО + формула доверия + 3 инструмента Здесь и Сейчас)
- source: wiki/sources/2026-05-14-tg-olegcloser-may-7-13-2026.md
- created:
  - wiki/canon/marketing-frameworks/soprano-discovery-technique.md
  - wiki/canon/marketing-frameworks/trust-formula-shevelev-echo.md
  - wiki/canon/marketing-frameworks/here-and-now-closing-tools-3.md
  - wiki/evolving/content-trends/expert-cobranded-tg-carousel-pattern.md
- updated:
  - wiki/canon/marketing-frameworks/sales-100-formula-shevelev.md
  - wiki/canon/marketing-frameworks/objection-after-holidays-vrkr.md
  - wiki/canon/marketing-frameworks/business-reality-show-format.md
  - wiki/evolving/competitor-positioning/zakryvatel-sdelok-ai-agent.md
  - wiki/evolving/content-trends/sales-ai-narrative-hooks-2026.md
- superseded: 1 (см. updated entries)
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_olegcloser_20260514-084835.md + 13 children (media)

## [2026-05-15 16:37] [ingest] | Telegram @techsparks (Андрей Себрант) — 17 постов 6–14 мая 2026 (5583–5599)
- source: wiki/sources/2026-05-14-tg-techsparks-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/ai-general-purpose-technology-analogy.md
  - wiki/canon/marketing-frameworks/sebrant-cult-of-linearity.md
  - wiki/canon/marketing-frameworks/ai-native-dev-andre-dataist.md
  - wiki/canon/marketing-frameworks/anthropic-constitutional-reasoning-paper-2026.md
  - wiki/evolving/content-trends/slopshaming-counter-hook-2026.md
  - wiki/evolving/content-trends/ai-doomer-marcus-anachronism-hook.md
  - wiki/volatile-strict/competitor-news/thinking-machines-interaction-model-2026-05.md
  - wiki/volatile-strict/competitor-news/google-googlebook-2026-fall.md
- updated:
  - wiki/evolving/content-trends/sebrant-cognitive-exoskeleton-hooks.md
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 3, volatile-strict: 2, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/tg_techsparks_20260514-094318.md + 14 children (video/media)

## [2026-05-15 16:49] [ingest] | Дзен/Деловой Мир — Варако (Далее): HR-бренд как инструмент выживания 2026
- source: wiki/sources/2026-05-14-dzen-delovoymir-varako-hr-brand-survival-2026.md
- created:
  - wiki/canon/marketing-frameworks/varako-hr-brand-survival-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md
  - wiki/canon/marketing-frameworks/employer-branding-review-funnel.md
  - wiki/canon/marketing-frameworks/hr-brand-ambassador-program.md
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md
  - wiki/evolving/content-trends/employee-content-employer-trust-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_dzen.ru_a_agQ-rFrEqxFxxgre_ebe205ba.md

## [2026-05-15 16:57] [ingest] | Telegram @peregudov — 10 постов 431–440 (май 2026): First Day Thinking + Билдеры
- source: wiki/sources/2026-05-14-tg-peregudov-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/first-day-thinking-peregudov.md
  - wiki/canon/marketing-frameworks/builders-role-merging-peregudov.md
  - wiki/evolving/content-trends/practitioner-shifts-position-format.md
- updated:
  - wiki/canon/marketing-frameworks/multi-agent-marketing-org-principles.md
  - wiki/evolving/industry-trends/ai-native-company-architecture-2026.md
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md
  - wiki/canon/marketing-frameworks/peregudov-vibecoding-founder-playbook-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_peregudov_20260514-090248.md + 5 children (media/video)

## [2026-05-15 17:01] [ingest] | vc.ru Telegram @vcnews — дайджест 50 постов 5–8 мая 2026
- source: wiki/sources/2026-05-14-tg-vcnews-may-5-8-2026.md
- created:
  - wiki/volatile-strict/competitor-news/anthropic-claude-dreams-mode-2026-05.md
  - wiki/volatile-strict/competitor-news/openai-realtime-audio-models-2026-05.md
  - wiki/volatile-strict/competitor-news/openai-chatgpt-spreadsheets-2026-05.md
  - wiki/volatile-strict/competitor-news/spacexai-rename-2026-05.md
  - wiki/volatile-strict/competitor-news/apple-ios27-third-party-ai-2026.md
  - wiki/volatile-strict/competitor-news/apple-intelligence-settlement-2026-05.md
  - wiki/volatile-strict/industry-news/character-ai-pennsylvania-lawsuit-2026-05.md
  - wiki/volatile-strict/industry-news/samsung-exits-china-consumer-2026.md
  - wiki/evolving-strict/competitor-metrics/deepseek-valuation-2026-05.md
  - wiki/evolving-strict/competitor-metrics/moonshot-kimi-arr-2026-05.md
- updated:
  - wiki/volatile-strict/industry-news/ai-model-releases-mar-apr-2026.md
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
  - wiki/evolving-strict/competitor-metrics/instagram-bot-purge-may-2026.md
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 8, evolving-strict: 3, evolving: 3, sources: 1}
- touched: 15 pages
- raw: raw/processed/articles/tg_vcnews_20260514-071415.md + 48 children (media/video)

## [2026-05-15 19:32] [ingest] | Налогообложение дистанционных работников — zhazhda.biz (reference article)
- source: wiki/sources/2026-05-14-zhazhda-biz-base-nalogooblozhenie-distancionnyh-rabotnikov.md
- created:
  - wiki/canon-strict/legal-claims/ru-remote-worker-tax-residency-distinction.md
- updated:
  - wiki/canon/marketing-frameworks/distributed-team-management-principles.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, canon: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/web_zhazhda.biz_base_nalogooblozhenie-distancionnyh-rabotnikov_640f10a7.md

## [2026-05-15 19:36] [ingest] | Telegram @recruiter_live — дамп 14 постов (ids 4456..4469, май 2026)
- source: wiki/sources/2026-05-14-tg-recruiter-live-may-2026.md
- created:
  - wiki/evolving/industry-trends/ru-recruitment-fraud-patterns-2026.md
  - wiki/volatile-strict/industry-news/ru-ma-deals-q1-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-job-seeker-experience-2026.md
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md
  - wiki/evolving/industry-trends/ru-offline-retail-decline-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, evolving-strict: 1, volatile-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_recruiter_live_20260514-071518.md

## [2026-05-15 19:40] [ingest] | Telegram @ProductsAndStartups (Байрам Аннаков) — 9 постов 6–14 мая 2026 (1740–1748)
- source: wiki/sources/2026-05-14-tg-products-and-startups-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/vibecoding-stanford-study-2026.md
  - wiki/canon/marketing-frameworks/slot-machine-vs-printer-genai-strategies.md
  - wiki/canon/marketing-frameworks/generative-ui-design-system-inference.md
  - wiki/canon/marketing-frameworks/ceo-cto-ai-adoption-bridge.md
  - wiki/evolving-strict/competitor-metrics/stanford-vibecoding-stats-apr-2026.md
  - wiki/evolving/competitor-positioning/ai-product-engineer-course-empatika-2026.md
- updated:
  - wiki/canon/marketing-frameworks/harness-engineering-for-ai-agents.md
  - wiki/canon/marketing-frameworks/claude-skills-architecture.md
  - wiki/evolving/content-trends/ai-product-engineer-content-hooks.md
  - wiki/evolving/industry-trends/ai-productivity-j-curve-2026.md
  - wiki/evolving/industry-trends/ai-cognitive-atrophy-identity-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving: 3, evolving-strict: 1, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_ProductsAndStartups_20260514-090022.md

## [2026-05-15 19:44] [ingest] | Жажда — ТОП-10 мобильных приложений для предпринимателя (evergreen ~2015-2017)
- source: wiki/sources/2026-05-14-zhazhda-mobile-apps-for-entrepreneur-evergreen.md
- created:
  - wiki/evolving/content-trends/zhazhda-biz-evergreen-listicle-genre.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_mobilnye-prilozheniya-dlya-predprinimatelya_85e1b288.md

## [2026-05-15 19:48] [ingest] | Telegram @rff_channel — Recruitment for Friends, 6–13 мая 2026 (10 постов, ids 4403..4416, HH April 2026 чарты + RConf AI promo)
- source: wiki/sources/2026-05-14-tg-rff-channel-may-2026.md
- created:
  - wiki/evolving-strict/market-data/hh-vacancies-resumes-cooling-2024-2026.md
  - wiki/volatile-strict/competitor-news/rconf-ai-cultural-fit-2026-05.md
- updated:
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md
  - wiki/evolving/industry-trends/ru-hr-tech-ai-landscape-2026.md
  - wiki/canon/marketing-frameworks/varako-hr-brand-survival-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 2, volatile-strict: 1, evolving: 1, canon: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_rff_channel_20260514-071537.md

## [2026-05-15 19:52] [ingest] | Telegram @Theedinorogblog (Дмитрий Филонов) — 26 постов 7923–7948 (5–14 мая 2026)
- source: wiki/sources/2026-05-14-tg-theedinorog-may-2026.md
- created:
  - wiki/volatile-strict/competitor-news/openai-musk-trial-may-2026.md
  - wiki/volatile-strict/competitor-news/openai-anthropic-secondary-share-ban-2026-05.md
  - wiki/volatile-strict/competitor-news/anthropic-openai-business-customers-may-2026.md
  - wiki/volatile-strict/competitor-news/isomorphic-labs-2-1b-raise-2026-05.md
  - wiki/evolving/content-trends/musk-tone-flip-pattern.md
  - wiki/volatile/weekly-digest/edinorog-may-2026-digest.md
- updated:
  - wiki/volatile-strict/industry-news/openai-altman-new-yorker-dossier.md
  - wiki/evolving-strict/competitor-metrics/deepseek-valuation-2026-05.md
  - wiki/evolving-strict/competitor-metrics/nebius-arr-2025-2026.md
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md
  - wiki/evolving/industry-trends/humanoid-robot-narrative-shift-2026.md
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
  - wiki/volatile-strict/competitor-news/anthropic-spacex-colossus-rental-2026-05.md
  - wiki/volatile-strict/competitor-news/spacexai-rename-2026-05.md
  - wiki/volatile-strict/competitor-news/thinking-machines-interaction-model-2026-05.md
  - wiki/volatile-strict/industry-news/character-ai-pennsylvania-lawsuit-2026-05.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 2, volatile-strict: 6, volatile: 1, sources: 1}
- touched: 16 pages
- raw: raw/processed/articles/tg_Theedinorogblog_20260514-084756.md

## [2026-05-15 19:56] [ingest] | Обзор российских премий для предпринимателей — Жажда
- source: wiki/sources/2026-05-14-zhazhda-biz-lifestyle-premii-dlja-predprinimatelej-v-rossii.md
- created:
  - wiki/canon/marketing-frameworks/business-awards-as-smb-pr-channel.md
- updated:
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md
  - wiki/canon/marketing-frameworks/infopovod-criteria-smb-pr.md
  - wiki/canon/marketing-frameworks/outlier-content-pr-case-studies.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_premii-dlja-predprinimatelej-v-rossii_c84fc520.md

## [2026-05-15 20:00] [ingest] | Telegram @rybakovigor — выгрузка 9 постов 6–12 мая 2026 (бандл с 7 медиа)
- source: wiki/sources/2026-05-14-tg-rybakovigor-may06-12-2026.md
- created:
  - wiki/canon/marketing-frameworks/career-growth-decoupling-rybakov.md
  - wiki/evolving/content-trends/founder-philanthropy-panel-format.md
- updated:
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md
  - wiki/evolving/content-trends/founder-history-edutainment-format.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_rybakovigor_20260514-082958.md

## [2026-05-15 20:55] [ingest] | Telegram @bezsmuzi (Максим Кульгин) — дамп 50 постов 5–7 мая 2026
- source: wiki/sources/2026-05-14-tg-bezsmuzi-may-5-7.md
- created:
  - wiki/volatile-strict/competitor-news/openai-gpt-5-5-every-review-2026-05.md
  - wiki/volatile-strict/competitor-news/xai-grok-4-3-release-2026-05.md
  - wiki/volatile-strict/competitor-news/microsoft-trellis-2-image-to-3d-2026-05.md
  - wiki/volatile-strict/industry-news/ru-cyberdruzhiny-mediapatrols-decree-2026-05.md
  - wiki/volatile-strict/industry-news/ru-domain-verification-gosuslugi-sept-2026.md
  - wiki/volatile-strict/industry-news/ru-minpromtorg-cross-border-vat-2027-2029.md
  - wiki/volatile-strict/industry-news/ru-yaplakal-blocked-2026-05.md
  - wiki/evolving/competitor-positioning/konsol-pro-freelance-compliance-2026.md
  - wiki/evolving/competitor-positioning/studio-lebedeva-2026.md
  - wiki/evolving/content-trends/niche-billionaire-revenue-reveal-format.md
  - wiki/evolving/content-trends/founder-cafe-coldpitch-fundraising-hook.md
  - wiki/evolving/industry-trends/ru-it-relocation-minsk-2026.md
- updated:
  - wiki/evolving-strict/competitor-metrics/llm-web-traffic-2026-04.md (+market-share OpenAI 77%→56% / Gemini 25% / Claude ~6% (Кульгин 15870); +Grok 4.3 + GPT-5.5 + TRELLIS.2 release context)
  - wiki/evolving-strict/competitor-metrics/llm-token-pricing-deflation-2025-2026.md (+Grok 4.3 row ($2.50/M output) fills mid-tier price point)
  - wiki/evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026.md (+numeric anchors 1% net margin (1к/105к) + 80% селлеров оборот ~600к/мес (independent cross-check))
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (+4 новых вектора: 18 кибердружины, 19 верификация доменов, 20 блок ЯПлакалъ, 17.5 НДС cross-check (Кульгин))
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 7, evolving: 5, evolving-strict: 3, sources: 1}
- touched: 16 pages
- raw: raw/processed/articles/tg_bezsmuzi_20260514-085258.md + 42 children (media/video, PDF 15894 missing)

## [2026-05-16 12:00] [ingest] | zhazhda.biz листикл «программы и сервисы для бухучета» (~2017) — no relevant extractions (override haiku verdict)
- source: wiki/sources/2026-05-14-zhazhda-biz-lifestyle-programmy-i-servisy-dlya-buhucheta-efc2dd3b.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_programmy-i-servisy-dlya-buhucheta_efc2dd3b.md (+ .note.md + .triage.json + .bundle.json)

## [2026-05-15 20:12] [ingest] | Telegram @solokumi (Роман Кумар Виас) — 12 постов 5–12 мая 2026 (FETE-фреймворк + GEO-плейбук + Claude Code Skills volume 2)
- source: wiki/sources/2026-05-14-tg-solokumi-may-2026.md
- created:
  - wiki/canon/marketing-frameworks/fete-outreach-framework-clay.md
  - wiki/evolving/content-trends/geo-playbook-2026-q2.md
  - wiki/evolving/competitor-positioning/refocus-claude-code-marketing-stack-2026.md
- updated:
  - wiki/evolving/content-trends/claude-code-skills-bank-2026.md
  - wiki/evolving/content-trends/aeo-geo-llm-search-optimization-2026.md
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md
  - wiki/evolving/content-trends/sales-ops-ai-tooling-stack-2026.md
  - wiki/canon/marketing-frameworks/seo-for-ai-era-playbook.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 6, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_solokumi_20260514-084911.md

## [2026-05-15 19:32] [ingest] | Telegram @breakingtrends — 23 поста 5–14 мая 2026 (Mash −40M TG, Anthropic+Blackstone, MS 67%, Хуанг blue-collar)
- source: wiki/sources/2026-05-14-tg-breakingtrends-may05-14.md
- created:
  - wiki/volatile-strict/competitor-news/anthropic-blackstone-consulting-2026-05.md
  - wiki/volatile-strict/competitor-news/claude-blocks-ru-accounts-2026-05.md
  - wiki/volatile-strict/competitor-news/android-pause-point-doomscroll-2026.md
  - wiki/volatile-strict/industry-news/disney-ru-license-exit-2027.md
  - wiki/evolving/content-trends/founder-mode-monk-mode-relationships-hook.md
  - wiki/evolving/industry-trends/blue-collar-ai-resilience-2026.md
  - wiki/evolving-strict/market-data/ms-ai-67pct-org-success-2026.md
  - wiki/evolving/content-trends/pay-for-performance-ai-superusers-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-telegram-blocking-max-migration-2026.md (+Mash quantitative anchor: TG потерял ~40M юзеров, access rate 98%→13%)
  - wiki/volatile-strict/industry-news/ru-mobile-internet-shutdowns-may-2026.md (+Минцифры 2026-05-07 подтверждение 9 мая full shutdown без white-list, без SMS; 7 и 8 мая — без ограничений)
  - wiki/evolving/industry-trends/ai-knowledge-worker-climb-2025-2026.md (+Сигнал 11: Fortune pay-for-performance + AI-superusers (Google + Accenture); cross-link на новую content-trends страницу)
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (+Хуанг blue-collar counter-anchor (+30%/+25% за 3 года); cross-link на новую industry-trends страницу)
  - wiki/evolving/competitor-positioning/breaking-trends-pr-agency.md (+3-й дамп; +новый voice axis (Виктория Загитова HRD/COO на Lenta.ru); rhythm ↓ до 2.5 поста/день)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, evolving-strict: 1, volatile-strict: 4, sources: 1}
- touched: 13 pages
- raw: raw/processed/articles/tg_breakingtrends_20260514-082953.md + 19 children (17 media + 2 video)

## [2026-05-15 20:20] [ingest] | zhazhda.biz «Программы и сервисы для ведения бюджета» (evergreen ~2016) — 6-й образец жанра
- source: wiki/sources/2026-05-14-zhazhda-budget-apps-evergreen-2016.md
- created:
  - wiki/evolving/content-trends/ru-personal-finance-listicle-baseline-2016.md
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_programmy-i-servisy-dlya-vedeniya-byudzheta_f0d4dcb6.md

## [2026-05-15 20:24] [ingest] | Cossa.ru (@cossaru) — Telegram-дайджест за 5–14 мая 2026
- source: wiki/sources/2026-05-14-tg-cossaru-may-5-14-2026.md
- created:
  - wiki/evolving-strict/market-data/digital-ad-cpm-shifts-q1-2026.md
  - wiki/evolving-strict/market-data/ogilvy-influencer-trends-2026.md
  - wiki/evolving-strict/market-data/duda-ai-traffic-conversion-2026.md
  - wiki/evolving-strict/campaign-metrics/mindbox-channel-shift-2025.md
  - wiki/evolving-strict/market-data/ru-crm-agency-market-2025.md
  - wiki/canon/marketing-frameworks/dmitry-kot-ai-text-5-insights.md
  - wiki/canon/marketing-frameworks/ai-skills-vs-prompts-architecture.md
  - wiki/canon/marketing-frameworks/ai-search-measurable-vs-dark-zone.md
  - wiki/canon/marketing-frameworks/smm-analytics-2026-framework.md
  - wiki/evolving/industry-trends/digital-indoor-retail-media-ru-2026.md
  - wiki/evolving/content-trends/real-life-video-content-developer-case.md
  - wiki/evolving/content-trends/ai-aeo-must-haves-2026.md
- updated:
  - wiki/canon/marketing-frameworks/ai-text-markers-checklist.md
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md
  - wiki/evolving/industry-trends/influencer-marketplace-failure-paradox.md
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 3, evolving-strict: 5, sources: 1}
- touched: 16 pages
- raw: raw/processed/articles/tg_cossaru_20260514-082854.md

## [2026-05-15 20:28] [ingest] | Telegram @startupoftheday (Александр Горный) — 15 постов 5–13 мая 2026 (5053–5067)
- source: wiki/sources/2026-05-14-tg-startupoftheday-may-5-13-2026.md
- created:
  - wiki/canon/marketing-frameworks/llm-bot-customer-tolerance-gorny-frame.md
  - wiki/evolving/content-trends/llm-self-censorship-hook-gorny-2026.md
  - wiki/volatile-strict/competitor-news/agentsbar-ai-partnership-matchmaking-2026-05.md
  - wiki/volatile-strict/competitor-news/qcomment-fake-review-market-ru-2026.md
  - wiki/canon/marketing-frameworks/gdp-vs-marketcap-flow-stock-distinction-gorny.md
  - wiki/canon/marketing-frameworks/marketplace-distributor-revival-model-neato.md
  - wiki/canon/marketing-frameworks/paid-demo-cold-outreach-thesis-gorny.md
  - wiki/evolving/industry-trends/big-tech-concentration-not-bubble-gorny-2026.md
  - wiki/evolving/competitor-positioning/dadata-brand-by-inn-ru-sales-enrichment-2026.md
- updated:
  - wiki/evolving/competitor-positioning/aiacademy-claude-code-course-gorny-shevchenko-2026.md
  - wiki/canon/marketing-frameworks/fete-outreach-framework-clay.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 3, volatile-strict: 2, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_startupoftheday_20260514-071623.md

## [2026-05-15 19:35] [ingest] | Жажда: 9 сервисов онлайн-записи клиентов ~2016 — pre-YClients RU online-booking SaaS baseline
- source: wiki/sources/2026-05-14-zhazhda-online-booking-services-evergreen-2016.md
- created:
  - wiki/evolving/content-trends/ru-online-booking-saas-baseline-2016.md
  - wiki/evolving/competitor-positioning/yclients-pre-dominance-context-2016.md
- updated:
  - wiki/evolving/content-trends/zhazhda-biz-evergreen-listicle-genre.md (+6th observed instance (online-booking services ~2016): подтверждение жанровых маркеров (анонимность, отсутствие дат, TOP-N, parsing-loss имён прод...)
  - wiki/evolving-strict/competitor-metrics/ru-saas-revenue-rating-2025.md (+historical context для YClients +43%: ссылка на 2016-snapshot baseline (YClients не упоминался в 2016, лидер в 2025) — типовая длина SMB-SaaS-конс...)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+source link: online-booking SaaS demand 2016-snapshot — ещё одно подтверждение SMB-сервисного-сегмента (салоны/авто/мед/общепит))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 1, canon: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_servisy-dlya-onlajn-zapisi-klientov_6c6bf379.md

## [2026-05-15 20:36] [ingest] | TG @egoshin_kedprof — мини-дамп 3 постов 5–12 мая 2026 (подкаст «Поколение ИИ», Claude RU-block + Нейрофонд EGOSHIN800, Gemini 3.1 Pro thermo-demo)
- source: wiki/sources/2026-05-14-tg-egoshin-kedprof-may-5-12-2026.md
- created:
  - wiki/canon/marketing-frameworks/egoshin-education-formula-2026.md
  - wiki/evolving/competitor-positioning/neurofond-positioning-2026-05.md
  - wiki/volatile-strict/industry-news/anthropic-ru-block-egoshin-vendor-confirmation-2026-05.md
- updated:
  - wiki/canon/marketing-frameworks/egoshin-ai-adoption-ladder.md
  - wiki/canon/product-knowledge/gro-team.md
  - wiki/evolving/content-trends/ai-translator-curator-channel-pattern-egoshin.md
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, volatile-strict: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_egoshin_kedprof_20260514-085652.md

## [2026-05-15 20:40] [ingest] | Telegram @stodnevka2 (Армен Петросян) — 6–14 мая 2026, 11 постов + 1 медиа
- source: wiki/sources/2026-05-14-tg-stodnevka2-may-6-14-2026.md
- created:
  - wiki/canon/marketing-frameworks/petrosian-flexible-goal-pole.md
  - wiki/canon/marketing-frameworks/petrosian-perspective-shift-questions.md
  - wiki/canon/marketing-frameworks/petrosian-content-as-accelerator.md
  - wiki/canon/marketing-frameworks/petrosian-i-only-try-five-minute-start.md
  - wiki/canon/marketing-frameworks/petrosian-supporter-vs-challenger-confidant.md
  - wiki/canon/marketing-frameworks/petrosian-ball-task-prioritization.md
- updated:
  - wiki/canon/marketing-frameworks/krylov-morning-phone-protocol.md
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md
  - wiki/evolving/industry-trends/max-messenger-author-rejection-2026.md
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 7, evolving: 3, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/tg_stodnevka2_20260514-090104.md

## [2026-05-16 12:00] [ingest] | zhazhda.biz листикл «Выбираем планировщик задач для предпринимателя» (evergreen ~2016) — 7-й инстанс жанра
- source: wiki/sources/2026-05-16-zhazhda-task-manager-business-evergreen-2016.md
- created:
  - wiki/evolving/content-trends/ru-task-manager-listicle-baseline-2016.md
  - wiki/canon/marketing-frameworks/saas-tool-selection-rubric-pre-ai-2016.md
- updated:
  - wiki/evolving/content-trends/zhazhda-biz-evergreen-listicle-genre.md (+7-й инстанс жанра (task-manager листикл) — matrix-вариация (5 продуктов × 3 платформенных кластера), parsing-artifacts (потеря заголовков секций, ...)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+Pre-AI productivity-стек сегмента (Todoist/Wunderlist/Things 2016) как shared mental model founder'ов 30+; positioning GRO как complementary, не s...)
  - wiki/evolving/content-trends/daily-streak-gamification-in-finance.md (+Todoist Karma (~2013) как ранний массовый productivity-gamification prior — расширен historical-перенос streak-паттерна (productivity → fitness → ...)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 3, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_task-manager-business_2ab7ae12.md + 3 sidecars (.bundle.json, .note.md, .triage.json)

## [2026-05-15 20:48] [ingest] | Telegram @hh_ru_official — 12 постов (7–13 мая 2026): итоги «Галочки» + студенческая карусель стажировок
- source: wiki/sources/2026-05-14-tg-hh-ru-official-may-7-13-2026.md
- created:
  - wiki/evolving-strict/campaign-metrics/hh-ru-galochka-campaign-results-2026.md
- updated:
  - wiki/evolving/content-trends/hh-ru-galochka-mascot-campaign.md
  - wiki/evolving/content-trends/hh-ru-blog-content-patterns.md
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_hh_ru_official_20260514-071559.md

## [2026-05-15 20:52] [ingest] | Telegram @techno_yandex — 6 постов 6–13 мая 2026 (bundle)
- source: wiki/sources/2026-05-14-tg-techno-yandex-may-6-13-2026.md
- created:
  - wiki/canon/marketing-frameworks/ai-tech-glossary-techno-yandex-2026.md
  - wiki/canon/marketing-frameworks/techno-pessimism-vs-optimism-historical-frame.md
  - wiki/evolving/content-trends/dead-internet-theory-counter-trend-2026.md
  - wiki/evolving/content-trends/voice-to-text-tools-roundup-2026-05.md
  - wiki/evolving/content-trends/techno-yandex-explainer-rubric-format.md
  - wiki/volatile-strict/competitor-news/google-fitbit-air-health-2026-05.md
  - wiki/volatile-strict/competitor-news/spotify-personal-podcasts-ai-agents-2026-05.md
  - wiki/volatile-strict/competitor-news/telegram-ai-bots-styles-update-2026-05.md
  - wiki/volatile-strict/competitor-news/familiar-machines-companion-robot-2026.md
- updated:
  - wiki/volatile-strict/competitor-news/openai-gpt-5-5-every-review-2026-05.md
  - wiki/volatile-strict/competitor-news/unity-agent-beta-2026.md
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 3, volatile-strict: 6, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/tg_techno_yandex_20260514-091243.md

## [2026-05-15 20:56] [ingest] | Жажда.biz: 5 полезных курсов для предпринимателя (ноябрь–декабрь 2016)
- source: wiki/sources/2026-05-14-zhazhda-biz-treningi-dec-2016.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 0 pages
- raw: raw/processed/articles/web_zhazhda.biz_lifestyle_treningi-dec-2016_a2bdff4f.md

## [2026-05-15 21:00] [ingest] | Telegram @telega_Rinata (Ринат Алиев) — 6 постов 7–13 мая 2026 (вуз+ИИ, сон, founder-camp, эмоция, выплаты, passion)
- source: wiki/sources/2026-05-14-tg-telega-rinata-may-7-13-2026.md
- created:
  - wiki/canon/marketing-frameworks/passion-driven-work-criterion-gerasimova.md
  - wiki/evolving/content-trends/dominant-emotion-hiring-hook.md
  - wiki/sources/2026-05-14-tg-telega-rinata-may-7-13-2026.md
- updated:
  - wiki/evolving/content-trends/telegram-native-formats.md
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
  - wiki/evolving/product-reception/gro-productivity-energy-angle.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 5, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_telega_Rinata_20260514-090100.md

## [2026-05-15 21:04] [ingest] | Telegram @HR_kak_delat — 6 постов 6–14 мая 2026 (ids 1984–1989): HBR 5 шагов оргизменений + 3 engagement-механики HR-клуба + RBI рекрутер
- source: wiki/sources/2026-05-14-tg-hr-kak-delat-may-6-14-2026.md
- created:
  - wiki/canon/marketing-frameworks/hbr-5-org-change-tips-2026.md
  - wiki/evolving/content-trends/hr-club-engagement-mechanics-2026.md
  - wiki/evolving/competitor-positioning/hr-kak-delat-club-community-positioning.md
- updated:
  - wiki/canon/marketing-frameworks/change-management-tuckman-kotter-ramazanov.md
  - wiki/canon/marketing-frameworks/internal-change-communication-protocol.md
  - wiki/evolving/content-trends/job-posting-as-content-2026.md
  - wiki/canon/target-audience/hrd-portrait-2025-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_hr_kak_delat_20260514-071521.md

## [2026-05-15 21:08] [ingest] | Telegram @hutzp — выборка 14 сообщений (3513–3527, 2026-05-06…2026-05-13): joint-giveaway + промо Изионист-сборника + Прохоров-кейс + личное
- source: wiki/sources/2026-05-14-tg-hutzp-may-2026-bundle.md
- created:
  - wiki/evolving/content-trends/joint-multi-author-giveaway-pattern.md
  - wiki/evolving/content-trends/short-form-history-business-parable-pattern.md
- updated:
  - wiki/evolving/content-trends/telegram-author-channel-patterns.md
  - wiki/evolving/competitor-positioning/settersgroup-ecosystem.md
  - wiki/evolving/industry-trends/russian-cultural-code-branding-2026.md
  - wiki/evolving/content-trends/founder-history-edutainment-format.md
  - wiki/evolving/content-trends/sweepstake-promocode-combo-mechanics.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 7, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_hutzp_20260514-084900.md

## [2026-05-15 21:12] [ingest] | Дзен/Деловой Мир — Селихов: новый потребитель e-commerce и психология онлайн-покупок 2025
- source: wiki/sources/2026-05-14-dzen-delovoymir-selikhov-ecommerce-consumer-2026.md
- created:
  - wiki/canon/marketing-frameworks/risk-first-consumer-decision-online.md
  - wiki/evolving/industry-trends/ecommerce-trust-decision-shift-ru-2026.md
  - wiki/evolving-strict/market-data/ru-ecommerce-consumer-journey-2026.md
  - wiki/evolving/content-trends/gender-split-product-listing-ru-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-ecommerce-platformization-reshetnikov-2026.md
  - wiki/volatile-strict/industry-news/ru-counterfeit-marketplaces-letter-2026-04.md
  - wiki/canon/marketing-frameworks/trust-as-managed-asset-coin-principle.md
  - wiki/canon/marketing-frameworks/marketplace-distribution-diversification-5-channels.md
  - wiki/evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026.md
  - wiki/evolving/customer-feedback/gro-app-store-reviews.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, evolving-strict: 3, volatile-strict: 1, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/web_dzen.ru_a_agRnG1rEqxFxxkyL_fb7e7514.md

## [2026-05-15 21:16] [ingest] | Telegram: @temno — Аркадий Морейнис, дайджест 5–14 мая 2026 (16 постов + 16 изображений, ids 7818..7833)
- source: wiki/sources/2026-05-14-tg-temno-moreynis-may-5-14-2026.md
- created:
  - wiki/canon/marketing-frameworks/latent-demand-ai-startup-search-moreynis.md
  - wiki/canon/marketing-frameworks/genius-audience-over-genius-idea-moreynis.md
  - wiki/canon/marketing-frameworks/corporate-raider-mental-model-lutke.md
  - wiki/canon/marketing-frameworks/switching-tools-product-pattern-moreynis.md
  - wiki/canon/marketing-frameworks/digital-basement-peer-learning-lutke.md
  - wiki/canon/marketing-frameworks/three-question-product-test-moreynis.md
  - wiki/evolving/industry-trends/marketplace-community-convergence-2026.md
  - wiki/evolving/content-trends/marketing-for-ai-agents-content-hooks.md
- updated:
  - wiki/canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis.md
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md
  - wiki/canon/marketing-frameworks/jevons-paradox-ai-positioning.md
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md
  - wiki/evolving/content-trends/moreynis-hand-drawn-meme-format.md
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving: 2, sources: 1}
- touched: 15 pages
- raw: raw/processed/articles/tg_temno_20260514-083415.md

## [2026-05-15 21:20] [ingest] | Telegram @incrussiamedia — дайджест 5–11 мая 2026 (50 сообщений)
- source: wiki/sources/2026-05-14-tg-incrussiamedia-may-5-11-2026.md
- created:
  - wiki/canon/marketing-frameworks/self-service-fitness-model-2026.md
  - wiki/canon/marketing-frameworks/frambini-marketing-tax-counter-hook.md
  - wiki/evolving-strict/market-data/ru-msp-state-support-q1-2026.md
  - wiki/evolving-strict/market-data/ru-side-gig-shift-pay-q1-2026.md
  - wiki/evolving-strict/market-data/ru-newcomer-wage-overtake-2025.md
  - wiki/evolving/content-trends/inc-russia-brand-history-series-2026.md
  - wiki/volatile-strict/industry-news/ru-fns-outstaff-control-2026-05.md
  - wiki/volatile-strict/industry-news/morgan-stanley-etrade-crypto-2026-05.md
- updated:
  - wiki/evolving-strict/market-data/ru-psychology-services-2025-2026.md
  - wiki/evolving-strict/market-data/ru-fitness-club-unit-economics-2026.md
  - wiki/canon/marketing-frameworks/breakage-business-model-fitness.md
  - wiki/evolving/industry-trends/ru-fitness-market-2016-2026.md
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md
  - wiki/evolving-strict/market-data/ru-msp-credit-volume-2025.md
  - wiki/evolving/content-trends/short-form-history-business-parable-pattern.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, evolving-strict: 5, volatile-strict: 2, sources: 1}
- touched: 16 pages
- raw: raw/processed/articles/tg_incrussiamedia_20260514-071921.md

## [2026-05-16 13:35] [ingest] | Дзен/Деловой Мир — «Экономия как новая роскошь»: умное потребление и predictive loyalty (Euromonitor + Кравченко + Demis Group)
- source: wiki/sources/2026-05-14-dzen-delovoymir-smart-consumption-marketing-2026.md
- created:
  - wiki/canon/marketing-frameworks/smart-consumption-status-shift-2026.md
  - wiki/canon/marketing-frameworks/kravchenko-predictive-loyalty-2026.md
  - wiki/canon/marketing-frameworks/two-russias-regional-split-2026.md
  - wiki/evolving/content-trends/dupe-trend-russia-2026.md
  - wiki/evolving/content-trends/consumer-manipulation-marketing-tactics-2026.md
  - wiki/evolving/industry-trends/optical-personalization-gap-2026.md
  - wiki/evolving-strict/market-data/global-consumer-anxiety-euromonitor-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-ecommerce-platformization-reshetnikov-2026.md (Третий cross-check 11,5 трлн ₽ / +28% YoY (Деловой Мир со ссылкой на АКИТ); добавлено ключевое уточнение «основная динамика роста — регионы»)
  - wiki/canon/marketing-frameworks/yudin-personalization-vs-manipulation-test.md (Добавлена секция Consumer-side: пользователи применяют тест «наизнанку» (70% cart-abandonment, 64% trial-cancel, 72% service-shopping) — поведенчес...)
  - wiki/canon/marketing-frameworks/real-time-personalization-cvm-mechanics.md (Update 2026-05-16 — industry-wide gap: 64% «оптической» персонализации, <18% глубокого AI; ссылка на новую gap-страницу)
  - wiki/evolving-strict/market-data/deloitte-marketing-trends-2026.md (Cross-corroboration к Сдвигу 2 «потребители-избирательные диктаторы»: Euromonitor 3/5, 72%, 64% поведенческие метрики из Делового Мира 2026-05-14)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 3, evolving-strict: 3, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/web_dzen.ru_a_agRthxUdvlFXlr0Z_25b10ec3.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json)

## [2026-05-15 21:28] [ingest] | Telegram @kwork_kwork — пост 565 (2026-05-12): тизер про влияние цены на решение о покупке
- source: wiki/sources/2026-05-14-tg-kwork-may12-2026-pricing-teaser.md
- created: none
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 0 pages
- raw: raw/processed/articles/tg_kwork_kwork_20260514-071611.md

## [2026-05-16 14:44] [ingest] | Telegram @moibiz — Нацагентство «Мой бизнес» дайджест 5–14 мая 2026 (43 сообщения + 39 медиа-вложений)
- source: wiki/sources/2026-05-14-tg-moibiz-may-5-14-2026.md
- created:
  - wiki/volatile-strict/industry-news/ru-sbp-b2b-limit-30m-2027.md
  - wiki/volatile-strict/industry-news/ru-mediator-platforms-registry-2026-05.md
  - wiki/volatile-strict/industry-news/ru-msp-innovation-residents-2026-05.md
  - wiki/evolving-strict/market-data/ru-macro-snapshot-may-2026.md
  - wiki/evolving-strict/market-data/ru-ip-count-2026-may.md
  - wiki/evolving-strict/market-data/ru-creative-industries-public-perception-2026.md
  - wiki/canon/target-audience/ru-msp-tech-demand-2026.md
  - wiki/canon/marketing-frameworks/ru-smb-financing-ladder-8-instruments.md
- updated:
  - wiki/evolving-strict/market-data/ru-self-employed-2025.md
  - wiki/volatile-strict/industry-news/ru-fns-outstaff-control-2026-05.md
  - wiki/evolving/competitor-positioning/max-messenger.md
  - wiki/evolving/competitor-positioning/novatorix-moibiz-ai-consultant-2026.md
  - wiki/evolving-strict/market-data/ru-franchise-market-q1-2026.md
  - wiki/evolving-strict/market-data/ru-msp-state-support-q1-2026.md
  - wiki/evolving/competitor-positioning/tbiznes-smb-support-defensive-positioning-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 3, evolving-strict: 5, volatile-strict: 3, sources: 1}
- touched: 15 pages
- raw: raw/processed/articles/tg_moibiz_20260514-082641.md (+ 38 children: media/video/audio bundled)

## [2026-05-16 14:45] [ingest] | Telegram @rb_ru — B2B-дайджест 5–13 мая 2026 (45 постов + 45 children)
- source: wiki/sources/2026-05-14-tg-rb-ru-may-5-13-2026.md
- created:
  - wiki/evolving/competitor-positioning/lidertask-strive-positioning.md
  - wiki/evolving-strict/market-data/ru-messenger-ad-platforms-share-2026.md
  - wiki/evolving/industry-trends/ru-ad-agency-experimentation-fear-2026.md
  - wiki/volatile-strict/competitor-news/wildberries-ai-assistant-wb-pomoshnik-2026.md
  - wiki/canon/marketing-frameworks/niche-filling-vacated-market-pattern.md
  - wiki/evolving-strict/market-data/ru-gender-pay-gap-2025.md
  - wiki/evolving-strict/market-data/ru-layoff-disputes-2026.md
  - wiki/evolving-strict/market-data/ru-women-wellness-shift-2026.md
  - wiki/evolving/industry-trends/ru-exotic-tourism-shift-2026.md
  - wiki/evolving/competitor-positioning/rb-ru-print-magazine-positioning.md
- updated:
  - wiki/evolving-strict/market-data/ru-it-labor-market-salaries-2026.md
  - wiki/volatile-strict/competitor-news/claude-blocks-ru-accounts-2026-05.md
  - wiki/volatile-strict/competitor-news/openai-musk-trial-may-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 3, evolving-strict: 5, volatile-strict: 2, sources: 1}
- touched: 14 pages
- raw: raw/processed/articles/tg_rb_ru_20260514-072036.md (+ 44 children: media/video bundled)

## [2026-05-16 14:48] [ingest] | Telegram @vcnews — 50 постов 8–12 мая 2026: AI-гонка (Codex Chrome + Daybreak + Deployment Co + ByteDance $30B), Cerebras price-up, Apple-Intel + AirPods, T-Bank Долями BNPL-aggregator
- source: wiki/sources/2026-05-14-tg-vcnews-may-8-12-2026.md
- created:
  - wiki/volatile-strict/competitor-news/openai-codex-chrome-extension-2026-05.md
  - wiki/volatile-strict/competitor-news/openai-deployment-company-tomoro-2026-05.md
  - wiki/volatile-strict/competitor-news/openai-daybreak-gpt55-cyber-2026-05.md
  - wiki/volatile-strict/competitor-news/openai-chatgpt-emergency-contact-2026-05.md
  - wiki/volatile-strict/competitor-news/apple-airpods-camera-siri-2026-05.md
  - wiki/volatile-strict/competitor-news/apple-intel-chip-deal-2026-05.md
  - wiki/volatile-strict/competitor-news/bytedance-ai-capex-30b-2026-05.md
  - wiki/volatile-strict/competitor-news/mirumi-companion-robot-2026-05.md
  - wiki/volatile-strict/competitor-news/tbank-doli-bnpl-aggregator-2026-05.md
  - wiki/volatile-strict/industry-news/ru-budget-deficit-2026-q1.md
  - wiki/volatile-strict/industry-news/ru-china-trade-q1-2026.md
  - wiki/volatile-strict/industry-news/yandex-mlu-eu-fine-2026-05.md
  - wiki/evolving/content-trends/character-collectibles-trend-2026.md
  - wiki/evolving/industry-trends/screenless-wearables-trend-2026.md
- updated:
  - wiki/volatile-strict/competitor-news/claude-blocks-ru-accounts-2026-05.md (vcnews 61269 cross-source confirmation Baza-источника)
  - wiki/volatile-strict/industry-news/cerebras-ipo-2026-05.md (Supersession: цена $115-125 → $150-160, target $3.5B → $4.8B, cap $48.8B)
  - wiki/volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05.md (+Codex Chrome ext +OpenAI Daybreak — расширение OpenAI на 2 новых фронта)
  - wiki/volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026.md (vcnews 61277 reconcile: 423 уязвимостей Firefox, baseline 20-30/мес, Mozilla не доверяет автофикс)
  - wiki/canon/marketing-frameworks/ai-text-markers-checklist.md (vc.ru третий независимый источник на AI-text маркеры — confidence high)
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (Update W19/W20 — eight-front race)
  - wiki/volatile-strict/industry-news/ru-mobile-internet-shutdowns-may-2026.md (vcnews 61284: Минцифры официально снимает ограничения 9 мая — cycle closed)
  - wiki/evolving/competitor-positioning/tbank-doli-bnpl-sub-brand-palette-lavender.md (Product-architecture evolution: solo BNPL → BNPL-aggregator)
  - wiki/evolving/industry-trends/humanoid-robot-narrative-shift-2026.md (vcnews cross-source on Unitree GD01, Mirumi character-toy parallel, 4 sub-categories)
  - wiki/volatile-strict/competitor-news/replit-stripe-3digit-growth-2026-05.md (vcnews 61298 cross-source: Replit CEO про Cursor-дифференциацию)
- superseded: wiki/volatile-strict/industry-news/cerebras-ipo-2026-05.md
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 4, volatile-strict: 12, sources: 1}
- touched: 24 pages
- raw: raw/processed/articles/tg_vcnews_20260514-071959.md + 47 children (44 jpg + 3 mp4 in media/ and video/)

## [2026-05-18 05:42] [ingest] | Telegram @your_pet_project — Табунов посты 621–629 (6–13 мая 2026, третий ingest канала, дельта 9 постов)
- source: wiki/sources/2026-05-13-tg-your-pet-project-may-6-13-2026.md
- created:
  - wiki/canon/marketing-frameworks/build-in-public-as-paid-traffic-anti-pattern.md
  - wiki/canon/marketing-frameworks/social-proof-traffic-asset-framework-tabunov.md
  - wiki/canon/marketing-frameworks/ai-influencer-grandma-playbook.md
  - wiki/canon/marketing-frameworks/five-no-pet-project-tabunov.md
  - wiki/evolving-strict/competitor-metrics/yp-may-2026-50k-mrr-app-cluster.md
  - wiki/volatile-strict/industry-news/supreme-ai-bot-merc-decay-case-2026-05.md
- updated:
  - wiki/evolving/content-trends/your-pet-project-channel-hooks.md
  - wiki/canon/marketing-frameworks/bootstrap-vs-startup-tabunov.md
  - wiki/evolving/content-trends/ai-solopreneur-narrative-hooks.md
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 1, evolving-strict: 1, volatile-strict: 1, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/tg_your_pet_project_20260514-083418.md (+ 7 children: 7 jpg in media/ bundled)

## [2026-05-18 05:46] [ingest] | Telegram @vyakuba — 46 постов 5–14 мая 2026 (Самуи/Панган тур, 8-card carousel «Эволюция мышления», Apple-ecosystem-frame, Goyard anti-marketing, club reopen)
- source: wiki/sources/2026-05-14-tg-vyakuba-may-5-14-2026.md
- created:
  - wiki/canon/marketing-frameworks/yakuba-thinking-evolution-levels.md
  - wiki/canon/marketing-frameworks/goyard-anti-marketing-luxury-friction.md
  - wiki/canon/marketing-frameworks/apple-ecosystem-recurring-revenue-frame.md
  - wiki/canon/marketing-frameworks/first-15-sec-sales-contact.md
- updated:
  - wiki/evolving/competitor-positioning/vyakuba-sales-training.md
  - wiki/evolving/content-trends/vyakuba-instagram-carousel-format.md
  - wiki/evolving/content-trends/ru-sales-infobiz-content-patterns.md
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md
  - wiki/evolving/content-trends/sales-ai-narrative-hooks-2026.md
  - wiki/canon/marketing-frameworks/peer-environment-aspiration-tokovinin.md
  - wiki/canon/marketing-frameworks/premium-perception-through-price.md
  - wiki/canon/marketing-frameworks/ai-amplifier-fragmented-vs-modular-jobs.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 7, evolving: 5, sources: 1}
- touched: 13 pages
- raw: raw/processed/articles/tg_vyakuba_20260514-083912.md (+ 38 children: 24 jpg + 14 mp4 in media/ and video/ bundled)

## [2026-05-18 06:53] [ingest] | Telegram @recruiter_live — micro-пост 4470 (LinkedIn активность 14 мая 2026)
- source: wiki/sources/2026-05-16-tg-recruiter-live-may-14-2026.md
- created: none
- updated:
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (LinkedIn-активность + cross-channel перенос на @jobsIndustry, RU recruitment-тренд)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/tg_recruiter_live_20260516-091000.md

## [2026-05-18 07:03] [ingest] | Telegram @typicalcompany — 3 поста 6-12 мая 2026 (productized-pivot + AI-операционка Remove/Compress/Rebuild + Jobs 1995 «product-vs-marketing»)
- source: wiki/sources/2026-05-14-tg-typicalcompany-may-6-12-2026.md
- created:
  - wiki/canon/marketing-frameworks/typical-productized-services-pivot.md
  - wiki/canon/marketing-frameworks/ai-productivity-3-levers-typical.md
  - wiki/canon/marketing-frameworks/jobs-product-vs-marketing-people-1995.md
- updated:
  - wiki/evolving/competitor-positioning/typical-company.md (+ 3 поста, content-pause закрыт, ритм 2-3 поста/нед)
  - wiki/canon/marketing-frameworks/ai-productivity-3-shifts-typical.md (cross-link с новой рамкой 3 рычагов)
  - wiki/volatile-strict/competitor-news/apple-intelligence-settlement-2026-05.md (TYPICAL-фрейм Jobs-1995 как объяснительная рамка $250M settlement)
  - wiki/evolving/industry-trends/ai-for-managers-2025-2026.md (+ TYPICAL post 1331/1332/1333 продолжение narrative)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, volatile-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_typicalcompany_20260514-071139.md (+ 1 child: video/tg_typicalcompany_1333.mp4 — Jobs «Lost Interview» 40 sec)

## [2026-05-18 07:06] [ingest] | Telegram @typicalcompany — 2 поста 14–15 мая 2026 (Anthropic 81k AI-рисков + OpenAI dual-CEO Альтман/Симо IPO $850B)
- source: wiki/sources/2026-05-16-tg-typicalcompany-may-14-15-2026.md
- created:
  - wiki/canon/marketing-frameworks/typical-six-ai-management-risks.md
  - wiki/canon/marketing-frameworks/openai-dual-ceo-management-contours.md
  - wiki/evolving-strict/market-data/anthropic-81k-ai-concerns-regional-2026.md
  - wiki/evolving/industry-trends/ai-narrative-second-phase-risk-pivot-2026.md
  - wiki/volatile-strict/competitor-news/openai-fidji-simo-ipo-ceo-2026-05.md
- updated:
  - wiki/evolving/industry-trends/ai-for-managers-2025-2026.md (+ second-phase narrative pivot risk-discipline)
  - wiki/evolving/competitor-positioning/typical-company.md (+ 2 поста, регулярная публикация подтверждена)
  - wiki/volatile-strict/industry-news/openai-852b-valuation-doubt-2026.md (+ dual-CEO context Симо)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, evolving-strict: 1, volatile-strict: 2, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_typicalcompany_20260516-010500.md (+ 1 child: media/tg_typicalcompany_1335.jpg — slope-chart Anthropic 81k)

## [2026-05-18 07:17] [ingest] | GRO — страница оплаты интенсива (groapp.ru/payment-intensive-tarif2): second monetization track high-ticket B2B
- source: wiki/sources/2026-05-16-groapp-payment-intensive-tarif2.md
- created:
  - wiki/canon/product-knowledge/gro-intensive.md
- updated:
  - wiki/canon/product-knowledge/gro-pricing.md (+ second track «Интенсив», структурная картина: подписка 2 490 ₽/мес + high-ticket Интенсив)
  - wiki/canon/product-knowledge/gro-app-overview.md (+ ссылка на второй продуктовый трек)
  - wiki/canon/target-audience/gro-segments.md (+ B2B/cohort-формат как доп. surface для трёх сегментов)
  - wiki/canon/positioning/gro-value-proposition.md (+ second-track как extension value-prop)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_groapp.ru_payment-intensive-tarif2_88d64388.md

## [2026-05-18 07:22] [ingest] | Дзен/Деловой Мир — Том Соулфул (Drivee): «Управлять не надо кричать», стили управления 2026
- source: wiki/sources/2026-05-14-dzen-delovoy-mir-soulful-management-styles-2026.md
- created:
  - wiki/canon/marketing-frameworks/management-styles-2026-soulful.md
  - wiki/canon/marketing-frameworks/delegation-formula-7-elements-soulful.md
  - wiki/canon/marketing-frameworks/management-style-obsolete-6-signals-soulful.md
  - wiki/canon/marketing-frameworks/manager-weekly-reflection-3-questions-soulful.md
  - wiki/canon/marketing-frameworks/cry-as-cheap-system-crutch-soulful.md
  - wiki/evolving/content-trends/expert-column-corporate-pr-format-soulful.md
- updated:
  - wiki/evolving-strict/market-data/employee-engagement-quiet-quitting-2026.md (+ Gallup-цитирование Соулфула на quiet-quitting)
  - wiki/evolving-strict/market-data/ru-it-labor-market-salaries-2026.md (+ hh/SuperJob-цитата на дефицит кадров)
  - wiki/evolving/industry-trends/gen-z-workforce-shift-2026.md (+ Соулфул-фрейм ситуативный leadership под Gen-Z)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 2, evolving-strict: 2, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/web_dzen.ru_a_agTL9FrEqxFxxuMk_704d6174.md

## [2026-05-18 07:23] [ingest] | Pressfeed: 13 кейсов адаптации российских компаний к ИИ-поиску (GEO/AEO RU practitioner consensus, май 2026)
- source: wiki/sources/2026-05-18-pressfeed-13-cases-ai-search-adaptation.md
- created:
  - wiki/evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026.md
  - wiki/evolving-strict/market-data/ru-ai-search-traffic-share-2026.md
  - wiki/canon/marketing-frameworks/llm-friendly-video-transcription.md
  - wiki/evolving/industry-trends/seo-to-pr-substitution-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md (+ 13 кейсов RU-practitioner-data)
  - wiki/evolving/content-trends/aeo-geo-llm-search-optimization-2026.md (+ RU specifics для Яндекс/Алисы)
  - wiki/canon/marketing-frameworks/seo-for-ai-era-playbook.md (+ RU operational дополнения)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 4, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_13-istorij-o-tom-kak-kompanii-adaptiruyutsya-k-ii-poisku_cf123429.md

## [2026-05-18 07:30] [ingest] | Pressfeed: 4 способа подготовить интересный инфоповод для статьи (PR-практика SMB)
- source: wiki/sources/2026-05-18-pressfeed-4-sposoba-infopovod.md
- created:
  - wiki/canon/marketing-frameworks/infopovod-generation-4-techniques.md
- updated:
  - wiki/canon/marketing-frameworks/infopovod-criteria-smb-pr.md (+ 4 техники конструирования как extension критериев)
  - wiki/canon/marketing-frameworks/performance-pr-framework.md (+ техники как input PR-funnel)
  - wiki/canon/marketing-frameworks/outlier-content-pr-case-studies.md (+ примеры через 4 техники)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_4-sposoba-podgotovit-interesnyj-infopovod-dlya-stati_4532e031.md

## [2026-05-18 07:33] [ingest] | Pressfeed: 22 идеи для пресс-релизов + 7 типов + newsjacking (PR-таксономия SMB)
- source: wiki/sources/2026-05-18-pressfeed-22-press-release-ideas.md
- created:
  - wiki/canon/marketing-frameworks/press-release-types-7-categories.md
  - wiki/canon/marketing-frameworks/press-release-22-topic-ideas.md
  - wiki/canon/marketing-frameworks/newsjacking-technique.md
- updated:
  - wiki/canon/marketing-frameworks/infopovod-criteria-smb-pr.md (+ матрица 22 тем как операционный каталог)
  - wiki/canon/marketing-frameworks/performance-pr-framework.md (+ типизация relevant под PR-канал)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_22-idei-dlya-vashih-press-relizov-kakie-temy-zainteresuyut-k_dcc9c3b3.md

## [2026-05-18 06:42] [ingest] | Pressfeed: 14 историй об освоении MAX (Mediascope 61,5 млн mar 2026, CPA ЭКО 244 ₽, Thai Traditions B2B-as-Slack)
- source: wiki/sources/2026-05-18-pressfeed-14-max-cases.md
- created:
  - wiki/evolving-strict/campaign-metrics/max-messenger-channel-economics-2026.md
  - wiki/evolving/content-trends/max-messenger-content-patterns-2026.md
- updated:
  - wiki/evolving/competitor-positioning/max-messenger.md (supersession: day-rate → exact IAP 2 490 ₽: + Pressfeed-14 meta-сигнал отраслевой компиляции — Mediascope 61,5 млн mar 2026 (+43,6% YoY), CPA ЭКО 244 ₽ = TG-парит, +40% Q1 спрос на ботов, лимит 5 ботов/ЮЛ, 30% брендов готовы к channel-migration; +10-й под-паттерн Thai Traditions B2B-as-Slack)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, evolving-strict: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_14-istorij-ob-osvoenii-messendzhera-maks_c487d612.md (+ .note.md + .triage.json sidecars)

## [2026-05-18 21:28] [ingest] | Pressfeed: 7 шагов к построению сильного личного бренда в 2026 (Юлия Магась, PReach)
- source: wiki/sources/2026-05-18-pressfeed-magas-personal-brand-7-steps.md
- created:
  - wiki/canon/marketing-frameworks/personal-brand-7-steps-magas.md
  - wiki/canon/marketing-frameworks/ravix-group-niche-spike-case.md
  - wiki/canon/marketing-frameworks/expert-content-pillar-topology-magas.md
  - wiki/canon/marketing-frameworks/personal-brand-channels-5-types-magas.md
  - wiki/canon/marketing-frameworks/competitor-positioning-research-10-15-magas.md
- updated:
  - wiki/evolving/content-trends/personal-brand-shift-2026.md
  - wiki/canon/marketing-frameworks/niche-vs-mass-marketing.md
  - wiki/canon/marketing-frameworks/microniche-marketing-packages.md
  - wiki/canon/marketing-frameworks/performance-pr-framework.md
  - wiki/canon/marketing-frameworks/infopovod-criteria-smb-pr.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 9, evolving: 1, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_7-shagov-k-postroeniyu-silnogo-lichnogo-brenda-v-2026-godu_2999b8a0.md

## [2026-05-18 21:28] [ingest] | Pressfeed: B2B-пиар после эпохи простых охватов (вебинар-анонс, агентство 4D, 21 мая 2026) — сдвиг от каналов к экспертному влиянию + 7-мерная модель измерения цифрового следа
- source: wiki/sources/2026-05-18-pressfeed-b2b-pr-after-simple-reach.md
- created:
  - wiki/canon/marketing-frameworks/b2b-pr-influence-shift-2026.md
  - wiki/canon/marketing-frameworks/pr-measurement-digital-footprint.md
  - wiki/evolving/content-trends/b2b-pr-formats-analytical-content-2026.md
- updated:
  - wiki/canon/marketing-frameworks/performance-pr-framework.md (+ extended digital footprint measurement (citability, AI-visibility, incoming requests, expert positioning) + cross-links to b2b-pr-influence-shift and pr-measurement-digital-footprint)
  - wiki/canon/marketing-frameworks/infopovod-criteria-smb-pr.md (+ trendwatching as pre-criterion (themes at intersection of trends, not internal news); link to b2b-pr-influence-shift-2026)
  - wiki/evolving/industry-trends/seo-to-pr-substitution-2026.md (+ B2B-specific framing: AI-visibility requires thematic-coherent expert footprint, not just trusted-site presence; journalist filter tightening as parallel signal)
  - wiki/evolving/industry-trends/native-pr-russia-2026.md (+ B2B-projection: 5 levers of B2B-PR restructuring (semantic architecture, trendwatching, analytical content, owned channels, collabs) as operational version of long-term DocsInBox/EMC forecast)
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md (+ AI-visibility-as-KPI B2B framing: thematic-coherent expert footprint required (not just Schema.org+llms.txt); new sub-KPI «AI-citability quality» (cited as expert vs cited as mention))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_b2b-piar-posle-epohi-prostyh-ohvatov-vebinar_e971cf79.md (+ .note.md + .triage.json sidecars)

## [2026-05-18 21:32] [ingest] | Pressfeed/PRAGMATIX: AI меняет правила поиска — данные важнее лендинга (product-data-as-architecture + agentic commerce L2-L3)
- source: wiki/sources/2026-05-18-pressfeed-pragmatix-ai-data-over-landing.md
- created:
  - wiki/canon/marketing-frameworks/product-data-as-architecture-pragmatix.md
  - wiki/evolving/industry-trends/ai-search-product-discovery-layer-2026.md
  - wiki/evolving-strict/market-data/ai-search-commerce-benchmarks-2026.md
  - wiki/volatile-strict/industry-news/yandex-alice-find-cheaper-agent-2026-05.md
  - wiki/volatile-strict/industry-news/openai-stripe-chatgpt-checkout-2026-05.md
  - wiki/volatile-strict/industry-news/sap-joule-tender-analysis-agent-2026.md
- updated:
  - wiki/evolving/industry-trends/agentic-commerce-stripe-2026.md
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md
  - wiki/evolving/content-trends/aeo-geo-llm-search-optimization-2026.md
  - wiki/canon/marketing-frameworks/seo-for-ai-era-playbook.md
  - wiki/evolving/industry-trends/ecommerce-trust-decision-shift-ru-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 3, evolving-strict: 1, volatile-strict: 3, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_ai-menyaet-pravila-poiska-teper-vse-reshayut-dannye-a-ne-len_977d7e2e.md

## [2026-05-18 21:44] [ingest] | Pressfeed — Анна Тарасова: «Бренд завода как невидимая сила, начинающая приносить реальные деньги» (industrial-B2B brand framework + proof-driven content pattern)
- source: wiki/sources/2026-05-18-pressfeed-tarasova-zavod-brand.md
- created:
  - wiki/canon/marketing-frameworks/industrial-b2b-brand-framework-tarasova.md
  - wiki/evolving/content-trends/proof-driven-b2b-content-pattern.md
- updated:
  - wiki/canon/marketing-frameworks/b2b-services-client-maturity-funnel.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_brend-zavoda-kak-nevidimaya-sila-nachinaet-prinosit-realnye-_a60f72ac.md

## [2026-05-18 21:46] [ingest] | Pressfeed: чат-боты в e-commerce — когда нужны и точно окупятся (ROI-рамка Юлии Евсеевой)
- source: wiki/sources/2026-05-19-pressfeed-chatbot-roi-framework-evseeva.md
- created:
  - wiki/canon/marketing-frameworks/chatbot-roi-4-economic-effects.md
  - wiki/canon/marketing-frameworks/chatbot-readiness-checklist.md
  - wiki/canon/marketing-frameworks/chatbot-vendor-selection-criteria.md
- updated:
  - wiki/canon/marketing-frameworks/llm-bot-customer-tolerance-gorny-frame.md
  - wiki/canon/marketing-frameworks/ai-smb-pilot-three-traps.md
  - wiki/canon/marketing-frameworks/cpa-calculator-pre-launch-roi.md
  - wiki/canon/marketing-frameworks/automation-vs-digital-transformation-framework.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 7, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_chat-boty-v-elektronnoj-kommerczii-kogda-oni-realno-nuzhny-i_687abc04.md

## [2026-05-18 21:30] [ingest] | Pressfeed/Insight Analytics (Кравченко): object-oriented retrieval, Faire +40% AI-Overviews, GEO-monitoring discipline, architectural shift
- source: wiki/sources/2026-05-18-pressfeed-kravchenko-insight-analytics-structured-data.md
- created:
  - wiki/canon/marketing-frameworks/object-oriented-retrieval-kravchenko.md
  - wiki/canon/marketing-frameworks/geo-monitoring-discipline-2026.md
- updated:
  - wiki/evolving/content-trends/aeo-geo-llm-search-optimization-2026.md (+Кравченко-update: object-oriented retrieval, Faire +40% AI-Overviews case, booking +15%/+30%, inventory accuracy, JSON-LD приоритет, GEO-мониторинг discipline, architectural shift, готовый slogan)
  - wiki/canon/marketing-frameworks/seo-for-ai-era-playbook.md (+Микроразметка extended (Product/Offer/Brand/Person); +JSON-LD priority calibration; +Архитектурный сдвиг capex vs opex table; +Inventory accuracy section; +ссылки на object-oriented retrieval и GEO-monitoring discipline)
  - wiki/evolving/content-trends/geo-playbook-2026-q2.md (+Update 2026-05-18 Кравченко: механика II расширена (Faire case +40% AI-Overviews + расширение Schema до Product/Offer/Brand), механика VI расширена до GEO-monitoring discipline; +inventory accuracy + 2 новых пункта в operational checklist)
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md (+Update 2026-05-18 Кравченко: object-oriented retrieval, Faire +40% benchmark, inventory accuracy, architectural shift (capex vs opex), GEO-monitoring discipline; +готовый slogan «видимость = интерпретация»)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_brendy-uhodyat-v-ten-algoritmov-pochemu-strukturirovannye-da_8acbddf9.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-18 22:00] [ingest] | Pressfeed/Язовский: GEO-оптимизация за 6 шагов + 3 RU SMB-кейса (Perplexity 24%/GigaChat 20% distribution, 9× рост 2025)
- source: wiki/sources/2026-05-18-pressfeed-yazovsky-geo-6-steps-smb.md
- created:
  - wiki/canon/marketing-frameworks/geo-smb-6-step-playbook-yazovsky.md
  - wiki/evolving-strict/campaign-metrics/geo-smb-case-benchmarks-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-ai-search-traffic-share-2026.md (+Язовский distribution AI-traffic Perplexity 24%/GigaChat 20% (первый RU-замер по источникам); +9× рост RU AI-traffic 2025; +35% RU users use AI for fact search; +12-18% Яндекс CTR падение коммерции; +кросс-ссылки на SMB-плейбук и benchmarks)
  - wiki/evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026.md (+Update Язовский SMB-уровень: 8й practitioner-голос дополняет corporate 13-кейсов; подтверждение 7 паттернов RU consensus + уникальный SMB-угол (self-audit, 6 шагов, 3 SMB-кейса); рекомендация микса для GRO (SMB diagnostics + corporate PR))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving-strict: 1, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_dlya-kakogo-biznesa-kritichna-geo-optimizacziya-i-kak-ee-nac_07edc3f0.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-18 22:21] [ingest] | Pressfeed — Интенсивы по нейросетям: можно ли быстро освоить AI и начать применять (RU-landscape + 5-критериев качества)
- source: wiki/sources/2026-05-18-pressfeed-ai-intensives-overview.md
- created:
  - wiki/canon/marketing-frameworks/ai-intensive-format-criteria.md
  - wiki/evolving/industry-trends/ru-ai-intensive-courses-landscape-2026.md
- updated:
  - wiki/canon/product-knowledge/gro-intensive.md
  - wiki/canon/target-audience/gro-segments.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_intensivy-po-nejrosetyam-mozhno-li-bystro-osvoit-ai-i-nachat_fa177dae.md

## [2026-05-18 22:22] [ingest] | Pressfeed: Главная страница b2b-сайта — гайд по основным блокам и правилам наполнения (LZ.Media, SEO-агентство Самара)
- source: wiki/sources/2026-05-18-pressfeed-b2b-homepage-blocks-guide.md
- created:
  - wiki/canon/marketing-frameworks/b2b-homepage-client-route-structure-lz-media.md
  - wiki/canon/marketing-frameworks/serp-driven-website-blocks-discovery.md
  - wiki/canon/marketing-frameworks/specificity-test-strip-company-name.md
  - wiki/canon/marketing-frameworks/about-us-block-anti-cliche-b2b.md
- updated:
  - wiki/canon/marketing-frameworks/tabunov-landing-anatomy.md
  - wiki/canon/marketing-frameworks/ai-text-markers-checklist.md
  - wiki/canon/marketing-frameworks/b2b-services-client-maturity-funnel.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 7, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_glavnaya-stranicza-b2b-sajta-gajd-po-osnovnym-blokam-i-pravi_55196fb6.md

## [2026-05-19 20:43] [ingest] | Pressfeed — Какие курсы по нейросетям подойдут новичку с нуля (paid-placement школы Барановой)
- source: wiki/sources/2026-05-19-pressfeed-kakie-kursy-novichku-baranova-placement.md
- created:
  - wiki/canon/marketing-frameworks/beginner-edu-3-differentiators.md
  - wiki/evolving/content-trends/pressfeed-paid-placement-ai-edu-pattern.md
- updated:
  - wiki/evolving/industry-trends/ru-ai-intensive-courses-landscape-2026.md
  - wiki/canon/marketing-frameworks/ai-intensive-format-criteria.md
  - wiki/canon/product-knowledge/gro-intensive.md
  - wiki/canon/target-audience/gro-segments.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kakie-kursy-po-nejrosetyam-podojdut-novichku-s-nulya-obzor-p_39197096.md

## [2026-05-19 20:45] [ingest] | Pressfeed/LZ.Media: Как ИИ влияет на контент-маркетинг — где помогает, где вредит (май 2026)
- source: wiki/sources/2026-05-19-pressfeed-lz-media-ai-content-marketing-limits.md
- created:
  - wiki/canon/marketing-frameworks/ai-content-marketing-delegation-frame-lz-media.md
  - wiki/evolving-strict/market-data/ai-content-transparency-demand-2026.md
- updated:
  - wiki/evolving/content-trends/ai-content-overload-trust-crisis-2026.md
  - wiki/evolving/content-trends/ai-text-detection-landscape-2026.md
  - wiki/evolving/industry-trends/ai-marketing-limits-2026.md
  - wiki/canon/marketing-frameworks/ai-text-markers-checklist.md
  - wiki/canon/marketing-frameworks/b2b-homepage-client-route-structure-lz-media.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-ii-vliyaet-na-kontent-marketing_264b00dc.md

## [2026-05-19 20:51] [ingest] | Pressfeed — Нейросеть для курсов: 15+ доступных в РФ сервисов (production stack для онлайн-обучения)
- source: wiki/sources/2026-05-19-pressfeed-ai-tools-for-online-courses-15.md
- created:
  - wiki/canon/marketing-frameworks/ai-course-production-conveyor-7-stages.md
  - wiki/evolving/content-trends/ru-ai-course-production-stack-2026.md
  - wiki/canon/marketing-frameworks/ai-content-3-limitations-pressfeed.md
- updated:
  - wiki/canon/marketing-frameworks/ai-intensive-format-criteria.md
  - wiki/evolving/industry-trends/ru-ai-intensive-courses-landscape-2026.md
  - wiki/canon/product-knowledge/gro-intensive.md
  - wiki/evolving/content-trends/ai-video-tools-stack-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-ispolzovat-nejroseti-dlya-sozdaniya-kursov-15-instrument_bbe7f0a1.md

## [2026-05-19 20:50] [ingest] | Pressfeed: личная эффективность руководителя — внимание как ограниченный управленческий ресурс (CEO-essay, параллельная рамка к Спиридонову)
- source: wiki/sources/2026-05-18-pressfeed-ceo-focus-essay.md
- created:
  - wiki/canon/marketing-frameworks/attention-as-managed-resource-pressfeed-ceo.md
  - wiki/evolving/content-trends/pressfeed-ceo-personal-effectiveness-essay-pattern-2026.md
- updated:
  - wiki/canon/marketing-frameworks/signal-noise-essentialism-spiridonov.md (+параллельная рамка Pressfeed-CEO «время vs внимание»: delta-таблица (управляемая единица, asymmetry, founder-bottleneck, strategy/ops, energy, biographic anchor, self-test, AI-era angle, attribution); двойной перевод как content-tool; cross-link в Связь и Связанные)
  - wiki/canon/marketing-frameworks/owner-strategist-operator-three-roles-separation.md (+Pressfeed-CEO как параллельная рамка founder-bottleneck (управление ресурсами vs разделение ролей); 2 cross-link в Связь со смежными и Cross-links; +sources update)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_lichnaya-effektivnost-rukovoditelya-pochemu-problema-ne-vo-v_95feadf4.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-19 20:55] [ingest] | Pressfeed/Гущина (PR Group): 6 правил нетворкинга — operational handbook на per-эпизод уровне (третья ось networking-кластера)
- source: wiki/sources/2026-05-19-pressfeed-guschina-networking-6-rules.md
- created:
  - wiki/canon/marketing-frameworks/networking-6-rules-guschina.md
- updated:
  - wiki/canon/marketing-frameworks/personal-brand-channels-5-types-magas.md (+операционализация Канала 4 (нетворкинг) через handbook Гущиной + cross-link на Воронина (mental model темпорального построения))
  - wiki/canon/marketing-frameworks/voronin-preventive-social-capital.md (+секция Operational handbook на per-эпизод уровне (Гущина дополняет Воронина: стратегия 5-10 лет + тактика 24 часов))
  - wiki/canon/marketing-frameworks/sales-follow-up-second-touch-fomichev.md (+секция Перенос на networking-контекст (Гущина: тот же принцип второго касания, окно 24ч, артефакт = фото/контекст))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-prevratit-znakomstva-v-soczialnyj-kapital-pravila-netvor_2a37739e.md (+ .note.md + .triage.json sidecars)

## [2026-05-19 21:00] [ingest] | Pressfeed: 10 признаков, что бизнесу нужен PR (диагностический чек-лист + sarafan-growth-ceiling pattern)
- source: wiki/sources/2026-05-19-pressfeed-pr-readiness-10-signals-checklist.md
- created:
  - wiki/canon/marketing-frameworks/pr-readiness-10-signals-checklist.md
  - wiki/canon/marketing-frameworks/sarafan-growth-ceiling-pattern.md
- updated:
  - wiki/canon/marketing-frameworks/b2b-pr-influence-shift-2026.md (+upstream-link на PR-readiness-чек-лист (gating-вопрос «пора ли?») и sarafan-growth-ceiling (root-cause); +источник в sources)
  - wiki/canon/marketing-frameworks/infopovod-criteria-smb-pr.md (+секция «когда применять» — критерии работают downstream от PR-readiness-чек-листа; +источник)
  - wiki/canon/marketing-frameworks/b2b-services-client-maturity-funnel.md (+связка стадий 3–5 воронки с PR-readiness-чек-листом; отсутствие публичного следа = выпадение из воронки на стадиях 4–5; +источник)
  - wiki/canon/marketing-frameworks/performance-pr-framework.md (+upstream-gating-links на pr-readiness-10-signals-checklist и sarafan-growth-ceiling-pattern в связанных страницах; +источник)
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+enrich-секция «Структурный триггер: потолок сарафана» — 4 fingerprint-симптома исчерпания personal-contacts-модели роста; ссылки на sarafan-growth-ceiling-pattern и pr-readiness-10-signals-checklist; +источник)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-ponyat-chto-vashemu-biznesu-uzhe-nuzhen-pr_c04b6721.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-19 21:05] [ingest] | Pressfeed/«В точку» — 5 методов таргета в сложных нишах (B2B/long-cycle playbook + benchmarks кейс застройщика Нижний Новгород)
- source: wiki/sources/2026-05-19-pressfeed-target-ads-construction-5-methods-vtochku.md
- created:
  - wiki/canon/marketing-frameworks/purchase-scenario-segmentation-vtochku.md
  - wiki/canon/marketing-frameworks/competitor-community-targeting-vtochku.md
  - wiki/canon/marketing-frameworks/three-tier-funnel-budget-split-vtochku.md
  - wiki/canon/marketing-frameworks/single-fear-utp-vtochku.md
  - wiki/canon/marketing-frameworks/hot-lead-share-kpi-vtochku.md
  - wiki/evolving-strict/campaign-metrics/long-cycle-niche-targeting-benchmarks-2026.md
- updated:
  - wiki/canon/marketing-frameworks/hyperseg-funnel-replication.md (+cross-link на purchase-scenario-segmentation-vtochku как pre-step (сценарии покупки как input для построения матрицы — превращает 50-60 произвольных связок в 6-18 содержательных); +source)
  - wiki/canon/marketing-frameworks/cpa-calculator-pre-launch-roi.md (+source-link на vtochku-playbook (hot-lead-share как корректировка верхней границы CPHL до запуска))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 7, evolving-strict: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-nastraivat-targetirovannuyu-reklamu-v-stroitelstve-i-dru_3ae90678.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-19 21:17] [ingest] | Pressfeed/LZ.Media: Как предпринимателю стать спикером — готовимся к первому выступлению (Cherednichenko 4-frame)
- source: wiki/sources/2026-05-19-pressfeed-lz-media-speaker-first-event-prep.md
- created:
  - wiki/canon/marketing-frameworks/speaker-event-type-selection-cherednichenko.md
  - wiki/canon/marketing-frameworks/speaker-marketing-kit-structure-cherednichenko.md
  - wiki/canon/marketing-frameworks/speaker-event-discovery-channels-cherednichenko.md
  - wiki/canon/marketing-frameworks/speaker-economics-reality-cherednichenko.md
- updated:
  - wiki/canon/marketing-frameworks/speaking-as-marketing-channel.md
  - wiki/evolving/content-trends/event-speaker-carousel-format.md
  - wiki/canon/marketing-frameworks/performance-pr-framework.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-predprinimatelyu-stat-spikerom-gotovimsya-k-pervomu-vyst_795ddf16.md

## [2026-05-19 21:27] [ingest] | Pressfeed/Стадлей: SEO-статьи для эксперта — кейс психолога (топ Яндекса по 3 запросам, b17.ru + Дзен)
- source: wiki/sources/2026-05-19-pressfeed-stadley-seo-articles-expert-case.md
- created:
  - wiki/canon/marketing-frameworks/seo-search-intent-content-method-stadley.md
  - wiki/canon/marketing-frameworks/expert-trust-platforms-leverage-method.md
  - wiki/canon/marketing-frameworks/seo-article-as-digital-asset-stadley.md
- updated:
  - wiki/evolving/content-trends/ru-geo-aeo-practitioner-playbook-2026.md
  - wiki/evolving/industry-trends/seo-to-pr-substitution-2026.md
  - wiki/canon/marketing-frameworks/seo-for-ai-era-playbook.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 2, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-psiholog-i-biznes-kouch-vyshla-v-top-poiska-s-pomoshhyu-_7b98ebc5.md

## [2026-05-19 21:35] [ingest] | Pressfeed/«В точку» — Как продвигать услугу, которой не доверяют: 4 метода SMM для сложных ниш (кейс доставки авто)
- source: wiki/sources/2026-05-19-pressfeed-distrust-niche-smm-4-methods-vtochku.md
- created:
  - wiki/canon/marketing-frameworks/distrust-niche-smm-playbook-vtochku.md
  - wiki/canon/marketing-frameworks/customer-fears-as-content-pillar.md
  - wiki/canon/marketing-frameworks/customer-photos-with-metrics-ugc.md
  - wiki/canon/marketing-frameworks/filter-not-list-comparison-format.md
  - wiki/canon/marketing-frameworks/a4-content-strategy-doc.md
  - wiki/canon/marketing-frameworks/pre-approved-content-formats.md
  - wiki/evolving/content-trends/short-form-engagement-vtochku-case-2026.md
  - wiki/evolving-strict/campaign-metrics/distrust-niche-smm-vtochku-benchmarks.md
- updated:
  - wiki/canon/marketing-frameworks/single-fear-utp-vtochku.md
  - wiki/evolving/content-trends/smm-strategy-trends-2026.md
  - wiki/canon/marketing-frameworks/chatbot-roi-4-economic-effects.md
  - wiki/canon/marketing-frameworks/purchase-scenario-segmentation-vtochku.md
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving: 1, evolving-strict: 1, sources: 1}
- touched: 13 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-prodvigat-uslugu-kotoroj-ne-doveryayut-4-metoda-smm-dlya_26555a1c.md

## [2026-05-19 21:35] [ingest] | Pressfeed/Ковпак: как выжимать продажи из локальных медиа и блог-платформ — рабочие связки
- source: wiki/sources/2026-05-19-pressfeed-kovpak-local-media-sales-funnel.md
- created:
  - wiki/canon/marketing-frameworks/local-media-sales-funnel-kovpak.md
  - wiki/canon/marketing-frameworks/native-90-10-ratio-moderated-platforms.md
  - wiki/canon/marketing-frameworks/exclusive-data-for-journalists-free-placement.md
  - wiki/evolving-strict/campaign-metrics/local-media-cpl-benchmarks-2026.md
  - wiki/evolving/industry-trends/local-media-overheated-paid-shift-2026.md
- updated:
  - wiki/canon/marketing-frameworks/native-advertising.md
  - wiki/canon/marketing-frameworks/performance-pr-framework.md
  - wiki/evolving/industry-trends/native-pr-russia-2026.md
  - wiki/canon/marketing-frameworks/seo-for-ai-era-playbook.md
  - wiki/evolving-strict/campaign-metrics/pressfeed-pr-cases-2026.md
  - wiki/canon/marketing-frameworks/petrochenkov-2026-q2-channel-priority.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 8, evolving: 2, evolving-strict: 2, sources: 1}
- touched: 11 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-vyzhimat-prodazhi-iz-lokalnyh-media-i-blog-platform-rabo_ee156186.md

## [2026-05-19 21:46] [ingest] | Pressfeed/Тарасова: «Компас в бурю — зачем современному заводу точная маркетинговая стратегия» (industrial B2B)
- source: wiki/sources/2026-05-20-pressfeed-tarasova-kompas-zavod-strategy.md
- created:
  - wiki/canon/marketing-frameworks/industrial-b2b-no-strategy-degradation-tarasova.md
  - wiki/evolving/industry-trends/industrial-marketing-strategy-as-survival-condition-2026.md
- updated:
  - wiki/canon/marketing-frameworks/industrial-b2b-brand-framework-tarasova.md
  - wiki/evolving/content-trends/proof-driven-b2b-content-pattern.md
  - wiki/canon/marketing-frameworks/b2b-services-client-maturity-funnel.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kompas-v-buryu-zachem-sovremennomu-zavodu-tochnaya-marketing_5eff4af5.md

## [2026-05-19 21:47] [ingest] | Pressfeed: Канал «ВКонтакте» — как создать и вести, что публиковать (VK channels playbook)
- source: wiki/sources/2026-05-19-pressfeed-vk-channels-playbook.md
- created:
  - wiki/canon/marketing-frameworks/vk-channels-playbook-pressfeed.md
  - wiki/evolving/content-trends/vk-channels-brand-exemplars-2026.md
- updated:
  - wiki/canon/marketing-frameworks/personal-brand-channels-5-types-magas.md
  - wiki/canon/marketing-frameworks/vk-ads-2026-niche-playbook.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kanal-vkontakte-novaya-vozmozhnost-vovlech-auditoriyu-kak-eg_fbd8d132.md

## [2026-05-19 21:52] [ingest] | Pressfeed: Лучшие публикации за апрель 2026 (дайджест) — audit-only digest, no extractions
- source: wiki/sources/2026-05-19-pressfeed-luchshie-publikaczii-aprel-2026-digest.md
- created:
  - none
- updated:
  - none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 page
- raw: raw/processed/articles/web_news.pressfeed.ru_luchshie-publikaczii-za-aprel-2026-go_ede4b1fa.md

## [2026-05-19 21:53] [ingest] | Pressfeed: Что такое медиамониторинг и как он стал базовым навыком в PR (СКАН-Интерфакс кейсы)
- source: wiki/sources/2026-05-19-pressfeed-mediamonitoring-pr-base-skill.md
- created:
  - wiki/canon/marketing-frameworks/media-monitoring-pr-framework.md
  - wiki/evolving/industry-trends/pr-competence-shift-2026.md
- updated:
  - wiki/canon/marketing-frameworks/pr-measurement-digital-footprint.md
  - wiki/canon/marketing-frameworks/b2b-pr-influence-shift-2026.md
  - wiki/canon/marketing-frameworks/crisis-pr-principles.md
  - wiki/canon/marketing-frameworks/performance-pr-framework.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-mediamonitoring-stal-bazovym-navykom-pr-speczialista_8c198d47.md

## [2026-05-19 22:01] [ingest] | Pressfeed: Мониторинг СМИ как инструмент прогнозирования, а не отчётности (weak-signals + Byju collapse case)
- source: wiki/sources/2026-05-19-pressfeed-mediamonitoring-prognozirovanie-weak-signals.md
- created:
  - wiki/canon/marketing-frameworks/weak-signals-crisis-3-stages.md
  - wiki/canon/marketing-frameworks/convenient-blame-association-pattern.md
  - wiki/canon-strict/historical-campaigns/byju-reputation-collapse-case.md
- updated:
  - wiki/canon/marketing-frameworks/crisis-pr-principles.md
  - wiki/canon/marketing-frameworks/black-pr-community-doubt-mechanic.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, canon-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_monitoring-smi-kak-instrument-prognozirovaniya-a-ne-otchetno_e82e4a9d.md

## [2026-05-19 22:01] [ingest] | Pressfeed/PR DOCTOR: маркетинг, пиар и продажи в погоне за лидами (3-dept conflict frame + event-coordination + GTM anchor + CMO-парадокс)
- source: wiki/sources/2026-05-19-pressfeed-prdoctor-marketing-pr-sales-conflict.md
- created:
  - wiki/canon/marketing-frameworks/three-dept-conflict-prdoctor.md
  - wiki/canon/marketing-frameworks/event-coordination-checklist-prdoctor.md
  - wiki/canon/marketing-frameworks/gtm-shared-understanding-anchor.md
  - wiki/evolving-strict/market-data/cmo-strategist-executor-gap-2026.md
- updated:
  - wiki/canon/marketing-frameworks/marketing-sales-alignment-framework.md (+PR DOCTOR 3-departmental extension note во вводной части (рамка неполна для организаций с PR-отделом); +cross-ref на CMO-парадокс 84%/64%; +5 новых links в Связанных страницах)
  - wiki/canon/marketing-frameworks/b2b-pr-influence-shift-2026.md (+organizational frame section: PR не standalone функция, а часть 3-dept системы; mapping 3 PR DOCTOR-рычагов на смысловую архитектуру/sales-ownership/system-KPI; production-executive anti-pattern; +cross-ref CMO-парадокс)
  - wiki/canon/marketing-frameworks/refused-customer-interview.md (+Feedback Loop (Рычаг 3 marketing-sales-alignment) как scalable proxy для refused-customer interview: интервью для глубины, CRM-feedback для покрытия объёма, комплементарно)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_marketing-piar-i-prodazhi-kto-glavnyj-v-pogone-za-lidami_367c52fa.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-20 00:36] [ingest] | Pressfeed: анонс вебинара «Как продвигаться, когда всё отключено» (Кузнецова, Академия Pressfeed) — irrelevant audit-only
- source: wiki/sources/2026-05-19-pressfeed-kak-prodvigatsya-kogda-vsyo-otklyucheno-vebinar.md
- created:
  - none
- updated:
  - none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 page
- raw: raw/processed/articles/web_news.pressfeed.ru_kak-prodvigatsya-kogda-vsyo-otklyucheno-vebinar_5d3e4263.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-19 12:50] [ingest] | Telegram @gurinovich_shares 917–919 (14–18 мая 2026) — Новак-growth, быстрый контент, AI-производительность [bundle: +2 видео, transcript pending]
- source: wiki/sources/2026-05-19-tg-gurinovich-shares-may-14-18-2026.md
- created:
  - wiki/evolving/content-trends/fast-content-consumption-shift-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-macro-snapshot-may-2026.md
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 1, evolving-strict: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_gurinovich_shares_20260519-124008.md + 2 video children (918, 919)

## [2026-05-22 20:25] [ingest] | Telegram @gro_me — посты 379–389 (14–19 мая 2026): Чмух «личный бренд vs репутация», карусель рефрейминга, расширение ICP, герой Гудимова
- source: wiki/sources/2026-05-19-tg-gro-me-379-389.md
- created:
  - wiki/canon/marketing-frameworks/personal-brand-vs-reputation-chmukh.md
  - wiki/evolving/content-trends/news-reframing-carousel-gro.md
- updated:
  - wiki/evolving/product-reception/gro-channel-content-history.md (+раздел «Май 2026 (вторая половина), посты 379–389»; +Арка 6 (расширение ICP вниз + контент=демонстрация продукта); Чмух в Арке 5.)
  - wiki/evolving/content-trends/gro-content-rubrics-system.md (+Чмух в гостевые эксперты #отпервоголица; +Гудимова/Bionova в Герои GRO; +секция про карусель «Рефрейминг новостей» (#помесим).)
  - wiki/canon/brand-guidelines/gro-channel-tone-of-voice.md (+цитаты «элегантная публичность» и про планку предпринимательства; +Чмух в гостевой пул; +секция расширения ICP (пост 388); +секция #людидела/Гудимова.)
  - wiki/evolving/industry-trends/blue-collar-ai-resilience-2026.md (+секция «GRO операционализировал тренд в контенте» (reframe-карточка «синие воротнички», пост 384) как подтверждённый кейс.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 4, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_gro_me_20260519-170005.md + 10 children (media/tg_gro_me_{379,381-389}.jpg)

## [2026-05-19 09:50] [ingest] | Telegram @hh_ru_official — 16 постов 15–18 мая 2026 (HeadHunter Q1 2026 финрезультаты + зарплатный рост по профессиям)
- source: wiki/sources/2026-05-19-tg-hh-ru-official-may-15-18-2026.md
- created:
  - wiki/evolving-strict/competitor-metrics/headhunter-group-q1-2026.md
  - wiki/evolving-strict/market-data/ru-salary-growth-by-profession-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-hrtech-market-2023-2025.md
  - wiki/evolving-strict/market-data/ru-labor-market-q1-2026.md
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md
  - wiki/evolving/content-trends/hh-ru-blog-content-patterns.md
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 4, evolving: 3, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_hh_ru_official_20260519-095003.md

## [2026-05-22 20:30] [ingest] | Telegram @howtomake10x (Крылов) 18–19 мая 2026 — loyal-core retention-инсайт «Азбуки вкуса» (6,2%→36%) + вебинар Mindbox/SKMS (bundle: 1 article + 2 media)
- source: wiki/sources/2026-05-19-tg-howtomake10x-1571-1572.md
- created:
  - wiki/evolving-strict/market-data/azbuka-vkusa-loyal-core-revenue-2026.md
  - wiki/volatile-strict/industry-news/mindbox-skms-retention-webinar-2026-05.md
- updated:
  - wiki/canon/marketing-frameworks/retention-benchmarks-b2c.md (+секция loyal-core revenue-concentration (комплементарный B2C-retention-срез: ~6% базы держат ~⅓ выручки, переток в ядро = leading-indicator, selective retention); +5 cross-links; +source)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving-strict: 1, volatile-strict: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_howtomake10x_20260519-132001.md + 2 children (raw/processed/media/tg_howtomake10x_1571.jpg, tg_howtomake10x_1572.jpg)

## [2026-05-22 01:45] [ingest] | Telegram @hutzp — 16 сообщений (3528–3543, 14–19 мая 2026): intellectual-club event-format + SETTERS EDUCATION + Creator-leadership фреймворк + recruitment-as-content
- source: wiki/sources/2026-05-19-tg-hutzp-may-14-19-2026.md
- created:
  - wiki/evolving/content-trends/founder-intellectual-club-event-format.md
  - wiki/canon/marketing-frameworks/creator-leadership-paradigm-shift.md
- updated:
  - wiki/evolving/competitor-positioning/settersgroup-ecosystem.md (+SETTERS EDUCATION как 5-я единица экосистемы (курс «Креативное лидерство» B2C + B2B corp-edu + суб-бренд найма A-Teams by SM); +операционная анатомия интеллектуального клуба изионистов (Бобков/Багаутдинов, T-Бизнес co-sponsor))
  - wiki/evolving/content-trends/telegram-author-channel-patterns.md (+sub-pattern «recruitment-as-content» (3537, вакансия как brand-post в фирменном визуале A-Teams by SM); +подтверждение устойчивости ритуала «Цитата недели» через 5+ недель (3538 Соррентино))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, canon: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_hutzp_20260519-125006.md + 16 children → status: processed

## [2026-05-19 10:26] [ingest] | Telegram @incrussiamedia — дайджест 11–17 мая 2026 (RU ИИ-видимость брендов, distinctive brand assets, потреб-терроризм маркетплейсов, research-4-questions)
- source: wiki/sources/2026-05-19-tg-incrussiamedia-may-11-17-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-ai-visibility-index-banks-2026.md
  - wiki/canon/marketing-frameworks/distinctive-brand-asset-cases.md
  - wiki/canon/marketing-frameworks/consumer-terrorism-marketplace-defense.md
  - wiki/canon/marketing-frameworks/research-need-4-questions-pre-start.md
- updated:
  - wiki/evolving/content-trends/aeo-geo-llm-search-optimization-2026.md
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md
  - wiki/evolving-strict/market-data/ru-business-ai-adoption-2026.md
- superseded:
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, evolving-strict: 2, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_incrussiamedia_20260519-102655.md

## [2026-05-22 02:00] [ingest] | Telegram @kwork_kwork — пост 566 (2026-05-19) «Цифровой порядок фрилансера»: новый digital-order productivity content-vector для Сегмента 3 + подтверждение бренд-канального ритма
- source: wiki/sources/2026-05-19-tg-kwork-566-digital-order-freelancer.md
- created:
  - wiki/evolving/content-trends/digital-organization-freelancer-hooks.md
- updated:
  - wiki/evolving/content-trends/marketplace-content-driven-category-dev.md (+пост 566 как 5-я точка наблюдаемой последовательности (supply-side digital-order content-vector, не категориальный шаг); уточнение buyer-shift гипотезы (565 не получил продолжения → ослабление); editorial-ритм 565→566 = 7 дней без дрейфа; +cross-link на digital-organization-freelancer-hooks)
  - wiki/evolving/content-trends/freelancer-growth-narrative-hooks.md (+cross-link на digital-organization-freelancer-hooks как параллельный content-угол для той же фрилансер-аудитории)
  - wiki/evolving/product-reception/gro-productivity-energy-angle.md (+cross-link на digital-organization-freelancer-hooks как смежную operational/space productivity-ось (другой вход в ту же ценность))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_kwork_kwork_20260519-100001.md + 1 child (raw/processed/media/tg_kwork_kwork_566.jpg)

## [2026-05-22 01:58] [ingest] | Telegram @kommersant — bundle 50 постов + 19 медиа за 6 мая 2026 (преим. нерелевантный новостной дайджест; 3 релевантных кластера: облачный рынок РФ + AI в авторынке Avito + автокредиты)
- source: wiki/sources/2026-05-19-tg-kommersant-20260519-110036.md
- created:
  - wiki/evolving-strict/market-data/ru-cloud-datacenter-regional-2026.md
  - wiki/evolving/industry-trends/ai-automotive-marketplace-avito-2026.md
  - wiki/evolving-strict/market-data/ru-auto-credit-q2-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-macro-snapshot-may-2026.md (+second-source corroboration от «Ъ» (6 мая): недельная дефляция 0,02% (28.04–04.05), годовая инфляция 5,6%, нефтегаз +40% MoM >855 млрд ₽; +2 cross-link (autocredit, cloud); +source)
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (+second-source corroboration vector 15 (mobile-internet shutdown): «Ъ» пост 106810 — Билайн/МегаФон/Т2 предупредили о перебоях перед 9 мая, рассылка повторная (4 мая), отключение уже было 5 мая до 12:00 → серия отключений, усиливает structural-pattern тезис; +source)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 3, evolving: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_kommersant_20260519-110036.md + 19 children (18 media + 1 video) → status: processed

## [2026-05-22 20:30] [ingest] | @moibiz (Минэк/Нацагентство «Мой бизнес») — 22 поста 14–19 мая 2026 (Минэк×Сбер «новая норма», AI-инфраструктура, креативный код)
- source: wiki/sources/2026-05-19-tg-moibiz-may-14-19-2026.md
- created:
  - wiki/evolving-strict/market-data/ru-entrepreneurship-as-norm-minec-sber-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-business-ai-adoption-2026.md (+§8: consumer AI spend РФ ~10% ежемесячно + «AI для бизнеса стала инфраструктурой» (@moibiz дайджесты 7543/7555) + cross-table row)
  - wiki/evolving-strict/market-data/ru-creative-industries-public-perception-2026.md (+рост креативных компаний/ИП +46% за 3 года + анонс нацпрограммы «Креативный код. Россия» (Авито генпартнёр, ТАСС))
  - wiki/evolving/industry-trends/ru-smb-trends-corpmsp-2025.md (тренд 2: третье подтверждение «предпринимательство как новая норма» (Минэк×Сбер 38%/51%) — массовизация, не только молодёжь)
  - wiki/canon/target-audience/gro-segments.md (+«совмещающие» (51%) как сегмент-мост между Сегментами 1 и 2 + мотивационный профиль запуска (Минэк×Сбер))
  - wiki/evolving-strict/market-data/ru-youth-entrepreneurs-2026.md (+cross-ref на мотивационно-поведенческий срез той же когорты (Минэк×Сбер))
  - wiki/evolving-strict/market-data/ru-self-employed-segments-2026.md (+cross-ref на поведенческий контекст соло-режима (42% без сотрудников, Минэк×Сбер))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 5, evolving: 1, canon: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_moibiz_20260519-111502.md + 16 children (media/jpg) → processed

## [2026-05-22 21:10] [ingest] | Telegram @neuraldvig — 4-й срез 50 постов + 50 медиа за 2026-05-13..19 (промт-доля рекорд 18%, anti-hallucination 2-я ось honesty-промтов, OpenRouter RU-блок, недельная AI-news сводка)
- source: wiki/sources/2026-05-19-tg-neuraldvig-may-13-19-2026.md
- created:
  - wiki/volatile/weekly-digest/ai-news-digest-2026-05-13-19.md
- updated:
  - wiki/evolving/content-trends/ai-news-channel-prompt-packs.md (+4-й срез @neuraldvig (10683..10732): 9/50=18% feed-доля (рекорд, выше коридора 10-12%, держим как medium-confidence единичный пик); +таблица 9 образцов; +image-generation промты как новый подтип (10683 Midjourney, 10721 ГигаЧат LEGO — редкий RU-вендорный); +anti-hallucination 10710 как вторая ось honesty-промтов; +Lyra meta-prompt 10706; XML-структура закрепляется (10726 русскоязычный); +source)
  - wiki/evolving/content-trends/anti-flattery-prompt-canon-2026.md (+вторая ось honesty-контрактов: anti-hallucination промт 10710 (русскоязычный, «не выдумывай, помечай [Не проверено]») рядом с anti-flattery 10639; +таблица двух осей; +импликация для GRO (honesty by design по обеим осям: не льстит и не выдумывает); +tag anti-hallucination; +source)
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (+расширение 15-го вектора: OpenRouter (агрегатор LLM-API) блокирует RU-доступ к американским моделям + режет пополнение (@neuraldvig 10711) — сужение доступа смещается с прямого вендора на инфраструктурного посредника, закрывает обходной путь; +source)
  - wiki/evolving/content-trends/telegram-native-formats.md (+4-й дамп @neuraldvig (2026-05-13..19): промт-доля 18% (выше коридора), ad-плотность ~10% (рекорд за 4 среза, банковские erid: Сбер ×2/Альфа/оператор/Зерокодер), усиление AI-tools-radar роли (4 анонса инструментов за неделю → рубрика-кандидат «AI-инструмент недели» для GRO); +2 source (3-й и 4-й срезы))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, volatile: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_neuraldvig_20260519-135724.md + 50 children (32 media jpg + 18 video mp4) -> status: processed

## [2026-05-19 16:30] [ingest] | Telegram @olegcloser — 14–19 мая 2026 (bundle: 18 дыр PDF + open live + Закрыватель re-promo)
- source: wiki/sources/2026-05-19-tg-olegcloser-may-14-19-2026.md
- created:
  - wiki/sources/2026-05-19-olegcloser-18-holes-checklist-pdf.md
  - wiki/canon/marketing-frameworks/sales-system-18-holes-shevelev.md
- updated:
  - wiki/canon/marketing-frameworks/business-reality-show-format.md (+content-payload summary asset (PDF «18 дыр» как 2-й слой re-purposing finale-видео) + документированная механика open live (100/100 мест, 5 новых бизнесов, live-чат как social proof) + 2 source/cross-links)
  - wiki/evolving/competitor-positioning/zakryvatel-sdelok-ai-agent.md (+раздел re-promo пост-cohort (пост 2305): symptom-driven hook, role-expansion предприниматель→РОП→менеджер, anti-ChatGPT differentiator, 400+ бизнесов, бесплатная экскурсия funnel, старт ПРОКАЧКИ 27 мая)
  - wiki/evolving/content-trends/sales-ai-narrative-hooks-2026.md (+cycle-4 hooks (пост 2305): symptom-first «зависшие клиенты = первый симптом», anti-ChatGPT differentiator, role-expansion «должно быть у каждого: X/Y/Z»)
  - wiki/canon/marketing-frameworks/sales-100-formula-shevelev.md (+cross-link на новый 18-holes фреймворк (формула 100% = решение дыры №5) + новый source)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 2, sources: 2}
- touched: 7 pages
- raw: raw/processed/articles/tg_olegcloser_20260519-123519.md + 6 children (1 pdf, 2 video, 3 media) → processed/. Видео 2302/2303 без транскрипта (whisper quota 429) — кандидаты на --enrich позже.

## [2026-05-22 02:05] [ingest] | Telegram @mspiridonov — 11 постов 14–19 мая 2026 (Just AI distribution kit, Think Week, diagnostic-prompt, Figure AI livestream) [bundle: primary + 7 children]
- source: wiki/sources/2026-05-19-tg-mspiridonov-may-14-19-2026.md
- created:
  - wiki/canon/marketing-frameworks/poc-first-enterprise-adoption-just-ai.md
  - wiki/canon/marketing-frameworks/think-week-structured-reading-gates.md
  - wiki/evolving/content-trends/self-diagnosing-prompt-lead-magnet-2026.md
- updated:
  - wiki/evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026.md (+Just AI open distribution kit (on-prem, free-month, 3-й трекаемый advertorial, erid 2VtzqwqNSUw); two-track GTM (Cloud SMB vs on-prem enterprise); усиление advertorial-frequency signal.)
  - wiki/evolving/industry-trends/humanoid-robot-narrative-shift-2026.md (+Cross-source того же Figure AI livestream (@mspiridonov 4410): PR/маркетинговый угол (viral livestream как anti-skeptic proof-of-capability, ~3 сек/посылка), reconcile с breakingtrends performance-данными.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 3, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_mspiridonov_20260519-122127.md + 7 children (6 media jpg, 1 video mp4) → processed/. Видео 4410: транскрипт НЕ получен (whisper 429 insufficient_quota); .audio.mp3 сохранён рядом; подлежит wiki-ingest --enrich при восстановлении квоты.

## [2026-05-22 02:13] [ingest] | TG @peregudov — 4 поста 15 мая 2026 (441–444): PR/бренд как драйвер exit-стоимости (3 экзита) + observational content-hook «скрытое мастерство» (bundled: 1 silent mp4 + 1 jpg)
- source: wiki/sources/2026-05-19-tg-peregudov-may-15-2026.md
- created:
  - wiki/canon/marketing-frameworks/pr-as-exit-value-driver-peregudov.md
  - wiki/evolving/content-trends/hidden-mastery-observation-hook.md
- updated:
  - wiki/canon/marketing-frameworks/b2b-pr-influence-shift-2026.md (+Practitioner-свидетельство Рычага 3 (system-level Revenue KPIs): Перегудов с 3 экзитами формулирует exit-стоимость как верхний рубеж бизнес-результата PR; смещение аудитории PR с клиентов на инвесторов/покупателей; +source, +2 cross-links)
  - wiki/canon/marketing-frameworks/narrative-as-brand-currency.md (+cross-links на hidden-mastery-observation-hook (конкретная narrative-форма) и pr-as-exit-value-driver-peregudov (операционализация метрики «притяжение ресурсов» до инвесторов/покупателей); +source)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_peregudov_20260519-134600.md + 2 children (video/tg_peregudov_442.mp4 silent-no-audio, media/tg_peregudov_443.jpg) → processed

## [2026-05-22 02:14] [ingest] | Telegram: @petrochenkow — 2026-05-19 11:25 UTC (увольнения 2026 + AI-usability-тест через аватары) [bundle: primary + 2 media children]
- source: wiki/sources/2026-05-19-tg-petrochenkow-20260519-112501.md
- created:
  - wiki/canon/marketing-frameworks/ai-persona-usability-test-petrochenkov.md
  - wiki/evolving/content-trends/ai-synthetic-usability-test-hook-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md (+Петроченков как 6-й практик-голос на разворот рынка труда: +43% увольнений к апр-2026, кейс «-20% персонала через ИИ», K-образное расслоение (low-skill вымывает / high-skill дефицит), ценностный reframe «оздоровление, а не кризис».)
  - wiki/canon/marketing-frameworks/refused-customer-interview.md (+раздел «Синтетический pre-launch-прокси: AI-persona usability-тест (Петроченков)»: дешёвая pre-fact гипотеза дыр воронки до залива трафика, комплементарно к post-fact интервью с отказниками; рекомендуемая последовательность; cross-link.)
  - wiki/evolving/industry-trends/ai-marketing-limits-2026.md (+data-point «что ИИ делает хорошо»: синтетический usability-тест через AI-аватар совпадает с живыми респондентами до 80% (Петроченков 1301-1302); вписан в TL;DR «ИИ как дешёвый второй пилот для диагностики восприятия».)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 3, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_petrochenkow_20260519-112501.md + 2 children (media: tg_petrochenkow_1301.jpg шаблон-аватар, tg_petrochenkow_1302.jpg пример AI-вывода) → processed/. Bundle вручную: .bundle.json отсутствовал, дети резолвлены из _(attached:)_ маркеров.

## [2026-05-22 20:30] [ingest] | Telegram @opora_russia — дайджест 7191–7213 (14–19 мая 2026): VK Реклама deck + Форум МСП ПМЭФ + 3PL + Исламские рынки [bundle: primary + 12 children]
- source: wiki/sources/2026-05-19-tg-opora-russia-may-14-19.md
- created:
  - wiki/canon/marketing-frameworks/vk-reklama-official-campaign-guide-2026.md
  - wiki/evolving-strict/market-data/ru-3pl-logistics-outsourcing-2026.md
  - wiki/evolving/industry-trends/ru-msp-islamic-markets-pivot-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-generated-creatives-in-advertising.md (+VK Реклама AI Gen «Креативная студия» как второй платформенный сигнал; таблица 2 подтверждённых кейсов.)
  - wiki/canon/marketing-frameworks/vk-ads-2026-niche-playbook.md (+cross-ref на официальный vendor-канон VK Реклама; sources +deck.)
  - wiki/volatile-strict/industry-news/pmef-2026-program-announcement.md (+секция Форум МСП (3 июня): 5-блочная программа, тема «Креативный код экономики», пленар с Новаком.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, evolving-strict: 1, volatile-strict: 1, sources: 2}
- touched: 8 pages
- raw: raw/processed/articles/tg_opora_russia_20260519-110508.md + 12 children (11 media + 1 documents) → processed/

## [2026-05-22 20:30] [ingest] | Heavyweight bundle child: VK Реклама официальный deck (PDF 7201) — source-page
- source: wiki/sources/2026-05-19-vk-reklama-effective-campaigns-deck.md
- created:
  - none
- updated:
  - none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/documents/tg_opora_russia_7201.pdf → processed/

## [2026-05-22 02:18] [ingest] | Telegram @portnyaginlive — 3-й дамп (открытие Siberia на Бауманской: immersive-theater event + B2B-закупка), 15-19 мая 2026
- source: wiki/sources/2026-05-19-tg-portnyaginlive-20260519-122009.md
- created:
  - wiki/evolving/content-trends/immersive-theater-brand-launch-event.md
- updated:
  - wiki/evolving/content-trends/portnyagin-founder-channel-patterns.md (+3-й дамп: format #7 закрыл дугу teaser→execution (immersive launch); +13-й формат (B2B-закупка на consumer founder-канале, 11258); +раздел доп.наблюдений; +cross-links на immersive-theater и новый source)
  - wiki/evolving/content-trends/cultural-narrative-brand-storytelling.md (+cross-link на immersive-theater-brand-launch-event (физическая активация нарратива на open-event) + новый source)
  - wiki/evolving/content-trends/factory-tour-pro-day-event-format.md (+cross-link на immersive-theater (рациональное operational vs эмоциональное sensory immersion))
  - wiki/evolving/content-trends/extreme-pr-event-audience-segmentation.md (+cross-links на immersive-theater (механизм перевода аудитории) и factory-tour-pro-day)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_portnyaginlive_20260519-122009.md + 11 children (raw/processed/media/tg_portnyaginlive_11248..11258.jpg) + sidecars

## [2026-05-19 10:55] [ingest] | Telegram @rbc_news — 50 постов 6–7 мая 2026 (дайджест; search-distribution platform risk Яндекс vs финмаркетплейсы)
- source: wiki/sources/2026-05-19-tg-rbc-news-20260519-105509.md
- created:
  - wiki/evolving/industry-trends/ru-search-distribution-platform-risk-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
  - wiki/volatile/raw-notes/ru-platform-access-april-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, volatile: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/tg_rbc_news_20260519-105509.md

## [2026-05-22 02:30] [ingest] | Telegram @ProductsAndStartups (Байрам Аннаков) — 7 постов 15–19 мая 2026 (1749–1755): accountability premium, страхование AI-агентов, OOD adversarial-атаки, дистилляция Code w/ Claude 2026 [bundle]
- source: wiki/sources/2026-05-19-tg-products-and-startups-may-15-19-2026.md
- created:
  - wiki/evolving/industry-trends/ai-accountability-premium-2026.md
  - wiki/volatile-strict/competitor-news/elevenlabs-aiuc-agent-insurance-2026.md
  - wiki/canon/marketing-frameworks/ai-agent-architectural-guardrails-2026.md
  - wiki/evolving/industry-trends/code-with-claude-2026-frameworks.md
  - wiki/evolving/content-trends/ai-augmented-content-consumption-pipeline-2026.md
- updated:
  - wiki/canon/marketing-frameworks/ceo-cto-ai-adoption-bridge.md (+Шаг 3.5 (accountability-ось поверх верификации) из поста 1750 «Заметки с полей - 2»; +cross-links на accountability-premium и guardrails; +источник 1750.)
  - wiki/evolving/industry-trends/ai-value-migration-2026.md (+cross-source confirmation direction #3 (верификация→accountability) от Аннакова + рыночное доказательство (страховка AIUC); апгрейд тезиса от спорного к sedimented consensus; +источник 1750.)
  - wiki/canon/marketing-frameworks/harness-engineering-for-ai-agents.md (+Update 2026-05-18: Advisor pattern (Code w/ Claude 2026) как production-форма правила «7×Haiku» — Haiku-executor с Opus-advisor через tool call; +источник 1752.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, volatile-strict: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_ProductsAndStartups_20260519-133332.md + 7 children (1749-1755, media) → processed; видео 1752 transcript unavailable (whisper quota 429), покрыто текстом+OCR

## [2026-05-22 20:31] [ingest] | Telegram @recruiter_live — дамп 18-19 мая 2026 (5 постов, 4-й дамп): HH «единая карьерная история» + resume-SEO + сезонный «переход после бонусов» + книга-трансформация
- source: wiki/sources/2026-05-19-tg-recruiter-live-may-18-19-2026.md
- created:
  - none
- updated:
  - wiki/evolving/competitor-positioning/hh-ru-hrtech-platform.md (+секция «Единая карьерная история» + resume-SEO ранжирование (синхронизация блоков опыта между резюме; заголовок/summary/skills > переписывание опыта); прямое продолжение edit-history feature поста 4462)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (+Hook 32 «Перестаньте переписывать резюме под каждую вакансию» (HH единая карьерная история + resume-SEO) +Hook 33 «Окно перехода после бонусов» (сезонность финансисты/юристы) + книга-трансформация Бриджес)
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (+сезонный sub-pattern «переход после бонусов» (апрель→май, CFO ~40%/юристы ~15% ленты LinkedIn) в май-срез + timing-aware GRO-следствие)
  - wiki/evolving/industry-trends/skill-based-hiring-russia-2026.md (+candidate-side проявление навыкоцентричности: HH «единая карьерная история» + resume-SEO (целостность профиля + явный skills-набор > tactic-подгонка опыта))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_recruiter_live_20260519-091001.md + 3 children (media/4473,4474,4475.jpg) + sidecars

## [2026-05-22 02:31] [ingest] | Telegram @rff_channel — 14–18 мая 2026 (14 постов, ids 4417..4430): sponsored-ads Альфа-Банка, новый паттерн bank × cultural-institution co-branding (Альфа × Подписные)
- source: wiki/sources/2026-05-18-tg-rff-channel-may14-18-2026.md
- created:
  - wiki/evolving/content-trends/bank-cultural-institution-cobranding-2026.md
- updated:
  - wiki/evolving/content-trends/collectible-card-design-fintech.md (+второй RU-кейс cobranded-карты (Альфа 6 гравировок × Подписные) — валидирует прогноз о copy-paradigm; добавлены explicit limited-edition и theme-binding-дивергенция vs T-Bank; обновлена таблица сравнения банков.)
  - wiki/evolving/industry-trends/russian-cultural-code-branding-2026.md (+fintech арендует культурный код через heritage-институт (Альфа × Подписные) — частично закрывает gap «нет потребительских брендов с русским кодом, только культурно-туристический сегмент».)
  - wiki/evolving/content-trends/founder-channel-sponsored-ad-formats-2026.md (+Pattern 4: vertical-community-канал (HR/@rff_channel) как ad-площадка крупного рекламодателя (Альфа ×3 кампании/неделя), audience-overlap targeting «предприниматель + HR»; обновлена таблица сравнения паттернов.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_rff_channel_20260519-094602.md + 14 children (11 media jpg + 3 video mp4)

## [2026-05-22 20:30] [ingest] | Telegram @rb_ru (Russian Business) — дайджест 14–19 мая 2026, 27 постов (bundle: 1 статья + 23 jpg + 4 mp4); 5 релевантных извлечений из новостного дампа
- source: wiki/sources/2026-05-19-tg-rb-ru-may-14-19-2026.md
- created:
  - wiki/evolving/content-trends/brand-cancellation-response-playbook-2026.md
  - wiki/volatile-strict/industry-news/roscosmos-rocket-advertising-2026.md
  - wiki/volatile-strict/industry-news/sber-business-comms-platform-2027.md
- updated:
  - wiki/evolving/industry-trends/ai-narrative-second-phase-risk-pivot-2026.md (+Duolingo CEO walkback как 5-й независимый сигнал 2-й фазы и первый executive self-reversal (фон Ан публично откатил forced-AI mandate апр-2025 под давлением сотрудников/рынка))
  - wiki/evolving/content-trends/wtf-hr-ai-skeptic-hooks.md (+6-е hook-семейство «Duolingo-reversal» (executive self-reversal сильнее SalesForce-наблюдателя); 5→6 семейств)
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md (+раздел 5b: измеримый эффект VPN-ограничений на маркетплейсы (WB −10%, Ozon/Я.Маркет −3%, отрасль ~7 млрд ₽) — первый numeric proof collateral damage по резидентным RU-сервисам)
  - wiki/canon/marketing-frameworks/crisis-pr-principles.md (+поджанр «культура отмены» (cancel culture) с cross-ref на 2-сценарный playbook; специализация общей рамки под скорость соцсетевой отмены)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, volatile-strict: 2, canon: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_rb_ru_20260519-103520.md + 27 children (23 media/jpg + 4 video/mp4) → status: processed

## [2026-05-22 00:00] [ingest] | Telegram @solokumi пост 416 (Кумар Виас) — OpenClaw vs Hermes сравнение AI-агентов + cost-routing + reaction-gate content-формат
- source: wiki/sources/2026-05-19-tg-solokumi-416-openclaw-vs-hermes.md
- created:
  - wiki/evolving/competitor-positioning/openclaw-vs-hermes-agent-tools-2026.md
  - wiki/evolving/content-trends/ai-tool-comparison-reaction-gate-format.md
  - wiki/sources/2026-05-19-tg-solokumi-416-openclaw-vs-hermes.md
- updated:
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md (+раздел «DIY-agent commoditization» (Кумар Виас): OpenClaw vs Hermes как 6-й угол валидации тренда — bottom-up массовизация агент-конструкторов, self-learning память мейнстримится, cost-routing снижает capital-барьер; +2 cross-links; updated→2026-05-22.)
  - wiki/evolving/industry-trends/ai-agent-economy-2026.md (+§14 «Cost-routing как операционная переменная»: ClawRouters auto-route на дешёвую модель (-70-90% по словам автора, conf:low) + Hermes VPS $5/мес + OpenRouter 200+ моделей; model-routing как новый GTM-слой; +2 cross-links; updated→2026-05-22.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_solokumi_20260519-125500.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-22 14:51] [ingest] | Telegram @selfworkru — 8 постов 14–18 мая 2026 (ФЗ-168: 5 исключений для латиницы + платформенные преференции самозанятым ≥2,9%)
- source: wiki/sources/2026-05-19-tg-selfworkru-may-14-18-2026.md
- created:
  - wiki/volatile-strict/industry-news/ru-self-employed-platform-preferences-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-brand-russification-law-2026.md (+раздел «5 легальных исключений для латиницы» (товарные знаки Роспатента 6-12 мес; фирменные наименования ЕГРЮЛ; техтермины; наименования произведений/псевдонимы; фантазийные наименования) + 2 cross-links + source.)
  - wiki/canon/target-audience/gro-segments.md (+регуляторный попутный ветер Сегмента 3 (платформенные преференции ≥2,9%, ФЗ-168 исключения как фоновый сигнал) + source.)
  - wiki/evolving-strict/market-data/ru-self-employed-2025.md (+cross-link на платформенные преференции как сигнал регуляторного взросления формата самозанятости.)
  - wiki/volatile-strict/industry-news/ru-mediator-platforms-registry-2026-05.md (+cross-link на платформенные преференции самозанятым как следующий шаг платформенной регуляторики.)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 2, evolving: 1, canon: 1, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_selfworkru_20260519-100506.md + 8 children (1 video + 7 media)

## [2026-05-22 14:55] [ingest] | Telegram @forbesrussia — дайджест 7-8 мая 2026 (50 постов, 8 релевантных marketing-сигналов)
- source: wiki/sources/2026-05-19-tg-forbesrussia-20260519-104004.md
- created:
  - wiki/volatile-strict/competitor-news/adobe-acquires-semrush-2026-05.md
  - wiki/evolving/industry-trends/ai-tax-labor-erosion-2026.md
  - wiki/evolving-strict/market-data/ru-platform-employment-market-2026.md
  - wiki/evolving-strict/market-data/ru-middle-class-segments-2026.md
  - wiki/evolving/industry-trends/proptech-ai-housing-management-ru-2026.md
- updated:
  - wiki/evolving/content-trends/forbes-russia-native-ad-pattern-2026.md (Третье подтверждение шаблона: +4 кейса 7-8 мая (Кронунг/PropTech blogs-колонки, Alfa-Bank brandvoice про AI-агенты, форум «Движение» spetsproekt+erid); «Информационная поддержка» закрепилась как доминирующий disclaimer)
  - wiki/evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2.md (+FT-подтверждение Anthropic ~$1T primary raise летом 2026 (vs OpenAI $852B); закрывает primary/secondary разрыв в пользу повышения primary)
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (+объёмный якорь под расширение гиг-контура: ссылка на ru-platform-employment-market-2026 (38 млрд ₽, +56%, закон))
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1, volatile-strict: 1, evolving: 4, evolving-strict: 3}
- touched: 9 pages
- raw: raw/processed/articles/tg_forbesrussia_20260519-104004.md + 20 children (media) → processed

## [2026-05-22 20:30] [ingest] | Telegram @startupoftheday (Горный) — 8 постов 14–19 мая 2026 (5068–5075)
- source: wiki/sources/2026-05-22-tg-startupoftheday-may-14-19-2026.md
- created:
  - wiki/canon/marketing-frameworks/influencer-pyramid-mavrck-5-tiers.md
- updated:
  - wiki/evolving/industry-trends/influencer-marketplace-failure-paradox.md (Mavrck data-point: market-leader ($300M) = agency-tool, НЕ маркетплейс — structural confirmation гипотез через winners)
  - wiki/canon/marketing-frameworks/ugc-and-microinfluencers.md (cross-link на 5-уровневую пирамиду Mavrck, расширяющую таксономию вниз (адвокаты/рефералы/лоялисты))
  - wiki/evolving/industry-trends/ai-marketing-limits-2026.md (Omni semantic-layer лимит ($120M/$1.5B): AI-аналитика без слоя определений даёт формально-валидный, но вводящий в заблуждение output)
  - wiki/canon/marketing-frameworks/llm-bot-customer-tolerance-gorny-frame.md (Descript расширение frame на роль видеомонтажёра + новая moat-erosion ось (general-purpose агент обходит специализированный продукт))
  - wiki/evolving/industry-trends/software-moat-erosion-2026.md (Gorny 2.0 Descript: специализированный prosumer-продукт обходится general-purpose агентом из коробки — commoditization сверху)
  - wiki/evolving/content-trends/vibe-coding-curse-content-hooks-2026.md (Горный vibecoding-flood second voice + Ikigai Magic кейс (Hook 5: книга→приложение за выходные, дистрибуция как узкое горло))
  - wiki/evolving/industry-trends/ru-vertical-ai-signals-2026.md (Сигнал 14 Ikigai Magic — первый consumer self-development vertical AI (vibecoding-flood proof-point в нише GRO))
  - wiki/evolving/competitor-positioning/aiacademy-claude-code-course-gorny-shevchenko-2026.md (финальный 4-й анонс курса (5069): 2 вебинара ~4ч, старт суббота 16 мая, высокая частота author-promo подтверждена)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 5, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_startupoftheday_20260519-101000.md (+ .note.md, .triage.json)

## [2026-05-22 14:55] [ingest] | Telegram @rybakovigor — 20 постов 14–18 мая 2026 (бандл 1 текст + 19 медиа): «быть собой» frame + Эквиум×Физтех2050 карусель + многосредие essay + бизнес-сериал эп.3 + #УтроТНТ
- source: wiki/sources/2026-05-19-tg-rybakovigor-may14-18-2026.md
- created:
  - wiki/canon/marketing-frameworks/strength-as-constraint-reinvention-rybakov.md
  - wiki/canon/marketing-frameworks/business-university-bridge-equium-phystech.md
  - wiki/evolving/content-trends/founder-tv-morning-show-appearance-format.md
- updated:
  - wiki/evolving/content-trends/rybakov-management-narrative-hooks.md (+4 хука (#27 «быть собой больше не помогает» — сила как ограничение; #28 «стоимость совместного действия» — многосредие; #29 «правила 90-х устарели» — anachronism-risk; #30 «один вопрос меняет годы» — practice-leverage); счётчик 26→30; +5 cross-links + source)
  - wiki/evolving/content-trends/telegram-native-formats.md (+3-й Equium-карусель sub-exemplar (Эквиум × Физтех 2050, 9 страниц, msg 6557–6565) — тройное подтверждение формата + calibration-правило «объём = функция значимости инфоповода»; +source)
  - wiki/evolving/content-trends/founder-history-edutainment-format.md (+эпизод 3 «жёсткие правила 90-х» (msg 6573) — self-diagnosis/anachronism-угол «возможно, ТЫ ведёшь дела по правилам 90-х»; pattern-эволюция через 3 эпизода (memoir→math→self-diagnosis); +cross-link + source)
  - wiki/canon/marketing-frameworks/environment-architecture-entrepreneur-safety.md (+межсубъектный уровень «многосредие / стоимость совместного действия» (essay msg 6569) — расширение от внутрифирменной к межсубъектной архитектуре + новая метрика; +2 cross-links + source)
  - wiki/canon/marketing-frameworks/community-as-evolution-vs-business-as-deal.md (+operationalization рамки (Эквиум × Физтех 2050 bridge + essay многосредие) — доказательство, что «сообщество-эволюция» реализуется через институт-партнёрства + снижение стоимости совместного действия; +cross-link + source)
- superseded: none
- sensitive flag: msg 6569 содержит № банковского счёта благотворит. кампании — не перенесён в слои, остаётся в raw/
- layer-touched: {canon: 4, evolving: 4, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_rybakovigor_20260519-114138.md + 19 children (11 media jpg + 8 video mp4) → status: processed

## [2026-05-22 20:30] [ingest] | Telegram @stodnevka2 (Армен Петросян) — 5 постов 15–19 мая 2026 (минимализм инструментов, штиль, три зоны риска, content-as-method, кризисная describe-the-state + market-mood) + 1 инфографика
- source: wiki/sources/2026-05-22-tg-stodnevka2-may-15-19-2026.md
- created:
  - wiki/canon/marketing-frameworks/petrosian-tool-fetish-minimalism.md
  - wiki/canon/marketing-frameworks/petrosian-third-problem-type-stillness.md
  - wiki/canon/marketing-frameworks/petrosian-three-risk-zones.md
- updated:
  - wiki/canon/marketing-frameworks/petrosian-content-as-accelerator.md (+секция content-as-method (пост 2310): книжная часть 2 готова за 2 мес, «методом была сама рассылка», emergent-method «план рождается из шагов»; +source 2026-05-22.)
  - wiki/evolving/industry-trends/max-messenger-author-rejection-2026.md (+update 2026-05-22: книжная часть 2 подтверждена готовой (closing datapoint), newsletter cadence ~75+ дней; +market-mood signal «охваты падают, покупок меньше, режим выживания, туман» — расширение рамки с platform-decay на macro-demand-decay; +source.)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (+расширение шахматной секции (пост 2311): «размытая тревога опаснее конкретной», «сегодня решаю только сегодняшнее», 4-шаговый describe-the-state протокол, 5 новых hook-формулировок для жанра «работа в тумане», +2 trinity-cross-link на новые страницы; +source.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 2, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_stodnevka2_20260519-133500.md + 1 child (raw/processed/media/tg_stodnevka2_2309.jpg) + 3 sidecars → status: processed

## [2026-05-22 15:10] [ingest] | Telegram @Theedinorogblog — 14 постов + 9 медиа 14–19 мая 2026 (стартап-новости bundle: 4 столпа B2B-аутрич, «Кампус» edtech, Figure AI PR, OpenClaw $1,3M 2nd-source)
- source: wiki/sources/2026-05-19-tg-theedinorog-may-14-19-2026.md
- created:
  - wiki/volatile/weekly-digest/edinorog-may-14-19-2026-digest.md
  - wiki/canon/marketing-frameworks/b2b-outreach-4-pillars-leadgenvalley.md
  - wiki/evolving/competitor-positioning/kampus-edtech-ru-2026.md
- updated:
  - wiki/evolving/industry-trends/humanoid-robot-narrative-shift-2026.md (+третий RU-источник того же Figure AI livestream (Edinorog 7959): displacement-frame «человек умудрился не проиграть» + livestream-merch как PR-приём (120 ч нон-стоп + магазин мерча))
  - wiki/evolving/industry-trends/agent-first-world-openclaw-2026.md (+second-RU-attestation $1,3 млн/мес токенов OpenClaw (Edinorog 7956 via VC) к fully-agentic-team сигналу; стоимость стала предметом публичной дискуссии)
  - wiki/evolving/content-trends/competitor-data-poisoning-defense-pattern.md (+cross-ref на новый продуктовый/метрический профиль «Кампуса» (второе появление в корпусе, питч 7950))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 4, volatile: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_Theedinorogblog_20260519-123147.md + 9 children (5 media + 4 video) → status: processed

## [2026-05-22 15:05] [ingest] | Telegram @techsparks (Себрант) — 6 постов 14–18 мая 2026 (5600–5605): Monet confirmation-bias + Economist acceptance-pivot + AI-vs-EV энергия + Шмидт освистан (bundle: primary + 5 children, видео 5602 без транскрипта quota 429)
- source: wiki/sources/2026-05-19-tg-techsparks-monet-economist-may-2026.md
- created:
  - wiki/evolving/content-trends/ai-confirmation-bias-monet-experiment-2026.md
  - wiki/evolving/industry-trends/ai-narrative-acceptance-economist-pivot-2026.md
  - wiki/evolving-strict/market-data/ai-vs-ev-energy-consumption-2026.md
- updated:
  - wiki/evolving/content-trends/slopshaming-counter-hook-2026.md (+раздел «Эмпирическая опора — Monet-эксперимент SHL0MS»: натурное подтверждение тезиса о гейткипинге (метка AI → достроенная критика подлинного Моне); +cross-link на новую страницу Monet-эксперимента; +source)
  - wiki/evolving/industry-trends/ai-narrative-second-phase-risk-pivot-2026.md (+раздел «Mainstream-слой и аудиторные сигналы (@techsparks)»: Economist acceptance-pivot как более поздний mainstream-слой (движение к 3-й фазе) + Шмидт освистан студентами как audience-backlash на 1-фазную adoption-риторику; +2 cross-links; +source)
  - wiki/evolving/industry-trends/ai-energy-bottleneck-debunked-gorny-2026.md (+раздел «Второй независимый RU counter-anchor — Себрант (EV-vs-AI энергия)»: два RU-эксперта (Горный макро-расчёт + Себрант EV-сравнение) независимо опровергают AI-energy-bottleneck; +строка в triangulation-таблицу; +cross-link на strict-страницу цифр; +source)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, evolving-strict: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_techsparks_20260519-141927.md + 5 children (media/5601,5603,5604,5605 + video/5602, all → processed; video .audio.mp3 audit-sidecar included)

## [2026-05-22 15:10] [ingest] | Telegram @techno_yandex — бандл 24 постов 14–19 мая 2026 (AI-фотосессия how-to + ML-планировщик роботов + гиперконтекст)
- source: wiki/sources/2026-05-19-tg-techno-yandex-may-14-19-2026.md
- created:
  - wiki/evolving/content-trends/ai-photoshoot-prompt-framework-2026.md
  - wiki/evolving-strict/product-metrics/yandex-delivery-robot-ml-planner-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-personalization-industrial-shift-2026.md (+2-й RU B2C predictive-intent кейс — Яндекс «Моя волна» гиперконтекст (context-aware рекомендации: день/время/локация/устройство → «музыкальный сценарий момента»); подтверждает переход стадии context-aware B2C из «единиц» в «нормализуется» (после VK Видео); +source +2 cross-link; updated 05-06→05-19)
  - wiki/evolving/content-trends/plastic-ai-content-pushback-hook.md (+Vendor self-own exemplar — Sony Xperia 1 VIII «лучшая антиреклама ИИ» (AI-ассистент камеры пересветил/убил детали): empirical content-hook «AI делает хуже, не лучше», 2 готовые формулировки; +source +2 cross-link; updated 05-05→05-19)
  - wiki/evolving/content-trends/ai-impersonation-into-classic-scenes-2026.md (+5-й канал self-insertion — «себя на матче»/«Нейротренды» Яндекс (@techno_yandex 5232): mass-consumer self-insertion + вендорский how-to, расширяет тренд из creator-нишы в consumer-tool; +source +2 cross-link; updated 05-14→05-19)
  - wiki/evolving/content-trends/ai-in-pr-workflows-2026.md (+cross-link на новый sibling Яндекс-how-to (ai-photoshoot-prompt-framework-2026) + новый source — awareness-фронт расширяется от профессионалов к массовому пользователю)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, evolving-strict: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_techno_yandex_20260519-140657.md + 24 children (18 jpg + 6 mp4) → processed

## [2026-05-22 20:30] [ingest] | Telegram @temno (Морейнис) — 4-й дамп 14–19 мая 2026 (9 постов + 9 изображений, bundle)
- source: wiki/sources/2026-05-19-tg-temno-moreynis-may-14-19-2026.md
- created:
  - wiki/canon/marketing-frameworks/sell-the-answer-not-platform-moreynis.md
  - wiki/canon/marketing-frameworks/only-product-scales-harvey-moreynis.md
  - wiki/canon/marketing-frameworks/able-and-willing-customer-selection-moreynis.md
  - wiki/evolving/industry-trends/open-extensible-saas-shift-2026.md
  - wiki/evolving-strict/market-data/chatgpt-entrepreneur-industry-mix-2026.md
- updated:
  - wiki/evolving/industry-trends/ai-native-company-architecture-2026.md (+аксиоматическая дефиниция Морейниса «ИИ-нативная компания > ИИ-нативный продукт» (тройное отрицание) + 3 операционных maxim (агентов делать не людей нанимать; SKILLS.md вместо должностных инструкций); 2-й независимый RU-голос к Перегудову)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+под-рамка «масштабируемая самозанятость» (Морейнис 7842): ИИ снимает потолок руки×часы; self-selection insight (anti-management disposition = pro-AI-native-solo); 0-employee вариант micro-team)
  - wiki/canon/marketing-frameworks/b2b-ai-sales-playbook-moreynis.md (+4-й source; усиление правила 5 industry-mix данными (массовый ИИ-предприниматель = non-tech сервисный SMB); cross-ref на 3 новые sibling-страницы)
  - wiki/evolving/content-trends/moreynis-hand-drawn-meme-format.md (+4-й последовательный дамп (four-source convergence); возврат архетипа B (a16z-карточка 7834) — уточнён как periodic, не выбывший; формат идентичен)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 3, evolving-strict: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_temno_20260519-122010.md + 9 children (media/tg_temno_7834..7842.jpg) + sidecars (.note.md ×10, .triage.json ×1)

## [2026-05-22 20:30] [ingest] | TG @typicalcompany пост 1337 (18 мая) — Тим Кук как операционный CEO-стратег (5-й ingest канала, bundle +1 фото)
- source: wiki/sources/2026-05-22-tg-typicalcompany-may-18-2026-tim-cook.md
- created:
  - wiki/canon/marketing-frameworks/operational-ceo-as-strategist-cook.md
- updated:
  - wiki/evolving/competitor-positioning/typical-company.md (+Continuity-update пост 1337 (пятый ingest): новый content-pillar «бизнес-кейс CEO как management-урок» + CEO-succession Apple-серия (1333/1336/1337) + наблюдение о снижении фактологической аккуратности (Apple-датировка); confidence сохранён medium-high)
  - wiki/canon/marketing-frameworks/operational-turnaround-playbook-wiedeking.md (+Cross-ref секция: production-first CEO в рост-режиме (Кук) vs turnaround-режиме (Wiedeking); оба делают операционку стратегией)
  - wiki/canon/marketing-frameworks/apple-ecosystem-recurring-revenue-frame.md (+Секция «кто построил эту экосистему» — Apple Services/recurring как результат операционной дисциплины Кука, не визии Джобса; cross-ref на cook-рамку)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_typicalcompany_20260519-010501.md + 1 child (media/tg_typicalcompany_1337.jpg) + 3 sidecars → status: processed

## [2026-05-22 15:20] [ingest] | Telegram @t_jrnl (Тинькофф Журнал) — дайджест 09–13 мая 2026 (маркетплейс-комиссии + editorial-форматы)
- source: wiki/sources/2026-05-19-tg-t-jrnl-may-9-13-2026.md
- created:
  - wiki/evolving/content-trends/t-j-editorial-format-playbook-2026.md
- updated:
  - wiki/evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026.md (+категорийно-максимальные комиссии Т—Ж (Я.Маркет 68% / Ozon 55% / WB 33%) как independent numeric cross-check practitioner-диапазона 25-35%; раскрытие дисперсии комиссий.)
  - wiki/evolving-strict/campaign-metrics/ru-marketplace-channel-economics-2026-05.md (+per-platform детализация комиссий Т—Ж, уточняющая baseline-строку «25-35%» вверх (до 68% для нишевых категорий).)
  - wiki/evolving/content-trends/news-reframing-carousel-gro.md (+cross-ref на t-j-editorial-format-playbook (числовая карусель Т—Ж как exemplar того же карусельного принципа).)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 2, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_t_jrnl_20260519-105011.md + 49 children (media/*.jpg)

## [2026-05-22 15:18] [ingest] | Telegram @tinkoffbank — батч 10694–10718 (14–18 мая 2026): Город→logistics, Т-Мобайл, Кэшбэк месяца, Вклад в поколение, Доли-агрегатор (bundle: 1 article + 22 media)
- source: wiki/sources/2026-05-19-tg-tinkoffbank-10694-10718-may-batch.md
- created:
  - wiki/evolving/content-trends/tbank-recurring-monthly-cashback-format-2026.md
  - wiki/evolving/content-trends/csr-grant-as-referable-content-2026.md
- updated:
  - wiki/evolving/industry-trends/tbank-corporate-platform-stack-2026.md (+«Город»→«Отправка посылок» (2-я merchant-категория, multi-courier aggregation), +Т-Мобайл telecom-vertical (390₽/50ГБ, MNP-retention), +«Кэшбэк месяца» recurring loyalty, +«Вклад в поколение» CSR/Т-Образование adjacency; обновлён updated + sources)
  - wiki/volatile-strict/competitor-news/tbank-doli-bnpl-aggregator-2026-05.md (+раздел «Consumer-facing подтверждение»: aggregator-мессаджинг #10706 «все магазины-партнёры и графики списаний в одном приложении» вышел в consumer-канал; 4-split без комиссии, летние партнёры; inline-маркеры [conf:high, src:2026-05-15])
  - wiki/evolving/content-trends/daily-streak-gamification-in-finance.md (+раздел «Контраст: daily-streak vs monthly-window»: «Кэшбэк месяца» как дополняющий cadence-режим, закрывающий ограничение daily-streak (mass-retail); cross-ref на новую страницу формата)
  - wiki/evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay.md (+обновление май-батч #10706/#10714: подтверждение lifestyle-object-hero вариации (Доли mint headline-overlay, «Кэшбэк месяца» жёлтый product-crate как brand-accent на нейтральном BG))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, volatile-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_tinkoffbank_20260519-104504.md + 22 children → raw/processed/media/ (all + sidecars)

## [2026-05-22 15:18] [ingest] | Telegram @TorbosovLife — re-dump 50 постов 11–15 мая 2026 (AI-рилсы краудсорсинг + premium-RE май + Dubai-cooling); bundle primary + 48 children
- source: wiki/sources/2026-05-19-tg-torbosov-life-may-2026.md
- created:
  - wiki/evolving/content-trends/torbosov-ai-reels-repurposing-2026.md
- updated:
  - wiki/evolving/content-trends/contrarian-framing-expert-telegram.md (+второй дамп Торбосова как мульти-паттерн-кейс; контр-нарративная рамка применена к искусству (#культпросвет 19672) — третий под-приём вариации 4-го элемента (historical-precedent-anchor); +source в sources/front-matter)
  - wiki/evolving-strict/market-data/ru-premium-real-estate-q1-2026.md (+раздел «Обновление 2026-05-19» с майскими Whitewill operational numbers (Dubai +$15m, Solaya off-plan ₽312,4m=AED15,554k [conf:high], Bluewaters 4 выкупа, Dubai-cooling-прогноз) — все с inline [conf:*,src:*] маркерами; +source)
  - wiki/evolving/industry-trends/ru-premium-segment-cooling-2026.md (+четвёртый sentinel (cross-geo Dubai) от того же оператора Торбосова: «до осени не жду активности от покупателей»; cross-geo caveat (тот же информант, но географическое расширение); +source)
  - wiki/evolving/content-trends/founder-history-edutainment-format.md (+смежный variant «curator-edutainment» (Торбосов #культпросвет/#подомам vs personal-history Рыбакова): сравнительная таблица + структура curator-поста + перенос в GRO (доступно молодому бренду без 30-летнего timeline); +source)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_TorbosovLife_20260519-114702.md + 48 children (45 media/jpg, 1 audio/ogg [transcript deferred — whisper 429], 2 video/mp4) → status: processed

## [2026-05-22 15:25] [ingest] | Telegram @vcnews — 50 постов 12–14 мая 2026 (Cerebras IPO close, Anthropic credits live, RU marketing-кейсы)
- source: wiki/sources/2026-05-19-tg-vcnews-may-12-14-2026.md
- created:
  - wiki/volatile/weekly-digest/2026-05-19-tg-vcnews-may-12-14-digest.md
  - wiki/evolving/content-trends/irnby-nike-lookalike-ad-controversy-2026.md
  - wiki/evolving/content-trends/swatch-ap-royal-pop-hype-mismatch-2026.md
  - wiki/volatile-strict/competitor-news/google-gemini-intelligence-android-2026-05.md
  - wiki/volatile-strict/competitor-news/notion-developer-platform-agents-2026-05.md
- updated:
  - wiki/volatile-strict/industry-news/cerebras-ipo-2026-05.md (supersession: IPO ЗАКРЫТ — $5,55 млрд raised (выше price-up target $4,8 млрд), cap после IPO ~$40 млрд (~$49 млрд с опционами), pre-IPO estimate $48,8 млрд superseded)
  - wiki/volatile-strict/competitor-news/anthropic-third-party-credits-2026-06.md (анонс → подтверждённый запуск (vc.ru second-source): кредиты через SDK/GitHub Actions/OpenClaw, не в чате, overflow по API; caveat снят, confidence medium→high)
  - wiki/volatile-strict/competitor-news/thinking-machines-interaction-model-2026-05.md (4-й источник: первая публичная демо TML-Interaction (vc.ru, с видео), подтверждение product-rollout phase, reconcile product-name TML-Interaction)
  - wiki/volatile-strict/competitor-news/google-googlebook-2026-fall.md (vc.ru second-source + детали: Android+ChromeOS, Gemini Intelligence до уровня указателя мыши; cross-link на Gemini-Intelligence-Android)
  - wiki/volatile-strict/competitor-news/android-pause-point-doomscroll-2026.md (vc.ru second-source: подтверждение Pause Point, вариативность интервенции (пауза/дыхание/таймер))
  - wiki/evolving/competitor-positioning/max-messenger.md (+Update 2026-05-12: операторская A2P-сделка (Билайн/МТС/Мегафон/Т2 + MAX) — транзакционный канал OTP + сообщения компаний, конкуренция SMS-агрегаторам)
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (+Update 2026-05-19 vcnews 12-14 мая: два сигнала закрылись фактом (Cerebras IPO, Anthropic credits), Google consumer-волна (Gemini Intelligence/GoogleBook), Thinking Machines демо, Notion agents, Wispr $2B, Cisco $15,8B)
  - wiki/evolving/content-trends/engineered-scandal-attention-playbook.md (+documented example Irnby/Nike lookalike-провокация (2-й кейс), sample size 1→2)
- superseded:
  - wiki/volatile-strict/industry-news/cerebras-ipo-2026-05.md
- sensitive flag: none
- layer-touched: {volatile: 1, evolving: 4, volatile-strict: 7, sources: 1}
- touched: 14 pages
- raw: raw/processed/articles/tg_vcnews_20260519-102022.md + 47 children (44 jpg + 3 mp4) + sidecars (.note.md, .triage.json)

## [2026-05-18 21:00] [ingest] | Pressfeed/Слотина — клонирование сайта эксперта: playbook первых часов + медиакапитал как защита + takedown-бенчмарк
- source: wiki/sources/2026-05-18-pressfeed-website-clone-fraud-playbook-slotina.md
- created:
  - wiki/canon/marketing-frameworks/website-clone-incident-playbook-2026.md
  - wiki/evolving/content-trends/media-capital-as-clone-defense-2026.md
  - wiki/evolving-strict/campaign-metrics/website-clone-takedown-cost-benchmark-2026.md
- updated:
  - wiki/evolving/content-trends/ai-screenshot-trust-crisis-2026.md
  - wiki/evolving/content-trends/anti-impersonation-operational-notice.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 3, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_moshenniki-skopirovali-sajt-chto-predprinyat-ekspertu-v-perv_57926a5d.md

## [2026-05-22 21:00] [ingest] | Pressfeed — замена Google Forms (11 RU-сервисов опросов): 152-ФЗ локализация ПДн + импортозамещение + тарифы + survey design
- source: wiki/sources/2026-05-22-pressfeed-survey-tools-data-localization-ru.md
- created:
  - wiki/canon-strict/legal-claims/ru-data-localization-152fz-2025.md
  - wiki/evolving/industry-trends/ru-survey-tools-import-substitution-2026.md
  - wiki/evolving-strict/market-data/ru-survey-tools-pricing-2026.md
  - wiki/canon/marketing-frameworks/survey-design-best-practices.md
- updated:
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md
  - wiki/evolving/industry-trends/ru-digital-regulatory-squeeze-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 2, evolving: 2, evolving-strict: 1, canon: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_na-zamenu-gugl-formam-11-servisov-dlya-oprosov-razreshennyh-_a10cd00c.md

## [2026-05-22 02:15] [ingest] | Pressfeed: нейросети/конструкторы для приложений без кода (10+ сервисов) — новый RU app-builder inventory (3 под-типа) + disambiguation от agent-builders + content-нарратив «приложение собирает каждый»
- source: wiki/sources/2026-05-22-pressfeed-nocode-app-builders-10-servisov.md
- created:
  - wiki/evolving/competitor-positioning/ru-nocode-app-builder-platforms-2026.md
  - wiki/evolving/content-trends/no-code-everyone-builds-narrative-2026.md
- updated:
  - wiki/evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026.md (+disambiguation-врезка agent-builder ≠ app-builder с cross-ref на новый inventory; +GigaStudio (Сбер) как новый app-builder-сосед к ГигаЧат Бизнес; +2 link в Связанные страницы; +source.)
  - wiki/evolving/competitor-positioning/vibecoding-stack-ecosystem-2026.md (+подсекция «RU-локализованные prompt-to-app аналоги» в L1 (Чатиум/Miniapps.ai/GigaStudio vs Lovable/Base44/Rork; Rork-аналога в RU нет — gap); +2 link; +source.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_nejroseti-i-konstruktory-dlya-sozdaniya-prilozhenij-bez-znan_0fc9d0c1.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-22 15:33] [ingest] | Telegram @your_pet_project (Табунов) — посты 630–632 (FaceKit AI-инфлюенсер app-кейс + 10 пунктов про рынок РФ) [bundle: 1 article + 1 image]
- source: wiki/sources/2026-05-19-tg-your-pet-project-may-14-18-2026.md
- created:
  - wiki/evolving-strict/competitor-metrics/facekit-ai-influencer-app-monetization-2026.md
  - wiki/canon/marketing-frameworks/abandon-cart-paywall-dark-patterns.md
  - wiki/canon/marketing-frameworks/ru-it-market-launch-playbook-tabunov.md
  - wiki/evolving-strict/market-data/ru-it-market-launch-economics-2026.md
- updated:
  - wiki/canon/marketing-frameworks/ai-influencer-grandma-playbook.md (+FaceKit как второй cross-corroborating AI-инфлюенсер кейс (AI-аватары продают софт/подписку, не только физпродукт); +сравнительная таблица бабушки vs FaceKit; +2 cross-ref + delta-секция)
  - wiki/evolving/content-trends/your-pet-project-channel-hooks.md (+дельта 4-го дампа (посты 631-632): 6 FaceKit-hooks + 8 RU-рынок-hooks; +5 cross-ref в backlinks; +новый source)
  - wiki/evolving/industry-trends/ai-solopreneurship-window-2026-2029.md (+RU-специфика окна (Табунов 632): «запускаться проще, масштабировать сложнее», дефицит трафика как главный RU-constraint вместо капитала, русский венчур не заливает ниши → соло-преимущество; +новый source)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, evolving-strict: 2, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_your_pet_project_20260519-122011.md + 1 child (raw/processed/media/tg_your_pet_project_631.jpg)

## [2026-05-18 11:50] [ingest] | Pressfeed: От креатива к конверсии — 4-этапный фреймворк продающей кампании + температура аудитории
- source: wiki/sources/2026-05-18-pressfeed-creative-to-conversion-campaign.md
- created:
  - wiki/canon/marketing-frameworks/creative-to-conversion-campaign-framework.md
  - wiki/canon/marketing-frameworks/audience-temperature-cold-warm-hot.md
- updated:
  - wiki/canon/marketing-frameworks/qualitative-adjectives-ad-copy.md (+cross-link на creative-to-conversion (A/B заголовков = самый дешёвый рычаг этапа 3; заголовок = первый из 3 обязательных элементов креатива по редакции Pressfeed); +source в front-matter, updated 2026-05-18)
  - wiki/canon/marketing-frameworks/funnel-simplicity-principle.md (+cross-link на creative-to-conversion (правило 2 = outcome-фокус этапов 1-2, правило 1 = чёткость CTA этапа 2); +source в front-matter, updated 2026-05-18)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_ot-kreativa-k-konversii-kak-sozdavat-reklamnye-kampanii-koto_e64c9ef8.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-18 21:00] [ingest] | Pressfeed/Середа — вебинар «Рынок труда 2026: кто диктует правила» (update-only)
- source: wiki/sources/2026-05-18-pressfeed-rynok-truda-2026-sereda.md
- created:
  - none
- updated:
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
  - wiki/evolving/industry-trends/candidate-side-ai-services-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_rynok-truda-2026-kto-diktuet-pravila-i-kak-iskat-rabotu-v-no_de037c0d.md

## [2026-05-18 21:00] [ingest] | Pressfeed/Жаринов — кризис как перезагрузка (crisis-speed-gap фреймворк + опережающие индикаторы)
- source: wiki/sources/2026-05-18-pressfeed-krizis-perezagruzka-zharinov.md
- created:
  - wiki/canon/marketing-frameworks/crisis-speed-gap-zharinov.md
- updated:
  - wiki/canon/marketing-frameworks/business-crisis-playbook-apollo13.md
  - wiki/canon/marketing-frameworks/weak-signals-crisis-3-stages.md
  - wiki/canon/marketing-frameworks/change-management-tuckman-kotter-ramazanov.md
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_padenie-kak-instrument-pochemu-krizis-v-biznese-eto-ne-konec_8fb38f79.md

## [2026-05-23 18:46] [ingest] | Pressfeed: Обновления Telegram 2025–2026 — capabilities-карта + global-post-search lead-gen + Stars/подарки монетизация + расширение Telegram Ads
- source: wiki/sources/2026-05-18-pressfeed-telegram-updates-2025-2026.md
- created:
  - wiki/evolving/content-trends/telegram-platform-capabilities-2026.md
  - wiki/canon/marketing-frameworks/telegram-global-post-search-leadgen.md
  - wiki/evolving/content-trends/telegram-stars-gifts-creator-monetization-2026.md
- updated:
  - wiki/evolving-strict/campaign-metrics/telegram-ads-benchmarks-2026.md (+раздел «Расширение рекламного инвентаря Telegram Ads 2025–2026»: Banner in Video, реклама в ботах от 1000 пользователей, поиск по ключевым словам, Pixel Tag, снижение порога входа (5 inline-маркеров conf:medium/src:2026-05-18) + 2 cross-ref + источник в front-matter)
  - wiki/canon/marketing-frameworks/smm-analytics-2026-framework.md (+раздел «Telegram-специфика аналитики»: дефицит нативной аналитики TG → TGStat/Telemetr/Popsters/Adstat.pro; глобальный поиск постов как источник сигнала; +механика «сообщение каналу» в Связь-с-GRO; +3 cross-ref + источник)
  - wiki/evolving/content-trends/telegram-native-formats.md (+2 cross-ref на новые capabilities/monetization страницы в Связанных + источник в front-matter)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, canon: 2, evolving-strict: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_obnovleniya-telegram-v-2025-2026-obzor-novyh-vozmozhnostej-v_9d605de6.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 00:00] [ingest] | Pressfeed: Рерайт текстов в 2026 — ландшафт AI-рерайт-инструментов (3 задачи + 5 категорий + бенчмарк качества + детектор≠доказательство)
- source: wiki/sources/2026-05-18-pressfeed-rerajt-tools-2026-landscape.md
- created:
  - wiki/canon/marketing-frameworks/rewrite-task-tool-matching-2026.md
  - wiki/evolving/competitor-positioning/ai-rewriter-tool-landscape-5-tiers-2026.md
  - wiki/evolving-strict/competitor-metrics/llm-rewrite-quality-benchmark-2026.md
- updated:
  - wiki/evolving/content-trends/ai-text-detection-landscape-2026.md (+секция «детектор ≠ доказательство оригинальности» (Text.ru/Advego/GPTZero/Originality.ai/ZeroGPT врут в обе стороны; фактчек = ручная сверка по первоисточникам); уникальность ≠ оригинальность.)
  - wiki/canon/marketing-frameworks/ai-content-marketing-delegation-frame-lz-media.md (+секция «операционный нижний слой»: cross-ref на rewrite-task-tool-matching как «каким инструментом» выполнить делегированное; 2 из 6 горячих зон = 2 из 3 задач рерайта; trap скрытой модели.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_rerajt-tekstov-v-2026-na-chyom-realno-rabotayut-redakczii-i-_cab61ab7.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-07 21:00] [ingest] | Деловой Петербург — 68% петербуржцев: автоматизация как инструмент эффективности (update-only)
- source: wiki/sources/2026-05-07-dp-68-peterburzhcev-avtomatizaciya-effektivnost.md
- created:
  - none
- updated:
  - wiki/evolving-strict/market-data/hh-automation-survey-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_07_68-peterburzhcev-schitajut-avtomatizaciju_765f311c.md

## [2026-05-18 21:00] [ingest] | Pressfeed — Топ-12 подборок книг (listicle-hub SEO-pattern: «подборка подборок» как pillar)
- source: wiki/sources/2026-05-18-pressfeed-top-12-book-collections-listicle-hub.md
- created:
  - wiki/evolving/content-trends/pressfeed-listicle-hub-seo-pattern.md
- updated:
  - wiki/evolving/content-trends/pressfeed-paid-placement-ai-edu-pattern.md
  - wiki/evolving/content-trends/pressfeed-ceo-personal-effectiveness-essay-pattern-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_top-12-podborok-knig-dlya-piarshhikov-marketologov-i-vseh-kt_3c022fc1.md

## [2026-05-18 11:50] [ingest] | Pressfeed: Скорость сайта как основа роста интернет-магазина (advertorial Smink) — site-speed conversion lever + platform-advertorial pattern
- source: wiki/sources/2026-05-18-pressfeed-skorost-sajta-rost-internet-magazina.md
- created:
  - wiki/canon/marketing-frameworks/site-speed-as-conversion-lever.md
  - wiki/evolving/content-trends/pressfeed-platform-advertorial-pattern.md
- updated:
  - wiki/canon/marketing-frameworks/mobile-ux-b2b-conversion.md (+cross-ref на site-speed-as-conversion-lever как смежный технический рычаг конверсии)
  - wiki/evolving/content-trends/vcru-hr-content-patterns-2026.md (+cross-ref на pressfeed-platform-advertorial-pattern (контраст тонкий platform-advertorial vs серийный SEO-лонгрид))
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_skorost-sajta-kak-osnova-rosta-internet-magazina-praktichesk_59fa1c61.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 18:50] [ingest] | Pressfeed/Горская — «Владелец устал: бизнес — зеркало владельца» (founder-bottleneck личностный регистр)
- source: wiki/sources/2026-05-18-pressfeed-gorskaya-owner-as-mirror.md
- created:
  - wiki/canon/marketing-frameworks/owner-as-mirror-transformation-gorskaya.md
- updated:
  - wiki/canon/target-audience/ru-smb-founder-owner-seller.md (+«зеркало владельца» recognition-hook в секцию маркетинговых хуков: болевой профиль выгорания founder'а из колонки Горской дословно совпадает с маркерами сегмента.)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (+cross-ref на owner-as-mirror-transformation-gorskaya как личностный регистр того же owner-escape problem-space + source.)
  - wiki/canon/marketing-frameworks/owner-strategist-operator-three-roles-separation.md (+cross-ref на owner-as-mirror как личностный близнец структурного фрейма разделения ролей.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_vladelecz-ustal-pochemu-biznes-ne-rastet-i-kak-vyjti-iz-tupi_250a8863.md (+ .note.md, .triage.json)

## [2026-05-23 13:51] [ingest] | Pressfeed: запрет иностранных слов по 168-ФЗ — детали КоАП (ст. 14.8), B2B-исключение + 14 сервисов автопроверки на англицизмы
- source: wiki/sources/2026-05-18-pressfeed-168fz-anglicism-check-services.md
- created:
  - wiki/evolving/content-trends/ru-anglicism-check-tools-2026.md
- updated:
  - wiki/evolving/industry-trends/ru-brand-russification-law-2026.md (+ст. 14.8 КоАП (вилки штрафов), B2B-исключение, надзор Роспотребнадзор/ФАС без спец-штрафов, требование «перевод на виду в том же оформлении», ссылка на compliance-тулинг.)
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md (168-ФЗ subsection: +B2B-исключение, +ст. 14.8 КоАП и детализация ст. 14.3 ч.1 (inline-маркеры), +требование к оформлению перевода, +ссылка на тулинг автопроверки.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, canon-strict: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_news.pressfeed.ru_zapret-inostrannyh-slov-po-168-fz-14-servisov-dlya-proverki-_ad37e6ad.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 00:00] [ingest] | dp.ru — зарплаты СЗФО апрель 2026 (no relevant extractions: boilerplate-only crawl)
- source: wiki/sources/2026-05-08-www-dp-ru-a-2026-05-08-peterburg-v-aprele-stal-samim-d7ca8951.md
- created:
  - none
- updated:
  - none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_08_peterburg-v-aprele-stal-samim_d7ca8951.md

## [2026-05-23 00:00] [ingest] | dp.ru: Петербург третий по числу психологов-предпринимателей — контент не извлечён (фетч захватил только boilerplate), audit-only
- source: wiki/sources/2026-05-08-dp-ru-peterburg-psihologi-predprinimateli.md
- created:
  - none
- updated:
  - none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 pages
- raw: raw/processed/articles/web_www.dp.ru_a_2026_05_08_peterburg-okazalsja-tretim_c5441b5d.md (+ 3 sidecars: .bundle.json, .note.md, .triage.json)

## [2026-05-23 20:30] [ingest] | Demis Group/Дзен — квартальный аудит маркетинга (7 зон) + агентская экспертная колонка как content-trend
- source: wiki/sources/2026-05-19-dzen-demis-quarterly-marketing-audit.md
- created:
  - wiki/canon/marketing-frameworks/quarterly-marketing-audit-demis-7-zones.md
  - wiki/evolving/content-trends/demis-group-seo-agency-expert-column-pattern-2026.md
- updated:
  - wiki/canon/marketing-frameworks/marketing-audit-protocol.md (+cross-ref на квартальный аудит Demis: one-time диагностика расхождений (опрос) vs регулярная каденция ревизии систем/метрик.)
  - wiki/canon/marketing-frameworks/marketing-sales-alignment-framework.md (+cross-ref: этот фреймворк = зона 7 квартального аудита Demis (синхронизация маркетинга и продаж) + source.)
  - wiki/evolving/content-trends/expert-column-corporate-pr-format-soulful.md (+cross-ref на агентский sibling-вариант Дзен-колонки (Demis Group): персональный vs корпоративный бай-лайн.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 2, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_dzen.ru_a_agcEWFU4_3gzP-Vp_171841c5.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 19:15] [ingest] | Telegram @HR_kak_delat — посты 1990-1991 (15-18 мая 2026): прогноз HR до 2040 + бережная оптимизация ч.2
- source: wiki/sources/2026-05-19-tg-hr-kak-delat-may-15-18-2026.md
- created:
  - wiki/evolving/industry-trends/hr-profession-2040-fork-spk.md
  - wiki/canon/marketing-frameworks/gentle-optimization-10-ideas-hr-club.md
- updated:
  - wiki/canon/marketing-frameworks/hbr-5-org-change-tips-2026.md (+cross-ref на gentle-optimization-10-ideas (эта страница = идеи 1-5, продолжение в посте 1991))
  - wiki/canon/marketing-frameworks/change-management-tuckman-kotter-ramazanov.md (+коммуникационно-эмоциональный слой (идеи 6-10) в «Связь с другими рамками» + related-pages + source)
  - wiki/evolving/industry-trends/ru-labor-market-shift-2026.md (+cross-ref на hr-profession-2040-fork-spk как long-horizon проекцию краткосрочного сдвига)
  - wiki/evolving/industry-trends/ai-tax-labor-erosion-2026.md (+cross-ref на hr-profession-2040-fork-spk (UBI/технологическая безработица как long-horizon проекция fiscal-shift))
  - wiki/evolving/industry-trends/gen-z-workforce-shift-2026.md (+cross-ref на hr-profession-2040-fork-spk (кадровая мобильность/сокращение ролей как поколенческий фон))
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, canon: 3}
- touched: 7 pages
- raw: raw/processed/articles/tg_hr_kak_delat_20260519-094001.md

## [2026-05-23 14:16] [ingest] | Telegram @recruiter_live — дамп 19–22 мая 2026 (WB B2B-экспорт в Китай + границы NDA + карьерные хуки)
- source: wiki/sources/2026-05-23-tg-recruiter-live-may-19-22-2026.md
- created:
  - wiki/canon-strict/legal-claims/ru-nda-confidentiality-limits-2026.md
  - wiki/volatile-strict/industry-news/wb-china-b2b-export-2026-05.md
- updated:
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
  - wiki/evolving/industry-trends/ru-job-seeker-experience-2026.md
  - wiki/volatile-strict/industry-news/ru-china-trade-q1-2026.md
  - wiki/evolving/industry-trends/ru-marketplace-seller-squeeze-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon-strict: 1, volatile-strict: 2, evolving: 3, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_recruiter_live_20260523-091000.md (+ 3 media children: tg_recruiter_live_4477.jpg, _4478.jpg, _4481.jpg)

## [2026-05-23 14:16] [ingest] | TG @typicalcompany — посты 1338-1339 (20-22 мая 2026): HBR-«суперкоманды» (Friedman) + 9 книг для руководителей
- source: wiki/sources/2026-05-23-tg-typicalcompany-may-20-22-2026.md
- created:
  - wiki/canon/marketing-frameworks/hbr-superteam-7-practices-friedman.md
  - wiki/evolving/content-trends/research-digest-to-course-module-mapping.md
- updated:
  - wiki/evolving/competitor-positioning/typical-company.md
  - wiki/evolving/content-trends/book-recommendation-carousel-tg.md
  - wiki/canon/marketing-frameworks/sbi-grow-feedback-framework.md
- superseded: 1 supersession
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_typicalcompany_20260523-010501.md

## [2026-05-23 19:20] [ingest] | Telegram @psilonsk — 4-й дамп (range 5563..5569, week 3 мая): миллиметровка-antipattern + ИИ-как-инструмент + возврат платной интеграции
- source: wiki/sources/2026-05-19-tg-psilonsk-may-2026-week3.md
- created:
  - wiki/canon/marketing-frameworks/millimetrovka-overengineered-product-antipattern.md
- updated:
  - wiki/evolving/content-trends/psilonsk-management-hooks-bank.md (+ветка 13.x (бизнес-образ/личный бренд 5566, миллиметровка 5567, ИИ-как-инструмент 5568, observation платной интеграции 5569); окно наблюдения до ≈11,1 нед, 4-й дамп в sources.)
  - wiki/evolving/content-trends/psilonsk-channel-patterns.md (+4-й столбец метрик (окно 4: 7 постов / 4 дня), окно до ≈11,1 нед / 83 поста; supersession наблюдения о коммерческой нагрузке (нулевая→эпизодическая, возврат интеграции 5569); рекламный креатив 5569 как функциональное исключение из декоративных обложек.)
  - wiki/canon/marketing-frameworks/ai-amplifier-fragmented-vs-modular-jobs.md (+operational-механика amplify от Колганова (5568): декомпозиция задачи до делегирования ИИ как «как именно» fragmented-amplify; cross-attribution, остаётся confidence high.)
- superseded: wiki/evolving/content-trends/psilonsk-channel-patterns.md
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_psilonsk_20260519-131003.md + 4 children (media 5566-5569)

## [2026-05-19 09:30] [ingest] | GRO — чекаут интенсива Тариф 1 (240k/400k ₽, идентичен Тарифу 2 → тарифы различаются не ценой; founder+CMO pair подтверждён вторично)
- source: wiki/sources/2026-05-19-groapp-payment-intensive-tarif1.md
- created:
  - none
- updated:
  - wiki/canon/product-knowledge/gro-intensive.md (Тариф 1 = Тариф 2 по цене (240k/400k); корректировка модели «тарифы = ценовые уровни» → различаются НЕ ценой; частично закрыт open question #2.)
  - wiki/canon/product-knowledge/gro-pricing.md (Структура Тарифа 1 зафиксирована: идентична Тарифу 2; снята пометка «структура Тарифа 1 не зафиксирована».)
  - wiki/canon/target-audience/gro-segments.md (Вторичное подтверждение founder+CMO buyer-pair: тот же pair-pattern и цены на чекауте Тарифа 1 → устойчивый, не разовый дизайн.)
  - wiki/canon/marketing-frameworks/premium-perception-through-price.md (GRO «Интенсив» оформлен как собственный concrete-case premium-через-цену; стабильность цены между tarif1/tarif2 = deliberate anchor (не себестоимость); обновлён устаревший тезис «если GRO введёт premium-tier».)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_groapp.ru_payment-intensive-tarif1_1e913e3d.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 20:30] [ingest] | Деловой мир (Дзен) — билайн.ПРОдвижение: ИИ автозаполняет юр-блок в рекламных СМС (AI adtech: креатив → compliance)
- source: wiki/sources/2026-05-19-dzen-delovoy-mir-bilayn-prodvizhenie-ai-legal-sms.md
- created:
  - wiki/volatile-strict/competitor-news/bilayn-prodvizhenie-ai-legal-block-sms-2026-05.md
- updated:
  - wiki/evolving/industry-trends/ai-generated-creatives-in-advertising.md (+второй вектор тренда: AI расширяется из генерации креатива в автоматизацию compliance (юр-блок СМС, билайн.ПРОдвижение как 3-й RU-кейс) + таблица векторов + cross-refs.)
  - wiki/canon-strict/legal-claims/ad-marking-russia-2026.md (+секция «Обязательные сведения о рекламодателе в СМС + платформенная автоматизация»: состав юр-блока СМС, платформенный compliance-тулинг (Билайн Adtech), −8% reject (inline-маркеры).)
  - wiki/evolving/industry-trends/digital-indoor-retail-media-ru-2026.md (+cross-ref на второй adtech-вектор того же игрока (Билайн Adtech): AI-юр-блок в СМС — широта стека offline-инвентарь + AI-кабинет.)
  - wiki/evolving-strict/campaign-metrics/mindbox-channel-shift-2025.md (+cross-ref: supply-side контрапункт к оттоку из SMS — оператор снижает операционную стоимость SMS-промо AI-compliance-автоматизацией (−8% reject, inline-маркер).)
- superseded: none
- sensitive flag: none
- layer-touched: {volatile-strict: 1, evolving: 2, canon-strict: 1, evolving-strict: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_dzen.ru_a_agq24lrEqxFxzel0_503ac109.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-19 15:45] [ingest] | Дзен/Деловой мир — кейс Дикси × Билайн Adtech: Smart TV → офлайн-продажи (тест-контроль + Stable ID, +23,4 п.п. инкремента) + фреймворк измерения click-less каналов
- source: wiki/sources/2026-05-19-dzen-diksi-bilayn-smart-tv-offline-sales-case.md
- created:
  - wiki/canon/marketing-frameworks/clickless-channel-incrementality-stable-id.md
  - wiki/evolving-strict/campaign-metrics/diksi-bilayn-smart-tv-incrementality-2026.md
- updated:
  - wiki/evolving/industry-trends/digital-indoor-retail-media-ru-2026.md (+RU-валидация измеримости CTV/Smart TV (кейс Билайн Adtech × «Дикси», +23,4 п.п. инкремента) в секции «Связь с глобальным трендом» и в конкурентном ландшафте; +2 cross-link, +source, updated→2026-05-19.)
  - wiki/evolving-strict/market-data/digital-ad-cpm-shifts-q1-2026.md (+RU-валидация перехода на «подключённые экраны»: кейс Дикси доказал измеримый офлайн-эффект Smart TV через Stable ID [conf:medium, src:2026-05-19]; +3 cross-link, +source, updated→2026-05-19.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving-strict: 2, evolving: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_dzen.ru_a_agVwrVrEqxFxx5qI_60ff34a0.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 20:30] [ingest] | Деловой мир (Дзен) — Hook Model + Fogg + habit-retention диагностики (формирование привычки к продукту, Захар Константинов)
- source: wiki/sources/2026-05-19-dzen-delovoymir-habit-product-hook-model.md
- created:
  - wiki/canon/marketing-frameworks/hook-model-habit-loop.md
  - wiki/canon/marketing-frameworks/fogg-behavior-model.md
  - wiki/canon/marketing-frameworks/habit-retention-diagnostics.md
- updated:
  - wiki/canon/marketing-frameworks/retention-benchmarks-b2c.md (+секция «бенчмарки vs механики»: пороги говорят «дырявое ли ведро», habit-framework family отвечает «как поднять числа и почему пользователь возвращается»; cross-ref на Hook Model / Fogg / habit-diagnostics)
  - wiki/evolving/content-trends/social-media-addiction-design-patterns.md (+связка Pattern 2 (variable reward) = «переменная награда» элемент Hook Model — те же механики ethics-нейтрально как retention; граница через тест Юдина)
  - wiki/evolving/content-trends/daily-streak-gamification-in-finance.md (+теоретическая рамка: streak = «инвестиция» + «переменная награда» элементы Hook Model; streak-break churn = loss aversion; этический фильтр honest-прогресс vs FOMO)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 2, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_dzen.ru_a_agxRslU4_3gzRgjq_5d2f1512.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 14:28] [ingest] | Дзен/Деловой мир — Мул (Work Solutions): искать сотрудника по цифровому следу, а не по диплому (OSINT-найм + «ноль факапов» + цифровая гигиена)
- source: wiki/sources/2026-05-19-dzen-delovoymir-mul-digital-footprint-hiring.md
- created:
  - wiki/evolving/industry-trends/candidate-osint-digital-footprint-hiring-2026.md
  - wiki/canon/marketing-frameworks/zero-fuckups-antipatterns-culture-mul.md
  - wiki/evolving/content-trends/candidate-digital-hygiene-hooks-2026.md
- updated:
  - wiki/canon/target-audience/it-specialist-candidate-profile-2026.md
  - wiki/evolving/industry-trends/skill-based-hiring-russia-2026.md
  - wiki/canon/marketing-frameworks/recruitment-methods-taxonomy.md
  - wiki/evolving/content-trends/expert-column-corporate-pr-format-soulful.md
  - wiki/evolving/content-trends/demis-group-seo-agency-expert-column-pattern-2026.md
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 5, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/web_dzen.ru_a_agX9QFU4_3gzPn-l_ae2a6641.md

## [2026-05-23 14:44] [ingest] | hr-portal.ru — «Как оформить повышение в должности?» (evergreen HR-объяснялка, textbook reference; backfill в career-аудиторию)
- source: wiki/sources/2026-05-19-web-hr-portal-kak-oformit-povyshenie-v-dolzhnosti.md
- created: none
- updated:
  - wiki/evolving/content-trends/hr-portal-evergreen-genre-2026.md
  - wiki/evolving/content-trends/career-audience-hooks-2026.md
  - wiki/canon/target-audience/gro-segments.md
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, canon: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_kak-oformit-povyshenie-v-dolzhnosti_891abceb.md

## [2026-05-23 21:05] [ingest] | Telegram @vyakuba — 4-й срез 14–19 мая 2026 (Москва reality-событие, lesson-2 lead-magnet, 2 новых 7-card carousel: trust-habits + employee-side «Фразы начальника»)
- source: wiki/sources/2026-05-19-tg-vyakuba-may-14-19-2026.md
- created:
  - wiki/canon/marketing-frameworks/assertive-boundary-replies-vyakuba.md
- updated:
  - wiki/evolving/competitor-positioning/vyakuba-sales-training.md (4-й срез: Москва 9–10 окт reality-событие (новый offline-tier), «Про Продажи» поток 1 июня + lesson-2 lead-magnet (24h gated try-before-buy), affiliate cross-promo Бараковского, новая аудиторная вертикаль (employee-side), updated product-ladder.)
  - wiki/evolving/content-trends/vyakuba-instagram-carousel-format.md (Новая lime-green палитра (3-я визуальная), list-карусель как 3-й архетип (7 карточек), employee-side тема «Фразы начальника»; 2 новые 7-card carousel.)
  - wiki/evolving/content-trends/ru-sales-infobiz-content-patterns.md (Жанр 3 +free-lesson lead-magnet (try-before-buy); Жанр 10 +list-карусель/employee-side/lime-green; новые жанры 13 (reality-разбор-событие) и 14 (affiliate cross-promo инфобиз-автора).)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (Hooks 4-го среза Якубы: «репутация из мелочей» (trust-as-accumulation), «спокойные продажи сильнее давления», «уверенность звучит тихо» (employee-side boundary), «профессионализм ≠ доступность 24/7», IT-кейс «лид за 1500 ₽» + 3 micro-hooks.)
  - wiki/canon/marketing-frameworks/trust-as-managed-asset-coin-principle.md (Новая секция trust-as-accumulation: carousel «5 привычек, которым доверяют деньги» как bottom-up формирование монеты + «репутация собирается из мелких действий».)
  - wiki/canon/marketing-frameworks/first-15-sec-sales-contact.md (Concrete-case (6871): IT-компания, лид за 1500 ₽ слит за секунды («я посмотрю на сайте / хорошо, до свидания»), incentive-design root cause.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 4, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_vyakuba_20260519-122309.md + 20 children (4 video mp4 + 16 media jpg, + sidecars) → processed

## [2026-05-23 23:40] [ingest] | hr-portal.ru — «Ротация как развитие персонала» (evergreen textbook; career-stage timing model как scaffold + Hook 37 employee-side reframe)
- source: wiki/sources/2026-05-19-web-hr-portal-rotaciya-razvitie-personala.md
- created:
  - wiki/canon/marketing-frameworks/rotation-career-stage-timing-model.md
- updated:
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (+Hook 37 «Горизонтальный рост = развитие, не понижение» (hr-portal.ru ротация, employee-side reframe); +funnel-mapping row; +2 source/related cross-links.)
  - wiki/evolving/content-trends/hr-portal-evergreen-genre-2026.md (+2-й экземпляр жанра в выборке (ротация) → подтверждение всех маркеров + первый случай textbook-scaffold, вынесенного в canon; +career-development content-angle; +source.)
  - wiki/canon/marketing-frameworks/career-growth-decoupling-rybakov.md (+секция «Классическая рамка, от которой произошёл декаплинг» с cross-link на rotation-career-stage-timing-model как доцифровой baseline.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_rotaciya-kak-sredstvo-razvitiya-personala_18336beb.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 23:40] [ingest] | hr-portal.ru — «Конфликты в организациях» (конфликтология Шейнова → canon-фрейм organizational-conflict-taxonomy; backfill genre+Сегмент2; triage uncertain→разрешён вручную)
- source: wiki/sources/2026-05-19-web-hr-portal-konflikty-v-organizaciyah.md
- created:
  - wiki/canon/marketing-frameworks/organizational-conflict-taxonomy-sheinov.md
- updated:
  - wiki/canon/marketing-frameworks/thomas-kilmann-conflict-strategies.md (+cross-ref на комплементарную организационную рамку (taxonomy-sheinov): TK = как реагировать, та = типы/причины/профилактика; +source.)
  - wiki/evolving/content-trends/hr-portal-evergreen-genre-2026.md (+3-е подтверждение жанра, новый management/textbook-подтип (конфликтология) поверх процедурных how-to; числа без attribution как маркер; 2-й слой SEO-арбитража (management-запросы).)
  - wiki/canon/target-audience/gro-segments.md (+content-angle «первые конфликты в команде» Сегменту 2 (founder→manager): рефрейминг текучка/бунт = несовершенство системы, не плохие люди.)
  - wiki/canon/marketing-frameworks/management-styles-2026-soulful.md (+cross-ref на conflict-taxonomy: ситуативный стиль как практический ответ на conflict-prevention.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_konflikty-v-organizaciyah_ef82f6ba.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 23:55] [ingest] | hr-portal.ru — «Повышаем работоспособность сотрудников» (work-capacity ритмы + 6 рычагов → новый ритмический content-register productivity angle)
- source: wiki/sources/2026-05-19-web-hr-portal-povyshaem-rabotosposobnost-sotrudnikov.md
- created:
  - wiki/canon/marketing-frameworks/work-capacity-rhythms-textbook.md
- updated:
  - wiki/evolving/product-reception/gro-productivity-energy-angle.md (+7-й (ритмический/хронобиологический) регистр content-mix: ось «когда что делать» (10:00 пик / среда-провал), reframe усталости как нормы ритма, готовые календарно-привязанные hooks.)
  - wiki/evolving/content-trends/hr-portal-evergreen-genre-2026.md (+жанровая вариация author-persona («работаю менеджером по персоналу») — частичное нарушение маркера анонимности; уточнение, что hr-portal использует две под-формы evergreen (чистая анонимная + author-persona); genre-content overlap с productivity angle.)
  - wiki/evolving/industry-trends/cognitive-wellness-shift-2026.md (+«бумажный» предшественник тренда: work-capacity textbook оперирует теми же факторами (внимание/утомление/восстановление) в до-нейротеховой подаче; аргумент дифференциации GRO vs hardware (Neiry).)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (+6 рычагов работоспособности как employer-side зеркало consumer-self-management хуков; reframe «сколько рычагов вы применяете к себе» как мост leadership↔self-management.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 3, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_hr-portal.ru_article_povyshaem-rabotosposobnost-sotrudnikov_b6a4b0bf.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 23:55] [ingest] | vc.ru/hr — «Удалённая работа в Пензе» (programmatic geo-SEO листикл-воронка: новый 4-й RU-SEO-архетип + worker-side geo-arbitrage спрос на удалёнку)
- source: wiki/sources/2026-05-19-vcru-hr-udalennaya-rabota-v-penze.md
- created:
  - wiki/evolving/content-trends/geo-templated-local-seo-listicle-funnel-2026.md
- updated:
  - wiki/evolving/content-trends/vcru-hr-content-patterns-2026.md (+Паттерн 5 (geo-шаблонный local-SEO листикл-воронка) + строка переносимости + импликация «vc.ru/hr не однородно-экспертная площадка».)
  - wiki/evolving/industry-trends/return-to-office-global-2026.md (+секция worker-side: устойчивый региональный geo-arbitrage-спрос на удалёнку (противофаза корпоративному RTO), content-farm-ниша как индикатор спроса.)
  - wiki/canon/target-audience/gro-segments.md (+региональный geo-arbitrage под-портрет Сегмента 1 (удалёнка вне столиц, «столичные доходы при региональных расходах»).)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, canon: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_vc.ru_hr_2808612-udalennaya-rabota-v-penze-vakansii-i-sovety_165c0c33.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-19 15:10] [ingest] | vc.ru/hr (репост колонки для «Коммерсанта») — тренды рынка труда 2026: технологии-инфраструктура + pay-for-results + навыки-комбинации + усложнение роли > смена профессии + РШУ 48% выгорания
- source: wiki/sources/2026-05-19-vcru-hr-kommersant-trendy-rynka-truda-2026.md
- created: none
- updated:
  - wiki/evolving/industry-trends/ru-labor-market-employer-turn-2026.md (+8-й голос (vc.ru/hr колонка для Коммерсанта): технологии как инфраструктура рекрутинга, pay-for-results (вознаграждение привязано к результату, фикс не растёт), усложнение роли > смена профессии, hh весна −25%/+33% триангуляция; +3 cross-link, +source.)
  - wiki/evolving-strict/market-data/employee-engagement-quiet-quitting-2026.md (+РШУ конец 2025: 48% работающих россиян с симптомами выгорания (3-й независимый RU-якорь после hh 42%/33%) [conf:medium, src:2026-05-19]; +leadership-energy как критерий найма (эмоциональное отключение руководителей); +source.)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (+Hook 38 «Резюме читает робот раньше человека: цифры > отвечал за» (machine-readable резюме, прескриптивный угол к ATS-коллапсу); +Hook 39 «Не меняй профессию — усложняй роль» (anti-anxiety reframe); funnel-map + 3 cross-link + source.)
  - wiki/evolving/industry-trends/skill-based-hiring-russia-2026.md (+навыки-комбинации как новая норма работодателя (vc.ru/hr колонка): «не профессия вообще, а набор навыков под задачу» (инженерия+цифра, аналитика+коммуникация); demand-side формулировка навыкоцентричности; +2 cross-link, +source.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_vc.ru_hr_2808318-trendy-rynka-truda-v-2026-godu_ea184c98.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-19 15:10] [ingest] | vc.ru/hr — смена профессии банкир→финдир через предпринимательство (личный нарратив verified-финансиста): новый career-bridge архетип + proactive trend-watching методология
- source: wiki/sources/2026-05-19-vc-ru-hr-smena-professii-bankir-findir.md
- created:
  - wiki/evolving/content-trends/career-change-via-entrepreneurship-bridge-hooks.md
  - wiki/canon/marketing-frameworks/proactive-career-risk-management-trend-watching.md
- updated:
  - wiki/evolving/content-trends/late-starter-founder-narrative-hooks.md (+смежный архетип career-bridge (предпринимательство как мост, а не финал) + cross-links + source.)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (+Hook 38 «Настроить парус заранее: уходи из профессии до её сжатия» (финдир vc.ru/hr) с inline-маркером + cross-links + source.)
  - wiki/evolving/content-trends/ru-expat-founder-narrative-hooks.md (+под-архетип 5 «bootstrap через стартап-визу» (NL-консалтинг финансиста, relocate-for-job → founder на месте) + cross-links + source.)
  - wiki/canon/marketing-frameworks/entrepreneur-manager-mode-switching.md (+эмпирическая иллюстрация тренируемости режимов (предпринимательство как тренажёр проактивного режима, финансист) + cross-links + source.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 3, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/web_vc.ru_hr_2808290-smena-professii-ot-bankira-k-finansovomu-direktor_460eb590.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 23:55] [ingest] | vc.ru/hr — «Удалённая работа в Кемерово» (программатик гео-SEO content-farm): новый жанр площадки + trust-фреймворк вакансий + региональный leverage удалёнки
- source: wiki/sources/2026-05-19-vcru-hr-remote-work-kemerovo-city-seo-listicle.md
- created:
  - wiki/evolving/content-trends/local-seo-city-vacancy-content-farm-2026.md
- updated:
  - wiki/evolving/content-trends/vcru-hr-content-patterns-2026.md (+Паттерн 5 (программатик гео-city content-farm) + строка в таблице переносимости (anti-pattern для GRO) + cross-link на отдельный разбор и exemplar.)
  - wiki/evolving/industry-trends/ru-recruitment-fraud-patterns-2026.md (+Pattern 3 (классическая «pay-before-work» семья для entry-level remote) + раздел «Позитивные сигналы легитимности» (зеркало red-flag-чеклиста) + 2 cross-link.)
  - wiki/evolving/industry-trends/return-to-office-global-2026.md (+раздел «Demand-side persistence — региональный leverage удалёнки»: employer-side RTO не убил соискательский спрос на «удалёнку из {город}»; honest-angle для GRO Сегментам 1+3; +2 cross-link.)
  - wiki/canon/target-audience/gro-segments.md (+content-angle «региональный удалёнщик» (Сегменты 1+3) + «trust-фреймворк как honest content» (entry-level); +source; +3 cross-link.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 4, canon: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_vc.ru_hr_2808609-udalennaya-rabota-v-kemerovo-vakansii-na-domu-i-o_56dee405.md (+ 2 sidecars: .note.md, .triage.json)

## [2026-05-23 23:58] [ingest] | vc.ru/hr — чайка-менеджмент (seagull management): анти-паттерн + employee survival-playbook + owner-side системный корень (кейс-разбор видео, доцент МГТУ Баумана)
- source: wiki/sources/2026-05-19-vcru-hr-seagull-management-case.md
- created:
  - wiki/canon/marketing-frameworks/seagull-management-survival-playbook.md
- updated:
  - wiki/evolving/content-trends/founder-expert-hook-family-vcru.md (+третий инстанс Паттерна 2 (тот же автор-доцент МГТУ): кейс-разбор видео «чайка-менеджмент» → формат серийный; новый жанр «3-в-1» (концепт→playbook→учебные задания) для длинной SEO-статьи.)
  - wiki/evolving/content-trends/owner-escape-operations-hooks.md (+owner-side зеркало «чайка-менеджмент»: хуки «без системы прилёты обесцениваются», «хаос-как-инструмент = ловушка владельца», double-bind как anti-hook для GRO tone.)
  - wiki/evolving/content-trends/career-audience-hooks-2026.md (+Hook 38 «Начальник-чайка: 5 ошибок + survival» (employee-side, Сегмент 1) + строка в funnel-таблице; reframe «хаос как тренажёр», «выживают самые структурные».)
  - wiki/canon/target-audience/gro-segments.md (+employee-side angle «выживание у трудного руководителя» Сегменту 1 + owner-side angle «owner как чайка» Сегменту 2 (vc.ru/hr чайка-менеджмент).)
  - wiki/canon/marketing-frameworks/management-styles-2026-soulful.md (+cross-ref на эмпирический vc.ru-кейс авторитарного режима как «типового поведения» (чайка-менеджмент).)
  - wiki/canon/marketing-frameworks/cry-as-cheap-system-crutch-soulful.md (+cross-ref на vc.ru-кейс той же механики: крик-как-шум без результата, «без системы прилёты обесцениваются».)
  - wiki/canon/marketing-frameworks/management-style-obsolete-6-signals-soulful.md (+cross-ref на vc.ru-кейс сигнала #6 «нет плохих новостей» («боятся сказать правду до увольнения»).)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 3, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/web_vc.ru_hr_2803222-chajka-menedzhment-kak-vyjity-v-khaose-rossijskog_95eaed8d.md (+ 2 sidecars: .note.md, .triage.json) → processed

## [2026-05-24 04:40] [ingest] | condense dp.ru chunk1 (25 статей, 6 релевантных) — туризм СПб + дестинационный маркетинг + «опыт > обещания» + IKEA-Швеция offline-shift + господдержка МСП cross-source
- source: wiki/sources/2026-05-24-condense-dp-ru-chunk1.md
- created:
  - wiki/evolving/industry-trends/ru-domestic-tourism-spb-2026.md
  - wiki/canon/marketing-frameworks/destination-event-marketing-spb-2026.md
  - wiki/canon/marketing-frameworks/lived-experience-over-promises-high-deliberation.md
- updated:
  - wiki/evolving-strict/market-data/ru-msp-state-support-q1-2026.md (+Cross-source подтверждение dp.ru/«Известия» (2-й независимый медиа-носитель тех же Rodionoff-данных) + 2 новых datapoint: федпроект МСП 2025–2030 = 329,5 млрд ₽ (−21% к 2019–2024) + экспертный прогноз «гранты перестанут существовать через 18 месяцев»; +2 source, +caveat-уточнение.)
  - wiki/evolving/industry-trends/ru-offline-retail-decline-2026.md (+Глобальный параллельный сигнал (dp.ru): IKEA впервые за 40+ лет закрывает магазин в Швеции (Бурленге 31 тыс. м²), >20% продаж онлайн, формат-down-size, причина «адаптация к новым моделям покупательского поведения» — снимает аргумент «RU-специфика»; +RU-возврат через товарный знак 2025; +2 source; fix 2 broken links.)
  - wiki/canon/marketing-frameworks/value-for-customer-concept.md (+Секция «Современная RU-иллюстрация (dp.ru 2026)»: «опыт > цена/обещание» как проверка совокупности качеств на длинном горизонте; +cross-links на lived-experience + destination-marketing; +source.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, canon: 3, evolving-strict: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/_condense_dp.ru_chunk1_2026-05-24.md (+ .note.md sidecar); per-article стабы уже существовали в wiki/sources/ (не создавались)

## [2026-05-24 04:50] [ingest] | vc.ru/hr condensed — 30 статей (chunk1): 4-й батч Garmony advertorial + HR Tech рынок РФ + контртренд человечности
- source: wiki/sources/2026-05-24-vcru-hr-condensed-30-articles.md
- created:
  - wiki/evolving-strict/market-data/ru-labor-market-deficit-by-sector-2026.md
  - wiki/canon/marketing-frameworks/persuasion-not-deception-sales-psychology.md
  - wiki/evolving/industry-trends/ai-recruiting-humanity-countertrend-2026.md
- updated:
  - wiki/evolving/competitor-positioning/garmony-ai-advertorial-campaign-2026.md (+4-й батч: «3-е поколение»/«единая экосистема» messaging, таксономия «Класс 1/3», GTM-хуки «5 минут/152-ФЗ из коробки», модульные связки, ROI 810–3186%, time-to-hire кейсы, расширенная карта игроков и цен.)
  - wiki/evolving-strict/market-data/ru-hr-tech-market-size-2026.md (+триангуляция 40,6 млрд +12% H1-2025, adoption-breakdown 44–49% (обучение/рекрутинг/порталы), только 5% «полноценно», глобально 87% / $1,12 млрд к 2030, Gartner 76%, first-response рычаг.)
  - wiki/evolving/industry-trends/ru-hr-tech-ai-landscape-2026.md (+расширенная карта игроков (Naimee/Xenia/Sever.AI/hirehire/AI HR PRO/Empany + HRM-слой), ось эволюции точности keyword→ML→NLP, agentic AI shift, КЭДО как законодательный драйвер.)
  - wiki/evolving/content-trends/vcru-top10-advertorial-pattern-2026.md (+4 тактических конверсионных приёма: «было/стало» в часах, «день из жизни до/после», «реальные кейсы ≠ маркетинг», disclaimer-паттерн для доходных тем.)
  - wiki/canon/target-audience/gro-segments.md (+SMB «ChatGPT лежит мёртвым грузом» adoption-gap pain Сег2 + entry-level «удалёнщики/новички» под-портрет Сег3 (входные роли + мошеннические вакансии).)
  - wiki/evolving/industry-trends/ru-recruitment-fraud-patterns-2026.md (+корроборация Pattern 3 (entry-level remote fraud-маркеры) из второго независимого источника + список входных удалённых ролей.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, evolving-strict: 2, canon: 2, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/_condense_vc.ru_chunk1_2026-05-24.md (+ 1 sidecar: .note.md) → processed

## [2026-05-24 05:05] [ingest] | Condensed vc.ru chunk2 — 30 статей (vc.ru/hr + Спиридонов id79772)
- source: wiki/sources/2026-05-24-condense-vcru-chunk2.md
- created:
  - wiki/canon/marketing-frameworks/productivity-vs-efficiency-mckinsey-spiridonov.md
  - wiki/canon/marketing-frameworks/ai-implementation-5-steps-spiridonov.md
  - wiki/canon/marketing-frameworks/ux-microcopy-craft-avito.md
  - wiki/canon/marketing-frameworks/employee-data-compliance-3-lenses.md
  - wiki/evolving/content-trends/adaptive-quiz-lead-magnet-2026.md
  - wiki/evolving/content-trends/niche-positioning-mechanism-not-symptom-2026.md
  - wiki/evolving/industry-trends/hr-as-media-marketing-convergence-2026.md
- updated:
  - wiki/evolving-strict/market-data/ai-search-commerce-benchmarks-2026.md (+второй Adobe-замер: генеративный чат-бот трафик +1200-1700% YoY US, опрос 39%/53%/92%/87%, поведение +12%/−23% (Спиридонов).)
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md (+Спиридонов RU-voice: чат-бот как точка старта клиентского пути + ambient AI / «смерть смартфона».)
  - wiki/canon/target-audience/senior-employees-50plus-ru-2026.md (+глобальный silver-economy контекст (50+ владеют >50% мировых активов / ~80% US) + ICP-сигнал «50+ как потребитель» для GRO.)
  - wiki/canon/marketing-frameworks/partnerships-growth-multiplier.md (+личная методология партнёрств Спиридонова (4 правила) + channel-pivot Insight Estate Таиланд + Microsoft×OpenAI/Pfizer×BioNTech якоря.)
  - wiki/canon/marketing-frameworks/spiridonov-three-engagement-formats.md (+май-2026 content-cluster: прагматический романтизм, 8 барьеров+resilience-хук, директор по маркетингу личного бренда, вдохновение>инструкция + Deadly Vipers own-platform, диагностика-перед-действием.)
  - wiki/evolving/content-trends/podcast-driven-author-channel-patterns.md (+второй exemplar «Визионеры» Спиридонова: weekly podcast + weekly big-post + monthly curation = multi-cadence engine.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 7, evolving: 5, evolving-strict: 1, sources: 1}
- touched: 14 pages
- raw: raw/processed/articles/_condense_vc.ru_chunk2_2026-05-24.md (+ .note.md sidecar)

## [2026-05-24 05:00] [ingest] | vc.ru chunk3 — авторский блог Максима Спиридонова (30 статей, condensed): бизнес-фреймворки (Метод-5/доверие/амёба/прагматический романтизм) + AI-тренды (плато ИИ-чатботов, венчурный пузырь, гонка гуманоидов) + Reforma
- source: wiki/sources/2026-05-24-vcru-spiridonov-id79772-chunk3-condensed.md
- created:
  - wiki/canon/marketing-frameworks/metod-spiridonova-5-components.md
  - wiki/canon/marketing-frameworks/spiridonov-trust-4-stages-framework.md
  - wiki/canon/marketing-frameworks/amoeba-management-inamori.md
  - wiki/canon/marketing-frameworks/universe-25-corporate-comfort-hook.md
  - wiki/canon/marketing-frameworks/pragmatic-romanticism-positioning.md
  - wiki/evolving/competitor-positioning/reforma-business-club-spiridonov.md
  - wiki/evolving-strict/competitor-metrics/reforma-community-metrics-2026.md
  - wiki/evolving-strict/market-data/ai-startup-valuations-bidding-war-2026.md
  - wiki/evolving/content-trends/ad-shift-woke-to-conservative-giveaway-2026.md
- updated:
  - wiki/evolving/content-trends/dead-internet-theory-counter-trend-2026.md (+demand-side anchors «гонка за объёмом не работает» (Google AI 14%, нейросети цитируют human 82%, термин «слоп») + плато ИИ-чатботов (GPT-5, «ксерокопия с ксерокопии») как опора model-collapse.)
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md (+Сигнал 6 «Битва роботов»: Пекин $20B + фонд $137B, цель лидерства 2027, 90% контроль цепочки поставок, UBTech Geely/Foxconn, триангуляция 36 vs 8 моделей.)
  - wiki/evolving-strict/market-data/humanoid-robot-unit-economics-2024-2050.md (+Morgan Stanley industry-size прогноз ≥$5 трлн к 2050 (industry-якорь рядом с population-якорем ~1 млрд units) + гос-финансирование Пекина $20B/$137B.)
  - wiki/evolving/industry-trends/ai-value-migration-2026.md (+плато ИИ-чатботов (GPT-5) как триггер миграции ценности + «зоны искажённой реальности» на венчуре (bubble-сигнал, reconcile с Горным).)
  - wiki/canon/marketing-frameworks/spiridonov-three-engagement-formats.md (+кросс-линки на содержательное ядро «Метода» (5 компонентов, прагматический романтизм, фреймворк доверия, амёба) + вебинар «о Методе» 16/30 окт как funnel-entry.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving: 5, evolving-strict: 3, sources: 1}
- touched: 15 pages
- raw: raw/processed/articles/_condense_vc.ru_chunk3_2026-05-24.md (+ .note.md sidecar)

## [2026-05-24 05:00] [ingest] | condense vc.ru/T-Bank chunk6 — 30 статей (research-PR + события + дофамин-банкинг + BNPL turnover)
- source: wiki/sources/2026-05-24-condense-vc-ru-tbank-chunk6-30.md
- created:
  - wiki/evolving-strict/market-data/ru-consumer-services-research-pr-2024-2025.md
  - wiki/evolving-strict/market-data/ru-bnpl-business-turnover-effect-2024.md
  - wiki/evolving-strict/campaign-metrics/ru-offline-brand-event-reach-benchmarks-2026.md
  - wiki/evolving/content-trends/research-as-pr-transactional-data-format.md
  - wiki/evolving/competitor-positioning/tbank-dofamin-banking-navigator-2025.md
- updated:
  - wiki/evolving/industry-trends/tbank-corporate-platform-stack-2026.md (Развёрнут раздел «Дофамин-банкинг и AI-UX» (app 7.0, Навигатор, Co-Pilot, Gen-T, 46M, Сферы) + ссылка на отдельную positioning-страницу; +новый раздел research-as-PR и офлайн-события как awareness-каналы; +6 cross-link, +source.)
  - wiki/canon/marketing-frameworks/marketplace-distribution-diversification-5-channels.md (+Empirical lifecycle-case «Много лосося» (Кретов, T-Bank eCommerce): эксклюзив-буст→2-летний потолок→мультиплатформа возобновляет рост; ~7 тыс. бизнесов сделали сайт после маркетплейсов; добавлена временнáя ось фреймворка; +3 cross-link, +source.)
  - wiki/evolving/content-trends/tbank-vc-ru-content-mix-2019-2024.md (+4 cross-link (research-as-PR, event-reach-бенчмарки, дофамин-банкинг positioning, chunk6 source) — детализация edu/research и event-слоёв контент-микса.)
  - wiki/evolving-strict/market-data/ru-bnpl-aov-uplift-2023.md (+Follow-up (2024): AOV +26% развёрнут в business-turnover ×3 + кейс Mollis +53%; forward-link на ru-bnpl-business-turnover-effect-2024; +source.)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 4, evolving: 4, canon: 1, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/_condense_vc.ru_chunk6_2026-05-24.md (+ 1 sidecar: .note.md) → processed

## [2026-05-24 05:05] [ingest] | vc.ru chunk4 condensed (30 статей, 12 extracted) — Спиридонов AI/рынок труда (2023 трек) + brain rot метрики + OpenAI positioning + форекс-экономика + NoCode/152-ФЗ + NIO + FOMO-инвестиции
- source: wiki/sources/2026-05-24-vcru-chunk4-condensed.md
- created:
  - wiki/evolving-strict/market-data/forex-broker-economics-2026.md
  - wiki/canon/marketing-frameworks/niche-content-crowdfunding-breakthrough-kondrashov.md
  - wiki/evolving/industry-trends/nocode-smb-localization-window-2026.md
  - wiki/evolving/competitor-positioning/openai-positioning-shift-nonprofit-commercial.md
- updated:
  - wiki/evolving/industry-trends/ai-replacing-jobs-global-2026.md (+ранний (2023) трек Accenture reskilling >550K + IgniteTech ~80% замена/EBITDA 75% + контр-интуитивный инсайт «сопротивлялись разработчики, не маркетологи» + «человек + ИИ» предшественник sorting-test'а.)
  - wiki/canon/marketing-frameworks/ai-amplifier-fragmented-vs-modular-jobs.md (+ранний (2023) предшественник «человек + ИИ» того же автора (vc.ru id79772_2317994) — 2-летний эмпирический трек фрейма.)
  - wiki/evolving/content-trends/social-media-addiction-design-patterns.md (+quantitative-layer brain rot: 47 сек удержание (vs 2.5 мин 2004), 58 проверок/день, 25 мин на возврат, слово года +230%, «текст >минуты = избыточное усилие», BRS-14 воронка-как-формат.)
  - wiki/evolving/content-trends/fast-content-consumption-shift-2026.md (+второй независимый источник (vc.ru brain rot): 47 сек удержание, «текст >минуты = усилие» — поднял базовый demand-side тезис до confidence medium.)
  - wiki/canon/marketing-frameworks/housel-psychology-of-money-spiridonov.md (+FOMO/зависть companion-тезис (vc.ru «Уроки Ньютона» 2023): зависть>жадность, «в этот раз по-другому» антипаттерн, Компания Южных морей 1720 как воспроизводимый паттерн пузырей.)
  - wiki/evolving/industry-trends/china-ai-manufacturing-momentum-2026.md (+Сигнал 6: NIO премиум-EV референс (150+ брендов, станции замены батарей ~3 мин) + сервисный сегмент аудита китайских поставщиков для RU-брендов («сервисная экономика»).)
  - wiki/evolving/content-trends/community-monthly-recap-digest-format-2026.md (+смежный author-channel вариант «топ публикаций месяца» (Спиридонов) как сериализованный месячный retention-формат + охватные темы-референсы для контент-плана.)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 3, evolving: 6, evolving-strict: 1, sources: 1}
- touched: 12 pages
- raw: raw/processed/articles/_condense_vc.ru_chunk4_2026-05-24.md (+ 1 sidecar: .note.md)

## [2026-05-24 05:10] [ingest] | vc.ru chunk5 condensed (30 статей, 16 extracted) — reusable рамки vc.ru/story (диагностика процесса / sunk-cost / survivorship / цена-уважение / recognition-economy / JIT-обучение / personal-brand-устойчивость / founder-risk Yeezy) + контент-паттерны (evergreen-сторителлинг + AI-backlash / deep-context / Adidas-Puma эндорс / VFX-крафт) + Т-Банк (DNPL Благо Долями / антифрод / Умная камера / employer-brand Tinkoff Space) + market-data (благотворительность РФ / провал метавселенных)
- source: wiki/sources/2026-05-24-condense-vcru-chunk5.md
- created:
  - wiki/canon/marketing-frameworks/process-deconstruction-three-questions.md
  - wiki/canon/marketing-frameworks/unverifiable-product-sunk-cost-persuasion.md
  - wiki/canon/marketing-frameworks/survivorship-bias-marketing-wald.md
  - wiki/canon/marketing-frameworks/pricing-as-self-respect-anti-discount-trap.md
  - wiki/canon/marketing-frameworks/recognition-economy-non-material-motivation.md
  - wiki/canon/marketing-frameworks/microlearning-jit-in-flow-of-work.md
  - wiki/canon/marketing-frameworks/personal-brand-resilience-vs-hype-angle.md
  - wiki/canon/positioning/founder-led-brand-fragility-yeezy.md
  - wiki/evolving/content-trends/vcru-story-evergreen-storytelling-genre.md
  - wiki/evolving/content-trends/deep-context-cultural-philosophy-content.md
  - wiki/evolving/content-trends/sport-brand-history-endorsement-origins.md
  - wiki/evolving/content-trends/expert-vfx-craft-content-quality-criteria.md
  - wiki/evolving/competitor-positioning/tbank-brand-journalism-employer-storytelling.md
  - wiki/evolving/product-reception/meta-horizon-worlds-metaverse-failure.md
  - wiki/evolving-strict/market-data/ru-charity-giving-market-tinkoff-2023.md
  - wiki/evolving-strict/market-data/metaverse-vr-market-decline-2024-2026.md
  - wiki/evolving-strict/product-metrics/tbank-smart-camera-product-metrics.md
  - wiki/evolving-strict/campaign-metrics/tbank-antifraud-service-metrics.md
  - wiki/volatile-strict/competitor-news/tbank-blago-dolyami-dnpl-launch-2026.md
  - wiki/volatile-strict/competitor-news/tbank-fraud-scenario-hybrid-firstperson-content.md
  - wiki/canon/target-audience/recruitment-pr-marketing-worker-side-signals.md
- updated:
  - wiki/evolving/content-trends/tbank-vc-ru-content-mix-2019-2024.md (+cross-link на новую страницу форматных механик бренд-журналистики/employer-storytelling Т-Банка (chunk5).)
  - wiki/canon/marketing-frameworks/employee-intrinsic-demotivation-6-factors.md (+cross-link на recognition-economy (горизонтальная экономика признания адресует факторы #4 непричастность и #6 отсутствие признания).)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 9, evolving: 6, evolving-strict: 4, volatile-strict: 2, sources: 1}
- touched: 23 pages
- raw: raw/processed/articles/_condense_vc.ru_chunk5_2026-05-24.md (+ 1 sidecar: .note.md)

## [2026-05-27 15:10] [ingest] | Forbes.ru — тег «200 крупнейших непубличных компаний» (triaged-out, audit-only)
- source: wiki/sources/2026-05-26-forbes-tag-200-largest-private-companies.md
- created: none (audit-only ingest, теги-страница без релевантного контента)
- updated: none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 page
- raw: raw/processed/articles/web_www.forbes.ru_tegi_200-krupneyshih-nepublichnyh-kompaniy_9a52e3ae.md → processed

## [2026-05-27 15:14] [ingest] | Telegram @community_tech (Воронин/«Атланты») — тизер #992 «Атланты Сити»
- source: wiki/sources/2026-05-26-tg-community-tech-atlanty-city-ooh-992.md
- created: none
- updated:
  - wiki/volatile/weekly-digest/voronin-community-tech-feb-apr-2026.md (+тизер #992, 9-канальный event-marketing микс расширен наблюдением tease-and-reveal формата)
  - wiki/evolving/competitor-positioning/atlanty-business-club-positioning-2026.md (+OOH-наблюдение «Атланты Сити» как новый продуктовый трек клуба)
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1, volatile: 1, evolving: 1}
- touched: 3 pages
- raw: raw/processed/articles/tg_community_tech_20260526-134000.md → processed (+ 1 child media)

## [2026-05-27 15:18] [ingest] | TG @typicalcompany — посты 1340-1341 (25 мая 2026): «рефлексы изменений»
- source: wiki/sources/2026-05-26-tg-typicalcompany-may-25-2026-change-reflexes.md
- created:
  - wiki/canon/marketing-frameworks/change-reflexes-velonski-gartner.md
- updated:
  - wiki/evolving/competitor-positioning/typical-company.md (+трек «рефлексы изменений» как новый продуктовый ракурс TYPICAL)
  - wiki/canon/marketing-frameworks/change-management-tuckman-kotter-ramazanov.md (+рефлексы Велонски-Gartner как дополняющий уровень change-management)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 1, sources: 1}
- touched: 3 pages
- raw: raw/processed/articles/tg_typicalcompany_20260526-010500.md → processed

## [2026-05-27 15:22] [ingest] | Дзен (Деловой мир) / Артем Первухин (KINETICA) — Performance: 5 течей воронки
- source: wiki/sources/2026-05-26-dzen-delovoymir-pervukhin-funnel-5-leaks.md
- created:
  - wiki/canon/marketing-frameworks/pervukhin-funnel-5-leaks-diagnostic.md
  - wiki/canon/marketing-frameworks/niche-dynamics-vs-self-comparison-benchmark.md
  - wiki/canon/marketing-frameworks/value-based-bidding-vs-lead-cost.md
  - wiki/canon/marketing-frameworks/algorithm-training-conversion-action-selection.md
  - wiki/evolving-strict/campaign-metrics/kinetica-funnel-optimization-cases-2025.md
- updated:
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md (+кейсы KINETICA с inline-маркерами по 2025)
  - wiki/canon/marketing-frameworks/neuroslop-era-performance-marketing-shift-tabunov.md (+5 течей как операционная разбивка performance-сдвига)
  - wiki/canon/marketing-frameworks/cpa-calculator-pre-launch-roi.md (+связка с диагностикой 5 течей)
  - wiki/canon/marketing-frameworks/site-speed-as-conversion-lever.md (+перекрёстная связь с течью «техники сайта»)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving-strict: 2, sources: 1}
- touched: 10 pages
- raw: raw/processed/articles/web_dzen.ru_a_ahQEAFU4_3gzT96R_72be4f38.md → processed

## [2026-05-27 15:23] [ingest] | Telegram @portnyaginlive — 3 поста (бизнес с друзьями, формула Эйнштейна, история 7-Eleven)
- source: wiki/sources/2026-05-26-tg-portnyaginlive-20260526-122652.md
- created:
  - wiki/canon/marketing-frameworks/partner-as-leadership-role-portnyagin.md
  - wiki/canon/marketing-frameworks/einstein-success-formula-silence-as-control.md
  - wiki/canon-strict/historical-campaigns/seven-eleven-suzuki-takeover-1991-2026.md
- updated:
  - wiki/canon/marketing-frameworks/partner-strength-over-idea-batyrev.md (+Портнягин-голос: партнёр > идея, фокус на лидерскую роль)
  - wiki/canon/marketing-frameworks/distressed-asset-consolidation-playbook.md (+7-Eleven/Сузуки 1991 как 5-й кейс playbook'а distressed-takeover)
  - wiki/canon-strict/historical-campaigns/samwer-rocket-internet-fast-follower.md (+ cross-link 7-Eleven как контр-кейс «fast-follower vs distressed-takeover»)
  - wiki/evolving/content-trends/portnyagin-founder-channel-patterns.md (+3-постовый срез: партнёрство/формула/история, формат «лонгрид→цитата→исторический разбор»)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, canon-strict: 1, evolving: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_portnyaginlive_20260526-122652.md → processed (+ 3 child media)

## [2026-05-27 15:36] [ingest] | Forbes.ru tag-page «30 under 30» — 15 заголовков, агрегированный срез
- source: wiki/sources/2026-05-26-forbes-tegi-30-under-30.md
- created:
  - wiki/evolving/content-trends/forbes-30-under-30-content-franchise.md
- updated:
  - wiki/evolving/content-trends/hiring-meme-pricing-list-tabunov.md (+Forbes 30 under 30 как listicle-эталон с социальным капиталом)
  - wiki/canon/marketing-frameworks/social-proof-traffic-asset-framework-tabunov.md (+«30 under 30» как 9-й тип pre-validated social proof)
  - wiki/evolving/content-trends/forbes-russia-native-ad-pattern-2026.md (+тег-страница как эволюция native-формата Forbes RU)
  - wiki/evolving-strict/market-data/ru-youth-entrepreneurs-2026.md (+15 имён за 2024-2026, отраслевое распределение)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, canon: 1, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/web_www.forbes.ru_tegi_30-under-30_49015bc9.md → processed

## [2026-05-27 15:42] [ingest] | Telegram @fomichevkirill — дамп канала, 20–26 мая 2026 (7 содержательных постов)
- source: wiki/sources/2026-05-26-tg-fomichevkirill-may-20-26-2026.md
- created:
  - wiki/canon/marketing-frameworks/agreement-fixation-discipline-fomichev.md
  - wiki/evolving-strict/competitor-metrics/dome-foundation-investment-fund-2026.md
  - wiki/evolving/competitor-positioning/zarya-ventures-hr-tech-investor-2026.md
  - wiki/evolving/industry-trends/closed-vc-camp-format-spring-ai-weekend-2026.md
- updated:
  - wiki/evolving/content-trends/sponsored-author-channel-monetization-fomichev.md (+рубрика «Коннект» + новые spons. интеграции, май-срез)
  - wiki/canon/marketing-frameworks/sales-follow-up-second-touch-fomichev.md (+«фиксация договорённостей» как продление дисциплины follow-up'а)
  - wiki/evolving-strict/market-data/publishing-founder-growth-premium-2026.md (+Фомичёв 4-й голос «премии за публичность founder'а», май срез)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 2, evolving-strict: 2, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_fomichevkirill_20260526-130502.md → processed (+ 6 child media)

## [2026-05-27 15:42] [ingest] | Дзен (Деловой мир) / Артем Первухин (KINETICA) — Brand vs Performance: two-track стратегия
- source: wiki/sources/2026-05-27-dzen-delovoymir-pervukhin-brand-vs-performance.md
- created:
  - wiki/canon/marketing-frameworks/brand-vs-performance-two-track-strategy-pervukhin.md
  - wiki/canon/marketing-frameworks/share-of-search-brand-metric.md
  - wiki/canon/marketing-frameworks/brand-lift-measurement-by-platform.md
  - wiki/canon/marketing-frameworks/assisted-conversions-attribution-3-models.md
  - wiki/canon/marketing-frameworks/brand-sprint-testing-quarterly-three-iterations.md
  - wiki/evolving-strict/campaign-metrics/brand-investment-timeline-benchmarks.md
- updated:
  - wiki/canon/marketing-frameworks/three-tier-funnel-budget-split-vtochku.md (+ two-track как стратегическая надстройка над 50/30/20 split)
  - wiki/canon/marketing-frameworks/neuroslop-era-performance-marketing-shift-tabunov.md (+ brand-капитал как контр-ход neuroslop'у performance-эры)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving-strict: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/web_dzen.ru_a_ahQVE3M-KU9rtjGg_28255071.md → processed

## [2026-05-27 15:43] [ingest] | Telegram @psilonsk — дамп 2026-05-20…2026-05-26 (Сергей Колганов, week4)
- source: wiki/sources/2026-05-26-tg-psilonsk-may-2026-week4.md
- created:
  - wiki/canon/marketing-frameworks/work-life-boundary-monitor-not-intervene.md
  - wiki/canon/marketing-frameworks/kill-half-working-projects-courage.md
  - wiki/canon/marketing-frameworks/legal-led-company-antipattern.md
  - wiki/canon/marketing-frameworks/meeting-time-filling-parkinsons-antipattern.md
  - wiki/canon/marketing-frameworks/consultant-as-discipline-enforcer.md
- updated:
  - wiki/evolving/content-trends/psilonsk-management-hooks-bank.md (+5 новых хуков-фреймов week4, расширение банка для блога GRO)
  - wiki/evolving/content-trends/psilonsk-channel-patterns.md (+week4 как 4-й observed-срез, паттерн 3-рубричного цикла стабилен)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 5, evolving: 2, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_psilonsk_20260526-131002.md → processed (+ 5 child media)

## [2026-05-27 15:56] [ingest] | Telegram @cossaru — дайджест 19–25 мая 2026 (50 постов)
- source: wiki/sources/2026-05-26-tg-cossaru-may-19-25-2026.md
- created:
  - wiki/canon/marketing-frameworks/germ-generative-engine-reputation-management.md
  - wiki/canon/marketing-frameworks/igc-influencer-generated-content-taxonomy.md
  - wiki/canon/marketing-frameworks/dsp-programmatic-incrementality-bidease.md
  - wiki/canon/marketing-frameworks/psychographic-design-4-types-opencore.md
  - wiki/canon/marketing-frameworks/utp-content-format-azbuka-ishmysh.md
  - wiki/canon/marketing-frameworks/audience-feedback-content-strategy-pivot-ishmysh.md
  - wiki/evolving-strict/market-data/ipsos-ai-shopping-agents-us-2026.md
  - wiki/evolving-strict/market-data/on24-webinar-engagement-benchmarks-2025.md
  - wiki/evolving-strict/market-data/apptica-ru-mobile-creatives-q1-2026.md
  - wiki/evolving/industry-trends/sms-b2b-infrastructure-channel-2026.md
  - wiki/evolving/content-trends/postmarketing-ugovorite-malchika-show-format.md
  - wiki/volatile-strict/industry-news/meta-layoffs-8000-may-2026.md
  - wiki/volatile-strict/industry-news/yandex-direct-max-messenger-ads-beta-2026-05.md
- updated:
  - wiki/evolving-strict/market-data/digital-ad-market-ru-2024-2026.md (+Apptica/Bidease/ОРД-Тензор данные Q1 2026)
  - wiki/evolving/competitor-positioning/max-messenger.md (+Яндекс Директ MAX-Messenger beta как новый рекламный inventory)
  - wiki/canon/marketing-frameworks/ai-skills-vs-prompts-architecture.md (+Cossa подтверждает skills>prompts парадигму)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 6, evolving: 1, evolving-strict: 3, volatile-strict: 2, sources: 1}
- touched: 16 pages
- raw: raw/processed/articles/tg_cossaru_20260526-112013.md → processed (+ 49 child media)

## [2026-05-28 22:40] [ingest] | RuStore (featuring) — PhotoGen: AI Image 2 (профиль AI-генератора фото/видео)
- source: wiki/sources/2026-05-26-rustore-photogen-ai-image-2.md
- created:
  - wiki/evolving/competitor-positioning/photogen-ai-image-2-rustore-2026.md
  - wiki/canon/marketing-frameworks/coin-credit-freemium-monetization-mobile-ai.md
- updated:
  - wiki/evolving/industry-trends/ai-generated-creatives-in-advertising.md (backfill из PhotoGen RuStore-профиля)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving: 2, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_www.rustore.ru_catalog_featuring_0a2b8d26-62a7-41c8-b95c-f30dfb77a302_029601da.md → processed

## [2026-05-28 22:43] [ingest] | Telegram @telega_Rinata — дамп 2026-05-19…2026-05-22 (Ринат Алиев, AI-трансформация + Big Tech)
- source: wiki/sources/2026-05-26-tg-telega-rinata-may-19-22-2026.md
- created:
  - wiki/canon/marketing-frameworks/ai-performance-review-5-level-ladder.md
  - wiki/canon/marketing-frameworks/ai-transformation-by-company-size-aliev.md
- updated:
  - wiki/evolving/competitor-positioning/ru-nocode-ai-agent-platforms-2026.md (backfill из @telega_Rinata)
  - wiki/canon/marketing-frameworks/poc-first-enterprise-adoption-just-ai.md (backfill из @telega_Rinata)
  - wiki/volatile-strict/competitor-news/anthropic-karpathy-join-2026-05.md (backfill из @telega_Rinata)
  - wiki/volatile-strict/industry-news/meta-layoffs-8000-may-2026.md (backfill из @telega_Rinata)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 1, volatile-strict: 2, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_telega_Rinata_20260526-133009.md → processed (+ 2 child media; 1 missing child: video/tg_telega_Rinata_628.mp4)

## [2026-05-28 22:44] [ingest] | Telegram @techno_yandex — 20–25 мая 2026 (25 постов + 24 медиа)
- source: wiki/sources/2026-05-26-tg-techno-yandex-may-20-25-2026.md
- created:
  - wiki/canon/marketing-frameworks/few-shot-vs-zero-shot-prompting.md
  - wiki/canon/marketing-frameworks/bm25-hybrid-search-ranking.md
  - wiki/evolving/content-trends/ai-image-detection-perspective-geometry-2026.md
  - wiki/evolving/competitor-positioning/alice-ai-art-cyrillic-architecture-2026.md
  - wiki/evolving/industry-trends/ai-in-gamedev-debate-2026.md
  - wiki/volatile-strict/industry-news/higgsfield-hell-grind-cannes-2026-05.md
  - wiki/volatile-strict/competitor-news/spotify-universal-ai-remixes-2026-05.md
- updated:
  - wiki/volatile-strict/competitor-news/google-gemini-3-5-flash-launch-2026-05.md (backfill из @techno_yandex)
  - wiki/volatile-strict/competitor-news/google-gemini-omni-video-2026-05.md (backfill из @techno_yandex)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 2, evolving: 2, volatile-strict: 3, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_techno_yandex_20260526-140419.md → processed (+ 24 child media; 3 missing children: video/tg_techno_yandex_5266.mp4, video/tg_techno_yandex_5270.mp4, video/tg_techno_yandex_5271.mp4)

## [2026-05-28 22:45] [ingest] | Telegram @temno (Аркадий Морейнис) — дамп 20–26 мая 2026 (12 постов «Тренд дня»)
- source: wiki/sources/2026-05-26-tg-temno-moreynis-may-20-26-2026.md
- created:
  - wiki/canon/marketing-frameworks/minimum-viable-promotion-moreynis.md
  - wiki/canon/marketing-frameworks/make-what-people-dont-want-yet-moreynis.md
  - wiki/canon/marketing-frameworks/breakthrough-where-progress-stalled-moreynis.md
  - wiki/canon/marketing-frameworks/necessity-over-demand-moreynis.md
  - wiki/canon/marketing-frameworks/reward-in-process-motivation-moreynis.md
  - wiki/canon/marketing-frameworks/rising-tide-market-timing-moreynis.md
- updated:
  - wiki/canon/marketing-frameworks/latent-demand-ai-startup-search-moreynis.md (backfill из @temno май-среза)
  - wiki/canon/marketing-frameworks/real-time-personalization-cvm-mechanics.md (backfill из @temno май-среза)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 8, sources: 1}
- touched: 9 pages
- raw: raw/processed/articles/tg_temno_20260526-122654.md → processed (+ 12 child media)

## [2026-05-28 22:45] [ingest] | Telegram @vcnews — дайджест 14–18 мая 2026 (50 постов, 47 медиа)
- source: wiki/sources/2026-05-26-tg-vcnews-may-14-18-2026.md
- created:
  - wiki/evolving/content-trends/sony-xperia-ai-photo-pr-fail-2026.md
  - wiki/evolving/content-trends/heinz-nhl-jersey-napkin-stunt-2026.md
  - wiki/evolving/content-trends/nintendo-pokemon-airport-ip-placemaking-2026.md
  - wiki/volatile-strict/industry-news/microsoft-forces-copilot-over-claude-code-2026-05.md
- updated:
  - wiki/evolving-strict/market-data/kantar-brandz-2026-most-valuable.md (backfill из @vcnews)
  - wiki/evolving/content-trends/swatch-ap-royal-pop-hype-mismatch-2026.md (backfill из @vcnews)
  - wiki/canon/marketing-frameworks/newsjacking-technique.md (backfill из @vcnews)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 5, volatile-strict: 1, evolving-strict: 1, canon: 1, sources: 1}
- touched: 8 pages
- raw: raw/processed/articles/tg_vcnews_20260526-102155.md → processed (+ 47 child media; 7 missing children: video/tg_vcnews_61394.mp4, 61401, 61402, 61403, 61404, 61408, 61409)

## [2026-05-28 22:49] [ingest] | Forbes.ru — тег «3D-печать» (landing scrape, нерелевантно)
- source: wiki/sources/2026-05-26-forbes-tegi-3d-pechat.md
- created:
  - none
- updated:
  - none
- superseded: none
- sensitive flag: none
- layer-touched: {sources: 1}
- touched: 1 page (audit-only, нерелевантный источник)
- raw: raw/processed/articles/web_www.forbes.ru_tegi_3d-pechat-0_c63b4608.md → processed

## [2026-05-28 22:50] [ingest] | Forbes.ru — тег «безалкогольные напитки» (подборка новостей, май 2026)
- source: wiki/sources/2026-05-26-forbes-bezalkogolnye-napitki-tag.md
- created:
  - wiki/evolving/industry-trends/ru-non-alcoholic-beverages-market-2026.md
  - wiki/evolving-strict/market-data/ru-non-alcoholic-beverages-2026.md
  - wiki/evolving/content-trends/forbes-founder-bet-narrative-format.md
- updated:
  - none
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 2, evolving-strict: 1, sources: 1}
- touched: 4 pages
- raw: raw/processed/articles/web_www.forbes.ru_tegi_bezalkogol-nye-napitki_1bb02eda.md → processed

## [2026-05-28 22:53] [ingest] | Telegram @vyakuba — дамп 20–26 мая 2026 (5-й срез, Владимир Якуба)
- source: wiki/sources/2026-05-26-tg-vyakuba-may-20-26-2026.md
- created:
  - wiki/canon/marketing-frameworks/sale-begins-after-price-vyakuba.md
  - wiki/canon/marketing-frameworks/summer-counter-cyclical-sales-vyakuba.md
  - wiki/canon/marketing-frameworks/service-as-removed-friction-automation-paradox-vyakuba.md
  - wiki/canon/marketing-frameworks/secret-shopper-sales-diagnostic-vyakuba.md
- updated:
  - wiki/evolving/content-trends/ru-sales-infobiz-content-patterns.md (backfill из @vyakuba 5-го среза)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 4, evolving: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/tg_vyakuba_20260526-123152.md → processed (+ 19 child media; 8 missing children: video/tg_vyakuba_6884.mp4, 6886, 6887, 6889, 6892, 6896, 6897, 6909)

## [2026-05-28 22:55] [ingest] | Telegram @techsparks (Себрант) — дайджест 19–25 мая 2026 (10 постов)
- source: wiki/sources/2026-05-26-tg-techsparks-may-19-25-2026.md
- created:
  - none
- updated:
  - wiki/evolving/industry-trends/ai-search-aeo-geo-2026.md (backfill из @techsparks)
  - wiki/evolving-strict/market-data/ai-search-commerce-benchmarks-2026.md (backfill из @techsparks)
  - wiki/evolving/industry-trends/hollywood-ai-institutional-shift-2026.md (backfill из @techsparks)
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (backfill из @techsparks)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving: 3, evolving-strict: 1, sources: 1}
- touched: 5 pages
- raw: raw/processed/articles/tg_techsparks_20260526-142011.md → processed (+ 9 child media; 1 missing child: video/tg_techsparks_5607.mp4)

## [2026-05-28 22:58] [ingest] | Telegram @Theedinorogblog — 24 поста 19–26 мая 2026 (стартап/AI-новости, SpaceX S-1, ARR-скам)
- source: wiki/sources/2026-05-26-tg-theedinorog-may-19-26-2026.md
- created:
  - wiki/evolving-strict/market-data/ai-adoption-penetration-feb-2026.md
  - wiki/canon/marketing-frameworks/contracted-vs-live-arr-inflation-stevenson.md
  - wiki/evolving/industry-trends/eu-sanctions-contractor-payments-risk-2026.md
  - wiki/volatile/weekly-digest/edinorog-may-19-26-2026-digest.md
- updated:
  - wiki/evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2.md (backfill из @Theedinorogblog)
  - wiki/evolving/industry-trends/ai-corporate-race-mar-may-2026.md (backfill из @Theedinorogblog)
- superseded: none
- sensitive flag: none
- layer-touched: {evolving-strict: 2, canon: 1, evolving: 2, volatile: 1, sources: 1}
- touched: 7 pages
- raw: raw/processed/articles/tg_Theedinorogblog_20260526-123658.md → processed (+ 17 child media; 2 missing children: video/tg_Theedinorogblog_7972.mp4, 7986)

## [2026-05-28 23:05] [ingest] | Управление партнёрством (глава из книги, e-xecutive.ru, пер. Иванов/Фербер)
- source: wiki/sources/2026-05-26-web-e-xecutive-upravlenie-partnerstvom.md
- created:
  - wiki/canon/marketing-frameworks/professional-service-firm-governance-maister.md
- updated:
  - none
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, sources: 1}
- touched: 2 pages
- raw: raw/processed/articles/web_www.e-xecutive.ru_education_glavy-iz-knig_339469-upravlenie-partnerstvom_e34571f2.md → processed

## [2026-05-28 23:06] [ingest] | Дзен (Деловой мир) — «Купер» × Билайн Adtech: кросс-канальная атрибуция и синергия медиаканалов
- source: wiki/sources/2026-05-26-dzen-kuper-bilayn-cross-channel-attribution.md
- created:
  - wiki/canon/marketing-frameworks/channel-role-funnel-mapping-media-mix.md
  - wiki/evolving-strict/campaign-metrics/kuper-bilayn-cross-channel-incrementality-2026.md
- updated:
  - wiki/canon/marketing-frameworks/clickless-channel-incrementality-stable-id.md (backfill из Купер×Билайн кейса)
  - wiki/evolving-strict/campaign-metrics/diksi-bilayn-smart-tv-incrementality-2026.md (backfill из Купер×Билайн кейса)
  - wiki/evolving/industry-trends/digital-indoor-retail-media-ru-2026.md (backfill из Купер×Билайн кейса)
- superseded: none
- sensitive flag: none
- layer-touched: {canon: 1, evolving-strict: 1, evolving: 1, sources: 1}
- touched: 6 pages
- raw: raw/processed/articles/web_dzen.ru_a_ahVF3HM-KU9rt6LC_bc514862.md → processed
