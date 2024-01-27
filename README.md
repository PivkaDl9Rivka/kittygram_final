https://github.com/PivkaDl9Rivka/kittygram_final/actions/workflows/main.yml

## Описание
Проект Kittygram даёт возможность пользователям поделиться фотографиями и достижениями своих любимых котиков. Зарегистрированные пользователи могут создавать, просматривать, редактировать и удалять свои записи.
Проект был создан для тренировки запуска проектов в контейнерах docker и использования систем интеграции и доставки кода (CI/CD) для автоматического деплоя. В данной работе был использован GitHub Action. 


## Teхнологии 
*Python
*Django
*Djangorestframework
*Djoser
*Gunicorn
*pytest
*Docker
*React (frontend)

К проекту подключена база PostgreSQL.Предусмотрена автоматическая упаковка частей проекта(backend, frontend, nginx, db) в образы с помощью Docker и размещение их в удаленном репозитории на DockerHub, а также автоматизация деплоя на удаленный сервер с помощью GitHub actions. На удаленном сервере установлена операционная система Ubuntu. Перед деплоем предусмотрено автоматическое тестирование backend части проекта с помощью pytest.

### Развертывание проекта
1. Клонировать репозиторий:
git clone https://github.com/your/repository.git
2. Создать и установить виртуальное окружение:
python -m venv venv
3. Установить зависимости:
pip install -r requirements.txt
4. Провести миграции:
python manage.py migrate
4. Запустить проект:
python manage.py runserver

## Локальный запуск проекта через Docker
1. В корневой дирректории выполните команды:
docker-compose up
docker compose exec backend python manage.py migrate
docker compose exec backend python manage.py createsuperuser
docker compose exec backend python manage.py collectstatic

## Автор
Паранин Максим