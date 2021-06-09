# DemoSQLInjection
Demo project for showcasing SQL injection, PHP Laravel, Docker practices.

## Deployment with Docker
### Requirements
- Docker
- docker-compose
- Nginx (for reverse proxy, optional)

### Deployment
```bash
cp .env.example .env
# edit .env
docker-compose build
docker-compose run score_server php artisan key:generate
# copy application key (between braces) to APP_KEY in .env
docker-compose up
