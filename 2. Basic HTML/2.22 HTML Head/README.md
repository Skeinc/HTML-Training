# Секция `<head>`

Метаданные документа: кодировка, заголовок вкладки, стили, скрипты. На странице не отображается.

← [Базовый HTML](../README.md) · [Title](../2.12%20HTML%20Page%20Title/README.md) · [Favicon](../2.11%20HTML%20Favicon/README.md)

- [Типичное содержимое](#типичное-содержимое)
- [Элементы](#элементы)
- [Чего избегать](#чего-избегать)

## Типичное содержимое

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Название страницы</title>
    <meta name="description" content="Краткое описание для поисковиков">
    <link rel="icon" href="/favicon.ico">
    <link rel="stylesheet" href="styles.css">
    <script src="app.js" defer></script>
</head>
```

## Элементы

| Элемент | Назначение |
|---------|------------|
| `<meta charset>` | Кодировка (UTF-8) |
| `<meta name="viewport">` | Масштаб на мобильных |
| `<title>` | Заголовок вкладки |
| `<meta name="description">` | Описание для сниппета (не для «keywords») |
| `<link rel="stylesheet">` | Внешний CSS |
| `<link rel="icon">` | Favicon |
| `<style>` | CSS на этой странице |
| `<script>` | JavaScript |
| `<base href="…">` | База для относительных URL (редко; один на документ) |

`viewport` обязателен для адаптивной вёрстки — [Адаптивность](../2.24%20HTML%20Responsive/README.md).

## Чего избегать

- `<meta http-equiv="refresh">` — авто-перезагрузка; раздражает пользователей
- `<meta name="keywords">` — поисковики игнорируют с ~2009 года
- Скрипты в `<head>` без `defer`/`async` — блокируют отрисовку
- `<base>` без необходимости — ломает все относительные ссылки

## Дальше

- [Кодировка](../2.31%20HTML%20Charset/README.md)
- [SEO Basics](../../7.%20SEO%20Basics/7.1%20SEO%20Basics/README.md)
- [Open Graph и JSON-LD](../../7.%20SEO%20Basics/7.2%20Open%20Graph%20and%20Structured%20Data/README.md)
