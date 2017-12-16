# Мультиязычность
Мультиязычность может быть реализована двумя путями:
- Таблицей `language` в базе данных
- Файлами language.json в папке `/app/localization`

## language - Локализация таблицей в БД
- `id` - integer - в других таблицах `language_id`
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
 
