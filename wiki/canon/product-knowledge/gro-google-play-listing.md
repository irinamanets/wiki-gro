---
id: mkt:canon/product-knowledge/gro-google-play-listing
title: GRO — листинг в Google Play (Android, RU)
type: page
subtype: asset
layer: canon
theme: product-knowledge
tags: [product, google-play, android, distribution, pricing]
confidence: high
stale: false
created: 2026-04-10
updated: 2026-04-10
sources: [sources/2026-04-10-gro-googleplay-listing.md, sources/2026-04-10-gro-rustore-listing.md]
namespace: mkt
---

# GRO — листинг в Google Play (Android, RU)

Каноническая справка о том, как GRO выглядит в Google Play Store (RU storefront) на 2026-04-10. Это вторая из трёх ingested точек дистрибуции продукта после [[canon/product-knowledge/gro-app-store-listing|App Store iOS]] и параллельно с [[canon/product-knowledge/gro-rustore-listing|RuStore]]; страница по веб-кабинету появится после соответствующего ingest-а.

Задача страницы — быть reference-точкой для контент-команды: какая сейчас версия в Android-сборке, какой минимум Android, в какой категории GRO числится в Google Play, сколько там установок, и как Android-листинг отличается от iOS.

## Техническая конфигурация

- **Package ID:** `pro.gro` — единый bundle/package ID со всеми другими платформами (App Store и [[canon/product-knowledge/gro-rustore-listing|RuStore]] используют тот же идентификатор, подтверждено прямым ingest-ом всех трёх сторов).
- **Текущая версия:** **1.6.14** `[conf:high, src:2026-04-10]`. **Идентично iOS-сборке** — значит, релиз v1.6.14 был кроссплатформенным (iOS обновился 31 марта 2026, Android — 30 марта).
- **Последнее обновление:** **30 марта 2026** `[conf:high, src:2026-04-10]`.
- **Минимальный Android:** **7.0 (Nougat)** `[conf:high, src:2026-04-10]` — покрывает ~99% активных устройств в РФ, в креативах можно не оговаривать требования к телефону.
- **Категория в Google Play:** **«Стиль жизни» (LIFESTYLE)** `[conf:high, src:2026-04-10]`. **Google Play — единственный из трёх сторов, где GRO в lifestyle-вертикали**: в App Store и в [[canon/product-knowledge/gro-rustore-listing|RuStore]] продукт в business-вертикали («Бизнес» и «Бизнес-сервисы» соответственно). То есть 2:1 в пользу business, и Google Play — исключение. Осознанный это выбор команды или инерция — открытый вопрос к продукт-команде.
- **Возрастной рейтинг (IARC):** **3+** `[conf:high, src:2026-04-10]`. Несопоставимо напрямую с iOS-овскими «16+» или RuStore-овским «0+» — разные рейтинговые системы, все три валидны.

## Провайдер и юрлицо

- **Developer name (видимый на карточке):** Romsfort East.
- **Developer legal (из блока «О разработчике»):** `ROMSFORT EAST ADVISORY MANAGEMENT CONSULTANCIES L.L.C`, Дубай, ОАЭ. Это то же самое юрлицо-publisher, что и в App Store (см. [[canon/product-knowledge/gro-app-store-listing]]), — публикация из Дубая через нерезидентную структуру. **В [[canon/product-knowledge/gro-rustore-listing|RuStore]] publisher другой** — там напрямую указано российское ООО ГРО, потому что VK-стор требует российское юрлицо. То есть команда держит две параллельные корпоративные ветки: Romsfort East (Dubai) под Apple/Google и ООО ГРО под RuStore. В контенте ни то, ни другое не упоминать, см. [[canon/product-knowledge/gro-team|команда GRO]] для настоящей команды продукта.
- **Developer website (в JSON-LD и карточке):** `https://groapp.ru/`.
- **Email поддержки в карточке Google Play:** **`legal@gro.pro`** — тот же email подтверждён в [[canon/product-knowledge/gro-rustore-listing|RuStore]], не встречается на [[sources/2026-04-10-groapp-landing|лендинге]] и в [[canon/product-knowledge/gro-app-store-listing|App Store]]. После ingest-а RuStore уверенность выше: `gro.pro` — **устойчивый legal/support-домен**, используемый стабильно в обоих Android-сторах. Домен `gro.pro` отдельный от `groapp.ru`, по префиксу `legal@` — для юридической переписки. Где ещё используется — всё ещё открытый вопрос (mail-сервера, subdomain веб-кабинета).

