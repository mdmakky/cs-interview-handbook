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
| 📙 | **PART 3** — Database Integration *(Coming Soon)* | SQLAlchemy, PostgreSQL, ORM, Alembic, CRUD, Transactions |
| 📕 | **PART 4** — Authentication & Security *(Coming Soon)* | JWT, OAuth2, Password Hashing, CORS, Rate Limiting |
| 📓 | **PART 5** — Async Programming *(Coming Soon)* | async/await, Event Loop, Async DB, Concurrency |
| 📔 | **PART 6** — Advanced FastAPI *(Coming Soon)* | WebSockets, Streaming, Custom Middleware, Caching |
| 📒 | **PART 7** — Testing & Debugging *(Coming Soon)* | Pytest, TestClient, Mocking, Logging |
| 📃 | **PART 8** — Deployment & DevOps *(Coming Soon)* | Uvicorn, Docker, Nginx, CI/CD, VPS |
| 🗂️ | **PART 9** — System Design *(Coming Soon)* | Microservices, Redis, Celery, API Gateway |
| 💼 | **PART 10** — FastAPI Projects *(Coming Soon)* | Auth System, Blog API, E-commerce, Chat API |
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

> **📌 পরবর্তী:** [PART 3 — Database Integration](#toc) *(Coming Soon)*
>
> PART 3 তে থাকবে: SQLAlchemy setup, PostgreSQL integration, ORM models, Alembic migrations, async database operations, CRUD with real DB।

---

*এই হ্যান্ডবুক Bangladesh এর Junior SWE ও Python Backend Developer interview এর জন্য তৈরি। প্রতিটি concept real interview scenario মাথায় রেখে explain করা হয়েছে।*
