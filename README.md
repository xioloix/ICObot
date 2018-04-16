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
