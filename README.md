## `Статус сборки` [![Build status](https://ci.appveyor.com/api/projects/status/shgpba4lsgrsgf7d?svg=true)](https://ci.appveyor.com/project/AndryRusff/aqa-1-2)
# Тестирование API, CI
## Домашнее задание по курсу "Автоматизированное тестирование"
## Тема: «1.2. Тестирование API, CI», задание №1: «Настройка CI», задание №2: «JSON Schema»
### Задача
Часть 1
Подключить интергацию с Appveyor, badge необходимо разместить в файле README.md для отображения текущего статуса вашего проекта.
Часть 2
1. Добавить зависимость rest-assured
2. Включить проверку схемы.
Модифицируйте существующий тест так, чтобы он проверял соответствие схеме. Для этого:

      // код теста
      .then()
          .statusCode(200)
          // static import для JsonSchemaValidator.matchesJsonSchemaInClasspath
          .body(matchesJsonSchemaInClasspath("accounts.schema.json"))
      ;

### Что сделано:
	1. Задание №1 - настроен и подкючен CI AppVeyor, произведена проверка корректной работы (сделан коммит, содержащий ошибку).
	1. Задание №2:
		- Существующий тест модифицирован, чтобы он проверял соответствие Json Schema Validator;
		- Исправлена схема (найден способ валидации значения поля на два из возможных значения: "RUB" или "USD").
### Предварительные требования
- На компьютере пользователя должна быть установлена Intellij IDEA
### Установка и запуск
1. Склонировать проект на свой компьютер
	- открыть терминал Intellij IDEA 
	- ввести команду git clone https://github.com/AndryRusff/AQA-1-2/
1. Открыть склонированный проект 
1. Перейти во вкладку Terminal (Alt+F12) и запустить приложение командой java -jar artifacts/app-mbank.jar
1. Запустить авто-тесты в новой вкладке Terminal командой ./gradlew clean test
