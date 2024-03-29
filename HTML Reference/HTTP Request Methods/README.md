# Методы HTTP-запросов

HTTP (HyperText Transfer Protocol) - это протокол, используемый для передачи данных между клиентом (обычно веб-браузером) и сервером в Интернете. При взаимодействии с веб-серверами клиенты отправляют HTTP-запросы для получения данных или выполнения операций на сервере.

Протокол передачи гипертекста (HTTP) предназначен для обеспечения связи между клиентами и серверами.

HTTP работает как протокол запроса-ответа между клиентом и сервером.

## Что такое HTTP методы запросов?

HTTP определяет несколько методов запросов, которые клиент может использовать для указания желаемого действия при взаимодействии с сервером. Некоторые из наиболее распространненых методов включают:

1. **GET:** Запрашивает представление ресурса. Данные передаются в строке запроса URL;

2. **POST:** Используется для отправки данных на сервер для создания или обновлении ресурса. Данные передаются в теле запроса;

3. **PUT:** Заменяет все текущие представления ресурса данными, переданными в теле запроса;

4. **DELETE:** Удаляет указанный ресурс;

5. **PATCH:** Применяет частичные изменения к ресурсу;

6. **HEAD:** Запрашивает заголовки ответа, без тела ответа;

7. **OPTIONS:** Используется для получения информации о возможностях сервера или параметрах конкретного ресурса;

8. **CONNECT:** Используется для запуска двусторонней связи с запрошенным ресурсом;

9. **TRACE:** Используется для выполнения обратной проверки сообщения, которая проверяет путь к целевому ресурсу.

## Метод GET

GET используется для запроса данных из указанного ресурса.

Обратите внимание, что строка запроса (пары имя/значение) отправляется в URL-адресе запроса GET:

```
/test/demo_form.php?name1=value1&name2=value2
```

**Некоторые примечания по запросу GET:**

- GET-запросы можно кэшировать;
- GET-запросы остаются в истории браузера;
- GET-запросы можно добавить в закладки;
- Запрос GET никогда не следует использовать при работе с конфиденциальными данными;
- GET-запрос имеет ограничение по длине;
- Запрос GET используется только для запроса данных (не для изменения).

## Метод POST

POST используется для отправки данных на сервер для создания/обновления ресурса.

Данные, отправленные на сервер с помощью POST, хранятся в теле запроса HTTP:

```
POST /test/demo_form.php HTTP/1.1
Host: w3schools.com

name1=value1&name2=value2
```

**Некоторые примечания по запросам POST:**

- POST-запрос никогда не кэшируется;
- POST-запрос не сохраняется в истории браузера;
- POST-запрос нельзя добавить в закладки;
- POST-запрос не имеет ограничений по длине данных.

## Метод PUT

PUT используется для отправки данных на сервер для создания/обновления ресурса.

Разница между POST и PUT заключается в том, что запросы PUT идемпотентны. То есть вызов одного и того же PUT запроса несколько раз будет давать один и тот же результат. Напротив, повторный вызов запроса POST имеет побочные эффекты, связанные с созданием одного и того же ресурса несколько раз.

## Метод HEAD

HEAD почти идентичен GET, но без тела ответа.

Другими словами, если GET/users возвращает список пользователей, то HEAD/users выполнит тот же запрос, но не вернет список пользователей.

Запрос HEAD полезен для проверки того, что вернет запрос GET, прежде чем фактически выполнить запрос GET - запрос HEAD может прочитать заголовок Content-Length, чтобы проверить размер файла, без фактической загрузки файла.

## Метод DELETE

Метод DELETE удаляет указанный ресурс.

## Метод PATCH

Метод PATCH используется для внесения частичных изменений в ресурс.

## Метод OPTION

Метод OPTIONS описывает параметры связи для целевого ресурса.

## Метод CONNECT

Метод CONNECT используется для запуска двусторонней связи (туннеля) с запрошенным ресурсом.

## Метод TRACE

Метод TRACE используется для выполнения обратной проверки сообщения, которая проверяет путь к целевому ресурсу.

## Заключение

HTTP методы запросов предоставляют мощные инструменты для взаимодействия с веб-сервером и обработки различных операций на сервере. Понимание этих методов позволяет разработчикам создавать эффективные веб-приложения, обеспечивать безопасность данных и управлять ресурсами на сервере. Каждый метод имеет свои особенности и использование, и знание их помогает выбрать подходящий метод для конкретной задачи при разработке веб-приложений.