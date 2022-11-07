## Information Security:

1. Как должны храниться пароли в базах данных (Salt&Pepper, Rainbow Tables, Adaptive Hashing)?
   <details>
      <summary> Ответ: </summary>

   Подробнее: https://habr.com/ru/company/acribia/blog/413157/
    </details>


2. Как передавать секреты в application (Secrets management)?
   <details>
      <summary> Ответ: </summary>

   Подробнее: https://habr.com/ru/company/oleg-bunin/blog/438740/
    </details>


3. Сравните CI/CD SAST и DAST?
   <details>
      <summary> Ответ: </summary>

   Подробнее: https://itsecforu.ru/2022/02/21/🐛-sast-или-dast-что-лучше-использовать-для-те/
    </details>


4. Какие вы знаете Kubernetes security practices? RBAC? OPA? Какие недостатки RBAC и какие кейсы знаете?
   <details>
      <summary> Ответ: </summary>

   Подробнее: https://habr.com/ru/company/southbridge/blog/655409/
    </details>


5. Расскажите о защите от DDOS атак, WAF.
   <details>
      <summary> Ответ: </summary>

   Подробнее: https://www.anti-malware.ru/practice/methods/How-to-protect-from-DDoS-correctly
    </details>


6. Что такое Rootless containers и для чего он нужен?
   <details>
      <summary> Ответ: </summary>

   Подробнее: https://itsecforu.ru/2022/03/22/🐳-что-такое-docker-без-root-rootless/
    </details>


7. Что такое AppArmor и Seccomp и зачем они нужны?
   <details>
      <summary> Ответ: </summary>

   AppArmor - это реализация Модуля безопасности линукс по управлению доступом на основе имен. AppArmor ограничивает отдельные программы набором перечисленных файлов и возможностями в соответствии с правилами Posix 1003.1e.

   Seccomp (сокращение от secure computing) — механизм ядра Linuх, позволяющий процессам определять системные вызовы, которые они будут использовать. Если злоумышленник получит возможность выполнить произвольный код, seccomp не даст ему использовать системные вызовы, которые не были заранее объявлены.

    Seccomp — разработка Google. Он используется, в частности, в браузере Google Chrome для запуска плагинов.

   Подробнее: 

    https://help.ubuntu.ru/wiki/руководство_по_ubuntu_server/безопасность/apparmor

   https://habr.com/ru/company/selectel/blog/322046/   
    </details>


8. Приходилось ли работать с Falco? Если да, то что реализовывали?
   <details>
      <summary> Ответ: </summary>
    Ваш опыт
   Подробнее:
    </details>


9. HashiCorp Vault и как правильно передать нам секреты в контейнере и CI pipeline?
   <details>
      <summary> Ответ: </summary>

   Подробнее: https://habr.com/ru/company/oleg-bunin/blog/438740/
    </details>


10. Что такое Admission Controllers и какие вы использовали?
    <details>
      <summary> Ответ: </summary>

    Admission Controllers (контроллеры доступа) позволяют добавить дополнительные опции в работу Kubernetes для изменения или валидации объектов при запросах к Kubernetes API. Если в результате работы контроллера запрос отклоняется, то отклоняется весь запрос к API-серверу, а конечному пользователю возвращается ошибка.

Подробнее: https://kb.selectel.ru/docs/cloud/managed-kubernetes/manage-cluster/admission-controllers/
</details>


11. Как хранятся секреты etcd? Как просмотреть ресурсы в etcd?
   <details>
      <summary> Ответ: </summary>

Подробнее: https://habr.com/ru/company/southbridge/blog/658123/
</details>


12. Чем проверяете на уязвимости ваш Kubernetes cluster?
   <details>
      <summary> Ответ: </summary>

Подробнее: https://habr.com/ru/company/otus/blog/664546/
</details>


13. Что такое Secure SDLC?
    <details>
      <summary> Ответ: </summary>
    
    Security Development Lifecycle (SDL, жизненный цикл безопасной разработки) — концепция разработки, заключающаяся в формировании требований к приложению, безопасном программировании, тестировании, сертификации, эксплуатации и обновлении.

Подробнее: https://ru.wikipedia.org/wiki/Security_Development_Lifecycle
</details>


14. Что вы знаете о Cloud Infrastructure Attack via a Pull Request и как этого избежать?
   <details>
      <summary> Ответ: </summary>

Подробнее: https://goteleport.com/blog/hack-via-pull-request/
</details>
