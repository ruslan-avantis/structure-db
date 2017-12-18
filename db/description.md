# Тексты
Универсальная таблица для текстов, не принадлежащая другим таблицам. Таблица содержащая в себе описания товаров, статьи, обзоры и все другие тексты. Тексты занимают больше всего памяти при обработке и места на диске. Для того чтобы было удобно оптимизировать мы вынесли все тексты в одну таблицу. также это таблица где может быть разрешен текст c html тегами.

# description - описания
- `id` - integer - технический id
- `description_id` - integer - основной id
- `site_id` - integer - сайт
- `table_name` - integer - название таблицы `product`, `article`
- `unit_id` - integer - id записи
- `text` - string - текст
- `sort` - integer - сортировка
- `state` - integer - статус
- `score` - integer - количество запросов
### `description` schema - структура таблицы
```json
{
"description_id": "integer",
"site_id": "integer",
"table_name": "string",
"unit_id": "integer",
"text": "string",
"sort": "integer",
"state": "integer",
"score": "string"
}
```
