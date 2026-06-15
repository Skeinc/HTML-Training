# Глобальные атрибуты HTML

Работают на **любом** HTML-элементе (если спецификация не запрещает).

← [HTML Reference](../README.md)

| Атрибут | Назначение |
|---------|------------|
| `id` | Уникальный идентификатор |
| `class` | Имена классов для CSS/JS |
| `style` | Инлайн CSS (лучше избегать) |
| `title` | Всплывающая подсказка |
| `lang` | Язык фрагмента |
| `dir` | Направление текста: `ltr`, `rtl`, `auto` |
| `hidden` | Скрыть элемент |
| `tabindex` | Порядок фокуса с клавиатуры |
| `contenteditable` | Редактируемый контент |
| `draggable` | Перетаскивание |
| `spellcheck` | Проверка орфографии |
| `accesskey` | Горячая клавиша фокуса |
| `data-*` | Произвольные данные для JS |
| `translate` | Переводить ли элемент (`yes`/`no`) |
| `slot` | Имя слота для Shadow DOM |
| `popover` | Нативный popover (`auto`, `manual`) |
| `inert` | Исключить из фокуса и поиска |

```html
<div id="app" class="container" data-user-id="42" lang="ru" hidden>
```

Подробнее: [MDN: Global attributes](https://developer.mozilla.org/ru/docs/Web/HTML/Global_attributes).

См. также: [Атрибуты в Introduction](../../1.%20Introduction%20to%20HTML/1.3%20HTML%20attributes/README.md).
