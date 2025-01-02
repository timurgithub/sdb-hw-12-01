# Домашнее задание к занятию «Базы данных» - `Акаев Тимур`

### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

### Ответ

1. Сотрудники
идентификатор (первичный ключ) - serial
ФИО - varchar(100)
идентификатор должности (внешний ключ) - integer
идентификатор подразделения (внешний ключ) - integer
дата найма - date
идентификатор проекта (внешний ключ) - integer

2. Должности
идентификатор (первичный ключ) - serial
наименование должности - varchar(50)

3. Подразделения
идентификатор (первичный ключ) - serial
наименование подразделения - varchar(100)
тип подразделения - varchar(20)
адрес филиала - varchar(200)

4. Оклады
идентификатор (первичный ключ) - serial
идентификатор сотрудника (внешний ключ) - integer
оклад - numeric(10, 2)

5. Проекты
идентификатор (первичный ключ) - serial
наименование проекта - varchar(100)

6. Филиалы
идентификатор (первичный ключ) - serial
адрес - varchar(200)

7. Связь сотрудники-проекты
идентификатор (первичный ключ) - serial
идентификатор сотрудника (внешний ключ) - integer
идентификатор проекта (внешний ключ) - integer

