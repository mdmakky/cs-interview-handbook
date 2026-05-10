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
| [PART 5](#part5) | Message Queues & Distributed Systems | Kafka, RabbitMQ, Pub/Sub | 🔜 |
| [PART 6](#part6) | System Design Case Studies | URL Shortener, Chat App, E-commerce | 🔜 |
| [PART 7](#part7) | Low-Level Design (LLD) | SOLID, Design Patterns, UML | 🔜 |
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

*হ্যান্ডবুক তৈরিতে: Senior Software Architect, Backend Engineer & System Design Interviewer*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 10 | সম্পন্ন: PART 1-4 ✅ | বাকি: PART 5-10 🔜*
