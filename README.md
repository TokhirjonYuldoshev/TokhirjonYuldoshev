# Привет, меня зовут Тохиржон 👋

## QA Engineer | QA Automation

**Playwright · TypeScript · API · SQL · GitHub Actions · Docker · Jenkins**

Занимаюсь ручным и автоматизированным тестированием Web/API. Пишу автотесты на **Playwright + TypeScript**, работаю с REST API, SQL и DevTools, строю CI-пайплайны в GitHub Actions и Jenkins, использую Docker и автоматизированную отчётность.

В портфолио — проекты с **Unit / API / E2E**, cross-browser testing, Allure, accessibility, Lighthouse, visual regression, security и stability-проверками.

Сейчас развиваюсь в направлении **QA Automation** и рассматриваю позиции **QA Engineer / QA Automation Engineer**.

---

## 🧰 Основной стек

| Направление | Инструменты и технологии |
| --- | --- |
| Automation | Playwright, TypeScript, POM, fixtures, helpers, test-data factories |
| Web | DevTools, HTML/CSS, Figma, Perfect Pixel |
| API | REST, SOAP, Postman, Swagger, JSON, HTTP |
| Test Management | Jira, YouTrack, Qase, TestRail, Confluence |
| Databases | SQL, PostgreSQL, MySQL, MongoDB |
| CI/CD & Infrastructure | GitHub Actions, Jenkins, Docker, Bash, Git |
| Reporting | Allure Report, Playwright HTML Report, trace, screenshots, video |
| Mobile | Android Studio, Xcode, Charles Proxy, Fiddler, Proxyman |
| Quality | ESLint, TypeScript typecheck, npm audit, accessibility, Lighthouse, visual regression |

---

## 🚀 Ключевые проекты

### 1. [PomidorQA QA Automation](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)

Мой основной standalone-проект по **QA Automation на Playwright + TypeScript**.

- Unit / API / E2E уровни тестирования;
- cross-browser E2E: **Chromium / Firefox / WebKit**;
- Page Object Model, fixtures, helpers и уникальные test data;
- CI на **GitHub Actions** с `retries=0`;
- **Allure Report + Playwright HTML Report**;
- trace, screenshots, video и failure artifacts;
- **Nightly Regression** и отдельный Stability workflow для поиска flaky-тестов;
- **Accessibility Audit** через axe-core;
- **Performance Smoke** через Lighthouse;
- **Visual Regression**;
- Security gates с `npm audit`, ESLint и TypeScript typecheck;
- Telegram-уведомления о результатах CI;
- manual-only **Registration Contract Smoke** для проверки реального HTTP-контракта регистрации.

### 2. [Hybrid QA Monitoring System](https://github.com/TokhirjonYuldoshev/qa-docker-monitor)

Мониторинг здоровья PostgreSQL в двух средах:

- **GitHub Actions** — cloud checks;
- **Jenkins** — локальный pipeline;
- PostgreSQL в Docker;
- автоматические SQL health checks;
- Telegram alerts при успехе и ошибках.

**Стек:** Docker · PostgreSQL · Jenkins · GitHub Actions · Telegram Bot API

### 3. [DevOps CI/CD Automation Project](https://github.com/TokhirjonYuldoshev/my-docker-project)

Production-style учебный CI/CD pipeline:

- Python + Pytest;
- Flake8 static analysis;
- Jenkins Declarative Pipeline;
- Docker image build;
- публикация image в Docker Hub;
- Telegram build notifications.

**Стек:** Python · Pytest · Flake8 · Docker · Jenkins · Docker Hub

---

## 🧪 Manual QA / API / SQL портфолио

### Web testing — DemoShopping

- 5 чек-листов и **45+ тест-кейсов** на корзину, checkout и оплату;
- **28 баг-репортов**, включая blocker-дефекты;
- локализация проблем через DevTools Network / Console;
- тестирование API и верификация данных через SQL.

[🔗 Открыть Web-документацию](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=0#gid=0)

### API testing — Postman

- [PetStore Collection](./PetStore.postman_collection.json) — `User`, `Pet`, `Store`, CRUD;
- [DemoShopping Collection](./DemoShopping.postman_collection.json) — `Products`, `Cart`, `Orders`, `Payment`;
- E2E API scenarios и автопроверки в Postman Runner.

### SQL & NoSQL

- JOIN, подзапросы, агрегаты;
- MySQL / PostgreSQL / MongoDB;
- проверка данных приложения через запросы к БД.

[🔗 Примеры SQL / NoSQL](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=1293622627#gid=1293622627)

### Mobile testing

- Android: установка, прерывания, смена темы и основные пользовательские сценарии;
- **30 тест-кейсов** на основной пользовательский flow;
- баг-репорты на критические crash-сценарии с логами и шагами воспроизведения.

[🔗 Открыть Mobile-документацию](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=292251871#gid=292251871)

---

## 🎓 Обучение

Мой путь обучения строился от ручного тестирования и SQL к полноценной автоматизации:

1. **[Тестирование ПО с нуля. Теория + практика. Продвинутый курс с ИИ](https://stepik.org/course/245575/promo)** — Артём Русов, Stepik  
   Анализ требований, тест-дизайн, тест-план и тестовая стратегия, тест-документация, Web/Mobile, API, MySQL/MongoDB, Git/GitHub/Bash и основы CI/CD.
2. **SQL практикум. SELECT-запросы** — практика SQL и работы с данными.
3. **QA за 60 дней** — ручное и API-тестирование.
4. **AQA за 60 дней** — Playwright + TypeScript.

Дополнительно постоянно развиваю практические навыки через собственные QA/AQA pet-проекты и CI-инфраструктуру.

---

## 📚 Образование

- **Санкт-Петербургский государственный технологический институт (СПбГТИ)** — Бизнес-информатика, 2024–н.в.
- **Южно-Казахстанская государственная медицинская академия (ЮКГМА)** — Фармация, провизор, 2006.

Профильный бэкграунд в фармацевтике помогает быстрее погружаться в предметную область, в том числе при работе с MedTech-продуктами.

---

## 📫 Контакты

- **Email:** [toxir.yuldoshev1983@gmail.com](mailto:toxir.yuldoshev1983@gmail.com)
- **Telegram:** [@TokhirjonYuldoshev](https://t.me/TokhirjonYuldoshev)
- **LinkedIn:** [tokhirjon-yuldoshev](https://www.linkedin.com/in/tokhirjon-yuldoshev/)

---

![Visitor Badge](https://visitor-badge.laobi.icu/badge?page_id=TokhirjonYuldoshev)
