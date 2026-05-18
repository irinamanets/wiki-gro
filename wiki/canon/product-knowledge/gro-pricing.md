---
id: mkt:canon/product-knowledge/gro-pricing
title: GRO — публичная цена и промо-оффер
type: page
subtype: concept
layer: canon
theme: product-knowledge
tags: [product, pricing, landing-page]
confidence: high
stale: false
created: 2026-04-10
updated: 2026-05-16  # +intensive track: 240k/400k ₽ tariff-2 (founder vs founder+CMO)
sources: [sources/2026-04-10-groapp-landing.md, sources/2026-04-10-gro-appstore-listing.md, sources/2026-04-10-gro-googleplay-listing.md, sources/2026-04-10-gro-rustore-listing.md, sources/2026-04-10-gro-lk-auth.md, sources/2026-05-16-groapp-payment-intensive-tarif2.md]
namespace: mkt
---

# GRO — публичная цена и промо-оффер

Срез публичного ценообразования GRO по состоянию на 2026-04-10. Три first-party источника: [[sources/2026-04-10-groapp-landing|лендинг groapp.ru]] (day-rate подача), [[sources/2026-04-10-gro-appstore-listing|листинг в App Store iOS]] (точные IAP per-SKU) и [[sources/2026-04-10-gro-googleplay-listing|листинг в Google Play]] (агрегированный IAP-диапазон, подтверждающий оба SKU). Это каноническая точка отсчёта для маркетингового контента: цифры, которые можно цитировать в креативах, постах и рассылках, поступают отсюда.

**Важно (2026-05-16):** эта страница описывает **подписочный контур** (low-ticket, broad-funnel). У GRO существует **второй ценовой контур — «Интенсив»** (high-ticket, narrow-funnel), 240 000–400 000 ₽ за тариф. Полностью отдельный продукт, отдельная аудитория, отдельная checkout-страница. Описание: [[canon/product-knowledge/gro-intensive]]. Эти два контура — **не альтернативы**, а разные продуктовые треки с разной экономикой. **Не миксовать в одном креативе** — см. раздел «Антипаттерны контентной подачи» в [[canon/product-knowledge/gro-intensive]].

## Оффер на лендинге

Верхний оффер, повторяющийся и в hero-блоке, и в финальном CTA:

> **Попробовать 14 дней за 1 ₽**

Это trial-оффер, а не бессрочная цена. По истечении триала подписка переходит на регулярный тариф.

## Регулярная цена

На лендинге в блоке «выйти на новый уровень» цена подана так:

- **83 ₽** — за день роста (при списании за месяц)
- **249 ₽** — перечёркнутая «исходная» цена

То есть фактический рекламируемый тариф — **83 ₽/день**, что при 30 днях даёт порядка 2 490 ₽/месяц.
<!-- superseded 2026-04-10 by [[sources/2026-04-10-gro-appstore-listing]] : изначально деривация «83 × 30 ≈ 2 490», точная цифра не была подтверждена независимым источником -->
Точное подтверждение из листинга App Store iOS (IAP, секция «Встроенные покупки»): **подписка (1 месяц) = 2 490,00 ₽** `[conf:high, src:2026-04-10]`. Это совпадает с деривацией из лендинга (83 ₽ × 30 дней = 2 490 ₽) — значит, «83 ₽/день» на лендинге — это не маркетинговое округление, а честный day-rate от фактической месячной цены.

**Кросс-платформенное подтверждение.** [[sources/2026-04-10-gro-googleplay-listing|Google Play]] показывает IAP-диапазон **«От 2 490,00 ₽ до 2 990,00 ₽ за товар»** `[conf:high, src:2026-04-10]`. Нижняя граница диапазона точно совпадает с месячной подпиской из App Store, а верхняя — с отдельным SKU «100% Энергии» (см. ниже). Таким образом, **оба ценовых SKU независимо подтверждены в двух сторах**.

