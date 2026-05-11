<a id="top"></a>

# 🎯 OOP Interview Preparation Handbook
---

> **💡 হ্যান্ডবুক ব্যবহারের নিয়ম:**  
> প্রতিটি টপিক মনোযোগ দিয়ে পড়ুন। Code examples নিজে লিখুন। Interview questions নিজে উত্তর দেওয়ার চেষ্টা করুন তারপর model answer দেখুন।

---

<a id="toc"></a>

## 📋 সূচিপত্র — Table of Contents

> **💡 নিচের যেকোনো PART এ সরাসরি ক্লিক করুন। প্রতিটি PART এর শেষে [⬆ শীর্ষে ফিরুন](#top) বাটন আছে।**

| | PART | বিষয়বস্তু |
|:-:|------|------------|
| 📘 | [**PART 1** — OOP Fundamentals](#part1) | Class, Object, Encapsulation, Abstraction, Inheritance, Polymorphism |
| 📗 | [**PART 2** — Advanced OOP](#part2) | SOLID, Interface, Virtual Functions, Binding, Diamond Problem |
| 📙 | [**PART 3** — Interview Q&A (৫০টি)](#part3) | Theoretical Questions, Common Mistakes, Follow-up Patterns |
| 📕 | [**PART 4** — Coding Problems](#part4) | Student, Bank, Employee, Library Management Systems |
| 📓 | [**PART 5** — Language-Specific OOP](#part5) | Java, C++, Python, C# — তুলনা ও Interview Traps |
| 📔 | [**PART 6** — Advanced Topics](#part6) | Memory, Garbage Collection, Design Patterns (GoF), MVC |
| 📒 | [**PART 7** — BD Interview Prep](#part7) | Mock Interview, Company Patterns, Checklist, Rapid-fire |

<details>
<summary><strong>📘 PART 1 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [১.১ OOP কী?](#১১-object-oriented-programming-oop-কী)
- [১.২ Class এবং Object](#১২-class-এবং-object)
- [১.৩ Constructor ও Destructor](#১৩-constructor-এবং-destructor)
- [১.৪ Access Modifiers](#১৪-access-modifiers-অ্যাক্সেস-মডিফায়ার)
- [১.৫ Encapsulation](#১৫-encapsulation-এনক্যাপসুলেশন)
- [১.৬ Abstraction](#১৬-abstraction-অ্যাবস্ট্রাকশন)
- [১.৭ Inheritance](#১৭-inheritance-ইনহেরিটেন্স)
- [১.৮ Polymorphism](#১৮-polymorphism-পলিমরফিজম)
- [১.৯ Overloading vs Overriding](#১৯-method-overloading-vs-method-overriding)
- [১.১০ Interview Q&A](#১১০-part-1--interview-questions--answers)

</details>

<details>
<summary><strong>📗 PART 2 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [২.১ Static vs Dynamic Binding](#২১-static-binding-vs-dynamic-binding)
- [২.২ Interface](#২২-interface-ইন্টারফেস)
- [২.৩ Abstract Class vs Interface](#২৩-abstract-class-vs-interface)
- [২.৪ Virtual Function ও Pure Virtual Function](#২৪-virtual-function-এবং-pure-virtual-function)
- [২.৫ Copy Constructor ও Deep/Shallow Copy](#২৫-copy-constructor-এবং-deep-vs-shallow-copy)
- [২.৬ Diamond Problem](#২৬-diamond-problem-ডায়মন্ড-সমস্যা)
- [২.৭ SOLID Principles](#২৭-solid-principles)
- [২.৮ Dependency Injection](#২৮-dependency-injection-di)
- [২.৯ Coupling ও Cohesion](#২৯-coupling-এবং-cohesion)
- [২.১০ Interview Q&A](#২১০-part-2--interview-questions--answers)

</details>

<details>
<summary><strong>📙 PART 3 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৩.১ ৫০টি Theoretical Q&A](#৩১-theoretical-interview-questions-৫০টি-বিস্তারিত-প্রশ্নোত্তর)
- [৩.২ Common Interview Mistakes](#৩২-common-interview-mistakes-এবং-কীভাবে-এড়াবেন)
- [৩.৩ Follow-up Question Patterns](#৩৩-follow-up-question-patterns-common-sequences)

</details>

<details>
<summary><strong>📕 PART 4 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৪.১ Student Management System](#৪১-student-management-system)
- [৪.২ Bank Management System](#৪২-bank-management-system)
- [৪.৩ Employee Management System](#৪৩-employee-management-system)
- [৪.৪ Library Management System](#৪৪-library-management-system)
- [৪.৫ Coding Interview কৌশল](#৪৫-coding-problem--interview-কৌশল-সব-system-এর-জন্য)

</details>

<details>
<summary><strong>📓 PART 5 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৫.১ Java OOP](#৫১-java-oop--বিস্তারিত)
- [৫.২ C++ OOP](#৫২-c-oop--java-এর-সাথে-তুলনা)
- [৫.৩ Python OOP](#৫৩-python-oop--বৈশিষ্ট্য-ও-interview-traps)
- [৫.৪ C# OOP](#৫৪-c-oop--java-এর-সাথে-তুলনা)
- [৫.৫ Language তুলনা Table](#৫৫-language-তুলনা--quick-reference-table)
- [৫.৬ BD Interview Language Questions](#৫৬-bangladeshi-interview-তে-language-specific-প্রশ্ন)

</details>

<details>
<summary><strong>📔 PART 6 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৬.১ Memory Management — Stack vs Heap](#৬১-memory-management--stack-vs-heap)
- [৬.২ Garbage Collection](#৬২-garbage-collection--java)
- [৬.৩ Design Patterns (GoF)](#৬৩-design-patterns--gang-of-four-gof)
- [৬.৪ MVC Architecture](#৬৪-mvc-architecture--oop-দিয়ে)
- [৬.৫ Object Cloning](#৬৫-object-cloning--shallow-vs-deep-copy-revisited)
- [৬.৬ Exception Handling ও OOP](#৬৬-exception-handling-ও-oop)
- [৬.৭ Advanced Interview Questions](#৬৭-advanced-oop-interview-questions)

</details>

<details>
<summary><strong>📒 PART 7 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৭.১ BD Company Interview Structure](#৭১-bangladeshi-tech-company--interview-structure)
- [৭.২ Fresher Viva — Common Q&A](#৭২-fresher-viba--সবচেয়ে-বেশি-জিজ্ঞেস-করা-প্রশ্ন-ও-আদর্শ-উত্তর)
- [৭.৩ Project Explanation Strategy](#৭৩-project-explanation--oop-দিয়ে-কীভাবে-বলবেন)
- [৭.৪ Complete Mock Interview](#৭৪-complete-mock-interview--পূর্ণ-কথোপকথন)
- [৭.৫ Interview ভুল এড়ানো](#৭৫-সাধারণ-interview-ভুল--এড়িয়ে-চলুন)
- [৭.৬ 30-মিনিটের Checklist](#৭৬-30-মিনিটের-interview-preparation-checklist)
- [৭.৭ এক লাইনের সংজ্ঞা](#৭৭-oop-concept--এক-লাইনের-স্মরণীয়-সংজ্ঞা)
- [৭.৮ Rapid-Fire (৫০টি Q&A)](#৭৮-final-rapid-fire--৫০টি-quick-qa)
- [৭.৯ Revision Plan](#৭৯-হ্যান্ডবুক-ব্যবহার-গাইড--revision-plan)

</details>

---

<a id="part1"></a>

# PART 1: OOP Fundamentals (মূল ধারণাসমূহ)

> **📍 এই PART এর Sections:** [১.১ OOP কী?](#১১-object-oriented-programming-oop-কী) · [১.২ Class & Object](#১২-class-এবং-object) · [১.৩ Constructor](#১৩-constructor-এবং-destructor) · [১.৪ Access Modifiers](#১৪-access-modifiers-অ্যাক্সেস-মডিফায়ার) · [১.৫ Encapsulation](#১৫-encapsulation-এনক্যাপসুলেশন) · [১.৬ Abstraction](#১৬-abstraction-অ্যাবস্ট্রাকশন) · [১.৭ Inheritance](#১৭-inheritance-ইনহেরিটেন্স) · [১.৮ Polymorphism](#১৮-polymorphism-পলিমরফিজম) · [১.৯ Overloading vs Overriding](#১৯-method-overloading-vs-method-overriding) · [১.১০ Interview Qs](#১১০-part-1--interview-questions--answers)

---

## ১.১ Object-Oriented Programming (OOP) কী?

### সংজ্ঞা (Definition)

**Object-Oriented Programming (OOP)** হলো একটি programming paradigm বা পদ্ধতি যেখানে software কে **objects** এর সমষ্টি হিসেবে design করা হয়। প্রতিটি object এর নিজস্ব **data (attributes/properties)** এবং **behavior (methods/functions)** থাকে।

OOP এর মূল ভিত্তি হলো real-world entities কে code এ represent করা।

### Real-Life Analogy (বাস্তব উদাহরণ)

চিন্তা করুন একটি **গাড়ি (Car)** সম্পর্কে:

| বিষয় | Real World | OOP |
|------|-----------|-----|
| গাড়ির ধরন বা blueprint | গাড়ির design/model | **Class** |
| একটি নির্দিষ্ট গাড়ি | আপনার নিজের গাড়ি | **Object** |
| গাড়ির রঙ, ব্র্যান্ড, গতি | গাড়ির বৈশিষ্ট্য | **Attributes / Properties** |
| চালানো, থামানো, হর্ন দেওয়া | গাড়ির কাজ | **Methods / Behaviors** |

**বাস্তব কথায়:** "Car" একটি class। আপনার বাসার Toyota Corolla একটি object। রঙ, ইঞ্জিন capacity হলো attribute। চালানো, ব্রেক করা হলো method।

### OOP এর চারটি মূল স্তম্ভ (Four Pillars of OOP)

```
┌─────────────────────────────────────────┐
│           OOP এর ৪টি Pillar            │
├──────────────┬──────────────────────────┤
│ Encapsulation│ Data লুকিয়ে রাখা         │
│ Abstraction  │ অপ্রয়োজনীয় detail লুকানো │
│ Inheritance  │ বৈশিষ্ট্য উত্তরাধিকার     │
│ Polymorphism │ একই নামে ভিন্ন কাজ       │
└──────────────┴──────────────────────────┘
```

### OOP ব্যবহারের কারণ (Why OOP?)

- **Reusability:** একবার লেখা code বারবার ব্যবহার করা যায়
- **Modularity:** বড় problem কে ছোট ছোট অংশে ভাগ করা যায়
- **Maintainability:** code সহজে update ও debug করা যায়
- **Scalability:** system সহজে বড় করা যায়
- **Real-world modeling:** বাস্তব জিনিসকে সহজে represent করা যায়

### OOP vs Procedural Programming তুলনা

| বিষয় | Procedural | OOP |
|------|-----------|-----|
| Focus | Functions/Procedures | Objects |
| Data | Global বা Parameter হিসেবে পাস | Object এর ভেতরে থাকে |
| Code Reuse | Function call | Inheritance & Composition |
| Security | কম | বেশি (Encapsulation) |
| উদাহরণ | C, Pascal | C++, Java, Python, C# |

### Interview-Style Explanation

**Interview প্রশ্ন:** "OOP কী? কেন আমরা OOP ব্যবহার করি?"

**ভালো উত্তর:**
> "OOP হলো একটি programming paradigm যেখানে আমরা software কে objects এর সমষ্টি হিসেবে design করি। প্রতিটি object এর নিজস্ব state (data) এবং behavior (methods) থাকে। আমরা OOP ব্যবহার করি কারণ এটি code reusability বাড়ায়, real-world problems সহজে model করা যায়, এবং large-scale applications maintain করা সহজ হয়। OOP এর চারটি মূল pillar হলো Encapsulation, Abstraction, Inheritance এবং Polymorphism।"

### Common Mistakes

- ❌ OOP মানে শুধু class লেখা — এটি ভুল ধারণা
- ❌ "OOP মানে Java" — Python, C++, C# সবই OOP support করে
- ✅ OOP একটি design philosophy, শুধু syntax নয়

### Follow-up Interview Questions

1. OOP এর ৪টি Pillar কী কী?
2. OOP কি সবসময় best approach?
3. Functional programming vs OOP — কোনটি কখন ব্যবহার করবেন?

---

## ১.২ Class এবং Object

### সংজ্ঞা (Definition)

**Class** হলো একটি **blueprint** বা template যা দিয়ে objects তৈরি করা হয়। এটি define করে object এর কী কী properties থাকবে এবং কী কী কাজ করতে পারবে।

**Object** হলো class এর একটি **instance** — অর্থাৎ class থেকে তৈরি একটি নির্দিষ্ট entity যার নিজস্ব memory এবং state আছে।

### Real-Life Analogy

| Blueprint | Object |
|-----------|--------|
| বাড়ির নকশা (design) | আসল বাড়ি |
| Cookie cutter (ছাঁচ) | Cookie |
| মানুষের ধারণা | আপনি নিজে |
| `Student` class | `রাফি`, `সুমাইয়া` নামের student |

### Code Example — C++

```cpp
#include <iostream>
#include <string>
using namespace std;

// Class definition (Blueprint)
class Student {
public:
    // Attributes (Properties)
    string name;
    int age;
    float cgpa;

    // Method (Behavior)
    void displayInfo() {
        cout << "Name: " << name << endl;
        cout << "Age: " << age << endl;
        cout << "CGPA: " << cgpa << endl;
    }

    void study() {
        cout << name << " is studying..." << endl;
    }
};

int main() {
    // Object creation
    Student student1;  // Object 1
    student1.name = "Rafi Ahmed";
    student1.age = 22;
    student1.cgpa = 3.75;

    Student student2;  // Object 2
    student2.name = "Sumaiya Islam";
    student2.age = 21;
    student2.cgpa = 3.90;

    // Method calls
    student1.displayInfo();
    student1.study();

    cout << "---" << endl;

    student2.displayInfo();

    return 0;
}
```

**Output:**
```
Name: Rafi Ahmed
Age: 22
CGPA: 3.75
Rafi Ahmed is studying...
---
Name: Sumaiya Islam
Age: 21
CGPA: 3.90
```

### Code Example — Java

```java
// Class definition
public class Student {
    // Attributes
    String name;
    int age;
    float cgpa;

    // Method
    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("CGPA: " + cgpa);
    }

    void study() {
        System.out.println(name + " is studying...");
    }

    public static void main(String[] args) {
        // Object creation
        Student s1 = new Student();
        s1.name = "Rafi Ahmed";
        s1.age = 22;
        s1.cgpa = 3.75f;

        Student s2 = new Student();
        s2.name = "Sumaiya Islam";
        s2.age = 21;
        s2.cgpa = 3.90f;

        s1.displayInfo();
        s1.study();
        System.out.println("---");
        s2.displayInfo();
    }
}
```

### গুরুত্বপূর্ণ পার্থক্য: Class vs Object

| বিষয় | Class | Object |
|------|-------|--------|
| প্রকৃতি | Template/Blueprint | Instance/Real entity |
| Memory | নিজে memory নেয় না | Memory allocate হয় |
| সংখ্যা | একটি class | অনেক objects |
| Define | `class` keyword দিয়ে | `new` keyword দিয়ে (Java/C++) |
| উদাহরণ | `Student` | `student1`, `student2` |

### Interview Tips

**প্রশ্ন:** "Class এবং Object এর পার্থক্য বলুন।"

**Memory Tip:** 
- Class = Cookie Cutter (ছাঁচ)
- Object = Cookie (তৈরি হওয়া জিনিস)

**Common Mistakes:**
- ❌ Class এবং Object কে একই মনে করা
- ❌ "Class থেকে শুধু একটি Object তৈরি হয়" — ভুল, অনেক হতে পারে
- ✅ প্রতিটি object এর নিজস্ব copy of attributes থাকে, কিন্তু methods share করা হয়

---

## ১.৩ Constructor এবং Destructor

### Constructor কী?

**Constructor** হলো একটি **special method** যা object তৈরি হওয়ার সময় **automatically call** হয়। এর কাজ হলো object কে **initialize** করা।

**Constructor এর বৈশিষ্ট্য:**
- Class এর নামের মতোই নাম হয়
- কোনো **return type** নেই (void ও না)
- Object create হওয়ার সময় automatically execute হয়
- Overload করা যায় (multiple constructors থাকতে পারে)

### Constructor এর প্রকারভেদ

```
Constructor এর ধরন
│
├── Default Constructor       → কোনো parameter নেই
├── Parameterized Constructor → parameter আছে
├── Copy Constructor          → অন্য object থেকে copy করে
└── Move Constructor (C++11)  → Ownership transfer করে
```

### Destructor কী?

**Destructor** হলো একটি special method যা object **destroy** হওয়ার সময় automatically call হয়। এর কাজ হলো allocated memory বা resources **free** করা।

**Destructor এর বৈশিষ্ট্য:**
- নামের আগে `~` (tilde) চিহ্ন থাকে (C++ এ)
- কোনো parameter নেই
- কোনো return type নেই
- **Overload করা যায় না** — শুধু একটি থাকে
- Java তে `finalize()` method (deprecated) বা Garbage Collector করে

### Code Example — C++

```cpp
#include <iostream>
#include <string>
using namespace std;

class BankAccount {
private:
    string ownerName;
    double balance;
    int accountNumber;

public:
    // 1. Default Constructor
    BankAccount() {
        ownerName = "Unknown";
        balance = 0.0;
        accountNumber = 0;
        cout << "Default Constructor called! Account created." << endl;
    }

    // 2. Parameterized Constructor
    BankAccount(string name, double initialBalance, int accNum) {
        ownerName = name;
        balance = initialBalance;
        accountNumber = accNum;
        cout << "Parameterized Constructor called! Account for "
             << ownerName << " created." << endl;
    }

    // 3. Copy Constructor
    BankAccount(const BankAccount& other) {
        ownerName = other.ownerName;
        balance = other.balance;
        accountNumber = other.accountNumber + 1; // নতুন account number
        cout << "Copy Constructor called! Account copied for "
             << ownerName << endl;
    }

    void showDetails() {
        cout << "Owner: " << ownerName
             << " | Balance: " << balance
             << " | Account#: " << accountNumber << endl;
    }

    // Destructor
    ~BankAccount() {
        cout << "Destructor called! Account for "
             << ownerName << " is being closed." << endl;
    }
};

int main() {
    cout << "=== Creating Objects ===" << endl;

    BankAccount acc1;                              // Default Constructor
    BankAccount acc2("Rafi Ahmed", 50000.0, 1001); // Parameterized
    BankAccount acc3(acc2);                        // Copy Constructor

    cout << "\n=== Account Details ===" << endl;
    acc1.showDetails();
    acc2.showDetails();
    acc3.showDetails();

    cout << "\n=== Program Ending (Destructors called) ===" << endl;
    // Destructors call হবে LIFO (Last In First Out) order এ
    return 0;
}
```

**Output:**
```
=== Creating Objects ===
Default Constructor called! Account created.
Parameterized Constructor called! Account for Rafi Ahmed created.
Copy Constructor called! Account copied for Rafi Ahmed

=== Account Details ===
Owner: Unknown | Balance: 0 | Account#: 0
Owner: Rafi Ahmed | Balance: 50000 | Account#: 1001
Owner: Rafi Ahmed | Balance: 50000 | Account#: 1002

=== Program Ending (Destructors called) ===
Destructor called! Account for Rafi Ahmed is being closed.
Destructor called! Account for Rafi Ahmed is being closed.
Destructor called! Account for Unknown is being closed.
```

### Code Example — Java

```java
public class BankAccount {
    private String ownerName;
    private double balance;
    private int accountNumber;

    // Default Constructor
    public BankAccount() {
        this.ownerName = "Unknown";
        this.balance = 0.0;
        this.accountNumber = 0;
        System.out.println("Default Constructor: Account created.");
    }

    // Parameterized Constructor
    public BankAccount(String name, double balance, int accNum) {
        this.ownerName = name;
        this.balance = balance;
        this.accountNumber = accNum;
        System.out.println("Parameterized Constructor: Account for " + name + " created.");
    }

    void showDetails() {
        System.out.println("Owner: " + ownerName + 
                           " | Balance: " + balance + 
                           " | Account#: " + accountNumber);
    }

    // Java তে Destructor নেই, Garbage Collector handles memory
    // finalize() deprecated — ব্যবহার করা উচিত নয়
    // AutoCloseable interface use করুন

    public static void main(String[] args) {
        BankAccount acc1 = new BankAccount();
        BankAccount acc2 = new BankAccount("Sumaiya", 75000.0, 2001);
        acc1.showDetails();
        acc2.showDetails();
    }
}
```

### Constructor vs Destructor তুলনা

| বিষয় | Constructor | Destructor |
|------|------------|-----------|
| কখন call হয় | Object তৈরির সময় | Object destroy হওয়ার সময় |
| উদ্দেশ্য | Initialize করা | Resources free করা |
| Parameters | থাকতে পারে | থাকে না |
| Return type | নেই | নেই |
| Overloading | সম্ভব | সম্ভব নয় |
| Java তে | `constructor()` | Garbage Collector |
| C++ তে | `ClassName()` | `~ClassName()` |
| সংখ্যা | একাধিক হতে পারে | শুধু একটি |

### Interview Tips

**প্রশ্ন:** "Constructor কি return করতে পারে?"

**উত্তর:** না। Constructor এর কোনো return type নেই। এমনকি `void`ও না। Constructor implicit ভাবে newly created object টিকে return করে।

**প্রশ্ন:** "Java তে Destructor আছে কি?"

**উত্তর:** Java তে traditional Destructor নেই। Java Garbage Collector automatically memory manage করে। পুরনো `finalize()` method টি Java 9 থেকে deprecated। Resource management এর জন্য `try-with-resources` এবং `AutoCloseable` interface ব্যবহার করা হয়।

### Common Mistakes

- ❌ Constructor এ return type দেওয়া (compile error হবে)
- ❌ Destructor এ parameter দেওয়ার চেষ্টা করা
- ❌ Java তে destructor আছে মনে করা
- ✅ C++ এ dynamic memory allocate করলে destructor এ `delete` করতে হবে

---

## ১.৪ Access Modifiers (অ্যাক্সেস মডিফায়ার)

### সংজ্ঞা

**Access Modifiers** হলো keywords যা class এর members (variables এবং methods) এর **visibility** এবং **accessibility** নিয়ন্ত্রণ করে।

### তিনটি প্রধান Access Modifier

```
Access Modifiers
│
├── public    → সবাই access করতে পারবে
├── private   → শুধু নিজের class
└── protected → নিজের class + subclass
```

### Detailed Access Rules

| Modifier | Same Class | Same Package | Subclass | Outside World |
|----------|-----------|--------------|----------|---------------|
| `public` | ✅ | ✅ | ✅ | ✅ |
| `protected` | ✅ | ✅ | ✅ | ❌ |
| `default` (Java) | ✅ | ✅ | ❌ | ❌ |
| `private` | ✅ | ❌ | ❌ | ❌ |

> **C++ Note:** C++ এ `default` নেই। Class এ default হলো `private`, struct এ default হলো `public`।

### Code Example — C++

```cpp
#include <iostream>
#include <string>
using namespace std;

class Employee {
public:
    string name;        // সবাই access করতে পারবে
    string department;

protected:
    double salary;      // Employee এবং তার subclass access করতে পারবে

private:
    string password;    // শুধু Employee class নিজে access করতে পারবে
    int employeeId;

public:
    // Constructor
    Employee(string n, string dept, double sal, string pass, int id) {
        name = n;
        department = dept;
        salary = sal;
        password = pass;  // private member নিজের class থেকে set করা যায়
        employeeId = id;
    }

    // public method দিয়ে private data access করা (Encapsulation)
    double getSalary() {
        return salary;
    }

    int getId() {
        return employeeId;
    }

    void displayPublicInfo() {
        cout << "Name: " << name << " | Dept: " << department << endl;
    }

    // private member এ access করার method
    bool verifyPassword(string inputPass) {
        return password == inputPass;
    }
};

class Manager : public Employee {
public:
    Manager(string n, string dept, double sal, string pass, int id)
        : Employee(n, dept, sal, pass, id) {}

    void showManagerSalary() {
        // protected member subclass থেকে access করা যায়
        cout << name << "'s salary: " << salary << endl;

        // private member subclass থেকে access করা যায় না
        // cout << password;  // ERROR! ❌
    }
};

int main() {
    Employee emp("Rafi Ahmed", "Engineering", 85000, "secret123", 1001);

    // public member — directly access করা যায়
    cout << emp.name << endl;       // ✅
    cout << emp.department << endl; // ✅

    // protected member — outside থেকে access করা যায় না
    // cout << emp.salary;          // ❌ ERROR

    // private member — কোনোভাবেই outside থেকে না
    // cout << emp.password;        // ❌ ERROR

    // public methods দিয়ে private data access করুন
    cout << "Salary: " << emp.getSalary() << endl;  // ✅
    cout << "ID: " << emp.getId() << endl;           // ✅

    cout << "Password correct: "
         << emp.verifyPassword("secret123") << endl; // ✅

    // Subclass test
    Manager mgr("Sumaiya Islam", "HR", 120000, "mgr456", 2001);
    mgr.showManagerSalary();

    return 0;
}
```

### Code Example — Java

```java
public class Employee {
    public String name;          // সবাই access পাবে
    protected double salary;     // subclass এবং same package
    private String password;     // শুধু এই class
    private int employeeId;

    public Employee(String name, double salary, String password, int id) {
        this.name = name;
        this.salary = salary;
        this.password = password;
        this.employeeId = id;
    }

    // Getter methods (public interface for private data)
    public double getSalary() { return salary; }
    public int getId() { return employeeId; }
    public boolean verifyPassword(String input) {
        return password.equals(input);
    }
}

class Manager extends Employee {
    public Manager(String name, double salary, String pass, int id) {
        super(name, salary, pass, id);
    }

    public void showSalary() {
        // protected — subclass access করতে পারে
        System.out.println(name + "'s salary: " + salary);

        // private — subclass access করতে পারে না
        // System.out.println(password); // ❌ Compile Error
    }
}
```

### Real-Life Analogy

- **public** = বাড়ির সামনের দরজা — সবাই আসতে পারে
- **protected** = পরিবারের সদস্যদের জন্য ঘর — আত্মীয়রাও পারে
- **private** = নিজের ব্যক্তিগত diary — শুধু নিজে পড়তে পারবে

### Interview Questions

**প্রশ্ন:** "Private member কি inherit হয়?"

**উত্তর:** হ্যাঁ, private members **inherit** হয় কিন্তু **directly access** করা যায় না subclass থেকে। Subclass সেগুলো inherit করে কিন্তু parent class এর public/protected methods দিয়ে সেগুলোতে access করতে হয়।

**Common Mistake:**
- ❌ "Private means not inherited" — ভুল! Inherited হয়, কিন্তু directly accessible না
- ✅ Private members memory তে exist করে, শুধু direct access blocked

---

## ১.৫ Encapsulation (এনক্যাপসুলেশন)

### সংজ্ঞা

**Encapsulation** হলো OOP এর একটি fundamental concept যেখানে **data (attributes)** এবং **methods** কে একসাথে এক জায়গায় (class) রাখা হয় এবং data কে **বাইরের world থেকে লুকিয়ে রাখা হয়** — শুধুমাত্র নির্দিষ্ট methods এর মাধ্যমে access দেওয়া হয়।

সহজ কথায়: **"Data hiding + Data binding"**

### Real-Life Analogy

**ক্যাপসুল ওষুধ:** একটি ক্যাপসুলে ভেতরে ওষুধ থাকে — আপনি সরাসরি ওষুধ স্পর্শ করতে পারবেন না, ক্যাপসুলের মাধ্যমেই নিতে হবে।

**ATM Machine:** আপনি ATM এর ভেতরের mechanism দেখতে পান না। Card দিন, PIN দিন, টাকা নিন। ভেতরের কাজ লুকানো।

### Encapsulation এর সুবিধা

- **Data Security:** বাইরে থেকে সরাসরি data change করা যায় না
- **Validation:** Setter methods এ validation logic যোগ করা যায়
- **Flexibility:** Implementation পরিবর্তন করলেও বাইরের code ভাঙে না
- **Maintainability:** Code easily maintain করা যায়

### Code Example — C++ (Getter & Setter)

```cpp
#include <iostream>
#include <string>
#include <stdexcept>
using namespace std;

class BankAccount {
private:
    string ownerName;
    double balance;
    string accountNumber;
    int pin;

public:
    // Constructor
    BankAccount(string name, string accNum, int userPin) {
        ownerName = name;
        accountNumber = accNum;
        balance = 0.0;
        pin = userPin;
    }

    // Getter methods
    string getOwnerName() const {
        return ownerName;
    }

    double getBalance() const {
        return balance;
    }

    string getAccountNumber() const {
        return accountNumber;
    }

    // Setter with validation
    void setOwnerName(string newName) {
        if (newName.empty()) {
            throw invalid_argument("Name cannot be empty!");
        }
        ownerName = newName;
    }

    // Deposit method with validation
    void deposit(double amount) {
        if (amount <= 0) {
            cout << "❌ Invalid deposit amount!" << endl;
            return;
        }
        balance += amount;
        cout << "✅ Deposited: " << amount
             << " | New Balance: " << balance << endl;
    }

    // Withdraw method with validation
    bool withdraw(double amount, int userPin) {
        if (userPin != pin) {
            cout << "❌ Wrong PIN! Transaction failed." << endl;
            return false;
        }
        if (amount <= 0 || amount > balance) {
            cout << "❌ Invalid amount or insufficient funds!" << endl;
            return false;
        }
        balance -= amount;
        cout << "✅ Withdrawn: " << amount
             << " | Remaining Balance: " << balance << endl;
        return true;
    }

    void showStatement() const {
        cout << "=== Account Statement ===" << endl;
        cout << "Owner: " << ownerName << endl;
        cout << "Account#: " << accountNumber << endl;
        cout << "Balance: BDT " << balance << endl;
    }
};

int main() {
    BankAccount myAccount("Rafi Ahmed", "BD-1001", 1234);

    myAccount.deposit(50000);
    myAccount.deposit(25000);
    myAccount.withdraw(10000, 1234);  // সঠিক PIN
    myAccount.withdraw(10000, 9999);  // ভুল PIN

    // balance সরাসরি access করা যাবে না
    // myAccount.balance = 999999;  // ❌ ERROR! Private

    myAccount.showStatement();

    return 0;
}
```

**Output:**
```
✅ Deposited: 50000 | New Balance: 50000
✅ Deposited: 25000 | New Balance: 75000
✅ Withdrawn: 10000 | Remaining Balance: 65000
❌ Wrong PIN! Transaction failed.
=== Account Statement ===
Owner: Rafi Ahmed
Account#: BD-1001
Balance: BDT 65000
```

### Code Example — Java

```java
public class Student {
    private String name;
    private int age;
    private float cgpa;
    private String rollNumber;

    public Student(String name, int age, String roll) {
        this.name = name;
        setAge(age);  // validation সহ
        this.rollNumber = roll;
        this.cgpa = 0.0f;
    }

    // Getters
    public String getName() { return name; }
    public int getAge() { return age; }
    public float getCgpa() { return cgpa; }
    public String getRollNumber() { return rollNumber; }

    // Setters with validation
    public void setAge(int age) {
        if (age < 15 || age > 60) {
            throw new IllegalArgumentException("Age must be between 15 and 60");
        }
        this.age = age;
    }

    public void setCgpa(float cgpa) {
        if (cgpa < 0.0f || cgpa > 4.0f) {
            throw new IllegalArgumentException("CGPA must be between 0.0 and 4.0");
        }
        this.cgpa = cgpa;
    }

    @Override
    public String toString() {
        return "Student{name='" + name + "', age=" + age + 
               ", cgpa=" + cgpa + ", roll='" + rollNumber + "'}";
    }

    public static void main(String[] args) {
        Student s = new Student("Sumaiya Islam", 21, "CSE-2021-001");
        s.setCgpa(3.85f);
        System.out.println(s);

        // s.cgpa = 5.0f;  // ❌ Compile Error! Private
        // s.setCgpa(5.0f); // ❌ Runtime Exception!
    }
}
```

### Interview-Style Explanation

**প্রশ্ন:** "Encapsulation কী? এটি কীভাবে কাজ করে?"

**ভালো উত্তর:**
> "Encapsulation হলো data এবং methods কে একসাথে class এ bundle করা এবং private access modifier দিয়ে data কে বাইরের world থেকে protect করা। শুধুমাত্র public getter/setter methods দিয়ে data access করতে হয়। এতে আমরা setter এ validation logic যোগ করতে পারি, যা data integrity নিশ্চিত করে। উদাহরণ: BankAccount class এ balance private রাখলে কেউ সরাসরি balance বাড়াতে পারবে না — deposit() method call করতে হবে।"

### Common Mistakes

- ❌ সব fields public রাখা — Encapsulation ভাঙে
- ❌ Getter/Setter ছাড়াই private data রাখা — data useless হয়ে যায়
- ❌ Setter এ কোনো validation না রাখা — Encapsulation এর benefit নষ্ট
- ✅ Private fields + Public methods = Proper Encapsulation

---

## ১.৬ Abstraction (অ্যাবস্ট্রাকশন)

### সংজ্ঞা

**Abstraction** হলো user কে শুধু **প্রয়োজনীয় তথ্য** দেখানো এবং **অপ্রয়োজনীয় implementation details লুকিয়ে রাখা**।

**সহজ কথায়:** "What to show, what to hide"

### Encapsulation vs Abstraction পার্থক্য

| বিষয় | Encapsulation | Abstraction |
|------|-------------|------------|
| উদ্দেশ্য | Data protect করা | Complexity লুকানো |
| How | Private + Getter/Setter | Abstract class + Interface |
| Focus | Data hiding | Implementation hiding |
| উদাহরণ | `balance` private রাখা | `drive()` method — engine কীভাবে চলে জানা দরকার নেই |

### Real-Life Analogy

- **TV Remote:** আপনি Channel পরিবর্তন করেন — কীভাবে signal যায় জানেন না
- **Driving a car:** আপনি গাড়ি চালান — engine এর ভেতরের কাজ জানা দরকার নেই
- **ATM:** Card swipe করুন, টাকা নিন — ভেতরের banking system জানা দরকার নেই

### Abstraction Achieve করার উপায়

```
Abstraction
│
├── Abstract Class   → partial abstraction (0-100%)
└── Interface        → pure abstraction (100%) [Java]
    (Pure Virtual)   → C++ এ abstract class দিয়ে
```

### Code Example — C++

```cpp
#include <iostream>
#include <string>
using namespace std;

// Abstract Class (Abstraction)
class Shape {
protected:
    string color;

public:
    Shape(string c) : color(c) {}

    // Pure virtual functions — subclass অবশ্যই implement করবে
    virtual double calculateArea() = 0;
    virtual double calculatePerimeter() = 0;
    virtual void draw() = 0;

    // Concrete method
    void showColor() {
        cout << "Color: " << color << endl;
    }

    virtual ~Shape() {}
};

// Concrete class
class Circle : public Shape {
private:
    double radius;
    const double PI = 3.14159;

public:
    Circle(double r, string color) : Shape(color), radius(r) {}

    double calculateArea() override {
        return PI * radius * radius;
    }

    double calculatePerimeter() override {
        return 2 * PI * radius;
    }

    void draw() override {
        cout << "Drawing a circle with radius " << radius << endl;
    }
};

class Rectangle : public Shape {
private:
    double width, height;

public:
    Rectangle(double w, double h, string color)
        : Shape(color), width(w), height(h) {}

    double calculateArea() override {
        return width * height;
    }

    double calculatePerimeter() override {
        return 2 * (width + height);
    }

    void draw() override {
        cout << "Drawing a rectangle " << width << "x" << height << endl;
    }
};

int main() {
    // Shape s("red");  // ❌ Cannot instantiate abstract class

    Shape* shapes[2];
    shapes[0] = new Circle(5.0, "Red");
    shapes[1] = new Rectangle(4.0, 6.0, "Blue");

    for (int i = 0; i < 2; i++) {
        shapes[i]->draw();
        shapes[i]->showColor();
        cout << "Area: " << shapes[i]->calculateArea() << endl;
        cout << "Perimeter: " << shapes[i]->calculatePerimeter() << endl;
        cout << "---" << endl;
    }

    delete shapes[0];
    delete shapes[1];

    return 0;
}
```

### Code Example — Java

```java
// Abstract class
abstract class Animal {
    private String name;
    private int age;

    public Animal(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Abstract methods — subclass must implement
    public abstract void makeSound();
    public abstract String getType();

    // Concrete method — common behavior
    public void displayInfo() {
        System.out.println(getType() + " Name: " + name + ", Age: " + age);
    }

    public String getName() { return name; }
}

class Dog extends Animal {
    private String breed;

    public Dog(String name, int age, String breed) {
        super(name, age);
        this.breed = breed;
    }

    @Override
    public void makeSound() {
        System.out.println(getName() + " says: Woof! Woof!");
    }

    @Override
    public String getType() { return "Dog"; }
}

class Cat extends Animal {
    public Cat(String name, int age) {
        super(name, age);
    }

    @Override
    public void makeSound() {
        System.out.println(getName() + " says: Meow!");
    }

    @Override
    public String getType() { return "Cat"; }
}

public class AbstractionDemo {
    public static void main(String[] args) {
        Animal[] animals = {
            new Dog("Bruno", 3, "Labrador"),
            new Cat("Whiskers", 2)
        };

        for (Animal a : animals) {
            a.displayInfo();
            a.makeSound();
            System.out.println();
        }
    }
}
```

### Interview Tips

**প্রশ্ন:** "Abstraction এবং Encapsulation এর পার্থক্য বলুন।"

**Memory Trick:**
- **Encapsulation** = How we **protect** data (private fields + getters/setters)
- **Abstraction** = How we **simplify** complex systems (abstract class + interface)

**প্রশ্ন:** "Abstract class কি instantiate করা যায়?"

**উত্তর:** না। Abstract class directly instantiate করা যায় না কারণ এতে incomplete methods (pure virtual/abstract) থাকে। Reference বা pointer তৈরি করা যায়, কিন্তু object তৈরি করা যায় না।

---

## ১.৭ Inheritance (ইনহেরিটেন্স)

### সংজ্ঞা

**Inheritance** হলো একটি mechanism যেখানে একটি class (child/derived/subclass) অন্য একটি class (parent/base/superclass) এর **properties এবং methods পায় বা উত্তরাধিকার সূত্রে গ্রহণ করে**।

**মূল কথা:** Code reuse এবং "is-a" relationship।

### Real-Life Analogy

- সন্তান বাবা-মার বৈশিষ্ট্য পায় — চোখের রঙ, উচ্চতা
- কিন্তু সন্তান নিজস্ব বৈশিষ্ট্যও রাখতে পারে
- এবং কিছু বৈশিষ্ট্য override করতে পারে (নিজের মতো করে)

### Inheritance এর প্রকারভেদ

```
Inheritance এর ধরন
│
├── Single Inheritance       → A → B (একটি parent, একটি child)
├── Multi-level Inheritance  → A → B → C (chain)
├── Hierarchical Inheritance → A → B, A → C (একটি parent, অনেক child)
├── Multiple Inheritance     → A, B → C (Java তে নেই, C++ এ আছে)
└── Hybrid Inheritance       → উপরের combination
```

### Code Example — C++ (সব ধরন)

```cpp
#include <iostream>
#include <string>
using namespace std;

// ===== 1. Single Inheritance =====
class Animal {
protected:
    string name;
    int age;

public:
    Animal(string n, int a) : name(n), age(a) {}

    void eat() {
        cout << name << " is eating." << endl;
    }

    void sleep() {
        cout << name << " is sleeping." << endl;
    }

    virtual void makeSound() {
        cout << name << " makes a sound." << endl;
    }
};

// Single Inheritance: Dog inherits from Animal
class Dog : public Animal {
private:
    string breed;

public:
    Dog(string n, int a, string b) : Animal(n, a), breed(b) {}

    void fetch() {
        cout << name << " (" << breed << ") is fetching!" << endl;
    }

    void makeSound() override {
        cout << name << " says: Woof!" << endl;
    }
};

// ===== 2. Multi-level Inheritance =====
class GuideDog : public Dog {
private:
    string owner;

public:
    GuideDog(string n, int a, string b, string o)
        : Dog(n, a, b), owner(o) {}

    void guide() {
        cout << name << " is guiding " << owner << "." << endl;
    }
};

// ===== 3. Hierarchical Inheritance =====
class Cat : public Animal {
public:
    Cat(string n, int a) : Animal(n, a) {}

    void purr() {
        cout << name << " is purring." << endl;
    }

    void makeSound() override {
        cout << name << " says: Meow!" << endl;
    }
};

// ===== 4. Multiple Inheritance (C++ only) =====
class Flyable {
public:
    void fly() {
        cout << "Flying..." << endl;
    }
};

class FlyingDog : public Dog, public Flyable {
public:
    FlyingDog(string n, int a, string b) : Dog(n, a, b) {}
};

int main() {
    cout << "=== Single Inheritance ===" << endl;
    Dog dog("Bruno", 3, "Labrador");
    dog.eat();          // Inherited from Animal
    dog.makeSound();    // Overridden
    dog.fetch();        // Dog's own method

    cout << "\n=== Multi-level Inheritance ===" << endl;
    GuideDog guide("Max", 4, "German Shepherd", "Rafi");
    guide.eat();        // From Animal
    guide.fetch();      // From Dog
    guide.guide();      // GuideDog's own
    guide.makeSound();  // Overridden in Dog

    cout << "\n=== Hierarchical Inheritance ===" << endl;
    Cat cat("Whiskers", 2);
    cat.eat();         // From Animal
    cat.makeSound();   // Overridden
    cat.purr();        // Cat's own

    cout << "\n=== Multiple Inheritance ===" << endl;
    FlyingDog fd("Sky", 2, "Mixed");
    fd.eat();      // From Animal
    fd.fetch();    // From Dog
    fd.fly();      // From Flyable

    return 0;
}
```

### Code Example — Java

```java
// Java Multiple Inheritance (Interface দিয়ে)
interface Swimmable {
    void swim();
}

interface Flyable {
    void fly();
}

abstract class Animal {
    protected String name;

    public Animal(String name) {
        this.name = name;
    }

    public abstract void makeSound();

    public void eat() {
        System.out.println(name + " is eating.");
    }
}

// Single Inheritance
class Dog extends Animal implements Swimmable {
    public Dog(String name) {
        super(name);
    }

    @Override
    public void makeSound() {
        System.out.println(name + " says: Woof!");
    }

    @Override
    public void swim() {
        System.out.println(name + " is swimming!");
    }
}

// Multi-level Inheritance
class GoldenRetriever extends Dog {
    public GoldenRetriever(String name) {
        super(name);
    }

    public void fetch() {
        System.out.println(name + " (Golden Retriever) is fetching!");
    }
}

public class InheritanceDemo {
    public static void main(String[] args) {
        GoldenRetriever gr = new GoldenRetriever("Buddy");
        gr.eat();       // From Animal
        gr.makeSound(); // From Dog
        gr.swim();      // From Swimmable interface
        gr.fetch();     // Own method
    }
}
```

### Inheritance Terminology

| Term | অর্থ |
|------|------|
| Parent / Base / Super class | যে class থেকে inherit করা হয় |
| Child / Derived / Sub class | যে class inherit করে |
| `extends` (Java) | Inheritance keyword |
| `:` public (C++) | Inheritance syntax |
| `super()` / `super.method()` | Parent class call করা |
| `is-a` relationship | Inheritance এর মূল সম্পর্ক |

### Interview Tips

**প্রশ্ন:** "Java তে Multiple Inheritance কেন নেই?"

**উত্তর:** Java তে class দিয়ে multiple inheritance নেই কারণ **Diamond Problem** হতে পারে — দুটি parent class এ একই method থাকলে কোনটি call হবে বোঝা যায় না। Java এই সমস্যা avoid করতে multiple inheritance of classes বাদ দিয়েছে, তবে **Interface** দিয়ে এই কাজ করা যায়।

**প্রশ্ন:** "Composition vs Inheritance — কখন কোনটি ব্যবহার করবেন?"

**উত্তর:** 
- "**is-a**" relationship → Inheritance (Dog **is a** Animal)
- "**has-a**" relationship → Composition (Car **has a** Engine)
- Inheritance এর চেয়ে Composition prefer করুন (Favor Composition over Inheritance)

---

## ১.৮ Polymorphism (পলিমরফিজম)

### সংজ্ঞা

**Polymorphism** মানে "**অনেক রূপ**" (Poly = many, Morph = forms)।

এটি হলো OOP এর একটি concept যেখানে **একই নামের method বা operation বিভিন্ন context এ বিভিন্নভাবে কাজ করতে পারে।**

### Polymorphism এর প্রকারভেদ

```
Polymorphism
│
├── Compile-time Polymorphism (Static Binding)
│   ├── Method Overloading
│   └── Operator Overloading (C++)
│
└── Runtime Polymorphism (Dynamic Binding)
    └── Method Overriding (Virtual Functions)
```

### Real-Life Analogy

- **"+" অপারেটর:** `2 + 3 = 5` (integer), `"Hello" + " World" = "Hello World"` (string)
- **কথা বলা:** মানুষ কথা বলে (হাসতে হাসতে), বিড়াল কথা বলে (Meow), কুকুর কথা বলে (Woof) — সবাই "কথা বলে" কিন্তু ভিন্নভাবে
- **Shape.draw():** Circle আঁকলে গোল হবে, Rectangle আঁকলে চতুর্ভুজ হবে — same method call, different behavior

### Type 1: Method Overloading (Compile-time)

```cpp
#include <iostream>
#include <string>
using namespace std;

class Calculator {
public:
    // Same method name, different parameters
    int add(int a, int b) {
        cout << "Adding two integers: ";
        return a + b;
    }

    double add(double a, double b) {
        cout << "Adding two doubles: ";
        return a + b;
    }

    int add(int a, int b, int c) {
        cout << "Adding three integers: ";
        return a + b + c;
    }

    string add(string a, string b) {
        cout << "Concatenating strings: ";
        return a + b;
    }
};

int main() {
    Calculator calc;

    cout << calc.add(5, 3) << endl;
    cout << calc.add(3.14, 2.71) << endl;
    cout << calc.add(1, 2, 3) << endl;
    cout << calc.add("Hello, ", "World!") << endl;

    return 0;
}
```

**Output:**
```
Adding two integers: 8
Adding two doubles: 5.85
Adding three integers: 6
Concatenating strings: Hello, World!
```

### Type 2: Method Overriding (Runtime Polymorphism)

```cpp
#include <iostream>
#include <string>
#include <vector>
using namespace std;

class Shape {
protected:
    string name;

public:
    Shape(string n) : name(n) {}

    virtual double getArea() {
        return 0.0;
    }

    virtual void describe() {
        cout << "Shape: " << name << " | Area: " << getArea() << endl;
    }

    virtual ~Shape() {}
};

class Circle : public Shape {
    double radius;

public:
    Circle(double r) : Shape("Circle"), radius(r) {}

    double getArea() override {
        return 3.14159 * radius * radius;
    }
};

class Rectangle : public Shape {
    double width, height;

public:
    Rectangle(double w, double h)
        : Shape("Rectangle"), width(w), height(h) {}

    double getArea() override {
        return width * height;
    }
};

class Triangle : public Shape {
    double base, height;

public:
    Triangle(double b, double h)
        : Shape("Triangle"), base(b), height(h) {}

    double getArea() override {
        return 0.5 * base * height;
    }
};

int main() {
    // Polymorphism in action — same type, different objects
    vector<Shape*> shapes;
    shapes.push_back(new Circle(5.0));
    shapes.push_back(new Rectangle(4.0, 6.0));
    shapes.push_back(new Triangle(3.0, 8.0));

    cout << "=== Runtime Polymorphism Demo ===" << endl;

    // Same method call — different behavior based on actual type
    for (Shape* s : shapes) {
        s->describe();  // Which getArea() is called? Decided at RUNTIME!
    }

    // Cleanup
    for (Shape* s : shapes) {
        delete s;
    }

    return 0;
}
```

**Output:**
```
=== Runtime Polymorphism Demo ===
Shape: Circle | Area: 78.5398
Shape: Rectangle | Area: 24
Shape: Triangle | Area: 12
```

### Java Example — Runtime Polymorphism

```java
abstract class PaymentMethod {
    protected String userName;
    protected double amount;

    public PaymentMethod(String user, double amt) {
        this.userName = user;
        this.amount = amt;
    }

    // Method to override
    public abstract void processPayment();

    public void showReceipt() {
        System.out.println("User: " + userName + " | Amount: BDT " + amount);
        processPayment();
    }
}

class BkashPayment extends PaymentMethod {
    private String bkashNumber;

    public BkashPayment(String user, double amt, String number) {
        super(user, amt);
        this.bkashNumber = number;
    }

    @Override
    public void processPayment() {
        System.out.println("✅ bKash payment of BDT " + amount +
                           " processed to " + bkashNumber);
    }
}

class NagadPayment extends PaymentMethod {
    public NagadPayment(String user, double amt) {
        super(user, amt);
    }

    @Override
    public void processPayment() {
        System.out.println("✅ Nagad payment of BDT " + amount + " processed!");
    }
}

class CreditCardPayment extends PaymentMethod {
    private String cardNumber;

    public CreditCardPayment(String user, double amt, String card) {
        super(user, amt);
        this.cardNumber = card.substring(card.length() - 4); // Last 4 digits
    }

    @Override
    public void processPayment() {
        System.out.println("✅ Credit card ****" + cardNumber +
                           " payment of BDT " + amount + " processed!");
    }
}

public class PolymorphismDemo {
    public static void main(String[] args) {
        // Same reference type (PaymentMethod), different object types
        PaymentMethod[] payments = {
            new BkashPayment("Rafi", 500.0, "01712345678"),
            new NagadPayment("Sumaiya", 750.0),
            new CreditCardPayment("Tanvir", 2000.0, "4111111111111234")
        };

        System.out.println("=== Payment Processing ===");
        for (PaymentMethod p : payments) {
            p.showReceipt(); // Runtime Polymorphism!
            System.out.println("---");
        }
    }
}
```

### Polymorphism Summary Table

| বিষয় | Compile-time | Runtime |
|------|-------------|---------|
| অন্য নাম | Static/Early Binding | Dynamic/Late Binding |
| কখন নির্ধারিত হয় | Compile time এ | Runtime এ |
| কীভাবে | Overloading | Overriding |
| কোনটি call হবে | Parameter type দেখে | Actual object type দেখে |
| Performance | তুলনামূলক দ্রুত | কিছুটা ধীর (vtable lookup) |
| Keyword | — | `virtual` (C++), `@Override` (Java) |

---

## ১.৯ Method Overloading vs Method Overriding

### সংজ্ঞা

**Overloading:** একই class এ **একই নামের** কিন্তু **ভিন্ন signature** এর একাধিক method থাকা।

**Overriding:** Child class এ **parent class এর method কে redefine** করা।

### বিস্তারিত তুলনা

| বিষয় | Overloading | Overriding |
|------|------------|-----------|
| কোথায় হয় | Same class এ | Parent-Child class এ |
| Method নাম | Same | Same |
| Parameters | ভিন্ন (type/number/order) | Same |
| Return type | ভিন্ন হতে পারে | Same হতে হবে (covariant allowed) |
| Binding | Compile-time (Static) | Runtime (Dynamic) |
| Inheritance | দরকার নেই | দরকার |
| `virtual` keyword | দরকার নেই | C++ এ parent এ `virtual` লাগে |
| `@Override` | নেই | Java তে recommended |

### Code Example — Overloading vs Overriding

```cpp
#include <iostream>
#include <string>
using namespace std;

class MathHelper {
public:
    // === OVERLOADING: Same class, different parameters ===
    int multiply(int a, int b) {
        cout << "[int*int] ";
        return a * b;
    }

    double multiply(double a, double b) {
        cout << "[double*double] ";
        return a * b;
    }

    int multiply(int a, int b, int c) {
        cout << "[int*int*int] ";
        return a * b * c;
    }
};

class Animal {
public:
    virtual void speak() {
        cout << "Animal speaks" << endl;
    }

    void breathe() {
        cout << "Animal breathes" << endl;
    }
};

class Dog : public Animal {
public:
    // === OVERRIDING: Same signature, different behavior ===
    void speak() override {
        cout << "Dog says: Woof!" << endl;
    }

    // Overloading within Dog class
    void fetch() {
        cout << "Dog fetches!" << endl;
    }

    void fetch(string item) {
        cout << "Dog fetches: " << item << endl;
    }
};

int main() {
    cout << "=== OVERLOADING ===" << endl;
    MathHelper m;
    cout << m.multiply(3, 4) << endl;
    cout << m.multiply(3.14, 2.71) << endl;
    cout << m.multiply(2, 3, 4) << endl;

    cout << "\n=== OVERRIDING ===" << endl;
    Animal* a = new Dog();  // Polymorphism
    a->speak();             // Runtime: "Dog says: Woof!" — not "Animal speaks"

    cout << "\n=== OVERLOADING in Dog ===" << endl;
    Dog d;
    d.fetch();
    d.fetch("ball");

    delete a;
    return 0;
}
```

### সহজে মনে রাখার Trick

```
Overloading:
  Same name + Different PARAMS = Compile-time decision
  "Load" করুন একই নামে বিভিন্ন version

Overriding:
  Same name + Same PARAMS + Inheritance = Runtime decision
  Parent এর method কে "Override" (overwrite) করুন
```

### Common Interview Tricks

**প্রশ্ন:** "Return type পরিবর্তন করলে কি overloading হয়?"

**উত্তর:** না। C++ এবং Java উভয়তে শুধু return type পরিবর্তন করা overloading হয় না — এটি compile error দেবে। Parameter এর type, number, বা order পরিবর্তন করতে হবে।

**প্রশ্ন:** "Private method কি override হয়?"

**উত্তর:** না। Private methods inherit হয় না, তাই override করার প্রশ্নই নেই। Child class এ same name এর method লিখলে সেটি overriding নয়, সেটি একটি নতুন method।

**প্রশ্ন:** "Static method কি override হয়?"

**উত্তর:** না। Static methods class level এ থাকে, object level এ নয়। Java তে এটিকে **Method Hiding** বলে, Overriding নয়। C++ এ static methods virtual হতে পারে না।

---

## ১.৯ Quick Reference: PART 1 Summary Table

| Concept | সংক্ষিপ্ত সংজ্ঞা | Key Keyword |
|---------|-----------------|------------|
| OOP | Object-based programming paradigm | Class, Object |
| Class | Blueprint/Template | `class` |
| Object | Class এর instance | `new` |
| Constructor | Object তৈরির সময় auto-call | `ClassName()` |
| Destructor | Object destroy এর সময় auto-call | `~ClassName()` (C++) |
| Access Modifier | Visibility control | `public`, `private`, `protected` |
| Encapsulation | Data hiding + binding | Private + Getter/Setter |
| Abstraction | Complexity hiding | Abstract class, Interface |
| Inheritance | Parent থেকে properties পাওয়া | `extends`, `:` |
| Polymorphism | একই নামে ভিন্ন আচরণ | `virtual`, `override` |
| Overloading | Same name, different params | Compile-time |
| Overriding | Parent method redefine | Runtime, `virtual` |

---

## ১.১০ PART 1 — Interview Questions & Answers

### Rapid-Fire Questions

**Q1: OOP এর ৪টি Pillar কী?**  
A: Encapsulation, Abstraction, Inheritance, Polymorphism

**Q2: Class এবং Object এর পার্থক্য?**  
A: Class হলো Blueprint, Object হলো সেই blueprint থেকে তৈরি real entity।

**Q3: Constructor এর return type কী?**  
A: কোনো return type নেই — এমনকি void ও না।

**Q4: Java তে Destructor আছে কি?**  
A: না। Java তে Garbage Collector memory manage করে।

**Q5: Overloading এবং Overriding এর পার্থক্য?**  
A: Overloading = same class + different params (compile-time). Overriding = parent-child + same params (runtime).

**Q6: Private member কি inherit হয়?**  
A: হ্যাঁ, কিন্তু directly access করা যায় না — parent এর public/protected methods দিয়ে access করতে হয়।

**Q7: Abstract class instantiate করা যায় কি?**  
A: না। Abstract class এ অসম্পূর্ণ methods থাকে।

**Q8: Encapsulation এবং Abstraction এর পার্থক্য?**  
A: Encapsulation = data protect করা (private fields)। Abstraction = complexity লুকানো (abstract class/interface)।

**Q9: Java তে multiple inheritance কেন নেই?**  
A: Diamond Problem avoid করতে। Interface দিয়ে কাজ করা যায়।

**Q10: Runtime polymorphism কীভাবে কাজ করে?**  
A: Virtual table (vtable) এর মাধ্যমে runtime এ সঠিক method খুঁজে call করা হয়।

---

> **⚠️ PART 1 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part2"></a>

# PART 2: Advanced OOP (উন্নত ধারণাসমূহ)

> **📍 এই PART এর Sections:** [২.১ Static vs Dynamic Binding](#২১-static-binding-vs-dynamic-binding) · [২.২ Interface](#২২-interface-ইন্টারফেস) · [২.৩ Abstract Class vs Interface](#২৩-abstract-class-vs-interface) · [২.৪ Virtual Function](#২৪-virtual-function-এবং-pure-virtual-function) · [২.৫ Copy Constructor](#২৫-copy-constructor-এবং-deep-vs-shallow-copy) · [২.৬ Diamond Problem](#২৬-diamond-problem-ডায়মন্ড-সমস্যা) · [২.৭ SOLID](#২৭-solid-principles) · [২.৮ Dependency Injection](#২৮-dependency-injection-di) · [২.৯ Coupling & Cohesion](#২৯-coupling-এবং-cohesion) · [২.১০ Interview Qs](#২১০-part-2--interview-questions--answers)

---

## ২.১ Static Binding vs Dynamic Binding

### সংজ্ঞা

**Binding** মানে হলো একটি function call এর সাথে সেই function এর actual code কে **link করা**।

**Static Binding (Early Binding):**
Compile time এ নির্ধারণ করা হয় কোন function call হবে। Compiler দেখে reference/variable এর **declared type** — actual object type নয়।

**Dynamic Binding (Late Binding):**
Runtime এ নির্ধারণ করা হয় কোন function call হবে। Actual object এর type দেখে সঠিক function খোঁজা হয়। `virtual` keyword এর মাধ্যমে C++ এ এটি কাজ করে।

### Real-Life Analogy

- **Static:** বই কেনার আগেই ঠিক করা — "আমি physics বই কিনব" (compile time decision)
- **Dynamic:** দোকানে গিয়ে দেখে সিদ্ধান্ত নেওয়া — actual stock দেখে (runtime decision)

### Code Example — C++

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    // Static binding — NOT virtual
    void staticSpeak() {
        cout << "Animal (static): Some sound" << endl;
    }

    // Dynamic binding — virtual
    virtual void dynamicSpeak() {
        cout << "Animal (dynamic): Some sound" << endl;
    }

    virtual ~Animal() {}
};

class Dog : public Animal {
public:
    void staticSpeak() {       // Hides parent's method — NOT overriding
        cout << "Dog (static): Woof!" << endl;
    }

    void dynamicSpeak() override {  // True overriding
        cout << "Dog (dynamic): Woof!" << endl;
    }
};

class Cat : public Animal {
public:
    void staticSpeak() {
        cout << "Cat (static): Meow!" << endl;
    }

    void dynamicSpeak() override {
        cout << "Cat (dynamic): Meow!" << endl;
    }
};

int main() {
    Animal* a1 = new Dog();
    Animal* a2 = new Cat();

    cout << "=== Static Binding (compile-time) ===" << endl;
    // Compiler sees Animal* — calls Animal's version regardless of actual type
    a1->staticSpeak();   // Animal (static): Some sound  ← WRONG object!
    a2->staticSpeak();   // Animal (static): Some sound  ← WRONG object!

    cout << "\n=== Dynamic Binding (runtime) ===" << endl;
    // Runtime checks actual object type — calls correct override
    a1->dynamicSpeak();  // Dog (dynamic): Woof!   ✅ Correct!
    a2->dynamicSpeak();  // Cat (dynamic): Meow!   ✅ Correct!

    delete a1;
    delete a2;
    return 0;
}
```

**Output:**
```
=== Static Binding (compile-time) ===
Animal (static): Some sound
Animal (static): Some sound

=== Dynamic Binding (runtime) ===
Dog (dynamic): Woof!
Cat (dynamic): Meow!
```

### তুলনা সারণি

| বিষয় | Static Binding | Dynamic Binding |
|------|---------------|----------------|
| কখন নির্ধারিত | Compile time | Runtime |
| Speed | দ্রুত | তুলনামূলক ধীর |
| Flexibility | কম | বেশি |
| Keyword | — | `virtual` (C++) |
| Polymorphism | না | হ্যাঁ |
| Method type | Normal, overloaded | Virtual, overridden |
| Java তে | Non-overridden methods | All overridden methods |

### Interview Tips

**প্রশ্ন:** "Java তে কি সব methods dynamically bound?"

**উত্তর:** Java তে instance methods default এ dynamically bound (Java implicitly `virtual`)। তবে `static`, `private`, এবং `final` methods statically bound কারণ এগুলো override হয় না।

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.২ Interface (ইন্টারফেস)

### সংজ্ঞা

**Interface** হলো একটি **pure abstract contract** যা define করে কী কী methods থাকতে **হবে** — কিন্তু সেগুলো কীভাবে implement হবে তা বলে না।

- Java তে `interface` keyword ব্যবহার হয়
- C++ এ সব methods pure virtual রেখে abstract class দিয়ে interface simulate করা হয়
- Interface শুধু **"what"** বলে, **"how"** বলে না

### Real-Life Analogy

**চাকরির contract:** Contract বলে "আপনাকে report লিখতে হবে, meeting করতে হবে" — কিন্তু কীভাবে করবেন সেটা আপনার ব্যাপার। Interface ঠিক এই contract এর মতো।

### Code Example — Java

```java
// Interface — pure contract
interface Printable {
    // Interface এ সব methods implicitly public abstract
    void print();
    void printPreview();

    // Java 8+ — default method (optional implementation)
    default void printToFile(String filename) {
        System.out.println("Saving to file: " + filename);
    }

    // Java 8+ — static method
    static String getSupportedFormats() {
        return "PDF, DOC, TXT";
    }
}

interface Saveable {
    void save();
    void load(String path);
}

// Class implementing multiple interfaces
class Document implements Printable, Saveable {
    private String content;
    private String title;

    public Document(String title, String content) {
        this.title = title;
        this.content = content;
    }

    @Override
    public void print() {
        System.out.println("Printing: " + title);
        System.out.println("Content: " + content);
    }

    @Override
    public void printPreview() {
        System.out.println("Preview of: " + title + " (first 50 chars)");
        System.out.println(content.substring(0, Math.min(50, content.length())));
    }

    @Override
    public void save() {
        System.out.println("Saving document: " + title);
    }

    @Override
    public void load(String path) {
        System.out.println("Loading document from: " + path);
    }
}

class Spreadsheet implements Printable, Saveable {
    private String sheetName;

    public Spreadsheet(String name) {
        this.sheetName = name;
    }

    @Override
    public void print() {
        System.out.println("Printing spreadsheet: " + sheetName);
    }

    @Override
    public void printPreview() {
        System.out.println("Spreadsheet preview: " + sheetName);
    }

    @Override
    public void save() {
        System.out.println("Saving spreadsheet: " + sheetName);
    }

    @Override
    public void load(String path) {
        System.out.println("Loading spreadsheet from: " + path);
    }
}

public class InterfaceDemo {
    // Method accepts any Printable — programming to interface
    public static void printAll(Printable[] items) {
        for (Printable item : items) {
            item.print();
            System.out.println("---");
        }
    }

    public static void main(String[] args) {
        Printable[] items = {
            new Document("OOP Guide", "Object-Oriented Programming is..."),
            new Spreadsheet("Budget 2026")
        };

        printAll(items);

        // Default method
        items[0].printToFile("oop_guide.pdf");

        // Static method
        System.out.println("Formats: " + Printable.getSupportedFormats());
    }
}
```

### C++ Interface Simulation

```cpp
#include <iostream>
#include <string>
using namespace std;

// C++ Interface (all pure virtual)
class IPayable {
public:
    virtual double calculatePay() = 0;
    virtual void generatePaySlip() = 0;
    virtual ~IPayable() {}
};

class IReportable {
public:
    virtual void generateReport() = 0;
    virtual ~IReportable() {}
};

// Implementing "multiple interfaces" via multiple inheritance
class Employee : public IPayable, public IReportable {
private:
    string name;
    double hourlyRate;
    int hoursWorked;

public:
    Employee(string n, double rate, int hours)
        : name(n), hourlyRate(rate), hoursWorked(hours) {}

    double calculatePay() override {
        return hourlyRate * hoursWorked;
    }

    void generatePaySlip() override {
        cout << "=== Pay Slip ===" << endl;
        cout << "Employee: " << name << endl;
        cout << "Hours: " << hoursWorked
             << " | Rate: " << hourlyRate << endl;
        cout << "Total Pay: BDT " << calculatePay() << endl;
    }

    void generateReport() override {
        cout << "Employee Report — " << name
             << " worked " << hoursWorked << " hours." << endl;
    }
};

int main() {
    Employee emp("Rafi Ahmed", 500.0, 160);
    emp.generatePaySlip();
    emp.generateReport();

    // Programming to interface
    IPayable* payable = &emp;
    cout << "Pay: BDT " << payable->calculatePay() << endl;

    return 0;
}
```

### Interface সম্পর্কে গুরুত্বপূর্ণ তথ্য

| বিষয় | Java Interface | C++ (simulated) |
|------|--------------|----------------|
| Keyword | `interface` | `class` with pure virtual |
| Variables | `public static final` | নেই |
| Methods | `public abstract` (default) | `= 0` (pure virtual) |
| Constructor | নেই | নেই |
| Multiple implementation | হ্যাঁ | হ্যাঁ |
| Java 8+ | `default`, `static` methods | — |

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৩ Abstract Class vs Interface

### সংজ্ঞা পার্থক্য

**Abstract Class:** কিছু methods implemented (concrete) এবং কিছু unimplemented (abstract) থাকতে পারে। Partial abstraction।

**Interface:** সব methods abstract (Java 8 এর আগে)। Pure contract। 100% abstraction।

### বিস্তারিত তুলনা

| বিষয় | Abstract Class | Interface |
|------|--------------|-----------|
| Keyword | `abstract class` | `interface` |
| Methods | Concrete + Abstract | Abstract (default/static Java 8+) |
| Variables | যেকোনো type | `public static final` |
| Constructor | থাকতে পারে | নেই |
| Multiple inherit | ❌ (Java) | ✅ |
| Access modifier | যেকোনো | `public` (implicit) |
| "is-a" vs "can-do" | "is-a" relationship | "can-do" capability |
| কখন ব্যবহার | Shared code + contract | Pure contract |

### কখন কোনটি ব্যবহার করবেন

```
Abstract Class ব্যবহার করুন যখন:
  ✅ Related classes এ shared code আছে
  ✅ "is-a" relationship আছে (Dog is-a Animal)
  ✅ Non-public members দরকার
  ✅ State (instance variables) দরকার

Interface ব্যবহার করুন যখন:
  ✅ Unrelated classes এ common behavior দরকার
  ✅ Multiple inheritance দরকার
  ✅ "can-do" capability define করতে (Flyable, Printable)
  ✅ API/Contract define করতে
```

### Code Example — Java (পার্থক্য স্পষ্ট করা)

```java
// Abstract Class — "is-a" + shared code
abstract class Vehicle {
    protected String brand;
    protected int speed;
    private int manufactureYear;  // private possible

    public Vehicle(String brand, int year) {
        this.brand = brand;
        this.manufactureYear = year;
        this.speed = 0;
    }

    // Concrete method — shared by all vehicles
    public void accelerate(int amount) {
        speed += amount;
        System.out.println(brand + " speed: " + speed + " km/h");
    }

    public void brake() {
        speed = Math.max(0, speed - 20);
        System.out.println(brand + " braked. Speed: " + speed + " km/h");
    }

    // Abstract method — each vehicle implements differently
    public abstract String getFuelType();
    public abstract void startEngine();

    public int getYear() { return manufactureYear; }
}

// Interfaces — "can-do" capabilities
interface GPSEnabled {
    void getLocation();
    void setDestination(String dest);
}

interface ElectricChargeable {
    void charge(int minutes);
    int getBatteryPercentage();
}

// Concrete class inheriting abstract + implementing interfaces
class ElectricCar extends Vehicle implements GPSEnabled, ElectricChargeable {
    private int batteryLevel;
    private String currentLocation;

    public ElectricCar(String brand, int year) {
        super(brand, year);
        this.batteryLevel = 100;
        this.currentLocation = "Dhaka";
    }

    @Override
    public String getFuelType() { return "Electric"; }

    @Override
    public void startEngine() {
        System.out.println(brand + " electric motor starts silently.");
    }

    @Override
    public void getLocation() {
        System.out.println("Current location: " + currentLocation);
    }

    @Override
    public void setDestination(String dest) {
        System.out.println("Navigating to: " + dest);
    }

    @Override
    public void charge(int minutes) {
        batteryLevel = Math.min(100, batteryLevel + minutes / 2);
        System.out.println("Charged for " + minutes + " mins. Battery: " + batteryLevel + "%");
    }

    @Override
    public int getBatteryPercentage() { return batteryLevel; }
}

public class AbstractVsInterface {
    public static void main(String[] args) {
        ElectricCar tesla = new ElectricCar("Tesla Model 3", 2024);
        tesla.startEngine();
        tesla.accelerate(60);
        tesla.getLocation();
        tesla.setDestination("Chittagong");
        tesla.charge(30);
        System.out.println("Fuel: " + tesla.getFuelType());
        System.out.println("Battery: " + tesla.getBatteryPercentage() + "%");
    }
}
```

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৪ Virtual Function এবং Pure Virtual Function

### Virtual Function কী?

**Virtual Function** হলো C++ এর একটি function যা `virtual` keyword দিয়ে declare করা হয় এবং child class এ **override** করা যায়। Parent class pointer/reference দিয়ে call করলে runtime এ সঠিক child class এর version call হয় — এটাই **Runtime Polymorphism**।

### Pure Virtual Function কী?

**Pure Virtual Function** হলো এমন virtual function যার parent class এ **কোনো implementation নেই** — শুধু declaration আছে। `= 0` দিয়ে declare করা হয়।

```cpp
virtual void functionName() = 0;  // Pure Virtual
```

যে class এ কমপক্ষে একটি pure virtual function আছে সেটি **Abstract Class** — instantiate করা যাবে না।

### Code Example — C++

```cpp
#include <iostream>
#include <string>
#include <vector>
using namespace std;

class Notification {
protected:
    string recipient;
    string message;

public:
    Notification(string r, string m) : recipient(r), message(m) {}

    // Regular virtual — has default implementation, can be overridden
    virtual void logSent() {
        cout << "[LOG] Notification sent to: " << recipient << endl;
    }

    // Pure virtual — subclass MUST implement
    virtual void send() = 0;
    virtual string getType() = 0;

    // Non-virtual — cannot be overridden via polymorphism
    void showDetails() {
        cout << "Type: " << getType()
             << " | To: " << recipient
             << " | Msg: " << message << endl;
    }

    virtual ~Notification() {}
};

class EmailNotification : public Notification {
private:
    string emailAddress;

public:
    EmailNotification(string r, string m, string email)
        : Notification(r, m), emailAddress(email) {}

    void send() override {
        cout << "📧 Email sent to " << emailAddress
             << ": " << message << endl;
    }

    string getType() override { return "Email"; }

    // Overriding virtual (optional — but can customize)
    void logSent() override {
        cout << "[EMAIL LOG] Sent to " << emailAddress << endl;
    }
};

class SMSNotification : public Notification {
private:
    string phoneNumber;

public:
    SMSNotification(string r, string m, string phone)
        : Notification(r, m), phoneNumber(phone) {}

    void send() override {
        cout << "📱 SMS sent to " << phoneNumber
             << ": " << message << endl;
    }

    string getType() override { return "SMS"; }
    // logSent() NOT overridden — uses parent's default
};

class PushNotification : public Notification {
private:
    string deviceToken;

public:
    PushNotification(string r, string m, string token)
        : Notification(r, m), deviceToken(token) {}

    void send() override {
        cout << "🔔 Push notification to device [" << deviceToken
             << "]: " << message << endl;
    }

    string getType() override { return "Push"; }
};

// Notification sender — works with ANY Notification type
void sendAll(vector<Notification*>& notifications) {
    for (Notification* n : notifications) {
        n->showDetails();
        n->send();        // Runtime polymorphism — correct send() called
        n->logSent();     // Virtual — correct version called
        cout << endl;
    }
}

int main() {
    // Notification n("x", "y");  // ❌ Cannot instantiate abstract class

    vector<Notification*> queue;
    queue.push_back(new EmailNotification("Rafi", "Interview tomorrow!", "rafi@gmail.com"));
    queue.push_back(new SMSNotification("Sumaiya", "Meeting at 3pm", "01712345678"));
    queue.push_back(new PushNotification("Tanvir", "App update available", "tok_abc123"));

    cout << "=== Sending All Notifications ===" << endl;
    sendAll(queue);

    for (Notification* n : queue) delete n;
    return 0;
}
```

### Virtual Destructor — কেন জরুরি?

```cpp
class Base {
public:
    Base() { cout << "Base constructor" << endl; }

    // Without virtual destructor:
    // ~Base() { cout << "Base destructor" << endl; }  // ❌ MEMORY LEAK!

    // With virtual destructor:
    virtual ~Base() { cout << "Base destructor" << endl; }  // ✅
};

class Derived : public Base {
    int* data;
public:
    Derived() {
        data = new int[100];
        cout << "Derived constructor" << endl;
    }
    ~Derived() {
        delete[] data;  // Memory freed
        cout << "Derived destructor" << endl;
    }
};

int main() {
    Base* b = new Derived();
    delete b;
    // Without virtual ~Base(): only ~Base() called — Derived's data LEAKS!
    // With virtual ~Base(): both ~Derived() and ~Base() called correctly ✅
}
```

### Virtual vs Pure Virtual তুলনা

| বিষয় | Virtual | Pure Virtual |
|------|---------|-------------|
| Syntax | `virtual void f()` | `virtual void f() = 0` |
| Implementation | Parent এ আছে | নেই |
| Override | Optional | Mandatory (subclass এ) |
| Abstract class | না (হতে পারে) | হ্যাঁ (class abstract হয়) |
| Object create | পারবে | পারবে না |

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৫ Copy Constructor এবং Deep vs Shallow Copy

### Copy Constructor কী?

**Copy Constructor** হলো একটি special constructor যা **অন্য একটি object এর data দিয়ে নতুন object তৈরি করে**।

```cpp
ClassName(const ClassName& other);  // Copy Constructor signature
```

### কখন Copy Constructor call হয়?

```cpp
MyClass obj2 = obj1;          // Copy constructor
MyClass obj3(obj1);           // Copy constructor
void func(MyClass obj) {}     // Pass by value — copy constructor
MyClass func() { return obj; }// Return by value — copy constructor
```

### Shallow Copy কী?

**Shallow Copy** মানে — শুধু values copy করা। যদি pointer থাকে, **pointer টি copy হয় — pointed data নয়**। ফলে দুটি object একই memory location point করে → **Dangling pointer** সমস্যা।

### Deep Copy কী?

**Deep Copy** মানে — pointer যে memory point করে সেই **data ও আলাদাভাবে copy করা**। প্রতিটি object এর নিজস্ব independent memory থাকে।

### Code Example — C++

```cpp
#include <iostream>
#include <cstring>
using namespace std;

// ===== Shallow Copy Problem =====
class ShallowExample {
public:
    char* name;
    int age;

    ShallowExample(const char* n, int a) {
        name = new char[strlen(n) + 1];
        strcpy(name, n);
        age = a;
        cout << "Constructor: " << name << endl;
    }

    // Default copy constructor = SHALLOW copy (compiler generated)
    // This causes problems!

    ~ShallowExample() {
        cout << "Destructor: " << name << endl;
        delete[] name;  // DOUBLE DELETE if shallow copied!
    }
};

// ===== Deep Copy Solution =====
class DeepExample {
public:
    char* name;
    int age;
    int* scores;
    int scoreCount;

    DeepExample(const char* n, int a, int* s, int count) {
        // Allocate and copy name
        name = new char[strlen(n) + 1];
        strcpy(name, n);
        age = a;

        // Allocate and copy scores array
        scoreCount = count;
        scores = new int[count];
        for (int i = 0; i < count; i++) {
            scores[i] = s[i];
        }

        cout << "Constructor: " << name << endl;
    }

    // Deep Copy Constructor
    DeepExample(const DeepExample& other) {
        // Deep copy name
        name = new char[strlen(other.name) + 1];
        strcpy(name, other.name);
        age = other.age;

        // Deep copy scores — NEW memory allocation!
        scoreCount = other.scoreCount;
        scores = new int[scoreCount];
        for (int i = 0; i < scoreCount; i++) {
            scores[i] = other.scores[i];
        }

        cout << "Deep Copy Constructor: " << name << endl;
    }

    // Copy Assignment Operator
    DeepExample& operator=(const DeepExample& other) {
        if (this == &other) return *this;  // Self-assignment check

        // Free existing memory
        delete[] name;
        delete[] scores;

        // Deep copy
        name = new char[strlen(other.name) + 1];
        strcpy(name, other.name);
        age = other.age;
        scoreCount = other.scoreCount;
        scores = new int[scoreCount];
        for (int i = 0; i < scoreCount; i++) {
            scores[i] = other.scores[i];
        }

        cout << "Copy Assignment: " << name << endl;
        return *this;
    }

    void showInfo() const {
        cout << "Name: " << name << " | Age: " << age << " | Scores: ";
        for (int i = 0; i < scoreCount; i++) {
            cout << scores[i];
            if (i < scoreCount - 1) cout << ", ";
        }
        cout << endl;
    }

    void modifyFirstScore(int val) {
        scores[0] = val;
    }

    ~DeepExample() {
        cout << "Destructor: " << name << endl;
        delete[] name;
        delete[] scores;
    }
};

int main() {
    cout << "=== Deep Copy Demo ===" << endl;
    int marks[] = {85, 90, 78, 92, 88};

    DeepExample student1("Rafi Ahmed", 22, marks, 5);
    DeepExample student2 = student1;  // Deep Copy Constructor

    cout << "\nBefore modification:" << endl;
    student1.showInfo();
    student2.showInfo();

    // Modifying student2 should NOT affect student1
    student2.modifyFirstScore(99);
    strcpy(student2.name, "Sumaiya Islam");

    cout << "\nAfter modifying student2:" << endl;
    student1.showInfo();  // student1 unchanged ✅
    student2.showInfo();

    cout << "\nDestructors will be called:" << endl;
    return 0;
}
```

**Output:**
```
=== Deep Copy Demo ===
Constructor: Rafi Ahmed
Deep Copy Constructor: Rafi Ahmed

Before modification:
Name: Rafi Ahmed | Age: 22 | Scores: 85, 90, 78, 92, 88
Name: Rafi Ahmed | Age: 22 | Scores: 85, 90, 78, 92, 88

After modifying student2:
Name: Rafi Ahmed | Age: 22 | Scores: 85, 90, 78, 92, 88   ← Unchanged ✅
Name: Sumaiya Islam | Age: 22 | Scores: 99, 90, 78, 92, 88

Destructors will be called:
Destructor: Sumaiya Islam
Destructor: Rafi Ahmed
```

### Deep vs Shallow Copy তুলনা

| বিষয় | Shallow Copy | Deep Copy |
|------|-------------|----------|
| কী copy হয় | Values + pointers | Values + pointed data |
| Memory | Shared | Independent |
| Pointer | Same address | নতুন address |
| Problem | Double delete, dangling pointer | বেশি memory use |
| কখন নিরাপদ | No dynamic memory | Dynamic memory আছে |
| Compiler generated | Shallow | নিজে লিখতে হয় |

### The Rule of Three (C++)

> **যদি এগুলোর একটি define করতে হয়, সবগুলোই করুন:**
> 1. Destructor
> 2. Copy Constructor
> 3. Copy Assignment Operator

C++11 এ **Rule of Five** — Move Constructor ও Move Assignment Operator যোগ হয়েছে।

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৬ Diamond Problem (ডায়মন্ড সমস্যা)

### সমস্যাটি কী?

**Diamond Problem** হলো Multiple Inheritance এ একটি ambiguity সমস্যা যেখানে একটি class দুটি parent class থেকে inherit করে এবং উভয় parent class একই grandparent class থেকে inherit করে। ফলে grandparent এর members দুইবার copy হয়।

### Diagram

```
         Animal
        /      \
      Dog      Cat
        \      /
        DogCat (?)
```

`DogCat` এ `Animal` এর members দুইটি copy আসে — কোনটি ব্যবহার করব?

### Code Example — C++ এ সমস্যা ও সমাধান

```cpp
#include <iostream>
using namespace std;

// === PROBLEM: Without Virtual Inheritance ===
class Animal_Bad {
public:
    string name;
    Animal_Bad() : name("Animal") {
        cout << "Animal_Bad constructor" << endl;
    }
    void eat() { cout << name << " is eating." << endl; }
};

class Dog_Bad : public Animal_Bad {
public:
    Dog_Bad() { cout << "Dog_Bad constructor" << endl; }
};

class Cat_Bad : public Animal_Bad {
public:
    Cat_Bad() { cout << "Cat_Bad constructor" << endl; }
};

class DogCat_Bad : public Dog_Bad, public Cat_Bad {
public:
    DogCat_Bad() { cout << "DogCat_Bad constructor" << endl; }
};

// === SOLUTION: Virtual Inheritance ===
class Animal {
public:
    string name;
    Animal() : name("Animal") {
        cout << "Animal constructor (only once!)" << endl;
    }
    void eat() { cout << name << " is eating." << endl; }
};

// Virtual inheritance — shares single copy of Animal
class Dog : virtual public Animal {
public:
    Dog() { cout << "Dog constructor" << endl; }
    void bark() { cout << "Woof!" << endl; }
};

class Cat : virtual public Animal {
public:
    Cat() { cout << "Cat constructor" << endl; }
    void meow() { cout << "Meow!" << endl; }
};

class DogCat : public Dog, public Cat {
public:
    DogCat() { cout << "DogCat constructor" << endl; }
};

int main() {
    cout << "=== PROBLEM (without virtual) ===" << endl;
    DogCat_Bad hybrid_bad;
    // hybrid_bad.eat();     // ❌ AMBIGUOUS! Which Animal::eat()?
    // hybrid_bad.name;      // ❌ AMBIGUOUS!
    hybrid_bad.Dog_Bad::eat();   // Must specify which path
    hybrid_bad.Cat_Bad::eat();   // Two separate eat() calls

    cout << "\n=== SOLUTION (with virtual inheritance) ===" << endl;
    DogCat hybrid;
    hybrid.eat();    // ✅ No ambiguity — only ONE Animal
    hybrid.bark();   // From Dog
    hybrid.meow();   // From Cat
    hybrid.name = "HybridPet";  // ✅ One copy of name

    return 0;
}
```

### Java তে Diamond Problem এর সমাধান

Java class এ multiple inheritance নেই তাই diamond problem নেই।  
কিন্তু Java 8+ এ interface এ `default` methods থাকায় একটি রূপ আসতে পারে:

```java
interface A {
    default void hello() {
        System.out.println("Hello from A");
    }
}

interface B extends A {
    default void hello() {
        System.out.println("Hello from B");
    }
}

interface C extends A {
    default void hello() {
        System.out.println("Hello from C");
    }
}

// Class must explicitly override to resolve ambiguity
class D implements B, C {
    @Override
    public void hello() {
        B.super.hello();  // Explicitly choosing B's version
        // OR: C.super.hello();
        // OR: custom implementation
        System.out.println("Hello from D (resolved)");
    }
}

public class DiamondJava {
    public static void main(String[] args) {
        D obj = new D();
        obj.hello();
    }
}
```

### সহজে মনে রাখার Trick

> **Diamond = দুই বাবা, এক দাদু → কোন বাবার মাধ্যমে দাদুর সম্পদ পাব?**  
> Solution: `virtual inheritance` (C++) বা multiple class inheritance avoid (Java)

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৭ SOLID Principles

**SOLID** হলো ৫টি object-oriented design principle এর সংক্ষিপ্ত রূপ যা Robert C. Martin ("Uncle Bob") প্রবর্তন করেন। এগুলো মেনে চললে software maintainable, scalable, এবং testable হয়।

```
S — Single Responsibility Principle (SRP)
O — Open/Closed Principle (OCP)
L — Liskov Substitution Principle (LSP)
I — Interface Segregation Principle (ISP)
D — Dependency Inversion Principle (DIP)
```

---

### S — Single Responsibility Principle (SRP)

> **"A class should have only ONE reason to change."**
> একটি class এর শুধু **একটি কাজ** থাকা উচিত।

```java
// ❌ VIOLATION — একটি class অনেক কিছু করছে
class Employee_Bad {
    private String name;
    private double salary;

    // Responsibility 1: Employee data management
    public void calculateSalary() { /* ... */ }

    // Responsibility 2: Database operation
    public void saveToDatabase() { /* SQL queries */ }

    // Responsibility 3: Report generation
    public void generateReport() { /* HTML/PDF generation */ }

    // Responsibility 4: Email sending
    public void sendPaySlipEmail() { /* SMTP logic */ }
}

// ✅ CORRECT — প্রতিটি class একটি কাজ করে
class Employee {
    private String name;
    private double salary;

    public Employee(String name, double salary) {
        this.name = name;
        this.salary = salary;
    }

    public double calculateSalary() {
        return salary;
    }

    public String getName() { return name; }
    public double getSalary() { return salary; }
}

class EmployeeRepository {
    public void save(Employee emp) {
        System.out.println("Saving " + emp.getName() + " to DB...");
    }

    public Employee findById(int id) {
        return null; // DB query
    }
}

class PaySlipGenerator {
    public String generate(Employee emp) {
        return "Pay Slip for " + emp.getName() + ": BDT " + emp.getSalary();
    }
}

class EmailService {
    public void sendPaySlip(Employee emp, String paySlip) {
        System.out.println("Sending email to " + emp.getName());
        System.out.println("Content: " + paySlip);
    }
}
```

---

### O — Open/Closed Principle (OCP)

> **"Open for extension, Closed for modification."**
> নতুন feature যোগ করতে existing code **পরিবর্তন না করে** নতুন code **যোগ করুন**।

```java
// ❌ VIOLATION — নতুন shape যোগ করতে এই method পরিবর্তন করতে হবে
class AreaCalculator_Bad {
    public double calculateArea(Object shape) {
        if (shape instanceof Circle) {
            Circle c = (Circle) shape;
            return Math.PI * c.radius * c.radius;
        } else if (shape instanceof Rectangle) {
            Rectangle r = (Rectangle) shape;
            return r.width * r.height;
        }
        // নতুন shape আসলে এখানে আরও code যোগ করতে হবে ❌
        return 0;
    }
}

// ✅ CORRECT — Open for extension
interface Shape {
    double calculateArea();  // Each shape knows its own area
}

class Circle implements Shape {
    private double radius;
    public Circle(double r) { this.radius = r; }

    @Override
    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}

class Rectangle implements Shape {
    private double width, height;
    public Rectangle(double w, double h) { this.width = w; this.height = h; }

    @Override
    public double calculateArea() {
        return width * height;
    }
}

// নতুন Shape — existing code পরিবর্তন ছাড়াই
class Triangle implements Shape {
    private double base, height;
    public Triangle(double b, double h) { this.base = b; this.height = h; }

    @Override
    public double calculateArea() {
        return 0.5 * base * height;
    }
}

class AreaCalculator {
    public double totalArea(Shape[] shapes) {
        double total = 0;
        for (Shape s : shapes) {
            total += s.calculateArea();  // Works for ANY Shape ✅
        }
        return total;
    }
}
```

---

### L — Liskov Substitution Principle (LSP)

> **"Subclass objects should be replaceable by their parent class objects without breaking the program."**
> Child class কে parent class এর জায়গায় ব্যবহার করা যাবে — behavior ভাঙা ছাড়াই।

```java
// ❌ VIOLATION — Square extends Rectangle কিন্তু behavior ভাঙে
class Rectangle {
    protected double width, height;

    public void setWidth(double w) { this.width = w; }
    public void setHeight(double h) { this.height = h; }
    public double getArea() { return width * height; }
}

class Square extends Rectangle {
    @Override
    public void setWidth(double w) {
        this.width = w;
        this.height = w;  // Square এ width = height
    }

    @Override
    public void setHeight(double h) {
        this.width = h;
        this.height = h;
    }
}

// LSP ভাঙার প্রমাণ
void testRectangle(Rectangle r) {
    r.setWidth(4);
    r.setHeight(5);
    // Expected area: 20 — but Square gives 25! ❌
    assert r.getArea() == 20 : "Expected 20, got " + r.getArea();
}

// ✅ CORRECT — আলাদা hierarchy
interface Shape2D {
    double getArea();
}

class RectangleFixed implements Shape2D {
    private double width, height;
    public RectangleFixed(double w, double h) { this.width = w; this.height = h; }

    @Override
    public double getArea() { return width * height; }
}

class SquareFixed implements Shape2D {
    private double side;
    public SquareFixed(double s) { this.side = s; }

    @Override
    public double getArea() { return side * side; }
}
```

---

### I — Interface Segregation Principle (ISP)

> **"Clients should not be forced to depend on interfaces they don't use."**
> একটি বড় interface এর বদলে **ছোট ছোট specific interfaces** তৈরি করুন।

```java
// ❌ VIOLATION — সব কিছু এক interface এ
interface Worker_Bad {
    void work();
    void eat();
    void sleep();
    void attendMeeting();
    void writeCode();
    void testCode();
}

// Robot কে eat(), sleep() implement করতে বাধ্য হয় ❌
class Robot implements Worker_Bad {
    public void work() { System.out.println("Robot working..."); }
    public void eat() { throw new UnsupportedOperationException("Robots don't eat!"); }
    public void sleep() { throw new UnsupportedOperationException("Robots don't sleep!"); }
    public void attendMeeting() { System.out.println("Robot in meeting..."); }
    public void writeCode() { System.out.println("Robot coding..."); }
    public void testCode() { System.out.println("Robot testing..."); }
}

// ✅ CORRECT — Segregated interfaces
interface Workable {
    void work();
}

interface Eatable {
    void eat();
}

interface Sleepable {
    void sleep();
}

interface Developer {
    void writeCode();
    void testCode();
}

// Human implements all relevant
class HumanDeveloper implements Workable, Eatable, Sleepable, Developer {
    public void work() { System.out.println("Human working..."); }
    public void eat() { System.out.println("Human eating lunch..."); }
    public void sleep() { System.out.println("Human sleeping..."); }
    public void writeCode() { System.out.println("Human writing Java..."); }
    public void testCode() { System.out.println("Human running tests..."); }
}

// Robot implements only relevant
class RobotDeveloper implements Workable, Developer {
    public void work() { System.out.println("Robot working 24/7..."); }
    public void writeCode() { System.out.println("Robot generating code..."); }
    public void testCode() { System.out.println("Robot running automated tests..."); }
}
```

---

### D — Dependency Inversion Principle (DIP)

> **"High-level modules should not depend on low-level modules. Both should depend on abstractions."**
> Concrete implementation এর উপর নির্ভর না করে **abstractions (interface/abstract class)** এর উপর নির্ভর করুন।

```java
// ❌ VIOLATION — High-level class directly depends on low-level class
class MySQLDatabase {
    public void save(String data) {
        System.out.println("Saving to MySQL: " + data);
    }
}

class UserService_Bad {
    private MySQLDatabase db = new MySQLDatabase();  // Tightly coupled ❌

    public void createUser(String username) {
        // Business logic
        String userData = "User: " + username;
        db.save(userData);  // Depends on MySQL directly
    }
}

// ✅ CORRECT — Depend on abstraction
interface Database {
    void save(String data);
    String findById(int id);
}

class MySQLDatabase_Fixed implements Database {
    @Override
    public void save(String data) {
        System.out.println("MySQL: Saving → " + data);
    }

    @Override
    public String findById(int id) {
        return "MySQL: Found user " + id;
    }
}

class MongoDatabase implements Database {
    @Override
    public void save(String data) {
        System.out.println("MongoDB: Inserting document → " + data);
    }

    @Override
    public String findById(int id) {
        return "MongoDB: Found document " + id;
    }
}

class UserService {
    private Database db;  // Depends on abstraction ✅

    // Dependency Injection via Constructor
    public UserService(Database database) {
        this.db = database;
    }

    public void createUser(String username) {
        String userData = "User: " + username + " | Created: 2026";
        db.save(userData);
    }

    public String getUser(int id) {
        return db.findById(id);
    }
}

public class DIPDemo {
    public static void main(String[] args) {
        // Inject MySQL
        UserService mysqlService = new UserService(new MySQLDatabase_Fixed());
        mysqlService.createUser("Rafi Ahmed");

        // Switch to MongoDB — UserService code unchanged ✅
        UserService mongoService = new UserService(new MongoDatabase());
        mongoService.createUser("Sumaiya Islam");
    }
}
```

### SOLID Quick Reference

| Principle | মূল কথা | Trick |
|-----------|---------|-------|
| **S**RP | একটি class = একটি কাজ | "One job, one class" |
| **O**CP | extend করুন, modify নয় | "Open door, closed wall" |
| **L**SP | Child = Parent এর replacement | "Sub is-a Super always" |
| **I**SP | ছোট interface, সব implement নয় | "Fat interface = bad" |
| **D**IP | Abstraction এ নির্ভর করুন | "Depend on contracts" |

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৮ Dependency Injection (DI)

### সংজ্ঞা

**Dependency Injection** হলো একটি design pattern যেখানে কোনো class তার dependencies নিজে create করে না — বরং **বাইরে থেকে provide করা হয়**।

### Injection এর তিনটি উপায়

```
Dependency Injection
│
├── Constructor Injection  → Constructor দিয়ে
├── Setter Injection       → Setter method দিয়ে
└── Interface Injection    → Interface method দিয়ে
```

```java
// Constructor Injection (সবচেয়ে preferred)
class OrderService {
    private final PaymentGateway paymentGateway;
    private final NotificationService notifier;

    // Dependencies injected via constructor
    public OrderService(PaymentGateway gateway, NotificationService notifier) {
        this.paymentGateway = gateway;
        this.notifier = notifier;
    }

    public void placeOrder(String item, double price, String customerPhone) {
        System.out.println("Processing order: " + item);
        boolean paid = paymentGateway.processPayment(price);
        if (paid) {
            notifier.sendConfirmation(customerPhone, item);
        }
    }
}

interface PaymentGateway {
    boolean processPayment(double amount);
}

interface NotificationService {
    void sendConfirmation(String contact, String item);
}

class BkashGateway implements PaymentGateway {
    public boolean processPayment(double amount) {
        System.out.println("bKash: Processing BDT " + amount);
        return true;
    }
}

class SMSNotifier implements NotificationService {
    public void sendConfirmation(String phone, String item) {
        System.out.println("SMS to " + phone + ": Order for '" + item + "' confirmed!");
    }
}

public class DIDemo {
    public static void main(String[] args) {
        // Wiring dependencies manually (in real apps: Spring Framework does this)
        PaymentGateway bkash = new BkashGateway();
        NotificationService sms = new SMSNotifier();

        OrderService orderService = new OrderService(bkash, sms);
        orderService.placeOrder("Laptop", 85000.0, "01712345678");
    }
}
```

### DI এর সুবিধা

| সুবিধা | ব্যাখ্যা |
|-------|---------|
| Loose Coupling | Class নিজের dependency তৈরি করে না |
| Testability | Mock objects inject করে unit test সহজ |
| Flexibility | Implementation swap করা যায় |
| SOLID DIP | Abstraction এ নির্ভর করা হয় |

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.৯ Coupling এবং Cohesion

### Coupling কী?

**Coupling** হলো দুটি class বা module এর মধ্যে **নির্ভরশীলতার মাত্রা**।

- **Tight Coupling (খারাপ):** একটি পরিবর্তন করলে অন্যটিও পরিবর্তন করতে হয়
- **Loose Coupling (ভালো):** Class গুলো স্বাধীন, একটি পরিবর্তনে অন্যটি প্রভাবিত হয় না

### Cohesion কী?

**Cohesion** হলো একটি class এর ভেতরে সব methods ও data কতটা **একই উদ্দেশ্যে** কাজ করে।

- **High Cohesion (ভালো):** Class এর সব কিছু একটি স্পষ্ট উদ্দেশ্যে কাজ করে
- **Low Cohesion (খারাপ):** Class অনেক ধরনের unrelated কাজ করে

### Code Example

```java
// ❌ Tight Coupling + Low Cohesion
class BadOrderProcessor {
    // Tight coupling — directly creates dependencies
    MySQLDatabase db = new MySQLDatabase();
    EmailService email = new EmailService();
    SMSService sms = new SMSService();
    PdfGenerator pdf = new PdfGenerator();
    InventoryManager inventory = new InventoryManager();

    // Low cohesion — does too many things
    public void processOrder(Order order) {
        // Order processing
        inventory.reduce(order.getItem(), order.getQuantity());
        db.saveOrder(order);
        // PDF generation
        pdf.generateInvoice(order);
        // Notifications
        email.sendConfirmation(order.getEmail(), order);
        sms.sendAlert(order.getPhone(), "Order placed!");
        // Analytics
        db.updateSalesReport(order);
    }
}

// ✅ Loose Coupling + High Cohesion
class OrderProcessor {
    private final OrderRepository orderRepo;
    private final NotificationService notifier;
    private final InventoryService inventory;

    // Constructor injection (loose coupling)
    public OrderProcessor(OrderRepository repo,
                          NotificationService notifier,
                          InventoryService inventory) {
        this.orderRepo = repo;
        this.notifier = notifier;
        this.inventory = inventory;
    }

    // High cohesion — only handles order processing
    public boolean processOrder(Order order) {
        if (!inventory.isAvailable(order.getItemId(), order.getQuantity())) {
            return false;
        }
        inventory.reserve(order.getItemId(), order.getQuantity());
        orderRepo.save(order);
        notifier.notifyOrderConfirmation(order);
        return true;
    }
}
```

### Goal: Low Coupling + High Cohesion

```
        Cohesion
           ↑
   HIGH    │  ✅ Best
           │
   LOW     │  ❌ Worst
           └─────────────→ Coupling
              LOW    HIGH
              ✅      ❌
```

| Combination | মূল্যায়ন |
|------------|---------|
| High Cohesion + Low Coupling | ✅ Best — Ideal design |
| High Cohesion + High Coupling | ⚠️ Acceptable |
| Low Cohesion + Low Coupling | ⚠️ Needs refactor |
| Low Cohesion + High Coupling | ❌ Worst — Spaghetti code |

---

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ২.১০ PART 2 — Interview Questions & Answers

### Core Questions

**Q1: Static এবং Dynamic binding এর পার্থক্য কী?**  
A: Static binding compile time এ হয় (overloading, non-virtual), Dynamic binding runtime এ হয় (virtual functions, overriding)।

**Q2: Interface এবং Abstract class এর মধ্যে কোনটি বেছে নেবেন কখন?**  
A: "is-a" relationship এবং shared code থাকলে Abstract class। "can-do" capability এবং multiple inheritance দরকার হলে Interface।

**Q3: Pure Virtual Function কী? কেন ব্যবহার করা হয়?**  
A: `= 0` দিয়ে declare করা virtual function যার parent এ implementation নেই। Subclass কে implement করতে বাধ্য করতে এবং class কে abstract করতে ব্যবহার হয়।

**Q4: Virtual Destructor কেন দরকার?**  
A: Parent pointer দিয়ে child object delete করলে virtual destructor না থাকলে শুধু parent destructor call হয় — child এর allocated memory leak হয়।

**Q5: Shallow copy এর সমস্যা কী?**  
A: Pointer copy হলে দুটি object একই memory point করে। একটি object destroy হলে সেই memory free হয়, অন্যটি dangling pointer হয় → double delete → undefined behavior।

**Q6: Rule of Three কী?**  
A: C++ এ Destructor, Copy Constructor, Copy Assignment Operator — এগুলোর একটি define করলে তিনটিই করতে হবে।

**Q7: Diamond Problem কীভাবে C++ সমাধান করে?**  
A: Virtual Inheritance দিয়ে — `class Dog : virtual public Animal` — grandparent class এর একটিই copy shared হয়।

**Q8: SOLID এর "S" কী?**  
A: Single Responsibility Principle — একটি class এর শুধু একটি কারণে change হওয়া উচিত।

**Q9: Dependency Injection এর সুবিধা কী?**  
A: Loose coupling, testability (mock injection), flexibility (implementation swap), SOLID DIP মেনে চলা।

**Q10: High Cohesion এবং Low Coupling কেন ভালো?**  
A: High Cohesion = class focused ও maintainable। Low Coupling = classes independent, change করলে অন্যটি ভাঙে না। এই দুটি একসাথে থাকলে software robust ও scalable হয়।

---

### Tricky Questions

**Q: Interface এ variable থাকতে পারে কি?**  
A: Java তে হ্যাঁ, কিন্তু সেগুলো automatically `public static final` — অর্থাৎ constants। Mutable instance variable রাখা যায় না।

**Q: একটি class কি নিজেকে inherit করতে পারে?**  
A: না। এটি circular dependency তৈরি করবে এবং compile error হবে।

**Q: Abstract class এর constructor থাকতে পারে কি?**  
A: হ্যাঁ। Abstract class instantiate করা না গেলেও, subclass এর constructor `super()` দিয়ে abstract class এর constructor call করে।

**Q: `final` method কি override হতে পারে?**  
A: না। Java তে `final` method override করা যায় না। C++ এ `override final` দিয়ে একই কাজ করা যায়।

---

> **⚠️ PART 2 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part3"></a>

# PART 3: Interview Questions — সম্পূর্ণ প্রশ্নোত্তর ভান্ডার

> **📍 এই PART এর Sections:** [৩.১ ৫০টি বিস্তারিত প্রশ্নোত্তর](#৩১-theoretical-interview-questions-৫০টি-বিস্তারিত-প্রশ্নোত্তর) · [৩.২ Common Mistakes](#৩২-common-interview-mistakes-এবং-কীভাবে-এড়াবেন) · [৩.৩ Follow-up Patterns](#৩৩-follow-up-question-patterns-common-sequences)

> **ব্যবহারের নিয়ম:** প্রথমে নিজে উত্তর দেওয়ার চেষ্টা করুন। তারপর model answer পড়ুন। প্রতিদিন ১০টি করে মুখস্থ নয়, বুঝে পড়ুন।

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.১ Theoretical Interview Questions (৫০টি বিস্তারিত প্রশ্নোত্তর)

---

### ✅ বিভাগ ১: OOP মূল ধারণা (প্রশ্ন ১–১০)

---

**প্রশ্ন ১: Object-Oriented Programming কী এবং Procedural Programming থেকে কীভাবে আলাদা?**

**উত্তর:**
Object-Oriented Programming (OOP) হলো একটি programming paradigm যেখানে software কে **objects** এর সমষ্টি হিসেবে design করা হয়। প্রতিটি object এর নিজস্ব **state (data/attributes)** এবং **behavior (methods)** থাকে।

| বিষয় | Procedural | OOP |
|------|-----------|-----|
| Focus | Functions | Objects |
| Data | Global বা parameter | Object এর ভেতরে |
| Approach | Top-down | Bottom-up |
| Reuse | Function call | Inheritance, Composition |
| Security | কম | বেশি (Encapsulation) |
| উদাহরণ | C, Pascal | Java, C++, Python |

OOP এ "real-world" entities কে model করা যায় — যেমন Student, BankAccount, Employee। এটি large-scale software development এর জন্য বেশি উপযুক্ত।

**Follow-up:** "OOP কি সবসময় ভালো approach?"  
**উত্তর:** না। ছোট script বা performance-critical system এ Procedural বা Functional approach ভালো হতে পারে। OOP complex systems এর জন্য সবচেয়ে উপযুক্ত।

---

**প্রশ্ন ২: OOP এর চারটি মূল pillar কী কী? প্রতিটি এক বাক্যে বলুন।**

**উত্তর:**

| Pillar | এক বাক্যে |
|--------|----------|
| **Encapsulation** | Data এবং methods একসাথে class এ রাখা এবং private রেখে বাইরে থেকে protect করা |
| **Abstraction** | User কে শুধু প্রয়োজনীয় তথ্য দেখানো, implementation details লুকিয়ে রাখা |
| **Inheritance** | একটি class অন্য class এর properties ও methods পাওয়া (code reuse) |
| **Polymorphism** | একই নামের method বিভিন্ন context এ বিভিন্নভাবে আচরণ করা |

**Memory Trick:** **"EAIP"** — Every Animal Is Polymorphic  
অথবা: **"A PIE"** — Abstraction, Polymorphism, Inheritance, Encapsulation

---

**প্রশ্ন ৩: Class এবং Object এর পার্থক্য কী? উদাহরণ দিন।**

**উত্তর:**
- **Class** হলো একটি **blueprint বা template** — যেমন বাড়ির নকশা। Class নিজে কোনো memory নেয় না।
- **Object** হলো সেই blueprint থেকে তৈরি **real entity** — যেমন আসল বাড়ি। Object create হলে memory allocate হয়।

```java
// Class = Blueprint
class Car {
    String brand;
    int speed;
    void accelerate() { speed += 10; }
}

// Objects = Real instances
Car car1 = new Car(); // Object 1 — নিজস্ব memory
Car car2 = new Car(); // Object 2 — আলাদা memory
car1.brand = "Toyota";
car2.brand = "Honda";
// car1 এবং car2 আলাদা state রাখে কিন্তু একই class share করে
```

**Common Mistake:** "একটি class থেকে শুধু একটি object তৈরি হয়" — **ভুল!** একটি class থেকে যতটি চাই ততটি object তৈরি করা যায়।

---

**প্রশ্ন ৪: Constructor কী? কতো প্রকার Constructor আছে?**

**উত্তর:**
Constructor হলো class এর একটি special method যা **object তৈরির সময় automatically call** হয় এবং object কে **initialize** করে।

**বৈশিষ্ট্য:**
- Class এর নামের মতো নাম
- কোনো return type নেই (void ও না)
- Overload করা যায়

**প্রকারভেদ:**

| Type | বিবরণ |
|------|-------|
| Default Constructor | কোনো parameter নেই। Object create হলে auto-call হয় |
| Parameterized Constructor | Parameter নিয়ে custom initialization করে |
| Copy Constructor | অন্য object এর data দিয়ে নতুন object তৈরি করে |
| Move Constructor (C++11) | Temporary object এর ownership নেয় |

**Follow-up:** "Java তে default constructor কখন compiler generate করে?"  
**উত্তর:** যখন programmer কোনো constructor define করেন না, তখন compiler automatically no-argument constructor generate করে। কিন্তু যদি programmer যেকোনো একটি constructor define করেন, compiler আর default constructor দেয় না।

---

**প্রশ্ন ৫: Encapsulation কী? কেন এটি গুরুত্বপূর্ণ?**

**উত্তর:**
Encapsulation হলো data (attributes) ও methods কে একসাথে class এ bundle করা এবং `private` access modifier দিয়ে data কে বাইরে থেকে **protect** করা। শুধু `public` getter/setter methods দিয়ে controlled access দেওয়া হয়।

**কেন গুরুত্বপূর্ণ:**
1. **Data Security** — বাইরে থেকে directly data change করা যায় না
2. **Validation** — Setter এ business rules enforce করা যায়
3. **Maintainability** — Implementation বদলালেও বাইরের code ভাঙে না
4. **Modularity** — প্রতিটি class নিজের data নিজে manage করে

```java
class Employee {
    private double salary;  // Hidden

    public void setSalary(double salary) {
        if (salary < 0) throw new IllegalArgumentException("Salary cannot be negative!");
        this.salary = salary;  // Validated before setting
    }

    public double getSalary() { return salary; }
}
```

**Real-life analogy:** ATM machine — আপনি PIN দিন, টাকা নিন। ভেতরের system দেখতে বা ছুঁতে পারবেন না।

---

**প্রশ্ন ৬: Abstraction এবং Encapsulation এর পার্থক্য বলুন।**

**উত্তর:**

| বিষয় | Encapsulation | Abstraction |
|------|-------------|------------|
| উদ্দেশ্য | Data protect করা | Complexity লুকানো |
| "What" vs "How" | "How" লুকায় (implementation) | "What" দেখায় (interface) |
| Level | Class level | Design level |
| Tool | `private` + getter/setter | Abstract class, Interface |
| Analogy | ক্যাপসুল ওষুধ | TV remote |

**সহজ মনে রাখার উপায়:**
- Encapsulation = **"আমি কীভাবে কাজ করি সেটা জানাব না"** (data hiding)
- Abstraction = **"তোমার যা জানা দরকার শুধু সেটা দেখাব"** (complexity hiding)

---

**প্রশ্ন ৭: Inheritance কী? "is-a" এবং "has-a" relationship বলতে কী বোঝায়?**

**উত্তর:**
Inheritance হলো একটি mechanism যেখানে একটি **child class** অন্য একটি **parent class** এর properties ও methods **উত্তরাধিকার সূত্রে পায়**। এটি code reuse নিশ্চিত করে।

**"is-a" relationship (Inheritance এর জন্য):**
- Dog **is-a** Animal → `class Dog extends Animal`
- Manager **is-a** Employee → `class Manager extends Employee`
- ElectricCar **is-a** Vehicle → `class ElectricCar extends Vehicle`

**"has-a" relationship (Composition এর জন্য):**
- Car **has-a** Engine → `class Car { Engine engine; }`
- University **has-a** Department → `class University { Department[] depts; }`

**গুরুত্বপূর্ণ নিয়ম:** Inheritance তখনই ব্যবহার করুন যখন সত্যিকারের "is-a" relationship আছে। শুধু code reuse এর জন্য ভুল hierarchy তৈরি করবেন না।

---

**প্রশ্ন ৮: Polymorphism কী? কত প্রকার? উদাহরণ দিন।**

**উত্তর:**
Polymorphism মানে "অনেক রূপ" — একই method বা interface বিভিন্ন ধরনের object এর জন্য বিভিন্নভাবে কাজ করে।

**দুই প্রকার:**

**১. Compile-time Polymorphism (Method Overloading):**
```java
class Printer {
    void print(int n) { System.out.println("Printing int: " + n); }
    void print(String s) { System.out.println("Printing string: " + s); }
    void print(double d) { System.out.println("Printing double: " + d); }
}
// কোন print() call হবে compile time এ নির্ধারিত
```

**২. Runtime Polymorphism (Method Overriding):**
```java
class Shape { virtual void draw() { /* base */ } }
class Circle extends Shape { void draw() { /* circle */ } }
class Square extends Shape { void draw() { /* square */ } }

Shape s = new Circle();
s.draw(); // Runtime এ Circle এর draw() call হবে
```

---

**প্রশ্ন ৯: Method Overloading এবং Method Overriding এর পার্থক্য কী?**

**উত্তর:**

| বিষয় | Overloading | Overriding |
|------|------------|-----------|
| কোথায় | Same class | Parent-Child class |
| Method নাম | Same | Same |
| Parameters | ভিন্ন | Same |
| Return type | ভিন্ন হতে পারে | Same (covariant possible) |
| Binding | Compile-time (Static) | Runtime (Dynamic) |
| `virtual` কি লাগে? | না | C++ এ হ্যাঁ |
| Inheritance | লাগে না | লাগে |

**Trick Question:** "শুধু return type পরিবর্তন করলে কি overloading হয়?"  
**উত্তর:** **না।** Java ও C++ উভয়তে শুধু return type change করে overloading হয় না — compiler error হবে। Parameter signature ভিন্ন হতে হবে।

---

**প্রশ্ন ১০: Access Modifiers কী কী? প্রতিটির scope বলুন।**

**উত্তর:**

| Modifier | Same Class | Same Package | Subclass | Outside |
|----------|-----------|-------------|---------|---------|
| `public` | ✅ | ✅ | ✅ | ✅ |
| `protected` | ✅ | ✅ | ✅ | ❌ |
| `default` (Java) | ✅ | ✅ | ❌ | ❌ |
| `private` | ✅ | ❌ | ❌ | ❌ |

**C++ Note:** Class এ members default = `private`, struct এ default = `public`।

**Tricky:** "Private member কি inherit হয়?"  
**উত্তর:** হ্যাঁ, inherit হয় কিন্তু directly access করা যায় না। Parent class এর public/protected methods দিয়ে access করতে হয়।

---

### ✅ বিভাগ ২: Inheritance ও Polymorphism (প্রশ্ন ১১–২০)

---

**প্রশ্ন ১১: Java তে Multiple Inheritance কেন নেই? কীভাবে এই সীমাবদ্ধতা overcome করা যায়?**

**উত্তর:**
Java তে **class দিয়ে multiple inheritance** নেই কারণ **Diamond Problem** হতে পারে।

```
        Animal
       /      \
     Dog      Cat
       \      /
       DogCat
```

যদি `Dog` ও `Cat` উভয়ই `Animal` এর `speak()` method override করে, তাহলে `DogCat` কোন `speak()` call করবে — এটি ambiguous।

**Overcome করার উপায়:**
```java
// Interface দিয়ে multiple inheritance
interface Swimmable { void swim(); }
interface Flyable { void fly(); }

class Duck implements Swimmable, Flyable {
    public void swim() { System.out.println("Duck swimming"); }
    public void fly() { System.out.println("Duck flying"); }
}
```

Java Interface এ (Java 8+) `default` method থাকলে একই diamond problem আসতে পারে, কিন্তু Java তে সেক্ষেত্রে **explicitly override করতে বাধ্য করা হয়**।

---

**প্রশ্ন ১২: `super` keyword কী? কখন ব্যবহার করা হয়?**

**উত্তর:**
`super` keyword দিয়ে **parent class এর members** access করা হয়।

**তিনটি ব্যবহার:**
```java
class Animal {
    String name;
    Animal(String name) { this.name = name; }
    void speak() { System.out.println("Animal sound"); }
}

class Dog extends Animal {
    String breed;

    Dog(String name, String breed) {
        super(name);      // 1. Parent constructor call
        this.breed = breed;
    }

    void speak() {
        super.speak();    // 2. Parent method call
        System.out.println(name + " says Woof!");
    }

    void show() {
        System.out.println(super.name + " | " + breed); // 3. Parent field access
    }
}
```

**Rules:**
- `super()` constructor call অবশ্যই **প্রথম statement** হতে হবে
- `this()` এবং `super()` একসাথে ব্যবহার করা যায় না

---

**প্রশ্ন ১৩: Inheritance এর প্রকারভেদ বলুন এবং Java তে কোন কোনটি সম্ভব?**

**উত্তর:**

| Type | বিবরণ | Java | C++ |
|------|-------|------|-----|
| Single | A → B | ✅ | ✅ |
| Multi-level | A → B → C | ✅ | ✅ |
| Hierarchical | A → B, A → C | ✅ | ✅ |
| Multiple | A, B → C (class) | ❌ | ✅ |
| Hybrid | উপরের combination | Interface এ ✅ | ✅ |

Java তে class দিয়ে Multiple Inheritance নেই কিন্তু Interface দিয়ে করা যায়।

---

**প্রশ্ন ১৪: Runtime Polymorphism কীভাবে কাজ করে? vtable কী?**

**উত্তর:**
Runtime Polymorphism কাজ করে **Virtual Table (vtable)** এর মাধ্যমে।

**vtable কী:**
প্রতিটি class এর জন্য compiler একটি **vtable (virtual dispatch table)** তৈরি করে — এটি function pointers এর একটি array যেখানে প্রতিটি virtual function এর address থাকে।

প্রতিটি object এ একটি hidden pointer থাকে — **vptr (virtual pointer)** — যা সেই class এর vtable কে point করে।

```
Animal* a = new Dog();
a->speak();
// 1. a এর vptr দেখ
// 2. vptr Dog এর vtable point করছে
// 3. vtable এ speak এর address খোঁজ
// 4. Dog::speak() call কর
```

**এই কারণে runtime polymorphism static binding এর চেয়ে সামান্য ধীর** — কারণ প্রতিটি virtual function call এ একটি extra indirection (vtable lookup) হয়।

---

**প্রশ্ন ১৫: `final` keyword Java তে কীভাবে OOP এ ব্যবহার হয়?**

**উত্তর:**

| ব্যবহার | অর্থ |
|---------|------|
| `final` variable | Value পরিবর্তন করা যাবে না (constant) |
| `final` method | Override করা যাবে না |
| `final` class | Extend (inherit) করা যাবে না |

```java
final class ImmutableConfig {  // Cannot be extended
    final int MAX_SIZE = 100;  // Constant

    final void load() {        // Cannot be overridden
        System.out.println("Loading config...");
    }
}

// class MyConfig extends ImmutableConfig { } // ❌ Compile Error!
```

**Real example:** `String` class Java তে `final` — কেউ String কে extend করে behavior পরিবর্তন করতে পারবে না।

---

**প্রশ্ন ১৬: Upcasting এবং Downcasting কী?**

**উত্তর:**

**Upcasting:** Child object কে Parent reference দিয়ে hold করা — **automatic, safe**।
```java
Animal a = new Dog("Bruno"); // Upcasting — automatic
a.makeSound();               // Dog এর makeSound() call হবে (polymorphism)
```

**Downcasting:** Parent reference কে Child type এ cast করা — **explicit, risky**।
```java
Animal a = new Dog("Bruno");
Dog d = (Dog) a;             // Downcasting — explicit
d.fetch();                   // Dog-specific method access

// Risky example:
Animal a2 = new Cat("Whiskers");
Dog d2 = (Dog) a2;           // ❌ ClassCastException at runtime!

// Safe downcasting with instanceof
if (a instanceof Dog) {
    Dog safeD = (Dog) a;
    safeD.fetch();
}
```

---

**প্রশ্ন ১৭: Composition কি Inheritance এর চেয়ে ভালো? কেন?**

**উত্তর:**
General rule: **"Favor Composition over Inheritance"** — Gang of Four (GoF) Design Patterns বই থেকে।

**Inheritance এর সমস্যা:**
- Tight coupling — parent পরিবর্তন হলে child ভাঙতে পারে
- Liskov Substitution Principle ভাঙতে পারে (Square-Rectangle problem)
- Multiple inheritance সমস্যা

**Composition এর সুবিধা:**
- Loose coupling
- Runtime এ behavior পরিবর্তন করা যায়
- More flexible

```java
// Inheritance (less flexible)
class Logger extends FileWriter { /* tightly coupled to FileWriter */ }

// Composition (flexible)
class Logger {
    private Writer writer;  // Can be FileWriter, NetworkWriter, etc.
    public Logger(Writer writer) { this.writer = writer; }
    public void log(String msg) { writer.write(msg); }
}
```

**কখন Inheritance:** সত্যিকারের "is-a" এবং LSP মেনে চলে।  
**কখন Composition:** "has-a" এবং flexible behavior দরকার।

---

**প্রশ্ন ১৮: Static method কি Override হয়? কেন?**

**উত্তর:**
**না।** Static methods **class level** এ belong করে, object level এ নয়। তাই static methods override হয় না।

Java তে child class এ same signature এর static method লিখলে সেটি **Method Hiding** — overriding নয়।

```java
class Parent {
    static void staticMethod() { System.out.println("Parent static"); }
    void instanceMethod() { System.out.println("Parent instance"); }
}

class Child extends Parent {
    static void staticMethod() { System.out.println("Child static"); }  // Hiding
    @Override
    void instanceMethod() { System.out.println("Child instance"); }     // Overriding
}

Parent p = new Child();
p.staticMethod();   // "Parent static" — Static binding, not polymorphic!
p.instanceMethod(); // "Child instance" — Dynamic binding ✅
```

---

**প্রশ্ন ১৯: Constructor কি inherit হয়?**

**উত্তর:**
**না।** Constructor inherit হয় না। কিন্তু child class এর constructor থেকে `super()` দিয়ে parent এর constructor call করা যায়।

```java
class Animal {
    String name;
    Animal(String name) {
        this.name = name;
        System.out.println("Animal constructor: " + name);
    }
}

class Dog extends Animal {
    String breed;
    Dog(String name, String breed) {
        super(name);   // Parent constructor explicitly called
        this.breed = breed;
        System.out.println("Dog constructor: " + breed);
    }
}

// new Dog("Bruno", "Lab") output:
// Animal constructor: Bruno
// Dog constructor: Lab
```

যদি `super()` explicitly না লেখা হয়, Java automatically **no-argument super()** call করে। যদি parent এ no-arg constructor না থাকে, compile error।

---

**প্রশ্ন ২০: Object class Java তে কী? সব class কি Object কে extend করে?**

**উত্তর:**
হ্যাঁ। Java তে `java.lang.Object` হলো **সব class এর ultimate parent**। যদি কোনো class explicitly কিছু extend না করে, সে automatically `Object` কে extend করে।

**Object class এর গুরুত্বপূর্ণ methods:**

| Method | কাজ |
|--------|-----|
| `toString()` | Object এর String representation |
| `equals(Object o)` | দুটি object equal কিনা |
| `hashCode()` | Object এর hash value |
| `getClass()` | Runtime class জানা |
| `clone()` | Object copy করা |
| `finalize()` | GC এর আগে call (deprecated) |

**Important:** `equals()` override করলে `hashCode()` ও override করতে হবে — না হলে HashMap/HashSet এ সমস্যা হবে।

---

### ✅ বিভাগ ৩: Abstract Class, Interface, Virtual (প্রশ্ন ২১–৩০)

---

**প্রশ্ন ২১: Abstract Class কী? কখন ব্যবহার করবেন?**

**উত্তর:**
Abstract class হলো এমন একটি class যা `abstract` keyword দিয়ে declare করা হয় এবং যাতে কমপক্ষে একটি `abstract` method থাকতে পারে। Abstract class **directly instantiate করা যায় না**।

**বৈশিষ্ট্য:**
- Concrete এবং Abstract methods উভয়ই থাকতে পারে
- Constructor থাকতে পারে
- Instance variables থাকতে পারে
- Access modifiers যেকোনো হতে পারে

```java
abstract class DatabaseConnection {
    private String host;
    private int port;

    // Constructor — subclass super() দিয়ে call করবে
    public DatabaseConnection(String host, int port) {
        this.host = host;
        this.port = port;
    }

    // Concrete — common to all DB connections
    public void logConnection() {
        System.out.println("Connecting to " + host + ":" + port);
    }

    // Abstract — each DB implements differently
    public abstract void connect();
    public abstract void disconnect();
    public abstract boolean executeQuery(String query);
}

class MySQLConnection extends DatabaseConnection {
    public MySQLConnection(String host, int port) {
        super(host, port);
    }

    @Override public void connect() { System.out.println("MySQL connected"); }
    @Override public void disconnect() { System.out.println("MySQL disconnected"); }
    @Override public boolean executeQuery(String q) {
        System.out.println("MySQL executing: " + q);
        return true;
    }
}
```

**কখন ব্যবহার:** Related classes এ shared code + কিছু behavior subclass কে নিজে implement করতে হবে।

---

**প্রশ্ন ২২: Interface কী? Java 8 এ Interface এ কী নতুন যোগ হয়েছে?**

**উত্তর:**
Interface হলো একটি pure contract যা define করে কী কী methods implement করতে হবে। Interface এর সব methods implicitly `public abstract`।

**Java 8 এর আগে:** শুধু abstract methods এবং `public static final` constants।

**Java 8+ এ নতুন:**

| Feature | বিবরণ |
|---------|-------|
| `default` method | Interface এ concrete implementation দেওয়া যায় |
| `static` method | Interface এর utility methods |
| `private` method (Java 9) | Interface এর internal helper |

```java
interface Validator {
    // Abstract (must implement)
    boolean validate(String input);

    // Default (optional to override)
    default String getErrorMessage() {
        return "Validation failed!";
    }

    // Static utility
    static boolean isNotEmpty(String s) {
        return s != null && !s.isEmpty();
    }
}

class EmailValidator implements Validator {
    @Override
    public boolean validate(String email) {
        return Validator.isNotEmpty(email) && email.contains("@");
    }

    @Override
    public String getErrorMessage() {
        return "Invalid email format!";
    }
}
```

---

**প্রশ্ন ২৩: Abstract Class vs Interface — কোনটি কখন choose করবেন?**

**উত্তর:**

```
Abstract Class choose করুন যখন:
  ✅ "is-a" relationship আছে
  ✅ Related classes এ shared implementation দরকার
  ✅ private বা protected members দরকার
  ✅ Constructor logic দরকার
  ✅ Instance state (non-final variables) দরকার
  উদাহরণ: Animal, Vehicle, Shape hierarchy

Interface choose করুন যখন:
  ✅ Unrelated classes এ common behavior দরকার
  ✅ Multiple inheritance দরকার
  ✅ API/Contract define করতে হবে
  ✅ "can-do" capability (Flyable, Printable, Serializable)
  উদাহরণ: Comparable, Runnable, Serializable
```

**Real interview answer:** "যদি base class এ কিছু shared implementation থাকে এবং 'is-a' relationship থাকে, Abstract class ব্যবহার করব। যদি শুধু contract define করতে হয় এবং multiple inheritance দরকার হয়, Interface ব্যবহার করব।"

---

**প্রশ্ন ২৪: Virtual Function এবং Pure Virtual Function এর পার্থক্য কী?**

**উত্তর:**

| বিষয় | Virtual Function | Pure Virtual Function |
|------|----------------|----------------------|
| Syntax | `virtual void f()` | `virtual void f() = 0` |
| Implementation | Parent এ আছে | নেই |
| Override | Optional | Mandatory |
| Class type | Concrete হতে পারে | Abstract class হয় |
| Instantiation | পারা যায় | পারা যায় না |

```cpp
class Animal {
public:
    virtual void breathe() {          // Virtual — has implementation
        cout << "Breathing..." << endl;
    }
    virtual void makeSound() = 0;     // Pure virtual — NO implementation
    virtual ~Animal() {}
};

class Dog : public Animal {
public:
    // makeSound() MUST be implemented — otherwise Dog is also abstract
    void makeSound() override {
        cout << "Woof!" << endl;
    }
    // breathe() — optional to override
};
```

---

**প্রশ্ন ২৫: Why should we use `virtual` destructor in C++?**

**উত্তর:**
Parent class pointer দিয়ে child object delete করার সময়, `virtual` destructor না থাকলে **শুধু parent এর destructor call হয়** — child এর destructor call হয় না। ফলে child এ allocated memory free হয় না → **memory leak**।

```cpp
class Base {
public:
    int* data;
    Base() { data = new int[10]; }

    // ❌ Without virtual:
    // ~Base() { delete[] data; }  // Child destructor never called!

    // ✅ With virtual:
    virtual ~Base() {
        delete[] data;
        cout << "Base destroyed" << endl;
    }
};

class Derived : public Base {
public:
    char* name;
    Derived() { name = new char[50]; }
    ~Derived() {
        delete[] name;  // ✅ Called only if Base destructor is virtual
        cout << "Derived destroyed" << endl;
    }
};

int main() {
    Base* b = new Derived();
    delete b;  // With virtual: both destructors called ✅
}
```

**Rule:** যদি class এ কোনো virtual function থাকে, **destructor কে virtual করুন**।

---

**প্রশ্ন ২৬: Shallow Copy এবং Deep Copy এর পার্থক্য কী? কখন Deep Copy দরকার?**

**উত্তর:**

**Shallow Copy:** Object এর values copy হয়। Pointer থাকলে pointer এর address copy হয় — pointed data নয়। ফলে দুটি object **একই memory share** করে।

**Deep Copy:** Pointer যে data point করছে সেটাও **নতুন memory তে copy** হয়। প্রতিটি object **independent memory** রাখে।

**Deep Copy কখন দরকার:**
- Class এ raw pointer (`int*`, `char*`) থাকলে
- Dynamic memory allocation থাকলে
- Object independent state রাখা দরকার হলে

```cpp
// Shallow Problem:
class Shallow {
public:
    int* value;
    Shallow(int v) { value = new int(v); }
    // Default copy: copies pointer address — BOTH point to same int!
};
Shallow a(10), b = a;  // b.value == a.value (same address)
*b.value = 99;         // a.value also becomes 99! ❌

// Deep Solution:
class Deep {
public:
    int* value;
    Deep(int v) { value = new int(v); }
    Deep(const Deep& other) {          // Deep copy constructor
        value = new int(*other.value); // NEW allocation
    }
};
Deep x(10), y = x;  // y.value != x.value (different addresses)
*y.value = 99;      // x.value still 10 ✅
```

---

**প্রশ্ন ২৭: Diamond Problem কী? C++ কীভাবে সমাধান করে?**

**উত্তর:**
Diamond Problem হলো Multiple Inheritance এ এমন একটি সমস্যা যেখানে একটি class দুটি parent থেকে inherit করে এবং উভয় parent একই grandparent থেকে inherit করে — ফলে grandparent এর members **দুইবার** আসে।

```
      A (grandparent)
     / \
    B   C (parents)
     \ /
      D (child) — has TWO copies of A!
```

**C++ সমাধান: Virtual Inheritance**
```cpp
class A { public: int x; };
class B : virtual public A { };  // virtual keyword
class C : virtual public A { };  // virtual keyword
class D : public B, public C { }; // Only ONE copy of A

D obj;
obj.x = 10;  // ✅ No ambiguity
```

**Java সমাধান:** Class এ multiple inheritance নেই তাই problem নেই। Interface এ `default` method conflict হলে explicitly override করতে হয়।

---

**প্রশ্ন ২৮: SOLID Principles কী? প্রতিটি এক বাক্যে বলুন।**

**উত্তর:**

| Principle | বাংলায় মূল কথা |
|-----------|--------------|
| **S** — SRP | একটি class এর শুধু একটি reason to change থাকা উচিত |
| **O** — OCP | Extend করুন, existing code modify করবেন না |
| **L** — LSP | Child object সবসময় parent এর জায়গায় ব্যবহারযোগ্য হওয়া উচিত |
| **I** — ISP | Client কে অপ্রয়োজনীয় interface implement করতে বাধ্য করবেন না |
| **D** — DIP | Abstraction এর উপর নির্ভর করুন, concrete class এর উপর নয় |

**Interview tip:** প্রতিটির জন্য একটি করে real-life code example মুখস্থ করুন।

---

**প্রশ্ন ২৯: Coupling কী? Tight এবং Loose Coupling এর পার্থক্য?**

**উত্তর:**
Coupling হলো দুটি class বা module এর মধ্যে **নির্ভরশীলতার মাত্রা**।

**Tight Coupling (খারাপ):**
- একটি class সরাসরি অন্য class এর concrete implementation জানে
- একটি পরিবর্তনে অন্যটি ভাঙতে পারে
- Unit testing কঠিন

```java
// Tight Coupling ❌
class OrderService {
    MySQLDatabase db = new MySQLDatabase(); // Directly depends on MySQL
}
```

**Loose Coupling (ভালো):**
- Class গুলো interface বা abstract class এর মাধ্যমে interact করে
- Independent পরিবর্তন সম্ভব
- Testing সহজ

```java
// Loose Coupling ✅
class OrderService {
    Database db; // Depends on abstraction
    OrderService(Database db) { this.db = db; } // DI
}
```

---

**প্রশ্ন ৩০: Dependency Injection কী? কোন কোন ধরনের DI আছে?**

**উত্তর:**
Dependency Injection হলো একটি design pattern যেখানে কোনো class তার dependencies নিজে create করে না — **বাইরে থেকে provide করা হয়**। এটি Loose Coupling ও Testability নিশ্চিত করে।

**তিন ধরনের DI:**

```java
// 1. Constructor Injection (সবচেয়ে preferred ✅)
class Service {
    private final Repository repo;
    Service(Repository repo) { this.repo = repo; }
}

// 2. Setter Injection
class Service {
    private Repository repo;
    void setRepo(Repository repo) { this.repo = repo; }
}

// 3. Field Injection (Spring এ @Autowired — not recommended for testing)
class Service {
    @Autowired
    private Repository repo;
}
```

**Constructor Injection কেন সবচেয়ে ভালো:**
- Object সবসময় valid state এ থাকে
- `final` fields use করা যায়
- Testing এ easily mock inject করা যায়

---

### ✅ বিভাগ ৪: Advanced Questions (প্রশ্ন ৩১–৪০)

---

**প্রশ্ন ৩১: Liskov Substitution Principle (LSP) কী? কোন উদাহরণ দিয়ে LSP violation দেখান।**

**উত্তর:**
LSP বলে: "যেখানে parent class object ব্যবহার করা হয়, সেখানে child class object ব্যবহার করলে program এর behavior পরিবর্তন হওয়া উচিত নয়।"

**Classic LSP Violation — Square-Rectangle Problem:**
```java
class Rectangle {
    protected int width, height;
    void setWidth(int w) { width = w; }
    void setHeight(int h) { height = h; }
    int getArea() { return width * height; }
}

class Square extends Rectangle {
    @Override
    void setWidth(int w) { width = height = w; }  // Forces square constraint
    @Override
    void setHeight(int h) { width = height = h; }
}

// LSP Test:
Rectangle r = new Square();
r.setWidth(4);
r.setHeight(5);
// Expected: 4 * 5 = 20
// Actual: 5 * 5 = 25 ❌ — LSP violated!
```

**Fix:** Square এবং Rectangle কে common interface দিয়ে model করুন, inheritance নয়।

---

**প্রশ্ন ৩২: `this` keyword কী? কতটি ব্যবহার আছে?**

**উত্তর:**
`this` keyword current object এর reference।

```java
class Employee {
    String name;
    int age;

    Employee(String name, int age) {
        this.name = name;   // 1. Instance variable vs parameter disambiguation
        this.age = age;
    }

    Employee(String name) {
        this(name, 25);     // 2. Another constructor call (this())
    }

    Employee getEmployee() {
        return this;        // 3. Return current object
    }

    void chain() {
        System.out.println(this.name); // 4. Call instance method/field
    }

    void passAsArgument(Logger logger) {
        logger.log(this);  // 5. Pass current object as argument
    }
}
```

---

**প্রশ্ন ৩৩: Java এ `instanceof` operator কী? কখন ব্যবহার করা উচিত?**

**উত্তর:**
`instanceof` operator runtime এ check করে একটি object কোনো specific class এর instance কিনা।

```java
Animal a = new Dog("Bruno");

System.out.println(a instanceof Animal); // true
System.out.println(a instanceof Dog);    // true
System.out.println(a instanceof Cat);    // false

// Safe downcasting
if (a instanceof Dog) {
    Dog d = (Dog) a;
    d.fetch();  // ✅ Safe — no ClassCastException
}

// Java 16+ Pattern Matching (cleaner)
if (a instanceof Dog d) {
    d.fetch();  // d already cast ✅
}
```

**কখন avoid করবেন:** Frequent `instanceof` check মানে design ভালো নয় — Polymorphism দিয়ে সমাধান করুন।

---

**প্রশ্ন ৩৪: Object Cloning কী? `Cloneable` interface কীভাবে কাজ করে?**

**উত্তর:**
Object Cloning মানে একটি object এর exact copy তৈরি করা।

```java
class Student implements Cloneable {
    String name;
    int age;
    int[] marks;

    Student(String name, int age, int[] marks) {
        this.name = name;
        this.age = age;
        this.marks = marks;
    }

    // Shallow clone (default)
    @Override
    public Student clone() throws CloneNotSupportedException {
        return (Student) super.clone();
        // marks array এর address copy হবে — shallow!
    }

    // Deep clone
    public Student deepClone() throws CloneNotSupportedException {
        Student cloned = (Student) super.clone();
        cloned.marks = marks.clone();  // Array ও copy করা হলো
        return cloned;
    }
}
```

**Note:** `Cloneable` হলো একটি marker interface (কোনো method নেই)। `clone()` আসে `Object` class থেকে। Modern Java তে Copy Constructor বা factory methods prefer করা হয়।

---

**প্রশ্ন ৩৫: Association, Aggregation, এবং Composition এর পার্থক্য কী?**

**উত্তর:**
তিনটিই class এর মধ্যে relationship, কিন্তু **dependency এর মাত্রা** আলাদা।

| বিষয় | Association | Aggregation | Composition |
|------|------------|------------|------------|
| সম্পর্ক | General | "has-a" (weak) | "has-a" (strong) |
| Lifetime | Independent | Independent | Dependent |
| Owner | নেই | Weak ownership | Strong ownership |
| উদাহরণ | Teacher-Student | Department-Teacher | House-Room |

```java
// Association — Teacher "uses" Student (no ownership)
class Teacher {
    void teach(Student s) { /* */ }
}

// Aggregation — Department "has" Teachers (Teachers exist independently)
class Department {
    List<Teacher> teachers; // Teachers can exist without Department
    Department(List<Teacher> teachers) { this.teachers = teachers; }
}

// Composition — House "owns" Rooms (Rooms cannot exist without House)
class House {
    private List<Room> rooms = new ArrayList<>(); // Created inside House
    House(int roomCount) {
        for (int i = 0; i < roomCount; i++) {
            rooms.add(new Room(i + 1)); // Room created by House
        }
    }
    // When House is destroyed, Rooms are also destroyed
}
```

---

**প্রশ্ন ৩৬: Cohesion কী? High Cohesion কেন ভালো?**

**উত্তর:**
Cohesion হলো একটি class বা module এর ভেতরে সব elements কতটা **একটি নির্দিষ্ট উদ্দেশ্যে** কাজ করে তার পরিমাপ।

**High Cohesion (ভালো):**
- Class এর সব methods একটি স্পষ্ট responsibility পালন করে
- Class বোঝা সহজ, maintain করা সহজ
- Reuse করা সহজ

**Low Cohesion (খারাপ):**
- Class অনেক ধরনের unrelated কাজ করে ("God Class")
- বোঝা কঠিন, পরিবর্তন risky

```java
// Low Cohesion ❌ — এক class সব করে
class Everything {
    void saveToDatabase() { }
    void generatePDFReport() { }
    void sendEmail() { }
    void calculateTax() { }
    void updateUI() { }
}

// High Cohesion ✅ — প্রতিটি class একটি কাজে focused
class TaxCalculator { double calculateTax(double income) { /* */ } }
class ReportGenerator { String generateReport(Data d) { /* */ } }
class EmailSender { void sendEmail(String to, String body) { /* */ } }
```

---

**প্রশ্ন ৩৭: Java তে `equals()` এবং `==` এর পার্থক্য কী?**

**উত্তর:**

| বিষয় | `==` | `equals()` |
|------|------|-----------|
| কী compare করে | Reference (address) | Content (value) |
| Default behavior | Address comparison | Address comparison (Object এ) |
| Override করা যায় | না | হ্যাঁ |
| Primitive তে | Value compare করে | N/A |

```java
String s1 = new String("Hello");
String s2 = new String("Hello");

System.out.println(s1 == s2);       // false — different objects!
System.out.println(s1.equals(s2));  // true — same content ✅

// String literal pool
String s3 = "Hello";
String s4 = "Hello";
System.out.println(s3 == s4);       // true — same pool reference
```

**Rule:** Object comparison এ সবসময় `equals()` ব্যবহার করুন। `==` শুধু primitive বা intentional reference check এ।

---

**প্রশ্ন ৩৮: Method Hiding কী? Overriding থেকে কীভাবে আলাদা?**

**উত্তর:**

**Method Hiding:** Static method এর ক্ষেত্রে — child class এ same signature এর static method লিখলে parent এর static method **hide** হয়। এটি polymorphic নয়।

**Method Overriding:** Instance (virtual) method এ — runtime এ actual object এর type দেখে সঠিক method call হয়।

```java
class Parent {
    static void staticM() { System.out.println("Parent static"); }
    void instanceM() { System.out.println("Parent instance"); }
}

class Child extends Parent {
    static void staticM() { System.out.println("Child static"); }  // Hiding
    @Override
    void instanceM() { System.out.println("Child instance"); }     // Overriding
}

Parent p = new Child();
p.staticM();   // "Parent static" ← Reference type decides (compile-time)
p.instanceM(); // "Child instance" ← Object type decides (runtime)
```

---

**প্রশ্ন ৩৯: Marker Interface কী? উদাহরণ দিন।**

**উত্তর:**
Marker Interface হলো এমন interface যাতে **কোনো method বা field নেই** — শুধু type marker হিসেবে কাজ করে। JVM বা framework এই marker দেখে special behavior প্রদান করে।

**Java এর বিখ্যাত Marker Interfaces:**
- `Serializable` — Object serialize করা যাবে
- `Cloneable` — `clone()` method call করা যাবে
- `RandomAccess` — Collection এ random access efficient

```java
import java.io.*;

class Employee implements Serializable {  // Marker — no methods to implement
    private static final long serialVersionUID = 1L;
    String name;
    double salary;

    Employee(String name, double salary) {
        this.name = name;
        this.salary = salary;
    }
}

// Now Employee objects can be serialized:
ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("emp.dat"));
oos.writeObject(new Employee("Rafi", 80000));
```

---

**প্রশ্ন ৪০: Functional Interface কী? Lambda এবং OOP এর সম্পর্ক?**

**উত্তর:**
**Functional Interface** হলো Java 8+ এ এমন interface যাতে **ঠিক একটি abstract method** থাকে। `@FunctionalInterface` annotation দিয়ে enforce করা হয়।

```java
@FunctionalInterface
interface Greeting {
    void greet(String name);  // Single abstract method
}

// Lambda expression = anonymous class এর shorthand
Greeting formal = name -> System.out.println("Good morning, " + name + "!");
Greeting casual = name -> System.out.println("Hey " + name + "!");

formal.greet("Mr. Rafi");  // Good morning, Mr. Rafi!
casual.greet("Rafi");      // Hey Rafi!

// Common Java functional interfaces:
// Runnable — void run()
// Comparator<T> — int compare(T a, T b)
// Predicate<T> — boolean test(T t)
// Function<T,R> — R apply(T t)
```

Lambda expressions OOP এর সাথে conflict করে না — এগুলো Functional Interface এর **anonymous implementation** মাত্র।

---

### ✅ বিভাগ ৫: ব্যাংক ও কোম্পানি-ভিত্তিক প্রশ্ন (প্রশ্ন ৪১–৫০)

---

**প্রশ্ন ৪১: একটি real-world system design এ OOP কীভাবে apply করবেন? উদাহরণ দিন।**

**উত্তর:**
উদাহরণ: **Online Food Ordering System (যেমন Foodpanda, Shohoz Food)**

```
Classes/Abstractions:
├── User (Abstract)
│   ├── Customer extends User
│   └── DeliveryPerson extends User
├── Restaurant
├── MenuItem
├── Order
│   ├── OrderItem (Composition — Order owns OrderItems)
│   └── OrderStatus (enum)
├── PaymentMethod (Interface)
│   ├── BkashPayment implements PaymentMethod
│   ├── NagadPayment implements PaymentMethod
│   └── CreditCardPayment implements PaymentMethod
└── NotificationService (Interface)
    ├── SMSNotification implements NotificationService
    └── PushNotification implements NotificationService
```

**OOP Principles applied:**
- Encapsulation: `Order.totalAmount` private, `getTotal()` public
- Abstraction: `PaymentMethod` interface
- Inheritance: `Customer`, `DeliveryPerson` extends `User`
- Polymorphism: `payment.process()` — different behavior by type

---

**প্রশ্ন ৪২: `HashMap` কীভাবে `equals()` এবং `hashCode()` ব্যবহার করে? OOP connection কী?**

**উত্তর:**
`HashMap` এ key store করতে `hashCode()` এবং `equals()` উভয়ই ব্যবহার হয়:

1. **`hashCode()`** → কোন bucket এ রাখবে নির্ধারণ করে
2. **`equals()`** → একই bucket এ collision হলে exact match খোঁজে

**Rule (OOP Contract):** `equals()` true return করলে `hashCode()` অবশ্যই same হতে হবে। উল্টোটা guarantee নয়।

```java
class Student {
    String id;
    String name;

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (!(o instanceof Student)) return false;
        Student s = (Student) o;
        return id.equals(s.id);
    }

    @Override
    public int hashCode() {
        return id.hashCode();  // Must be consistent with equals
    }
}

HashMap<Student, Double> grades = new HashMap<>();
Student s1 = new Student();
s1.id = "CSE001"; s1.name = "Rafi";
grades.put(s1, 3.75);

Student s2 = new Student();
s2.id = "CSE001"; s2.name = "Rafi Ahmed";  // Same id
System.out.println(grades.get(s2));  // 3.75 ✅ — equals() matches
```

---

**প্রশ্ন ৪৩: Object Immutability কী? Immutable class কীভাবে তৈরি করবেন?**

**উত্তর:**
Immutable object হলো এমন object যার **state তৈরির পরে পরিবর্তন করা যায় না**।

**Immutable Class তৈরির নিয়ম:**
1. Class `final` করুন
2. সব fields `private final`
3. কোনো setter নেই
4. Mutable fields এর deep copy return করুন

```java
public final class ImmutableStudent {
    private final String name;
    private final int age;
    private final int[] scores;  // Mutable array

    public ImmutableStudent(String name, int age, int[] scores) {
        this.name = name;
        this.age = age;
        this.scores = scores.clone();  // Defensive copy
    }

    public String getName() { return name; }
    public int getAge() { return age; }
    public int[] getScores() { return scores.clone(); }  // Return copy, not original
}
```

**সুবিধা:** Thread-safe, HashMap key হিসেবে safe।  
**উদাহরণ:** Java এর `String`, `Integer`, `LocalDate`।

---

**প্রশ্ন ৪৪: Design Pattern কী? Singleton Pattern কীভাবে implement করবেন?**

**উত্তর:**
Design Pattern হলো software design এর পুনরাবৃত্তযোগ্য সমস্যার proven সমাধান।

**Singleton Pattern:** নিশ্চিত করে যে একটি class এর **শুধু একটিই instance** তৈরি হবে এবং সেটিতে global access থাকবে।

```java
public class DatabaseManager {
    // volatile — ensures visibility across threads
    private static volatile DatabaseManager instance;
    private String connectionUrl;

    // Private constructor — কেউ new করতে পারবে না
    private DatabaseManager() {
        connectionUrl = "jdbc:mysql://localhost:3306/mydb";
        System.out.println("Database connection initialized");
    }

    // Double-checked locking — thread-safe
    public static DatabaseManager getInstance() {
        if (instance == null) {
            synchronized (DatabaseManager.class) {
                if (instance == null) {
                    instance = new DatabaseManager();
                }
            }
        }
        return instance;
    }

    public String getConnection() { return connectionUrl; }
}

// Usage:
DatabaseManager db1 = DatabaseManager.getInstance();
DatabaseManager db2 = DatabaseManager.getInstance();
System.out.println(db1 == db2);  // true — same object!
```

---

**প্রশ্ন ৪৫: Factory Pattern কী? কখন ব্যবহার করবেন?**

**উত্তর:**
Factory Pattern হলো object creation এর একটি design pattern যেখানে client code কে directly `new` করতে হয় না — একটি factory method বা class object তৈরির দায়িত্ব নেয়।

```java
// Product interface
interface Notification {
    void send(String message, String recipient);
}

// Concrete products
class EmailNotification implements Notification {
    public void send(String message, String recipient) {
        System.out.println("Email to " + recipient + ": " + message);
    }
}

class SMSNotification implements Notification {
    public void send(String message, String recipient) {
        System.out.println("SMS to " + recipient + ": " + message);
    }
}

class PushNotification implements Notification {
    public void send(String message, String recipient) {
        System.out.println("Push to " + recipient + ": " + message);
    }
}

// Factory — client doesn't know which class is instantiated
class NotificationFactory {
    public static Notification create(String type) {
        return switch (type.toLowerCase()) {
            case "email" -> new EmailNotification();
            case "sms"   -> new SMSNotification();
            case "push"  -> new PushNotification();
            default      -> throw new IllegalArgumentException("Unknown type: " + type);
        };
    }
}

// Client code
Notification n = NotificationFactory.create("sms");
n.send("Order confirmed!", "01712345678");
```

**কখন ব্যবহার:**
- Object creation complex হলে
- Client কে concrete class জানানো দরকার নেই
- Runtime এ type নির্ধারিত হলে

---

**প্রশ্ন ৪৬: Observer Pattern কী? Real-world উদাহরণ দিন।**

**উত্তর:**
Observer Pattern এ একটি **Subject (Observable)** থাকে যা state change হলে তার registered **Observers** কে notify করে।

**Real-world উদাহরণ:** YouTube subscription — নতুন video upload হলে subscribers notification পায়।

```java
import java.util.*;

interface Observer {
    void update(String event, Object data);
}

interface Subject {
    void addObserver(Observer o);
    void removeObserver(Observer o);
    void notifyObservers(String event, Object data);
}

class OrderSystem implements Subject {
    private List<Observer> observers = new ArrayList<>();
    private String orderStatus;

    public void addObserver(Observer o) { observers.add(o); }
    public void removeObserver(Observer o) { observers.remove(o); }

    public void notifyObservers(String event, Object data) {
        for (Observer o : observers) {
            o.update(event, data);
        }
    }

    public void updateOrderStatus(String status) {
        this.orderStatus = status;
        System.out.println("Order status updated: " + status);
        notifyObservers("ORDER_STATUS_CHANGED", status);
    }
}

class EmailObserver implements Observer {
    private String email;
    EmailObserver(String email) { this.email = email; }

    public void update(String event, Object data) {
        System.out.println("Email to " + email + ": Order " + data);
    }
}

class SMSObserver implements Observer {
    private String phone;
    SMSObserver(String phone) { this.phone = phone; }

    public void update(String event, Object data) {
        System.out.println("SMS to " + phone + ": Order " + data);
    }
}

public class ObserverDemo {
    public static void main(String[] args) {
        OrderSystem order = new OrderSystem();
        order.addObserver(new EmailObserver("rafi@gmail.com"));
        order.addObserver(new SMSObserver("01712345678"));

        order.updateOrderStatus("Shipped");
        order.updateOrderStatus("Delivered");
    }
}
```

---

**প্রশ্ন ৪৭: MVC Pattern কী? OOP এর সাথে কীভাবে সম্পর্কিত?**

**উত্তর:**
MVC = **Model-View-Controller** — একটি architectural pattern যা application কে তিনটি layer এ divide করে।

| Component | কাজ | OOP Concept |
|-----------|-----|------------|
| **Model** | Data ও business logic | Classes, Encapsulation |
| **View** | User Interface | Abstraction (user দেখে শুধু UI) |
| **Controller** | Model ও View সংযোগ | Dependency Injection |

```java
// Model
class StudentModel {
    private String name;
    private float cgpa;

    public StudentModel(String name, float cgpa) {
        this.name = name;
        this.cgpa = cgpa;
    }

    public String getName() { return name; }
    public float getCgpa() { return cgpa; }
    public void setCgpa(float cgpa) { this.cgpa = cgpa; }
}

// View
class StudentView {
    public void displayStudent(String name, float cgpa) {
        System.out.println("=== Student Profile ===");
        System.out.println("Name: " + name);
        System.out.println("CGPA: " + cgpa);
    }
}

// Controller
class StudentController {
    private StudentModel model;
    private StudentView view;

    public StudentController(StudentModel model, StudentView view) {
        this.model = model;
        this.view = view;
    }

    public void updateCgpa(float newCgpa) {
        model.setCgpa(newCgpa);
    }

    public void display() {
        view.displayStudent(model.getName(), model.getCgpa());
    }
}
```

---

**প্রশ্ন ৪৮: Stack এবং Heap এ object কীভাবে store হয়?**

**উত্তর:**

| বিষয় | Stack | Heap |
|------|-------|------|
| কী store হয় | Primitive, References, Method frames | Objects |
| Memory size | ছোট, fixed | বড়, dynamic |
| Access speed | দ্রুত | ধীর |
| Lifetime | Method শেষ হলে | GC collect না করা পর্যন্ত |
| Thread | প্রতিটি thread এর আলাদা stack | Shared between threads |

```java
void method() {
    int x = 10;           // x → Stack
    String s = "Hello";   // s (reference) → Stack, "Hello" object → Heap

    Student rafi = new Student("Rafi", 22);
    // rafi (reference) → Stack
    // Student object → Heap
}
// method শেষ: x, s, rafi Stack থেকে pop হয়
// Student object → Heap এ থাকে যতক্ষণ GC না নেয়
```

---

**প্রশ্ন ৪৯: Garbage Collection কী? Java তে কীভাবে কাজ করে?**

**উত্তর:**
Garbage Collection (GC) হলো Java এর automatic memory management system যা **unreachable objects** এর memory automatically free করে।

**কীভাবে কাজ করে:**
1. Object এর কোনো reference না থাকলে "unreachable" হয়
2. GC (Mark and Sweep algorithm) unreachable objects identify করে
3. সেই memory reclaim করে

```java
void example() {
    Student s = new Student("Rafi");  // Object created in Heap
    s = null;  // Reference removed — Object now eligible for GC
    s = new Student("Sumaiya");      // New object; previous one GC-eligible

    // System.gc(); — GC request (not guaranteed!)
}
```

**GC Algorithms:** Mark and Sweep, Generational GC (Young/Old Generation), G1GC।

**Important:** GC কখন run করবে programmer নিয়ন্ত্রণ করতে পারে না। `System.gc()` শুধু request, guarantee নয়।

---

**প্রশ্ন ৫০: আপনার project এ OOP কীভাবে apply করেছেন? (Project-based question)**

**উত্তর কাঠামো (Template):**

> "আমার [project নাম] project এ আমি OOP এর সব চারটি pillar apply করেছি।  
> 
> **Encapsulation:** সব entity class যেমন `User`, `Product`, `Order` এর fields private রেখে getter/setter দিয়ে access দিয়েছি।  
>
> **Abstraction:** Payment handling এর জন্য `PaymentService` interface তৈরি করেছি — bKash ও Nagad implementation আলাদা class এ।  
>
> **Inheritance:** `User` abstract class থেকে `Customer` এবং `Admin` class inherit করেছি — common fields (name, email) parent এ, specific behavior child এ।  
>
> **Polymorphism:** `PaymentService.process()` method call করলে runtime এ সঠিক implementation (bKash/Nagad) execute হয়।  
>
> **SOLID:** Single Responsibility মেনে `OrderService` শুধু order logic, `EmailService` শুধু email পাঠায়। Dependency Injection দিয়ে services loosely coupled রেখেছি।"

**Tip:** এই template নিজের project এর সাথে match করিয়ে বলুন।

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.২ Common Interview Mistakes এবং কীভাবে এড়াবেন

| ভুল | কেন হয় | সঠিক পদ্ধতি |
|-----|---------|------------|
| Constructor এ return type দেওয়া | Confusion with regular method | Constructor এর কোনো return type নেই — void ও না |
| OOP = শুধু Java | সীমিত জ্ঞান | C++, Python, C# সবই OOP |
| Overloading = Overriding | নাম গুলিয়ে ফেলা | Overloading: same class + diff params; Overriding: parent-child + same params |
| Abstract class instantiate করার চেষ্টা | Abstract concept না বোঝা | Abstract class এ `new` করা যায় না |
| `==` দিয়ে String compare | Java এর reference semantics না বোঝা | `equals()` ব্যবহার করুন |
| Private member inherit হয় না মনে করা | Access ও inheritance গুলিয়ে ফেলা | Inherit হয়, access করা যায় না |
| Interface এ state রাখার চেষ্টা | Abstract concept না বোঝা | Interface এ শুধু `public static final` constants |
| Virtual destructor না দেওয়া | C++ এর nuance না জানা | Polymorphic class এ virtual destructor আবশ্যক |
| equals() override করে hashCode() না করা | Contract না জানা | দুটি সবসময় একসাথে override করুন |
| Dependency সরাসরি `new` করা | DI concept না জানা | Interface inject করুন — loose coupling |

---

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৩.৩ Follow-up Question Patterns (Common Sequences)

```
Q: "OOP কী?" → follow-up → "৪টি pillar কী?" → "প্রতিটি উদাহরণ দিন"

Q: "Inheritance কী?" → follow-up → "Multiple inheritance Java তে নেই কেন?"
                                  → "Diamond problem কী?"
                                  → "Interface দিয়ে কীভাবে solve করবেন?"

Q: "Polymorphism কী?" → follow-up → "Runtime কীভাবে সঠিক method জানে?"
                                   → "vtable কী?"
                                   → "Virtual function কী?"

Q: "Encapsulation কী?" → follow-up → "Abstraction থেকে পার্থক্য?"
                                    → "Private member কি inherit হয়?"
                                    → "Getter/Setter ছাড়া encapsulation সম্ভব?"

Q: "SOLID বলুন" → follow-up → "LSP violation এর উদাহরণ?"
                              → "DIP কীভাবে implement করবেন?"
                              → "Dependency Injection কী?"
```

---

> **⚠️ PART 3 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part4"></a>

# PART 4: Coding Interview Problems — সম্পূর্ণ সমাধান

> **📍 এই PART এর Sections:** [৪.১ Student System](#৪১-student-management-system) · [৪.২ Bank System](#৪২-bank-management-system) · [৪.৩ Employee System](#৪৩-employee-management-system) · [৪.৪ Library System](#৪৪-library-management-system) · [৪.৫ Coding কৌশল](#৪৫-coding-problem--interview-কৌশল-সব-system-এর-জন্য)

> **ব্যবহারের নিয়ম:** প্রতিটি problem এ code নিজে লেখার চেষ্টা করুন। তারপর নিচের solution দেখুন। Dry run মাথায় করুন। Interview explanation strategy মুখস্থ করুন।

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.১ Student Management System

### Problem Statement

একটি **Student Management System** design করুন যেখানে:
- Student যোগ করা যাবে (নাম, রোল, বিভাগ, CGPA)
- Student এর তথ্য update করা যাবে
- Student খোঁজা যাবে (roll number দিয়ে)
- সব student এর তালিকা দেখা যাবে
- Student delete করা যাবে
- CGPA অনুযায়ী rank দেখা যাবে

**OOP Concepts Covered:**
- Encapsulation (private fields + getters/setters)
- Abstraction (interface)
- Inheritance (Graduate, Undergraduate)
- Polymorphism (displayInfo override)
- Composition (StudentManager has Students)

---

### Step-by-Step Explanation

```
Step 1: Student entity class তৈরি করি (Encapsulation)
Step 2: Undergraduate ও Graduate subclass তৈরি করি (Inheritance)
Step 3: StudentRepository interface তৈরি করি (Abstraction)
Step 4: StudentManager class দিয়ে CRUD implement করি (Composition)
Step 5: Main class এ demo চালাই
```

---

### Clean Code — Java

```java
import java.util.*;
import java.util.stream.*;

// ============================
// STEP 1: Base Student Class
// ============================
abstract class Student {
    private String name;
    private String rollNumber;
    private String department;
    private double cgpa;
    private int enrollmentYear;

    public Student(String name, String roll, String dept, double cgpa, int year) {
        setName(name);
        setRollNumber(roll);
        setDepartment(dept);
        setCgpa(cgpa);
        this.enrollmentYear = year;
    }

    // Getters
    public String getName()        { return name; }
    public String getRollNumber()  { return rollNumber; }
    public String getDepartment()  { return department; }
    public double getCgpa()        { return cgpa; }
    public int getEnrollmentYear() { return enrollmentYear; }

    // Setters with validation
    public void setName(String name) {
        if (name == null || name.trim().isEmpty())
            throw new IllegalArgumentException("Name cannot be empty.");
        this.name = name.trim();
    }

    public void setRollNumber(String roll) {
        if (roll == null || roll.trim().isEmpty())
            throw new IllegalArgumentException("Roll number cannot be empty.");
        this.rollNumber = roll.trim().toUpperCase();
    }

    public void setDepartment(String dept) {
        if (dept == null || dept.trim().isEmpty())
            throw new IllegalArgumentException("Department cannot be empty.");
        this.department = dept.trim();
    }

    public void setCgpa(double cgpa) {
        if (cgpa < 0.0 || cgpa > 4.0)
            throw new IllegalArgumentException("CGPA must be between 0.0 and 4.0.");
        this.cgpa = cgpa;
    }

    // Abstract — subclass decides how to display
    public abstract void displayInfo();

    public abstract String getStudentType();

    @Override
    public String toString() {
        return String.format("[%s] %s | Roll: %s | Dept: %s | CGPA: %.2f",
                getStudentType(), name, rollNumber, department, cgpa);
    }
}

// ============================
// STEP 2: Subclasses
// ============================
class UndergraduateStudent extends Student {
    private int currentSemester;
    private String major;

    public UndergraduateStudent(String name, String roll, String dept,
                                 double cgpa, int year, int semester, String major) {
        super(name, roll, dept, cgpa, year);
        if (semester < 1 || semester > 8)
            throw new IllegalArgumentException("Semester must be 1-8.");
        this.currentSemester = semester;
        this.major = major;
    }

    public int getCurrentSemester() { return currentSemester; }
    public void setCurrentSemester(int sem) {
        if (sem < 1 || sem > 8) throw new IllegalArgumentException("Invalid semester.");
        this.currentSemester = sem;
    }

    @Override
    public void displayInfo() {
        System.out.println("╔══════════════════════════════════════╗");
        System.out.println("║       UNDERGRADUATE STUDENT          ║");
        System.out.println("╠══════════════════════════════════════╣");
        System.out.printf("║ Name       : %-24s║%n", getName());
        System.out.printf("║ Roll       : %-24s║%n", getRollNumber());
        System.out.printf("║ Department : %-24s║%n", getDepartment());
        System.out.printf("║ Major      : %-24s║%n", major);
        System.out.printf("║ Semester   : %-24d║%n", currentSemester);
        System.out.printf("║ CGPA       : %-24.2f║%n", getCgpa());
        System.out.printf("║ Year       : %-24d║%n", getEnrollmentYear());
        System.out.println("╚══════════════════════════════════════╝");
    }

    @Override
    public String getStudentType() { return "UG"; }
}

class GraduateStudent extends Student {
    private String thesisTopic;
    private String supervisor;
    private boolean isFunded;

    public GraduateStudent(String name, String roll, String dept,
                            double cgpa, int year, String thesis, String supervisor, boolean funded) {
        super(name, roll, dept, cgpa, year);
        this.thesisTopic = thesis;
        this.supervisor = supervisor;
        this.isFunded = funded;
    }

    @Override
    public void displayInfo() {
        System.out.println("╔══════════════════════════════════════╗");
        System.out.println("║         GRADUATE STUDENT             ║");
        System.out.println("╠══════════════════════════════════════╣");
        System.out.printf("║ Name       : %-24s║%n", getName());
        System.out.printf("║ Roll       : %-24s║%n", getRollNumber());
        System.out.printf("║ Department : %-24s║%n", getDepartment());
        System.out.printf("║ Thesis     : %-24s║%n", thesisTopic);
        System.out.printf("║ Supervisor : %-24s║%n", supervisor);
        System.out.printf("║ CGPA       : %-24.2f║%n", getCgpa());
        System.out.printf("║ Funded     : %-24s║%n", isFunded ? "Yes" : "No");
        System.out.println("╚══════════════════════════════════════╝");
    }

    @Override
    public String getStudentType() { return "GRAD"; }
}

// ============================
// STEP 3: Repository Interface
// ============================
interface StudentRepository {
    void addStudent(Student student);
    boolean removeStudent(String rollNumber);
    Student findByRoll(String rollNumber);
    List<Student> findByDepartment(String department);
    List<Student> getAllStudents();
    List<Student> getTopStudents(int n);
    void updateCgpa(String rollNumber, double newCgpa);
}

// ============================
// STEP 4: Manager (Composition)
// ============================
class StudentManager implements StudentRepository {
    private final Map<String, Student> studentMap = new LinkedHashMap<>();

    @Override
    public void addStudent(Student student) {
        if (studentMap.containsKey(student.getRollNumber())) {
            throw new IllegalStateException("Student with roll "
                    + student.getRollNumber() + " already exists.");
        }
        studentMap.put(student.getRollNumber(), student);
        System.out.println("✅ Student added: " + student.getName());
    }

    @Override
    public boolean removeStudent(String rollNumber) {
        Student removed = studentMap.remove(rollNumber.toUpperCase());
        if (removed != null) {
            System.out.println("🗑️  Removed: " + removed.getName());
            return true;
        }
        System.out.println("❌ Student not found: " + rollNumber);
        return false;
    }

    @Override
    public Student findByRoll(String rollNumber) {
        return studentMap.get(rollNumber.toUpperCase());
    }

    @Override
    public List<Student> findByDepartment(String department) {
        return studentMap.values().stream()
                .filter(s -> s.getDepartment().equalsIgnoreCase(department))
                .collect(Collectors.toList());
    }

    @Override
    public List<Student> getAllStudents() {
        return new ArrayList<>(studentMap.values());
    }

    @Override
    public List<Student> getTopStudents(int n) {
        return studentMap.values().stream()
                .sorted((a, b) -> Double.compare(b.getCgpa(), a.getCgpa()))
                .limit(n)
                .collect(Collectors.toList());
    }

    @Override
    public void updateCgpa(String rollNumber, double newCgpa) {
        Student s = findByRoll(rollNumber);
        if (s == null) {
            System.out.println("❌ Student not found: " + rollNumber);
            return;
        }
        double old = s.getCgpa();
        s.setCgpa(newCgpa);
        System.out.printf("✅ CGPA updated for %s: %.2f → %.2f%n",
                s.getName(), old, newCgpa);
    }

    public void printAllStudents() {
        if (studentMap.isEmpty()) {
            System.out.println("No students registered.");
            return;
        }
        System.out.println("\n📋 ALL STUDENTS (" + studentMap.size() + " total)");
        System.out.println("─".repeat(60));
        studentMap.values().forEach(s -> System.out.println(s));
        System.out.println("─".repeat(60));
    }

    public void printRankList() {
        System.out.println("\n🏆 RANK LIST (by CGPA)");
        System.out.println("─".repeat(60));
        List<Student> ranked = getTopStudents(studentMap.size());
        for (int i = 0; i < ranked.size(); i++) {
            System.out.printf("Rank %2d: %s%n", (i + 1), ranked.get(i));
        }
        System.out.println("─".repeat(60));
    }
}

// ============================
// STEP 5: Main / Demo
// ============================
public class StudentManagementSystem {
    public static void main(String[] args) {
        StudentManager manager = new StudentManager();

        // Adding students
        System.out.println("=== Adding Students ===");
        manager.addStudent(new UndergraduateStudent(
                "Rafi Ahmed", "CSE-2021-001", "CSE", 3.75, 2021, 7, "AI"));
        manager.addStudent(new UndergraduateStudent(
                "Sumaiya Islam", "CSE-2021-002", "CSE", 3.92, 2021, 7, "Networking"));
        manager.addStudent(new UndergraduateStudent(
                "Tanvir Hassan", "EEE-2022-001", "EEE", 3.50, 2022, 5, "Power"));
        manager.addStudent(new GraduateStudent(
                "Dr. Nasrin", "GRAD-2020-001", "CSE", 3.95, 2020,
                "ML in Healthcare", "Prof. Rahman", true));

        // Display all
        manager.printAllStudents();

        // Search
        System.out.println("\n🔍 Searching for CSE-2021-001:");
        Student found = manager.findByRoll("CSE-2021-001");
        if (found != null) found.displayInfo();

        // Update CGPA
        System.out.println("\n📝 Updating CGPA:");
        manager.updateCgpa("CSE-2021-001", 3.85);

        // Department filter
        System.out.println("\n🏢 CSE Department students:");
        manager.findByDepartment("CSE")
               .forEach(s -> System.out.println("  → " + s));

        // Rank list
        manager.printRankList();

        // Remove
        System.out.println("\n🗑️  Removing student:");
        manager.removeStudent("EEE-2022-001");
        manager.printAllStudents();
    }
}
```

### Dry Run (Trace)

```
addStudent("Rafi Ahmed", "CSE-2021-001", ...)
  → studentMap.containsKey("CSE-2021-001") = false
  → studentMap.put("CSE-2021-001", rafiObject)
  → Output: "✅ Student added: Rafi Ahmed"

findByRoll("CSE-2021-001")
  → studentMap.get("CSE-2021-001")
  → returns rafiObject
  → rafiObject.displayInfo() — UndergraduateStudent এর displayInfo() call হয় (Polymorphism)

updateCgpa("CSE-2021-001", 3.85)
  → findByRoll("CSE-2021-001") → rafiObject
  → old = 3.75
  → rafiObject.setCgpa(3.85) → validation passes → cgpa = 3.85
  → Output: "✅ CGPA updated for Rafi Ahmed: 3.75 → 3.85"

getTopStudents(4)
  → Stream of all students
  → sorted by CGPA descending: Dr.Nasrin(3.95) > Sumaiya(3.92) > Rafi(3.85) > Tanvir(3.50)
  → Rank list printed
```

### Interview Explanation Strategy

> **"আমি Student Management System এ OOP এর সব pillar apply করেছি।**
>
> প্রথমে `Student` abstract class বানিয়েছি — **Encapsulation** এ সব fields private, validation সহ setter। **Abstraction** এ `displayInfo()` pure abstract — প্রতিটি subclass নিজে implement করে।
>
> `UndergraduateStudent` ও `GraduateStudent` — **Inheritance** — shared fields parent এ, specific fields child এ।
>
> `StudentRepository` interface — contract define করে। `StudentManager` implement করে — **Composition**, `Map<String, Student>` দিয়ে data hold করে।
>
> `printRankList()` এ `Stream` sort করলে `getCgpa()` call হয় সব student এ — **Polymorphism** — runtime এ সঠিক object এর cgpa return হয়।"

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.২ Bank Management System

### Problem Statement

একটি **Bank Management System** design করুন যেখানে:
- Account খোলা যাবে (Savings, Current, Fixed Deposit)
- Deposit এবং Withdraw করা যাবে
- Transfer করা যাবে এক account থেকে অন্যটিতে
- Transaction history দেখা যাবে
- Interest calculate হবে account type অনুযায়ী
- Balance check করা যাবে

---

### Clean Code — Java

```java
import java.util.*;
import java.time.LocalDateTime;
import java.time.format.DateTimeFormatter;

// ============================
// Transaction Record
// ============================
class Transaction {
    public enum Type { DEPOSIT, WITHDRAWAL, TRANSFER_IN, TRANSFER_OUT, INTEREST }

    private final Type type;
    private final double amount;
    private final double balanceAfter;
    private final String description;
    private final LocalDateTime timestamp;

    public Transaction(Type type, double amount, double balanceAfter, String desc) {
        this.type = type;
        this.amount = amount;
        this.balanceAfter = balanceAfter;
        this.description = desc;
        this.timestamp = LocalDateTime.now();
    }

    @Override
    public String toString() {
        String icon = switch (type) {
            case DEPOSIT, TRANSFER_IN, INTEREST -> "📈";
            case WITHDRAWAL, TRANSFER_OUT       -> "📉";
        };
        return String.format("%s [%s] %-16s BDT %10.2f | Balance: %10.2f | %s",
                icon,
                timestamp.format(DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm")),
                type, amount, balanceAfter, description);
    }
}

// ============================
// Abstract Account
// ============================
abstract class BankAccount {
    private final String accountNumber;
    private final String ownerName;
    private double balance;
    private final List<Transaction> transactions = new ArrayList<>();
    private boolean isActive = true;

    public BankAccount(String accountNumber, String ownerName, double initialDeposit) {
        this.accountNumber = accountNumber;
        this.ownerName = ownerName;
        if (initialDeposit < getMinimumBalance())
            throw new IllegalArgumentException(
                "Minimum opening balance is BDT " + getMinimumBalance());
        this.balance = initialDeposit;
        recordTransaction(Transaction.Type.DEPOSIT, initialDeposit, "Account opened");
    }

    // Template method — subclass provides minimum balance
    public abstract double getMinimumBalance();
    public abstract double calculateInterest();
    public abstract String getAccountType();

    // Common operations — Encapsulation
    public synchronized void deposit(double amount) {
        validateActive();
        if (amount <= 0) throw new IllegalArgumentException("Deposit amount must be positive.");
        balance += amount;
        recordTransaction(Transaction.Type.DEPOSIT, amount, "Cash deposit");
        System.out.printf("✅ Deposited BDT %.2f to %s. New balance: BDT %.2f%n",
                amount, accountNumber, balance);
    }

    public synchronized void withdraw(double amount) {
        validateActive();
        if (amount <= 0) throw new IllegalArgumentException("Withdrawal amount must be positive.");
        if (amount > balance - getMinimumBalance())
            throw new IllegalStateException(
                "Insufficient funds. Minimum balance BDT " + getMinimumBalance() + " must be maintained.");
        balance -= amount;
        recordTransaction(Transaction.Type.WITHDRAWAL, amount, "Cash withdrawal");
        System.out.printf("✅ Withdrawn BDT %.2f from %s. Remaining: BDT %.2f%n",
                amount, accountNumber, balance);
    }

    public synchronized void transfer(BankAccount target, double amount) {
        validateActive();
        if (amount <= 0) throw new IllegalArgumentException("Transfer amount must be positive.");
        if (amount > balance - getMinimumBalance())
            throw new IllegalStateException("Insufficient balance for transfer.");

        balance -= amount;
        recordTransaction(Transaction.Type.TRANSFER_OUT, amount,
                "Transfer to " + target.getAccountNumber());

        target.balance += amount;
        target.recordTransaction(Transaction.Type.TRANSFER_IN, amount,
                "Transfer from " + this.accountNumber);

        System.out.printf("✅ Transferred BDT %.2f: %s → %s%n",
                amount, accountNumber, target.getAccountNumber());
    }

    public void applyInterest() {
        double interest = calculateInterest();
        if (interest > 0) {
            balance += interest;
            recordTransaction(Transaction.Type.INTEREST, interest,
                    getAccountType() + " interest applied");
            System.out.printf("💰 Interest BDT %.2f applied to %s%n", interest, accountNumber);
        }
    }

    private void validateActive() {
        if (!isActive) throw new IllegalStateException("Account " + accountNumber + " is inactive.");
    }

    private void recordTransaction(Transaction.Type type, double amount, String desc) {
        transactions.add(new Transaction(type, amount, balance, desc));
    }

    public void printStatement() {
        System.out.println("\n" + "═".repeat(80));
        System.out.printf("  ACCOUNT STATEMENT — %s (%s)%n", accountNumber, getAccountType());
        System.out.printf("  Owner: %s | Balance: BDT %.2f%n", ownerName, balance);
        System.out.println("═".repeat(80));
        if (transactions.isEmpty()) {
            System.out.println("  No transactions.");
        } else {
            transactions.forEach(t -> System.out.println("  " + t));
        }
        System.out.println("═".repeat(80));
    }

    // Getters
    public String getAccountNumber() { return accountNumber; }
    public String getOwnerName()     { return ownerName; }
    public double getBalance()        { return balance; }
    public boolean isActive()         { return isActive; }
    public void closeAccount()        { this.isActive = false; }

    @Override
    public String toString() {
        return String.format("[%s] Acc#: %s | Owner: %-20s | Balance: BDT %10.2f | %s",
                getAccountType(), accountNumber, ownerName, balance,
                isActive ? "ACTIVE" : "CLOSED");
    }
}

// ============================
// Account Types (Inheritance)
// ============================
class SavingsAccount extends BankAccount {
    private static final double MIN_BALANCE = 1000.0;
    private static final double INTEREST_RATE = 0.06; // 6% per year
    private int withdrawalsThisMonth = 0;
    private static final int MAX_MONTHLY_WITHDRAWALS = 5;

    public SavingsAccount(String accNum, String owner, double initial) {
        super(accNum, owner, initial);
    }

    @Override
    public double getMinimumBalance() { return MIN_BALANCE; }

    @Override
    public double calculateInterest() {
        return getBalance() * INTEREST_RATE / 12; // Monthly interest
    }

    @Override
    public String getAccountType() { return "SAVINGS"; }

    @Override
    public synchronized void withdraw(double amount) {
        if (withdrawalsThisMonth >= MAX_MONTHLY_WITHDRAWALS)
            throw new IllegalStateException(
                "Monthly withdrawal limit (" + MAX_MONTHLY_WITHDRAWALS + ") reached.");
        super.withdraw(amount);
        withdrawalsThisMonth++;
    }

    public void resetMonthlyCounter() { withdrawalsThisMonth = 0; }
}

class CurrentAccount extends BankAccount {
    private static final double MIN_BALANCE = 5000.0;
    private static final double OVERDRAFT_LIMIT = 10000.0;
    private static final double INTEREST_RATE = 0.02; // 2% per year

    public CurrentAccount(String accNum, String owner, double initial) {
        super(accNum, owner, initial);
    }

    @Override
    public double getMinimumBalance() { return MIN_BALANCE; }

    @Override
    public double calculateInterest() {
        return getBalance() * INTEREST_RATE / 12;
    }

    @Override
    public String getAccountType() { return "CURRENT"; }

    // Current accounts can go below minimum (overdraft) up to a limit
    @Override
    public synchronized void withdraw(double amount) {
        if (amount <= 0) throw new IllegalArgumentException("Amount must be positive.");
        if (amount > getBalance() + OVERDRAFT_LIMIT)
            throw new IllegalStateException("Overdraft limit exceeded (BDT " + OVERDRAFT_LIMIT + ").");
        // Bypass parent validation — call grandparent logic manually via deposit approach
        super.withdraw(Math.min(amount, getBalance() - getMinimumBalance()));
    }
}

class FixedDepositAccount extends BankAccount {
    private static final double MIN_BALANCE = 10000.0;
    private final double interestRate;
    private final int tenureMonths;
    private final LocalDateTime maturityDate;
    private boolean matured = false;

    public FixedDepositAccount(String accNum, String owner,
                                double amount, double rate, int months) {
        super(accNum, owner, amount);
        this.interestRate = rate;
        this.tenureMonths = months;
        this.maturityDate = LocalDateTime.now().plusMonths(months);
    }

    @Override
    public double getMinimumBalance() { return MIN_BALANCE; }

    @Override
    public double calculateInterest() {
        // Simple interest: P × R × T
        return getBalance() * interestRate * (tenureMonths / 12.0);
    }

    @Override
    public String getAccountType() { return "FIXED DEPOSIT"; }

    @Override
    public synchronized void withdraw(double amount) {
        if (!matured)
            throw new IllegalStateException(
                "FD cannot be withdrawn before maturity: " +
                maturityDate.format(DateTimeFormatter.ofPattern("yyyy-MM-dd")));
        super.withdraw(amount);
    }

    public void mature() {
        this.matured = true;
        applyInterest();
        System.out.println("🎉 Fixed Deposit matured! Interest applied.");
    }

    public LocalDateTime getMaturityDate() { return maturityDate; }
}

// ============================
// Bank (Composition + Factory)
// ============================
class Bank {
    private final String bankName;
    private final Map<String, BankAccount> accounts = new LinkedHashMap<>();
    private int accountCounter = 1000;

    public Bank(String name) { this.bankName = name; }

    private String generateAccountNumber(String prefix) {
        return prefix + "-" + (++accountCounter);
    }

    // Factory methods
    public SavingsAccount openSavingsAccount(String owner, double initial) {
        String accNum = generateAccountNumber("SAV");
        SavingsAccount acc = new SavingsAccount(accNum, owner, initial);
        accounts.put(accNum, acc);
        System.out.println("🏦 Savings account opened: " + accNum + " for " + owner);
        return acc;
    }

    public CurrentAccount openCurrentAccount(String owner, double initial) {
        String accNum = generateAccountNumber("CUR");
        CurrentAccount acc = new CurrentAccount(accNum, owner, initial);
        accounts.put(accNum, acc);
        System.out.println("🏦 Current account opened: " + accNum + " for " + owner);
        return acc;
    }

    public FixedDepositAccount openFDAccount(String owner, double amount,
                                              double rate, int months) {
        String accNum = generateAccountNumber("FD");
        FixedDepositAccount acc = new FixedDepositAccount(accNum, owner, amount, rate, months);
        accounts.put(accNum, acc);
        System.out.printf("🏦 FD account opened: %s for %s | Rate: %.1f%% | %d months%n",
                accNum, owner, rate * 100, months);
        return acc;
    }

    public BankAccount getAccount(String accNum) {
        BankAccount acc = accounts.get(accNum);
        if (acc == null) throw new NoSuchElementException("Account not found: " + accNum);
        return acc;
    }

    public void applyInterestToAll() {
        System.out.println("\n💰 Applying monthly interest to all accounts...");
        accounts.values().stream()
                .filter(BankAccount::isActive)
                .forEach(BankAccount::applyInterest);
    }

    public void printAllAccounts() {
        System.out.println("\n🏛️  " + bankName + " — ALL ACCOUNTS");
        System.out.println("─".repeat(80));
        accounts.values().forEach(a -> System.out.println("  " + a));
        System.out.println("─".repeat(80));
        double totalDeposits = accounts.values().stream()
                .mapToDouble(BankAccount::getBalance).sum();
        System.out.printf("  Total deposits: BDT %.2f%n", totalDeposits);
    }
}

// ============================
// Main Demo
// ============================
public class BankManagementSystem {
    public static void main(String[] args) {
        Bank bank = new Bank("Sonali Digital Bank");

        System.out.println("=== Opening Accounts ===");
        SavingsAccount rafiAcc = bank.openSavingsAccount("Rafi Ahmed", 50000);
        CurrentAccount bizAcc  = bank.openCurrentAccount("Rafi's Business", 100000);
        FixedDepositAccount fdAcc = bank.openFDAccount("Sumaiya Islam", 200000, 0.09, 12);

        System.out.println("\n=== Transactions ===");
        rafiAcc.deposit(25000);
        rafiAcc.withdraw(10000);
        bizAcc.deposit(50000);

        System.out.println("\n=== Transfer ===");
        rafiAcc.transfer(bizAcc, 15000);

        System.out.println("\n=== Monthly Interest ===");
        bank.applyInterestToAll();

        System.out.println("\n=== FD Maturity ===");
        fdAcc.mature();

        System.out.println("\n=== Statements ===");
        rafiAcc.printStatement();

        bank.printAllAccounts();
    }
}
```

### Dry Run

```
openSavingsAccount("Rafi Ahmed", 50000)
  → generateAccountNumber("SAV") → "SAV-1001"
  → new SavingsAccount("SAV-1001", "Rafi Ahmed", 50000)
    → getMinimumBalance() = 1000 ≤ 50000 ✅
    → balance = 50000
    → recordTransaction(DEPOSIT, 50000, "Account opened")
  → accounts.put("SAV-1001", acc)

rafiAcc.withdraw(10000)
  → withdrawalsThisMonth(0) < MAX(5) ✅
  → super.withdraw(10000)
    → validateActive() → isActive=true ✅
    → 10000 ≤ (50000 - 1000) = 49000 ✅
    → balance = 50000 - 10000 = 40000
    → recordTransaction(WITHDRAWAL, 10000, "Cash withdrawal")
  → withdrawalsThisMonth = 1

rafiAcc.transfer(bizAcc, 15000)
  → validateActive() ✅
  → 15000 ≤ (40000 - 1000) = 39000 ✅
  → rafiAcc.balance = 40000 - 15000 = 25000
  → recordTransaction(TRANSFER_OUT, 15000, "Transfer to CUR-1002")
  → bizAcc.balance = 150000 + 15000 = 165000
  → bizAcc.recordTransaction(TRANSFER_IN, 15000, "Transfer from SAV-1001")

calculateInterest() for SavingsAccount:
  → 25000 × 0.06 / 12 = 125.0
  → balance = 25000 + 125 = 25125
```

### Interview Explanation Strategy

> **"এই Bank Management System এ আমি Template Method Pattern ও Factory Pattern ব্যবহার করেছি OOP এর সাথে।**
>
> `BankAccount` abstract class — **Template Method**: `withdraw()`, `deposit()` common logic parent এ, `getMinimumBalance()`, `calculateInterest()`, `getAccountType()` abstract — subclass implement করে।
>
> `SavingsAccount`, `CurrentAccount`, `FixedDepositAccount` — **Inheritance** — type-specific rules আলাদা।
>
> **Encapsulation:** `balance` private, শুধু `deposit()`, `withdraw()`, `transfer()` দিয়ে change হয় — সরাসরি access নেই।
>
> **Polymorphism:** `bank.applyInterestToAll()` — সব account এ `applyInterest()` call হয় → `calculateInterest()` virtual — runtime এ Savings এর 6%, FD এর 9% আলাদাভাবে calculate হয়।
>
> `Bank` class factory methods দিয়ে account তৈরি করে — client `new` করে না।"

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৩ Employee Management System

### Problem Statement

একটি **Employee Management System** design করুন যেখানে:
- Full-time, Part-time, Contract employee আছে
- Salary calculate হবে employee type অনুযায়ী
- Department management
- Leave management
- Performance review
- Payroll generation

---

### Clean Code — Java

```java
import java.util.*;
import java.util.stream.*;

// ============================
// Enums
// ============================
enum Department { CSE, HR, FINANCE, MARKETING, OPERATIONS }
enum LeaveType  { SICK, CASUAL, ANNUAL, MATERNITY }
enum Grade      { A, B, C, D, F }

// ============================
// Leave Record
// ============================
class LeaveRecord {
    private final LeaveType type;
    private final int days;
    private final String reason;
    private boolean approved;

    public LeaveRecord(LeaveType type, int days, String reason) {
        this.type = type;
        this.days = days;
        this.reason = reason;
        this.approved = false;
    }

    public void approve() { this.approved = true; }

    @Override
    public String toString() {
        return String.format("Leave[%s, %d days, %s, %s]",
                type, days, reason, approved ? "APPROVED" : "PENDING");
    }
}

// ============================
// Abstract Employee
// ============================
abstract class Employee {
    private final String employeeId;
    private String name;
    private Department department;
    private int yearsOfExperience;
    private Grade performanceGrade;
    private final List<LeaveRecord> leaveHistory = new ArrayList<>();
    private int availableLeaveDays = 20;

    public Employee(String id, String name, Department dept, int experience) {
        this.employeeId = id;
        setName(name);
        this.department = dept;
        this.yearsOfExperience = experience;
        this.performanceGrade = Grade.B; // Default
    }

    // Abstract: Each type calculates salary differently
    public abstract double calculateGrossSalary();
    public abstract double calculateNetSalary();
    public abstract String getEmployeeType();

    // Common: Template method for payslip
    public final void generatePaySlip() {
        System.out.println("\n" + "═".repeat(50));
        System.out.printf("  PAY SLIP — %s (%s)%n", name, getEmployeeType());
        System.out.println("═".repeat(50));
        System.out.printf("  Employee ID : %s%n", employeeId);
        System.out.printf("  Department  : %s%n", department);
        System.out.printf("  Experience  : %d years%n", yearsOfExperience);
        System.out.printf("  Performance : Grade %s%n", performanceGrade);
        System.out.println("  " + "─".repeat(46));
        printSalaryDetails(); // Hook — subclass can override
        System.out.printf("  Gross Salary: BDT %,.2f%n", calculateGrossSalary());
        System.out.printf("  Net Salary  : BDT %,.2f%n", calculateNetSalary());
        System.out.println("═".repeat(50));
    }

    // Hook method — subclass overrides for custom salary breakdown
    protected void printSalaryDetails() {}

    public boolean applyLeave(LeaveType type, int days, String reason) {
        if (days > availableLeaveDays) {
            System.out.printf("❌ %s: Insufficient leave balance (%d days available)%n",
                    name, availableLeaveDays);
            return false;
        }
        LeaveRecord leave = new LeaveRecord(type, days, reason);
        leaveHistory.add(leave);
        availableLeaveDays -= days;
        leave.approve(); // Auto-approve for simplicity
        System.out.printf("✅ %s: %d days %s leave approved. Remaining: %d days%n",
                name, days, type, availableLeaveDays);
        return true;
    }

    public void setPerformanceGrade(Grade grade) {
        this.performanceGrade = grade;
        System.out.printf("📊 %s performance grade set to: %s%n", name, grade);
    }

    // Getters / Setters
    public String getEmployeeId()       { return employeeId; }
    public String getName()             { return name; }
    public Department getDepartment()   { return department; }
    public int getYearsOfExperience()   { return yearsOfExperience; }
    public Grade getPerformanceGrade()  { return performanceGrade; }
    public int getAvailableLeaveDays()  { return availableLeaveDays; }

    public void setName(String name) {
        if (name == null || name.trim().isEmpty())
            throw new IllegalArgumentException("Name cannot be empty.");
        this.name = name.trim();
    }

    public void setDepartment(Department dept) { this.department = dept; }

    @Override
    public String toString() {
        return String.format("[%s] %s (ID: %s) | Dept: %s | Salary: BDT %,.0f",
                getEmployeeType(), name, employeeId, department, calculateNetSalary());
    }
}

// ============================
// Full-Time Employee
// ============================
class FullTimeEmployee extends Employee {
    private double basicSalary;
    private double houseAllowance;    // 40% of basic
    private double medicalAllowance;  // 10% of basic
    private double transportAllowance;// 10% of basic
    private static final double TAX_RATE = 0.10;
    private static final double PF_RATE  = 0.10; // Provident Fund

    public FullTimeEmployee(String id, String name, Department dept,
                             int experience, double basicSalary) {
        super(id, name, dept, experience);
        this.basicSalary = basicSalary;
        this.houseAllowance     = basicSalary * 0.40;
        this.medicalAllowance   = basicSalary * 0.10;
        this.transportAllowance = basicSalary * 0.10;
    }

    @Override
    public double calculateGrossSalary() {
        return basicSalary + houseAllowance + medicalAllowance + transportAllowance;
    }

    @Override
    public double calculateNetSalary() {
        double gross = calculateGrossSalary();
        double tax   = gross * TAX_RATE;
        double pf    = basicSalary * PF_RATE;
        return gross - tax - pf;
    }

    @Override
    public String getEmployeeType() { return "FULL-TIME"; }

    @Override
    protected void printSalaryDetails() {
        System.out.printf("  Basic       : BDT %,.2f%n", basicSalary);
        System.out.printf("  House Allw. : BDT %,.2f%n", houseAllowance);
        System.out.printf("  Medical     : BDT %,.2f%n", medicalAllowance);
        System.out.printf("  Transport   : BDT %,.2f%n", transportAllowance);
        System.out.printf("  Tax (10%%)   : BDT %,.2f%n", calculateGrossSalary() * TAX_RATE);
        System.out.printf("  PF (10%%)    : BDT %,.2f%n", basicSalary * PF_RATE);
    }

    public void giveIncrement(double percentage) {
        double oldSalary = basicSalary;
        basicSalary *= (1 + percentage / 100);
        houseAllowance     = basicSalary * 0.40;
        medicalAllowance   = basicSalary * 0.10;
        transportAllowance = basicSalary * 0.10;
        System.out.printf("💹 %s increment: BDT %,.0f → BDT %,.0f (%.1f%%)%n",
                getName(), oldSalary, basicSalary, percentage);
    }
}

// ============================
// Part-Time Employee
// ============================
class PartTimeEmployee extends Employee {
    private double hourlyRate;
    private int hoursWorkedThisMonth;

    public PartTimeEmployee(String id, String name, Department dept,
                             int experience, double hourlyRate) {
        super(id, name, dept, experience);
        this.hourlyRate = hourlyRate;
        this.hoursWorkedThisMonth = 0;
    }

    public void logHours(int hours) {
        if (hours < 0) throw new IllegalArgumentException("Hours cannot be negative.");
        hoursWorkedThisMonth += hours;
        System.out.printf("⏱️  %s logged %d hours. Total this month: %d%n",
                getName(), hours, hoursWorkedThisMonth);
    }

    @Override
    public double calculateGrossSalary() {
        return hourlyRate * hoursWorkedThisMonth;
    }

    @Override
    public double calculateNetSalary() {
        return calculateGrossSalary() * 0.90; // 10% tax flat
    }

    @Override
    public String getEmployeeType() { return "PART-TIME"; }

    @Override
    protected void printSalaryDetails() {
        System.out.printf("  Hourly Rate : BDT %,.2f%n", hourlyRate);
        System.out.printf("  Hours Worked: %d hrs%n", hoursWorkedThisMonth);
        System.out.printf("  Tax (10%%)   : BDT %,.2f%n", calculateGrossSalary() * 0.10);
    }
}

// ============================
// Contract Employee
// ============================
class ContractEmployee extends Employee {
    private double contractAmount;
    private int contractDurationMonths;
    private int monthsCompleted;

    public ContractEmployee(String id, String name, Department dept,
                             int experience, double contractAmount, int durationMonths) {
        super(id, name, dept, experience);
        this.contractAmount = contractAmount;
        this.contractDurationMonths = durationMonths;
        this.monthsCompleted = 0;
    }

    public void completeMonth() {
        if (monthsCompleted < contractDurationMonths) monthsCompleted++;
    }

    @Override
    public double calculateGrossSalary() {
        return contractAmount / contractDurationMonths; // Monthly installment
    }

    @Override
    public double calculateNetSalary() {
        return calculateGrossSalary() * 0.85; // 15% tax + no benefits
    }

    @Override
    public String getEmployeeType() { return "CONTRACT"; }

    @Override
    protected void printSalaryDetails() {
        System.out.printf("  Contract Amt: BDT %,.2f%n", contractAmount);
        System.out.printf("  Duration    : %d months (%d completed)%n",
                contractDurationMonths, monthsCompleted);
        System.out.printf("  Monthly     : BDT %,.2f%n", calculateGrossSalary());
        System.out.printf("  Tax (15%%)   : BDT %,.2f%n", calculateGrossSalary() * 0.15);
    }
}

// ============================
// Department Manager
// ============================
class DepartmentManager {
    private final Department department;
    private final List<Employee> employees = new ArrayList<>();

    public DepartmentManager(Department department) {
        this.department = department;
    }

    public void addEmployee(Employee emp) {
        if (emp.getDepartment() != department)
            throw new IllegalArgumentException(emp.getName() + " is not in " + department);
        employees.add(emp);
        System.out.println("👤 " + emp.getName() + " added to " + department);
    }

    public void removeEmployee(String id) {
        employees.removeIf(e -> e.getEmployeeId().equals(id));
    }

    public void runMonthlyPayroll() {
        System.out.println("\n💼 MONTHLY PAYROLL — " + department);
        System.out.println("─".repeat(60));
        double totalCost = 0;
        for (Employee e : employees) {
            e.generatePaySlip(); // Polymorphism
            totalCost += e.calculateNetSalary();
        }
        System.out.printf("%n💰 Total payroll cost for %s: BDT %,.2f%n",
                department, totalCost);
    }

    public Employee getTopPerformer() {
        return employees.stream()
                .min(Comparator.comparing(e -> e.getPerformanceGrade().ordinal()))
                .orElse(null);
    }

    public List<Employee> getEmployees() { return Collections.unmodifiableList(employees); }
}

// ============================
// Main Demo
// ============================
public class EmployeeManagementSystem {
    public static void main(String[] args) {
        // Create full-time employees
        FullTimeEmployee rafi = new FullTimeEmployee(
                "EMP-001", "Rafi Ahmed", Department.CSE, 3, 60000);
        FullTimeEmployee sumaiya = new FullTimeEmployee(
                "EMP-002", "Sumaiya Islam", Department.CSE, 5, 80000);

        // Part-time
        PartTimeEmployee tanvir = new PartTimeEmployee(
                "EMP-003", "Tanvir Hassan", Department.CSE, 1, 400);
        tanvir.logHours(80);
        tanvir.logHours(40);

        // Contract
        ContractEmployee nasrin = new ContractEmployee(
                "EMP-004", "Nasrin Akter", Department.CSE, 2, 600000, 6);

        // Department setup
        DepartmentManager cse = new DepartmentManager(Department.CSE);
        cse.addEmployee(rafi);
        cse.addEmployee(sumaiya);
        cse.addEmployee(tanvir);
        cse.addEmployee(nasrin);

        // Performance reviews
        sumaiya.setPerformanceGrade(Grade.A);
        rafi.setPerformanceGrade(Grade.B);

        // Leave management
        rafi.applyLeave(LeaveType.ANNUAL, 5, "Family vacation");
        sumaiya.applyLeave(LeaveType.SICK, 2, "Flu");

        // Increment
        rafi.giveIncrement(15.0);

        // Payroll
        cse.runMonthlyPayroll();

        // Top performer
        Employee top = cse.getTopPerformer();
        if (top != null)
            System.out.printf("%n🏆 Top performer in CSE: %s (Grade %s)%n",
                    top.getName(), top.getPerformanceGrade());
    }
}
```

### Interview Explanation Strategy

> **"Employee Management System এ আমি Template Method Pattern সবচেয়ে বেশি ব্যবহার করেছি।**
>
> `generatePaySlip()` method `final` — override করা যাবে না। কিন্তু ভেতরে `printSalaryDetails()` একটি **hook method** — subclass override করে নিজের breakdown দেখায়।
>
> `calculateGrossSalary()` ও `calculateNetSalary()` abstract — Full-time এ basic+allowances, Part-time এ hourly×hours, Contract এ monthly installment।
>
> **Polymorphism:** `runMonthlyPayroll()` এ সব employee এর `generatePaySlip()` call হয় — runtime এ সঠিক subclass এর logic execute হয়।"

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৪ Library Management System

### Problem Statement

একটি **Library Management System** design করুন যেখানে:
- Book যোগ করা ও delete করা যাবে
- Member registration করা যাবে
- Book issue ও return করা যাবে
- Fine calculate হবে (overdue এ)
- Search করা যাবে (title, author, ISBN)
- Reservation system থাকবে

---

### Clean Code — Java

```java
import java.util.*;
import java.time.*;
import java.time.format.DateTimeFormatter;
import java.util.stream.*;

// ============================
// Book (Encapsulation)
// ============================
class Book {
    private final String isbn;
    private String title;
    private String author;
    private String genre;
    private int totalCopies;
    private int availableCopies;

    public Book(String isbn, String title, String author, String genre, int copies) {
        this.isbn = isbn;
        this.title = title;
        this.author = author;
        this.genre = genre;
        this.totalCopies = copies;
        this.availableCopies = copies;
    }

    public boolean isAvailable()   { return availableCopies > 0; }
    public void checkOut()         {
        if (!isAvailable()) throw new IllegalStateException("No copies available.");
        availableCopies--;
    }
    public void returnCopy()       { if (availableCopies < totalCopies) availableCopies++; }

    // Getters
    public String getIsbn()         { return isbn; }
    public String getTitle()        { return title; }
    public String getAuthor()       { return author; }
    public String getGenre()        { return genre; }
    public int getAvailableCopies() { return availableCopies; }
    public int getTotalCopies()     { return totalCopies; }

    @Override
    public String toString() {
        return String.format("ISBN: %-14s | %-35s by %-20s | %d/%d available",
                isbn, title, author, availableCopies, totalCopies);
    }
}

// ============================
// Loan Record
// ============================
class LoanRecord {
    public enum Status { ACTIVE, RETURNED, OVERDUE }

    private final String loanId;
    private final String memberId;
    private final String isbn;
    private final LocalDate issueDate;
    private final LocalDate dueDate;
    private LocalDate returnDate;
    private Status status;
    private double fine;

    private static final int LOAN_PERIOD_DAYS = 14;
    private static final double FINE_PER_DAY   = 5.0; // BDT 5 per day

    public LoanRecord(String loanId, String memberId, String isbn) {
        this.loanId = loanId;
        this.memberId = memberId;
        this.isbn = isbn;
        this.issueDate = LocalDate.now();
        this.dueDate = issueDate.plusDays(LOAN_PERIOD_DAYS);
        this.status = Status.ACTIVE;
        this.fine = 0;
    }

    public double processReturn() {
        this.returnDate = LocalDate.now();
        this.status = Status.RETURNED;
        if (returnDate.isAfter(dueDate)) {
            long overdueDays = ChronoUnit.DAYS.between(dueDate, returnDate);
            this.fine = overdueDays * FINE_PER_DAY;
            System.out.printf("⚠️  Overdue by %d days. Fine: BDT %.2f%n", overdueDays, fine);
        }
        return fine;
    }

    public boolean isOverdue() {
        return status == Status.ACTIVE && LocalDate.now().isAfter(dueDate);
    }

    public String getLoanId()  { return loanId; }
    public String getMemberId(){ return memberId; }
    public String getIsbn()    { return isbn; }
    public Status getStatus()  { return status; }
    public double getFine()    { return fine; }
    public LocalDate getDueDate(){ return dueDate; }

    @Override
    public String toString() {
        String dueDateStr = dueDate.format(DateTimeFormatter.ofPattern("dd MMM yyyy"));
        return String.format("Loan[%s] ISBN: %s | Due: %s | %s%s",
                loanId, isbn, dueDateStr, status,
                fine > 0 ? " | Fine: BDT " + fine : "");
    }
}

// ============================
// Member (Abstract — Inheritance)
// ============================
abstract class LibraryMember {
    private final String memberId;
    private String name;
    private String email;
    private final LocalDate membershipDate;
    private final List<LoanRecord> loanHistory = new ArrayList<>();
    private double totalFines = 0;

    public LibraryMember(String memberId, String name, String email) {
        this.memberId = memberId;
        setName(name);
        this.email = email;
        this.membershipDate = LocalDate.now();
    }

    public abstract int getMaxBooksAllowed();
    public abstract int getLoanPeriodDays();
    public abstract String getMemberType();

    public List<LoanRecord> getActiveLoanRecords() {
        return loanHistory.stream()
                .filter(l -> l.getStatus() == LoanRecord.Status.ACTIVE)
                .collect(Collectors.toList());
    }

    public boolean canBorrow() {
        return getActiveLoanRecords().size() < getMaxBooksAllowed();
    }

    public void addLoanRecord(LoanRecord record) {
        loanHistory.add(record);
    }

    public LoanRecord findActiveLoan(String isbn) {
        return loanHistory.stream()
                .filter(l -> l.getIsbn().equals(isbn) && l.getStatus() == LoanRecord.Status.ACTIVE)
                .findFirst().orElse(null);
    }

    public void payFine(double amount) {
        if (amount <= 0 || amount > totalFines)
            throw new IllegalArgumentException("Invalid fine payment.");
        totalFines -= amount;
        System.out.printf("✅ %s paid fine: BDT %.2f. Remaining: BDT %.2f%n",
                name, amount, totalFines);
    }

    public void addFine(double amount) { totalFines += amount; }

    // Getters
    public String getMemberId()  { return memberId; }
    public String getName()      { return name; }
    public String getEmail()     { return email; }
    public double getTotalFines(){ return totalFines; }
    public List<LoanRecord> getLoanHistory() { return Collections.unmodifiableList(loanHistory); }

    public void setName(String name) {
        if (name == null || name.trim().isEmpty())
            throw new IllegalArgumentException("Name cannot be empty.");
        this.name = name.trim();
    }

    @Override
    public String toString() {
        return String.format("[%s] %s (ID: %s) | Active loans: %d/%d | Fines: BDT %.2f",
                getMemberType(), name, memberId,
                getActiveLoanRecords().size(), getMaxBooksAllowed(), totalFines);
    }
}

// ============================
// Member Types (Polymorphism)
// ============================
class StudentMember extends LibraryMember {
    private String university;
    private String studentId;

    public StudentMember(String memberId, String name, String email,
                          String university, String studentId) {
        super(memberId, name, email);
        this.university = university;
        this.studentId = studentId;
    }

    @Override public int getMaxBooksAllowed() { return 3; }
    @Override public int getLoanPeriodDays()  { return 14; }
    @Override public String getMemberType()   { return "STUDENT"; }
}

class FacultyMember extends LibraryMember {
    private String designation;
    private String department;

    public FacultyMember(String memberId, String name, String email,
                          String designation, String department) {
        super(memberId, name, email);
        this.designation = designation;
        this.department = department;
    }

    @Override public int getMaxBooksAllowed() { return 10; }
    @Override public int getLoanPeriodDays()  { return 30; }
    @Override public String getMemberType()   { return "FACULTY"; }
}

class PublicMember extends LibraryMember {
    private String address;

    public PublicMember(String memberId, String name, String email, String address) {
        super(memberId, name, email);
        this.address = address;
    }

    @Override public int getMaxBooksAllowed() { return 2; }
    @Override public int getLoanPeriodDays()  { return 7; }
    @Override public String getMemberType()   { return "PUBLIC"; }
}

// ============================
// Library System (Composition)
// ============================
class Library {
    private final String libraryName;
    private final Map<String, Book> books    = new LinkedHashMap<>();
    private final Map<String, LibraryMember> members = new LinkedHashMap<>();
    private final List<LoanRecord> allLoans  = new ArrayList<>();
    private int loanCounter = 1;

    public Library(String name) { this.libraryName = name; }

    // Book management
    public void addBook(Book book) {
        books.put(book.getIsbn(), book);
        System.out.println("📚 Book added: " + book.getTitle());
    }

    public void removeBook(String isbn) {
        Book removed = books.remove(isbn);
        if (removed != null) System.out.println("🗑️  Removed: " + removed.getTitle());
        else System.out.println("❌ Book not found: " + isbn);
    }

    // Member management
    public void registerMember(LibraryMember member) {
        members.put(member.getMemberId(), member);
        System.out.println("👤 Member registered: " + member.getName()
                + " [" + member.getMemberType() + "]");
    }

    // Issue book
    public LoanRecord issueBook(String memberId, String isbn) {
        LibraryMember member = members.get(memberId);
        Book book = books.get(isbn);

        if (member == null) throw new NoSuchElementException("Member not found: " + memberId);
        if (book == null)   throw new NoSuchElementException("Book not found: " + isbn);
        if (!member.canBorrow())
            throw new IllegalStateException(member.getName() + " has reached borrow limit ("
                    + member.getMaxBooksAllowed() + " books).");
        if (!book.isAvailable())
            throw new IllegalStateException("'" + book.getTitle() + "' is not available.");

        book.checkOut();
        String loanId = "LN-" + String.format("%04d", loanCounter++);
        LoanRecord loan = new LoanRecord(loanId, memberId, isbn);
        member.addLoanRecord(loan);
        allLoans.add(loan);

        System.out.printf("📖 Issued: '%s' to %s | Due: %s%n",
                book.getTitle(), member.getName(),
                loan.getDueDate().format(DateTimeFormatter.ofPattern("dd MMM yyyy")));
        return loan;
    }

    // Return book
    public double returnBook(String memberId, String isbn) {
        LibraryMember member = members.get(memberId);
        Book book = books.get(isbn);

        if (member == null || book == null)
            throw new NoSuchElementException("Member or book not found.");

        LoanRecord loan = member.findActiveLoan(isbn);
        if (loan == null)
            throw new IllegalStateException(member.getName() + " has no active loan for this book.");

        double fine = loan.processReturn();
        book.returnCopy();
        if (fine > 0) member.addFine(fine);

        System.out.printf("↩️  Returned: '%s' by %s%n", book.getTitle(), member.getName());
        return fine;
    }

    // Search
    public List<Book> searchByTitle(String keyword) {
        return books.values().stream()
                .filter(b -> b.getTitle().toLowerCase().contains(keyword.toLowerCase()))
                .collect(Collectors.toList());
    }

    public List<Book> searchByAuthor(String author) {
        return books.values().stream()
                .filter(b -> b.getAuthor().toLowerCase().contains(author.toLowerCase()))
                .collect(Collectors.toList());
    }

    public List<Book> getAvailableBooks() {
        return books.values().stream()
                .filter(Book::isAvailable)
                .collect(Collectors.toList());
    }

    // Reports
    public void printOverdueReport() {
        System.out.println("\n⚠️  OVERDUE BOOKS REPORT");
        System.out.println("─".repeat(60));
        List<LoanRecord> overdue = allLoans.stream()
                .filter(LoanRecord::isOverdue)
                .collect(Collectors.toList());

        if (overdue.isEmpty()) {
            System.out.println("  No overdue loans. ✅");
        } else {
            overdue.forEach(l -> {
                LibraryMember m = members.get(l.getMemberId());
                Book b = books.get(l.getIsbn());
                System.out.printf("  %-20s | %-30s | Due: %s%n",
                        m != null ? m.getName() : "Unknown",
                        b != null ? b.getTitle() : "Unknown",
                        l.getDueDate().format(DateTimeFormatter.ofPattern("dd MMM yyyy")));
            });
        }
    }

    public void printCatalog() {
        System.out.println("\n📚 " + libraryName + " — CATALOG");
        System.out.println("─".repeat(80));
        books.values().forEach(b -> System.out.println("  " + b));
        System.out.println("─".repeat(80));
        System.out.println("  Total books: " + books.size());
    }

    public void printMembers() {
        System.out.println("\n👥 REGISTERED MEMBERS");
        System.out.println("─".repeat(70));
        members.values().forEach(m -> System.out.println("  " + m));
    }
}

// ============================
// Main Demo
// ============================
public class LibraryManagementSystem {
    public static void main(String[] args) {
        Library lib = new Library("BUET Central Library");

        // Add books
        System.out.println("=== Adding Books ===");
        lib.addBook(new Book("978-0-13-110362-7", "The C Programming Language",
                "Kernighan & Ritchie", "Programming", 3));
        lib.addBook(new Book("978-0-13-468599-1", "Clean Code",
                "Robert C. Martin", "Software Engineering", 2));
        lib.addBook(new Book("978-0-201-63361-0", "Design Patterns",
                "Gang of Four", "Software Engineering", 2));
        lib.addBook(new Book("978-0-13-235088-4", "Effective Java",
                "Joshua Bloch", "Java", 4));

        // Register members
        System.out.println("\n=== Registering Members ===");
        lib.registerMember(new StudentMember(
                "MEM-001", "Rafi Ahmed", "rafi@buet.ac.bd", "BUET", "1905001"));
        lib.registerMember(new FacultyMember(
                "MEM-002", "Dr. Sumaiya", "sumaiya@buet.ac.bd", "Professor", "CSE"));
        lib.registerMember(new PublicMember(
                "MEM-003", "Tanvir Hassan", "tanvir@gmail.com", "Dhaka"));

        // Issue books
        System.out.println("\n=== Issuing Books ===");
        lib.issueBook("MEM-001", "978-0-13-110362-7");
        lib.issueBook("MEM-001", "978-0-13-235088-4");
        lib.issueBook("MEM-002", "978-0-13-468599-1");
        lib.issueBook("MEM-002", "978-0-201-63361-0");

        // Search
        System.out.println("\n=== Search Results ===");
        System.out.println("Search 'Java':");
        lib.searchByTitle("java").forEach(b -> System.out.println("  → " + b));
        System.out.println("Search by 'Martin':");
        lib.searchByAuthor("martin").forEach(b -> System.out.println("  → " + b));

        // Return with fine simulation
        System.out.println("\n=== Returning Books ===");
        lib.returnBook("MEM-001", "978-0-13-110362-7");
        lib.returnBook("MEM-002", "978-0-13-468599-1");

        // Catalog & reports
        lib.printCatalog();
        lib.printMembers();
        lib.printOverdueReport();
    }
}
```

### Dry Run

```
issueBook("MEM-001", "978-0-13-110362-7")
  → member = "Rafi Ahmed" (StudentMember, max 3 books)
  → book = "The C Programming Language" (3 copies available)
  → member.canBorrow() → activeLoanRecords.size()(0) < 3 ✅
  → book.isAvailable() → availableCopies(3) > 0 ✅
  → book.checkOut() → availableCopies = 2
  → loanId = "LN-0001"
  → new LoanRecord("LN-0001", "MEM-001", "978-...")
    → issueDate = today, dueDate = today + 14
  → member.addLoanRecord(loan)
  → Output: "Issued: 'The C Programming Language' to Rafi Ahmed | Due: ..."

returnBook("MEM-001", "978-0-13-110362-7")
  → member.findActiveLoan("978-...") → LN-0001 (ACTIVE)
  → loan.processReturn()
    → returnDate = today
    → returnDate.isAfter(dueDate)? No (returned on time)
    → fine = 0
  → book.returnCopy() → availableCopies = 3
  → Output: "Returned: 'The C Programming Language' by Rafi Ahmed"
```

### Interview Explanation Strategy

> **"Library Management System এ আমি Strategy Pattern এর মতো approach নিয়েছি।**
>
> `LibraryMember` abstract — `getMaxBooksAllowed()`, `getLoanPeriodDays()`, `getMemberType()` abstract। Student: 3 books/14 days, Faculty: 10 books/30 days, Public: 2 books/7 days। **Polymorphism** দিয়ে same `issueBook()` method সব member type এর জন্য কাজ করে।
>
> `Library` class — **Composition** — `Map<String, Book>`, `Map<String, LibraryMember>`, `List<LoanRecord>` hold করে। Book ও Member আলাদাভাবে exist করতে পারে।
>
> **Encapsulation:** `Book.availableCopies` private — শুধু `checkOut()` ও `returnCopy()` দিয়ে change হয়। Fine calculation `LoanRecord` এর ভেতরেই — বাইরে logic নেই।"

---

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৪.৫ Coding Problem — Interview কৌশল (সব system এর জন্য)

### যে ধাপগুলো Interview এ follow করবেন

```
Step 1: Problem বুঝুন (2 মিনিট)
  → "এটি কি শুধু একটি demo নাকি production-ready?"
  → "কোন OOP concepts demonstrate করতে হবে?"
  → Requirements clarify করুন

Step 2: Design আগে বলুন (3 মিনিট)
  → "আমি প্রথমে classes identify করব"
  → Entities বলুন: Student, Course, Department
  → Relationships বলুন: "Student has-a Course list"
  → "এখানে Inheritance ব্যবহার করব কারণ..."

Step 3: Code লেখা শুরু করুন
  → Abstract class বা Interface আগে লিখুন
  → Concrete class একটি একটি করে
  → Main demo শেষে

Step 4: Code চলার পর explain করুন
  → "এখানে Polymorphism কাজ করছে কারণ..."
  → "এই method টি override করা হয়েছে..."
  → OOP pillars point out করুন

Step 5: Follow-up handle করুন
  → "আরো improve করতে হলে কী যোগ করতেন?"
  → "Exception handling add করতাম..."
  → "Database layer যোগ করতাম Repository pattern দিয়ে..."
```

### Common Coding Mistakes যা এড়াবেন

| ভুল | সঠিক পদ্ধতি |
|-----|------------|
| সব কিছু একটি class এ | SRP মেনে আলাদা class |
| Public fields | Private + getter/setter |
| No validation in setters | Boundary check, exception throw |
| No abstract class/interface | Hierarchy design করুন |
| Copy-paste code | Parent class এ common logic রাখুন |
| Magic numbers | Named constants (static final) |
| No error handling | IllegalArgumentException, NoSuchElementException |
| Return null | Optional বা Exception throw |

---

> **⚠️ PART 4 সম্পন্ন হয়েছে।**  
> পরবর্তী PART এর জন্য বলুন: **"PART 5 লিখুন"**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part5"></a>

# PART 5: Language-Specific OOP — Java, C++, Python, C\#

> **📍 এই PART এর Sections:** [৫.১ Java OOP](#৫১-java-oop--বিস্তারিত) · [৫.২ C++ OOP](#৫২-c-oop--java-এর-সাথে-তুলনা) · [৫.৩ Python OOP](#৫৩-python-oop--বৈশিষ্ট্য-ও-interview-traps) · [৫.৪ C# OOP](#৫৪-c-oop--java-এর-সাথে-তুলনা) · [৫.৫ Language তুলনা](#৫৫-language-তুলনা--quick-reference-table) · [৫.৬ BD Interview](#৫৬-bangladeshi-interview-তে-language-specific-প্রশ্ন)

> **ব্যবহারের নিয়ম:** প্রতিটি section এ নির্দিষ্ট ভাষার OOP বৈশিষ্ট্য, Java এর সাথে পার্থক্য, এবং interview trap গুলো মনোযোগ দিয়ে পড়ুন। Bangladeshi companies তে Java ও C++ সম্পর্কিত প্রশ্ন সবচেয়ে বেশি হয়।

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.১ Java OOP — বিস্তারিত

### Java OOP এর মূল বৈশিষ্ট্য

| বৈশিষ্ট্য | Java আচরণ |
|-----------|-----------|
| Memory management | Automatic (Garbage Collector) |
| Multiple Inheritance | Class দিয়ে নয়, শুধু Interface দিয়ে |
| Pointer | নেই — শুধু references |
| Default access modifier | `package-private` (কোনো keyword নেই) |
| Object parent | সব class `Object` extend করে implicitly |
| Method dispatch | Default-ই virtual (runtime polymorphism) |
| Constructor inheritance | হয় না — super() দিয়ে call করতে হয় |
| Destructor | নেই — `finalize()` deprecated |

---

### Java Runtime Polymorphism — বিস্তারিত

```java
// Java তে সব non-static, non-final, non-private method virtual
class Animal {
    public void sound() {
        System.out.println("Animal sound");
    }

    // এটি virtual নয় — override হয় না
    public static void staticMethod() {
        System.out.println("Animal static");
    }

    // এটি override হয় না — hide হয়
    private void privateMethod() {
        System.out.println("Animal private");
    }
}

class Dog extends Animal {
    @Override
    public void sound() {
        System.out.println("Woof!");  // Runtime এ এটি call হবে
    }

    // Method hiding — override নয়
    public static void staticMethod() {
        System.out.println("Dog static");
    }
}

public class PolymorphismDemo {
    public static void main(String[] args) {
        Animal a = new Dog();

        a.sound();         // "Woof!" — Runtime polymorphism ✅
        a.staticMethod();  // "Animal static" — Compile-time binding ❌ (no override)

        // Covariant return type (Java 5+)
        // Child method এর return type parent এর subtype হতে পারে
    }
}
```

---

### Java Interface — Default ও Static Methods (Java 8+)

```java
interface Printable {
    // Abstract method
    void print();

    // Default method — subclass override করতে পারে, না করলেও চলে
    default void printTwice() {
        print();
        print();
    }

    // Static method — interface name দিয়ে call করতে হয়
    static void info() {
        System.out.println("This is the Printable interface");
    }
}

interface Saveable {
    void save();

    default void backup() {
        System.out.println("Default backup");
    }
}

// Multiple interface implement করা — Diamond Problem সমাধান
class Document implements Printable, Saveable {
    @Override
    public void print() {
        System.out.println("Printing document...");
    }

    @Override
    public void save() {
        System.out.println("Saving document...");
    }

    // যদি দুটো interface এ একই default method থাকে, override বাধ্যতামূলক
    @Override
    public void backup() {
        Saveable.super.backup(); // কোন interface এর default চাই তা specify করা
    }
}

// Java 9+: Private methods in interface
interface Logger {
    default void log(String msg) {
        formatAndPrint(msg); // private helper call
    }

    private void formatAndPrint(String msg) {
        System.out.println("[LOG] " + msg);
    }
}
```

---

### Java এ Generics ও OOP

```java
// Generic class — Type-safe container
class Box<T> {
    private T value;

    public Box(T value) { this.value = value; }
    public T getValue()  { return value; }

    @Override
    public String toString() {
        return "Box[" + value + "]";
    }
}

// Bounded Type Parameter
class NumberBox<T extends Number> {
    private T value;
    public NumberBox(T v) { this.value = v; }

    public double doubleValue() {
        return value.doubleValue(); // Number এর method call করা যাচ্ছে
    }
}

// Wildcard
class Printer {
    // ? extends Number — read-only (upper bounded)
    public static void printNumbers(List<? extends Number> list) {
        list.forEach(System.out::println);
    }

    // ? super Integer — write-friendly (lower bounded)
    public static void addIntegers(List<? super Integer> list) {
        list.add(42);
    }
}
```

---

### Java Enum এ OOP

```java
// Java Enum — class এর মতো — method, constructor, field থাকতে পারে
enum Planet {
    MERCURY(3.303e+23, 2.4397e6),
    VENUS  (4.869e+24, 6.0518e6),
    EARTH  (5.976e+24, 6.37814e6);

    private final double mass;
    private final double radius;
    private static final double G = 6.67300E-11;

    Planet(double mass, double radius) {
        this.mass = mass;
        this.radius = radius;
    }

    public double surfaceGravity() {
        return G * mass / (radius * radius);
    }

    public double surfaceWeight(double otherMass) {
        return otherMass * surfaceGravity();
    }
}

// Abstract method in Enum — প্রতিটি constant override করে
enum Operation {
    PLUS  { @Override public double apply(double x, double y) { return x + y; } },
    MINUS { @Override public double apply(double x, double y) { return x - y; } },
    TIMES { @Override public double apply(double x, double y) { return x * y; } };

    public abstract double apply(double x, double y);
}
```

---

### Java OOP Interview Questions — সবচেয়ে জিজ্ঞেস করা

**Q: Java তে কেন multiple inheritance নেই?**
> Java তে class দিয়ে multiple inheritance নেই কারণ Diamond Problem। দুটো parent এ একই method থাকলে compiler কোনটি নেবে বুঝতে পারবে না — ambiguity। Interface দিয়ে multiple inheritance সম্ভব কারণ interface শুধু contract define করে, implementation নয়। Java 8 এর default method যদি conflict করে, child class অবশ্যই override করতে বাধ্য।

**Q: `String` immutable কেন?**
> ১. Security — String pool reuse করে, mutable হলে shared reference দিয়ে অন্যজন value বদলে দিতে পারত।
> ২. Thread-safe — Immutable object synchronization ছাড়াই multiple threads ব্যবহার করতে পারে।
> ৩. Hash consistency — HashMap key হিসেবে ব্যবহার হয়, hashCode stable থাকা দরকার।

**Q: `==` vs `.equals()` পার্থক্য?**
> `==` reference compare করে (stack এ address)। `.equals()` value compare করে (Object এ default `==`, String এ overridden)।
> ```java
> String a = new String("hello");
> String b = new String("hello");
> a == b       // false — different objects
> a.equals(b)  // true — same content
> ```

**Q: `final`, `finally`, `finalize` পার্থক্য?**
> - `final`: variable (reassign নয়), method (override নয়), class (extend নয়)
> - `finally`: try-catch-finally block — সবসময় execute হয়
> - `finalize()`: GC এর আগে call হয় (deprecated Java 9+, অবিশ্বস্ত)

**Q: `abstract class` vs `interface` কখন কোনটা?**
> `abstract class`: যখন shared state (fields) ও partial implementation দরকার। "Is-a" relationship।
> `interface`: যখন শুধু contract দরকার, multiple inheritance দরকার। "Can-do" (Capability) relationship।
> **Rule:** `interface` দিয়ে শুরু করুন। State দরকার হলে `abstract class`।

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.২ C++ OOP — Java এর সাথে তুলনা

### C++ vs Java মূল পার্থক্য

| বিষয় | C++ | Java |
|-------|-----|------|
| Memory | Manual (`new`/`delete`) | Automatic (GC) |
| Multiple Inheritance | Class দিয়েও সম্ভব | শুধু Interface দিয়ে |
| Pointer | আছে (`*`, `->`) | নেই (শুধু reference) |
| Virtual | Explicit `virtual` keyword লাগে | Default-ই virtual |
| Destructor | আছে (`~ClassName()`) | নেই (`finalize()` deprecated) |
| Operator Overloading | আছে | নেই (শুধু `+` String এ) |
| Templates | আছে (compile-time generics) | Generics আছে (runtime) |
| Header/Source | `.h` + `.cpp` আলাদা | একই `.java` file |
| Default access | `private` (class), `public` (struct) | `package-private` |
| Object creation | Stack বা Heap উভয়ই | শুধু Heap (`new`) |

---

### C++ Virtual Function ও Vtable — বিস্তারিত

```cpp
#include <iostream>
#include <string>
using namespace std;

class Shape {
public:
    // virtual না হলে runtime polymorphism হবে না
    virtual double area() const = 0;     // Pure virtual
    virtual string name() const = 0;

    // Non-virtual — always calls Shape's version
    void describe() const {
        // name() ও area() virtual — subclass এর version call হবে
        cout << name() << " has area: " << area() << endl;
    }

    virtual ~Shape() {  // Virtual destructor — বাধ্যতামূলক!
        cout << "Shape destructor" << endl;
    }
};

class Circle : public Shape {
private:
    double radius;
public:
    Circle(double r) : radius(r) {}

    double area() const override {
        return 3.14159 * radius * radius;
    }

    string name() const override { return "Circle"; }

    ~Circle() override {
        cout << "Circle destructor" << endl;
    }
};

class Rectangle : public Shape {
private:
    double width, height;
public:
    Rectangle(double w, double h) : width(w), height(h) {}

    double area() const override { return width * height; }
    string name() const override { return "Rectangle"; }

    ~Rectangle() override {
        cout << "Rectangle destructor" << endl;
    }
};

int main() {
    // Heap allocation — pointer to base class
    Shape* shapes[] = {
        new Circle(5.0),
        new Rectangle(4.0, 6.0)
    };

    for (Shape* s : shapes) {
        s->describe();  // Polymorphism — runtime dispatch via vtable
    }

    // Virtual destructor থাকায় সঠিক destructor call হবে
    for (Shape* s : shapes) {
        delete s;  // ~Circle() ও ~Rectangle() call হবে, তারপর ~Shape()
    }

    return 0;
}
```

**Output:**
```
Circle has area: 78.5397
Rectangle has area: 24
Circle destructor
Shape destructor
Rectangle destructor
Shape destructor
```

---

### C++ Memory Management ও OOP

```cpp
#include <iostream>
#include <memory>  // smart pointers
using namespace std;

class Resource {
private:
    int* data;
    int size;

public:
    // Constructor
    Resource(int size) : size(size) {
        data = new int[size];  // Heap allocation
        cout << "Resource allocated: " << size << " ints" << endl;
    }

    // ==========================================
    // Rule of Three (C++03) / Rule of Five (C++11)
    // ==========================================

    // 1. Destructor
    ~Resource() {
        delete[] data;
        cout << "Resource freed" << endl;
    }

    // 2. Copy Constructor — Deep copy
    Resource(const Resource& other) : size(other.size) {
        data = new int[size];
        copy(other.data, other.data + size, data);
        cout << "Resource copied" << endl;
    }

    // 3. Copy Assignment Operator
    Resource& operator=(const Resource& other) {
        if (this != &other) {  // Self-assignment check
            delete[] data;
            size = other.size;
            data = new int[size];
            copy(other.data, other.data + size, data);
        }
        return *this;
    }

    // 4. Move Constructor (C++11)
    Resource(Resource&& other) noexcept : data(other.data), size(other.size) {
        other.data = nullptr;  // Steal — source এ null set
        other.size = 0;
        cout << "Resource moved" << endl;
    }

    // 5. Move Assignment (C++11)
    Resource& operator=(Resource&& other) noexcept {
        if (this != &other) {
            delete[] data;
            data = other.data;
            size = other.size;
            other.data = nullptr;
            other.size = 0;
        }
        return *this;
    }

    void fill(int val) {
        for (int i = 0; i < size; i++) data[i] = val;
    }

    void print() const {
        for (int i = 0; i < size; i++) cout << data[i] << " ";
        cout << endl;
    }
};

// Smart pointers — modern C++ OOP
void smartPointerDemo() {
    // unique_ptr — single owner
    unique_ptr<Resource> r1 = make_unique<Resource>(5);
    r1->fill(10);
    r1->print();
    // r1 scope শেষে automatically delete হবে — no memory leak

    // shared_ptr — reference counting
    shared_ptr<Resource> r2 = make_shared<Resource>(3);
    shared_ptr<Resource> r3 = r2;  // ref count = 2
    r2->fill(20);
    // দুটো শেষ হলে তখন delete হবে

    // weak_ptr — circular reference ভাঙতে
    weak_ptr<Resource> r4 = r2;  // ref count বাড়ে না
}
```

---

### C++ Multiple Inheritance ও Diamond Problem

```cpp
class A {
public:
    virtual void hello() { cout << "Hello from A" << endl; }
    int x = 10;
};

class B : public A {
public:
    void hello() override { cout << "Hello from B" << endl; }
};

class C : public A {
public:
    void hello() override { cout << "Hello from C" << endl; }
};

// Diamond Problem — D তে A এর দুটো copy
class D_Bad : public B, public C {
    // D_Bad d;
    // d.hello(); → ERROR: ambiguous — B::hello or C::hello?
    // d.x       → ERROR: ambiguous — B::A::x or C::A::x?
};

// Virtual Inheritance — একটাই A
class B2 : virtual public A {};
class C2 : virtual public A {};

class D_Good : public B2, public C2 {
public:
    void hello() override {
        cout << "Hello from D_Good" << endl;
    }
};

int main() {
    D_Good d;
    d.hello();  // "Hello from D_Good" — no ambiguity
    d.x = 42;   // single A::x — no ambiguity
    return 0;
}
```

---

### C++ OOP Interview Questions

**Q: C++ এ `virtual` keyword কখন লাগে?**
> C++ এ method গুলো default-এ non-virtual (Java এর উল্টো)। Runtime polymorphism চাইলে base class এ `virtual` লিখতে হয়। Pure virtual (`= 0`) হলে abstract। `override` keyword (C++11) compile-time check নিশ্চিত করে।

**Q: Virtual destructor কখন বাধ্যতামূলক?**
> যখন base class pointer দিয়ে derived class object `delete` করা হয়। Virtual destructor না থাকলে শুধু base destructor call হয় — derived class এর memory leak হয়।

**Q: `new`/`delete` vs `malloc`/`free` পার্থক্য?**
> `new` constructor call করে, `delete` destructor call করে। `malloc`/`free` শুধু memory allocate/deallocate করে — constructor/destructor call হয় না। OOP এ সবসময় `new`/`delete` ব্যবহার করুন।

**Q: Stack vs Heap object — C++ এ পার্থক্য?**
> ```cpp
> MyClass obj;           // Stack — scope শেষে automatic destroy
> MyClass* p = new MyClass(); // Heap — explicit delete না করলে leak
> ```
> Stack faster। Heap lifetime control করা যায়।

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৩ Python OOP — বৈশিষ্ট্য ও Interview Traps

### Python OOP এর মূল বৈশিষ্ট্য

| বৈশিষ্ট্য | Python আচরণ |
|-----------|------------|
| Typing | Dynamic — runtime type check |
| Access modifier | Convention মাত্র (`_` protected, `__` private-like) |
| Multiple Inheritance | সরাসরি সম্ভব (MRO দিয়ে solve) |
| Abstract class | `abc` module — `@abstractmethod` |
| Interface | নেই নিজস্ব — ABC দিয়ে simulate |
| Constructor | `__init__()` |
| Destructor | `__del__()` (অবিশ্বস্ত) |
| Operator Overloading | Dunder methods (`__add__`, `__str__`, etc.) |
| Memory | Reference counting + cyclic GC |

---

### Python OOP Code

```python
from abc import ABC, abstractmethod
from typing import List, Optional

# ============================
# Abstract Base Class
# ============================
class Animal(ABC):
    def __init__(self, name: str, age: int):
        self._name = name   # Protected (convention)
        self.__age = age    # Name-mangled → _Animal__age (pseudo-private)

    @property
    def name(self) -> str:
        return self._name

    @property
    def age(self) -> int:
        return self.__age

    @age.setter
    def age(self, value: int):
        if value < 0:
            raise ValueError("Age cannot be negative.")
        self.__age = value

    @abstractmethod
    def sound(self) -> str:
        pass

    @abstractmethod
    def move(self) -> str:
        pass

    def describe(self) -> str:
        # Template method pattern
        return f"{self.name} says '{self.sound()}' and {self.move()}"

    def __str__(self) -> str:
        return f"{type(self).__name__}(name={self._name}, age={self.__age})"

    def __repr__(self) -> str:
        return self.__str__()

    def __eq__(self, other) -> bool:
        if not isinstance(other, Animal):
            return NotImplemented
        return self._name == other._name and self.__age == other.__age


# ============================
# Concrete Classes
# ============================
class Dog(Animal):
    def __init__(self, name: str, age: int, breed: str):
        super().__init__(name, age)
        self.breed = breed

    def sound(self) -> str: return "Woof"
    def move(self)  -> str: return "runs"

    def fetch(self, item: str) -> str:
        return f"{self._name} fetches the {item}!"


class Bird(Animal):
    def __init__(self, name: str, age: int, can_fly: bool = True):
        super().__init__(name, age)
        self.can_fly = can_fly

    def sound(self) -> str: return "Tweet"
    def move(self)  -> str: return "flies" if self.can_fly else "walks"


# ============================
# Multiple Inheritance + MRO
# ============================
class Flyable:
    def fly(self) -> str:
        return f"{self.__class__.__name__} is flying"

class Swimmable:
    def swim(self) -> str:
        return f"{self.__class__.__name__} is swimming"

class Duck(Animal, Flyable, Swimmable):
    def sound(self) -> str: return "Quack"
    def move(self)  -> str: return "waddles"

    def show_abilities(self):
        print(self.fly())
        print(self.swim())
        print(self.describe())


# ============================
# Class vs Static vs Instance Methods
# ============================
class Counter:
    _count = 0      # Class variable — shared

    def __init__(self, name: str):
        self.name = name        # Instance variable
        Counter._count += 1

    def greet(self) -> str:         # Instance method — self
        return f"Hi, I'm {self.name}"

    @classmethod
    def get_count(cls) -> int:      # Class method — cls
        return cls._count

    @staticmethod
    def validate_name(name: str) -> bool:   # Static — no self/cls
        return bool(name and name.strip())

    def __del__(self):
        Counter._count -= 1


# ============================
# Dunder (Magic) Methods
# ============================
class Vector:
    def __init__(self, x: float, y: float):
        self.x = x
        self.y = y

    def __add__(self, other: 'Vector') -> 'Vector':
        return Vector(self.x + other.x, self.y + other.y)

    def __sub__(self, other: 'Vector') -> 'Vector':
        return Vector(self.x - other.x, self.y - other.y)

    def __mul__(self, scalar: float) -> 'Vector':
        return Vector(self.x * scalar, self.y * scalar)

    def __abs__(self) -> float:         # len equivalent for math
        return (self.x**2 + self.y**2) ** 0.5

    def __eq__(self, other) -> bool:
        return self.x == other.x and self.y == other.y

    def __str__(self)  -> str: return f"Vector({self.x}, {self.y})"
    def __repr__(self) -> str: return self.__str__()

    def __len__(self)  -> int: return 2  # 2D vector has 2 components

    def __getitem__(self, index: int) -> float:
        if index == 0: return self.x
        if index == 1: return self.y
        raise IndexError("Vector index out of range")


# ============================
# Demo
# ============================
if __name__ == "__main__":
    dog = Dog("Rex", 3, "Labrador")
    bird = Bird("Tweety", 2)
    duck = Duck("Donald", 5)

    animals: List[Animal] = [dog, bird, duck]
    for a in animals:
        print(a.describe())   # Polymorphism

    print("\nMRO for Duck:", [cls.__name__ for cls in Duck.__mro__])

    v1 = Vector(3, 4)
    v2 = Vector(1, 2)
    print(f"\n{v1} + {v2} = {v1 + v2}")
    print(f"|{v1}| = {abs(v1)}")

    print(f"\nCounter count: {Counter.get_count()}")
    c1 = Counter("Alice")
    c2 = Counter("Bob")
    print(f"Counter count: {Counter.get_count()}")
```

---

### Python MRO (Method Resolution Order)

```
Duck.__mro__ = [Duck, Animal, Flyable, Swimmable, ABC, object]

যখন duck.method() call হয়:
  1. Duck এ খোঁজো
  2. না পেলে Animal এ
  3. না পেলে Flyable এ
  4. না পেলে Swimmable এ
  5. না পেলে ABC এ
  6. না পেলে object এ
  7. না পেলে AttributeError

C3 Linearization algorithm ব্যবহার করে Python MRO নির্ধারণ করে।
```

---

### Python OOP Interview Questions

**Q: Python এ `__init__` ও `__new__` পার্থক্য?**
> `__new__` object তৈরি করে (class এর instance allocate করে)। `__init__` তৈরি object initialize করে। সাধারণত `__new__` override করার দরকার নেই — Singleton বা immutable type (tuple subclass) এ ব্যবহার হয়।

**Q: Python এ private variable আসলে কতটা private?**
> Python এ সত্যিকারের private নেই। `__var` name mangling করে `_ClassName__var` হয়ে যায় — বাইরে থেকে `obj._ClassName__var` দিয়ে access করা যায়। এটা convention-based protection, enforced নয়।

**Q: `@property` কেন ব্যবহার করা হয়?**
> Encapsulation। Public field এর মতো syntax রেখে setter এ validation add করা যায়:
> ```python
> @age.setter
> def age(self, val):
>     if val < 0: raise ValueError("...")
>     self.__age = val
> ```
> Client code `obj.age = -1` করলে validation trigger হয়।

**Q: `isinstance()` vs `type()` পার্থক্য?**
> `type(obj) == MyClass` — শুধু exact type match। `isinstance(obj, MyClass)` — inheritance check করে।
> ```python
> isinstance(Dog("Rex", 3, "Lab"), Animal)  # True — Dog is-a Animal
> type(Dog("Rex", 3, "Lab")) == Animal      # False — type is Dog
> ```
> OOP এ সবসময় `isinstance()` ব্যবহার করুন।

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৪ C\# OOP — Java এর সাথে তুলনা

### C\# vs Java মূল পার্থক্য

| বৈশিষ্ট্য | C# | Java |
|----------|-----|------|
| Properties | Built-in `get`/`set` | Manual getter/setter method |
| Struct | Value type (stack) | নেই |
| Delegates/Events | Built-in | Functional Interface (Java 8) |
| `sealed` | Class extend করা বন্ধ | `final` |
| `override` | Explicit keyword বাধ্যতামূলক | `@Override` annotation (optional) |
| `virtual` | Explicit দরকার (Java এর মতো নয়) | Default-ই virtual |
| Extension Methods | আছে | নেই |
| LINQ | Built-in | Stream API |
| Nullable | `int?`, `string?` | `Optional<T>` |
| Access modifiers | `internal`, `protected internal` | `package-private` |

---

### C\# OOP Code

```csharp
using System;
using System.Collections.Generic;
using System.Linq;

// ============================
// Abstract Class
// ============================
public abstract class Shape {
    // Auto-implemented property (C# বৈশিষ্ট্য)
    public string Color { get; set; } = "White";
    public string Name  { get; protected set; }

    protected Shape(string name) {
        Name = name;
    }

    // Abstract methods
    public abstract double Area();
    public abstract double Perimeter();

    // Virtual method — override করা যাবে
    public virtual string Describe() {
        return $"{Name} | Color: {Color} | Area: {Area():F2} | Perimeter: {Perimeter():F2}";
    }

    // Sealed method — আর override করা যাবে না
    public sealed string GetType_Description() {
        return $"Type: {GetType().Name}";
    }

    public override string ToString() => Describe();
}

// ============================
// Concrete Classes
// ============================
public class Circle : Shape {
    public double Radius { get; private set; }

    public Circle(double radius) : base("Circle") {
        if (radius <= 0) throw new ArgumentException("Radius must be positive.");
        Radius = radius;
    }

    public override double Area()      => Math.PI * Radius * Radius;
    public override double Perimeter() => 2 * Math.PI * Radius;
}

public class Rectangle : Shape {
    public double Width  { get; private set; }
    public double Height { get; private set; }

    public Rectangle(double w, double h) : base("Rectangle") {
        Width = w; Height = h;
    }

    public override double Area()      => Width * Height;
    public override double Perimeter() => 2 * (Width + Height);

    // Method hiding দেখাতে new keyword
    public new string Describe() {
        return $"Rectangle {Width}x{Height}";
    }
}

// ============================
// Interface
// ============================
public interface IResizable {
    void Resize(double factor);
    double ScaledArea(double factor);
}

public interface IDrawable {
    void Draw();
}

// Multiple interface implement
public class Square : Shape, IResizable, IDrawable {
    public double Side { get; private set; }

    public Square(double side) : base("Square") {
        Side = side;
    }

    public override double Area()      => Side * Side;
    public override double Perimeter() => 4 * Side;

    public void Resize(double factor) {
        Side *= factor;
        Console.WriteLine($"Square resized. New side: {Side:F2}");
    }

    public double ScaledArea(double factor) => Area() * factor * factor;

    public void Draw() {
        Console.WriteLine($"Drawing a {Side}x{Side} square");
    }
}

// ============================
// Generic Class
// ============================
public class Repository<T> where T : class {
    private readonly List<T> _items = new();

    public void Add(T item)    => _items.Add(item);
    public bool Remove(T item) => _items.Remove(item);
    public IReadOnlyList<T> GetAll() => _items.AsReadOnly();
    public int Count => _items.Count;

    public IEnumerable<T> Where(Func<T, bool> predicate) =>
        _items.Where(predicate);
}

// ============================
// Extension Method (C# unique)
// ============================
public static class ShapeExtensions {
    // Shape class তে আলাদাভাবে method যোগ না করে extend করা
    public static bool IsLargerThan(this Shape shape, double threshold) {
        return shape.Area() > threshold;
    }

    public static string Summary(this Shape shape) {
        return $"[{shape.Name}] Area={shape.Area():F2}";
    }
}

// ============================
// Delegates ও Events
// ============================
public class ShapeEventArgs : EventArgs {
    public Shape Shape { get; }
    public ShapeEventArgs(Shape shape) { Shape = shape; }
}

public class ShapeManager {
    private readonly Repository<Shape> _repo = new();

    // Event declaration
    public event EventHandler<ShapeEventArgs>? ShapeAdded;
    public event EventHandler<ShapeEventArgs>? ShapeRemoved;

    public void AddShape(Shape shape) {
        _repo.Add(shape);
        ShapeAdded?.Invoke(this, new ShapeEventArgs(shape));  // Event fire
    }

    public Shape? GetLargest() {
        return _repo.GetAll().OrderByDescending(s => s.Area()).FirstOrDefault();
    }

    public void PrintAll() {
        foreach (var s in _repo.GetAll()) {
            Console.WriteLine("  " + s.Summary()); // Extension method
        }
    }
}

// ============================
// Main Demo
// ============================
class Program {
    static void Main() {
        var manager = new ShapeManager();

        // Event subscription (lambda)
        manager.ShapeAdded += (sender, e) =>
            Console.WriteLine($"✅ Added: {e.Shape.Name}");

        manager.AddShape(new Circle(5));
        manager.AddShape(new Rectangle(4, 6));
        var sq = new Square(7);
        manager.AddShape(sq);

        Console.WriteLine("\n--- All Shapes ---");
        manager.PrintAll();

        Console.WriteLine("\n--- Polymorphism ---");
        Shape[] shapes = { new Circle(3), new Rectangle(2, 5), new Square(4) };
        foreach (var s in shapes) {
            Console.WriteLine(s.Describe());  // Runtime polymorphism
            Console.WriteLine($"  Large? {s.IsLargerThan(20)}"); // Extension method
        }

        // IResizable polymorphism
        if (sq is IResizable resizable) {
            resizable.Resize(1.5);
        }

        var largest = manager.GetLargest();
        Console.WriteLine($"\nLargest shape: {largest?.Name} (Area: {largest?.Area():F2})");
    }
}
```

---

### C\# OOP Interview Questions

**Q: C# `property` ও Java getter/setter পার্থক্য?**
> C# property syntax clean ও concise:
> ```csharp
> public int Age { get; private set; }     // Auto-property
> public int Age {                          // Full property
>     get => _age;
>     set { if (value >= 0) _age = value; }
> }
> ```
> Java তে manually `getAge()`/`setAge()` method লিখতে হয়।

**Q: `virtual` + `override` কেন Java এর চেয়ে explicit?**
> C# এ method default non-virtual (C++ এর মতো)। `virtual` না দিলে override হয় না। `override` keyword বাধ্যতামূলক — accidental hiding এড়ানো যায়। `sealed override` করলে আর কেউ override করতে পারবে না।

**Q: `struct` vs `class` C# এ?**
> `struct` value type — stack এ থাকে, copy semantics। `class` reference type — heap এ, reference semantics।
> ```csharp
> struct Point { public int X, Y; }
> Point a = new Point { X=1, Y=2 };
> Point b = a;   // Copy — b আলাদা object
> b.X = 99;      // a.X এখনো 1
> ```

**Q: C# `delegate` ও Java functional interface পার্থক্য?**
> C# `delegate` type-safe function pointer। Java functional interface (`@FunctionalInterface`) lambda target হিসেবে ব্যবহার হয়। C# events built-in publisher-subscriber pattern delegate এর উপর ভিত্তি করে।

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৫ Language তুলনা — Quick Reference Table

### OOP Feature Comparison

| Feature | Java | C++ | Python | C# |
|---------|------|-----|--------|----|
| **Encapsulation** | `private`/`public`/`protected`/package | `private`/`public`/`protected` | Convention: `_`, `__` | `private`/`public`/`protected`/`internal` |
| **Inheritance** | Single (class), Multiple (interface) | Multiple (class) | Multiple (class) | Single (class), Multiple (interface) |
| **Polymorphism** | Default virtual | Explicit `virtual` | Default virtual | Explicit `virtual` |
| **Abstract Class** | `abstract class` | Pure virtual method | `ABC` + `@abstractmethod` | `abstract class` |
| **Interface** | `interface` | Pure abstract class | `ABC` (simulation) | `interface` |
| **Constructor** | Same name as class | Same name as class | `__init__()` | Same name as class |
| **Destructor** | No (GC) | `~ClassName()` | `__del__()` (unreliable) | `~ClassName()` (finalizer) |
| **Operator Overloading** | No (+ for String only) | Yes | Yes (dunder) | Yes |
| **Memory** | GC | Manual + Smart Ptr | Ref counting + GC | GC |
| **Generics** | Type erasure (runtime) | Templates (compile-time) | Duck typing | Reified (runtime) |
| **Properties** | Manual get/set | No built-in | `@property` | Built-in `{ get; set; }` |
| **Extension Methods** | No | No | No (monkey-patch) | Yes |
| **Null Safety** | `Optional<T>` | Pointer (can be null) | `Optional` / `None` check | Nullable `?`, `??` |

---

### Common Interview Trap — Language Mixing

**ভুল ধারণা যা interview এ হয়:**

| ভুল বলা | সঠিক উত্তর |
|---------|-----------|
| "Java তেও virtual লাগে" | Java তে default-ই virtual — explicitly লাগে না |
| "Python এ private আছে" | Name mangling আছে, true private নেই |
| "C++ এ GC আছে" | নেই — manual / smart pointer |
| "C# এ Java এর মতো" | C# এ virtual explicit, property built-in, struct আছে |
| "Interface এ code থাকে না" | Java 8+ default method, C# default interface method আছে |
| "Python multiple inheritance নেই" | আছে — MRO (C3 linearization) দিয়ে resolve হয় |

---

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৫.৬ Bangladeshi Interview তে Language-Specific প্রশ্ন

### Java Focus (সবচেয়ে বেশি)

```
প্রশ্ন ১: Java তে String immutable কেন?
প্রশ্ন ২: equals() vs hashCode() contract কী?
প্রশ্ন ৩: ArrayList vs LinkedList — OOP perspective
প্রশ্ন ৪: try-with-resources কীভাবে কাজ করে? (AutoCloseable interface)
প্রশ্ন ৫: Lambda expression কোন interface implement করে?
প্রশ্ন ৬: Stream কি OOP নাকি Functional?
প্রশ্ন ৭: Comparable vs Comparator interface পার্থক্য?
প্রশ্ন ৮: HashMap কীভাবে hashCode/equals ব্যবহার করে?
```

### Java equals/hashCode Contract

```java
public class Student {
    private String rollNumber;
    private String name;

    public Student(String roll, String name) {
        this.rollNumber = roll;
        this.name = name;
    }

    // Contract: যদি a.equals(b) == true → a.hashCode() == b.hashCode()
    // Reverse true নয়: same hashCode মানে equals নয় (collision হতে পারে)

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;       // Same reference
        if (obj == null) return false;
        if (getClass() != obj.getClass()) return false;
        Student other = (Student) obj;
        return Objects.equals(rollNumber, other.rollNumber);
    }

    @Override
    public int hashCode() {
        return Objects.hash(rollNumber);   // Same field as equals
    }
}

// Comparable — natural ordering (class নিজেই implement করে)
class StudentComparable implements Comparable<StudentComparable> {
    private double cgpa;

    @Override
    public int compareTo(StudentComparable other) {
        return Double.compare(other.cgpa, this.cgpa); // Descending
    }
}

// Comparator — external/custom ordering (আলাদা class বা lambda)
Comparator<Student> byName = Comparator.comparing(s -> s.name);
Comparator<Student> byRoll = Comparator.comparing(s -> s.rollNumber);

List<Student> students = new ArrayList<>();
students.sort(byName.thenComparing(byRoll));
```

### C++ Focus (বিশেষত embedded/system companies)

```
প্রশ্ন ১: vtable কী? কখন তৈরি হয়?
প্রশ্ন ২: virtual destructor না থাকলে কী সমস্যা?
প্রশ্ন ৩: copy constructor এবং copy assignment operator এর পার্থক্য?
প্রশ্ন ৪: Rule of Three কী? Rule of Five?
প্রশ্ন ৫: unique_ptr vs shared_ptr পার্থক্য?
প্রশ্ন ৬: const member function কী?
প্রশ্ন ৭: friend function কেন ব্যবহার করা হয়? এটা encapsulation ভাঙে?
```

### C++ const member function

```cpp
class Circle {
private:
    double radius;
public:
    Circle(double r) : radius(r) {}

    // const member function — object কে modify করবে না
    double area() const {
        return 3.14159 * radius * radius;
        // radius = 5; // ERROR — const function এ modify করা যাবে না
    }

    // Non-const — object modify করতে পারে
    void setRadius(double r) { radius = r; }
};

void printArea(const Circle& c) {
    cout << c.area() << endl;  // OK — area() is const
    // c.setRadius(5);          // ERROR — const reference এ non-const call নয়
}
```

---

> **⚠️ PART 5 সম্পন্ন হয়েছে।**  
> পরবর্তী PART এর জন্য বলুন: **"PART 6 লিখুন"**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part6"></a>

# PART 6: Advanced OOP Topics — Memory, Design Patterns, GC, Architecture

> **📍 এই PART এর Sections:** [৬.১ Memory Management](#৬১-memory-management--stack-vs-heap) · [৬.২ Garbage Collection](#৬২-garbage-collection--java) · [৬.৩ Design Patterns (GoF)](#৬৩-design-patterns--gang-of-four-gof) · [৬.৪ MVC Architecture](#৬৪-mvc-architecture--oop-দিয়ে) · [৬.৫ Object Cloning](#৬৫-object-cloning--shallow-vs-deep-copy-revisited) · [৬.৬ Exception Handling](#৬৬-exception-handling-ও-oop) · [৬.৭ Advanced Interview Qs](#৬৭-advanced-oop-interview-questions)

> **ব্যবহারের নিয়ম:** এই part টি senior-level প্রশ্নের জন্য। Freshers যদি এগুলো জানেন, interview এ অনেক এগিয়ে থাকবেন। প্রতিটি section মনোযোগ দিয়ে পড়ুন এবং code নিজে লিখে দেখুন।

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.১ Memory Management — Stack vs Heap

### Stack ও Heap — মূল পার্থক্য

```
┌─────────────────────────────────────────────────────────────┐
│                        MEMORY LAYOUT                        │
├──────────────────────────┬──────────────────────────────────┤
│          STACK           │             HEAP                 │
├──────────────────────────┼──────────────────────────────────┤
│ LIFO (Last In First Out) │ Dynamic, unordered               │
│ Fixed size (usually 1-8MB)│ Large (limited by RAM)          │
│ Auto-managed             │ Manual (C++) / GC (Java/Python)  │
│ Very fast (CPU register) │ Slower (malloc/new)              │
│ Local variables          │ Objects created with new         │
│ Method call frames       │ Long-lived data                  │
│ Primitive types (Java)   │ All objects (Java)               │
│ Stack overflow possible  │ OutOfMemoryError possible        │
└──────────────────────────┴──────────────────────────────────┘
```

### Java Memory Layout — বিস্তারিত

```
JVM Memory Structure:
┌─────────────────────────────────────────────────────────────┐
│                         JVM MEMORY                          │
├──────────────┬──────────────────────────────────────────────┤
│   STACK      │                  HEAP                        │
│  (per thread)│  ┌───────────────┬────────────────────────┐  │
│              │  │  Young Gen    │      Old Gen            │  │
│ frame1:      │  │ ┌───┬───────┐ │                        │  │
│  local vars  │  │ │E0 │Survivor│ │   Long-lived objects  │  │
│  operands    │  │ │   │ S0, S1 │ │   (survived GC)       │  │
│ frame2:      │  │ └───┴───────┘ │                        │  │
│  ...         │  └───────────────┴────────────────────────┘  │
│              │                                              │
│   METHOD     │  ┌─────────────────────────────────────────┐ │
│   AREA       │  │          METASPACE (Java 8+)            │ │
│              │  │  Class metadata, static fields, methods │ │
└──────────────┴──┴─────────────────────────────────────────┴─┘
```

### Java তে Object Lifecycle

```java
public class ObjectLifecycle {

    static int instanceCount = 0;  // Metaspace (static)

    private String name;            // Heap (instance field)
    private int[] data;             // Heap (array reference)

    public ObjectLifecycle(String name, int size) {
        this.name = name;
        this.data = new int[size];  // Separate heap allocation
        instanceCount++;
        System.out.println("Created: " + name);
    }

    public static void demonstrateMemory() {
        // Stack এ reference variable, Heap এ object
        ObjectLifecycle obj1 = new ObjectLifecycle("A", 100);
        // Stack: obj1 → Heap address 0x1A2B
        // Heap: ObjectLifecycle object with name="A", data=[...]

        ObjectLifecycle obj2 = obj1;
        // Stack: obj2 → same Heap address 0x1A2B
        // Heap: SAME object — not a copy!

        obj2.name = "B";
        System.out.println(obj1.name); // "B" — same object!

        // Primitive — Stack এ value সরাসরি
        int x = 10;     // Stack: x=10
        int y = x;      // Stack: y=10 (copy)
        y = 20;
        System.out.println(x); // 10 — আলাদা

        // Method এ pass করলে:
        modifyPrimitive(x);    // x changed → only local copy
        modifyObject(obj1);    // obj1 changed → same heap object
    }

    static void modifyPrimitive(int val) {
        val = 999; // Only local stack copy changed
    }

    static void modifyObject(ObjectLifecycle obj) {
        obj.name = "Modified"; // Heap object changed!
    }

    // Object lifecycle ends when no references point to it
    // GC marks it for collection
    @Override
    protected void finalize() {
        // Deprecated in Java 9 — don't rely on this
        System.out.println("GC collecting: " + name);
        instanceCount--;
    }
}
```

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.২ Garbage Collection — Java

### GC Algorithms Overview

```
Mark and Sweep:
  Phase 1 — Mark: GC root থেকে reachable সব object mark করো
  Phase 2 — Sweep: unmarked object মুছে ফেলো
  Phase 3 — Compact (optional): memory defragment করো

Generational GC (Java default):
  Young Generation:
    Eden Space → নতুন object জন্মায় এখানে
    Survivor S0, S1 → Minor GC তে জীবিতরা যায়
  
  Old Generation (Tenured):
    বহুবার Survivor পার করে জীবিত object এখানে যায়
    Major GC (Full GC) এখানে হয় — ব্যয়বহুল

  Metaspace:
    Class metadata — কখনো GC হয় না (explicitly unload ছাড়া)
```

### Memory Leak — Java তে কীভাবে হয়?

```java
import java.util.*;

public class MemoryLeakExamples {

    // ========================================
    // Memory Leak Example 1: Static Collection
    // ========================================
    private static final List<Object> CACHE = new ArrayList<>();

    public static void addToCache(Object obj) {
        CACHE.add(obj);
        // ❌ কখনো clear হয় না — objects accumulate হতে থাকে
    }

    // Fix: WeakReference বা explicit clear
    private static final Map<String, WeakReference<Object>> WEAK_CACHE = new HashMap<>();

    public static void addToWeakCache(String key, Object obj) {
        WEAK_CACHE.put(key, new WeakReference<>(obj));
        // ✅ GC চাইলে reclaim করতে পারে
    }

    // ========================================
    // Memory Leak Example 2: Listener not removed
    // ========================================
    interface EventListener { void onEvent(String event); }

    static List<EventListener> listeners = new ArrayList<>();

    public static void registerListener(EventListener l) {
        listeners.add(l);
        // ❌ Listener deregister না করলে object কখনো GC হবে না
    }

    public static void removeListener(EventListener l) {
        listeners.remove(l); // ✅ Always deregister
    }

    // ========================================
    // Memory Leak Example 3: Inner class
    // ========================================
    class Inner {
        // ❌ Non-static inner class implicitly holds reference to outer class
        // Outer class GC হতে পারবে না যতক্ষণ Inner জীবিত
    }

    static class StaticNested {
        // ✅ Static nested class — outer reference নেই
    }

    // ========================================
    // try-with-resources — resource leak fix
    // ========================================
    public static void properResourceHandling(String filename) {
        // AutoCloseable implement করা যেকোনো resource এভাবে handle করুন
        try (var reader = new java.io.BufferedReader(new java.io.FileReader(filename))) {
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (java.io.IOException e) {
            System.err.println("Error: " + e.getMessage());
        }
        // ✅ reader.close() automatically called — no leak
    }
}
```

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৩ Design Patterns — Gang of Four (GoF)

> Design Pattern হলো commonly occurring problem এর proven solution template। OOP interview এ এই pattern গুলো জানা অত্যন্ গুরুত্বপূর্ণ।

### Pattern Categories

```
Creational Patterns  — Object কীভাবে তৈরি হবে
  ├── Singleton     — একটিমাত্র instance
  ├── Factory       — Object তৈরির responsibility আলাদা করা
  ├── Abstract Factory — Related objects এর family তৈরি
  ├── Builder       — Complex object step-by-step তৈরি
  └── Prototype     — Existing object copy করে নতুন তৈরি

Structural Patterns  — Class/Object কীভাবে compose হবে
  ├── Adapter       — Incompatible interface compatible করা
  ├── Decorator     — Runtime এ behavior যোগ করা
  ├── Facade        — Complex subsystem simple interface দেওয়া
  ├── Composite     — Tree structure (part-whole hierarchy)
  └── Proxy         — Object এর surrogate/placeholder

Behavioral Patterns  — Object interaction ও responsibility
  ├── Observer      — One-to-many notification
  ├── Strategy      — Algorithm family, interchangeable
  ├── Template Method— Skeleton fixed, steps override করা যায়
  ├── Command       — Request encapsulate করা
  └── Iterator      — Collection traverse করা
```

---

### Singleton Pattern

```java
// Thread-safe Singleton — Double-checked locking
public class DatabaseConnection {
    // volatile — ensures visibility across threads
    private static volatile DatabaseConnection instance = null;
    private String connectionString;
    private int activeConnections = 0;

    // Private constructor — বাইরে থেকে new করা যাবে না
    private DatabaseConnection() {
        this.connectionString = "jdbc:mysql://localhost:3306/mydb";
        System.out.println("Database connection established.");
    }

    // Thread-safe getInstance
    public static DatabaseConnection getInstance() {
        if (instance == null) {                    // First check (no lock)
            synchronized (DatabaseConnection.class) {
                if (instance == null) {            // Second check (with lock)
                    instance = new DatabaseConnection();
                }
            }
        }
        return instance;
    }

    public void query(String sql) {
        activeConnections++;
        System.out.println("Executing: " + sql + " [connections: " + activeConnections + "]");
        activeConnections--;
    }

    public String getConnectionString() { return connectionString; }
}

// Enum Singleton — সবচেয়ে safe (Joshua Bloch recommended)
public enum AppConfig {
    INSTANCE;

    private String appName    = "MyApp";
    private String version    = "1.0.0";
    private int    maxThreads = 10;

    public String getAppName()    { return appName; }
    public String getVersion()    { return version; }
    public int    getMaxThreads() { return maxThreads; }
    public void   setMaxThreads(int n) { this.maxThreads = n; }
}

// Usage:
// DatabaseConnection.getInstance().query("SELECT * FROM users");
// AppConfig.INSTANCE.getAppName();
```

**Interview এ বলুন:**
> "Singleton এ double-checked locking ব্যবহার করি thread safety এর জন্য। `volatile` keyword JVM instruction reordering prevent করে। কিন্তু আমি prefer করি Enum Singleton — serialization ও reflection attack থেকে safe।"

---

### Factory Method Pattern

```java
// Product hierarchy
abstract class Notification {
    protected String recipient;
    protected String message;

    public Notification(String recipient, String message) {
        this.recipient = recipient;
        this.message = message;
    }

    public abstract void send();
    public abstract String getType();

    @Override
    public String toString() {
        return String.format("[%s] To: %s | Msg: %s", getType(), recipient, message);
    }
}

class EmailNotification extends Notification {
    private String subject;

    public EmailNotification(String email, String subject, String body) {
        super(email, body);
        this.subject = subject;
    }

    @Override
    public void send() {
        System.out.println("📧 EMAIL to " + recipient
                + " | Subject: " + subject + " | Body: " + message);
    }

    @Override
    public String getType() { return "EMAIL"; }
}

class SMSNotification extends Notification {
    public SMSNotification(String phone, String text) {
        super(phone, text);
    }

    @Override
    public void send() {
        System.out.println("📱 SMS to " + recipient + ": " + message);
    }

    @Override
    public String getType() { return "SMS"; }
}

class PushNotification extends Notification {
    private String deviceToken;

    public PushNotification(String deviceToken, String title, String body) {
        super(deviceToken, body);
        this.deviceToken = deviceToken;
    }

    @Override
    public void send() {
        System.out.println("🔔 PUSH to device " + deviceToken
                + " | " + recipient + ": " + message);
    }

    @Override
    public String getType() { return "PUSH"; }
}

// Factory — object তৈরির responsibility এক জায়গায়
public class NotificationFactory {
    public enum Channel { EMAIL, SMS, PUSH }

    // Static factory method
    public static Notification create(Channel channel,
                                       String recipient, String message) {
        return switch (channel) {
            case EMAIL -> new EmailNotification(recipient, "Notification", message);
            case SMS   -> new SMSNotification(recipient, message);
            case PUSH  -> new PushNotification(recipient, "Alert", message);
        };
    }

    // Factory method with configuration
    public static List<Notification> createBulk(List<String> recipients,
                                                  Channel channel, String message) {
        List<Notification> notifications = new ArrayList<>();
        for (String r : recipients) {
            notifications.add(create(channel, r, message));
        }
        return notifications;
    }
}

// Usage:
// Notification n = NotificationFactory.create(Channel.EMAIL, "user@test.com", "Hello!");
// n.send();
```

**Interview এ বলুন:**
> "Factory Pattern এ client `new` ব্যবহার করে না — factory কে বলে 'আমাকে একটি Notification দাও'। নতুন type যোগ করতে শুধু factory তে একটি case যোগ করতে হয় — client code change হয় না। এটি OCP (Open-Closed Principle) enforce করে।"

---

### Observer Pattern

```java
import java.util.*;

// Event data class
class StockPriceEvent {
    private final String symbol;
    private final double oldPrice;
    private final double newPrice;
    private final java.time.LocalDateTime timestamp;

    public StockPriceEvent(String symbol, double oldPrice, double newPrice) {
        this.symbol   = symbol;
        this.oldPrice = oldPrice;
        this.newPrice = newPrice;
        this.timestamp = java.time.LocalDateTime.now();
    }

    public String getSymbol()   { return symbol; }
    public double getOldPrice() { return oldPrice; }
    public double getNewPrice() { return newPrice; }
    public double getChange()   { return newPrice - oldPrice; }
    public double getChangePct(){ return (getChange() / oldPrice) * 100; }

    @Override
    public String toString() {
        return String.format("[%s] %.2f → %.2f (%+.2f%%)",
                symbol, oldPrice, newPrice, getChangePct());
    }
}

// Observer interface
interface StockObserver {
    void onPriceChanged(StockPriceEvent event);
    String getObserverName();
}

// Subject interface
interface StockSubject {
    void subscribe(StockObserver observer);
    void unsubscribe(StockObserver observer);
    void notifyObservers(StockPriceEvent event);
}

// Concrete Subject
class StockMarket implements StockSubject {
    private final Map<String, Double> prices = new HashMap<>();
    private final List<StockObserver> observers = new ArrayList<>();

    @Override
    public void subscribe(StockObserver observer) {
        if (!observers.contains(observer)) {
            observers.add(observer);
            System.out.println("✅ Subscribed: " + observer.getObserverName());
        }
    }

    @Override
    public void unsubscribe(StockObserver observer) {
        observers.remove(observer);
        System.out.println("❌ Unsubscribed: " + observer.getObserverName());
    }

    @Override
    public void notifyObservers(StockPriceEvent event) {
        // All observers notify করা — Polymorphism
        observers.forEach(o -> o.onPriceChanged(event));
    }

    public void updatePrice(String symbol, double newPrice) {
        double oldPrice = prices.getOrDefault(symbol, newPrice);
        prices.put(symbol, newPrice);
        if (oldPrice != newPrice) {
            notifyObservers(new StockPriceEvent(symbol, oldPrice, newPrice));
        }
    }

    public double getPrice(String symbol) {
        return prices.getOrDefault(symbol, 0.0);
    }
}

// Concrete Observers
class AlertObserver implements StockObserver {
    private final String name;
    private final double threshold; // % change to trigger alert

    public AlertObserver(String name, double threshold) {
        this.name = name;
        this.threshold = threshold;
    }

    @Override
    public void onPriceChanged(StockPriceEvent event) {
        if (Math.abs(event.getChangePct()) >= threshold) {
            System.out.printf("🚨 ALERT [%s]: %s — Significant move: %+.2f%%%n",
                    name, event, event.getChangePct());
        }
    }

    @Override
    public String getObserverName() { return "AlertObserver[" + name + "]"; }
}

class PortfolioObserver implements StockObserver {
    private final String ownerName;
    private final Map<String, Integer> holdings = new HashMap<>(); // symbol → shares

    public PortfolioObserver(String owner) { this.ownerName = owner; }

    public void addHolding(String symbol, int shares) {
        holdings.put(symbol, shares);
    }

    @Override
    public void onPriceChanged(StockPriceEvent event) {
        Integer shares = holdings.get(event.getSymbol());
        if (shares != null) {
            double pnl = event.getChange() * shares;
            System.out.printf("💼 Portfolio [%s]: %s | Shares: %d | P&L: %+.2f BDT%n",
                    ownerName, event, shares, pnl);
        }
    }

    @Override
    public String getObserverName() { return "Portfolio[" + ownerName + "]"; }
}

class LoggerObserver implements StockObserver {
    private final List<String> log = new ArrayList<>();

    @Override
    public void onPriceChanged(StockPriceEvent event) {
        String entry = java.time.LocalDateTime.now() + " | " + event;
        log.add(entry);
        System.out.println("📝 LOG: " + entry);
    }

    @Override
    public String getObserverName() { return "Logger"; }

    public List<String> getLog() { return Collections.unmodifiableList(log); }
}

// Demo
class StockMarketDemo {
    public static void main(String[] args) {
        StockMarket market = new StockMarket();

        // Observers
        AlertObserver     alert     = new AlertObserver("MainAlert", 2.0);
        PortfolioObserver rafiPort  = new PortfolioObserver("Rafi");
        LoggerObserver    logger    = new LoggerObserver();

        rafiPort.addHolding("GRAMEENPHONE", 100);
        rafiPort.addHolding("BRAC BANK", 50);

        // Subscribe
        market.subscribe(alert);
        market.subscribe(rafiPort);
        market.subscribe(logger);

        // Price updates — all observers notified
        System.out.println("\n=== Market Updates ===");
        market.updatePrice("GRAMEENPHONE", 350.00);
        market.updatePrice("GRAMEENPHONE", 362.50);  // +3.6% — triggers alert
        market.updatePrice("BRAC BANK", 45.00);
        market.updatePrice("BRAC BANK", 43.20);      // -4% — triggers alert

        // Unsubscribe
        market.unsubscribe(logger);
        market.updatePrice("GRAMEENPHONE", 360.00);  // Logger won't receive this
    }
}
```

**Interview এ বলুন:**
> "Observer Pattern এ StockMarket হলো Subject — `List<StockObserver>` maintain করে। Price change হলে সব observer কে `onPriceChanged()` call দিয়ে notify করে। Observer গুলো আলাদা — Alert, Portfolio, Logger — কিন্তু same interface implement করে। **Loose coupling** — Market জানে না observer কী করছে, observer জানে না কীভাবে notify হচ্ছে।"

---

### Strategy Pattern

```java
// Strategy Interface
interface SortStrategy {
    void sort(int[] array);
    String getName();
}

// Concrete Strategies
class BubbleSort implements SortStrategy {
    @Override
    public void sort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j]; arr[j] = arr[j + 1]; arr[j + 1] = temp;
                }
            }
        }
    }

    @Override
    public String getName() { return "Bubble Sort O(n²)"; }
}

class MergeSort implements SortStrategy {
    @Override
    public void sort(int[] arr) {
        if (arr.length <= 1) return;
        mergeSort(arr, 0, arr.length - 1);
    }

    private void mergeSort(int[] arr, int left, int right) {
        if (left < right) {
            int mid = (left + right) / 2;
            mergeSort(arr, left, mid);
            mergeSort(arr, mid + 1, right);
            merge(arr, left, mid, right);
        }
    }

    private void merge(int[] arr, int left, int mid, int right) {
        int n1 = mid - left + 1, n2 = right - mid;
        int[] L = Arrays.copyOfRange(arr, left, mid + 1);
        int[] R = Arrays.copyOfRange(arr, mid + 1, right + 1);
        int i = 0, j = 0, k = left;
        while (i < n1 && j < n2)
            arr[k++] = (L[i] <= R[j]) ? L[i++] : R[j++];
        while (i < n1) arr[k++] = L[i++];
        while (j < n2) arr[k++] = R[j++];
    }

    @Override
    public String getName() { return "Merge Sort O(n log n)"; }
}

// Context — uses strategy
class DataSorter {
    private SortStrategy strategy;

    public DataSorter(SortStrategy strategy) {
        this.strategy = strategy;
    }

    // Strategy swap at runtime
    public void setStrategy(SortStrategy strategy) {
        System.out.println("Strategy changed to: " + strategy.getName());
        this.strategy = strategy;
    }

    public int[] sort(int[] data) {
        int[] copy = Arrays.copyOf(data, data.length);
        long start = System.nanoTime();
        strategy.sort(copy);
        long elapsed = System.nanoTime() - start;
        System.out.printf("Sorted with %s in %d ns%n", strategy.getName(), elapsed);
        return copy;
    }
}

// Usage
class StrategyDemo {
    public static void main(String[] args) {
        int[] data = {64, 34, 25, 12, 22, 11, 90};

        DataSorter sorter = new DataSorter(new BubbleSort());
        sorter.sort(data);

        // Runtime strategy swap
        sorter.setStrategy(new MergeSort());
        sorter.sort(data);

        // Lambda as strategy (Java 8+)
        SortStrategy javaBuiltIn = arr -> Arrays.sort(arr);
        sorter.setStrategy(new SortStrategy() {
            public void sort(int[] arr) { Arrays.sort(arr); }
            public String getName()     { return "Java Built-in"; }
        });
        sorter.sort(data);
    }
}
```

---

### Builder Pattern

```java
// Builder Pattern — Complex object construction
public class HttpRequest {
    // Required fields
    private final String url;
    private final String method;

    // Optional fields
    private final Map<String, String> headers;
    private final String body;
    private final int timeoutSeconds;
    private final boolean followRedirects;
    private final String authToken;

    // Private constructor — only Builder can create
    private HttpRequest(Builder builder) {
        this.url             = builder.url;
        this.method          = builder.method;
        this.headers         = Collections.unmodifiableMap(
                                    new HashMap<>(builder.headers));
        this.body            = builder.body;
        this.timeoutSeconds  = builder.timeoutSeconds;
        this.followRedirects = builder.followRedirects;
        this.authToken       = builder.authToken;
    }

    // Static nested Builder class
    public static class Builder {
        // Required
        private final String url;
        private final String method;

        // Optional with defaults
        private Map<String, String> headers = new HashMap<>();
        private String body            = null;
        private int    timeoutSeconds  = 30;
        private boolean followRedirects = true;
        private String authToken       = null;

        public Builder(String url, String method) {
            if (url == null || url.trim().isEmpty())
                throw new IllegalArgumentException("URL is required.");
            this.url    = url.trim();
            this.method = method.toUpperCase();
        }

        public Builder header(String name, String value) {
            this.headers.put(name, value);
            return this; // method chaining
        }

        public Builder body(String body) {
            this.body = body;
            return this;
        }

        public Builder timeout(int seconds) {
            if (seconds <= 0) throw new IllegalArgumentException("Timeout must be positive.");
            this.timeoutSeconds = seconds;
            return this;
        }

        public Builder noRedirects() {
            this.followRedirects = false;
            return this;
        }

        public Builder bearerToken(String token) {
            this.authToken = token;
            this.headers.put("Authorization", "Bearer " + token);
            return this;
        }

        public HttpRequest build() {
            // Cross-field validation
            if ("POST".equals(method) || "PUT".equals(method)) {
                if (body == null)
                    System.out.println("⚠️  Warning: POST/PUT without body.");
            }
            return new HttpRequest(this);
        }
    }

    @Override
    public String toString() {
        return String.format("HttpRequest{method=%s, url=%s, timeout=%ds, headers=%s}",
                method, url, timeoutSeconds, headers);
    }
}

// Clean usage — method chaining
class BuilderDemo {
    public static void main(String[] args) {
        HttpRequest request = new HttpRequest.Builder(
                "https://api.example.com/users", "POST")
            .header("Content-Type", "application/json")
            .header("Accept", "application/json")
            .bearerToken("eyJhbGciOiJIUzI1NiJ9...")
            .body("{\"name\": \"Rafi\", \"email\": \"rafi@test.com\"}")
            .timeout(60)
            .build();

        System.out.println(request);
    }
}
```

**Interview এ বলুন:**
> "Builder Pattern constructor telescoping এর সমস্যা সমাধান করে। অনেক optional parameter থাকলে constructor overload অনেক হয়ে যায়। Builder দিয়ে method chaining এ শুধু দরকারী fields set করা যায়, object immutable রাখা যায়, cross-field validation build() এ একবার হয়।"

---

### Decorator Pattern

```java
// Component interface
interface TextProcessor {
    String process(String text);
}

// Concrete component
class PlainText implements TextProcessor {
    @Override
    public String process(String text) { return text; }
}

// Abstract Decorator
abstract class TextDecorator implements TextProcessor {
    protected final TextProcessor wrapped;

    public TextDecorator(TextProcessor processor) {
        this.wrapped = processor;
    }

    @Override
    public String process(String text) {
        return wrapped.process(text); // Delegate to wrapped
    }
}

// Concrete Decorators
class UpperCaseDecorator extends TextDecorator {
    public UpperCaseDecorator(TextProcessor p) { super(p); }

    @Override
    public String process(String text) {
        return super.process(text).toUpperCase();
    }
}

class TrimDecorator extends TextDecorator {
    public TrimDecorator(TextProcessor p) { super(p); }

    @Override
    public String process(String text) {
        return super.process(text).trim();
    }
}

class HtmlEscapeDecorator extends TextDecorator {
    public HtmlEscapeDecorator(TextProcessor p) { super(p); }

    @Override
    public String process(String text) {
        return super.process(text)
                .replace("&", "&amp;")
                .replace("<", "&lt;")
                .replace(">", "&gt;")
                .replace("\"", "&quot;");
    }
}

class WordCountDecorator extends TextDecorator {
    private int lastWordCount = 0;

    public WordCountDecorator(TextProcessor p) { super(p); }

    @Override
    public String process(String text) {
        String processed = super.process(text);
        lastWordCount = processed.split("\\s+").length;
        return processed + " [" + lastWordCount + " words]";
    }

    public int getLastWordCount() { return lastWordCount; }
}

// Usage — Compose decorators at runtime
class DecoratorDemo {
    public static void main(String[] args) {
        String input = "  <Hello> World & Everyone!  ";

        // Chain: Trim → HtmlEscape → UpperCase
        TextProcessor processor = new UpperCaseDecorator(
                                    new HtmlEscapeDecorator(
                                      new TrimDecorator(
                                        new PlainText())));

        System.out.println(processor.process(input));
        // Output: "<HELLO> WORLD &AMP; EVERYONE!" (trimmed, escaped, uppercased)

        // Java I/O is Decorator pattern
        // new BufferedReader(new InputStreamReader(new FileInputStream("file.txt")))
        // FileInputStream → InputStreamReader → BufferedReader
    }
}
```

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৪ MVC Architecture — OOP দিয়ে

### MVC কী?

```
MVC = Model + View + Controller

Model:   Data ও business logic — database থেকে data পড়া/লেখা
View:    Presentation — user কে দেখানো (UI, JSON response)
Controller: User input নেওয়া, Model call করা, View কে data দেওয়া

Data Flow:
User → Controller → Model → Controller → View → User
```

### Java তে MVC Implementation

```java
import java.util.*;
import java.util.stream.*;

// ========================================
// MODEL — Data + Business Logic
// ========================================
class ProductModel {
    private int id;
    private String name;
    private double price;
    private int stock;
    private String category;

    public ProductModel(int id, String name, double price, int stock, String category) {
        this.id       = id;
        this.name     = name;
        this.price    = price;
        this.stock    = stock;
        this.category = category;
    }

    // Getters
    public int    getId()       { return id; }
    public String getName()     { return name; }
    public double getPrice()    { return price; }
    public int    getStock()    { return stock; }
    public String getCategory() { return category; }

    // Setters with validation (business rule)
    public void setPrice(double price) {
        if (price < 0) throw new IllegalArgumentException("Price cannot be negative.");
        this.price = price;
    }

    public void setStock(int stock) {
        if (stock < 0) throw new IllegalArgumentException("Stock cannot be negative.");
        this.stock = stock;
    }

    public boolean isInStock() { return stock > 0; }

    @Override
    public String toString() {
        return String.format("Product{id=%d, name='%s', price=%.2f, stock=%d}",
                id, name, price, stock);
    }
}

// Repository — Database access simulation
interface ProductRepository {
    void save(ProductModel product);
    Optional<ProductModel> findById(int id);
    List<ProductModel> findAll();
    List<ProductModel> findByCategory(String category);
    boolean delete(int id);
}

class InMemoryProductRepository implements ProductRepository {
    private final Map<Integer, ProductModel> store = new LinkedHashMap<>();
    private int nextId = 1;

    @Override
    public void save(ProductModel product) {
        store.put(product.getId(), product);
    }

    @Override
    public Optional<ProductModel> findById(int id) {
        return Optional.ofNullable(store.get(id));
    }

    @Override
    public List<ProductModel> findAll() {
        return new ArrayList<>(store.values());
    }

    @Override
    public List<ProductModel> findByCategory(String category) {
        return store.values().stream()
                .filter(p -> p.getCategory().equalsIgnoreCase(category))
                .collect(Collectors.toList());
    }

    @Override
    public boolean delete(int id) {
        return store.remove(id) != null;
    }
}

// ========================================
// VIEW — Presentation Layer
// ========================================
class ProductView {
    public void displayProduct(ProductModel product) {
        System.out.println("┌─────────────────────────────────────┐");
        System.out.printf( "│ ID       : %-26d│%n", product.getId());
        System.out.printf( "│ Name     : %-26s│%n", product.getName());
        System.out.printf( "│ Price    : BDT %-22.2f│%n", product.getPrice());
        System.out.printf( "│ Stock    : %-26d│%n", product.getStock());
        System.out.printf( "│ Category : %-26s│%n", product.getCategory());
        System.out.printf( "│ In Stock : %-26s│%n", product.isInStock() ? "✅ Yes" : "❌ No");
        System.out.println("└─────────────────────────────────────┘");
    }

    public void displayProductList(List<ProductModel> products) {
        if (products.isEmpty()) {
            System.out.println("No products found.");
            return;
        }
        System.out.printf("%-4s %-25s %10s %6s %-12s%n",
                "ID", "Name", "Price", "Stock", "Category");
        System.out.println("─".repeat(60));
        products.forEach(p -> System.out.printf("%-4d %-25s %10.2f %6d %-12s%n",
                p.getId(), p.getName(), p.getPrice(), p.getStock(), p.getCategory()));
        System.out.println("─".repeat(60));
        System.out.println("Total: " + products.size() + " products");
    }

    public void displayError(String message) {
        System.err.println("❌ Error: " + message);
    }

    public void displaySuccess(String message) {
        System.out.println("✅ " + message);
    }
}

// ========================================
// CONTROLLER — Handles user requests
// ========================================
class ProductController {
    private final ProductRepository repository;
    private final ProductView view;

    // Dependency Injection — repository ও view বাইরে থেকে inject হয়
    public ProductController(ProductRepository repository, ProductView view) {
        this.repository = repository;
        this.view = view;
    }

    public void addProduct(String name, double price, int stock, String category) {
        try {
            ProductModel product = new ProductModel(
                    generateId(), name, price, stock, category);
            repository.save(product);
            view.displaySuccess("Product added: " + name);
            view.displayProduct(product);
        } catch (IllegalArgumentException e) {
            view.displayError(e.getMessage());
        }
    }

    public void viewProduct(int id) {
        repository.findById(id)
                .ifPresentOrElse(
                    view::displayProduct,
                    () -> view.displayError("Product not found: ID " + id)
                );
    }

    public void listAllProducts() {
        List<ProductModel> products = repository.findAll();
        view.displayProductList(products);
    }

    public void listByCategory(String category) {
        List<ProductModel> products = repository.findByCategory(category);
        System.out.println("\n📦 Products in category: " + category);
        view.displayProductList(products);
    }

    public void updatePrice(int id, double newPrice) {
        repository.findById(id).ifPresentOrElse(product -> {
            try {
                product.setPrice(newPrice);
                repository.save(product);
                view.displaySuccess("Price updated for: " + product.getName());
            } catch (IllegalArgumentException e) {
                view.displayError(e.getMessage());
            }
        }, () -> view.displayError("Product not found: ID " + id));
    }

    public void deleteProduct(int id) {
        if (repository.delete(id)) {
            view.displaySuccess("Product deleted: ID " + id);
        } else {
            view.displayError("Product not found: ID " + id);
        }
    }

    private int generateId() {
        return repository.findAll().stream()
                .mapToInt(ProductModel::getId)
                .max()
                .orElse(0) + 1;
    }
}

// ========================================
// MAIN — Wiring everything together
// ========================================
class MVCDemo {
    public static void main(String[] args) {
        // Dependency wiring
        ProductRepository repo = new InMemoryProductRepository();
        ProductView view = new ProductView();
        ProductController controller = new ProductController(repo, view);

        System.out.println("=== Adding Products ===");
        controller.addProduct("Laptop", 75000, 10, "Electronics");
        controller.addProduct("Mouse", 1200, 50, "Electronics");
        controller.addProduct("Desk", 12000, 5, "Furniture");
        controller.addProduct("Chair", 8000, 8, "Furniture");

        System.out.println("\n=== All Products ===");
        controller.listAllProducts();

        System.out.println("\n=== View Single Product ===");
        controller.viewProduct(1);

        System.out.println("\n=== Category Filter ===");
        controller.listByCategory("Electronics");

        System.out.println("\n=== Update Price ===");
        controller.updatePrice(1, 72000);

        System.out.println("\n=== Delete Product ===");
        controller.deleteProduct(3);
        controller.listAllProducts();
    }
}
```

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৫ Object Cloning — Shallow vs Deep Copy (Revisited)

```java
import java.util.*;

// Cloneable implement করে shallow copy
class Address implements Cloneable {
    String street;
    String city;

    public Address(String street, String city) {
        this.street = street;
        this.city = city;
    }

    @Override
    public Address clone() {
        try {
            return (Address) super.clone();
        } catch (CloneNotSupportedException e) {
            throw new RuntimeException(e);
        }
    }

    @Override
    public String toString() { return street + ", " + city; }
}

class Person implements Cloneable {
    String name;
    int age;
    Address address;         // Reference type — cloning সমস্যা এখানে
    List<String> hobbies;    // Mutable collection — আরেকটি সমস্যা

    public Person(String name, int age, Address address, List<String> hobbies) {
        this.name    = name;
        this.age     = age;
        this.address = address;
        this.hobbies = hobbies;
    }

    // Shallow Copy — address ও hobbies এর reference copy হয়
    public Person shallowCopy() {
        try {
            return (Person) super.clone();
            // ⚠️ this.address ও other.address same object!
        } catch (CloneNotSupportedException e) {
            throw new RuntimeException(e);
        }
    }

    // Deep Copy — সব mutable field এর নতুন copy তৈরি করি
    public Person deepCopy() {
        Address newAddress = new Address(this.address.street, this.address.city);
        List<String> newHobbies = new ArrayList<>(this.hobbies);
        return new Person(this.name, this.age, newAddress, newHobbies);
    }

    @Override
    public String toString() {
        return String.format("Person{name=%s, age=%d, address=%s, hobbies=%s}",
                name, age, address, hobbies);
    }
}

class CloningDemo {
    public static void main(String[] args) {
        Address addr  = new Address("Mirpur-10", "Dhaka");
        List<String> hobbies = new ArrayList<>(Arrays.asList("Reading", "Coding"));
        Person original = new Person("Rafi", 25, addr, hobbies);

        // ─── Shallow Copy ───
        Person shallow = original.shallowCopy();
        shallow.name = "Shallow Rafi";          // Primitive — independent ✅
        shallow.address.city = "Chittagong";    // Reference — modifies BOTH! ❌
        shallow.hobbies.add("Gaming");          // Reference — modifies BOTH! ❌

        System.out.println("Original: " + original);
        System.out.println("Shallow : " + shallow);
        // Original city also changed to "Chittagong"!

        // ─── Deep Copy ───
        Person original2 = new Person("Sumaiya", 23,
                new Address("Dhanmondi", "Dhaka"),
                new ArrayList<>(Arrays.asList("Music", "Art")));

        Person deep = original2.deepCopy();
        deep.name = "Deep Sumaiya";
        deep.address.city = "Sylhet";           // Independent ✅
        deep.hobbies.add("Dancing");            // Independent ✅

        System.out.println("\nOriginal2: " + original2);
        System.out.println("Deep    : " + deep);
        // original2.address.city still "Dhaka"
    }
}
```

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৬ Exception Handling ও OOP

```java
// Custom Exception Hierarchy — OOP দিয়ে
public class AppException extends RuntimeException {
    private final String errorCode;
    private final java.time.LocalDateTime timestamp;

    public AppException(String errorCode, String message) {
        super(message);
        this.errorCode = errorCode;
        this.timestamp = java.time.LocalDateTime.now();
    }

    public AppException(String errorCode, String message, Throwable cause) {
        super(message, cause);
        this.errorCode = errorCode;
        this.timestamp = java.time.LocalDateTime.now();
    }

    public String getErrorCode() { return errorCode; }
    public java.time.LocalDateTime getTimestamp() { return timestamp; }

    @Override
    public String toString() {
        return String.format("[%s] %s | %s | at %s",
                errorCode, getClass().getSimpleName(),
                getMessage(), timestamp);
    }
}

// Domain-specific exceptions (Inheritance)
class ValidationException extends AppException {
    private final String fieldName;

    public ValidationException(String field, String message) {
        super("VALIDATION_ERROR", field + ": " + message);
        this.fieldName = field;
    }

    public String getFieldName() { return fieldName; }
}

class ResourceNotFoundException extends AppException {
    public ResourceNotFoundException(String resourceType, Object id) {
        super("NOT_FOUND", resourceType + " with ID '" + id + "' not found.");
    }
}

class BusinessRuleException extends AppException {
    public BusinessRuleException(String rule, String message) {
        super("BUSINESS_RULE_" + rule, message);
    }
}

// Usage — clean exception handling
class OrderService {
    private final Map<Integer, String> orders = new HashMap<>();

    public void placeOrder(int userId, String item, int quantity) {
        // Validation
        if (item == null || item.trim().isEmpty())
            throw new ValidationException("item", "cannot be empty");
        if (quantity <= 0)
            throw new ValidationException("quantity", "must be positive");
        if (quantity > 100)
            throw new BusinessRuleException("MAX_QUANTITY",
                "Cannot order more than 100 items at once.");

        // Process
        orders.put(userId, item + " x" + quantity);
        System.out.println("✅ Order placed: " + item + " x" + quantity);
    }

    public String getOrder(int userId) {
        String order = orders.get(userId);
        if (order == null)
            throw new ResourceNotFoundException("Order", userId);
        return order;
    }
}

class ExceptionDemo {
    public static void main(String[] args) {
        OrderService service = new OrderService();

        // Clean try-catch with specific exception types
        try {
            service.placeOrder(1, "Laptop", 2);
            service.placeOrder(2, "", 5);       // ValidationException
        } catch (ValidationException e) {
            System.out.println("Validation failed on field: " + e.getFieldName());
            System.out.println(e);
        } catch (BusinessRuleException e) {
            System.out.println("Business rule violated: " + e);
        } catch (AppException e) {
            System.out.println("App error [" + e.getErrorCode() + "]: " + e.getMessage());
        }

        try {
            service.getOrder(99); // ResourceNotFoundException
        } catch (ResourceNotFoundException e) {
            System.out.println(e);
        }
    }
}
```

---

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৬.৭ Advanced OOP Interview Questions

**Q: Design Pattern কী? কেন দরকার?**
> Design Pattern হলো software design এ বারবার দেখা যাওয়া সমস্যার সিদ্ধান্ত template। Code reuse নয়, **design reuse**। Singleton, Factory, Observer — প্রতিটি নির্দিষ্ট সমস্যার প্রমাণিত সমাধান। Communication সহজ হয় — "Singleton use করেছি" বললে সবাই বোঝে।

**Q: Singleton এ কী সমস্যা হতে পারে?**
> ১. Testing কঠিন — mock করা যায় না সহজে  
> ২. Global state — hidden dependency তৈরি হয়  
> ৩. Thread safety — double-checked locking না থাকলে race condition  
> ৪. Reflection attack — `Constructor.setAccessible(true)` দিয়ে bypass  
> **Enum Singleton** এই সব সমস্যা solve করে।

**Q: Factory vs Abstract Factory পার্থক্য?**
> Factory: একটি product type তৈরি করে (e.g., Notification)  
> Abstract Factory: Related products এর family তৈরি করে (e.g., UIFactory → Button + TextBox + ScrollBar সব একটি theme এ)

**Q: Decorator Pattern কোথায় ব্যবহার হয়?**
> Java I/O — `new BufferedReader(new InputStreamReader(new FileInputStream(...)))`। প্রতিটি wrapper decorator। Runtime এ capability যোগ করে, inheritance ছাড়াই।

**Q: Stack Overflow কীভাবে হয়?**
> Method call হলে stack frame push হয়। Recursive call যদি base case ছাড়া চলতে থাকে — stack full হয়ে `StackOverflowError` throw হয়। Circular reference ও কারণ হতে পারে।

**Q: Memory Leak Java তে কীভাবে হয়?**
> Java তে GC থাকলেও leak হয় যখন object এর reference থাকে কিন্তু আর ব্যবহার নেই:  
> ১. Static collection এ unlimited add  
> ২. Event listener deregister না করা  
> ৩. Non-static inner class — outer class reference hold করে  
> ৪. ThreadLocal — remove না করলে thread pool এ leak

**Q: `Comparable` vs `Comparator` কখন কোনটা?**
> `Comparable` — class এর **natural ordering** define করে। Class নিজেই implement করে।  
> `Comparator` — **external/custom ordering** — class change না করে বাইরে define করা যায়।  
> Multiple sort criteria দরকার হলে `Comparator` — `Comparator.comparing(...).thenComparing(...)`।

---

> **⚠️ PART 6 সম্পন্ন হয়েছে।**  
> পরবর্তী PART এর জন্য বলুন: **"PART 7 লিখুন"**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part7"></a>

# PART 7: Bangladeshi Interview Preparation — Mock Interview ও Confidence Guide

> **📍 এই PART এর Sections:** [৭.১ BD Company Interview Structure](#৭১-bangladeshi-tech-company--interview-structure) · [৭.২ Fresher Viva](#৭২-fresher-viva--সবচেয়ে-বেশি-জিজ্ঞেস-করা-প্রশ্ন-ও-আদর্শ-উত্তর) · [৭.৩ Project Explanation](#৭৩-project-explanation--oop-দিয়ে-কীভাবে-বলবেন) · [৭.৪ Mock Interview](#৭৪-complete-mock-interview--পূর্ণ-কথোপকথন) · [৭.৫ Common Mistakes](#৭৫-সাধারণ-interview-ভুল--এড়িয়ে-চলুন) · [৭.৬ Checklist](#৭৬-30-মিনিটের-interview-preparation-checklist) · [৭.৭ Quick Definitions](#৭৭-oop-concept--এক-লাইনের-স্মরণীয়-সংজ্ঞা) · [৭.৮ Rapid-Fire 50](#৭৮-final-rapid-fire--৫০টি-quick-qa)

> **এটি হ্যান্ডবুকের শেষ PART।** এখানে BD tech industry এর real interview pattern, সাধারণ ভুল, এবং সম্পূর্ণ mock interview conversations দেওয়া হয়েছে। প্রতিটি mock conversation জোরে জোরে পড়ুন — মুখস্থ নয়, pattern আয়ত্ত করুন।

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.১ Bangladeshi Tech Company — Interview Structure

### সাধারণ Interview Process

```
Round 1: Written/Online Test (30-60 min)
  ├── MCQ: OOP concepts, Java/C++ basics
  ├── Short answer: Define, difference, advantage
  └── Simple coding: Class design, fix the bug

Round 2: Technical Interview (45-90 min)
  ├── CV review: Project explanation
  ├── OOP theory: Definitions, differences, use-cases
  ├── Live coding: Class hierarchy design on paper/whiteboard
  └── Problem solving: Simple DS/Algorithm + OOP design

Round 3: HR Interview (15-30 min)
  ├── Salary expectation
  ├── Career goal
  └── Team fit

Round 4 (Senior-level): System Design (60-90 min)
  └── Only for 2+ years experience
```

### BD Companies তে OOP প্রশ্নের Pattern

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Company Type        Common OOP Questions
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Service Company     4 pillars definition, abstract vs interface,
(BJIT, Brain Station, SELISE, Braincraft)
                    polymorphism example, simple class design

Product Company     SOLID principles, Design patterns (Singleton,
(Chaldal, Shohoz, Pathao, Shuttle)
                    Factory), system design basics, scalability

Banking/Fintech     Security-conscious OOP, encapsulation emphasis,
(BRAC IT, Dutch-Bangla, ShurjoPay)
                    exception handling, transaction design

Telecom IT          C++ knowledge (Grameenphone, Robi), vtable,
                    memory management, performance

Startup             Practical OOP in project, framework knowledge
                    (Spring Boot), REST API design
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.২ Fresher Viva — সবচেয়ে বেশি জিজ্ঞেস করা প্রশ্ন ও আদর্শ উত্তর

### প্রশ্ন ১: "OOP কী? কেন ব্যবহার করা হয়?"

**দুর্বল উত্তর (এড়িয়ে চলুন):**
> "OOP মানে Object Oriented Programming। এখানে object থাকে।"

**শক্তিশালী উত্তর:**
> "OOP হলো একটি programming paradigm যেখানে real-world entities কে object হিসেবে model করা হয়। প্রতিটি object এ data (fields) ও behavior (methods) একসাথে থাকে।
>
> কেন ব্যবহার করা হয়? তিনটি কারণে:
> এক — **Maintainability**: Code modular থাকে, একটি class change করলে অন্যটিতে প্রভাব পড়ে না।
> দুই — **Reusability**: Inheritance দিয়ে existing code extend করা যায়।
> তিন — **Real-world modeling**: Software আর real system এর মধ্যে সরাসরি mapping থাকে — বোঝা সহজ।
>
> আমি আমার Student Management System project এ OOP use করেছিলাম — Student abstract class, UndergraduateStudent ও GraduateStudent subclass — real university structure এর সাথে directly map করে।"

---

### প্রশ্ন ২: "Encapsulation explain করুন — real example দিয়ে।"

**শক্তিশালী উত্তর:**
> "Encapsulation মানে data আর method একসাথে wrap করা এবং internal state বাইরে থেকে direct access এ রক্ষা করা।
>
> Real life example: ATM Machine। আপনি PIN দেন, টাকা নেন — কিন্তু ভেতরে কীভাবে balance check হচ্ছে, কোন database call হচ্ছে সেটা দেখতে পান না। শুধু defined interface — card slot, keypad, screen — দিয়ে interact করেন।
>
> Code এ: `BankAccount` class এ `balance` field `private`। শুধু `deposit()`, `withdraw()` method দিয়ে change হয়। সরাসরি `account.balance = -1000` করা যায় না। Validation সব setter এ।
>
> Benefits: invalid state prevent হয়, implementation change করলেও client code break হয় না।"

---

### প্রশ্ন ৩: "Abstraction vs Encapsulation — পার্থক্য কী?"

**অনেকে confuse করে। শক্তিশালী উত্তর:**
> "দুটো আলাদা concept।
>
> **Encapsulation** — *HOW* hide করা। Implementation details লুকানো। `private` fields, `public` methods। Internal complexity hide।
>
> **Abstraction** — *WHAT* দেখানো। Unnecessary detail বাদ দিয়ে essential feature দেখানো। Abstract class বা interface দিয়ে 'কী করতে পারবে' define, 'কীভাবে করবে' hide।
>
> উদাহরণ: `List<String> list = new ArrayList<>()` — Abstraction, আমি জানি list কী করতে পারে (`add`, `remove`, `get`), কিন্তু ArrayList internally resizable array ব্যবহার করে — সেটা Encapsulation।
>
> সহজ মনে রাখার উপায়: Abstraction = design level, Encapsulation = implementation level।"

---

### প্রশ্ন ৪: "Compile-time vs Runtime Polymorphism পার্থক্য কী?"

**শক্তিশালী উত্তর:**
> "Compile-time polymorphism হয় Method Overloading দিয়ে — same method name, different parameters। Compiler compile সময় কোন method call হবে decide করে। Fast।
>
> Runtime polymorphism হয় Method Overriding দিয়ে — parent class এর method child এ override। কোন method call হবে runtime এ JVM decide করে — reference type নয়, actual object type দেখে।
>
> উদাহরণ:
> ```java
> Animal a = new Dog();
> a.sound(); // Runtime এ Dog এর sound() call হয় — Runtime Polymorphism
> ```
> এখানে `a` Animal type কিন্তু actual object Dog। JVM vtable দেখে Dog এর `sound()` call করে।"

---

### প্রশ্ন ৫: "Abstract Class ব্যবহার করবেন নাকি Interface? কীভাবে decide করবেন?"

**শক্তিশালী উত্তর:**
> "আমি তিনটি প্রশ্ন করি নিজেকে:
>
> এক — **shared state দরকার?** হ্যাঁ হলে Abstract Class। Interface এ field থাকে না।
>
> দুই — **'is-a' relationship?** হ্যাঁ হলে Abstract Class। Dog is-a Animal → `abstract class Animal`।
>
> তিন — **'can-do' / capability?** হ্যাঁ হলে Interface। Flyable, Printable, Comparable → interface।
>
> প্রথমে Interface দিয়ে শুরু করুন। যদি common implementation share করতে হয় তাহলে Abstract Class। Java তে multiple interface implement করা যায় কিন্তু multiple class extend যায় না — তাই Interface বেশি flexible।"

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৩ Project Explanation — OOP দিয়ে কীভাবে বলবেন

### সূত্র: STAR + OOP Mapping

```
S — Situation: কী project ছিল, কী problem solve করতে হয়েছিল
T — Task: আপনার specific responsibility কী ছিল
A — Action: কী OOP concepts apply করেছেন, কেন
R — Result: কী অর্জন হয়েছে
```

### Example: "আপনার project সম্পর্কে বলুন"

**দুর্বল উত্তর:**
> "আমার project ছিল একটি Student Management System। আমি Java দিয়ে বানিয়েছি। Student add, delete, update করা যায়।"

**শক্তিশালী উত্তর (STAR + OOP):**
> "আমার final year project ছিল একটি University Student Management System যেখানে একটি বিশ্ববিদ্যালয়ের Undergraduate ও Graduate student দের data manage করতে হতো।
>
> আমার responsibility ছিল backend OOP design ও core business logic।
>
> আমি **Inheritance** ব্যবহার করেছি — `Student` abstract class থেকে `UndergraduateStudent` ও `GraduateStudent` extend করেছি। Common fields — name, roll, CGPA — parent এ, type-specific fields — semester, thesis topic — child এ।
>
> **Encapsulation** দিয়ে সব fields private রেখে validated setter ব্যবহার করেছি — CGPA সরাসরি set করা যেত না, validation ছাড়া।
>
> **Abstraction** দিয়ে `StudentRepository` interface তৈরি করেছি — `add`, `findByRoll`, `getTopStudents` method define, implementation আলাদা `StudentManager` class এ।
>
> Result: নতুন student type যোগ করতে শুধু একটি নতুন subclass তৈরি করতে হয়, existing code change করতে হয় না। OCP মেনে চলেছে।"

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৪ Complete Mock Interview — পূর্ণ কথোপকথন

### Mock Interview 1: Entry-Level Java Developer (Service Company)

---

**Interviewer:** আসুন, বসুন। আপনার CV দেখলাম। আচ্ছা, সরাসরি technical এ যাই — OOP এর চারটি pillar কী?

**Candidate (ভালো উত্তর):**
> "অবশ্যই। চারটি pillar হলো:
> এক — **Encapsulation**: Data ও method একসাথে class এ রাখা, internal state hide করা। Private fields, public methods।
> দুই — **Abstraction**: Essential details দেখানো, unnecessary complexity hide করা। Abstract class ও interface দিয়ে।
> তিন — **Inheritance**: Existing class extend করে নতুন class তৈরি। Code reuse, 'is-a' relationship।
> চার — **Polymorphism**: একই interface, আলাদা behavior। Overloading (compile-time) ও Overriding (runtime)।"

---

**Interviewer:** ভালো। এখন বলুন — `abstract class` ও `interface` এর পার্থক্য কী? কোনটি কখন use করবেন?

**Candidate:**
> "মূল পার্থক্যগুলো হলো:
> Abstract class এ constructor, instance variable, concrete method থাকতে পারে। Interface এ (Java 8 এর আগে) শুধু abstract method।
>
> Java 8 থেকে interface এ default ও static method যোগ হয়েছে, তবু instance variable থাকে না।
>
> একটি class শুধু একটি abstract class extend করতে পারে, কিন্তু multiple interface implement করতে পারে।
>
> কখন কোনটি? Abstract class: যখন subclasses এর মধ্যে shared state বা partial implementation দরকার, 'is-a' relationship আছে। Interface: যখন capability define করতে হবে, multiple inheritance দরকার, 'can-do' relationship।
>
> Simple rule: Interface দিয়ে শুরু করুন। Common code share করতে হলে Abstract class।"

---

**Interviewer:** আচ্ছা, এই code টি দেখুন। কী সমস্যা আছে বলুন।

```java
class Animal {
    String name;

    Animal(String name) { this.name = name; }

    void sound() { System.out.println("Some sound"); }
}

class Dog extends Animal {
    Dog(String name) { super(name); }

    void sound() { System.out.println("Woof"); }
}

public class Main {
    public static void main(String[] args) {
        Animal a = new Dog("Rex");
        a.sound();
    }
}
```

**Candidate:**
> "Code টি technically কাজ করবে — output হবে 'Woof' কারণ runtime polymorphism। কিন্তু কিছু improvement করা যায়:
>
> এক — `name` field `public` বা package-private — Encapsulation ভাঙছে। `private` করে getter যোগ করা উচিত।
>
> দুই — `Animal` যদি কখনো standalone instantiate হওয়া না উচিত হয়, তাহলে `abstract` করা উচিত এবং `sound()` abstract রাখা উচিত — তাহলে প্রতিটি subclass নিজের sound define করতে বাধ্য হবে।
>
> তিন — `@Override` annotation add করা উচিত `Dog.sound()` তে — accidental signature mismatch catch করতে।
>
> চার — `Animal` এর constructor parameter validation নেই — `name` null বা empty হলে?
>
> Code টি Polymorphism ভালো demonstrate করছে — `Animal` reference, `Dog` object, `sound()` call — সঠিকভাবে Dog এর method call হচ্ছে।"

---

**Interviewer:** ভালো বলেছেন। এখন একটু coding — আমাকে একটি `Shape` hierarchy design করুন। Circle ও Rectangle থাকবে।

**Candidate:**
> "অবশ্যই। আমি abstract class দিয়ে শুরু করব।"

```java
abstract class Shape {
    private String color;

    public Shape(String color) {
        this.color = color;
    }

    public String getColor() { return color; }

    // Abstract — subclass must implement
    public abstract double area();
    public abstract double perimeter();

    // Template method — final, cannot override
    public final void describe() {
        System.out.printf("%s [Color: %s, Area: %.2f, Perimeter: %.2f]%n",
                getClass().getSimpleName(), color, area(), perimeter());
    }
}

class Circle extends Shape {
    private double radius;

    public Circle(String color, double radius) {
        super(color);
        if (radius <= 0) throw new IllegalArgumentException("Radius must be positive.");
        this.radius = radius;
    }

    @Override
    public double area()      { return Math.PI * radius * radius; }
    @Override
    public double perimeter() { return 2 * Math.PI * radius; }
}

class Rectangle extends Shape {
    private double width, height;

    public Rectangle(String color, double w, double h) {
        super(color);
        this.width = w; this.height = h;
    }

    @Override
    public double area()      { return width * height; }
    @Override
    public double perimeter() { return 2 * (width + height); }
}
```

> "এখানে Encapsulation — `radius`, `width`, `height` private। Abstraction — `area()` ও `perimeter()` abstract, subclass implement করে। Polymorphism —
> ```java
> Shape[] shapes = { new Circle("Red", 5), new Rectangle("Blue", 4, 6) };
> for (Shape s : shapes) s.describe(); // Runtime polymorphism
> ```"

---

**Interviewer:** চমৎকার। একটু SOLID নিয়ে জিজ্ঞেস করি — Single Responsibility Principle বলুন।

**Candidate:**
> "Single Responsibility Principle বলে একটি class এর শুধু একটি কারণে পরিবর্তন হওয়া উচিত — মানে একটি class এর একটিমাত্র responsibility।
>
> উদাহরণ: একটি `Employee` class যদি salary calculate করে এবং database তে save করে এবং PDF report generate করে — এটি SRP ভাঙছে। তিনটি আলাদা responsibility।
>
> Fix: `Employee` — শুধু data। `SalaryCalculator` — calculation। `EmployeeRepository` — persistence। `ReportGenerator` — report।
>
> কেন গুরুত্বপূর্ণ? Salary calculation logic change করতে হলে শুধু `SalaryCalculator` change হবে — database code বা report code affect হবে না।"

---

**Interviewer:** আচ্ছা, আর কিছু জানতে চান?

**Candidate (good follow-up questions):**
> "হ্যাঁ, কয়েকটি প্রশ্ন আছে। আপনাদের backend stack কী — Spring Boot ব্যবহার করেন? Project এ কোন design patterns actively follow করেন? New joiners এর জন্য mentorship program আছে কি?"

---

### Mock Interview 2: Fresher — ভুল উত্তর ও সংশোধন

এই section এ candidate ভুল উত্তর দেয় এবং interviewer সংশোধন করেন।

---

**Interviewer:** Polymorphism কী?

**Candidate (ভুল):**
> "Polymorphism মানে একই নামে অনেক method থাকা।"

**Interviewer:** শুধু এটুকু? আর কিছু?

**Candidate (আরো ভুল):**
> "হ্যাঁ, overloading এ একই নামে method থাকে।"

**Interviewer (সংশোধন):**
> "Overloading Polymorphism এর একটি ধরন — Compile-time। কিন্তু Runtime Polymorphism হলো মূল concept — parent class reference দিয়ে child class method call। Overriding। আপনাকে উভয়টি জানতে হবে।"

**Candidate (সংশোধিত উত্তর হওয়া উচিত ছিল):**
> "Polymorphism মানে 'many forms' — একই interface, আলাদা implementation।
> দুটি ধরন:
> Compile-time — Overloading, same name different parameters, compiler decide করে।
> Runtime — Overriding, parent reference child object, JVM runtime এ decide করে। এটাই মূল OOP concept।"

---

**Interviewer:** Inheritance কী সমস্যা তৈরি করতে পারে?

**Candidate (ভুল):**
> "Inheritance তেমন সমস্যা করে না।"

**Interviewer:** একটু ভাবুন — Diamond Problem?

**Candidate (সংশোধিত উত্তর হওয়া উচিত):**
> "ঠিক বলেছেন। Inheritance এর কয়েকটি সমস্যা আছে:
> এক — Diamond Problem: Multiple inheritance এ A → B, A → C, D → B, C — D তে A এর কোন version? Java তে class এ multiple inheritance নেই বলে এটি এড়ানো যায়।
> দুই — Tight coupling: Subclass parent এর implementation এর উপর depend করে। Parent change করলে সব child affect হতে পারে।
> তিন — Fragile base class: Parent class change করলে subclass break হতে পারে।
> এজন্য 'Favour Composition over Inheritance' — inheritance কে 'is-a' relationship এ সীমাবদ্ধ রাখুন।"

---

### Mock Interview 3: Mid-Level (1-2 years experience)

---

**Interviewer:** Design Patterns কতটুকু জানেন? একটি বলুন যা আপনি project এ use করেছেন।

**Candidate:**
> "আমি Singleton, Factory, Observer pattern জানি। Project এ Singleton সবচেয়ে বেশি use করেছি — database connection management এ।
>
> Context: Application এ multiple জায়গায় DB connection দরকার। প্রতিবার নতুন connection তৈরি হলে performance খারাপ।
>
> Solution: `DatabaseManager` singleton — শুধু একটিই instance, সব request একই connection pool use করে।
>
> Implementation এ double-checked locking এবং `volatile` keyword — thread safety নিশ্চিত করতে।
>
> কিন্তু একটা সীমাবদ্ধতা জানি — Singleton unit test এ mock করা কঠিন। তাই dependency injection দিয়ে interface inject করা better practice।"

---

**Interviewer:** SOLID principles জানেন? Open-Closed Principle বলুন — example দিয়ে।

**Candidate:**
> "Open-Closed Principle বলে — software entities extension এর জন্য open, modification এর জন্য closed।
>
> মানে: নতুন feature যোগ করতে existing tested code modify না করে নতুন class add করুন।
>
> Example: আমার notification system এ প্রথমে শুধু Email ছিল। SMS যোগ করতে হলো।
>
> OCP ভাঙা version:
> ```java
> class NotificationService {
>     void send(String type, String msg) {
>         if (type.equals("EMAIL")) { /* email */ }
>         else if (type.equals("SMS")) { /* sms */ }
>         // নতুন type আসলে এই method modify করতে হবে — OCP ভঙ্গ
>     }
> }
> ```
>
> OCP মানা version: `Notification` abstract class, `EmailNotification`, `SMSNotification` subclass। `NotificationFactory` দিয়ে create। নতুন `PushNotification` যোগ করতে শুধু নতুন class, existing code touch করতে হয় না।"

---

**Interviewer:** আচ্ছা, আপনার কাছে একটি scenario — আপনাকে একটি Payment System design করতে বলা হয়েছে। Credit Card, bKash, Nagad support করতে হবে। কীভাবে design করবেন?

**Candidate:**
> "আমি প্রথমে requirements clarify করব — শুধু payment processing নাকি refund, transaction history ও দরকার?
>
> Design:
>
> প্রথমে `PaymentMethod` interface — `processPayment(amount)`, `refund(transactionId)`, `getType()` method।
>
> তারপর concrete implementations: `CreditCardPayment`, `BkashPayment`, `NagadPayment` — প্রতিটি নিজের API call করে।
>
> `Transaction` record class — id, amount, method, timestamp, status।
>
> `PaymentProcessor` context class — যেকোনো `PaymentMethod` inject করা যায় (Strategy Pattern)।
>
> `PaymentFactory` — payment method string থেকে সঠিক object তৈরি।
>
> এতে OCP মানা হয় — নতুন payment method যোগ করতে শুধু নতুন class implement করতে হবে।
>
> SOLID:
> SRP — প্রতিটি class একটি কাজ।
> OCP — নতুন method extension দিয়ে।
> LSP — সব PaymentMethod replaceable।
> DIP — `PaymentProcessor` interface এ depend করে, concrete class এ নয়।"

---

**Interviewer:** খুব ভালো। শেষ প্রশ্ন — আপনার দুর্বলতা কী technical দিক থেকে?

**Candidate (সৎ ও smart উত্তর):**
> "System Design এ আমি এখনো শিখছি — বড় scale এর distributed system design আমার কাছে নতুন। তবে আমি actively লেখাপড়া করছি — Design Patterns ভালোভাবে শিখেছি এখন।
>
> আরেকটি দুর্বলতা — unit testing এ আমি বেশি লিখি না এখনো। কিন্তু TDD এর গুরুত্ব বুঝি এবং JUnit, Mockito শিখছি।
>
> আমার শক্তি — OOP design, clean code, Java core। দুর্বল দিকগুলোতে কাজ করছি।"

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৫ সাধারণ Interview ভুল — এড়িয়ে চলুন

### Technical ভুল

| ভুল | কেন সমস্যা | সমাধান |
|-----|-----------|--------|
| Definition মুখস্থ, example নেই | Surface knowledge বোঝা যায় | প্রতিটি concept এ code example দিন |
| "Java তে virtual keyword লাগে" | Java তে default virtual | "C++ এ লাগে, Java তে সব non-static method virtual" বলুন |
| Abstract ও Interface কে same বলা | মূল pার্থক্য ধরা পড়বে | Instance variable, constructor — key differences মনে রাখুন |
| Polymorphism = শুধু overloading | Runtime polymorphism বড় concept | Overloading + Overriding দুটোই বলুন, runtime টা emphasize করুন |
| `==` ও `.equals()` confuse করা | String comparison এ common trap | `==` reference, `.equals()` value — সবসময় |
| NullPointerException কোথা থেকে আসে বলতে না পারা | Practical knowledge দেখায় | Null reference এ method call, uninitialized object |
| Design pattern জিজ্ঞেস করলে blank হয়ে যাওয়া | Intermediate knowledge gap | Singleton + Factory minimum জানুন |

### Communication ভুল

| ভুল | সমাধান |
|-----|--------|
| হ্যাঁ/না দিয়ে উত্তর শেষ করা | সব সময় example যোগ করুন |
| "জানি না" বলে থেমে যাওয়া | "সরাসরি জানি না, তবে আমার মনে হয়..." বলুন |
| দ্রুত কথা বলা, থামা নেই | Pause নিন, চিন্তা করুন |
| প্রশ্ন না বোঝা সত্ত্বেও উত্তর দেওয়া | "আপনি কি এটা জানতে চাইছেন...?" বলুন |
| Project জিজ্ঞেস করলে technical না বলা | OOP concepts mention করুন project এ |
| বেতন আগে জিজ্ঞেস করা | HR round এর জন্য অপেক্ষা করুন |

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৬ 30-মিনিটের Interview Preparation Checklist

### Interview এর আগের দিন

```
□ OOP 4 pillars — definition + 1 example each (মুখে বলুন, লিখুন না)
□ Abstract Class vs Interface — 5টি পার্থক্য মুখস্থ
□ Overloading vs Overriding — code example মাথায়
□ SOLID principles — প্রতিটির one-liner
□ Singleton pattern — code না দেখে লিখুন
□ Factory pattern — code না দেখে লিখুন
□ আপনার project OOP দিয়ে explain করুন (3 মিনিটের script)
□ Java: equals/hashCode, String immutable, == vs .equals()
□ CV পড়ুন — সব technology সম্পর্কে প্রশ্নের জন্য ready
```

### Interview এর দিন

```
□ 15 মিনিট আগে পৌঁছান
□ Interviewer কে কী project করেন জিজ্ঞেস করুন — context বুঝুন
□ প্রশ্ন না বুঝলে repeat করতে বলুন
□ Code লেখার আগে design বলুন
□ Edge case mention করুন — "null হলে কী হবে?"
□ Interview শেষে 2-3টি smart প্রশ্ন করুন
```

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৭ OOP Concept — এক লাইনের স্মরণীয় সংজ্ঞা

> এই সংজ্ঞাগুলো মনে রাখুন — interview শুরুতে সংক্ষেপে বলুন, তারপর বিস্তারিত।

| Concept | এক লাইন সংজ্ঞা |
|---------|--------------|
| **Class** | Object এর blueprint — attributes ও behaviors define করে |
| **Object** | Class এর instance — memory তে actual entity |
| **Encapsulation** | Data আর method একসাথে — internal state hide করা |
| **Abstraction** | Essential দেখানো, detail hide — "what" not "how" |
| **Inheritance** | Parent এর property child এ — code reuse, "is-a" |
| **Polymorphism** | একই interface, আলাদা behavior — "many forms" |
| **Overloading** | Same name, different parameters — compile-time |
| **Overriding** | Parent method redefine — runtime dispatch |
| **Abstract Class** | Partial implementation — instantiate করা যায় না |
| **Interface** | Pure contract — "can-do" capability define করে |
| **Constructor** | Object তৈরির সময় চলে — initialization |
| **Destructor** | Object মুছে যাওয়ার সময় — cleanup (C++) |
| **Static** | Class এর — object ছাড়া access, shared |
| **Final** | Immutable variable, unoverridable method, unextendable class |
| **Singleton** | শুধু একটি instance — global access point |
| **Factory** | Object তৈরি encapsulate — client `new` করে না |
| **Observer** | One-to-many notification — loose coupling |
| **SRP** | একটি class, একটি responsibility |
| **OCP** | Extension এ open, modification এ closed |
| **LSP** | Subclass parent কে replace করতে পারে |
| **ISP** | বড় interface ভেঙে ছোট specific interface |
| **DIP** | Abstraction এ depend করো, concrete তে নয় |

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৮ Final Rapid-Fire — ৫০টি Quick Q&A

> **Practice method:** একজন বলবে প্রশ্ন, আপনি ১ বাক্যে উত্তর দেবেন। ৩০ সেকেন্ডের বেশি নয়।

**১.** Class কী? → Object এর blueprint।  
**২.** Object কী? → Class এর instance, memory তে।  
**৩.** Constructor কী? → Object তৈরির সময় চলা special method।  
**৪.** Constructor কি return করে? → না, কিছু return করে না।  
**৫.** Java তে default constructor কখন? → কোনো constructor না লিখলে।  
**৬.** `this` keyword কী? → Current object এর reference।  
**৭.** `super` keyword কী? → Parent class এর reference।  
**৮.** Encapsulation কীভাবে implement করা হয়? → Private fields, public getters/setters।  
**৯.** Abstraction কীভাবে achieve হয়? → Abstract class ও Interface দিয়ে।  
**১০.** Inheritance কোন keyword দিয়ে? → `extends` (class), `implements` (interface)।  
**১১.** Java তে multiple inheritance কেন নেই? → Diamond Problem এড়াতে।  
**১২.** Method Overloading কী? → Same name, different parameters, same class।  
**১৩.** Method Overriding কী? → Child class parent এর method redefine করা।  
**১৪.** `@Override` কী করে? → Compile-time check — সত্যিই override কিনা।  
**১৫.** `static` method কি override হয়? → না — method hiding হয়।  
**১৬.** `final` method কি override হয়? → না।  
**১৭.** `abstract` method কি body থাকে? → না — শুধু signature।  
**১৮.** Abstract class instantiate করা যায়? → না।  
**১৯.** Interface instantiate করা যায়? → না, শুধু implement করা যায়।  
**২০.** Interface এ variable কেমন? → `public static final` — constant।  
**২১.** Java 8 এ interface এ কী নতুন? → Default method ও Static method।  
**২২.** `instanceof` কী করে? → Object কোন class এর instance তা check করে।  
**২৩.** Upcasting কী? → Child object কে parent reference দিয়ে refer করা।  
**২৪.** Downcasting কী? → Parent reference থেকে child type এ cast।  
**২৫.** `ClassCastException` কখন? → Incompatible downcast করলে।  
**২৬.** Shallow copy কী? → Reference copy — same objects point।  
**২৭.** Deep copy কী? → Object এর নতুন independent copy।  
**২৮.** `String` কি immutable? → হ্যাঁ — change হলে নতুন object তৈরি।  
**২৯.** `==` vs `.equals()` String এ? → `==` reference, `.equals()` content।  
**৩০.** `final` variable কি change করা যায়? → না — once assigned।  
**৩১.** Singleton Pattern কী? → একটি class এর শুধু একটি instance।  
**৩২.** Factory Pattern কী? → Object creation encapsulate করা।  
**৩৩.** Observer Pattern কী? → One-to-many event notification।  
**৩৪.** Decorator Pattern কী? → Runtime এ object এ behavior যোগ করা।  
**৩৫.** Strategy Pattern কী? → Algorithm family — runtime এ swap করা যায়।  
**৩৬.** SRP কী? → একটি class এর একটিই responsibility।  
**৩৭.** OCP কী? → Extension এ open, modification এ closed।  
**৩৮.** LSP কী? → Subclass parent কে replace করতে পারে।  
**৩৯.** ISP কী? → Interface ছোট, specific রাখো।  
**৪০.** DIP কী? → Abstraction এ depend করো, concrete তে নয়।  
**৪১.** Dependency Injection কী? → Dependency বাইরে থেকে inject করা।  
**৪২.** Composition vs Inheritance? → Composition more flexible — "has-a" vs "is-a"।  
**৪৩.** Coupling কী? → Classes এর মধ্যে dependency — কম হওয়া ভালো।  
**৪৪.** Cohesion কী? → Class এর methods কতটা related — বেশি হওয়া ভালো।  
**৪৫.** Java তে GC কী করে? → Unreachable object এর memory reclaim করে।  
**৪৬.** Memory Leak Java তে? → Static collection এ unreferenced object।  
**৪৭.** Stack Overflow কেন হয়? → Infinite recursion, stack frame শেষ।  
**৪৮.** `NullPointerException` কেন? → Null reference এ method call।  
**৪৯.** `try-with-resources` কী? → AutoCloseable resource automatically close হয়।  
**৫০.** Polymorphism এর সুবিধা? → New type যোগ করা সহজ, existing code change নেই।  

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## ৭.৯ হ্যান্ডবুক ব্যবহার গাইড — Revision Plan

### ৭ দিনের Revision Schedule

```
Day 1 — PART 1 পড়ুন (OOP Fundamentals)
  ✦ 4 pillars definition মুখে বলুন
  ✦ Constructor/Destructor code নিজে লিখুন
  ✦ Quick Reference Table মনে রাখুন

Day 2 — PART 2 পড়ুন (Advanced OOP)
  ✦ Static vs Dynamic binding বুঝুন
  ✦ Abstract class vs Interface comparison
  ✦ SOLID 5 principles — example মুখে বলুন

Day 3 — PART 3 পড়ুন (50 Q&A)
  ✦ প্রতিটি প্রশ্ন নিজে উত্তর দেওয়ার চেষ্টা করুন আগে
  ✦ যেগুলো পারেননি সেগুলো mark করুন
  ✦ Marked গুলো পরের দিন review করুন

Day 4 — PART 4 পড়ুন (Coding Problems)
  ✦ প্রতিটি system কাগজে draw করুন (class diagram)
  ✦ Student Management System নিজে লিখুন
  ✦ Interview explanation strategy practice করুন

Day 5 — PART 5 পড়ুন (Language-Specific)
  ✦ Java focus: equals/hashCode, Comparable/Comparator
  ✦ যে ভাষায় interview দেবেন সেটা বেশি পড়ুন

Day 6 — PART 6 পড়ুন (Design Patterns)
  ✦ Singleton code না দেখে লিখুন
  ✦ Factory + Observer pattern বুঝুন
  ✦ MVC architecture diagram আঁকুন

Day 7 — PART 7 পড়ুন (এই PART)
  ✦ Mock Interview 1 জোরে জোরে পড়ুন (দুই ভূমিকায়)
  ✦ 50 Rapid-fire নিজে করুন
  ✦ Project explanation 3 মিনিট practice করুন
```

### Interview এর আগের রাতে

```
❌ নতুন topic শিখবেন না
❌ রাত জাগবেন না
✅ PART 7 এর Rapid-fire একবার করুন
✅ Project explanation একবার বলুন
✅ সকালে fresh মাথায় যান
```

---

> **🎉 হ্যান্ডবুক সম্পূর্ণ হয়েছে!**  
> সাতটি PART এ সম্পূর্ণ OOP Interview Preparation কভার করা হয়েছে।  
> **শুভকামনা আপনার interview এ!** 🚀

---

<div align="right"><a href="#part7">⬆ PART 7 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

## হ্যান্ডবুক সূচি (Index)

| PART | বিষয় | মূল topics |
|------|-------|-----------|
| **PART 1** | OOP Fundamentals | 4 pillars, Class/Object, Constructor, Access Modifiers, Quick Reference |
| **PART 2** | Advanced OOP | Static/Dynamic Binding, Interface, Abstract Class, Virtual Functions, SOLID, DI |
| **PART 3** | Interview Q&A | 50 Theoretical Questions, Common Mistakes, Follow-up Patterns |
| **PART 4** | Coding Problems | Student/Bank/Employee/Library Management System — Full Java Code |
| **PART 5** | Language-Specific | Java, C++, Python, C# — পার্থক্য, traps, BD company focus |
| **PART 6** | Advanced Topics | Memory, GC, Design Patterns (6টি), MVC, Exception Hierarchy |
| **PART 7** | BD Interview Focus | Company patterns, Mock Interviews, 50 Rapid-fire, Revision Plan |

---

*হ্যান্ডবুক তৈরিতে: Senior Software Engineer & Technical Interviewer*  
*Version: 1.0 | তারিখ: মে ২০২৬*  
*মোট PART: 7 | সম্পূর্ণ*
