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
| [PART 3](#part3) | Database Design | SQL vs NoSQL, Sharding, Replication | 🔜 |
| [PART 4](#part4) | Caching & Performance | Redis, Rate Limiting, CDN | 🔜 |
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

*হ্যান্ডবুক তৈরিতে: Senior Software Architect, Backend Engineer & System Design Interviewer*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 10 | সম্পন্ন: PART 1-2 ✅ | বাকি: PART 3-10 🔜*
