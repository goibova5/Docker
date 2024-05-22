
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
