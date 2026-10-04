<p align="center">
  <img src="./assets/qa-engineer-banner.svg" alt="QA Engineer — Manual · Automation · API · Playwright" width="100%">
</p>

<h1 align="center">Tokhirjon Yuldoshev</h1>

<p align="center">
  <strong>QA Engineer · Manual + Automation · API · Playwright · TypeScript</strong>
</p>

<p align="center">
  <a href="https://yty.toxir-yuldoshev1983.chatgpt.site/">YTY QA Portfolio</a> ·
  <a href="https://drive.google.com/drive/folders/1jOgOuHUcla3uYUn19Nq9-hPdJ7Xr0nen">Portfolio</a> ·
  <a href="https://github.com/TokhirjonYuldoshev/pomidorqa-tests">PomidorQA</a> ·
  <a href="https://github.com/TokhirjonYuldoshev/BP-Diary-Android">BP Diary</a> ·
  <a href="https://github.com/TokhirjonYuldoshev/WinUtil-RU">WinUtil RU</a> ·
  <a href="https://drive.google.com/file/d/1sFf6KpRQRxlrhqmqi_G3z0rfFplJzo3G/view">Resume RU</a> ·
  <a href="https://drive.google.com/file/d/1J40-R5QbODzNcwXBoEmEsB0l2Xt5BvsB/view">Resume EN</a> ·
  <a href="https://drive.google.com/drive/folders/1iMNJ7UCQ5xz69Uy0mDM2vGnYydHUeNhJ">Certificates</a> ·
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

Основной стек: **Playwright + TypeScript**, REST API, Postman, Chrome DevTools, SQL, Git и GitHub Actions.

**Санкт-Петербург · удалённый / гибридный / офисный формат**

