[Back](../../Readme.md)
# User registration

> _POST_ http://172.104.142.164:8080/sanarip-tamga/api/login

### Request:
```JSON
{
  "username" : "admin",
  "password" : "admin"
}
```

### Response:

* ### 200 Успешно
```json
{
    "USER": {
        "id": 1,
        "sendEmailUponPasswordChange": false,
        "selected": false,
        "name": "Admin",
        "useSignatureForStock": false,
        "singleTab": false,
        "isIncludeSubContextProjects": false,
        "noHelp": false,
        "blocked": true,
        "useSignatureForPurchaseQuotations": false,
        "isSuperPfpUser": false,
        "useSignatureForSalesQuotations": false,
        "isPfpValidator": false,
        "fullName": "Admin",
        "stepStatusSelect": 0,
        "receiveEmails": true,
        "forcePasswordChange": false
    },
    "SESSION_ID": "A695F1BFC91A42DBE3B32801B5B36F38"
}
```
После получения ответа, нужно сохранить **JSESSIONID**, он нужен для запросов которые требуют авторизацию
* ### 401 Unauthorized
```text
Response header: 
JSESSIONID=E245E1BC01B497A861CE0F656990C28D; Path=/axelor-sanarip-tamga-6.3.0; HttpOnly;

Возвращает html
```