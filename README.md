## Setup Docker Laravel

### Passo a passo

Faça o download da versão mais recente publicada nas Tag's

Clone Repositório para dentro do seu Projeto Laravel criado recentemente
```sh
git clone https://github.com/daniloferreirasousa/setup-docker-laravel.git ./
```

Crie o Arquivo .env
```sh
cp .env.example .env
```

Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME="Nome do seu Projeto"
APP_URL=http://localhost:8001
APP_USER=user  // não usar espaços em branco
APP_UID=1000  // recomendado
```

Crie a imagem do seu Container
```sh
docker-compose build --no-cache
```

Suba os containers do projeto
```sh
docker-compose up -d
```


Acessar o container
```sh
docker-compose exec -it app bash
```


Instalar as dependências do projeto
```sh
composer install
```

Atualizar as dependências caso hajam atualizações
```sh
composer update
```


Acesse o projeto
[http://localhost:8989](http://localhost:8002)
