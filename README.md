# Привет, я Руслан 👋

**Python Backend Developer.** Пишу REST API на FastAPI: от моделей и миграций до авторизации, кэша, тестов и запуска в Docker.

## 💪 Сильные стороны

- **Быстро осваиваю новое.** Redis-кэш, обработчики исключений FastAPI и тесты на pytest с подменой зависимостей освоил и внедрил в свой проект за несколько дней — с нуля до рабочего результата.
- **Нормально воспринимаю code review.** Прохожу ревью своего кода, разбираюсь в каждом замечании и исправляю итерациями, пока всё не заработает правильно, а не «лишь бы прошло».
- **Докапываюсь до причины.** Не ограничиваюсь «у меня работает»: проверяю граничные случаи — просроченный токен, чужой заказ, запрещённый переход статуса, недоступный Redis.
- **Думаю о безопасности.** Пароли только в виде хешей Argon2, права по ролям, клиент не видит чужие данные, секреты не попадают в Git.
- **Довожу до запуска.** Проект поднимается одной командой в Docker Compose, с миграциями, healthcheck и понятным README.

## 🛠 Стек

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy_2-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker_Compose-2496ED?style=flat&logo=docker&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

- **Backend:** FastAPI, Pydantic, SQLAlchemy 2, Alembic
- **Данные:** PostgreSQL, Redis (кэширование)
- **Безопасность:** JWT, хеширование паролей Argon2, разграничение прав по ролям
- **Инфраструктура:** Docker, Docker Compose
- **Тестирование:** Pytest, TestClient, подмена зависимостей FastAPI

## 🚀 Проекты

### [OrderFlow Backend](https://github.com/AlphaZero-developer/OrderFlowBackend)
REST API сервиса заказов: клиент создаёт заказ и следит за его статусом, менеджер ведёт заказы всех клиентов.

- Регистрация и вход по JWT, пароли хранятся в виде хешей Argon2
- Роли `client` и `manager`: клиент видит только свои заказы, менеджер — все
- Жизненный цикл заказа с таблицей допустимых переходов статусов
- Кэш списков заказов в Redis с инвалидацией после изменений; при недоступном Redis API продолжает работать через PostgreSQL
- Единая обработка ошибок через собственные исключения и обработчики FastAPI
- Миграции Alembic, запуск в Docker Compose (API, PostgreSQL, Redis) с healthcheck
- Тесты на pytest: права доступа, переходы статусов, ошибки, обновление кэша

`FastAPI` `SQLAlchemy 2` `PostgreSQL` `Redis` `Alembic` `JWT` `Pytest` `Docker Compose`

### [Todo Backend](https://github.com/AlphaZero-developer/todo-backend)
REST API списка задач, который запускается в Docker Compose одной командой.

- CRUD задач на FastAPI + PostgreSQL
- Кэширование списка задач в Redis со сбросом при любом изменении
- Разделение на routers, services, repositories
- Запуск в один клик на Windows (`start.bat`)

`FastAPI` `PostgreSQL` `Redis` `Docker Compose`

## 📚 Сейчас изучаю

- Брокеры сообщений: **RabbitMQ** — очереди, обменники, гарантии доставки
- Микросервисную архитектуру и асинхронное взаимодействие сервисов через очереди
- Асинхронный Python: async SQLAlchemy и async-эндпоинты FastAPI

## 📫 Контакты

[![Telegram](https://img.shields.io/badge/Telegram-@antistress__67-26A5E4?style=flat&logo=telegram&logoColor=white)](https://t.me/antistress_67)
[![Email](https://img.shields.io/badge/Email-csgomail152@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:csgomail152@gmail.com)
