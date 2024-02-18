# Атрибуты форм ввода HTML

Атрибуты форм ввода HTML играют ключевую роль в улучшении функциональности и внешнего вида элементов форм на веб-страницах. Понимание и использование этих атрибутов позволяют разработчикам создавать более интерактивные и удобные формы.

## Атрибут формы

Входной ``form`` атрибут указывает форму, ``<input>`` к которой принадлежит элемент. Значение этого атрибуты должно быть равно атрибуту id элемента ``<form>``, которому он принадлежит.

```
<form action="" id="form">
    <label for="fname">First name:</label>
    <input type="text" id="fname" name="fname"><br><br>

    <input type="submit" value="Send">
</form>

<label for="lname">Last name:</label>
<input type="text" id="lname" name="lname" form="form">
```

## Атрибут формирования

Атрибут ввода ``formaction`` указывает URL-адрес файла, который будет обрабатывать вводимые данные при отправке формы.

**Примечание:** Этот атрибут переопределяет ``action`` атрибут элемента ``<form>``.

Атрибут ``formaction`` работает со следующими типами ввода: submit и image.

```
<form action="">
    <label for="fname">First name:</label>
    <input type="text" id="fname" name="fname"><br><br>

    <label for="lname">Last name:</label>
    <input type="text" id="lname" name="lname"><br><br>

    <input type="submit" value="Send">
    <input type="submit" formaction="/action_page.php" value="Send as Admin">
</form>
```

## Атрибут formenctype

Атрибут ввода ``formenctype`` указывает, как данные формы должны быть закодированы при отправке (только для форм с методом POST).

**Примечание:** Этот атрибут переопределяет атрибут enctype элемента ``<form>``.

Атрибут ``formenctype`` работает со следующими типами ввода: submit и image.

В качестве примера - форма с двумя кнопками отправки. Первый отправляет данные формы с кодировкой по умолчанию, второй отправляет данные формы, закодированные как "multipart/form-data":

```
<form action="" method="post">
    <label for="fname">First name:</label>
    <input type="text" id="fname" name="fname"><br><br>

    <label for="lname">Last name:</label>
    <input type="text" id="lname" name="lname"><br><br>

    <input type="submit" value="Send">
    <input type="submit" formenctype="multipart/form-data" value="Send as Multipart/form-data">
</form>
```

## Атрибут formmethod

Атрибут ввода ``formmethod`` определяет метод HTTP для отправки данных формы на URL-адрес действия.

**Примечание:** Этот атрибут переопределяет атрибут метода элемента ``<form>``.

Атрибут ``formmethod`` работает со следующими типами ввода: submit и image.

Данные формы могут быть отправлены как переменные URL (method GET) или как почтовая транзакция HTTP (method POST).

**Примечания к методу GET:**

- Этот метод добавляет данные формы к URL-адресу в парах имя/значение.
- Этот метод полезен для отправки форм, когда пользователь хочет добавить результат в закладки.
- Существует ограничение на объем данных, которые вы можете разместить в URL-адресе (различается в зависимости от браузера), поэтому вы не можете быть уверены, что все данные формы будут правильно переданы.
- Никогда не используйте метод GET для передачи конфиденциальной информации (Пароль или другая конфиденциальная информация будет видна в адресной строке браузера).

**Примечания к методу POST:**

- Этот метод отправляет данные формы как почтовую транзакцию HTTP.
- Отправленные формы с методом POST нельзя добавить в закладки.
- Метод POST более надежен и безопасен, чем GET, а POST не имеет ограничений по размеру.

Например, форма с двумя кнопками отправки. Первый отправляет данные формы с помощью метода GET, второй отправляет данные формы с помощью метода POST:

```
<form action="" method="get">
    <label for="fname">First name:</label>
    <input type="text" id="fname" name="fname"><br><br>

    <label for="lname">Last name:</label>
    <input type="text" id="lname" name="lname"><br><br>

    <input type="submit" value="Send using GET">
    <input type="submit" formmethod="post" value="Send using POST">
</form>
```

## Атрибут formtarget

Входной ``formtarget`` атрибут указывает имя или ключевое слово, указывающее, где отображать ответ, полученный после отправки формы.

**Примечание:** Этот атрибут переопределяет целевой атрибут элемента ``<form>``.

Атрибут ``formtarget`` работает со следующими типами ввода: submit и image.

Пример, форма с двумя кнопками отправки и разными целевыми окнами:

```
<form action="">
    <label for="fname">First name:</label>
    <input type="text" id="fname" name="fname"><br><br>

    <label for="lname">Last name:</label>
    <input type="text" id="lname" name="lname"><br><br>

    <input type="submit" value="Send">
    <input type="submit" formtarget="_blank" value="Send to a new window/tab">
</form>
```

## Атрибут formnovalidate

Атрибут ввода ``formnovalidate`` указывает, что элемент ``<input>`` не должен проверяться при отправке.

**Примечание:** Этот атрибут переопределяет атрибут novalidate элемента ``<form>``.

Атрибут ``formnovalidate`` работает со следующими типами ввода: submit.

```
<form action="">
    <label for="email">Enter your email:</label>
    <input type="email" id="email" name="email"><br><br>

    <input type="submit" value="Send">
    <input type="submit" formnovalidate="formnovalidate" value="Send without validation">
</form>
```

## Атрибут novalidate

Атрибут ``novalidate`` есть ``<form>`` атрибут.

Если присутствует, novalidate указывает, что все данные формы не должны проверяться при отправке.

```
<form action="" novalidate>
    <label for="email">Enter your email:</label>
    <input type="email" id="email" name="email"><br><br>

    <input type="submit" value="Send">
</form>
```

## Заключение

Эти атрибуты ввода HTML предоставляют разработчикам набор инструментов для создания более динамичных и удобных форм. Используя эти атрибуты, веб-разработчики могут настраивать элементы формы для удовлетворения конкретных требований и улучшения общего пользовательского опыта. Буть то предоставление подсказок, соблюдение форматов ввода или управление взаимодействием пользователя, понимание этих атрибутов является неотъемлемым элементов эффективной веб-разработки.