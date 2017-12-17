# Цены
## price - Таблица цен
- `id` - integer - в других таблицах `price_id`
- `site_id` - integer - id сайта
- `product_id` - integer - id товара
- `category_id` - integer - id категории
- `price` - double - артикул
- `oldprice` - double - артикул
- `currency_id` - integer - валюта
- `pay_online` - integer - возможна оплата онлайн
- `available` - integer - количество в наличии
- `guarantee` - integer - гарантия месяцев
- `terms_of_delivery` - string - условия доставки
- `locking` - integer - запретить продажу
- `supplier_item_id` - integer - id цены в прайс-листе поставщика
- `alias_id` - string - id алиас
- `state` - integer - статус
- `created` - string - дата создания
- `modified` - string - дата изменения

### `price` schema - структура таблицы
```json
{
"site_id": "integer",
"product_id": "integer",
"category_id": "integer",
"price": "double",
"oldprice": "double",
"currency_id": "integer",
"pay_online": "integer",
"available": "integer",
"guarantee": "integer",
"terms_of_delivery": "string",
"locking": "integer",
"supplier_item_id": "integer",
"alias_id": "string",
"state": "integer",
"created": "string",
"modified": "string"
}
```







