---
id: mkt:volatile-strict/competitor-news/tencent-hunyuan-translation-on-device-2026-05
title: "Tencent Hunyuan Hy-MT1.5-1.8B (AngelSlim): on-device переводчик 33 языков, 440 МБ (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [tencent, ai, hunyuan, angelslim, on-device, edge-ai, translation, open-source, china, 2026]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-bezsmuzi-may-8-11-2026.md]
namespace: mkt
---

# Tencent Hunyuan Hy-MT1.5-1.8B (AngelSlim) — on-device переводчик мая 2026

Open-source выпуск Tencent в мае 2026: **Hy-MT1.5-1.8B-1.25bit** — компактный переводчик на базе тулкита квантизации AngelSlim. Зафиксировано через [[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026|пост 15961 Максима Кульгина]] от 2026-05-09 с прямой ссылкой на HuggingFace.

`confidence: medium` — официальный HuggingFace-репозиторий ([huggingface.co/AngelSlim/Hy-MT1.5-1.8B-1.25bit](https://huggingface.co/AngelSlim/Hy-MT1.5-1.8B-1.25bit)) — проверяемый первичный артефакт. Заявления о точности vs Google Translate — vendor-claim, не независимый бенчмарк.

## Что выпущено

| Параметр | Значение | Source |
|---|---|---|
| Параметров модели | **1,8B** (квантизованы до 1,25 бит/параметр) | `[conf:medium, src:2026-05-09]` |
| Размер на диске | **440 МБ** | `[conf:medium, src:2026-05-09]` |
| Языков | **33**, включая ru/en | `[conf:medium, src:2026-05-09]` |
| Inference target | Локально на смартфоне (Android: APK в один клик) | `[conf:medium, src:2026-05-09]` |
| Зависимость от интернета | **Нет** (full on-device) | `[conf:medium, src:2026-05-09]` |
| Vendor claim про точность | Превосходит Google Translate (по словам Tencent) | `[conf:low, src:2026-05-09]` |
| License | Open-source через HuggingFace | `[conf:medium, src:2026-05-09]` |

## Что нового технически

**1,25-бит квантизация** через AngelSlim — это **экстремальное сжатие** (стандарт 4–8 бит). Это позволяет 1,8B-параметрическую модель упаковать в 440 МБ при сохранении (по vendor-claim) качества near-FP16. Если результаты подтвердятся независимыми бенчмарками — это становится **референсной точкой** для edge-AI инференса.

## Маркетинговое значение

### 1. Структурный ответ Китая на cloud-AI монополию OpenAI/Anthropic

Tencent (наряду с DeepSeek, ByteDance, Alibaba) формирует **локально-исполнимую edge-AI ветку** в открытом доступе. Это не первый такой релиз — но самый показательный по соотношению **функциональности/размера**:

- 33 языка (большой language-pack)
- 440 МБ (помещается в среднестатистическое мобильное приложение)
- On-device (нет зависимости от $20/mo подписки на cloud-API)

Стратегический эффект: **mass-market AI без OpenAI ценника**. Пользователь в РФ (где доступ к ChatGPT/Claude ограничен) получает функциональность через локальное приложение.

### 2. Под-кейс «зачем платить $20 за подписку, если есть локально и бесплатно»

Связан с прямой ремаркой Кульгина в том же дампе (пост 15951): «программисты покупают подписки за $20 в обход блокировок Claude через биржи». Эта economy-of-circumvention для cloud-AI делает edge-AI стратегически привлекательным для **RU mass market** — нет geo-блокировок, нет necessity платить через зарубежные карты, нет VPN-overhead.

### 3. Content-content-angle для блога GRO

«Open-source перевод 33 языков в 440 МБ. Локально. Без интернета. Без OpenAI» — это hook-формула, которая работает для аудитории, чувствительной к платным AI-подпискам (часть founder/SMB ЦА GRO).

### 4. Связь с потенциальной voice-функциональностью GRO

GRO — продукт с короткой 4-шаговой механикой; голосовой/мобильный AI-инференс **on-device** — релевантный technical-вектор для пользовательского опыта в регионах с нестабильным интернетом. См. также [[volatile-strict/competitor-news/openai-realtime-audio-models-2026-05|OpenAI Realtime API]] — там cloud-маршрут, здесь — on-device альтернатива.

## Что мониторить

- **Независимые бенчмарки** Hy-MT1.5-1.8B-1.25bit vs Google Translate, DeepL, OpenAI на парах en-ru, ru-en, zh-en, zh-ru.
- **Latency / energy / battery impact** на средних Android-смартфонах — критично для mass-market adoption.
- **Производные продукты** (mobile apps, browser extensions) на базе этой модели в RU/CN рынках.
- **Tencent's next release** в той же ветке — если 1,8B → 7B с тем же 1,25-битным квантованием получится, это станет new edge-AI baseline.

## Caveat'ы

- **Vendor claim «превосходит Google Translate»** — требует независимой верификации. Tencent публиковал similar claims для предыдущих моделей с разной степенью достоверности.
- **440 МБ** — это сам файл; runtime memory может быть больше (1-2 ГБ на средних телефонах).
- **APK не из официальных сторов** (HuggingFace демка) — для massmarket-installation нужен Google Play / RuStore канал.
- **Демо-видео** прикреплено к посту 15961 (`raw/processed/video/tg_bezsmuzi_15961.mp4`), но whisper VAD показал **no speech detected** (ratio 0%) — это **silent demo**, не аудио-инструкция. [conf:low, src:2026-05-26]

## TTL

**60 дней (до 2026-07-25)** — конкретные характеристики edge-AI быстро устаревают (новые версии раз в квартал). Сохраняется до подтверждённого следующего Hunyuan-релиза или появления независимого бенчмарка.

## Связанные страницы

- [[sources/2026-05-26-tg-bezsmuzi-may-8-11-2026]] — источник-якорь
- [[volatile-strict/competitor-news/openai-realtime-audio-models-2026-05]] — cloud-альтернатива (OpenAI Realtime)
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий контекст AI-гонки
- [[evolving/industry-trends/ai-agent-economy-2026]] — связь с агент-экосистемой
- [[evolving/industry-trends/ai-agents-saas-seat-compression-2026]] — структурный сдвиг pricing
