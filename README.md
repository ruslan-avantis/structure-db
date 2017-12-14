# db.json - Структуры базы данных
Мы вывели структуру базы данных для [API Shop](https://github.com/pllano/api-shop), [api-json-db](https://github.com/pllano/api-json-db), [APIS-2018](https://github.com/pllano/APIS-2018/) в отдельный репозиторий.

### Поддерживаемые типы данных в db.json
- `boolean` — Логический тип `true` или `false`
- `integer` — Целое число	
- `string` — Строковый тип
- `double` — Число с плавающей точкой

## Префиксы таблиц и полей
Для дополнительной безопасности в начале названия базы, таблиц и полей может быть указан префикс

Установить префиксы
```php
$db->setPrefixDb("jhbg"); // Установить префикс базы
$db->setPrefixTable("sf"); // Установить префикс таблиц
$db->setPrefixColumn("jhbg5r"); // Установить префикс полей
```
Пример использования: 
- `jhbg_db_name` - Префикс базы
- `sf_table_name` - Префикс таблиц
- `jhbg5r_login` - Префикс полей

## Шаблоны
Предлагайте свои варинаты структуры базы данных

## База / таблицы
### Список основных таблиц
- `config` - Конфигурация системы
- `user` - Пользователи
- `user_data` - Данные пользователя
- `cart` - Корзина
- `order` - Заказы
- `pay` - Платежи
- `product` - Товары
- `property` - Свойства
- `address` - Адреса
- `location` - База адресов
- Или мелкими таблицами
- `location_country` - Страна
- `location_region` - Область (регион)
- `location_city` - Город (населенный пункт)
- `location_district` - Район города
- `location_street` - Улица
### Список основных дополнительных таблиц
- `test` - Тестовая таблица
### Поля таблиц
#### user
- `id` - integer - id пользователя
- `alias_id` - string - Второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `role` - integer - Роль пользователя по умолчанию `role=1` (покупатель)
- `login` - string - Логин пользователя (может не использоватся) если для идентификации используются `email` и `phone`
- `password` - string - Хеш пароля созданный `password_hash` проверяется `password_verify`
- `email` - string - Email пользователя проверяется `filter_var($email, FILTER_VALIDATE_EMAIL);`
- `phone` - string - Телефон пользователя в международном формате `без +` `380670000001` сначала очищается `\Pllano\ApiShop\Core\Utility::phone_clean();`  потом проверяется `preg_match("/^[\+0-9\-\(\)\s]*$/", $phone);`
- `language` - string - Язык выбранный пользователем (по умолчанию ru) также хранится в `$session->language`
- `cookie` - string - Cookies пользователя установленные `setcookie();` зашифрованные [defuse/php-encryption](https://github.com/defuse/php-encryption). Для того чтобы усложнить подмену cookie и убрать лишние запросы к базе. Сначала пробуем расшифровать cookie. Если не можем расшифровать, значит идет подмена cookie. Отказываем в доступе и записываем IP адрес в черный список при повторении блокируем.
- `state` - Статус 1 активный или 0 неактивный
#### user_data
- `id` - integer
- `user_id` - integer - id пользователя в таблице `user`
- `alias_id` - string - Второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `state` - Статус 1 активный или 0 неактивный
#### config
- `id` - integer
- `alias_id` - string - Второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)

<a name="feedback"></a>
## Поддержка, обратная связь, новости

Общайтесь с нами через почту open.source@pllano.com

Если вы нашли баг в db.json загляните в
[issues](https://github.com/pllano/db.json/issues), возможно, про него мы уже знаем и
скоро исправим. Если нет, лучше всего сообщить о нём там. Там же вы можете оставлять свои
пожелания и предложения.

За новостями вы можете следить по
[коммитам](https://github.com/pllano/db.json/commits/master) в этом репозитории.
[RSS](https://github.com/pllano/db.json/commits/master.atom).

Лицензия db.json
-------

The MIT License (MIT). Please see [LICENSE](https://github.com/pllano/db.json/blob/master/LICENSE) for more information.

 
