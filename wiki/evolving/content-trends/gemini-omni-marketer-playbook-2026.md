---
id: mkt:evolving/content-trends/gemini-omni-marketer-playbook-2026
title: "Gemini Omni для маркетолога: reuse-first playbook + 5 use-case промптов + prompt-формула (май 2026)"
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [gemini-omni, video, ai, prompt-formula, marketing-playbook, kumar-vias, reuse, content-production, performance-creatives]
confidence: medium
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-solokumi-may-20-22-2026.md]
namespace: mkt
---

# Gemini Omni для маркетолога: reuse-first playbook (май 2026)

**Тезис.** В отличие от стека генеративных видео-моделей ([[evolving/content-trends/ai-video-tools-stack-2026]]), которые конкурируют **между собой** на метрике «качество генерации с нуля», Gemini Omni открывает **новый use-case класса** — **редактирование и пересборка существующего видео-контента через текстовый чат**. Главная operational рекомендация Романа Кумара Виаса ([[sources/2026-05-26-tg-solokumi-may-20-22-2026|@solokumi пост 419]], 2026-05-22) для маркетологов:

> Маркетосам нужно **первым делом тестировать не генерацию с нуля, а реюзать старые фото продукта и горизонтальные ролики**. Omni интересен не как десятый генератор слоповых видосов, а как **флоу переработки того, что уже есть**.

Это **evolving**: сам **класс use-case** (reuse over generate) стабилен, но **набор capabilities Omni** + **best-practice промпты** дрейфуют с каждым релизом. Каноническая база — [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05|официальный анонс на Google I/O 2026]].

## Главная operational рамка: reuse > generate

| Подход | Когда применять | Стек |
|---|---|---|
| **Generate** (генерация с нуля) | Когда нужно **сценарий, которого нет в существующих ассетах** (street interview, character-driven story) | Seedance 2.0, Veo3, Sora 2 — см. [[evolving/content-trends/ai-video-tools-stack-2026]] |
| **Reuse** (пересборка существующего) | Когда есть **горизонтальные ролики / фото продукта / скрины / маршруты**, и нужно **адаптировать в новый формат** (вертикаль, разные стили, A/B тесты креатива) | **Gemini Omni Flash** |

**Почему reuse-first работает для маркетинга:** у любого продукта с 2+ года истории **уже есть**: пакет фото продукта в разных ракурсах, набор горизонтальных рекламных роликов, скрины UI, photo-shoot материалы. **Эти ассеты лежат мёртвым грузом** на диске, потому что не подходят под текущий формат (вертикаль для Shorts, новый стиль). Omni позволяет **переработать накопленный контент за минуты**, без перебора съёмочной команды.

## 5 use-case промптов от Кумара Виаса (для маркетинга — actionable)

Все 5 промптов даны дословно в посте 419 — можно копировать и тестировать. Адаптировано под GRO / fitness-app маркетинг в комментариях ниже.

### I. Шортс из 8-10 случайных фото галереи за минуту

```
Turn these photos into a 10-second travel recap in 9:16. Keep real people recognizable, add smooth movement between shots, warm color grading.
```

**Use-case для маркетинга:** превращение **накопленного фото-stock'а** (фотографии счастливых пользователей, скриншоты тренировок, фото офиса) в готовый Reels/Shorts **за минуту** без участия монтажёра.

**GRO-application:** скриншоты UI с разных этапов тренировки → 10-секундный recap «как одна тренировка проходит». Или фото пользователей с подписями (через альт-данные стора) → testimonial Reel.

### II. 5 вариантов рекламы из одного фото продукта (база + ремикс)

```
Use this photo as the base. Keep the logo unchanged. Create a 10-second vertical ad with slow camera movement and a clean CTA frame. Do not invent new packaging text.
```

Затем ремикс:

```
Change the background to dark luxury, keep the lighting
```

**Use-case для маркетинга:** **массовое A/B тестирование креативов** на одном продукте — генерируешь 5+ вариантов рекламы из одного исходника, тестируешь все в performance-кампании, оставляешь победителя.

**GRO-application:** скриншот трекинга прогресса → 5 вариантов «утренний / вечерний / спортзал / дом / парк». Тестируешь, какой контекст лучше конвертит сегмент «карьерист 28+ м».

