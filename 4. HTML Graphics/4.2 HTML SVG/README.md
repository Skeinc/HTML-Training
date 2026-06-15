# HTML SVG

**Scalable Vector Graphics** — векторная графика в XML, встраивается прямо в HTML.

← [HTML Graphics](../README.md) · [Canvas](../4.1%20HTML%20Canvas/README.md)

- [Встраивание](#встраивание)
- [Примеры фигур](#примеры-фигур)
- [Canvas vs SVG](#canvas-vs-svg)
- [Дальше](#дальше)

## Встраивание

**Inline** (предпочтительно для иконок и UI):

```html
<svg width="120" height="120" viewBox="0 0 120 120" aria-hidden="true">
    <circle cx="60" cy="60" r="50" fill="#4a90d9"/>
</svg>
```

**Внешний файл:**

```html
<img src="logo.svg" alt="Логотип компании">
```

**CSS:** `background-image: url(icon.svg)`.

## Примеры фигур

```html
<svg width="200" height="100">
    <rect x="10" y="10" width="80" height="40" fill="tomato"/>
    <circle cx="150" cy="50" r="30" fill="gold" stroke="#333"/>
    <text x="10" y="90" font-size="14">SVG-текст</text>
</svg>
```

Градиенты, `<defs>`, `<use>`, анимация через CSS или SMIL. Сложные иллюстрации — в редакторе (Figma, Inkscape) → export SVG.

## Canvas vs SVG

| Задача | Выбор |
|--------|-------|
| Иконка, логотип, диаграмма | SVG |
| Игра, частые перерисовки, фильтры пикселей | Canvas |
| Интерактив по клику на фигуру | SVG (события на элементах) |

## Дальше

- [Изображения](../2.%20Basic%20HTML/2.10%20HTML%20Images/README.md)
- [Справочник: svg](../../HTML%20Reference/HTML%20Tags/Images/Tag%20%3Csvg%3E/README.md)
