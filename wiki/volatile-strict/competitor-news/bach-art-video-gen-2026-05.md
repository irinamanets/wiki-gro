---
id: mkt:volatile-strict/competitor-news/bach-art-video-gen-2026-05
title: "Bach.Art — новый video-gen с фокусом на консистентность персонажей (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [video-generation, ai, consistency, face-replacement, competitor]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-cgevent-may05-08-2026.md]
namespace: mkt
---

# Bach.Art — новый video-gen с фокусом на консистентность персонажей

## Что произошло

В мае 2026 запущен сервис [Bach.Art](https://www.bach.art/) — новый AI video-generator от стартапа **Video Rebirth** `[conf:medium, src:2026-05-08]`. Освещён @cgevent (пост #15644, 2026-05-08).

## Ключевые характеристики

| Параметр | Значение | Source |
|---|---|---|
| Качество | По оценке @cgevent — на уровне Kling 3, не Seedance 2.0 | `[conf:medium, src:2026-05-08]` |
| Open source | Нет, closed model | `[conf:high, src:2026-05-08]` |
| Free plan: ежедневный credit-бюджет | **60 кредитов при логине Google + 60 ежедневно** | `[conf:high, src:2026-05-08]` |
| Платный плагин | **$15 за 800 кредитов** (не сгорают в конце месяца) | `[conf:high, src:2026-05-08]` |
| Стоимость 6 сек видео 720p | **24 кредита** | `[conf:high, src:2026-05-08]` |
| Multi-Shot Montage (макс длительность) | **30 секунд** (5 клипов × 6 сек + 4 склейки в одном промпте) | `[conf:high, src:2026-05-08]` |
| Image-to-Video | Да | `[conf:high, src:2026-05-08]` |
| Reference-to-Video | Да, **до 8 картинок на входе** | `[conf:high, src:2026-05-08]` |
| Аудио / липсинк / войсовер | Да | `[conf:high, src:2026-05-08]` |
| **Face-fence (фильтр на лица актёров)** | **Похоже, отсутствует** — Tom Cruise, Brad Pitt доступны для генерации `[conf:medium, src:2026-05-08]` |

## Уникальные конкурентные преимущества

### 1. Multi-Shot Montage до 30 секунд по одному промпту

В отличие от большинства video-gen, где **6-8 секунд = один промпт**, Bach.Art позволяет **в одном промпте описать всю раскадровку**, и модель сама склеит 5 клипов с заявленным режиссёрским контролем. Это **сравнимо с Seedance `[cut]`-feature**, но в Bach.Art это позиционируется как первичный feature, а не недокументированный trick.

### 2. Self-positioning «без фильтров на лица актёров»

Прямая цитата автора @cgevent:
> *«Не Сиденс, но! У них похоже (пока) нет вообще никаких фильтров на лица актеров и селебов. Пробуем, кидаем в коменты Томов Круизов и Бредов Питаф.»*

Это **сигнал market-positioning**: Bach.Art целится в сегмент, отсечённый Seedance/Sora face-fence — **создателей parody-content, deepfake-моделирования, FuruFuru-style impersonation** (см. [[evolving/content-trends/ai-impersonation-into-classic-scenes-2026]]). Это **этически контroversial positioning**, но **функционально дифференцирующий**.

### 3. Reference-to-Video с 8 картинками

Большинство видео-генов принимают 1-2 reference image. **8 reference** — позволяет давать модели **много discrete cues**: лицо + стиль освещения + локация + одежда + props + позиция + emotion + камера-угол. Сравнимо с **@-системой Seedance 2.0** (12 файлов) — Bach.Art в этом аспекте конкурирует на тот же ценовой ярус.

## Где встаёт в существующий tools stack

См. [[evolving/content-trends/ai-video-tools-stack-2026]] — Bach.Art добавляется как **новая модель**:

| Параметр | Bach.Art (май 2026) |
|---|---|
| Стоимость | $15 / 800 кр = $0.019 / кр; одно видео 6 сек 720p = 24 кр = **$0.45 / видео** или **~$0.075 / сек** |
| Скорость | Не указано, **позиция в Kling 3 диапазоне** |
| Face consistency | **Декларируется как ключевая фича** |
| Key feature | **Multi-Shot Montage 30 сек по одному промпту**, отсутствие face-fence |
| Целевой use-case | Parody content, character-driven длинные сцены без сшивания, образ знаменитости |

**Сравнение с конкурентами:**
- Seedance 2.0 ($0.03/сек) — дешевле, но 30 мин генерации и жёсткая цензура
- Runway Gen-4.5 (9× Seedance) — кинематографический язык, но дрифт >5 сек
- Kling 3.0 — лучшая face consistency, но без Multi-Shot и face-fence работает
- **Bach.Art** — **аналог Kling 3.0 по консистентности + без face-fence**

## Бизнес-модель и риски

### Бизнес-модель

- **Free-trial sustainable** — 60 кредитов/день = 2.5 видео 6 сек/день бесплатно = низкий churn рисков
- **Платная конверсия легко** — $15 / 800 кредитов = ~33 видео = пользователь, который любит сервис, заплатит $15-30/мес
- **Кредиты не сгорают** — снижение friction для импульсивной оплаты

### Регуляторные риски

- **Без face-fence** — это **прямой регуляторный риск** в EU/UK по AI Act, в США по NO FAKES Act / state-level deepfake laws
- **Tom Cruise / Brad Pitt** генерация без consent — это **likely violation US right of publicity**
- **Сервис, вероятно, будет вынужден ввести фильтры в течение 2026 года** — раннее адопшн окно для creator'ов составит максимум 6-12 месяцев

### Маркетинговый риск для GRO (не использовать как пример)

Bach.Art **не подходит как content-anchor для GRO** в текущем виде — face-fence-bypass позиционирование привязано к ethically-controversial use cases. **Только как «ещё один competitor в landscape»** упоминать, не как **proof-point** или recommendation.

## Применимость для GRO-контента

### Если делать content по теме «AI video tools 2026»

Bach.Art можно **упомянуть как пример «специализированной модели для character-consistency»**, но **сразу указать caveat про face-fence** — это **не для коммерческих use cases с подменой лица знаменитости**.

### Если делать content по теме «consistency in AI generation»

Bach.Art — **анчер для тезиса**, что **face consistency** стала отдельным product category. До 2026 это была feature; теперь — основа позиционирования отдельных competitor'ов.

## Anti-patterns

- **Не использовать Bach.Art в production GRO-контенте до января 2027** — регуляторный landscape слишком меняется
- **Не цитировать «без фильтров на лица актёров» как преимущество** — это **этически proxy для compliance-нарушения**
- **Не сравнивать с GRO по analogy** — Bach.Art это video-tool; ложная аналогия

## Связь с другими страницами

- [[evolving/content-trends/ai-video-tools-stack-2026]] — добавляется как новая модель
- [[evolving/content-trends/ai-impersonation-into-classic-scenes-2026]] — Bach.Art встаёт в этот тренд
- [[evolving/industry-trends/india-ai-film-lab-2026]] — параллельный нарратив «отсутствие regulations как фича»
- [[volatile-strict/competitor-news/elevenmusic-platform-launch-2026-05]] — аналогичный новый player в audio-domain
- [[sources/2026-05-14-tg-cgevent-may05-08-2026]] — первоисточник
