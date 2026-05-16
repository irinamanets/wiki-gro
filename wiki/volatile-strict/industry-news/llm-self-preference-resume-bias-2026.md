---
id: mkt:volatile-strict/industry-news/llm-self-preference-resume-bias-2026
title: "LLM self-preference bias в HR: резюме на «своей» модели проходит на 20–60% чаще"
type: page
subtype: news
layer: volatile-strict
theme: industry-news
tags: [ai, hr, content, research, bias, llm]
confidence: medium
stale: false
created: 2026-05-05
updated: 2026-05-05
sources: [sources/2026-05-05-tg-ai-newz-apr-may-2026.md]
namespace: mkt
---

# LLM self-preference bias: резюме «робот пишет, робот читает» (май 2026)

## Что зафиксировано

Академический препринт (arxiv.org/abs/2509.00462), процитированный 2 мая 2026 в [[sources/2026-05-05-tg-ai-newz-apr-may-2026|@ai_newz пост 4558]], исследует двусторонний AI-сценарий в HR: **кандидат пишет резюме через LLM, компания скринит резюме через LLM**. Два главных вывода:

1. **Резюме, переписанные LLM, чаще проходят автоматический отбор**, чем семантически идентичные резюме, написанные человеком вручную `[conf:medium, src:2026-05-02]`.
2. **Когда оценщик и автор используют одну и ту же модель, кандидат проходит шортлист на 20–60% чаще** при идентичном содержании `[conf:medium, src:2026-05-02]`. Эффект назван **self-preference bias** — модель-оценщик «узнаёт свой стиль» и предпочитает тексты, похожие на её собственный output.

## Цифры

| Сценарий | Результат |
|---|---|
| Резюме LLM-rewritten vs hand-crafted (тот же кандидат, оценщик-LLM) | LLM-rewritten проходит чаще `[conf:medium, src:2026-05-02]` |
| Совпадение модели автора и оценщика | +20% до +60% к шансам шортлиста vs «mismatched» пары `[conf:medium, src:2026-05-02]` |

## Caveat

- **Препринт, не peer-reviewed.** ArXiv-публикация, цитата через AI-новостной канал — `confidence: medium` уровня вторичного источника, нужно отслеживать peer review до повышения.
- **Методология:** симуляция, не натурное исследование на живом найме. Результаты могут не воспроизводиться в production-HR-системах с custom-fine-tuned моделями.
- **Эффект 20–60%** `[conf:medium, src:2026-05-02]` — диапазон зависит от моделей пары; оригинальная статья даёт детализацию по комбинациям.

## Маркетинговая интерпретация для GRO

### 1. Hook для блог-контента про скрытые искажения AI в найме

Готовая контент-формулировка: *«Раньше люди подстраивали CV под рекрутера, теперь нужно подстраивать под модель-оценщика. Ваше резюме с AI работает не потому, что оно лучше — потому что HR-LLM узнаёт свой диалект».*

Hook'и-расширения:
- «AI-нарциссизм» — модели предпочитают свой output. Применимо не только к HR — к любому workflow «AI генерирует → AI оценивает» (peer review, content moderation, A/B-тестирование креативов через LLM).
- Связка с [[canon/marketing-frameworks/ai-text-markers-checklist|чек-листом 12 маркеров AI-текста]] — мы знаем, что «человеческий читатель» учится отличать AI; новая исследовательская волна утверждает обратный effect — «LLM-читатель» узнаёт «своих».

### 2. Anti-pattern для контента GRO

- **Нельзя писать** «AI-резюме гарантированно проходит» — bias direction зависит от модели-оценщика, и кандидат не контролирует, какая модель используется в HR-системе.
- **Можно писать** «AI-резюме чаще проходит, потому что HR-системы тоже на AI» — это аккуратно, поддерживается данными, и помещает GRO в нарратив «инструмент для new reality of work».

### 3. Связь с broader narrative

Самореферентный AI-loop — параллель с уже зафиксированным трендом:
- [[evolving/industry-trends/candidate-side-ai-services-2026]] — рост рынка AI-инструментов на стороне соискателя
- [[evolving/content-trends/career-audience-hooks-2026]] — career-hook-набор, в который этот сигнал ложится как новый Hook 14
- [[evolving/content-trends/ai-text-detection-landscape-2026]] — обратная сторона: как люди и автоматические детекторы пытаются распознать AI-текст; здесь же — обратный эффект, AI **предпочитает** AI-текст

## TTL

Volatile-strict TTL: 14–90 дней. Чекпоинт: **2026-08** — отследить peer review публикации, появление вторичных подтверждений на других моделях/датасетах. Если эффект подтвердится — повышаем `confidence: high` и переносим в `evolving-strict/market-data` как устойчивый паттерн.

## Связанные страницы

- [[sources/2026-05-05-tg-ai-newz-apr-may-2026]] — первоисточник (вторичная цитата академического препринта)
- [[evolving/industry-trends/candidate-side-ai-services-2026]] — рынок candidate-side AI
- [[evolving/content-trends/career-audience-hooks-2026]] — career-hook-набор для GRO
- [[evolving/content-trends/ai-text-detection-landscape-2026]] — обратная сторона: human-detection AI-текста
- [[canon/marketing-frameworks/ai-text-markers-checklist]] — чек-лист маркеров AI-текста (контраст: люди отличают, LLM «узнаёт своих»)

## Backlinks

_6 pages link to this one._

- [[evolving-strict/market-data/ai-resume-acceptance-rff-poll-2026]]
- [[evolving/content-trends/career-audience-hooks-2026]]
- [[evolving/industry-trends/ai-cheat-interview-pattern-2026]]
- [[index]]
- [[sources/2026-05-05-tg-ai-newz-apr-may-2026]]
- [[volatile/weekly-digest/ai-industry-news-w15-w18-2026]]
