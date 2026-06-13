# Технический срез конкурентов: robots / sitemap / URL

Дата среза: 2026-06-13.

Документ фиксирует первичные факты по `robots.txt`, sitemap и URL-структурам конкурентов. Это не SEO-стратегия, не оценка приоритетов и не финальный аудит страниц.

## Методика

- Проверялись `robots.txt`, sitemap из robots и стандартные адреса sitemap.
- Если sitemap был sitemap index, разворачивались релевантные дочерние карты, когда это было быстро и однозначно.
- Количество URL указано только там, где sitemap удалось получить и распарсить.
- Если sitemap не найден, недоступен или вместо XML отдан HTML, это зафиксировано отдельно.
- Сырые временные файлы не сохраняются в репозиторий.

## Брокеры / кредитные помощники

| Домен | robots.txt | sitemap | URL | Основные URL-паттерны | Комментарий |
| --- | --- | --- | ---: | --- | --- |
| `finardi.ru` | есть | `https://finardi.ru/sitemap.xml` | 106 | `/service/`, `/service_ip/`, `/service_ooo/`, `/blog/`, `/news/`, `/cases/` | Компактная брокерская структура. Есть `kredit-pod-zalog-avto`, рефинансирование, плохая КИ, без справок. Отдельной ПТС-структуры в sitemap не видно. |
| `lioncredit.ru` | есть | `https://www.lioncredit.ru/sitemap.xml` | 165 | `/uslugi/`, `/uslugibiz/`, `/informaciya/` | Релевантный брокерский сайт: ПТС, залог авто, деньги под ПТС, рефинансирование под залог авто, плохая КИ, безработные, без справок. |
| `binkor.ru` | есть | `https://binkor.ru/sitemap-all-in-one.xml` | 2 846 | `/product/`, `/news/`, `/calculator/`, `/business/` | Большая SEO-структура. Много страниц по суммам, срокам, плохой КИ, без справок, рефинансированию, статьям 2026 года и калькуляторам. |
| `fin-partners.ru` | есть | `https://fin-partners.ru/sitemap_index.xml` | 312 | `/novosti/`, `/poleznoe/`, `/dt_otzyvy/`, `/ipoteka/`, `/kredity-na-avtomobil/`, `/avtolombard/` | Широкий финансовый брокер. Авто/ПТС не core, но есть полезные разделы по кредитам, авто и рефинансированию. |
| `mkbkfin.ru` | есть | `https://mkbkfin.ru/sitemap.xml` | 96 | `/services/`, `/articles/`, `/company/`, `/calculator/` | Брокерская структура, есть залог авто, залог имущества, рефинансирование, просрочки, без справок. |
| `altarifinance.ru` | есть | sitemap в robots не указан; `/sitemap.xml` отдает HTML | не посчитано | не определено | Нужна ручная проверка структуры сайта. |
| `monolit-realty.ru` | есть | `https://monolit-realty.ru/sitemap_index.xml` | 104 | `/kredit-pod-zalog-2/`, `/refinansirovanie-2/`, `/ipoteka/`, `/zajm-ot-chastnogo-investora/` | Широкий залоговый брокер. Основной фокус выглядит ближе к недвижимости; авто почти не видно. |
| `mbk.ru` | есть | `https://www.mbk.ru/sitemap.xml` | 1 773 | `/blogs/`, `/credit/`, `/zaimy/`, `/refinansirovanie/`, `/dengi/`, `/broker/` | Большая брокерская SEO-структура. Много кредитных, заемных и проблемных интентов; ПТС точечно. |
| `ooorefin.ru` | есть | `https://ooorefin.ru/sitemap.xml` | 3 | главная, политика, одна служебная страница | SEO-структуры почти нет. |
| `pts-zaim.com` | есть | `/sitemap.xml` | 5 | главная, контакты, `kredit-pod-zalog-avto.php`, `dengi-pod-pts.php` | Маленький нишевый ПТС-сайт. Полезен как точечный референс, но не как пример большой SEO-структуры. |

## Агрегаторы / маркетплейсы

