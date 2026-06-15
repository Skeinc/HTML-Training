# robots.txt и sitemap.xml

Файлы в **корне сайта**, не в HTML — но критичны для индексации поисковиками.

← [SEO Basics](../README.md) · [Основы](../7.1%20SEO%20Basics/README.md) · [Meta robots](../7.4%20Meta%20Robots%20and%20Canonical/README.md)

- [robots.txt](#robotstxt)
- [sitemap.xml](#sitemapxml)
- [Связь с HTML](#связь-с-html)
- [Дальше](#дальше)

## robots.txt

`https://example.com/robots.txt` — правила для краулеров:

```text
User-agent: *
Disallow: /admin/
Disallow: /private/
Allow: /blog/

Sitemap: https://example.com/sitemap.xml
```

| Директива | Смысл |
|-----------|-------|
| `User-agent: *` | Для всех роботов |
| `Disallow` | Не индексировать путь |
| `Allow` | Исключение из Disallow |
| `Sitemap` | URL карты сайта |

`robots.txt` — **рекомендация**, не защита. Страница с внешней ссылкой всё равно может попасть в индекс.

## sitemap.xml

Список URL для краулера:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://example.com/</loc>
        <lastmod>2026-06-11</lastmod>
        <changefreq>weekly</changefreq>
        <priority>1.0</priority>
    </url>
    <url>
        <loc>https://example.com/blog/html-forms</loc>
        <lastmod>2026-06-10</lastmod>
    </url>
</urlset>
```

Для больших сайтов — несколько sitemap + индексный файл. Генерируют CMS, плагины или скрипты.

Укажите sitemap в [Google Search Console](https://search.google.com/search-console).

## Связь с HTML

| В HTML | Аналог в файлах |
|--------|-----------------|
| `meta robots noindex` | Запрет индекса **одной** страницы |
| `link rel="canonical"` | Канонический URL в sitemap |
| Чистые URL в `<a href>` | Те же пути в `<loc>` |

Подробнее про запрет индексации — [meta robots](7.4%20Meta%20Robots%20and%20Canonical/README.md).

## Дальше

- [Meta robots и canonical](7.4%20Meta%20Robots%20and%20Canonical/README.md)
- [Основы SEO](../7.1%20SEO%20Basics/README.md)
- [Интернет: HTTP](../../../Internet/2.%20What%20is%20HTTP%3F/README.md)
