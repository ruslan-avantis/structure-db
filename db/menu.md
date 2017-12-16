# Меню
## menu
- `id` - integer - в других таблицах `menu_id`
- `parent_id` -integer - id родительский пункт меню по умолчанию `0`
- `sort` - integer - Сортировка
- `roles` - string - Роли через запятую которым разрешон доступ
- `class` - string - Класс меню
- `icon` - string - Иконка
- `state` - integer - Выкл. = 0 или Вкл. = 1
 
### `menu` schema - структура таблицы
```json
{
"parent_id": "integer",
"state": "integer",
"roles": "string",
"class": "string",
"icon": "string",
"sort": "integer"
}
```
 
