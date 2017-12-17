# Изображения
## image
- `id` - integer - в других таблицах `image_id`
- `site_id` - integer - сайт
- `product_id` - integer - id товара
- `image_path` - string - локальный URL
- `sort` - integer - сортировка
- `alias` - string - алиас
- `state` - integer - статус
### `image` schema - структура таблицы
```json
{
"site_id": "integer",
"product_id": "integer",
"image_path": "string",
"sort": "integer",
"alias": "string",
"state": "integer"
}
```
### `image` relations - связи
```json
"relations": {
 "product": {
  "type": "belongsTo",
  "keys": {
   "local": "product_id",
   "foreign": "id"
  }
 }
}
```
