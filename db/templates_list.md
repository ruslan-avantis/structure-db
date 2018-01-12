# Список шаблонов
## templates_list
- `id` - integer - технический id
- `templates_list_id` - integer - основной id
- `title` - string - название шаблона
- `keywords` - string - массив с ключевыми словами
- `kategorie` - string - категория
- `description` - string - полное описание шаблона
- `note` - string - краткое описания шаблона
- `image` - string - картинка шаблона
- `dir` - string - папка шаблона
- `uri` - string - ссылка на дистрибутив шаблона
- `price` - double - Цена
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`
- `score` - integer - Популярность
### `templates_list` schema - структура таблицы
```json
{
    "templates_list_id": "integer",
    "title": "string",
    "keywords": "string",
    "kategorie": "string",
    "description": "string",
    "note": "string",
    "image": "string",
    "dir": "string",
    "uri": "string",
    "price": "double",
    "sort": "integer",
    "state": "integer",
    "score": "integer"
}
```
