---
id: mkt:canon/marketing-frameworks/landing-15min-figma-cursor
title: "Landing за 15 минут — Figma html.to.design + Cursor + Claude Code"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [landing, no-code, claude-code, cursor, figma, vibecoding, mvp, hypothesis-testing]
confidence: high
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-solokumi-redump-dec25-apr26.md]
namespace: mkt
---

# Landing за 15 минут — pipeline маркетолога без дизайнера и разработчика

8-шаговый воспроизводимый процесс, в котором маркетолог собирает кликабельный лендинг за ~15 минут, используя как референс уже понравившийся ему сайт. Подходит для тестирования гипотез: вместо того чтобы 2 недели делать «свой» дизайн с нуля или платить дизайнеру/разработчику, проверяешь оффер и контент на готовом скелете — и итерируешь.

Это canon: **сам pipeline** стабилен — копируешь дизайн как код через Figma plugin → загружаешь в Cursor → доливаешь промпт через Claude Code → итерируешь. Конкретные инструменты (cursor.com, claude.com, html.to.design, Tilda) могут смещаться, но **последовательность** «возьми готовый дизайн → переведи в код → итерируй промптом → опубликуй» — устойчивая инвариантная.

Источник: Р. Кумар Виас, [[sources/2026-05-05-tg-solokumi-redump-dec25-apr26|@solokumi]] пост 358 (2025-12-23). На том же логическом уровне, что и [[canon/marketing-frameworks/ai-video-production-pipeline]] — каноническая декомпозиция creative-задачи.

## Когда применять

- **Тестирование гипотезы** — нужен лендинг под конкретный оффер, который, возможно, протестируется и убьётся через неделю
- **MVP-запуск** — собрать минимальную целевую страницу для проверки рыночного интереса до серьёзного дизайн-вложения
- **Brief к подрядчику** — собрать draft, который потом отдадите дизайнеру/разработчику не как ТЗ-текст, а как готовый Figma-макет
- **A/B-вариант** — нужно попробовать радикально другой visual (например, скопировать дизайн конкурента и проверить, не работает ли он лучше)

**Не подходит для:** финальной production-страницы, которую вы готовы показывать публично с бренд-обязательствами. Качество результата за 15 минут — для proof-of-concept, не финальный artifact.

## Что нужно

- **Сайт-референс по дизайну** — любая страница в интернете, которая нравится визуально
- **Figma** (бесплатный аккаунт)
- **Cursor** (Claude Code как extension; подписка Claude Pro для полного доступа)
- **html.to.design** plugin для Figma
- *(опционально)* Tilda для финальной публикации

## Канонические 8 шагов

### Шаг 1 — Выбери жертву

Берёшь любой сайт, который нравится по дизайну. Импортируешь в Figma через plugin html.to.design за 2 клика. Через 1–2 минуты получаешь полностью редактируемый макет в Figma.

### Шаг 2 — Скопируй сайт как код

В Figma: `Copy as → Code → CSS (all layers)`. На выходе — HTML+CSS-блок, который вставляется куда угодно.

### Шаг 3 — Создай проект в Cursor

