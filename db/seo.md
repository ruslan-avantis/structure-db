# SEO
Универсальная таблица не принадлежащая другим таблицам. Таблица SEO позволяет организовать отдельный доступ для SEO специалиста. Связать индивидуальные SEO параметры можно с любой таблицей.
## seo - Таблица индивидуальных SEO параметров
- `id` - integer - технический id
- `seo_id` - integer - основной id
- `site_id` - integer - сайт
- `table_name` - integer - название таблицы `product` или `category`
- `unit_id` - integer - уникальный id записи
- `seo_h1` - string - заменит автоматически сгенерированный `<h1></h1>`
- `seo_title` - string - заменит автоматически сгенерированный `<title></title>`
- `seo_keywords` - string - заменит автоматически сгенерированный `<meta name="keywords" content="">`
- `seo_description` - string - заменит автоматически сгенерированный `<meta name="description" content="">`
- `seo_text` - string - SEO текст, обычно выводится внизу
- `robots` - string - по умолчанию `index, follow` вывод `<meta name="robots" content="index, follow">`
- `canonical` - string - выводится `<link name="canonical" content="">`
- `sitemap_xml` - integer - выводить в sitemap
- `sitemap_html` - integer - выводить в sitemap
- `hreflang` - integer
### `seo` schema - структура таблицы
```json
{
"seo_id": "integer",
"site_id": "integer",
"table_name": "string",
"unit_id": "integer",
"seo_h1": "string",
"seo_title": "string",
"seo_keywords": "string",
"seo_description": "string",
"seo_text": "string",
"robots": "string",
"canonical": "string",
"sitemap_xml": "integer",
"sitemap_html": "integer",
"hreflang": "string"
}
```
