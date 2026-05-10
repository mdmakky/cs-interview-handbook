# 🏗️ System Design Interview Handbook
### বাংলাদেশের Junior Software Engineer ও Backend Developer-দের জন্য সম্পূর্ণ System Design গাইড

---

[![GitHub](https://img.shields.io/badge/GitHub-cs--interview--handbook-181717?style=for-the-badge&logo=github)](https://github.com/mdmakky/cs-interview-handbook)
![Language](https://img.shields.io/badge/Language-Bengali%20%2B%20English-green?style=for-the-badge)
![Level](https://img.shields.io/badge/Level-Junior%20Engineer-blue?style=for-the-badge)
![Parts](https://img.shields.io/badge/Total%20Parts-10-orange?style=for-the-badge)

---

> **লক্ষ্য:** বাংলাদেশের top software companies (Brain Station 23, Kaz Software, Priyo.com, Chaldal, Shohoz, SSL Wireless, DataSoft, BJIT, TigerIT, Pathao, ShopUp ইত্যাদি) তে Junior Engineer ও Backend Developer পদে সফলভাবে interview দেওয়া।

---

## 📚 সূচিপত্র (Table of Contents)

| PART | বিষয় | Topics | Status |
|------|-------|--------|--------|
| [PART 1](#part1) | System Design Fundamentals | Scalability, CAP, Monolith vs Microservices | ✅ |
| [PART 2](#part2) | Networking & Communication | HTTP, REST, WebSocket, JWT, CDN | ✅ |
| [PART 3](#part3) | Database Design | SQL vs NoSQL, Sharding, Replication | ✅ |
| [PART 4](#part4) | Caching & Performance | Redis, Rate Limiting, CDN | ✅ |
| [PART 5](#part5) | Message Queues & Distributed Systems | Kafka, RabbitMQ, Pub/Sub | ✅ |
| [PART 6](#part6) | System Design Case Studies | URL Shortener, Chat App, E-commerce | ✅ |
| [PART 7](#part7) | Low-Level Design (LLD) | SOLID, Design Patterns, UML | ✅ |
| [PART 8](#part8) | Cloud & DevOps Basics | AWS, Docker, Kubernetes, CI/CD | 🔜 |
| [PART 9](#part9) | Interview Q&A Bank | 200+ Questions with Detailed Answers | 🔜 |
| [PART 10](#part10) | Bangladeshi Interview Preparation | BD Company Patterns, Mock Interviews | 🔜 |

---

<details>
<summary>📖 <strong>PART 1: System Design Fundamentals</strong> — কী কী শিখবো?</summary>

- System Design কী এবং কেন গুরুত্বপূর্ণ
- High-Level Design (HLD) vs Low-Level Design (LLD)
- Scalability, Reliability, Availability, Maintainability
- Performance, Latency vs Throughput
- CAP Theorem
- Monolithic vs Microservices Architecture
- Stateless vs Stateful Systems
- Horizontal vs Vertical Scaling

</details>

<details>
<summary>🌐 <strong>PART 2: Networking & Communication Basics</strong> — কী কী শিখবো?</summary>

- Client-Server Architecture
- HTTP vs HTTPS
- REST API ও GraphQL
- WebSocket
- TCP vs UDP
- DNS ও CDN
- Load Balancer ও Reverse Proxy
- API Gateway
- Authentication vs Authorization
- JWT ও Session Management

</details>

<details>
<summary>📨 <strong>PART 5: Message Queues & Distributed Systems</strong> — কী কী শিখবো?</summary>

- Message Queue basics ও benefits
- Apache Kafka — Topic, Partition, Consumer Group
- RabbitMQ — Exchange types, routing
- Pub/Sub model vs Point-to-Point
- Event-Driven Architecture
- Distributed Systems fundamentals
- Distributed Transactions — 2PC vs Saga
- Consensus — Raft algorithm
- Fault Tolerance — Circuit Breaker, Retry, Bulkhead

</details>

<details>
<summary>🏗️ <strong>PART 6: System Design Case Studies</strong> — কী কী শিখবো?</summary>

- System Design Framework (7 Steps)
- URL Shortener (bit.ly)
- Chat Application (WhatsApp)
- Social Media Feed (Facebook/Twitter)
- Online Banking System
- Food Delivery App (Pathao Food)
- Ride Sharing App (Pathao/Uber)
- YouTube-like Video Platform
- E-commerce System (Chaldal/Daraz)
- Hospital Management System

</details>

<details>
<summary>🧩 <strong>PART 7: Low-Level Design (LLD)</strong> — কী কী শিখবো?</summary>

- SOLID Principles (SRP, OCP, LSP, ISP, DIP) — real code examples
- Design Patterns: Singleton, Factory, Observer, Strategy, Adapter, Builder, Decorator
- Composition over Inheritance
- Dependency Injection
- LLD Case Study: Parking Lot System
- LLD Case Study: Library Management System

</details>

<details>
<summary>☁️ <strong>PART 8: Cloud & DevOps Basics</strong> — কী কী শিখবো?</summary>

- Cloud Computing: IaaS, PaaS, SaaS
- AWS Core Services: EC2, S3, RDS, Lambda, VPC, CloudFront
- Docker: Dockerfile, containers, Docker Compose
- Kubernetes: Deployment, Service, HPA, kubectl commands
- CI/CD Pipeline: GitHub Actions, deployment stages
- Nginx: Reverse proxy, load balancing, SSL, rate limiting
- Monitoring: Prometheus, Grafana, Golden Signals
- Logging: Structured logs, ELK Stack
- Deployment Strategies: Rolling, Blue-Green, Canary

</details>

<details>
<summary>🗄️ <strong>PART 3: Database Design in System Design</strong> — কী কী শিখবো?</summary>

- SQL vs NoSQL — কোনটা কখন
- Database Scaling (Vertical, Read Replicas, Sharding)
- Replication — Master-Slave, Synchronous vs Asynchronous
- Sharding — Range, Hash, Directory, Geographic
- Indexing — B-Tree, Composite, Full-text
- Caching Patterns — Cache-Aside, Write-Through
- Read-Heavy vs Write-Heavy systems
- Data Consistency — Strong vs Eventual
- ACID vs BASE

</details>

<details>
<summary>⚡ <strong>PART 4: Caching & Performance Optimization</strong> — কী কী শিখবো?</summary>

- Caching কী এবং cache tiers
- Redis — Data structures, implementation, use cases
- Memcached vs Redis
- Cache Invalidation — TTL, Event-based, Versioning
- Cache problems — Stampede, Penetration, Avalanche
- CDN Caching — Cache-Control headers
- Browser Caching — ETag, Cache Busting
- Rate Limiting — Token Bucket, Fixed Window, Sliding Window
- Compression — gzip, Brotli
- Lazy Loading — Images, ORM, API Pagination

</details>

---

<a id="part1"></a>

---

# PART 1: System Design Fundamentals
### 🏗️ System Design এর মূল ভিত্তি

> **Interview টিপস:** System Design interview তে প্রথমেই interviewer দেখতে চায় তুমি একটা problem কে কতটা structured ভাবে ভাবতে পারো। Definition জানার চেয়ে বেশি জরুরি হলো real-world analogy দিয়ে explain করতে পারা।

---

## 1.1 System Design কী? (What is System Design)

### 📖 সংজ্ঞা (Definition)
System Design হলো একটি software system-এর **architecture, components, modules, interfaces, এবং data flow** পরিকল্পনা করার প্রক্রিয়া। এটি একটি high-level blueprint যা বলে দেয় — কোন component কীভাবে কাজ করবে, কোথায় data store হবে, কীভাবে scale হবে।

### 🎯 Real-Life Analogy
> বাড়ি বানানোর কথা ভাবো। একজন architect প্রথমে blueprint তৈরি করেন — কোথায় room থাকবে, কোথায় bathroom, কতগুলো floor। System Design হলো সেই blueprint — তুমি code লেখার আগে ভাবছো system টা কীভাবে বানাবো।

**বাস্তব উদাহরণ:**
- তুমি Pathao-র মতো একটা Ride Sharing App বানাবে
- System Design তোমাকে বলবে: কীভাবে rider আর driver match করবে? Location কোথায় store হবে? ১০ লাখ user একসাথে app use করলে server কি টিকবে?

### 💼 Practical Use Case
```
E-commerce App (Chaldal-এর মতো):
- User app open করলো → CDN থেকে static content আসবে
- Product search করলো → Search Service call হবে
- Cart এ add করলো → Cart Service + Database
- Payment করলো → Payment Gateway + Order Service
- Notification আসবে → Notification Service (Email/SMS)

প্রতিটা step-এ কোন technology use হবে — এটাই System Design।
```

### 🎤 Interview-Style Explanation
> **Interviewer:** "System Design কী বলো?"
> 
> **তোমার উত্তর:** "System Design হলো একটা software system এর high-level architecture plan করা। মানে হলো — কোন component কীভাবে communicate করবে, data কোথায় store হবে, system কীভাবে scale হবে — এই সব decision নেওয়া। যেমন একটা food delivery app বানাতে হলে আমাকে আগে ঠিক করতে হবে: user service, restaurant service, order service, payment service — এগুলো কীভাবে কথা বলবে।"

### ⚠️ Common Mistakes
- শুধু code level এ চিন্তা করা, big picture না দেখা
- Scalability consider না করে design করা
- Database selection এ চিন্তা না করা
- Single point of failure না ধরা

### ❓ Follow-up Questions
1. "System Design আর Software Architecture এর পার্থক্য কী?"
2. "তুমি কি কোনো real project এ System Design করেছো?"
3. "High-Level Design আর Low-Level Design কখন করো?"

---

## 1.2 System Design কেন গুরুত্বপূর্ণ? (Why System Design is Important)

### 📖 গুরুত্ব
System Design ছাড়া বানানো system গুলো:
- ❌ Scale করতে পারে না (১০০ user হলে crash)
- ❌ Maintain করা কঠিন
- ❌ একটা component fail করলে পুরো system down
- ❌ Cost বেশি, performance কম

### 📊 তুলনামূলক চিত্র

| Design ছাড়া | Design সহ |
|------------|-----------|
| Code করতে করতে architecture ঠিক করা | আগে plan, তারপর code |
| Scale করতে পারে না | Horizontal scaling সহজ |
| Tight coupling — একটা ভাঙলে সব ভাঙে | Loose coupling — independent components |
| Maintenance nightmare | Easy to maintain |
| Security holes | Security by design |

### 🏢 বাংলাদেশের Context
BD তে যেসব companies interview নেয় (Brain Station 23, BJIT, Kaz, TigerIT) তারা দেখতে চায় তুমি একটা real system design করতে পারো কিনা। Fresher হলেও basic concepts জানা দরকার।

---

## 1.3 High-Level Design (HLD) vs Low-Level Design (LLD)

### 📖 সংজ্ঞা

**High-Level Design (HLD):**
- System এর overall architecture
- কোন components থাকবে
- কোন technology use হবে (database, cache, queue)
- Components এর মধ্যে communication কীভাবে হবে
- Scale করার strategy

**Low-Level Design (LLD):**
- Specific class/function design
- Database schema
- API endpoints এর detailed design
- Algorithm selection
- Code structure (OOP principles, Design Patterns)

### 🏗️ Architecture Diagram (Text Format)

```
HLD — E-commerce System Overview:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                    [ Client: Browser/App ]
                            │
                    [ Load Balancer ]
                    ┌─────────┬─────────┐
                    ▼         ▼         ▼
             [Web Server] [Web Server] [Web Server]
                    │
          ┌─────────┼─────────┐
          ▼         ▼         ▼
    [User Service] [Product] [Order Service]
          │         Service        │
          ▼             │          ▼
      [User DB]    [Product DB]  [Order DB]
                        │
                   [Redis Cache]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

```
LLD — Order Service এর Class Design:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
class Order:
    - order_id: UUID
    - user_id: int
    - items: List[OrderItem]
    - status: OrderStatus (PENDING, CONFIRMED, DELIVERED)
    - total_price: Decimal
    - created_at: DateTime
    
    + place_order()
    + cancel_order()
    + update_status()
    + calculate_total()
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 তুলনা

| বিষয় | HLD | LLD |
|------|-----|-----|
| Focus | Overall architecture | Specific implementation |
| Audience | Tech leads, stakeholders | Developers |
| Detail level | Abstract | Detailed |
| Output | Architecture diagram | Class diagrams, DB schema |
| When | Project শুরুতে | Feature development এ |

### ❓ Interview Questions
1. "একটা Chat Application এর HLD describe করো"
2. "LLD তে কোন principles follow করো?"
3. "HLD বানানোর পর LLD কীভাবে শুরু করো?"

---

## 1.4 Scalability

### 📖 সংজ্ঞা
Scalability হলো system-এর **increasing load handle করার ক্ষমতা** — user বাড়লেও, data বাড়লেও system ঠিকমতো কাজ করবে।

### 🎯 Real-Life Analogy
> রেস্তোরাঁর কথা ভাবো। প্রথমে ১০ টেবিল, ১ জন cook। Customer বাড়লে কী করবে?
> - Option 1: বড় kitchen বানাও, powerful stove কিনো (Vertical Scaling)
> - Option 2: আরেকটা রেস্তোরাঁ খোলো পাশে (Horizontal Scaling)

### 📊 Scaling Types

```
Vertical Scaling (Scale Up):
━━━━━━━━━━━━━━━━━━━━━━━━━━━
Before: [Server: 4 CPU, 8GB RAM]
After:  [Server: 16 CPU, 64GB RAM]
→ Same server, more power
→ Limit আছে, cost বেশি

Horizontal Scaling (Scale Out):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Before: [Server 1]
After:  [Server 1] [Server 2] [Server 3]
→ Multiple servers, load balance
→ Theoretically unlimited
```

### 💡 Scalability Metrics

| Metric | Description | Example |
|--------|-------------|---------|
| Throughput | প্রতি সেকেন্ডে কতটা request handle | 10,000 req/sec |
| Latency | একটা request-এর response time | 100ms |
| Concurrency | একসাথে কতজন user | 1 million concurrent |

### 🎤 Interview Explanation
> "Scalability মানে হলো আমার system যেন user বাড়লেও ভেঙে না পড়ে। দুইভাবে scale করা যায় — Vertical মানে একটা server কে powerful করা, Horizontal মানে অনেকগুলো server একসাথে চালানো। Production এ সাধারণত Horizontal scaling বেশি use হয় কারণ এর limit নেই এবং fault tolerant।"

### ⚠️ Common Mistakes
- Premature optimization — আগেই over-engineer করা
- Vertical scaling এর limit ignore করা
- Database কে scalability bottleneck হিসেবে না দেখা

### ❓ Follow-up Questions
1. "তোমার project এ কীভাবে scalability handle করেছিলে?"
2. "Database কীভাবে scale করবে?"
3. "Auto-scaling কী?"

---

## 1.5 Reliability

### 📖 সংজ্ঞা
Reliability হলো system এর **consistently correct কাজ করার ক্ষমতা** — hardware fail করলেও, software bug হলেও, human error হলেও।

### 🎯 Real-Life Analogy
> বিমান এর কথা ভাবো। একটা engine fail করলেও বিমান চলে। কারণ redundancy আছে। Reliable system মানে হলো single point of failure নেই।

### 🔑 Reliability Techniques

```
1. Redundancy:
   ┌─────────────┐     ┌─────────────┐
   │  Primary DB  │────▶│  Replica DB  │
   └─────────────┘     └─────────────┘
   Primary fail করলে Replica take over

2. Replication:
   Master DB ──write──▶ Slave DB 1
              ──write──▶ Slave DB 2

3. Failover:
   Load Balancer → Server 1 (fail)
                 → Server 2 (take over automatically)
```

### 📊 Reliability Metrics

| Metric | Description |
|--------|-------------|
| MTBF | Mean Time Between Failures — গড়ে কতক্ষণ পর fail |
| MTTR | Mean Time To Recovery — fail হলে ঠিক হতে কতক্ষণ |
| Error Rate | মোট request এর কত % fail হয় |

### ❓ Interview Questions
1. "তোমার system এ data loss হলে কী করবে?"
2. "Single point of failure কী এবং কীভাবে avoid করবে?"
3. "Graceful degradation কী?"

---

## 1.6 Availability

### 📖 সংজ্ঞা
Availability হলো system **কতটুকু সময় up থাকে** — accessible এবং operational।

### 📊 Availability Percentages (Nines)

| Availability | Yearly Downtime | মাসিক Downtime |
|-------------|-----------------|---------------|
| 90% (1 nine) | 36.5 days | 72 hours |
| 99% (2 nines) | 3.65 days | 7.2 hours |
| 99.9% (3 nines) | 8.77 hours | 43.8 min |
| 99.99% (4 nines) | 52.6 minutes | 4.4 min |
| 99.999% (5 nines) | 5.26 minutes | 26 sec |

> **Interview টিপস:** "Five nines" মানে 99.999% availability — এটা Netflix, Amazon এর level।

### 🎯 Real-Life Analogy
> Grameenphone এর network। যদি সারাদিনে ২.৪ ঘন্টা network না থাকে — সেটা 90% availability। কিন্তু bank এর ATM এর জন্য 99.99% দরকার।

### 🔑 High Availability কীভাবে?

```
Active-Active Setup:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Load Balancer
    ├──▶ Server A (active)
    └──▶ Server B (active)
দুটোই একসাথে কাজ করে

Active-Passive Setup:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Load Balancer
    ├──▶ Server A (active) ← primary
    └──▶ Server B (standby) ← takes over if A fails
```

### ❓ Interview Questions
1. "99.9% vs 99.99% availability এর পার্থক্য কী practically?"
2. "Planned downtime কীভাবে manage করবে?"
3. "Availability আর Reliability কি একই?"

---

## 1.7 Maintainability

### 📖 সংজ্ঞা
Maintainability হলো system **সহজে modify, debug, update করার ক্ষমতা** — নতুন developer এসেও সহজে বুঝতে পারবে।

### 🔑 Maintainability Pillars

| Pillar | মানে | Example |
|--------|------|---------|
| Operability | System চালানো সহজ | Good logging, monitoring |
| Simplicity | Code বোঝা সহজ | Clean code, documentation |
| Evolvability | নতুন feature যোগ সহজ | Modular design, loose coupling |

### 💡 Best Practices
```
✅ করো:
- Clear naming conventions
- Proper documentation/comments
- Modular code (separate concerns)
- Comprehensive tests
- Good logging

❌ এড়িয়ে চলো:
- Spaghetti code (সব এক জায়গায়)
- Magic numbers/strings
- Over-engineering
- No tests
```

---

## 1.8 Performance

### 📖 সংজ্ঞা
Performance হলো system **কতটা দ্রুত এবং efficiently কাজ করে** — CPU, memory, disk, network সব মিলিয়ে।

### 📊 Performance Metrics

| Metric | Description | Good Value |
|--------|-------------|------------|
| Response Time | Request এর জবাব আসতে কত সময় | < 200ms |
| Throughput | প্রতি সেকেন্ডে কত request | 10K+ req/s |
| CPU Utilization | CPU কতটা busy | < 70% normally |
| Memory Usage | RAM এর ব্যবহার | Stable, no leak |
| Error Rate | কত % request fail | < 0.1% |

### 🔑 Performance Bottleneck Points
```
Typical Web App Performance Issues:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Client] → [Network] → [Load Balancer] → [Server] → [Database]

Bottleneck হতে পারে:
• Client-side: Heavy JavaScript, unoptimized images
• Network: High latency, low bandwidth
• Server: CPU intensive operations, memory leak
• Database: N+1 queries, missing indexes, slow joins
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 1.9 Latency vs Throughput

### 📖 সংজ্ঞা

**Latency:** একটা operation complete হতে কত সময় লাগে (ms/sec)
**Throughput:** প্রতি unit time এ কত operation করা যায় (req/sec, MB/s)

### 🎯 Real-Life Analogy
> পাইপ দিয়ে পানি যাওয়ার কথা ভাবো:
> - **Latency** = পানির একটা molecule এক প্রান্ত থেকে অন্য প্রান্তে যেতে কত সময়
> - **Throughput** = প্রতি মিনিটে কত লিটার পানি যায়

### 📊 Latency Numbers (Every Engineer Knows This!)

```
Operation                    Latency
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
L1 cache reference           ~0.5 ns
RAM reference                ~100 ns
SSD random read              ~100 μs
Network: same data center    ~500 μs
Network: Bangladesh to US    ~200 ms
HDD seek time                ~10 ms
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### ⚖️ Trade-off
> সাধারণত Latency কমালে Throughput কমে, আবার Throughput বাড়ালে Latency বাড়তে পারে। Batch processing এ throughput বেশি কিন্তু latency বেশি।

### ❓ Interview Questions
1. "High latency আর low throughput — কোন scenario তে কোনটা বেশি problem?"
2. "Database query latency কমাতে কী করবে?"
3. "P99 latency মানে কী?"

> **Memory Tip:** "Latency = Late = কতটা দেরি | Throughput = Through = কতটা পার হলো"

---

## 1.10 CAP Theorem

### 📖 সংজ্ঞা
CAP Theorem বলে: একটা distributed system এ তুমি **সর্বোচ্চ দুইটা** guarantee দিতে পারবে — তিনটা একসাথে possible না।

- **C — Consistency:** সব node এ একই সময়ে একই data দেখাবে
- **A — Availability:** প্রতিটা request এর একটা response পাবে (error হলেও)
- **P — Partition Tolerance:** Network partition হলেও system কাজ করবে

### 🎯 Real-Life Analogy
> তোমার ২টা ব্যাংক account একই bank এর দুই শাখায়:
> - **Consistency:** দুই শাখায় একই balance দেখাবে (সব time)
> - **Availability:** যেকোনো শাখায় গেলেই সার্ভিস পাবে
> - **Partition Tolerance:** দুই শাখার মধ্যে connection গেলেও কাজ চলবে

> Network partition real world এ ঘটেই। তাই P সবসময় রাখতে হয়।
> তার মানে তোমাকে choose করতে হবে: **CP** নাকি **AP**?

### 📊 CAP Choices

```
CAP Triangle:
                    Consistency (C)
                          △
                          │
                          │
           CP ────────────┼──────────── CA
        (MongoDB,         │          (RDBMS-single)
         HBase,           │
         Zookeeper)       │
                          │
              ────────────┼────────────
                    AP    │
                (Cassandra,│
                 DynamoDB, │
                 CouchDB)  │
                           ▼
                    Partition Tolerance (P)
```

| System | Type | কোথায় Use |
|--------|------|-----------|
| MySQL (single node) | CA | Traditional apps |
| MongoDB | CP | Consistency দরকার |
| Cassandra | AP | High availability দরকার |
| Redis | CP | Cache, strong consistency |
| DynamoDB | AP | Amazon scale |

### 🎤 Interview Explanation
> "CAP Theorem বলে distributed system এ Consistency, Availability, এবং Partition Tolerance — তিনটা একসাথে fully guarantee করা যায় না। Network partition real life এ হয়ই — তাই P বাদ দেওয়া যায় না। তাই আমাদের choose করতে হয় CP বা AP। যেমন banking system এ CP choose করবো — data inconsistency হলে বিপদ। কিন্তু social media feed এ AP choose করবো — একটু stale data চলবে, কিন্তু availability দরকার।"

### ⚠️ Common Mistakes
- "CAP মানে তিনটাই পাবো" — ভুল!
- P ignore করে CA system design করা (distributed এ কাজ করে না)
- CP আর AP এর trade-off বুঝতে না পারা

### ❓ Follow-up Questions
1. "Cassandra কেন AP choose করলো?"
2. "Banking system এ CAP এর কোন combination use করবে?"
3. "PACELC Theorem কী? (CAP এর extension)"

> **Memory Tip:** "CAP = তুমি সর্বোচ্চ দুইটা পাবে। Network partition (P) বাদ দেওয়া যায় না। তাই C বা A choose করো।"

---

## 1.11 Monolithic vs Microservices Architecture

### 📖 সংজ্ঞা

**Monolithic Architecture:**
- পুরো application একটা single unit হিসেবে build হয়
- সব features একই codebase এ
- একসাথে deploy হয়

**Microservices Architecture:**
- Application অনেকগুলো small, independent services এ ভাগ
- প্রতিটা service আলাদা deploy হয়
- Services API দিয়ে communicate করে

### 🏗️ Architecture Diagrams

```
Monolithic:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
┌─────────────────────────────────────────────────┐
│              Single Application                  │
│  ┌──────────┐ ┌──────────┐ ┌──────────────────┐ │
│  │   User   │ │  Order   │ │    Payment       │ │
│  │  Module  │ │  Module  │ │    Module        │ │
│  └──────────┘ └──────────┘ └──────────────────┘ │
│  ┌──────────┐ ┌──────────┐                       │
│  │ Product  │ │Notification│                      │
│  │  Module  │ │  Module  │                       │
│  └──────────┘ └──────────┘                       │
└─────────────────────────────────────────────────┘
                      │
              ┌───────────────┐
              │  One Database │
              └───────────────┘
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Microservices:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
                   [API Gateway]
          ┌──────────┬──────────┬──────────┐
          ▼          ▼          ▼          ▼
    [User Service] [Order] [Payment] [Notification]
          │          │          │          │
     [User DB]  [Order DB] [Payment DB] [Queue]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 বিস্তারিত তুলনা

| বিষয় | Monolithic | Microservices |
|------|-----------|--------------|
| Development | শুরুতে সহজ | Setup জটিল |
| Deployment | এক জায়গায় deploy | আলাদা আলাদা deploy |
| Scaling | পুরো app scale করতে হয় | শুধু যে service দরকার |
| Technology | একটাই tech stack | প্রতি service আলাদা |
| Testing | সহজ (একটা unit) | জটিল (distributed) |
| Team Size | ছোট team এ ভালো | বড় team এ ভালো |
| Failure | একটা bug পুরো app নামায় | Isolated failure |
| Data | Shared database | Separate database per service |
| Communication | Internal function call | HTTP/gRPC/Message Queue |
| BD Junior Interview | বেশি জিজ্ঞেস করে | Concepts জানতে হবে |

### 🎯 কখন কোনটা?

```
Monolithic বেছে নাও যখন:
✅ Startup বা small project
✅ Team ছোট (2-5 জন)
✅ Business logic simple
✅ Quick MVP দরকার
✅ BD এর বেশিরভাগ small companies

Microservices বেছে নাও যখন:
✅ Large scale product (Pathao, Chaldal scale)
✅ Multiple teams independently কাজ করবে
✅ Different services এ different scaling দরকার
✅ Technology flexibility দরকার
```

### 🎤 Interview Explanation
> "Monolithic হলো সব কিছু একটা application এ — develop করা সহজ কিন্তু scale করা কঠিন। Microservices এ প্রতিটা feature আলাদা service — scale করা সহজ কিন্তু complexity বেশি। BD তে বেশিরভাগ small company monolithic use করে, আর বড় product company (Pathao, Chaldal) microservices এ move করছে।"

### ⚠️ Common Mistakes
- ছোট project এ microservices নেওয়া (over-engineering)
- Monolith কে "legacy" মনে করা — এখনো valid!
- Microservices এ distributed transactions ignore করা

---

## 1.12 Stateless vs Stateful Systems

### 📖 সংজ্ঞা

**Stateless System:**
- প্রতিটা request independent
- Server কোনো previous request মনে রাখে না
- Client ই state maintain করে (token, cookie)

**Stateful System:**
- Server previous request এর information মনে রাখে
- Session এ user এর state store থাকে

### 🎯 Real-Life Analogy
> **Stateless:** ATM machine — তোমার card pin দেও, কাজ শেষ। পরের বার গেলে আবার pin দিতে হবে। ATM তোমাকে "চেনে না"।
> 
> **Stateful:** Bank এর customer care agent — তুমি কল করলে সে তোমার account history দেখে কথা বলে। পরেরবার call করলে "আপনি আগে এই বিষয়ে call করেছিলেন" বলতে পারে।

### 📊 তুলনা

| বিষয় | Stateless | Stateful |
|------|-----------|---------|
| Server memory | কম (state নেই) | বেশি (state store) |
| Scalability | সহজ (যেকোনো server handle করতে পারে) | কঠিন (same server এ যেতে হয়) |
| Failure recovery | সহজ | কঠিন (state হারিয়ে যায়) |
| Example | REST API | WebSocket, FTP sessions |
| JWT | Stateless auth | Session-based auth |

### 💡 Modern Trend
> Modern web apps stateless design এ যাচ্ছে। JWT token use করে stateless authentication। Session state Redis এ store করলেও stateless server রাখা যায়।

---

## 1.13 Horizontal vs Vertical Scaling

### 📖 সংজ্ঞা

**Vertical Scaling (Scale Up):**
- একটা server এর resources বাড়াও (CPU, RAM, SSD)
- Limit আছে — hardware এর limitation
- Generally costly

**Horizontal Scaling (Scale Out):**
- আরো server যোগ করো
- Load Balancer দিয়ে traffic distribute
- Theoretically unlimited
- Cloud এ popular (AWS EC2 Auto Scaling)

### 🏗️ Visual Diagram

```
Vertical Scaling:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Before:                After:
┌──────────────┐       ┌──────────────┐
│   Server     │       │   Server     │
│   4 CPU      │  ──▶  │   32 CPU     │
│   8 GB RAM   │       │   128 GB RAM │
└──────────────┘       └──────────────┘
  Same server, upgraded

Horizontal Scaling:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Before:                After:
                       [Load Balancer]
┌──────────────┐       ┌──────┐ ┌──────┐ ┌──────┐
│   Server 1   │  ──▶  │ S1   │ │ S2   │ │ S3   │
└──────────────┘       └──────┘ └──────┘ └──────┘
  One server         Three servers, load distributed
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 বিস্তারিত তুলনা

| বিষয় | Vertical Scaling | Horizontal Scaling |
|------|-----------------|-------------------|
| Cost | কম (প্রথমে) | বেশি (বেশি server) |
| Complexity | কম | বেশি (load balancer, distribution) |
| Downtime | Yes (upgrade করতে) | No (rolling deploy) |
| Limit | Hardware limit | Unlimited (theoretically) |
| Failure risk | Single point | Multiple instances — safer |
| Use case | Database, legacy apps | Web servers, APIs |
| BD context | Small companies | Product companies |

### 🎤 Interview Explanation
> "Vertical scaling মানে একটা server কে powerful করা, horizontal মানে multiple server। Database usually vertical scale করা হয় (কারণ distributed DB জটিল), কিন্তু web application layer horizontal scale করা হয় load balancer দিয়ে। Modern cloud system এ horizontal scaling prefer করা হয় কারণ এটা fault tolerant।"

### ❓ Follow-up Questions
1. "Database কি horizontally scale করা যায়?"
2. "Auto-scaling কীভাবে কাজ করে?"
3. "Kubernetes কীভাবে horizontal scaling করে?"

---

## 📋 PART 1: Quick Revision Table

| Concept | এক কথায় | Key Point |
|---------|---------|-----------|
| System Design | Blueprint of a system | Architecture plan |
| HLD | Overall architecture | Big picture |
| LLD | Detailed implementation | Class, DB design |
| Scalability | Load handle করার ক্ষমতা | Scale up vs out |
| Reliability | Consistently কাজ করা | No single point of failure |
| Availability | কতটা সময় up থাকে | 99.9% = 3 nines |
| Maintainability | সহজে modify করা | Clean, modular |
| Latency | একটা request এর time | ms |
| Throughput | প্রতি sec এ requests | req/sec |
| CAP Theorem | তিনটার মধ্যে দুইটা | C+P বা A+P |
| Monolithic | সব একসাথে | Simple but hard to scale |
| Microservices | আলাদা আলাদা services | Complex but scalable |
| Stateless | Server state রাখে না | JWT, REST |
| Horizontal Scaling | More servers | Cloud preferred |
| Vertical Scaling | Bigger server | DB common |

---

## 🎯 PART 1: Top 10 Interview Questions with Answers

<details>
<summary><strong>Q1: System Design interview এ কোথা থেকে শুরু করবে?</strong></summary>

**উত্তর:**
System Design interview এ সবসময় এই steps follow করো:

1. **Clarify Requirements** — "এই system এ কতজন user থাকবে? কোন features দরকার?"
2. **Define Scope** — "আমি এই interview এ শুধু core flow design করবো"
3. **Estimate Scale** — "Daily Active Users: 1M, Reads: 10K req/s"
4. **High-Level Architecture** — Component গুলো আঁকো
5. **Deep Dive** — একটা component বিস্তারিত explain করো
6. **Identify Bottlenecks** — "এখানে bottleneck হতে পারে"
7. **Propose Solutions** — Cache, Queue, etc.

</details>

<details>
<summary><strong>Q2: CAP Theorem ব্যবহারিকভাবে explain করো</strong></summary>

**উত্তর:**
Banking system বানাচ্ছি। দুইটা server (Dhaka, Chittagong) এর মধ্যে network connection গেলো:
- **Consistency choose করলে (CP):** Chittagong server request reject করবে (কারণ Dhaka server এর সাথে sync করতে পারছে না)
- **Availability choose করলে (AP):** Chittagong server request serve করবে কিন্তু stale data দিতে পারে

Banking এ CP choose করবো — পুরনো data দিলে disaster। Social media feed এ AP choose করবো — একটু পুরনো post দেখালে সমস্যা নেই।

</details>

<details>
<summary><strong>Q3: Monolith থেকে Microservices এ কীভাবে migrate করবে?</strong></summary>

**উত্তর:**
Strangler Fig Pattern use করবো:
1. নতুন features microservice হিসেবে বানাও
2. Old monolith এর একটা module কে আলাদা করো
3. API Gateway দিয়ে routing করো
4. ধীরে ধীরে পুরো monolith কে microservice এ convert করো

Big bang migration করবো না — too risky।

</details>

<details>
<summary><strong>Q4: High Availability কীভাবে achieve করবে?</strong></summary>

**উত্তর:**
- **Redundancy:** Multiple servers, database replicas
- **Load Balancer:** Traffic distribute করবে
- **Health Checks:** Unhealthy server কে automatic remove করবে
- **Auto-scaling:** Traffic বাড়লে নতুন server start
- **Multi-region deployment:** একটা datacenter down হলে অন্যটা নেবে
- **Circuit Breaker:** Failing service কে isolate করবে

</details>

<details>
<summary><strong>Q5: Latency কমাতে কী করবে?</strong></summary>

**উত্তর:**
- **Caching:** Frequently accessed data Redis এ cache করো
- **CDN:** Static files user এর কাছের server থেকে serve
- **Database indexing:** Query fast করো
- **Async processing:** Heavy tasks queue এ পাঠাও
- **Connection pooling:** DB connection overhead কমাও
- **Compression:** Response data compress করো

</details>

<details>
<summary><strong>Q6: Stateless vs Stateful এর practical example দাও</strong></summary>

**উত্তর:**
- **Stateless REST API + JWT:** প্রতিটা request এ token পাঠাও। Server কোনো session মনে রাখে না। যেকোনো server handle করতে পারে। Scale করা সহজ।
- **Stateful WebSocket:** Real-time chat এ connection open থাকে। Server state রাখে — কোন user কোন room এ। Same server এ থাকতে হয় (sticky session)।

</details>

<details>
<summary><strong>Q7: Horizontal scaling এ কী কী challenges আসে?</strong></summary>

**উত্তর:**
- **Session management:** Stateful হলে সমস্যা (সমাধান: Redis session store)
- **Data consistency:** Multiple servers same time এ write করলে conflict
- **Distributed transactions:** ACID maintain করা কঠিন
- **Service discovery:** Services কীভাবে একে অন্যকে খুঁজে পাবে
- **Increased complexity:** Debugging, monitoring কঠিন

</details>

<details>
<summary><strong>Q8: একটা system কে reliable করতে কী করবে?</strong></summary>

**উত্তর:**
- **Redundancy:** No single point of failure
- **Replication:** Database replica
- **Failover:** Automatic switchover
- **Health checks + Alerts:** Monitoring
- **Graceful degradation:** Core feature চলবে, optional feature বন্ধ
- **Retry logic:** Transient failure এ retry
- **Circuit breaker:** Cascade failure prevent

</details>

<details>
<summary><strong>Q9: Throughput বাড়াতে কী করবে?</strong></summary>

**উত্তর:**
- **Horizontal scaling:** More servers = more throughput
- **Async processing:** Blocking operations এড়াও
- **Batch processing:** Multiple requests একসাথে handle
- **Caching:** Database load কমাও
- **Connection pooling:** Overhead কমাও
- **Message queues:** Peak traffic buffer করো

</details>

<details>
<summary><strong>Q10: LLD আর HLD interview এ কীভাবে handle করবে?</strong></summary>

**উত্তর:**
- **HLD question:** "Design a YouTube clone"
  - Components: Video Upload Service, Encoding Service, CDN, Database, Search
  - Draw architecture diagram
  - Discuss scaling strategy

- **LLD question:** "Design a Parking Lot system"
  - Classes: ParkingLot, ParkingFloor, ParkingSpot, Vehicle, Ticket
  - Relationships: has-a, is-a
  - SOLID principles apply
  - Design Patterns: Strategy (parking fee calculation)

</details>

<div align="right">

[⬆ উপরে যাও](#) | [📚 সূচিপত্র](#) | [PART 2 →](#part2)

</div>

---

<a id="part2"></a>

---

# PART 2: Networking & Communication Basics
### 🌐 System Design এর Communication Layer

> **Interview টিপস:** Networking concepts system design এর backbone। Load Balancer, CDN, API Gateway — এগুলো বুঝলে তুমি যেকোনো architecture diagram explain করতে পারবে।

---

## 2.1 Client-Server Architecture

### 📖 সংজ্ঞা
Client-Server Architecture হলো এমন একটা model যেখানে **Client** (browser, app) **Server** এর কাছে request করে এবং Server response দেয়।

### 🔄 Request-Response Flow

```
Client-Server Communication Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Step 1: User browser এ "www.chaldal.com" type করলো
Step 2: DNS lookup — IP address find করে (e.g., 103.x.x.x)
Step 3: TCP connection establish (3-way handshake)
Step 4: HTTP GET request পাঠালো
Step 5: Server request receive করলো
Step 6: Business logic run করলো (DB query, etc.)
Step 7: HTTP Response পাঠালো (200 OK + HTML/JSON)
Step 8: Browser response render করলো

[Browser] ──GET /products──▶ [DNS] ──resolve──▶ [103.x.x.x]
                                                      │
[Browser] ◀──200 OK + JSON── [Server] ◀──query── [Database]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎯 Types of Clients
| Client Type | Example | Communication |
|------------|---------|--------------|
| Thin Client | Browser | Server এ সব processing |
| Thick Client | Desktop App | কিছু processing locally |
| Mobile Client | Android/iOS App | API call করে |

### ❓ Interview Questions
1. "Client-Server আর Peer-to-Peer এর পার্থক্য?"
2. "Server কি কখনো Client হতে পারে?"
3. "3-tier architecture কী?"

---

## 2.2 HTTP vs HTTPS

### 📖 সংজ্ঞা

**HTTP (HyperText Transfer Protocol):**
- Web এ data transfer এর protocol
- Plain text এ data যায় (unencrypted)
- Port: 80
- ⚠️ Insecure — যে কেউ intercept করতে পারে

**HTTPS (HTTP Secure):**
- HTTP + TLS/SSL encryption
- Data encrypted হয়ে যায়
- Port: 443
- Certificate (SSL/TLS) দরকার

### 🔒 HTTPS কীভাবে কাজ করে?

```
TLS Handshake Process:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Client ──"Hello, আমি এই ciphers support করি"──▶ Server
2. Server ──"OK, এই cipher use করবো + Certificate"──▶ Client
3. Client certificate verify করলো (CA trusted?)
4. Client ──Session key negotiate (encrypted)──▶ Server
5. উভয় পক্ষ same session key দিয়ে encrypt/decrypt করে
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 HTTP Methods

| Method | কাজ | Request Body | Idempotent |
|--------|-----|-------------|-----------|
| GET | Data পড়া | নেই | হ্যাঁ |
| POST | নতুন data তৈরি | আছে | না |
| PUT | পুরো resource update | আছে | হ্যাঁ |
| PATCH | আংশিক update | আছে | না সবসময় |
| DELETE | Resource মুছে ফেলা | নেই সাধারণত | হ্যাঁ |

### 📊 HTTP Status Codes (Must Know!)

| Code Range | মানে | Examples |
|-----------|------|---------|
| 2xx | Success | 200 OK, 201 Created, 204 No Content |
| 3xx | Redirect | 301 Moved, 302 Found, 304 Not Modified |
| 4xx | Client Error | 400 Bad Request, 401 Unauthorized, 403 Forbidden, 404 Not Found, 429 Too Many Requests |
| 5xx | Server Error | 500 Internal Error, 502 Bad Gateway, 503 Service Unavailable, 504 Gateway Timeout |

### 🎤 Interview Explanation
> "HTTP আর HTTPS এর মূল পার্থক্য হলো security। HTTP তে data plain text এ যায় — যে কেউ network intercept করলে দেখতে পারবে। HTTPS এ TLS encryption থাকে — data encrypted। Production সব সময় HTTPS use করতে হবে। Let's Encrypt দিয়ে free SSL certificate পাওয়া যায়।"

### ⚠️ Security Note
```
❌ HTTP তে password পাঠানো:
GET /login?password=abc123   ← Network এ plain text!

✅ HTTPS তে:
POST /login (body: {password: "abc123"}) ← Encrypted!
```

---

## 2.3 REST API

### 📖 সংজ্ঞা
REST (Representational State Transfer) হলো HTTP দিয়ে API design করার একটা **architectural style** — rules এর set।

### 🔑 REST Principles (6টি)

| Principle | মানে |
|-----------|------|
| Client-Server | Client আর Server আলাদা |
| Stateless | Server session রাখে না |
| Cacheable | Response cache করা যায় |
| Uniform Interface | Consistent URL/method |
| Layered System | Client জানে না কয় layer আছে |
| Code on Demand | Optional: server executable code দিতে পারে |

### 📋 RESTful API Design Examples

```python
# E-commerce API Design:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# Products CRUD:
GET    /api/v1/products           # সব product list
GET    /api/v1/products/{id}      # একটা product
POST   /api/v1/products           # নতুন product তৈরি
PUT    /api/v1/products/{id}      # পুরো product update
PATCH  /api/v1/products/{id}      # আংশিক update
DELETE /api/v1/products/{id}      # product delete

# Nested Resources:
GET    /api/v1/orders/{id}/items  # order এর items
POST   /api/v1/users/{id}/address # user এর address যোগ

# Query Parameters:
GET /api/v1/products?category=electronics&sort=price&page=1&limit=20

# Response Format:
{
    "status": "success",
    "data": {
        "id": 1,
        "name": "Samsung TV",
        "price": 45000
    },
    "meta": {
        "total": 150,
        "page": 1,
        "limit": 20
    }
}
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 REST Best Practices

| Practice | ✅ করো | ❌ করো না |
|----------|--------|---------|
| Nouns use করো | /products | /getProducts |
| Plural use করো | /users | /user |
| Version করো | /api/v1/ | /api/ |
| HTTP methods ঠিকমতো | GET for read | GET for delete |
| Proper status codes | 201 for created | 200 for everything |
| Meaningful error messages | {error: "User not found"} | {error: "Error"} |

### 🎤 Interview Explanation
> "REST API হলো HTTP দিয়ে data exchange করার একটা standard approach। URL এ noun use করি (resource), HTTP method দিয়ে action বলি। Stateless মানে server প্রতিটা request কে independent treat করে — authentication token প্রতিটা request এ পাঠাতে হয়।"

### ❓ Interview Questions
1. "REST API কে stateless বলার কারণ কী?"
2. "PUT আর PATCH এর পার্থক্য?"
3. "API versioning কেন করা উচিত?"
4. "Idempotent মানে কী?"

> **Memory Tip:** "REST = Resource + HTTP Methods (CRUD operations mapped to GET/POST/PUT/PATCH/DELETE)"

---

## 2.4 GraphQL Basics

### 📖 সংজ্ঞা
GraphQL হলো Facebook এর তৈরি API query language — client নিজেই decide করে কোন data চাই, কতটা চাই।

### 🔄 REST vs GraphQL তুলনা

```
REST এ Over-fetching সমস্যা:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
GET /users/1
Response: {
    id: 1, name: "Rahim", email: "...",
    phone: "...", address: {...},  ← তোমার দরকার নেই
    orders: [...],                  ← তোমার দরকার নেই
    preferences: {...}              ← তোমার দরকার নেই
}
শুধু name দরকার ছিল, সব data এলো!

GraphQL এ:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
query {
    user(id: 1) {
        name         ← শুধু name চাই
    }
}
Response: { "data": { "user": { "name": "Rahim" } } }
```

### 📊 REST vs GraphQL

| বিষয় | REST | GraphQL |
|------|------|---------|
| Endpoint | Multiple (/users, /posts) | Single (/graphql) |
| Data fetching | Fixed response | Client controlled |
| Over-fetching | Problem আছে | নেই |
| Under-fetching | Multiple calls লাগে | একটাই query |
| Learning curve | কম | বেশি |
| Caching | HTTP caching সহজ | জটিল |
| Use case | Simple CRUD | Complex data relationships |
| BD Interview | বেশি জিজ্ঞেস করে | Concept level জানলেই হবে |

### 🎤 Interview Explanation
> "GraphQL REST এর under-fetching আর over-fetching সমস্যা solve করে। Client exactly কোন data চাই সেটা specify করতে পারে। একটাই endpoint থেকে যেকোনো data। কিন্তু simple CRUD app এ REST ই যথেষ্ট, GraphQL এর complexity নেওয়ার দরকার নেই।"

---

## 2.5 WebSocket

### 📖 সংজ্ঞা
WebSocket হলো **full-duplex, persistent connection** যেখানে client এবং server উভয়েই যেকোনো সময় message পাঠাতে পারে।

### 🔄 HTTP vs WebSocket

```
HTTP (Request-Response):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Client ──request──▶ Server ──response──▶ Client
Connection close
Client ──request──▶ Server ──response──▶ Client
Connection close (আবার)

WebSocket (Persistent Connection):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Client ──WebSocket handshake──▶ Server
[Connection stays open]
Client ──message──▶ Server
Server ──message──▶ Client  (server pushed!)
Client ──message──▶ Server
[Both can send anytime]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎯 Use Cases
- Real-time chat (WhatsApp web)
- Live notifications
- Online games
- Stock price updates
- Live collaboration (Google Docs)
- Live sports score

### 💻 Code Example (Python)
```python
# WebSocket Server (FastAPI):
from fastapi import WebSocket

@app.websocket("/ws/chat/{room_id}")
async def websocket_endpoint(websocket: WebSocket, room_id: str):
    await websocket.accept()
    try:
        while True:
            data = await websocket.receive_text()
            # Broadcast to all users in room
            await broadcast_to_room(room_id, data)
    except WebSocketDisconnect:
        await handle_disconnect(room_id)
```

### 📊 HTTP Polling vs WebSocket

| Method | Description | Latency | Server Load |
|--------|-------------|---------|-------------|
| Short Polling | প্রতি X সেকেন্ডে request | High | High |
| Long Polling | Server response hold করে | Medium | Medium |
| WebSocket | Persistent connection | Low | Efficient |
| SSE | Server → Client only | Low | Low |

### 🎤 Interview Explanation
> "WebSocket use করি যখন real-time bidirectional communication দরকার। Chat app এ HTTP polling use করলে প্রতি সেকেন্ডে request যাবে — server এ load বেশি, latency বেশি। WebSocket এ একটা connection open থাকে, server যেকোনো সময় push করতে পারে। Chat, notification, live update — এই সব এ WebSocket।"

---

## 2.6 TCP vs UDP

### 📖 সংজ্ঞা

**TCP (Transmission Control Protocol):**
- Reliable, ordered, error-checked delivery
- Connection-oriented (3-way handshake)
- Slower কিন্তু guaranteed delivery

**UDP (User Datagram Protocol):**
- Unreliable, unordered delivery
- Connectionless
- Faster কিন্তু no guarantee

### 🔄 TCP 3-Way Handshake

```
TCP Connection Establishment:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Client                          Server
   │                               │
   │──── SYN (connect করতে চাই) ──▶│
   │                               │
   │◀─ SYN-ACK (ok, তৈরি আছি) ───│
   │                               │
   │──── ACK (ধন্যবাদ, শুরু করি) ─▶│
   │                               │
   │     [Data Transfer]           │
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 TCP vs UDP তুলনা

| বিষয় | TCP | UDP |
|------|-----|-----|
| Connection | Connection-oriented | Connectionless |
| Reliability | Guaranteed delivery | No guarantee |
| Order | Ordered | Unordered |
| Speed | Slower | Faster |
| Header size | 20 bytes | 8 bytes |
| Use case | HTTP, Email, File Transfer | Video streaming, Gaming, DNS |
| Error checking | Yes (checksum + ACK) | Yes (checksum only) |
| Flow control | Yes | No |

### 🎯 Real-Life Analogy
> **TCP:** Registered mail — confirmation পাও যে চিঠি পৌঁছেছে। হারিয়ে গেলে আবার পাঠানো হয়।
> 
> **UDP:** Normal mail — ফেলে দাও, পৌঁছালো কিনা জানো না। কিন্তু দ্রুত।

### 🎤 Interview Explanation
> "TCP reliable কিন্তু UDP fast। HTTP, HTTPS, database connections — সব TCP use করে কারণ data loss হলে problem। কিন্তু video streaming এ UDP use করি — একটা frame miss গেলে wait করার চেয়ে পরের frame দেখানো ভালো। DNS query তে UDP — fast response দরকার, packet ছোট।"

---

## 2.7 DNS (Domain Name System)

### 📖 সংজ্ঞা
DNS হলো internet এর **phone book** — human-readable domain name (google.com) কে machine-readable IP address (142.250.x.x) এ convert করে।

### 🔄 DNS Resolution Flow

```
DNS Lookup Process:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Browser: "chaldal.com এর IP কী?"

1. Browser Cache check করে → নেই
2. OS Cache (hosts file) check করে → নেই
3. Recursive DNS Resolver (ISP এর) কে জিজ্ঞেস করে
4. Resolver → Root DNS Server: ".com কার কাছে?"
5. Root → Resolver: "TLD Server এর কাছে যাও"
6. Resolver → TLD Server (.com): "chaldal.com কার কাছে?"
7. TLD → Resolver: "chaldal এর Authoritative DNS"
8. Resolver → Authoritative DNS: "chaldal.com এর IP?"
9. Authoritative → Resolver: "103.x.x.x" (TTL সহ)
10. Resolver → Browser: "103.x.x.x" (cache করে রাখে TTL পর্যন্ত)

Total time: ~100ms (first time), ~0ms (cached)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 DNS Record Types

| Record Type | কাজ | Example |
|------------|-----|---------|
| A | Domain → IPv4 | chaldal.com → 103.x.x.x |
| AAAA | Domain → IPv6 | chaldal.com → 2001:xxxx |
| CNAME | Domain → Domain | www → chaldal.com |
| MX | Mail server | chaldal.com → mail.google.com |
| TXT | Text info | SPF, DKIM records |
| NS | Nameserver | chaldal.com → ns1.cloudflare.com |

### 🎯 Real-Life Analogy
> ফোনবুকের মতো — তুমি "Rahim" এর নাম জানো, DNS তোমাকে তার phone number (IP) বলে দেয়।

### ❓ Interview Questions
1. "DNS caching কীভাবে কাজ করে? TTL কী?"
2. "DNS কি কখনো security threat হতে পারে? (DNS Spoofing)"
3. "www.domain.com আর domain.com এর DNS কীভাবে আলাদা configure করে?"

---

## 2.8 CDN (Content Delivery Network)

### 📖 সংজ্ঞা
CDN হলো globally distributed servers যারা **user এর কাছের location থেকে content serve করে** — latency কমায়, speed বাড়ায়।

### 🌍 CDN Architecture

```
CDN Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Origin Server — Dhaka]
        │
        ├──▶ [CDN PoP — Singapore] ← দক্ষিণ-পূর্ব এশিয়া users
        ├──▶ [CDN PoP — Mumbai] ← ভারত users
        ├──▶ [CDN PoP — London] ← Europe users
        └──▶ [CDN PoP — New York] ← US users

BD User → requests image → nearest CDN (Singapore) serves it
Without CDN: BD User → Dhaka Origin server (same place, slow if overloaded)
With CDN: BD User → Singapore CDN (~20ms) vs US User → NY CDN (~5ms)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎯 CDN কী Cache করে?
- Static files: Images, CSS, JavaScript, fonts
- Video content (YouTube-এর edge servers)
- HTML pages (JAMstack sites)
- API responses (sometimes)

### 📊 CDN Benefits

| Benefit | Description |
|---------|-------------|
| Faster load time | User এর কাছের server |
| Reduced server load | Origin server এ pressure কম |
| DDoS protection | Distributed — attack absorb করে |
| Global reach | যেকোনো location এ fast |
| Bandwidth saving | Origin থেকে কম traffic |

### 🎤 Interview Explanation
> "CDN use করি কারণ static files (images, JS, CSS) origin server থেকে serve করলে latency বেশি হয়। CDN globally distributed servers রাখে — user এর কাছের server থেকে content serve হয়। Cloudflare, AWS CloudFront popular CDN providers। e-commerce site এ product images CDN থেকে serve করলে page load অনেক fast হয়।"

---

## 2.9 Load Balancer

### 📖 সংজ্ঞা
Load Balancer হলো এমন একটা component যা incoming traffic কে **multiple servers এ distribute করে** — কোনো একটা server overloaded হয় না।

### 🏗️ Load Balancer Architecture

```
Load Balancer Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
User Requests (10,000 req/sec)
              │
       [Load Balancer]
       ┌──────┼──────┐
       ▼      ▼      ▼
   [Server1] [Server2] [Server3]
   (33% load)(33% load)(33% load)
       │      │       │
       └──────┴───────┘
              │
          [Database]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Load Balancing Algorithms

| Algorithm | কাজ | কখন Use |
|-----------|-----|---------|
| Round Robin | পালাক্রমে প্রতিটা server | সব server সমান |
| Weighted RR | বেশি powerful server এ বেশি | Servers আলাদা spec |
| Least Connections | কম active connection এ | Unequal processing time |
| IP Hash | Same IP → Same server | Session affinity দরকার |
| Random | যেকোনো server randomly | Simple setup |

### 🔑 Layer 4 vs Layer 7 Load Balancer

```
Layer 4 (Transport Layer):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
- TCP/UDP level routing
- Fast, low overhead
- Content দেখে না
- Example: AWS NLB

Layer 7 (Application Layer):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
- HTTP header, URL দেখে routing করে
- URL-based routing:
  /api/* → API servers
  /images/* → Image servers
  /admin/* → Admin servers
- More intelligent
- Example: AWS ALB, Nginx
```

### 🎤 Interview Explanation
> "Load Balancer traffic distribute করে multiple servers এ। Round Robin সবচেয়ে simple — একটার পর একটা। কিন্তু servers যদি আলাদা powerful হয় তাহলে Weighted Round Robin। Sticky session দরকার হলে IP Hash। Layer 7 load balancer content দেখে route করে — /api requests আলাদা server এ, /static images আলাদা server এ।"

### ❓ Interview Questions
1. "Load Balancer নিজেই fail করলে কী হবে? (Single point of failure?)"
2. "Health check কীভাবে কাজ করে?"
3. "Sticky session কী এবং কেন দরকার?"

---

## 2.10 Reverse Proxy

### 📖 সংজ্ঞা
Reverse Proxy হলো এমন একটা server যা client এর request receive করে এবং backend server এ forward করে — client সরাসরি backend দেখতে পায় না।

### 🔄 Forward Proxy vs Reverse Proxy

```
Forward Proxy:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Client] → [Forward Proxy] → [Internet/Server]
Client এর পক্ষে request করে
(VPN, corporate proxy)

Reverse Proxy:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Client] → [Reverse Proxy] → [Backend Servers]
Server এর পক্ষে response দেয়
(Nginx, Apache as reverse proxy)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎯 Reverse Proxy Benefits
- **Security:** Backend IP hide করে
- **SSL Termination:** HTTPS decrypt করে backend এ HTTP পাঠায়
- **Load Balancing:** Multiple backend এ distribute
- **Caching:** Static content cache করে
- **Compression:** Response compress করে
- **Request routing:** URL based routing

### 💻 Nginx Reverse Proxy Config
```nginx
# Nginx as Reverse Proxy for Django/FastAPI:
server {
    listen 80;
    server_name chaldal.com;
    
    location /api/ {
        proxy_pass http://localhost:8000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
    
    location /static/ {
        root /var/www/html;  # Direct file serve
    }
}
```

---

## 2.11 API Gateway

### 📖 সংজ্ঞা
API Gateway হলো microservices system এ **single entry point** — সব client request আসে API Gateway তে, সে appropriate service এ route করে।

### 🏗️ API Gateway Architecture

```
API Gateway Pattern:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Mobile App]  [Web Browser]  [Third-party]
      │              │              │
      └──────────────┴──────────────┘
                     │
              [API Gateway]
              ┌──────────────────────────────┐
              │ Authentication               │
              │ Rate Limiting               │
              │ Request Routing             │
              │ Load Balancing              │
              │ Logging & Monitoring        │
              │ Protocol Translation        │
              └──────────────────────────────┘
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
    [User Service] [Order]  [Payment]
                  [Service] [Service]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 API Gateway Features

| Feature | কাজ |
|---------|-----|
| Authentication | JWT/API Key verify |
| Authorization | Permission check |
| Rate Limiting | Abuse prevent |
| Request Routing | Correct service এ পাঠায় |
| Load Balancing | Traffic distribute |
| SSL Termination | HTTPS handle |
| Logging | সব request log |
| Circuit Breaker | Failing service protect |
| Caching | Response cache |
| Protocol Translation | REST → gRPC |

### 🎤 Interview Explanation
> "API Gateway microservices এর front door। সব request এখান দিয়ে আসে — authentication এখানেই হয়, প্রতিটা service কে আলাদাভাবে authentication করতে হয় না। Rate limiting এখানে করলে abuse prevent হয়। Kong, AWS API Gateway, Nginx — popular API Gateway tools।"

---

## 2.12 Authentication vs Authorization

### 📖 সংজ্ঞা

**Authentication (প্রমাণীকরণ):** তুমি কে? Identity verify করা।
**Authorization (অনুমোদন):** তুমি কী করতে পারবে? Permission check করা।

### 🎯 Real-Life Analogy
> কনসার্টে যাওয়ার কথা ভাবো:
> - **Authentication:** দরজায় ticket দেখানো (তুমি কে, ticket valid কিনা)
> - **Authorization:** VIP area তে ঢুকতে পারবে কিনা (কী permission আছে)

### 🔄 Flow Diagram

```
Auth Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. User login করলো (email + password)
   ↓
2. Authentication: Password hash verify করলো
   ↓
3. Token issue করলো (JWT)
   ↓
4. User /admin/dashboard request করলো (JWT সহ)
   ↓
5. Authentication check: JWT valid? ✅
   ↓
6. Authorization check: user এর role "admin"? ✅/❌
   ↓
7. Access grant অথবা 403 Forbidden
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Authentication Methods

| Method | কীভাবে | Example |
|--------|--------|---------|
| Basic Auth | username:password base64 | Internal tools |
| Session-based | Server এ session store | Traditional web |
| Token-based (JWT) | Stateless token | Modern APIs |
| OAuth 2.0 | Third-party auth | "Login with Google" |
| API Key | Static key | Third-party APIs |
| MFA | Multiple factors | Banking |

---

## 2.13 JWT (JSON Web Token)

### 📖 সংজ্ঞা
JWT হলো **compact, self-contained token** যা user information এবং claims নিরাপদে represent করে।

### 🔑 JWT Structure

```
JWT = Header.Payload.Signature

Example JWT:
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.
eyJ1c2VyX2lkIjoxMjMsInJvbGUiOiJhZG1pbiIsImV4cCI6MTcxODk1MDQwMH0.
SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Header (Base64 decoded):
{
    "alg": "HS256",    ← Algorithm
    "typ": "JWT"       ← Type
}

Payload (Base64 decoded):
{
    "user_id": 123,
    "role": "admin",
    "exp": 1718950400,  ← Expiry timestamp
    "iat": 1718864000   ← Issued at
}

Signature:
HMACSHA256(
    base64UrlEncode(header) + "." + base64UrlEncode(payload),
    secret_key
)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔄 JWT Flow

```
JWT Authentication Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. POST /login {email, password}
         ↓
2. Server: password verify করলো ✅
         ↓
3. Server: JWT token generate করলো
         ↓
4. Response: {token: "eyJ..."}
         ↓
5. Client: token localStorage/cookie তে save করলো
         ↓
6. GET /profile
   Authorization: Bearer eyJ...
         ↓
7. Server: JWT verify করলো (signature + expiry)
         ↓
8. Response: user profile data
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 💻 JWT Implementation (Python)
```python
import jwt
from datetime import datetime, timedelta

SECRET_KEY = "your-secret-key"  # Environment variable এ রাখো!

# Token Generate:
def generate_token(user_id: int, role: str) -> str:
    payload = {
        "user_id": user_id,
        "role": role,
        "exp": datetime.utcnow() + timedelta(hours=24),
        "iat": datetime.utcnow()
    }
    return jwt.encode(payload, SECRET_KEY, algorithm="HS256")

# Token Verify:
def verify_token(token: str) -> dict:
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=["HS256"])
        return payload
    except jwt.ExpiredSignatureError:
        raise Exception("Token expired")
    except jwt.InvalidTokenError:
        raise Exception("Invalid token")
```

### 📊 JWT vs Session-based Auth

| বিষয় | JWT (Stateless) | Session (Stateful) |
|------|-----------------|-------------------|
| Server storage | কিছু store করে না | Session DB/Memory |
| Scalability | সহজ (stateless) | কঠিন (shared session store) |
| Token revoke | কঠিন (expiry পর্যন্ত valid) | সহজ (session delete) |
| Performance | Fast (no DB lookup) | DB/Cache lookup দরকার |
| Token size | Larger | Small (session ID) |
| Security | Payload visible (but signed) | Server side only |

### ⚠️ JWT Security Best Practices
```
✅ করো:
- Short expiry time (15min - 24hr)
- Refresh token use করো
- HTTPS only
- Secret key environment variable এ রাখো
- Algorithm explicitly specify করো

❌ করো না:
- Secret data payload এ রেখো না (visible!)
- "none" algorithm accept করো না
- Long lived tokens
- localStorage (XSS vulnerable) — httpOnly cookie better
```

### 🎤 Interview Explanation
> "JWT stateless authentication এর জন্য ideal। Server কিছু store করে না — token এ ই সব information আছে। Signature দিয়ে verify করা যায়। কিন্তু একটা সমস্যা — token revoke করা কঠিন, expiry পর্যন্ত valid থাকে। সমাধান হলো short expiry (15min) + refresh token। Sensitive data payload এ রাখবো না কারণ base64 decoded করলে দেখা যায়।"

---

## 2.14 Session Management

### 📖 সংজ্ঞা
Session Management হলো user এর **login state maintain করার mechanism** — user কোন request করলে server বুঝতে পারে এটা authenticated user।

### 🔄 Session-based Auth Flow

```
Session Authentication Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. POST /login {email, password}
         ↓
2. Server: credentials verify করলো
         ↓
3. Server: Session তৈরি করলো → Session DB তে store
   Session: {session_id: "abc123", user_id: 456, role: "user"}
         ↓
4. Response: Set-Cookie: session_id=abc123; HttpOnly; Secure
         ↓
5. Client: cookie automatically save করলো
         ↓
6. GET /dashboard
   Cookie: session_id=abc123
         ↓
7. Server: Session DB তে session_id lookup করলো
   Found: user_id=456, role="user"
         ↓
8. Response: dashboard data
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Session Storage Options

| Storage | Description | Use Case |
|---------|-------------|---------|
| In-memory (server RAM) | Fast, সহজ | Single server, dev |
| Database | Persistent | Production (slow) |
| Redis | Fast + Persistent | Production (recommended) |
| Distributed Cache | Multiple server shared | Horizontal scaled |

### 🔑 Cookie Security Attributes

```
Set-Cookie: session_id=abc123; 
    HttpOnly;       ← JavaScript access করতে পারবে না (XSS protect)
    Secure;         ← HTTPS only
    SameSite=Strict ← CSRF protect
    Max-Age=86400;  ← 24 hour expiry
    Path=/;
```

### 🎤 Interview Explanation
> "Session-based auth এ server session store করে — প্রতিটা request এ session ID check করে। এটা JWT এর চেয়ে revoke করা সহজ — session delete করলেই logout। কিন্তু horizontal scaling এ problem — server 1 এর session server 2 এ নেই। সমাধান: Redis shared session store।"

---

## 📋 PART 2: Quick Revision Table

| Concept | এক কথায় | Key Point |
|---------|---------|-----------|
| Client-Server | Request-Response model | Client requests, server responds |
| HTTP | Web protocol | Port 80, plain text |
| HTTPS | Secure HTTP | Port 443, TLS encrypted |
| REST API | HTTP-based API style | Stateless, resource-based URLs |
| GraphQL | Query language for API | Client specifies exact data |
| WebSocket | Persistent connection | Full-duplex, real-time |
| TCP | Reliable protocol | 3-way handshake, guaranteed |
| UDP | Fast protocol | No guarantee, streaming |
| DNS | Domain → IP | Distributed phone book |
| CDN | Distributed content serving | Nearest server, fast |
| Load Balancer | Traffic distribution | Round robin, least connections |
| Reverse Proxy | Server-side proxy | Nginx, security, SSL termination |
| API Gateway | Microservice entry point | Auth, routing, rate limiting |
| Authentication | তুমি কে? | Identity verification |
| Authorization | তুমি কী করতে পারো? | Permission check |
| JWT | Stateless token | Header.Payload.Signature |
| Session | Server-side state | Cookie + Session DB |

---

## 🎯 PART 2: Top 15 Interview Questions with Answers

<details>
<summary><strong>Q1: HTTP আর HTTPS এর পার্থক্য বলো</strong></summary>

**উত্তর:**
HTTP port 80 তে কাজ করে, data plain text এ যায় — যে কেউ intercept করতে পারে। HTTPS port 443, TLS encryption — data encrypted। Production এ সবসময় HTTPS। SSL certificate (Let's Encrypt free) দরকার। TLS Handshake এ client-server session key negotiate করে।

</details>

<details>
<summary><strong>Q2: REST API design করার best practices কী?</strong></summary>

**উত্তর:**
1. Nouns use করো URL এ (products, না getProducts)
2. HTTP methods ঠিকমতো (GET read, POST create, PUT/PATCH update, DELETE)
3. Proper status codes (201 for created, 404 for not found)
4. API versioning (/api/v1/)
5. Pagination (page, limit params)
6. Meaningful error messages
7. HTTPS only
8. Authentication (JWT/API Key)
9. Rate limiting
10. Documentation (Swagger/OpenAPI)

</details>

<details>
<summary><strong>Q3: WebSocket কখন use করবে, কখন HTTP polling?</strong></summary>

**উত্তর:**
WebSocket use করো:
- Real-time chat (বার্তা instant দরকার)
- Live notifications
- Online gaming (low latency দরকার)
- Live stock prices
- Collaborative editing

HTTP Polling use করো:
- Data rarely changes (প্রতি 30 sec এ check)
- Simple implementation দরকার
- WebSocket support নেই (rare)

Short Polling > Long Polling > WebSocket (complexity ও performance এর tradeoff)

</details>

<details>
<summary><strong>Q4: Load Balancer single point of failure হলে কী করবে?</strong></summary>

**উত্তর:**
Active-Active Load Balancer redundancy:
- দুইটা LB চলবে simultaneously
- Virtual IP (Keepalived/VRRP) use করবো
- একটা fail করলে অন্যটা Virtual IP নেবে
- DNS level এ multiple LB IP রাখা যায়
- AWS এ ALB/NLB managed service — AWS handle করে

</details>

<details>
<summary><strong>Q5: JWT এর সমস্যা কী এবং কীভাবে solve করবে?</strong></summary>

**উত্তর:**
**সমস্যা 1 — Token revoke করা যায় না:**
সমাধান: Short expiry (15min) + Refresh Token (7 days)। Logout এ refresh token blacklist করো (Redis এ)।

**সমস্যা 2 — Payload visible:**
সমাধান: Sensitive data রাখবো না। শুধু user_id, role, expiry।

**সমস্যা 3 — Token stolen:**
সমাধান: HttpOnly Cookie তে store করো (না localStorage)। HTTPS only।

</details>

<details>
<summary><strong>Q6: CDN কীভাবে dynamic content serve করে?</strong></summary>

**উত্তর:**
CDN মূলত static content এর জন্য। Dynamic content এর জন্য:
- Edge Computing (Cloudflare Workers) — CDN node এই code run হয়
- API response cache করা (short TTL দিয়ে)
- Surrogate keys — specific content invalidate করা
- Cache-Control headers দিয়ে caching behavior control

Full dynamic content (personalized) CDN bypass করে origin server থেকে আসে।

</details>

<details>
<summary><strong>Q7: DNS lookup কীভাবে speed করবে?</strong></summary>

**উত্তর:**
- TTL (Time to Live) optimize করো — বেশি TTL মানে বেশি cache
- DNS prefetching: `<link rel="dns-prefetch" href="//api.example.com">`
- Anycast routing (Cloudflare DNS 1.1.1.1 use করে)
- Local DNS resolver cache করে
- Reduce DNS lookups — third-party resources কম করো

</details>

<details>
<summary><strong>Q8: API Gateway আর Load Balancer এর পার্থক্য কী?</strong></summary>

**উত্তর:**
| | API Gateway | Load Balancer |
|--|--|--|
| কাজ | Auth, routing, rate limit, transform | Traffic distribute |
| Layer | Application (L7) | L4 বা L7 |
| Intelligence | High (content-aware) | Medium/Low |
| Use case | Microservices | Any backend |
| Cost | Higher | Lower |

API Gateway = smart traffic manager। Load Balancer = traffic distributor।
Microservices এ: Client → API Gateway → Load Balancer → Services।

</details>

<details>
<summary><strong>Q9: Rate Limiting কীভাবে implement করবে?</strong></summary>

**উত্তর:**
Algorithms:
1. **Fixed Window:** প্রতি minute এ max 100 requests
2. **Sliding Window:** Last 60 seconds এ 100 requests
3. **Token Bucket:** Tokens refill হয়, burst allow করে
4. **Leaky Bucket:** Fixed rate এ process

Implementation:
```python
# Redis দিয়ে Rate Limiting:
import redis
r = redis.Redis()

def rate_limit(user_id: str, limit: int = 100) -> bool:
    key = f"rate:{user_id}:{int(time.time() / 60)}"
    count = r.incr(key)
    r.expire(key, 60)
    return count <= limit
```

API Gateway level এ করলে সব service এ আলাদা implement করতে হয় না।

</details>

<details>
<summary><strong>Q10: Session hijacking কী এবং কীভাবে prevent করবে?</strong></summary>

**উত্তর:**
Session Hijacking: attacker session ID চুরি করে user হিসেবে act করে।

Prevention:
- HttpOnly cookie (JS access করতে পারবে না)
- Secure flag (HTTPS only)
- SameSite=Strict (CSRF prevent)
- Short session expiry
- Regenerate session ID after login
- HTTPS everywhere
- IP binding (session কে IP এ bind)

</details>

<details>
<summary><strong>Q11: TCP 3-way handshake কেন দরকার?</strong></summary>

**উত্তর:**
3-way handshake দুই পক্ষই নিশ্চিত হয়:
1. SYN: "আমি connect করতে চাই" — Client alive এবং send করতে পারছে
2. SYN-ACK: "OK" — Server alive, receive ও send করতে পারছে
3. ACK: "ধন্যবাদ" — Client alive এবং receive করতে পারছে

এছাড়া sequence numbers exchange হয় — data order maintain করতে। Bidirectional communication এর foundation।

</details>

<details>
<summary><strong>Q12: Reverse Proxy কেন use করবে সরাসরি server expose না করে?</strong></summary>

**উত্তর:**
- **Security:** Backend IP, port hide করে
- **SSL Termination:** HTTPS Nginx handle করে, backend HTTP
- **Caching:** Static files cache করে backend এর load কমায়
- **Compression:** gzip compression
- **Request filtering:** Malicious request block
- **Load Distribution:** Multiple backend এ route করে
- **Logging:** Centralized access logs

Nginx সবচেয়ে popular — configuration সহজ, performance excellent।

</details>

<details>
<summary><strong>Q13: OAuth 2.0 কীভাবে কাজ করে?</strong></summary>

**উত্তর:**
"Login with Google" flow:
1. User "Login with Google" click করলো
2. App → Google authorization server
3. User Google এ login করলো + permission দিলো
4. Google → App কে Authorization Code দিলো
5. App → Google: Code exchange করে Access Token নিলো
6. App → Google API: Access Token দিয়ে user info নিলো
7. App নিজের JWT issue করলো

OAuth 2.0 authorization framework, OpenID Connect তার উপর authentication layer।

</details>

<details>
<summary><strong>Q14: GraphQL এ N+1 problem কী?</strong></summary>

**উত্তর:**
```graphql
query {
    users {        ← 1 DB query
        orders {   ← N DB queries (প্রতি user এর জন্য)
            total
        }
    }
}
```
100 users → 101 DB queries! (1 + 100)

Solution: DataLoader (batch + cache):
```python
# DataLoader: N queries → 1 batch query
async def batch_load_orders(user_ids):
    return await db.query(
        "SELECT * FROM orders WHERE user_id IN (?)", user_ids
    )
```

</details>

<details>
<summary><strong>Q15: HTTP/2 আর HTTP/1.1 এর পার্থক্য কী?</strong></summary>

**উত্তর:**
| | HTTP/1.1 | HTTP/2 |
|--|--|--|
| Connections | Multiple connections | Single connection |
| Multiplexing | নেই (HOL blocking) | আছে (parallel streams) |
| Headers | Text, repeated | Binary, compressed (HPACK) |
| Server Push | নেই | আছে |
| Performance | Slow | 2-3x faster |

HTTP/2 এ একটা connection এ multiple request simultaneously চলে — HTTP/1.1 এ queue হয়ে থাকে।

</details>

---

## 🔥 Rapid Fire Q&A — PART 1 & 2

| প্রশ্ন | উত্তর |
|--------|--------|
| HTTP default port? | 80 |
| HTTPS default port? | 443 |
| WebSocket default port? | 80 (WS), 443 (WSS) |
| JWT কয় ভাগে? | ৩ ভাগ (Header.Payload.Signature) |
| CAP এর P মানে? | Partition Tolerance |
| REST stateless মানে? | Server session রাখে না |
| CDN কী cache করে? | Static files (images, CSS, JS) |
| 404 status code মানে? | Not Found |
| 503 status code মানে? | Service Unavailable |
| DNS এর কাজ কী? | Domain → IP resolution |
| Load balancer algorithm default? | Round Robin |
| JWT এ sensitive data রাখা যাবে? | না (visible) |
| TCP vs UDP — কোনটা reliable? | TCP |
| Monolith এর সুবিধা? | Simple, easy to develop |
| Microservice এর সুবিধা? | Independent scaling |
| 5 nines availability মানে? | 99.999% |
| CAP তে banking কোনটা choose করবে? | CP |
| Horizontal scaling এর সুবিধা? | Unlimited, fault tolerant |
| API Gateway এর কাজ? | Auth, routing, rate limit |
| Reverse Proxy example? | Nginx, Apache |

---

<div align="right">

[⬆ উপরে যাও](#) | [📚 সূচিপত্র](#) | [PART 3 →](#part3)

</div>

---



<a id="part3"></a>

---

# PART 3: Database Design in System Design
### 🗄️ System এ Database এর ভূমিকা

> **Interview টিপস:** System Design interview এ database নিয়ে সবচেয়ে বেশি প্রশ্ন আসে। "কোন database use করবে এবং কেন?" — এই প্রশ্নের confident উত্তর দিতে পারলে interviewer impressed হবে।

---

## 3.1 SQL vs NoSQL

### 📖 সংজ্ঞা

**SQL (Relational Database):**
- Structured data, predefined schema
- Tables, rows, columns
- ACID compliance
- Complex queries, JOINs support
- উদাহরণ: MySQL, PostgreSQL, SQLite, SQL Server

**NoSQL (Non-Relational Database):**
- Flexible/dynamic schema
- Various data models (document, key-value, column, graph)
- Eventually consistent (mostly)
- Horizontal scaling সহজ
- উদাহরণ: MongoDB, Redis, Cassandra, DynamoDB, Neo4j

### 📊 বিস্তারিত তুলনা

| বিষয় | SQL | NoSQL |
|------|-----|-------|
| Schema | Fixed, predefined | Flexible, dynamic |
| Data model | Tables & rows | Documents, K-V, Column, Graph |
| Relationships | JOINs (strong) | Embedded/denormalized |
| ACID | ✅ Full support | ⚠️ Varies (some support) |
| Scaling | Vertical (mostly) | Horizontal (easy) |
| Query language | SQL (standardized) | Varies per DB |
| Performance | Complex queries ভালো | Simple, high-volume reads ভালো |
| Maturity | দীর্ঘদিনের, proven | তুলনামূলক নতুন |
| Use case | Financial, ERP, CRM | Real-time, Big Data, Cache |
| BD Junior interviews | বেশি জিজ্ঞেস করে | Concept জানলেই হবে |

### 🎯 NoSQL Types

```
NoSQL Database Types:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Document Store (MongoDB):
   {
     "_id": "123",
     "name": "Rahim",
     "orders": [
       {"item": "Rice", "qty": 2},
       {"item": "Dal", "qty": 1}
     ]
   }
   Use: CMS, E-commerce, User profiles

2. Key-Value (Redis, DynamoDB):
   "user:123" → "{name: Rahim, role: admin}"
   Use: Cache, Session, Real-time leaderboard

3. Column Family (Cassandra, HBase):
   Row key → Multiple columns per family
   Use: Time-series, IoT, Analytics

4. Graph (Neo4j):
   Nodes + Edges + Properties
   Use: Social networks, Fraud detection, Recommendations
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎯 Database Selection Strategy

```
Decision Tree — কোন Database বেছে নেবে?
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Data কি structured এবং relationships complex?
    → YES: SQL (PostgreSQL / MySQL)

Data কি document-based এবং schema flexible?
    → YES: MongoDB

High-speed key-value access দরকার (cache)?
    → YES: Redis

Massive write throughput, time-series, IoT?
    → YES: Cassandra

Graph-based relationships (social network)?
    → YES: Neo4j

Fully managed, serverless, AWS ecosystem?
    → YES: DynamoDB
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎤 Interview Explanation
> "SQL vs NoSQL একটা trade-off। আমি সবসময় SQL দিয়ে শুরু করি — data যদি structured হয়, relationships complex হয়, financial data হয়। NoSQL choose করি যখন schema flexible দরকার, horizontal scale দরকার, বা write throughput অনেক বেশি। MongoDB document store, Redis cache এর জন্য — দুটোই আলাদা purpose।"

### ⚠️ Common Mistakes
- "NoSQL মানেই fast, SQL মানেই slow" — ভুল। Context নির্ভর।
- NoSQL এ complex relationships করার চেষ্টা
- SQL কে scale করা যায় না ভাবা
- একটা system এ শুধু একটাই database use করার চিন্তা (Polyglot persistence)

---

## 3.2 Database Scaling

### 📖 সংজ্ঞা
Database scaling মানে বেশি data এবং বেশি traffic handle করার ক্ষমতা বাড়ানো।

### 🔑 Scaling Strategies

```
Database Scaling Options:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. Vertical Scaling (Scale Up):
   ┌──────────────────┐      ┌──────────────────┐
   │ DB: 8 CPU, 32GB  │ ──▶  │ DB: 32 CPU, 256GB│
   └──────────────────┘      └──────────────────┘
   Limit আছে, expensive

2. Read Replicas:
   ┌──────────────┐
   │  Primary DB  │ ──write──▶ [Application writes here]
   │  (Master)    │
   └──────┬───────┘
          │ replication
   ┌──────┴──────┐──────────────┐
   │  Replica 1  │  Replica 2   │  [Application reads from replicas]
   └─────────────┘──────────────┘

3. Sharding (Horizontal Partitioning):
   User ID 1-1000    → Shard 1 (DB Server 1)
   User ID 1001-2000 → Shard 2 (DB Server 2)
   User ID 2001+     → Shard 3 (DB Server 3)

4. Caching Layer:
   Application → Redis → DB (cache miss হলে)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 3.3 Replication

### 📖 সংজ্ঞা
Replication মানে **একই data multiple servers এ copy রাখা** — availability, reliability, এবং read performance বাড়ানো।

### 🔄 Replication Types

```
Master-Slave (Primary-Replica) Replication:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
         [Application]
         ┌─────┴──────┐
       Write          Read
         │              │
    [Primary DB]   [Replica 1]
    (Master)    ──▶ [Replica 2]   ← sync হয় continuously
                ──▶ [Replica 3]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Master-Master (Multi-Primary) Replication:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Primary 1] ←──sync──▶ [Primary 2]
Both accept reads AND writes
Conflict resolution দরকার
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Replication Modes

| Mode | কীভাবে | Latency | Data Loss Risk |
|------|--------|---------|---------------|
| Synchronous | Primary wait করে replica confirm | বেশি | শূন্য |
| Asynchronous | Primary write করে, replica পরে sync | কম | সামান্য possible |
| Semi-synchronous | কমপক্ষে একটা replica confirm | মাঝামাঝি | কম |

### 🎤 Interview Explanation
> "Replication দুই কাজে লাগে — high availability এবং read scaling। Master-Slave তে write সব master এ, read replicas এ distribute হয়। Master fail করলে slave কে promote করি — failover। কিন্তু replication lag হতে পারে asynchronous mode এ — replica তে stale data থাকতে পারে।"

### ❓ Interview Questions
1. "Replication lag কী এবং কীভাবে handle করবে?"
2. "Master fail করলে কী হবে? (Failover process)"
3. "Synchronous replication এর downside কী?"

---

## 3.4 Sharding

### 📖 সংজ্ঞা
Sharding হলো **large database কে smaller pieces (shards) এ ভাগ করা** — প্রতিটা shard আলাদা server এ থাকে।

### 🏗️ Sharding Strategies

```
1. Range-based Sharding:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
User ID: 1 - 1,000,000      → Shard 1
User ID: 1,000,001 - 2,000,000 → Shard 2
User ID: 2,000,001+         → Shard 3

✅ Simple, range queries efficient
❌ Hotspot problem (নতুন user সব Shard 3 এ!)

2. Hash-based Sharding:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
shard = hash(user_id) % number_of_shards

user_id=123 → hash → Shard 1
user_id=456 → hash → Shard 3
user_id=789 → hash → Shard 2

✅ Even distribution, no hotspot
❌ Range queries inefficient, resharding কঠিন

3. Directory-based Sharding:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Lookup Table/Directory]
user_id=123 → Shard 2
user_id=456 → Shard 1
user_id=789 → Shard 3

✅ Flexible, resharding সহজ
❌ Directory নিজেই bottleneck/single point of failure

4. Geographic Sharding:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Bangladesh users → BD Shard (Asia DB)
US users        → US Shard (US DB)
Europe users    → EU Shard (EU DB)

✅ Low latency for users, GDPR compliance
❌ Cross-region queries কঠিন
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### ⚠️ Sharding Challenges
```
Sharding এর সমস্যাগুলো:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
❌ Cross-shard JOINs: User Shard 1 এ, Order Shard 3 এ
   → JOIN করা complex/impossible
   → Denormalization বা Application-level JOIN দরকার

❌ Cross-shard Transactions: ACID maintain করা কঠিন
   → Two-Phase Commit (2PC) use করতে হয়

❌ Rebalancing: নতুন shard যোগ করলে data move করতে হয়
   → Consistent Hashing দিয়ে minimize করা যায়

❌ Hotspot: একটা shard এ বেশি load
   → Proper sharding key selection critical
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎤 Interview Explanation
> "Sharding vertical scaling এর limit হলে use করি — data কে multiple servers এ horizontally ভাগ করি। Hash-based sharding even distribution দেয়। কিন্তু সমস্যা হলো cross-shard queries — JOIN করা কঠিন, transaction manage করা কঠিন। তাই sharding এ যাওয়ার আগে read replicas, caching সব try করি।"

---

## 3.5 Partitioning

### 📖 সংজ্ঞা
Partitioning হলো **একটা table কে logical বা physical pieces এ ভাগ করা** — same database server এ থাকে (sharding থেকে আলাদা)।

### 📊 Partitioning Types

```
1. Horizontal Partitioning (Row-based):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
orders_2024 (Jan-Jun) → Partition 1
orders_2024 (Jul-Dec) → Partition 2
orders_2025           → Partition 3
[Same server, different tables/files]

2. Vertical Partitioning (Column-based):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
users table:
Partition A: id, name, email (frequently accessed)
Partition B: bio, profile_pic, preferences (rarely accessed)

3. Range Partitioning (Date/Time):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
-- PostgreSQL Partition by date:
CREATE TABLE orders (
    id BIGINT,
    created_at DATE,
    total DECIMAL
) PARTITION BY RANGE (created_at);

CREATE TABLE orders_2025_q1 PARTITION OF orders
    FOR VALUES FROM ('2025-01-01') TO ('2025-04-01');
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎤 Interview Explanation
> "Partitioning আর Sharding সহজে confuse হয়। Partitioning একটা server এর মধ্যে — table কে ভাগ করি। Sharding multiple servers এ। Time-series data এ date-based partitioning দারুণ কাজ করে — পুরনো partition delete করা সহজ, query fast।"

---

## 3.6 Indexing

### 📖 সংজ্ঞা
Index হলো database এ **extra data structure** যা queries কে fast করে — book এর সূচিপত্রের মতো।

### 🔄 Index কীভাবে কাজ করে?

```
Index ছাড়া (Full Table Scan):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SELECT * FROM users WHERE email = 'rahim@gmail.com';

Row 1: id=1, email='karim@gmail.com'  ← check
Row 2: id=2, email='salam@gmail.com'  ← check
...
Row 999999: id=999999, email='rahim@gmail.com' ← FOUND!
O(n) — 1 million rows scan করতে হলো!

Index সহ (B-Tree Index):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Index: email → row_pointer]
B-Tree তে binary search → O(log n)
'rahim@gmail.com' → row_id=999999 → directly fetch
Millions of rows তেও milliseconds!
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Index Types

| Type | কাজ | Best For |
|------|-----|---------|
| B-Tree (default) | Range queries, equality | Most queries |
| Hash | Equality only (=) | Exact match lookups |
| Composite | Multiple columns together | Multi-column WHERE |
| Unique | Duplicate prevent | email, username |
| Full-text | Text search | Blog search, product name |
| Partial | Subset of rows | WHERE status='active' |

### 💻 SQL Index Examples
```sql
-- Single column index:
CREATE INDEX idx_users_email ON users(email);

-- Composite index:
CREATE INDEX idx_orders_user_date ON orders(user_id, created_at);

-- Unique index:
CREATE UNIQUE INDEX idx_users_email_unique ON users(email);

-- Partial index (only active users):
CREATE INDEX idx_active_users ON users(email) WHERE status = 'active';

-- Full-text search index (PostgreSQL):
CREATE INDEX idx_products_fts ON products USING gin(to_tsvector('english', name));
```

### ⚠️ Index Trade-offs
```
✅ Index এর সুবিধা:
- SELECT query অনেক fast
- ORDER BY, GROUP BY fast

❌ Index এর অসুবিধা:
- Extra disk space (sometimes 20-30% extra)
- INSERT/UPDATE/DELETE slow (index ও update করতে হয়)
- Too many indexes → write performance খারাপ
```

### 🎤 Interview Explanation
> "Index হলো database এর সূচিপত্র — full table scan না করে সরাসরি data খুঁজে পায়। B-Tree index most common — range queries এ efficient। কিন্তু সব column এ index দিলে write operation slow হয়। Rule of thumb: WHERE, JOIN, ORDER BY column গুলোতে index দাও।"

### ❓ Interview Questions
1. "Index থাকলেও কখন কখন full table scan হয়?"
2. "Composite index এর column order কেন important?"
3. "Covering index কী?"
4. "Index এর কারণে insert কীভাবে slow হয়?"

---

## 3.7 Caching (Database Level)

### 📖 সংজ্ঞা
Database caching মানে **frequently accessed data কে memory তে রেখে** database query এড়ানো।

### 🔄 Caching Patterns

```
Cache-Aside (Lazy Loading) — সবচেয়ে Common:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. App → Redis: "user:123 আছে?"
2. Cache Miss → App → Database
3. Database → App → Redis cache করো
4. পরবর্তী request → Cache Hit → fast!

[App] ──check──▶ [Redis Cache]
              Cache Miss ↓
         [Database] ──data──▶ [App] ──store──▶ [Redis]

Write-Through — Write এও cache update:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Write: App → Database + Redis (same time)
✅ Cache always fresh
❌ Write latency বেশি

Write-Back (Write-Behind) — Cache প্রথমে:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Write: App → Redis (async) → Database later
✅ Write fast
❌ Data loss risk (Redis crash হলে)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 3.8 Read-Heavy vs Write-Heavy Systems

### 📖 সংজ্ঞা

**Read-Heavy System:** বেশিরভাগ operation হলো read — data পড়া।
**Write-Heavy System:** বেশিরভাগ operation হলো write — data লেখা।

### 📊 Optimization Strategies

```
Read-Heavy System (e.g., News site, Blog):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Read : Write ratio → 100:1 বা বেশি
Solutions:
✅ Read Replicas — reads multiple servers এ distribute
✅ Caching (Redis) — DB hit কম করো
✅ CDN — static content edge এ
✅ Database indexing — queries fast করো
✅ Denormalization — JOINs কমাও

Write-Heavy System (e.g., IoT sensors, logging):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Write : Read ratio → 10:1 বা বেশি
Solutions:
✅ Sharding — writes multiple servers এ distribute
✅ Message Queue (Kafka) — burst writes buffer করো
✅ Batch writes — একসাথে অনেক write
✅ LSM-tree DB (Cassandra, RocksDB) — write-optimized
✅ Avoid unnecessary indexes — write fast করো
✅ Async writes — immediate response, write later
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎤 Interview Explanation
> "System design এ প্রথমেই জিজ্ঞেস করি — read-heavy নাকি write-heavy? Twitter feed read-heavy (1:100 write:read) — read replicas, cache use করি। IoT sensor data write-heavy — Cassandra বা Kafka use করি। Design সম্পূর্ণ আলাদা।"

---

## 3.9 Data Consistency

### 📖 সংজ্ঞা
Data Consistency মানে **সব nodes বা users একই time এ same data দেখবে।**

### 📊 Consistency Levels

```
Strong Consistency:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Write হওয়ার সাথে সাথে সব node update
পরের read সবসময় latest data পাবে
Example: Banking, Stock trading
Cost: High latency, low availability

Eventual Consistency:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Write হলে সব node eventually update হবে
কিছু সময় পুরনো data দেখা যেতে পারে
Example: Social media likes, DNS propagation
Cost: Low latency, high availability

Read-Your-Own-Writes:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
তুমি নিজে যা write করেছো তা সাথে সাথে দেখবে
অন্যরা হয়তো later দেখবে
Example: Facebook post — তুমি সাথে সাথে দেখো
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 3.10 Eventual Consistency

### 📖 সংজ্ঞা
Eventual Consistency হলো guarantee যে **সব updates propagate হলে সব nodes same value দেখাবে** — কিন্তু কতক্ষণ লাগবে সেটা নির্দিষ্ট নয়।

### 🎯 Real-Life Analogy
> Facebook এ status update করলে — তুমি সাথে সাথে দেখো। তোমার বন্ধু (অন্য region এ) হয়তো ৫ সেকেন্ড পরে দেখবে। কিন্তু eventually সবাই same status দেখবে। এটাই eventual consistency।

### 📊 Eventual Consistency কোথায় OK?

| ✅ OK | ❌ Not OK |
|-------|---------|
| Social media likes | Bank balance |
| Product view count | Stock inventory |
| DNS propagation | Payment processing |
| User profile update | Medical records |
| Shopping cart (sometimes) | Flight seat booking |

### 🎤 Interview Explanation
> "Eventual consistency মানে হলো system strong consistency sacrifice করে high availability আর low latency পায়। Cassandra AP database — এটা eventual consistency দেয়। Social media feed এ fine — like count ১ সেকেন্ড পরে update হলে সমস্যা নেই। কিন্তু banking তে CP database দরকার — money অনেক consistent হতে হবে।"

---

## 3.11 ACID vs BASE

### 📖 সংজ্ঞা

**ACID (SQL Databases এর guarantee):**
- **A — Atomicity:** Transaction পুরো হয় বা একদম হয় না
- **C — Consistency:** Database সবসময় valid state এ থাকে
- **I — Isolation:** Concurrent transactions একে অন্যকে affect করে না
- **D — Durability:** Committed data permanent (crash হলেও)

**BASE (NoSQL Databases এর approach):**
- **B — Basically Available:** System সবসময় response দেয় (data stale হলেও)
- **A — Soft State:** System state change হতে পারে input ছাড়াই
- **E — Eventually Consistent:** সময়মতো সব node sync হবে

### 🎯 Real-Life Analogy
> **ACID — Bank Transfer:**
> তুমি ৫০০০ টাকা Bkash থেকে পাঠাচ্ছো।
> - Atomicity: তোমার account থেকে কাটবে AND recipient পাবে — একসাথে বা একদমই না
> - Consistency: Total money system এ same থাকবে
> - Isolation: অন্য transaction তোমার transaction এ interfere করবে না
> - Durability: Transaction complete হলে power গেলেও টাকা safe

> **BASE — Facebook Like:**
> তুমি একটা post এ like দিলে — তোমার বন্ধু হয়তো এখনই দেখবে না, কিছুক্ষণ পরে দেখবে।

### 📊 ACID vs BASE তুলনা

| বিষয় | ACID | BASE |
|------|------|------|
| Consistency | Strong | Eventual |
| Availability | Sacrifice করে | Prioritize করে |
| Complexity | High | Low |
| Performance | Lower (locks, etc.) | Higher |
| Scale | Harder | Easier |
| Use case | Financial, Medical | Social, Analytics |
| Examples | PostgreSQL, MySQL | Cassandra, DynamoDB |

### 🎤 Interview Explanation
> "ACID guarantee হলো strong consistency — banking এ এটা দরকার। BASE হলো availability কে priority দেওয়া — eventual consistency accept করা। NoSQL databases বেশিরভাগ BASE follow করে, তাই scale করা সহজ কিন্তু strong consistency নেই। Modern systems often polyglot — banking transactions PostgreSQL (ACID), user feed Cassandra (BASE)।"

### ❓ Interview Questions
1. "ACID এর Isolation এর different levels কী কী?"
2. "Phantom read কী?"
3. "Two-Phase Commit (2PC) কী?"
4. "Saga pattern কী এবং কেন use করো?"

---

## 📋 PART 3: Quick Revision Table

| Concept | এক কথায় | Key Point |
|---------|---------|-----------|
| SQL | Relational, ACID | Tables, JOINs, structured |
| NoSQL | Non-relational, BASE | Flexible, scalable |
| Replication | Data copy in multiple servers | Read scaling, availability |
| Sharding | Horizontal DB partition | Write scaling, large data |
| Partitioning | Table partition (same server) | Query performance |
| Indexing | Fast lookup data structure | B-Tree most common |
| Cache-Aside | App manages cache | Most common pattern |
| Write-Through | Write DB + cache together | Consistent cache |
| Read-Heavy | বেশি read | Replicas, cache |
| Write-Heavy | বেশি write | Sharding, queue, LSM |
| Strong Consistency | সব node same data instantly | Banking |
| Eventual Consistency | Eventually same, not instantly | Social media |
| ACID | Atomicity, Consistency, Isolation, Durability | SQL |
| BASE | Basically Available, Soft state, Eventually consistent | NoSQL |

---

## 🎯 PART 3: Top 10 Interview Questions

<details>
<summary><strong>Q1: SQL vs NoSQL — কোনটা বেছে নেবে এবং কেন?</strong></summary>

**উত্তর:**
এটা use case নির্ভর। আমি এভাবে decide করি:

**SQL choose করি যখন:**
- Data structured এবং relationships complex (users, orders, payments)
- ACID guarantee দরকার (banking, finance)
- Complex queries/JOINs দরকার
- Data consistency critical

**NoSQL choose করি যখন:**
- Schema flexible বা evolving (product catalog)
- Massive horizontal scaling দরকার
- High write throughput (IoT, logs)
- Key-value simple access (session, cache)
- Graph relationships (social network)

Real answer: Most production systems use both (Polyglot Persistence) — user data PostgreSQL, cache Redis, search Elasticsearch.

</details>

<details>
<summary><strong>Q2: Database sharding করবে কখন এবং কীভাবে?</strong></summary>

**উত্তর:**
Sharding করার আগে এই steps নিই:

1. **Optimize queries** — indexes, query rewrite
2. **Add read replicas** — reads distribute করো
3. **Add caching** — Redis দিয়ে DB load কমাও
4. **Vertical scale** — bigger hardware
5. **তারপর sharding** — এটা last resort কারণ complexity অনেক বাড়ে

Sharding key সতর্কে choose করি:
- Even distribution (hotspot avoid)
- Common query pattern এর সাথে align
- Join minimal করার চেষ্টা
- Future growth consider

Hash-based sharding usually prefer করি — even distribution। কিন্তু Consistent Hashing use করি resharding সহজ করতে।

</details>

<details>
<summary><strong>Q3: Database index কখন দেবে, কখন দেবে না?</strong></summary>

**উত্তর:**
**Index দেবো:**
- WHERE clause এ frequently used columns
- JOIN condition columns (foreign keys)
- ORDER BY, GROUP BY columns
- High cardinality columns (email, user_id)

**Index দেবো না:**
- Low cardinality columns (gender: M/F — শুধু ২টা value)
- Rarely queried columns
- Small tables (full scan faster)
- Frequently updated columns (index maintenance overhead)
- Too many indexes → write performance দেখো

Rule: Production এ EXPLAIN ANALYZE দিয়ে query plan দেখো, সেটা বলবে index দরকার কিনা।

</details>

<details>
<summary><strong>Q4: N+1 query problem কী এবং কীভাবে fix করবে?</strong></summary>

**উত্তর:**
```python
# N+1 Problem:
users = User.objects.all()  # 1 query
for user in users:
    print(user.orders.all())  # N queries (প্রতি user এর জন্য!)
# Total: N+1 queries!

# Fix: Eager loading (JOIN/prefetch):
users = User.objects.prefetch_related('orders').all()
# Total: 2 queries (users + all orders in one go)

# অথবা SQL JOIN:
SELECT u.*, o.*
FROM users u
LEFT JOIN orders o ON o.user_id = u.id;
# Total: 1 query!
```

Django তে `select_related` (FK/OneToOne) এবং `prefetch_related` (ManyToMany) use করো।

</details>

<details>
<summary><strong>Q5: ACID transaction কীভাবে implement করবে?</strong></summary>

**উত্তর:**
```python
# Django/SQLAlchemy transaction:
from django.db import transaction

def transfer_money(from_user_id, to_user_id, amount):
    with transaction.atomic():  # ACID transaction শুরু
        from_user = User.objects.select_for_update().get(id=from_user_id)
        to_user = User.objects.select_for_update().get(id=to_user_id)
        
        if from_user.balance < amount:
            raise ValueError("Insufficient balance")
        
        from_user.balance -= amount
        to_user.balance += amount
        
        from_user.save()
        to_user.save()
    # transaction.atomic() এর block শেষ → commit
    # Exception হলে → automatic rollback

# select_for_update() → row-level lock
# concurrent requests একসাথে same row update করতে পারবে না
```

</details>

<details>
<summary><strong>Q6: Database replication lag কীভাবে handle করবে?</strong></summary>

**উত্তর:**
Replication lag মানে master এ write হওয়ার পর replica তে পৌঁছাতে কিছু সময় লাগে।

**Solutions:**
1. **Read-your-own-writes:** User নিজে write করা data পড়তে চাইলে master থেকে read করো
2. **Monotonic reads:** Same user কে same replica থেকে read করাও (sticky session)
3. **Synchronous replication:** Lag শূন্য কিন্তু write latency বেশি
4. **Application level:** Write করার পর কিছুটা wait করো (wait_for_replica)
5. **Cache:** Write করার সাথে cache update করো — read replica এর উপর depend না করে

```python
# Read-your-own-writes pattern:
def get_user(user_id, just_updated=False):
    if just_updated:
        return db_master.get_user(user_id)  # master থেকে read
    return db_replica.get_user(user_id)     # replica থেকে read
```

</details>

<details>
<summary><strong>Q7: Eventual consistency এ কীভাবে conflict resolve করবে?</strong></summary>

**উত্তর:**
Distributed systems এ two nodes একই data আলাদাভাবে update করলে conflict হয়।

**Conflict Resolution Strategies:**

1. **Last Write Wins (LWW):** Latest timestamp জেতে
   - Simple কিন্তু data loss হতে পারে
   - Cassandra default

2. **Multi-Version Concurrency Control (MVCC):**
   - সব versions রাখো, user decide করুক
   - Amazon shopping cart

3. **CRDTs (Conflict-free Replicated Data Types):**
   - Mathematically conflict-free operations
   - Counters, sets

4. **Application-level merge:**
   - Business logic দিয়ে merge করো
   - Google Docs operational transformation

</details>

<details>
<summary><strong>Q8: Polyglot persistence কী?</strong></summary>

**উত্তর:**
Polyglot persistence মানে একটা application এ **multiple database technologies** use করা — প্রতিটা use case এর জন্য best-fit database।

**উদাহরণ (E-commerce):**
```
User profiles, orders → PostgreSQL (ACID, relationships)
Product search        → Elasticsearch (full-text search)
Session data          → Redis (fast key-value)
Product images        → S3 (object storage)
Analytics data        → Redshift/BigQuery (columnar, OLAP)
Real-time inventory   → Redis (fast atomic operations)
Recommendations       → Neo4j (graph relationships)
```

প্রতিটা database তার purpose এ best। কিন্তু complexity বেশি — operations, backups, monitoring সব আলাদা।

</details>

<details>
<summary><strong>Q9: Database connection pool কী এবং কেন দরকার?</strong></summary>

**উত্তর:**
প্রতিটা DB connection establish করতে সময় লাগে (~100ms) এবং resource দরকার। প্রতিটা request এ নতুন connection বানালে:
- Slow (connection overhead)
- Resource wasteful
- DB connection limit exceed হতে পারে

**Connection Pool:**
```python
# SQLAlchemy connection pool:
from sqlalchemy import create_engine

engine = create_engine(
    "postgresql://user:pass@localhost/db",
    pool_size=20,        # permanent connections
    max_overflow=10,     # extra connections if needed
    pool_timeout=30,     # wait time for available connection
    pool_recycle=1800    # connection refresh interval
)
```

Pool তে আগে থেকে connections ready থাকে। Request আসলে pool থেকে connection নেয়, শেষে ফেরত দেয়।

</details>

<details>
<summary><strong>Q10: Database এ Deadlock কী এবং কীভাবে prevent করবে?</strong></summary>

**উত্তর:**
Deadlock: দুটো transaction একে অন্যের lock এর জন্য wait করছে — কেউই proceed করতে পারছে না।

```
Transaction A: Lock(user_1) → waiting for Lock(user_2)
Transaction B: Lock(user_2) → waiting for Lock(user_1)
→ Deadlock!
```

**Prevention:**
1. **Consistent lock ordering:** সবসময় same order এ locks নাও (user_1 আগে, user_2 পরে)
2. **Lock timeout:** অনেকক্ষণ wait করলে rollback
3. **SELECT FOR UPDATE NOWAIT:** Lock না পেলে immediately fail
4. **Minimize transaction scope:** ছোট ছোট transactions
5. **Deadlock detection:** DB automatically detect করে একটাকে rollback করে

```python
# Correct lock ordering (always lock smaller ID first):
def transfer(from_id, to_id, amount):
    first_id, second_id = sorted([from_id, to_id])
    with transaction.atomic():
        first = User.objects.select_for_update().get(id=first_id)
        second = User.objects.select_for_update().get(id=second_id)
        # proceed...
```

</details>

<div align="right">

[⬆ উপরে যাও](#) | [📚 সূচিপত্র](#) | [PART 4 →](#part4)

</div>

---

<a id="part4"></a>

---

# PART 4: Caching & Performance Optimization
### ⚡ System কে দ্রুত করার কৌশল

> **Interview টিপস:** Caching system design এর সবচেয়ে powerful tool। "System slow হচ্ছে, কী করবে?" — প্রায় সব ক্ষেত্রে answer এ cache আসবে। এটা ভালো বুঝলে interview এ অনেক এগিয়ে থাকবে।

---

## 4.1 Caching কী? (What is Caching)

### 📖 সংজ্ঞা
Caching হলো **frequently accessed data কে fast storage এ রাখা** — পরের request এ slow source (DB, API) থেকে না নিয়ে cache থেকে serve করা।

### 🎯 Real-Life Analogy
> পরীক্ষার আগে textbook থেকে important points নিজের খাতায় লিখে রাখো — পরীক্ষার হলে textbook খোঁজার দরকার নেই, খাতা দেখো। Cache হলো সেই খাতা।

### 📊 Caching Tiers

```
Cache Hierarchy (Fastest to Slowest):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
L1 CPU Cache       ~0.5 ns    ← Fastest, smallest (KB)
L2 CPU Cache       ~5 ns
L3 CPU Cache       ~40 ns
RAM                ~100 ns    ← Application level cache
SSD                ~100 μs
Redis (network)    ~0.5 ms    ← Distributed cache
HDD                ~10 ms
Database           ~100ms+    ← Slowest
Network (CDN miss) ~200ms+
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Caching Benefits
```
Without Cache:                    With Cache:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
100 users → 100 DB queries        100 users → 1 DB query
                                             99 cache hits
Response time: ~200ms             Response time: ~2ms
DB load: High                     DB load: Minimal
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 4.2 Redis

### 📖 সংজ্ঞা
Redis (Remote Dictionary Server) হলো **in-memory data structure store** — cache, session store, message broker, real-time database হিসেবে use হয়।

### 🔑 Redis Data Structures

```
Redis এর Data Types:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. String:
   SET user:123:name "Rahim"
   GET user:123:name → "Rahim"
   SETEX session:abc 3600 "user_data"  ← TTL সহ

2. Hash (Object store):
   HSET user:123 name "Rahim" email "rahim@mail.com" age 25
   HGET user:123 name → "Rahim"
   HGETALL user:123 → {name: Rahim, email: ..., age: 25}

3. List (Queue/Stack):
   LPUSH notifications:user:123 "New message!"
   RPOP notifications:user:123 → "New message!"

4. Set (Unique values):
   SADD online_users "user:123" "user:456"
   SMEMBERS online_users → {"user:123", "user:456"}
   SISMEMBER online_users "user:123" → 1 (true)

5. Sorted Set (Leaderboard):
   ZADD leaderboard 1500 "player:rahim"
   ZADD leaderboard 2000 "player:karim"
   ZRANK leaderboard "player:rahim" → 1 (2nd place)
   ZRANGE leaderboard 0 9 WITHSCORES → top 10

6. HyperLogLog (Unique count):
   PFADD visitors "ip1" "ip2" "ip3"
   PFCOUNT visitors → 3 (approximate unique)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 💻 Redis Implementation (Python)

```python
import redis
import json
from functools import wraps

r = redis.Redis(host='localhost', port=6379, db=0)

# Cache-Aside Pattern:
def get_user(user_id: int) -> dict:
    cache_key = f"user:{user_id}"
    
    # Cache check:
    cached = r.get(cache_key)
    if cached:
        return json.loads(cached)  # Cache Hit!
    
    # Cache Miss → DB query:
    user = db.query("SELECT * FROM users WHERE id = %s", user_id)
    
    # Cache store with TTL:
    r.setex(cache_key, 3600, json.dumps(user))  # 1 hour TTL
    return user

# Decorator pattern for caching:
def cache(ttl=3600):
    def decorator(func):
        @wraps(func)
        def wrapper(*args, **kwargs):
            key = f"{func.__name__}:{args}:{kwargs}"
            cached = r.get(key)
            if cached:
                return json.loads(cached)
            result = func(*args, **kwargs)
            r.setex(key, ttl, json.dumps(result))
            return result
        return wrapper
    return decorator

@cache(ttl=600)  # 10 minutes cache
def get_product_list(category: str) -> list:
    return db.query("SELECT * FROM products WHERE category = %s", category)
```

### 🔑 Redis Use Cases

| Use Case | Redis Command | Example |
|----------|-------------|---------|
| Cache | GET/SET/SETEX | Product data, user profile |
| Session store | SETEX | User login session |
| Rate limiting | INCR + EXPIRE | API rate limit |
| Pub/Sub | PUBLISH/SUBSCRIBE | Real-time notifications |
| Job queue | LPUSH/RPOP | Background tasks |
| Leaderboard | ZADD/ZRANGE | Game rankings |
| Real-time counter | INCR | Page views, likes |
| Distributed lock | SET NX | Prevent duplicate operations |

### 🎤 Interview Explanation
> "Redis আমার go-to caching solution। In-memory তাই অনেক fast (sub-millisecond)। String, Hash, List, Set, Sorted Set — আলাদা use case এ আলাদা data structure। TTL দিয়ে cache expiry set করি। Production এ Redis Cluster use করি high availability এর জন্য।"

---

## 4.3 Memcached Basics

### 📖 সংজ্ঞা
Memcached হলো **simple distributed memory caching system** — শুধু key-value string store করে।

### 📊 Redis vs Memcached

| বিষয় | Redis | Memcached |
|------|-------|-----------|
| Data structures | String, Hash, List, Set, Sorted Set | শুধু String |
| Persistence | Optional (RDB/AOF) | নেই (memory only) |
| Replication | আছে | নেই (manually) |
| Pub/Sub | আছে | নেই |
| Cluster | আছে | আছে |
| Lua scripting | আছে | নেই |
| Memory efficiency | Slightly higher | Slightly lower overhead |
| Use case | Versatile, feature-rich | Simple string cache only |
| Recommended | ✅ Modern choice | Legacy systems |

### 🎤 Interview Explanation
> "Memcached শুধু simple string caching — Redis এর subset। আজকাল নতুন project এ Redis use করি কারণ Redis এ অনেক বেশি features আছে। Memcached পুরনো systems এ দেখি।"

---

## 4.4 Cache Invalidation

### 📖 সংজ্ঞা
Cache Invalidation মানে **stale (outdated) data কে cache থেকে remove বা update করা** যাতে user পুরনো data না দেখে।

> **বিখ্যাত quote:** "There are only two hard things in Computer Science: cache invalidation and naming things." — Phil Karlton

### 🔑 Cache Invalidation Strategies

```
1. TTL (Time-To-Live) — সবচেয়ে Common:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
r.setex("product:123", 3600, data)  # 1 hour পর auto expire
✅ Simple, automatic
❌ Stale data TTL পর্যন্ত থাকতে পারে

2. Event-based Invalidation:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
def update_product(product_id, new_data):
    db.update("products", product_id, new_data)
    r.delete(f"product:{product_id}")  # Cache clear!
✅ Always fresh after update
❌ Miss করলে stale data

3. Cache-through (Write-Through):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
def update_product(product_id, new_data):
    db.update("products", product_id, new_data)
    r.setex(f"product:{product_id}", 3600, new_data)  # Also update cache
✅ Cache always consistent
❌ Write latency বেশি

4. Cache Versioning:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Version increment করলে পুরনো key automatically stale:
version = r.incr("product:123:version")
cache_key = f"product:123:v{version}"
✅ Instant invalidation across all caches
❌ Old keys accumulate (cleanup দরকার)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### ⚠️ Cache Problems

```
1. Cache Stampede (Thundering Herd):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Cache expire → ১০০০ request একসাথে DB তে যায়!
→ DB overloaded

Solution:
- Mutex/Lock: একটাই DB query, বাকি wait
- Probabilistic early expiration: TTL এর কাছাকাছি time এ refresh
- Background refresh: TTL শেষের আগেই background এ refresh

2. Cache Penetration:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Non-existent key এর request → সবসময় DB hit
→ Attacker intentionally করলে DB overload

Solution:
- Bloom Filter: "এই key exist করে?" fast check
- Cache null result: "user:999" → null store করো

3. Cache Avalanche:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
একসাথে অনেক cache expire → সব DB তে যায়

Solution:
- Random TTL: 3600 ± random(300) — সব একসাথে expire না করে
- Pre-warming: Deploy এর আগে cache গরম করো
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎤 Interview Explanation
> "Cache invalidation কঠিন কারণ data update হলে cache এ পুরনো data থাকে। TTL based approach simple — কিছু সময়ের জন্য stale data accept করি। Critical data এ event-based invalidation — update হলে সাথে সাথে cache delete। Cache Stampede problem এ mutex lock বা probabilistic refresh use করি।"

---

## 4.5 CDN Caching

### 📖 সংজ্ঞা
CDN (Content Delivery Network) globally distributed servers এ **static content cache করে** — user এর কাছের server থেকে serve করে।

### 🔄 CDN Cache Flow

```
CDN Caching Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
First Request (BD User → Singapore CDN):
[BD User] ──GET /logo.png──▶ [Singapore CDN]
                               Cache Miss!
[Singapore CDN] ──GET /logo.png──▶ [Origin Server, Dhaka]
[Origin] ──logo.png──▶ [Singapore CDN] (cache করে রাখলো)
[Singapore CDN] ──logo.png──▶ [BD User]
Latency: ~500ms

Second Request (any BD User):
[BD User] ──GET /logo.png──▶ [Singapore CDN]
                               Cache Hit! ✅
[Singapore CDN] ──logo.png──▶ [BD User]
Latency: ~20ms (25x faster!)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Cache-Control Headers

```http
# Response headers that control CDN caching:

# 1 hour cache, CDN can cache:
Cache-Control: public, max-age=3600

# No CDN cache, browser can cache:
Cache-Control: private, max-age=3600

# Never cache:
Cache-Control: no-store

# Validate before using:
Cache-Control: no-cache

# Immutable (versioned assets):
Cache-Control: public, max-age=31536000, immutable
# e.g., /static/app.abc123.js — hash in filename
```

### 🎯 What to CDN Cache?

| ✅ CDN তে Cache করো | ❌ CDN তে Cache করো না |
|--------------------|----------------------|
| Images, videos | Personalized content |
| CSS, JavaScript | User-specific API responses |
| HTML static pages | Payment pages |
| Fonts | Auth pages |
| PDF, documents | Real-time data |

---

## 4.6 Browser Caching

### 📖 সংজ্ঞা
Browser user এর machine এ **files locally store করে** — পরের visit এ server থেকে না নিয়ে local থেকে load করে।

### 🔑 Browser Cache Headers

```
ETag + Last-Modified (Validation):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Server Response:
    ETag: "abc123xyz"
    Last-Modified: Sun, 11 May 2026 00:00:00 GMT

Browser পরের বার:
    If-None-Match: "abc123xyz"
    If-Modified-Since: Sun, 11 May 2026 00:00:00 GMT

Server: পরিবর্তন নেই → 304 Not Modified (no body)
        পরিবর্তন আছে → 200 OK (new content)

Benefit: Bandwidth save! File transfer না হলে শুধু headers।
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 💡 Cache Busting
```html
<!-- Problem: CSS update করলে browser পুরনো CSS দেখায়! -->
<link rel="stylesheet" href="/static/app.css">

<!-- Solution: Content hash filename এ যোগ করো: -->
<link rel="stylesheet" href="/static/app.a1b2c3d4.css">
<!-- File change হলে hash বদলায় → browser নতুন file download করে -->
```

---

## 4.7 Rate Limiting

### 📖 সংজ্ঞা
Rate Limiting মানে **একটা client কতবার request করতে পারবে** তার সীমা নির্ধারণ করা — abuse, DDoS, spam prevent করতে।

### 🔑 Rate Limiting Algorithms

```
1. Fixed Window Counter:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Per minute: max 100 requests
Window: 00:00 - 01:00 → counter
        01:00 - 02:00 → counter reset

Problem: Window boundary এ burst possible
(59তম second এ 100 + 00তম second এ 100 = 200 in 2 sec)

2. Sliding Window Log:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Last 60 seconds এর সব timestamps track করো
Count > 100 হলে block

✅ Accurate
❌ Memory intensive (সব timestamps store)

3. Token Bucket (Most Popular):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Bucket এ tokens আছে (e.g., 100)
প্রতি request এ 1 token consume
প্রতি second এ 10 tokens refill
Bucket full হলে নতুন token overflow (discard)

✅ Burst allow করে
✅ Smooth rate limiting
Example: AWS API Gateway, Stripe

4. Leaky Bucket:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Requests queue তে আসে, fixed rate এ process হয়
Burst absorb করে কিন্তু fixed rate output
Example: Nginx limit_req
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 💻 Redis দিয়ে Rate Limiting

```python
import redis
import time

r = redis.Redis()

def check_rate_limit(user_id: str, limit: int = 100, window: int = 60) -> bool:
    """
    Sliding Window Rate Limiter using Redis
    Returns True if request is allowed, False if rate limited
    """
    now = time.time()
    key = f"rate_limit:{user_id}"
    
    pipe = r.pipeline()
    # Remove old timestamps outside window
    pipe.zremrangebyscore(key, 0, now - window)
    # Count current requests in window
    pipe.zcard(key)
    # Add current request timestamp
    pipe.zadd(key, {str(now): now})
    # Set expiry
    pipe.expire(key, window)
    
    results = pipe.execute()
    request_count = results[1]
    
    if request_count >= limit:
        return False  # Rate limited!
    return True

# API endpoint এ use:
def api_endpoint(request):
    user_id = request.user.id
    if not check_rate_limit(str(user_id), limit=100, window=60):
        return Response(
            {"error": "Rate limit exceeded. Try after 60 seconds."},
            status=429  # Too Many Requests
        )
    # Process request...
```

### 📊 Rate Limiting Headers

```http
HTTP/1.1 200 OK
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 45
X-RateLimit-Reset: 1683849600

HTTP/1.1 429 Too Many Requests
Retry-After: 30
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 0
```

---

## 4.8 Compression

### 📖 সংজ্ঞা
Compression মানে **data size কমানো** — network transfer এ কম bandwidth, faster load।

### 🔑 Compression Types

```
HTTP Response Compression:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Client Header: Accept-Encoding: gzip, br, deflate
Server Response: Content-Encoding: gzip

Algorithms:
- gzip: Most compatible, good compression (60-80% for text)
- Brotli (br): Better than gzip for text, modern browsers
- deflate: Older, less common

Example:
Raw HTML: 100 KB
gzip compressed: 20 KB  ← 80% smaller!
Brotli compressed: 17 KB ← Even better!

Nginx compression config:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
gzip on;
gzip_types text/plain text/css application/json application/javascript;
gzip_min_length 1000;
gzip_comp_level 6;
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Compression Comparison

| Algorithm | Ratio | Speed | CPU Cost |
|-----------|-------|-------|---------|
| gzip level 6 | ~65% | Fast | Medium |
| Brotli level 11 | ~70% | Slow | High |
| Brotli level 4 | ~65% | Fast | Low |
| LZ4 | ~50% | Very fast | Very low |

> **Rule:** Text content (HTML, JSON, CSS) compress করো। Images, videos আলাদা format (JPEG, WebP, H.264) ইতিমধ্যে compressed।

---

## 4.9 Lazy Loading

### 📖 সংজ্ঞা
Lazy Loading মানে **data বা resource তখনই load করো যখন actually দরকার** — আগে থেকে সব load না করা।

### 🔑 Types of Lazy Loading

```
1. Image Lazy Loading (Browser):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
<img src="product.jpg" loading="lazy" alt="Product">
← User scroll না করা পর্যন্ত image load হয় না

2. Database Lazy Loading (ORM):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Eager (load everything upfront):
user = User.objects.select_related('profile').get(id=123)
# SELECT users JOIN profiles in one query

# Lazy (load when accessed):
user = User.objects.get(id=123)
# SELECT from users only
# পরে:
profile = user.profile  # তখন SELECT from profiles (extra query!)
# N+1 problem হতে পারে!

3. Module Lazy Loading (JavaScript):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// Admin module শুধু admin page এ দরকার:
const AdminPanel = lazy(() => import('./AdminPanel'));
// Initial load fast — AdminPanel bundle আলাদা চলে

4. API Pagination (Lazy Data Loading):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
GET /api/products?page=1&limit=20   ← প্রথমে ২০টা
GET /api/products?page=2&limit=20   ← user scroll করলে আরো ২০টা
← 1 million products একসাথে load না করে
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 4.10 Performance Bottleneck Analysis

### 📖 কীভাবে Bottleneck খুঁজবে?

```
Performance Debugging Process:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Step 1: Measure (পরিমাপ করো)
   - Response time distribution (P50, P95, P99)
   - Error rate
   - CPU, Memory, Disk, Network usage
   - Database query times

Step 2: Profile (কোথায় সময় যাচ্ছে?)
   - Application profiler (cProfile, py-spy)
   - Database slow query log
   - APM tools (Datadog, New Relic, Jaeger)

Step 3: Identify Bottleneck
   Common bottlenecks:
   - Database: Slow queries, missing indexes, N+1
   - Network: High latency, no CDN, uncompressed
   - Application: CPU intensive code, memory leak
   - External APIs: Slow third-party calls

Step 4: Fix
   - Add cache
   - Add index
   - Optimize query
   - Add CDN
   - Use async/background processing

Step 5: Validate
   - Run load test again
   - Compare metrics
   - Repeat if needed
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Performance Optimization Checklist

```
Database Optimization:
✅ Proper indexes on WHERE/JOIN/ORDER BY columns
✅ No N+1 queries (use JOIN or prefetch)
✅ Query pagination (LIMIT/OFFSET)
✅ Connection pooling
✅ Read replicas for read-heavy loads
✅ Cache frequent queries in Redis
✅ Analyze slow query log

Application Optimization:
✅ Async processing for heavy tasks (Celery, Queue)
✅ Response compression (gzip/brotli)
✅ Efficient algorithms (O(n) not O(n²))
✅ Memory leak check
✅ Connection reuse (HTTP Keep-Alive)

Frontend Optimization:
✅ Image compression (WebP, AVIF)
✅ Lazy loading images
✅ Code splitting (bundle size কমাও)
✅ CDN for static assets
✅ Browser caching headers
✅ Minimize HTTP requests

Infrastructure Optimization:
✅ Load balancing
✅ Auto-scaling
✅ CDN
✅ Proper server sizing
```

---

## 📋 PART 4: Quick Revision Table

| Concept | এক কথায় | Key Point |
|---------|---------|-----------|
| Caching | Fast storage এ data রাখা | DB hits কমায় |
| Redis | In-memory data store | Multi data structures |
| Memcached | Simple string cache | Redis এর subset |
| Cache-Aside | App manages cache | Most common pattern |
| Write-Through | Write DB + cache together | Consistent |
| Cache Stampede | Cache expire → DB overload | Mutex/probabilistic fix |
| Cache Penetration | Non-existent key → DB | Bloom filter |
| Cache Avalanche | Many caches expire together | Random TTL |
| CDN Caching | Edge server এ static files | Nearest server |
| Browser Caching | Local machine এ file store | ETag, Cache-Control |
| Rate Limiting | Request সংখ্যা সীমা | 429 Too Many Requests |
| Token Bucket | Burst-friendly rate limit | AWS API Gateway |
| Compression | Data size কমানো | gzip 60-80% smaller |
| Lazy Loading | দরকার হলে তবেই load | Performance, UX |
| TTL | Cache expiry time | Auto-invalidation |

---

## 🎯 PART 4: Top 10 Interview Questions

<details>
<summary><strong>Q1: Cache কোথায় রাখবে এবং কী cache করবে?</strong></summary>

**উত্তর:**
**Cache করার জন্য ideal data:**
- Frequently read, rarely changed: Product catalog, user profile
- Expensive to compute: Complex aggregations, recommendation results
- Shared across users: Configuration, category lists
- External API responses: Weather data, exchange rates

**Cache করবো না:**
- User-specific sensitive data (payment info)
- Real-time data (live stock prices)
- Rapidly changing data (inventory count - better to cache with short TTL)
- Data যা rarely accessed

**কোথায় রাখবো:**
- Application in-memory (local cache): Same process এ, fastest, no network
- Redis (distributed cache): Multiple servers share, persistent option
- CDN: Static files, global distribution

</details>

<details>
<summary><strong>Q2: Redis আর Memcached এর মধ্যে কোনটা choose করবে?</strong></summary>

**উত্তর:**
**Redis choose করবো যখন:**
- Multiple data structures দরকার (Hash, List, Sorted Set)
- Persistence দরকার (restart এর পরেও data থাকবে)
- Pub/Sub messaging দরকার
- Distributed locks দরকার
- Lua scripting দরকার
- Atomic operations (INCR, ZADD)

**Memcached choose করবো যখন:**
- শুধু simple string caching (pure cache use case)
- Very high throughput, extremely low latency
- Legacy system এ already আছে

**Real answer:** আজকাল প্রায় সবাই Redis use করে। Memcached শুধু specific legacy cases এ।

</details>

<details>
<summary><strong>Q3: Cache Invalidation এর best strategy কী?</strong></summary>

**উত্তর:**
Context নির্ভর:

**TTL-based** (product list, static content):
```python
r.setex("products:category:electronics", 3600, data)
# 1 hour পর auto expire — acceptable stale window
```

**Event-based** (user profile, critical data):
```python
def update_user(user_id, data):
    db.update(user_id, data)
    r.delete(f"user:{user_id}")  # Immediate invalidation
```

**Write-through** (high read consistency দরকার):
```python
def update_product(product_id, data):
    db.update(product_id, data)
    r.setex(f"product:{product_id}", 3600, data)  # Cache also updated
```

**Combination:** TTL as safety net + event-based for known updates।

</details>

<details>
<summary><strong>Q4: Rate Limiting implement করলে কোন algorithm use করবে?</strong></summary>

**উত্তর:**
**Token Bucket** — most cases এ best:
- Burst handle করতে পারে (user হঠাৎ ১০টা request করলে OK)
- Average rate enforce করে
- AWS API Gateway, Stripe এই algorithm use করে

```python
def token_bucket_rate_limit(user_id, capacity=100, refill_rate=10):
    # capacity: max tokens (burst size)
    # refill_rate: tokens per second
    key = f"token_bucket:{user_id}"
    now = time.time()
    
    bucket = r.hgetall(key)
    tokens = float(bucket.get(b'tokens', capacity))
    last_refill = float(bucket.get(b'last_refill', now))
    
    # Refill tokens
    elapsed = now - last_refill
    tokens = min(capacity, tokens + elapsed * refill_rate)
    
    if tokens >= 1:
        tokens -= 1
        r.hset(key, mapping={'tokens': tokens, 'last_refill': now})
        r.expire(key, 3600)
        return True  # Allowed
    return False  # Rate limited
```

</details>

<details>
<summary><strong>Q5: Redis cluster কীভাবে কাজ করে?</strong></summary>

**উত্তর:**
Redis Cluster horizontally scale করে:
- Data 16384 hash slots এ ভাগ
- প্রতিটা node কিছু slots responsible
- Key → hash(key) % 16384 → সঠিক node এ যায়

```
Redis Cluster (3 master + 3 replica):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Master 1 (slots 0-5460)     → Replica 1
Master 2 (slots 5461-10922) → Replica 2
Master 3 (slots 10923-16383)→ Replica 3

GET user:123
→ hash("user:123") = 5649
→ Slot 5649 → Master 2
→ Data returned
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

Master fail করলে Replica automatically promoted। High availability।

</details>

<details>
<summary><strong>Q6: Cache hit rate কীভাবে improve করবে?</strong></summary>

**উত্তর:**
Cache Hit Rate = Cache Hits / Total Requests × 100%

**Improve করার উপায়:**
1. **TTL বাড়াও:** Data বেশিক্ষণ cache এ থাকলে hit rate বাড়বে (কিন্তু staleness বাড়বে)
2. **Cache warming:** Deploy এর আগে cache কে popular data দিয়ে গরম করো
3. **Better cache key design:** Granular keys — না হলে অনেক miss
4. **Increase cache size:** More data cache → fewer misses
5. **Identify hot data:** কোন data সবচেয়ে বেশি request হয় সেটা cache করো
6. **Reduce churn:** Cache থেকে data বের করার আগে expiry বাড়াও

Target: Production এ 90%+ hit rate ভালো।

</details>

<details>
<summary><strong>Q7: HTTP Cache-Control header কীভাবে set করবে?</strong></summary>

**উত্তর:**
```python
# Django example:
from django.views.decorators.cache import cache_control

# Public static content (CDN cache করবে):
@cache_control(public=True, max_age=86400)  # 24 hours
def product_image(request, image_id):
    ...

# Private user content:
@cache_control(private=True, max_age=3600)  # 1 hour, no CDN
def user_profile(request):
    ...

# Never cache:
@cache_control(no_store=True)
def payment_page(request):
    ...

# Versioned static files (forever):
# /static/app.abc123.css
Cache-Control: public, max-age=31536000, immutable
```

ETag use করলে conditional requests কাজ করে — bandwidth save।

</details>

<details>
<summary><strong>Q8: Distributed caching এ data consistency কীভাবে maintain করবে?</strong></summary>

**উত্তর:**
Multiple app servers → Multiple cache instances → Consistency challenge।

**Solutions:**

1. **Centralized cache (Redis):** সব app server একই Redis → consistent
2. **Cache invalidation broadcast:** একটা server cache update করলে সব server কে notify (Pub/Sub)
3. **Short TTL:** Stale window ছোট রাখো
4. **Versioned cache keys:** Update হলে নতুন key → পুরনো automatically stale

```python
# Pub/Sub based invalidation:
# Server A: user update করলো
r.delete(f"user:{user_id}")
r.publish("cache_invalidation", f"user:{user_id}")

# Server B, C: subscribe করে listen করছে
def on_invalidation(message):
    key = message['data']
    local_cache.delete(key)
```

</details>

<details>
<summary><strong>Q9: Image optimization কীভাবে করবে?</strong></summary>

**উত্তর:**
```
Image Optimization Strategy:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Format:
   JPEG → Photos (lossy, small)
   PNG → Logos, transparent (lossless)
   WebP → Better than both, 30% smaller
   AVIF → Even better, newer browsers

2. Resize:
   Serve appropriate size: Mobile → 400px, Desktop → 1200px
   srcset: Browser chooses right size
   <img srcset="img-400.webp 400w, img-1200.webp 1200w">

3. Compression:
   imagemin, squoosh, Sharp (Node.js)
   Quality 80-85% বেশিরভাগ case এ পার্থক্য বোঝা যায় না

4. Lazy Loading:
   <img loading="lazy"> (browser native)

5. CDN:
   Images CDN তে serve করো
   Cloudflare Images auto resize/convert করে

Result: 70-90% image size reduction possible!
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

</details>

<details>
<summary><strong>Q10: Background job queue কীভাবে performance improve করে?</strong></summary>

**উত্তর:**
Heavy operations (email send, PDF generate, image resize) synchronously করলে user request slow হয়।

**Pattern: Async background processing**

```python
# Without queue (slow):
def register_user(data):
    user = create_user(data)
    send_welcome_email(user)     # 2-3 seconds!
    generate_avatar(user)        # 1 second!
    send_sms_notification(user)  # 1 second!
    return {"message": "Registered"}
# Total: 4-5 seconds wait!

# With Celery + Redis queue:
from celery import shared_task

@shared_task
def send_welcome_email(user_id):
    # background এ run হবে
    ...

def register_user(data):
    user = create_user(data)
    send_welcome_email.delay(user.id)    # Queue তে পাঠালো, return immediately
    generate_avatar.delay(user.id)
    send_sms_notification.delay(user.id)
    return {"message": "Registered"}
# Total: ~100ms! User অপেক্ষা করে না।
```

Queue: Redis বা RabbitMQ। Worker: Celery (Python), Bull (Node.js), Sidekiq (Ruby)।

</details>

---

## 🔥 Rapid Fire Q&A — PART 3 & 4

| প্রশ্ন | উত্তর |
|--------|--------|
| Redis default port? | 6379 |
| Cache miss কী? | Cache এ data নেই → DB query |
| Cache hit কী? | Cache এ data আছে → fast response |
| TTL মানে? | Time To Live — cache expiry |
| Rate limit exceed হলে কোন status code? | 429 Too Many Requests |
| Sharding আর Partitioning পার্থক্য? | Sharding multiple servers, Partitioning same server |
| SQL এর ACID এর A মানে? | Atomicity |
| NoSQL এর BASE এর E মানে? | Eventually Consistent |
| Redis sorted set কীসে use? | Leaderboard, ranking |
| Cache Stampede সমাধান? | Mutex lock বা probabilistic refresh |
| Bloom Filter কীসে use? | Cache penetration prevent |
| gzip compression এ কত % ছোট হয়? | Text এ 60-80% |
| Index কোন column এ? | WHERE, JOIN, ORDER BY |
| Master-Slave DB তে write কোথায়? | শুধু Master এ |
| Eventual consistency কোথায় OK? | Social media, DNS |
| Strong consistency কোথায় দরকার? | Banking, payments |
| Connection pool এর সুবিধা? | Connection overhead কমায় |
| Lazy loading কখন? | দরকার হলে তবেই |
| Replication lag কী? | Master → Replica sync delay |
| Hot key problem কী? | একটা cache key এ অতিরিক্ত load |

<div align="right">

[⬆ উপরে যাও](#) | [📚 সূচিপত্র](#) | [PART 5 →](#part5)

</div>

---



<a id="part5"></a>

---

# PART 5: Message Queues & Distributed Systems
### 📨 Async Communication ও Distributed Architecture

> **Interview টিপস:** Message Queue এবং Event-driven architecture বড় system এর backbone। "Order place হলে email, SMS, inventory update — সব কীভাবে handle করবে?" — এই প্রশ্নে Message Queue explain করতে পারলে interviewer impressed হবে।

---

## 5.1 Message Queue Basics

### 📖 সংজ্ঞা
Message Queue হলো **producer এবং consumer এর মধ্যে async buffer** — producer message পাঠায়, consumer নিজের সময়মতো সেটা process করে। দুজনকে একসাথে online থাকতে হয় না।

### 🎯 Real-Life Analogy
> ডাকবাক্সের কথা ভাবো। তুমি চিঠি লিখে ডাকবাক্সে ফেলে দিলে — কাজ শেষ। Postman পরে এসে নিয়ে যাবে, recipient পরে পাবে। তোমাকে recipient এর জন্য অপেক্ষা করতে হলো না।

### 🔄 Message Queue Flow

```
Without Message Queue (Tight Coupling):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Order Service ──synchronous call──▶ Email Service
             ──synchronous call──▶ SMS Service
             ──synchronous call──▶ Inventory Service
             ──synchronous call──▶ Analytics Service

সমস্যা:
❌ Email Service down → Order fail!
❌ Response slow → User অপেক্ষা করে
❌ একটা fail → সব fail (no isolation)
❌ Scaling কঠিন

With Message Queue (Loose Coupling):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Order Service ──publish "order.placed"──▶ [Message Queue]
                                                │
                    ┌───────────────────────────┤
                    ▼           ▼               ▼
             Email Service   SMS Service   Inventory Service
             (subscribes)    (subscribes)  (subscribes)

সুবিধা:
✅ Email Service down হলেও Order complete
✅ Order Service fast response (queue এ দিয়েই return)
✅ প্রতিটা service independently scale
✅ Retry logic queue এ থাকে
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Message Queue Key Concepts

| Concept | মানে | উদাহরণ |
|---------|------|---------|
| Producer | Message পাঠানো | Order Service |
| Consumer | Message receive করে process | Email Service |
| Queue | Message রাখার জায়গা | Kafka Topic, RabbitMQ Queue |
| Message | Data payload | {order_id: 123, user_id: 456} |
| Broker | Queue manage করে | Kafka, RabbitMQ |
| Dead Letter Queue | Failed messages এর জায়গা | Retry শেষে fail হলে |
| Acknowledgment | Consumer process করলে confirm | Message delete হয় |

---

## 5.2 Apache Kafka

### 📖 সংজ্ঞা
Kafka হলো **distributed event streaming platform** — high-throughput, fault-tolerant, real-time data pipeline। LinkedIn তৈরি করেছে, Apache foundation এ।

### 🏗️ Kafka Architecture

```
Kafka Core Components:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Producer]                [Kafka Broker Cluster]              [Consumer]
                    ┌─────────────────────────────┐
Order Service ────▶ │  Topic: "order-events"       │ ──▶ Email Consumer
                    │  ┌──────────────────────────┐│ ──▶ SMS Consumer
                    │  │ Partition 0: msg1, msg4  ││ ──▶ Inventory Consumer
                    │  │ Partition 1: msg2, msg5  ││ ──▶ Analytics Consumer
                    │  │ Partition 2: msg3, msg6  ││
                    │  └──────────────────────────┘│
                    └─────────────────────────────┘
                    
Key Concepts:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Topic: Logical category (order-events, user-events, payment-events)
Partition: Topic এর শার্ড — parallel processing এর জন্য
Offset: প্রতিটা message এর sequential ID (partition এ)
Consumer Group: একসাথে কাজ করা consumers
Replication Factor: কতটা broker এ data copy থাকবে
Retention: Messages কতদিন রাখবে (default 7 days)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔄 Kafka Consumer Group

```
Consumer Group Scaling:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Topic: order-events (3 partitions)
Consumer Group: email-service (3 consumers)

Partition 0 ──▶ Consumer A
Partition 1 ──▶ Consumer B
Partition 2 ──▶ Consumer C
[Parallel processing — 3x throughput!]

Consumer Group: analytics-service (1 consumer)
Partition 0,1,2 ──▶ Consumer D (একাই সব)
[আলাদা group, same messages পায় — independent!]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 💻 Kafka Code Example (Python — kafka-python)

```python
from kafka import KafkaProducer, KafkaConsumer
import json

# Producer:
producer = KafkaProducer(
    bootstrap_servers=['localhost:9092'],
    value_serializer=lambda v: json.dumps(v).encode('utf-8')
)

def on_order_placed(order):
    # Order DB তে save করলাম
    producer.send('order-events', {
        'event': 'order.placed',
        'order_id': order.id,
        'user_id': order.user_id,
        'total': float(order.total),
        'timestamp': order.created_at.isoformat()
    })
    producer.flush()
    return {"message": "Order placed successfully"}  # Fast response!

# Consumer (Email Service):
consumer = KafkaConsumer(
    'order-events',
    bootstrap_servers=['localhost:9092'],
    group_id='email-service',
    auto_offset_reset='earliest',
    value_deserializer=lambda x: json.loads(x.decode('utf-8'))
)

for message in consumer:
    event = message.value
    if event['event'] == 'order.placed':
        send_order_confirmation_email(event['user_id'], event['order_id'])
        print(f"Email sent for order {event['order_id']}")
```

### 📊 Kafka Features

| Feature | Description |
|---------|-------------|
| Throughput | Millions of messages/sec |
| Durability | Disk এ persist, replication |
| Replay | পুরনো messages আবার consume করতে পারো |
| Ordering | Partition এ ordered |
| Retention | Messages দিনের পর দিন রাখে |
| Exactly-once | Exactly-once delivery semantics |
| Stream processing | Kafka Streams, KSQL |

### 🎤 Interview Explanation
> "Kafka high-throughput event streaming এর জন্য। Order place হলে order-events topic এ publish করি। Email service, SMS service, analytics — সবাই subscribe করে — independently consume করে। Kafka messages disk এ store করে তাই replay possible। প্রতি partition এ ordering guarantee আছে। ১ million events/sec handle করতে পারে।"

---

## 5.3 RabbitMQ

### 📖 সংজ্ঞা
RabbitMQ হলো **traditional message broker** — complex routing, multiple messaging patterns support করে। AMQP protocol use করে।

### 🏗️ RabbitMQ Architecture

```
RabbitMQ Core:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Producer]
    │
    ▼
[Exchange] ← Routing decision এখানে
    │
    ├─[Binding: routing_key="email"]──▶ [Queue: email_queue] ──▶ [Email Consumer]
    ├─[Binding: routing_key="sms"]────▶ [Queue: sms_queue]   ──▶ [SMS Consumer]
    └─[Binding: routing_key="*"]──────▶ [Queue: all_queue]   ──▶ [Analytics Consumer]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Exchange Types

| Exchange Type | Routing | Use Case |
|--------------|---------|---------|
| Direct | Exact routing key match | Specific queue routing |
| Fanout | সব queues এ broadcast | Notifications to all |
| Topic | Pattern matching (*.error, logs.#) | Log levels, categories |
| Headers | Message headers based | Complex routing |

### 💻 RabbitMQ Code (Python — pika)

```python
import pika
import json

# Publisher:
connection = pika.BlockingConnection(pika.ConnectionParameters('localhost'))
channel = connection.channel()

channel.exchange_declare(exchange='order_events', exchange_type='topic')

channel.basic_publish(
    exchange='order_events',
    routing_key='order.placed',
    body=json.dumps({'order_id': 123, 'user_id': 456}),
    properties=pika.BasicProperties(
        delivery_mode=2,  # Make message persistent
    )
)

# Consumer (Email):
channel.queue_declare(queue='email_queue', durable=True)
channel.queue_bind(exchange='order_events', queue='email_queue', routing_key='order.*')

def callback(ch, method, properties, body):
    event = json.loads(body)
    send_email(event['user_id'], event['order_id'])
    ch.basic_ack(delivery_tag=method.delivery_tag)  # Acknowledge!

channel.basic_consume(queue='email_queue', on_message_callback=callback)
channel.start_consuming()
```

### 📊 Kafka vs RabbitMQ

| বিষয় | Kafka | RabbitMQ |
|------|-------|---------|
| Paradigm | Event streaming (log) | Message broker (queue) |
| Throughput | Millions/sec | Thousands/sec |
| Message retention | Days/weeks (configurable) | Consumed হলে delete |
| Replay | ✅ Yes (offset replay) | ❌ No (consumed = gone) |
| Ordering | Partition level | Queue level |
| Routing | Topic + partition key | Exchange + routing key |
| Use case | Event streaming, analytics | Task queue, RPC |
| Complexity | Higher | Lower |
| When to use | High volume, replay দরকার | Complex routing, lower volume |

### 🎤 Interview Explanation
> "RabbitMQ traditional task queue — background job, email send, payment processing। Complex routing দরকার হলে RabbitMQ ভালো। কিন্তু high throughput বা event replay দরকার হলে Kafka। BD junior projects এ RabbitMQ বা Celery+Redis common।"

---

## 5.4 Pub/Sub Model

### 📖 সংজ্ঞা
Pub/Sub (Publish-Subscribe) হলো messaging pattern যেখানে **publisher নির্দিষ্ট subscriber কে চেনে না** — topic এ publish করে, interested subscriber রা receive করে।

### 🔄 Pub/Sub vs Point-to-Point

```
Point-to-Point (Queue):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Producer ──▶ [Queue] ──▶ একজন Consumer (only!)
Message একবারই consume হয়
Use: Task distribution

Pub/Sub:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Publisher ──▶ [Topic] ──▶ Subscriber A
                      ──▶ Subscriber B  (সবাই পায়!)
                      ──▶ Subscriber C
Message সব subscriber পায়
Use: Notifications, event broadcasting
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎯 Real-World Examples
- Google Cloud Pub/Sub
- AWS SNS (Simple Notification Service)
- Redis Pub/Sub
- Kafka topics (pub/sub semantics)

### 💻 Redis Pub/Sub

```python
import redis
import threading

r = redis.Redis()

# Publisher:
def publish_notification(user_id, message):
    r.publish(f"user:{user_id}:notifications", message)

# Subscriber:
def listen_for_notifications(user_id):
    pubsub = r.pubsub()
    pubsub.subscribe(f"user:{user_id}:notifications")
    for message in pubsub.listen():
        if message['type'] == 'message':
            print(f"Notification: {message['data']}")
```

---

## 5.5 Event-Driven Architecture

### 📖 সংজ্ঞা
Event-Driven Architecture (EDA) হলো system design approach যেখানে **components events দিয়ে communicate করে** — direct API call এর বদলে।

### 🏗️ Event-Driven Order System

```
E-commerce Event Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
User places order
       │
       ▼
[Order Service] ──publishes──▶ order.placed event
                                      │
              ┌───────────────────────┼──────────────────────────┐
              ▼                       ▼                          ▼
   [Payment Service]         [Inventory Service]      [Notification Service]
   listens: order.placed     listens: order.placed    listens: order.placed
   processes payment         reserves stock           sends email/SMS
   publishes:                publishes:               publishes:
   payment.completed         inventory.reserved       notification.sent
          │                         │
          ▼                         ▼
   [Order Service]          [Order Service]
   updates order status     updates order status
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Event-Driven বনাম Request-Driven

| বিষয় | Request-Driven (REST) | Event-Driven |
|------|----------------------|-------------|
| Coupling | Tight (জানতে হয় কোথায় call করবে) | Loose (event publish করলেই হলো) |
| Availability | Dependent (সব service up থাকতে হবে) | Independent |
| Complexity | Simple | Higher (event tracking কঠিন) |
| Debugging | Easy (call stack আছে) | Hard (distributed tracing দরকার) |
| Scalability | Manual | Auto (consumers add করো) |
| Use case | CRUD, synchronous flows | Complex workflows, microservices |

### 🔑 Event Design Best Practices

```python
# Good Event Structure:
{
    "event_id": "uuid-here",           # Unique ID
    "event_type": "order.placed",      # Namespaced type
    "aggregate_id": "order-123",       # Which entity
    "timestamp": "2026-05-11T10:00:00Z",
    "version": "1.0",                  # Schema version
    "data": {                          # Payload
        "order_id": 123,
        "user_id": 456,
        "items": [...],
        "total": 1500.00
    },
    "metadata": {
        "source": "order-service",
        "correlation_id": "req-789"    # Request tracing
    }
}
```

---

## 5.6 Distributed Systems Basics

### 📖 সংজ্ঞা
Distributed System হলো **multiple computers (nodes) যারা একসাথে কাজ করে single system এর মতো** — user দেখতে পায় না যে এটা আলাদা machines।

### 🔑 Distributed System Challenges

```
The 8 Fallacies of Distributed Computing:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Network is reliable          → Network fail করে!
2. Latency is zero              → Latency আছেই
3. Bandwidth is infinite        → Bandwidth limited
4. Network is secure            → Security threat আছে
5. Topology doesn't change      → Nodes আসে যায়
6. One administrator            → Multiple teams
7. Transport cost is zero       → Data transfer cost আছে
8. Network is homogeneous       → Different hardware/OS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Key Distributed System Concepts

```
1. Clock Synchronization:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Different machines এর clock different হতে পারে
Logical clocks (Lamport timestamps) use করে ordering
Vector clocks: causality track করে

2. Idempotency:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Same operation multiple times = same result
Payment retry safe করতে idempotency key use করো:
POST /payments {idempotency_key: "order-123-attempt-1"}
Duplicate request → same response, no double charge!

3. Two Generals Problem:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Unreliable network এ 100% consensus impossible
→ "At least once", "at most once", "exactly once" trade-offs

4. Split Brain:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Network partition → দুই দল নিজেকে leader ভাবে
→ Data inconsistency
Solution: Quorum (majority vote), Fencing
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 5.7 Distributed Transactions

### 📖 সংজ্ঞা
Distributed Transaction মানে **multiple services/databases এ একসাথে ACID guarantee করা** — সব হবে অথবা কিছুই হবে না।

### 🔄 Two-Phase Commit (2PC)

```
2PC Protocol:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[Coordinator (Order Service)]

Phase 1 — Prepare:
Coordinator ──"prepare"──▶ Payment Service: "তুমি কি deduct করতে পারবে?"
Coordinator ──"prepare"──▶ Inventory Service: "তুমি কি reserve করতে পারবে?"

Payment: "Yes, ready" (lock করলো)
Inventory: "Yes, ready" (lock করলো)

Phase 2 — Commit (or Rollback):
সবাই Yes দিলে:
Coordinator ──"commit"──▶ Payment Service: "এখন commit করো"
Coordinator ──"commit"──▶ Inventory Service: "এখন commit করো"

কেউ No দিলে:
Coordinator ──"rollback"──▶ সবাই

সমস্যা:
❌ Coordinator fail করলে সবাই blocked (locks hold)
❌ Slow (multiple network round trips)
❌ Single point of failure
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Saga Pattern (Modern Solution)

```
Saga Pattern — Choreography:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Order placed
    │
    ▼
Payment Service: deduct money ✅
    │ publishes: payment.completed
    ▼
Inventory Service: reserve stock ✅
    │ publishes: inventory.reserved
    ▼
Shipping Service: create shipment ✅
    │ publishes: shipment.created
    ▼
Order: CONFIRMED ✅

Failure Scenario (Inventory fail):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Payment ✅ → Inventory ❌
    │
    ▼ Compensating Transaction:
Payment Service: refund money ← Inventory publishes: inventory.failed

প্রতিটা step এ forward transaction + compensating transaction define করি
Failure হলে reverse/compensate করি
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 2PC vs Saga

| বিষয় | 2PC | Saga |
|------|-----|------|
| Consistency | Strong (ACID) | Eventual |
| Availability | Lower (locks) | Higher |
| Complexity | Lower | Higher |
| Failure handling | Coordinator rollback | Compensating transactions |
| Performance | Slow | Fast |
| Use case | Tightly coupled, small | Microservices, loosely coupled |

---

## 5.8 Consensus Basics

### 📖 সংজ্ঞা
Consensus মানে **distributed system এ সব nodes একটা value তে agree করা** — leader election, configuration management এ দরকার।

### 🔑 Raft Consensus Algorithm (Simplified)

```
Raft — Leader Election:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
3 nodes: A, B, C
শুরুতে সবাই Follower

Timeout হলে Candidate হয়:
Node A: "আমি leader হতে চাই, vote দাও"
Node B: "OK, A কে vote দিলাম"
Node C: "OK, A কে vote দিলাম"

Majority (2/3) vote পেলে Node A = Leader!

Leader কাজ:
- সব writes Leader এর কাছে যায়
- Leader Followers এ replicate করে
- Majority confirm করলে commit
- Heartbeat পাঠায় (আমি alive)

Leader fail করলে:
- Heartbeat বন্ধ → Followers timeout
- নতুন election শুরু
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🎯 Consensus Tools
- **ZooKeeper:** Distributed coordination (Kafka ব্যবহার করে)
- **etcd:** Kubernetes configuration store (Raft use করে)
- **Consul:** Service discovery + health checking

---

## 5.9 Fault Tolerance

### 📖 সংজ্ঞা
Fault Tolerance মানে **system এর কিছু অংশ fail করলেও পুরো system কাজ করতে থাকবে** — gracefully handle করবে।

### 🔑 Fault Tolerance Patterns

```
1. Circuit Breaker:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
States: CLOSED → OPEN → HALF_OPEN

CLOSED: Normal, requests pass through
Failures exceed threshold → OPEN
OPEN: Requests immediately fail (no call to failing service)
After timeout → HALF_OPEN: Test request
Success → CLOSED | Failure → OPEN

Real code (using pybreaker):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
import pybreaker

payment_breaker = pybreaker.CircuitBreaker(
    fail_max=5,      # 5 failures → OPEN
    reset_timeout=30  # 30 seconds later → HALF_OPEN
)

@payment_breaker
def call_payment_service(amount):
    return requests.post("http://payment-service/pay", json={"amount": amount})

# OPEN state এ call করলে: CircuitBreakerError immediately
# User কে: "Service temporarily unavailable, please try later"
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

2. Retry with Exponential Backoff:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
import time
import random

def call_with_retry(func, max_retries=3, base_delay=1):
    for attempt in range(max_retries):
        try:
            return func()
        except Exception as e:
            if attempt == max_retries - 1:
                raise
            delay = base_delay * (2 ** attempt) + random.uniform(0, 0.5)
            # Attempt 1: ~1s, Attempt 2: ~2s, Attempt 3: ~4s (+ jitter)
            time.sleep(delay)

3. Bulkhead Pattern:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
জাহাজের compartment এর মতো — একটা flood হলে বাকিগুলো safe
Thread pool / connection pool per service:
Payment: max 10 connections
Email: max 5 connections
→ Email service fail করলে Payment service এর connection pool safe

4. Graceful Degradation:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Recommendation service fail করলে:
→ Default/popular products দেখাও (not personalized, but functional)
Search service slow হলে:
→ Basic search চালাও (advanced filters ছাড়া)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Fault Tolerance Metrics

| Metric | মানে | Target |
|--------|------|--------|
| RTO | Recovery Time Objective — কত দ্রুত recover | < 1 hour |
| RPO | Recovery Point Objective — কত data হারাতে পারি | 0 - 1 hour |
| Error Budget | Acceptable downtime | 99.9% → 8.7h/year |

---

## 📋 PART 5: Quick Revision Table

| Concept | এক কথায় | Key Point |
|---------|---------|-----------|
| Message Queue | Async buffer between producer/consumer | Decoupling |
| Kafka | High-throughput event streaming | Replay, partition, retention |
| RabbitMQ | Feature-rich message broker | Complex routing, AMQP |
| Pub/Sub | One publisher, many subscribers | Topic-based |
| Event-Driven | Events দিয়ে communicate | Loose coupling |
| Distributed System | Many computers, one system | Fallacies apply |
| 2PC | Two-phase commit | Strong consistency, slow |
| Saga Pattern | Compensating transactions | Eventual consistency |
| Circuit Breaker | Failing service protect | CLOSED/OPEN/HALF_OPEN |
| Retry + Backoff | Transient failure handle | Exponential delay |
| Bulkhead | Resource isolation | Thread/connection pool |
| Graceful Degradation | Core চলবে, optional বন্ধ | UX focused |
| Idempotency | Same operation = same result | Payment safety |
| Consensus | Nodes agree on value | Raft, Paxos |
| Dead Letter Queue | Failed message storage | Debugging, retry |

---

## 🎯 PART 5: Top 10 Interview Questions

<details>
<summary><strong>Q1: Message Queue কেন use করবে? সরাসরি API call করলে হয় না?</strong></summary>

**উত্তর:**
সরাসরি API call (synchronous) এর সমস্যা:
- **Availability:** Email service down থাকলে order fail!
- **Performance:** Order service email পাঠানোর জন্য অপেক্ষা করে
- **Coupling:** Order service জানতে হয় email service এর address
- **Scaling:** Email slow হলে order service ও slow

Message Queue সমাধান করে:
- **Decoupling:** Order service শুধু event publish করে
- **Availability:** Email service down হলেও order সফল — queue তে থাকবে, পরে process হবে
- **Performance:** Publish করেই return — user দেরি পায় না
- **Retry:** Failed messages automatically retry হয়

Use case: Email, SMS, notification, image processing, report generation।

</details>

<details>
<summary><strong>Q2: Kafka আর RabbitMQ এর মধ্যে কোনটা choose করবে?</strong></summary>

**উত্তর:**
**Kafka choose করবো:**
- ১ million+ events/sec throughput দরকার
- Event replay দরকার (audit log, reprocess)
- Multiple consumer groups same data consume করবে
- Event sourcing, CQRS pattern
- Real-time analytics pipeline

**RabbitMQ choose করবো:**
- Complex routing logic (topic, fanout, direct exchange)
- Traditional task queue (background jobs)
- Message TTL, priority queue দরকার
- Smaller scale, simpler setup
- RPC pattern দরকার

**BD Junior context:** Celery + Redis বেশি common (simple, easy setup)। Kafka enterprise level এ।

</details>

<details>
<summary><strong>Q3: Circuit Breaker কীভাবে implement করবে?</strong></summary>

**উত্তর:**
```python
import time
from enum import Enum

class State(Enum):
    CLOSED = "closed"
    OPEN = "open"
    HALF_OPEN = "half_open"

class CircuitBreaker:
    def __init__(self, fail_max=5, reset_timeout=30):
        self.fail_max = fail_max
        self.reset_timeout = reset_timeout
        self.failures = 0
        self.state = State.CLOSED
        self.last_failure_time = None
    
    def call(self, func, *args, **kwargs):
        if self.state == State.OPEN:
            if time.time() - self.last_failure_time > self.reset_timeout:
                self.state = State.HALF_OPEN
            else:
                raise Exception("Circuit is OPEN — service unavailable")
        
        try:
            result = func(*args, **kwargs)
            self._on_success()
            return result
        except Exception as e:
            self._on_failure()
            raise
    
    def _on_success(self):
        self.failures = 0
        self.state = State.CLOSED
    
    def _on_failure(self):
        self.failures += 1
        self.last_failure_time = time.time()
        if self.failures >= self.fail_max:
            self.state = State.OPEN
```

Production এ Netflix Hystrix, resilience4j (Java) বা pybreaker (Python) use করি।

</details>

<details>
<summary><strong>Q4: Saga pattern কীভাবে implement করবে?</strong></summary>

**উত্তর:**
**Choreography Saga (Event-based):**
```python
# Order Service:
def place_order(order_data):
    order = create_order(order_data)
    # Publish event — কে শুনবে সেটা জানি না
    kafka.publish("order.created", {
        "order_id": order.id,
        "amount": order.total
    })
    return order

# Payment Service (listens to order.created):
def on_order_created(event):
    try:
        deduct_payment(event["amount"], event["order_id"])
        kafka.publish("payment.completed", event)
    except InsufficientFunds:
        kafka.publish("payment.failed", event)  # Compensate!

# Order Service (listens to payment.failed):
def on_payment_failed(event):
    cancel_order(event["order_id"])  # Compensating transaction
```

**Orchestration Saga (Central coordinator):**
```python
class OrderSaga:
    def execute(self, order_data):
        order = self.create_order(order_data)
        
        try:
            self.deduct_payment(order)
            self.reserve_inventory(order)
            self.create_shipment(order)
            self.confirm_order(order)
        except PaymentFailed:
            self.cancel_order(order)
        except InventoryFailed:
            self.refund_payment(order)
            self.cancel_order(order)
```

</details>

<details>
<summary><strong>Q5: Idempotency কীভাবে implement করবে payment এ?</strong></summary>

**উত্তর:**
```python
import uuid
import redis

r = redis.Redis()

def process_payment(idempotency_key: str, amount: float, user_id: int):
    """
    Idempotent payment processing
    Same idempotency_key দিলে same result, no double charge
    """
    cache_key = f"payment:idempotency:{idempotency_key}"
    
    # Already processed check:
    existing = r.get(cache_key)
    if existing:
        return json.loads(existing)  # Same result return করো
    
    # Process payment:
    result = payment_gateway.charge(user_id, amount)
    
    # Store result with TTL (24 hours):
    r.setex(cache_key, 86400, json.dumps(result))
    
    return result

# Client sends unique key per operation:
response = process_payment(
    idempotency_key=f"order-{order_id}-payment",
    amount=1500.00,
    user_id=123
)
```

Network timeout → client retry → same key → same result, no double charge!

</details>

<details>
<summary><strong>Q6: Event Sourcing কী?</strong></summary>

**উত্তর:**
Event Sourcing মানে system এর state current value হিসেবে store না করে **সব events sequence হিসেবে store করা**।

```
Traditional: users table
id=123: balance = 5000

Event Sourcing: account_events table
1. AccountCreated     {user_id: 123, initial_balance: 0}
2. MoneyDeposited     {user_id: 123, amount: 10000}
3. MoneyWithdrawn     {user_id: 123, amount: 3000}
4. MoneyDeposited     {user_id: 123, amount: 1000}
→ Replay করলে: 0 + 10000 - 3000 + 1000 = 8000 ✅

সুবিধা:
✅ Complete audit trail
✅ Time-travel (যেকোনো সময়ের state জানা যায়)
✅ Event replay (bug fix করে reprocess)
✅ CQRS friendly

সমস্যা:
❌ Storage বেশি
❌ Current state পেতে replay করতে হয় (Snapshot দিয়ে optimize)
❌ Complexity বেশি
```

Use case: Banking, financial systems, audit-heavy applications।

</details>

<details>
<summary><strong>Q7: Distributed lock কীভাবে implement করবে?</strong></summary>

**উত্তর:**
একই time এ multiple servers same operation করলে race condition হতে পারে। Distributed lock prevent করে।

```python
import redis
import uuid
import time

r = redis.Redis()

class DistributedLock:
    def __init__(self, key, timeout=10):
        self.key = f"lock:{key}"
        self.timeout = timeout
        self.token = str(uuid.uuid4())  # Unique token
    
    def acquire(self) -> bool:
        # SET NX EX — atomic: শুধু key না থাকলে set করো
        result = r.set(self.key, self.token, nx=True, ex=self.timeout)
        return result is not None
    
    def release(self):
        # Lua script — atomic check + delete
        # শুধু আমার token হলেই delete করো (অন্য কেউ কে না!)
        lua_script = """
        if redis.call("get", KEYS[1]) == ARGV[1] then
            return redis.call("del", KEYS[1])
        else
            return 0
        end
        """
        r.eval(lua_script, 1, self.key, self.token)

# Usage:
def process_order(order_id):
    lock = DistributedLock(f"order:{order_id}", timeout=30)
    if lock.acquire():
        try:
            # Critical section — শুধু একটা server process করবে
            do_process(order_id)
        finally:
            lock.release()
    else:
        raise Exception("Order already being processed")
```

Production এ Redlock algorithm (multiple Redis nodes) বা Zookeeper use করি।

</details>

<details>
<summary><strong>Q8: Dead Letter Queue কীভাবে use করবে?</strong></summary>

**উত্তর:**
Dead Letter Queue (DLQ) হলো failed messages এর গন্তব্য — repeatedly fail করা messages এখানে যায়।

```
Normal Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Queue ──▶ Consumer ──▶ Success ✅ → Message deleted

Failure Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Queue ──▶ Consumer ──▶ Fail → Retry 1
                    ──▶ Fail → Retry 2
                    ──▶ Fail → Retry 3
                    ──▶ Still Fail → Dead Letter Queue ❌

DLQ তে কী করবো:
- Alert পাঠাও (Slack, email)
- Manual investigation করো
- Fix করে re-queue করো
- Error logging এ save করো
```

AWS SQS, RabbitMQ — সব DLQ support করে। Production এ অবশ্যই DLQ configure করতে হবে।

</details>

<details>
<summary><strong>Q9: Microservices এ service discovery কীভাবে কাজ করে?</strong></summary>

**উত্তর:**
Microservices এ services dynamically start/stop হয়, IP change হয়। কীভাবে খুঁজে পাবে?

**Client-side discovery:**
```
Service A → Service Registry (Consul/Eureka): "Payment service কোথায়?"
Registry → "192.168.1.5:8080"
Service A → 192.168.1.5:8080 (directly)
```

**Server-side discovery:**
```
Service A → Load Balancer → Registry lookup → Payment Service
Service A জানে না IP — LB জানে
```

**Kubernetes (Modern):**
```yaml
# Service কে domain name দিয়ে access করো:
http://payment-service:8080  # K8s DNS resolve করে
# কোন IP তে আছে সেটা জানার দরকার নেই!
```

Tools: Consul, Eureka (Netflix), etcd, Kubernetes built-in DNS।

</details>

<details>
<summary><strong>Q10: Eventual consistency এ কীভাবে user experience ভালো রাখবে?</strong></summary>

**উত্তর:**
Eventual consistency তে user stale data দেখতে পারে — কিন্তু UX ভালো রাখার techniques:

1. **Optimistic UI Update:**
```javascript
// Like button click:
// Server response এর আগেই UI তে like দেখাও
setLikeCount(prev => prev + 1);  // Immediate UI
await api.like(postId);           // Background API call
// API fail করলে rollback করো
```

2. **Read-your-own-writes:**
```python
def update_profile(user_id, data):
    db_master.update(user_id, data)
    # User নিজে profile দেখলে master থেকে read
    cache.set(f"user:{user_id}:just_updated", True, ttl=5)

def get_profile(user_id, requesting_user_id):
    if requesting_user_id == user_id and cache.get(f"user:{user_id}:just_updated"):
        return db_master.get(user_id)  # নিজের profile master থেকে
    return db_replica.get(user_id)
```

3. **Feedback messaging:** "Your changes will be visible to others within a few seconds"

4. **Versioning:** Data এর version track করো — stale detect করলে refresh করো।

</details>

<div align="right">

[⬆ উপরে যাও](#) | [📚 সূচিপত্র](#) | [PART 6 →](#part6)

</div>

---

<a id="part6"></a>

---

# PART 6: System Design Case Studies
### 🏗️ Real Systems Design করা শেখো

> **Interview টিপস:** Case study questions এ interviewer দেখতে চায় তুমি কীভাবে একটা real system ধাপে ধাপে design করো। Requirements clarify করো, scale estimate করো, architecture আঁকো, bottleneck ধরো — এই flow follow করলে যেকোনো system design করতে পারবে।

---

## System Design Interview Framework

```
প্রতিটা Case Study তে এই 7 Steps Follow করো:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Step 1: Clarify Requirements (2-3 min)
  → Functional requirements (কী করবে)
  → Non-functional requirements (কত fast, কত available)
  → Scope define করো (কোন feature এই interview এ)

Step 2: Capacity Estimation (2 min)
  → Users কত? DAU/MAU?
  → Read:Write ratio?
  → Storage কত?
  → Bandwidth কত?

Step 3: High-Level Design (5-10 min)
  → Core components identify করো
  → Architecture diagram আঁকো
  → Data flow explain করো

Step 4: Database Design (3-5 min)
  → কোন database use করবে?
  → Schema design করো
  → Indexing strategy

Step 5: API Design (2-3 min)
  → Core endpoints define করো
  → Request/Response format

Step 6: Scale & Optimize (5 min)
  → Bottleneck identify করো
  → Cache কোথায় দেবে?
  → Sharding/replication strategy
  → Load balancing

Step 7: Deep Dive (remaining time)
  → Interviewer যেটা জিজ্ঞেস করে সেটা বিস্তারিত
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 6.1 URL Shortener (bit.ly / TinyURL)

### 📋 Requirements

**Functional:**
- Long URL দিলে short URL তৈরি করবে (e.g., bit.ly/abc123)
- Short URL এ গেলে original URL এ redirect করবে
- Custom alias support (optional)
- Expiry date support (optional)
- Click analytics (optional)

**Non-Functional:**
- Low latency redirect (< 50ms)
- High availability (99.99%)
- Short code unique হতে হবে

### 📊 Capacity Estimation

```
Assumptions:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Write: 100 URLs/second (new URL create)
Read: 10,000 redirects/second (100:1 read:write ratio)
Storage: 100 URLs/sec × 86400 sec × 365 days × 5 years
       = ~15 billion URLs
URL size: ~500 bytes average
Total storage: 15B × 500B ≈ 7.5 TB
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🏗️ Architecture

```
URL Shortener Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Create URL Flow:
[Client] ──POST /shorten {url: "https://long.url/path"}──▶
[API Gateway] ──▶ [URL Service]
                        │
                 Generate short_code (Base62)
                        │
                 [Database] ← store {short_code, long_url, created_at, expiry}
                        │
                 [Cache: Redis] ← pre-cache popular URLs
                        │
                 Return: {short_url: "https://bit.ly/abc123"}

Redirect Flow:
[User] ──GET bit.ly/abc123──▶ [Load Balancer]
                              ──▶ [Redirect Service]
                                        │
                                  Redis cache check
                                  Cache Hit → 301/302 redirect (fast!)
                                  Cache Miss → DB lookup → cache store → redirect
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Short Code Generation

```python
import hashlib
import base64
import string
import random

BASE62 = string.ascii_letters + string.digits  # 62 characters

# Method 1: Random generation:
def generate_short_code(length=7) -> str:
    return ''.join(random.choices(BASE62, k=length))
# 62^7 = 3.5 trillion combinations!

# Method 2: Counter-based (guaranteed unique):
# Global counter (Redis INCR) → Base62 encode
def encode_base62(num: int) -> str:
    result = []
    while num:
        result.append(BASE62[num % 62])
        num //= 62
    return ''.join(reversed(result))

counter = redis.incr("url_counter")  # Atomic increment
short_code = encode_base62(counter)  # e.g., 1000000 → "4c92"

# Method 3: MD5 Hash (first 7 chars):
def hash_url(url: str) -> str:
    return hashlib.md5(url.encode()).hexdigest()[:7]
# Risk: collision possible
```

### 🗄️ Database Design

```sql
CREATE TABLE urls (
    id          BIGINT PRIMARY KEY AUTO_INCREMENT,
    short_code  VARCHAR(10) UNIQUE NOT NULL,
    long_url    TEXT NOT NULL,
    user_id     BIGINT,              -- NULL if anonymous
    created_at  TIMESTAMP DEFAULT NOW(),
    expires_at  TIMESTAMP,           -- NULL = no expiry
    click_count BIGINT DEFAULT 0
);

CREATE INDEX idx_short_code ON urls(short_code);  -- Primary lookup

-- Analytics table:
CREATE TABLE url_clicks (
    id          BIGINT PRIMARY KEY AUTO_INCREMENT,
    short_code  VARCHAR(10),
    clicked_at  TIMESTAMP,
    ip_address  VARCHAR(45),
    user_agent  TEXT,
    country     VARCHAR(2)
);
```

### 🔌 API Design

```
POST /api/v1/shorten
Request:  { "url": "https://very-long-url.com/path", "custom_alias": "mylink", "expires_in": 86400 }
Response: { "short_url": "https://bit.ly/abc123", "short_code": "abc123", "expires_at": "..." }

GET /{short_code}
Response: 301 Redirect to long_url (or 302 for analytics tracking)

GET /api/v1/analytics/{short_code}
Response: { "clicks": 1234, "top_countries": [...], "clicks_by_day": [...] }

DELETE /api/v1/urls/{short_code}
Response: 204 No Content
```

### ⚡ Scaling Strategy

```
Bottlenecks ও Solutions:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Redirect latency:
   Solution: Redis cache (short_code → long_url)
   Cache TTL: 24 hours for popular URLs
   Cache Hit Rate: 90%+ → most redirects from Redis only!

2. Database write throughput:
   Solution: Write to DB async (queue) + cache immediately
   Popular URLs pre-cache করো (warming)

3. Database read scaling:
   Solution: Read replicas
   Redirect service → replica reads only

4. Analytics write load:
   Solution: Kafka → analytics consumer async
   Redirect service শুধু event publish করে, DB write করে না

5. Short code uniqueness (distributed):
   Solution: Centralized counter (Redis INCR) বা
             Range-based allocation (Server A gets 1-1M, Server B gets 1M-2M)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 6.2 Chat Application (WhatsApp/Messenger)

### 📋 Requirements

**Functional:**
- One-to-one messaging
- Group chat (max 256 members)
- Message delivery status (sent/delivered/read)
- Online/offline status
- Media files (image, video)
- Message history

**Non-Functional:**
- Real-time delivery (< 100ms)
- High availability (99.99%)
- 1 billion users, 100 billion messages/day

### 📊 Capacity Estimation

```
Scale:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DAU: 500M users
Messages/day: 100B
Messages/sec: 100B / 86400 ≈ 1.15M messages/sec!
Average message size: 100 bytes (text)
Storage/day: 100B × 100B = 10TB/day
Media: separate object storage (S3)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🏗️ Architecture

```
Chat Application Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[User A App] ←──WebSocket──▶ [Chat Server A]
[User B App] ←──WebSocket──▶ [Chat Server B]

Message Flow (A → B):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. User A WebSocket → Chat Server A: {"to": "B", "msg": "Hello!"}
2. Chat Server A → Message Queue (Kafka): message event publish
3. Message Service → DB save: message_id, content, sender, receiver, timestamp
4. Routing Service: "User B কোন Chat Server এ আছে?" (Redis)
5. Chat Server B → User B WebSocket: message push

Components:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Load Balancer] ──▶ [Chat Servers (WebSocket)] ──▶ [Kafka]
                                                        │
[Presence Service]  [User Service]              [Message Service]
(online/offline)    (auth, profile)             (store, deliver)
      │                   │                            │
 [Redis]             [User DB]                  [Message DB]
 (online map)        (PostgreSQL)               (Cassandra)
                                                        │
                                              [Media Storage: S3]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🗄️ Database Design

```sql
-- Users:
CREATE TABLE users (id, username, phone, created_at);

-- Messages (Cassandra — write-heavy, time-series):
CREATE TABLE messages (
    conversation_id UUID,
    message_id      TIMEUUID,  -- Time-ordered UUID
    sender_id       UUID,
    content         TEXT,
    media_url       TEXT,
    message_type    VARCHAR,   -- text/image/video/audio
    status          VARCHAR,   -- sent/delivered/read
    created_at      TIMESTAMP,
    PRIMARY KEY (conversation_id, message_id)
) WITH CLUSTERING ORDER BY (message_id DESC);

-- Online presence (Redis):
HSET user:presence:123 status "online" last_seen "2026-05-11T10:00:00"
EXPIRE user:presence:123 300  -- 5 min TTL (heartbeat refresh)

-- WebSocket connection routing (Redis):
SET user:socket:123 "chat-server-7"  -- user 123 → server 7
```

### 🔌 API Design

```
WebSocket Events:
SEND:    { type: "message", to: "user_id", content: "Hello!", msg_id: "client-uuid" }
RECEIVE: { type: "message", from: "user_id", content: "Hello!", msg_id: "...", ts: "..." }
STATUS:  { type: "status", msg_id: "...", status: "delivered" }
TYPING:  { type: "typing", in: "conversation_id" }

REST API:
GET  /api/v1/conversations                    → conversation list
GET  /api/v1/conversations/{id}/messages      → message history (paginated)
POST /api/v1/media/upload                     → get upload URL (S3 presigned)
PUT  /api/v1/messages/{id}/read               → mark as read
```

### ⚡ Key Design Decisions

```
1. WebSocket vs HTTP Polling:
   WebSocket — persistent, server can push, low latency ✅

2. Message Storage — Cassandra:
   Write-heavy (1M+ writes/sec), time-series queries, horizontal scale ✅
   "Give me last 50 messages of conversation X" → efficient

3. Offline Message Delivery:
   User offline → message store in DB
   User online → pull undelivered messages (or push via Notification Service)

4. End-to-End Encryption:
   Client generate key pair
   Public key server এ store
   Message encrypt with recipient's public key
   Server decrypt করতে পারে না!

5. Message Fan-out (Group Chat):
   Group এ 256 members → 1 message → 256 deliveries
   Fan-out service: Message Queue → parallel delivery workers
```

---

## 6.3 Social Media Feed (Facebook/Twitter)

### 📋 Requirements
- User post create করবে (text, image, video)
- Friends/followers এর posts feed এ দেখাবে
- Like, comment, share
- Real-time notifications

### 🏗️ Feed Generation Architecture

```
Feed Generation — Two Approaches:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Approach 1: Pull Model (Read time generation):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
User requests feed
→ Get all followers
→ Get their recent posts
→ Merge + Sort + Rank
→ Return feed

✅ Storage সহজ (no pre-computation)
❌ Slow for users with many followers
❌ Every request এ heavy computation

Approach 2: Push Model (Write time fan-out):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
User posts
→ Get all followers list
→ Pre-compute feed for EACH follower
→ Store in each follower's feed cache

User requests feed → Simply read pre-computed feed!

✅ Feed read fast
❌ Celebrity post (10M followers) → 10M writes! (Fan-out explosion)

Approach 3: Hybrid (Twitter/Instagram approach):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Normal users: Push model (pre-compute feed)
Celebrities (1M+ followers): Pull model (read time merge)
When fetching feed: pre-computed + celebrity posts merge করো
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🏗️ Full Architecture

```
Social Media System:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Client] ──▶ [API Gateway]
                    │
          ┌─────────┼──────────┐
          ▼         ▼          ▼
    [Post Service] [User]  [Feed Service]
    [Like Service] [Service] [Notification]
          │              │        Service
    [Post DB:         [User DB]
     PostgreSQL]         │
          │          [Follow DB:
    [Media: S3]       PostgreSQL]
          │                │
    [Kafka:           [Feed Cache:
     post.created]     Redis]
          │
   [Fan-out Worker]
   (reads followers → updates feed cache)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🗄️ Database Design

```sql
-- Posts:
CREATE TABLE posts (
    id          BIGSERIAL PRIMARY KEY,
    user_id     BIGINT REFERENCES users(id),
    content     TEXT,
    media_urls  JSONB,
    like_count  INT DEFAULT 0,
    created_at  TIMESTAMP DEFAULT NOW()
);

-- Follows (graph-like):
CREATE TABLE follows (
    follower_id BIGINT,
    followee_id BIGINT,
    created_at  TIMESTAMP DEFAULT NOW(),
    PRIMARY KEY (follower_id, followee_id)
);
CREATE INDEX idx_followee ON follows(followee_id);  -- "কে আমাকে follow করে?"

-- Feed (Redis Sorted Set — score=timestamp):
ZADD feed:user:123 1715428800 "post:456"
ZADD feed:user:123 1715432400 "post:789"
ZREVRANGE feed:user:123 0 19  -- Latest 20 posts
```

---

## 6.4 Online Banking System

### 📋 Requirements
- Account management (create, view balance)
- Money transfer (within bank, inter-bank)
- Transaction history
- Card management
- Fraud detection

### 🏗️ Architecture

```
Banking System Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Mobile/Web] ──HTTPS──▶ [WAF] ──▶ [API Gateway]
                                        │
                              [Auth Service (JWT)]
                                        │
                    ┌───────────────────┼───────────────────┐
                    ▼                   ▼                   ▼
            [Account Service]  [Transaction Service]  [Card Service]
                    │                   │
            [Account DB:        [Transaction DB:
             PostgreSQL]         PostgreSQL (ACID)]
             (ACID critical)     (Immutable — no update/delete)
                                        │
                               [Kafka: transaction.completed]
                                        │
                    ┌──────────────────┤
                    ▼                  ▼
            [Fraud Detection]  [Notification Service]
            [ML Service]       (Email, SMS, Push)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Critical Design Decisions

```
1. ACID Transactions (Double-entry bookkeeping):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
BEGIN TRANSACTION;
    -- Debit from sender:
    UPDATE accounts SET balance = balance - 5000
    WHERE id = 123 AND balance >= 5000;  -- Check balance atomically
    
    -- Credit to receiver:
    UPDATE accounts SET balance = balance + 5000 WHERE id = 456;
    
    -- Audit log:
    INSERT INTO transactions (from_id, to_id, amount, type) 
    VALUES (123, 456, 5000, 'transfer');
COMMIT;

2. Idempotency (No double debit!):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Every transfer request has unique idempotency_key
Duplicate request → same response, no double debit

3. Optimistic Locking (Concurrent transfer):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
accounts table has version column
UPDATE accounts SET balance = balance - 5000, version = version + 1
WHERE id = 123 AND version = current_version;
0 rows updated → retry (someone else updated)

4. Immutable Transaction Log:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Transactions never UPDATE or DELETE
Only INSERT — audit trail intact
Append-only for compliance
```

---

## 6.5 Food Delivery App (Pathao Food / Shohoz Food)

### 📋 Requirements
- Restaurant browse, menu view
- Order placement
- Real-time order tracking
- Delivery person assignment
- Payment
- Rating/review

### 🏗️ Architecture

```
Food Delivery Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Customer App]    [Restaurant App]    [Delivery App]
       │                 │                  │
       └─────────────────┴──────────────────┘
                         │
                   [API Gateway]
          ┌──────────────┼───────────────┐
          ▼              ▼               ▼
  [Restaurant Service] [Order Service] [Delivery Service]
  (menu, availability)  (ACID trans)   (assignment, tracking)
          │              │               │
  [Restaurant DB]  [Order DB]     [Location Service]
                         │         (Redis GeoSpatial)
                   [Kafka:         GEOADD, GEORADIUS
                    order.placed]
                         │
          ┌──────────────┴──────────────┐
          ▼                             ▼
  [Notification Service]       [Delivery Assignment]
  (Push, SMS)                  (nearest available driver)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Real-Time Location Tracking

```python
# Redis GeoSpatial — Delivery person location:
import redis
r = redis.Redis()

# Delivery person location update (every 5 seconds):
def update_location(driver_id: str, lat: float, lng: float):
    r.geoadd("drivers:online", lng, lat, driver_id)
    r.expire(f"driver:{driver_id}:active", 30)  # Timeout = offline

# Find nearest available drivers:
def find_nearest_drivers(restaurant_lat, restaurant_lng, radius_km=5):
    drivers = r.georadius(
        "drivers:online",
        restaurant_lng, restaurant_lat,
        radius_km, unit='km',
        withcoord=True,
        withdist=True,
        sort='ASC',
        count=10
    )
    return drivers

# Assignment algorithm:
def assign_driver(order, drivers):
    for driver in drivers:
        driver_id, distance, coords = driver
        if is_driver_available(driver_id):
            send_order_request(driver_id, order)
            # Driver accepts → assigned!
            # No response in 30 sec → next driver
            break
```

### 🗄️ Database Design

```sql
-- Orders (State machine):
CREATE TABLE orders (
    id              BIGSERIAL PRIMARY KEY,
    customer_id     BIGINT,
    restaurant_id   BIGINT,
    driver_id       BIGINT,
    status          VARCHAR(20),  -- PLACED, CONFIRMED, PREPARING, PICKED_UP, DELIVERED
    total_amount    DECIMAL(10,2),
    delivery_address JSONB,
    estimated_time  INT,          -- minutes
    created_at      TIMESTAMP DEFAULT NOW(),
    delivered_at    TIMESTAMP
);

-- Real-time tracking (time-series in InfluxDB or Cassandra):
-- driver_id, lat, lng, timestamp
-- Query: "last position of driver X" → fast!
```

---

## 6.6 Ride Sharing App (Pathao / Uber)

### 📋 Requirements
- Rider requests ride
- Nearest driver match করবে
- Real-time tracking
- Dynamic pricing (surge)
- Payment

### 🏗️ Architecture

```
Ride Sharing Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Rider App]                         [Driver App]
     │                                    │
     │──POST /rides/request               │──PUT /drivers/location
     ▼                                    ▼
[API Gateway] ──────────────────▶ [Location Service]
     │                            (Redis GeoSpatial)
     ▼                                    │
[Ride Service]                            │
     │                           [Driver Matching Service]
     │←──── Find nearest driver ──────────┤
     │                                    │
     │──Notify driver (WebSocket/Push)    │
     │                                    │
[Ride DB]    [Pricing Service]    [ETA Service]
(PostgreSQL) (surge calculation)  (routing engine)
     │
[Kafka: ride.events]
     │
[Analytics, Notification, Payment]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Surge Pricing Algorithm

```python
def calculate_surge_price(pickup_lat, pickup_lng, base_price):
    """
    Supply-Demand based surge pricing
    """
    radius = 2  # km

    # Available drivers nearby:
    available_drivers = redis.georadius(
        "drivers:available", pickup_lng, pickup_lat, radius, unit='km'
    )
    driver_count = len(available_drivers)

    # Active ride requests nearby:
    demand = redis.get(f"demand:{pickup_lat:.2f}:{pickup_lng:.2f}") or 0
    demand = int(demand)

    # Surge calculation:
    if driver_count == 0:
        surge_multiplier = 3.0  # No driver → 3x
    elif demand / max(driver_count, 1) > 2:
        surge_multiplier = 2.0  # High demand → 2x
    elif demand / max(driver_count, 1) > 1:
        surge_multiplier = 1.5  # Moderate demand → 1.5x
    else:
        surge_multiplier = 1.0  # Normal

    return base_price * surge_multiplier
```

---

## 6.7 YouTube-like Video Platform

### 📋 Requirements
- Video upload
- Video streaming (adaptive bitrate)
- Search
- Recommendations
- Comments, likes
- Subscriptions

### 🏗️ Architecture

```
Video Platform Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Upload Flow:
[Creator] ──upload raw video──▶ [Upload Service] ──▶ [S3: raw-videos/]
                                                          │
                                                    [Kafka: video.uploaded]
                                                          │
                                               [Video Processing Workers]
                                               Transcode: 360p, 720p, 1080p, 4K
                                               Thumbnail generate
                                               Audio extract
                                                          │
                                                [S3: processed-videos/]
                                                          │
                                                    [CDN distribution]

Watch Flow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Viewer] ──GET /watch?v=abc123──▶ [API Gateway]
                                        │
                               [Video Metadata Service]
                               (title, description, URLs)
                                        │
                               [CDN PoP nearest to user]
                               Adaptive Bitrate Streaming (HLS/DASH)
                               Good network → 1080p
                               Slow network → auto-switch to 360p
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Key Design Points

```
1. Video Transcoding:
   Raw upload → FFmpeg workers → Multiple resolutions
   Distributed: Different workers handle different videos
   Queue: Kafka/SQS for job distribution

2. Adaptive Bitrate Streaming (HLS):
   Video → chunks (2-10 second segments)
   Player: bandwidth monitor করে quality adjust
   .m3u8 manifest → lists all quality options

3. View Count (Eventually Consistent):
   INCR in Redis (fast, atomic)
   Batch write to DB every 30 seconds
   Exact count not critical (1M vs 1.001M doesn't matter)

4. Search:
   Elasticsearch: full-text on title, description, tags
   Autocomplete: Redis Sorted Set or Elasticsearch
   ML ranking: engagement signals (watch time, likes)

5. Recommendations:
   Collaborative filtering: similar users watched similar videos
   Content-based: video metadata, tags
   Offline ML pipeline → precomputed recommendations stored
```

---

## 6.8 E-commerce System (Chaldal/Daraz-like)

### 📋 Requirements
- Product catalog (search, filter)
- Shopping cart
- Order management
- Inventory management
- Payment processing
- Delivery tracking

### 🏗️ Architecture

```
E-commerce Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Web/Mobile] ──▶ [CDN] (static assets)
                 [API Gateway] (auth, routing, rate limit)
                        │
    ┌────────────────────┼────────────────────────────┐
    ▼                    ▼                            ▼
[Product Service]  [Cart Service]           [Order Service]
[Search: ES]       [Redis session]          [Saga pattern]
[DB: PostgreSQL]                            [DB: PostgreSQL]
    │                                            │
[Inventory]                              [Payment Service]
[Service]                                [3rd party gateway]
[Redis atomic]                                   │
                                        [Kafka: order.placed]
                                                 │
                                    ┌────────────┤
                                    ▼            ▼
                            [Notification]  [Inventory
                            [Service]        Reserve]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Inventory Race Condition Solution

```python
# Problem: 100 users একসাথে last item কিনতে চায়!
# Without atomic operation → oversell!

# Solution: Redis atomic decrement with check:
def reserve_inventory(product_id: str, quantity: int) -> bool:
    key = f"inventory:{product_id}"
    
    lua_script = """
    local current = tonumber(redis.call('get', KEYS[1])) or 0
    if current >= tonumber(ARGV[1]) then
        redis.call('decrby', KEYS[1], ARGV[1])
        return 1  -- success
    else
        return 0  -- insufficient stock
    end
    """
    result = r.eval(lua_script, 1, key, quantity)
    return bool(result)
    # Atomic! No race condition.
```

---

## 6.9 Hospital Management System

### 📋 Requirements
- Patient registration
- Doctor appointment booking
- Medical records management
- Lab results
- Prescription management
- Billing

### 🏗️ Architecture

```
Hospital System Architecture:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Patient Portal] [Doctor App] [Admin Dashboard]
        │               │             │
        └───────────────┴─────────────┘
                        │
                  [API Gateway]
         ┌──────────────┼──────────────────────┐
         ▼              ▼                      ▼
 [Patient Service] [Appointment Service] [Medical Records]
 [Registration]    [Scheduling]          [EHR Service]
         │              │                      │
 [Patient DB]    [Appointment DB]       [Records DB]
 (PostgreSQL)    (PostgreSQL)           (PostgreSQL + S3 for files)
         │
 [Billing Service]  [Lab Service]  [Pharmacy Service]
         │              │
 [Payment Gateway] [Lab Results DB]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🔑 Critical Design Decisions

```
1. HIPAA/Data Privacy (Bangladesh DPAI consideration):
   - Patient data encrypted at rest (AES-256)
   - TLS in transit
   - Audit log: কে কখন কোন record দেখেছে
   - Role-based access: Doctor শুধু তার patient দেখবে

2. Appointment Slot Management:
   - Distributed lock (Redis) — same slot double booking prevent
   - Doctor schedule management (time-slot based)

3. Medical Records:
   - Immutable records (compliance)
   - Version control (amendments, not deletions)
   - Fast retrieval (indexed by patient_id, date)
   - Large files (X-ray, MRI) → S3

4. Lab Integration:
   - HL7 FHIR standard (international healthcare data format)
   - Lab results → automatically push to doctor dashboard
   - Critical value alerts (immediate notification)
```

---

## 📋 PART 6: Case Studies Quick Reference

| System | DB Choice | Cache | Queue | Special |
|--------|-----------|-------|-------|---------|
| URL Shortener | PostgreSQL | Redis (redirects) | - | Base62 encoding |
| Chat App | Cassandra | Redis (presence) | Kafka | WebSocket, fan-out |
| Social Feed | PostgreSQL | Redis (feed) | Kafka | Hybrid fan-out |
| Banking | PostgreSQL | Redis (session) | Kafka | ACID, idempotency |
| Food Delivery | PostgreSQL | Redis Geo | Kafka | Location, state machine |
| Ride Sharing | PostgreSQL | Redis Geo | Kafka | Surge pricing, matching |
| Video Platform | PostgreSQL + S3 | CDN | SQS/Kafka | HLS, transcoding |
| E-commerce | PostgreSQL + ES | Redis | Kafka | Inventory atomic |
| Hospital | PostgreSQL + S3 | Redis | - | RBAC, immutable records |

---

## 🎯 PART 6: Top Interview Questions

<details>
<summary><strong>Q1: URL Shortener design করো (30 মিনিটে)</strong></summary>

**Framework দিয়ে উত্তর:**
1. **Requirements:** Short URL create, redirect, analytics optional
2. **Scale:** 100 writes/sec, 10K reads/sec, 7.5TB storage 5 years
3. **Architecture:** API → URL Service → DB + Redis Cache
4. **DB:** PostgreSQL (short_code UNIQUE INDEX)
5. **Short code:** Counter-based Base62 (no collision)
6. **Cache:** Redis (short_code → long_url, TTL 24h)
7. **Redirect:** 302 (tracking) vs 301 (client cache)
8. **Scale:** Read replicas + Redis → 99%+ cache hit

</details>

<details>
<summary><strong>Q2: WhatsApp design করার সবচেয়ে tricky part কী?</strong></summary>

**উত্তর:**
Tricky parts:
1. **Message delivery at scale:** 1M+ msg/sec → Kafka fan-out
2. **Offline delivery:** User offline → store, deliver when online
3. **Group chat fan-out:** 256 members → 256 pushes
4. **End-to-end encryption:** Server key নেই → Signal Protocol
5. **Multi-device sync:** WhatsApp Web → same messages সব device এ
6. **Presence (online/offline):** 500M users → Redis with TTL + heartbeat

</details>

<details>
<summary><strong>Q3: Social media feed design এ Fan-out on Write আর Fan-out on Read এর পার্থক্য কী?</strong></summary>

**উত্তর:**
- **Fan-out on Write:** Post করার সময় সব followers এর feed update করো। Read fast, Write expensive। Celebrity (10M followers) → 10M Redis operations!

- **Fan-out on Read:** Feed request এর সময় followers এর posts merge করো। Write সহজ, Read expensive। Millions of users এর feed generate করতে slow।

- **Hybrid (Twitter/Instagram):** Regular users → write-time fan-out। Celebrities → read-time pull and merge।

</details>

<details>
<summary><strong>Q4: Banking system এ double debit কীভাবে prevent করবে?</strong></summary>

**উত্তর:**
3 layer protection:
1. **Idempotency key:** Client unique key পাঠায় → duplicate request → same response
2. **Database unique constraint:** `UNIQUE(idempotency_key)` → DB level block
3. **SELECT FOR UPDATE + Check:** `UPDATE accounts SET balance=balance-X WHERE id=Y AND balance>=X` → atomic check
4. **Distributed lock:** High-value transfers এ Redis lock

```sql
-- Atomic: deduct only if sufficient balance
UPDATE accounts 
SET balance = balance - 5000, version = version + 1
WHERE id = 123 AND balance >= 5000 AND version = 7;
-- 0 rows → insufficient balance or concurrent modification
```

</details>

<details>
<summary><strong>Q5: Video streaming এ adaptive bitrate কীভাবে কাজ করে?</strong></summary>

**উত্তর:**
HLS (HTTP Live Streaming):
1. Video → FFmpeg → multiple quality (360p, 720p, 1080p)
2. প্রতিটা quality → 2-10 second chunks (.ts files)
3. Manifest file (.m3u8) → lists all qualities + chunk URLs

```
#EXTM3U
#EXT-X-STREAM-INF:BANDWIDTH=800000,RESOLUTION=640x360
360p/playlist.m3u8
#EXT-X-STREAM-INF:BANDWIDTH=2400000,RESOLUTION=1280x720
720p/playlist.m3u8
#EXT-X-STREAM-INF:BANDWIDTH=4800000,RESOLUTION=1920x1080
1080p/playlist.m3u8
```

Player logic:
- Network bandwidth measure করে
- Good bandwidth → 1080p chunk download
- Bandwidth drops → next chunk থেকে 360p switch
- Buffer আছে → seamless quality switch

CDN এর edge servers এই chunks cache করে। User কাছের CDN থেকে পায় — low latency।

</details>

<div align="right">

[⬆ উপরে যাও](#) | [📚 সূচিপত্র](#) | [PART 7 →](#part7)

</div>

---

*হ্যান্ডবুক তৈরিতে: Senior Software Architect, Backend Engineer & System Design Interviewer*
*Version: 1.0 | তারিখ: মে ২০২৬*


<a id="part7"></a>

---

# PART 7: Low-Level Design (LLD)
### 🧩 SOLID, Design Patterns ও Object-Oriented Design

> **Interview টিপস:** LLD interview এ interviewer দেখতে চায় তুমি real-world problem কে clean, maintainable code এ রূপ দিতে পারো কিনা। SOLID principles ও common Design Patterns জানলে যেকোনো LLD প্রশ্নে confident থাকবে।

---

## 7.1 SOLID Principles

SOLID হলো 5টি object-oriented design principle যা code কে **maintainable, extensible ও testable** রাখে।

---

### S — Single Responsibility Principle (SRP)

> **"একটা class এর শুধু একটাই কারণ থাকবে change হওয়ার।"**

```python
# ❌ BAD — একটা class এ অনেক দায়িত্ব:
class OrderService:
    def create_order(self, items):
        # Order logic
        pass
    def send_email(self, user, order):  # ← Email responsibility!
        smtp.send(...)
    def generate_invoice_pdf(self, order):  # ← PDF responsibility!
        pdf.create(...)
    def save_to_db(self, order):  # ← DB responsibility!
        db.save(...)

# ✅ GOOD — প্রতিটা class এর একটা দায়িত্ব:
class OrderService:
    def __init__(self, repo, emailer, invoicer):
        self.repo = repo
        self.emailer = emailer
        self.invoicer = invoicer

    def create_order(self, items):
        order = Order(items)
        self.repo.save(order)
        self.emailer.send_confirmation(order)
        self.invoicer.generate(order)
        return order

class OrderRepository:
    def save(self, order): db.save(order)

class EmailService:
    def send_confirmation(self, order): smtp.send(...)

class InvoiceService:
    def generate(self, order): pdf.create(...)
```

---

### O — Open/Closed Principle (OCP)

> **"Software entity open for extension, but closed for modification।"**  
> নতুন feature যোগ করতে existing code বদলাতে হবে না — extend করবো।

```python
# ❌ BAD — নতুন payment type যোগ করতে existing code বদলাতে হয়:
class PaymentProcessor:
    def process(self, payment_type, amount):
        if payment_type == "bkash":
            bkash.charge(amount)
        elif payment_type == "nagad":
            nagad.charge(amount)
        elif payment_type == "card":   # ← নতুন type → code change!
            card.charge(amount)

# ✅ GOOD — নতুন type যোগ করতে শুধু নতুন class লিখবো:
from abc import ABC, abstractmethod

class PaymentMethod(ABC):
    @abstractmethod
    def charge(self, amount: float) -> bool:
        pass

class BkashPayment(PaymentMethod):
    def charge(self, amount: float) -> bool:
        return bkash_api.charge(amount)

class NagadPayment(PaymentMethod):
    def charge(self, amount: float) -> bool:
        return nagad_api.charge(amount)

class CardPayment(PaymentMethod):   # ← New class, no existing code change!
    def charge(self, amount: float) -> bool:
        return card_gateway.charge(amount)

class PaymentProcessor:
    def process(self, payment: PaymentMethod, amount: float):
        return payment.charge(amount)
```

---

### L — Liskov Substitution Principle (LSP)

> **"Subclass দিয়ে parent class replace করলেও program ঠিকঠাক কাজ করবে।"**

```python
# ❌ BAD — Square inherits Rectangle কিন্তু behavior ভাঙে:
class Rectangle:
    def set_width(self, w): self.width = w
    def set_height(self, h): self.height = h
    def area(self): return self.width * self.height

class Square(Rectangle):
    def set_width(self, w):
        self.width = w
        self.height = w   # ← Square constraint! Rectangle এর behavior ভাঙে
    def set_height(self, h):
        self.width = h
        self.height = h

def print_area(rect: Rectangle):
    rect.set_width(5)
    rect.set_height(10)
    print(rect.area())  # Rectangle → 50 ✅, Square → 100 ❌ (LSP violated!)

# ✅ GOOD — Common abstraction:
class Shape(ABC):
    @abstractmethod
    def area(self) -> float: pass

class Rectangle(Shape):
    def __init__(self, w, h): self.w = w; self.h = h
    def area(self) -> float: return self.w * self.h

class Square(Shape):
    def __init__(self, s): self.s = s
    def area(self) -> float: return self.s * self.s
```

---

### I — Interface Segregation Principle (ISP)

> **"Client কে এমন methods এ depend করতে বাধ্য করবে না যা সে use করে না।"**

```python
# ❌ BAD — Fat interface:
class Worker(ABC):
    @abstractmethod
    def work(self): pass
    @abstractmethod
    def eat(self): pass    # Robot কে এটা implement করতে হয়!
    @abstractmethod
    def sleep(self): pass  # Robot কে এটাও!

class Robot(Worker):
    def work(self): print("Working")
    def eat(self): raise NotImplementedError  # ❌ Forced!
    def sleep(self): raise NotImplementedError  # ❌ Forced!

# ✅ GOOD — Segregated interfaces:
class Workable(ABC):
    @abstractmethod
    def work(self): pass

class Eatable(ABC):
    @abstractmethod
    def eat(self): pass

class Human(Workable, Eatable):
    def work(self): print("Working")
    def eat(self): print("Eating")

class Robot(Workable):       # শুধু Workable implement করে
    def work(self): print("Working")
```

---

### D — Dependency Inversion Principle (DIP)

> **"High-level modules low-level modules এর উপর depend করবে না — উভয়ই abstraction এর উপর depend করবে।"**

```python
# ❌ BAD — High-level OrderService directly depends on MySQL:
class OrderService:
    def __init__(self):
        self.db = MySQLDatabase()  # ← Concrete class! Swap করতে পারবো না।

    def save_order(self, order):
        self.db.execute("INSERT INTO orders ...")

# ✅ GOOD — Depend on abstraction (interface):
class OrderRepository(ABC):
    @abstractmethod
    def save(self, order) -> None: pass
    @abstractmethod
    def find_by_id(self, id: int): pass

class MySQLOrderRepository(OrderRepository):
    def save(self, order): mysql_db.execute("INSERT ...")
    def find_by_id(self, id): return mysql_db.query("SELECT ...")

class MongoOrderRepository(OrderRepository):  # Swap করলেও OrderService change নেই!
    def save(self, order): mongo_col.insert_one(order.to_dict())
    def find_by_id(self, id): return mongo_col.find_one({"_id": id})

class OrderService:
    def __init__(self, repo: OrderRepository):  # ← Interface inject করো
        self.repo = repo

    def create_order(self, items):
        order = Order(items)
        self.repo.save(order)
        return order
```

### 📊 SOLID Quick Summary

| Principle | এক কথায় | মনে রাখার উপায় |
|-----------|---------|----------------|
| **S**RP | একটা class, একটা কাজ | Chef শুধু রান্না করে |
| **O**CP | Extend করো, modify করো না | পুরনো code touch না করে নতুন feature |
| **L**SP | Subclass = Parent এর drop-in replacement | Square is-a Shape, not Rectangle |
| **I**SP | Small, focused interfaces | Robot কে eat() implement করতে বাধ্য না |
| **D**IP | Interface এর উপর depend করো | OrderService → Repository (interface) |

---

## 7.2 Design Patterns

Design Patterns হলো **common software problems এর proven solutions** — প্রতিবার নতুন করে ভাবতে হয় না।

### 3 Categories:

| Category | উদ্দেশ্য | Patterns |
|----------|---------|---------|
| **Creational** | Object কীভাবে তৈরি করবো | Singleton, Factory, Builder, Prototype |
| **Structural** | Objects কীভাবে compose করবো | Adapter, Decorator, Facade, Proxy |
| **Behavioral** | Objects কীভাবে communicate করবে | Observer, Strategy, Command, Iterator |

---

## 7.3 Singleton Pattern

> **"একটা class এর শুধু একটাই instance তৈরি হবে — global access point থাকবে।"**

```python
# Thread-safe Singleton (Python):
import threading

class DatabaseConnection:
    _instance = None
    _lock = threading.Lock()

    def __new__(cls):
        if cls._instance is None:
            with cls._lock:  # Thread-safe!
                if cls._instance is None:  # Double-checked locking
                    cls._instance = super().__new__(cls)
                    cls._instance._connected = False
        return cls._instance

    def connect(self, host, port):
        if not self._connected:
            self._connection = create_connection(host, port)
            self._connected = True

    def execute(self, query):
        return self._connection.execute(query)

# Usage:
db1 = DatabaseConnection()
db2 = DatabaseConnection()
print(db1 is db2)  # True — same instance!
```

**কখন use করবো:** Database connection pool, Logger, Configuration manager, Cache manager।

**সতর্কতা:** Global state তৈরি করে — testing কঠিন হয়। Unit test এ mock করতে হয়।

---

## 7.4 Factory Pattern

> **"Object creation logic আলাদা করো — client কে concrete class জানতে হবে না।"**

```python
from abc import ABC, abstractmethod

# Product interface:
class Notification(ABC):
    @abstractmethod
    def send(self, message: str, recipient: str) -> bool: pass

# Concrete products:
class SMSNotification(Notification):
    def send(self, message, recipient):
        print(f"SMS to {recipient}: {message}")
        return sms_gateway.send(recipient, message)

class EmailNotification(Notification):
    def send(self, message, recipient):
        print(f"Email to {recipient}: {message}")
        return smtp.send(recipient, message)

class PushNotification(Notification):
    def send(self, message, recipient):
        print(f"Push to {recipient}: {message}")
        return fcm.send(recipient, message)

# Factory:
class NotificationFactory:
    _creators = {
        "sms": SMSNotification,
        "email": EmailNotification,
        "push": PushNotification,
    }

    @classmethod
    def create(cls, notification_type: str) -> Notification:
        creator = cls._creators.get(notification_type)
        if not creator:
            raise ValueError(f"Unknown notification type: {notification_type}")
        return creator()

    @classmethod
    def register(cls, type_name: str, creator):
        """নতুন notification type যোগ করা (OCP!)"""
        cls._creators[type_name] = creator

# Usage — client concrete class জানে না:
def notify_user(user, message, method="email"):
    notifier = NotificationFactory.create(method)
    notifier.send(message, user.contact)
```

---

## 7.5 Observer Pattern

> **"Subject (publisher) এর state change হলে সব Observer (subscriber) automatically notify হয়।"**

```python
from abc import ABC, abstractmethod
from typing import List

# Observer interface:
class EventObserver(ABC):
    @abstractmethod
    def update(self, event_type: str, data: dict) -> None: pass

# Subject (Observable):
class OrderEventPublisher:
    def __init__(self):
        self._observers: List[EventObserver] = []

    def subscribe(self, observer: EventObserver):
        self._observers.append(observer)

    def unsubscribe(self, observer: EventObserver):
        self._observers.remove(observer)

    def notify(self, event_type: str, data: dict):
        for observer in self._observers:
            observer.update(event_type, data)

    def place_order(self, order):
        # Business logic:
        saved_order = db.save(order)
        # Notify all observers:
        self.notify("order.placed", {
            "order_id": saved_order.id,
            "user_id": order.user_id,
            "total": float(order.total)
        })
        return saved_order

# Concrete observers:
class EmailObserver(EventObserver):
    def update(self, event_type, data):
        if event_type == "order.placed":
            email_service.send_confirmation(data["user_id"], data["order_id"])

class InventoryObserver(EventObserver):
    def update(self, event_type, data):
        if event_type == "order.placed":
            inventory.reserve(data["order_id"])

class AnalyticsObserver(EventObserver):
    def update(self, event_type, data):
        analytics.track(event_type, data)

# Wiring:
publisher = OrderEventPublisher()
publisher.subscribe(EmailObserver())
publisher.subscribe(InventoryObserver())
publisher.subscribe(AnalyticsObserver())

# নতুন observer যোগ করতে publisher change করতে হয় না! (OCP ✅)
```

---

## 7.6 Strategy Pattern

> **"Algorithm family define করো, encapsulate করো এবং interchange করো — runtime এ algorithm বদলানো যাবে।"**

```python
from abc import ABC, abstractmethod

# Strategy interface:
class SortStrategy(ABC):
    @abstractmethod
    def sort(self, data: list) -> list: pass

# Concrete strategies:
class QuickSortStrategy(SortStrategy):
    def sort(self, data): return quick_sort(data)

class MergeSortStrategy(SortStrategy):
    def sort(self, data): return merge_sort(data)

class BubbleSortStrategy(SortStrategy):
    def sort(self, data): return bubble_sort(data)

# Context:
class DataSorter:
    def __init__(self, strategy: SortStrategy = None):
        self._strategy = strategy or QuickSortStrategy()

    def set_strategy(self, strategy: SortStrategy):
        self._strategy = strategy  # Runtime এ switch!

    def sort(self, data: list) -> list:
        return self._strategy.sort(data)

# Usage:
sorter = DataSorter()
sorter.sort([3, 1, 4, 1, 5])       # QuickSort default

sorter.set_strategy(MergeSortStrategy())
sorter.sort([3, 1, 4, 1, 5])       # Now MergeSort!

# Real example — Discount strategy:
class DiscountStrategy(ABC):
    @abstractmethod
    def calculate(self, price: float) -> float: pass

class NoDiscount(DiscountStrategy):
    def calculate(self, price): return price

class PercentageDiscount(DiscountStrategy):
    def __init__(self, percent): self.percent = percent
    def calculate(self, price): return price * (1 - self.percent / 100)

class FlatDiscount(DiscountStrategy):
    def __init__(self, amount): self.amount = amount
    def calculate(self, price): return max(0, price - self.amount)

class EidSpecialDiscount(DiscountStrategy):
    def calculate(self, price):
        return price * 0.5 if price > 1000 else price * 0.8
```

---

## 7.7 Adapter Pattern

> **"Incompatible interfaces কে একসাথে কাজ করাও — existing code না বদলে।"**

```python
# Real scenario: পুরনো SMS service নতুন Notification interface এ wrap করো

# Existing (legacy) SMS service — interface আলাদা:
class LegacySMSService:
    def sendTextMessage(self, phoneNumber: str, textContent: str):
        print(f"Legacy SMS: {phoneNumber} → {textContent}")

# নতুন standard Notification interface:
class Notification(ABC):
    @abstractmethod
    def send(self, message: str, recipient: str) -> bool: pass

# Adapter — legacy service কে নতুন interface এ wrap করে:
class SMSAdapter(Notification):
    def __init__(self, legacy_sms: LegacySMSService):
        self._legacy = legacy_sms

    def send(self, message: str, recipient: str) -> bool:
        try:
            # Interface translate:
            self._legacy.sendTextMessage(recipient, message)
            return True
        except Exception:
            return False

# Usage — client নতুন interface use করে:
legacy = LegacySMSService()
adapter = SMSAdapter(legacy)

# এখন adapter দিয়ে যেকোনো Notification-compatible code এ use করা যাবে:
notify_user(adapter, "Your order is confirmed!", "+8801712345678")
```

---

## 7.8 Builder Pattern

> **"Complex object step-by-step তৈরি করো — same construction process different representations তৈরি করতে পারে।"**

```python
from dataclasses import dataclass, field
from typing import List, Optional

@dataclass
class QueryBuilder:
    """SQL Query Builder — method chaining with Builder pattern"""
    _table: str = ""
    _conditions: List[str] = field(default_factory=list)
    _columns: List[str] = field(default_factory=list)
    _limit: Optional[int] = None
    _offset: Optional[int] = None
    _order_by: Optional[str] = None

    def select(self, *columns) -> "QueryBuilder":
        self._columns = list(columns) if columns else ["*"]
        return self  # Method chaining!

    def from_table(self, table: str) -> "QueryBuilder":
        self._table = table
        return self

    def where(self, condition: str) -> "QueryBuilder":
        self._conditions.append(condition)
        return self

    def order_by(self, column: str, direction="ASC") -> "QueryBuilder":
        self._order_by = f"{column} {direction}"
        return self

    def limit(self, n: int) -> "QueryBuilder":
        self._limit = n
        return self

    def offset(self, n: int) -> "QueryBuilder":
        self._offset = n
        return self

    def build(self) -> str:
        cols = ", ".join(self._columns) if self._columns else "*"
        query = f"SELECT {cols} FROM {self._table}"
        if self._conditions:
            query += " WHERE " + " AND ".join(self._conditions)
        if self._order_by:
            query += f" ORDER BY {self._order_by}"
        if self._limit:
            query += f" LIMIT {self._limit}"
        if self._offset:
            query += f" OFFSET {self._offset}"
        return query

# Usage — fluent, readable:
query = (QueryBuilder()
    .select("id", "name", "email")
    .from_table("users")
    .where("status = 'active'")
    .where("age > 18")
    .order_by("created_at", "DESC")
    .limit(10)
    .offset(20)
    .build())

print(query)
# SELECT id, name, email FROM users WHERE status = 'active' AND age > 18
#   ORDER BY created_at DESC LIMIT 10 OFFSET 20
```

---

## 7.9 Decorator Pattern

> **"Object এর behavior dynamically add করো — subclassing ছাড়া।"**

```python
from abc import ABC, abstractmethod
import time
import functools

# Base interface:
class DataService(ABC):
    @abstractmethod
    def get_data(self, key: str) -> dict: pass

# Concrete component:
class DatabaseDataService(DataService):
    def get_data(self, key: str) -> dict:
        return db.query(f"SELECT * FROM data WHERE key='{key}'")

# Decorator base:
class DataServiceDecorator(DataService):
    def __init__(self, wrapped: DataService):
        self._wrapped = wrapped

    def get_data(self, key: str) -> dict:
        return self._wrapped.get_data(key)

# Cache decorator:
class CachingDecorator(DataServiceDecorator):
    def __init__(self, wrapped, cache, ttl=300):
        super().__init__(wrapped)
        self._cache = cache
        self._ttl = ttl

    def get_data(self, key: str) -> dict:
        cached = self._cache.get(key)
        if cached:
            return cached
        data = self._wrapped.get_data(key)
        self._cache.set(key, data, ex=self._ttl)
        return data

# Logging decorator:
class LoggingDecorator(DataServiceDecorator):
    def get_data(self, key: str) -> dict:
        start = time.time()
        result = self._wrapped.get_data(key)
        elapsed = (time.time() - start) * 1000
        print(f"get_data('{key}') took {elapsed:.2f}ms")
        return result

# Compose decorators:
service = DatabaseDataService()
service = CachingDecorator(service, redis_client, ttl=600)
service = LoggingDecorator(service)

# সব decorator এর behavior একসাথে:
data = service.get_data("user:123")
# Logging → Cache check → DB query (if cache miss)
```

---

## 7.10 LLD Case Study: Parking Lot System

### 📋 Requirements
- Multiple floors, multiple spots per floor
- Spot types: Compact, Large, Motorbike
- Vehicle types: Car, Truck, Motorbike
- Park/Unpark vehicle
- Calculate parking fee
- Check availability

### 🏗️ Class Design

```
Class Diagram:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[ParkingLot]
  - floors: List[ParkingFloor]
  + park(vehicle): Ticket
  + unpark(ticket): float (fee)
  + get_available_count(type): int

[ParkingFloor]
  - floor_no: int
  - spots: List[ParkingSpot]
  + get_available_spot(vehicle_type): ParkingSpot

[ParkingSpot]  ←abstract
  - spot_id: str
  - is_occupied: bool
  - vehicle: Optional[Vehicle]
  + can_fit(vehicle): bool
  + park(vehicle): void
  + unpark(): Vehicle

[CompactSpot(ParkingSpot)] — fits Car, Motorbike
[LargeSpot(ParkingSpot)]   — fits Car, Truck
[BikeSpot(ParkingSpot)]    — fits Motorbike only

[Vehicle]  ←abstract
  - license_plate: str
  - vehicle_type: VehicleType

[Car(Vehicle)]
[Truck(Vehicle)]
[Motorbike(Vehicle)]

[Ticket]
  - ticket_id: str
  - vehicle: Vehicle
  - spot: ParkingSpot
  - entry_time: datetime

[FeeCalculator]  ←Strategy pattern!
  + calculate(ticket): float

[HourlyFeeCalculator(FeeCalculator)]
[DailyFeeCalculator(FeeCalculator)]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 💻 Implementation

```python
from abc import ABC, abstractmethod
from datetime import datetime
from enum import Enum
from typing import Optional, List
import uuid

class VehicleType(Enum):
    CAR = "car"
    TRUCK = "truck"
    MOTORBIKE = "motorbike"

class SpotType(Enum):
    COMPACT = "compact"
    LARGE = "large"
    BIKE = "bike"

class Vehicle(ABC):
    def __init__(self, license_plate: str, vehicle_type: VehicleType):
        self.license_plate = license_plate
        self.vehicle_type = vehicle_type

class Car(Vehicle):
    def __init__(self, plate): super().__init__(plate, VehicleType.CAR)

class Truck(Vehicle):
    def __init__(self, plate): super().__init__(plate, VehicleType.TRUCK)

class Motorbike(Vehicle):
    def __init__(self, plate): super().__init__(plate, VehicleType.MOTORBIKE)


class ParkingSpot(ABC):
    def __init__(self, spot_id: str, spot_type: SpotType):
        self.spot_id = spot_id
        self.spot_type = spot_type
        self.is_occupied = False
        self.vehicle: Optional[Vehicle] = None

    @abstractmethod
    def can_fit(self, vehicle: Vehicle) -> bool: pass

    def park(self, vehicle: Vehicle):
        if self.is_occupied:
            raise ValueError(f"Spot {self.spot_id} is occupied!")
        if not self.can_fit(vehicle):
            raise ValueError(f"Vehicle type {vehicle.vehicle_type} doesn't fit!")
        self.vehicle = vehicle
        self.is_occupied = True

    def unpark(self) -> Vehicle:
        if not self.is_occupied:
            raise ValueError(f"Spot {self.spot_id} is empty!")
        vehicle = self.vehicle
        self.vehicle = None
        self.is_occupied = False
        return vehicle

class CompactSpot(ParkingSpot):
    def __init__(self, spot_id):
        super().__init__(spot_id, SpotType.COMPACT)

    def can_fit(self, vehicle: Vehicle) -> bool:
        return vehicle.vehicle_type in [VehicleType.CAR, VehicleType.MOTORBIKE]

class LargeSpot(ParkingSpot):
    def __init__(self, spot_id):
        super().__init__(spot_id, SpotType.LARGE)

    def can_fit(self, vehicle: Vehicle) -> bool:
        return True  # All vehicles fit

class BikeSpot(ParkingSpot):
    def __init__(self, spot_id):
        super().__init__(spot_id, SpotType.BIKE)

    def can_fit(self, vehicle: Vehicle) -> bool:
        return vehicle.vehicle_type == VehicleType.MOTORBIKE


class Ticket:
    def __init__(self, vehicle: Vehicle, spot: ParkingSpot):
        self.ticket_id = str(uuid.uuid4())[:8]
        self.vehicle = vehicle
        self.spot = spot
        self.entry_time = datetime.now()


class FeeCalculator(ABC):
    @abstractmethod
    def calculate(self, ticket: Ticket) -> float: pass

class HourlyFeeCalculator(FeeCalculator):
    RATES = {
        VehicleType.CAR: 30,       # 30 taka/hour
        VehicleType.TRUCK: 60,     # 60 taka/hour
        VehicleType.MOTORBIKE: 15  # 15 taka/hour
    }

    def calculate(self, ticket: Ticket) -> float:
        hours = (datetime.now() - ticket.entry_time).seconds / 3600
        hours = max(1, round(hours))  # Minimum 1 hour
        rate = self.RATES[ticket.vehicle.vehicle_type]
        return hours * rate


class ParkingFloor:
    def __init__(self, floor_no: int, spots: List[ParkingSpot]):
        self.floor_no = floor_no
        self.spots = spots

    def get_available_spot(self, vehicle: Vehicle) -> Optional[ParkingSpot]:
        for spot in self.spots:
            if not spot.is_occupied and spot.can_fit(vehicle):
                return spot
        return None


class ParkingLot:
    def __init__(self, floors: List[ParkingFloor],
                 fee_calculator: FeeCalculator = None):
        self.floors = floors
        self._fee_calculator = fee_calculator or HourlyFeeCalculator()
        self._active_tickets: dict = {}

    def park(self, vehicle: Vehicle) -> Ticket:
        for floor in self.floors:
            spot = floor.get_available_spot(vehicle)
            if spot:
                spot.park(vehicle)
                ticket = Ticket(vehicle, spot)
                self._active_tickets[ticket.ticket_id] = ticket
                print(f"Parked {vehicle.license_plate} at spot {spot.spot_id} — Ticket: {ticket.ticket_id}")
                return ticket
        raise Exception("No available spot for this vehicle type!")

    def unpark(self, ticket_id: str) -> float:
        ticket = self._active_tickets.pop(ticket_id, None)
        if not ticket:
            raise ValueError("Invalid ticket!")
        ticket.spot.unpark()
        fee = self._fee_calculator.calculate(ticket)
        print(f"Unparked {ticket.vehicle.license_plate} — Fee: {fee} taka")
        return fee

    def get_available_count(self) -> dict:
        counts = {"compact": 0, "large": 0, "bike": 0}
        for floor in self.floors:
            for spot in floor.spots:
                if not spot.is_occupied:
                    counts[spot.spot_type.value] += 1
        return counts


# Usage:
floor1 = ParkingFloor(1, [
    CompactSpot("F1-C1"), CompactSpot("F1-C2"),
    LargeSpot("F1-L1"),
    BikeSpot("F1-B1"), BikeSpot("F1-B2"),
])

lot = ParkingLot([floor1])

car = Car("DHA-GA-1234")
ticket = lot.park(car)
print(lot.get_available_count())

import time; time.sleep(1)  # Simulate time
fee = lot.unpark(ticket.ticket_id)
```

---

## 7.11 LLD Case Study: Library Management System

### 📋 Requirements
- Books, members management
- Book issue/return
- Fine calculation
- Book search

### 🏗️ Class Design

```python
from datetime import datetime, timedelta
from enum import Enum
from typing import Optional, List

class BookStatus(Enum):
    AVAILABLE = "available"
    ISSUED = "issued"
    RESERVED = "reserved"
    LOST = "lost"

class Book:
    def __init__(self, isbn, title, author, total_copies=1):
        self.isbn = isbn
        self.title = title
        self.author = author
        self.total_copies = total_copies
        self.available_copies = total_copies

    def is_available(self): return self.available_copies > 0

class Member:
    MAX_BOOKS = 3
    FINE_PER_DAY = 5  # 5 taka

    def __init__(self, member_id, name, email):
        self.member_id = member_id
        self.name = name
        self.email = email
        self.issued_books: List["BookLoan"] = []

    def can_borrow(self): return len(self.issued_books) < self.MAX_BOOKS

class BookLoan:
    LOAN_DAYS = 14

    def __init__(self, book: Book, member: Member):
        self.loan_id = str(uuid.uuid4())[:8]
        self.book = book
        self.member = member
        self.issue_date = datetime.now()
        self.due_date = self.issue_date + timedelta(days=self.LOAN_DAYS)
        self.return_date: Optional[datetime] = None

    def is_overdue(self): return datetime.now() > self.due_date

    def calculate_fine(self) -> float:
        if not self.is_overdue(): return 0
        end = self.return_date or datetime.now()
        overdue_days = (end - self.due_date).days
        return overdue_days * Member.FINE_PER_DAY

class Library:
    def __init__(self):
        self._books: dict = {}
        self._members: dict = {}
        self._loans: dict = {}

    def add_book(self, book: Book):
        self._books[book.isbn] = book

    def register_member(self, member: Member):
        self._members[member.member_id] = member

    def issue_book(self, member_id: str, isbn: str) -> BookLoan:
        member = self._members.get(member_id)
        book = self._books.get(isbn)

        if not member: raise ValueError("Member not found!")
        if not book: raise ValueError("Book not found!")
        if not member.can_borrow(): raise ValueError("Member has max books issued!")
        if not book.is_available(): raise ValueError("Book not available!")

        book.available_copies -= 1
        loan = BookLoan(book, member)
        member.issued_books.append(loan)
        self._loans[loan.loan_id] = loan
        return loan

    def return_book(self, loan_id: str) -> float:
        loan = self._loans.get(loan_id)
        if not loan: raise ValueError("Invalid loan ID!")

        loan.return_date = datetime.now()
        loan.book.available_copies += 1
        loan.member.issued_books.remove(loan)
        fine = loan.calculate_fine()
        return fine

    def search(self, query: str) -> List[Book]:
        q = query.lower()
        return [
            b for b in self._books.values()
            if q in b.title.lower() or q in b.author.lower() or q in b.isbn
        ]
```

---

## 📋 PART 7: Quick Revision Table

| Pattern | Category | মূল ধারণা | Use Case |
|---------|----------|-----------|---------|
| Singleton | Creational | একটাই instance | DB connection, Logger |
| Factory | Creational | Object creation encapsulate | Notification, Payment |
| Builder | Creational | Step-by-step object build | SQL Query, HTTP Request |
| Adapter | Structural | Incompatible interface wrap | Legacy system integration |
| Decorator | Structural | Behavior dynamically add | Cache, Logging, Auth |
| Observer | Behavioral | Event broadcast | Order events, UI updates |
| Strategy | Behavioral | Algorithm swap করো | Sorting, Discount, Payment |

| SOLID | মনে রাখো |
|-------|---------|
| SRP | একটা class, একটা কারণ |
| OCP | Open extend, Closed modify |
| LSP | Subclass = Parent replacement |
| ISP | Small interfaces |
| DIP | Interface এর উপর depend |

---

## 🎯 PART 7: Top 10 Interview Questions

<details>
<summary><strong>Q1: SOLID principles বাংলায় explain করো — real example দিয়ে</strong></summary>

**উত্তর:**

**S — Single Responsibility:** OrderService শুধু order logic করবে। Email পাঠানো EmailService এর কাজ। এতে class ছোট থাকে, test করা সহজ।

**O — Open/Closed:** নতুন payment method যোগ করতে PaymentProcessor class বদলাবো না। নতুন class লিখবো। Existing code untouched → existing tests break হবে না।

**L — Liskov Substitution:** Square is-a Shape হতে পারে, কিন্তু Rectangle এর subclass হলে area calculation ভুল হয়। Subclass কে parent এর জায়গায় রাখলে behavior same থাকতে হবে।

**I — Interface Segregation:** IWorker এ work(), eat(), sleep() একসাথে রাখলে Robot কে eat() implement করতে বাধ্য হবে। আলাদা রাখো।

**D — Dependency Inversion:** OrderService কে MySQLRepository এর উপর depend না করে IOrderRepository (interface) এর উপর depend করাও। Test এ MockRepository inject করা যাবে।

</details>

<details>
<summary><strong>Q2: Singleton pattern কীভাবে implement করবে? Thread-safe করবে কীভাবে?</strong></summary>

**উত্তর:**
```python
import threading

class Singleton:
    _instance = None
    _lock = threading.Lock()

    def __new__(cls):
        if cls._instance is None:
            with cls._lock:
                if cls._instance is None:  # Double-checked locking
                    cls._instance = super().__new__(cls)
        return cls._instance
```

Double-checked locking কেন: প্রথম `if` লক ছাড়া check করে performance এর জন্য। লকের ভেতরে দ্বিতীয়বার check করে কারণ দুটো thread একই সময়ে প্রথম check pass করতে পারে।

</details>

<details>
<summary><strong>Q3: Observer আর Pub/Sub এর পার্থক্য কী?</strong></summary>

**উত্তর:**

| বিষয় | Observer | Pub/Sub |
|------|---------|---------|
| Coupling | Subject Observer কে directly জানে | Publisher subscriber কে জানে না |
| Communication | Same process/thread | Asynchronous (message broker) |
| Scope | Single application | Distributed systems |
| Implementation | In-memory callbacks | Kafka, RabbitMQ, Redis |
| Use case | UI events, order events (same service) | Microservices communication |

Observer: OrderService directly EmailObserver.update() call করে।
Pub/Sub: Kafka topic এ publish করে, subscriber আলাদা machine এ।

</details>

<details>
<summary><strong>Q4: Strategy আর Factory pattern এর পার্থক্য কী?</strong></summary>

**উত্তর:**

**Factory:** Object কীভাবে create করবো — creation এর সমস্যা solve করে।
```python
payment = PaymentFactory.create("bkash")
```

**Strategy:** Object কীভাবে behave করবে — behavior এর সমস্যা solve করে।
```python
processor = PaymentProcessor(BkashStrategy())
processor.pay(1000)
processor.set_strategy(NagadStrategy())  # Runtime change!
processor.pay(500)
```

Factory: "কোন class instantiate করবো?"
Strategy: "কোন algorithm use করবো?"

</details>

<details>
<summary><strong>Q5: Dependency Injection (DI) কী এবং SOLID এর সাথে connection কী?</strong></summary>

**উত্তর:**
Dependency Injection মানে class নিজে dependency তৈরি না করে বাইরে থেকে receive করে।

```python
# Without DI (bad):
class OrderService:
    def __init__(self):
        self.repo = MySQLOrderRepository()  # Hardcoded!

# With DI (good):
class OrderService:
    def __init__(self, repo: OrderRepository):  # Injected!
        self.repo = repo

# Wiring (composition root):
repo = MySQLOrderRepository()
service = OrderService(repo)

# Test এ:
mock_repo = MockOrderRepository()
service = OrderService(mock_repo)  # Easy to test!
```

DI + SOLID connection:
- **D** (Dependency Inversion): Interface inject করো
- **S** (SRP): Wiring এর দায়িত্ব আলাদা (composition root)
- **O** (OCP): Different implementation inject করে behavior change

</details>

<details>
<summary><strong>Q6: Design করো — Coffee machine (Builder pattern)</strong></summary>

**উত্তর:**
```python
class Coffee:
    def __init__(self):
        self.size = None
        self.shots = 1
        self.milk = False
        self.sugar = 0
        self.flavor = None

class CoffeeBuilder:
    def __init__(self): self._coffee = Coffee()

    def size(self, size: str) -> "CoffeeBuilder":
        self._coffee.size = size; return self

    def shots(self, n: int) -> "CoffeeBuilder":
        self._coffee.shots = n; return self

    def with_milk(self) -> "CoffeeBuilder":
        self._coffee.milk = True; return self

    def sugar(self, teaspoons: int) -> "CoffeeBuilder":
        self._coffee.sugar = teaspoons; return self

    def flavor(self, flavor: str) -> "CoffeeBuilder":
        self._coffee.flavor = flavor; return self

    def build(self) -> Coffee:
        if not self._coffee.size:
            raise ValueError("Size is required!")
        return self._coffee

# Usage:
latte = (CoffeeBuilder()
    .size("large")
    .shots(2)
    .with_milk()
    .sugar(1)
    .flavor("vanilla")
    .build())
```

</details>

<details>
<summary><strong>Q7: Parking lot system design করো (LLD)</strong></summary>

**উত্তর (Framework):**

**Classes identify করো:**
- `ParkingLot` — top-level coordinator
- `ParkingFloor` — floor management
- `ParkingSpot` (abstract) + `CompactSpot`, `LargeSpot`, `BikeSpot`
- `Vehicle` (abstract) + `Car`, `Truck`, `Motorbike`
- `Ticket` — issue করলে ticket দেয়
- `FeeCalculator` (Strategy) — fee calculate

**Key Design Decisions:**
1. `ParkingSpot.can_fit(vehicle)` — polymorphism
2. `FeeCalculator` Strategy pattern — easily swap hourly/daily/monthly
3. `ParkingLot` manages `active_tickets` map — O(1) lookup

**Patterns used:** Strategy (fee), Factory (spot type), Template Method (parking spot hierarchy)

</details>

<details>
<summary><strong>Q8: Decorator pattern কী? Python decorator এর সাথে কী সম্পর্ক?</strong></summary>

**উত্তর:**
Decorator Design Pattern এবং Python `@decorator` syntax আলাদা — কিন্তু same concept।

**Design Pattern:** Object wrap করে behavior add করো।
```python
service = LoggingDecorator(CachingDecorator(DatabaseService()))
```

**Python syntax:** Function wrap করে behavior add করো।
```python
def cache(func):
    cached = {}
    def wrapper(*args):
        if args not in cached:
            cached[args] = func(*args)
        return cached[args]
    return wrapper

@cache  # Equivalent to: get_user = cache(get_user)
def get_user(user_id):
    return db.query(user_id)
```

উভয়েই: existing code না বদলে behavior add করা। Decorator pattern এ class level, Python এ function level।

</details>

<details>
<summary><strong>Q9: Composition over Inheritance — কেন?</strong></summary>

**উত্তর:**
Inheritance সমস্যা:
- Tight coupling — parent change হলে সব child ভাঙে
- Fragile base class problem
- Multiple inheritance — diamond problem
- "is-a" relationship নিশ্চিত করতে হয়

Composition সুবিধা:
```python
# ❌ Inheritance:
class LoggingOrderService(OrderService):
    def create_order(self, items):
        logger.log("Creating order")
        return super().create_order(items)

# ✅ Composition:
class OrderService:
    def __init__(self, repo, logger):  # Composed!
        self.repo = repo
        self.logger = logger

    def create_order(self, items):
        self.logger.log("Creating order")
        return self.repo.save(Order(items))
```

Rule: "Favor composition over inheritance" — GoF Design Patterns।
Use inheritance only for true "is-a" relationships।

</details>

<details>
<summary><strong>Q10: Design করো — Notification System (multiple channels)</strong></summary>

**উত্তর:**
```python
# Factory + Observer + Strategy combined:

class NotificationChannel(ABC):
    @abstractmethod
    def send(self, user_id: int, message: str) -> bool: pass

class EmailChannel(NotificationChannel):
    def send(self, user_id, message):
        email = get_user_email(user_id)
        return smtp.send(email, message)

class SMSChannel(NotificationChannel):
    def send(self, user_id, message):
        phone = get_user_phone(user_id)
        return sms_api.send(phone, message)

class PushChannel(NotificationChannel):
    def send(self, user_id, message):
        token = get_device_token(user_id)
        return fcm.send(token, message)

class NotificationService:
    def __init__(self):
        self._channels: List[NotificationChannel] = []

    def add_channel(self, channel: NotificationChannel):
        self._channels.append(channel)

    def notify(self, user_id: int, message: str):
        results = []
        for channel in self._channels:
            try:
                results.append(channel.send(user_id, message))
            except Exception as e:
                logger.error(f"Channel {channel} failed: {e}")
        return any(results)  # At least one succeeded

# Usage:
notifier = NotificationService()
notifier.add_channel(EmailChannel())
notifier.add_channel(SMSChannel())
notifier.add_channel(PushChannel())

notifier.notify(user_id=123, message="Your order is confirmed!")
```

</details>

<div align="right">

[⬆ উপরে যাও](#) | [📚 সূচিপত্র](#) | [PART 8 →](#part8)

</div>

<a id="part8"></a>

---

# PART 8: Cloud & DevOps Basics
### ☁️ AWS, Docker, Kubernetes, CI/CD

> **Interview টিপস:** Junior engineer হিসেবে Cloud/DevOps এর basics জানা এখন mandatory। "তোমার project টা কীভাবে deploy করলে?" বা "Docker কী?" — এই প্রশ্নগুলো এখন common। এই PART এ practical knowledge focus করা হয়েছে।

---

## 8.1 Cloud Computing Basics

### 📖 সংজ্ঞা
Cloud Computing মানে **internet এর মাধ্যমে computing resources (server, storage, database, networking) on-demand ব্যবহার করা** — নিজে hardware কিনতে হয় না।

### 📊 Cloud Service Models

```
Cloud Service Models:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

IaaS (Infrastructure as a Service):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
তুমি পাও: Virtual machines, storage, networking
তুমি manage করো: OS, Runtime, App, Data
Provider manage করে: Physical hardware, datacenter

Example: AWS EC2, Google Compute Engine, Azure VMs
Use: Custom server setup, full control দরকার হলে

PaaS (Platform as a Service):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
তুমি পাও: Runtime environment (OS + runtime pre-configured)
তুমি manage করো: App, Data
Provider manage করে: Hardware, OS, Runtime, Middleware

Example: Heroku, AWS Elastic Beanstalk, Google App Engine
Use: Developer শুধু code deploy করতে চায়, infra চিন্তা না করে

SaaS (Software as a Service):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
তুমি পাও: Ready-to-use software
তুমি manage করো: শুধু data/config
Provider manage করে: Everything

Example: Gmail, Slack, Zoom, Salesforce
Use: End users
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 Cloud Deployment Models

| Model | মানে | Example |
|-------|------|---------|
| Public Cloud | বড় provider এর shared infrastructure | AWS, GCP, Azure |
| Private Cloud | নিজস্ব datacenter এ cloud | On-premise OpenStack |
| Hybrid Cloud | Public + Private mix | Critical data private, rest public |
| Multi-Cloud | Multiple providers use করো | AWS + GCP একসাথে |

### 📊 Cloud এর সুবিধা

| Traditional (On-Premise) | Cloud |
|--------------------------|-------|
| Capital expense (CAPEX) | Operational expense (OPEX) |
| Hardware কিনতে হয় | Pay-as-you-go |
| Capacity fixed | Elastic (scale up/down) |
| Slow provisioning (weeks) | Fast provisioning (minutes) |
| Global reach কঠিন | Global regions instantly |

---

## 8.2 AWS Core Services

### 🖥️ Compute

```
AWS EC2 (Elastic Compute Cloud):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Virtual server — Linux/Windows install করে নিজের app চালাও
Instance types:
  t3.micro   → 1 vCPU, 1GB RAM (Free tier, development)
  t3.medium  → 2 vCPU, 4GB RAM (Small production)
  m5.large   → 2 vCPU, 8GB RAM (General purpose)
  c5.large   → 2 vCPU, 4GB RAM (Compute optimized)
  r5.large   → 2 vCPU, 16GB RAM (Memory optimized)

Pricing:
  On-Demand: Per hour pay, no commitment (most expensive)
  Reserved: 1-3 year commit → 60-70% cheaper
  Spot: Unused capacity → 90% cheaper (can be interrupted!)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

AWS Lambda (Serverless):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Code upload করো, AWS run করবে — server manage করতে হয় না
Event-driven: HTTP request, S3 upload, Cron, SQS message
Pricing: Per invocation (first 1M free/month!)
Timeout: Max 15 minutes
Cold start: First invocation slow (~100ms to 1s)
Use case: API endpoints, image resize, scheduled tasks
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🗄️ Storage

```
AWS S3 (Simple Storage Service):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Object storage — files, images, videos, backups
Unlimited storage, 99.999999999% (11 nines) durability
Bucket: Container (like a folder)
Object: File + metadata
Key: Object এর unique identifier (path)

CLI commands:
aws s3 mb s3://my-bucket                          # Bucket create
aws s3 cp file.txt s3://my-bucket/               # Upload
aws s3 sync ./local-folder s3://my-bucket/       # Sync folder
aws s3 ls s3://my-bucket/                        # List objects
aws s3 rm s3://my-bucket/file.txt                # Delete

Storage classes:
  Standard: Frequently accessed (most expensive)
  IA (Infrequent Access): Less frequent, cheaper
  Glacier: Archive, retrieve takes hours (cheapest)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🗃️ Database Services

```
AWS RDS (Relational Database Service):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Managed SQL database: PostgreSQL, MySQL, MariaDB, Oracle, SQL Server
AWS handles: Backups, patches, failover, monitoring
Multi-AZ: Standby replica in another availability zone → High availability
Read Replicas: Read load distribute করো

AWS DynamoDB:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Managed NoSQL (key-value + document)
Serverless, automatically scales
Single-digit millisecond latency
Use: Session store, gaming leaderboard, shopping cart

AWS ElastiCache:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Managed Redis or Memcached
In-memory cache layer
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 🌐 Networking

```
AWS VPC (Virtual Private Cloud):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
নিজের isolated network define করো
Public Subnet: Internet access আছে (web server)
Private Subnet: Internet access নেই (database)
Security Group: Virtual firewall (port/IP rules)
NAT Gateway: Private subnet থেকে internet access

VPC Architecture:
[Internet] ──▶ [Internet Gateway] ──▶ [Public Subnet: Load Balancer, Web]
                                       [Private Subnet: App Server, DB]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

AWS CloudFront (CDN):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Global CDN — 450+ edge locations
Static assets (S3), API responses cache করে
DDoS protection (AWS Shield)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📊 AWS Services Quick Map

| Need | Service |
|------|---------|
| Virtual server | EC2 |
| Serverless function | Lambda |
| File/object storage | S3 |
| SQL database | RDS |
| NoSQL database | DynamoDB |
| Cache | ElastiCache |
| Message queue | SQS, SNS |
| Container orchestration | ECS, EKS |
| DNS | Route 53 |
| CDN | CloudFront |
| Load balancer | ALB/NLB |
| Monitoring | CloudWatch |
| Secret management | Secrets Manager |

---

## 8.3 Docker

### 📖 সংজ্ঞা
Docker হলো **container platform** — application ও তার dependencies একসাথে package করে portable container বানানো যায়। "My machine এ কাজ করে" সমস্যার solution।

### 🔄 Virtual Machine vs Container

```
Virtual Machine:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[App A] [App B] [App C]
[ OS  ] [ OS  ] [ OS  ]   ← প্রতিটার নিজস্ব OS (GBs!)
[  Hypervisor (VMware)  ]
[    Physical Hardware   ]
Heavy: GBs, slow to start (minutes)

Container:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[App A] [App B] [App C]
[ Lib] [ Lib] [ Lib ]     ← শুধু libraries (MBs!)
[     Docker Engine      ]  ← Shared OS kernel
[    Physical Hardware   ]
Lightweight: MBs, fast start (seconds)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📦 Dockerfile

```dockerfile
# Python FastAPI App:
FROM python:3.11-slim

WORKDIR /app

# Dependencies আগে copy করো (layer cache optimize)
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Application code copy
COPY . .

# Non-root user (security best practice)
RUN adduser --disabled-password appuser
USER appuser

EXPOSE 8000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
```

```dockerfile
# Node.js App:
FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
RUN npm ci --only=production

COPY . .

RUN addgroup -S appgroup && adduser -S appuser -G appgroup
USER appuser

EXPOSE 3000
CMD ["node", "server.js"]
```

### 🔧 Docker Commands

```bash
# Image build:
docker build -t myapp:1.0 .
docker build -t myapp:latest -f Dockerfile.prod .

# Run container:
docker run -d -p 8000:8000 --name myapp myapp:1.0
docker run -d -p 5432:5432 -e POSTGRES_PASSWORD=secret postgres:15
docker run -it ubuntu bash   # Interactive terminal

# Container management:
docker ps                    # Running containers
docker ps -a                 # All containers
docker stop myapp            # Stop
docker start myapp           # Start
docker restart myapp         # Restart
docker rm myapp              # Delete
docker logs myapp            # View logs
docker logs -f myapp         # Follow logs (like tail -f)
docker exec -it myapp bash   # Enter running container

# Image management:
docker images                # List images
docker rmi myapp:1.0         # Delete image
docker pull nginx:latest     # Pull from registry
docker push myrepo/myapp:1.0 # Push to registry

# Registry:
docker tag myapp:1.0 myrepo/myapp:1.0
docker login
docker push myrepo/myapp:1.0
```

### 🐙 Docker Compose

```yaml
# docker-compose.yml — Multi-service app:
version: '3.9'

services:
  web:
    build: .
    ports:
      - "8000:8000"
    environment:
      DATABASE_URL: postgresql://postgres:secret@db:5432/mydb
      REDIS_URL: redis://redis:6379
    depends_on:
      - db
      - redis
    volumes:
      - ./logs:/app/logs
    restart: unless-stopped

  db:
    image: postgres:15
    environment:
      POSTGRES_DB: mydb
      POSTGRES_PASSWORD: secret
    volumes:
      - postgres_data:/var/lib/postgresql/data
    restart: unless-stopped

  redis:
    image: redis:7-alpine
    restart: unless-stopped

  nginx:
    image: nginx:alpine
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - ./nginx.conf:/etc/nginx/nginx.conf
      - ./ssl:/etc/nginx/ssl
    depends_on:
      - web

volumes:
  postgres_data:
```

```bash
# Docker Compose commands:
docker compose up -d          # Start all services (detached)
docker compose down           # Stop and remove containers
docker compose down -v        # Also remove volumes!
docker compose logs web       # Service logs
docker compose ps             # Service status
docker compose exec web bash  # Enter service container
docker compose build          # Rebuild images
docker compose pull           # Pull latest images
```

---

## 8.4 Kubernetes (K8s)

### 📖 সংজ্ঞা
Kubernetes হলো **container orchestration platform** — containers কে automatically deploy, scale, manage করে। Docker Compose production এ যথেষ্ট না — Kubernetes বড় scale এ দরকার।

### 🏗️ Kubernetes Architecture

```
Kubernetes Cluster:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Control Plane (Master Node)]
  ├── API Server: সব communication এর gateway
  ├── etcd: Cluster state store (key-value)
  ├── Scheduler: Pod কোন node এ যাবে decide করে
  └── Controller Manager: Desired state maintain করে

[Worker Nodes]
  ├── Node 1: [Pod A] [Pod B] ← kubelet, kube-proxy
  ├── Node 2: [Pod C] [Pod D]
  └── Node 3: [Pod E] [Pod F]

Pod: Kubernetes এর smallest deployable unit (1+ containers)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📄 Kubernetes YAML Files

```yaml
# Deployment — App replicas manage করে:
apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp
  labels:
    app: myapp
spec:
  replicas: 3                  # 3 copies চালাও
  selector:
    matchLabels:
      app: myapp
  template:
    metadata:
      labels:
        app: myapp
    spec:
      containers:
      - name: myapp
        image: myrepo/myapp:1.0
        ports:
        - containerPort: 8000
        resources:
          requests:
            memory: "128Mi"
            cpu: "100m"
          limits:
            memory: "256Mi"
            cpu: "500m"
        env:
        - name: DATABASE_URL
          valueFrom:
            secretKeyRef:
              name: myapp-secrets
              key: database-url
        livenessProbe:
          httpGet:
            path: /health
            port: 8000
          initialDelaySeconds: 30
          periodSeconds: 10
        readinessProbe:
          httpGet:
            path: /ready
            port: 8000
          initialDelaySeconds: 5
          periodSeconds: 5
```

```yaml
# Service — Network access দেয়:
apiVersion: v1
kind: Service
metadata:
  name: myapp-service
spec:
  selector:
    app: myapp
  ports:
  - port: 80
    targetPort: 8000
  type: ClusterIP     # Internal only
  # type: LoadBalancer  # External (creates AWS ELB)
  # type: NodePort      # Expose on node port
```

```yaml
# HorizontalPodAutoscaler — Auto scaling:
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: myapp-hpa
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: myapp
  minReplicas: 2
  maxReplicas: 20
  metrics:
  - type: Resource
    resource:
      name: cpu
      target:
        type: Utilization
        averageUtilization: 70    # CPU 70% → scale up
```

### 🔧 kubectl Commands

```bash
# Apply/delete resources:
kubectl apply -f deployment.yaml
kubectl delete -f deployment.yaml

# Pod management:
kubectl get pods                          # List pods
kubectl get pods -w                       # Watch (live)
kubectl describe pod myapp-xyz-abc        # Pod details
kubectl logs myapp-xyz-abc                # Pod logs
kubectl logs -f myapp-xyz-abc             # Follow logs
kubectl exec -it myapp-xyz-abc -- bash    # Enter pod

# Deployment management:
kubectl get deployments
kubectl rollout status deployment/myapp
kubectl rollout history deployment/myapp
kubectl rollout undo deployment/myapp     # Rollback!
kubectl scale deployment myapp --replicas=5

# Service/Ingress:
kubectl get services
kubectl get ingress

# ConfigMap & Secrets:
kubectl create secret generic myapp-secrets   --from-literal=database-url="postgresql://..."
kubectl get secrets
kubectl describe secret myapp-secrets
```

### 🔑 Key K8s Concepts

```
ConfigMap: Non-sensitive config (env vars, config files)
Secret: Sensitive data (passwords, API keys) — base64 encoded
PersistentVolume (PV): Storage provisioning
PersistentVolumeClaim (PVC): Pod storage request করে
Ingress: HTTP routing rules (path-based, host-based)
Namespace: Cluster এর logical partition (dev/staging/prod)
```

---

## 8.5 CI/CD Pipeline

### 📖 সংজ্ঞা
- **CI (Continuous Integration):** Code push করলে automatically build + test চলে
- **CD (Continuous Delivery):** Staging এ automatically deploy হয়
- **CD (Continuous Deployment):** Production এ automatically deploy হয়

### 🔄 CI/CD Flow

```
Developer Workflow:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
git push ──▶ GitHub/GitLab
                  │
                  ▼
          [CI Pipeline Triggered]
                  │
         ┌────────┴────────┐
         ▼                 ▼
    [Unit Tests]    [Lint/Format Check]
         │                 │
         └────────┬────────┘
                  ▼
         [Build Docker Image]
                  │
                  ▼
         [Integration Tests]
                  │
                  ▼
         [Push to Registry]
                  │
                  ▼
         [Deploy to Staging]
                  │
                  ▼
         [E2E Tests on Staging]
                  │
                  ▼
         [Manual Approval] ← Production এর আগে
                  │
                  ▼
         [Deploy to Production]
                  │
                  ▼
         [Health Check / Smoke Test]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📄 GitHub Actions Example

```yaml
# .github/workflows/ci-cd.yml
name: CI/CD Pipeline

on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

env:
  REGISTRY: ghcr.io
  IMAGE_NAME: ${{ github.repository }}

jobs:
  test:
    runs-on: ubuntu-latest
    services:
      postgres:
        image: postgres:15
        env:
          POSTGRES_PASSWORD: testpass
          POSTGRES_DB: testdb
        ports:
          - 5432:5432
        options: >-
          --health-cmd pg_isready
          --health-interval 10s
          --health-timeout 5s
          --health-retries 5

    steps:
    - uses: actions/checkout@v4

    - name: Set up Python
      uses: actions/setup-python@v5
      with:
        python-version: '3.11'

    - name: Cache dependencies
      uses: actions/cache@v4
      with:
        path: ~/.cache/pip
        key: ${{ runner.os }}-pip-${{ hashFiles('requirements.txt') }}

    - name: Install dependencies
      run: pip install -r requirements.txt

    - name: Run linting
      run: |
        ruff check .
        black --check .

    - name: Run tests
      env:
        DATABASE_URL: postgresql://postgres:testpass@localhost:5432/testdb
      run: pytest --cov=app --cov-report=xml

    - name: Upload coverage
      uses: codecov/codecov-action@v4

  build-and-push:
    needs: test
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'

    steps:
    - uses: actions/checkout@v4

    - name: Log in to registry
      uses: docker/login-action@v3
      with:
        registry: ${{ env.REGISTRY }}
        username: ${{ github.actor }}
        password: ${{ secrets.GITHUB_TOKEN }}

    - name: Build and push Docker image
      uses: docker/build-push-action@v5
      with:
        context: .
        push: true
        tags: ${{ env.REGISTRY }}/${{ env.IMAGE_NAME }}:${{ github.sha }}

  deploy-staging:
    needs: build-and-push
    runs-on: ubuntu-latest
    environment: staging

    steps:
    - name: Deploy to staging
      run: |
        kubectl set image deployment/myapp           myapp=${{ env.REGISTRY }}/${{ env.IMAGE_NAME }}:${{ github.sha }}           --namespace=staging
        kubectl rollout status deployment/myapp --namespace=staging

  deploy-production:
    needs: deploy-staging
    runs-on: ubuntu-latest
    environment: production    # Manual approval required

    steps:
    - name: Deploy to production
      run: |
        kubectl set image deployment/myapp           myapp=${{ env.REGISTRY }}/${{ env.IMAGE_NAME }}:${{ github.sha }}           --namespace=production
        kubectl rollout status deployment/myapp --namespace=production
```

### 📊 CI/CD Tools

| Tool | Type | Use Case |
|------|------|---------|
| GitHub Actions | CI/CD | GitHub repos এ integrated |
| GitLab CI/CD | CI/CD | GitLab repos এ integrated |
| Jenkins | CI/CD | Self-hosted, highly customizable |
| ArgoCD | GitOps CD | Kubernetes deployment |
| CircleCI | CI/CD | Fast, SaaS |

---

## 8.6 Nginx

### 📖 সংজ্ঞা
Nginx হলো **high-performance web server + reverse proxy** — static files serve করে, requests forward করে, load balance করে, SSL terminate করে।

### 📄 Nginx Configuration

```nginx
# /etc/nginx/nginx.conf

# HTTP → HTTPS redirect:
server {
    listen 80;
    server_name example.com www.example.com;
    return 301 https://$server_name$request_uri;
}

# Main HTTPS server:
server {
    listen 443 ssl http2;
    server_name example.com www.example.com;

    # SSL/TLS:
    ssl_certificate     /etc/nginx/ssl/cert.pem;
    ssl_certificate_key /etc/nginx/ssl/key.pem;
    ssl_protocols TLSv1.2 TLSv1.3;
    ssl_ciphers HIGH:!aNULL:!MD5;

    # Security headers:
    add_header X-Frame-Options "SAMEORIGIN";
    add_header X-Content-Type-Options "nosniff";
    add_header X-XSS-Protection "1; mode=block";

    # Static files (served directly by Nginx — fast!):
    location /static/ {
        alias /app/staticfiles/;
        expires 1y;
        add_header Cache-Control "public, immutable";
    }

    location /media/ {
        alias /app/media/;
        expires 30d;
    }

    # API → FastAPI backend:
    location /api/ {
        proxy_pass http://app:8000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_read_timeout 90s;
    }

    # Load balancing (multiple app servers):
    upstream app_servers {
        least_conn;                        # Least connections algorithm
        server app1:8000 weight=3;
        server app2:8000 weight=2;
        server app3:8000 weight=1;
    }

    location / {
        proxy_pass http://app_servers;
    }

    # Rate limiting:
    limit_req_zone $binary_remote_addr zone=api:10m rate=10r/s;
    location /api/auth/ {
        limit_req zone=api burst=5 nodelay;
        proxy_pass http://app:8000;
    }

    # Gzip compression:
    gzip on;
    gzip_types text/plain text/css application/json application/javascript;
    gzip_min_length 1000;
}
```

---

## 8.7 Monitoring & Logging

### 📊 Monitoring Stack

```
Prometheus + Grafana (Most common stack):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Your App] ─/metrics endpoint─▶ [Prometheus] ─query─▶ [Grafana]
                                 (scrapes every 15s)    (dashboards)
                                      │
                                 [AlertManager]
                                 (Slack/Email alert when threshold crossed)

App তে metrics expose করো (Python):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
from prometheus_client import Counter, Histogram, Gauge, start_http_server

REQUEST_COUNT = Counter('http_requests_total', 'Total HTTP requests',
                        ['method', 'endpoint', 'status'])
REQUEST_LATENCY = Histogram('http_request_duration_seconds',
                            'HTTP request latency', ['endpoint'])
ACTIVE_USERS = Gauge('active_users', 'Currently active users')

@app.middleware("http")
async def metrics_middleware(request, call_next):
    start = time.time()
    response = await call_next(request)
    duration = time.time() - start
    REQUEST_COUNT.labels(
        method=request.method,
        endpoint=request.url.path,
        status=response.status_code
    ).inc()
    REQUEST_LATENCY.labels(endpoint=request.url.path).observe(duration)
    return response

# GET /metrics → Prometheus scrapes this
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📋 Key Metrics to Monitor

```
Golden Signals (Google SRE):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. Latency:    Request কত দ্রুত serve হচ্ছে (p50, p95, p99)
2. Traffic:    Requests per second (RPS)
3. Errors:     Error rate (4xx, 5xx percentage)
4. Saturation: Resource utilization (CPU, Memory, Disk)

Alert rules (example):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
- Error rate > 1% → Alert
- p99 latency > 1s → Alert
- CPU > 80% for 5 minutes → Alert
- Disk usage > 85% → Alert
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### 📝 Structured Logging

```python
import logging
import json
from datetime import datetime

class JSONFormatter(logging.Formatter):
    def format(self, record):
        log_data = {
            "timestamp": datetime.utcnow().isoformat(),
            "level": record.levelname,
            "message": record.getMessage(),
            "logger": record.name,
            "module": record.module,
        }
        if hasattr(record, 'request_id'):
            log_data['request_id'] = record.request_id
        if record.exc_info:
            log_data['exception'] = self.formatException(record.exc_info)
        return json.dumps(log_data)

logger = logging.getLogger(__name__)
handler = logging.StreamHandler()
handler.setFormatter(JSONFormatter())
logger.addHandler(handler)

# Usage:
logger.info("Order created", extra={"request_id": "req-123", "order_id": 456})
# Output: {"timestamp": "2026-05-11T...", "level": "INFO",
#          "message": "Order created", "request_id": "req-123", "order_id": 456}
```

### 📊 Logging Stack (ELK)

```
ELK Stack:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[App] ──JSON logs──▶ [Filebeat/Fluentd] ──▶ [Logstash] ──▶ [Elasticsearch]
                     (log shipper)         (parse/transform)  (index, store)
                                                                    │
                                                              [Kibana]
                                                           (search, dashboard)

Cloud alternatives:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
AWS: CloudWatch Logs
GCP: Cloud Logging
Self-hosted: Grafana Loki (lightweight, recommended)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 8.8 Deployment Strategies

```
1. Rolling Deployment (Default K8s):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Old version থেকে gradually নতুন version এ replace করো
v1 v1 v1 v1 → v2 v1 v1 v1 → v2 v2 v1 v1 → v2 v2 v2 v2
Zero downtime, কিন্তু briefly দুই version চলে

2. Blue-Green Deployment:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Blue: Current production (v1)
Green: New version (v2) — deploy করো, test করো
Traffic switch: Load balancer → Blue থেকে Green এ
Rollback: Instant! শুধু LB switch back করো

3. Canary Deployment:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
ছোট % traffic নতুন version এ → monitor করো → problem নেই → gradually বাড়াও
5% → 10% → 25% → 50% → 100%
Risk কম, real user data দিয়ে test

4. Feature Flags:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Code deploy করো, feature বন্ধ রাখো
Config দিয়ে specific users/regions এ enable করো
Problem হলে: Config update → feature off (no deployment!)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 📋 PART 8: Quick Revision Table

| Topic | Key Points |
|-------|-----------|
| IaaS/PaaS/SaaS | EC2/Beanstalk/Gmail — control vs convenience trade-off |
| EC2 | Virtual server, instance types, pricing models |
| S3 | Object storage, 11 nines durability, storage classes |
| RDS | Managed SQL, Multi-AZ, Read Replicas |
| Lambda | Serverless, event-driven, pay per invocation |
| VPC | Private network, public/private subnet, security group |
| Docker | Container, Dockerfile, image vs container |
| Docker Compose | Multi-service local development |
| Kubernetes | Container orchestration, Deployment, Service, HPA |
| CI/CD | Build → Test → Deploy pipeline |
| Nginx | Reverse proxy, load balance, SSL, rate limit |
| Prometheus/Grafana | Metrics scraping + visualization |
| ELK/Loki | Log aggregation + search |
| Rolling Deploy | Gradual replace, zero downtime |
| Blue-Green | Two environments, instant rollback |
| Canary | Gradual traffic shift, risk reduction |

---

## 🎯 PART 8: Top 10 Interview Questions

<details>
<summary><strong>Q1: Docker কী? VM এর চেয়ে কীভাবে আলাদা?</strong></summary>

**উত্তর:**
Docker হলো container platform। Application + dependencies একসাথে package করে — যেকোনো machine এ একই ভাবে run করে।

**VM vs Container:**
- VM: নিজস্ব OS kernel — GBs storage, minutes startup
- Container: Host OS kernel share করে — MBs storage, seconds startup

**Real benefit:**
```
Dev machine তে: Python 3.9, Ubuntu
Production: Python 3.11, CentOS
→ "Works on my machine" problem!

Docker: Same image সব জায়গায় → consistent environment
```

</details>

<details>
<summary><strong>Q2: Docker image আর container এর পার্থক্য কী?</strong></summary>

**উত্তর:**
- **Image:** Read-only template (blueprint) — `Dockerfile` থেকে build হয়
- **Container:** Image এর running instance

```
Analogy:
Image = Class definition
Container = Object (instance of class)

একটা Image থেকে multiple containers চালানো যায়:
docker run myapp  → Container 1
docker run myapp  → Container 2
docker run myapp  → Container 3
```

Image layers: Dockerfile এর প্রতিটা instruction একটা layer। Cache করে — rebuild fast।

</details>

<details>
<summary><strong>Q3: Kubernetes কেন দরকার? Docker Compose দিয়ে হয় না?</strong></summary>

**উত্তর:**
Docker Compose: Single machine, development/small scale।
Kubernetes: Multiple machines, production grade।

**K8s এর extra benefits:**
1. **Auto-healing:** Pod crash হলে automatically restart
2. **Auto-scaling:** CPU বাড়লে pods বাড়াও (HPA)
3. **Rolling update:** Zero downtime deployment
4. **Service discovery:** Pods নিজেরা খুঁজে পায়
5. **Load balancing:** Built-in
6. **Secret management:** Secure config injection
7. **Multi-node:** Hundreds of machines manage

```
Production scenario:
3:00 AM — App এ sudden 10x traffic spike
Docker Compose: Manual scale করতে হবে (তুমি ঘুমাও!)
Kubernetes HPA: CPU 70% দেখলে → auto 5 → 20 pods → traffic handle
```

</details>

<details>
<summary><strong>Q4: CI/CD pipeline কী এবং কেন দরকার?</strong></summary>

**উত্তর:**
CI (Continuous Integration): Code push হলে auto build + test।
CD (Continuous Delivery/Deployment): Auto staging/production deploy।

**কেন দরকার:**
- Manual deploy: Error prone, time consuming
- "Works on my machine": Environment differences
- Late integration: বড় merge conflict
- Slow feedback: Bug production এ গেলে দেরিতে জানা যায়

**Benefits:**
✅ Fast feedback (push করেই জানো test pass হলো কিনা)
✅ Consistent deploy process
✅ Rollback সহজ (git tag → deploy)
✅ Team parallel কাজ করতে পারে

**BD company তে:** GitHub Actions (free), GitLab CI (self-host) সবচেয়ে common।

</details>

<details>
<summary><strong>Q5: Blue-Green deployment কীভাবে কাজ করে?</strong></summary>

**উত্তর:**
```
Initial state:
Blue (v1) — Production (100% traffic)
Green — Empty

Deploy v2:
Blue (v1) — Production (100% traffic)
Green (v2) — Deploy করো, test করো (staging)

Switch:
Load Balancer: Blue → Green
Green (v2) — Production (100% traffic) ✅
Blue (v1) — Standby (rollback এর জন্য রাখো)

Problem হলে:
Load Balancer: Green → Blue (30 seconds rollback!)
```

**সুবিধা:** Zero downtime, instant rollback।
**সমস্যা:** Double infrastructure cost (two identical environments)।

</details>

<details>
<summary><strong>Q6: Nginx কীভাবে reverse proxy হিসেবে কাজ করে?</strong></summary>

**উত্তর:**
```
Client → Nginx (Port 80/443) → Backend App (Port 8000)

Nginx যা করে:
1. SSL termination: HTTPS decrypt করে, HTTP forward করে
2. Static files: /static/ direct serve (fast!)
3. Load balance: Multiple backend servers এ distribute
4. Rate limiting: DDoS/brute-force protect
5. Caching: Response cache করে
6. Compression: gzip করে response ছোট করে
7. Header modification: Real IP forward করে

Backend app এর সুবিধা:
- SSL জানে না, HTTP only
- Rate limiting জানে না, Nginx করে
- Static files serve করে না, Nginx করে
→ App শুধু business logic!
```

</details>

<details>
<summary><strong>Q7: Kubernetes এ Pod fail হলে কী হয়?</strong></summary>

**উত্তর:**
Kubernetes এর Controller Manager desired state maintain করে।

```
Desired state: replicas: 3
Current state: Pod crash → 2 running

Controller Manager detects: 2 ≠ 3
Action: নতুন Pod schedule করো!
Result: 3 running (auto-healed!)

যদি Node fail করে:
Scheduler: Pods অন্য healthy node এ reschedule করে

লিভ প্রোব (livenessProbe):
/health endpoint check করে
Fail করলে → Container restart করো (stuck process fix)

রেডিনেস প্রোব (readinessProbe):
App ready হলেই traffic পাঠাও
Starting up → traffic নেই → Ready → traffic starts
```

</details>

<details>
<summary><strong>Q8: Environment variables আর secrets কীভাবে manage করবে?</strong></summary>

**উত্তর:**
```
❌ Never do:
# Hardcode secrets in code:
DATABASE_URL = "postgresql://admin:password123@prod-db:5432/mydb"
# Git এ push করলে publicly accessible!

✅ Local development:
.env file (gitignore এ রাখো!)
DATABASE_URL=postgresql://localhost:5432/mydb

python-dotenv:
from dotenv import load_dotenv
load_dotenv()
db_url = os.environ["DATABASE_URL"]

✅ Docker:
docker run -e DATABASE_URL="..." myapp
# Or: --env-file .env

✅ Production (Kubernetes):
kubectl create secret generic myapp-secrets   --from-literal=db-url="postgresql://prod-db/myapp"

Deployment এ reference করো (না, hardcode না):
env:
- name: DATABASE_URL
  valueFrom:
    secretKeyRef:
      name: myapp-secrets
      key: db-url

✅ AWS:
AWS Secrets Manager — rotate secrets, audit log
```

</details>

<details>
<summary><strong>Q9: Monitoring এ কোন metrics সবার আগে দেখবে?</strong></summary>

**উত্তর:**
Google SRE এর Golden Signals:

1. **Latency (p95, p99):** 95th/99th percentile response time।
   Alert: p99 > 1 second
   "Average" misleading — 100 users, 1 user 10s → average okay, user experience bad

2. **Error Rate:** 5xx errors / total requests × 100%।
   Alert: > 0.1% for 2 minutes
   
3. **Traffic (RPS):** Requests per second।
   Sudden spike → scale up দরকার
   Sudden drop → app down হতে পারে!
   
4. **Saturation:** CPU, Memory, Disk I/O।
   CPU > 80% sustained → scale out
   Memory leak → memory বাড়তে থাকে

Dashboard order:
Error rate → Latency → Traffic → Saturation

</details>

<details>
<summary><strong>Q10: তোমার Django/FastAPI project কীভাবে production এ deploy করবে?</strong></summary>

**উত্তর (Step by Step):**

```
1. Dockerfile লেখো:
   FROM python:3.11-slim
   COPY requirements.txt .
   RUN pip install -r requirements.txt
   COPY . .
   CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]

2. GitHub Actions CI/CD setup:
   push → test → build image → push to registry

3. AWS EC2 তে:
   - EC2 instance launch (t3.small)
   - Security Group: 80, 443, 22 open
   - Docker install
   - docker pull + docker run
   - Nginx install + configure
   - SSL: Let's Encrypt (certbot)

4. Scale করলে:
   - EC2 Auto Scaling Group
   - Application Load Balancer
   - RDS for database (না docker)
   - ElastiCache for Redis

5. Alternatively (easier):
   - AWS Elastic Beanstalk (PaaS)
   - Heroku (most simple)
   - Railway.app (simple + free tier)
```

</details>

<div align="right">

[⬆ উপরে যাও](#) | [📚 সূচিপত্র](#) | [PART 9 →](#part9)

</div>

---

*হ্যান্ডবুক তৈরিতে: Senior Software Architect, Backend Engineer & System Design Interviewer*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 10 | সম্পন্ন: PART 1-8 ✅ | বাকি: PART 9-10 🔜*
