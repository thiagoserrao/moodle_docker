# Create your self-built Docker Moodle tesing environment

This repository provides a minimal Moodle testing environment based on docker compose.

![php7.4](https://img.shields.io/badge/php-7.4-orange)

## Disclaimer

This deployment is **NOT** intended for a production environment.
It is an reference implementation aimed at Moodle testers.


## How to start
1.) Clone this repository inside a folder

```sh
git clone https://github.com/thiagoserrao/moodle_docker.git
```

2.) Place your favourite moodle version inside **src/moodle**. You can get it from [moodle.org](https://download.moodle.org/releases/latest/).

3.) Install moodle via browser at http://localhost:8088

OR

via CLI:

```sh
docker exec -it docker_moodle-app  php admin/cli/install.php --lang=de --wwwroot=localhost --dataroot=/var/www/moodledata --dbtype=mariadb --dbhost=docker_moodle-db  --dbname=moodle --dbuser=moodledude --dbpass=mysecretpassword --prefix=mdl_ --fullname=moodle_minimal --shortname=moodle_minimal --adminpass=test --adminemail=admin@moodle.invalid --agree-license --non-interactive
```
