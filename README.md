# db.json - Структуры базы данных
Мы вывели структуру базы данных для [API Shop](https://github.com/pllano/api-shop), [api-json-db](https://github.com/pllano/api-json-db), [APIS-2018](https://github.com/pllano/APIS-2018/) в отдельный репозиторий.

### Поддерживаемые типы данных в db.json
- `boolean` — Логический тип `true` или `false`
- `integer` — Целое число	
- `string` — Строковый тип
- `double` — Число с плавающей точкой

## Префиксы таблиц и полей
Для дополнительной безопасности в начале названия таблиц или полей может быть указан префикс

Установить префиксы
```php
$db->setPrefixTable("sf"); // Установить префикс таблиц
$db->setPrefixColumn("jhbg5r"); // Установить префикс полей
```
Результат:
- `sf_user` - Таблица `user`
- `jhbg5r_login` - Поле `login`

## База / таблицы
### Список основных таблиц
#### Конфигурация
- `config` - Конфигурация системы
- `seller` - Конфигурация продавца
#### Пользователи
- `user` - Пользователи
- `user_data` - Данные пользователя
#### Тикет система - Связь с покупателем
- `tickets` - Основная таблица тикет системы
- `ticket_category` - Категории тикетов
- `tickets_status` - Статусы и связи тикетов
- `tickets_message` - Сообщения
- `messages` - Сообщения
- `question` - Вопросы с сайта
#### Боты и машинное обучение
- `chat_bot` - Бот роутер - через него проходит общение между ботами и пользователями
- `support_bot` - Бот автоматически отвечает на популярные вопросы до покупки
- `service_bot` - Бот автоматически отвечает на популярные вопросы после покупки
- `search_bot` - Бот помогающий в поиске по сайту
- `view_bot` - Бот на основании интересов пользователя предлагает товары
- `seller_bot` - Бот продавец-консультант
- `storage_bot` - Бот отвечающий по наличию товара
- `order_bot` - Бот дает информацию по заказам
- `archive` - Общий архив информации для всех ботов
#### Отзывы
При создании отзыва автоматически создается Тикет, что дает возможность проконтролировать реакцию персонала на отзывы клиентов.
- `reviews` - Отзывы
- `ratings` - Рейтинги: отзывов, коментарией итд.
#### Маркетинг
- `product_discount` - Акции и скидки
- `promo_code` - Промо коды и дисконтные карты
#### Товары
- `product` - Товары
- `product_image` - Картинки товара
- `product_description` - Описания товара
- `product_type` - Типы товара
- `brands` - Бренды
- `brand_series` - Серии товара
- `product_complect` - Комплекты: Товар состоит из ...
- `product_buytogether` - Вместе дешевле
#### Цены на сайте
- `seller_price_rule` - Ценовые правила продавца
- `price_out` - Прайс-листы продавца для вывода на сайте
#### Поставщики и Цены
- `supplier` - Поставщики
- `supplier_price_rule` - Ценовые правила поставщиков
- `price` - Прайс-листы поставщиков
#### Свойства
- `product_property` - Свойства товара
- `property` - Настройки и связи набора и списка свойств
- `property_set` - Наборы свойств
- `property_list` - Список свойств
- `property_value` - Значения свойств
#### Адреса
- `address` - Адреса
- `location` - База адресов
- Или мелкими таблицами
- `location_country` - Страна
- `location_region` - Область (регион)
- `location_city` - Город (населенный пункт)
- `location_district` - Район города
- `location_street` - Улица
#### Заказы
- `cart` - Корзина
- `orders` - Заказы
- `pay` - Платежи

### Список основных дополнительных таблиц
- `test` - Тестовая таблица

## Таблицы - детализация
### Свойства
Наша структура свойств показала себя очень хорошо при высоких нагрузках и большой посещаемости
#### `product_property` - Свойства товаров
Мы думаем над тем чтобы эту таблицу сделать двухуровневую id=product_id `{"product_id":1212, "value":[arr]}` это ускорит скорость работы в несколько раз.
- `id` - integer - id
- `product_id` - integer - id товара
- `property_id` - integer - id свойства
- `property_value_id` - integer - id значения
- `value` - string - значение
- `individual` - string - индивидуальное значение
- `state` - integer - id
#### `property` - Связи набора и списка свойств а также настройки 
- `id` - integer - id
- `property_set_id` - integer - связь с таблицей `property_set`
- `property_list_id` - integer - связь с таблицей `property_list`
- `sort` - integer
- `filter` - integer
- `multi` - integer
- `empty` - integer
- `view` - integer
- `short` - integer
- `primary` - integer
- `secondary` - integer
- `multiadmin` - integer
- `other` - integer
- `other_same` - integer
- `same` - integer
- `seo` - integer
- `mod` - integer
- `mod_view` - integer
#### `property_set` - Наборы свойств
- `id` - integer - id
- `name` - string - Название набора свойств
#### `property_list` - Список свойств
- `id` - integer - id
- `name` - string - Название свойства
- `name_set` - string - Название в наборе
- `name_filter` - string - Название в фильтрах
- `name_product` - string - Название в товаре
- `name_other` - string - Название в других
#### `property_value` - Значения свойств
- `id` - integer - id
- `value` - string - Значение свойства
- `seo` - string - Название для SEO
- `description` - string - Описание значения
- `unit` - string - ENUM (`'-'`,`'см'`,`'м'`,`'кг'`,`'г'`,`'мм'`,`'MGz'`,`'Mb'`)
- `image` - string - Картинка значения
- `alias` - string - Алиас значения
- `sort` - integer - Сортировка
- `state` - integer - Активный: 1 или 0
### Пользователь
#### user
- `id` - integer - id пользователя
- `alias_id` - string - Второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `role` - integer - Роль пользователя по умолчанию `role=1` (покупатель)
- `login` - string - Логин пользователя (может не использоватся) если для идентификации используются `email` и `phone`
- `password` - string - Хеш пароля созданный `password_hash` проверяется `password_verify`
- `email` - string - Email пользователя проверяется `filter_var($email, FILTER_VALIDATE_EMAIL);` при желании можно шифровать с помощью [defuse/php-encryption](https://github.com/defuse/php-encryption)
- `phone` - string - Телефон пользователя в международном формате `без +` `380670000001` сначала очищается `\Pllano\ApiShop\Core\Utility::phone_clean();`  потом проверяется `preg_match("/^[\+0-9\-\(\)\s]*$/", $phone);` при желании можно шифровать с помощью [defuse/php-encryption](https://github.com/defuse/php-encryption)
- `language` - string - Язык выбранный пользователем (по умолчанию ru) также хранится в `$session->language`
- `cookie` - string - Cookies пользователя установленные `setcookie();` зашифрованные [defuse/php-encryption](https://github.com/defuse/php-encryption). Для того чтобы усложнить подмену cookie и убрать лишние запросы к базе. Сначала пробуем расшифровать cookie. Если не можем расшифровать, значит идет подмена cookie. Отказываем в доступе и записываем IP адрес в черный список при повторении блокируем.
- `state` - Статус 1 активный или 0 неактивный
#### user_data - Таблица личных данных пользователей.
Эту таблицу при желании можно шифровать полностью
- `id` - integer
- `user_id` - integer - id пользователя в таблице `user`
- `alias_id` - string - Второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `state` - Статус 1 активный или 0 неактивный
### Конфигурация и настройки системы
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

 
