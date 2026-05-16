---
id: mkt:canon/marketing-frameworks/three-partner-majority-rule-smb
title: "Three-partner simple-majority rule (SMB governance, 33/33/33 equity)"
type: page
subtype: concept
layer: canon
theme: marketing-frameworks
tags: [smb, governance, partnership, decision-making, founder-playbook, equity]
confidence: medium
stale: false
created: 2026-05-06
updated: 2026-05-06
sources: [sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet.md, sources/2026-05-06-yt-biznes-s-nulya-electrobike-prequel-decision-procurement.md]
namespace: mkt
---

# Three-partner simple-majority rule (33/33/33 SMB)

Governance pattern для 3-партнёрного SMB на equity 33/33/33: **«если один против, а двое других за — решение принимается»**. В отличие от классического founder-veto (CEO имеет блок-право в любом решении), здесь **founder может быть переголосован партнёрами**. Pattern зафиксирован в финале электробайк-серии Муратаева ([[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]], раздел «Партнёрский decision-rule»), упомянут в prequel ([[sources/2026-05-06-yt-biznes-s-nulya-electrobike-prequel-decision-procurement]]).

## Цитата founder'а

Когда два партнёра без участия Кирилла (Кирилл / Илья / Андрей по 33/33/33) приняли решение про profit-share механикам:

> «Кстати, это вот с точки зрения партнерского договора, если вам будет интересно. Мы его скоро выкатим. Мы его сейчас доделываем. Но у нас было такое условие, которое мы прямо бы говорили, что если один против, а двое другие за, то решение вступает в силу. Вот. И даже если я был против, а вы были бы за, мы бы это сделали. Да, все верно. Но как будто было бы правильно обсудить все равно. Нет. Возможно, у меня были бы аргументы».

Founder сначала **подтверждает rule**, потом **acknowledged** что emotionally хочется «обсудить всё равно», но **не блокирует** rule.

## Структура

| Параметр | Значение |
|---|---|
| Equity split | 33% / 33% / 33% (трое равных партнёров) |
| Decision threshold | Simple majority (2 из 3) |
| Founder veto | **Отсутствует** (founder тоже одинаково subordinated) |
| Communication norm | Не требуется ALL-hands, но **разумно** проговаривать (founder explicitly says «было бы правильно обсудить») |
| Escape hatch | Не зафиксирован (что делать если партнёры в постоянном 2v1 conflict?) |

## Где работает

**Условия применимости:**

1. **Equal-equity SMB (3 партнёра по 33/33/33)** — необходимое условие. Если 51/30/19 — founder уже имеет implicit majority.
2. **Trust между партнёрами высокий** — founder доверяет, что 2 партнёра не будут systematically оверriding его на operational уровне.
3. **Operational separation of concerns** — каждый партнёр имеет clear domain (Кирилл = маркетинг/контент, Илья = operations, Андрей = B2B-development). Partнёры **не голосуют по чужому домену**.
4. **Speed-of-decision важна** — pattern reduces decision-bottleneck на founder'е.

**Условия НЕприменимости:**

- Founder с majority equity (>50%) — pattern не нужен, founder имеет implicit veto.
- Strict-controlled VC-funded стартап — в венчурных компаниях board-of-directors уже implements voting rules with class structures.
- High-stakes decisions (продажа компании, dilution) — обычно нужен super-majority или unanimous, не simple-majority.

## Сравнение с альтернативными governance-структурами SMB

| Структура | Decision rule | Применимость |
|---|---|---|
| **Founder-veto** | Founder имеет блок на любое решение | Single-founder + invest-партнёры (не equity-equal) |
| **Three-partner majority (33/33/33)** | 2 of 3 → принимается, founder без veto | Этот pattern (Муратаев) |
| **Unanimous-required** | Все согласны, иначе не принято | Family-run SMB, 50/50 партнёры |
| **Founder-CEO + advisory board** | Founder решает, advisors советуют | Solo founder с consult-friends |
| **Rotating chair** | Decision-маker ротируется между партнёрами | Редкость, требует maturity |

