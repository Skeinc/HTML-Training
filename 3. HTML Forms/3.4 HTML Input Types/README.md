# Типы ввода HTML

HTML предоставляет разнообразные элементы ввода, которые позволяют пользователям взаимодействовать с веб-страницами.

Вот различные типы ввода, которые вы можете использовать в HTML:

- **input type="button"**;
- **input type="checkbox"**;
- **input type="color"**;
- **input type="date"**;
- **input type="datetime-local"**;
- **input type="email"**;
- **input type="file"**;
- **input type="hidden"**;
- **input type="image"**;
- **input type="month"**;
- **input type="number"**;
- **input type="password"**;
- **input type="radio"**;
- **input type="range"**;
- **input type="reset"**;
- **input type="search"**;
- **input type="submit"**;
- **input type="tel"**;
- **input type="text"**;
- **input type="time"**;
- **input type="url"**;
- **input type="week"**.

**Совет:** Значением атрибута по умолчанию ``type`` является "text".

## Тип ввода Текст

``<input type="text">`` определяет однострочное поле ввода текста:

```
<label for="fname">First name:</label>
<input type="text" id="fname" name="fname"><br>
```

## Тип ввода Пароль

``<input type="password">`` определяет поле пароль:

```
<label for="pwd">Password:</label>
<input type="password" id="pwd" name="pwd"><br>
```

Символы в поле пароля замаскированы (отображаются звездочками или кружками).

## Тип ввода Отправить

``<input type="submit">`` определяет кнопку для отправки данных формы в обработчик формы. Обработчик формы обычно представляет собой серверную страницу со скриптом для обработки входных данных. Обработчик формы указан в атрибуте формы ``action``:

```
<input type="submit" value="Send"><br>
```

Если вы опустите атрибут ``value`` кнопки отправки, кнопка получит текст по умолчанию.

## Тип ввода Сброс

``<input type="reset">`` определяет кнопку сброса, которая сбрасывает все значения формы к значениям по умолчанию:

```
<input type="reset" value="Reset"><br>
```

Если вы измените входные значения, а затем нажмете кнопку "Сбросить", данные формы будут сброшены до значений по умолчанию.

## Тип входа Радио

``<input type="radio">`` определяет переключатель.

Радиокнопки позволяют пользователю выбрать только один из ограниченного числа вариантов:

```
<form action="">
    <label for="html">HTML</label>
    <input type="radio" id="html" name="fav_language" value="HTML"><br>

    <label for="css">CSS</label>
    <input type="radio" id="css" name="fav_language" value="CSS"><br>
</form>
```

## Флажок типа ввода

``<input type="checkbox">`` определяет флажок. Флажки позволяют пользователю выбирать НОЛЬ или БОЛЬШЕ вариантов из ограниченного числа вариантов.

```
<form action="">
    <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
    <label for="vehicle1">I have a bike</label><br>

    <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
    <label for="vehicle2">I have a car</label><br>

    <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
    <label for="vehicle3">I have a boat</label><br>
</form>
```

## Кнопка типа ввода

``<input type="button">`` определяет кнопку:

```
<input type="button" value="Click me!" onclick="alert('Hello, World!')">
```

## Тип ввода Цвет

Используется ``<input type="color">`` для полей ввода, которые должны содержать цвет. В зависимости от поддержки браузера в поле ввода может отображаться палитра цветов.

```
<form action="">
    <label for="favcolor">Select your favorite color:</label>
    <input type="color" id="favcolor" name="favcolor">
</form>
```

## Тип ввода Дата

Используется ``<input type="date">`` для полей ввода, которые должны содержать дату. В зависимости от поддержки браузера в поле ввода может отображаться средство выбора даты.

```
<form action="">
    <label for="birthday">Birthday:</label>
    <input type="date" id="birthday" name="birthday">
</form>
```

Вы также можете использовать атрибуты ``min`` и ``max`` для добавления ограничений к датам.

## Тип ввода Datetime-local

Определяет ``<input type="datetime-local">`` поле ввода даты и времени без часового пояса. В зависимости от поддержки браузера в поле ввода может отображаться средство выбора даты.

```
<form action="">
    <label for="birthdaytime">Birthday (date and time):</label>
    <input type="datetime-local" id="birthdaytime" name="birthdaytime">
</form>
```

## Тип ввода Электронная почта

Используется ``<input type="email">`` для полей ввода, которые должны содержать адрес электронной почты. В зависимости от поддержки браузера адрес электронной почты может автоматически проверяться при отправке. Некоторые смартфоны распознают тип электронной почты и добавляют к клавиатуре "".com"", чтобы соответствовать вводу электронной почты.

```
<form action="">
    <label for="email">Enter your email:</label>
    <input type="email" id="email" name="email">
</form>
```

## Тип ввода Изображение

Определяет ``<input type="image">`` изображение как кнопку отправки. В атрибуте указан путь к изображению ``src``:

