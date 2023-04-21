# Дипломный проект по профессии «Тестировщик»

## **Процедура запуска авто-тестов**

### Перед запуском авто-тестов необходимо установить:

* [Docker Desktop](https://www.docker.com/products/docker-desktop)

### Запуск авто-тестов:

1. Запустить контейнеры СУБД MySQl, PostgerSQL и Node.js командой в терминале:

```
docker-compose up -d
```

2. Запустить SUT, работающей на СУБД MySQl командой:

```
java -Dspring.datasource.url=jdbc:mysql://localhost:3306/app -jar artifacts/aqa-shop.jar
```

на СУБД PostgreSQL командой:

```
java -Dspring.datasource.url=jdbc:postgresql://localhost:5432/app -jar artifacts/aqa-shop.jar
```

3. В новом терминале запустить авто-тесты командой для MySQL:

```
gradlew clean test -Durl=jdbc:mysql://localhost:3306/app
```

для PostgreSQL:

```
gradlew clean test -Durl=jdbc:postgresql://localhost:5432/app
```

4. Сгенерировать отчеты двумя командами:

```
gradlew allureReport
```

```
gradlew allureServe
```

5. Остановить и удалить все контейнеры командой:

```
docker-compose down 
```

## **Документация**

* [План автоматизации тестирования](https://github.com/mioamio/neto-qa-diploma/blob/main/documentation/Plan.md)
* [Отчет по итогам автоматизированного тестирования](https://github.com/mioamio/neto-qa-diploma/blob/main/documentation/Report.md)
* [Отчет по итогам автоматизации](https://github.com/mioamio/neto-qa-diploma/blob/main/documentation/Summary.md)
