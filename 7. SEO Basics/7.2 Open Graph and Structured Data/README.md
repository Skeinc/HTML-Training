# Open Graph и структурированные данные

Как страница выглядит при шаринге в соцсетях и как поисковики понимают тип контента.

← [SEO Basics](../README.md) · [Основы](../7.1%20SEO%20Basics/README.md) · [robots и sitemap](../7.3%20Robots%20and%20Sitemap/README.md)

- [Open Graph](#open-graph)
- [Twitter / X Cards](#twitter--x-cards)
- [JSON-LD](#json-ld)
- [Проверка](#проверка)
- [Дальше](#дальше)

## Open Graph

Мета-теги для превью ссылки в Telegram, VK, Facebook и др.:

```html
<head>
    <meta property="og:title" content="Как устроены HTML-формы">
    <meta property="og:description" content="Краткий анонс статьи для карточки.">
    <meta property="og:image" content="https://example.com/preview.jpg">
    <meta property="og:url" content="https://example.com/blog/html-forms">
    <meta property="og:type" content="article">
    <meta property="og:locale" content="ru_RU">
</head>
```

| Свойство | Зачем |
|----------|-------|
| `og:title` | Заголовок карточки (может отличаться от `<title>`) |
| `og:description` | Подзаголовок |
| `og:image` | Картинка превью (рекомендуется ≥ 1200×630 px) |
| `og:url` | Канонический URL страницы |
| `og:type` | `website`, `article`, `product`… |

Если `og:*` нет, соцсеть возьмёт `<title>` и `meta description` — результат менее предсказуем.

## Twitter / X Cards

Аналог для X (Twitter):

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Как устроены HTML-формы">
<meta name="twitter:description" content="Краткий анонс статьи.">
<meta name="twitter:image" content="https://example.com/preview.jpg">
```

`summary_large_image` — крупное превью; `summary` — компактная карточка.

Часто дублируют те же значения, что и в Open Graph — это нормально.

## JSON-LD

Структурированные данные в `<script>` — поисковик понимает тип страницы (статья, FAQ, товар):

```html
<script type="application/ld+json">
{
    "@context": "https://schema.org",
    "@type": "Article",
    "headline": "Как устроены HTML-формы",
    "author": {
        "@type": "Person",
        "name": "Иван Иванов"
    },
    "datePublished": "2026-06-11",
    "image": "https://example.com/preview.jpg"
}
</script>
```

| `@type` | Когда |
|---------|-------|
| `Article` / `BlogPosting` | Статья, пост блога |
| `Product` | Карточка товара |
| `FAQPage` | Блок вопрос–ответ |
| `Organization` | О компании на главной |

JSON-LD не отображается на странице — только для машин. Не вставляйте в видимый контент то, чего пользователь не видит (правило Google о misleading structured data).

Проверка разметки: [Google Rich Results Test](https://search.google.com/test/rich-results).

## Проверка

- [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) — кэш Open Graph
- Rich Results Test — JSON-LD
- View Page Source — убедитесь, что теги в `<head>`, URL картинок абсолютные (`https://…`)

## Дальше

- [Основы SEO](../7.1%20SEO%20Basics/README.md)
- [Meta robots и canonical](7.4%20Meta%20Robots%20and%20Canonical/README.md)
- [Page Title](../../2.%20Basic%20HTML/2.12%20HTML%20Page%20Title/README.md)
- [Изображения](../../2.%20Basic%20HTML/2.10%20HTML%20Images/README.md) — `alt` и превью
