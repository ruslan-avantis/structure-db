# Контент
## article - Контент
- `id` - integer - технический id
- `article_id` - integer - основной id
- `title` - string - название статьи
- `annotation` - string - краткое описание
- `description_id` - integer - текст статьи
- `seo_id` - integer - таблица seo
- `og_id` - integer - таблица og
- `image_id` - integer - таблица image
- `alias` - string - алиас для URL
- `created` - string - дата создания
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`

### `article` schema - структура таблицы
```json
{
"article_id": "integer",
"title": "string",
"annotation": "string",
"description_id": "integer",
"seo_id": "integer",
"og_id": "integer",
"image_id": "integer",
"alias": "string",
"created": "string",
"sort": "integer",
"state": "integer"
}
```
