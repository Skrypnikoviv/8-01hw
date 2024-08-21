# Домашнее задание к занятию «Работа с данными (DDL/DML)» - `Скрыпников Илья`


### Задание 1. СУБД
Задание можно выполнить как в любом IDE, так и в командной строке.

Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp.

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

1.4. Дайте все права для пользователя sys_temp.

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос:

ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

**Ответ:
```
CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY 'tempass';
SELECT user,authentication_string,host FROM mysql.user;
GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost'WITH GRANT OPTION;
SHOW GRANTS FOR 'sys_temp'@'localhost';
```

![12-02-1](https://github.com/user-attachments/assets/db5820e0-e066-4861-8fee-3ae23bfe91c7)

![12-02-2](https://github.com/user-attachments/assets/82f30586-b51a-4f9b-814e-0770411cc9d2)

![12-02-3](https://github.com/user-attachments/assets/2e68c45d-f04c-4414-9748-f9848fe05bee)


