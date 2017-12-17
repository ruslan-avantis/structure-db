# Товар
## product - Локализация таблицей в БД
- `id` - integer - в других таблицах `language_id`
- `mod_id` - integer - id товара родителя обеденяющего группу товаров
- `type_id` - integer - id типа товара
- `brand_id` - integer - id бренда
- `serie_id` - integer - id серии
- `articul` - string - артикул
- `name` - string - полное название товара
- `code` - integer - `GTIN` или `EAN` код
- `intro` - integer - краткое описание
- `description_id` - integer
- `seo_id` - integer - eo_id - SEO плагин
- `og_id` - integer - og_id - Open Graph
- `publish_beg` - integer - дата включения
- `publish_end` - integer - дата выключения
- `priority` - integer - приоритет подымает в выдаче
- `authorize` - integer - товар только для зарегестрированных пользователей
- `alias` - integer - алиас
- `state` - integer
### `product` schema - структура таблицы
```json
{
"mod_id": "integer",
"type_id": "integer",
"brand_id": "integer",
"serie_id": "integer",
"articul": "string",
"name": "string",
"code": "string",
"intro": "string",
"description_id": "integer",
"seo_id": "integer",
"og_id": "integer",
"publish_beg": "string",
"publish_beg": "string",
"priority": "string",
"authorize": "string",
"alias": "integer",
"state": "integer"
}
```
