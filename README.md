<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Setup Guide</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
            background-color: #f4f4f4;
        }

        h1 {
            color: #333;
            border-bottom: 2px solid #333;
            padding-bottom: 5px;
        }

        h2 {
            color: #555;
            margin-top: 20px;
        }

        p {
            color: #777;
        }

        code {
            background-color: #f0f0f0;
            padding: 2px 5px;
            border-radius: 3px;
            font-family: "Courier New", Courier, monospace;
        }

        pre {
            background-color: #f0f0f0;
            padding: 10px;
            border-radius: 5px;
            overflow-x: auto;
        }

        a {
            color: #3498db;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <h1>Setup Guide</h1>

    <h2>Step-1: Server</h2>
    <p>
        - Install XAMPP (<a href="https://www.apachefriends.org/" target="_blank">https://www.apachefriends.org/</a>)<br>
        - Install/update Composer (<a href="https://getcomposer.org/download/" target="_blank">https://getcomposer.org/download/</a>)<br>
        - Install Laravel Installer globally (cmd: <code>composer global require laravel/installer</code>)
    </p>

    <h2>Step-2: Laravel App</h2>
    <p>
        - Create Laravel app using Laravel Installer (cmd: <code>laravel new your-app-name</code>)<br>
        - Run your app (cmd: <code>php artisan serve</code>)<br>
        - Create database & configure it into .env file<br>
        <strong>Example:</strong>
        <pre>
            DB_CONNECTION=mysql
            DB_HOST=your-host
            DB_PORT=your-port-number
            DB_DATABASE=your-database-name
            DB_USERNAME=your-username
            DB_PASSWORD=your-password
        </pre>
        - Database migrations (cmd: <code>php artisan migrate</code>)
    </p>

    <h2>Step-3: Shopify App</h2>
    <p>
        - Create Shopify app at Shopify Partner
    </p>

    <h2>Step-4: Laravel-Shopify Package</h2>
    <p>
        - Laravel-Shopify package (<a href="https://github.com/Kyon147/laravel-shopify/wiki/Installation" target="_blank">https://github.com/Kyon147/laravel-shopify/wiki/Installation</a>)<br>
        - Install it into Laravel app (cmd: <code>composer require kyon147/laravel-shopify</code>)<br>
        - Create configuration file in Laravel app (cmd: <code>php artisan vendor:publish --tag=shopify-config</code>)<br>
        - Configure Shopify app credentials into .env file<br>
        <strong>Example:</strong>
        <pre>
            SHOPIFY_APP_NAME="your-app-name"
            SHOPIFY_API_KEY="your-app-api-key"
            SHOPIFY_API_SECRET="your-app-api-secret-key"
        </pre>
    </p>

    <h2>Step-5: Ngrok</h2>
    <p>
        - Login/Signup (<a href="https://ngrok.com/" target="_blank">https://ngrok.com/</a>)<br>
        - Install (cmd: <code>choco install ngrok</code>)<br>
        - Add Authtoken (cmd: <code>ngrok config add-authtoken your-token</code>)<br>
        - Create new domain (<a href="https://dashboard.ngrok.com/cloud-edge/domains" target="_blank">https://dashboard.ngrok.com/cloud-edge/domains</a>)<br>
        - Start tunnel (cmd: <code>ngrok http --domain=your-ngrok-domain your-port-number</code>)
    </p>

    <h2>Step-6: App URL Setup in Shopify</h2>
    <p>
        - Documentation (<a href="https://github.com/Kyon147/laravel-shopify/wiki/Installation#shopify-app" target="_blank">https://github.com/Kyon147/laravel-shopify/wiki/Installation#shopify-app</a>)<br>
        - Setup app URL: <code>https://your-ngrok-tunneling-url/</code><br>
        - Setup redirection URL: <code>https://your-ngrok-tunneling-url/authenticate</code>
    </p>

    <h2>Step-7: Configure Route & Model</h2>
    <p>
        - Setup route & blade (<a href="https://github.com/Kyon147/laravel-shopify/wiki/Installation" target="_blank">https://github.com/Kyon147/laravel-shopify/wiki/Installation</a>)<br>
        - Setup model
    </p>

    <h2>Step-8: Install App into Shopify Store</h2>
    <p>
        - Install app
    </p>

</body>
</html>
