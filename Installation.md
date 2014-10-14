== Install Laravel on Ubuntu

```
sudo apt-get install php5-mcrypt

sudo php5enmod mcrypt

sudo service apache2 restart

curl -sS https://getcomposer.org/installer | php
(คำสั่งข้างบนถ้ารันแล้ว มี error ประมาณว่า curl ยังไม่ install ให้รัน sudo apt-get install curl ก่อน)

sudo mv ./composer.phar /usr/bin/composer

composer global require "laravel/installer=~1.1"

cd /var/www/html

sudo ~/.composer/vendor/bin/laravel new blog (ในตัวอย่างนี้คือ project ชื่อ blog)

ls
```
แล้วดูว่ามีโฟลเดอร์ project เราแล้วหรือยัง ถ้ามีแสดงว่ามาถูกทางละ 

```
cd blog/

sudo chmod -R 775 app/

cd app

sudo chmod -R 777 storage/

```

เปิด browser แล้วพิมพ์ Your'IPorHostName/blog/public
ถ้าลงสำเร็จจะเห็นหน้า welcome ของ Laravel


