# Классы в HTML

Атрибут `class` группирует элементы для CSS и JavaScript. Один класс — на многих элементах.

← [Базовый HTML](../README.md) · [id](../2.18%20HTML%20Id/README.md) · [CSS в HTML](../2.8%20HTML%20Styles%20CSS/README.md)

- [HTML и CSS](#html-и-css)
- [Несколько классов](#несколько-классов)
- [JavaScript](#javascript)
- [Практика](#практика)

## HTML и CSS

```html
<p class="warning">Внимание!</p>
<p class="warning">Ещё одно предупреждение.</p>
```

```css
.warning {
    color: #856404;
    background: #fff3cd;
    padding: 8px;
}
```

В CSS селектор класса — точка + имя: `.warning`.

## Несколько классов

Через пробел:

```html
<button class="btn btn-primary">Отправить</button>
```

Элемент получит стили обоих классов `.btn` и `.btn-primary`.

## JavaScript

```javascript
document.querySelectorAll('.warning');
element.classList.add('active');
element.classList.remove('warning');
element.classList.toggle('open');
```

Устаревший `getElementsByClassName` — лучше `querySelectorAll`.

## Практика

- Имена осмысленные: `card`, `nav-link`, не `div2` или `redText`
- Стили в CSS-файле, не дублируйте `style=""` на каждом элементе
- Имена **чувствительны к регистру**: `Warning` ≠ `warning`

## Дальше

- [id](../2.18%20HTML%20Id/README.md) — уникальный идентификатор
- [Стиль кода](../2.27%20HTML%20Style%20Guide/README.md)
