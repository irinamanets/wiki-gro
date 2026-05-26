---
id: mkt:evolving-strict/market-data/ru-business-closures-vat-margin-squeeze-2025-2026
title: "Закрытия бизнеса РФ 2025–2026 + НДС/ставка vs низкомаржинальные модели (по Батыреву)"
type: page
subtype: metric
layer: evolving-strict
theme: market-data
tags: [market-data, ru-smb, business-closures, vat, margin, consumer-demand, batyrev]
confidence: low
stale: false
created: 2026-05-25
updated: 2026-05-25
sources: [sources/2026-05-25-yt-batyrev-uncertainty-leadership-team.md]
namespace: mkt
---

# Закрытия бизнеса РФ 2025–2026 + сдавливание маржи НДС/ставкой

Качественно-количественный срез давления на RU SMB по пересказу Максима Батырева в выпуске Серебряного Дождя ([[sources/2026-05-25-yt-batyrev-uncertainty-leadership-team]]). **Все числа self-reported спикером** («насколько я слышал статистику»), первоисточники не названы → `confidence: low`, для питча/презентации верифицировать на ФНС/Росстат/ЕГРЮЛ.

## Динамика регистраций

- РФ 2025: **закрылось ~400 тыс. компаний, открылось ~100 тыс.** `[conf:low, src:2026-05-25]` — по словам спикера, **впервые** закрытий кратно больше открытий.
- Прогноз спикера на 2026: **открытий будет ещё меньше, закрытий — больше** `[conf:low, src:2026-05-25]`.

## Механика сдавливания маржи (НДС + ключевая ставка)

Иллюстративный кейс из выпуска — аптека «с первого этажа»:

- Выручка: **>20 млн ₽** `[conf:low, src:2026-05-25]`
- Маржа: **~3%** → ~**5–4 млн ₽** прибыли `[conf:low, src:2026-05-25]`
- Повышение **НДС** «убьёт» бизнес, который раньше «мог на упрощёнке» `[conf:low, src:2026-05-25]`

Системный тезис спикера: во многих отраслях **рентабельность ниже ключевой ставки** `[conf:low, src:2026-05-25]` → модель не выживает даже при повышении цен, потому что добавляется **падение потребительского спроса** (люди «зажимают деньги», считают каждые 500 ₽).

## Сдвиг потребительских моделей (qualitative)

- Покупатели переходят от импульсивного «накидал в корзину» к расчётливому «дешевле на 500 ₽ — потому что разумно» `[conf:low, src:2026-05-25]`.
- Спикер трактует это как **«очищение» от старых потребительских моделей** — нормализация бережливости.

## Триангуляция с верифицированными датасетами

Эти self-reported числа **директионально согласуются** с уже зафиксированными в вики метриками (которые имеют более высокую confidence):

- [[evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026]] — независимый сигнал сдавливания маржи на маркетплейсах
- [[evolving-strict/market-data/ru-business-q1-2026-survey]] — опросные данные по ухудшению условий SMB Q1 2026
- [[evolving-strict/market-data/ru-macro-snapshot-may-2026]] — макро-фон (дефляция, PMI Services 49,7 — стагнация в услугах)
- [[evolving-strict/market-data/ru-entrepreneurship-as-norm-minec-sber-2026]] — counter-сигнал (вовлечённость в предпринимательство растёт) → закрытия идут на фоне притока новичков

## Применимость для GRO-аудитории

Контекст-якорь для контента под Сегмент 2 ([[canon/target-audience/ru-smb-founder-owner-seller]]): острая cash-pressure повышает готовность пробовать инструменты продуктивности/эффективности. Концептуальная пара — [[canon/marketing-frameworks/crisis-as-self-test-batyrev]] (кризис как тест) и [[canon/marketing-frameworks/batyrev-uncertainty-era-management]] (реакция > проактивность).

**Content-caveat:** числа использовать только с пометкой «по словам Батырева / self-reported», не как факт; для серьёзных материалов брать верифицированные датасеты выше.

## Связанные страницы

- [[evolving-strict/market-data/ru-marketplace-margin-collapse-may-2026]]
- [[evolving-strict/market-data/ru-business-q1-2026-survey]]
- [[evolving-strict/market-data/ru-macro-snapshot-may-2026]]
- [[canon/marketing-frameworks/crisis-as-self-test-batyrev]]
- [[canon/target-audience/ru-smb-founder-owner-seller]]
- [[sources/2026-05-25-yt-batyrev-uncertainty-leadership-team]]
