# Local PHP playground

## How to use
- Install docker
- Compose
  ```shell
  docker compose up
  ```
- Get into fpm container
  ```shell
  docker exec -ti -w /srv lc_php-fpm bash
  ```
- Initiate new laravel project
- Start local dev server
  ```shell
  ./artisan serve --host=0.0.0.0
  ```
- Open http://127.0.0.1:8000/ in browser