```
<form action="">
    <input type="image" src="https://www.google.com/url?sa=i&url=https%3A%2F%2Fcommons.wikimedia.org%2Fwiki%2FFile%3APerspective-Button-Go-icon.png&psig=AOvVaw1jysolnjoUe6xoY7EVYpSa&ust=1708016464541000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCKD-1KWnq4QDFQAAAAAdAAAAABAR" alt="Submit" width="50" height="50">
</form>
```

## Тип ввода Файл

Определяет ``<input type="file">`` поле выбора файла и кнопку "Обзор" для загрузки файлов.

```
<form action="">
    <label for="file">Select a file:</label>
    <input type="file" id="file" name="file">
</form>
```

## Тип входа: Скрытый

Определяет ``<input type="hidden">`` скрытое поле ввода (не видимое пользователю). Скрытое поле позволяет разработчикам включать данные, которые пользователи не могут видеть или изменять при отправке формы. Скрытое поле часто хранит запись базы данных, которую необходимо обновить при отправке формы.

**Примечание:** Хотя значение не отображается пользователю в содержимом страницы, оно видно (и может быть отредактировано) с помощью инструментов разработчика любого браузера или функции "Просмотр исходного кода". Не используйте скрытые входы в качестве меры безопасности.

```
<form action="">
    <label for="fname">First name:</label>
    <input type="text" id="fname" name="fname"><br>
    <input type="hidden" id="custId" name="custId" value="3487">
</form>
```

## Тип ввода Месяц

Позволяет ``<input type="month">`` пользователю выбрать месяц и год:

В зависимости от поддержки браузера в поле ввода может отображаться средство выбора даты.

```
<form action="">
    <label for="bdaymonth">Birthday (month and year):</label>
    <input type="month" id="bdaymonth" name="bdaymonth">
</form>
```

## Тип ввода Номер

Определяет ``<input type="number">`` поле числового ввода. Вы также можете установить ограничения на принимаемые номера. В следующем примере показано числовое поле ввода, в которое можно ввести значение от 1 до 5:

```
<form action="">
    <label for="quantity">Quantity (between 1 and 5):</label>
    <input type="number" id="quantity" name="quantity" min="1" max="5">
</form>
```

### Ограничения ввода

Вот список некоторых распространненых ограничений ввода:

- **checked:** Указывает, что поле ввода должно быть предварительно выбрано, при загрузке страницы;
- **disabled:** Указывает, что поле ввода должно быть отключено;
- **max:** Указывает максимальное значение для поле ввода;
- **maxlength:** Указывание максимальную длину значения для поле ввода;
- **min:** Указывает минимальное значение для поле ввода;
- **pattern:** Указывает регулярное выражение для проверки входного значения;
- **readonly:** Указывает, что поле ввода может быть только читаемым;
- **required:** Указывает, что поле ввода должно быть обязательно заполненным;
- **size:** Указывает ширину (в символах) поля ввода;
- **step:** Указывает допустимые интервалы чисел для поля ввода;
- **value:** Указывает дефолтное значение для поля ввода.

## Тип ввода Диапозон

Определяет ``<input type="range">`` элемент управления для ввода числа, точное значение которого не имеет значения (например, ползунок). Диапозон по умолчанию - от 0 до 100. Однако вы можете установить ограничения на то, какие числа принимаются ``min``, с помощью атрибутов ``max``, и ``step``:

```
<form action="">
    <label for="vol">Volume (between 0 and 50):</label>
    <input type="range" id="vol" name="vol" min="0" max="50">
</form>
```

## Тип ввода Поиск

Используется ``<input type="search">`` для полей поиска (поле поиска ведет себя как обычное текстовое поле).

```
<form action="">
    <label for="search">Search:</label>
    <input type="search" id="search" name="search">
</form>
```

## Тип ввода Телефон

Используется ``<input type="tel">`` для полей ввода, которые должны содержать номер телефона.

```
<form action="">
    <label for="phone">Enter your phone number:</label>
    <input type="tel" id="phone" name="phone" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}">
</form>
```

## Тип ввода Время

Позволяет ``<input type="time">`` пользователю выбрать время (без часового пояса). В зависимости от поддержки браузера в поле ввода может отображаться средство выбора времени.

```
<form action="">
    <label for="appt">Select a time:</label>
    <input type="time" id="appt" name="appt">
</form>
```

## Тип ввода URL-адрес

Используется ``<input type="url">`` для полей ввода, которые должны содержать URL-адрес. В зависимости от поддержки браузера поле URL-адреса может автоматически проверяться при отправке. Некоторые смартфоны распознают тип URL-адреса и добавляют на клавиатуру ".com" в соответствии с водом URL-адреса.

```
<form action="">
    <label for="homepage">Add your homepage:</label>
    <input type="url" id="homepage" name="homepage">
</form>
```

## Тип ввода Неделя

Позволяет ``<input type="week">`` пользователю выбрать неделю и год. В зависимости от поддержки браузера в поле ввода может отображаться средство выбора даты.

```
<form action="">
    <label for="week">Select a week:</label>
    <input type="week" id="week" name="week">
</form>
```

## Заключение

Используя разнообразие типов ввода, вы можете создавать более функциональные и интересные веб-формы, которые удовлетворят потребности ваших пользователей.