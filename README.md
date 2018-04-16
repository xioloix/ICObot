# ICObot
---
Это Телеграм Бот пример токен сейла в Телеграме. 
---

## Системные требования

python 2.7, MySQL, Apache, Nginx, pip, nodejs, npm.

---

## Установка и запуск проекта
* Создать каталог проекта
```
#!bash
mkdir ~/my_project 
```
* Зайти в каталог проекта
```
#!bash
cd ~/my_project 
```
* Клонировать репозиторий
```
#!bash
git clone https://github.com/ethereumcoder/ICObot.git ./
```
* Создать БД
* Скопировать файл app/config/database.php в каталог app/config/local, отредактировать этот файл, внести свои настройки БД

* Установить зависимости
```
#!bash
pip install -r requirements.txt
```
* Применить миграции
```
#!bash
python manage.py migrate
```
---

[TOC]

## __Пользователь__

`User`

Таблица `users`

Базовая учетная запись

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, intger|
|usernmae|`имя пользователя`|string|
|email|`emial`|string|
|password|`пароль`|string|
|confirmation_code|`код подтверждения`|string|
|remember_token|`remember_token`|string|
|confirmed|`одобренный`|bool|
|created_at|`создан`|timestamp|
|updated_at|`обновлен`|timestamp|

## __Роль__

`Role`

Таблица `roles`

Роли пользователей

|Свойство|Название|Описание|
|---|---|---|
|name|`название`|string|
|created_at|`создана`|timestamp|
|updated_at|`обновлена`|timestamp|

## __Категория товара__

`ProductCategory`

Таблица `product_categories`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|parent_id|`parent_id`|FK, integer|
|position|`позиция в меню`|integer|
|title|`заголовок`|string|
|slug|`адрес`|string|
|keywords|`ключевые слова`|string|
|description|`описание`|text|
|created_at|`создана`|timestamp|
|updated_at|`обновлена`|timestamp|

## __Бренд__

`Brand`

Таблица `brands`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|title|`заголовок`|string|
|description|`описание`|text|
|created_at|`создан`|timestamp|
|updated_at|`обновлен`|timestamp|

## __Класс__

`ProductClass`

Таблица `product_classes`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|title|`заголовок`|string|
|description|`описание`|text|
|created_at|`создан`|timestamp|
|updated_at|`обновлен`|timestamp|

## __Тип__

`ProductType`

Таблица `product_types`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|title|`заголовок`|string|
|description|`описание`|text|
|created_at|`создан`|timestamp|
|updated_at|`обновлен`|timestamp|

## __Коллекция__

`ProductCollection`

Таблица `product_collections`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|product_category_id|`product_category_id`|FK, integer|
|brand_id|`brand_id`|FK, integer|
|product_class_id|`class_id`|FK, integer|
|product_type_id|`type_id`|FK, integer|
|title|`заголовок`|string|
|slug|`адрес`|string|
|keywords|`ключевые слова`|string|
|description|`описание`|text|
|measure|`единица измерения`|string|
|width|`ширина`|integer|
|height|`высота`|integer|
|lgth|`длина`|integer|
|quantity_in_package|`количество в упаковке`|integer|
|life|`срок службы`|integer|
|image|`изображение`|string|
|image_alt|`alt для изображения`|string|
|image_title|`title для изображения`|string|
|home|`выводить на главную`|bool|
|created_at|`создана`|timestamp|
|updated_at|`обновлена`|timestamp|

## __Товар__

`Product`

Таблица `products`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|product_category_id|`product_category_id`|FK, integer|
|product_collection_id|`product_collection_id`|FK, integer|
|brand_id|`brand_id`|FK, integer|
|product_class_id|`class_id`|FK, integer|
|product_type_id|`type_id`|FK, integer|
|title|`заголовок`|string|
|slug|`адрес`|string|
|keywords|`ключевые слова`|string|
|description|`описание`|text|
|measure|`единица измерения`|string|
|width|`ширина`|integer|
|height|`высота`|integer|
|lgth|`длина`|integer|
|quantity_in_package|`количество в упаковке`|integer|
|life|`срок службы`|integer|
|color|`цвет`|string|
|material|`материал`|string|
|image|`изображение`|string|
|image_alt|`alt для изображения`|string|
|image_title|`title для изображения`|string|
|created_at|`создан`|timestamp|
|updated_at|`обновлен`|timestamp|

## __Новость__

`News`

Таблица `news`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|title|`заголовок`|string|
|slug|`адрес`|string|
|keywords|`ключевые слова`|string|
|description|`описание`|text|
|content|`контент`|string|
|image|`картинка`|string|
|image_alt|`alt для изображения`|string|
|image_title|`title для изображения`|string|
|state|`состояние`|boolean|
|created_at|`создана`|timestamp|
|updated_at|`обновлена`|timestamp|

## __Статья__

`Article`

Таблица `articles`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|title|`заголовок`|string|
|slug|`адрес`|string|
|keywords|`ключевые слова`|string|
|description|`описание`|text|
|content|`контент`|string|
|image|`картинка`|string|
|image_alt|`alt для изображения`|string|
|image_title|`title для изображения`|string|
|state|`состояние`|boolean|
|created_at|`создана`|timestamp|
|updated_at|`обновлена`|timestamp|

## __Вопрос-ответ__

`faq`

Таблица `faqs`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|name_author|`Имя автора вопроса`|string|
|answer|`ответ`|text|
|question|`Вопрос`|text|
|state|`состояние`|boolean|
|created_at|`создан`|timestamp|
|updated_at|`обновлен`|timestamp|

## __Статичная страница__

`page`

Таблица `pages`

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, integer|
|title|`заголовок`|string|
|keywords|`ключевые слова`|string|
|slug|`адрес`|string|
|description|`описание`|text|
|content|`контент`|string|
|image|`картинка`|string|
|image_alt|`alt для изображения`|string|
|image_title|`title для изображения`|string|
|state|`состояние`|boolean|
|created_at|`создана`|timestamp|
|updated_at|`обновлена`|timestamp|
