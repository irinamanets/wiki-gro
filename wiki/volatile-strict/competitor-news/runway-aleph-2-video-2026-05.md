---
id: mkt:volatile-strict/competitor-news/runway-aleph-2-video-2026-05
title: "Runway Aleph 2.0 — frame-to-video edit, релиз через 2 дня после Gemini Omni"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [runway, aleph-2, video-generation, ai-video-editing, frame-edit-propagation, frontier-video]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26  # +2-nd attest @cgevent (15731, 15735): 1080p / до 30 сек, доступ с подписки Standard, промокод RUNWAY50 (Pro 50% off). Тест Цыпцына — переодевание ниндзя в розовый из погони (Seedance), 'выглядит как ответ редактирующим возможностям Gemini Omni'. Multishot работает, replace объекта с физикой/освещением, бэкграунд нетронут.
sources: [sources/2026-05-26-tg-neuraldvig-may-19-22-2026.md, sources/2026-05-26-tg-cgevent-may19-25-2026.md]
namespace: mkt
---

# Runway Aleph 2.0 — frame-to-video edit, релиз через 2 дня после Gemini Omni

**Дата события:** 2026-05-22 (релиз ретранслирован [[sources/2026-05-26-tg-neuraldvig-may-19-22-2026|@neuraldvig пост 10774]]). `[conf:high, src:2026-05-22]`

## Что вышло

Runway дропнули **Aleph 2.0** — новую модель видеогенерации/редактирования с **frame-edit propagation** механикой. `[conf:high, src:2026-05-22]`

| Параметр | Значение | Source |
|---|---|---|
| Компания | Runway ML | `[conf:high, src:2026-05-22]` |
| Модель | Aleph 2.0 | `[conf:high, src:2026-05-22]` |
| Mechanic | Достаточно поменять **всего один кадр** из видео → Aleph переносит изменения **на весь ролик** | `[conf:high, src:2026-05-22]` |
| Релиз-окно | Через **2 дня после Gemini Omni** (20 мая) | `[conf:high, src:2026-05-22]` |
| Доступ | [app.runwayml.com](https://app.runwayml.com/home) | `[conf:high, src:2026-05-22]` |

## Что это значит

### 1. Frame-edit propagation — новая UX-парадигма для video AI

До Aleph 2.0 video editing в AI был либо:
- **Promt-based** (Veo, Seedance, Sora) — описываешь сценарий → получаешь ролик
- **Mask-based** (Runway 1.x, Synthesia) — выделяешь зону → меняешь в ней

**Frame-edit propagation** — **новая парадигма**: меняешь один кадр (в любом редакторе, как картинку), Aleph переносит изменение через весь ролик с temporal consistency. Это:
- Снимает **artistic ambiguity** (промт никогда не передаёт точное намерение)
- Использует **standard image-editing UX** (привычный для пользователя Photoshop)
- Сохраняет **direct control** в руках пользователя

### 2. Контр-удар Gemini Omni через 2 дня

[[volatile-strict/competitor-news/google-gemini-omni-video-2026-05|Gemini Omni]] на Google I/O 2026-05-20 показал multimodal-layering ('поменяй скульптуру на мыльные пузыри', 'когда рука касается зеркала — оно плывёт'). Runway ответил через 2 дня **с другим подходом** — frame-edit propagation. Это **разделение рынка video AI** на:
- **Promt-natural-language editing** (Gemini Omni) — описываешь словами
- **Frame-direct editing** (Runway Aleph 2.0) — меняешь картинку

Конкуренция на разных UX-углах, не на одних benchmark'ах. См. также [[evolving/content-trends/ai-video-tools-stack-2026|AI-video-tools stack]] — Runway по-прежнему держит позицию в категории, но **переопределяет UX** через Aleph 2.0.

### 3. «Убили Gemini Omni через 2 дня» — narrative-hook

Сама формулировка @neuraldvig — *«Gemini Omni убили через 2 дня после релиза — Runway дропнули новую модель»* — это **рыночный нарратив**, который запускает media-цикл. Через 1-2 недели жди статей с заголовком «Runway переиграл Google на собственном I/O». Это **сильное PR-окно** для Runway.

## Почему это важно для GRO

1. **AI-video-tools landscape переопределён** — нужно обновлять [[evolving/content-trends/ai-video-tools-stack-2026|AI-video-tools stack]] страницу: Aleph 2.0 заходит как **новая категория** «frame-edit propagation», не как ещё одна prompt-to-video модель.

2. **Контент-hook для сегмента 1 ЦА** (карьеристы): *«Что Runway Aleph 2.0 значит для маркетологов и видеомейкеров — 5 минут на разбор»* — quick-take формат, который любит этот сегмент.

3. **Параллель для контента «AI-инструменты двигаются разными UX»** — Runway vs Gemini = два разных подхода к одной задаче. Reusable рамка для contentplan'а: *«Vibe-coding vs frame-direct vs prompt-based: куда движется AI-tooling в 2026»* — широкий охватный пост для блога GRO.

## Capability-уточнения от @cgevent (2-nd attest, 15731+15735)

[[sources/2026-05-26-tg-cgevent-may19-25-2026|Дамп @cgevent 19-25 мая]] добавляет конкретные параметры по Aleph 2:

| Параметр | Значение | Source |
|---|---|---|
| Разрешение | **1080p** | `[conf:high, src:2026-05-22]` |
| Длина | **до 30 сек** | `[conf:high, src:2026-05-22]` |
| Доступ | подписка от **Standard** (без уточнения версии) | `[conf:high, src:2026-05-22]` |
| Промокод | `RUNWAY50` (50% off на Pro) | `[conf:high, src:2026-05-22]` |
| Multishot | работает в сценах из **Seedance 2** | `[conf:high, src:2026-05-22]` |
| Стиль | смена стиля всему кадру | `[conf:high, src:2026-05-22]` |
| Точечный edit | замена объектов (куртка, лампа) с **учётом физики и освещения**, бэкграунд **нетронут** | `[conf:high, src:2026-05-22]` |
| Workspace | [Studio](https://app.runwayml.com/video-tools/teams/guest/ai-tools/generate?mode=edit) с превью, текстовыми правками, реф-картинками | `[conf:high, src:2026-05-22]` |

### Тест Цыпцына

Исходник — погоня в стиле ниндзя, сделанная в Seedance. Инструкция Aleph 2: **«переодеть всех ниндзя в розовый»** `[conf:medium, src:2026-05-22]`. Результат — все ниндзя переоделись (и водитель попал под раздачу). **Вердикт Цыпцына: «Выглядит как ответ редактирующим возможностям Gemini Omni»** — то есть Aleph 2 позиционируется как прямой конкурент Omni Editing, не как замена Veo/Sora генерации.

## Connections

- [[evolving/content-trends/ai-video-tools-stack-2026]] — AI-video-tools stack (нужен update — 30 сек / 1080p / frame-edit propagation)
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] — параллельный Gemini Omni релиз
- [[volatile-strict/competitor-news/capcut-gemini-partnership-2026-05]] — параллельный partnership Google + CapCut той же недели
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — макро-гонка AI-релизов
- [[evolving/industry-trends/hollywood-ai-institutional-shift-2026]] — институциональная legitimacy AI-кино
- [[evolving/industry-trends/india-ai-film-lab-2026]] — India regulatory arbitrage в кино
- [[sources/2026-05-26-tg-neuraldvig-may-19-22-2026]] — первоисточник
- [[sources/2026-05-26-tg-cgevent-may19-25-2026]] — 2-nd attest источник