**Inline-маркер для GRO:** прямая параллель с [[canon/marketing-frameworks/andromeda-creative-framework-2026|Andromeda creative framework]] — массовое производство креативов делает performance-кампанию устойчивее к креатив-burnout.

### III. Старый горизонтальный ролик → вертикальный Shorts

```
Recut into a 9:16 vertical. Keep the speaker centered, add faster pacing and captions. Do not invent new scenes.
```

**Use-case для маркетинга:** **миграция накопленного youtube-контента в Shorts/Reels/TikTok** без пересъёмки. Захватывает **второй жизненный цикл** контента.

**GRO-application:** старые лендинговые видео с CMO про продукт → вертикальный Reels с автоподписями для TikTok-аудитории. Перевыпуск без затрат.

### IV. Скрин Google Maps маршрута → travel POV видео

```
Turn this Google Maps route into a first-person travel video. Keep it realistic. Add city sounds and warm evening lighting. 15-second vertical.
```

**Use-case для маркетинга:** **превращение data-визуализации в эмоциональный контент**. Маршрут на карте — статичен, POV-видео — эмоционально и привлекательно.

**GRO-application:** статистика прогресса (график веса / силы / выносливости) → POV-видео «недельная прогулка по парку, который ты прошёл за неделю, измеряемая в км». Превращает абстрактные числа в фигурально проходимое пространство.

### V. AI-аватар себя в студийной интро-сцене

```
Appear in a clean minimal studio with confident posture and soft lighting. Keep my face and movements natural. 15-second vertical intro.
```

**Use-case для маркетинга:** **бесконечная фабрика контента для founder-led brand** или эксперта без съёмочной площадки. Один раз сделал AI-аватар → бесконечно ставишь в любые сцены.

**GRO-application:** AI-аватар CMO / founder GRO → серия 15-секундных видео под все направления (тренинг, нутриция, мотивация) без физических съёмок.

**Кумар Виас фреймит это как killing-feature:** «будем тестить» на Refocus.

## Prompt-формула Gemini Omni (Кумар Виас, дословно)

```
Use this as the base [вводные] → Keep [что нельзя менять] → Change [что нужно менять] → Add [добавь стиль/движение] → Output as [формат] → Do not add [что не нужно]
```

**6 операционных слотов** в формуле:

| Слот | Что заполняет | Пример |
|---|---|---|
| `Use this as the base` | Указатель на reference-файл (фото/видео/скрин) | «Use this product photo as the base» |
| `Keep` | **Защитная инструкция** — что нельзя менять (брендинг, лицо, лого) | «Keep the logo unchanged, keep the speaker's face identifiable» |
| `Change` | Что нужно изменить (фон, ракурс, цвет, объект) | «Change the background to dark luxury» |
| `Add` | Добавить стиль или движение (камера, lighting, color grading) | «Add slow camera movement, warm color grading» |
| `Output as` | Формат вывода (длительность, ratio, разрешение) | «Output as 10-second vertical 9:16» |
| `Do not add` | **Anti-hallucination guard** — что НЕ должно появиться | «Do not invent new packaging text, do not add subtitles» |

**Почему формула работает (4 слота — defensive, 2 — generative):**
- `Keep` + `Do not add` — **defensive слоты**: предотвращают мутацию ассета. Это **главная проблема reuse-флоу** — без них Omni «творит», а ты хотел минимальную правку.
- `Use this as the base` + `Output as` — **structural слоты**: задают контейнер.
- `Change` + `Add` — **generative слоты**: единственные, где Omni реально работает creative.

**Operational tip:** при первой пробе обязательно класть **сильные `Keep` + `Do not add` инструкции** — иначе Omni добавит логотипы, выдуманные подписи, лишние объекты.

