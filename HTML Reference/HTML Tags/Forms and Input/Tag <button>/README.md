# Тег button

Тег ``<button>`` представляет собой важный элемент для создания интерактивных кнопок на веб-страницах. Он предоставляет разработчикам гибкий инструмент для создания различных видов кнопок, используемых для отправки форм, выполнения скриптов и других действий.

Тег ``<button>`` используется для создания кнопок на веб-страницах. Он может содержать текст, изображение или даже другие HTML-элементы.

```
<button type="button">Click me!</button>
```

Атрибут ``type`` определяет тип кнопки. Значение ``<button>`` указывает, что это обычная кнопка.

## Определение и использование

Тег ``<button>`` определяет кнопку, на которую можно нажать. Внутри ``<button>`` элемента вы можете поместить текст. Это возможно с кнопкой, созданной с помощью элемента.

**Совет:** Всегда указывайте ``type`` атрибут элемента ``<button>``, чтобы сообщить браузеру, какой тип кнопки это.

**Совет:** Вы можете легко стилизовать кнопки с помощью CSS.

## Атрибуты

- **autofocus:** autofocus | Определяет, следует ли элементу автоматически получить фокус при загрузке страницы;
- **disabled:** disabled | Определяет, должен ли элемент быть отключен;
- **form:** form_id |  Определяет, к какой форме принадлежит элемент;
- **formaction:** URL | Указывает URL файла, который будет обрабатывать элемент управления вводом при отправке формы (для type="submit" и type="image");
- **formenctype:** application/x-www-form-urlencoded, multipart/form-data, text/plain | Указывает, как данные формы должны быть закодированы при их отправке на сервер (для type="submit" и type="image");
- **formmethod:** get, post | Определяет метод HTTP для отправки данных на URL-адрес действия (для type="submit" и type="image");
- **formnovalidate:** formnovalidate | Определяет, необходимо ли проверять элементы формы при их отправке;
- **formtarget:** _blank, _self, _parent, _top, framename |  Указывает, где следует отображать ответ после отправки формы;
- **popovetarget:** element_id | Указывает, какой элемент вызвать (только для type="button");
- **popovetargetaction:** hide, show, toggle | Определяет действие, которое произойдет с элементом при щелчке на кнопку (только для type="button");
- **name:** text | Определяет имя элемента;
- **type:** button, submit, reset | Определяет тип элемента;
- **value:** text | Определяет значение элемента;

## Примечания

- Тег ``<button>`` поддерживает глобальные атрибуты в HTML;
- Тег ``<button>`` поддерживает атрибуты событий в HTML.

## Заключение

Тег ``<button>`` является важным элементов для создания интерактивных кнопок на веб-страницах. Благодаря разнообразным атрибутам и типам, он обеспечивает гибкость при создании различных видов кнопок для разных сценариев использования. Используйте ``<button>`` для улучшения пользовательского опыта и добавления функциональности к вашим веб-приложениям.