# user

## `user` schema - структура таблицы
```json
{
"alias": "string",
"role": "string",
"language": "string",
"login": "string",
"password": "string",
"email": "string",
"phone": "string",
"cookie": "string",
"state": "integer"
}
```
## `user` relations - связи
```json
"relations": {
 "user_data": {
  "type": "hasMany",
  "keys": {
   "local": "id",
   "foreign": "user_id"
  }
 },
 "cart": {
  "type": "hasMany",
  "keys": {
    "local": "id",
    "foreign": "user_id"
  }
 }
}
```