## Установки и социальное доказательство

Числа (публичный bucket, internal точное значение) живут в дрейфующих метрик-страницах:
- Установки — [[evolving-strict/product-metrics/gro-store-installs]]
- Рейтинги — [[evolving-strict/product-metrics/gro-store-ratings]]

На момент последнего ingest-а Google Play показывал минимальный bucket «100+», скрывал рейтинг из-за малой базы, ноль видимых отзывов на странице. iOS-отзывы (см. [[evolving/customer-feedback/gro-app-store-reviews]]) **нельзя** напрямую пересаживать в Google Play (против правил обоих сторов), но можно переиспользовать как текст на лендинге и в постах.

**Вывод для distribution-стратегии** (устойчивый, не дрейфует с цифрами): Android-канал GRO практически не задействован. У команды пока нет никакого социального доказательства внутри самого стора. Это **огромный gap** для Android-ориентированного performance-маркетинга: любой CPA-креатив, ведущий в Google Play, приземляется на листинг без user proof. До накопления хотя бы 50+ оценок:

- **Не запускать масштабные CPA-кампании** под Android, пока листинг пустой.
- Приоритет — собрать первые 20–50 оценок любым органическим путём (попросить ранних пользователей, in-app review prompt после значимых action-событий).

## Позиционирование в листинге

Google Play-описание **дословно совпадает** с App Store-описанием: ровно та же новая рамка — «GRO — помощник в принятии решений и личном росте», с тем же anti-positioning «это не курсы и не советы» и теми же блоками «Кому подойдёт», «Как это работает», «Что ты получаешь».

**Ключевое наблюдение: новая рамка «помощник в принятии решений» — это каноническая подача GRO в обоих магазинах.** Это не App-Store-специфичное упражнение, а устойчивый сдвиг позиционирования относительно лендинга `groapp.ru`, где всё ещё живёт старая рамка «твой личный тренажёр роста». См. [[canon/positioning/gro-value-proposition]] и Contradictions-блок в [[canon/product-knowledge/gro-app-overview]].

## Треки (предметные области)

Явно перечислены шесть тем в разделе «Как это работает»:

- карьера
- деньги
- коммуникации
- мышление
- фокус
- продуктивность

Этот набор **идентичен App Store** и **отличается от лендинга** (продажи, маркетинг, коммуникации, цели, мышление, мотивация). Пересечение — только **коммуникации** и **мышление**. Разнобой треков, таким образом, устойчивый (store-канон vs landing-канон), а не случайная iOS-особенность. См. `## Contradictions` в [[canon/product-knowledge/gro-app-overview]].

## In-app purchases

Google Play не раскрывает разбивку IAP по конкретным SKU, как это делает App Store, — но показывает агрегированный **диапазон цен**:

| Показатель | Значение | Source |
|---|---|---|
| IAP-диапазон | От 2 490,00 ₽ до 2 990,00 ₽ за товар | `[conf:high, src:2026-04-10]` |
| Установка | Бесплатно | `[conf:high, src:2026-04-10]` |

Нижняя граница диапазона (**2 490 ₽** `[conf:high, src:2026-04-10]`) — это месячная подписка, уже подтверждённая в App Store. Верхняя граница (**2 990 ₽** `[conf:high, src:2026-04-10]`) — это SKU **«100% Энергии»**, тоже знакомый из App Store. Google Play таким образом даёт **кросс-платформенное подтверждение обоих ценовых SKU**. Детальный комментарий и правила цитирования — в [[canon/product-knowledge/gro-pricing]].

