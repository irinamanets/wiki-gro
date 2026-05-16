---
id: mkt:volatile-strict/competitor-news/tbiznes-vat-compensation-offer-2026-h1
title: "Т-Бизнес — компенсация 50% НДС с эквайринга H1 2026 (apply 1–30 июня)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [competitor, t-bank, tbiznes, smb, vat-compensation, defensive-positioning, offer, b2b]
confidence: high
stale: false
created: 2026-04-17
updated: 2026-04-17
sources: [sources/2026-04-14-tg-tinkoffbank-10566-tbiznes-vat-compensation-2026.md]
namespace: mkt
---

# Т-Бизнес — компенсация 50% НДС с эквайринга H1 2026 `[conf:high, src:2026-04-14]`

**TTL: до 2026-06-30** (дата закрытия window подачи заявок). После 2026-06-30 страница помечается `stale: true` или переписывается как post-mortem historical-reference (move в `canon-strict/historical-campaigns/`).

Пакет мер поддержки SMB-клиентов Т-Бизнеса в ответ на изменения в налоговом законодательстве РФ 2026. Объявлен 2026-04 в TG-посте @tinkoffbank [#10566](https://t.me/tinkoffbank/10566). Framework-анализ защитного позиционирования — в [[evolving/competitor-positioning/tbiznes-smb-support-defensive-positioning-2026]].

## Механика

| Параметр | Значение | Source |
|---|---|---|
| Provider | АО «Т-Банк», Т-Бизнес sub-бренд | `[conf:high, src:2026-04-14]` |
| Freeze pricing | Сохраняется прежняя стоимость бухобслуживания на весь 2026 год | `[conf:high, src:2026-04-14]` |
| Консультации | Бесплатно по вопросам налогов и отчётности | `[conf:high, src:2026-04-14]` |
| Компенсация НДС | **50%** от уплаченного НДС с торгового и интернет-эквайринга | `[conf:high, src:2026-04-14]` |
| Период компенсации | Первое полугодие 2026 (январь–июнь) | `[conf:high, src:2026-04-14]` |
| Пример unit-math | НДС 2,2 ₽ → возврат 1,1 ₽ | `[conf:high, src:2026-04-14]` |
| Application window | 1–30 июня 2026 | `[conf:high, src:2026-04-14]` |
| Канал подачи заявки | Поддержка в личном кабинете Т-Бизнеса | `[conf:high, src:2026-04-14]` |
| Landing | https://u.tbank.ru/supportb2b | `[conf:high, src:2026-04-14]` |

## Eligibility criteria (все одновременно)

1. **Клиент Т-Бизнеса** с эквайрингом **и** расчётным счётом `[conf:high, src:2026-04-14]`.
2. **Выручка до 20 000 000 ₽/год** в период 2025–2026 `[conf:high, src:2026-04-14]`.
3. **Оборот за полгода от 10 000 ₽** `[conf:high, src:2026-04-14]`.
4. **Подана заявка через поддержку** в личном кабинете Т-Бизнеса в window 1–30 июня 2026 `[conf:high, src:2026-04-14]`.

## Эффективная экономика

- **Диапазон ICP:** SMB с годовой выручкой до 20 000 000 ₽ (~170 000 ₽/мес средне) и с минимальной активностью от 10 000 ₽/полгода `[conf:high, src:2026-04-14]`. Это **активные, но sub-scale предприниматели**: отсекаются и спящие ИП (<10k ₽/полгода), и mid-market (>20M ₽/год).
- **Maximum theoretical compensation:** зависит от эквайринг-оборота клиента, NOT ограничена absolute cap. Например, при обороте эквайринга 5 000 000 ₽/полгода и комиссии ~1.5% → комиссия 75 000 ₽, НДС на неё ~15 000 ₽, компенсация **~7 500 ₽** на клиента за H1 2026 `[conf:medium, src:2026-04-14]` (эстимейт based on typical acquiring-rates).
- **Retention-value:** измеряется не в $$, а в **switching-cost** — клиент, получивший compensation, инвестирован в relationship, churn-probability снижается (типично 30–50% меньше churn в reward-loyal-cycle) `[conf:low, src:2026-04-14]`.

## Позиционирование

Из caption TG-поста:

- **«Мы видим, как меняется нагрузка на бизнес»** — listening-acknowledge cost-shock без political-framing `[conf:high, src:2026-04-14]`.
- **«Хотим помочь не только словом, но и делом»** — word-deed dichotomy, anti-fluff signal `[conf:high, src:2026-04-14]`.
- **«Берём часть нагрузки на себя»** — солидарность framing, «одна лодка» сигнал `[conf:high, src:2026-04-14]`.

## Context: регуляторный trigger

Offer — response на изменения в налоговом законодательстве РФ, вступившие в силу **с начала 2026 года** `[conf:high, src:2026-04-14]`. Повысили **нагрузку на эквайринг** для SMB (вероятнее всего — введение/изменение НДС на банковские комиссии за эквайринг; полная регуляторная spec за пределами scope marketing-memory).

Это **classic defensive-solidarity move** при regulatory-shock'е — см. фреймворк в [[evolving/competitor-positioning/tbiznes-smb-support-defensive-positioning-2026]].

## Распределительная канализация offer'a

Offer опубликован **в consumer-channel @tinkoffbank**, не в @tbank_business. Это **up-promote from B2B sub-brand into consumer-channel**:

- Consumer-audience включает много SMB-founders/самозанятых (overlap между consumer ICP и SMB ICP в РФ ~20–30%) `[conf:low, src:2026-04-14]`.
- Одна creative-unit работает как **retention-message** для existing Т-Бизнес-clients (которые подписаны на @tinkoffbank тоже) и как **acquisition-hook** для consumer-entrepreneurs, кто не был в курсе Т-Бизнес.
- Economically-efficient cross-channel use — одна креативная единица, максимальный reach.

## Conversion expectations (гипотезы)

- **Apply-rate среди eligible existing clients:** ожидаем **30–50%** (narrow window + concrete cash-return = high conversion) `[conf:low, src:2026-04-14]`.
- **Acquisition-uplift (new Т-Бизнес clients from consumer-channel offer):** сложно измерить без attribution data от Т-Банка, но **halo-effect** обычно 2–5% acquisition-lift в defensive-periods `[conf:low, src:2026-04-14]`.

## Применение для GRO

1. **Direct applicability:** GRO — не Т-Бизнес-client (B2B SMB-bank service), так что offer non-applicable directly. Но если GRO имеет эквайринг-relationship с Т-Бизнес — проверить eligibility до 30 июня 2026.
2. **Indirect marketing intel:** offer demonstrates **Т-Бизнес retention-strategy 2026**. Если GRO целевая — стартап-segment, важно знать, что **Т-Бизнес активно защищает SMB-ICP**. Это означает:
   - Converts к другим банкам затруднены (switching-cost inflated через compensation);
   - Сигнал рынку: SMB-banking — территория Т-Бизнес в 2026.
3. **Template для future GRO-offer'ов:** использовать эту структуру (freeze + consulting + compensation + narrow window) как шаблон для GRO reactive-offer'ов в response на market-shocks.

## Связанные страницы

- [[sources/2026-04-14-tg-tinkoffbank-10566-tbiznes-vat-compensation-2026]] — primary-источник
- [[evolving/competitor-positioning/tbiznes-smb-support-defensive-positioning-2026]] — фреймворк defensive-solidarity-move
- [[evolving/industry-trends/tbank-corporate-platform-stack-2026]] — Т-Банк как ecosystem-player
- [[volatile-strict/competitor-news/yandex-direct-opora-promo-2026-04]] — параллельный B2B-offer (acquisition vs defensive)
- [[evolving/competitor-positioning/tbank-premium-sub-brand-palette]] — матрица sub-brands T-Bank
