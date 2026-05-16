---
id: mkt:evolving-strict/market-data/ai-driven-layoffs-2025-2026
title: AI-driven сокращения штатов 2025–2026 — Amazon, Microsoft, Сбер, РФ-опрос
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [ai-agents, labor-market, career, awareness, content, market-trends]
confidence: medium
stale: false
created: 2026-04-14
updated: 2026-05-05  # +Coinbase −14% (~700), Crypto.com −12% (~180), Block −40% (~4000) с прямой AI-аргументацией CEO; реструктуризация Coinbase $50–60M
sources: [sources/2026-04-14-tg-t-jrnl-apr2026.md, sources/2026-04-16-forbes-ru-snap-stock-9pct-ai-layoffs.md, sources/2026-05-05-vc-ru-condensed.md, sources/2026-05-05-vcru-crypto-2910180-coinbase-uvolit-14-sotrudnikov.md, sources/2026-05-05-vcru-hr-2803781-crypto-com-sokrashchenie-sotrudnikov.md, sources/2026-05-05-vcru-hr-2805167-professii-pod-ugrozoy-kakie-raboty-zamenit-iskuss.md]
namespace: mkt
---

# AI-driven сокращения штатов 2025–2026

Первая страница в `evolving-strict/market-data/`, посвящённая **корпоративной стороне** AI-воздействия на труд: публичные, атрибутированные CEO-заявления о том, что конкретный процент штата сокращён в 2025 году в связи с внедрением ИИ. Дополняет [[evolving-strict/market-data/ai-labor-market-anthropic-2026|Anthropic Labor Market Impact Study]], который фиксирует **пользовательскую** сторону (observed exposure), — здесь мы фиксируем сторону **HR-решений**.

Страница нужна marketing-memory для того, чтобы контент GRO под [[canon/target-audience/gro-segments|карьерный сегмент]] мог опираться на конкретные цифры (а не общие «ИИ заменит всех») и подтверждал нарратив «готовься заранее» конкретными процентами с корпоративного уровня.

**Важно про confidence.** Сами цифры Amazon/Microsoft/Сбер — `conf:high` (публичные заявления CEO), но страница целиком помечена `confidence: medium`, т.к. единственный на сегодня ingest-источник — Т-Ж, который **переупаковывает** эти заявления, и цифра 47% по РФ идёт без первоисточника опроса. `[conf:medium, src:2026-04-13]` При появлении прямых ingest'ов Anthropic/Bloomberg/Reuters/Forbes повысим до high.

## Публичные корпоративные заявления 2025–2026

| Компания | Сокращение | Кто озвучил | Дата заявления | Риторика | Source |
|---|---|---|---|---|---|
| Amazon | **10%** | Andy Jassy (CEO) | 2025 | «Генеративный ИИ и "агенты" позволяют выполнять задачи меньшими силами» | `[conf:high, src:2026-04-13]` |
| Microsoft | **7%** | Satya Nadella (CEO) | 2025 | Письмо о сокращениях сопровождено размышлениями о возможностях эпохи нейросетей | `[conf:high, src:2026-04-13]` |
| Сбер | **20%** | Герман Греф (глава банка) | 2025 | «Благодаря технологиям сократили 20% сотрудников, включая каждого пятого инженера» | `[conf:high, src:2026-04-13]` |
| Snap | **до 16%** | Evan Spiegel (CEO) | 2026-04-15 | «Стремительное развитие ИИ позволяет нашим командам сократить объём рутинной работы, увеличить скорость и лучше поддерживать сообщество, партнёров, рекламодателей»; $500M годовой экономии ко 2H 2026; операционная база: >65% нового кода генерируют ИИ-агенты, >1M запросов/мес | `[conf:high, src:2026-04-16]` |
| Coinbase | **−14%** (~700 чел) | Brian Armstrong (CEO) | 2026-05 | «Самый большой риск — бездействие» на фоне AI; расходы на реструктуризацию **$50–60 млн** | `[conf:high, src:2026-05-05]` |
| Crypto.com | **−12%** (~180 чел) | Kris Marszalek (CEO) | 2026-05 | «компании, которые не сделают это немедленно, проиграют»; уволенные «не смогли адаптироваться к новой реальности» | `[conf:medium, src:2026-05-05]` |
| Block | **>40%** (~4000 чел) | Jack Dorsey (CEO) | 2026-02 | «большинство компаний придут к тому же» | `[conf:medium, src:2026-05-05]` |

