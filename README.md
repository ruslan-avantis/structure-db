# db.json - Структуры базы данных
Мы вывели структуру базы данных для [API Shop](https://github.com/pllano/api-shop), [api-json-db](https://github.com/pllano/api-json-db), [APIS-2018](https://github.com/pllano/APIS-2018/) в отдельный репозиторий.

### Поддерживаемые типы данных в db.json
- `boolean` — Логический тип `true` или `false`
- `integer` — Целое число	
- `string` — Строковый тип
- `double` — Число с плавающей точкой

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
- `alias` - string - второй id в виде 12 случайных символов созданный `\jsonDB\Db::random_alias_id();`
- `user_data_id` - integer - id данных пользователя
- `role` - integer - роль пользователя по умолчанию `role=1` (покупатель)
- `login` - string - логин пользователя (может не использоватся) если для идентификации используются `email` и `phone`
- `password` - string - хеш пароля созданный `password_hash` проверяется `password_verify`
- `email` - string - email пользователя проверяется `filter_var($email, FILTER_VALIDATE_EMAIL);`
- `phone` - string - телефон пользователя без + в международном формате `380670000001` сначала очищается `\jsonDB\Db::phone_clean();`  потом проверяется `preg_match("/^[\+0-9\-\(\)\s]*$/", $phone);`
- `language` - string - язык выбранный пользователем по умолчанию ru
- `cookie` - string - Cookies пользователя установленные `setcookie();` зашифрованные [defuse/php-encryption](https://github.com/defuse/php-encryption)
#### user_data
- `id` - integer
- `alias` - string - второй id в виде 12 случайных символов созданный `\jsonDB\Db::random_alias_id();`
- `user_id` - integer
#### config
- `id` - integer
- `alias` - string - второй id в виде 12 случайных созданный `\jsonDB\Db::random_alias_id();`

<a name="feedback"></a>
## Поддержка, обратная связь, новости

Общайтесь с нами через почту open.source@pllano.com

Если вы нашли баг в db.json загляните в
[issues](https://github.com/pllano/db.json/issues), возможно, про него мы уже знаем и
чиним. Если нет, лучше всего сообщить о нём там. Там же вы можете оставлять свои
пожелания и предложения.

За новостями вы можете следить по
[коммитам](https://github.com/pllano/db.json/commits/master) в этом репозитории.
[RSS](https://github.com/pllano/db.json/commits/master.atom).

Лицензия db.json
-------

The MIT License (MIT). Please see [LICENSE](https://github.com/pllano/db.json/blob/master/LICENSE) for more information.

 
