Hi, I'm Taras Iasko 👋  
Backend & DevOps Engineer | Docker · Kubernetes · Terraform · CI/CD · Observability · Secure Pipelines

Software engineer with 3+ years in commercial development and hands-on DevOps on production projects. I build and operate containerized systems end-to-end: Spring Boot backends, security-hardened CI/CD pipelines, Infrastructure as Code, monitoring and alerting, and secrets management. Currently Backend Tech Lead on a production real-time multiplayer platform, where I own both the backend architecture and the delivery pipeline.

I like systems that are reproducible, observable and safe by default, and I learn new tooling by building something real with it.

---

## 🛠️ DevOps & Infrastructure

**Containers & orchestration:** Docker, Docker Compose, Kubernetes (kind, manifests, kustomize, Helm, StatefulSets, ConfigMaps/Secrets, PVCs)  
**Infrastructure as Code:** Terraform (deploying Kubernetes manifests to a remote Rocky Linux server)  
**CI/CD:** Jenkins (webhook-triggered pipelines, auto-deploy), GitHub Actions (GHCR images, deploy jobs)  
**Security tooling:** HashiCorp Vault, Trivy, OWASP ZAP, Snyk, Semgrep, Gitleaks, GitGuardian  
**Monitoring & alerting:** Prometheus, Grafana, Loki + Promtail, Alertmanager (Telegram and email notifications)  
**Linux & networking:** Ubuntu, Rocky Linux, Nginx (reverse proxy, load balancing, rate limiting with Lua), Certbot / HTTPS certificates, journalctl, systemd, cron, network diagnostics (ping, dig, telnet, nc, ss)  
**Scripting:** Bash, Python (automation, load testing)  
**Messaging:** Apache Kafka (fundamentals)  
**Cloud / hosting:** Hetzner VPS, DigitalOcean, Azure

## ☕ Backend

Java 17/21, Spring Boot, Spring Security, Spring MVC, JPA/Hibernate, REST API, WebSocket, OAuth2 / JWT  
PostgreSQL, MySQL, MongoDB, Redis, MinIO  
JUnit, Mockito, Selenium, TDD, code review, clean code, design patterns

## 🌐 Frontend (working knowledge)

React, TypeScript, JavaScript, Thymeleaf

---

## 📦 Projects

### MafiaTheGame — Production Real-Time Multiplayer Platform
Role: Backend Tech Lead · Team of 4 · [mafiathegames.com](https://mafiathegames.com)

Own the backend architecture and the delivery pipeline end-to-end; direct a second backend developer and mentor junior contributors.

**Infrastructure & delivery**
• Operate 13+ containerized services (Spring Boot, MongoDB, Redis, MinIO, Nginx, Vault, monitoring stack)  
• Jenkins CI/CD pipeline with webhook-triggered automatic deployment to a Hetzner VPS  
• Security stages in the pipeline: Gitleaks, Semgrep, Snyk, Trivy, OWASP ZAP  
• Prometheus / Grafana / Loki monitoring with Alertmanager routing alerts to Telegram  
• Running the full stack on Kubernetes (kind): hand-written manifests, then kustomize and a Helm chart; MongoDB as a StatefulSet; practicing pod failover across replicas  
• Terraform code for deploying the Kubernetes manifests to a remote Rocky Linux server  
• Migrating the deployment to GitHub Actions with images in GHCR

**Security**
• 3-layer bot protection: Cloudflare (WAF / Captcha) → Nginx with Lua rate limiting (keeps load off the Java backend) → Redis block state  
• Auth design: OAuth2 login via Google/GitHub exchanging a one-time code for a JWT; short-lived access tokens, refresh tokens in HttpOnly cookies; Redis-backed JTI store so logout/revocation invalidates tokens immediately  
• Secrets incident: a secret was committed to git; I rotated it, cleaned the history and added Gitleaks and GitGuardian to block future commits

**Backend & quality**
• Spring Boot backend with Spring Security, WebSocket real-time communication, MongoDB + Redis serving live multiplayer sessions  
• 600+ unit and integration tests (JUnit, Mockito) in a TDD workflow, plus custom Python load-testing tooling

**Incidents I diagnosed and fixed**
• OOM kills (resized the server and tuned memory)  
• Docker networking issues (localhost vs. service names inside containers)  
• A 502 Bad Gateway: found via journalctl that Nginx had stopped after a bad config change under load; fixed the config and restarted the service

Stack: Java 21, Spring Boot, MongoDB, Redis, Docker, Kubernetes, Terraform, Jenkins, GitHub Actions, Nginx, Vault, Prometheus/Grafana/Loki, Python

---

### NovaMarket (ShadowStore) — E-Commerce Platform
Role: Full-Stack / Backend Developer (freelance, two engagements) · [shadowstore.app](https://shadowstore.app)

Rescued a legacy Spring MVC codebase and later returned for a modernization pass.

• Migrated legacy Spring MVC to Spring Boot with Thymeleaf server-side rendering  
• Rebuilt the storefront and admin panel: product catalog, shopping cart, session-based auth  
• Upgraded Spring Boot 2.4 → 3.x and JDK 21; migrated the persistence layer to MongoDB  
• Set up Jenkins CI/CD with OWASP ZAP scanning and automated deployment to Azure

Stack: Java, Spring Boot 3, JDK 21, Thymeleaf, MongoDB, Docker, Jenkins, OWASP ZAP, Azure

---

### Online English School Platform — Security Audit & Refactor
Role: Backend Developer & DevOps (freelance) · Client name withheld

• Audited a legacy multi-language backend and found hardcoded secrets in a public repository; fixed secrets handling  
• Diagnosed a recurring server crash caused by old Docker images and dangling builds eating disk and RAM; added a weekly cron + Bash cleanup script  
• Refactored ad-hoc multithreaded logic into dedicated services

Stack: Java, Python, JavaScript, Docker, Git

---

### Other projects
• **Online School Management System** — Spring Boot REST API with JWT and role-based access control; user management, scheduling and grade tracking; JUnit/Mockito and Selenium end-to-end tests  
• **Winner** — corporate website with a React admin panel and Node.js backend; i18n, WebSocket messaging, PostgreSQL schema design ([uk-winner.com](https://uk-winner.com/en/))

---

## 🎓 Education


• B.Sc. (Bc.), Automobile Production, TUKE Košice

## 🌍 Languages

Ukrainian (native) · Russian (fluent) · Slovak (C1) · English (B1, actively improving) · German (basic)

---

## 📈 Currently Learning

• Ansible  
• Kubernetes in production-style setups (load balancing, failover)  
• Python for automation  
• English for technical communication

---

## 📫 Contact

GitHub: https://github.com/TorresSteit  
LinkedIn: https://linkedin.com/in/torressteit  
Location: Bratislava, Slovakia
