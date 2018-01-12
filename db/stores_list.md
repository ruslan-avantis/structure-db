# Список магазинов
## stores_list
- `id` - integer - технический id
- `stores_list_id` - integer - основной id
- `title` - string - название магазина
- `keywords` - string - массив с ключевыми словами
- `description` - string - полное описание магазина
- `note` - string - краткое описания магазина
- `image` - string - картинка магазина
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`
- `score` - integer - Популярность
### `stores_list` schema - структура таблицы
```json
{
"stores_list_id": "integer",
"title": "string",
"keywords": "string",
"description": "string",
"note": "string",
"image": "string",
"sort": "integer",
"state": "integer",
"score": "integer"
}
```
