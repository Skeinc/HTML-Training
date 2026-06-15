# Основы SEO

SEO — оптимизация сайта, чтобы поисковики правильно индексировали контент, а пользователи находили релевантные страницы.

← [SEO Basics](../README.md) · [Open Graph](../7.2%20Open%20Graph%20and%20Structured%20Data/README.md)

- [Технический минимум в HTML](#технический-минимум-в-html)
- [Контент](#контент)
- [Техническое SEO](#техническое-seo)
- [Чего избегать](#чего-избегать)
- [Мониторинг](#мониторинг)

SEO — долгий процесс; «волшебных» meta keywords нет.

Полный пример `<head>` для статьи — в [`index.html`](index.html).

## Технический минимум в HTML

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Уникальный заголовок страницы — Бренд</title>
    <meta name="description" content="Краткое описание 150–160 символов для сниппета">
    <link rel="canonical" href="https://example.com/page">
</head>
```

| Элемент | Зачем |
|---------|-------|
| `<title>` | Заголовок в выдаче и вкладке |
| `meta description` | Сниппет (не влияет на ранг напрямую, но влияет на CTR) |
| `canonical` | Одна каноническая URL при дублях |
| `lang` на `<html>` | Язык страницы |
| Семантика `h1`–`h6` | Структура для краулера |

`meta keywords` поисковики игнорируют.

## Контент

- Отвечайте на реальный запрос пользователя, не «набивайте» ключевые слова
- Один чёткий `h1`, подзаголовки по иерархии
- Уникальный текст на каждой странице
- `alt` у изображений — описание, не спам
- Внутренние ссылки на связанные материалы

## Техническое SEO

| Задача | Действие |
|--------|----------|
| Индексация | [robots.txt и sitemap](../7.3%20Robots%20and%20Sitemap/README.md) |
| Дубли и noindex | [canonical, meta robots](../7.4%20Meta%20Robots%20and%20Canonical/README.md) |
| Скорость | [Core Web Vitals](../7.5%20Core%20Web%20Vitals/README.md), lazy-load |
| Мобильная версия | адаптивная вёрстка, viewport |
| HTTPS | обязательный стандарт |
| Структурированные данные | JSON-LD — см. [7.2](../7.2%20Open%20Graph%20and%20Structured%20Data/README.md) |

Чистые URL (`/blog/html-forms`), без лишних параметров.

## Чего избегать

- Скрытый текст и клоакинг
- Дублирование одного контента на многих URL без canonical
- Заголовки ради ключей, не ради смысла
- Покупка ссылок с некачественных площадок

Качественный контент + техническая гигиена + ссылки с авторитетных сайтов — базовая модель.

## Мониторинг

- [Google Search Console](https://search.google.com/search-console) — индексация, ошибки
- Google Analytics / аналог — трафик и поведение
- Проверяйте позиции и страницы входа, исправляйте 404 и битые ссылки

## Дальше

- [Open Graph и JSON-LD](../7.2%20Open%20Graph%20and%20Structured%20Data/README.md)
- [robots.txt и sitemap](../7.3%20Robots%20and%20Sitemap/README.md)
- [Page Title](../../2.%20Basic%20HTML/2.12%20HTML%20Page%20Title/README.md)