**Официальный гайд Google по формуле:** [deepmind.google/models/gemini-omni/prompt-guide](https://deepmind.google/models/gemini-omni/prompt-guide/). Дополнительные примеры с разбором: [gemini-omni-ai.org/video-prompts](https://gemini-omni-ai.org/video-prompts).

## Доступ и стек

**Стек по контексту использования** (по [@solokumi пост 419](https://t.me/solokumi/419)):

| Окно | Сценарий | Где |
|---|---|---|
| **Быстрые правки** (1 видео за минуту) | A/B тесты, итеративные правки | **Gemini app** — chat-based интерфейс |
| **Полноценный продакшн** (storytelling, multi-shot) | Кампания-серия, бренд-ролик | **Google Flow** — продвинутый UI |
| **Публикация** | Прямой выпуск | **YouTube Shorts** — публикация одной кнопкой |

**Pricing (vision-confirmed в Google Flow):**
- **Omni Flash:** 30 credits / video (10 сек) — план AI Plus $20/мес даёт 1 000 кр = **33 видео/мес** `[conf:high, src:2026-05-20]`
- AI Plus от $20/мес, AI Ultra от $100/мес `[conf:high, src:2026-05-20]`

См. подробное сравнение и pipeline-prescription Цыпцына («генерация в Seedance, редактирование в Omni») в [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]].

## Ограничения для маркетингового pipeline

**Текущие узкие места Omni Flash (на 2026-05-22):**

1. **Качество генерации с нуля — слабее Seedance** (см. оценку @cgevent в [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05|основной странице Omni]]). Это **подтверждает reuse-first позиционирование** — если генерировать с нуля, Omni не лучший выбор.
2. **Длительность 10 секунд** (60 кадров) — узкое место для длинных стори. Для performance-креативов это idealn, для бренд-роликов мало.
3. **Цензура** — детали скачут у Avatar/Cameo (очки исчезают, борода меняется) — пока не для серьёзного founder-led video, скорее для творческих экспериментов.
4. **Pricing per-credit** — для **массового производства креативов** (100+ роликов / месяц) Seedance остаётся дешевле ($0.03/sec у Seedance vs ~$0.06/sec эквивалент у Omni Flash в Google Flow).

**Что меняет это положение в ближайшие 3–6 месяцев** (декларированное Google в I/O):
- Длительность **до 30 секунд** (обещано в подкасте Introducing Gemini Omni)
- **Video-референс лица** (KYC-style scan) — улучшит Avatar/Cameo консистентность
- Tooling для **storytelling** в Flow (длинные продолжения клипов)

## Cross-application к GRO

**MVP-эксперимент** для маркетинговой команды GRO (1 неделя):

1. **День 1:** Купить AI Plus подписку ($20). Собрать рабочий пакет ассетов: 10 фото продукта (UI screenshots, маркетплейс-скрины), 3 горизонтальных видео с прошлых кампаний, 1 фото CMO.
2. **День 2–3:** Прогнать все 5 use-case промптов на собственных ассетах, оценить, какие 2–3 дают **прямо публикуемый** результат.
3. **День 4:** Сделать prompt-template библиотеку для команды по формуле Кумара Виаса (со слотами `Keep` / `Do not add` под GRO-бренд-гайдлайн).
4. **День 5:** Запустить **A/B тест в performance-кампании**: 10 креативов сгенерированы через Omni (reuse-flow), 10 креативов сгенерированы через старый pipeline. Метрика — CPM, CTR, CPA. Итоги — через 2 недели.

**Ожидаемый результат на бенчмарках Refocus/Kumar:** **снижение CPM креатива в ~3-5×** vs съёмка реального ролика, при сопоставимой конверсии.

## Связь с другими страницами

- [[evolving/content-trends/ai-video-tools-stack-2026]] — общий стек AI-видео моделей; эта страница — **operational playbook одного из инструментов стека** под маркетинговый use-case
- [[volatile-strict/competitor-news/google-gemini-omni-video-2026-05]] — каноническая страница Gemini Omni (релиз, pricing, capability-разбор)
- [[canon/marketing-frameworks/ai-video-production-pipeline]] — 5-этапный pipeline; **Omni захватывает этап V (правки/адаптация) полнее, чем предшествующие модели**
- [[canon/marketing-frameworks/andromeda-creative-framework-2026]] — рамка массового производства креативов; Omni делает массу 5× дешевле для reuse-сценария
- [[evolving/content-trends/ai-static-creative-templates-2026]] — параллельный стек статических креативов; Omni закрывает разрыв static → video
- [[evolving/industry-trends/ai-native-marketer-skillset-2026]] — навыки AI-маркетолога; prompt-формула Omni — новый required-навык
- [[sources/2026-05-26-tg-solokumi-may-20-22-2026]] — первоисточник, @solokumi пост 419, 2026-05-22

## Sources

- [[sources/2026-05-26-tg-solokumi-may-20-22-2026]] — Кумар Виас @solokumi пост 419, 2026-05-22, маркетинговый разбор Gemini Omni: 5 use-cases + prompt-формула + reuse-first рекомендация
