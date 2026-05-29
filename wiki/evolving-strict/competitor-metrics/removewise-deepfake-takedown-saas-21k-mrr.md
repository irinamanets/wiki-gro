---
id: mkt:evolving-strict/competitor-metrics/removewise-deepfake-takedown-saas-21k-mrr
title: "RemoveWise — $21K MRR deepfake-takedown SaaS (bootstrap-кейс соло-фаундера)"
type: page
subtype: competitor
layer: evolving-strict
theme: competitor-metrics
tags: [saas-case, mrr, deepfake, high-ticket, bootstrap, cold-outreach, founder-led, recurring-revenue]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-your-pet-project-may-20-25-2026.md]
namespace: mkt
---

# RemoveWise — $21K MRR deepfake-takedown SaaS

Bootstrap-кейс, цитируемый Михаилом Табуновым в [[sources/2026-05-26-tg-your-pet-project-may-20-25-2026|посте 636 (2026-05-22)]]. RemoveWise — сервис удаления AI-дипфейков знаменитостей с YouTube/Facebook/TikTok и других платформ. Founder — Joe (фамилия не указана), бывший legal operations в YouTube/Google. Запущен ≈ноябрь-декабрь 2025 (6+ недель до первого платежа от момента увольнения, точная дата запуска не указана).

`confidence: medium`: цифры процитированы Табуновым из своего ресерча кейса; не верифицированы независимыми источниками (Stripe Dashboard / SimilarWeb / Crunchbase). Numerical claims даны с inline-маркерами для audit trail. Скриншот лендинга (см. source page) подтверждает порядок величин: 70 000+ deepfakes removed на dashboard'е консистентно с $21K MRR при чеке $2-5K (≈4-10 клиентов).

## Operational метрики

| Метрика | Значение | Source |
|---|---|---|
| MRR (Monthly Recurring Revenue) | $21 000 | `[conf:medium, src:2026-05-22]` |
| Чек на клиента | $2 000-5 000/мес | `[conf:medium, src:2026-05-22]` |
| Команда | Founder + 1 подрядчик на операционку | `[conf:medium, src:2026-05-22]` |
| Внешние инвестиции | $0 | `[conf:medium, src:2026-05-22]` |
| Время от первого cold-email до увольнения из Google | ≈ дни (5 emails → 3 ответа = pre-launch validation) | `[conf:medium, src:2026-05-22]` |
| Время от запуска до первого платежа | 6 недель | `[conf:medium, src:2026-05-22]` |
| Lifetime deepfakes removed (по лендингу) | 70 000+ | `[conf:medium, src:2026-05-22]` |
| Lifetime fraudulent views blocked | 320M+ | `[conf:medium, src:2026-05-22]` |

**Расчётные derivatives** (calculated):
- Предполагаемое количество клиентов: $21K / ($2-5K) = **4-10 платящих клиентов** на текущей выручке
- ARR (Annualized Run Rate): $252K `[conf:medium, src:2026-05-22]`
- Стоимость стека на старте: $0 (Excel + email-шаблоны + ручной мониторинг)

## Метрики дашборда RemoveWise (со скриншота лендинга)

Скриншот «Public Figure Protection Portal» (Live Monitoring Active, дата снапшота лендинга ≈ май 2026):

