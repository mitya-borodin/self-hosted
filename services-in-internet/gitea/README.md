# Gitea

Документация в [Install-with-docker](https://docs.gitea.com/installation/install-with-docker)

## Использование

```bash
cp docker-compose.example.yaml docker-compose.yaml

mkdir ./pg-data
```

Задаем значение переменным:

- GITEA__database__PASSWD=
- POSTGRES_PASSWORD=

```bash
docker compose up -d
```

`HOST_ADDRESS` - адрес вашего хоста в интернете или локальной сети.

Доступ из интернета к WEB GUI по адресу `http://HOST_ADDRESS:3001`, дальнейшая установка будет происходить в WEB GUI, там же создается супер пользователь и его пароль.

Остальное взаимодействие происходит через WEB GUI.

## Безопасность

Стоит запретить доступ к WEB GUI через интернет, изменив:

```yaml
    ports:
      - "127.0.0.1:3001:3000"
      - "222:22"
```

Доступ к WEB GUI получать только через тунэль.

## Кейс использования для хранения конфигураций контроллера WB

См. <https://github.com/vvzvlad/vestasync>
