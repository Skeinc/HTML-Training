# Руководство по стилю HTML

Соглашения для читаемого и предсказуемого кода.

← [Базовый HTML](../README.md)

- [Документ](#документ)
- [Разметка](#разметка)
- [Файлы и пути](#файлы-и-пути)
- [Комментарии и скрипты](#комментарии-и-скрипты)

## Документ

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Осмысленный заголовок</title>
</head>
<body>
    …
</body>
</html>
```

- Всегда `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`, `<title>`
- `lang` на `<html>` — для скринридеров и переводчиков
- `charset` и `viewport` — в начале `<head>`

## Разметка

| Правило | Пример |
|---------|--------|
| Теги и атрибуты — строчными | `<div class="card">` |
| Значения атрибутов в кавычках | `href="/about"` |
| Закрывайте парные теги | `<p>…</p>` |
| Семантика вместо лишних `div` | `<nav>`, не `<div class="nav">` |
| `alt` у всех значимых `<img>` | `alt="Описание"` |
| Отступы — 2 или 4 пробела, единообразно | не смешивать с табами |
| Короткие строки | переносить длинные атрибуты |

Без пробелов вокруг `=` в атрибутах: `class="btn"`, не `class = "btn"`.

## Файлы и пути

- Имена файлов — **lowercase**: `about.html`, `main.css`
- Расширения: `.html`, `.css`, `.js` (`.htm` допустим, но редок)
- Главная страница папки — обычно `index.html`
- На Linux-серверах `Photo.jpg` ≠ `photo.jpg`

## Комментарии и скрипты

```html
<link rel="stylesheet" href="styles.css">
<script src="app.js" defer></script>
```

- CSS и JS — во внешних файлах, не инлайн на всю страницу
- `type` у `<script>` и `<link>` в HTML5 не обязателен
- Комментарии — [отдельная статья](../2.6%20HTML%20Comments/README.md)

## Дальше

- [HTML5 и строгая разметка](../2.33%20HTML%20Versus%20XHTML/README.md)
- [Семантика](../2.26%20HTML%20Semantics/README.md)
