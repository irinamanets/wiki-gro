---
id: mkt:evolving-strict/competitor-metrics/atlanty-community-engagement-metrics-2026
title: "Бизнес-клуб «Атланты»: community-engagement метрики (апрель 2026)"
type: page
subtype: metric
layer: evolving-strict
theme: competitor-metrics
tags: [competitor, community, club, ru, benchmark, engagement, telegram]
confidence: medium
stale: false
created: 2026-05-19
updated: 2026-05-19
sources: [sources/2026-05-19-tg-community-tech-voronin-april-recap-991.md]
namespace: mkt
---

# Бизнес-клуб «Атланты»: community-engagement метрики (апрель 2026)

Реальные self-reported метрики платного бизнес-клуба «Атланты» (founder — Михаил Воронин) за апрель 2026, опубликованные в месячном recap-посте + инфографике «Ключевые цифры» на канале [@community_tech](https://t.me/community_tech/991), 2026-05-15. Это **первый numeric benchmark по членской базе** этого конкретного игрока — раньше «Атланты» фигурировали в wiki только качественно (см. [[evolving/industry-trends/ru-smb-mentor-community-market-2026]]).

`confidence: medium` — числа self-reported клубом в маркетинговом recap-посте, без независимой верификации (нет публичного аудита, нет внешней TG-аналитики). Достаточно конкретны для use как порядок величины и benchmark engagement-механик, но не как hard-факт о размере клуба. Цитировать только с атрибуцией.

## Снимок метрик (апрель 2026)

Метрики разделены на **stock** (накопленный размер базы) и **flow** (активность за месяц):

| Метрика | Значение | Тип | Source |
|---|---|---|---|
| Предпринимателей в сообществе (всего) | 1231 | stock | `[conf:medium, src:2026-05-15]` |
| Новых резидентов за месяц | 16 | flow | `[conf:medium, src:2026-05-15]` |
| Мероприятий проведено за месяц | 90 | flow | `[conf:medium, src:2026-05-15]` |
| Решённых запросов внутри сообщества за месяц | 215 | flow | `[conf:medium, src:2026-05-15]` |
| Благодарностей между резидентами за месяц | 259 | flow | `[conf:medium, src:2026-05-15]` |

Числа **1231** и **16** присутствуют только в инфографике-картинке, числа **90/215/259** дублируются и в тексте поста, и в инфографике. См. [[sources/2026-05-19-tg-community-tech-voronin-april-recap-991]] раздел «Распознанный текст».

## Производные коэффициенты (расчётные)

Расчёты ниже выведены из чисел выше — это аналитический слой, не первичные данные. Полезны как engagement-benchmark для membership-сообщества:

- **Месячный прирост базы (gross):** 16 / 1231 ≈ **1,3%** новых резидентов к базе за месяц `[conf:medium, src:2026-05-15]` (без данных о churn это gross, не net — нетто-прирост может быть ниже).
- **Плотность мероприятий:** 90 мероприятий / 1231 резидент ≈ **0,073 события на резидента в месяц**, или ~**3 мероприятия в день** при ~30 днях `[conf:medium, src:2026-05-15]`. Это очень высокий event-throughput — клуб операционализирует «90 событий/мес» как core proof-of-vitality.
- **Peer-to-peer reciprocity:** 259 благодарностей / 1231 резидент ≈ **0,21 благодарности на резидента в месяц** `[conf:medium, src:2026-05-15]`. Клуб трекает «благодарности друг другу» как proxy-метрику социального капитала внутри сообщества — нетипичный, но осмысленный engagement-KPI для community-продукта.
- **Resolution throughput:** 215 решённых запросов / 1231 резидент ≈ **0,17 решённого запроса на резидента в месяц** `[conf:medium, src:2026-05-15]`. «Решённый запрос» = peer-help событие (резидент попросил → сообщество/АтлантGPT помогло), что клуб использует как доказательство utility членства.

**Caveat по attribution:** все коэффициенты — функция от self-reported числителя и знаменателя; sample = маркетинговый recap (selection bias в сторону «хороших» месяцев). Не использовать как hard-бенчмарк, только как порядок величины и иллюстрацию того, **какие KPI** клуб публично трекает.

## Что эти метрики говорят о модели «Атланты»

1. **Размер базы ~1200 платящих резидентов** — это order-of-magnitude больше, чем у emerging-игроков категории (Команда А Крылова ~200+, Бизнес-Баня Стрельникова ~450+, см. [[evolving/industry-trends/ru-smb-mentor-community-market-2026]]). Подтверждает позиционирование «крупнейший бизнес-клуб РФ» на уровне порядка величины `[conf:medium, src:2026-05-15]`.
2. **Клуб трекает engagement, а не выручку.** Публичная панель метрик — это events / peer-help / благодарности / прирост базы, ни одного revenue/pricing числа. Это **намеренный proof-of-vitality нарратив** для membership-продукта (доказываем «клуб живой», а не «клуб богатый»). См. content-формат в [[evolving/content-trends/community-monthly-recap-digest-format-2026]].
3. **Высокая event-плотность (90/мес)** — главный operational moat: воспроизвести 3 мероприятия в день требует зрелой оргмашины. Это barrier для emerging-конкурентов категории `[conf:medium, src:2026-05-15]`.

## Использование для GRO

- **Benchmark engagement-KPI для community-продукта.** Если GRO когда-либо запустит membership/community-слой (см. monetization paths в [[evolving/industry-trends/marketplace-community-convergence-2026]]), эти 4 KPI (прирост базы, плотность событий, peer-help resolution, peer reciprocity) — готовый набор для собственной proof-of-vitality панели.
- **Реалистичный порядок величины.** «1231 платящий резидент» — это потолок зрелого RU-бизнес-клуба после ~9 лет работы. Полезно для калибровки ожиданий по размеру любого community-сегмента в РФ.
- **Не competitor по продукту**, но benchmark по community-mechanics. GRO — self-serve тренажёр, не клуб; цифры используем как референс, не как конкурентную мишень.

## Contradictions

Нет — первый numeric-ingest метрик «Атланты». Прошлые ingest'ы канала (фев–май 2026) давали только качественные сигналы и один cross-promo benchmark (см. [[evolving-strict/campaign-metrics/cross-promo-speaker-swap-benchmark-2026]]). По мере поступления новых месячных recap'ов сравнивать динамику и при необходимости делать supersession.

## Что нужно для повышения confidence

- ≥2 независимых месячных recap'а подряд для оценки динамики прироста и стабильности event-throughput.
- Внешняя TG-аналитика канала @community_tech (subscriber count, reach) для триангуляции «1231».
- Любой публичный pricing-сигнал, чтобы оценить ARPU/выручку (сейчас отсутствует).

## Связанные страницы
- [[sources/2026-05-19-tg-community-tech-voronin-april-recap-991]] — источник
- [[evolving/competitor-positioning/atlanty-business-club-positioning-2026]] — competitor-профиль клуба
- [[evolving/industry-trends/ru-smb-mentor-community-market-2026]] — категория RU-paid-peer-community
- [[evolving/content-trends/community-monthly-recap-digest-format-2026]] — content-формат, в котором эти метрики опубликованы
- [[evolving-strict/campaign-metrics/cross-promo-speaker-swap-benchmark-2026]] — другой numeric benchmark того же канала
- [[canon/marketing-frameworks/voronin-preventive-social-capital]] — framework Воронина о социальном капитале
- [[volatile/weekly-digest/voronin-community-tech-feb-apr-2026]] — сводный дайджест канала
