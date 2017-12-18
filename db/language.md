# Языки
## language - Список языков
- `id` - integer - технический id
- `language_id` - integer - основной id
- `name` - string - Название языка
- `site_id` - integer - id сайта
- `state` - integer - Выкл. = 0 или Вкл. = 1
- `score` - integer - количество запросов

### `language` schema - структура таблицы
```json
{
"language_id": "integer",
"name": "string",
"site_id": "integer",
"state": "integer",
"score": "integer"
}
```
 
