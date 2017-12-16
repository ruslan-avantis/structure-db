# Корзина
## cart
- `id` - integer - в других таблицах `cart_id`
- `site_id` - integer - сайт
- `product_id` - integer - id товара
- `order_id` - integer - id заказа 
- `status_id` - integer - id статус товара
- `num` - integer - колличество товара
- `price` - double - цена товара `0.00`
- `currency_id` - integer - валюта товара
- `supplier_id` - integer - id поставщика
- `price_list_id` - integer - id в прайс-листе поставщика
- `seller_id` - integer - id продавца
- `price_id` - integer - id в прайс-листе продавца
- `state` - integer - статус
### `cart` schema - структура таблицы
```json
{
"site_id": "integer",
"product_id": "integer",
"order_id": "integer",
"status_id": "integer",
"num": "integer",
"price": "double",
"currency_id": "integer",
"supplier_id": "integer",
"price_list_id": "integer",
"seller_id": "integer",
"price_id": "integer",
"state": "integer"
}
```
### `cart` relations - связи
```json
"relations": {
 "order": {
  "type": "belongsTo",
  "keys": {
   "local": "order_id",
   "foreign": "id"
  }
 }
}
```
