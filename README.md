🔹 Шаг 1: Установка Django и зависимостей
📌 1. Создаем виртуальное окружение (рекомендуется)
Открываем терминал и вводим:

bash
python -m venv venv
source venv/bin/activate   # для macOS/Linux
venv\Scripts\activate      # для Windows

📌 2. Устанавливаем Django и Django REST Framework (DRF)
bash

pip install django djangorestframework

📌 3. Создаем Django-проект
bash

django-admin startproject backend
cd backend

📌 4. Запускаем сервер и проверяем работу
bash

python manage.py runserver
✅ Если всё правильно, в браузере по адресу http://127.0.0.1:8000/ откроется стартовая страница Django.

🔹 Шаг 2: Настройка базовой структуры проекта
📌 1. Создаем приложение core (основная логика)
bash

python manage.py startapp core
Теперь у нас такая структура:

bash

backend/
│── backend/          # Настройки Django
│── core/             # Наше основное приложение
│── manage.py         # Управление Django-проектом

📌 2. Добавляем core и rest_framework в settings.py
Открываем backend/settings.py и добавляем:

python

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    
    # Наше приложение - added 'core'
    'core',

    # Django REST Framework (для API) - added 'rest_framework'
    'rest_framework',
]