| Домен | robots.txt | sitemap | URL | Основные URL-паттерны | Комментарий |
| --- | --- | --- | ---: | --- | --- |
| `bankiros.ru` | есть | `https://bankiros.ru/sitemap.xml` | релевантные карты: 2 133 | `/zaymy/`, `/zaymy/info/`, `/mfo/`, `/credits/`, `/autocredits/` | Sitemap index. Развернуты релевантные карты: `zaymy` 163 URL, `zaymy-info` 359, `mfo` 1 298, `credits` 313. |
| `bip.ru` | есть | `https://bip.ru/sitemap.xml` | 10 360 | `/osago/`, `/shtrafy/`, `/info/`, `/kasko/`, отдельные ПТС-страницы | Большой авто/ОСАГО-портал. ПТС-страниц мало, но есть прямые URL под залог авто и ПТС. |
| `vbr.ru` | есть | `https://www.vbr.ru/sitemap.xml` | релевантная карта: 14 | `/autolombard/` | Sitemap index на 81 карту. Развернута релевантная карта `Autolombard`: есть ПТС, залог авто, грузовое авто, мототехника, спецтехника, перезалог. |
| `banki.ru` | не получен через curl | sitemap не получен | не посчитано | не определено | Через curl возник редиректный цикл / защита. Нужна ручная проверка через браузер или другой способ. |
| `finuslugi.ru` | есть | sitemap в robots не указан; стандартные sitemap-адреса дают 404 | не посчитано | не определено | Нужна отдельная проверка структуры и целевых страниц. |
| `sravni.ru` | есть | sitemap в robots не указан; стандартный sitemap возвращает HTML, не XML | не посчитано | не определено | Нужна отдельная проверка структуры и целевых страниц. |

## МФО / автозалоговые компании / автоломбарды

| Домен | robots.txt | sitemap | URL | Основные URL-паттерны | Комментарий |
| --- | --- | --- | ---: | --- | --- |
| `vashinvestor.ru` | есть | `https://vashinvestor.ru/sitemap.xml` | 7 888 | гео-папки, `/blog/`, `/post/`, ПТС/залоговые лендинги | Очень большая programmatic-сетка: ПТС, залог, гео, проблемные интенты, рефинансирование. |
| `cashmotor.ru` | есть | `https://cashmotor.ru/sitemap.xml` | 103 | `/news/`, `/lp-pts/`, `/lp-pts-bz/`, `/promo-sp-pts/` | Есть ПТС-лендинги. В дочернем sitemap встречаются legacy-URL старого/связанного домена `lombard-capital.ru` после смены домена. |
| `carmoney.ru` | есть | `https://carmoney.ru/sitemap.xml` | 82 | `/uslovija/`, ПТС/залоговые лендинги | Есть `dengi-pod-zalog-pts`, юрлица, грузовые авто, спецтехника, без отказа, онлайн на карту. |
| `cashdrive.ru` | есть | `https://cashdrive.ru/sitemap.xml` | 110 | `/media/`, ПТС/залоговые лендинги | Есть мото, спецтехника, грузовое авто, безработные, без отказа, дубликат ПТС, калькуляторные URL. |
| `creddy.ru` | есть | `https://creddy.ru/sitemap.xml` | 24 | FAQ, ПТС/залоговые лендинги | Маленькая, но точная ПТС-структура: FAQ, без офиса, без осмотра, рефинансирование, авто остается, без отказа. |
| `centrofinans.ru` | есть | `https://centrofinans.ru/sitemap.xml` | 924 | `/blog/`, `/vakansii/`, `/dokumenty/`, `/novosti/`, `/akcii/` | Большая структура, но ПТС в основном через блог/автозайм, не как явное SEO-core направление. |
| `autolombardn1.ru` | есть | `https://autolombardn1.ru/sitemap.xml` | 406 | `/metro/`, `/districts/`, `/cities/` | Сильная локальная гео-сетка: метро, районы, города. |
| `zalog24h.ru` | есть | `https://zalog24h.ru/sitemap.xml` | 65 | `/dengi-pod-zalog/`, `/zajm-pod-zalog-pts/`, `/zajm-pod-zalog-avtomobilya/`, статьи | Нишевая структура под залог, ПТС, районы/направления, статьи по автоломбарду. |
| `autolombard-moskva.ru` | есть | `https://www.autolombard-moskva.ru/sitemap.xml` | 930 | `/services/`, `/about/`, `/pledge-pts/`, `/pledge-auto/`, `/avtozajm/`, `/kredit_pod_zalog_avto/` | Большая локальная структура: услуги, ПТС, авто, залог, калькулятор, FAQ. |

