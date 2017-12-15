# user_data - Таблица личных данных пользователей.
Эту таблицу при желании можно шифровать полностью
- `id` - integer
- `user_id` - integer - id пользователя в таблице `user`
- `alias_id` - string - Второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `ticketed` - integer - Имеет доступ к Тикет системе
- `admin_access` - integer - Имеет доступ а админ панель
- `state` - Статус 1 активный или 0 неактивный
