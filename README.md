# Привет, я Руслан 👋

### Backend Developer · Python / FastAPI · Go · PostgreSQL

Разрабатываю backend-системы, в которых важны **бизнес-логика, состояния, безопасность и предсказуемое поведение**, а не просто набор CRUD-эндпоинтов.

Мой опыт включает **реально использовавшийся Telegram backend на Go**, сервисы на Python/FastAPI, PostgreSQL, Redis, WebSocket, интеграции с AI API, тестирование и развёртывание через Docker. Умею разбираться в существующем коде, проектировать отдельные подсистемы и доводить приложение до рабочего состояния.

**Самая сильная работа в моём портфолио — [Mirohodec Warden](https://github.com/AlphaZero-developer/mirohodec-warden).** Это многофункциональный backend, который я разрабатывал для реального сообщества и запускал на VPS. В нём совмещены модерация нескольких чатов, антиспам, AI-персонаж, многопользовательская Mafia, хранилища данных и административная веб-панель.

Сейчас основной профессиональный фокус — **Python Backend Development**, проектирование API и развитие навыков построения надёжных сервисов.

---

## ⭐ Главный проект: [Mirohodec Warden](https://github.com/AlphaZero-developer/mirohodec-warden)

**Go backend для Telegram-сообществ: модерация, AI-персонаж Лайя, Mafia и административная платформа.**

Это **самый масштабный и технически насыщенный проект из представленных здесь**. В отличие от учебного API, система объединяет несколько независимых сценариев с долгоживущим состоянием, настройками отдельных сообществ и взаимодействием с внешними сервисами. Исходная версия работала на VPS и использовалась в реальном сообществе, в том числе в коммерческом контексте.

### Что реализовал

| Подсистема | Инженерные задачи |
|---|---|
| **Модерация нескольких чатов** | Индивидуальные настройки сообществ, предупреждения с истечением срока, автоматическая эскалация ограничений, защита администраторов |
| **Антиспам** | Анализ сообщений по временным окнам, повторов, ссылок, пересылок, упоминаний и других сигналов; страйки и cooldown-политики |
| **AI-персонаж Лайя** | Интеграция с внешним LLM API, контекст диалога, характер персонажа, ограничения ответов и фильтрация качества |
| **Многопользовательская Mafia** | Комнаты, роли, ночные действия, дневные обсуждения, голосование, переходы фаз, ELO, достижения и защита скрытой информации |
| **Хранение данных** | Адаптеры JSON и PostgreSQL, миграции SQL, перенос состояния между хранилищами |
| **Веб-управление** | Административная панель, HTTP API, серверная проверка Telegram Mini App init data, WebSocket для игровых сценариев |
| **Эксплуатация** | Docker, структурированные логи, Prometheus-метрики, graceful shutdown, обновление конфигурации |

### Какие задачи здесь действительно сложные

**Модерация — это политика, а не команда `/ban`.** Система должна учитывать действующие предупреждения, правила конкретного чата, защищённых пользователей и уже наложенные ограничения. Для эскалации наказаний выделена тестируемая доменная логика.

**Mafia — это машина состояний.** Игра проходит через регистрацию, распределение ролей, ночные и дневные фазы, голосование и завершение. Нужно контролировать допустимость действий, приватность ролей и согласованность состояния между запросами.

**AI-персонаж — отдельная подсистема.** Лайя не просто отвечает на сообщения: у неё есть контекст, заданная манера общения, обработка качества ответов и сценарии взаимодействия с участниками. При этом модерация может работать независимо от доступности внешней AI-модели.

**Один backend, несколько интерфейсов.** Telegram-обработчики, административный HTTP-сервер и игровые WebSocket-эндпоинты обращаются к общей логике и хранилищам.

### Что показывает публичный репозиторий

Публичная версия подготовлена для технического просмотра: удалены секреты, данные пользователей и конфигурация VPS, добавлены документация, CI и тесты. Часть политик выделена в независимые доменные модули; крупные файлы переработаны и ограничены 200 строками.

При этом я **не называю legacy-код идеальной Clean Architecture**: основная часть приложения исторически находится в `cmd/warden`, и архитектурный долг прямо описан в документации. Для меня качество инженерного решения включает понимание его ограничений, а не только красивую структуру папок.

`Go 1.23` `PostgreSQL` `JSON` `Telegram Bot API` `HTTP` `WebSocket` `AI API` `Docker` `Prometheus` `CI`

**[Открыть код, архитектуру и технический кейс →](https://github.com/AlphaZero-developer/mirohodec-warden)**

---

## 🚀 Другие backend-проекты

### [Find Me · Backend Showcase](https://github.com/AlphaZero-developer/FindMeShowcase)

**Публичная запускаемая демонстрация backend-логики сервиса знакомств Find Me.**

Основной продукт разрабатывается как Telegram Mini App с отдельными сценариями профилей, рекомендаций, переписок, платежей и уведомлений. В публичном showcase я изолировал ключевые правила, чтобы их можно было изучать, запускать и тестировать без приватной инфраструктуры.

- Взаимная фильтрация анкет и приоритет географии при поиске.
- Лайки, совпадения и раскрытие контактов только при согласии обеих сторон.
- Идемпотентность реакций и ограничения на уровне базы данных.
- Разделение **API → Application → Domain → Infrastructure**.
- Repository Protocols, Unit of Work, SQLAlchemy 2 и Alembic.
- Тесты Pytest, интерактивная демонстрация и Swagger/OpenAPI.
- Воспроизводимый запуск FastAPI и PostgreSQL через Docker Compose.

**Архитектурный акцент:** доменные правила не зависят от FastAPI и ORM; application-слой работает с абстракциями хранилища. Это мой наиболее показательный пример изоляции бизнес-логики в Python.

`Python 3.12` `FastAPI` `Pydantic` `SQLAlchemy 2` `PostgreSQL` `Alembic` `Pytest` `Docker` `Clean Architecture`

**[Исходный код и интерактивное демо →](https://github.com/AlphaZero-developer/FindMeShowcase)**

### [OrderFlow Backend](https://github.com/AlphaZero-developer/OrderFlowBackend)

**REST API для управления заказами с авторизацией, ролевыми ограничениями и контролем жизненного цикла.**

- JWT-аутентификация, Argon2 для хранения паролей, роли `client` и `manager`.
- Проверка прав доступа к конкретным ресурсам.
- Таблица допустимых переходов статусов заказа и защита бизнес-инвариантов.
- Redis cache-aside для списков заказов, инвалидация после изменения данных.
- Продолжение работы через PostgreSQL при сбое Redis.
- Собственные исключения и централизованная обработка HTTP-ошибок.
- Разделение routers, services, repositories; миграции и автоматизированные тесты.

`Python` `FastAPI` `PostgreSQL` `SQLAlchemy 2` `Redis` `JWT` `Argon2` `Alembic` `Pytest` `Docker Compose`

**[Исходный код →](https://github.com/AlphaZero-developer/OrderFlowBackend)**

### [Todo Backend](https://github.com/AlphaZero-developer/todo-backend)

Небольшой REST API с PostgreSQL, Redis-кэшированием, инвалидацией при изменениях и разделением на routes, services и repositories. Включает Docker Compose и скрипт быстрого запуска для Windows.

`FastAPI` `PostgreSQL` `Redis` `Docker Compose`

**[Исходный код →](https://github.com/AlphaZero-developer/todo-backend)**

---

## 🛠 Технологии

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

| Область | Стек и подходы |
|---|---|
| **Языки и API** | Python, Go, FastAPI, REST, HTTP, WebSocket, Pydantic |
| **Данные** | PostgreSQL, SQLAlchemy 2, Alembic, Redis, SQL, JSON |
| **Архитектура** | Layered Architecture, Clean Architecture для отдельных проектов, Repository Pattern, Dependency Injection, Unit of Work |
| **Безопасность** | JWT, Argon2, RBAC, проверки прав на ресурсы, серверная валидация Telegram init data |
| **Качество и эксплуатация** | Pytest, Go tests, Docker, Docker Compose, GitHub Actions, структурированные логи, Prometheus |
| **Интеграции** | Telegram Bot API, внешние AI API, HTTP-сервисы |
| **Изучаю глубже** | RabbitMQ, aio-pika, событийное взаимодействие, распределённые транзакции и отказоустойчивость |

## 🧠 Как подхожу к разработке

- **Начинаю с сценария и инвариантов.** Сначала определяю, какие состояния допустимы, кто может выполнять действие и что произойдёт при повторном запросе или сбое.
- **Разделяю ответственность.** Транспорт, бизнес-правила и доступ к данным не должны превращаться в один обработчик на сотни строк. При этом не добавляю абстракции только ради названия паттерна.
- **Думаю об отказах.** Проверяю границы доступа, повторные операции, сбои внешних зависимостей, корректную обработку ошибок и восстановление состояния.
- **Делаю код проверяемым.** Изолирую правила, пишу тесты, использую миграции, конфигурацию окружения и воспроизводимый запуск.
- **Могу работать с legacy.** Не считаю переписывание с нуля универсальным решением: сначала важно сохранить поведение и понять взаимосвязи системы.

Сейчас развиваюсь в **Python Backend**, асинхронном программировании (`asyncio`, `httpx`, async SQLAlchemy), брокерах сообщений и архитектуре распределённых приложений.

---

## 📫 Контакты

[![Telegram](https://img.shields.io/badge/Telegram-@antistress__67-26A5E4?style=flat&logo=telegram&logoColor=white)](https://t.me/antistress_67)
[![Email](https://img.shields.io/badge/Email-csgomail152%40gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:csgomail152@gmail.com)

**Открыт к предложениям по Python Backend Development, разработке API, интеграциям и backend-сервисам.**

[Все репозитории](https://github.com/AlphaZero-developer?tab=repositories)
