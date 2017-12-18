# Контакты
Универсальная таблица не принадлежащая другим таблицам
## contact
- `id` - integer - технический id
- `contact_id` - integer - основной id
- `site_id` - integer - id сайта
- `table_name` - string - название таблицы `user_data`
- `unit_id` - integer - id записи
- `type` - string - тип контакта `email`, `tel`, `phone`, `site`
- `value` - string - значение 1
- `value_plus` - string - дополнительное значение
- `sort` - integer - сортировка
- `state` - integer - статус
- `score` - integer - количество запросов
### `contact` schema - структура таблицы
```json
{
"contact_id": "integer",
"site_id": "integer",
"table_name": "string",
"unit_id": "integer",
"type": "string",
"value": "string",
"value_plus": "string",
"sort": "integer",
"state": "integer",
"score": "integer"
}
```
