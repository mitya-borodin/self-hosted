# Mosquitto

[Официальный сайт](https://mosquitto.org)
[Докер образ](https://hub.docker.com/_/eclipse-mosquitto)
[Создание своего брокера MQTT](https://wirenboard.com/wiki/MQTT#Создание_своего_брокера_MQTT)

Для создания собственно брокера используется докер и образ сервиса.

Конфигурация была составлена из настроек указанных в документации [Создание своего брокера MQTT](https://wirenboard.com/wiki/MQTT#Создание_своего_брокера_MQTT) и знаний о настройке docker-compose файла.

## Использование

Придумываем username и password которые будут указаны в `mosquitto.pwd`.

- username будет `wirenboard`.  
- password будет `new-wirenboard-password`

```bash
touch mosquitto.pwd
```

При помощи утилиты `mosquitto_passwd -c ./mosquitto.pwd wirenboard`, создаем пароль для пользователя, нужно будет ввести его два раза, и пара username + password сохраняется в `./mosquitto.pwd`, причем пароль хранится в зашифрованном виде.

Запускаем сервис:

``` bash
docker compose up -d
```

Проверить доступность сервиса можно при помощи программы <https://mqtt-explorer.com>
