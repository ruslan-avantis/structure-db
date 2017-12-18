# Мультиязычность
Мультиязычность может быть реализована двумя путями:
- Таблицей `localization` в базе данных
- Файлами language.json в папке `/app/localization`

## localization - Локализация
- `id` - integer - технический id
- `localization_id` - integer - основной id
- `site_id` - integer - id сайта
- `state` - integer - Выкл. = 0 или Вкл. = 1
- `en` - string - English
- `ua` - string - Українська
- `ru` - string - Русский
- `be` - string - Беларускі
- `kk` - string - Қазақша
- `ka` - string - ქართული
- `de` - string - Deutsch
- `fr` - string - Français
- `pl` - string - Polski
- `it` - string - Italiano
- `es` - string - Español
- `tr` - string - Türk
- `ar` - string - العربية
- `hi` - string - हिन्दी
- `bn` - string - বাঙালি
- `pt` - string - Portugues
- `jp` - string - 日本語
 
### `localization` schema - структура таблицы
```json
{
"language_id": "integer",
"state": "integer",
"en": "string",
"ua": "string",
"ru": "string",
"be": "string",
"kk": "string",
"ka": "string",
"de": "string",
"fr": "string",
"pl": "string",
"it": "string",
"es": "string",
"tr": "string",
"ar": "string",
"hi": "string",
"bn": "string",
"pt": "string",
"jp": "string"
}
```
 
