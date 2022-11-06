## Clouds and Automation:

1. Какова роль и преимущества облачных сервисов для DevOps?
   <details>
      <summary> Ответ: </summary>

   Подробнее: https://vc.ru/dev/139276-mogut-li-oblachnye-servisy-vzyat-na-sebya-rol-devops
    </details>


2. Что такое immutable infrastructure? Как достичь? В чем преимущества и недостатки? Packer, AMI и т. д.
   <details>
      <summary> Ответ: </summary>

   ***Immutable Infrastructure*** — подход к созданию неизменяемой инфраструктуры. Идея его не нова в мире, хоть и не слишком распространена. Мы начали его использовать, когда поняли, что не все можно запустить в Kubernetes, и нам нужны виртуальные машины.

   Это подход о виртуалках, к которым надо относиться как к "пакетам" или контейнерам. Образ виртуальной машины, приложение и его окружение — неделимое целое. Деплой новой версии приложения подразумевает создание нового образа виртуальной машины, развертывание из него виртуалки и введение машины в строй на замену "старых" виртуалок. В общем, это практически попытка сделать контейнер из виртуалки.

   Подробнее: https://habr.com/ru/company/semrush/blog/517382/
    </details>


3. Структура Terraform. Как организовать multi-environment project? Terraform workspaces?
   <details>
      <summary> Ответ: </summary>

   ***Конфигурация Terraform*** состоит из файлов с расширением ". tf", в которых описываются настройки провайдеров, ресурсы, запрашиваются и выводятся данные. Обычно под каждый проект создается отдельный рабочий каталог/папка, в который добавляются файлы с описанием конфигурации инфраструктуры.

   ***Как организовать multi-environment project:*** https://www.digitalocean.com/community/tutorials/how-to-deploy-multiple-environments-with-workspaces-in-your-terraform-project

   ***Terraform workspaces:*** https://developer.hashicorp.com/terraform/language/state/workspaces

   Подробнее: https://habr.com/ru/company/semrush/blog/517382/
    </details>


4. Лучшие практики по использованию многих Terraform states.
   <details>
      <summary> Ответ: </summary>

    ХЗ

   Подробнее:
    </details>


5. Как организовать доступ команде разработчиков к AWS/GCP/Azure? Role-based access, assume role, SSO.
   <details>
      <summary> Ответ: </summary>
 
   Подробнее: https://learn.microsoft.com/ru-ru/azure/active-directory/saas-apps/amazon-web-service-tutorial
    </details>


6. Что такое Terraform provider, module?
   <details>
      <summary> Ответ: </summary>

   ***Модуль Terraform:*** https://habr.com/ru/post/553576/

    Позволяет вам создавать логическую абстракцию поверх некоторого набора ресурсов. Другими словами, модуль позволяет вам группировать ресурсы вместе и повторно использовать эту группу позже, возможно, много раз.

   ***Terraform Provider:*** https://devops-courses.zone3000.net/terraform-bazovye-printsipy-i-instrumenty/

    Это может быть физическая или виртуальная машина, сетевое оборудование, контейнер. Терраформ помогает создавать и управлять этими ресурсами в рамках созданной инфраструктуры. В этой схеме за взаимодействие API и передачу ресурсов отвечает Terraform Provider.
    </details>


7. Как версионировать Terraform modules?
   <details>
      <summary> Ответ: </summary>
    
    хз

   Подробнее:
    </details>


8. Когда нужно использовать local-exec и remote-exec?
   <details>
      <summary> Ответ: </summary>

   ***local-exec Provisioner:*** https://runebook.dev/ru/docs/terraform/provisioners/local-exec

    Вызывает локальный исполняемый файл после того, как ресурс создан. Это вызывает процесс на машине, на которой запущен Terraform, а не на ресурсе. См. remote-exec обеспечения удаленного выполнения для выполнения команд на ресурсе.

   ***Средство обеспечения remote-exec:*** https://runebook.dev/ru/docs/terraform/provisioners/remote-exec

    Вызывает сценарий на удаленном ресурсе после его создания. Это может быть использовано для запуска инструмента управления конфигурацией, самозагрузок в кластер, и т.д. Чтобы вызвать локальный процесс, увидеть local-exec Provisioner вместо этого. Средство обеспечения remote-exec поддерживает подключения типа ssh и winrm.
    </details>


9. Что такое golden image и как его создать?
   <details>
      <summary> Ответ: </summary>

   ***«Золотой образ» (Gold Image)*** — это предварительно настроенная виртуальная машина, которая используется как шаблон для клонирования виртуальных рабочих мест.

   Подробнее: https://docs.sbercloud.ru/vdi/ag/topics/guides__gold-image-create.html
    </details>
