# WireGuard Easy

Документация в [WireGuard Easy](https://github.com/wg-easy/wg-easy)

## Использование

```bash
cp docker-compose.example.yaml docker-compose.yaml
```

Задаем значение переменным:

- WG_HOST=
- PASSWORD=

```bash
docker compose up -d
```

Доступ из интернета к WEB GUI по адресу `http://WG_HOST:51821`, пароль из переменной `PASSWORD`.

Остальное взаимодействие происходит через WEB GUI.

## Безопасность

Стоит запретить доступ к WEB GUI через интернет, изменив:

```yaml
    ports:
      - "51820:51820/udp"
      - "127.0.0.1:51821:51821/tcp"
```

Доступ к WEB GUI получать только через тунэль.
