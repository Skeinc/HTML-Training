# Тег template

Тег ``<template>`` представляет собой мощный инструмент, введенный в HTML5, для создания шаблонов, которые могут быть использованы для клонирования и вставки в документ по мере необходимости. Тег ``<template>`` предназначен для определения фрагмента HTML, который не должен отображаться при загрузке страницы. Вместо этого его содержимое может быть использовано с помощью JavaScript для создания динамических элементов.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tag template</title>
</head>
<body>
    <button onclick="showContent()" type="button">Show hidden content</button>

    <template id="greeting">
        <p>Hello, dude! My name is Dmitry Anufriev, i'm 21 y.o frontend developer. My favorite framework is Angular 17!</p>
    </template>

    <script>
        function showContent(){
            const template = document.getElementsByTagName("template")[0];
            const cloneElement = template.content.cloneNode(true);
            document.body.appendChild(cloneElement);
        }
    </script>
</body>
</html>
```

## Использование с помощью JavaScript

JavaScript может использоваться для извлечения содержимого тега ``<template>`` и вставки его в документ.

## Совместимость и Полифиллы

Хотя большинство современных браузеров отображают тег ``<template>``, для обеспечения совместимости с более старыми браузерами можно использовать полифиллы, такие как HTMLTemplateElement или template-polyfill.

## Примечания

- Вы можете использовать ``<template>`` тег, если у вас есть HTML-код, который вы хотите использовать снова и снова, но не раньше, чем вы об этом попросите. Чтобы сделать это без тега ``<template>``, вам необходимо создать HTML-код с помощью JavaScript, чтобы браузер не отображал код.
- Тег ``<template>`` поддерживает глобальные атрибуты в HTML.
- Тег ``<template>`` не поддерживает атрибуты событий в HTML.

## Заключение

Тег ``<template>`` в HTML предоставляет эффективный способ создания и использования шаблонов в веб-разработке. Используйте его для улучшения организации кода, создания динамических компонентов и улучшения производительности ваших веб-приложений.