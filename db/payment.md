# Платежи
## payment
- `id` - integer - в других таблицах `order_id`
- `site_id` - integer - сайт
- `resource_id` - integer - идентификатор ресурса платежа
- `operator` - integer - person_id, проведший денежную операцию
- `payer_id` - integer - уникальный идентификатор источника платежа
- `payee_id` - integer - уникальный идентификатор получателя платежа
- `cell_id` - integer - уникальный идентификатор ячейки платежа
- `object` - string - `product`, `order` или `user`
- `sign` - string - знак операции `+` или `-`
- `sum` - double - сумма платежа
- `date` - string - дата проведения платежа
- `created` - string - дата создания
- `alias_id` - string - алиас
- `state` - integer - статус
### `payment` schema - структура таблицы
```json
{
"site_id": "integer",
"resource_id": "integer",
"operator": "integer",
"payer_id": "integer",
"payee_id": "integer",
"cell_id": "integer",
"object": "string",
"sign": "string",
"sum": "double",
"date": "string",
"created": "string",
"alias_id": "string",
"state": "integer"
}
```
### `payment` relations - связи
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
