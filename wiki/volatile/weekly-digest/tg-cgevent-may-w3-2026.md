---
id: mkt:volatile/weekly-digest/tg-cgevent-may-w3-2026
title: "Дайджест @cgevent — 8–19 мая 2026 (Tier A/B/C)"
type: page
subtype: notes
layer: volatile
theme: weekly-digest
tags: [content, telegram, ai, cg, video-generation, voice-ai, agentic, digest]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-cgevent-may08-19-2026.md]
namespace: mkt
---

# Дайджест @cgevent — 8–19 мая 2026

Конденсированная карта для быстрого скана content-team. Полная карта релевантности и фактологии — в [[sources/2026-05-19-tg-cgevent-may08-19-2026]]. Предыдущий дайджест канала — [[volatile/weekly-digest/tg-cgevent-may-w2-2026]] (5–8 мая).

## Tier A — главные индустриальные события

### A.1. Higgsfield Super Computer — агент «сделай всё» + первый разоблачающий тест

Higgsfield надстроил над своим мета-интерфейсом **агент**, который сам выбирает модели, анализирует автора и его соцсети, имеет коннекты (Notion/Gmail/Drive/Figma/Slack), работает в телеге. Под капотом Claude Opus 4.7. **Первый тест Киселёва провалился:** упала песочница TTS, не подгрузился ffmpeg, новое правило «подтвердить авторство» заблокировало 3 ролика (агент не может подтвердить своё авторство), >1500 кредитов в трубу. Вердикт «продукт сырой, игрушка для богатых». → [[volatile-strict/competitor-news/higgsfield-super-computer-agent-2026-05]], апдейт [[evolving/industry-trends/software-moat-erosion-2026]].

### A.2. Thinking Machines (Мира Мурати) Interaction Models

Реалтайм-голос/мультимодальность микрокусочками 200 мс, аудио+видео+текст параллельно, асинхронное мышление. Умеет перебивать, говорить одновременно (синхроперевод), реагировать на визуальные триггеры. 276B MoE / 12B активных, FD-bench v1.5 77.8 vs 46–54 у конкурентов. Research preview закрытый. → [[volatile-strict/competitor-news/thinking-machines-interaction-model-2026-05]], апдейт [[evolving/industry-trends/ai-corporate-race-mar-may-2026]].

### A.3. Волна новых image/video/world-моделей

- **HiDream-O1 (8B)** — оказался «загадочным Peanut» с арены (vivago.ai): pixel-space, no VAE, рассуждающий prompt-агент. Дистиллят пока мылит.
- **Krea K-2** — раскатили всем + безлимит без кредитов на неделю. Художественные стили, тег жанра первым словом промпта.
- **AsymFLUX.2 Klein** — pixel-space, +40% скорости.
- **Starchild-1 (Odyssey)** — multimodal world model реалтайм 20FPS, управление голосом.
- **HY-World-2.0 / Pixal3D (Tencent)** — опенсорс генератор миров + 3D-генератор на Trellis.2.
- → апдейт [[evolving/content-trends/ai-video-tools-stack-2026]].

## Tier B — значимые тренды

### B.1. «Нейропрожарка» — 7 разборов за неделю, вошла коммерческая реклама

Семь breakdown-ов. Главный сдвиг: **KGM Torres** — первый **коммерческий рекламный ролик по реальному брифу** (ИИ-студия Ноль, 24 часа, статуэтка, 15–20 тыс ₽, ~16 ч). Также ТВ-ролик «неидеальная жизнь» (Щи Продакшен, 1 мес) с осознанной де-идеализацией ИИ-картинки через выкуп прав на лица реальных актёров. → апдейт [[evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format]].

### B.2. Claude Design — кейс игрового UI-прототипа

@VAI_ART: GPT Image 2 (генерация UI) → Claude Design (скриншот → кликабельный HTML-прототип игрового интерфейса) за пару итераций. «Средний интерфейс раньше — месяц, теперь сильно короче». → апдейт [[evolving/competitor-positioning/claude-design-2026]].

### B.3. Gemini Omni — cgevent-аттестация

Подтверждение утечки: omni-модель Google, видео + улучшенный звук, >12M контекст, может заменить Veo 3.1. В математике/тексте «явно получше» Seedance. Сильно цензурирована. → апдейт [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]].

## Tier C — операционные сигналы

### C.1. RU enterprise-AI (industrial)

- **Норникель × ИОНХ РАН** — генеративный дизайн неорганических материалов (4-этапный конвейер до роботизированного синтеза, горизонт 2 года).
- **Норникель AI-архитектор** — генеративная система проектирования заводов: сроки документации −вдвое, эффект 10 млрд ₽/год.
- **Т-Банк Nulla** — ИИ-агенты для пентеста: 45 мин вместо 2–3 дней, потестили на 1300 сервисах.

### C.2. Video2Video / нейрорендер

Замена персонажа в Seedance мультиреференсом (`change the girl in the video to the man in the image`). Тезис: для каждой страны/стриминга можно подменять персонажей.

### C.3. Viggle P.I.N.O.C / LTX Director

Viggle pivot в нейромокап (видео → fbx/glb-скелет, бесплатно). LTX Director — All-in-One Timeline Editor в ComfyUI («никаких агентов и токенов» — контр-тренд к Higgsfield Super Computer).

### C.4. Audit-only (зафиксировано, в слои не ушло)

Cloudflare ирония найма 1111 / увольнения 1100 (15649); Anthropic NLA interpretability (15658); Unitree 4-метровый мех $650K (15663); Emergence World agent-симуляция «Дом-2 для ИИ» (15686); ChatGPT personal-finance US/Pro (15687); Monet social-experiment про предвзятость к «нейромазне» (15675).

## Применимость для контент-команды GRO

### Готовые hook'и
1. **«Агент сделает всё ≠ сделает хорошо»** (Super Computer тест) — anti-hype, подтверждает «система важнее инструмента».
2. **«Голос вышел на проактивный уровень»** (Interaction Models) — анчер для b2b-разговора об AI-агентах на телефоне.
3. **«Реклама теперь делается за 24 часа и 15 тыс ₽»** (KGM Torres) — solo/студийный production-shift для creator-контента.
4. **«Прототип за 10 минут вместо месяца»** (Claude Design game-UI) — низкий порог входа в продукт-прототипирование.

### Готовые анти-hook'и (не использовать)
1. «AI-агент заменит продакшн-команду» — тест Super Computer прямо опровергает.
2. «Просто включи агента и получи результат» — непредсказуемая token-экономика.
3. Прямое сравнение «как они делают кино за $16, так вы ставите цели в GRO» — нарушает specificity-принцип (см. neuroprozharka-страницу).

## Связь с другими страницами
- [[sources/2026-05-19-tg-cgevent-may08-19-2026]] — полная карта релевантности и фактологии
- [[volatile/weekly-digest/tg-cgevent-may-w2-2026]] — предыдущий дайджест канала (5–8 мая)
- [[volatile-strict/competitor-news/higgsfield-super-computer-agent-2026-05]] — Tier A.1
- [[volatile-strict/competitor-news/thinking-machines-interaction-model-2026-05]] — Tier A.2
- [[evolving/content-trends/ai-video-tools-stack-2026]] — Tier A.3 новые модели
- [[evolving/content-trends/neuroprozharka-ai-indie-filmmaking-format]] — Tier B.1
- [[evolving/competitor-positioning/claude-design-2026]] — Tier B.2
</content>
