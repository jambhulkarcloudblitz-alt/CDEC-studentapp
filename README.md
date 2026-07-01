# MariaDB Setup and Configuration Guide for Windows

This guide explains how to set up MariaDB, create a database, and Create Database User

## 1. Installing MariaDB

Installing MariaDB on Ubntu

```shell
apt update && apt install mariadb-server -y
```

## 2. Securing MariaDB

Open the Command Prompt as Administrator and run the following command to secure your installation:

```shell

mysql_secure_installation
```

Follow the prompts to:
Set a root password.
Remove insecure default users and test databases.
Disable remote root login.

## 3. Setting Up the Database

Open terminal and login to MariaDB:

```bash

mysql -u root -p
```
---

# if you are using RDS database 
install client to connect database to server 
```
sudo apt update
sudo apt install mysql-client
```
```
mysql -h <endpoint> -u <username> -p
```


Enter the root password when prompted.

Create a new database and user:

```sql
CREATE DATABASE student_db;
GRANT ALL PRIVILEGES ON springbackend.* TO 'username'@'localhost' IDENTIFIED BY 'your_password';
```
## in this case if Password Redhat123 and used ec2 instance DB 
```
CREATE DATABASE student_db;
```
```
use student_db;
```
```
GRANT ALL PRIVILEGES ON springbackend.* TO 'root'@'localhost' IDENTIFIED BY 'Redhat123';
```

## if DB-instance were used then use this queary
```sql
CREATE DATABASE student_db;
GRANT ALL PRIVILEGES ON springbackend.* TO 'admin'@'localhost' IDENTIFIED BY 'Redhat123';
```



Replace username and your_password with your desired username and password.

Exit MariaDB:

```sql

EXIT;
```

## 4. You will need Database Credentials to Connect Backend with Database
1. DB_HOST
2. DB_USER
3. DB_PASS
4. DB_PORT
5. DB_NAME

CHANGES DONE BY DEV

