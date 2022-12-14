## Виртуализация: 

Отличный список вопросов по докеру(ИМХО): https://habr.com/ru/company/southbridge/blog/528206/

1. В чем разница между виртуализацией и контейнеризацией? В чем плюсы и минусы?
    <details>
      <summary> Ответ: </summary>

   Основное отличие контейнера от виртуальной машины заключается в том, что контейнер использует ядро хоста для обработки данных.

   ***Контейнер*** - это виртуальная среда, которая обеспечивает интерфейс взаимодействия между пользовательскими приложениями и методами ядра.

   ***Виртуальная машина*** - это полностью изолированная программная среда, эмулирующая аппаратное обеспечение некоторой платформы.

   ***Контейнеры и виртуальные машины*** — это просто разные способы предоставления и использования вычислительных ресурсов — процессоров, памяти и ввода-вывода — которые уже присутствуют в физическом компьютере. Хотя цель виртуализации, по сути, та же, что и у контейнеров, подход существенно отличается, и каждый подход предлагает уникальные характеристики и компромиссы для корпоративных рабочих нагрузок.

   ***Преимущества виртуальных машин***:
   
   ***Независимость***. Изолированность каждой ВМ означает, что сбои и отказы в ОС или приложениях ВМ не повлияют на другие ВМ на том же компьютере или на других компьютерах в среде центра обработки данных.
   
   ***Использование ресурсов***. Поскольку несколько ВМ могут быть инициализированы и развернуты на одном физическом компьютере, система может эффективно размещать несколько рабочих нагрузок без необходимости покупать несколько компьютеров. Это позволяет консолидировать серверы в центре обработки данных.
   
   ***Доступность***. Переносимость виртуальных машин позволяет сбалансировать работу виртуальных машин на нескольких системах для повышения производительности и поддержки задач обслуживания системы. ВМ также можно копировать в файлы или восстанавливать из них, что обеспечивает быструю защиту и восстановление ВМ.
   
   ***Гибкость***. Для каждой ВМ требуется своя ОС, но каждая ОС может быть разной. Это позволяет предприятию использовать несколько ОС на одном физическом компьютере.
   
   ***Безопасность***. Гипервизоры и логическая изоляция, которую они обеспечивают, доказали свою безопасность для виртуальных машин. Даже если одна ВМ может быть заражена, это не приведет к заражению других ВМ.

   ***Недостатки Виртуальных машин***:
   
   ***Размер***. Экземпляры ВМ могут быть большими, с использованием нескольких процессоров и значительного объема памяти. Это хорошо подходит для рабочих нагрузок корпоративного класса, но на практике существует ограничение на количество виртуальных машин, которые можно развернуть на одном компьютере.
   
   ***Время***. Создание и развертывание виртуальных машин может занимать от нескольких секунд до нескольких минут. Хотя это не так много времени с человеческой точки зрения, ВМ могут недостаточно быстро масштабироваться для удовлетворения динамических или краткосрочных вычислительных потребностей.
   
   ***Лицензирование программного обеспечения***. Каждая ВМ нуждается в ОС и рабочей нагрузке, поэтому стоимость лицензирования ОС и приложений может стать значительной. Предприятие должно внимательно управлять развертыванием ВМ для учета лицензий и обеспечения того, чтобы ВМ с дорогостоящими лицензиями ОС и приложений работали и выполняли продуктивную работу для предприятия, избегая разрастания ВМ.

   ***Преимущества контейнеров***:
   
   ***Размер***. Контейнеры используют одно общее ядро ОС и не используют собственные уникальные ОС, поэтому контейнеры являются гораздо меньшими логическими единицами, чем виртуальные машины. Это позволяет компьютеру одновременно размещать гораздо больше контейнеров, чем ВМ.
   
   ***Скорость***. Небольшой размер экземпляров контейнеров позволяет создавать и уничтожать их гораздо быстрее, чем ВМ. Благодаря этому контейнеры хорошо подходят для быстрого масштабирования и краткосрочного использования, что может быть нецелесообразно для ВМ.
   
   ***Уникальный гипервизор***. Для хостинга и управления контейнерами используются специализированные гипервизорные платформы, такие как Docker, rkt и Apache Mesos.
   
   ***Неизменяемость***. В отличие от ВМ, контейнеры не изменяются. Вместо этого контейнерный оркестратор в программном слое контейнера запускает и останавливает контейнеры, когда они необходимы. Аналогичным образом, программное обеспечение, работающее в контейнерах, не обновляется, как традиционное ПО. Вместо этого обновления включаются в новый образ контейнера, который может быть развернут там, где это необходимо.

   ***Недостатки контейнеров***:
   
   ***Производительность***. Контейнеров может быть много, и контейнеры используют общую ОС в дополнение к контейнерному слою. Это означает, что контейнеры эффективно используют ресурсы, но между контейнерами могут возникать разногласия при попытке получить доступ к аппаратным ресурсам, таким как сети. Такое соперничество может повлиять на общую производительность контейнера.
   
   ***Совместимость***. Контейнеры, упакованные для одной платформы, такие как Docker, могут не работать с другими платформами. Аналогично, некоторые контейнерные инструменты могут не работать с различными контейнерными платформами. Например, Red Hat OpenShift работает только с оркестратором Kubernetes. Учитывайте экосистему контейнеров при оценке контейнерных технологий для предприятия.
   
   ***Хранение***. Контейнеры изначально спроектированы так, чтобы быть без статических данных — данные в контейнере исчезают, когда исчезает контейнер. Существуют способы обеспечения постоянного хранения для контейнеров, например, Docker Data Volumes, но вопрос постоянного хранения контейнеров часто рассматривается как нечто отдельное.
   
   ***Пригодность***. Контейнеры, как правило, представляют собой небольшие и гибкие структуры, лучше всего подходящие для компонентов приложений или микросервисов. Полнофункциональные корпоративные приложения обычно плохо работают в контейнерах. Учитывайте пригодность при планировании развертывания контейнеров.

   Подробнее: https://www.itc.by/kontejnery-i-virtualnye-mashiny-v-chem-klyuchevye-razlichiya/
   </details>


