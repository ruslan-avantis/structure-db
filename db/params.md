# `params` - Свойства товаров
Мы думаем над тем чтобы эту таблицу сделать двухуровневую id=product_id `{"product_id":1212, "value":[arr]}` это ускорит скорость работы в несколько раз.
- `id` - integer - технический id
- `param_id` - integer - основной id
- `product_id` - integer - id товара
- `field` - string - поле
- `value` - string - значение
- `individual` - string - индивидуальное значение
- `property_id` - integer - id свойства
- `property_value_id` - integer - id значения
- `state` - integer - id
- `score` - integer - количество запросов
### `property_product` schema - структура таблицы
```json
{
"param_id": "integer",
"product_id": "integer",
"field": "string",
"value": "string",
"individual": "string",
"property_id": "integer",
"property_value_id": "integer",
"state": "integer",
"score": "string"
}
```
