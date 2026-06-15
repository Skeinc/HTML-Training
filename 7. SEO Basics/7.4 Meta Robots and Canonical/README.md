# Meta robots, canonical и hreflang

Управление индексацией и дублями страниц из `<head>`.

← [SEO Basics](../README.md) · [robots и sitemap](../7.3%20Robots%20and%20Sitemap/README.md) · [Core Web Vitals](../7.5%20Core%20Web%20Vitals/README.md)

- [canonical](#canonical)
- [meta robots](#meta-robots)
- [hreflang](#hreflang)
- [Когда что использовать](#когда-что-использовать)
- [Дальше](#дальше)

## canonical

Одна «главная» URL при нескольких адресах одного контента:

```html
<link rel="canonical" href="https://example.com/blog/html-forms">
```

Примеры дублей: `?utm_source=…`, `http` vs `https`, `/page` и `/page/`.

## meta robots

```html
<meta name="robots" content="noindex, nofollow">
```

| Значение | Эффект |
|----------|--------|
| `index` / `noindex` | Индексировать страницу или нет |
| `follow` / `nofollow` | Переходить по ссылкам со страницы |
| `noarchive` | Не показывать кэш в выдаче |

Чаще всего:
- черновики, личный кабинет → `noindex`;
- страница благодарности после оплаты → `noindex`;
- доверенные внешние ссылки → обычный `follow` (nofollow — для рекламы, UGC).

## hreflang

Мультиязычные или региональные версии:

```html
<link rel="alternate" hreflang="ru" href="https://example.com/ru/page">
<link rel="alternate" hreflang="en" href="https://example.com/en/page">
<link rel="alternate" hreflang="x-default" href="https://example.com/page">
```

Помогает Google показать русскую версию в `.ru` и английскую в `.com`.

На странице должна быть ссылка **на саму себя** с правильным `hreflang`.

## Когда что использовать

| Задача | Решение |
|--------|---------|
| Дубль URL с параметрами | `canonical` |
| Страница не для поиска | `noindex` |
| Разные языки | `hreflang` |
| Весь раздел закрыть | `Disallow` в robots.txt + `noindex` на страницах |

`noindex` в meta сильнее, чем `Disallow` в robots.txt для исключения из выдачи.

## Дальше

- [Основы SEO](../7.1%20SEO%20Basics/README.md)
- [Open Graph](7.2%20Open%20Graph%20and%20Structured%20Data/README.md)
