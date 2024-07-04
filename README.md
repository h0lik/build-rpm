#Установка openssl в centos - 7.9
OpenSSL-1.1.1 требуеться для установки пакета OpenSSH 9.7p1 
Скачиваем пакет openssl 
```bash
wget https://github.com/h0lik/build-rpm/raw/main/openssl/openssl-1.0.2k-19.el7.x86_64.rpm
```
Проверяем какая версия стоит в данный момент

```bash
openssl version
```
получим openssl 1.0.2
далее удалить пакет openssl удалять будет через утилиту *rpm* так как если удалить через привычный *yum remove* то он удалил все зависмые пакеты нам этого не надо 
```bash
rpm -e --nodeps "пакет openssl"
```
после чего проверим есть ли в системе openssl 
```bash
openssl version
```
как видим пакета openssl у нас нету. Перейдем в директорию с пакетом openssl и выполним команду по установки пакетов  

```bash
yum -y install ./openssl-1.0.2k-19.el7.x86_64.rpm
```

