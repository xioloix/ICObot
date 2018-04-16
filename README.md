# ICObot

---

Это Телеграм Бот пример токен сейла в Телеграме.
Подключайся к [CryptoMafiaMarket](https://t.me/CryptoMafiaMarket)
 
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

# Понятия и сущности

## __Пользователь__

`ProfileTelegram`

Таблица `mytelegram_profiletelegram`

Базовая учетная запись

|Свойство|Название|Описание|
|---|---|---|
|id|`id`|PK, intger|
|parent_id|`пригласитель`|FK self, intger|
|telegram_user_id|`АйДи юзера Телеграм`|intger|
|usernmae|`имя пользователя`|varchar255|
|first_name|`имя`|varchar255|
|last_name|`фамилия`|varchar255|
|address|`эфереум адрес`|varchar255|
|locale|`язык`|varchar255|
|ban|`забанен?`|bool|
|created|`создан`|timestamp|
|updated|`обновлен`|timestamp|
