# Тохиржон Йулдошев

## QA Engineer | Автоматизация тестирования | Инженерия качества

**Основной стек:** Playwright · TypeScript · API · SQL · GitHub Actions · Docker · Jenkins

Работаю с ручным и автоматизированным тестированием веб-приложений и API. Основное направление автоматизации — **Playwright + TypeScript**.

В портфолио делаю акцент не только на написании тестов, а на построении управляемой системы качества: риск-ориентированной стратегии, обязательных проверках в CI, воспроизводимых запусках, диагностике сбоев, сохранении доказательств, нефункциональном тестировании и наблюдаемости.

Санкт-Петербург · рассматриваю удалённый, гибридный и офисный формат работы

## Профессиональный профиль

Подхожу к тестированию как к инженерной дисциплине. Для меня качество — это не количество тестов, а понятная система сигналов, в которой каждый уровень проверки имеет назначение, владелец результата понимает причину сбоя, а CI не маскирует реальные дефекты повторными запусками.

В проектах разделяю функциональные, инфраструктурные и security-проверки, использую обязательные проверки перед слиянием, сохраняю отчёты и диагностические материалы, документирую критерии входа и выхода, правила разбора инцидентов и границы ответственности.

## Ключевые компетенции

| Направление | Практика |
| --- | --- |
| Автоматизация тестирования | Playwright + TypeScript, модульные, API и сквозные проверки, Page Object Model, fixtures, helpers, подготовка тестовых данных |
| Межбраузерное тестирование | Chromium, Firefox, WebKit; управляемые запуски в GitHub Actions |
| CI/CD и контроль качества | обязательные проверки, защищённая ветка `main`, правила слияния, GitHub Actions, Jenkins |
| Отчётность и диагностика | Allure, Playwright HTML, JUnit XML, trace, screenshots, video, артефакты ошибок, GitHub Actions Summary |
| Нефункциональное тестирование | Accessibility с axe-core, Lighthouse, Visual Regression, stability-проверки |
| Безопасность зависимостей и образов | npm audit, Trivy, CycloneDX SBOM, Dependabot, проверка достижимости уязвимого кода |
| Инфраструктурное тестирование | Docker, PostgreSQL, проверка запуска контейнера, non-root policy, synthetic health checks |
| Управление качеством | риск-ориентированная стратегия, критерии входа и выхода, правила разбора сбоев, incident runbooks |
| Наблюдаемость | структурированные уведомления Telegram для PR, push, ручных и плановых запусков без подмены результата тестов |

## Статус CI

[![PomidorQA CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml)
[![Database Health](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml)
[![Python & Docker CI](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml)

---

## Ключевые проекты

### 1. [PomidorQA QA Automation](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)

Основной проект по автоматизации тестирования на **Playwright + TypeScript**. Здесь собрана наиболее полная модель контроля качества: от модульных и API-проверок до межбраузерных сквозных тестов, нефункциональных проверок и CI-политик.

- модульные, API и сквозные уровни тестирования;
- Chromium, Firefox и WebKit в автоматической матрице браузеров;
- Page Object Model, fixtures, helpers и управляемые тестовые данные;
- GitHub Actions с `workers=1` и `retries=0` для сквозных проверок живого окружения;
- локальная последовательность обязательных проверок: Node.js 24 → lint → typecheck → Unit → API;
- Allure, Playwright HTML, trace, screenshots, video и диагностические артефакты при сбоях;
- Nightly Regression и отдельный Stability workflow без повторных попыток;
- Accessibility Audit, Lighthouse и Visual Regression;
- npm audit, CycloneDX SBOM и контролируемые обновления Dependabot;
- отдельные Telegram-уведомления для основного CI, Nightly, Security, Stability, Accessibility, Lighthouse и Visual Regression;
- защищённая ветка `main` с обязательными проверками перед слиянием;
- [риск-ориентированная стратегия тестирования](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/test-strategy.md) и [регламент разбора сбоев CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/ci-incident-runbook.md);
- ручной Registration Contract Smoke для проверки реального HTTP-контракта регистрации.

**Технологии:** Playwright · TypeScript · Node.js 24 · GitHub Actions · Allure · axe-core · Lighthouse · CycloneDX · Telegram Bot API

### 2. [Гибридный QA-мониторинг PostgreSQL](https://github.com/TokhirjonYuldoshev/qa-docker-monitor)

Проект по контролю состояния PostgreSQL, где результат определяется не простым `ping`, а **реальной записью данных с последующим точным чтением и проверкой результата**.

- PostgreSQL 16 в service container и плановый синтетический write/read health check;
- уникальные маркеры каждого запуска и точная проверка `CREATE / INSERT / SELECT`;
- Windows/Jenkins contract tests с изолированными заменителями команд;
- обязательная проверка `CI / Required gate`, объединяющая критичные сигналы;
- отдельный `PostgreSQL Image Security`: Trivy CRITICAL scan, проверка `gosu` через `govulncheck` и CycloneDX SBOM;
- структурированный итог каждого запуска в GitHub Actions Summary;
- Telegram-уведомления для database health и PostgreSQL Image Security на PR, push, ручных и плановых запусках;
- сбой Telegram не влияет на реальный результат проверки базы данных или security-политики;
- [описание границ мониторинга](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/blob/main/docs/monitoring-boundary.md) и [регламент разбора инцидентов](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/blob/main/docs/incident-runbook.md);
- Dependabot, анализ рисков PR и security policy.

**Технологии:** PostgreSQL · Docker · GitHub Actions · Jenkins · Windows · Trivy · CycloneDX · govulncheck · Telegram Bot API

### 3. [Jenkins + Docker: CI/CD-пайплайн для QA](https://github.com/TokhirjonYuldoshev/my-docker-project)

Компактный инфраструктурный проект, который показывает построение независимых проверок качества в CI/CD без искусственного увеличения количества тестов.

- проверка зависимостей через `pip check`, Flake8 и Pytest с JUnit-отчётом;
- сборка Docker-образа и проверка реального запуска контейнера;
- отдельная проверка запуска от непривилегированного пользователя;
- Trivy блокирует исправляемые уязвимости уровня `CRITICAL`, CycloneDX сохраняет SBOM;
- независимые проверки объединены в обязательный `CI / Required gate`;
- Python 3.12 и закреплённые версии зависимостей разработки;
- еженедельная полная проверка для выявления инфраструктурного и security-дрейфа;
- Jenkins Declarative Pipeline: зависимости → lint → тесты → сборка → non-root policy → runtime smoke;
- публикация Docker Hub разрешена только из `main`;
- [регламент разбора сбоев CI/CD](https://github.com/TokhirjonYuldoshev/my-docker-project/blob/main/docs/pipeline-incident-runbook.md) и [границы проекта](https://github.com/TokhirjonYuldoshev/my-docker-project/blob/main/docs/scope-and-nongoals.md);
- Telegram-уведомления для Pull Request, push в `main`, ручных и еженедельных запусков;
- транспорт уведомлений не изменяет результат сборки, тестов или security-проверок.

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

1. **[Тестирование ПО с нуля. Теория + практика. Продвинутый курс с ИИ](https://stepik.org/course/245575/promo)** — Артём Русов, Stepik
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
