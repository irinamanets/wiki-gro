---
id: mkt:canon/marketing-frameworks/abandon-cart-paywall-dark-patterns
title: "Abandon-cart downsell + face-scan-before-paywall — paywall-механики мобильных подписок"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [paywall, abandon-cart, downsell, dark-pattern, sunk-cost, mobile-subscription, conversion, monetization, decision]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-your-pet-project-may-14-18-2026.md]
namespace: mkt
---

# Abandon-cart downsell + face-scan-before-paywall

Две paywall-механики мобильных подписок, задокументированные на кейсе FaceKit ([[sources/2026-05-19-tg-your-pet-project-may-14-18-2026]] пост 631, Табунов). Помещены в `canon` как **стабильные переиспользуемые механики** (структура воронки не дрейфует между версиями продукта), численные метрики самого кейса — в [[evolving-strict/competitor-metrics/facekit-ai-influencer-app-monetization-2026]].

`confidence: medium` — описание механик single-source, но обе — общеотраслевые паттерны мобильной подписочной монетизации (Cal AI, RevenueCat-экосистема и др.), консистентны с независимыми наблюдениями.

## Механика 1 — Abandon-cart downsell

Когда пользователь **не купил с первого пейволла**, ему сразу подсовывается предложение подешевле (downsell-tier).

- На FaceKit: основные тарифы год $40 / неделя $10, а **abandon-cart-tier — $20**. Половина выручки приходит именно через эту механику (см. метрики). `[conf:medium, src:2026-05-15]`
- Логика: первый пейволл «снимает сливки» (готовые платить полную цену), второй пейволл **конвертирует колеблющихся**, у которых якорь цены уже сформирован первым экраном — $20 после $40 выглядит как «скидка», хотя это просто второй проход.
- Это price-discrimination внутри одной сессии: разные пользователи платят разную цену в зависимости от ценовой чувствительности, выявленной первым отказом.

**Как НЕ-dark-применить в GRO:** второй paywall-tier с честным downsell (например, более дешёвый месячный вместо годового, или trial-extension) — легитимная conversion-механика, если без введения в заблуждение по цене/ценности. Главный takeaway: **один paywall оставляет деньги на столе; колеблющихся надо ловить вторым оффером**.

## Механика 2 — Face-scan-before-paywall (sunk-cost trap)

Пользователь сначала тратит **30 секунд на 3D-скан лица**, ждёт обработки, и **только потом** видит цену.

- Это эксплуатация **sunk-cost эффекта**: чем больше пользователь вложил усилий/времени до момента оплаты, тем выше вероятность, что он заплатит, чтобы «не потерять» вложенное.
- Обобщённый паттерн: **отложить раскрытие цены до тех пор, пока пользователь не совершит вовлекающее действие** (квиз, скан, генерация результата, персонализация).
- Граница dark-pattern: становится манипулятивным, когда (а) цена сознательно скрыта, чтобы спровоцировать лишние усилия, и (б) ценность результата иллюзорна (как псевдонаучный «golden ratio» в FaceKit). Cross-ref общую таксономию dark patterns: [[evolving/content-trends/social-media-addiction-design-patterns]].

**Как НЕ-dark-применить в GRO:** дать пользователю **реальный мини-результат до пейволла** (например, разбор одной ситуации, демо-репетиция), чтобы он почувствовал ценность — это легитимный «value-first onboarding», а не sunk-cost trap. Граница: результат должен быть реальным, а цена — не скрытой намеренно. Связано с [[canon/marketing-frameworks/tabunov-onboarding-principles|180-секундным онбордингом]] и [[canon/marketing-frameworks/funnel-simplicity-principle]].

## Когда это становится dark pattern (граница для GRO)

| Легитимно | Dark pattern |
|---|---|
| Downsell с честной ценой/ценностью | Скрытие реальной цены, fake-«скидка» |
| Value-first demo до paywall | Sunk-cost trap с иллюзорным результатом |
| Прозрачные тарифы | Псевдонаучные термины ради trust-иллюзии |

GRO как серьёзный self-development/wellness продукт для AI-aware ЦА (см. [[canon/target-audience/gro-segments]]) **может брать структуру** (второй tier, value-first), но **не манипулятивную начинку** — иначе trust-разрушение. Legal-контекст маркировки и недобросовестных практик — [[canon-strict/legal-claims/ad-marking-russia-2026]].

## Связанные страницы
- [[evolving-strict/competitor-metrics/facekit-ai-influencer-app-monetization-2026]] — кейс-источник с метриками
- [[canon/marketing-frameworks/ai-influencer-grandma-playbook]] — тот же AI-инфлюенсер-контекст дистрибуции
- [[canon/marketing-frameworks/tabunov-onboarding-principles]] — value-first онбординг как анти-sunk-cost
- [[canon/marketing-frameworks/funnel-simplicity-principle]] — упрощение воронки
- [[evolving/content-trends/social-media-addiction-design-patterns]] — общая таксономия dark patterns
- [[canon-strict/legal-claims/ad-marking-russia-2026]] — legal-граница недобросовестных практик
- [[sources/2026-05-19-tg-your-pet-project-may-14-18-2026]] — источник
