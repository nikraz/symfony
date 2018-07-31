# symfony

git init

git clone https://github.com/nikraz/symfony.git

cd symfony

# Create .env file usig this schema
----------------------------------------------
###> symfony/framework-bundle ###

APP_ENV=dev

APP_SECRET=9f118bb78d5d064470490c6ca7eb22af

DATABASE_URL=mysql://{DATABASE_USER}:{DATABASE_PASSWORD}@{DATABASE_HOST}:{DATABASE_PORT}/{DATABASE_NAME}

###< doctrine/doctrine-bundle ###

AUTH0_CLIENT_ID=(Client ID on Auth0)
AUTH0_CLIENT_SECRET=(Client Secret on Auth0)
AUTH0_DOMAIN=(Domain on Auth0)
-----------------------------------------------

#create auth0 account
https://auth0.com/signup
 
In the dashboard, click Applications on the left:
Create Application
Add a name
Choose Regular Web Applications type

Configure callback URL:
In the new Auth0 Application, go to the settings tab.
Find the text box labeled Allowed Callback URLs.
Paste the following in: http://127.0.0.1:8000/auth0/callback.

Configure Auth0 Application to require usernames:
In the navigation bar find and click Connections
Then click Database
Click on Username-Password-Authentication
Toggle Requires Username to on.

Go to the Applications section again and pick your Application.

#composer install


php bin/console doctrine:database:create
php bin/console doctrine:schema:update --force
php bin/console doctrine:fixtures:load

yarn add sass-loader node-sass --dev (use only if incompatible with npm)--ignore-engines
/usr/local/bin/yarn run encore dev --watch

php bin/console server:run



