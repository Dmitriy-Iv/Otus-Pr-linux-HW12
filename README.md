# **Введение**

В данном домашнем задании нам необходимо получить практический опыт работы с Systemd.

---

# **Подготовка и запуск окружения**

1. Клонируем на свой компьютер данный репозиторий.
```
dima@Test-Ubuntu-1:~/otus$ git clone https://github.com/Dmitriy-Iv/Otus-Pr-linux-HW12.git
```

2. Переходим в склонированный репозиторий и запускаем Vagrantfile.
```
dima@Test-Ubuntu-1:~/otus$ cd Otus-Pr-linux-HW12/
dima@Test-Ubuntu-1:~/otus/Otus-Pr-linux-HW12$ vagrant up
```

### **Комментарии к домашнему заданию по Systemd**

Для выполнения данного задания был создан Vagrantfile, в нём же прописан запуск playbook. 
В playbook каждое задание - это копирование подготовленных файлов конфигов в нужные директории и страрт нужных сервисов (демонов).
При успешном исполнении мы должны увидеть в выводе playbook успешное выполнение каждой из трёх секций домашнего задания из методички.

1. Вывод лога, в котором видно - что наш сервис нашёл ключевое слово.
![alt text](/screenshots/hw12-1.PNG?raw=true "Screenshot1") 

2. Вывод в консоль, что наш сервис spawn-fcgi запущен и работает.
![alt text](/screenshots/hw12-2.PNG?raw=true "Screenshot2") 

3. Вывод в консоль, что наши сервисы, запущенные из шаблона -  httpd@first и  httpd@second запущены и работают, а также проверка выводом ss -tnulp.
![alt text](/screenshots/hw12-3.PNG?raw=true "Screenshot3")