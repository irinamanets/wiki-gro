---
id: mkt:canon/product-knowledge/gro-rustore-listing
title: GRO — листинг в RuStore (Android, RU)
type: page
subtype: asset
layer: canon
theme: product-knowledge
tags: [product, rustore, android, distribution]
confidence: high
stale: false
created: 2026-04-10
updated: 2026-04-10
sources: [sources/2026-04-10-gro-rustore-listing.md]
namespace: mkt
---

# GRO — листинг в RuStore (Android, RU)

Каноническая справка о том, как GRO выглядит в RuStore (российский магазин приложений VK) на 2026-04-10. Это третья и — на данный момент — последняя ingested точка дистрибуции продукта после [[canon/product-knowledge/gro-app-store-listing|App Store iOS]] и [[canon/product-knowledge/gro-google-play-listing|Google Play]]. RuStore особенно важен в российском Android-сегменте: часть устройств поставляется без Google Services, и для таких пользователей RuStore — единственный легальный канал установки GRO.

Задача страницы — быть reference-точкой для контент- и CPA-команды: какая сейчас версия в RuStore-сборке, в какой категории GRO там числится, сколько установок, какие permissions запрашивает и чем подача отличается от Apple/Google.

## Техническая конфигурация

- **Package ID:** `pro.gro` — единый со всеми другими платформами ([[canon/product-knowledge/gro-app-store-listing|App Store]], [[canon/product-knowledge/gro-google-play-listing|Google Play]]).
- **Текущая версия:** **1.6.14** `[conf:high, src:2026-04-10]`. **Совпадает с App Store и Google Play** — кроссплатформенный релиз покрывает и RuStore.
- **Дата последнего обновления:** **30 мар 2026** `[conf:high, src:2026-04-10]` — день-в-день с Google Play (в App Store — 31 марта по UTC).
- **Размер установки:** **49,1 МБ** `[conf:high, src:2026-04-10]`. В App Store то же приложение весит 77,6 МБ — разница нормальная (APK без iOS-фреймворков).
- **Минимальный Android:** **7.0** `[conf:high, src:2026-04-10]` — совпадает с Google Play, покрывает ~99% активных Android-устройств в РФ.
- **Категория в RuStore:** **«Бизнес-сервисы»** `[conf:high, src:2026-04-10]`.
- **Тег внутри категории:** «Личные помощники» — первый раз, когда слово «помощник» из нового стор-канона («помощник в принятии решений») закреплено как формальный тег внутри стора.
- **Возрастной рейтинг:** **0+** `[conf:high, src:2026-04-10]`. Третья разная шкала: Apple 16+, Google Play (IARC) 3+, RuStore 0+. Все три валидны, системы разные.
- **Запрашиваемые permissions:** Местоположение (единственное раскрытое разрешение).
- **Модерация:** пометка «Проверено вручную и антивирусом» — служебный бэйдж RuStore, маркетингового веса не имеет.

## Провайдер и юрлицо

- **Developer name (видимый в карточке RuStore):** **«ООО ГРО»** `[conf:high, src:2026-04-10]`.
- **Developer website:** `https://groapp.ru/`.
- **Support email:** **`legal@gro.pro`** — тот же, что в [[canon/product-knowledge/gro-google-play-listing|Google Play]]. Подтверждает, что `gro.pro` — устойчивый legal/support-домен команды, используемый стабильно в обоих Android-сторах.

**Ключевое отличие от iOS/Google Play-дистрибуций.** В App Store publisher — `Romsfort East Advisory Management Consultancies LLC` (Дубай), в Google Play — `Romsfort East`. В RuStore publisher — **непосредственно российское ООО ГРО**, без посредника-нерезидента. То есть команда держит **две параллельные корпоративные ветки дистрибуции**:

| Канал | Publisher (видимый) | Legal entity |
|---|---|---|
| App Store iOS | Romsfort East Advisory Management consultancies LLC | © ООО "ГРО" в копирайте |
| Google Play | Romsfort East | Romsfort East Advisory Management Consultancies L.L.C (Dubai, UAE) |
| RuStore | **ООО ГРО** | ООО ГРО |

Это типовой паттерн для российских B2C-продуктов после 2022-го: зарубежный publisher (Dubai) под глобальные стора Apple/Google для обхода платёжных и санкционных ограничений; российское юрлицо под RuStore, где требование «российский разработчик» встроено в политики VK-стора. Маркетинговый вывод — **в контенте эти юрлица не цитировать**; «кто делает GRO» коммуницируется через founders (см. [[canon/product-knowledge/gro-team]]).

## Установки и социальное доказательство

