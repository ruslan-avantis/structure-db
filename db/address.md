# Адреса
Универсальная таблица адресов не принадлежащая другим таблицам
## address
- `id` - integer - технический id
- `contact_id` - integer - основной id
- `site_id` - integer - id сайта
- `table_name` - string - название таблицы `user_data`
- `unit_id` - integer - id записи
- `country_id` - integer - id страны
- `region_id` - integer - id региона
- `postal_code_id` - integer - id почтового кода
- `city_id` - integer - id города
- `district_id` - integer - id района
- `street_id` - integer - id улицы
- `number` - string - номер дома
- `parade` - string - парадное
- `floor` - string - этаж
- `apartment` - string - номер
- `additional` - string - дополнительно к адресу
- `note` - string - примечание
- `sort` - integer - сортировка
- `state` - integer - статус
### `address` schema - структура таблицы
```json
{
"contact_id": "integer",
"site_id": "integer",
"table_name": "string",
"unit_id": "integer",
"country_id": "integer",
"region_id": "integer",
"postal_code_id": "integer",
"city_id": "integer",
"district_id": "integer",
"street_id": "integer",
"number": "string",
"parade": "string",
"floor": "string",
"apartment": "string",
"additional": "string",
"note": "string",
"sort": "integer",
"state": "integer"
}
```
