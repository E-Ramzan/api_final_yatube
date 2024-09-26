# Описание:
Данный проект - это **rest_api** для обычного блога. Благодаря сделанной системе rest_api этот проект **можно подключить к SPA приложениям** и использовать.

Технологический стек: 
- Django
- DRF (Django Rest Framework)
- Djoser
- JWT Authentication
- Pillow

# Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```bash
git clone https://github.com/Griver2006/api_final_yatube.git
```
```
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:
```bash
python3 -m venv env
```
```bash
source env/bin/activate
```

Установить зависимости из файла requirements.txt:
```bash
python3 -m pip install --upgrade pip
```
```bash
pip install -r requirements.txt
```

Выполнить миграции:
```bash
python3 manage.py migrate
```
Запустить проект:
```bash
python3 manage.py runserver
```

# Примеры
## Запросы к подпискам
POST: http://127.0.0.1:8000/api/v1/follow/
Body: 
```json
{
  "following": "following_user"
}
```

Ответ:
```json
{
  "user": "just_user",
  "following": "following_user"
}
```



## Запросы к постам
GET: http://127.0.0.1:8000/api/v1/posts/

Ответ:
```json
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}
```

GET: http://127.0.0.1:8000/api/v1/posts/{id}/

Ответ:
```json
{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2019-08-24T14:15:22Z",
  "image": "string",
  "group": 0
}
```


Итд

# Реквизиты
Автор: Элиханов Рамзан
GitHub: https://github.com/Griver2006
