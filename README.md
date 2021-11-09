<h1>При первом запуске проекта делаем такие комманды</h1>
<p><b>1.</b> docker-compose build</p>
<p><b>2</b>.docker-compose up -d</p>
<p><b>3</b>.docker-compose ps</p>
<p><b>4</b>composer install
<p><b>5</b>composer update
<p><b>6</b>php artisan key:generate
<hr>
<h2>Для использования миграции</h2>
<p><docker ps -a<br>
docker exec -it php-fpm sh<br>
cd /var/www/current/<br>
php artisan migrate
</p>
<h3>Дополнительные комманды</h3>
<p>8.sudo nano /etc/hosts</p>
<p>9.docker stop $(docker ps -a -q)</p>
<p>10.docker rm $(docker ps -a -q)</p>
<p>11.docker exec -it (сюда вставить название контейнера и убрать скобки) bash -l</p>
<p>12.mysql -u (сюда логин) -p(сюда пароль. Без пробелов)</p>
<h3>при ошибке There is no existing directory at "l/src/storage/logs" and it could not be created: Permission denied сделать</h3>


1. sudo chmod -R 777 . (для папки storage и всех вложенных папок)

2. php artisan route:clear

3. php artisan config:clear

4. php artisan cache:clear

ссылка на сайт на котором я брал инфу для установки laravel в docker
https://www.digitalocean.com/community/tutorials/how-to-install-and-set-up-laravel-with-docker-compose-on-ubuntu-20-04-ru

