# Изображения
Универсальная таблица не принадлежащая другим таблицам
## image
- `id` - integer - в других таблицах `image_id`
- `site_id` - integer - сайт
- `table_name` - integer - название таблицы `product`
- `unit_id` - integer - id записи
- `image_path` - string - локальный URL
- `sort` - integer - сортировка
- `alias` - string - алиас
- `state` - integer - статус
### `image` schema - структура таблицы
```json
{
"site_id": "integer",
"table_name": "string",
"unit_id": "integer",
"image_path": "string",
"sort": "integer",
"alias": "string",
"state": "integer"
}
```
## `product` - изображение товара
В базе данных храним локальную ссылку на оригинал изображения, на сайте автоматически генерируются необходимые размеры. Рекомендуем обрабатывать изображения с помощью двух пакетов: сначала [spatie/image-optimizer](https://github.com/spatie/image-optimizer) оптимизировать вес а потом [imagine/imagine](https://github.com/avalanche123/Imagine) генерировать в указанный размер.
