[Back](../../Readme.md)
# User registration

> _POST_ http://172.104.142.164:8080/sanarip-tamga/api/register

### Request body:
```JSON
{
  "firstName" : "имя",
  "lastName" : "фамилия",
  "email" : "почта@gmail.com"
}
```
Можно ещё отправить другие поля для заполнения (прим. дата рождения, номер телелфона, и т.д поля)<br>
При условии 
* Что в талице есть такое поле
* Правильно написано название поле 
```JSON
{
  "firstName" : "имя",
  "lastName" : "фамилия",
  "email" : "почта@gmail.com",
  "birthDate" : "2015-03-01", 
  "phone" : "996 000 000 000",
}
```


### Response body:

* ### 200 Успешно
```JSON
{
  "status": 0,
  "data": "SUCCESS"
}
```
* ### 400 если почта уже есть в БД 
```JSON
{
  "status": -1,
  "data": {
    "message": "email already exists!"
  }
}
```
* ### 400 если полностью отправить null
```JSON
{
  "status": -1,
  "data": {
    "message": "object is null"
  }
}
```

* ### 400 если один из полей или все поля **_null_**
```JSON
{
  "status": -4,
  "errors": {
    "firstName": "must not be null",
    "lastName": "must not be null",
    "email": "must not be null"
  }
}
```
```JSON
{
  "status": -4,
  "errors": {
    "firstName": "must not be null"
  }
}
```