# Мультиязычность
Мультиязычность может быть реализована двумя путями:
- Таблицей `language` в базе данных
- Файлами language.json в папке `/app/localization`

## language - Локализация таблицей в БД
- `id` - integer - в других таблицах `language_id`
- `state` - integer - Выкл. = 0 или Вкл. = 1
- `ru` - string - Русский
- `ua` - string - Украинский
- `en` - string
- `de` - string
- `fr` - string
- `pl` - string
- `it` - string
- `es` - string
- `tr` - string
- `ar` - string
- `hi` - string
- `bn` - string
- `ko` - string
- `pt` - string
- `jp` - string
- `cn` - string
