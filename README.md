# Flower Shop

Flower Shop - это веб-приложение и Telegram-бот для онлайн-магазина цветов, разработанное с использованием Django и python-telegram-bot.

## Функциональность

- Веб-сайт:
  - Регистрация пользователей
  - Просмотр каталога цветов
  - Оформление заказа

- Telegram-бот:
  - Просмотр списка доступных товаров
  - Оформление заказа

## Установка

1. Клонируйте репозиторий:
   ```
   git clone https://github.com/your-username/flower-shop.git
   cd flower-shop
   ```

2. Создайте виртуальное окружение и активируйте его:
   ```
   python -m venv venv
   source venv/bin/activate  # Для Unix или MacOS
   venv\Scripts\activate  # Для Windows
   ```

3. Установите зависимости:
   ```
   pip install -r requirements.txt
   ```

4. Примените миграции:
   ```
   python manage.py migrate
   ```

5. Создайте суперпользователя:
   ```
   python manage.py createsuperuser
   ```

6. Запустите сервер разработки:
   ```
   python manage.py runserver
   ```

## Настройка Telegram-бота

1. Получите токен для вашего бота у [@BotFather](https://t.me/BotFather) в Telegram.
2. Создайте файл `telegram_bot_token.txt` в корневой папке проекта и вставьте в него токен.
3. Добавьте `TELEGRAM_BOT_TOKEN` в файл `settings.py`:
   ```python
   with open('telegram_bot_token.txt') as f:
       TELEGRAM_BOT_TOKEN = f.read().strip()
   ```

## Запуск Telegram-бота
