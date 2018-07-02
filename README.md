# Docker VM addresses #
#### Project URL ####
<http://192.168.99.100:8000>
#### Adminer URL ####
<http://192.168.99.100:8100>

# Useful commands #

#### bash ####
```bash
docker-compose exec php bash
docker-compose exec php php -v
```

#### Composer ####
```bash
docker-compose run composer update 
docker-compose run composer -V 
```

#### node.js/npm ####
```bash
docker-compose run node node -v
docker-compose run node npm -v
docker-compose run node npm install jquery
```

#### Symfony ####
```bash
docker-compose exec php php /var/www/symfony/bin/console cache:clear
```

#### MySQL ####
```bash
docker-compose exec db mysql -uroot -p"root"
```

#### Check CPU consumption ####
```bash
docker stats
```

#### Docker multiple machines ####
```bash
docker-machine create --driver virtualbox dev1 
@FOR /f "tokens=*" %i IN ('docker-machine env dev1') DO @%i

docker-machine create --driver virtualbox dev2 
@FOR /f "tokens=*" %i IN ('docker-machine env dev2') DO @%i
```

# Sources #
<https://github.com/maxpou/docker-symfony>

<https://stackoverflow.com/questions/38356585/multiple-websites-and-php-versions-with-docker-compose>

<https://serverfault.com/questions/819774/docker-compose-exec-composer-as-user>

<https://stackoverflow.com/questions/48127851/how-to-use-composer-with-docker-compose>

<https://github.com/nanoninja/docker-nginx-php-mysql>

<https://www.newmediacampaigns.com/blog/docker-for-php-developers>

<https://www.goodbytes.be/blog/article/docker-a-simple-example-for-a-php-mysql-setup>

<https://blog.codeship.com/using-docker-compose-for-php-development/>

<http://geekyplatypus.com/dockerise-your-php-application-with-nginx-and-php7-fpm>

<https://blog.codeship.com/docker-machine-compose-and-swarm-how-they-work-together/>