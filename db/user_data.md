# user_data - Таблица личных данных пользователей.
Эту таблицу при желании можно шифровать полностью
- `id` - integer
- `user_id` - integer - id пользователя в таблице `user`
- `ticketed` - integer - Имеет доступ к тикет системе 1 нет 0
- `admin_access` - integer - Имеет доступ а админ панель 1 нет 0
- `alias_id` - string - Второй id в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `state` - integer - Выкл. = 0 или Вкл. = 1
### `menu` schema - структура таблицы
```json
{
"user_id": "integer",
"ticketed": "integer",
"admin_access": "integer",
"alias_id": "string",
"state": "integer"
}
```
