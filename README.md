# bablocar-seo

Короткая карта SEO/pSEO-проекта BabloCar.

Главный принцип: source of truth по опубликованной структуре - sitemap и его локальный снимок, а не ручная визуальная карта. Если нужна визуальная структура, ее быстро пересобираем из `site_structure/live_sitemap_0.xml`.

## Статус

Текущая live-сетка на 23.07.2026:

- 9 городов: Новосибирск, Самара, Казань, Москва, Екатеринбург, Санкт-Петербург, Красноярск, Нижний Новгород, Челябинск;
- 6 базовых интентов;
- 6 текущих модификаторов;
- 387 коммерческих страниц в sitemap;
- 388 коммерческих страниц с главной;
- 7 служебных страниц `/info`.

Формула текущего города:

```text
1 городской хаб + 6 интентов + 6 интентов x 6 модификаторов = 43 страницы
```

Текущий этап: расширение pSEO-сетки. Ближайшая цель - довести матрицу до 9 интентов на 9 городах.

## Текущие сущности

Города:

```text
novosibirsk
samara
kazan
moscow
ekaterinburg
sankt-peterburg
krasnoyarsk
nizhniy-novgorod
chelyabinsk
```

Интенты:

```text
zaim-pod-zalog-pts
kredit-pod-zalog-avto
dengi-pod-zalog-mashiny
zaim-pod-zalog-avto
dengi-pod-zalog-avto
zaim-pod-zalog-mashiny
```

Модификаторы:

```text
online
na-kartu
bez-spravok
bez-podtverzhdeniya-dohoda
s-plohoi-kreditnoi-istoriei
dlya-biznesa
```

## Следующие публикации

По текущему плану:

| Очередь | Публикуем | Slug | Прирост |
| ---: | --- | --- | ---: |
| 1 | Кредит под залог машины | `kredit-pod-zalog-mashiny` | +63 |
| 2 | Кредит под залог ПТС | `kredit-pod-zalog-pts` | +63 |
| 3 | Деньги под залог ПТС | `dengi-pod-zalog-pts` | +63 |
| 4 | Уфа | `ufa` | +64 |

После трех интентов будет:

```text
9 городов x (1 хаб + 9 интентов + 9 x 6 модификаторов) = 576 коммерческих страниц
```

## Роли документов

- `seo_strategy/programmatic_geo_strategy.md` - главная стратегия, математика, очередность публикаций и ограничения.
- `site_structure/live_sitemap_0.xml` - локальный снимок live sitemap: `https://bablocar.ru/sitemap-0.xml`.
- `site_structure/live_publication_smoke_check.md` - короткий чеклист после публикации города, интента или модификатора.
- `site_structure/page_generation_rules.md` - правила масштабирования: город -> интент -> модификатор.
- `site_structure/page_meta_hero_checklist.md` - что проверять в meta/hero: title, description, eyebrow, H1, lead.
- `site_structure/commercial_landing_template.md` - базовый шаблон коммерческого лендинга.
- `site_structure/commercial_landing_audit.md` - короткие аудиты готовых коммерческих страниц.
- `site_structure/commercial_landing_block_review.md` - подробный разбор блоков и визуальных референсов.
- `site_structure/service_pages.md` - служебные страницы `/info`.
- `partners/safe_claims.md` - безопасные и рискованные формулировки.
- `partners/partner_conditions.md` - агрегированные условия партнеров.
- `competitors/findings.md` - выводы по рынку и конкурентным подходам.
- `product/product_brief.md` - продуктовые факты, ограничения и позиционирование.

## Правила проекта

- BabloCar - брокер/сервис подбора, не кредитор.
- Не обещаем 100% одобрение, деньги за 15 минут и одинаковые условия для всех.
- Автомобиль остается у клиента только как аккуратное УТП, без юридически жестких обещаний.
- В глобальном дисклеймере не фиксируем жесткое "от 2%", если нет подтвержденной ПСК.
- Севастополь и Махачкалу временно не включаем в план без отдельного решения.

## Рабочий процесс после публикации

1. Обновить `site_structure/live_sitemap_0.xml` из `https://bablocar.ru/sitemap-0.xml`.
2. Проверить счетчики sitemap: города, интенты, модификаторы, `/info`.
3. Для новой сущности проверить верхний слой: `200`, canonical, noindex, title, description, H1.
4. Проверить связку с хабом: город -> базовые интенты.
5. Обновить `seo_strategy/programmatic_geo_strategy.md`.
6. В Яндекс Вебмастере отправлять верхний слой: хаб + базовые интенты, без модиков на первом проходе.

## Локальные и черновые данные

Семантика и сырые выгрузки не являются частью обычного git-пакета.

В рабочем дереве могут быть незакоммиченные черновики инструментов аудита (`docs/`, `scripts/`, `reports/`, `package.json`). Их не удаляем и не пушим без отдельного решения.
