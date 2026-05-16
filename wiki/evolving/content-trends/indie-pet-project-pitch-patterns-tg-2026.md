---
id: mkt:evolving/content-trends/indie-pet-project-pitch-patterns-tg-2026
title: Анатомия indie-pet-project self-pitch'а в Telegram 2026 — корпус 24 submission'ов в куратор-канале @boris_again
type: page
subtype: trend
layer: evolving
theme: content-trends
tags: [content, telegram, founder-voice, indie, pet-projects, self-pitch, content-format, awareness, ai-tooling]
confidence: medium
stale: false
created: 2026-05-14
updated: 2026-05-14
sources: [sources/2026-05-14-tg-boris-again-may-2026.md]
namespace: mkt
---

# Анатомия indie pet-project self-pitch'а в Telegram 2026

Reusable content-паттерн: как individual developers / индивидуальные фаундеры self-pitch'ат свои **pet-проекты** в чужом авторском Telegram-канале, когда канал-куратор открывает submission-окно. Корпус собран на одной неделе (2026-05-09…2026-05-13), когда [Борис Цейтлин @boris_again](https://t.me/boris_again) объявил [«неделю пет-проектов»](https://t.me/boris_again/3871) и опубликовал **24 reader-submitted self-pitches** с минимальной редакторской правкой. Полный source-дамп: [[sources/2026-05-14-tg-boris-again-may-2026]].

