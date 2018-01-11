# Список шаблонов
## install_templates_list
- `id` - integer - технический id
- `install_templates_list_id` - integer - основной id
- `title` - string - название шаблона
- `keywords` - string - массив с ключевыми словами
- `description` - string - полное описание шаблона
- `note` - string - краткое описания шаблона
- `image` - string - картинка шаблона
- `price` - double - Цена
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`
- `score` - integer - Популярность
### `install_templates_list` schema - структура таблицы
```json
{
    "install_templates_list_id": "integer",
    "title": "string",
    "keywords": "string",
    "description": "string",
    "note": "string",
    "image": "string",
    "price": "double",
    "sort": "integer",
    "state": "integer",
    "score": "integer"
}
```
