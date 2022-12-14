# Laravel Microservices com RabbitMQ (micro 02)

## Requisitos
Este microservice 02 depende do microservice 01, portanto, primeiramente subir o [microservice 01](https://github.com/uesleisales/laravel-microservice-01)

### Instalação
Clonar Projeto
```sh
git clone https://github.com/uesleisales/laravel-microservice-02.git
```

Acessar o projeto
```sh
cd laravel-microservice-02
```

Criar o Arquivo .env
```sh
cp .env.example .env
```

Atualizar as variáveis de ambiente do arquivo .env
```dosini
APP_NAME=EspecializaTi
APP_URL=http://localhost:8001

DB_CONNECTION=mysql
DB_HOST=db_micro_02
DB_PORT=3306
DB_DATABASE=micro_02
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```

Subir os containers do projeto
```sh
docker-compose up -d
```

Acessar o container
```sh
docker-compose exec micro_02 bash
```

Instalar as dependências do projeto
```sh
composer install
```

Gerar a key do projeto Laravel
```sh
php artisan key:generate
```

Rodar os testes
```sh
php artisan test
```

Acessar o projeto
[http://localhost:8001](http://localhost:8001)
