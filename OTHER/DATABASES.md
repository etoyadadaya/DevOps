1. Как настроить master-slave репликацию в mysql (кратко)?

<details>
  <summary>Ответ</summary>

Необходимы 2 сервера: master и slave.

1. На обеих сервера устанавливаем сервер MySQL одинаковой версии.
2. Включаем сервер базы данных на обеих серверах.
3. Настраиваем master - в `/etc/my.cnf` устанавливаем слеюущие значения:
```
# выбираем ID сервера, произвольное число, лучше начинать с 1
server-id = 1
# путь к бинарному логу
log_bin = /var/log/mysql/mysql-bin.log
# название Вашей базы данных, которая будет реплицироваться
binlog_do_db = newdatabase
```
Перезапускаем сервер базы данных.
4. Подключаемся к master серверу, создаем пользователя и назначаем ему права для выполнения репликации.
```
mysql -u root -p <пароль root сервера БД>
GRANT REPLICATION SLAVE ON *.* TO 'slave_user'@'%' IDENTIFIED BY 'password';
FLUSH PRIVILEGES;
```
5. На master сервере делаем дамп базы данных c блокировкой таблиц.
```
mysqldump -u root -p --lock-all-tables newdatabase > newdatabase.sql
```
6. Переносим дамп базы на slave сервер, создаем базу данных с таким же именем и импортируем базу.
```
CREATE DATABASE newdatabase;
mysql -u root -p newdatabase < newdatabase.sql
```
7. Настраиваем slave в `/etc/my.cnf`:
```
# ID Слейва, удобно выбирать следующим числом после Мастера
server-id = 2
# Путь к relay логу
relay-log = /var/log/mysql/mysql-relay-bin.log
# Путь к bin логу на Мастере
log_bin = /var/log/mysql/mysql-bin.log
# База данных для репликации
binlog_do_db = newdatabase
```
Перезапускаем сервер базы данных.
8. Запускаем репликацию на slave сервере.
```
CHANGE MASTER TO MASTER_HOST='10.10.0.1', MASTER_USER='slave_user', MASTER_PASSWORD='password',
MASTER_LOG_FILE = 'mysql-bin.000001', MASTER_LOG_POS = 107;
##Указанные значения мы берем из настроек Мастера
После этого запускаем репликацию на Слейве:
START SLAVE;
```
9. Проверяем статус репликации:
```
SHOW SLAVE STATUSG
```

</details>

2. Какой тип базы данных использует Prometheus?

<details>
  <summary>Ответ</summary>

Prometheus использует TSDB (time series database).

</details>