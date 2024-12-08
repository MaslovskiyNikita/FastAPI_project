# Backend
## Guideline for git

   1. Форкаем данный репозиторий (В github)
   2. Клонируем данный репозиторий на ваш ПК (git clone https://github.com/TevenixLevelUps/Backend)
   2. Жестко чет пишем
   3. Добавляем изменения в staging (git add .)
   4. Фиксируем прибыль (изменения) (git commit -m "Some title for commit.")
   5. Отправляем изменения в удаленный репозиторий (git push -u https://github.com/TevenixLevelUps/Backend)
   6. Создаем PR в вашем удаленном github репозитории. Укажите ФИО и ссылку на ТГ.
   Будут вопросы - обращайтесь в группу левелапов дабы избежать повторяющихся вопросов. Стесняетесь - @timoxgagarin

## Task 1

Необходимо создать CRUD для сайта барбершопа. Это подразумевает наличие следующих объектов:

1. Услуги
- id
- название
- описание
- цена
- время для исполнения
- картинка (*)

2. Специалисты
- id
- имя
- аватарка (*)

3. Заказы
- id
- имя заказчика
- id услуги
- id специалиста
- время заказа

### Основные условия:
Вам надо добавить эндпоинты для:
- CRUD услуг
- CR-D специалистов
- CR-D заказов


Обратите внимание, что пользователь не знает id ваших услуг и специалистов)
Сделайте так, чтобы нельзя было делать заказы у специалиста во время, когда он занят (403 Forbidden)
Абстракции приветствуются (в следующей лекции мы рассмотрим работу с бд, с абстракциями вам будет проще перенести ваш код на новую систему хранения данных).
На данный момент храните ваши данные в словарях, где id это ключ, а схема - значение.

### Дополнительные условия
- Сделайте красивой документацию
- Подключите CORS
- Сделайте свой Middleware для предотвращения DoS/DDoS
- Кастомные фичи приветствуются, но не уходим за рамки имеющихся эндпоинтов

P.S. Помните, это все делать не обязательно. Все это делается дабы вы закрепили пройденый материал и изучили что-то новое. Будут вопросы - обращайтесь в группу левелапа.

# Task 2

Подключите SQLAlchemy к вашему проекту. Не забудьте про миграции через alembic.

# Task 3

Подключите Redis к вашему проекту. Попробуйте кэшировать GET запросы и инвалидировать кэш при остальных видах запросов. Замените реализацию RateLimit с Middleware на реализацию через Redis.

# Task 4

Покройте тестами ваш проект (юнит и интеграционными). Добавьте pre-commit файл для прогонки линтеров. 

Задачки со звездочкой:
1. Настройте CI пайплайн для Github Actions.
2. Напишите 1 e2e тест.

# Task 5

Разделите приложение на несколько контейнеров и напишите docker-compose.yml для их совместного запуска
