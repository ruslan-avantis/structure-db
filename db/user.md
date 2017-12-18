# Пользователь
## user
- `id` - integer - технический id
- `user_id` - integer - основной id
- `role_id` - integer - Роль пользователя по умолчанию `role_id=1` (покупатель)
- `login` - string - Логин пользователя (может не использоватся) если для идентификации используются `email` и `phone`
- `password` - string - Хеш пароля созданный `password_hash` проверяется `password_verify`
- `email` - string - Email пользователя проверяется `filter_var($email, FILTER_VALIDATE_EMAIL);` при желании можно шифровать с помощью [defuse/php-encryption](https://github.com/defuse/php-encryption)
- `phone` - string - Телефон пользователя в международном формате `без +` `380670000001` сначала очищается `\Pllano\ApiShop\Core\Utility::phone_clean();`  потом проверяется `preg_match("/^[\+0-9\-\(\)\s]*$/", $phone);` при желании можно шифровать с помощью [defuse/php-encryption](https://github.com/defuse/php-encryption)
- `language` - string - Язык выбранный пользователем (по умолчанию ru) также хранится в `$session->language`
- `cookie` - string - Cookies пользователя установленные `setcookie();` зашифрованные [defuse/php-encryption](https://github.com/defuse/php-encryption). Для того чтобы усложнить подмену cookie и убрать лишние запросы к базе. Сначала пробуем расшифровать cookie. Если не можем расшифровать, значит идет подмена cookie. Отказываем в доступе и записываем IP адрес в черный список при повторении блокируем.
- `alias_id` - string - Второй id в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `state` - Статус 1 активный или 0 неактивный
- `score` - integer - количество запросов
### `user` schema - структура таблицы
```json
{
"user_id": "string",
"role_id": "string",
"login": "string",
"password": "string",
"email": "string",
"phone": "string",
"language": "string",
"cookie": "string",
"alias_id": "string",
"state": "integer",
"score": "integer"
}
```
### `user` relations - связи
```json
"relations": {
 "user_data": {
  "type": "hasMany",
  "keys": {
   "local": "role_id",
   "foreign": "user_id"
  }
 },
 "cart": {
  "type": "hasMany",
  "keys": {
    "local": "role_id",
    "foreign": "user_id"
  }
 }
}
```
