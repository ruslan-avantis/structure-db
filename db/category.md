# Категории
## category - Категории товара
- `id` - integer - технический id
- `category_id` - integer - основной id
- `parent_id` - integer - id родительской категории по умолчанию `0`
- `site_id` - integer - мультисайтовость
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
- `og_id` - og_id - Open Graph
- `seo_id` - seo_id - Таблица SEO
- `alias` - string - используется при формировании URL
- `alias_id` - string - второй id в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`
- `score` - integer - количество запросов
 
### `category` schema - структура таблицы
```json
{
"category_id": "integer",
"parent_id": "integer",
"site_id": "integer",
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
"seo_id": "integer",
"og_id": "integer",
"alias": "string",
"alias_id": "string",
"sort": "integer",
"state": "integer",
"score": "integer"
}
```
