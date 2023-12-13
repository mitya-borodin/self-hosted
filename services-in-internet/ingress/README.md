# Ingress powered by nginx-ls

[Nginx-ls](https://github.com/nginx-le/nginx-le)
[Dockerfile](./Dockerfile), несет функцию документации, чтобы понимать, какие файлы участвую в образе.

## Использование

```bash
docker compose up -d 
```

Необходимо изменить `A` запись на регистраторе домена, чтобы `Certbot` смог выпустить сертификаты через `Let's encrypt`.
