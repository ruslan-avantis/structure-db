# Тексты
Универсальная таблица для текстов, не принадлежащая другим таблицам
# description - описания
- `id` - integer - технический id
- `description_id` - integer - основной id
- `site_id` - integer - сайт
- `table_name` - integer - название таблицы `product`
- `unit_id` - integer - id записи
- `text` - string - текст
- `sort` - integer - сортировка
- `state` - integer - статус
### `description` schema - структура таблицы
```json
{
"description_id": "integer",
"site_id": "integer",
"table_name": "string",
"unit_id": "integer",
"text": "string",
"sort": "integer",
"state": "integer"
}
```
