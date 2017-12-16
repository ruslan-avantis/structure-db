# Заказы
## order
- `id` - integer - в других таблицах `order_id`
- `site_id` - integer - сайт
- `order_type` - integer - тип заказа
- `user_id` - integer - id пользователя
- `status_id` - integer - id статус заказа
- `delivery_id` - integer - id доставки
- `adress_id` - integer - адрес доставки
- `conditions_id` - integer - id контракта
- `seller_id` - integer - id продавца
- `state` - integer - статус
- `alias_id` - string - алиас
### `order` schema - структура таблицы
```json
{
"site_id": "integer",
"order_type": "integer",
"user_id": "integer",
"status_id": "integer",
"delivery_id": "integer",
"adress_id": "integer",
"conditions_id": "integer",
"seller_id": "integer",
"state": "integer",
"alias_id": "string"
}
```
### `order` relations - связи
```json
"relations": {
 "user": {
  "type": "belongsTo",
  "keys": {
   "local": "user_id",
   "foreign": "id"
  }
 }
}
```
