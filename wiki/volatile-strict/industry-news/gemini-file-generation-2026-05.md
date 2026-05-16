---
id: mkt:volatile-strict/industry-news/gemini-file-generation-2026-05
title: "Gemini генерит Workspace-файлы и форматы документов (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [google, gemini, file-generation, workspace, anthropic-parity]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-cgevent-apr30-may05-2026.md]
namespace: mkt
---

# Gemini — file generation парность с Claude (май 2026)

Google объявил, что **Gemini теперь умеет генерировать разные типы файлов** `[conf:high, src:2026-05-01]`. Это **догоняющий шаг** — Claude умеет так давно `[conf:high, src:2026-05-01]`.

## Поддерживаемые форматы

`[conf:high, src:2026-05-01]`:

- **Workspace files**: Docs, Sheets, Slides
- **Document formats**: .pdf, .docx, .xlsx, .csv
- **Markup/text**: LaTeX, Plain Text (TXT), Rich Text Format (RTF), Markdown (MD)

Источник: [blog.google/innovation-and-ai/products/gemini-app/generate-files-in-gemini](https://blog.google/innovation-and-ai/products/gemini-app/generate-files-in-gemini/).

## Реальные ограничения (из теста @cgevent)

@cgevent протестировал — отчёт:

- **Сгенерил Excel с диаграммой → справился** `[conf:medium, src:2026-05-01]`
- **Просил отредактировать PDF → начал тупить**: `[conf:medium, src:2026-05-01]`
  - С пятого раза отдал ссылку на скачивание
  - Долго отнекивался
  - **Не смог сохранить одну из картинок внутри документа**

Вывод автора: «**это скорее генерация документов, чем редактирование**» `[conf:medium, src:2026-05-01]`. То есть Gemini = **good for create-from-scratch, not for round-trip editing** существующих документов.

## Маркетинговое значение

### Парность с Claude по generation files

Это очередное проявление **feature-parity race** между frontier-models. Сценарий:
- Anthropic делает feature
- 6-12 месяцев потом Google добавляет ту же feature
- Через ещё 6 месяцев OpenAI добавляет

Это **снижает дифференциацию по features**, и сила переходит в:
1. Цену
2. Скорость
3. Интеграции с экосистемой
4. Надёжность

Применимость для GRO marketing-нарратива слабая (GRO не frontier-model AI-tool). Но как **anchor** для разговоров о AI-tools commoditization: «features больше не отличают лидеров, отличают integration-quality».

### Hook для блог-постов про AI-tools

«Gemini теперь генерит Excel-файлы. Claude умеет так давно. Через полгода все frontier models будут уметь то же самое. Что отличает — **глубина интеграции в workflow пользователя**, не сам факт `<feature X>`. Это применимо и к product-design GRO». `[conf:medium, src:2026-05-01]`

## Связь с другими wiki-страницами

- [[volatile-strict/industry-news/ai-model-releases-mar-apr-2026]] — параллельный модель-релиз tracker
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — Q2 2026 общая картина
- [[volatile-strict/competitor-news/google-gemini-macos-native-app-2026-04]] — параллельный Google Gemini шаг
- [[canon/positioning/gro-value-proposition]] — дифференциация через системность, не features
- [[sources/2026-05-05-tg-cgevent-apr30-may05-2026]] — источник
