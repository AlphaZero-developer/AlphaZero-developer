# Привет, я Руслан 👋

**Python Backend Developer | FastAPI · Microservices · PostgreSQL**

Разрабатываю backend веб-приложений: от проектирования архитектуры и бизнес-логики до межсервисного взаимодействия, работы с базами данных, авторизации, тестирования и развёртывания.

Работаю с **FastAPI, PostgreSQL, SQLAlchemy, Redis и Docker**. Изучаю распределённые системы, брокеры сообщений и событийное взаимодействие сервисов.

Основной проект — **Find Me**, сервис знакомств на базе Telegram Mini App с микросервисной архитектурой, системой рекомендаций, чатом, подписками и уведомлениями.

## 💪 Сильные стороны

- **Проектирование архитектуры.** Разделяю ответственность между API, сервисным слоем, доменной логикой и инфраструктурой. Использую Repository Pattern, Dependency Injection и Unit of Work там, где они решают конкретные задачи.
- **Микросервисный подход.** Работаю с разделением приложения на самостоятельные сервисы: API Gateway, профили, сообщения, платежи и уведомления. Уделяю внимание границам ответственности и взаимодействию компонентов.
- **Базы данных.** Проектирую модели и связи в PostgreSQL, использую SQLAlchemy 2, миграции Alembic и Redis для кэширования.
- **Безопасность.** JWT-авторизация, хеширование паролей Argon2, разграничение доступа по ролям, проверка прав на ресурсы, защита конфиденциальных данных.
- **Надёжность.** Проверяю пограничные сценарии, обработку ошибок, идемпотентность операций и поведение системы при отказах зависимостей.
- **Тестирование.** Пишу тесты с Pytest, проверяю API через TestClient, использую подмену зависимостей и изолированные тестовые базы данных.
- **Развёртывание.** Docker, Docker Compose, конфигурация окружения, миграции, healthcheck и воспроизводимый локальный запуск.

## 🛠 Технологический стек

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy_2-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

| Направление | Технологии и подходы |
|---|---|
| **Backend** | Python, FastAPI, Pydantic, REST API |
| **Базы данных** | PostgreSQL, SQLAlchemy 2, Alembic |
| **Кэширование** | Redis |
| **Архитектура** | Microservices, Layered Architecture, Clean Architecture, Repository Pattern, Unit of Work |
| **Безопасность** | JWT, Argon2, RBAC |
| **Инфраструктура** | Docker, Docker Compose, Healthchecks |
| **Тестирование** | Pytest, TestClient, Dependency Overrides |
| **В процессе изучения** | RabbitMQ, aio-pika, асинхронное взаимодействие через брокеры сообщений |

## 🏗 Архитектура и инженерные подходы

**Микросервисная архитектура**

Разделение крупного приложения на сервисы с самостоятельными зонами ответственности. Работа с межсервисными API, конфигурацией окружения и согласованной работой компонентов в Docker Compose.

**Асинхронность и обмен сообщениями**

Изучаю RabbitMQ и aio-pika для событийного взаимодействия сервисов, обработки фоновых задач и доставки сообщений через очереди.

**Работа с данными**

Реляционные модели PostgreSQL, миграции, управление транзакциями, ограничения уникальности, кэширование и согласованность данных.

**Разделение бизнес-логики**

HTTP-обработчики отвечают за транспортный уровень, application-сервисы управляют сценариями, domain содержит бизнес-правила, а infrastructure реализует доступ к внешним ресурсам.

## 🚀 Проекты

### [Find Me | Backend Showcase](https://github.com/AlphaZero-developer/FindMeShowcase)

**Публичная демонстрация архитектуры backend сервиса знакомств Find Me.**

Основной Find Me представляет собой Telegram Mini App с микросервисной архитектурой. В приложении выделены отдельные компоненты:

- **API Gateway:** входная точка для клиентских запросов.
- **Profiles Service:** анкеты, пользовательские данные и рекомендации.
- **Chat Service:** переписки и взаимодействие пользователей.
- **Payment Service:** подписки и платёжные сценарии.
- **Notifications Service:** уведомления и их обработка.

