# Валюты
## currency
- `id` - integer - в других таблицах `currency_id`
- `state` - integer - Выкл. = 0 или Вкл. = 1
- `blank` - integer - Валюта по умолчанию `UAH=1`, `USD=0`, `EUR=0`
- `name` - string - `грн.`, `EUR`, `$`
- `iso_code` - string - код `UAH`, `USD`, `EUR`
- `iso_code_num` - string - код `980`, `840`, `978`
- `sign` - string - `₴`, `€`, `$`
- `course` - string - курс в национальном банке `UAH=1.00`
- `course_br` - string - покупка `UAH=1.00`
- `course_ar` - string - продажа `UAH=1.00`
- `modified` - string - дата и время обновления курса
 
### `currency` schema - структура таблицы
```json
{
"state": "integer",
"blank": "integer",
"name": "string",
"iso_code": "string",
"iso_code_num": "string",
"sign": "string",
"course": "double",
"course_br": "double",
"course_ar": "double",
"modified": "string"
}
```
 
