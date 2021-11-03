# Тестовая сборка wordpress

Для сборки и запуска достаточно выполнить комманду:

```docker-compose up -d```

Для данного проекта были использованы официальные репозитории:

https://github.com/docker-library/mysql

https://github.com/docker-library/php

https://github.com/nginxinc/docker-nginx

https://github.com/docker-library/wordpress/

https://github.com/phpmyadmin/docker


Контейнеры слинкованы как named, так и bind volumes.
Связь между MySQL 8, Wordpress, PhpMyAdmin осуществляется через socket-файлы
Nginx осуществляет fastcgi-обработку через socket-файлы

После сборки на сервер пробрасывается 80-й порт.
По http://ip-адрес хоста доступен становится инсталятор Wordpress последней версии.
По http://ip-адрес/pma доступен PhpMyAdmin с запросом учетной записи и пароля для подключения к MySQL
Пароль по умолчанию на root для MySQL: SecretPassword123
