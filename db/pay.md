# Оплаты
## pay
- `id` - integer - в других таблицах `order_id`
- `site_id` - integer - сайт
- `user_id` - integer - user_id пользователь выполнивший операцию
- `order_id` - integer - id заказа
- `payment_type` - string - тип платежа
- `payment_system` - string - название банка или платежной системы
- `sign` - string - знак операции `+` или `-`
- `sum` - double - сумма платежа `0.00`
- `date` - string - дата проведения платежа `2017-11-15 18:35`
- `created` - string - дата создания `2017-11-15 18:35`
- `alias_id` - string - алиас
- `state` - integer - статус `0` или `1`
### `pay` schema - структура таблицы
```json
{
"site_id": "integer",
"user_id": "integer",
"order_id": "integer",
"payment_type": "string",
"payment_system": "string",
"sign": "string",
"sum": "double",
"date": "string",
"created": "string",
"alias_id": "string",
"state": "integer"
}
```
### `pay` relations - связи
```json
"relations": {
 "user": {
  "type": "belongsTo",
  "keys": {
   "local": "user_id",
   "foreign": "id"
  }
 },
  "order": {
  "type": "belongsTo",
  "keys": {
   "local": "order_id",
   "foreign": "id"
  }
 }
}
```
