# Счета
Мы планируем доработать данную таблицу чтобы она подходила для счетов всех видов валют и платежных систем
## account
- `id` - integer - в других таблицах `account_id`
- `default` - string - По умолчанию 1 или нет 0
- `corporation_id` -integer - Юр. лицо которому принадлежит счет
- `conditions_id` - string - id договора по умолчанию при выставлении счета
- `prefix_invoice` - string - Префикс для выписки счетов
- `payment_mode` - string - Тип счета (наличные, безналичные, online money, bitcoin итд.)
- `identification_code` - string - Идентификационный код
- `vat_id` - string - Налоговый номер
- `account_number` - string - Номер счета
- `payment_system` - string - Название Банка или платежной системы
- `bic` - string - BIC (Business Identifier Codes) - Код банка или платежной системы
- `swift` - string - SWIFT - Международный код банка или платежной системы
- `iban` - string - IBAN - счет в международном формате
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
 