[![PomidorQA CI](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/playwright.yml)
[![PomidorQA Security](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/security.yml/badge.svg)](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/actions/workflows/security.yml)

---

## Избранные QA-проекты

### [PomidorQA — Automation QA](https://github.com/TokhirjonYuldoshev/pomidorqa-tests)

Основной automation-проект на **Playwright + TypeScript** с Unit, API и E2E-проверками, cross-browser regression и traceability от требований до тестов.

- **50 / 50 requirements** прошли аудит;
- **45 / 50 requirements automated = 90%**;
- **121 automated checks**: 10 Unit + 11 API + 100 E2E;
- **100 E2E** выполняются в Chromium, Firefox и WebKit;
- **retries=0**;
- Page Object Model, fixtures/helpers, API-based Arrange и cleanup;
- GitHub Actions quality gates, Allure, Playwright HTML, JSON/JUnit, traces, screenshots и video.

[Repository](https://github.com/TokhirjonYuldoshev/pomidorqa-tests) ·
[Coverage Matrix](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/coverage-matrix.md) ·
[Test Strategy](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/test-strategy.md) ·
[CI Runbook](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/ci-incident-runbook.md)

**Stack:** Playwright · TypeScript · Node.js · GitHub Actions · Allure · axe-core · Lighthouse

---

### [BP Diary — Android · QA · Privacy & Release Engineering](https://github.com/TokhirjonYuldoshev/BP-Diary-Android)

Android-приложение для структурированного дневника артериального давления с **local-first** хранением, аналитикой, напоминаниями, PDF-отчётами и защищёнными резервными копиями.

- текущий stable: **V18 / 5.8.2**;
- Android build и mobile UI regression в GitHub Actions;
- защищённый Full Backup: PBKDF2-SHA-256 + AES-GCM-256;
- App Lock через системную Android-аутентификацию и Screen Privacy через `FLAG_SECURE`;
- русский, English и O‘zbekcha (Lotin);
- формализованный release gate с отдельными build/UI quality checks.

[Repository](https://github.com/TokhirjonYuldoshev/BP-Diary-Android) ·
[Stable Release](https://github.com/TokhirjonYuldoshev/BP-Diary-Android/releases/tag/v5.8.2) ·
[Security](https://github.com/TokhirjonYuldoshev/BP-Diary-Android/blob/main/SECURITY.md) ·
[Architecture](https://github.com/TokhirjonYuldoshev/BP-Diary-Android/blob/main/ARCHITECTURE.md)

**Stack:** Android · JavaScript · Playwright · GitHub Actions · Security · Release Engineering

---

### [Pizzaed — Manual QA + REST API](https://drive.google.com/drive/folders/1HWGeywjJ2qnSpFE4awpLrqIGwLfKhCHu)

Учебный интернет-магазин: каталог, фильтрация, корзина, промокоды, доставка и оформление заказа.

- подготовил **чек-лист из 163 проверок**;
- разработал **68 тест-кейсов**;
- составил test plan со scope, рисками, entry/exit criteria и окружением;
- собрал Postman collection: **7 API-запросов / 11 автоматических проверок**;
- Postman Runner: **11 / 11 passed**;
- использовал variables, JavaScript и dynamic ID chaining;
- оформил отдельные **Selected Bug Reports**.

[Test Plan](https://drive.google.com/file/d/15k9sKUtTIPpGfeWJInJ0y-y1pWpPAwGm/view) ·
[Checklist — 163](https://drive.google.com/file/d/19kPAyDkhjnGMDD6UsfZI0aGNmfVhI7D7/view) ·
[Test Cases — 68](https://drive.google.com/file/d/1bKqsyOt3x6yEm5yLOcKcuNFYnSf9TwP3/view) ·
[Postman Collection](https://drive.google.com/file/d/15s96s0tLzJSFMU4XNQOzy27rM-kNWRZp/view) ·
[Runner 11/11](https://drive.google.com/file/d/1GcxOnm7WePykHxIefxn2ibdl3iZPrGUX/view) ·
[Bug Reports](https://docs.google.com/document/d/1SW8HppEPKJh7--DG1pnzdFJosgVcwpBKWLIWk_IS4ns/edit)

**Stack:** Manual QA · REST API · Postman · Chrome DevTools · Test Design

---

## Open Source Contributions

### [Chris Titus Tech — WinUtil · PR #5111](https://github.com/ChrisTitusTech/winutil/pull/5111)

Внёс документационное исправление в официальный upstream-репозиторий **ChrisTitusTech/winutil**.

- исправлено противоречие в FAQ о поддержке Windows LTSC;
- формулировка приведена в соответствие с текущей политикой поддержки Windows 11;
- изменение прошло upstream review и было **merged** в официальный проект;
- PR связан с [Issue #5117](https://github.com/ChrisTitusTech/winutil/issues/5117), закрытым после принятия изменения.

Отдельно развиваю [**WinUtil RU**](https://github.com/TokhirjonYuldoshev/WinUtil-RU) — независимую русскую локализацию WinUtil со строгим контролем upstream parity. Это отдельный проект: upstream contribution и локализационные изменения не смешиваются.

[WinUtil RU Repository](https://github.com/TokhirjonYuldoshev/WinUtil-RU) ·
[Technical Audit](https://github.com/TokhirjonYuldoshev/WinUtil-RU/blob/russian/docs/AUDIT-RU.md)

**Stack:** PowerShell · Windows · GitHub Actions · Localization · Upstream Parity

---

## Инженерные практики

- **Requirements → Test Cases → Evidence:** связываю требования с конкретными проверками и результатами.
- **Test design:** позитивные/негативные сценарии, boundary values, equivalence classes, error guessing.
- **Automation architecture:** Page Object Model, fixtures, helpers, уникальные данные и изолированные BrowserContext.
- **API testing:** Arrange/cleanup через API, Postman variables, JavaScript и автоматические assertions.
- **CI & diagnostics:** GitHub Actions, Allure, Playwright HTML, JUnit/JSON, traces, screenshots и video.
- **Reliable signal:** retries=0; продуктовые дефекты отделяются от infrastructure/CI failures.

---

## Дополнительные инженерные проекты

<details>
<summary><b>QA Docker Monitor — PostgreSQL health & contract monitoring</b></summary>

Система мониторинга PostgreSQL, где health подтверждается реальной записью и точным read-back текущего запуска.

- synthetic PostgreSQL health check;
- Windows/Jenkins-compatible contract tests;
- GitHub Actions quality gate;
- Trivy и CycloneDX SBOM;
- Telegram observability.

[Repository](https://github.com/TokhirjonYuldoshev/qa-docker-monitor)

**Stack:** PostgreSQL · PowerShell · Docker · GitHub Actions · Jenkins

</details>

<details>
<summary><b>Python + Docker — CI/CD quality pipeline</b></summary>

Учебный CI/CD-проект с независимыми quality-сигналами.

- Pytest + JUnit evidence;
- Flake8 и dependency checks;
- Docker build + runtime smoke;
- non-root validation;
- Trivy и CycloneDX SBOM;
- Jenkins Declarative Pipeline.

[Repository](https://github.com/TokhirjonYuldoshev/my-docker-project)

**Stack:** Python · Pytest · Docker · GitHub Actions · Jenkins

</details>

---


## Технологии

| Направление | Инструменты |
| --- | --- |
| Manual QA | Test design, Checklists, Test Cases, Bug Reports |
| Automation | Playwright, TypeScript |
| API | REST API, Postman, JavaScript |
| Mobile / Release | Android, mobile UI regression, release gates |
| Data | SQL, PostgreSQL, MySQL |
| QA / Debugging | Chrome DevTools, Charles Proxy |
| TMS / Bug Tracking | TestRail, TestIT, тестовые прогоны, жизненный цикл дефекта |
| CI / Reporting | GitHub Actions, Allure, Playwright HTML, JUnit, JSON |
| Platform / Scripting | PowerShell, Docker, Jenkins, Pytest |
| Security / Supply Chain | Trivy, CycloneDX SBOM |
| Version Control | Git, GitHub |

<details>
<summary><b>Образование</b></summary>

- **Санкт-Петербургский государственный технологический институт (СПбГТИ)** — Бизнес-информатика, 2024–н.в.
- **Южно-Казахстанская государственная медицинская академия (ЮКГМА)** — Фармация, провизор, 2006.

</details>

---

## Контакты

- **Email:** [toxir.yuldoshev1983@gmail.com](mailto:toxir.yuldoshev1983@gmail.com)
- **Telegram:** [@TokhirjonYuldoshev](https://t.me/TokhirjonYuldoshev)
- **LinkedIn:** [tokhirjon-yuldoshev](https://www.linkedin.com/in/tokhirjon-yuldoshev/)

---

## QA Portfolio

📁 **[Open full QA Portfolio](https://drive.google.com/drive/folders/1jOgOuHUcla3uYUn19Nq9-hPdJ7Xr0nen)**

- **Resume:** [RU](https://drive.google.com/file/d/1sFf6KpRQRxlrhqmqi_G3z0rfFplJzo3G/view) · [EN](https://drive.google.com/file/d/1J40-R5QbODzNcwXBoEmEsB0l2Xt5BvsB/view)
- **Manual QA / API:** [Pizzaed](https://drive.google.com/drive/folders/1HWGeywjJ2qnSpFE4awpLrqIGwLfKhCHu)
- **Automation QA:** [PomidorQA](https://github.com/TokhirjonYuldoshev/pomidorqa-tests) · [Coverage Matrix](https://github.com/TokhirjonYuldoshev/pomidorqa-tests/blob/main/docs/coverage-matrix.md)
- **Certificates:** [AIQA AQA](https://aiqa.su/certificate/AIQA-AQA-2026-0006) · [AIQA QA](https://aiqa.su/certificate/AIQA-2026-000001) · [Stepik Testing](https://stepik.org/cert/3095342) · [Stepik SQL](https://stepik.org/cert/3112640) · [Stepik QA Practice](https://stepik.org/cert/3095365) · [PDF copies](https://drive.google.com/drive/folders/1iMNJ7UCQ5xz69Uy0mDM2vGnYydHUeNhJ)
