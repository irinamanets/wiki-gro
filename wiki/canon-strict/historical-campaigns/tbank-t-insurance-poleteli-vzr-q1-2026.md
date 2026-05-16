---
id: mkt:canon-strict/historical-campaigns/tbank-t-insurance-poleteli-vzr-q1-2026
title: Т-Страхование ВЗР POLETELI — промо Q1 2026 (скидка 10% + розыгрыш 1,1 млн ₽)
type: page
subtype: campaign
layer: canon-strict
theme: historical-campaigns
tags: [competitor, t-bank, t-insurance, travel-insurance, promo, sweepstakes, telegram, creative-reference]
confidence: high
stale: false
created: 2026-04-17
updated: 2026-04-17
sources: [sources/2026-04-14-tg-tinkoffbank-10537-vzr-poleteli.md]
namespace: mkt
---

# Т-Страхование ВЗР POLETELI — промо Q1 2026

Потребительская промо-кампания АО «Т-Страхование» (входит в Т-Банк-группу) по ВЗР-страхованию (выездное страхование путешественников). Кампания размещалась в потребительском Telegram-канале [@tinkoffbank](https://t.me/tinkoffbank) (пост [#10537](https://t.me/tinkoffbank/10537)) с креативным bundle из двух изображений. `[conf:high, src:2026-04-14]`

## Временные рамки

| Параметр | Значение | Source |
|---|---|---|
| Наблюдение креатива | 2026-04-14 (backfill в raw-очередь) | `[conf:high, src:2026-04-14]` |
| Дедлайн акции | до **29 марта 2026** (подразумеваемый год) | `[conf:high, src:2026-04-14]` |
| Фаза на момент записи | post-campaign (кампания завершилась ~2 недели до ingest'а) | `[conf:high, src:2026-04-17]` |

## Механика

| Элемент | Параметр | Source |
|---|---|---|
| Промокод | `POLETELI` | `[conf:high, src:2026-04-14]` |
| Скидка по промокоду | **-10%** на полис ВЗР | `[conf:high, src:2026-04-14]` |
| Призовой фонд (sweepstakes) | **1 100 000 ₽** общий | `[conf:high, src:2026-04-14]` |
| Главный приз | **1 × 300 000 ₽** | `[conf:high, src:2026-04-14]` |
| Средний уровень | **3 × 100 000 ₽** | `[conf:high, src:2026-04-14]` |
| Массовый уровень | **10 × 50 000 ₽** | `[conf:high, src:2026-04-14]` |
| Всего победителей | **14 человек** | `[conf:high, src:2026-04-14]` |
| Гарантированный приз | кэшбэк **20%** в «Супермаркетах в Городе», до **300 ₽** | `[conf:high, src:2026-04-14]` |
| Landing | `https://u.tbank.ru/vzr-promo` | `[conf:high, src:2026-04-14]` |
| Страховщик | АО «Т-Страхование», лицензии ЦБ РФ СЛ/СИ/ОС № **0191** | `[conf:high, src:2026-04-14]` |

## Tiered-prize архитектура

Распределение призового фонда построено по убывающей пирамиде (300k → 100k → 50k), но именно *соотношение числа победителей* сделано намеренно нелинейным:

| Уровень | Шанс на уровне | Долевой вес фонда | Роль в мотивации |
|---|---|---|---|
| 1 × 300 000 ₽ `[conf:high, src:2026-04-14]` | 7% победителей | 27% фонда | aspirational hero — заголовок креатива |
| 3 × 100 000 ₽ `[conf:high, src:2026-04-14]` | 21% победителей | 27% фонда | mid-tier credibility — «реально выиграть большое» |
| 10 × 50 000 ₽ `[conf:high, src:2026-04-14]` | 71% победителей | 45% фонда | mass reach — повышает perceived odds |

**Маркетинговое следствие.** Hero-цифра (300 000) выполняет attention-функцию в креативе, а mass-tier (50k × 10) — функцию «розыгрыш реально работает, шансов много». Этот паттерн — reusable для любой sweepstakes-промо-механики: см. [[evolving/content-trends/sweepstake-promocode-combo-mechanics]].

## Комбо-формула «скидка + розыгрыш + дедлайн»

Кампания объединяет **три разных мотиватора** в одной акции:

1. **Promocode -10%** `[conf:high, src:2026-04-14]` — rational reward для уверенных в покупке пользователей (закрывает холодных колеблющихся по цене).
2. **Sweepstakes 1,1M ₽** — emotional hope-reward для колеблющихся по необходимости (закрывает «не было бы страховки, если бы не шанс выиграть»).
3. **Дедлайн 29 марта** — urgency-trigger для прокрастинирующих (закрывает «подумаю позже»).

Каждый элемент закрывает свой психологический сегмент. По framework'у [[evolving/content-trends/urgency-window-launch-playbook]] это стандартная launch-playbook формула, адаптированная для страхового продукта.

## Креативный bundle — два изображения с разделением функций

Креатив поставлен как **carousel из двух изображений**:

- **#10537 (hero).** `[conf:high, src:2026-04-14]` Чемодан с пачками денег в бирюзово-жёлтой палитре Т-Страхования. Заголовок: «Покупайте полис для путешествий и участвуйте в розыгрыше до 300 000 ₽». Жёлтый контрастный тег-купон `POLETELI` с надписью «–10% по промокоду до 29 марта». Функция: attention + offer.
- **#10538 (mechanics detail).** Белая карточка с 3 иконками (🎁💧⭐) и прозрачной иерархией призов. Функция: credibility + specifics.

Разделение функций между креативами позволяет алгоритму TG поймать более длительный dwell-time от пользователей, листающих carousel (второй креатив прочитывают только те, кто заинтересовался первым).

## Caption-hook: emoji-poll перед CTA

Caption начинается с **эмоджи-опроса** («в отпуске вы обычно: 👍/😎/❤️»), а не с прямого продаж­ного hook'а. Это даёт:
- Low-barrier engagement (реакция вместо покупки) — кормит алгоритм канала перед hard-sell'ом.
- Self-segmentation аудитории (активные vs пассивные путешественники) — пригодится для retargeting по реакциям.
- Soft-start тон: сначала игровой вопрос, потом офер.

Детальнее паттерн разобран в [[evolving/content-trends/sweepstake-promocode-combo-mechanics]] → секция «Emoji-poll softener перед hard-sell».

## Multi-channel CTA

Внизу поста — три канала подписки:

- **МАКС** (u.tbank.ru/maxtbank) — официальный мессенджер РФ, активно продвигается с 2026-03-30 (см. [[evolving/competitor-positioning/max-messenger]]).
- **ВКонтакте** (u.tbank.ru/vktbank)
- **Telegram @tbank** (t.me/tbank)

Порядок «МАКС → ВКонтакте → Telegram» — политический сигнал: Т-Банк ставит national RU-messenger первым в cross-promo, что отражает общую тенденцию больших RU-брендов по импортозамещению каналов дистрибуции.

## Регуляторная подпись

Оба креатива содержат юридическую подпись внизу мелким серым шрифтом:

> АО «Т-Страхование», лицензии ЦБ РФ СЛ № 0191, СИ № 0191, ОС № 0191 - 03

Паттерн допустимой legal-компоновки для страховых креативов: полная юр.подпись, но не мешает восприятию — расположена в нижнем углу, минимальный контраст, не конкурирует с hero-текстом. Relevant для любой страховой или financial-service рекламы. См. [[canon-strict/legal-claims/ad-marking-russia-2026]] для сопоставления с общими требованиями маркировки РФ.

## Application для GRO

- **Прямая неприменимость.** GRO — не страховой продукт, промо с 14 денежными призами и лицензионной подписью — не наш масштаб (нужны лицензированный страховщик + призовой фонд на миллион ₽).
- **Извлечённая механика `discount + sweepstake + deadline`** — адаптируется на любой launch/promo: скидка на годовую подписку + розыгрыш подарка (в нашем случае — годовой подписки GRO) + дедлайн. Масштаб призового фонда может быть в 100× меньше, структурная логика сохраняется.
- **Emoji-poll как soft-opener** перед промо — прямо переносимо в собственные TG-каналы GRO. Например: «Как у вас идёт тренировочный цикл? 💪 — на пике / 😴 — пропустил неделю / 🔥 — вхожу в новый сезон». Потом промо-офер.
- **Tiered-prize иерархия (27/27/45)** — если когда-либо будет sweepstakes, пирамида «1 hero / 3 mid / 10 mass» — готовый шаблон распределения, протестированный крупным игроком.
- **Бренд-визуал «чемодан с деньгами»** — универсальный travel-insurance стандарт, не стоит копировать в fitness-категорию; но принцип «одно мощное заглавное изображение-метафора + второй детализирующий креатив» переносимо.

## Связанные страницы

- [[evolving/content-trends/sweepstake-promocode-combo-mechanics]] — reusable паттерн промо-формулы
- [[evolving/content-trends/telegram-native-formats]] — нативные форматы TG, в т.ч. emoji-polls
- [[evolving/content-trends/urgency-window-launch-playbook]] — launch-playbook с urgency-дедлайном
- [[canon-strict/legal-claims/ad-marking-russia-2026]] — требования маркировки рекламы в РФ
- [[evolving/competitor-positioning/max-messenger]] — положение MAX как cross-promo канала для RU-брендов
- [[volatile-strict/competitor-news/yandex-direct-opora-promo-2026-04]] — сопоставимая промо-акция другого крупного RU-игрока
- [[sources/2026-04-14-tg-tinkoffbank-10537-vzr-poleteli]] — первоисточник с обоими креативами

## Backlinks

_10 pages link to this one._

- [[canon-strict/historical-campaigns/tbank-sdelka-real-estate-escrow-launch-2026]]
- [[canon-strict/historical-campaigns/tbank-tinvest-tolk-pro-2026-04]]
- [[evolving/competitor-positioning/tbank-tinvest-premium-positioning]]
- [[evolving/content-trends/branded-show-format-t-bank-stars-vs-fraudsters]]
- [[evolving/content-trends/event-speaker-carousel-format]]
- [[evolving/content-trends/sweepstake-promocode-combo-mechanics]]
- [[evolving/content-trends/telegram-native-formats]]
- [[index]]
- [[sources/2026-04-14-tg-tinkoffbank-10537-vzr-poleteli]]
- [[sources/2026-04-17-tg-tinkoffbank-10539-tolk-pro-speakers]]
