---
id: mkt:volatile-strict/industry-news/anthropic-ru-block-egoshin-vendor-confirmation-2026-05
title: Anthropic блокирует RU-учётки Claude (2026-05-08) — vendor-side confirmation от Егошина (founder Нейрофонд)
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [ai, b2b, b2c, awareness]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-egoshin-kedprof-may-5-12-2026.md, sources/2026-05-14-tg-neuraldvig-may-5-12-2026.md]
namespace: mkt
---

# Anthropic блокирует RU-учётки Claude (2026-05-08) — vendor-side confirmation

Second-source confirmation волны блокировок RU-аккаунтов Claude'ом со стороны Anthropic. Первичный сигнал зафиксирован в [[sources/2026-05-14-tg-neuraldvig-may-5-12-2026|@neuraldvig пост 10650 (Baza-репортаж)]] и развёрнут в 15-й вектор [[evolving/industry-trends/ru-digital-regulatory-squeeze-2026|RU regulatory squeeze]]. Эта страница фиксирует **vendor-side подтверждение** того же события через канал Константина Егошина (founder «Кеды профессора» + Нейрофонд + co-founder GRO).

## Факты

- **Событие:** Anthropic начал массово блокировать аккаунты российских пользователей Claude, включая Pro/Team подписки. Потеря всех чатов / проектов / кода / наработок. Деньги за подписку возвращают `[conf:high, src:2026-05-08]`
- **Дата подтверждения от vendor-стороны:** 2026-05-08 (пост 569 @egoshin_kedprof)
- **Прямая цитата Егошина:** «С утра все новости о том, что Антропик блокирует учетки российских пользователей в Claude. Печально. Если вас заблокировали, а Opus или Sonnet вам нужны, приходите к нам в Нейрофонд, там всё работает: promo.neurofond.ru/» `[conf:high, src:2026-05-08]`
- **Первичный сигнал (media-сторона):** Baza-репортаж, ретранслированный @neuraldvig (пост 10650): «по данным Baza, доступ к аккаунтам потеряли уже сотни человек… причиной волн блокировок стали новые проверки аккаунтов с постоянным переподключением VPN и сменой региона» `[conf:medium, src:2026-05-08]`
- **Affected audience:** разработчики (Claude Code пользователи), маркетологи, продуктовые менеджеры — все, кто использовал Claude как core productivity tool через серую регистрацию + VPN

## Почему это vendor-side confirmation (а не дубль)

Сигнал от Егошина **квалитативно отличается** от Baza/neuraldvig-репортажа:

- **Baza/@neuraldvig** — это **media-сторона**: репортаж от RU-новостного агрегатора со ссылкой на источник (Baza), без конкретного affected user. Имеет confidence: medium.
- **Егошин** — это **vendor-сторона RU AI-vendor'a (Нейрофонд)**, который **наблюдает миграцию пользователей в реальном времени** через свою admin-panel. Когда Egoshin пишет «приходите к нам, у нас всё работает» — это **подразумевает наблюдаемый inflow**. Это **операционное подтверждение** того, что блокировка реальна и влияет на user-base.

Это поднимает confidence Baza-сигнала с `medium` до `high` через **vendor-side observation** (см. CLAUDE.md правила confidence: ≥2 независимых источника + не противоречат).

## Импликации

### Краткосрочные (1-4 недели)

1. **Inflow в RU AI-агрегаторы.** Нейрофонд, Bothub, GigaChat, YandexGPT и другие RU-нативные сервисы видят cтап пользователей. Точные цифры неизвестны, но **paid-acquisition cost** для RU AI-агрегаторов в этот период должен временно упасть (organic-inflow заменяет paid).
2. **Volatility в developer-комьюнити.** Claude Code users теряют контекст бесед — это самый болезненный сегмент. Большинство мигрирует на Codex (OpenAI) или на RU-LLM (DeepSeek через RU-агрегаторы). Это краткосрочное disruption в developer-workflows.
3. **Content-opportunity для RU vendors.** Шаблон поста Егошина — образец **opportunistic positioning playbook** (см. [[evolving/competitor-positioning/neurofond-positioning-2026-05]]): trigger → empathy → solution + promocode. Переносим на любой RU-нативный продукт.

### Среднесрочные (1-3 месяца)

1. **TTL: 30 дней re-verify.** Нужна проверка, продолжается ли волна банов (вторая партия в июне? коллегиальное решение Anthropic об ограничениях vs локальный issue?), и реагирует ли OpenAI идентично. Если волна разовая — это сильный, но кратковременный сигнал; если систематическая — структурное преимущество RU-нативных продуктов.
2. **Vendor-trust-shift.** Russian users получают усиленный signal «западные AI-вендоры могут отключить вас без предупреждения» → доверие к RU-нативным продуктам (включая GRO) растёт. Это **косвенный tailwind**.
3. **Регуляторный echo.** Если волна продолжится, может появиться российский регуляторный ответ (РКН, Минцифры) на блокировки западных вендоров. Это **гипотетический** vector-16 в [[evolving/industry-trends/ru-digital-regulatory-squeeze-2026]] (vendor-blocked-by-vendor → regulator-blocks-vendor), но требует подтверждения.

### Долгосрочные (3-12 месяцев)

- **Vendor-risk awareness** становится постоянным фактором при выборе AI-tool в RU. Это **постоянно действующее давление** в сторону RU-нативных или multi-vendor решений (Нейрофонд-class).
- Для **GRO** долгосрочный эффект **нейтрально-позитивный**: GRO ≠ AI-агрегатор, поэтому Claude-блокировка не угрожает GRO-stack напрямую. Но vendor-trust-shift повышает базовую readyness аудитории к RU-AI-продуктам.

## Content-hooks для GRO

1. **«GRO работает в России. Без VPN. Без риска бана аккаунта.»** — короткое противопоставление с Claude/OpenAI workaround-аудитории. Уже зафиксировано в [[evolving/industry-trends/ru-digital-regulatory-squeeze-2026]] как content-hook.
2. **«Что делать, если ваш AI-tool заблокировали»** — образовательный пост для GRO-блога: список RU-альтернатив по типам задач (writing → Нейрофонд/Bothub; code → DeepSeek/GigaChat Code; ideas → GRO для behavior-change). Это не прямое promo, это образовательный hook + soft inclusion GRO в список.
3. **«Урок неустойчивости из истории Claude RU-block»** — long-form пост про vendor-risk management: что произошло, почему, как защититься (multi-vendor strategy, RU-нативные backups, локальные данные). Этот hook резонирует с founder-аудиторией.

## Связанные страницы

- [[evolving/industry-trends/ru-digital-regulatory-squeeze-2026]] — 15-й вектор, развёрнутый контекст
- [[evolving/competitor-positioning/neurofond-positioning-2026-05]] — Нейрофонд как opportunistic-positioning beneficiary
- [[volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05]] — Codex vs Claude Code shift из-за Anthropic блокировок
- [[volatile-strict/competitor-news/anthropic-800b-identity-verification-2026-04]] — apr-2026 identity verification, предтеча текущей волны
- [[sources/2026-05-14-tg-egoshin-kedprof-may-5-12-2026]] — vendor-side confirmation source
- [[sources/2026-05-14-tg-neuraldvig-may-5-12-2026]] — media-side первичный сигнал
