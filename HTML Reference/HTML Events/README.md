# HTML-события (обзор)

Атрибуты вроде `onclick`, `onchange`, `onsubmit` вызывают JS при действии пользователя.

← [HTML Reference](../README.md)

## В HTML

```html
<button type="button" onclick="alert('Привет')">Клик</button>
```

## В современных проектах

Логику выносят в `.js`:

```javascript
button.addEventListener('click', () => alert('Привет'));
```

Так проще тестировать, нет inline-кода в разметке, работает Content Security Policy.

## Частые события

| Событие | Когда |
|---------|-------|
| `click` | Клик |
| `submit` | Отправка формы |
| `change` | Изменилось значение поля |
| `input` | Ввод в поле (каждый символ) |
| `keydown` / `keyup` | Клавиатура |
| `load` | Ресурс загружен |
| `DOMContentLoaded` | DOM готов |

Полный список: [MDN: Event reference](https://developer.mozilla.org/ru/docs/Web/Events).

См. [JavaScript в HTML](../../2.%20Basic%20HTML/2.20%20HTML%20JavaScript/README.md).
