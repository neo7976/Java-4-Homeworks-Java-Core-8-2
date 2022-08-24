## Java-4-Homeworks-Java-Core-8-2

`C:\Windows\System32\drivers\etc`  - путь корректировки нашего hosts

Добавляем - `127.0.0.1 netology.homework`


[Ссылка на java файлы решения ДЗ](src/main/java)



## Задача "Клиент-сервер с рюшечками"

### Описание
В этом задании вам предлагается более жизненный пример, где вы задействуете файл hosts, часто используемый при настройке окружения, и глубже погрузитесь во взаимодействие на сокетах.

Для выполнения задания нужно отредактировать файл `hosts`, чтобы запросы на адрес `netology.homework` перенаправлялись на ваш локальный компьютер (`127.0.0.1`)  
И усовершенствовать предыдущее задание, чтобы оно работало через адрес `netology.homework`, а общение происходило в несколько(3-5) шагов, в форме диалога  

### Реализация
Добавьте в файл `hosts` новую строку, в которой пропишите резолвинг `netology.homework` на ваш локальный компьютер (`127.0.0.1`). Подробную инструкцию по работе с этим файлом вы можете найти по ссылке в презентации.  

Далее усовершенствуйте первую задачу следующим образом:
1. В клиентской части замените адрес подключения `localhost` на `netology.homework`
2. В серверной и клиентской части сделайте последовательность вызовов в рамках одной сессии таким образом, чтобы получился некий диалог между клиентом и сервером, содержащий от 3 до 5 (или больше) шагов. Например,   
- при подключении сервер спрашивает: `Write your name`. Клиент читает это сообщение и отправляет ему имя.   
- Сервер читает имя, запоминает его, и задает следующий вопрос: `Are you child? (yes/no)`. Клиент отвечает `yes` или `no`.   
- На что сервер, если увидел `yes`, отвечает `Welcome to the kids area, %username%! Let's play!`, а если `no`, то `Welcome to the adult zone, %username%! Have a good rest, or a good working day!` (где %username% - имя клиента из предыдущего шага)
