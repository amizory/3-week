# CI/CD

* [Основы CI/CD](#Основы-CI/CD)
* [Build Automation Tools](#Build-Automation-Tools)
* [Основы GitLab CI](#Основы-GitLab-CI)
* [Основы Jenkins](#Основы-Jenkins)

## <a id="Основы-CI/CD">Основы CI/CD</a>

```txt
1 - Continuous Integration, Continuous Delivery, Continuous Deployment.
2 - Какие проблемы решают правильно выстроенные процессы CI/CD.
3 - Основные стадии (этапы) CI-пайплайна.
4 - Обзор и сравнение основных инструментов для построения CI/CD пайплайнов: 
    Jenkins, GitLab CI, GitHub Actions, TeamCity, Bitbucket Pipelines, Atlassian Bamboo.
```

### Notice-1

```txt
1 - Что такое Continuous Integration?

->  Continuous Integration (CI) - это практика разработки программного обеспечения,
    которая предполагает автоматическое объединение изменений кода в единую
    основную ветку несколько раз в день, с последующей автоматической сборкой и
    тестированием. Это позволяет выявить ошибки и проблемы на ранней стадии разработки,
    что упрощает их исправление и уменьшает риск критических ошибок в будущем.
```

```txt
2 - Какие проблемы решают правильно выстроенный CI пайплайн?

->  - Уменьшает количество ошибок и багов в коде, поскольку автоматическое
    тестирование выявляет проблемы на ранней стадии
    - Ускоряет процесс выпуска новой версии продукта, поскольку автоматическая
    сборка и тестирование сокращают время, необходимое для подготовки релиза
    - Повышает качество кода и снижает риск критических ошибок, поскольку
    автоматическое тестирование и проверка кода обеспечивают его стабильность и надежность
    - Уменьшает время, необходимое для выявления и исправления ошибок, поскольку
    проблемы выявляются на ранней стадии и могут быть быстро исправлены
    - Повышает прозрачность и видимость процесса разработки, поскольку все участники
    команды могут видеть текущее состояние проекта и отслеживать прогресс
    - Автоматизирует рутинные задачи и снижает нагрузку на разработчиков, поскольку
    многие задачи, такие как сборка и тестирование, выполняются автоматически
    - Улучшает сотрудничество между разработчиками, поскольку все изменения кода
    интегрируются в единую основную ветку и могут быть быстро проверены и одобрены.
```

```txt
3 - Какие могут быть стадии CI пайплайна?

->  - Сборка (Build): сборка кода в исполняемый файл или пакет. 
    Этот этап включает в себя компиляцию кода, сборку библиотек и других
    зависимостей.

    - Тестирование (Test): автоматическое тестирование кода на наличие ошибок и багов.
    Этот этап включает в себя выполнение юнит-тестов, интеграционных тестов и
    других типов тестов.

    - Проверка кода (Code Review): проверка кода на соответствие стандартам
    и требованиям.
    Этот этап включает в себя проверку кода на наличие ошибок,
    соответствие стандартам кодирования и другие требования.

    - Анализ кода (Code Analysis): анализ кода на наличие проблем с производительностью,
    безопасностью и т.п. Этот этап включает в себя анализ кода на наличие проблем с
    производительностью, безопасностью, совместимостью и других аспектов.

    - Тестирование интеграции (Integration Test): тестирование интеграции кода
    с другими компонентами системы. Этот этап включает в себя тестирование интеграции
    кода с другими компонентами системы, такими как базы данных, API и другие сервисы.

    - Тестирование системы (System Test): тестирование системы в целом на наличие
    ошибок и багов. Этот этап включает в себя тестирование системы в целом на наличие
    ошибок и багов, включая функциональное тестирование, тестирование производительности
    и другие типы тестов.

    - Развертывание (Deployment): автоматическое развертывание кода в
    продакшн-окружение. Этот этап включает в себя автоматическое развертывание кода
    в продакшн-окружение, включая настройку серверов, баз данных и других компонентов
    системы.

    - Мониторинг (Monitoring): мониторинг системы после развертывания для выявления
    проблем и ошибок. Этот этап включает в себя мониторинг системы после развертывания
    для выявления проблем и ошибок, включая мониторинг производительности, безопасности
    и других аспектов.
    
    - Отчетность (Reporting): создание отчетов о результатах тестирования и анализа
    кода. Этот этап включает в себя создание отчетов о результатах тестирования и
    анализа кода, включая отчеты о тестировании, анализ кода и другие типы отчетов.

    - Уведомление (Notification): уведомление разработчиков и других заинтересованных
    лиц о результатах тестирования и анализа кода. Этот этап включает в себя уведомление
    разработчиков и других заинтересованных лиц о результатах тестирования и анализа кода,
    включая уведомление о проблемах, ошибках и других важных событиях.

    - Обратная связь (Feedback): предоставление обратной связи разработчикам о результатах
    тестирования и анализа кода. Этот этап включает в себя предоставление обратной связи
    разработчикам о результатах тестирования и анализа кода, включая рекомендации по
    улучшению кода и других аспектов.

    - Итерация (Iteration): повторение цикла CI/CD для обеспечения непрерывного улучшения
    и развития системы. Этот этап включает в себя повторение цикла CI/CD для обеспечения
    непрерывного улучшения и развития системы, включая повторное тестирование, анализ и
    другие этапы.
```

```txt
4 - Что такое Continuous Delivery/Continuous Deployment?

->  - Continuous Delivery (CD) и Continuous Deployment (CD) - это две связанные концепции,
    которые предполагают автоматическое развертывание кода в продакшн-окружение после
    прохождения всех этапов тестирования и анализа.

    - Continuous Delivery (CD) - это практика разработки программного обеспечения,
    которая предполагает автоматическое подготовку кода к развертыванию в
    продакшн-окружение после прохождения всех этапов тестирования и анализа. Это
    означает, что код готов к развертыванию в любой момент, но фактическое
    развертывание может быть отложено.

    - Continuous Deployment (CD) - это практика разработки программного обеспечения,
    которая предполагает автоматическое развертывание кода в продакшн-окружение после
    прохождения всех этапов тестирования и анализа. Это означает, что код автоматически
    развертывается в продакшн-окружение после прохождения всех этапов тестирования
    и анализа.
```

```txt
5 - Какие проблемы решают правильно выстроенный CD пайплайн?

->  - Уменьшает время, необходимое для выпуска новой версии продукта
    - Повышает качество кода и снижает риск критических ошибок
    - Уменьшает количество ошибок и багов в продакшн-окружении
    - Повышает прозрачность и видимость процесса разработки
    - Автоматизирует рутинные задачи и снижает нагрузку на разработчиков
    - Улучшает сотрудничество между разработчиками и операционными командами
    - Повышает гибкость и адаптивность системы
    - Уменьшает риск человеческой ошибки при развертывании кода
    - Повышает безопасность системы за счет автоматического развертывания
      обновлений и исправлений.
```

### Intern-1

```txt
1 - Какие инструменты могут использоваться на различных стадиях CI пайплайна 
    (например, для проверки кода, поиска уязвимых пакетов, сборки и т.д.)?  

->  Проверка кода
    - SonarQube: инструмент для анализа кода и выявления проблем с качеством кода

    Поиск уязвимых пакетов
    - Maven Dependency Plugin: инструмент для анализа зависимостей в проекте

    Сборка
    - Maven: инструмент для сборки и управления зависимостями в проекте
    - Gradle: инструмент для сборки и управления зависимостями в проекте
    - Jenkins, GitLab CI: инструмент для автоматизации сборки и развертывания проекта

    Тестирование
    - JUnit: инструмент для написания и запуска юнит-тестов
    - Selenium: инструмент для автоматизации тестирования веб-приложений

    Развертывание
    - Docker: инструмент для контейнеризации приложений
    - Kubernetes: инструмент для оркестрации контейнеров
    - Ansible: инструмент для автоматизации развертывания и конфигурации
    приложений
    - Terraform: инструмент для автоматизации развертывания и конфигурации
    инфраструктуры

    Мониторинг
    - Prometheus: инструмент для мониторинга и сбора метрик
    - Grafana: инструмент для визуализации метрик и логов
    - ELK Stack (Elasticsearch, Logstash, Kibana): инструмент для сбора,
    обработки и визуализации логов

    Уведомление
    - Slack: инструмент для уведомления команды о событиях в CI пайплайне
    - Email: инструмент для уведомления команды о событиях в CI пайплайне
```

```txt
2 - Чем отличаются Jenkins и GitLab CI?

->  Это два популярных инструмента для автоматизации сборки, тестирования 
    развертывания приложений

    Jenkins
    - Это автономный инструмент, может быть использован для автоматизации
    различных задач по сборке, тестированию и развертыванию приложений
    и мониторинга
    - Он может быть интегрирован с различными системами контроля версий,
    такими как Git, SVN и Mercurial.
    - Jenkins имеет большое сообщество разработчиков и пользователей, что
    обеспечивает широкий спектр плагинов и интеграций с другими инструментами.

    GitLab CI
    - GitLab CI - это инструмент для автоматизации сборки, тестирования
    и развертывания приложений, который является частью платформы GitLab.
    - GitLab CI тесно интегрирован с системой контроля версий GitLab, что
    позволяет автоматически запускать сборку и тестирование приложений при каждом
    коммите.
    - GitLab CI имеет более простую и интуитивно понятную конфигурацию, чем Jenkins,
    что делает его более доступным для начинающих пользователей.
    - GitLab CI также имеет более тесную интеграцию с другими инструментами GitLab,
    такими как GitLab Runner и GitLab Pages.
```

### Advanced-1

```txt
1 - Как работать с секретами в пайплайнах?

->  Важный аспект обеспечения безопасности и конфиденциальности данных
    в автоматизированных процессах. Секреты - это чувствительные данные,
    такие как пароли, ключи, сертификаты и другие конфиденциальные информации,
    которые необходимы для работы пайплайна

    Правила работы с секретами
    - Не храните секреты в открытом виде
    - Используйте зашифрованные секреты
    - Используйте секретные переменные: используйте секретные переменные,
    такие как environment variables или secret variables, для хранения и передачи секретов
    - Ограничьте доступ к секретам
    - Удаляйте секреты после использования

    Инструменты для работы с секретами - AWS Secrets Manager, Jenkins Credentials Plugin,
    HashiCorp's Vault

    Использовать:
    - автоматизированные процессы - для управления секретами и конфиденциальными данными
    - аудит и мониторинг - для отслеживания доступа к секретам и конфиденциальным данным
    - шифрование - для хранения и передачи секретов и конфиденциальных данных
    - ограничения доступа - для ограничения доступа к секретам и конфиденциальным данным
    - регулярные обновления - для обновления секретов и конфиденциальных данных
```

```txt
2 - Какие есть стратегии развёртывания?

->  - Rolling Update: стратегия предполагает постепенное развёртывание
    изменений в продакшн-окружение. Это означает, что изменения будут доступны
    пользователям поэтапно, а не одновременно.

    - A/B Testing: стратегия предполагает развёртывание двух версий
    приложения: A и B. Пользователи случайным образом распределяются между двумя версиями,
    и результаты сравниваются.

    - Canary Release: стратегия предполагает развёртывание
    изменений в продакшн-окружение для небольшой группы пользователей. Если
    изменения работают корректно, они развёртываются для всех пользователей.

    - Blue-Green Deployment: стратегия предполагает создание двух идентичных окружений:
    blue и green. Изменения развёртываются в green-окружении, а затем пользователи
    переключаются на green-окружение, а blue-окружение становится резервным

    - Dark Launching: стратегия предполагает развёртывание изменений в продакшн-окружение,
    но они не доступны пользователям. Это позволяет тестировать изменения в
    продакшн-окружении без воздействия на пользователей.

    - Shadow Deployment: стратегия предполагает создание копии продакшн-окружения,
    в которой развёртываются изменения. Если изменения работают корректно,
    они развёртываются в продакшн-окружение

    - Big Bang: стратегия предполагает одновременное развёртывание всех изменений
    в продакшн-окружение. Это означает, что все изменения будут доступны пользователям
    сразу после развёртывания

    - Immutable Infrastructure: стратегия Immutable Infrastructure предполагает
    создание новой инфраструктуры для каждого развёртывания. Это позволяет избежать
    проблем с конфигурацией и зависимостями
```

```txt
3 - Как можно реализовать zero downtime деплой? 

->  Zero downtime деплой - это процесс развёртывания изменений в приложении без
    остановки работы приложения. Это означает, что пользователи могут продолжать
    использовать приложение без перерыва, даже когда изменения развёртываются

    1 - Blue-Green Deployment: создать две идентичные копии приложения, одна из
    которых является активной, а другая - резервной. Изменения развёртываются в
    резервной копии, а затем пользователи переключаются на резервную копию.

    2 - Rolling Update: развёртывать изменения в приложении поэтапно,
    обновляя одну часть приложения за раз. Это позволяет избежать остановки работы
    приложения.

    3 - Canary Release: развёртывать изменения в приложении для небольшой
    группы пользователей, а затем, если изменения работают корректно, развёртывать
    их для всех пользователей.

    4 - Load Balancing: использовать балансировку нагрузки для распределения
    трафика между несколькими копиями приложения. Это позволяет развёртывать
    изменения в одной копии приложения, не останавливая работу других копий

    5 - Containerization: использовать контейнеризацию для развёртывания 
    изменений в приложении. Это позволяет создать новую копию приложения с
    изменениями, а затем переключиться на новую копию без остановки работы приложения

    6 - Serverless Architecture: использовать серверную архитектуру для
    развёртывания изменений в приложении. Это позволяет создать новую копию
    приложения с изменениями, а затем переключиться на новую копию без остановки
    работы приложения
```

```txt
4 - Что такое GitOps? 

->  GitOps - это подход к управлению инфраструктурой и приложениями,
    который использует Git как основную систему управления конфигурацией.

    GitOps позволяет управлять инфраструктурой и приложениями как кодом,
    используя Git для хранения и управления конфигурацией

    GitOps основан на следующих принципах:
    - Git как основная система управления конфигурацией: Git используется
    для хранения и управления конфигурацией инфраструктуры и приложений.
    - Код как конфигурация: конфигурация инфраструктуры и приложений представлена
    в виде кода, который может быть изменен и управляем как любой другой код.
    - Автоматическое применение конфигурации: конфигурация инфраструктуры
    и приложений автоматически применяется после изменения кода.
    - Мониторинг и аудит: изменения конфигурации инфраструктуры и приложений
    отслеживаются и аудируются для обеспечения прозрачности и безопасности

    GitOps может быть использован для управления различными типами
    инфраструктуры и приложений, включая:
    - Контейнеризированные приложения: GitOps может быть использован
    для управления контейнеризированными приложениями, такими как Docker.
    - Клауд-инфраструктура: GitOps может быть использован для
    управления облачной инфраструктурой, такой как AWS или Azure.
    - Микросервисная архитектура: GitOps может быть использован
    для управления микросервисной архитектурой, такой как Kubernetes.

    GitOps предоставляет следующие преимущества:
    - Упрощенное управление конфигурацией
    - Автоматическое применение конфигурации
    - Повышенная прозрачность и безопасность
    - Улучшенная совместная работа  
```

```txt
5 - Как обеспечить версионный контроль схемы базы данных?
    Какие инструменты для этого существуют?

->  Версионный контроль схемы базы данных - это процесс управления
    изменениями в структуре базы данных, чтобы обеспечить ее целостность
    и совместимость с приложением. Это важно для предотвращения ошибок и
    проблем с базой данных, которые могут возникнуть при изменении схемы

    - Git: Git - это инструмент для управления версиями кода, который
    также можно использовать для управления версиями схемы базы данных.
    - SQL Source Control: SQL Source Control - это инструмент для
    управления версиями схемы базы данных, который позволяет автоматически
    применять изменения в схеме базы данных
    - Flyway: Flyway - это инструмент для управления версиями схемы базы
    данных, который позволяет автоматически применять изменения в схеме базы данных

    Для обеспечения версионного контроля схемы базы данных можно
    использовать следующие методы:
    - Использование SQL-файлов: SQL-файлы можно использовать для хранения
    изменений в схеме базы данных.
    - Использование версионных таблиц: Версионные таблицы можно использовать
    для хранения изменений в схеме базы данных.
    - Использование хранимых процедур: Хранимые процедуры можно использовать
    для автоматического применения изменений в схеме базы данных
    - Использование триггеров: Триггеры можно использовать для
    автоматического применения изменений в схеме базы данных.
    - Использование пакетов: Пакеты можно использовать для автоматического
    применения изменений в схеме базы данных.

```

## <a id="Build-Automation-Tools">Build Automation Tools</a>

```txt
1 - Назначение Dependency Management Tools.
2 - Maven, Gradle, Npm.
3 - Использование Build Automation Tools в CI/CD пайплайнах.
```

### Notice-2

```txt
1 - Что такое dependency management tool (инструмент управления зависимостями)?
    Что здесь имеется в виду под зависимостями?

->  Dependency management tool (инструмент управления зависимостями) - это
    программный инструмент, который помогает управлять зависимостями в проекте. 

    В контексте программирования, зависимости могут быть:
    - Библиотеки: сторонние библиотеки, которые предоставляют определенные
    функции или классы, которые можно использовать в проекте.
    - Модули: сторонние модули, которые предоставляют определенные функции
    или классы, которые можно использовать в проекте.
    - Пакеты: сторонние пакеты, которые предоставляют определенные функции
    или классы, которые можно использовать в проекте.
    - Фреймворки: сторонние фреймворки, которые предоставляют определенные
    функции или классы, которые можно использовать в проекте

    Зависимости могут быть необходимы для реализации определенной функциональности
    в проекте, но они также могут создавать проблемы, если не управлять ими должным
    образом. Например, если зависимость устарела или содержит ошибки, это может
    привести к проблемам в проекте.

    Инструменты управления зависимостями помогают решить эти проблемы,
    предоставляя следующие функции:
    - Управление версиями зависимостей: инструменты управления зависимостями помогают
    управлять версиями зависимостей, чтобы обеспечить, что проект использует
    последние версии зависимостей.
    - Обнаружение конфликтов: инструменты управления зависимостями помогают
    обнаруживать конфликты между зависимостями, чтобы предотвратить проблемы в проекте.
    - Автоматическое обновление зависимостей: инструменты управления
    зависимостями помогают автоматически обновлять зависимости, чтобы
    обеспечить, что проект использует последние версии зависимостей.
    - Управление лицензиями: инструменты управления зависимостями помогают
    управлять лицензиями зависимостей, чтобы обеспечить, что проект
    соответствует требованиям лицензий
```

```txt
2 - Что из себя представляет maven/gradle? Какие функции у них есть? 

->  Это два популярных инструмента для управления зависимостями и сборки
    проектов в Java.

    Maven - 2004/Gradle - 2008
    Функции:
    - Управление зависимостями: позволяет управлять зависимостями
    в проекте, включая версии и конфигурацию.
    - Сборка проекта: позволяет собирать проект в различные
    форматы, включая JAR, WAR и EAR.
    - Тестирование: позволяет запускать тесты для проекта.
    - Деплой: позволяет деплоить проект в различные среды,
    включая Tomcat, JBoss и WebSphere.
    - Плагины: Maven имеет большое количество плагинов, которые
    позволяют расширить его функциональность.
    
    - Гибкая конфигурация: Gradle позволяет гибко конфигурировать проект,
    включая возможность использования различных языков программирования.

    Преимущества Maven:
    - Более широкое распространение и поддержка
    - Более большое количество плагинов
    - Более простая конфигурация
    Недостатки Maven:
    - Более сложная конфигурация для больших проектов
    - Более медленная скорость сборки

    Преимущества Gradle:
    - Более гибкая конфигурация
    - Более быстрая скорость сборки
    - Более современный дизайн
    Недостатки Gradle:
    - Меньшее количество плагинов
    - Меньшая поддержка
```

```txt
3 - Что такое npm?

->  npm (Node Package Manager) - это менеджер пакетов для Node.js,
    который позволяет управлять зависимостями и пакетами в проект

    npm имеет следующие функции:
    - Управление зависимостями: npm позволяет управлять зависимостями
    в проекте, включая версии и конфигурацию.
    - Сборка проекта: npm позволяет собирать проект в различные
    форматы, включая JavaScript и CSS.
    - Тестирование: npm позволяет запускать тесты для проекта.
    - Деплой: npm позволяет деплоить проект в различные
    среды, включая Node.js и браузеры.
    - Плагины: npm имеет большое количество плагинов, которые
    позволяют расширить его функциональность.

    npm install react/npm update/npm uninstall/npm run/npm test
```

### Intern-2

```txt
1 - Чем отличаются maven и gradle друг от друга?

->  Различия
    - Конфигурация: Maven использует XML-файлы для конфигурации проекта,
    тогда как Gradle использует Groovy-файлы.
    - Система зависимостей: Maven использует систему зависимостей для
    управления версиями библиотек, тогда как Gradle также использует
    систему зависимостей, но с некоторыми различиями в реализации.
    - Плагины: Maven имеет более широкий спектр плагинов, чем Gradle,
    но Gradle имеет более простую систему плагинов.
    - Скорость сборки: Gradle имеет более быструю скорость сборки,
    чем Maven, особенно для больших проектов.
    - Гибкость: Gradle имеет более гибкую систему конфигурации, чем Maven,
    что позволяет более легко настраивать проект.

    Если вы уже используете Maven и хотите сохранить существующую конфигурацию,
    то Maven может быть лучшим выбором. Если вы хотите более гибкую систему
    конфигурации и более быструю скорость сборки, то Gradle может быть
    лучшим выбором
```

```txt
2 - Какие Dependency Management/Build Automation инструменты
    используются на твоём проекте?

->  Maven - это инструмент для управления зависимостями и
    сборки проектов в Java. Он используется для управления версиями
    библиотек и сборки проекта

    Docker - это инструмент для контейнеризации приложений.
    Он используется для создания контейнеров для приложения и управления ими

    Jenkins - это инструмент для автоматизации сборки и развертывания
    приложений. Он используется для автоматизации сборки и развертывания
    приложения

    Kubernetes - это инструмент для оркестрации контейнеров, который
    позволяет автоматизировать процесс развертывания и управления приложениями

    GitLab CI/CD - это инструмент для автоматизации сборки и развертывания
    приложений. Он используется для автоматизации сборки и развертывания
    приложения
```

### Advanced-2

```txt
1 - Как Dependency Management/Build Automation инструменты используются
    в CI/CD пайплайнах?

->  Для автоматизации процесса сборки и развертывания приложения.
    CI/CD пайплайн - это процесс, который автоматически собирает, тестирует
    и развертывает приложение.

    Dependency Management инструменты, такие как Maven, Gradle и npm,
    используются для управления зависимостями приложения. Они автоматически
    скачивают и устанавливают необходимые библиотеки и пакеты.

    Build Automation инструменты, такие как Jenkins используются для
    автоматизации процесса сборки приложения. Они компилируют код,
    выполняют тесты и создают исполняемые файлы.

    Развертывание - это процесс, который автоматически развертывает
    приложение в продакшн-окружение.
```

## <a id="Основы-GitLab-CI ">Основы GitLab CI</a>

```txt
1 - Раннеры, установка и настройка раннера.
2 - Ситаксис пайплайнов GitLab CI.
3 - Тригеры запуска пайплайнов.
4 - Работа с переменными и секретами.
5 - Механизмы переиспользования кода пайплайнов.
6 - Запуск тестов в пайплайн.
7 - Деплой приложения с помощью GitLab CI.
8 - GitLab CI Best Practice.
```

### Notice-3

```txt
1 - Что такое GitLab Runner? Какие виды раннеров бывают? 

->  GitLab Runner - это инструмент, который выполняет задачи
    CI/CD (например, сборку, тестирование и развёртывание кода) в GitLab.
    Он позволяет автоматизировать процесс сборки и тестирования кода, а
    также обеспечивает возможность интеграции с другими инструментами и сервисами.

    Виды раннеров:
    - Shared Runner (общий раннер): предоставляется GitLab и доступен
    для всех проектов. Это значит, что любой проект в GitLab может использовать
    общий раннер для выполнения задач CI/CD
    - Specific Runner (специальный раннер): создается для конкретного проекта
    или группы проектов. Этот тип раннера позволяет настроить его под конкретные
    нужды проекта или группы проектов
    - Group Runner (раннер группы): создается для группы проектов. Этот
    тип раннера позволяет настроить его для группы проектов, что упрощает
    управление задачами CI/CD для нескольких проектов
    - Project Runner (раннер проекта): создается для одного проекта.
    Этот тип раннера позволяет настроить его под конкретные нужды одного проекта

    Раннеры можно классифицировать по типу исполняемой задачи:
    - Docker Runner: исполняет задачи в контейнерах Docker.
    - Shell Runner: исполняет задачи в оболочке операционной системы.
    - VirtualBox Runner: исполняет задачи в виртуальной машине VirtualBox.
    - Kubernetes Runner: исполняет задачи в кластере Kubernetes.
```

```txt
2 - Какие есть триггеры запуска пайплайнов в GitLab CI?

->  - Push: пайплайн запускается при push-коммите в репозиторий.
    - Merge Request: пайплайн запускается при создании или
    обновлении merge request.
    - Scheduled: пайплайн запускается по расписанию, которое можно
    настроить в файле .gitlab-ci.yml.
    - Manual: пайплайн запускается вручную, когда пользователь 
    нажимает кнопку "Run pipeline" в интерфейсе GitLab.
    - API: пайплайн запускается через API GitLab, что позволяет
    запускать пайплайны извне GitLab.
    - Webhook: пайплайн запускается при получении webhook-уведомления
    от внешнего сервиса.
```

### Intern-3

```txt
1 - Как подключить новый раннер?

->  - Скачать и установить GitLab Runner: скачайте и установите GitLab
    Runner на сервер или виртуальную машину, где будет работать раннер.
    - Зарегистрировать раннер: зарегистрируйте раннер в GitLab, указав
    URL-адрес GitLab и токен регистрации раннера.
    - Настроить конфигурацию раннера: настройте конфигурацию раннера,
    указав исполняемую среду (например, Docker, Shell) и другие необходимые параметры.
    - Запустить раннер: запустите раннер, используя команду gitlab-runner start.
    - Проверить статус раннера: проверьте статус раннера в GitLab, перейдя в
    раздел "CI/CD" > "Раннеры" и найдя раннер в списке.

    gitlab-runner register 
    --url https://your-gitlab-instance.com 
    --token your-registration-token
```

```txt
2 - Как сделать так, чтобы пайплайн запускался только при открытии MR
    в ветку master?

->  Можно использовать условие rules в файле .gitlab-ci.yml
    rules:
        - if: '$CI_PIPELINE_SOURCE == "merge_request_event" && 
        $CI_MERGE_REQUEST_TARGET_BRANCH == "master"'
    Также можно использовать условие only вместо rules:
    only:
        - merge_requests
        - master
    В обоих случаях необходимо указать when: on_success или when: always,
    чтобы указать, когда пайплайн должен быть запущен.
```

```txt
3 - Как работать с секретами в GitLab CI?

->  - Variables: можно создать переменные окружения в разделе
    "CI/CD" > "Variables" в GitLab. Эти переменные можно
    использовать в файле .gitlab-ci.yml как $VARIABLE_NAME.

    - Secrets: можно создать секреты в разделе
    "CI/CD" > "Secrets" в GitLab. Эти секреты
    можно использовать в файле .gitlab-ci.yml как $SECRET_NAME.

    - Environment variables: можно создать переменные окружения
    в файле .gitlab-ci.yml используя ключевое слово environment.

    variables:
        SECRET_KEY: $SECRET_KEY
    script:
        - echo "Secret key is $SECRET_KEY"

    secrets:
        SECRET_KEY: $SECRET_KEY
    script:
        - echo "Secret key is $SECRET_KEY"
```

### Advanced-3

```txt
1 - Как можно переиспользовать код пайплайнов в GitLab CI?

->  - Включение файлов: можно включить файлы .gitlab-ci.yml
    из других репозиториев или директорий используя ключевое слово include.
    include:
        - project: 'my-group/my-project'
          file: '.gitlab-ci.yml'

    - Вложенные пайплайны: можно создать вложенные пайплайны,
    которые наследуют конфигурацию родительского пайплайна.
    stages:
        - build
        - test
    build:
        stage: build
        script:
            - echo "Building..."
    test:
        stage: test
        script:
            - echo "Testing..."
    include:
        - local: 'nested-pipeline.yml'

    - Шаблоны пайплайнов: можно создать шаблоны пайплайнов,
    которые можно использовать в нескольких проектах.
    template:
        - project: 'my-group/my-template'
          file: '.gitlab-ci.yml'
    
    - Библиотеки пайплайнов: можно создать библиотеки пайплайнов,
    которые содержат повторно используемый код.
    library:
        - project: 'my-group/my-library'
          file: 'pipeline-library.yml'

    - Микросервисы: можно создать микросервисы, которые предоставляют
    повторно используемый функционал.
    microservice:
        - project: 'my-group/my-microservice'
          file: 'microservice.yml'

    - Пайплайны как код: можно хранить пайплайны как код в отдельном
    репозитории и включать их в другие проекты.
    pipeline:
        - project: 'my-group/my-pipeline'
          file: '.gitlab-ci.yml'
```

```txt
2 - Как запустить стадии пайплайна параллельно? В каких ситуациях может
    потребоваться параллельный запуск стадий пайплайна?

->  В GitLab CI можно запустить стадии пайплайна параллельно, используя
    ключевое слово parallel в файле .gitlab-ci.yml.

    stages:
        - build
        - test
        - deploy

    build:
        stage: build
        script:
            - echo "Building..."

    test:
        stage: test
        script:
            - echo "Testing..."

    deploy:
        stage: deploy
        script:
            - echo "Deploying..."

    parallel:
        - build
        - test
    
    В этом примере стадии build и test будут запущены параллельно.

    Параллельный запуск стадий пайплайна может потребоваться в следующих
    ситуациях:
    - Ускорение процесса сборки: если у вас есть несколько стадий сборки,
    которые не зависят друг от друга, вы можете запустить их параллельно,
    чтобы ускорить процесс сборки.
    - Параллельное тестирование: если у вас есть несколько наборов тестов,
    которые не зависят друг от друга, вы можете запустить их параллельно,
    чтобы ускорить процесс тестирования.
    - Разделение ресурсов: если у вас есть несколько стадий пайплайна,
    которые требуют разных ресурсов (например, CPU, память), вы можете
    запустить их параллельно, чтобы разделить ресурсы и ускорить процесс.
    - Уменьшение времени ожидания: если у вас есть несколько стадий пайплайна,
    которые требуют ожидания (например, ожидание ответа от внешнего сервиса),
    вы можете запустить их параллельно, чтобы уменьшить время ожидания.

    Однако, параллельный запуск стадий пайплайна также может привести
    к следующим проблемам:
    - Конфликты ресурсов: если несколько стадий пайплайна требуют одних
    и тех же ресурсов, это может привести к конфликтам и замедлению процесса.
    - Сложность управления: параллельный запуск стадий пайплайна может
    усложнить управление процессом и отслеживание ошибок.
```

## <a id="Основы-Jenkins">Основы Jenkins</a>

```txt
1  - Установка Jenkins. 
2  - Основные плагины.
3  - Подключение и настройка агентов.
4  - Понятие Pipeline, Build, Job, Stage, Jenkinsfile.
5  - Декларативный синтаксис пайплайнов.
6  - Триггеры запуска пайплайнов. 
7  - Работа с секретами.
8  - Запуск тестов в пайплайне.
9  - Docker-агент.
10 - Post-build actions.
11 - Jenkins Best Practice.
```

### Notice-4

```txt
1 - Что такое Jenkins-агент? Как добавить новый агент?

->
```

```txt
2 - Почему не рекомендуется запускать пайплайны на мастере?

->
```

```txt
3 - Что такое Job, Build и pipeline в Jenkins? Какая между ними взаимосвязь?

->
```

```txt
4 - Какие виды синтаксиса пайплайнов поддерживает Jenkins? В чем отличия между ними?

->
```

```txt
5 - Какие есть тригеры запуска пайплайнов в Jenkins?

->  
```

### Intern-4

```txt
1 - Как работать с секретами в Jenkins?

->
```

```txt
2 - Как запустить определенную стадию пайплайна в Docker-контейнере?

->
```

```txt
3 - Как гарантировать, что определенные шаги пайплайна будут выполнены в
    любом случае, независимо от того, успешно завершился пайплайн или нет?

->
```

```txt
4 - Что означает статус билда UNSTABLE?

->
```

```txt
5 - Как запускать пайплайн по вебхуку?

->  
```

```txt
6 - Как запускать отдельные стадии пайплайна параллельно друг с другом?

->  
```

### Advanced-4

```txt
1 - Как запускать Jenkins-пайплайн из консоли?

->
```

```txt
2 - Как запускать Jenkins-пайплайн из другого Jenkins-пайплайна?

->
```
