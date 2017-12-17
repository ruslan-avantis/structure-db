# Тексты
Универсальная таблица не принадлежащая другим таблицам
# description - описания
- `id` - integer - в других таблицах `image_id`
- `site_id` - integer - сайт
- `table_name` - integer - название таблицы `product`
- `unit_id` - integer - id записи
- `text` - string - текст
- `sort` - integer - сортировка
- `state` - integer - статус
### `description` schema - структура таблицы
```json
{
"site_id": "integer",
"table_name": "string",
"unit_id": "integer",
"text": "string",
"sort": "integer",
"state": "integer"
}
```
