# Счета
## account
- `id` - integer - в других таблицах `account_id`
- `default` - string - По умолчанию 1 или нет 0
- `corporation_id` -integer - Юр. лицо которому принадлежит счет
- `conditions_id` - string - id договора по умолчанию при выставлении счета
- `prefix_invoice` - string - Префикс для выписки счетов
- `payment_mode` - string - Тип счета (наличные, безналичные итд.)
- `identification_code` - string - Идентификационный код
- `vat_id` - string - Налоговый номер
- `bank` - string - Название Банка
- `bic` - string - BIC (Business Identifier Codes) - Код банка
- `swift` - string - SWIFT - Международный код банка
- `account_number` - string - Номер счета
- `iban` - string - IBAN
- `state` - integer - Выкл. = 0 или Вкл. = 1
 
### `account` schema - структура таблицы
```json
{
"default": "integer",
"corporation_id": "integer",
"conditions_id": "string",
"prefix_invoice": "string",
"payment_mode": "string",
"identification_code": "string",
"vat_id": "string",
"bank": "string",
"bic": "string",
"swift": "string",
"account_number": "string",
"iban": "string",
"state": "integer"
}
```
 
