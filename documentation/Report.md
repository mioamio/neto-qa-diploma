# Отчет по итогам автоматизированного тестирования

### **Краткое описание**

Автоматизация тестирования выполнялась с использованием следующих инструментов:

* **Junit 5** 

```
 testImplementation 'org.junit.jupiter:junit-jupiter:5.7.2'
```

* **Selenide** 

```
testImplementation 'com.codeborne:selenide:5.23.0'
```

* **Allure** 

```
testImplementation 'io.qameta.allure:allure-selenide:2.14.0'
```

Для работы с БД и симулятором банковских сервисов использовался [Docker](https://www.docker.com/products/docker-desktop)

Отчет Gradle:


![test](https://user-images.githubusercontent.com/98706916/234461595-e7bf2017-6e5b-4cb6-9df8-dcb4e131e3c9.jpg)

### **Отчет Allure:**

![test](https://user-images.githubusercontent.com/98706916/235362193-d7fbc19d-4080-4809-bcd4-57edc5634be1.jpg)

Ссылки на найденные ошибки:

- Сумма оплаты тура в базе данных при оплате отличается https://github.com/mioamio/neto-qa-diploma/issues/1
- Неподходящее название в заголовке страницы https://github.com/mioamio/neto-qa-diploma/issues/2
- Двойное уведомление при отправке запроса с не валидным номером карты https://github.com/mioamio/neto-qa-diploma/issues/3
- Неправильное поведение отображения сообщения об ошибке под полем ввода после исправления https://github.com/mioamio/neto-qa-diploma/issues/4
- Падение веб-сервера при отправке некорректным значением поля "Номер карты" https://github.com/mioamio/neto-qa-diploma/issues/5
- Неполная валидация поля "Месяц" https://github.com/mioamio/neto-qa-diploma/issues/6
- Неполная валидация поля "CVC/CVV" https://github.com/mioamio/neto-qa-diploma/issues/7
- Отсутствует валидация поля "Владелец" https://github.com/mioamio/neto-qa-diploma/issues/8
- Операция проходит успешно при отправке карты со статусом DECLINED https://github.com/mioamio/neto-qa-diploma/issues/9
- Отображение кредитной истории в базе данных при оплате в кредит не записывается https://github.com/mioamio/neto-qa-diploma/issues/10
