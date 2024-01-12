Этот репозиторий содержит скрипты Python для автоматизированного создания интентов в DialogFlow и их использования в VK и Telegram ботах. 
## Как установить
Python3 должен быть уже установлен. Затем используйте pip (или pip3, есть конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```
### Настройка переменных окружения.
Часть настроек скрипта берётся из переменных окружения. Чтобы их определить, создайте файл `.env` и запишите туда данные в таком формате: `ПЕРЕМЕННАЯ=значение`.
Для Telegram-бота нужно зарегистрироваться у BotFather и получить токен. Больше информации можно получить на сайте [way23.ru](https://way23.ru/).
Доступные переменные:
`TG_TOKEN` — API ключ, который вы получаете при создании бота в Telegram
`TG_CHAT_ID`— идентификатор пользователя telegram для получения логов
`VK_TOKEN` — API ключ, который вы получаете при создании группы в ВКонтакте
`PROJECT_ID` — ProjectID, который вы получили, когда создавали проект в DialogFlow
`GOOGLE_APPLICATION_CREDENTIALS` — путь до файла application_default_credentials
## Использование
Создание интентов в DialogFlow

Выполните скрипт dialogflow_intent.py для создания интентов в [DialogFlow](https://dialogflow.cloud.google.com/).
```sh
python dialogflow_intent.py
```
## Тренировка бота
Тренировать бота можно с помощью скрипта dialogflow_intent.py, который запускается следующей командой
```sh
python dialogflow_intent.py --p [путь до файла json]
```

Запуск скрипта в telegram командой:
```sh
python telegram_bot.py
```
Запуск скрипта в VK командой:
```sh
python vk_bot.py
```
Пример использования в telegram:
![Verb_play_tg.gif](gif%2FVerb_play_tg.gif)

Пример использования в VK:
![Verb_play_vk.gif](gif%2FVerb_play_vk.gif)

## Цели проекта
Код написан в образовательных целях на онлайн-курсе для веб-разработчиков [dvmn.org](https://dvmn.org/)