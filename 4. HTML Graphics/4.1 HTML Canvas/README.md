# HTML Canvas

Прямоугольная область для рисования **через JavaScript**. Сам `<canvas>` — только контейнер.

← [HTML Graphics](../README.md) · [SVG](../4.2%20HTML%20SVG/README.md)

- [Разметка](#разметка)
- [Контекст 2D](#контекст-2d)
- [Ограничения](#ограничения)
- [Дальше](#дальше)

## Разметка

```html
<canvas id="board" width="400" height="200"></canvas>
```

| Атрибут | Зачем |
|---------|-------|
| `id` | Связь со скриптом |
| `width` / `height` | Размер в пикселях (не путать с CSS-размером) |

Границы и фон — через CSS. Демо — в [`index.html`](index.html).

## Контекст 2D

```javascript
const canvas = document.getElementById('board');
const ctx = canvas.getContext('2d');

ctx.fillStyle = '#4a90d9';
ctx.fillRect(10, 10, 100, 50);

ctx.beginPath();
ctx.arc(200, 100, 40, 0, Math.PI * 2);
ctx.stroke();

ctx.font = '20px sans-serif';
ctx.fillText('Привет', 280, 105);
```

API: линии, дуги, текст, `drawImage()` для картинок, градиенты, трансформации. Для анимации — `requestAnimationFrame`.

Есть также `webgl` / `webgl2` для 3D.

## Ограничения

- Нет доступности «из коробки» — для скринридеров нужен fallback или ARIA
- При изменении сцены перерисовывайте весь кадр (пиксели не «запоминаются» как объекты)
- На Retina учитывайте `devicePixelRatio` для чёткости

## Дальше

- [SVG](../4.2%20HTML%20SVG/README.md) — когда нужен вектор и DOM-события на фигурах
- [Справочник: canvas](../../HTML%20Reference/HTML%20Tags/Images/Tag%20%3Ccanvas%3E/README.md)
