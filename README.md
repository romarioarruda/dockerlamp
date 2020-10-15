# Docker LAMP

Ambiente de desenvolvimento usando `Docker Compose`.
>
Stack:

* PHP 7.4
* Apache 2.4
* Mysql 8.0
* phpMyAdmin

## Instalação

Faça o clone desse repositório e execute `docker-compose up -d`.

```shell
git clone https://github.com/romarioarruda/dockerlamp.git

cd dockerlamp/

docker-compose up -d
```

Sua stack está pronta!! Acesse `http://localhost:8081` no seu navegador.

## Configuração

_**DOCUMENT_ROOT**_

É o diretório que o Apache vai servir, nesse caso é a pasta `./public`. Coloque seus arquivos dentro desse diretório.

## Web Server

O Apache está configurado para usar a porta `8081`. você pode acessar `http://localhost:8081`.

#### Módulos do Apache

Por padrão, os seguintes módulos estão habilitados:

* rewrite
* headers

> Se desejar habilitar outros módulos, atualize o arquivo `Dockerfile`.

> IMPORTANTE: Você vai precisar fazer um novo build caso altere o Dockerfile. Para isso, basta executar `docker-compose build` e restarte os containers.

## Database

Essa stack vem com as seguintes credenciais:

_**SENHA DO ROOT**_

`/br4vu5_root/is`

_**BANCO**_

`crud_teste`

_**USUÁRIO**_

`devuser`

_**SENHA DO USUÁRIO**_

`devpass`

## PHP

A versão do PHP utilizada nessa stack é a `7.4`

#### Extensões do PHP

Por padrão, os seguintes módulos estarão habilitados:

* mysqli
* pdo_sqlite
* pdo_mysql
* mbstring
* zip
* intl
* mcrypt
* curl
* json
* iconv
* xml
* xmlrpc
* gd

> Se desejar habilitar outros módulos, atualize o arquivo `Dockerfile`.

> IMPORTANTE: Você vai precisar fazer um novo build caso altere o Dockerfile. Para isso, execute `docker-compose build` e restarte os containers.

## phpMyAdmin

O phpMyAdmin está configurado para usar a porta `8080`, com as credenciais:

http://localhost:8080/
username: `root`
password: `/br4vu5_root/is`
