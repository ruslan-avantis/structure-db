# Контент (Статьи, Обзоры)
## article - Контент
- `id` - integer - технический id
- `article_id` - integer - основной id
- `article_category_id` - integer - принадлежит категории
- `title` - string - название статьи
- `annotation` - string - краткое описание
- `description_id` - integer - текст статьи
- `seo_id` - integer - таблица seo
- `og_id` - integer - таблица og
- `image_id` - integer - таблица image
- `alias` - string - алиас для URL
- `created` - datetime - дата создания
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`
- `score` - integer - количество запросов
### `article` schema - структура таблицы
```json
{
"article_id": "integer",
"article_category_id": "integer",
"title": "string",
"annotation": "string",
"description_id": "integer",
"seo_id": "integer",
"og_id": "integer",
"image_id": "integer",
"alias": "string",
"created": "datetime",
"sort": "integer",
"state": "integer",
"score": "integer"
}
```
### `article` schema - связи
```json
"relations": {
"article_category": {
"type": "belongsTo",
"keys": {
"local": "article_category_id",
"foreign": "article_category_id"
}
}
}
```
