# Тохиржон Йулдошев

## QA Automation Engineer · Playwright / TypeScript · API · CI/CD · Docker

Автоматизирую проверку веб-приложений и API и строю CI-процессы, в которых результат можно **доказать, воспроизвести и быстро диагностировать**.

Основной стек: **Playwright + TypeScript**, REST API, SQL, GitHub Actions, Docker и Jenkins. В проектах связываю требования с конкретными проверками, разделяю функциональные и инфраструктурные сигналы и не использую retries как способ скрыть нестабильность.

**Санкт-Петербург · удалённый / гибридный / офисный формат**

[![PomidorQA CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml)
[![PomidorQA Security](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/security.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/security.yml)
[![Database Health](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml)
[![Python & Docker CI](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml)

---

## Инженерный фокус

- **Requirements → evidence:** требование связывается с конкретным test case, а не только с именем spec-файла.
- **Надёжный тестовый сигнал:** `retries=0`, управляемые данные, отдельные BrowserContext, причинные ожидания вместо произвольных sleep.
- **CI как система контроля качества:** обязательные gates, branch protection, агрегирующие проверки, отчёты и диагностические artifacts.
- **Разделение ответственности:** продуктовые ошибки, инфраструктурные сбои, security findings и проблемы доставки уведомлений не смешиваются в один сигнал.
- **Нефункциональные проверки:** accessibility, Lighthouse, visual regression, container/security scanning и SBOM.
- **Incident-ready диагностика:** trace, screenshots, video, JUnit/JSON, Allure, GitHub Actions Summary и runbooks.

## Ключевые результаты

| Область | Подтверждённый результат |
| --- | --- |
| Requirement coverage | **50 / 50** требований имеют статус; **45 / 50 automated (90%)** |
| Traceability | requirement → **точный spec-файл → конкретный `test(...)` / `test.fail(...)`** |
| Автоматизированные проверки | **121**: 10 Unit + 11 API + 100 E2E |
| Cross-browser | 100 E2E в **Chromium + Firefox + WebKit**, `retries=0` |
| GitHub Actions | **10 отдельных workflows** в основном automation-проекте |
| CI concurrency | `workers=4` внутри browser job, `max-parallel=2` |
| Security / quality | npm audit, Trivy, CycloneDX SBOM, Dependabot, pinned Actions |

---

## Ключевые проекты

### [PomidorQA — система автоматизации тестирования](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)

Основной проект на **Playwright + TypeScript** с многоуровневой автоматизацией, cross-browser CI и проверяемой связью между требованиями и тестами.

- **50 / 50 требований** прошли аудит покрытия;
- **45 требований** подтверждаются автоматизированными проверками;
- **121 проверка**: Unit, API и E2E;
- **100 E2E** выполняются в Chromium, Firefox и WebKit;
- Page Objects, fixtures, API-based Arrange и централизованный cleanup;
- отдельные Accessibility, Lighthouse, Visual Regression, Nightly, Stability и AI Review workflows;
- security gates: npm audit, dependency review, CycloneDX SBOM;
- Allure, Playwright HTML, JSON/JUnit, traces, screenshots и video;
- branch protection, squash-only merge flow и обязательные checks;
- точная traceability: requirement → test-файл → объявленный `test(...)`.

Полезные документы:
[coverage matrix](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/coverage-matrix.md) ·
[test strategy](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/test-strategy.md) ·
[CI incident runbook](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/ci-incident-runbook.md)

**Стек:** Playwright · TypeScript · Node.js 24 · GitHub Actions · Allure · axe-core · Lighthouse · CycloneDX

---

### [QA Docker Monitor — PostgreSQL health & contract monitoring](https://github.com/TokhirjonYuldoshev/qa-docker-monitor)

Мониторинг, где состояние БД подтверждается не доступностью порта, а **реальной записью и точным read-back текущего запуска**.

- synthetic PostgreSQL health check с уникальным marker каждого run;
- Windows/Jenkins-compatible contract tests для production monitor script;
- aggregate `CI / Required gate`;
- Trivy, CycloneDX SBOM и reachability-проверка через `govulncheck`;
- структурированные GitHub Actions Summary;
- Telegram используется как observability transport и не переписывает database-health exit code;
- документированные monitoring boundaries и incident runbook.

**Стек:** PostgreSQL · Docker · GitHub Actions · Jenkins · Windows · Trivy · CycloneDX · govulncheck

---

### [Python + Docker — CI/CD quality pipeline](https://github.com/TokhirjonYuldoshev/my-docker-project)

Проект по построению независимых quality-сигналов для Python/Docker delivery pipeline.

- `pip check`, Flake8 и Pytest с JUnit evidence;
- Docker build + реальный runtime smoke;
- проверка non-root runtime user;
- Trivy для fixable `CRITICAL` findings;
- CycloneDX SBOM;
- единый `CI / Required gate`;
- Jenkins Declarative Pipeline;
- публикация Docker image разрешена только из подтверждённой `main`;
- Telegram отделён от build/test/security result.

**Стек:** Python 3.12 · Pytest · Flake8 · Docker · Trivy · CycloneDX · Jenkins · GitHub Actions

---

## Технологии

| Направление | Инструменты |
| --- | --- |
| Test Automation | Playwright, TypeScript, Pytest, Postman |
| API & Data | REST API, SQL, PostgreSQL, MySQL, MongoDB |
| CI/CD | GitHub Actions, Jenkins, Docker, Dependabot |
| Reporting | Allure, Playwright HTML, JUnit, JSON reports |
| Security | npm audit, Trivy, CycloneDX SBOM |
| Non-functional | axe-core, Lighthouse, Visual Regression |
| QA tools | DevTools, Charles Proxy, Jira, YouTrack, Qase, TestRail |
| Version Control | Git, GitHub |

<details>
<summary><b>Дополнительная QA-практика: manual, API, SQL, mobile</b></summary>

### Web / manual testing

- 5 чек-листов и **45+ тест-кейсов** для корзины, checkout и оплаты;
- **28 баг-репортов**;
- локализация проблем через DevTools Network и Console;
- API- и SQL-проверки данных.

[Документация DemoShopping](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=0#gid=0)

### Postman

- [PetStore Collection](./PetStore.postman_collection.json) — User / Pet / Store / CRUD;
- [DemoShopping Collection](./DemoShopping.postman_collection.json) — Products / Cart / Orders / Payment;
- сквозные API-сценарии и автоматические проверки.

### SQL / NoSQL

JOIN, подзапросы, агрегатные функции; практика с PostgreSQL, MySQL и MongoDB.

[Примеры SQL / NoSQL](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=1293622627#gid=1293622627)

### Mobile

- Android: installation, interruptions, theme switching и пользовательские сценарии;
- **30 тест-кейсов** на основной пользовательский путь;
- баг-репорты с логами и воспроизводимыми шагами.

[Документация по mobile testing](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=292251871#gid=292251871)

</details>

<details>
<summary><b>Образование и предметный бэкграунд</b></summary>

- **Санкт-Петербургский государственный технологический институт (СПбГТИ)** — Бизнес-информатика, 2024–н.в.
- **Южно-Казахстанская государственная медицинская академия (ЮКГМА)** — Фармация, провизор, 2006.

Фармацевтический бэкграунд помогает быстро погружаться в предметную область, особенно в системах с повышенными требованиями к качеству данных и процессов.

</details>

---

## Контакты

- **Email:** [toxir.yuldoshev1983@gmail.com](mailto:toxir.yuldoshev1983@gmail.com)
- **Telegram:** [@TokhirjonYuldoshev](https://t.me/TokhirjonYuldoshev)
- **LinkedIn:** [tokhirjon-yuldoshev](https://www.linkedin.com/in/tokhirjon-yuldoshev/)
