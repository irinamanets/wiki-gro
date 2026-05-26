---
id: mkt:volatile-strict/industry-news/ai-cyber-0day-wave-may-2026
title: "AI cyber-security 0-day волна — Google GTIG / MS MDASH / UK AISI / ExploitBench (май 2026)"
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [ai, cybersecurity, 0-day, vulnerability-research, google, microsoft, uk-aisi, anthropic, claude-mythos]
confidence: high
stale: false
created: 2026-05-26
updated: 2026-05-26
sources: [sources/2026-05-26-tg-boris-again-may-19-24-2026.md]
namespace: mkt
---

# AI cyber-security 0-day волна — Google GTIG / MS MDASH / UK AISI / ExploitBench (май 2026)

**Дата событий:** ~2026-05-11 .. 2026-05-15 (попало в weekly digest 17 мая) `[conf:high, src:2026-05-17]`. Зафиксировано в [[sources/2026-05-26-tg-boris-again-may-19-24-2026|@boris_again, пост 3916]].

## Что произошло

В одну неделю — **четыре независимых события** про AI и cybersecurity, **все на стороне offence**:

### 1. Google GTIG: первая реальная AI 0-day-атака в проде

[Google Threat Intelligence Group](https://cloud.google.com/blog/topics/threat-intelligence/ai-vulnerability-exploitation-initial-access) **зафиксировал первый случай крупной AI-driven 0-day-атаки** в продакшен-окружении `[conf:high, src:2026-05-17]`. То есть это **не симуляция, не red-team тест, а реальный observed attack** с использованием LLM для эксплуатации zero-day уязвимости.

**Значение:** **«первая бабочка»** будущего рынка. До мая 2026 разговоры про AI-cyber-offence были theoretical / lab-controlled. GTIG-фиксация = переход в **production-observed regime**. Это **поворотная точка**: с этого момента defensive вендоры (Microsoft, CrowdStrike, Palo Alto) могут продавать «AI-augmented attack protection» как distinct product.

### 2. Microsoft MDASH: 100+ агентов нашли «очередную кучу» критических уязвимостей

[Microsoft MDASH](https://www.microsoft.com/en-us/security/blog/2026/05/12/defense-at-ai-speed-microsofts-new-multi-model-agentic-security-system-tops-leading-industry-benchmark/) — **multi-model agentic security system** из **100+ агентов на разных моделях**, который найдёт **«очередную кучу критических уязвимостей первого дня»** `[conf:high, src:2026-05-12]`.

**Значение:** **первый production-scale multi-agent system** в cybersecurity. До MDASH такие системы существовали либо как research-papers (AutoGen, MetaGPT, CAMEL), либо как small-team experiments. **100+ агентов на разных моделях** = первый случай, когда multi-LLM-ensemble используется в проде с конкретным метрикованным outcome (найдены критические уязвимости).

Это также **архитектурный choice**: разные модели для разных под-задач, не «один большой агент на всё». Параллель с тем, как Anthropic Glasswing Coalition использует Claude Mythos в коллаборации с другими вендорами.

### 3. UK AISI «Cooling Tower»: Claude Mythos прошёл ICS-симулятор в 3 из 10

[UK AI Safety Institute](https://www.aisi.gov.uk/blog/our-evaluation-of-claude-mythos-previews-cyber-capabilities) выпустил отчёт **«Cooling Tower»**: Claude Mythos Preview — **первая модель**, которая смогла пройти симулятор атаки на промышленную систему управления (ICS, industrial control system) — в **3 из 10 попыток** `[conf:medium, src:2026-05-15]`.

**Значение:** **ICS = критическая инфраструктура** (электросети, водоснабжение, нефтегаз). До этого модели не справлялись с такими сценариями вообще. 3/10 — это **низкая success rate**, но **больше нуля** = qualitative threshold. См. также [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]] про более ранний report.

### 4. ExploitBench: Mythos 18/41, остальные — 0

[ExploitBench](https://arxiv.org/abs/2605.14153): на 41 уязвимости Claude Mythos Preview **довёл до рабочего эксплойта 18**, **остальные модели — ноль** `[conf:medium, src:2026-05-15]`.

**Значение:** Mythos **категорически отличается от всех остальных публичных моделей** на задаче «найти уязвимость → довести до работающего эксплойта». Это **новая ось capability gap'а** — не «качество ответа», не «agentic horizon», а **«доведение security-research до exploit-stage»**.

## Что значит для рынка

### 1. AI cyber-security становится distinct category (не подмножеством AI safety)

До мая 2026 AI cyber-security был размыт между:
- AI safety (alignment, model-deceit)
- Traditional cybersecurity (firewall, SIEM)
- Vulnerability research (CVE-database, bug bounties)

После этой недели **AI-cyber становится своей категорией** с конкретными метриками (ExploitBench), своими benchmarks (ICS-симулятор UK AISI), своими product-launches (MDASH). Все три vendors (Google / Microsoft / Anthropic + UK government) синхронно подтверждают это позиционирование.

### 2. «Defence-at-AI-speed» как product category

Microsoft в названии анонса MDASH использует **«Defense at AI Speed»**. Это **готовый маркетинговый фреймворк**: если атаки теперь делают LLM-агенты (Google GTIG), то и защита должна работать **с такой же скоростью** — то есть тоже LLM-агенты. Это **продуктовая категория, которая родилась в эту неделю**.

### 3. Anthropic Mythos укрепляет cybersecurity-niche

Из четырёх событий **два касаются Mythos** (UK AISI, ExploitBench), и одно — Glasswing-коалиция (где Mythos — основной модель). То есть Anthropic **последовательно строит cybersecurity-positioning** через Mythos, не через Claude (см. [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]]). К концу мая Mythos стал **de-facto «security frontier model»**.

### 4. AI-cyber как новый контент-нарратив

Для GRO как контент-сервиса появляется **новая отдельная категория тематик**:
- AI-augmented attacks как реальный threat
- Defensive product-category «AI speed defense»
- Mythos vs Claude как security-vs-general split

## Почему это важно для GRO

1. **Готовый content-cluster про AI-cyber** для блога. Темы: «AI 0-day стала реальностью», «Microsoft MDASH — как 100 агентов конкурируют с хакерами», «Anthropic строит две модели — Claude для дружелюбия, Mythos для войны». Это **high-engagement, low-competition** тематика для tech-аудитории.
2. **Vendor positioning hook**: «безопасность как новая ось AI-конкуренции». Это можно встроить в любую дискуссию о выборе AI-стека для бизнеса — теперь это не только цена / качество / latency, но и **security-track record вендора**.
3. **Связь с регуляторами**: UK AISI, EU AI Act, US Executive Orders — все это **legal infrastructure**, которая будет требовать audit AI-vendor'ов на security. GRO как клиент таких вендоров косвенно затрагивается.

## Связанные страницы

- [[sources/2026-05-26-tg-boris-again-may-19-24-2026]] — первоисточник (пост 3916)
- [[volatile-strict/industry-news/anthropic-claude-mythos-glasswing-2026]] — родственный нарратив про Mythos и Glasswing (обновляется в этом ingest'е с production attestation update'ом)
- [[evolving/industry-trends/ai-corporate-race-mar-may-2026]] — общий нарратив гонки
- [[evolving/industry-trends/agent-first-world-openclaw-2026]] — multi-agent как architectural-pattern (MDASH — пример)
- [[evolving/content-trends/ai-tool-comparison-reaction-gate-format]] — готовый pattern для «Mythos vs Claude» сравнительного контента
