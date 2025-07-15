# Проект по автоматизации тестирования API системы eDiscovery

## Используемые инструменты:
1. Язык программирования — Java 17
2. Стратегия тестирования — Пятиуровневая модель тестирования API
3. Сборщик проекта — Gradle
4. Отчетность — Allure Report
5. Тестовый фреймворк — JUnit 5
6. Библиотека для тестирования RestFulApi - Rest Assured
7. Библиотека для работы с базами данных - postgresql
8. CI/CD - Jenkins
9. Вспомогательные библиотеки: AssertJ, Lombok, Faker, Gson, Jackson

## Структура проекта (пакеты):
- apiMethods - пакет с классами-фасадами взаимодействиями с сущностями
![image](/images/project_structure/apiMethods.png)

- dao - пакет для работы с сущностями напрямую через sql (создание, чтение, удаление записей)
![image](/images/project_structure/dao.png)

- databases - пакет для работы с базами данных PostgreSQL, SQLite
![image](/images/project_structure/databases.png)

- dataGenerators - пакет с классами-фасадами для упрощённого взаимодействия с сущностями по API
![image](/images/project_structure/dataGenerators.png)

- dataProviders - пакет с провайдерами тестовых данных для параметризованных тестов
![image](/images/project_structure/dataProviders.png)

- dbEntities - пакет с моделями сущностей в sql
![image](/images/project_structure/dbEntities.png)

- helpers - вспомогательные классы (enum-ы, используемые на бэке; эталонные данные; отслеживание и очистка создаваемых сущностей; логгирование http запросов и ответов в отчёт allure, тексты ошибок для негативных текстов)
![image](/images/project_structure/helpers.png)

- models - пакет с моделями сущностей для API
![image](/images/project_structure/models.png)

- spec - пакет со спецификациями запросов и ответов
![image](/images/project_structure/spec.png)

- tests - пакет с тестовыми классами. Для каждого уровня тестов используется отдельный пакет с классами. Внутри тестового класса используются Nested - классы для группировки тестов
![image](/images/project_structure/tests.png)


## Отчёт от тестировании:
### Суммарная информация об итогах тестирования
![image](/images/test_report/overview.png)

### Отчёт о тестах в разрезе сьютов
![image](/images/test_report/suites.png)

### Графики с процентным соотношением успешных/неуспешных, пропущенных тестов; соотношению количества тестов по важности/продолжительности
![image](/images/test_report/graphs.png)

### Отчёт о тестировании в разрезе Epic / Feature / Story
![image](/images/test_report/behaviors.png)

### Тестовый сценарий состоит из шагов с детальной информацией по выполнению каждого шага
![image](/images/test_report/steps.png)
![image](/images/test_report/requestDetails.png)


### Для Smoke и Sanity тестов в gradle создаются отдельные задачи для более узкого тестирования (используются тэги)
![image](/images/project_structure/gradleTasks.png)


### Тестовые сценарии привязываются к задачам / дефектам
![image](/images/test_report/links.png)


### При запуске автотестов в CI/CD отображается тренд результатов автотестов с учётом предыдущих запусков
![image](/images/test_report/trend.png)


### После выполнения тестов, отчёт о тестировании упаковывается в единый html файл
![image](/images/project_structure/gradleSingleReport.png)

