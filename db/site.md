# Мультисайтовость
Если вы планируете реализовывать мультисайтовость необходимо в каждой таблице добавить поле  `site_id`
## site - Конфигурация и настройки системы
- `id` - integer - технический id
- `site_id` - integer - id сайта
- `state` - integer - Выкл. = 0 или Вкл. = 1
- `authorize` - integer - доступный всем 0 или только зарегестрированным 1
- `cookie_consent` - string - Согласие с cookie. По умолчанию 0
- `http_protocol` - string - по умолчанию `https`
- `robots` - string - по умолчанию `index, follow` вывод `<meta name="robots" content="index, follow">`
- `uri` - string - URL сайта в формате `example.com`
- `name` - string - заглавие сайта `<h1></h1>`
- `title` - string - выводится `<title></title>`
- `keywords` - string - выводится `<meta name="keywords" content="">`
- `description` - string - выводится `<meta name="description" content="">`
- `icon` - string - по умолчанию `<link rel="icon" href="favicon.ico">`
- `lang` - string - по умолчанию `<html lang="ru">`
- `logo_url` - string - URL логотипа. По умолчанию `/images/jogo.jpg`
- `logo_title` - string - текст для `alt` картинки и `title` ссылки
- `copyright` - string - текст для copyright. По умолчанию `""`
- `template` - string - название шаблона. По умолчанию `/themes/templates/template`
- `country_id` - integer - код страны. По умолчанию `1` = `UA`
- `currency_id` - integer - валюта. По умолчанию `1` = `UAH`, `грн.`
- `prefix_invoice` - string - Префикс в счетах. По умолчанию `APISHOP_`
- `vat_tax` - double - НДС в счетах. По умолчанию 0.00 `%`
- `alias_id` - string - второй id созданный `\Pllano\ApiShop\Core\Utility::random_alias_id();` в виде 12 случайных символов (Пример: 2fd4f3fbd83f)
 
## На рассмотрении
- `api_key` - string - Ключ доступа к API. Генерируется автоматически.
- `crypt_key` - string - Ключ шифрования API. Генерируется автоматически.

### `site` schema - структура таблицы
```json
{
"state": "integer",
"site_id": "integer",
"authorize": "integer",
"cookie_consent": "string",
"http_protocol": "string",
"robots": "string",
"uri": "string",
"name": "string",
"title": "string",
"keywords": "string",
"description": "string",
"icon": "string",
"lang": "string",
"logo_url": "string",
"logo_title": "string",
"copyright": "string",
"template": "string",
"country_id": "integer",
"currency_id": "integer",
"prefix_invoice": "string",
"vat_tax": "double",
"alias_id": "string"
}
```
### `site` schema - связи
```json
"relations": {
 "product": {
  "type": "hasMany",
  "keys": {
   "local": "site_id",
   "foreign": "site_id"
  }
 },
  "category": {
  "type": "hasMany",
  "keys": {
   "local": "site_id",
   "foreign": "site_id"
  }
 },
  "order": {
  "type": "hasMany",
  "keys": {
   "local": "site_id",
   "foreign": "site_id"
  }
 }
}
```