`confidence: medium` — корпус N=24, **одна неделя в одном канале**, обобщение требует валидации на других curator-каналах (Табунов [@your_pet_project](https://t.me/your_pet_project) — параллельный РУ-аналог, но там более редакторский формат, см. [[evolving/content-trends/your-pet-project-channel-hooks]]). Hook'и совместимы с founder-voice tone из [[evolving/content-trends/contrarian-framing-expert-telegram]] и нарративом [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]].

## Краткий тезис

В мае 2026 в русскоязычном AI/dev Telegram-segment'е сложилась **готовая микро-форма**: 80–250-словный self-pitch индивидуального pet-project'а, который один человек шлёт в куратор-канал, а куратор публикует «как есть». **Эта форма — не Product Hunt-launch (длинный) и не Show HN-комментарий (минимальный), а нечто среднее: native-Telegram-post с founder-voice'ом**. Корпус 24-х submission'ов даёт нам:

- **Стабильную скелетную структуру** (см. ниже) — 5–6 элементов в фиксированном порядке.
- **Тонкие tone-сигналы** (self-deprecation, личная боль-origin, отказ от маркетинговых клише).
- **Sub-clusters по категориям проектов** (AI-tooling, B2B-utilities, gamified consumer, dev-infra, joke/concept).

Эта микро-форма — **готовый template** для GRO content-team, когда нужно либо: (a) показать сегменту «фрилансеры / предприниматели» «вот как соло-фаундеры рассказывают о своих продуктах сейчас», (b) cherry-pick конкретные pitch'и в собственные посты как иллюстрации [[evolving/industry-trends/ai-solopreneurship-window-2026-2029|тренда соло-пренерства]], или (c) воссоздать тон при анонсе собственного pet-проекта в GRO-канале.

## Скелетная структура self-pitch'а (стабильная)

Из 24 проанализированных submission'ов **20 (83%)** содержат большинство из следующих 6 элементов в близком к этому порядку:

### 1. Personal-pain origin story / introduction

**Сигнал:** «Я разработчик. Делал жене интерактивный подарок на день рождения…», «Когда работал в Толоке, узнал неожиданную вещь…», «Я, когда в Швейцарии работу искал, столкнулся с проблемами…».

**Функция:** легитимирует автора как **builder, у которого был real problem**, а не как маркетолога. Это RU-эквивалент английского «I built X because Y» pattern из IndieHackers/HackerNews. Обычно 1–3 предложения. Цель — не self-promo, а **установить контекст use-case'а**.

**Примеры из корпуса:**
- 3875 Uspamin: «Я разработчик. Делал жене интерактивный подарок на день рождения, не открытку.»
- 3881 Job Seek: «Я, когда в Швейцарии работу искал, столкнулся с проблемами…»
- 3897 AnastasiyaW: «Я довольно плотно работаю с Клодом, трачу по три недельных лимита в неделю и прыгаю между аккаунтами. Под это завела систему быстрой работы.»
- 3882 GetBestJobBot: «Меня очень утомило внимательно читать описание вакансий перед откликом чтобы мне на них ответили только пять процентов, поэтому решил делать наоборот.»
- 3865 axor-core: «Привет всем, я Дима, AI инженер, или как там это теперь называется.»

**GRO-применение:** прямой template для постов про реальных пользователей продукта — origin story «я бывший X, столкнулся с проблемой Y, GRO помог сделать Z». Хорошо для сегмента «фрилансеры» и «карьеристы» в смене позиционирования.

### 2. Название продукта + one-line value-prop

**Сигнал:** «**Stape** — сервис для выплат удалённым исполнителям в 242 локациях»; «**PanicMode**: демон для Linux-серверов, для защиты от тихого падения»; «**Plotva**, это забавный разговорный чат-бот, который не похож на типичного ассистента а имеет свой характер».

**Функция:** ровно то, что пользователь должен понять за **2 секунды чтения**. Стиль — описательный, **не маркетинговый** (не «революционный AI-помощник», а «забавный разговорный чат-бот»).

**Anti-pattern:** в корпусе **нет** ни одного pitch'а с буззвордами «AI-powered», «next-generation», «revolutionary». Tone обычно занижен — «забавный», «небольшой», «маленький», «бесплатный», «пет-проект».

### 3. 2–5 пунктов «что внутри» / killer-фичи в булет-листе

**Сигнал:** Stape: «от онбординга до выплаты — 60 секунд; юридический риск на них, не на вас; подрядчики получают на карту, счёт или USDT без комиссии». axor-core: «пользовательский интент классифицируется и выбирается полиси для этого типа задач; в зависимости от полиси применяется сжатие контекста и формируется allow list тулов; разрешается или запрещается спавнить саб агентов…».

**Функция:** оператионная conviction — **что конкретно делает продукт**. Не «улучшит вашу жизнь», а «60 секунд от онбординга до выплаты». Удобно для скана.

**Длина:** 2–5 буллетов оптимум, в корпусе встречаются и одно-предложенческие версии (Plotva 3880, otter_sticker_bot 3893) — это работает только если concept self-explanatory.

### 4. Tech-stack / архитектура (опционально, signal в dev-аудитории)

**Сигнал:** Uspamin: «Стек: Next.js, Supabase, Cloudflare, Vercel. Локализация на 19 языков через DeepL с автоматическим конвейером»; Pinefall: «использую такие нейронки, как Tripo3D и Codex»; PanicMode: «Легкий Rust потребляет в обычном режиме меньше процента CPU, и меньше 40 мб от оперативки. Бинарник ~9МБ».

**Функция:** **сигнал «я разработчик, не маркетолог»** для tech-audience. Также — **доказательство, что pet-project реален** (а не лендинг-обещание). В дайджестах общего контента этот элемент **отсутствовал бы**, но в curator-канале tech-developer'а tech-stack legitimises submission.

**GRO-применение:** В контенте для предпринимателей tech-stack обычно избыточен, но **в постах для «фрилансеров»** (часто = разработчики) — релевантен.

### 5. CTA — ссылка на GitHub/демо/бота/лендинг

**Сигнал:** «https://github.com/Bucha11/axor-core», «https://www.uspamin.org», «@hotColdGameBot», «https://thestape.com/demo?utm_source=telegram&utm_medium=boris-again&utm_campaign=06052026» (для paid ad — с UTM).

**Функция:** дистрибуция. **Обычно одна ссылка**, иногда две (GitHub + блог-пост, демо + статья на Хабре).

**Сравнение paid vs. organic:** paid-ad (3864 Stape) имеет **UTM в ссылке** и **маркировку рекламы**: «Реклама. ООО ГЕЙМИНГ ИНТЕРТЕЙМЕНТ ФЗЕ ИНН 9909668088 erid:2VtzqwQHPvP» (см. [[canon-strict/legal-claims/ad-marking-russia-2026]]). Все остальные **organic submissions** идут без маркировки.

### 6. Self-deprecating closer / call for feedback (опционально, но усиливает)

**Сигнал:** «Буду рад обратной связи, особенно технической» (Uspamin); «Если кто найдёт баги буду рад посмотреть) ну и нагрузку накинуть тоже будет прикольно)» (Image2PDFRocketBot); «жду ваши предложения, пожелания и теплые слова» (axor-core); «Поддержите в твитере а то я устал жить без большого твитера» (AlexWortega 3869); «Вот, вдруг звезды сойдутся!)» (SadSabrina 3900).

