---
id: mkt:evolving-strict/campaign-metrics/tbank-antifraud-service-metrics
title: "Т-Банк «Защитим или вернём деньги»: метрики антифрод-сервиса"
type: page
subtype: metric
layer: evolving-strict
theme: campaign-metrics
tags: [campaign-metrics, t-bank, tinkoff, antifraud, fraud, service-metrics, trust]
confidence: medium
stale: false
created: 2026-05-24
updated: 2026-05-24
sources: [sources/2026-05-24-condense-vcru-chunk5.md]
namespace: mkt
---

# Т-Банк «Защитим или вернём деньги»: метрики антифрод-сервиса

Числовые показатели антифрод-сервиса Т-Банка (Тинькофф Защита) из корп. блога (vc.ru/tbank, статья про новый сценарий мошенничества, 2026-05-19). Контент-маркетинговый разбор кейса — в [[volatile-strict/competitor-news/tbank-fraud-scenario-hybrid-firstperson-content]].

## Метрики сервиса

- Сервис определяет мошенничество во время звонка с вероятностью >99%. `[conf:medium, src:2026-05-19]`
- С сентября 2023 по февраль 2024 сервис «спас» 170 млн ₽. `[conf:medium, src:2026-05-19]`
- Сумма компенсаций клиентам (когда деньги всё же украли) — 4,5 млн ₽. `[conf:medium, src:2026-05-19]`
- Рост атак по новому «гибридному» сценарию — в 3,5 раза (март к январю 2024). `[conf:medium, src:2026-05-19]`

## Интерпретация

- **>99% точность + 170 млн ₽ «спасено» за полгода** `[conf:medium, src:2026-05-19]` — proof-point эффективности, который банк использует как контент-аргумент доверия (security-as-marketing).
- **170 млн «спасено» vs 4,5 млн компенсаций** `[conf:medium, src:2026-05-19]` — соотношение, выгодное для месседжа «работает в подавляющем большинстве случаев, а если нет — компенсируем».
- **Рост атак ×3,5** `[conf:medium, src:2026-05-19]` — обоснование актуальности сервиса (растущая угроза = растущая потребность).

`confidence: medium` — данные самого вендора (Т-Банк) из маркетингового материала; для бенчмарка нужна независимая верификация.

## Применение для GRO

1. **Proof-point как контент-аргумент** — модель «один сильный числовой proof (>99% / 170 млн ₽) → доверие». Применимо к подаче метрик результата GRO (см. [[canon/marketing-frameworks/customer-photos-with-metrics-ugc]]). [conf:low, src:2026-05-24]
2. **Security/guarantee-as-marketing** — гарантия («защитим или вернём») как маркетинговый месседж снижает риск-барьер; перенос на любые money-back/результат-гарантии.
3. **Растущая угроза = растущая потребность** — рамка обоснования актуальности продукта через рост проблемы.

## Связанные страницы

- [[sources/2026-05-24-condense-vcru-chunk5]] — первоисточник
- [[volatile-strict/competitor-news/tbank-fraud-scenario-hybrid-firstperson-content]] — контент-кейс антифрода
- [[evolving/content-trends/branded-show-format-t-bank-stars-vs-fraudsters]] — «Звёзды против мошенников» (тот же fraud-awareness вектор)
- [[canon/marketing-frameworks/customer-photos-with-metrics-ugc]] — метрика как proof-point
- [[canon/marketing-frameworks/customer-fears-as-content-pillar]] — страх как контент-пиллар
</content>
