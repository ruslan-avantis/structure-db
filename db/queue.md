# Очередь запросов
## `queue`
- `id` - integer
- `resource` - string - Название ресурса
- `resource_id` - integer - id записи
- `request` - string - Тип запроса `POST` `PUT` `PATCH` `DELETE`
- `request_body` - string - Тело запроса в виде массива кодированное base64_encode
### `queue` schema - структура таблицы
```json
{
"resource": "string",
"resource_id": "integer",
"request": "string",
"request_body": "string"
}
```
