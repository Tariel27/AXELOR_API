[Back](../../Readme.md)
# Delete records

## Удаление ПИ
>DELETE http://172.104.142.164:8080/sanarip-tamga/ws/rest/:model/:id

Пример:
>DELETE http://172.104.142.164:8080/sanarip-tamga/ws/rest/com.axelor.apps.sale.db.Declaration/1

Ответ: 
```json
{
  "status": 0,
  "data": [
    {
      "id": 1,
      "$version": 1,
      "$wkfStatus": null
    }
  ]
}
```