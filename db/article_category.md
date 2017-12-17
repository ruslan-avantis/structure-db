# Категории контента
## article_category - Контент
- `id` - integer - технический id
- `article_category_id` - integer - основной id
- `title` - string - название
- `seo_id` - integer - таблица seo
- `og_id` - integer - таблица og
- `image_id` - integer - таблица image
- `alias` - string - алиас для URL
- `created` - string - дата создания
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`

### `article_category` schema - структура таблицы
```json
{
"article_category_id": "integer",
"title": "string",
"seo_id": "integer",
"og_id": "integer",
"image_id": "integer",
"alias": "string",
"created": "string",
"sort": "integer",
"state": "integer"
}
```
