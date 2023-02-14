# Axelor API

### Примичание
Статусы

| status | описание         |
|--------|------------------|
| 0      | success          |
| -1     | failure          |
| -4     | validation error |

Справочник\описание полей в теле запроса.

| name   | desc                                   |
|--------|----------------------------------------|
| model  | название модели                        |
| offset | смещение страницы                      |
| limit  | лимит пагинации                        |
| sortBy | список полей для сортировки результата |
| fields | название полей                         |

- User
  * [User registration](docs/user/Register.md)
  * [User authorization](docs/user/Auth.md)
- Records from DataBase
  * [Select records](docs/record/Select.md)
  * [Delete records](docs/record/Delete.md)
  * [Edit, Save, Update records](docs/record/OtherFunctional.md)
- 