Для запуска автотестов требуется:

для проверки работы с базой данных MySql:

1. Должен быть установлен на компьютере Docker например Docker desktop

2. В IntelliJ IDEA должен быть установлен плагин Docker

3. Выкачать репозиторий с помощью команды git clone

4. Открыть его в IntelliJ IDEA

5. В новом окне терминала запустить команду docker-compose up

6. В новом окне терминала из папки artifacts запустить jar файл командой java -jar aqa-shop.jar

7. В новом окне терминала запустить тесты с указанием подключения к конкретной базе данных командой
 ./gradlew test --info "-Durl=jdbc:mysql://localhost:3306/app" "-Duser=user" "-Dpass=pass" ( подробные логи) или командой 
 ./gradlew test "-Durl=jdbc:mysql://localhost:3306/app" "-Duser=user" "-Dpass=pass" ( без подробных логов)

8. Отчеты по тестированию можно просмотреть в папках build\allure-results, build\reports

для проверки работы с базой данных Postgres:

1. Должен быть установлен на компьютере Docker например Docker desktop

2. В IntelliJ IDEA должен быть установлен плагин Docker

3. Выкачать репозиторий с помощью команды git clone

4. Открыть его в IntelliJ IDEA

5. В новом окне терминала запустить команду docker-compose up

6. В файле application.properties в папке artifacts закоментировать строки подключения к базе данных mysql и раскоментировать строки подключения к postgres :

spring.datasource.url=jdbc:postgresql://localhost:5432/appps
spring.datasource.username=userps
spring.datasource.password=passps

7. В новом окне терминала из папки artifacts запустить jar файл командой java -jar aqa-shop.jar

8. В новом окне терминала запустить тесты с указанием подключения к конкретной базе данных командой
 ./gradlew test --info "-Durl=jdbc:postgresql://localhost:5432/appps" "-Duser=userps" "-Dpass=passps" ( подробные логи) или командой 
 ./gradlew test "-Durl=jdbc:postgresql://localhost:5432/appps" "-Duser=userps" "-Dpass=passps" ( без подробных логов)

9. Отчеты по тестированию можно просмотреть в папках build\allure-results, build\reports
