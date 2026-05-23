---
id: mkt:evolving/content-trends/ai-augmented-content-consumption-pipeline-2026
title: "AI-augmented потребление контента — транскрипт → zettelkasten → generative mini-site (Аннаков, 2026-05)"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [content, ai-agents, repurposing, generative-ui, notebooklm, zettelkasten, consideration]
confidence: low
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-products-and-startups-may-15-19-2026.md]
namespace: mkt
---

# AI-augmented потребление контента — pipeline персонализации

## Наблюдение

По Байраму Аннакову (пост 1753, [[sources/2026-05-19-tg-products-and-startups-may-15-19-2026]]), длинный экспертный контент (конференции, лекции) можно потреблять **персонализированно** через AI-pipeline вместо линейного просмотра:

1. **Транскрипт** YouTube — через [yt-dlp](https://github.com/BayramAnnakov/youtube-playlist-to-markdown), либо «вручную» через AssemblyAI, если транскрипта нет.
2. **Фильтрация через личный zettelkasten** — прогон транскрипта по своей базе знаний для отбора наиболее «близких» кусочков лекции (релевантных именно тебе/твоему каналу).
3. **Generative mini-site** для дипдайва (интерактивная HTML-страница) + **NotebookLM** для прослушивания на прогулках.

Реальный артефакт этого pipeline — mini-сайт «Code with Claude 2026» (см. OCR в [[sources/2026-05-19-tg-products-and-startups-may-15-19-2026]] и дистилляцию в [[evolving/industry-trends/code-with-claude-2026-frameworks]]): Top 10 ideas, Framework Library, All Talks с фильтрами по релевантности.

## Ключевой тезис: визуализировать аутпут модели как интерактивный HTML, а не markdown

> Идея визуализировать аутпут модели в виде **HTML-странички, а не markdown-файла**, причём сделать её интерактивной — например, покрутить разные сценарии поста или лекции, нелинейно организовать материалы конференции — оказалась суперудобной и полезной. — Аннаков, пост 1753 `[conf:low, src:2026-05-19]`

Это прикладной кейс того же сдвига, что описан в [[canon/marketing-frameworks/generative-ui-design-system-inference]] (Generative UI — дизайн-система как inference-система): аутпут LLM становится не текстом, а **сгенерированным интерфейсом** под конкретную задачу/пользователя.

## Чем отличается от соседних страниц

- [[evolving/content-trends/fast-content-consumption-shift-2026]] — про **пассивное быстрое** потребление (нарезки, x1.5, demand-side attention-compression). **Эта страница** — про **активное глубокое** AI-augmented потребление (отбор релевантного, нелинейная навигация). Два противоположных полюса одного спектра «как люди потребляют длинный контент в 2026».
- [[evolving/content-trends/tg-posts-seo-repurposing]] — про репурпозинг **своего** контента под дистрибуцию. Здесь — про репурпозинг **чужого** контента под личное усвоение, но техники пересекаются (транскрипт → структурирование → новый формат).

## Почему это важно для GRO

1. **Готовый репурпозинг-pipeline для контент-команды.** ГРО производит/потребляет много экспертного видео/подкастов. Pipeline «транскрипт → фильтр через свою базу → generative HTML» — это операционный шаблон, как из одной конференции вытащить и Top-ideas-пост, и Framework Library для слайдов, и драфты постов (у Аннакова в mini-сайте прямо есть вкладка «Telegram Post Drafts»).
2. **Контент-angle про «AI меняет, как мы учимся».** Для awareness/consideration-аудитории ГРО: персонализированное потребление знаний — это growth-нарратив, конгруэнтный продукту (осознанная практика, рост навыка).
3. **Generative HTML как формат подачи.** ГРО может экспериментировать с интерактивными HTML-разборами вместо статичных постов — выше вовлечённость, нелинейная навигация.

## Hooks

- «Не смотри конференцию целиком. Прогони транскрипт через свою базу знаний — и получи только то, что близко именно тебе.»
- «Аутпут AI — это уже не markdown-файл, а интерактивная страница, которую можно крутить.» `[conf:low, src:2026-05-19]`
- «Из одной конфы — пост, слайды для курса и драфты в Telegram. Один pipeline.»

## Caveat'ы и TTL

- `confidence: low` — личная методология одного эксперта (verified), не индустриальный стандарт. Но техники (yt-dlp, AssemblyAI, NotebookLM, generative HTML) — реальные и воспроизводимые.
- `evolving`, TTL soft 180 дней. Re-verify к 2026-11: стал ли «generative mini-site вместо markdown» массовым форматом; появились ли turnkey-инструменты для этого pipeline.

## Связанные страницы

- [[evolving/industry-trends/code-with-claude-2026-frameworks]] — артефакт этого pipeline (дистилляция конференции)
- [[canon/marketing-frameworks/generative-ui-design-system-inference]] — теоретическая рамка «аутпут как интерфейс»
- [[evolving/content-trends/fast-content-consumption-shift-2026]] — противоположный полюс (пассивное быстрое потребление)
- [[evolving/content-trends/tg-posts-seo-repurposing]] — репурпозинг контента под дистрибуцию
- [[sources/2026-05-19-tg-products-and-startups-may-15-19-2026]] — источник (пост 1753)
