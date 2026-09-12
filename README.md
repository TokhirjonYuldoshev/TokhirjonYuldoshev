# Тохиржон Йулдошев

## Инженер по качеству (QA) | Автоматизация тестирования | CI/CD

**Основные технологии:** Playwright · TypeScript · API · SQL · GitHub Actions · Docker · Jenkins

Работаю с ручным и автоматизированным тестированием веб-приложений и API. Основное направление автоматизации — **Playwright + TypeScript**.

В портфолио делаю акцент на системном подходе к качеству: риск-ориентированной стратегии, обязательных проверках в CI, воспроизводимых запусках, диагностике причин сбоев, сохранении доказательств, нефункциональном тестировании и прозрачности состояния системы.

Санкт-Петербург · рассматриваю удалённый, гибридный и офисный формат работы

## Профессиональный подход

Для меня качество — это управляемая инженерная система, а не количество тестов. Каждый уровень проверки должен отвечать на конкретный вопрос, а результат CI должен позволять быстро понять, что именно сломалось, где находится причина и какое действие требуется дальше.

В проектах придерживаюсь следующих принципов:

- строить набор проверок от рисков продукта и инфраструктуры;
- не скрывать нестабильность повторными попытками;
- разделять функциональные, инфраструктурные и проверки безопасности;
- сохранять отчёты, журналы и диагностические материалы для разбора сбоев;
- отделять уведомления и внешние интеграции от фактического результата тестов;
- фиксировать правила слияния, критерии успешности и порядок разбора инцидентов в документации.

## Ключевые компетенции

| Направление | Практика |
| --- | --- |
| Автоматизация тестирования | Playwright + TypeScript, модульные, API и сквозные проверки, Page Object Model, фикстуры, вспомогательные функции, подготовка тестовых данных |
| Межбраузерное тестирование | Chromium, Firefox, WebKit; управляемые запуски в GitHub Actions |
| CI/CD и контроль качества | обязательные проверки перед слиянием, защищённая ветка `main`, правила слияния, GitHub Actions, Jenkins |
| Отчётность и диагностика | Allure, Playwright HTML, JUnit XML, трассировки, снимки экрана, видео, артефакты ошибок, GitHub Actions Summary |
| Нефункциональное тестирование | доступность интерфейса с axe-core, Lighthouse, визуальная регрессия, проверки стабильности |
| Безопасность | npm audit, Trivy, CycloneDX SBOM, Dependabot, проверка достижимости уязвимого кода |
| Инфраструктура | Docker, PostgreSQL, проверка реального запуска контейнера, контроль запуска без root, синтетические проверки состояния |
| Управление качеством | риск-ориентированная стратегия, критерии входа и выхода, правила разбора сбоев, регламенты инцидентов |
| Наблюдаемость | структурированные уведомления в Telegram для запросов на слияние, изменений в `main`, ручных и плановых запусков |

## Текущий статус CI

