# HTML Плагины

HTML Plug-ins - расширение возможностей вашего веб-сайта.

HTML Плагины представляют собой мощный инструмент для расширения функциональности веб-сайтов. Они позволяют добавлять различные возможности и элементы на веб-страницы, делая сайт более интерактивным и привлекательным для пользователей.

Плагины - это компьютерные программы, расширяющие стандартные функциональные возможности браузера.

## Плагины

Плагины были разработны для использования в самых разных целях:

- Запуск Java-апплетов;
- Запуск элементов управления Microsoft ActiveX;
- Для отображения Flash-роликов;
- Для отображения карт;
- Для сканирования на наличие вирусов;
- Чтобы подтвердить банковский идентификатор.

**Предупреждение:**

Большинство браузеров больше не поддерживают Java-апплеты и плагины. Элементы ActiveX больше не поддерживаются ни в одном браузере. В современных браузерах также отключена поддержка Shockwave Flash.

## Элемент object

Элемент ``<object>`` поддерживается всеми браузерами.

Элемент ``<object>`` определяет встроенный объект в HTML-документе.

Он был разработан для встраивания плагинов (таких как Java-апплеты, программы чтения PDF-файлов и проигрыватели Flash) в веб-страницы, но также можно использовать для включения HTML в HTML:

```
<object width="100%" height="500px" data="../5.2 HTML  Видео/index.html"></object>
```

Или изображения, если хотите

```
<object data="audi.jpeg"></object>
```

## Элемент embed

Элемент ``<embed>`` поддерживается во всех основных браузерах.

Элемент ``<embed>`` также определяет встроенный объект в HTML-документе.

Веб-браузеры уже давно поддерживают элемент ``<embed>``. Однако до HTML5 он не был частью спецификации HTML.

```
<embed src="audi.jpeg">
```

Обратите внимание, что элемент ``<embed>`` не имеет закрывающего тега. Он не может содержать альтернативный текст.

Элемент ``<embed>`` также можно использовать для включения HTML в HTML:

```
<embed width="100%" height="500px" src="../5.3 HTML Аудио/index.html">
```

## Заключение

HTML-плагины представляют собой отличный способ улучшить возможности вашего веб-сайта и сделать его более привлекательным для пользователей. Подобранные и использованные плагины могут значительно улучшить функциональность сайта и обогатить пользовательский опыт.