**Веб-кабинет: четвёртого подтверждения тоже нет.** [[sources/2026-04-10-gro-lk-auth|Экран регистрации `lk.groapp.ru/auth/`]] **не раскрывает цены pre-auth** — paywall находится после OTP-кода и через публичный WebFetch не прочитывается. Это не противоречие, а отсутствие раскрытия. Маркетинговое следствие: если контент-ссылка должна вести пользователя на прозрачную цену, направлять её нужно на лендинг [[sources/2026-04-10-groapp-landing|groapp.ru]] (где «83 ₽/день» и trial «14 дней за 1 ₽» видны сразу), **а не** на `lk.groapp.ru/auth/`. Веб-кабинет — это регистрационная воронка, не ценностная витрина.

**RuStore: третьего подтверждения нет.** [[sources/2026-04-10-gro-rustore-listing|RuStore]] **не раскрывает IAP** на публичной странице каталога — ни per-SKU, ни агрегированного диапазона. Видимая пометка «(Доступ ко всем трекам и функциям — по подписке)» без цифр. Это не противоречие, а отсутствие раскрытия: RuStore-каталог не показывает встроенные покупки до установки. Если возникнет подозрение, что команда держит **разный** ценовой оффер в разных сторах, верификация делается через установку из RuStore на реальное устройство. Пока таких подозрений нет, и канон цены держится на App Store + Google Play.

Маркировка «249 ₽» на лендинге работает как anchor: показывает скидку относительно некой «полной» цены, но лендинг не раскрывает условия, при которых действует 249 ₽. В App Store такой цены нет — только реальная подписка 2 490 ₽ и триал 1 ₽. Это усиливает риск цитирования «249 ₽» как обычной цены (см. ниже).

## Дополнительный SKU: «100% Энергии» — 2 990 ₽

В [[sources/2026-04-10-gro-appstore-listing|листинге App Store]] рядом с подпиской показан второй встроенный продукт:

- **«100% Энергии» — 2 990,00 ₽** `[conf:high, src:2026-04-10]` (также подтверждено верхней границей диапазона IAP в Google Play `[conf:high, src:2026-04-10]`)

Этого SKU **нет на лендинге groapp.ru**. Природа позиции не задокументирована публично — по названию похоже на механику «энергии» в играх и AI-приложениях (лимит генераций/попыток в день + разовая покупка расширенного лимита), но это **интерпретация с `conf:low`**, а не факт. До верификации продуктом или через ingest веб-кабинета / RuStore / Google Play:

- **Не цитировать** «100% Энергии» как известный оффер в контенте.
- **Не связывать** его с подпиской как «подписка + энергия = XXX ₽».
- Зафиксировать как открытый вопрос для следующей query-сессии с продуктом.

## Как это использовать в контенте

- В hero-креативах можно цитировать оба оффера: trial («14 дней за 1 ₽») и регулярный тариф в day-rate подаче («83 ₽ в день»).
- **Не цитируй 249 ₽ как «обычную цену» без уточнения** — лендинг использует её как anchor, а не как реальный sold-rate. Иначе это риск с точки зрения [[canon-strict/legal-claims/ad-marking-russia-2026|маркировки рекламы и правдивости цен]] в РФ.
- Day-rate подача («83 ₽ в день») — сильный psychological anchor, удобно использовать в сравнении «дешевле чашки кофе» (это обычная формула, под которую цена и подбирается).

## Второй ценовой контур — «Интенсив» (high-ticket B2B)

По [[sources/2026-05-16-groapp-payment-intensive-tarif2|чекауту payment-intensive-tarif2]] зафиксирован отдельный продуктовый трек GRO — **«Интенсив»** с тарифной серией `tarif1...tarifN`. Конкретный «Тариф 2» имеет две ценовые точки:

- «Иду один» — **240 000 ₽** `[conf:high, src:2026-05-16]`
- «Иду с директором по маркетингу» — **400 000 ₽** `[conf:high, src:2026-05-16]`

**Это не альтернатива подписке**, а отдельный продукт для другого ICP (см. [[canon/product-knowledge/gro-intensive]]):
- Подписка — broad-funnel low-ticket (~2 490 ₽/мес), все три сегмента из [[canon/target-audience/gro-segments]]
- Интенсив — narrow-funnel high-ticket (240–400k ₽), owner SMB с маркетинговой функцией (founder + CMO bundle)

**Структура «Тарифа 1» и других тарифов на 2026-05-16 не зафиксирована** — известна только «Тарифа 2».

### Как это использовать в контенте