**Enrich 2026-04-16 (Forbes.ru).** Snap добавлен как четвёртый кейс. Важны два момента: (1) цифра 16% теперь корроборирована двумя независимыми ingest-источниками (Т-Ж + Forbes.ru), confidence на уровне строки — `high`; (2) Snap — первый кейс в таблице, где одновременно с заявлением о сокращениях раскрыты операционные AI-метрики (65% кода, 1M+ запросов/мес) — это даёт пример «того, как выглядит AI-first компания в масштабе», а не только заявленный процент `[conf:high, src:2026-04-16]`.

**Enrich 2026-05-05 (vc.ru condensed 46 articles).** Coinbase / Crypto.com / Block добавлены как fifth–seventh cases в таблице. Все три — **криптофинансовая вертикаль**, которая публично использует AI-аргументацию для cost-cutting в момент структурного давления (биткоин −40% с октября 2025). Anthropic параллельно выпустила исследование о профессиях под угрозой автоматизации `[conf:medium, src:2026-05-05]`; в зоне риска — юристы, аналитики, IT-специалисты, преподаватели; «безопасные» — те, где требуется живое взаимодействие с людьми.

Четыре наблюдения, вытекающие из таблицы:

1. **Диапазон 7–20% за один год** — это уже не «экспериментальное внедрение». Medians публичных tech-сокращений в 2023–2024 были на порядок меньше и объяснялись «оптимизацией после covid-найма». В 2025 риторика изменилась: CEO лично увязывают цифры с ИИ, а не прячут за формулировкой «restructuring». `[conf:medium, src:2026-04-13]`
2. **Сбер опережает глобальные tech-бигтехи по проценту** — и единственный из трёх, кто публично назвал срез по инженерам (каждый пятый). Для GRO-контента это полезный анекдот именно потому, что Сбер — не западный аутлаер, а российский ориентир, понятный аудитории. `[conf:high, src:2026-04-13]`
3. **Три разные юрисдикции, одинаковый риторический ход** — синхронность важнее абсолютных цифр. Это означает, что CEO в 2025 году начали считать «ИИ-оптимизация» легитимным публичным обоснованием для investor-relations и медиа. `[conf:medium, src:2026-04-13]`
4. **Рынок стал поощрять AI-layoffs.** Объявление Snap 15.04.2026 о 16%-сокращении вызвало рост акций на **8,7% до $6,1 на пике** в первый же день торгов на NYSE `[conf:high, src:2026-04-16]`. Это превращает паттерн CEO-заявлений в самоподдерживающуюся петлю: cost-cutting через AI не штрафуется рынком, а вознаграждается — значит, для peer-CEO не делать того же становится ответственностью перед акционерами. Snap параллельно с сокращениями прогнозирует **+12% роста выручки Q1 до $1,5 млрд** `[conf:high, src:2026-04-16]` — рынок интерпретирует как «путь к прибыльности», а не как падение.

## Российский корпоративный спрос — опрос конца 2025

- **47% компаний из сегмента крупного бизнеса РФ** в конце 2025 года заявили, что намерены оптимизировать штат с помощью внедрения ИИ `[conf:medium, src:2026-04-13]`. Это та половина-минус-три корпоративного крупняка, которая **вслух** подтвердила намерение. Реальная доля вероятно выше — те, кто не готов публично говорить про сокращения, в опрос не попали.
- Первоисточник опроса Т-Ж не назвал; при появлении оригинала — обновить confidence.
- Контекст: в РФ **массовых** AI-driven увольнений **пока нет** (по состоянию на апрель 2026 в риторике Т-Ж), но повсеместное внедрение идёт `[conf:medium, src:2026-04-11]`. Это отсрочка, а не отсутствие.

## Что это значит для marketing-memory GRO

