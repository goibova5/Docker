
## Модуль 2
# Задание 1
1.	Установить виртуальную машину на ALT Linux
2.	Установить Docker.
3.	Запустить контейнер «Hello World»
4.	Удалить контейнер.
5.	Сделать документация на github
-------

Устанавливам машину на базе ОС ALT Linux.
Обновляем вссе пакеты:
```
apt-get update
```
Устанавливаем пакет Docker:
```
apt-get install -y docker-engine
```


Запускаем Docker:
```
systemctl enable --now docker
```

Скачиваем контейнер Hello-World:

```
docker pull hello-world
```


Запускаем контейнер Hello-World:
```
docker run hello-world
```

Смотрим список контейнеров:
```
docker images
```
Останавливаем контейнер:
```
docker rm -v *ID контейнера*
```

Удаляем контейнер:
```
docker rmi *ID контейнера*
```
# Задание 2
1.На базе образа NGINX последней версии создать катомный образ с измененным файлом index.html. 
В файле должен быть заготовок H1 с вашей ФИО


2.Запустить контейнер на порту 80

-------
Установливаем nginx:
```
apt-get update
apt-get install nginx -y
```
Далее нужно запустить nginx:
```
systemctl enabled --now nginx
```
Запускаем его в docker:
```
docker pull nginx
```
Запускаем контейнер на 80 порте:
```
docker run --rm -d --anme nginx -v /data/app:/var/www/html -p 0.0.0.0:80:80 nginx
```
 И в конце проверяем запущенные контейнеры:
 ```
docker ps
```
# Задание 3

1.	Установить виртуальную машину на ALT Linux.
2.	Установить Docker.
3.	На базе образа NGINX последней версии создать кастомный образ с измененным файлом index.html. В файле должен быть заготовок H1 с вашей ФИО.
4.	Запустить контейнер на порту 80.
5.	Продемонстрировать результат преподавателю.
6.	Сделать документация на github.

------

Запускаем интерактивную оболочку в контейнере Docker с помощью docker exec с флагами -i и -t:
```
docker exec -it nginx /bin/bash
```
Чтобы начать их редактировать нужно будет заново скачать программу, которой мы пользуемся для редака файлов, а именно ```nano``` или  ```vim```:
```
apt-get update
apt-get install -y nano
```

Далее необходимо открыть файл index.html:

```
nano /usr/share/nginx/html/index.html
```

В нём меняем заголовок и, по желанию, описание:

![image](https://github.com/goibova5/Docker/assets/148867942/e8216d88-e78b-4841-8f88-da9d316c9c12)

Залание выполнено!


![image](https://github.com/goibova5/Docker/assets/148867942/22e3613c-4ed8-49a4-83bb-42fb4b8d7458)


# Задание 4

1.	Установить виртуальную машину на ALT Linux.
2.	Установить Docker.
3.	Создать образ для приложения работающего на фреймворке FastApi
4.	Запустить контейнер на порту 80.
5.	Продемонстрировать результат преподавателю.
6.	Сделать документация на github.

------
