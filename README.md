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
![image](https://github.com/user-attachments/assets/fb4ccbbf-277b-4711-a618-3b7136122342)

- dao - пакет для работы с сущностями напрямую через sql (создание, чтение, удаление записей)
![image](https://github.com/user-attachments/assets/8b72b933-b43a-454d-91d0-058dfa21aea8)

- databases - пакет для работы с базами данных PostgreSQL, SQLite
![image](https://github.com/user-attachments/assets/dea66f02-5c44-482d-bce9-d6e0ad580410)

- dataGenerators - пакет с классами-фасадами для упрощённого взаимодействия с сущностями по API
![image](https://github.com/user-attachments/assets/c7573fdb-6360-4b23-a607-b9a2f40dd0d3)

- dataProviders - пакет с провайдерами тестовых данных для параметризованных тестов
![image](https://github.com/user-attachments/assets/ffa0e12c-02ba-4cd7-bc45-1c0bdc88e57e)

- dbEntities - пакет с моделями сущностей в sql
![image](https://github.com/user-attachments/assets/78a767cf-13bd-4a84-924e-b1c2e895d7f2)

- helpers - вспомогательные классы (enum-ы, используемые на бэке; эталонные данные; отслеживание и очистка создаваемых сущностей; логгирование http запросов и ответов в отчёт allure, тексты ошибок для негативных текстов)
![image](https://github.com/user-attachments/assets/f57351a0-c0e2-4a81-a488-d68fed140a45)

- models - пакет с моделями сущностей для API
![image](https://github.com/user-attachments/assets/4ae7dedb-d920-45e5-a535-68f6341ef59d)

- spec - пакет со спецификациями запросов и ответов
![image](https://github.com/user-attachments/assets/07e3baf1-a465-4a40-b713-a0ba78a05943)

- tests - пакет с тестовыми классами. Для каждого уровня тестов используется отдельный пакет с классами. Внутри тестового класса используются Nested - классы для группировки тестов
![image](https://github.com/user-attachments/assets/e87bdd7f-2192-4963-9bd5-486e242333c2)


## Отчёт от тестировании:
### Суммарная информация об итогах тестирования
![image](https://github.com/user-attachments/assets/337022a0-2597-4eb3-ba8e-4623661ab918)

### Отчёт о тестах в разрезе сьютов
![image](https://github.com/user-attachments/assets/156eff00-2ab3-419a-84c4-09ffcb90b638)

### Графики с процентным соотношением успешных/неуспешных, пропущенных тестов; соотношению количества тестов по важности/продолжительности
![image](https://github.com/user-attachments/assets/df7dae79-ae6e-44e1-80de-e60bff267821)

### Отчёт о тестировании в разрезе Epic / Feature / Story
![image](https://github.com/user-attachments/assets/73c2b606-80a3-46df-8e71-2e8661b59542)

### Тестовый сценарий состоит из шагов с детальной информацией по выполнению каждого шага
![image](https://github.com/user-attachments/assets/fc92db68-bb3a-4d43-a022-a23250500461)
![image](https://github.com/user-attachments/assets/ebe642cb-7dd4-4869-bd3d-db36a6901818)


### Для Smoke и Sanity тестов в gradle создаются отдельные задачи для более узкого тестирования (используются тэги)
![image](https://github.com/user-attachments/assets/19416031-0705-4066-85e8-3854392e0c49)


### Тестовые сценарии привязываются к задачам / дефектам
![image](https://github.com/user-attachments/assets/6b34b3b9-ab6f-46d4-8a61-1e262915800d)


### При запуске автотестов в CI/CD отображается тренд результатов автотестов с учётом предыдущих запусков
![image](https://github.com/user-attachments/assets/a17ad3b0-89cd-49cd-932b-dc097c0cc341)


### После выполнения тестов, отчёт о тестировании упыковывается в единый html файл
![image](https://github.com/user-attachments/assets/cd49024f-b105-4691-89d5-8aea3d5f6d2e)

