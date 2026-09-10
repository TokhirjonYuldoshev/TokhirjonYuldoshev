# Тохиржон Йулдошев

## QA Engineer | QA Automation

**Playwright · TypeScript · API · SQL · GitHub Actions · Docker · Jenkins**

QA Engineer focused on **test automation, API testing and CI quality engineering**.

Санкт-Петербург · рассматриваю удалённый / гибридный / офисный формат

Работаю с ручным и автоматизированным тестированием Web/API. Основное направление автоматизации — **Playwright + TypeScript**. Строю воспроизводимые CI-пайплайны, работаю с SQL, Docker, Jenkins и автоматизированной отчётностью.

## Portfolio highlights

| Область | Что реализовано |
| --- | --- |
| Test Automation | Playwright + TypeScript, Unit / API / E2E, POM, fixtures, helpers, test-data factories |
| Cross-browser CI | Chromium / Firefox / WebKit, GitHub Actions, `retries=0` |
| Reporting & Diagnostics | Allure, Playwright HTML, trace, screenshots, video, failure artifacts |
| Non-functional QA | Accessibility (axe-core), Lighthouse, Visual Regression, security и stability checks |
| Quality governance | protected `main`, strict required checks, risk-based merge policy и failure classification |
| Infrastructure | Docker, Jenkins, PostgreSQL, container runtime smoke, Trivy, Telegram Bot API |

### Live CI status

[![PomidorQA CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml)
[![Database Health](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml)
[![Python & Docker CI](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml)

---

## Ключевые проекты

### 1. [PomidorQA QA Automation](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)

Основной standalone-проект по **QA Automation на Playwright + TypeScript**.

- Unit / API / E2E уровни;
- Chromium / Firefox / WebKit;
- Page Object Model, fixtures и уникальные test data;
- GitHub Actions CI с `retries=0`;
- Allure + Playwright HTML;
- Nightly Regression и Stability workflow;
- Accessibility Audit, Lighthouse и Visual Regression;
- security gates и Telegram notifications;
- protected `main` со strict required checks и risk-based QA quality-gate policy;
- manual-only Registration Contract Smoke для реального HTTP-контракта регистрации.

### 2. [Hybrid QA Monitoring System](https://github.com/TokhirjonYuldoshev/qa-docker-monitor)

QA monitoring для проверки **доступности и возможности записи в PostgreSQL**:

- PostgreSQL service container и scheduled SQL write-health checks в GitHub Actions;
- реальный `CREATE/INSERT` вместо поверхностной проверки порта;
- GitHub Actions summary и явные failure semantics;
- health signal отделён от Telegram notification transport;
- Docker + Windows/Jenkins-compatible monitoring.

**Стек:** PostgreSQL · Docker · GitHub Actions · Jenkins · Telegram Bot API

### 3. [Jenkins + Docker CI Pipeline](https://github.com/TokhirjonYuldoshev/my-docker-project)

Компактный CI/Docker pet-project с независимыми quality gates:

- GitHub Actions: Flake8, Pytest, Docker build и **container runtime smoke**;
- Trivy container security gate блокирует fixable CRITICAL vulnerabilities;
- независимые checks агрегируются в стабильный **`CI / Required gate`**;
- Python 3.12 baseline, non-root runtime, pinned development dependencies и контролируемые Dependabot updates;
- Jenkins Declarative Pipeline: lint → tests → build → runtime smoke → Docker Hub push;
- Jenkins Credentials, гарантированная cleanup-попытка и Telegram build notifications;
- notification transport не подменяет реальный build/test signal.

**Стек:** Python 3.12 · Pytest · Flake8 · Docker · Trivy · Jenkins · GitHub Actions · Docker Hub

---

<details>
<summary><b>Manual QA / API / SQL / Mobile portfolio</b></summary>

### Web testing — DemoShopping

- 5 чек-листов и **45+ тест-кейсов** на корзину, checkout и оплату;
- **28 баг-репортов**, включая blocker-дефекты;
- локализация проблем через DevTools Network / Console;
- API testing и SQL-верификация данных.

[Открыть Web-документацию](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=0#gid=0)

### API testing — Postman

- [PetStore Collection](./PetStore.postman_collection.json) — `User`, `Pet`, `Store`, CRUD;
- [DemoShopping Collection](./DemoShopping.postman_collection.json) — `Products`, `Cart`, `Orders`, `Payment`;
- E2E API scenarios и автопроверки в Postman Runner.

### SQL & NoSQL

SQL: JOIN, подзапросы, агрегаты. Практика с PostgreSQL, MySQL и MongoDB.

[Примеры SQL / NoSQL](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=1293622627#gid=1293622627)

### Mobile testing

- Android: установка, прерывания, смена темы и пользовательские сценарии;
- **30 тест-кейсов** на основной flow;
- bug reports на критические crash-сценарии с логами и шагами воспроизведения.

[Открыть Mobile-документацию](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=292251871#gid=292251871)

</details>

---

## Стек

`Playwright` `TypeScript` `Postman` `REST API` `SQL` `PostgreSQL` `MySQL` `MongoDB` `Git` `GitHub Actions` `Docker` `Trivy` `Jenkins` `Python` `Pytest` `Allure` `DevTools` `Jira` `YouTrack` `Qase` `TestRail` `Charles Proxy`

---

<details>
<summary><b>Обучение и образование</b></summary>

### QA / AQA

1. **[Тестирование ПО с нуля. Теория + практика. Продвинутый курс с ИИ](https://stepik.org/course/245575/promo)** — Артём Русов, Stepik
2. **SQL практикум. SELECT-запросы** — Pragmatic Programmer, Stepik
3. **QA за 60 дней** — ручное и API-тестирование
4. **AQA за 60 дней** — Playwright + TypeScript

### Образование

- **Санкт-Петербургский государственный технологический институт (СПбГТИ)** — Бизнес-информатика, 2024–н.в.
- **Южно-Казахстанская государственная медицинская академия (ЮКГМА)** — Фармация, провизор, 2006.

Профильный фармацевтический бэкграунд помогает быстро погружаться в предметную область, в том числе MedTech.

</details>

---

## Контакты

- **Email:** [toxir.yuldoshev1983@gmail.com](mailto:toxir.yuldoshev1983@gmail.com)
- **Telegram:** [@TokhirjonYuldoshev](https://t.me/TokhirjonYuldoshev)
- **LinkedIn:** [tokhirjon-yuldoshev](https://www.linkedin.com/in/tokhirjon-yuldoshev/)

![Visitor Badge](https://visitor-badge.laobi.icu/badge?page_id=TokhirjonYuldoshev)
