# seo
- `id` - integer - в других таблицах `seo_id`
- `seo_h1` - string - заменит автоматически сгенерированный `<h1></h1>`
- `seo_title` - string - заменит автоматически сгенерированный `<title></title>`
- `seo_keywords` - string - заменит автоматически сгенерированный `<meta name="keywords" content="">`
- `seo_description` - string - заменит автоматически сгенерированный `<meta name="description" content="">`
- `seo_text` - string - SEO текст, обычно выводится внизу
### `seo` schema - структура таблицы
```json
{
"seo_h1": "string",
"seo_title": "string",
"seo_keywords": "string",
"seo_description": "string",
"seo_text": "string"
}
```
