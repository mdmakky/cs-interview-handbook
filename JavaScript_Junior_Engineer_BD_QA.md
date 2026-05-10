<a id="top"></a>

# 🚀 JavaScript Interview Preparation Handbook — Junior Engineer Bangladesh
---

> **💡 হ্যান্ডবুক ব্যবহারের নিয়ম:**  
> প্রতিটি টপিক মনোযোগ দিয়ে পড়ুন। Code examples নিজে লিখে চালিয়ে দেখুন।  
> Interview questions নিজে উত্তর দেওয়ার চেষ্টা করুন, তারপর model answer দেখুন।  
> JavaScript একটি **dynamic language** — concept বোঝার পাশাপাশি হাতে-কলমে practice অপরিহার্য।

---

<a id="toc"></a>

## 📋 সূচিপত্র — Table of Contents

> **💡 নিচের যেকোনো PART-এ সরাসরি ক্লিক করুন। প্রতিটি PART-এর শেষে শীর্ষে ফিরুন বাটন আছে।**

| | PART | বিষয়বস্তু | অবস্থা |
|:-:|------|------------|:------:|
| 📘 | [**PART 1** — JavaScript Fundamentals](#part1) | Variables, Data Types, Functions, Scope, Hoisting, Closures | ✅ |
| 📗 | [**PART 2** — Advanced JavaScript](#part2) | Execution Context, Event Loop, Promises, Async/Await, Prototype | 🔜 |
| 📙 | [**PART 3** — DOM & Browser APIs](#part3) | DOM Manipulation, Events, Local Storage, Cookies | ✅ |
| 📕 | [**PART 4** — ES6+ Features](#part4) | Destructuring, Spread/Rest, Optional Chaining, Map, Set | 🔜 |
| 📓 | [**PART 5** — Asynchronous JavaScript](#part5) | Callbacks, Promises, Async/Await, Error Handling | 🔜 |
| 📔 | [**PART 6** — Object-Oriented JavaScript](#part6) | OOP, Classes, Prototypes, SOLID | 🔜 |
| 📒 | [**PART 7** — Frontend Development](#part7) | SPA, Virtual DOM, React Basics, State Management | 🔜 |
| 📃 | [**PART 8** — Node.js & Backend](#part8) | Express.js, REST API, JWT, Streams, Middleware | 🔜 |
| 📑 | [**PART 9** — Coding Interview Q&A](#part9) | 150 Theoretical + 100 Coding + 30 Tricky Questions | 🔜 |
| 🗂️ | [**PART 10** — Mini Projects](#part10) | Todo App, Weather App, Calculator, Auth System, CRUD | 🔜 |
| ⚡ | [**PART 11** — Performance & Optimization](#part11) | Lazy Loading, Memory Leaks, Code Splitting, Tree Shaking | 🔜 |
| 🇧🇩 | [**PART 12** — BD Interview Prep](#part12) | Mock Interview, Company Patterns, Fresher Tips, Rapid-fire | 🔜 |

<details>
<summary><strong>📘 PART 1 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [১.১ JavaScript কী?](#১১-javascript-কী)
- [১.২ JavaScript-এর ইতিহাস](#১২-javascript-এর-ইতিহাস)
- [১.৩ JavaScript কীভাবে কাজ করে — Engine ও Runtime](#১৩-javascript-কীভাবে-কাজ-করে--engine-ও-runtime)
- [১.৪ Variables — var, let, const](#১৪-variables--var-let-const)
- [১.৫ Data Types — Primitive vs Non-Primitive](#১৫-data-types--primitive-vs-non-primitive)
- [১.৬ Type Conversion ও Type Coercion](#১৬-type-conversion-ও-type-coercion)
- [১.৭ Operators](#১৭-operators)
- [১.৮ Conditions (if/else, switch, ternary)](#১৮-conditions)
- [১.৯ Loops](#১৯-loops)
- [১.১০ Functions](#১১০-functions)
- [১.১১ Arrow Functions](#১১১-arrow-functions)
- [১.১২ Scope](#১১২-scope)
- [১.১৩ Hoisting](#১১৩-hoisting)
- [১.১৪ Closures](#১১৪-closures)
- [১.১৫ Template Literals](#১১৫-template-literals)
- [১.১৬ PART 1 — Interview Questions & Answers](#১১৬-part-1--interview-questions--answers)

</details>

<details>
<summary><strong>📗 PART 2 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [২.১ Execution Context](#২১-execution-context)
- [২.২ Call Stack](#২২-call-stack)
- [২.৩ Memory Heap](#২৩-memory-heap)
- [২.৪ Event Loop](#২৪-event-loop)
- [২.৫ Callback Queue ও Microtask Queue](#২৫-callback-queue--microtask-queue)
- [২.৬ Callback Functions](#২৬-callback-functions)
- [২.৭ Promises](#২৭-promises)
- [২.৮ Async/Await](#২৮-asyncawait)
- [২.৯ Fetch API](#২৯-fetch-api)
- [২.১০ this keyword](#২১০-this-keyword)
- [২.১১ bind, call, apply](#২১১-bind-call-apply)
- [২.১২ Prototype](#২১২-prototype)
- [২.১৩ Prototype Chain](#২১৩-prototype-chain)
- [২.১৪ Inheritance](#২১৪-inheritance-in-javascript)
- [২.১৫ Classes](#২১৫-classes)
- [২.১৬ Modules](#২১৬-modules)
- [২.১৭ Debouncing ও Throttling](#২১৭-debouncing--throttling)
- [২.১৮ Currying](#২১৮-currying)
- [২.১৯ Memoization](#২১৯-memoization)
- [২.২০ Interview Q&A](#২২০-part-2--interview-questions--answers)

</details>

<details>
<summary><strong>📙 PART 3 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৩.১ DOM কী?](#৩১-dom-কী)
- [৩.২ DOM Manipulation](#৩২-dom-manipulation)
- [৩.৩ DOM Traversal](#৩৩-dom-traversal)
- [৩.৪ Event Handling](#৩৪-event-handling)
- [৩.৫ Event Bubbling](#৩৫-event-bubbling)
- [৩.৬ Event Capturing](#৩৬-event-capturing)
- [৩.৭ Event Delegation](#৩৭-event-delegation)
- [৩.৮ Local Storage](#৩৮-local-storage)
- [৩.৯ Session Storage](#৩৯-session-storage)
- [৩.১০ Cookies](#৩১০-cookies)
- [৩.১১ Browser APIs](#৩১১-browser-apis)
- [৩.১২ Form Validation](#৩১২-form-validation)
- [৩.১৩ Interview Q&A](#৩১৩-part-3--interview-questions--answers)

</details>

<details>
<summary><strong>📕 PART 4 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

<details>
<summary><strong>📓 PART 5 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

<details>
<summary><strong>📔 PART 6 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

<details>
<summary><strong>📒 PART 7 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

<details>
<summary><strong>📃 PART 8 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

<details>
<summary><strong>📑 PART 9 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

<details>
<summary><strong>🗂️ PART 10 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

<details>
<summary><strong>⚡ PART 11 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

<details>
<summary><strong>🇧🇩 PART 12 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

*(শীঘ্রই আসছে)*

</details>

---

<a id="part1"></a>

# PART 1 — JavaScript Fundamentals

> **📍 এই PART-এর Sections:** [১.১ JS কী?](#১১-javascript-কী) · [১.২ ইতিহাস](#১২-javascript-এর-ইতিহাস) · [১.৩ Engine ও Runtime](#১৩-javascript-কীভাবে-কাজ-করে--engine-ও-runtime) · [১.৪ Variables](#১৪-variables--var-let-const) · [১.৫ Data Types](#১৫-data-types--primitive-vs-non-primitive) · [১.৬ Type Conversion](#১৬-type-conversion-ও-type-coercion) · [১.৭ Operators](#১৭-operators) · [১.৮ Conditions](#১৮-conditions) · [১.৯ Loops](#১৯-loops) · [১.১০ Functions](#১১০-functions) · [১.১১ Arrow Functions](#১১১-arrow-functions) · [১.১২ Scope](#১১২-scope) · [১.১৩ Hoisting](#১১৩-hoisting) · [১.১৪ Closures](#১১৪-closures) · [১.১৫ Template Literals](#১১৫-template-literals) · [১.১৬ Interview Q&A](#১১৬-part-1--interview-questions--answers)

---

## ১.১ JavaScript কী?

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা (Definition)

**JavaScript** হলো একটি **high-level, interpreted, dynamic programming language** যা মূলত ওয়েব ব্রাউজারে ওয়েবপেজকে interactive করার জন্য তৈরি হয়েছিল। বর্তমানে এটি **frontend, backend (Node.js), mobile apps (React Native), desktop apps (Electron)** সহ প্রায় সব জায়গায় ব্যবহৃত হয়।

> **সহজ কথায়:** HTML ওয়েবপেজের কাঠামো তৈরি করে, CSS সাজায়, আর JavaScript প্রাণ দেয়।

### 🏠 বাস্তব জীবনের উদাহরণ (Real-life Analogy)

> একটি বাড়ির কথা চিন্তা করুন:
> - **HTML** = বাড়ির দেয়াল, মেঝে, ছাদ (কাঠামো)
> - **CSS** = রং, আসবাবপত্র, সাজসজ্জা (ডিজাইন)
> - **JavaScript** = বিদ্যুৎ, পানি, দরজার কলিং বেল (কার্যকারিতা)
>
> JavaScript ছাড়া ওয়েবসাইট একটি মৃত বাড়ির মতো — দেখতে সুন্দর হতে পারে, কিন্তু কিছুই করতে পারে না।

### 🎯 JavaScript-এর বৈশিষ্ট্য

| বৈশিষ্ট্য | ব্যাখ্যা |
|-----------|---------|
| **Interpreted** | Source code সরাসরি run হয়, আলাদা compile করতে হয় না |
| **Dynamic Typing** | Variable-এর type runtime-এ নির্ধারিত হয় |
| **Single-threaded** | একসময় একটি কাজ করে, কিন্তু async দিয়ে non-blocking |
| **Multi-paradigm** | OOP, Functional, Procedural — সব স্টাইলে লেখা যায় |
| **Event-driven** | ব্যবহারকারীর action (click, scroll) এ react করতে পারে |
| **First-class Functions** | Function কে variable-এ রাখা যায়, argument হিসেবে পাঠানো যায় |

### 💼 Practical Use Cases

```javascript
// ১. Button Click করলে কিছু করা
document.querySelector('#btn').addEventListener('click', function() {
  alert('আমাকে ক্লিক করা হয়েছে!');
});

// ২. API থেকে data আনা
fetch('https://api.example.com/users')
  .then(response => response.json())
  .then(data => console.log(data));

// ৩. Form validation
function validateEmail(email) {
  return email.includes('@') && email.includes('.');
}
```

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "JavaScript কী এবং কেন এটি important?"
>
> **আদর্শ উত্তর:** "JavaScript একটি high-level, interpreted, dynamic scripting language যা originally Brendan Eich 1995 সালে মাত্র 10 দিনে তৈরি করেছিলেন। এটি web browser-এ run হওয়ার জন্য design করা হয়েছিল — webpage-কে interactive করতে। বর্তমানে JavaScript সবচেয়ে popular programming language কারণ এটি দিয়ে frontend (React, Vue), backend (Node.js), mobile (React Native), এবং desktop (Electron) সব ধরনের application তৈরি করা যায়। এটি single-threaded কিন্তু Event Loop-এর মাধ্যমে asynchronous operation handle করতে পারে।"

### ⚠️ Common Mistakes

- ❌ JavaScript ও Java এক মনে করা — এরা সম্পূর্ণ আলাদা ভাষা
- ❌ JavaScript শুধু ব্রাউজারে চলে — ভুল, Node.js দিয়ে server-এও চলে
- ❌ JavaScript weakly typed মানে type নেই — type আছে, কিন্তু flexible

### ❓ Follow-up Interview Questions

<details>
<summary><strong>প্রশ্নগুলো দেখুন ও উত্তর মিলিয়ে নিন</strong></summary>

**Q: "JavaScript কি compiled নাকি interpreted language?"**
> **A:** JavaScript মূলত **interpreted**, কিন্তু আধুনিক JS engines (V8) **JIT (Just-In-Time) Compilation** ব্যবহার করে performance বাড়ায়। তাই বলা যায় এটি **interpreted + JIT compiled**।

**Q: "JavaScript কি strongly typed নাকি weakly typed?"**
> **A:** JavaScript **weakly (loosely) typed** ও **dynamically typed**। Variable declare করার সময় type বলতে হয় না, এবং runtime-এ type automatically convert হতে পারে।

**Q: "Java এবং JavaScript-এর পার্থক্য কী?"**
> **A:** নাম একটু মিল ছাড়া এরা সম্পূর্ণ আলাদা। Java একটি compiled, statically typed, OOP language যা JVM-এ চলে। JavaScript একটি interpreted, dynamically typed, multi-paradigm language যা browser/Node.js-এ চলে।

</details>

---

## ১.২ JavaScript-এর ইতিহাস

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংক্ষিপ্ত ইতিহাস

| সাল | ঘটনা |
|-----|------|
| **1995** | Brendan Eich, Netscape-এ মাত্র **10 দিনে** JavaScript তৈরি করেন। নাম ছিল প্রথমে **Mocha**, তারপর **LiveScript** |
| **1995** | Java-র popularity দেখে নাম রাখা হয় **JavaScript** (marketing কৌশল) |
| **1997** | ECMA International **ECMAScript (ES1)** standard প্রকাশ করে |
| **1999** | **ES3** — Regular Expressions, try/catch চালু |
| **2009** | **ES5** — `strict mode`, `JSON`, `Array.forEach()` যোগ |
| **2009** | **Node.js** তৈরি — JS এখন server-এও চলে |
| **2015** | **ES6 (ES2015)** — সবচেয়ে বড় আপডেট: `let`, `const`, Arrow Functions, Classes, Promises, Modules |
| **2016+** | প্রতি বছর নতুন ES version (ES2016, ES2017, ...) |
| **বর্তমান** | JavaScript বিশ্বের **সবচেয়ে popular** programming language (Stack Overflow Survey) |

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "ECMAScript কী?"
>
> **আদর্শ উত্তর:** "ECMAScript হলো JavaScript-এর **official standard specification**। ECMA International নামক organization এই standard maintain করে। JavaScript হলো এই specification-এর implementation। আমরা যখন বলি ES6 বা ES2015, তার মানে ECMAScript 2015 version-এর features। প্রতি বছর নতুন features যোগ হয় — ES2016, ES2017 এভাবে।"

### 💡 Memory Tip

> **Mocha → LiveScript → JavaScript** — নামের এই পরিবর্তন মনে রাখুন।  
> **"১০ দিনে তৈরি"** — এই fact প্রায়ই interview-এ জিজ্ঞেস করা হয়।  
> **ES6 = ES2015** — এই equivalence মনে রাখুন।

---

## ১.৩ JavaScript কীভাবে কাজ করে — Engine ও Runtime

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 JS Engine কী?

**JavaScript Engine** হলো একটি program যা JavaScript code পড়ে এবং execute করে।

| Engine | Browser/Platform |
|--------|-----------------|
| **V8** | Google Chrome, Node.js |
| **SpiderMonkey** | Mozilla Firefox |
| **JavaScriptCore (Nitro)** | Safari |
| **Chakra** | Microsoft Edge (পুরনো) |

### ⚙️ Engine-এর ভেতরে কী হয়?

```
JS Code (Source)
      ↓
  Parser → Abstract Syntax Tree (AST)
      ↓
  Interpreter (Ignition in V8)
      ↓
  Bytecode
      ↓
  JIT Compiler (TurboFan in V8) → Optimized Machine Code
      ↓
  CPU Execute করে
```

### 🏠 Runtime কী?

**JavaScript Runtime** হলো JS Engine + সব extra tools যা JS কে কাজ করতে সাহায্য করে।

**Browser Runtime:**
```
┌─────────────────────────────────────────┐
│           Browser Runtime               │
│  ┌──────────┐  ┌────────────────────┐  │
│  │ JS Engine│  │   Web APIs         │  │
│  │  (V8)    │  │ (DOM, fetch, timer)│  │
│  └──────────┘  └────────────────────┘  │
│  ┌──────────────────────────────────┐  │
│  │     Callback Queue / Task Queue  │  │
│  └──────────────────────────────────┘  │
│  ┌──────────────────────────────────┐  │
│  │          Event Loop              │  │
│  └──────────────────────────────────┘  │
└─────────────────────────────────────────┘
```

**Node.js Runtime:**
- V8 Engine + **libuv** (file system, network, timers)

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Browser-এ JavaScript কীভাবে execute হয়?"
>
> **আদর্শ উত্তর:** "Browser-এ JavaScript execute করার জন্য একটি JS Engine থাকে — Chrome-এ V8। Engine প্রথমে source code parse করে AST (Abstract Syntax Tree) তৈরি করে। তারপর Interpreter সেটাকে Bytecode-এ convert করে। Frequently used code-কে JIT Compiler optimize করে machine code-এ convert করে CPU execute করে। Browser-এ DOM, fetch, setTimeout এগুলো Web APIs — JS Engine এর বাইরে। এগুলো শেষ হলে callback queue-তে যায়, Event Loop সেটাকে Call Stack-এ push করে।"

### ⚠️ Common Mistakes

- ❌ মনে করা JS Engine এবং JS Runtime একই — Engine হলো Runtime-এর একটি অংশ
- ❌ setTimeout মনে করা JS Engine-এর অংশ — এটি Web API (Browser-এর অংশ)

---

## ১.৪ Variables — var, let, const

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Variable** হলো data store করার একটি named container। JavaScript-এ variable declare করার তিনটি উপায়: `var`, `let`, `const`।

### 🏠 বাস্তব জীবনের উদাহরণ

> - **`var`** = পুরনো আমলের একটি বাক্স যেটা যেকোনো জায়গা থেকে access করা যায় এবং যেকোনো সময় পরিবর্তন করা যায় — বিশৃঙ্খল!
> - **`let`** = একটি আধুনিক বাক্স যেটা নির্দিষ্ট ঘরের মধ্যে সীমাবদ্ধ, পরিবর্তনযোগ্য
> - **`const`** = একটি সিল করা বাক্স — একবার রাখলে আর পরিবর্তন করা যাবে না

### 📊 var vs let vs const তুলনা

| বৈশিষ্ট্য | `var` | `let` | `const` |
|-----------|-------|-------|---------|
| **Scope** | Function scope | Block scope | Block scope |
| **Hoisting** | হয় (undefined) | হয় (TDZ error) | হয় (TDZ error) |
| **Re-declare** | ✅ পারবে | ❌ পারবে না | ❌ পারবে না |
| **Re-assign** | ✅ পারবে | ✅ পারবে | ❌ পারবে না |
| **Global object property** | ✅ হয় | ❌ হয় না | ❌ হয় না |
| **কখন ব্যবহার** | পুরনো code, এড়িয়ে চলুন | যখন value বদলাবে | যখন value বদলাবে না |

### 💻 Code Examples

```javascript
// ১. var — function scope, re-declare করা যায়
var name = "Rahim";
var name = "Karim"; // OK — re-declare
console.log(name); // "Karim"

function testVar() {
  var x = 10;
  if (true) {
    var x = 20; // SAME variable — var is function-scoped!
    console.log(x); // 20
  }
  console.log(x); // 20 (অপ্রত্যাশিত!)
}

// ২. let — block scope, re-declare করা যায় না
let age = 25;
// let age = 30; // SyntaxError: Identifier 'age' already declared

function testLet() {
  let y = 10;
  if (true) {
    let y = 20; // DIFFERENT variable — let is block-scoped
    console.log(y); // 20
  }
  console.log(y); // 10 (প্রত্যাশিত!)
}

// ৩. const — block scope, re-assign করা যায় না
const PI = 3.14159;
// PI = 3.14; // TypeError: Assignment to constant variable

// কিন্তু object/array-এর ভেতরে পরিবর্তন করা যায়!
const person = { name: "Rahim", age: 25 };
person.age = 26; // OK! (object mutate করা)
// person = {}; // TypeError (variable re-assign করা যাবে না)

const numbers = [1, 2, 3];
numbers.push(4); // OK!
// numbers = []; // TypeError
```

### 🔍 Temporal Dead Zone (TDZ)

```javascript
// var — hoisting, undefined পাবে
console.log(myVar); // undefined (hoisted)
var myVar = "hello";

// let — hoisting হয়, কিন্তু TDZ-এ থাকে
console.log(myLet); // ReferenceError: Cannot access 'myLet' before initialization
let myLet = "world";

// const — একই TDZ behavior
console.log(myConst); // ReferenceError
const myConst = "!";
```

> **TDZ কী?** Variable declare হওয়ার আগে যে zone-এ সে থাকে সেখানে access করা যায় না — এটাই **Temporal Dead Zone**।

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "var, let, এবং const-এর মধ্যে পার্থক্য কী? কোনটি কখন ব্যবহার করবেন?"
>
> **আদর্শ উত্তর:** "তিনটির মূল পার্থক্য scope এবং mutability নিয়ে।  
> `var` function-scoped এবং hoisting-এ undefined পায়, re-declare করা যায় — এটি bug-prone তাই আমরা এড়িয়ে চলি।  
> `let` block-scoped এবং re-assign করা যায় কিন্তু re-declare যায় না। Loop counter বা পরিবর্তনযোগ্য value-র জন্য ব্যবহার করি।  
> `const` block-scoped এবং re-assign করা যায় না। তবে মনে রাখতে হবে `const` object বা array-এর ক্ষেত্রে variable-কে re-assign থেকে রোধ করে, কিন্তু object-এর property পরিবর্তন করা যায়।  
> Best practice হলো: সবসময় `const` দিয়ে শুরু করুন, যদি re-assign দরকার হয় তাহলে `let` ব্যবহার করুন, `var` ব্যবহার করবেন না।"

### ⚠️ Common Mistakes

```javascript
// ❌ Mistake 1: const মানে immutable value মনে করা
const arr = [1, 2, 3];
arr.push(4); // এটা কিন্তু valid! (Array mutate হচ্ছে, variable নয়)

// ❌ Mistake 2: var দিয়ে loop variable
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1000); // 3, 3, 3 (প্রত্যাশিত ছিল 0, 1, 2)
}

// ✅ সঠিক — let দিয়ে
for (let j = 0; j < 3; j++) {
  setTimeout(() => console.log(j), 1000); // 0, 1, 2
}

// ❌ Mistake 3: var global object দূষণ
var globalVar = "I pollute window";
console.log(window.globalVar); // "I pollute window" (Browser-এ)

let notGlobal = "I don't";
console.log(window.notGlobal); // undefined
```

### ❓ Follow-up Interview Questions

<details>
<summary><strong>প্রশ্নগুলো দেখুন ও উত্তর মিলিয়ে নিন</strong></summary>

**Q: "const দিয়ে declare করা object-কে কি পুরোপুরি immutable করা যায়?"**
> **A:** হ্যাঁ, `Object.freeze()` দিয়ে। `const` শুধু re-assignment রোধ করে, কিন্তু `Object.freeze(obj)` object-এর properties পরিবর্তনও রোধ করে।

**Q: "var কেন এড়িয়ে চলা উচিত?"**
> **A:** তিনটি কারণ: (১) Function scope-এর জন্য unexpected bugs হয়, (২) Re-declare করা যায় বলে accidental overwrite হতে পারে, (৩) Hoisting-এ `undefined` পাওয়া যায় যা debugging কঠিন করে।

**Q: "TDZ কী? কেন এটি useful?"**
> **A:** Temporal Dead Zone হলো variable declare হওয়ার আগের time period। এই সময়ে access করলে `ReferenceError` আসে। এটি useful কারণ variable declare হওয়ার আগে ব্যবহার করা programming bug — TDZ এই bug ধরিয়ে দেয়।

</details>

---

## ১.৫ Data Types — Primitive vs Non-Primitive

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

JavaScript-এ দুই ধরনের data type আছে:

### 1️⃣ Primitive Types (৭টি)

| Type | উদাহরণ | typeof |
|------|---------|--------|
| **Number** | `42`, `3.14`, `NaN`, `Infinity` | `"number"` |
| **String** | `"hello"`, `'world'`, `` `template` `` | `"string"` |
| **Boolean** | `true`, `false` | `"boolean"` |
| **Undefined** | `let x;` (declare but no value) | `"undefined"` |
| **Null** | `let y = null;` | `"object"` ⚠️ (JS bug!) |
| **Symbol** | `Symbol('id')` | `"symbol"` |
| **BigInt** | `9007199254740991n` | `"bigint"` |

### 2️⃣ Non-Primitive (Reference) Types

| Type | উদাহরণ | typeof |
|------|---------|--------|
| **Object** | `{ name: "Rahim" }` | `"object"` |
| **Array** | `[1, 2, 3]` | `"object"` |
| **Function** | `function() {}` | `"function"` |
| **Date** | `new Date()` | `"object"` |
| **RegExp** | `/pattern/` | `"object"` |

### 🏠 বাস্তব জীবনের উদাহরণ

> - **Primitive** = টাকার কয়েন — কাউকে দিলে সে copy পায়, আপনার কাছে আপনারটা থাকে
> - **Non-Primitive (Reference)** = বাড়ির চাবি — কাউকে copy দিলে সেই একই বাড়িতে দুজনেরই access থাকে

```javascript
// Primitive — value copy হয়
let a = 10;
let b = a; // b = 10 (copy)
b = 20;
console.log(a); // 10 (অপরিবর্তিত)
console.log(b); // 20

// Reference — reference copy হয়
let obj1 = { name: "Rahim" };
let obj2 = obj1; // obj2 ও একই object-কে point করে
obj2.name = "Karim";
console.log(obj1.name); // "Karim" (পরিবর্তিত হয়ে গেছে!)
console.log(obj2.name); // "Karim"
```

### 🔍 typeof ব্যবহার ও Gotchas

```javascript
console.log(typeof 42);          // "number"
console.log(typeof "hello");     // "string"
console.log(typeof true);        // "boolean"
console.log(typeof undefined);   // "undefined"
console.log(typeof null);        // "object" ← JS-এর famous bug!
console.log(typeof Symbol());    // "symbol"
console.log(typeof 42n);         // "bigint"
console.log(typeof {});          // "object"
console.log(typeof []);          // "object" ← Array ও object!
console.log(typeof function(){}); // "function"

// Array check করার সঠিক উপায়
console.log(Array.isArray([]));  // true
console.log(Array.isArray({}));  // false

// null check
let x = null;
console.log(x === null); // true (সঠিক উপায়)
```

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Primitive এবং Reference type-এর পার্থক্য কী?"
>
> **আদর্শ উত্তর:** "Primitive types হলো: Number, String, Boolean, Undefined, Null, Symbol, BigInt। এগুলো **value by value** copy হয় — মানে একটি variable থেকে অন্যটিতে assign করলে আলাদা copy তৈরি হয়। তাই একটা পরিবর্তন করলে অন্যটা প্রভাবিত হয় না।  
> Reference types হলো Object, Array, Function। এগুলো **memory-তে** store থাকে এবং variable-এ সেই memory-র address (reference) store হয়। তাই একটি variable থেকে অন্যটিতে assign করলে দুজনেই same memory-r দিকে point করে — একটা পরিবর্তন করলে দুজনেই দেখতে পায়।"

### ⚠️ Common Mistakes

```javascript
// ❌ Mistake 1: typeof null === "object" — এটা JS bug
if (typeof myVar === "object") {
  // null এও এই block-এ ঢুকে পড়বে!
}
// ✅ সঠিক
if (myVar !== null && typeof myVar === "object") { }

// ❌ Mistake 2: NaN check
console.log(NaN === NaN); // false! NaN কখনো নিজের সমান নয়
// ✅ সঠিক
console.log(Number.isNaN(NaN)); // true

// ❌ Mistake 3: Array check
console.log(typeof []); // "object" — Array বোঝা যাচ্ছে না
// ✅ সঠিক
console.log(Array.isArray([])); // true
```

### ❓ Follow-up Interview Questions

<details>
<summary><strong>প্রশ্নগুলো দেখুন</strong></summary>

**Q: "NaN কী? এটা কোন type?"**
> **A:** NaN = "Not a Number"। এটা ironically `Number` type! অসম্ভব mathematical operation করলে পাওয়া যায়: `"hello" * 2 = NaN`। Special property: `NaN === NaN` সবসময় `false`। Check করতে `Number.isNaN()` ব্যবহার করুন।

**Q: "null এবং undefined-এর পার্থক্য?"**
> **A:** `undefined` মানে variable declare হয়েছে কিন্তু কোনো value assign হয়নি — JS নিজে দেয়। `null` মানে programmer ইচ্ছাকৃতভাবে "কোনো value নেই" বুঝাতে সেট করেছে। `typeof null === "object"` JS-এর একটি historical bug।

**Q: "Deep copy vs Shallow copy?"**
> **A:** Shallow copy-তে nested object/array-গুলো copy হয় না, reference copy হয়। Deep copy-তে সম্পূর্ণ নতুন copy তৈরি হয়। `Object.assign()` ও spread operator shallow copy করে। `JSON.parse(JSON.stringify(obj))` বা `structuredClone()` deep copy করে।

</details>

---

## ১.৬ Type Conversion ও Type Coercion

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

| | ব্যাখ্যা |
|--|---------|
| **Type Conversion (Explicit)** | Programmer নিজে type পরিবর্তন করে |
| **Type Coercion (Implicit)** | JavaScript নিজে automatically type পরিবর্তন করে |

### 💻 Explicit Conversion

```javascript
// String → Number
Number("42");       // 42
Number("3.14");     // 3.14
Number("hello");    // NaN
Number(true);       // 1
Number(false);      // 0
Number(null);       // 0
Number(undefined);  // NaN
parseInt("42px");   // 42 (number পর্যন্ত parse করে)
parseFloat("3.14abc"); // 3.14

// Number → String
String(42);         // "42"
(42).toString();    // "42"
(42).toString(2);   // "101010" (binary)
(42).toString(16);  // "2a" (hex)

// Any → Boolean
Boolean(0);         // false
Boolean("");        // false
Boolean(null);      // false
Boolean(undefined); // false
Boolean(NaN);       // false
Boolean(false);     // false
// বাকি সব: true
Boolean(1);         // true
Boolean("hello");   // true
Boolean([]);        // true (empty array!)
Boolean({});        // true (empty object!)
```

### 🔥 Implicit Coercion — Interview Trap!

```javascript
// + operator — string priority
"5" + 3;        // "53" (number → string, concatenate)
"5" + true;     // "5true"
"5" + null;     // "5null"
"5" + undefined; // "5undefined"

// - * / % — number priority
"5" - 3;        // 2 (string → number)
"5" * "2";      // 10
"5" / "2";      // 2.5
"5" - "hello";  // NaN

// == (loose equality) — type coercion হয়
0 == false;     // true
1 == true;      // true
"" == false;    // true
null == undefined; // true
null == 0;      // false (!)
[] == false;    // true (!)
[] == ![];      // true (!!! famous trick)

// === (strict equality) — coercion হয় না
0 === false;    // false
"5" === 5;      // false
```

### 🧠 Falsy Values মুখস্থ করুন

> JavaScript-এ মাত্র **6টি** falsy value আছে:
> `false`, `0`, `""` (empty string), `null`, `undefined`, `NaN`
>
> বাকি সব **truthy** — `[]`, `{}`, `"0"`, `-1` সব truthy!

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "`==` এবং `===` এর পার্থক্য কী?"
>
> **আদর্শ উত্তর:** "`==` হলো loose equality বা abstract equality। এটি compare করার আগে type coercion করে। যেমন `0 == false` true কারণ false কে number-এ convert করলে 0 হয়। `===` হলো strict equality — এটি type coercion করে না। দুটো value strict equal হতে হলে তাদের value এবং type উভয়ই same হতে হবে। Best practice: সবসময় `===` ব্যবহার করুন।"

### ⚠️ Tricky Examples (Interview Favorites!)

```javascript
console.log(1 + "2" + "2"); // "122" (১+২="12", "12"+"2"="122")
console.log(1 + +"2" + "2"); // "32" (+"2"=2, 1+2=3, 3+"2"="32")
console.log("A" - "B" + "2"); // "NaN2" (NaN+"2")
console.log([] + []);   // "" (empty string)
console.log([] + {});   // "[object Object]"
console.log({} + []);   // 0 বা "[object Object]" (context-dependent!)
console.log(+"");       // 0
console.log(+null);     // 0
console.log(+undefined); // NaN
console.log(+true);     // 1
console.log(+"hello");  // NaN
```

---

## ১.৭ Operators

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 Operator-এর প্রকারভেদ

```javascript
// ১. Arithmetic Operators
console.log(10 + 3);  // 13
console.log(10 - 3);  // 7
console.log(10 * 3);  // 30
console.log(10 / 3);  // 3.3333...
console.log(10 % 3);  // 1 (remainder/modulus)
console.log(2 ** 10); // 1024 (exponentiation, ES2016)

// ২. Assignment Operators
let x = 10;
x += 5;   // x = x + 5 = 15
x -= 3;   // x = x - 3 = 12
x *= 2;   // x = x * 2 = 24
x /= 4;   // x = x / 4 = 6
x **= 2;  // x = x ** 2 = 36

// ৩. Comparison Operators
console.log(5 > 3);    // true
console.log(5 >= 5);   // true
console.log(5 < 3);    // false
console.log(5 == "5"); // true (type coercion)
console.log(5 === "5"); // false (strict)
console.log(5 != "5"); // false
console.log(5 !== "5"); // true

// ৪. Logical Operators
console.log(true && false); // false (AND)
console.log(true || false); // true (OR)
console.log(!true);         // false (NOT)

// Short-circuit evaluation
let name = null;
let displayName = name || "Guest"; // "Guest"
let admin = true;
admin && console.log("Admin logged in"); // runs

// ৫. Nullish Coalescing (??) — ES2020
let val = null ?? "default"; // "default"
let val2 = 0 ?? "default";   // 0 (0 is not null/undefined)
let val3 = 0 || "default";   // "default" (0 is falsy)

// ৬. Optional Chaining (?.) — ES2020
let user = { profile: { name: "Rahim" } };
console.log(user?.profile?.name);    // "Rahim"
console.log(user?.address?.city);    // undefined (no error)

// ৭. Ternary Operator
let age = 20;
let status = age >= 18 ? "Adult" : "Minor"; // "Adult"

// ৮. Bitwise Operators (Interview-এ আসতে পারে)
console.log(5 & 3);   // 1  (AND)
console.log(5 | 3);   // 7  (OR)
console.log(5 ^ 3);   // 6  (XOR)
console.log(~5);       // -6 (NOT)
console.log(5 << 1);  // 10 (Left shift)
console.log(5 >> 1);  // 2  (Right shift)
```

### 💡 Operator Precedence (গুরুত্বপূর্ণ)

```javascript
// উচ্চ থেকে নিম্ন (মনে রাখার উপায়: PUMA)
// P - Parentheses ()
// U - Unary (!, -, +, typeof)
// M - Multiplication, Division, Modulus
// A - Addition, Subtraction

console.log(2 + 3 * 4);      // 14 (*, then +)
console.log((2 + 3) * 4);    // 20 (parentheses first)
console.log(true || false && false); // true (&& > ||)
```

### ⚠️ Common Mistakes

```javascript
// ❌ = vs == vs ===
if (x = 5) { } // assignment (bug!), always true
if (x == 5) { } // loose comparison
if (x === 5) { } // strict comparison ✅

// ❌ && এবং || এর return value না জানা
console.log(1 && 2);       // 2 (শেষ truthy value)
console.log(null && "hi"); // null (প্রথম falsy value)
console.log(null || "hi"); // "hi" (প্রথম truthy value)
console.log(0 || null || "yes"); // "yes"
```

---

## ১.৮ Conditions

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 if / else if / else

```javascript
let score = 75;

if (score >= 90) {
  console.log("A+");
} else if (score >= 80) {
  console.log("A");
} else if (score >= 70) {
  console.log("B");
} else if (score >= 60) {
  console.log("C");
} else {
  console.log("Fail");
}
// Output: "B"
```

### 💻 switch Statement

```javascript
let day = "Monday";

switch (day) {
  case "Saturday":
  case "Sunday":
    console.log("Weekend!");
    break;
  case "Monday":
    console.log("Start of work week");
    break;
  default:
    console.log("Weekday");
}

// ⚠️ break না দিলে fall-through হয়
switch (1) {
  case 1:
    console.log("one");
    // break নেই!
  case 2:
    console.log("two"); // এটাও execute হবে!
  default:
    console.log("default"); // এটাও!
}
// Output: "one", "two", "default"
```

### 💻 Ternary Operator

```javascript
// একটি line-এ simple if-else
let age = 20;
let message = age >= 18 ? "Vote করতে পারবেন" : "Vote করতে পারবেন না";

// Nested ternary (এড়িয়ে চলুন, অপঠনযোগ্য)
let grade = score >= 90 ? "A+" : score >= 80 ? "A" : "B";
```

### 💻 Short-circuit as Condition

```javascript
// && এবং || condition হিসেবে
let isLoggedIn = true;
isLoggedIn && showDashboard(); // isLoggedIn হলেই showDashboard() run

let username = getUserName() || "Guest"; // username না পেলে "Guest"
```

### ❓ Follow-up Questions

<details>
<summary><strong>প্রশ্নগুলো দেখুন</strong></summary>

**Q: "switch statement-এ break না দিলে কী হয়?"**
> **A:** **Fall-through** হয় — match হওয়া case থেকে শুরু করে পরের সব cases execute হতে থাকে `break` বা function শেষ না হওয়া পর্যন্ত। কখনো কখনো intentionally ব্যবহার করা হয় (যেমন একাধিক case-এ একই code)।

</details>

---

## ১.৯ Loops

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 সব ধরনের Loop

```javascript
// ১. for loop
for (let i = 0; i < 5; i++) {
  console.log(i); // 0, 1, 2, 3, 4
}

// ২. while loop
let count = 0;
while (count < 5) {
  console.log(count);
  count++;
}

// ৩. do...while (কমপক্ষে একবার execute হয়)
let num = 10;
do {
  console.log(num); // 10 (condition false হলেও একবার চলে)
  num++;
} while (num < 5);

// ৪. for...of (Array/String/Iterable-এর values)
const fruits = ["Apple", "Banana", "Mango"];
for (const fruit of fruits) {
  console.log(fruit); // "Apple", "Banana", "Mango"
}

// ৫. for...in (Object-এর keys)
const person = { name: "Rahim", age: 25, city: "Dhaka" };
for (const key in person) {
  console.log(`${key}: ${person[key]}`);
}
// name: Rahim
// age: 25
// city: Dhaka

// ৬. Array forEach
fruits.forEach((fruit, index) => {
  console.log(`${index}: ${fruit}`);
});

// ৭. break ও continue
for (let i = 0; i < 10; i++) {
  if (i === 3) continue; // 3 skip করবে
  if (i === 7) break;    // 7-এ loop বন্ধ
  console.log(i); // 0, 1, 2, 4, 5, 6
}
```

### 📊 Loop তুলনা

| Loop | কখন ব্যবহার |
|------|------------|
| `for` | নির্দিষ্ট সংখ্যক iteration |
| `while` | condition-based, শেষ কবে জানা নেই |
| `do...while` | কমপক্ষে একবার চালাতে হবে |
| `for...of` | Array/Iterable-এর values |
| `for...in` | Object-এর keys |
| `forEach` | Array — break/continue দরকার নেই |

### ⚠️ Common Mistakes

```javascript
// ❌ for...in দিয়ে Array iterate (prototype properties আসতে পারে)
const arr = [10, 20, 30];
for (const index in arr) {
  console.log(arr[index]); // কাজ করে কিন্তু index string হয়
}
// ✅ Array-এর জন্য for...of বা forEach

// ❌ forEach-এ break/continue
arr.forEach(item => {
  if (item === 20) break; // SyntaxError!
});
// ✅ for...of ব্যবহার করুন
```

---

## ১.১০ Functions

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Function** হলো একটি reusable block of code যা একটি নির্দিষ্ট কাজ করে। JavaScript-এ function **first-class citizen** — মানে function কে variable-এ রাখা, argument হিসেবে পাঠানো, এবং return করা যায়।

### 🏠 বাস্তব জীবনের উদাহরণ

> Function হলো একটি **রেসিপি** — একবার লিখুন, বারবার রান্না করুন। উপকরণ (parameters) দিন, ফলাফল (return value) পান।

### 💻 Function-এর প্রকারভেদ

```javascript
// ১. Function Declaration (Hoisted)
function greet(name) {
  return `হ্যালো, ${name}!`;
}
console.log(greet("Rahim")); // "হ্যালো, Rahim!"

// hoisted — declare করার আগেও call করা যায়
sayHi(); // "Hi!" — works!
function sayHi() { console.log("Hi!"); }

// ২. Function Expression (Not Hoisted)
const multiply = function(a, b) {
  return a * b;
};
// multiply(); // declare করার আগে call করলে error
console.log(multiply(3, 4)); // 12

// ৩. Named Function Expression
const factorial = function fact(n) {
  if (n <= 1) return 1;
  return n * fact(n - 1); // নাম দিয়ে নিজেকে call করা যায়
};

// ৪. IIFE — Immediately Invoked Function Expression
(function() {
  console.log("আমি সঙ্গে সঙ্গে চলি!");
})(); // শেষে () দিয়ে তাৎক্ষণিক invoke

// ৫. Higher-Order Function
function applyOperation(num, operation) {
  return operation(num);
}
const double = n => n * 2;
console.log(applyOperation(5, double)); // 10

// ৬. Default Parameters (ES6)
function greetUser(name = "Guest", greeting = "হ্যালো") {
  return `${greeting}, ${name}!`;
}
console.log(greetUser());           // "হ্যালো, Guest!"
console.log(greetUser("Rahim"));    // "হ্যালো, Rahim!"

// ৭. Rest Parameters (ES6)
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}
console.log(sum(1, 2, 3, 4, 5)); // 15

// ৮. arguments object (old way, only in regular functions)
function showArgs() {
  console.log(arguments); // array-like object
  console.log(Array.from(arguments));
}
showArgs(1, 2, 3);
```

### 📊 Function Declaration vs Expression

| | Function Declaration | Function Expression |
|--|---------------------|---------------------|
| **Hoisting** | ✅ সম্পূর্ণ hoisted | ❌ variable অংশ hoisted (undefined) |
| **Call timing** | Declare করার আগেও | Declare করার পরে |
| **নাম** | বাধ্যতামূলক | Optional |
| **কখন ব্যবহার** | General purpose | Callback, module, conditional |

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "First-class function বলতে কী বোঝায়?"
>
> **আদর্শ উত্তর:** "JavaScript-এ functions হলো first-class citizen — মানে function-কে অন্য যেকোনো value-র মতো treat করা যায়। তিনটি বৈশিষ্ট্য: (১) Function কে variable-এ assign করা যায়, (২) Function কে অন্য function-এর argument হিসেবে পাঠানো যায় (callback), (৩) Function থেকে function return করা যায় (higher-order function)। এই feature-এর জন্যই JavaScript-এ functional programming এবং patterns যেমন closure, currying, memoization সম্ভব।"

---

## ১.১১ Arrow Functions

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Arrow Function** হলো ES6-এ আসা function-এর সংক্ষিপ্ত syntax। কিন্তু শুধু syntax নয় — এর `this` binding behavior আলাদা।

### 💻 Syntax

```javascript
// Regular function
function add(a, b) { return a + b; }

// Arrow function — সব equivalent
const add1 = (a, b) => { return a + b; };
const add2 = (a, b) => a + b;            // implicit return
const square = x => x * x;               // single param, no ()
const greet = () => "Hello!";            // no param

// Object return করতে () লাগবে
const getUser = () => ({ name: "Rahim", age: 25 });
```

### 🔑 Arrow Function vs Regular Function — মূল পার্থক্য

```javascript
// ১. this binding
const timer = {
  seconds: 0,
  
  // Regular function — this হারিয়ে যায়
  startRegular: function() {
    setInterval(function() {
      this.seconds++; // ❌ এখানে this = window/undefined
      console.log(this.seconds);
    }, 1000);
  },
  
  // Arrow function — this parent থেকে inherit করে (lexical this)
  startArrow: function() {
    setInterval(() => {
      this.seconds++; // ✅ এখানে this = timer object
      console.log(this.seconds);
    }, 1000);
  }
};

// ২. arguments object নেই
function regular() {
  console.log(arguments); // OK
}

const arrow = () => {
  console.log(arguments); // ReferenceError!
};
// Arrow-এ rest parameter ব্যবহার করুন: (...args) => { console.log(args); }

// ৩. constructor হিসেবে ব্যবহার করা যায় না
const Person = (name) => { this.name = name; };
// new Person("Rahim"); // TypeError: Person is not a constructor

// ৪. prototype property নেই
const arrowFn = () => {};
console.log(arrowFn.prototype); // undefined
```

### 📊 কখন কোনটি ব্যবহার করবেন

| পরিস্থিতি | Regular Function | Arrow Function |
|-----------|-----------------|----------------|
| Method in object | ✅ | ❌ (this problem) |
| Constructor | ✅ | ❌ |
| Callback | দুটোই চলে | ✅ প্রিয় |
| Array methods (.map, .filter) | দুটোই | ✅ সংক্ষিপ্ত |
| Event handler (DOM) | ✅ | ⚠️ this ভিন্ন |
| IIFE | ✅ | ✅ |

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Arrow function কখন ব্যবহার করবেন না?"
>
> **আদর্শ উত্তর:** "Arrow function তিনটি পরিস্থিতিতে ব্যবহার করা উচিত নয়: (১) Object-এর method হিসেবে — কারণ arrow function-এর `this` lexically bound, তাই object-কে point করবে না, window/undefined point করবে। (২) Constructor হিসেবে — `new` keyword দিয়ে arrow function call করা যায় না। (৩) Event handler-এ যদি `this` দিয়ে element access করতে হয় — কারণ arrow-এ `this` enclosing scope-এর হবে।"

---

## ১.১২ Scope

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Scope** নির্ধারণ করে কোথায় variable accessible এবং কোথায় নয়।

### 🏠 বাস্তব জীবনের উদাহরণ

> Scope হলো **দৃশ্যমানতার এলাকা**। আপনার ঘরের জিনিসপত্র বাইরের লোক দেখতে পায় না, কিন্তু আপনি বাইরের রাস্তা দেখতে পান — inner scope → outer scope access করা যায়, কিন্তু বিপরীতে নয়।

### 💻 Scope-এর প্রকারভেদ

```javascript
// ১. Global Scope
let globalVar = "আমি সবার accessible";

function anyFunction() {
  console.log(globalVar); // ✅ accessible
}

// ২. Function Scope (Local Scope)
function myFunction() {
  let localVar = "শুধু এই function-এ";
  console.log(localVar); // ✅
}
// console.log(localVar); // ❌ ReferenceError

// ৩. Block Scope (let/const — ES6)
{
  let blockVar = "এই block-এ শুধু";
  const blockConst = "আমিও block-scoped";
  var oldVar = "আমি function/global scoped";
}
// console.log(blockVar);  // ❌ ReferenceError
// console.log(blockConst); // ❌ ReferenceError
console.log(oldVar); // ✅ "আমি function/global scoped" (var!)

// ৪. Lexical Scope (Static Scope)
function outer() {
  let outerVar = "outer";
  
  function inner() {
    console.log(outerVar); // ✅ inner, outer-এর variable access করতে পারে
  }
  
  inner();
}

// ৫. Scope Chain
let a = "global a";

function first() {
  let b = "first's b";
  
  function second() {
    let c = "second's c";
    console.log(a); // ✅ global থেকে
    console.log(b); // ✅ parent (first) থেকে
    console.log(c); // ✅ নিজের
  }
  
  second();
}
```

### 📊 Scope Chain ভিজুয়াল

```
Global Scope: { a }
  └── first() Scope: { b }
        └── second() Scope: { c }
              → c খুঁজলে: নিজের scope → first scope → global scope
              → Scope Chain!
```

### ⚠️ Common Mistakes

```javascript
// ❌ Variable shadowing — একই নামে ভেতরে declare
let count = 0;
function increment() {
  let count = 1; // outer count shadow করে
  count++;
  console.log(count); // 2 (local)
}
console.log(count); // 0 (global, unchanged)

// ❌ Accidental global
function bad() {
  x = 10; // let/const/var নেই — global হয়ে যায়!
}
bad();
console.log(x); // 10 (leak!)

// ✅ Always use let/const
function good() {
  let x = 10; // local
}
```

---

## ১.১৩ Hoisting

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Hoisting** হলো JavaScript-এর এমন একটি behavior যেখানে variable এবং function declarations execution-এর আগে তাদের scope-এর শীর্ষে "তুলে" নেওয়া হয়।

### 🏠 বাস্তব জীবনের উদাহরণ

> একটি ক্লাসে পরীক্ষার আগের দিন শিক্ষক বললেন "কালকের পরীক্ষায় রহিম টপার হবে।" এটা হলো hoisting — ঘটনার আগেই declaration। কিন্তু রহিম আসলে পরীক্ষা দেওয়ার পরই result জানা যাবে (initialization)।

### 💻 Code Examples

```javascript
// ১. var hoisting — undefined পাওয়া যায়
console.log(myVar); // undefined (hoisted, কিন্তু value নেই)
var myVar = "Hello";
console.log(myVar); // "Hello"

// JavaScript আসলে এভাবে দেখে:
var myVar;           // ← হয়স্টেড শীর্ষে
console.log(myVar);  // undefined
myVar = "Hello";
console.log(myVar);  // "Hello"

// ২. let/const hoisting — TDZ (Temporal Dead Zone)
// console.log(myLet); // ReferenceError: Cannot access before initialization
let myLet = "World";

// ৩. Function Declaration — সম্পূর্ণ hoisted
sayHello(); // ✅ "Hello!" — declare করার আগে call করা যায়
function sayHello() {
  console.log("Hello!");
}

// ৪. Function Expression — NOT fully hoisted
// greet(); // TypeError: greet is not a function
var greet = function() {
  console.log("Greetings!");
};
// greet(); // এখন কাজ করবে

// ৫. Class Declaration — TDZ (hoisted but not initialized)
// const obj = new MyClass(); // ReferenceError
class MyClass {
  constructor() { this.name = "test"; }
}
```

### 📊 Hoisting সারাংশ

| Declaration Type | Hoisted? | Initial Value | TDZ? |
|-----------------|----------|---------------|------|
| `var` | ✅ হ্যাঁ | `undefined` | ❌ নেই |
| `let` | ✅ হ্যাঁ | — (TDZ) | ✅ আছে |
| `const` | ✅ হ্যাঁ | — (TDZ) | ✅ আছে |
| `function` declaration | ✅ হ্যাঁ | সম্পূর্ণ function | ❌ নেই |
| `function` expression | আংশিক | `undefined` | ❌ নেই |
| `class` | ✅ হ্যাঁ | — (TDZ) | ✅ আছে |

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Hoisting কী? কেন এটি জানা দরকার?"
>
> **আদর্শ উত্তর:** "Hoisting হলো JavaScript engine-এর এমন behavior যেখানে code execute হওয়ার আগে JS engine variable ও function declarations গুলো তাদের scope-এর শুরুতে move করে (conceptually)। তবে শুধু declaration hoisted হয়, initialization নয়। `var` hoisting-এ `undefined` পাওয়া যায়, `let`/`const`-এ Temporal Dead Zone-এর জন্য ReferenceError। Function declaration সম্পূর্ণ hoisted হয়, তাই declare করার আগে call করা যায়। এটি জানা দরকার কারণ unexpected bugs এড়াতে এবং code execution order বুঝতে।"

---

## ১.১৪ Closures

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Closure** হলো একটি function যেটি তার **outer function-এর variables মনে রাখে**, এমনকি outer function execute শেষ হওয়ার পরেও।

> সহজ কথায়: একটি function + সেটি যে lexical environment-এ তৈরি হয়েছে — এই দুটো মিলে closure।

### 🏠 বাস্তব জীবনের উদাহরণ

> ধরুন আপনি একটি backpack নিয়ে বাড়ি থেকে বের হলেন। Backpack-এ বাড়ির সব দরকারি জিনিস আছে। বাড়ি থেকে দূরে গেলেও backpack-এর জিনিস ব্যবহার করতে পারবেন। Closure হলো এই backpack — function তার environment carry করে।

### 💻 Closure Examples

```javascript
// ১. Basic Closure
function makeCounter() {
  let count = 0; // outer variable
  
  return function() {  // ← এটি closure
    count++;
    return count;
  };
}

const counter = makeCounter();
console.log(counter()); // 1
console.log(counter()); // 2
console.log(counter()); // 3
// count variable বাইরে থেকে directly access করা যায় না!

// ২. Multiple Closures — independent state
const counter1 = makeCounter();
const counter2 = makeCounter();
counter1(); // 1
counter1(); // 2
counter2(); // 1 (আলাদা count!)

// ৩. Closure for Data Privacy (Encapsulation)
function createBankAccount(initialBalance) {
  let balance = initialBalance; // private variable
  
  return {
    deposit(amount) {
      balance += amount;
      console.log(`Deposited ${amount}. Balance: ${balance}`);
    },
    withdraw(amount) {
      if (amount > balance) {
        console.log("Insufficient funds!");
        return;
      }
      balance -= amount;
      console.log(`Withdrawn ${amount}. Balance: ${balance}`);
    },
    getBalance() {
      return balance; // controlled access
    }
  };
}

const account = createBankAccount(1000);
account.deposit(500);   // Deposited 500. Balance: 1500
account.withdraw(200);  // Withdrawn 200. Balance: 1300
console.log(account.getBalance()); // 1300
// account.balance → undefined (private!)

// ৪. Closure in Loop — Classic Bug
// ❌ Bug with var
for (var i = 0; i < 3; i++) {
  setTimeout(function() {
    console.log(i); // 3, 3, 3 (সব একই i!)
  }, 1000);
}

// ✅ Fix 1: let (block-scoped)
for (let j = 0; j < 3; j++) {
  setTimeout(function() {
    console.log(j); // 0, 1, 2
  }, 1000);
}

// ✅ Fix 2: IIFE closure
for (var k = 0; k < 3; k++) {
  (function(k) {
    setTimeout(function() {
      console.log(k); // 0, 1, 2
    }, 1000);
  })(k);
}

// ৫. Closure for Memoization
function memoize(fn) {
  const cache = {};
  return function(...args) {
    const key = JSON.stringify(args);
    if (cache[key]) {
      console.log("Cache থেকে!");
      return cache[key];
    }
    cache[key] = fn(...args);
    return cache[key];
  };
}

const slowSquare = n => {
  // expensive calculation simulation
  return n * n;
};
const fastSquare = memoize(slowSquare);
console.log(fastSquare(5)); // 25 (calculated)
console.log(fastSquare(5)); // 25 (cache থেকে!)
```

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Closure কী? Real-world use case কী?"
>
> **আদর্শ উত্তর:** "Closure হলো একটি function যেটি তার outer lexical environment-এর variables remember করে, এমনকি outer function-এর execution শেষ হওয়ার পরেও। JavaScript-এ প্রতিটি function যখন তৈরি হয়, সে তার surrounding scope-এর reference ধরে রাখে — এটাই closure। Real-world use cases: (১) Data privacy — private variables তৈরি করা (module pattern), (২) Counter, accumulator তৈরি করা, (৩) Event handlers-এ state maintain করা, (৪) Currying ও partial application, (৫) Memoization।"

### ⚠️ Common Mistakes

```javascript
// ❌ Memory leak — closure unnecessarily holds references
function createLeak() {
  const largeData = new Array(1000000).fill("data");
  return function() {
    // largeData ব্যবহার না করলেও closure ধরে রাখে
    console.log("Hello");
  };
}
// ✅ Necessary references-ই ধরে রাখুন
```

---

## ১.১৫ Template Literals

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Template Literals** (বা Template Strings) হলো ES6-এ আসা backtick (`` ` ``) দিয়ে লেখা string যেখানে expressions embed করা যায়।

### 💻 Code Examples

```javascript
const name = "Rahim";
const age = 25;
const city = "Dhaka";

// ❌ পুরনো পদ্ধতি
const old = "আমার নাম " + name + ", বয়স " + age + ", শহর " + city;

// ✅ Template Literal
const modern = `আমার নাম ${name}, বয়স ${age}, শহর ${city}`;

// Expression evaluate করা যায়
console.log(`2 + 2 = ${2 + 2}`);           // "2 + 2 = 4"
console.log(`${age >= 18 ? "Adult" : "Minor"}`); // "Adult"

// Multiline string (সবচেয়ে বড় সুবিধা)
const html = `
  <div class="card">
    <h2>${name}</h2>
    <p>Age: ${age}</p>
    <p>City: ${city}</p>
  </div>
`;

// Function call
function toUpper(str) { return str.toUpperCase(); }
console.log(`${toUpper(name)}`); // "RAHIM"

// Nested template literals
const items = ["Apple", "Banana", "Mango"];
const list = `
  <ul>
    ${items.map(item => `<li>${item}</li>`).join("")}
  </ul>
`;

// Tagged Template Literals (Advanced)
function highlight(strings, ...values) {
  return strings.reduce((result, str, i) => {
    return result + str + (values[i] ? `<mark>${values[i]}</mark>` : "");
  }, "");
}
const highlighted = highlight`নাম: ${name}, বয়স: ${age}`;
// "নাম: <mark>Rahim</mark>, বয়স: <mark>25</mark>"
```

### 📊 Template Literals Features

| Feature | Example |
|---------|---------|
| String interpolation | `` `Hello ${name}` `` |
| Multi-line | `` `line1
line2` `` without `\n` |
| Expression | `` `${2 + 2}` `` |
| Function call | `` `${fn()}` `` |
| Ternary | `` `${x > 0 ? "pos" : "neg"}` `` |
| Tagged template | `` fn`hello ${name}` `` |

---

## ১.১৬ PART 1 — Interview Questions & Answers

<div align="right"><a href="#part1">⬆ PART 1 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

> এই section-এ PART 1-এর সব topics থেকে গুরুত্বপূর্ণ interview questions ও বিস্তারিত answers আছে।

<details>
<summary><strong>🔹 JavaScript Basics (Q1–Q10)</strong></summary>
<br>

**Q1: JavaScript কী এবং কেন এত popular?**
> **A:** JavaScript একটি high-level, interpreted, dynamically-typed, multi-paradigm programming language। Popular কারণ: (১) Browser-এর একমাত্র native language, (২) Node.js দিয়ে backend-এও চলে, (৩) বিশাল ecosystem (npm), (৪) Versatile — web, mobile, desktop সব জায়গায়, (৫) Easy to learn।

**Q2: JavaScript কি compiled নাকি interpreted?**
> **A:** JavaScript মূলত interpreted, কিন্তু আধুনিক engines (V8) JIT (Just-In-Time) compilation ব্যবহার করে। Parse → Bytecode → Optimized Machine Code। তাই technically "interpreted + JIT compiled"।

**Q3: ECMAScript কী?**
> **A:** ECMAScript হলো JavaScript-এর official standard, ECMA International দ্বারা maintained। ES6 (2015), ES7 (2016) এভাবে versions। JavaScript হলো এই standard-এর implementation।

**Q4: var, let, const-এর পার্থক্য?**
> **A:** Scope: var=function, let/const=block। Hoisting: var=undefined, let/const=TDZ error। Re-declare: var=✅, let/const=❌। Re-assign: var/let=✅, const=❌। Best practice: const সবসময়, পরিবর্তনযোগ্য হলে let, var কখনো নয়।

**Q5: Primitive এবং Reference type-এর পার্থক্য?**
> **A:** Primitive (Number, String, Boolean, null, undefined, Symbol, BigInt): stack-এ store, value copy হয়। Reference (Object, Array, Function): heap-এ store, reference copy হয়। তাই reference type-এ একটি পরিবর্তন সব references-এ দেখা যায়।

**Q6: typeof null কেন "object"?**
> **A:** JavaScript-এর একটি historical bug। 1995 সালে যখন JS তৈরি, type information bits-এ store হতো। null-এর bits ছিল 000 যা object-এর tag ছিল। এই bug backward compatibility-র জন্য এখনও আছে। null check করতে `=== null` ব্যবহার করুন।

**Q7: == এবং === এর পার্থক্য?**
> **A:** `==` (loose equality): type coercion করে, তারপর compare। `===` (strict equality): type coercion করে না। Best practice: সবসময় `===` — কারণ `==` এর coercion rules confusing (`0 == false // true`, `"" == false // true`)।

**Q8: Truthy এবং Falsy value কী?**
> **A:** Falsy (মাত্র 6টি): `false`, `0`, `""`, `null`, `undefined`, `NaN`। বাকি সব truthy। Trick: `[]` এবং `{}` truthy! `"0"` truthy! `-1` truthy!

**Q9: Hoisting কী?**
> **A:** JS engine code execute করার আগে variable/function declarations scope-এর শীর্ষে নিয়ে যায়। `var` → undefined দিয়ে initialize। `let`/`const` → TDZ (Temporal Dead Zone), access করলে ReferenceError। Function declaration → সম্পূর্ণ hoisted। Function expression → শুধু variable part hoisted।

**Q10: Closure কী? কেন গুরুত্বপূর্ণ?**
> **A:** Closure হলো inner function যেটি outer function-এর variables মনে রাখে execution শেষেও। Important কারণ: data privacy, stateful functions, module pattern, currying, memoization। JavaScript-এর অনেক advanced pattern closure-এর উপর নির্ভরশীল।

</details>

<details>
<summary><strong>🔹 Functions & Scope (Q11–Q20)</strong></summary>
<br>

**Q11: Arrow function কী? Regular function থেকে কীভাবে আলাদা?**
> **A:** Arrow function ES6-এর সংক্ষিপ্ত syntax। পার্থক্য: (১) `this` — arrow lexical this, regular function নিজের this, (২) `arguments` object — arrow-এ নেই, (৩) Constructor — arrow function constructor হিসেবে ব্যবহার করা যায় না, (৪) `prototype` — arrow-এ নেই।

**Q12: Lexical scope কী?**
> **A:** Lexical scope মানে scope function কোথায় **লেখা** হয়েছে তার উপর নির্ভর করে, কোথায় **call** হয়েছে তার উপর নয়। Inner function সবসময় outer function-এর variables access করতে পারে — এটাই lexical scoping।

**Q13: Scope chain কী?**
> **A:** কোনো variable খুঁজতে JS প্রথমে current scope দেখে, না পেলে outer scope, তারপর আরও outer — global scope পর্যন্ত। এই chain-কেই scope chain বলে।

**Q14: IIFE কী এবং কেন ব্যবহার করা হয়?**
> **A:** Immediately Invoked Function Expression — `(function() { ... })()` — declare হওয়ার সাথে সাথে execute হয়। ব্যবহার: (১) Global scope pollution এড়ানো, (২) Private variables তৈরি, (৩) Module pattern, (৪) পুরনো browser-এ block scope simulate করা।

**Q15: Higher-Order Function কী?**
> **A:** যে function অন্য function-কে argument হিসেবে নেয় অথবা function return করে। উদাহরণ: `Array.map()`, `Array.filter()`, `Array.reduce()`। JavaScript-এ functional programming-এর মূল ভিত্তি।

**Q16: Callback function কী?**
> **A:** Callback হলো একটি function যেটি অন্য function-এ argument হিসেবে পাঠানো হয় এবং পরে call করা হয়। Asynchronous operation-এ widely used: `setTimeout(callback, 1000)`, event handlers, API calls।

**Q17: Pure function কী?**
> **A:** Pure function-এর দুটো বৈশিষ্ট্য: (১) Same input-এ সবসময় same output, (২) Side effects নেই (বাইরের কিছু পরিবর্তন করে না)। Functional programming-এর মূল নীতি — predictable, testable।

**Q18: Temporal Dead Zone কী?**
> **A:** `let`/`const` variable declare হওয়ার আগের time period যেখানে variable technically exist করে কিন্তু access করা যায় না। Access করলে `ReferenceError`। এটি intentional — declare করার আগে ব্যবহার করা programming bug।

**Q19: Function-এ default parameter কীভাবে কাজ করে?**
> **A:** ES6 থেকে `function greet(name = "Guest")` এভাবে default value দেওয়া যায়। Argument `undefined` বা দেওয়া না হলে default value ব্যবহার হয়। `null` দিলে কিন্তু null-ই থাকে।

**Q20: Rest parameters কী?**
> **A:** `function sum(...numbers)` — যেকোনো সংখ্যক arguments কে array হিসেবে collect করে। পুরনো `arguments` object এর modern alternative। Arrow function-এও কাজ করে।

</details>

<details>
<summary><strong>🔹 Data Types & Operators (Q21–Q30)</strong></summary>
<br>

**Q21: NaN কী? কীভাবে check করবেন?**
> **A:** NaN = "Not a Number"। Type: `number`। উৎপত্তি: `"abc" * 2`, `0/0`। Special: `NaN === NaN` is `false`! Check: `Number.isNaN(value)` — global `isNaN()` এড়িয়ে চলুন (coercion করে)।

**Q22: null, undefined, NaN-এর মধ্যে পার্থক্য?**
> **A:** `undefined` = value assign হয়নি (JS দেয়)। `null` = programmer intentionally "no value" সেট করেছে। `NaN` = invalid math result, type হলো number। `null == undefined` true, কিন্তু `null === undefined` false।

**Q23: JavaScript-এ সব falsy values কী?**
> **A:** `false`, `0`, `-0`, `0n` (BigInt zero), `""` (empty string), `null`, `undefined`, `NaN`। মনে রাখুন: `[]` এবং `{}` truthy।

**Q24: typeof operator কী return করে?**
> **A:** `"number"`, `"string"`, `"boolean"`, `"undefined"`, `"object"` (null-এর জন্যও!), `"symbol"`, `"bigint"`, `"function"`। Array-এর জন্য "object" — তাই `Array.isArray()` ব্যবহার করুন।

**Q25: Short-circuit evaluation কী?**
> **A:** `&&` — বাম দিক falsy হলে বাম দিক return, নইলে ডান দিক। `||` — বাম দিক truthy হলে বাম দিক return, নইলে ডান দিক। Default value pattern: `let name = input || "Guest"`।

**Q26: Nullish coalescing operator (??) কী?**
> **A:** ES2020। `??` — বাম দিক `null` বা `undefined` হলে ডান দিক return করে, অন্য falsy value (`0`, `""`, `false`) হলে বাম দিকই return করে। `||` এর সাথে পার্থক্য এখানেই।

**Q27: Optional chaining (?.) কী?**
> **A:** ES2020। `obj?.prop` — obj null/undefined হলে `undefined` return করে, error throw করে না। Deep object navigation-এ safe: `user?.address?.city`। Function call-এও: `obj?.method()`।

**Q28: Type Coercion কী? কখন হয়?**
> **A:** JavaScript automatically type convert করে। উদাহরণ: `"5" + 3 = "53"` (number → string), `"5" - 3 = 2` (string → number), `if (value)` (any → boolean)। `==` comparison-এ coercion হয়, `===`-এ হয় না।

**Q29: Deep copy এবং Shallow copy কীভাবে করবেন?**
> **A:** Shallow copy: `Object.assign({}, obj)`, spread `{...obj}`, `[...arr]`। Deep copy: `JSON.parse(JSON.stringify(obj))` (function/undefined/Symbol হারায়), `structuredClone(obj)` (modern, safe), Lodash `_.cloneDeep()`।

**Q30: Symbol কী? কখন ব্যবহার করবেন?**
> **A:** Symbol হলো ES6-এর unique primitive type। `Symbol("id") !== Symbol("id")` — প্রতিটি Symbol unique। ব্যবহার: unique object keys (collision এড়ানো), private-like properties, well-known symbols (`Symbol.iterator`)।

</details>

---

<div align="right">
  <a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a>
</div>

---

> **🚀 PART 2 আসছে:** Advanced JavaScript — Execution Context, Call Stack, Event Loop, Promises, Async/Await, Prototype Chain এবং আরও অনেক কিছু।
>
> **💬 পরবর্তী PART পেতে:** "PART 2 দাও" বা "Next" লিখুন।


---

<a id="part2"></a>

# PART 2 — Advanced JavaScript

> **📍 এই PART-এর Sections:** [২.১ Execution Context](#২১-execution-context) · [২.২ Call Stack](#২২-call-stack) · [২.৩ Memory Heap](#২৩-memory-heap) · [২.৪ Event Loop](#২৪-event-loop) · [২.৫ Callback Queue](#২৫-callback-queue--microtask-queue) · [২.৬ Callback Functions](#২৬-callback-functions) · [২.৭ Promises](#২৭-promises) · [২.৮ Async/Await](#২৮-asyncawait) · [২.৯ Fetch API](#২৯-fetch-api) · [২.১০ this keyword](#২১০-this-keyword) · [২.১১ bind, call, apply](#২১১-bind-call-apply) · [২.১২ Prototype](#২১২-prototype) · [২.১৩ Prototype Chain](#২১৩-prototype-chain) · [২.১৪ Inheritance](#২১৪-inheritance-in-javascript) · [২.১৫ Classes](#২১৫-classes) · [২.১৬ Modules](#২১৬-modules) · [২.১৭ Debouncing & Throttling](#২১৭-debouncing--throttling) · [২.১৮ Currying](#২১৮-currying) · [২.১৯ Memoization](#২১৯-memoization) · [২.২০ Interview Q&A](#২২০-part-2--interview-questions--answers)

---

## ২.১ Execution Context

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Execution Context** হলো JavaScript code execute হওয়ার পরিবেশ (environment)। প্রতিটি JS code একটি Execution Context-এর মধ্যে চলে।

### 🏠 বাস্তব জীবনের উদাহরণ

> একটি মঞ্চ নাটকের কথা ভাবুন। প্রতিটি দৃশ্যের (scene) জন্য আলাদা সেট থাকে — আলো, পর্দা, props। প্রতিটি function call একটি নতুন "দৃশ্য" তৈরি করে যার নিজস্ব variables, scope, `this` আছে।

### 📊 Execution Context-এর প্রকারভেদ

| ধরন | কখন তৈরি হয় | কতটি থাকে |
|-----|-------------|-----------|
| **Global Execution Context (GEC)** | Program শুরুতে | শুধু একটি |
| **Function Execution Context (FEC)** | প্রতিটি function call-এ | প্রতিটি call-এ নতুন |
| **Eval Execution Context** | `eval()` এ | এড়িয়ে চলুন |

### ⚙️ Execution Context-এ কী থাকে?

```
Execution Context
├── Variable Environment
│   ├── Variables (var)
│   ├── Function declarations
│   └── arguments object
├── Lexical Environment
│   ├── let, const
│   └── Outer environment reference (scope chain)
└── this binding
```

### 💻 দুটি Phase

```javascript
// Phase 1: Creation Phase (Memory Allocation)
// Phase 2: Execution Phase (Code runs line by line)

var name = "Rahim";      // Phase 1: name = undefined
                          // Phase 2: name = "Rahim"

function greet() {        // Phase 1: greet = function (fully hoisted)
  var msg = "Hello";     // নতুন FEC তৈরি
  console.log(msg);
}

greet();                  // Phase 2: FEC তৈরি, execute, destroy
```

### 📊 Execution Context Lifecycle

```
GEC তৈরি
  ↓
Creation Phase: var hoisting (undefined), function declarations, this setup
  ↓
Execution Phase: code line by line
  ↓
greet() call → FEC তৈরি
  ↓
FEC Creation Phase → FEC Execution Phase
  ↓
greet() শেষ → FEC destroy
  ↓
GEC চলতে থাকে
```

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Execution Context কী? এটি কীভাবে কাজ করে?"
>
> **আদর্শ উত্তর:** "Execution Context হলো JavaScript code execute হওয়ার পরিবেশ। দুটি প্রধান type: Global Execution Context (program শুরুতে একটি তৈরি হয়) এবং Function Execution Context (প্রতিটি function call-এ নতুন তৈরি হয়)। প্রতিটি context দুটি phase-এ কাজ করে: Creation Phase — variable declarations hoisted হয়, `var` undefined পায়, function declarations fully hoisted হয়, `this` set হয়। Execution Phase — code line by line execute হয়। Function শেষ হলে তার context destroy হয়।"

---

## ২.২ Call Stack

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Call Stack** হলো একটি **LIFO (Last In, First Out)** data structure যেখানে JS engine Execution Contexts track করে। JavaScript single-threaded — একসময় একটি কাজ, এই stack দিয়ে manage করা হয়।

### 🏠 বাস্তব জীবনের উদাহরণ

> থালা বাসনের স্তূপের কথা ভাবুন। নতুন থালা উপরে রাখা হয়, তুলতেও উপর থেকে নেওয়া হয়। function call = নতুন থালা রাখা, function return = থালা তোলা।

### 💻 Call Stack Visualization

```javascript
function multiply(a, b) {
  return a * b;           // 3rd — এখানে calculate হয়
}

function square(n) {
  return multiply(n, n);  // 2nd — multiply কে call করে
}

function printSquare(n) {
  const result = square(n); // 1st — square কে call করে
  console.log(result);
}

printSquare(5);

/*  Call Stack এভাবে দেখায়:

    Step 1: [GEC]
    Step 2: [GEC] [printSquare]
    Step 3: [GEC] [printSquare] [square]
    Step 4: [GEC] [printSquare] [square] [multiply]
    Step 5: [GEC] [printSquare] [square] (multiply returns 25)
    Step 6: [GEC] [printSquare] (square returns 25)
    Step 7: [GEC] (printSquare logs 25, returns)
    Step 8: [GEC]
*/
```

### 🔥 Stack Overflow

```javascript
// Recursive function without base case
function infinite() {
  return infinite(); // নিজেকেই call করে থাকে
}

infinite(); // Uncaught RangeError: Maximum call stack size exceeded
```

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Call Stack কী? Stack Overflow কেন হয়?"
>
> **আদর্শ উত্তর:** "Call Stack হলো LIFO data structure যেখানে JavaScript engine function calls track করে। প্রতিটি function call একটি frame (stack frame) push করে। Function return হলে frame pop হয়। JavaScript single-threaded, তাই একসময় একটিই function execute হয় — Call Stack-এর top frame। Stack Overflow হয় যখন function বারবার নিজেকে call করে (infinite recursion) এবং stack-এর maximum size অতিক্রম করে। Chrome-এ এই limit প্রায় ১০,০০০ থেকে ১৫,০০০।"

---

## ২.৩ Memory Heap

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Memory Heap** হলো unstructured memory যেখানে JavaScript objects, arrays, functions store হয়। Stack-এ primitive values ও references store হয়, Heap-এ actual objects।

```
Memory Layout:
┌─────────────────┐  ┌─────────────────────────────┐
│    CALL STACK   │  │         MEMORY HEAP         │
│                 │  │                             │
│  let x = 10    │  │  { name: "Rahim" }  ←──┐   │
│  let obj ──────┼──┼──►                      │   │
│  (reference)   │  │  [1, 2, 3]              │   │
│                 │  │  function() {}          │   │
└─────────────────┘  └─────────────────────────────┘
```

### 🗑️ Garbage Collection

JS engine automatically unreachable objects কে Heap থেকে সরিয়ে দেয় — এটা **Garbage Collection**। V8 **Mark-and-Sweep** algorithm ব্যবহার করে।

```javascript
function example() {
  let obj = { name: "Rahim" }; // Heap-এ তৈরি
  // function শেষ হলে obj-এর reference নেই
  // Garbage Collector এটি পরিষ্কার করবে
}
example();

// Memory Leak উদাহরণ
let leakedObjects = [];
function leak() {
  leakedObjects.push(new Array(10000).fill("data")); // reference রয়ে যাচ্ছে!
}
```

---

## ২.৪ Event Loop

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Event Loop** হলো JavaScript-এর সেই mechanism যা single-threaded হওয়া সত্ত্বেও asynchronous operations handle করতে দেয়।

### 🏠 বাস্তব জীবনের উদাহরণ

> একজন রেস্টুরেন্টের ওয়েটার কল্পনা করুন। সে একসময় একজন customer serve করতে পারে (single-threaded)। কিন্তু রান্না হওয়ার সময় (async) অন্য customer নেয়। রান্না শেষে notification পেলে আবার সেই customer-এ যায়। Event Loop এই ওয়েটার।

### 📊 Complete Picture

```
┌─────────────────────────────────────────────────────────────┐
│                     Browser / Node.js                       │
│                                                             │
│  ┌──────────────┐    ┌─────────────────────────────────┐  │
│  │  Call Stack  │    │           Web APIs               │  │
│  │              │    │  setTimeout, fetch, DOM events   │  │
│  │  [main()]    │    │  (Browser এর অংশ, JS নয়)       │  │
│  │              │    └──────────────────┬──────────────┘  │
│  └──────┬───────┘                       │                  │
│         │                               ▼                  │
│         │                    ┌──────────────────────┐      │
│         │     Event Loop     │   Callback Queue     │      │
│         │ ◄──────────────────│   (Macrotask Queue)  │      │
│         │  Stack খালি হলে   │   [cb1, cb2, ...]    │      │
│         │  queue থেকে নেয়  └──────────────────────┘      │
│         │                    ┌──────────────────────┐      │
│         │  ◄─────────────────│   Microtask Queue    │      │
│         │  Macrotask আগে!   │   [Promise.then...]  │      │
│                              └──────────────────────┘      │
└─────────────────────────────────────────────────────────────┘
```

### 💻 Dry Run — Event Loop

```javascript
console.log("1: Start");              // ① Sync — তাৎক্ষণিক

setTimeout(() => {
  console.log("2: Timeout");          // ④ Macrotask queue — শেষে
}, 0);

Promise.resolve()
  .then(() => console.log("3: Promise")); // ③ Microtask queue — Timeout এর আগে

console.log("4: End");                // ② Sync — তাৎক্ষণিক

/*
Output:
1: Start
4: End
3: Promise    ← Microtask (Promise) আগে
2: Timeout    ← Macrotask (setTimeout) পরে
*/
```

### 🔍 Event Loop Algorithm

```
1. Call Stack খালি না হওয়া পর্যন্ত execute করো
2. Microtask Queue সম্পূর্ণ খালি করো (Promise callbacks)
3. Callback Queue থেকে একটি Macrotask নাও
4. আবার ১ থেকে শুরু
```

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "JavaScript single-threaded হওয়ার পরও async কাজ কীভাবে করে?"
>
> **আদর্শ উত্তর:** "JavaScript single-threaded — একটি Call Stack, একসময় একটি কাজ। কিন্তু async operations যেমন `setTimeout`, `fetch` ব্রাউজারের Web APIs-এ যায় — JS engine এগুলো wait করে না। Web API কাজ শেষ করলে callback Callback Queue-এ যায়। Event Loop সবসময় দেখে — Call Stack খালি কিনা। খালি হলে Microtask Queue সম্পূর্ণ drain করে (Promise callbacks), তারপর Callback Queue থেকে একটি Macrotask নেয়। এভাবে non-blocking behavior অর্জন করা হয়।"

### ⚠️ Common Mistakes

```javascript
// ❌ setTimeout(fn, 0) মানে "সঙ্গে সঙ্গে" নয়
setTimeout(() => console.log("এটা পরে আসবে"), 0);
console.log("এটা আগে আসবে");

// ❌ Microtask vs Macrotask ভুল ধারণা
// Microtask (Promise.then, queueMicrotask, MutationObserver) → সবসময় setTimeout আগে
```

---

## ২.৫ Callback Queue & Microtask Queue

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📊 Macrotask vs Microtask

| | Macrotask Queue | Microtask Queue |
|--|----------------|----------------|
| **নাম** | Callback Queue / Task Queue | Microtask Queue / Job Queue |
| **কী যায়** | `setTimeout`, `setInterval`, `setImmediate`, I/O, UI rendering | `Promise.then/catch/finally`, `queueMicrotask`, `MutationObserver` |
| **Priority** | কম | বেশি (Macrotask এর আগে) |
| **একবারে কতটি** | একটি Macrotask | সব Microtasks drain হয় |

### 💻 Detailed Example

```javascript
console.log("Script start");      // 1

setTimeout(() => {
  console.log("setTimeout");      // 5
}, 0);

Promise.resolve()
  .then(() => {
    console.log("Promise 1");     // 3
  })
  .then(() => {
    console.log("Promise 2");     // 4
  });

console.log("Script end");        // 2

/*
Output:
Script start   ← sync
Script end     ← sync
Promise 1      ← microtask
Promise 2      ← microtask (Promise chain)
setTimeout     ← macrotask (সবার শেষে)
*/
```

### 💡 Memory Tip

> **"Micro আগে, Macro পরে"** — Promise (micro) সবসময় setTimeout (macro) এর আগে।

---

## ২.৬ Callback Functions

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Callback Function** হলো একটি function যেটি অন্য function-এ argument হিসেবে পাঠানো হয় এবং পরে (বা asynchronously) call করা হয়।

### 💻 Code Examples

```javascript
// ১. Synchronous Callback
function greet(name, callback) {
  console.log(`Hello, ${name}!`);
  callback();
}

greet("Rahim", () => {
  console.log("Callback executed!");
});

// ২. Asynchronous Callback
function fetchData(url, onSuccess, onError) {
  // Simulating async operation
  setTimeout(() => {
    const success = true;
    if (success) {
      onSuccess({ data: "User data" });
    } else {
      onError(new Error("Fetch failed"));
    }
  }, 1000);
}

fetchData(
  "https://api.example.com",
  (result) => console.log("Success:", result),
  (err) => console.error("Error:", err)
);

// ৩. Callback Hell (Pyramid of Doom) — সমস্যা
getUser(userId, (user) => {
  getPosts(user.id, (posts) => {
    getComments(posts[0].id, (comments) => {
      getLikes(comments[0].id, (likes) => {
        // আরও nested... বোঝা কঠিন!
        console.log(likes);
      });
    });
  });
});

// ✅ Solution: Promises অথবা Async/Await
```

### ⚠️ Callback Hell কেন সমস্যা?

- Readability কমে যায়
- Error handling কঠিন হয়
- Debug করা কঠিন
- Code maintain করা কঠিন

---

## ২.৭ Promises

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Promise** হলো future-এ complete হবে এমন একটি asynchronous operation-এর representation। এটি callback hell-এর সমাধান।

### 🏠 বাস্তব জীবনের উদাহরণ

> Online-এ বই order করলে একটি **tracking number** পান। এটাই Promise — এখনো বই পাননি, কিন্তু একটি commitment পেয়েছেন। বই আসলে (fulfilled) নিন, না আসলে (rejected) complaint করুন।

### 📊 Promise States

```
                  ┌─────────────┐
                  │   PENDING   │ ← শুরুর অবস্থা
                  └──────┬──────┘
              ____________│____________
             │                        │
             ▼                        ▼
      ┌─────────────┐         ┌─────────────┐
      │  FULFILLED  │         │  REJECTED   │
      │  (success)  │         │  (failure)  │
      └─────────────┘         └─────────────┘
```

### 💻 Promise তৈরি ও ব্যবহার

```javascript
// ১. Promise তৈরি
const myPromise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("Data loaded successfully!"); // fulfilled
  } else {
    reject(new Error("Something went wrong!")); // rejected
  }
});

// ২. Promise ব্যবহার
myPromise
  .then((result) => {
    console.log("✅ Success:", result);
    return result.toUpperCase(); // chaining!
  })
  .then((upperResult) => {
    console.log("✅ Uppercase:", upperResult);
  })
  .catch((error) => {
    console.error("❌ Error:", error.message);
  })
  .finally(() => {
    console.log("🏁 Always runs (loading spinner বন্ধ)");
  });

// ৩. Practical API example
function fetchUser(id) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (id > 0) {
        resolve({ id, name: "Rahim", email: "rahim@example.com" });
      } else {
        reject(new Error("Invalid user ID"));
      }
    }, 1000);
  });
}

fetchUser(1)
  .then(user => {
    console.log("User:", user.name);
    return fetchUser(2); // chaining
  })
  .then(user2 => console.log("User2:", user2.name))
  .catch(err => console.error(err.message));
```

### 💻 Promise Static Methods

```javascript
const p1 = Promise.resolve("First");
const p2 = new Promise(resolve => setTimeout(() => resolve("Second"), 1000));
const p3 = new Promise((_, reject) => setTimeout(() => reject("Error!"), 500));

// ১. Promise.all — সব resolve হলে এগোয়, একটা reject হলে সব reject
Promise.all([p1, p2])
  .then(results => console.log(results)) // ["First", "Second"]
  .catch(err => console.error(err));

// ২. Promise.allSettled — সব complete হওয়ার পর সব result (ES2020)
Promise.allSettled([p1, p3])
  .then(results => results.forEach(r => console.log(r.status, r.value || r.reason)));
// {status: "fulfilled", value: "First"}
// {status: "rejected", reason: "Error!"}

// ৩. Promise.race — যেটি আগে settle করবে সেটি
Promise.race([p2, p3])
  .then(result => console.log("Winner:", result))
  .catch(err => console.error("First to fail:", err)); // p3 আগে reject

// ৪. Promise.any — যেটি আগে fulfill করবে (ES2021)
Promise.any([p3, p1])
  .then(result => console.log("First fulfilled:", result)); // "First"
```

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Promise কী? .then(), .catch(), .finally() কীভাবে কাজ করে?"
>
> **আদর্শ উত্তর:** "Promise হলো একটি object যা future-এ complete হবে এমন async operation represent করে। তিনটি state: pending (অপেক্ষায়), fulfilled (সফল), rejected (ব্যর্থ)। `.then()` — fulfilled হলে run হয়, একটি নতুন Promise return করে তাই chaining সম্ভব। `.catch()` — rejected হলে অথবা .then()-এ error হলে run হয়। `.finally()` — সফল বা ব্যর্থ যাই হোক, সবসময় run হয় — loading indicator বন্ধ করতে useful।"

---

## ২.৮ Async/Await

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Async/Await** হলো Promise-এর উপরে built একটি syntactic sugar যা asynchronous code-কে synchronous-এর মতো পড়তে ও লিখতে সাহায্য করে। ES2017 (ES8) এ আসে।

### 💻 Promise vs Async/Await তুলনা

```javascript
// ❌ Promise chain (readable কিন্তু nested)
function getUserData(userId) {
  return fetchUser(userId)
    .then(user => fetchPosts(user.id))
    .then(posts => fetchComments(posts[0].id))
    .then(comments => console.log(comments))
    .catch(err => console.error(err));
}

// ✅ Async/Await (অনেক পরিষ্কার)
async function getUserData(userId) {
  try {
    const user = await fetchUser(userId);     // wait করে
    const posts = await fetchPosts(user.id);  // তারপর এটি
    const comments = await fetchComments(posts[0].id);
    console.log(comments);
  } catch (err) {
    console.error(err);
  }
}
```

### 💻 Async/Await বিস্তারিত

```javascript
// ১. async function সবসময় Promise return করে
async function getValue() {
  return 42;
}
getValue().then(v => console.log(v)); // 42 (Promise wrapped)

// ২. await শুধু async function-এর ভেতরে
async function fetchData() {
  console.log("Fetching...");
  const data = await new Promise(resolve =>
    setTimeout(() => resolve("Data!"), 1000)
  );
  console.log("Got:", data); // 1 second পরে
}

// ৩. Error Handling
async function riskyOperation() {
  try {
    const result = await someAsyncThing();
    return result;
  } catch (error) {
    console.error("Caught:", error.message);
    throw error; // re-throw যদি দরকার
  } finally {
    console.log("Cleanup");
  }
}

// ৪. Parallel execution — await একটি একটি করে না!
async function sequential() {
  const a = await fetchA(); // 2 seconds wait
  const b = await fetchB(); // আরও 2 seconds wait
  // মোট: 4 seconds
}

async function parallel() {
  const [a, b] = await Promise.all([fetchA(), fetchB()]); // একসাথে
  // মোট: 2 seconds (যেটি বেশি সময় নেয়)
}

// ৫. for...of এর সাথে await (sequential)
const userIds = [1, 2, 3];
async function processAll() {
  for (const id of userIds) {
    const user = await fetchUser(id);
    console.log(user.name);
  }
}

// ৬. forEach এ await — কাজ করে না!
async function wrong() {
  userIds.forEach(async (id) => {
    const user = await fetchUser(id); // ❌ await এখানে ঠিকমতো কাজ করে না
  });
}
```

### ⚠️ Common Mistakes

```javascript
// ❌ Top-level await — শুধু module-এ কাজ করে
const data = await fetch("..."); // SyntaxError (non-module context)

// ❌ forEach এর ভেতরে await
arr.forEach(async item => {
  await doSomething(item); // forEach await এর জন্য wait করে না!
});
// ✅ for...of বা Promise.all ব্যবহার করুন

// ❌ Sequential যখন Parallel হওয়া উচিত
const user = await fetchUser(id);
const settings = await fetchSettings(id); // user-এর উপর নির্ভরশীল নয়!
// ✅ Parallel করুন:
const [user, settings] = await Promise.all([fetchUser(id), fetchSettings(id)]);
```

---

## ২.৯ Fetch API

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Fetch API** হলো browser-এর built-in API যা HTTP requests করতে ব্যবহৃত হয়। `XMLHttpRequest`-এর আধুনিক বিকল্প।

### 💻 Fetch Examples

```javascript
// ১. GET request
async function getUsers() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/users");

    if (!response.ok) { // HTTP error check (4xx, 5xx)
      throw new Error(`HTTP Error: ${response.status}`);
    }

    const users = await response.json();
    console.log(users);
  } catch (error) {
    console.error("Fetch failed:", error.message);
  }
}

// ২. POST request
async function createUser(userData) {
  try {
    const response = await fetch("https://api.example.com/users", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "Authorization": "Bearer " + token
      },
      body: JSON.stringify(userData)
    });

    const newUser = await response.json();
    return newUser;
  } catch (error) {
    throw new Error("User creation failed: " + error.message);
  }
}

// ৩. PUT / DELETE
async function updateUser(id, data) {
  const response = await fetch(`/api/users/${id}`, {
    method: "PUT",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify(data)
  });
  return response.json();
}

async function deleteUser(id) {
  const response = await fetch(`/api/users/${id}`, { method: "DELETE" });
  return response.ok;
}
```

### ⚠️ Fetch-এর Gotcha

```javascript
// ❌ Network error ছাড়া fetch কখনো reject করে না!
const response = await fetch("https://api.example.com/bad-endpoint");
// 404, 500 — এগুলো reject করে না, response.ok = false হয়

// ✅ সবসময় response.ok check করুন
if (!response.ok) {
  throw new Error(`HTTP ${response.status}: ${response.statusText}`);
}
```

---

## ২.১০ this keyword

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**`this`** হলো JavaScript-এর একটি special keyword যা function-এর execution context-এ current object-কে refer করে। `this`-এর value নির্ধারিত হয় function **কীভাবে call হয়েছে** তার উপর।

### 🏠 বাস্তব জীবনের উদাহরণ

> "আমি কে?" — এই প্রশ্নের উত্তর নির্ভর করে কে জিজ্ঞেস করছে। classroom-এ teacher বললে "teacher", student বললে "student"। `this` এভাবেই context অনুযায়ী পরিবর্তন হয়।

### 💻 this-এর বিভিন্ন Context

```javascript
// ১. Global context
console.log(this); // Browser: window, Node.js: {}

// ২. Regular Function — Global context (non-strict) বা undefined (strict)
function regularFn() {
  console.log(this); // Window / undefined (strict mode)
}
regularFn();

// ৩. Method — Object যে call করছে
const user = {
  name: "Rahim",
  greet() {
    console.log(`Hello, ${this.name}`); // this = user object
  }
};
user.greet(); // "Hello, Rahim"

// ৪. Method বের করে call করলে this হারায়!
const { greet } = user;
greet(); // "Hello, undefined" (this = Window!)

// ৫. Arrow Function — Lexical this (outer scope থেকে inherit)
const obj = {
  name: "Rahim",
  greetArrow: () => {
    console.log(this.name); // ❌ this = Window (outer scope)
  },
  greetRegular() {
    const inner = () => {
      console.log(this.name); // ✅ this = obj (outer regular function থেকে)
    };
    inner();
  }
};

// ৬. Constructor Function
function Person(name) {
  this.name = name; // this = নতুন object (new দিয়ে call করলে)
}
const rahim = new Person("Rahim");
console.log(rahim.name); // "Rahim"

// ৭. Event Handler
button.addEventListener("click", function() {
  console.log(this); // this = button element
});

button.addEventListener("click", () => {
  console.log(this); // this = Window (arrow function!)
});

// ৮. Class
class Animal {
  constructor(name) {
    this.name = name;
  }
  speak() {
    console.log(`${this.name} makes a sound`);
  }
}
```

### 📊 this Summary

| Context | this-এর মান |
|---------|------------|
| Global (browser) | `window` |
| Global (Node.js) | `{}` (module) |
| Regular function (non-strict) | `window` |
| Regular function (strict) | `undefined` |
| Method | Method owner object |
| Arrow function | Enclosing lexical scope-এর this |
| Constructor (`new`) | নতুন তৈরি object |
| Event handler (regular) | Event target element |
| `call`/`apply`/`bind` | Explicitly set করা object |

---

## ২.১১ bind, call, apply

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

তিনটিই `Function.prototype`-এর method যা `this`-এর value manually set করতে দেয়।

### 💻 Code Examples

```javascript
const person1 = { name: "Rahim", age: 25 };
const person2 = { name: "Karim", age: 30 };

function introduce(greeting, punctuation) {
  console.log(`${greeting}, আমি ${this.name}, বয়স ${this.age}${punctuation}`);
}

// ১. call — সঙ্গে সঙ্গে call করে, arguments আলাদা আলাদা
introduce.call(person1, "হ্যালো", "!");
// "হ্যালো, আমি Rahim, বয়স 25!"

introduce.call(person2, "নমস্কার", "।");
// "নমস্কার, আমি Karim, বয়স 30।"

// ২. apply — সঙ্গে সঙ্গে call করে, arguments array হিসেবে
introduce.apply(person1, ["হ্যালো", "!"]);
// "হ্যালো, আমি Rahim, বয়স 25!"

// apply-এর practical use: spread-এর আগে
const numbers = [3, 1, 4, 1, 5, 9];
console.log(Math.max.apply(null, numbers)); // 9
// Modern: Math.max(...numbers)

// ৩. bind — নতুন function return করে (call করে না)
const greetRahim = introduce.bind(person1, "হ্যালো");
// later...
greetRahim("!"); // "হ্যালো, আমি Rahim, বয়স 25!"
greetRahim("?"); // "হ্যালো, আমি Rahim, বয়স 25?"

// Practical use of bind
class Timer {
  constructor() {
    this.seconds = 0;
  }
  start() {
    // bind না করলে this হারাবে
    setInterval(this.tick.bind(this), 1000);
  }
  tick() {
    this.seconds++;
    console.log(this.seconds);
  }
}
```

### 📊 call vs apply vs bind

| | `call` | `apply` | `bind` |
|-|--------|---------|--------|
| **কখন execute হয়** | তাৎক্ষণিক | তাৎক্ষণিক | পরে (returns function) |
| **Arguments** | আলাদা আলাদা | Array | আলাদা আলাদা |
| **Return** | Function-এর return | Function-এর return | নতুন bound function |
| **মনে রাখার কৌশল** | **C**all = **C**omma separated | **A**pply = **A**rray | **B**ind = **B**ound later |

---

## ২.১২ Prototype

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

JavaScript-এ প্রতিটি object-এর একটি hidden internal property আছে — `[[Prototype]]` — যেটি অন্য একটি object-কে point করে। এই linked object-কে **prototype** বলে।

### 🏠 বাস্তব জীবনের উদাহরণ

> বাবা-ছেলের সম্পর্ক। ছেলের নিজের property নেই এমন কিছু খুঁজলে বাবার কাছে যায়, বাবার কাছে না পেলে দাদার কাছে। এটাই Prototype chain।

### 💻 Prototype Examples

```javascript
// ১. প্রতিটি object-এর prototype
const arr = [1, 2, 3];
// arr.__proto__ === Array.prototype
// Array.prototype.__proto__ === Object.prototype
// Object.prototype.__proto__ === null

// এজন্যই arr.map(), arr.filter() কাজ করে
// এগুলো Array.prototype-এ defined

// ২. Object.create() — prototype manually set
const animal = {
  type: "Animal",
  describe() {
    return `${this.name} is a ${this.type}`;
  }
};

const dog = Object.create(animal); // dog-এর prototype = animal
dog.name = "Rex";
dog.type = "Dog";
console.log(dog.describe()); // "Rex is a Dog"
console.log(dog.hasOwnProperty("name")); // true
console.log(dog.hasOwnProperty("describe")); // false (prototype-এ)

// ৩. Constructor Function ও prototype
function Person(name, age) {
  this.name = name;
  this.age = age;
}

// Method prototype-এ রাখা (memory efficient)
Person.prototype.greet = function() {
  return `আমি ${this.name}`;
};

const rahim = new Person("Rahim", 25);
const karim = new Person("Karim", 30);

console.log(rahim.greet()); // "আমি Rahim"
console.log(karim.greet()); // "আমি Karim"
// greet function শুধু একটি, কিন্তু দুজনেই use করছে!

// ৪. Prototype check
console.log(rahim.__proto__ === Person.prototype); // true
console.log(rahim instanceof Person); // true
```

---

## ২.১৩ Prototype Chain

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📊 Prototype Chain Visualization

```
rahim (object)
  └── __proto__ → Person.prototype
        ├── greet: function
        └── __proto__ → Object.prototype
              ├── hasOwnProperty: function
              ├── toString: function
              └── __proto__ → null (chain শেষ)
```

### 💻 Property Lookup

```javascript
function Animal(name) {
  this.name = name;
}
Animal.prototype.type = "Animal";
Animal.prototype.breathe = function() {
  return `${this.name} breathes`;
};

function Dog(name, breed) {
  Animal.call(this, name); // parent constructor call
  this.breed = breed;
}
// Dog.prototype কে Animal.prototype থেকে inherit করা
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog; // fix constructor reference

Dog.prototype.bark = function() {
  return `${this.name} says Woof!`;
};

const rex = new Dog("Rex", "Labrador");
console.log(rex.name);       // "Rex" (own property)
console.log(rex.breed);      // "Labrador" (own property)
console.log(rex.bark());     // "Rex says Woof!" (Dog.prototype)
console.log(rex.breathe());  // "Rex breathes" (Animal.prototype)
console.log(rex.type);       // "Animal" (Animal.prototype)

// Property lookup order:
// rex → Dog.prototype → Animal.prototype → Object.prototype → null
```

### 🎤 Interview-style Explanation

> **প্রশ্ন:** "Prototype Chain কী?"
>
> **আদর্শ উত্তর:** "Prototype Chain হলো linked objects-এর একটি chain। কোনো property বা method খোঁজার সময় JS প্রথমে object-এর নিজের properties দেখে। না পেলে `__proto__` দিয়ে prototype object-এ যায়, সেখানেও না পেলে prototype-এর prototype-এ — এভাবে `null` পর্যন্ত। এই chain traversal-ই Prototype Chain। এর ফলে methods memory-তে একবার define হয়ে সব instances share করতে পারে।"

---

## ২.১৪ Inheritance in JavaScript

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 JavaScript-এ Inheritance-এর উপায়

```javascript
// ১. Prototypal Inheritance (classical way)
function Vehicle(brand) {
  this.brand = brand;
}
Vehicle.prototype.start = function() {
  return `${this.brand} started`;
};

function Car(brand, model) {
  Vehicle.call(this, brand); // parent call
  this.model = model;
}
Car.prototype = Object.create(Vehicle.prototype);
Car.prototype.constructor = Car;
Car.prototype.honk = function() {
  return `${this.brand} ${this.model} goes Beep!`;
};

const myCar = new Car("Toyota", "Corolla");
console.log(myCar.start()); // "Toyota started" (inherited)
console.log(myCar.honk());  // "Toyota Corolla goes Beep!"

// ২. ES6 Class (syntactic sugar, same prototype under hood)
class Vehicle2 {
  constructor(brand) {
    this.brand = brand;
  }
  start() {
    return `${this.brand} started`;
  }
}

class Car2 extends Vehicle2 {
  constructor(brand, model) {
    super(brand); // parent constructor
    this.model = model;
  }
  honk() {
    return `${this.brand} ${this.model} goes Beep!`;
  }
}

const myCar2 = new Car2("Honda", "Civic");
console.log(myCar2.start()); // "Honda started"
console.log(myCar2.honk());  // "Honda Civic goes Beep!"
```

---

## ২.১৫ Classes

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

ES6 Class হলো Prototype-based inheritance-এর **syntactic sugar**। ভেতরে prototype chain-ই ব্যবহার করে, কিন্তু পরিষ্কার OOP syntax দেয়।

### 💻 Class Features

```javascript
class BankAccount {
  // Private field (ES2022)
  #balance;
  #transactionHistory = [];

  // Static property
  static bankName = "BD Bank";
  static totalAccounts = 0;

  constructor(owner, initialBalance = 0) {
    this.owner = owner;
    this.#balance = initialBalance;
    BankAccount.totalAccounts++;
  }

  // Getter
  get balance() {
    return this.#balance;
  }

  // Setter
  set balance(amount) {
    if (amount < 0) throw new Error("Balance cannot be negative");
    this.#balance = amount;
  }

  // Method
  deposit(amount) {
    if (amount <= 0) throw new Error("Invalid amount");
    this.#balance += amount;
    this.#transactionHistory.push({ type: "deposit", amount });
    return this;  // method chaining
  }

  withdraw(amount) {
    if (amount > this.#balance) throw new Error("Insufficient funds");
    this.#balance -= amount;
    this.#transactionHistory.push({ type: "withdrawal", amount });
    return this;
  }

  getHistory() {
    return [...this.#transactionHistory]; // copy return
  }

  // Static method
  static compare(acc1, acc2) {
    return acc1.balance - acc2.balance;
  }

  toString() {
    return `${this.owner}: ৳${this.#balance}`;
  }
}

// Inheritance
class SavingsAccount extends BankAccount {
  #interestRate;

  constructor(owner, initialBalance, interestRate) {
    super(owner, initialBalance); // BankAccount constructor
    this.#interestRate = interestRate;
  }

  addInterest() {
    const interest = this.balance * this.#interestRate;
    this.deposit(interest);
    return this;
  }
}

// ব্যবহার
const acc = new BankAccount("Rahim", 1000);
acc.deposit(500).withdraw(200); // method chaining
console.log(`${acc}`); // "Rahim: ৳1300"

const savings = new SavingsAccount("Karim", 5000, 0.05);
savings.addInterest(); // 5% interest যোগ
console.log(savings.balance); // 5250

console.log(BankAccount.bankName);      // "BD Bank"
console.log(BankAccount.totalAccounts); // 2
```

---

## ২.১৬ Modules

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Modules** হলো code কে আলাদা আলাদা file-এ ভাগ করার পদ্ধতি। ES6 নিয়ে এসেছে native `import`/`export` syntax।

### 💻 ES6 Modules

```javascript
// ========== math.js ==========
// Named exports
export const PI = 3.14159;
export function add(a, b) { return a + b; }
export function multiply(a, b) { return a * b; }

// Default export
export default class Calculator {
  add(a, b) { return a + b; }
}

// ========== app.js ==========
// Named import
import { PI, add, multiply } from "./math.js";
console.log(PI);        // 3.14159
console.log(add(2, 3)); // 5

// Rename
import { add as sum } from "./math.js";
console.log(sum(2, 3)); // 5

// Import all
import * as Math from "./math.js";
console.log(Math.PI);

// Default import (যেকোনো নাম দেওয়া যায়)
import Calc from "./math.js";
const calc = new Calc();

// Dynamic import (lazy loading)
async function loadModule() {
  const module = await import("./heavy-module.js");
  module.doSomething();
}
```

### 📊 CommonJS vs ES Modules

| | CommonJS (Node.js) | ES Modules |
|-|--------------------|-----------|
| **Syntax** | `require()` / `module.exports` | `import` / `export` |
| **Loading** | Synchronous | Asynchronous |
| **Static analysis** | ❌ | ✅ (Tree shaking) |
| **Browser** | ❌ (নেটিভ) | ✅ |
| **Default** | Node.js | Browser + Modern Node.js |

---

## ২.১৭ Debouncing & Throttling

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

দুটিই function call-এর frequency কমানোর technique — performance optimization।

### 🏠 বাস্তব জীবনের উদাহরণ

> **Debouncing** = Elevator button। অনেকে চাপলে শেষ চাপের পর একটু অপেক্ষা করে তারপর যায়।
> **Throttling** = Machine gun — সর্বোচ্চ 1 টি bullet/second, যতই trigger টানুন।

### 💻 Implementation

```javascript
// ১. Debounce — শেষ call-এর পর delay শেষে execute
function debounce(fn, delay) {
  let timeoutId;
  return function(...args) {
    clearTimeout(timeoutId); // আগের timer cancel
    timeoutId = setTimeout(() => {
      fn.apply(this, args);
    }, delay);
  };
}

// Practical: Search bar
const searchInput = document.querySelector("#search");
const search = debounce((query) => {
  console.log("API call:", query);
  // fetchResults(query);
}, 500);

searchInput.addEventListener("input", (e) => search(e.target.value));
// User দ্রুত type করলে API call হবে না, থামলে 500ms পরে একবার হবে

// ২. Throttle — নির্দিষ্ট interval-এ execute
function throttle(fn, limit) {
  let inThrottle = false;
  return function(...args) {
    if (!inThrottle) {
      fn.apply(this, args);
      inThrottle = true;
      setTimeout(() => {
        inThrottle = false;
      }, limit);
    }
  };
}

// Practical: Scroll event
const handleScroll = throttle(() => {
  console.log("Scroll position:", window.scrollY);
}, 100); // সর্বোচ্চ প্রতি 100ms-এ একবার

window.addEventListener("scroll", handleScroll);
```

### 📊 Debounce vs Throttle

| | Debounce | Throttle |
|-|---------|---------|
| **Execute করে** | শেষ call-এর পর delay-এ | প্রতি interval-এ সর্বোচ্চ একবার |
| **Use case** | Search, resize | Scroll, mousemove, button click |
| **Pattern** | "একটু থামো, তারপর করো" | "নিয়মিত বিরতিতে করো" |

---

## ২.১৮ Currying

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Currying** হলো একটি function যেটি multiple arguments নেয় তাকে একটি chain of functions-এ রূপান্তর করা — প্রতিটি function একটি argument নেয়।

### 🏠 বাস্তব জীবনের উদাহরণ

> `add(2, 3)` এর বদলে `add(2)(3)` — প্রথম call-এ 2 "মনে" রাখে, দ্বিতীয় call-এ 3 যোগ করে।

### 💻 Currying Examples

```javascript
// Regular function
function add(a, b, c) {
  return a + b + c;
}

// Curried version
function curriedAdd(a) {
  return function(b) {
    return function(c) {
      return a + b + c;
    };
  };
}
// Arrow function version
const curriedAdd2 = a => b => c => a + b + c;

console.log(curriedAdd(1)(2)(3)); // 6
console.log(curriedAdd2(1)(2)(3)); // 6

// Partial application — একটি argument fix করে নতুন function
const add5 = curriedAdd(5);
console.log(add5(3)(2)); // 10
console.log(add5(10)(1)); // 16

// Practical: Logging
const log = level => message => date =>
  `[${date}] [${level}] ${message}`;

const infoLog = log("INFO");
const errorLog = log("ERROR");

console.log(infoLog("Server started")("2026-05-11"));
// "[2026-05-11] [INFO] Server started"
console.log(errorLog("DB connection failed")("2026-05-11"));
// "[2026-05-11] [ERROR] DB connection failed"

// Generic curry utility
function curry(fn) {
  return function curried(...args) {
    if (args.length >= fn.length) {
      return fn.apply(this, args);
    }
    return function(...args2) {
      return curried.apply(this, args.concat(args2));
    };
  };
}

const curriedMultiply = curry((a, b, c) => a * b * c);
console.log(curriedMultiply(2)(3)(4)); // 24
console.log(curriedMultiply(2, 3)(4)); // 24
console.log(curriedMultiply(2)(3, 4)); // 24
```

---

## ২.১৯ Memoization

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Memoization** হলো একটি optimization technique যেখানে function-এর result cache করা হয়। Same input আবার এলে calculation না করে cache থেকে result দেওয়া হয়।

### 🏠 বাস্তব জীবনের উদাহরণ

> একবার ৯ × ৯ = ৮১ হিসেব করার পর মুখস্থ রাখুন — পরেরবার না ভেবেই বলুন। এটাই memoization।

### 💻 Implementation

```javascript
// Basic memoize
function memoize(fn) {
  const cache = new Map();

  return function(...args) {
    const key = JSON.stringify(args);

    if (cache.has(key)) {
      console.log("⚡ Cache hit!");
      return cache.get(key);
    }

    const result = fn.apply(this, args);
    cache.set(key, result);
    console.log("🔄 Calculated fresh");
    return result;
  };
}

// Heavy computation example
function slowFactorial(n) {
  if (n <= 1) return 1;
  return n * slowFactorial(n - 1);
}

const fastFactorial = memoize(slowFactorial);
console.log(fastFactorial(10)); // 🔄 Calculated: 3628800
console.log(fastFactorial(10)); // ⚡ Cache hit!: 3628800

// Fibonacci with memoization
const memoFib = memoize(function fib(n) {
  if (n <= 1) return n;
  return memoFib(n - 1) + memoFib(n - 2);
});
// O(2^n) → O(n) complexity!

// React useMemo equivalent (conceptual)
function expensiveCalculation(data) {
  return data.filter(x => x > 100).map(x => x * 2);
}
// React-এ: const result = useMemo(() => expensiveCalculation(data), [data]);
```

---

## ২.২০ PART 2 — Interview Questions & Answers

<div align="right"><a href="#part2">⬆ PART 2 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

<details>
<summary><strong>🔹 Execution Context & Event Loop (Q1–Q10)</strong></summary>
<br>

**Q1: Execution Context কী? কত ধরনের?**
> **A:** Execution Context হলো JS code execute হওয়ার পরিবেশ। তিন ধরন: Global EC (একটিমাত্র, program শুরুতে), Function EC (প্রতিটি function call-এ), Eval EC (এড়িয়ে চলুন)। প্রতিটিতে Variable Environment, Lexical Environment, ও this binding থাকে।

**Q2: Creation Phase এবং Execution Phase কী?**
> **A:** Creation Phase-এ: var declarations hoisted (undefined), function declarations fully hoisted, this set হয়। Execution Phase-এ: code line by line execute হয়, variable values assign হয়।

**Q3: Event Loop কী? কীভাবে async code handle করে?**
> **A:** Event Loop JS-এর concurrency model। Call Stack খালি হলে Microtask Queue সম্পূর্ণ drain করে, তারপর Macrotask Queue থেকে একটি task নেয়। এভাবে single-threaded হওয়া সত্ত্বেও non-blocking async behavior।

**Q4: Microtask ও Macrotask-এর পার্থক্য?**
> **A:** Microtask: Promise.then/catch/finally, queueMicrotask, MutationObserver। Macrotask: setTimeout, setInterval, setImmediate, I/O। Microtask সবসময় পরবর্তী Macrotask-এর আগে চলে।

**Q5: নিচের output কী হবে?**
```javascript
console.log("A");
setTimeout(() => console.log("B"), 0);
Promise.resolve().then(() => console.log("C"));
console.log("D");
```
> **A:** A → D → C → B। Sync (A, D) → Microtask (C) → Macrotask (B)।

**Q6: Call Stack overflow কখন হয়?**
> **A:** Recursion-এ base case না থাকলে বা অতিরিক্ত nested function calls। "Maximum call stack size exceeded" error।

**Q7: setTimeout(fn, 0) মানে কি fn সঙ্গে সঙ্গে চলবে?**
> **A:** না। 0ms delay মানে "যত তাড়াতাড়ি সম্ভব" — কিন্তু Call Stack খালি হওয়া এবং Microtask Queue drain হওয়ার পরে। Sync code সবসময় আগে।

**Q8: Promise.all এবং Promise.allSettled-এর পার্থক্য?**
> **A:** `Promise.all` — একটি reject হলে সব reject। সব fulfill হলে সব values array-এ। `Promise.allSettled` — সব complete হওয়ার পর প্রতিটির status/value অথবা reason দেয়। কোনো একটি fail হলেও বাকিগুলোর result পাওয়া যায়।

**Q9: async function কী return করে?**
> **A:** সবসময় একটি Promise। `return 42` করলে `Promise.resolve(42)` হিসেবে return হয়। Exception throw করলে `Promise.reject(error)` হয়।

**Q10: Callback Hell কী? কীভাবে সমাধান করবেন?**
> **A:** Multiple nested callbacks — "Pyramid of Doom"। সমাধান: (১) Named functions দিয়ে flatten করা, (২) Promises এবং chaining, (৩) Async/Await — সবচেয়ে পরিষ্কার।

</details>

<details>
<summary><strong>🔹 this, Prototype & Classes (Q11–Q20)</strong></summary>
<br>

**Q11: this keyword কীভাবে নির্ধারিত হয়?**
> **A:** Call site দিয়ে: Regular function = window/undefined(strict)। Method call = object। Arrow function = enclosing lexical this। Constructor (new) = নতুন object। call/apply/bind = explicitly set।

**Q12: bind, call, apply-এর পার্থক্য?**
> **A:** তিনটিই this set করে। call: `fn.call(obj, arg1, arg2)` তাৎক্ষণিক call, আলাদা args। apply: `fn.apply(obj, [arg1, arg2])` তাৎক্ষণিক, array args। bind: `fn.bind(obj)` নতুন function return করে, পরে call।

**Q13: Arrow function-এ this কী?**
> **A:** Arrow function-এর নিজের this নেই — enclosing lexical scope থেকে inherit করে। Define করার সময় surrounding context-এর this নিয়ে নেয়। তাই object method হিসেবে use করলে object-এর this পাবে না।

**Q14: Prototype কী?**
> **A:** JS-এর প্রতিটি object-এর একটি `[[Prototype]]` hidden property আছে যা অন্য object-কে point করে। Property lookup-এ নিজের কাছে না পেলে prototype-এ যায় — chain বেয়ে null পর্যন্ত।

**Q15: `__proto__` এবং `prototype`-এর পার্থক্য?**
> **A:** `__proto__` হলো প্রতিটি object-এর instance property — তার prototype-কে point করে। `prototype` হলো শুধু function object-এর property — `new` দিয়ে তৈরি instances-এর `__proto__` হয় এই `prototype`।

**Q16: ES6 Class কি নতুন OOP পদ্ধতি?**
> **A:** না — syntactic sugar। Class-এর ভেতরে prototype chain-ই ব্যবহার হয়। `typeof MyClass === "function"`। কিন্তু `class` keyword দিয়ে OOP code পরিষ্কার ও readable।

**Q17: `extends` এবং `super` কীভাবে কাজ করে?**
> **A:** `extends` prototype chain সেট করে Child prototype → Parent prototype। `super()` parent constructor call করে। `super.method()` parent method call করে। `super()` child constructor-এ `this` use করার আগে call করতে হবে।

**Q18: Private class fields (#) কী?**
> **A:** ES2022 — `#fieldName` দিয়ে private field declare করলে class-এর বাইরে থেকে access করা যায় না। `obj.#field` SyntaxError দেবে। নিজে property access restrict করার native JS পদ্ধতি।

**Q19: Static methods কখন ব্যবহার করবেন?**
> **A:** Instance-এর উপর নির্ভরশীল নয় এমন utility methods। `MyClass.method()` দিয়ে call করা যায়, `instance.method()` দিয়ে নয়। যেমন: `Array.isArray()`, `Object.keys()`, `Math.max()`।

**Q20: Currying এবং Partial Application-এর পার্থক্য?**
> **A:** Currying: `f(a, b, c)` → `f(a)(b)(c)` — সব argument একটি একটি করে। Partial Application: কিছু argument আগে fix করে নতুন function — `f(a, b, c)` → `g(b, c)` যেখানে `a` fixed।

</details>

<details>
<summary><strong>🔹 Performance & Patterns (Q21–Q25)</strong></summary>
<br>

**Q21: Debounce এবং Throttle কী? কখন কোনটি ব্যবহার করবেন?**
> **A:** Debounce: শেষ call-এর পর delay — search bar (user টাইপ থামলে API call)। Throttle: নির্দিষ্ট interval-এ একবার — scroll/resize handler। উভয়ই performance optimization।

**Q22: Memoization কী? কখন কার্যকর?**
> **A:** Function result cache করা — same input-এ পুনরায় calculate না করে cache থেকে দেওয়া। Pure function-এ কার্যকর (same input → same output)। Fibonacci, factorial — expensive recursive calculation-এ। React-এ useMemo/useCallback।

**Q23: Module system কেন দরকার?**
> **A:** Code organization, reusability, encapsulation, naming collision এড়ানো। ES Modules: static analysis সম্ভব তাই tree shaking কাজ করে (unused code bundle থেকে বাদ)।

**Q24: Fetch API-এ error handling কীভাবে করবেন?**
> **A:** Fetch শুধু network error-এ reject করে। 4xx/5xx status-এ reject করে না। সঠিক pattern: `if (!response.ok) throw new Error(...)`, তারপর try/catch বা .catch()।

**Q25: Memory Leak কীভাবে হয়? কীভাবে এড়াবেন?**
> **A:** Closure-এ unnecessary reference ধরে রাখলে, Event listener remove না করলে, global variable leak, circular reference। এড়ানো: removeEventListener, WeakMap/WeakRef ব্যবহার, unnecessary references null করা।

</details>

---

<div align="right">
  <a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a>
</div>

---

> **🚀 PART 3 আসছে:** DOM & Browser APIs — DOM Manipulation, Event Handling, Event Bubbling/Capturing, Event Delegation, Local Storage, Cookies এবং আরও অনেক কিছু।
>
> **💬 পরবর্তী PART পেতে:** "PART 3 দাও" লিখুন।


---

<a id="part3"></a>

# PART 3 — DOM & Browser APIs

> **📍 এই PART-এর Sections:** [৩.১ DOM কী?](#৩১-dom-কী) · [৩.২ DOM Manipulation](#৩২-dom-manipulation) · [৩.৩ DOM Traversal](#৩৩-dom-traversal) · [৩.৪ Event Handling](#৩৪-event-handling) · [৩.৫ Event Bubbling](#৩৫-event-bubbling) · [৩.৬ Event Capturing](#৩৬-event-capturing) · [৩.৭ Event Delegation](#৩৭-event-delegation) · [৩.৮ Local Storage](#৩৮-local-storage) · [৩.৯ Session Storage](#৩৯-session-storage) · [৩.১০ Cookies](#৩১০-cookies) · [৩.১১ Browser APIs](#৩১১-browser-apis) · [৩.১২ Form Validation](#৩১২-form-validation) · [৩.১৩ Interview Q&A](#৩১৩-part-3--interview-questions--answers)

---

## ৩.১ DOM কী?

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**DOM (Document Object Model)** হলো HTML document-এর একটি tree-shaped representation যা browser তৈরি করে। JavaScript এই tree-এর মাধ্যমে HTML elements পড়তে, পরিবর্তন করতে, যোগ করতে ও মুছতে পারে।

### 🏠 বাস্তব জীবনের উদাহরণ

> একটি পারিবারিক বংশতালিকার মতো। বাবা-মা → সন্তান → নাতিপুতি। HTML-এ `<html>` হলো root, `<body>` তার সন্তান, `<div>`, `<p>` তার নাতি। DOM এই সম্পর্ক map করে এবং JavaScript সেই map ব্যবহার করে যেকোনো element-এ পৌঁছাতে পারে।

### 📊 DOM Tree Visualization

```
Document
└── <html>
    ├── <head>
    │   ├── <title> "My Page" </title>
    │   └── <meta charset="UTF-8">
    └── <body>
        ├── <h1 id="title"> Hello </h1>
        ├── <nav class="menu">
        │   ├── <a href="/"> Home </a>
        │   └── <a href="/about"> About </a>
        └── <div class="container">
            ├── <p> Paragraph 1 </p>
            └── <ul>
                ├── <li> Item 1 </li>
                └── <li> Item 2 </li>
```

### 📊 DOM Node Types

| Node Type | উদাহরণ |
|-----------|---------|
| **Element Node** | `<div>`, `<p>`, `<span>` |
| **Text Node** | `"Hello World"` (element-এর ভেতরের text) |
| **Attribute Node** | `id="title"`, `class="menu"` |
| **Comment Node** | `<!-- comment -->` |
| **Document Node** | `document` object নিজে |

---

## ৩.২ DOM Manipulation

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Element Select করা

```javascript
// ১. getElementById — সবচেয়ে দ্রুত (single element)
const title = document.getElementById("title");

// ২. getElementsByClassName — HTMLCollection (live)
const items = document.getElementsByClassName("item");
// items[0], items[1] — index দিয়ে access

// ৩. getElementsByTagName — HTMLCollection
const paragraphs = document.getElementsByTagName("p");

// ৪. querySelector — CSS selector, প্রথম match
const btn = document.querySelector("#submit-btn");
const firstItem = document.querySelector(".item");
const input = document.querySelector("input[type='email']");

// ৫. querySelectorAll — NodeList (সব match)
const allItems = document.querySelectorAll(".item");
allItems.forEach(item => console.log(item.textContent));

// ৬. Modern selectors
const nav = document.querySelector("nav > a:first-child");
const checked = document.querySelectorAll("input:checked");
```

### 💻 Content পরিবর্তন করা

```javascript
const el = document.querySelector("#message");

// ১. textContent — plain text (XSS safe ✅)
el.textContent = "নতুন বার্তা";
console.log(el.textContent); // "নতুন বার্তা"

// ২. innerHTML — HTML parse করে (XSS risk ⚠️)
el.innerHTML = "<strong>Bold</strong> text";
el.innerHTML = "<img src=x onerror=alert(1)>"; // ❌ XSS!

// ✅ User input হলে textContent ব্যবহার করুন
el.textContent = userInput; // XSS safe

// ৩. innerText — visible text শুধু (CSS-aware)
el.innerText = "দৃশ্যমান text";

// ৪. value — input elements
const input = document.querySelector("#name");
input.value = "Rahim";
console.log(input.value); // "Rahim"
```

### 💻 Attributes পরিবর্তন করা

```javascript
const img = document.querySelector("img");
const link = document.querySelector("a");

// getAttribute / setAttribute / removeAttribute
console.log(img.getAttribute("src"));      // "photo.jpg"
img.setAttribute("src", "new-photo.jpg");
img.setAttribute("alt", "New Photo");
img.removeAttribute("title");

// Direct property access (বেশি ব্যবহৃত)
img.src = "new-photo.jpg";
img.alt = "New Photo";
link.href = "https://example.com";
link.target = "_blank";

// dataset — data-* attributes
// HTML: <div data-user-id="123" data-role="admin">
const div = document.querySelector("[data-user-id]");
console.log(div.dataset.userId);  // "123"
console.log(div.dataset.role);    // "admin"
div.dataset.status = "active";    // data-status="active" যোগ হয়
```

### 💻 CSS Styles পরিবর্তন করা

```javascript
const box = document.querySelector(".box");

// ১. Inline style
box.style.backgroundColor = "blue";
box.style.fontSize = "18px";
box.style.display = "none";     // hide
box.style.display = "";         // inline style সরিয়ে default

// ২. CSS Classes (বেশি ভালো পদ্ধতি)
box.classList.add("active");
box.classList.remove("hidden");
box.classList.toggle("dark-mode");    // থাকলে সরায়, না থাকলে যোগ করে
box.classList.contains("active");     // true/false
box.classList.replace("old", "new");

// ৩. getComputedStyle — computed styles পড়া
const styles = window.getComputedStyle(box);
console.log(styles.fontSize);    // "18px"
console.log(styles.color);       // "rgb(0, 0, 0)"
```

### 💻 Element তৈরি ও যোগ করা

```javascript
// ১. createElement
const newDiv = document.createElement("div");
newDiv.className = "card";
newDiv.textContent = "নতুন Card";

// ২. append / prepend / before / after (modern)
const container = document.querySelector(".container");
container.append(newDiv);           // শেষে যোগ
container.prepend(newDiv);          // শুরুতে যোগ

const existingEl = document.querySelector(".existing");
existingEl.before(newDiv);          // existingEl-এর আগে
existingEl.after(newDiv);           // existingEl-এর পরে

// ৩. appendChild / insertBefore (পুরনো)
container.appendChild(newDiv);
container.insertBefore(newDiv, existingEl);

// ৪. innerHTML দিয়ে (সহজ কিন্তু XSS risk)
container.innerHTML += "<div class='card'>নতুন</div>";

// ৫. insertAdjacentHTML (নিরাপদ + দ্রুত)
container.insertAdjacentHTML("beforeend", "<div>শেষে</div>");
container.insertAdjacentHTML("afterbegin", "<div>শুরুতে</div>");
// positions: beforebegin, afterbegin, beforeend, afterend

// ৬. Element remove করা
const toRemove = document.querySelector(".old-item");
toRemove.remove();                  // modern
toRemove.parentNode.removeChild(toRemove); // পুরনো

// ৭. DocumentFragment — performance optimization
const fragment = document.createDocumentFragment();
for (let i = 0; i < 100; i++) {
  const li = document.createElement("li");
  li.textContent = `Item ${i}`;
  fragment.appendChild(li);
}
document.querySelector("ul").appendChild(fragment); // একবারেই DOM update
```

### ⚠️ Common Mistakes

```javascript
// ❌ innerHTML দিয়ে user input
el.innerHTML = userInput; // XSS vulnerability!
// ✅ textContent
el.textContent = userInput;

// ❌ Loop-এ বারবার DOM update (reflow)
for (let i = 0; i < 1000; i++) {
  list.innerHTML += "<li>" + i + "</li>"; // প্রতিবার reflow!
}
// ✅ DocumentFragment বা একবারে innerHTML
```

---

## ৩.৩ DOM Traversal

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Navigation Properties

```javascript
const parent = document.querySelector(".parent");

// Parent navigation
parent.parentNode;           // যেকোনো node (text node সহ)
parent.parentElement;        // শুধু element parent

// Children navigation
parent.childNodes;           // সব child nodes (text nodes সহ)
parent.children;             // শুধু element children (HTMLCollection)
parent.firstChild;           // প্রথম child node (text হতে পারে)
parent.firstElementChild;    // প্রথম element child
parent.lastChild;
parent.lastElementChild;
parent.childElementCount;    // কতটি element child

// Sibling navigation
const child = parent.firstElementChild;
child.nextSibling;           // পরের node
child.nextElementSibling;    // পরের element
child.previousSibling;
child.previousElementSibling;

// closest — ancestor খোঁজা
const btn = document.querySelector(".btn");
const form = btn.closest("form");    // btn-এর সবচেয়ে কাছের form ancestor
const modal = btn.closest(".modal"); // closest CSS selector match

// matches — CSS selector check
btn.matches(".primary-btn");   // true/false
btn.matches("[disabled]");

// Practical example
document.querySelector("ul").querySelectorAll("li").forEach((li, i) => {
  li.textContent = `Item ${i + 1}`;
  li.dataset.index = i;
});
```

---

## ৩.৪ Event Handling

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Event** হলো browser-এ ঘটে যাওয়া যেকোনো ঘটনা — click, keypress, scroll, form submit। JavaScript এই events-এ **listen** করে এবং **react** করে।

### 💻 Event Listener যোগ করার পদ্ধতি

```javascript
const btn = document.querySelector("#myBtn");

// ১. addEventListener (সবচেয়ে ভালো পদ্ধতি ✅)
btn.addEventListener("click", function(event) {
  console.log("Clicked!", event);
});

// Arrow function
btn.addEventListener("click", (e) => {
  console.log("Target:", e.target);
});

// Named function (remove করা সম্ভব)
function handleClick(e) {
  console.log("Click handled");
}
btn.addEventListener("click", handleClick);
btn.removeEventListener("click", handleClick); // সরানো যায়

// ২. Inline HTML (এড়িয়ে চলুন ❌)
// <button onclick="handleClick()">Click</button>

// ৩. on-property (সীমাবদ্ধ)
btn.onclick = function() { console.log("clicked"); };
// শুধু একটি handler — পরের টি আগেরটি override করে
```

### 💻 Event Object (e / event)

```javascript
document.querySelector("form").addEventListener("submit", (e) => {
  e.preventDefault();   // form submit হবে না (page reload রোধ)

  console.log(e.type);         // "submit"
  console.log(e.target);       // form element
  console.log(e.currentTarget); // listener যেখানে attached

  // Mouse events
  console.log(e.clientX, e.clientY);   // viewport position
  console.log(e.pageX, e.pageY);       // page position
  console.log(e.button);               // 0=left, 1=middle, 2=right

  // Keyboard events
  console.log(e.key);         // "Enter", "a", "ArrowUp"
  console.log(e.code);        // "KeyA", "Space"
  console.log(e.ctrlKey);     // Ctrl চাপা আছে? true/false
  console.log(e.shiftKey);
  console.log(e.altKey);

  e.stopPropagation();  // bubbling বন্ধ
});

// Common Events
const events = [
  // Mouse: click, dblclick, mousedown, mouseup, mouseover, mouseout, mousemove
  // Keyboard: keydown, keyup, keypress (deprecated)
  // Form: submit, change, input, focus, blur, reset
  // Window: load, DOMContentLoaded, resize, scroll
  // Touch: touchstart, touchend, touchmove
];
```

### 💻 Practical Event Examples

```javascript
// ১. Input live validation
const emailInput = document.querySelector("#email");
emailInput.addEventListener("input", (e) => {
  const valid = e.target.value.includes("@");
  e.target.classList.toggle("valid", valid);
  e.target.classList.toggle("invalid", !valid);
});

// ২. Keyboard shortcuts
document.addEventListener("keydown", (e) => {
  if (e.ctrlKey && e.key === "s") {
    e.preventDefault();
    saveDocument();
  }
  if (e.key === "Escape") closeModal();
});

// ৩. Once option — একবার শুনবে
btn.addEventListener("click", handleClick, { once: true });

// ৪. Passive option — scroll performance
window.addEventListener("scroll", onScroll, { passive: true });
```

---

## ৩.৫ Event Bubbling

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Event Bubbling** হলো যখন কোনো element-এ event ঘটে, সেই event সেই element থেকে শুরু হয়ে parent → grandparent → document পর্যন্ত উপরে "bubble" করে।

### 🏠 বাস্তব জীবনের উদাহরণ

> পানিতে ঢিল ফেললে বুদবুদ নিচ থেকে উপরে ওঠে। Event ঘটে innermost element-এ, তারপর উপরে উঠতে থাকে।

### 💻 Bubbling Example

```html
<div id="outer">    <!-- ③ তৃতীয়ে fire হয় -->
  <div id="middle"> <!-- ② দ্বিতীয়ে fire হয় -->
    <button id="inner">Click me</button> <!-- ① প্রথমে fire হয় -->
  </div>
</div>
```

```javascript
document.getElementById("inner").addEventListener("click", () => {
  console.log("Inner clicked");   // ① প্রথমে
});

document.getElementById("middle").addEventListener("click", () => {
  console.log("Middle clicked");  // ② দ্বিতীয়ে (bubble)
});

document.getElementById("outer").addEventListener("click", () => {
  console.log("Outer clicked");   // ③ তৃতীয়ে (bubble)
});

// inner button click করলে:
// Inner clicked
// Middle clicked
// Outer clicked
```

### 💻 Bubbling বন্ধ করা

```javascript
document.getElementById("inner").addEventListener("click", (e) => {
  e.stopPropagation(); // bubble বন্ধ — parent-এ পৌঁছাবে না
  console.log("Inner only");
});

// stopImmediatePropagation — same element-এর অন্য handlers-ও বন্ধ
btn.addEventListener("click", (e) => {
  e.stopImmediatePropagation();
  console.log("Only this handler");
});
btn.addEventListener("click", () => {
  console.log("This won't run");  // blocked
});
```

---

## ৩.৬ Event Capturing

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Event Capturing** (বা Trickling) হলো bubbling-এর বিপরীত — event document থেকে নিচের দিকে target element পর্যন্ত ভ্রমণ করে। Default-এ disabled — তৃতীয় argument `true` দিলে সক্রিয় হয়।

### 💻 Event Flow — তিনটি Phase

```
Event Flow (click on #inner):

CAPTURING Phase (↓):          BUBBLING Phase (↑):
document                       #inner
  ↓                              ↑
html                           #middle
  ↓                              ↑
body                           #outer
  ↓                              ↑
#outer                         body
  ↓                              ↑
#middle                        html
  ↓                              ↑
#inner (TARGET Phase)          document
```

```javascript
// Bubbling (default, 3rd arg false বা omit)
outer.addEventListener("click", () => console.log("Outer bubble"), false);

// Capturing (3rd arg = true)
outer.addEventListener("click", () => console.log("Outer capture"), true);
middle.addEventListener("click", () => console.log("Middle capture"), true);

// inner click করলে:
// Outer capture   ← capturing phase (বাইরে থেকে)
// Middle capture  ← capturing phase
// Inner...        ← target phase
// Middle bubble   ← bubbling phase (ভেতর থেকে)
// Outer bubble    ← bubbling phase
```

### 📊 Bubbling vs Capturing

| | Bubbling | Capturing |
|--|---------|-----------|
| **Direction** | ভেতর → বাইরে ↑ | বাইরে → ভেতর ↓ |
| **Default** | ✅ (3rd arg false) | ❌ (3rd arg true) |
| **ব্যবহার** | সাধারণ event handling | বিশেষ intercept দরকারে |

---

## ৩.৭ Event Delegation

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Event Delegation** হলো child elements-এ আলাদা আলাদা listener না দিয়ে **parent element-এ একটি listener** দেওয়া এবং bubbling ব্যবহার করে কোন child-এ click হয়েছে বের করা।

### 🏠 বাস্তব জীবনের উদাহরণ

> অফিসে ১০০ জন কর্মীর কাছে আলাদা আলাদা ফোন না দিয়ে একটি receptionist রাখা হলো। যে call আসে, receptionist বুঝে সঠিক ব্যক্তির কাছে পাঠায়। Event Delegation এই receptionist।

### 💻 Event Delegation Examples

```javascript
// ❌ Non-delegated — প্রতিটি item-এ listener (inefficient)
document.querySelectorAll(".todo-item").forEach(item => {
  item.addEventListener("click", handleItemClick);
  // নতুন item যোগ হলে তাতে listener নেই!
});

// ✅ Delegated — parent-এ একটি listener
const todoList = document.querySelector("#todo-list");
todoList.addEventListener("click", (e) => {
  // কোন child-এ click হয়েছে?
  const item = e.target.closest(".todo-item");
  if (!item) return; // list-এ click কিন্তু item-এ নয়

  if (e.target.matches(".delete-btn")) {
    item.remove();
  } else if (e.target.matches(".complete-btn")) {
    item.classList.toggle("completed");
  } else {
    item.classList.toggle("selected");
  }
});

// dynamically যোগ করা items-এ এও কাজ করবে!
function addItem(text) {
  const li = document.createElement("li");
  li.className = "todo-item";
  li.innerHTML = `
    <span>${text}</span>
    <button class="complete-btn">✓</button>
    <button class="delete-btn">✗</button>
  `;
  todoList.appendChild(li);
  // নতুন listener দিতে হয়নি!
}
```

### 📊 Event Delegation এর সুবিধা

| সুবিধা | ব্যাখ্যা |
|--------|---------|
| **Memory efficient** | ১০০টির বদলে একটি listener |
| **Dynamic elements** | নতুন যোগ হওয়া elements-এও কাজ করে |
| **Code simple** | Listener management সহজ |
| **Performance** | Attach/detach overhead কম |

---

## ৩.৮ Local Storage

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Local Storage** হলো browser-এ data store করার একটি mechanism যা **permanent** — browser বন্ধ করলেও, computer restart করলেও data থাকে। Origin-specific (same domain, same protocol, same port)।

### 💻 Local Storage API

```javascript
// ১. Data সংরক্ষণ
localStorage.setItem("username", "Rahim");
localStorage.setItem("theme", "dark");

// Object/Array সংরক্ষণ (stringify করতে হবে)
const user = { name: "Rahim", age: 25, role: "admin" };
localStorage.setItem("user", JSON.stringify(user));

const tasks = ["Task 1", "Task 2", "Task 3"];
localStorage.setItem("tasks", JSON.stringify(tasks));

// ২. Data পড়া
const username = localStorage.getItem("username"); // "Rahim"
const theme = localStorage.getItem("theme");       // "dark"
const missing = localStorage.getItem("notExist");  // null

// Object পড়া (parse করতে হবে)
const storedUser = JSON.parse(localStorage.getItem("user"));
console.log(storedUser.name); // "Rahim"

const storedTasks = JSON.parse(localStorage.getItem("tasks") || "[]");
// || "[]" — null হলে empty array default

// ৩. Data মুছে ফেলা
localStorage.removeItem("theme");
localStorage.clear(); // সব মুছে ফেলা

// ৪. Keys iterate করা
for (let i = 0; i < localStorage.length; i++) {
  const key = localStorage.key(i);
  console.log(key, localStorage.getItem(key));
}

// ৫. Storage event (অন্য tab-এ change detect করা)
window.addEventListener("storage", (e) => {
  console.log("Key changed:", e.key);
  console.log("Old value:", e.oldValue);
  console.log("New value:", e.newValue);
});
```

### 💻 Practical: Dark Mode সংরক্ষণ

```javascript
// সংরক্ষণ
function toggleDarkMode() {
  const isDark = document.body.classList.toggle("dark-mode");
  localStorage.setItem("darkMode", isDark ? "true" : "false");
}

// Page load-এ apply
const savedTheme = localStorage.getItem("darkMode");
if (savedTheme === "true") {
  document.body.classList.add("dark-mode");
}
```

---

## ৩.৯ Session Storage

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Session Storage** Local Storage-এর মতোই, কিন্তু **tab/browser বন্ধ করলে data মুছে যায়**। প্রতিটি tab-এর আলাদা session storage।

### 💻 Session Storage API

```javascript
// API একই — localStorage → sessionStorage
sessionStorage.setItem("formData", JSON.stringify({ step: 2, data: {} }));
const formData = JSON.parse(sessionStorage.getItem("formData"));
sessionStorage.removeItem("formData");
sessionStorage.clear();

// Practical: Multi-step form progress
function saveProgress(step, data) {
  sessionStorage.setItem("formStep", step);
  sessionStorage.setItem("formData", JSON.stringify(data));
}

function loadProgress() {
  return {
    step: parseInt(sessionStorage.getItem("formStep") || "1"),
    data: JSON.parse(sessionStorage.getItem("formData") || "{}")
  };
}
```

### 📊 localStorage vs sessionStorage vs Cookie

| | localStorage | sessionStorage | Cookie |
|--|-------------|---------------|--------|
| **Lifetime** | Permanent | Tab বন্ধ পর্যন্ত | Expiry date পর্যন্ত |
| **Storage** | ~5-10 MB | ~5 MB | ~4 KB |
| **Server access** | ❌ | ❌ | ✅ (HTTP header) |
| **Tab sharing** | ✅ | ❌ (per tab) | ✅ |
| **API** | key-value | key-value | string |
| **Use case** | Theme, preferences | Form progress | Auth token, session |

---

## ৩.১০ Cookies

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Cookie** হলো server বা client থেকে set করা ছোট data যা প্রতিটি HTTP request-এ server-এ পাঠানো হয়। Authentication, session tracking-এ ব্যবহৃত।

### 💻 Cookie Manipulation

```javascript
// Cookie set (basic)
document.cookie = "username=Rahim";

// Options সহ
document.cookie = "token=abc123; expires=Thu, 31 Dec 2026 23:59:59 GMT; path=/; Secure; SameSite=Strict";

// Max-Age (seconds) দিয়ে
document.cookie = "session=xyz; max-age=3600; path=/"; // 1 ঘন্টা

// Cookie read — সব cookies একসাথে আসে
console.log(document.cookie); // "username=Rahim; token=abc123"

// নির্দিষ্ট cookie read করার utility
function getCookie(name) {
  const cookies = document.cookie.split("; ");
  const found = cookies.find(c => c.startsWith(name + "="));
  return found ? found.split("=")[1] : null;
}
console.log(getCookie("username")); // "Rahim"

// Cookie delete — expires অতীতে সেট
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/";

// Cookie utility class
class CookieManager {
  static set(name, value, days = 7, options = {}) {
    const expires = new Date(Date.now() + days * 864e5).toUTCString();
    const secure = options.secure ? "; Secure" : "";
    const sameSite = `; SameSite=${options.sameSite || "Lax"}`;
    document.cookie = `${name}=${encodeURIComponent(value)}; expires=${expires}; path=${options.path || "/"}${secure}${sameSite}`;
  }

  static get(name) {
    const match = document.cookie.match(new RegExp(`(^| )${name}=([^;]+)`));
    return match ? decodeURIComponent(match[2]) : null;
  }

  static delete(name) {
    document.cookie = `${name}=; expires=Thu, 01 Jan 1970 00:00:00 GMT; path=/`;
  }
}

CookieManager.set("theme", "dark", 30);
console.log(CookieManager.get("theme")); // "dark"
```

### ⚠️ Cookie Security Flags

| Flag | ব্যাখ্যা |
|------|---------|
| **Secure** | শুধু HTTPS-এ পাঠানো হবে |
| **HttpOnly** | JavaScript access করতে পারবে না (XSS protection, server set করে) |
| **SameSite=Strict** | Cross-site request-এ পাঠানো হবে না (CSRF protection) |
| **SameSite=Lax** | Top-level navigation-এ পাঠানো হবে |
| **SameSite=None** | Cross-site-এ পাঠানো হবে (Secure লাগবে) |

---

## ৩.১১ Browser APIs

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Geolocation API

```javascript
// ব্যবহারকারীর অবস্থান জানা
if ("geolocation" in navigator) {
  navigator.geolocation.getCurrentPosition(
    (position) => {
      const { latitude, longitude, accuracy } = position.coords;
      console.log(`Lat: ${latitude}, Lng: ${longitude}`);
    },
    (error) => {
      console.error("Error:", error.message);
    },
    { enableHighAccuracy: true, timeout: 5000 }
  );

  // Continuous tracking
  const watchId = navigator.geolocation.watchPosition(
    (pos) => updateMap(pos.coords)
  );
  // বন্ধ করতে:
  navigator.geolocation.clearWatch(watchId);
}
```

### 💻 Intersection Observer API

```javascript
// Element viewport-এ এলে lazy load করা
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      // element দেখা যাচ্ছে
      const img = entry.target;
      img.src = img.dataset.src;      // lazy load
      img.classList.add("visible");
      observer.unobserve(img);        // একবারেই যথেষ্ট
    }
  });
}, {
  threshold: 0.1,        // 10% দেখা গেলে trigger
  rootMargin: "0px 0px -100px 0px"  // 100px আগে trigger
});

document.querySelectorAll("img[data-src]").forEach(img => {
  observer.observe(img);
});
```

### 💻 History API

```javascript
// SPA routing
window.history.pushState({ page: "about" }, "About", "/about");
window.history.replaceState({ page: "home" }, "Home", "/");
window.history.back();
window.history.forward();
window.history.go(-2);

// Back/forward button handle
window.addEventListener("popstate", (e) => {
  console.log("State:", e.state);
  renderPage(e.state?.page || "home");
});
```

### 💻 Clipboard API

```javascript
// Copy to clipboard
async function copyText(text) {
  try {
    await navigator.clipboard.writeText(text);
    console.log("Copied!");
  } catch (err) {
    console.error("Copy failed:", err);
  }
}

// Paste from clipboard
async function pasteText() {
  const text = await navigator.clipboard.readText();
  console.log("Pasted:", text);
}
```

### 💻 Notification API

```javascript
async function showNotification(title, body) {
  const permission = await Notification.requestPermission();

  if (permission === "granted") {
    const notification = new Notification(title, {
      body,
      icon: "/icon.png",
      badge: "/badge.png"
    });

    notification.onclick = () => {
      window.focus();
      notification.close();
    };
  }
}
```

### 💻 Web Storage Events ও Other Useful APIs

```javascript
// ১. ResizeObserver — element resize track
const resizeObserver = new ResizeObserver(entries => {
  entries.forEach(entry => {
    const { width, height } = entry.contentRect;
    console.log(`Size: ${width}x${height}`);
  });
});
resizeObserver.observe(document.querySelector(".responsive-box"));

// ২. MutationObserver — DOM change track
const mutationObserver = new MutationObserver(mutations => {
  mutations.forEach(mutation => {
    console.log("DOM changed:", mutation.type);
    mutation.addedNodes.forEach(node => console.log("Added:", node));
  });
});
mutationObserver.observe(document.querySelector("#dynamic-content"), {
  childList: true,
  subtree: true,
  attributes: true
});

// ৩. Page Visibility API
document.addEventListener("visibilitychange", () => {
  if (document.hidden) {
    pauseVideo(); // tab hidden হলে pause
  } else {
    resumeVideo();
  }
});

// ৪. Online/Offline detection
window.addEventListener("online", () => console.log("Back online!"));
window.addEventListener("offline", () => console.log("Offline!"));
console.log(navigator.onLine); // true/false
```

---

## ৩.১২ Form Validation

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 HTML5 Built-in Validation

```html
<form id="registration-form" novalidate>
  <input type="text" id="name" required minlength="2" maxlength="50"
         placeholder="পুরো নাম">
  <input type="email" id="email" required placeholder="ইমেইল">
  <input type="tel" id="phone" pattern="[0-9]{11}" placeholder="01XXXXXXXXX">
  <input type="password" id="password" required minlength="8">
  <input type="number" id="age" min="18" max="100">
  <button type="submit">নিবন্ধন করুন</button>
</form>
```

### 💻 Custom JavaScript Validation

```javascript
class FormValidator {
  constructor(formId) {
    this.form = document.getElementById(formId);
    this.errors = {};
    this.setupValidation();
  }

  // Validation rules
  validators = {
    name: (value) => {
      if (!value.trim()) return "নাম আবশ্যক";
      if (value.trim().length < 2) return "নাম কমপক্ষে ২ অক্ষর হতে হবে";
      return null; // null = valid
    },

    email: (value) => {
      if (!value) return "ইমেইল আবশ্যক";
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!emailRegex.test(value)) return "সঠিক ইমেইল দিন";
      return null;
    },

    phone: (value) => {
      if (!value) return "ফোন নম্বর আবশ্যক";
      const phoneRegex = /^01[3-9]\d{8}$/; // BD mobile
      if (!phoneRegex.test(value)) return "সঠিক বাংলাদেশি নম্বর দিন (01XXXXXXXXX)";
      return null;
    },

    password: (value) => {
      if (!value) return "পাসওয়ার্ড আবশ্যক";
      if (value.length < 8) return "পাসওয়ার্ড কমপক্ষে ৮ অক্ষর";
      if (!/[A-Z]/.test(value)) return "একটি বড় হাতের অক্ষর লাগবে";
      if (!/[0-9]/.test(value)) return "একটি সংখ্যা লাগবে";
      return null;
    }
  };

  validateField(fieldName, value) {
    const validator = this.validators[fieldName];
    if (!validator) return null;

    const error = validator(value);
    this.showError(fieldName, error);
    return error;
  }

  showError(fieldName, error) {
    const field = this.form.querySelector(`#${fieldName}`);
    const errorEl = this.form.querySelector(`#${fieldName}-error`);

    if (error) {
      field?.classList.add("invalid");
      field?.classList.remove("valid");
      if (errorEl) errorEl.textContent = error;
    } else {
      field?.classList.remove("invalid");
      field?.classList.add("valid");
      if (errorEl) errorEl.textContent = "";
    }
  }

  setupValidation() {
    // Real-time validation on input
    ["name", "email", "phone", "password"].forEach(fieldName => {
      const field = this.form.querySelector(`#${fieldName}`);
      field?.addEventListener("blur", (e) => {
        this.validateField(fieldName, e.target.value);
      });
      field?.addEventListener("input", (e) => {
        if (this.errors[fieldName]) { // error থাকলেই live validate
          this.validateField(fieldName, e.target.value);
        }
      });
    });

    // Form submit
    this.form.addEventListener("submit", (e) => {
      e.preventDefault();

      let hasError = false;
      ["name", "email", "phone", "password"].forEach(fieldName => {
        const value = this.form.querySelector(`#${fieldName}`)?.value || "";
        const error = this.validateField(fieldName, value);
        if (error) {
          this.errors[fieldName] = error;
          hasError = true;
        }
      });

      if (!hasError) {
        this.onSuccess();
      }
    });
  }

  onSuccess() {
    const formData = new FormData(this.form);
    const data = Object.fromEntries(formData.entries());
    console.log("Form submitted:", data);
    // API call করুন
  }
}

const validator = new FormValidator("registration-form");
```

### 💻 Constraint Validation API

```javascript
const input = document.querySelector("#email");

// Built-in validation state
console.log(input.validity.valid);       // সব ঠিক আছে?
console.log(input.validity.valueMissing); // required কিন্তু খালি?
console.log(input.validity.typeMismatch); // email format ভুল?
console.log(input.validity.tooShort);    // minlength পূরণ হয়নি?
console.log(input.validity.patternMismatch); // pattern match করেনি?
console.log(input.validationMessage);    // browser-এর error message

// Custom error set
input.setCustomValidity("এই ইমেইল ইতিমধ্যে নিবন্ধিত");
input.setCustomValidity(""); // error clear
```

---

## ৩.১৩ PART 3 — Interview Questions & Answers

<div align="right"><a href="#part3">⬆ PART 3 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

<details>
<summary><strong>🔹 DOM & Events (Q1–Q15)</strong></summary>
<br>

**Q1: DOM কী? JavaScript কীভাবে DOM ব্যবহার করে?**
> **A:** DOM (Document Object Model) হলো HTML document-এর tree-shaped object representation যা browser তৈরি করে। JavaScript `document` object-এর মাধ্যমে DOM access করে — elements পড়তে, পরিবর্তন করতে, যোগ করতে ও মুছতে পারে। DOM manipulation-ই web interactivity-র মূল ভিত্তি।

**Q2: querySelector এবং getElementById-এর পার্থক্য?**
> **A:** `getElementById` শুধু ID দিয়ে search করে, দ্রুততম। `querySelector` যেকোনো CSS selector ব্যবহার করতে পারে — class, attribute, pseudo-class সহ। `querySelectorAll` সব matches দেয়। Modern code-এ `querySelector`/`querySelectorAll` prefer করা হয়।

**Q3: innerHTML এবং textContent-এর পার্থক্য? কোনটি নিরাপদ?**
> **A:** `innerHTML` HTML parse করে — HTML tags কাজ করে কিন্তু user input দিলে XSS vulnerability। `textContent` plain text — HTML tags escape হয়, XSS safe। User input display করতে সবসময় `textContent` ব্যবহার করুন।

**Q4: Event Bubbling কী? কীভাবে বন্ধ করবেন?**
> **A:** Event ঘটে innermost element-এ, তারপর parent → grandparent → document পর্যন্ত উপরে "bubble" করে। বন্ধ করতে: `e.stopPropagation()` — bubble বন্ধ হয়। `e.stopImmediatePropagation()` — same element-এর অন্য handlers-ও বন্ধ।

**Q5: Event Capturing কী? Bubbling থেকে কীভাবে আলাদা?**
> **A:** Capturing-এ event document থেকে নিচে target-এ আসে। Bubbling-এ target থেকে উপরে যায়। Capturing activate: `addEventListener("click", fn, true)`। Event flow: Capturing (↓) → Target → Bubbling (↑)। Default হলো bubbling।

**Q6: Event Delegation কী? কেন ব্যবহার করবেন?**
> **A:** Child elements-এর বদলে parent-এ একটি listener — bubbling ব্যবহার করে কোন child-এ event হয়েছে `e.target` দিয়ে বের করা। সুবিধা: (১) Memory efficient, (২) Dynamic elements-এও কাজ করে, (৩) Code simple।

**Q7: preventDefault() কী করে?**
> **A:** Browser-এর default behavior বন্ধ করে। যেমন: form submit-এ page reload বন্ধ, `<a>` click-এ navigation বন্ধ, right-click-এ context menu বন্ধ। `stopPropagation()` থেকে আলাদা — এটি শুধু default বন্ধ করে, bubbling নয়।

**Q8: Event-এ `target` এবং `currentTarget`-এর পার্থক্য?**
> **A:** `e.target` — actual element যেখানে event ঘটেছে (innermost)। `e.currentTarget` — যে element-এ listener attached আছে। Delegation-এ: `e.target` = clicked child, `e.currentTarget` = parent যেখানে listener আছে।

**Q9: DOMContentLoaded এবং load event-এর পার্থক্য?**
> **A:** `DOMContentLoaded` — HTML parse হয়ে DOM ready হলে fire হয় (CSS, images-এর জন্য wait করে না)। `load` — সব resources (CSS, images, scripts) load সম্পন্ন হলে fire হয়। Script-এর জন্য সাধারণত `DOMContentLoaded` prefer করা হয়।

**Q10: DocumentFragment কী? কেন ব্যবহার করবেন?**
> **A:** DocumentFragment হলো একটি virtual DOM node — এতে elements যোগ করলে actual DOM-এ reflow হয় না। সব elements যোগ করে একবারে DOM-এ insert করলে performance অনেক ভালো। ১০০০ items insert-এ প্রতিটিতে reflow না হয়ে একটি reflow।

**Q11: Local Storage এবং Session Storage-এর পার্থক্য?**
> **A:** `localStorage` — permanent, browser বন্ধেও থাকে, সব tab share করে। `sessionStorage` — tab বন্ধ হলে মুছে যায়, প্রতিটি tab আলাদা। উভয়ে ~5MB, শুধু string store করে (object-এ JSON.stringify/parse দরকার), server-এ যায় না।

**Q12: Cookie-এর HttpOnly এবং Secure flag কী?**
> **A:** `HttpOnly` — JavaScript দিয়ে cookie read করা যাবে না (XSS attack থেকে রক্ষা — server set করে)। `Secure` — শুধু HTTPS connection-এ পাঠানো হবে। `SameSite=Strict` — CSRF attack থেকে রক্ষা।

**Q13: Intersection Observer কী? কীভাবে ব্যবহার করবেন?**
> **A:** Element কখন viewport-এ enter/exit করে তা detect করে, scroll event ছাড়াই। Lazy loading, infinite scroll, animation trigger-এ ব্যবহার। `scroll` event-এর চেয়ে অনেক বেশি performant।

**Q14: MutationObserver কী?**
> **A:** DOM-এ কোনো change হলে detect করে — attribute change, child nodes যোগ/বাদ, text content change। Virtual DOM implementation, dynamic content monitoring-এ ব্যবহার।

**Q15: Form validation-এ HTML5 API vs JavaScript-এর পার্থক্য?**
> **A:** HTML5 built-in: `required`, `minlength`, `pattern` — সহজ কিন্তু custom error message বা complex logic কঠিন। JavaScript: সম্পূর্ণ control, custom messages, async validation (API call), multi-field validation সম্ভব। Production-এ দুটিই ব্যবহার করা হয়।

</details>

<details>
<summary><strong>🔹 Tricky & Practical Questions (Q16–Q20)</strong></summary>
<br>

**Q16: Event listener remove করতে না পারলে কী সমস্যা হয়?**
> **A:** **Memory leak**। Element DOM থেকে remove হলেও listener active থাকলে সেই element ও তার closure garbage collected হয় না। `removeEventListener` দিয়ে remove করুন। অথবা `{ once: true }` option ব্যবহার করুন।

**Q17: `closest()` method কী করে?**
> **A:** Current element থেকে শুরু করে ancestor chain-এ CSS selector match খোঁজে। Event delegation-এ `e.target.closest(".item")` দিয়ে nested element-এ click হলে parent item বের করা যায়।

**Q18: Cookies JavaScript দিয়ে set করা এবং server দিয়ে set করার পার্থক্য?**
> **A:** Server `Set-Cookie` header দিয়ে `HttpOnly` flag সহ cookie set করলে JavaScript access করতে পারে না (XSS safe)। JavaScript `document.cookie` দিয়ে set করলে JS-এ readable — sensitive data (auth token) server থেকে HttpOnly cookie-তে রাখুন।

**Q19: Web Storage-এ Object সরাসরি রাখা যায় না কেন?**
> **A:** Web Storage শুধু string store করে। Object রাখতে `JSON.stringify()`, পড়তে `JSON.parse()` দরকার। Function, `undefined`, `Symbol` JSON-এ serialize হয় না — হারিয়ে যায়।

**Q20: Passive event listener কী? কেন দরকার?**
> **A:** `{ passive: true }` option দিলে browser জানে এই listener `preventDefault()` call করবে না — তাই scroll rendering optimize করতে পারে। Touch/scroll events-এ passive listener না থাকলে browser scroll শুরু করার আগে JS-এর জন্য wait করে — জার্কি scroll। `window.addEventListener("scroll", fn, { passive: true })`।

</details>

---

<div align="right">
  <a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a>
</div>

---

> **🚀 PART 4 আসছে:** ES6+ Features — Destructuring, Spread/Rest, Optional Chaining, Nullish Coalescing, Map, Set, WeakMap, WeakSet, Array Methods, Dynamic Import এবং আরও।
>
> **💬 পরবর্তী PART পেতে:** "PART 4 দাও" লিখুন।


---

<a id="part4"></a>

# PART 4 — ES6+ Features

> **📍 এই PART-এর Sections:** [৪.১ Destructuring](#৪১-destructuring) · [৪.২ Spread Operator](#৪২-spread-operator) · [৪.৩ Rest Operator](#৪৩-rest-operator) · [৪.৪ Optional Chaining](#৪৪-optional-chaining) · [৪.৫ Nullish Coalescing](#৪৫-nullish-coalescing) · [৪.৬ Map](#৪৬-map) · [৪.৭ Set](#৪৭-set) · [৪.৮ WeakMap ও WeakSet](#৪৮-weakmap-ও-weakset) · [৪.৯ Array Methods](#৪৯-array-methods) · [৪.১০ Object Methods](#৪১০-object-methods) · [৪.১১ Iterators ও Generators](#৪১১-iterators-ও-generators) · [৪.১২ Dynamic Import](#৪১২-dynamic-import) · [৪.১৩ Interview Q&A](#৪১৩-part-4--interview-questions--answers)

---

## ৪.১ Destructuring

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Destructuring** হলো Array বা Object থেকে values বের করে আলাদা variables-এ assign করার সংক্ষিপ্ত পদ্ধতি। ES6-এর অন্যতম গুরুত্বপূর্ণ feature।

### 🏠 বাস্তব জীবনের উদাহরণ

> মনে করুন একটি গিফট বাক্সে তিনটি জিনিস আছে। আগে একটা একটা করে বের করতে হতো। Destructuring দিয়ে এক লাইনে তিনটিই বের করা যায়।

### 💻 Array Destructuring

```javascript
// পুরনো পদ্ধতি
const colors = ["red", "green", "blue"];
const first = colors[0];
const second = colors[1];

// ✅ Array Destructuring
const [red, green, blue] = colors;
console.log(red);   // "red"
console.log(green); // "green"

// ১. Skip করা
const [, , third] = colors;
console.log(third); // "blue"

// ২. Default values
const [a = "default", b = "fallback"] = ["hello"];
console.log(a); // "hello"
console.log(b); // "fallback"

// ৩. Rest with destructuring
const [head, ...tail] = [1, 2, 3, 4, 5];
console.log(head); // 1
console.log(tail); // [2, 3, 4, 5]

// ৪. Swap variables (elegant!)
let x = 1, y = 2;
[x, y] = [y, x];
console.log(x, y); // 2, 1

// ৫. Function return
function getCoords() {
  return [23.8103, 90.4125]; // Dhaka coordinates
}
const [lat, lng] = getCoords();

// ৬. Nested array
const matrix = [[1, 2], [3, 4]];
const [[a1, a2], [b1, b2]] = matrix;
console.log(a1, b2); // 1, 4
```

### 💻 Object Destructuring

```javascript
const user = {
  name: "Rahim",
  age: 25,
  city: "Dhaka",
  role: "Developer",
  address: {
    street: "Mirpur",
    zip: "1216"
  }
};

// Basic
const { name, age, city } = user;
console.log(name, age); // "Rahim" 25

// ১. Rename করা
const { name: userName, age: userAge } = user;
console.log(userName); // "Rahim"

// ২. Default values
const { name: n, salary = 50000 } = user;
console.log(salary); // 50000 (না থাকলে default)

// ৩. Nested destructuring
const { address: { street, zip } } = user;
console.log(street); // "Mirpur"

// ৪. Rest
const { name: nm, ...rest } = user;
console.log(rest); // { age: 25, city: "Dhaka", role: "Developer", address: {...} }

// ৫. Function parameter destructuring
function greetUser({ name, age, city = "Unknown" }) {
  return `${name} (${age}) থেকে ${city}`;
}
console.log(greetUser(user)); // "Rahim (25) থেকে Dhaka"

// ৬. API response handling
async function fetchUser(id) {
  const response = await fetch(`/api/users/${id}`);
  const { data: { user: { name, email } }, status } = await response.json();
  // deeply nested একবারে
}

// ৭. Array of objects
const users = [
  { id: 1, name: "Rahim" },
  { id: 2, name: "Karim" }
];
const [{ name: first }, { name: second }] = users;
console.log(first, second); // "Rahim" "Karim"
```

### ⚠️ Common Mistakes

```javascript
// ❌ undefined থেকে destructure করা
const { name } = undefined; // TypeError!
// ✅ Default value দিন
const { name } = user || {};
// বা optional chaining:
const name = user?.name;

// ❌ Rename আর default একসাথে
const { name: n = "Guest" } = {}; // ✅ এটা valid!
// syntax: { key: newName = defaultValue }

// ❌ Nested destructuring-এ intermediate undefined
const { address: { street } } = { name: "Rahim" }; // TypeError! address undefined
// ✅
const { address: { street } = {} } = { name: "Rahim" };
```

---

## ৪.২ Spread Operator

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Spread Operator (`...`)** iterable (array, string, object) কে individual elements-এ ছড়িয়ে দেয়।

### 💻 Spread Examples

```javascript
// ১. Array copy ও merge
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

const copy = [...arr1];          // shallow copy
const merged = [...arr1, ...arr2]; // [1, 2, 3, 4, 5, 6]
const withExtra = [0, ...arr1, ...arr2, 7]; // [0, 1, 2, 3, 4, 5, 6, 7]

// ২. Object copy ও merge
const defaults = { theme: "light", lang: "en", fontSize: 14 };
const userPrefs = { theme: "dark", fontSize: 16 };

const merged2 = { ...defaults, ...userPrefs };
// { theme: "dark", lang: "en", fontSize: 16 }
// ⚠️ পরেরটি আগেরটি override করে

// ৩. Function arguments
function sum(a, b, c) { return a + b + c; }
const nums = [1, 2, 3];
console.log(sum(...nums)); // 6 (apply এর modern alternative)

// Math.max
console.log(Math.max(...[3, 1, 4, 1, 5, 9])); // 9

// ৪. String spread
const chars = [..."Hello"]; // ["H", "e", "l", "l", "o"]
const unique = [...new Set("hello")]; // ["h", "e", "l", "o"]

// ৫. DOM NodeList to Array
const elements = [...document.querySelectorAll(".item")];
elements.map(el => el.style.color = "red"); // এখন map করা যাবে

// ৬. Immutable state update (React pattern)
const state = { user: "Rahim", count: 0 };
const newState = { ...state, count: state.count + 1 };
// { user: "Rahim", count: 1 } — original অপরিবর্তিত

// ৭. Remove a property immutably
const { role, ...withoutRole } = user;
// withoutRole-এ role নেই
```

### ⚠️ Shallow Copy — সতর্কতা

```javascript
const original = { name: "Rahim", address: { city: "Dhaka" } };
const copy = { ...original };

copy.name = "Karim";          // OK — primitive, independent
copy.address.city = "Ctg";    // ❌ original.address.city ও বদলে গেছে!

// কারণ: address একটি nested object — reference copy হয়েছে
// Deep copy এর জন্য structuredClone() বা JSON.parse(JSON.stringify())
```

---

## ৪.৩ Rest Operator

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Rest Operator (`...`)** — spread-এর বিপরীত। বাকি সব elements-কে একটি array-এ collect করে। Syntax একই (`...`) কিন্তু context আলাদা।

```javascript
// ১. Function parameters
function sum(first, second, ...rest) {
  console.log(first);  // 1
  console.log(second); // 2
  console.log(rest);   // [3, 4, 5]
  return first + second + rest.reduce((a, b) => a + b, 0);
}
sum(1, 2, 3, 4, 5); // 15

// ২. Destructuring rest
const [head, ...tail] = [1, 2, 3, 4];
// head = 1, tail = [2, 3, 4]

const { name, ...others } = { name: "Rahim", age: 25, city: "Dhaka" };
// name = "Rahim", others = { age: 25, city: "Dhaka" }

// ৩. Rest must be last
function wrong(first, ...rest, last) {} // SyntaxError!
function correct(first, ...rest) {
  const last = rest[rest.length - 1]; // workaround
}
```

### 📊 Spread vs Rest

| | Spread (`...`) | Rest (`...`) |
|--|---------------|-------------|
| **কী করে** | ছড়িয়ে দেয় | একসাথে করে |
| **Context** | Function call, array/object literal | Function params, destructuring |
| **দিক** | One → Many | Many → One |
| **Example** | `fn(...arr)` | `fn(...args)` |

---

## ৪.৪ Optional Chaining

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Optional Chaining (`?.`)** — ES2020। Nested object-এর property access-এ intermediate value `null` বা `undefined` হলে error না দিয়ে `undefined` return করে।

### 💻 Optional Chaining Examples

```javascript
const user = {
  name: "Rahim",
  address: {
    city: "Dhaka",
    zip: "1216"
  },
  getFullName() {
    return `${this.name} Ahmed`;
  }
};

// ❌ পুরনো পদ্ধতি — verbose
const city = user && user.address && user.address.city;
const zip = user && user.address && user.address.zip;

// ✅ Optional Chaining
console.log(user?.address?.city);        // "Dhaka"
console.log(user?.phone?.number);        // undefined (error নেই!)
console.log(user?.address?.country?.code); // undefined

// Method call
console.log(user?.getFullName?.());      // "Rahim Ahmed"
console.log(user?.nonExistentMethod?.()); // undefined

// Array access
const users = [{ name: "Rahim" }];
console.log(users?.[0]?.name);           // "Rahim"
console.log(users?.[5]?.name);           // undefined

// With Nullish Coalescing
const city2 = user?.address?.city ?? "Unknown City";
console.log(city2); // "Dhaka"

const phone = user?.phone?.number ?? "No phone";
console.log(phone); // "No phone"

// API response handling
async function getUser(id) {
  const response = await fetch(`/api/users/${id}`);
  const data = await response.json();
  // Safe deeply nested access
  return data?.user?.profile?.avatar ?? "/default-avatar.png";
}
```

---

## ৪.৫ Nullish Coalescing

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Nullish Coalescing (`??`)** — ES2020। বাম দিক `null` বা `undefined` হলে ডান দিক return করে। `||` থেকে পার্থক্য: `0`, `""`, `false` এগুলো falsy কিন্তু nullish নয়।

```javascript
// || vs ?? তুলনা
console.log(0 || "default");    // "default" (0 falsy)
console.log(0 ?? "default");    // 0 (0 nullish নয়!)

console.log("" || "default");   // "default" ("" falsy)
console.log("" ?? "default");   // "" ("" nullish নয়!)

console.log(false || "default"); // "default"
console.log(false ?? "default"); // false

console.log(null || "default");  // "default"
console.log(null ?? "default");  // "default"

console.log(undefined || "default"); // "default"
console.log(undefined ?? "default"); // "default"

// Practical use cases
function getUserSettings(settings) {
  return {
    fontSize: settings.fontSize ?? 16,  // 0 হলেও রাখা যাবে
    darkMode: settings.darkMode ?? false, // false হলেও রাখা যাবে
    username: settings.username ?? "Guest"
  };
}

getUserSettings({ fontSize: 0, darkMode: false });
// { fontSize: 0, darkMode: false, username: "Guest" }
// ✅ fontSize: 0 এবং darkMode: false সঠিকভাবে রাখা হয়েছে

// ??= — Logical Nullish Assignment (ES2021)
let config = { port: null };
config.port ??= 3000;  // null ছিল, তাই 3000 assign
config.port ??= 8080;  // 3000 আছে (not null), তাই change হয়নি
console.log(config.port); // 3000
```

---

## ৪.৬ Map

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Map** হলো key-value pairs-এর collection যেখানে key যেকোনো type হতে পারে (object, function, primitive)। Regular object-এর key শুধু string বা Symbol।

### 💻 Map API

```javascript
// ১. Map তৈরি
const map = new Map();

// set — key-value যোগ
map.set("name", "Rahim");
map.set(1, "Number key");
map.set(true, "Boolean key");
const objKey = { id: 1 };
map.set(objKey, "Object as key!"); // Object key — regular object-এ সম্ভব নয়

// get
console.log(map.get("name"));   // "Rahim"
console.log(map.get(1));        // "Number key"
console.log(map.get(objKey));   // "Object as key!"
console.log(map.get("missing")); // undefined

// has, delete, size
console.log(map.has("name"));  // true
map.delete("name");
console.log(map.size);         // 3

// ২. Iteration
const scores = new Map([
  ["Rahim", 95],
  ["Karim", 87],
  ["Jamal", 92]
]);

for (const [name, score] of scores) {
  console.log(`${name}: ${score}`);
}

scores.forEach((score, name) => {
  console.log(`${name}: ${score}`);
});

console.log([...scores.keys()]);   // ["Rahim", "Karim", "Jamal"]
console.log([...scores.values()]); // [95, 87, 92]
console.log([...scores.entries()]); // [["Rahim", 95], ...]

// ৩. Map থেকে Array এবং Object
const arr = [...scores]; // [["Rahim", 95], ["Karim", 87], ...]
const obj = Object.fromEntries(scores); // { Rahim: 95, Karim: 87, ... }

// Object থেকে Map
const config = { host: "localhost", port: 3000 };
const configMap = new Map(Object.entries(config));
```

### 📊 Map vs Object

| | Map | Object |
|--|-----|--------|
| **Key type** | যেকোনো type | String বা Symbol |
| **Order** | Insertion order ✅ | ES2015+ string keys ordered |
| **Size** | `.size` | `Object.keys(obj).length` |
| **Iteration** | Direct iterable | `for...in` বা methods |
| **Performance** | frequent add/delete-এ ভালো | Simple lookups-এ ভালো |
| **JSON** | ❌ সরাসরি নয় | ✅ |

---

## ৪.৭ Set

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Set** হলো **unique values-এর** collection। Duplicate automatically বাদ পড়ে।

### 💻 Set API

```javascript
// ১. Set তৈরি
const set = new Set([1, 2, 3, 2, 1, 3]);
console.log(set); // Set {1, 2, 3} — duplicates বাদ

set.add(4);
set.add(2);      // duplicate — ignored
set.delete(1);
console.log(set.has(3));  // true
console.log(set.size);    // 3

// ২. Array এর duplicate সরানো (সবচেয়ে popular use)
const numbers = [1, 2, 2, 3, 3, 4, 5, 5];
const unique = [...new Set(numbers)];
console.log(unique); // [1, 2, 3, 4, 5]

// String থেকে unique chars
const uniqueChars = [...new Set("programming")];
// ["p", "r", "o", "g", "a", "m", "i", "n"]

// ৩. Iteration
const fruits = new Set(["Apple", "Banana", "Mango"]);
for (const fruit of fruits) {
  console.log(fruit);
}
fruits.forEach(fruit => console.log(fruit));

// ৪. Set operations (JS-এ built-in নেই, manually করতে হয়)
const setA = new Set([1, 2, 3, 4]);
const setB = new Set([3, 4, 5, 6]);

// Union (একত্রিত)
const union = new Set([...setA, ...setB]); // {1, 2, 3, 4, 5, 6}

// Intersection (সাধারণ)
const intersection = new Set([...setA].filter(x => setB.has(x))); // {3, 4}

// Difference (A-তে আছে B-তে নেই)
const difference = new Set([...setA].filter(x => !setB.has(x))); // {1, 2}

// ৫. Object uniqueness (reference-based, কাজ করে না!)
const objSet = new Set();
objSet.add({ id: 1 });
objSet.add({ id: 1 }); // আলাদা reference — দুটোই যোগ হবে!
console.log(objSet.size); // 2 (expected 1, but 2!)
```

---

## ৪.৮ WeakMap ও WeakSet

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**WeakMap** ও **WeakSet** হলো Map ও Set-এর special versions যেখানে key/value শুধু object হতে পারে এবং **garbage collection** prevent করে না।

```javascript
// WeakMap — key হতে হবে object, GC prevent করে না
const weakMap = new WeakMap();

let user = { name: "Rahim" };
weakMap.set(user, { sessionData: "abc123" });
console.log(weakMap.get(user)); // { sessionData: "abc123" }

user = null; // object reference মুছে দিলে
// GC weakMap entry পরিষ্কার করবে — memory leak নেই!

// Practical: Private data
const _private = new WeakMap();
class Person {
  constructor(name, age) {
    _private.set(this, { age }); // private data
    this.name = name;
  }
  getAge() {
    return _private.get(this).age;
  }
}

const p = new Person("Rahim", 25);
console.log(p.getAge()); // 25
console.log(p.age);      // undefined (private!)

// WeakSet — unique objects, GC-friendly
const weakSet = new WeakSet();
let obj = { id: 1 };
weakSet.add(obj);
console.log(weakSet.has(obj)); // true
obj = null; // auto-cleaned

// Practical: Tracking visited objects
const visited = new WeakSet();
function process(obj) {
  if (visited.has(obj)) return; // circular reference রোধ
  visited.add(obj);
  // process...
}
```

### 📊 Map/Set vs WeakMap/WeakSet

| | Map/Set | WeakMap/WeakSet |
|--|---------|----------------|
| **Key type** | যেকোনো | Object only |
| **GC** | Prevent করে | Prevent করে না |
| **Iterable** | ✅ | ❌ |
| **Size** | `.size` | ❌ |
| **Use case** | General | Private data, caching |

---

## ৪.৯ Array Methods

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Transformation Methods

```javascript
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const users = [
  { name: "Rahim", age: 25, score: 85 },
  { name: "Karim", age: 30, score: 92 },
  { name: "Jamal", age: 22, score: 78 },
  { name: "Nadia", age: 28, score: 96 }
];

// ১. map — প্রতিটি element transform করে নতুন array
const doubled = numbers.map(n => n * 2);
// [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

const names = users.map(u => u.name);
// ["Rahim", "Karim", "Jamal", "Nadia"]

const userCards = users.map(({ name, score }) => ({
  display: `${name}: ${score}%`,
  passed: score >= 80
}));

// ২. filter — condition সত্য এমন elements
const evens = numbers.filter(n => n % 2 === 0); // [2, 4, 6, 8, 10]
const passing = users.filter(u => u.score >= 80); // Rahim, Karim, Nadia

// ৩. reduce — array → single value
const sum = numbers.reduce((acc, n) => acc + n, 0); // 55
const max = numbers.reduce((max, n) => n > max ? n : max, -Infinity); // 10

// Object তৈরি
const scoreMap = users.reduce((map, user) => {
  map[user.name] = user.score;
  return map;
}, {});
// { Rahim: 85, Karim: 92, Jamal: 78, Nadia: 96 }

// ৪. find / findIndex
const highScorer = users.find(u => u.score > 90); // Karim
const idx = users.findIndex(u => u.name === "Jamal"); // 2

// ৫. some / every
const anyPass = users.some(u => u.score > 90);   // true (Karim, Nadia)
const allPass = users.every(u => u.score > 75);  // true (সবার > 75)

// ৬. flat / flatMap (ES2019)
const nested = [[1, 2], [3, [4, 5]]];
console.log(nested.flat());    // [1, 2, 3, [4, 5]]
console.log(nested.flat(2));   // [1, 2, 3, 4, 5]
console.log(nested.flat(Infinity)); // সব flatten

const sentences = ["Hello World", "Foo Bar"];
const words = sentences.flatMap(s => s.split(" "));
// ["Hello", "World", "Foo", "Bar"]

// ৭. sort — মনে রাখুন: mutates original!
const nums = [10, 1, 20, 2, 5];
nums.sort((a, b) => a - b); // ascending: [1, 2, 5, 10, 20]
nums.sort((a, b) => b - a); // descending: [20, 10, 5, 2, 1]

// Object sort
users.sort((a, b) => b.score - a.score); // score descending

// sort না করতে চাইলে copy
const sorted = [...numbers].sort((a, b) => b - a);

// ৮. Array.from
Array.from({ length: 5 }, (_, i) => i + 1); // [1, 2, 3, 4, 5]
Array.from("Hello"); // ["H", "e", "l", "l", "o"]
Array.from(new Set([1, 2, 2, 3])); // [1, 2, 3]

// ৯. at() — negative index (ES2022)
const arr = [1, 2, 3, 4, 5];
console.log(arr.at(-1));  // 5 (last)
console.log(arr.at(-2));  // 4 (second last)

// ১০. includes / indexOf
console.log([1, 2, 3].includes(2));    // true
console.log([1, 2, NaN].includes(NaN)); // true (indexOf-এ false!)
console.log([1, 2, 3].indexOf(2));     // 1

// ১১. Method chaining
const result = users
  .filter(u => u.age >= 25)
  .sort((a, b) => b.score - a.score)
  .map(u => `${u.name}: ${u.score}`)
  .join(", ");
// "Nadia: 96, Karim: 92, Rahim: 85"
```

### 📊 Array Methods Quick Reference

| Method | কী করে | Mutates? | Return |
|--------|---------|----------|--------|
| `map` | Transform | ❌ | নতুন array |
| `filter` | Filter | ❌ | নতুন array |
| `reduce` | Accumulate | ❌ | Single value |
| `find` | প্রথম match | ❌ | Element বা undefined |
| `findIndex` | প্রথম match index | ❌ | Index বা -1 |
| `some` | কোনো একটি match? | ❌ | Boolean |
| `every` | সব match? | ❌ | Boolean |
| `flat` | Flatten | ❌ | নতুন array |
| `flatMap` | map + flat | ❌ | নতুন array |
| `sort` | Sort | ✅ | Same array |
| `reverse` | Reverse | ✅ | Same array |
| `push/pop` | Add/remove শেষে | ✅ | Length/element |
| `shift/unshift` | Add/remove শুরুতে | ✅ | Element/length |
| `splice` | Insert/remove যেখানে | ✅ | Removed elements |
| `slice` | Portion copy | ❌ | নতুন array |
| `includes` | আছে কিনা? | ❌ | Boolean |
| `indexOf` | প্রথম index | ❌ | Index বা -1 |
| `join` | Array → String | ❌ | String |
| `concat` | Merge | ❌ | নতুন array |
| `fill` | Fill with value | ✅ | Same array |

---

## ৪.১০ Object Methods

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 ES6+ Object Methods

```javascript
const user = { name: "Rahim", age: 25, city: "Dhaka" };

// ১. Object.keys / values / entries
console.log(Object.keys(user));    // ["name", "age", "city"]
console.log(Object.values(user));  // ["Rahim", 25, "Dhaka"]
console.log(Object.entries(user)); // [["name","Rahim"],["age",25],["city","Dhaka"]]

// Iteration
Object.entries(user).forEach(([key, value]) => {
  console.log(`${key}: ${value}`);
});

// ২. Object.assign — shallow merge
const defaults = { theme: "light", lang: "en" };
const config = Object.assign({}, defaults, { theme: "dark" });
// { theme: "dark", lang: "en" }
// Modern alternative: spread { ...defaults, ...overrides }

// ৩. Object.freeze — immutable object
const constants = Object.freeze({ PI: 3.14159, E: 2.71828 });
constants.PI = 3; // silently ignored (strict mode-এ TypeError)
constants.new = "value"; // ignored
console.log(constants.PI); // 3.14159 (unchanged)

// ৪. Object.fromEntries — entries থেকে object (ES2019)
const entries = [["name", "Rahim"], ["age", 25]];
const obj = Object.fromEntries(entries);
// { name: "Rahim", age: 25 }

// Map → Object
const map = new Map([["a", 1], ["b", 2]]);
const fromMap = Object.fromEntries(map); // { a: 1, b: 2 }

// Query string parse
const params = new URLSearchParams("name=Rahim&age=25");
const paramsObj = Object.fromEntries(params); // { name: "Rahim", age: "25" }

// ৫. Object.create
const proto = {
  greet() { return `Hello, ${this.name}`; }
};
const person = Object.create(proto);
person.name = "Rahim";
console.log(person.greet()); // "Hello, Rahim"

// ৬. Computed property names
const key = "dynamic";
const obj2 = {
  [key]: "value",              // dynamic key
  [`${key}Count`]: 5,         // template literal key
  ["method" + "Name"]() {}    // computed method name
};
console.log(obj2.dynamic);     // "value"
console.log(obj2.dynamicCount); // 5

// ৭. Shorthand property
const name = "Rahim";
const age = 25;
const user2 = { name, age }; // { name: "Rahim", age: 25 }

// ৮. Property shorthand methods
const calculator = {
  value: 0,
  add(n) { this.value += n; return this; }, // shorthand
  multiply(n) { this.value *= n; return this; },
  result() { return this.value; }
};
console.log(calculator.add(5).multiply(3).result()); // 15

// ৯. Object.hasOwn (ES2022 — hasOwnProperty alternative)
console.log(Object.hasOwn(user, "name")); // true
console.log(Object.hasOwn(user, "toString")); // false (prototype)
```

---

## ৪.১১ Iterators ও Generators

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 Iterator Protocol

```javascript
// Iterator — next() method আছে যা {value, done} return করে
function makeRangeIterator(start, end) {
  let current = start;
  return {
    next() {
      if (current <= end) {
        return { value: current++, done: false };
      }
      return { value: undefined, done: true };
    },
    [Symbol.iterator]() { return this; } // iterable করে
  };
}

const range = makeRangeIterator(1, 5);
console.log(range.next()); // { value: 1, done: false }
console.log(range.next()); // { value: 2, done: false }

for (const num of makeRangeIterator(1, 5)) {
  console.log(num); // 1, 2, 3, 4, 5
}
```

### 💻 Generators (function*)

```javascript
// Generator — yield দিয়ে একটা একটা value produce করে
function* numberGenerator(start = 1) {
  while (true) {
    yield start++; // একটা value দিয়ে pause
  }
}

const gen = numberGenerator();
console.log(gen.next()); // { value: 1, done: false }
console.log(gen.next()); // { value: 2, done: false }
console.log(gen.next()); // { value: 3, done: false }

// Finite generator
function* fibonacci() {
  let [a, b] = [0, 1];
  while (true) {
    yield a;
    [a, b] = [b, a + b];
  }
}

const fib = fibonacci();
const first10 = Array.from({ length: 10 }, () => fib.next().value);
console.log(first10); // [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]

// Practical: Pagination
function* paginate(data, pageSize) {
  for (let i = 0; i < data.length; i += pageSize) {
    yield data.slice(i, i + pageSize);
  }
}

const allUsers = Array.from({ length: 25 }, (_, i) => `User ${i + 1}`);
const pages = paginate(allUsers, 10);
console.log(pages.next().value); // ["User 1", ..., "User 10"]
console.log(pages.next().value); // ["User 11", ..., "User 20"]
console.log(pages.next().value); // ["User 21", ..., "User 25"]
```

---

## ৪.১২ Dynamic Import

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Dynamic Import (`import()`)** — ES2020। Module-কে runtime-এ, on-demand load করা। Static import-এর বিপরীতে lazy loading সম্ভব।

```javascript
// Static import (always loads)
import { heavyFunction } from "./heavy-module.js";

// Dynamic import (on-demand)
async function loadHeavyModule() {
  const module = await import("./heavy-module.js");
  module.heavyFunction();
}

// Conditional loading
async function loadChart(type) {
  if (type === "bar") {
    const { BarChart } = await import("./bar-chart.js");
    return new BarChart();
  } else {
    const { LineChart } = await import("./line-chart.js");
    return new LineChart();
  }
}

// User action-এ load
document.querySelector("#load-btn").addEventListener("click", async () => {
  const { default: Modal } = await import("./modal.js");
  new Modal().show();
});

// Code splitting (React-এ)
// const LazyComponent = React.lazy(() => import("./HeavyComponent"));

// Error handling
async function safeImport(path) {
  try {
    const module = await import(path);
    return module;
  } catch (err) {
    console.error(`Module ${path} load failed:`, err);
    return null;
  }
}
```

---

## ৪.১৩ PART 4 — Interview Questions & Answers

<div align="right"><a href="#part4">⬆ PART 4 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

<details>
<summary><strong>🔹 Destructuring, Spread, Rest (Q1–Q10)</strong></summary>
<br>

**Q1: Destructuring কী? Array ও Object destructuring-এর পার্থক্য?**
> **A:** Destructuring হলো Array বা Object থেকে values extract করে variables-এ assign করার সংক্ষিপ্ত syntax। Array destructuring position-based `[a, b] = arr`। Object destructuring name-based `{ name, age } = obj`। Object-এ rename করা যায় `{ name: n }`, default value দেওয়া যায় `{ age = 18 }`।

**Q2: Spread এবং Rest operator-এর পার্থক্য?**
> **A:** দুটিতেই `...` — কিন্তু context আলাদা। Spread: iterable কে ছড়িয়ে দেয় — `fn(...arr)`, `[...arr1, ...arr2]`। Rest: বাকি সব একত্র করে — `function(a, ...rest)`, `const [head, ...tail] = arr`। Spread = one → many, Rest = many → one।

**Q3: `||` এবং `??` (Nullish Coalescing)-এর পার্থক্য?**
> **A:** `||` — বাম দিক falsy (false, 0, "", null, undefined, NaN) হলে ডান দিক। `??` — শুধু null বা undefined হলে ডান দিক। `0 || 5 = 5` কিন্তু `0 ?? 5 = 0`। API response-এ 0 বা "" valid value হলে `??` ব্যবহার করুন।

**Q4: Optional Chaining (?.) কী? কখন দরকার?**
> **A:** Nested property access-এ intermediate null/undefined হলে TypeError না দিয়ে undefined return করে। `user?.address?.city` — address না থাকলে error নেই। Method call: `obj?.method?.()`, Array: `arr?.[0]`. Deep API response navigate করতে এবং optional properties-এ essential।

**Q5: Object-এ spread করলে কী হয়? Deep vs Shallow copy?**
> **A:** `{...obj}` shallow copy করে — top-level primitive values নতুন copy পায়, nested objects শুধু reference copy হয়। Nested object পরিবর্তন করলে original-ও পরিবর্তিত হয়। Deep copy-র জন্য `structuredClone()` বা `JSON.parse(JSON.stringify())`।

**Q6: Array-এর duplicate remove করবেন কীভাবে?**
> **A:** `[...new Set(arr)]` — সবচেয়ে সহজ। `arr.filter((v, i, a) => a.indexOf(v) === i)` — traditional। Object array-এ: `arr.filter((v, i, a) => a.findIndex(t => t.id === v.id) === i)` — property-based।

**Q7: Array sort কীভাবে কাজ করে? ভুল কোথায়?**
> **A:** Default sort টা numbers-কে string হিসেবে sort করে — `[10, 1, 20].sort()` = `[1, 10, 20]`। Number sort-এর জন্য: `arr.sort((a, b) => a - b)` ascending। sort original array mutate করে — copy করতে `[...arr].sort()` বা `arr.toSorted()` (ES2023)।

**Q8: map, filter, reduce-এর মধ্যে পার্থক্য?**
> **A:** `map` — প্রতিটি element transform, same length array। `filter` — condition true elements, subset array। `reduce` — সব elements একত্র করে single value (sum, object, nested array)। তিনটিই non-mutating, নতুন array/value return করে।

**Q9: Map এবং Object-এর পার্থক্য? কখন Map ব্যবহার করবেন?**
> **A:** Map: যেকোনো type key (object, function), insertion order guaranteed, `.size` property, directly iterable, frequent add/delete-এ performant। Object: string/Symbol key, JSON serializable। Object-কে key হিসেবে ব্যবহার করতে, dynamic keys অনেক হলে, বা iteration performance দরকার হলে Map।

**Q10: Set-এ Object-এর uniqueness কীভাবে কাজ করে?**
> **A:** Set reference equality ব্যবহার করে। `new Set([{id:1}, {id:1}])` size 2 হবে কারণ দুটি আলাদা object reference। Primitive values (`1, "a", true`) strict equality দিয়ে unique check হয়।

</details>

<details>
<summary><strong>🔹 Advanced ES6+ (Q11–Q20)</strong></summary>
<br>

**Q11: WeakMap এবং WeakSet কেন দরকার? কখন ব্যবহার করবেন?**
> **A:** WeakMap/WeakSet-এর key/value object-গুলো Garbage Collection prevent করে না। Object reference চলে গেলে auto-cleanup হয় — memory leak এড়ানো যায়। Use case: private class data, DOM element-এর metadata সংরক্ষণ (element remove হলে auto-clean), circular structure handling।

**Q12: Generator function কী? সাধারণ function থেকে কীভাবে আলাদা?**
> **A:** Generator (`function*`) `yield` দিয়ে value দিতে পারে এবং pause হতে পারে। `.next()` call করলে পরবর্তী yield পর্যন্ত চলে। Regular function একবার চলে সম্পূর্ণ return করে। Use case: infinite sequences (Fibonacci), lazy evaluation, pagination, async flow control।

**Q13: Dynamic import কেন ব্যবহার করবেন?**
> **A:** Lazy loading — module শুধু দরকারের সময় load করা। Bundle size কমায় (code splitting)। Conditional loading — কোন module দরকার runtime-এ decide করা। Initial page load দ্রুত হয়।

**Q14: Array-এর `flat()` এবং `flatMap()` কী?**
> **A:** `flat(depth)` — nested array flatten করে। Default depth 1, `flat(Infinity)` সম্পূর্ণ flatten। `flatMap(fn)` — প্রতিটি element-এ map করে তারপর এক level flatten — `map().flat()` এর shortcut কিন্তু efficient।

**Q15: `Object.freeze()` এবং `const`-এর পার্থক্য?**
> **A:** `const` — variable re-assignment রোধ করে, কিন্তু object mutate করা যায়। `Object.freeze()` — object-এর properties পরিবর্তন রোধ করে (shallow — nested objects freeze হয় না)। `const` + `Object.freeze()` একসাথে দিলে সম্পূর্ণ immutable (top level)।

**Q16: Computed property names কী?**
> **A:** Object-এ dynamic key ব্যবহার: `{ [varName]: value }`, `{ [\`prefix_${id}\`]: data }`। Runtime-এ key নির্ধারণ করতে হলে useful। Redux action creators, API response normalization-এ ব্যবহার।

**Q17: `Array.from()` কী? কখন ব্যবহার করবেন?**
> **A:** Array-like (NodeList, arguments) বা iterable (Set, Map, String) থেকে real Array তৈরি করে। দ্বিতীয় argument: map function। `Array.from({length: 5}, (_, i) => i)` = `[0,1,2,3,4]`। `Array.from(document.querySelectorAll("li"))` — NodeList → Array।

**Q18: Symbol কী? কখন ব্যবহার করবেন?**
> **A:** ES6-এর unique primitive। প্রতিটি Symbol() unique — `Symbol("id") !== Symbol("id")`। Object key হিসেবে collision-free unique keys। Well-known Symbols: `Symbol.iterator` (iterable করতে), `Symbol.toPrimitive` (type conversion customize)। Library/framework-এ internal properties hide করতে।

**Q19: Optional Chaining কি undefined এবং null উভয়-এ কাজ করে?**
> **A:** হ্যাঁ — `?.` শুধু `null` বা `undefined`-এ short-circuit করে। `0`, `false`, `""` (falsy কিন্তু nullish নয়) — short-circuit করে না। `0?.toString()` = `"0"` (0 valid value)।

**Q20: Destructuring-এ default value কখন কাজ করে?**
> **A:** শুধু `undefined`-এ। `null`-এ কাজ করে না! `const { a = 5 } = { a: undefined }` → `a = 5`. `const { a = 5 } = { a: null }` → `a = null`। এই behavior `??` operator-এর মতোই।

</details>

---

<div align="right">
  <a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a>
</div>

---

> **🚀 PART 5 আসছে:** Asynchronous JavaScript — Synchronous vs Async, setTimeout, setInterval, Callback Hell, Promise Chaining, Promise.all, Async/Await Internals, Error Handling, Real API Calls।
>
> **💬 পরবর্তী PART পেতে:** "PART 5 দাও" লিখুন।


---

<a id="part5"></a>

# PART 5 — Asynchronous JavaScript

> **📍 এই PART-এর Sections:** [৫.১ Sync vs Async](#৫১-synchronous-vs-asynchronous) · [৫.২ setTimeout ও setInterval](#৫২-settimeout-ও-setinterval) · [৫.৩ Callback Hell](#৫৩-callback-hell) · [৫.৪ Promise](#৫৪-promise) · [৫.৫ Promise Chaining](#৫৫-promise-chaining) · [৫.৬ Promise Combinators](#৫৬-promise-combinators) · [৫.৭ Async/Await](#৫৭-asyncawait) · [৫.৮ Error Handling](#৫৮-error-handling) · [৫.৯ Real API Calls](#৫৯-real-api-calls) · [৫.১০ AbortController](#৫১০-abortcontroller) · [৫.১১ Interview Q&A](#৫১১-part-5--interview-questions--answers)

---

## ৫.১ Synchronous vs Asynchronous

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Synchronous (Sync):** এক লাইন শেষ হলে পরের লাইন। কোনো কাজ দীর্ঘ সময় নিলে বাকি সব wait করে (blocking)।

**Asynchronous (Async):** দীর্ঘ কাজ শুরু করে দিয়ে বাকি code চালাতে থাকে। কাজ শেষ হলে callback/Promise-এর মাধ্যমে জানায় (non-blocking)।

### 🏠 বাস্তব জীবনের উদাহরণ

> **Sync:** রেস্তোরাঁয় এক গ্রাহকের order নেওয়া → রান্না → পরিবেশন → তারপর পরের গ্রাহক।
> **Async:** সব গ্রাহকের order নেওয়া → রান্না চলতে থাকুক → যার রান্না হয় তাকে পরিবেশন।

### 💻 Sync vs Async — Comparison

```javascript
// Synchronous — blocking
console.log("১");
console.log("২");          // ২ সবার আগে print হবে না
console.log("৩");
// Output: ১, ২, ৩ (order guaranteed)

// Asynchronous — non-blocking
console.log("শুরু");
setTimeout(() => console.log("Async কাজ"), 1000); // 1 second পরে
console.log("শেষ");
// Output: শুরু → শেষ → Async কাজ
// "শেষ" "Async কাজ"-এর আগে print হয়!

// JavaScript single-threaded কিন্তু async কাজ browser/Node API handle করে
// Event Loop async operations manage করে
```

---

## ৫.২ setTimeout ও setInterval

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 setTimeout

```javascript
// setTimeout — নির্দিষ্ট সময় পরে একবার চালায়
const timerId = setTimeout(function() {
  console.log("2 সেকেন্ড পরে!");
}, 2000);

// Cancel করা
clearTimeout(timerId);

// Arrow function + argument
setTimeout((name, city) => {
  console.log(`${name} থেকে ${city}`);
}, 1000, "Rahim", "Dhaka");

// 0ms delay — event loop-এর পরে চলে
setTimeout(() => console.log("Event loop পরে"), 0);
console.log("এটা আগে");
// Output: "এটা আগে" → "Event loop পরে"

// Recursive setTimeout (setInterval-এর alternative)
function repeatTask() {
  doWork();
  setTimeout(repeatTask, 1000); // কাজ শেষ হওয়ার পরে 1s
}
// setInterval-এর চেয়ে ভালো — কাজ শেষ হওয়ার পরে পরবর্তী schedule হয়
```

### 💻 setInterval

```javascript
// setInterval — নির্দিষ্ট সময় পরপর চালায়
let count = 0;
const intervalId = setInterval(() => {
  count++;
  console.log(`Count: ${count}`);
  if (count >= 5) {
    clearInterval(intervalId); // বন্ধ করা
  }
}, 1000);

// Clock example
function updateClock() {
  const now = new Date();
  document.querySelector("#clock").textContent =
    `${now.getHours()}:${now.getMinutes()}:${now.getSeconds()}`;
}
const clockInterval = setInterval(updateClock, 1000);
updateClock(); // প্রথমেই একবার চালানো

// ⚠️ setInterval vs setTimeout (recursive)
// setInterval: task start থেকে count — task দীর্ঘ হলে overlap সম্ভব
// setTimeout recursive: task শেষ থেকে count — overlap নেই
```

---

## ৫.৩ Callback Hell

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Callback Hell** (বা Pyramid of Doom) — multiple async operations যখন nested callbacks-এ লেখা হয়, code গভীর হতে থাকে এবং পড়া ও maintain করা কঠিন হয়।

```javascript
// ❌ Callback Hell — ধাপে ধাপে user data fetch
getUserId(function(userId) {
  getUser(userId, function(user) {
    getOrders(user.id, function(orders) {
      getOrderDetails(orders[0].id, function(details) {
        getShippingInfo(details.shippingId, function(shipping) {
          console.log(shipping);
          // আরও nested হতে পারে...
        }, function(err) { handleError(err); });
      }, function(err) { handleError(err); });
    }, function(err) { handleError(err); });
  }, function(err) { handleError(err); });
}, function(err) { handleError(err); });
// 😵 পড়া কঠিন, error handling repetitive, maintain nightmare

// ✅ Solution 1: Named functions (partial fix)
function onUserId(userId) { getUser(userId, onUser, handleError); }
function onUser(user) { getOrders(user.id, onOrders, handleError); }
function onOrders(orders) { getOrderDetails(orders[0].id, onDetails, handleError); }

// ✅ Solution 2: Promises (better)
getUserId()
  .then(userId => getUser(userId))
  .then(user => getOrders(user.id))
  .then(orders => getOrderDetails(orders[0].id))
  .then(details => getShippingInfo(details.shippingId))
  .then(shipping => console.log(shipping))
  .catch(handleError); // একটি error handler সবার জন্য!

// ✅ Solution 3: Async/Await (best)
async function getShipping() {
  try {
    const userId = await getUserId();
    const user = await getUser(userId);
    const orders = await getOrders(user.id);
    const details = await getOrderDetails(orders[0].id);
    const shipping = await getShippingInfo(details.shippingId);
    console.log(shipping);
  } catch (err) {
    handleError(err);
  }
}
```

---

## ৫.৪ Promise

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Promise** হলো async operation-এর eventual result represent করা object। তিনটি state:
- **Pending** — চলছে
- **Fulfilled** — সফল হয়েছে (resolve)
- **Rejected** — ব্যর্থ হয়েছে (reject)

### 💻 Promise তৈরি ও ব্যবহার

```javascript
// ১. Promise তৈরি
const myPromise = new Promise((resolve, reject) => {
  // Async কাজ করুন
  const success = true;
  if (success) {
    resolve("কাজ সফল হয়েছে!");  // fulfill
  } else {
    reject(new Error("কাজ ব্যর্থ হয়েছে!"));  // reject
  }
});

// ২. Promise consume
myPromise
  .then(result => console.log(result))     // "কাজ সফল হয়েছে!"
  .catch(error => console.error(error))    // rejection handle
  .finally(() => console.log("সর্বদা চলবে")); // সবসময়

// ৩. Practical: setTimeout-কে Promise-এ wrap
function delay(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

async function runAfterDelay() {
  console.log("শুরু");
  await delay(2000); // 2 সেকেন্ড wait
  console.log("2 সেকেন্ড পরে");
}

// ৪. API call Promise
function fetchUserData(id) {
  return new Promise((resolve, reject) => {
    fetch(`https://jsonplaceholder.typicode.com/users/${id}`)
      .then(response => {
        if (!response.ok) {
          reject(new Error(`HTTP Error: ${response.status}`));
          return;
        }
        return response.json();
      })
      .then(data => resolve(data))
      .catch(err => reject(err));
  });
}

// ৫. Promise states visualization
// Promise তৈরির সময়: pending
// resolve() call হলে: fulfilled → .then() চলে
// reject() call হলে: rejected → .catch() চলে
// একবার settled হলে আর state পরিবর্তন হয় না

// ৬. Promise.resolve / Promise.reject (shorthand)
Promise.resolve("immediate value").then(console.log); // "immediate value"
Promise.reject(new Error("immediate error")).catch(console.error);
```

---

## ৫.৫ Promise Chaining

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Chaining বিস্তারিত

```javascript
// প্রতিটি .then() একটি নতুন Promise return করে
fetch("/api/user/1")
  .then(response => {
    console.log("Response received");
    return response.json();           // json parsing — Promise return
  })
  .then(userData => {
    console.log("User:", userData.name);
    return fetch(`/api/posts?userId=${userData.id}`); // নতুন fetch
  })
  .then(response => response.json())
  .then(posts => {
    console.log("Posts count:", posts.length);
    return posts.filter(p => p.published);
  })
  .then(publishedPosts => {
    // আর কোনো async কাজ নেই
    renderPosts(publishedPosts);
  })
  .catch(error => {
    // যেকোনো step-এ error → এখানে আসবে
    console.error("কোথাও সমস্যা:", error.message);
  })
  .finally(() => {
    hideLoadingSpinner(); // সব সময় — success বা error
  });

// ⚠️ Common mistake: return না করা
fetch("/api/user")
  .then(response => {
    response.json(); // ❌ return নেই!
    // পরের .then() undefined পাবে
  })
  .then(data => console.log(data)); // undefined!

// ✅ সঠিক:
fetch("/api/user")
  .then(response => response.json()) // return implicit with arrow fn
  .then(data => console.log(data));  // data পাবে
```

---

## ৫.৬ Promise Combinators

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Promise.all

```javascript
// সব Promises একসাথে চালায়, সব fulfilled হলে resolve
const p1 = fetch("/api/users").then(r => r.json());
const p2 = fetch("/api/products").then(r => r.json());
const p3 = fetch("/api/orders").then(r => r.json());

try {
  const [users, products, orders] = await Promise.all([p1, p2, p3]);
  // তিনটি API call parallel-এ — সময় সাশ্রয়!
  console.log(users.length, products.length, orders.length);
} catch (error) {
  // যেকোনো একটি reject হলে সাথে সাথে reject (fail-fast)
  console.error("একটি request ব্যর্থ:", error.message);
}

// Sequential vs Parallel comparison:
// Sequential: 3 × 1s = 3s
const u = await fetch("/api/users").then(r => r.json());
const p = await fetch("/api/products").then(r => r.json());

// Parallel: max(1s, 1s, 1s) = 1s
const [u2, p2_] = await Promise.all([
  fetch("/api/users").then(r => r.json()),
  fetch("/api/products").then(r => r.json())
]);
```

### 💻 Promise.allSettled

```javascript
// সব Promises-এর result পায়, fail হলেও (ES2020)
const results = await Promise.allSettled([
  fetch("/api/critical").then(r => r.json()),
  fetch("/api/optional").then(r => r.json()), // এটি fail হলেও চলবে
  fetch("/api/extra").then(r => r.json())
]);

results.forEach(result => {
  if (result.status === "fulfilled") {
    console.log("সফল:", result.value);
  } else {
    console.log("ব্যর্থ:", result.reason.message);
  }
});
// কোনো reject হলেও সব results পাওয়া যায়
```

### 💻 Promise.race ও Promise.any

```javascript
// Promise.race — প্রথমটি settle হলে resolve/reject
const fastest = await Promise.race([
  fetch("/api/server-1").then(r => r.json()),
  fetch("/api/server-2").then(r => r.json()),
  new Promise((_, reject) => setTimeout(() => reject(new Error("Timeout")), 5000))
]);
// সবচেয়ে দ্রুত response বা timeout

// Promise.any — প্রথম fulfilled resolve করে (ES2021)
try {
  const result = await Promise.any([
    fetch("/api/cdn-1").then(r => r.json()), // ব্যর্থ হতে পারে
    fetch("/api/cdn-2").then(r => r.json()), // ব্যর্থ হতে পারে
    fetch("/api/cdn-3").then(r => r.json())  // এটি সফল হলেই হলো
  ]);
  // যেকোনো একটি সফল হলে result পাওয়া যায়
} catch (err) {
  // AggregateError — সবগুলো ব্যর্থ হলে
  console.error("সবগুলো ব্যর্থ");
}
```

### 📊 Promise Combinators তুলনা

| Method | কখন Resolve | কখন Reject | Use Case |
|--------|------------|-----------|----------|
| `Promise.all` | সব fulfilled | যেকোনো একটি reject | সব দরকার |
| `Promise.allSettled` | সব settle | কখনো না | সব results দরকার |
| `Promise.race` | প্রথমটি settle | প্রথমটি reject | Fastest wins |
| `Promise.any` | প্রথম fulfilled | সব reject (AggregateError) | যেকোনো একটি হলেই |

---

## ৫.৭ Async/Await

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Async/Await** — ES2017। Promise-এর syntactic sugar — async code-কে synchronous-এর মতো লেখা যায়। `async function` সবসময় Promise return করে।

### 💻 Async/Await বিস্তারিত

```javascript
// ১. Basic async/await
async function getUserData(id) {
  const response = await fetch(`/api/users/${id}`); // Promise-এর জন্য wait
  const data = await response.json();               // JSON parsing wait
  return data; // automatically Promise.resolve(data)-তে wrap হয়
}

// Call করা
getUserData(1).then(data => console.log(data));
// অথবা:
const data = await getUserData(1); // async context-এ

// ২. async function সবসময় Promise return করে
async function getValue() {
  return 42;
}
getValue() instanceof Promise; // true
getValue().then(v => console.log(v)); // 42

// ৩. Await একটি expression
async function example() {
  const num = await Promise.resolve(10);  // 10
  const str = await "hello";              // "hello" (non-Promise, wrap হয়)
  const doubled = await (num * 2);        // 20

  // Inline calculation
  const result = await fetch("/api")
    .then(r => r.json())
    .then(d => d.value * 2);

  return result;
}

// ৪. Sequential vs Parallel in async/await
// Sequential (ধীর)
async function sequential() {
  const user = await fetchUser();       // wait করে
  const posts = await fetchPosts();     // তারপর wait
  // মোট: user time + posts time
}

// Parallel (দ্রুত)
async function parallel() {
  const [user, posts] = await Promise.all([
    fetchUser(),   // একসাথে শুরু
    fetchPosts()   // একসাথে শুরু
  ]);
  // মোট: max(user time, posts time)
}

// ৫. Await in loops
async function processItems(ids) {
  // ❌ Sequential (each awaits previous)
  for (const id of ids) {
    const item = await fetchItem(id);
    processItem(item);
  }

  // ✅ Parallel
  const items = await Promise.all(ids.map(id => fetchItem(id)));
  items.forEach(processItem);
}

// ৬. Top-level await (ES2022, ES Modules)
// const data = await fetch("/api").then(r => r.json());
// browser modules এবং Node.js-এ সরাসরি ব্যবহার করা যায়
```

---

## ৫.৮ Error Handling

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 try/catch/finally with Async/Await

```javascript
async function fetchUserProfile(userId) {
  try {
    const response = await fetch(`/api/users/${userId}`);

    if (!response.ok) {
      throw new Error(`HTTP Error: ${response.status} ${response.statusText}`);
    }

    const user = await response.json();
    return user;

  } catch (error) {
    if (error.name === "TypeError") {
      // Network error (offline, DNS failure)
      console.error("Network error:", error.message);
    } else if (error.message.includes("HTTP Error")) {
      // HTTP error (404, 500 etc.)
      console.error("Server error:", error.message);
    } else {
      // Other errors (JSON parse, etc.)
      console.error("Unexpected error:", error.message);
    }
    throw error; // re-throw — caller-ও জানুক
  } finally {
    hideLoadingSpinner(); // সবসময় চলে
  }
}

// ২. Custom Error classes
class ApiError extends Error {
  constructor(message, statusCode, endpoint) {
    super(message);
    this.name = "ApiError";
    this.statusCode = statusCode;
    this.endpoint = endpoint;
  }
}

class ValidationError extends Error {
  constructor(message, fields) {
    super(message);
    this.name = "ValidationError";
    this.fields = fields;
  }
}

// throw করা
throw new ApiError("Not Found", 404, "/api/users/999");
throw new ValidationError("Invalid form", { email: "সঠিক ইমেইল দিন" });

// ধরা
try {
  await fetchUserProfile(999);
} catch (error) {
  if (error instanceof ApiError) {
    if (error.statusCode === 404) showNotFound();
    if (error.statusCode === 401) redirectToLogin();
  } else if (error instanceof ValidationError) {
    showFieldErrors(error.fields);
  } else {
    showGenericError();
  }
}

// ৩. Unhandled Promise rejection catch
window.addEventListener("unhandledrejection", (event) => {
  console.error("Unhandled rejection:", event.reason);
  event.preventDefault(); // browser error থামানো
});

// Node.js-এ
process.on("unhandledRejection", (reason, promise) => {
  console.error("Unhandled rejection:", reason);
});

// ৪. Safe async wrapper — every call-এ try/catch না লিখতে
async function safeAsync(fn, ...args) {
  try {
    const result = await fn(...args);
    return [result, null];
  } catch (error) {
    return [null, error];
  }
}

const [user, error] = await safeAsync(fetchUserProfile, 1);
if (error) {
  handleError(error);
} else {
  renderUser(user);
}
```

---

## ৫.৯ Real API Calls

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Fetch API — Complete Guide

```javascript
// ১. GET request
async function getUsers() {
  const response = await fetch("https://jsonplaceholder.typicode.com/users");
  if (!response.ok) throw new Error(`Error: ${response.status}`);
  return response.json();
}

// ২. POST request
async function createUser(userData) {
  const response = await fetch("https://jsonplaceholder.typicode.com/users", {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
      "Authorization": `Bearer ${getToken()}`
    },
    body: JSON.stringify(userData)
  });
  if (!response.ok) throw new Error(`Error: ${response.status}`);
  return response.json();
}

// ৩. PUT / PATCH
async function updateUser(id, changes) {
  const response = await fetch(`/api/users/${id}`, {
    method: "PATCH", // PATCH: partial update, PUT: full replace
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify(changes)
  });
  return response.json();
}

// ৪. DELETE
async function deleteUser(id) {
  const response = await fetch(`/api/users/${id}`, { method: "DELETE" });
  return response.ok;
}

// ৫. API Service class
class ApiService {
  constructor(baseUrl, token = null) {
    this.baseUrl = baseUrl;
    this.token = token;
  }

  getHeaders(extra = {}) {
    const headers = { "Content-Type": "application/json", ...extra };
    if (this.token) headers["Authorization"] = `Bearer ${this.token}`;
    return headers;
  }

  async request(endpoint, options = {}) {
    const url = `${this.baseUrl}${endpoint}`;
    const config = { headers: this.getHeaders(), ...options };

    const response = await fetch(url, config);

    if (response.status === 401) {
      this.token = await refreshToken();
      return this.request(endpoint, options); // retry
    }

    if (!response.ok) {
      const errorData = await response.json().catch(() => ({}));
      throw new ApiError(
        errorData.message || `HTTP ${response.status}`,
        response.status,
        endpoint
      );
    }

    if (response.status === 204) return null; // No content
    return response.json();
  }

  get(endpoint) { return this.request(endpoint); }
  post(endpoint, data) {
    return this.request(endpoint, { method: "POST", body: JSON.stringify(data) });
  }
  patch(endpoint, data) {
    return this.request(endpoint, { method: "PATCH", body: JSON.stringify(data) });
  }
  delete(endpoint) { return this.request(endpoint, { method: "DELETE" }); }
}

const api = new ApiService("https://api.example.com", userToken);
const users = await api.get("/users");
const newUser = await api.post("/users", { name: "Rahim", email: "rahim@bd.com" });
```

---

## ৫.১০ AbortController

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Request Cancel করা

```javascript
// ১. Basic AbortController
const controller = new AbortController();
const signal = controller.signal;

// Fetch request চালু
const fetchPromise = fetch("/api/large-data", { signal });

// 5 সেকেন্ড পরে cancel
const timeoutId = setTimeout(() => controller.abort(), 5000);

try {
  const response = await fetchPromise;
  clearTimeout(timeoutId);
  return response.json();
} catch (error) {
  if (error.name === "AbortError") {
    console.log("Request cancelled");
  } else {
    throw error;
  }
}

// ২. Practical: Search input — debounce + cancel
let searchController = null;

async function searchUsers(query) {
  // আগের request cancel
  if (searchController) searchController.abort();
  searchController = new AbortController();

  try {
    const response = await fetch(`/api/search?q=${query}`, {
      signal: searchController.signal
    });
    const results = await response.json();
    displayResults(results);
  } catch (error) {
    if (error.name !== "AbortError") {
      showError(error.message);
    }
  }
}

document.querySelector("#search").addEventListener("input", (e) => {
  searchUsers(e.target.value);
});

// ৩. Timeout utility
async function fetchWithTimeout(url, timeout = 5000) {
  const controller = new AbortController();
  const id = setTimeout(() => controller.abort(), timeout);
  try {
    const response = await fetch(url, { signal: controller.signal });
    clearTimeout(id);
    return response;
  } catch (error) {
    if (error.name === "AbortError") throw new Error("Request timeout");
    throw error;
  }
}
```

---

## ৫.১১ PART 5 — Interview Questions & Answers

<div align="right"><a href="#part5">⬆ PART 5 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

<details>
<summary><strong>🔹 Core Async Concepts (Q1–Q12)</strong></summary>
<br>

**Q1: JavaScript কি সত্যিই single-threaded? তাহলে async কীভাবে কাজ করে?**
> **A:** হ্যাঁ, JavaScript single-threaded — একসময়ে একটি কাজ। কিন্তু browser/Node.js-এর Web APIs (fetch, setTimeout, DOM events) আলাদা thread-এ কাজ করে। শেষ হলে callback queue-তে রাখে। Event Loop call stack খালি হলে সেই callback তুলে চালায়। তাই JS non-blocking async কাজ করতে পারে।

**Q2: Callback, Promise, এবং Async/Await-এর পার্থক্য?**
> **A:** Callback: function argument হিসেবে — callback hell, error handling কঠিন। Promise: chainable `.then()/.catch()` — আরও পরিষ্কার, central error handling। Async/Await: Promise-এর syntactic sugar — synchronous-এর মতো লেখা, সবচেয়ে readable। সব তিনটিই async handle করে, শুধু syntax আলাদা।

**Q3: Promise-এর তিনটি state কী?**
> **A:** ১. **Pending** — শুরু হয়েছে, এখনো শেষ হয়নি। ২. **Fulfilled** — সফল (`resolve()` call হয়েছে)। ৩. **Rejected** — ব্যর্থ (`reject()` call হয়েছে)। Fulfilled/Rejected = Settled। একবার settle হলে আর state পরিবর্তন হয় না।

**Q4: async function সবসময় কী return করে?**
> **A:** সবসময় **Promise** return করে। `return 42` করলে `Promise.resolve(42)`, exception throw করলে `Promise.reject(error)`। `await asyncFn()` দিয়ে unwrap করা যায়।

**Q5: Promise.all এবং Promise.allSettled-এর পার্থক্য?**
> **A:** `Promise.all` — যেকোনো একটি reject হলে সাথে সাথে reject (fail-fast)। `Promise.allSettled` — সব settle হওয়া পর্যন্ত wait, প্রতিটির `{status, value/reason}` দেয়। কিছু optional হলে বা সব results দরকার হলে `allSettled`।

**Q6: await ছাড়া async function call করলে কী হয়?**
> **A:** Promise return করে, resolve হওয়া value পাওয়া যায় না। `const data = fetchData()` — data হলো Promise object, actual data নয়। `.then()` বা `await` দিয়ে unwrap করতে হবে।

**Q7: Microtask queue কী? Callback queue থেকে পার্থক্য?**
> **A:** Microtask queue (Promise callbacks, `queueMicrotask`) Callback queue-এর চেয়ে **বেশি priority** পায়। Event loop: call stack খালি → microtask queue সম্পূর্ণ খালি → তারপর callback queue থেকে একটি। তাই Promise `.then()` setTimeout-এর আগে চলে।

**Q8: try/catch কি Async/Await error ধরতে পারে?**
> **A:** হ্যাঁ — `await` expression-এ try/catch সরাসরি কাজ করে। `await`-এ rejected Promise হলে exception throw হয়। `.catch()` ছাড়া Promise chain-এ `.catch()` বা outer try/catch দরকার।

**Q9: `setTimeout(fn, 0)` — কী করে?**
> **A:** 0ms delay মানে সাথে সাথে নয় — call stack খালি হওয়ার পরে, callback queue থেকে। Synchronous code সব শেষ হওয়ার পরে চলে। Use case: expensive computation-কে defer করা, DOM update হতে দেওয়া তারপর কাজ করা।

**Q10: setInterval এবং recursive setTimeout-এর পার্থক্য কী?**
> **A:** `setInterval` — কাজ শুরু থেকে interval count। কাজ 1.5s নিলেও 1s পরে পরের কাজ শুরু — overlap সম্ভব। Recursive `setTimeout` — কাজ শেষ হওয়ার পরে পরের timer শুরু — overlap নেই, consistent gap। Long-running tasks-এ setTimeout recursive পছন্দনীয়।

**Q11: AbortController কেন দরকার?**
> **A:** Component unmount হলে বা user নতুন search করলে পুরনো pending request cancel করা। Memory leak এবং stale data রোধ করে। Timeout implement করতে (`abort()` নির্দিষ্ট সময় পরে)।

**Q12: Promise chaining-এ `return` না করলে কী হয়?**
> **A:** পরের `.then()` `undefined` পায়। `.then()` implicitly `Promise.resolve(undefined)` return করে। সবসময় `.then()` callback-এ value `return` করতে হবে পরের chain-এ পাঠাতে হলে।

</details>

<details>
<summary><strong>🔹 Practical & Tricky (Q13–Q20)</strong></summary>
<br>

**Q13: নিচের code-এর output কী?**
```javascript
console.log("A");
setTimeout(() => console.log("B"), 0);
Promise.resolve().then(() => console.log("C"));
console.log("D");
```
> **A:** `A → D → C → B`। A, D synchronous (call stack)। C Promise microtask (call stack খালির পরে, macrotask আগে)। B setTimeout macrotask (সবার শেষে)।

**Q14: API call-এ loading/error state কীভাবে manage করবেন?**
> **A:**
```javascript
async function fetchWithState(url) {
  setLoading(true);
  setError(null);
  try {
    const res = await fetch(url);
    if (!res.ok) throw new Error(`HTTP ${res.status}`);
    const data = await res.json();
    setData(data);
  } catch (err) {
    setError(err.message);
  } finally {
    setLoading(false); // সবসময় loading বন্ধ
  }
}
```

**Q15: Parallel API calls-এ একটি fail করলেও বাকিগুলোর result রাখতে চাই — কীভাবে?**
> **A:** `Promise.allSettled()` ব্যবহার করুন। প্রতিটি result-এর `status === "fulfilled"` check করে value নিন, `"rejected"` হলে fallback।

**Q16: async/await কি synchronous কোডের মতো? Block করে?**
> **A:** না। `await` শুধু সেই async function-কে pause করে — call stack block করে না। অন্য code, event handler, timer চলতে পারে। `await` হলো non-blocking pause।

**Q17: Fetch API কি সব HTTP error (404, 500)-এ reject করে?**
> **A:** না — fetch শুধু network failure-এ reject করে। HTTP 404, 500 — fulfilled হয় (response পাওয়া যায়)। তাই `response.ok` বা `response.status` check করতে হয়।

**Q18: Promise constructor-এ synchronous কোড থাকলে কখন চলে?**
> **A:** সাথে সাথে, synchronously। `new Promise((resolve, reject) => { /* এখানে sync code */ })` — executor তাৎক্ষণিক চলে। শুধু `.then()` callback asynchronous।

**Q19: `async function` ছাড়া top-level `await` কাজ করে কি?**
> **A:** ES modules (`.mjs` বা `type="module"` script)-এ top-level await কাজ করে (ES2022)। Regular scripts-এ async function-এর ভেতরে থাকতে হবে।

**Q20: একটি Promise কি দুইবার resolve করা যায়?**
> **A:** না। একবার resolve বা reject হলে state স্থায়ী। পরবর্তী `resolve()` বা `reject()` call ignored। এই "immutability" Promise-এর গুরুত্বপূর্ণ property।

</details>

---

<div align="right">
  <a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a>
</div>

---

> **🚀 PART 6 আসছে:** Object-Oriented JavaScript — Objects, Constructor Functions, Prototypes, Classes, Encapsulation, Inheritance, Polymorphism, Abstraction, SOLID Principles।
>
> **💬 পরবর্তী PART পেতে:** "PART 6 দাও" লিখুন।


---

<a id="part6"></a>

# PART 6 — Object-Oriented JavaScript

> **📍 এই PART-এর Sections:** [৬.১ Objects](#৬১-objects) · [৬.২ Constructor Functions](#৬২-constructor-functions) · [৬.৩ Prototype](#৬৩-prototype) · [৬.৪ Prototype Chain](#৬৪-prototype-chain) · [৬.৫ ES6 Classes](#৬৫-es6-classes) · [৬.৬ Encapsulation](#৬৬-encapsulation) · [৬.৭ Inheritance](#৬৭-inheritance) · [৬.৮ Polymorphism](#৬৮-polymorphism) · [৬.৯ Abstraction](#৬৯-abstraction) · [৬.১০ SOLID Principles](#৬১০-solid-principles-in-javascript) · [৬.১১ Interview Q&A](#৬১১-part-6--interview-questions--answers)

---

## ৬.১ Objects

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

JavaScript-এ **Object** হলো key-value pairs-এর collection। Function সহ যেকোনো কিছু object হতে পারে। JS-এ প্রায় সব কিছুই (Array, Function, Date) আসলে object।

### 💻 Object তৈরির পদ্ধতি

```javascript
// ১. Object Literal (সবচেয়ে সাধারণ)
const person = {
  name: "Rahim",
  age: 25,
  city: "Dhaka",
  greet() {
    return `আমি ${this.name}, ${this.city} থেকে`;
  }
};

// ২. Object.create()
const personProto = {
  greet() { return `Hello, I am ${this.name}`; }
};
const john = Object.create(personProto);
john.name = "John";
console.log(john.greet()); // "Hello, I am John"

// ৩. Constructor Function (৬.২-এ বিস্তারিত)
function Person(name, age) {
  this.name = name;
  this.age = age;
}
const p = new Person("Rahim", 25);

// ৪. Class (৬.৫-এ বিস্তারিত)
class Animal { constructor(name) { this.name = name; } }

// Object properties
const car = {
  brand: "Toyota",
  model: "Corolla",
  year: 2022,
  isRunning: false,
  start() { this.isRunning = true; console.log("Started!"); },
  stop() { this.isRunning = false; console.log("Stopped!"); }
};

// Property access
console.log(car.brand);         // dot notation
console.log(car["model"]);      // bracket notation (dynamic key-এ দরকার)
const key = "year";
console.log(car[key]);          // dynamic key — bracket required

// Property check
"brand" in car;                 // true (prototype-ও check করে)
car.hasOwnProperty("brand");    // true (own property শুধু)
Object.hasOwn(car, "brand");    // true (modern, ES2022)

// Property enumerate
Object.keys(car);               // ["brand", "model", "year", "isRunning", "start", "stop"]
Object.values(car);
Object.entries(car);

// Property descriptor
Object.defineProperty(car, "id", {
  value: "CAR-001",
  writable: false,    // পরিবর্তন করা যাবে না
  enumerable: false,  // Object.keys-এ আসবে না
  configurable: false // delete করা যাবে না
});
```

---

## ৬.২ Constructor Functions

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Constructor Function** হলো `new` keyword দিয়ে object তৈরির function। ES6 Classes-এর আগের পদ্ধতি। এখনো জানা দরকার কারণ JS-এর prototype-ভিত্তিক inheritance বোঝার জন্য।

### 💻 Constructor Function বিস্তারিত

```javascript
// Convention: PascalCase নাম
function Person(name, age, city) {
  // new দিয়ে call করলে:
  // ১. নতুন empty object তৈরি হয়
  // ২. this সেই object-কে point করে
  // ৩. Person.prototype লিংক হয়
  // ৪. object return হয় (implicit)

  this.name = name;
  this.age = age;
  this.city = city;
  // ❌ Method এখানে রাখলে প্রতিটি instance-এ copy হয় (memory waste)
}

// Methods prototype-এ রাখুন — সব instances share করে
Person.prototype.greet = function() {
  return `আমি ${this.name}, ${this.age} বছর, ${this.city}`;
};

Person.prototype.birthday = function() {
  this.age++;
  return `${this.name}-এর বয়স এখন ${this.age}`;
};

// Static method
Person.create = function(name, age) {
  return new Person(name, age, "Unknown");
};

// Instance তৈরি
const rahim = new Person("Rahim", 25, "Dhaka");
const karim = new Person("Karim", 30, "Chittagong");

console.log(rahim.greet()); // "আমি Rahim, 25 বছর, Dhaka"
console.log(rahim instanceof Person); // true

// ⚠️ new ছাড়া call করলে this = global (বা undefined strict mode-এ)
const wrong = Person("Oops", 20, "X"); // this হবে window/global!

// Guard against missing new:
function SafePerson(name) {
  if (!(this instanceof SafePerson)) {
    return new SafePerson(name);
  }
  this.name = name;
}
```

### 💻 `new` keyword কী করে?

```javascript
// new Person("Rahim", 25) এর equivalent:
function myNew(Constructor, ...args) {
  // ১. নতুন object তৈরি — prototype link
  const obj = Object.create(Constructor.prototype);
  // ২. Constructor চালানো — this = obj
  const result = Constructor.apply(obj, args);
  // ৩. Constructor object return করলে সেটা, নইলে obj
  return result instanceof Object ? result : obj;
}

const p = myNew(Person, "Rahim", 25, "Dhaka");
console.log(p.greet()); // কাজ করবে!
```

---

## ৬.৩ Prototype

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

JavaScript-এ প্রতিটি object-এর একটি **prototype** আছে — এটি আরেকটি object যা থেকে properties ও methods inherit করা হয়। এটিই JS-এর inheritance-এর মূল mechanism।

### 💻 Prototype বিস্তারিত

```javascript
function Animal(name) {
  this.name = name;
}
Animal.prototype.speak = function() {
  return `${this.name} makes a sound`;
};
Animal.prototype.type = "Animal";

const dog = new Animal("Rex");

// Prototype chain
console.log(dog.__proto__ === Animal.prototype); // true
console.log(Animal.prototype.__proto__ === Object.prototype); // true
console.log(Object.prototype.__proto__); // null (chain শেষ)

// Property lookup
dog.speak();   // dog নিজে নেই → Animal.prototype-এ খোঁজে → পায়
dog.toString(); // নিজে নেই → Animal.prototype-এ নেই → Object.prototype-এ পায়

// hasOwnProperty
console.log(dog.hasOwnProperty("name"));  // true (own)
console.log(dog.hasOwnProperty("speak")); // false (prototype-এ)

// Prototype-এ method যোগ করা (existing objects-এও কাজ করে)
Animal.prototype.breathe = function() {
  return `${this.name} is breathing`;
};
console.log(dog.breathe()); // কাজ করবে — dog তৈরির পরেও!

// Built-in prototypes extend (⚠️ Production-এ করবেন না)
Array.prototype.sum = function() {
  return this.reduce((acc, n) => acc + n, 0);
};
[1, 2, 3].sum(); // 6 — কিন্তু এটি bad practice!

// Object.getPrototypeOf — modern way
console.log(Object.getPrototypeOf(dog) === Animal.prototype); // true
```

---

## ৬.৪ Prototype Chain

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 💻 Chain visualization

```
dog (instance)
  └── __proto__ → Animal.prototype
                  ├── speak()
                  ├── type: "Animal"
                  └── __proto__ → Object.prototype
                                  ├── toString()
                                  ├── hasOwnProperty()
                                  ├── valueOf()
                                  └── __proto__ → null (chain শেষ)

Property lookup: dog.speak()
  1. dog নিজে "speak" আছে? → না
  2. Animal.prototype-এ আছে? → হ্যাঁ → পাওয়া গেছে ✓

Property lookup: dog.toString()
  1. dog নিজে? → না
  2. Animal.prototype-এ? → না
  3. Object.prototype-এ? → হ্যাঁ → পাওয়া গেছে ✓

Property lookup: dog.nonExistent
  1. dog? → না  2. Animal.prototype? → না  3. Object.prototype? → না
  4. null → undefined return
```

### 💻 Prototype Chain Inheritance (Pre-Class)

```javascript
// Animal → Dog → GoldenRetriever

function Animal(name) {
  this.name = name;
}
Animal.prototype.eat = function() { return `${this.name} is eating`; };

function Dog(name, breed) {
  Animal.call(this, name); // parent constructor call
  this.breed = breed;
}
// Prototype chain সেটআপ
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog; // constructor fix

Dog.prototype.bark = function() { return `${this.name}: Woof!`; };

const rex = new Dog("Rex", "Labrador");
console.log(rex.eat());  // "Rex is eating" (Animal থেকে)
console.log(rex.bark()); // "Rex: Woof!" (Dog থেকে)
console.log(rex instanceof Dog);    // true
console.log(rex instanceof Animal); // true
```

---

## ৬.৫ ES6 Classes

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

ES6 **Class** হলো prototype-based inheritance-এর **syntactic sugar** — ভেতরে কিন্তু prototype-ই ব্যবহার হয়। Code আরও পরিষ্কার ও readable।

### 💻 Class সম্পূর্ণ Features

```javascript
class Animal {
  // Class field (ES2022)
  #sound = "..."; // private field
  static count = 0; // static field

  constructor(name, age) {
    this.name = name;
    this.age = age;
    Animal.count++;
  }

  // Instance method
  speak() {
    return `${this.name} says ${this.#sound}`;
  }

  // Getter
  get info() {
    return `${this.name} (${this.age} বছর)`;
  }

  // Setter
  set info(value) {
    [this.name, this.age] = value.split(",");
  }

  // Static method — instance ছাড়া call করা যায়
  static create(name) {
    return new Animal(name, 0);
  }

  static getCount() {
    return `মোট ${Animal.count}টি animal তৈরি হয়েছে`;
  }

  // toString override
  toString() {
    return `Animal(${this.name})`;
  }
}

const cat = new Animal("Tom", 3);
console.log(cat.speak());          // "Tom says ..."
console.log(cat.info);             // "Tom (3 বছর)"
cat.info = "Jerry,2";
console.log(cat.name, cat.age);    // "Jerry" "2"
console.log(Animal.count);         // 1
console.log(Animal.getCount());    // "মোট 1টি animal তৈরি হয়েছে"
console.log(Animal.create("Max")); // Animal { name: "Max", age: 0 }

// Class expression
const MyClass = class {
  constructor(val) { this.val = val; }
};
```

---

## ৬.৬ Encapsulation

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Encapsulation** — data এবং methods একসাথে রাখা এবং internal implementation বাইরে থেকে লুকানো। শুধু প্রয়োজনীয় interface বাইরে expose করা।

### 💻 Private Fields ও Methods

```javascript
class BankAccount {
  // Private fields — # prefix
  #balance;
  #owner;
  #transactions = [];

  constructor(owner, initialBalance) {
    this.#owner = owner;
    this.#balance = initialBalance;
    this.#log("Account created", initialBalance);
  }

  // Private method
  #log(action, amount) {
    this.#transactions.push({
      action,
      amount,
      date: new Date().toISOString(),
      balance: this.#balance
    });
  }

  // Public interface
  deposit(amount) {
    if (amount <= 0) throw new Error("Deposit must be positive");
    this.#balance += amount;
    this.#log("Deposit", amount);
    return this;
  }

  withdraw(amount) {
    if (amount <= 0) throw new Error("Amount must be positive");
    if (amount > this.#balance) throw new Error("Insufficient funds");
    this.#balance -= amount;
    this.#log("Withdrawal", amount);
    return this;
  }

  get balance() { return this.#balance; } // read-only
  get owner() { return this.#owner; }

  getStatement() {
    return this.#transactions.map(t =>
      `${t.date}: ${t.action} ${t.amount} → Balance: ${t.balance}`
    ).join("
");
  }
}

const account = new BankAccount("Rahim", 10000);
account.deposit(5000).withdraw(2000); // chaining

console.log(account.balance); // 13000
// account.#balance = 99999;  // SyntaxError! Private field
console.log(account.getStatement());
```

---

## ৬.৭ Inheritance

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Inheritance** — parent class-এর properties ও methods child class-এ পাওয়া। `extends` এবং `super` keyword ব্যবহার করা হয়।

### 💻 Class Inheritance

```javascript
class Shape {
  #color;

  constructor(color) {
    this.#color = color;
  }

  get color() { return this.#color; }

  area() {
    throw new Error("area() অবশ্যই implement করতে হবে");
  }

  toString() {
    return `${this.constructor.name} [color: ${this.#color}, area: ${this.area()}]`;
  }
}

class Circle extends Shape {
  #radius;

  constructor(radius, color) {
    super(color); // parent constructor — প্রথমে call করতে হবে
    this.#radius = radius;
  }

  get radius() { return this.#radius; }

  area() {
    return Math.PI * this.#radius ** 2;
  }

  circumference() {
    return 2 * Math.PI * this.#radius;
  }
}

class Rectangle extends Shape {
  #width;
  #height;

  constructor(width, height, color) {
    super(color);
    this.#width = width;
    this.#height = height;
  }

  area() {
    return this.#width * this.#height;
  }

  perimeter() {
    return 2 * (this.#width + this.#height);
  }
}

class Square extends Rectangle {
  constructor(side, color) {
    super(side, side, color); // Rectangle-এর constructor
  }
}

const c = new Circle(5, "red");
const r = new Rectangle(4, 6, "blue");
const s = new Square(4, "green");

console.log(c.area());        // 78.539...
console.log(c.toString());    // "Circle [color: red, area: 78.539...]"
console.log(r.perimeter());   // 20
console.log(s.area());        // 16

console.log(c instanceof Circle);    // true
console.log(c instanceof Shape);     // true
console.log(s instanceof Square);    // true
console.log(s instanceof Rectangle); // true
console.log(s instanceof Shape);     // true

// super — method call
class Animal {
  speak() { return `${this.name} makes a sound`; }
}

class Dog extends Animal {
  speak() {
    const base = super.speak(); // parent method call
    return `${base} — specifically: Woof!`;
  }
}

const d = new Dog();
d.name = "Rex";
console.log(d.speak()); // "Rex makes a sound — specifically: Woof!"
```

---

## ৬.৮ Polymorphism

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Polymorphism** — একই interface (method name) different classes-এ different আচরণ করা। Method overriding-এর মাধ্যমে implement হয়।

### 💻 Polymorphism in Practice

```javascript
class Notification {
  constructor(message, recipient) {
    this.message = message;
    this.recipient = recipient;
  }

  // Template method — subclass override করবে
  send() {
    throw new Error("send() implement করতে হবে");
  }

  // Common logic
  validate() {
    if (!this.message) throw new Error("Message খালি হতে পারবে না");
    if (!this.recipient) throw new Error("Recipient দরকার");
    return true;
  }
}

class EmailNotification extends Notification {
  send() {
    this.validate();
    console.log(`Email → ${this.recipient}: "${this.message}"`);
    return { type: "email", status: "sent" };
  }
}

class SMSNotification extends Notification {
  send() {
    this.validate();
    console.log(`SMS → ${this.recipient}: "${this.message}"`);
    return { type: "sms", status: "sent" };
  }
}

class PushNotification extends Notification {
  send() {
    this.validate();
    console.log(`Push → Device ${this.recipient}: "${this.message}"`);
    return { type: "push", status: "sent" };
  }
}

// Polymorphic usage — same interface, different behavior
const notifications = [
  new EmailNotification("Welcome!", "rahim@bd.com"),
  new SMSNotification("OTP: 123456", "01712345678"),
  new PushNotification("নতুন message এসেছে", "device-token-abc")
];

// প্রতিটি আলাদাভাবে জানি না, সবাই .send() বলি
const results = notifications.map(n => n.send());
// সবার আলাদা আচরণ কিন্তু একই call

// ব্যবহারিক সুবিধা: নতুন notification type যোগ করতে
// শুধু নতুন class তৈরি করলেই হবে, এই loop পরিবর্তন লাগবে না
```

---

## ৬.৯ Abstraction

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 সংজ্ঞা

**Abstraction** — complexity লুকিয়ে শুধু প্রয়োজনীয় details দেখানো। User জানে "কী করে" কিন্তু "কীভাবে করে" জানার দরকার নেই।

### 💻 Abstraction — Abstract Class Pattern

```javascript
// JS-এ native abstract class নেই, pattern দিয়ে implement করি
class Database {
  constructor() {
    if (new.target === Database) {
      throw new Error("Database abstract class — directly instantiate করা যাবে না");
    }
  }

  // Abstract methods
  connect() { throw new Error("connect() implement করতে হবে"); }
  disconnect() { throw new Error("disconnect() implement করতে হবে"); }
  query(sql) { throw new Error("query() implement করতে হবে"); }

  // Concrete method (shared logic)
  async execute(sql) {
    await this.connect();
    try {
      return await this.query(sql);
    } finally {
      await this.disconnect();
    }
  }
}

class MySQLDatabase extends Database {
  constructor(config) {
    super();
    this.config = config;
    this.connection = null;
  }

  async connect() {
    this.connection = await createMySQLConnection(this.config);
    console.log("MySQL connected");
  }

  async disconnect() {
    await this.connection?.close();
    console.log("MySQL disconnected");
  }

  async query(sql) {
    return this.connection.execute(sql);
  }
}

class MongoDatabase extends Database {
  async connect() { /* MongoDB connection */ }
  async disconnect() { /* MongoDB disconnect */ }
  async query(query) { /* MongoDB query */ }
}

// Abstraction in use — user শুধু execute() জানে
const db = new MySQLDatabase({ host: "localhost", db: "myapp" });
const users = await db.execute("SELECT * FROM users");
// connect/disconnect details লুকানো

// new Database(); // Error: abstract class!
```

---

## ৬.১০ SOLID Principles in JavaScript

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

### 📖 SOLID কী?

| Letter | Principle |
|--------|-----------|
| **S** | Single Responsibility |
| **O** | Open/Closed |
| **L** | Liskov Substitution |
| **I** | Interface Segregation |
| **D** | Dependency Inversion |

### 💻 S — Single Responsibility Principle

```javascript
// ❌ এক class অনেক কাজ করছে
class UserManager {
  createUser(data) { /* DB save */ }
  validateUser(data) { /* validation */ }
  sendWelcomeEmail(user) { /* email */ }
  generateReport(users) { /* report */ }
  logActivity(action) { /* logging */ }
}

// ✅ প্রতিটি class একটি কাজ
class UserRepository {
  async create(data) { /* DB save */ }
  async findById(id) { /* DB query */ }
}

class UserValidator {
  validate(data) { /* validation logic */ }
}

class EmailService {
  sendWelcome(user) { /* email */ }
}

class UserService {
  constructor(repo, validator, emailService) {
    this.repo = repo;
    this.validator = validator;
    this.emailService = emailService;
  }

  async registerUser(data) {
    this.validator.validate(data);
    const user = await this.repo.create(data);
    this.emailService.sendWelcome(user);
    return user;
  }
}
```

### 💻 O — Open/Closed Principle

```javascript
// ❌ নতুন payment type যোগ করতে এই class পরিবর্তন লাগে
class PaymentProcessor {
  process(type, amount) {
    if (type === "credit") { /* credit */ }
    else if (type === "paypal") { /* paypal */ }
    else if (type === "bkash") { /* bkash */ } // নতুন যোগ করতে class পরিবর্তন!
  }
}

// ✅ Extension-এর জন্য open, modification-এর জন্য closed
class PaymentMethod {
  process(amount) { throw new Error("implement করুন"); }
}

class CreditCardPayment extends PaymentMethod {
  process(amount) { console.log(`Credit card: ${amount}`); }
}

class BkashPayment extends PaymentMethod {
  process(amount) { console.log(`bKash: ${amount}`); }
}

class PaymentProcessor2 {
  process(paymentMethod, amount) {
    paymentMethod.process(amount); // নতুন type = শুধু নতুন class
  }
}
// NagadPayment যোগ করতে PaymentProcessor2 পরিবর্তন লাগবে না!
```

### 💻 L — Liskov Substitution Principle

```javascript
// Parent যেখানে কাজ করে, child সেখানেও কাজ করতে হবে
class Bird {
  fly() { return `${this.name} is flying`; }
}

// ❌ Penguin fly করতে পারে না — LSP violation
class Penguin extends Bird {
  fly() { throw new Error("Penguins cannot fly!"); }
}

// ✅ Better design
class Bird2 {
  move() { return `${this.name} is moving`; }
}
class FlyingBird extends Bird2 {
  fly() { return `${this.name} is flying`; }
}
class SwimmingBird extends Bird2 {
  swim() { return `${this.name} is swimming`; }
}
class Eagle extends FlyingBird { }
class Penguin2 extends SwimmingBird { }
```

### 💻 D — Dependency Inversion Principle

```javascript
// ❌ High-level module directly depends on low-level
class OrderService {
  constructor() {
    this.db = new MySQLDatabase(); // concrete class-এ depend
    this.email = new GmailService(); // concrete class
  }
}

// ✅ Depend on abstractions (interfaces/abstract classes)
class OrderService2 {
  constructor(database, emailService) { // inject করা হয়
    this.db = database;         // যেকোনো DB
    this.email = emailService;  // যেকোনো email service
  }

  async createOrder(data) {
    const order = await this.db.save(data);
    await this.email.send(order.userEmail, "Order confirmed");
    return order;
  }
}

// Test-এ mock inject করা সহজ
const mockDb = { save: async (d) => ({ ...d, id: 1 }) };
const mockEmail = { send: async () => true };
const service = new OrderService2(mockDb, mockEmail);
```

---

## ৬.১১ PART 6 — Interview Questions & Answers

<div align="right"><a href="#part6">⬆ PART 6 উপরে</a> &nbsp;|&nbsp; <a href="#toc">📚 TOC</a></div>

<details>
<summary><strong>🔹 OOP Core Concepts (Q1–Q12)</strong></summary>
<br>

**Q1: JavaScript কি সত্যিকারের OOP language?**
> **A:** JavaScript prototype-based OOP language — class-based (Java, C++) নয়। ES6 Classes হলো prototype-এর syntactic sugar। তবে OOP-এর চারটি pillar (Encapsulation, Inheritance, Polymorphism, Abstraction) সবই JS-এ implement করা যায়।

**Q2: Prototype এবং Prototype Chain কী?**
> **A:** প্রতিটি JS object-এর একটি `[[Prototype]]` (internal link) আছে — আরেকটি object। Property না পেলে prototype-এ খোঁজে, সেখানে না পেলে prototype-এর prototype-এ — `null` পর্যন্ত। এটি Prototype Chain। Class inheritance ভেতরে এটিই ব্যবহার করে।

**Q3: `__proto__` এবং `prototype`-এর পার্থক্য?**
> **A:** `__proto__` — প্রতিটি object instance-এর internal prototype link (deprecated, `Object.getPrototypeOf()` ব্যবহার করুন)। `prototype` — শুধু functions-এর property, `new` দিয়ে তৈরি instances-এর `__proto__` হয়।

**Q4: Class কি ES6-এ নতুন OOP add করেছে?**
> **A:** না। Class সম্পূর্ণ syntactic sugar — ভেতরে prototype-based inheritance-ই ব্যবহার হয়। `typeof MyClass === "function"` — class আসলে function। পার্থক্য শুধু syntax এবং কিছু behavior (strict mode, hoisting নেই)।

**Q5: `super` কীভাবে কাজ করে?**
> **A:** Constructor-এ `super()` — parent constructor call। Method-এ `super.method()` — parent method call। Child class constructor-এ `this` access করার আগে `super()` call বাধ্যতামূলক। Static method-এ `super.staticMethod()` — parent static।

**Q6: Private class field (`#`) কীভাবে কাজ করে?**
> **A:** ES2022-এর feature। `#fieldName` — class বাইরে access করা যায় না (সত্যিকারের private)। Symbol বা closure-ভিত্তিক privacy-এর চেয়ে জোরালো। `instance.#field` — SyntaxError। Subclass-ও access করতে পারে না।

**Q7: Encapsulation কেন দরকার?**
> **A:** Internal implementation hide করে — বাইরের code শুধু public interface দেখে। ভেতরে পরিবর্তন করলে বাইরের code ভাঙে না। Invariants রক্ষা করা যায় (balance negative হতে দেওয়া যাবে না)। Code maintainable ও secure হয়।

**Q8: Inheritance vs Composition — কোনটি ভালো?**
> **A:** "Composition over Inheritance" — software engineering principle। Inheritance: tight coupling, deep hierarchy সমস্যা। Composition: object-এ অন্য object-এর instance রাখা — flexible। JS-এ mixins, higher-order functions দিয়ে composition সহজ। Simple hierarchy-তে inheritance, complex behavior-এ composition।

**Q9: Polymorphism কীভাবে JS-এ implement হয়?**
> **A:** Method overriding — child class parent-এর method redefine করে। Duck typing — object-এর type না জেনে method call করা (`if (obj.fly)`)। `instanceof` বা `typeof` check ছাড়াই same interface-এ different types কাজ করে।

**Q10: `new.target` কী?**
> **A:** Constructor/function-এ `new.target` — `new` দিয়ে call হলে constructor reference, নইলে `undefined`। Abstract class implement করতে: `if (new.target === AbstractClass) throw Error()`।

**Q11: Mixin pattern কী?**
> **A:** JS-এ multiple inheritance নেই। Mixin: একটি object-এর methods অন্য class-এ copy করা।
```javascript
const Serializable = (Base) => class extends Base {
  serialize() { return JSON.stringify(this); }
};
const Validatable = (Base) => class extends Base {
  validate() { /* ... */ }
};
class User extends Serializable(Validatable(Entity)) { }
```

**Q12: Static method কখন ব্যবহার করবেন?**
> **A:** Instance-এর state দরকার নেই এমন utility/factory methods-এ। `Math.max()`, `Array.from()`, `Object.keys()` সব static। Factory: `User.create()`, `Date.now()`, utility: `MathHelper.clamp()`।

</details>

<details>
<summary><strong>🔹 Advanced OOP (Q13–Q20)</strong></summary>
<br>

**Q13: Constructor function এবং Class-এর পার্থক্য?**
> **A:** Class: strict mode enforced, hoisting নেই (TDZ), `new` বাধ্যতামূলক, cleaner syntax, private fields support। Constructor function: hoisted, `new` ছাড়া call করা যায় (কিন্তু bug), prototype manually setup করতে হয়। ভেতরে একই — prototype-based।

**Q14: Getter/Setter কখন ব্যবহার করবেন?**
> **A:** Computed property (একাধিক field থেকে), validation (setter-এ check), lazy calculation (প্রথমবার access-এ compute, cache করা), backward compatibility (property → method transition)। `get fullName()` — `firstName + " " + lastName`।

**Q15: Object.create() এবং `new`-এর পার্থক্য?**
> **A:** `new Constructor()` — constructor function চলে। `Object.create(proto)` — constructor ছাড়া proto-র সাথে link করা object। `Object.create(null)` — prototype-হীন pure object (JSON-like)।

**Q16: SOLID কেন জানা দরকার?**
> **A:** SOLID মানা মানে maintainable, testable, extensible code। S: change করলে একটি জায়গায় affect। O: নতুন feature = নতুন class, পুরনো code অপরিবর্তিত। L: subtypes replace করা যায়। I:불필요한 dependency নেই। D: testing সহজ (mock inject)।

**Q17: Prototype-এ method রাখা vs constructor-এ রাখার পার্থক্য?**
> **A:** Constructor-এ: প্রতিটি instance-এ আলাদা copy — memory expensive। Prototype-এ: সব instances share করে — memory efficient। ১০০০ instance হলে prototype-এ method = ১টি copy, constructor-এ = ১০০০ copy।

**Q18: `instanceof` কীভাবে কাজ করে?**
> **A:** Prototype chain-এ খোঁজে। `a instanceof B` — `a.__proto__ === B.prototype` বা তার chain-এ? `Symbol.hasInstance` override করে customize করা যায়।

**Q19: Method chaining (Fluent Interface) কীভাবে implement করবেন?**
> **A:** প্রতিটি method `this` return করলে chain করা যায়:
```javascript
account.deposit(1000).withdraw(500).transfer(200);
```
Builder pattern-এ দরকারি।

**Q20: `Object.freeze()` দিয়ে কি সত্যিকারের immutable object তৈরি করা যায়?**
> **A:** Shallow freeze শুধু — top-level properties freeze হয়। Nested object freeze হয় না। Deep freeze-এর জন্য recursive:
```javascript
function deepFreeze(obj) {
  Object.getOwnPropertyNames(obj).forEach(name => {
    const val = obj[name];
    if (typeof val === "object" && val !== null) deepFreeze(val);
  });
  return Object.freeze(obj);
}
```

</details>

---

<div align="right">
  <a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a>
</div>

---

> **🚀 PART 7 আসছে:** JavaScript in Frontend Development — SPA basics, Virtual DOM, React fundamentals, Component architecture, State management, API integration, Routing।
>
> **💬 পরবর্তী PART পেতে:** "PART 7 দাও" লিখুন।