**Функция:** **антитеза маркетинговому CTA**. Не «зарегистрируйтесь сейчас», а «потыкайте, расскажите что не так». **Tone-инвертирование**: подавление продажного импульса работает как трастовый сигнал (если автор не давит — продукт сам себя продаёт или вообще не продаётся, и обе ситуации легитимны).

**Это — главный sub-pattern, отличающий organic-pitch от paid-ad.** В paid-ad (3864 Stape) closer звучит: «Если у вас похожая боль — вот ссылка на консультацию» — explicit-sales. В organic pitch — никогда так прямо.

## Sub-clusters по категориям проектов

Корпус N=24 разбивается на 5 устойчивых под-категорий:

### Cluster A: AI/Dev-tooling (8 submissions = 33%)

`axor-core` (3865, agent governance), `paperreview.ai claude-code skill` (3869), `ULTRAPACK` (Цейтлин-own, 3851 — был в предыдущем дампе), `nitpicker` (3891), `mnemonik.xyz` (3888, MCP context reuse), `claude-code-config + happyin.space` (3897 AnastasiyaW), `Borealis audio LLM tutorial` (3887), `metal-faster-whisper / CT Transcriber` (3894).

**Tone:** dev-to-dev. Минимум маркетинга, максимум tech-stack. **Builder для builder'а**.

