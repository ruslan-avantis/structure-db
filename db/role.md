# Роли пользователей
## role
- `id` - integer - технический id
- `role_id` - integer - в других таблицах `role_id`
- `name` - string - Название роли
- `ename` - string - Краткое название
- `iname` - string - Внутреннее название
- `sort` - integer - Сортировка
- `state` - integer - Выкл. = 0 или Вкл. = 1
- `score` - integer - количество запросов
### `role` schema - структура таблицы
```json
{
"role_id": "integer",
"name": "string",
"ename": "string",
"iname": "string",
"sort": "integer",
"state": "integer",
"score": "integer"
}
```
### `role` relations - связи
```json
"relations": {
 "user": {
  "type": "hasMany",
  "keys": {
   "local": "role_id",
   "foreign": "role_id"
  }
 }
}
```
