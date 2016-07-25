
## Описание

Web cервис отвечающий за конвертацию единиц измерений. 
Пример работы: Пользователь делает запрос по `http://unit.converter/convert/?from=kg&to=g&value=100`. В ответ пользователь получает `100000`

## План работ(первые шаги)

- Проектирование API
  - В swagger editor проектируем структуру будущего API
  - Сохранить готовую структуру в `swagger.yml`
- Проектирование БД
  - Определиться с таблицами
  - Определиться с полями и индексами
  - Сохранить готовую схему временно в `shema.example.sql`
- Организация окружения при помощи Docker
  - Разобраться с Docker
  - Поиск нужного контейнера или создание своего
    - Установка нужных нам библиотек в нем?
      - mysql?
  - Реализация запуска через docker-compose с подключением контейнера `mysql`
- Создание базового приложения
  - Реализация основного контроллера управления величинами - /measures/
    - Показывать список существующих величин в базе данных


## Возможности

- Получение списка величин по роутеру `/measures/`
- Получение списка единиц в т.ч. с фильтрацией по величине по роутеру `/units/`
- Конвертация единич измерений в т.ч. массово по роутеру`/convert/`

## Технологии

- MySQL
- Python
- Docker
- Swagger

## Полезные ссылки

- [swagger editor](http://editor.swagger.io/#/)

## Похожие сервисы

- [npm module](https://www.npmjs.com/package/convert-units)
- [online converter](http://converter.eu/api/)
- [unit converter](http://www.unitconverters.net/)
- [convert me](http://www.convert-me.com/ru/)
- [extended converter](http://www.onlineconversion.com/)
- [dutsch converter](https://www.digitaldutch.com/unitconverter/density.htm)
