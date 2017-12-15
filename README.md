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
#### Глобальные
- `site` - Конфигурация сайта
- `currency` - Валюты
- `language` - Мультиязычность
- `category` - Категории
- `menu` - Меню

- `account` - Счета
- `corporation` - Юридические лица
- `delivery` - Способы доставки
#### Пользователи
- `user` - Пользователи
- `user_data` - Данные пользователя
- `user_role` - Роли пользователей
- `address` - Адреса пользователей системы
- `person` - Контактные лица (поставщиков итд.)
#### Корзина
- `cart` - Корзина
- `order` - Заказы
- `pay` - Оплаты
#### ERP
- `invoice` - Счета
- `invoice_product` - Товары в заказе
- `invoice_product_status` - Статусы товаров
- `contract` - Договора
- `payment` - Платежи
- `payment_type` - Типы платежей
- `reclamation` - Рекламации
- `bill` - Приходные накладные
- `bill_move` - Накладные перемещения
- `bill_product` - Товары в приходных накладных
- `inventarization` - Инвентаризация
- `inventarization_item` - Товары в инвентаризации
#### Логи и история
- `history_order` - История заказов
- `history_invoice` - История счетов
- `history_product` - История товаров
- `history_payment` - История платежей
#### API
- `api` - Ключи доступа к API
- `api_request` - Запросы к API
- `api_response` - Ответы сервисов на запрос к ихним API
#### SEO
- `seo` - SEO тексты
- `error` - Лог ошибок
- `redirect` - Редиректы
#### Контент
- `article` - Статьи
- `article_category` - Категории статей
#### Конфигурация продавца
- `seller` - Конфигурация продавца
#### Тикет система - Связь с покупателем
- `ticket` - Основная таблица тикет системы
- `ticket_category` - Категории тикетов
- `ticket_status` - Статусы и связи тикетов
- `ticket_message` - Сообщения
- `message` - Сообщения
- `question` - Вопросы с сайта
#### Подписки и рассылки (email, sms итд.)
- `subscription` - Подписки на рассылки
- `sending` - Рассылки
- `sending_set` - Настройки рассылок
- `sending_contact` - Контакты
- `sending_statistic` - Статистика рассылок
#### Боты и машинное обучение
- `bot` - Типы и настройки ботов
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
- `review` - Отзывы и обзоры
- `comment` - Коментарии
- `rating` - Рейтинги: отзывов, коментарией итд.
#### Маркетинг
- `discount` - Акции и скидки
- `customer` - Клиенты
- `promo_code` - Промо коды
- `discount_card` - Дисконтные карты
- `special_offer` - Специальные предложения
- `proposals` -  Предложения
#### Товары
- `product` - Товары
- `image` - Картинки товара
- `description` - Описания товара
- `type` - Типы товара
- `brand` - Бренды
- `serie` - Серии товара
- `complect` - Комплекты: Товар состоит из ...
- `buytogether` - Вместе дешевле
- `relevance` - Релевантность, Популярность, Рейтинг
#### Цены на сайте
- `price` - Прайс-листы продавца для вывода на сайте
- `price_rule` - Ценовые правила продавца
#### Прайс-листы
- `price_list` - Прайс-листы
- `price_list_rule` - Ценовые правила
#### Поставщики и Цены
- `supplier` - Поставщики
- `supplier_currency` - Курсы валют поставщиков
- `supplier_account` - Юр. лица поставщиков (связь с таблицей account)
#### Свойства
- `product_property` - Свойства товара
- `property` - Настройки и связи набора и списка свойств
- `property_set` - Наборы свойств
- `property_list` - Список свойств
- `property_value` - Значения свойств
#### Адреса
- `location` - База адресов
- База адресов может иметь очень большой размер. У нас разбира на отдельные таблицы.
- `country` - Страна
- `region` - Область (регион)
- `city` - Город (населенный пункт)
- `district` - Район города
- `street` - Улица
### Список основных дополнительных таблиц


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
- `role_id` - integer - Роль пользователя по умолчанию `role=1` (покупатель)
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
- `ticketed` - integer - Имеет доступ к Тикет системе
- `admin_access` - integer - Имеет доступ а админ панель
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

 