[![PomidorQA CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml)
[![Database Health](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml)
[![Python & Docker CI](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml)

---

## Ключевые проекты

### 1. [PomidorQA QA Automation](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)

Основной проект по автоматизации тестирования на **Playwright + TypeScript**. В нём собрана многоуровневая система контроля качества: от модульных и API-проверок до межбраузерных сквозных тестов, проверок безопасности и нефункционального тестирования.

- модульные, API и сквозные уровни тестирования;
- Chromium, Firefox и WebKit в автоматической матрице браузеров;
- Page Object Model, фикстуры, вспомогательные функции и управляемые тестовые данные;
- GitHub Actions с `workers=1` и `retries=0` для сквозных проверок живого окружения;
- локальная последовательность обязательных проверок: Node.js 24 → статический анализ → проверка типов → модульные тесты → API-тесты;
- Allure, Playwright HTML, трассировки, снимки экрана, видео и диагностические материалы при сбоях;
- ночной регрессионный запуск и отдельная проверка стабильности без повторных попыток;
- проверки доступности интерфейса, производительности через Lighthouse и визуальной регрессии;
- npm audit, CycloneDX SBOM и контролируемые обновления Dependabot;
- отдельные уведомления в Telegram для основного CI, ночной регрессии, безопасности, стабильности, доступности, Lighthouse и визуальной регрессии;
- защищённая ветка `main` с обязательными проверками перед слиянием;
- [риск-ориентированная стратегия тестирования](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/test-strategy.md) и [регламент разбора сбоев CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/ci-incident-runbook.md);
- ручная проверка Registration Contract Smoke для реального HTTP-контракта регистрации.

**Технологии:** Playwright · TypeScript · Node.js 24 · GitHub Actions · Allure · axe-core · Lighthouse · CycloneDX · Telegram Bot API

### 2. [Гибридный QA-мониторинг PostgreSQL](https://github.com/TokhirjonYuldoshev/qa-docker-monitor)

Проект по контролю состояния PostgreSQL, где итог определяется не простым `ping`, а **реальной записью данных с последующим точным чтением и проверкой результата**.

- PostgreSQL 16 в контейнере GitHub Actions и плановая синтетическая проверка записи и чтения;
- уникальный маркер каждого запуска и точная проверка `CREATE / INSERT / SELECT`;
- контрактные проверки для Windows/Jenkins с изолированными заменителями внешних команд;
- обязательная проверка `CI / Required gate`, объединяющая критичные сигналы;
- отдельная проверка `PostgreSQL Image Security`: Trivy для критических уязвимостей, `govulncheck` для проверки достижимости уязвимого кода и CycloneDX SBOM;
- структурированный итог каждого запуска в GitHub Actions Summary;
- уведомления в Telegram для проверки базы данных и безопасности PostgreSQL на запросах на слияние, изменениях в `main`, ручных и плановых запусках;
- сбой Telegram не влияет на фактический результат проверки базы данных или политики безопасности;
- [описание границ мониторинга](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/blob/main/docs/monitoring-boundary.md) и [регламент разбора инцидентов](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/blob/main/docs/incident-runbook.md);
- Dependabot, анализ рисков изменений и политика безопасности.

**Технологии:** PostgreSQL · Docker · GitHub Actions · Jenkins · Windows · Trivy · CycloneDX · govulncheck · Telegram Bot API

### 3. [Jenkins + Docker: CI/CD-пайплайн для QA](https://github.com/TokhirjonYuldoshev/my-docker-project)

Инфраструктурный проект, который показывает построение независимых проверок качества в CI/CD без искусственного увеличения количества тестов.

- проверка зависимостей через `pip check`, статический анализ Flake8 и Pytest с JUnit-отчётом;
- сборка Docker-образа и проверка реального запуска контейнера;
- отдельный контроль запуска от непривилегированного пользователя;
- Trivy блокирует исправляемые уязвимости уровня `CRITICAL`, CycloneDX сохраняет SBOM;
- независимые проверки объединены в обязательный `CI / Required gate`;
- Python 3.12 и закреплённые версии зависимостей разработки;
- еженедельная полная проверка для выявления изменений в инфраструктуре и безопасности;
- Jenkins Declarative Pipeline: зависимости → статический анализ → тесты → сборка → контроль пользователя → проверка запуска контейнера;
- публикация Docker Hub разрешена только из `main`;
- [регламент разбора сбоев CI/CD](https://github.com/TokhirjonYuldoshev/my-docker-project/blob/main/docs/pipeline-incident-runbook.md) и [границы и ограничения проекта](https://github.com/TokhirjonYuldoshev/my-docker-project/blob/main/docs/scope-and-nongoals.md);
- уведомления в Telegram для запросов на слияние, изменений в `main`, ручных и еженедельных запусков;
- транспорт уведомлений не изменяет результат сборки, тестов или проверок безопасности.

**Технологии:** Python 3.12 · Pytest · Flake8 · Docker · Trivy · CycloneDX · Jenkins · GitHub Actions · Docker Hub · Telegram Bot API

---

<details>
<summary><b>Ручное тестирование, API, SQL и мобильные приложения</b></summary>

### Веб-тестирование — DemoShopping

- 5 чек-листов и **45+ тест-кейсов** для корзины, оформления заказа и оплаты;
- **28 баг-репортов**, включая блокирующие дефекты;
- локализация проблем через DevTools Network и Console;
- API-тестирование и SQL-проверка данных.

[Открыть документацию по веб-тестированию](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=0#gid=0)

### API-тестирование — Postman

- [PetStore Collection](./PetStore.postman_collection.json) — `User`, `Pet`, `Store`, CRUD;
- [DemoShopping Collection](./DemoShopping.postman_collection.json) — `Products`, `Cart`, `Orders`, `Payment`;
- сквозные API-сценарии и автоматические проверки в Postman Runner.

### SQL и NoSQL

SQL: JOIN, подзапросы, агрегатные функции. Практика с PostgreSQL, MySQL и MongoDB.

[Примеры SQL / NoSQL](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=1293622627#gid=1293622627)

### Мобильное тестирование

- Android: установка, прерывания, смена темы и пользовательские сценарии;
- **30 тест-кейсов** на основной пользовательский сценарий;
- баг-репорты по критичным падениям приложения с логами и шагами воспроизведения.

[Открыть документацию по мобильному тестированию](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=292251871#gid=292251871)

</details>

---

## Технологии и инструменты

`Playwright` `TypeScript` `Postman` `REST API` `SQL` `PostgreSQL` `MySQL` `MongoDB` `Git` `GitHub Actions` `Docker` `Trivy` `CycloneDX` `Jenkins` `Python` `Pytest` `Allure` `DevTools` `Jira` `YouTrack` `Qase` `TestRail` `Charles Proxy`

---

<details>
<summary><b>Обучение и образование</b></summary>

### Тестирование и автоматизация

1. **[Тестирование ПО с нуля. Теория + практика. Продвинутый курс с ИИ](https://stepik.org/course/245575/promo)** 
2. **SQL практикум. SELECT-запросы** — Pragmatic Programmer, Stepik
3. **QA за 60 дней** — ручное и API-тестирование
4. **AQA за 60 дней** — Playwright + TypeScript

### Образование

- **Санкт-Петербургский государственный технологический институт (СПбГТИ)** — Бизнес-информатика, 2024–н.в.
- **Южно-Казахстанская государственная медицинская академия (ЮКГМА)** — Фармация, провизор, 2006.

Фармацевтический бэкграунд помогает быстро погружаться в предметную область, в том числе в проекты MedTech.

</details>

---

## Контакты

- **Email:** [toxir.yuldoshev1983@gmail.com](mailto:toxir.yuldoshev1983@gmail.com)
- **Telegram:** [@TokhirjonYuldoshev](https://t.me/TokhirjonYuldoshev)
- **LinkedIn:** [tokhirjon-yuldoshev](https://www.linkedin.com/in/tokhirjon-yuldoshev/)
