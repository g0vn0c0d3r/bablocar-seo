# bablocar-seo

Главная база знаний SEO-проекта Bablocar.

README нужен как короткий навигатор по проекту и верхнеуровневый стратегический слой: что уже решено, где лежат документы, на каком этапе roadmap мы находимся, какие принципы нельзя потерять при дальнейшей работе.

Детальные аудиты, таблицы, брифы, стратегии и будущие ТЗ живут в отдельных файлах. README не заменяет их, а связывает между собой.

## Базовые правила

- Проект начинается с нуля.
- Рабочая папка: `/Users/mikhail/Projects/bablocar-seo`.
- Старые файлы, старая семантика и старые вводные не используются без отдельного подтверждения.
- Не использовать `/Users/mikhail/Documents/Займы`.
- В Git храним управляемые документы и код.
- Сырые CSV, Excel, PDF, скриншоты и тяжелые экспорты не коммитим без отдельного решения.
- `README.md` должен оставаться актуальной картой проекта и фиксировать важные стратегические решения.

## Текущий статус

Собраны и зафиксированы:

- продуктовая база Bablocar;
- партнерские условия и безопасные формулировки;
- конкурентный блок;
- общий вывод по конкурентам;
- очищенная база семантики;
- рабочая методология programmatic geo strategy.

Текущий рабочий этап: SEO-стратегия и разметка семантики под programmatic geo matrix.

Следующий логичный шаг: разложить `clean_semantic.csv` на `canonical_intents`, `intent_aliases`, `modifiers`, `cities`, `applicability_rules` и `generation_rules`.

## Roadmap

| Этап | Статус | Результат / артефакт |
| --- | --- | --- |
| 1. Продуктовая база | Готово | `product/product_brief.md`, `product/bablocar_product_description.md` |
| 2. Партнеры / ограничения / безопасные формулировки | Готово | `partners/partner_conditions.md`, `partners/safe_claims.md` |
| 3. Конкуренты и рынок | Готово | `competitors/analysis_plan.md`, `competitors/technical_sitemap_audit.md`, `competitors/audits/`, `competitors/findings.md` |
| 4. Сбор семантики | Готово как локальный рабочий массив | `semantic/raw_csv/`, `semantic/combined_raw.csv` |
| 5. Обработка семантики | Готово как очищенная база | `semantic/clean_semantic.csv`, `semantic/strict_trash.csv`, `semantic/semantic_review.xlsx` |
| 6. SEO-стратегия | В работе | `seo_strategy/programmatic_geo_strategy.md`; далее нужны справочники и матрица |
| 7. Структура сайта | Не начато | Будет после стратегии и матрицы |
| 8. Шаблоны страниц | Не начато | Будет после структуры |
| 9. ТЗ на страницы | Не начато | Будет после шаблонов |
| 10. Производство и запуск | Не начато | Будет после ТЗ и контроля качества |

Полная дорожная карта: `roadmap.md`.

## Ключевые решения

README фиксирует только решения уровня управления проектом. Детальные продуктовые факты, ограничения, формулировки, SEO-правила и будущие шаблоны страниц хранятся в профильных документах.

На текущем этапе зафиксировано:

- проект ведется как новый SEO-проект без старых вводных;
- основной рабочий этап сейчас — `SEO-стратегия`;
- структура roadmap состоит из 10 этапов, без отдельного этапа предварительных гипотез;
- SEO-стратегия строится через programmatic geo matrix;
- очищенная семантика является входом для справочников, а не готовой картой сайта;
- README не дублирует продуктовый бриф, безопасные формулировки и стратегию страниц.

## Рабочая логика запуска

Ближайшая последовательность:

```text
clean_semantic.csv
-> canonical_intents
-> intent_aliases
-> modifiers
-> cities
-> applicability_rules
-> generation_rules
-> programmatic geo matrix
-> site structure
-> page templates
-> page briefs
```

Главный принцип текущего этапа:

```text
сначала справочники и правила
-> потом матрица
-> потом структура сайта
-> потом шаблоны и ТЗ
```

Детальная методология этапа лежит в `seo_strategy/programmatic_geo_strategy.md`.

## Семантика

Текущие локальные артефакты:

- `semantic/raw_csv/` — сырые CSV-выгрузки по первичным группам;
- `semantic/combined_raw.csv` — объединенная сырая база;
- `semantic/clean_semantic.csv` — очищенная рабочая база;
- `semantic/strict_trash.csv` — удаленные нецелевые запросы с причиной;
- `semantic/semantic_review.xlsx` — локальная таблица для просмотра clean-базы.

Текущее состояние:

- `17 516` сырых строк;
- `14 920` уникальных запросов после точного дедупа;
- `6 480` строк в `clean_semantic.csv`;
- `8 440` строк в `strict_trash.csv`;
- `0` строк со статусом `needs_check`;
- `135` строк со статусом `risky`.

Семантика готова как очищенная база, но еще не как финальное ядро под структуру сайта. Следующий шаг — разметка по методологии `seo_strategy/programmatic_geo_strategy.md` и сбор справочников для programmatic geo matrix.

## Документы проекта

### Главные документы

- `roadmap.md` — дорожная карта проекта.
- `product/product_brief.md` — продуктовая база Bablocar.
- `partners/safe_claims.md` — безопасные формулировки.
- `partners/partner_conditions.md` — агрегированные условия партнеров.
- `competitors/findings.md` — общий вывод по конкурентам.
- `seo_strategy/programmatic_geo_strategy.md` — методология programmatic geo strategy.

### Конкуренты

- `competitors/analysis_plan.md` — план конкурентной аналитики.
- `competitors/technical_sitemap_audit.md` — технический срез конкурентов.
- `competitors/audits/` — детальные аудиты отдельных конкурентов.

Текущие аудиты:

- `competitors/audits/lioncredit_pts_audit.md`;
- `competitors/audits/creddy_pts_audit.md`;
- `competitors/audits/carmoney_pts_audit.md`;
- `competitors/audits/cashmotor_pts_audit.md`;
- `competitors/audits/cashdrive_pts_audit.md`;
- `competitors/audits/zalog24h_pts_audit.md`;
- `competitors/audits/autolombardn1_pts_audit.md`;
- `competitors/audits/autolombard_moskva_pts_audit.md`;
- `competitors/audits/vashinvestor_pts_audit.md`;
- `competitors/audits/centrofinans_pts_audit.md`.

### Локальные рабочие артефакты

- `semantic/` — локальная семантика и Excel-обзор, ignored в Git.
- `page_prototypes/` — локальные скриншоты / выгрузки прототипа генератора, ignored в Git.

## Следующий рабочий шаг

1. Разметить `semantic/clean_semantic.csv` по методологии из `seo_strategy/programmatic_geo_strategy.md`.
2. Собрать справочники: `canonical_intents`, `intent_aliases`, `modifiers`, `cities`, `applicability_rules`, `generation_rules`.
3. Отдельно разобрать `risky`-формулировки через `partners/safe_claims.md`.
4. Сформировать programmatic geo matrix: `city x canonical_intent x allowed_modifier`.
5. После этого переходить к проектированию структуры сайта и шаблонов страниц.
