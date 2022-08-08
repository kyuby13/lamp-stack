# lamp-stack
Install LAMP Stack -> Apache Mysql PHP PhpMyadmin
# Jalankan docker
docker-compose up -d
# Hasil docker ps
[root@myansible lamp]# docker ps

CONTAINER ID   IMAGE                         COMMAND                  CREATED          STATUS         PORTS                                   NAMES

d00218648efd   lamp_web-server               "docker-php-entrypoi…"   23 seconds ago   Up 7 seconds   0.0.0.0:8080->80/tcp, :::8080->80/tcp   lamp_web-server_1

7e97af19738d   mysql:8.0.19                  "docker-entrypoint.s…"   23 seconds ago   Up 8 seconds   3306/tcp, 33060/tcp                     lamp_mysql-server_1

f2a01fcedfc7   phpmyadmin/phpmyadmin:5.0.1   "/docker-entrypoint.…"   23 seconds ago   Up 7 seconds   0.0.0.0:5000->80/tcp, :::5000->80/tcp   lamp_phpmyadmin_1
# Akses phpmyadmin
http://ipaddr:5000

user : root

pass :  secret
# Akses web
http://ipaddr:8080

# Jika muncul error
Connection failed: SQLSTATE[HY000] [1049] Unknown database 'app1'

Silahkan buat databases app1 lewat phpmyadmin

