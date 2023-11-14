# Описание
Это веб-приложение на Python, разработанное для анализа и определения соответствия входящих данных известным шаблонам форм. Приложение принимает данные через POST-запросы и сравнивает их с рядом предопределенных шаблонов. В случае отсутствия соответствия, приложение автоматически типизирует поля и возвращает список полей с определенными типами.

## Установка и настройка

Для начала работы с приложением выполните следующие шаги:

1. Убедитесь, что на вашей машине установлен **Python** версии **3.6 и выше.**

2. Установите необходимые зависимости, используя команду:

**pip install -r requirements.txt**

3. Запустите сервер разработки:

**python manage.py runserver**

После этих шагов приложение будет доступно по адресу: **`http://127.0.0.1:8000/`.**

## Использование

- Отправьте POST-запрос с данными в формате `f_name1=value1&f_name2=value2` на URL `/get_form/`. 
- В ответе вы получите имя подходящего шаблона формы или список полей с их типами, если соответствующий шаблон не найден.

### Примеры запросов

**POST-запрос с известной формой:**

POST http://127.0.0.1:8000/get_form/
Data: email=test@example.com&phone=+7 123 456 78 90


**POST-запрос с неизвестной формой:**

POST http://127.0.0.1:8000/get_form/
Data: custom_field1=value1&custom_field2=2023-11-14

## База данных

В проекте используется TinyDB как основная система управления базой данных. Данные о шаблонах форм хранятся в файле `db.json`, который включен в состав проекта.

## Запуск тестов

Тесты можно запустить следующей командой:
**python manage.py test GetForm**


## Дополнительная информация

- **Python**: Приложение разработано на Python версии 3.12.


## Ссылка на репозиторий

[Ссылка на репозиторий проекта](https://github.com/MemphisAton/Test-e.Kom.git)

## Контактная информация

- **E-mail**: MemphisAton@gmail.com
- **Telegram**: [@MemphisAton](https://t.me/MemphisAton)