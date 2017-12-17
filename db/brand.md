# Бренды
## brand - Бренды
- `id` - integer - технический id
- `brand_id` - integer - основной id
- `title` - string - название типа товара
- `seo_id` - integer - таблица seo
- `og_id` - integer - таблица og
- `image_id` - integer - таблица image
- `alias` - string - алиас для URL
- `related` - string - бренды с похожими товарами
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = `1`

### `brand` schema - структура таблицы
```json
{
"brand_id": "integer",
"title": "string",
"seo_id": "integer",
"og_id": "integer",
"image_id": "integer",
"alias": "string",
"related": "string",
"sort": "integer",
"state": "integer"
}
```
