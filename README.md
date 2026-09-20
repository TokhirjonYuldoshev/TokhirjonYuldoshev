# Тохиржон Йулдошев

## QA Automation Engineer · Playwright / TypeScript · API · CI/CD · Docker

Автоматизирую проверку веб-приложений и API и строю CI-процессы, где результат можно **доказать, воспроизвести и быстро диагностировать**.

Работаю с **Playwright + TypeScript**, REST API, SQL, GitHub Actions, Docker и Jenkins. Основной подход: требования связываются с конкретными проверками, функциональные и инфраструктурные сигналы разделяются, а retries не используются для маскировки нестабильности.

**Санкт-Петербург · удалённый / гибридный / офисный формат**

[![PomidorQA CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml)
[![PomidorQA Security](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/security.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/security.yml)
[![Database Health](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml)
[![Python & Docker CI](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml)

[PomidorQA](https://github.com/TokhirjonYuldoshev/pomidorqa-tests) ·
[Coverage matrix](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/coverage-matrix.md) ·
[LinkedIn](https://www.linkedin.com/in/tokhirjon-yuldoshev/) ·
[Telegram](https://t.me/TokhirjonYuldoshev) ·
[Email](mailto:toxir.yuldoshev1983@gmail.com)

---

## Инженерный подход

- **Requirements → evidence:** требование связано с конкретным test case, а не только с названием spec-файла.
- **Надёжный тестовый сигнал:** `retries=0`, уникальные данные, отдельные `BrowserContext`, причинные ожидания вместо произвольных sleep.
- **CI как quality system:** обязательные gates, branch protection, агрегирующие проверки, security checks и machine-readable reports.
- **Диагностика без угадывания:** trace, screenshots, video, JUnit/JSON, Allure, GitHub Actions Summary и incident runbooks.
- **Разделение сигналов:** продуктовые дефекты, CI/infrastructure incidents, security findings и notification failures имеют разных владельцев и не подменяют друг друга.

## Подтверждённые результаты

| Область | Результат |
| --- | --- |
| Requirement audit | **50 / 50** требований имеют определённый статус |
| Automated coverage | **45 / 50 (90%)** требований подтверждаются автоматизированными проверками |
| Exact traceability | **50 уникальных test-case references** в **22 test-файлах** |
| Автоматизация | **121 проверка**: 10 Unit + 11 API + 100 E2E |
| Cross-browser | 100 E2E в **Chromium + Firefox + WebKit**, `retries=0` |
| GitHub Actions | **10 workflows** в основном automation-проекте |
| Security / quality | npm audit, dependency review, Trivy, CycloneDX SBOM, Dependabot, pinned Actions |

---

## Избранные проекты

### [PomidorQA — test automation system](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)

Основной проект на **Playwright + TypeScript**: многоуровневая автоматизация, cross-browser regression и проверяемая traceability от требования до объявленного `test(...)`.

- **50 / 50 requirements** прошли аудит; **45 / 50 automated**;
- **121 проверка**: Unit, API и E2E;
- **100 E2E** исполняются в Chromium, Firefox и WebKit;
- Page Objects, fixtures, API-based Arrange, централизованный cleanup и независимые BrowserContext;
- Accessibility, Lighthouse, Visual Regression, Nightly, Stability и AI Review вынесены в отдельные workflows;
- обязательные CI/security gates, Allure, Playwright HTML, JSON/JUnit, traces, screenshots и video;
- squash-only merge flow и защищённый `main`.

[Coverage matrix](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/coverage-matrix.md) ·
[Test strategy](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/test-strategy.md) ·
[CI incident runbook](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/ci-incident-runbook.md)

**Стек:** Playwright · TypeScript · Node.js 24 · GitHub Actions · Allure · axe-core · Lighthouse · CycloneDX

---

### [QA Docker Monitor — PostgreSQL health & contract monitoring](https://github.com/TokhirjonYuldoshev/qa-docker-monitor)

Система мониторинга, где исправность БД подтверждается не только доступностью порта, а **реальной записью и точным read-back текущего запуска**.

- synthetic PostgreSQL health check с уникальным marker каждого run;
- Windows/Jenkins-compatible contract tests для monitor script;
- единый `CI / Required gate`;
- Trivy, CycloneDX SBOM и reachability-проверка через `govulncheck`;
- Telegram остаётся observability transport и не переписывает database-health exit code;
- monitoring boundaries и incident response задокументированы.

**Стек:** PostgreSQL · Docker · GitHub Actions · Jenkins · Windows · Trivy · CycloneDX · govulncheck

---

### [Python + Docker — CI/CD quality pipeline](https://github.com/TokhirjonYuldoshev/my-docker-project)

Pipeline с независимыми quality-сигналами для Python/Docker delivery.

- `pip check`, Flake8 и Pytest с JUnit evidence;
- Docker build + runtime smoke + non-root policy;
- Trivy для fixable `CRITICAL` findings и CycloneDX SBOM;
- единый `CI / Required gate`;
- Jenkins Declarative Pipeline;
- публикация Docker image разрешена только из подтверждённой `main`;
- Telegram отделён от build/test/security result.

**Стек:** Python 3.12 · Pytest · Flake8 · Docker · Trivy · CycloneDX · Jenkins · GitHub Actions

---

## Технологии

| Направление | Инструменты |
| --- | --- |
| Automation | Playwright, TypeScript, Pytest, Postman |
| API & Data | REST API, SQL, PostgreSQL, MySQL, MongoDB |
| CI/CD | GitHub Actions, Jenkins, Docker, Dependabot |
| Reporting | Allure, Playwright HTML, JUnit, JSON |
| Security | npm audit, Trivy, CycloneDX SBOM |
| Non-functional | axe-core, Lighthouse, Visual Regression |
| QA / Debugging | DevTools, Charles Proxy, Jira, YouTrack, Qase, TestRail |
| Version Control | Git, GitHub |

<details>
<summary><b>Дополнительная QA-практика: manual, API, SQL, mobile</b></summary>

### Web / manual testing

- 5 чек-листов и **45+ тест-кейсов** для корзины, checkout и оплаты;
- **28 баг-репортов**;
- локализация проблем через DevTools Network и Console;
- API- и SQL-проверки данных.

[Документация DemoShopping](https://docs.google.com/spreadsheets/d/10L3WmvIuV3qYr8N86WoHXyFqlFgBHpgU7K7eCbUssYk/edit?pli=1&gid=0#gid=0)

### API / Postman

- [PetStore Collection](./PetStore.postman_collection.json) — User / Pet / Store / CRUD;
- [DemoShopping Collection](./DemoShopping.postman_collection.json) — Products / Cart / Orders / Payment;
- сквозные API-сценарии и автоматические проверки.

### SQL / NoSQL

JOIN, подзапросы и агрегатные функции; практика с PostgreSQL, MySQL и MongoDB.

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
