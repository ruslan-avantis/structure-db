# Мультисайтовость
## site - Конфигурация и настройки системы
- `id` - integer - в других таблицах `site_id`
- `uri` - string - URL сайта в формате `example.com`
- `name` - string - Внутреннее название сайта `Example.com`
- `logo_url` - string - URL логотипа
- `logo_title` - string - текст для `alt` картинки и `title` ссылки
- `robots` - string - по умолчанию `index, follow` вывод `<meta name="robots" content="index, follow">`
- `http_protocol` - string - по умолчанию `https`
- `authorize` - integer - Доступный всем 0 или только зарегестрированным 1
- `copyright` - string - текст для copyright
- `alias_id` - string - Второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `state` - integer - 0 или 1
