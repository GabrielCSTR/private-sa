
# Setup Docker Para Projetos Laravel
[Desenvolvido por Zhyon Hosting](https://zyonhosting.com.br)

### Passo a passo
Clone Repositório
```sh
git clone https://github.com/especializati/setup-docker-laravel.git
```


Clone os Arquivos do Laravel
```sh
git clone https://github.com/laravel/laravel.git example-project
```


Copie os arquivos docker-compose.yml, Dockerfile e o diretório docker/ para o seu projeto
```sh
cp -r setup-docker-laravel/* example-project/
```


Crie o Arquivo .env
```sh
cd example-project/
cp .env.example .env
```


Atualizar as variáveis de ambiente do arquivo .env
```dosini
APP_NAME=EspecializaTi
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```


Acessar o container
```sh
docker-compose exec curso_x bash
```


Instalar as dependências do projeto
```sh
composer install
```


Gerar a key do projeto Laravel
```sh
php artisan key:generate
```


Acessar o projeto
[http://localhost](http://localhost)