2. Как при запуске Docker-контейнера «повесить» его из 80-го порта в контейнере на 8081 на хост?
    <details>
      <summary> Ответ: </summary>

   В первую очередь стоит обновить файл hostconfig.json. Для этого найдем ключ привязки портов в этом файле. Поскольку при запуске Docker-контейнера маппинг не был настроен, поле ключа PortBindings Docker-контейнера будет пустым:
   
   "PortBindings": {"80/tcp":[{"HostIp":"","HostPort":"82"}]}

   "ExposedPorts": {"80/tcp":{},"82/tcp":{},"8080/tcp":{} }

   Подробнее: https://ru.hexlet.io/blog/posts/mapping-docker
    </details>


3. Как передать в виртуальную машину USB device?
    <details>
      <summary> Ответ: </summary>

   На данный момент можно использовать следующие технологии для проброса USB устройства в Hyper-V.

   1: Проброс USB дисков с хоста Hyper-V;
   
   2: Расширенные возможности консоли Hyper-V — Enhanced Session Mode;
   
   3: Проброс USB устройства через RDP сессию;
   
   4: Использование программного/аппаратного средства для проброса USB по сети (USB over IP).

   Подробнее: https://winitpro.ru/index.php/2014/06/26/kak-napryamuyu-probrosit-usb-disk-v-virtualnuyu-mashinu-hyper-v/
    </details>


4. Docker-контейнер потребляет многие SWAP. Что делать?
    <details>
      <summary> Ответ: </summary>

   ***Параметр memory-swap***:

   С помощью параметра memory-swap можно разрешить контейнеру записывать на диск данные, превышающие размер оперативной памяти, выделенной контейнеру. Он работает, только если используется одновременно с параметром memory. Например, если memory = "400m" и memory-swap = "1g", то контейнер может использовать 400мб оперативной памяти и 600мб подкачки (1гб-400мб).
   
   Подробнее: https://habr.com/ru/company/southbridge/blog/528206/
    </details>
