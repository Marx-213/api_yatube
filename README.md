# api_yatube

![Python](https://img.shields.io/badge/Python_3.7-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Python](https://img.shields.io/badge/django_2.2.16-%23092E20?style=for-the-badge&logo=django&logoColor=white)
![Python](https://img.shields.io/badge/drf_3.12.4-%23092E20?style=for-the-badge&logo=django&logoColor=white)

Реализация API для всех моделей приложения Yatube.
Добавлено новое приложение с именем "api", вся логика реализована именно там.
Данный API должен быть доступен только аутентифицированным пользователям. Использована аутентификация по токену TokenAuthentication.
Аутентифицированный пользователь имеет возможность на изменить или удалить свой контент; в остальных случаях доступ предоставляется только для чтения. При попытке изменить чужие данные возвращается код 403 Forbidden.


### Установка
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/yandex-praktikum/api_yatube.git
``` 
Установить и активировать виртуальное окружение:
``` 
python3 -m venv env
source env/bin/activate
```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
pip install -r requirements.txt
``` 
Перейти в папку yatube_api, применить миграции и запустить сервер:
```
cd yatube_api
python3 manage.py migrate
python3 manage.py runserver
``` 
