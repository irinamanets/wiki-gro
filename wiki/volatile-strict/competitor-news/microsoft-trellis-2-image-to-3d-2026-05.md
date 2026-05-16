---
id: mkt:volatile-strict/competitor-news/microsoft-trellis-2-image-to-3d-2026-05
title: "Microsoft TRELLIS.2 — open-source 4B Image-to-3D модель (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: competitor-news
tags: [microsoft, open-source, ai, 3d, image-to-3d, creative-tools, gen-ai]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-bezsmuzi-may-5-7.md]
namespace: mkt
---

# Microsoft TRELLIS.2 — open-source Image-to-3D (май 2026)

Microsoft опубликовала **TRELLIS.2** — open-source модель на 4B параметров, генерирующая 3D-ассеты из одного входного изображения. Релиз: GitHub `microsoft/TRELLIS.2`. Сигнализировано Кульгиным в @bezsmuzi пост 15892 (2026-05-06), см. [[sources/2026-05-14-tg-bezsmuzi-may-5-7]].

**Почему `volatile-strict`:** Конкретный релиз с числовыми параметрами и публикационной датой; news о творческих AI-инструментах устаревает за квартал.

## Технические параметры

| Параметр | Значение | Source |
|---|---|---|
| Размер модели | 4B параметров | `[conf:medium, src:2026-05-06]` |
| Архитектура | Native 3D VAE | `[conf:medium, src:2026-05-06]` |
| Пространственное сжатие | 16x | `[conf:medium, src:2026-05-06]` |
| Лицензия | Open-source (GitHub: microsoft/TRELLIS.2) | `[conf:medium, src:2026-05-06]` |
| Input | Image | `[conf:medium, src:2026-05-06]` |
| Output | 3D asset | `[conf:medium, src:2026-05-06]` |

> «Модель построена на нативных 3D VAE с 16-кратным пространственным сжатием, что даёт более эффективную, масштабируемую и детализированную генерацию 3D-объектов.» (Кульгин ретранслирует).

## Сигнал — bigtech open-sources core tools

TRELLIS.2 продолжает паттерн **bigtech освобождает creative-tools в open-source**, который Anthropic делает для MCP ([[evolving/industry-trends/anthropic-creative-tools-mcp-2026]]), Google для Gemini-models, Meta для Llama. Стратегическое следствие:

- **Open-source creative AI становится default** для creators / 3D-artists, **не proprietary SaaS**. Это давление на closed-source players типа Polycam, Spline, Kaedim.
- **Image-to-3D capability commoditizes.** В сегменте AR/VR/game-dev / e-commerce 3D-моделей — стоимость генерации ассета падает к нулю при наличии GPU локально или дешёвого cloud-inference.
- **Microsoft strategy:** AI research arm pushes open-source releases как противовес OpenAI proprietary stack (несмотря на инвестиции). Это **внутри-Microsoft хеджирование**.

## Маркетинговые выводы для GRO

1. **Если GRO когда-либо войдёт в 3D / AR / визуализацию продуктов** — TRELLIS.2 как **out-of-the-box** capability для product mockups без графического дизайнера. Используется в conjunction с FLUX/SDXL для image-generation первого шага.
2. **Контент-хук:** «Microsoft выложил Image-to-3D модель в open-source. 3D ассет из одной фотки. Что это значит для маркетинговых креативов next-quarter?»
3. **Watch list:** появится ли в Russian creator-economy инструмент-обёртка над TRELLIS.2 (типа neuroprozharka использует Stable Diffusion как backend) — это marker для **AI-creator-stack локализации**.

## TTL и план верификации

- **TTL: 90 дней** (до 2026-08-14). Re-verify: появятся ли benchmark vs. конкуренты (Hunyuan3D, RodinAI, Trip3D), как принят open-source community.
- **Контр-сигнал:** если license issues или quality complaints — пересмотреть `confidence`.

## Связанные страницы

- [[evolving/industry-trends/anthropic-creative-tools-mcp-2026]] — параллельный bigtech open-source push
- [[evolving/industry-trends/software-moat-erosion-2026]] — рамка commoditization
- [[evolving/content-trends/ai-video-tools-stack-2026]] — родственный сегмент
- [[volatile-strict/competitor-news/openai-codex-vs-claude-code-2026-05]] — competitor pattern
- [[sources/2026-05-14-tg-bezsmuzi-may-5-7]] — первоисточник, пост 15892