**GRO-применение:** этот cluster — **сильный сигнал, что AI-tooling сегмент в RU = «builder'ы строят для других builder'ов»**, не для конечного пользователя. GRO как **end-user-направленный продукт** (для целеустремлённых людей, не для разработчиков) **должен это знать**: AI-tooling Telegram-сегмент не равен «общая русская AI-аудитория». Когда GRO упоминается в этих каналах — она там как **exotic** (направлена на не-developer'ов), а не как «один из своих».

### Cluster B: B2B-utilities / productivity (5 submissions = 21%)

`Stape` (3864, paid, B2B международные выплаты), `PanicMode` (3872, Linux server reliability), `Job Seek / jseek.co` (3881, job aggregator), `GetBestJobBot` (3882, HH-автокликер), `Image2PDFRocketBot` (3883, image→PDF).

**Tone:** problem-solution. Personal pain → product. Простой утилитарный язык, конкретные операционные числа («$50 за транзакцию», «60 секунд от онбординга», «<1% CPU, <40MB RAM»).

**Особенность:** этот cluster имеет **наибольшее пересечение с marketing-стилем**. Pitch'и phr из этого cluster'а **близки** к традиционному B2B-копирайту — но без буззвордов.

### Cluster C: Gamified consumer (5 submissions = 21%)

`Uspamin` (3875, интерактивные подарки), `corovans` (3873, игра «грабить корованы»), `hotColdGameBot` (3877, словарная игра), `wishapp` (3878, вишлист), `Pinefall` (3898, horror-game нуар).

**Tone:** playful, often с personal-emotion-аркой (Uspamin — про жену, Pinefall — про портье в 60-х в Америке). Tech-stack упоминается **гордо** (Next.js + Supabase + Cloudflare + Vercel + DeepL 19 языков) — это **builder-signal**, который привлекает других builder'ов даже в consumer-категории.

**Anti-pattern:** **никаких** упоминаний «accelerator», «funding», «valuation» — все эти pitch'и — **deliberately not-startup**. Это **bootstrap-vs-startup** divide (см. [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]]).

### Cluster D: Dev-infra / niche utilities (4 submissions = 17%)

`Ushqyn` (3874, $25 FPGA MLP), `getmeridian.org` (3879, VPN deploy), `g6chess.com` (3884, шахматный анализ через URL-префикс), `otter_sticker_bot` (3893, sticker-management).

**Tone:** «вот специфичная задача, я её решил для себя, может кому пригодится». **Низкий-самопиар, низкий-маркетинг**. Готовы быть нишевыми.

### Cluster E: Joke / concept / non-products (2 submissions = 8%)

`respect-ai.com` (3889, блокчейн-запись «респекта ИИ», явно joke), `fittrace_bot` (3885, voice workout logging — minimal pitch). Тут уже **граничные случаи**, которые автор подаёт «для записи, не претензия на market».

## Tone-сигналы и микро-приёмы

Помимо скелета и кластеров, в корпусе устойчиво наблюдаются **micro-tone-сигналы**, отличающие successful indie-pitch от рекламы:

### Self-deprecation как trust-signal

- «маленький сайт» (Uspamin)
- «небольшой проект» (otter_sticker_bot)
- «бесплатный пакет», «бесплатно по умолчанию» (Uspamin, SadSabrina)
- «никакой рекламы (ненавижу её)» (Uspamin)
- «нет явного процесса, всё в бете» (Job Seek)
- «делал для себя, но вдруг кому-то ещё будет полезным» (fittrace_bot)
- «PS био (и даже хемо!) информатикой тоже все еще занимаюсь» (3896 — emotional aside, не маркетинг)

**Маркетинговая логика:** само-занижение **парадоксально работает как trust-signal**, потому что **противоположно ожидаемому маркетинговому tone**. Anti-pattern (что НЕ работает): «революционная AI-платформа», «next-generation», «100% guaranteed». Эти фразы в корпусе **отсутствуют** ровно потому, что они = красный флаг скама.

### Технический честный self-disclosure

- «UI и некоторые вещи ещё допиливаю» (fittrace_bot)
- «если не сможет (редко), сохранит только ссылку» (wishapp — honest о fallback)
- «в эмоциональных формулировках на каких-то языках возможны неточности. Если заметите неуклюжий перевод на родном языке, напишите, поправлю» (Uspamin)
- «Кореляцию я конечно же не посчитал, но пока совпало» (paperreview.ai 3869)

**Маркетинговая логика:** прямое признание ограничений работает **сильнее**, чем гарантии. **Это hooks для GRO**, например: «GRO не сделает за вас работу. GRO заставит вас увидеть, что вы её **не делаете**.» — anti-promise-hook.

### Принципиальный отказ от рекламы / accounts / paywall'ов

- «никакой рекламы, никаких аккаунтов, бесплатно по умолчанию» (Uspamin)
- «Опционально можно один раз заплатить десять фунтов, чтобы подарок остался навсегда, но большинству это не нужно» (Uspamin) — **explicit отказ от subscription-greed**
- «бесплатный» курс у SadSabrina (3900)

**Это — крайне сильный builder-tone для consumer-cluster'а.** Он **резонирует с GRO-positioning**, где free-trial (14 дней) — central trust-signal, но **не должен путаться** с anti-paywall-нарративом — у GRO есть подписочная модель, и нельзя пытаться скопировать «бесплатность» Uspamin'а как USP. **Используется для tone, не для бизнес-модели.**

### Open-source / GitHub-first дистрибуция

В Cluster A (AI/Dev-tooling) **8 из 8** проектов имеют **GitHub-репо как главную CTA-ссылку**. В Cluster D (niche-utilities) — 2 из 4 (Ushqyn, panicmode-like). В Cluster B (B2B-utilities) — 1 из 5 (jseek.co имеет GitHub `colophon-group/jobseek`, остальные — лендинги или Telegram-боты). В Cluster C (consumer) — 0 из 5 (всё закрытое).

**Сигнал:** open-source = **default дистрибуция для AI/dev-tooling**, **не default для B2B-utilities и consumer**. Это **граница category-norm'ы**: если GRO как продукт хочет позиционироваться в AI-tooling-сегменте, отсутствие GitHub-репо станет structural-mismatch'ем. Если как consumer-продукт — отсутствие GitHub нормально и ожидаемо.

## Анатомия paid vs. organic — формальное сравнение

Сравним **3864 Stape (paid)** с **3865 axor-core (organic)** и **3875 Uspamin (organic)**:

| Элемент | Stape (paid) | axor-core (organic) | Uspamin (organic) |
|---|---|---|---|
| Personal-pain origin | Есть: «Когда работал в Толоке…» | Есть: «Привет всем, я Дима, AI инженер…» | Есть: «Делал жене интерактивный подарок…» |
| Название + value-prop | «Stape — сервис для выплат удалённым исполнителям в 242 локациях» | «не очередной клон лангчейна, мета враппер для агентов» | «Uspamin. Бесплатный сайт, где можно собрать интерактивный подарок» |
| Bullet-list фич | 3 буллета (онбординг 60с / юридический риск / без комиссии) | 4 буллета (классификация полиси / сжатие контекста / спавн саб-агентов / логи) | 5+ буллетов (форматы внутри: викторина, адвент, мемори, фотопазл…) |
| Tech-stack | Нет (B2B-utility, не нужен) | Implicit (LangChain, Claude SDK references) | **Explicit**: Next.js, Supabase, Cloudflare, Vercel, DeepL |
| CTA | UTM-link, **explicit sales** «вот ссылка на консультацию» | GitHub-link, «жду ваши предложения, пожелания и теплые слова» | URL + «Буду рад обратной связи, особенно технической» |
| Trust-signals | 600+ компаний, 10K+ подрядчиков, partners Sumsub/DocuSign/Microsoft | 1 star / 0 forks (на момент скриншота) — **никаких** | Платная опция €10 «чтобы подарок остался навсегда» |
| Маркировка | **«Реклама. ООО ГЕЙМИНГ ИНТЕРТЕЙМЕНТ ФЗЕ ИНН 9909668088 erid:2VtzqwQHPvP»** | Нет | Нет |
| Self-deprecation | Нет — confident-tone | Имплицитно: «не очередной клон» — антитеза, не самозанижение | Есть: «маленький сайт», «никакой рекламы (ненавижу её)» |
| Length | ~180 слов | ~190 слов | ~280 слов |

**Главный delta:** **organic pitches содержат self-deprecation + technical self-disclosure + отказ от закрывающей продажи**, paid ad — нет. Это **structural distinction**, которую можно использовать как **detection-rule** для GRO content team: если pitch выглядит organic, но содержит explicit-sales CTA — это либо плохо замаскированная реклама, либо начинающий automator-bot. Trust-signal: длинный organic-pitch без CTA.

## Готовый template для GRO content

Когда GRO хочет показать в своих каналах конкретный соло-фаундер-built продукт (либо для иллюстрации тренда, либо как case study), готовый template из этого корпуса:

```
{Personal-pain origin, 1-3 sentence}.

{Имя продукта + one-line value-prop, 1 sentence — описательно, без буззвордов}.

Что внутри:
• {Feature 1, operationally concrete}
• {Feature 2}
• {Feature 3}

{Optional: 1 sentence про tech-stack или architecture}

{CTA — ссылка}

{Optional: self-deprecating closer / call for feedback}
```

**Длина:** 80–250 слов. **Tone:** builder-to-builder, без маркетинговых превосходных степеней. **Trust-signal:** одно реальное ограничение / honest fallback.

**Anti-patterns** (что НЕ использовать):
- Буззворды «революционный», «next-generation», «AI-powered», «100% guaranteed»
- Explicit-sales CTA «зарегистрируйтесь сейчас», «бесплатная консультация» — это paid-ad-маркер, отталкивает builder-аудиторию
- Перечисление крупных партнёров как trust-signal без context'а — это тоже paid-ad-маркер
- Метрики бизнеса (MRR, valuation, fundraising) — это VC-pitch, не indie-pitch

## Связь с другими страницами

### С [[evolving/content-trends/your-pet-project-channel-hooks]]

@your_pet_project Табунова — **параллельный РУ-аналог**, но это **полноценный case-study канал** (длинные посты с деконструкцией). Этот корпус (@boris_again неделя пет-проектов) — **raw submissions без редакторской деконструкции**. Два sources дают нам два уровня:

- **@your_pet_project Табунова** — как curator-эксперт **анализирует** успешные pet-проекты после факта (с фокусом на business-economics, traffic-mentality, unit-economy).
- **@boris_again неделя пет-проектов** — как curator **публикует raw self-pitches** до того, как они стали известными (фокус на tone, structure, technical honesty).

Оба полезны для GRO content, но для **разных стадий воронки**: Табунов-формат сильнее для **consideration** (когда нужна экономическая логика), Цейтлин-формат сильнее для **awareness** (когда нужно показать «вот как это выглядит, ты тоже можешь»).

### С [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]]

24 reader-submitted pet-проектa за одну неделю — **сильное эмпирическое доказательство активности indie-сегмента в RU-AI-вертикали**. Не статистика и не nominal-цифры (как «100K проектов на Lovable в день»), а **24 живых пример'а** разнообразия категорий. Поддерживает нарратив **«окно соло-фаундера открыто»** не количественно, а качественно — показывает, что **разнообразие** проектов (AI-tooling, B2B-utilities, consumer-games, dev-infra) тоже растёт.

### С [[evolving/content-trends/contrarian-framing-expert-telegram]]

Цейтлин **сам** использует контр-нарративную рамку в куратор-постах — например, в 3867 он публично **отказался от интеграции** с брендом, который прислал плагиат как бриф. Это — **editorial discipline-signal**, проявляющийся в рамках кураторской недели. Эту черту можно ловить в любых autor-каналах, но в недели-пет-проектов она резонирует особенно сильно: куратор отказывает плохо подготовленным брендам — следовательно, опубликованные submission'ы прошли его фильтр.

### С [[canon/target-audience/gro-segments]]

Корпус полезен для **трёх сегментов GRO**:

- **Карьеристы:** Cluster B (B2B-utilities) и Cluster D (dev-infra) дают шаблоны, как «разработчик решил свою боль и сделал product». GRO может ссылаться на эти примеры как доказательство, что **навык building'а pet-проекта = карьерный капитал** (резонирует с [[evolving/content-trends/career-audience-hooks-2026|career-audience-hooks-2026]]).
- **Предприниматели:** Cluster A (AI-tooling) и Cluster C (consumer-games) показывают, как **индивидуальные builder'ы становятся первыми продавцами**. Не nominal-numbers, а **template** того, как pitch'нуть свой продукт после launch'а.
- **Фрилансеры:** Cluster D (dev-infra, niche-utilities) — прямо резонирует. **Pet-project как карьерный hack** (см. [[evolving/content-trends/your-pet-project-channel-hooks|hook «Pruefs (доказательства) как карьерный hack»]]).

## Что нужно, чтобы повысить confidence

- **Найти 2+ параллельных curator-канала** в RU с похожим crowdsourced-submission форматом и проверить, повторяется ли структура.
- **Подсчитать engagement на самих pitch-постах** (reactions, comments) — какие cluster'ы / tone-сигналы коррелируют с большим engagement.
- **Проверить дальнейшую судьбу 24 pet-проектов** через 3–6 месяцев — какие выросли, какие умерли, какие повторили pitch в других каналах.

## Связанные страницы

- [[sources/2026-05-14-tg-boris-again-may-2026]] — исходник, дамп 36 постов
- [[evolving/content-trends/your-pet-project-channel-hooks]] — параллельный канал Табунова (более редакторский формат)
- [[evolving/content-trends/telegram-author-channel-patterns]] — общий каталог auto-channel-паттернов, в который добавлен sub-pattern «weekly themed crowdsourced content»
- [[evolving/content-trends/ai-solopreneur-narrative-hooks]] — нарратив соло-пренерства, к которому корпус добавляет 2 новых hooks (anti-LLM-outreach, agent-readable KB)
- [[evolving/industry-trends/ai-solopreneurship-window-2026-2029]] — главный мета-нарратив, который этот корпус emпирически поддерживает
- [[evolving/content-trends/contrarian-framing-expert-telegram]] — структура авторского post'а, в которую куратор-week-формат вписывается
- [[canon/target-audience/gro-segments]] — на каких сегментов GRO разные cluster'ы маппятся
- [[canon/target-audience/ru-ai-telegram-audience-segments]] — «Продвинутый» сегмент (17%), который этот канал представляет
- [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] — все 24 pitch'а — bootstrap, не startup (явный divide)
- [[canon-strict/legal-claims/ad-marking-russia-2026]] — paid-vs-organic distinction поддержан маркировкой `erid:...`
