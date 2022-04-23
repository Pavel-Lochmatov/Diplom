Для запуска автотестов требуется:

1. Должен быть установлен на компьютере Docker например Docker desktop

2. В IntelliJ IDEA должен быть установлен плагин Docker

3. Выкачать репозиторий с помощью команды git clone

4. Открыть его в IntelliJ IDEA

5. В терменале запустить команду docker-compose up

6. Из папки artifacts запустить jar файл командой java -jar aqa-shop.jar

7. Открыть еще один терменал и запустить команду   ./gradlew clean test

8. Отчеты по тестированию можно просмотреть в папках build\allure-results, build\reports