| Метрика | Значение |
|---|---|
| Videos removed | 9 247 `[conf:medium, src:2026-05-22]` |
| Total views removed | 14.2M `[conf:medium, src:2026-05-22]` |
| Audience protected (subscribers of offending channels) | 1.1M `[conf:medium, src:2026-05-22]` |
| Avg days to removal | 3.1d `[conf:medium, src:2026-05-22]` |
| Estimated diverted revenue (this month) | $42 600 (↑ $3 840 vs prev month, Conservative Est. $3 CPM) `[conf:medium, src:2026-05-22]` |
| Top threat sources (top channel total views removed) | 3.2M `[conf:medium, src:2026-05-22]` |
| Top threat sources (#5 channel total views removed) | 780K `[conf:medium, src:2026-05-22]` |

**Note:** dashboard'ные метрики — per-client view (не aggregate), скриншот вероятно демонстрирует one customer-tier. «70 000+ deepfakes removed» в top-bar лендинга = aggregate lifetime.

## Founder profile

| Параметр | Значение |
|---|---|
| Имя | Joe (фамилия не указана) `[conf:medium, src:2026-05-22]` |
| Предыдущая роль | Legal operations team, YouTube (Google) `[conf:medium, src:2026-05-22]` |
| Insider credential | «Лично участвовал в написании политики YouTube по удалению дипфейков» `[conf:medium, src:2026-05-22]` |
| Decision-trigger | Увидел проблему изнутри + 5 cold-email'ов → 3 ответа = pre-validation `[conf:medium, src:2026-05-22]` |

## Operational growth stack (как добывают клиентов)

1. **Mониторинг платформ** (YouTube, Facebook, TikTok и другие сайты) на дипфейки публичных персон
2. **Документирование** с пруфами (URL, просмотры)
3. **Cold email** — паттерн «вот что я нашёл про вас» (см. [[canon/marketing-frameworks/cold-outreach-with-found-problem-removewise]])
4. **LinkedIn follow-up** для тех, кто не ответил на почту
5. **Referral request** после онбординга (peer-network инфлюенсеров)
6. **SEO-блог** с long-tail запросами («how to remove a deepfake»)

## ICP (Ideal Customer Profile)

- **Кто:** инфлюенсеры, селебрити, публичные персоны с миллионной аудиторией
- **Что болит:** AI-дипфейки рекламируют от их имени крипто-скам, портят рекламные контракты
- **Почему YouTube self-service не работает:** жалобы отклоняются («не те поля, не те формулировки»)
- **Что покупают:** не tool, а **service** — мониторинг + жалоба по correct-template + follow-up до удаления
- **Готовность платить:** $2-5K/мес = премия за защиту репутации vs стоимость PA / legal ассистента ($5-15K/мес full-time)

## Defensible business model — почему «отвалиться нельзя»

Из тезисов Табунова:
- **Спрос растёт structurally:** технологии генерации дипфейков дешевеют → больше дипфейков → больше клиентов
- **Recurring inherent:** «сегодня удалили десять — завтра появятся пятнадцать новых»
- **LTV огромный:** churn практически нулевой (отвалиться = фейки появляются неконтролируемо = клиент возвращается)
- **Чем известнее человек, тем больше его лицо подделывают** — каждый клиент со временем становится дороже

«Идеальный Recurring Revenue.» `[conf:medium, src:2026-05-22]`

## Bootstrap-classification

| Критерий | Соответствие |
|---|---|
| Live на деньги клиента, не инвестора | ✅ ($0 investments) |
| Solo / micro-team | ✅ (founder + 1 contractor) |
| Запущен «на коленке» | ✅ (Excel + email scripts на старте) |
| Validation через прямую продажу | ✅ (5 emails → 3 ответа до запуска) |
| Founder ушёл из найма после validation | ✅ |

→ **Каноничный bootstrap-кейс**. Применимо к [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] как референс «как правильно».

## Сравнение с другими bootstrap-кейсами в вики

| Кейс | MRR/ARR | Команда | Ниша | Pricing |
|---|---|---|---|---|
| **RemoveWise** | $21K MRR ($252K ARR) | Founder + 1 | Deepfake takedown (B2C-celeb high-ticket) | $2-5K/мес |
| Wave AI | $7M ARR | Solo | (см. [[volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026]]) | — |
| Medvi | $401M revenue | Двое братьев + $20K | (см. там же) | — |
| Den's project (4th launch) | $9.2K за 2 месяца | Solo | (см. там же) | — |
| FaceKit | $110K за 4 месяца | Solo | AI-инфлюенсер app | — |

RemoveWise сидит между «маленьким Wave AI» и «средним Den's» по MRR. **Уникальность кейса в pricing-зоне** ($2-5K/мес = высокий чек для solo-founder'а с zero marketing budget'ом).

## Risks и caveats

- **Single source verification:** все цифры — от Табунова (founder-voice, не аудит). Возможные искажения: округление, marketing-tilt, выборка лучшего месяца.
- **Platform-dependency:** business model зависит от того, что YouTube/Facebook/TikTok принимают жалобы. Если платформы изменят policy в сторону auto-removal (что Joe сам помогал писать), TAM сжимается.
- **Regulatory landscape moving:** в США / ЕС обсуждается legislation про deepfake-labeling. Если законодательство решит проблему systemically — RemoveWise теряет основной use-case.
- **Competition:** at $21K MRR и $2-5K/мес чеке — это **очень тонкий рынок** (≤10 клиентов). Любой крупный игрок (Microsoft, Adobe, Reality Defender) может смести нишу за месяц, если решит зайти.

Эти риски — стандартные для **specialized B2C-celeb high-ticket SaaS** на ранней стадии; не обесценивают кейс как **операционный пример bootstrap-validation'а**.

## Связанные страницы

- [[canon/marketing-frameworks/cold-outreach-with-found-problem-removewise]] — operational pattern outreach'а кейса
- [[canon/marketing-frameworks/agent-vs-saas-pricing-arbitrage]] — RemoveWise — пример agent-pricing коридора ($2-5K/мес = service, не tool)
- [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] — каноничный bootstrap-кейс, иллюстрация рамки
- [[canon/marketing-frameworks/five-no-pet-project-tabunov]] — соответствие всем 5 НЕТ
- [[canon/marketing-frameworks/zero-to-one-vs-scale-tabunov]] — кейс сейчас в zero-to-one фазе (ручной онбординг, один канал)
- [[canon/marketing-frameworks/social-proof-traffic-asset-framework-tabunov]] — pruefs «70 000+ deepfakes removed» на лендинге
- [[evolving/industry-trends/deepfake-removal-saas-market-2026]] — макро-тренд индустрии
- [[volatile-strict/industry-news/ai-solopreneur-cases-jan-apr-2026]] — каталог других bootstrap-кейсов для сравнения
- [[sources/2026-05-26-tg-your-pet-project-may-20-25-2026]] — первоисточник (пост 636)
