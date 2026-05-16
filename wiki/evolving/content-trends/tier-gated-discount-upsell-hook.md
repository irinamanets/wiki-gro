---
id: mkt:evolving/content-trends/tier-gated-discount-upsell-hook
title: "Tier-gated discount — upsell-механика через вилку скидки в одном креативе"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [content, partnerships, upsell, pricing, creative-reference, t-bank, travel, decision]
confidence: medium
stale: false
created: 2026-04-17
updated: 2026-04-17  # +#10583 Т-Путешествия лето — 2x2 tier-grid (подписка × first/repeat booking) как эволюция механики, теперь 4 tiers в одном оффере
sources: [sources/2026-04-14-tg-tinkoffbank-10567-utair-closed-sale.md, sources/2026-04-14-tg-tinkoffbank-10583-summer-hotel-pool-glasses.md]
namespace: mkt
---

# Tier-gated discount hook

Наблюдаемый паттерн: один promo-креатив содержит **две цифры скидки** — baseline для всех и upgraded для tier'а partner'а (например, премиум-тариф авиакомпании или premium-подписка retailer'а). Плашки визуально равнозначны, что превращает offer в **a/b choice** с decision-framing: пользователь либо покупает baseline сейчас, либо **апгрейднется в tier** ради extra-скидки.

Base-кейс — Utair «Евробизнес» × Т-Путешествия (апрель 2026): до 20% baseline / до 50% с тарифом «Евробизнес» в одном creative'е ([[sources/2026-04-14-tg-tinkoffbank-10567-utair-closed-sale]]). `[conf:high, src:2026-04-14]`

## Анатомия механики

**Три обязательных элемента:**

1. **Baseline discount** — нижняя граница (до 20% в base-кейсе). `[conf:high, src:2026-04-14]` Доступна всем без условий, работает как «простой» offer.
2. **Tier-gated discount** — верхняя граница (до 50% с тарифом «Евробизнес»). `[conf:high, src:2026-04-14]` Требует upgrade в tier partner'а или подписку premium-уровня.
3. **Visual equivalence плашек** — обе цифры расположены горизонтально, одного размера, одной типографики. Нет визуальной иерархии «главный/дополнительный». Это ключ к a/b-choice framing.

**Композиционные правила:**
- Плашки располагаются в одну строку (в горизонтальных креативах) или одна под другой равного размера (в вертикальных).
- Цифры — крупные, текст условия — мелкий под/рядом с цифрой.
- Разделитель между плашками — gap или тонкая линия, **не стрелка** (стрелка создаст hierarchy).

## Почему это работает в 2026

1. **Anchoring + decoy эффект.** Классическая behavioral economics: две видимые цены заставляют мозг сравнивать, а не оценивать в абсолюте. 50% воспринимается как **очевидно лучше**, что motivated либо к upgrade'у в tier, либо к purchase'у prime-tier вообще.
2. **Upsell через chan partner, не через self-promote.** Вместо агрессивного «купи наш premium» offer говорит «у нас есть extra benefits для тех, у кого partner-premium». Это **soft-sell** — upgrade воспринимается как **actionable optimization** существующего решения, а не как новая покупка.
3. **Удаляет «friction choice» для commitment'ов.** Пользователь, ещё не решивший купить авиабилет, **в процессе оценки скидки** автоматически rethink'ает свой tier-status. Это внедрение upsell-thinking в **research phase** без необходимости дополнительного touchpoint'а.
4. **Два CTR-уровня в одном креативе.** Пользователи с tier'ом кликают **из-за premium-скидки**, пользователи без tier'а — **из-за baseline-offer'а**. Это удваивает addressable-audience без раздвоения креатива.

## Вариации механики

### A. Partner-tier upsell (base-кейс)

**Как в Utair × Т-Путешествия:** baseline открытая — extra требует tier у partner'а (авиакомпания, ритейлер, hotel chain). Bank здесь — channel distribution, gain — commission + tier-upsell partner'а.

### B. Provider-subscription upsell

**Вариация:** baseline открытая — extra требует premium-подписку на сервис-provider. Пример hypothet: «Скидка 15% на еду в Delivery Club / 30% с T-Premium». Upsell здесь идёт к T-Premium (собственный tier bank'а), не к partner'у.

### C. Member-only tier gap

**Вариация:** baseline — member price, extra — только first-N-members или VIP-cohort. Часто используется в community-продуктах (см. [[evolving/content-trends/urgency-window-launch-playbook]] где VIP-tier раскрывается через countdown).

### D. Payment-method discount

**Вариация (также известная):** «баланс-карта 10% / наша карта 25%». Широко используется ритейлерами для driver'а payment-tier (Яндекс.Плюс, Сбер Прайм). Механически тот же tier-gated paradigm.

### E. 2×2 tier-matrix (Т-Путешествия лето, #10583) — второй observed T-Bank кейс

**Усложнённая вариация механики.** Вместо линейных 2 tier'ов (baseline vs premium) — **2×2 matrix** по двум независимым дименсиям: (подписка Pro/T-Premium vs no-sub) × (first booking vs repeat). Результат — 4 tier'а в одном оффере `[conf:high, src:2026-04-14]`:

| Tier | Подписка | Booking | Cashback |
|---|---|---|---|
| 1 | Pro/T-Premium | First | до 10% |
| 2 | No-sub | First | до 7% |
| 3 | Pro/T-Premium | Repeat | до 7% |
| 4 | No-sub | Repeat | до 5% |

Это расширяет механику из linear upsell-hook в **multi-dimensional loyalty-matrix**. Две ортогональные dimension'ы:
- **Subscription-status** — стимулирует конверсию в Pro/T-Premium.
- **Booking-recency** — стимулирует first-time trial (unknown segment).

**Когда применять multi-tier-matrix:**
- Running продукт с выраженным **subscription-layer** (не one-shot purchase).
- Product с meaningful difference между new-user vs repeat-user economics (travel, subscription-box, SaaS).
- Brand имеет **multiple loyalty-dimensions** (tier, streak-count, spent-volume, referrals).

**Design-trade-off:** 4-tier matrix sacrifices **instant-comparability** (user'у нужно читать caption, чтобы найти свой tier) ради **granularity offer'а**. T-Bank держит **max-цифру (до 10%)** в pill-badge креатива для scroll-readability, но full-matrix — в caption. Hybrid solution: visual-hero показывает best-case, caption раскрывает matrix.

## Ограничения

1. **Requires чистое partnership-alignment.** Две цены требуют согласования с partner'ом о том, какой tier раскрывает какую скидку. Без подписанного agreement — offer будет либо не-honored'ся, либо создаст customer-service-issue.
2. **Не работает для «чёрных» скидок.** Если baseline — 5%, extra — 7%, gap не чувствуется. Минимальный effective-gap ≥ 20 percentage points для психологического эффекта.
3. **Transparency-риск.** Если tier-condition скрыт или сложен, пользователь чувствует «скам». Креатив Utair solution'ит это **через явный текст «с тарифом "Евробизнес"»** прямо в plashке — no-hidden-fees trust-signal.
4. **Channel-complexity.** Offer-delivery (auto-apply в checkout) требует integration'а с partner-billing-системой. Utair × Т-Путешествия решает это тем, что **cost уже включена в отображаемую цену** — user не вводит promocode, не сверяет tier. Без этой интеграции механика не work'ает.

## Переносимость на GRO

GRO не имеет travel-партнёров, но tier-gated-discount-hook — **universal для B2C-upsell'ов**. Variants для GRO:

1. **GRO Free baseline / GRO Pro extra:** в promo-креатив для 3rd-party-offer (например, скидка на wellness-partner) показать две цифры — 10% для Free-юзеров, 25% для Pro-юзеров. Driver для upgrade'а без явного `buy Pro`.
2. **Launch-cohort tier:** «скидка 20% first 500 / 30% beta-members / 40% founders» — триplет разрывов, усиливающий community-effect.
3. **Annual vs monthly tier:** при cross-sell'е дополнительного продукта показать «скидка X% для monthly / Y% для annual» — driver'ет annual-upgrade.

**Важное соображение:** в GRO нет классических «partners» в смысле travel/retail, но есть потенциальные **content-creator partnerships** (инфлюенсеры в fitness/wellness) и **corp-wellness программы** (HR-B2B channel). Tier-gated-discount применим к обоим.

## Gap и неизвестные

- **Conversion-rate разница** между baseline и tier-gated-кликами не известна публично. Нужен internal-тест через UTM split.
- **Long-term эффект на tier-upgrade volume** — если вариация B стимулирует upgrade в T-Premium через travel-offer, это **indirect revenue** для banking product. Публичных данных нет.
- **Cross-cultural transferability.** В RU-рынке tier-гейтинг воспринимается как «уместный» (за премиум-платишь — премиум-получаешь). В других культурах может вызвать «скам-reaction». GRO должно тестировать на целевых гео.

## Связанные страницы

- [[sources/2026-04-14-tg-tinkoffbank-10567-utair-closed-sale]] — base-кейс Utair × Т-Путешествия (линейные 2 tier'а)
- [[sources/2026-04-14-tg-tinkoffbank-10583-summer-hotel-pool-glasses]] — 2×2 tier-matrix evolution (подписка × booking-recency)
- [[evolving/content-trends/gift-with-purchase-premium-bundling]] — GWP как inverse-механика (purchase → gift)
- [[canon/marketing-frameworks/partnerships-growth-multiplier]] — partnerships как multiplier роста (context для tier-discount)
- [[evolving/content-trends/urgency-window-launch-playbook]] — VIP-tier-gap через countdown/cohort
- [[evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay]] — визуальный протокол, от которого креатив #10567 делает partner-color отклонение
- [[evolving/content-trends/telegram-native-formats]] — TG-native pill-tag-based креативы

## Backlinks

_5 pages link to this one._

- [[evolving/competitor-positioning/tbank-consumer-visual-style-yellow-block-flatlay]]
- [[index]]
- [[sources/2026-04-14-tg-tinkoffbank-10567-utair-closed-sale]]
- [[sources/2026-04-14-tg-tinkoffbank-10568-academeg-fuel-cashback]]
- [[sources/2026-04-14-tg-tinkoffbank-10583-summer-hotel-pool-glasses]]
