#Exchange Rate Service

    Our shops store all product prices in EUR. We need to show the players the prices in their local currency.

    To archive this we need to create a service to take care of currency exchange rates.

    We get the exchange rates from https://fixer.io/ (you need to create a free account for development)

    The data should be fetched and stored periodically.

    We also need an API for the shops to query the rates.

    Think simple ! We only care about USD, GBP and RUB

    Conditions of satisfaction
    the service is developed in php - choose the framework and php version which fits best for you ; )
    exchange rates for EUR to USD, GBP and RUB got fetched hourly
    exchange rates are stored in a database
    an api for querying exchange rates by currency and timerange was created
    a docker file for the service was created
    a docker-compose file to run the service in development was created


#How to start

start.prod

and wait a few minutes till the deploy complete and go to the http://php80.clean.public/

#How to connect to container

docker exec -it php80.clean.public bash -l

#How to stop

stop.prod

#Creditinal

login: root
pass:  1234

#Console command 

php bin/console app:e:p --handler=dummy --description=fixer

#RestApi

use restApi Autorize on the page http://php80.clean.public/ 


#How to install manual

#Install

    cd /opt/WWW/container.ite-ng.ru/projects/nginx/clean && git checkout TravianGamesGmbH
    
    sed -i -e 's/172.18.2.1/maria.db.public/' .env && sed -i -e 's/172.18.2.1/maria.db.public/' .env.test
    
    composer install && npm install
    
    php /opt/WWW/container.ite-ng.ru/projects/nginx/clean/bin/console c:c
    
    php /opt/WWW/container.ite-ng.ru/projects/nginx/clean/bin/console a:i --symlink
    
    php /opt/WWW/container.ite-ng.ru/projects/nginx/clean/bin/console d:d:c
    
    php /opt/WWW/container.ite-ng.ru/projects/nginx/clean/bin/console d:s:c
    
    php /opt/WWW/container.ite-ng.ru/projects/nginx/clean/bin/console fos:js-routing:dump --format=json --target=public/js/fos_js_routes.json
    
    webpack --env=prod
    
    php /opt/WWW/container.ite-ng.ru/projects/nginx/clean/bin/console fos:user:create root root@root 1234 --super-admin
    
    php bin/console evrinoma:menu:create
    
#Test App

    php vendor/phpunit/phpunit/phpunit --bootstrap tests/bootstrap.php --configuration phpunit.xml.dist tests/Functional/Controller/
    
#Test Bundle

    cd /opt/WWW/container.ite-ng.ru/projects/nginx/clean/vendor/evrinoma/exchange-rate-bundle
    
    sed -i -e 's/172.18.2.1/maria.db.public/' .env.test
    
    composer install --dev
    
    /usr/bin/php vendor/phpunit/phpunit/phpunit --bootstrap src/Tests/bootstrap.php --configuration phpunit.xml.dist src/Tests

#Source code

    **Application**
    
    https://github.com/evrinoma/clean branch TravianGamesGmbH
    
    **ExchangeRate service**
    
    https://github.com/evrinoma/ExchangeRateBundle branch master
    
    **Fetch service**
    
    https://github.com/evrinoma/FetchBundle branch master

#DevOps

    **AutoDeployer**
    https://github.com/evrinoma/dockerPublic
    
    **Docker files**
    
    MariaDB
    
    https://github.com/evrinoma/docker/blob/master/docker/db/maria/10.3.27/Dockerfile
    
    PHP80
    
    https://github.com/evrinoma/docker/blob/master/docker/php80/Dockerfile

    
