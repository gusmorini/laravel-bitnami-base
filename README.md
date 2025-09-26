## comandos:

```bash
podman run --rm -it -v ./src/:/app bitnami/laravel:latest composer install
```

```bash
cp ./src/.env.example ./src/.env
```

```dotenv
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=passwd
```

```bash
podman-compose up -d
```

```bash
podman-compose exec laravel php artisan key:generate
```

```bash
podman-compose exec laravel php artisan migrate
```

### caso algum erro de permissão

```bash
podman-compose exec laravel chmod -R 777 .
```
