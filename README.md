# api_final Описание:
Проект представляет собой API для проекта yatube.
Для аутентификации использованы JWT-токены.
У неаутентифицированных пользователей доступ к API только на чтение. Исключение — эндпоинт /follow/.

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:yandex-praktikum/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

source venv/scripts/activate

```
python -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

# Примеры:
Создание юзера -  http://127.0.0.1:8000/api/v1/users/ передаём POST  запросом :
{
    "username": "name",
    "password": "password"
}

Для доступа к API необходимо получить токен:

Нужно выполнить POST-запрос http://127.0.0.1:8000/api/v1/jwt/create/ передав поля username и password. API вернет JWT-токен
