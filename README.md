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
| 🏥 | **Healthcare / pharmacy SaaS** · *contract* | Pharmacy management platform: Django + DRF, PostgreSQL, Celery, Redis, Docker, CI/CD, plus a separate FastAPI AI attendance service kept in sync over webhooks and REST (private) |
| 🔧 | **Spare-parts shop system** · *own product* | Arabic-first inventory and stock system for car spare-parts shops: Django + React, offline-first, packaged as a one-click Windows installer, planned to become a cloud SaaS (private) |
| ♻️ | [**dropme-recycling-backend**](https://github.com/aliemadabdo/dropme-recycling-backend) | Scan → recycle → earn-points API with an audited points ledger, DB-level idempotency, rate limits, JWT, Docker |
| ⚙️ | [**Django-code-generator**](https://github.com/aliemadabdo/Django-code-generator) | Tool that generates Django models, forms and URLs from a web UI |

### 🔩 Low-level roots

| | Project | What it is |
|---|---|---|
| 🚗 | [**Collision-Avoidance**](https://github.com/aliemadabdo/Collision-Avoidance) | Bare-metal AVR robot car on a small timer-driven RTOS scheduler we wrote ourselves, with layered MCAL/HAL drivers (ultrasonic via input capture, PWM motors, LCD) |
| 📡 | [**vehicle_telemetry**](https://github.com/aliemadabdo/vehicle_telemetry) | C++ vehicle telemetry simulator: polymorphic sensors, RAII, singleton logger, multi-platform CI |
| 💳 | [**Payment-App-Project**](https://github.com/aliemadabdo/Payment-App-Project) | Card → terminal → server payment flow in plain C |
| 🎓 | **ADAS + V2X** · *graduation project* | Advanced Driver Assistance System with Driver Monitoring and Vehicle-to-Everything communication |

---

### 📌 What I care about

- **Correctness under concurrency**: transactions, locking, idempotency, ledgers that always balance
- **Boring, reliable infrastructure**: containers, CI, observability
- **Learning now:** Terraform and Kubernetes
