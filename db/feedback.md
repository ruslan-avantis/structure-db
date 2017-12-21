# Обратная связь
## Ресурс `feedback`
- `id` - integer - технический id
- `feedback_id` - integer - основной id
- `title` - string - Заголовок ошибки
- `description` - string - Описание ошибки
- `uri` - string - URL запроса
- `type` - string - Тип запроса
- `param` - string - Параметры запроса
- `created` - datatime - Дата создания

### `feedback` schema - структура ресурса
```json
{
"feedback_id": "integer",
"title": "string",
"description": "string",
"uri": "string",
"type": "string",
"param": "string",
"created": "datatime"
}
```
