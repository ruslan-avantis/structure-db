# db.json - Структура базы данных интернет-магазина
Мы вывели структуру базы данных для [API Shop](https://github.com/pllano/api-shop), [api-json-db](https://github.com/pllano/api-json-db), [APIS-2018](https://github.com/pllano/APIS-2018/) в отдельный репозиторий.

Мы решили вывести 

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

### Использование в API Shop
Скачайте файл [db.json](https://github.com/pllano/db.json/blob/master/db.json) отредактируйте его если вы хотите внести свои дополнения. Скопируйте файл в папку `ваша_бд`/`core`/ API Shop автоматически создаст новые таблицы.

## База / таблицы
#### Глобальные
- [`site`](https://github.com/pllano/db.json/blob/master/db/site.md) - Мультисайтовость
- [`language`](https://github.com/pllano/db.json/blob/master/db/language.md) - Мультиязычность
- [`currency`](https://github.com/pllano/db.json/blob/master/db/currency.md) - Валюты
- [`category`](https://github.com/pllano/db.json/blob/master/db/category.md) - Категории
- [`menu`](https://github.com/pllano/db.json/blob/master/db/menu.md) - Меню
- [`account`](https://github.com/pllano/db.json/blob/master/db/account.md) - Счета
- [`corporation`](https://github.com/pllano/db.json/blob/master/db/corporation.md) - Юридические лица
- [`delivery`](https://github.com/pllano/db.json/blob/master/db/delivery.md) - Способы доставки
#### Пользователи
- [`user`](https://github.com/pllano/db.json/blob/master/db/user.md) - Пользователи 
- [`user_data`](https://github.com/pllano/db.json/blob/master/db/user_data.md) - Данные пользователя
- [`role`](https://github.com/pllano/db.json/blob/master/db/role.md) - Роли пользователей
- [`address`](https://github.com/pllano/db.json/blob/master/db/address.md) - Адреса пользователей системы
- [`person`](https://github.com/pllano/db.json/blob/master/db/person.md) - Контактные лица (поставщиков итд.)
#### Корзина
- [`cart`](https://github.com/pllano/db.json/blob/master/db/cart.md) - Корзина
- [`order`](https://github.com/pllano/db.json/blob/master/db/order.md) - Заказы
- [`pay`](https://github.com/pllano/db.json/blob/master/db/pay.md) - Оплаты
#### ERP
- [`invoice`](https://github.com/pllano/db.json/blob/master/db/invoice.md) - Счета
- [`invoice_product`](https://github.com/pllano/db.json/blob/master/db/invoice_product.md) - Товары в счетах
- [`invoice_product_status`](https://github.com/pllano/db.json/blob/master/db/invoice_product_status.md) - Статусы товаров
- [`contract`](https://github.com/pllano/db.json/blob/master/db/contract.md) - Договора
- [`payment`](https://github.com/pllano/db.json/blob/master/db/payment.md) - Платежи
- [`payment_type`](https://github.com/pllano/db.json/blob/master/db/payment_type.md) - Типы платежей
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
#### API
- [`api`](https://github.com/pllano/db.json/blob/master/db/api.md) - Ключи доступа к API
- [`api_request`](https://github.com/pllano/db.json/blob/master/db/api_request.md) - Запросы к API
- [`api_response`](https://github.com/pllano/db.json/blob/master/db/api_response.md) - Ответы сервисов на запрос к ихним API
#### SEO
- [`seo`](https://github.com/pllano/db.json/blob/master/db/seo.md) - SEO тексты
- [`error`](https://github.com/pllano/db.json/blob/master/db/error.md) - Лог ошибок
- [`redirect`](https://github.com/pllano/db.json/blob/master/db/redirect.md) - Редиректы
#### Контент
- [`article`](https://github.com/pllano/db.json/blob/master/db/article.md) - Статьи
- [`article_category`](https://github.com/pllano/db.json/blob/master/db/article_category.md) - Категории статей
#### Конфигурация продавца
- [`seller`](https://github.com/pllano/db.json/blob/master/db/seller.md) - Конфигурация продавца
#### Тикет система - Связь с покупателем
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
- [`sending_contact`](https://github.com/pllano/db.json/blob/master/db/sending_contact.md) - Контакты
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
#### Отзывы
При создании отзыва автоматически создается Тикет, что дает возможность проконтролировать реакцию персонала на отзывы клиентов.
- [`review`](https://github.com/pllano/db.json/blob/master/db/review.md) - Отзывы и обзоры
- [`comment`](https://github.com/pllano/db.json/blob/master/db/comment.md) - Коментарии
- [`rating`](https://github.com/pllano/db.json/blob/master/db/rating.md) - Рейтинги: отзывов, коментарией итд.
#### Маркетинг
- [`discount`](https://github.com/pllano/db.json/blob/master/db/discount.md) - Акции и скидки
- [`customer`](https://github.com/pllano/db.json/blob/master/db/customer.md) - Клиенты
- [`promo_code`](https://github.com/pllano/db.json/blob/master/db/promo_code.md) - Промо коды
- [`discount_card`](https://github.com/pllano/db.json/blob/master/db/discount_card.md) - Дисконтные карты
- [`special_offer`](https://github.com/pllano/db.json/blob/master/db/special_offer.md) - Специальные предложения
- [`proposals`](https://github.com/pllano/db.json/blob/master/db/proposals.md) -  Предложения
#### Товары
- [`product`](https://github.com/pllano/db.json/blob/master/db/product.md) - Товары
- [`image`](https://github.com/pllano/db.json/blob/master/db/image.md) - Картинки
- [`description`](https://github.com/pllano/db.json/blob/master/db/description.md) - Описания
- [`type`](https://github.com/pllano/db.json/blob/master/db/type.md) - Типы товара
- [`brand`](https://github.com/pllano/db.json/blob/master/db/brand.md) - Бренды
- [`serie`](https://github.com/pllano/db.json/blob/master/db/serie.md) - Серии товара
- [`complect`](https://github.com/pllano/db.json/blob/master/db/complect.md) - Комплекты: Товар состоит из ...
- [`buytogether`](https://github.com/pllano/db.json/blob/master/db/buytogether.md) - Вместе дешевле
- [`relevance`](https://github.com/pllano/db.json/blob/master/db/relevance.md) - Релевантность, Популярность, Рейтинг
#### Цены на сайте
- [`price`](https://github.com/pllano/db.json/blob/master/db/price.md) - Прайс-листы продавца для вывода на сайте
- [`price_rule`](https://github.com/pllano/db.json/blob/master/db/price_rule.md) - Ценовые правила продавца
#### Прайс-листы
- [`price_list`](https://github.com/pllano/db.json/blob/master/db/price_list.md) - Прайс-листы
- [`price_list_rule`](https://github.com/pllano/db.json/blob/master/db/price_list_rule.md) - Ценовые правила
#### Поставщики и Цены
- [`supplier`](https://github.com/pllano/db.json/blob/master/db/supplier.md) - Поставщики
- [`supplier_currency`](https://github.com/pllano/db.json/blob/master/db/supplier_currency.md) - Курсы валют поставщиков
- [`supplier_account`](https://github.com/pllano/db.json/blob/master/db/supplier_account.md) - Юр. лица поставщиков (связь с таблицей account)
#### Свойства
- [`product_property`](https://github.com/pllano/db.json/blob/master/db/product_property.md) - Свойства товара
- [`property`](https://github.com/pllano/db.json/blob/master/db/property.md) - Настройки и связи набора и списка свойств
- [`property_set`](https://github.com/pllano/db.json/blob/master/db/property_set.md) - Наборы свойств
- [`property_list`](https://github.com/pllano/db.json/blob/master/db/property_list.md) - Список свойств
- [`property_value`](https://github.com/pllano/db.json/blob/master/db/property_value.md) - Значения свойств
#### Адреса
- База адресов может быть покупная или собираемая автоматически в процессе работы сайта
- [`location`](https://github.com/pllano/db.json/blob/master/db/location.md) - База адресов
- База адресов может иметь очень большой размер. У нас разбита на отдельные таблицы.
- [`country`](https://github.com/pllano/db.json/blob/master/db/country.md) - Страна
- [`region`](https://github.com/pllano/db.json/blob/master/db/region.md) - Область (регион)
- [`city`](https://github.com/pllano/db.json/blob/master/db/city.md) - Город (населенный пункт)
- [`district`](https://github.com/pllano/db.json/blob/master/db/district.md) - Район города
- [`street`](https://github.com/pllano/db.json/blob/master/db/street.md) - Улица

### Использование в MySql
Если вам подходит наша структура базы данных, вы может использовать ее в своих проектах.
#### Создаем таблицы в MySQL
```php
if (file_exists('db.json')){
    // Загрузить файл db.json
    $db = json_decode(file_get_contents('db.json'), true);
    $count = count($db_json);
 
    if ($count >= 1) {
        // Подключаетесь к базе
        $link = mysqli_connect($host, $user, $password, $database)
            or die("Ошибка " . mysqli_error($link));
 
        foreach($db as $unit){
            // Если существует поле table
            if (isset($unit["table"]) && $unit["action"] == "create") {
                if (count($unit["schema"]) >= 1) {
                    $row = "";
                    $value = "";
                    
                    foreach($unit["schema"] as $key => $value){
                        if (isset($key) && isset($value)) {
                            if ($key != "id") {
                                // Конвертируем тип
                                $value = str_replace("boolean", "CHAR( 5 ) NOT NULL", $value);
                                $value = str_replace("string", "VARCHAR( 255 ) NOT NULL", $value);
                                $value = str_replace("integer", "INT( 11 ) NOT NULL", $value);
                                $value = str_replace("double", "FLOAT( 11, 2 ) NOT NULL", $value);
                                $row .= ", ".$key." ".$value;
                            }
                        }
                    }
                    // Формируем запрос
                    $query ="CREATE Table ".$unit["table"]."(id INT NOT NULL AUTO_INCREMENT PRIMARY KEY".$row.")";
                    // Отправляем запрос
                    $result = mysqli_query($link, $query) or die("Ошибка " . mysqli_error($link));
                }
            }
        }
 
        // Закрываем соединение с БД
        mysqli_close($link);
        echo "Создание таблиц прошло успешно";
    }
}
```

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

 
