---
id: mkt:evolving-strict/campaign-metrics/mindbox-channel-shift-2025
title: "Mindbox 2025: email/SMS сдвиг 26:1, push впервые превысили email +45%"
type: page
subtype: metric
layer: evolving-strict
theme: campaign-metrics
tags: [campaign-metrics, email, push, sms, crm, retention, channels, ru]
confidence: high
stale: false
created: 2026-05-14
updated: 2026-06-01  # +cross-link на B2B-кейс Банка Синара (каскад PUSH→SMS) — enterprise-валидация того же channel-shift
sources: [sources/2026-05-14-tg-cossaru-may-5-14-2026.md]
namespace: mkt
---

# Mindbox 2025: channel-shift в прямых коммуникациях

Исследование Mindbox по [результатам 2025 года](https://www.cossa.ru/news/348419/) (опубликовано в [Cossa.ru @cossaru пост 23115](https://t.me/cossaru/23115) от 2026-05-06): на фоне подорожания SMS и блокировок мессенджеров бизнес массово перенёс прямые коммуникации в email и мобильные push-уведомления.

## Цифры

| Метрика 2025 | Значение | Source |
|---|---|---|
| Объём проанализированных рассылок | 62 млрд отправлений | `[conf:high, src:2026-05-06]` |
| Каналов анализа | email, SMS, мобильные push | `[conf:high, src:2026-05-06]` |
| Соотношение email/SMS у клиентов Mindbox | 26:1 (раньше было примерно 1:1) | `[conf:high, src:2026-05-06]` |
| Push vs email | push впервые превысили email на 45% | `[conf:high, src:2026-05-06]` |

## Причины сдвига

- **Подорожание SMS** — стоимость SMS-операторской рассылки выросла, экономика канала ухудшилась `[conf:high, src:2026-05-06]`
- **Блокировки мессенджеров** в РФ — компании потеряли часть pushes через мессенджер-боты и стали активнее использовать нативные мобильные push (через приложения) и email `[conf:high, src:2026-05-06]`
- **Email и push условно бесплатны** по сравнению с SMS — для маркетинга, который хочет частые касания, это критический фактор `[conf:high, src:2026-05-06]`

Mindbox изучили эффективность 62 млрд рассылок по доле в выручке, открытиям, кликам и конверсии в заказ `[conf:high, src:2026-05-06]`.

## Что это значит для маркетинга

- **SMS как retention-канал умирает** — оставлять SMS только для критичных триггеров (подтверждение заказа, OTP), массовые промо-рассылки переводить в push
- **Mobile push становится главным retention-каналом** — впервые количественно подтверждённо, что push обогнал email в коммерческих рассылках
- **Email не умер**, но его роль трансформировалась — больше «образовательный» формат с длинным контентом, меньше — оперативные триггеры
- **Стек CRM-агентств растёт** (см. [[evolving-strict/market-data/ru-crm-agency-market-2025]]) — рынок CRM-услуг +38% YoY, отражает увеличение спроса на грамотную orchestrate этих каналов [conf:low, src:2026-05-14]

## Связь с GRO

- **Push — приоритет № 1** для GRO как мобильного приложения. Mindbox-данные подтверждают, что инвестиции в push-инфраструктуру (сегментация, персонализация, частота, время отправки) дают непропорциональный возврат
- **Email — для long-form контента**: гайды, истории пользователей, ежемесячные дайджесты результатов. Не пытаемся email конкурировать с push в оперативности
- **SMS — только для критичных** триггеров (платёж, восстановление пароля), бюджет в SMS-маркетинг можно сократить и переложить в push-инфраструктуру

## Связанные страницы

- [[evolving-strict/market-data/ru-crm-agency-market-2025]] — параллельный сигнал: рынок CRM-услуг растёт +38%, отражает спрос на orchestrate этих каналов [conf:low, src:2026-05-14]
- [[evolving-strict/market-data/digital-ad-market-ru-2024-2026]] — общий контекст digital-рекламы в РФ
- [[evolving/industry-trends/ru-digital-regulatory-squeeze-2026]] — регуляторное давление на мессенджеры и блокировки как driver сдвига
- [[evolving/industry-trends/ru-telegram-blocking-max-migration-2026]] — блокировка мессенджеров → миграция в push/email
- [[volatile-strict/competitor-news/bilayn-prodvizhenie-ai-legal-block-sms-2026-05]] — supply-side контрапункт: на фоне оттока из SMS оператор (Билайн Adtech) снижает операционную стоимость SMS-промо AI-автоматизацией compliance (−8% reject'ов `[conf:high, src:2026-05-19]`)
- [[canon/marketing-frameworks/b2b-digital-transformation-case-patterns]] — кейс Банка Синара: каскад PUSH→SMS в омниканальном шлюзе (enterprise-валидация того же сдвига)
- [[sources/2026-05-14-tg-cossaru-may-5-14-2026]] — первоисточник
