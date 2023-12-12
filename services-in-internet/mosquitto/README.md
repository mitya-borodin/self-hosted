# Mosquitto

[Официальный сайт](https://mosquitto.org)
[Докер образ](https://hub.docker.com/_/eclipse-mosquitto)
[Создание своего брокера MQTT](https://wirenboard.com/wiki/MQTT#Создание_своего_брокера_MQTT)

Для создания собственно брокера используется докер и образ сервиса.

Конфигурация была составлена из настроек указанных в документации [Создание своего брокера MQTT](https://wirenboard.com/wiki/MQTT#Создание_своего_брокера_MQTT) и знаний о настройке docker-compose файла.

## Использование

Придумываем username и password которые будут указаны в `mosquitto.pwd`.

```bash
cp mosquitto.example.pwd mosquitto.pwd
```

Заменяем username и password, не то что придумали.

Запускаем сервис:

``` bash
docker compose up -d
```

Проверить доступность сервиса можно при помощи программы <https://mqtt-explorer.com>
