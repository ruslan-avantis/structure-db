# Список типов магазинов
## install_stores_list - Категории товара
- `id` - integer - технический id
- `install_stores_list_id` - integer - основной id

- `name` - string - заглавие `<h1></h1>`
- `title` - string - выводится `<title></title>`
- `keywords` - string - ключевые слова (типы товаров)
- `description` - string - описание магазина
- `image` - string - картинка категории
- `text` - string - описания категории
- `note` - string - краткое описания категории
- `og_id` - og_id - Open Graph
- `seo_id` - seo_id - Таблица SEO
- `alias` - string - используется при формировании URL
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`
- `score` - integer - количество запросов
 
### `install_stores_list` schema - структура таблицы
```json
{
"install_stores_list_id": "integer",
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
"sort": "integer",
"state": "integer",
"score": "integer"
}
```
