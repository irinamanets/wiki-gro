---
id: mkt:canon/brand-guidelines/gro-typography
title: GRO — типографический стек бренда
type: page
subtype: concept
layer: canon
theme: brand-guidelines
tags: [brand-guidelines, visual-identity, typography, web-app]
confidence: medium
stale: false
created: 2026-04-10
updated: 2026-04-10
sources: [sources/2026-04-10-gro-lk-auth.md]
namespace: mkt
---

# GRO — типографический стек бренда

Первый каноничный сигнал о визуальной идентичности GRO. До этого ingest'а раздел [[canon/brand-guidelines]] был пустым (см. gap в [[overview]]).

Источник — [[sources/2026-04-10-gro-lk-auth|веб-кабинет `lk.groapp.ru/auth/`]], в HTML-шелле которого команда явно **preload'ит** все шрифты, используемые в продукте. Preload-тегов в `<head>` — это строго те шрифты, которые команда считает обязательными к моментальной отрисовке, то есть **активно используются** в интерфейсе (а не лежат в fallback-стеке).

**Почему `confidence: medium`, а не `high`:** источник один (веб-кабинет), лендинг `groapp.ru` построен на Tilda и использует свою типографику, стор-листинги вообще не раскрывают шрифты. Для повышения до `high` нужно второе независимое подтверждение — скриншот мобильного приложения, design-system документ от команды, или лендинг на том же стеке. Сам стек как **факт существования** — `high`, а вот «это весь брендовый стек» — `medium`, потому что может не закрывать все поверхности.

## Три шрифта стека

| Шрифт | Роль | Гарнитура | Вариаций в preload |
|---|---|---|---|
| **Montserrat** | Основной body / UI | Sans-serif, geometric | 8 весов × (regular + italic) = 16 файлов |
| **Unbounded** | Дисплейный / акцентный | Sans-serif, display, с характерными широкими пропорциями | 1 файл (Regular) |
| **SpaceMono** | Моноширинный | Monospace, technical | 1 файл (Regular) |

### Montserrat — основной шрифт

Montserrat в стеке подан **максимально полным набором весов**:

- Thin (100) + italic
- ExtraLight (200) + italic
- Light (300) + italic
- Regular (400) + italic
- Medium (500) + italic
- SemiBold (600) + italic
- Bold (700) + italic
- ExtraBold (800) + italic
- Black (900) + italic

Команда явно держит возможность использовать **любой вес от Thin до Black**, что означает: в продукте предусмотрена богатая типографическая иерархия (не два-три веса, а весь спектр). Это характерно для зрелых дизайн-систем, где одна гарнитура закрывает весь UI от мелкой подписи до заголовка-афиши.

**Характер Montserrat:** geometric sans-serif, вдохновлённый вывесками buenos-aires'кого района Монтсеррат; популярен в tech-продуктах и b2c-стартапах за нейтральность и чистоту. Это **безопасный, современный, легко читаемый выбор** — GRO не пытается выглядеть avant-garde, команда идёт в мейнстрим startup-эстетики.

### Unbounded — дисплейный акцент

Unbounded — display sans-serif от российской студии Contrast Foundry. Характерные широкие пропорции, жирные формы, геометрия с лёгкой экспрессией.

**Маркетинговое следствие:** Unbounded — **осознанный акцент на российской графической сцене**. Это не «взяли первый попавшийся Google-шрифт», это выбор с design-сторителлингом. В контенте про GRO (например, founder-интервью о том, как строится продукт) это можно использовать как микро-proof-point: «русскоязычный продукт для российского рынка, который даже в типографике поддерживает российский design community».

Preload только **Regular** — это значит, что Unbounded используется **точечно**, скорее всего только для дисплейных элементов: крупные заголовки hero-экранов, акцентные цитаты, возможно логотип-wordmark. Если бы он шёл на весь текст, команда preload'ила бы минимум Bold.

### SpaceMono — моноширинный

SpaceMono — open-source моноширинный шрифт от Google Fonts, автор Colophon Foundry. Используется в tech-продуктах для отрисовки кода, чисел, таймеров, данных.

**Маркетинговое следствие:** наличие моноширинного шрифта **в брендовом стеке pre-auth формы** — сильный сигнал о том, что в интерфейсе GRO есть элементы, требующие моноширинной подачи. Гипотезы (`conf:medium`):

- Счётчики прогресса («Шаг 3 из 6»)
- Таймеры тренировок (до 20 минут на тренировку — в [[canon/product-knowledge/gro-app-overview|обзоре]] упомянуто)
- Числовые метрики в диагностике
- OTP-коды в форме регистрации

