# Оплаты
## pay
- `id` - integer - технический id
- `pay_id` - integer - основной id
- `site_id` - integer - сайт
- `user_id` - integer - user_id пользователь выполнивший операцию
- `order_id` - integer - id заказа
- `payment_type` - string - тип платежа
- `payment_system` - string - название банка или платежной системы
- `sign` - string - знак операции `+` или `-`
- `sum` - double - сумма платежа `0.00`
- `date` - datetime - дата проведения платежа `2017-11-15 18:35`
- `created` - datetime - дата создания `2017-11-15 18:35`
- `alias` - string - алиас
- `state` - integer - статус `0` или `1`
- `score` - integer - количество запросов
### `pay` schema - структура таблицы
```json
{
"pay_id": "integer",
"site_id": "integer",
"user_id": "integer",
"order_id": "integer",
"payment_type": "string",
"payment_system": "string",
"sign": "string",
"sum": "double",
"date": "datetime",
"created": "datetime",
"alias": "string",
"state": "integer",
"score": "integer"
}
```
### `pay` relations - связи
```json
"relations": {
 "user": {
  "type": "belongsTo",
  "keys": {
   "local": "user_id",
   "foreign": "pay_id"
  }
 },
  "order": {
  "type": "belongsTo",
  "keys": {
   "local": "order_id",
   "foreign": "pay_id"
  }
 }
}
```
