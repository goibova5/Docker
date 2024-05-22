# Docker
Модуль 2

1.	Установить виртуальную машину на ALT Linux
2.	Установить Docker.
3.	Запустить контейнер «Hello World»
4.	Удалить контейнер.
5.	Сделать документация на github


1
Устанавливам машину на базе ОС ALT Linux.
Обновляем вссе пакеты:
```
apt-get update
```
2
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

3
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
4
Удаляем контейнер:
```
docker rmi *ID контейнера*
```

