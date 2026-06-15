# Атрибуты HTML-элементов

Краткая сводка часто используемых атрибутов. Полный список — на [MDN](https://developer.mozilla.org/ru/docs/Web/HTML/Attributes).

← [HTML Reference](../README.md) · [Глобальные](HTML%20Global%20Attributes/README.md)

## Форма

| Атрибут | Элемент | Назначение |
|---------|---------|------------|
| `action` | `form` | URL отправки |
| `method` | `form` | `get` / `post` |
| `enctype` | `form` | Кодировка тела (`multipart/form-data` для файлов) |
| `name` | `input`, `select`, `textarea` | Имя поля в запросе |
| `type` | `input` | Тип поля |
| `value` | `input`, `button` | Значение |
| `placeholder` | `input`, `textarea` | Подсказка |
| `required` | поля формы | Обязательное |
| `disabled` | поля формы | Неактивно, не отправляется |
| `readonly` | поля формы | Только чтение, отправляется |
| `pattern` | `input` | RegExp-валидация |
| `min` / `max` | `input` | Числа, даты |
| `for` | `label` | Связь с `id` поля |

Урок: [HTML Forms](../../3.%20HTML%20Forms/README.md).

## Ссылки и медиа

| Атрибут | Элемент | Назначение |
|---------|---------|------------|
| `href` | `a` | URL |
| `target` | `a`, `form` | Где открыть (`_blank` + `rel="noopener"`) |
| `rel` | `a`, `link` | Отношение (`stylesheet`, `icon`, `nofollow`…) |
| `src` | `img`, `script`, `iframe`… | URL ресурса |
| `alt` | `img` | Альтернативный текст |
| `width` / `height` | `img`, `video`, `canvas` | Размеры |
| `controls` | `video`, `audio` | Панель управления |
| `poster` | `video` | Превью до play |

## Таблицы

| Атрибут | Назначение |
|---------|------------|
| `colspan` / `rowspan` | Объединение ячеек |
| `scope` | `col` / `row` для `th` |

## Прочее

| Атрибут | Элемент | Назначение |
|---------|---------|------------|
| `charset` | `meta` | Кодировка |
| `content` | `meta` | Значение meta |
| `name` | `meta` | Имя meta (`viewport`, `description`) |
| `defer` / `async` | `script` | Загрузка скрипта |
| `sandbox` | `iframe` | Ограничения embed |
| `aria-*` | любой | Доступность |

События `onclick` и др. — см. [HTML Events](HTML%20Events/README.md); в проектах предпочтительнее `addEventListener`.
