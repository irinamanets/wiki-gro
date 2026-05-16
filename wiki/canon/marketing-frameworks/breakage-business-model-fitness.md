---
id: mkt:canon/marketing-frameworks/breakage-business-model-fitness
title: "Breakage business model — продукт, который большинство не использует (фитнес-кейс 91%)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [subscription, retention, smb, fitness, saas, pricing, low-usage, renewal, founder-playbook]
confidence: medium
stale: false
created: 2026-05-06
updated: 2026-05-15  # +self-service single-operator extension паттерна (Суворов/Фитбейс через Inc. Russia 36713): автоматизация **усиливает** breakage через убирание human-touch
sources: [sources/2026-05-05-yt-biznes-s-nulya-fitness-club-economics.md, sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc.md, sources/2026-05-14-tg-incrussiamedia-may-5-11-2026.md]
namespace: mkt
---

# Breakage business model

**Breakage business model** — категория subscription-бизнесов, в которых **большинство клиентов сознательно или несознательно НЕ используют купленный продукт активно**, и это не баг/риск, а **explicit core economic mechanism** модели. Цена и юнит-экономика рассчитываются с предположением низкого usage; если бы все купившие начали реально пользоваться — модель **физически не справилась бы**.

Канонический RU SMB-кейс: фитнес-клубы. По данным founder-интервью Ильи в подкасте «Бизнес с нуля» 2026-05-05 ([[sources/2026-05-05-yt-biznes-s-nulya-fitness-club-economics]]), **91% базы абонементов клуба в Невском районе СПб посещают клуб 1–3 раза за весь годовой цикл**. Это не аномалия отдельного клуба, а отраслевая константа.

## Структурная диагностика breakage-модели

Бизнес работает на breakage если совпадают **три условия**:

1. **Capacity floor < paid base** — физическая/операционная мощность продукта ниже количества активных клиентов. Если бы все покупатели использовали продукт регулярно — мощность переполнилась бы (фитнес: 25 000 базы × 3 посещения/неделя = 7 500 посещений/день, помещение 2000 м² не примет).
2. **Low engagement self-selecting** — продукт привлекателен **в момент покупки** (resolution, FOMO, social proof), но требует регулярного активного действия для использования. Customer voluntarily оплачивает, потом не приходит — без принуждения, без чувства вины (или с чувством вины, которое **дополнительно драйвит renewal**).
3. **Low average ticket + autorenewal-friendly mechanics** — индивидуальная цена низкая (~1 000 ₽/мес equivalent), что снижает порог принятия решения «продлить» по сравнению с порогом первой покупки.

Когда эти три условия срабатывают одновременно, **breakage становится business-model**, а не побочным эффектом плохого продукта.

### Self-service single-operator extension паттерна

Второй экземпляр breakage-cluster'а зафиксирован у Василия Суворова (founder экосистемы «Фитбейс») в колонке на Inc. Russia 2026-05-05 ([[sources/2026-05-14-tg-incrussiamedia-may-5-11-2026|пост 36713]]): self-service фитнес 100–200 м², один оператор, мобильное приложение + автоматизация заменяют ресепшен и отдел продаж, годовой потолок до **7 млн ₽**. Все три условия breakage соблюдены, но **усиленно**:

- **Capacity floor резко уменьшен** (100–200 м² вместо 2000 м²), `paid base` пропорционально уменьшена («несколько сотен» vs 25 000)
- **Engagement-trigger ослаблен**: убрана human-touch (ресепшен, тренеры в зале, отдел удержания) → no-show усиливается, а не лечится
- **Auto-renewal встроена в приложение** (стандартный subscription paradigm)

**Ключевой инсайт паттерна**: **автоматизация → усиление breakage**, а не противоядие от него. Self-service модель — это не «исправленный» breakage, а **более чистая** его реализация: убрав human-touch, founder убрал последний reason для customer прийти (вижу тренера = чувствую обязательство), что **product-design choice** на стороне максимизации breakage. См. полный playbook на [[canon/marketing-frameworks/self-service-fitness-model-2026]].

## Канонические примеры за пределами фитнеса