- **Не цитировать** цены интенсива в креативах подписки — это разные продукты для разных аудиторий. Mix ломает обе подачи.
- **Не использовать** «240 000 ₽» как hero-anchor в широком funnel — высокая цена отпугнёт low-ticket аудиторию ещё до того, как они поймут, что это другой продукт.
- Интенсив-аудиторию вести через **founder-content** ([[sources/2026-05-12-tg-gro-me-channel-dump|@gro_me]], blog), не через performance-каналы подписки.

## Связанные страницы

- [[canon/product-knowledge/gro-app-overview]] — обзор продукта, механика 4 шагов
- [[canon/product-knowledge/gro-intensive]] — второй продуктовый трек GRO (high-ticket B2B), 240–400k ₽
- [[canon/product-knowledge/gro-app-store-listing]] — листинг iOS, откуда взяты точные цифры IAP
- [[canon/product-knowledge/gro-google-play-listing]] — листинг Android (Google Play), дающий кросс-платформенное подтверждение IAP-диапазона
- [[canon/product-knowledge/gro-rustore-listing]] — листинг Android (RuStore), который цен не раскрывает, но и не противоречит каноне
- [[canon/product-knowledge/gro-web-app]] — веб-версия, где цена тоже скрыта pre-auth (paywall после регистрации)
- [[canon/positioning/gro-value-proposition]] — позиционирование, к которому привязана цена
- [[canon-strict/legal-claims/ad-marking-russia-2026]] — правовые ограничения на цитирование цен в рекламе РФ

## Contradictions

- **[2026-04-10]** Лендинг подаёт «83 ₽/день при списании за месяц», что derivation-но даёт ≈2 490 ₽/мес, но не фиксирует явно. [[sources/2026-04-10-gro-appstore-listing|App Store]] подтверждает **ровно 2 490,00 ₽/месяц**. Противоречия нет, деривация и фактическая цена сошлись — но теперь источник истины для месячной цены — App Store, а для day-rate-подачи — лендинг.
- **[2026-04-10]** На лендинге нет упоминания SKU «100% Энергии» (2 990 ₽), в App Store он есть явно, а в [[sources/2026-04-10-gro-googleplay-listing|Google Play]] подтверждён как верхняя граница IAP-диапазона. Это не противоречие, а **неполнота лендинга** — он раскрывает только подписку, а не все IAP. До выяснения природы «100% Энергии» в контенте его не цитировать.

## Backlinks

_28 pages link to this one._

- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]]
- [[canon/marketing-frameworks/premium-perception-through-price]]
- [[canon/marketing-frameworks/retention-benchmarks-b2c]]
- [[canon/marketing-frameworks/subscription-consumption-model-shift-tokovinin]]
- [[canon/marketing-frameworks/tabunov-onboarding-principles]]
- [[canon/marketing-frameworks/zero-to-one-vs-scale-tabunov]]
- [[canon/positioning/gro-value-proposition]]
- [[canon/product-knowledge/gro-app-overview]]
- [[canon/product-knowledge/gro-app-store-listing]]
- [[canon/product-knowledge/gro-google-play-listing]]
- [[canon/product-knowledge/gro-rustore-listing]]
- [[canon/product-knowledge/gro-web-app]]
- [[evolving-strict/competitor-metrics/glority-global-paint-by-numbers-publisher]]
- [[evolving-strict/market-data/ru-beauty-health-ecommerce-q1-2026]]
- [[evolving-strict/market-data/ru-psychology-services-2025-2026]]
- [[evolving/content-trends/owner-escape-operations-hooks]]
- [[evolving/industry-trends/agentic-commerce-stripe-2026]]
- [[evolving/industry-trends/ru-smb-sales-q1-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-04-10-gro-appstore-listing]]
- [[sources/2026-04-10-gro-googleplay-listing]]
- [[sources/2026-04-10-gro-lk-auth]]
- [[sources/2026-04-10-gro-rustore-listing]]
- [[sources/2026-04-10-groapp-landing]]
- [[sources/2026-04-30-groapp-landing-refresh]]
- [[volatile-strict/industry-news/ru-subscription-autocharge-law-2026-03]]
- [[volatile/weekly-digest/ai-industry-news-w11-w15-2026]]
