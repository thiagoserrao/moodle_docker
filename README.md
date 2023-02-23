# Crie seu próprio ambiente de teste Moodle no Docker

Este repositório fornece um ambiente de teste Moodle mínimo baseado no docker compose.

![php7.4](https://img.shields.io/badge/php-7.4-orange)

## AVISO

Esta implantação **NÃO** se destina a um ambiente de produção.
É uma implementação de referência destinada a testes e desenvolvimento.


## Como começar
1.) Clone este repositório dentro de uma pasta

```sh
git clone https://github.com/thiagoserrao/moodle_docker.git
```

2.) Realize o download de uma das versões do Moodle abaixo e descompacte na pasta  **src/moodle**. 

[Moodle 3.8](https://download.moodle.org/download.php/stable38/moodle-3.8.9.zip)

[Moodle 3.9](https://download.moodle.org/download.php/stable39/moodle-latest-39.zip)

[Moodle 3.10](https://download.moodle.org/download.php/stable310/moodle-3.10.11.zip)

[Moodle 3.11](https://download.moodle.org/download.php/stable311/moodle-latest-311.zip)

[Moodle 4.0](https://download.moodle.org/download.php/stable400/moodle-latest-400.zip)

3.) Instale o Moodle via navegador em http://localhost:8088

OU

via CLI:

``
docker exec -it docker_moodle-app  php admin/cli/install.php --lang=pt_br --wwwroot=localhost --dataroot=/var/www/moodledata --dbtype=mariadb --dbhost=docker_moodle-db  --dbname=moodle --dbuser=moodledude --dbpass=mysecretpassword --prefix=mdl_ --fullname=Moodle --shortname=moodle_docker --adminpass=Trocar123 --adminemail=admin@moodle.invalid --agree-license --non-interactive
``