## JSON-LD ghost: старая рамка в SEO-разметке

Неочевидный, но операционно важный нюанс. В `schema.org/SoftwareApplication`-разметке Google Play страницы поле `description` равно:

> GRO — твой личный тренажёр роста в бизнесе

Это **старый tagline с лендинга**, не обновлённый при смене продуктовой рамки. В видимом UI-описании на этой же странице уже используется новая рамка («помощник в принятии решений»), а в schema.org — старая. Следствия:

- **SEO-риск.** В поисковой выдаче Google и в rich snippets Google берёт описание из schema.org, поэтому пользователь, который ищет GRO через Google, увидит старую рамку «тренажёр роста в бизнесе». Это надо проверить руками в поисковой выдаче.
- **Техдолг Play Console.** Скорее всего, это «short description» в Play Console, которое команда не обновила при смене «full description». Чинится одним изменением в Play Console.

В контент-стратегии об этом помнить при планировании SEO и PR: пока старый short description не заменён, весь inbound-поиск через Google Play видит GRO сквозь старую рамку.

## Что НЕ выносить в контент

- **Точное число установок 448** — только internal, Google Play сам показывает «100+». Цитирование 448 = утечка.
- **Адрес Romsfort East в Дубае и email `hello@romsfort.com`** — это служебная legal-информация, не бренд. Любые упоминания «кто стоит за GRO» → [[canon/product-knowledge/gro-team]].
- **`legal@gro.pro`** — не публиковать как публичный контакт поддержки продукта, это legal-контакт. Для пользовательской поддержки использовать страницы из [[sources/2026-04-10-groapp-landing|лендинга]].
- **Рейтинг Android** — его нет, **не выдумывать**. Если нужен «рейтинг GRO в магазинах» в контенте — использовать только iOS (4,0 при 11 оценках, с оговоркой про размер выборки) из [[canon/product-knowledge/gro-app-store-listing]].

## Связанные страницы

- [[canon/product-knowledge/gro-app-store-listing]] — iOS-дистрибуция, параллельная эта Android-странице
- [[canon/product-knowledge/gro-rustore-listing]] — параллельный Android-листинг RuStore (тот же продукт, но publisher — ООО ГРО)
- [[canon/product-knowledge/gro-app-overview]] — механика продукта, 4 шага, треки (с Contradictions про разнобой)
- [[canon/product-knowledge/gro-pricing]] — сводка цены, с кросс-платформенным подтверждением IAP
- [[canon/product-knowledge/gro-team]] — реальная команда GRO (не Romsfort East)
- [[canon/positioning/gro-value-proposition]] — позиционирование продукта
- [[sources/2026-04-10-gro-googleplay-listing]] — source-страница этого листинга
- [[sources/2026-04-10-gro-appstore-listing]] — iOS-источник, с которым сопоставляем

## Backlinks

_17 pages link to this one._

- [[canon/marketing-frameworks/tabunov-landing-anatomy]]
- [[canon/product-knowledge/gro-app-overview]]
- [[canon/product-knowledge/gro-app-store-listing]]
- [[canon/product-knowledge/gro-pricing]]
- [[canon/product-knowledge/gro-rustore-listing]]
- [[canon/product-knowledge/gro-team]]
- [[canon/product-knowledge/gro-web-app]]
- [[evolving-strict/market-data/app-store-slop-2026]]
- [[evolving-strict/market-data/ru-beauty-health-ecommerce-q1-2026]]
- [[evolving-strict/product-metrics/gro-store-installs]]
- [[evolving-strict/product-metrics/gro-store-ratings]]
- [[evolving/industry-trends/agentic-commerce-stripe-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-04-10-gro-googleplay-listing]]
- [[sources/2026-04-10-gro-lk-auth]]
- [[sources/2026-04-10-gro-rustore-listing]]