| Категория | Breakage signal | Капитал-расход модели |
|---|---|---|
| Спортзалы / фитнес-клубы | 91% базы 1-3 посещения/год (RU 2026) | Помещение, оборудование |
| Языковые приложения | 80%+ инсталлов off в первый месяц | Тарифы, retention-механики, native ads |
| Online-курсы (massive self-paced) | <10% completion rate | Контент-производство (one-time) |
| Подарочные сертификаты (gift cards) | 10–30% не активируются совсем | Эмиссия, accounting (US Generally Accepted Accounting Principles разрешают признавать выручку через 2 года unredeemed) |
| Магазины-членства (warehouse club, e.g. Costco) | средний customer redemption ниже maximum | Помещение, инвентарь |
| Software trials → paid subscriptions | Many subscribe → don't use → forget to cancel | Хостинг, поддержка |
| Streaming-сервисы (часто называется «zombie subscribers») | 22–34% подписчиков не использовали >30 дней (Deloitte/Antenna) | Контент-лицензии |

GRO принадлежит к категории productivity-app, поэтому breakage-сценарий **прямо применим** при определённом дизайне retention-механик.

## Механика монетизации в breakage-модели

Breakage-бизнес зарабатывает в **3 этапа**:

### Этап 1: Acquisition — продать тем, кто верит, что использует

- **Психологический триггер покупки:** New Year resolution, после врача-отзыва, после социального события (свадьба, отпуск, фотосессия)
- **Низкая цена unit pricing**: 17 900 ₽/год → ~1 500 ₽/мес equivalent — порог решения ниже, чем 200 000 ₽ персональный тренер
- **High intent в момент acquisition**: customer честно планирует ходить
- **Channels for acquisition**: VK-сообщество с тренировочным контентом, наружка, амбассадоры-спортсмены, корпоративные абонементы (B2B-канал — собственники бизнеса для своих сотрудников)

### Этап 2: Активация — пусть приходят 1-3 раза

- **Не отпугивать** при первой попытке: должна быть «горячая вода, более-менее необшарпанные стены, среднее оборудование» (Илья: «за 1 300 ₽/мес у нас есть это всё»)
- **Не пытаться навязать привычку**: customer сам решает, формирует ли её
- **Социальная составляющая** (групповые занятия 50 в неделю в кейсе Ильи) — для женской аудитории, которая **более склонна к продлению** через социальные связи в зале
- **Детские секции** — захват семьи, не только индивидуального customer'а: «отвезти ребенка на занятия, при этом самой пойти на йогу» = повышение average lifecycle через **multi-member household lock-in**

### Этап 3: Renewal — где делается основная маржа

Это **ключевой момент** breakage-модели:

- Customer не использует продукт, но получает **renewal-сообщение** через 11 месяцев
- Менеджер/sms/email напоминает «у нас сегодня акция, только сегодня, только сейчас, для вас как клиента — за 15 900 ₽ продлим, заморозку подарим, массаж, ещё что-нибудь» — стандартный bundle-extension
- Customer-психология: **«я заплатил год, ничего не использовал — стыдно бросать сейчас»** + **«если откажусь, я подтверждаю, что прошлый год был зря»** + cashback ещё не использованный = легко проходит порог «да, продлеваю»
- **Luft по цене** для торгующихся клиентов: если customer звонит и торгуется, менеджер может опуститься до 9 900 ₽ — но **только полугодовой**, не годовой. Это защищает price anchor от erosion. Потолок переговоров определён сезоном (летом проще договориться, осенью — нет)

В кейсе Ильи: **продляемость 70%** базы — это threshold для health, ниже — «начнутся вопросы». То есть **70% покупателей, не используя продукт, его перепокупают**.

## Implications для marketing-нарратива

### Для founder'а breakage-бизнеса

**1. Не извиняться за breakage** — это не дефект продукта. Это feature рынка. Любой моральный дискомфорт founder'а вокруг «они платят и не используют» — это **personal, не business issue**. Customer **выбирает** не использовать; founder обеспечил доступ.

**2. Renewal-CAC должен быть **меньше**, чем acquisition-CAC** — потому что renewal-customer уже в базе, контактные данные есть, история есть, payment-method часто сохранён. Ratio acquisition-CAC : renewal-CAC должно быть 5×–10× в пользу renewal.

