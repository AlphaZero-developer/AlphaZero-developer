<div align="center">

# Руслан · Backend Developer

**Python / FastAPI · Go · PostgreSQL · AI Integrations**

Разрабатываю серверную часть приложений: API, бизнес-логику, работу с данными,
аутентификацию, интеграции и сервисы с долгоживущим состоянием.

[**Проекты**](#-избранные-проекты) · [**Решённые задачи**](#-какие-задачи-решаю) · [**Связаться**](#-контакты)

</div>

## 🛠️ Технологии

**Языки и backend**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-1F2937?style=flat-square)
![WebSocket](https://img.shields.io/badge/WebSocket-374151?style=flat-square)
![HTTPX](https://img.shields.io/badge/HTTPX-2563EB?style=flat-square)

**Базы данных и хранение**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy_2-D71F00?style=flat-square)
![Alembic](https://img.shields.io/badge/Alembic-374151?style=flat-square)

**Инфраструктура, качество и интеграции**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram_Bot_API-26A5E4?style=flat-square&logo=telegram&logoColor=white)
![LLM API](https://img.shields.io/badge/LLM_API_Integration-5B21B6?style=flat-square)

**Подходы:** Layered Architecture, изоляция Domain/Application/Infrastructure, Repository Pattern, Dependency Injection, Unit of Work, идемпотентность и моделирование состояний. Применяю их там, где они оправданы задачей.

## 🎯 Какие задачи решаю

| Направление | Что делал в проектах |
|:--|:--|
| **API и backend** | Проектировал REST-эндпоинты, HTTP/WebSocket-взаимодействие, обработку ошибок, контракты запросов и ответов |
| **Бизнес-логика** | Машины состояний заказов и игр, правила модерации, антиспам, контекст команд, разрешение неоднозначностей |
| **Базы данных** | PostgreSQL / SQLite, модели и связи, SQLAlchemy, миграции Alembic, JSON-хранилища |
| **Авторизация и безопасность** | JWT, Argon2, RBAC, проверки доступа к ресурсам, привязка сессий к устройствам, проверка Telegram init data |
| **AI и автоматизация** | Интеграция LLM через HTTP API, контекстные ответы, AI-персонажи, маршрутизация намерений и валидация предложенных действий |
| **Надёжность** | Идемпотентные операции, защита от дубликатов событий, ограничение запросов, изоляция состояний, graceful shutdown |
| **Тестирование и запуск** | Pytest / Go tests, Docker Compose, GitHub Actions, структурированные логи, метрики, воспроизводимые демо |

**Практический опыт:** разрабатывал и запускал на VPS Telegram-бота **Mirohodec Warden** и голосового ассистента **LiS**. Публичные репозитории представляют очищенные, документированные версии этих работ; их состав и ограничения описаны отдельно.

---

## 🚀 Избранные проекты

### 01 · [Mirohodec Warden](https://github.com/AlphaZero-developer/mirohodec-warden) · Go / Telegram backend

**Самый масштабный проект моего портфолио:** многокомпонентный backend Telegram-сообществ, работавший на VPS и использовавшийся в реальных сценариях, включая коммерческое использование.

- **Модерация нескольких чатов:** отдельные политики, временные предупреждения, эскалация наказаний, защита администраторов.
- **Антиспам:** временные окна, повторяющиеся сообщения, ссылки, пересылки, страйки и cooldown.
- **AI-персонаж Лайя:** внешний LLM API, контекст, характер, фильтры ответов и ограничения поведения.
- **Mafia:** игровые комнаты, секретные роли, фазы, ночные действия, голосования, рейтинги ELO и достижения.
- **Инфраструктура:** PostgreSQL / JSON, миграции, HTTP API, WebSocket, веб-панель, Docker, структурированные логи и Prometheus.

**Инженерный фокус:** согласованность игровых состояний, правила модерации и взаимодействие нескольких подсистем в одном backend. Для публичного showcase выделены тестируемые доменные политики. Legacy-части и архитектурный долг задокументированы, а не скрыты.

`Go 1.23` `PostgreSQL` `Telegram Bot API` `WebSocket` `AI API` `Prometheus` `Docker`

[**Код и архитектура ↗**](https://github.com/AlphaZero-developer/mirohodec-warden) · [**Технический кейс ↗**](https://github.com/AlphaZero-developer/mirohodec-warden/blob/main/docs/CASE_STUDY.md)

---

### 02 · [LiS Assistant](https://github.com/AlphaZero-developer/lis-assistent) · Python / Voice & AI backend

**Голосовой ассистент с удалённым управлением и контекстным диспетчером команд.** Оригинальная Windows-версия включала офлайн-распознавание речи через **Vosk**, управление системой и медиа, Spotify Web API, backend для телефона и мониторинг задач Codex.

Публичный **backend showcase** выделяет ключевую серверную вертикаль:

- **Intent routing:** определение команды, контекст сессии и запрос уточнения вместо случайного действия.
- **Command lifecycle:** `repeat`, `undo`, история, ограниченное состояние и идемпотентность по `request_id`.
- **Remote API:** регистрация устройств, handshake, токены с ограниченным сроком, HTTP и WebSocket.
- **Security:** HMAC-отпечатки устройств, rate limiting, аудит без хранения личного текста команд.
- **Agent events:** состояния задач `started → running → completed / failed`, дедупликация событий.
- **Optional LLM fallback:** модель предлагает структурированное намерение, которое проверяется по allowlist. Произвольные команды ОС не исполняются.

> В showcase действия над устройствами **симулируются**. Vosk, Spotify и настоящий Windows-control принадлежат исходному ассистенту, а LLM fallback добавлен в публичную демонстрацию. Это не полная копия старого приложения.

<a href="https://github.com/AlphaZero-developer/lis-assistent">
  <img src="https://raw.githubusercontent.com/AlphaZero-developer/lis-assistent/main/docs/preview.png" alt="Интерактивная панель LiS Assistant" width="720" />
</a>

`Python 3.11+` `FastAPI` `Pydantic` `WebSocket` `SQLite` `HTTPX` `Pytest` `Docker` `LLM API`

[**Исходный код ↗**](https://github.com/AlphaZero-developer/lis-assistent) · [**Архитектура ↗**](https://github.com/AlphaZero-developer/lis-assistent/blob/main/docs/ARCHITECTURE.md) · [**Что взято из оригинала ↗**](https://github.com/AlphaZero-developer/lis-assistent/blob/main/docs/ORIGIN.md)

---

### 03 · [Find Me · Backend Showcase](https://github.com/AlphaZero-developer/FindMeShowcase) · Python / Clean Architecture

**Публичный запускаемый срез backend-логики сервиса знакомств Find Me.** Показывает проектирование доменных правил, независимых от веб-фреймворка и ORM.

- Двусторонняя фильтрация анкет и географическая приоритизация рекомендаций.
- Лайки, взаимные совпадения и раскрытие контактов только при согласии обеих сторон.
- Идемпотентная обработка повторных реакций и ограничения уникальности в БД.
- Разделение **API → Application → Domain → Infrastructure**.
- Repository Protocols, Unit of Work, SQLAlchemy 2, Alembic и автоматизированные тесты.
- Веб-демо и Swagger API, запуск через Docker Compose с PostgreSQL.

<a href="https://github.com/AlphaZero-developer/FindMeShowcase">
  <img src="https://raw.githubusercontent.com/AlphaZero-developer/FindMeShowcase/main/docs/showcase-desktop.png" alt="Find Me Backend Showcase" width="720" />
</a>

`Python 3.12` `FastAPI` `SQLAlchemy 2` `PostgreSQL` `Alembic` `Pytest` `Docker`

[**Код и запуск ↗**](https://github.com/AlphaZero-developer/FindMeShowcase) · [**Архитектурные решения ↗**](https://github.com/AlphaZero-developer/FindMeShowcase/blob/main/docs/ARCHITECTURE.md)

---

### 04 · [OrderFlow Backend](https://github.com/AlphaZero-developer/OrderFlowBackend) · Python / REST API

**API управления заказами с ролевой моделью и контролируемыми переходами статусов.**

- JWT-аутентификация, Argon2, роли `client` / `manager`, проверка прав на заказ.
- Бизнес-правила переходов `new → in_progress → ready → completed` и отмены.
- PostgreSQL, SQLAlchemy 2, миграции Alembic.
- Redis cache-aside и инвалидация кэша после изменений; fallback при недоступности Redis.
- Разделение routes / services / repositories, централизованные ошибки и тесты.

`Python` `FastAPI` `PostgreSQL` `Redis` `JWT` `Argon2` `Pytest` `Docker Compose`

[**Исходный код ↗**](https://github.com/AlphaZero-developer/OrderFlowBackend)

<details>
<summary><b>Ранний проект · Todo Backend</b></summary>

[Todo Backend](https://github.com/AlphaZero-developer/todo-backend) — REST API задач на FastAPI, PostgreSQL и Redis. CRUD, cache invalidation, слои routers/services/repositories, Docker Compose и запуск через `start.bat`.

</details>

---

## 🧩 Инженерный подход

- Начинаю с **предметной области и ограничений**, затем выбираю структуру приложения.
- Отделяю бизнес-правила от HTTP и работы с БД, когда это упрощает тестирование и развитие.
- Проектирую с учётом **повторных запросов, сбоев зависимостей и переходов состояния**.
- Предпочитаю воспроизводимые примеры, тесты и документацию заявлениям о «безупречной архитектуре».
- Продолжаю углубляться в `asyncio`, асинхронный SQLAlchemy, RabbitMQ / aio-pika и распределённые системы.

## 📫 Контакты

[![Telegram](https://img.shields.io/badge/Telegram-@antistress__67-26A5E4?style=flat-square&logo=telegram&logoColor=white)](https://t.me/antistress_67)
[![Email](https://img.shields.io/badge/Email-csgomail152%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:csgomail152@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Все_репозитории-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/AlphaZero-developer?tab=repositories)

**Открыт к предложениям по Python Backend Development**, API, AI-интеграциям и автоматизации бизнес-процессов.
