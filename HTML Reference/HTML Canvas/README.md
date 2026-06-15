# Canvas (справочник)

Элемент `<canvas>` — контейнер для растровой графики через JavaScript API.

← [HTML Reference](../README.md)

Урок: [HTML Canvas](../../4.%20HTML%20Graphics/4.1%20HTML%20Canvas/README.md) · Тег: [`<canvas>`](HTML%20Tags/Images/Tag%20%3Ccanvas%3E/README.md)

```html
<canvas id="c" width="300" height="150"></canvas>
<script>
  const ctx = document.getElementById('c').getContext('2d');
  ctx.fillRect(0, 0, 300, 150);
</script>
```

[MDN: Canvas API](https://developer.mozilla.org/ru/docs/Web/API/Canvas_API)
