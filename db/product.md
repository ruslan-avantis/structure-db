# Товар
В таблице товаров нет полей `image`, `description`, `seo`, `og`, `price` в связи с тем что эти данные выведены в отдельные таблицы 
[image](https://github.com/pllano/db.json/blob/master/db/image.md), 
[description](https://github.com/pllano/db.json/blob/master/db/description.md), 
[seo](https://github.com/pllano/db.json/blob/master/db/seo.md), 
[og](https://github.com/pllano/db.json/blob/master/db/og.md),
[price](https://github.com/pllano/db.json/blob/master/db/price.md) 
## product - Таблица товара
- `id` - integer - в других таблицах `product_id`
- `type_id` - integer - id типа товара
- `brand_id` - integer - id бренда
- `serie_id` - integer - id серии
- `articul` - string - артикул
- `name` - string - полное название товара
- `code` - integer - `GTIN` или `EAN` код
- `intro` - integer - краткое описание
- `template` - integer - индивидуальный шаблон страницы товара
- `publish_beg` - integer - дата включения
- `publish_end` - integer - дата выключения
- `mod_id` - integer - id товара родителя обеденяющего несколько товаров в группу
- `complect_id` - integer - входит в комплект `product_id` или нет `0`
- `priority` - integer - приоритет подымает в выдаче
- `authorize` - integer - товар только для зарегестрированных пользователей
- `alias` - integer - алиас
- `state` - integer - статус
### `product` schema - структура таблицы
```json
{
"type_id": "integer",
"brand_id": "integer",
"serie_id": "integer",
"articul": "string",
"name": "string",
"code": "string",
"intro": "string",
"template": "string",
"publish_beg": "string",
"publish_beg": "string",
"mod_id": "integer",
"complect_id": "integer",
"priority": "integer",
"authorize": "integer",
"alias": "integer",
"state": "integer"
}
```
