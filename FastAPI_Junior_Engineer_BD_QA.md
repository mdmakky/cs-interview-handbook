<a id="top"></a>

# ⚡ FastAPI Interview Preparation Handbook
### বাংলাদেশের Python Backend Developer ও Junior SWE-দের জন্য সম্পূর্ণ FastAPI Interview Guide

---

> **💡 হ্যান্ডবুক ব্যবহারের নিয়ম:**
> প্রতিটি টপিক মনোযোগ দিয়ে পড়ুন। Code examples নিজে লিখুন। Interview questions নিজে উত্তর দেওয়ার চেষ্টা করুন তারপর model answer দেখুন।

---

<a id="toc"></a>

## 📋 সূচিপত্র — Table of Contents

> **💡 নিচের যেকোনো PART এ সরাসরি ক্লিক করুন। প্রতিটি PART এর শেষে [⬆ শীর্ষে ফিরুন](#top) বাটন আছে।**

| | PART | বিষয়বস্তু |
|:-:|------|------------|
| 📘 | [**PART 1** — FastAPI Fundamentals](#part1) | FastAPI কী, ASGI vs WSGI, Architecture, Path/Query Params, Pydantic, Validation |
| 📗 | [**PART 2** — Routing & API Development](#part2) | APIRouter, CRUD, HTTP Methods, File Upload, Dependency Injection, Middleware |
| 📙 | [**PART 3** — Database Integration](#part3) | SQLAlchemy, PostgreSQL, ORM, Alembic, CRUD, Transactions |
| 📕 | [**PART 4** — Authentication & Security](#part4) | JWT, OAuth2, Password Hashing, CORS, Rate Limiting |
| 📓 | [**PART 5** — Async Programming](#part5) | async/await, Event Loop, Async DB, Concurrent Requests, Background Tasks |
| 📔 | [**PART 6** — Advanced FastAPI](#part6) | WebSockets, Streaming, Custom Middleware, Exception Handling, Caching |
| 📒 | [**PART 7** — Testing & Debugging](#part7) | Pytest, TestClient, Fixtures, Mocking, Logging, Debugging |
| 📃 | [**PART 8** — Deployment & DevOps](#part8) | Uvicorn, Docker, Nginx, CI/CD, VPS Deployment |
| 🗂️ | [**PART 9** — System Design](#part9) | Microservices, Message Queues, API Gateway, Redis, DB Scaling |
| 💼 | [**PART 10** — FastAPI Projects](#part10) | Auth System, Blog API, E-commerce, Chat API |
| ❓ | **PART 11** — Interview Q&A Bank *(Coming Soon)* | ১৫০ Theoretical + ১০০ Coding + Rapid-fire |
| 🇧🇩 | **PART 12** — BD Interview Prep *(Coming Soon)* | Local company patterns, Mock interview, Project explanation |

<details>
<summary><strong>📘 PART 1 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [১.১ FastAPI কী?](#১১-fastapi-কী)
- [১.২ FastAPI কেন জনপ্রিয়?](#১২-fastapi-কেন-জনপ্রিয়)
- [১.৩ FastAPI vs Flask vs Django](#১৩-fastapi-vs-flask-vs-django)
- [১.৪ ASGI vs WSGI](#১৪-asgi-vs-wsgi)
- [১.৫ FastAPI Architecture](#১৫-fastapi-architecture)
- [১.৬ FastAPI Install ও Project Structure](#১৬-fastapi-install-ও-project-structure)
- [১.৭ প্রথম API তৈরি](#১৭-প্রথম-api-তৈরি)
- [১.৮ Path Parameters](#১৮-path-parameters)
- [১.৯ Query Parameters](#১৯-query-parameters)
- [১.১০ Request Body](#১১০-request-body)
- [১.১১ Response Model](#১১১-response-model)
- [১.১২ Pydantic Basics](#১১২-pydantic-basics)
- [১.১৩ Type Hints](#১১৩-type-hints)
- [১.১৪ Validation](#১১৪-validation)
- [১.১৫ PART 1 — Interview Q&A](#১১৫-part-1--interview-questions--answers)

</details>

<details>
<summary><strong>📗 PART 2 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [২.১ APIRouter](#২১-apirouter)
- [২.২ Modular Routing](#২২-modular-routing)
- [২.৩ CRUD APIs তৈরি](#২৩-crud-apis-তৈরি)
- [২.৪ HTTP Methods বিস্তারিত](#২৪-http-methods-বিস্তারিত)
- [২.৫ Status Codes](#২৫-status-codes)
- [২.৬ Response Handling](#২৬-response-handling)
- [২.৭ File Upload](#২৭-file-upload)
- [২.৮ Form Data](#২৮-form-data)
- [২.৯ Header Handling](#২৯-header-handling)
- [২.১০ Cookie Handling](#২১০-cookie-handling)
- [২.১১ Dependency Injection](#২১১-dependency-injection)
- [২.১২ Middleware](#২১২-middleware)
- [২.১৩ Background Tasks](#২১৩-background-tasks)
- [২.১৪ PART 2 — Interview Q&A](#২১৪-part-2--interview-questions--answers)

</details>

<details>
<summary><strong>📙 PART 3 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৩.১ SQLAlchemy কী?](#৩১-sqlalchemy-কী)
- [৩.২ FastAPI তে SQLAlchemy Setup](#৩২-fastapi-তে-sqlalchemy-setup)
- [৩.৩ Database Models](#৩৩-database-models)
- [৩.৪ Pydantic Schemas vs DB Models](#৩৪-pydantic-schemas-vs-db-models)
- [৩.৫ Database Session Dependency](#৩৫-database-session-dependency)
- [৩.৬ CRUD Operations with DB](#৩৬-crud-operations-with-db)
- [৩.৭ Relationships (One-to-Many, Many-to-Many)](#৩৭-relationships)
- [৩.৮ Alembic Migration](#৩৮-alembic-migration)
- [৩.৯ Async SQLAlchemy](#৩৯-async-sqlalchemy)
- [৩.১০ Connection Pooling ও Transactions](#৩১০-connection-pooling-ও-transactions)
- [৩.১১ PART 3 — Interview Q&A](#৩১১-part-3--interview-questions--answers)

</details>

<details>
<summary><strong>📕 PART 4 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৪.১ Authentication vs Authorization](#৪১-authentication-vs-authorization)
- [৪.২ Password Hashing](#৪২-password-hashing)
- [৪.৩ JWT Authentication](#৪৩-jwt-authentication)
- [৪.৪ OAuth2 with Password Flow](#৪৪-oauth2-with-password-flow)
- [৪.৫ Refresh Tokens](#৪৫-refresh-tokens)
- [৪.৬ Role-Based Access Control (RBAC)](#৪৬-role-based-access-control-rbac)
- [৪.৭ CORS](#৪৭-cors)
- [৪.৮ Rate Limiting](#৪৮-rate-limiting)
- [৪.৯ Environment Variables ও Secrets](#৪৯-environment-variables-ও-secrets)
- [৪.১০ API Security Best Practices](#৪১০-api-security-best-practices)
- [৪.১১ PART 4 — Interview Q&A](#৪১১-part-4--interview-questions--answers)

</details>

---

<a id="part1"></a>

# PART 1: FastAPI Fundamentals (মূল ধারণাসমূহ)

> **📍 এই PART এর Sections:** [১.১](#১১-fastapi-কী) · [১.২](#১২-fastapi-কেন-জনপ্রিয়) · [১.৩](#১৩-fastapi-vs-flask-vs-django) · [১.৪](#১৪-asgi-vs-wsgi) · [১.৫](#১৫-fastapi-architecture) · [১.৬](#১৬-fastapi-install-ও-project-structure) · [১.৭](#১৭-প্রথম-api-তৈরি) · [১.৮](#১৮-path-parameters) · [১.৯](#১৯-query-parameters) · [১.১০](#১১০-request-body) · [১.১১](#১১১-response-model) · [১.১২](#১১২-pydantic-basics) · [১.১৩](#১১৩-type-hints) · [১.১৪](#১১৪-validation) · [১.১৫](#১১৫-part-1--interview-questions--answers)

---

## ১.১ FastAPI কী?

**FastAPI** হলো Python দিয়ে তৈরি একটি modern, high-performance web framework যা দিয়ে REST API বানানো হয়। এটি Python 3.7+ এর **type hints** এর উপর ভিত্তি করে তৈরি এবং **Starlette** ও **Pydantic** এর উপর নির্মিত।

**মূল কথায়:** FastAPI = Fast (পারফরম্যান্সে) + API (তৈরির কাজে সর্বোত্তম)।

### 🏠 বাস্তব জীবনের উদাহরণ

একটি **রেস্তোরাঁর অর্ডার সিস্টেম** কল্পনা করুন:
- **Waiter** = API Endpoint (client এর request নেয়)
- **Kitchen** = Backend logic (কাজ করে)
- **Menu** = API Documentation (কী কী পাওয়া যায়)
- **Order Slip** = Request Body (কী চাওয়া হয়েছে)
- **Food** = Response (ফলাফল ফেরত দেয়)

FastAPI তে আপনি menu (docs) automatically পান, order slip এর format validate হয়, এবং kitchen অনেক দ্রুত কাজ করে।

### 💡 FastAPI এর জন্ম কীভাবে?

```
২০১৮ সালে Sebastián Ramírez (tiangolo) FastAPI তৈরি করেন।
তিনি Flask এর simplicity এবং Django এর power একসাথে চাইছিলেন,
কিন্তু modern async support ও automatic validation সহ।
ফলাফল: FastAPI — যা এখন GitHub এ সবচেয়ে জনপ্রিয় Python frameworks এর একটি।
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI কী? কেন এটি ব্যবহার করবেন?"

**আদর্শ উত্তর:**
> "FastAPI হলো Python এর একটি modern web framework যা দিয়ে REST API তৈরি করা হয়। এটি Starlette এর উপর built, তাই async support আছে। Pydantic ব্যবহার করে automatic data validation করে। সবচেয়ে বড় সুবিধা হলো এটি NodeJS এবং Go এর কাছাকাছি performance দেয়, Python এর সহজ syntax রেখে। আমি FastAPI বেছে নিই কারণ এটি type hints থেকে automatic API documentation generate করে, validation built-in আছে, এবং async operations সহজে handle করা যায়।"

### ⚠️ Common Mistakes

- ❌ FastAPI = Django REST Framework মনে করা
- ❌ FastAPI শুধু small project এর জন্য — বড় production app এও চলে
- ❌ `async def` না বুঝে ব্যবহার করা
- ✅ FastAPI একটি standalone framework, Django এর extension নয়

### ❓ Follow-up Interview Questions

1. FastAPI এবং Flask এর মধ্যে কোনটি বেছে নেবেন এবং কেন?
2. FastAPI কি production-ready?
3. FastAPI তে automatic documentation কীভাবে কাজ করে?

---

## ১.২ FastAPI কেন জনপ্রিয়?

FastAPI এর জনপ্রিয়তার কারণ শুধু speed নয় — এর developer experience অনেক উন্নত।

### FastAPI এর মূল সুবিধাসমূহ

| সুবিধা | বিস্তারিত |
|--------|-----------|
| **🚀 High Performance** | NodeJS ও Go এর সমতুল্য speed। Python frameworks এর মধ্যে সবচেয়ে দ্রুত। |
| **📝 Automatic Docs** | Swagger UI (/docs) এবং ReDoc (/redoc) automatic generate হয় |
| **✅ Built-in Validation** | Pydantic দিয়ে request/response data automatically validate হয় |
| **🔑 Type Safety** | Python type hints দিয়ে editor autocomplete ও error detection |
| **⚡ Async Support** | `async/await` দিয়ে concurrent requests handle করা যায় |
| **🧪 Easy Testing** | Built-in TestClient দিয়ে সহজে test লেখা যায় |
| **🔌 Standards-based** | OpenAPI ও JSON Schema standard follow করে |
| **📦 Dependency Injection** | Built-in DI system যা clean architecture নিশ্চিত করে |

### FastAPI Performance বেঞ্চমার্ক

```
Requests per second (approximate):
┌─────────────────────────────────────────────┐
│ FastAPI      ████████████████████  ~50,000  │
│ Django REST  ████████             ~10,000  │
│ Flask        █████████            ~12,000  │
│ Node/Express ████████████████████  ~45,000  │
└─────────────────────────────────────────────┘
(এগুলো approximate, real-world এ vary করে)
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI এত popular কেন?"

**আদর্শ উত্তর:**
> "FastAPI জনপ্রিয় কারণ এটি একসাথে তিনটি বড় সমস্যা সমাধান করে। প্রথমত, performance — এটি ASGI এবং async support এর কারণে Python frameworks এর মধ্যে সবচেয়ে দ্রুত। দ্বিতীয়ত, developer productivity — type hints থেকে automatic validation এবং documentation generate হওয়ায় manually অনেক কম কাজ করতে হয়। তৃতীয়ত, modern standards — OpenAPI specification follow করে, তাই industry standard API documentation তৈরি হয়। এই তিনটি combination এটিকে Python backend development এর first choice বানিয়েছে।"

### ⚠️ Common Mistakes

- ❌ "FastAPI শুধু speed এর জন্য" — validation ও DX এর জন্যও সমান গুরুত্বপূর্ণ
- ✅ Performance + Developer Experience উভয় কারণে জনপ্রিয়

---

## ১.৩ FastAPI vs Flask vs Django

এটি বাংলাদেশের interview তে সবচেয়ে বেশি জিজ্ঞেস করা প্রশ্নগুলোর একটি।

### বিস্তারিত তুলনা টেবিল

| বিষয় | FastAPI | Flask | Django |
|-------|---------|-------|--------|
| **Type** | API Framework | Micro Framework | Full-stack Framework |
| **Performance** | ⭐⭐⭐⭐⭐ (Highest) | ⭐⭐⭐ | ⭐⭐⭐ |
| **Learning Curve** | মাঝারি | সহজ | কঠিন |
| **Async Support** | ✅ Built-in | ⚠️ Limited | ⚠️ Limited (Django 4+) |
| **Auto Documentation** | ✅ (Swagger/ReDoc) | ❌ Manual | ❌ Manual |
| **Data Validation** | ✅ (Pydantic) | ❌ Manual | ⚠️ Forms only |
| **ORM** | ❌ (আলাদা SQLAlchemy) | ❌ (আলাদা) | ✅ Built-in |
| **Admin Panel** | ❌ | ❌ | ✅ |
| **Template Engine** | ❌ (API-focused) | ✅ (Jinja2) | ✅ (Django Template) |
| **Use Case** | REST API, Microservices | Simple API, Prototype | Full-stack Web App |
| **Community** | নতুন কিন্তু দ্রুত বাড়ছে | বড় | সবচেয়ে বড় |
| **Production Use** | Netflix, Uber, Microsoft | Pinterest, LinkedIn | Instagram, Spotify |

### কখন কোনটি ব্যবহার করবেন?

```
FastAPI ব্যবহার করুন যখন:
  ✅ শুধু REST API বানাতে হবে
  ✅ High performance দরকার
  ✅ Async operations আছে
  ✅ Microservices architecture
  ✅ Modern Python project

Flask ব্যবহার করুন যখন:
  ✅ Simple, small API দরকার
  ✅ Maximum flexibility চাই
  ✅ Prototype বা POC
  ✅ Flask ecosystem পরিচিত

Django ব্যবহার করুন যখন:
  ✅ Full-stack web application
  ✅ Admin panel দরকার
  ✅ Rapid development (battery-included)
  ✅ Built-in ORM দিয়ে কাজ করতে চাই
  ✅ Large team project
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI, Flask, Django এর মধ্যে পার্থক্য কী?"

**আদর্শ উত্তর:**
> "তিনটি Python web framework কিন্তু ভিন্ন ভিন্ন use case এর জন্য। Django হলো 'batteries included' — Admin panel, ORM, Authentication সব built-in আছে, full-stack web app এর জন্য সেরা। Flask হলো micro-framework — lightweight, flexible, কিন্তু সব নিজে add করতে হয়। FastAPI হলো modern API framework — performance সবচেয়ে বেশি, async built-in, automatic documentation ও validation আছে। আমি backend API বানাতে হলে FastAPI বেছে নিই, full-stack web app এর দরকার হলে Django।"

### ⚠️ Common Mistakes

- ❌ "Django এর চেয়ে FastAPI ভালো" — দুটি আলাদা purpose এর জন্য
- ❌ Flask কে outdated বলা — এখনও অনেক জায়গায় use হয়
- ✅ সঠিক tool সঠিক কাজে

---

## ১.৪ ASGI vs WSGI

এই concept টি FastAPI এর performance এর রহস্য বোঝার চাবিকাঠি।

### WSGI কী? (Web Server Gateway Interface)

**WSGI** হলো Python web applications এবং web servers এর মধ্যে communication এর একটি পুরনো standard (PEP 3333)।

```
WSGI এর সমস্যা:
Client Request → WSGI Server → Python App → Response
(একবারে একটি request, synchronous)
```

**WSGI Servers:** Gunicorn, uWSGI
**WSGI Frameworks:** Django, Flask

### ASGI কী? (Asynchronous Server Gateway Interface)

**ASGI** হলো WSGI এর modern successor যা async operations, WebSockets, এবং HTTP/2 support করে।

```
ASGI এর সুবিধা:
Multiple Clients → ASGI Server → Python App (async) → Multiple Responses
(একসাথে অনেক request, asynchronous)
```

**ASGI Servers:** Uvicorn, Hypercorn, Daphne
**ASGI Frameworks:** FastAPI, Starlette, Django (3.0+)

### WSGI vs ASGI তুলনা

| বিষয় | WSGI | ASGI |
|-------|------|------|
| **Concurrency** | Synchronous | Asynchronous |
| **WebSocket** | ❌ নেই | ✅ আছে |
| **HTTP/2** | ❌ নেই | ✅ আছে |
| **Performance** | কম | বেশি |
| **Complexity** | সহজ | মাঝারি |
| **Python Version** | Python 2/3 | Python 3.5+ |
| **Server** | Gunicorn, uWSGI | Uvicorn, Hypercorn |

### Real-Life Analogy

```
WSGI = একটি single-lane রাস্তা
  → একটি গাড়ি যায়, সেটি শেষ হলে পরেরটি যায়
  → Traffic jam হয় বেশি request এলে

ASGI = একটি multi-lane highway
  → অনেক গাড়ি একসাথে যেতে পারে
  → Long wait (DB query) এর সময় অন্য গাড়ি চলতে পারে
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "ASGI এবং WSGI এর পার্থক্য কী? FastAPI কোনটি ব্যবহার করে?"

**আদর্শ উত্তর:**
> "WSGI হলো পুরনো Python web server standard যা synchronous — একবারে একটি request handle করে। ASGI হলো এর modern async version যা একসাথে অনেক concurrent request handle করতে পারে এবং WebSocket ও HTTP/2 support করে। FastAPI, ASGI framework Starlette এর উপর built, তাই এটি async/await দিয়ে high concurrency handle করতে পারে। Production এ FastAPI কে Uvicorn ASGI server এর সাথে run করা হয়।"

### ⚠️ Common Mistakes

- ❌ ASGI মানে শুধু `async def` লিখলেই হয় — Uvicorn server লাগবে
- ❌ WSGI server (Gunicorn alone) দিয়ে FastAPI চালানো
- ✅ FastAPI → Uvicorn (ASGI) → Production এ Gunicorn+Uvicorn worker

---

## ১.৫ FastAPI Architecture

FastAPI কীভাবে internally কাজ করে সেটি বুঝলে interview এ অনেক প্রশ্নের উত্তর দেওয়া সহজ হয়।

### FastAPI এর Layer গুলো

```
┌─────────────────────────────────────────────────┐
│              FastAPI Application                │
├─────────────────────────────────────────────────┤
│  Request → Middleware → Router → Endpoint       │
│                ↓             ↓                  │
│           Auth Check    Dependency              │
│                ↓        Injection               │
│           Rate Limit        ↓                   │
│                         Business Logic          │
│                             ↓                   │
│                    Pydantic Validation          │
│                             ↓                   │
│                      Response Model             │
│                             ↓                   │
│                    JSON Response                │
└─────────────────────────────────────────────────┘
```

### FastAPI এর Key Components

| Component | কাজ | Example |
|-----------|-----|---------|
| **Starlette** | Core ASGI framework | Routing, Middleware, Request/Response |
| **Pydantic** | Data validation & serialization | Request body validation |
| **Uvicorn** | ASGI server | HTTP request serve করে |
| **OpenAPI** | API documentation standard | /docs, /redoc generate করে |
| **Python Type Hints** | Type safety | Editor support, validation |

### Request Life Cycle

```
Browser/Client
     ↓ HTTP Request
  Uvicorn (ASGI Server)
     ↓
  Starlette (Core)
     ↓
  Middleware Stack (Auth, CORS, Logging)
     ↓
  Router (কোন endpoint?)
     ↓
  Dependencies (Injection)
     ↓
  Pydantic Validation (Request Body)
     ↓
  Your Function (Business Logic)
     ↓
  Pydantic Serialization (Response)
     ↓
  JSON Response → Client
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI internally কীভাবে কাজ করে?"

**আদর্শ উত্তর:**
> "FastAPI দুটি main library এর উপর built — Starlette এবং Pydantic। Starlette ASGI-based routing, middleware, WebSocket সব handle করে। Pydantic data validation ও serialization করে। যখন একটি request আসে, Uvicorn সেটি receive করে ASGI application এ পাস করে। তারপর Middleware stack দিয়ে যায় — Auth check, CORS, logging ইত্যাদি। Router সঠিক endpoint খুঁজে বের করে, Dependency Injection resolve হয়, Pydantic request data validate করে, আপনার function run করে, এবং response Pydantic model দিয়ে serialize হয়ে JSON হিসেবে client এ ফেরে।"

---

## ১.৬ FastAPI Install ও Project Structure

### Installation

```bash
# Virtual environment তৈরি (সবসময় করুন!)
python -m venv venv

# Activate করুন
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# FastAPI এবং Uvicorn install
pip install fastapi uvicorn

# Development এ সব dependencies সহ
pip install "fastapi[all]"
# এটি install করে: fastapi, uvicorn, pydantic, python-multipart, email-validator, jinja2 etc.

# requirements.txt তৈরি
pip freeze > requirements.txt
```

### Professional Project Structure

```
my_fastapi_project/
├── app/
│   ├── __init__.py
│   ├── main.py                 ← Application entry point
│   ├── config.py               ← Settings & environment variables
│   │
│   ├── api/
│   │   ├── __init__.py
│   │   ├── deps.py             ← Shared dependencies
│   │   └── v1/
│   │       ├── __init__.py
│   │       ├── router.py       ← All routes collected here
│   │       └── endpoints/
│   │           ├── __init__.py
│   │           ├── users.py    ← User endpoints
│   │           ├── items.py    ← Item endpoints
│   │           └── auth.py     ← Auth endpoints
│   │
│   ├── core/
│   │   ├── __init__.py
│   │   ├── security.py         ← JWT, hashing
│   │   └── config.py           ← App configuration
│   │
│   ├── db/
│   │   ├── __init__.py
│   │   ├── base.py             ← Base DB class
│   │   ├── session.py          ← DB session
│   │   └── models/
│   │       ├── __init__.py
│   │       ├── user.py         ← User DB model
│   │       └── item.py         ← Item DB model
│   │
│   ├── schemas/
│   │   ├── __init__.py
│   │   ├── user.py             ← Pydantic schemas
│   │   └── item.py
│   │
│   └── crud/
│       ├── __init__.py
│       ├── base.py             ← Generic CRUD
│       ├── user.py             ← User CRUD operations
│       └── item.py
│
├── tests/
│   ├── __init__.py
│   ├── conftest.py
│   └── test_users.py
│
├── alembic/                    ← Database migrations
│   └── versions/
│
├── .env                        ← Environment variables (gitignore!)
├── .gitignore
├── requirements.txt
├── alembic.ini
└── README.md
```

### Simple Starter Structure (শুরুর জন্য)

```
simple_project/
├── main.py          ← সব code এখানে (শুরুতে)
├── models.py        ← Pydantic models
├── database.py      ← DB connection
├── requirements.txt
└── .env
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI project কীভাবে structure করবেন?"

**আদর্শ উত্তর:**
> "আমি FastAPI project কে কয়েকটি layer এ structure করি — api layer (routes/endpoints), schemas layer (Pydantic models), crud layer (database operations), db layer (models ও session), core layer (security, config)। এই separation of concerns নিশ্চিত করে যে business logic, database logic, ও API layer আলাদা থাকে। ছোট project এ সব main.py তে রাখা যায়, কিন্তু production project এ modular structure follow করা উচিত।"

### ⚠️ Common Mistakes

- ❌ Virtual environment ছাড়া install করা
- ❌ সব code main.py তে রাখা (বড় project এ)
- ❌ .env file git এ push করা
- ✅ শুরু থেকে clean structure রাখুন

---

## ১.৭ প্রথম API তৈরি

### সবচেয়ে সহজ FastAPI App

```python
# main.py
from fastapi import FastAPI

# FastAPI app instance তৈরি
app = FastAPI(
    title="আমার প্রথম API",
    description="Bangladesh Interview Prep API",
    version="1.0.0"
)

# Root endpoint
@app.get("/")
def read_root():
    return {"message": "স্বাগতম! FastAPI চলছে ✅"}

# Simple GET endpoint
@app.get("/hello/{name}")
def say_hello(name: str):
    return {"message": f"নমস্কার, {name}!"}
```

### Run করা

```bash
# Development mode (auto-reload সহ)
uvicorn main:app --reload

# Custom host ও port
uvicorn main:app --reload --host 0.0.0.0 --port 8000

# Output:
# INFO:     Uvicorn running on http://127.0.0.1:8000
# INFO:     Application startup complete.
```

### Auto-generated Documentation দেখুন

```
http://127.0.0.1:8000/docs      ← Swagger UI (interactive)
http://127.0.0.1:8000/redoc     ← ReDoc (readable)
http://127.0.0.1:8000/openapi.json  ← Raw OpenAPI JSON
```

### FastAPI App এর Lifecycle

```python
from fastapi import FastAPI
from contextlib import asynccontextmanager

# Modern lifespan approach (FastAPI 0.95+)
@asynccontextmanager
async def lifespan(app: FastAPI):
    # Startup: DB connect, cache warm-up
    print("App চালু হচ্ছে... 🚀")
    yield
    # Shutdown: DB disconnect, cleanup
    print("App বন্ধ হচ্ছে... 🛑")

app = FastAPI(lifespan=lifespan)

@app.get("/")
def root():
    return {"status": "running"}
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI তে প্রথম API কীভাবে বানাবেন?"

**আদর্শ উত্তর:**
> "প্রথমে `pip install fastapi uvicorn` দিয়ে install করি। তারপর main.py তে `from fastapi import FastAPI` import করে `app = FastAPI()` দিয়ে instance তৈরি করি। Decorator দিয়ে endpoint define করি — যেমন `@app.get('/')` মানে GET request এলে এই function চলবে। তারপর `uvicorn main:app --reload` দিয়ে server চালু করলে `localhost:8000/docs` এ automatic Swagger UI পাওয়া যায়।"

---

## ১.৮ Path Parameters

**Path Parameters** হলো URL এর অংশ যা dynamic data বহন করে।

### Basic Path Parameter

```python
from fastapi import FastAPI

app = FastAPI()

# {item_id} হলো path parameter
@app.get("/items/{item_id}")
def get_item(item_id: int):
    return {"item_id": item_id, "name": f"Item {item_id}"}

# Call: GET /items/42
# Response: {"item_id": 42, "name": "Item 42"}
```

### Multiple Path Parameters

```python
@app.get("/users/{user_id}/orders/{order_id}")
def get_user_order(user_id: int, order_id: int):
    return {
        "user_id": user_id,
        "order_id": order_id,
        "detail": f"User {user_id} এর Order {order_id}"
    }

# Call: GET /users/5/orders/123
```

### Path Parameter with Enum (Predefined Values)

```python
from enum import Enum
from fastapi import FastAPI

class Category(str, Enum):
    electronics = "electronics"
    clothing = "clothing"
    food = "food"

app = FastAPI()

@app.get("/products/{category}")
def get_products_by_category(category: Category):
    if category == Category.electronics:
        return {"category": category, "items": ["Phone", "Laptop"]}
    elif category == Category.clothing:
        return {"category": category, "items": ["Shirt", "Pants"]}
    return {"category": category, "items": []}

# Call: GET /products/electronics  ✅
# Call: GET /products/invalid      ❌ 422 Validation Error
```

### Path Parameter with Validation

```python
from fastapi import FastAPI, Path

app = FastAPI()

@app.get("/items/{item_id}")
def get_item(
    item_id: int = Path(
        ...,                    # ... মানে required
        title="Item ID",
        description="1 থেকে 1000 এর মধ্যে হতে হবে",
        ge=1,                   # greater than or equal to 1
        le=1000                 # less than or equal to 1000
    )
):
    return {"item_id": item_id}

# Call: GET /items/0    ❌ Validation Error (ge=1 fail)
# Call: GET /items/500  ✅ 
# Call: GET /items/1001 ❌ Validation Error (le=1000 fail)
```

### Order Matters! (গুরুত্বপূর্ণ)

```python
# ⚠️ সতর্কতা: Fixed path আগে রাখুন, dynamic পরে

@app.get("/users/me")       # এটি আগে define করুন
def get_current_user():
    return {"user": "current user"}

@app.get("/users/{user_id}")  # এটি পরে
def get_user(user_id: int):
    return {"user_id": user_id}

# ❌ যদি {user_id} আগে থাকে, /users/me তে গেলে
#    FastAPI "me" কে user_id হিসেবে নিতে চাইবে → int error
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Path parameter এবং Query parameter এর পার্থক্য কী?"

**আদর্শ উত্তর:**
> "Path parameter URL এর অংশ হিসেবে আসে, যেমন `/users/42` তে `42` হলো path parameter। এটি typically resource identify করতে ব্যবহার হয়। Query parameter URL এর `?` এর পরে আসে, যেমন `/items?page=1&limit=10`। Path parameter required, query parameter optional হতে পারে। FastAPI তে curly braces দিয়ে path parameter define করি এবং function argument এর নাম match করাই।"

### ⚠️ Common Mistakes

- ❌ Type annotation না দিলে FastAPI string হিসেবে নেয়, int validation হয় না
- ❌ Fixed path (`/users/me`) এর আগে dynamic path (`/users/{id}`) define করা
- ✅ সবসময় type hint দিন path parameter এ

---

## ১.৯ Query Parameters

**Query Parameters** হলো URL এর `?` এর পরে `key=value` format এ data পাঠানোর পদ্ধতি।

### Basic Query Parameters

```python
from fastapi import FastAPI
from typing import Optional

app = FastAPI()

# name ও age উভয়ই query parameter (path এ নেই কিন্তু function এ আছে)
@app.get("/search")
def search_items(
    keyword: str,              # Required query param
    page: int = 1,             # Optional, default = 1
    limit: int = 10,           # Optional, default = 10
    active: bool = True        # Optional, default = True
):
    return {
        "keyword": keyword,
        "page": page,
        "limit": limit,
        "active": active
    }

# Call: GET /search?keyword=laptop
# → {"keyword": "laptop", "page": 1, "limit": 10, "active": true}

# Call: GET /search?keyword=phone&page=2&limit=5&active=false
# → {"keyword": "phone", "page": 2, "limit": 5, "active": false}
```

### Optional Query Parameter

```python
from typing import Optional

@app.get("/items")
def get_items(
    category: Optional[str] = None,   # Optional — None if not provided
    min_price: Optional[float] = None,
    max_price: Optional[float] = None
):
    filters = {}
    if category:
        filters["category"] = category
    if min_price is not None:
        filters["min_price"] = min_price
    if max_price is not None:
        filters["max_price"] = max_price

    return {"filters": filters, "items": []}

# Call: GET /items                           → filters: {}
# Call: GET /items?category=electronics      → filters: {category: electronics}
# Call: GET /items?min_price=100&max_price=500
```

### Query Parameter Validation

```python
from fastapi import FastAPI, Query

app = FastAPI()

@app.get("/products")
def get_products(
    q: Optional[str] = Query(
        None,
        min_length=3,          # কমপক্ষে ৩ character
        max_length=50,         # সর্বোচ্চ ৫০ character
        title="Search Query",
        description="পণ্য খোঁজার keyword"
    ),
    page: int = Query(1, ge=1),         # minimum 1
    limit: int = Query(10, ge=1, le=100) # 1-100 এর মধ্যে
):
    return {"q": q, "page": page, "limit": limit}

# Call: GET /products?q=ab  ❌ min_length=3 fail
# Call: GET /products?q=laptop&page=2&limit=20  ✅
```

### Multiple Values একই Query Parameter এ

```python
from typing import List

@app.get("/filter")
def filter_items(tags: List[str] = Query([])):
    return {"tags": tags}

# Call: GET /filter?tags=python&tags=fastapi&tags=backend
# → {"tags": ["python", "fastapi", "backend"]}
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI তে pagination কীভাবে implement করবেন?"

**আদর্শ উত্তর:**
> "FastAPI তে pagination query parameters দিয়ে implement করি। `page` এবং `limit` বা `skip` ও `limit` দুটি approach আছে। আমি সাধারণত `skip` ও `limit` পছন্দ করি কারণ database query তে সরাসরি ব্যবহার করা যায়। `skip = (page - 1) * limit` দিয়ে offset বের করা যায়। FastAPI তে Query() দিয়ে default values ও validation add করলে clean API হয়।"

---

## ১.১০ Request Body

**Request Body** হলো POST/PUT/PATCH request এ client থেকে পাঠানো JSON data।

### Basic Request Body

```python
from fastapi import FastAPI
from pydantic import BaseModel

app = FastAPI()

# Pydantic model দিয়ে request body define করুন
class Item(BaseModel):
    name: str
    description: str = None  # Optional field
    price: float
    in_stock: bool = True

@app.post("/items/")
def create_item(item: Item):
    return {
        "message": "Item তৈরি হয়েছে",
        "item": item,
        "total_with_tax": item.price * 1.15
    }

# Request Body (JSON):
# {
#   "name": "Laptop",
#   "price": 75000,
#   "description": "HP Laptop 15 inch"
# }
```

### Request Body + Path + Query একসাথে

```python
@app.put("/items/{item_id}")
def update_item(
    item_id: int,               # Path parameter
    item: Item,                 # Request body
    notify: bool = False        # Query parameter
):
    result = {
        "item_id": item_id,
        "updated_item": item,
        "notification_sent": notify
    }
    return result

# PUT /items/5?notify=true
# Body: {"name": "Updated Laptop", "price": 80000}
```

### Nested Models

```python
from typing import List, Optional
from pydantic import BaseModel

class Address(BaseModel):
    street: str
    city: str
    country: str = "Bangladesh"

class User(BaseModel):
    name: str
    email: str
    age: int
    address: Address          # Nested model
    tags: List[str] = []      # List field

@app.post("/users/")
def create_user(user: User):
    return {"message": "User তৈরি হয়েছে", "user": user}

# Request Body:
# {
#   "name": "Rafi Ahmed",
#   "email": "rafi@example.com",
#   "age": 25,
#   "address": {
#     "street": "Mirpur 10",
#     "city": "Dhaka"
#   },
#   "tags": ["developer", "python"]
# }
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI তে request body কীভাবে handle করেন? Validation কীভাবে হয়?"

**আদর্শ উত্তর:**
> "FastAPI তে Pydantic BaseModel দিয়ে request body define করি। Function parameter এ সেই model এর type annotation দিলে FastAPI automatically JSON parse করে, Pydantic দিয়ে validate করে, এবং model instance তৈরি করে দেয়। Validation fail হলে automatic 422 Unprocessable Entity error সুন্দর error message সহ return হয়। কোনো extra validation code লিখতে হয় না।"

---

## ১.১১ Response Model

**Response Model** দিয়ে API কী return করবে সেটি define করা হয় এবং sensitive data filter করা হয়।

### Basic Response Model

```python
from fastapi import FastAPI
from pydantic import BaseModel
from typing import Optional

app = FastAPI()

class UserCreate(BaseModel):
    name: str
    email: str
    password: str          # Input এ password আছে

class UserResponse(BaseModel):
    id: int
    name: str
    email: str
    # password নেই! Response এ password পাঠাবো না

# response_model দিয়ে বলছি কী return করবে
@app.post("/users/", response_model=UserResponse)
def create_user(user: UserCreate):
    # DB তে save করার পর (simulate করছি)
    new_user = {
        "id": 1,
        "name": user.name,
        "email": user.email,
        "password": user.password  # এটি DB তে আছে কিন্তু response এ আসবে না
    }
    return new_user  # FastAPI UserResponse দিয়ে filter করবে

# Response: {"id": 1, "name": "Rafi", "email": "rafi@x.com"}
# password response এ থাকবে না ✅
```

### Response Model Exclude/Include

```python
from typing import List

class Product(BaseModel):
    id: int
    name: str
    price: float
    cost_price: float      # Internal — response এ দেখাতে চাই না
    is_active: bool

@app.get(
    "/products/{id}",
    response_model=Product,
    response_model_exclude={"cost_price"}  # এই field বাদ দাও
)
def get_product(id: int):
    return {
        "id": id,
        "name": "Laptop",
        "price": 75000,
        "cost_price": 50000,   # Response এ আসবে না
        "is_active": True
    }
```

### List Response

```python
@app.get("/users/", response_model=List[UserResponse])
def get_all_users():
    users = [
        {"id": 1, "name": "Rafi", "email": "rafi@x.com", "password": "hashed"},
        {"id": 2, "name": "Sumaiya", "email": "sumaiya@x.com", "password": "hashed"},
    ]
    return users  # password automatically filter হবে
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Response model কেন ব্যবহার করেন? শুধু `return` করলেই হয় না?"

**আদর্শ উত্তর:**
> "Response model তিনটি কারণে গুরুত্বপূর্ণ। প্রথমত, security — password, internal_notes এর মতো sensitive fields automatically filter হয়, ভুলে include করার risk নেই। দ্বিতীয়ত, documentation — Swagger UI তে এই model দেখিয়ে দেয় API কী return করে। তৃতীয়ত, validation — return data টি model এর সাথে match করছে কিনা check হয়। শুধু return করলে এই তিনটি সুবিধা পাওয়া যায় না।"

---

## ১.১২ Pydantic Basics

**Pydantic** হলো FastAPI এর সবচেয়ে গুরুত্বপূর্ণ dependency। এটি data validation ও serialization করে।

### Pydantic BaseModel

```python
from pydantic import BaseModel, EmailStr, Field
from typing import Optional, List
from datetime import datetime

class Product(BaseModel):
    # Basic fields
    name: str
    price: float
    quantity: int

    # Optional with default
    description: Optional[str] = None
    is_available: bool = True

    # Field with validation
    stock: int = Field(
        ...,                    # Required
        ge=0,                   # >= 0
        le=10000,               # <= 10000
        description="Stock পরিমাণ"
    )

    # Constrained string
    sku: str = Field(..., min_length=3, max_length=20, pattern=r"^[A-Z0-9-]+$")

    # List field
    tags: List[str] = []

    # Datetime
    created_at: datetime = Field(default_factory=datetime.now)
```

### Pydantic Validators

```python
from pydantic import BaseModel, validator, root_validator

class UserRegistration(BaseModel):
    username: str
    email: str
    password: str
    confirm_password: str
    age: int

    # Field-level validator
    @validator("username")
    def username_must_be_alphanumeric(cls, v):
        if not v.isalnum():
            raise ValueError("Username শুধু letters ও numbers দিয়ে হতে হবে")
        return v.lower()   # lowercase এ convert করে return

    @validator("age")
    def age_must_be_adult(cls, v):
        if v < 18:
            raise ValueError("বয়স কমপক্ষে ১৮ হতে হবে")
        return v

    # Root validator (multiple fields এক সাথে)
    @root_validator
    def passwords_match(cls, values):
        pw = values.get("password")
        cpw = values.get("confirm_password")
        if pw and cpw and pw != cpw:
            raise ValueError("Password ও Confirm Password মিলছে না")
        return values
```

### Pydantic Model Config

```python
from pydantic import BaseModel

class Item(BaseModel):
    name: str
    price: float

    class Config:
        # ORM mode — SQLAlchemy model থেকে directly create করা যাবে
        orm_mode = True  # Pydantic v1
        # অথবা Pydantic v2:
        # from_attributes = True

        # JSON এ snake_case → camelCase
        # alias_generator = to_camel

        # Extra fields reject করো
        extra = "forbid"   # "ignore" বা "allow" ও দেওয়া যায়
```

### Pydantic v1 vs v2 পার্থক্য

| Feature | Pydantic v1 | Pydantic v2 |
|---------|-------------|-------------|
| `orm_mode` | `orm_mode = True` | `from_attributes = True` |
| Validator | `@validator` | `@field_validator` |
| Root validator | `@root_validator` | `@model_validator` |
| Performance | Normal | ~5-50x faster |
| Import | `from pydantic import ...` | same |

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Pydantic কী করে? কেন FastAPI তে এটি গুরুত্বপূর্ণ?"

**আদর্শ উত্তর:**
> "Pydantic হলো Python এর data validation library। FastAPI এটি ব্যবহার করে request/response data validate ও serialize করতে। আমি Pydantic BaseModel দিয়ে data schema define করি — কোন field কোন type, কোনটি required/optional, validation rules কী। যখন request আসে, Pydantic automatically JSON কে Python object এ convert করে এবং validate করে। Validation fail হলে সুন্দর error message দেয়। ORM mode enable করলে SQLAlchemy model থেকে সরাসরি Pydantic object তৈরি হয়।"

---

## ১.১৩ Type Hints

**Type Hints** হলো Python এর একটি feature যা variable ও function এর type explicitly declare করতে দেয়। FastAPI এর সব কিছু এর উপর নির্মিত।

### Python Type Hints Basics

```python
# Variable type hints
name: str = "Rafi"
age: int = 25
price: float = 99.99
is_active: bool = True

# Function type hints
def greet(name: str, age: int) -> str:
    return f"নমস্কার {name}, আপনার বয়স {age}"

# Return type hint
def add(a: int, b: int) -> int:
    return a + b
```

### Complex Type Hints (FastAPI তে বেশি ব্যবহার)

```python
from typing import Optional, List, Dict, Tuple, Union, Any
from datetime import datetime, date

# Optional — None অথবা নির্দিষ্ট type
name: Optional[str] = None

# List
tags: List[str] = []
prices: List[float] = [10.5, 20.0]

# Dict
metadata: Dict[str, Any] = {}

# Union — একাধিক type এর যেকোনো একটি
id_or_name: Union[int, str]   # Python 3.10+: int | str

# Tuple
coordinates: Tuple[float, float] = (23.8, 90.4)

# Nested types
users: List[Dict[str, Any]] = [{"name": "Rafi", "age": 25}]
```

### FastAPI তে Type Hints এর ভূমিকা

```python
from fastapi import FastAPI
from pydantic import BaseModel
from typing import Optional, List

app = FastAPI()

class Item(BaseModel):
    name: str                      # Required string
    price: float                   # Required float
    description: Optional[str] = None  # Optional string
    tags: List[str] = []           # List of strings

# Type hints দিয়ে FastAPI জানে:
# 1. item_id → URL থেকে int হিসেবে নাও (path param)
# 2. q → Query string থেকে নাও, optional (query param)
# 3. item → Request body থেকে parse করো (body)
@app.get("/items/{item_id}")
def get_item(
    item_id: int,
    q: Optional[str] = None
) -> dict:
    result = {"item_id": item_id}
    if q:
        result["q"] = q
    return result
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Type hints কী? FastAPI তে এটি কেন জরুরি?"

**আদর্শ উত্তর:**
> "Type hints হলো Python এ variable ও function এর data type explicitly declare করার syntax। এটি runtime এ enforce করে না, কিন্তু FastAPI এটি runtime এ ব্যবহার করে। Type hint দেখে FastAPI বুঝতে পারে কোন parameter path থেকে আসবে, কোনটি query string থেকে, কোনটি request body থেকে। Pydantic type hint দেখে validation করে। Editor ভালো autocomplete দেয়। Type hints ছাড়া FastAPI এর automatic validation ও documentation সম্ভব হতো না।"

---

## ১.১৪ Validation

FastAPI + Pydantic এর সবচেয়ে শক্তিশালী feature হলো automatic validation।

### Built-in Validation Types

```python
from fastapi import FastAPI, Query, Path, Body
from pydantic import BaseModel, Field
from typing import Optional

app = FastAPI()

# ─── String Validation ───────────────────────────────
class ProductSchema(BaseModel):
    name: str = Field(
        ...,
        min_length=2,          # কমপক্ষে ২ character
        max_length=100,        # সর্বোচ্চ ১০০ character
        pattern=r"^[a-zA-Z\s]+$"  # Regex: শুধু letters ও spaces
    )
    sku: str = Field(..., min_length=3, max_length=20)
    
    # ─── Numeric Validation ─────────────────────────
    price: float = Field(..., gt=0, le=1_000_000)  # 0 < price <= 1,000,000
    stock: int = Field(0, ge=0)           # stock >= 0
    discount: float = Field(0, ge=0, le=100)  # 0-100%
    
    # ─── Email Validation ───────────────────────────
    # pip install "pydantic[email]" দরকার
    # contact_email: EmailStr = None

# ─── Path Parameter Validation ───────────────────────
@app.get("/products/{product_id}")
def get_product(
    product_id: int = Path(..., ge=1, title="Product ID")
):
    return {"product_id": product_id}

# ─── Query Parameter Validation ──────────────────────
@app.get("/search")
def search(
    q: Optional[str] = Query(None, min_length=2, max_length=50),
    page: int = Query(1, ge=1),
    limit: int = Query(10, ge=1, le=100)
):
    return {"q": q, "page": page, "limit": limit}
```

### Custom Validator দিয়ে Business Logic Validation

```python
from pydantic import BaseModel, validator
from datetime import date

class BookingRequest(BaseModel):
    check_in: date
    check_out: date
    guests: int
    room_type: str

    @validator("guests")
    def guests_must_be_positive(cls, v):
        if v <= 0:
            raise ValueError("Guest সংখ্যা কমপক্ষে ১ হতে হবে")
        if v > 10:
            raise ValueError("Guest সংখ্যা ১০ এর বেশি হবে না")
        return v

    @validator("check_out")
    def checkout_after_checkin(cls, v, values):
        if "check_in" in values and v <= values["check_in"]:
            raise ValueError("Check-out তারিখ Check-in তারিখের পরে হতে হবে")
        return v

    @validator("room_type")
    def valid_room_type(cls, v):
        allowed = ["single", "double", "suite", "deluxe"]
        if v.lower() not in allowed:
            raise ValueError(f"Room type হতে হবে: {', '.join(allowed)}")
        return v.lower()
```

### Validation Error Response Format

```json
{
  "detail": [
    {
      "loc": ["body", "price"],
      "msg": "ensure this value is greater than 0",
      "type": "value_error.number.not_gt",
      "ctx": {"limit_value": 0}
    },
    {
      "loc": ["body", "name"],
      "msg": "field required",
      "type": "value_error.missing"
    }
  ]
}
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI তে কীভাবে input validation করেন? Custom validation কীভাবে add করবেন?"

**আদর্শ উত্তর:**
> "FastAPI তে validation দুটি level এ হয়। প্রথম level হলো Pydantic built-in validation — Field() দিয়ে min_length, max_length, ge, le, regex ইত্যাদি define করা যায়। দ্বিতীয় level হলো custom validator — Pydantic এর @validator decorator দিয়ে business logic validation করা যায়। যেমন check-out তারিখ check-in এর পরে হতে হবে এই validation শুধু custom validator দিয়ে করা যায়। Validation fail হলে FastAPI automatically 422 status code সহ field-level error message return করে।"

### ⚠️ Common Mistakes

- ❌ Validation logic controller function এ লেখা
- ❌ Optional field এ None check না করা
- ❌ `int` type এ string pass করলে error হবে — 422, 500 নয়
- ✅ Pydantic model এ validation রাখুন — DRY principle

---

## ১.১৫ PART 1 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: FastAPI কী এবং এটি কোন framework এর উপর built?**

> FastAPI হলো modern Python web framework যা REST API তৈরির জন্য ব্যবহৃত হয়। এটি **Starlette** (ASGI framework, routing/middleware) এবং **Pydantic** (data validation/serialization) এর উপর built। Production এ **Uvicorn** ASGI server দিয়ে run করা হয়।

---

**Q2: FastAPI এর automatic documentation কীভাবে কাজ করে?**

> FastAPI Python এর type hints ও Pydantic models থেকে **OpenAPI specification** generate করে। সেই specification থেকে `/docs` এ **Swagger UI** এবং `/redoc` এ **ReDoc** interface serve করে। এই documentation সবসময় code এর সাথে synchronized থাকে কারণ এটি code থেকেই generate হয়।

---

**Q3: ASGI ও WSGI এর পার্থক্য কী?**

> WSGI (Web Server Gateway Interface) synchronous standard — একবারে একটি request। ASGI (Asynchronous Server Gateway Interface) async standard — concurrent requests, WebSocket, HTTP/2 support করে। FastAPI ASGI-based, তাই `async def` দিয়ে concurrent I/O operations efficiently handle করা যায়।

---

**Q4: Pydantic এর `orm_mode` (বা v2 তে `from_attributes`) কী কাজ করে?**

> সাধারণত Pydantic model শুধু dict/JSON থেকে তৈরি হয়। `orm_mode = True` দিলে SQLAlchemy ORM object থেকেও Pydantic model তৈরি করা যায়। DB query করে SQLAlchemy model পেলে সেটি সরাসরি response model এ convert করা যায়।

---

**Q5: Path parameter ও Query parameter এর পার্থক্য উদাহরণসহ বলুন।**

> Path parameter URL structure এর অংশ: `/users/{user_id}` — resource identify করে। Query parameter URL এর `?` এর পরে: `/users?page=1&limit=10` — filtering, pagination এ ব্যবহার হয়। Path parameter সবসময় required, query parameter optional default value সহ থাকতে পারে।

---

**Q6: `response_model` ব্যবহার না করলে কী সমস্যা হতে পারে?**

> Response model ছাড়া return করা সব data client এ যাবে — password, internal fields, sensitive data সহ। Security risk তৈরি হয়। এছাড়া Swagger documentation তে response schema দেখাবে না। Response model দিলে automatic filtering, documentation, ও response validation হয়।

---

**Q7: FastAPI তে required এবং optional field কীভাবে define করবেন?**

```python
from pydantic import BaseModel, Field
from typing import Optional

class Item(BaseModel):
    name: str                    # Required — default নেই
    price: float                 # Required
    description: Optional[str] = None  # Optional — None default
    tax: float = 0.0             # Optional — 0.0 default
    stock: int = Field(..., ge=0)  # Required, ... মানে required
```

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|--------|-------|
| FastAPI কে তৈরি করেন? | Sebastián Ramírez (tiangolo) |
| FastAPI documentation কোথায় পাওয়া যায়? | `/docs` (Swagger) ও `/redoc` |
| Pydantic কী? | Data validation ও serialization library |
| ASGI server এর উদাহরণ? | Uvicorn, Hypercorn, Daphne |
| `ge` মানে কী Field() এ? | Greater than or equal (≥) |
| `le` মানে কী? | Less than or equal (≤) |
| Path param কীভাবে define করেন? | URL এ `{param_name}` |
| Query param কীভাবে optional করবেন? | `= None` বা `= Query(None)` |
| 422 status code মানে কী? | Unprocessable Entity — validation error |
| `async def` vs `def` FastAPI তে? | async = non-blocking, def = blocking |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part2"></a>

# PART 2: Routing & API Development

> **📍 এই PART এর Sections:** [২.১](#২১-apirouter) · [২.২](#২২-modular-routing) · [২.৩](#২৩-crud-apis-তৈরি) · [২.৪](#২৪-http-methods-বিস্তারিত) · [২.৫](#২৫-status-codes) · [২.৬](#২৬-response-handling) · [২.৭](#২৭-file-upload) · [২.৮](#২৮-form-data) · [২.৯](#২৯-header-handling) · [২.১০](#২১০-cookie-handling) · [২.১১](#২১১-dependency-injection) · [২.১২](#২১২-middleware) · [২.১৩](#২১৩-background-tasks) · [২.১৪](#২১৪-part-2--interview-questions--answers)

---

## ২.১ APIRouter

**APIRouter** হলো FastAPI এর routing system। এটি দিয়ে related endpoints কে আলাদা module এ রাখা যায় এবং main app এ include করা যায়।

### 🏠 বাস্তব জীবনের উদাহরণ

একটি বড় অফিস ভবন কল্পনা করুন:
- **Main App** = ভবনের Reception (সব কিছু এখানে সংযুক্ত)
- **APIRouter** = আলাদা আলাদা Department (HR, Finance, Engineering)
- প্রতিটি Department এর নিজস্ব rules ও team আছে
- Reception শুধু কোন Department এ যেতে হবে সেটি জানে

### Basic APIRouter

```python
# routers/users.py
from fastapi import APIRouter

# Router তৈরি
router = APIRouter(
    prefix="/users",        # সব endpoint এ /users prefix যোগ হবে
    tags=["Users"],         # Swagger তে grouping এর জন্য
    responses={
        404: {"description": "User পাওয়া যায়নি"}
    }
)

@router.get("/")            # আসলে: GET /users/
def get_users():
    return [{"id": 1, "name": "Rafi"}, {"id": 2, "name": "Sumaiya"}]

@router.get("/{user_id}")   # আসলে: GET /users/{user_id}
def get_user(user_id: int):
    return {"id": user_id, "name": "Rafi Ahmed"}

@router.post("/")           # আসলে: POST /users/
def create_user(name: str):
    return {"id": 3, "name": name}
```

```python
# routers/items.py
from fastapi import APIRouter

router = APIRouter(prefix="/items", tags=["Items"])

@router.get("/")
def get_items():
    return [{"id": 1, "name": "Laptop"}]
```

```python
# main.py
from fastapi import FastAPI
from routers import users, items

app = FastAPI()

# Router include করুন
app.include_router(users.router)
app.include_router(items.router)

# Result:
# GET /users/          → users router
# GET /users/{id}      → users router
# GET /items/          → items router
```

### Router এ Dependencies যোগ করা

```python
from fastapi import APIRouter, Depends
from .deps import get_current_user  # Auth dependency

# এই router এর সব endpoint এ auth check হবে
protected_router = APIRouter(
    prefix="/admin",
    tags=["Admin"],
    dependencies=[Depends(get_current_user)]  # সব endpoint এ apply
)

@protected_router.get("/dashboard")
def admin_dashboard():
    return {"data": "Admin only content"}
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "APIRouter কেন ব্যবহার করবেন? সব endpoint main.py তে রাখলে কী সমস্যা?"

**আদর্শ উত্তর:**
> "APIRouter ব্যবহার করি code কে modular রাখতে। বড় project এ সব endpoint main.py তে রাখলে file হাজার লাইনের হয়ে যায়, team এ কাজ করা কঠিন হয়, এবং specific feature খুঁজে পেতে সমস্যা হয়। APIRouter দিয়ে user endpoints, product endpoints, auth endpoints আলাদা file এ রাখি, prefix ও tags দিয়ে organize করি। Router level এ dependencies দিলে সব endpoint automatically সেই dependency পায় — যেমন auth check।"

---

## ২.২ Modular Routing

Professional project এ routing এর সঠিক structure কীভাবে রাখবেন।

### Complete Modular Structure

```
app/
├── main.py
└── api/
    └── v1/
        ├── __init__.py
        ├── router.py        ← সব routes collect করে
        └── endpoints/
            ├── __init__.py
            ├── users.py
            ├── products.py
            └── auth.py
```

```python
# app/api/v1/endpoints/users.py
from fastapi import APIRouter, HTTPException, status
from typing import List
from app.schemas.user import UserCreate, UserResponse

router = APIRouter()

# In-memory fake DB (বাস্তবে SQLAlchemy ব্যবহার করবেন)
fake_db: List[dict] = []

@router.get("/", response_model=List[UserResponse])
def list_users():
    return fake_db

@router.post("/", response_model=UserResponse, status_code=status.HTTP_201_CREATED)
def create_user(user: UserCreate):
    new_user = {"id": len(fake_db) + 1, **user.dict()}
    fake_db.append(new_user)
    return new_user

@router.get("/{user_id}", response_model=UserResponse)
def get_user(user_id: int):
    user = next((u for u in fake_db if u["id"] == user_id), None)
    if not user:
        raise HTTPException(
            status_code=status.HTTP_404_NOT_FOUND,
            detail=f"User {user_id} পাওয়া যায়নি"
        )
    return user
```

```python
# app/api/v1/router.py
from fastapi import APIRouter
from app.api.v1.endpoints import users, products, auth

api_router = APIRouter()

api_router.include_router(auth.router, prefix="/auth", tags=["Authentication"])
api_router.include_router(users.router, prefix="/users", tags=["Users"])
api_router.include_router(products.router, prefix="/products", tags=["Products"])
```

```python
# app/main.py
from fastapi import FastAPI
from app.api.v1.router import api_router

app = FastAPI(title="My API", version="1.0.0")

# All v1 routes under /api/v1/
app.include_router(api_router, prefix="/api/v1")

# Result:
# POST /api/v1/auth/login
# GET  /api/v1/users/
# POST /api/v1/users/
# GET  /api/v1/products/
```

### API Versioning Strategy

```python
# main.py
from fastapi import FastAPI
from app.api.v1.router import api_router as v1_router
from app.api.v2.router import api_router as v2_router

app = FastAPI()

app.include_router(v1_router, prefix="/api/v1")
app.include_router(v2_router, prefix="/api/v2")

# Clients use /api/v1 (old) বা /api/v2 (new)
# Breaking changes এলে নতুন version তৈরি করুন
```

---

## ২.৩ CRUD APIs তৈরি

**CRUD** = **C**reate, **R**ead, **U**pdate, **D**elete — এটি সব backend API এর মূল।

### Complete CRUD Implementation

```python
# schemas/product.py
from pydantic import BaseModel, Field
from typing import Optional
from datetime import datetime

class ProductBase(BaseModel):
    name: str = Field(..., min_length=2, max_length=100)
    description: Optional[str] = None
    price: float = Field(..., gt=0)
    stock: int = Field(0, ge=0)

class ProductCreate(ProductBase):
    pass  # Create এ extra field নেই

class ProductUpdate(BaseModel):
    # Update এ সব field optional (partial update)
    name: Optional[str] = None
    description: Optional[str] = None
    price: Optional[float] = None
    stock: Optional[int] = None

class ProductResponse(ProductBase):
    id: int
    created_at: datetime
    updated_at: Optional[datetime] = None

    class Config:
        orm_mode = True
```

```python
# api/endpoints/products.py
from fastapi import APIRouter, HTTPException, status
from typing import List, Optional
from datetime import datetime
from schemas.product import ProductCreate, ProductUpdate, ProductResponse

router = APIRouter()

# In-memory storage (বাস্তবে DB ব্যবহার করবেন)
products_db: dict = {}
counter = 0

# ─── CREATE ─────────────────────────────────────────
@router.post(
    "/",
    response_model=ProductResponse,
    status_code=status.HTTP_201_CREATED,
    summary="নতুন Product তৈরি করুন"
)
def create_product(product: ProductCreate):
    global counter
    counter += 1
    new_product = {
        "id": counter,
        "created_at": datetime.now(),
        "updated_at": None,
        **product.dict()
    }
    products_db[counter] = new_product
    return new_product

# ─── READ ALL ───────────────────────────────────────
@router.get(
    "/",
    response_model=List[ProductResponse],
    summary="সব Product এর তালিকা"
)
def list_products(
    skip: int = 0,
    limit: int = 10,
    search: Optional[str] = None
):
    items = list(products_db.values())

    # Search filter
    if search:
        items = [p for p in items if search.lower() in p["name"].lower()]

    # Pagination
    return items[skip: skip + limit]

# ─── READ ONE ───────────────────────────────────────
@router.get(
    "/{product_id}",
    response_model=ProductResponse,
    summary="নির্দিষ্ট Product এর তথ্য"
)
def get_product(product_id: int):
    product = products_db.get(product_id)
    if not product:
        raise HTTPException(
            status_code=status.HTTP_404_NOT_FOUND,
            detail=f"Product ID {product_id} পাওয়া যায়নি"
        )
    return product

# ─── UPDATE (Full) ──────────────────────────────────
@router.put(
    "/{product_id}",
    response_model=ProductResponse,
    summary="Product সম্পূর্ণ Update করুন"
)
def update_product(product_id: int, product: ProductCreate):
    if product_id not in products_db:
        raise HTTPException(status_code=404, detail="Product পাওয়া যায়নি")

    products_db[product_id].update({
        **product.dict(),
        "updated_at": datetime.now()
    })
    return products_db[product_id]

# ─── PARTIAL UPDATE ─────────────────────────────────
@router.patch(
    "/{product_id}",
    response_model=ProductResponse,
    summary="Product আংশিক Update করুন"
)
def partial_update_product(product_id: int, product: ProductUpdate):
    if product_id not in products_db:
        raise HTTPException(status_code=404, detail="Product পাওয়া যায়নি")

    # শুধু পাঠানো fields update করুন (None বাদ)
    update_data = product.dict(exclude_unset=True)
    products_db[product_id].update({
        **update_data,
        "updated_at": datetime.now()
    })
    return products_db[product_id]

# ─── DELETE ─────────────────────────────────────────
@router.delete(
    "/{product_id}",
    status_code=status.HTTP_204_NO_CONTENT,
    summary="Product Delete করুন"
)
def delete_product(product_id: int):
    if product_id not in products_db:
        raise HTTPException(status_code=404, detail="Product পাওয়া যায়নি")
    del products_db[product_id]
    # 204 No Content — response body নেই
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "PUT ও PATCH এর পার্থক্য কী?"

**আদর্শ উত্তর:**
> "PUT মানে full replacement — পুরো resource টি নতুন data দিয়ে replace করা হয়। পাঠানো নতুন data তে যা নেই সেটি reset হয় বা error হয়। PATCH মানে partial update — শুধু পাঠানো fields update হয়, বাকিগুলো অপরিবর্তিত থাকে। FastAPI তে PATCH এর জন্য সব field Optional করা model ব্যবহার করি এবং `exclude_unset=True` দিয়ে শুধু client এর পাঠানো fields নিই।"

---

## ২.৪ HTTP Methods বিস্তারিত

| Method | Decorator | কাজ | Idempotent? | Body? |
|--------|-----------|-----|-------------|-------|
| **GET** | `@app.get()` | Data পড়া | ✅ হ্যাঁ | ❌ না |
| **POST** | `@app.post()` | নতুন resource তৈরি | ❌ না | ✅ হ্যাঁ |
| **PUT** | `@app.put()` | Resource সম্পূর্ণ replace | ✅ হ্যাঁ | ✅ হ্যাঁ |
| **PATCH** | `@app.patch()` | Resource আংশিক update | ⚠️ পরিস্থিতি ভেদে | ✅ হ্যাঁ |
| **DELETE** | `@app.delete()` | Resource মুছে ফেলা | ✅ হ্যাঁ | ❌ সাধারণত না |
| **OPTIONS** | `@app.options()` | CORS preflight | ✅ হ্যাঁ | ❌ না |
| **HEAD** | `@app.head()` | GET এর মতো, body ছাড়া | ✅ হ্যাঁ | ❌ না |

### Idempotent মানে কী?

```
Idempotent = একই request বারবার করলে একই result পাওয়া যায়

GET /users/1      → বারবার করলেও same user ফেরে  ✅ Idempotent
DELETE /users/1   → প্রথমবার delete হয়, পরেরবার 404  ✅ Idempotent (result same)
PUT /users/1 {...} → বারবার করলেও same state  ✅ Idempotent
POST /users {...}  → প্রতিবার নতুন user তৈরি হয়  ❌ NOT Idempotent
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "POST ও PUT এর পার্থক্য কী?"

**আদর্শ উত্তর:**
> "POST ব্যবহার হয় নতুন resource তৈরিতে। Server resource এর ID assign করে, তাই same request পাঠালে দুটি resource তৈরি হয় — not idempotent। PUT ব্যবহার হয় existing resource replace করতে, client ID জানে এবং পাঠায়। Same PUT request বারবার করলে result same থাকে — idempotent। REST convention অনুযায়ী `POST /users` নতুন user, `PUT /users/5` user 5 কে replace করে।"

---

## ২.৫ Status Codes

HTTP status codes সঠিকভাবে ব্যবহার করা professional API এর চিহ্ন।

### Status Code চার্ট

| Range | মানে | উদাহরণ |
|-------|------|---------|
| **2xx** | ✅ Success | 200 OK, 201 Created, 204 No Content |
| **3xx** | ↩️ Redirect | 301 Moved, 302 Found |
| **4xx** | ❌ Client Error | 400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not Found, 422 Unprocessable |
| **5xx** | 💥 Server Error | 500 Internal Server Error, 503 Service Unavailable |

### FastAPI তে Status Codes

```python
from fastapi import FastAPI, HTTPException, status
from fastapi.responses import JSONResponse

app = FastAPI()

# সাধারণ status codes
@app.post("/items/", status_code=status.HTTP_201_CREATED)
def create_item(name: str):
    return {"name": name}

# 204 No Content (delete এ)
@app.delete("/items/{id}", status_code=status.HTTP_204_NO_CONTENT)
def delete_item(id: int):
    pass  # body নেই

# Custom error response
@app.get("/users/{user_id}")
def get_user(user_id: int):
    if user_id == 0:
        raise HTTPException(
            status_code=status.HTTP_400_BAD_REQUEST,
            detail="User ID 0 valid নয়"
        )
    if user_id > 1000:
        raise HTTPException(
            status_code=status.HTTP_404_NOT_FOUND,
            detail={"message": "User পাওয়া যায়নি", "user_id": user_id}
        )
    return {"user_id": user_id}
```

### সঠিক Status Code ব্যবহারের Guide

```
GET request:
  ✅ পাওয়া গেছে → 200 OK
  ❌ পাওয়া যায়নি → 404 Not Found

POST request:
  ✅ তৈরি হয়েছে → 201 Created
  ❌ Invalid data → 422 Unprocessable Entity
  ❌ Already exists → 409 Conflict

PUT/PATCH:
  ✅ Updated → 200 OK
  ❌ Not found → 404 Not Found

DELETE:
  ✅ Deleted → 204 No Content
  ❌ Not found → 404 Not Found

Auth:
  ❌ Not logged in → 401 Unauthorized
  ❌ No permission → 403 Forbidden
```

---

## ২.৬ Response Handling

FastAPI তে response বিভিন্নভাবে customize করা যায়।

### Response Types

```python
from fastapi import FastAPI
from fastapi.responses import (
    JSONResponse,
    HTMLResponse,
    PlainTextResponse,
    RedirectResponse,
    FileResponse,
    StreamingResponse
)

app = FastAPI()

# JSON Response (default)
@app.get("/json")
def json_response():
    return {"message": "Hello"}  # automatically JSONResponse

# HTML Response
@app.get("/html", response_class=HTMLResponse)
def html_response():
    return "<h1>নমস্কার!</h1>"

# Plain Text
@app.get("/text", response_class=PlainTextResponse)
def text_response():
    return "Hello World"

# Redirect
@app.get("/old-url")
def redirect():
    return RedirectResponse(url="/new-url", status_code=301)

# Custom Headers সহ Response
@app.get("/custom")
def custom_response():
    return JSONResponse(
        content={"message": "Custom"},
        status_code=200,
        headers={"X-Custom-Header": "my-value"}
    )
```

### Custom Exception Handler

```python
from fastapi import FastAPI, Request
from fastapi.responses import JSONResponse

app = FastAPI()

# Custom exception class
class ItemNotFoundError(Exception):
    def __init__(self, item_id: int):
        self.item_id = item_id

# Exception handler register
@app.exception_handler(ItemNotFoundError)
async def item_not_found_handler(request: Request, exc: ItemNotFoundError):
    return JSONResponse(
        status_code=404,
        content={
            "error": "Item Not Found",
            "message": f"Item {exc.item_id} পাওয়া যায়নি",
            "path": str(request.url)
        }
    )

@app.get("/items/{item_id}")
def get_item(item_id: int):
    if item_id not in [1, 2, 3]:
        raise ItemNotFoundError(item_id=item_id)
    return {"item_id": item_id}
```

---

## ২.৭ File Upload

### Single File Upload

```python
from fastapi import FastAPI, UploadFile, File, HTTPException
import shutil
import os

app = FastAPI()

UPLOAD_DIR = "uploads"
os.makedirs(UPLOAD_DIR, exist_ok=True)

@app.post("/upload/")
async def upload_file(file: UploadFile = File(...)):
    # File info
    print(f"Filename: {file.filename}")
    print(f"Content-Type: {file.content_type}")
    print(f"Size: {file.size} bytes")

    # File type validation
    allowed_types = ["image/jpeg", "image/png", "image/gif", "application/pdf"]
    if file.content_type not in allowed_types:
        raise HTTPException(
            status_code=400,
            detail=f"শুধু {', '.join(allowed_types)} allowed"
        )

    # Size limit: 5MB
    if file.size > 5 * 1024 * 1024:
        raise HTTPException(status_code=400, detail="File size 5MB এর বেশি হবে না")

    # Save to disk
    file_path = os.path.join(UPLOAD_DIR, file.filename)
    with open(file_path, "wb") as buffer:
        shutil.copyfileobj(file.file, buffer)

    return {
        "filename": file.filename,
        "content_type": file.content_type,
        "size": file.size,
        "saved_path": file_path
    }
```

### Multiple File Upload

```python
from typing import List

@app.post("/upload/multiple/")
async def upload_multiple_files(files: List[UploadFile] = File(...)):
    results = []
    for file in files:
        file_path = os.path.join(UPLOAD_DIR, file.filename)
        with open(file_path, "wb") as buffer:
            shutil.copyfileobj(file.file, buffer)
        results.append({
            "filename": file.filename,
            "size": file.size
        })
    return {"uploaded_files": results, "count": len(results)}
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "FastAPI তে file upload কীভাবে করবেন? `File` ও `UploadFile` এর পার্থক্য কী?"

**আদর্শ উত্তর:**
> "FastAPI তে `UploadFile` দিয়ে file upload handle করি। `File(...)` মানে required, `File(None)` মানে optional। `UploadFile` এর `filename`, `content_type`, `size` attributes আছে এবং `file.read()` বা `shutil.copyfileobj()` দিয়ে content পড়া যায়। `UploadFile` async streaming support করে তাই বড় file এও memory issue হয় না। `bytes` type দিলে পুরো file memory তে লোড হয়, `UploadFile` দিলে streaming হয়।"

---

## ২.৮ Form Data

```python
from fastapi import FastAPI, Form
from typing import Optional

app = FastAPI()

# pip install python-multipart  ← দরকার!

@app.post("/login/")
def login(
    username: str = Form(...),
    password: str = Form(...)
):
    # HTML form এ বা Postman এ form-data দিয়ে পাঠান
    if username == "admin" and password == "secret":
        return {"status": "logged in", "user": username}
    return {"status": "invalid credentials"}

# Form + File একসাথে
@app.post("/profile/")
async def update_profile(
    name: str = Form(...),
    bio: Optional[str] = Form(None),
    avatar: UploadFile = File(None)
):
    result = {"name": name, "bio": bio}
    if avatar:
        result["avatar"] = avatar.filename
    return result
```

### ⚠️ গুরুত্বপূর্ণ: Form + JSON একসাথে নয়

```python
# ❌ এটি কাজ করবে না — Form ও JSON body একসাথে না
@app.post("/wrong/")
def wrong_endpoint(
    name: str = Form(...),
    item: Item = Body(...)  # এটি Form এর সাথে কাজ করে না
):
    pass

# ✅ সঠিক: Form ও File, অথবা শুধু JSON
```

---

## ২.৯ Header Handling

```python
from fastapi import FastAPI, Header
from typing import Optional

app = FastAPI()

@app.get("/items/")
def get_items(
    user_agent: Optional[str] = Header(None),     # User-Agent header
    accept_language: Optional[str] = Header(None), # Accept-Language header
    x_token: Optional[str] = Header(None)          # Custom X-Token header
):
    return {
        "User-Agent": user_agent,
        "Language": accept_language,
        "Token": x_token
    }

# Note: FastAPI automatically converts header names
# user_agent → User-Agent (underscore to hyphen)
# x_token → X-Token
```

### Custom Request Header Validation

```python
@app.get("/secure/")
def secure_endpoint(x_api_key: str = Header(...)):
    # Header: X-Api-Key: my-secret-key
    if x_api_key != "my-secret-key":
        raise HTTPException(
            status_code=401,
            detail="Invalid API Key"
        )
    return {"access": "granted"}
```

---

## ২.১০ Cookie Handling

```python
from fastapi import FastAPI, Cookie, Response
from typing import Optional

app = FastAPI()

# Cookie পড়া
@app.get("/profile/")
def get_profile(session_id: Optional[str] = Cookie(None)):
    if not session_id:
        return {"status": "not logged in"}
    return {"status": "logged in", "session": session_id}

# Cookie set করা
@app.post("/login/")
def login(response: Response, username: str, password: str):
    if username == "admin" and password == "secret":
        # Cookie set
        response.set_cookie(
            key="session_id",
            value="abc123xyz",
            httponly=True,      # JavaScript access block
            secure=True,        # HTTPS only
            samesite="lax",     # CSRF protection
            max_age=3600        # 1 ঘন্টা
        )
        return {"status": "logged in"}
    raise HTTPException(status_code=401, detail="Invalid credentials")

# Cookie delete করা
@app.post("/logout/")
def logout(response: Response):
    response.delete_cookie("session_id")
    return {"status": "logged out"}
```

---

## ২.১১ Dependency Injection

**Dependency Injection (DI)** হলো FastAPI এর সবচেয়ে শক্তিশালী feature। এটি code reuse ও separation of concerns নিশ্চিত করে।

### 🏠 বাস্তব জীবনের উদাহরণ

একটি **রেস্তোরাঁ** এর কথা ভাবুন:
- প্রতিটি waiter (endpoint) কে নিজে থেকে চাবি নিয়ে store room খুলতে হয় না
- Manager (Dependency) চাবি manage করে
- Waiter শুধু Manager কে বলে "আমার এটা দরকার" (`Depends(get_db)`)
- Manager সেটি দিয়ে দেয়

### Basic Dependency

```python
from fastapi import FastAPI, Depends
from typing import Optional

app = FastAPI()

# Simple dependency function
def get_query_params(
    skip: int = 0,
    limit: int = 10,
    search: Optional[str] = None
):
    return {"skip": skip, "limit": limit, "search": search}

# Dependency ব্যবহার
@app.get("/items/")
def get_items(params: dict = Depends(get_query_params)):
    return {"params": params, "items": []}

@app.get("/users/")
def get_users(params: dict = Depends(get_query_params)):
    return {"params": params, "users": []}
# একই pagination logic দুই জায়গায় reuse হচ্ছে ✅
```

### Database Session Dependency

```python
from fastapi import Depends
from sqlalchemy.orm import Session
from database import SessionLocal

# DB session dependency
def get_db():
    db = SessionLocal()
    try:
        yield db          # endpoint এ db পাস করে
    finally:
        db.close()        # request শেষে automatically close

@app.get("/users/")
def get_users(db: Session = Depends(get_db)):
    # db automatically manage হয়
    users = db.query(User).all()
    return users
```

### Authentication Dependency

```python
from fastapi import Depends, HTTPException, status
from fastapi.security import HTTPBearer, HTTPAuthorizationCredentials
import jwt

security = HTTPBearer()

def get_current_user(credentials: HTTPAuthorizationCredentials = Depends(security)):
    token = credentials.credentials
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=["HS256"])
        user_id = payload.get("sub")
        return {"user_id": user_id}
    except jwt.ExpiredSignatureError:
        raise HTTPException(status_code=401, detail="Token expired")
    except jwt.JWTError:
        raise HTTPException(status_code=401, detail="Invalid token")

# Protected endpoint
@app.get("/me/")
def get_profile(current_user: dict = Depends(get_current_user)):
    return current_user

# Admin only dependency
def require_admin(current_user: dict = Depends(get_current_user)):
    if current_user.get("role") != "admin":
        raise HTTPException(status_code=403, detail="Admin access required")
    return current_user

@app.delete("/users/{id}")
def delete_user(id: int, admin: dict = Depends(require_admin)):
    return {"deleted": id}
```

### Class-based Dependency

```python
class PaginationParams:
    def __init__(
        self,
        page: int = 1,
        size: int = 10,
        sort_by: str = "id",
        order: str = "asc"
    ):
        self.skip = (page - 1) * size
        self.limit = size
        self.sort_by = sort_by
        self.order = order

@app.get("/products/")
def get_products(pagination: PaginationParams = Depends()):
    return {
        "skip": pagination.skip,
        "limit": pagination.limit,
        "sort_by": pagination.sort_by
    }
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Dependency Injection কী? FastAPI তে কেন এটি গুরুত্বপূর্ণ?"

**আদর্শ উত্তর:**
> "Dependency Injection মানে একটি function এর দরকারীয় resources বাইরে থেকে inject করা, নিজে create করা নয়। FastAPI এর `Depends()` দিয়ে এটি করা হয়। এটি তিনটি কারণে গুরুত্বপূর্ণ — প্রথমত reusability, DB session, auth check, pagination params একবার লিখে বারবার use করা যায়। দ্বিতীয়ত testability, testing এর সময় fake dependency inject করা যায়। তৃতীয়ত separation of concerns, business logic আলাদা থাকে infrastructure logic থেকে। FastAPI এর `yield` dependency দিয়ে DB connection lifecycle automatically manage হয়।"

---

## ২.১২ Middleware

**Middleware** হলো request-response cycle এর মাঝখানে execute হওয়া code। প্রতিটি request এ চলে।

### 🏠 বাস্তব জীবনের উদাহরণ

একটি **Security Gate** এর মতো:
- প্রতিটি মানুষ (request) গেট দিয়ে ঢুকতে হয়
- Gate এ ID check হয় (Auth middleware)
- Entry log হয় (Logging middleware)
- Time record হয় (Timing middleware)
- বের হওয়ার সময়ও gate দিয়ে যেতে হয় (Response middleware)

### Custom Middleware

```python
from fastapi import FastAPI, Request
from fastapi.middleware.base import BaseHTTPMiddleware
import time
import uuid

app = FastAPI()

# Request timing middleware
class TimingMiddleware(BaseHTTPMiddleware):
    async def dispatch(self, request: Request, call_next):
        # Request এর আগে
        start_time = time.time()
        request_id = str(uuid.uuid4())[:8]

        print(f"[{request_id}] {request.method} {request.url}")

        # Actual endpoint call
        response = await call_next(request)

        # Response এর পরে
        process_time = time.time() - start_time
        response.headers["X-Process-Time"] = str(process_time)
        response.headers["X-Request-ID"] = request_id

        print(f"[{request_id}] Status: {response.status_code} | Time: {process_time:.3f}s")

        return response

app.add_middleware(TimingMiddleware)
```

### CORS Middleware

```python
from fastapi.middleware.cors import CORSMiddleware

app.add_middleware(
    CORSMiddleware,
    allow_origins=[
        "http://localhost:3000",      # React dev server
        "https://myapp.com",          # Production frontend
    ],
    allow_credentials=True,
    allow_methods=["GET", "POST", "PUT", "DELETE", "PATCH"],
    allow_headers=["*"],
)
```

### Multiple Middleware Stack

```python
# Middleware stack (নিচ থেকে উপরে execute হয়)
app.add_middleware(TimingMiddleware)      # 3rd: সবার শেষে add, সবার আগে run
app.add_middleware(CORSMiddleware, ...)  # 2nd
app.add_middleware(GZipMiddleware)       # 1st: সবার আগে add, সবার শেষে run

# Execution order:
# Request:  TimingMiddleware → CORSMiddleware → GZipMiddleware → Endpoint
# Response: GZipMiddleware → CORSMiddleware → TimingMiddleware → Client
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Middleware কী? Real use case কী কী?"

**আদর্শ উত্তর:**
> "Middleware হলো code যা প্রতিটি request এর আগে এবং response এর পরে run করে। Real use cases: Authentication check (প্রতিটি request এ token valid কিনা), Request logging (কে কখন কোন API call করল), Response time tracking (X-Process-Time header), CORS handling (cross-origin requests allow করা), Rate limiting (abuse prevent করা), GZip compression (response size কমানো)। FastAPI তে `BaseHTTPMiddleware` extend করে বা `@app.middleware('http')` decorator দিয়ে custom middleware তৈরি করি।"

---

## ২.১৩ Background Tasks

**Background Tasks** হলো response পাঠানোর পরে asynchronously execute হওয়া task।

### 🏠 বাস্তব জীবনের উদাহরণ

Amazon এ order করার পরে:
1. "Your order is confirmed" response আসে → **সাথে সাথে** ✅
2. Email notification পাঠানো হয় → **Background এ** (1-2 সেকেন্ড পরে)
3. Inventory update হয় → **Background এ**
4. Warehouse notify হয় → **Background এ**

User কে order confirm এর জন্য email পাঠানোর কারণে wait করতে হয় না।

### Basic Background Tasks

```python
from fastapi import FastAPI, BackgroundTasks
import time

app = FastAPI()

# Background এ run হবে এই function
def send_welcome_email(email: str, username: str):
    # Email sending simulate করছি
    time.sleep(2)  # Real এ smtplib বা sendgrid ব্যবহার করুন
    print(f"Welcome email sent to {email} for user {username}")

def update_analytics(user_id: int, action: str):
    time.sleep(1)
    print(f"Analytics updated: user {user_id} did {action}")

@app.post("/register/")
def register_user(
    username: str,
    email: str,
    background_tasks: BackgroundTasks
):
    # ১. User তৈরি করুন (Main task)
    new_user = {"id": 1, "username": username, "email": email}

    # ২. Background tasks add করুন (response এর পরে run হবে)
    background_tasks.add_task(send_welcome_email, email, username)
    background_tasks.add_task(update_analytics, new_user["id"], "register")

    # ৩. সাথে সাথে response পাঠান (email এর জন্য wait করবে না)
    return {
        "message": "Registration successful!",
        "user": new_user,
        "note": "Welcome email পাঠানো হচ্ছে..."
    }
```

### Background Tasks with Dependency Injection

```python
def write_log(message: str):
    with open("app.log", "a") as f:
        f.write(f"{datetime.now()}: {message}\n")

@app.get("/items/{item_id}")
async def get_item(
    item_id: int,
    background_tasks: BackgroundTasks
):
    item = {"id": item_id, "name": "Test Item"}

    # Response এর পরে log লেখা হবে
    background_tasks.add_task(write_log, f"Item {item_id} accessed")

    return item
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Background Tasks কী? Celery এর সাথে পার্থক্য কী?"

**আদর্শ উত্তর:**
> "Background Tasks হলো FastAPI built-in feature যা response পাঠানোর পরে কিছু কাজ async এ করে। Email পাঠানো, log লেখা, analytics update এর জন্য ভালো। সীমাবদ্ধতা হলো এটি same process এ চলে, তাই server restart হলে pending tasks হারায় এবং heavy tasks (video processing, large file) server কে slow করে। Celery হলো distributed task queue — আলাদা worker process, Redis/RabbitMQ broker ব্যবহার করে, task retry, scheduling, monitoring সব আছে। Simple tasks → Background Tasks, complex/heavy/critical tasks → Celery।"

---

## ২.১৪ PART 2 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: APIRouter কী? এর prefix ও tags কী কাজ করে?**

> APIRouter দিয়ে related endpoints একসাথে group করা হয়। `prefix="/users"` মানে router এর সব route এর আগে `/users` automatically যোগ হবে। `tags=["Users"]` Swagger documentation এ grouping এর জন্য ব্যবহার হয় — related endpoints এক section এ দেখায়।

---

**Q2: Dependency Injection এর সুবিধা কী কী?**

> ১. **Reusability:** DB session, auth check একবার লিখে সব endpoint এ use। ২. **Testability:** Testing এ fake dependency inject করা যায়। ৩. **Separation of Concerns:** Business logic আলাদা, infrastructure logic আলাদা। ৪. **Lifecycle Management:** `yield` দিয়ে DB connection automatically close হয়। ৫. **Composability:** Dependency এর মধ্যে dependency থাকতে পারে।

---

**Q3: Middleware এবং Dependency Injection এর পার্থক্য কী?**

> Middleware **প্রতিটি** request এ চলে, নির্দিষ্ট endpoint select করা যায় না। DI **নির্দিষ্ট** endpoint বা router এ apply করা যায়। Middleware global cross-cutting concerns (logging, CORS, timing) এর জন্য ভালো। DI specific business logic (auth for specific routes, DB session) এর জন্য ভালো।

---

**Q4: PUT ও PATCH এর পার্থক্য code সহ বলুন।**

```python
# PUT — Full replacement, সব field পাঠাতে হয়
class ProductFull(BaseModel):
    name: str          # Required
    price: float       # Required
    stock: int         # Required

@app.put("/products/{id}")
def full_update(id: int, product: ProductFull): ...

# PATCH — Partial update, শুধু পরিবর্তিত field পাঠান
class ProductPartial(BaseModel):
    name: Optional[str] = None    # Optional
    price: Optional[float] = None
    stock: Optional[int] = None

@app.patch("/products/{id}")
def partial_update(id: int, product: ProductPartial):
    update_data = product.dict(exclude_unset=True)  # None field বাদ
    ...
```

---

**Q5: Background Tasks কখন ব্যবহার করবেন? Celery এর সাথে পার্থক্য?**

> Background Tasks: Simple, fast, non-critical tasks যা same process এ চলতে পারে — email notification, log writing, analytics update। Celery: Heavy, critical, scheduled tasks — video processing, bulk email, payment processing, retry needed tasks। Background Tasks এ broker/worker লাগে না, Celery তে Redis/RabbitMQ ও worker process লাগে।

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|--------|-------|
| APIRouter এ prefix দিলে কী হয়? | সব endpoint URL এর শুরুতে prefix যোগ হয় |
| CORS কী? | Cross-Origin Resource Sharing — different domain থেকে API call permission |
| Middleware কোথায় চলে? | প্রতিটি request এ, endpoint এর আগে ও পরে |
| `Depends()` কীভাবে কাজ করে? | FastAPI dependency resolve করে function এ inject করে |
| File upload এ কোন package লাগে? | `python-multipart` |
| `yield` dependency কীসের জন্য? | Resource lifecycle manage করতে (DB session close) |
| 201 status code কখন? | নতুন resource তৈরি হলে |
| 204 status code কখন? | Delete successful, response body নেই |
| `exclude_unset=True` কীসের জন্য? | PATCH এ শুধু sent fields নিতে |
| Background task কখন execute হয়? | Response পাঠানোর পরে |

---

[⬆ শীর্ষে ফিরুন](#top)

---

---

<a id="part3"></a>

# PART 3: Database Integration

> **📍 এই PART এর Sections:** [৩.১](#৩১-sqlalchemy-কী) · [৩.২](#৩২-fastapi-তে-sqlalchemy-setup) · [৩.৩](#৩৩-database-models) · [৩.৪](#৩৪-pydantic-schemas-vs-db-models) · [৩.৫](#৩৫-database-session-dependency) · [৩.৬](#৩৬-crud-operations-with-db) · [৩.৭](#৩৭-relationships) · [৩.৮](#৩৮-alembic-migration) · [৩.৯](#৩৯-async-sqlalchemy) · [৩.১০](#৩১০-connection-pooling-ও-transactions) · [৩.১১](#৩১১-part-3--interview-questions--answers)

---

## ৩.১ SQLAlchemy কী?

**SQLAlchemy** হলো Python এর সবচেয়ে জনপ্রিয় ORM (Object Relational Mapper) library। এটি দিয়ে SQL database কে Python objects হিসেবে handle করা যায় — সরাসরি SQL লিখতে হয় না।

### ORM মানে কী?

```
ORM = Object Relational Mapper

Database Table  ←→  Python Class
Table Row       ←→  Class Instance (Object)
Table Column    ←→  Class Attribute
SQL Query       ←→  Python Method Call
```

### 🏠 বাস্তব জীবনের উদাহরণ

**ORM ছাড়া (Raw SQL):**
```python
# সরাসরি SQL লিখতে হয়, error-prone
cursor.execute("SELECT * FROM users WHERE id = %s AND active = %s", (user_id, True))
row = cursor.fetchone()
user = {"id": row[0], "name": row[1], "email": row[2]}
```

**ORM দিয়ে (SQLAlchemy):**
```python
# Python এর মতো, readable ও safe
user = db.query(User).filter(User.id == user_id, User.active == True).first()
```

### SQLAlchemy এর দুটি স্তর

| স্তর | নাম | ব্যবহার |
|-----|-----|---------|
| **Core** | SQL Expression Language | Raw SQL এর কাছাকাছি, maximum control |
| **ORM** | Object Relational Mapper | High-level, Python class দিয়ে কাজ |

FastAPI তে সাধারণত **ORM** স্তর ব্যবহার হয়।

### 🎤 Interview-style Explanation

**প্রশ্ন:** "ORM কী? Raw SQL এর চেয়ে ORM কেন ভালো?"

**আদর্শ উত্তর:**
> "ORM মানে Object Relational Mapper — এটি database table কে Python class এ map করে। Raw SQL এর চেয়ে ORM ভালো কারণ: ১. SQL injection এর risk কম (parameterized queries automatically), ২. Python syntax এ কাজ হয় তাই readable, ৩. Database agnostic — PostgreSQL থেকে SQLite বা MySQL এ switch করা সহজ। তবে Complex query তে Raw SQL বেশি performant হতে পারে।"

---

## ৩.২ FastAPI তে SQLAlchemy Setup

### Installation

```bash
pip install sqlalchemy psycopg2-binary  # PostgreSQL এর জন্য
pip install sqlalchemy                   # শুধু SQLite এর জন্য
pip install "sqlalchemy[asyncio]" asyncpg  # Async PostgreSQL
```

### Sync SQLAlchemy Setup (SQLite দিয়ে শুরু)

```python
# app/database.py
from sqlalchemy import create_engine
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker

# Database URL format:
# SQLite:     "sqlite:///./app.db"
# PostgreSQL: "postgresql://user:password@localhost/dbname"
# MySQL:      "mysql+pymysql://user:password@localhost/dbname"

DATABASE_URL = "sqlite:///./app.db"

# Engine তৈরি
engine = create_engine(
    DATABASE_URL,
    connect_args={"check_same_thread": False}  # SQLite only
    # pool_size=5,          # PostgreSQL তে connection pool
    # max_overflow=10,
    # echo=True             # SQL queries log করতে
)

# Session factory
SessionLocal = sessionmaker(
    autocommit=False,
    autoflush=False,
    bind=engine
)

# Base class for all models
Base = declarative_base()
```

### PostgreSQL Connection

```python
# app/core/config.py
from pydantic_settings import BaseSettings  # pip install pydantic-settings

class Settings(BaseSettings):
    DATABASE_URL: str = "postgresql://postgres:password@localhost:5432/myapp"
    
    class Config:
        env_file = ".env"

settings = Settings()

# app/database.py
from sqlalchemy import create_engine
from app.core.config import settings

engine = create_engine(
    settings.DATABASE_URL,
    pool_size=5,
    max_overflow=10,
    pool_pre_ping=True    # Connection alive কিনা check করে
)
```

### ⚠️ Common Mistakes

- ❌ `check_same_thread=False` PostgreSQL এ দেওয়া — শুধু SQLite এর জন্য
- ❌ Engine directly endpoint এ use করা — Session dependency ব্যবহার করুন
- ✅ Connection string কখনো code এ hardcode করবেন না — `.env` ফাইলে রাখুন

---

## ৩.৩ Database Models

SQLAlchemy ORM Model = Database Table এর Python representation।

### Basic Model

```python
# app/models/user.py
from sqlalchemy import Column, Integer, String, Boolean, DateTime, Text
from sqlalchemy.sql import func
from app.database import Base

class User(Base):
    __tablename__ = "users"           # Table এর নাম

    # Primary Key
    id = Column(Integer, primary_key=True, index=True)

    # String columns
    username = Column(String(50), unique=True, index=True, nullable=False)
    email = Column(String(100), unique=True, index=True, nullable=False)
    full_name = Column(String(100), nullable=True)

    # Hashed password (plain password কখনো store করবেন না!)
    hashed_password = Column(String(255), nullable=False)

    # Boolean
    is_active = Column(Boolean, default=True)
    is_admin = Column(Boolean, default=False)

    # Auto timestamps
    created_at = Column(DateTime(timezone=True), server_default=func.now())
    updated_at = Column(DateTime(timezone=True), onupdate=func.now())

    def __repr__(self):
        return f"<User(id={self.id}, username={self.username})>"
```

```python
# app/models/post.py
from sqlalchemy import Column, Integer, String, Text, ForeignKey, Boolean
from sqlalchemy.orm import relationship
from app.database import Base

class Post(Base):
    __tablename__ = "posts"

    id = Column(Integer, primary_key=True, index=True)
    title = Column(String(200), nullable=False)
    content = Column(Text, nullable=False)
    published = Column(Boolean, default=False)

    # Foreign Key — User এর সাথে সম্পর্ক
    owner_id = Column(Integer, ForeignKey("users.id"), nullable=False)

    # Relationship (Python level — SQL এ join হয়)
    owner = relationship("User", back_populates="posts")
```

```python
# User model এ posts relationship যোগ করুন
class User(Base):
    # ... আগের সব column ...
    posts = relationship("Post", back_populates="owner")
```

### Table তৈরি করা

```python
# app/main.py
from app.database import engine, Base
import app.models.user    # import করলে model register হয়
import app.models.post

# সব registered model এর table তৈরি করুন
Base.metadata.create_all(bind=engine)
```

### Column Types Reference

| SQLAlchemy Type | Python Type | SQL Type |
|-----------------|-------------|----------|
| `Integer` | `int` | INT |
| `String(n)` | `str` | VARCHAR(n) |
| `Text` | `str` | TEXT |
| `Float` | `float` | FLOAT |
| `Boolean` | `bool` | BOOLEAN |
| `DateTime` | `datetime` | TIMESTAMP |
| `Date` | `date` | DATE |
| `JSON` | `dict` | JSON |
| `Enum` | `enum` | ENUM |

---

## ৩.৪ Pydantic Schemas vs DB Models

এই পার্থক্যটি interview তে প্রায়ই জিজ্ঞেস করা হয়।

```
SQLAlchemy Model  →  Database Table (DB layer)
Pydantic Schema   →  API Request/Response (API layer)

এই দুটি আলাদা রাখা হয় কারণ:
- DB model এ সব column আছে (password, internal fields)
- API response এ সব দেখানো নিরাপদ নয়
- Request এ কিছু field read-only (id, created_at)
```

### Schema Design Pattern

```python
# app/schemas/user.py
from pydantic import BaseModel, EmailStr
from datetime import datetime
from typing import Optional

# ─── Base (shared fields) ────────────────────────────
class UserBase(BaseModel):
    username: str
    email: EmailStr
    full_name: Optional[str] = None

# ─── Create (client → server) ────────────────────────
class UserCreate(UserBase):
    password: str          # Create এ password আসে

# ─── Update (partial update) ─────────────────────────
class UserUpdate(BaseModel):
    full_name: Optional[str] = None
    email: Optional[EmailStr] = None

# ─── Response (server → client) ──────────────────────
class UserResponse(UserBase):
    id: int
    is_active: bool
    created_at: datetime
    # password নেই ← security!

    class Config:
        orm_mode = True    # SQLAlchemy object থেকে তৈরি হতে পারবে
        # Pydantic v2: from_attributes = True
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "SQLAlchemy model ও Pydantic schema আলাদা রাখেন কেন?"

**আদর্শ উত্তর:**
> "দুটি আলাদা রাখি কারণ তাদের দায়িত্ব ভিন্ন। SQLAlchemy model database এর সাথে কথা বলে — সব column আছে, password hash, timestamps সব। Pydantic schema API এর contract define করে — client কী পাঠাবে, server কী return করবে। যেমন UserCreate schema তে password আছে কিন্তু UserResponse এ নেই। এই separation ছাড়া accidentally password response এ পাঠানোর risk থাকে। এটি বাস্তবে separation of concerns এর একটি উদাহরণ।"

---

## ৩.৫ Database Session Dependency

```python
# app/database.py (আগে থেকেই আছে)
from sqlalchemy.orm import Session

def get_db():
    """
    Database session dependency.
    প্রতিটি request এ নতুন session তৈরি হয়,
    request শেষে automatically close হয়।
    """
    db = SessionLocal()
    try:
        yield db          # endpoint এ db inject হয়
    finally:
        db.close()        # সবসময় close হবে, error হলেও

# app/api/endpoints/users.py
from fastapi import Depends
from sqlalchemy.orm import Session
from app.database import get_db
from app.models.user import User
from app.schemas.user import UserCreate, UserResponse

@router.get("/{user_id}", response_model=UserResponse)
def get_user(user_id: int, db: Session = Depends(get_db)):
    user = db.query(User).filter(User.id == user_id).first()
    if not user:
        raise HTTPException(status_code=404, detail="User পাওয়া যায়নি")
    return user
```

---

## ৩.৬ CRUD Operations with DB

### CRUD Layer (Best Practice)

```python
# app/crud/user.py
from sqlalchemy.orm import Session
from typing import Optional, List
from app.models.user import User
from app.schemas.user import UserCreate, UserUpdate
from app.core.security import get_password_hash

# ─── CREATE ─────────────────────────────────────────
def create_user(db: Session, user: UserCreate) -> User:
    hashed_password = get_password_hash(user.password)
    db_user = User(
        username=user.username,
        email=user.email,
        full_name=user.full_name,
        hashed_password=hashed_password
    )
    db.add(db_user)
    db.commit()
    db.refresh(db_user)   # DB থেকে id, created_at refresh করে
    return db_user

# ─── READ ────────────────────────────────────────────
def get_user(db: Session, user_id: int) -> Optional[User]:
    return db.query(User).filter(User.id == user_id).first()

def get_user_by_email(db: Session, email: str) -> Optional[User]:
    return db.query(User).filter(User.email == email).first()

def get_users(db: Session, skip: int = 0, limit: int = 100) -> List[User]:
    return db.query(User).offset(skip).limit(limit).all()

# ─── UPDATE ──────────────────────────────────────────
def update_user(db: Session, user_id: int, user_update: UserUpdate) -> Optional[User]:
    db_user = get_user(db, user_id)
    if not db_user:
        return None

    # শুধু পাঠানো fields update করুন
    update_data = user_update.dict(exclude_unset=True)
    for field, value in update_data.items():
        setattr(db_user, field, value)

    db.commit()
    db.refresh(db_user)
    return db_user

# ─── DELETE ──────────────────────────────────────────
def delete_user(db: Session, user_id: int) -> bool:
    db_user = get_user(db, user_id)
    if not db_user:
        return False
    db.delete(db_user)
    db.commit()
    return True
```

### Endpoint Layer (thin, uses CRUD)

```python
# app/api/endpoints/users.py
from fastapi import APIRouter, Depends, HTTPException, status
from sqlalchemy.orm import Session
from typing import List
from app.database import get_db
from app.schemas.user import UserCreate, UserResponse, UserUpdate
from app.crud import user as crud_user

router = APIRouter()

@router.post("/", response_model=UserResponse, status_code=201)
def create_user(user: UserCreate, db: Session = Depends(get_db)):
    # Email already exists?
    if crud_user.get_user_by_email(db, user.email):
        raise HTTPException(status_code=409, detail="Email ইতিমধ্যে registered")
    return crud_user.create_user(db, user)

@router.get("/", response_model=List[UserResponse])
def list_users(skip: int = 0, limit: int = 10, db: Session = Depends(get_db)):
    return crud_user.get_users(db, skip=skip, limit=limit)

@router.get("/{user_id}", response_model=UserResponse)
def get_user(user_id: int, db: Session = Depends(get_db)):
    user = crud_user.get_user(db, user_id)
    if not user:
        raise HTTPException(status_code=404, detail="User পাওয়া যায়নি")
    return user

@router.patch("/{user_id}", response_model=UserResponse)
def update_user(user_id: int, user: UserUpdate, db: Session = Depends(get_db)):
    updated = crud_user.update_user(db, user_id, user)
    if not updated:
        raise HTTPException(status_code=404, detail="User পাওয়া যায়নি")
    return updated

@router.delete("/{user_id}", status_code=204)
def delete_user(user_id: int, db: Session = Depends(get_db)):
    if not crud_user.delete_user(db, user_id):
        raise HTTPException(status_code=404, detail="User পাওয়া যায়নি")
```

### Common SQLAlchemy Queries

```python
# সব record
users = db.query(User).all()

# Filter
active_users = db.query(User).filter(User.is_active == True).all()

# Multiple filters (AND)
result = db.query(User).filter(
    User.is_active == True,
    User.is_admin == False
).all()

# OR condition
from sqlalchemy import or_
result = db.query(User).filter(
    or_(User.email == email, User.username == username)
).first()

# LIKE search
users = db.query(User).filter(User.username.like(f"%{query}%")).all()

# Order by
users = db.query(User).order_by(User.created_at.desc()).all()

# Count
count = db.query(User).filter(User.is_active == True).count()

# Pagination
users = db.query(User).offset(skip).limit(limit).all()

# Join
from sqlalchemy.orm import joinedload
users_with_posts = db.query(User).options(joinedload(User.posts)).all()
```

---

## ৩.৭ Relationships

### One-to-Many (একজন User এর অনেক Post)

```python
# models/user.py
class User(Base):
    __tablename__ = "users"
    id = Column(Integer, primary_key=True)
    username = Column(String(50))

    # One user → Many posts
    posts = relationship("Post", back_populates="owner", cascade="all, delete-orphan")

# models/post.py
class Post(Base):
    __tablename__ = "posts"
    id = Column(Integer, primary_key=True)
    title = Column(String(200))
    owner_id = Column(Integer, ForeignKey("users.id"))

    # Many posts → One user
    owner = relationship("User", back_populates="posts")
```

```python
# ব্যবহার:
user = db.query(User).filter(User.id == 1).first()
print(user.posts)     # User এর সব posts — lazy load হয়

post = db.query(Post).filter(Post.id == 1).first()
print(post.owner)     # Post এর owner user
```

### Many-to-Many (Student ↔ Course)

```python
# Association Table (junction table)
from sqlalchemy import Table

student_course = Table(
    "student_course",
    Base.metadata,
    Column("student_id", Integer, ForeignKey("students.id"), primary_key=True),
    Column("course_id", Integer, ForeignKey("courses.id"), primary_key=True)
)

class Student(Base):
    __tablename__ = "students"
    id = Column(Integer, primary_key=True)
    name = Column(String(100))
    courses = relationship("Course", secondary=student_course, back_populates="students")

class Course(Base):
    __tablename__ = "courses"
    id = Column(Integer, primary_key=True)
    title = Column(String(200))
    students = relationship("Student", secondary=student_course, back_populates="courses")
```

### Eager vs Lazy Loading

```python
# Lazy Loading (default) — access করলে তখন query হয়
user = db.query(User).first()
posts = user.posts    # এখানে DB query হবে (N+1 problem!)

# Eager Loading — একসাথে join করে আনে
from sqlalchemy.orm import joinedload, selectinload

# joinedload — SQL JOIN ব্যবহার করে
users = db.query(User).options(joinedload(User.posts)).all()

# selectinload — আলাদা query কিন্তু N+1 avoid করে
users = db.query(User).options(selectinload(User.posts)).all()
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "N+1 problem কী? কীভাবে এড়াবেন?"

**আদর্শ উত্তর:**
> "N+1 problem হলো: 1টি query তে N জন user আনলাম, তারপর প্রতিটি user এর posts এর জন্য আলাদা আলাদা N টি query হয় — মোট N+1 query। 100 user হলে 101 query, 1000 user হলে 1001 query। Solution হলো eager loading — `joinedload()` দিয়ে SQL JOIN এ একসাথে আনা, অথবা `selectinload()` দিয়ে 2টি query তে সব আনা। Production এ lazy loading সাবধানে ব্যবহার করতে হয়।"

---

## ৩.৮ Alembic Migration

**Alembic** হলো SQLAlchemy এর official database migration tool।

### 🏠 বাস্তব জীবনের উদাহরণ

আপনার production database এ 10,000 user আছে। নতুন feature এর জন্য `phone_number` column যোগ করতে হবে। পুরো DB delete করে নতুন করে তৈরি করা যাবে না — **Migration** দরকার।

```
Migration = Live database এ controlled ভাবে schema change করা
(Table add, column add, column rename, index create ইত্যাদি)
```

### Alembic Setup

```bash
pip install alembic

# Project এ initialize
alembic init alembic

# Directory structure:
# alembic/
# ├── env.py          ← Configure করতে হবে
# ├── script.py.mako  ← Migration template
# └── versions/       ← Migration files এখানে
# alembic.ini         ← Main config
```

```python
# alembic/env.py এ এটি configure করুন:
from app.database import Base
from app.models import user, post    # সব models import করুন

target_metadata = Base.metadata

# alembic.ini তে:
# sqlalchemy.url = postgresql://user:pass@localhost/dbname
```

### Migration Workflow

```bash
# ১. Model change করুন (নতুন column যোগ করুন)
# user.py তে: phone = Column(String(20), nullable=True)

# ২. Auto-generate migration
alembic revision --autogenerate -m "add phone to users"
# Creates: alembic/versions/abc123_add_phone_to_users.py

# ৩. Migration file দেখুন ও verify করুন
# (সবসময় auto-generated migration verify করুন!)

# ৪. Migration apply করুন
alembic upgrade head

# Rollback করুন
alembic downgrade -1       # একধাপ পিছনে
alembic downgrade base     # সব migration rollback

# History দেখুন
alembic history

# Current version দেখুন
alembic current
```

### Generated Migration File দেখতে এরকম

```python
# alembic/versions/abc123_add_phone_to_users.py

def upgrade():
    op.add_column(
        "users",
        sa.Column("phone", sa.String(length=20), nullable=True)
    )

def downgrade():
    op.drop_column("users", "phone")
```

### ⚠️ Common Mistakes

- ❌ Production এ `Base.metadata.create_all()` ব্যবহার করা — শুধু development এ
- ❌ Auto-generated migration verify না করা
- ❌ Migration file edit না করা (complex changes auto-detect হয় না)
- ✅ CI/CD pipeline এ `alembic upgrade head` যোগ করুন

---

## ৩.৯ Async SQLAlchemy

FastAPI async support এর পূর্ণ সুবিধা নিতে Async SQLAlchemy ব্যবহার করুন।

### Setup

```bash
pip install "sqlalchemy[asyncio]" asyncpg  # PostgreSQL async driver
# অথবা SQLite async এর জন্য:
pip install aiosqlite
```

```python
# app/database.py (Async version)
from sqlalchemy.ext.asyncio import create_async_engine, AsyncSession
from sqlalchemy.orm import sessionmaker, declarative_base

# Async database URL
ASYNC_DATABASE_URL = "postgresql+asyncpg://user:pass@localhost/dbname"
# SQLite: "sqlite+aiosqlite:///./app.db"

# Async engine
async_engine = create_async_engine(
    ASYNC_DATABASE_URL,
    pool_size=10,
    max_overflow=20,
    echo=False
)

# Async session factory
AsyncSessionLocal = sessionmaker(
    async_engine,
    class_=AsyncSession,
    expire_on_commit=False
)

Base = declarative_base()

# Async dependency
async def get_async_db():
    async with AsyncSessionLocal() as session:
        yield session
```

### Async CRUD Operations

```python
# app/crud/async_user.py
from sqlalchemy.ext.asyncio import AsyncSession
from sqlalchemy import select, update, delete
from app.models.user import User
from app.schemas.user import UserCreate

async def get_user(db: AsyncSession, user_id: int):
    result = await db.execute(
        select(User).where(User.id == user_id)
    )
    return result.scalar_one_or_none()

async def get_users(db: AsyncSession, skip: int = 0, limit: int = 10):
    result = await db.execute(
        select(User).offset(skip).limit(limit)
    )
    return result.scalars().all()

async def create_user(db: AsyncSession, user: UserCreate):
    db_user = User(**user.dict())
    db.add(db_user)
    await db.commit()
    await db.refresh(db_user)
    return db_user

async def delete_user(db: AsyncSession, user_id: int):
    await db.execute(delete(User).where(User.id == user_id))
    await db.commit()
```

```python
# app/api/endpoints/async_users.py
from fastapi import APIRouter, Depends
from sqlalchemy.ext.asyncio import AsyncSession
from app.database import get_async_db

router = APIRouter()

@router.get("/{user_id}")
async def get_user(user_id: int, db: AsyncSession = Depends(get_async_db)):
    user = await async_crud.get_user(db, user_id)
    if not user:
        raise HTTPException(status_code=404, detail="User পাওয়া যায়নি")
    return user
```

### Sync vs Async কখন কোনটি?

| পরিস্থিতি | Recommendation |
|-----------|---------------|
| Simple API, small traffic | Sync (সহজ, কম complexity) |
| High concurrency, many I/O ops | Async (better performance) |
| Existing sync codebase | Sync (mixing complex) |
| New project, modern setup | Async |
| Heavy CPU computation | Sync (async CPU বাঁচায় না) |

---

## ৩.১০ Connection Pooling ও Transactions

### Connection Pooling

```python
# Connection Pool কী?
# ─────────────────────────────────────────────────────
# প্রতিটি request এ নতুন DB connection তৈরি করা expensive
# Connection Pool = pre-created connections এর group
# Request আসলে pool থেকে connection নেয়, শেষে ফেরত দেয়

engine = create_engine(
    DATABASE_URL,
    pool_size=10,          # Permanent connections সংখ্যা
    max_overflow=20,       # Extra connections (peak load)
    pool_timeout=30,       # Connection পেতে max wait (seconds)
    pool_recycle=1800,     # 30 মিনিট পরে connection নতুন করে
    pool_pre_ping=True     # Dead connection detect করে
)

# Pool status check
print(engine.pool.status())
```

### Transactions

```python
from sqlalchemy.orm import Session

def transfer_money(
    db: Session,
    from_user_id: int,
    to_user_id: int,
    amount: float
):
    """
    Money transfer — atomic operation।
    সবটুকু সফল হবে, অথবা কিছুই হবে না।
    """
    try:
        # Transaction শুরু হয় db.begin() তে অথবা auto
        from_user = db.query(User).filter(User.id == from_user_id).with_for_update().first()
        to_user = db.query(User).filter(User.id == to_user_id).with_for_update().first()

        if not from_user or not to_user:
            raise ValueError("User পাওয়া যায়নি")

        if from_user.balance < amount:
            raise ValueError("Insufficient balance")

        from_user.balance -= amount
        to_user.balance += amount

        db.commit()   # সফল হলে commit
        return True

    except Exception as e:
        db.rollback()  # যেকোনো error এ rollback
        raise e
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Database transaction কী? ACID properties কী?"

**আদর্শ উত্তর:**
> "Transaction হলো একটি logical unit of work — হয় সবটুকু execute হবে, অথবা কিছুই হবে না। ACID properties: **Atomicity** — সব operations এক সাথে সফল বা fail; **Consistency** — DB সবসময় valid state এ থাকবে; **Isolation** — একটি transaction অন্যটির মাঝে interfere করবে না; **Durability** — commit হলে data permanent। Bank transfer এর উদাহরণ — টাকা কাটা হলো কিন্তু জমা হয়নি এটি acceptable নয়, তাই transaction দরকার।"

---

## ৩.১১ PART 3 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: SQLAlchemy ORM ও Core এর পার্থক্য কী?**

> ORM (Object Relational Mapper) level এ Python class দিয়ে কাজ হয় — `db.query(User).filter(...)`. Core level এ SQL Expression Language ব্যবহার হয় যা raw SQL এর কাছাকাছি কিন্তু Python syntax এ। ORM simple CRUD এর জন্য ভালো, Core complex queries ও performance-critical operations এর জন্য বেশি control দেয়।

---

**Q2: `db.commit()` ও `db.refresh()` কী করে?**

> `db.commit()` pending changes database এ permanently save করে — এর আগে পর্যন্ত changes শুধু memory তে থাকে। `db.refresh(obj)` commit এর পরে database থেকে object এর latest state reload করে — এটি দরকার কারণ DB auto-generated values (id, created_at, updated_at) memory তে আপডেট হয় না commit ছাড়া।

---

**Q3: Alembic কি production এ use করা safe?**

> হ্যাঁ, Alembic production এর জন্যই তৈরি। `alembic upgrade head` production deployment এর অংশ হওয়া উচিত। তবে auto-generated migration সবসময় manually review করুন — complex changes (column rename) সঠিকভাবে detect নাও হতে পারে। Deployment এর আগে staging environment এ test করুন।

---

**Q4: N+1 query problem কী এবং সমাধান কী?**

> N টি parent record এনে প্রতিটির জন্য আলাদা child query হলে total N+1 queries হয়। Solution: eager loading — `joinedload()` দিয়ে SQL JOIN এ একসাথে আনা, অথবা `selectinload()` দিয়ে 2 queries তে সব আনা। ORM debug করতে `echo=True` দিয়ে SQL log দেখুন।

---

**Q5: Async SQLAlchemy কখন ব্যবহার করবেন?**

> High concurrency API তে যেখানে অনেক I/O-bound operations (DB queries, external API calls) একসাথে হয়। Async দিলে একটি DB query এর wait এর সময় অন্য request serve করা যায়। Simple low-traffic API তে sync ই যথেষ্ট এবং simpler। নতুন project শুরু করলে async setup recommend করি।

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|--------|-------|
| ORM মানে কী? | Object Relational Mapper |
| `Base.metadata.create_all()` কী করে? | সব registered model এর DB table তৈরি করে |
| `orm_mode = True` কেন লাগে? | SQLAlchemy object থেকে Pydantic model তৈরির জন্য |
| Alembic কী? | SQLAlchemy migration tool |
| `yield` dependency তে কেন? | Request পরে DB session close করার জন্য |
| Lazy loading এর সমস্যা? | N+1 query problem |
| `with_for_update()` কী করে? | Row lock করে (concurrent update থেকে রক্ষা) |
| `pool_pre_ping=True` কীসের জন্য? | Dead DB connection detect করে replace করে |
| Async DB driver for PostgreSQL? | asyncpg |
| `db.rollback()` কখন? | Error হলে transaction cancel করতে |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part4"></a>

# PART 4: Authentication & Security

> **📍 এই PART এর Sections:** [৪.১](#৪১-authentication-vs-authorization) · [৪.২](#৪২-password-hashing) · [৪.৩](#৪৩-jwt-authentication) · [৪.৪](#৪৪-oauth2-with-password-flow) · [৪.৫](#৪৫-refresh-tokens) · [৪.৬](#৪৬-role-based-access-control-rbac) · [৪.৭](#৪৭-cors) · [৪.৮](#৪৮-rate-limiting) · [৪.৯](#৪৯-environment-variables-ও-secrets) · [৪.১০](#৪১০-api-security-best-practices) · [৪.১১](#৪১১-part-4--interview-questions--answers)

---

## ৪.১ Authentication vs Authorization

এই দুটির পার্থক্য interview এ প্রায়ই জিজ্ঞেস করা হয়।

| বিষয় | Authentication | Authorization |
|-------|---------------|---------------|
| **প্রশ্ন** | "আপনি কে?" | "আপনি কী করতে পারবেন?" |
| **কাজ** | Identity verify করা | Permission check করা |
| **উদাহরণ** | Login করা | Admin page access করা |
| **কখন হয়** | আগে | Authentication এর পরে |
| **Failure code** | 401 Unauthorized | 403 Forbidden |

### 🏠 বাস্তব জীবনের উদাহরণ

```
একটি অফিস ভবনে প্রবেশ:
  ১. Security গেটে ID card দেখান → Authentication (আপনি কে?)
  ২. 5th floor এ যেতে চান → Authorization (আপনার permission আছে?)

  Authentication fail → "আমি আপনাকে চিনি না" (401)
  Authorization fail  → "আপনি এখানে যেতে পারবেন না" (403)
```

---

## ৪.২ Password Hashing

**Plain password কখনো database এ store করবেন না।** এটি সবচেয়ে বড় security mistake।

### bcrypt দিয়ে Hashing

```bash
pip install "passlib[bcrypt]"
```

```python
# app/core/security.py
from passlib.context import CryptContext

# bcrypt context তৈরি
pwd_context = CryptContext(schemes=["bcrypt"], deprecated="auto")

def get_password_hash(password: str) -> str:
    """Plain password → hashed password"""
    return pwd_context.hash(password)

def verify_password(plain_password: str, hashed_password: str) -> bool:
    """Login এ verify করুন"""
    return pwd_context.verify(plain_password, hashed_password)
```

```python
# ব্যবহার:
plain = "MySecret123"
hashed = get_password_hash(plain)
print(hashed)
# $2b$12$EixZaYVK1fsbw1ZfbX3OXePaWxn96p36WQoeG6Lruj3vjPGga31lW

# Verify
print(verify_password("MySecret123", hashed))   # True
print(verify_password("WrongPassword", hashed)) # False
```

### কেন bcrypt?

```
MD5/SHA1  → ❌ Fast hash — brute force সহজ
SHA256    → ❌ Fast hash — rainbow table attack
bcrypt    → ✅ Slow hash (intentionally!) — brute force কঠিন
           → Salt automatically add করে — rainbow table আটকায়
           → Cost factor adjust করা যায় (future-proof)
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Password কীভাবে store করেন? MD5 কি ব্যবহার করা উচিত?"

**আদর্শ উত্তর:**
> "Password plain text এ বা reversible encryption এ store করা উচিত নয়। আমি bcrypt বা argon2 দিয়ে one-way hashing করি। MD5 বা SHA-1 ব্যবহার করা উচিত নয় কারণ এগুলো fast hash — GPU দিয়ে seconds এ billions of attempts করা যায়। bcrypt intentionally slow এবং automatic salt add করে তাই rainbow table attack কাজ করে না। passlib library দিয়ে FastAPI তে সহজে implement করা যায়।"

---

## ৪.৩ JWT Authentication

**JWT (JSON Web Token)** হলো stateless authentication এর সবচেয়ে জনপ্রিয় পদ্ধতি।

### JWT Structure

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9  ← Header (Base64)
.eyJzdWIiOiIxMjM0IiwiZXhwIjoxNjAwMDAwfQ  ← Payload (Base64)
.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c  ← Signature (HMAC)

Header:  {"alg": "HS256", "typ": "JWT"}
Payload: {"sub": "user_id_123", "exp": 1600000, "role": "admin"}
Signature: HMAC-SHA256(header + "." + payload, SECRET_KEY)
```

### JWT Implementation

```bash
pip install "python-jose[cryptography]"
```

```python
# app/core/security.py
from jose import JWTError, jwt
from datetime import datetime, timedelta
from typing import Optional

SECRET_KEY = "your-super-secret-key-min-32-chars"  # .env থেকে নিন!
ALGORITHM = "HS256"
ACCESS_TOKEN_EXPIRE_MINUTES = 30

def create_access_token(data: dict, expires_delta: Optional[timedelta] = None) -> str:
    """JWT Access Token তৈরি করুন"""
    to_encode = data.copy()

    expire = datetime.utcnow() + (
        expires_delta if expires_delta
        else timedelta(minutes=ACCESS_TOKEN_EXPIRE_MINUTES)
    )
    to_encode.update({"exp": expire})

    return jwt.encode(to_encode, SECRET_KEY, algorithm=ALGORITHM)

def decode_token(token: str) -> Optional[dict]:
    """Token decode ও verify করুন"""
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=[ALGORITHM])
        return payload
    except JWTError:
        return None
```

### Full Auth Flow

```python
# app/schemas/auth.py
from pydantic import BaseModel

class Token(BaseModel):
    access_token: str
    token_type: str = "bearer"

class TokenData(BaseModel):
    user_id: Optional[int] = None
    role: Optional[str] = None
```

```python
# app/api/endpoints/auth.py
from fastapi import APIRouter, Depends, HTTPException, status
from fastapi.security import OAuth2PasswordBearer, OAuth2PasswordRequestForm
from sqlalchemy.orm import Session
from app.database import get_db
from app.core.security import verify_password, create_access_token
from app.crud.user import get_user_by_email
from app.schemas.auth import Token

router = APIRouter()

# Token এর URL (client এখানে POST করবে)
oauth2_scheme = OAuth2PasswordBearer(tokenUrl="/api/v1/auth/login")

# ─── LOGIN ───────────────────────────────────────────
@router.post("/login", response_model=Token)
def login(
    form_data: OAuth2PasswordRequestForm = Depends(),
    db: Session = Depends(get_db)
):
    # User খোঁজো
    user = get_user_by_email(db, form_data.username)  # username field এ email

    # Verify
    if not user or not verify_password(form_data.password, user.hashed_password):
        raise HTTPException(
            status_code=status.HTTP_401_UNAUTHORIZED,
            detail="Email বা Password ভুল",
            headers={"WWW-Authenticate": "Bearer"}
        )

    if not user.is_active:
        raise HTTPException(status_code=400, detail="Account inactive")

    # Token তৈরি
    access_token = create_access_token(
        data={"sub": str(user.id), "role": "admin" if user.is_admin else "user"}
    )

    return {"access_token": access_token, "token_type": "bearer"}
```

### Current User Dependency

```python
# app/api/deps.py
from fastapi import Depends, HTTPException, status
from fastapi.security import OAuth2PasswordBearer
from jose import JWTError
from sqlalchemy.orm import Session
from app.database import get_db
from app.core.security import decode_token
from app.crud.user import get_user
from app.models.user import User

oauth2_scheme = OAuth2PasswordBearer(tokenUrl="/api/v1/auth/login")

def get_current_user(
    token: str = Depends(oauth2_scheme),
    db: Session = Depends(get_db)
) -> User:
    credentials_exception = HTTPException(
        status_code=status.HTTP_401_UNAUTHORIZED,
        detail="Token invalid বা expired",
        headers={"WWW-Authenticate": "Bearer"},
    )

    payload = decode_token(token)
    if payload is None:
        raise credentials_exception

    user_id = payload.get("sub")
    if user_id is None:
        raise credentials_exception

    user = get_user(db, int(user_id))
    if user is None:
        raise credentials_exception

    return user

def get_current_active_user(
    current_user: User = Depends(get_current_user)
) -> User:
    if not current_user.is_active:
        raise HTTPException(status_code=400, detail="Account inactive")
    return current_user
```

```python
# Protected endpoints
@router.get("/me", response_model=UserResponse)
def get_my_profile(current_user: User = Depends(get_current_active_user)):
    return current_user

@router.put("/me", response_model=UserResponse)
def update_my_profile(
    update_data: UserUpdate,
    current_user: User = Depends(get_current_active_user),
    db: Session = Depends(get_db)
):
    return crud_user.update_user(db, current_user.id, update_data)
```

### JWT এর সুবিধা ও সীমাবদ্ধতা

| সুবিধা | সীমাবদ্ধতা |
|--------|-----------|
| **Stateless** — server এ session store করতে হয় না | Token revoke করা কঠিন (expire পর্যন্ত valid) |
| **Scalable** — multiple servers এ কাজ করে | Token size বড় (session ID এর চেয়ে) |
| **Self-contained** — user info token এ আছে | Secret key leak হলে সব token compromise |
| **Standard** — সব platform support করে | Sensitive info payload এ রাখা যায় না |

---

## ৪.৪ OAuth2 with Password Flow

FastAPI তে OAuth2 Password Flow implement করা।

```python
# Complete working example:

# main.py
from fastapi import FastAPI, Depends, HTTPException, status
from fastapi.security import OAuth2PasswordBearer, OAuth2PasswordRequestForm
from pydantic import BaseModel
from typing import Optional

app = FastAPI()

# Fake DB
fake_users_db = {
    "rafi@example.com": {
        "id": 1,
        "email": "rafi@example.com",
        "full_name": "Rafi Ahmed",
        "hashed_password": "$2b$12$...",  # bcrypt hash of "secret123"
        "role": "user",
        "is_active": True
    },
    "admin@example.com": {
        "id": 2,
        "email": "admin@example.com",
        "full_name": "Admin User",
        "hashed_password": "$2b$12$...",
        "role": "admin",
        "is_active": True
    }
}

oauth2_scheme = OAuth2PasswordBearer(tokenUrl="token")

@app.post("/token")
async def login_for_access_token(
    form_data: OAuth2PasswordRequestForm = Depends()
):
    user = fake_users_db.get(form_data.username)
    if not user or not verify_password(form_data.password, user["hashed_password"]):
        raise HTTPException(
            status_code=401,
            detail="Incorrect email or password",
            headers={"WWW-Authenticate": "Bearer"}
        )

    token = create_access_token({"sub": str(user["id"]), "role": user["role"]})
    return {"access_token": token, "token_type": "bearer"}

@app.get("/users/me")
async def read_users_me(token: str = Depends(oauth2_scheme)):
    payload = decode_token(token)
    if not payload:
        raise HTTPException(status_code=401, detail="Invalid token")
    return {"user_id": payload["sub"], "role": payload["role"]}
```

---

## ৪.৫ Refresh Tokens

Access token short-lived রাখুন এবং Refresh token দিয়ে নতুন access token নিন।

```
Access Token:  ৩০ মিনিট expire  →  API calls এর জন্য
Refresh Token: ৭ দিন expire     →  নতুন access token নেওয়ার জন্য
```

```python
# app/core/security.py
REFRESH_TOKEN_EXPIRE_DAYS = 7

def create_refresh_token(user_id: int) -> str:
    expire = datetime.utcnow() + timedelta(days=REFRESH_TOKEN_EXPIRE_DAYS)
    data = {
        "sub": str(user_id),
        "exp": expire,
        "type": "refresh"   # Token type mark করুন
    }
    return jwt.encode(data, SECRET_KEY, algorithm=ALGORITHM)

# app/api/endpoints/auth.py
@router.post("/login", response_model=TokenPair)
def login(form_data: OAuth2PasswordRequestForm = Depends(), db: Session = Depends(get_db)):
    user = authenticate_user(db, form_data.username, form_data.password)
    if not user:
        raise HTTPException(status_code=401, detail="Invalid credentials")

    access_token = create_access_token({"sub": str(user.id)})
    refresh_token = create_refresh_token(user.id)

    return {
        "access_token": access_token,
        "refresh_token": refresh_token,
        "token_type": "bearer"
    }

@router.post("/refresh", response_model=Token)
def refresh_token(refresh_token: str, db: Session = Depends(get_db)):
    payload = decode_token(refresh_token)

    if not payload or payload.get("type") != "refresh":
        raise HTTPException(status_code=401, detail="Invalid refresh token")

    user_id = payload.get("sub")
    user = get_user(db, int(user_id))
    if not user:
        raise HTTPException(status_code=401, detail="User পাওয়া যায়নি")

    new_access_token = create_access_token({"sub": str(user.id)})
    return {"access_token": new_access_token, "token_type": "bearer"}
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** "Access token ও Refresh token এর পার্থক্য কী? কেন দুটি দরকার?"

**আদর্শ উত্তর:**
> "Access token short-lived (১৫-৩০ মিনিট) — প্রতিটি API call এ পাঠানো হয়। Refresh token long-lived (৭-৩০ দিন) — শুধু নতুন access token নেওয়ার সময় ব্যবহার হয়। দুটি দরকার কারণ: শুধু long-lived access token থাকলে চুরি হলে অনেকক্ষণ attacker access পাবে। শুধু short-lived থাকলে user বারবার login করতে হবে। Refresh token server-side revoke করা যায় (DB blacklist), কিন্তু access token stateless তাই expire পর্যন্ত valid থাকে।"

---

## ৪.৬ Role-Based Access Control (RBAC)

```python
# app/api/deps.py
from enum import Enum

class UserRole(str, Enum):
    user = "user"
    moderator = "moderator"
    admin = "admin"

def require_role(*roles: UserRole):
    """Factory function — নির্দিষ্ট role এর জন্য dependency তৈরি করে"""
    def role_checker(current_user: User = Depends(get_current_active_user)):
        user_role = current_user.role
        if user_role not in [r.value for r in roles]:
            raise HTTPException(
                status_code=status.HTTP_403_FORBIDDEN,
                detail=f"এই action এর জন্য {[r.value for r in roles]} role দরকার"
            )
        return current_user
    return role_checker

# ব্যবহার:
@router.get("/admin/dashboard")
def admin_dashboard(
    admin: User = Depends(require_role(UserRole.admin))
):
    return {"dashboard": "admin data"}

@router.get("/reports")
def view_reports(
    user: User = Depends(require_role(UserRole.admin, UserRole.moderator))
):
    return {"reports": "data"}

@router.delete("/users/{id}")
def delete_user(
    id: int,
    admin: User = Depends(require_role(UserRole.admin)),
    db: Session = Depends(get_db)
):
    crud_user.delete_user(db, id)
```

---

## ৪.৭ CORS

**CORS (Cross-Origin Resource Sharing)** — Browser এ different origin থেকে API call করার permission।

```
Origin = Protocol + Domain + Port
http://localhost:3000  ←→  http://localhost:8000
এই দুটি different origin → CORS লাগবে
```

```python
from fastapi.middleware.cors import CORSMiddleware

app = FastAPI()

# Development
app.add_middleware(
    CORSMiddleware,
    allow_origins=["http://localhost:3000", "http://localhost:5173"],
    allow_credentials=True,                    # Cookies allow
    allow_methods=["GET", "POST", "PUT", "DELETE", "PATCH", "OPTIONS"],
    allow_headers=["Authorization", "Content-Type"],
)

# Production — specific origins
ALLOWED_ORIGINS = [
    "https://myapp.com",
    "https://www.myapp.com",
    "https://admin.myapp.com"
]

app.add_middleware(
    CORSMiddleware,
    allow_origins=ALLOWED_ORIGINS,
    allow_credentials=True,
    allow_methods=["*"],
    allow_headers=["*"],
)

# ⚠️ NEVER do this in production:
# allow_origins=["*"]  with  allow_credentials=True
# এটি CORS misconfiguration — security vulnerability
```

### CORS কীভাবে কাজ করে

```
Browser → Preflight (OPTIONS) request → Server
Server  → "এই origin allow" → Browser
Browser → Actual request → Server
Server  → Response with CORS headers

CORS Headers:
  Access-Control-Allow-Origin: https://myapp.com
  Access-Control-Allow-Methods: GET, POST, DELETE
  Access-Control-Allow-Headers: Authorization, Content-Type
```

---

## ৪.৮ Rate Limiting

```bash
pip install slowapi  # FastAPI rate limiting
```

```python
from fastapi import FastAPI, Request
from slowapi import Limiter, _rate_limit_exceeded_handler
from slowapi.util import get_remote_address
from slowapi.errors import RateLimitExceeded

# Rate limiter setup
limiter = Limiter(key_func=get_remote_address)
app = FastAPI()
app.state.limiter = limiter
app.add_exception_handler(RateLimitExceeded, _rate_limit_exceeded_handler)

# Specific endpoint এ rate limit
@app.get("/api/data")
@limiter.limit("10/minute")         # প্রতি minute এ ১০ বার
async def get_data(request: Request):
    return {"data": "value"}

@app.post("/auth/login")
@limiter.limit("5/minute")          # Login এ strict limit — brute force আটকায়
async def login(request: Request):
    return {"token": "..."}

# User-based rate limit (auth এর পরে)
@app.get("/api/search")
@limiter.limit("100/hour")
async def search(request: Request, current_user = Depends(get_current_user)):
    return {"results": []}
```

---

## ৪.৯ Environment Variables ও Secrets

```bash
pip install pydantic-settings python-dotenv
```

```python
# app/core/config.py
from pydantic_settings import BaseSettings
from typing import List

class Settings(BaseSettings):
    # App
    APP_NAME: str = "My FastAPI App"
    DEBUG: bool = False
    API_PREFIX: str = "/api/v1"

    # Security — .env থেকে লোড হবে
    SECRET_KEY: str                    # Required — no default
    ALGORITHM: str = "HS256"
    ACCESS_TOKEN_EXPIRE_MINUTES: int = 30
    REFRESH_TOKEN_EXPIRE_DAYS: int = 7

    # Database
    DATABASE_URL: str                  # Required

    # CORS
    ALLOWED_ORIGINS: List[str] = ["http://localhost:3000"]

    class Config:
        env_file = ".env"
        env_file_encoding = "utf-8"

# Singleton pattern
settings = Settings()
```

```bash
# .env file (NEVER commit to git!)
SECRET_KEY=your-super-secret-key-minimum-32-characters-long
DATABASE_URL=postgresql://user:password@localhost:5432/myapp
DEBUG=False
ALLOWED_ORIGINS=["https://myapp.com","https://www.myapp.com"]
```

```bash
# .gitignore তে যোগ করুন:
.env
.env.local
.env.production
```

```python
# ব্যবহার:
from app.core.config import settings

engine = create_engine(settings.DATABASE_URL)
token = jwt.encode(data, settings.SECRET_KEY, algorithm=settings.ALGORITHM)
```

### ⚠️ Security Rules

- ❌ SECRET_KEY code এ hardcode করবেন না
- ❌ .env file git এ push করবেন না
- ❌ Production SECRET_KEY development এ ব্যবহার করবেন না
- ✅ Production এ environment variables (server config) ব্যবহার করুন
- ✅ SECRET_KEY কমপক্ষে 32 characters random string

---

## ৪.১০ API Security Best Practices

### OWASP API Security Top 10 এর প্রাসঙ্গিক Items

```
১. Broken Object Level Authorization (BOLA)
   ❌ /users/{any_id}/data → যেকোনো user এর data দেখা যায়
   ✅ শুধু নিজের data বা admin হলে অন্যের

২. Broken Authentication
   ❌ Weak tokens, no expiry, plain password store
   ✅ JWT + bcrypt + expiry + refresh token

৩. Excessive Data Exposure
   ❌ DB object সরাসরি return (password সহ)
   ✅ response_model দিয়ে filter

৪. Rate Limiting নেই
   ❌ Unlimited login attempts → brute force
   ✅ slowapi দিয়ে rate limiting

৫. Security Misconfiguration
   ❌ CORS allow_origins=["*"] with credentials
   ✅ Specific origins, HTTPS only production
```

### Security Checklist

```python
# app/main.py — Production security setup
from fastapi import FastAPI
from fastapi.middleware.cors import CORSMiddleware
from fastapi.middleware.trustedhost import TrustedHostMiddleware
from fastapi.middleware.httpsredirect import HTTPSRedirectMiddleware

app = FastAPI(
    # Production এ docs disable করুন
    docs_url=None if settings.DEBUG == False else "/docs",
    redoc_url=None if settings.DEBUG == False else "/redoc",
)

# HTTPS redirect (production)
if not settings.DEBUG:
    app.add_middleware(HTTPSRedirectMiddleware)

# Trusted hosts
app.add_middleware(
    TrustedHostMiddleware,
    allowed_hosts=["myapp.com", "www.myapp.com", "api.myapp.com"]
)

# Security headers middleware
@app.middleware("http")
async def add_security_headers(request, call_next):
    response = await call_next(request)
    response.headers["X-Content-Type-Options"] = "nosniff"
    response.headers["X-Frame-Options"] = "DENY"
    response.headers["X-XSS-Protection"] = "1; mode=block"
    response.headers["Strict-Transport-Security"] = "max-age=31536000"
    return response
```

---

## ৪.১১ PART 4 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: JWT stateless মানে কী? Session-based auth এর সাথে পার্থক্য কী?**

> Session-based auth: Server database/memory তে session store করে। প্রতিটি request এ session ID DB তে lookup করতে হয়। Multiple server এ scale করা কঠিন। JWT stateless: Token এ সব info আছে, server কিছু store করে না। যেকোনো server decode করতে পারে। Scale করা সহজ। Trade-off হলো JWT revoke করা কঠিন — expire পর্যন্ত valid থাকে।

---

**Q2: JWT এর payload এ কোন ধরনের data রাখা উচিত এবং কোনটি রাখা উচিত নয়?**

> রাখা যাবে: user_id, role, email, token type, expiry। রাখা উচিত নয়: password, credit card, sensitive personal info, large amount of data। কারণ JWT payload শুধু Base64 encoded — যেকোনো কেউ decode করে পড়তে পারে (শুধু signature verify করতে secret key লাগে, পড়তে না)।

---

**Q3: SQL Injection কী? FastAPI + SQLAlchemy তে কীভাবে prevent করবেন?**

> SQL Injection = user input সরাসরি SQL query তে ব্যবহার করলে attacker SQL manipulate করতে পারে। SQLAlchemy ORM automatically parameterized queries use করে তাই injection prevent হয়। Raw SQL লিখলে অবশ্যই `text()` ও bind parameters ব্যবহার করুন: `db.execute(text("SELECT * FROM users WHERE id = :id"), {"id": user_id})`।

---

**Q4: CORS এর সাথে `allow_origins=["*"]` production এ কি নিরাপদ?**

> `allow_origins=["*"]` মানে যেকোনো domain API call করতে পারবে। `allow_credentials=True` সাথে একসাথে ব্যবহার করা যায় না (browser block করে)। শুধু `["*"]` public API তে OK, কিন্তু authenticated endpoints এ specific origins দেওয়া উচিত। Production এ সবসময় specific domains — আপনার frontend URL।

---

**Q5: bcrypt এ salt কী? কেন দরকার?**

> Salt হলো random data যা hash করার আগে password এর সাথে যোগ করা হয়। দরকার কারণ: ১. একই password দুই user এ ভিন্ন hash produce করে — attacker বুঝতে পারে না কারা same password ব্যবহার করছে। ২. Rainbow table attack (pre-computed hash lookup) prevent করে। bcrypt automatically unique salt generate করে এবং hash এর সাথে store করে — আলাদা save করতে হয় না।

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|--------|-------|
| JWT মানে কী? | JSON Web Token |
| JWT এর তিনটি অংশ? | Header, Payload, Signature |
| 401 vs 403? | 401 = Not authenticated, 403 = Not authorized |
| bcrypt vs MD5? | bcrypt slow & salted (safe), MD5 fast (unsafe) |
| CORS কী? | Cross-Origin Resource Sharing |
| OAuth2PasswordRequestForm কী? | Login form এর username/password receive করার helper |
| Refresh token কোথায় store করা ভালো? | HTTP-only cookie (XSS থেকে safe) |
| Rate limiting কেন? | Brute force ও DDoS আটকাতে |
| `.env` file কোথায় রাখবেন না? | Git repository তে |
| `expire_on_commit=False` async session এ কেন? | Commit এর পরেও object attribute access করতে |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part5"></a>

# PART 5: Async Programming

> **📍 এই PART এর Sections:** [৫.१](#५१-asyncawait-পরিচয়) · [५.२](#५२-event-loop) · [५.३](#५३-asyncio-module) · [५.४](#०५४-fastapi-এ-async-endpoints) · [०५.५](#०५५-concurrent-http-requests) · [०५.६](#०५६-async-context-managers) · [००५.७](#०५७-asyncio-tasks-ও-task-management) · [००५.८](#००५८-background-tasks) · [००५.९](#००५९-part-5--interview-questions--answers)

---

## ५.१ Async/Await পরিচয়

**Async** মানে \"asynchronous\" — একটি operation শেষ হওয়ার জন্য অপেক্ষা না করে অন্য কাজ করা।

### 🏠 বাস্তব জীবনের উদাহরণ

```
রেস্টুরেন্টে ওয়েটার:
  Sync (old way): গ্রাহক A কে খাবার serve করে, A খাওয়া শেষ না হওয়া পর্যন্ত অপেক্ষা করে।
             অন্য গ্রাহকরা অপেক্ষা করে। খুবই inefficient।
  
  Async (new way): গ্রাহক A কে খাবার serve করে, সাথে সাথে B কে order নেয়,
             C কে পানি দেয়, D র টেবিল clear করে। যখন A খাওয়া শেষ করে
             তখন bill দেয়। সবাই একসাথে serve হয়।
```

### Sync vs Async Code

```python
# ─── SYNC (blocking) ───────────────────────────
import requests
import time

start = time.time()
response1 = requests.get(\"https://api.example.com/user/1\")  # 2 sec
response2 = requests.get(\"https://api.example.com/user/2\")  # 2 sec
response3 = requests.get(\"https://api.example.com/user/3\")  # 2 sec
print(f\"Total: {time.time() - start:.1f} sec\")  # 6 sec ❌

# ─── ASYNC (non-blocking) ─────────────────────────
import aiohttp
import asyncio
import time

async def fetch_users():
    start = time.time()
    async with aiohttp.ClientSession() as session:
        # Concurrently করে fetch করুন
        async with session.get(\"https://api.example.com/user/1\") as r1:
            pass
        async with session.get(\"https://api.example.com/user/2\") as r2:
            pass
        async with session.get(\"https://api.example.com/user/3\") as r3:
            pass
    print(f\"Total: {time.time() - start:.1f} sec\")  # 2 sec ✅

asyncio.run(fetch_users())
```

### async/await Syntax

```python
# async function সংজ্ঞা
async def greet(name: str) -> str:
    # await — \"এখানে কিছু হতে দিন, এই সময়ে আমি অন্য কিছু করব না\"
    result = await some_async_operation(name)
    return result

# ব্যবহার
asyncio.run(greet(\"Rafi\"))  # Run করুন
```

### 🎤 Interview-style Explanation

**প্রশ্ন:** \"Sync ও async এর পার্থক্য কী? কেন FastAPI async ব্যবহার করে?\"

**আদর্শ উত্তর:**
> \"Sync: একটি operation শেষ হওয়া পর্যন্ত পরবর্তী operation block থাকে। Async: একটি operation (যেমন DB query, HTTP request) কে ফিরিয়ে দিয়ে engine অন্য request serve করে। FastAPI ASGI framework, যা async support করে — একই thread এ হাজারো concurrent connections handle করতে পারে। High concurrency scenario এ sync থেকে 10-100x better performance পাওয়া যায়।\"

---

## ०५.२ Event Loop

**Event Loop** হলো asyncio এর core — এটি async tasks manage করে।

Event loop একটি thread এ হাজার হাজার concurrent request handle করতে পারে:

```
┌─────────────────────────────────────────┐
│  Event Loop (Single Thread)             │
├─────────────────────────────────────────┤
│ Task 1 (DB query) → wait           │
│ Task 2 (HTTP) → wait               │
│ Task 3 (File read) → wait          │
│                                     │
│ Task 1 ready → resume              │
│ Task 2 ready → resume              │
│ Task 3 ready → resume              │
└─────────────────────────────────────────┘
```

### Basic Example

```python
import asyncio

async def task1():
    print(\"Task 1 শুরু\")
    await asyncio.sleep(2)
    print(\"Task 1 শেষ\")

async def task2():
    print(\"Task 2 শুরু\")
    await asyncio.sleep(1)
    print(\"Task 2 শেষ\")

async def main():
    # একসাথে run করুন
    await asyncio.gather(task1(), task2())  # Total 2 sec (not 3)

asyncio.run(main())
```

---

## ०५.३ asyncio Module

```python
import asyncio

# gather — multiple coroutines একসাথে
results = await asyncio.gather(async_func1(), async_func2())

# create_task — background এ run করুন
task = asyncio.create_task(async_func())
await task

# sleep — non-blocking wait
await asyncio.sleep(2)

# timeout
try:
    await asyncio.wait_for(operation(), timeout=5)
except asyncio.TimeoutError:
    print(\"Timeout\")
```

---

## ०५.४ FastAPI এ Async Endpoints

```python
from fastapi import FastAPI

app = FastAPI()

@app.get(\"/async\")
async def get_async_data():
    await asyncio.sleep(1)  # non-blocking
    return {\"data\": \"value\"}
```

---

## ०५.५ Concurrent HTTP Requests

```bash
pip install httpx
```

```python
import httpx
import asyncio

async def fetch_users(user_ids):
    async with httpx.AsyncClient() as client:
        tasks = [client.get(f\"https://api.example.com/users/{uid}\") for uid in user_ids]
        responses = await asyncio.gather(*tasks)
        return [r.json() for r in responses]
```

---

## ०५.६ Async Context Managers

```python
async def async_operation():
    async with aiohttp.ClientSession() as session:
        async with session.get(\"https://api.example.com\") as response:
            data = await response.json()
            return data
```

---

## ०५.७ asyncio Tasks ও Task Management

```python
async def main():
    # Create task
    task = asyncio.create_task(long_operation())
    
    # Cancel করুন
    task.cancel()
    
    # Multiple tasks
    tasks = [asyncio.create_task(op()) for _ in range(3)]
    results = await asyncio.gather(*tasks)
```

---

## ०५.८ Background Tasks

```python
from fastapi import BackgroundTasks

@app.post(\"/register\")
async def register(user_data: dict, background_tasks: BackgroundTasks):
    user = save_user(user_data)
    
    # Background task add করুন
    background_tasks.add_task(send_email, user[\"email\"])
    
    return {\"status\": \"success\"}
```

---

## ००५.९ PART 5 — Interview Questions & Answers

**Q: Sync এবং Async এ Thread ও Event Loop এর পার্থক্য?**

> Sync: প্রতিটি request একটি thread এ চলে। Async: একটি thread (event loop) এ হাজার concurrent requests চলে। Async I/O-bound operations এ much better।

---

### Rapid-Fire

| প্রশ্ন | উত্তর |
|--------|----------|
| `async def`? | Async function definition |
| `await`? | Coroutine complete হওয়ার জন্য wait |
| `asyncio.gather()`? | Multiple coroutines একসাথে run |
| `create_task()`? | Background এ schedule করুন |
| `asyncio.sleep()`? | Non-blocking sleep |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id=\"part6\"></a>

# PART 6: Advanced FastAPI

> **📍 এই PART এর Sections:** [६.१](#०६१-websockets) · [०६.२](#०६२-streaming-responses) · [०६.३](#००६३-custom-middleware) · [००६.४](#०००६४-exception-handling) · [०००६.५](#०००००६५-custom-validation) · [०००००६.६](#०००००००६६-lifespan-events) · [००००००६.७](#०००००००००६७-dependency-overrides) · [०००००००००००६.८](#०००००००००००००६८-pagination-filtering-searching) · [००००००००००००००६.९](#००००००००००००००००६९-caching-with-redis) · [०००००००००००००००००६.१०](#०००००००००००००००००००००६१०-part-6--interview-questions--answers)

---

## ०६.१ WebSockets

**WebSocket** = Persistent bidirectional connection — real-time communication।

### Basic WebSocket

```python
from fastapi import FastAPI, WebSocket

@app.websocket(\"/ws\")
async def websocket_endpoint(websocket: WebSocket):
    await websocket.accept()
    try:
        while True:
            data = await websocket.receive_text()
            await websocket.send_text(f\"Echo: {data}\")
    except Exception as e:
        print(f\"Error: {e}\")
    finally:
        await websocket.close()
```

### Multi-client Broadcasting

```python
class ConnectionManager:
    def __init__(self):
        self.active_connections = []

    async def connect(self, websocket: WebSocket):
        await websocket.accept()
        self.active_connections.append(websocket)

    async def broadcast(self, message: str):
        for connection in self.active_connections:
            await connection.send_text(message)

manager = ConnectionManager()

@app.websocket(\"/ws/chat\")
async def websocket_endpoint(websocket: WebSocket):
    await manager.connect(websocket)
    try:
        while True:
            data = await websocket.receive_text()
            await manager.broadcast(f\"Message: {data}\")
    except Exception:
        manager.active_connections.remove(websocket)
```

---

## ०६.२ Streaming Responses

```python
from fastapi.responses import StreamingResponse

@app.get(\"/download\")
async def download_file():
    def file_generator():
        with open(\"file.zip\", \"rb\") as f:
            while chunk := f.read(8192):
                yield chunk

    return StreamingResponse(file_generator())

@app.get(\"/stream-events\")
async def stream_events():
    async def event_generator():
        for i in range(5):
            yield f\"data: Message {i}\\\\n\\\\n\"
            await asyncio.sleep(1)

    return StreamingResponse(event_generator(), media_type=\"text/event-stream\")
```

---

## ००६.३ Custom Middleware

```python
from fastapi.middleware.base import BaseHTTPMiddleware
from starlette.requests import Request
import time

class LoggingMiddleware(BaseHTTPMiddleware):
    async def dispatch(self, request: Request, call_next):
        start = time.time()
        response = await call_next(request)
        elapsed = time.time() - start
        response.headers[\"X-Process-Time\"] = str(elapsed)
        return response

app.add_middleware(LoggingMiddleware)
```

---

## ०००६.४ Exception Handling

```python
from fastapi import HTTPException

@app.get(\"/users/{user_id}\")
def get_user(user_id: int):
    if user_id < 0:
        raise HTTPException(status_code=400, detail=\"Invalid ID\")
    return {\"user_id\": user_id}

class CustomException(Exception):
    pass

@app.exception_handler(CustomException)
async def custom_exception_handler(request, exc):
    return JSONResponse(status_code=400, content={\"error\": str(exc)})
```

---

## ०००००६.५ Custom Validation

```python
from pydantic import BaseModel, field_validator

class User(BaseModel):
    username: str
    age: int

    @field_validator(\"username\")
    @classmethod
    def username_valid(cls, v):
        if len(v) < 3:
            raise ValueError(\"Too short\")
        return v.lower()
```

---

## ०००००००६.६ Lifespan Events

```python
from contextlib import asynccontextmanager

@asynccontextmanager
async def lifespan(app: FastAPI):
    # Startup
    print(\"Starting up...\")
    yield
    # Shutdown
    print(\"Shutting down...\")

app = FastAPI(lifespan=lifespan)
```

---

## ०००००००००६.७ Dependency Overrides

```python
from fastapi.testclient import TestClient

def get_current_user():
    return {\"user_id\": 1}

def override_get_current_user():
    return {\"user_id\": 999}

client = TestClient(app)
app.dependency_overrides[get_current_user] = override_get_current_user

response = client.get(\"/me\")
```

---

## ०००००००००००००००००००००००००८ Pagination, Filtering, Searching

```python
from fastapi import Query

@app.get(\"/items\")
def list_items(
    skip: int = Query(0, ge=0),
    limit: int = Query(10, ge=1, le=100)
):
    return items[skip:skip+limit]

@app.get(\"/search\")
def search(q: str = Query(..., min_length=1)):
    results = db.query(Product).filter(Product.name.ilike(f\"%{q}%\")).all()
    return {\"query\": q, \"results\": results}
```

---

## ००००००००००००००००००००००००९ Caching with Redis

```bash
pip install redis
```

```python
import redis
import json

redis_client = redis.Redis(host=\"localhost\", port=6379)

@app.get(\"/data\")
def get_data():
    cached = redis_client.get(\"data_key\")
    if cached:
        return json.loads(cached)
    
    result = {\"data\": \"computed\"}
    redis_client.setex(\"data_key\", 300, json.dumps(result))
    return result
```

---

## ०००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००००့ PART 6 — Interview Questions & Answers

**Q: WebSocket এবং HTTP polling এর পার্থক্য?**

> HTTP polling: বারবার request (inefficient)। WebSocket: persistent connection (real-time, efficient)।

---

### Rapid-Fire

| প্রশ্ন | উত্তর |
|--------|----------|
| WebSocket URL? | ws:// বা wss:// |
| Streaming Response? | Chunks এ পাঠানো |
| Middleware order? | FIFO (প্রথম add, শেষে execute) |
| HTTPException default status? | 400 |
| Field validator? | Pydantic model এ |
| Lifespan when? | Startup/shutdown |
| Override dependency? | `app.dependency_overrides[func] = mock` |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part7"></a>

# PART 7: Testing & Debugging

> **📍 এই PART এর Sections:** [७.१](#७१-pytest-setup) · [७.२](#७२-testclient) · [७.३](#७३-fixtures) · [७.४](#७४-mocking) · [०७.५](#०७५-logging) · [०००७.६](#०००७६-debugging) · [००००७.७](#००००७७-coverage) · [०००००००७.८](#०००००००७८-part-7--interview-questions--answers)

---

## ७.१ Pytest Setup

```bash
pip install pytest pytest-asyncio httpx
```

### প্রথম Test

```python
# tests/test_main.py
import pytest
from fastapi.testclient import TestClient
from app.main import app

client = TestClient(app)

def test_read_root():
    response = client.get("/")
    assert response.status_code == 200
    assert response.json() == {"message": "Hello"}

def test_get_item():
    response = client.get("/items/42")
    assert response.status_code == 200
    assert response.json()["item_id"] == 42
```

### Run Tests

```bash
pytest tests/                    # সব test চালান
pytest tests/test_main.py        # নির্দিষ্ট file
pytest tests/test_main.py::test_read_root  # নির্দিষ্ট test
pytest -v                        # Verbose output
pytest -s                        # Print statements show করুন
pytest --cov=app                 # Code coverage
```

---

## ७.२ TestClient

```python
from fastapi.testclient import TestClient
from app.main import app

client = TestClient(app)

# GET
response = client.get("/users/1")
assert response.status_code == 200

# POST
response = client.post(
    "/users",
    json={"username": "rafi", "email": "rafi@example.com"}
)
assert response.status_code == 201

# Headers
response = client.get("/users/me", headers={"Authorization": "Bearer token123"})
assert response.status_code == 200
```

---

## ७.३ Fixtures

Fixtures = reusable test setup।

```python
import pytest
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker
from app.database import Base, get_db
from app.main import app
from fastapi.testclient import TestClient

@pytest.fixture(scope="session")
def test_db():
    engine = create_engine("sqlite:///./test.db")
    Base.metadata.create_all(bind=engine)
    yield engine
    Base.metadata.drop_all(bind=engine)

@pytest.fixture
def db_session(test_db):
    connection = test_db.connect()
    transaction = connection.begin()
    session = sessionmaker(bind=connection)()
    
    yield session
    
    session.close()
    transaction.rollback()
    connection.close()

@pytest.fixture
def client(db_session):
    def override_get_db():
        return db_session
    
    app.dependency_overrides[get_db] = override_get_db
    yield TestClient(app)
    app.dependency_overrides.clear()

# ব্যবহার
def test_create_user(client):
    response = client.post(
        "/users",
        json={"username": "rafi", "email": "rafi@example.com", "password": "Secret123"}
    )
    assert response.status_code == 201
    assert response.json()["username"] == "rafi"
```

---

## ७.४ Mocking

```python
from unittest.mock import patch, MagicMock
import pytest

@pytest.fixture
def mock_external_api():
    with patch("app.services.fetch_user_from_external_api") as mock:
        mock.return_value = {"id": 1, "name": "External User"}
        yield mock

def test_with_mocked_api(client, mock_external_api):
    response = client.get("/users/external/1")
    assert response.status_code == 200
    mock_external_api.assert_called_once_with(1)

@pytest.fixture
async def mock_async_db():
    with patch("app.database.query_user") as mock:
        mock.return_value = {"id": 1, "username": "test"}
        yield mock

@pytest.mark.asyncio
async def test_async_operation(mock_async_db):
    result = await fetch_user(1)
    assert result["username"] == "test"
```

---

## ०७.५ Logging

```python
import logging
from fastapi import FastAPI

logger = logging.getLogger(__name__)

app = FastAPI()

@app.get("/users/{user_id}")
def get_user(user_id: int):
    logger.info(f"Fetching user {user_id}")
    user = db.get_user(user_id)
    if not user:
        logger.warning(f"User {user_id} not found")
        raise HTTPException(status_code=404)
    return user

def test_user_not_found(client, caplog):
    with caplog.at_level(logging.WARNING):
        response = client.get("/users/999")
    assert response.status_code == 404
    assert "not found" in caplog.text
```

---

## ០ ०७.६ Debugging

### pdb

```python
@app.get("/debug")
def debug_endpoint():
    import pdb; pdb.set_trace()  # Breakpoint
    return {"data": "value"}
```

### Logging

```python
logger.debug(f"Variable: {var}")
logger.info(f"Operation started")
logger.warning(f"Deprecated method")
logger.error(f"DB connection failed: {error}")
```

### VS Code Debugging

`.vscode/launch.json`:
```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "FastAPI",
            "type": "python",
            "request": "launch",
            "module": "uvicorn",
            "args": ["app.main:app", "--reload"]
        }
    ]
}
```

---

## ०७.७ Coverage

```bash
pytest --cov=app tests/
pytest --cov=app --cov-report=html tests/  # HTML report
```

---

## ०७.८ PART 7 — Interview Questions & Answers

**Q: Unit test vs Integration test?**

> Unit test: isolated function test। Integration test: multiple components together। Unit faster, integration comprehensive।

---

### Rapid-Fire

| প্রশ্ন | উত্তর |
|--------|----------|
| TestClient? | Sync client for async endpoints |
| Fixture scope? | function, class, module, session |
| Mock purpose? | External service simulation |
| pdb.set_trace()? | Debugging breakpoint |
| Coverage? | Test percentage measure |
| @pytest.mark.asyncio? | Run async tests |
| dependency_overrides? | Fake dependency injection |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part8"></a>

# PART 8: Deployment & DevOps

> **📍 এই PART এর Sections:** [०८.१](#०८१-uvicorn-configuration) · [०८.२](#०८२-docker) · [०८.३](#०८३-nginx) · [०८.४](#०८४-cicd-with-github-actions) · [०८.५](#०८५-vps-deployment) · [०८.६](#०८६-production-checklist) · [०८.७](#०८७-part-8--interview-questions--answers)

---

## १०८.१ Uvicorn Configuration

### Development

```bash
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```

### Production

```bash
# With gunicorn (sync)
gunicorn -w 4 -k uvicorn.workers.UvicornWorker app.main:app

# Async-optimized
uvicorn app.main:app --host 0.0.0.0 --port 8000 --workers 4 --loop uvloop
```

---

## १०८.२ Docker

### Dockerfile

```dockerfile
FROM python:3.11-slim

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0"]
```

### docker-compose.yml

```yaml
version: '3.8'

services:
  web:
    build: .
    ports:
      - "8000:8000"
    environment:
      DATABASE_URL: postgresql://user:pass@db:5432/myapp
      SECRET_KEY: secret
    depends_on:
      - db

  db:
    image: postgres:15
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: pass
      POSTGRES_DB: myapp
    volumes:
      - postgres_data:/var/lib/postgresql/data

volumes:
  postgres_data:
```

---

## १०८.३ Nginx

```nginx
upstream fastapi {
    server 127.0.0.1:8000;
}

server {
    listen 80;
    server_name myapp.com;

    location / {
        proxy_pass http://fastapi;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location /ws {
        proxy_pass http://fastapi;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
    }
}
```

---

## १०८.४ CI/CD with GitHub Actions

### .github/workflows/tests.yml

```yaml
name: Tests

on:
  push:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-python@v4
        with:
          python-version: '3.11'
      
      - name: Install dependencies
        run: pip install -r requirements.txt pytest
      
      - name: Run tests
        run: pytest tests/
```

---

## १०८.५ VPS Deployment

### Setup

```bash
ssh root@vps-ip

apt update && apt upgrade -y
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

git clone https://github.com/user/app.git /var/www/myapp
cd /var/www/myapp
nano .env
docker-compose up -d
```

### SSL

```bash
apt install certbot python3-certbot-nginx
certbot certonly --standalone -d myapp.com
```

---

## १०८.६ Production Checklist

- [ ] DEBUG = False
- [ ] SECRET_KEY random
- [ ] Database backups setup
- [ ] CORS configured
- [ ] HTTPS enabled
- [ ] Rate limiting enabled
- [ ] Logging configured
- [ ] Health check endpoint
- [ ] Database migrations automated
- [ ] Error monitoring (Sentry)

---

## ०८.७ PART 8 — Interview Questions & Answers

**Q: Multiple Uvicorn workers কেন?**

> Single worker = single event loop। High concurrency এর জন্য multiple workers parallel processing।

---

### Rapid-Fire

| প্রশ্ন | উত্তর |
|--------|----------|
| Uvicorn port? | 8000 (default) |
| Gunicorn role? | Process manager |
| Nginx role? | Reverse proxy |
| Docker benefit? | Environment consistency |
| Health check? | `/health` endpoint |
| Workers count? | CPU cores × 2 (approx) |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part9"></a>

# PART 9: System Design with FastAPI

**Microservices Architecture**

```
Monolith: একটি process এ সব
Microservices: আলাদা service
```

```python
from fastapi import FastAPI
import httpx

# Main API service
@app.get("/data")
async def get_data(token: str):
    async with httpx.AsyncClient() as client:
        resp = await client.post(
            "http://auth-service:8001/verify",
            json={"token": token}
        )
    return {"data": "value"}
```

**Message Queues - Celery**

```python
from celery import Celery

celery = Celery("tasks", broker="redis://localhost:6379")

@celery.task
def send_email(email: str):
    time.sleep(5)
    return "Sent"

@app.post("/email")
def email_task(email: str):
    send_email.delay(email)
    return {"status": "queued"}
```

**Redis Caching**

```python
import redis

redis_client = redis.Redis()

@app.get("/users/{uid}")
def get_user(uid: int):
    cached = redis_client.get(f"user:{uid}")
    if cached:
        return json.loads(cached)
    
    user = db.get(uid)
    redis_client.setex(f"user:{uid}", 300, json.dumps(user))
    return user
```

**Database Scaling**

- Master-Slave Replication
- Sharding (horizontal partitioning)
- Connection pooling

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part10"></a>

# PART 10: FastAPI Project Examples

**Project 1: Auth System**

```python
class User(Base):
    __tablename__ = "users"
    id = Column(Integer, primary_key=True)
    username = Column(String, unique=True)
    hashed_password = Column(String)

@app.post("/register")
def register(user: UserCreate, db: Session = Depends(get_db)):
    if db.query(User).filter(User.username == user.username).first():
        raise HTTPException(status_code=400)
    
    hashed = get_password_hash(user.password)
    db_user = User(username=user.username, hashed_password=hashed)
    db.add(db_user)
    db.commit()
    return {"message": "Created"}

@app.post("/login")
def login(form: OAuth2PasswordRequestForm = Depends(), db: Session = Depends(get_db)):
    user = db.query(User).filter(User.username == form.username).first()
    if not user or not verify_password(form.password, user.hashed_password):
        raise HTTPException(status_code=401)
    
    token = create_access_token({"sub": str(user.id)})
    return {"access_token": token}
```

**Project 2: Blog API**

```python
class Post(Base):
    __tablename__ = "posts"
    id = Column(Integer, primary_key=True)
    title = Column(String)
    content = Column(Text)
    author_id = Column(Integer, ForeignKey("users.id"))

@app.post("/posts")
def create_post(
    post: PostCreate,
    user = Depends(get_current_user),
    db: Session = Depends(get_db)
):
    db_post = Post(title=post.title, content=post.content, author_id=user.id)
    db.add(db_post)
    db.commit()
    return db_post

@app.get("/posts")
def list_posts(skip: int = 0, limit: int = 10, db: Session = Depends(get_db)):
    return db.query(Post).offset(skip).limit(limit).all()
```

**Project 3: Chat API**

```python
class ConnectionManager:
    def __init__(self):
        self.active: list[WebSocket] = []

    async def connect(self, ws: WebSocket):
        await ws.accept()
        self.active.append(ws)

    async def broadcast(self, message: str):
        for conn in self.active:
            await conn.send_text(message)

manager = ConnectionManager()

@app.websocket("/ws/chat")
async def websocket_endpoint(ws: WebSocket):
    await manager.connect(ws)
    try:
        while True:
            data = await ws.receive_text()
            await manager.broadcast(f"Message: {data}")
    except:
        manager.active.remove(ws)
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 PART 11 & 12:** Coming Soon — Interview Q&A Bank + Bangladesh Interview Prep

---

*এই হ্যান্ডবুক Bangladesh এর Junior SWE ও Python Backend Developer interview এর জন্য তৈরি। সব PART 360° coverage দেয়।*
