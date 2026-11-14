# Hi, I'm Ali Emad 👋

**Backend Software Engineer** building payment systems in **fintech**, with a **low-level / embedded** background.

I work on the POS software team at **[Paymob](https://paymob.com)**, building backend services for point-of-sale payments.
I studied Electronics & Communication Engineering at Alexandria University, where I started with C, microcontrollers and RTOS.
That background still shapes how I write backend code: I care about what runs under the framework, where state lives,
and what happens when two requests hit the same row at the same time.

📍 Egypt · 💼 [LinkedIn](https://www.linkedin.com/in/ali-emad-a90288218/) · ✉️ [aliemadabdellatif@gmail.com](mailto:aliemadabdellatif@gmail.com)

---

### 🧰 Tech stack

**Backend:** Python · Django · Django REST Framework · FastAPI · Celery · Redis
**Data:** PostgreSQL · SQLite
**Infra & DevOps:** Docker · GitHub Actions · AWS · Linux
**Low-level:** C · C++ · bare-metal AVR / 8051 · RTOS scheduling · layered MCAL/HAL drivers · Linux

---

### 🏗️ What I've built

| | Project | What it is |
|---|---|---|
| 💳 | **POS payments backend** · *Paymob* | Backend services for point-of-sale payment flows (private, company code) |
| 🏥 | **Pharmacy management SaaS** · *contract* | Full pharmacy platform: inventory, POS, accounting, online store, AI attendance. [Details ↓](#-pharmacy-management-saas) |
| 🔧 | **Spare-parts shop system** · *own product* | Arabic-first inventory and stock system for car spare-parts shops: Django + React, offline-first, packaged as a one-click Windows installer, planned to become a cloud SaaS (private) |
| ♻️ | [**dropme-recycling-backend**](https://github.com/aliemadabdo/dropme-recycling-backend) | Scan → recycle → earn-points API with an audited points ledger, DB-level idempotency, rate limits, JWT, Docker |
| ⚙️ | [**Django-code-generator**](https://github.com/aliemadabdo/Django-code-generator) | Tool that generates Django models, forms and URLs from a web UI |

---

### 🏥 Pharmacy Management SaaS

A platform for running multi-branch pharmacies. I work on it as a backend engineer (contract, private code).
It is split into four services: **Backend** (Django + DRF), **Frontend**, **AI service** (FastAPI) and **Online Store**.

**What I built**

- **Inventory and stock:** stock tracked per product, batch and branch; purchase orders; a PostgreSQL reconciliation query and data migration that fixed stock discrepancies at batch-branch level
- **POS and pricing:** offline-capable POS using a write-ahead queue (sales are saved locally first and synced when the connection returns), a two-level discount and tax pricing system, and receipts and payments
- **Online store:** a `store` app (cart, admin) reusing the platform's global customers, receipts and payments, with card payments through **Paymob**
- **Real-time notifications:** Django Channels WebSockets with a custom JWT authentication middleware, plus DRF endpoints
- **Dashboards:** section-grouped API endpoints, precomputed by Celery Beat and cached in Redis so they load fast
- **Thermal label printing:** an API that generates TSPL printer commands, with Arabic text rendered as bitmaps (reshaping and right-to-left handling)
- **AI attendance service:** face-recognition attendance as a separate FastAPI service with its own database. It can be sold alone, and it stays in sync with the PMS over webhooks and REST when both are installed
- **Async jobs and performance:** Celery + Redis in production (emails, password-reset flow, scheduled jobs), N+1 query fixes and serializer and queryset tuning, OpenAPI docs with drf-spectacular

**Stack:** Python · Django · DRF · Django Channels · FastAPI · PostgreSQL · Celery · Redis · Docker Compose · GitHub Actions

---

### 🔩 Low-level roots

| | Project | What it is |
|---|---|---|
| 🚗 | [**Collision-Avoidance**](https://github.com/aliemadabdo/Collision-Avoidance) | Bare-metal AVR robot car on a small timer-driven RTOS scheduler we wrote ourselves, with layered MCAL/HAL drivers (ultrasonic via input capture, PWM motors, LCD) |
| 📡 | [**vehicle_telemetry**](https://github.com/aliemadabdo/vehicle_telemetry) | C++ vehicle telemetry simulator: polymorphic sensors, RAII, singleton logger, multi-platform CI |
| 💳 | [**Payment-App-Project**](https://github.com/aliemadabdo/Payment-App-Project) | Card → terminal → server payment flow in plain C |
| 🎓 | **ADAS + V2X** · *graduation project* | Advanced Driver Assistance System with Driver Monitoring and Vehicle-to-Everything communication |