## Примеры релевантных URL

### Брокеры

- `https://finardi.ru/service/kredit-pod-zalog-avto/`
- `https://www.lioncredit.ru/uslugi/kredit-pod-zalog-pts`
- `https://www.lioncredit.ru/uslugi/dengi-pod-zalog-pts`
- `https://www.lioncredit.ru/uslugi/zaym-pod-zalog-pts`
- `https://www.lioncredit.ru/uslugi/refinansirovanie-kredita-pod-zalog-avto`
- `https://mkbkfin.ru/services/kredity-pod-zalog-imushchestva/kredit-pod-zalog-avtomobilya/`
- `https://pts-zaim.com/kredit-pod-zalog-avto.php`
- `https://pts-zaim.com/dengi-pod-pts.php`

### Агрегаторы

- `https://bip.ru/kredity-pod-zalog-avto`
- `https://bip.ru/kredity-pod-zalog-pts`
- `https://bip.ru/zajm-pod-zalog-avto`
- `https://bip.ru/zajm-pod-zalog-pts`
- `https://bankiros.ru/zaymy`
- `https://bankiros.ru/zaymy/bezrabotnym`
- `https://bankiros.ru/credits/bez-spravki-o-dohodah`
- `https://bankiros.ru/autocredits/refinansirovanie-avtokredita`
- `https://www.vbr.ru/autolombard/pod-zalog-avto/`
- `https://www.vbr.ru/autolombard/pod-zalog-pts/`

### МФО / автозалоговые / автоломбарды

- `https://vashinvestor.ru/zaym-pod-zalog-pts-gruzovogo-avtomobilya`
- `https://vashinvestor.ru/srochnyy-zaym-pod-zalog-pts-avtomobilya`
- `https://vashinvestor.ru/dengi-pod-zalog-pts-bez-otkaza`
- `https://vashinvestor.ru/dengi-pod-zalog-pts-bez-spravok-o-dohodah`
- `https://cashmotor.ru/lp-pts/`
- `https://cashmotor.ru/lp-pts-bz/`
- `https://carmoney.ru/dengi-pod-zalog-pts`
- `https://carmoney.ru/dengi-pod-zalog-yuridicheskim-licam`
- `https://cashdrive.ru/zajmy-pod-zalog-gruzovogo-avto`
- `https://cashdrive.ru/zajmy-pod-zalog-avto-s-dublikatom-pts`
- `https://creddy.ru/faq_pts`
- `https://creddy.ru/refinansirovanie-zajma-pod-pts/`
- `https://creddy.ru/dengi-pod-zalog-avto-ostaetsya-u-vas/`
- `https://zalog24h.ru/zajm-pod-zalog-pts/dlya-yuridicheskih-lits/`
- `https://www.autolombard-moskva.ru/avtozajm/`
- `https://www.autolombard-moskva.ru/avtozalog/`

## Что требует отдельной проверки

- `banki.ru`: robots/sitemap не получены через curl из-за редиректов/защиты.
- `finuslugi.ru`: robots доступен, но sitemap не указан; стандартные sitemap-адреса дают 404.
- `sravni.ru`: robots доступен, но sitemap не указан; стандартный sitemap возвращает HTML, не XML.
- `altarifinance.ru`: robots доступен, но sitemap в robots не указан; `/sitemap.xml` возвращает HTML.
- `cashmotor.ru`: в дочернем sitemap встречаются URL старого/связанного домена `lombard-capital.ru`; похоже на наследие после смены домена и неочищенный sitemap.

## Промежуточные наблюдения

- Среди брокеров есть два типа структур: компактные сайты на 100-200 URL и крупные SEO-сетки на 1 000+ URL.
- Самые крупные programmatic-структуры в первом срезе: `vashinvestor.ru`, `binkor.ru`, `mbk.ru`, `bip.ru`.
- Самые точные ПТС/авто-залоговые URL среди брокеров видны у `lioncredit.ru`, `pts-zaim.com`, частично у `mkbkfin.ru`.
- Агрегаторы часто используют sitemap index и раздельные карты по продуктам.
- Локальные автоломбарды активно используют гео-структуру: метро, районы, города, услуги.
- Этот документ фиксирует только технический слой. Структурный SEO-анализ страниц нужно делать отдельным следующим шагом.
