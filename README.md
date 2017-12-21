# db.json — Структура базы данных для интернет-магазина
Проектирование структуры базы данных важнейшая задача при создании любой CMS. 

Если вам подходит наша структура базы данных, вы может использовать ее в своих проектах.
## Вышла [1.0.1-BETA-1](https://github.com/pllano/db.json/releases)
В нашем первом релизе [`1.0.1-BETA-1`](https://github.com/pllano/db.json/releases) проработаны 24 основные таблицы. Минимальный набор для легкого интернет-магазина.

## Наш подход к проектировании базы данных
Главное это: максимальная скорость доступа к данным и минимальное количество полей в самых запрашиваемых таблицах.
- Пример: одно числовое поле в таблице с 1 млн. записей может занимать более 50 Мб.

Му уверены в том, если возможно обойтись полем в одной таблице и не дублировать эти поля в двух таблицах, нужно поступать именно так. Мы считаем что такой подход дает более широкие возможности (хранить несколько описаний товара или несколько цен), а также не сильно уступает по скорости доступа, чем запрос конкретного `id`. Учитывая что файл `table_name.json` открывается для чтения полностью, то по скорости при наличии достаточного количества оперативной памяти нет особой разницы искать один `id` или несколько `price_id`.
- Пример: В таблице `product` мы убрали прямую связь с таблицами: 
[description](https://github.com/pllano/db.json/blob/master/db/description.md), 
[seo](https://github.com/pllano/db.json/blob/master/db/seo.md), 
[og](https://github.com/pllano/db.json/blob/master/db/og.md),
[price](https://github.com/pllano/db.json/blob/master/db/price.md)

Необходимо максимально группировать данные с потенциально большим объемом. 
- Пример: Тексты, Картинки - одна таблица текстов и одна таблица картинок для всей базы данных.

## Мы очень верим в то что вы поможете ее усовершенствовать !
### Использование в API Shop
- Скачайте файл [db.json](https://github.com/pllano/db.json/blob/master/db.json) отредактируйте его если вы хотите внести свои дополнения.
- Скопируйте файл в папку `ваша_бд`/`core`/ и база данных [api-json-db](https://github.com/pllano/api-json-db) или [API Shop](https://github.com/pllano/api-shop) автоматически создаст новые таблицы.
### Поддерживаемые типы данных в db.json
- `boolean` — Логический тип `true` или `false`
- `integer` — Целое число
- `double` — Число с плавающей точкой
- `string` — Строка
- `text` — Текст (Строка в которой разрешены символы `html`)
- `datetime` — Дата (Строка с проверкой на соответствие формату: `0000-00-00 00:00`)

### Параметр `relations`
`relations` - Очень важный параметр запроса позволяющий получать в ответе необходимые данные из других связанных ресурсов.

Используется четыри символа: `'` `.` `,` `:`

Сами ресурсы перечисляем через точку `'product'.'user'.'user_data'.'address'` экранируя одинарными кавычками
```
"relations" => "'product'.'user'.'user_data'.'address'"
```

Если необходимо запросить конкретные данные указываем их через двоеточие `'user:phone'` если нужно несколько через запятую `'product:type_id,brand_id,serie_id,articul'`

```
"relations" => "'product:type_id,brand_id,serie_id,articul'.'user:phone'.'address:street_id'"
```

## Структура базы состоит из 24 основных таблиц
#### Глобальные
- [`site`](https://github.com/pllano/db.json/blob/master/db/site.md) - Конфигурация сайта
- [`localization`](https://github.com/pllano/db.json/blob/master/db/localization.md) - Список языков
- [`language`](https://github.com/pllano/db.json/blob/master/db/language.md) - Мультиязычность

#### Товары
- [`category`](https://github.com/pllano/db.json/blob/master/db/category.md) - Категории
- [`product`](https://github.com/pllano/db.json/blob/master/db/product.md) - Товары
- [`type`](https://github.com/pllano/db.json/blob/master/db/type.md) - Типы товара
- [`brand`](https://github.com/pllano/db.json/blob/master/db/brand.md) - Бренды
- [`serie`](https://github.com/pllano/db.json/blob/master/db/serie.md) - Серии товара
- [`images`](https://github.com/pllano/db.json/blob/master/db/images.md) - Изображения
- [`seo`](https://github.com/pllano/db.json/blob/master/db/seo.md) - SEO тексты
- [`description`](https://github.com/pllano/db.json/blob/master/db/description.md) - Описания и тексты
- [`price`](https://github.com/pllano/db.json/blob/master/db/price.md) - Прайс-листы продавца для вывода на сайте
- [`params`](https://github.com/pllano/db.json/blob/master/db/params.md) - Свойства товара
#### Пользователи
- [`role`](https://github.com/pllano/db.json/blob/master/db/role.md) - Роли пользователей
- [`user`](https://github.com/pllano/db.json/blob/master/db/user.md) - Пользователи
- [`user_data`](https://github.com/pllano/db.json/blob/master/db/user_data.md) - Данные пользователя
- [`contact`](https://github.com/pllano/db.json/blob/master/db/contact.md) - Контактные данные
- [`address`](https://github.com/pllano/db.json/blob/master/db/address.md) - Адреса
#### Корзина
- [`currency`](https://github.com/pllano/db.json/blob/master/db/currency.md) - Валюты
- [`cart`](https://github.com/pllano/db.json/blob/master/db/cart.md) - Корзина
- [`order`](https://github.com/pllano/db.json/blob/master/db/order.md) - Заказы
- [`pay`](https://github.com/pllano/db.json/blob/master/db/pay.md) - Оплаты
#### Контент
- [`article`](https://github.com/pllano/db.json/blob/master/db/article.md) - Статьи
- [`article_category`](https://github.com/pllano/db.json/blob/master/db/article_category.md) - Категории статей

## В разработке еще 70+ дополнительных таблиц
#### Глобальные
- [`menu`](https://github.com/pllano/db.json/blob/master/db/menu.md) - Меню
- [`account`](https://github.com/pllano/db.json/blob/master/db/account.md) - Счета
- [`corporation`](https://github.com/pllano/db.json/blob/master/db/corporation.md) - Юридические лица
#### Цены на сайте
- [`seller`](https://github.com/pllano/db.json/blob/master/db/seller.md) - Конфигурация продавца
- [`price_rule`](https://github.com/pllano/db.json/blob/master/db/price_rule.md) - Ценовые правила продавца
#### Поставщики и Прайс-листы
- [`price_list`](https://github.com/pllano/db.json/blob/master/db/price_list.md) - Прайс-листы
- [`price_list_rule`](https://github.com/pllano/db.json/blob/master/db/price_list_rule.md) - Ценовые правила
- [`supplier`](https://github.com/pllano/db.json/blob/master/db/supplier.md) - Поставщики
- [`supplier_currency`](https://github.com/pllano/db.json/blob/master/db/supplier_currency.md) - Курсы валют поставщиков
- [`supplier_account`](https://github.com/pllano/db.json/blob/master/db/supplier_account.md) - Юр. лица поставщиков (связь с таблицей account)
#### Свойства товаров
- [`property_product`](https://github.com/pllano/db.json/blob/master/db/property_product.md) - Свойства товара
- [`property`](https://github.com/pllano/db.json/blob/master/db/property.md) - Настройки и связи набора и списка свойств
- [`property_set`](https://github.com/pllano/db.json/blob/master/db/property_set.md) - Наборы свойств
- [`property_list`](https://github.com/pllano/db.json/blob/master/db/property_list.md) - Список свойств
- [`property_value`](https://github.com/pllano/db.json/blob/master/db/property_value.md) - Значения свойств
#### Отзывы
При создании отзыва автоматически создается Тикет, что дает возможность проконтролировать реакцию персонала на отзывы клиентов.
- [`review`](https://github.com/pllano/db.json/blob/master/db/review.md) - Отзывы и обзоры
- [`comment`](https://github.com/pllano/db.json/blob/master/db/comment.md) - Коментарии
- [`rating`](https://github.com/pllano/db.json/blob/master/db/rating.md) - Рейтинги: отзывов, коментарией итд.
#### Адреса
- База адресов может быть покупная или собираться автоматически в процессе работы сайта
- [`location`](https://github.com/pllano/db.json/blob/master/db/location.md) - База адресов
- [`country`](https://github.com/pllano/db.json/blob/master/db/country.md) - Страна
- [`region`](https://github.com/pllano/db.json/blob/master/db/region.md) - Область (регион)
- [`postal_code`](https://github.com/pllano/db.json/blob/master/db/postal_code.md) - Почтовый индекс
- [`city`](https://github.com/pllano/db.json/blob/master/db/city.md) - Город (населенный пункт)
- [`district`](https://github.com/pllano/db.json/blob/master/db/district.md) - Район города
- [`street`](https://github.com/pllano/db.json/blob/master/db/street.md) - Улица
#### Товары
- [`complect`](https://github.com/pllano/db.json/blob/master/db/complect.md) - Комплекты: Товар состоит из ...
- [`buytogether`](https://github.com/pllano/db.json/blob/master/db/buytogether.md) - Вместе дешевле
- [`relevance`](https://github.com/pllano/db.json/blob/master/db/relevance.md) - Релевантность, Популярность, Рейтинг
#### Маркетинг
- [`customer`](https://github.com/pllano/db.json/blob/master/db/customer.md) - Клиенты
- [`promo_code`](https://github.com/pllano/db.json/blob/master/db/promo_code.md) - Промо коды
- [`discount_card`](https://github.com/pllano/db.json/blob/master/db/discount_card.md) - Дисконтные карты
- [`special_offer`](https://github.com/pllano/db.json/blob/master/db/special_offer.md) - Специальные предложения
- [`proposals`](https://github.com/pllano/db.json/blob/master/db/proposals.md) -  Предложения
#### ERP
- [`person`](https://github.com/pllano/db.json/blob/master/db/person.md) - Сотрудники компании, поставщиков итд.
- [`invoice`](https://github.com/pllano/db.json/blob/master/db/invoice.md) - Счета
- [`invoice_product`](https://github.com/pllano/db.json/blob/master/db/invoice_product.md) - Товары в счетах
- [`invoice_product_status`](https://github.com/pllano/db.json/blob/master/db/invoice_product_status.md) - Статусы товаров
- [`contract`](https://github.com/pllano/db.json/blob/master/db/contract.md) - Договора
- [`payment`](https://github.com/pllano/db.json/blob/master/db/payment.md) - Платежи
- [`payment_type`](https://github.com/pllano/db.json/blob/master/db/payment_type.md) - Типы платежей
- [`payment_resource`](https://github.com/pllano/db.json/blob/master/db/payment_resource.md) - Ресурсы платежей
- [`delivery`](https://github.com/pllano/db.json/blob/master/db/delivery.md) - Доставка
- [`delivery_options`](https://github.com/pllano/db.json/blob/master/db/delivery_options.md) - Способы доставки
- [`reclamation`](https://github.com/pllano/db.json/blob/master/db/reclamation.md) - Рекламации
- [`bill`](https://github.com/pllano/db.json/blob/master/db/bill.md) - Приходные накладные
- [`bill_move`](https://github.com/pllano/db.json/blob/master/db/bill_move.md) - Накладные перемещения
- [`bill_product`](https://github.com/pllano/db.json/blob/master/db/bill_product.md) - Товары в приходных накладных
- [`inventarization`](https://github.com/pllano/db.json/blob/master/db/inventarization.md) - Инвентаризация
- [`inventarization_item`](https://github.com/pllano/db.json/blob/master/db/inventarization_item.md) - Товары в инвентаризации
#### Логи и история
- [`history_order`](https://github.com/pllano/db.json/blob/master/db/history_order.md) - История заказов
- [`history_invoice`](https://github.com/pllano/db.json/blob/master/db/history_invoice.md) - История счетов
- [`history_product`](https://github.com/pllano/db.json/blob/master/db/history_product.md) - История товаров
- [`history_payment`](https://github.com/pllano/db.json/blob/master/db/history_payment.md) - История платежей
- [`error`](https://github.com/pllano/db.json/blob/master/db/error.md) - Лог ошибок
- [`redirect`](https://github.com/pllano/db.json/blob/master/db/redirect.md) - Редиректы
#### API
- [`api`](https://github.com/pllano/db.json/blob/master/db/api.md) - Ключи доступа к API
- [`api_request`](https://github.com/pllano/db.json/blob/master/db/api_request.md) - Запросы к API
- [`api_response`](https://github.com/pllano/db.json/blob/master/db/api_response.md) - Ответы сервисов на запрос к ихним API
#### Тикет система - Связь
- [`ticket`](https://github.com/pllano/db.json/blob/master/db/ticket.md) - Основная таблица тикет системы
- [`ticket_category`](https://github.com/pllano/db.json/blob/master/db/ticket_category.md) - Категории тикетов
- [`ticket_status`](https://github.com/pllano/db.json/blob/master/db/ticket_status.md) - Статусы и связи тикетов
- [`ticket_message`](https://github.com/pllano/db.json/blob/master/db/ticket_message.md) - Сообщения
- [`message`](https://github.com/pllano/db.json/blob/master/db/message.md) - Сообщения
- [`question`](https://github.com/pllano/db.json/blob/master/db/question.md) - Вопросы с сайта
#### Подписки и рассылки (email, sms итд.)
- [`subscription`](https://github.com/pllano/db.json/blob/master/db/subscription.md) - Подписки на рассылки
- [`sending`](https://github.com/pllano/db.json/blob/master/db/sending.md) - Рассылки
- [`sending_set`](https://github.com/pllano/db.json/blob/master/db/sending_set.md) - Настройки рассылок
- [`sending_statistic`](https://github.com/pllano/db.json/blob/master/db/sending_statistic.md) - Статистика рассылок
#### Боты и машинное обучение
- [`bot`](https://github.com/pllano/db.json/blob/master/db/bot.md) - Типы и настройки ботов
- [`chat_bot`](https://github.com/pllano/db.json/blob/master/db/chat_bot.md) - Бот роутер - через него проходит общение между ботами и пользователями
- [`support_bot`](https://github.com/pllano/db.json/blob/master/db/support_bot.md) - Бот автоматически отвечает на популярные вопросы до покупки
- [`service_bot`](https://github.com/pllano/db.json/blob/master/db/service_bot.md) - Бот автоматически отвечает на популярные вопросы после покупки
- [`search_bot`](https://github.com/pllano/db.json/blob/master/db/search_bot.md) - Бот помогающий в поиске по сайту
- [`view_bot`](https://github.com/pllano/db.json/blob/master/db/view_bot.md) - Бот на основании интересов пользователя предлагает товары
- [`seller_bot`](https://github.com/pllano/db.json/blob/master/db/seller_bot.md) - Бот продавец-консультант
- [`storage_bot`](https://github.com/pllano/db.json/blob/master/db/storage_bot.md) - Бот отвечающий по наличию товара
- [`order_bot`](https://github.com/pllano/db.json/blob/master/db/order_bot.md) - Бот дает информацию по заказам
- [`archive`](https://github.com/pllano/db.json/blob/master/db/archive.md) - Общий архив информации для всех ботов

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

### Использование в MySql
#### Пример скрипта на PHP для создания таблиц в базе MySQL из файла [db.json](https://github.com/pllano/db.json/blob/master/db.json)
```php
$uri_db = "db.json";
if (file_exists($uri_db)){
    // Загрузить файл db.json
    $db = json_decode(file_get_contents($uri_db), true);
    if (count($db) >= 1) {
        // Подключаетесь к базе
        $link = mysqli_connect($host, $user, $password, $database) or die("Ошибка " . mysqli_error($link));
        if (!$link) {exit;}
    
        foreach($db as $table){
            // Если существует поле table
            if (isset($table["table"])) {
                if (count($table["schema"]) >= 1 && $table["action"] == "create") {
                    $row = ""; 
                    foreach($table["schema"] as $key => $value){
                        if (isset($key) && isset($value)) {
                            if ($key != "id" && preg_match("[a-z0-9_]", $key)) {
                              if ($value == "boolean" || $value == "string" || 
                                $value == "integer" || $value == "double") {
                                // Конвертируем тип
                                $value = str_replace("boolean", "CHAR( 5 ) NOT NULL DEFAULT ''", $value);
                                $value = str_replace("text", "TEXT NOT NULL DEFAULT ''", $value);
                                $value = str_replace("datetime", "DATETIME NOT NULL", $value);
                                $value = str_replace("string", "VARCHAR( 255 ) NOT NULL DEFAULT ''", $value);
                                $value = str_replace("integer", "INT( 11 ) NOT NULL DEFAULT '0'", $value);
                                $value = str_replace("double", "FLOAT( 11, 2 ) NOT NULL DEFAULT '0.00'", $value);
                                $row .= ", ".$key." ".$value;
                            } else {
                                echo "название поля или тип данных не определены";
                            }
                              } else {
                                  echo $key." не прошел проверку preg_match [a-z0-9_]";
                              }
                        } else {
                            echo "value у ".$key." должен иметь один из типов: boolean, string, integer, double";
                        }
                    }
                    
                    if (!mysql_query("SELECT * FROM `".$table["table"]."`")){
                        // Создаем таблицу
                        $query ="CREATE TABLE IF NOT EXISTS ".$table["table"]."(
                            id INT( 11 ) UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY".$row."
                            )";
                    } else {
                        // Обновляем существующую таблицу
                        $query ="ALTER TABLE ".$table["table"]." 
                            CHANGE id INT( 11 ) UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY".$row;
                    }
                    // Отправляем запрос
                    mysqli_query($link, $query) or die("Ошибка " . mysqli_error($link));
                    
                } else {
                    echo "У ".$table["table"]." отсутствует schema или action != create";
                }
            } else {
                echo "Название одной из таблиц не определено";
            }
        }
        // Закрываем соединение с БД
        mysqli_close($link);
        echo "Создание таблиц прошло успешно";
    return true;
    } else {
        echo "Таблицы в файле db.json не найдены";
        return false;
    }
} else {
    echo "По указанному пути ".$uri_db." файл не найден";
    return false;
}
```
При желании можно дописать автоматическое создание индексов и связей.

При очень больших таблицах (свыше 1 млн. записей) мы предлагаем разбивать таблицу на несколько таблиц.

## Идеи
Разбивка таблицы на несколько таблиц по указанному лимиту записей
### Описание идеи: 
- Ставим лимит для одного файла 100.000 записей
- `table_name` - первая таблица содержит в 10 раз меньше записей чем выставлено в лимите, это самые часто запрашиваемые данные, база индексирует по полю score количеству запросов. Доступ к самым популярным данным всегда будет минимум в 10 раз быстрее чем к менее популярным.
- `table_name_1` - содержит от `id`=1 до `id`=100000
- `table_name_2` - содержит от `id`=100001 до `id`=200000
- Записи не смещаются вверх при удалении и `id`=100002 не может попасть в таблицу `table_name_1` даже если в таблице останеться 1000 записей.
- Мы всегда знаем в какой таблице запись с конкретным id.
- Зная последний id мы всегда знаем сколько у нас таблиц.

<a name="feedback"></a>
## Поддержка, обратная связь, новости

Пишите нам на почту open.source@pllano.com

Вы можете оставлять свои предложения и пожелания в [issues](https://github.com/pllano/db.json/issues), или вы нашли баг в db.json загляните в [issues](https://github.com/pllano/db.json/issues), возможно, про него мы уже знаем и скоро исправим. Если нет, лучше всего сообщить о нём там.

За новостями вы можете следить по
[коммитам](https://github.com/pllano/db.json/commits/master) в этом репозитории.
[RSS](https://github.com/pllano/db.json/commits/master.atom).

Лицензия db.json
-------
The MIT License (MIT). Please see [LICENSE](https://github.com/pllano/db.json/blob/master/LICENSE) for more information.
 