## Risks и mitigation

### Risk 1: 2v1 systematic ostracism

Два партнёра systematically блокируют founder'а / другого партнёра.

**Mitigation:** mandate communication norm («было бы правильно обсудить всё равно» — даже без veto-rights). В Муратаевском случае founder этого себя не получил, но **acknowledged** norm.

### Risk 2: Founder уходит из контента / коммитмента

Если founder узнаёт что его постоянно overriding, он эмоционально выходит из проекта (показывает less commitment к public face канала).

**Mitigation:** Founder explicitly verbalizes norm на камеру, что повышает **psychological commitment** партнёров не overriding founder'а unfairly.

### Risk 3: Voting deadlock (1v1v1)

Pattern не explains что делать если каждый из 3 имеет уникальную позицию (А хочет X, Б хочет Y, В хочет Z).

**Mitigation:** не зафиксировано в Муратаевском случае. Возможные пути: (a) откладывать решение и пересматривать; (b) third-party arbiter; (c) предметная декомпозиция X/Y/Z до пересечения.

## Применимость к не-SMB контекстам

Pattern может быть adopted в:

- **Co-founder triо в стартап-стадии** — до VC, когда founders ещё equal-equity. После VC-раунда обычно превышается majority-shareholder structure.
- **Совет директоров с 3-membership** — applied как board-rule.
- **Family-run business с 3 наследниками** — distributing decision-rights поверх equal-share inheritance.
- **Open-source проекты с core-trinity maintainers** — analogous applicable.

## Связь с другими governance-структурами вики

| Page | Связь | Различие |
|---|---|---|
| [[canon/marketing-frameworks/profit-share-service-revenue-smb]] | Тот же эпизод | Decision о profit-share **была сделана** через 1v2 right (Кирилл против — overruled). Pattern in action |
| [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] | Same founder, related ideology | Anti-perfectionism = «не блокируйся на качестве, иди вперёд». 3-partner rule = «не блокируйся на consensus, иди вперёд». Та же operational скорость |
| [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] | Same audience | Tabunov бутстрапер обычно solo-founder. 3-partner = другое equity-структура. Контраст-видение |
| [[canon/marketing-frameworks/b2b-pivot-anchor-customer-smb]] | Same source-серия | Pivot decision **тоже** был simple-majority? Не зафиксировано explicitly, но pattern is consistent |

## Применимость к GRO-content

GRO **не SMB-rental**, но 3-partner founder-trio часто встречается в RU SMB (~30% co-founded SMB по venture-data в Carta-stats). Этот pattern может быть **content-hook** для GRO-блога:

> «Если вы founder в 33/33/33 партнёрстве — какое governance-rule используете? 1 voice = блок? Или simple majority? Pattern Муратаева — second variant. Что вы выбрали?»

Это **identification-prompt** для founder-сегмента ([[canon/target-audience/ru-smb-founder-owner-seller]]).

## Связанные страницы

- [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]] — anchor (rule articulated на камеру)
- [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-prequel-decision-procurement]] — earlier source (33/33/33 equity-структура зафиксирована до запуска)
- [[canon/marketing-frameworks/profit-share-service-revenue-smb]] — соседний pattern, decision о котором был сделан через эту rule
- [[canon/marketing-frameworks/anti-perfectionism-mvp-launch-muratayev]] — operational ideology того же founder'а
- [[canon/target-audience/ru-smb-founder-owner-seller]] — ICP применимости
- [[canon/marketing-frameworks/bootstrap-vs-startup-tabunov]] — соседняя founder-philosophy

## Backlinks

_5 pages link to this one._

- [[canon/marketing-frameworks/multi-generational-family-business-survival]]
- [[canon/marketing-frameworks/profit-share-service-revenue-smb]]
- [[evolving/content-trends/biznes-s-nulya-founder-diy-format-2026]]
- [[index]]
- [[sources/2026-05-06-yt-biznes-s-nulya-electrobike-month1-bilanc-couriers-meet]]
