Here is the rewritten README.md code in GitHub flavored markdown:

Setup Guide
Step-1: Server
Install XAMPP (https://www.apachefriends.org/)
Install/update Composer (https://getcomposer.org/download/)
Install Laravel Installer globally (cmd: composer global require laravel/installer)
Step-2: Laravel App
Create Laravel app using Laravel Installer (cmd: laravel new your-app-name)
Run your app (cmd: php artisan serve)
Create database & configure it into .env file
Example:

DB_CONNECTION=mysql
DB_HOST=your-host
DB_PORT=your-port-number
DB_DATABASE=your-database-name
DB_USERNAME=your-username
DB_PASSWORD=your-password

Database migrations (cmd: php artisan migrate)
Step-3: Shopify App
Create Shopify app at Shopify Partner
Step-4: Laravel-Shopify Package
Laravel-Shopify package (https://github.com/Kyon147/laravel-shopify/wiki/Installation)
Install it into Laravel app (cmd: composer require kyon147/laravel-shopify)
Create configuration file in Laravel app (cmd: php artisan vendor:publish --tag=shopify-config)
Configure Shopify app credentials into .env file
Example:

SHOPIFY_APP_NAME="your-app-name"
SHOPIFY_API_KEY="your-app-api-key"
SHOPIFY_API_SECRET="your-app-api-secret-key"

Step-5: Ngrok
Login/Signup (https://ngrok.com/)
Install (cmd: choco install ngrok)
Add Authtoken (cmd: ngrok config add-authtoken your-token)
Create new domain (https://dashboard.ngrok.com/cloud-edge/domains)
Start tunnel (cmd: ngrok http --domain=your-ngrok-domain your-port-number)

Step-6: App URL Setup in Shopify
Documentation (https://github.com/Kyon147/laravel-shopify/wiki/Installation#shopify-app)
Setup app URL: https://your-ngrok-tunneling-url/
Setup redirection URL: https://your-ngrok-tunneling-url/authenticate
Step-7: Configure Route & Model
Setup route & blade (https://github.com/Kyon147/laravel-shopify/wiki/Installation)
Setup model
Step-8: Install App into Shopify Store
Install app
