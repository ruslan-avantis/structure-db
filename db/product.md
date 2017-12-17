# Товар
Здесь нет поля цены `price` по той причине что товар это статическое явление, а цена динамическое и у товара может быть несколько поставщиков. Цены выведены в отдельную таблицу [price](https://github.com/pllano/db.json/blob/master/db/price.md)  которая генерируется в зависимости от наличия товаров в прайс-листах поставщиков. Система не предусматривает ручного обновления цен.

В таблице товаров нет полей `image`, `description`, `seo`, `og` в связи с тем что эти данные выведены в отдельные универсальные таблицы 
[image](https://github.com/pllano/db.json/blob/master/db/image.md), 
[description](https://github.com/pllano/db.json/blob/master/db/description.md), 
[seo](https://github.com/pllano/db.json/blob/master/db/seo.md), 
[og](https://github.com/pllano/db.json/blob/master/db/og.md)

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
- `mod_id` - integer - id товара родителя объединяющего несколько товаров в группу
- `complect_id` - integer - входит в комплект `product_id` или нет `0`
- `priority` - integer - приоритет искусственно поднимает в выдаче
- `authorize` - integer - товар только для зарегистрированных пользователей
- `alias` - integer - алиас
- `state` - integer - статус
- `publish_beg` - integer - дата включения
- `publish_end` - integer - дата выключения
- `created` - integer - дата создания
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
"mod_id": "integer",
"complect_id": "integer",
"priority": "integer",
"authorize": "integer",
"alias": "integer",
"state": "integer",
"publish_beg": "string",
"publish_beg": "string",
"created": "string"
}
```
