# Лабораторная работа №1
Итак, после создания репозитория с помощью шаблона, клонирования его и
выполенения инструкций к лабораторной работе имеем файл:
```bash
#!/bin/bash

echo "Welcome to ITMO University"
```
Сама задачка - написать скрипт для приветствия человека со сколь угодно
сложным именем.

Отметим, что имя передаётся в качестве аргумента при вызове файла
и может содержать пробелы. Принимая во внимание последнее, имя стоит получать как
перечисление всех аргументов, а не только первого (что считывало бы просто первое слово).

Напишем же сей [скрипт](script.bash):
```cmd
nano script.bash
```
Меняем содержимое:
```bash
#!/bin/bash

# Using $* instead $1 to take all arguments
echo "Welcome, $*"
```
Пробуем запустить:
```cmd
bash script.bash linux is the worst os
>> out: Welcome, linux is the worst os
```
Таким образом, задача решена