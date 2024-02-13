# Элементы HTML форм

Формы предоставляют пользователю средство взаимодействия с веб-сайтами, позволяя отправлять данные и осуществлять разнообразные действия.

Элемент HTML ``<form>`` может содержать один или несколько из следующих элементов формы:

- **input**;
- **label**;
- **select**;
- **textarea**;
- **button**;
- **fieldset**;
- **legend**;
- **datalist**;
- **output**;
- **option**;
- **optgroup**.

## Элемент input

Одним из наиболее часто используемых элементов формы является ``<input>`` элемент. Элемент ``<input>`` может отображаться несколькими способами, в зависимости от ``type`` атрибута.

```
<label for="fname">First name:</label>
<input type="text" name="fname" id="fname">
```

## Элемент label

Элемент ``<label>`` определяет метку для нескольких элементов формы. Этот ``<label>`` элемент полезен для пользователей программ чтения с экрана, поскольку программа чтения с экрана прочитает вслух метку, когда пользователь сосредоточиться на элементе ввода.

Этот ``<label>`` элемент также помогает пользователям, у которых возникают трудности с нажатием на очень маленькие области (например, переключатели или флажки), поскольку, когда пользователь щелкает текст внутри элемента ``<label>``, он переключает переключатель/флажок.

Атрибут ``for`` тега ``<label>`` должен быть равен ``id`` атрибуту элемента ``<input>``, чтобы связать их вместе.

```
<label for="fname">First name:</label>
<input type="text" name="fname" id="fname">
```

## Элемент select

Элемент ``<select>`` определяет раскрывающийся список:

```
<label for="cars">Choose a car:</label>
<select name="cars" id="cars" size="2" multiple>
    <option value="volvo" selected>Volvo</option>
    <option value="fiat">Fiat</option>
    <option value="audi">Audi</option>
    <option value="lada">Lada</option>
</select>
```

Элемент ``<option>`` определяет опцию, которую можно выбрать. По умолчанию выбирается первый элемент раскрывающегося списка. Чтобы определить предварительно выбранный параметр, добавьте ``selected`` к нему атрибут:

Используйте ``size`` атрибут, чтобы указать количество видимых значений.

Используйте ``multiple`` атрибут, чтобы позволить пользователю выбрать более одного значения.

## Элемент textarea

Элемент ``<textarea>`` определяет многострочное поле ввода (текстовую область):

```
<textarea name="message" cols="30" rows="10">
    The car was playing in the garden.
</textarea>
```

Атрибут ``rows`` определяет видимое количество строк в текстовой области. Атрибут ``cols`` определяет видимую ширину текстовой области.

## Элемент button

Элемент ``<button>`` определяет кнопку, на которую можно нажать:

```
<button type="button" onclick="alert('Hello, world!')">Click me</button>
```

**Примечание:** Всегда указывайте ``type`` атрибут элемента кнопки. Разные браузеры могут использовать разные типы по умолчанию для элемента кнопки.

## Элементы fieldset и legend

Этот ``<fieldset>`` элемент используется для группировки связанных данных в форме. Элемент ``<legend>`` определяет заголовок для ``<fieldset>`` элемента.

```
<form action="">
    <fieldset>
        <legend>Personalia:</legend>
        <label for="fname">First name:</label>
        <input type="text" id="fname" name="fname" value="John">

        <br>

        <label for="lname">Last name:</label>
        <input type="text" id="lname" name="lname" value="Doe">

        <br>

        <input type="submit" value="Send">
    </fieldset>
</form>
```

## Элемент datalist

Элемент ``<datalist>`` определяет список предопределенных параметров для ``input`` элемента. Пользователи увидят раскрывающийся список предварительно определенных параметров при ввода данных. Атрибут ``list`` элемента ``<input>`` должен ссылаться на ``id`` атрибут элемента ``<datalist>``

Пример:

```
<form action="">
    <input list="browsers">
    <datalist id="browsers">
        <option value="Edge">
        <option value="Firefox">
        <option value="Chrome">
        <option value="Opera">
        <option value="Safari">
    </datalist>
</form>
```

## Элемент output

Элемент ``<output>`` представляет собой результат вычисления (например, выполняемого сценарием).

Пример:

```
<form action="" oninput="x.value=parseInt(a.value)+parseInt(b.value)">
    0
    <input type="range" name="a" id="a" value="50">
    100 +
    <input type="range" name="b" id="b" value="50">
    =
    <output name="x" for="a b"></output>
    <br><br>
    <input type="submit">
</form>
```

## Заключение

Элементы форм HTML представляют множество возможностей для создания интерактивных и удобных форм на веб-сайтах. Понимание и использование этих элементов позволяют разработчикам создавать более дружелюбные и функциональные пользовательские интерфейсы.