Установи Cursor с [cursor.com](https://cursor.com/home). В Cursor создаёшь папку, внутри неё файл `code.md`. Туда вставляешь скопированный код.

### Шаг 4 — Подключи Claude Code

В Extensions внутри Cursor находишь Claude Code, устанавливаешь, авторизуешься (нужна подписка Claude Pro). Альтернативы — обычный агент Cursor или Codex, но Claude Code лучше держит сложные задачи.

### Шаг 5 — Подготовь промпт (самая важная часть)

Это самый трудозатратный и самый ценный шаг. Виас даёт [драфт-промпт](https://docs.google.com/document/d/1EFzMUw0l0IMjKthBU0QkH7MjcO1KIPKMglX4OoBY7lE/edit) (через @solokumi 358) — его наполняешь:

- Данными о продукте (что продаём, кому, какой trade-off)
- Структурой блоков (hero, проблема, решение, CTA, отзывы, FAQ, footer)
- Параметрами от текущего CSS (использовать какие шрифты, какую палитру)

Хорошо написанный промпт — даже если этот pipeline вы потом не закончите — переиспользуем в других генераторах (Lovable, Base44, v0, Antigravity), это ваш переносимый artifact.

### Шаг 6 — Запусти генерацию

В Cursor открываешь Claude Code, вставляешь готовый промпт, ждёшь 5–7 минут. Claude собирает `index.html`, `styles.css` и связанные файлы.

### Шаг 7 — Дорабатывай итерациями

Правки прямо в чате с Claude Code. Можно:
- Писать точные правки по блокам («увеличь padding hero до 80px»)
- Прикладывать скриншот и отмечать, что не так
- Просить «обнови мобильную версию»

Чаще всего правятся: размеры шрифтов, отступы, шрифты, контраст и читаемость, мобильная версия.

### Шаг 8 — Публикация

Три варианта:
- **(a) Через GitHub** — выгружаешь файлы в репозиторий → деплоишь через Vercel/Netlify/GitHub Pages
- **(b) Через Figma** — собираешь все файлы Cursor в `.zip` → плагин `html.to.design` → вкладка `file` → импорт `.zip` обратно в Figma → отдаёшь дизайнеру/маркетологу для production
- **(c) Через Tilda** — Figma → Zero Block → Import from Figma (нужен Figma API access token) → готовый блок в Tilda

## Шаблон промпта для шага 5

В источнике Виас публикует [Google Doc-драфт](https://docs.google.com/document/d/1EFzMUw0l0IMjKthBU0QkH7MjcO1KIPKMglX4OoBY7lE/edit) — без него pipeline теряет 80% эффективности. Кастомизация под ваш продукт обязательна, но структура промпта стабильна:

1. **Контекст продукта** — что, для кого, ключевая ценность
2. **Желаемая структура блоков** — список секций с короткими описаниями содержания
3. **Дизайн-инварианты** — что переносим из исходного CSS, что меняем
4. **Tone of voice** — стиль текста на лендинге
5. **CTA-цели** — что должно произойти, когда юзер кликает

## Anti-patterns

- **Пропустить html.to.design шаг и просто сказать Claude «сделай лендинг по описанию»** — получаешь generic-AI-дизайн вместо адаптированного референса. Сила pipeline — именно в опоре на чужой работающий дизайн.
- **Не подготовить промпт перед запуском** — самый частый failure-mode. Виас называет это «самой трудозатратной и самой важной частью всего процесса». Без проработанного промпта результат — мусор.
- **Использовать первый результат как final** — это proof-of-concept, всегда планируйте 2–3 итерации правок.
- **Игнорировать мобильную версию** — Claude по умолчанию делает desktop-first; мобильная адаптация почти всегда требует отдельной итерации.

## Связь с другими страницами

- [[canon/marketing-frameworks/ai-video-production-pipeline]] — параллельный canonical pipeline для видеокреативов (та же декомпозиционная логика)
- [[canon/marketing-frameworks/claude-md-structure-marketing]] — как закрепить стиль и брендинг в `CLAUDE.md`, чтобы скилл лендинг-сборки работал воспроизводимо в команде
- [[canon/marketing-frameworks/claude-skills-architecture]] — этот pipeline можно упаковать в Claude Skill с REFERENCE.md (бренд-гайд, ToV) для всей команды
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]] — Cursor, Claude Code, Lovable, Base44, v0 — альтернативы внутри L1/L2 уровней
- [[canon/marketing-frameworks/tabunov-landing-anatomy]] — что должно быть на лендинге (анатомия), независимо от того, как ты его собрал

## Backlinks

_8 pages link to this one._

- [[canon/marketing-frameworks/ai-productivity-3-shifts-typical]]
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]]
- [[evolving/competitor-positioning/claude-design-2026]]
- [[evolving/competitor-positioning/vibecoding-stack-ecosystem-2026]]
- [[evolving/content-trends/ai-tools-self-hosting-arbitrage]]
- [[index]]
- [[overview]]
- [[sources/2026-05-05-tg-solokumi-redump-dec25-apr26]]
