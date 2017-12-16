# Юридические лица
Название компании или частного предпринимателя
## corporation
- `id` - integer - в других таблицах `corporation_id`
- `supplier_id` - integer
- `seller_id` - integer
- `address_id` - integer 
- `title` - string
- `alias_id` - string
- `state` - integer
 
### `corporation` schema - структура таблицы
```json
{
"supplier_id": "integer",
"seller_id": "integer",
"address_id": "integer",
"title": "string",
"alias_id": "string",
"state": "integer"
}
```
 
