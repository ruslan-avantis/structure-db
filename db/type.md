# Типы товара
К типу товара привязывается набор свойств
## type - Типы товара
- `id` - integer - технический id
- `type_id` - integer - основной id
- `title` - string - название типа товара
- `category_id` - integer - id категории
- `property_set_id` - integer - привязка к набору свойств
- `seo_id` - integer - таблица seo
- `og_id` - integer - таблица og
- `image_id` - integer - таблица image
- `alias` - string - алиас для URL
- `related` - string - сопутствующие типы товаров
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`
- `score` - integer - количество запросов
### `category` schema - структура таблицы
```json
{
"type_id": "integer",
"title": "string",
"category_id": "integer",
"property_set_id": "integer",
"seo_id": "integer",
"og_id": "integer",
"image_id": "integer",
"alias": "string",
"related": "string",
"sort": "integer",
"state": "integer",
"score": "string"
}
```
