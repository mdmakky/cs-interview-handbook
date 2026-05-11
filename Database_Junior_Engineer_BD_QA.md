<a id="top"></a>

# 🗄️ Database Interview Preparation Handbook
## বাংলাদেশের Junior Software Engineer ইন্টারভিউয়ের জন্য সম্পূর্ণ Database গাইড

**লেখক:** Senior Database Engineer & Backend Architect  
**লক্ষ্য:** বাংলাদেশের শীর্ষ সফটওয়্যার কোম্পানিতে Junior SWE / Backend Developer পদে চাকরি পাওয়া  
**ভাষা:** বাংলা (Technical terms ইংরেজিতে)

---

> **💡 হ্যান্ডবুক ব্যবহারের নিয়ম:**  
> প্রতিটি টপিক মনোযোগ দিয়ে পড়ুন। SQL examples নিজে run করুন। Interview questions নিজে উত্তর দেওয়ার চেষ্টা করুন তারপর model answer দেখুন।

---

<a id="toc"></a>

## 📋 সূচিপত্র — Table of Contents

> **💡 নিচের যেকোনো PART এ সরাসরি ক্লিক করুন। প্রতিটি PART এর শেষে [⬆ শীর্ষে ফিরুন](#top) বাটন আছে।**

| | PART | বিষয়বস্তু |
|:-:|------|------------|
| 📘 | [**PART 1** — Database Fundamentals](#part1) | Database, DBMS vs RDBMS, Keys, Constraints, Relationships, ER Diagram, Normalization |
| 📗 | [**PART 2** — SQL Fundamentals](#part2) | SELECT, WHERE, JOINs, GROUP BY, Subquery, DML Commands |
| 📙 | [**PART 3** — Advanced SQL & Database Concepts](#part3) | Indexing, Transactions, ACID, Isolation, Views, Stored Procedures, Triggers, Sharding |
| 📕 | [**PART 4** — Normalization & Database Design](#part4) | Normalization (1NF–BCNF), Denormalization, Schema Design, Data Types, Constraints |
| 📓 | [**PART 5** — Backend & Real Project Database Design](#part5) | ORM, Connection Pooling, Migration, Caching, Performance Tuning, Real Project Patterns |
| 📔 | [**PART 6** — Database Interview Questions](#part6) | Top 50 Interview Q&A, Scenario-based Questions, BD Company-specific, Cheat Sheet |
| 📒 | [**PART 7** — Language & Framework Database Integration](#part7) | PHP/Laravel, Python/Django, Node.js, Raw Query vs ORM, Environment Config, Best Practices |
| 📃 | [**PART 8** — NoSQL & Modern Databases](#part8) | NoSQL কী, MongoDB, Redis, Elasticsearch, SQL vs NoSQL, CAP Theorem, When to Use |
| 📄 | [**PART 9** — Bangladeshi Interview Preparation](#part9) | BD Job Interview Prep, Common Mistakes, CV Tips, Mock Interviews, Final Revision |

<details>
<summary><strong>📄 PART 9 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৯.১ বাংলাদেশের IT Job Market](#৯১-বাংলাদেশের-it-job-market)
- [৯.২ Interview Process — BD Companies](#৯২-interview-process--bd-companies)
- [৯.৩ সবচেয়ে Common Interview Questions](#৯৩-সবচেয়ে-common-interview-questions)
- [৯.৪ সাধারণ ভুল ও কীভাবে এড়াবেন](#৯৪-সাধারণ-ভুল-ও-কীভাবে-এড়াবেন)
- [৯.৫ CV ও Portfolio Tips](#৯৫-cv-ও-portfolio-tips)
- [৯.৬ SQL Cheat Sheet — Quick Revision](#৯৬-sql-cheat-sheet--quick-revision)
- [৯.৭ Mock Interview — Full Session](#৯৭-mock-interview--full-session)
- [৯.৮ Interview Day Checklist](#৯৮-interview-day-checklist)
- [৯.৯ Final Study Plan](#৯৯-final-study-plan)

</details>

<details>
<summary><strong>📃 PART 8 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৮.১ NoSQL কী?](#৮১-nosql-কী)
- [৮.২ SQL vs NoSQL](#৮২-sql-vs-nosql)
- [৮.৩ CAP Theorem](#৮৩-cap-theorem)
- [৮.৪ MongoDB — Document Database](#৮৪-mongodb--document-database)
- [৮.৫ Redis — Key-Value Store](#৮৫-redis--key-value-store)
- [৮.৬ Elasticsearch — Search Engine](#৮৬-elasticsearch--search-engine)
- [৮.৭ Cassandra — Wide-Column Store](#৮৭-cassandra--wide-column-store)
- [৮.৮ কোন Database কখন?](#৮৮-কোন-database-কখন)
- [৮.৯ PART 8 — Interview Q&A](#৮৯-part-8--interview-questions--answers)

</details>

<details>
<summary><strong>📒 PART 7 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৭.১ PHP ও MySQL](#৭১-php-ও-mysql)
- [৭.২ Laravel Database (Eloquent & Query Builder)](#৭২-laravel-database-eloquent--query-builder)
- [৭.৩ Python ও MySQL](#৭৩-python-ও-mysql)
- [৭.৪ Django ORM — বিস্তারিত](#৭৪-django-orm--বিস্তারিত)
- [৭.৫ Node.js ও MySQL](#৭৫-nodejs-ও-mysql)
- [৭.৬ Environment Configuration & Security](#৭৬-environment-configuration--security)
- [৭.৭ Database Testing](#৭৭-database-testing)
- [৭.৮ PART 7 — Interview Q&A](#৭৮-part-7--interview-questions--answers)

</details>

<details>
<summary><strong>📔 PART 6 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৬.১ Database Fundamentals Q&A](#৬১-database-fundamentals-qa)
- [৬.২ SQL Q&A](#৬২-sql-qa)
- [৬.৩ Advanced Concepts Q&A](#৬৩-advanced-concepts-qa)
- [৬.৪ Design & Normalization Q&A](#৬৪-design--normalization-qa)
- [৬.৫ Performance & Optimization Q&A](#৬৫-performance--optimization-qa)
- [৬.৬ Scenario-based Questions](#৬৬-scenario-based-questions)
- [৬.৭ বাংলাদেশি কোম্পানির বাস্তব প্রশ্ন](#৬৭-বাংলাদেশি-কোম্পানির-বাস্তব-প্রশ্ন)
- [৬.৮ Database Cheat Sheet](#৬৮-database-cheat-sheet)

</details>

<details>
<summary><strong>📓 PART 5 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৫.১ ORM কী?](#৫১-orm-কী)
- [৫.২ ORM vs Raw SQL](#৫২-orm-vs-raw-sql)
- [৫.৩ Database Migration](#৫৩-database-migration)
- [৫.৪ Connection Pooling](#৫৪-connection-pooling)
- [৫.৫ N+1 Query Problem](#৫৫-n1-query-problem)
- [৫.৬ Database Caching](#৫৬-database-caching)
- [৫.৭ Pagination — Best Practices](#৫৭-pagination--best-practices)
- [৫.৮ Soft Delete Pattern](#৫৮-soft-delete-pattern)
- [৫.৯ Audit Trail Pattern](#৫৯-audit-trail-pattern)
- [৫.১০ Multi-tenancy Design](#৫১০-multi-tenancy-design)
- [৫.১১ Database Security](#৫১১-database-security)
- [৫.১২ Backup & Recovery](#৫১২-backup--recovery)
- [৫.১৩ Real Project — Job Portal Schema](#৫১৩-real-project--job-portal-schema)
- [৫.১৪ PART 5 — Interview Q&A](#৫১৪-part-5--interview-questions--answers)

</details>

<details>
<summary><strong>📕 PART 4 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৪.১ Normalization কী?](#৪১-normalization-কী)
- [৪.২ 1NF — First Normal Form](#৪২-1nf--first-normal-form)
- [৪.৩ 2NF — Second Normal Form](#৪৩-2nf--second-normal-form)
- [৪.৪ 3NF — Third Normal Form](#৪৪-3nf--third-normal-form)
- [৪.৫ BCNF — Boyce-Codd Normal Form](#৪৫-bcnf--boyce-codd-normal-form)
- [৪.৬ 4NF ও 5NF](#৪৬-4nf-ও-5nf)
- [৪.৭ Denormalization](#৪৭-denormalization)
- [৪.৮ ER Diagram থেকে Schema](#৪৮-er-diagram-থেকে-schema)
- [৪.৯ Data Types নির্বাচন](#৪৯-data-types-নির্বাচন)
- [৪.১০ Constraints — বিস্তারিত](#৪১০-constraints--বিস্তারিত)
- [৪.১১ Relationships Implementation](#৪১১-relationships-implementation)
- [৪.১২ Schema Design Best Practices](#৪১২-schema-design-best-practices)
- [৪.১৩ Real Project Schema Design](#৪১৩-real-project-schema-design)
- [৪.১৪ PART 4 — Interview Q&A](#৪১৪-part-4--interview-questions--answers)

</details>

<details>
<summary><strong>📙 PART 3 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৩.১ Indexing](#৩১-indexing)
- [৩.২ Clustered vs Non-clustered Index](#৩২-clustered-vs-non-clustered-index)
- [৩.৩ Transactions](#৩৩-transactions)
- [৩.৪ ACID Properties](#৩৪-acid-properties)
- [৩.৫ Isolation Levels](#৩৫-isolation-levels)
- [৩.৬ Deadlock](#৩৬-deadlock)
- [৩.৭ Views](#৩৭-views)
- [৩.৮ Stored Procedure](#৩৮-stored-procedure)
- [৩.৯ Trigger](#৩৯-trigger)
- [৩.১০ Cursor](#৩১০-cursor)
- [৩.১১ Functions (User-Defined)](#৩১১-functions-user-defined)
- [৩.১২ Query Optimization](#৩১২-query-optimization)
- [৩.১৩ Query Execution Plan](#৩১৩-query-execution-plan)
- [৩.১৪ Partitioning](#৩১৪-partitioning)
- [৩.১৫ Sharding](#৩১৫-sharding)
- [৩.১৬ Replication](#৩১৬-replication)
- [৩.১৭ PART 3 — Interview Q&A](#৩১৭-part-3--interview-questions--answers)

</details>

<details>
<summary><strong>📗 PART 2 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [২.১ SELECT](#২১-select)
- [২.২ WHERE](#২২-where)
- [২.৩ ORDER BY](#২৩-order-by)
- [২.৪ GROUP BY](#২৪-group-by)
- [২.৫ HAVING](#২৫-having)
- [২.৬ DISTINCT](#২৬-distinct)
- [২.৭ LIMIT](#২৭-limit)
- [২.৮ INSERT](#২৮-insert)
- [২.৯ UPDATE](#২৯-update)
- [২.১০ DELETE](#২১০-delete)
- [২.১১ LIKE](#২১১-like)
- [২.১২ IN](#২১২-in)
- [২.১৩ BETWEEN](#২১৩-between)
- [২.১৪ INNER JOIN](#২১৪-inner-join)
- [২.১৫ LEFT JOIN](#২১৫-left-join)
- [২.১৬ RIGHT JOIN](#২১৬-right-join)
- [২.১৭ FULL JOIN](#২১৭-full-join)
- [২.১৮ SELF JOIN](#২১৮-self-join)
- [২.১৯ UNION vs UNION ALL](#২১৯-union-vs-union-all)
- [২.২০ Subquery ও Nested Query](#২২০-subquery-ও-nested-query)
- [২.২১ PART 2 — Interview Q&A](#২২১-part-2--interview-questions--answers)

</details>

<details>
<summary><strong>📘 PART 1 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [১.১ Database কী?](#১১-database-কী)
- [১.২ DBMS vs RDBMS](#১২-dbms-vs-rdbms)
- [১.৩ Database এর সুবিধা](#১৩-database-এর-সুবিধা)
- [১.৪ Database এর প্রকারভেদ](#১৪-database-এর-প্রকারভেদ)
- [১.৫ Relational Database](#১৫-relational-database)
- [১.৬ Table, Row, Column](#১৬-table-row-column)
- [১.৭ Primary Key](#১৭-primary-key)
- [১.৮ Foreign Key](#১৮-foreign-key)
- [১.৯ Candidate Key](#১৯-candidate-key)
- [১.১০ Super Key](#১১০-super-key)
- [১.১১ Composite Key](#১১১-composite-key)
- [১.১২ Unique Key](#১১২-unique-key)
- [১.১৩ NULL](#১১৩-null)
- [১.১৪ Constraints](#১১৪-constraints)
- [১.১৫ Relationships](#১১৫-relationships)
- [১.১৬ ER Diagram](#১১৬-er-diagram)
- [১.১৭ Schema vs Instance](#১১৭-schema-vs-instance)
- [১.১৮ Data Integrity](#১১৮-data-integrity)
- [১.১৯ Normalization Overview](#১১৯-normalization-overview)
- [১.২০ PART 1 — Interview Q&A](#১২০-part-1--interview-questions--answers)

</details>

---

<a id="part1"></a>

# PART 1: Database Fundamentals (মূল ধারণাসমূহ)

> **📍 এই PART এর Sections:** [১.১ Database কী?](#১১-database-কী) · [১.২ DBMS vs RDBMS](#১২-dbms-vs-rdbms) · [১.৩ সুবিধা](#১৩-database-এর-সুবিধা) · [১.৪ প্রকারভেদ](#১৪-database-এর-প্রকারভেদ)

---

## ১.১ Database কী?

### সংজ্ঞা (Definition)

**Database** হলো একটি **সংগঠিত তথ্যভান্ডার (organized collection of data)** যেখানে structured আকারে data সংরক্ষণ করা হয় এবং সহজে access, manage ও update করা যায়।

সহজ ভাষায়: Database হলো একটি **ডিজিটাল ফাইল ক্যাবিনেট** যেখানে সব তথ্য সুশৃঙ্খলভাবে সাজানো থাকে।

### Real-Life Analogy

একটি **স্কুলের অফিসের ফাইল ক্যাবিনেট** চিন্তা করুন:

| বাস্তব জগৎ | Database |
|-----------|----------|
| ফাইল ক্যাবিনেট | Database |
| প্রতিটি ড্রয়ার | Table |
| প্রতিটি ফাইল/পৃষ্ঠা | Row (Record) |
| ফাইলের প্রতিটি তথ্য (নাম, রোল) | Column (Field) |
| ক্যাবিনেটের নিয়মকানুন | Schema |

### Practical Use Case

- **E-commerce:** পণ্যের তথ্য, অর্ডার, customer details সংরক্ষণ
- **Banking:** Account balance, transaction history
- **Hospital:** Patient records, prescription, appointment
- **Social Media:** User profiles, posts, comments, likes

### Interview-Style Explanation

**প্রশ্ন:** "Database কী? কেন আমরা Database ব্যবহার করি?"

**আদর্শ উত্তর:**
> "Database হলো একটি organized data collection যেখানে structured আকারে data store করা হয়। আমরা Database ব্যবহার করি কারণ flat file-এ data রাখলে duplicate হয়, search করা কঠিন হয়, এবং multiple user একসাথে access করতে পারে না। Database এই সমস্যাগুলো সমাধান করে — data redundancy কমায়, fast querying enable করে, এবং data security নিশ্চিত করে।"

### Common Mistakes

- ❌ Database মানেই শুধু MySQL — Oracle, PostgreSQL, MongoDB সবই database
- ❌ Excel spreadsheet = Database — Excel structured কিন্তু proper DBMS নয়
- ✅ Database হলো data এর organized digital repository

### Follow-up Interview Questions

1. Database ছাড়া কি application বানানো সম্ভব?
2. File system এবং Database এর মধ্যে পার্থক্য কী?
3. In-memory database কী?

---

## ১.২ DBMS vs RDBMS

### সংজ্ঞা

**DBMS (Database Management System)** হলো একটি **software system** যা database তৈরি, manage, এবং control করে।

**RDBMS (Relational Database Management System)** হলো DBMS এর একটি বিশেষ ধরন যেখানে data **tables (relations)** আকারে সংরক্ষিত হয় এবং tables এর মধ্যে **relationships** থাকে।

### তুলনা টেবিল

| বিষয় | DBMS | RDBMS |
|------|------|-------|
| Data structure | যেকোনো format (hierarchical, network, object) | শুধু Tables (rows & columns) |
| Relationship | Tables এর মধ্যে সম্পর্ক নেই | Foreign key দিয়ে tables যুক্ত |
| Normalization | সাধারণত নেই | আছে |
| ACID properties | সব সময় নয় | সম্পূর্ণভাবে support করে |
| SQL support | সীমিত বা নেই | সম্পূর্ণভাবে SQL support |
| উদাহরণ | XML DB, IMS (IBM) | MySQL, PostgreSQL, Oracle, SQL Server |
| Security | কম | বেশি (role-based access) |

### Real-Life Analogy

- **DBMS** = যেকোনো ধরনের গুদামঘর যেখানে জিনিস রাখা যায়
- **RDBMS** = সুশৃঙ্খল গুদামঘর যেখানে প্রতিটি জিনিস নির্দিষ্ট র‍্যাকে সাজানো এবং সব র‍্যাক একে অপরের সাথে সম্পর্কিত

### Practical Use Case

বাংলাদেশের companies তে সবচেয়ে বেশি ব্যবহৃত RDBMS:

```
MySQL      → Web applications, startups (Chaldal, Pathao)
PostgreSQL → Enterprise, complex queries (Brain Station 23)
Oracle     → Banking, telecom (Grameenphone, bKash)
SQL Server → Microsoft stack companies
```

### Interview-Style Explanation

**প্রশ্ন:** "DBMS এবং RDBMS এর মধ্যে পার্থক্য কী?"

**আদর্শ উত্তর:**
> "DBMS হলো যেকোনো software যা data manage করে। RDBMS হলো DBMS এর একটি specific type যেখানে data tables এ stored থাকে এবং tables গুলো relationships দিয়ে connected। RDBMS এর মূল বৈশিষ্ট্য হলো — SQL support, ACID compliance, এবং referential integrity। MySQL, PostgreSQL হলো RDBMS এর উদাহরণ।"

### Common Mistakes

- ❌ "DBMS মানে শুধু MySQL" — MySQL হলো RDBMS, DBMS এর একটি type
- ❌ সব database ACID compliant — NoSQL database সাধারণত fully ACID নয়
- ✅ RDBMS সবসময় DBMS, কিন্তু সব DBMS RDBMS নয়

---

## ১.৩ Database এর সুবিধা

### মূল সুবিধাসমূহ

```
┌────────────────────────────────────────────────┐
│           Database এর ৮টি মূল সুবিধা           │
├────────────────────────────────────────────────┤
│ 1. Data Redundancy হ্রাস (No duplicate data)    │
│ 2. Data Consistency (সব জায়গায় একই data)       │
│ 3. Data Sharing (Multiple user একসাথে)          │
│ 4. Data Security (User-based access control)   │
│ 5. Data Integrity (নির্ভরযোগ্য তথ্য)            │
│ 6. Backup & Recovery (Data নষ্ট হলে ফিরে পাওয়া) │
│ 7. Fast Data Access (Indexing দিয়ে দ্রুত খোঁজা) │
│ 8. Concurrent Access (একসাথে অনেকে ব্যবহার)    │
└────────────────────────────────────────────────┘
```

### File System vs Database — বিস্তারিত তুলনা

| সমস্যা (File System) | সমাধান (Database) |
|---------------------|------------------|
| একই student এর নাম দুই ফাইলে → Duplicate | Normalization এ একটি table এ রাখো |
| একটি ফাইল corrupt হলে data loss | Backup & Recovery mechanism |
| দুইজন একসাথে edit করলে conflict | Transaction & Locking mechanism |
| নির্দিষ্ট record খুঁজতে পুরো ফাইল scan | Index দিয়ে O(log n) তে খোঁজা |
| কে access করতে পারবে নিয়ন্ত্রণ নেই | Role-based Access Control (RBAC) |

### Interview-Style Explanation

**প্রশ্ন:** "কেন আমরা simple file এর বদলে Database ব্যবহার করি?"

**আদর্শ উত্তর:**
> "File system এ data রাখলে redundancy, inconsistency, এবং concurrent access এর সমস্যা হয়। Database এই সমস্যাগুলো সমাধান করে। বিশেষ করে — data একবার লিখলেই যথেষ্ট (no redundancy), transaction দিয়ে consistency নিশ্চিত হয়, এবং DBMS নিজেই concurrent users manage করে। এছাড়া SQL দিয়ে complex query করা যায় যা file এ সম্ভব নয়।"

---

## ১.৪ Database এর প্রকারভেদ

### ধরনসমূহ

```
Database এর প্রকারভেদ
│
├── Relational Database (SQL)
│   ├── MySQL
│   ├── PostgreSQL
│   ├── Oracle
│   └── SQL Server
│
├── NoSQL Database
│   ├── Document → MongoDB
│   ├── Key-Value → Redis
│   ├── Column-family → Cassandra
│   └── Graph → Neo4j
│
├── NewSQL Database
│   ├── CockroachDB
│   └── Google Spanner
│
├── In-Memory Database
│   ├── Redis
│   └── Memcached
│
└── Cloud Database
    ├── AWS RDS
    ├── Google Firebase
    └── Azure SQL
```

### তুলনা টেবিল

| ধরন | কখন ব্যবহার | উদাহরণ |
|-----|------------|--------|
| Relational | Structured data, complex queries, financial systems | MySQL, PostgreSQL |
| Document | Flexible schema, JSON data, content management | MongoDB |
| Key-Value | Caching, session management, real-time data | Redis |
| Column-family | Big data, analytics, time-series | Cassandra |
| Graph | Social networks, recommendation engines | Neo4j |

### Interview Tip

> বাংলাদেশের Junior level interview এ মূলত **MySQL** এবং **PostgreSQL** সম্পর্কে জিজ্ঞেস করা হয়। MongoDB সম্পর্কে basic ধারণা থাকলেই যথেষ্ট। Senior level এ Redis, Cassandra আসে।

---

## ১.৫ Relational Database

### সংজ্ঞা

**Relational Database** হলো একটি database যেখানে data **tables (relations)** আকারে সংরক্ষিত হয় এবং tables গুলো **keys** এর মাধ্যমে একে অপরের সাথে **সম্পর্কিত (related)**।

এটি **E.F. Codd** ১৯৭০ সালে **Relational Model** হিসেবে প্রবর্তন করেন।

### মূল বৈশিষ্ট্য

- **Table (Relation):** Data rows ও columns এ organized
- **Row (Tuple):** একটি নির্দিষ্ট record
- **Column (Attribute):** Data এর একটি নির্দিষ্ট property
- **Primary Key:** প্রতিটি row কে uniquely identify করে
- **Foreign Key:** Tables এর মধ্যে সম্পর্ক তৈরি করে
- **SQL:** Data query ও manipulate করার ভাষা

### Real-Life Analogy

একটি **University Database** চিন্তা করুন:

```
Students Table              Courses Table
┌────┬────────┬─────┐      ┌────┬──────────────┐
│ ID │ Name   │ Dept│      │ ID │ Course Name  │
├────┼────────┼─────┤      ├────┼──────────────┤
│ 1  │ Rafi   │ CSE │      │ 1  │ OOP          │
│ 2  │ Sumi   │ EEE │      │ 2  │ Database     │
└────┴────────┴─────┘      └────┴──────────────┘

Enrollment Table (সম্পর্ক)
┌────────────┬───────────┐
│ Student_ID │ Course_ID │
├────────────┼───────────┤
│     1      │     1     │
│     1      │     2     │
│     2      │     2     │
└────────────┴───────────┘
```

---

## ১.৬ Table, Row, Column

### সংজ্ঞা

| Term | সংজ্ঞা | উদাহরণ |
|------|--------|--------|
| **Table (Relation)** | একটি নির্দিষ্ট entity এর data এর সংগ্রহ | `students`, `orders`, `products` |
| **Row (Record/Tuple)** | Table এর একটি নির্দিষ্ট entry | একজন student এর সব তথ্য |
| **Column (Field/Attribute)** | Data এর একটি নির্দিষ্ট property | `name`, `age`, `email` |
| **Cell** | একটি নির্দিষ্ট row এবং column এর intersection | `"Rafi Ahmed"` |
| **Degree** | Table এর column সংখ্যা | 5 columns = degree 5 |
| **Cardinality** | Table এর row সংখ্যা | 1000 rows = cardinality 1000 |

### SQL Example

```sql
-- Table তৈরি
CREATE TABLE students (
    id       INT          PRIMARY KEY AUTO_INCREMENT,
    name     VARCHAR(100) NOT NULL,
    email    VARCHAR(150) UNIQUE NOT NULL,
    age      INT,
    dept     VARCHAR(50)
);

-- Data insert
INSERT INTO students (name, email, age, dept)
VALUES ('Rafi Ahmed', 'rafi@example.com', 22, 'CSE');

-- Data দেখা
SELECT * FROM students;
```

**Output:**

```
+----+------------+------------------+-----+------+
| id | name       | email            | age | dept |
+----+------------+------------------+-----+------+
|  1 | Rafi Ahmed | rafi@example.com |  22 | CSE  |
+----+------------+------------------+-----+------+
```

---

## ১.৭ Primary Key

### সংজ্ঞা

**Primary Key** হলো একটি column বা columns এর সমষ্টি যা table এর প্রতিটি row কে **uniquely identify** করে।

### Primary Key এর বৈশিষ্ট্য

```
Primary Key এর ৩টি বাধ্যতামূলক নিয়ম
┌─────────────────────────────────────────┐
│ 1. UNIQUE — প্রতিটি row এ ভিন্ন মান    │
│ 2. NOT NULL — কখনো খালি থাকবে না       │
│ 3. IMMUTABLE — পরিবর্তন না করাই ভালো  │
└─────────────────────────────────────────┘
```

### Real-Life Analogy

- **NID নম্বর** → প্রতিটি বাংলাদেশি নাগরিকের unique
- **Student Roll Number** → একটি school এ unique
- **Product Barcode** → প্রতিটি পণ্যের unique identifier

### SQL Example

```sql
-- Simple Primary Key
CREATE TABLE students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(100) NOT NULL
);

-- Composite Primary Key (দুটো column মিলে primary key)
CREATE TABLE enrollment (
    student_id INT,
    course_id  INT,
    PRIMARY KEY (student_id, course_id)
);
```

### Interview-Style Explanation

**প্রশ্ন:** "Primary Key কী? কেন দরকার?"

**আদর্শ উত্তর:**
> "Primary Key হলো একটি column বা column combination যা প্রতিটি row কে uniquely identify করে। এটি NOT NULL এবং UNIQUE হতে বাধ্য। Primary Key ছাড়া আমরা নির্দিষ্ট একটি record খুঁজে পাব না। উদাহরণ — দুজন student এর নাম 'Rafi' হতে পারে, কিন্তু তাদের `student_id` আলাদা। তাই `student_id` primary key হওয়া উচিত।"

### Common Mistakes

- ❌ Name কে Primary Key করা — নাম duplicate হতে পারে
- ❌ Email কে Primary Key করা — email পরিবর্তন হতে পারে, আর PK stable হওয়া উচিত
- ✅ Auto-increment integer বা UUID best practice

### Follow-up Interview Questions

1. Natural Key vs Surrogate Key কী?
2. একটি table এ কয়টি Primary Key থাকতে পারে?
3. Primary Key automatically Index তৈরি করে কি?

---

## ১.৮ Foreign Key

### সংজ্ঞা

**Foreign Key** হলো একটি table এর column যা **অন্য table এর Primary Key কে reference** করে। এটি দুটি table এর মধ্যে **সম্পর্ক (relationship)** তৈরি করে এবং **Referential Integrity** নিশ্চিত করে।

### Real-Life Analogy

- **Student** table এর `dept_id` column → **Department** table এর `id` কে point করে
- যেমন: আপনার **Passport** এ **NID নম্বর** থাকে, সেই NID নম্বর আসলে **NID Database** এ আছে

### SQL Example

```sql
-- Parent Table
CREATE TABLE departments (
    dept_id   INT          PRIMARY KEY AUTO_INCREMENT,
    dept_name VARCHAR(100) NOT NULL
);

-- Child Table with Foreign Key
CREATE TABLE students (
    student_id INT          PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(100) NOT NULL,
    dept_id    INT,
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
        ON DELETE SET NULL
        ON UPDATE CASCADE
);
```

### ON DELETE / ON UPDATE Behavior

| Option | মানে |
|--------|------|
| `CASCADE` | Parent delete হলে child-ও delete হবে |
| `SET NULL` | Parent delete হলে child এর FK = NULL |
| `RESTRICT` | Parent delete করতে দেবে না যদি child থাকে |
| `NO ACTION` | RESTRICT এর মতোই (default) |
| `SET DEFAULT` | Parent delete হলে child এর FK = default value |

### Interview-Style Explanation

**প্রশ্ন:** "Foreign Key কী? Referential Integrity বলতে কী বোঝায়?"

**আদর্শ উত্তর:**
> "Foreign Key হলো একটি column যা অন্য table এর Primary Key কে reference করে এবং দুটি table এর মধ্যে logical relationship তৈরি করে। Referential Integrity মানে হলো — child table এ এমন কোনো value থাকবে না যা parent table এ exist করে না। যেমন, `students` table এ `dept_id = 99` থাকতে পারবে না যদি `departments` table এ `id = 99` না থাকে।"

### Common Mistakes

- ❌ Foreign Key ছাড়া join করা — logically হয় কিন্তু integrity নিশ্চিত হয় না
- ❌ Foreign Key column এ Index না দেওয়া — performance hit
- ✅ Foreign Key সবসময় indexed থাকা উচিত (MySQL automatically করে)

### Follow-up Interview Questions

1. Foreign Key ছাড়া কি relationship express করা যায়?
2. Self-referential Foreign Key কী? উদাহরণ দিন।
3. Cascade delete কখন dangerous?

---

## ১.৯ Candidate Key

### সংজ্ঞা

**Candidate Key** হলো একটি table এর সেই column বা column combination যা **Primary Key হওয়ার যোগ্য** — অর্থাৎ UNIQUE এবং NOT NULL।

একটি table এ **একাধিক Candidate Key** থাকতে পারে। তাদের মধ্যে **একটিকে Primary Key** হিসেবে বেছে নেওয়া হয়, বাকিগুলো **Alternate Key** হয়ে যায়।

### উদাহরণ

```
students table:
┌────────────┬────────────┬──────────────────┬──────────┐
│ student_id │ roll_number│ email            │ name     │
├────────────┼────────────┼──────────────────┼──────────┤
│ 1          │ CSE-2024-01│ rafi@example.com │ Rafi     │
│ 2          │ CSE-2024-02│ sumi@example.com │ Sumaiya  │
└────────────┴────────────┴──────────────────┴──────────┘

Candidate Keys:
  → student_id    (UNIQUE + NOT NULL ✅)
  → roll_number   (UNIQUE + NOT NULL ✅)
  → email         (UNIQUE + NOT NULL ✅)

Primary Key হিসেবে বেছে নেওয়া হলো: student_id
Alternate Keys: roll_number, email
```

### Interview Tip

> **Memory Trick:** "Candidate = প্রার্থী। যারা Primary Key হওয়ার প্রার্থী তারাই Candidate Key।"

---

## ১.১০ Super Key

### সংজ্ঞা

**Super Key** হলো যেকোনো column বা column combination যা দিয়ে table এর প্রতিটি row কে **uniquely identify** করা যায়। Candidate Key হলো **Minimum Super Key** (অপ্রয়োজনীয় column বাদ দিলে)।

### উদাহরণ

```
students table: (student_id, name, email)

Super Keys:
  → {student_id}                    ✅ Minimal → Candidate Key
  → {email}                         ✅ Minimal → Candidate Key
  → {student_id, name}              ✅ Super Key (কিন্তু Candidate Key নয়)
  → {student_id, email}             ✅ Super Key
  → {student_id, name, email}       ✅ Super Key
  → {name}                          ❌ নাম unique নয়
```

### Key সম্পর্কের চিত্র

```
Super Key (সবচেয়ে বড় সেট)
  └── Candidate Key (Minimal Super Key)
        ├── Primary Key (বেছে নেওয়া একটি)
        └── Alternate Key (বাকিগুলো)
```

---

## ১.১১ Composite Key

### সংজ্ঞা

**Composite Key** হলো **দুই বা তার বেশি columns** এর সমষ্টি যা মিলে একটি table এর rows কে uniquely identify করে। একটি single column এ uniqueness না থাকলে multiple columns মিলে Composite Key তৈরি করা হয়।

### Real-Life Analogy

- **Student-Course Enrollment:** একজন student অনেক course নিতে পারে, একটি course এ অনেক student থাকতে পারে। তাই `(student_id, course_id)` একসাথে composite primary key।

### SQL Example

```sql
CREATE TABLE enrollment (
    student_id INT  NOT NULL,
    course_id  INT  NOT NULL,
    grade      CHAR(2),
    PRIMARY KEY (student_id, course_id),  -- Composite Primary Key
    FOREIGN KEY (student_id) REFERENCES students(student_id),
    FOREIGN KEY (course_id)  REFERENCES courses(course_id)
);
```

### Common Mistakes

- ❌ Composite key এর মানে দুটো আলাদা primary key — না, একসাথে একটি key
- ✅ Many-to-Many relationship এ composite key সবচেয়ে বেশি দরকার

---

## ১.১২ Unique Key

### সংজ্ঞা

**Unique Key** হলো একটি constraint যা নিশ্চিত করে যে একটি column এর সব value **unique** হবে। Primary Key এর মতোই, তবে **NULL ধারণ করতে পারে**।

### Primary Key vs Unique Key তুলনা

| বিষয় | Primary Key | Unique Key |
|------|------------|-----------|
| NULL value | ❌ অনুমতি নেই | ✅ একটি NULL অনুমতি আছে (MySQL) |
| প্রতি table এ সংখ্যা | শুধুমাত্র ১টি | একাধিক হতে পারে |
| Index | Clustered Index | Non-clustered Index |
| মূল উদ্দেশ্য | Row identification | Column uniqueness নিশ্চিত |

### SQL Example

```sql
CREATE TABLE users (
    user_id  INT          PRIMARY KEY AUTO_INCREMENT,
    email    VARCHAR(150) UNIQUE NOT NULL,    -- Unique, no NULL
    phone    VARCHAR(15)  UNIQUE,             -- Unique, NULL ok
    username VARCHAR(50)  UNIQUE NOT NULL
);

-- Duplicate email insert করার চেষ্টা করলে:
-- ERROR 1062 (23000): Duplicate entry for key 'email'
```

---

## ১.১৩ NULL

### সংজ্ঞা

**NULL** হলো database এ **অজানা বা অনুপস্থিত মানের** প্রতীক। এটি **0 (শূন্য)** বা **empty string ('')** নয় — এটি সম্পূর্ণ আলাদা একটি বিশেষ state।

### NULL এর বৈশিষ্ট্য

```sql
-- NULL কোনো value এর সাথে equal নয়, এমনকি নিজের সাথেও
SELECT NULL = NULL;    -- Result: NULL (not TRUE!)
SELECT NULL != NULL;   -- Result: NULL (not FALSE!)

-- NULL check করতে IS NULL বা IS NOT NULL ব্যবহার করতে হয়
SELECT * FROM students WHERE phone IS NULL;
SELECT * FROM students WHERE phone IS NOT NULL;

-- NULL এ arithmetic করলে সবসময় NULL আসে
SELECT 5 + NULL;  -- Result: NULL
SELECT NULL * 0;  -- Result: NULL (0 নয়!)
```

### Real-Life Analogy

- **NULL** = "জানি না" বা "প্রযোজ্য নয়"
- কোনো student এর phone number না জানলে NULL
- কোনো employee এর manager না থাকলে (CEO) manager_id = NULL

### Interview-Style Explanation

**প্রশ্ন:** "NULL কী? NULL = 0 কি সত্য?"

**আদর্শ উত্তর:**
> "NULL মানে 'unknown' বা 'missing value' — এটি 0 বা empty string নয়। `NULL = NULL` এমনকি FALSE নয়, এটি NULL। তাই NULL check করতে `= NULL` ব্যবহার করলে কাজ হয় না, `IS NULL` বা `IS NOT NULL` ব্যবহার করতে হয়। এটি Three-Valued Logic (TRUE, FALSE, NULL) এর অংশ।"

### Common Mistakes

- ❌ `WHERE column = NULL` — এটি কাজ করে না
- ✅ `WHERE column IS NULL` — সঠিক পদ্ধতি
- ❌ NULL কে 0 ধরে calculation করা — সব calculation NULL হয়ে যাবে

---

## ১.১৪ Constraints

### সংজ্ঞা

**Constraints** হলো database এ **নিয়মকানুন (rules)** যা data এর **integrity এবং validity** নিশ্চিত করে। এগুলো table define করার সময় set করা হয়।

### সকল Constraint এর বিবরণ

| Constraint | কাজ | উদাহরণ |
|-----------|-----|--------|
| `PRIMARY KEY` | Unique + NOT NULL row identifier | `student_id` |
| `FOREIGN KEY` | Referential integrity নিশ্চিত | `dept_id` references departments |
| `UNIQUE` | Column এ duplicate বন্ধ | `email` |
| `NOT NULL` | NULL value বন্ধ | `name` |
| `CHECK` | Custom validation rule | `age > 0 AND age < 150` |
| `DEFAULT` | কোনো value না দিলে default ব্যবহার | `status DEFAULT 'active'` |
| `AUTO_INCREMENT` | Automatically value বাড়ে | `id` |

### SQL Example

```sql
CREATE TABLE employees (
    emp_id     INT            PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(100)   NOT NULL,
    email      VARCHAR(150)   UNIQUE NOT NULL,
    salary     DECIMAL(10, 2) CHECK (salary > 0),
    dept_id    INT            NOT NULL,
    status     VARCHAR(20)    DEFAULT 'active',
    join_date  DATE           DEFAULT (CURRENT_DATE),
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
        ON DELETE RESTRICT
        ON UPDATE CASCADE
);

-- CHECK constraint এর উদাহরণ
-- salary = -5000 দিলে: ERROR — Check constraint violated
```

### Interview-Style Explanation

**প্রশ্ন:** "Database Constraints কী? কেন দরকার?"

**আদর্শ উত্তর:**
> "Constraints হলো database level এ enforce করা rules যা invalid data insert হওয়া থেকে রক্ষা করে। Application level এ validation দিলেও, database level এ constraints রাখলে যেকোনো source থেকে আসা invalid data block হয়। যেমন — NOT NULL constraint থাকলে কোনো bug বা direct SQL insert এ NULL value আসতে পারবে না।"

---

## ১.১৫ Relationships

### ধরনসমূহ

Database এ তিন ধরনের relationship থাকে:

---

### One-to-One (১:১)

**সংজ্ঞা:** Table A এর একটি row, Table B এর **শুধুমাত্র একটি** row এর সাথে সম্পর্কিত।

**Real-Life Analogy:** একজন ব্যক্তির একটিমাত্র NID Card

```sql
-- User এবং UserProfile (1:1)
CREATE TABLE users (
    user_id  INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) UNIQUE NOT NULL
);

CREATE TABLE user_profiles (
    profile_id  INT PRIMARY KEY AUTO_INCREMENT,
    user_id     INT UNIQUE NOT NULL,         -- UNIQUE ensures 1:1
    bio         TEXT,
    avatar_url  VARCHAR(255),
    FOREIGN KEY (user_id) REFERENCES users(user_id)
        ON DELETE CASCADE
);
```

**কখন ব্যবহার:**
- Main table অনেক বড় হলে optional data আলাদা রাখতে
- Security কারণে sensitive data আলাদা রাখতে (password hash)

---

### One-to-Many (১:N)

**সংজ্ঞা:** Table A এর একটি row, Table B এর **একাধিক** row এর সাথে সম্পর্কিত। Database এ **সবচেয়ে সাধারণ** relationship।

**Real-Life Analogy:**
- একজন Teacher → অনেক Students
- একটি Department → অনেক Employees
- একটি Customer → অনেক Orders

```sql
-- Department (1) → Employees (Many)
CREATE TABLE departments (
    dept_id   INT          PRIMARY KEY AUTO_INCREMENT,
    dept_name VARCHAR(100) NOT NULL
);

CREATE TABLE employees (
    emp_id  INT          PRIMARY KEY AUTO_INCREMENT,
    name    VARCHAR(100) NOT NULL,
    dept_id INT,
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
);

-- একটি department এর সব employees
SELECT e.name, d.dept_name
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
WHERE d.dept_id = 1;
```

---

### Many-to-Many (M:N)

**সংজ্ঞা:** Table A এর একটি row, Table B এর **একাধিক** row এর সাথে সম্পর্কিত এবং উল্টোটাও সত্য। এটি implement করতে একটি **Junction Table (Bridge Table)** দরকার।

**Real-Life Analogy:**
- একজন Student → অনেক Courses নিতে পারে
- একটি Course → অনেক Students থাকতে পারে

```sql
-- Students (M) ↔ Courses (N) — Junction Table: enrollment
CREATE TABLE students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(100) NOT NULL
);

CREATE TABLE courses (
    course_id   INT PRIMARY KEY AUTO_INCREMENT,
    course_name VARCHAR(100) NOT NULL
);

-- Junction Table
CREATE TABLE enrollment (
    student_id   INT  NOT NULL,
    course_id    INT  NOT NULL,
    enrolled_at  DATE DEFAULT (CURRENT_DATE),
    grade        CHAR(2),
    PRIMARY KEY (student_id, course_id),
    FOREIGN KEY (student_id) REFERENCES students(student_id) ON DELETE CASCADE,
    FOREIGN KEY (course_id)  REFERENCES courses(course_id)   ON DELETE CASCADE
);

-- একজন student এর সব courses
SELECT s.name, c.course_name, e.grade
FROM enrollment e
INNER JOIN students s ON e.student_id = s.student_id
INNER JOIN courses  c ON e.course_id  = c.course_id
WHERE s.student_id = 1;
```

### Relationship তুলনা

| Relationship | উদাহরণ | Implementation |
|-------------|--------|----------------|
| One-to-One | User → Profile | UNIQUE Foreign Key |
| One-to-Many | Dept → Employees | Foreign Key (child তে) |
| Many-to-Many | Students ↔ Courses | Junction Table |

### Interview-Style Explanation

**প্রশ্ন:** "Many-to-Many relationship কীভাবে implement করবেন?"

**আদর্শ উত্তর:**
> "Many-to-Many relationship দুটো table দিয়ে directly implement করা যায় না। এর জন্য একটি Junction Table বা Bridge Table দরকার। এই table এ দুটো parent table এর Primary Key রাখা হয় এবং একসাথে Composite Primary Key হিসেবে ব্যবহার করা হয়। এতে duplicate enrollment prevent হয় এবং referential integrity maintain হয়।"

---

## ১.১৬ ER Diagram

### সংজ্ঞা

**ER Diagram (Entity-Relationship Diagram)** হলো database design এর একটি **visual representation** যেখানে entities, তাদের attributes, এবং তাদের মধ্যে relationships চিত্রের মাধ্যমে দেখানো হয়। **Peter Chen** ১৯৭৬ সালে এটি প্রবর্তন করেন।

### ER Diagram এর Components

| Symbol | নাম | কাজ |
|--------|-----|-----|
| **Rectangle** | Entity | Table (যেমন: Student, Course) |
| **Ellipse** | Attribute | Column (যেমন: name, age) |
| **Diamond** | Relationship | Tables এর সম্পর্ক |
| **Double Ellipse** | Multi-valued Attribute | একাধিক value (যেমন: phone numbers) |
| **Dashed Ellipse** | Derived Attribute | অন্য attribute থেকে calculated (যেমন: age from DOB) |
| **Double Rectangle** | Weak Entity | নিজে identify হতে পারে না |
| **Line** | Connection | Entity-Attribute, Entity-Relationship সংযোগ |

### Simple ER Diagram উদাহরণ (Text Representation)

```
[Student] ──── has ──── [Student_ID (PK)]
    │                   [Name]
    │                   [Email]
    │                   [Age]
    │
 ENROLLS (M:N)
    │
    │
[Course] ──── has ──── [Course_ID (PK)]
                        [Course_Name]
                        [Credits]

Cardinality:
Student ||──── ENROLLS ────|| Course
        M                   N
```

### Interview-Style Explanation

**প্রশ্ন:** "ER Diagram কী? কীভাবে তৈরি করেন?"

**আদর্শ উত্তর:**
> "ER Diagram হলো database design এর visual blueprint। এটি দিয়ে আমরা tables, columns, এবং relationships design করি coding শুরুর আগে। প্রথমে entities identify করি (যেমন Student, Course), তারপর attributes (name, age), তারপর relationships (Student ENROLLS Course)। Cardinality (1:1, 1:N, M:N) দিয়ে সম্পর্কের ধরন দেখাই। এই diagram থেকেই SQL schema তৈরি হয়।"

---

## ১.১৭ Schema vs Instance

### সংজ্ঞা

| Term | সংজ্ঞা | উদাহরণ |
|------|--------|--------|
| **Schema** | Database এর **structure বা blueprint** — কোন tables আছে, কী কী columns, কী কী constraints | `CREATE TABLE students (id INT, name VARCHAR(100))` |
| **Instance** | একটি নির্দিষ্ট সময়ে database এ **actual data** | students table এ এখন ৫০০ জন student এর record |

### Real-Life Analogy

- **Schema** = বাড়ির নকশা (blueprint) — কতটি রুম, কোথায় দরজা
- **Instance** = এই মুহূর্তে বাড়িতে কে কে আছে

### চিত্র

```
Schema (পরিবর্তন হয় না বা কম হয়):
  ┌──────────────────────────────────┐
  │ TABLE: students                  │
  │   - id: INT PK                   │
  │   - name: VARCHAR(100) NOT NULL  │
  │   - email: VARCHAR(150) UNIQUE   │
  └──────────────────────────────────┘

Instance (প্রতিনিয়ত পরিবর্তন হয়):
  ┌────┬────────────┬──────────────────┐
  │ id │ name       │ email            │
  ├────┼────────────┼──────────────────┤
  │  1 │ Rafi Ahmed │ rafi@gmail.com   │
  │  2 │ Sumi Islam │ sumi@gmail.com   │
  └────┴────────────┴──────────────────┘
  (আজকে ২ জন, কালকে ২০০ জনও হতে পারে)
```

---

## ১.১৮ Data Integrity

### সংজ্ঞা

**Data Integrity** মানে হলো database এ সংরক্ষিত data **সঠিক, সামঞ্জস্যপূর্ণ এবং নির্ভরযোগ্য** থাকা।

### Data Integrity এর ৪টি ধরন

| ধরন | সংজ্ঞা | Enforce করার উপায় |
|-----|--------|------------------|
| **Entity Integrity** | প্রতিটি row uniquely identifiable | Primary Key |
| **Referential Integrity** | FK সবসময় valid PK reference করবে | Foreign Key |
| **Domain Integrity** | Column এ শুধু valid value থাকবে | Data Type, CHECK, NOT NULL |
| **User-defined Integrity** | Business rules অনুযায়ী validation | Triggers, Stored Procedures |

### SQL Example

```sql
-- Entity Integrity: PRIMARY KEY দিয়ে
CREATE TABLE products (
    product_id INT PRIMARY KEY AUTO_INCREMENT,   -- Entity Integrity
    name       VARCHAR(100) NOT NULL,
    price      DECIMAL(10,2) CHECK (price >= 0), -- Domain Integrity
    category   VARCHAR(50) DEFAULT 'general'
);

-- Referential Integrity: FOREIGN KEY দিয়ে
CREATE TABLE order_items (
    item_id    INT PRIMARY KEY AUTO_INCREMENT,
    order_id   INT NOT NULL,
    product_id INT NOT NULL,
    quantity   INT CHECK (quantity > 0),         -- Domain Integrity
    FOREIGN KEY (product_id) REFERENCES products(product_id)
        ON DELETE RESTRICT  -- Referential Integrity enforce
);
```

---

## ১.১৯ Normalization Overview

### সংজ্ঞা

**Normalization** হলো database design এর একটি প্রক্রিয়া যেখানে **data redundancy (পুনরাবৃত্তি) কমানো** এবং **data integrity বাড়ানো** হয় — table গুলোকে সুশৃঙ্খলভাবে ভাগ করে।

> **বিস্তারিত Normalization PART 4 এ আলোচনা করা হবে।**

### সংক্ষিপ্ত Normal Forms

| Normal Form | মূল নিয়ম |
|------------|----------|
| **1NF** | প্রতিটি cell এ atomic (একটি) value থাকবে, কোনো repeating group নয় |
| **2NF** | 1NF + কোনো Partial Dependency নেই |
| **3NF** | 2NF + কোনো Transitive Dependency নেই |
| **BCNF** | 3NF এর আরও strict version |

### Real-Life উদাহরণ (সমস্যা)

```
❌ Unnormalized Table:
┌────────┬───────────────┬──────────────────────┬──────────────────────┐
│ Stu_ID │ Name          │ Courses              │ Instructor           │
├────────┼───────────────┼──────────────────────┼──────────────────────┤
│   1    │ Rafi          │ OOP, Database        │ Dr. Karim, Dr. Alam  │
│   2    │ Sumi          │ OOP                  │ Dr. Karim            │
└────────┴───────────────┴──────────────────────┴──────────────────────┘

সমস্যা:
- Courses column এ multiple value (1NF লঙ্ঘন)
- Dr. Karim OOP পড়ান — এটি দুই জায়গায় আছে (Redundancy)
- Rafi delete হলে Dr. Karim OOP পড়ান এই তথ্যও হারায় (Delete Anomaly)
```

```
✅ Normalized (3NF):
Students: (student_id, name)
Courses: (course_id, course_name, instructor_id)
Instructors: (instructor_id, instructor_name)
Enrollment: (student_id, course_id)
```

### Interview Tip

> "Normalization মানে শুধু 1NF, 2NF, 3NF মুখস্থ নয় — বুঝতে হবে কেন করছি এবং কখন Denormalization করা উচিত।"

---

## ১.২০ PART 1 — Interview Questions & Answers

### সেকশন ১: মৌলিক প্রশ্নোত্তর

**Q1: Database এবং Spreadsheet (Excel) এর মধ্যে পার্থক্য কী?**

> **উত্তর:** Excel হলো flat file যেখানে limited rows, no relationships, no concurrent multi-user access, এবং no transaction support। Database এ millions of rows, tables এর মধ্যে relationships, simultaneous user access, ACID transactions, এবং complex query করা যায়। Production application এ সবসময় proper database ব্যবহার করা উচিত।

---

**Q2: Primary Key এবং Unique Key এর মধ্যে পার্থক্য কী?**

> **উত্তর:** Primary Key হলো row identifier — NULL হতে পারে না এবং প্রতি table এ শুধু একটি। Unique Key NULL ধারণ করতে পারে (MySQL এ একটি) এবং একটি table এ একাধিক থাকতে পারে। Primary Key automatically Clustered Index তৈরি করে, Unique Key Non-clustered Index।

---

**Q3: Foreign Key এর কাজ কী? ON DELETE CASCADE মানে কী?**

> **উত্তর:** Foreign Key referential integrity নিশ্চিত করে — child table এ এমন value থাকতে পারবে না যা parent table এ নেই। `ON DELETE CASCADE` মানে parent record delete হলে সব child records automatically delete হবে। যেমন — একটি Order delete হলে তার সব Order_Items ও delete হবে। এটি convenient কিন্তু অসাবধানে ব্যবহার করলে accidental data loss হতে পারে।

---

**Q4: NULL = 0 কি? NULL এ arithmetic করলে কী হয়?**

> **উত্তর:** না। NULL মানে "unknown" — এটি 0 বা empty string নয়। NULL এ যেকোনো arithmetic করলে result NULL হয় (5 + NULL = NULL)। NULL compare করতে `IS NULL` বা `IS NOT NULL` ব্যবহার করতে হয়, `= NULL` কাজ করে না।

---

**Q5: Candidate Key, Super Key, এবং Primary Key এর সম্পর্ক কী?**

> **উত্তর:** Super Key হলো যেকোনো column combination যা rows uniquely identify করে। Candidate Key হলো Minimal Super Key — unnecessary columns বাদ দিলে যা থাকে। Candidate Keys এর মধ্যে থেকে একটিকে Primary Key হিসেবে বেছে নেওয়া হয়, বাকিগুলো Alternate Key। সব Primary Key, Candidate Key। সব Candidate Key, Super Key।

---

**Q6: One-to-Many এবং Many-to-Many relationship implement করার পদ্ধতি কী?**

> **উত্তর:** One-to-Many: Child table এ Parent এর Primary Key Foreign Key হিসেবে রাখো। Many-to-Many: দুটো Parent table এর Primary Key ধারণ করে একটি Junction Table তৈরি করো এবং দুটো column মিলে Composite Primary Key করো।

---

### সেকশন ২: Rapid-Fire প্রশ্নোত্তর

| প্রশ্ন | সংক্ষিপ্ত উত্তর |
|-------|----------------|
| DBMS এর full form | Database Management System |
| RDBMS এর inventor | E.F. Codd (১৯৭০) |
| SQL এর full form | Structured Query Language |
| একটি table এ কয়টি PK হতে পারে? | শুধুমাত্র ১টি |
| NULL = '' কি? | না, সম্পূর্ণ আলাদা |
| Composite Key কোথায় দরকার? | Many-to-Many junction table এ |
| Junction Table এর অন্য নাম | Bridge Table / Associative Table |
| ER Diagram কে তৈরি করেন? | Peter Chen (১৯৭৬) |
| Schema পরিবর্তন হলে Instance পরিবর্তন হয়? | না, সবসময় নয় |
| Referential Integrity কোন Key নিশ্চিত করে? | Foreign Key |

---

### Follow-up Questions (Interview এ জিজ্ঞেস হতে পারে)

1. Database এ Index কী? কেন দরকার? *(PART 3 এ বিস্তারিত)*
2. Transaction কী? ACID বলতে কী বোঝায়? *(PART 3 এ বিস্তারিত)*
3. 1NF, 2NF, 3NF কী? *(PART 4 এ বিস্তারিত)*
4. NoSQL কখন ব্যবহার করবেন? *(PART 8 এ বিস্তারিত)*
5. Database Optimization কীভাবে করবেন? *(PART 3 এ বিস্তারিত)*

---

> **⚠️ PART 1 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part2"></a>

# PART 2: SQL Fundamentals (SQL এর মূল ভিত্তি)

> **📍 এই PART এর Sections:** [Setup](#practice-database-setup) · [২.১ SELECT](#২১-select) · [২.২ WHERE](#২২-where) · [২.৩ ORDER BY](#২৩-order-by)

> **ব্যবহারের নিয়ম:** প্রতিটি query নিজে একটি database এ run করুন। MySQL Workbench বা DBeaver ব্যবহার করুন। শুধু পড়লে হবে না — লিখতে হবে।

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## Practice Database Setup

সব PART 2 উদাহরণ নিচের tables ব্যবহার করবে:

```sql
CREATE DATABASE company_db;
USE company_db;

CREATE TABLE departments (
    dept_id   INT          PRIMARY KEY AUTO_INCREMENT,
    dept_name VARCHAR(100) NOT NULL,
    location  VARCHAR(100)
);

CREATE TABLE employees (
    emp_id     INT            PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(100)   NOT NULL,
    email      VARCHAR(150)   UNIQUE NOT NULL,
    salary     DECIMAL(10, 2),
    dept_id    INT,
    join_date  DATE,
    manager_id INT,
    FOREIGN KEY (dept_id)    REFERENCES departments(dept_id),
    FOREIGN KEY (manager_id) REFERENCES employees(emp_id)
);

CREATE TABLE projects (
    project_id   INT          PRIMARY KEY AUTO_INCREMENT,
    project_name VARCHAR(100) NOT NULL,
    budget       DECIMAL(15,2),
    dept_id      INT,
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
);

INSERT INTO departments (dept_name, location) VALUES
    ('Engineering', 'Dhaka'),
    ('Marketing',   'Chittagong'),
    ('HR',          'Dhaka'),
    ('Finance',     'Sylhet');

INSERT INTO employees (name, email, salary, dept_id, join_date, manager_id) VALUES
    ('Karim Ahmed',  'karim@company.com',  85000, 1, '2020-01-15', NULL),
    ('Rafi Hasan',   'rafi@company.com',   60000, 1, '2021-03-10', 1),
    ('Sumi Islam',   'sumi@company.com',   55000, 2, '2021-07-01', NULL),
    ('Tanvir Khan',  'tanvir@company.com', 70000, 1, '2022-01-20', 1),
    ('Nadia Parvin', 'nadia@company.com',  50000, 3, '2022-05-15', NULL),
    ('Imran Ali',    'imran@company.com',  65000, 2, '2023-02-28', 3),
    ('Fatema Begum', 'fatema@company.com', 45000, 4, '2023-08-10', NULL),
    ('Sakib Rahman', 'sakib@company.com',  75000, 1, '2020-11-05', 1);

INSERT INTO projects (project_name, budget, dept_id) VALUES
    ('ERP System',         5000000, 1),
    ('Marketing Campaign', 1500000, 2),
    ('HR Portal',           800000, 3),
    ('Mobile App',         3000000, 1);
```

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১ SELECT

### সংজ্ঞা

**SELECT** হলো SQL এর সবচেয়ে মৌলিক ও সবচেয়ে বেশি ব্যবহৃত command। এটি দিয়ে database থেকে data **পড়া (read)** হয়। SELECT **DQL (Data Query Language)** এর অন্তর্গত।

### Syntax

```sql
SELECT column1, column2, ...   -- কোন columns দেখতে চান
FROM   table_name               -- কোন table থেকে
WHERE  condition                -- কোন শর্তে (optional)
GROUP BY column                 -- গ্রুপ করতে (optional)
HAVING group_condition          -- গ্রুপের শর্ত (optional)
ORDER BY column ASC|DESC        -- সাজানো (optional)
LIMIT  n;                       -- কতটি row (optional)
```

### উদাহরণ

```sql
-- সব columns
SELECT * FROM employees;

-- নির্দিষ্ট columns
SELECT name, salary, dept_id FROM employees;

-- Column alias
SELECT name   AS employee_name,
       salary AS monthly_salary
FROM employees;

-- Expression
SELECT name,
       salary,
       salary * 12  AS annual_salary,
       salary * 0.1 AS bonus
FROM employees;
```

### Interview Trick

> "`SELECT *` production code এ ব্যবহার করা উচিত নয় — (১) অপ্রয়োজনীয় data transfer, (২) নতুন column যোগ হলে application break হতে পারে, (৩) Index ভালোভাবে ব্যবহার হয় না।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.২ WHERE

### সংজ্ঞা

**WHERE** clause দিয়ে নির্দিষ্ট **শর্তে** data filter করা হয়। SELECT, UPDATE, DELETE সব এ ব্যবহার হয়।

### উদাহরণ

```sql
SELECT name, salary FROM employees WHERE salary > 60000;

SELECT name, salary, dept_id
FROM employees
WHERE salary > 50000 AND dept_id = 1;

SELECT name FROM employees WHERE dept_id = 1 OR dept_id = 2;

-- NULL check
SELECT name FROM employees WHERE manager_id IS NULL;
SELECT name FROM employees WHERE manager_id IS NOT NULL;
```

### Comparison Operators

| Operator | মানে | উদাহরণ |
|----------|------|--------|
| `=` | সমান | `WHERE dept_id = 1` |
| `!=` বা `<>` | সমান নয় | `WHERE status != 'inactive'` |
| `>` | বড় | `WHERE salary > 50000` |
| `<` | ছোট | `WHERE salary < 80000` |
| `>=` | বড় বা সমান | `WHERE salary >= 60000` |
| `IS NULL` | NULL | `WHERE manager_id IS NULL` |
| `IS NOT NULL` | NULL নয় | `WHERE email IS NOT NULL` |

### Common Mistakes

- ❌ `WHERE salary = NULL` → কাজ করে না
- ✅ `WHERE salary IS NULL` → সঠিক

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৩ ORDER BY

### সংজ্ঞা

**ORDER BY** দিয়ে result **ascending (ASC)** বা **descending (DESC)** order এ সাজানো হয়। Default হলো ASC।

### উদাহরণ

```sql
SELECT name, salary FROM employees ORDER BY salary;
SELECT name, salary FROM employees ORDER BY salary DESC;

-- Multiple column sort
SELECT name, dept_id, salary
FROM employees
ORDER BY dept_id ASC, salary DESC;
```

### Interview Trick

> "ORDER BY ছাড়া SELECT এর result order গ্যারান্টিড নয়। Consistent result চাইলে সবসময় ORDER BY দিন।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৪ GROUP BY

### সংজ্ঞা

**GROUP BY** দিয়ে একই value এর rows কে **group এ** আনা হয় এবং প্রতিটি group এ **aggregate function** apply করা হয়।

### Aggregate Functions

| Function | কাজ |
|----------|-----|
| `COUNT()` | row গণনা |
| `SUM()` | যোগফল |
| `AVG()` | গড় |
| `MAX()` | সর্বোচ্চ |
| `MIN()` | সর্বনিম্ন |

### উদাহরণ

```sql
-- প্রতি department এ কতজন
SELECT dept_id, COUNT(*) AS total_employees
FROM employees
GROUP BY dept_id;

-- মোট ও গড় salary প্রতি department
SELECT
    dept_id,
    COUNT(*)    AS headcount,
    SUM(salary) AS total_salary,
    AVG(salary) AS avg_salary,
    MAX(salary) AS highest,
    MIN(salary) AS lowest
FROM employees
GROUP BY dept_id;

-- JOIN সহ GROUP BY
SELECT
    d.dept_name,
    COUNT(e.emp_id) AS headcount,
    AVG(e.salary)   AS avg_salary
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
GROUP BY d.dept_id, d.dept_name
ORDER BY avg_salary DESC;
```

### Common Mistakes

```sql
-- ❌ name GROUP BY তে নেই
SELECT dept_id, name, COUNT(*) FROM employees GROUP BY dept_id;
-- ERROR: 'name' is not in GROUP BY

-- ✅ সঠিক
SELECT dept_id, COUNT(*) FROM employees GROUP BY dept_id;
```

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৫ HAVING

### সংজ্ঞা

**HAVING** হলো GROUP BY এর পরের **group-level filter**।

### WHERE vs HAVING

| বিষয় | WHERE | HAVING |
|------|-------|--------|
| কখন apply | GROUP BY এর **আগে** | GROUP BY এর **পরে** |
| কীসে filter | Individual rows | Groups |
| Aggregate function | ব্যবহার করা যায় না | ব্যবহার করা যায় |

### উদাহরণ

```sql
-- ৩ এর বেশি employee আছে এমন departments
SELECT dept_id, COUNT(*) AS total
FROM employees
GROUP BY dept_id
HAVING COUNT(*) > 2;

-- Average salary ৬০,০০০ এর বেশি
SELECT d.dept_name, AVG(e.salary) AS avg_salary
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
GROUP BY d.dept_id, d.dept_name
HAVING AVG(e.salary) > 60000;

-- WHERE এবং HAVING একসাথে
SELECT dept_id, AVG(salary) AS avg_sal
FROM employees
WHERE join_date >= '2021-01-01'
GROUP BY dept_id
HAVING AVG(salary) > 55000;
```

### Interview-Style Explanation

**প্রশ্ন:** "WHERE এবং HAVING এর মধ্যে পার্থক্য কী?"

**আদর্শ উত্তর:**
> "WHERE হলো row-level filter — GROUP BY এর আগে কাজ করে, aggregate function ব্যবহার করা যায় না। HAVING হলো group-level filter — GROUP BY এর পরে কাজ করে, aggregate function ব্যবহার করা যায়।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৬ DISTINCT

### সংজ্ঞা

**DISTINCT** দিয়ে result এ **duplicate values বাদ** দেওয়া হয়।

### উদাহরণ

```sql
SELECT DISTINCT dept_id FROM employees;

SELECT COUNT(DISTINCT dept_id) AS total_departments
FROM employees;

SELECT DISTINCT salary FROM employees ORDER BY salary;
```

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৭ LIMIT

### সংজ্ঞা

**LIMIT** দিয়ে কতটি rows return হবে তা নির্ধারণ হয়। Pagination এ LIMIT + **OFFSET** ব্যবহার হয়।

### উদাহরণ

```sql
SELECT name, salary FROM employees LIMIT 5;

SELECT name, salary FROM employees ORDER BY salary DESC LIMIT 3;

-- Pagination
SELECT name, salary FROM employees LIMIT 5 OFFSET 0;  -- Page 1
SELECT name, salary FROM employees LIMIT 5 OFFSET 5;  -- Page 2
SELECT name, salary FROM employees LIMIT 5 OFFSET 10; -- Page 3
```

### Interview Trick

> "Large table এ `OFFSET 999995 LIMIT 5` করলে প্রথম ১০ লাখ rows skip করে — slow। Production এ **Keyset/Cursor-based pagination** ব্যবহার করুন।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৮ INSERT

### সংজ্ঞা

**INSERT** দিয়ে table এ **নতুন row যোগ** করা হয়। এটি **DML** এর অংশ।

### উদাহরণ

```sql
-- Single row
INSERT INTO employees (name, email, salary, dept_id, join_date)
VALUES ('Rahim Uddin', 'rahim@company.com', 55000, 2, '2024-01-15');

-- Multiple rows
INSERT INTO employees (name, email, salary, dept_id, join_date)
VALUES
    ('Ayesha Siddika', 'ayesha@company.com', 62000, 1, '2024-02-01'),
    ('Masum Billah',   'masum@company.com',  48000, 3, '2024-03-10');

-- INSERT ... SELECT
INSERT INTO employees_archive (name, email, salary)
SELECT name, email, salary FROM employees
WHERE join_date < '2021-01-01';

-- UPSERT
INSERT INTO employees (emp_id, name, salary)
VALUES (2, 'Rafi Hasan', 65000)
ON DUPLICATE KEY UPDATE salary = 65000;
```

### Common Mistakes

- ❌ Column names ছাড়া insert — structure পরিবর্তন হলে break হবে
- ✅ সবসময় column names explicitly লিখুন

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৯ UPDATE

### সংজ্ঞা

**UPDATE** দিয়ে বিদ্যমান rows এর **data পরিবর্তন** করা হয়।

> ⚠️ WHERE না দিলে **সব rows update হয়ে যাবে!**

### উদাহরণ

```sql
UPDATE employees SET salary = 70000 WHERE emp_id = 2;

UPDATE employees
SET salary  = 75000,
    dept_id = 1
WHERE emp_id = 2;

-- ১০% বৃদ্ধি (Engineering)
UPDATE employees SET salary = salary * 1.10 WHERE dept_id = 1;

-- ❌ DANGEROUS!
UPDATE employees SET salary = 50000;
```

### Safe Practice

```sql
-- আগে SELECT দিয়ে confirm করুন
SELECT * FROM employees WHERE emp_id = 2;
UPDATE employees SET salary = 70000 WHERE emp_id = 2;
```

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১০ DELETE

### সংজ্ঞা

**DELETE** দিয়ে table থেকে **row মুছে ফেলা** হয়।

### DELETE vs TRUNCATE vs DROP

| বিষয় | DELETE | TRUNCATE | DROP |
|------|--------|----------|------|
| কী করে | নির্দিষ্ট rows মুছে | সব rows (table থাকে) | পুরো table মুছে |
| WHERE | ✅ আছে | ❌ নেই | ❌ নেই |
| Rollback | ✅ হ্যাঁ | ❌ না | ❌ না |
| Trigger | ✅ হ্যাঁ | ❌ না | ❌ না |
| Auto-increment reset | ❌ না | ✅ হ্যাঁ | ✅ হ্যাঁ |
| Speed | ধীর | দ্রুত | দ্রুততম |

### উদাহরণ

```sql
DELETE FROM employees WHERE emp_id = 9;

DELETE FROM employees WHERE dept_id = 4 AND salary < 40000;

DELETE FROM employees
WHERE dept_id IN (
    SELECT dept_id FROM departments WHERE location = 'Sylhet'
);

TRUNCATE TABLE employees;  -- fast, no rollback
DROP TABLE employees;      -- table সহ সব
```

### Interview-Style Explanation

**প্রশ্ন:** "DELETE, TRUNCATE, DROP এর পার্থক্য?"

**আদর্শ উত্তর:**
> "DELETE হলো DML — WHERE দেওয়া যায়, rollback সম্ভব। TRUNCATE হলো DDL — সব rows সরায়, rollback হয় না, auto-increment reset হয়। DROP হলো DDL — পুরো table ও structure দুটোই মুছে।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১১ LIKE

### সংজ্ঞা

**LIKE** দিয়ে **pattern matching** করা হয়।
- `%` → যেকোনো সংখ্যক character
- `_` → ঠিক একটি character

### উদাহরণ

```sql
SELECT name FROM employees WHERE name LIKE 'K%';       -- 'K' দিয়ে শুরু
SELECT name FROM employees WHERE name LIKE '%ah%';     -- মাঝে 'ah'
SELECT name FROM employees WHERE name LIKE '_____';    -- ঠিক ৫ character
SELECT name FROM employees WHERE name NOT LIKE 'K%';
SELECT name, email FROM employees WHERE email LIKE '%@company.com';
```

### Interview Trick

> "`LIKE '%keyword%'` — leading wildcard থাকলে index ব্যবহার হয় না, full table scan হয়। Large table এ slow। Full-text search এর জন্য `FULLTEXT INDEX` বা Elasticsearch ব্যবহার করুন।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১২ IN

### সংজ্ঞা

**IN** দিয়ে একটি column এ **list এর মধ্যে** value match করা হয়। Multiple OR এর shortcut।

### উদাহরণ

```sql
SELECT name, dept_id FROM employees WHERE dept_id IN (1, 2, 3);

SELECT * FROM departments
WHERE dept_name IN ('Engineering', 'Marketing', 'Finance');

SELECT name FROM employees WHERE dept_id NOT IN (3, 4);

-- Subquery সহ
SELECT name FROM employees
WHERE dept_id IN (
    SELECT dept_id FROM departments WHERE location = 'Dhaka'
);
```

### ⚠️ NOT IN + NULL সমস্যা

```sql
-- Subquery তে NULL থাকলে NOT IN সবসময় empty result!
-- Safe alternative: NOT EXISTS
SELECT name FROM employees e
WHERE NOT EXISTS (
    SELECT 1 FROM departments d WHERE d.dept_id = e.dept_id
);
```

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১৩ BETWEEN

### সংজ্ঞা

**BETWEEN** দিয়ে একটি **range এর মধ্যে** value খোঁজা হয়। **Inclusive** — উভয় প্রান্ত সহ।

### উদাহরণ

```sql
SELECT name, salary FROM employees
WHERE salary BETWEEN 50000 AND 70000;

SELECT name, join_date FROM employees
WHERE join_date BETWEEN '2021-01-01' AND '2022-12-31';

SELECT name, salary FROM employees
WHERE salary NOT BETWEEN 50000 AND 70000;
```

### Interview Trick

> "BETWEEN সবসময় inclusive। DateTime এ `< '2022-01-01'` বেশি safe।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১৪ INNER JOIN

### সংজ্ঞা

**INNER JOIN** দুটো table এর **matching rows** return করে। Non-matching rows বাদ যায়।

### উদাহরণ

```sql
SELECT
    e.name       AS employee_name,
    e.salary,
    d.dept_name,
    d.location
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id;

-- তিনটি table
SELECT e.name, d.dept_name, p.project_name
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
INNER JOIN projects    p ON p.dept_id = d.dept_id;
```

### Interview Trick

> "`JOIN` লিখলেই INNER JOIN বোঝায়। কিন্তু explicit `INNER JOIN` লেখা readability বাড়ায়।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১৫ LEFT JOIN

### সংজ্ঞা

**LEFT JOIN** — বাম table এর **সব rows** return করে। ডান table এ match না থাকলে **NULL** আসে।

### উদাহরণ

```sql
-- সব employees (department না থাকলেও)
SELECT e.name, e.salary, d.dept_name
FROM employees e
LEFT JOIN departments d ON e.dept_id = d.dept_id;

-- Department নেই এমন employees
SELECT e.name
FROM employees e
LEFT JOIN departments d ON e.dept_id = d.dept_id
WHERE d.dept_id IS NULL;

-- প্রতিটি department এ কতজন (০ সহ)
SELECT d.dept_name, COUNT(e.emp_id) AS headcount
FROM departments d
LEFT JOIN employees e ON d.dept_id = e.dept_id
GROUP BY d.dept_id, d.dept_name;
```

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১৬ RIGHT JOIN

### সংজ্ঞা

**RIGHT JOIN** — ডান table এর **সব rows** return করে। বাম table এ match না থাকলে NULL।

### উদাহরণ

```sql
SELECT e.name, d.dept_name
FROM employees e
RIGHT JOIN departments d ON e.dept_id = d.dept_id;

-- সমতুল্য LEFT JOIN:
SELECT e.name, d.dept_name
FROM departments d
LEFT JOIN employees e ON d.dept_id = e.dept_id;
```

### Interview Trick

> "`A RIGHT JOIN B` = `B LEFT JOIN A` — Most developers LEFT JOIN prefer করেন।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১৭ FULL JOIN

### সংজ্ঞা

**FULL JOIN** — উভয় table এর **সব rows** return করে। MySQL এ সরাসরি নেই।

### উদাহরণ

```sql
-- PostgreSQL / SQL Server
SELECT e.name, d.dept_name
FROM employees e
FULL OUTER JOIN departments d ON e.dept_id = d.dept_id;

-- MySQL: LEFT UNION RIGHT
SELECT e.name, d.dept_name
FROM employees e LEFT JOIN departments d ON e.dept_id = d.dept_id
UNION
SELECT e.name, d.dept_name
FROM employees e RIGHT JOIN departments d ON e.dept_id = d.dept_id;
```

### Interview Trick

> "MySQL এ FULL OUTER JOIN নেই। `LEFT JOIN UNION RIGHT JOIN` দিয়ে simulate করতে হয়।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১৮ SELF JOIN

### সংজ্ঞা

**SELF JOIN** হলো একটি table কে **নিজের সাথেই join** করা। Hierarchical data এর জন্য ব্যবহৃত।

### উদাহরণ

```sql
-- প্রতিটি employee এবং তার manager
SELECT
    e.name AS employee,
    m.name AS manager
FROM employees e
LEFT JOIN employees m ON e.manager_id = m.emp_id
ORDER BY m.name;
```

### Interview Trick

> "SELF JOIN এ table একটাই কিন্তু alias দুটো (`e` এবং `m`) — SQL দুটো আলাদা table মনে করে।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১৯ UNION vs UNION ALL

### সংজ্ঞা

| Keyword | কাজ | Duplicate |
|---------|-----|----------|
| `UNION` | result একত্রিত | বাদ দেয় |
| `UNION ALL` | result একত্রিত | রাখে (দ্রুত) |

### নিয়ম

- একই সংখ্যক columns, compatible data type
- Column names first SELECT থেকে

### উদাহরণ

```sql
SELECT name, salary FROM employees WHERE dept_id = 1
UNION
SELECT name, salary FROM employees WHERE dept_id = 2;

SELECT name, salary FROM employees WHERE dept_id = 1
UNION ALL
SELECT name, salary FROM employees WHERE dept_id = 2
ORDER BY salary DESC;
```

### Interview-Style Explanation

**প্রশ্ন:** "UNION এবং UNION ALL এর পার্থক্য? কোনটি দ্রুত?"

**আদর্শ উত্তর:**
> "UNION duplicate বাদ দেয় — sorting/hashing করতে হয়, তাই slow। UNION ALL duplicate রাখে — check করে না, তাই দ্রুত। Duplicate থাকবে না জানা থাকলে UNION ALL ব্যবহার করুন।"

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.২০ Subquery ও Nested Query

### সংজ্ঞা

**Subquery** হলো একটি query এর **ভেতরে আরেকটি query**।

### ধরন

```
Subquery
├── Scalar    → single value
├── Column    → multiple rows, একটি column
├── Table     → derived table (FROM এ)
└── Correlated → outer এর প্রতিটি row এর জন্য inner চলে
```

### উদাহরণ

```sql
-- Scalar: সর্বোচ্চ salary এর employee
SELECT name, salary FROM employees
WHERE salary = (SELECT MAX(salary) FROM employees);

-- Column: Dhaka departments এর employees
SELECT name FROM employees
WHERE dept_id IN (
    SELECT dept_id FROM departments WHERE location = 'Dhaka'
);

-- Derived Table
SELECT dept_id, avg_salary
FROM (
    SELECT dept_id, AVG(salary) AS avg_salary
    FROM employees
    GROUP BY dept_id
) AS dept_avg
WHERE avg_salary > 60000;

-- Correlated: নিজের dept average এর বেশি salary
SELECT name, salary, dept_id
FROM employees e
WHERE salary > (
    SELECT AVG(salary) FROM employees WHERE dept_id = e.dept_id
);

-- EXISTS
SELECT dept_name FROM departments d
WHERE EXISTS (
    SELECT 1 FROM employees e WHERE e.dept_id = d.dept_id
);

-- NOT EXISTS
SELECT dept_name FROM departments d
WHERE NOT EXISTS (
    SELECT 1 FROM employees e WHERE e.dept_id = d.dept_id
);
```

### Subquery vs JOIN

| পরিস্থিতি | Subquery | JOIN |
|-----------|----------|------|
| Single value (MAX, MIN) | ভালো | awkward |
| Existence check | ভালো | possible |
| Multiple columns | কঠিন | ভালো |
| Performance | ধীর হতে পারে | সাধারণত দ্রুত |

### Common Mistakes

```sql
-- ❌ Scalar subquery তে multiple rows — error
SELECT name FROM employees
WHERE salary = (SELECT salary FROM employees WHERE dept_id = 1);

-- ✅ IN ব্যবহার করুন
SELECT name FROM employees
WHERE salary IN (SELECT salary FROM employees WHERE dept_id = 1);
```

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.২১ PART 2 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: INNER JOIN এবং LEFT JOIN এর পার্থক্য কী?**

> **উত্তর:** INNER JOIN শুধু matching rows return করে। LEFT JOIN বাম table এর সব rows return করে — ডান table এ match না থাকলে NULL দেয়। সব employees দেখাতে হলে (department না থাকলেও) LEFT JOIN দরকার।

---

**Q2: নিচের query কী return করবে?**

```sql
SELECT COUNT(*) FROM employees WHERE 1 = 0;
```

> **উত্তর:** `0` — `1 = 0` সবসময় FALSE, কোনো row match করে না। কিন্তু `COUNT(*)` সবসময় একটি row return করে।

---

**Q3: HAVING ছাড়া কি GROUP BY চলে?**

> **উত্তর:** হ্যাঁ। HAVING optional। তবে GROUP BY ছাড়া HAVING চলে না।

---

**Q4: Self Join কী? উদাহরণ দিন।**

> **উত্তর:** Self Join মানে একটি table নিজের সাথে join করা। Hierarchical data এর জন্য — `employees` table এ `manager_id` একই table এর `emp_id` reference করে। `SELECT e.name, m.name AS manager FROM employees e LEFT JOIN employees m ON e.manager_id = m.emp_id` — প্রতিটি employee ও তার manager এর নাম দেয়।

---

**Q5: `SELECT *` কেন bad practice?**

> **উত্তর:** (১) অপ্রয়োজনীয় data transfer, (২) নতুন column যোগ হলে application break হতে পারে, (৩) Covering Index এর সুবিধা নেওয়া যায় না।

---

### সেকশন ২: Practice Problems

```sql
-- Problem 1: সবচেয়ে বেশি employee আছে কোন department?
SELECT d.dept_name, COUNT(e.emp_id) AS total
FROM departments d
LEFT JOIN employees e ON d.dept_id = e.dept_id
GROUP BY d.dept_id, d.dept_name
ORDER BY total DESC
LIMIT 1;

-- Problem 2: নিজের department এর average এর বেশি salary
SELECT e.name, e.salary, e.dept_id
FROM employees e
WHERE e.salary > (
    SELECT AVG(salary) FROM employees WHERE dept_id = e.dept_id
);

-- Problem 3: কোনো project নেই এমন departments
SELECT d.dept_name
FROM departments d
WHERE d.dept_id NOT IN (
    SELECT DISTINCT dept_id FROM projects WHERE dept_id IS NOT NULL
);

-- Problem 4: ২০২২ এ join করা Engineering employees
SELECT e.name, e.salary, e.join_date
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
WHERE d.dept_name = 'Engineering'
  AND e.join_date BETWEEN '2022-01-01' AND '2022-12-31'
ORDER BY e.join_date;

-- Problem 5: প্রতিটি manager ও তার team size
SELECT
    m.name          AS manager,
    COUNT(e.emp_id) AS team_size
FROM employees e
INNER JOIN employees m ON e.manager_id = m.emp_id
GROUP BY m.emp_id, m.name
ORDER BY team_size DESC;
```

---

### সেকশন ৩: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| DML এর full form | Data Manipulation Language |
| DQL এর full form | Data Query Language |
| SELECT কোন language? | DQL |
| INSERT, UPDATE, DELETE কোন? | DML |
| JOIN এর default type | INNER JOIN |
| UNION ALL duplicate রাখে? | হ্যাঁ |
| GROUP BY ছাড়া HAVING চলে? | না |
| `LIMIT 5 OFFSET 10` মানে? | ১১তম থেকে ৫টি |
| LIKE এ wildcard কয়টি? | ২টি (`%` এবং `_`) |
| BETWEEN inclusive কি? | হ্যাঁ |
| NOT IN এ NULL থাকলে? | Empty result |
| Correlated subquery কী? | Outer row এর জন্য inner চলে |
| MySQL এ FULL JOIN আছে? | না — UNION দিয়ে simulate |
| `A RIGHT JOIN B` সমতুল্য? | `B LEFT JOIN A` |

---

> **⚠️ PART 2 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

*হ্যান্ডবুক তৈরিতে: Senior Database Engineer & Backend Architect*  
*Version: 1.0 | তারিখ: মে ২০২৬*  
*মোট PART: 9 | চলমান — PART 2 সম্পন্ন*

<a id="part3"></a>

# PART 3: Advanced SQL & Database Concepts (উন্নত ধারণাসমূহ)

> **📍 এই PART এর Sections:** [৩.১ Indexing](#৩১-indexing) · [৩.২ Clustered vs Non-clustered](#৩২-clustered-vs-non-clustered-index) · [৩.৩ Transactions](#৩৩-transactions) · [৩.৪ ACID](#৩৪-acid-properties)

> **ব্যবহারের নিয়ম:** এই PART টি Senior-level concepts ধারণ করে। Freshers যদি এগুলো জানেন, interview এ অনেক এগিয়ে থাকবেন। PART 2 এর `company_db` setup ব্যবহার করে examples practice করুন।

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১ Indexing

### সংজ্ঞা

**Index** হলো database এর একটি **data structure** যা table এর নির্দিষ্ট column(s) এর উপর তৈরি করা হয় যাতে query **দ্রুততর** হয়। Index ছাড়া database পুরো table scan করে (Full Table Scan) — Index থাকলে সরাসরি সঠিক location এ যায়।

### Real-Life Analogy

- **Index ছাড়া** = একটি বইয়ের প্রতিটি পৃষ্ঠা পড়ে "Database" শব্দ খোঁজা
- **Index সহ** = বইয়ের পেছনে Index দেখে সরাসরি সঠিক পৃষ্ঠায় যাওয়া

### Internal Working

MySQL এ Index সাধারণত **B-Tree (Balanced Tree)** data structure ব্যবহার করে:

```
B-Tree Index on salary:
               [60000]
              /       \
        [50000]       [75000]
        /    \        /    \
   [45000] [55000] [70000] [85000]

Search salary = 70000:
  Root → 70000 > 60000 → Right → 70000 < 75000 → Left → Found!
  Time: O(log n) — লক্ষ rows এও মাত্র ~20 step
```

### Index তৈরি ও ব্যবহার

```sql
-- Simple Index তৈরি
CREATE INDEX idx_salary ON employees(salary);

-- Unique Index
CREATE UNIQUE INDEX idx_email ON employees(email);

-- Composite Index (multiple columns)
CREATE INDEX idx_dept_salary ON employees(dept_id, salary);

-- Index দেখা
SHOW INDEX FROM employees;

-- Index মুছে ফেলা
DROP INDEX idx_salary ON employees;

-- Index এর সুবিধা পরীক্ষা
EXPLAIN SELECT * FROM employees WHERE salary > 60000;
-- key: idx_salary দেখালে Index ব্যবহার হচ্ছে
```

### কখন Index দেবেন

```
✅ Index দেওয়া উচিত:
  → WHERE clause এ বারবার ব্যবহৃত columns
  → JOIN এ ব্যবহৃত columns (FK columns)
  → ORDER BY তে ব্যবহৃত columns
  → UNIQUE constraint এর columns

❌ Index না দেওয়াই ভালো:
  → খুব ছোট table (< 1000 rows)
  → বারবার INSERT/UPDATE/DELETE হয় এমন table
  → Boolean বা low-cardinality columns (gender: M/F)
  → LIKE '%keyword%' এ index কাজ করে না
```

### Index এর Cost

```
┌──────────────────────────────────────────────────┐
│ Index এর Trade-off                               │
├──────────────────────────────────────────────────┤
│ সুবিধা: SELECT দ্রুত হয়                          │
│ অসুবিধা: INSERT/UPDATE/DELETE ধীর হয়             │
│          Extra disk space লাগে                   │
│ কারণ: প্রতিটি write operation এ index update হয় │
└──────────────────────────────────────────────────┘
```

### Interview-Style Explanation

**প্রশ্ন:** "Index কী? কীভাবে কাজ করে? কখন দেওয়া উচিত নয়?"

**আদর্শ উত্তর:**
> "Index হলো একটি data structure (সাধারণত B-Tree) যা নির্দিষ্ট column এর values সাজিয়ে রাখে যাতে query দ্রুত হয়। Index ছাড়া O(n) full scan, Index দিয়ে O(log n) search। তবে Index সবসময় ভালো নয় — প্রতিটি INSERT/UPDATE/DELETE এ Index ও update হয়, তাই write-heavy table এ Index performance কমায়। Low cardinality column এ (যেমন gender) Index দেওয়া waste।"

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.২ Clustered vs Non-clustered Index

### সংজ্ঞা

| বিষয় | Clustered Index | Non-clustered Index |
|------|----------------|---------------------|
| **সংখ্যা** | প্রতি table এ শুধু **১টি** | একাধিক হতে পারে |
| **Data storage** | Physical data Index order এ সাজানো থাকে | Separate structure, pointer দিয়ে আসল data তে যায় |
| **Speed** | Faster (data সরাসরি) | Slightly slower (extra lookup) |
| **Primary Key** | Automatically Clustered Index হয় | — |
| **উদাহরণ** | Phone book (নাম অনুযায়ী সাজানো) | বইয়ের পেছনের Index |

### Visual Comparison

```
Clustered Index (Primary Key: emp_id):
Table data physically sorted by emp_id:
  [1: Karim] [2: Rafi] [3: Sumi] [4: Tanvir] ...
  Data আর Index একসাথে

Non-clustered Index (salary):
Index structure (salary → row pointer):
  [45000 → row@offset_7]
  [50000 → row@offset_5]
  [55000 → row@offset_3]
  [60000 → row@offset_2]
  তারপর pointer follow করে actual data এ যাও
```

### SQL Example

```sql
-- MySQL এ PRIMARY KEY = Clustered Index (automatically)
CREATE TABLE employees (
    emp_id INT PRIMARY KEY,  -- এটিই Clustered Index
    name   VARCHAR(100),
    salary DECIMAL(10,2)
);

-- Non-clustered Index (additional)
CREATE INDEX idx_salary ON employees(salary);        -- Non-clustered
CREATE INDEX idx_name   ON employees(name);          -- Non-clustered

-- Covering Index: query তে দরকারি সব columns Index এ থাকলে
-- table এ যেতে হয় না (Index Only Scan)
CREATE INDEX idx_dept_sal ON employees(dept_id, salary);
-- এই query Covering Index ব্যবহার করবে:
SELECT dept_id, salary FROM employees WHERE dept_id = 1;
```

### Interview Trick

> "MySQL (InnoDB) এ Primary Key সবসময় Clustered Index। UUID বা random PK ব্যবহার করলে নতুন row insert এ B-Tree rebalance হয় — performance hit। Sequential INT বা BIGINT AUTO_INCREMENT best practice।"

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.৩ Transactions

### সংজ্ঞা

**Transaction** হলো একটি **logical unit of work** যা এক বা একাধিক SQL operations ধারণ করে। হয় সব operations সফলভাবে execute হবে (**COMMIT**), নাহয় কোনোটাই হবে না (**ROLLBACK**)।

### Real-Life Analogy

**Bank Transfer:** Karim এর account থেকে Rafi তে ৫,০০০ টাকা পাঠানো:

```
Transaction শুরু:
  Step 1: Karim এর balance - 5000
  Step 2: Rafi এর balance  + 5000

যদি Step 1 সফল কিন্তু Step 2 fail:
  → Transaction ROLLBACK → উভয় step বাতিল
  → Data consistent থাকে (টাকা হারায় না)
```

### Transaction Commands

| Command | কাজ |
|---------|-----|
| `BEGIN` / `START TRANSACTION` | Transaction শুরু |
| `COMMIT` | সব changes permanent করা |
| `ROLLBACK` | সব changes বাতিল করা |
| `SAVEPOINT name` | মাঝপথে checkpoint তৈরি |
| `ROLLBACK TO SAVEPOINT name` | নির্দিষ্ট checkpoint এ ফেরা |

### SQL Example

```sql
-- Bank Transfer Transaction
START TRANSACTION;

-- Step 1: Debit
UPDATE accounts
SET balance = balance - 5000
WHERE account_id = 1;  -- Karim

-- Step 2: Credit
UPDATE accounts
SET balance = balance + 5000
WHERE account_id = 2;  -- Rafi

-- দুটোই সফল হলে permanent করো
COMMIT;

-- যেকোনো একটি fail হলে সব বাতিল
-- ROLLBACK;

-- SAVEPOINT উদাহরণ
START TRANSACTION;
INSERT INTO orders (customer_id, total) VALUES (1, 5000);
SAVEPOINT after_order;

INSERT INTO order_items (order_id, product_id) VALUES (LAST_INSERT_ID(), 10);
-- এখানে error হলে
ROLLBACK TO SAVEPOINT after_order;  -- order insert রেখে item insert বাতিল
COMMIT;
```

### Autocommit

```sql
-- MySQL এ default autocommit = ON
-- প্রতিটি statement automatically commit হয়
SELECT @@autocommit;  -- 1 = ON

-- Autocommit বন্ধ করা
SET autocommit = 0;

-- এখন manually COMMIT বা ROLLBACK দিতে হবে
UPDATE employees SET salary = 90000 WHERE emp_id = 1;
COMMIT;  -- এখন permanent
```

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.৪ ACID Properties

### সংজ্ঞা

**ACID** হলো Transaction এর চারটি মূল বৈশিষ্ট্য যা data integrity নিশ্চিত করে:

```
┌─────────────────────────────────────────────────────────┐
│                    ACID Properties                       │
├──────────────────┬──────────────────────────────────────┤
│ A — Atomicity    │ সব অথবা কিছুই না                      │
│ C — Consistency  │ Valid state থেকে Valid state এ যায়   │
│ I — Isolation    │ Concurrent transactions আলাদা থাকে    │
│ D — Durability   │ Commit হলে permanently সংরক্ষিত       │
└──────────────────┴──────────────────────────────────────┘
```

### বিস্তারিত ব্যাখ্যা

#### A — Atomicity (অবিভাজ্যতা)

Transaction এর সব operations একটি **একক unit** — হয় সব হবে, নাহয় কিছুই হবে না।

```sql
-- Bank transfer: দুটো UPDATE — atomically ঘটতে হবে
START TRANSACTION;
UPDATE accounts SET balance = balance - 1000 WHERE id = 1;
UPDATE accounts SET balance = balance + 1000 WHERE id = 2;
COMMIT;
-- যদি ২য় UPDATE fail করে → ROLLBACK → ১ম UPDATE ও বাতিল
```

#### C — Consistency (সামঞ্জস্যতা)

Transaction সম্পন্ন হওয়ার পর database **valid state** এ থাকবে। সব constraints, rules পূরণ হবে।

```
Bank example:
  Before: Karim=10000, Rafi=5000 → Total=15000
  After transfer: Karim=5000, Rafi=10000 → Total=15000
  Total সবসময় same থাকে → Consistent
```

#### I — Isolation (বিচ্ছিন্নতা)

Concurrent transactions একে অপরের উপর **হস্তক্ষেপ করবে না**। প্রতিটি transaction যেন একা execute হচ্ছে এরকম মনে হবে।

```sql
-- Transaction A এবং B একসাথে চলছে
-- A: SELECT balance → 10000
-- B: UPDATE balance = balance - 5000
-- A: আবার SELECT → Isolation level অনুযায়ী 10000 বা 5000 দেখাতে পারে
```

#### D — Durability (স্থায়িত্ব)

COMMIT হওয়ার পর data **permanently stored** — server crash বা power failure হলেও data থাকবে।

```
COMMIT হওয়ার পর:
  → Data disk এ লেখা হয় (Write-Ahead Log / WAL)
  → Server restart হলেও data পাওয়া যাবে
```

### Interview-Style Explanation

**প্রশ্ন:** "ACID কী? Real-life উদাহরণ দিয়ে বোঝান।"

**আদর্শ উত্তর:**
> "ACID হলো Transaction এর চারটি property। Atomicity — bank transfer এ debit ও credit হয় অথবা কিছুই হয় না। Consistency — transfer এর আগে ও পরে মোট টাকা একই থাকে। Isolation — একসাথে দুজন একই account এ কাজ করলে একে অপরের operation দেখতে পায় না (isolation level অনুযায়ী)। Durability — payment confirm হওয়ার পর server বন্ধ হলেও transaction টি থাকে।"

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.৫ Isolation Levels

### সংজ্ঞা

**Isolation Level** নির্ধারণ করে concurrent transactions একে অপরের changes কতটুকু দেখতে পাবে।

### Concurrency Problems

| সমস্যা | বিবরণ |
|--------|-------|
| **Dirty Read** | Transaction A uncommitted data পড়ে, পরে A ROLLBACK করলে পড়া data invalid |
| **Non-Repeatable Read** | Transaction A একই row দুইবার পড়ে, মাঝে B update করে — দুইবার আলাদা result |
| **Phantom Read** | Transaction A একটি query চালায়, B নতুন row insert করে, A আবার চালালে নতুন row দেখায় |

### Isolation Levels তুলনা

| Isolation Level | Dirty Read | Non-Repeatable Read | Phantom Read | Performance |
|----------------|-----------|---------------------|-------------|------------|
| **READ UNCOMMITTED** | ✅ হয় | ✅ হয় | ✅ হয় | সবচেয়ে দ্রুত |
| **READ COMMITTED** | ❌ হয় না | ✅ হয় | ✅ হয় | দ্রুত |
| **REPEATABLE READ** | ❌ হয় না | ❌ হয় না | ✅ হয় (MySQL তে না) | মধ্যম |
| **SERIALIZABLE** | ❌ হয় না | ❌ হয় না | ❌ হয় না | সবচেয়ে ধীর |

> **MySQL (InnoDB) এর default: REPEATABLE READ**

### SQL Example

```sql
-- Current isolation level দেখা
SELECT @@transaction_isolation;

-- Isolation level পরিবর্তন
SET SESSION TRANSACTION ISOLATION LEVEL READ COMMITTED;
SET SESSION TRANSACTION ISOLATION LEVEL REPEATABLE READ;
SET SESSION TRANSACTION ISOLATION LEVEL SERIALIZABLE;

-- Transaction A (Terminal 1)
START TRANSACTION;
SELECT salary FROM employees WHERE emp_id = 1;  -- 85000

-- Transaction B (Terminal 2) — একই সময়ে
UPDATE employees SET salary = 90000 WHERE emp_id = 1;
COMMIT;

-- Transaction A আবার পড়ে:
-- READ COMMITTED: 90000 দেখাবে (Non-Repeatable Read!)
-- REPEATABLE READ: 85000 দেখাবে (consistent snapshot)
SELECT salary FROM employees WHERE emp_id = 1;
COMMIT;
```

### Interview Trick

> "বাংলাদেশের interview এ সাধারণত Isolation Level এর নাম ও Dirty/Non-Repeatable/Phantom Read এর definition জিজ্ঞেস করা হয়। MySQL এর default REPEATABLE READ মনে রাখুন।"

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.৬ Deadlock

### সংজ্ঞা

**Deadlock** হলো এমন পরিস্থিতি যেখানে দুটি বা তার বেশি transaction একে অপরের **lock release এর জন্য অপেক্ষা** করছে — ফলে কেউই এগোতে পারছে না।

### Visual Representation

```
Transaction A                    Transaction B
──────────────                   ──────────────
Lock Row 1 (Karim) ✅            Lock Row 2 (Rafi) ✅
Wait for Row 2... ⏳             Wait for Row 1... ⏳
       ↑                                ↓
       └────────── DEADLOCK ────────────┘
       উভয়ই wait করছে, কেউই এগোতে পারছে না
```

### Real-Life Example

```sql
-- Transaction A:
START TRANSACTION;
UPDATE accounts SET balance = balance - 1000 WHERE id = 1; -- Lock Row 1
-- এখন Row 2 এর জন্য wait করছে...
UPDATE accounts SET balance = balance + 1000 WHERE id = 2;

-- Transaction B (একই সময়ে):
START TRANSACTION;
UPDATE accounts SET balance = balance - 500 WHERE id = 2;  -- Lock Row 2
-- এখন Row 1 এর জন্য wait করছে...
UPDATE accounts SET balance = balance + 500 WHERE id = 1;

-- DEADLOCK! MySQL automatically একটি transaction ROLLBACK করে দেয়
-- ERROR 1213: Deadlock found when trying to get lock
```

### Deadlock Prevention

```sql
-- 1. সবসময় একই order এ rows lock করুন
-- A এবং B উভয়ই id=1 তারপর id=2 lock করলে deadlock হবে না

-- 2. Transaction ছোট রাখুন (কম lock, কম সময়)

-- 3. SELECT ... FOR UPDATE — explicitly lock করুন
START TRANSACTION;
SELECT * FROM accounts WHERE id = 1 FOR UPDATE;  -- explicit lock
UPDATE accounts SET balance = balance - 1000 WHERE id = 1;
COMMIT;

-- 4. Lock Timeout সেট করুন
SET innodb_lock_wait_timeout = 5;  -- ৫ সেকেন্ড পর timeout
```

### Interview-Style Explanation

**প্রশ্ন:** "Deadlock কী? কীভাবে prevent করবেন?"

**আদর্শ উত্তর:**
> "Deadlock হলো circular wait — Transaction A, B এর lock এর জন্য wait, B, A এর lock এর জন্য wait। কেউই এগোতে পারে না। MySQL automatically victim transaction ROLLBACK করে deadlock resolve করে। Prevention এর জন্য — সবসময় same order এ rows lock করুন, transaction ছোট রাখুন, lock timeout সেট করুন।"

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.৭ Views

### সংজ্ঞা

**View** হলো একটি **virtual table** যা একটি stored SELECT query থেকে তৈরি হয়। View এ actual data store হয় না — প্রতিবার query করলে underlying table থেকে data আনে।

### View এর সুবিধা

```
┌──────────────────────────────────────────────────────┐
│ View এর সুবিধা                                       │
├──────────────────────────────────────────────────────┤
│ 1. Security: sensitive columns লুকানো যায়           │
│ 2. Simplicity: complex query কে simple view বানানো  │
│ 3. Reusability: বারবার একই query লিখতে হয় না       │
│ 4. Abstraction: underlying table structure লুকানো   │
└──────────────────────────────────────────────────────┘
```

### SQL Example

```sql
-- Simple View তৈরি
CREATE VIEW engineering_employees AS
SELECT e.emp_id, e.name, e.salary, e.join_date
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
WHERE d.dept_name = 'Engineering';

-- View ব্যবহার (সাধারণ table এর মতো)
SELECT * FROM engineering_employees;
SELECT name, salary FROM engineering_employees WHERE salary > 70000;

-- Security View: salary লুকিয়ে রাখা
CREATE VIEW public_employees AS
SELECT emp_id, name, email, dept_id
FROM employees;
-- এই view দিয়ে salary দেখা যাবে না

-- Updatable View (simple view এ UPDATE করা যায়)
UPDATE engineering_employees
SET salary = 70000
WHERE emp_id = 2;

-- View দেখা
SHOW FULL TABLES WHERE Table_type = 'VIEW';

-- View মুছে ফেলা
DROP VIEW IF EXISTS engineering_employees;

-- View definition দেখা
SHOW CREATE VIEW engineering_employees;
```

### View vs Table

| বিষয় | View | Table |
|------|------|-------|
| Data store হয়? | ❌ না (virtual) | ✅ হ্যাঁ |
| Performance | Slightly slower | Faster |
| Update করা যায়? | Simple view তে হ্যাঁ | সবসময় হ্যাঁ |
| Index দেওয়া যায়? | না (Materialized View ছাড়া) | হ্যাঁ |

### Materialized View

> **Materialized View** হলো View এর cached version যেখানে data physically stored থাকে। MySQL এ নেই, PostgreSQL এ আছে। Performance ভালো কিন্তু data stale হতে পারে।

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.৮ Stored Procedure

### সংজ্ঞা

**Stored Procedure** হলো database এ সংরক্ষিত **pre-compiled SQL statements এর সমষ্টি** যা একটি নামে call করা যায়। এটি database এর function এর মতো।

### Stored Procedure এর সুবিধা

- **Performance:** Pre-compiled, বারবার compile করতে হয় না
- **Security:** Table এ direct access না দিয়ে procedure দিয়ে access দেওয়া
- **Code Reuse:** একবার লিখলে বারবার call করা যায়
- **Network:** Multiple query এর বদলে একটি call — network traffic কমে

### SQL Example

```sql
-- Simple Stored Procedure
DELIMITER //
CREATE PROCEDURE GetEmployeesByDept(IN dept_name VARCHAR(100))
BEGIN
    SELECT e.name, e.salary, e.email
    FROM employees e
    INNER JOIN departments d ON e.dept_id = d.dept_id
    WHERE d.dept_name = dept_name
    ORDER BY e.salary DESC;
END //
DELIMITER ;

-- Call করা
CALL GetEmployeesByDept('Engineering');
CALL GetEmployeesByDept('Marketing');

-- OUT parameter সহ
DELIMITER //
CREATE PROCEDURE GetDeptStats(
    IN  p_dept_id  INT,
    OUT p_count    INT,
    OUT p_avg_sal  DECIMAL(10,2)
)
BEGIN
    SELECT COUNT(*), AVG(salary)
    INTO p_count, p_avg_sal
    FROM employees
    WHERE dept_id = p_dept_id;
END //
DELIMITER ;

-- Call করা
CALL GetDeptStats(1, @count, @avg_sal);
SELECT @count AS employee_count, @avg_sal AS average_salary;

-- Salary বাড়ানোর Procedure (Business Logic)
DELIMITER //
CREATE PROCEDURE GiveSalaryRaise(
    IN  p_dept_id    INT,
    IN  p_percentage DECIMAL(5,2)
)
BEGIN
    DECLARE v_dept_name VARCHAR(100);

    -- Validation
    IF p_percentage <= 0 OR p_percentage > 50 THEN
        SIGNAL SQLSTATE '45000'
        SET MESSAGE_TEXT = 'Raise percentage must be between 0 and 50';
    END IF;

    SELECT dept_name INTO v_dept_name
    FROM departments WHERE dept_id = p_dept_id;

    UPDATE employees
    SET salary = salary * (1 + p_percentage / 100)
    WHERE dept_id = p_dept_id;

    SELECT CONCAT(v_dept_name, ' department: ', ROW_COUNT(), ' employees updated') AS result;
END //
DELIMITER ;

CALL GiveSalaryRaise(1, 10);  -- Engineering এ ১০% raise

-- Procedure দেখা ও মুছে ফেলা
SHOW PROCEDURE STATUS WHERE Db = 'company_db';
DROP PROCEDURE IF EXISTS GetEmployeesByDept;
```

### Common Mistakes

- ❌ Complex business logic সব stored procedure এ রাখা — maintainability কঠিন
- ✅ Simple, reusable operation এর জন্য stored procedure ভালো
- ❌ Stored procedure কে application-level validation এর বিকল্প ভাবা

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.৯ Trigger

### সংজ্ঞা

**Trigger** হলো database এ একটি **automatic action** যা নির্দিষ্ট event (INSERT, UPDATE, DELETE) এর আগে বা পরে **automatically execute** হয়।

### Trigger এর ধরন

| Timing | Event | উদাহরণ |
|--------|-------|--------|
| **BEFORE INSERT** | Insert এর আগে | Data validation |
| **AFTER INSERT** | Insert এর পরে | Audit log লেখা |
| **BEFORE UPDATE** | Update এর আগে | Old value সংরক্ষণ |
| **AFTER UPDATE** | Update এর পরে | Cache invalidate |
| **BEFORE DELETE** | Delete এর আগে | Soft delete |
| **AFTER DELETE** | Delete এর পরে | Cleanup |

### SQL Example

```sql
-- Audit Log Table
CREATE TABLE salary_audit (
    audit_id    INT          PRIMARY KEY AUTO_INCREMENT,
    emp_id      INT,
    old_salary  DECIMAL(10,2),
    new_salary  DECIMAL(10,2),
    changed_at  DATETIME     DEFAULT CURRENT_TIMESTAMP,
    changed_by  VARCHAR(100) DEFAULT USER()
);

-- AFTER UPDATE Trigger: salary পরিবর্তন হলে audit log লেখো
DELIMITER //
CREATE TRIGGER trg_salary_audit
AFTER UPDATE ON employees
FOR EACH ROW
BEGIN
    IF OLD.salary <> NEW.salary THEN
        INSERT INTO salary_audit (emp_id, old_salary, new_salary)
        VALUES (OLD.emp_id, OLD.salary, NEW.salary);
    END IF;
END //
DELIMITER ;

-- Test করা
UPDATE employees SET salary = 95000 WHERE emp_id = 1;
SELECT * FROM salary_audit;

-- BEFORE INSERT Trigger: email lowercase করা
DELIMITER //
CREATE TRIGGER trg_normalize_email
BEFORE INSERT ON employees
FOR EACH ROW
BEGIN
    SET NEW.email = LOWER(TRIM(NEW.email));
END //
DELIMITER ;

-- BEFORE DELETE Trigger: soft delete (আসলে delete না করে flag)
CREATE TABLE employees_deleted (
    emp_id     INT,
    name       VARCHAR(100),
    deleted_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

DELIMITER //
CREATE TRIGGER trg_soft_delete
BEFORE DELETE ON employees
FOR EACH ROW
BEGIN
    INSERT INTO employees_deleted (emp_id, name)
    VALUES (OLD.emp_id, OLD.name);
END //
DELIMITER ;

-- Trigger দেখা ও মুছে ফেলা
SHOW TRIGGERS FROM company_db;
DROP TRIGGER IF EXISTS trg_salary_audit;
```

### Trigger এর সতর্কতা

```
⚠️ Trigger এর সমস্যা:
  → Invisible side effects — UPDATE করলে কোথায় কী হচ্ছে বোঝা কঠিন
  → Performance overhead — প্রতিটি DML এ trigger চলে
  → Debug করা কঠিন
  → Cascading triggers (trigger থেকে trigger) বিপজ্জনক

✅ Trigger কখন ব্যবহার করবেন:
  → Audit logging
  → Data normalization
  → Derived column update (denormalization)
  → Referential integrity (FK দিয়ে সম্ভব নয় এমন)
```

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১০ Cursor

### সংজ্ঞা

**Cursor** হলো একটি database object যা **result set এর rows একটি একটি করে** process করতে দেয়। Set-based operation সম্ভব না হলে cursor ব্যবহার করা হয়।

### Cursor এর ধাপ

```
১. DECLARE   → Cursor declare করো
২. OPEN      → Query execute করো, result set তৈরি করো
৩. FETCH     → একটি row নিয়ে এসো
৪. CLOSE     → Cursor বন্ধ করো
```

### SQL Example

```sql
DELIMITER //
CREATE PROCEDURE ProcessSalaryRaises()
BEGIN
    DECLARE v_emp_id    INT;
    DECLARE v_salary    DECIMAL(10,2);
    DECLARE v_done      BOOLEAN DEFAULT FALSE;

    -- Cursor declare
    DECLARE emp_cursor CURSOR FOR
        SELECT emp_id, salary FROM employees WHERE dept_id = 1;

    -- No more rows handler
    DECLARE CONTINUE HANDLER FOR NOT FOUND SET v_done = TRUE;

    OPEN emp_cursor;

    emp_loop: LOOP
        FETCH emp_cursor INTO v_emp_id, v_salary;

        IF v_done THEN
            LEAVE emp_loop;
        END IF;

        -- Business logic: salary এর ভিত্তিতে raise
        IF v_salary < 60000 THEN
            UPDATE employees SET salary = v_salary * 1.15 WHERE emp_id = v_emp_id;
        ELSEIF v_salary < 75000 THEN
            UPDATE employees SET salary = v_salary * 1.10 WHERE emp_id = v_emp_id;
        ELSE
            UPDATE employees SET salary = v_salary * 1.05 WHERE emp_id = v_emp_id;
        END IF;
    END LOOP;

    CLOSE emp_cursor;
END //
DELIMITER ;
```

### Interview Trick

> "Cursor সাধারণত **avoid** করা উচিত — row-by-row processing SET-based SQL এর চেয়ে অনেক ধীর। বেশিরভাগ cursor logic একটি single UPDATE বা INSERT...SELECT দিয়ে করা যায়। Cursor শুধু যখন row-by-row logic unavoidable তখন ব্যবহার করুন।"

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১১ Functions (User-Defined)

### সংজ্ঞা

**User-Defined Function (UDF)** হলো Stored Procedure এর মতো কিন্তু একটি **single value return** করে এবং SELECT এ সরাসরি ব্যবহার করা যায়।

### Function vs Stored Procedure

| বিষয় | Function | Stored Procedure |
|------|----------|-----------------|
| Return | একটি value | Multiple result sets |
| SELECT এ ব্যবহার | ✅ হ্যাঁ | ❌ না |
| DML (INSERT/UPDATE) | ❌ না (MySQL তে) | ✅ হ্যাঁ |
| Transaction | ❌ না | ✅ হ্যাঁ |

### SQL Example

```sql
-- Salary grade return করে এমন Function
DELIMITER //
CREATE FUNCTION GetSalaryGrade(p_salary DECIMAL(10,2))
RETURNS VARCHAR(20)
DETERMINISTIC
BEGIN
    DECLARE v_grade VARCHAR(20);

    IF p_salary >= 80000 THEN
        SET v_grade = 'Senior';
    ELSEIF p_salary >= 60000 THEN
        SET v_grade = 'Mid-level';
    ELSEIF p_salary >= 40000 THEN
        SET v_grade = 'Junior';
    ELSE
        SET v_grade = 'Intern';
    END IF;

    RETURN v_grade;
END //
DELIMITER ;

-- SELECT এ সরাসরি ব্যবহার
SELECT name, salary, GetSalaryGrade(salary) AS grade
FROM employees
ORDER BY salary DESC;

-- Tax calculation function
DELIMITER //
CREATE FUNCTION CalculateTax(p_salary DECIMAL(10,2))
RETURNS DECIMAL(10,2)
DETERMINISTIC
BEGIN
    DECLARE v_tax DECIMAL(10,2);

    IF p_salary > 80000 THEN
        SET v_tax = p_salary * 0.25;
    ELSEIF p_salary > 50000 THEN
        SET v_tax = p_salary * 0.15;
    ELSE
        SET v_tax = 0;
    END IF;

    RETURN v_tax;
END //
DELIMITER ;

SELECT name,
       salary,
       CalculateTax(salary) AS monthly_tax,
       salary - CalculateTax(salary) AS net_salary
FROM employees;

-- Function মুছে ফেলা
DROP FUNCTION IF EXISTS GetSalaryGrade;
```

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১২ Query Optimization

### সংজ্ঞা

**Query Optimization** হলো SQL query কে **দ্রুততর এবং কম resource-consuming** করার প্রক্রিয়া।

### Optimization Techniques

#### ১. Index ব্যবহার করুন

```sql
-- ❌ Slow: WHERE এ function ব্যবহার — index কাজ করে না
SELECT * FROM employees WHERE YEAR(join_date) = 2022;

-- ✅ Fast: Range condition — index ব্যবহার হয়
SELECT * FROM employees
WHERE join_date BETWEEN '2022-01-01' AND '2022-12-31';

-- ❌ Slow: Leading wildcard — full scan
SELECT * FROM employees WHERE name LIKE '%Hasan';

-- ✅ Better: Trailing wildcard — index ব্যবহার হয়
SELECT * FROM employees WHERE name LIKE 'Hasan%';
```

#### ২. SELECT * এড়ানো

```sql
-- ❌ সব columns — বেশি data transfer
SELECT * FROM employees WHERE dept_id = 1;

-- ✅ শুধু দরকারি columns
SELECT emp_id, name, salary FROM employees WHERE dept_id = 1;
```

#### ৩. Subquery এর বদলে JOIN

```sql
-- ❌ Correlated Subquery — প্রতিটি row এ inner query চলে
SELECT name FROM employees e
WHERE dept_id = (SELECT dept_id FROM departments WHERE dept_name = 'Engineering');

-- ✅ JOIN — একবারে
SELECT e.name
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
WHERE d.dept_name = 'Engineering';
```

#### ৪. LIMIT ব্যবহার করুন

```sql
-- Testing বা paging এ LIMIT দিন
SELECT * FROM employees ORDER BY salary DESC LIMIT 10;
```

#### ৫. NOT IN এর বদলে NOT EXISTS

```sql
-- ❌ NOT IN: NULL সমস্যা ও slow
SELECT name FROM employees
WHERE dept_id NOT IN (SELECT dept_id FROM departments);

-- ✅ NOT EXISTS: সাধারণত দ্রুত
SELECT name FROM employees e
WHERE NOT EXISTS (
    SELECT 1 FROM departments d WHERE d.dept_id = e.dept_id
);
```

#### ৬. OR এর বদলে IN বা UNION

```sql
-- ❌ Multiple OR
SELECT * FROM employees WHERE dept_id = 1 OR dept_id = 2 OR dept_id = 3;

-- ✅ IN — cleaner, often faster
SELECT * FROM employees WHERE dept_id IN (1, 2, 3);
```

### Optimization Tips Summary

```
┌─────────────────────────────────────────────────────────┐
│ Query Optimization — মনে রাখার নিয়ম                    │
├─────────────────────────────────────────────────────────┤
│ → WHERE clause এ Index column ব্যবহার করুন             │
│ → Function দিয়ে Index column wrap করবেন না             │
│ → SELECT * এড়িয়ে specific columns লিখুন               │
│ → JOIN, UNION ALL, IN prefer করুন                      │
│ → LIMIT দিন যেখানে সম্ভব                               │
│ → EXPLAIN দিয়ে query plan দেখুন                        │
│ → Covering Index ব্যবহার করুন                          │
└─────────────────────────────────────────────────────────┘
```

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১৩ Query Execution Plan

### সংজ্ঞা

**EXPLAIN** statement দিয়ে MySQL দেখায় কীভাবে একটি query execute হবে — কোন index ব্যবহার হচ্ছে, কতটি rows scan হবে, join order কী।

### EXPLAIN Output

```sql
EXPLAIN SELECT e.name, d.dept_name
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
WHERE e.salary > 60000;
```

| Column | মানে |
|--------|------|
| `id` | Query এর ধাপ |
| `select_type` | SIMPLE, SUBQUERY, JOIN |
| `table` | কোন table |
| `type` | Access type (ALL, index, range, ref, const) |
| `key` | ব্যবহৃত index |
| `rows` | Estimated rows scanned |
| `Extra` | Using index, Using where, Using filesort |

### Access Type (ভালো → খারাপ)

```
const   → Primary Key বা Unique এ single row (সবচেয়ে ভালো)
eq_ref  → JOIN এ unique/PK match
ref     → Non-unique index
range   → BETWEEN, >, < এ index range
index   → Full index scan
ALL     → Full table scan (সবচেয়ে খারাপ)
```

### উদাহরণ

```sql
-- Index নেই — ALL (খারাপ)
EXPLAIN SELECT * FROM employees WHERE salary > 60000;
-- type: ALL, rows: 8 (সব rows scan)

-- Index যোগ করার পর
CREATE INDEX idx_salary ON employees(salary);
EXPLAIN SELECT * FROM employees WHERE salary > 60000;
-- type: range, key: idx_salary, rows: 4 (কম scan)

-- EXPLAIN ANALYZE (MySQL 8.0+) — actual execution data
EXPLAIN ANALYZE SELECT * FROM employees WHERE dept_id = 1;
```

### Interview Trick

> "EXPLAIN এ `type: ALL` দেখলে সেটি full table scan — সমস্যার লক্ষণ। Index যোগ করুন বা query rewrite করুন। `rows` column এর value কম হওয়া ভালো।"

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১৪ Partitioning

### সংজ্ঞা

**Partitioning** হলো একটি বড় table কে **physically আলাদা ছোট অংশে** ভাগ করা — logically এটি একটি table থাকে, কিন্তু data আলাদা আলাদা partition এ store হয়।

### Partitioning এর ধরন

| ধরন | কীভাবে | উদাহরণ |
|-----|--------|--------|
| **RANGE** | Value range অনুযায়ী | join_date অনুযায়ী বছর ভেদে |
| **LIST** | নির্দিষ্ট values | dept_id = 1, 2, 3 |
| **HASH** | Hash function | emp_id % 4 |
| **KEY** | MySQL internal hash | Auto |

### SQL Example

```sql
-- RANGE Partitioning: বছর অনুযায়ী
CREATE TABLE orders (
    order_id   INT          NOT NULL,
    customer_id INT         NOT NULL,
    order_date  DATE        NOT NULL,
    total      DECIMAL(10,2),
    PRIMARY KEY (order_id, order_date)
)
PARTITION BY RANGE (YEAR(order_date)) (
    PARTITION p2022 VALUES LESS THAN (2023),
    PARTITION p2023 VALUES LESS THAN (2024),
    PARTITION p2024 VALUES LESS THAN (2025),
    PARTITION p2025 VALUES LESS THAN (2026),
    PARTITION pmax  VALUES LESS THAN MAXVALUE
);

-- 2023 সালের orders শুধু p2023 partition scan করবে — দ্রুত!
SELECT * FROM orders WHERE order_date BETWEEN '2023-01-01' AND '2023-12-31';

-- Partition দেখা
SELECT PARTITION_NAME, TABLE_ROWS
FROM information_schema.PARTITIONS
WHERE TABLE_NAME = 'orders';

-- পুরানো partition drop করা (data purge — খুব দ্রুত)
ALTER TABLE orders DROP PARTITION p2022;
```

### Partitioning এর সুবিধা

- **Query performance:** শুধু relevant partition scan করে (**Partition Pruning**)
- **Maintenance:** পুরানো partition সহজে drop করা যায়
- **Parallel processing:** আলাদা partition parallel process হতে পারে

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১৫ Sharding

### সংজ্ঞা

**Sharding** হলো database কে **আলাদা servers এ** horizontal ভাবে ভাগ করা। Partitioning একটি server এ, Sharding **multiple servers** এ।

### Sharding vs Partitioning

| বিষয় | Partitioning | Sharding |
|------|-------------|---------|
| Location | একই server | আলাদা servers |
| Scale | Vertical scaling | Horizontal scaling |
| Complexity | কম | বেশি |
| Use case | Medium data | Very large data (TB+) |

### Sharding Strategy

```
Sharding by user_id:
  User 1-1M    → Shard 1 (Server A)
  User 1M-2M   → Shard 2 (Server B)
  User 2M-3M   → Shard 3 (Server C)

Shard Key: user_id
  user_id % 3 = 0 → Server A
  user_id % 3 = 1 → Server B
  user_id % 3 = 2 → Server C
```

### Sharding এর চ্যালেঞ্জ

```
⚠️ Sharding এর সমস্যা:
  → Cross-shard JOIN কঠিন বা অসম্ভব
  → Rebalancing কঠিন (hotspot shard)
  → Transaction across shards — distributed transaction দরকার
  → Application layer জটিল হয়

✅ কখন Sharding করবেন:
  → Single server এর storage/performance limit ছাড়িয়ে গেলে
  → Read/Write throughput অনেক বেশি হলে
  → Facebook, Twitter, Pathao scale এ
```

### Interview Trick

> "Junior level interview এ Sharding এর concept জানলেই যথেষ্ট। Real implementation খুব complex। বলুন: Sharding হলো data horizontally multiple servers এ distribute করা। Shard key এর choice critical — hotspot avoid করতে হবে।"

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১৬ Replication

### সংজ্ঞা

**Replication** হলো এক database server এর data **অন্য server(s) এ automatically copy** করা। এতে High Availability এবং Read Scalability নিশ্চিত হয়।

### Replication Types

```
Master-Slave (Primary-Replica) Replication:
  ┌──────────────┐
  │   Master DB  │ ← Writes (INSERT, UPDATE, DELETE)
  │  (Primary)   │
  └──────┬───────┘
         │ Binary Log (changes replicate)
    ┌────┴────────────┐
    ↓                 ↓
┌─────────┐       ┌─────────┐
│ Slave 1 │       │ Slave 2 │
│(Replica)│       │(Replica)│
└─────────┘       └─────────┘
     ↑ Reads only        ↑ Reads only
```

### Replication এর সুবিধা

| সুবিধা | ব্যাখ্যা |
|--------|---------|
| **High Availability** | Master fail হলে Slave promote হয় |
| **Read Scalability** | Read queries Slave থেকে serve করা যায় |
| **Backup** | Slave থেকে backup নিলে Master affected হয় না |
| **Geographical distribution** | Different regions এ Slave রাখা |

### Replication Lag

```sql
-- Slave এ replication lag দেখা
SHOW SLAVE STATUS\G
-- Seconds_Behind_Master: 0 = কোনো lag নেই
-- Seconds_Behind_Master: 5 = ৫ সেকেন্ড পিছিয়ে
```

### Synchronous vs Asynchronous Replication

| ধরন | মানে | Trade-off |
|-----|------|----------|
| **Asynchronous** (default) | Master commit করে, পরে Slave কে replicate করে | দ্রুত, কিন্তু Slave পিছিয়ে থাকতে পারে |
| **Synchronous** | Master wait করে Slave confirm না আসা পর্যন্ত | Slow, কিন্তু কোনো data loss নেই |
| **Semi-synchronous** | অন্তত একটি Slave confirm করলে commit | Balance |

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১৭ PART 3 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: Index কী? Index কি সবসময় performance বাড়ায়?**

> **উত্তর:** Index হলো B-Tree data structure যা query দ্রুত করে। না — Index সবসময় performance বাড়ায় না। Read query দ্রুত করে কিন্তু প্রতিটি INSERT/UPDATE/DELETE এ Index ও update হয় — write-heavy table এ Index overhead তৈরি করে। Low-cardinality column এ (gender: M/F) Index অর্থহীন। Composite Index এ column order গুরুত্বপূর্ণ।

---

**Q2: ACID এর প্রতিটি property উদাহরণসহ বোঝান।**

> **উত্তর:** Bank transfer উদাহরণে — **Atomicity:** Karim থেকে debit ও Rafi তে credit একসাথে হবে নাহয় কোনোটাই নয়। **Consistency:** Transfer এর আগে ও পরে মোট balance একই থাকবে। **Isolation:** আরেকটি transaction Karim এর balance পরিবর্তন হওয়া দেখবে না যতক্ষণ না আমাদের transaction commit হয়। **Durability:** Commit হওয়ার পর server crash হলেও transaction টি থাকবে।

---

**Q3: Deadlock কীভাবে হয়? কীভাবে সমাধান করবেন?**

> **উত্তর:** Transaction A, Row 1 lock করে Row 2 এর জন্য wait করছে। Transaction B, Row 2 lock করে Row 1 এর জন্য wait করছে — circular dependency। MySQL automatically victim transaction ROLLBACK করে। Prevention: একই order এ rows lock করুন, transaction ছোট রাখুন, innodb_lock_wait_timeout সেট করুন।

---

**Q4: View কী? Materialized View এর সাথে পার্থক্য?**

> **উত্তর:** View হলো stored SELECT query থেকে তৈরি virtual table — data physically store হয় না, query করলে underlying table থেকে আনে। Materialized View হলো View এর cached version — data physically stored, তাই দ্রুত কিন্তু stale হতে পারে। MySQL এ Materialized View নেই, PostgreSQL এ আছে।

---

**Q5: Stored Procedure এবং Function এর মধ্যে পার্থক্য?**

> **উত্তর:** Function একটি single value return করে এবং SELECT এ ব্যবহার করা যায়, DML করতে পারে না। Stored Procedure multiple result sets return করতে পারে, DML করতে পারে, Transaction handle করতে পারে, কিন্তু SELECT এ সরাসরি ব্যবহার করা যায় না।

---

**Q6: Sharding এবং Partitioning এর পার্থক্য কী?**

> **উত্তর:** Partitioning হলো একটি table কে physically একই server এ ছোট অংশে ভাগ করা। Sharding হলো data multiple servers এ distribute করা — horizontal scaling। Partitioning medium scale এ ভালো, Sharding million users scale এ দরকার। Sharding cross-shard JOIN কঠিন করে তোলে।

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| MySQL এর default index structure | B-Tree |
| Clustered Index কয়টি থাকতে পারে? | শুধু ১টি |
| MySQL এর default isolation level | REPEATABLE READ |
| Dirty Read কোন isolation level এ হয়? | READ UNCOMMITTED |
| COMMIT না করলে কী হয়? | Autocommit ON হলে auto commit, নাহলে ROLLBACK |
| Trigger কি Transaction এ rollback হয়? | হ্যাঁ |
| Cursor কি set-based SQL এর চেয়ে দ্রুত? | না, ধীর |
| EXPLAIN এ `type: ALL` মানে? | Full table scan |
| Partitioning ও Sharding এর পার্থক্য? | Same server vs multiple servers |
| Replication lag কী? | Master ও Slave এর data এর সময়ের পার্থক্য |
| Read Replica কীসের জন্য? | Read scalability ও backup |
| Materialized View কোন DB তে আছে? | PostgreSQL (MySQL তে নেই) |
| SAVEPOINT কী? | Transaction এর মধ্যে checkpoint |
| `SELECT ... FOR UPDATE` কী করে? | Row explicitly lock করে |

---

> **⚠️ PART 3 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

*হ্যান্ডবুক তৈরিতে: Senior Database Engineer & Backend Architect*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 9 | চলমান — PART 3 সম্পন্ন*


<a id="part4"></a>

# PART 4: Normalization & Database Design (ডেটাবেজ ডিজাইন)

> **📍 এই PART এর Sections:** [৪.১ Normalization কী?](#৪১-normalization-কী) · [৪.২ 1NF](#৪২-1nf--first-normal-form) · [৪.৩ 2NF](#৪৩-2nf--second-normal-form) · [৪.৪ 3NF](#৪৪-3nf--third-normal-form)

> **ব্যবহারের নিয়ম:** এই PART টি Database Design এর মূল ভিত্তি। Interview এ প্রায়ই Normalization এর step-by-step process এবং ER Diagram থেকে Schema তৈরি জিজ্ঞেস করা হয়। প্রতিটি Normal Form উদাহরণসহ বুঝুন।

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.১ Normalization কী?

### সংজ্ঞা

**Normalization** হলো relational database design এর একটি প্রক্রিয়া যেখানে table কে systematic ভাবে organize করা হয় যাতে:

- **Data Redundancy** (একই data বারবার) কমানো যায়
- **Data Anomalies** (Insert/Update/Delete এ সমস্যা) দূর করা যায়
- **Data Integrity** নিশ্চিত করা যায়

### Data Anomalies — কেন Normalization দরকার?

**Unnormalized Table (সমস্যাযুক্ত):**

```
employees_projects (সব এক table এ):
┌────────┬──────────┬────────┬───────────┬─────────────┬──────────────┐
│ emp_id │ emp_name │ dept   │ dept_head │ project_id  │ project_name │
├────────┼──────────┼────────┼───────────┼─────────────┼──────────────┤
│ 1      │ Karim    │ Engg   │ Mr. Hasan │ P001        │ ERP System   │
│ 1      │ Karim    │ Engg   │ Mr. Hasan │ P002        │ Mobile App   │
│ 2      │ Rafi     │ Engg   │ Mr. Hasan │ P001        │ ERP System   │
│ 3      │ Sumi     │ HR     │ Ms. Lima  │ P003        │ HR Portal    │
└────────┴──────────┴────────┴───────────┴─────────────┴──────────────┘
```

**সমস্যাগুলো:**

```
❌ Insert Anomaly:
   নতুন department যোগ করতে চাইলে employee লাগে
   employee ছাড়া department store করা যাচ্ছে না

❌ Update Anomaly:
   Mr. Hasan এর নাম পরিবর্তন হলে
   Engineering এর সব rows update করতে হবে
   একটি miss হলে inconsistency

❌ Delete Anomaly:
   Sumi কে delete করলে HR department ও
   Ms. Lima এর তথ্য হারিয়ে যাবে
```

### Normalization এর লক্ষ্য

```
Unnormalized → 1NF → 2NF → 3NF → BCNF → 4NF → 5NF
              (প্রতিটি step এ আরও refined)
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.২ 1NF — First Normal Form

### নিয়ম

১. **Atomic values:** প্রতিটি cell এ একটি মাত্র value (list বা set নয়)
২. **Same data type:** একটি column এ সব values একই type
৩. **Unique column names:** কোনো duplicate column নেই
৪. **Row order independent:** rows এর order গুরুত্বপূর্ণ নয়

### 1NF লঙ্ঘনের উদাহরণ

```
❌ 1NF লঙ্ঘন — Non-atomic values:
┌────────┬──────────┬────────────────────────┐
│ emp_id │ name     │ phone_numbers          │
├────────┼──────────┼────────────────────────┤
│ 1      │ Karim    │ 01711-111111, 01811-... │  ← Multiple values!
│ 2      │ Rafi     │ 01722-222222           │
└────────┴──────────┴────────────────────────┘

❌ 1NF লঙ্ঘন — Repeating Groups:
┌────────┬──────────┬──────────┬──────────┐
│ emp_id │ name     │ skill_1  │ skill_2  │  ← Repeating columns!
├────────┼──────────┼──────────┼──────────┤
│ 1      │ Karim    │ Python   │ MySQL    │
└────────┴──────────┴──────────┴──────────┘
```

### 1NF তে রূপান্তর

```sql
-- ❌ Before: Non-atomic
CREATE TABLE bad_employees (
    emp_id INT,
    name   VARCHAR(100),
    skills VARCHAR(500)  -- "Python, MySQL, Django"
);

-- ✅ After 1NF: Separate table
CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    name   VARCHAR(100) NOT NULL
);

CREATE TABLE employee_skills (
    emp_id   INT,
    skill    VARCHAR(100),
    PRIMARY KEY (emp_id, skill),
    FOREIGN KEY (emp_id) REFERENCES employees(emp_id)
);

INSERT INTO employee_skills VALUES (1, 'Python'), (1, 'MySQL'), (1, 'Django');
```

### 1NF Checklist

```
✅ প্রতিটি column এ একটি মাত্র value
✅ Comma-separated values নেই
✅ Repeating groups (skill_1, skill_2, skill_3) নেই
✅ Primary Key আছে
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৩ 2NF — Second Normal Form

### নিয়ম

**পূর্বশর্ত:** Table টি 1NF এ থাকতে হবে।

**মূল নিয়ম:** প্রতিটি non-key column কে **সম্পূর্ণ Primary Key** এর উপর নির্ভরশীল হতে হবে — **Partial Dependency** থাকবে না।

> Partial Dependency: Composite PK এর একটি অংশের উপর নির্ভর করা

### Partial Dependency কী?

```
Table: order_items
PK: (order_id, product_id)  ← Composite Primary Key

┌──────────┬────────────┬──────────────┬───────────────┐
│ order_id │ product_id │ quantity     │ product_name  │
├──────────┼────────────┼──────────────┼───────────────┤
│ 1        │ P01        │ 3            │ Laptop        │
│ 1        │ P02        │ 1            │ Mouse         │
│ 2        │ P01        │ 2            │ Laptop        │
└──────────┴────────────┴──────────────┴───────────────┘

product_name → শুধু product_id এর উপর নির্ভর করে
               order_id এর দরকার নেই
               → Partial Dependency! ❌
```

### 2NF তে রূপান্তর

```sql
-- ❌ Before 2NF: Partial Dependency
-- order_id + product_id → quantity (Full Dependency ✅)
-- product_id → product_name (Partial Dependency ❌)

-- ✅ After 2NF: Decompose
CREATE TABLE products (
    product_id   VARCHAR(10)  PRIMARY KEY,
    product_name VARCHAR(200) NOT NULL,
    unit_price   DECIMAL(10,2)
);

CREATE TABLE order_items (
    order_id   INT         NOT NULL,
    product_id VARCHAR(10) NOT NULL,
    quantity   INT         NOT NULL,
    PRIMARY KEY (order_id, product_id),
    FOREIGN KEY (product_id) REFERENCES products(product_id)
);
```

### 2NF শুধু Composite PK এ প্রযোজ্য

```
⚠️ Important:
Single column PK থাকলে 2NF violation সম্ভব নয়
কারণ Partial Dependency শুধু Composite PK এ হয়
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৪ 3NF — Third Normal Form

### নিয়ম

**পূর্বশর্ত:** Table টি 2NF এ থাকতে হবে।

**মূল নিয়ম:** কোনো **Transitive Dependency** থাকবে না।

> Transitive Dependency: Non-key column → Non-key column → PK

### Transitive Dependency কী?

```
Table: employees
PK: emp_id

┌────────┬──────────┬─────────┬───────────┬──────────────┐
│ emp_id │ name     │ dept_id │ dept_name │ dept_head    │
├────────┼──────────┼─────────┼───────────┼──────────────┤
│ 1      │ Karim    │ 10      │ Engg      │ Mr. Hasan    │
│ 2      │ Rafi     │ 10      │ Engg      │ Mr. Hasan    │
│ 3      │ Sumi     │ 20      │ HR        │ Ms. Lima     │
└────────┴──────────┴─────────┴───────────┴──────────────┘

emp_id → dept_id ✅ (Direct)
dept_id → dept_name (Transitive!) ❌
dept_id → dept_head (Transitive!) ❌

dept_name, dept_head non-key column এর (dept_id) উপর নির্ভর করছে
```

### 3NF তে রূপান্তর

```sql
-- ❌ Before 3NF: Transitive Dependency
-- emp_id → dept_id → dept_name, dept_head

-- ✅ After 3NF: Separate departments
CREATE TABLE departments (
    dept_id   INT          PRIMARY KEY,
    dept_name VARCHAR(100) NOT NULL,
    dept_head VARCHAR(100)
);

CREATE TABLE employees (
    emp_id  INT          PRIMARY KEY,
    name    VARCHAR(100) NOT NULL,
    dept_id INT,
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
);

-- এখন:
-- emp_id → dept_id (Direct, OK)
-- dept_id → dept_name, dept_head (শুধু departments table এ, OK)
-- কোনো Transitive Dependency নেই
```

### সহজ মনে রাখার নিয়ম

```
3NF মনে রাখুন:
"Every non-key attribute must depend on
 the key, the whole key, and nothing but the key."

→ "the key" = 2NF (Full Dependency)
→ "the whole key" = 2NF (No Partial Dep.)
→ "nothing but the key" = 3NF (No Transitive Dep.)
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৫ BCNF — Boyce-Codd Normal Form

### সংজ্ঞা

**BCNF (বা 3.5NF)** হলো 3NF এর আরও কঠোর রূপ। 3NF এর সব নিয়ম পালন করে এবং:

**মূল নিয়ম:** প্রতিটি functional dependency X → Y এ, **X অবশ্যই Superkey** হতে হবে।

> BCNF লঙ্ঘন: 3NF এ থেকেও যদি non-superkey column অন্য column কে determine করে

### BCNF vs 3NF

```
Table: course_teacher
Scenario: একটি student একটি course এ একজন teacher এর কাছে পড়ে
          প্রতিটি teacher শুধু একটি course পড়ায়

Columns: student_id, course_id, teacher_id

Dependencies:
  (student_id, course_id) → teacher_id  [PK determines teacher]
  (student_id, teacher_id) → course_id  [alternate key]
  teacher_id → course_id                 ← এটাই BCNF লঙ্ঘন!
                                            teacher_id superkey নয়
                                            কিন্তু course_id determine করছে
```

### BCNF তে রূপান্তর

```sql
-- ❌ BCNF লঙ্ঘন
CREATE TABLE course_teacher (
    student_id INT,
    course_id  INT,
    teacher_id INT,
    PRIMARY KEY (student_id, course_id)
    -- teacher_id → course_id: BCNF violation
);

-- ✅ BCNF: Decompose
CREATE TABLE teacher_courses (
    teacher_id INT PRIMARY KEY,
    course_id  INT NOT NULL
);

CREATE TABLE student_teachers (
    student_id INT,
    teacher_id INT,
    PRIMARY KEY (student_id, teacher_id),
    FOREIGN KEY (teacher_id) REFERENCES teacher_courses(teacher_id)
);
```

### Normal Forms Summary

```
┌──────┬──────────────────────────────────────────────────────┐
│ Form │ মূল নিয়ম                                             │
├──────┼──────────────────────────────────────────────────────┤
│ 1NF  │ Atomic values, কোনো repeating group নেই             │
│ 2NF  │ 1NF + No Partial Dependency                          │
│ 3NF  │ 2NF + No Transitive Dependency                       │
│ BCNF │ 3NF + Every determinant is a Superkey               │
└──────┴──────────────────────────────────────────────────────┘
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৬ 4NF ও 5NF

### 4NF — Fourth Normal Form

**পূর্বশর্ত:** BCNF  
**মূল নিয়ম:** **Multi-valued Dependency** থাকবে না।

```
Table: employee_hobbies_skills
┌────────┬─────────┬────────┐
│ emp_id │ hobby   │ skill  │
├────────┼─────────┼────────┤
│ 1      │ Cricket │ Python │
│ 1      │ Cricket │ MySQL  │
│ 1      │ Chess   │ Python │
│ 1      │ Chess   │ MySQL  │
└────────┴─────────┴────────┘

emp_id →→ hobby  (Multi-valued dependency)
emp_id →→ skill  (Multi-valued dependency)
hobby এবং skill একে অপর থেকে স্বাধীন কিন্তু
বারবার cartesian product হচ্ছে → 4NF লঙ্ঘন

✅ 4NF: আলাদা table
CREATE TABLE employee_hobbies (emp_id INT, hobby VARCHAR(100));
CREATE TABLE employee_skills  (emp_id INT, skill VARCHAR(100));
```

### 5NF — Fifth Normal Form

```
5NF (PJ/NF): Join Dependency দূর করা
Real-world interview এ 4NF ও 5NF খুব কম জিজ্ঞেস করা হয়
"জানি — Multi-valued Dependency এবং Join Dependency" বললেই যথেষ্ট
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৭ Denormalization

### সংজ্ঞা

**Denormalization** হলো ইচ্ছাকৃতভাবে **redundancy যোগ** করা — Read performance উন্নত করতে। Normalization এর বিপরীত দিক।

### কখন Denormalize করবেন?

```
✅ Denormalize করুন যখন:
  → Read-heavy system (reporting, analytics)
  → Complex JOIN এ performance সমস্যা
  → Real-time dashboard যেখানে milliseconds গুরুত্বপূর্ণ
  → Data warehouse / OLAP system

❌ Denormalize করবেন না যখন:
  → Write-heavy system (frequent INSERT/UPDATE)
  → Data integrity critical
  → OLTP system (banking, e-commerce transactions)
```

### Denormalization Techniques

```sql
-- Technique 1: Duplicate column যোগ করা
-- employees তে dept_name copy করা (JOIN এড়াতে)
ALTER TABLE employees ADD COLUMN dept_name VARCHAR(100);
-- এখন dept join ছাড়াই dept_name পাওয়া যাবে
-- কিন্তু dept_name update হলে দুই জায়গায় update করতে হবে

-- Technique 2: Computed/Derived column
ALTER TABLE orders ADD COLUMN total_items INT DEFAULT 0;
-- order_items COUNT(*) না করে সরাসরি পড়া যাবে
-- Trigger দিয়ে automatically update করা যায়

-- Technique 3: Summary/Aggregate Table
CREATE TABLE dept_salary_summary (
    dept_id      INT PRIMARY KEY,
    avg_salary   DECIMAL(10,2),
    total_salary DECIMAL(12,2),
    employee_count INT,
    last_updated DATETIME DEFAULT CURRENT_TIMESTAMP
);
-- রাতে batch job দিয়ে update করা
-- Dashboard এ এই table থেকে পড়লে JOIN লাগে না
```

### Normalization vs Denormalization

```
┌──────────────────────┬─────────────────────────────┐
│ Normalization        │ Denormalization              │
├──────────────────────┼─────────────────────────────┤
│ Data Integrity ✅    │ Data Redundancy ⚠️           │
│ Write দ্রুত          │ Read দ্রুত                   │
│ Storage কম           │ Storage বেশি                 │
│ Complex JOIN         │ Simple Query                 │
│ OLTP System          │ OLAP / Reporting             │
└──────────────────────┴─────────────────────────────┘
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৮ ER Diagram থেকে Schema

### ER Diagram এর মূল উপাদান

```
Entity          → Table
Attribute       → Column
Primary Key     → PK column
Relationship    → Foreign Key বা Junction Table
Cardinality     → FK constraint এর design
```

### Relationship Implementation

#### 1:1 (One-to-One)

```sql
-- একজন employee এর একটি passport
-- Passport table এ emp_id unique FK

CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    name   VARCHAR(100)
);

CREATE TABLE passports (
    passport_id VARCHAR(20) PRIMARY KEY,
    emp_id      INT UNIQUE NOT NULL,     -- UNIQUE → 1:1
    issue_date  DATE,
    expiry_date DATE,
    FOREIGN KEY (emp_id) REFERENCES employees(emp_id)
);
```

#### 1:N (One-to-Many)

```sql
-- একটি department এ অনেক employee
-- Employee table এ dept_id FK

CREATE TABLE departments (
    dept_id   INT          PRIMARY KEY,
    dept_name VARCHAR(100) NOT NULL
);

CREATE TABLE employees (
    emp_id  INT          PRIMARY KEY,
    name    VARCHAR(100) NOT NULL,
    dept_id INT,                         -- FK → 1:N
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
);
```

#### M:N (Many-to-Many)

```sql
-- একজন employee অনেক project এ, একটি project এ অনেক employee
-- Junction/Bridge table দরকার

CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    name   VARCHAR(100)
);

CREATE TABLE projects (
    project_id INT PRIMARY KEY,
    title      VARCHAR(200)
);

-- Junction Table (Bridge/Associative Table)
CREATE TABLE employee_projects (
    emp_id     INT  NOT NULL,
    project_id INT  NOT NULL,
    role       VARCHAR(100),            -- extra attribute
    joined_at  DATE DEFAULT (CURDATE()),
    PRIMARY KEY (emp_id, project_id),  -- Composite PK
    FOREIGN KEY (emp_id)     REFERENCES employees(emp_id) ON DELETE CASCADE,
    FOREIGN KEY (project_id) REFERENCES projects(project_id) ON DELETE CASCADE
);
```

### ER থেকে Schema — Complete Example

```
ER Design: E-commerce System
- Customer (customer_id, name, email)
- Order (order_id, date, status)
- Product (product_id, name, price, stock)
- Category (category_id, name)

Relationships:
- Customer 1:N Order
- Order M:N Product (with quantity)
- Product M:N Category (একটি product একাধিক category তে থাকতে পারে)
```

```sql
-- Schema Implementation
CREATE TABLE customers (
    customer_id INT          PRIMARY KEY AUTO_INCREMENT,
    name        VARCHAR(100) NOT NULL,
    email       VARCHAR(150) UNIQUE NOT NULL,
    phone       VARCHAR(20),
    created_at  DATETIME     DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE categories (
    category_id INT          PRIMARY KEY AUTO_INCREMENT,
    name        VARCHAR(100) NOT NULL UNIQUE
);

CREATE TABLE products (
    product_id INT            PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(200)   NOT NULL,
    price      DECIMAL(10,2)  NOT NULL CHECK (price >= 0),
    stock      INT            NOT NULL DEFAULT 0 CHECK (stock >= 0)
);

CREATE TABLE product_categories (
    product_id  INT NOT NULL,
    category_id INT NOT NULL,
    PRIMARY KEY (product_id, category_id),
    FOREIGN KEY (product_id)  REFERENCES products(product_id)  ON DELETE CASCADE,
    FOREIGN KEY (category_id) REFERENCES categories(category_id) ON DELETE CASCADE
);

CREATE TABLE orders (
    order_id    INT           PRIMARY KEY AUTO_INCREMENT,
    customer_id INT           NOT NULL,
    order_date  DATETIME      DEFAULT CURRENT_TIMESTAMP,
    status      ENUM('pending','processing','shipped','delivered','cancelled') DEFAULT 'pending',
    total       DECIMAL(12,2) NOT NULL DEFAULT 0,
    FOREIGN KEY (customer_id) REFERENCES customers(customer_id)
);

CREATE TABLE order_items (
    order_id   INT            NOT NULL,
    product_id INT            NOT NULL,
    quantity   INT            NOT NULL CHECK (quantity > 0),
    unit_price DECIMAL(10,2)  NOT NULL,
    PRIMARY KEY (order_id, product_id),
    FOREIGN KEY (order_id)   REFERENCES orders(order_id)   ON DELETE CASCADE,
    FOREIGN KEY (product_id) REFERENCES products(product_id)
);
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৯ Data Types নির্বাচন

### সঠিক Data Type কেন গুরুত্বপূর্ণ?

```
✅ সঠিক Data Type:
  → Storage কম লাগে
  → Query দ্রুত হয়
  → Data integrity নিশ্চিত হয়
  → Index efficient হয়
```

### Numeric Types

```sql
-- Integer Types (Storage ও Range অনুযায়ী বেছে নিন)
TINYINT    -- -128 to 127 (1 byte) — is_active, status flag
SMALLINT   -- -32768 to 32767 (2 bytes) — age, quantity (ছোট)
MEDIUMINT  -- ~8 million (3 bytes)
INT        -- ~2 billion (4 bytes) — সাধারণ ID, count
BIGINT     -- ~9 quintillion (8 bytes) — large ID, timestamp

-- Best practice: UNSIGNED ব্যবহার করুন যেখানে negative দরকার নেই
CREATE TABLE employees (
    emp_id    INT UNSIGNED PRIMARY KEY AUTO_INCREMENT,  -- negative হবে না
    age       TINYINT UNSIGNED,                          -- 0-255 যথেষ্ট
    salary    DECIMAL(10,2),                             -- exact precision
    rating    FLOAT                                      -- approximate OK
);

-- Decimal vs Float vs Double
DECIMAL(10,2)  -- exact, money এর জন্য (10 digits total, 2 after decimal)
FLOAT          -- approximate (4 bytes), scientific calculation
DOUBLE         -- approximate (8 bytes), more precision than FLOAT

-- ❌ Money এর জন্য FLOAT কখনো নয় — rounding error!
-- ✅ Money এর জন্য DECIMAL(12,2)
```

### String Types

```sql
-- CHAR vs VARCHAR
CHAR(10)     -- Fixed length, সবসময় 10 bytes — country code, gender
VARCHAR(100) -- Variable length, actual size + 1-2 bytes — name, email

-- কখন CHAR: সবসময় same length (phone, postal code, status codes)
-- কখন VARCHAR: variable length (name, address, description)

CREATE TABLE employees (
    emp_id      INT           PRIMARY KEY,
    name        VARCHAR(100)  NOT NULL,
    gender      CHAR(1),                   -- 'M', 'F', 'O'
    nid         CHAR(17),                  -- সবসময় ১৭ character
    email       VARCHAR(150)  UNIQUE,
    bio         TEXT,                      -- Long text, no length limit concern
    description VARCHAR(500)               -- Medium text with known max
);

-- TEXT Types
TINYTEXT   -- 255 chars
TEXT       -- 65535 chars — সাধারণ description
MEDIUMTEXT -- 16MB — article content
LONGTEXT   -- 4GB — very large content

-- ⚠️ TEXT এ Index দেওয়া সীমিত, VARCHAR এ সহজ
```

### Date/Time Types

```sql
DATE        -- '2026-05-10' (3 bytes) — birthday, join_date
TIME        -- 'HH:MM:SS' — daily schedule
DATETIME    -- '2026-05-10 14:30:00' (8 bytes) — created_at, no timezone
TIMESTAMP   -- '2026-05-10 14:30:00' (4 bytes) — auto-updates, timezone aware
YEAR        -- 4-digit year

CREATE TABLE events (
    event_id    INT       PRIMARY KEY,
    title       VARCHAR(200),
    event_date  DATE,                          -- শুধু date
    start_time  TIME,                          -- শুধু time
    created_at  DATETIME  DEFAULT CURRENT_TIMESTAMP,
    updated_at  TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);

-- DATETIME vs TIMESTAMP
-- DATETIME: '1000-01-01' to '9999-12-31' — timezone convert করে না
-- TIMESTAMP: '1970-01-01' to '2038-01-19' — UTC তে store করে, timezone aware
-- Best Practice: created_at/updated_at এর জন্য TIMESTAMP
```

### ENUM ও SET

```sql
-- ENUM: একটি নির্দিষ্ট list থেকে একটি value
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    status   ENUM('pending', 'processing', 'shipped', 'delivered', 'cancelled')
             DEFAULT 'pending'
);

-- SET: একটি list থেকে একাধিক value (bit mask)
CREATE TABLE users (
    user_id     INT PRIMARY KEY,
    permissions SET('read', 'write', 'delete', 'admin')
);

-- ⚠️ ENUM/SET তে নতুন value যোগ করতে ALTER TABLE লাগে — flexible design এ avoid করুন
-- ✅ Alternative: status table বা VARCHAR
```

### JSON Type (MySQL 5.7+)

```sql
-- Semi-structured data এর জন্য
CREATE TABLE products (
    product_id   INT  PRIMARY KEY,
    name         VARCHAR(200),
    attributes   JSON  -- {"color": "red", "size": "XL", "weight": 1.5}
);

-- JSON query
SELECT name,
       attributes->>'$.color' AS color,
       attributes->>'$.size'  AS size
FROM products
WHERE attributes->>'$.color' = 'red';
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.১০ Constraints — বিস্তারিত

### সব Constraints এক নজরে

```sql
CREATE TABLE employees (
    -- PRIMARY KEY: unique + not null, clustered index
    emp_id      INT            PRIMARY KEY AUTO_INCREMENT,

    -- NOT NULL: এই column empty হতে পারবে না
    name        VARCHAR(100)   NOT NULL,

    -- UNIQUE: duplicate value নেই (NULL allow হয়)
    email       VARCHAR(150)   UNIQUE,
    nid         CHAR(17)       UNIQUE NOT NULL,

    -- DEFAULT: value না দিলে এটি ব্যবহার হবে
    is_active   TINYINT(1)     DEFAULT 1,
    join_date   DATE           DEFAULT (CURDATE()),
    created_at  DATETIME       DEFAULT CURRENT_TIMESTAMP,

    -- CHECK: value validation (MySQL 8.0.16+)
    salary      DECIMAL(10,2)  CHECK (salary >= 0),
    age         INT            CHECK (age BETWEEN 18 AND 65),

    -- FOREIGN KEY
    dept_id     INT,
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
        ON DELETE SET NULL    -- parent delete হলে FK NULL হয়
        ON UPDATE CASCADE     -- parent PK update হলে FK ও update হয়
);
```

### ON DELETE / ON UPDATE Options

| Option | মানে |
|--------|------|
| `CASCADE` | Parent delete/update হলে child ও delete/update হয় |
| `SET NULL` | Parent delete/update হলে FK NULL হয় |
| `SET DEFAULT` | Parent delete হলে FK default value নেয় |
| `RESTRICT` | Child row থাকলে parent delete করা যাবে না |
| `NO ACTION` | RESTRICT এর মতো (MySQL এ same) |

```sql
-- উদাহরণ:
-- Department delete হলে employee কী হবে?

-- Option 1: CASCADE — department delete হলে employees ও delete
FOREIGN KEY (dept_id) REFERENCES departments(dept_id) ON DELETE CASCADE

-- Option 2: SET NULL — department delete হলে dept_id NULL হয়
FOREIGN KEY (dept_id) REFERENCES departments(dept_id) ON DELETE SET NULL

-- Option 3: RESTRICT — employee থাকলে department delete করা যাবে না
FOREIGN KEY (dept_id) REFERENCES departments(dept_id) ON DELETE RESTRICT
```

### Composite Constraints

```sql
-- Composite Primary Key
CREATE TABLE order_items (
    order_id   INT NOT NULL,
    product_id INT NOT NULL,
    quantity   INT NOT NULL,
    PRIMARY KEY (order_id, product_id)  -- Composite PK
);

-- Composite Unique
CREATE TABLE employee_projects (
    emp_id     INT NOT NULL,
    project_id INT NOT NULL,
    UNIQUE KEY uq_emp_project (emp_id, project_id)  -- Combined unique
);
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.১১ Relationships Implementation

### Self-Referencing (Recursive Relationship)

```sql
-- Employee এর manager ও employee
CREATE TABLE employees (
    emp_id     INT          PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(100) NOT NULL,
    manager_id INT,         -- নিজের table এর FK (self-reference)
    FOREIGN KEY (manager_id) REFERENCES employees(emp_id)
);

-- Data
INSERT INTO employees VALUES (1, 'Mr. Hasan', NULL);     -- Top manager
INSERT INTO employees VALUES (2, 'Karim', 1);             -- Hasan এর under
INSERT INTO employees VALUES (3, 'Rafi', 1);
INSERT INTO employees VALUES (4, 'Sumi', 2);              -- Karim এর under

-- Manager hierarchy বের করা (Self JOIN)
SELECT e.name AS employee,
       m.name AS manager
FROM employees e
LEFT JOIN employees m ON e.manager_id = m.emp_id;

-- Recursive CTE দিয়ে hierarchy tree
WITH RECURSIVE org_chart AS (
    SELECT emp_id, name, manager_id, 0 AS level
    FROM employees WHERE manager_id IS NULL
    UNION ALL
    SELECT e.emp_id, e.name, e.manager_id, oc.level + 1
    FROM employees e
    INNER JOIN org_chart oc ON e.manager_id = oc.emp_id
)
SELECT REPEAT('  ', level) || name AS hierarchy FROM org_chart;
```

### Polymorphic Association

```sql
-- একটি comment যেকোনো entity তে belong করতে পারে (post, video, product)
CREATE TABLE comments (
    comment_id    INT          PRIMARY KEY AUTO_INCREMENT,
    user_id       INT          NOT NULL,
    content       TEXT         NOT NULL,
    entity_type   VARCHAR(50)  NOT NULL,  -- 'post', 'video', 'product'
    entity_id     INT          NOT NULL,  -- সেই entity এর id
    created_at    DATETIME     DEFAULT CURRENT_TIMESTAMP,
    INDEX idx_entity (entity_type, entity_id)
);

-- Post এর comments
SELECT * FROM comments WHERE entity_type = 'post' AND entity_id = 10;

-- ⚠️ FK constraint দেওয়া যায় না (polymorphic এর সীমাবদ্ধতা)
-- ✅ Alternative: Separate comment tables per entity (strict FK নিশ্চিত করে)
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.১২ Schema Design Best Practices

### Naming Conventions

```sql
-- ✅ Consistent naming:
-- Table: snake_case, plural
-- Column: snake_case, singular descriptive
-- PK: table_name_id বা id
-- FK: referenced_table_id
-- Index: idx_table_column
-- Constraint: uq_table_column, fk_table_ref

CREATE TABLE customer_orders (       -- plural, snake_case
    order_id    INT PRIMARY KEY,     -- table_id format
    customer_id INT,                 -- FK: referenced table + _id
    order_date  DATE NOT NULL,
    CONSTRAINT fk_orders_customer
        FOREIGN KEY (customer_id) REFERENCES customers(customer_id),
    CONSTRAINT uq_order_reference
        UNIQUE KEY (order_reference_number)
);
```

### Always Include

```sql
CREATE TABLE any_table (
    id         INT          PRIMARY KEY AUTO_INCREMENT,  -- Surrogate PK
    -- ... actual columns ...
    created_at DATETIME     DEFAULT CURRENT_TIMESTAMP,  -- audit trail
    updated_at TIMESTAMP    DEFAULT CURRENT_TIMESTAMP
                            ON UPDATE CURRENT_TIMESTAMP, -- auto-update
    is_deleted TINYINT(1)   DEFAULT 0                   -- soft delete
);
```

### Avoid Common Mistakes

```
❌ SELECT * ব্যবহার করে schema design করা
❌ VARCHAR(255) সব string column এ — প্রয়োজনমতো বেছে নিন
❌ INT সব number এ — TINYINT, SMALLINT use করুন
❌ NULL এর over-use — NOT NULL ব্যবহার করুন যেখানে সম্ভব
❌ FLOAT money এর জন্য — DECIMAL ব্যবহার করুন
❌ Generic column names (data1, value, info)
❌ Space বা hyphen column/table নামে — snake_case ব্যবহার করুন
❌ Reserved keywords (order, group, select) table/column নামে
✅ UNSIGNED যেখানে negative value নেই
✅ DEFAULT value যেখানে applicable
✅ created_at/updated_at সব table এ
✅ Soft delete (is_deleted) hard delete এর বদলে
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.১৩ Real Project Schema Design

### E-Commerce Database (সম্পূর্ণ উদাহরণ)

```sql
-- ===== E-Commerce Schema =====

CREATE DATABASE ecommerce_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
USE ecommerce_db;

-- Users
CREATE TABLE users (
    user_id     INT            PRIMARY KEY AUTO_INCREMENT,
    name        VARCHAR(100)   NOT NULL,
    email       VARCHAR(150)   UNIQUE NOT NULL,
    password    VARCHAR(255)   NOT NULL,  -- hashed
    phone       VARCHAR(20),
    role        ENUM('customer','seller','admin') DEFAULT 'customer',
    is_active   TINYINT(1)     DEFAULT 1,
    created_at  DATETIME       DEFAULT CURRENT_TIMESTAMP,
    updated_at  TIMESTAMP      DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);

-- Addresses (1 user : N addresses)
CREATE TABLE addresses (
    address_id  INT            PRIMARY KEY AUTO_INCREMENT,
    user_id     INT            NOT NULL,
    label       VARCHAR(50)    DEFAULT 'home',  -- home, office, other
    street      VARCHAR(255)   NOT NULL,
    city        VARCHAR(100)   NOT NULL,
    district    VARCHAR(100),
    postal_code VARCHAR(10),
    is_default  TINYINT(1)     DEFAULT 0,
    FOREIGN KEY (user_id) REFERENCES users(user_id) ON DELETE CASCADE
);

-- Categories (Self-referencing for subcategories)
CREATE TABLE categories (
    category_id INT            PRIMARY KEY AUTO_INCREMENT,
    name        VARCHAR(100)   NOT NULL,
    slug        VARCHAR(100)   UNIQUE NOT NULL,
    parent_id   INT            DEFAULT NULL,  -- NULL = top level
    FOREIGN KEY (parent_id) REFERENCES categories(category_id)
);

-- Products
CREATE TABLE products (
    product_id   INT            PRIMARY KEY AUTO_INCREMENT,
    seller_id    INT            NOT NULL,
    name         VARCHAR(255)   NOT NULL,
    slug         VARCHAR(255)   UNIQUE NOT NULL,
    description  TEXT,
    price        DECIMAL(10,2)  NOT NULL CHECK (price >= 0),
    stock        INT            NOT NULL DEFAULT 0 CHECK (stock >= 0),
    is_active    TINYINT(1)     DEFAULT 1,
    created_at   DATETIME       DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (seller_id) REFERENCES users(user_id)
);

-- Product-Category (M:N)
CREATE TABLE product_categories (
    product_id  INT NOT NULL,
    category_id INT NOT NULL,
    PRIMARY KEY (product_id, category_id),
    FOREIGN KEY (product_id)  REFERENCES products(product_id)  ON DELETE CASCADE,
    FOREIGN KEY (category_id) REFERENCES categories(category_id)
);

-- Orders
CREATE TABLE orders (
    order_id     INT            PRIMARY KEY AUTO_INCREMENT,
    customer_id  INT            NOT NULL,
    address_id   INT,
    status       ENUM('pending','confirmed','processing',
                      'shipped','delivered','cancelled','refunded')
                 DEFAULT 'pending',
    subtotal     DECIMAL(12,2)  NOT NULL,
    shipping_fee DECIMAL(8,2)   DEFAULT 0,
    total        DECIMAL(12,2)  NOT NULL,
    notes        TEXT,
    ordered_at   DATETIME       DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (customer_id) REFERENCES users(user_id),
    FOREIGN KEY (address_id)  REFERENCES addresses(address_id) ON DELETE SET NULL
);

-- Order Items
CREATE TABLE order_items (
    order_id    INT            NOT NULL,
    product_id  INT            NOT NULL,
    quantity    INT            NOT NULL CHECK (quantity > 0),
    unit_price  DECIMAL(10,2)  NOT NULL,
    total_price DECIMAL(12,2)  GENERATED ALWAYS AS (quantity * unit_price) STORED,
    PRIMARY KEY (order_id, product_id),
    FOREIGN KEY (order_id)   REFERENCES orders(order_id)   ON DELETE CASCADE,
    FOREIGN KEY (product_id) REFERENCES products(product_id)
);

-- Reviews
CREATE TABLE reviews (
    review_id   INT            PRIMARY KEY AUTO_INCREMENT,
    product_id  INT            NOT NULL,
    user_id     INT            NOT NULL,
    rating      TINYINT        NOT NULL CHECK (rating BETWEEN 1 AND 5),
    comment     TEXT,
    created_at  DATETIME       DEFAULT CURRENT_TIMESTAMP,
    UNIQUE KEY uq_user_product_review (user_id, product_id),  -- একজন user একটি product এ একটি review
    FOREIGN KEY (product_id) REFERENCES products(product_id) ON DELETE CASCADE,
    FOREIGN KEY (user_id)    REFERENCES users(user_id)
);

-- Indexes for performance
CREATE INDEX idx_products_seller  ON products(seller_id);
CREATE INDEX idx_products_active  ON products(is_active, price);
CREATE INDEX idx_orders_customer  ON orders(customer_id, ordered_at);
CREATE INDEX idx_order_items_prod ON order_items(product_id);
```

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.১৪ PART 4 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: Normalization কী? কেন দরকার?**

> **উত্তর:** Normalization হলো database table organize করার systematic প্রক্রিয়া যা data redundancy কমায় এবং data anomalies দূর করে। এটি দরকার কারণ — without normalization: Insert Anomaly (department ছাড়া employee add করা যায় না), Update Anomaly (manager এর নাম সব rows এ update করতে হয়), Delete Anomaly (শেষ employee delete করলে department ও হারিয়ে যায়)।

---

**Q2: 1NF, 2NF, 3NF এর মধ্যে পার্থক্য উদাহরণসহ বলুন।**

> **উত্তর:** 1NF: প্রতিটি cell এ একটি atomic value, কোনো repeating group নেই (phone: "01711, 01811" → invalid)। 2NF: 1NF + Composite PK এর কোনো partial dependency নেই (order_items তে product_name শুধু product_id এর উপর নির্ভর করে — partial dep → আলাদা products table)। 3NF: 2NF + Transitive dependency নেই (employees তে dept_name আছে কিন্তু emp_id → dept_id → dept_name — transitive → আলাদা departments table)।

---

**Q3: 2NF violation শুধু কখন হয়?**

> **উত্তর:** শুধু তখন যখন table এ **Composite Primary Key** আছে। Single column PK এ 2NF violation সম্ভব নয় কারণ Partial Dependency সংজ্ঞা অনুযায়ী Composite Key এর একটি অংশের উপর নির্ভর করতে হয়।

---

**Q4: BCNF ও 3NF এর পার্থক্য কী?**

> **উত্তর:** 3NF তে শর্ত হলো: transitive dependency থাকবে না — মানে non-key column অন্য non-key column এর উপর নির্ভর করবে না। BCNF আরও কঠোর — প্রতিটি functional dependency X → Y এ X অবশ্যই superkey হতে হবে। 3NF এ থেকেও BCNF লঙ্ঘন সম্ভব যখন non-superkey column অন্য column determine করে (multiple candidate keys থাকলে)।

---

**Q5: CHAR ও VARCHAR এর পার্থক্য কী? কখন কোনটি ব্যবহার করবেন?**

> **উত্তর:** CHAR fixed length — সবসময় declared size এ store হয় (CHAR(10) → সবসময় 10 bytes, padding দিয়ে)। VARCHAR variable length — actual data + 1-2 bytes overhead। CHAR ব্যবহার করুন যখন সব values সমান length (country code: BD, phone: CHAR(11), gender: CHAR(1))। VARCHAR ব্যবহার করুন variable length data তে (name, email, address)।

---

**Q6: ON DELETE CASCADE এবং ON DELETE SET NULL এর পার্থক্য?**

> **উত্তর:** ON DELETE CASCADE: parent row delete হলে child rows ও automatically delete হয় (order delete হলে order_items ও যাক)। ON DELETE SET NULL: parent delete হলে child এর FK column NULL হয় (employee এর department delete হলে emp.dept_id = NULL হোক, employee টি থাকুক)। কোনটি ব্যবহার করবেন business logic অনুযায়ী — orphan data রাখতে চাইলে SET NULL, না রাখতে চাইলে CASCADE।

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| 1NF এর মূল নিয়ম | Atomic values, no repeating groups |
| 2NF শুধু কখন প্রযোজ্য? | Composite Primary Key থাকলে |
| Transitive Dependency কী? | A → B → C, যেখানে B non-key |
| BCNF এর মূল নিয়ম | Every determinant must be a superkey |
| M:N relationship implement | Junction/Bridge table দিয়ে |
| 1:1 relationship implement | FK column এ UNIQUE constraint |
| Money store করতে | DECIMAL(10,2) — FLOAT নয় |
| Auto-update column | TIMESTAMP ON UPDATE CURRENT_TIMESTAMP |
| Soft delete কীভাবে? | is_deleted TINYINT DEFAULT 0 |
| ENUM এর সমস্যা | নতুন value যোগে ALTER TABLE লাগে |
| Self-referencing FK | manager_id → employees(emp_id) |
| Denormalization কখন? | Read-heavy, reporting, dashboard |
| VARCHAR(255) সবসময়? | না — প্রয়োজনমতো size দিন |
| created_at vs updated_at | DATETIME vs TIMESTAMP (auto-update) |

---

> **⚠️ PART 4 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

*হ্যান্ডবুক তৈরিতে: Senior Database Engineer & Backend Architect*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 9 | চলমান — PART 4 সম্পন্ন*


<a id="part5"></a>

# PART 5: Backend & Real Project Database Design (ব্যাকএন্ড ও বাস্তব প্রজেক্ট)

> **📍 এই PART এর Sections:** [৫.১ ORM কী?](#৫১-orm-কী) · [৫.২ ORM vs Raw SQL](#৫২-orm-vs-raw-sql) · [৫.৩ DB Migration](#৫৩-database-migration) · [৫.৪ Connection Pooling](#৫৪-connection-pooling)

> **ব্যবহারের নিয়ম:** এই PART টি real-world backend development এ database কীভাবে ব্যবহার হয় তা দেখায়। Junior Engineer interview এ এই topics থেকে practical scenario-based প্রশ্ন আসে। প্রতিটি pattern বুঝুন এবং কখন কোনটি প্রযোজ্য তা বলতে পারুন।

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.১ ORM কী?

### সংজ্ঞা

**ORM (Object-Relational Mapping)** হলো একটি programming technique যা database table এবং application এর object এর মধ্যে **bridge** হিসেবে কাজ করে। SQL লেখার বদলে programming language এর code দিয়ে database operation করা যায়।

### ORM এর কাজ

```
Without ORM (Raw SQL):
  Python Code → SQL String → Database → Result → Manual Mapping

With ORM:
  Python Object → ORM → SQL (auto-generated) → Database → Python Object
```

### Popular ORM গুলো

| Language | ORM |
|----------|-----|
| Python | SQLAlchemy, Django ORM |
| PHP | Eloquent (Laravel), Doctrine |
| Java | Hibernate, JPA |
| Node.js | Sequelize, Prisma, TypeORM |
| Ruby | ActiveRecord (Rails) |
| Go | GORM |

### Django ORM উদাহরণ

```python
# Models (Table definition)
from django.db import models

class Department(models.Model):
    dept_name = models.CharField(max_length=100)
    created_at = models.DateTimeField(auto_now_add=True)

    class Meta:
        db_table = 'departments'

class Employee(models.Model):
    name       = models.CharField(max_length=100)
    email      = models.EmailField(unique=True)
    salary     = models.DecimalField(max_digits=10, decimal_places=2)
    department = models.ForeignKey(Department, on_delete=models.SET_NULL, null=True)
    join_date  = models.DateField(auto_now_add=True)
    is_active  = models.BooleanField(default=True)

    class Meta:
        db_table = 'employees'

# ORM Queries (Django ORM → SQL)
# SELECT * FROM employees;
employees = Employee.objects.all()

# SELECT * FROM employees WHERE salary > 60000;
high_paid = Employee.objects.filter(salary__gt=60000)

# SELECT * FROM employees WHERE dept_id = 1 ORDER BY salary DESC LIMIT 10;
top_eng = Employee.objects.filter(
    department__dept_name='Engineering'
).order_by('-salary')[:10]

# JOIN: SELECT e.name, d.dept_name FROM employees e JOIN departments d ...
Employee.objects.select_related('department').filter(is_active=True)

# INSERT
emp = Employee.objects.create(name='Karim', email='karim@example.com', salary=75000)

# UPDATE
Employee.objects.filter(department__dept_name='Engineering').update(salary=models.F('salary') * 1.10)

# DELETE
Employee.objects.filter(is_active=False).delete()

# Aggregate
from django.db.models import Avg, Count, Max
Employee.objects.filter(department_id=1).aggregate(
    avg_salary=Avg('salary'),
    total=Count('id'),
    max_salary=Max('salary')
)
```

### Sequelize (Node.js) উদাহরণ

```javascript
const { Model, DataTypes } = require('sequelize');

class Employee extends Model {}
Employee.init({
  emp_id:  { type: DataTypes.INTEGER, primaryKey: true, autoIncrement: true },
  name:    { type: DataTypes.STRING(100), allowNull: false },
  salary:  { type: DataTypes.DECIMAL(10,2) },
  dept_id: { type: DataTypes.INTEGER, references: { model: 'departments', key: 'dept_id' } }
}, { sequelize, tableName: 'employees', timestamps: true });

// Queries
const employees = await Employee.findAll({ where: { salary: { [Op.gt]: 60000 } } });
const emp = await Employee.findByPk(1);
await Employee.update({ salary: 80000 }, { where: { emp_id: 1 } });
await Employee.destroy({ where: { is_active: false } });
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.২ ORM vs Raw SQL

### তুলনা

| বিষয় | ORM | Raw SQL |
|------|-----|---------|
| **Development Speed** | দ্রুত | ধীর (বেশি লিখতে হয়) |
| **Learning Curve** | ORM শিখতে হয় | SQL জানলেই হয় |
| **Performance** | Overhead আছে | Optimal |
| **Complex Query** | কঠিন | সহজ |
| **Database Migration** | সহজ | কঠিন |
| **SQL Injection** | Auto-protected | Manual parameterize করতে হয় |
| **Debugging** | Generated SQL দেখা কঠিন | Direct |

### কখন কোনটি ব্যবহার করবেন?

```
✅ ORM ব্যবহার করুন:
  → CRUD operations
  → Simple to medium complexity queries
  → Rapid development
  → Team SQL knowledge কম

✅ Raw SQL ব্যবহার করুন:
  → Complex reporting queries
  → Performance-critical operations
  → Bulk data processing
  → Database-specific features (EXPLAIN, PROCEDURE)

✅ Hybrid (Best Practice):
  → ORM দিয়ে সাধারণ কাজ
  → Complex analytics এ Raw SQL বা Stored Procedure
```

### ORM Generated SQL দেখা

```python
# Django: Generated SQL print করা
qs = Employee.objects.filter(salary__gt=60000).order_by('-salary')
print(qs.query)
# SELECT `employees`.`emp_id`, `employees`.`name`, `employees`.`salary`
# FROM `employees` WHERE `employees`.`salary` > 60000
# ORDER BY `employees`.`salary` DESC

# Django debug toolbar দিয়েও দেখা যায়
```

---

## ৫.৩ Database Migration

### সংজ্ঞা

**Database Migration** হলো database schema এর **version-controlled পরিবর্তন** — table তৈরি, column যোগ/বাদ দেওয়া, index পরিবর্তন করা — এমনভাবে যা track করা যায় এবং rollback করা যায়।

### কেন Migration দরকার?

```
সমস্যা ছাড়া:
  Dev DB: users table এ phone column যোগ করলেন
  Production DB: phone column নেই
  → Application crash!

Migration দিয়ে:
  Migration file: "Add phone to users table"
  যেকোনো environment এ: python manage.py migrate
  → সব DB same schema
```

### Django Migration

```python
# Step 1: Model এ পরিবর্তন
class Employee(models.Model):
    name    = models.CharField(max_length=100)
    email   = models.EmailField()
    phone   = models.CharField(max_length=20, null=True)  # নতুন column

# Step 2: Migration file তৈরি
# python manage.py makemigrations
# Creates: 0003_employee_add_phone.py

# Step 3: Apply করা
# python manage.py migrate

# Generated migration file:
from django.db import migrations, models

class Migration(migrations.Migration):
    dependencies = [('myapp', '0002_previous_migration')]

    operations = [
        migrations.AddField(
            model_name='employee',
            name='phone',
            field=models.CharField(max_length=20, null=True),
        ),
    ]

# Rollback
# python manage.py migrate myapp 0002
```

### Raw SQL Migration (Flyway / Liquibase)

```sql
-- V3__add_phone_to_employees.sql (Flyway format)
ALTER TABLE employees ADD COLUMN phone VARCHAR(20) NULL;
CREATE INDEX idx_employees_phone ON employees(phone);

-- Migration table (auto-managed by tool)
SELECT * FROM flyway_schema_history;
-- version | description       | installed_on | success
-- 1       | create tables     | 2026-01-01   | 1
-- 2       | add email unique  | 2026-02-15   | 1
-- 3       | add phone column  | 2026-05-10   | 1
```

### Migration Best Practices

```
✅ Migration Rules:
  → Migration files কখনো edit করবেন না (committed হলে)
  → Backward compatible changes করুন (column drop এর আগে app deploy করুন)
  → Large table এ ALTER TABLE এ production এ lock হয়
    → pt-online-schema-change বা gh-ost ব্যবহার করুন
  → Migration test environment এ আগে test করুন
  → Data migration আলাদা migration file এ রাখুন
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৪ Connection Pooling

### সংজ্ঞা

**Connection Pooling** হলো database connections এর একটি **cache** যা reuse করা যায়। প্রতিটি request এ নতুন connection তৈরি না করে pool থেকে existing connection নেওয়া হয়।

### কেন দরকার?

```
Without Pooling:
  Request 1 → New Connection (100ms) → Query → Close Connection
  Request 2 → New Connection (100ms) → Query → Close Connection
  1000 requests → 1000 connections → Server overwhelmed!

With Pooling:
  Startup → Create 10 connections (pool)
  Request 1 → Take connection from pool (1ms) → Query → Return to pool
  Request 2 → Take connection from pool (1ms) → Query → Return to pool
  1000 requests → 10 connections share → Fast!
```

### Connection Pool Configuration

```python
# Python — SQLAlchemy connection pool
from sqlalchemy import create_engine

engine = create_engine(
    'mysql+pymysql://user:pass@localhost/company_db',
    pool_size=10,        # সবসময় ১০টি connection active থাকবে
    max_overflow=20,     # peak এ ৩০ পর্যন্ত (10+20)
    pool_timeout=30,     # ৩০ সেকেন্ড পর connection timeout
    pool_recycle=3600,   # ১ ঘণ্টা পর connection refresh (MySQL 8h timeout)
)
```

```javascript
// Node.js — mysql2 connection pool
const mysql = require('mysql2');

const pool = mysql.createPool({
    host:            'localhost',
    user:            'app_user',
    password:        'secret',
    database:        'company_db',
    connectionLimit: 10,        // max connections
    waitForConnections: true,   // pool full হলে wait করবে
    queueLimit:      0          // unlimited queue
});

// Pool থেকে connection নেওয়া
pool.promise().query('SELECT * FROM employees')
    .then(([rows]) => console.log(rows));
    // Automatically returns connection to pool
```

```php
// Laravel — config/database.php
'mysql' => [
    'driver'    => 'mysql',
    'host'      => env('DB_HOST', '127.0.0.1'),
    'database'  => env('DB_DATABASE', 'forge'),
    'options'   => [
        PDO::ATTR_PERSISTENT => true,  // Persistent connections
    ],
],
```

### Pool Size নির্ধারণ

```
Rule of thumb:
  Pool Size = (CPU Cores × 2) + Effective Spindle Count
  
  4 core server, SSD:
  Pool Size = (4 × 2) + 1 = 9 ≈ 10

  Overtly large pool আসলে performance কমায়!
  100 connections → Context switching overhead → Slower
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৫ N+1 Query Problem

### সংজ্ঞা

**N+1 Query Problem** হলো ORM এর সবচেয়ে সাধারণ performance problem। N টি record এর জন্য N+1 টি query চলে (1টি list query + N টি detail query)।

### N+1 সমস্যার উদাহরণ

```python
# ❌ N+1 Problem
# প্রথম query: সব employees আনো
employees = Employee.objects.all()  # 1 query: SELECT * FROM employees

# প্রতিটি employee এর জন্য আলাদা query
for emp in employees:
    print(emp.department.dept_name)  # N query: SELECT * FROM departments WHERE id=?

# Total: 1 + N queries (যেমন 100 employees → 101 queries!)
# SQL log:
# SELECT * FROM employees;
# SELECT * FROM departments WHERE dept_id = 1;
# SELECT * FROM departments WHERE dept_id = 1;
# SELECT * FROM departments WHERE dept_id = 2;
# ... (100 times)
```

### N+1 সমাধান

```python
# ✅ Solution 1: select_related (JOIN)
# Django ORM — INNER JOIN use করে
employees = Employee.objects.select_related('department').all()
# 1 query: SELECT e.*, d.* FROM employees e JOIN departments d ON e.dept_id = d.dept_id

for emp in employees:
    print(emp.department.dept_name)  # No extra query!

# ✅ Solution 2: prefetch_related (separate query, Python এ merge)
# M:N বা Reverse FK এর জন্য
employees = Employee.objects.prefetch_related('projects').all()
# 2 queries:
# SELECT * FROM employees;
# SELECT * FROM employee_projects WHERE emp_id IN (1,2,3,...);
```

```javascript
// Sequelize — N+1 সমাধান
// ❌ N+1
const employees = await Employee.findAll();
for (const emp of employees) {
    const dept = await emp.getDepartment();  // N extra queries!
}

// ✅ Eager Loading (include)
const employees = await Employee.findAll({
    include: [{ model: Department }]  // LEFT JOIN
});
// employees[0].Department.dept_name — no extra query
```

```sql
-- Raw SQL: সবসময় JOIN ব্যবহার করুন
-- ❌ N+1 equivalent
SELECT emp_id FROM employees;
-- then for each emp_id:
SELECT dept_name FROM departments WHERE dept_id = ?;

-- ✅ Single JOIN query
SELECT e.name, d.dept_name
FROM employees e
LEFT JOIN departments d ON e.dept_id = d.dept_id;
```

### N+1 Detect করা

```python
# Django: django-debug-toolbar বা query count
from django.db import connection
print(len(connection.queries))  # Query count দেখুন

# যদি employee count এর চেয়ে বেশি queries → N+1 সমস্যা
```

---

## ৫.৬ Database Caching

### সংজ্ঞা

**Database Caching** হলো frequently accessed data কে **fast storage (RAM)** এ রাখা যাতে database এ বারবার query করতে না হয়।

### Caching Layers

```
Request → Application Cache (in-memory dict) → miss?
       → Redis/Memcached Cache               → miss?
       → Database Query                      → result
                                             → store in cache
                                             → return result
```

### Redis Caching উদাহরণ

```python
import redis
import json

r = redis.Redis(host='localhost', port=6379, db=0)

def get_department_employees(dept_id):
    cache_key = f"dept:{dept_id}:employees"

    # Cache hit check
    cached = r.get(cache_key)
    if cached:
        return json.loads(cached)

    # Cache miss — database query
    employees = Employee.objects.filter(dept_id=dept_id).values('name', 'salary')
    result = list(employees)

    # Cache store with TTL (5 minutes)
    r.setex(cache_key, 300, json.dumps(result, default=str))

    return result

# Cache invalidation — employee update হলে
def update_employee_salary(emp_id, new_salary):
    Employee.objects.filter(emp_id=emp_id).update(salary=new_salary)

    # Related cache invalidate করো
    emp = Employee.objects.get(emp_id=emp_id)
    cache_key = f"dept:{emp.dept_id}:employees"
    r.delete(cache_key)  # Cache delete → next request fresh data আনবে
```

### Caching Strategies

| Strategy | কীভাবে | কখন |
|----------|--------|-----|
| **Cache-Aside** (Lazy) | Miss হলে DB থেকে আনো, cache এ রাখো | সাধারণ use case |
| **Write-Through** | Write এ DB + Cache দুটোতেই লেখো | Consistency critical |
| **Write-Behind** | Cache এ লেখো, পরে async DB তে | High write throughput |
| **Read-Through** | Cache automatically DB থেকে load করে | Transparent caching |

### Cache Invalidation সমস্যা

```
Cache Invalidation এর দুটো কঠিন সমস্যা:
  1. কখন invalidate করবেন?
  2. কোন cache key invalidate করবেন?

Solutions:
  → TTL (Time-To-Live): নির্দিষ্ট সময় পর auto-expire
  → Event-based: data update হলে manually delete
  → Cache versioning: key তে version যোগ (dept:1:v2:employees)
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৭ Pagination — Best Practices

### কেন Pagination দরকার?

```
SELECT * FROM orders;  -- ১ million rows → Memory overflow!

Pagination: ছোট chunk এ data আনো
```

### Offset-based Pagination

```sql
-- Page 1: rows 1-20
SELECT * FROM orders ORDER BY order_id LIMIT 20 OFFSET 0;

-- Page 2: rows 21-40
SELECT * FROM orders ORDER BY order_id LIMIT 20 OFFSET 20;

-- Page 100: rows 1981-2000
SELECT * FROM orders ORDER BY order_id LIMIT 20 OFFSET 1980;
```

**সমস্যা:**

```
❌ Offset এর সমস্যা:
  → Large offset এ SLOW: OFFSET 10000 মানে 10000 rows skip করতে হয়
  → Data insertion হলে page shift: OFFSET 20 এ থাকতে থাকতে
    নতুন row insert হলে একই data দুইবার বা data miss হয়
```

### Cursor-based Pagination (Keyset)

```sql
-- ✅ Cursor Pagination: অনেক দ্রুত
-- First page
SELECT * FROM orders
ORDER BY order_id
LIMIT 20;
-- Last row এর order_id ধরে রাখুন (cursor = 20)

-- Next page: cursor এর পরের rows
SELECT * FROM orders
WHERE order_id > 20   -- cursor value
ORDER BY order_id
LIMIT 20;
-- Index ব্যবহার হয়, fast!

-- API Response
{
  "data": [...],
  "next_cursor": 40,  -- last item এর id
  "has_next": true
}
```

### API Pagination Design

```python
# Django REST — PageNumberPagination
from rest_framework.pagination import PageNumberPagination, CursorPagination

class StandardPagination(PageNumberPagination):
    page_size = 20
    page_size_query_param = 'page_size'
    max_page_size = 100

class CursorBasedPagination(CursorPagination):
    page_size = 20
    ordering = 'created_at'  # Stable sort field
```

### Count Query এর সমস্যা

```sql
-- ❌ Total count এ SLOW (large table)
SELECT COUNT(*) FROM orders WHERE customer_id = 1;

-- ✅ Approximate count (good enough for UI)
SELECT TABLE_ROWS FROM information_schema.TABLES
WHERE TABLE_NAME = 'orders';

-- ✅ Cache count separately
-- অথবা শুধু "has_next" দেখান, exact count এড়িয়ে চলুন
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৮ Soft Delete Pattern

### সংজ্ঞা

**Soft Delete** হলো data physically delete না করে **একটি flag দিয়ে** deleted হিসেবে mark করা।

### কেন Soft Delete?

```
✅ Soft Delete এর সুবিধা:
  → Audit trail: কখন delete হয়েছে জানা যায়
  → Recovery: ভুলে delete হলে restore করা যায়
  → Referential integrity: FK violation এড়ানো
  → Compliance: GDPR, legal requirements

❌ Soft Delete এর সমস্যা:
  → Table এ extra rows জমে → Query ধীর
  → সব query তে WHERE is_deleted=0 যোগ করতে হয়
  → UNIQUE constraint এ সমস্যা (deleted user এর email নতুন user নিতে পারে না)
```

### Soft Delete Implementation

```sql
-- Table design
ALTER TABLE employees
    ADD COLUMN is_deleted   TINYINT(1)  DEFAULT 0,
    ADD COLUMN deleted_at   DATETIME    DEFAULT NULL,
    ADD COLUMN deleted_by   INT         DEFAULT NULL;

-- Index — active records দ্রুত আনতে
CREATE INDEX idx_employees_active ON employees(is_deleted, dept_id);

-- Soft Delete
UPDATE employees
SET is_deleted = 1, deleted_at = NOW(), deleted_by = 5
WHERE emp_id = 10;

-- সব active employees
SELECT * FROM employees WHERE is_deleted = 0;

-- Restore
UPDATE employees
SET is_deleted = 0, deleted_at = NULL, deleted_by = NULL
WHERE emp_id = 10;
```

### UNIQUE Constraint সমস্যা সমাধান

```sql
-- সমস্যা: deleted user এর email নতুন user নিতে পারে না
-- UNIQUE(email) থাকলে conflict!

-- Solution 1: email তে deleted suffix যোগ করা
UPDATE users
SET email = CONCAT(email, '.deleted.', UNIX_TIMESTAMP())
WHERE user_id = 10 AND is_deleted = 0;
UPDATE users SET is_deleted = 1 WHERE user_id = 10;

-- Solution 2: Partial/Filtered UNIQUE (MySQL এ সরাসরি নেই, PostgreSQL এ আছে)
-- MySQL workaround: UNIQUE(email, is_deleted) — কিন্তু দুইজন delete হলে conflict

-- Solution 3: Separate deleted_users table এ move করা (hard archive)
```

### Django Soft Delete

```python
from django.db import models
from django.utils import timezone

class SoftDeleteManager(models.Manager):
    def get_queryset(self):
        return super().get_queryset().filter(is_deleted=False)

class SoftDeleteModel(models.Model):
    is_deleted = models.BooleanField(default=False)
    deleted_at = models.DateTimeField(null=True, blank=True)

    objects = SoftDeleteManager()           # Default: active only
    all_objects = models.Manager()          # Including deleted

    def delete(self, *args, **kwargs):
        self.is_deleted = True
        self.deleted_at = timezone.now()
        self.save()

    def restore(self):
        self.is_deleted = False
        self.deleted_at = None
        self.save()

    class Meta:
        abstract = True

class Employee(SoftDeleteModel):
    name   = models.CharField(max_length=100)
    salary = models.DecimalField(max_digits=10, decimal_places=2)

# Usage
emp = Employee.objects.get(pk=1)
emp.delete()        # Soft delete
emp.restore()       # Restore
Employee.objects.all()          # Only active
Employee.all_objects.all()      # All including deleted
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৯ Audit Trail Pattern

### সংজ্ঞা

**Audit Trail** হলো database এ কী পরিবর্তন হয়েছে, কে করেছে, কখন করেছে তার **সম্পূর্ণ ইতিহাস** রাখার pattern।

### Audit Table Design

```sql
-- Generic Audit Log Table
CREATE TABLE audit_logs (
    log_id      BIGINT        PRIMARY KEY AUTO_INCREMENT,
    table_name  VARCHAR(100)  NOT NULL,
    record_id   BIGINT        NOT NULL,
    action      ENUM('INSERT','UPDATE','DELETE') NOT NULL,
    old_values  JSON,                 -- পরিবর্তনের আগের data
    new_values  JSON,                 -- পরিবর্তনের পরের data
    changed_by  INT,                  -- User ID (NULL = system)
    changed_at  DATETIME      NOT NULL DEFAULT CURRENT_TIMESTAMP,
    ip_address  VARCHAR(45),
    INDEX idx_audit_table_record (table_name, record_id),
    INDEX idx_audit_changed_at   (changed_at)
);

-- Employee specific audit
CREATE TABLE employee_salary_audit (
    audit_id    INT            PRIMARY KEY AUTO_INCREMENT,
    emp_id      INT            NOT NULL,
    old_salary  DECIMAL(10,2),
    new_salary  DECIMAL(10,2)  NOT NULL,
    reason      VARCHAR(255),
    changed_by  INT            NOT NULL,
    changed_at  DATETIME       DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (emp_id) REFERENCES employees(emp_id)
);
```

### Trigger দিয়ে Audit

```sql
-- Salary change এ auto audit
DELIMITER //
CREATE TRIGGER trg_employee_salary_audit
AFTER UPDATE ON employees
FOR EACH ROW
BEGIN
    IF OLD.salary <> NEW.salary THEN
        INSERT INTO employee_salary_audit
            (emp_id, old_salary, new_salary, changed_at)
        VALUES
            (NEW.emp_id, OLD.salary, NEW.salary, NOW());
    END IF;
END //
DELIMITER ;
```

### Application-level Audit (Django)

```python
from django.db import models
import json

class AuditLog(models.Model):
    table_name = models.CharField(max_length=100)
    record_id  = models.BigIntegerField()
    action     = models.CharField(max_length=10)
    old_values = models.JSONField(null=True)
    new_values = models.JSONField(null=True)
    changed_by = models.ForeignKey('User', null=True, on_delete=models.SET_NULL)
    changed_at = models.DateTimeField(auto_now_add=True)

def log_change(instance, action, old_data=None):
    AuditLog.objects.create(
        table_name=instance.__class__.__name__,
        record_id=instance.pk,
        action=action,
        old_values=old_data,
        new_values={f.name: str(getattr(instance, f.name)) for f in instance._meta.fields}
    )
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.১০ Multi-tenancy Design

### সংজ্ঞা

**Multi-tenancy** হলো একটি application **একাধিক client (tenant)** কে serve করা যেখানে প্রতিটি tenant এর data আলাদা থাকে। SaaS product এর মূল ভিত্তি।

### Three Approaches

#### Approach 1: Shared Database, Shared Table (tenant_id column)

```sql
-- সব tenant এর data একই table এ
CREATE TABLE invoices (
    invoice_id  INT          PRIMARY KEY AUTO_INCREMENT,
    tenant_id   INT          NOT NULL,    -- ← এটিই isolation
    customer_id INT          NOT NULL,
    amount      DECIMAL(10,2),
    created_at  DATETIME     DEFAULT CURRENT_TIMESTAMP,
    INDEX idx_tenant (tenant_id)          -- প্রতিটি query তে tenant_id filter
);

-- সব query তে tenant_id যোগ করতে হবে
SELECT * FROM invoices WHERE tenant_id = 5 AND customer_id = 100;
```

**সুবিধা:** সহজ, কম infrastructure cost  
**অসুবিধা:** একটি bug এ অন্য tenant এর data দেখা যেতে পারে

#### Approach 2: Shared Database, Separate Schema

```sql
-- প্রতিটি tenant এর জন্য আলাদা schema (database)
CREATE DATABASE tenant_5_db;
USE tenant_5_db;
CREATE TABLE invoices (...);  -- Same structure, separate data

-- Application routing
function getConnection(tenantId) {
    return connect(`tenant_${tenantId}_db`);
}
```

**সুবিধা:** ভালো isolation  
**অসুবিধা:** Schema migration সব databases এ করতে হয়

#### Approach 3: Separate Database per Tenant

```
Tenant 1 → Server A (DB A)
Tenant 2 → Server B (DB B)
Tenant 3 → Server A (DB C)
```

**সুবিধা:** সর্বোচ্চ isolation, compliance সহজ  
**অসুবিধা:** Expensive, management complex

### Best Practice

```
Small SaaS: Shared DB + tenant_id column (Approach 1)
Medium SaaS: Shared DB + Separate Schema (Approach 2)
Enterprise: Separate DB (Approach 3)
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.১১ Database Security

### SQL Injection Prevention

```python
# ❌ Vulnerable — User input directly SQL এ
user_input = "1 OR 1=1"
query = f"SELECT * FROM users WHERE user_id = {user_input}"
# Executes: SELECT * FROM users WHERE user_id = 1 OR 1=1
# → সব users দেখা যাবে!

# ✅ Parameterized Query — সবসময় এটি ব্যবহার করুন
cursor.execute("SELECT * FROM users WHERE user_id = %s", (user_id,))

# ✅ ORM — automatically parameterized
User.objects.filter(user_id=user_id)  # Safe

# ✅ SQLAlchemy
session.execute(text("SELECT * FROM users WHERE user_id = :uid"), {"uid": user_id})
```

### Database User Permissions

```sql
-- ❌ App root user দিয়ে connect করা — কখনো করবেন না
-- ✅ Least privilege principle

-- Application user — শুধু দরকারি permission
CREATE USER 'app_user'@'localhost' IDENTIFIED BY 'strong_password_here';

-- শুধু SELECT, INSERT, UPDATE
GRANT SELECT, INSERT, UPDATE ON company_db.* TO 'app_user'@'localhost';

-- DELETE permission নেই (soft delete ব্যবহার করুন)
-- DROP, ALTER, CREATE permission নেই

-- Read-only user (reporting)
CREATE USER 'readonly_user'@'%' IDENTIFIED BY 'another_strong_pass';
GRANT SELECT ON company_db.* TO 'readonly_user'@'%';

FLUSH PRIVILEGES;
```

### Password Hashing

```python
# ❌ Plain text password কখনো database এ রাখবেন না
# ✅ bcrypt বা Argon2 দিয়ে hash করুন

import bcrypt

password = "user_password"
hashed = bcrypt.hashpw(password.encode(), bcrypt.gensalt())
# Store hashed in DB, never plain text

# Verify
bcrypt.checkpw(password.encode(), hashed)  # True
```

### Sensitive Data Encryption

```sql
-- Sensitive columns encrypt করা
-- AES_ENCRYPT/AES_DECRYPT (MySQL)
INSERT INTO employees (name, nid_encrypted)
VALUES ('Karim', AES_ENCRYPT('1234567890123456789', UNHEX(SHA2('secret_key',256))));

SELECT name, AES_DECRYPT(nid_encrypted, UNHEX(SHA2('secret_key',256))) AS nid
FROM employees WHERE emp_id = 1;

-- Best practice: Application level encryption (not DB level)
-- DB compromised হলেও data safe
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.১২ Backup & Recovery

### Backup Types

| Type | কীভাবে | কখন |
|------|--------|-----|
| **Full Backup** | পুরো DB copy | Weekly |
| **Incremental** | Last backup এর পর পরিবর্তন | Daily |
| **Differential** | Last full backup এর পর পরিবর্তন | Daily |
| **Logical** | mysqldump (SQL statements) | Development, small DB |
| **Physical** | Raw data files copy | Production, large DB |

### MySQL Backup Commands

```bash
# Full logical backup (mysqldump)
mysqldump -u root -p company_db > company_db_backup_2026-05-10.sql

# Specific tables
mysqldump -u root -p company_db employees departments > partial_backup.sql

# Compress করে backup
mysqldump -u root -p company_db | gzip > company_db_2026-05-10.sql.gz

# Restore
mysql -u root -p company_db < company_db_backup_2026-05-10.sql

# Compressed restore
gunzip < company_db_2026-05-10.sql.gz | mysql -u root -p company_db

# Point-in-time recovery (Binary Log)
mysqlbinlog --start-datetime="2026-05-10 10:00:00"             --stop-datetime="2026-05-10 14:30:00"             /var/log/mysql/mysql-bin.000001 | mysql -u root -p
```

### Backup Best Practices

```
✅ 3-2-1 Backup Rule:
  → 3 copies of data
  → 2 different storage media
  → 1 offsite backup (cloud/remote)

✅ Test Restore করুন:
  → Backup নেওয়া যথেষ্ট নয়
  → Regular restore drill করুন
  → "Backup আছে কিন্তু restore কাজ করে না" = কোনো backup নেই

✅ Automation:
  → Cron job দিয়ে automated backup
  → 0 2 * * * mysqldump ... (রাত ২টায় daily backup)

✅ Retention Policy:
  → Daily: 7 days
  → Weekly: 4 weeks
  → Monthly: 12 months
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.১৩ Real Project — Job Portal Schema

```sql
-- ===== Job Portal Database =====

CREATE DATABASE jobportal_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
USE jobportal_db;

-- Users (Unified: Job Seeker + Recruiter)
CREATE TABLE users (
    user_id    INT            PRIMARY KEY AUTO_INCREMENT,
    name       VARCHAR(100)   NOT NULL,
    email      VARCHAR(150)   UNIQUE NOT NULL,
    password   VARCHAR(255)   NOT NULL,
    role       ENUM('jobseeker','recruiter','admin') NOT NULL DEFAULT 'jobseeker',
    phone      VARCHAR(20),
    avatar_url VARCHAR(500),
    is_active  TINYINT(1)     DEFAULT 1,
    created_at DATETIME       DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP      DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);

-- Companies
CREATE TABLE companies (
    company_id   INT            PRIMARY KEY AUTO_INCREMENT,
    recruiter_id INT            NOT NULL,
    name         VARCHAR(200)   NOT NULL,
    industry     VARCHAR(100),
    size         ENUM('1-10','11-50','51-200','201-500','500+'),
    website      VARCHAR(500),
    description  TEXT,
    logo_url     VARCHAR(500),
    is_verified  TINYINT(1)     DEFAULT 0,
    FOREIGN KEY (recruiter_id) REFERENCES users(user_id)
);

-- Job Listings
CREATE TABLE jobs (
    job_id       INT             PRIMARY KEY AUTO_INCREMENT,
    company_id   INT             NOT NULL,
    title        VARCHAR(255)    NOT NULL,
    description  TEXT            NOT NULL,
    requirements TEXT,
    job_type     ENUM('full-time','part-time','contract','internship','remote') NOT NULL,
    experience   ENUM('fresher','1-2 years','3-5 years','5+ years') DEFAULT 'fresher',
    salary_min   DECIMAL(10,2),
    salary_max   DECIMAL(10,2),
    location     VARCHAR(200),
    deadline     DATE,
    status       ENUM('draft','active','closed','expired') DEFAULT 'active',
    views        INT             DEFAULT 0,
    created_at   DATETIME        DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (company_id) REFERENCES companies(company_id) ON DELETE CASCADE,
    INDEX idx_jobs_status_created (status, created_at DESC),
    INDEX idx_jobs_location       (location),
    INDEX idx_jobs_type           (job_type, experience)
);

-- Skills (Master list)
CREATE TABLE skills (
    skill_id INT          PRIMARY KEY AUTO_INCREMENT,
    name     VARCHAR(100) UNIQUE NOT NULL
);

-- Job required skills (M:N)
CREATE TABLE job_skills (
    job_id   INT NOT NULL,
    skill_id INT NOT NULL,
    PRIMARY KEY (job_id, skill_id),
    FOREIGN KEY (job_id)   REFERENCES jobs(job_id)   ON DELETE CASCADE,
    FOREIGN KEY (skill_id) REFERENCES skills(skill_id)
);

-- Job Seeker Profiles
CREATE TABLE profiles (
    profile_id  INT            PRIMARY KEY AUTO_INCREMENT,
    user_id     INT            UNIQUE NOT NULL,  -- 1:1 with user
    headline    VARCHAR(255),
    summary     TEXT,
    resume_url  VARCHAR(500),
    linkedin    VARCHAR(500),
    github      VARCHAR(500),
    experience_years TINYINT  DEFAULT 0,
    FOREIGN KEY (user_id) REFERENCES users(user_id) ON DELETE CASCADE
);

-- Profile skills (M:N)
CREATE TABLE profile_skills (
    profile_id INT NOT NULL,
    skill_id   INT NOT NULL,
    level      ENUM('beginner','intermediate','advanced') DEFAULT 'intermediate',
    PRIMARY KEY (profile_id, skill_id),
    FOREIGN KEY (profile_id) REFERENCES profiles(profile_id) ON DELETE CASCADE,
    FOREIGN KEY (skill_id)   REFERENCES skills(skill_id)
);

-- Job Applications
CREATE TABLE applications (
    app_id       INT            PRIMARY KEY AUTO_INCREMENT,
    job_id       INT            NOT NULL,
    user_id      INT            NOT NULL,
    cover_letter TEXT,
    status       ENUM('applied','screening','interview','offered','rejected','withdrawn')
                 DEFAULT 'applied',
    applied_at   DATETIME       DEFAULT CURRENT_TIMESTAMP,
    updated_at   TIMESTAMP      DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
    UNIQUE KEY uq_job_user (job_id, user_id),   -- একই job এ একবারই apply
    FOREIGN KEY (job_id)  REFERENCES jobs(job_id)   ON DELETE CASCADE,
    FOREIGN KEY (user_id) REFERENCES users(user_id) ON DELETE CASCADE,
    INDEX idx_applications_user   (user_id, applied_at DESC),
    INDEX idx_applications_job    (job_id, status)
);

-- Saved Jobs
CREATE TABLE saved_jobs (
    user_id    INT      NOT NULL,
    job_id     INT      NOT NULL,
    saved_at   DATETIME DEFAULT CURRENT_TIMESTAMP,
    PRIMARY KEY (user_id, job_id),
    FOREIGN KEY (user_id) REFERENCES users(user_id) ON DELETE CASCADE,
    FOREIGN KEY (job_id)  REFERENCES jobs(job_id)   ON DELETE CASCADE
);

-- Useful Views
CREATE VIEW active_jobs_with_company AS
SELECT j.job_id, j.title, j.job_type, j.experience,
       j.salary_min, j.salary_max, j.location, j.deadline,
       c.name AS company_name, c.logo_url, c.is_verified
FROM jobs j
INNER JOIN companies c ON j.company_id = c.company_id
WHERE j.status = 'active' AND (j.deadline IS NULL OR j.deadline >= CURDATE());
```

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.১৪ PART 5 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: ORM কি সবসময় Raw SQL এর চেয়ে ধীর?**

> **উত্তর:** না সবসময় নয়, তবে overhead আছে। ORM প্রতিটি query তে object mapping এবং query building এ extra processing করে। Simple CRUD এ পার্থক্য negligible। Complex query তে (multiple JOINs, aggregations) ORM এর generated SQL optimized নাও হতে পারে। Best practice: ORM দিয়ে সাধারণ কাজ, performance-critical analytics এ Raw SQL।

---

**Q2: N+1 Query Problem কী? কীভাবে detect ও solve করবেন?**

> **উত্তর:** N+1 হলো ORM এ loop এর মধ্যে related object access করলে N টি extra query চলে। যেমন 100 employees এর department দেখাতে গেলে 101 queries (1+100)। Detect: Django debug toolbar, query count log। Solve: select_related() (JOIN), prefetch_related() (separate query + merge)। Raw SQL এ সবসময় JOIN ব্যবহার করুন।

---

**Q3: Connection Pooling কী? Pool size কত রাখবেন?**

> **উত্তর:** Connection Pool হলো pre-created database connections এর cache। প্রতিটি request এ নতুন connection তৈরি (100ms overhead) এর বদলে pool থেকে existing connection নেওয়া হয়। Pool size সূত্র: (CPU cores × 2) + disk spindles। 4-core SSD server এ ~10। খুব বড় pool আসলে context switching overhead বাড়ায় — performance কমে।

---

**Q4: Cursor-based Pagination এবং Offset-based Pagination এর পার্থক্য?**

> **উত্তর:** Offset Pagination: `LIMIT 20 OFFSET 1000` — database 1000 rows skip করে পরেরগুলো দেয় — large offset এ slow। Data insert হলে page shift হয় (same data twice বা miss)। Cursor Pagination: `WHERE id > last_id LIMIT 20` — Index ব্যবহার করে, সবসময় দ্রুত, consistent। Infinite scroll এ cursor pagination best।

---

**Q5: Soft Delete এর সুবিধা ও সমস্যা কী?**

> **উত্তর:** সুবিধা: audit trail, recovery সম্ভব, FK integrity বজায় থাকে। সমস্যা: table এ extra rows জমে (index ও বড় হয়), সব query তে `WHERE is_deleted=0` যোগ করতে হয়, UNIQUE constraint এ conflict (deleted user এর email)। UNIQUE সমস্যার সমাধান: deleted row এ email এ timestamp suffix যোগ করা।

---

**Q6: Database এ SQL Injection কীভাবে prevent করবেন?**

> **উত্তর:** সবচেয়ে গুরুত্বপূর্ণ: Parameterized Query / Prepared Statement ব্যবহার করুন — user input কখনো SQL string এ directly concatenate করবেন না। ORM automatically parameterize করে। Additional: Database user এ least privilege (app user এর DROP/ALTER নেই), Input validation, WAF (Web Application Firewall)।

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| ORM এর পূর্ণরূপ | Object-Relational Mapping |
| Django ORM এ JOIN | select_related() |
| Django ORM এ M:N prefetch | prefetch_related() |
| Migration rollback কীভাবে? | migrate app_name previous_version |
| Connection Pool এর default size | সাধারণত 5-10 |
| N+1 এর সমাধান | Eager loading (JOIN/prefetch) |
| Cache-Aside strategy | Miss হলে DB থেকে আনো, cache এ রাখো |
| Soft delete column | is_deleted TINYINT DEFAULT 0 |
| Audit log তে কী থাকে | table, record_id, action, old/new values, user, time |
| Multi-tenancy সহজ approach | tenant_id column |
| Password DB তে কীভাবে? | bcrypt/Argon2 hash — কখনো plain text নয় |
| DB user এর সবচেয়ে কম permission | SELECT, INSERT, UPDATE only |
| 3-2-1 Backup মানে | 3 copies, 2 media, 1 offsite |
| mysqldump কী? | Logical backup tool |

---

> **⚠️ PART 5 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

*হ্যান্ডবুক তৈরিতে: Senior Database Engineer & Backend Architect*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 9 | চলমান — PART 5 সম্পন্ন*


<a id="part6"></a>

# PART 6: Database Interview Questions (ইন্টারভিউ প্রশ্নোত্তর সংকলন)

> **📍 এই PART এর Sections:** [৬.১ Fundamentals Q&A](#৬১-database-fundamentals-qa) · [৬.২ SQL Q&A](#৬২-sql-qa) · [৬.৩ Advanced Q&A](#৬৩-advanced-concepts-qa) · [৬.৪ Design & Normalization Q&A](#৬৪-design--normalization-qa)

> **ব্যবহারের নিয়ম:** এই PART টি সম্পূর্ণ interview preparation এর জন্য। PART 1–5 এর সব concepts এখানে প্রশ্নোত্তর আকারে সংকলিত। Interview এর আগের রাতে এই PART টি পুরো পড়ুন। প্রতিটি উত্তর নিজের ভাষায় বলার চেষ্টা করুন।

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.১ Database Fundamentals Q&A

**Q1: Database এবং DBMS এর পার্থক্য কী?**

> **উত্তর:** Database হলো structured data এর collection — files, tables, records। DBMS (Database Management System) হলো সেই data manage করার software — MySQL, PostgreSQL, Oracle। DBMS ছাড়া database শুধু files, DBMS দিয়ে সেই data query, update, secure করা যায়।

---

**Q2: RDBMS কী? কোন কোন database RDBMS?**

> **উত্তর:** RDBMS (Relational DBMS) হলো এমন DBMS যা data কে interrelated tables এ store করে এবং SQL দিয়ে query করা যায়। ACID properties support করে। উদাহরণ: MySQL, PostgreSQL, Oracle, SQL Server, SQLite। Non-relational (NoSQL): MongoDB, Redis, Cassandra।

---

**Q3: Primary Key এবং Foreign Key এর পার্থক্য?**

> **উত্তর:** Primary Key: একটি table এ প্রতিটি row কে uniquely identify করে — duplicate ও NULL হয় না, প্রতি table এ একটি। Foreign Key: অন্য table এর Primary Key কে reference করে — referential integrity নিশ্চিত করে, NULL হতে পারে (optional relationship)। FK ছাড়া relationship logically exist করে কিন্তু database enforce করে না।

---

**Q4: Candidate Key, Super Key, Alternate Key কী?**

> **উত্তর:** Super Key: একটি বা একাধিক columns যা row uniquely identify করতে পারে (emp_id), (emp_id, name) উভয়ই Super Key। Candidate Key: Minimal Super Key — extra column নেই (emp_id একটি Candidate Key, (emp_id, name) নয়)। Primary Key: নির্বাচিত Candidate Key। Alternate Key: Primary Key ছাড়া বাকি Candidate Keys (email, nid)।

---

**Q5: NULL কী? NULL = 0 বা NULL = "" কি সত্য?**

> **উত্তর:** NULL মানে **value এর অনুপস্থিতি** — unknown বা not applicable। NULL ≠ 0, NULL ≠ ""। NULL এর সাথে যেকোনো arithmetic/comparison NULL return করে: `NULL = NULL` → NULL (false), `NULL + 5` → NULL। NULL check করতে `IS NULL` বা `IS NOT NULL` ব্যবহার করুন, `= NULL` নয়।

---

**Q6: Constraint কী কী ধরনের?**

> **উত্তর:** PRIMARY KEY (unique + not null), FOREIGN KEY (referential integrity), UNIQUE (duplicate নেই, NULL allow), NOT NULL (empty হবে না), DEFAULT (value না দিলে এটি), CHECK (value validation — MySQL 8.0.16+)। Constraints data integrity নিশ্চিত করে।

---

**Q7: ER Diagram এ Entity, Attribute, Relationship কী?**

> **উত্তর:** Entity: real-world object যার data store করি (Employee, Department) — table হয়। Attribute: entity এর property (name, salary) — column হয়। Relationship: entities এর মধ্যে সম্পর্ক (Employee works_in Department) — FK বা junction table হয়। Cardinality: 1:1, 1:N, M:N।

---

**Q8: 1:1, 1:N, M:N Relationship কীভাবে implement করবেন?**

> **উত্তর:** 1:1: এক table এ অন্যটির FK রাখুন, UNIQUE constraint দিন (passport তে emp_id UNIQUE)। 1:N: "N" দিকের table এ "1" দিকের PK FK হিসেবে রাখুন (employees তে dept_id)। M:N: Junction table তৈরি করুন যাতে দুটো FK Composite PK হয় (employee_projects: emp_id + project_id)।

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.২ SQL Q&A

**Q9: INNER JOIN এবং LEFT JOIN এর পার্থক্য?**

> **উত্তর:** INNER JOIN: শুধু দুই table এ match করে এমন rows — মিল না থাকলে বাদ। LEFT JOIN: বাম table এর সব rows + ডান table এ match থাকলে তার data, না থাকলে NULL। উদাহরণ: সব employees এবং তাদের department (department না থাকলেও) → LEFT JOIN। শুধু department আছে এমন employees → INNER JOIN।

---

**Q10: GROUP BY এবং HAVING এর পার্থক্য?**

> **উত্তর:** GROUP BY: rows কে গ্রুপ করে aggregate function (COUNT, SUM, AVG) প্রয়োগ করতে। HAVING: GROUP BY এর পরে গ্রুপ filter করে — aggregate condition এ। WHERE aggregate এ কাজ করে না, HAVING করে। উদাহরণ: `GROUP BY dept_id HAVING COUNT(*) > 5` — ৫ এর বেশি employee আছে এমন department।

---

**Q11: WHERE এবং HAVING এর পার্থক্য?**

> **উত্তর:** WHERE: individual rows filter করে, GROUP BY এর আগে চলে, aggregate function ব্যবহার করা যায় না। HAVING: groups filter করে, GROUP BY এর পরে চলে, aggregate function ব্যবহার করা যায়। `WHERE salary > 50000` → individual rows। `HAVING AVG(salary) > 50000` → groups।

---

**Q12: Subquery এবং JOIN — কোনটি ভালো?**

> **উত্তর:** সাধারণত JOIN দ্রুত — optimizer JOIN ভালো optimize করে। Correlated Subquery ধীর কারণ প্রতিটি outer row তে inner query চলে। তবে কিছু ক্ষেত্রে subquery readable — EXISTS check, single value return এ। EXPLAIN দিয়ে দুটোর execution plan তুলনা করুন।

---

**Q13: UNION এবং UNION ALL এর পার্থক্য?**

> **উত্তর:** UNION: duplicate rows বাদ দেয় (internally DISTINCT করে) — ধীর। UNION ALL: সব rows রাখে duplicate সহ — দ্রুত। Duplicate নিশ্চিতভাবে না থাকলে বা দরকার না হলে UNION ALL prefer করুন। দুটো result set এর column number ও data type same হতে হবে।

---

**Q14: DELETE, TRUNCATE, DROP এর পার্থক্য?**

> **উত্তর:**
> - **DELETE:** Row-by-row delete, WHERE দিয়ে specific rows, ROLLBACK করা যায়, trigger চলে, AUTO_INCREMENT reset হয় না।
> - **TRUNCATE:** সব rows একবারে delete, WHERE দেওয়া যায় না, ROLLBACK সাধারণত যায় না, trigger চলে না, AUTO_INCREMENT reset হয়।
> - **DROP:** পুরো table structure + data মুছে ফেলে — table আর থাকে না।

---

**Q15: LIKE operator এ % এবং _ এর পার্থক্য?**

> **উত্তর:** `%` যেকোনো length এর যেকোনো characters (zero বা more)। `_` ঠিক একটি character। `LIKE 'Ka%'` → Karim, Kamal, Kabir। `LIKE 'Ka_im'` → Karim (K-a-?-i-m)। Leading `%LIKE` index ব্যবহার করতে পারে না — full scan।

---

**Q16: Aggregate Functions কী কী?**

> **উত্তর:** `COUNT(*)` — সব rows (NULL সহ), `COUNT(col)` — non-NULL rows। `SUM(col)` — যোগফল। `AVG(col)` — গড়। `MAX(col)` — সর্বোচ্চ। `MIN(col)` — সর্বনিম্ন। `GROUP_CONCAT(col)` — values comma-separated string এ। সবই NULL values ignore করে (COUNT(*) ছাড়া)।

---

**Q17: Window Functions কী? Regular Aggregate থেকে পার্থক্য?**

> **উত্তর:** Window Function: rows এর একটি "window" তে aggregate calculate করে কিন্তু rows বাদ দেয় না — প্রতিটি row তার নিজের data রাখে। Regular Aggregate GROUP BY তে rows একত্রিত করে ফেলে।

```sql
-- Window Function উদাহরণ
SELECT name, salary, dept_id,
       AVG(salary) OVER (PARTITION BY dept_id) AS dept_avg,
       RANK() OVER (PARTITION BY dept_id ORDER BY salary DESC) AS rank_in_dept
FROM employees;
-- প্রতিটি row থাকে + department এর average ও rank দেখায়
```

---

**Q18: COALESCE এবং IFNULL এর পার্থক্য?**

> **উত্তর:** `IFNULL(expr, fallback)` — MySQL specific, শুধু দুটো argument। `COALESCE(a, b, c, ...)` — standard SQL, প্রথম non-NULL value return করে, যতগুলো argument দেওয়া যায়। `COALESCE(NULL, NULL, 5)` → 5। Production এ COALESCE prefer করুন।

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৩ Advanced Concepts Q&A

**Q19: Index কী? কীভাবে কাজ করে?**

> **উত্তর:** Index হলো B-Tree data structure যা column এর values sorted রাখে। Index ছাড়া O(n) full scan, Index দিয়ে O(log n) binary search। CREATE INDEX idx_salary ON employees(salary) → salary column এ B-Tree তৈরি হয়। Trade-off: READ দ্রুত, WRITE ধীর (index ও update করতে হয়), extra disk space।

---

**Q20: Clustered ও Non-clustered Index এর পার্থক্য?**

> **উত্তর:** Clustered Index: physical data এই order এ stored — MySQL InnoDB তে Primary Key automatically Clustered। প্রতি table এ একটি। Non-clustered: separate structure, pointer দিয়ে actual data তে যায়। Multiple হতে পারে। Covering Index: query র সব column index এ থাকলে table এ যেতে হয় না।

---

**Q21: Transaction কী? COMMIT ও ROLLBACK কী করে?**

> **উত্তর:** Transaction হলো logical unit of work — হয় সব হবে নয়তো কিছুই নয়। COMMIT: সব changes permanent করা — disk এ লেখা হয়। ROLLBACK: সব changes বাতিল করা — original state এ ফেরা। `START TRANSACTION` → operations → `COMMIT` (success) বা `ROLLBACK` (failure)।

---

**Q22: ACID এর চারটি property বোঝান।**

> **উত্তর:** **Atomicity** — bank transfer: debit ও credit দুটোই হবে নয়তো কোনোটাই নয়। **Consistency** — transfer এর আগে ও পরে মোট balance একই। **Isolation** — concurrent transactions একে অপরের uncommitted data দেখে না। **Durability** — COMMIT হওয়ার পর server crash হলেও data থাকে (WAL log)।

---

**Q23: Isolation Levels কী কী? Default কোনটি?**

> **উত্তর:** READ UNCOMMITTED (Dirty Read হয়), READ COMMITTED (Dirty Read নেই), REPEATABLE READ (Non-Repeatable Read নেই — MySQL default), SERIALIZABLE (সব problem নেই কিন্তু ধীরতম)। MySQL InnoDB default: REPEATABLE READ। যত বেশি isolation তত কম concurrency, তত বেশি performance cost।

---

**Q24: Deadlock কী? কীভাবে সমাধান হয়?**

> **উত্তর:** Transaction A, B এর lock এর জন্য wait। B, A এর lock এর জন্য wait — circular dependency, কেউ এগোতে পারছে না। MySQL automatically detect করে এবং একটি transaction (victim) ROLLBACK করে। Prevention: একই order এ rows lock করুন, transaction ছোট রাখুন, lock timeout সেট করুন।

---

**Q25: View কী? কখন ব্যবহার করবেন?**

> **উত্তর:** View হলো stored SELECT query থেকে তৈরি virtual table — data physically store হয় না। ব্যবহার: security (sensitive columns লুকানো), simplicity (complex query কে simple view বানানো), reusability। Materialized View: data cached — PostgreSQL তে আছে, MySQL তে নেই।

---

**Q26: Stored Procedure ও Function এর পার্থক্য?**

> **উত্তর:** Function: single value return, SELECT এ ব্যবহার যোগ্য, DML করতে পারে না। Stored Procedure: multiple result sets, DML করতে পারে, transaction handle করে, SELECT এ সরাসরি ব্যবহার যায় না। দুটোই pre-compiled, reusable।

---

**Q27: Trigger কী? কখন সতর্ক থাকবেন?**

> **উত্তর:** Trigger হলো automatic action যা INSERT/UPDATE/DELETE event এ আগে বা পরে চলে। Audit logging, data normalization এ useful। সতর্কতা: invisible side effects (কোথায় কী হচ্ছে বোঝা কঠিন), debug কঠিন, cascading triggers বিপজ্জনক, performance overhead।

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৪ Design & Normalization Q&A

**Q28: Normalization কী? কেন দরকার?**

> **উত্তর:** Normalization হলো table organize করার process যা redundancy কমায় এবং anomaly দূর করে। Insert Anomaly (department ছাড়া employee add করা যায় না), Update Anomaly (manager এর নাম সব rows এ বদলাতে হয়), Delete Anomaly (শেষ employee delete করলে department হারিয়ে যায়) — এই সমস্যাগুলো দূর করে।

---

**Q29: 1NF, 2NF, 3NF এর মূল পার্থক্য কী?**

> **উত্তর:** 1NF: Atomic values, কোনো repeating group বা list নেই (phone: "01711, 01811" invalid)। 2NF: 1NF + Composite PK এ Partial Dependency নেই (order_items তে product_name শুধু product_id এ নির্ভর করলে 2NF লঙ্ঘন)। 3NF: 2NF + Transitive Dependency নেই (employees তে dept_id → dept_name থাকলে 3NF লঙ্ঘন)।

---

**Q30: Denormalization কখন করবেন?**

> **উত্তর:** Read-heavy system এ যেখানে JOIN এর performance cost সমস্যা করছে। Data Warehouse, Reporting, Analytics, Dashboard এ। Denormalization মানে ইচ্ছাকৃতভাবে redundancy যোগ করা — Read দ্রুত হয় কিন্তু Write ধীর ও inconsistency risk বাড়ে। OLTP system (banking, e-commerce) এ এড়িয়ে চলুন।

---

**Q31: CHAR এবং VARCHAR এর মধ্যে কোনটি কখন?**

> **উত্তর:** CHAR(n): fixed n bytes সবসময় — সব values same length এ (country code: CHAR(2), gender: CHAR(1), phone: CHAR(11))। VARCHAR(n): variable — actual size + 1-2 bytes। name, email, address এ VARCHAR। VARCHAR storage efficient কিন্তু CHAR slightly faster (no length calculation)।

---

**Q32: Money store করতে কোন data type?**

> **উত্তর:** DECIMAL(precision, scale) — যেমন DECIMAL(12,2) (10 digits + 2 decimal)। FLOAT বা DOUBLE কখনো নয় — floating point rounding error এ financial data incorrect হয়। `0.1 + 0.2 = 0.30000000000000004` (float) — DECIMAL এ ঠিকঠাক।

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৫ Performance & Optimization Q&A

**Q33: Query slow হলে কী করবেন? Step-by-step বলুন।**

> **উত্তর:**
> 1. `EXPLAIN` দিয়ে execution plan দেখুন — `type: ALL` (full scan) দেখলে সমস্যা
> 2. WHERE, JOIN, ORDER BY column এ Index আছে কিনা দেখুন
> 3. `SELECT *` এর বদলে শুধু দরকারি columns নিন
> 4. Subquery → JOIN এ রূপান্তর করুন
> 5. WHERE এ function ব্যবহার এড়িয়ে চলুন (`WHERE YEAR(date)` → range condition)
> 6. LIMIT যোগ করুন
> 7. Index যোগ করুন এবং আবার EXPLAIN দিয়ে confirm করুন

---

**Q34: Index থাকলেও কখন কাজ করে না?**

> **উত্তর:**
> - `WHERE UPPER(name) = 'KARIM'` — function wrap করলে index কাজ করে না
> - `WHERE name LIKE '%Karim'` — leading wildcard
> - `WHERE salary + 1000 > 60000` — column এ arithmetic
> - Low cardinality column (gender: শুধু M/F) — optimizer full scan prefer করে
> - Composite index এ first column skip করলে (idx: dept_id, salary → WHERE salary > 60000 এ কাজ করে না)

---

**Q35: EXPLAIN এর output কীভাবে পড়বেন?**

> **উত্তর:** `type` column সবচেয়ে গুরুত্বপূর্ণ — `const` (best), `eq_ref`, `ref`, `range`, `index`, `ALL` (worst/full scan)। `key` column দেখুন — কোন index ব্যবহার হচ্ছে। `rows` — estimated scanned rows (কম হওয়া ভালো)। `Extra: Using index` — Covering Index (table এ যেতে হয়নি, দ্রুত)। `Extra: Using filesort` — extra sort — index দিয়ে avoid করুন।

---

**Q36: Partitioning এবং Sharding এর পার্থক্য?**

> **উত্তর:** Partitioning: একটি server এ একটি table কে physically ভাগ করা (RANGE, LIST, HASH)। Partition Pruning: query শুধু relevant partition scan করে। Sharding: data multiple servers এ distribute করা — horizontal scaling। Partitioning medium scale, Sharding Facebook/Instagram scale। Sharding এ cross-shard JOIN কঠিন।

---

**Q37: Replication কী? কী কাজে লাগে?**

> **উত্তর:** Replication: Master এর data Slave server(s) এ automatically copy হওয়া। কাজ: High Availability (Master fail হলে Slave promote), Read Scalability (READ query Slave থেকে), Backup (Slave থেকে backup নিলে Master affected হয় না)। Replication Lag: Master ও Slave এর data এর সময়ের পার্থক্য।

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৬ Scenario-based Questions

**Q38: একটি e-commerce site এ orders table এ 10 million rows আছে। Customer এর সব orders page করে দেখাতে চাই — কীভাবে করবেন?**

> **উত্তর:** Cursor-based Pagination ব্যবহার করব। `WHERE customer_id = ? AND order_id > last_cursor ORDER BY order_id LIMIT 20`। (customer_id, order_id) এ Composite Index দেব। Offset Pagination এড়াব কারণ large offset এ database সব rows skip করে — 10M row এ `OFFSET 9999980` অনেক slow।

---

**Q39: User table এ email UNIQUE আছে। Soft Delete implement করতে চাই — কিন্তু deleted user এর email নতুন user নিতে পারছে না। কীভাবে সমাধান করবেন?**

> **উত্তর:** Delete করার সময় email কে modify করব: `UPDATE users SET email = CONCAT(email, '.deleted.', UNIX_TIMESTAMP()), is_deleted = 1 WHERE user_id = ?`। এতে original email free হয়ে যায় নতুন user এর জন্য, কিন্তু deleted user এর record থাকে। Alternative: deleted_email আলাদা column এ সংরক্ষণ করা।

---

**Q40: দুটো transaction একসাথে একই row update করলে কী হয়?**

> **উত্তর:** Database এর Isolation Level অনুযায়ী। READ COMMITTED এ: পরেরজনের UPDATE প্রথমজনের committed value দেখে, তারপর update করে (Last Write Wins)। SERIALIZABLE এ: পরেরজন wait করবে। Race condition prevent করতে `SELECT ... FOR UPDATE` (Pessimistic Locking) বা version column দিয়ে Optimistic Locking ব্যবহার করুন।

---

**Q41: একটি reports query আছে যা employees, departments, projects, client সব JOIN করে — অনেক slow। কীভাবে fast করবেন?**

> **উত্তর:** প্রথমে EXPLAIN দিয়ে bottleneck খুঁজব। JOIN columns এ Index আছে কিনা দেখব। Report যদি রিয়েলটাইম না হয় — Materialized/Summary table তৈরি করব (nightly job দিয়ে pre-computed data store)। Redis cache ব্যবহার করব (TTL: 5-15 মিনিট)। SELECT শুধু দরকারি columns। Subquery → JOIN এ রূপান্তর।

---

**Q42: Database এ লক্ষ লক্ষ rows delete করতে হবে। কীভাবে করবেন?**

> **উত্তর:** একবারে `DELETE FROM logs WHERE created_at < '2025-01-01'` করলে table lock হবে, replication lag বাড়বে। সঠিক উপায়: batch এ delete করুন:
> ```sql
> DELETE FROM logs WHERE created_at < '2025-01-01' LIMIT 1000;
> -- কিছুক্ষণ wait করুন (SLEEP বা application loop)
> -- আবার run করুন যতক্ষণ ROW_COUNT() = 0
> ```
> অথবা Partitioned table হলে `ALTER TABLE logs DROP PARTITION p2024` — instant!

---

**Q43: সব employees এবং তাদের সর্বোচ্চ salary দেওয়া project এর নাম দেখাতে চাই। Query লিখুন।**

```sql
SELECT
    e.name AS employee_name,
    p.title AS top_project,
    ep.salary AS project_salary
FROM employees e
INNER JOIN (
    -- প্রতিটি employee এর সর্বোচ্চ project salary
    SELECT emp_id, MAX(salary) AS max_salary
    FROM employee_projects
    GROUP BY emp_id
) AS max_ep ON e.emp_id = max_ep.emp_id
INNER JOIN employee_projects ep
    ON ep.emp_id = e.emp_id AND ep.salary = max_ep.max_salary
INNER JOIN projects p ON ep.project_id = p.project_id
ORDER BY e.name;
```

---

**Q44: Department এর মধ্যে সর্বোচ্চ salary পাওয়া employee এর নাম বের করুন।**

```sql
-- Method 1: Subquery
SELECT e.name, e.salary, d.dept_name
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id
WHERE e.salary = (
    SELECT MAX(salary) FROM employees WHERE dept_id = e.dept_id
);

-- Method 2: Window Function (দ্রুত ও elegant)
WITH ranked AS (
    SELECT name, salary, dept_id,
           RANK() OVER (PARTITION BY dept_id ORDER BY salary DESC) AS rnk
    FROM employees
)
SELECT r.name, r.salary, d.dept_name
FROM ranked r
INNER JOIN departments d ON r.dept_id = d.dept_id
WHERE r.rnk = 1;
```

---

**Q45: Employee এর salary এর running total (cumulative sum) বের করুন।**

```sql
SELECT
    name,
    salary,
    dept_id,
    SUM(salary) OVER (
        PARTITION BY dept_id
        ORDER BY emp_id
        ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW
    ) AS running_total
FROM employees
ORDER BY dept_id, emp_id;
```

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৭ বাংলাদেশি কোম্পানির বাস্তব প্রশ্ন

> এই section এ বাংলাদেশের real interview এ জিজ্ঞেস করা প্রশ্নগুলো সংকলন করা হয়েছে।

---

**Q46: "আপনি কোন database ব্যবহার করেছেন? কেন MySQL বেছে নিয়েছিলেন?"**

> **আদর্শ উত্তর:** "আমি MySQL ও PostgreSQL দুটোই ব্যবহার করেছি। MySQL বেছে নিয়েছিলাম কারণ — ব্যাপক community support, Laravel/Django এর সাথে excellent integration, performance ভালো, এবং hosting সহজলভ্য। PostgreSQL বেছে নিতাম যদি Advanced JSON operations, Full-text search, বা WINDOW functions এর complex use case থাকত।"

---

**Q47: "JOIN ছাড়া কি দুটো table এর data একসাথে দেখানো যায়?"**

> **উত্তর:** হ্যাঁ — Subquery দিয়ে: `SELECT name, (SELECT dept_name FROM departments WHERE dept_id = e.dept_id) FROM employees e`। তবে এটি Correlated Subquery — প্রতিটি row এ inner query চলে — JOIN এর চেয়ে ধীর। UNION দিয়েও আলাদা result sets combine করা যায় কিন্তু JOIN এর বিকল্প নয়।

---

**Q48: "আপনার project এ database optimization করেছেন? কীভাবে?"**

> **আদর্শ উত্তর:** "হ্যাঁ। প্রথমে slow queries EXPLAIN দিয়ে analyze করেছিলাম। একটি report query তে full table scan হচ্ছিল — WHERE clause এর columns এ Index দেওয়ার পর query time 3 seconds থেকে 200ms এ নেমে আসে। এছাড়া N+1 problem ছিল — ORM এ select_related() ব্যবহার করে 50টি query কে 2টিতে reduce করেছিলাম। Dashboard এর জন্য Redis caching যোগ করেছিলাম।"

---

**Q49: "MySQL এবং MongoDB এর মধ্যে কোনটি বেছে নেবেন এবং কেন?"**

> **উত্তর:** Project এর nature এর উপর নির্ভর করে। **MySQL বেছে নেব:** structured data, complex relationships, ACID transactions, financial data, e-commerce। **MongoDB বেছে নেব:** flexible schema (document structure বারবার পরিবর্তন হয়), high write throughput, horizontal scaling দরকার, JSON-like data (product catalog with varying attributes)। Real project এ প্রায়ই দুটোই একসাথে ব্যবহার হয়।

---

**Q50: "Indexes সবসময় দেওয়া উচিত — এটি কি সত্য?"**

> **উত্তর:** না, সবসময় নয়। Index READ দ্রুত করে কিন্তু WRITE ধীর করে (প্রতিটি INSERT/UPDATE/DELETE এ index ও update)। কম দেওয়া উচিত: ছোট table (< 1000 rows, full scan দ্রুত), write-heavy table, low cardinality column (gender: শুধু M/F), LIKE '%keyword' pattern এ। সঠিক columns এ সঠিক index দিন — অতিরিক্ত index overhead।

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৮ Database Cheat Sheet

### SQL Commands Quick Reference

```sql
-- ══════════════════════════════════════════════
-- DDL (Data Definition Language)
-- ══════════════════════════════════════════════
CREATE TABLE table_name (col1 TYPE CONSTRAINTS, ...);
ALTER TABLE table_name ADD COLUMN col TYPE;
ALTER TABLE table_name DROP COLUMN col;
ALTER TABLE table_name MODIFY COLUMN col NEW_TYPE;
DROP TABLE IF EXISTS table_name;
TRUNCATE TABLE table_name;

-- ══════════════════════════════════════════════
-- DML (Data Manipulation Language)
-- ══════════════════════════════════════════════
INSERT INTO table (col1, col2) VALUES (v1, v2);
INSERT INTO table (col1, col2) SELECT c1, c2 FROM other;
UPDATE table SET col1 = v1 WHERE condition;
DELETE FROM table WHERE condition;

-- ══════════════════════════════════════════════
-- DQL (Data Query Language)
-- ══════════════════════════════════════════════
SELECT [DISTINCT] cols
FROM   table1
[JOIN  table2 ON condition]
WHERE  condition
GROUP BY col
HAVING aggregate_condition
ORDER BY col [ASC|DESC]
LIMIT  n OFFSET m;

-- ══════════════════════════════════════════════
-- TCL (Transaction Control Language)
-- ══════════════════════════════════════════════
START TRANSACTION;
SAVEPOINT sp1;
ROLLBACK TO SAVEPOINT sp1;
COMMIT;
ROLLBACK;

-- ══════════════════════════════════════════════
-- DCL (Data Control Language)
-- ══════════════════════════════════════════════
GRANT SELECT, INSERT ON db.table TO 'user'@'host';
REVOKE DELETE ON db.* FROM 'user'@'host';
```

### JOIN Visual Reference

```
employees (e)          departments (d)
┌────┬───────┬─────┐   ┌─────┬──────────┐
│ id │ name  │d_id │   │ id  │ name     │
├────┼───────┼─────┤   ├─────┼──────────┤
│ 1  │ Karim │ 1   │   │ 1   │ Engg     │
│ 2  │ Rafi  │ 2   │   │ 2   │ HR       │
│ 3  │ Sumi  │ NULL│   │ 3   │ Finance  │
└────┴───────┴─────┘   └─────┴──────────┘

INNER JOIN:  Karim(Engg), Rafi(HR)           [match only]
LEFT JOIN:   Karim(Engg), Rafi(HR), Sumi(NULL) [all left]
RIGHT JOIN:  Karim(Engg), Rafi(HR), NULL(Finance) [all right]
FULL JOIN:   Karim, Rafi, Sumi(NULL), NULL(Finance) [all]
```

### Normal Forms Quick Reference

```
1NF → Atomic values, no lists, no repeating groups
2NF → 1NF + No Partial Dependency (Composite PK only)
3NF → 2NF + No Transitive Dependency
BCNF→ 3NF + Every determinant is a Superkey

মনে রাখুন: "The key, the whole key, nothing but the key"
```

### Index Decision Guide

```
দিন ✅                     দেবেন না ❌
─────────────────────────  ──────────────────────────
WHERE এ বারবার ব্যবহৃত     ছোট table (< 1000 rows)
JOIN এর ON column (FK)     Write-heavy table
ORDER BY column            Low cardinality (gender)
UNIQUE column              LIKE '%keyword' pattern
                           বহু index আছে এমন table
```

### Isolation Levels Summary

```
Level               Dirty  Non-Rep  Phantom  Speed
──────────────────  ─────  ───────  ───────  ─────
READ UNCOMMITTED    ✅      ✅        ✅      ⚡⚡⚡⚡
READ COMMITTED      ❌      ✅        ✅      ⚡⚡⚡
REPEATABLE READ*    ❌      ❌        ✅      ⚡⚡
SERIALIZABLE        ❌      ❌        ❌      ⚡
(* MySQL default)
```

### ACID মনে রাখার Trick

```
A — All or Nothing    (Atomicity)
C — Consistent state  (Consistency)
I — Invisible to others (Isolation)
D — Durable forever   (Durability)
```

### Common MySQL Commands

```sql
-- Database management
SHOW DATABASES;
CREATE DATABASE db_name CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
USE db_name;
DROP DATABASE db_name;

-- Table info
SHOW TABLES;
DESCRIBE employees;
SHOW CREATE TABLE employees;
SHOW INDEX FROM employees;

-- User & Permission
CREATE USER 'user'@'localhost' IDENTIFIED BY 'password';
GRANT ALL ON db.* TO 'user'@'localhost';
SHOW GRANTS FOR 'user'@'localhost';
REVOKE ALL ON db.* FROM 'user'@'localhost';
DROP USER 'user'@'localhost';

-- Performance
EXPLAIN SELECT ...;
EXPLAIN ANALYZE SELECT ...;     -- MySQL 8.0+
SHOW PROCESSLIST;               -- Current connections
SHOW STATUS LIKE 'Questions';   -- Server statistics
SET GLOBAL slow_query_log = 1;  -- Enable slow query log

-- Backup
mysqldump -u root -p db_name > backup.sql
mysql -u root -p db_name < backup.sql
```

### Interview এর আগে যা মনে রাখবেন

```
📌 মূল বিষয়গুলো:
✅ JOIN types ও কখন কোনটি (INNER, LEFT, RIGHT, FULL)
✅ GROUP BY + HAVING vs WHERE
✅ Index কী, কখন দেব/দেব না
✅ ACID Properties — উদাহরণসহ
✅ Transaction — COMMIT, ROLLBACK, SAVEPOINT
✅ Normalization — 1NF, 2NF, 3NF examples
✅ Primary Key vs Foreign Key
✅ NULL এর বিশেষত্ব
✅ DELETE vs TRUNCATE vs DROP
✅ Stored Procedure vs Function
✅ View — কী, কেন, সীমাবদ্ধতা
✅ Deadlock — কী, কীভাবে হয়, prevention
✅ N+1 Problem — কী, সমাধান
✅ EXPLAIN output পড়া
✅ CHAR vs VARCHAR, DECIMAL vs FLOAT

📌 Bonus (Senior impression):
✅ Window Functions (RANK, ROW_NUMBER, SUM OVER)
✅ Cursor-based Pagination
✅ Connection Pooling
✅ Replication vs Partitioning vs Sharding
✅ Isolation Levels
```

---

> **⚠️ PART 6 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

*হ্যান্ডবুক তৈরিতে: Senior Database Engineer & Backend Architect*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 9 | চলমান — PART 6 সম্পন্ন*


<a id="part7"></a>

# PART 7: Language & Framework Database Integration (ভাষা ও ফ্রেমওয়ার্ক)

> **📍 এই PART এর Sections:** [৭.১ PHP & MySQL](#৭১-php-ও-mysql) · [৭.২ Laravel Eloquent](#৭২-laravel-database-eloquent--query-builder) · [৭.৩ Python & MySQL](#৭৩-python-ও-mysql) · [৭.৪ Django ORM](#৭৪-django-orm--বিস্তারিত)

> **ব্যবহারের নিয়ম:** এই PART টি real project এ বিভিন্ন programming language দিয়ে database এর সাথে কীভাবে কাজ করতে হয় তা দেখায়। বাংলাদেশের interview এ সাধারণত PHP/Laravel অথবা Python/Django অথবা Node.js জিজ্ঞেস করা হয়। আপনি যে framework ব্যবহার করেন সেটির section বিশেষভাবে পড়ুন।

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.১ PHP ও MySQL

### PDO দিয়ে MySQL Connection

```php
<?php
// config/database.php
define('DB_HOST', 'localhost');
define('DB_USER', 'app_user');
define('DB_PASS', 'secret');
define('DB_NAME', 'company_db');

function getConnection(): PDO {
    static $pdo = null;
    if ($pdo === null) {
        $dsn = "mysql:host=" . DB_HOST . ";dbname=" . DB_NAME . ";charset=utf8mb4";
        $options = [
            PDO::ATTR_ERRMODE            => PDO::ERRMODE_EXCEPTION,
            PDO::ATTR_DEFAULT_FETCH_MODE => PDO::FETCH_ASSOC,
            PDO::ATTR_EMULATE_PREPARES   => false,  // Real prepared statements
        ];
        $pdo = new PDO($dsn, DB_USER, DB_PASS, $options);
    }
    return $pdo;
}
```

### CRUD Operations (PDO)

```php
// ✅ Parameterized Query — SQL Injection safe
$pdo = getConnection();

// SELECT
$stmt = $pdo->prepare("SELECT * FROM employees WHERE dept_id = ? AND salary > ?");
$stmt->execute([$dept_id, $min_salary]);
$employees = $stmt->fetchAll();

// Named parameters (cleaner)
$stmt = $pdo->prepare(
    "SELECT name, salary FROM employees WHERE dept_id = :dept AND is_active = :active"
);
$stmt->execute([':dept' => $dept_id, ':active' => 1]);
$employees = $stmt->fetchAll(PDO::FETCH_ASSOC);

// INSERT
$stmt = $pdo->prepare(
    "INSERT INTO employees (name, email, salary, dept_id) VALUES (?, ?, ?, ?)"
);
$stmt->execute([$name, $email, $salary, $dept_id]);
$new_id = $pdo->lastInsertId();

// UPDATE
$stmt = $pdo->prepare("UPDATE employees SET salary = ? WHERE emp_id = ?");
$stmt->execute([$new_salary, $emp_id]);
$affected = $stmt->rowCount();

// DELETE (Soft)
$stmt = $pdo->prepare(
    "UPDATE employees SET is_deleted = 1, deleted_at = NOW() WHERE emp_id = ?"
);
$stmt->execute([$emp_id]);

// Transaction
try {
    $pdo->beginTransaction();

    $stmt = $pdo->prepare("UPDATE accounts SET balance = balance - ? WHERE id = ?");
    $stmt->execute([$amount, $from_id]);

    $stmt = $pdo->prepare("UPDATE accounts SET balance = balance + ? WHERE id = ?");
    $stmt->execute([$amount, $to_id]);

    $pdo->commit();
} catch (Exception $e) {
    $pdo->rollBack();
    throw $e;
}
```

### MySQLi (Alternative)

```php
// MySQLi — PHP এর older style, এখনও ব্যবহৃত
$conn = new mysqli('localhost', 'user', 'pass', 'company_db');
$conn->set_charset('utf8mb4');

// Prepared Statement
$stmt = $conn->prepare("SELECT * FROM employees WHERE dept_id = ?");
$stmt->bind_param("i", $dept_id);  // "i" = integer, "s" = string, "d" = double
$stmt->execute();
$result = $stmt->get_result();
$employees = $result->fetch_all(MYSQLI_ASSOC);
$stmt->close();
$conn->close();
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.২ Laravel Database (Eloquent & Query Builder)

### Database Configuration

```php
// .env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=company_db
DB_USERNAME=app_user
DB_PASSWORD=secret

// config/database.php (auto-reads from .env)
'mysql' => [
    'driver'    => 'mysql',
    'host'      => env('DB_HOST', '127.0.0.1'),
    'database'  => env('DB_DATABASE', 'forge'),
    'username'  => env('DB_USERNAME', 'forge'),
    'password'  => env('DB_PASSWORD', ''),
    'charset'   => 'utf8mb4',
    'collation' => 'utf8mb4_unicode_ci',
    'strict'    => true,
],
```

### Eloquent ORM

```php
// app/Models/Employee.php
namespace App\Models;

use Illuminate\Database\Eloquent\Model;
use Illuminate\Database\Eloquent\SoftDeletes;

class Employee extends Model {
    use SoftDeletes;  // is_deleted column ব্যবহার করে

    protected $table    = 'employees';
    protected $fillable = ['name', 'email', 'salary', 'dept_id'];
    protected $hidden   = ['password'];
    protected $casts    = ['salary' => 'decimal:2', 'is_active' => 'boolean'];

    // Relationship
    public function department() {
        return $this->belongsTo(Department::class, 'dept_id');
    }

    public function projects() {
        return $this->belongsToMany(Project::class, 'employee_projects')
                    ->withPivot('role', 'joined_at');
    }
}

// ── Eloquent Queries ──────────────────────────
// SELECT all
$employees = Employee::all();

// WHERE + ORDER
$topPaid = Employee::where('salary', '>', 60000)
                   ->orderBy('salary', 'desc')
                   ->limit(10)
                   ->get();

// Eager Loading (N+1 solve)
$employees = Employee::with('department')->get();
$employees = Employee::with(['department', 'projects'])->get();

// Aggregates
$avg = Employee::where('dept_id', 1)->avg('salary');
$count = Employee::where('is_active', true)->count();

// CREATE
$emp = Employee::create([
    'name'    => 'Karim',
    'email'   => 'karim@example.com',
    'salary'  => 75000,
    'dept_id' => 1,
]);

// UPDATE
Employee::where('dept_id', 1)->update(['salary' => DB::raw('salary * 1.10')]);

// Soft Delete
$emp->delete();          // is_deleted flag set
Employee::withTrashed()->find($id);   // deleted সহ
Employee::onlyTrashed()->get();        // শুধু deleted
$emp->restore();         // restore

// Scopes
class Employee extends Model {
    public function scopeActive($query) {
        return $query->where('is_active', true);
    }
    public function scopeInDept($query, $deptId) {
        return $query->where('dept_id', $deptId);
    }
}
// Usage:
Employee::active()->inDept(1)->get();
```

### Query Builder

```php
use Illuminate\Support\Facades\DB;

// Raw query builder (non-ORM)
$employees = DB::table('employees')
    ->select('employees.name', 'departments.dept_name', 'employees.salary')
    ->join('departments', 'employees.dept_id', '=', 'departments.dept_id')
    ->where('employees.salary', '>', 60000)
    ->whereNotNull('employees.email')
    ->orderBy('salary', 'desc')
    ->paginate(20);

// Raw SQL (complex query)
$stats = DB::select('
    SELECT d.dept_name, COUNT(e.emp_id) AS total, AVG(e.salary) AS avg_salary
    FROM departments d
    LEFT JOIN employees e ON d.dept_id = e.dept_id
    GROUP BY d.dept_id
    HAVING COUNT(e.emp_id) > ?
', [3]);

// Transaction
DB::transaction(function () use ($amount, $from, $to) {
    DB::table('accounts')->where('id', $from)->decrement('balance', $amount);
    DB::table('accounts')->where('id', $to)->increment('balance', $amount);
});

// চেষ্টার সংখ্যা সহ
DB::transaction(function () { /* ... */ }, 3);  // ৩ বার retry
```

### Laravel Migration

```php
// database/migrations/2026_05_10_create_employees_table.php
use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;
use Illuminate\Support\Facades\Schema;

class CreateEmployeesTable extends Migration {
    public function up() {
        Schema::create('employees', function (Blueprint $table) {
            $table->id();                           // BIGINT UNSIGNED AUTO_INCREMENT PK
            $table->string('name', 100);
            $table->string('email', 150)->unique();
            $table->decimal('salary', 10, 2)->default(0);
            $table->foreignId('dept_id')
                  ->nullable()
                  ->constrained('departments')      // FK automatically
                  ->nullOnDelete();
            $table->boolean('is_active')->default(true);
            $table->timestamps();                   // created_at + updated_at
            $table->softDeletes();                  // deleted_at column
        });
    }

    public function down() {
        Schema::dropIfExists('employees');
    }
}

// Migration commands
// php artisan make:migration create_employees_table
// php artisan migrate
// php artisan migrate:rollback
// php artisan migrate:status
// php artisan migrate:fresh --seed   (সব drop করে নতুন করে + seed)
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৩ Python ও MySQL

### mysql-connector-python

```python
import mysql.connector
from contextlib import contextmanager

# Connection config
DB_CONFIG = {
    'host':     'localhost',
    'user':     'app_user',
    'password': 'secret',
    'database': 'company_db',
    'charset':  'utf8mb4',
}

@contextmanager
def get_cursor():
    """Context manager — auto-close connection"""
    conn = mysql.connector.connect(**DB_CONFIG)
    cursor = conn.cursor(dictionary=True)  # dict rows
    try:
        yield conn, cursor
        conn.commit()
    except Exception:
        conn.rollback()
        raise
    finally:
        cursor.close()
        conn.close()

# SELECT
def get_employees_by_dept(dept_id: int) -> list:
    with get_cursor() as (conn, cur):
        cur.execute(
            "SELECT emp_id, name, salary FROM employees WHERE dept_id = %s AND is_active = 1",
            (dept_id,)  # tuple — always use parameterized!
        )
        return cur.fetchall()

# INSERT
def create_employee(name: str, email: str, salary: float, dept_id: int) -> int:
    with get_cursor() as (conn, cur):
        cur.execute(
            "INSERT INTO employees (name, email, salary, dept_id) VALUES (%s, %s, %s, %s)",
            (name, email, salary, dept_id)
        )
        return cur.lastrowid

# UPDATE
def update_salary(emp_id: int, new_salary: float) -> int:
    with get_cursor() as (conn, cur):
        cur.execute(
            "UPDATE employees SET salary = %s WHERE emp_id = %s",
            (new_salary, emp_id)
        )
        return cur.rowcount

# Transaction
def transfer_funds(from_id: int, to_id: int, amount: float) -> None:
    conn = mysql.connector.connect(**DB_CONFIG)
    cur = conn.cursor()
    try:
        conn.start_transaction()
        cur.execute("UPDATE accounts SET balance = balance - %s WHERE id = %s", (amount, from_id))
        cur.execute("UPDATE accounts SET balance = balance + %s WHERE id = %s", (amount, to_id))
        conn.commit()
    except Exception:
        conn.rollback()
        raise
    finally:
        cur.close()
        conn.close()
```

### PyMySQL (Alternative)

```python
import pymysql

conn = pymysql.connect(
    host='localhost', user='app_user',
    password='secret', database='company_db',
    charset='utf8mb4', cursorclass=pymysql.cursors.DictCursor
)

with conn:
    with conn.cursor() as cursor:
        cursor.execute("SELECT * FROM employees WHERE dept_id = %s", (1,))
        rows = cursor.fetchall()
```

### SQLAlchemy (Python ORM)

```python
from sqlalchemy import create_engine, Column, Integer, String, Numeric, ForeignKey
from sqlalchemy.orm import declarative_base, Session, relationship

DATABASE_URL = "mysql+pymysql://app_user:secret@localhost/company_db"
engine = create_engine(DATABASE_URL, pool_size=10, pool_recycle=3600)
Base = declarative_base()

class Department(Base):
    __tablename__ = 'departments'
    dept_id   = Column(Integer, primary_key=True, autoincrement=True)
    dept_name = Column(String(100), nullable=False)
    employees = relationship('Employee', back_populates='department')

class Employee(Base):
    __tablename__ = 'employees'
    emp_id  = Column(Integer, primary_key=True, autoincrement=True)
    name    = Column(String(100), nullable=False)
    salary  = Column(Numeric(10, 2))
    dept_id = Column(Integer, ForeignKey('departments.dept_id'))
    department = relationship('Department', back_populates='employees')

# Queries
with Session(engine) as session:
    # SELECT with JOIN
    employees = (
        session.query(Employee)
        .join(Department)
        .filter(Employee.salary > 60000)
        .order_by(Employee.salary.desc())
        .all()
    )

    # INSERT
    emp = Employee(name='Karim', salary=75000, dept_id=1)
    session.add(emp)
    session.commit()

    # UPDATE
    session.query(Employee).filter_by(emp_id=1).update({'salary': 80000})
    session.commit()
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৪ Django ORM — বিস্তারিত

### Settings Configuration

```python
# settings.py
DATABASES = {
    'default': {
        'ENGINE':   'django.db.backends.mysql',
        'NAME':     os.environ.get('DB_NAME', 'company_db'),
        'USER':     os.environ.get('DB_USER', 'app_user'),
        'PASSWORD': os.environ.get('DB_PASSWORD', ''),
        'HOST':     os.environ.get('DB_HOST', 'localhost'),
        'PORT':     os.environ.get('DB_PORT', '3306'),
        'OPTIONS': {
            'charset': 'utf8mb4',
            'init_command': "SET sql_mode='STRICT_TRANS_TABLES'",
        },
        'CONN_MAX_AGE': 60,  # Connection pooling — 60s reuse
    }
}
```

### Advanced Django ORM

```python
from django.db import models
from django.db.models import Avg, Count, Max, Min, Sum, F, Q, Subquery, OuterRef

class Department(models.Model):
    dept_name  = models.CharField(max_length=100)
    class Meta:
        db_table = 'departments'

class Employee(models.Model):
    name      = models.CharField(max_length=100)
    email     = models.EmailField(unique=True)
    salary    = models.DecimalField(max_digits=10, decimal_places=2)
    dept      = models.ForeignKey(Department, on_delete=models.SET_NULL, null=True)
    is_active = models.BooleanField(default=True)
    join_date = models.DateField(auto_now_add=True)

    class Meta:
        db_table = 'employees'

# ── Advanced Queries ─────────────────────────────

# F() — column reference (atomic update, no race condition)
Employee.objects.filter(dept_id=1).update(salary=F('salary') * 1.10)

# Q() — complex OR/AND conditions
from django.db.models import Q
employees = Employee.objects.filter(
    Q(salary__gt=80000) | Q(dept__dept_name='Engineering'),
    is_active=True  # AND
)

# Aggregation
from django.db.models import Avg, Count
stats = Department.objects.annotate(
    emp_count=Count('employee'),
    avg_salary=Avg('employee__salary'),
    max_salary=Max('employee__salary')
).filter(emp_count__gt=2)

# Subquery
from django.db.models import Subquery, OuterRef
top_salary = Employee.objects.filter(
    dept=OuterRef('pk')
).order_by('-salary').values('salary')[:1]

depts = Department.objects.annotate(top_earner_salary=Subquery(top_salary))

# Raw SQL in Django
employees = Employee.objects.raw(
    "SELECT * FROM employees WHERE salary > %s ORDER BY salary DESC",
    [60000]
)

# Extra complex: cursor
from django.db import connection
with connection.cursor() as cursor:
    cursor.execute("""
        SELECT d.dept_name, COUNT(e.id) as total, AVG(e.salary) as avg_sal
        FROM departments d
        LEFT JOIN employees e ON d.id = e.dept_id
        GROUP BY d.id
    """)
    rows = cursor.fetchall()

# select_related vs prefetch_related
# 1:1 বা FK (forward): select_related → JOIN
employees = Employee.objects.select_related('dept').all()

# Reverse FK বা M:N: prefetch_related → separate query
departments = Department.objects.prefetch_related('employee_set').all()

# only() — শুধু নির্দিষ্ট columns
employees = Employee.objects.only('name', 'salary')

# defer() — নির্দিষ্ট columns বাদ দিয়ে
employees = Employee.objects.defer('bio', 'notes')

# values() — dict return
Employee.objects.values('name', 'salary').filter(dept_id=1)

# values_list() — tuple return
Employee.objects.values_list('name', 'salary', flat=False)
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৫ Node.js ও MySQL

### mysql2 (Promise-based)

```javascript
const mysql = require('mysql2/promise');

// Connection Pool
const pool = mysql.createPool({
    host:            process.env.DB_HOST || 'localhost',
    user:            process.env.DB_USER || 'app_user',
    password:        process.env.DB_PASSWORD || '',
    database:        process.env.DB_NAME || 'company_db',
    connectionLimit: 10,
    waitForConnections: true,
    charset:         'utf8mb4',
});

// ── CRUD ─────────────────────────────────────────

// SELECT (parameterized — SQL injection safe)
async function getEmployeesByDept(deptId) {
    const [rows] = await pool.query(
        'SELECT emp_id, name, salary FROM employees WHERE dept_id = ? AND is_active = 1',
        [deptId]
    );
    return rows;
}

// INSERT
async function createEmployee(name, email, salary, deptId) {
    const [result] = await pool.execute(
        'INSERT INTO employees (name, email, salary, dept_id) VALUES (?, ?, ?, ?)',
        [name, email, salary, deptId]
    );
    return result.insertId;
}

// UPDATE
async function updateSalary(empId, newSalary) {
    const [result] = await pool.execute(
        'UPDATE employees SET salary = ? WHERE emp_id = ?',
        [newSalary, empId]
    );
    return result.affectedRows;
}

// Transaction
async function transferFunds(fromId, toId, amount) {
    const conn = await pool.getConnection();
    try {
        await conn.beginTransaction();

        await conn.execute(
            'UPDATE accounts SET balance = balance - ? WHERE id = ?',
            [amount, fromId]
        );
        await conn.execute(
            'UPDATE accounts SET balance = balance + ? WHERE id = ?',
            [amount, toId]
        );

        await conn.commit();
    } catch (err) {
        await conn.rollback();
        throw err;
    } finally {
        conn.release();  // Pool এ ফেরত
    }
}
```

### Prisma ORM (Modern Node.js)

```javascript
// schema.prisma
datasource db {
  provider = "mysql"
  url      = env("DATABASE_URL")
}

model Employee {
  emp_id    Int        @id @default(autoincrement())
  name      String     @db.VarChar(100)
  email     String     @unique @db.VarChar(150)
  salary    Decimal    @db.Decimal(10, 2)
  dept_id   Int?
  is_active Boolean    @default(true)
  dept      Department? @relation(fields: [dept_id], references: [dept_id])

  @@map("employees")
}

// queries
const { PrismaClient } = require('@prisma/client');
const prisma = new PrismaClient();

// SELECT with relation
const employees = await prisma.employee.findMany({
    where:   { salary: { gt: 60000 }, is_active: true },
    include: { dept: true },           // JOIN (N+1 safe)
    orderBy: { salary: 'desc' },
    take:    10,
});

// CREATE
const emp = await prisma.employee.create({
    data: { name: 'Karim', email: 'karim@example.com', salary: 75000, dept_id: 1 }
});

// UPDATE
await prisma.employee.update({
    where: { emp_id: 1 },
    data:  { salary: 80000 },
});

// Transaction
await prisma.$transaction([
    prisma.account.update({ where: { id: fromId }, data: { balance: { decrement: amount } } }),
    prisma.account.update({ where: { id: toId },   data: { balance: { increment: amount } } }),
]);
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৬ Environment Configuration & Security

### .env ফাইল ব্যবহার

```bash
# .env (কখনো Git এ push করবেন না!)
DB_HOST=localhost
DB_PORT=3306
DB_NAME=company_db
DB_USER=app_user
DB_PASSWORD=your_strong_password_here
DB_POOL_SIZE=10

# .gitignore তে যোগ করুন:
.env
*.env
.env.local
.env.production
```

```python
# Python — python-dotenv
from dotenv import load_dotenv
import os

load_dotenv()  # .env ফাইল load করে

DB_CONFIG = {
    'host':     os.getenv('DB_HOST', 'localhost'),
    'user':     os.getenv('DB_USER'),
    'password': os.getenv('DB_PASSWORD'),
    'database': os.getenv('DB_NAME'),
}
```

```javascript
// Node.js — dotenv
require('dotenv').config();

const pool = mysql.createPool({
    host:     process.env.DB_HOST,
    user:     process.env.DB_USER,
    password: process.env.DB_PASSWORD,
    database: process.env.DB_NAME,
});
```

```php
// PHP — vlucas/phpdotenv
$dotenv = Dotenv\Dotenv::createImmutable(__DIR__);
$dotenv->load();
$dotenv->required(['DB_HOST', 'DB_NAME', 'DB_USER', 'DB_PASSWORD']);

$host = $_ENV['DB_HOST'];
$user = $_ENV['DB_USER'];
```

### Production Security Checklist

```
✅ Database Connection Security:
  → .env file কখনো Git এ push করবেন না
  → .gitignore তে .env যোগ করুন
  → Production এ environment variables ব্যবহার করুন (না .env file)
  → SSL/TLS দিয়ে DB connection encrypt করুন

✅ User Permissions:
  → App user: SELECT, INSERT, UPDATE only
  → No DROP, ALTER, CREATE for app user
  → Read-only user for reporting
  → Root user শুধু admin কাজে

✅ Network:
  → DB server publicly accessible রাখবেন না
  → Firewall দিয়ে শুধু app server IP allow করুন
  → VPC/Private network এ DB রাখুন

✅ Passwords:
  → Strong password (20+ chars, mixed)
  → Password manager ব্যবহার করুন
  → Regular rotation
  → User password bcrypt/argon2 hash করুন
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৭ Database Testing

### Unit Testing — Mock Database

```python
# Python — pytest + unittest.mock
import pytest
from unittest.mock import patch, MagicMock

def get_employee(emp_id: int) -> dict:
    with get_cursor() as (conn, cur):
        cur.execute("SELECT * FROM employees WHERE emp_id = %s", (emp_id,))
        return cur.fetchone()

# Test with mock (actual DB hit নেই)
@patch('myapp.db.get_cursor')
def test_get_employee(mock_cursor_ctx):
    mock_conn = MagicMock()
    mock_cur  = MagicMock()
    mock_cur.fetchone.return_value = {'emp_id': 1, 'name': 'Karim', 'salary': 75000}
    mock_cursor_ctx.return_value.__enter__.return_value = (mock_conn, mock_cur)

    result = get_employee(1)
    assert result['name'] == 'Karim'
    mock_cur.execute.assert_called_once()
```

### Django Test Database

```python
# Django automatically creates a test DB (test_company_db)
# python manage.py test

from django.test import TestCase
from myapp.models import Employee, Department

class EmployeeModelTest(TestCase):
    def setUp(self):
        # প্রতিটি test এর আগে fresh data
        self.dept = Department.objects.create(dept_name='Engineering')
        self.emp  = Employee.objects.create(
            name='Karim', email='karim@test.com',
            salary=75000, dept=self.dept
        )

    def test_employee_creation(self):
        self.assertEqual(self.emp.name, 'Karim')
        self.assertEqual(Employee.objects.count(), 1)

    def test_salary_update(self):
        self.emp.salary = 85000
        self.emp.save()
        updated = Employee.objects.get(pk=self.emp.pk)
        self.assertEqual(updated.salary, 85000)

    def test_department_relation(self):
        self.assertEqual(self.emp.dept.dept_name, 'Engineering')

    def tearDown(self):
        # TestCase automatically rolls back transactions
        pass
```

### Laravel Testing

```php
// tests/Feature/EmployeeTest.php
namespace Tests\Feature;

use Tests\TestCase;
use App\Models\Employee;
use App\Models\Department;
use Illuminate\Foundation\Testing\RefreshDatabase;

class EmployeeTest extends TestCase {
    use RefreshDatabase;  // প্রতিটি test এর পর DB reset

    public function test_can_create_employee(): void {
        $dept = Department::factory()->create();

        $response = $this->postJson('/api/employees', [
            'name'    => 'Karim',
            'email'   => 'karim@example.com',
            'salary'  => 75000,
            'dept_id' => $dept->id,
        ]);

        $response->assertStatus(201);
        $this->assertDatabaseHas('employees', ['email' => 'karim@example.com']);
    }

    public function test_salary_must_be_positive(): void {
        $response = $this->postJson('/api/employees', [
            'name'   => 'Test',
            'salary' => -1000,  // invalid
        ]);
        $response->assertStatus(422);  // Validation error
    }
}
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৮ PART 7 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: Laravel এ Eloquent এবং Query Builder এর মধ্যে পার্থক্য কী?**

> **উত্তর:** Eloquent হলো Laravel এর Full ORM — Model class দিয়ে কাজ করে, relationships (belongsTo, hasMany, belongsToMany) automatically manage করে, Model events (creating, created, updated) fire করে। Query Builder হলো Fluent SQL Builder — Model ছাড়া `DB::table()` দিয়ে SQL-like syntax এ query করা যায়। Eloquent overhead বেশি কিন্তু features বেশি। Raw performance দরকার হলে Query Builder বা Raw SQL।

---

**Q2: Django ORM এ select_related() এবং prefetch_related() কখন কোনটি?**

> **উত্তর:** `select_related()`: FK বা OneToOne forward relationship এ — SQL JOIN করে এক query তে আনে। `prefetch_related()`: Reverse FK (employee.project_set) বা ManyToMany এ — আলাদা query চালায় তারপর Python এ merge করে। Rule: FK → select_related, M:N বা Reverse → prefetch_related। দুটোই N+1 সমস্যা সমাধান করে।

---

**Q3: PHP তে PDO এবং MySQLi এর মধ্যে পার্থক্য?**

> **উত্তর:** PDO: Database Agnostic — MySQL, PostgreSQL, SQLite সব এ কাজ করে, শুধু DSN change করলেই। Named parameters support করে। MySQLi: শুধু MySQL, slightly faster কারণ MySQL-specific। দুটোই Prepared Statement support করে (SQL Injection safe)। New project এ PDO prefer করুন — database change করলে কোড পরিবর্তন কম।

---

**Q4: ORM এ F() object কী? কেন দরকার?**

> **উত্তর:** Django এর `F()` object database column কে Python এ না এনে সরাসরি database এ reference করে। `Employee.objects.update(salary=F('salary') * 1.10)` — একটি UPDATE query তে হয়, Python এ read → calculate → write করতে হয় না। Race condition avoid করে — concurrent update এ correct।

---

**Q5: Node.js এ connection.release() কেন গুরুত্বপূর্ণ?**

> **উত্তর:** Connection Pool ব্যবহার করলে প্রতিটি query এর পরে `conn.release()` না করলে connection pool এ ফেরত যায় না। Pool exhausted হয়ে নতুন requests hang করে। `finally` block এ সবসময় `release()` করুন — error হলেও। Prisma বা `pool.query()` (shorthand) ব্যবহার করলে automatically release হয়।

---

**Q6: .env ফাইল Git এ push হয়ে গেলে কী করবেন?**

> **উত্তর:** তাৎক্ষণিকভাবে: database password change করুন, Git history থেকে মুছুন (`git filter-branch` বা BFG Repo Cleaner), force push করুন। .gitignore তে .env যোগ করুন। যদি public repo হয়ে থাকে — credentials already compromised ধরে নিন। GitHub Secret Scanning alert আসতে পারে। ভবিষ্যতে: `git-secrets` বা `pre-commit` hook দিয়ে prevent করুন।

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| Laravel এ DB migration চালানো | `php artisan migrate` |
| Django ORM এ raw SQL | `Model.objects.raw()` বা `connection.cursor()` |
| PDO তে SQL injection prevent | Prepared Statement + parameterized query |
| Node.js এ transaction শেষে | `conn.release()` finally block এ |
| Django test DB | `test_` prefix এ আলাদা DB তৈরি হয় |
| Laravel এ soft delete trait | `use SoftDeletes` |
| Django এ F() কী করে? | DB column কে Python না এনে DB তে calculate |
| Prisma কী? | Type-safe Node.js ORM |
| CONN_MAX_AGE (Django) কী? | Connection reuse timeout (pool এর মতো) |
| Laravel factory কী? | Test data generate করার tool |
| `.env` কোথায় রাখবেন না | Git repository তে |
| SQLAlchemy Session কী? | Unit of work — DB transaction wrapper |
| mysql2 vs mysql (Node) | mysql2 Promise support করে, দ্রুত |
| Django makemigrations কী করে? | Model change থেকে migration file তৈরি |

---

> **⚠️ PART 7 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

*হ্যান্ডবুক তৈরিতে: Senior Database Engineer & Backend Architect*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 9 | চলমান — PART 7 সম্পন্ন*


<a id="part8"></a>

# PART 8: NoSQL & Modern Databases

> **📍 এই PART এর Sections:** [৮.১ NoSQL কী?](#৮১-nosql-কী) · [৮.২ SQL vs NoSQL](#৮২-sql-vs-nosql) · [৮.৩ CAP Theorem](#৮৩-cap-theorem) · [৮.৪ MongoDB](#৮৪-mongodb--document-database)

> **ব্যবহারের নিয়ম:** এই PART টি NoSQL databases এর ধারণা, SQL এর সাথে তুলনা, এবং কখন কোন database ব্যবহার করতে হয় তা ব্যাখ্যা করে। বাংলাদেশের Mid/Senior level interview তে এই প্রশ্নগুলো সাধারণত জিজ্ঞেস করা হয়।

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.১ NoSQL কী?

NoSQL ("Not Only SQL") হলো এমন database systems যেগুলো traditional relational model এর বাইরে data store করে। Fixed schema নেই, horizontal scaling সহজ, এবং flexible data structures সমর্থন করে।

### NoSQL Database Types

| Type | উদাহরণ | Data Model | Best For |
|------|---------|------------|----------|
| **Document** | MongoDB, CouchDB | JSON/BSON documents | CMS, User profiles, Catalogs |
| **Key-Value** | Redis, DynamoDB | key → value | Caching, Session, Leaderboard |
| **Wide-Column** | Cassandra, HBase | Rows + dynamic columns | Time-series, IoT, Analytics |
| **Graph** | Neo4j, ArangoDB | Nodes + Edges | Social networks, Recommendation |
| **Search Engine** | Elasticsearch, Solr | Inverted index | Full-text search, Log analysis |
| **Time-Series** | InfluxDB, TimescaleDB | Timestamps + values | Monitoring, Metrics |

### NoSQL এর বৈশিষ্ট্য

```
Schema-less:     প্রতিটি document এর আলাদা structure হতে পারে
Horizontal Scale: Sharding দিয়ে হাজারো server এ ছড়িয়ে দেওয়া যায়
Eventual Consistency: সব node এ data সাথে সাথে না গেলেও eventually যায়
High Availability: Replication দিয়ে node failure সহ্য করে
```

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.২ SQL vs NoSQL

| বিষয় | SQL (Relational) | NoSQL |
|------|-----------------|-------|
| **Schema** | Fixed, strict | Flexible, schema-less |
| **Scaling** | Vertical (বড় server) | Horizontal (বেশি server) |
| **ACID** | সম্পূর্ণ ACID | সাধারণত BASE (Eventually consistent) |
| **Joins** | Complex JOINs সহজ | JOIN নেই, embedding করতে হয় |
| **Query Language** | SQL (standard) | Database-specific API |
| **Transactions** | Multi-table transactions | সীমিত (MongoDB 4+ তে আছে) |
| **Relationships** | Foreign Keys | Embedding বা Reference |
| **Best For** | Complex queries, reporting | High write volume, flexible schema |

### ACID vs BASE

```
ACID (SQL):
  Atomicity    — সব হবে অথবা কিছু হবে না
  Consistency  — Data সবসময় valid state এ
  Isolation    — Concurrent transactions আলাদা
  Durability   — Committed data হারায় না

BASE (NoSQL):
  Basically Available  — System সবসময় respond করে
  Soft state           — Data state সময়ের সাথে change হতে পারে
  Eventually Consistent — সব replica eventually agree করবে
```

### কোনটি কখন?

```
✅ SQL ব্যবহার করুন যখন:
  → Complex relationships ও JOINs দরকার
  → Strong consistency প্রয়োজন (banking, finance)
  → Data structure predictable ও stable
  → Complex reporting ও analytics

✅ NoSQL ব্যবহার করুন যখন:
  → Schema frequently change হয়
  → Massive scale (millions of writes/sec)
  → Unstructured বা semi-structured data
  → High read/write throughput দরকার
  → Distributed globally (low latency)
```

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.৩ CAP Theorem

CAP Theorem বলে: একটি distributed system এ নিচের ৩টির মধ্যে শুধু ২টি guarantee করা সম্ভব।

```
C — Consistency:    সব node এ একই সময় একই data দেখাবে
A — Availability:   সব request এ response আসবে (timeout ছাড়া)
P — Partition Tolerance: Network failure এ system চলতে থাকবে
```

**Real world এ P সবসময় দরকার** (network failure হবেই), তাই choice হলো C বা A।

| Database | ধরন | কী sacrifice করে |
|----------|-----|-----------------|
| MySQL, PostgreSQL | CA | Partition tolerance |
| MongoDB | CP | Availability |
| Cassandra | AP | Consistency |
| Redis (cluster) | CP | Availability |
| DynamoDB | AP | Consistency |

### PACELC Extension

```
If Partition: choose P → A (availability) বা P → C (consistency)
Else (normal): choose E → L (latency) বা E → C (consistency)

Example: DynamoDB → PA/EL (high availability, low latency, eventual consistency)
```

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.৪ MongoDB — Document Database

MongoDB JSON-like BSON documents এ data store করে। Schema নেই — প্রতিটি document আলাদা হতে পারে।

### Core Concepts

```
Database → Collection → Document
  (MySQL: Database → Table → Row)

Document example:
{
  "_id": ObjectId("507f1f77bcf86cd799439011"),
  "name": "Karim Ahmed",
  "email": "karim@example.com",
  "salary": 75000,
  "skills": ["Python", "MongoDB", "React"],
  "address": {
    "city": "Dhaka",
    "district": "Dhaka"
  },
  "joined_at": ISODate("2024-01-15")
}
```

### MongoDB CRUD

```javascript
// MongoDB Shell / Node.js Driver

// ── CREATE ──────────────────────────────────────────
db.employees.insertOne({
    name: "Karim", email: "karim@example.com",
    salary: 75000, dept: "Engineering", skills: ["Python", "SQL"]
});

db.employees.insertMany([
    { name: "Rahim", salary: 60000, dept: "HR" },
    { name: "Sadia", salary: 90000, dept: "Engineering" }
]);

// ── READ ────────────────────────────────────────────
db.employees.find({ dept: "Engineering" });
db.employees.find({ salary: { $gt: 70000 } });

// Multiple conditions (AND)
db.employees.find({ dept: "Engineering", salary: { $gte: 60000 } });

// OR condition
db.employees.find({ $or: [{ dept: "HR" }, { salary: { $gt: 80000 } }] });

// Projection (specific fields)
db.employees.find({ dept: "Engineering" }, { name: 1, salary: 1, _id: 0 });

// Sort, Limit, Skip
db.employees.find().sort({ salary: -1 }).limit(10).skip(20);

// ── UPDATE ──────────────────────────────────────────
// $set — নির্দিষ্ট field update
db.employees.updateOne(
    { email: "karim@example.com" },
    { $set: { salary: 85000 } }
);

// $inc — increment
db.employees.updateMany(
    { dept: "Engineering" },
    { $inc: { salary: 5000 } }
);

// $push — array তে element যোগ
db.employees.updateOne(
    { email: "karim@example.com" },
    { $push: { skills: "Docker" } }
);

// ── DELETE ──────────────────────────────────────────
db.employees.deleteOne({ email: "karim@example.com" });
db.employees.deleteMany({ dept: "Temp", salary: { $lt: 30000 } });
```

### MongoDB Aggregation Pipeline

```javascript
// SQL এর GROUP BY, JOIN এর equivalent
db.employees.aggregate([
    // Stage 1: Filter
    { $match: { salary: { $gt: 50000 } } },

    // Stage 2: Group
    { $group: {
        _id: "$dept",
        total: { $sum: 1 },
        avg_salary: { $avg: "$salary" },
        max_salary: { $max: "$salary" }
    }},

    // Stage 3: Sort
    { $sort: { avg_salary: -1 } },

    // Stage 4: Limit
    { $limit: 5 }
]);

// $lookup — JOIN equivalent
db.employees.aggregate([
    {
        $lookup: {
            from:         "departments",
            localField:   "dept_id",
            foreignField: "_id",
            as:           "department"
        }
    },
    { $unwind: "$department" },  // array → single object
    { $project: { name: 1, salary: 1, "department.name": 1 } }
]);
```

### Embedding vs Referencing

```javascript
// Embedding (denormalization) — Related data একসাথে
// Fast read, একটি query তে সব
{
    "_id": ObjectId("..."),
    "order_id": "ORD-001",
    "customer": { "name": "Karim", "email": "karim@ex.com" },
    "items": [
        { "product": "Laptop", "qty": 1, "price": 85000 },
        { "product": "Mouse",  "qty": 2, "price": 800 }
    ]
}

// Referencing — আলাদা collection এ FK এর মতো
{
    "_id": ObjectId("..."),
    "order_id": "ORD-001",
    "customer_id": ObjectId("507f..."),  // Reference
    "items": [ObjectId("aaa"), ObjectId("bbb")]
}

// Rule:
// Embed: data একসাথে read হয়, child document বেশি grow করে না
// Reference: data আলাদাভাবেও access হয়, large subdocuments
```

### MongoDB Indexing

```javascript
// Single field index
db.employees.createIndex({ email: 1 });        // 1 = ascending
db.employees.createIndex({ salary: -1 });       // -1 = descending

// Compound index
db.employees.createIndex({ dept: 1, salary: -1 });

// Unique index
db.employees.createIndex({ email: 1 }, { unique: true });

// TTL index (auto-delete after time)
db.sessions.createIndex({ created_at: 1 }, { expireAfterSeconds: 3600 });

// Text search index
db.articles.createIndex({ title: "text", content: "text" });
db.articles.find({ $text: { $search: "database optimization" } });

// Explain (query plan দেখুন)
db.employees.find({ email: "karim@ex.com" }).explain("executionStats");
```

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.৫ Redis — Key-Value Store

Redis (Remote Dictionary Server) হলো in-memory data structure store। Caching, session management, pub/sub, rate limiting এ widely ব্যবহৃত।

### Redis Data Types

```bash
# ── String ────────────────────────────────────────
SET user:1:name "Karim Ahmed"
GET user:1:name
SETEX session:abc123 3600 "user_data_json"  # 3600s TTL
INCR page:views              # atomic counter
INCRBY salary:emp1 5000

# ── Hash (Object store) ───────────────────────────
HSET employee:1 name "Karim" salary "75000" dept "Engineering"
HGET employee:1 name
HGETALL employee:1
HMSET employee:2 name "Rahim" salary "60000"
HDEL employee:1 dept

# ── List (Queue/Stack) ────────────────────────────
LPUSH job_queue "send_email"        # Left push (head)
RPUSH job_queue "resize_image"      # Right push (tail)
LPOP job_queue                      # Pop from left (FIFO queue)
BRPOP job_queue 30                  # Blocking pop (30s timeout)
LRANGE job_queue 0 -1               # All elements

# ── Set (Unique items) ────────────────────────────
SADD online_users 101 102 103
SISMEMBER online_users 101          # Check membership O(1)
SREM online_users 102
SCARD online_users                  # Count
SINTERSTORE common tags:post:1 tags:post:2  # Intersection

# ── Sorted Set (Leaderboard) ──────────────────────
ZADD leaderboard 1500 "player:1"
ZADD leaderboard 2200 "player:2"
ZADD leaderboard 1800 "player:3"
ZRANGE leaderboard 0 -1 WITHSCORES  # Ascending
ZREVRANGE leaderboard 0 2 WITHSCORES # Top 3
ZINCRBY leaderboard 500 "player:1"   # Add score
ZRANK leaderboard "player:1"         # Rank (0-based)
```

### Redis Use Cases

```python
import redis

r = redis.Redis(host='localhost', port=6379, db=0, decode_responses=True)

# ── Caching ──────────────────────────────────────
CACHE_TTL = 3600  # 1 hour

def get_employee(emp_id: int) -> dict:
    cache_key = f"employee:{emp_id}"

    # Cache check
    cached = r.get(cache_key)
    if cached:
        return json.loads(cached)

    # DB থেকে আনুন
    emp = db.query("SELECT * FROM employees WHERE emp_id = %s", (emp_id,))

    # Cache এ store করুন
    r.setex(cache_key, CACHE_TTL, json.dumps(emp))
    return emp

def update_employee(emp_id: int, data: dict) -> None:
    db.execute("UPDATE employees SET salary = %s WHERE emp_id = %s",
               (data['salary'], emp_id))
    # Cache invalidate
    r.delete(f"employee:{emp_id}")

# ── Session Management ────────────────────────────
def create_session(user_id: int) -> str:
    session_id = str(uuid.uuid4())
    r.setex(f"session:{session_id}", 86400, json.dumps({"user_id": user_id}))
    return session_id

def get_session(session_id: str) -> dict | None:
    data = r.get(f"session:{session_id}")
    return json.loads(data) if data else None

# ── Rate Limiting ─────────────────────────────────
def is_rate_limited(user_id: int, limit: int = 100) -> bool:
    key = f"rate_limit:{user_id}:{datetime.now().strftime('%Y%m%d%H')}"
    current = r.incr(key)
    if current == 1:
        r.expire(key, 3600)  # 1 hour window
    return current > limit

# ── Pub/Sub ───────────────────────────────────────
# Publisher
def publish_event(channel: str, data: dict) -> None:
    r.publish(channel, json.dumps(data))

# Subscriber
def subscribe_events(channel: str) -> None:
    pubsub = r.pubsub()
    pubsub.subscribe(channel)
    for message in pubsub.listen():
        if message['type'] == 'message':
            process(json.loads(message['data']))
```

### Redis Persistence

```
RDB (Redis Database):
  → নির্দিষ্ট সময় পর পর snapshot নেয়
  → Fast restart, কিন্তু last snapshot এর পর data হারাতে পারে
  → config: save 900 1 (900s এ অন্তত 1 change হলে)

AOF (Append Only File):
  → প্রতিটি write operation log করে
  → Slower কিন্তু data loss কম
  → fsync: always / everysec / no

Best Practice: RDB + AOF দুটোই চালু রাখুন
```

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.৬ Elasticsearch — Search Engine

Elasticsearch হলো distributed search ও analytics engine। Apache Lucene এর উপর built। Full-text search, log analysis (ELK Stack), এ widely ব্যবহৃত।

### Core Concepts

```
Index     → MySQL Table
Document  → MySQL Row  
Field     → MySQL Column
Shard     → Horizontal partition (auto-distributes)
Replica   → Shard এর copy (high availability)
```

### Basic Operations

```bash
# Index তৈরি
PUT /employees
{
  "mappings": {
    "properties": {
      "name":    { "type": "text" },
      "email":   { "type": "keyword" },
      "salary":  { "type": "double" },
      "bio":     { "type": "text", "analyzer": "standard" },
      "join_date": { "type": "date" }
    }
  }
}

# Document index করুন
POST /employees/_doc/1
{
  "name": "Karim Ahmed",
  "email": "karim@example.com",
  "salary": 75000,
  "bio": "Senior software engineer with expertise in databases"
}

# Full-text search
GET /employees/_search
{
  "query": {
    "match": { "bio": "database engineer" }
  }
}

# Multi-field search
GET /employees/_search
{
  "query": {
    "multi_match": {
      "query": "software engineer",
      "fields": ["name", "bio", "skills"]
    }
  }
}

# Bool query (complex)
GET /employees/_search
{
  "query": {
    "bool": {
      "must":   [ { "match": { "bio": "database" } } ],
      "filter": [ { "range": { "salary": { "gte": 60000 } } } ],
      "must_not": [ { "term": { "is_active": false } } ]
    }
  },
  "sort":  [ { "salary": { "order": "desc" } } ],
  "from":  0,
  "size":  10
}

# Aggregation
GET /employees/_search
{
  "aggs": {
    "by_dept": {
      "terms": { "field": "dept.keyword" },
      "aggs": {
        "avg_salary": { "avg": { "field": "salary" } }
      }
    }
  }
}
```

### MySQL + Elasticsearch (Hybrid)

```
MySQL → Primary data store (ACID, relationships)
Elasticsearch → Search index (full-text, fast lookup)

Sync pattern:
  1. MySQL তে data write
  2. Message Queue (RabbitMQ/Kafka) এ event পাঠান
  3. Consumer ES এ index করে
  4. Search request → ES, Detail request → MySQL
```

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.৭ Cassandra — Wide-Column Store

Apache Cassandra একটি distributed NoSQL database। Extremely high write throughput এবং geographic distribution এর জন্য ডিজাইন করা হয়েছে।

### Key Characteristics

```
Masterless Architecture: কোনো single point of failure নেই
Write-optimized: Writes অত্যন্ত দ্রুত (log-structured)
Partition Key: Data কোন node এ যাবে তা নির্ধারণ করে
Clustering Key: Partition এর ভেতরে sort order
Tunable Consistency: প্রতি query তে consistency level set করা যায়
```

### CQL (Cassandra Query Language)

```sql
-- Table তৈরি (Primary key design critical!)
CREATE TABLE employee_activity (
    dept_id    UUID,
    recorded_at TIMESTAMP,
    emp_id     UUID,
    action     TEXT,
    details    TEXT,
    PRIMARY KEY ((dept_id), recorded_at, emp_id)
    -- dept_id = partition key (same node এ থাকবে)
    -- recorded_at, emp_id = clustering keys (sort order)
) WITH CLUSTERING ORDER BY (recorded_at DESC);

-- INSERT
INSERT INTO employee_activity (dept_id, recorded_at, emp_id, action)
VALUES (uuid(), toTimestamp(now()), uuid(), 'login');

-- SELECT (partition key দিয়ে সবসময় query করুন)
SELECT * FROM employee_activity
WHERE dept_id = ? AND recorded_at > '2026-01-01'
ORDER BY recorded_at DESC
LIMIT 100;
```

### Cassandra এ যা করা যায় না

```
❌ JOIN নেই
❌ ALLOW FILTERING ছাড়া non-partition key WHERE এ query slow
❌ Aggregation সীমিত
❌ Secondary index সাধারণত এড়িয়ে চলুন
✅ Design your queries first, then your tables (query-driven data modeling)
```

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.৮ কোন Database কখন?

### Decision Matrix

| Use Case | Recommended DB | কারণ |
|----------|---------------|------|
| E-commerce orders, finance | **PostgreSQL/MySQL** | ACID, complex joins |
| User sessions, caching | **Redis** | In-memory, TTL, O(1) lookup |
| Product catalog (flexible schema) | **MongoDB** | Schema-less, nested docs |
| Full-text search | **Elasticsearch** | Inverted index, relevance scoring |
| Social graph, recommendations | **Neo4j** | Graph traversal সহজ |
| IoT sensor data, metrics | **InfluxDB/TimescaleDB** | Time-series optimized |
| Global high-write (log, activity) | **Cassandra** | Horizontal scale, AP |
| Real-time leaderboard | **Redis Sorted Set** | O(log N) ranking |
| Message queue | **Redis List / Kafka** | FIFO, pub/sub |
| Config/distributed lock | **etcd/ZooKeeper** | Strong consistency |

### Real Architecture Example (E-commerce)

```
┌─────────────────────────────────────────────────────┐
│                  E-commerce Platform                 │
├─────────────────────────────────────────────────────┤
│  MySQL          → Orders, Users, Payments (ACID)    │
│  MongoDB        → Product Catalog (flexible schema) │
│  Redis          → Cart, Sessions, Product cache     │
│  Elasticsearch  → Product Search, Autocomplete      │
│  Cassandra      → Click logs, Activity feed         │
│  InfluxDB       → Server metrics, Monitoring        │
└─────────────────────────────────────────────────────┘
```

### Polyglot Persistence

```
একটি application এ multiple databases ব্যবহার করাকে Polyglot Persistence বলে।
প্রতিটি database তার strengths অনুযায়ী কাজে লাগানো হয়।

Trade-offs:
✅ প্রতিটি use case এ optimal performance
✅ একটি DB এর failure অন্যটিকে affect করে না
❌ Operational complexity বাড়ে
❌ Data consistency across DBs maintain করা কঠিন
❌ Team কে multiple technologies শিখতে হয়
```

---

<div align="right"><a href="#part8">⬆ PART 8 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৮.৯ PART 8 — Interview Questions & Answers

### সেকশন ১: মূল প্রশ্নোত্তর

**Q1: NoSQL এবং SQL এর মধ্যে মূল পার্থক্য কী?**

> **উত্তর:** SQL: Fixed schema, ACID compliant, complex JOINs, vertical scaling। NoSQL: Schema-less, BASE model (eventually consistent), horizontal scaling। SQL complex relationships ও strong consistency দরকার হলে (banking, ERP)। NoSQL flexible schema, massive scale, high write throughput দরকার হলে (social media, logs, real-time)।

---

**Q2: CAP Theorem কী? Real world এ এটি কীভাবে applicable?**

> **উত্তর:** CAP Theorem: Consistency, Availability, Partition Tolerance — distributed system এ তিনটির মধ্যে মাত্র দুটি guarantee করা সম্ভব। Network partition (P) real world এ inevitable, তাই CP (MongoDB — consistency বেশি) বা AP (Cassandra — availability বেশি) choose করতে হয়। Banking system CP choose করবে (wrong data দেওয়া যাবে না), social media AP choose করবে (কিছুটা stale data চলবে, কিন্তু system down হবে না)।

---

**Q3: MongoDB তে Embedding এবং Referencing — কোনটি কখন?**

> **উত্তর:** Embedding: Data সবসময় একসাথে read হয়, child document independently access হয় না, data size bounded (BSON limit 16MB)। যেমন: Order → items array embedded। Referencing: Data independently access হয়, shared data (একই author অনেক articles এ), large subdocuments। যেমন: Employee → dept_id reference। General rule: "embed করুন যদি না করার কারণ না থাকে।"

---

**Q4: Redis এ কোন data type কোন use case এ?**

> **উত্তর:** String → Simple cache, counter, session। Hash → Object store (user profile, settings)। List → Queue (job queue), timeline। Set → Unique items (online users), tag intersection। Sorted Set → Leaderboard, priority queue, range query। সব operation গুলো O(1) বা O(log N) — এটাই Redis এর শক্তি।

---

**Q5: Elasticsearch এবং MySQL এ Full-text Search এর পার্থক্য?**

> **উত্তর:** MySQL LIKE '%keyword%' → Full table scan, O(n), case-sensitive issues, relevance ranking নেই। Elasticsearch → Inverted index, O(1) lookup, relevance scoring (TF-IDF/BM25), fuzzy matching, analyzers (stemming, stop words), distributed। Production এ MySQL FULLTEXT index ব্যবহার করা যায় কিন্তু ES এর মতো powerful না। Large scale search এ Elasticsearch।

---

**Q6: Redis এ Cache Invalidation কীভাবে করবেন?**

> **উত্তর:** তিনটি strategy: (1) TTL-based — data write করার সময় TTL set করুন, expire হলে next request এ DB থেকে refetch। (2) Write-through — data update হলে সাথে cache ও update করুন। (3) Cache-aside + explicit delete — data update হলে `cache.delete(key)` করুন, next request এ refetch। Stale data সমস্যা এড়াতে update ও delete atomic হওয়া উচিত।

---

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| MongoDB BSON limit | 16 MB per document |
| Redis persistence দুটি mode | RDB (snapshot) + AOF (log) |
| Cassandra এ JOIN আছে কি? | না |
| CAP এ P কী? | Partition Tolerance |
| ES এ shard কী? | Index এর horizontal partition |
| MongoDB aggregation এর জন্য | $match, $group, $sort, $lookup |
| Redis Sorted Set operation | O(log N) |
| Cassandra কোন CAP? | AP |
| MongoDB কোন CAP? | CP |
| Polyglot Persistence কী? | একই app এ multiple DB |
| Redis TTL set করতে | SETEX বা EXPIRE command |
| ES এ _id কী? | Document এর unique identifier |
| MongoDB ObjectId কত bits? | 96 bits (12 bytes) |
| Graph DB উদাহরণ | Neo4j, ArangoDB |

---

> **⚠️ PART 8 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---


<a id="part9"></a>

# PART 9: Bangladeshi Interview Preparation (বাংলাদেশ ইন্টারভিউ প্রস্তুতি)

> **📍 এই PART এর Sections:** [৯.১ BD IT Job Market](#৯১-বাংলাদেশের-it-job-market) · [৯.২ Interview Process](#৯২-interview-process--bd-companies) · [৯.৩ Common Questions](#৯৩-সবচেয়ে-common-interview-questions) · [৯.৪ Common Mistakes](#৯৪-সাধারণ-ভুল-ও-কীভাবে-এড়াবেন)

> **ব্যবহারের নিয়ম:** এই PART টি বাংলাদেশের actual IT job interview এর জন্য targeted। বাস্তব অভিজ্ঞতার উপর ভিত্তি করে common questions, mistakes, CV tips এবং complete mock interview session রয়েছে।

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.১ বাংলাদেশের IT Job Market

### Company Categories

```
Tier 1 — Product Companies (International):
  Samsung R&D, Ericsson, Pathao Tech, Shajgoj Tech
  → Salary: ৳60,000–৳2,00,000+
  → Interview: Algorithmic + System Design + DB Deep Dive
  → Standard: Very High

Tier 2 — Local Product Companies:
  Shohoz, Chaldal, Shikho, 10 Minute School Tech
  → Salary: ৳40,000–৳1,20,000
  → Interview: Practical coding + DB + Framework
  → Standard: High

Tier 3 — Service/Outsourcing Companies:
  Brain Station 23, Kaz Software, Leads Corporation, Therap Services
  → Salary: ৳25,000–৳80,000
  → Interview: Framework skills + practical projects
  → Standard: Medium-High

Tier 4 — Software Houses & Agencies:
  Local development firms
  → Salary: ৳15,000–৳50,000
  → Interview: Portfolio + practical skills
  → Standard: Varies

Government IT:
  a2i, ICT Division, Bangladesh Computer Council
  → Written exam + viva
  → Database/networking fundamentals
```

### Junior Engineer হিসেবে কী দরকার

```
✅ Must Have:
  → SQL (SELECT, JOIN, GROUP BY, subquery)
  → RDBMS concepts (normalization, indexes, FK)
  → কমপক্ষে ১টি framework এ DB integration (Laravel/Django/Node)
  → Git (basic version control)
  → ১টি real project (personal বা academic)

✅ Good to Have:
  → Stored procedures / views
  → Query optimization basics
  → Redis basics (caching)
  → API design basics (REST)
  → Docker basics

✅ Bonus (Senior বা Product companies):
  → NoSQL (MongoDB বা Redis deep dive)
  → System design concepts
  → Transaction isolation levels
  → Replication / sharding concepts
```

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.২ Interview Process — BD Companies

### Typical Stages

```
Stage 1: CV Screening
  → Keywords: framework name, DB name, project description
  → GitHub link গুরুত্বপূর্ণ
  → 1 page CV preferred for juniors

Stage 2: Written/Online Test (30–90 min)
  → SQL queries (definitely)
  → Logical/aptitude questions
  → OOP concepts (MCQ)
  → Algorithmic problems (varies by company)

Stage 3: Technical Interview (1–2 rounds)
  → Database concepts deep dive
  → Framework-specific questions
  → Code writing on whiteboard/screen
  → Project discussion (আপনার CV তে লেখা project)

Stage 4: HR Interview
  → Salary expectation
  → Joining timeline
  → Career goals
  → Team fit
```

### Written Test — SQL Question Patterns

```sql
-- বাংলাদেশের written test এ সচরাচর আসে:

-- ১. Basic JOIN
SELECT e.name, d.dept_name
FROM employees e
JOIN departments d ON e.dept_id = d.dept_id;

-- ২. Aggregate with GROUP BY + HAVING
SELECT dept_id, COUNT(*) AS total, AVG(salary) AS avg_sal
FROM employees
GROUP BY dept_id
HAVING COUNT(*) > 3;

-- ৩. Subquery
SELECT name, salary
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);

-- ৪. Ranking (TOP N per group)
SELECT name, dept_id, salary
FROM employees e1
WHERE 3 > (
    SELECT COUNT(*)
    FROM employees e2
    WHERE e2.dept_id = e1.dept_id AND e2.salary > e1.salary
);

-- ৫. NULL handling
SELECT name, COALESCE(phone, 'N/A') AS phone
FROM employees;

-- ৬. Date functions
SELECT name, DATEDIFF(CURDATE(), join_date) AS days_worked
FROM employees
WHERE YEAR(join_date) = 2024;

-- ৭. String functions
SELECT CONCAT(first_name, ' ', last_name) AS full_name,
       UPPER(email), LENGTH(name)
FROM employees;

-- ৮. Multiple table JOIN
SELECT e.name, d.dept_name, p.project_name
FROM employees e
JOIN departments d ON e.dept_id = d.dept_id
JOIN employee_projects ep ON e.emp_id = ep.emp_id
JOIN projects p ON ep.proj_id = p.proj_id
WHERE p.status = 'active';
```

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.৩ সবচেয়ে Common Interview Questions

### Database Concepts (সবচেয়ে বেশি জিজ্ঞেস করা হয়)

**১. Primary Key এবং Foreign Key এর পার্থক্য?**
> PK: Table এর প্রতিটি row কে uniquely identify করে, NULL হতে পারে না, একটি table এ একটিই PK। FK: অন্য table এর PK reference করে, referential integrity maintain করে, NULL হতে পারে (optional relationship)।

**২. Normalization কী? 1NF, 2NF, 3NF?**
> Redundancy কমিয়ে data integrity বাড়ানোর প্রক্রিয়া। 1NF: Atomic values, no repeating groups। 2NF: 1NF + non-key attributes পুরোপুরি PK এর উপর dependent। 3NF: 2NF + non-key attributes অন্য non-key attribute এর উপর dependent নয় (transitive dependency নেই)।

**৩. Index কী? কেন ব্যবহার করি?**
> Index হলো B-Tree data structure যা query speed বাড়ায়। SELECT দ্রুত হয় কিন্তু INSERT/UPDATE/DELETE slow হয় এবং extra storage লাগে। Frequently searched columns এ, FK columns এ, UNIQUE columns এ index তৈরি করুন।

**৪. JOIN এর types কী কী?**
> INNER JOIN: দুই table এ match আছে এমন rows। LEFT JOIN: বাম table এর সব row + match থাকলে ডান table। RIGHT JOIN: ডান table এর সব + বাম এর match। FULL OUTER JOIN: দুই table এর সব rows। CROSS JOIN: Cartesian product।

**৫. Transaction কী? ACID কী?**
> Transaction হলো একসাথে execute হওয়া SQL operations এর একটি unit — সব succeed করবে অথবা সব rollback হবে। ACID: Atomicity (all or nothing), Consistency (valid state), Isolation (concurrent transactions আলাদা), Durability (committed data persist)।

**৬. View কী? কখন ব্যবহার করি?**
> View হলো stored SELECT query — virtual table। Complex query কে simplify করতে, security (sensitive columns hide করতে), ও frequently used query reuse করতে ব্যবহার করা হয়। View নিজে data store করে না।

**৭. Stored Procedure কী?**
> Database এ stored precompiled SQL statements এর collection। Execution plan cache হয় তাই দ্রুত। Business logic DB তে রাখা যায়। Network roundtrip কমে। কিন্তু debugging কঠিন, version control কঠিন।

**৮. N+1 Problem কী?**
> ORM দিয়ে parent records এনে প্রতিটির জন্য আলাদা query চালালে N+1 queries হয়। ১টি query এ ১০টি employees → তারপর ১০টি query, প্রতিটির department এর জন্য = ১১টি query। সমাধান: Eager Loading (JOIN দিয়ে এক query তে আনুন)।

**৯. Deadlock কী? কীভাবে এড়াবেন?**
> দুটি transaction পরস্পরের lock এর জন্য অপেক্ষা করলে Deadlock হয়। এড়াতে: সবসময় একই order এ table/row lock করুন, transaction ছোট রাখুন, timeout set করুন, deadlock হলে retry করুন।

**১০. SQL Injection কী? কীভাবে prevent করবেন?**
> User input সরাসরি SQL query তে insert করলে attacker malicious SQL execute করাতে পারে। Prevent: Parameterized queries / Prepared Statements, Input validation, Least privilege (limited DB user), ORM ব্যবহার।

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.৪ সাধারণ ভুল ও কীভাবে এড়াবেন

### Technical Mistakes

```
❌ ভুল: "আমি জানি না" বলে চুপ থাকা
✅ সঠিক: "এই মুহূর্তে ঠিক মনে নেই, তবে আমি এটি এভাবে approach করব..."

❌ ভুল: Theory জানে কিন্তু example দিতে পারে না
✅ সঠিক: প্রতিটি concept এর জন্য real/practical example রেডি রাখুন

❌ ভুল: SQL লিখতে বসে সরাসরি code করা
✅ সঠিক: প্রথমে বলুন "আমি প্রথমে structure টা বুঝি", তারপর step by step লিখুন

❌ ভুল: JOIN এর পরিবর্তে subquery দিয়ে সব করা
✅ সঠিক: JOIN সম্পর্কে confident থাকুন, এটি বেশি efficient

❌ ভুল: Index সম্পর্কে জিজ্ঞেস করলে শুধু "speed বাড়ায়" বলা
✅ সঠিক: B-Tree structure, trade-off (slow write, extra space) বলুন

❌ ভুল: "আমার project এ database ছিল না"
✅ সঠিক: যেকোনো project এ অন্তত SQLite দিয়ে হলেও DB ব্যবহার করুন

❌ ভুল: Transaction কখন দরকার জানে না
✅ সঠিক: Fund transfer, order creation — multiple table এ একসাথে write = transaction
```

### Behavioral Mistakes

```
❌ Salary expectation জিজ্ঞেস করলে অস্বস্তি দেখানো
✅ Market rate research করুন এবং confidently range বলুন

❌ "আমি সব পারি" বলা
✅ Strengths সৎভাবে বলুন, শেখার ইচ্ছা দেখান

❌ Interview এ দেরিতে আসা (online হলেও)
✅ ১০ মিনিট আগে ready থাকুন

❌ Interviewer এর কথা না শুনে নিজের উত্তর দেওয়া
✅ প্রশ্ন সম্পূর্ণ শুনুন, প্রয়োজনে clarify করুন

❌ Previous employer সম্পর্কে negative কথা বলা
✅ Professional থাকুন, growth ও learning focus করুন
```

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.৫ CV ও Portfolio Tips

### CV Structure (Junior Engineer)

```
[নাম] | [Email] | [Phone] | [GitHub] | [LinkedIn] | [Portfolio URL]

SUMMARY (2-3 lines):
  Backend developer with X years experience in PHP/Laravel and MySQL.
  Experienced in building RESTful APIs and database optimization.

SKILLS:
  Languages:  PHP, Python, JavaScript, SQL
  Frameworks: Laravel, Django, Node.js (Express)
  Databases:  MySQL, PostgreSQL, Redis, MongoDB (basic)
  Tools:      Git, Docker (basic), Linux, Postman

EXPERIENCE:
  Company Name | Role | Duration
  → Bullet points: action verb + what you did + impact
  → "Optimized slow queries reducing page load by 40%"
  → "Designed MySQL schema for 100K+ users"

PROJECTS (সবচেয়ে গুরুত্বপূর্ণ):
  Project Name | [GitHub Link] | [Live Demo]
  → Tech stack clearly mention করুন
  → Database design সম্পর্কে একটি bullet দিন
  → "MySQL database with 12 normalized tables, full-text search"

EDUCATION:
  University | Degree | Year | CGPA (যদি ভালো হয়)
```

### GitHub Portfolio

```
✅ করুন:
  → README.md সব project এ (ER diagram, setup instructions)
  → Regular commits (না করলে blank দেখায়)
  → At least ১টি বড় project (CRUD + Authentication + DB)
  → Database schema file (schema.sql) রাখুন repo তে
  → .env.example রাখুন (actual credentials ছাড়া)

❌ করবেন না:
  → Empty repositories
  → .env file push করবেন না (credentials!)
  → Commit message: "fix", "update", "asdf" — descriptive রাখুন
  → আধা-করা projects
```

### Project Description Template (Interview এ বলার জন্য)

```
"আমি [Project Name] তৈরি করেছি যেটি [কী সমস্যা সমাধান করে]।
Tech stack: [Language] + [Framework] + [Database]।
Database এ [কতটি table, ER relationship] ব্যবহার করেছি।
সবচেয়ে challenging ছিল [একটি technical challenge] যেটি আমি
[solution] দিয়ে solve করেছি। এর ফলে [improvement/result]।"

Example:
"আমি একটি e-commerce system তৈরি করেছি যেটি local retailers কে
online store manage করতে সাহায্য করে। Laravel + MySQL ব্যবহার করেছি।
Database এ ১৫টি normalized table আছে — products, categories,
orders, order_items, users, etc। সবচেয়ে challenging ছিল
inventory management — যখন order place হয় তখন atomically
stock decrease করা। Transaction দিয়ে race condition solve করেছি।"
```

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.৬ SQL Cheat Sheet — Quick Revision

### সব গুরুত্বপূর্ণ Syntax একনজরে

```sql
-- ── SELECT ───────────────────────────────────────
SELECT col1, col2, COUNT(*) AS cnt, AVG(salary) AS avg_sal
FROM employees
WHERE salary > 50000
  AND dept_id IN (1, 2, 3)
  AND name LIKE 'K%'
  AND join_date BETWEEN '2024-01-01' AND '2024-12-31'
  AND phone IS NOT NULL
GROUP BY dept_id
HAVING COUNT(*) > 2
ORDER BY avg_sal DESC
LIMIT 10 OFFSET 20;

-- ── JOINs ─────────────────────────────────────────
-- INNER
SELECT e.name, d.dept_name FROM employees e
JOIN departments d ON e.dept_id = d.dept_id;

-- LEFT (all employees, even without dept)
SELECT e.name, d.dept_name FROM employees e
LEFT JOIN departments d ON e.dept_id = d.dept_id;

-- Self JOIN (manager-employee)
SELECT e.name AS emp, m.name AS manager
FROM employees e
LEFT JOIN employees m ON e.manager_id = m.emp_id;

-- ── SUBQUERIES ────────────────────────────────────
-- Scalar subquery
SELECT name FROM employees
WHERE salary = (SELECT MAX(salary) FROM employees);

-- Correlated subquery
SELECT name, salary FROM employees e
WHERE salary > (SELECT AVG(salary) FROM employees WHERE dept_id = e.dept_id);

-- IN subquery
SELECT name FROM employees
WHERE dept_id IN (SELECT dept_id FROM departments WHERE location = 'Dhaka');

-- EXISTS
SELECT name FROM employees e
WHERE EXISTS (SELECT 1 FROM projects p
              JOIN employee_projects ep ON p.proj_id = ep.proj_id
              WHERE ep.emp_id = e.emp_id AND p.status = 'active');

-- ── WINDOW FUNCTIONS ──────────────────────────────
SELECT name, salary, dept_id,
    RANK()       OVER (PARTITION BY dept_id ORDER BY salary DESC) AS dept_rank,
    ROW_NUMBER() OVER (ORDER BY salary DESC)                      AS overall_row,
    LAG(salary)  OVER (PARTITION BY dept_id ORDER BY join_date)  AS prev_salary,
    SUM(salary)  OVER (PARTITION BY dept_id)                     AS dept_total
FROM employees;

-- ── CTEs ──────────────────────────────────────────
WITH dept_avg AS (
    SELECT dept_id, AVG(salary) AS avg_sal FROM employees GROUP BY dept_id
),
high_earners AS (
    SELECT e.name, e.salary, da.avg_sal
    FROM employees e JOIN dept_avg da ON e.dept_id = da.dept_id
    WHERE e.salary > da.avg_sal
)
SELECT * FROM high_earners ORDER BY salary DESC;

-- ── DDL ───────────────────────────────────────────
CREATE TABLE employees (
    emp_id    INT          AUTO_INCREMENT PRIMARY KEY,
    name      VARCHAR(100) NOT NULL,
    email     VARCHAR(150) UNIQUE NOT NULL,
    salary    DECIMAL(10,2) DEFAULT 0,
    dept_id   INT,
    is_active TINYINT(1)   DEFAULT 1,
    join_date DATE         DEFAULT (CURRENT_DATE),
    FOREIGN KEY (dept_id) REFERENCES departments(dept_id) ON DELETE SET NULL,
    INDEX idx_dept (dept_id),
    INDEX idx_salary (salary)
);

ALTER TABLE employees ADD COLUMN phone VARCHAR(20);
ALTER TABLE employees MODIFY COLUMN salary DECIMAL(12,2);
ALTER TABLE employees DROP COLUMN phone;
CREATE INDEX idx_name ON employees(name);
DROP INDEX idx_name ON employees;

-- ── DML ───────────────────────────────────────────
INSERT INTO employees (name, email, salary, dept_id) VALUES ('Karim', 'k@e.com', 75000, 1);
UPDATE employees SET salary = salary * 1.10 WHERE dept_id = 1;
DELETE FROM employees WHERE is_active = 0 AND join_date < '2020-01-01';

-- ── TRANSACTION ───────────────────────────────────
START TRANSACTION;
UPDATE accounts SET balance = balance - 10000 WHERE id = 1;
UPDATE accounts SET balance = balance + 10000 WHERE id = 2;
COMMIT;  -- অথবা ROLLBACK;

-- ── USEFUL FUNCTIONS ──────────────────────────────
-- String
CONCAT(first_name, ' ', last_name), UPPER(name), LOWER(email),
LENGTH(name), SUBSTRING(name, 1, 5), TRIM(name), REPLACE(str, 'old', 'new')

-- Date
NOW(), CURDATE(), CURTIME(),
DATE_FORMAT(join_date, '%Y-%m-%d'),
DATEDIFF(NOW(), join_date),
DATE_ADD(join_date, INTERVAL 1 YEAR),
YEAR(join_date), MONTH(join_date), DAY(join_date)

-- Conditional
COALESCE(phone, email, 'N/A'),
NULLIF(salary, 0),
IF(salary > 70000, 'Senior', 'Junior'),
CASE WHEN salary > 80000 THEN 'A' WHEN salary > 60000 THEN 'B' ELSE 'C' END

-- Aggregate
COUNT(*), COUNT(DISTINCT dept_id), SUM(salary), AVG(salary), MAX(salary), MIN(salary)

-- ── VIEW ──────────────────────────────────────────
CREATE VIEW active_employees AS
SELECT e.emp_id, e.name, d.dept_name, e.salary
FROM employees e JOIN departments d ON e.dept_id = d.dept_id
WHERE e.is_active = 1;

-- ── STORED PROCEDURE ──────────────────────────────
DELIMITER //
CREATE PROCEDURE GetDeptEmployees(IN p_dept_id INT)
BEGIN
    SELECT emp_id, name, salary
    FROM employees
    WHERE dept_id = p_dept_id AND is_active = 1
    ORDER BY salary DESC;
END //
DELIMITER ;
CALL GetDeptEmployees(1);
```

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.৭ Mock Interview — Full Session

> **ব্যবহার:** একজন বন্ধুকে interviewer বানান, অথবা নিজে নিজে উত্তর দেওয়ার চেষ্টা করুন। উত্তর দেওয়ার পর এই handbook থেকে দেখুন ঠিক হয়েছে কিনা।

---

### Mock Interview Round 1 — Concepts (20 min)

**Q1:** Database এবং DBMS এর মধ্যে পার্থক্য বলুন।
**Q2:** Relational database কেন use করি? কখন NoSQL better?
**Q3:** Primary Key এবং Unique Key এর মধ্যে পার্থক্য কী?
**Q4:** 1NF, 2NF, 3NF ব্যাখ্যা করুন, example সহ।
**Q5:** Index কীভাবে কাজ করে? Clustered এবং Non-clustered এর পার্থক্য?
**Q6:** ACID property গুলো কী? Transaction কেন দরকার?
**Q7:** Deadlock কী? কীভাবে detect ও prevent করা যায়?
**Q8:** View এবং Stored Procedure এর মধ্যে পার্থক্য?

---

### Mock Interview Round 2 — SQL Writing (30 min)

```sql
-- এই schema ব্যবহার করুন:
-- departments(dept_id, dept_name, location)
-- employees(emp_id, name, email, salary, dept_id, manager_id, join_date, is_active)
-- projects(proj_id, project_name, start_date, end_date, status)
-- employee_projects(emp_id, proj_id, role, hours_worked)
```

**লিখুন:**

1. প্রতিটি department এ কতজন active employee আছে এবং তাদের গড় বেতন কত — সর্বোচ্চ গড় বেতনের department প্রথমে।

2. প্রতিটি employee এর নাম, তাদের manager এর নাম এবং বেতনের পার্থক্য দেখান।

3. যে employees এর বেতন তাদের department এর গড় বেতনের চেয়ে বেশি তাদের দেখান।

4. প্রতিটি department এ বেতনের দিক থেকে top ৩ জন employee দেখান।

5. কোন projects এ কোনো employee assigned নেই তা দেখান।

6. ২০২৪ সালে join করা employees এর মধ্যে সবচেয়ে বেশি project এ কাজ করেছে কে?

---

### Mock Interview Round 2 — উত্তর

```sql
-- ১. Department stats
SELECT d.dept_name, COUNT(e.emp_id) AS total_emp, ROUND(AVG(e.salary), 2) AS avg_salary
FROM departments d
LEFT JOIN employees e ON d.dept_id = e.dept_id AND e.is_active = 1
GROUP BY d.dept_id, d.dept_name
ORDER BY avg_salary DESC;

-- ২. Employee + Manager + salary diff
SELECT e.name AS employee, m.name AS manager,
       e.salary AS emp_salary, m.salary AS mgr_salary,
       (m.salary - e.salary) AS salary_diff
FROM employees e
LEFT JOIN employees m ON e.manager_id = m.emp_id;

-- ৩. Above department average
SELECT e.name, e.salary, d.dept_name
FROM employees e
JOIN departments d ON e.dept_id = d.dept_id
WHERE e.salary > (
    SELECT AVG(e2.salary) FROM employees e2 WHERE e2.dept_id = e.dept_id
)
ORDER BY e.dept_id, e.salary DESC;

-- ৪. Top 3 per department (window function)
SELECT name, dept_name, salary
FROM (
    SELECT e.name, d.dept_name, e.salary,
           RANK() OVER (PARTITION BY e.dept_id ORDER BY e.salary DESC) AS rnk
    FROM employees e JOIN departments d ON e.dept_id = d.dept_id
) ranked
WHERE rnk <= 3;

-- ৫. Projects with no employees
SELECT p.proj_id, p.project_name
FROM projects p
LEFT JOIN employee_projects ep ON p.proj_id = ep.proj_id
WHERE ep.emp_id IS NULL;

-- ৬. Most active 2024 hire
SELECT e.name, COUNT(ep.proj_id) AS project_count
FROM employees e
JOIN employee_projects ep ON e.emp_id = ep.emp_id
WHERE YEAR(e.join_date) = 2024
GROUP BY e.emp_id, e.name
ORDER BY project_count DESC
LIMIT 1;
```

---

### Mock Interview Round 3 — Scenario (15 min)

**Scenario 1:**
> "আমাদের application এ users table এ 5 million rows আছে। `WHERE email = ?` query অনেক slow। কী করবেন?"

**Expected Answer:**
> `email` column এ index আছে কিনা দেখব — `SHOW INDEX FROM users`। না থাকলে `CREATE UNIQUE INDEX idx_email ON users(email)` করব। তারপর `EXPLAIN SELECT * FROM users WHERE email = ?` দিয়ে query plan দেখব। Index থাকার পরও slow হলে: column এ function wrap করা হচ্ছে কিনা, implicit type casting হচ্ছে কিনা দেখব।

**Scenario 2:**
> "দুটি user একসাথে একই product এর last ১টি stock কিনতে চাইছে। Race condition কীভাবে prevent করবেন?"

**Expected Answer:**
> Transaction + SELECT FOR UPDATE ব্যবহার করব: `START TRANSACTION; SELECT stock FROM products WHERE id = ? FOR UPDATE; -- check stock > 0; UPDATE products SET stock = stock - 1 WHERE id = ?; INSERT INTO orders ...; COMMIT;` এই approach এ DB level lock থাকায় concurrent requests এ একজনই stock পাবে।

**Scenario 3:**
> "আমাদের application এ কিছু API খুব slow কারণ DB এ অনেক বার query হচ্ছে। কীভাবে diagnose করবেন?"

**Expected Answer:**
> প্রথমে slow query log enable করব (`slow_query_log = ON, long_query_time = 1`)। তারপর most frequent queries দেখব। ORM থেকে generated queries log করব — N+1 problem check করব। `EXPLAIN ANALYZE` দিয়ে প্রতিটি slow query এর plan দেখব। Index missing আছে কিনা দেখব। তারপর Redis caching implement করব frequently read কিন্তু rarely changed data এর জন্য।

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.৮ Interview Day Checklist

### আগের দিন

```
✅ Technical Preparation:
  □ SQL basics revision (JOIN, GROUP BY, subquery)
  □ ACID, Normalization, Index একবার পড়ুন
  □ নিজের project এর technical details refresh করুন
  □ Company সম্পর্কে research করুন (tech stack, product)

✅ Logistics:
  □ Interview location/link confirm করুন
  □ Online হলে: camera, mic, internet test করুন
  □ কোড editor/IDE ready রাখুন (VS Code)
  □ ঘুম ভালো করুন
```

### Interview এর দিন

```
✅ Before:
  □ ১৫-২০ মিনিট আগে ready থাকুন
  □ পানি পাশে রাখুন
  □ Distraction-free environment (mute phone)

✅ During:
  □ প্রশ্ন সম্পূর্ণ শুনুন
  □ জানলে confidently বলুন
  □ না জানলে: "এই মুহূর্তে মনে নেই, তবে আমি এভাবে approach করব..."
  □ SQL লেখার সময় আগে schema টা বলুন, তারপর ধাপে ধাপে লিখুন
  □ Clarifying questions করুন (requirements এ ambiguity থাকলে)

✅ After:
  □ Interviewer কে সময় দেওয়ার জন্য ধন্যবাদ জানান
  □ Next steps সম্পর্কে জিজ্ঞেস করুন
  □ Interview এ কী ভুল হলো নোট করুন (improve এর জন্য)
```

### Salary Negotiation

```
Research করুন:
  → LinkedIn Jobs, Glassdoor, BD Tech salaries Facebook groups
  → Junior Backend: ৳25,000–৳60,000 (company tier অনুযায়ী)
  → "আমার expected range ৳X–৳Y। আপনাদের budget কেমন?"

যদি offer কম হয়:
  → "আমি এই role এ অনেক আগ্রহী। ৳X সম্ভব কিনা আলোচনা করা যায়?"
  → একবার counter করুন, বারবার না
```

---

<div align="right"><a href="#part9">⬆ PART 9 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৯.৯ Final Study Plan

### ৭ দিনের Revision Plan (Interview আগে)

```
Day 1 — Foundation:
  ✓ PART 1 পড়ুন (Database Fundamentals)
  ✓ company_db schema মুখস্ত করুন
  ✓ Basic SELECT, JOIN, WHERE practice করুন

Day 2 — Core SQL:
  ✓ PART 2 পড়ুন (Advanced SQL)
  ✓ GROUP BY, HAVING, Subquery practice
  ✓ ৫টি JOIN query নিজে লিখুন

Day 3 — Design:
  ✓ PART 3 পড়ুন (Normalization)
  ✓ PART 4 পড়ুন (Database Design)
  ✓ একটি ER diagram আঁকুন (e-commerce)

Day 4 — Performance:
  ✓ Window Functions practice (RANK, LAG, SUM OVER)
  ✓ Index concept মনে রাখুন
  ✓ Transaction + ACID

Day 5 — Framework:
  ✓ আপনার framework (Laravel/Django/Node) এর DB section পড়ুন
  ✓ N+1 problem ও solution মনে করুন
  ✓ PART 7 relevant section পড়ুন

Day 6 — NoSQL + Mock:
  ✓ PART 8 — MongoDB, Redis quick read
  ✓ CAP Theorem মনে রাখুন
  ✓ Mock Interview Round 1 & 2 করুন

Day 7 — Final:
  ✓ SQL Cheat Sheet (Section ৯.৬) এ চোখ বোলান
  ✓ নিজের project ভালো করে explain করার practice করুন
  ✓ Interview Day Checklist (Section ৯.৮) follow করুন
  ✓ ভালো ঘুমান!
```

### Topic Priority Matrix

```
Must Know (100% জিজ্ঞেস হবে):
  ★★★ PRIMARY KEY, FOREIGN KEY, JOIN types
  ★★★ GROUP BY, HAVING, aggregate functions
  ★★★ Subquery (scalar, correlated, IN)
  ★★★ Normalization (1NF–3NF)
  ★★★ Index — কী, কেন, কখন
  ★★★ Transaction, ACID
  ★★★ N+1 problem ও eager loading

Very Likely (জিজ্ঞেস হওয়ার সম্ভাবনা বেশি):
  ★★☆ Window Functions (RANK, ROW_NUMBER)
  ★★☆ CTE (WITH clause)
  ★★☆ View, Stored Procedure
  ★★☆ SQL Injection prevention
  ★★☆ Soft Delete pattern
  ★★☆ Redis caching basics

Good to Know (Senior level / বোনাস):
  ★☆☆ Replication, Sharding
  ★☆☆ CAP Theorem
  ★☆☆ Elasticsearch basics
  ★☆☆ Query execution plan (EXPLAIN)
  ★☆☆ Isolation levels
  ★☆☆ Cassandra architecture
```

---

> **✅ PART 9 সম্পন্ন — হ্যান্ডবুক সম্পূর্ণ হয়েছে!**
>
> এই হ্যান্ডবুকটি বাংলাদেশের Junior Database/Backend Engineer Interview এর জন্য সম্পূর্ণ প্রস্তুতি প্রদান করে। শুভকামনা!

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

*হ্যান্ডবুক তৈরিতে: Senior Database Engineer & Backend Architect*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 9 | সম্পূর্ণ ✅*
