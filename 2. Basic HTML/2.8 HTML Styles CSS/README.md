# CSS в HTML

Три способа подключить стили к разметке. В проектах предпочтителен **внешний CSS**.

← [Базовый HTML](../README.md) · [Инлайн-стили](../2.3%20HTML%20Styles/README.md) · [Классы](../2.17%20HTML%20Classes/README.md)

- [Три способа](#три-способа)
- [Примеры](#примеры)
- [Каскад](#каскад)
- [Дальше](#дальше)

## Три способа

| Способ | Как | Когда |
|--------|-----|-------|
| **Inline** | `style="…"` на элементе | Один элемент, прототип |
| **Внутренний** | `<style>` в `<head>` | Одна страница, демо |
| **Внешний** | `<link rel="stylesheet" href="style.css">` | Реальные проекты |

## Примеры

**Inline:**

```html
<h1 style="color: navy;">Заголовок</h1>
```

**Внутренний:**

```html
<head>
    <style>
        body { font-family: system-ui, sans-serif; }
        .highlight { background: #fff3cd; }
    </style>
</head>
```

**Внешний:**

```html
<head>
    <link rel="stylesheet" href="styles/main.css">
</head>
```

Файл `.css` содержит только правила CSS, без HTML-тегов.

## Каскад

CSS — **каскадный**: стили наследуются от родителя к потомкам, а при конфликте побеждает более специфичное или позднее правило. Подробнее — в серии CSS-Training.

## Дальше

- [Классы](../2.17%20HTML%20Classes/README.md) и [id](../2.18%20HTML%20Id/README.md)
- [Адаптивность](../2.24%20HTML%20Responsive/README.md) — media queries в CSS
- [Head](../2.22%20HTML%20Head/README.md) — где подключать `<link>` и `<style>`
