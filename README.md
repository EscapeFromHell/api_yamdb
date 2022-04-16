# **YaMDb Project**

### _api_yamdb_

# Описание

Проект **YaMDb** собирает **отзывы (Review)** пользователей на **произведения (Titles)**. Произведения делятся на категории: «Книги», «Фильмы», «Музыка». Список **категорий (Category)** может быть расширен администратором (например, можно добавить категорию «Изобразительное искусство» или «Ювелирка»).  

Сами произведения в **YaMDb** не хранятся, здесь нельзя посмотреть фильм или послушать музыку.  

В каждой категории есть **произведения**: книги, фильмы или музыка. Например, в категории «Книги» могут быть произведения «Винни-Пух и все-все-все» и «Марсианские хроники», а в категории «Музыка» — песня «Давеча» группы «Насекомые» и вторая сюита Баха.  

Произведению может быть присвоен **жанр (Genre)** из списка предустановленных (например, «Сказка», «Рок» или «Артхаус»). Новые жанры может создавать только администратор.  

Благодарные или возмущённые пользователи оставляют к произведениям текстовые **отзывы (Review)** и ставят произведению оценку в диапазоне от одного до десяти (целое число); из пользовательских оценок формируется усреднённая оценка произведения — **рейтинг** (целое число). На одно произведение пользователь может оставить только один отзыв.  

# Технологии

- [Python 3.8.8](https://www.python.org/downloads/release/python-388/)
- [Django 2.2.16](https://www.djangoproject.com/)
- [Django Rest Framework 3.12.4](https://www.django-rest-framework.org/)

# Установка

Клонируйте репозиторий и перейдите в него в командной строке:
```sh
git clone https://github.com/nickolaEO/api_yamdb.git
```
```sh
cd api_yamdb
```
Создайте и активируйте виртуальное окружение:
```sh
python -m venv venv
```
```sh
source venv/Scripts/activate
```
Установите зависимости из файла _requirements.txt_:
```sh
python -m pip install --upgrade pip
```
```sh
pip install -r requirements.txt
```
Выполните миграции:
```sh
python manage.py migrate
```
Запустите проект:
```sh
python manage.py runserver
```

# Примеры запросов

**GET**: http://127.0.0.1:8000/api/v1/categories/  
Пример ответа:
```json
[
  {
    "count": 0,
    "next": "string",
    "previous": "string",
    "results": [
      {
        "name": "string",
        "slug": "string"
      }
    ]
  }
]
```

**POST**: http://127.0.0.1:8000/api/v1/categories/  
Тело запроса:
```json
{
  "name": "string",
  "slug": "string"
}
```
Пример ответа:
```json
{
  "name": "string",
  "slug": "string"
}
```

**GET**: http://127.0.0.1:8000/api/v1/users/  
Пример ответа:
```json
[
  {
    "count": 0,
    "next": "string",
    "previous": "string",
    "results": [
      {
        "username": "string",
        "email": "user@example.com",
        "first_name": "string",
        "last_name": "string",
        "bio": "string",
        "role": "user"
      }
    ]
  }
]
```

## License

MIT

**Free Software**
