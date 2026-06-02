---
id: mkt:canon/marketing-frameworks/llm-task-spec-decomposition-molyanov
title: Декомпозиция сложной задачи через нейросеть (user-spec → tech-spec → атомарные задачи)
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [ai, frameworks, productivity, copywriting, agentic]
confidence: medium
stale: false
created: 2026-06-01
updated: 2026-06-01
sources: [sources/2026-06-01-condense-vcru-molyanov-may-2026.md, sources/2026-06-01-vc-ru-molyanov-2324828-kak-reshat-sloznye-zadachi-s-pomoshchyu-ney.md, sources/2026-06-01-vc-ru-molyanov-2315566-kak-claude-code-upravlyaet-zadachami-s-pomo.md, sources/2026-06-01-vc-ru-molyanov-2697980-kak-nakapyvat-opyt-rabotyi-s-neyronnyimi-se.md]
namespace: mkt
---

# Декомпозиция сложной задачи через нейросеть

Reusable-методология Павла Молянова (verified expert) для задач, в которых ты сам мало разбираешься — применима и к вайбкодингу, и к управлению компанией, и к контент-продакшену. Canon: подход стабилен между версиями моделей. По мнению автора (атрибуция, conf:medium).

## Шаблон «user-spec → tech-spec → атомарные задачи»

По мнению Молянова [[sources/2026-06-01-vc-ru-molyanov-2324828-kak-reshat-sloznye-zadachi-s-pomoshchyu-ney]], последовательность такая:

1. Дать нейронке контекст «кто я / что за проект».
2. Описать задачу как понимаешь.
3. Нейросеть задаёт много уточняющих вопросов.
4. Отвечаешь.
5. Нейросеть приносит **user-spec** — понятийное ТЗ простыми словами (по SMART).
6. После согласования превращает его в подробный **tech-spec** на много страниц.
7. Бьёт tech-spec на **атомарные задачи** с критериями приёмки.

Ключ — не прыгать сразу к исполнению, а дать модели вытащить из тебя контекст вопросами и зафиксировать его письменно до начала работы.

## Связка агентов в контент-продакшене

Молянов строит «связку агентов» для копирайтинга по аналогии с разработкой [[sources/2026-06-01-vc-ru-molyanov-2315566-kak-claude-code-upravlyaet-zadachami-s-pomo]]: агент-сеошник собирает семантику → анализирует выдачу → пишет ТЗ → агент-автор собирает инфу и пишет план → редактор согласовывает → черновик → финальную статью проверяют сеошник, редактор и корректор. Цель — готовая статья для публикации на vc.ru/Reddit без ручной сборки. Под свои задачи он построил 6 агентов в Claude Code (каждый под участок работы, строил ~1,5 месяца).

## Накопление опыта во внешней документации

Дополняющий принцип [[sources/2026-06-01-vc-ru-molyanov-2697980-kak-nakapyvat-opyt-rabotyi-s-neyronnyimi-se]]: «агенты пока не умеют накапливать опыт сами — новая сессия = новый болванчик». Задача «руководителя ИИ» — фиксировать накопленный опыт во внешней документации (CLAUDE-подобные md-файлы), а не в чате. Каждый раз, когда агент лажает → сразу дописывать/править инструкцию, чтобы ошибка не повторилась.

## Применение к GRO

- Шаблон спецификации — готовый content-hook для сегмента «предприниматели/фрилансеры»: «не давай нейронке задачу — дай ей вытащить из тебя ТЗ».
- Принцип «опыт живёт в документации, а не в чате» переносится на любой knowledge-work и резонирует с позиционированием GRO как системы, а не разовых сессий.

## Связанные страницы
- [[sources/2026-06-01-condense-vcru-molyanov-may-2026]]
- [[canon/marketing-frameworks/harness-engineering-for-ai-agents]]
- [[evolving/content-trends/molyanov-ai-content-automation-patterns]]
- [[evolving-strict/competitor-metrics/claude-opus-4-6-release-benchmarks-2026]]
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]