Preload только Regular, без Bold — SpaceMono тоже точечный акцент.

## Как использовать в контенте

Три практических следствия для marketing-memory:

1. **Если в собственном контенте (посты, статьи, презентации, промо-материалы) команда использует бренд-шрифты, а не произвольные — канон:** Montserrat для body/UI, Unbounded для акцентов, SpaceMono для чисел/кода. Это закрывает открытый вопрос «каким шрифтом набирать маркетинговые материалы про GRO».
2. **Design-сторителлинг.** Комбинация «международный Montserrat + российский Unbounded + техничный SpaceMono» — готовая канва для поста о том, как GRO строит визуальную идентичность (international foundation + local craft + tech accent). Это переиспользуемый hook.
3. **Визуальная консистентность между каналами.** Если стор-скриншоты, лендинг и веб-кабинет должны выглядеть одинаково, дизайнерам контента достаточно проверить одну вещь — используют ли они эти три шрифта. Если да — совпадение с продуктом гарантировано; если нет — материалы визуально «отклеиваются» от продукта.

## Что НЕ задокументировано (gaps)

- **Типографическая иерархия**: какие размеры у H1/H2/body/caption, какие line-height, letter-spacing. Стек определён, но точные параметры — нет.
- **Фирменные цвета.** CSS-бандл веб-кабинета не прочитан — цвета в вики не занесены. Следующий шаг — ingest визуального дизайна (скриншоты приложения или лендинга + извлечение palette).
- **Tone of voice в копирайтинге.** Заголовок «Сохраним твою точку старта» на веб-кабинете — один сильный образец, но не правило. Нужно больше точек данных (тексты стор-листингов, лендинг, testimonials) для синтеза toV-guidelines.
- **Logo/wordmark** — как нарисован логотип GRO, какая типографика в нём заложена (подозреваем Unbounded, но не проверено).
- **Mobile vs web consistency.** Этот ingest видит только web-версию. Использует ли мобильное приложение те же шрифты (что логично при общем React Native кодбейсе, см. [[canon/product-knowledge/gro-web-app#технологический-стек]]) — гипотеза `conf:medium`, не подтверждено.

## Связанные страницы

- [[canon/product-knowledge/gro-web-app]] — веб-версия, из которой извлечён стек
- [[canon/product-knowledge/gro-app-overview]] — обзор продукта, визуальная идентичность которого здесь описана
- [[canon/positioning/gro-value-proposition]] — позиционирование, с которым должна визуально согласовываться типографика
- [[sources/2026-04-10-gro-lk-auth]] — источник данных о стеке

## Backlinks

_29 pages link to this one._

- [[canon/brand-guidelines/lapshina-founder-tov]]
- [[canon/marketing-frameworks/ankusheva-ai-implementation-triad]]
- [[canon/marketing-frameworks/patagonia-refusal-as-asset]]
- [[canon/product-knowledge/gro-web-app]]
- [[evolving-strict/market-data/app-store-slop-2026]]
- [[evolving/competitor-positioning/settersgroup-ecosystem]]
- [[evolving/competitor-positioning/tbank-premium-sub-brand-palette]]
- [[evolving/competitor-positioning/vyakuba-sales-training]]
- [[evolving/content-trends/ai-product-engineer-content-hooks]]
- [[evolving/content-trends/entertainment-over-pain-framing]]
- [[evolving/content-trends/moreynis-hand-drawn-meme-format]]
- [[evolving/content-trends/podcast-driven-author-channel-patterns]]
- [[evolving/content-trends/psilonsk-channel-patterns]]
- [[evolving/content-trends/psilonsk-management-hooks-bank]]
- [[evolving/content-trends/smm-strategy-trends-2026]]
- [[evolving/content-trends/tabunov-founder-growth-hooks]]
- [[evolving/content-trends/telegram-author-channel-patterns]]
- [[evolving/content-trends/telegram-native-formats]]
- [[evolving/content-trends/weekly-news-roundup-yt-format-gorny]]
- [[evolving/content-trends/your-pet-project-channel-hooks]]
- [[evolving/content-trends/youtube-thumbnail-face-trend]]
- [[evolving/industry-trends/russian-cultural-code-branding-2026]]
- [[index]]
- [[overview]]
- [[sources/2026-04-10-gro-lk-auth]]
- [[sources/2026-04-14-tg-wtf-hr-nov24-oct25]]
- [[sources/2026-05-05-tg-psilonsk-may-2026-extension]]
- [[volatile-strict/competitor-news/microsoft-copilot-agents-2026-04]]
- [[volatile/weekly-digest/voronin-community-tech-feb-apr-2026]]
