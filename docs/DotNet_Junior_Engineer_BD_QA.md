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
| PART 3 | OOP in C# | ⏳ |
| PART 4 | Advanced C# | ⏳ |
| PART 5 | ASP.NET Core Fundamentals | ⏳ |
| PART 6 | Web API Development | ⏳ |
| PART 7 | Database & Entity Framework Core | ⏳ |
| PART 8 | Authentication & Security | ⏳ |
| PART 9 | Frontend Integration & Full Stack | ⏳ |
| PART 10 | Testing & Debugging | ⏳ |
| PART 11 | Deployment & DevOps Basics | ⏳ |
| PART 12 | System Design with .NET | ⏳ |
| PART 13 | .NET Projects | ⏳ |
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
