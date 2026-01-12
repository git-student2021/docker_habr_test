## docker_habr_test
Try docker https://habr.com/ru/articles/963180/

1. Переходим в директорию приложения

'''cd docker_habr_test'''

2 Собираем образ с помощью docker build
docker build -t my-python-app .

3 Чтобы убедиться, что образ действительно создался, можно выполнить команду
docker images

4 Запускаем контейнер из образа с помощью docker run
docker run -d -p 8080:5000 --name my-running-app my-python-app

5 Посмотреть, что запущено
docker ps

6 Если хотите увидеть вообще все контейнеры, включая те, что были остановлены, добавьте флаг -a
docker ps -a

7 Заглянуть внутрь
docker logs my-running-app

8 Проверяем результат
[Кликаем сюда](http://localhost:8080) - Откроется в браузере.

9 Остановить контейнер
docker stop my-running-app

10 Запуск остановленного контейнера
docker  start my-running-app

11 Остановить контейнер
docker stop my-running-app

12 Удалить контейнер
docker rm my-running-app