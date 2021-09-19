<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

## Description
Nestjs NATS&TCP app

## Running NATS
```bash
$ docker-compose up --build
```

Поднять NATS.
Запустить скрипты start:debug(напр.) для сервисов writer и reader.
Сообщений отправляются с момента запуска сервиса reader.

В сервисе reader предусмотрены API для остановки/включения отправки сообщений:

GET (localhost:3002)/api/sendDataOn

GET (localhost:3002)/api/sendDataFF

Также предусмотрены API для разовой отправки конкретного сообщения(DATA/FILE) выбранным транспортом(NATS/TCP).

GET (localhost:3002)/api/nats/object

GET (localhost:3002)/api/nats/file

GET (localhost:3002)/api/tcp/object

GET (localhost:3002)/api/tcp/file