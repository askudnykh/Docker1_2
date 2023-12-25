Задание Docker 2

В settings.py в ALLOWED_HOSTS записаны "localhost", "127.0.0.1", а также внесены изменения в DATABASES для работы с sqlite3
Обновлен файл requirements.txt: pip freeze>requirements.txt
Создан файл Dockerfile
Создан файл .dockerignore, в котором указаны файлы, которые не нужно копировать в образ
Для того чтобы создать контейнер для REST API сервера нужно выполнить команду (из директории проекта): docker build -t django_project .
Для запуска контейнера нужно выполнить команду:
run --name=django_test -d -p 8000:8000 django_project
Для проверки работоспособности можно получить список продуктов (GET-запрос) здесь: http://localhost:8000/api/v1/products/, 
Или отправить запрос из файла requests-examples.http.
