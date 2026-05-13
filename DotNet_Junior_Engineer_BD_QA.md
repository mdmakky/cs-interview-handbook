<a id="top"></a>

# 🔷 .NET Interview Preparation Handbook
### বাংলাদেশের Junior .NET / ASP.NET Core Developer-দের জন্য সম্পূর্ণ Interview Preparation Guide

> 💡 **হ্যান্ডবুক ব্যবহারের নিয়ম:**
> প্রতিটি টপিক মনোযোগ দিয়ে পড়ুন। Code examples নিজে লিখুন। Interview questions নিজে উত্তর দেওয়ার চেষ্টা করুন তারপর model answer দেখুন।

---

## 📋 সূচিপত্র — Table of Contents

> 💡 নিচের যেকোনো PART এ সরাসরি ক্লিক করুন। প্রতিটি PART এর শেষে 🔝 শীর্ষে ফিরুন বাটন আছে।

| PART | বিষয়বস্তু | অবস্থা |
|------|-----------|--------|
| [PART 1](#part1) | .NET Fundamentals | ✅ |
| [PART 2](#part2) | C# Fundamentals | ✅ |
| [PART 3](#part3) | OOP in C# | ✅ |
| [PART 4](#part4) | Advanced C# | ✅ |
| [PART 5](#part5) | ASP.NET Core Fundamentals | ✅ |
| [PART 6](#part6) | Web API Development | ✅ |
| [PART 7](#part7) | Database & Entity Framework Core | ✅ |
| [PART 8](#part8) | Authentication & Security | ✅ |
| [PART 9](#part9) | Frontend Integration & Full Stack | ✅ |
| [PART 10](#part10) | Testing & Debugging | ✅ |
| [PART 11](#part11) | Deployment & DevOps Basics | ✅ |
| [PART 12](#part12) | System Design with .NET | ✅ |
| [PART 13](#part13) | .NET Projects | ✅ |
| PART 14 | Interview Questions Bank | ⏳ |
| PART 15 | Bangladeshi Interview Preparation | ⏳ |

---

<a id="part1"></a>
## PART 1: .NET Fundamentals

> CLR, CTS, CLS, JIT, Garbage Collection, Assemblies, NuGet — .NET-এর core architecture সম্পর্কে সম্পূর্ণ ধারণা।

| # | বিষয় |
|---|-------|
| 1 | [.NET কী?](#p1-what-is-dotnet) |
| 2 | [.NET-এর ইতিহাস](#p1-history) |
| 3 | [.NET Framework vs .NET Core vs .NET (5+)](#p1-versions) |
| 4 | [CLR — Common Language Runtime](#p1-clr) |
| 5 | [CTS — Common Type System](#p1-cts) |
| 6 | [CLS — Common Language Specification](#p1-cls) |
| 7 | [JIT Compiler](#p1-jit) |
| 8 | [Managed vs Unmanaged Code](#p1-managed) |
| 9 | [IL — Intermediate Language](#p1-il) |
| 10 | [Garbage Collection](#p1-gc) |
| 11 | [Assemblies](#p1-assemblies) |
| 12 | [NuGet Packages](#p1-nuget) |
| 13 | [SDK vs Runtime](#p1-sdk-runtime) |
| 14 | [Solution & Project Structure](#p1-structure) |

---

<a id="p1-what-is-dotnet"></a>
### Topic 1: .NET কী?

**সংজ্ঞা (Definition):**

**.NET** হলো Microsoft-এর তৈরি একটি **free, open-source, cross-platform developer platform** — যা দিয়ে web applications, desktop applications, mobile apps, cloud services, games, এবং IoT solutions তৈরি করা যায়।

.NET একটি **platform**, একটি single programming language নয়। এই platform-এ C#, F#, এবং Visual Basic (VB.NET) — এই তিনটি প্রধান programming language ব্যবহার করা যায়।

```
.NET Platform
├── Languages         → C#, F#, VB.NET
├── Runtime           → CLR (Common Language Runtime)
├── Base Class Library → System, Collections, IO, Net, Threading...
├── Frameworks        → ASP.NET Core, Entity Framework, MAUI, Blazor
└── Tools             → dotnet CLI, NuGet, MSBuild
```

**🏠 Real-life Analogy:**

ধরুন .NET হলো একটি **শহরের infrastructure** — রাস্তা, বিদ্যুৎ, পানি সব আছে। C# হলো সেই শহরে চলা গাড়ির একটি model। শহরের infrastructure (CLR, Base Class Library) সব গাড়িকে (language) support করে, কিন্তু যাত্রীরা (developers) নিজের পছন্দের গাড়ি বেছে নিতে পারেন।

**Practical Use Case:**

বাংলাদেশের Brain Station 23, BJIT, Therap Services, DataSoft — এই companies-গুলো .NET দিয়ে enterprise-grade backend systems তৈরি করে। ASP.NET Core দিয়ে REST API, Entity Framework Core দিয়ে Database, Azure দিয়ে Cloud deployment।

**🎤 Interview-style Explanation:**

```
প্রশ্ন: .NET কী এবং এটা কেন ব্যবহার করা হয়?

উত্তর:
.NET হলো Microsoft-এর একটি cross-platform developer platform যেটা দিয়ে
web, mobile, desktop এবং cloud applications তৈরি করা যায়।

এটা ব্যবহার করার কারণ:
1. Cross-platform — Windows, Linux, macOS-এ চলে
2. High performance — ASP.NET Core বিশ্বের fastest web frameworks-এর একটি
3. Strong typing — C# statically typed, runtime errors কম
4. Huge ecosystem — NuGet packages, Microsoft support
5. Enterprise-ready — বড় company-র production system এ ব্যবহার হয়
```

**⚠️ Common Mistakes:**

- .NET আর C# একই মনে করা — .NET হলো platform, C# হলো language
- .NET Framework আর .NET (Core) কে একই মনে করা — দুটো আলাদা
- ".NET is only for Windows" — এটা ভুল, modern .NET cross-platform

**❓ Follow-up Interview Questions:**

1. .NET কোন types of application তৈরিতে ব্যবহার হয়?
2. .NET-এর কোন feature টি আপনার কাছে সবচেয়ে useful মনে হয়?
3. Java আর .NET-এর মধ্যে পার্থক্য কী?

---

<a id="p1-history"></a>
### Topic 2: .NET-এর ইতিহাস

```
Timeline:

2002 → .NET Framework 1.0 release (Windows only)
         C# 1.0, ASP.NET WebForms, ADO.NET

2005 → .NET Framework 2.0
         Generics, Nullable types

2008 → .NET Framework 3.5
         LINQ, Lambda expressions, Extension methods

2010 → .NET Framework 4.0
         Task Parallel Library, dynamic keyword

2016 → .NET Core 1.0 (বিপ্লব!)
         Cross-platform, open-source, high performance
         Linux ও macOS support

2017 → .NET Core 2.0
         Huge performance improvements

2019 → .NET Core 3.0/3.1
         Windows Forms, WPF on Core, gRPC support

2020 → .NET 5 (Unified Platform)
         .NET Framework + .NET Core → একটাই .NET
         Versioning simplified: এখন শুধু ".NET"

2021 → .NET 6 (LTS — Long Term Support)
         Minimal APIs, Hot reload, MAUI preview

2022 → .NET 7
         Performance, Native AOT preview

2023 → .NET 8 (LTS — বর্তমানে most stable)
         Blazor full-stack, Native AOT stable

2024 → .NET 9
         AI integration, performance improvements
```

**মূল পরিবর্তন যা interview-এ আসে:**

| বিষয় | .NET Framework | .NET Core / .NET 5+ |
|-------|---------------|---------------------|
| Platform | Windows only | Cross-platform |
| Open Source | না | হ্যাঁ |
| Performance | Moderate | High |
| Deployment | IIS only | IIS, Kestrel, Docker |
| Future | Legacy | Active development |

**🎤 Interview Tip:**

```
"আমি .NET 6/7/8 নিয়ে কাজ করেছি কারণ এটা LTS version
এবং cross-platform support আছে। .NET Framework-এ legacy
projects maintain করেছি।"
```

---

<a id="p1-versions"></a>
### Topic 3: .NET Framework vs .NET Core vs .NET (5+)

এটা interview-এ সবচেয়ে বেশি জিজ্ঞেস করা প্রশ্নগুলোর একটি।

**বিস্তারিত তুলনা:**

| বৈশিষ্ট্য | .NET Framework | .NET Core | .NET 5+ |
|-----------|---------------|-----------|---------|
| প্রথম release | 2002 | 2016 | 2020 |
| Platform | Windows only | Cross-platform | Cross-platform |
| Open Source | না | হ্যাঁ | হ্যাঁ |
| Performance | Moderate | High | Very High |
| Microservices | কঠিন | সহজ | সহজ |
| Docker support | সীমিত | পূর্ণ | পূর্ণ |
| Side-by-side versions | না | হ্যাঁ | হ্যাঁ |
| WinForms/WPF | হ্যাঁ | .NET Core 3.0+ | হ্যাঁ |
| Supported by Microsoft | Legacy mode | .NET 5+ এ merge | Active |
| কোথায় ব্যবহার | Legacy enterprise apps | New projects | New projects |

**Side-by-side Installation:**

```
.NET Core / .NET 5+ এর একটি বড় সুবিধা হলো একই machine-এ
multiple versions চালানো যায়:

C:\> dotnet --list-runtimes
Microsoft.AspNetCore.App 6.0.20
Microsoft.AspNetCore.App 7.0.10
Microsoft.AspNetCore.App 8.0.0

Project A → .NET 6 ব্যবহার করতে পারে
Project B → .NET 8 ব্যবহার করতে পারে
— কোনো conflict নেই!

.NET Framework-এ এটা সম্ভব ছিল না।
```

**কোনটা কখন ব্যবহার করবেন:**

```
✅ .NET 8 (বা সর্বশেষ LTS) ব্যবহার করুন যদি:
   - নতুন project শুরু করছেন
   - Cross-platform deployment দরকার
   - Docker/Cloud deployment করবেন
   - High performance API দরকার

⚠️ .NET Framework রাখুন যদি:
   - Existing legacy codebase আছে
   - Windows-only dependencies আছে (COM components, Registry access)
   - Migration cost বেশি
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: .NET Framework এবং .NET Core-এর মধ্যে মূল পার্থক্য কী?

উত্তর:
.NET Framework ছিল Windows-only, closed-source এবং শুধু IIS-এ
deploy করা যেত। 2002 সালে শুরু হয়েছিল।

.NET Core 2016 সালে আসে এবং এটা cross-platform — Windows, Linux,
macOS-এ চলে। Open-source এবং Docker-friendly।

2020 সালে .NET 5 দিয়ে দুটো unify হয়ে যায় — এখন শুধু ".NET"
বলা হয়। বর্তমানে .NET 8 সবচেয়ে stable LTS version।

নতুন project-এ আমি .NET 8 ব্যবহার করব কারণ এটা actively
maintained, cross-platform, এবং high performance।
```

---

<a id="p1-clr"></a>
### Topic 4: CLR — Common Language Runtime

**সংজ্ঞা:**

**CLR (Common Language Runtime)** হলো .NET-এর **execution engine** — এটা .NET applications চালানোর জন্য দায়ী। CLR হলো .NET-এর হৃদয়।

CLR কাজ করে:
- Code execute করা
- Memory manage করা (Garbage Collection)
- Type safety নিশ্চিত করা
- Exception handling
- Security enforcement
- Thread management

**Architecture:**

```
┌─────────────────────────────────────────────────┐
│              .NET Application                   │
│    (C# / F# / VB.NET source code)               │
└──────────────────┬──────────────────────────────┘
                   │ Compile করলে
                   ▼
┌─────────────────────────────────────────────────┐
│         IL (Intermediate Language)              │
│              (.dll / .exe file)                 │
└──────────────────┬──────────────────────────────┘
                   │ Runtime-এ
                   ▼
┌─────────────────────────────────────────────────┐
│                   CLR                          │
│  ┌──────────┐  ┌─────────┐  ┌───────────────┐  │
│  │ JIT      │  │   GC    │  │ Exception     │  │
│  │Compiler  │  │(Memory) │  │  Handler      │  │
│  └──────────┘  └─────────┘  └───────────────┘  │
│  ┌──────────┐  ┌─────────┐  ┌───────────────┐  │
│  │ Type     │  │Security │  │   Thread      │  │
│  │ Safety   │  │ Manager │  │  Manager      │  │
│  └──────────┘  └─────────┘  └───────────────┘  │
└──────────────────┬──────────────────────────────┘
                   │
                   ▼
         Native Machine Code
         (CPU execute করে)
```

**🏠 Real-life Analogy:**

CLR হলো একটি **অনুবাদক + manager**। ধরুন আপনি বাংলায় কথা বললেন (C# code লিখলেন), CLR সেটা machine-এর ভাষায় অনুবাদ করে (JIT) এবং সাথে সব resources manage করে — memory পরিষ্কার করা (GC), নিরাপত্তা দেখা (Security), এরর সামলানো (Exception)।

**CLR-এর প্রধান উপাদান:**

```csharp
// CLR কী কী manage করে তার উদাহরণ:

// 1. Memory Management — আপনি new করলেই CLR heap-এ allocate করে
var list = new List<string>(); // CLR heap-এ memory allocate করল

// 2. Type Safety — CLR নিশ্চিত করে type mismatch হবে না
string name = "Rahim";
// int x = name; // CLR এটা allow করবে না — type safety

// 3. Exception Handling — CLR exceptions propagate করে
try
{
    int result = 10 / 0;
}
catch (DivideByZeroException ex)
{
    Console.WriteLine(ex.Message); // CLR exception deliver করল
}

// 4. Garbage Collection — CLR নিজেই memory free করে
// আপনাকে free() বা delete() call করতে হয় না (C/C++ এর মতো)
```

**CLR vs JVM তুলনা (Interview-এ প্রায়ই আসে):**

| বৈশিষ্ট্য | CLR (.NET) | JVM (Java) |
|-----------|-----------|-----------|
| Language | C#, F#, VB.NET | Java, Kotlin, Scala |
| Intermediate Code | IL (MSIL) | Bytecode |
| Compilation | JIT | JIT |
| Memory Model | Generational GC | Generational GC |
| Cross-platform | .NET Core থেকে | সবসময় |
| Native Interop | P/Invoke | JNI |

**🎤 Interview-style Explanation:**

```
প্রশ্ন: CLR কী এবং এটা কীভাবে কাজ করে?

উত্তর:
CLR মানে Common Language Runtime — এটা .NET-এর execution
engine। আমরা যে C# code লিখি সেটা সরাসরি machine code হয় না,
প্রথমে IL (Intermediate Language) এ compile হয়।

Runtime-এ CLR সেই IL code কে JIT compiler দিয়ে native
machine code-এ convert করে execute করে।

CLR-এর কাজ:
1. JIT Compilation — IL → Machine Code
2. Garbage Collection — unused memory automatically free করা
3. Type Safety — invalid type conversion prevent করা
4. Exception Handling — exceptions properly propagate করা
5. Security — code permission check করা

এটা Java-র JVM-এর মতো কাজ করে — দুটোই managed runtime।
```

**⚠️ Common Mistakes:**

- CLR আর JIT কে একই মনে করা — JIT হলো CLR-এর একটি component
- "CLR শুধু Windows-এ চলে" — .NET Core/5+ এ CLR cross-platform
- CLR আর .NET কে একই মনে করা — CLR হলো .NET-এর একটি অংশ

---

<a id="p1-cts"></a>
### Topic 5: CTS — Common Type System

**সংজ্ঞা:**

**CTS (Common Type System)** হলো .NET-এর type system — যা define করে কীভাবে types declare, use, এবং manage করতে হবে CLR-এ।

CTS নিশ্চিত করে যে C# এ লেখা `int` আর VB.NET-এ লেখা `Integer` একই underlying type (`System.Int32`) — যাতে আলাদা .NET languages একে অপরের সাথে কাজ করতে পারে।

**CTS-এর Type Hierarchy:**

```
System.Object (সব type এর root)
├── Value Types (Stack-এ store হয়)
│   ├── Built-in Value Types
│   │   ├── System.Int32  (int)
│   │   ├── System.Int64  (long)
│   │   ├── System.Double (double)
│   │   ├── System.Boolean (bool)
│   │   ├── System.Char   (char)
│   │   └── System.Decimal (decimal)
│   ├── Struct (user-defined value type)
│   └── Enum
└── Reference Types (Heap-এ store হয়)
    ├── Class
    ├── Interface
    ├── Delegate
    ├── Array
    └── String
```

**Value Type vs Reference Type — সবচেয়ে গুরুত্বপূর্ণ পার্থক্য:**

```csharp
// ─────────────────────────────────────
// VALUE TYPE — Stack-এ store হয়
// Copy হলে নতুন copy তৈরি হয়
// ─────────────────────────────────────
int a = 10;
int b = a;   // b হলো a-এর copy
b = 20;
Console.WriteLine(a); // 10 — a অপরিবর্তিত
Console.WriteLine(b); // 20

// ─────────────────────────────────────
// REFERENCE TYPE — Heap-এ store হয়
// Copy হলে একই object-এর reference copy হয়
// ─────────────────────────────────────
int[] arr1 = { 1, 2, 3 };
int[] arr2 = arr1;  // arr2 হলো arr1-এর reference
arr2[0] = 99;
Console.WriteLine(arr1[0]); // 99 — arr1 ও পরিবর্তিত!
Console.WriteLine(arr2[0]); // 99

// ─────────────────────────────────────
// STRUCT — Value Type (user-defined)
// ─────────────────────────────────────
struct Point
{
    public int X;
    public int Y;
}

Point p1 = new Point { X = 1, Y = 2 };
Point p2 = p1;  // copy হয়
p2.X = 99;
Console.WriteLine(p1.X); // 1 — p1 অপরিবর্তিত
```

**Type Mapping — Language থেকে CTS:**

| C# Alias | CTS Type | Size | Range |
|----------|----------|------|-------|
| `int` | `System.Int32` | 4 bytes | -2B to 2B |
| `long` | `System.Int64` | 8 bytes | -9.2×10¹⁸ to 9.2×10¹⁸ |
| `double` | `System.Double` | 8 bytes | ±5.0×10⁻³²⁴ to ±1.7×10³⁰⁸ |
| `decimal` | `System.Decimal` | 16 bytes | ±1.0×10⁻²⁸ to ±7.9×10²⁸ |
| `bool` | `System.Boolean` | 1 byte | true/false |
| `char` | `System.Char` | 2 bytes | Unicode |
| `string` | `System.String` | Variable | Unicode text |
| `object` | `System.Object` | Variable | Any type |

**🎤 Interview-style Explanation:**

```
প্রশ্ন: CTS কী? Value Type আর Reference Type-এর পার্থক্য কী?

উত্তর:
CTS মানে Common Type System। এটা .NET-এর type system যা
define করে কীভাবে types define ও use হবে।

সবচেয়ে গুরুত্বপূর্ণ concept হলো Value Type vs Reference Type:

Value Type (int, bool, struct, enum) — Stack-এ store হয়।
Assignment করলে new copy তৈরি হয়। Fast।

Reference Type (class, array, string, delegate) — Heap-এ
store হয়। Assignment করলে reference copy হয়, data নয়।

এটা জানা important কারণ এটা না জানলে subtle bugs হয় —
যেমন reference type copy করে modify করলে original-ও
change হয়ে যায়।
```

---

<a id="p1-cls"></a>
### Topic 6: CLS — Common Language Specification

**সংজ্ঞা:**

**CLS (Common Language Specification)** হলো .NET languages-এর জন্য একটি **minimum set of rules/features** — যা follow করলে সব .NET languages একে অপরের সাথে interoperate করতে পারে।

সহজ কথায়: CLS হলো চুক্তি — "যদি তুমি CLS follow কর, তাহলে তোমার code সব .NET languages থেকে ব্যবহার করা যাবে।"

**CLS Rules (গুরুত্বপূর্ণ কিছু):**

```
✅ CLS-compliant:
   - Public methods-এর names case-insensitive unique হতে হবে
   - Public API-তে unsigned types (uint, ulong) ব্যবহার করা যাবে না
   - Pointer types use করা যাবে না public API-তে
   - Method overloading শুধু parameter type/count-এ হবে
   - Exception class System.Exception থেকে inherit করতে হবে

❌ CLS non-compliant উদাহরণ:
```

```csharp
// ❌ CLS non-compliant — uint (unsigned) public API-তে
public void ProcessData(uint count) { } // VB.NET-এ সমস্যা

// ✅ CLS compliant — int ব্যবহার করুন
public void ProcessData(int count) { }

// ❌ CLS non-compliant — case শুধু আলাদা করে দুই method
public void Calculate() { }
public void calculate() { } // VB.NET case-insensitive, সমস্যা!

// CLSCompliant attribute দিয়ে enforce করুন:
[assembly: CLSCompliant(true)]
public class MyLibrary
{
    // এখন CLS violations build error দেবে
}
```

**CTS vs CLS সম্পর্ক:**

```
CTS ⊃ CLS

CTS = সব possible types ও rules (বড় set)
CLS = CTS-এর subset যা সব languages support করে

Analogy:
CTS = বাংলাদেশের সব আইন
CLS = UN-এর common international rules যা সবাই follow করে
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: CLS কী এবং কেন প্রয়োজন?

উত্তর:
CLS মানে Common Language Specification। .NET-এ C#, F#,
VB.NET ইত্যাদি আলাদা languages আছে। CLS হলো minimum rules
যা follow করলে সব language থেকে সেই code ব্যবহার করা যাবে।

উদাহরণ: C#-এ লেখা class library যদি CLS-compliant হয়,
তাহলে VB.NET project থেকেও সেই library use করা যাবে।

Public API design করার সময় CLS follow করা important — এতে
interoperability নিশ্চিত হয়।
```

---

<a id="p1-jit"></a>
### Topic 7: JIT Compiler

**সংজ্ঞা:**

**JIT (Just-In-Time) Compiler** হলো CLR-এর একটি component যা IL (Intermediate Language) code কে runtime-এ native machine code-এ convert করে।

"Just-In-Time" মানে ঠিক যখন দরকার, তখনই compile করা — আগে থেকে সব compile না করে।

**Compilation Flow:**

```
C# Source Code (.cs)
        │
        ▼  [C# Compiler — csc.exe / Roslyn]
        │
IL Code (.dll / .exe এর ভেতরে)
        │
        ▼  [JIT Compiler — Runtime-এ]
        │
Native Machine Code (x64/x86/ARM)
        │
        ▼
CPU Execute করে
```

**JIT-এর প্রকারভেদ:**

```
1. Standard JIT (Normal JIT):
   - Method প্রথমবার call হলে compile করে
   - Compiled code cache করে রাখে
   - পরের বার same method → cached code use করে
   - সবচেয়ে common

2. Pre-JIT (NGEN / Native AOT):
   - Application install-এর সময় সব code compile করে
   - Startup faster, কিন্তু memory বেশি
   - .NET 8-এ Native AOT: সব IL কে আগেই native compile করে

3. Econo-JIT (আর ব্যবহার হয় না):
   - Resource-constrained devices-এ ছিল
```

**JIT Optimization — Interview-এ জিজ্ঞেস করা হয়:**

```csharp
// JIT এই optimizations করে:

// 1. Inlining — ছোট method-এর body সরাসরি call site-এ paste করে
[MethodImpl(MethodImplOptions.AggressiveInlining)]
private static int Add(int a, int b) => a + b;
// JIT এটাকে inline করবে — method call overhead নেই

// 2. Dead code elimination
bool debug = false;
if (debug)
{
    Console.WriteLine("Debug"); // JIT এই block remove করে দেয়
}

// 3. Loop unrolling — loop কে unfold করে performance বাড়ায়
// 4. Register allocation — variables CPU registers-এ রাখে
```

**Warm-up vs Cold Start:**

```
Cold Start: Application প্রথমবার চালু হলে
→ JIT সব code compile করে
→ প্রথম request slow

Warm-up: Application কিছুক্ষণ চললে
→ Frequently used code compiled ও cached
→ Subsequent requests fast

Production solution: 
→ Startup-এ key endpoints-এ dummy requests পাঠান
→ .NET 8 Native AOT দিয়ে pre-compile করুন
→ ReadyToRun (R2R) compilation ব্যবহার করুন
```

**AOT vs JIT (Modern .NET):**

| বৈশিষ্ট্য | JIT | Native AOT (.NET 8) |
|-----------|-----|---------------------|
| Compilation time | Runtime | Build time |
| Startup | Slower | Very fast |
| Memory | IL + Native | Only native |
| Optimization | Runtime adaptive | Build-time static |
| Platform | Any | Platform-specific |
| Use case | Most apps | Microservices, CLI tools |

**🎤 Interview-style Explanation:**

```
প্রশ্ন: JIT Compiler কী এবং কীভাবে কাজ করে?

উত্তর:
JIT মানে Just-In-Time Compiler। C# code প্রথমে IL
(Intermediate Language) এ compile হয়। যখন application
run করে, CLR-এর JIT compiler সেই IL কে real-time-এ
native machine code-এ convert করে।

"Just-In-Time" মানে ঠিক যখন কোনো method প্রথমবার call
হয়, তখনই সেটা compile হয় এবং cache হয়। পরের বার সেই
method আবার call হলে cached native code সরাসরি run করে।

এর সুবিধা: runtime-এ hardware-specific optimization করা যায়।
এর অসুবিধা: cold start slow — কারণ প্রথমবার compile করতে সময় লাগে।

.NET 8-এ Native AOT দিয়ে এই সমস্যা solve করা যায়।
```

---

<a id="p1-managed"></a>
### Topic 8: Managed vs Unmanaged Code

**সংজ্ঞা:**

**Managed Code:** যে code CLR-এর control-এ চলে। Memory management, type safety, exception handling — সব CLR করে। C# code হলো managed code।

**Unmanaged Code:** যে code CLR-এর বাইরে চলে। Developer নিজে memory manage করেন। C, C++ code হলো unmanaged।

**পার্থক্য:**

| বৈশিষ্ট্য | Managed Code | Unmanaged Code |
|-----------|-------------|----------------|
| Memory management | CLR/GC করে | Developer করেন |
| Memory leak risk | কম | বেশি |
| Type safety | CLR enforce করে | নেই |
| Performance | Slight overhead | Direct hardware access |
| Language | C#, VB.NET, F# | C, C++, Assembly |
| Pointer | সীমিত (unsafe) | সরাসরি |
| Example | ASP.NET Core app | Win32 API, COM |

```csharp
// ──────────────────────────────
// MANAGED CODE (সাধারণ C#)
// ──────────────────────────────
class ManagedExample
{
    public void Run()
    {
        // Memory CLR manage করে — আপনাকে free করতে হবে না
        var list = new List<int>();
        list.Add(1);
        list.Add(2);
        // list out of scope হলে GC automatically free করবে
    }
}

// ──────────────────────────────────────────────────
// UNMANAGED CODE — unsafe block দিয়ে C# এ pointer
// ──────────────────────────────────────────────────
class UnmanagedExample
{
    public unsafe void UsePointer()
    {
        int value = 42;
        int* ptr = &value;    // pointer — unmanaged style
        Console.WriteLine(*ptr); // 42
        // এখানে developer নিজে সাবধান থাকতে হবে
    }
}

// ──────────────────────────────────────────────────
// P/Invoke — Managed code থেকে Unmanaged (C/Win32) call
// ──────────────────────────────────────────────────
using System.Runtime.InteropServices;

class PInvokeExample
{
    // Windows API function call করা
    [DllImport("user32.dll", CharSet = CharSet.Unicode)]
    static extern int MessageBox(IntPtr hWnd, string text, string caption, uint type);

    public void ShowMessage()
    {
        MessageBox(IntPtr.Zero, "Hello from C#!", "Title", 0);
    }
}
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: Managed code কী? Unmanaged code কী?

উত্তর:
Managed code হলো সেই code যা CLR-এর supervision-এ চলে।
C# লিখলে সেটা managed code। CLR memory manage করে,
type safety enforce করে, exceptions handle করে।

Unmanaged code হলো CLR-এর বাইরে — যেমন C/C++ code।
Developer নিজে malloc/free বা new/delete করেন।
Memory leak, buffer overflow-এর risk বেশি।

C# থেকে P/Invoke দিয়ে unmanaged Windows API বা
C library call করা যায়। যেমন native file dialog
বা GPU programming-এ দরকার হয়।
```

---

<a id="p1-il"></a>
### Topic 9: IL — Intermediate Language

**সংজ্ঞা:**

**IL (Intermediate Language)** — Microsoft Intermediate Language (MSIL) বা Common Intermediate Language (CIL) নামেও পরিচিত — হলো CPU-independent instruction set যেখানে C# code প্রথমে compile হয়।

IL হলো .NET-এর "middle step" — source code (C#) আর native machine code (x64) এর মাঝামাঝি।

**কেন IL দরকার:**

```
একটি IL ফাইল (.dll) → যেকোনো platform-এ চলতে পারে
কারণ প্রতিটি platform-এর নিজস্ব CLR/JIT আছে
যা সেই platform-এর জন্য IL কে native code-এ convert করে

Windows x64:  IL → x64 machine code
Linux ARM64:  IL → ARM64 machine code
macOS x64:    IL → x64 machine code
```

**IL দেখার উপায়:**

```csharp
// এই C# code লিখুন:
public class Calculator
{
    public int Add(int a, int b)
    {
        return a + b;
    }
}
```

```il
// IL output (ildasm.exe বা dotnet-ildasm দিয়ে দেখুন):
.method public hidebysig instance int32
    Add(int32 a, int32 b) cil managed
{
    .maxstack  2
    IL_0000:  ldarg.1      // a load করো
    IL_0001:  ldarg.2      // b load করো
    IL_0002:  add          // যোগ করো
    IL_0003:  ret          // return করো
}
```

**IL দেখার tool:**

```bash
# .NET SDK install থাকলে:
dotnet tool install -g dotnet-ildasm

# অথবা ILSpy (GUI tool) — ildasm.exe alternative
# Visual Studio-তে: View → Other Windows → IL Disassembler
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: IL বা MSIL কী?

উত্তর:
IL মানে Intermediate Language। যখন C# code compile হয়,
সরাসরি machine code হয় না — প্রথমে IL-এ convert হয়।
IL হলো CPU-independent bytecode।

Runtime-এ CLR-এর JIT compiler এই IL কে target
platform-এর native machine code-এ convert করে।

এটার সুবিধা হলো platform independence —
একই .dll file Windows, Linux, macOS সব জায়গায় চলে।
প্রতিটি platform-এর নিজস্ব JIT সেই IL execute করে।

Java-র bytecode-এর সাথে concept একই।
```

---

<a id="p1-gc"></a>
### Topic 10: Garbage Collection (GC)

**সংজ্ঞা:**

**Garbage Collection (GC)** হলো CLR-এর automatic memory management system। এটা heap থেকে আর ব্যবহার না হওয়া objects-এর memory automatically free করে।

C/C++-এ developer নিজে `free()`/`delete` করেন। C#-এ CLR-এর GC নিজেই করে।

**Heap Memory — Generation Model:**

```
.NET GC তিনটি "Generation" ব্যবহার করে:

┌─────────────────────────────────────────────────────────┐
│                      Managed Heap                       │
├───────────────┬───────────────┬─────────────────────────┤
│  Generation 0 │  Generation 1 │     Generation 2        │
│  (Gen 0)      │  (Gen 1)      │     (Gen 2)             │
│  Short-lived  │  Medium-lived │     Long-lived          │
│  ~256 KB      │  ~2 MB        │     Unlimited           │
├───────────────┴───────────────┴─────────────────────────┤
│                   Large Object Heap (LOH)               │
│                   (>85,000 bytes objects)               │
└─────────────────────────────────────────────────────────┘
```

**GC কীভাবে কাজ করে:**

```
1. Allocation:
   new Object() → Gen 0 heap-এ allocate হয়

2. Gen 0 Collection (সবচেয়ে frequent):
   → Gen 0 full হলে GC trigger হয়
   → জীবিত objects Gen 1-এ promote হয়
   → মৃত objects এর memory reclaim হয়

3. Gen 1 Collection (কম frequent):
   → Gen 1 full হলে
   → জীবিত objects Gen 2-এ promote হয়

4. Gen 2 Collection (Full GC — সবচেয়ে ব্যয়বহুল):
   → সব generations collect করে
   → Application pause হয় (Stop-the-World)

মূল নীতি: "Short-lived objects বেশি, long-lived কম"
বেশিরভাগ objects Gen 0-তেই মারা যায় — এটা GC-কে fast রাখে
```

**GC Roots — কোন objects "জীবিত":**

```
GC কীভাবে বোঝে কোন object আর দরকার নেই?
→ GC Roots থেকে reachable কিনা check করে

GC Roots:
- Stack variables (local variables, parameters)
- Static variables
- CPU registers
- GC Handles

যদি কোনো object কোনো root থেকে reachable না হয়
→ সেটা "garbage" — collect করা হবে
```

**Code Example:**

```csharp
// ──────────────────────────────────
// GC Basics
// ──────────────────────────────────
class GCDemo
{
    public void BasicGC()
    {
        // Gen 0 তে allocate হয়
        var obj1 = new byte[1000];
        var obj2 = new string("Hello");

        // obj1 = null; // এখন obj1 reachable নয় → garbage

        // Explicitly GC চালাতে পারেন (production-এ avoid করুন)
        GC.Collect();

        Console.WriteLine($"Gen of obj2: {GC.GetGeneration(obj2)}");
    }
}

// ──────────────────────────────────────────────────
// IDisposable — Unmanaged resources manual cleanup
// ──────────────────────────────────────────────────
class DatabaseConnection : IDisposable
{
    private bool _disposed = false;
    private IntPtr _nativeHandle; // unmanaged resource

    public void Query() { /* DB query */ }

    public void Dispose()
    {
        Dispose(true);
        GC.SuppressFinalize(this); // GC কে বলছি finalizer run করতে হবে না
    }

    protected virtual void Dispose(bool disposing)
    {
        if (!_disposed)
        {
            if (disposing)
            {
                // managed resources cleanup
            }
            // unmanaged resources cleanup
            // CloseHandle(_nativeHandle);
            _disposed = true;
        }
    }
}

// using statement — scope শেষে automatically Dispose() call হয়
void UseConnection()
{
    using var conn = new DatabaseConnection();
    conn.Query();
} // এখানে conn.Dispose() automatically call হয়

// ──────────────────────────────────────────
// Large Object Heap (LOH) — 85KB+ objects
// ──────────────────────────────────────────
void LOHExample()
{
    // 85000 bytes এর বেশি → LOH-এ যাবে
    var largeArray = new byte[100_000]; // LOH
    var smallArray = new byte[1_000];   // Gen 0
}
```

**GC Pressure — Performance Interview Question:**

```csharp
// ❌ GC Pressure বাড়ায় — বেশি allocation, বেশি GC
void HighGCPressure()
{
    for (int i = 0; i < 100000; i++)
    {
        var temp = new StringBuilder(); // প্রতি iteration নতুন object
        temp.Append("Hello " + i);      // string concatenation = allocation
    }
}

// ✅ GC Pressure কমায় — reuse, pool, struct
void LowGCPressure()
{
    var sb = new StringBuilder(); // একটাই object, reuse করা হচ্ছে
    for (int i = 0; i < 100000; i++)
    {
        sb.Clear();
        sb.Append("Hello ");
        sb.Append(i);
    }
}

// ArrayPool — array reuse করে allocation কমায়
using System.Buffers;

void UseArrayPool()
{
    var pool = ArrayPool<byte>.Shared;
    byte[] buffer = pool.Rent(1024); // pool থেকে নিন
    try
    {
        // buffer use করুন
    }
    finally
    {
        pool.Return(buffer); // pool-এ ফেরত দিন
    }
}
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: Garbage Collection কী? কীভাবে কাজ করে?

উত্তর:
GC হলো CLR-এর automatic memory management। C#-এ
যখন new করি তখন heap-এ object allocate হয়। যখন
সেই object আর কোনো variable reference না করে,
তখন GC সেটা automatically free করে।

GC Generational model ব্যবহার করে — Gen 0, Gen 1, Gen 2।
নতুন objects Gen 0-তে যায়। Gen 0 full হলে GC run করে।
বেঁচে থাকা objects Gen 1-এ move করে।

Performance tip: বেশি short-lived object তৈরি করলে GC
বেশি কাজ করে। StringBuilder, ArrayPool, object pooling
দিয়ে GC pressure কমানো যায়।

Unmanaged resources (file handle, DB connection) এর জন্য
IDisposable implement করতে হয় এবং using statement
ব্যবহার করতে হয়।
```

**⚠️ Common Mistakes:**

```csharp
// ❌ Memory leak — event handler unsubscribe করা হয়নি
class Publisher
{
    public event EventHandler DataChanged;
}

class Subscriber
{
    private Publisher _pub;
    public Subscriber(Publisher pub)
    {
        _pub = pub;
        _pub.DataChanged += OnDataChanged; // subscribe
        // কিন্তু কখনো unsubscribe করা হয়নি
        // Subscriber কখনো GC হবে না!
    }
    private void OnDataChanged(object s, EventArgs e) { }

    // ✅ Fix: IDisposable implement করুন
    public void Dispose()
    {
        _pub.DataChanged -= OnDataChanged; // unsubscribe
    }
}
```

---

<a id="p1-assemblies"></a>
### Topic 11: Assemblies

**সংজ্ঞা:**

**Assembly** হলো .NET-এর deployment ও versioning unit। এটা হয় `.dll` (class library) বা `.exe` (executable application) ফাইল।

Assembly-তে থাকে:
- IL code
- Metadata (types, methods, properties সম্পর্কে তথ্য)
- Manifest (assembly identity, dependencies)
- Resources (images, strings, etc.)

**Assembly-র প্রকারভেদ:**

```
1. Private Assembly:
   - শুধু একটি application ব্যবহার করে
   - Application folder-এ থাকে
   - সবচেয়ে সাধারণ

2. Shared Assembly (GAC — Global Assembly Cache):
   - Multiple applications share করে
   - Strong name দরকার (digitally signed)
   - GAC-এ install করতে হয়
   - উদাহরণ: .NET Framework's mscorlib.dll

3. Satellite Assembly:
   - Localization/resource ধারণ করে
   - Culture-specific strings, images
   - Main assembly-র পাশে culture folder-এ থাকে
```

**Assembly Structure:**

```
MyApp.dll
├── Manifest
│   ├── Assembly name: MyApp
│   ├── Version: 1.0.0.0
│   ├── Culture: neutral
│   ├── Public key token: null (unsigned)
│   └── Dependencies: System.dll, Newtonsoft.Json.dll
├── Type Metadata
│   ├── Class: CustomerService
│   │   ├── Method: GetCustomer(int id)
│   │   └── Method: CreateCustomer(Customer c)
│   └── Class: ProductRepository
└── IL Code
    └── (actual method implementations)
```

**Assembly দেখার Tool:**

```bash
# dotnet CLI দিয়ে
dotnet tool install -g dotnet-ildasm

# ILSpy (GUI) — সবচেয়ে popular
# https://github.com/icsharpcode/ILSpy

# Reflector, dnSpy — alternatives
```

```csharp
// Runtime-এ Assembly information পড়া
using System.Reflection;

var assembly = Assembly.GetExecutingAssembly();
Console.WriteLine($"Name: {assembly.GetName().Name}");
Console.WriteLine($"Version: {assembly.GetName().Version}");
Console.WriteLine($"Location: {assembly.Location}");

// সব types list করা
foreach (var type in assembly.GetTypes())
{
    Console.WriteLine(type.FullName);
}

// Runtime-এ Assembly load করা (Plugin system)
var pluginAssembly = Assembly.LoadFrom("MyPlugin.dll");
var pluginType = pluginAssembly.GetType("MyPlugin.PluginClass");
var plugin = Activator.CreateInstance(pluginType);
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: Assembly কী?

উত্তর:
Assembly হলো .NET-এর deployment unit। C# project compile
করলে .dll বা .exe ফাইল তৈরি হয় — এটাই Assembly।

Assembly-তে IL code, type metadata, এবং manifest থাকে।
Manifest-এ assembly-র name, version, এবং dependencies
লেখা থাকে।

Private assembly শুধু একটি app ব্যবহার করে। Shared assembly
GAC-এ install করে multiple apps share করে।

Reflection দিয়ে runtime-এ assembly load করে plugins
তৈরি করা যায়।
```

---

<a id="p1-nuget"></a>
### Topic 12: NuGet Packages

**সংজ্ঞা:**

**NuGet** হলো .NET-এর official package manager। Third-party libraries install, update, remove করার জন্য। npm (Node.js), pip (Python) এর মতো .NET-এর জন্য।

**NuGet.org** — সব public packages এখানে: https://www.nuget.org

**Daily Use Commands:**

```bash
# Package install করা
dotnet add package Newtonsoft.Json
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Serilog.AspNetCore

# Specific version install
dotnet add package Newtonsoft.Json --version 13.0.3

# Package remove করা
dotnet remove package Newtonsoft.Json

# সব packages update করা
dotnet update

# Install করা packages list দেখা
dotnet list package

# Outdated packages দেখা
dotnet list package --outdated

# NuGet source থেকে restore করা
dotnet restore
```

**.csproj ফাইলে PackageReference:**

```xml
<!-- MyProject.csproj -->
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>net8.0</TargetFramework>
  </PropertyGroup>

  <ItemGroup>
    <!-- NuGet packages -->
    <PackageReference Include="Microsoft.EntityFrameworkCore" Version="8.0.0" />
    <PackageReference Include="Microsoft.EntityFrameworkCore.SqlServer" Version="8.0.0" />
    <PackageReference Include="Serilog.AspNetCore" Version="8.0.0" />
    <PackageReference Include="Newtonsoft.Json" Version="13.0.3" />
    <PackageReference Include="Swashbuckle.AspNetCore" Version="6.5.0" />
  </ItemGroup>
</Project>
```

**Bangladeshi Projects-এ সবচেয়ে বেশি ব্যবহৃত NuGet packages:**

| Package | কাজ |
|---------|-----|
| `Microsoft.EntityFrameworkCore` | ORM — Database access |
| `Microsoft.EntityFrameworkCore.SqlServer` | SQL Server provider |
| `Serilog.AspNetCore` | Structured logging |
| `AutoMapper` | Object mapping |
| `FluentValidation` | Input validation |
| `Swashbuckle.AspNetCore` | Swagger/OpenAPI docs |
| `Microsoft.AspNetCore.Authentication.JwtBearer` | JWT authentication |
| `BCrypt.Net-Next` | Password hashing |
| `Newtonsoft.Json` | JSON serialization |
| `Dapper` | Micro-ORM |

**নিজের NuGet Package তৈরি:**

```bash
# Pack করুন
dotnet pack --configuration Release

# NuGet.org-এ publish করুন
dotnet nuget push ./bin/Release/MyPackage.1.0.0.nupkg \
  --api-key YOUR_API_KEY \
  --source https://api.nuget.org/v3/index.json
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: NuGet কী?

উত্তর:
NuGet হলো .NET-এর package manager — JavaScript-এর npm বা
Python-এর pip-এর মতো। Third-party libraries আমাদের project-এ
add করার জন্য।

dotnet add package দিয়ে install করা হয়। এটা .csproj ফাইলে
PackageReference হিসেবে যোগ হয় এবং NuGet.org থেকে
download হয়।

আমি projects-এ EF Core, Serilog, AutoMapper, JWT Bearer,
FluentValidation ইত্যাদি packages ব্যবহার করেছি।
```

---

<a id="p1-sdk-runtime"></a>
### Topic 13: SDK vs Runtime

**সংজ্ঞা:**

**Runtime:** শুধু .NET application run করার জন্য। End user-দের machine-এ install করা হয়। Compile করার capability নেই।

**SDK (Software Development Kit):** Development-এর জন্য। Runtime + Compiler + CLI tools + Build tools সব একসাথে। Developer machine-এ install করা হয়।

**পার্থক্য:**

| বৈশিষ্ট্য | Runtime | SDK |
|-----------|---------|-----|
| কাজ | App চালানো | App develop ও build করা |
| Include করে | CLR, Base libraries | Runtime + Compiler + CLI + Build tools |
| Size | Smaller (~30MB) | Larger (~200MB) |
| কার জন্য | End users, Servers | Developers |
| Build করতে পারে? | না | হ্যাঁ |

**কোথায় কোনটা install করবেন:**

```
Developer machine → SDK install করুন (এটা Runtime-ও include করে)
Production server → Runtime install করুন (app শুধু run করে)
Docker image → 
  Build stage: SDK image (microsoft/dotnet-sdk)
  Final stage: Runtime image (microsoft/dotnet-aspnet)
```

**Dockerfile-এ পার্থক্য:**

```dockerfile
# ──────────────────────────────────────────────────────
# Multi-stage Dockerfile — Best Practice
# ──────────────────────────────────────────────────────

# Stage 1: Build — SDK image ব্যবহার করুন
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src
COPY *.csproj .
RUN dotnet restore
COPY . .
RUN dotnet publish -c Release -o /app/publish

# Stage 2: Run — Runtime image ব্যবহার করুন (smaller!)
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS final
WORKDIR /app
COPY --from=build /app/publish .
ENTRYPOINT ["dotnet", "MyApp.dll"]

# SDK image: ~700MB
# ASP.NET Runtime image: ~200MB
# Final image অনেক ছোট!
```

**dotnet CLI — SDK-এর প্রধান tool:**

```bash
# Version check
dotnet --version           # SDK version
dotnet --list-sdks         # installed SDKs
dotnet --list-runtimes     # installed runtimes

# Project create
dotnet new webapi -n MyApi
dotnet new console -n MyConsole
dotnet new classlib -n MyLibrary

# Build & Run
dotnet build
dotnet run
dotnet watch run    # Hot reload

# Publish
dotnet publish -c Release -r linux-x64 --self-contained
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: .NET SDK আর Runtime-এর পার্থক্য কী?

উত্তর:
SDK হলো developer-এর tool — এতে compiler, CLI, build tools
সব আছে এবং Runtime-ও include করে।

Runtime শুধু application run করার জন্য — compile করতে পারে না।

Production server-এ আমরা শুধু Runtime install করি — কারণ
application আগেই compiled। Developer machine-এ SDK install করি।

Docker-এ multi-stage build ব্যবহার করি — build stage-এ SDK image,
final stage-এ Runtime image। এতে production image অনেক ছোট হয়।
```

---

<a id="p1-structure"></a>
### Topic 14: Solution & Project Structure

**.NET Solution Structure:**

```
MyCompany.sln                          ← Solution file (সব projects এর container)
├── src/
│   ├── MyCompany.API/                 ← ASP.NET Core Web API project
│   │   ├── Controllers/
│   │   ├── Middleware/
│   │   ├── Program.cs
│   │   └── MyCompany.API.csproj
│   ├── MyCompany.Application/         ← Business Logic (Use Cases)
│   │   ├── Services/
│   │   ├── DTOs/
│   │   ├── Interfaces/
│   │   └── MyCompany.Application.csproj
│   ├── MyCompany.Domain/              ← Entities, Domain Models
│   │   ├── Entities/
│   │   ├── Enums/
│   │   └── MyCompany.Domain.csproj
│   └── MyCompany.Infrastructure/      ← EF Core, External Services
│       ├── Data/
│       ├── Repositories/
│       └── MyCompany.Infrastructure.csproj
└── tests/
    ├── MyCompany.UnitTests/
    └── MyCompany.IntegrationTests/
```

**একটি ASP.NET Core Project-এর ভেতরের Structure:**

```
MyCompany.API/
├── Controllers/
│   ├── CustomersController.cs
│   ├── ProductsController.cs
│   └── AuthController.cs
├── Middleware/
│   ├── ExceptionHandlingMiddleware.cs
│   └── RequestLoggingMiddleware.cs
├── Extensions/
│   └── ServiceCollectionExtensions.cs
├── appsettings.json           ← Configuration (Development)
├── appsettings.Development.json
├── appsettings.Production.json
├── Program.cs                 ← Application entry point
└── MyCompany.API.csproj       ← Project file
```

**Program.cs — .NET 6+ Minimal Hosting:**

```csharp
// Program.cs — .NET 6/7/8 এর minimal hosting model
var builder = WebApplication.CreateBuilder(args);

// Services register করুন
builder.Services.AddControllers();
builder.Services.AddEndpointsApiExplorer();
builder.Services.AddSwaggerGen();

// Database
builder.Services.AddDbContext<AppDbContext>(options =>
    options.UseSqlServer(builder.Configuration.GetConnectionString("Default")));

// Custom services
builder.Services.AddScoped<ICustomerService, CustomerService>();
builder.Services.AddScoped<ICustomerRepository, CustomerRepository>();

// Authentication
builder.Services.AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
    .AddJwtBearer(/* config */);

var app = builder.Build();

// Middleware pipeline
if (app.Environment.IsDevelopment())
{
    app.UseSwagger();
    app.UseSwaggerUI();
}

app.UseHttpsRedirection();
app.UseAuthentication();
app.UseAuthorization();
app.MapControllers();

app.Run();
```

**appsettings.json Structure:**

```json
{
  "ConnectionStrings": {
    "Default": "Server=localhost;Database=MyDb;Trusted_Connection=True;"
  },
  "JwtSettings": {
    "Secret": "your-super-secret-key-minimum-32-characters",
    "Issuer": "MyCompany.API",
    "Audience": "MyCompany.Client",
    "ExpiryMinutes": 60
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}
```

**.csproj File — Project Configuration:**

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">

  <PropertyGroup>
    <TargetFramework>net8.0</TargetFramework>
    <Nullable>enable</Nullable>
    <ImplicitUsings>enable</ImplicitUsings>
    <RootNamespace>MyCompany.API</RootNamespace>
  </PropertyGroup>

  <ItemGroup>
    <!-- Project references -->
    <ProjectReference Include="..\MyCompany.Application\MyCompany.Application.csproj" />
    <ProjectReference Include="..\MyCompany.Infrastructure\MyCompany.Infrastructure.csproj" />
  </ItemGroup>

  <ItemGroup>
    <!-- NuGet packages -->
    <PackageReference Include="Microsoft.AspNetCore.Authentication.JwtBearer" Version="8.0.0" />
    <PackageReference Include="Swashbuckle.AspNetCore" Version="6.5.0" />
    <PackageReference Include="Serilog.AspNetCore" Version="8.0.0" />
  </ItemGroup>

</Project>
```

**Multi-project Solution তৈরি:**

```bash
# Solution তৈরি
dotnet new sln -n MyCompany

# Projects তৈরি
dotnet new webapi -n MyCompany.API -o src/MyCompany.API
dotnet new classlib -n MyCompany.Application -o src/MyCompany.Application
dotnet new classlib -n MyCompany.Domain -o src/MyCompany.Domain
dotnet new classlib -n MyCompany.Infrastructure -o src/MyCompany.Infrastructure
dotnet new xunit -n MyCompany.UnitTests -o tests/MyCompany.UnitTests

# Solution-এ projects add করা
dotnet sln add src/MyCompany.API/MyCompany.API.csproj
dotnet sln add src/MyCompany.Application/MyCompany.Application.csproj
dotnet sln add src/MyCompany.Domain/MyCompany.Domain.csproj
dotnet sln add src/MyCompany.Infrastructure/MyCompany.Infrastructure.csproj
dotnet sln add tests/MyCompany.UnitTests/MyCompany.UnitTests.csproj

# Project references add করা
dotnet add src/MyCompany.API reference src/MyCompany.Application/MyCompany.Application.csproj
dotnet add src/MyCompany.Infrastructure reference src/MyCompany.Domain/MyCompany.Domain.csproj
```

**🎤 Interview-style Explanation:**

```
প্রশ্ন: .NET Solution ও Project structure কীভাবে organize করেন?

উত্তর:
আমি Layered/Clean Architecture follow করি:

Solution-এর মধ্যে চারটি প্রধান project:
1. Domain — Entities, business rules (কোনো dependency নেই)
2. Application — Use cases, DTOs, interfaces (Domain-এর উপর নির্ভর করে)
3. Infrastructure — EF Core, external services (Application implement করে)
4. API — Controllers, middleware (Application কে call করে)

এই separation-এ প্রতিটি layer-এর responsibility আলাদা।
Domain core business logic ধারণ করে এবং কোনো framework-এর উপর
নির্ভর করে না। Testing সহজ হয়।

appsettings.json-এ connection strings এবং config রাখি।
Secrets production-এ environment variables বা Azure Key Vault-এ।
```

---

## PART 1 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| .NET | Microsoft-এর cross-platform developer platform |
| .NET Framework | Windows-only, legacy, 2002 থেকে |
| .NET Core / .NET 5+ | Cross-platform, open-source, 2016 থেকে |
| CLR | Execution engine — JIT, GC, Type safety |
| CTS | Type system — Value Type vs Reference Type |
| CLS | Languages-এর মধ্যে interop-এর minimum rules |
| IL (MSIL) | CPU-independent bytecode — compile-এর output |
| JIT | IL → Native machine code, runtime-এ |
| Managed Code | CLR-এর control-এ — C# code |
| Unmanaged Code | CLR-এর বাইরে — C/C++, P/Invoke দিয়ে call |
| GC | Automatic heap memory management |
| Gen 0/1/2 | GC generations — short to long-lived objects |
| IDisposable | Unmanaged resources manually cleanup |
| Assembly | .dll/.exe — .NET deployment unit |
| NuGet | .NET package manager |
| SDK | Development tool (Runtime + Compiler + CLI) |
| Runtime | শুধু app run করার জন্য |
| Solution | Multiple projects-এর container (.sln) |

---

## PART 1 Interview Q&A

```
প্রশ্ন: .NET কী?
উত্তর: Microsoft-এর cross-platform, open-source developer platform।
Web, mobile, desktop, cloud app তৈরি করা যায়।
C#, F#, VB.NET ব্যবহার করা যায়।

প্রশ্ন: CLR এর কাজ কী?
উত্তর: .NET-এর execution engine।
JIT দিয়ে IL কে native code-এ convert করে।
GC দিয়ে memory manage করে।
Type safety, exception handling, security enforce করে।

প্রশ্ন: Value Type আর Reference Type-এর পার্থক্য?
উত্তর:
Value Type (int, struct) → Stack-এ store, copy করলে new copy
Reference Type (class, array) → Heap-এ store, copy করলে reference copy

প্রশ্ন: GC কীভাবে কাজ করে?
উত্তর: Gen 0, Gen 1, Gen 2 — তিন generation-এ heap divide।
নতুন objects Gen 0-তে।
Gen 0 full → GC run → জীবিত objects Gen 1-এ promote।
IDisposable দিয়ে unmanaged resources manually clean করতে হয়।

প্রশ্ন: Assembly কী?
উত্তর: .NET-এর deployment unit।
Compile করলে .dll বা .exe হয়।
IL code, metadata, manifest থাকে।

প্রশ্ন: SDK আর Runtime-এর পার্থক্য?
উত্তর:
SDK → Developer-এর জন্য: compiler + CLI + Runtime সব একসাথে।
Runtime → Production server-এর জন্য: শুধু app run করা।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 2 — C# Fundamentals (Variables, Data Types, Loops, Methods, Exception Handling, Collections এবং আরও...)

---

<a id="part2"></a>
## PART 2: C# Fundamentals

> Variables, Data Types, Operators, Loops, Methods, Arrays, Collections, Strings, Exception Handling, File I/O, Nullable Types, var vs dynamic, String vs StringBuilder।

| # | বিষয় |
|---|-------|
| 1 | [C# পরিচিতি ও Basics](#p2-basics) |
| 2 | [Variables ও Data Types](#p2-datatypes) |
| 3 | [Operators](#p2-operators) |
| 4 | [Conditional Statements](#p2-conditionals) |
| 5 | [Loops](#p2-loops) |
| 6 | [Methods ও Parameters](#p2-methods) |
| 7 | [Arrays](#p2-arrays) |
| 8 | [Collections](#p2-collections) |
| 9 | [Strings](#p2-strings) |
| 10 | [Exception Handling](#p2-exceptions) |
| 11 | [File Handling](#p2-files) |
| 12 | [Nullable Types](#p2-nullable) |
| 13 | [var vs dynamic](#p2-var-dynamic) |
| 14 | [String vs StringBuilder](#p2-stringbuilder) |

---

<a id="p2-basics"></a>
### Topic 1: C# পরিচিতি ও Basics

**C# কী:**

C# (উচ্চারণ: "C Sharp") হলো Microsoft-এর তৈরি **strongly-typed, object-oriented, general-purpose** programming language। .NET platform-এর primary language।

```
বৈশিষ্ট্য:
✅ Strongly typed       — compile-time type checking
✅ Object-Oriented      — class, inheritance, polymorphism
✅ Component-oriented   — properties, events, delegates
✅ Safe                 — garbage collected, no raw pointers
✅ Modern               — async/await, LINQ, pattern matching
✅ Versatile            — web, desktop, mobile, cloud, games
```

**First C# Program:**

```csharp
// Program.cs — .NET 6+ (Top-level statements)
Console.WriteLine("Hello, Bangladesh!");

// অথবা traditional style:
namespace MyApp
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello, Bangladesh!");
            Console.ReadLine(); // enter চাপার আগে পর্যন্ত window খোলা থাকে
        }
    }
}
```

**C# Version History (Interview-এ জিজ্ঞেস হয়):**

| Version | .NET | মূল Feature |
|---------|------|-------------|
| C# 6 | .NET 4.6 | String interpolation, null-conditional |
| C# 7 | .NET 4.7 / Core 1 | Tuples, pattern matching, local functions |
| C# 8 | .NET Core 3 | Nullable reference types, async streams |
| C# 9 | .NET 5 | Records, init properties, top-level statements |
| C# 10 | .NET 6 | Global usings, file-scoped namespace |
| C# 11 | .NET 7 | Raw strings, required members |
| C# 12 | .NET 8 | Primary constructors, collection expressions |

**C# Program Structure:**

```csharp
// ── Namespace ──────────────────────────────────────────
namespace MyCompany.MyApp;   // C# 10+ file-scoped namespace

// ── Using directives ───────────────────────────────────
using System;
using System.Collections.Generic;
using System.Linq;

// ── Class ──────────────────────────────────────────────
public class CustomerService
{
    // ── Fields ─────────────────────────────────────────
    private readonly List<Customer> _customers = new();

    // ── Properties ─────────────────────────────────────
    public int Count => _customers.Count;

    // ── Methods ────────────────────────────────────────
    public void Add(Customer customer) => _customers.Add(customer);

    public Customer? GetById(int id) =>
        _customers.FirstOrDefault(c => c.Id == id);
}

// ── Record (C# 9+) ─────────────────────────────────────
public record Customer(int Id, string Name, string Email);
```

---

<a id="p2-datatypes"></a>
### Topic 2: Variables ও Data Types

**Variable Declaration:**

```csharp
// ── Explicit type ──────────────────────────
int age = 25;
string name = "Rahim";
double salary = 55000.50;
bool isActive = true;

// ── var — compiler type infer করে ────────
var city = "Dhaka";       // string
var count = 10;            // int
var price = 99.99;         // double

// ── const — compile-time constant ─────────
const double PI = 3.14159;
const int MAX_SIZE = 100;
// PI = 3.0; // ❌ Error — const পরিবর্তন করা যায় না

// ── readonly — runtime constant ───────────
readonly DateTime CreatedAt = DateTime.Now;
// constructor-এ set করা যায়, তারপর নয়
```

**Built-in Data Types — সম্পূর্ণ তালিকা:**

```csharp
// ── Integer types ─────────────────────────────────────
byte   b = 255;                // 0 to 255 (8-bit unsigned)
sbyte  sb = -128;              // -128 to 127 (8-bit signed)
short  s = 32767;              // -32,768 to 32,767 (16-bit)
ushort us = 65535;             // 0 to 65,535 (16-bit unsigned)
int    i = 2_147_483_647;      // ~±2 billion (32-bit) ← সবচেয়ে বেশি ব্যবহার
uint   ui = 4_294_967_295U;    // 0 to ~4 billion
long   l = 9_223_372_036L;     // ~±9.2 × 10¹⁸ (64-bit)
ulong  ul = 18_446_744_073UL;  // 0 to ~1.8 × 10¹⁹

// ── Floating-point types ──────────────────────────────
float   f = 3.14f;             // 7 digits precision (32-bit)
double  d = 3.14159265358979;  // 15-16 digits precision (64-bit) ← সাধারণ ব্যবহার
decimal m = 99.99m;            // 28-29 digits precision ← টাকার হিসাব!

// ── Text types ────────────────────────────────────────
char   c = 'A';                // একটি Unicode character (16-bit)
string str = "Hello, বাংলাদেশ!"; // Unicode text (reference type)

// ── Boolean ───────────────────────────────────────────
bool isLoggedIn = false;

// ── Special types ─────────────────────────────────────
object obj = 42;              // সব type-এর base
dynamic dyn = "Hello";        // runtime type — পরে আলোচনা হবে
```

**Interview Trap: float vs double vs decimal:**

```csharp
// ─────────────────────────────────────────────────────
// decimal ব্যবহার করুন টাকার হিসাবে — floating point error নেই
// ─────────────────────────────────────────────────────

// ❌ float/double — binary floating point error আছে
double price1 = 0.1 + 0.2;
Console.WriteLine(price1);         // 0.30000000000000004 ← ভুল!

decimal price2 = 0.1m + 0.2m;
Console.WriteLine(price2);         // 0.3 ← সঠিক!

// Bank account, eCommerce, financial calculation → সবসময় decimal
decimal accountBalance = 10_000.50m;
decimal transactionAmount = 500.25m;
decimal newBalance = accountBalance - transactionAmount; // 9500.25
```

**Type Conversion:**

```csharp
// ── Implicit Conversion (safe, no data loss) ──────────
int x = 100;
long y = x;        // int → long ✅ automatic
double z = x;      // int → double ✅ automatic

// ── Explicit Conversion / Cast (possible data loss) ───
double pi = 3.14159;
int piInt = (int)pi;     // 3 — decimal part কাটা যায়!
Console.WriteLine(piInt); // 3

long bigNum = 3_000_000_000L;
int smallNum = (int)bigNum; // ❌ overflow! data loss হবে

// ── Convert class ─────────────────────────────────────
string numStr = "42";
int parsed = Convert.ToInt32(numStr);    // "42" → 42
double d = Convert.ToDouble("3.14");
bool b = Convert.ToBoolean("true");

// ── Parse — string → specific type ───────────────────
int a = int.Parse("100");
double price = double.Parse("99.99");
DateTime date = DateTime.Parse("2026-01-15");

// ── TryParse — safe (exception throw করে না) ─────────
string input = "abc";
if (int.TryParse(input, out int result))
{
    Console.WriteLine($"Parsed: {result}");
}
else
{
    Console.WriteLine("Invalid number"); // এটা চলবে
}
```

**🎤 Interview-style Q&A:**

```
প্রশ্ন: int আর long-এর পার্থক্য কী? কখন কোনটা ব্যবহার করবেন?

উত্তর:
int → 32-bit, range ±2 billion। সাধারণ counter, id, index-এ।
long → 64-bit, range ±9.2×10¹⁸। File size, timestamp, large IDs-এ।

যেমন Unix timestamp লং টাইপ হয়। Phone number (01XXXXXXXXX)
long হওয়া উচিত — কিন্তু সাধারণত string রাখি কারণ
leading zero হারিয়ে যায় না।

প্রশ্ন: decimal কেন ব্যবহার করি financial calculation-এ?

উত্তর:
float ও double binary floating-point, তাই 0.1 + 0.2 = 0.30000...004।
decimal decimal-based, তাই exact। টাকার হিসাবে penny হারানো মানে
real money হারানো — তাই সবসময় decimal।
```

---

<a id="p2-operators"></a>
### Topic 3: Operators

```csharp
// ── Arithmetic Operators ──────────────────────────────
int a = 10, b = 3;
Console.WriteLine(a + b);   // 13  — Addition
Console.WriteLine(a - b);   // 7   — Subtraction
Console.WriteLine(a * b);   // 30  — Multiplication
Console.WriteLine(a / b);   // 3   — Division (integer division!)
Console.WriteLine(a % b);   // 1   — Modulus (remainder)

double x = 10.0, y = 3.0;
Console.WriteLine(x / y);   // 3.333...  — double division

// ── Increment / Decrement ─────────────────────────────
int count = 5;
count++;          // Post-increment: use করার পরে বাড়ে
++count;          // Pre-increment: use করার আগে বাড়ে
count--;          // Post-decrement
--count;          // Pre-decrement

int pre = ++count;   // count বাড়িয়ে তারপর assign
int post = count++;  // assign করে তারপর count বাড়ায়

// ── Assignment Operators ──────────────────────────────
int n = 10;
n += 5;    // n = n + 5 = 15
n -= 3;    // n = n - 3 = 12
n *= 2;    // n = n * 2 = 24
n /= 4;    // n = n / 4 = 6
n %= 4;    // n = n % 4 = 2

// ── Comparison Operators ──────────────────────────────
int p = 5, q = 10;
bool r1 = p == q;    // false — equal
bool r2 = p != q;    // true  — not equal
bool r3 = p > q;     // false — greater than
bool r4 = p < q;     // true  — less than
bool r5 = p >= q;    // false — greater or equal
bool r6 = p <= q;    // true  — less or equal

// ── Logical Operators ─────────────────────────────────
bool isAdult = true;
bool hasId = false;

bool canEnter = isAdult && hasId;   // false — AND (উভয় true হতে হবে)
bool isEligible = isAdult || hasId; // true  — OR (যেকোনো একটি true)
bool notAdult = !isAdult;           // false — NOT

// Short-circuit evaluation:
// && → প্রথমটা false হলে দ্বিতীয়টা check করে না
// || → প্রথমটা true হলে দ্বিতীয়টা check করে না

// ── Null-coalescing Operator (??) ─────────────────────
string? input = null;
string name = input ?? "Anonymous";   // "Anonymous"
Console.WriteLine(name);

// ── Null-conditional Operator (?.) ───────────────────
string? text = null;
int? length = text?.Length;           // null — exception নেই!
// text?.ToUpper()?.Replace("A", "a") — chaining

// ── Ternary Operator ──────────────────────────────────
int score = 75;
string grade = score >= 60 ? "Pass" : "Fail";  // "Pass"

// ── is / as operators ─────────────────────────────────
object obj = "Hello";
bool isString = obj is string;          // true
string? str = obj as string;            // "Hello" (null if fails)
// string str2 = (string)obj;           // throws if fails

// C# 7+ pattern matching with is:
if (obj is string s && s.Length > 3)
{
    Console.WriteLine($"String: {s}");  // "Hello"
}

// ── Bitwise Operators ─────────────────────────────────
int flags = 0b0000_0101;   // 5
int mask  = 0b0000_0011;   // 3
Console.WriteLine(flags & mask);  // 1  — AND
Console.WriteLine(flags | mask);  // 7  — OR
Console.WriteLine(flags ^ mask);  // 6  — XOR
Console.WriteLine(~flags);        // -6 — NOT
Console.WriteLine(flags << 1);    // 10 — Left shift
Console.WriteLine(flags >> 1);    // 2  — Right shift
```

**🎤 Interview Trap:**

```
প্রশ্ন: == এবং .Equals() এর পার্থক্য কী?

উত্তর:
Value types-এ উভয়ই value compare করে।

Reference types-এ:
== → reference equality (same memory address?)
.Equals() → logical equality (same content?)

কিন্তু string একটি exception:
string a = "Hello";
string b = "Hello";
a == b       // true  — string-এ == content compare করে
a.Equals(b)  // true  — content compare

object o1 = new object();
object o2 = new object();
o1 == o2       // false — different references
o1.Equals(o2)  // false — by default reference equality

Custom class-এ Equals() override করে content equality define করতে পারি।
```

---

<a id="p2-conditionals"></a>
### Topic 4: Conditional Statements

```csharp
// ── if / else if / else ───────────────────────────────
int marks = 78;

if (marks >= 80)
{
    Console.WriteLine("A+");
}
else if (marks >= 70)
{
    Console.WriteLine("A");      // এটা চলবে
}
else if (marks >= 60)
{
    Console.WriteLine("B");
}
else
{
    Console.WriteLine("Fail");
}

// ── switch statement ──────────────────────────────────
string day = "Monday";

switch (day)
{
    case "Saturday":
    case "Sunday":
        Console.WriteLine("Weekend");
        break;
    case "Monday":
        Console.WriteLine("Workday");  // এটা চলবে
        break;
    default:
        Console.WriteLine("Other day");
        break;
}

// ── switch expression (C# 8+) ─────────────────────────
int statusCode = 404;
string message = statusCode switch
{
    200 => "OK",
    201 => "Created",
    400 => "Bad Request",
    401 => "Unauthorized",
    403 => "Forbidden",
    404 => "Not Found",       // এটা select হবে
    500 => "Server Error",
    _   => "Unknown"          // default
};
Console.WriteLine(message); // "Not Found"

// ── Pattern Matching (C# 7+) ──────────────────────────
object shape = new Circle { Radius = 5 };

string description = shape switch
{
    Circle c when c.Radius > 10 => "Large circle",
    Circle c                    => $"Circle r={c.Radius}",  // এটা
    Rectangle r                 => $"Rectangle {r.Width}x{r.Height}",
    _                           => "Unknown shape"
};
Console.WriteLine(description); // "Circle r=5"

// ── Null check patterns ────────────────────────────────
string? name = GetName();

// Old style:
if (name != null) { Console.WriteLine(name.ToUpper()); }

// Modern C# 8+:
if (name is not null) { Console.WriteLine(name.ToUpper()); }
if (name is { Length: > 0 }) { Console.WriteLine("Non-empty"); }

// Helper records for pattern matching demo
record Circle(double Radius);
record Rectangle(double Width, double Height);
static string? GetName() => "Rahim";
```

---

<a id="p2-loops"></a>
### Topic 5: Loops

```csharp
// ── for loop ──────────────────────────────────────────
for (int i = 0; i < 5; i++)
{
    Console.Write(i + " "); // 0 1 2 3 4
}

// Reverse loop
for (int i = 10; i >= 1; i--)
{
    Console.Write(i + " "); // 10 9 8 ... 1
}

// ── while loop ────────────────────────────────────────
int n = 1;
while (n <= 5)
{
    Console.Write(n + " "); // 1 2 3 4 5
    n++;
}

// ── do-while loop — অন্তত একবার চলে ──────────────────
int x = 0;
do
{
    Console.Write(x + " "); // 0 (একবারই চলে)
    x++;
} while (x < 0); // condition false হলেও প্রথমবার চলে

// ── foreach — Collections iterate করার জন্য ──────────
var names = new List<string> { "Rahim", "Karim", "Jamal" };
foreach (var name in names)
{
    Console.WriteLine(name);
}

string[] cities = { "Dhaka", "Chittagong", "Sylhet" };
foreach (string city in cities)
{
    Console.WriteLine(city);
}

// ── break and continue ────────────────────────────────
for (int i = 0; i < 10; i++)
{
    if (i == 3) continue;  // 3 skip করবে
    if (i == 7) break;     // 7-এ loop শেষ
    Console.Write(i + " "); // 0 1 2 4 5 6
}

// ── Nested loops ──────────────────────────────────────
for (int row = 1; row <= 3; row++)
{
    for (int col = 1; col <= 3; col++)
    {
        Console.Write($"({row},{col}) ");
    }
    Console.WriteLine();
}
// (1,1) (1,2) (1,3)
// (2,1) (2,2) (2,3)
// (3,1) (3,2) (3,3)

// ── LINQ এর with loops ────────────────────────────────
// foreach replace করার জন্য LINQ (Part 4-এ বিস্তারিত)
var evens = Enumerable.Range(1, 10).Where(n => n % 2 == 0);
foreach (var e in evens)
    Console.Write(e + " "); // 2 4 6 8 10
```

**🎤 Interview Q&A:**

```
প্রশ্ন: for এবং foreach-এর পার্থক্য?

উত্তর:
for → index দিয়ে iterate করে, মাঝে modify করা যায়।
foreach → collection-এর প্রতিটি element read করে।
         Iteration-এর সময় collection modify করা যায় না।

foreach ব্যবহার করুন যখন: শুধু read করতে হবে, clean code।
for ব্যবহার করুন যখন: index দরকার, reverse iteration, step control।

প্রশ্ন: foreach loop চলার সময় List modify করলে কী হয়?

উত্তর: InvalidOperationException throw করে —
"Collection was modified; enumeration operation may not execute."

Solution: ToList() দিয়ে copy করে iterate করুন,
অথবা for loop ব্যবহার করুন।
```

---

<a id="p2-methods"></a>
### Topic 6: Methods ও Parameters

**Method Declaration:**

```csharp
// ── Basic method ──────────────────────────────────────
public int Add(int a, int b)
{
    return a + b;
}

// ── Expression body (C# 6+) ───────────────────────────
public int Multiply(int a, int b) => a * b;

// ── void method ───────────────────────────────────────
public void PrintGreeting(string name)
{
    Console.WriteLine($"Hello, {name}!");
}

// ── Static method ─────────────────────────────────────
public static double CalculateTax(decimal amount, double rate)
{
    return (double)amount * rate / 100;
}
```

**Parameter Types:**

```csharp
public class ParameterDemo
{
    // ── 1. Value parameters (default) ─────────────────
    // Copy pass হয় — original পরিবর্তন হয় না
    public void DoubleValue(int x)
    {
        x = x * 2;  // local copy
    }

    void TestValue()
    {
        int n = 5;
        DoubleValue(n);
        Console.WriteLine(n); // 5 — পরিবর্তন হয়নি
    }

    // ── 2. ref parameter ──────────────────────────────
    // Reference pass হয় — original পরিবর্তন হয়
    public void DoubleRef(ref int x)
    {
        x = x * 2;
    }

    void TestRef()
    {
        int n = 5;
        DoubleRef(ref n);
        Console.WriteLine(n); // 10 — পরিবর্তন হয়েছে!
    }

    // ── 3. out parameter ──────────────────────────────
    // Method থেকে multiple values return করার জন্য
    // Call করার আগে initialize করতে হয় না
    public bool TryDivide(int a, int b, out int result)
    {
        if (b == 0)
        {
            result = 0;
            return false;
        }
        result = a / b;
        return true;
    }

    void TestOut()
    {
        if (TryDivide(10, 2, out int result))
            Console.WriteLine($"Result: {result}"); // 5
    }

    // ── 4. params — variable number of arguments ──────
    public int Sum(params int[] numbers)
    {
        return numbers.Sum();
    }

    void TestParams()
    {
        Console.WriteLine(Sum(1, 2, 3));           // 6
        Console.WriteLine(Sum(10, 20, 30, 40));    // 100
        Console.WriteLine(Sum(new int[] { 5, 5 }));// 10
    }

    // ── 5. Optional parameters (default values) ───────
    public string CreateGreeting(string name, string prefix = "Mr.", bool formal = true)
    {
        return formal ? $"Dear {prefix} {name}," : $"Hey {name}!";
    }

    void TestOptional()
    {
        Console.WriteLine(CreateGreeting("Rahim"));              // Dear Mr. Rahim,
        Console.WriteLine(CreateGreeting("Karim", "Dr."));       // Dear Dr. Karim,
        Console.WriteLine(CreateGreeting("Jamal", formal: false)); // Hey Jamal!
    }

    // ── 6. Named arguments ────────────────────────────
    void TestNamed()
    {
        // parameter নাম দিয়ে pass করলে order গুরুত্বপূর্ণ নয়
        var result = CreateGreeting(
            formal: false,
            name: "Nadia",
            prefix: "Ms."
        ); // Hey Nadia!
    }

    // ── 7. in parameter (C# 7.2+) — readonly ref ──────
    // Large struct pass করার সময় copy avoid করে
    public double CalculateArea(in Point topLeft, in Point bottomRight)
    {
        double width = Math.Abs(bottomRight.X - topLeft.X);
        double height = Math.Abs(bottomRight.Y - topLeft.Y);
        return width * height;
    }
}

record struct Point(double X, double Y);
```

**Local Functions (C# 7+):**

```csharp
public int Factorial(int n)
{
    // Local function — শুধু এই method-এর ভেতরে visible
    int Calculate(int num)
    {
        if (num <= 1) return 1;
        return num * Calculate(num - 1);
    }

    if (n < 0) throw new ArgumentException("n must be >= 0");
    return Calculate(n);
}

// Static local function (C# 8+) — outer scope capture করে না
public double ProcessData(double[] data)
{
    return data.Select(static x => Normalize(x)).Sum();

    static double Normalize(double value) => value / 100.0;
}
```

**Method Overloading:**

```csharp
public class Calculator
{
    // Same name, different parameters — compile করে ঠিক করে
    public int Add(int a, int b) => a + b;
    public double Add(double a, double b) => a + b;
    public int Add(int a, int b, int c) => a + b + c;
    public string Add(string a, string b) => a + b;
}

var calc = new Calculator();
Console.WriteLine(calc.Add(1, 2));          // 3  (int version)
Console.WriteLine(calc.Add(1.5, 2.5));      // 4.0 (double version)
Console.WriteLine(calc.Add(1, 2, 3));       // 6  (3-param version)
Console.WriteLine(calc.Add("Hello", " World")); // "Hello World"
```

---

<a id="p2-arrays"></a>
### Topic 7: Arrays

```csharp
// ── Single-dimensional array ──────────────────────────
int[] numbers = new int[5];          // [0, 0, 0, 0, 0]
int[] scores = { 85, 92, 78, 96, 88 }; // Initializer
int[] grades = new int[] { 70, 80, 90 };

Console.WriteLine(scores[0]);        // 85 — 0-indexed
Console.WriteLine(scores.Length);    // 5
scores[2] = 100;                     // Modify

// ── Iteration ─────────────────────────────────────────
for (int i = 0; i < scores.Length; i++)
    Console.Write(scores[i] + " ");

foreach (int score in scores)
    Console.Write(score + " ");

// ── Array Methods ─────────────────────────────────────
int[] data = { 5, 2, 8, 1, 9, 3 };

Array.Sort(data);                    // [1, 2, 3, 5, 8, 9]
Array.Reverse(data);                 // [9, 8, 5, 3, 2, 1]
int idx = Array.IndexOf(data, 5);    // 2 (sorted হওয়ার পরে)
Array.Fill(data, 0);                 // [0, 0, 0, 0, 0, 0]

// ── LINQ with arrays ──────────────────────────────────
int[] marks = { 45, 78, 92, 61, 55, 88 };
int max = marks.Max();               // 92
int min = marks.Min();               // 45
double avg = marks.Average();        // 69.83...
int[] passed = marks.Where(m => m >= 60).ToArray(); // [78, 92, 61, 88]

// ── Multi-dimensional array ───────────────────────────
int[,] matrix = new int[3, 3];
int[,] grid = {
    { 1, 2, 3 },
    { 4, 5, 6 },
    { 7, 8, 9 }
};

Console.WriteLine(grid[1, 2]); // 6 — row 1, col 2

for (int row = 0; row < 3; row++)
{
    for (int col = 0; col < 3; col++)
        Console.Write(grid[row, col] + " ");
    Console.WriteLine();
}

// ── Jagged array (array of arrays) ───────────────────
int[][] jagged = new int[3][];
jagged[0] = new int[] { 1, 2 };
jagged[1] = new int[] { 3, 4, 5 };
jagged[2] = new int[] { 6 };

Console.WriteLine(jagged[1][2]); // 5 — row 1, index 2

// ── Array Copying ─────────────────────────────────────
int[] original = { 1, 2, 3, 4, 5 };

// Shallow copy
int[] copy1 = (int[])original.Clone();
int[] copy2 = new int[original.Length];
Array.Copy(original, copy2, original.Length);

// LINQ ToArray
int[] copy3 = original.ToArray();

// Span<T> — zero-copy slice (modern, high-performance)
Span<int> slice = original.AsSpan(1, 3); // [2, 3, 4] — no copy!
```

**🎤 Interview Q&A:**

```
প্রশ্ন: Array আর List-এর পার্থক্য কী?

উত্তর:
Array → Fixed size, declaration-এ size define করতে হয়।
         Access O(1), insert/delete costly।
         int[] arr = new int[10];

List<T> → Dynamic size, automatically grows।
           Add/Remove সহজ।
           List<int> list = new List<int>();

সাধারণত List ব্যবহার করি কারণ size জানা যায় না।
Performance-critical code বা fixed-size buffer-এ Array।
```

---

<a id="p2-collections"></a>
### Topic 8: Collections

**.NET Collections Overview:**

```
System.Collections.Generic (সবচেয়ে বেশি ব্যবহৃত):
├── List<T>           — Dynamic array
├── Dictionary<K,V>  — Key-value store (hash map)
├── HashSet<T>        — Unique elements
├── Queue<T>          — FIFO
├── Stack<T>          — LIFO
├── LinkedList<T>     — Doubly linked list
└── SortedDictionary<K,V> — Sorted key-value

System.Collections.Concurrent (Thread-safe):
├── ConcurrentDictionary<K,V>
├── ConcurrentQueue<T>
└── ConcurrentBag<T>
```

**List\<T\> — সবচেয়ে বেশি ব্যবহৃত:**

```csharp
var students = new List<string>();

// Add
students.Add("Rahim");
students.Add("Karim");
students.AddRange(new[] { "Jamal", "Nadia" });
students.Insert(1, "Sadia"); // index 1-এ insert

// Access
Console.WriteLine(students[0]);        // "Rahim"
Console.WriteLine(students.Count);     // 5

// Search
bool has = students.Contains("Karim"); // true
int idx = students.IndexOf("Jamal");   // 2 (shifted after insert)

// Remove
students.Remove("Sadia");             // by value
students.RemoveAt(0);                 // by index
students.RemoveAll(s => s.Length > 5); // by condition

// Sort
students.Sort();
students.Sort((a, b) => a.Length.CompareTo(b.Length)); // custom

// LINQ on List
var longNames = students.Where(s => s.Length > 4).ToList();
var upperNames = students.Select(s => s.ToUpper()).ToList();
var firstStudent = students.FirstOrDefault();

// Iteration
foreach (var s in students)
    Console.WriteLine(s);
```

**Dictionary\<TKey, TValue\>:**

```csharp
var studentGrades = new Dictionary<string, int>
{
    { "Rahim", 85 },
    { "Karim", 92 },
    ["Jamal"] = 78  // C# 6+ index initializer
};

// Add / Update
studentGrades["Nadia"] = 88;
studentGrades.Add("Sadia", 95);
studentGrades["Rahim"] = 90; // update existing

// Access — safe way
if (studentGrades.TryGetValue("Karim", out int grade))
    Console.WriteLine($"Karim: {grade}"); // 92

// Dangerous — throws KeyNotFoundException if not found
// int g = studentGrades["Unknown"]; // ❌

// Contains check
bool exists = studentGrades.ContainsKey("Jamal"); // true

// Iterate
foreach (var (name, g) in studentGrades)
    Console.WriteLine($"{name}: {g}");

// Keys and Values
IEnumerable<string> names = studentGrades.Keys;
IEnumerable<int> grades = studentGrades.Values;

// Count
Console.WriteLine(studentGrades.Count); // 5

// Remove
studentGrades.Remove("Sadia");
```

**HashSet\<T\> — Unique elements:**

```csharp
var set1 = new HashSet<int> { 1, 2, 3, 4, 5 };
var set2 = new HashSet<int> { 3, 4, 5, 6, 7 };

set1.Add(3); // false — already exists, no duplicate!
Console.WriteLine(set1.Count); // 5

// Set operations
set1.IntersectWith(set2);  // {3, 4, 5} — common
set1.UnionWith(set2);      // {1,2,3,4,5,6,7} — all
set1.ExceptWith(set2);     // {1, 2} — difference

bool subset = set1.IsSubsetOf(set2);
bool superset = set1.IsSupersetOf(set2);

// Duplicate removal — এটাই HashSet-এর সবচেয়ে common use
int[] withDuplicates = { 1, 2, 2, 3, 3, 3, 4 };
var unique = new HashSet<int>(withDuplicates); // {1, 2, 3, 4}
```

**Queue\<T\> ও Stack\<T\>:**

```csharp
// ── Queue — FIFO (First In, First Out) ───────────────
// Use case: Task queue, request processing, BFS

var taskQueue = new Queue<string>();
taskQueue.Enqueue("Send Email");
taskQueue.Enqueue("Process Payment");
taskQueue.Enqueue("Update Inventory");

Console.WriteLine(taskQueue.Peek());    // "Send Email" — remove করে না
Console.WriteLine(taskQueue.Dequeue()); // "Send Email" — remove করে
Console.WriteLine(taskQueue.Count);     // 2

// ── Stack — LIFO (Last In, First Out) ────────────────
// Use case: Undo/Redo, expression evaluation, DFS

var history = new Stack<string>();
history.Push("/home");
history.Push("/products");
history.Push("/products/details/5");

Console.WriteLine(history.Peek()); // "/products/details/5"
Console.WriteLine(history.Pop());  // "/products/details/5" — remove
Console.WriteLine(history.Pop());  // "/products"
// Back button এর মতো!
```

**Interview-এ Collection Choice:**

```
প্রশ্ন: কোন Collection কখন ব্যবহার করবেন?

উত্তর:
List<T>           → Default choice। Dynamic list, ordered, duplicates allowed।
Dictionary<K,V>   → Fast lookup by key। O(1) average। Key-value data।
HashSet<T>        → Unique elements। Fast contains check। Duplicate removal।
Queue<T>          → FIFO processing। Task queues, BFS।
Stack<T>          → LIFO। Undo/Redo, expression parsing, DFS।
SortedDictionary  → Key দিয়ে sorted order দরকার হলে।
ConcurrentDict    → Multi-threaded environment-এ Dictionary।

Performance:
List access   → O(1)
List search   → O(n)
Dictionary    → O(1) average (key lookup)
HashSet       → O(1) average (contains)
```

---

<a id="p2-strings"></a>
### Topic 9: Strings

**String Basics:**

```csharp
// ── String declaration ────────────────────────────────
string name = "Rahim";
string empty = "";
string nullStr = null;

// ── String properties ─────────────────────────────────
Console.WriteLine(name.Length);          // 5
Console.WriteLine(string.IsNullOrEmpty(nullStr));    // true
Console.WriteLine(string.IsNullOrWhiteSpace("   ")); // true

// ── Common string methods ─────────────────────────────
string text = "  Hello, Bangladesh!  ";

// Case
Console.WriteLine(text.ToUpper());   // "  HELLO, BANGLADESH!  "
Console.WriteLine(text.ToLower());   // "  hello, bangladesh!  "

// Trim
Console.WriteLine(text.Trim());      // "Hello, Bangladesh!"
Console.WriteLine(text.TrimStart()); // "Hello, Bangladesh!  "
Console.WriteLine(text.TrimEnd());   // "  Hello, Bangladesh!"

// Search
string sentence = "The quick brown fox";
Console.WriteLine(sentence.Contains("quick"));      // true
Console.WriteLine(sentence.StartsWith("The"));      // true
Console.WriteLine(sentence.EndsWith("fox"));        // true
Console.WriteLine(sentence.IndexOf("brown"));       // 10

// Manipulation
Console.WriteLine(sentence.Replace("fox", "cat"));  // "The quick brown cat"
Console.WriteLine(sentence.Substring(4, 5));        // "quick"
Console.WriteLine(sentence.Remove(4, 6));           // "The brown fox"

// Split & Join
string csv = "Dhaka,Chittagong,Sylhet,Rajshahi";
string[] cities = csv.Split(',');
// ["Dhaka", "Chittagong", "Sylhet", "Rajshahi"]

string joined = string.Join(" | ", cities);
// "Dhaka | Chittagong | Sylhet | Rajshahi"

// ── String comparison ─────────────────────────────────
string a = "hello";
string b = "HELLO";
Console.WriteLine(a == b);                                       // false
Console.WriteLine(a.Equals(b, StringComparison.OrdinalIgnoreCase)); // true
Console.WriteLine(string.Compare(a, b, ignoreCase: true));       // 0 (equal)
```

**String Formatting:**

```csharp
string name = "Rahim";
int age = 25;
decimal salary = 55000.50m;

// ── String interpolation (C# 6+) — সবচেয়ে ভালো ──────
string msg1 = $"Name: {name}, Age: {age}, Salary: {salary:C}";

// ── Format specifiers ─────────────────────────────────
decimal amount = 12345.678m;
Console.WriteLine($"{amount:F2}");    // 12345.68  — 2 decimal places
Console.WriteLine($"{amount:N2}");    // 12,345.68 — thousand separator
Console.WriteLine($"{amount:C}");     // $12,345.68 — currency (locale-based)
Console.WriteLine($"{amount:P}");     // 1,234,567.80% — percent

int num = 255;
Console.WriteLine($"{num:X}");        // FF — hexadecimal
Console.WriteLine($"{num:B}");        // 11111111 — binary (.NET 8+)
Console.WriteLine($"{num:D8}");       // 00000255 — padded decimal

DateTime now = DateTime.Now;
Console.WriteLine($"{now:dd/MM/yyyy}");        // 13/05/2026
Console.WriteLine($"{now:yyyy-MM-dd HH:mm}");  // 2026-05-13 04:30
Console.WriteLine($"{now:dddd, dd MMMM yyyy}"); // Tuesday, 13 May 2026

// ── string.Format (old style) ─────────────────────────
string msg2 = string.Format("Name: {0}, Age: {1}", name, age);

// ── Verbatim string (@) — escape নেই ─────────────────
string path = @"C:\Users\Rahim\Documents\file.txt"; // \U, \D escape হয় না
string multiline = @"Line 1
Line 2
Line 3"; // newline literal

// ── Raw string literal (C# 11+) ───────────────────────
string json = """
    {
        "name": "Rahim",
        "age": 25
    }
    """; // no escape needed, no leading spaces issue
```

---

<a id="p2-exceptions"></a>
### Topic 10: Exception Handling

**Exception Hierarchy:**

```
System.Exception
├── System.SystemException
│   ├── NullReferenceException     — null object access
│   ├── IndexOutOfRangeException   — array bound violation
│   ├── InvalidCastException       — invalid type cast
│   ├── DivideByZeroException      — divide by zero
│   ├── OverflowException          — arithmetic overflow
│   ├── StackOverflowException     — infinite recursion
│   ├── OutOfMemoryException       — memory exhausted
│   └── InvalidOperationException  — invalid state
├── System.ApplicationException    — app-specific (avoid, use Exception directly)
└── System.IO.IOException
    ├── FileNotFoundException
    └── DirectoryNotFoundException
```

**try-catch-finally:**

```csharp
// ── Basic try-catch ───────────────────────────────────
try
{
    int[] arr = { 1, 2, 3 };
    Console.WriteLine(arr[10]); // ❌ IndexOutOfRangeException
}
catch (IndexOutOfRangeException ex)
{
    Console.WriteLine($"Array error: {ex.Message}");
}

// ── Multiple catch blocks ─────────────────────────────
void ProcessFile(string path, string input)
{
    try
    {
        string content = File.ReadAllText(path);
        int number = int.Parse(input);
        int result = 100 / number;
        Console.WriteLine(result);
    }
    catch (FileNotFoundException ex)
    {
        Console.WriteLine($"File not found: {ex.FileName}");
    }
    catch (FormatException ex)
    {
        Console.WriteLine($"Invalid number format: {ex.Message}");
    }
    catch (DivideByZeroException)
    {
        Console.WriteLine("Cannot divide by zero");
    }
    catch (Exception ex) // catch-all — সবচেয়ে শেষে
    {
        Console.WriteLine($"Unexpected error: {ex.Message}");
        // Log করুন, rethrow করুন production-এ
        throw; // original stack trace preserve করে rethrow
    }
    finally
    {
        // সবসময় চলে — exception হোক বা না হোক
        Console.WriteLine("Processing complete");
        // Resource cleanup এখানে
    }
}

// ── when filter (C# 6+) ───────────────────────────────
try
{
    // HTTP call
}
catch (HttpRequestException ex) when (ex.StatusCode == System.Net.HttpStatusCode.NotFound)
{
    Console.WriteLine("Resource not found");
}
catch (HttpRequestException ex) when (ex.StatusCode == System.Net.HttpStatusCode.Unauthorized)
{
    Console.WriteLine("Unauthorized");
}

// ── Custom Exception ──────────────────────────────────
public class ValidationException : Exception
{
    public string FieldName { get; }
    public object InvalidValue { get; }

    public ValidationException(string fieldName, object invalidValue, string message)
        : base(message)
    {
        FieldName = fieldName;
        InvalidValue = invalidValue;
    }

    public ValidationException(string message, Exception innerException)
        : base(message, innerException) { }
}

// Custom exception throw করা
public void ValidateAge(int age)
{
    if (age < 0 || age > 150)
        throw new ValidationException("Age", age, $"Age {age} is invalid");
}

void UseValidation()
{
    try
    {
        ValidateAge(-5);
    }
    catch (ValidationException ex)
    {
        Console.WriteLine($"Validation failed for {ex.FieldName}: {ex.Message}");
    }
}
```

**Best Practices:**

```csharp
// ❌ BAD — Empty catch (exception গিলে ফেলা)
try { /* code */ }
catch (Exception) { } // কী হলো কেউ জানবে না!

// ❌ BAD — Exception দিয়ে flow control
try
{
    int.Parse(input);
}
catch (FormatException)
{
    // এটা flow control — expensive!
    return false;
}
// TryParse ব্যবহার করুন

// ✅ GOOD — Specific exception, log করুন
try
{
    var data = await dbContext.Users.FindAsync(id);
}
catch (SqlException ex) when (ex.Number == 1205) // deadlock
{
    _logger.LogError(ex, "Deadlock while fetching user {Id}", id);
    throw new RetryableException("Database deadlock", ex);
}

// ✅ GOOD — TryParse দিয়ে exception avoid
if (!int.TryParse(input, out int value))
    return BadRequest("Invalid number");

// ✅ GOOD — using statement resource cleanup guarantee
using var stream = new FileStream(path, FileMode.Open);
// stream.Dispose() automatically called এমনকি exception হলেও
```

**🎤 Interview Q&A:**

```
প্রশ্ন: finally block কখন চলে না?

উত্তর:
প্রায় সবসময় finally চলে। কিন্তু চলে না যদি:
1. StackOverflowException — stack নেই, CLR crash
2. Environment.FailFast() — জোর করে process kill
3. Power off / process kill
4. Infinite loop in catch/try

প্রশ্ন: throw আর throw ex-এর পার্থক্য?

উত্তর:
throw;    → original stack trace preserve করে rethrow।
throw ex; → stack trace reset করে — exception কোথা থেকে
            এসেছে তার তথ্য হারায়!

সবসময় throw; ব্যবহার করুন rethrow করার সময়।
```

---

<a id="p2-files"></a>
### Topic 11: File Handling

```csharp
using System.IO;

// ── File read/write ───────────────────────────────────

// Simple text write
File.WriteAllText("data.txt", "Hello, Bangladesh!");

// Simple text read
string content = File.ReadAllText("data.txt");
Console.WriteLine(content); // "Hello, Bangladesh!"

// Write lines
string[] lines = { "Line 1", "Line 2", "Line 3" };
File.WriteAllLines("lines.txt", lines);

// Read lines
string[] readLines = File.ReadAllLines("lines.txt");
foreach (var line in readLines)
    Console.WriteLine(line);

// Append
File.AppendAllText("data.txt", "\nNew line added");

// ── StreamReader / StreamWriter — large files ─────────
// Large file-এ File.ReadAllText() memory-তে সব load করে → bad
// StreamReader line by line পড়ে → memory efficient

using var reader = new StreamReader("large_file.txt");
while (!reader.EndOfStream)
{
    string? line = reader.ReadLine();
    Console.WriteLine(line);
}

using var writer = new StreamWriter("output.txt", append: true);
writer.WriteLine("New entry: " + DateTime.Now);
// using block শেষে automatically flush ও close হয়

// ── FileStream — binary files ─────────────────────────
using var fs = new FileStream("binary.dat", FileMode.Create);
byte[] data = { 0x48, 0x65, 0x6C, 0x6C, 0x6F }; // "Hello"
fs.Write(data, 0, data.Length);

// ── Directory operations ──────────────────────────────
string dir = @"C:\Temp\MyApp";
if (!Directory.Exists(dir))
    Directory.CreateDirectory(dir);

string[] files = Directory.GetFiles(dir, "*.txt");
string[] subdirs = Directory.GetDirectories(dir);

// ── Path operations — cross-platform ─────────────────
string basePath = AppDomain.CurrentDomain.BaseDirectory;
string filePath = Path.Combine(basePath, "logs", "app.log");
// Path.Combine handles / vs \ automatically

string fileName = Path.GetFileName(filePath);      // "app.log"
string extension = Path.GetExtension(filePath);    // ".log"
string nameNoExt = Path.GetFileNameWithoutExtension(filePath); // "app"
string directory = Path.GetDirectoryName(filePath); // ".../logs"

// ── File Info & Directory Info ────────────────────────
var fileInfo = new FileInfo("data.txt");
Console.WriteLine($"Size: {fileInfo.Length} bytes");
Console.WriteLine($"Created: {fileInfo.CreationTime}");
Console.WriteLine($"Modified: {fileInfo.LastWriteTime}");

// ── Async File I/O (production-এ সবসময় async) ────────
async Task WriteLogAsync(string message)
{
    string logPath = Path.Combine("logs", "app.log");
    await File.AppendAllTextAsync(logPath, $"{DateTime.Now}: {message}\n");
}

async Task<string> ReadConfigAsync(string path)
{
    return await File.ReadAllTextAsync(path);
}
```

**Production File Pattern:**

```csharp
// ASP.NET Core-এ file upload handling
public async Task<string> SaveUploadedFile(IFormFile file, string uploadDir)
{
    if (file.Length == 0)
        throw new ArgumentException("Empty file");

    // Allowed extensions check
    var allowedExtensions = new[] { ".jpg", ".jpeg", ".png", ".pdf" };
    var extension = Path.GetExtension(file.FileName).ToLowerInvariant();
    if (!allowedExtensions.Contains(extension))
        throw new InvalidOperationException($"File type {extension} not allowed");

    // Unique filename — original name-এ trust করবেন না (security!)
    var uniqueFileName = $"{Guid.NewGuid()}{extension}";
    var filePath = Path.Combine(uploadDir, uniqueFileName);

    Directory.CreateDirectory(uploadDir); // ensure directory exists

    using var stream = new FileStream(filePath, FileMode.Create);
    await file.CopyToAsync(stream);

    return uniqueFileName;
}
```

---

<a id="p2-nullable"></a>
### Topic 12: Nullable Types

**Value Type Nullable:**

```csharp
// ── Nullable<T> — value type-কে null করার জন্য ────────
// int normally null হতে পারে না — এটা value type
// int? মানে Nullable<int>

int? age = null;         // age হয় int না হয় null
int? score = 85;

// Check করুন
if (age.HasValue)
    Console.WriteLine(age.Value);
else
    Console.WriteLine("Age not provided");

// Null-coalescing operator
int displayAge = age ?? 0;          // 0 if null
int displayScore = score ?? 0;      // 85

// Null-conditional + coalescing
int? dbScore = null;
int finalScore = dbScore ?? score ?? 0; // chain

// GetValueOrDefault
int safeAge = age.GetValueOrDefault();     // 0
int safeAge2 = age.GetValueOrDefault(18);  // 18 (custom default)

// ── Nullable arithmetic ────────────────────────────────
int? a = 10;
int? b = null;
int? sum = a + b;   // null — কোনো operand null হলে result null
int? mul = a * 3;   // 30

// ── Database থেকে nullable column read করা ────────────
// Entity Framework
public class Student
{
    public int Id { get; set; }
    public string Name { get; set; } = string.Empty;
    public int? PhoneNumber { get; set; }    // nullable column
    public DateTime? GraduationDate { get; set; } // nullable date
}
```

**C# 8+ Nullable Reference Types:**

```csharp
// .csproj এ enable করুন:
// <Nullable>enable</Nullable>

// এখন string null হতে পারে না by default
string name = "Rahim";
// name = null; // ⚠️ Warning!

// null হতে পারে এমন — ? দিতে হবে
string? nullableName = null; // ✅ OK

// Non-null assert — আপনি জানেন এটা null নয়
string definitelyNotNull = nullableName!; // ! = null-forgiving operator

// Pattern for ASP.NET Core:
public class UserDto
{
    public string Name { get; set; } = string.Empty;  // non-nullable
    public string? MiddleName { get; set; }             // nullable
    public string Email { get; set; } = string.Empty;
    public string? PhoneNumber { get; set; }
}

// Method signatures
public string GetUserName(int userId)     // never null
{
    return "Rahim"; // always return string
}

public string? FindUserEmail(int userId)  // might be null
{
    return null; // user not found
}

// Null check before use
string? email = FindUserEmail(5);
if (email is not null)
{
    Console.WriteLine(email.ToUpper()); // safe
}
// অথবা:
Console.WriteLine(email?.ToUpper() ?? "No email");
```

**🎤 Interview Q&A:**

```
প্রশ্ন: Nullable types কেন দরকার?

উত্তর:
Database-এ অনেক column optional (NULL হতে পারে)।
C#-এ int, bool, DateTime — এগুলো value type, null হয় না।
int? দিয়ে database-এর NULL represent করা যায়।

C# 8+ এ nullable reference types enable করলে
compiler warning দেয় যদি null dereference হওয়ার chance থাকে।
এটা NullReferenceException কমাতে সাহায্য করে।

প্রশ্ন: NullReferenceException কীভাবে prevent করবেন?

উত্তর:
1. null check: if (obj != null) বা if (obj is not null)
2. Null-conditional: obj?.Property
3. Null-coalescing: obj ?? defaultValue
4. C# 8+ nullable reference types enable করুন
5. Guard clauses: method শুরুতেই null throw করুন
   if (customer is null) throw new ArgumentNullException(nameof(customer));
```

---

<a id="p2-var-dynamic"></a>
### Topic 13: var vs dynamic

```csharp
// ── var — compile-time type inference ─────────────────
// Compiler compile-time-এ type determine করে
// Runtime-এ type পরিবর্তন করা যায় না

var name = "Rahim";          // string — compile-time fix
var count = 42;               // int
var prices = new List<decimal>(); // List<decimal>

// name = 100; // ❌ Compile error — type already fixed as string

// Hover করলে IDE type দেখাবে
// var শুধু local variable-এ ব্যবহার করা যায়
// Method return type, parameter, field-এ var যায় না

// Good use of var:
var customer = dbContext.Customers.Find(id);  // type long হতে পারে
var result = from c in customers where c.Age > 18 select c; // complex LINQ
var dict = new Dictionary<string, List<Customer>>(); // long type name

// ─────────────────────────────────────────────────────
// ── dynamic — runtime type resolution ────────────────
// Type check compile-time-এ হয় না — runtime-এ হয়
// Intellisense কাজ করে না
// Runtime error possible

dynamic obj = "Hello";
Console.WriteLine(obj.Length);     // 5 — string, OK

obj = 42;                          // ✅ type পরিবর্তন করা যায়!
Console.WriteLine(obj + 10);       // 52 — int now

obj = new List<int> { 1, 2, 3 };
Console.WriteLine(obj.Count);      // 3

// Runtime error:
// obj.NonExistentMethod(); // ❌ RuntimeBinderException at runtime

// ── Use cases for dynamic ─────────────────────────────
// 1. COM Interop (Office automation)
// dynamic excelApp = Activator.CreateInstance(Type.GetTypeFromProgID("Excel.Application"));
// excelApp.Visible = true;

// 2. JSON parsing with unknown structure
using System.Text.Json;
string json = """{"name":"Rahim","age":25}""";
dynamic jsonObj = JsonSerializer.Deserialize<dynamic>(json);

// 3. Reflection alternative
dynamic service = GetService("CustomerService");
service.ProcessOrder(orderId);
```

**var vs dynamic তুলনা:**

| বৈশিষ্ট্য | `var` | `dynamic` |
|-----------|-------|-----------|
| Type check | Compile-time | Runtime |
| Type পরিবর্তন | না | হ্যাঁ |
| Performance | Normal | Slower (runtime dispatch) |
| Intellisense | ✅ পূর্ণ | ❌ নেই |
| Error detection | Compile-time | Runtime |
| Use case | Clean code, LINQ | COM, JSON, Reflection |

**🎤 Interview Q&A:**

```
প্রশ্ন: var কি dynamic-এর মতো?

উত্তর: না — এটা একটি common misconception।

var → strongly typed, compile-time। Compiler type infer করে।
      Type পরিবর্তন করা যায় না। Performance normal।

dynamic → loosely typed, runtime। Type যেকোনো সময় পরিবর্তন হতে পারে।
          Runtime error possible। Performance slower।

var শুধু code লেখা সহজ করে — type safety একই থাকে।
dynamic সত্যিকারের runtime flexibility দেয়।

সাধারণ code-এ var ব্যবহার করুন, dynamic avoid করুন।
```

---

<a id="p2-stringbuilder"></a>
### Topic 14: String vs StringBuilder

**String Immutability:**

```csharp
// ── String immutable — প্রতিটি operation নতুন object ─
string str = "Hello";
str += ", World";  // নতুন string object তৈরি হয়, পুরানোটা garbage

// ❌ Loop-এ string concatenation — GC nightmare!
string result = "";
for (int i = 0; i < 10000; i++)
{
    result += i.ToString();  // প্রতি iteration নতুন object!
    // 10000 intermediate strings তৈরি হয় → GC pressure
}

// ── StringBuilder — mutable buffer ───────────────────
// একটি buffer-এ সব changes — কোনো intermediate object নেই
var sb = new StringBuilder();
for (int i = 0; i < 10000; i++)
{
    sb.Append(i);    // same buffer-এ add
}
string final = sb.ToString(); // শুধু একটি string তৈরি
```

**StringBuilder API:**

```csharp
var sb = new StringBuilder(capacity: 256); // initial capacity hint

// Append
sb.Append("Hello");
sb.Append(", ");
sb.Append("Bangladesh");
sb.AppendLine("!");            // Append + newline
sb.AppendFormat("Today: {0:dd/MM/yyyy}", DateTime.Now);
sb.Append($"Version: {1.0}");  // interpolation ও কাজ করে

// Insert / Remove / Replace
sb.Insert(5, " Dear");         // position 5-এ insert
sb.Remove(5, 5);               // position 5 থেকে 5 chars remove
sb.Replace("Bangladesh", "BD"); // replace all occurrences

// Access
Console.WriteLine(sb.Length);  // length
Console.WriteLine(sb[0]);      // 'H' — index access
sb[0] = 'h';                   // character modify

// Clear and reuse (object pooling pattern)
sb.Clear(); // reset — new StringBuilder() এর চেয়ে efficient

string result = sb.ToString();
```

**কখন কোনটা ব্যবহার করবেন:**

```csharp
// ── Use string when: ──────────────────────────────────
// 1. Concatenation কম (< 3-4 operations)
string greeting = "Hello, " + name + "!"; // fine

// 2. String interpolation — internally optimized
string msg = $"User {userId} logged in at {DateTime.Now}"; // fine

// 3. Immutability আপনার favor-এ (thread-safe, hash key)

// ── Use StringBuilder when: ───────────────────────────
// 1. Loop-এ concatenation
var htmlBuilder = new StringBuilder();
foreach (var item in menuItems)
{
    htmlBuilder.Append("<li>");
    htmlBuilder.Append(item.Name);
    htmlBuilder.AppendLine("</li>");
}

// 2. Dynamic SQL building (Dapper প্যাটার্ন)
var sql = new StringBuilder("SELECT * FROM Orders WHERE 1=1");
if (customerId.HasValue) sql.Append($" AND CustomerId = {customerId}");
if (startDate.HasValue) sql.Append($" AND OrderDate >= '{startDate:yyyy-MM-dd}'");

// 3. Large text generation (reports, CSV export)
async Task<string> GenerateCsvReport(List<Order> orders)
{
    var csv = new StringBuilder();
    csv.AppendLine("OrderId,CustomerId,Amount,Date");
    foreach (var order in orders)
    {
        csv.Append(order.Id).Append(',')
           .Append(order.CustomerId).Append(',')
           .Append(order.Amount).Append(',')
           .AppendLine(order.Date.ToString("yyyy-MM-dd"));
    }
    return csv.ToString();
}
```

**Performance Comparison:**

| Operation | String (+) | StringBuilder |
|-----------|-----------|---------------|
| 10 concatenations | Fast | Slightly slower (overhead) |
| 1000 concatenations | Very slow | Fast |
| 10,000 concatenations | Extremely slow | Fast |
| Memory allocations | Many | One buffer |
| GC pressure | High | Low |
| Thread safety | Immutable = safe | Not thread-safe |

**🎤 Interview-style Explanation:**

```
প্রশ্ন: String আর StringBuilder-এর পার্থক্য কী? কখন কোনটা ব্যবহার করবেন?

উত্তর:
String immutable — প্রতিটি modification নতুন string object তৈরি করে।
Loop-এ string concatenation করলে হাজার হাজার intermediate
objects তৈরি হয় — GC pressure বাড়ে, performance কমে।

StringBuilder mutable — একটি buffer-এ সব changes হয়।
Loop-এ append করলে শুধু buffer grow হয়, নতুন object নয়।

Rule of thumb:
- 3-4 concatenation → string বা interpolation fine
- Loop-এ concatenation → StringBuilder ব্যবহার করুন
- HTML/CSV/SQL building → StringBuilder
```

---

## PART 2 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| `int` | 32-bit integer, ±2 billion |
| `decimal` | Financial calculation — no floating point error |
| `var` | Compile-time type inference, strongly typed |
| `dynamic` | Runtime type, loosely typed, avoid unless needed |
| Value Type | Stack-stored, copy on assignment (int, struct, enum) |
| Reference Type | Heap-stored, reference copy (class, array, string) |
| `ref` parameter | Reference pass — original পরিবর্তন হয় |
| `out` parameter | Multiple return values |
| `params` | Variable number of arguments |
| Array | Fixed size, O(1) access |
| List\<T\> | Dynamic array, Add/Remove সহজ |
| Dictionary\<K,V\> | O(1) key lookup |
| HashSet\<T\> | Unique elements, fast Contains |
| String | Immutable — + করলে নতুন object |
| StringBuilder | Mutable buffer — loop concatenation-এ |
| `int?` | Nullable value type |
| `string?` | Nullable reference type (C# 8+) |
| `??` | Null-coalescing: left ?? right |
| `?.` | Null-conditional: obj?.Property |
| try-catch-finally | Exception handling — finally সবসময় চলে |
| `throw;` | Original stack trace preserve করে rethrow |
| Custom Exception | Exception inherit করে তৈরি করুন |
| TryParse | Safe parsing — exception throw করে না |

---

## PART 2 Interview Q&A

```
প্রশ্ন: int? কী?
উত্তর: Nullable<int> — int null হতে পারে।
Database-এ NULL value represent করার জন্য।

প্রশ্ন: var কি type-safe?
উত্তর: হ্যাঁ। var compile-time type infer করে।
dynamic-এর মতো runtime loose নয়।

প্রশ্ন: foreach-এ List modify করা যায় না কেন?
উত্তর: Enumerator invalidate হয়ে যায়।
InvalidOperationException throw করে।
Solution: ToList() copy করে iterate করুন।

প্রশ্ন: throw আর throw ex পার্থক্য?
উত্তর: throw — original stack trace রাখে।
throw ex — stack trace reset করে। সবসময় throw ব্যবহার করুন।

প্রশ্ন: String কেন immutable?
উত্তর: Thread safety, hashing consistency, security।
string Pool-এ intern করা যায়।

প্রশ্ন: Dictionary-এ key না থাকলে কী হয়?
উত্তর: direct access → KeyNotFoundException।
TryGetValue → safe, false return করে।
সবসময় TryGetValue ব্যবহার করুন।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 3 — OOP in C# (Class, Object, Encapsulation, Inheritance, Polymorphism, SOLID Principles এবং আরও...)

---

<a id="part3"></a>
## PART 3: OOP in C#

> Class & Object, Constructor & Destructor, Encapsulation, Abstraction, Inheritance, Polymorphism, Method Overloading & Overriding, Abstract Class, Interface, Sealed Class, Static Class, Access Modifiers, SOLID Principles, Dependency Injection।

| # | বিষয় |
|---|-------|
| 1 | [Class ও Object](#p3-class-object) |
| 2 | [Constructor ও Destructor](#p3-constructor) |
| 3 | [Encapsulation](#p3-encapsulation) |
| 4 | [Abstraction](#p3-abstraction) |
| 5 | [Inheritance](#p3-inheritance) |
| 6 | [Polymorphism](#p3-polymorphism) |
| 7 | [Method Overloading vs Overriding](#p3-overload-override) |
| 8 | [Abstract Class](#p3-abstract-class) |
| 9 | [Interface](#p3-interface) |
| 10 | [Abstract Class vs Interface](#p3-abstract-vs-interface) |
| 11 | [Sealed Class ও Static Class](#p3-sealed-static) |
| 12 | [Access Modifiers](#p3-access-modifiers) |
| 13 | [SOLID Principles](#p3-solid) |
| 14 | [Dependency Injection Basics](#p3-di) |

---

<a id="p3-class-object"></a>
### Topic 1: Class ও Object

**সহজ ভাষায়:**

- **Class** হলো **blueprint** বা ছাঁচ — যেমন বাড়ির নকশা।
- **Object** হলো সেই ছাঁচ থেকে তৈরি **real instance** — যেমন নকশা থেকে তৈরি আসল বাড়ি।

```csharp
// ── Class definition ──────────────────────────────────
public class BankAccount
{
    // ── Fields (state) ─────────────────────────────────
    private string _accountNumber;
    private decimal _balance;
    private readonly string _ownerName;

    // ── Properties (controlled access to fields) ───────
    public string AccountNumber => _accountNumber;
    public string OwnerName => _ownerName;
    public decimal Balance => _balance; // read-only outside

    // ── Auto-property ──────────────────────────────────
    public DateTime CreatedAt { get; private set; }
    public bool IsActive { get; set; } = true;

    // ── Constructor ────────────────────────────────────
    public BankAccount(string accountNumber, string ownerName, decimal initialDeposit)
    {
        _accountNumber = accountNumber;
        _ownerName = ownerName;
        _balance = initialDeposit;
        CreatedAt = DateTime.UtcNow;
    }

    // ── Methods (behaviour) ────────────────────────────
    public void Deposit(decimal amount)
    {
        if (amount <= 0)
            throw new ArgumentException("Deposit amount must be positive");
        _balance += amount;
    }

    public bool Withdraw(decimal amount)
    {
        if (amount <= 0 || amount > _balance) return false;
        _balance -= amount;
        return true;
    }

    public override string ToString() =>
        $"Account: {_accountNumber} | Owner: {_ownerName} | Balance: {_balance:C}";
}

// ── Object creation ───────────────────────────────────
var account1 = new BankAccount("BD001", "Rahim", 10000m);
var account2 = new BankAccount("BD002", "Karim", 5000m);

// প্রতিটি object তার নিজস্ব state রাখে
account1.Deposit(2000m);
account2.Withdraw(1000m);

Console.WriteLine(account1); // Account: BD001 | Owner: Rahim | Balance: ৳12,000.00
Console.WriteLine(account2); // Account: BD002 | Owner: Karim | Balance: ৳4,000.00
```

**Record (C# 9+) — immutable data objects:**

```csharp
// Record — value equality, immutable by default
public record Customer(int Id, string Name, string Email);

var c1 = new Customer(1, "Rahim", "rahim@example.com");
var c2 = new Customer(1, "Rahim", "rahim@example.com");

Console.WriteLine(c1 == c2);    // true — value equality (class হলে false হতো!)
Console.WriteLine(c1.Name);     // "Rahim"
// c1.Name = "Karim"; // ❌ init-only, immutable

// Non-destructive mutation (with expression)
var c3 = c1 with { Email = "new@example.com" };
Console.WriteLine(c3); // Customer { Id = 1, Name = Rahim, Email = new@example.com }
```

**Struct vs Class:**

```csharp
// ── Struct — Value type, stack allocated ──────────────
public struct Point
{
    public double X { get; init; }
    public double Y { get; init; }

    public Point(double x, double y) { X = x; Y = y; }
    public double DistanceTo(Point other) =>
        Math.Sqrt(Math.Pow(X - other.X, 2) + Math.Pow(Y - other.Y, 2));
}

// ── Class — Reference type, heap allocated ────────────
public class PointClass
{
    public double X { get; set; }
    public double Y { get; set; }
}

Point p1 = new Point(3, 4);
Point p2 = p1;  // COPY — value type
p2 = p2 with { X = 10 }; // p1 unchanged

PointClass pc1 = new PointClass { X = 3, Y = 4 };
PointClass pc2 = pc1;  // REFERENCE — same object!
pc2.X = 10;            // pc1.X ও 10 হয়ে যাবে!
```

| বৈশিষ্ট্য | Class | Struct |
|-----------|-------|--------|
| Type | Reference type | Value type |
| Memory | Heap | Stack |
| Null হতে পারে | হ্যাঁ | না (Nullable<T> ছাড়া) |
| Inheritance | হ্যাঁ | না |
| Default copy | Reference copy | Value copy |
| Use case | Complex objects | Small, simple data |

---

<a id="p3-constructor"></a>
### Topic 2: Constructor ও Destructor

**Constructor:**

```csharp
public class Person
{
    public string Name { get; }
    public int Age { get; }
    public string Email { get; private set; }

    // ── 1. Default Constructor ─────────────────────────
    // C# automatically তৈরি করে যদি কোনো constructor না থাকে
    // যদি কোনো constructor define করেন, default আর থাকে না

    // ── 2. Parameterized Constructor ──────────────────
    public Person(string name, int age)
    {
        Name = name;
        Age = age;
        Email = $"{name.ToLower().Replace(" ", ".")}@example.com";
    }

    // ── 3. Constructor Overloading ─────────────────────
    public Person(string name) : this(name, 0)
    // this(name, 0) → অন্য constructor call করে (constructor chaining)
    {
    }

    // ── 4. Static Constructor — class load-এর সময় একবার ─
    static Person()
    {
        Console.WriteLine("Person class loaded");
        // Static fields initialize করার জন্য
    }

    // ── 5. Copy Constructor ────────────────────────────
    public Person(Person other) : this(other.Name, other.Age)
    {
        Email = other.Email;
    }
}

var p1 = new Person("Rahim", 25);
var p2 = new Person("Karim");       // Age = 0
var p3 = new Person(p1);            // copy of p1

Console.WriteLine(p1.Name);         // "Rahim"
Console.WriteLine(p1.Email);        // "rahim@example.com"
```

**Object Initializer (Constructor alternative):**

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; } = string.Empty;
    public decimal Price { get; set; }
    public string Category { get; set; } = "General";
    public bool IsAvailable { get; set; } = true;

    // Required properties (C# 11+)
    public required string SKU { get; set; }
}

// Object initializer — named properties দিয়ে set করা
var product = new Product
{
    Id = 1,
    Name = "Laptop",
    Price = 75000m,
    Category = "Electronics",
    SKU = "LAP-001"         // required — must be set
};

// Primary Constructor (C# 12+) — clean syntax
public class OrderService(IOrderRepository repo, ILogger<OrderService> logger)
{
    public async Task<Order> GetOrderAsync(int id) =>
        await repo.GetByIdAsync(id) ?? throw new KeyNotFoundException();
}
```

**Destructor / Finalizer:**

```csharp
public class ResourceHolder
{
    private IntPtr _handle;   // unmanaged resource
    private bool _disposed = false;

    public ResourceHolder()
    {
        _handle = /* allocate native resource */ IntPtr.Zero;
    }

    // ── Destructor / Finalizer ─────────────────────────
    // GC যখন object collect করে তখন call করে
    // ~ClassName() — কখন call হবে guarantee নেই
    // Expensive — GC-এ extra work করে
    ~ResourceHolder()
    {
        Dispose(false);
        Console.WriteLine("Finalizer called");
    }

    // ── IDisposable pattern — সঠিক উপায় ──────────────
    public void Dispose()
    {
        Dispose(true);
        GC.SuppressFinalize(this); // finalizer আর দরকার নেই
    }

    protected virtual void Dispose(bool disposing)
    {
        if (_disposed) return;

        if (disposing)
        {
            // Managed resources dispose করুন
        }
        // Unmanaged resources release করুন
        _handle = IntPtr.Zero;
        _disposed = true;
    }
}

// using statement — automatically Dispose() call করে
using var resource = new ResourceHolder();
// resource.Dispose() automatically called এমনকি exception হলেও
```

**🎤 Interview Q&A:**

```
প্রশ্ন: Constructor আর Destructor এর কাজ কী?

উত্তর:
Constructor → Object তৈরির সময় call হয়। Initial state set করে।
Destructor → Object destroy হওয়ার আগে GC call করে। Unmanaged
             resources cleanup-এর জন্য। কখন call হবে নিশ্চিত নয়।

সাধারণত IDisposable + using pattern ব্যবহার করুন।
Destructor শুধু unmanaged resources-এর জন্য।

প্রশ্ন: Static constructor কী?

উত্তর: Class প্রথমবার use হওয়ার সময় একবারই call হয়।
Static fields initialize করার জন্য।
Parameter নেই, access modifier নেই।
```

---

<a id="p3-encapsulation"></a>
### Topic 3: Encapsulation

**সহজ ভাষায়:**

> **Encapsulation** মানে data ও methods এক জায়গায় bundle করা এবং internal details **লুকিয়ে রাখা**। বাইরে থেকে শুধু যা দরকার তাই expose করা।

**Analogy:** ATM machine — আপনি PIN দেন ও টাকা তোলেন। ভেতরে কীভাবে transaction process হয় জানেন না — এটাই encapsulation।

```csharp
public class SavingsAccount
{
    // ── Private fields — বাইরে সরাসরি access নেই ──────
    private decimal _balance;
    private readonly decimal _minimumBalance = 500m;
    private readonly List<string> _transactionLog = new();

    // ── Public property — controlled read access ───────
    public decimal Balance => _balance; // get only

    public IReadOnlyList<string> TransactionHistory =>
        _transactionLog.AsReadOnly(); // safe read-only view

    // ── Constructor — initial state setup ─────────────
    public SavingsAccount(decimal initialDeposit)
    {
        if (initialDeposit < _minimumBalance)
            throw new InvalidOperationException(
                $"Minimum initial deposit is {_minimumBalance:C}");
        _balance = initialDeposit;
        Log($"Account opened with {initialDeposit:C}");
    }

    // ── Public methods — controlled behaviour ──────────
    public void Deposit(decimal amount)
    {
        ValidateAmount(amount);
        _balance += amount;
        Log($"Deposited {amount:C}. New balance: {_balance:C}");
    }

    public bool Withdraw(decimal amount)
    {
        ValidateAmount(amount);
        if (_balance - amount < _minimumBalance)
        {
            Log($"Withdrawal {amount:C} denied — minimum balance rule");
            return false;
        }
        _balance -= amount;
        Log($"Withdrew {amount:C}. New balance: {_balance:C}");
        return true;
    }

    // ── Private helper — internal implementation ───────
    private void ValidateAmount(decimal amount)
    {
        if (amount <= 0)
            throw new ArgumentException("Amount must be positive");
    }

    private void Log(string message) =>
        _transactionLog.Add($"[{DateTime.Now:HH:mm:ss}] {message}");
}

// ── Usage ─────────────────────────────────────────────
var account = new SavingsAccount(1000m);
account.Deposit(500m);
account.Withdraw(900m);         // false — would go below minimum

// account._balance = 1000000m; // ❌ Compile error — private!
Console.WriteLine(account.Balance); // only way to see balance
```

**Properties — Encapsulation-এর মূল হাতিয়ার:**

```csharp
public class Employee
{
    private string _name = string.Empty;
    private int _age;
    private decimal _salary;

    // Full property with validation
    public string Name
    {
        get => _name;
        set
        {
            if (string.IsNullOrWhiteSpace(value))
                throw new ArgumentException("Name cannot be empty");
            _name = value.Trim();
        }
    }

    // Property with range validation
    public int Age
    {
        get => _age;
        set
        {
            if (value < 18 || value > 65)
                throw new ArgumentOutOfRangeException(nameof(Age), "Age must be 18-65");
            _age = value;
        }
    }

    // Computed / derived property
    public decimal MonthlySalary
    {
        get => _salary;
        private set => _salary = value > 0 ? value : 0;
    }
    public decimal AnnualSalary => _salary * 12; // computed

    // Init-only property (C# 9+) — constructor or initializer only
    public string EmployeeId { get; init; } = Guid.NewGuid().ToString();
}
```

---

<a id="p3-abstraction"></a>
### Topic 4: Abstraction

**সহজ ভাষায়:**

> **Abstraction** মানে complexity লুকিয়ে শুধু **relevant details** expose করা। "কী করে" বলুন, "কীভাবে করে" লুকান।

**Analogy:** Car চালানো — accelerator চাপলে গাড়ি যায়। Engine internally কীভাবে কাজ করে জানতে হয় না।

```csharp
// ── Abstract class দিয়ে abstraction ──────────────────
public abstract class PaymentProcessor
{
    // Abstract method — subclass MUST implement করবে
    public abstract bool ProcessPayment(decimal amount, string reference);
    public abstract string GetProviderName();

    // Concrete method — shared behaviour
    public string GenerateReference() =>
        $"PAY-{DateTime.Now:yyyyMMddHHmmss}-{Guid.NewGuid().ToString("N")[..8].ToUpper()}";

    // Template method pattern — algorithm structure define করে
    public bool Execute(decimal amount)
    {
        if (amount <= 0) return false;
        string reference = GenerateReference();
        bool success = ProcessPayment(amount, reference);
        if (success)
            LogSuccess(amount, reference);
        else
            LogFailure(amount, reference);
        return success;
    }

    private void LogSuccess(decimal amount, string ref_) =>
        Console.WriteLine($"[{GetProviderName()}] ৳{amount} paid. Ref: {ref_}");

    private void LogFailure(decimal amount, string ref_) =>
        Console.WriteLine($"[{GetProviderName()}] Payment ৳{amount} FAILED. Ref: {ref_}");
}

// Concrete implementations — internal details different কিন্তু interface same
public class BkashProcessor : PaymentProcessor
{
    private readonly string _merchantId;

    public BkashProcessor(string merchantId) => _merchantId = merchantId;

    public override string GetProviderName() => "bKash";

    public override bool ProcessPayment(decimal amount, string reference)
    {
        // bKash-specific API call
        Console.WriteLine($"Calling bKash API for merchant {_merchantId}...");
        return true; // simulate success
    }
}

public class NagadProcessor : PaymentProcessor
{
    public override string GetProviderName() => "Nagad";

    public override bool ProcessPayment(decimal amount, string reference)
    {
        // Nagad-specific API call
        Console.WriteLine("Calling Nagad API...");
        return true;
    }
}

// ── Usage — caller doesn't care about internals ───────
PaymentProcessor processor = new BkashProcessor("MERCHANT-001");
processor.Execute(500m);

processor = new NagadProcessor();
processor.Execute(1000m);
// Same interface, different internal implementations
```

---

<a id="p3-inheritance"></a>
### Topic 5: Inheritance

**সহজ ভাষায়:**

> **Inheritance** মানে parent class-এর properties ও methods **child class পেয়ে যায়**। Code reuse ও "is-a" relationship।

**Analogy:** Manager is-a Employee। Manager সব Employee কাজ করতে পারে + নিজস্ব extra কাজ।

```csharp
// ── Base class (Parent) ───────────────────────────────
public class Employee
{
    public int Id { get; set; }
    public string Name { get; set; } = string.Empty;
    public decimal BaseSalary { get; protected set; }
    public DateTime JoinDate { get; set; }

    public Employee(int id, string name, decimal baseSalary)
    {
        Id = id;
        Name = name;
        BaseSalary = baseSalary;
        JoinDate = DateTime.Today;
    }

    public virtual decimal CalculateSalary()  // virtual — override করা যাবে
    {
        return BaseSalary;
    }

    public virtual string GetRole() => "Employee";

    public void ClockIn() => Console.WriteLine($"{Name} clocked in");
    public void ClockOut() => Console.WriteLine($"{Name} clocked out");

    public override string ToString() =>
        $"[{GetRole()}] {Name} | Salary: {CalculateSalary():C}";
}

// ── Derived class (Child) ─────────────────────────────
public class SalesEmployee : Employee
{
    public decimal CommissionRate { get; set; }  // extra property
    public decimal MonthlySales { get; set; }

    public SalesEmployee(int id, string name, decimal baseSalary, decimal commissionRate)
        : base(id, name, baseSalary)  // base constructor call
    {
        CommissionRate = commissionRate;
    }

    // override — polymorphism
    public override decimal CalculateSalary() =>
        BaseSalary + (MonthlySales * CommissionRate / 100);

    public override string GetRole() => "Sales Executive";
}

// ── Multi-level inheritance ────────────────────────────
public class SalesManager : SalesEmployee
{
    public List<SalesEmployee> TeamMembers { get; } = new();

    public SalesManager(int id, string name, decimal baseSalary)
        : base(id, name, baseSalary, commissionRate: 5) { }

    public override decimal CalculateSalary()
    {
        decimal teamBonus = TeamMembers.Sum(m => m.MonthlySales) * 0.01m;
        return base.CalculateSalary() + teamBonus;  // base class method call
    }

    public override string GetRole() => "Sales Manager";

    public void AddTeamMember(SalesEmployee emp) => TeamMembers.Add(emp);
}

// ── Usage ─────────────────────────────────────────────
var emp = new Employee(1, "Rahim", 30000m);
var sales = new SalesEmployee(2, "Karim", 25000m, 3)
{
    MonthlySales = 200000m
};
var manager = new SalesManager(3, "Jamal", 50000m);
manager.AddTeamMember(sales);

Console.WriteLine(emp);      // [Employee] Rahim | Salary: ৳30,000.00
Console.WriteLine(sales);    // [Sales Executive] Karim | Salary: ৳31,000.00
Console.WriteLine(manager);  // [Sales Manager] Jamal | Salary: ...

// ── Type checking ─────────────────────────────────────
Employee e = manager;       // upcasting — implicit, safe
Console.WriteLine(e is SalesManager);    // true
Console.WriteLine(e is SalesEmployee);   // true (inheritance chain)
Console.WriteLine(e is Employee);        // true

var m = e as SalesManager;  // downcasting — explicit
if (m is not null) Console.WriteLine(m.TeamMembers.Count);
```

**Inheritance Rules — C#:**

```
✅ C# supports single inheritance (একটি class একটি base class থেকে inherit করে)
✅ Multi-level inheritance (A → B → C) supported
✅ Multiple interface implementation supported
❌ Multiple class inheritance নেই (C++ এর মতো)

sealed class → inherit করা যায় না
abstract class → directly instantiate করা যায় না
```

---

<a id="p3-polymorphism"></a>
### Topic 6: Polymorphism

**সহজ ভাষায়:**

> **Polymorphism** মানে **একই interface, ভিন্ন behaviour**। Same method call → object অনুযায়ী ভিন্ন কাজ।

**Analogy:** "Draw()" বললে Circle বৃত্ত আঁকে, Square বর্গ আঁকে — একই call, ভিন্ন result।

**Runtime Polymorphism (virtual/override):**

```csharp
public abstract class Shape
{
    public string Color { get; set; } = "Black";
    public abstract double Area();         // abstract — must override
    public abstract double Perimeter();
    public virtual void Draw()             // virtual — can override
    {
        Console.WriteLine($"Drawing {GetType().Name} in {Color}");
    }
    public override string ToString() =>
        $"{GetType().Name}: Area={Area():F2}, Perimeter={Perimeter():F2}";
}

public class Circle : Shape
{
    public double Radius { get; init; }
    public Circle(double radius) => Radius = radius;
    public override double Area() => Math.PI * Radius * Radius;
    public override double Perimeter() => 2 * Math.PI * Radius;
}

public class Rectangle : Shape
{
    public double Width { get; init; }
    public double Height { get; init; }
    public Rectangle(double width, double height) { Width = width; Height = height; }
    public override double Area() => Width * Height;
    public override double Perimeter() => 2 * (Width + Height);
    public override void Draw()
    {
        base.Draw(); // parent method call
        Console.WriteLine($"  Width: {Width}, Height: {Height}");
    }
}

public class Triangle : Shape
{
    public double A { get; init; }
    public double B { get; init; }
    public double C { get; init; }
    public Triangle(double a, double b, double c) { A = a; B = b; C = c; }
    public override double Perimeter() => A + B + C;
    public override double Area()
    {
        double s = Perimeter() / 2;
        return Math.Sqrt(s * (s - A) * (s - B) * (s - C)); // Heron's formula
    }
}

// ── Polymorphic behaviour ─────────────────────────────
var shapes = new List<Shape>
{
    new Circle(5),
    new Rectangle(4, 6),
    new Triangle(3, 4, 5)
};

// Same method call → different behaviour per object
foreach (Shape shape in shapes)
{
    shape.Draw();                         // runtime dispatch
    Console.WriteLine(shape.Area());      // each calculates differently
}

// Total area — doesn't need to know specific types
double totalArea = shapes.Sum(s => s.Area());
Console.WriteLine($"Total area: {totalArea:F2}");
```

**Compile-time Polymorphism (Overloading):**

```csharp
public class Printer
{
    // Same name, different signature — compile-time resolution
    public void Print(string text) =>
        Console.WriteLine($"Text: {text}");

    public void Print(int number) =>
        Console.WriteLine($"Number: {number}");

    public void Print(string text, ConsoleColor color)
    {
        Console.ForegroundColor = color;
        Console.WriteLine(text);
        Console.ResetColor();
    }

    public void Print(object obj) =>
        Console.WriteLine($"Object: {obj}");
}
```

---

<a id="p3-overload-override"></a>
### Topic 7: Method Overloading vs Overriding

```
─────────────────────────────────────────────────────────
         Overloading          vs        Overriding
─────────────────────────────────────────────────────────
 Same class                       Parent-Child class
 Same name, different params      Same name, same params
 Compile-time resolution          Runtime resolution
 No inheritance needed            Requires inheritance
 virtual/override নেই             virtual + override keyword
 Static / instance উভয়           Instance methods only
 Return type ভিন্ন হতে পারে       Return type same হতে হবে
─────────────────────────────────────────────────────────
```

```csharp
public class Calculator
{
    // ── Overloading — same class, different parameters ─
    public int Add(int a, int b) => a + b;
    public double Add(double a, double b) => a + b;
    public decimal Add(decimal a, decimal b) => a + b;
    public int Add(int a, int b, int c) => a + b + c;
    // Compile-time — parameter types দেখে সঠিক version call করে
}

public class Animal
{
    public virtual string Speak() => "...";   // virtual
    public string Name { get; set; } = "Animal";
}

public class Dog : Animal
{
    public override string Speak() => "Woof!";  // override
    // Same signature, different implementation
}

public class Cat : Animal
{
    public override string Speak() => "Meow!";  // override
}

// Polymorphic call — runtime decides
Animal[] animals = { new Dog(), new Cat(), new Animal() };
foreach (var a in animals)
    Console.WriteLine(a.Speak()); // Woof! / Meow! / ...

// ── new keyword — hiding (NOT overriding) ─────────────
public class Base
{
    public virtual void Method() => Console.WriteLine("Base.Method");
}

public class Derived : Base
{
    // override — polymorphic, runtime dispatch
    public override void Method() => Console.WriteLine("Derived.Method (override)");
}

public class HiddenDerived : Base
{
    // new — hides base method, NOT polymorphic!
    public new void Method() => Console.WriteLine("HiddenDerived.Method (new/hide)");
}

Base b = new Derived();
b.Method(); // "Derived.Method (override)" — runtime dispatch works

Base h = new HiddenDerived();
h.Method(); // "Base.Method" ← Base version! hiding is NOT polymorphic
```

**🎤 Interview Trap:**

```
প্রশ্ন: override আর new-এর পার্থক্য?

উত্তর:
override → polymorphism। Base class reference দিয়ে call করলেও
          derived class-এর version call হয়। Runtime dispatch।

new → method hiding। Base class reference হলে base version call হয়।
     Polymorphism কাজ করে না।

Production code-এ সবসময় override ব্যবহার করুন।
new/hiding rarely useful — mostly confusing।
```

---

<a id="p3-abstract-class"></a>
### Topic 8: Abstract Class

**সহজ ভাষায়:**

> Abstract class হলো **incomplete blueprint** — কিছু method define করে, কিছু implement করে না। Subclass-কে বাকি কাজ complete করতে হয়।

```csharp
// abstract class — directly instantiate করা যায় না
public abstract class ReportGenerator
{
    // Abstract methods — MUST be overridden
    protected abstract string GetTitle();
    protected abstract IEnumerable<string> GetData();
    protected abstract string FormatRow(string data);

    // Concrete methods — shared implementation
    public string GenerateHeader() =>
        $"=== {GetTitle()} — Generated: {DateTime.Now:dd/MM/yyyy} ===";

    public string GenerateFooter() =>
        $"=== Total: {GetData().Count()} records ===";

    // Template Method — defines the algorithm structure
    public string Generate()
    {
        var sb = new System.Text.StringBuilder();
        sb.AppendLine(GenerateHeader());
        foreach (var item in GetData())
            sb.AppendLine(FormatRow(item));
        sb.AppendLine(GenerateFooter());
        return sb.ToString();
    }

    // Virtual — can optionally override
    protected virtual string GetSeparator() => new string('-', 50);
}

// Concrete implementation — all abstract methods implemented
public class SalesReport : ReportGenerator
{
    private readonly List<(string Product, decimal Amount)> _sales;

    public SalesReport(List<(string, decimal)> sales) => _sales = sales;

    protected override string GetTitle() => "Monthly Sales Report";

    protected override IEnumerable<string> GetData() =>
        _sales.Select(s => $"{s.Product}|{s.Amount:C}");

    protected override string FormatRow(string data)
    {
        var parts = data.Split('|');
        return $"  {parts[0],-20} {parts[1],12}";
    }
}

public class InventoryReport : ReportGenerator
{
    private readonly Dictionary<string, int> _stock;

    public InventoryReport(Dictionary<string, int> stock) => _stock = stock;

    protected override string GetTitle() => "Inventory Status Report";
    protected override IEnumerable<string> GetData() =>
        _stock.Select(kv => $"{kv.Key}|{kv.Value}");
    protected override string FormatRow(string data)
    {
        var parts = data.Split('|');
        string status = int.Parse(parts[1]) < 10 ? "⚠ LOW" : "OK";
        return $"  {parts[0],-20} {parts[1],5} units  [{status}]";
    }
}

// Usage
// var r = new ReportGenerator(); // ❌ Cannot instantiate abstract class!

var salesReport = new SalesReport(new List<(string, decimal)>
{
    ("Laptop", 75000m), ("Mouse", 800m), ("Keyboard", 1500m)
});
Console.WriteLine(salesReport.Generate());
```

---

<a id="p3-interface"></a>
### Topic 9: Interface

**সহজ ভাষায়:**

> **Interface** হলো **contract** — "তুমি এই কাজগুলো করতে পারবে" এই guarantee। Class-কে implement করতে হবে। কোনো implementation নেই (C# 8 default interface members আসার আগে)।

```csharp
// ── Interface definition ──────────────────────────────
public interface IRepository<T> where T : class
{
    Task<T?> GetByIdAsync(int id);
    Task<IEnumerable<T>> GetAllAsync();
    Task<T> AddAsync(T entity);
    Task UpdateAsync(T entity);
    Task DeleteAsync(int id);
    Task<bool> ExistsAsync(int id);
}

public interface ISearchable<T>
{
    Task<IEnumerable<T>> SearchAsync(string query);
    Task<IEnumerable<T>> FilterAsync(Func<T, bool> predicate);
}

// ── Multiple interface implementation ─────────────────
public class CustomerRepository : IRepository<Customer>, ISearchable<Customer>
{
    private readonly AppDbContext _context;

    public CustomerRepository(AppDbContext context) => _context = context;

    // IRepository<Customer> implementation
    public async Task<Customer?> GetByIdAsync(int id) =>
        await _context.Customers.FindAsync(id);

    public async Task<IEnumerable<Customer>> GetAllAsync() =>
        await _context.Customers.ToListAsync();

    public async Task<Customer> AddAsync(Customer customer)
    {
        _context.Customers.Add(customer);
        await _context.SaveChangesAsync();
        return customer;
    }

    public async Task UpdateAsync(Customer customer)
    {
        _context.Customers.Update(customer);
        await _context.SaveChangesAsync();
    }

    public async Task DeleteAsync(int id)
    {
        var customer = await GetByIdAsync(id);
        if (customer is not null)
        {
            _context.Customers.Remove(customer);
            await _context.SaveChangesAsync();
        }
    }

    public async Task<bool> ExistsAsync(int id) =>
        await _context.Customers.AnyAsync(c => c.Id == id);

    // ISearchable<Customer> implementation
    public async Task<IEnumerable<Customer>> SearchAsync(string query) =>
        await _context.Customers
            .Where(c => c.Name.Contains(query) || c.Email.Contains(query))
            .ToListAsync();

    public async Task<IEnumerable<Customer>> FilterAsync(Func<Customer, bool> predicate) =>
        (await GetAllAsync()).Where(predicate);
}

// ── Interface-based programming (Dependency Inversion) ─
public class CustomerService
{
    private readonly IRepository<Customer> _repository;
    private readonly ISearchable<Customer> _search;

    // Constructor injection — interface দিয়ে, concrete class নয়
    public CustomerService(IRepository<Customer> repository, ISearchable<Customer> search)
    {
        _repository = repository;
        _search = search;
    }

    public async Task<Customer?> GetCustomerAsync(int id) =>
        await _repository.GetByIdAsync(id);

    public async Task<IEnumerable<Customer>> FindCustomersAsync(string query) =>
        await _search.SearchAsync(query);
}

// ── Default Interface Methods (C# 8+) ─────────────────
public interface ILogger
{
    void Log(string message);

    // Default implementation — override করতে হবে না
    void LogWarning(string message) => Log($"[WARN] {message}");
    void LogError(string message) => Log($"[ERROR] {message}");
    void LogInfo(string message) => Log($"[INFO] {message}");
}

public class ConsoleLogger : ILogger
{
    public void Log(string message) => Console.WriteLine(message);
    // LogWarning/LogError/LogInfo — default implementations ব্যবহার হবে
}
```

---

<a id="p3-abstract-vs-interface"></a>
### Topic 10: Abstract Class vs Interface

```
─────────────────────────────────────────────────────────────
         Abstract Class              vs        Interface
─────────────────────────────────────────────────────────────
 Partial implementation allowed          No impl (C# 8 default আছে)
 Fields, constructors allowed            No fields, no constructors
 Single inheritance                      Multiple implementation
 "is-a" relationship                     "can-do" capability
 Access modifiers on members             All public by default
 State (fields) রাখা যায়                State রাখা যায় না
 Use: shared base behaviour              Use: capability contract
─────────────────────────────────────────────────────────────
```

**কখন কোনটা ব্যবহার করবেন:**

```csharp
// ── Use Abstract Class when: ──────────────────────────
// Related classes যাদের common state ও behaviour আছে

public abstract class Vehicle
{
    // Common state
    protected int _speed = 0;
    protected int _fuel;

    // Common behaviour
    public void Accelerate(int amount) => _speed += amount;
    public void Brake(int amount) => _speed = Math.Max(0, _speed - amount);

    // Subclass-specific — must implement
    public abstract void StartEngine();
    public abstract int GetMaxSpeed();
}

// ── Use Interface when: ───────────────────────────────
// Unrelated classes share a capability

public interface ISerializable { string Serialize(); }
public interface IPrintable { void Print(); }
public interface IComparable<T> { int CompareTo(T other); }

// Car এবং Log — সম্পূর্ণ আলাদা কিন্তু উভয়ই serializable
public class Car : Vehicle, ISerializable, IPrintable
{
    public override void StartEngine() => Console.WriteLine("Vroom!");
    public override int GetMaxSpeed() => 200;
    public string Serialize() => System.Text.Json.JsonSerializer.Serialize(this);
    public void Print() => Console.WriteLine($"Car: speed={_speed}");
}

public class AuditLog : ISerializable, IPrintable
{
    public string Message { get; set; } = string.Empty;
    public string Serialize() => $"LOG: {Message}";
    public void Print() => Console.WriteLine(Serialize());
}

// ── Real-world pattern — combined ─────────────────────
// Abstract base + interface
public abstract class BaseService<T> : IDisposable where T : class
{
    protected readonly ILogger _logger;
    private bool _disposed;

    protected BaseService(ILogger logger) => _logger = logger;

    public abstract Task<T?> GetAsync(int id);

    protected virtual void Log(string msg) => _logger.Log(msg);

    public void Dispose()
    {
        if (!_disposed)
        {
            OnDispose();
            _disposed = true;
        }
    }
    protected virtual void OnDispose() { }
}
```

**🎤 Interview Q&A:**

```
প্রশ্ন: Abstract class কখন, Interface কখন?

উত্তর:
Abstract class → Related objects-এর shared code আছে।
                 Common base behaviour দরকার।
                 State (fields) দরকার।
                 "Employee is-a Person" — is-a relationship।
                 Example: Animal → Dog, Cat, Bird।

Interface → Unrelated objects-এ common capability।
            Multiple "can-do" behaviours দরকার।
            Contract define করতে।
            "CustomerService can-do IRepository operations।"
            Example: IDisposable, IComparable, IEnumerable।

Rule of thumb:
Abstract class → inheritance hierarchy, shared code
Interface → capability/contract, loose coupling

প্রশ্ন: C# Multiple inheritance নেই কেন? কীভাবে solve করা যায়?

উত্তর: Diamond problem এড়াতে। Multiple interface implement করে
multiple capabilities পাওয়া যায়।
```

---

<a id="p3-sealed-static"></a>
### Topic 11: Sealed Class ও Static Class

**Sealed Class:**

```csharp
// sealed — inherit করা যাবে না
public sealed class Configuration
{
    private static readonly Configuration _instance = new();

    // Singleton pattern — sealed class perfect fit
    public static Configuration Instance => _instance;

    private Configuration()
    {
        DatabaseUrl = Environment.GetEnvironmentVariable("DB_URL") ?? "localhost";
        AppName = "CS Interview Handbook";
    }

    public string DatabaseUrl { get; }
    public string AppName { get; }
    public bool IsProduction => DatabaseUrl.Contains("prod");
}

// Inheritance attempt:
// public class MyConfig : Configuration { } // ❌ Cannot inherit from sealed class

// sealed method — only in non-sealed class, stops further override
public class Animal
{
    public virtual void Breathe() => Console.WriteLine("Breathing...");
}

public class Mammal : Animal
{
    public sealed override void Breathe() =>
        Console.WriteLine("Lung breathing"); // sealed — cannot override further
}

public class Dog : Mammal
{
    // public override void Breathe() { } // ❌ Cannot override sealed method
}

// Use cases for sealed:
// 1. Singleton class
// 2. Immutable value objects
// 3. Security-sensitive classes (prevent extension attacks)
// 4. Performance — JIT can optimize sealed class calls
```

**Static Class:**

```csharp
// static class — instance তৈরি করা যায় না, সব members static
public static class MathHelper
{
    public static double Pi = Math.PI;

    public static bool IsPrime(int n)
    {
        if (n < 2) return false;
        for (int i = 2; i <= Math.Sqrt(n); i++)
            if (n % i == 0) return false;
        return true;
    }

    public static int Fibonacci(int n) =>
        n <= 1 ? n : Fibonacci(n - 1) + Fibonacci(n - 2);

    public static double Clamp(double value, double min, double max) =>
        Math.Max(min, Math.Min(max, value));
}

// Extension Methods — static class-এই থাকে
public static class StringExtensions
{
    public static bool IsNullOrEmpty(this string? value) =>
        string.IsNullOrEmpty(value);

    public static string ToPascalCase(this string value)
    {
        if (value.IsNullOrEmpty()) return value ?? "";
        return string.Join("", value.Split(' ')
            .Select(word => char.ToUpper(word[0]) + word[1..].ToLower()));
    }

    public static string Truncate(this string value, int maxLength, string suffix = "...")
    {
        if (value.Length <= maxLength) return value;
        return value[..(maxLength - suffix.Length)] + suffix;
    }
}

// Extension method usage — instance method-এর মতো call হয়
string title = "hello world from bangladesh";
Console.WriteLine(title.ToPascalCase());    // "Hello World From Bangladesh"
Console.WriteLine(title.Truncate(15));      // "hello world fro..."

// Static class — no instance, class name দিয়ে call
Console.WriteLine(MathHelper.IsPrime(17));  // true
Console.WriteLine(MathHelper.Fibonacci(10)); // 55
```

---

<a id="p3-access-modifiers"></a>
### Topic 12: Access Modifiers

```
───────────────────────────────────────────────────────────────────
Modifier          Same Class  Same Assembly  Subclass  Anywhere
───────────────────────────────────────────────────────────────────
public               ✅            ✅           ✅        ✅
private              ✅            ❌           ❌        ❌
protected            ✅            ❌           ✅        ❌
internal             ✅            ✅           ❌        ❌
protected internal   ✅            ✅           ✅        ❌
private protected    ✅            ❌           ✅*       ❌
───────────────────────────────────────────────────────────────────
* same assembly-এর subclass শুধু
```

```csharp
public class AccessDemo
{
    public string PublicField = "Everyone can see";
    private string _privateField = "Only this class";
    protected string ProtectedField = "This class + subclasses";
    internal string InternalField = "This assembly only";
    protected internal string ProtectedInternal = "Assembly or subclasses";
    private protected string PrivateProtected = "Same assembly subclasses";

    // ── Common patterns ───────────────────────────────
    // private field + public property
    private decimal _balance;
    public decimal Balance
    {
        get => _balance;
        private set => _balance = value >= 0 ? value : 0;
    }

    // private set — outside read, only this class writes
    public DateTime LastUpdated { get; private set; } = DateTime.Now;

    // internal — only within same project/assembly
    internal void InternalHelper() { }

    // protected — subclass can call, outside cannot
    protected virtual void OnBalanceChanged(decimal oldBalance) { }
}

// Practical usage guide:
// Fields      → private (always)
// Properties  → public get, private set (usually)
// Constructor → public (usually)
// Helper methods → private
// Methods for subclasses → protected
// API methods → public
// Cross-project utilities → internal
```

---

<a id="p3-solid"></a>
### Topic 13: SOLID Principles

> **SOLID** — Object-Oriented Design-এর ৫টি মূলনীতি যা maintainable, scalable code লেখতে সাহায্য করে।

---

**S — Single Responsibility Principle (SRP):**

> একটি class-এর একটিমাত্র কারণে পরিবর্তন হওয়া উচিত।

```csharp
// ❌ BAD — একটি class অনেক responsibility নিয়েছে
public class OrderManager
{
    public void CreateOrder(Order order) { /* DB save */ }
    public void SendEmail(Order order) { /* SMTP call */ }
    public void GenerateInvoice(Order order) { /* PDF create */ }
    public void UpdateInventory(Order order) { /* stock update */ }
    // এই class কে পরিবর্তন করতে হয় যখন:
    // DB structure বদলায়, email template বদলায়, invoice format বদলায়...
}

// ✅ GOOD — প্রতিটি class এক কাজ করে
public class OrderService
{
    private readonly IOrderRepository _repo;
    public OrderService(IOrderRepository repo) => _repo = repo;
    public async Task<Order> CreateAsync(CreateOrderDto dto) =>
        await _repo.AddAsync(dto.ToOrder());
}

public class OrderEmailService
{
    private readonly IEmailSender _email;
    public OrderEmailService(IEmailSender email) => _email = email;
    public async Task SendConfirmationAsync(Order order) =>
        await _email.SendAsync(order.CustomerEmail, "Order Confirmed", BuildBody(order));
    private string BuildBody(Order order) => $"Your order #{order.Id} is confirmed.";
}

public class InvoiceService
{
    public byte[] GeneratePdf(Order order) { /* PDF logic */ return Array.Empty<byte>(); }
}
```

---

**O — Open/Closed Principle (OCP):**

> Software entities **extension-এ open**, **modification-এ closed** হওয়া উচিত।

```csharp
// ❌ BAD — নতুন discount type যোগ করতে এই method পরিবর্তন করতে হয়
public decimal CalculateDiscount(Customer customer, decimal price)
{
    if (customer.Type == "Premium") return price * 0.20m;
    if (customer.Type == "Gold") return price * 0.15m;
    if (customer.Type == "Silver") return price * 0.10m;
    // নতুন "Diamond" type যোগ করতে এই if-chain বাড়াতে হবে!
    return 0;
}

// ✅ GOOD — interface দিয়ে extension, modification ছাড়া
public interface IDiscountStrategy
{
    decimal Calculate(decimal price);
}

public class PremiumDiscount : IDiscountStrategy
{
    public decimal Calculate(decimal price) => price * 0.20m;
}

public class GoldDiscount : IDiscountStrategy
{
    public decimal Calculate(decimal price) => price * 0.15m;
}

public class SilverDiscount : IDiscountStrategy
{
    public decimal Calculate(decimal price) => price * 0.10m;
}

// নতুন type যোগ করতে শুধু নতুন class তৈরি করুন
public class DiamondDiscount : IDiscountStrategy
{
    public decimal Calculate(decimal price) => price * 0.25m;
}

// OrderService এ কোনো পরিবর্তন দরকার নেই!
public class PricingService
{
    public decimal GetFinalPrice(decimal price, IDiscountStrategy strategy) =>
        price - strategy.Calculate(price);
}
```

---

**L — Liskov Substitution Principle (LSP):**

> Subclass যেকোনো জায়গায় parent class-এর জায়গায় ব্যবহার করা যাবে।

```csharp
// ❌ BAD — LSP violation
public class Rectangle
{
    public virtual int Width { get; set; }
    public virtual int Height { get; set; }
    public int Area() => Width * Height;
}

public class Square : Rectangle
{
    // Square-এ Width = Height, তাই override করতে হয়
    public override int Width
    {
        get => base.Width;
        set { base.Width = value; base.Height = value; } // ← এটাই সমস্যা!
    }
    public override int Height
    {
        get => base.Height;
        set { base.Width = value; base.Height = value; }
    }
}

// LSP violation — Rectangle দিয়ে কাজ করা code Square-এ ভেঙে যায়
void ResizeRectangle(Rectangle r)
{
    r.Width = 5;
    r.Height = 10;
    Console.WriteLine(r.Area()); // Rectangle → 50, Square → 100! ❌
}

// ✅ GOOD — separate hierarchy
public abstract class Shape2D
{
    public abstract int Area();
}

public class Rectangle2D : Shape2D
{
    public int Width { get; init; }
    public int Height { get; init; }
    public override int Area() => Width * Height;
}

public class Square2D : Shape2D
{
    public int Side { get; init; }
    public override int Area() => Side * Side;
}
```

---

**I — Interface Segregation Principle (ISP):**

> Clients-কে তাদের প্রয়োজন নেই এমন methods implement করতে বাধ্য করা উচিত নয়।

```csharp
// ❌ BAD — fat interface
public interface IWorker
{
    void Work();
    void Eat();
    void Sleep();
    void GetPaid();
}
// Robot-কে Eat() ও Sleep() implement করতে হয় — অর্থহীন!

// ✅ GOOD — segregated interfaces
public interface IWorkable { void Work(); }
public interface IEatable  { void Eat(); void Sleep(); }
public interface IPayable  { void GetPaid(); }

public class HumanWorker : IWorkable, IEatable, IPayable
{
    public void Work()    => Console.WriteLine("Human working");
    public void Eat()     => Console.WriteLine("Human eating");
    public void Sleep()   => Console.WriteLine("Human sleeping");
    public void GetPaid() => Console.WriteLine("Human paid");
}

public class Robot : IWorkable  // শুধু যা relevant
{
    public void Work() => Console.WriteLine("Robot working 24/7");
}

// Real-world example — repository interfaces
public interface IReadRepository<T>
{
    Task<T?> GetByIdAsync(int id);
    Task<IEnumerable<T>> GetAllAsync();
}

public interface IWriteRepository<T>
{
    Task<T> AddAsync(T entity);
    Task UpdateAsync(T entity);
    Task DeleteAsync(int id);
}

// Read-only service শুধু IReadRepository নেয়
public class ReportService
{
    private readonly IReadRepository<Order> _repo;
    public ReportService(IReadRepository<Order> repo) => _repo = repo;
}

// CQRS command handler শুধু IWriteRepository নেয়
public class CreateOrderHandler
{
    private readonly IWriteRepository<Order> _repo;
    public CreateOrderHandler(IWriteRepository<Order> repo) => _repo = repo;
}
```

---

**D — Dependency Inversion Principle (DIP):**

> High-level modules low-level modules-এর উপর depend করবে না। উভয়ই abstraction-এর উপর depend করবে।

```csharp
// ❌ BAD — high-level class directly creates low-level dependency
public class OrderService_Bad
{
    // Concrete class directly — tightly coupled!
    private readonly SqlOrderRepository _repo = new SqlOrderRepository();
    private readonly SmtpEmailService _email = new SmtpEmailService();

    public void PlaceOrder(Order order)
    {
        _repo.Save(order);           // SQL-specific
        _email.Send(order.Email);    // SMTP-specific
    }
    // Test করা impossible — real DB ও SMTP ছাড়া
    // SQL থেকে MongoDB migrate → এই class পরিবর্তন করতে হবে
}

// ✅ GOOD — depend on abstractions
public class OrderService_Good
{
    private readonly IOrderRepository _repo;   // interface
    private readonly IEmailService _email;      // interface

    // Constructor injection — DI container automatically inject করবে
    public OrderService_Good(IOrderRepository repo, IEmailService email)
    {
        _repo = repo;
        _email = email;
    }

    public async Task PlaceOrderAsync(Order order)
    {
        await _repo.SaveAsync(order);
        await _email.SendAsync(order.CustomerEmail,
            "Order Confirmed", $"Order #{order.Id} placed!");
    }
}

// Test-এ mock inject করা যায়
// Production-এ real implementation inject হয়
// MongoDB migrate করতে শুধু MongoOrderRepository তৈরি করুন

// ASP.NET Core DI registration:
// builder.Services.AddScoped<IOrderRepository, SqlOrderRepository>();
// builder.Services.AddScoped<IEmailService, SmtpEmailService>();
// builder.Services.AddScoped<OrderService_Good>();
```

---

<a id="p3-di"></a>
### Topic 14: Dependency Injection Basics

**সহজ ভাষায়:**

> **DI** মানে class নিজে dependency তৈরি না করে **বাইরে থেকে পেয়ে যাওয়া**। Constructor-এ চাইলেই পাওয়া যায়।

**Analogy:** Restaurant customer নিজে রান্না করে না — waiter food দিয়ে যায়। আপনি শুধু order করুন।

```csharp
// ── Service interfaces ────────────────────────────────
public interface IProductRepository
{
    Task<Product?> GetByIdAsync(int id);
    Task<IEnumerable<Product>> GetAllAsync();
    Task<Product> CreateAsync(Product product);
}

public interface IEmailService
{
    Task SendAsync(string to, string subject, string body);
}

public interface ICacheService
{
    Task<T?> GetAsync<T>(string key);
    Task SetAsync<T>(string key, T value, TimeSpan expiry);
    Task RemoveAsync(string key);
}

// ── Service with multiple dependencies ───────────────
public class ProductService
{
    private readonly IProductRepository _repository;
    private readonly ICacheService _cache;
    private readonly ILogger<ProductService> _logger;

    // Constructor injection — সব dependencies inject হয়
    public ProductService(
        IProductRepository repository,
        ICacheService cache,
        ILogger<ProductService> logger)
    {
        _repository = repository;
        _cache = cache;
        _logger = logger;
    }

    public async Task<Product?> GetProductAsync(int id)
    {
        // Try cache first
        var cacheKey = $"product:{id}";
        var cached = await _cache.GetAsync<Product>(cacheKey);
        if (cached is not null)
        {
            _logger.LogInformation("Cache hit for product {Id}", id);
            return cached;
        }

        // Fetch from DB
        var product = await _repository.GetByIdAsync(id);
        if (product is not null)
        {
            await _cache.SetAsync(cacheKey, product, TimeSpan.FromMinutes(10));
            _logger.LogInformation("Product {Id} cached", id);
        }
        return product;
    }

    public async Task<Product> CreateProductAsync(CreateProductDto dto)
    {
        var product = new Product
        {
            Name = dto.Name,
            Price = dto.Price,
            Category = dto.Category
        };
        return await _repository.CreateAsync(product);
    }
}
```

**ASP.NET Core DI Registration:**

```csharp
// Program.cs — service registration
var builder = WebApplication.CreateBuilder(args);

// ── Lifetime types ────────────────────────────────────

// Transient — প্রতিটি request-এ নতুন instance
// Lightweight, stateless services-এর জন্য
builder.Services.AddTransient<IEmailService, SmtpEmailService>();

// Scoped — প্রতিটি HTTP request-এ একটি instance
// Web request-এ সব জায়গায় same instance
// Database context, Unit of Work
builder.Services.AddScoped<IProductRepository, EfProductRepository>();
builder.Services.AddScoped<ProductService>();
builder.Services.AddDbContext<AppDbContext>(options =>
    options.UseSqlServer(builder.Configuration.GetConnectionString("Default")));

// Singleton — Application জীবনকাল একটি instance
// Config, cache, expensive objects
builder.Services.AddSingleton<ICacheService, RedisCacheService>();
builder.Services.AddSingleton<IConfiguration>(builder.Configuration);

var app = builder.Build();
```

**DI in Controller:**

```csharp
[ApiController]
[Route("api/[controller]")]
public class ProductsController : ControllerBase
{
    private readonly ProductService _productService;

    // ASP.NET Core automatically inject করে
    public ProductsController(ProductService productService)
    {
        _productService = productService;
    }

    [HttpGet("{id}")]
    public async Task<ActionResult<Product>> GetProduct(int id)
    {
        var product = await _productService.GetProductAsync(id);
        return product is null ? NotFound() : Ok(product);
    }

    [HttpPost]
    public async Task<ActionResult<Product>> CreateProduct(CreateProductDto dto)
    {
        var product = await _productService.CreateProductAsync(dto);
        return CreatedAtAction(nameof(GetProduct), new { id = product.Id }, product);
    }
}
```

**Service Lifetime — কখন কোনটা:**

```
Transient  → প্রতিবার নতুন instance চাই।
             Stateless operations, email sender, validators।
             ⚠ Singleton-এ inject করলে Captive Dependency!

Scoped     → HTTP request-এর মধ্যে state share করতে চাই।
             DbContext (default scoped), Unit of Work, basket।
             ⚠ Singleton-এ inject করবেন না।

Singleton  → Application-wide single instance।
             Config, connection pool, cache, expensive resources।
             Thread-safe হতে হবে।
```

**Testing with DI (Mock):**

```csharp
// xUnit + Moq
public class ProductServiceTests
{
    private readonly Mock<IProductRepository> _repoMock = new();
    private readonly Mock<ICacheService> _cacheMock = new();
    private readonly Mock<ILogger<ProductService>> _loggerMock = new();
    private readonly ProductService _sut;

    public ProductServiceTests()
    {
        _sut = new ProductService(_repoMock.Object, _cacheMock.Object, _loggerMock.Object);
    }

    [Fact]
    public async Task GetProductAsync_WhenCached_ReturnsCachedProduct()
    {
        // Arrange
        var expected = new Product { Id = 1, Name = "Laptop", Price = 75000m };
        _cacheMock.Setup(c => c.GetAsync<Product>("product:1"))
                  .ReturnsAsync(expected);

        // Act
        var result = await _sut.GetProductAsync(1);

        // Assert
        Assert.Equal(expected, result);
        _repoMock.Verify(r => r.GetByIdAsync(It.IsAny<int>()), Times.Never);
    }
}
```

---

## PART 3 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| Class | Blueprint — state + behaviour |
| Object | Class-এর instance — real entity |
| Struct | Value type, stack, copy semantics |
| Record | Immutable value object, value equality |
| Encapsulation | Data hiding — private fields, public properties |
| Abstraction | Complexity hiding — relevant interface expose |
| Inheritance | Parent → Child, code reuse, is-a relationship |
| Polymorphism | Same interface, different behaviour |
| Overloading | Same name, different params — compile-time |
| Overriding | virtual + override — runtime dispatch |
| `new` keyword | Method hiding — NOT polymorphic |
| Abstract Class | Incomplete blueprint, shared code, no instantiation |
| Interface | Pure contract, multiple implementation |
| Sealed | No inheritance allowed |
| Static Class | No instance, utility methods, extension methods |
| `public` | Everywhere accessible |
| `private` | This class only |
| `protected` | This class + subclasses |
| `internal` | Same assembly only |
| SRP | One class, one reason to change |
| OCP | Open for extension, closed for modification |
| LSP | Subclass substitutable for parent |
| ISP | Small focused interfaces, not fat ones |
| DIP | Depend on abstraction, not concrete |
| DI | Dependencies injected from outside |
| Transient | New instance every time |
| Scoped | New instance per HTTP request |
| Singleton | One instance for app lifetime |

---

## PART 3 Interview Q&A

```
প্রশ্ন: OOP-এর ৪টি pillar কী?
উত্তর: Encapsulation, Abstraction, Inheritance, Polymorphism।

প্রশ্ন: Abstract class আর Interface-এর পার্থক্য?
উত্তর: Abstract class → shared code, fields, single inheritance।
       Interface → contract, multiple implementation, no state।
       C# 8+ interface-এ default methods আছে।

প্রশ্ন: SOLID কী?
উত্তর: S-Single Responsibility, O-Open/Closed, L-Liskov Substitution,
       I-Interface Segregation, D-Dependency Inversion।
       Maintainable, testable, extensible code-এর design principles।

প্রশ্ন: Dependency Injection কেন ব্যবহার করা হয়?
উত্তর: Loose coupling। Unit testing সহজ (mock inject করা যায়)।
       SOLID-এর Dependency Inversion principle follow করে।
       ASP.NET Core built-in DI container আছে।

প্রশ্ন: Sealed class কেন ব্যবহার করা হয়?
উত্তর: Unintended inheritance prevent করে।
       JIT optimization সুবিধা।
       Security-sensitive class-এ extension prevent।

প্রশ্ন: override আর new-এর পার্থক্য?
উত্তর: override → polymorphic। Base reference থেকে derived method call হয়।
       new → hiding। Base reference থেকে base method call হয়।
       সবসময় override ব্যবহার করুন।

প্রশ্ন: Constructor chaining কী?
উত্তর: this() দিয়ে একই class-এর অন্য constructor call।
       base() দিয়ে parent class constructor call।
       Code duplication কমায়।

প্রশ্ন: Static constructor কখন call হয়?
উত্তর: Class প্রথমবার use হওয়ার আগে, একবারই।
       Static fields/properties initialize করার জন্য।
       Thread-safe by CLR guarantee।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 4 — Advanced C# (Delegates, Events, Lambda, LINQ, Generics, Async/Await, Threading, TPL, Memory Management, IDisposable, Boxing/Unboxing এবং আরও...)

---

<a id="part4"></a>
## PART 4: Advanced C#

> Delegates, Events, Lambda, LINQ, Generics, Async/Await, Threading & TPL, Memory Management, IDisposable, Boxing/Unboxing।

| # | বিষয় |
|---|-------|
| 1 | [Delegates](#p4-delegates) |
| 2 | [Events](#p4-events) |
| 3 | [Lambda Expressions](#p4-lambda) |
| 4 | [LINQ](#p4-linq) |
| 5 | [Generics](#p4-generics) |
| 6 | [Async/Await](#p4-async) |
| 7 | [Threading ও TPL](#p4-threading) |
| 8 | [Memory Management ও GC](#p4-memory) |
| 9 | [IDisposable ও using](#p4-idisposable) |
| 10 | [Boxing ও Unboxing](#p4-boxing) |
| 11 | [Pattern Matching (C# 7–12)](#p4-patterns) |

---

<a id="p4-delegates"></a>
### Topic 1: Delegates

**সহজ ভাষায়:**

> **Delegate** হলো method-এর reference — যেমন function pointer, কিন্তু type-safe। একটি variable-এ method store করা যায় এবং পরে call করা যায়।

**Analogy:** Delivery app-এ "on delivery complete, do this action" — আপনি বলছেন কী করতে হবে, app পরে execute করবে।

```csharp
// ── Delegate type declaration ─────────────────────────
public delegate int MathOperation(int a, int b);
public delegate void Notification(string message);
public delegate bool Validator<T>(T value);

// ── Method references ──────────────────────────────────
public class Calculator
{
    public static int Add(int a, int b) => a + b;
    public static int Subtract(int a, int b) => a - b;
    public static int Multiply(int a, int b) => a * b;
}

// Delegate usage
MathOperation op = Calculator.Add;
Console.WriteLine(op(10, 5));  // 15

op = Calculator.Subtract;
Console.WriteLine(op(10, 5));  // 5

op = Calculator.Multiply;
Console.WriteLine(op(10, 5));  // 50

// ── Multicast Delegate — multiple methods ─────────────
Notification notify = msg => Console.WriteLine($"[Email] {msg}");
notify += msg => Console.WriteLine($"[SMS] {msg}");
notify += msg => Console.WriteLine($"[Push] {msg}");

notify("Order shipped!");
// [Email] Order shipped!
// [SMS] Order shipped!
// [Push] Order shipped!

// ── Built-in Delegate types (no custom needed) ─────────
// Action — return type void
Action<string> log = msg => Console.WriteLine(msg);
Action<int, int> printSum = (a, b) => Console.WriteLine(a + b);
Action printHello = () => Console.WriteLine("Hello");

// Func — last type param is return type
Func<int, int, int> add = (a, b) => a + b;
Func<string, bool> isEmpty = s => string.IsNullOrEmpty(s);
Func<int, string> toStr = n => n.ToString();

// Predicate — returns bool
Predicate<int> isEven = n => n % 2 == 0;
Predicate<string> isLong = s => s.Length > 10;

Console.WriteLine(add(3, 4));       // 7
Console.WriteLine(isEven(6));       // true
Console.WriteLine(isLong("Hello")); // false

// ── Higher-order functions ────────────────────────────
public static List<T> Filter<T>(List<T> list, Predicate<T> condition)
{
    var result = new List<T>();
    foreach (var item in list)
        if (condition(item)) result.Add(item);
    return result;
}

var numbers = new List<int> { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
var evens = Filter(numbers, n => n % 2 == 0); // [2, 4, 6, 8, 10]
```

---

<a id="p4-events"></a>
### Topic 2: Events

**সহজ ভাষায়:**

> **Event** হলো delegate-এর উপর নির্মিত publisher-subscriber pattern। Object বলে "কিছু ঘটেছে", interested parties নিজেরা সাড়া দেয়।

```csharp
// ── Event declaration ─────────────────────────────────
public class OrderProcessor
{
    // EventHandler<T> — .NET standard event pattern
    public event EventHandler<OrderEventArgs>? OrderPlaced;
    public event EventHandler<OrderEventArgs>? OrderShipped;
    public event EventHandler? OrderCancelled;

    public async Task PlaceOrderAsync(Order order)
    {
        // Process order...
        await Task.Delay(100); // simulate work

        // Raise event — notify all subscribers
        OnOrderPlaced(new OrderEventArgs(order));
    }

    // Protected virtual — subclass can override notification logic
    protected virtual void OnOrderPlaced(OrderEventArgs e) =>
        OrderPlaced?.Invoke(this, e);  // ?. — safe if no subscribers

    protected virtual void OnOrderShipped(OrderEventArgs e) =>
        OrderShipped?.Invoke(this, e);

    protected virtual void OnOrderCancelled(EventArgs e) =>
        OrderCancelled?.Invoke(this, e);
}

// Event args — event data carry করে
public class OrderEventArgs : EventArgs
{
    public Order Order { get; }
    public DateTime Timestamp { get; }

    public OrderEventArgs(Order order)
    {
        Order = order;
        Timestamp = DateTime.UtcNow;
    }
}

// ── Subscribers ────────────────────────────────────────
public class EmailNotifier
{
    private readonly IEmailService _email;
    public EmailNotifier(IEmailService email) => _email = email;

    public void Subscribe(OrderProcessor processor)
    {
        processor.OrderPlaced += OnOrderPlaced;
        processor.OrderShipped += OnOrderShipped;
    }

    public void Unsubscribe(OrderProcessor processor)
    {
        processor.OrderPlaced -= OnOrderPlaced;  // always unsubscribe!
        processor.OrderShipped -= OnOrderShipped;
    }

    private async void OnOrderPlaced(object? sender, OrderEventArgs e)
    {
        await _email.SendAsync(
            e.Order.CustomerEmail,
            "Order Confirmed",
            $"Your order #{e.Order.Id} has been placed!");
    }

    private async void OnOrderShipped(object? sender, OrderEventArgs e) =>
        await _email.SendAsync(e.Order.CustomerEmail, "Shipped!", "Your order is on the way.");
}

// ── Usage ──────────────────────────────────────────────
var processor = new OrderProcessor();
var emailNotifier = new EmailNotifier(emailService);
emailNotifier.Subscribe(processor);
await processor.PlaceOrderAsync(order);
// EmailNotifier automatically notified
```

**🎤 Interview Q&A:**

```
প্রশ্ন: Delegate আর Event-এর পার্থক্য?

উত্তর:
Delegate → method reference। যেকেউ invoke করতে পারে।
Event → delegate wrapper। শুধু declaring class invoke করতে পারে।
        Subscribers শুধু += / -= করতে পারে।

Event → encapsulation। অন্য class accidentally invoke করতে পারে না।

প্রশ্ন: Memory leak কীভাবে হয় events-এ?

উত্তর: Unsubscribe না করলে! Publisher subscriber-এর reference রাখে,
GC collect করতে পারে না। সবসময় -= দিয়ে unsubscribe করুন,
বা IDisposable implement করুন।
```

---

<a id="p4-lambda"></a>
### Topic 3: Lambda Expressions

**সহজ ভাষায়:**

> **Lambda** হলো anonymous (নামহীন) function — inline method। `=>` arrow operator দিয়ে লেখা হয়।

```csharp
// ── Lambda syntax ──────────────────────────────────────
Func<int, int> square = x => x * x;
Func<int, int, int> add = (a, b) => a + b;
Action<string> print = msg => Console.WriteLine(msg);
Func<int, bool> isEven = n => n % 2 == 0;

// Multi-line lambda
Func<List<int>, double> average = numbers =>
{
    if (numbers.Count == 0) return 0;
    return numbers.Sum() / (double)numbers.Count;
};

// ── Closure — outer variable capture ─────────────────
int multiplier = 3;
Func<int, int> triple = x => x * multiplier;  // captures multiplier
Console.WriteLine(triple(5));  // 15

multiplier = 10;
Console.WriteLine(triple(5));  // 50! closure captures reference, not value!

// ── Lambda with LINQ ──────────────────────────────────
var orders = new List<Order> { /* ... */ };

var pending = orders.Where(o => o.Status == "Pending");
var amounts = orders.Select(o => o.Amount);
var sorted  = orders.OrderByDescending(o => o.Amount);
decimal total = orders.Sum(o => o.Amount);
bool hasLarge = orders.Any(o => o.Amount > 10000m);

// ── Expression trees vs Func ──────────────────────────
// Func<> → compiled delegate — runs in memory
Func<Order, bool> funcFilter = o => o.Amount > 10000;

// Expression<Func<>> → data structure — EF Core translates to SQL!
Expression<Func<Order, bool>> exprFilter = o => o.Amount > 10000;
// EF Core: WHERE Amount > 10000

// ── Static lambdas (C# 9+) ───────────────────────────
Func<int, int> fastSquare = static x => x * x; // cannot capture outer vars, faster
```

---

<a id="p4-linq"></a>
### Topic 4: LINQ

**সহজ ভাষায়:**

> **LINQ** (Language Integrated Query) — C# code-এ সরাসরি query লেখার সুবিধা। Collections, databases, XML — সব জায়গায় একই syntax।

```csharp
var students = new List<Student>
{
    new Student { Id=1, Name="Rahim",  Score=85, Dept="CSE" },
    new Student { Id=2, Name="Karim",  Score=92, Dept="EEE" },
    new Student { Id=3, Name="Jamal",  Score=67, Dept="CSE" },
    new Student { Id=4, Name="Nadia",  Score=78, Dept="CSE" },
    new Student { Id=5, Name="Sadia",  Score=95, Dept="BBA" },
    new Student { Id=6, Name="Rashed", Score=55, Dept="EEE" },
};

// ── Method syntax (Lambda) — সবচেয়ে বেশি ব্যবহৃত ─────
var cseStudents = students
    .Where(s => s.Dept == "CSE")
    .OrderByDescending(s => s.Score)
    .Select(s => new { s.Name, s.Score })
    .ToList();

// ── Query syntax (SQL-like) ────────────────────────────
var query = from s in students
            where s.Dept == "CSE"
            orderby s.Score descending
            select new { s.Name, s.Score };

// ── Filtering ─────────────────────────────────────────
var passed         = students.Where(s => s.Score >= 60);
var first          = students.First(s => s.Dept == "BBA");       // throws if not found
var firstOrNull    = students.FirstOrDefault(s => s.Score > 99); // null if not found
var single         = students.Single(s => s.Id == 1);            // throws if 0 or >1

// ── Projection ────────────────────────────────────────
var names     = students.Select(s => s.Name);
var nameGrade = students.Select(s => new { s.Name, Grade = s.Score >= 80 ? "A" : "B" });

// SelectMany — flatten nested collections
var allCourses = students.SelectMany(s => s.Courses); // List<List<Course>> → List<Course>

// ── Aggregation ───────────────────────────────────────
int count      = students.Count();
int passCount  = students.Count(s => s.Score >= 60);
double avg     = students.Average(s => s.Score);
int maxScore   = students.Max(s => s.Score);
int minScore   = students.Min(s => s.Score);
int totalScore = students.Sum(s => s.Score);

// ── Grouping ──────────────────────────────────────────
var byDept = students.GroupBy(s => s.Dept);
foreach (var group in byDept)
    Console.WriteLine($"{group.Key}: {group.Count()} students, Avg: {group.Average(s => s.Score):F1}");
// CSE: 3 students, Avg: 76.7
// EEE: 2 students, Avg: 73.5

// ── Joining ────────────────────────────────────────────
var departments = new List<Department>
{
    new Department { Code = "CSE", Name = "Computer Science" },
    new Department { Code = "EEE", Name = "Electrical Engineering" },
};

var studentDept = students.Join(
    departments,
    s => s.Dept,
    d => d.Code,
    (s, d) => new { s.Name, DeptName = d.Name, s.Score }
);

// ── Sorting ────────────────────────────────────────────
var sorted = students
    .OrderBy(s => s.Dept)
    .ThenByDescending(s => s.Score);

// ── Set operations ─────────────────────────────────────
var depts1 = new[] { "CSE", "EEE" };
var depts2 = new[] { "EEE", "BBA" };
var union     = depts1.Union(depts2);      // [CSE, EEE, BBA]
var intersect = depts1.Intersect(depts2);  // [EEE]
var except    = depts1.Except(depts2);     // [CSE]

// ── Pagination ────────────────────────────────────────
int page = 2, pageSize = 10;
var paged = students.Skip((page - 1) * pageSize).Take(pageSize);

// ── Deferred vs Immediate Execution ───────────────────
// Deferred — query object তৈরি হয়, execute হয় না
var query2 = students.Where(s => s.Score > 70); // not executed yet!

// Immediate — এখনই execute হয়
var list  = query2.ToList();   // executes
var arr   = query2.ToArray();  // executes
int cnt   = query2.Count();    // executes
bool any  = query2.Any();      // executes

// ── Complex aggregation ───────────────────────────────
var report = students
    .Where(s => s.Score >= 60)
    .GroupBy(s => s.Dept)
    .Select(g => new
    {
        Department  = g.Key,
        StudentCount = g.Count(),
        AverageScore = Math.Round(g.Average(s => s.Score), 1),
        TopStudent   = g.OrderByDescending(s => s.Score).First().Name
    })
    .OrderByDescending(r => r.AverageScore)
    .ToList();
```

**🎤 Interview Trap:**

```
প্রশ্ন: IEnumerable<T> আর IQueryable<T> পার্থক্য?

উত্তর:
IEnumerable<T> → In-memory LINQ। সব data load করে তারপর filter।
                 LINQ to Objects। Lambda → compiled code।

IQueryable<T> → EF Core, Dapper। Database-এ SQL generate করে।
                Lambda → Expression tree → SQL।
                WHERE clause database-এই execute হয়।

// ❌ Performance — সব orders load করে memory-তে filter
IEnumerable<Order> orders = dbContext.Orders; // সব loaded!
var big = orders.Where(o => o.Amount > 10000); // in-memory

// ✅ Database-এ SQL execute হয়
IQueryable<Order> orders = dbContext.Orders; // not loaded yet
var big = orders.Where(o => o.Amount > 10000); // SQL: WHERE Amount > 10000
var result = big.ToList(); // NOW executes query
```

---

<a id="p4-generics"></a>
### Topic 5: Generics

**সহজ ভাষায়:**

> **Generics** — type-safe code যা যেকোনো type-এর সাথে কাজ করে। Boxing overhead নেই, runtime error নেই।

```csharp
// ── Generic class ─────────────────────────────────────
public class Repository<T> where T : class, IEntity, new()
{
    private readonly List<T> _store = new();

    public void Add(T item)        => _store.Add(item);
    public T? GetById(int id)      => _store.FirstOrDefault(x => x.Id == id);
    public IEnumerable<T> GetAll() => _store.AsReadOnly();
    public int Count               => _store.Count;
}

// ── Generic method ────────────────────────────────────
public static void Swap<T>(ref T a, ref T b)
{
    T temp = a; a = b; b = temp;
}

int x = 5, y = 10;
Swap(ref x, ref y);  // x=10, y=5

// ── Generic constraints ───────────────────────────────
// where T : class           — reference type
// where T : struct          — value type
// where T : new()           — has parameterless constructor
// where T : BaseClass       — inherits from BaseClass
// where T : IInterface      — implements interface
// where T : notnull         — non-nullable (C# 8+)
// where T : unmanaged       — unmanaged type (int, struct with no refs)

public T CreateInstance<T>() where T : class, new() => new T();

// ── Generic Result type — error handling without exceptions ──
public class Result<T>
{
    public bool IsSuccess  { get; }
    public T?   Value      { get; }
    public string? Error   { get; }

    private Result(bool isSuccess, T? value, string? error)
    {
        IsSuccess = isSuccess;
        Value = value;
        Error = error;
    }

    public static Result<T> Success(T value)    => new(true, value, null);
    public static Result<T> Failure(string err) => new(false, default, err);

    public Result<TNew> Map<TNew>(Func<T, TNew> mapper) =>
        IsSuccess && Value is not null
            ? Result<TNew>.Success(mapper(Value))
            : Result<TNew>.Failure(Error!);
}

// Usage:
Result<Customer> result = await customerService.GetCustomerAsync(id);
if (result.IsSuccess)
    Console.WriteLine(result.Value!.Name);
else
    Console.WriteLine($"Error: {result.Error}");

// ── Covariance (out) and Contravariance (in) ──────────
IEnumerable<string> strings = new List<string>();
IEnumerable<object> objects = strings; // ✅ covariant — string is-a object

// IList<string> list = new List<string>();
// IList<object> objList = list; // ❌ invariant — compile error
```

---

<a id="p4-async"></a>
### Topic 6: Async/Await

**সহজ ভাষায়:**

> **Async/Await** — non-blocking operations। I/O wait করার সময় thread অন্য কাজ করতে পারে। Server throughput বাড়ে।

**Analogy:** Restaurant order করে চলে গেলেন (non-blocking) — খাবার তৈরি হলে call আসবে। না থেকে দাঁড়িয়ে wait করলেন না।

```csharp
// ── Basic async method ────────────────────────────────
public async Task<Customer> GetCustomerAsync(int id)
{
    // await — thread return করে, I/O complete হলে resume
    var customer = await _dbContext.Customers.FindAsync(id);
    if (customer is null)
        throw new KeyNotFoundException($"Customer {id} not found");
    return customer;
}

// ── async void — avoid! ───────────────────────────────
// Exception silently swallowed! Use Task instead.
public async void FireAndForget() // ❌ avoid
{
    await Task.Delay(1000);
    throw new Exception(); // nobody catches this!
}

// ── Sequential vs Parallel await ─────────────────────
// Sequential — one after another (slower)
public async Task<OrderSummary> GetSequentialAsync(int orderId)
{
    var order    = await _orderRepo.GetByIdAsync(orderId);
    var customer = await _customerRepo.GetByIdAsync(order.CustomerId);
    var items    = await _itemRepo.GetByOrderAsync(orderId);
    return new OrderSummary(order, customer, items);
}

// Parallel — all start at once (faster!)
public async Task<OrderSummary> GetParallelAsync(int orderId)
{
    var orderTask = _orderRepo.GetByIdAsync(orderId);
    var itemsTask = _itemRepo.GetByOrderAsync(orderId);
    await Task.WhenAll(orderTask, itemsTask);
    var customer = await _customerRepo.GetByIdAsync(orderTask.Result!.CustomerId);
    return new OrderSummary(orderTask.Result, customer, itemsTask.Result);
}

// ── Task combinators ──────────────────────────────────
// WhenAll — সব complete হওয়ার জন্য wait
var customers = await Task.WhenAll(ids.Select(id => _repo.GetByIdAsync(id)));

// WhenAny — যেকোনো একটি complete হলে return (race, timeout)
var firstDone = await Task.WhenAny(task1, task2, task3);

// ── CancellationToken — cooperative cancellation ──────
public async Task<IEnumerable<Product>> SearchAsync(
    string query,
    CancellationToken ct = default)
{
    return await _db.Products
        .Where(p => p.Name.Contains(query))
        .ToListAsync(ct);  // pass token down!
}

// ASP.NET Core controller — token auto-provided
[HttpGet("search")]
public async Task<ActionResult> Search([FromQuery] string q, CancellationToken ct)
{
    var results = await _service.SearchAsync(q, ct);
    return Ok(results);
}

// ── ConfigureAwait(false) — library code ─────────────
public async Task<string> GetDataAsync()
{
    // Library code-এ — deadlock prevention, slightly faster
    var data = await _httpClient.GetStringAsync(url).ConfigureAwait(false);
    return data;
}

// ── ValueTask — allocation-free for hot paths ─────────
public async ValueTask<int> GetCachedCountAsync()
{
    if (_cache.TryGetValue("count", out int cached))
        return cached;  // synchronous — no heap allocation!
    var count = await _db.Products.CountAsync();
    _cache["count"] = count;
    return count;
}

// ── Async streams (C# 8+) ─────────────────────────────
public async IAsyncEnumerable<Order> StreamOrdersAsync(
    [EnumeratorCancellation] CancellationToken ct = default)
{
    await foreach (var order in _db.Orders.AsAsyncEnumerable().WithCancellation(ct))
        yield return order;
}

// Consume:
await foreach (var order in StreamOrdersAsync(cancellationToken))
    Console.WriteLine(order.Id);
```

**🎤 Interview Q&A:**

```
প্রশ্ন: async void কেন dangerous?

উত্তর: Exception catch করা যায় না।
await করা যায় না — completion জানা যায় না।
Unit test করা কঠিন।
শুধু event handler-এ use করুন।

প্রশ্ন: Task আর ValueTask পার্থক্য?

উত্তর:
Task → Heap allocation। আলাদা Task object তৈরি হয়।
ValueTask → Stack-based। synchronous path-এ allocation নেই।
           Cache hit scenario-তে performance ভালো।
           Await শুধু একবার করুন।

প্রশ্ন: Deadlock কীভাবে হয়?

উত্তর:
.Result বা .Wait() দিয়ে async method block করলে।
async method synchronization context-এ return করতে চায়,
কিন্তু context blocked — deadlock!

Solution: সবসময় await। Library-এ ConfigureAwait(false)।
```

---

<a id="p4-threading"></a>
### Topic 7: Threading ও TPL

```csharp
using System.Threading;
using System.Threading.Tasks;
using System.Collections.Concurrent;

// ── Thread — low level (avoid in production) ─────────
var thread = new Thread(() =>
{
    Console.WriteLine($"Thread {Thread.CurrentThread.ManagedThreadId} running");
    Thread.Sleep(1000);
});
thread.IsBackground = true; // daemon thread
thread.Start();
thread.Join(); // wait for completion

// ── Task Parallel Library (TPL) — modern approach ─────

// Parallel.For — CPU-bound parallel work
Parallel.For(0, 1000, i => ProcessItem(i));

// Parallel.ForEach with max parallelism
Parallel.ForEach(orders,
    new ParallelOptions { MaxDegreeOfParallelism = 4 },
    order => ProcessOrder(order));

// ── PLINQ — parallel LINQ ─────────────────────────────
var results = bigList
    .AsParallel()
    .WithDegreeOfParallelism(4)
    .Where(x => IsExpensiveFilter(x))
    .Select(x => TransformItem(x))
    .ToList();

// ── Thread synchronization ────────────────────────────

// lock — mutual exclusion
private readonly object _lockObj = new();
private int _counter = 0;

public void Increment()
{
    lock (_lockObj)
    {
        _counter++;  // thread-safe
    }
}

// Interlocked — atomic operations (faster than lock for single ops)
private int _atomicCounter = 0;
public void AtomicIncrement() => Interlocked.Increment(ref _atomicCounter);

// SemaphoreSlim — limit concurrent access
private readonly SemaphoreSlim _semaphore = new(3); // max 3 concurrent

public async Task ProcessWithLimitAsync()
{
    await _semaphore.WaitAsync();
    try { await DoWorkAsync(); }
    finally { _semaphore.Release(); }
}

// ConcurrentDictionary — thread-safe dictionary
private readonly ConcurrentDictionary<string, int> _counts = new();

public void AddOrUpdate(string key) =>
    _counts.AddOrUpdate(key, 1, (k, v) => v + 1); // atomic!

// ── async vs parallel — key difference ───────────────
// async/await → I/O-bound। Thread wait না করে অন্য কাজ করে।
// Parallel/PLINQ → CPU-bound। Multiple cores-এ কাজ ভাগ করে।

// I/O bound (DB, HTTP, File) → async/await
public async Task<string> FetchDataAsync() =>
    await _httpClient.GetStringAsync(url);

// CPU bound (heavy computation) → Task.Run + Parallel
public async Task<int[]> ProcessLargeArrayAsync(int[] data) =>
    await Task.Run(() => data.AsParallel().Select(HeavyCompute).ToArray());
```

**🎤 Interview Q&A:**

```
প্রশ্ন: Thread আর Task-এর পার্থক্য?

উত্তর:
Thread → OS thread। Expensive (1MB stack)। Manual management।
Task → Abstraction over ThreadPool। Lightweight।
       async/await, cancellation, continuation support।
       Modern code-এ সবসময় Task ব্যবহার করুন।

প্রশ্ন: lock কখন ব্যবহার করবেন?

উত্তর: Shared mutable state-এ। Counter, List, Dictionary update।
Deadlock avoid করতে: সবসময় same order-এ lock করুন।
Fine-grained lock করুন — পুরো method lock করবেন না।
lock object → private readonly object।
```

---

<a id="p4-memory"></a>
### Topic 8: Memory Management ও GC

**সহজ ভাষায়:**

> .NET-এ **Garbage Collector (GC)** automatically memory manage করে। কিন্তু কীভাবে কাজ করে জানলে better code লেখা যায়।

```
Memory Layout:
─────────────────────────────────────────────────────
Stack                          Heap
─────────────────────────────────────────────────────
Value types (int, bool, struct) Reference types (class, array, string)
Method parameters              GC manages — automatic cleanup
Local variables                Large Object Heap (LOH): > 85KB
─────────────────────────────────────────────────────
Fast allocation/deallocation   GC marks & compacts
LIFO                           Gen 0 → Gen 1 → Gen 2
```

```csharp
// GC Generations:
// Gen 0 — new objects। সবচেয়ে বেশি collect হয়। Fast।
// Gen 1 — Gen 0 থেকে survive। Buffer।
// Gen 2 — Long-lived objects। Singleton, static।
// LOH   — 85KB+ objects। Rarely compacted।

// Memory info
long totalMemory = GC.GetTotalMemory(false);
Console.WriteLine($"Memory used: {totalMemory / 1024 / 1024} MB");

// ── Object pooling — GC pressure কমায় ───────────────
using System.Buffers;

byte[] buffer = ArrayPool<byte>.Shared.Rent(4096); // borrow
try
{
    int bytesRead = await stream.ReadAsync(buffer.AsMemory(0, buffer.Length));
}
finally
{
    ArrayPool<byte>.Shared.Return(buffer); // return to pool
}

// ── Span<T> — zero-copy stack slice ──────────────────
string text = "Hello, World!";

ReadOnlySpan<char> span = text.AsSpan(7, 6); // "World!" — no allocation!
Console.WriteLine(span.ToString());

// CSV parse without allocation
ReadOnlySpan<char> csv = "Dhaka,Chittagong,Sylhet".AsSpan();
int comma = csv.IndexOf(',');
ReadOnlySpan<char> first = csv[..comma]; // "Dhaka"

// Memory<T> — async context-এ use করা যায়
Memory<byte> buf = new byte[1024];
int read = await stream.ReadAsync(buf);

// ── String interning ──────────────────────────────────
string a = "hello";
string b = "hello";
Console.WriteLine(ReferenceEquals(a, b)); // true — literals are interned

string c = new string('h', 5); // not interned
Console.WriteLine(ReferenceEquals(a, c)); // false
```

---

<a id="p4-idisposable"></a>
### Topic 9: IDisposable ও using

**সহজ ভাষায়:**

> **IDisposable** — deterministic cleanup। GC কখন cleanup করবে জানা যায় না, কিন্তু `using` দিয়ে guaranteed cleanup।

```csharp
// ── Full IDisposable pattern ──────────────────────────
public class DatabaseConnection : IDisposable
{
    private SqlConnection? _connection;
    private bool _disposed = false;

    public DatabaseConnection(string connectionString)
    {
        _connection = new SqlConnection(connectionString);
        _connection.Open();
    }

    public void Dispose()
    {
        Dispose(true);
        GC.SuppressFinalize(this); // Don't run finalizer
    }

    protected virtual void Dispose(bool disposing)
    {
        if (_disposed) return;
        if (disposing)
        {
            _connection?.Close();
            _connection?.Dispose();
            _connection = null;
        }
        _disposed = true;
    }

    ~DatabaseConnection() => Dispose(false); // safety net finalizer
}

// ── using statement ───────────────────────────────────
using (var conn = new DatabaseConnection(connectionString))
{
    // use conn
} // Dispose() called automatically, even if exception!

// ── using declaration (C# 8+) — cleaner syntax ────────
using var conn2 = new DatabaseConnection(connectionString);
// Dispose called at end of enclosing scope

// ── IAsyncDisposable (C# 8+) ─────────────────────────
public class AsyncResource : IAsyncDisposable
{
    private readonly Stream _stream;
    public AsyncResource(string path) => _stream = File.OpenRead(path);

    public async ValueTask DisposeAsync()
    {
        await _stream.DisposeAsync();
        GC.SuppressFinalize(this);
    }
}

await using var resource = new AsyncResource("data.bin");

// ── Common disposable types — always use using ────────
using var file        = File.OpenRead("data.txt");
using var reader      = new StreamReader(file);
using var transaction = await dbContext.Database.BeginTransactionAsync();
using var scope       = serviceProvider.CreateScope();
```

**🎤 Interview Q&A:**

```
প্রশ্ন: using statement কীভাবে কাজ করে?

উত্তর: Compiler try-finally block-এ transform করে।
finally-তে Dispose() call হয় — exception হলেও।
IDisposable implement করা যেকোনো object-এ ব্যবহার করা যায়।

প্রশ্ন: Finalizer ও IDisposable পার্থক্য?

উত্তর:
IDisposable.Dispose() → Deterministic। আপনি যখন চান।
Finalizer (~ClassName) → Non-deterministic। GC যখন চায়।

Best practice: IDisposable implement করুন।
Unmanaged resource থাকলে finalizer add করুন safety net হিসেবে।
Dispose() call হলে GC.SuppressFinalize() দিয়ে finalizer skip করুন।
```

---

<a id="p4-boxing"></a>
### Topic 10: Boxing ও Unboxing

**সহজ ভাষায়:**

> **Boxing** — value type → reference type (heap allocation)।
> **Unboxing** — reference type → value type (heap থেকে copy)।
> **Performance cost** — avoid করুন।

```csharp
// ── Boxing ────────────────────────────────────────────
int value = 42;          // stack
object boxed = value;    // Boxing! heap allocation + copy

// ── Unboxing ──────────────────────────────────────────
int unboxed = (int)boxed; // Unboxing — cast + copy to stack
// double wrong = (double)boxed; // ❌ InvalidCastException!

// ── When boxing happens (implicit) ───────────────────
// 1. Value type in object variable
object n = 100;  // boxing

// 2. Non-generic collection (legacy code)
var list = new System.Collections.ArrayList();
list.Add(42);            // boxing!
int x = (int)list[0];   // unboxing!

// ✅ Generic collections — no boxing!
var genericList = new List<int>();
genericList.Add(42);   // NO boxing
int y = genericList[0]; // NO unboxing

// 3. Interface access on value type
IComparable comp = 42;  // boxing (int implements IComparable)

// ── How to avoid boxing ───────────────────────────────
// ✅ Generic collections: List<T>, Dictionary<K,V>
// ✅ Generic methods with constraints
// ✅ IEquatable<T>, IComparable<T> on structs
// ✅ Span<T> for temporary operations

// ── struct with generic interface — no boxing ─────────
public struct Temperature : IComparable<Temperature>
{
    public double Value { get; }
    public Temperature(double value) => Value = value;
    public int CompareTo(Temperature other) => Value.CompareTo(other.Value);
    // IComparable<Temperature> — generic, no boxing!
}

var t1 = new Temperature(36.6);
var t2 = new Temperature(37.0);
int cmp = t1.CompareTo(t2); // no boxing!
```

**Performance Impact:**

| Operation | Cost |
|-----------|------|
| Boxing | Heap allocation + copy |
| Unboxing | Cast check + copy |
| Generic List\<int\> | ~10× faster than ArrayList |
| GC pressure | Boxing creates short-lived objects |

---

<a id="p4-patterns"></a>
### Topic 11: Pattern Matching (C# 7–12)

```csharp
// ── Type patterns ─────────────────────────────────────
object shape = new Circle { Radius = 5 };

// C# 7 is pattern
if (shape is Circle c)
    Console.WriteLine($"Circle radius: {c.Radius}");

// C# 8 switch expression
string desc = shape switch
{
    Circle { Radius: > 10 } c => $"Large circle r={c.Radius}",
    Circle c                  => $"Small circle r={c.Radius}",
    Rectangle r               => $"Rect {r.Width}x{r.Height}",
    null                      => "null",
    _                         => "Unknown"
};

// ── Property patterns ─────────────────────────────────
var order = new Order { Status = "Paid", Amount = 15000m };

string message = order switch
{
    { Status: "Pending", Amount: < 1000 }  => "Small pending order",
    { Status: "Pending", Amount: >= 1000 } => "Large pending order",
    { Status: "Paid" }                     => "Order paid",
    { Status: "Cancelled" }               => "Order cancelled",
    _                                      => "Unknown status"
};

// ── Tuple patterns ────────────────────────────────────
(bool isAdmin, bool isActive) user = (true, true);

string access = user switch
{
    (true, true)   => "Full access",
    (true, false)  => "Admin disabled",
    (false, true)  => "Standard user",
    (false, false) => "No access"
};

// ── Relational patterns (C# 9+) ───────────────────────
int score = 78;
string grade = score switch
{
    >= 90 => "A+",
    >= 80 => "A",
    >= 70 => "B",
    >= 60 => "C",
    _     => "F"
}; // "B"

// ── Logical patterns (C# 9+) ─────────────────────────
string category = score switch
{
    > 90 and <= 100 => "Excellent",
    > 70 and <= 90  => "Good",
    > 50 and <= 70  => "Average",
    not > 50        => "Poor",
    _               => "Invalid"
};

// ── List patterns (C# 11+) ────────────────────────────
int[] arr = { 1, 2, 3, 4, 5 };

bool match1 = arr is [1, 2, ..];          // starts with 1, 2
bool match2 = arr is [.., 4, 5];          // ends with 4, 5
bool match3 = arr is [1, _, _, _, 5];     // 5 elements, first=1 last=5

if (arr is [var head, .. var tail])
    Console.WriteLine($"Head: {head}, Tail count: {tail.Length}");
```

---

## PART 4 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| Delegate | Method reference — type-safe function pointer |
| Action\<T\> | Delegate returning void |
| Func\<T, TResult\> | Delegate returning value |
| Predicate\<T\> | Delegate returning bool |
| Multicast | += দিয়ে multiple methods attach |
| Event | Delegate wrapper — only declaring class invokes |
| Lambda | `x => x * x` — anonymous function |
| Closure | Outer variable capture — reference, not value |
| LINQ | Language Integrated Query — method/query syntax |
| Deferred execution | ToList()/Count() না হলে query চলে না |
| IEnumerable\<T\> | In-memory LINQ |
| IQueryable\<T\> | Database LINQ — SQL generates |
| Generics `<T>` | Type-safe reusable code — no boxing |
| Generic constraint | `where T : class, IEntity, new()` |
| async/await | Non-blocking I/O — thread yield করে |
| Task | Async operation handle |
| ValueTask | Allocation-free async for hot paths |
| CancellationToken | Cooperative cancellation |
| ConfigureAwait(false) | Library code-এ deadlock prevention |
| async void | ❌ Dangerous — exceptions lost |
| Parallel.For | CPU-bound parallel execution |
| lock | Mutual exclusion — shared state protection |
| ConcurrentDictionary | Thread-safe dictionary |
| GC Generations | Gen 0 → Gen 1 → Gen 2 |
| Boxing | Value type → object (heap allocation) |
| Unboxing | Object → value type (explicit cast) |
| IDisposable | Deterministic cleanup |
| using | Guaranteed Dispose() even on exception |
| Span\<T\> | Zero-copy stack-based slice |
| Pattern matching | switch expression, is patterns |

---

## PART 4 Interview Q&A

```
প্রশ্ন: Delegate আর interface-এর পার্থক্য?
উত্তর: Delegate → single method callback। Event, LINQ।
       Interface → multiple method contract। OOP, DI।
       Single method → delegate। Multiple methods → interface।

প্রশ্ন: async/await কীভাবে কাজ করে internally?
উত্তর: Compiler state machine generate করে।
await point-এ current state save, thread return করে।
I/O complete হলে threadpool thread state restore করে continue করে।

প্রশ্ন: LINQ deferred execution কী?
উত্তর: Where/Select/OrderBy — query object তৈরি করে, execute করে না।
ToList()/ToArray()/Count()/First() → actually execute হয়।

প্রশ্ন: Boxing কখন হয়?
উত্তর: Value type object variable-এ store করলে।
Non-generic collection-এ। Interface cast-এ।
Generic collection ব্যবহার করলে boxing নেই।

প্রশ্ন: IDisposable কেন implement করবেন?
উত্তর: Unmanaged resources (file, DB connection, socket)।
using statement-এ deterministic cleanup guarantee।

প্রশ্ন: Task.WhenAll আর Task.WhenAny পার্থক্য?
উত্তর: WhenAll → সব tasks complete হওয়ার জন্য wait।
WhenAny → যেকোনো একটি complete হলেই return।
WhenAll → parallel fetching (DB + cache + API একসাথে)।
WhenAny → timeout, fallback, race।

প্রশ্ন: IEnumerable<T> আর IQueryable<T> পার্থক্য?
উত্তর: IEnumerable → in-memory filter।
IQueryable → database-এ SQL generate করে filter।
EF Core-এ সবসময় IQueryable রাখুন, যতক্ষণ না ToList() করতে হয়।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 5 — ASP.NET Core Fundamentals (Middleware, Routing, Dependency Injection, Configuration, Filters, Minimal APIs এবং আরও...)

---

<a id="part5"></a>
## PART 5: ASP.NET Core Fundamentals

> Middleware Pipeline, Routing, Dependency Injection, Configuration, Filters, Minimal APIs, Model Binding ও Validation।

| # | বিষয় |
|---|-------|
| 1 | [ASP.NET Core Architecture](#p5-architecture) |
| 2 | [Middleware Pipeline](#p5-middleware) |
| 3 | [Routing](#p5-routing) |
| 4 | [Dependency Injection Container](#p5-di) |
| 5 | [Configuration System](#p5-config) |
| 6 | [Action Filters ও Resource Filters](#p5-filters) |
| 7 | [Minimal APIs vs Controllers](#p5-minimal) |
| 8 | [Model Binding](#p5-binding) |
| 9 | [Validation](#p5-validation) |
| 10 | [Request/Response Pipeline Internals](#p5-pipeline) |

---

<a id="p5-architecture"></a>
### Topic 1: ASP.NET Core Architecture

```
┌─────────────────────────────────────────────────┐
│                  Client (Browser/Mobile)         │
└─────────────────────┬───────────────────────────┘
                      │ HTTP Request
┌─────────────────────▼───────────────────────────┐
│               Kestrel (HTTP Server)              │
└─────────────────────┬───────────────────────────┘
                      │
┌─────────────────────▼───────────────────────────┐
│          ASP.NET Core Middleware Pipeline        │
│  ┌──────────┐  ┌──────────┐  ┌──────────────┐  │
│  │Exception │→ │  Auth    │→ │   Routing    │  │
│  │Handler   │  │Middleware│  │  Middleware  │  │
│  └──────────┘  └──────────┘  └──────────────┘  │
│  ┌──────────┐  ┌──────────┐  ┌──────────────┐  │
│  │  CORS    │→ │  Static  │→ │  Endpoints   │  │
│  │Middleware│  │  Files   │  │  (Controller │  │
│  └──────────┘  └──────────┘  │   / Minimal) │  │
│                               └──────────────┘  │
└─────────────────────────────────────────────────┘
```

```csharp
// ── Program.cs — .NET 6+ minimal hosting model ────────
var builder = WebApplication.CreateBuilder(args);

// ── Service Registration (DI Container) ───────────────
builder.Services.AddControllers();
builder.Services.AddEndpointsApiExplorer();
builder.Services.AddSwaggerGen();
builder.Services.AddDbContext<AppDbContext>(opt =>
    opt.UseSqlServer(builder.Configuration.GetConnectionString("Default")));
builder.Services.AddScoped<IOrderService, OrderService>();
builder.Services.AddMemoryCache();

var app = builder.Build();

// ── Middleware Pipeline ────────────────────────────────
if (app.Environment.IsDevelopment())
{
    app.UseSwagger();
    app.UseSwaggerUI();
}

app.UseHttpsRedirection();   // HTTPS redirect
app.UseStaticFiles();        // wwwroot files
app.UseCors("AllowAll");     // CORS
app.UseAuthentication();     // who are you?
app.UseAuthorization();      // what can you do?
app.MapControllers();        // route to controllers

app.Run();
```

---

<a id="p5-middleware"></a>
### Topic 2: Middleware Pipeline

**সহজ ভাষায়:**

> **Middleware** হলো pipeline-এর প্রতিটি পদক্ষেপ। Request → middleware 1 → middleware 2 → ... → endpoint → ... → middleware 2 → middleware 1 → Response।

**Analogy:** Airport security — passport check, luggage scan, boarding gate — প্রতিটি step request process করে এবং পরের step-এ pass করে।

```csharp
// ── Middleware execution order (CRITICAL) ─────────────
//
//  Request →  A  →  B  →  C  →  Handler
//  Response ← A  ← B  ← C  ←
//
//  app.Use() — pipeline-এ add, পরের middleware call করে
//  app.Run() — terminal, পরের middleware call করে না
//  app.Map() — path prefix-এ branch করে

// ── Built-in middleware ordering ─────────────────────
app.UseExceptionHandler("/error"); // 1. সবার আগে — সব exception catch
app.UseHsts();                     // 2. HSTS header
app.UseHttpsRedirection();         // 3. HTTP → HTTPS
app.UseStaticFiles();              // 4. wwwroot files (no auth needed)
app.UseRouting();                  // 5. Route matching
app.UseCors();                     // 6. CORS headers
app.UseAuthentication();           // 7. Auth check (JWT, Cookie)
app.UseAuthorization();            // 8. Permission check
app.MapControllers();              // 9. Controller/endpoint dispatch

// ── Custom Middleware — class approach ────────────────
public class RequestLoggingMiddleware
{
    private readonly RequestDelegate _next;
    private readonly ILogger<RequestLoggingMiddleware> _logger;

    public RequestLoggingMiddleware(RequestDelegate next,
        ILogger<RequestLoggingMiddleware> logger)
    {
        _next = next;
        _logger = logger;
    }

    public async Task InvokeAsync(HttpContext context)
    {
        var sw = Stopwatch.StartNew();
        _logger.LogInformation(
            "Request {Method} {Path} started",
            context.Request.Method,
            context.Request.Path);

        await _next(context);  // pass to next middleware

        sw.Stop();
        _logger.LogInformation(
            "Request {Method} {Path} completed {StatusCode} in {Elapsed}ms",
            context.Request.Method,
            context.Request.Path,
            context.Response.StatusCode,
            sw.ElapsedMilliseconds);
    }
}

// Extension method — clean registration
public static class MiddlewareExtensions
{
    public static IApplicationBuilder UseRequestLogging(
        this IApplicationBuilder app) =>
        app.UseMiddleware<RequestLoggingMiddleware>();
}

// Usage:
app.UseRequestLogging();

// ── Inline middleware (simple cases) ─────────────────
app.Use(async (context, next) =>
{
    context.Response.Headers["X-Request-Id"] = Guid.NewGuid().ToString();
    await next(context);
});

// ── Short-circuit middleware ───────────────────────────
app.Use(async (context, next) =>
{
    if (context.Request.Headers["X-Maintenance-Key"] != "secret-key" &&
        IsMaintenanceMode())
    {
        context.Response.StatusCode = 503;
        await context.Response.WriteAsync("Under maintenance");
        return;  // short-circuit — পরের middleware call হয় না!
    }
    await next(context);
});

// ── Branching middleware ───────────────────────────────
app.Map("/health", healthApp =>
{
    healthApp.Run(async context =>
    {
        context.Response.ContentType = "application/json";
        await context.Response.WriteAsync("{\"status\":\"healthy\"}");
    });
});

// MapWhen — condition-based branching
app.MapWhen(
    ctx => ctx.Request.Path.StartsWithSegments("/api/v1"),
    v1App => v1App.UseMiddleware<V1ApiMiddleware>()
);
```

**🎤 Interview Q&A:**

```
প্রশ্ন: Middleware order কেন important?

উত্তর: UseAuthentication আগে না হলে UseAuthorization কাজ করে না।
UseExceptionHandler সবার আগে দিতে হয় — নাহলে আগের middleware-র exceptions miss হয়।
UseStaticFiles → UseRouting এর আগে — auth ছাড়াই static files serve করতে।

প্রশ্ন: app.Use() আর app.Run() পার্থক্য?

উত্তর:
Use() → next(context) call করে পরের middleware-এ pass করে।
Run() → terminal middleware। কোনো পরের middleware call করে না।
Map() → path prefix match করলে branch করে।
```

---

<a id="p5-routing"></a>
### Topic 3: Routing

```csharp
// ── Conventional routing ──────────────────────────────
app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");

// ── Attribute routing (API সবচেয়ে বেশি ব্যবহৃত) ──────
[ApiController]
[Route("api/v1/[controller]")] // [controller] → "orders"
public class OrdersController : ControllerBase
{
    // GET api/v1/orders
    [HttpGet]
    public IActionResult GetAll() => Ok();

    // GET api/v1/orders/5
    [HttpGet("{id:int}")]
    public IActionResult GetById(int id) => Ok();

    // GET api/v1/orders/5/items
    [HttpGet("{id:int}/items")]
    public IActionResult GetItems(int id) => Ok();

    // POST api/v1/orders
    [HttpPost]
    public IActionResult Create([FromBody] CreateOrderDto dto) => Ok();

    // PUT api/v1/orders/5
    [HttpPut("{id:int}")]
    public IActionResult Update(int id, [FromBody] UpdateOrderDto dto) => Ok();

    // DELETE api/v1/orders/5
    [HttpDelete("{id:int}")]
    public IActionResult Delete(int id) => Ok();
}

// ── Route constraints ─────────────────────────────────
// {id:int}        — integer only
// {id:guid}       — GUID
// {id:min(1)}     — int >= 1
// {id:range(1,100)} — int between 1-100
// {name:alpha}    — letters only
// {name:length(3,20)} — string 3-20 chars
// {id:required}   — must be provided

[HttpGet("{id:int:min(1)}")]       // id must be positive int
public IActionResult Get(int id) => Ok();

[HttpGet("{slug:alpha:length(3,50)}")]  // alpha, 3-50 chars
public IActionResult GetBySlug(string slug) => Ok();

// ── Route parameters ─────────────────────────────────
[HttpGet("search")]
public IActionResult Search(
    [FromQuery] string? q,          // /search?q=laptop
    [FromQuery] int page = 1,
    [FromQuery] int pageSize = 20) => Ok();

[HttpPost("upload")]
public IActionResult Upload([FromForm] IFormFile file) => Ok();

[HttpGet]
public IActionResult GetWithHeader(
    [FromHeader(Name = "X-Api-Key")] string apiKey) => Ok();
```

---

<a id="p5-di"></a>
### Topic 4: Dependency Injection Container

**সহজ ভাষায়:**

> **DI Container** নিজেই object তৈরি করে inject করে। Manual `new` করতে হয় না। Testable, loosely coupled code।

```csharp
// ── Service lifetimes ─────────────────────────────────
//
// Transient  — প্রতি inject-এ নতুন instance
// Scoped     — প্রতি HTTP request-এ একটি instance
// Singleton  — Application lifetime-এ একটি instance

builder.Services.AddTransient<IEmailSender, SmtpEmailSender>();
builder.Services.AddScoped<IOrderRepository, OrderRepository>();
builder.Services.AddSingleton<ICacheService, MemoryCacheService>();

// ── Keyed services (C# .NET 8+) ──────────────────────
builder.Services.AddKeyedScoped<IPaymentGateway, BkashGateway>("bkash");
builder.Services.AddKeyedScoped<IPaymentGateway, NagadGateway>("nagad");

// Usage in controller:
public class PaymentController : ControllerBase
{
    private readonly IPaymentGateway _bkash;
    private readonly IPaymentGateway _nagad;

    public PaymentController(
        [FromKeyedServices("bkash")] IPaymentGateway bkash,
        [FromKeyedServices("nagad")] IPaymentGateway nagad)
    {
        _bkash = bkash;
        _nagad = nagad;
    }
}

// ── Factory registration ──────────────────────────────
builder.Services.AddScoped<IDbConnection>(_ =>
    new SqlConnection(builder.Configuration.GetConnectionString("Default")));

// ── Options pattern — configure DI with settings ──────
public class SmtpOptions
{
    public string Host    { get; set; } = "";
    public int    Port    { get; set; }
    public string UserName { get; set; } = "";
    public string Password { get; set; } = "";
}

builder.Services.Configure<SmtpOptions>(
    builder.Configuration.GetSection("Smtp"));

// Service consuming options:
public class EmailService
{
    private readonly SmtpOptions _options;
    public EmailService(IOptions<SmtpOptions> options) =>
        _options = options.Value;
}

// ── Resolve from DI manually ──────────────────────────
// Avoid! Only in startup/factory code
using var scope = app.Services.CreateScope();
var dbContext = scope.ServiceProvider.GetRequiredService<AppDbContext>();
await dbContext.Database.MigrateAsync();
```

**🎤 Interview Q&A:**

```
প্রশ্ন: Scoped service Singleton-এ inject করলে কী হয়?

উত্তর: "Captive dependency" problem!
Singleton একটিই — পুরো app lifetime।
Scoped service প্রতি request-এ নতুন হওয়ার কথা।
Singleton এ inject হলে প্রথম request-এর Scoped instance সবার জন্য shared!

Solution: IServiceScopeFactory inject করে runtime-এ scope তৈরি করুন।

প্রশ্ন: Transient, Scoped, Singleton কোনটি কখন?

উত্তর:
Transient → Stateless, lightweight service। Email sender।
Scoped    → DB Context, Unit of Work। Per-request state।
Singleton → Cache, Configuration। Shared state। Thread-safe হতে হবে।
```

---

<a id="p5-config"></a>
### Topic 5: Configuration System

```csharp
// ── appsettings.json ──────────────────────────────────
// {
//   "ConnectionStrings": {
//     "Default": "Server=localhost;Database=MyDb;Trusted_Connection=true"
//   },
//   "Smtp": {
//     "Host": "smtp.gmail.com",
//     "Port": 587
//   },
//   "Jwt": {
//     "Key": "super-secret-key-min-32-chars",
//     "Issuer": "https://myapi.com",
//     "ExpiryMinutes": 60
//   },
//   "Logging": {
//     "LogLevel": { "Default": "Information" }
//   }
// }

// ── Reading configuration ─────────────────────────────
var connStr = builder.Configuration.GetConnectionString("Default");
var smtpHost = builder.Configuration["Smtp:Host"];
var port = builder.Configuration.GetValue<int>("Smtp:Port");

// ── Options pattern (strongly-typed, recommended) ─────
public class JwtOptions
{
    public const string SectionName = "Jwt";
    public string Key            { get; set; } = "";
    public string Issuer         { get; set; } = "";
    public int    ExpiryMinutes  { get; set; } = 60;
}

builder.Services
    .AddOptions<JwtOptions>()
    .BindConfiguration(JwtOptions.SectionName)
    .ValidateDataAnnotations()
    .ValidateOnStart();

// ── Environment variables override appsettings ────────
// Env: ConnectionStrings__Default=Server=prod-server...
// Env: Smtp__Host=smtp.sendgrid.com
// __ (double underscore) = : (colon) in hierarchy

// ── User Secrets — local dev only ────────────────────
// dotnet user-secrets init
// dotnet user-secrets set "Jwt:Key" "my-dev-secret-key"
// Stored in ~/.microsoft/usersecrets/{guid}/secrets.json
// Never commit to git!

// ── Environment-specific settings ────────────────────
// appsettings.json           — base config
// appsettings.Development.json — dev overrides
// appsettings.Production.json  — prod overrides
// Loaded in order, later overrides earlier

// ── IConfiguration in controller ─────────────────────
[ApiController]
[Route("api/[controller]")]
public class InfoController : ControllerBase
{
    private readonly IConfiguration _config;
    private readonly JwtOptions _jwt;

    public InfoController(IConfiguration config, IOptions<JwtOptions> jwt)
    {
        _config = config;
        _jwt = jwt.Value;
    }

    [HttpGet("env")]
    public IActionResult GetEnv() =>
        Ok(new { env = _config["ASPNETCORE_ENVIRONMENT"] ?? "Production" });
}
```

---

<a id="p5-filters"></a>
### Topic 6: Action Filters ও Resource Filters

**সহজ ভাষায়:**

> **Filter** — controller action-এর আগে/পরে code চালানো। Logging, auth check, caching, validation — cross-cutting concerns।

```
Filter Pipeline:
────────────────────────────────────────────────────
Authorization → Resource → Exception
                    ↓
               Action (Before) → Controller Action → Action (After)
                    ↓
               Result (Before) → Result Execution → Result (After)
────────────────────────────────────────────────────
```

```csharp
// ── Action Filter — before/after action method ────────
public class LogActionFilter : IActionFilter
{
    private readonly ILogger<LogActionFilter> _logger;
    public LogActionFilter(ILogger<LogActionFilter> logger) => _logger = logger;

    public void OnActionExecuting(ActionExecutingContext context)
    {
        _logger.LogInformation(
            "Action {Action} starting with args: {@Args}",
            context.ActionDescriptor.DisplayName,
            context.ActionArguments);
    }

    public void OnActionExecuted(ActionExecutedContext context)
    {
        if (context.Exception is not null)
            _logger.LogError(context.Exception, "Action threw exception");
        else
            _logger.LogInformation("Action completed");
    }
}

// ── Async Action Filter ───────────────────────────────
public class ValidateModelFilter : IAsyncActionFilter
{
    public async Task OnActionExecutionAsync(
        ActionExecutingContext context,
        ActionExecutionDelegate next)
    {
        // Before action
        if (!context.ModelState.IsValid)
        {
            context.Result = new BadRequestObjectResult(context.ModelState);
            return;  // short-circuit
        }

        await next();  // execute action

        // After action
    }
}

// ── Exception Filter ──────────────────────────────────
public class GlobalExceptionFilter : IExceptionFilter
{
    private readonly ILogger<GlobalExceptionFilter> _logger;
    public GlobalExceptionFilter(ILogger<GlobalExceptionFilter> logger) =>
        _logger = logger;

    public void OnException(ExceptionContext context)
    {
        _logger.LogError(context.Exception, "Unhandled exception");

        var problem = new ProblemDetails
        {
            Status = context.Exception is KeyNotFoundException ? 404 : 500,
            Title  = context.Exception is KeyNotFoundException
                        ? "Resource not found" : "Internal server error",
            Detail = context.Exception.Message
        };

        context.Result = new ObjectResult(problem) { StatusCode = problem.Status };
        context.ExceptionHandled = true;
    }
}

// ── Register globally ─────────────────────────────────
builder.Services.AddControllers(options =>
{
    options.Filters.Add<ValidateModelFilter>();
    options.Filters.Add<GlobalExceptionFilter>();
    options.Filters.Add<LogActionFilter>();
});

// ── Register per controller/action via attribute ──────
[ServiceFilter(typeof(LogActionFilter))]
public class OrdersController : ControllerBase
{
    [HttpPost]
    [ServiceFilter(typeof(ValidateModelFilter))]
    public IActionResult Create([FromBody] CreateOrderDto dto) => Ok();
}

// ── Custom attribute filter ───────────────────────────
[AttributeUsage(AttributeTargets.Method | AttributeTargets.Class)]
public class RequireApiKeyAttribute : ActionFilterAttribute
{
    public override void OnActionExecuting(ActionExecutingContext context)
    {
        if (!context.HttpContext.Request.Headers.TryGetValue("X-Api-Key", out var key) ||
            key != "expected-key")
        {
            context.Result = new UnauthorizedResult();
        }
    }
}

[HttpGet("internal")]
[RequireApiKey]
public IActionResult InternalEndpoint() => Ok();
```

---

<a id="p5-minimal"></a>
### Topic 7: Minimal APIs vs Controllers

```csharp
// ── Minimal API — .NET 6+ ─────────────────────────────
var app = WebApplication.Create(args);

// Simple endpoints
app.MapGet("/", () => "Hello World");

app.MapGet("/orders/{id:int}", async (int id, IOrderService service) =>
{
    var order = await service.GetByIdAsync(id);
    return order is null ? Results.NotFound() : Results.Ok(order);
});

app.MapPost("/orders", async (CreateOrderDto dto, IOrderService service) =>
{
    var order = await service.CreateAsync(dto);
    return Results.Created($"/orders/{order.Id}", order);
});

app.MapPut("/orders/{id:int}", async (int id, UpdateOrderDto dto, IOrderService service) =>
{
    var updated = await service.UpdateAsync(id, dto);
    return updated ? Results.NoContent() : Results.NotFound();
});

app.MapDelete("/orders/{id:int}", async (int id, IOrderService service) =>
{
    var deleted = await service.DeleteAsync(id);
    return deleted ? Results.NoContent() : Results.NotFound();
});

// ── Minimal API groups (organise routes) ─────────────
var ordersGroup = app.MapGroup("/api/v1/orders")
    .WithTags("Orders")
    .RequireAuthorization();

ordersGroup.MapGet("/", GetAllOrders);
ordersGroup.MapGet("/{id:int}", GetOrderById);
ordersGroup.MapPost("/", CreateOrder);

// ── Static handler methods ────────────────────────────
static async Task<IResult> GetAllOrders(IOrderService service) =>
    Results.Ok(await service.GetAllAsync());

static async Task<IResult> GetOrderById(int id, IOrderService service) =>
    await service.GetByIdAsync(id) is {} order
        ? Results.Ok(order)
        : Results.NotFound();

// ── Minimal API vs Controller — comparison ────────────
//
// Minimal API:
// ✅ Less boilerplate — no class, no [Route]
// ✅ Fast startup — fewer reflection overhead
// ✅ Simple CRUD APIs, microservices
// ❌ Harder to organise large codebases
// ❌ Less built-in features (filters, model binding)
//
// Controller:
// ✅ Convention-based routing
// ✅ Filters, action results, model binding
// ✅ Better for large, complex APIs
// ✅ Familiar MVC pattern
// ❌ More boilerplate
// ❌ Heavier startup
```

---

<a id="p5-binding"></a>
### Topic 8: Model Binding

**সহজ ভাষায়:**

> **Model Binding** — HTTP request-এর data (query string, body, route, header, form) → C# object-এ automatically convert।

```csharp
[ApiController]
[Route("api/[controller]")]
public class ProductsController : ControllerBase
{
    // ── Binding sources ───────────────────────────────

    // [FromRoute] — route parameter থেকে
    [HttpGet("{id:int}")]
    public IActionResult Get([FromRoute] int id) => Ok();

    // [FromQuery] — query string থেকে → /products?page=2&pageSize=10
    [HttpGet]
    public IActionResult GetAll(
        [FromQuery] int page = 1,
        [FromQuery] int pageSize = 20,
        [FromQuery] string? search = null) => Ok();

    // [FromBody] — JSON request body থেকে
    [HttpPost]
    public IActionResult Create([FromBody] CreateProductDto dto) => Ok();

    // [FromHeader] — request header থেকে
    [HttpGet("check")]
    public IActionResult Check(
        [FromHeader(Name = "X-Correlation-Id")] string correlationId) => Ok();

    // [FromForm] — multipart/form-data থেকে
    [HttpPost("upload")]
    public IActionResult Upload(
        [FromForm] string title,
        [FromForm] IFormFile image) => Ok();

    // Multiple sources in one action
    [HttpPut("{id:int}")]
    public IActionResult Update(
        [FromRoute] int id,
        [FromBody] UpdateProductDto dto,
        [FromHeader(Name = "If-Match")] string? etag = null) => Ok();
}

// ── Complex binding — nested objects ─────────────────
public class SearchRequest
{
    [FromQuery] public string? Query    { get; set; }
    [FromQuery] public int     Page     { get; set; } = 1;
    [FromQuery] public int     PageSize { get; set; } = 20;
    [FromQuery] public string? Sort     { get; set; } = "name";
    [FromQuery] public bool    Ascending { get; set; } = true;
}

[HttpGet("search")]
public IActionResult Search([FromQuery] SearchRequest request) => Ok();
// GET /search?Query=laptop&Page=2&Sort=price&Ascending=false

// ── Custom model binder ───────────────────────────────
public class CommaSeparatedBinder : IModelBinder
{
    public Task BindModelAsync(ModelBindingContext context)
    {
        var value = context.ValueProvider.GetValue(context.ModelName).FirstValue;
        if (string.IsNullOrEmpty(value))
        {
            context.Result = ModelBindingResult.Success(Array.Empty<int>());
            return Task.CompletedTask;
        }

        var ids = value.Split(',')
            .Select(s => int.TryParse(s, out var n) ? n : -1)
            .Where(n => n > 0)
            .ToArray();

        context.Result = ModelBindingResult.Success(ids);
        return Task.CompletedTask;
    }
}

// Usage: GET /products?ids=1,2,3,4
[HttpGet("bulk")]
public IActionResult GetBulk(
    [ModelBinder(typeof(CommaSeparatedBinder))] int[] ids) => Ok();
```

---

<a id="p5-validation"></a>
### Topic 9: Validation

```csharp
// ── Data Annotations ─────────────────────────────────
public class CreateOrderDto
{
    [Required(ErrorMessage = "Customer ID is required")]
    public int CustomerId { get; set; }

    [Required]
    [StringLength(200, MinimumLength = 3, ErrorMessage = "Notes must be 3-200 chars")]
    public string Notes { get; set; } = "";

    [Required]
    [MinLength(1, ErrorMessage = "At least one item required")]
    public List<OrderItemDto> Items { get; set; } = new();

    [Range(0, double.MaxValue, ErrorMessage = "Discount cannot be negative")]
    public decimal Discount { get; set; }

    [EmailAddress]
    public string? ContactEmail { get; set; }

    [Phone]
    public string? ContactPhone { get; set; }

    [Url]
    public string? CallbackUrl { get; set; }
}

public class OrderItemDto
{
    [Required]
    [Range(1, int.MaxValue)]
    public int ProductId { get; set; }

    [Required]
    [Range(1, 1000)]
    public int Quantity { get; set; }

    [Range(0.01, double.MaxValue)]
    public decimal UnitPrice { get; set; }
}

// ── [ApiController] — automatic 400 on invalid model ──
// [ApiController] attribute থাকলে ModelState invalid হলে
// automatically 400 BadRequest return হয়।
// explicit if (!ModelState.IsValid) check দরকার নেই।

[ApiController]  // auto-validates!
[Route("api/[controller]")]
public class OrdersController : ControllerBase
{
    [HttpPost]
    public async Task<IActionResult> Create([FromBody] CreateOrderDto dto)
    {
        // No need to check ModelState — [ApiController] handles it
        var order = await _service.CreateAsync(dto);
        return CreatedAtAction(nameof(GetById), new { id = order.Id }, order);
    }
}

// ── Custom validation attribute ────────────────────────
public class FutureDateAttribute : ValidationAttribute
{
    protected override ValidationResult? IsValid(
        object? value, ValidationContext context)
    {
        if (value is DateTime date && date > DateTime.UtcNow)
            return ValidationResult.Success;

        return new ValidationResult("Date must be in the future.");
    }
}

public class DeliveryDto
{
    [Required]
    [FutureDate]
    public DateTime DeliveryDate { get; set; }
}

// ── IValidatableObject — cross-field validation ────────
public class TransferDto : IValidatableObject
{
    [Required]
    public string FromAccount { get; set; } = "";
    [Required]
    public string ToAccount { get; set; } = "";
    [Range(1, 10_000_000)]
    public decimal Amount { get; set; }

    public IEnumerable<ValidationResult> Validate(ValidationContext context)
    {
        if (FromAccount == ToAccount)
            yield return new ValidationResult(
                "Cannot transfer to same account.",
                new[] { nameof(FromAccount), nameof(ToAccount) });

        if (Amount > 100_000 && string.IsNullOrEmpty(Notes))
            yield return new ValidationResult(
                "Notes required for transfers over 100,000.",
                new[] { nameof(Notes) });
    }

    public string? Notes { get; set; }
}

// ── FluentValidation (preferred for complex rules) ─────
// Install: dotnet add package FluentValidation.AspNetCore

public class CreateOrderValidator : AbstractValidator<CreateOrderDto>
{
    private readonly IProductRepository _products;

    public CreateOrderValidator(IProductRepository products)
    {
        _products = products;

        RuleFor(x => x.CustomerId)
            .GreaterThan(0).WithMessage("Invalid customer ID");

        RuleFor(x => x.Items)
            .NotEmpty().WithMessage("Order must have at least one item")
            .Must(items => items.Count <= 100).WithMessage("Max 100 items");

        RuleForEach(x => x.Items).ChildRules(item =>
        {
            item.RuleFor(x => x.Quantity).InclusiveBetween(1, 1000);
            item.RuleFor(x => x.UnitPrice).GreaterThan(0);
            item.RuleFor(x => x.ProductId)
                .MustAsync(async (id, ct) => await _products.ExistsAsync(id))
                .WithMessage("Product not found");
        });

        RuleFor(x => x.Discount)
            .InclusiveBetween(0, 100).WithMessage("Discount must be 0-100%");
    }
}

// Register:
builder.Services.AddFluentValidationAutoValidation();
builder.Services.AddScoped<IValidator<CreateOrderDto>, CreateOrderValidator>();
```

---

<a id="p5-pipeline"></a>
### Topic 10: Request/Response Pipeline Internals

```csharp
// ── HttpContext — request/response সব তথ্য ────────────
app.Use(async (HttpContext ctx, RequestDelegate next) =>
{
    // Request
    var method  = ctx.Request.Method;          // "GET", "POST"
    var path    = ctx.Request.Path;            // "/api/orders"
    var query   = ctx.Request.QueryString;     // "?page=1"
    var headers = ctx.Request.Headers;
    var body    = ctx.Request.Body;            // Stream
    var ip      = ctx.Connection.RemoteIpAddress;

    // User (after authentication)
    var userId  = ctx.User.FindFirst("sub")?.Value;
    var isAdmin = ctx.User.IsInRole("Admin");

    // Response
    ctx.Response.StatusCode = 200;
    ctx.Response.Headers["X-Custom"] = "value";
    ctx.Response.ContentType = "application/json";
    await ctx.Response.WriteAsync("{}");

    // Items — pass data between middleware
    ctx.Items["RequestId"] = Guid.NewGuid();
    await next(ctx);
    var reqId = ctx.Items["RequestId"] as Guid?;
});

// ── IHttpContextAccessor — access HttpContext in services ─
builder.Services.AddHttpContextAccessor();

public class CurrentUserService
{
    private readonly IHttpContextAccessor _accessor;
    public CurrentUserService(IHttpContextAccessor accessor) =>
        _accessor = accessor;

    public int? GetUserId()
    {
        var claim = _accessor.HttpContext?.User.FindFirst("sub");
        return int.TryParse(claim?.Value, out var id) ? id : null;
    }
}

// ── Problem Details — RFC 7807 standard error response ──
[HttpGet("{id:int}")]
public async Task<ActionResult<OrderDto>> GetById(int id)
{
    var order = await _service.GetByIdAsync(id);
    if (order is null)
        return Problem(
            statusCode: 404,
            title: "Order not found",
            detail: $"Order with ID {id} does not exist.");
    return Ok(order);
}

// Response:
// {
//   "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
//   "title": "Order not found",
//   "status": 404,
//   "detail": "Order with ID 99 does not exist."
// }
```

---

## PART 5 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| Middleware | Request/Response pipeline-এর প্রতিটি step |
| app.Use() | Next middleware-এ pass করে |
| app.Run() | Terminal — পরের middleware call করে না |
| Middleware order | ExceptionHandler → HTTPS → Static → Routing → CORS → Auth → Authz → Endpoints |
| Conventional routing | `{controller}/{action}/{id?}` pattern |
| Attribute routing | `[Route]`, `[HttpGet]`, `[HttpPost]` |
| Route constraints | `{id:int}`, `{id:guid}`, `{name:alpha}` |
| Transient | নতুন instance প্রতি inject-এ |
| Scoped | নতুন instance প্রতি HTTP request-এ |
| Singleton | একটি instance পুরো app-এ |
| Captive dependency | Scoped in Singleton = bug! |
| Options pattern | Strongly-typed config binding |
| User Secrets | Dev-এ secrets → never commit |
| Action Filter | Action আগে/পরে code চালানো |
| Exception Filter | Unhandled exceptions catch করা |
| `[ApiController]` | Auto 400 on invalid ModelState |
| Model Binding | HTTP data → C# object |
| `[FromBody]` | JSON body থেকে |
| `[FromQuery]` | Query string থেকে |
| `[FromRoute]` | Route parameter থেকে |
| `[FromHeader]` | Request header থেকে |
| Data Annotations | `[Required]`, `[Range]`, `[StringLength]` |
| FluentValidation | Complex business rule validation |
| `IValidatableObject` | Cross-field validation |
| Minimal API | Controller-less endpoint — less boilerplate |
| `Results.Ok()` | Minimal API result helper |
| HttpContext | Request/Response সব data |
| Problem Details | RFC 7807 standard error response format |

---

## PART 5 Interview Q&A

```
প্রশ্ন: Middleware আর Filter-এর পার্থক্য?
উত্তর:
Middleware → Entire pipeline-এ কাজ করে। Any request।
Filter → Controller/Action scope-এ কাজ করে। MVC/API specific।
Auth, logging, CORS → Middleware।
Validation, response shaping → Filter।

প্রশ্ন: [ApiController] কী করে?
উত্তর:
1. ModelState invalid হলে auto 400 return।
2. [FromBody] inference — explicit attribute না লিখলেও complex type = from body।
3. Problem Details format।
4. Route attribute required।

প্রশ্ন: Transient vs Scoped কোনটা DbContext-এ?
উত্তর: Scoped! DbContext per-request একটি থাকা উচিত।
Change tracking, transaction same request-এর সব operations-এ share হয়।
Transient হলে প্রতি inject-এ নতুন context — tracking হারায়।
Singleton হলে concurrency bug, connection leak।

প্রশ্ন: Configuration hierarchy কীভাবে কাজ করে?
উত্তর:
1. appsettings.json (base)
2. appsettings.{Environment}.json (override)
3. User Secrets (dev only, override)
4. Environment Variables (highest priority, override)
পরে load হওয়া same key-এর value আগেরটা override করে।

প্রশ্ন: FluentValidation কেন DataAnnotations-এর চেয়ে ভালো?
উত্তর:
DataAnnotations → Simple rules, attribute-based।
FluentValidation → Complex rules, async validation, dependency inject করা যায়।
                   DB check, conditional rules, unit testable।
Production complex validation → FluentValidation।

প্রশ্ন: Minimal API কখন ব্যবহার করবেন?
উত্তর:
Simple CRUD, microservice, small API → Minimal API।
Complex business logic, filters, multiple versioning → Controller।
.NET 8-এ দুটো একসাথেও ব্যবহার করা যায়।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 6 — Web API Development (REST Principles, HTTP Methods, Status Codes, API Versioning, Swagger/OpenAPI, Rate Limiting এবং আরও...)

---

<a id="part6"></a>
## PART 6: Web API Development

> REST Principles, HTTP Methods, Status Codes, Controllers, Response Shaping, API Versioning, Swagger/OpenAPI, CORS, Rate Limiting।

| # | বিষয় |
|---|-------|
| 1 | [REST Principles](#p6-rest) |
| 2 | [HTTP Methods ও Status Codes](#p6-http) |
| 3 | [Controller Best Practices](#p6-controller) |
| 4 | [Response Shaping ও DTOs](#p6-dto) |
| 5 | [API Versioning](#p6-versioning) |
| 6 | [Swagger / OpenAPI](#p6-swagger) |
| 7 | [CORS](#p6-cors) |
| 8 | [Rate Limiting](#p6-ratelimit) |
| 9 | [Health Checks](#p6-health) |
| 10 | [Global Error Handling](#p6-errors) |

---

<a id="p6-rest"></a>
### Topic 1: REST Principles

**REST (Representational State Transfer) — 6টি constraint:**

| Constraint | ব্যাখ্যা |
|------------|---------|
| **Client-Server** | UI এবং data logic আলাদা |
| **Stateless** | প্রতি request নিজেই complete — server session রাখে না |
| **Cacheable** | Response cacheable হলে indicate করতে হবে |
| **Uniform Interface** | Resource-based URL, HTTP methods |
| **Layered System** | Client জানে না কতটি layer আছে (proxy, LB, cache) |
| **Code on Demand** | Optional — server client code পাঠাতে পারে |

```
REST URL Design:
───────────────────────────────────────────────────
✅ Resource-based (noun, not verb)

GET    /api/orders          — list all orders
GET    /api/orders/5        — get order by id
POST   /api/orders          — create new order
PUT    /api/orders/5        — full update order 5
PATCH  /api/orders/5        — partial update order 5
DELETE /api/orders/5        — delete order 5

GET    /api/orders/5/items  — order 5-এর items
POST   /api/orders/5/items  — order 5-তে item add

❌ Verb-based (not REST)
GET /api/getOrder?id=5
POST /api/createOrder
POST /api/deleteOrder/5
GET /api/getAllActiveOrders
```

---

<a id="p6-http"></a>
### Topic 2: HTTP Methods ও Status Codes

```
HTTP Methods:
────────────────────────────────────────────────────
Method   | Safe? | Idempotent? | Body?  | Use
────────────────────────────────────────────────────
GET      |  ✅   |    ✅       |  ❌   | Read resource
HEAD     |  ✅   |    ✅       |  ❌   | Headers only (no body)
OPTIONS  |  ✅   |    ✅       |  ❌   | CORS preflight, capabilities
POST     |  ❌   |    ❌       |  ✅   | Create resource
PUT      |  ❌   |    ✅       |  ✅   | Full replace
PATCH    |  ❌   |    ❌       |  ✅   | Partial update
DELETE   |  ❌   |    ✅       |  ❌   | Delete resource
────────────────────────────────────────────────────
Safe = no side effects। Idempotent = same result multiple times।
```

```
HTTP Status Codes:
────────────────────────────────────────────────────
2xx Success:
200 OK              — GET, PUT, PATCH success
201 Created         — POST success (+ Location header)
204 No Content      — DELETE, PUT success (no body)

3xx Redirection:
301 Moved Permanently — permanent redirect
302 Found            — temporary redirect
304 Not Modified     — cached response still valid

4xx Client Error:
400 Bad Request      — invalid input, validation fail
401 Unauthorized     — not authenticated (no/bad token)
403 Forbidden        — authenticated but no permission
404 Not Found        — resource doesn't exist
405 Method Not Allowed — wrong HTTP method
409 Conflict         — duplicate, version conflict
422 Unprocessable    — validation error (semantic)
429 Too Many Requests — rate limit exceeded

5xx Server Error:
500 Internal Server Error — unexpected exception
502 Bad Gateway      — upstream server failed
503 Service Unavailable — overloaded/maintenance
────────────────────────────────────────────────────
```

```csharp
// ── Returning correct status codes ───────────────────
[ApiController]
[Route("api/v1/[controller]")]
public class OrdersController : ControllerBase
{
    private readonly IOrderService _service;
    public OrdersController(IOrderService service) => _service = service;

    // 200 OK
    [HttpGet]
    public async Task<ActionResult<PagedResult<OrderDto>>> GetAll(
        [FromQuery] int page = 1,
        [FromQuery] int pageSize = 20)
    {
        var result = await _service.GetPagedAsync(page, pageSize);
        return Ok(result);
    }

    // 200 OK or 404 Not Found
    [HttpGet("{id:int}")]
    public async Task<ActionResult<OrderDto>> GetById(int id)
    {
        var order = await _service.GetByIdAsync(id);
        return order is null ? NotFound() : Ok(order);
    }

    // 201 Created
    [HttpPost]
    public async Task<ActionResult<OrderDto>> Create([FromBody] CreateOrderDto dto)
    {
        var order = await _service.CreateAsync(dto);
        return CreatedAtAction(nameof(GetById), new { id = order.Id }, order);
        // Sets Location: /api/v1/orders/42
    }

    // 204 No Content or 404
    [HttpPut("{id:int}")]
    public async Task<IActionResult> Update(int id, [FromBody] UpdateOrderDto dto)
    {
        var updated = await _service.UpdateAsync(id, dto);
        return updated ? NoContent() : NotFound();
    }

    // 204 or 404
    [HttpDelete("{id:int}")]
    public async Task<IActionResult> Delete(int id)
    {
        var deleted = await _service.DeleteAsync(id);
        return deleted ? NoContent() : NotFound();
    }

    // 409 Conflict — duplicate
    [HttpPost("bulk")]
    public async Task<IActionResult> BulkCreate([FromBody] List<CreateOrderDto> dtos)
    {
        try
        {
            var result = await _service.BulkCreateAsync(dtos);
            return Ok(result);
        }
        catch (DuplicateOrderException ex)
        {
            return Conflict(new { message = ex.Message, duplicateId = ex.OrderId });
        }
    }
}
```

---

<a id="p6-controller"></a>
### Topic 3: Controller Best Practices

```csharp
// ── Thin controller — business logic service-এ ───────
// ❌ Fat controller — avoid!
[HttpPost]
public async Task<IActionResult> CreateBad([FromBody] CreateOrderDto dto)
{
    // Business logic in controller = bad!
    var customer = await _db.Customers.FindAsync(dto.CustomerId);
    if (customer is null) return BadRequest("Customer not found");
    var inventory = await _db.Products
        .Where(p => dto.Items.Select(i => i.ProductId).Contains(p.Id))
        .ToListAsync();
    foreach (var item in dto.Items)
    {
        var product = inventory.First(p => p.Id == item.ProductId);
        if (product.Stock < item.Quantity) return BadRequest($"Insufficient stock for {product.Name}");
        product.Stock -= item.Quantity;
    }
    var order = new Order { /* map */ };
    _db.Orders.Add(order);
    await _db.SaveChangesAsync();
    return CreatedAtAction(nameof(GetById), new { id = order.Id }, order);
}

// ✅ Thin controller — just orchestrate
[HttpPost]
public async Task<ActionResult<OrderDto>> Create([FromBody] CreateOrderDto dto)
{
    var order = await _orderService.CreateAsync(dto);
    return CreatedAtAction(nameof(GetById), new { id = order.Id }, order);
}

// ── ActionResult<T> — typed responses ────────────────
// ActionResult<T> allows both typed return and IActionResult
[HttpGet("{id:int}")]
public async Task<ActionResult<OrderDto>> GetById(int id)
{
    var order = await _service.GetByIdAsync(id);
    if (order is null) return NotFound();  // IActionResult
    return order;                          // implicit Ok(order)
}

// ── Async all the way ─────────────────────────────────
// ✅ Always use async Task for I/O operations
[HttpGet]
public async Task<ActionResult<IEnumerable<OrderDto>>> GetAll(
    CancellationToken ct) // ASP.NET Core injects this automatically
{
    var orders = await _service.GetAllAsync(ct);
    return Ok(orders);
}

// ── Pagination standard response ──────────────────────
[HttpGet]
public async Task<ActionResult<PagedResponse<OrderDto>>> GetPaged(
    [FromQuery] int page = 1,
    [FromQuery] int pageSize = 20)
{
    if (page < 1) return BadRequest("Page must be >= 1");
    if (pageSize is < 1 or > 100) return BadRequest("PageSize must be 1-100");

    var (items, total) = await _service.GetPagedAsync(page, pageSize);
    var response = new PagedResponse<OrderDto>
    {
        Data       = items,
        Page       = page,
        PageSize   = pageSize,
        TotalCount = total,
        TotalPages = (int)Math.Ceiling(total / (double)pageSize)
    };
    return Ok(response);
}

public class PagedResponse<T>
{
    public IEnumerable<T> Data   { get; set; } = Enumerable.Empty<T>();
    public int Page              { get; set; }
    public int PageSize          { get; set; }
    public int TotalCount        { get; set; }
    public int TotalPages        { get; set; }
    public bool HasNextPage      => Page < TotalPages;
    public bool HasPreviousPage  => Page > 1;
}
```

---

<a id="p6-dto"></a>
### Topic 4: Response Shaping ও DTOs

```csharp
// ── DTO pattern — never expose domain model directly ──
// Domain entity (never send to client!)
public class Order
{
    public int Id               { get; set; }
    public int CustomerId       { get; set; }
    public Customer Customer    { get; set; } = null!;
    public List<OrderItem> Items { get; set; } = new();
    public decimal TotalAmount  { get; set; }
    public string Status        { get; set; } = "";
    public DateTime CreatedAt   { get; set; }
    public string InternalNotes { get; set; } = ""; // sensitive!
    public bool IsDeleted       { get; set; }        // internal!
}

// Response DTO — what client sees
public record OrderDto(
    int    Id,
    string CustomerName,
    decimal TotalAmount,
    string Status,
    DateTime CreatedAt,
    IReadOnlyList<OrderItemDto> Items);

public record OrderItemDto(
    int    ProductId,
    string ProductName,
    int    Quantity,
    decimal UnitPrice,
    decimal LineTotal);

// Create DTO — what client sends
public record CreateOrderDto(
    int CustomerId,
    List<CreateOrderItemDto> Items,
    string? Notes);

public record CreateOrderItemDto(int ProductId, int Quantity);

// ── AutoMapper configuration ──────────────────────────
// Install: dotnet add package AutoMapper.Extensions.Microsoft.DependencyInjection
public class OrderMappingProfile : Profile
{
    public OrderMappingProfile()
    {
        CreateMap<Order, OrderDto>()
            .ForMember(dest => dest.CustomerName,
                       opt => opt.MapFrom(src => src.Customer.FullName));

        CreateMap<OrderItem, OrderItemDto>()
            .ForMember(dest => dest.ProductName,
                       opt => opt.MapFrom(src => src.Product.Name))
            .ForMember(dest => dest.LineTotal,
                       opt => opt.MapFrom(src => src.Quantity * src.UnitPrice));

        CreateMap<CreateOrderDto, Order>();
    }
}

builder.Services.AddAutoMapper(typeof(OrderMappingProfile));

// Usage in service:
public async Task<OrderDto> GetByIdAsync(int id)
{
    var order = await _db.Orders
        .Include(o => o.Customer)
        .Include(o => o.Items).ThenInclude(i => i.Product)
        .FirstOrDefaultAsync(o => o.Id == id)
        ?? throw new KeyNotFoundException();

    return _mapper.Map<OrderDto>(order);
}
```

---

<a id="p6-versioning"></a>
### Topic 5: API Versioning

```csharp
// Install: dotnet add package Asp.Versioning.Mvc

builder.Services.AddApiVersioning(options =>
{
    options.DefaultApiVersion = new ApiVersion(1, 0);
    options.AssumeDefaultVersionWhenUnspecified = true;
    options.ReportApiVersions = true; // adds API-Supported-Versions header
    options.ApiVersionReader = ApiVersionReader.Combine(
        new UrlSegmentApiVersionReader(),   // /api/v1/orders
        new HeaderApiVersionReader("X-Api-Version"), // header
        new QueryStringApiVersionReader("api-version") // ?api-version=1.0
    );
}).AddApiExplorer(options =>
{
    options.GroupNameFormat = "'v'VVV";
    options.SubstituteApiVersionInUrl = true;
});

// ── URL segment versioning ────────────────────────────
[ApiController]
[Route("api/v{version:apiVersion}/[controller]")]
[ApiVersion("1.0")]
public class OrdersV1Controller : ControllerBase
{
    [HttpGet]
    public IActionResult GetAll() => Ok(new { version = "v1", orders = Array.Empty<object>() });
}

[ApiController]
[Route("api/v{version:apiVersion}/[controller]")]
[ApiVersion("2.0")]
public class OrdersV2Controller : ControllerBase
{
    [HttpGet]
    public IActionResult GetAll() =>
        Ok(new { version = "v2", orders = Array.Empty<object>(), meta = new { pagination = true } });

    [HttpGet("{id:int}")]
    [MapToApiVersion("2.0")]
    public IActionResult GetById(int id) => Ok();
}

// ── Deprecating old versions ──────────────────────────
[ApiVersion("1.0", Deprecated = true)]
[ApiVersion("2.0")]
public class ProductsController : ControllerBase { /* ... */ }
```

---

<a id="p6-swagger"></a>
### Topic 6: Swagger / OpenAPI

```csharp
// Install: dotnet add package Swashbuckle.AspNetCore

builder.Services.AddEndpointsApiExplorer();
builder.Services.AddSwaggerGen(options =>
{
    options.SwaggerDoc("v1", new OpenApiInfo
    {
        Title       = "My API",
        Version     = "v1",
        Description = "Complete API documentation",
        Contact     = new OpenApiContact
        {
            Name  = "Dev Team",
            Email = "dev@example.com"
        }
    });

    // XML comments (enable in .csproj: <GenerateDocumentationFile>true</GenerateDocumentationFile>)
    var xml = Path.Combine(AppContext.BaseDirectory, $"{Assembly.GetExecutingAssembly().GetName().Name}.xml");
    options.IncludeXmlComments(xml);

    // JWT auth in Swagger UI
    options.AddSecurityDefinition("Bearer", new OpenApiSecurityScheme
    {
        Name         = "Authorization",
        Type         = SecuritySchemeType.Http,
        Scheme       = "Bearer",
        BearerFormat = "JWT",
        In           = ParameterLocation.Header,
        Description  = "Enter: Bearer {token}"
    });
    options.AddSecurityRequirement(new OpenApiSecurityRequirement
    {
        {
            new OpenApiSecurityScheme
            {
                Reference = new OpenApiReference
                    { Type = ReferenceType.SecurityScheme, Id = "Bearer" }
            },
            Array.Empty<string>()
        }
    });
});

// Middleware:
if (app.Environment.IsDevelopment())
{
    app.UseSwagger();
    app.UseSwaggerUI(c =>
    {
        c.SwaggerEndpoint("/swagger/v1/swagger.json", "My API v1");
        c.RoutePrefix = ""; // Swagger at root URL
    });
}

// ── XML Documentation comments ─────────────────────────
/// <summary>Get order by ID</summary>
/// <param name="id">Order ID (positive integer)</param>
/// <returns>Order details</returns>
/// <response code="200">Order found</response>
/// <response code="404">Order not found</response>
[HttpGet("{id:int}")]
[ProducesResponseType(typeof(OrderDto), StatusCodes.Status200OK)]
[ProducesResponseType(typeof(ProblemDetails), StatusCodes.Status404NotFound)]
public async Task<ActionResult<OrderDto>> GetById(int id) =>
    await _service.GetByIdAsync(id) is {} order ? Ok(order) : NotFound();
```

---

<a id="p6-cors"></a>
### Topic 7: CORS

```csharp
// CORS — Cross-Origin Resource Sharing
// Browser security: frontend (localhost:3000) → API (localhost:5000) blocked by default

builder.Services.AddCors(options =>
{
    // Development — allow all
    options.AddPolicy("Development", policy =>
        policy.AllowAnyOrigin()
              .AllowAnyMethod()
              .AllowAnyHeader());

    // Production — specific origins
    options.AddPolicy("Production", policy =>
        policy.WithOrigins(
                "https://myapp.com",
                "https://www.myapp.com",
                "https://admin.myapp.com")
              .WithMethods("GET", "POST", "PUT", "DELETE", "PATCH")
              .WithHeaders("Authorization", "Content-Type", "X-Api-Key")
              .AllowCredentials()  // cookies/auth headers
              .SetPreflightMaxAge(TimeSpan.FromMinutes(10))); // cache preflight
});

// Apply in pipeline (after UseRouting, before UseAuthorization)
app.UseCors(app.Environment.IsDevelopment() ? "Development" : "Production");

// ── Per-endpoint CORS ──────────────────────────────────
[HttpGet("public")]
[EnableCors("Development")]
public IActionResult PublicEndpoint() => Ok();

[HttpPost("internal")]
[DisableCors]
public IActionResult InternalEndpoint() => Ok();
```

---

<a id="p6-ratelimit"></a>
### Topic 8: Rate Limiting

```csharp
// .NET 7+ built-in rate limiting
using Microsoft.AspNetCore.RateLimiting;
using System.Threading.RateLimiting;

builder.Services.AddRateLimiter(options =>
{
    options.RejectionStatusCode = 429;

    // Fixed window — per window reset
    options.AddFixedWindowLimiter("fixed", opt =>
    {
        opt.Window            = TimeSpan.FromMinutes(1);
        opt.PermitLimit       = 100;
        opt.QueueProcessingOrder = QueueProcessingOrder.OldestFirst;
        opt.QueueLimit        = 10;
    });

    // Sliding window — smoother
    options.AddSlidingWindowLimiter("sliding", opt =>
    {
        opt.Window            = TimeSpan.FromMinutes(1);
        opt.SegmentsPerWindow = 6; // 10s segments
        opt.PermitLimit       = 100;
    });

    // Token bucket — burst-friendly
    options.AddTokenBucketLimiter("token", opt =>
    {
        opt.TokenLimit          = 100;
        opt.ReplenishmentPeriod = TimeSpan.FromSeconds(10);
        opt.TokensPerPeriod     = 20;
    });

    // Concurrency — simultaneous requests
    options.AddConcurrencyLimiter("concurrency", opt =>
    {
        opt.PermitLimit = 10;
        opt.QueueLimit  = 5;
    });

    // Per-user rate limiting
    options.AddPolicy("per-user", context =>
    {
        var userId = context.User.FindFirst("sub")?.Value ?? "anonymous";
        return RateLimitPartition.GetFixedWindowLimiter(userId, _ =>
            new FixedWindowRateLimiterOptions
            {
                Window      = TimeSpan.FromMinutes(1),
                PermitLimit = 60
            });
    });

    // On rejection — custom response
    options.OnRejected = async (context, ct) =>
    {
        context.HttpContext.Response.StatusCode = 429;
        if (context.Lease.TryGetMetadata(MetadataName.RetryAfter, out var retryAfter))
            context.HttpContext.Response.Headers["Retry-After"] =
                retryAfter.TotalSeconds.ToString();
        await context.HttpContext.Response.WriteAsync(
            "Rate limit exceeded. Try again later.", ct);
    };
});

app.UseRateLimiter(); // add to pipeline

// Apply to endpoints
app.MapControllers().RequireRateLimiting("per-user");

[HttpPost("upload")]
[EnableRateLimiting("concurrency")]
public IActionResult Upload([FromForm] IFormFile file) => Ok();

[HttpGet("public")]
[DisableRateLimiting]
public IActionResult Public() => Ok("No rate limiting here");
```

---

<a id="p6-health"></a>
### Topic 9: Health Checks

```csharp
// Install: dotnet add package AspNetCore.HealthChecks.SqlServer
//          dotnet add package AspNetCore.HealthChecks.Redis

builder.Services.AddHealthChecks()
    .AddSqlServer(
        connectionString: builder.Configuration.GetConnectionString("Default")!,
        name: "database",
        tags: new[] { "db", "sql" })
    .AddRedis(
        redisConnectionString: builder.Configuration["Redis:Connection"]!,
        name: "redis",
        tags: new[] { "cache" })
    .AddCheck("self", () => HealthCheckResult.Healthy(), tags: new[] { "live" });

// Map endpoints
app.MapHealthChecks("/health", new HealthCheckOptions
{
    ResponseWriter = UIResponseWriter.WriteHealthCheckUIResponse
});

app.MapHealthChecks("/health/live", new HealthCheckOptions
{
    Predicate = check => check.Tags.Contains("live")
});

app.MapHealthChecks("/health/ready", new HealthCheckOptions
{
    Predicate = check => check.Tags.Contains("db") || check.Tags.Contains("cache"),
    ResultStatusCodes =
    {
        [HealthStatus.Healthy]   = 200,
        [HealthStatus.Degraded]  = 200,
        [HealthStatus.Unhealthy] = 503
    }
});

// Custom health check
public class ExternalApiHealthCheck : IHealthCheck
{
    private readonly HttpClient _http;
    public ExternalApiHealthCheck(IHttpClientFactory factory) =>
        _http = factory.CreateClient();

    public async Task<HealthCheckResult> CheckHealthAsync(
        HealthCheckContext context,
        CancellationToken ct = default)
    {
        try
        {
            var response = await _http.GetAsync("https://api.external.com/ping", ct);
            return response.IsSuccessStatusCode
                ? HealthCheckResult.Healthy("External API reachable")
                : HealthCheckResult.Degraded($"External API returned {response.StatusCode}");
        }
        catch (Exception ex)
        {
            return HealthCheckResult.Unhealthy("External API unreachable", ex);
        }
    }
}

builder.Services.AddHealthChecks()
    .AddCheck<ExternalApiHealthCheck>("external-api");
```

---

<a id="p6-errors"></a>
### Topic 10: Global Error Handling

```csharp
// ── Exception handler middleware ──────────────────────
app.UseExceptionHandler(errorApp =>
{
    errorApp.Run(async context =>
    {
        var feature = context.Features.Get<IExceptionHandlerPathFeature>();
        var exception = feature?.Error;
        var logger = context.RequestServices
            .GetRequiredService<ILogger<Program>>();

        logger.LogError(exception, "Unhandled exception at {Path}", feature?.Path);

        var (status, title) = exception switch
        {
            KeyNotFoundException       => (404, "Resource not found"),
            UnauthorizedAccessException => (403, "Forbidden"),
            ArgumentException          => (400, "Bad request"),
            _                          => (500, "Internal server error")
        };

        context.Response.StatusCode = status;
        context.Response.ContentType = "application/problem+json";
        var problem = new ProblemDetails
        {
            Status = status,
            Title  = title,
            Detail = exception?.Message,
            Instance = context.Request.Path
        };
        await context.Response.WriteAsJsonAsync(problem);
    });
});

// ── IExceptionHandler (.NET 8+) — clean separation ────
public class GlobalExceptionHandler : IExceptionHandler
{
    private readonly ILogger<GlobalExceptionHandler> _logger;
    public GlobalExceptionHandler(ILogger<GlobalExceptionHandler> logger) =>
        _logger = logger;

    public async ValueTask<bool> TryHandleAsync(
        HttpContext context,
        Exception exception,
        CancellationToken ct)
    {
        _logger.LogError(exception, "Unhandled exception");

        var (status, title) = exception switch
        {
            KeyNotFoundException       => (404, "Not Found"),
            ValidationException ve     => (400, ve.Message),
            UnauthorizedAccessException => (403, "Forbidden"),
            _                          => (500, "Internal Server Error")
        };

        context.Response.StatusCode = status;
        await context.Response.WriteAsJsonAsync(
            new ProblemDetails { Status = status, Title = title, Detail = exception.Message },
            ct);

        return true; // handled
    }
}

builder.Services.AddExceptionHandler<GlobalExceptionHandler>();
builder.Services.AddProblemDetails();
app.UseExceptionHandler();
```

---

## PART 6 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| REST | Resource-based URL, stateless, HTTP methods |
| GET | Read — safe, idempotent |
| POST | Create — not idempotent → 201 Created |
| PUT | Full replace — idempotent → 204 No Content |
| PATCH | Partial update → 204 |
| DELETE | Delete — idempotent → 204 |
| 400 | Bad Request — validation fail |
| 401 | Unauthorized — not authenticated |
| 403 | Forbidden — no permission |
| 404 | Not Found |
| 409 | Conflict — duplicate |
| 429 | Too Many Requests — rate limit |
| DTO | Domain model expose করবেন না |
| `CreatedAtAction` | 201 + Location header |
| `ActionResult<T>` | Typed return + IActionResult |
| API Versioning | URL segment `/v1/`, header, query string |
| Swagger | OpenAPI spec, XML comments, ProducesResponseType |
| CORS | Cross-origin browser policy — WithOrigins |
| Rate Limiting | Fixed/Sliding Window, Token Bucket, per-user |
| Health Check | /health, /health/live, /health/ready |
| IExceptionHandler | .NET 8+ global error handler |
| Problem Details | RFC 7807 standard error format |

---

## PART 6 Interview Q&A

```
প্রশ্ন: PUT আর PATCH পার্থক্য?
উত্তর:
PUT → পুরো resource replace করে। সব fields পাঠাতে হবে।
      Missing fields → null/default হয়ে যায়।
PATCH → শুধু changed fields পাঠান। Partial update।
        PUT idempotent। PATCH generally not idempotent।

প্রশ্ন: 401 আর 403 পার্থক্য?
উত্তর:
401 Unauthorized → "আপনি কে?" — token নেই বা invalid।
                   Login করুন।
403 Forbidden → "আমি জানি আপনি কে, কিন্তু আপনার permission নেই।"
                Admin resource normal user hit করলে।

প্রশ্ন: API Versioning কেন দরকার?
উত্তর: Breaking changes করলে existing clients break হয়।
Version করলে পুরনো clients /v1/ ব্যবহার করতে পারে,
নতুন clients /v2/ তে migrate করতে পারে।
URL versioning সবচেয়ে visible এবং cacheable।

প্রশ্ন: CORS কী এবং কীভাবে handle করে?
উত্তর: Browser same-origin policy enforce করে।
Frontend (port 3000) → API (port 5000) — different origin।
Server WithOrigins() দিয়ে allowed origins declare করে।
Browser preflight OPTIONS request পাঠায়।
Server Access-Control-Allow-Origin header দিয়ে response দেয়।
CORS server-side security নয় — browser enforcement।

প্রশ্ন: Rate limiting কেন দরকার?
উত্তর: DoS/DDoS protection। Resource overuse prevent।
API abuse prevent। Fair usage enforce।
Fixed Window → simple কিন্তু window edge-এ burst।
Token Bucket → burst allow করে, সবচেয়ে flexible।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 7 — Database ও Entity Framework Core (EF Core Setup, Migrations, LINQ Queries, Relationships, Performance Optimization এবং আরও...)

---

<a id="part7"></a>
## PART 7: Database ও Entity Framework Core

> EF Core Setup, DbContext, Migrations, CRUD Operations, Relationships, LINQ Queries, Performance Optimization, Transactions, Dapper।

| # | বিষয় |
|---|-------|
| 1 | [EF Core Setup ও DbContext](#p7-setup) |
| 2 | [Migrations](#p7-migrations) |
| 3 | [CRUD Operations](#p7-crud) |
| 4 | [Relationships (1:1, 1:N, M:N)](#p7-relationships) |
| 5 | [LINQ Queries ও Loading Strategies](#p7-queries) |
| 6 | [Change Tracking](#p7-tracking) |
| 7 | [Transactions](#p7-transactions) |
| 8 | [Performance Optimization](#p7-performance) |
| 9 | [Raw SQL ও Dapper](#p7-rawsql) |
| 10 | [Repository Pattern with EF Core](#p7-repository) |

---

<a id="p7-setup"></a>
### Topic 1: EF Core Setup ও DbContext

```csharp
// Install:
// dotnet add package Microsoft.EntityFrameworkCore.SqlServer
// dotnet add package Microsoft.EntityFrameworkCore.Tools

// ── Entity models ─────────────────────────────────────
public class Customer
{
    public int    Id        { get; set; }
    public string FullName  { get; set; } = "";
    public string Email     { get; set; } = "";
    public string Phone     { get; set; } = "";
    public bool   IsActive  { get; set; } = true;
    public DateTime CreatedAt { get; set; }

    // Navigation properties
    public List<Order> Orders { get; set; } = new();
}

public class Order
{
    public int      Id         { get; set; }
    public int      CustomerId { get; set; }
    public decimal  TotalAmount { get; set; }
    public string   Status     { get; set; } = "Pending";
    public DateTime OrderDate  { get; set; }

    // Navigation properties
    public Customer        Customer { get; set; } = null!;
    public List<OrderItem> Items    { get; set; } = new();
}

public class OrderItem
{
    public int     Id        { get; set; }
    public int     OrderId   { get; set; }
    public int     ProductId { get; set; }
    public int     Quantity  { get; set; }
    public decimal UnitPrice { get; set; }

    public Order   Order   { get; set; } = null!;
    public Product Product { get; set; } = null!;
}

public class Product
{
    public int     Id       { get; set; }
    public string  Name     { get; set; } = "";
    public decimal Price    { get; set; }
    public int     Stock    { get; set; }
    public int     CategoryId { get; set; }
    public Category Category { get; set; } = null!;
}

// ── DbContext ─────────────────────────────────────────
public class AppDbContext : DbContext
{
    public AppDbContext(DbContextOptions<AppDbContext> options) : base(options) { }

    public DbSet<Customer>  Customers  { get; set; }
    public DbSet<Order>     Orders     { get; set; }
    public DbSet<OrderItem> OrderItems { get; set; }
    public DbSet<Product>   Products   { get; set; }
    public DbSet<Category>  Categories { get; set; }

    protected override void OnModelCreating(ModelBuilder modelBuilder)
    {
        // Apply all entity configurations from assembly
        modelBuilder.ApplyConfigurationsFromAssembly(typeof(AppDbContext).Assembly);

        // Soft delete global filter
        modelBuilder.Entity<Customer>()
            .HasQueryFilter(c => !c.IsDeleted);

        base.OnModelCreating(modelBuilder);
    }

    // Audit: auto-set CreatedAt/UpdatedAt
    public override Task<int> SaveChangesAsync(CancellationToken ct = default)
    {
        foreach (var entry in ChangeTracker.Entries<IAuditableEntity>())
        {
            if (entry.State == EntityState.Added)
                entry.Entity.CreatedAt = DateTime.UtcNow;
            if (entry.State is EntityState.Added or EntityState.Modified)
                entry.Entity.UpdatedAt = DateTime.UtcNow;
        }
        return base.SaveChangesAsync(ct);
    }
}

// ── Fluent API Configuration ──────────────────────────
public class OrderConfiguration : IEntityTypeConfiguration<Order>
{
    public void Configure(EntityTypeBuilder<Order> builder)
    {
        builder.ToTable("Orders");
        builder.HasKey(o => o.Id);

        builder.Property(o => o.Status)
            .HasMaxLength(20)
            .HasDefaultValue("Pending")
            .IsRequired();

        builder.Property(o => o.TotalAmount)
            .HasColumnType("decimal(18,2)");

        builder.HasOne(o => o.Customer)
            .WithMany(c => c.Orders)
            .HasForeignKey(o => o.CustomerId)
            .OnDelete(DeleteBehavior.Restrict);

        builder.HasIndex(o => o.CustomerId);
        builder.HasIndex(o => new { o.Status, o.OrderDate });
    }
}

// ── Registration ──────────────────────────────────────
builder.Services.AddDbContext<AppDbContext>(options =>
    options.UseSqlServer(
        builder.Configuration.GetConnectionString("Default"),
        sqlOptions =>
        {
            sqlOptions.EnableRetryOnFailure(
                maxRetryCount: 3,
                maxRetryDelay: TimeSpan.FromSeconds(5),
                errorNumbersToAdd: null);
            sqlOptions.CommandTimeout(30);
        })
    .EnableSensitiveDataLogging(builder.Environment.IsDevelopment())
    .LogTo(Console.WriteLine, LogLevel.Information));
```

---

<a id="p7-migrations"></a>
### Topic 2: Migrations

```bash
# ── Common EF Core CLI commands ────────────────────────

# Migration create করুন
dotnet ef migrations add InitialCreate

# Migration apply করুন (DB update)
dotnet ef database update

# Specific migration পর্যন্ত update
dotnet ef database update AddOrderIndex

# Migration rollback (one step)
dotnet ef database update PreviousMigrationName

# Migration SQL script generate (production use)
dotnet ef migrations script --output migration.sql

# Migration remove (last unapplied)
dotnet ef migrations remove

# DbContext list
dotnet ef dbcontext list

# DbContext info
dotnet ef dbcontext info
```

```csharp
// ── Programmatic migration (startup) ─────────────────
// Production-এ startup migration apply
app.Services.CreateScope().ServiceProvider
    .GetRequiredService<AppDbContext>()
    .Database.MigrateAsync()
    .GetAwaiter().GetResult();

// ── Data seeding ──────────────────────────────────────
protected override void OnModelCreating(ModelBuilder modelBuilder)
{
    modelBuilder.Entity<Category>().HasData(
        new Category { Id = 1, Name = "Electronics" },
        new Category { Id = 2, Name = "Clothing" },
        new Category { Id = 3, Name = "Books" }
    );
}

// ── Custom migration ──────────────────────────────────
public partial class AddFullTextSearch : Migration
{
    protected override void Up(MigrationBuilder migrationBuilder)
    {
        migrationBuilder.Sql(
            "CREATE FULLTEXT INDEX ON Products(Name, Description) KEY INDEX PK_Products");
    }

    protected override void Down(MigrationBuilder migrationBuilder)
    {
        migrationBuilder.Sql("DROP FULLTEXT INDEX ON Products");
    }
}
```

---

<a id="p7-crud"></a>
### Topic 3: CRUD Operations

```csharp
public class OrderService
{
    private readonly AppDbContext _db;
    public OrderService(AppDbContext db) => _db = db;

    // ── Create ────────────────────────────────────────
    public async Task<Order> CreateAsync(CreateOrderDto dto, CancellationToken ct = default)
    {
        var order = new Order
        {
            CustomerId = dto.CustomerId,
            OrderDate  = DateTime.UtcNow,
            Status     = "Pending",
            Items = dto.Items.Select(i => new OrderItem
            {
                ProductId = i.ProductId,
                Quantity  = i.Quantity,
                UnitPrice = i.UnitPrice
            }).ToList()
        };

        order.TotalAmount = order.Items.Sum(i => i.Quantity * i.UnitPrice);

        _db.Orders.Add(order);
        await _db.SaveChangesAsync(ct);
        return order;
    }

    // ── Read ──────────────────────────────────────────
    public async Task<Order?> GetByIdAsync(int id, CancellationToken ct = default) =>
        await _db.Orders
            .Include(o => o.Customer)
            .Include(o => o.Items).ThenInclude(i => i.Product)
            .FirstOrDefaultAsync(o => o.Id == id, ct);

    public async Task<List<Order>> GetByCustomerAsync(int customerId, CancellationToken ct = default) =>
        await _db.Orders
            .Where(o => o.CustomerId == customerId)
            .OrderByDescending(o => o.OrderDate)
            .AsNoTracking()  // read-only — faster!
            .ToListAsync(ct);

    // ── Update ────────────────────────────────────────
    public async Task<bool> UpdateStatusAsync(int id, string status, CancellationToken ct = default)
    {
        var order = await _db.Orders.FindAsync(new object[] { id }, ct);
        if (order is null) return false;

        order.Status = status;
        await _db.SaveChangesAsync(ct);
        return true;
    }

    // ── Bulk update (ExecuteUpdateAsync — EF Core 7+) ─
    public async Task<int> BulkCancelPendingAsync(DateTime before, CancellationToken ct = default) =>
        await _db.Orders
            .Where(o => o.Status == "Pending" && o.OrderDate < before)
            .ExecuteUpdateAsync(setter =>
                setter.SetProperty(o => o.Status, "Cancelled"),
            ct);
    // No entity load — direct SQL UPDATE!

    // ── Delete ────────────────────────────────────────
    public async Task<bool> DeleteAsync(int id, CancellationToken ct = default)
    {
        var order = await _db.Orders.FindAsync(new object[] { id }, ct);
        if (order is null) return false;

        _db.Orders.Remove(order);
        await _db.SaveChangesAsync(ct);
        return true;
    }

    // ── Bulk delete (ExecuteDeleteAsync — EF Core 7+) ─
    public async Task<int> DeleteOldOrdersAsync(DateTime before, CancellationToken ct = default) =>
        await _db.Orders
            .Where(o => o.Status == "Cancelled" && o.OrderDate < before)
            .ExecuteDeleteAsync(ct);
    // Direct SQL DELETE — no entity load!
}
```

---

<a id="p7-relationships"></a>
### Topic 4: Relationships

```csharp
// ── One-to-Many (সবচেয়ে সাধারণ) ─────────────────────
// Customer → Orders (1 customer has many orders)
public class Customer
{
    public int Id { get; set; }
    public List<Order> Orders { get; set; } = new(); // collection nav
}
public class Order
{
    public int CustomerId { get; set; }       // FK
    public Customer Customer { get; set; } = null!; // reference nav
}

// Fluent config:
builder.HasOne(o => o.Customer)
    .WithMany(c => c.Orders)
    .HasForeignKey(o => o.CustomerId)
    .OnDelete(DeleteBehavior.Restrict); // don't cascade delete

// ── One-to-One ────────────────────────────────────────
public class User
{
    public int Id { get; set; }
    public UserProfile? Profile { get; set; }
}
public class UserProfile
{
    public int UserId { get; set; } // PK = FK
    public User User  { get; set; } = null!;
    public string Bio { get; set; } = "";
}

builder.Entity<UserProfile>()
    .HasOne(p => p.User)
    .WithOne(u => u.Profile)
    .HasForeignKey<UserProfile>(p => p.UserId);

// ── Many-to-Many (EF Core 5+) ─────────────────────────
// Product ↔ Tag (many-to-many with join table)
public class Product
{
    public int Id { get; set; }
    public List<Tag> Tags { get; set; } = new();
}
public class Tag
{
    public int Id { get; set; }
    public List<Product> Products { get; set; } = new();
}

// EF Core 5+ auto join table (no explicit join entity needed):
modelBuilder.Entity<Product>()
    .HasMany(p => p.Tags)
    .WithMany(t => t.Products)
    .UsingEntity(j => j.ToTable("ProductTags"));

// ── Many-to-Many with payload (explicit join entity) ──
public class StudentCourse
{
    public int StudentId  { get; set; }
    public int CourseId   { get; set; }
    public DateTime EnrolledAt { get; set; }
    public string? Grade  { get; set; }

    public Student Student { get; set; } = null!;
    public Course  Course  { get; set; } = null!;
}

modelBuilder.Entity<StudentCourse>()
    .HasKey(sc => new { sc.StudentId, sc.CourseId }); // composite PK

modelBuilder.Entity<StudentCourse>()
    .HasOne(sc => sc.Student)
    .WithMany(s => s.Courses)
    .HasForeignKey(sc => sc.StudentId);

modelBuilder.Entity<StudentCourse>()
    .HasOne(sc => sc.Course)
    .WithMany(c => c.Students)
    .HasForeignKey(sc => sc.CourseId);
```

---

<a id="p7-queries"></a>
### Topic 5: LINQ Queries ও Loading Strategies

```csharp
// ── Loading strategies ────────────────────────────────

// 1. Eager Loading — Include দিয়ে একসাথে load
var orders = await _db.Orders
    .Include(o => o.Customer)
    .Include(o => o.Items)
        .ThenInclude(i => i.Product)
            .ThenInclude(p => p.Category)
    .Where(o => o.Status == "Pending")
    .ToListAsync();

// 2. Explicit Loading — পরে চাওয়ার সময় load
var order = await _db.Orders.FindAsync(id);
await _db.Entry(order).Reference(o => o.Customer).LoadAsync();
await _db.Entry(order).Collection(o => o.Items).LoadAsync();

// 3. Lazy Loading — access করলে auto load (avoid in API!)
// dotnet add package Microsoft.EntityFrameworkCore.Proxies
// options.UseLazyLoadingProxies() — N+1 problem risk!

// ── Projection — Select করুন শুধু দরকারি fields ────────
var summaries = await _db.Orders
    .Where(o => o.CustomerId == customerId)
    .Select(o => new OrderSummaryDto
    {
        Id         = o.Id,
        OrderDate  = o.OrderDate,
        TotalAmount = o.TotalAmount,
        Status     = o.Status,
        ItemCount  = o.Items.Count  // EF translates to COUNT(*)
    })
    .OrderByDescending(o => o.OrderDate)
    .ToListAsync();

// ── Filtered Include (EF Core 5+) ─────────────────────
var customers = await _db.Customers
    .Include(c => c.Orders.Where(o => o.Status == "Pending")
                          .OrderByDescending(o => o.OrderDate)
                          .Take(5))
    .ToListAsync();

// ── Compiled queries — repeated query performance ─────
private static readonly Func<AppDbContext, int, Task<Order?>> GetOrderById =
    EF.CompileAsyncQuery((AppDbContext db, int id) =>
        db.Orders.Include(o => o.Customer).FirstOrDefault(o => o.Id == id));

// Usage — skips query compilation overhead
var order = await GetOrderById(_db, 42);

// ── Split query — avoid cartesian explosion ───────────
// Large Include chains → JOIN produces many rows
var orders = await _db.Orders
    .Include(o => o.Items)
    .Include(o => o.Tags)
    .AsSplitQuery()  // 3 separate SQL queries instead of 1 huge JOIN
    .ToListAsync();

// Global split query:
options.UseQuerySplittingBehavior(QuerySplittingBehavior.SplitQuery)
```

---

<a id="p7-tracking"></a>
### Topic 6: Change Tracking

```csharp
// EF Core tracks entity changes — Added, Modified, Deleted, Unchanged

// ── AsNoTracking — read-only queries ─────────────────
// No snapshot, no tracking → faster!
var products = await _db.Products
    .AsNoTracking()
    .Where(p => p.IsActive)
    .ToListAsync();

// ── AsNoTrackingWithIdentityResolution (EF Core 5+) ───
// AsNoTracking but handles duplicate entities in graph
var orders = await _db.Orders
    .Include(o => o.Items).ThenInclude(i => i.Product)
    .AsNoTrackingWithIdentityResolution()
    .ToListAsync();

// ── Tracking state management ─────────────────────────
var order = new Order { Id = 5, Status = "Shipped" };

// Attach — tell EF this entity exists (but we loaded it outside)
_db.Attach(order);
_db.Entry(order).Property(o => o.Status).IsModified = true;
await _db.SaveChangesAsync(); // only updates Status column

// Entry state
var entry = _db.Entry(order);
Console.WriteLine(entry.State); // EntityState.Unchanged/Modified/Added/Deleted

// Detach
_db.Entry(order).State = EntityState.Detached;
```

---

<a id="p7-transactions"></a>
### Topic 7: Transactions

```csharp
// ── Implicit transaction — SaveChanges-এ auto ─────────
// সব changes একটি transaction-এ
_db.Orders.Add(order);
_db.Inventory.Update(inventory);
await _db.SaveChangesAsync(); // ✅ atomic

// ── Explicit transaction — multiple SaveChanges ────────
await using var transaction = await _db.Database.BeginTransactionAsync();
try
{
    // Step 1
    var order = new Order { /* ... */ };
    _db.Orders.Add(order);
    await _db.SaveChangesAsync();

    // Step 2 — needs order.Id from step 1
    await _paymentService.ProcessAsync(order.Id, dto.Amount);

    // Step 3
    order.Status = "Paid";
    await _db.SaveChangesAsync();

    await transaction.CommitAsync();
}
catch
{
    await transaction.RollbackAsync();
    throw;
}

// ── Savepoints (EF Core 5+) ───────────────────────────
await using var transaction = await _db.Database.BeginTransactionAsync();

await _db.Orders.AddAsync(order);
await _db.SaveChangesAsync();

await transaction.CreateSavepointAsync("OrderCreated");

try
{
    await _db.Notifications.AddAsync(notification);
    await _db.SaveChangesAsync();
}
catch
{
    await transaction.RollbackToSavepointAsync("OrderCreated");
    // order still saved, notification rolled back
}

await transaction.CommitAsync();

// ── Optimistic concurrency ────────────────────────────
public class Product
{
    public int    Id     { get; set; }
    public int    Stock  { get; set; }
    [Timestamp]
    public byte[] RowVersion { get; set; } = null!; // concurrency token
}

try
{
    var product = await _db.Products.FindAsync(id);
    product.Stock -= quantity;
    await _db.SaveChangesAsync();
}
catch (DbUpdateConcurrencyException)
{
    // Another user updated the same record — handle conflict
    // Reload and retry, or return 409 Conflict
}
```

---

<a id="p7-performance"></a>
### Topic 8: Performance Optimization

```csharp
// ── 1. AsNoTracking for read-only ─────────────────────
var list = await _db.Products.AsNoTracking().ToListAsync();

// ── 2. Select only needed columns ─────────────────────
// ❌ loads all columns
var products = await _db.Products.ToListAsync();

// ✅ loads only needed
var names = await _db.Products
    .Select(p => new { p.Id, p.Name, p.Price })
    .ToListAsync();

// ── 3. Avoid N+1 — use Include ────────────────────────
// ❌ N+1 — 1 query for orders + N queries for customers
var orders = await _db.Orders.ToListAsync();
foreach (var o in orders)
    Console.WriteLine(o.Customer.FullName); // lazy load = N queries!

// ✅ 1 query with JOIN
var orders = await _db.Orders.Include(o => o.Customer).ToListAsync();

// ── 4. Bulk operations — ExecuteUpdate/Delete (EF7+) ──
// ❌ loads all, updates one by one
var products = await _db.Products.Where(p => p.Stock == 0).ToListAsync();
foreach (var p in products) p.IsActive = false;
await _db.SaveChangesAsync(); // N UPDATE statements

// ✅ single SQL UPDATE
await _db.Products
    .Where(p => p.Stock == 0)
    .ExecuteUpdateAsync(s => s.SetProperty(p => p.IsActive, false));

// ── 5. Pagination ─────────────────────────────────────
// ❌ loads everything into memory first
var all = await _db.Orders.ToListAsync();
var page = all.Skip(20).Take(10);

// ✅ OFFSET FETCH in SQL
var page = await _db.Orders
    .OrderByDescending(o => o.OrderDate)
    .Skip((pageNumber - 1) * pageSize)
    .Take(pageSize)
    .ToListAsync();

// ── 6. Indexes ────────────────────────────────────────
protected override void OnModelCreating(ModelBuilder builder)
{
    builder.Entity<Order>()
        .HasIndex(o => o.CustomerId);

    builder.Entity<Order>()
        .HasIndex(o => new { o.Status, o.OrderDate })
        .HasFilter("Status <> 'Completed'"); // partial index

    builder.Entity<Product>()
        .HasIndex(p => p.Name)
        .IsUnique();
}

// ── 7. Compiled queries ────────────────────────────────
private static readonly Func<AppDbContext, string, IAsyncEnumerable<Product>>
    GetProductsByCategory =
        EF.CompileAsyncQuery((AppDbContext db, string category) =>
            db.Products
                .Where(p => p.Category.Name == category && p.IsActive)
                .AsNoTracking());

// ── 8. Connection pooling — default enabled ────────────
// DbContext Scoped → reused per request
// Don't use Singleton DbContext!

// ── 9. Second-level caching ────────────────────────────
// Cache frequently read, rarely changed data
public async Task<List<Category>> GetCategoriesAsync()
{
    const string key = "all-categories";
    if (_cache.TryGetValue(key, out List<Category>? cached))
        return cached!;

    var categories = await _db.Categories.AsNoTracking().ToListAsync();
    _cache.Set(key, categories, TimeSpan.FromMinutes(10));
    return categories;
}
```

---

<a id="p7-rawsql"></a>
### Topic 9: Raw SQL ও Dapper

```csharp
// ── EF Core Raw SQL ───────────────────────────────────
// FromSqlRaw — tracked entities
var orders = await _db.Orders
    .FromSqlRaw("SELECT * FROM Orders WHERE CustomerId = {0}", customerId)
    .Include(o => o.Customer)
    .ToListAsync();

// FromSqlInterpolated — parameterized (SQL injection safe!)
var orders2 = await _db.Orders
    .FromSqlInterpolated($"SELECT * FROM Orders WHERE CustomerId = {customerId}")
    .ToListAsync();

// ExecuteSqlRawAsync — non-query (UPDATE, DELETE, stored procedures)
await _db.Database.ExecuteSqlRawAsync(
    "UPDATE Products SET Stock = Stock - {0} WHERE Id = {1}",
    quantity, productId);

// ── Dapper — micro-ORM, raw SQL-এর জন্য সেরা ─────────
// dotnet add package Dapper

public class OrderReportService
{
    private readonly IDbConnection _db;
    public OrderReportService(IDbConnection db) => _db = db;

    // Simple query
    public async Task<IEnumerable<OrderDto>> GetByCustomerAsync(int customerId) =>
        await _db.QueryAsync<OrderDto>(
            "SELECT Id, TotalAmount, Status, OrderDate FROM Orders WHERE CustomerId = @CustomerId",
            new { CustomerId = customerId });

    // Multi-map — JOIN two tables
    public async Task<IEnumerable<OrderWithCustomer>> GetOrdersWithCustomerAsync()
    {
        const string sql = @"
            SELECT o.Id, o.TotalAmount, o.Status,
                   c.Id, c.FullName, c.Email
            FROM Orders o
            INNER JOIN Customers c ON o.CustomerId = c.Id";

        return await _db.QueryAsync<Order, Customer, OrderWithCustomer>(
            sql,
            (order, customer) => { order.Customer = customer; return order; },
            splitOn: "Id");
    }

    // Stored procedure
    public async Task<SalesReport> GetSalesReportAsync(DateTime from, DateTime to) =>
        await _db.QueryFirstOrDefaultAsync<SalesReport>(
            "sp_GetSalesReport",
            new { FromDate = from, ToDate = to },
            commandType: CommandType.StoredProcedure)
        ?? throw new InvalidOperationException("Report not available");

    // Scalar
    public async Task<int> GetOrderCountAsync(int customerId) =>
        await _db.ExecuteScalarAsync<int>(
            "SELECT COUNT(*) FROM Orders WHERE CustomerId = @Id",
            new { Id = customerId });
}

// Register IDbConnection
builder.Services.AddScoped<IDbConnection>(_ =>
    new SqlConnection(builder.Configuration.GetConnectionString("Default")));
```

---

<a id="p7-repository"></a>
### Topic 10: Repository Pattern with EF Core

```csharp
// ── Generic Repository ────────────────────────────────
public interface IRepository<T> where T : class
{
    Task<T?> GetByIdAsync(int id, CancellationToken ct = default);
    Task<IReadOnlyList<T>> GetAllAsync(CancellationToken ct = default);
    Task<IReadOnlyList<T>> FindAsync(Expression<Func<T, bool>> predicate, CancellationToken ct = default);
    Task AddAsync(T entity, CancellationToken ct = default);
    void Update(T entity);
    void Delete(T entity);
}

public class Repository<T> : IRepository<T> where T : class
{
    protected readonly AppDbContext _db;
    public Repository(AppDbContext db) => _db = db;

    public Task<T?> GetByIdAsync(int id, CancellationToken ct) =>
        _db.Set<T>().FindAsync(new object[] { id }, ct).AsTask();

    public Task<IReadOnlyList<T>> GetAllAsync(CancellationToken ct) =>
        _db.Set<T>().AsNoTracking().ToListAsync(ct)
            .ContinueWith(t => (IReadOnlyList<T>)t.Result);

    public async Task<IReadOnlyList<T>> FindAsync(
        Expression<Func<T, bool>> predicate, CancellationToken ct)
    {
        return await _db.Set<T>().AsNoTracking().Where(predicate).ToListAsync(ct);
    }

    public async Task AddAsync(T entity, CancellationToken ct) =>
        await _db.Set<T>().AddAsync(entity, ct);

    public void Update(T entity) => _db.Set<T>().Update(entity);
    public void Delete(T entity) => _db.Set<T>().Remove(entity);
}

// ── Specific repository ───────────────────────────────
public interface IOrderRepository : IRepository<Order>
{
    Task<Order?> GetWithDetailsAsync(int id, CancellationToken ct = default);
    Task<PagedResult<Order>> GetPagedByCustomerAsync(
        int customerId, int page, int pageSize, CancellationToken ct = default);
}

public class OrderRepository : Repository<Order>, IOrderRepository
{
    public OrderRepository(AppDbContext db) : base(db) { }

    public Task<Order?> GetWithDetailsAsync(int id, CancellationToken ct) =>
        _db.Orders
            .Include(o => o.Customer)
            .Include(o => o.Items).ThenInclude(i => i.Product)
            .AsNoTracking()
            .FirstOrDefaultAsync(o => o.Id == id, ct);

    public async Task<PagedResult<Order>> GetPagedByCustomerAsync(
        int customerId, int page, int pageSize, CancellationToken ct)
    {
        var query = _db.Orders
            .Where(o => o.CustomerId == customerId)
            .OrderByDescending(o => o.OrderDate);

        var total = await query.CountAsync(ct);
        var items = await query.Skip((page - 1) * pageSize).Take(pageSize)
            .AsNoTracking().ToListAsync(ct);

        return new PagedResult<Order>(items, total, page, pageSize);
    }
}

// ── Unit of Work ──────────────────────────────────────
public interface IUnitOfWork : IAsyncDisposable
{
    IOrderRepository Orders { get; }
    IRepository<Customer> Customers { get; }
    IRepository<Product> Products { get; }
    Task<int> SaveChangesAsync(CancellationToken ct = default);
}

public class UnitOfWork : IUnitOfWork
{
    private readonly AppDbContext _db;
    public IOrderRepository     Orders    { get; }
    public IRepository<Customer> Customers { get; }
    public IRepository<Product>  Products  { get; }

    public UnitOfWork(AppDbContext db)
    {
        _db = db;
        Orders    = new OrderRepository(db);
        Customers = new Repository<Customer>(db);
        Products  = new Repository<Product>(db);
    }

    public Task<int> SaveChangesAsync(CancellationToken ct) =>
        _db.SaveChangesAsync(ct);

    public ValueTask DisposeAsync() => _db.DisposeAsync();
}

// Register:
builder.Services.AddScoped<IUnitOfWork, UnitOfWork>();
```

---

## PART 7 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| DbContext | EF Core-এর unit of work — DB connection |
| DbSet\<T\> | Entity table representation |
| Fluent API | `OnModelCreating` → table, columns, relations configure |
| Data Annotations | `[Key]`, `[Required]`, `[MaxLength]` |
| Migration | Code → Database schema change |
| `dotnet ef migrations add` | New migration create |
| `dotnet ef database update` | Apply migrations |
| Include | Eager loading — related data |
| ThenInclude | Nested eager loading |
| AsNoTracking | Read-only → faster, no snapshot |
| Lazy Loading | Access করলে auto load → N+1 risk |
| N+1 Problem | Loop-এ per-entity query → use Include |
| ExecuteUpdateAsync | Load ছাড়া bulk UPDATE (EF7+) |
| ExecuteDeleteAsync | Load ছাড়া bulk DELETE (EF7+) |
| AsSplitQuery | Multiple queries instead of cartesian JOIN |
| Compiled Query | EF.CompileAsyncQuery — repeated use optimization |
| Transaction | `BeginTransactionAsync`, Commit, Rollback |
| Optimistic Concurrency | `[Timestamp]` / RowVersion |
| Savepoint | Transaction-এর মধ্যে partial rollback |
| Dapper | Micro-ORM — raw SQL, fast, stored procedures |
| Repository Pattern | Data access abstraction |
| Unit of Work | Multiple repos, single SaveChanges |
| Global Query Filter | `HasQueryFilter` — soft delete |
| Index | `HasIndex` — query performance |

---

## PART 7 Interview Q&A

```
প্রশ্ন: EF Core আর Dapper কোনটা কখন?

উত্তর:
EF Core → Complex domain model, migrations, LINQ, change tracking।
          CRUD-heavy applications।
Dapper → Performance-critical, complex reporting queries।
          Stored procedures। Raw SQL control দরকার।
          বেশিরভাগ production app-এ দুটোই ব্যবহার হয়।

প্রশ্ন: N+1 problem কী?

উত্তর: 1 query তে list load, তারপর প্রতি item-এর জন্য আলাদা query।
10টি orders → 1 + 10 = 11 queries।
Solution: Include() দিয়ে eager loading।
Detection: EF Core logging enable করুন।

প্রশ্ন: AsNoTracking কখন ব্যবহার করবেন?

উত্তর: Read-only operations-এ। API GET responses।
Change tracking না লাগলে — update করবেন না।
Performance difference: ~20-30% faster, কম memory।
ডেটা update করতে হলে → tracking দরকার।

প্রশ্ন: Optimistic আর Pessimistic concurrency পার্থক্য?

উত্তর:
Optimistic → conflict rare ধরে নেয়। RowVersion দিয়ে conflict detect।
             DbUpdateConcurrencyException → retry বা 409।
             EF Core default।
Pessimistic → lock ধরে রাখে। SELECT ... WITH (UPDLOCK)।
             High contention scenario। EF Core-এ manual।

প্রশ্ন: Repository Pattern-এর সুবিধা কী?

উত্তর: Data access abstraction। Service layer DB জানে না।
       Unit test-এ mock করা যায়।
       ORM swap করা সহজ হয়।
       Cons: EF Core নিজেই Unit of Work + Repository।
             Over-engineering হতে পারে simple apps-এ।

প্রশ্ন: Migration rollback কীভাবে করবেন?

উত্তর: dotnet ef database update PreviousMigrationName
       তারপর dotnet ef migrations remove।
       Production-এ: migration script generate করে DBA দিয়ে run।
       Down() method সবসময় implement করুন।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 8 — Authentication ও Security (JWT, Cookie Auth, Identity, OAuth2/OIDC, Role-based & Policy-based Authorization, Data Protection এবং আরও...)

---

<a id="part8"></a>
## PART 8: Authentication ও Security

> JWT Authentication, Cookie Auth, ASP.NET Core Identity, OAuth2/OIDC, Role-based & Policy-based Authorization, Data Protection, OWASP Top 10।

| # | বিষয় |
|---|-------|
| 1 | [Authentication vs Authorization](#p8-authn-authz) |
| 2 | [JWT Authentication](#p8-jwt) |
| 3 | [Refresh Tokens](#p8-refresh) |
| 4 | [ASP.NET Core Identity](#p8-identity) |
| 5 | [Role-based Authorization](#p8-roles) |
| 6 | [Policy-based Authorization](#p8-policies) |
| 7 | [OAuth2 ও OpenID Connect](#p8-oauth) |
| 8 | [Data Protection ও Encryption](#p8-dataprotection) |
| 9 | [OWASP Top 10 in .NET](#p8-owasp) |
| 10 | [Security Best Practices](#p8-bestpractices) |

---

<a id="p8-authn-authz"></a>
### Topic 1: Authentication vs Authorization

```
Authentication (AuthN) — "আপনি কে?"
→ Identity verify করা। Login। JWT/Cookie validate।

Authorization (AuthZ) — "আপনি কী করতে পারবেন?"
→ Permission check। Role, Policy, Claim।

Flow:
Request → [Authentication Middleware] → [Authorization Middleware] → Endpoint
             ↓ validates token/cookie        ↓ checks roles/policies
             sets HttpContext.User            allows or 403 Forbidden
```

---

<a id="p8-jwt"></a>
### Topic 2: JWT Authentication

**JWT Structure:**
```
Header.Payload.Signature
eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI0MiIsInJvbGUiOiJBZG1pbiJ9.xyz

Header:  { "alg": "HS256", "typ": "JWT" }
Payload: { "sub": "42", "name": "Rahim", "role": "Admin", "exp": 1234567890 }
Signature: HMACSHA256(base64(header) + "." + base64(payload), secret)
```

```csharp
// Install:
// dotnet add package Microsoft.AspNetCore.Authentication.JwtBearer
// dotnet add package System.IdentityModel.Tokens.Jwt

// ── JWT Service ───────────────────────────────────────
public class JwtService
{
    private readonly JwtOptions _options;
    public JwtService(IOptions<JwtOptions> options) => _options = options.Value;

    public string GenerateToken(User user, IList<string> roles)
    {
        var claims = new List<Claim>
        {
            new(JwtRegisteredClaimNames.Sub,   user.Id.ToString()),
            new(JwtRegisteredClaimNames.Email, user.Email),
            new(JwtRegisteredClaimNames.Name,  user.FullName),
            new(JwtRegisteredClaimNames.Jti,   Guid.NewGuid().ToString()), // unique token id
        };

        // Add roles as claims
        claims.AddRange(roles.Select(r => new Claim(ClaimTypes.Role, r)));

        var key = new SymmetricSecurityKey(
            Encoding.UTF8.GetBytes(_options.Key)); // must be >= 32 chars!

        var token = new JwtSecurityToken(
            issuer:   _options.Issuer,
            audience: _options.Audience,
            claims:   claims,
            expires:  DateTime.UtcNow.AddMinutes(_options.ExpiryMinutes),
            signingCredentials: new SigningCredentials(key, SecurityAlgorithms.HmacSha256));

        return new JwtSecurityTokenHandler().WriteToken(token);
    }

    public ClaimsPrincipal? ValidateToken(string token)
    {
        var handler = new JwtSecurityTokenHandler();
        try
        {
            return handler.ValidateToken(token,
                new TokenValidationParameters
                {
                    ValidateIssuer           = true,
                    ValidIssuer              = _options.Issuer,
                    ValidateAudience         = true,
                    ValidAudience            = _options.Audience,
                    ValidateIssuerSigningKey  = true,
                    IssuerSigningKey          = new SymmetricSecurityKey(
                        Encoding.UTF8.GetBytes(_options.Key)),
                    ValidateLifetime         = true,
                    ClockSkew                = TimeSpan.Zero, // no grace period
                },
                out _);
        }
        catch { return null; }
    }
}

// ── Register JWT authentication ────────────────────────
builder.Services
    .AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
    .AddJwtBearer(options =>
    {
        options.TokenValidationParameters = new TokenValidationParameters
        {
            ValidateIssuer           = true,
            ValidIssuer              = builder.Configuration["Jwt:Issuer"],
            ValidateAudience         = true,
            ValidAudience            = builder.Configuration["Jwt:Audience"],
            ValidateIssuerSigningKey  = true,
            IssuerSigningKey          = new SymmetricSecurityKey(
                Encoding.UTF8.GetBytes(builder.Configuration["Jwt:Key"]!)),
            ValidateLifetime         = true,
            ClockSkew                = TimeSpan.Zero
        };

        // SignalR — JWT from query string
        options.Events = new JwtBearerEvents
        {
            OnMessageReceived = ctx =>
            {
                var token = ctx.Request.Query["access_token"];
                if (!string.IsNullOrEmpty(token) &&
                    ctx.HttpContext.Request.Path.StartsWithSegments("/hubs"))
                    ctx.Token = token;
                return Task.CompletedTask;
            }
        };
    });

// ── Auth controller ────────────────────────────────────
[ApiController]
[Route("api/auth")]
public class AuthController : ControllerBase
{
    private readonly UserManager<AppUser> _userManager;
    private readonly JwtService           _jwt;

    public AuthController(UserManager<AppUser> userManager, JwtService jwt)
    {
        _userManager = userManager;
        _jwt = jwt;
    }

    [HttpPost("login")]
    public async Task<IActionResult> Login([FromBody] LoginDto dto)
    {
        var user = await _userManager.FindByEmailAsync(dto.Email);
        if (user is null || !await _userManager.CheckPasswordAsync(user, dto.Password))
            return Unauthorized(new { message = "Invalid credentials" });

        var roles = await _userManager.GetRolesAsync(user);
        var token = _jwt.GenerateToken(user, roles);

        return Ok(new
        {
            token,
            expiresIn = 3600,
            user = new { user.Id, user.Email, user.FullName }
        });
    }

    [HttpPost("register")]
    public async Task<IActionResult> Register([FromBody] RegisterDto dto)
    {
        var user = new AppUser
        {
            UserName = dto.Email,
            Email    = dto.Email,
            FullName = dto.FullName
        };

        var result = await _userManager.CreateAsync(user, dto.Password);
        if (!result.Succeeded)
            return BadRequest(result.Errors);

        await _userManager.AddToRoleAsync(user, "Customer");
        return Ok(new { message = "Registered successfully" });
    }

    [Authorize]
    [HttpGet("me")]
    public async Task<IActionResult> GetCurrentUser()
    {
        var userId = User.FindFirstValue(JwtRegisteredClaimNames.Sub);
        var user = await _userManager.FindByIdAsync(userId!);
        return Ok(new { user!.Id, user.Email, user.FullName });
    }
}
```

---

<a id="p8-refresh"></a>
### Topic 3: Refresh Tokens

```csharp
// JWT short-lived (15-60 min) + refresh token long-lived (7-30 days)

public class RefreshToken
{
    public int      Id        { get; set; }
    public string   Token     { get; set; } = "";   // random, stored in DB
    public int      UserId    { get; set; }
    public DateTime ExpiresAt { get; set; }
    public bool     IsRevoked { get; set; }
    public string?  ReplacedByToken { get; set; }  // rotation tracking
}

public class TokenService
{
    private readonly AppDbContext _db;
    private readonly JwtService   _jwt;

    public async Task<TokenPair> RefreshAsync(string refreshToken, CancellationToken ct)
    {
        var stored = await _db.RefreshTokens
            .Include(r => r.User)
            .FirstOrDefaultAsync(r => r.Token == refreshToken, ct);

        if (stored is null || stored.IsRevoked || stored.ExpiresAt < DateTime.UtcNow)
            throw new UnauthorizedAccessException("Invalid refresh token");

        // Rotate — revoke old, issue new
        stored.IsRevoked = true;

        var newRefresh = new RefreshToken
        {
            Token     = GenerateSecureToken(),
            UserId    = stored.UserId,
            ExpiresAt = DateTime.UtcNow.AddDays(30),
        };
        stored.ReplacedByToken = newRefresh.Token;

        _db.RefreshTokens.Add(newRefresh);
        await _db.SaveChangesAsync(ct);

        var roles  = await _userManager.GetRolesAsync(stored.User);
        var access = _jwt.GenerateToken(stored.User, roles);

        return new TokenPair(access, newRefresh.Token);
    }

    private static string GenerateSecureToken() =>
        Convert.ToBase64String(RandomNumberGenerator.GetBytes(64));
}

// ── Refresh endpoint ──────────────────────────────────
[HttpPost("refresh")]
public async Task<IActionResult> Refresh([FromBody] RefreshRequest dto)
{
    try
    {
        var tokens = await _tokenService.RefreshAsync(dto.RefreshToken, HttpContext.RequestAborted);
        return Ok(tokens);
    }
    catch (UnauthorizedAccessException)
    {
        return Unauthorized(new { message = "Invalid or expired refresh token" });
    }
}
```

---

<a id="p8-identity"></a>
### Topic 4: ASP.NET Core Identity

```csharp
// Install: dotnet add package Microsoft.AspNetCore.Identity.EntityFrameworkCore

// ── Custom AppUser ────────────────────────────────────
public class AppUser : IdentityUser<int>  // int PK instead of string
{
    public string FullName   { get; set; } = "";
    public DateTime CreatedAt { get; set; }
    public bool IsActive     { get; set; } = true;
}

// ── DbContext with Identity ───────────────────────────
public class AppDbContext : IdentityDbContext<AppUser, IdentityRole<int>, int>
{
    public AppDbContext(DbContextOptions<AppDbContext> options) : base(options) { }
    // Identity tables auto-created: AspNetUsers, AspNetRoles, AspNetUserRoles, etc.
}

// ── Register Identity ──────────────────────────────────
builder.Services
    .AddIdentity<AppUser, IdentityRole<int>>(options =>
    {
        // Password policy
        options.Password.RequiredLength         = 8;
        options.Password.RequireDigit           = true;
        options.Password.RequireUppercase       = true;
        options.Password.RequireNonAlphanumeric = false;

        // Lockout policy
        options.Lockout.MaxFailedAccessAttempts = 5;
        options.Lockout.DefaultLockoutTimeSpan  = TimeSpan.FromMinutes(15);
        options.Lockout.AllowedForNewUsers       = true;

        // User settings
        options.User.RequireUniqueEmail = true;
    })
    .AddEntityFrameworkStores<AppDbContext>()
    .AddDefaultTokenProviders(); // for email confirmation, password reset

// ── UserManager common operations ─────────────────────
public class UserService
{
    private readonly UserManager<AppUser> _users;
    private readonly RoleManager<IdentityRole<int>> _roles;

    // Create user
    public async Task<IdentityResult> CreateAsync(string email, string password, string fullName)
    {
        var user = new AppUser { UserName = email, Email = email, FullName = fullName };
        var result = await _users.CreateAsync(user, password);
        if (result.Succeeded)
            await _users.AddToRoleAsync(user, "Customer");
        return result;
    }

    // Password reset flow
    public async Task<string> GeneratePasswordResetTokenAsync(string email)
    {
        var user = await _users.FindByEmailAsync(email)
            ?? throw new KeyNotFoundException();
        return await _users.GeneratePasswordResetTokenAsync(user);
    }

    public async Task ResetPasswordAsync(string email, string token, string newPassword)
    {
        var user = await _users.FindByEmailAsync(email)
            ?? throw new KeyNotFoundException();
        var result = await _users.ResetPasswordAsync(user, token, newPassword);
        if (!result.Succeeded)
            throw new InvalidOperationException(string.Join(", ", result.Errors.Select(e => e.Description)));
    }

    // Email confirmation
    public async Task<string> GenerateEmailConfirmationTokenAsync(AppUser user) =>
        await _users.GenerateEmailConfirmationTokenAsync(user);

    public async Task ConfirmEmailAsync(string userId, string token)
    {
        var user = await _users.FindByIdAsync(userId)
            ?? throw new KeyNotFoundException();
        await _users.ConfirmEmailAsync(user, token);
    }
}
```

---

<a id="p8-roles"></a>
### Topic 5: Role-based Authorization

```csharp
// ── Seed roles ────────────────────────────────────────
var roleManager = app.Services.GetRequiredService<RoleManager<IdentityRole<int>>>();
foreach (var role in new[] { "Admin", "Manager", "Customer" })
{
    if (!await roleManager.RoleExistsAsync(role))
        await roleManager.CreateAsync(new IdentityRole<int>(role));
}

// ── Apply on endpoints ────────────────────────────────
// Require authentication (any role)
[Authorize]
[HttpGet("profile")]
public IActionResult GetProfile() => Ok(User.Identity!.Name);

// Require specific role
[Authorize(Roles = "Admin")]
[HttpDelete("{id:int}")]
public IActionResult Delete(int id) => Ok();

// Multiple roles (OR — any one)
[Authorize(Roles = "Admin,Manager")]
[HttpGet("reports")]
public IActionResult GetReports() => Ok();

// ── Claims-based role check in code ──────────────────
[HttpPost("{id:int}/approve")]
[Authorize]
public IActionResult Approve(int id)
{
    var userId = User.FindFirstValue(ClaimTypes.NameIdentifier);
    var isAdmin = User.IsInRole("Admin");
    var email   = User.FindFirstValue(ClaimTypes.Email);

    if (!isAdmin)
        return Forbid(); // 403

    return Ok();
}
```

---

<a id="p8-policies"></a>
### Topic 6: Policy-based Authorization

```csharp
// More flexible than role-based — combine claims, roles, custom logic

builder.Services.AddAuthorization(options =>
{
    // Simple role policy
    options.AddPolicy("AdminOnly",    p => p.RequireRole("Admin"));
    options.AddPolicy("ManagerOrAdmin", p => p.RequireRole("Admin", "Manager"));

    // Claim-based
    options.AddPolicy("VerifiedUser", p =>
        p.RequireClaim("email_verified", "true"));

    // Custom requirement
    options.AddPolicy("MinimumAge18", p =>
        p.Requirements.Add(new MinimumAgeRequirement(18)));

    options.AddPolicy("SameUserOrAdmin", p =>
        p.Requirements.Add(new SameUserOrAdminRequirement()));
});

// ── Custom requirement ────────────────────────────────
public class MinimumAgeRequirement : IAuthorizationRequirement
{
    public int MinimumAge { get; }
    public MinimumAgeRequirement(int age) => MinimumAge = age;
}

public class MinimumAgeHandler : AuthorizationHandler<MinimumAgeRequirement>
{
    protected override Task HandleRequirementAsync(
        AuthorizationHandlerContext context,
        MinimumAgeRequirement requirement)
    {
        var birthDateClaim = context.User.FindFirst("birthdate");
        if (birthDateClaim is null)
        {
            context.Fail();
            return Task.CompletedTask;
        }

        var birthDate = DateTime.Parse(birthDateClaim.Value);
        var age = DateTime.Today.Year - birthDate.Year;
        if (birthDate > DateTime.Today.AddYears(-age)) age--;

        if (age >= requirement.MinimumAge)
            context.Succeed(requirement);

        return Task.CompletedTask;
    }
}

// Register handler
builder.Services.AddScoped<IAuthorizationHandler, MinimumAgeHandler>();
builder.Services.AddScoped<IAuthorizationHandler, SameUserOrAdminHandler>();

// ── Resource-based authorization ──────────────────────
public class SameUserOrAdminHandler
    : AuthorizationHandler<SameUserOrAdminRequirement, Order>
{
    protected override Task HandleRequirementAsync(
        AuthorizationHandlerContext context,
        SameUserOrAdminRequirement requirement,
        Order resource)
    {
        var userId = context.User.FindFirstValue(JwtRegisteredClaimNames.Sub);
        if (context.User.IsInRole("Admin") || resource.CustomerId.ToString() == userId)
            context.Succeed(requirement);
        return Task.CompletedTask;
    }
}

// ── Controller with policy ────────────────────────────
[Authorize(Policy = "AdminOnly")]
[HttpGet("admin/dashboard")]
public IActionResult Dashboard() => Ok();

[Authorize(Policy = "VerifiedUser")]
[HttpPost("orders")]
public IActionResult CreateOrder([FromBody] CreateOrderDto dto) => Ok();

// Resource-based check in action
[HttpDelete("{id:int}")]
[Authorize]
public async Task<IActionResult> Delete(int id)
{
    var order = await _service.GetByIdAsync(id);
    if (order is null) return NotFound();

    var authResult = await _authorizationService
        .AuthorizeAsync(User, order, "SameUserOrAdmin");

    if (!authResult.Succeeded) return Forbid();

    await _service.DeleteAsync(id);
    return NoContent();
}
```

---

<a id="p8-oauth"></a>
### Topic 7: OAuth2 ও OpenID Connect

```
OAuth2 Flow (Authorization Code):
──────────────────────────────────────────────────────
1. User clicks "Login with Google"
2. App redirects → Google Authorization Server
3. User authenticates & consents
4. Google redirects back → App with authorization code
5. App exchanges code → Access Token (server-to-server)
6. App uses Access Token to call Google APIs
──────────────────────────────────────────────────────

OAuth2 vs OpenID Connect:
OAuth2      → Authorization। Access Token → API access।
OpenID Connect (OIDC) → Authentication। ID Token (JWT) → user identity।
OIDC is OAuth2 + identity layer।
```

```csharp
// ── External login (Google, GitHub) ───────────────────
// Install: dotnet add package Microsoft.AspNetCore.Authentication.Google

builder.Services
    .AddAuthentication()
    .AddGoogle(options =>
    {
        options.ClientId     = builder.Configuration["Google:ClientId"]!;
        options.ClientSecret = builder.Configuration["Google:ClientSecret"]!;
        options.Scope.Add("profile");
        options.Scope.Add("email");
    })
    .AddGitHub(options =>  // dotnet add package AspNet.Security.OAuth.GitHub
    {
        options.ClientId     = builder.Configuration["GitHub:ClientId"]!;
        options.ClientSecret = builder.Configuration["GitHub:ClientSecret"]!;
        options.Scope.Add("user:email");
    });

// ── Handle external login callback ────────────────────
[HttpGet("external-callback")]
public async Task<IActionResult> ExternalCallback()
{
    var info = await _signInManager.GetExternalLoginInfoAsync();
    if (info is null) return BadRequest("External login failed");

    // Try sign in with existing external login
    var result = await _signInManager.ExternalLoginSignInAsync(
        info.LoginProvider, info.ProviderKey, isPersistent: false);

    if (result.Succeeded)
    {
        var user = await _userManager.FindByLoginAsync(info.LoginProvider, info.ProviderKey);
        var roles = await _userManager.GetRolesAsync(user!);
        return Ok(new { token = _jwt.GenerateToken(user!, roles) });
    }

    // New user — register
    var email = info.Principal.FindFirstValue(ClaimTypes.Email)!;
    var newUser = new AppUser
    {
        UserName = email,
        Email    = email,
        FullName = info.Principal.FindFirstValue(ClaimTypes.Name) ?? email
    };

    var createResult = await _userManager.CreateAsync(newUser);
    if (!createResult.Succeeded) return BadRequest(createResult.Errors);

    await _userManager.AddLoginAsync(newUser, info);
    await _userManager.AddToRoleAsync(newUser, "Customer");

    var newRoles = await _userManager.GetRolesAsync(newUser);
    return Ok(new { token = _jwt.GenerateToken(newUser, newRoles) });
}
```

---

<a id="p8-dataprotection"></a>
### Topic 8: Data Protection ও Encryption

```csharp
// ── ASP.NET Core Data Protection ─────────────────────
// Symmetric encryption, key rotation, key storage

builder.Services
    .AddDataProtection()
    .PersistKeysToFileSystem(new DirectoryInfo("/var/keys"))
    .SetApplicationName("MyApp")
    .SetDefaultKeyLifetime(TimeSpan.FromDays(90));

// Usage — encrypt/decrypt strings
public class EncryptionService
{
    private readonly IDataProtector _protector;

    public EncryptionService(IDataProtectionProvider provider) =>
        _protector = provider.CreateProtector("MyApp.SensitiveData");

    public string Encrypt(string value) => _protector.Protect(value);

    public string? Decrypt(string encrypted)
    {
        try { return _protector.Unprotect(encrypted); }
        catch { return null; } // tampered or expired
    }
}

// Time-limited tokens (email confirmation, password reset)
public class TokenEncryptionService
{
    private readonly ITimeLimitedDataProtector _protector;

    public TokenEncryptionService(IDataProtectionProvider provider) =>
        _protector = provider
            .CreateProtector("MyApp.Tokens")
            .ToTimeLimitedDataProtector();

    public string CreateToken(string userId, TimeSpan lifetime) =>
        _protector.Protect(userId, lifetime);

    public string? ValidateToken(string token)
    {
        try { return _protector.Unprotect(token); }
        catch { return null; } // expired or invalid
    }
}

// ── Password hashing ──────────────────────────────────
// Identity handles this — but understanding is important
public class PasswordHashService
{
    private readonly IPasswordHasher<AppUser> _hasher;
    public PasswordHashService(IPasswordHasher<AppUser> hasher) => _hasher = hasher;

    public string Hash(AppUser user, string password) =>
        _hasher.HashPassword(user, password);

    public bool Verify(AppUser user, string hash, string password) =>
        _hasher.VerifyHashedPassword(user, hash, password)
            != PasswordVerificationResult.Failed;
}

// ── Secrets management ────────────────────────────────
// Development: dotnet user-secrets set "Jwt:Key" "..."
// Production:  Azure Key Vault / AWS Secrets Manager / environment variables

// Azure Key Vault:
builder.Configuration.AddAzureKeyVault(
    new Uri($"https://{vaultName}.vault.azure.net/"),
    new DefaultAzureCredential());
```

---

<a id="p8-owasp"></a>
### Topic 9: OWASP Top 10 in .NET

```csharp
// ── A01: Broken Access Control ────────────────────────
// ❌ Missing authorization
[HttpGet("{id:int}")]
public async Task<IActionResult> GetOrder(int id)
{
    var order = await _service.GetByIdAsync(id); // any user sees any order!
    return Ok(order);
}

// ✅ Check ownership
[HttpGet("{id:int}")]
[Authorize]
public async Task<IActionResult> GetOrder(int id)
{
    var userId = int.Parse(User.FindFirstValue("sub")!);
    var order = await _service.GetByIdAsync(id);
    if (order is null) return NotFound();
    if (!User.IsInRole("Admin") && order.CustomerId != userId) return Forbid();
    return Ok(order);
}

// ── A02: Cryptographic Failures ──────────────────────
// ❌ Storing plain text passwords
user.Password = password; // NEVER!

// ✅ Identity handles bcrypt hashing
await _userManager.CreateAsync(user, password); // hashed internally

// ❌ Weak JWT secret
"Jwt:Key": "secret"  // too short, guessable

// ✅ Strong secret (min 32 chars), via env/secrets
"Jwt:Key": "x7K9mP2qR5vN8wL3hJ6yT1bF4cD0eA" // stored in env var!

// ── A03: Injection ────────────────────────────────────
// ❌ SQL injection
var sql = $"SELECT * FROM Users WHERE Email = '{email}'"; // NEVER!
// email = "'; DROP TABLE Users; --"

// ✅ Parameterized (EF Core / Dapper)
var user = await _db.Users.Where(u => u.Email == email).FirstOrDefaultAsync();

await _db.Database.ExecuteSqlInterpolated(
    $"SELECT * FROM Users WHERE Email = {email}"); // safe — parameterized!

// ── A04: Insecure Design ──────────────────────────────
// ✅ Rate limit login — brute force prevention
// ✅ Account lockout (Identity: MaxFailedAccessAttempts)
// ✅ CAPTCHA on registration/login
// ✅ Input validation everywhere

// ── A05: Security Misconfiguration ────────────────────
// ✅ Remove default/debug endpoints in production
if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/error"); // no stack traces in prod!
    app.UseHsts();
}

// ✅ Security headers middleware
app.Use(async (ctx, next) =>
{
    ctx.Response.Headers["X-Content-Type-Options"]    = "nosniff";
    ctx.Response.Headers["X-Frame-Options"]           = "DENY";
    ctx.Response.Headers["X-XSS-Protection"]          = "1; mode=block";
    ctx.Response.Headers["Referrer-Policy"]            = "strict-origin";
    ctx.Response.Headers["Permissions-Policy"]         = "camera=(), microphone=()";
    await next();
});

// ── A06: Vulnerable Components ────────────────────────
// dotnet list package --vulnerable
// dotnet outdated (install: dotnet tool install dotnet-outdated-tool)
// GitHub Dependabot alerts

// ── A07: Auth Failures ────────────────────────────────
// ✅ JWT: short expiry (15-60 min), refresh tokens
// ✅ Refresh token rotation — revoke on use
// ✅ Token revocation list (Redis)
// ✅ HTTPS everywhere

// ── A08: Software & Data Integrity ───────────────────
// ✅ Verify NuGet package signatures
// ✅ Use official Microsoft packages
// ✅ CI/CD pipeline security scanning (Snyk, OWASP Dependency Check)

// ── A09: Logging & Monitoring ─────────────────────────
// ✅ Log auth failures, access denied
// ❌ Never log passwords, tokens, PII!
_logger.LogWarning("Failed login attempt for {Email}", email); // OK
_logger.LogInformation("User {Email} logged in with password {Password}", email, password); // NEVER!

// ── A10: SSRF (Server-Side Request Forgery) ───────────
// ❌ Fetching user-supplied URL
var data = await _httpClient.GetStringAsync(userProvidedUrl); // dangerous!

// ✅ Whitelist allowed domains
var allowed = new[] { "api.trusted.com", "data.safe-service.com" };
var uri = new Uri(userProvidedUrl);
if (!allowed.Contains(uri.Host))
    return BadRequest("URL not allowed");
```

---

<a id="p8-bestpractices"></a>
### Topic 10: Security Best Practices

```csharp
// ── 1. HTTPS enforcement ──────────────────────────────
app.UseHttpsRedirection();
app.UseHsts(); // HTTP Strict Transport Security

// ── 2. Secure cookies ────────────────────────────────
builder.Services.Configure<CookieAuthenticationOptions>(options =>
{
    options.Cookie.HttpOnly   = true;   // JS cannot access
    options.Cookie.Secure     = true;   // HTTPS only
    options.Cookie.SameSite   = SameSiteMode.Strict; // CSRF protection
    options.ExpireTimeSpan    = TimeSpan.FromHours(1);
    options.SlidingExpiration = true;
});

// ── 3. Anti-forgery (CSRF) ────────────────────────────
// API with JWT → CSRF not needed (no cookies)
// MVC with cookie auth → use [ValidateAntiForgeryToken]
builder.Services.AddAntiforgery(options =>
{
    options.HeaderName = "X-CSRF-TOKEN"; // SPA usage
});

// ── 4. Input sanitization ─────────────────────────────
// ❌ Storing raw HTML (XSS risk)
post.Content = dto.Content; // what if it contains <script>?

// ✅ Encode output (Razor does this automatically)
// For stored HTML, use HtmlSanitizer library:
// dotnet add package HtmlSanitizer
var sanitizer = new HtmlSanitizer();
post.Content = sanitizer.Sanitize(dto.Content);

// ── 5. Secrets never in code/config ───────────────────
// ❌ In appsettings.json — committed to git
"ConnectionStrings": { "Default": "Server=prod;Password=realpassword" }

// ✅ Environment variables or secrets manager
Environment.GetEnvironmentVariable("ConnectionStrings__Default")

// ── 6. Secure random ──────────────────────────────────
// ❌ Random — predictable
var token = new Random().Next(100000, 999999).ToString();

// ✅ Cryptographically secure
var bytes = RandomNumberGenerator.GetBytes(32);
var token = Convert.ToBase64String(bytes);

// ── 7. Minimal permissions ────────────────────────────
// DB user should only have SELECT/INSERT/UPDATE on needed tables
// Service account — minimal IAM permissions
// API keys — scoped to specific resources

// ── 8. Content Security Policy ───────────────────────
app.Use(async (ctx, next) =>
{
    ctx.Response.Headers["Content-Security-Policy"] =
        "default-src 'self'; script-src 'self'; style-src 'self' 'unsafe-inline'";
    await next();
});
```

---

## PART 8 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| Authentication | Identity verify — "আপনি কে?" |
| Authorization | Permission check — "আপনি কী করতে পারবেন?" |
| JWT | Header.Payload.Signature — stateless token |
| JWT Claims | sub, email, role, exp, jti |
| `[Authorize]` | Requires authentication |
| `[Authorize(Roles)]` | Role-based |
| `[Authorize(Policy)]` | Policy-based |
| Refresh Token | Long-lived, rotate on use, stored in DB |
| Token Rotation | Old revoked, new issued on refresh |
| Identity | UserManager, RoleManager, SignInManager |
| Lockout | MaxFailedAccessAttempts — brute force |
| Policy | IAuthorizationRequirement + Handler |
| Resource Auth | `_authorizationService.AuthorizeAsync(User, resource, policy)` |
| OAuth2 | Authorization framework — access token |
| OIDC | OAuth2 + identity layer — ID token |
| Data Protection | `IDataProtectionProvider` — encrypt/decrypt |
| SQL Injection | Parameterized queries — EF Core / Dapper |
| XSS | Output encoding, CSP, HtmlSanitizer |
| CSRF | SameSite cookies, antiforgery tokens |
| HTTPS | `UseHttpsRedirection()`, `UseHsts()` |
| Security Headers | X-Frame-Options, CSP, X-Content-Type-Options |
| Secrets | User Secrets (dev), Key Vault (prod) |
| OWASP A01 | Broken Access Control |
| OWASP A03 | Injection — SQL, LDAP |
| OWASP A07 | Identification & Auth Failures |

---

## PART 8 Interview Q&A

```
প্রশ্ন: JWT-এর সুবিধা ও অসুবিধা?
উত্তর:
✅ Stateless — server session রাখতে হয় না।
✅ Scalable — multiple servers-এ কাজ করে।
✅ Mobile-friendly।
❌ Revoke করা কঠিন — expiry পর্যন্ত valid।
❌ Payload বড় হলে request size বাড়ে।
❌ Secret compromise হলে সব token invalid করা কঠিন।

প্রশ্ন: JWT token revoke কীভাবে করবেন?
উত্তর:
Short expiry (15 min) + refresh token pattern।
Token blacklist (Redis-এ jti store)।
Refresh token revocation (DB-তে mark করুন)।
Key rotation (সব token invalid করতে)।

প্রশ্ন: Cookie auth কখন, JWT কখন?
উত্তর:
Cookie → Traditional web app, MVC, same-origin।
         Server-side session optional, CSRF protection দরকার।
JWT → SPA, Mobile app, Microservices, Cross-domain API।
      Stateless, scalable।

প্রশ্ন: Role-based vs Policy-based পার্থক্য?
উত্তর:
Role-based → Simple। Admin/User/Manager।
Policy-based → Complex। Multiple claims, custom logic, resource-based।
              বেশি flexible। Production preference।

প্রশ্ন: SQL Injection কীভাবে prevent করবেন .NET-এ?
উত্তর:
EF Core → LINQ queries auto-parameterized।
Dapper → @Parameter syntax।
FromSqlInterpolated → string interpolation but parameterized।
NEVER string concatenation বা FromSqlRaw with user input।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 9 — Frontend Integration ও Full Stack (.NET + React/Angular, SignalR Real-time, Blazor, gRPC, Background Services এবং আরও...)

---

<a id="part9"></a>
## PART 9: Frontend Integration ও Full Stack

> .NET + React/Angular, HttpClient, SignalR, Blazor, gRPC, Background Services, Caching, IHostedService।

| # | বিষয় |
|---|-------|
| 1 | [.NET + React/Angular Integration](#p9-spa) |
| 2 | [HttpClient ও IHttpClientFactory](#p9-httpclient) |
| 3 | [SignalR — Real-time Communication](#p9-signalr) |
| 4 | [Blazor](#p9-blazor) |
| 5 | [gRPC](#p9-grpc) |
| 6 | [Background Services ও IHostedService](#p9-background) |
| 7 | [Caching Strategies](#p9-caching) |
| 8 | [Distributed Systems Basics](#p9-distributed) |

---

<a id="p9-spa"></a>
### Topic 1: .NET + React/Angular Integration

```csharp
// ── Option 1: Separate projects (preferred production) ─
// Backend: ASP.NET Core Web API (port 5000)
// Frontend: React/Angular (port 3000 dev, CDN/static in prod)
// CORS configured on API → enables cross-origin calls

// ── Option 2: SPA inside .NET project ────────────────
// dotnet new react -o MyApp       (React template)
// dotnet new angular -o MyApp     (Angular template)

// Program.cs (SPA served from wwwroot/ClientApp/build)
builder.Services.AddSpaStaticFiles(config =>
    config.RootPath = "ClientApp/build");

app.UseSpaStaticFiles();
app.UseSpa(spa =>
{
    spa.Options.SourcePath = "ClientApp";
    if (app.Environment.IsDevelopment())
        spa.UseReactDevelopmentServer(npmScript: "start");
});

// ── Calling .NET API from React ───────────────────────
// services/api.ts
/*
const API_BASE = process.env.REACT_APP_API_URL ?? '/api';

const authFetch = async (url: string, options: RequestInit = {}) => {
  const token = localStorage.getItem('token');
  const res = await fetch(`${API_BASE}${url}`, {
    ...options,
    headers: {
      'Content-Type': 'application/json',
      ...(token ? { Authorization: `Bearer ${token}` } : {}),
      ...options.headers,
    },
  });
  if (res.status === 401) { logout(); return; }
  if (!res.ok) throw await res.json();
  return res.json();
};

export const orderApi = {
  getAll:   () => authFetch('/orders'),
  getById:  (id: number) => authFetch(`/orders/${id}`),
  create:   (dto: CreateOrderDto) =>
    authFetch('/orders', { method: 'POST', body: JSON.stringify(dto) }),
};
*/

// ── Environment-specific CORS ─────────────────────────
builder.Services.AddCors(opt =>
    opt.AddPolicy("SpaPolicy", policy => policy
        .WithOrigins(
            "http://localhost:3000",  // React dev
            "http://localhost:4200",  // Angular dev
            "https://myapp.com")     // Production
        .AllowAnyMethod()
        .AllowAnyHeader()
        .AllowCredentials()));

app.UseCors("SpaPolicy");
```

---

<a id="p9-httpclient"></a>
### Topic 2: HttpClient ও IHttpClientFactory

```csharp
// ❌ Don't create HttpClient with new — socket exhaustion!
// var client = new HttpClient(); // each call opens new TCP connection

// ✅ IHttpClientFactory — pooled connections
builder.Services.AddHttpClient();

// Named client
builder.Services.AddHttpClient("payments", client =>
{
    client.BaseAddress = new Uri("https://api.payment.com");
    client.DefaultRequestHeaders.Add("Accept", "application/json");
    client.Timeout = TimeSpan.FromSeconds(30);
});

// Typed client — preferred
builder.Services.AddHttpClient<PaymentGatewayClient>(client =>
{
    client.BaseAddress = new Uri(builder.Configuration["Payment:BaseUrl"]!);
});

public class PaymentGatewayClient
{
    private readonly HttpClient _http;
    public PaymentGatewayClient(HttpClient http) => _http = http;

    public async Task<PaymentResult> ChargeAsync(ChargeRequest request, CancellationToken ct)
    {
        var response = await _http.PostAsJsonAsync("/v1/charge", request, ct);
        response.EnsureSuccessStatusCode();
        return await response.Content.ReadFromJsonAsync<PaymentResult>(cancellationToken: ct)
            ?? throw new InvalidOperationException("Empty response");
    }
}

// ── Polly resilience policies ─────────────────────────
// dotnet add package Microsoft.Extensions.Http.Resilience

builder.Services.AddHttpClient<ExternalApiClient>()
    .AddStandardResilienceHandler(); // retry + circuit breaker + timeout

// Custom policy:
builder.Services.AddHttpClient<WeatherClient>()
    .AddResilienceHandler("weather-pipeline", pipeline =>
    {
        pipeline.AddRetry(new HttpRetryStrategyOptions
        {
            MaxRetryAttempts = 3,
            Delay            = TimeSpan.FromSeconds(1),
            BackoffType      = DelayBackoffType.Exponential,
            ShouldHandle     = args => args.Outcome.Result?.IsSuccessStatusCode is false
                ? PredicateResult.True() : PredicateResult.False()
        });
        pipeline.AddCircuitBreaker(new HttpCircuitBreakerStrategyOptions
        {
            FailureRatio     = 0.5,
            SamplingDuration = TimeSpan.FromSeconds(30),
            BreakDuration    = TimeSpan.FromSeconds(15)
        });
        pipeline.AddTimeout(TimeSpan.FromSeconds(10));
    });

// ── Calling external API ──────────────────────────────
public class GeoLocationService
{
    private readonly IHttpClientFactory _factory;
    public GeoLocationService(IHttpClientFactory factory) => _factory = factory;

    public async Task<string?> GetCountryAsync(string ip, CancellationToken ct)
    {
        using var client = _factory.CreateClient();
        var result = await client.GetFromJsonAsync<GeoResult>(
            $"https://ipapi.co/{ip}/json/", ct);
        return result?.CountryName;
    }
}
```

---

<a id="p9-signalr"></a>
### Topic 3: SignalR — Real-time Communication

**সহজ ভাষায়:** SignalR → server থেকে client-এ push। Chat, notifications, live dashboard।

```csharp
// ── Hub definition ────────────────────────────────────
public class NotificationHub : Hub
{
    // Client → Server call
    public async Task JoinGroup(string groupName) =>
        await Groups.AddToGroupAsync(Context.ConnectionId, groupName);

    public async Task LeaveGroup(string groupName) =>
        await Groups.RemoveFromGroupAsync(Context.ConnectionId, groupName);

    // Connection lifecycle
    public override async Task OnConnectedAsync()
    {
        var userId = Context.User?.FindFirstValue("sub");
        if (userId is not null)
            await Groups.AddToGroupAsync(Context.ConnectionId, $"user-{userId}");
        await base.OnConnectedAsync();
    }
}

// Register:
builder.Services.AddSignalR();
app.MapHub<NotificationHub>("/hubs/notifications");

// ── Server → Client push ──────────────────────────────
public class OrderService
{
    private readonly IHubContext<NotificationHub> _hub;
    public OrderService(IHubContext<NotificationHub> hub) => _hub = hub;

    public async Task UpdateOrderStatusAsync(int orderId, string status, int customerId)
    {
        // update DB...

        // Push to specific user
        await _hub.Clients
            .Group($"user-{customerId}")
            .SendAsync("OrderStatusUpdated", new { orderId, status });

        // Push to all connected clients
        await _hub.Clients.All.SendAsync("OrderUpdated", new { orderId, status });
    }
}

// ── React client ──────────────────────────────────────
/*
import * as signalR from '@microsoft/signalr';

const connection = new signalR.HubConnectionBuilder()
  .withUrl('/hubs/notifications', {
    accessTokenFactory: () => localStorage.getItem('token') ?? ''
  })
  .withAutomaticReconnect()
  .build();

connection.on('OrderStatusUpdated', ({ orderId, status }) => {
  console.log(`Order ${orderId} is now ${status}`);
  // update UI
});

await connection.start();
*/
```

---

<a id="p9-blazor"></a>
### Topic 4: Blazor

**সহজ ভাষায়:** Blazor → C# দিয়ে frontend। JavaScript না লিখেও interactive UI।

```
Blazor Hosting Models:
───────────────────────────────────────────────────────
Blazor Server    → Components run on server। SignalR দিয়ে UI update।
                  Small download। Network latency।
                  
Blazor WebAssembly (WASM) → .NET runs in browser।
                  Larger initial download। Offline capable।
                  
Blazor United (.NET 8+) → Server + WASM hybrid। Best of both।
───────────────────────────────────────────────────────
```

```csharp
// ── Blazor component ──────────────────────────────────
@page "/orders"
@inject IOrderService OrderService
@inject NavigationManager Nav

<h1>Orders</h1>

@if (_loading)
{
    <p>Loading...</p>
}
else if (_orders is null || !_orders.Any())
{
    <p>No orders found.</p>
}
else
{
    <table class="table">
        <thead><tr><th>ID</th><th>Amount</th><th>Status</th></tr></thead>
        <tbody>
        @foreach (var order in _orders)
        {
            <tr>
                <td>@order.Id</td>
                <td>@order.TotalAmount.ToString("C")</td>
                <td><span class="badge">@order.Status</span></td>
                <td>
                    <button @onclick="() => ViewDetail(order.Id)">Details</button>
                </td>
            </tr>
        }
        </tbody>
    </table>
}

@code {
    private List<OrderDto>? _orders;
    private bool _loading = true;

    protected override async Task OnInitializedAsync()
    {
        try
        {
            _orders = await OrderService.GetAllAsync();
        }
        finally
        {
            _loading = false;
        }
    }

    private void ViewDetail(int id) =>
        Nav.NavigateTo($"/orders/{id}");
}

// ── Data binding ──────────────────────────────────────
// Two-way: @bind="property"
// One-way: @property
// Event: @onclick, @oninput, @onchange
```

---

<a id="p9-grpc"></a>
### Topic 5: gRPC

**সহজ ভাষায়:** gRPC → Protocol Buffers দিয়ে binary communication। REST-এর চেয়ে ~7× faster। Microservices-এ internal communication-এর জন্য ideal।

```protobuf
// orders.proto
syntax = "proto3";
option csharp_namespace = "MyApp.Grpc";

service OrderService {
  rpc GetOrder (GetOrderRequest) returns (OrderResponse);
  rpc CreateOrder (CreateOrderRequest) returns (OrderResponse);
  rpc StreamOrders (StreamRequest) returns (stream OrderResponse);
}

message GetOrderRequest { int32 id = 1; }

message CreateOrderRequest {
  int32 customer_id = 1;
  repeated OrderItem items = 2;
}

message OrderItem {
  int32 product_id = 1;
  int32 quantity   = 2;
}

message OrderResponse {
  int32  id           = 1;
  double total_amount = 2;
  string status       = 3;
}

message StreamRequest { int32 customer_id = 1; }
```

```csharp
// dotnet add package Grpc.AspNetCore

// ── Server implementation ─────────────────────────────
public class OrderGrpcService : OrderService.OrderServiceBase
{
    private readonly IOrderRepository _repo;
    public OrderGrpcService(IOrderRepository repo) => _repo = repo;

    public override async Task<OrderResponse> GetOrder(
        GetOrderRequest request,
        ServerCallContext context)
    {
        var order = await _repo.GetByIdAsync(request.Id, context.CancellationToken)
            ?? throw new RpcException(new Status(StatusCode.NotFound, "Order not found"));

        return new OrderResponse
        {
            Id          = order.Id,
            TotalAmount = (double)order.TotalAmount,
            Status      = order.Status
        };
    }

    public override async Task StreamOrders(
        StreamRequest request,
        IServerStreamWriter<OrderResponse> responseStream,
        ServerCallContext context)
    {
        var orders = await _repo.GetByCustomerAsync(request.CustomerId);
        foreach (var order in orders)
        {
            context.CancellationToken.ThrowIfCancellationRequested();
            await responseStream.WriteAsync(new OrderResponse
            {
                Id          = order.Id,
                TotalAmount = (double)order.TotalAmount,
                Status      = order.Status
            });
            await Task.Delay(100, context.CancellationToken); // simulate streaming
        }
    }
}

// Register:
builder.Services.AddGrpc();
app.MapGrpcService<OrderGrpcService>();

// ── Client ────────────────────────────────────────────
builder.Services.AddGrpcClient<OrderService.OrderServiceClient>(options =>
    options.Address = new Uri("https://order-service:5001"));

// Usage:
var client = serviceProvider.GetRequiredService<OrderService.OrderServiceClient>();
var response = await client.GetOrderAsync(new GetOrderRequest { Id = 42 });
```

---

<a id="p9-background"></a>
### Topic 6: Background Services ও IHostedService

```csharp
// ── IHostedService — custom lifecycle ─────────────────
public class DatabaseCleanupService : IHostedService, IDisposable
{
    private Timer? _timer;
    private readonly ILogger<DatabaseCleanupService> _logger;
    private readonly IServiceScopeFactory _scopeFactory;

    public DatabaseCleanupService(
        ILogger<DatabaseCleanupService> logger,
        IServiceScopeFactory scopeFactory)
    {
        _logger = logger;
        _scopeFactory = scopeFactory;
    }

    public Task StartAsync(CancellationToken ct)
    {
        _logger.LogInformation("Database cleanup service starting");
        _timer = new Timer(DoWork, null, TimeSpan.Zero, TimeSpan.FromHours(24));
        return Task.CompletedTask;
    }

    private async void DoWork(object? state)
    {
        using var scope = _scopeFactory.CreateScope();
        var db = scope.ServiceProvider.GetRequiredService<AppDbContext>();
        var deleted = await db.Orders
            .Where(o => o.Status == "Cancelled" && o.OrderDate < DateTime.UtcNow.AddDays(-90))
            .ExecuteDeleteAsync();
        _logger.LogInformation("Deleted {Count} old cancelled orders", deleted);
    }

    public Task StopAsync(CancellationToken ct)
    {
        _timer?.Change(Timeout.Infinite, 0);
        return Task.CompletedTask;
    }

    public void Dispose() => _timer?.Dispose();
}

// ── BackgroundService — long-running ─────────────────
public class OrderProcessingWorker : BackgroundService
{
    private readonly ILogger<OrderProcessingWorker> _logger;
    private readonly IServiceScopeFactory _scopeFactory;
    private readonly IMessageQueue _queue;

    public OrderProcessingWorker(
        ILogger<OrderProcessingWorker> logger,
        IServiceScopeFactory scopeFactory,
        IMessageQueue queue)
    {
        _logger = logger;
        _scopeFactory = scopeFactory;
        _queue = queue;
    }

    protected override async Task ExecuteAsync(CancellationToken stoppingToken)
    {
        _logger.LogInformation("Order processor started");

        await foreach (var message in _queue.ReadAllAsync(stoppingToken))
        {
            try
            {
                using var scope = _scopeFactory.CreateScope();
                var service = scope.ServiceProvider.GetRequiredService<IOrderService>();
                await service.ProcessAsync(message, stoppingToken);
                await _queue.AcknowledgeAsync(message);
            }
            catch (Exception ex)
            {
                _logger.LogError(ex, "Failed to process order message {MessageId}", message.Id);
                await _queue.NackAsync(message);
            }
        }
    }
}

// Register:
builder.Services.AddHostedService<DatabaseCleanupService>();
builder.Services.AddHostedService<OrderProcessingWorker>();

// ── Quartz.NET — cron scheduling ──────────────────────
// dotnet add package Quartz.AspNetCore

builder.Services.AddQuartz(q =>
{
    var jobKey = new JobKey("DailyReport");
    q.AddJob<DailyReportJob>(opts => opts.WithIdentity(jobKey));
    q.AddTrigger(opts => opts
        .ForJob(jobKey)
        .WithIdentity("DailyReport-trigger")
        .WithCronSchedule("0 0 6 * * ?")); // 6 AM every day
});
builder.Services.AddQuartzHostedService(q => q.WaitForJobsToComplete = true);

public class DailyReportJob : IJob
{
    private readonly IReportService _reports;
    public DailyReportJob(IReportService reports) => _reports = reports;
    public async Task Execute(IJobExecutionContext context) =>
        await _reports.GenerateDailyReportAsync(context.CancellationToken);
}
```

---

<a id="p9-caching"></a>
### Topic 7: Caching Strategies

```csharp
// ── Memory Cache (single server) ─────────────────────
builder.Services.AddMemoryCache();

public class ProductService
{
    private readonly AppDbContext _db;
    private readonly IMemoryCache _cache;

    public async Task<List<Category>> GetCategoriesAsync()
    {
        const string key = "categories:all";

        return await _cache.GetOrCreateAsync(key, async entry =>
        {
            entry.AbsoluteExpirationRelativeToNow = TimeSpan.FromMinutes(30);
            entry.SlidingExpiration               = TimeSpan.FromMinutes(10);
            entry.Priority = CacheItemPriority.Normal;
            return await _db.Categories.AsNoTracking().ToListAsync();
        }) ?? new List<Category>();
    }

    public void InvalidateCategoriesCache() => _cache.Remove("categories:all");
}

// ── Distributed Cache (multi-server / Redis) ─────────
// dotnet add package Microsoft.Extensions.Caching.StackExchangeRedis

builder.Services.AddStackExchangeRedisCache(options =>
{
    options.Configuration = builder.Configuration["Redis:Connection"];
    options.InstanceName  = "MyApp:";
});

public class DistributedCacheService
{
    private readonly IDistributedCache _cache;
    private static readonly JsonSerializerOptions JsonOpts = new()
        { PropertyNamingPolicy = JsonNamingPolicy.CamelCase };

    public async Task<T?> GetAsync<T>(string key, CancellationToken ct = default)
    {
        var json = await _cache.GetStringAsync(key, ct);
        return json is null ? default : JsonSerializer.Deserialize<T>(json, JsonOpts);
    }

    public async Task SetAsync<T>(string key, T value, TimeSpan? expiry = null,
        CancellationToken ct = default)
    {
        var json = JsonSerializer.Serialize(value, JsonOpts);
        await _cache.SetStringAsync(key, json,
            new DistributedCacheEntryOptions
            {
                AbsoluteExpirationRelativeToNow = expiry ?? TimeSpan.FromMinutes(10)
            }, ct);
    }

    public Task RemoveAsync(string key, CancellationToken ct = default) =>
        _cache.RemoveAsync(key, ct);
}

// ── Response Caching (HTTP layer) ────────────────────
builder.Services.AddResponseCaching();
app.UseResponseCaching();

[HttpGet("categories")]
[ResponseCache(Duration = 300, VaryByQueryKeys = new[] { "page" })]
public async Task<IActionResult> GetCategories([FromQuery] int page = 1) => Ok();

// ── Output Caching (.NET 7+) ──────────────────────────
builder.Services.AddOutputCache(options =>
{
    options.AddBasePolicy(b => b.Expire(TimeSpan.FromMinutes(5)));
    options.AddPolicy("products", b => b
        .Expire(TimeSpan.FromMinutes(10))
        .VaryByQuery("category", "page", "pageSize")
        .Tag("products-cache"));
});
app.UseOutputCache();

[HttpGet]
[OutputCache(PolicyName = "products")]
public async Task<IActionResult> GetProducts([FromQuery] string? category) => Ok();

// Invalidate:
await _outputCacheStore.EvictByTagAsync("products-cache", HttpContext.RequestAborted);

// ── Cache-aside pattern ───────────────────────────────
public async Task<Order?> GetOrderAsync(int id)
{
    var key = $"order:{id}";

    // 1. Cache hit?
    var cached = await _cache.GetAsync<Order>(key);
    if (cached is not null) return cached;

    // 2. DB miss — load from DB
    var order = await _db.Orders.FindAsync(id);
    if (order is null) return null;

    // 3. Store in cache
    await _cache.SetAsync(key, order, expiry: TimeSpan.FromMinutes(15));
    return order;
}
```

---

<a id="p9-distributed"></a>
### Topic 8: Distributed Systems Basics

```csharp
// ── Message Queue (Azure Service Bus / RabbitMQ) ──────
// Decouple services. OrderService → queue → EmailService

// Publisher:
public class OrderService
{
    private readonly ServiceBusClient _bus;

    public async Task CreateAsync(CreateOrderDto dto)
    {
        // Save to DB...
        var order = await _db.SaveAsync(dto);

        // Publish event (fire and forget)
        var sender = _bus.CreateSender("order-events");
        await sender.SendMessageAsync(new ServiceBusMessage(
            JsonSerializer.Serialize(new OrderCreatedEvent(order.Id, order.CustomerId)))
        {
            ContentType   = "application/json",
            Subject       = "OrderCreated",
            CorrelationId = HttpContext.TraceIdentifier
        });
    }
}

// Subscriber (separate service):
public class OrderEmailWorker : BackgroundService
{
    protected override async Task ExecuteAsync(CancellationToken ct)
    {
        var processor = _bus.CreateProcessor("order-events");
        processor.ProcessMessageAsync += async args =>
        {
            var @event = JsonSerializer.Deserialize<OrderCreatedEvent>(args.Message.Body);
            await _emailService.SendOrderConfirmationAsync(@event!.CustomerId);
            await args.CompleteMessageAsync(args.Message, ct);
        };
        processor.ProcessErrorAsync += args =>
        {
            _logger.LogError(args.Exception, "Message processing error");
            return Task.CompletedTask;
        };
        await processor.StartProcessingAsync(ct);
        await Task.Delay(Timeout.Infinite, ct);
    }
}

// ── Idempotency — safe retry ──────────────────────────
[HttpPost("orders")]
public async Task<IActionResult> Create(
    [FromBody] CreateOrderDto dto,
    [FromHeader(Name = "Idempotency-Key")] string? idempotencyKey)
{
    if (idempotencyKey is not null)
    {
        // Check if already processed
        var existing = await _cache.GetAsync<OrderDto>($"idempotency:{idempotencyKey}");
        if (existing is not null) return Ok(existing); // return same response
    }

    var order = await _service.CreateAsync(dto);

    if (idempotencyKey is not null)
        await _cache.SetAsync($"idempotency:{idempotencyKey}", order,
            expiry: TimeSpan.FromDays(1));

    return CreatedAtAction(nameof(GetById), new { id = order.Id }, order);
}

// ── Outbox pattern — reliable event publishing ────────
// Problem: DB save + message publish — what if publish fails?
// Solution: Save event to DB in same transaction, background worker publishes

public class OutboxMessage
{
    public Guid   Id          { get; set; } = Guid.NewGuid();
    public string EventType   { get; set; } = "";
    public string Payload     { get; set; } = "";
    public DateTime CreatedAt  { get; set; }
    public bool   IsProcessed { get; set; }
}

// In OrderService — same transaction:
await using var tx = await _db.Database.BeginTransactionAsync();
_db.Orders.Add(order);
_db.OutboxMessages.Add(new OutboxMessage
{
    EventType = "OrderCreated",
    Payload   = JsonSerializer.Serialize(new OrderCreatedEvent(order.Id)),
    CreatedAt = DateTime.UtcNow
});
await _db.SaveChangesAsync(); // atomic!
await tx.CommitAsync();

// OutboxWorker publishes and marks processed
```

---

## PART 9 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| SPA Integration | Separate projects or UseReactDevelopmentServer |
| CORS | React:3000 → API:5000 cross-origin |
| IHttpClientFactory | Pooled connections — no socket exhaustion |
| Typed HttpClient | `AddHttpClient<T>` — DI-friendly |
| Polly | Retry, circuit breaker, timeout |
| SignalR | Server → Client push — WebSocket/SSE/Long Polling |
| Hub | `Hub` class — server-side SignalR |
| `IHubContext<T>` | Push from non-Hub class (services) |
| Blazor Server | Components on server + SignalR |
| Blazor WASM | .NET in browser via WebAssembly |
| gRPC | Binary Protocol Buffers — fast, typed |
| .proto | gRPC schema definition |
| IHostedService | Startup/shutdown lifecycle |
| BackgroundService | Long-running loop + cancellation |
| Quartz.NET | Cron scheduling |
| IMemoryCache | Single-server in-memory cache |
| IDistributedCache | Redis — multi-server cache |
| Response Caching | HTTP-level caching |
| Output Cache | .NET 7+ server-side output caching |
| Cache-aside | Check cache → DB miss → store |
| Message Queue | Async decoupling — Service Bus, RabbitMQ |
| Idempotency Key | Safe retry — same response for duplicate requests |
| Outbox Pattern | Reliable event publishing — same transaction |

---

## PART 9 Interview Q&A

```
প্রশ্ন: new HttpClient() কেন ব্যবহার করবেন না?
উত্তর: Socket exhaustion। প্রতি call-এ নতুন TCP connection।
DNS change reflect করে না।
IHttpClientFactory → connection pooling, lifetime management।
Always inject IHttpClientFactory বা typed client।

প্রশ্ন: SignalR কোন protocol ব্যবহার করে?
উত্তর: Priority order:
1. WebSocket (best — full-duplex)
2. Server-Sent Events (SSE) — server → client only
3. Long Polling — fallback
Client capability অনুযায়ী auto-negotiate।

প্রশ্ন: IHostedService আর BackgroundService পার্থক্য?
উত্তর:
IHostedService → StartAsync/StopAsync। Full lifecycle control।
BackgroundService → IHostedService implement করে। ExecuteAsync loop।
                    Simple background work-এ prefer।

প্রশ্ন: Memory Cache আর Distributed Cache কখন?
উত্তর:
Memory Cache → Single server, in-process। Session state, temp data।
Distributed Cache (Redis) → Multiple servers, shared state।
                            Auth tokens, sessions, rate limiting।
Production with load balancer → Distributed Cache।

প্রশ্ন: Outbox Pattern কেন দরকার?
উত্তর: DB save + message publish — atomicity নেই।
DB save সফল কিন্তু publish fail → inconsistency।
Outbox: same DB transaction-এ event store।
Background worker publish করে, failure-এ retry।
At-least-once delivery guarantee।

প্রশ্ন: gRPC কখন, REST API কখন?
উত্তর:
REST → Public API, browser clients, HTTP/JSON standard।
gRPC → Internal microservice communication, performance critical।
       Streaming, bidirectional। .NET-to-.NET।
       Browser support limited (grpc-web proxy দরকার)।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 10 — Testing ও Debugging (Unit Testing, Integration Testing, xUnit, Moq, TestContainers, Logging, Debugging Tips এবং আরও...)

---

<a id="part10"></a>
## PART 10: Testing ও Debugging

> Unit Testing, Integration Testing, xUnit, Moq, TestContainers, Logging (Serilog), Debugging এবং Performance Profiling।

| # | বিষয় |
|---|-------|
| 1 | [Unit Testing — xUnit & NUnit](#p10-unit) |
| 2 | [Test Patterns — AAA, Fixtures, Theory](#p10-patterns) |
| 3 | [Mocking with Moq](#p10-moq) |
| 4 | [Integration Testing — WebApplicationFactory](#p10-integration) |
| 5 | [TestContainers — Real DB in Tests](#p10-testcontainers) |
| 6 | [Test Coverage](#p10-coverage) |
| 7 | [Logging — ILogger, Serilog, Structured Logging](#p10-logging) |
| 8 | [Debugging Tips — VS Debugger, dotnet-trace](#p10-debugging) |
| 9 | [Performance Profiling](#p10-profiling) |
| 10 | [Testing Best Practices](#p10-bestpractices) |

---

<a id="p10-unit"></a>
### Topic 1: Unit Testing — xUnit & NUnit

```bash
# Setup
dotnet new xunit -o MyApp.Tests
cd MyApp.Tests
dotnet add reference ../MyApp/MyApp.csproj
dotnet add package Moq
dotnet add package FluentAssertions
dotnet add package Microsoft.AspNetCore.Mvc.Testing
```

```csharp
// ── xUnit ─────────────────────────────────────────────
public class OrderCalculatorTests
{
    private readonly OrderCalculator _sut; // System Under Test

    public OrderCalculatorTests()
    {
        _sut = new OrderCalculator();
    }

    [Fact]
    public void CalculateTotal_WithValidItems_ReturnsCorrectTotal()
    {
        // Arrange
        var items = new List<OrderItem>
        {
            new(ProductId: 1, Quantity: 2, UnitPrice: 100m),
            new(ProductId: 2, Quantity: 1, UnitPrice: 50m),
        };

        // Act
        var total = _sut.CalculateTotal(items);

        // Assert
        Assert.Equal(250m, total);
    }

    [Theory]
    [InlineData(0, false)]
    [InlineData(-1, false)]
    [InlineData(1, true)]
    [InlineData(100, true)]
    public void IsValidQuantity_ReturnsExpected(int quantity, bool expected)
    {
        var result = _sut.IsValidQuantity(quantity);
        Assert.Equal(expected, result);
    }

    [Fact]
    public void CalculateTotal_WithEmptyList_ThrowsArgumentException()
    {
        var act = () => _sut.CalculateTotal(new List<OrderItem>());
        Assert.Throws<ArgumentException>(act);
    }
}

// ── NUnit (alternative) ───────────────────────────────
[TestFixture]
public class ProductServiceNUnitTests
{
    private ProductService _sut = null!;

    [SetUp]
    public void Setup() => _sut = new ProductService();

    [TearDown]
    public void Cleanup() => _sut.Dispose();

    [Test]
    public void GetProduct_WhenExists_ReturnsProduct()
    {
        var result = _sut.GetById(1);
        Assert.That(result, Is.Not.Null);
        Assert.That(result!.Id, Is.EqualTo(1));
    }

    [TestCase(1, true)]
    [TestCase(999, false)]
    public void ProductExists_ReturnsExpected(int id, bool expected)
    {
        Assert.That(_sut.Exists(id), Is.EqualTo(expected));
    }
}
```

---

<a id="p10-patterns"></a>
### Topic 2: Test Patterns — AAA, Fixtures, Theory

```csharp
// ── AAA Pattern ───────────────────────────────────────
// Arrange — setup data and dependencies
// Act     — call the method being tested
// Assert  — verify the outcome

[Fact]
public async Task CreateOrder_ValidInput_ReturnsCreatedOrder()
{
    // Arrange
    var dto = new CreateOrderDto
    {
        CustomerId = 1,
        Items = new[] { new OrderItemDto(ProductId: 10, Quantity: 2) }
    };
    var mockRepo = new Mock<IOrderRepository>();
    mockRepo.Setup(r => r.AddAsync(It.IsAny<Order>(), It.IsAny<CancellationToken>()))
            .ReturnsAsync((Order o, CancellationToken _) => o);

    var service = new OrderService(mockRepo.Object);

    // Act
    var result = await service.CreateAsync(dto);

    // Assert
    Assert.NotNull(result);
    Assert.Equal(dto.CustomerId, result.CustomerId);
    mockRepo.Verify(r => r.AddAsync(It.IsAny<Order>(), It.IsAny<CancellationToken>()),
        Times.Once);
}

// ── Class Fixtures — shared setup ────────────────────
public class DatabaseFixture : IDisposable
{
    public AppDbContext Context { get; }

    public DatabaseFixture()
    {
        var options = new DbContextOptionsBuilder<AppDbContext>()
            .UseInMemoryDatabase(Guid.NewGuid().ToString())
            .Options;
        Context = new AppDbContext(options);
        Context.Database.EnsureCreated();
        SeedData();
    }

    private void SeedData()
    {
        Context.Products.AddRange(
            new Product { Id = 1, Name = "Widget", Price = 9.99m },
            new Product { Id = 2, Name = "Gadget", Price = 19.99m }
        );
        Context.SaveChanges();
    }

    public void Dispose() => Context.Dispose();
}

public class ProductRepositoryTests : IClassFixture<DatabaseFixture>
{
    private readonly AppDbContext _db;
    public ProductRepositoryTests(DatabaseFixture fixture) => _db = fixture.Context;

    [Fact]
    public async Task GetByIdAsync_ExistingId_ReturnsProduct()
    {
        var repo   = new ProductRepository(_db);
        var result = await repo.GetByIdAsync(1);
        Assert.Equal("Widget", result?.Name);
    }
}

// ── FluentAssertions — readable assertions ────────────
[Fact]
public void Order_ShouldHave_CorrectState()
{
    var order = Order.Create(customerId: 1);

    order.Should().NotBeNull();
    order.Status.Should().Be(OrderStatus.Pending);
    order.Items.Should().BeEmpty();
    order.CreatedAt.Should().BeCloseTo(DateTime.UtcNow, TimeSpan.FromSeconds(5));
}
```

---

<a id="p10-moq"></a>
### Topic 3: Mocking with Moq

```csharp
// ── Basic Mocking ──────────────────────────────────────
var mockRepo = new Mock<IOrderRepository>();

// Setup return value
mockRepo.Setup(r => r.GetByIdAsync(1, It.IsAny<CancellationToken>()))
        .ReturnsAsync(new Order { Id = 1, CustomerId = 100 });

// Setup — any matching argument
mockRepo.Setup(r => r.ExistsAsync(It.IsAny<int>(), It.IsAny<CancellationToken>()))
        .ReturnsAsync(true);

// Setup — throw exception
mockRepo.Setup(r => r.GetByIdAsync(999, It.IsAny<CancellationToken>()))
        .ThrowsAsync(new NotFoundException("Order not found"));

// ── Verify calls ──────────────────────────────────────
mockRepo.Verify(r => r.AddAsync(
    It.Is<Order>(o => o.CustomerId == 100),
    It.IsAny<CancellationToken>()), Times.Once);

mockRepo.Verify(r => r.DeleteAsync(It.IsAny<int>(), It.IsAny<CancellationToken>()),
    Times.Never);

// ── Callback — capture arguments ─────────────────────
Order? savedOrder = null;
mockRepo.Setup(r => r.AddAsync(It.IsAny<Order>(), It.IsAny<CancellationToken>()))
        .Callback<Order, CancellationToken>((o, _) => savedOrder = o)
        .ReturnsAsync((Order o, CancellationToken _) => o);

// After act:
Assert.Equal(100, savedOrder?.CustomerId);

// ── Mock HttpClient ───────────────────────────────────
// dotnet add package RichardSzalay.MockHttp

var mockHttp = new MockHttpMessageHandler();
mockHttp.When("https://api.example.com/products/*")
        .Respond("application/json",
            JsonSerializer.Serialize(new ProductDto { Id = 1, Name = "Widget" }));

var client  = mockHttp.ToHttpClient();
client.BaseAddress = new Uri("https://api.example.com");

var service = new ExternalProductService(client);
var result  = await service.GetProductAsync(1);
Assert.Equal("Widget", result?.Name);

// ── Mock ILogger ──────────────────────────────────────
var mockLogger = new Mock<ILogger<OrderService>>();

// Verify a warning was logged:
mockLogger.Verify(
    x => x.Log(
        LogLevel.Warning,
        It.IsAny<EventId>(),
        It.Is<It.IsAnyType>((v, _) => v.ToString()!.Contains("not found")),
        It.IsAny<Exception?>(),
        It.IsAny<Func<It.IsAnyType, Exception?, string>>()),
    Times.Once);
```

---

<a id="p10-integration"></a>
### Topic 4: Integration Testing — WebApplicationFactory

```csharp
// dotnet add package Microsoft.AspNetCore.Mvc.Testing

// ── Custom factory ────────────────────────────────────
public class TestWebAppFactory : WebApplicationFactory<Program>
{
    protected override void ConfigureWebHost(IWebHostBuilder builder)
    {
        builder.ConfigureServices(services =>
        {
            // Replace real DB with in-memory
            var dbDescriptor = services.SingleOrDefault(
                d => d.ServiceType == typeof(DbContextOptions<AppDbContext>));
            if (dbDescriptor is not null)
                services.Remove(dbDescriptor);

            services.AddDbContext<AppDbContext>(opts =>
                opts.UseInMemoryDatabase("TestDb_" + Guid.NewGuid()));

            // Replace external services with fakes
            services.AddScoped<IEmailService, FakeEmailService>();

            // Seed test data
            var sp = services.BuildServiceProvider();
            using var scope = sp.CreateScope();
            var db = scope.ServiceProvider.GetRequiredService<AppDbContext>();
            db.Database.EnsureCreated();
            SeedTestData(db);
        });
    }

    private static void SeedTestData(AppDbContext db)
    {
        db.Customers.Add(new Customer { Id = 1, Name = "Test User", Email = "test@test.com" });
        db.Products.Add(new Product { Id = 1, Name = "Widget", Price = 10m, Stock = 100 });
        db.SaveChanges();
    }
}

// ── Integration test ──────────────────────────────────
public class OrdersEndpointTests : IClassFixture<TestWebAppFactory>
{
    private readonly HttpClient _client;

    public OrdersEndpointTests(TestWebAppFactory factory)
    {
        _client = factory.CreateClient();
    }

    [Fact]
    public async Task GetOrder_ExistingId_Returns200WithOrder()
    {
        var response = await _client.GetAsync("/api/orders/1");

        response.StatusCode.Should().Be(HttpStatusCode.OK);
        var order = await response.Content.ReadFromJsonAsync<OrderDto>();
        order.Should().NotBeNull();
        order!.Id.Should().Be(1);
    }

    [Fact]
    public async Task CreateOrder_ValidPayload_Returns201()
    {
        var dto = new CreateOrderDto
        {
            CustomerId = 1,
            Items = new[] { new OrderItemDto(ProductId: 1, Quantity: 2) }
        };

        var response = await _client.PostAsJsonAsync("/api/orders", dto);

        response.StatusCode.Should().Be(HttpStatusCode.Created);
        response.Headers.Location.Should().NotBeNull();
    }

    [Fact]
    public async Task CreateOrder_InvalidPayload_Returns400()
    {
        var response = await _client.PostAsJsonAsync("/api/orders",
            new CreateOrderDto()); // empty/invalid

        response.StatusCode.Should().Be(HttpStatusCode.BadRequest);
    }
}

// ── Authenticated requests ────────────────────────────
public class AuthenticatedTestFactory : TestWebAppFactory
{
    protected override void ConfigureWebHost(IWebHostBuilder builder)
    {
        base.ConfigureWebHost(builder);
        builder.ConfigureTestServices(services =>
        {
            services.AddAuthentication("Test")
                .AddScheme<AuthenticationSchemeOptions, TestAuthHandler>("Test", _ => { });
        });
    }
}

public class TestAuthHandler : AuthenticationHandler<AuthenticationSchemeOptions>
{
    protected override Task<AuthenticateResult> HandleAuthenticateAsync()
    {
        var claims = new[] { new Claim(ClaimTypes.Name, "testuser"),
                             new Claim(ClaimTypes.Role, "Admin") };
        var identity  = new ClaimsIdentity(claims, "Test");
        var principal = new ClaimsPrincipal(identity);
        var ticket    = new AuthenticationTicket(principal, "Test");
        return Task.FromResult(AuthenticateResult.Success(ticket));
    }
}
```

---

<a id="p10-testcontainers"></a>
### Topic 5: TestContainers — Real DB in Tests

```csharp
// dotnet add package Testcontainers.PostgreSql
// dotnet add package Testcontainers.MsSql

public class PostgreSqlIntegrationTests : IAsyncLifetime
{
    private readonly PostgreSqlContainer _postgres = new PostgreSqlBuilder()
        .WithImage("postgres:16-alpine")
        .WithDatabase("testdb")
        .WithUsername("test")
        .WithPassword("test")
        .Build();

    private AppDbContext _db = null!;

    public async Task InitializeAsync()
    {
        await _postgres.StartAsync();

        var options = new DbContextOptionsBuilder<AppDbContext>()
            .UseNpgsql(_postgres.GetConnectionString())
            .Options;

        _db = new AppDbContext(options);
        await _db.Database.MigrateAsync(); // run real migrations
    }

    public async Task DisposeAsync()
    {
        await _db.DisposeAsync();
        await _postgres.DisposeAsync();
    }

    [Fact]
    public async Task Insert_And_Query_Product_Works()
    {
        // Arrange
        var product = new Product { Name = "Widget", Price = 9.99m, Stock = 50 };
        _db.Products.Add(product);
        await _db.SaveChangesAsync();

        // Act
        var fetched = await _db.Products.FindAsync(product.Id);

        // Assert
        fetched.Should().NotBeNull();
        fetched!.Name.Should().Be("Widget");
        fetched.Price.Should().Be(9.99m);
    }

    [Fact]
    public async Task Complex_Query_With_Joins_Returns_Correct_Results()
    {
        // Seed
        var customer = new Customer { Name = "Alice", Email = "alice@test.com" };
        _db.Customers.Add(customer);
        await _db.SaveChangesAsync();

        var order = new Order { CustomerId = customer.Id, Status = "Pending",
            Items = new List<OrderItem> { new() { ProductId = 1, Quantity = 2, UnitPrice = 9.99m } } };
        _db.Orders.Add(order);
        await _db.SaveChangesAsync();

        // Test complex LINQ query
        var result = await _db.Orders
            .Include(o => o.Customer)
            .Include(o => o.Items)
            .Where(o => o.Customer.Email == "alice@test.com")
            .FirstOrDefaultAsync();

        result.Should().NotBeNull();
        result!.Items.Should().HaveCount(1);
    }
}
```

---

<a id="p10-coverage"></a>
### Topic 6: Test Coverage

```bash
# dotnet test with coverage
dotnet test --collect:"XPlat Code Coverage"

# Generate HTML report
# dotnet tool install -g dotnet-reportgenerator-globaltool
reportgenerator \
  -reports:"**/coverage.cobertura.xml" \
  -targetdir:"coveragereport" \
  -reporttypes:Html

# Coverage thresholds in .csproj
# <PropertyGroup>
#   <CoverageThreshold>80</CoverageThreshold>
# </PropertyGroup>
```

```xml
<!-- .runsettings — coverage configuration -->
<?xml version="1.0" encoding="utf-8" ?>
<RunSettings>
  <DataCollectionRunSettings>
    <DataCollectors>
      <DataCollector friendlyName="XPlat Code Coverage">
        <Configuration>
          <Format>cobertura</Format>
          <Exclude>[*.Tests]*,[*.IntegrationTests]*</Exclude>
          <ExcludeByAttribute>GeneratedCodeAttribute,ExcludeFromCodeCoverageAttribute</ExcludeByAttribute>
        </Configuration>
      </DataCollector>
    </DataCollectors>
  </DataCollectionRunSettings>
</RunSettings>
```

```csharp
// Exclude from coverage — generated/trivial code
[ExcludeFromCodeCoverage]
public class AutoGeneratedMappingProfile : Profile { }
```

---

<a id="p10-logging"></a>
### Topic 7: Logging — ILogger, Serilog, Structured Logging

```csharp
// ── ILogger — built-in ────────────────────────────────
public class OrderService
{
    private readonly ILogger<OrderService> _logger;

    public OrderService(ILogger<OrderService> logger) => _logger = logger;

    public async Task<Order> CreateAsync(CreateOrderDto dto)
    {
        _logger.LogInformation("Creating order for customer {CustomerId}", dto.CustomerId);

        try
        {
            var order = await _repo.AddAsync(dto);

            // Structured logging — searchable properties
            _logger.LogInformation(
                "Order {OrderId} created for customer {CustomerId}. Total: {Total:C}",
                order.Id, dto.CustomerId, order.TotalAmount);

            return order;
        }
        catch (Exception ex)
        {
            _logger.LogError(ex,
                "Failed to create order for customer {CustomerId}", dto.CustomerId);
            throw;
        }
    }
}

// Log levels:
// LogTrace    → very detailed, rarely used in production
// LogDebug    → debug info, disabled in production
// LogInformation → general flow
// LogWarning  → unexpected, recoverable situation
// LogError    → failure, action required
// LogCritical → system failure, immediate attention

// ── Serilog ───────────────────────────────────────────
// dotnet add package Serilog.AspNetCore
// dotnet add package Serilog.Sinks.Console
// dotnet add package Serilog.Sinks.File
// dotnet add package Serilog.Sinks.Seq        (dev dashboard)
// dotnet add package Serilog.Sinks.ApplicationInsights

Log.Logger = new LoggerConfiguration()
    .MinimumLevel.Information()
    .MinimumLevel.Override("Microsoft.AspNetCore", LogEventLevel.Warning)
    .MinimumLevel.Override("Microsoft.EntityFrameworkCore.Database.Command", LogEventLevel.Warning)
    .Enrich.FromLogContext()
    .Enrich.WithEnvironmentName()
    .Enrich.WithMachineName()
    .WriteTo.Console(new JsonFormatter())   // JSON in production
    .WriteTo.File(
        path: "logs/app-.log",
        rollingInterval: RollingInterval.Day,
        retainedFileCountLimit: 14,
        formatter: new JsonFormatter())
    .WriteTo.Seq("http://localhost:5341")   // dev
    .CreateLogger();

builder.Host.UseSerilog();

// Request logging middleware:
app.UseSerilogRequestLogging(opts =>
{
    opts.MessageTemplate = "{RequestMethod} {RequestPath} responded {StatusCode} in {Elapsed:0.0000}ms";
    opts.EnrichDiagnosticContext = (diagnosticContext, httpContext) =>
    {
        diagnosticContext.Set("RequestHost", httpContext.Request.Host.Value);
        diagnosticContext.Set("UserAgent",   httpContext.Request.Headers["User-Agent"]);
        diagnosticContext.Set("UserId",      httpContext.User.FindFirstValue("sub"));
    };
});

// ── Log Scopes — correlation ID ──────────────────────
using (_logger.BeginScope(new Dictionary<string, object>
    { ["OrderId"] = orderId, ["CustomerId"] = customerId }))
{
    _logger.LogInformation("Processing payment");
    await _payment.ChargeAsync(orderId);
    _logger.LogInformation("Payment completed");
    // Both logs include OrderId and CustomerId
}
```

---

<a id="p10-debugging"></a>
### Topic 8: Debugging Tips

```csharp
// ── Conditional Breakpoints ───────────────────────────
// VS → Breakpoint → Conditions → "order.TotalAmount > 1000"
// Useful for catching specific cases without stopping every iteration

// ── Exception Breakpoints ─────────────────────────────
// VS → Debug → Windows → Exception Settings
// Check "Common Language Runtime Exceptions" → stops on any exception

// ── Debug Watch Expressions ───────────────────────────
// orders.Where(o => o.Status == "Pending").Count()
// items.Sum(i => i.UnitPrice * i.Quantity)

// ── DebuggerDisplay attribute ─────────────────────────
[DebuggerDisplay("Order #{Id} - {Status} ({TotalAmount:C})")]
public class Order
{
    public int    Id          { get; set; }
    public string Status      { get; set; } = "";
    public decimal TotalAmount { get; set; }
}
```

```bash
# ── dotnet-trace — CPU profiling ─────────────────────
dotnet tool install -g dotnet-trace
dotnet trace collect --process-id <PID> --duration 00:00:30
dotnet trace convert trace.nettrace --format speedscope
# Open speedscope.app → find hot paths

# ── dotnet-dump — memory analysis ────────────────────
dotnet tool install -g dotnet-dump
dotnet dump collect --process-id <PID>
dotnet dump analyze core_*

# Inside analyzer:
# dumpheap -stat         → objects by type
# gcroot <address>       → find GC roots
# dumpobj <address>      → inspect object

# ── dotnet-counters — live metrics ───────────────────
dotnet tool install -g dotnet-counters
dotnet counters monitor --process-id <PID> \
  System.Runtime Microsoft.AspNetCore.Hosting

# Key counters:
# cpu-usage            → CPU %
# gc-heap-size         → memory
# exception-count      → exceptions/sec
# requests-per-second  → throughput
# request-failed-rate  → error rate

# ── HTTP diagnostics ──────────────────────────────────
# appsettings.Development.json
# "Logging": { "LogLevel": { "Microsoft.AspNetCore": "Debug" } }
```

---

<a id="p10-profiling"></a>
### Topic 9: Performance Profiling

```csharp
// ── BenchmarkDotNet ───────────────────────────────────
// dotnet add package BenchmarkDotNet

[MemoryDiagnoser]
[SimpleJob(RuntimeMoniker.Net80)]
public class StringConcatBenchmarks
{
    private const int N = 10_000;

    [Benchmark(Baseline = true)]
    public string StringConcat()
    {
        var result = "";
        for (var i = 0; i < N; i++) result += i.ToString();
        return result;
    }

    [Benchmark]
    public string StringBuilder()
    {
        var sb = new StringBuilder();
        for (var i = 0; i < N; i++) sb.Append(i);
        return sb.ToString();
    }

    [Benchmark]
    public string StringJoin() =>
        string.Join("", Enumerable.Range(0, N));
}

// Run: dotnet run -c Release
// Output: Mean, Error, StdDev, Gen0 GC, Alloc

// ── Activity/Distributed Tracing ─────────────────────
using var activity = Activity.Current?.Source
    .StartActivity("ProcessOrder", ActivityKind.Internal);
activity?.SetTag("order.id", orderId);
activity?.SetTag("customer.id", customerId);

// OpenTelemetry:
// dotnet add package OpenTelemetry.AspNetCore
builder.Services.AddOpenTelemetry()
    .WithTracing(trace => trace
        .AddAspNetCoreInstrumentation()
        .AddEntityFrameworkCoreInstrumentation()
        .AddHttpClientInstrumentation()
        .AddOtlpExporter()); // Jaeger, Zipkin, Grafana Tempo
```

---

<a id="p10-bestpractices"></a>
### Topic 10: Testing Best Practices

```
Testing Pyramid:
────────────────────────────────────────────────────────
          /‾‾‾‾‾‾‾‾‾‾‾‾\
         /  E2E Tests    \    ← Few, slow, expensive
        /‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾\
       / Integration Tests \  ← Some, medium speed
      /‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾\
     /     Unit Tests        \ ← Many, fast, cheap
    /‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾‾\
────────────────────────────────────────────────────────
```

```csharp
// ✅ Good Test Design Rules:

// 1. One assert per test (ideally)
// 2. Test behavior, not implementation
// 3. Tests must be deterministic (no DateTime.Now, Guid.NewGuid without seeding)
// 4. Avoid testing private methods directly
// 5. Name: MethodName_Scenario_ExpectedResult

// ✅ Use test doubles correctly:
// Stub  → returns canned data  (no verification)
// Mock  → verifiable expectations
// Fake  → working implementation  (in-memory repo)
// Spy   → records calls for later verification

// ✅ Avoid common pitfalls:
// ❌  Assert.True(result == expected)   → use Assert.Equal
// ❌  Thread.Sleep in tests            → use Task.Delay or mock time
// ❌  Sharing state between tests      → IClassFixture isolation
// ❌  Testing framework code           → trust EF Core, test your code
// ❌  Mocking everything               → integration tests for the full flow

// ✅ Time abstraction for deterministic tests:
public interface IDateTimeProvider
{
    DateTime UtcNow { get; }
}

public class DateTimeProvider : IDateTimeProvider
{
    public DateTime UtcNow => DateTime.UtcNow;
}

// In tests:
var mockTime = new Mock<IDateTimeProvider>();
mockTime.Setup(t => t.UtcNow).Returns(new DateTime(2025, 1, 1, 12, 0, 0));
```

---

## PART 10 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| xUnit | `[Fact]`, `[Theory]`, `[InlineData]` |
| NUnit | `[Test]`, `[TestCase]`, `[SetUp]`, `[TearDown]` |
| AAA | Arrange → Act → Assert |
| `IClassFixture<T>` | Shared setup across test class |
| Moq | `Mock<T>`, `.Setup()`, `.Returns()`, `.Verify()` |
| FluentAssertions | `.Should().Be()` — readable assertions |
| WebApplicationFactory | Real HTTP integration tests in-process |
| TestContainers | Real Docker DB — real migrations in tests |
| `ILogger` | Built-in .NET logging abstraction |
| Serilog | Structured logging — JSON, sinks, enrichers |
| Log Scopes | Correlation ID across multiple log entries |
| dotnet-trace | CPU profiling with flame graph |
| dotnet-dump | Memory dump analysis |
| dotnet-counters | Live CPU, GC, requests per second |
| BenchmarkDotNet | Microbenchmarks — Mean, Alloc |
| OpenTelemetry | Distributed tracing — Jaeger, Grafana |
| Testing Pyramid | Many unit → some integration → few E2E |

---

## PART 10 Interview Q&A

```
প্রশ্ন: Unit Test আর Integration Test পার্থক্য?
উত্তর:
Unit Test     → Single class/method। Dependencies মক করা।
               Fast (milliseconds)। External dependency নেই।
Integration Test → Multiple components। Real DB/HTTP।
               Slower। WebApplicationFactory দিয়ে in-process।

প্রশ্ন: Moq-এ Setup আর Verify-এর পার্থক্য?
উত্তর:
Setup  → mock method কী return করবে define করে।
Verify → method actually কতবার call হয়েছে তা check করে।
Setup ছাড়া Verify করলে mock default value return করে।

প্রশ্ন: TestContainers কেন ব্যবহার করবেন?
উত্তর:
InMemory DB → EF Core-specific bugs miss করে, SQL syntax check নেই।
TestContainers → Real PostgreSQL/SQL Server Docker container।
Real migrations, real SQL — production-like behavior।
Slow কিন্তু reliable integration tests-এর জন্য ideal।

প্রশ্ন: Structured logging কী?
উত্তর:
Plain text: "Order 123 created for customer 456"
Structured: { OrderId: 123, CustomerId: 456, Action: "OrderCreated" }

Structured → searchable, filterable in Seq/Kibana/Application Insights।
_logger.LogInformation("Order {OrderId} created", orderId) — Serilog captures
OrderId as a property, not just a string।

প্রশ্ন: BenchmarkDotNet কখন ব্যবহার করবেন?
উত্তর: Performance-critical code-এ micro-benchmark।
String operations, LINQ vs loops, serialization।
-c Release mode-এ run করতে হয়।
[MemoryDiagnoser] → allocation tracking।
Never use Stopwatch for benchmarks — JIT warm-up, GC noise।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 11 — Deployment ও DevOps (Docker, Kubernetes, Azure, CI/CD, GitHub Actions এবং আরও...)

---

<a id="part11"></a>
## PART 11: Deployment ও DevOps Basics

> Docker, Kubernetes, Azure App Service, CI/CD, GitHub Actions, Health Checks, Environment Management।

| # | বিষয় |
|---|-------|
| 1 | [Docker — Containerize .NET App](#p11-docker) |
| 2 | [Docker Compose — Multi-container](#p11-compose) |
| 3 | [GitHub Actions — CI/CD Pipeline](#p11-gha) |
| 4 | [Azure App Service Deployment](#p11-azure) |
| 5 | [Kubernetes Basics (K8s)](#p11-k8s) |
| 6 | [Environment & Configuration Management](#p11-config) |
| 7 | [Health Checks & Readiness Probes](#p11-health) |
| 8 | [Secrets Management](#p11-secrets) |

---

<a id="p11-docker"></a>
### Topic 1: Docker — Containerize .NET App

```dockerfile
# ── Multi-stage Dockerfile (production best practice) ─
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src

# Copy only project files first → layer caching
COPY ["src/MyApp.Api/MyApp.Api.csproj",              "src/MyApp.Api/"]
COPY ["src/MyApp.Application/MyApp.Application.csproj", "src/MyApp.Application/"]
COPY ["src/MyApp.Domain/MyApp.Domain.csproj",        "src/MyApp.Domain/"]
COPY ["src/MyApp.Infrastructure/MyApp.Infrastructure.csproj", "src/MyApp.Infrastructure/"]
RUN dotnet restore "src/MyApp.Api/MyApp.Api.csproj"

# Copy source and build
COPY . .
WORKDIR "/src/src/MyApp.Api"
RUN dotnet build -c Release -o /app/build --no-restore

# Publish
FROM build AS publish
RUN dotnet publish -c Release -o /app/publish \
    --no-restore \
    /p:UseAppHost=false

# Final runtime image (smaller — no SDK)
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS final
WORKDIR /app
EXPOSE 8080

# Security: non-root user
RUN addgroup --system appgroup && adduser --system --ingroup appgroup appuser
USER appuser

COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "MyApp.Api.dll"]
```

```bash
# Build & run
docker build -t myapp:latest .
docker run -p 8080:8080 \
  -e ASPNETCORE_ENVIRONMENT=Production \
  -e ConnectionStrings__Default="Server=db;Database=myapp;..." \
  myapp:latest

# Tag & push to registry
docker tag myapp:latest myregistry.azurecr.io/myapp:1.0.0
docker push myregistry.azurecr.io/myapp:1.0.0

# Inspect running container
docker logs <container-id> --tail 50 -f
docker exec -it <container-id> sh
docker stats                        # live resource usage
```

```json
// .dockerignore — keep image small
{
  "files": [
    ".git", ".gitignore",
    "**/bin", "**/obj",
    "**/*.md",
    "tests/", "**/*.Tests",
    ".env", "docker-compose.override.yml"
  ]
}
```

---

<a id="p11-compose"></a>
### Topic 2: Docker Compose — Multi-container

```yaml
# docker-compose.yml — development environment
version: '3.9'

services:
  api:
    build:
      context: .
      dockerfile: src/MyApp.Api/Dockerfile
    ports:
      - "8080:8080"
    environment:
      - ASPNETCORE_ENVIRONMENT=Development
      - ConnectionStrings__Default=Host=db;Database=myapp;Username=app;Password=secret
      - Redis__Connection=redis:6379
    depends_on:
      db:
        condition: service_healthy
      redis:
        condition: service_started
    restart: unless-stopped
    volumes:
      - ./logs:/app/logs

  db:
    image: postgres:16-alpine
    environment:
      POSTGRES_DB:       myapp
      POSTGRES_USER:     app
      POSTGRES_PASSWORD: secret
    ports:
      - "5432:5432"
    volumes:
      - postgres_data:/var/lib/postgresql/data
    healthcheck:
      test: ["CMD-SHELL", "pg_isready -U app -d myapp"]
      interval: 5s
      timeout: 5s
      retries: 10

  redis:
    image: redis:7-alpine
    ports:
      - "6379:6379"
    command: redis-server --appendonly yes
    volumes:
      - redis_data:/data

  seq:
    image: datalust/seq:latest
    ports:
      - "5341:80"
    environment:
      ACCEPT_EULA: Y
    volumes:
      - seq_data:/data

volumes:
  postgres_data:
  redis_data:
  seq_data:
```

```bash
docker compose up -d          # start all services
docker compose logs api -f    # tail API logs
docker compose ps             # status
docker compose down -v        # stop + remove volumes (careful!)
docker compose exec api sh    # shell into API container
```

---

<a id="p11-gha"></a>
### Topic 3: GitHub Actions — CI/CD Pipeline

```yaml
# .github/workflows/ci-cd.yml
name: CI/CD Pipeline

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

env:
  REGISTRY:    ghcr.io
  IMAGE_NAME:  ${{ github.repository }}
  DOTNET_VERSION: '8.0.x'

jobs:
  # ── 1. Build & Test ──────────────────────────────────
  test:
    name: Build & Test
    runs-on: ubuntu-latest

    services:
      postgres:
        image: postgres:16-alpine
        env:
          POSTGRES_DB:       testdb
          POSTGRES_USER:     test
          POSTGRES_PASSWORD: test
        ports: ["5432:5432"]
        options: >-
          --health-cmd pg_isready
          --health-interval 10s
          --health-retries 5

    steps:
      - uses: actions/checkout@v4

      - name: Setup .NET
        uses: actions/setup-dotnet@v4
        with:
          dotnet-version: ${{ env.DOTNET_VERSION }}

      - name: Cache NuGet packages
        uses: actions/cache@v4
        with:
          path: ~/.nuget/packages
          key: ${{ runner.os }}-nuget-${{ hashFiles('**/*.csproj') }}
          restore-keys: ${{ runner.os }}-nuget-

      - name: Restore dependencies
        run: dotnet restore

      - name: Build
        run: dotnet build --no-restore -c Release

      - name: Run tests
        run: dotnet test --no-build -c Release \
          --collect:"XPlat Code Coverage" \
          --results-directory ./coverage
        env:
          ConnectionStrings__TestDb: Host=localhost;Database=testdb;Username=test;Password=test

      - name: Upload coverage
        uses: codecov/codecov-action@v4
        with:
          directory: ./coverage

  # ── 2. Build & Push Docker Image ─────────────────────
  docker:
    name: Build & Push Image
    needs: test
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'
    permissions:
      contents: read
      packages: write

    steps:
      - uses: actions/checkout@v4

      - name: Log in to Container Registry
        uses: docker/login-action@v3
        with:
          registry: ${{ env.REGISTRY }}
          username: ${{ github.actor }}
          password: ${{ secrets.GITHUB_TOKEN }}

      - name: Extract metadata
        id: meta
        uses: docker/metadata-action@v5
        with:
          images: ${{ env.REGISTRY }}/${{ env.IMAGE_NAME }}
          tags: |
            type=sha,prefix=sha-
            type=raw,value=latest

      - name: Build and push
        uses: docker/build-push-action@v5
        with:
          context: .
          push: true
          tags: ${{ steps.meta.outputs.tags }}
          cache-from: type=gha
          cache-to:   type=gha,mode=max

  # ── 3. Deploy to Azure ───────────────────────────────
  deploy:
    name: Deploy to Azure
    needs: docker
    runs-on: ubuntu-latest
    environment: production

    steps:
      - name: Deploy to Azure Web App
        uses: azure/webapps-deploy@v3
        with:
          app-name:     ${{ vars.AZURE_APP_NAME }}
          publish-profile: ${{ secrets.AZURE_PUBLISH_PROFILE }}
          images:       ${{ env.REGISTRY }}/${{ env.IMAGE_NAME }}:latest
```

---

<a id="p11-azure"></a>
### Topic 4: Azure App Service Deployment

```bash
# ── Azure CLI deployment ──────────────────────────────
az login
az group create --name myapp-rg --location eastus

# Create App Service Plan (Linux)
az appservice plan create \
  --name myapp-plan \
  --resource-group myapp-rg \
  --sku B1 \
  --is-linux

# Create Web App (Docker)
az webapp create \
  --resource-group myapp-rg \
  --plan myapp-plan \
  --name myapp-api \
  --deployment-container-image-name mcr.microsoft.com/dotnet/samples:aspnetapp

# Set environment variables
az webapp config appsettings set \
  --resource-group myapp-rg \
  --name myapp-api \
  --settings \
    ASPNETCORE_ENVIRONMENT=Production \
    "ConnectionStrings__Default=Server=...;Database=myapp;"

# Deploy via zip (no Docker)
dotnet publish -c Release -o ./publish
cd publish && zip -r ../app.zip . && cd ..
az webapp deploy \
  --resource-group myapp-rg \
  --name myapp-api \
  --src-path app.zip

# Enable logging
az webapp log config \
  --resource-group myapp-rg \
  --name myapp-api \
  --docker-container-logging filesystem

# Stream live logs
az webapp log tail --resource-group myapp-rg --name myapp-api
```

```csharp
// Program.cs — production-ready startup
var builder = WebApplication.CreateBuilder(args);

// Azure App Configuration (centralized config)
if (builder.Environment.IsProduction())
{
    builder.Configuration.AddAzureAppConfiguration(options =>
        options.Connect(builder.Configuration["AzureAppConfig:ConnectionString"])
               .UseFeatureFlags());
}

// Azure Application Insights telemetry
builder.Services.AddApplicationInsightsTelemetry(
    builder.Configuration["ApplicationInsights:ConnectionString"]);
```

---

<a id="p11-k8s"></a>
### Topic 5: Kubernetes Basics (K8s)

```yaml
# deployment.yml — app deployment
apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp-api
  namespace: production
  labels:
    app: myapp-api
spec:
  replicas: 3
  selector:
    matchLabels:
      app: myapp-api
  strategy:
    type: RollingUpdate
    rollingUpdate:
      maxSurge: 1
      maxUnavailable: 0     # zero-downtime deploy
  template:
    metadata:
      labels:
        app: myapp-api
    spec:
      containers:
        - name: api
          image: ghcr.io/myorg/myapp:sha-abc1234
          ports:
            - containerPort: 8080
          env:
            - name: ASPNETCORE_ENVIRONMENT
              value: Production
            - name: ConnectionStrings__Default
              valueFrom:
                secretKeyRef:
                  name: myapp-secrets
                  key: db-connection-string
          resources:
            requests:
              memory: "256Mi"
              cpu:    "250m"
            limits:
              memory: "512Mi"
              cpu:    "500m"
          # Health probes
          livenessProbe:
            httpGet:
              path: /health/live
              port: 8080
            initialDelaySeconds: 10
            periodSeconds:       15
          readinessProbe:
            httpGet:
              path: /health/ready
              port: 8080
            initialDelaySeconds: 5
            periodSeconds:       10

---
# service.yml — internal load balancer
apiVersion: v1
kind: Service
metadata:
  name: myapp-api-svc
spec:
  selector:
    app: myapp-api
  ports:
    - port: 80
      targetPort: 8080
  type: ClusterIP

---
# ingress.yml — external access
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: myapp-ingress
  annotations:
    nginx.ingress.kubernetes.io/rewrite-target: /
spec:
  rules:
    - host: api.myapp.com
      http:
        paths:
          - path: /
            pathType: Prefix
            backend:
              service:
                name: myapp-api-svc
                port:
                  number: 80
```

```bash
# Common kubectl commands:
kubectl apply -f deployment.yml        # deploy/update
kubectl get pods -n production         # list pods
kubectl logs <pod-name> -f             # live logs
kubectl describe pod <pod-name>        # debug events
kubectl exec -it <pod-name> -- sh      # shell
kubectl rollout status deployment/myapp-api
kubectl rollout undo deployment/myapp-api    # rollback
kubectl scale deployment myapp-api --replicas=5
```

---

<a id="p11-config"></a>
### Topic 6: Environment & Configuration Management

```csharp
// ── Configuration hierarchy (later overrides earlier) ─
// appsettings.json
// appsettings.{Environment}.json
// Environment variables (ASPNETCORE_ prefix → nested)
// User secrets (development only)
// Command line args

// appsettings.json
{
  "App": {
    "Name": "MyApp",
    "MaxPageSize": 100
  },
  "ConnectionStrings": {
    "Default": "placeholder"
  }
}

// Environment variable override:
// ConnectionStrings__Default="Server=prod.db;..."
// App__MaxPageSize=50

// ── Options pattern ───────────────────────────────────
public class AppSettings
{
    public const string Section = "App";
    public string Name        { get; init; } = "";
    public int    MaxPageSize  { get; init; } = 50;
}

builder.Services.Configure<AppSettings>(
    builder.Configuration.GetSection(AppSettings.Section));

// Usage:
public class ProductController
{
    private readonly AppSettings _settings;
    public ProductController(IOptions<AppSettings> opts) =>
        _settings = opts.Value;
}

// IOptionsMonitor — reloads on change (no restart)
// IOptionsSnapshot — per-request snapshot
// IOptions        — singleton, no reload

// ── User Secrets (dev only) ───────────────────────────
// dotnet user-secrets init
// dotnet user-secrets set "ConnectionStrings:Default" "Server=localhost;..."
// Stored in: ~/.microsoft/usersecrets/<guid>/secrets.json

// ── .NET 8 — named environments ──────────────────────
// ASPNETCORE_ENVIRONMENT: Development | Staging | Production
// Custom: QA, UAT, etc.

if (app.Environment.IsEnvironment("QA"))
{
    app.UseSwagger(); // only in QA
}
```

---

<a id="p11-health"></a>
### Topic 7: Health Checks ও Readiness Probes

```csharp
// dotnet add package AspNetCore.HealthChecks.NpgSql
// dotnet add package AspNetCore.HealthChecks.Redis
// dotnet add package AspNetCore.HealthChecks.Uris

builder.Services.AddHealthChecks()
    .AddNpgSql(
        connectionString: builder.Configuration.GetConnectionString("Default")!,
        name: "database",
        tags: new[] { "db", "ready" })
    .AddRedis(
        redisConnectionString: builder.Configuration["Redis:Connection"]!,
        name: "redis",
        tags: new[] { "cache", "ready" })
    .AddUrlGroup(
        uri: new Uri("https://api.payment.com/health"),
        name: "payment-gateway",
        tags: new[] { "external" })
    .AddCheck<CustomApplicationHealthCheck>("app-logic",
        tags: new[] { "ready" });

// Map endpoints:
app.MapHealthChecks("/health/live", new HealthCheckOptions
{
    // Liveness → is the process alive?
    Predicate = _ => false,   // no checks — just "I'm alive"
    ResponseWriter = WriteResponse
});

app.MapHealthChecks("/health/ready", new HealthCheckOptions
{
    // Readiness → can I serve traffic?
    Predicate = check => check.Tags.Contains("ready"),
    ResponseWriter = WriteResponse
});

app.MapHealthChecks("/health/full", new HealthCheckOptions
{
    ResponseWriter = WriteResponse
});

// JSON response writer:
static Task WriteResponse(HttpContext ctx, HealthReport report)
{
    ctx.Response.ContentType = "application/json; charset=utf-8";
    var result = JsonSerializer.Serialize(new
    {
        status   = report.Status.ToString(),
        duration = report.TotalDuration.TotalMilliseconds,
        checks   = report.Entries.Select(e => new
        {
            name     = e.Key,
            status   = e.Value.Status.ToString(),
            duration = e.Value.Duration.TotalMilliseconds,
            error    = e.Value.Exception?.Message
        })
    });
    return ctx.Response.WriteAsync(result);
}

// Custom health check:
public class CustomApplicationHealthCheck : IHealthCheck
{
    private readonly AppDbContext _db;
    public CustomApplicationHealthCheck(AppDbContext db) => _db = db;

    public async Task<HealthCheckResult> CheckHealthAsync(
        HealthCheckContext context, CancellationToken ct)
    {
        try
        {
            // Test a critical query
            var count = await _db.Orders
                .Where(o => o.CreatedAt > DateTime.UtcNow.AddMinutes(-1))
                .CountAsync(ct);

            return HealthCheckResult.Healthy($"Recent orders: {count}");
        }
        catch (Exception ex)
        {
            return HealthCheckResult.Unhealthy("Database query failed", ex);
        }
    }
}
```

---

<a id="p11-secrets"></a>
### Topic 8: Secrets Management

```csharp
// ── Development: User Secrets ─────────────────────────
// dotnet user-secrets set "Jwt:Secret" "dev-secret-32-chars-long"
// Never commit secrets to git

// ── Production: Azure Key Vault ──────────────────────
// dotnet add package Azure.Extensions.AspNetCore.Configuration.Secrets
// dotnet add package Azure.Identity

if (builder.Environment.IsProduction())
{
    var keyVaultUri = new Uri(builder.Configuration["KeyVault:Uri"]!);
    builder.Configuration.AddAzureKeyVault(
        keyVaultUri,
        new DefaultAzureCredential()); // Managed Identity — no credentials in code!
}

// Secret naming in Key Vault: "ConnectionStrings--Default" → "ConnectionStrings:Default"

// ── AWS Secrets Manager ───────────────────────────────
// Similar pattern with AWSSDK.SecretsManager

// ── Environment Variable injection (Docker/K8s) ───────
// K8s Secret:
// kubectl create secret generic myapp-secrets \
//   --from-literal=db-connection-string="Server=prod;..."
//
// Pod spec references via secretKeyRef (shown in K8s section)

// ── GitHub Actions Secrets ────────────────────────────
// Repository → Settings → Secrets
// ${{ secrets.MY_SECRET }} in workflow YAML
// Never echo or print secrets in logs

// ── .gitignore — critical files ──────────────────────
/*
appsettings.*.Local.json
.env
.env.local
secrets.json
*.pfx
*.p12
*/
```

---

## PART 11 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| Multi-stage Dockerfile | SDK build → runtime final (smaller image) |
| `.dockerignore` | bin/, obj/, .git → faster builds, smaller image |
| `docker compose` | Local multi-service dev environment |
| GitHub Actions | CI/CD — test → build → push → deploy |
| `actions/cache` | NuGet cache → faster builds |
| Azure App Service | PaaS — easy deployment, auto-scaling |
| Deployment slot | Staging → swap to production (zero-downtime) |
| K8s Deployment | Declarative pod management, rolling update |
| K8s Service | Internal load balancing across pods |
| K8s Ingress | External HTTP routing (nginx/traefik) |
| liveness probe | Is the pod alive? Restart if unhealthy |
| readiness probe | Can the pod serve traffic? Remove from LB |
| Options pattern | `IOptions<T>`, `IOptionsMonitor<T>` |
| User Secrets | Dev-only local secrets (not committed) |
| Azure Key Vault | Production secrets — Managed Identity |
| Health Checks | `/health/live`, `/health/ready` endpoints |
| `DefaultAzureCredential` | Managed Identity — no hardcoded credentials |

---

## PART 11 Interview Q&A

```
প্রশ্ন: Multi-stage Dockerfile-এর সুবিধা কী?
উত্তর: Final image-এ শুধু runtime (.NET aspnet)।
SDK image (~700MB) vs runtime (~200MB)।
Build tools, source code, intermediate files → production image-এ নেই।
Security surface কমে। Pull ও startup faster।

প্রশ্ন: liveness probe আর readiness probe পার্থক্য?
উত্তর:
liveness  → pod জীবিত আছে? Fail হলে K8s restart করে।
             /health/live → always return 200 (process running)
readiness → traffic নিতে পারবে? Fail হলে load balancer সরিয়ে দেয়।
             /health/ready → DB, Redis, dependencies check করে।
Startup-এ DB connect হওয়ার আগেই liveness pass কিন্তু readiness fail।

প্রশ্ন: Zero-downtime deployment কীভাবে করবেন?
উত্তর:
K8s: RollingUpdate strategy। maxUnavailable: 0 → নতুন pod ready হলে পুরোনো সরে।
Azure: Deployment slots — staging slot-এ deploy → swap।
       Both: Readiness probe সফল না হলে traffic যায় না।

প্রশ্ন: Secrets কীভাবে manage করবেন?
উত্তর:
Dev     → User Secrets (dotnet user-secrets) — never committed।
CI/CD   → GitHub Actions Secrets (${{ secrets.* }})।
Production → Azure Key Vault + Managed Identity।
             DefaultAzureCredential → no hardcoded credentials।
Never:  → appsettings.json-এ production secrets।
        → environment variables in Dockerfile।
        → .env files committed to git।

প্রশ্ন: GitHub Actions CI/CD-এ কী কী steps থাকা উচিত?
উত্তর:
1. Checkout code
2. Setup .NET SDK
3. Restore + cache NuGet
4. Build (Release)
5. Run tests (coverage)
6. Docker build + push (on main only)
7. Deploy to environment
PR → শুধু build + test। Main merge → full deploy।
Environment secrets → production-only deployment।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 12 — System Design with .NET (Microservices, DDD, CQRS, Event Sourcing, Clean Architecture এবং আরও...)

---

<a id="part12"></a>
## PART 12: System Design with .NET

> Clean Architecture, DDD, CQRS, Event Sourcing, Microservices, API Gateway, Saga Pattern।

| # | বিষয় |
|---|-------|
| 1 | [Clean Architecture](#p12-clean) |
| 2 | [Domain-Driven Design (DDD)](#p12-ddd) |
| 3 | [CQRS Pattern](#p12-cqrs) |
| 4 | [MediatR — in-process messaging](#p12-mediatr) |
| 5 | [Event Sourcing](#p12-eventsourcing) |
| 6 | [Microservices Architecture](#p12-microservices) |
| 7 | [API Gateway Pattern](#p12-gateway) |
| 8 | [Saga Pattern — distributed transactions](#p12-saga) |

---

<a id="p12-clean"></a>
### Topic 1: Clean Architecture

```
Clean Architecture Layers:
────────────────────────────────────────────────────────
  ┌─────────────────────────────────────────────┐
  │  Presentation (API, Controllers, Blazor)    │
  │  ┌─────────────────────────────────────┐    │
  │  │  Infrastructure (EF Core, Redis,    │    │
  │  │  Email, File Storage, External APIs)│    │
  │  │  ┌───────────────────────────────┐  │    │
  │  │  │  Application (Use Cases,      │  │    │
  │  │  │  Commands, Queries, DTOs,     │  │    │
  │  │  │  Interfaces, Validators)      │  │    │
  │  │  │  ┌─────────────────────────┐  │  │    │
  │  │  │  │  Domain (Entities,      │  │  │    │
  │  │  │  │  Value Objects, Events, │  │  │    │
  │  │  │  │  Aggregates, Rules)     │  │  │    │
  │  │  │  └─────────────────────────┘  │  │    │
  │  │  └───────────────────────────────┘  │    │
  │  └─────────────────────────────────────┘    │
  └─────────────────────────────────────────────┘
  Dependency direction: Inward only
  Domain knows nothing about outer layers
────────────────────────────────────────────────────────
```

```csharp
// ── Folder structure ──────────────────────────────────
// MyApp.Domain/
//   Entities/Order.cs, Product.cs
//   ValueObjects/Money.cs, Address.cs
//   Events/OrderCreatedEvent.cs
//   Interfaces/IRepository.cs           ← abstract contract
//   Exceptions/DomainException.cs

// MyApp.Application/
//   Orders/Commands/CreateOrder/
//     CreateOrderCommand.cs
//     CreateOrderCommandHandler.cs
//     CreateOrderCommandValidator.cs
//   Orders/Queries/GetOrder/
//     GetOrderQuery.cs
//     GetOrderQueryHandler.cs
//     OrderDto.cs
//   Common/Interfaces/IAppDbContext.cs

// MyApp.Infrastructure/
//   Persistence/AppDbContext.cs         ← implements IAppDbContext
//   Repositories/OrderRepository.cs    ← implements IRepository
//   Services/EmailService.cs

// MyApp.Api/
//   Controllers/OrdersController.cs
//   Program.cs

// ── Domain Entity ─────────────────────────────────────
public class Order : BaseEntity
{
    public int    CustomerId  { get; private set; }
    public Money  TotalAmount { get; private set; } = Money.Zero;
    public OrderStatus Status { get; private set; } = OrderStatus.Pending;

    private readonly List<OrderItem> _items = new();
    public IReadOnlyCollection<OrderItem> Items => _items.AsReadOnly();

    private readonly List<IDomainEvent> _events = new();
    public IReadOnlyCollection<IDomainEvent> DomainEvents => _events.AsReadOnly();

    // Private constructor — use factory method
    private Order() { }

    public static Order Create(int customerId)
    {
        Guard.Against.NegativeOrZero(customerId, nameof(customerId));
        var order = new Order { CustomerId = customerId };
        order._events.Add(new OrderCreatedEvent(order.Id, customerId));
        return order;
    }

    public void AddItem(Product product, int quantity)
    {
        Guard.Against.NegativeOrZero(quantity, nameof(quantity));
        if (Status != OrderStatus.Pending)
            throw new DomainException("Cannot add items to a non-pending order");

        var item = new OrderItem(product.Id, quantity, product.Price);
        _items.Add(item);
        TotalAmount = TotalAmount.Add(product.Price.Multiply(quantity));
    }

    public void Submit()
    {
        if (!_items.Any())
            throw new DomainException("Cannot submit empty order");
        Status = OrderStatus.Submitted;
        _events.Add(new OrderSubmittedEvent(Id, CustomerId, TotalAmount));
    }

    public void ClearDomainEvents() => _events.Clear();
}

// ── Value Object ─────────────────────────────────────
public record Money(decimal Amount, string Currency)
{
    public static readonly Money Zero = new(0, "BDT");

    public Money Add(Money other)
    {
        if (Currency != other.Currency)
            throw new DomainException("Cannot add different currencies");
        return new Money(Amount + other.Amount, Currency);
    }

    public Money Multiply(int qty) => new(Amount * qty, Currency);
}

// ── Application interface (ports) ────────────────────
public interface IAppDbContext
{
    DbSet<Order>   Orders   { get; }
    DbSet<Product> Products { get; }
    Task<int> SaveChangesAsync(CancellationToken ct);
}
```

---

<a id="p12-ddd"></a>
### Topic 2: Domain-Driven Design (DDD)

```
DDD Building Blocks:
────────────────────────────────────────────────────────
Entity          → Identity দিয়ে distinguish। Order, Customer।
Value Object    → Equality by value। Money, Address, Email।
Aggregate       → Consistency boundary। Order + OrderItems।
Aggregate Root  → Aggregate-এর entry point। Order only।
Domain Event    → Something happened। OrderCreated, OrderShipped।
Repository      → Aggregate persistence abstraction।
Domain Service  → Logic যা single entity-তে fit করে না।
Factory         → Complex aggregate creation।
Bounded Context → একটি domain model-এর boundary।
────────────────────────────────────────────────────────
```

```csharp
// ── Aggregate example ─────────────────────────────────
// Order is Aggregate Root. Access OrderItems only through Order.
// Never: orderItemRepository.Add(item) — go through Order.AddItem()

// ── Domain Service — cross-aggregate logic ────────────
public class PricingDomainService
{
    public Money CalculateOrderTotal(Order order, IReadOnlyList<Discount> discounts)
    {
        var subtotal = order.Items
            .Aggregate(Money.Zero, (sum, item) => sum.Add(item.LineTotal));

        var applicableDiscount = discounts
            .Where(d => d.IsApplicableTo(order))
            .OrderByDescending(d => d.Amount)
            .FirstOrDefault();

        return applicableDiscount is not null
            ? subtotal.Subtract(applicableDiscount.Amount)
            : subtotal;
    }
}

// ── Domain Events — dispatch after SaveChanges ────────
public class AppDbContext : DbContext
{
    private readonly IPublisher _publisher;

    public override async Task<int> SaveChangesAsync(CancellationToken ct)
    {
        var result = await base.SaveChangesAsync(ct);

        // Dispatch domain events after persisting
        var events = ChangeTracker.Entries<BaseEntity>()
            .SelectMany(e => e.Entity.DomainEvents)
            .ToList();

        foreach (var @event in events)
        {
            ChangeTracker.Entries<BaseEntity>()
                .ToList()
                .ForEach(e => e.Entity.ClearDomainEvents());
            await _publisher.Publish(@event, ct);
        }

        return result;
    }
}

// ── Ubiquitous Language ───────────────────────────────
// Code uses same terms as domain experts:
// "Submit order" not "ChangeOrderStatusToSubmitted"
// "Cancel" not "SetStatusCancelled"
// Use domain vocabulary in class, method, variable names

// ── Bounded Contexts ─────────────────────────────────
// OrderManagement BC → Order, OrderItem, OrderStatus
// Inventory BC       → Product, StockLevel, Reservation
// Billing BC         → Invoice, Payment, Refund
// Each BC has its own DB schema, its own Order concept
```

---

<a id="p12-cqrs"></a>
### Topic 3: CQRS Pattern

```
CQRS — Command Query Responsibility Segregation:
────────────────────────────────────────────────────────
Command → Write side। State change। Returns void/id।
           CreateOrderCommand, CancelOrderCommand
Query   → Read side। No state change। Returns data।
           GetOrderQuery, ListOrdersQuery

Benefits:
  - Read/write independently scaled and optimized
  - Read model = denormalized, fast SELECT
  - Write model = normalized, domain logic enforced
────────────────────────────────────────────────────────
```

```csharp
// ── Command ───────────────────────────────────────────
public record CreateOrderCommand(int CustomerId, List<OrderItemDto> Items)
    : IRequest<int>;  // returns created Order Id

public class CreateOrderCommandHandler : IRequestHandler<CreateOrderCommand, int>
{
    private readonly IAppDbContext _db;
    private readonly IMapper _mapper;

    public CreateOrderCommandHandler(IAppDbContext db, IMapper mapper)
    {
        _db     = db;
        _mapper = mapper;
    }

    public async Task<int> Handle(CreateOrderCommand request, CancellationToken ct)
    {
        var order = Order.Create(request.CustomerId);

        foreach (var item in request.Items)
        {
            var product = await _db.Products.FindAsync(new object[] { item.ProductId }, ct)
                ?? throw new NotFoundException(nameof(Product), item.ProductId);
            order.AddItem(product, item.Quantity);
        }

        _db.Orders.Add(order);
        await _db.SaveChangesAsync(ct);
        return order.Id;
    }
}

// ── Query ─────────────────────────────────────────────
public record GetOrderByIdQuery(int Id) : IRequest<OrderDetailDto?>;

public class GetOrderByIdQueryHandler : IRequestHandler<GetOrderByIdQuery, OrderDetailDto?>
{
    private readonly IAppDbContext _db;
    private readonly IMapper _mapper;

    public async Task<OrderDetailDto?> Handle(GetOrderByIdQuery request, CancellationToken ct)
    {
        // Read side: project directly to DTO — skip domain model
        return await _db.Orders
            .AsNoTracking()
            .Where(o => o.Id == request.Id)
            .ProjectTo<OrderDetailDto>(_mapper.ConfigurationProvider)
            .FirstOrDefaultAsync(ct);
    }
}

// ── Controller ────────────────────────────────────────
[ApiController, Route("api/[controller]")]
public class OrdersController : ControllerBase
{
    private readonly ISender _mediator;
    public OrdersController(ISender mediator) => _mediator = mediator;

    [HttpPost]
    public async Task<IActionResult> Create([FromBody] CreateOrderCommand command,
        CancellationToken ct)
    {
        var id = await _mediator.Send(command, ct);
        return CreatedAtAction(nameof(GetById), new { id }, null);
    }

    [HttpGet("{id:int}")]
    public async Task<ActionResult<OrderDetailDto>> GetById(int id, CancellationToken ct)
    {
        var result = await _mediator.Send(new GetOrderByIdQuery(id), ct);
        return result is null ? NotFound() : Ok(result);
    }
}
```

---

<a id="p12-mediatr"></a>
### Topic 4: MediatR — in-process messaging

```csharp
// dotnet add package MediatR
// dotnet add package MediatR.Extensions.Microsoft.DependencyInjection
// (or FluentValidation.DependencyInjectionExtensions)

builder.Services.AddMediatR(cfg =>
    cfg.RegisterServicesFromAssembly(typeof(CreateOrderCommand).Assembly));

// ── Pipeline Behaviors ────────────────────────────────
// Cross-cutting concerns: logging, validation, caching

// 1. Validation behavior (FluentValidation)
public class ValidationBehavior<TRequest, TResponse>
    : IPipelineBehavior<TRequest, TResponse>
    where TRequest : notnull
{
    private readonly IEnumerable<IValidator<TRequest>> _validators;

    public ValidationBehavior(IEnumerable<IValidator<TRequest>> validators)
        => _validators = validators;

    public async Task<TResponse> Handle(TRequest request,
        RequestHandlerDelegate<TResponse> next, CancellationToken ct)
    {
        if (!_validators.Any()) return await next();

        var context = new ValidationContext<TRequest>(request);
        var failures = _validators
            .Select(v => v.Validate(context))
            .SelectMany(r => r.Errors)
            .Where(f => f is not null)
            .ToList();

        if (failures.Any())
            throw new ValidationException(failures);

        return await next();
    }
}

// 2. Logging behavior
public class LoggingBehavior<TRequest, TResponse>
    : IPipelineBehavior<TRequest, TResponse>
    where TRequest : notnull
{
    private readonly ILogger<LoggingBehavior<TRequest, TResponse>> _logger;

    public async Task<TResponse> Handle(TRequest request,
        RequestHandlerDelegate<TResponse> next, CancellationToken ct)
    {
        var name = typeof(TRequest).Name;
        _logger.LogInformation("Handling {Request}: {@RequestData}", name, request);
        var sw = Stopwatch.StartNew();
        try
        {
            var response = await next();
            _logger.LogInformation(
                "Handled {Request} in {Elapsed}ms", name, sw.ElapsedMilliseconds);
            return response;
        }
        catch (Exception ex)
        {
            _logger.LogError(ex, "Error handling {Request}", name);
            throw;
        }
    }
}

// Register behaviors:
builder.Services.AddMediatR(cfg =>
{
    cfg.RegisterServicesFromAssembly(typeof(CreateOrderCommand).Assembly);
    cfg.AddBehavior(typeof(IPipelineBehavior<,>), typeof(LoggingBehavior<,>));
    cfg.AddBehavior(typeof(IPipelineBehavior<,>), typeof(ValidationBehavior<,>));
});

// FluentValidation:
public class CreateOrderCommandValidator : AbstractValidator<CreateOrderCommand>
{
    public CreateOrderCommandValidator()
    {
        RuleFor(c => c.CustomerId).GreaterThan(0);
        RuleFor(c => c.Items).NotEmpty();
        RuleForEach(c => c.Items).ChildRules(item =>
        {
            item.RuleFor(i => i.ProductId).GreaterThan(0);
            item.RuleFor(i => i.Quantity).InclusiveBetween(1, 100);
        });
    }
}
```

---

<a id="p12-eventsourcing"></a>
### Topic 5: Event Sourcing

```
Event Sourcing:
────────────────────────────────────────────────────────
Traditional:  Save current state → UPDATE orders SET status='Shipped'
Event Sourcing: Save events  → INSERT: OrderCreated, ItemAdded, OrderShipped

Benefits:
  - Complete audit log — who did what, when
  - Temporal queries — state at any point in time
  - Event replay — rebuild projections
  - CQRS natural fit

Concepts:
  Event Store  → append-only log of all events
  Projection   → current state built by replaying events
  Snapshot     → optimization — periodically persist state
────────────────────────────────────────────────────────
```

```csharp
// ── Domain Events ─────────────────────────────────────
public abstract record DomainEvent(Guid EventId, DateTime OccurredAt)
{
    protected DomainEvent() : this(Guid.NewGuid(), DateTime.UtcNow) { }
}

public record OrderCreatedEvent(int OrderId, int CustomerId) : DomainEvent;
public record OrderItemAddedEvent(int OrderId, int ProductId, int Qty, decimal Price) : DomainEvent;
public record OrderSubmittedEvent(int OrderId, decimal Total) : DomainEvent;
public record OrderShippedEvent(int OrderId, string TrackingNumber) : DomainEvent;

// ── Event-sourced Aggregate ───────────────────────────
public class EventSourcedOrder
{
    public int    Id         { get; private set; }
    public int    CustomerId { get; private set; }
    public string Status     { get; private set; } = "Pending";
    public decimal Total     { get; private set; }

    private readonly List<DomainEvent> _uncommittedEvents = new();

    // Rebuild from events (replay)
    public static EventSourcedOrder Rehydrate(IEnumerable<DomainEvent> events)
    {
        var order = new EventSourcedOrder();
        foreach (var e in events) order.Apply(e);
        return order;
    }

    public void Create(int customerId)
    {
        var @event = new OrderCreatedEvent(Id, customerId);
        Apply(@event);
        _uncommittedEvents.Add(@event);
    }

    public void Ship(string trackingNumber)
    {
        if (Status != "Submitted")
            throw new DomainException("Only submitted orders can be shipped");
        var @event = new OrderShippedEvent(Id, trackingNumber);
        Apply(@event);
        _uncommittedEvents.Add(@event);
    }

    // Apply — pure state transition, no side effects
    private void Apply(DomainEvent @event)
    {
        switch (@event)
        {
            case OrderCreatedEvent e:
                Id         = e.OrderId;
                CustomerId = e.CustomerId;
                Status     = "Pending";
                break;
            case OrderSubmittedEvent e:
                Status = "Submitted";
                Total  = e.Total;
                break;
            case OrderShippedEvent:
                Status = "Shipped";
                break;
        }
    }

    public IReadOnlyList<DomainEvent> GetUncommittedEvents() =>
        _uncommittedEvents.AsReadOnly();
    public void ClearUncommittedEvents() => _uncommittedEvents.Clear();
}

// ── Event Store ───────────────────────────────────────
public class EventStore
{
    private readonly AppDbContext _db;

    public async Task AppendAsync(int aggregateId, IEnumerable<DomainEvent> events,
        int expectedVersion, CancellationToken ct)
    {
        var currentVersion = await _db.EventStore
            .CountAsync(e => e.AggregateId == aggregateId, ct);

        if (currentVersion != expectedVersion)
            throw new ConcurrencyException($"Expected version {expectedVersion}, got {currentVersion}");

        foreach (var @event in events)
        {
            _db.EventStore.Add(new StoredEvent
            {
                AggregateId = aggregateId,
                EventType   = @event.GetType().Name,
                Payload     = JsonSerializer.Serialize(@event),
                OccurredAt  = @event.OccurredAt,
                Version     = ++currentVersion
            });
        }
        await _db.SaveChangesAsync(ct);
    }

    public async Task<IEnumerable<DomainEvent>> GetEventsAsync(int aggregateId,
        CancellationToken ct)
    {
        return await _db.EventStore
            .Where(e => e.AggregateId == aggregateId)
            .OrderBy(e => e.Version)
            .Select(e => Deserialize(e.EventType, e.Payload))
            .ToListAsync(ct);
    }
}
```

---

<a id="p12-microservices"></a>
### Topic 6: Microservices Architecture

```
Microservices — .NET Context:
────────────────────────────────────────────────────────
Services:
  OrderService    → orders DB (PostgreSQL)
  ProductService  → products DB (PostgreSQL)
  PaymentService  → payments DB (PostgreSQL)
  NotificationService → sends emails/SMS

Communication:
  Synchronous  → gRPC (internal), REST (external)
  Asynchronous → Message Bus (RabbitMQ, Azure Service Bus)

Each service:
  - Own DB (database-per-service)
  - Own deployment (Docker container)
  - Independent scaling
  - Independent deploy
────────────────────────────────────────────────────────
```

```csharp
// ── Service communication via HTTP ───────────────────
public class ProductServiceClient
{
    private readonly HttpClient _http;

    public ProductServiceClient(HttpClient http) => _http = http;

    public async Task<ProductDto?> GetProductAsync(int id, CancellationToken ct)
    {
        try
        {
            return await _http.GetFromJsonAsync<ProductDto>($"/api/products/{id}", ct);
        }
        catch (HttpRequestException ex) when (ex.StatusCode == HttpStatusCode.NotFound)
        {
            return null;
        }
    }

    public async Task<bool> ReserveStockAsync(int productId, int quantity,
        CancellationToken ct)
    {
        var response = await _http.PostAsJsonAsync(
            $"/api/products/{productId}/reserve",
            new { quantity }, ct);
        return response.IsSuccessStatusCode;
    }
}

// Register:
builder.Services.AddHttpClient<ProductServiceClient>(client =>
{
    client.BaseAddress = new Uri(builder.Configuration["Services:ProductService"]!);
}).AddStandardResilienceHandler();

// ── Service Discovery (Kubernetes) ───────────────────
// K8s DNS: http://product-service.default.svc.cluster.local
// appsettings.Production.json:
// "Services": { "ProductService": "http://product-service" }

// ── Async messaging ───────────────────────────────────
// OrderService publishes: OrderCreated event
// ProductService subscribes → decrements stock
// NotificationService subscribes → sends confirmation email
// PaymentService subscribes → initiates charge
```

---

<a id="p12-gateway"></a>
### Topic 7: API Gateway Pattern

```yaml
# YARP (Yet Another Reverse Proxy) — .NET API Gateway
# dotnet add package Yarp.ReverseProxy

# appsettings.json
{
  "ReverseProxy": {
    "Routes": {
      "orders-route": {
        "ClusterId": "orders-cluster",
        "Match": { "Path": "/api/orders/{**catch-all}" }
      },
      "products-route": {
        "ClusterId": "products-cluster",
        "Match": { "Path": "/api/products/{**catch-all}" }
      }
    },
    "Clusters": {
      "orders-cluster": {
        "Destinations": {
          "primary": { "Address": "http://order-service" }
        }
      },
      "products-cluster": {
        "Destinations": {
          "primary": { "Address": "http://product-service" }
        }
      }
    }
  }
}
```

```csharp
// Program.cs — API Gateway
builder.Services.AddReverseProxy()
    .LoadFromConfig(builder.Configuration.GetSection("ReverseProxy"));

// Add auth at gateway level
builder.Services.AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
    .AddJwtBearer(/* ... */);

app.UseAuthentication();
app.UseAuthorization();

// Custom middleware — rate limiting, request enrichment
app.Use(async (context, next) =>
{
    // Add correlation ID to forward to downstream services
    context.Request.Headers["X-Correlation-Id"] =
        context.TraceIdentifier;
    await next();
});

app.MapReverseProxy();
```

---

<a id="p12-saga"></a>
### Topic 8: Saga Pattern — distributed transactions

```
Saga Pattern:
────────────────────────────────────────────────────────
Problem: Microservices — no distributed ACID transactions।
         Order → Reserve Stock → Charge Payment → Send Email
         What if Payment fails? Need to undo Stock Reservation।

Saga types:
  Choreography → Events drive flow। No central coordinator।
                 Each service reacts to events।
                 
  Orchestration → Central saga orchestrator।
                  MassTransit StateMachine, Temporal।

Compensating Transactions: Undo completed steps on failure।
────────────────────────────────────────────────────────
```

```csharp
// ── Orchestration Saga (MassTransit StateMachine) ─────
// dotnet add package MassTransit.RabbitMQ

public class OrderSagaState : SagaStateMachineInstance
{
    public Guid  CorrelationId  { get; set; }
    public string CurrentState  { get; set; } = "";
    public int   OrderId        { get; set; }
    public int   CustomerId     { get; set; }
    public bool  StockReserved  { get; set; }
    public bool  PaymentCharged { get; set; }
}

public class OrderSaga : MassTransitStateMachine<OrderSagaState>
{
    public State AwaitingStockReservation { get; private set; } = null!;
    public State AwaitingPayment          { get; private set; } = null!;
    public State Completed                { get; private set; } = null!;
    public State Failed                   { get; private set; } = null!;

    public Event<OrderSubmittedEvent>      OrderSubmitted      { get; private set; } = null!;
    public Event<StockReservedEvent>       StockReserved       { get; private set; } = null!;
    public Event<StockReservationFailed>   StockFailed         { get; private set; } = null!;
    public Event<PaymentChargedEvent>      PaymentCharged      { get; private set; } = null!;
    public Event<PaymentFailedEvent>       PaymentFailed       { get; private set; } = null!;

    public OrderSaga()
    {
        InstanceState(x => x.CurrentState);

        Event(() => OrderSubmitted,  x => x.CorrelateById(m => m.Message.CorrelationId));
        Event(() => StockReserved,   x => x.CorrelateById(m => m.Message.CorrelationId));
        Event(() => PaymentCharged,  x => x.CorrelateById(m => m.Message.CorrelationId));
        Event(() => PaymentFailed,   x => x.CorrelateById(m => m.Message.CorrelationId));

        Initially(
            When(OrderSubmitted)
                .Then(ctx =>
                {
                    ctx.Saga.OrderId    = ctx.Message.OrderId;
                    ctx.Saga.CustomerId = ctx.Message.CustomerId;
                })
                .Publish(ctx => new ReserveStockCommand(ctx.Saga.CorrelationId, ctx.Saga.OrderId))
                .TransitionTo(AwaitingStockReservation));

        During(AwaitingStockReservation,
            When(StockReserved)
                .Then(ctx => ctx.Saga.StockReserved = true)
                .Publish(ctx => new ChargePaymentCommand(ctx.Saga.CorrelationId, ctx.Saga.OrderId))
                .TransitionTo(AwaitingPayment),
            When(StockFailed)
                .Publish(ctx => new CancelOrderCommand(ctx.Saga.OrderId, "Stock unavailable"))
                .TransitionTo(Failed));

        During(AwaitingPayment,
            When(PaymentCharged)
                .Then(ctx => ctx.Saga.PaymentCharged = true)
                .Publish(ctx => new SendOrderConfirmationCommand(ctx.Saga.OrderId))
                .TransitionTo(Completed),
            When(PaymentFailed)
                // Compensate: release stock
                .Publish(ctx => new ReleaseStockCommand(ctx.Saga.OrderId))
                .Publish(ctx => new CancelOrderCommand(ctx.Saga.OrderId, "Payment failed"))
                .TransitionTo(Failed));
    }
}
```

---

## PART 12 Quick Revision Table

| Concept | মূল কথা |
|---------|---------|
| Clean Architecture | Domain → Application → Infrastructure → Presentation |
| Dependency Rule | Dependencies point inward only |
| Entity | ID-based identity। Mutable state। |
| Value Object | Value equality। Immutable। `record` in C#। |
| Aggregate Root | Consistency boundary entry point |
| Domain Event | Something happened in domain — `OrderCreated` |
| Bounded Context | Domain model-এর isolated boundary |
| CQRS | Command (write) + Query (read) separation |
| Command | State change, returns id/void |
| Query | Read only, returns DTO |
| MediatR | in-process `ISender.Send()` dispatch |
| Pipeline Behavior | Cross-cutting — validation, logging, caching |
| Event Sourcing | State = replay of all events |
| Event Store | Append-only event log |
| Microservices | DB-per-service, independent deploy |
| YARP | .NET reverse proxy / API Gateway |
| Saga | Distributed transaction coordination |
| Compensating Transaction | Undo on failure |
| Choreography Saga | Event-driven, no coordinator |
| Orchestration Saga | Central state machine (MassTransit) |

---

## PART 12 Interview Q&A

```
প্রশ্ন: Clean Architecture-এ layer কীভাবে কাজ করে?
উত্তর: Dependency rule: শুধু inward।
Domain → কাউকে চেনে না।
Application → শুধু Domain।
Infrastructure → Application interface implement করে।
Presentation → Application commands/queries send করে।
Interface (IOrderRepository) Application-এ। Implementation Infrastructure-এ।

প্রশ্ন: CQRS কেন ব্যবহার করবেন?
উত্তর:
Read আর Write pattern আলাদা।
Write → complex domain logic, validation, transaction।
Read → fast projection, JOIN, DTO directly।
Separately scale করা যায়। Read replica।
MediatR দিয়ে Controller slim রাখা যায়।

প্রশ্ন: Event Sourcing আর traditional persistence-এর পার্থক্য?
উত্তর:
Traditional: Current state store। History হারিয়ে যায়।
Event Sourcing: All events store। Current state = replay।
Audit log free। Time travel queries।
Complex — snapshot ছাড়া replay slow হতে পারে।
কোথায়: Financial systems, compliance-heavy domains।

প্রশ্ন: Saga কেন দরকার?
উত্তর: Microservices-এ distributed ACID transaction নেই।
Order → Stock → Payment — যেকোনো step fail হতে পারে।
Saga → compensating transactions দিয়ে consistency।
Orchestration (MassTransit StateMachine) → central coordinator।
Choreography → events-driven, decoupled।

প্রশ্ন: Bounded Context কী?
উত্তর: একই শব্দের আলাদা meaning আলাদা context-এ।
Order: OrderService-এ → items, total, status।
Order: BillingService-এ → invoice, payment terms।
দুটো context নিজেদের Order model maintain করে।
Anti-Corruption Layer (ACL) দিয়ে boundaries cross করে।
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 13 — .NET Projects (Portfolio Projects with Full Source Code...)

---

<a id="part13"></a>
## PART 13: .NET Portfolio Projects

> Interview-এ দেখানোর জন্য ৫টি real-world project — structure, key code patterns, এবং what to highlight।

| # | Project | Stack | Difficulty |
|---|---------|-------|-----------|
| 1 | [REST API — E-Commerce Backend](#p13-ecom) | ASP.NET Core + EF Core + PostgreSQL | ⭐⭐ |
| 2 | [Clean Architecture — Task Manager](#p13-task) | Clean Arch + CQRS + MediatR | ⭐⭐⭐ |
| 3 | [Real-time Chat App](#p13-chat) | SignalR + React + Redis | ⭐⭐⭐ |
| 4 | [Microservices — Order System](#p13-micro) | .NET + Docker + RabbitMQ | ⭐⭐⭐⭐ |
| 5 | [Full Stack — Job Board](#p13-jobboard) | ASP.NET Core + Blazor + Azure | ⭐⭐⭐ |

---

<a id="p13-ecom"></a>
### Project 1: REST API — E-Commerce Backend

**GitHub-এ দেখানোর মতো কী আছে:**
- JWT Authentication + Refresh Tokens
- Role-based Authorization (Admin, Customer)
- EF Core migrations + seeding
- Generic Repository + Unit of Work
- FluentValidation + global error handling
- Swagger/OpenAPI documentation
- Pagination, filtering, sorting

```
Project Structure:
ECommerceApi/
├── Controllers/
│   ├── AuthController.cs       ← login, register, refresh
│   ├── ProductsController.cs   ← CRUD + search + pagination
│   ├── OrdersController.cs     ← create, list, cancel
│   └── AdminController.cs      ← admin-only endpoints
├── Models/
│   ├── Entities/               ← Product, Order, User, Category
│   └── DTOs/                   ← Request/Response DTOs
├── Services/
│   ├── AuthService.cs
│   ├── OrderService.cs
│   └── EmailService.cs
├── Repositories/
│   ├── IRepository.cs          ← generic interface
│   ├── Repository.cs           ← generic EF implementation
│   └── IUnitOfWork.cs
├── Data/
│   ├── AppDbContext.cs
│   └── Migrations/
├── Middleware/
│   └── ExceptionHandlingMiddleware.cs
└── Program.cs
```

```csharp
// ── Generic Repository ────────────────────────────────
public interface IRepository<T> where T : BaseEntity
{
    Task<T?> GetByIdAsync(int id, CancellationToken ct = default);
    Task<IReadOnlyList<T>> GetAllAsync(CancellationToken ct = default);
    Task<IReadOnlyList<T>> GetAsync(Expression<Func<T, bool>> predicate,
        CancellationToken ct = default);
    Task AddAsync(T entity, CancellationToken ct = default);
    void Update(T entity);
    void Remove(T entity);
}

public class Repository<T> : IRepository<T> where T : BaseEntity
{
    protected readonly AppDbContext _db;
    protected readonly DbSet<T> _set;

    public Repository(AppDbContext db)
    {
        _db  = db;
        _set = db.Set<T>();
    }

    public async Task<T?> GetByIdAsync(int id, CancellationToken ct)
        => await _set.FindAsync(new object[] { id }, ct);

    public async Task<IReadOnlyList<T>> GetAsync(
        Expression<Func<T, bool>> predicate, CancellationToken ct)
        => await _set.Where(predicate).AsNoTracking().ToListAsync(ct);

    public async Task AddAsync(T entity, CancellationToken ct)
        => await _set.AddAsync(entity, ct);

    public void Update(T entity) => _set.Update(entity);
    public void Remove(T entity) => _set.Remove(entity);

    public async Task<IReadOnlyList<T>> GetAllAsync(CancellationToken ct)
        => await _set.AsNoTracking().ToListAsync(ct);
}

// ── Pagination ────────────────────────────────────────
public record PagedResult<T>(
    IReadOnlyList<T> Items,
    int TotalCount,
    int Page,
    int PageSize)
{
    public int TotalPages => (int)Math.Ceiling(TotalCount / (double)PageSize);
    public bool HasNextPage => Page < TotalPages;
    public bool HasPreviousPage => Page > 1;
}

public static class QueryableExtensions
{
    public static async Task<PagedResult<T>> ToPagedResultAsync<T>(
        this IQueryable<T> query, int page, int pageSize, CancellationToken ct)
    {
        var total = await query.CountAsync(ct);
        var items = await query
            .Skip((page - 1) * pageSize)
            .Take(pageSize)
            .ToListAsync(ct);
        return new PagedResult<T>(items, total, page, pageSize);
    }
}

// Usage:
[HttpGet]
public async Task<ActionResult<PagedResult<ProductDto>>> GetProducts(
    [FromQuery] int page = 1,
    [FromQuery] int pageSize = 20,
    [FromQuery] string? search = null,
    [FromQuery] string? category = null,
    CancellationToken ct = default)
{
    var query = _db.Products.AsNoTracking()
        .Where(p => p.IsActive);

    if (!string.IsNullOrEmpty(search))
        query = query.Where(p => p.Name.Contains(search) ||
                                  p.Description.Contains(search));
    if (!string.IsNullOrEmpty(category))
        query = query.Where(p => p.Category.Slug == category);

    var result = await query
        .ProjectTo<ProductDto>(_mapper.ConfigurationProvider)
        .OrderBy(p => p.Name)
        .ToPagedResultAsync(page, pageSize, ct);

    return Ok(result);
}
```

**Interview-এ বলার points:**
- Generic Repository-এ Expression<Func<T,bool>> কীভাবে কাজ করে
- JWT refresh token rotation কেন important
- PagedResult record-এ computed properties
- AsNoTracking কেন read-only queries-তে

---

<a id="p13-task"></a>
### Project 2: Clean Architecture — Task Manager API

**GitHub-এ দেখানোর মতো কী আছে:**
- Clean Architecture 4-layer structure
- CQRS + MediatR + FluentValidation
- Pipeline behaviors (logging, validation)
- Domain events + event handlers
- Result pattern (no exceptions for business errors)

```
Project Structure:
TaskManager/
├── TaskManager.Domain/
│   ├── Entities/Task.cs, Project.cs, User.cs
│   ├── ValueObjects/TaskStatus.cs, Priority.cs
│   ├── Events/TaskCreatedEvent.cs, TaskCompletedEvent.cs
│   ├── Interfaces/ITaskRepository.cs
│   └── Exceptions/DomainException.cs
├── TaskManager.Application/
│   ├── Tasks/
│   │   ├── Commands/CreateTask/, CompleteTask/, DeleteTask/
│   │   └── Queries/GetTask/, ListTasks/
│   ├── Common/
│   │   ├── Behaviors/ValidationBehavior.cs, LoggingBehavior.cs
│   │   ├── Interfaces/IAppDbContext.cs, ICurrentUser.cs
│   │   └── Models/Result.cs
│   └── DependencyInjection.cs
├── TaskManager.Infrastructure/
│   ├── Persistence/AppDbContext.cs, Migrations/
│   ├── Repositories/TaskRepository.cs
│   └── DependencyInjection.cs
└── TaskManager.Api/
    ├── Controllers/TasksController.cs
    ├── Middleware/ExceptionHandlingMiddleware.cs
    └── Program.cs
```

```csharp
// ── Result pattern — no throw for business errors ─────
public class Result<T>
{
    public bool   IsSuccess { get; }
    public T?     Value     { get; }
    public string Error     { get; }

    private Result(T value)          { IsSuccess = true;  Value = value; Error = ""; }
    private Result(string error)     { IsSuccess = false; Value = default; Error = error; }

    public static Result<T> Success(T value) => new(value);
    public static Result<T> Failure(string error) => new(error);

    public TResult Match<TResult>(Func<T, TResult> onSuccess, Func<string, TResult> onFailure)
        => IsSuccess ? onSuccess(Value!) : onFailure(Error);
}

// Domain method returns Result:
public Result<Unit> Complete(int userId)
{
    if (Status == TaskStatus.Completed)
        return Result<Unit>.Failure("Task is already completed");
    if (AssignedUserId != userId)
        return Result<Unit>.Failure("Only assigned user can complete this task");

    Status      = TaskStatus.Completed;
    CompletedAt = DateTime.UtcNow;
    _events.Add(new TaskCompletedEvent(Id, userId));
    return Result<Unit>.Success(Unit.Value);
}

// Handler uses result:
public async Task<Result<Unit>> Handle(CompleteTaskCommand cmd, CancellationToken ct)
{
    var task = await _db.Tasks.FindAsync(new object[] { cmd.TaskId }, ct);
    if (task is null) return Result<Unit>.Failure("Task not found");

    var result = task.Complete(cmd.UserId);
    if (!result.IsSuccess) return result;

    await _db.SaveChangesAsync(ct);
    return Result<Unit>.Success(Unit.Value);
}

// Controller maps to HTTP:
[HttpPatch("{id:int}/complete")]
public async Task<IActionResult> Complete(int id, CancellationToken ct)
{
    var result = await _mediator.Send(new CompleteTaskCommand(id, _currentUser.Id), ct);
    return result.Match<IActionResult>(
        _ => NoContent(),
        error => BadRequest(new { error }));
}

// ── ICurrentUser — from JWT claims ───────────────────
public interface ICurrentUser
{
    int    Id       { get; }
    string Email    { get; }
    bool   IsAdmin  { get; }
}

public class CurrentUser : ICurrentUser
{
    private readonly IHttpContextAccessor _http;
    public CurrentUser(IHttpContextAccessor http) => _http = http;

    public int    Id      => int.Parse(_http.HttpContext!.User.FindFirstValue("sub")!);
    public string Email   => _http.HttpContext!.User.FindFirstValue(ClaimTypes.Email)!;
    public bool   IsAdmin => _http.HttpContext!.User.IsInRole("Admin");
}
```

---

<a id="p13-chat"></a>
### Project 3: Real-time Chat App

**GitHub-এ দেখানোর মতো কী আছে:**
- SignalR Hub with groups (chat rooms)
- React frontend with @microsoft/signalr
- Redis backplane (multiple server instances)
- Message persistence (last 50 messages on join)
- Online presence tracking

```csharp
// ── Chat Hub ──────────────────────────────────────────
[Authorize]
public class ChatHub : Hub
{
    private readonly IChatRepository _repo;
    private readonly IConnectionTracker _tracker;

    public ChatHub(IChatRepository repo, IConnectionTracker tracker)
    {
        _repo    = repo;
        _tracker = tracker;
    }

    public override async Task OnConnectedAsync()
    {
        var userId = GetUserId();
        await _tracker.AddConnectionAsync(userId, Context.ConnectionId);
        await Clients.Others.SendAsync("UserOnline", userId);
        await base.OnConnectedAsync();
    }

    public override async Task OnDisconnectedAsync(Exception? ex)
    {
        var userId = GetUserId();
        await _tracker.RemoveConnectionAsync(userId, Context.ConnectionId);
        var isStillOnline = await _tracker.IsOnlineAsync(userId);
        if (!isStillOnline)
            await Clients.Others.SendAsync("UserOffline", userId);
        await base.OnDisconnectedAsync(ex);
    }

    public async Task JoinRoom(string roomId)
    {
        await Groups.AddToGroupAsync(Context.ConnectionId, roomId);

        // Send last 50 messages
        var history = await _repo.GetRecentMessagesAsync(roomId, count: 50);
        await Clients.Caller.SendAsync("ChatHistory", history);
    }

    public async Task SendMessage(string roomId, string content)
    {
        if (string.IsNullOrWhiteSpace(content) || content.Length > 2000)
            throw new HubException("Invalid message");

        var userId   = GetUserId();
        var userName = GetUserName();
        var msg = await _repo.SaveMessageAsync(new ChatMessage
        {
            RoomId    = roomId,
            SenderId  = userId,
            Content   = content,   // sanitized before save
            SentAt    = DateTime.UtcNow
        });

        await Clients.Group(roomId).SendAsync("NewMessage", new
        {
            msg.Id, msg.SentAt, content,
            sender = new { id = userId, name = userName }
        });
    }

    private int    GetUserId()   => int.Parse(Context.User!.FindFirstValue("sub")!);
    private string GetUserName() => Context.User!.FindFirstValue(ClaimTypes.Name)!;
}

// ── Redis backplane — scale-out ───────────────────────
builder.Services.AddSignalR()
    .AddStackExchangeRedis(builder.Configuration["Redis:Connection"]!,
        opts => opts.Configuration.ChannelPrefix = RedisChannel.Literal("chat"));
```

---

<a id="p13-micro"></a>
### Project 4: Microservices — Order System

**GitHub-এ দেখানোর মতো কী আছে:**
- 3 independent .NET services (Order, Product, Notification)
- RabbitMQ message bus (MassTransit)
- Docker Compose local dev
- Outbox pattern
- YARP API Gateway
- Distributed tracing (OpenTelemetry)

```yaml
# docker-compose.yml
services:
  gateway:
    build: ./Gateway
    ports: ["8080:8080"]
    depends_on: [order-service, product-service]

  order-service:
    build: ./OrderService
    environment:
      - ConnectionStrings__Default=Host=order-db;Database=orders;...
      - RabbitMQ__Host=rabbitmq
    depends_on: [order-db, rabbitmq]

  product-service:
    build: ./ProductService
    environment:
      - ConnectionStrings__Default=Host=product-db;Database=products;...
    depends_on: [product-db]

  notification-service:
    build: ./NotificationService
    environment:
      - RabbitMQ__Host=rabbitmq
      - Smtp__Host=mailhog
    depends_on: [rabbitmq]

  order-db:     { image: postgres:16-alpine }
  product-db:   { image: postgres:16-alpine }
  rabbitmq:     { image: rabbitmq:3-management }
  mailhog:      { image: mailhog/mailhog }
```

```csharp
// ── MassTransit setup (OrderService) ──────────────────
builder.Services.AddMassTransit(x =>
{
    x.AddConsumers(typeof(Program).Assembly);

    x.UsingRabbitMq((ctx, cfg) =>
    {
        cfg.Host(builder.Configuration["RabbitMQ:Host"], h =>
        {
            h.Username(builder.Configuration["RabbitMQ:User"]);
            h.Password(builder.Configuration["RabbitMQ:Password"]);
        });
        cfg.ConfigureEndpoints(ctx);
    });
});

// OrderService publishes:
public class OrderService
{
    private readonly IBus _bus;

    public async Task<int> CreateAsync(CreateOrderDto dto, CancellationToken ct)
    {
        var order = Order.Create(dto.CustomerId);
        // ... add items, save to DB

        await _bus.Publish(new OrderCreatedEvent
        {
            OrderId    = order.Id,
            CustomerId = order.CustomerId,
            Total      = (double)order.TotalAmount,
            Items      = order.Items.Select(i => new OrderItemDto(i.ProductId, i.Quantity)).ToList()
        }, ct);

        return order.Id;
    }
}

// NotificationService subscribes:
public class OrderCreatedConsumer : IConsumer<OrderCreatedEvent>
{
    private readonly IEmailService _email;

    public async Task Consume(ConsumeContext<OrderCreatedEvent> context)
    {
        var msg = context.Message;
        await _email.SendOrderConfirmationAsync(msg.CustomerId, msg.OrderId, msg.Total);
    }
}
```

---

<a id="p13-jobboard"></a>
### Project 5: Full Stack — Job Board (Blazor + ASP.NET Core)

**GitHub-এ দেখানোর মতো কী আছে:**
- Blazor Server UI + ASP.NET Core API
- ASP.NET Core Identity (registration, login, roles)
- Employer posts jobs → Job Seeker applies
- File upload (CV/Resume → Azure Blob Storage)
- Email notifications (application received)
- Azure deployment

```csharp
// ── Blazor component — Job Listing ───────────────────
@page "/jobs"
@inject IJobApiClient JobApi
@inject NavigationManager Nav
@inject AuthenticationStateProvider AuthState

<PageTitle>Job Listings</PageTitle>

<div class="container mt-4">
    <div class="row mb-3">
        <div class="col-md-8">
            <input class="form-control" placeholder="Search jobs..."
                   @bind="_searchTerm" @bind:event="oninput"
                   @oninput="OnSearchChanged" />
        </div>
        <div class="col-md-4">
            <select class="form-select" @bind="_selectedCategory" @bind:after="LoadJobs">
                <option value="">All Categories</option>
                @foreach (var cat in _categories)
                {
                    <option value="@cat.Id">@cat.Name</option>
                }
            </select>
        </div>
    </div>

    @if (_loading)
    {
        <div class="text-center"><div class="spinner-border"></div></div>
    }
    else
    {
        @foreach (var job in _jobs)
        {
            <div class="card mb-3">
                <div class="card-body">
                    <h5 class="card-title">@job.Title</h5>
                    <p class="text-muted">@job.CompanyName • @job.Location</p>
                    <p>@job.SalaryRange</p>
                    <button class="btn btn-primary btn-sm"
                            @onclick="() => Nav.NavigateTo($\"/jobs/{job.Id}\")">
                        View Details
                    </button>
                    @if (_isAuthenticated && _isJobSeeker)
                    {
                        <button class="btn btn-outline-success btn-sm ms-2"
                                @onclick="() => ApplyToJob(job.Id)">
                            Quick Apply
                        </button>
                    }
                </div>
            </div>
        }

        <Pagination CurrentPage="_page" TotalPages="_totalPages"
                    OnPageChanged="OnPageChanged" />
    }
</div>

@code {
    private List<JobSummaryDto> _jobs    = new();
    private List<CategoryDto>   _categories = new();
    private bool   _loading      = true;
    private bool   _isAuthenticated;
    private bool   _isJobSeeker;
    private string _searchTerm   = "";
    private string _selectedCategory = "";
    private int    _page         = 1;
    private int    _totalPages   = 1;
    private Timer? _debounceTimer;

    protected override async Task OnInitializedAsync()
    {
        var auth = await AuthState.GetAuthenticationStateAsync();
        _isAuthenticated = auth.User.Identity?.IsAuthenticated ?? false;
        _isJobSeeker     = auth.User.IsInRole("JobSeeker");

        _categories = await JobApi.GetCategoriesAsync();
        await LoadJobs();
    }

    private async Task LoadJobs()
    {
        _loading = true;
        var result = await JobApi.GetJobsAsync(_page, _searchTerm, _selectedCategory);
        _jobs       = result.Items.ToList();
        _totalPages = result.TotalPages;
        _loading    = false;
    }

    private void OnSearchChanged(ChangeEventArgs e)
    {
        _searchTerm = e.Value?.ToString() ?? "";
        _debounceTimer?.Dispose();
        _debounceTimer = new Timer(async _ =>
        {
            _page = 1;
            await InvokeAsync(async () => { await LoadJobs(); StateHasChanged(); });
        }, null, 400, Timeout.Infinite);
    }

    private async Task ApplyToJob(int jobId)
    {
        // Navigate to apply page with CV upload
        Nav.NavigateTo($"/jobs/{jobId}/apply");
    }

    private async Task OnPageChanged(int newPage)
    {
        _page = newPage;
        await LoadJobs();
    }
}

// ── File Upload — CV to Azure Blob ───────────────────
public class BlobStorageService
{
    private readonly BlobServiceClient _client;
    private readonly string _container;

    public BlobStorageService(IConfiguration config)
    {
        _client    = new BlobServiceClient(config["AzureStorage:ConnectionString"]);
        _container = config["AzureStorage:CvContainer"]!;
    }

    public async Task<string> UploadCvAsync(Stream fileStream, string fileName,
        CancellationToken ct)
    {
        // Sanitize filename
        var extension = Path.GetExtension(fileName).ToLowerInvariant();
        if (extension is not ".pdf" and not ".docx")
            throw new ValidationException("Only PDF and DOCX files allowed");

        var safeFileName = $"{Guid.NewGuid()}{extension}";
        var container    = _client.GetBlobContainerClient(_container);
        var blob         = container.GetBlobClient(safeFileName);

        await blob.UploadAsync(fileStream, new BlobHttpHeaders
        {
            ContentType = extension == ".pdf"
                ? "application/pdf"
                : "application/vnd.openxmlformats-officedocument.wordprocessingml.document"
        }, cancellationToken: ct);

        return blob.Uri.ToString();
    }
}
```

---

## PART 13 Project Checklist

| প্রতিটি Project-এ থাকা উচিত | কেন? |
|------------------------------|------|
| README with screenshots | প্রথম impression — interviewer সবার আগে দেখে |
| Architecture diagram | যে কোনো level-এর interviewer বুঝতে পারে |
| Setup instructions | `docker compose up` one command করে চালানো যায় |
| Unit + Integration tests | `dotnet test` দিয়ে pass করে |
| CI/CD (GitHub Actions) | Badge দিয়ে দেখানো যায় — passing ✅ |
| `.env.example` (no secrets) | `.env` বা secrets committed না থাকা |
| Swagger UI | `/swagger` → live API documentation |
| Proper .gitignore | `bin/`, `obj/`, `.env`, `*.pfx` committed না |

## PART 13 Interview Talking Points

```
প্রশ্ন: আপনার most complex project কোনটা?
উত্তর: (Microservices project সম্পর্কে বলুন)
"আমি একটা order management system বানিয়েছি যেখানে 3টা
independent .NET microservice আছে। RabbitMQ + MassTransit
দিয়ে async communication। Docker Compose দিয়ে local dev।
সবচেয়ে interesting challenge ছিল outbox pattern implement
করা যাতে DB save আর event publish atomic হয়।"

প্রশ্ন: Clean Architecture কেন choose করলেন?
উত্তর: "Domain logic আর infrastructure সম্পূর্ণ আলাদা।
Test করতে সুবিধা — domain আর application layer-এ
কোনো DB dependency নেই, pure unit test।
আর পরে যদি PostgreSQL থেকে MongoDB-তে যেতে হয়,
শুধু Infrastructure layer change হবে।"

প্রশ্ন: আপনার project-এ কী improve করতেন?
উত্তর: "এখন basic Redis caching আছে। Production-এ
Output Cache + Redis distributed cache combination,
আর database query-গুলোতে query plans analyze করতাম।
Microservices project-এ distributed tracing (Jaeger/Tempo)
আরও properly integrate করতাম।"
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 14 — Interview Questions Bank (150 Theoretical + 100 Coding + 30 Tricky + 20 Rapid Fire + 30 Scenario-based...)
