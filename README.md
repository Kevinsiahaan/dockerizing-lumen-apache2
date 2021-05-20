-mulai containers
docker-compose up -d
-build
docker-compose build

-masuk ke container lumen 
docker exec -it lumen /bin/bash
-buat aplikasi
composer create-project --prefer-dist laravel/lumen my-app

setup database di .env
APP_NAME=Lumen
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost
APP_TIMEZONE=UTC

LOG_CHANNEL=stack
LOG_SLACK_WEBHOOK_URL=

DB_CONNECTION=pgsql
DB_HOST=lumen-postgres
DB_PORT=5432
DB_DATABASE=<db-name-here>
DB_USERNAME=<db-user-here>
DB_PASSWORD=<db-user-password>

CACHE_DRIVER=file
QUEUE_CONNECTION=sync


-uncoment $app->withFacades(); di file app.php
-xdebug jika diperlukan dengan remote xdebug.remote_host=<ip-address-here>