**3. Не отговаривать customer'а от покупки если он не уверен «буду ли ходить»** — это самоповреждение. Если customer проявил intent, его можно конвертить. Что произойдёт после — это его responsibility, не ваша.

**4. Сегментация клиентов по usage** — не для **product-marketing**, а для **renewal-marketing**:
- High usage (5%) — power users, для которых акции не нужны, они продлят сами или попросят бонус
- Medium usage (~10%) — выборочные пользователи, чувствительны к **personalization** в renewal-сообщении
- Low usage (91% base) — те самые, для кого работает «акция только сегодня», им нужен **низкий порог решения** + permission («заморозим, потом активируете»)

### Для продуктового маркетинга B2B (GRO как пример)

**Если GRO продаёт founder'у бизнеса**, и этот founder сам в breakage-бизнесе — нарратив о productivity-app **может прямо упоминать breakage-параллель**: «вы же продаёте абонемент, который большинство не использует. Так и с productivity-app — низкий usage не делает её бесполезной».

Это **identification hook**: founder узнаёт свою модель, понимает, что не нужно стесняться.

**Hook-формулировка:**
> «Не каждый день вы будете планировать. Это нормально. Не каждый ваш клиент тренируется в зале — но вы спокойно продаёте абонементы. Так же спокойно купите GRO. Дни, когда не пользуетесь, **не делают вас плохим founder'ом** — они делают вас обычным человеком, как 91% ваших же клиентов.»

### Для UX/onboarding

**1. Не наказывать low usage** — никаких «вы не пользовались уже 7 дней!» сообщений. Customer **уже** заплатил. Стыд — это противоположность retention.

**2. Маленькие касания вместо больших onboarding'ов** — если customer не использует продукт регулярно, **не нужно** заставлять его проходить 10-шаговый onboarding. Один шаг при заходе. Если возвращается через 2 недели — снова один шаг. Минимизация re-onboarding cost.

**3. Renewal-prompt timing** — за 30 дней до окончания, не на 365-й день. Customer должен **успеть** обработать решение, не чувствовать «я не успел отписаться».

**4. Pause/Freeze как retention-feature** — Илья даёт «заморозим до сентября» при renewal. В SaaS аналог = «pause subscription for 30 days without losing data». Сильнее, чем downgrade.

## Anti-patterns

### 1. Try to maximize usage at all costs

Если customer **не использует** ваш продукт, и вы вкладываете maximum effort в его активацию — вы можете:
- Раздражить low-engagement пользователей до точки churn'а
- Повысить себестоимость retention за счёт CRM/email/push-инфраструктуры
- Передать сигнал «вам стыдно, что не пользуетесь» — обратное retention

Multi-channel re-engagement-кампания для **всех** пользователей одинаково — это шотгана. Сегментируйте.

### 2. Punish breakage with restrictions

«Если ваш месяц прошёл, вы должны заплатить 50% pen alty» — это убивает renewal probability. Пускай customer покупает по своей psychological dynamic, не по контракту-mandate.

### 3. Public shame about breakage

«Большинство наших клиентов не используют продукт» — **никогда не говорите это публично**. Это эзотеричная информация для founder'а, но для customer-нарратива это **destroys positioning**. Customer хочет верить, что **именно он** будет использовать. Дайте ему эту веру.

### 4. Chase 100% engagement

Engagement = 100% requires capacity scaling, что разрушает unit-economics. Целиться надо в **healthy plateau** (для фитнеса ~70% продление при ~9% активном usage; для SaaS varies, но обычно 30-50% MAU/total subs = healthy).

### 5. Confuse breakage with bad product

Breakage ≠ плохой продукт. Customer **выбирает** не использовать. Если продукт настолько плох, что customer **не может** использовать — это другое (и customer не продлит). Различайте: «no-show» vs «can't-show».

## Связь с другими фреймворками вики

- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] — operational philosophy, что продукт можно запускать «колхозно» — потому что customer всё равно не пользуется им активно в первый период
- [[canon/marketing-frameworks/business-metrics-for-owners]] — breakage rate как **обязательная метрика** для subscription-бизнеса, наряду с MAU/MRR/Churn
- [[canon/marketing-frameworks/defector-loyalty-crm-analysis]] — комплементарная оптика: если breakage low (все используют), но defector rate high (все уходят) — это **другой** product-market issue
- [[canon/target-audience/ru-smb-founder-owner-seller]] — сегмент, для которого нарратив идентификации с breakage-моделью особенно резонантен

## Complementary mechanic: service-as-retention (rental-businesses)

В соседнем rental-бизнесе с rotating-asset утилизацией (электробайк-rental Муратаева, выпуск #4: [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]]) retention-механика **противоположна** breakage'у: customer **физически приходит каждую неделю** (продлить аренду), и founder намеренно держит **физический сервис на месте** как retention-asset.

| Свойство | Breakage (фитнес) | Service-as-retention (rental) |
|---|---|---|
| Customer engagement | Низкий (1-3 посещения/год) | **Высокий** (приходит каждую неделю продлевать) |
| Renewal trigger | Психологический (стыдно бросать) | **Operational** (нужен исправный байк) |
| Retention-mechanism | Subscription auto-renewal | **Quality service в кадре** + переманенный технарь |
| Breakage-attitude | Это feature модели | Это failure (нерабочий байк = churn) |
| Capacity-stress | Низкий (большинство не пользуется) | **Высокий** (все пользуются всегда) |

**Insight**: rental-бизнесы с **physical asset** (байки, машины, оборудование) — **противоположность** subscription-бизнесов с виртуальным asset (фитнес, SaaS). Retention строится не на «забыли отписаться», а на **«видим что есть кому починить»**. Это complement breakage-модели, не альтернатива — два разных category business-model'и в subscription space.

## Каноническое vs evolving

Эта механика **canon** (стабильна по природе subscription-бизнесов в любой экономике), но её **конкретные numbers** (91% breakage rate, 70% renewal threshold, 17 900 ₽ avg ticket) дрейфуют — это [[evolving-strict/market-data/ru-fitness-club-unit-economics-2026]].

Когда GRO проводит quarterly review своей retention-стратегии, общая теория breakage здесь — стабильный input. Конкретные RU SMB benchmarks обновляются через evolving-strict pages.

## Связанные страницы

- [[sources/2026-05-05-yt-biznes-s-nulya-fitness-club-economics]] — anchor-источник
- [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]] — complementary case (rental-бизнес = service-as-retention, противоположная механика)
- [[evolving-strict/market-data/ru-fitness-club-unit-economics-2026]] — конкретные RU 2026 numbers
- [[evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026]] — соседняя rental unit-economics (electric bike rental, противоположная retention-структура)
- [[canon/marketing-frameworks/b2b-pivot-anchor-customer-smb]] — adjacent-pattern для recurring-revenue в rental businesses
- [[evolving/industry-trends/ru-fitness-market-2016-2026]] — динамика breakage в условиях subscription-disruption
- [[canon/marketing-frameworks/business-metrics-for-owners]] — breakage как одна из ключевых метрик
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] — пересечение operational ideology
- [[canon/target-audience/ru-smb-founder-owner-seller]] — ICP-сегмент, для которого identification hook резонирует
- [[canon/marketing-frameworks/defector-loyalty-crm-analysis]] — комплементарная оптика defection vs breakage

## Backlinks

_14 pages link to this one._

- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]]
- [[canon/marketing-frameworks/b2b-pivot-anchor-customer-smb]]
- [[canon/marketing-frameworks/business-metrics-for-owners]]
- [[canon/marketing-frameworks/construction-site-content-marketing]]
- [[canon/marketing-frameworks/profit-share-service-revenue-smb]]
- [[canon/marketing-frameworks/trainer-rental-marketplace-model]]
- [[evolving-strict/market-data/ru-electrobike-rental-couriers-unit-economics-2026]]
- [[evolving-strict/market-data/ru-fitness-club-unit-economics-2026]]
- [[evolving/content-trends/biznes-s-nulya-founder-diy-format-2026]]
- [[evolving/industry-trends/ru-fitness-market-2016-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-yt-biznes-s-nulya-electrobike-month4-bilanc]]
- [[sources/2026-05-05-yt-biznes-s-nulya-fitness-club-economics]]
