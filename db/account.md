# Счета
Мы планируем доработать данную таблицу чтобы она подходила для счетов всех видов валют и платежных систем
## account
- `id` - integer - в других таблицах `account_id`
- `default` - integer - По умолчанию 1 или нет 0
- `corporation_id` -integer - Юр. лицо которому принадлежит счет
- `conditions_id` - integer - id договора по умолчанию при выставлении счета
- `prefix_invoice` - string - Префикс для выписки счетов
- `payment_mode` - string - Тип счета (наличные, безналичные, online money, bitcoin итд.)
- `identification_code` - string - Идентификационный код
- `vat_id` - string - Налоговый номер
- `merchant_code` - string - Код продавца
- `payment_account` - string - Номер счета
- `correspondent_account` - string - Корреспондентский счёт
- `payment_system` - string - Название банка или платежной системы (Payment service provider)
- `bic` - string - Банковский идентификационный код
- `swift` - string - SWIFT - Международный код банка или платежной системы
- `iban` - string - IBAN - счет в международном формате
- `state` - integer - Выкл. = 0 или Вкл. = 1
### `account` schema - структура таблицы
```json
{
"default": "integer",
"corporation_id": "integer",
"conditions_id": "integer",
"prefix_invoice": "string",
"payment_mode": "string",
"identification_code": "string",
"vat_id": "string",
"merchant_code": "string",
"payment_account": "string",
"correspondent_account": "string",
"payment_system": "string",
"bic": "string",
"swift": "string",
"iban": "string",
"state": "integer"
}
```
 
