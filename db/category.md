# Категории
## category - Категории товара
- `id` - integer - в других таблицах `category_id`
- `parent_id` - integer - id родительской категории по умолчанию `0`
- `site_id` - integer - мультисайтовость
- `state` - integer - Выкл. = 0 или Вкл. = `1`
- `sort` - integer - Сортировка
- `authorize` - integer - доступный всем `0` или только зарегестрированным 1
- `only_available` - integer - =`0` выводить все товары, =1 выводить только с наличия
- `products_limit` - integer - Товаров на страницу. По умолчанию `15`
- `categories_template` - string - Шаблон категории. По умолчанию `default`
- `products_template` - string - Шаблон карточки товара в списке товаров. По умолчанию `default`
- `name` - string - заглавие `<h1></h1>`
- `title` - string - выводится `<title></title>`
- `keywords` - string - выводится `<meta name="keywords" content="">`
- `description` - string - выводится `<meta name="description" content="">`
- `image` - string - картинка категории
- `text` - string - описания категории
- `note` - string - краткое описания категории
- `robots` - string - по умолчанию `index, follow` вывод `<meta name="robots" content="index, follow">`
- `canonical` - string - выводится `<link name="canonical" content="">`
- `og_id` - og_id - Open Graph
- `seo_id` - seo_id - SEO тексты
- `alias` - string - используется при формировании URL - генерируется `\Pllano\ApiShop\Core\Utility::get_alias($str, $charset = 'UTF-8');`
- `alias_id` - string - второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
 
 ### `category` schema - структура таблицы
```json
{
"parent_id": "integer",
"site_id": "integer",
"state": "integer",
"sort": "integer",
"authorize": "integer",
"only_available": "integer",
"products_limit": "integer",
"categories_template": "string",
"products_template": "string",
"name": "string",
"title": "string",
"keywords": "string",
"description": "string",
"image": "string",
"text": "string",
"note": "string",
"robots": "string",
"canonical": "string",
"seo_id": "integer",
"og_id": "integer",
"alias": "string",
"alias_id": "string"
}
```
