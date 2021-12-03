# Task Escaped

# How to start

start.prod

and wait a few minutes till the deploy complete and go to the http://php80.clean.public/

#How to connect to container

docker exec -it php80.clean.public bash -l

# How to stop

stop.prod

#Creditinal

login: root
pass: 1234

# Test results

docker exec -it php80.clean.public cat /tmp/tests.txt

# Console command


# RestApi

use restApi Autorize on the page http://php80.clean.public/

# How to install manual

   ## Install

        console=cd /opt/WWW/container.ite-ng.ru/projects/nginx/clean
        git checkout SarioMarketingGmbh
        sed -i -e 's/172.18.2.1/maria.db.public/' .env
        sed -i -e 's/172.18.2.1/maria.db.public/' .env.test
        composer install
        npm install
        php bin/console c:c
        php bin/console a:i --symlink
        php bin/console d:d:c
        php bin/console d:s:c
        php bin/console fos:js-routing:dump --format=json --target=public/js/fos_js_routes.json
        webpack --env=prod
        php bin/console fos:user:create root root@root 1234 --super-admin
        php bin/console fos:user:create user user@user 1234
        php bin/console fos:user:create manager manager@manager 1234
        php bin/console fos:user:create dev deve@dev 1234
        php bin/console evrinoma:menu:create
        #Test Application
        php vendor/phpunit/phpunit/phpunit --bootstrap tests/bootstrap.php --configuration phpunit.xml.dist tests/Functional/Controller/ >> /tmp/tests.txt

   ## Test (Library) Bundle

        cd /opt/WWW/container.ite-ng.ru/projects/nginx/clean/vendor/evrinoma/vacation-bundle
        sed -i -e 's/172.18.2.1/maria.db.public/' .env.test
        composer config -g github-oauth.github.com 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
        composer install --dev
        php vendor/phpunit/phpunit/phpunit --bootstrap src/Tests/bootstrap.php --configuration phpunit.xml.dist src/Tests >> /tmp/tests.txt

# Source code

**Application**

https://github.com/evrinoma/clean branch SarioMarketingGmbh

**Vacation service**

https://github.com/evrinoma/VacationBundle branch master

# DevOps

**AutoDeployer**

https://github.com/evrinoma/dockerPublic

# Step by Step

![Login](doc/img/login.png?raw=true "Login Page")

![apidoc](doc/img/apidoc.png?raw=true "ApiDoc Page")

![vacation text](doc/img/vacation.png?raw=true "Vacation Api")
