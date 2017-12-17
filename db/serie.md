# Серии
## serie - Серии
- `id` - integer - технический id
- `serie_id` - integer - основной id
- `title` - string - название типа товара
- `seo_id` - integer - таблица seo
- `og_id` - integer - таблица og
- `alias` - string - алиас для URL
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`

### `serie` schema - структура таблицы
```json
{
"serie_id": "integer",
"title": "string",
"seo_id": "integer",
"og_id": "integer",
"alias": "string",
"sort": "integer",
"state": "integer"
}
```