Основной продукт использует PostgreSQL, включая географические возможности PostGIS, и разворачивается как набор сервисов в Docker Compose.

**Публичный Showcase**

Репозиторий содержит изолированную, запускаемую демонстрацию ключевых backend-механизмов без раскрытия коммерческого исходного кода, платёжных интеграций и пользовательских данных.

Реализованы:

- Двусторонняя фильтрация анкет по предпочтениям пользователей.
- Географическая приоритизация рекомендаций.
- Система лайков и взаимных совпадений.
- Раскрытие контактов только после взаимного согласия.
- Идемпотентная обработка повторных реакций.
- Разделение на API, Application, Domain и Infrastructure.
- Repository Protocols и Unit of Work.
- Миграции Alembic, автоматизированные тесты Pytest.
- Интерактивный веб-интерфейс и Swagger API.
- Запуск через Docker Compose с PostgreSQL.

**Архитектурная особенность:** доменные правила не зависят от FastAPI и SQLAlchemy, а application-слой работает с абстракциями репозиториев.

Showcase не воспроизводит все микросервисы основного продукта. Его задача — продемонстрировать качество кода, архитектурные решения и проверяемую бизнес-логику.

`Python 3.12` `FastAPI` `SQLAlchemy 2` `PostgreSQL 17` `Alembic` `Pytest` `Docker Compose` `Clean Architecture`

**[Исходный код и инструкция по запуску](https://github.com/AlphaZero-developer/FindMeShowcase)**

---

### [OrderFlow Backend](https://github.com/AlphaZero-developer/OrderFlowBackend)

**REST API системы управления заказами с ролевой моделью, контролируемыми переходами статусов и Redis-кэшированием.**

- Регистрация и авторизация пользователей через JWT.
- Безопасное хранение паролей с Argon2.
- Разграничение доступа между `client` и `manager`.
- Контроль жизненного цикла заказа с таблицей допустимых переходов.
- Redis-кэширование списков заказов с инвалидацией при изменениях.
- Продолжение работы API через PostgreSQL при недоступности Redis.
- Централизованная обработка ошибок через собственные исключения.
- Разделение ответственности между routers, services и repositories.
- Миграции Alembic и контейнеризация через Docker Compose.
- Автоматизированные тесты прав доступа, бизнес-правил, ошибок и кэша.

`FastAPI` `SQLAlchemy 2` `PostgreSQL` `Redis` `Alembic` `JWT` `Pytest` `Docker Compose`

**[Исходный код](https://github.com/AlphaZero-developer/OrderFlowBackend)**

---

### [Todo Backend](https://github.com/AlphaZero-developer/todo-backend)

**REST API управления задачами с PostgreSQL и Redis.**

- CRUD-операции для задач.
- Хранение данных в PostgreSQL.
- Redis-кэширование списков задач.
- Инвалидация кэша при изменении данных.
- Разделение на routers, services и repositories.
- Контейнеризация через Docker Compose.
- Быстрый запуск в Windows через `start.bat`.

`FastAPI` `PostgreSQL` `Redis` `Docker Compose`

**[Исходный код](https://github.com/AlphaZero-developer/todo-backend)**

## 📚 Сейчас изучаю

Углубляюсь в backend-разработку и проектирование распределённых систем:

- **RabbitMQ и aio-pika:** exchanges, queues, routing keys, acknowledgements, retry-механизмы и обработка ошибок доставки.
- **Микросервисы:** границы сервисов, межсервисное взаимодействие, отказоустойчивость и согласованность данных.
- **Асинхронный Python:** asyncio, async SQLAlchemy, асинхронные HTTP-запросы через httpx.
- **Надёжность:** идемпотентность, обработка повторных событий, управление транзакциями и интеграционное тестирование.

## 📫 Контакты

[![Telegram](https://img.shields.io/badge/Telegram-@antistress__67-26A5E4?style=flat&logo=telegram&logoColor=white)](https://t.me/antistress_67)
[![Email](https://img.shields.io/badge/Email-csgomail152@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:csgomail152@gmail.com)

Открыт к предложениям по **Python Backend Development**, разработке API и backend-сервисов.