- **Нарратив «готовься заранее».** Формулировка «выиграют те, кто подготовился заранее к внедрению ИИ» (Т-Ж, подкаст «План Б», пост 34070) теперь подкреплена конкретными процентами с корпоративного уровня. **Enrich 2026-04-15:** расшифровка видео 34100 (тизер того же подкаста «План Б») добавляет смежный anti-infobiz тезис — ведущая критикует «курсы, упакованные в PDF», что усиливает контраст GRO-тренировок vs онлайн-курсов (см. [[canon/positioning/gro-value-proposition]]). Это готовый hook для [[canon/target-audience/gro-segments|карьерного сегмента]] — людей, которые прямо сейчас находятся в компаниях, где 47% крупняка планирует оптимизацию. `[conf:medium, src:2026-04-13]`
- **Резонанс с solo-преnerство-нарративом.** Публичное признание 20% сокращений в Сбере усиливает тезис [[evolving/industry-trends/ai-solopreneurship-window-2026-2029|«мелкие обходят крупных на окне 2026–2029»]]: если крупнейший банк страны заявляет, что ИИ позволил уволить пятую часть инженеров, то симметричное утверждение «один человек + агенты = микро-компания» перестаёт звучать как спекуляция. `[conf:high, src:2026-04-13]`
- **Content-hook для awareness.** Сочетание четырёх цифр (Amazon 10% / Microsoft 7% / Сбер 20% / Snap 16%) в одной визуализации — готовый infographic-format для постов awareness-стадии. `[conf:high, src:2026-04-16]` Snap-case особенно силён, т.к. сопровождается рыночным сигналом (+8,7% акций) и операционным бенчмарком (65% кода от ИИ). См. [[evolving/content-trends/career-audience-hooks-2026]] для конкретных формулировок.
- **Petля investor-дисциплины.** Рост акций Snap на новостях о layoffs — не разовая аномалия, а часть формирующегося паттерна: cost-cutting через AI вознаграждается капиталом. Это усиливает тезис «готовься заранее» — карьерная аудитория GRO оказывается в среде, где CEO структурно мотивированы продолжать AI-оптимизацию. `[conf:medium, src:2026-04-16]`
- **Anti-pattern для контента GRO.** Важно **не** использовать эти цифры в доминантно-негативном ключе («вас уволят») — это активирует дофамин страха без actionable. Правильная рамка — «вот скорость изменений, вот что это значит для ваших навыков, вот как GRO помогает системно расти внутри этого сдвига», с явной привязкой к [[canon/positioning/gro-value-proposition]].

## Связанные страницы

- [[evolving-strict/market-data/ai-labor-market-anthropic-2026]] — observed-exposure сторона (что пользователи реально автоматизируют)
- [[evolving/industry-trends/ru-labor-market-shift-2026]] — качественная рамка сдвига РФ-рынка труда
- [[evolving/industry-trends/ru-job-seeker-experience-2026]] — тот же сдвиг со стороны соискателя (анонимный vc.ru блог корроборирует Amazon 16k в январе 2026 своим собственным голосом, conf:low, но narrative дошёл до аудитории)
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — тезис про окно для мелких на 2026–2029
- [[evolving/content-trends/career-audience-hooks-2026]] — готовые hooks для карьерной аудитории
- [[canon/target-audience/gro-segments]] — сегменты ЦА GRO
- [[canon/positioning/gro-value-proposition]] — правильная рамка для использования этих цифр в контенте
- [[sources/2026-04-16-forbes-ru-snap-stock-9pct-ai-layoffs]] — Forbes.ru о Snap (15.04.2026): stock +9%, операционные AI-метрики `[conf:high, src:2026-04-16]`
- [[sources/2026-05-05-vc-ru-condensed]] — vc.ru condensed 46 articles (Coinbase/Crypto.com/Block enrich)
- [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]] — финансовый контекст Coinbase/Block + биткоина

## Contradictions

<!-- Пока нет противоречий. При появлении альтернативных цифр (например, если другой источник даст другую % для Amazon/MS/Сбер) — фиксировать здесь с атрибуцией. -->

## Backlinks

_22 pages link to this one._

- [[evolving-strict/competitor-metrics/ai-leaders-valuations-2026-q2]]
- [[evolving-strict/market-data/employee-engagement-quiet-quitting-2026]]
- [[evolving-strict/market-data/ru-economy-profit-per-employee-2024]]
- [[evolving-strict/market-data/us-ai-job-risk-tufts-2026]]
- [[evolving/content-trends/career-audience-hooks-2026]]
- [[evolving/content-trends/sebrant-cognitive-exoskeleton-hooks]]
- [[evolving/content-trends/wtf-hr-ai-skeptic-hooks]]
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]]
- [[evolving/industry-trends/ai-replacing-jobs-global-2026]]
- [[evolving/industry-trends/ru-job-seeker-experience-2026]]
- [[evolving/industry-trends/ru-labor-market-shift-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-04-14-tg-t-jrnl-apr2026]]
- [[sources/2026-04-14-tg-techno-yandex-mar-apr-2026]]
- [[sources/2026-04-14-tg-techsparks-mar-apr-2026]]
- [[sources/2026-04-14-vc-ru-hr-labor-market-opinion]]
- [[sources/2026-04-16-forbes-ru-snap-stock-9pct-ai-layoffs]]
- [[sources/2026-05-05-tg-recruiter-live-apr-may-2026]]
- [[sources/2026-05-05-vc-ru-condensed]]
- [[volatile-strict/competitor-news/microsoft-9000-voluntary-retirements-2026]]
- [[volatile-strict/industry-news/openai-industrial-policy-2026-04]]
