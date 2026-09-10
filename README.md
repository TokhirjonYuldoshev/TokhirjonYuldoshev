# Тохиржон Йулдошев

## QA Engineer | QA Automation

**Playwright · TypeScript · API · SQL · GitHub Actions · Docker · Jenkins**

QA Engineer с фокусом на **автоматизации тестирования, API, CI/CD quality gates и диагностируемой тестовой инфраструктуре**.

Санкт-Петербург · рассматриваю удалённый / гибридный / офисный формат

Работаю с ручным и автоматизированным тестированием Web/API. Основное направление автоматизации — **Playwright + TypeScript**. В portfolio-проектах строю воспроизводимые CI-пайплайны, разделяю независимые quality signals, сохраняю failure diagnostics и не маскирую реальные ошибки retries или вспомогательными интеграциями.

## Portfolio highlights

| Область | Что реализовано |
| --- | --- |
| Test Automation | Playwright + TypeScript, Unit / API / E2E, POM, fixtures, helpers, test-data factories |
| Cross-browser CI | Chromium / Firefox / WebKit, GitHub Actions, `workers=1`, `retries=0` для live E2E |
| Reporting & Diagnostics | Allure, Playwright HTML, trace, screenshots, video, failure artifacts, Actions Summary |
| Non-functional QA | Accessibility (axe-core), Lighthouse, Visual Regression, security и stability checks |
| Quality governance | protected `main`, strict required checks, risk-based merge policy, dependency maintenance |
| Infrastructure | Docker, Jenkins, PostgreSQL, container runtime smoke, Trivy, Telegram observability |

### Live CI status

[![PomidorQA CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml)
[![Database Health](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml)
[![Python & Docker CI](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml)

---

## Ключевые проекты

### 1. [PomidorQA QA Automation](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)

Основной standalone-проект по **QA Automation на Playwright + TypeScript**.

- Unit / API / E2E уровни тестирования;
- Chromium / Firefox / WebKit в автоматическом browser matrix;
- Page Object Model, fixtures, helpers и уникальные test data;
- GitHub Actions CI с `workers=1` и `retries=0` для live E2E;
- Allure + Playwright HTML, trace/screenshots/video и failure artifacts;
- Nightly Regression и Stability workflow;
- Accessibility Audit, Lighthouse и Visual Regression;
- security gates, controlled Dependabot maintenance и Telegram notifications;
- protected `main` со strict required checks и risk-based QA quality-gate policy;
- manual-only Registration Contract Smoke для реального HTTP-контракта регистрации.

**Стек:** Playwright · TypeScript · Node.js · GitHub Actions · Allure · axe-core · Lighthouse · Telegram Bot API

### 2. [Гибридный QA-мониторинг PostgreSQL](https://github.com/TokhirjonYuldoshev/qa-docker-monitor)

Проект мониторинга, где health signal основан не на `ping`, а на **реальной возможности записи в PostgreSQL**.

- PostgreSQL 16 service container и scheduled SQL write-health checks;
- реальный `CREATE/INSERT` как source of truth;
- Windows/Jenkins contract tests с изолированными command doubles;
- `CI / Required gate` агрегирует обязательные monitoring signals;
- структурированный GitHub Actions Summary;
- Telegram observability отделена от DB health и не может скрыть реальный failure;
- отдельный manual Telegram diagnostic workflow (`getMe` → `getChat` → `sendMessage`);
- Dependabot, PR risk review и security policy.

**Стек:** PostgreSQL · Docker · GitHub Actions · Jenkins · Windows · Telegram Bot API

### 3. [Jenkins + Docker: CI/CD-пайплайн для QA](https://github.com/TokhirjonYuldoshev/my-docker-project)

Компактный проект, сфокусированный на **pipeline design и независимых quality gates**, а не на искусственном количестве тестов.

- GitHub Actions: Flake8, Pytest, Docker build + **container runtime smoke**;
- Trivy container-security gate блокирует fixable `CRITICAL` vulnerabilities;
- независимые checks агрегируются в стабильный `CI / Required gate`;
- Python 3.12 baseline, non-root Docker runtime и pinned development dependencies;
- controlled Dependabot updates для Python, GitHub Actions и Docker base image;
- Jenkins Declarative Pipeline: lint → tests → build → runtime smoke → Docker Hub push;
- Telegram CI observability с русским структурированным итогом и прямой ссылкой на run;
- manual-only Telegram diagnostics;
- notification transport не подменяет реальный build/test/security signal.

**Стек:** Python 3.12 · Pytest · Flake8 · Docker · Trivy · Jenkins · GitHub Actions · Docker Hub · Telegram Bot API

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
