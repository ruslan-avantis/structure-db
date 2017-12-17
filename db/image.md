# Изображения
## image
- `id` - integer - в других таблицах `image_id`
- `site_id` - integer - сайт
- `product_id` - integer - id товара
- `image_path` - string - локальный URL
- `sort` - integer - сортировка
- `alias_id` - string - id в прайс-листе продавца
- `state` - integer - второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` (Пример: 2fd4f3fbd83f)
### `image` schema - структура таблицы
```json
{
"site_id": "integer",
"product_id": "integer",
"image_path": "string",
"sort": "integer",
"alias_id": "string",
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