Числа (bucket установок, рейтинг 0,0) живут в дрейфующих метрик-страницах:
- Установки — [[evolving-strict/product-metrics/gro-store-installs]]
- Рейтинги — [[evolving-strict/product-metrics/gro-store-ratings]]

На момент последнего ingest-а RuStore показывал первый bucket «до 1 тыс» без раскрытия точного числа и явное «0,0 / Нет оценок» — ни одной пользовательской оценки и ни одного видимого отзыва.

**Вывод для distribution-стратегии** (устойчивый). RuStore-канал GRO **ещё более пустой, чем Google Play**. При этом RuStore — **обязательный канал для части российских устройств** (без Google Services), игнорировать нельзя. Рекомендации:

- **Любой CPA-креатив, ведущий в RuStore, должен нести собственный proof** (testimonial-цитата, скриншот-отзыв с лендинга), потому что внутри листинга GRO социального доказательства нет вообще.
- **Приоритет на ближайшие месяцы — собрать первые 20–50 оценок в RuStore**: попросить ранних пользователей, встроить in-app review prompt (если RuStore SDK его поддерживает), опросить команду.
- **Текстовые testimonials с лендинга** (см. [[canon/product-knowledge/gro-testimonials]]) — не могут быть перенесены напрямую в сам листинг RuStore, но могут быть контентом вокруг креатива.
- **Не запускать масштабные paid-CPA** под RuStore до появления первых оценок — ROI будет проседать из-за пустой карточки.

## Позиционирование в листинге

RuStore-описание **дословно совпадает с App Store и Google Play-описаниями**. Та же новая рамка («GRO — помощник в принятии решений и личном росте»), те же блоки «Кому подойдёт GRO», «Как это работает», «Что ты получаешь», тот же anti-positioning («это не курсы и не советы», «на рынке много приложений про мотивацию…»). Треки совпадают с обоими другими сторами: **карьера, деньги, коммуникации, мышление, фокус, продуктивность**.

**Ключевое наблюдение: три из трёх ingested сторов используют один и тот же store-канон.** Это третье независимое подтверждение того, что новая рамка «помощник в принятии решений» и новый набор треков — устойчивая каноническая подача GRO в мобильной дистрибуции. Лендинг groapp.ru с его «ежедневным тренажёром» и старым набором треков (продажи, маркетинг, коммуникации, цели, мышление, мотивация) теперь выглядит окончательно изолированным — один против трёх. Гипотеза «лендинг устарел и ждёт апдейта» становится доминирующей. См. `## Contradictions` в [[canon/product-knowledge/gro-app-overview]].

## Треки (предметные области)

Явно перечислены шесть:

- карьера
- деньги
- коммуникации
- мышление
- фокус
- продуктивность

**Идентично App Store и Google Play**, **отличается от лендинга**. Разнобой устойчив и теперь подтверждён тройной выборкой стор-источников.

## Категории: три разных выбора

Любопытное наблюдение: GRO числится в разных категориях в трёх сторах:

| Стор | Категория | Характер |
|---|---|---|
| App Store | Бизнес | business-вертикаль |
| Google Play | Стиль жизни / LIFESTYLE | lifestyle-вертикаль |
| RuStore | Бизнес-сервисы | business-вертикаль |

**Два из трёх стора (Apple и RuStore) выбрали business-вертикаль; только Google Play — lifestyle.** Возможные причины:

- **Осознанное A/B** под разные аудитории стор (Google Play-пользователи в РФ скорее ищут lifestyle-контент, чем бизнес-инструменты).
- **Ошибка / инерция при публикации** — вероятность тоже ненулевая.
- **Разная таксономия сторов** — в App Store и RuStore есть удобная категория «Бизнес», в Google Play эквивалента нет, команда выбрала ближайшее.

Это не противоречие, а открытый продукт-вопрос к команде: осознанно ли GRO в Google Play оказалось в lifestyle, и если осознанно — есть ли отдельная креативная подача под эту аудиторию? Фиксируется как gap в [[overview]].

## In-app purchases

**RuStore не раскрывает IAP на публичной странице каталога.** В отличие от [[canon/product-knowledge/gro-app-store-listing|App Store]] с явным IAP-разделом и [[canon/product-knowledge/gro-google-play-listing|Google Play]] с агрегированным диапазоном «От 2 490,00 ₽ до 2 990,00 ₽ за товар», в RuStore нет ни списка встроенных покупок, ни диапазона цен. В описании приложения есть только фраза «(Доступ ко всем трекам и функциям — по подписке)», без цифр.

Для [[canon/product-knowledge/gro-pricing|ценовой каноники]] это означает:

- RuStore **не даёт** третьего независимого подтверждения цены 2 490 / 2 990 ₽ — просто потому что RuStore-каталог не показывает IAP.
- RuStore **не противоречит** App Store и Google Play — цена просто скрыта до установки.
- Если появится подозрение, что команда держит разный ценовой оффер в разных сторах, верификация делается установкой из RuStore на реальное устройство. Пока таких подозрений нет.

## Release notes

RuStore в блоке «Что нового» показывает для версии 1.6.14 (30 мар 2026):

> Обновлена диагностика и главная страница

Это **другая формулировка**, чем в App Store (где release-note — «Теперь подборки тренажеров подобраны индивидуально для твоего роста!»). Обе версии — 1.6.14, обе от конца марта 2026, но команда пишет release-notes отдельно под каждую площадку. Для контент-планирования это означает, что **«что нового» нельзя одним постом «отзеркалить» в трёх сторах** — формулировки разные и отражают разные стороны одного релиза:

- **App Store:** «подборки индивидуально» — усиление шага 4 ([[canon/product-knowledge/gro-app-overview|адаптация]]), персонализация.
- **RuStore:** «обновлена диагностика и главная» — усиление шага 1 (диагностика) и продуктовая UI.

В сумме картина v1.6.14 богаче: релиз затронул и первый шаг (диагностика), и последний (адаптация/персонализация), плюс UI-правки. Это стоит учесть в «release post»-формате, если такой появится в контент-плане.

## Permissions и compliance

RuStore показывает единственное разрешение: **Местоположение**. Google Play в блоке «Безопасность данных» декларирует заметно больше (идентификаторы устройства + личная информация + фото + видео). Причина — разные таксономии раскрытия: RuStore показывает только явные Android-permissions, Google Play декларирует серверный сбор. Противоречия нет, фиксируется как audit на случай вопросов приватности.

## Что НЕ выносить в контент

- **«ООО ГРО» как «настоящий publisher GRO»** — корпоративное юрлицо, а не бренд. Все упоминания «кто стоит за GRO» идут через [[canon/product-knowledge/gro-team|команду founders]], а не через ООО/LLC.
- **Точное число установок** — его нет даже в HTML-данных RuStore (только bucket «до 1 тыс»), выдумывать нельзя.
- **«Рейтинг в RuStore»** — его нет (0,0 «Нет оценок»). Не цитировать как «рейтинг в магазинах».
- **Email `legal@gro.pro`** — это legal-контакт, а не публичный контакт поддержки продукта. Для пользователей использовать контакты с [[sources/2026-04-10-groapp-landing|лендинга]].
- **Сравнение «49,1 МБ в RuStore vs 77,6 МБ в App Store»** как marketing-claim («GRO в RuStore компактнее») — это артефакт формата дистрибутива, а не реальное сравнение.

## Связанные страницы

- [[canon/product-knowledge/gro-app-store-listing]] — iOS-дистрибуция (категория Бизнес, publisher Romsfort East)
- [[canon/product-knowledge/gro-google-play-listing]] — Google Play-дистрибуция (категория LIFESTYLE, publisher Romsfort East)
- [[canon/product-knowledge/gro-app-overview]] — механика продукта, треки, дуальный framing
- [[canon/product-knowledge/gro-pricing]] — цена (RuStore не раскрывает IAP, поэтому не сдвигает канон)
- [[canon/product-knowledge/gro-team]] — реальная команда и publisher-структуры
- [[canon/positioning/gro-value-proposition]] — позиционирование, подтверждённое RuStore как устойчивое store-канон
- [[sources/2026-04-10-gro-rustore-listing]] — source-страница этого листинга
- [[sources/2026-04-10-gro-appstore-listing]] — iOS-источник
- [[sources/2026-04-10-gro-googleplay-listing]] — Google Play-источник

## Backlinks

_15 pages link to this one._

- [[canon/marketing-frameworks/tabunov-landing-anatomy]]
- [[canon/product-knowledge/gro-app-overview]]
- [[canon/product-knowledge/gro-app-store-listing]]
- [[canon/product-knowledge/gro-google-play-listing]]
- [[canon/product-knowledge/gro-pricing]]
- [[canon/product-knowledge/gro-team]]
- [[canon/product-knowledge/gro-web-app]]
- [[evolving-strict/market-data/app-store-slop-2026]]
- [[evolving-strict/market-data/ru-beauty-health-ecommerce-q1-2026]]
- [[evolving-strict/product-metrics/gro-store-installs]]
- [[evolving-strict/product-metrics/gro-store-ratings]]
- [[index]]
- [[overview]]
- [[sources/2026-04-10-gro-lk-auth]]
- [[sources/2026-04-10-gro-rustore-listing]]
