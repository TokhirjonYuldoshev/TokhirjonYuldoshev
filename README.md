<p align="center">
  <img src="./assets/qa-engineer-banner.svg" alt="QA Engineer — Manual · Automation · API · Playwright" width="100%">
</p>

<h1 align="center">Тохиржон Йулдошев</h1>

<p align="center">
  <strong>QA Engineer · Manual + Automation · API · Playwright · TypeScript</strong>
</p>

<p align="center">
  <a href="https://drive.google.com/drive/folders/1jOgOuHUcla3uYUn19Nq9-hPdJ7Xr0nen">Portfolio</a> ·
  <a href="https://github.com/TokhirjonYuldoshev/pomidorqa-tests">PomidorQA</a> ·
  <a href="https://drive.google.com/file/d/1XcQ2rN5_pdjz16d8FeRCuf7ShzFOVSKK/view">Resume</a> ·
  <a href="https://t.me/TokhirjonYuldoshev">Telegram</a> ·
  <a href="https://www.linkedin.com/in/tokhirjon-yuldoshev/">LinkedIn</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Playwright-TypeScript-2EAD33?logo=playwright&logoColor=white" alt="Playwright TypeScript">
  <img src="https://img.shields.io/badge/API-Postman-FF6C37?logo=postman&logoColor=white" alt="Postman API">
  <img src="https://img.shields.io/badge/CI-GitHub_Actions-2088FF?logo=githubactions&logoColor=white" alt="GitHub Actions CI">
  <img src="https://img.shields.io/badge/SQL-PostgreSQL-4169E1?logo=postgresql&logoColor=white" alt="SQL PostgreSQL">
</p>

Тестирую веб-приложения и REST API вручную и автоматизирую ключевые сценарии так, чтобы результат можно было **доказать, воспроизвести и быстро диагностировать**.

Основной стек: **Playwright + TypeScript**, REST API, Postman, Chrome DevTools, SQL, Git и GitHub Actions. Docker и Jenkins использую в отдельных учебных инженерных проектах. Основной подход: требования связываются с конкретными проверками, функциональные и инфраструктурные сигналы разделяются, а retries не используются для маскировки нестабильности.

**Санкт-Петербург · удалённый / гибридный / офисный формат**

[![PomidorQA CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml)
[![PomidorQA Security](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/security.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/security.yml)
[![Database Health](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/qa-docker-monitor/actions/workflows/main.yml)
[![Python & Docker CI](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/my-docker-project/actions/workflows/ci.yml)

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

---

## QA Portfolio

📁 **[QA Portfolio — Tokhirjon Yuldoshev](https://drive.google.com/drive/folders/1jOgOuHUcla3uYUn19Nq9-hPdJ7Xr0nen)**

### Резюме
- [Yuldoshev_Tokhirjon_QA_Resume.pdf](https://drive.google.com/file/d/1XcQ2rN5_pdjz16d8FeRCuf7ShzFOVSKK/view)

### Pizzaed — Manual QA + REST API
- [Test_Plan_Pizzaed.docx](https://drive.google.com/file/d/15k9sKUtTIPpGfeWJInJ0y-y1pWpPAwGm/view)
- [Checklist_Pizzaed_163_checks.docx](https://drive.google.com/file/d/19kPAyDkhjnGMDD6UsfZI0aGNmfVhI7D7/view)
- [Test_Cases_Pizzaed_68_cases.docx](https://drive.google.com/file/d/1bKqsyOt3x6yEm5yLOcKcuNFYnSf9TwP3/view)
- [Pizzaed_API_Postman_7_requests_11_tests.json](https://drive.google.com/file/d/15s96s0tLzJSFMU4XNQOzy27rM-kNWRZp/view)
- [Postman_Runner_11_of_11.png](https://drive.google.com/file/d/1GcxOnm7WePykHxIefxn2ibdl3iZPrGUX/view)
- [Pizzaed — Selected Bug Reports](https://docs.google.com/document/d/1SW8HppEPKJh7--DG1pnzdFJosgVcwpBKWLIWk_IS4ns/edit)

### PomidorQA — Automation QA
- [pomidorqa-tests](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)
- [PomidorQA — Automation QA Overview](https://docs.google.com/document/d/1F5aDy-gw0pHkVuSmt2PHZuCsvTmBjffh3i5T_u64C7A/edit)
- [coverage-matrix.md](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/coverage-matrix.md)

### Certificates
- [Certificates](https://drive.google.com/drive/folders/1iMNJ7UCQ5xz69Uy0mDM2vGnYydHUeNhJ)
