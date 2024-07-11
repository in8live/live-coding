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

### Local dev server (artisan)
- Start local dev server
  ```shell
  ./artisan serve --host=0.0.0.0
  ```
- Open http://localhost:8000/ in browser

### Local dev server (vite)
- Start local dev server (see vite.config.js.example for proper configuration)
  ```shell
  npm run dev
  ```
- Open http://localhost:5173/ in browser