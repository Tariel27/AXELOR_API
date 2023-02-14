[Back](../../Readme.md)
# User registration

> _POST_ http://172.104.142.164:8080/sanarip-tamga/login.jsp

### Request:
```JSON
{
  "username" : "admin",
  "password" : "admin"
}
```

### Response:

* ### 200 Успешно
```text
Response header:
    Cookie:
        CSRF-TOKEN=89c198d7-16d0-4054-80cf-8a21af3b2b13; Path=/sanarip-tamga;
        JSESSIONID=9050097914F58D38835F70670CF46C1C; Path=/sanarip-tamga; HttpOnly;

Response body: пусто
```
После получения ответа, нужно сохранить **JSESSIONID**, он нужен для запросов которые требуют авторизацию
* ### 401 Unauthorized
```text
Response header: 
JSESSIONID=E245E1BC01B497A861CE0F656990C28D; Path=/axelor-sanarip-tamga-6.3.0; HttpOnly;

Возвращает html
```