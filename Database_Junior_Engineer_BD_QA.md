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
| 📔 | **PART 6** — Database Interview Questions | *(শীঘ্রই আসছে)* |
| 📒 | **PART 7** — Language & Framework Database Integration | *(শীঘ্রই আসছে)* |
| 📃 | **PART 8** — NoSQL & Modern Databases | *(শীঘ্রই আসছে)* |
| 📄 | **PART 9** — Bangladeshi Interview Preparation | *(শীঘ্রই আসছে)* |




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
<summary><strong>� PART 2 — বিস্তারিত সূচি দেখুন</strong></summary>
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
<summary><strong>�📘 PART 1 — বিস্তারিত সূচি দেখুন</strong></summary>
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

> **ব্যবহারের নিয়ম:** প্রতিটি query নিজে একটি database এ run করুন। MySQL Workbench বা DBeaver ব্যবহার করুন। শুধু পড়লে হবে না — লিখতে হবে।

---

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

> **ব্যবহারের নিয়ম:** এই PART টি Senior-level concepts ধারণ করে। Freshers যদি এগুলো জানেন, interview এ অনেক এগিয়ে থাকবেন। PART 2 এর `company_db` setup ব্যবহার করে examples practice করুন।

---

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

> **ব্যবহারের নিয়ম:** এই PART টি Database Design এর মূল ভিত্তি। Interview এ প্রায়ই Normalization এর step-by-step process এবং ER Diagram থেকে Schema তৈরি জিজ্ঞেস করা হয়। প্রতিটি Normal Form উদাহরণসহ বুঝুন।

---

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
