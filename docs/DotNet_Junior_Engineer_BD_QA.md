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
| PART 2 | C# Fundamentals | ⏳ |
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
