# Атрибут `id` в HTML

Уникальный идентификатор **одного** элемента на странице. Якоря, CSS, JavaScript.

← [Базовый HTML](../README.md) · [Классы](../2.17%20HTML%20Classes/README.md) · [Ссылки](../2.9%20HTML%20Links/README.md)

- [Синтаксис](#синтаксис)
- [class vs id](#class-vs-id)
- [Якоря](#якоря)
- [JavaScript](#javascript)

## Синтаксис

```html
<h1 id="page-title">Мои города</h1>
```

Правила значения `id`:

- уникален в пределах документа
- не начинается с цифры
- без пробелов
- чувствителен к регистру

В CSS: `#page-title { … }`.

## class vs id

| | `class` | `id` |
|---|---------|------|
| Количество на странице | много элементов | один элемент |
| CSS | `.name` | `#name` |
| Типичное применение | стили группы | якорь, один виджет, связь label↔input |

## Якоря

```html
<h2 id="chapter-4">Глава 4</h2>
<a href="#chapter-4">К главе 4</a>
```

## JavaScript

```javascript
document.getElementById('page-title');
document.querySelector('#page-title');
```

Предпочитайте `class` для стилей группы; `id` — когда нужна гарантированная уникальность.

## Дальше

- [Ссылки и якоря](../2.9%20HTML%20Links/README.md)
- [HTML Forms](../../3.%20HTML%20Forms/README.md) — `label for="id"` и `input id="…"`
