[Back](../../Readme.md)
# Select records

## Полученя ПИ
>POST http://172.104.142.164:8080/sanarip-tamga/ws/rest/com.axelor.apps.sale.db.Declaration/search

Тело запроса:
```json
{
  "limit": 10,
  "sortBy": ["createdOn"],
  "fields": [
    "registrationNumberPreliminaryInformation", 
    "statusSelect", 
    "arrivalLocation.name", 
    "piType", 
    "createdOn", 
    "piCreateDate"
  ]
}
```
Ответ:
```json
{
  "status": 0,
  "offset": 0,
  "total": 2,
  "data": [
    {
      "id": 1,
      "version": 1,
      "statusSelect": 1,
      "$t:arrivalLocation.name": "МПТП ТОРУГАРТ",
      "arrivalLocation.name": "MPTP TORUGART",
      "piType": 1,
      "createdOn": "2023-02-14T10:29:27Z",
      "piCreateDate": "2023-02-14T10:29:44Z",
      "$wkfStatus": null
    },
    {
      "id": 2,
      "version": 1,
      "statusSelect": 3,
      "$t:arrivalLocation.name": "МПТП ТОРУГАРТ",
      "arrivalLocation.name": "MPTP TORUGART",
      "piType": 2,
      "createdOn": "2023-02-14T10:29:27Z",
      "piCreateDate": "2023-02-14T10:29:44Z",
      "$wkfStatus": null
    }
  ]
}
```
---
## ASK, DESK по полям
Нужно просто в теле запроса в поле **sortBy** добавить названия полей (прим **"createdOn"**), и будет сортироватся по ASK.  
Если добавить знак минуса перед названиями полей (прим **"-createdOn"**), будет сортироватся по DESC

>POST http://172.104.142.164:8080/sanarip-tamga/ws/rest/com.axelor.apps.sale.db.Declaration/search  

Тело запроса:
```json
{
  "limit": 10,
  "sortBy": ["-createdOn"],
  "fields": [
    "registrationNumberPreliminaryInformation", 
    "statusSelect", 
    "arrivalLocation.name", 
    "piType", 
    "createdOn", 
    "piCreateDate"
  ]
}
```
Ответ:
```json
{
  "status": 0,
  "offset": 0,
  "total": 2,
  "data": [
    {
      "id": 2,
      "version": 1,
      "statusSelect": 3,
      "$t:arrivalLocation.name": "МПТП ТОРУГАРТ",
      "arrivalLocation.name": "MPTP TORUGART",
      "registrationNumberPreliminaryInformation": "",
      "piType": 2,
      "createdOn": "2023-02-14T10:29:27Z",
      "piCreateDate": "2023-02-14T10:29:44Z",
      "$wkfStatus": null
    },
    {
      "id": 1,
      "version": 1,
      "statusSelect": 1,
      "$t:arrivalLocation.name": "МПТП ТОРУГАРТ",
      "arrivalLocation.name": "MPTP TORUGART",
      "registrationNumberPreliminaryInformation": "",
      "piType": 1,
      "createdOn": "2023-01-14T10:29:27Z",
      "piCreateDate": "2023-02-14T10:29:44Z",
      "$wkfStatus": null
    }
  ]
}
```
---
## FILTER
Фильтрация по полям, проще говоря продвинутый поиск  
Добавляется новое поле "**data**" внутри добавляется условия

>POST http://172.104.142.164:8080/sanarip-tamga/ws/rest/com.axelor.apps.sale.db.Declaration/search  

Тело запроса:
```json
{
  "offset": 0,
  "limit": 10,
  "fields": [
    "registrationNumberPreliminaryInformation",
    "statusSelect",
    "arrivalLocation.name",
    "piType",
    "createdOn",
    "piCreateDate"
  ],
  "sortBy": ["-createdOn"],
  "data": {
    "_domain": "self.piType = :type",
    "_domainContext": {
      "type": "1"
    }
  }
}
```

Ответ:
```json
{
  "status": 0,
  "offset": 0,
  "total": 2,
  "data": [
    {
      "id": 1,
      "version": 1,
      "statusSelect": 1,
      "registrationNumberPreliminaryInformation": "",
      "$t:arrivalLocation.name": "МПТП ТОРУГАРТ",
      "arrivalLocation.name": "MPTP TORUGART",
      "piType": 1,
      "createdOn": "2023-01-14T10:29:27Z",
      "piCreateDate": "2023-02-14T10:29:44Z",
      "$wkfStatus": null
    }
  ]
}
```



# 2 для юзеров
createdBy - это юзер
```json
{
  "offset": 0,
  "limit": 10,
  "fields": [
    "registrationNumberPreliminaryInformation",
    "statusSelect",
    "arrivalLocation.name",
    "piType",
    "createdOn",
    "piCreateDate"
  ],
  "sortBy": ["-createdOn"],
  "data": {
    "_domain": "self.createdBy.id = 1",
    "_domainContext": {
      "type": "1"
    }
  }
}
```
