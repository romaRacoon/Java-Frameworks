# Java-Frameworks
## Работа с БД. JDBC и Hibernate.
### [Задача 1](https://github.com/romaRacoon/PP1_1)
Задание:
1. Пройти 2 первых блока в приложении https://learngitbranching.js.org (Введение и Едем дальше).
2. Создать Git репозиторий на GitHub и залить туда пустой проект.
3. Склонируйте себе свой проект, используя IDE. Для этого необходимо выполнить следующие действия:

 1. На верхней панели найдите вкладку file -> new -> Project from Version Control...  
 2. В открывшемся окне, необходимо вставить в поле для ввода ссылку на репозиторий и нажать кнопку clone. Ссылку на репозиторий можно получить, нажав на кнопку Clone в вашем репозитории на https://github.com

### [Задача 2](https://github.com/romaRacoon/PP1_1)
Задание:
В этом задании мы познакомимся с такими технологиями, как:

 Maven  - https://maven.apache.org/
 JDBC - https://o7planning.org/ru/10167/java-jdbc-tutorial
 

Для выполнения задания необходимо:

 Клонировать/скачать заготовку по ссылке
 Установить на компьютер MySqlServer и Workbench. Создать подключение и схему через Workbench. Протестировать возможность соединения с базой через идею с помощью встроенной утилиты, как показано на рисунке:
Описание задачи:

Необходимо ознакомиться с заготовкой и доработать приложение, которое взаимодействует с базой оперируя пользователем ( класс User ) и проверить свои методы заранее написанными JUnit тестами. По итогу все тесты должны быть пройдены. Разрешается посмотреть реализацию тестов.

Для запуска теста необходимо найти класс в папке test ( показано в предыдущей лекции ) и при нажатии на него правой кнопкой мыши запустить, выбрав Run "Имя класса" 

Класс UserHibernateDaoImpl в рамках этой задачи не затрагивается (остаётся пустой)

User представляет из себя сущность с полями:

Long id
String name
String lastName
Byte age
         Архитектура приложения создана с опорой на паттерн проектирования MVC ( частично, у нас не WEB приложение)

Ознакомиться с паттерном можно здесь

 

Требования к классам приложения:

 Классы dao/service должны реализовывать соответствующие интерфейсы
 Класс dao должен иметь конструктор пустой/по умолчанию
 Все поля должны быть private
 service переиспользует методы dao
 Обработка всех исключений, связанных с работой с базой данных должна находиться в dao
 Класс Util должен содержать логику настройки соединения с базой данных
 

Необходимые операции:

 Создание таблицы для User(ов) – не должно приводить к исключению, если такая таблица уже существует
 Удаление таблицы User(ов) – не должно приводить к исключению, если таблицы не существует
 Очистка содержания таблицы
 Добавление User в таблицу
 Удаление User из таблицы ( по id )
 Получение всех User(ов) из таблицы
       

        Алгоритм работы приложения:

         В методе main класса Main должны происходить следующие операции:

 Создание таблицы User(ов)
 Добавление 4 User(ов) в таблицу с данными на свой выбор. После каждого добавления должен быть вывод в консоль ( User с именем – name добавлен в базу данных )
 Получение всех User из базы и вывод в консоль ( должен быть переопределен toString в классе User)
 Очистка таблицы User(ов)
 Удаление таблицы

### [Задача 3](https://github.com/romaRacoon/PP1_1)
В этом задании мы познакомимся с фреймворком Hibernate и научимся взаимодействовать с помощью него с базой данных.

Для выполнения задания необходимо:

 Ознакомиться с Hibernate. Подробнее узнать о Hibernate можно Здесь 
 Готовая прошлая задача ( работа будет происходить в этом же проекте )
 

Описание задачи:

В прошлой задаче мы познакомились с Maven и JDBC, доработали приложение, взаимодействующее с базой данных.

На этот раз обратим внимание на класс UserHibernateDaoImpl, который реализует тот же интерефейс, что и UserDaoJdbcImpl.

В рамках этой задачи необходимо реализовать взаимодействие с базой данных с помощью Hibernate и дописать методы в классе UserHibernateDaoImpl, проверить свои методы заранее написанными JUnit тестами из заготовки.

 

   Требования к классам приложения:

 UserHibernateDaoImpl должен реализовывать интерефейс UserDao
 В класс Util должна быть добавлена конфигурация для Hibernate ( рядом с JDBC), без использования xml.
 Service на этот раз использует реализацию dao через Hibernate
 Методы создания и удаления таблицы пользователей в классе UserHibernateDaoImpl должны быть реализованы с помощью SQL.
 

  Алгоритм приложения и операции не меняются в сравнении с предыдущим заданием.
