# Цены
## price - Таблица цен
- `id` - integer - технический id
- `price_id` - integer - основной id
- `template` - string - индивидуальный шаблон страницы товара
- `site_id` - integer - id сайта
- `product_id` - integer - id товара
- `category_id` - integer - id категории
- `price` - double - текущая цена
- `oldprice` - double - цена до (по умолчанию 0.00)
- `currency_id` - integer - валюта
- `pay_online` - integer - возможна оплата онлайн
- `available` - integer - количество в наличии
- `guarantee` - integer - гарантия месяцев
- `terms_of_delivery` - string - условия доставки
- `locking` - integer - запретить продажу
- `supplier_item_id` - integer - id цены в прайс-листе поставщика
- `alias` - string - id алиас
- `state` - integer - статус
- `created` - datetime - дата создания
- `modified` - datetime - дата изменения
- `score` - integer - количество запросов
### `price` schema - структура таблицы
```json
{
"price_id": "integer",
"template": "string",
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
"alias": "string",
"state": "integer",
"created": "string",
"modified": "string",
"score": "string"
}
```







