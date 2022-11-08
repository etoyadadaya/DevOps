1. Что означает user is not in the sudoers file?
<details><summary> Важная кнопка </summary>

***Данному пользователю не прописано разрешение на выполнение команды sudo в файле /etc/sudoers.***

</details>

2. Что такое Kernel?
<details><summary> Важная кнопка </summary>

***Ядро операционной системы.***

</details>

3. Можно ли в Ubuntu20.04.3 LTS работать от ROOT?
<details><summary> Важная кнопка </summary>

Можно при помощи вызова:

    sudo / su.

</details>

4. Что такое демоны?
<details><summary> Важная кнопка </summary>

***Демон*** - это работающий в фоновом режиме служебная программа или процесс.

</details>

5. Какая комбинация цифр отвечает за права на чтение и запись для владельца и на запись для группы и всех остальных?
<details><summary> Важная кнопка </summary>

    666

</details>

6. Что не является текстовым редактором?
<details><summary> Важная кнопка </summary>

    cat

</details>

7. Что такое системные пользователи?
<details><summary> Важная кнопка </summary>

***Учётные записи создаваемые системой для управления привилегиями и правами доступа к файлам и каталогам.***

</details>

8. Какой командой изменяются права доступа на файл?
<details><summary> Важная кнопка </summary>

    chmod

</details>

9. Выберите верный вариант du -s -h /root/ do -sh /root/ do -sh /root?
<details><summary> Важная кнопка </summary>

***Все верные:***

* du –s –h /root/ 

* du –sh /root

* du –sh /root/ или du –sh /root

</details>

10. Как выглядит маска 255.255.0.0 в префиксоной записи?
<details><summary> Важная кнопка </summary>

11111111.11111111.00000000.00000000 - ***двоичная запись.***

/16 - ***префиксная запись.***

</details>

11. Что такое SNAT?
<details><summary> Важная кнопка </summary>

***Изменение адреса и порта источника пакета, доступен в цепочках PREROUTING и POSTROUTING.***

</details>

12. Номер порта ssh?
<details><summary> Важная кнопка </summary>

***SSH*** — это протокол прикладного уровня. SSH-сервер обычно прослушивает соединения на ***TCP-порту 22***.

</details>

13. Чему равен адрес сети 128.0.1.1/8?
<details><summary> Важная кнопка </summary>

    128.0.0.0

</details>

14. Что такое dhcp?
<details><summary> Важная кнопка </summary>

***DHCP*** — сетевой протокол, позволяющий сетевым устройствам автоматически получать IP-адрес и другие параметры, необходимые для работы в сети TCP/IP. Данный протокол работает по модели «клиент-сервер».

</details>

15. Что такое localhost?
<details><summary> Важная кнопка </summary>

    127.0.0.1/8

***Доменное имя для частных адресов***

</details>

16. Как удалить все правила из iptables?
<details><summary> Важная кнопка </summary>

    iptables -F

</details>

17. Что из перечисленного localhost?
<details><summary> Важная кнопка </summary>

    127.255.255.1

</details>

18. Укажите динамический порт?
<details><summary> Важная кнопка </summary>

    50000

</details>

19. Какой параметр позволяет узнать существует ли файл, и является ли он файлом?
<details><summary> Важная кнопка </summary>

    -d

</details>

20. Какой параметр позволяет узнать пустой ли файл?
<details><summary> Важная кнопка </summary>

    -s

</details>

21. Выбрать вариант, который является комментарием?
<details><summary> Важная кнопка </summary>

    #comment

</details>

22. Что означает код возврата 1?
<details><summary> Важная кнопка </summary>

***В результате выполнения команды возникли ошибки.***

</details>

23. Что выведет скрипт?
<details><summary> Важная кнопка </summary>

</details>

24. Что выведет скрипт?
<details><summary> Важная кнопка </summary>

</details>

25. Чем отличается docker и виртуальная машина?
<details><summary> Важная кнопка </summary>

Отличие технологий, тем что ***виртуальная машина виртуализирует аппаратные ресурсы***, а ***контейнер виртуализирует только операционную систему.***

</details>

26. Как удалить Docker-образ?
<details><summary> Важная кнопка </summary>

    docker rmi

</details>

27. Какой командой можно вывести 5 последних строк файла?
<details><summary> Важная кнопка </summary>

    tail --lines=5 file

</details>

28. Как перенаправить stdout из одной команды в stdin другой?
<details><summary> Важная кнопка </summary>

    cmd1 < cmd2

</details>

29. Для чего придерживаться минимального количества вызовов RUN внутри образа?
<details><summary> Важная кнопка </summary>

***Чтобы не увеличивать объем образа, так как каждый RUN создает слой, который требует памяти.***

</details>

30. Как в gitlab-ci указать, что этап будет запускаться отдельно?
<details><summary> Важная кнопка </summary>

    rules:
    -when: manual

</details>

31. В чём значение слоёв образа?
<details><summary> Важная кнопка </summary>

***Каждый слой описывает какое-то изменение, которые должны быть выполнены с данными на запущенном контейнере.***

</details>

32. Что такое pipeline?
<details><summary> Важная кнопка </summary>

***Это последовательность выполнения стадий, каждая из которых включает несколько задач.***

</details>

33. Какой командой можно скопировать файл внутрь образа при написании файла dockerfile?
<details><summary> Важная кнопка </summary>

    COPY

</details>

34. За что отвечает \”%Referer}i\”  в combined Log Format?
<details><summary> Важная кнопка </summary>

***URL с которого перешел пользователь.***

</details>

35. С чего начинается bash-скрипт?
<details><summary> Важная кнопка </summary>

    #!/bin/bash или #!/bin/sh

</details>

36. Iptables -A INPUT -s 10.3.10.10/24 -j DROP разрешён ли доступ с ip 10.3.10.10?
<details><summary> Важная кнопка </summary>

***Нет, так как запрещена сеть 10.3.10.0/24***

</details>

37. Что такое GoAccess?
<details><summary> Важная кнопка </summary>

***Утилита для анализа веб-логов.***

</details>

38. Что будет выведено? fale echo$?
<details><summary> Важная кнопка </summary>

    command not found

</details>

39. Какие executorы бывают у gitlab-runnerа?
<details><summary> Важная кнопка </summary>

* kubernetes

* shell

* docker

* virtual box

* custom

* parallels

* ssh

</details>

40. Каким выражением можно посчитать всех пользователей в системе?
<details><summary> Важная кнопка </summary>

    cat /etc/passwd | wc -l

</details>
