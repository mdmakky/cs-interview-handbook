<a id="top"></a>

# Node.js Junior Engineer Interview Handbook (বাংলায়)

> **সম্পূর্ণ Node.js Interview Preparation — বাংলায়।**
> Junior থেকে Mid-level পর্যন্ত সব interview-এর জন্য। JavaScript runtime, Event Loop, Core Modules, Express, Database, Auth, REST API, Testing, Security, Performance — সব cover করা হয়েছে।

**👨‍💻 Target Audience:** Bangladesh-এর Junior Node.js / Backend Developer aspirants  
**🎯 Goal:** যেকোনো BD tech company-র interview crack করা  
**📚 Language:** বাংলায় ব্যাখ্যা, Technical terms ইংরেজিতে  

---

<a id="toc"></a>
## 📚 সম্পূর্ণ সূচি (Table of Contents)

| PART | বিষয় | Status |
|------|-------|--------|
| [PART 1](#part1) | Node.js Fundamentals — Architecture, Modules, npm | ✅ |
| [PART 2](#part2) | Core Modules ও Asynchronous Programming | ✅ |
| [PART 3](#part3) | Express.js Fundamentals | 🔜 |
| [PART 4](#part4) | Database Integration (MongoDB, PostgreSQL) | 🔜 |
| [PART 5](#part5) | Authentication ও Authorization | 🔜 |
| [PART 6](#part6) | REST API Design ও Validation | 🔜 |
| [PART 7](#part7) | Error Handling ও Logging | 🔜 |
| [PART 8](#part8) | Performance ও Scaling | 🔜 |
| [PART 9](#part9) | Testing (Jest, Supertest) | 🔜 |
| [PART 10](#part10) | Security Best Practices | 🔜 |
| [PART 11](#part11) | Advanced Topics (WebSockets, Streams, Microservices) | 🔜 |
| [PART 12](#part12) | Bangladesh Interview Preparation | 🔜 |

---

<a id="part1"></a>
## PART 1: Node.js Fundamentals — Architecture, Modules, npm

> Node.js-এর core concepts। এই PART-এ V8 Engine, Event Loop, Non-blocking I/O, Module System এবং npm সম্পর্কে সম্পূর্ণ ধারণা পাবেন।

| # | বিষয় |
|---|-------|
| 1 | [Node.js কী? ইতিহাস ও কেন ব্যবহার করি](#p1-intro) |
| 2 | [Node.js Architecture — V8, libuv, Event Loop](#p1-architecture) |
| 3 | [Single-threaded Non-blocking I/O Model](#p1-nonblocking) |
| 4 | [Event Loop — Deep Dive](#p1-eventloop) |
| 5 | [Global Objects ও Built-in Variables](#p1-globals) |
| 6 | [Module System — CommonJS vs ES Modules](#p1-modules) |
| 7 | [npm, package.json, npx](#p1-npm) |
| 8 | [প্রথম Node.js Application](#p1-firstapp) |
| 9 | [PART 1 Interview Q&A](#p1-qa) |

---

<a id="p1-intro"></a>
**Topic 1: Node.js কী? ইতিহাস ও কেন ব্যবহার করি**

**Node.js কী:**
Node.js হলো Chrome-এর V8 JavaScript Engine-এর উপরে তৈরি একটি **open-source, cross-platform JavaScript runtime environment**। অর্থাৎ JavaScript এখন শুধু browser-এ নয়, server-side-এও চলতে পারে।

```
Browser:   JavaScript → Chrome V8 → Web page manipulation
Node.js:   JavaScript → V8 Engine → File system, Network, Database...
```

**ইতিহাস:**
```
2009 — Ryan Dahl, Node.js create করেন (C++ এ V8 wrap করে)
2010 — npm (Node Package Manager) release
2015 — io.js fork → Node.js Foundation merge
2018 — Node.js 10 LTS (Long Term Support)
2020 — Node.js 14, ES Modules stable support
2022 — Node.js 18 LTS — fetch API built-in, Web Streams
2024 — Node.js 20/22 — TypeScript types built-in experiment
```

**কেন Node.js ব্যবহার করি:**
```
✅ JavaScript everywhere — Frontend ও Backend একই language
✅ Non-blocking I/O — অনেক concurrent requests handle করতে পারে
✅ Fast — V8 engine JIT compilation
✅ Huge ecosystem — npm-এ 2M+ packages
✅ Real-time applications-এর জন্য ideal (chat, gaming, live feeds)
✅ Microservices-এর জন্য lightweight
```

**কখন Node.js ব্যবহার করবেন না:**
```
❌ CPU-intensive tasks (image processing, ML, video encoding)
   — Single thread block হয়ে যায়
❌ Heavy computation-heavy কাজে
   — Python, Go, Java বেশি suitable
✅ I/O-bound কাজে (API calls, DB queries, file read) — Node.js excellent
```

---

<a id="p1-architecture"></a>
**Topic 2: Node.js Architecture — V8, libuv, Event Loop**

```
┌────────────────────────────────────────────────────────────┐
│                    Node.js Architecture                    │
├────────────────────────────────────────────────────────────┤
│  JavaScript Code (আপনার app.js)                           │
├────────────────────────────────────────────────────────────┤
│  Node.js Bindings (C++ bindings)                          │
├──────────────────────┬─────────────────────────────────────┤
│  V8 Engine           │  libuv                              │
│  (JS Execution,      │  (Event Loop, Thread Pool,          │
│   JIT Compiler,      │   Async I/O, OS abstraction)        │
│   Memory Management) │                                     │
├──────────────────────┴─────────────────────────────────────┤
│  Operating System (Linux / macOS / Windows)                │
└────────────────────────────────────────────────────────────┘
```

**V8 Engine:**
- Google Chrome-এর JavaScript engine (C++ এ লেখা)
- JavaScript → Machine code (JIT compilation)
- Garbage collection, memory management
- Node.js V8 ব্যবহার করে জন্যই JS এত fast

**libuv:**
- C library — cross-platform asynchronous I/O
- Event Loop implement করে
- Thread pool (default 4 threads) — heavy tasks-এর জন্য
- OS-level async APIs wrap করে (epoll on Linux, kqueue on macOS, IOCP on Windows)

**Node.js Layer:**
```
Your Code
    ↓
Node.js Standard Library (fs, http, path…)
    ↓
Node.js C++ Bindings
    ↓
V8 (JS execution) + libuv (async I/O)
    ↓
Operating System
```

---

<a id="p1-nonblocking"></a>
**Topic 3: Single-threaded Non-blocking I/O Model**

**Traditional Server (Apache, PHP):**
```
Request 1 → Thread 1 (waiting for DB...) → Response 1
Request 2 → Thread 2 (waiting for DB...) → Response 2
Request 3 → Thread 3 (waiting for DB...) → Response 3
...
100 requests → 100 threads → RAM exhausted!
```

**Node.js Model:**
```
Request 1 ─┐
Request 2 ─┤→ Single Thread → Event Loop
Request 3 ─┘
             ↓
     Async operations delegate to OS/libuv
             ↓
     Callback queue → Process → Response
```

**উদাহরণ:**
```javascript
// Blocking (synchronous) — BAD for Node.js
const fs = require('fs');
const data = fs.readFileSync('large-file.txt');  // Thread BLOCKS হয়
console.log(data);

// Non-blocking (asynchronous) — GOOD
fs.readFile('large-file.txt', (err, data) => {
    if (err) throw err;
    console.log(data);
});
console.log('এই line আগে print হবে!');
// Output:
// এই line আগে print হবে!
// (file content)
```

**কেন এটা efficient:**
```
File I/O করতে 100ms লাগে।
10,000 requests × 100ms = 1,000,000ms (blocking model)

Node.js: সব requests একসাথে start করো, OS করুক কাজ, callback আসলে process করো
10,000 requests → ~100ms (non-blocking model)
```

---

<a id="p1-eventloop"></a>
**Topic 4: Event Loop — Deep Dive**

**Event Loop কী:**
Node.js-এর হৃদয়। JavaScript single-threaded হওয়া সত্ত্বেও কীভাবে async কাজ করে — Event Loop এর জন্য।

**Event Loop Phases:**
```
   ┌───────────────────────────┐
┌─>│           timers          │  ← setTimeout, setInterval callbacks
│  └─────────────┬─────────────┘
│  ┌─────────────▼─────────────┐
│  │     pending callbacks     │  ← I/O errors
│  └─────────────┬─────────────┘
│  ┌─────────────▼─────────────┐
│  │       idle, prepare       │  ← internal use
│  └─────────────┬─────────────┘
│  ┌─────────────▼─────────────┐
│  │           poll            │  ← I/O callbacks (fs.readFile etc.)
│  └─────────────┬─────────────┘
│  ┌─────────────▼─────────────┐
│  │           check           │  ← setImmediate callbacks
│  └─────────────┬─────────────┘
│  ┌─────────────▼─────────────┐
└──│      close callbacks      │  ← socket.on('close')
   └───────────────────────────┘
```

**Priority Queue (প্রতিটি phase-এর মধ্যে):**
```
1. process.nextTick()    ← সর্বোচ্চ priority, phase শেষ হওয়ার আগেই
2. Microtasks (Promises) ← nextTick-এর পরে
3. Macro tasks (setTimeout, setImmediate, I/O callbacks)
```

**উদাহরণ — Execution Order:**
```javascript
console.log('1 — synchronous');

setTimeout(() => console.log('2 — setTimeout 0ms'), 0);

Promise.resolve().then(() => console.log('3 — Promise'));

process.nextTick(() => console.log('4 — nextTick'));

setImmediate(() => console.log('5 — setImmediate'));

console.log('6 — synchronous');

// Output:
// 1 — synchronous
// 6 — synchronous
// 4 — nextTick         (process.nextTick সবার আগে)
// 3 — Promise          (microtask)
// 2 — setTimeout 0ms   (timer phase)
// 5 — setImmediate     (check phase)
```

**setTimeout vs setImmediate:**
```javascript
// poll phase-এর মধ্যে (I/O callback-এ) setImmediate সবসময় আগে:
const fs = require('fs');
fs.readFile(__filename, () => {
    setTimeout(() => console.log('setTimeout'), 0);
    setImmediate(() => console.log('setImmediate'));
    // Output: setImmediate → setTimeout (always, inside I/O)
});

// top-level-এ: order non-deterministic (OS timing-এর উপর নির্ভর)
```

**process.nextTick() — কখন ব্যবহার করবেন:**
```javascript
// কোনো operation synchronously শুরু কিন্তু callback async চাইলে
function readData(callback) {
    // ❌ এটা bad — callback synchronously call হচ্ছে
    if (cachedData) {
        callback(null, cachedData);
    } else {
        fs.readFile('data.txt', callback);
    }

    // ✅ Consistent async behavior
    if (cachedData) {
        process.nextTick(() => callback(null, cachedData));
    } else {
        fs.readFile('data.txt', callback);
    }
}
```

---

<a id="p1-globals"></a>
**Topic 5: Global Objects ও Built-in Variables**

```javascript
// ────────────────────────────────────────────
// Global object (browser-এ window, Node-এ global)
// ────────────────────────────────────────────
global.myVar = 'hello';
console.log(myVar);  // 'hello'

// ────────────────────────────────────────────
// process object — current Node.js process info
// ────────────────────────────────────────────
console.log(process.version);      // 'v20.11.0'
console.log(process.platform);     // 'linux', 'darwin', 'win32'
console.log(process.pid);          // Process ID
console.log(process.env.NODE_ENV); // Environment variable
console.log(process.argv);         // Command line arguments
// process.argv[0] = 'node'
// process.argv[1] = '/path/to/script.js'
// process.argv[2] = first argument

process.exit(0);    // Clean exit
process.exit(1);    // Error exit

process.on('exit', (code) => console.log(`Exiting with code: ${code}`));
process.on('uncaughtException', (err) => {
    console.error('Uncaught:', err);
    process.exit(1);
});

// ────────────────────────────────────────────
// __dirname এবং __filename (CommonJS only)
// ────────────────────────────────────────────
console.log(__dirname);   // '/home/user/project/src' (current directory)
console.log(__filename);  // '/home/user/project/src/app.js' (current file)

// ES Modules-এ equivalent:
import { fileURLToPath } from 'url';
import { dirname } from 'path';
const __filename = fileURLToPath(import.meta.url);
const __dirname = dirname(__filename);

// ────────────────────────────────────────────
// Buffer — binary data
// ────────────────────────────────────────────
const buf = Buffer.from('Hello World', 'utf-8');
console.log(buf);           // <Buffer 48 65 6c 6c 6f...>
console.log(buf.toString()); // 'Hello World'
console.log(buf.length);     // 11

const buf2 = Buffer.alloc(10);  // 10 bytes, zero-filled
const buf3 = Buffer.allocUnsafe(10);  // 10 bytes, uninitialized (fast)

// ────────────────────────────────────────────
// setTimeout, setInterval, clearTimeout, clearInterval
// ────────────────────────────────────────────
const timer = setTimeout(() => console.log('1 sec later'), 1000);
clearTimeout(timer);  // cancel

const interval = setInterval(() => console.log('every 2s'), 2000);
setTimeout(() => clearInterval(interval), 10000);  // 10s পরে stop

// setImmediate — I/O callbacks-এর পরে, setTimeout(0) এর আগে
setImmediate(() => console.log('immediate'));

// ────────────────────────────────────────────
// console methods
// ────────────────────────────────────────────
console.log('info');
console.error('error');    // stderr-এ
console.warn('warning');
console.table([{name: 'Alice', age: 25}]);
console.time('label');
// ... code ...
console.timeEnd('label');  // label: 5.231ms
console.count('hits');     // hits: 1
console.dir(obj, { depth: null });  // deep object
```

---

<a id="p1-modules"></a>
**Topic 6: Module System — CommonJS vs ES Modules**

**CommonJS (default in Node.js):**
```javascript
// math.js — export করুন
function add(a, b) { return a + b; }
function subtract(a, b) { return a - b; }
const PI = 3.14159;

module.exports = { add, subtract, PI };
// অথবা:
exports.add = add;
exports.subtract = subtract;
// ⚠️ exports.add = ... OK, কিন্তু exports = { add } — WRONG!
// module.exports = { add } — সঠিক single object export

// app.js — import করুন
const math = require('./math');
console.log(math.add(2, 3));  // 5

// Destructuring
const { add, PI } = require('./math');

// Built-in modules
const fs = require('fs');
const path = require('path');
const http = require('http');

// npm packages
const express = require('express');
```

**ES Modules (modern, .mjs বা package.json "type": "module"):**
```javascript
// math.mjs — export
export function add(a, b) { return a + b; }
export const PI = 3.14159;
export default function multiply(a, b) { return a * b; }

// app.mjs — import
import multiply, { add, PI } from './math.mjs';
import * as math from './math.mjs';   // namespace import

// Dynamic import (lazy loading)
const module = await import('./heavy-module.mjs');
```

**CommonJS vs ES Modules পার্থক্য:**

| | CommonJS (CJS) | ES Modules (ESM) |
|---|---|---|
| Syntax | `require()` / `module.exports` | `import` / `export` |
| Loading | Synchronous | Asynchronous |
| Default | Node.js default | `"type": "module"` চাই |
| File ext | `.js` / `.cjs` | `.mjs` বা `.js` (with type) |
| Tree shaking | ❌ | ✅ (bundlers করে) |
| Top-level await | ❌ | ✅ |
| `__dirname` | ✅ | ❌ (workaround দরকার) |

**package.json এ type:**
```json
{
  "type": "module"    // সব .js files ESM হয়
}
// অথবা:
{
  "type": "commonjs"  // default — সব .js files CJS
}
// Mixed: .mjs = ESM always, .cjs = CJS always
```

**Module caching:**
```javascript
// require() cached — same file দুবার require করলে same object পাবেন
const a = require('./config');
const b = require('./config');
console.log(a === b);  // true (same reference)

// Cache clear (rare, testing-এ):
delete require.cache[require.resolve('./config')];
```

---

<a id="p1-npm"></a>
**Topic 7: npm, package.json, npx**

**npm (Node Package Manager):**
```bash
# ────────────────────────────────────────────
# Initialization
# ────────────────────────────────────────────
npm init           # interactive setup
npm init -y        # defaults সহ (সব yes)

# ────────────────────────────────────────────
# Install packages
# ────────────────────────────────────────────
npm install express              # production dependency
npm install --save-dev jest      # dev dependency (test, lint tools)
npm install -D typescript        # same as --save-dev
npm install -g nodemon           # global install (সব project-এ পাওয়া যাবে)
npm install                      # package.json থেকে সব install

# ────────────────────────────────────────────
# Package management
# ────────────────────────────────────────────
npm uninstall express            # remove
npm update express               # update to latest compatible
npm update                       # সব update
npm outdated                     # কোনটা outdated দেখুন
npm list                         # installed packages
npm list --depth=0               # top-level only

# ────────────────────────────────────────────
# Scripts
# ────────────────────────────────────────────
npm run start                    # package.json scripts.start
npm run dev                      # scripts.dev
npm test                         # scripts.test (no 'run' needed)
npm start                        # scripts.start (no 'run' needed)

# ────────────────────────────────────────────
# Audit
# ────────────────────────────────────────────
npm audit                        # security vulnerabilities check
npm audit fix                    # auto fix
npm audit fix --force            # breaking changes সহ fix (সাবধানে)
```

**package.json:**
```json
{
  "name": "my-node-app",
  "version": "1.0.0",
  "description": "My Node.js application",
  "main": "src/index.js",
  "type": "commonjs",
  "scripts": {
    "start": "node src/index.js",
    "dev": "nodemon src/index.js",
    "test": "jest --coverage",
    "lint": "eslint src/",
    "build": "tsc"
  },
  "keywords": ["node", "api"],
  "author": "Alice <alice@example.com>",
  "license": "MIT",
  "dependencies": {
    "express": "^4.18.2",
    "mongoose": "^7.5.0",
    "dotenv": "^16.3.1",
    "bcryptjs": "^2.4.3",
    "jsonwebtoken": "^9.0.2"
  },
  "devDependencies": {
    "jest": "^29.7.0",
    "supertest": "^6.3.3",
    "nodemon": "^3.0.1",
    "eslint": "^8.50.0"
  },
  "engines": {
    "node": ">=18.0.0"
  }
}
```

**Version ranges:**
```
"express": "4.18.2"   — exact version
"express": "^4.18.2"  — ^: compatible (patch+minor update ok, major না)
                         4.18.2, 4.19.0, 4.20.0 — ok; 5.0.0 — no
"express": "~4.18.2"  — ~: patch update ok only
                         4.18.2, 4.18.3 — ok; 4.19.0 — no
"express": "*"         — যেকোনো version (avoid!)
"express": ">=4.0.0"  — 4.0.0 বা তার উপরে
```

**package-lock.json:**
```
package.json: version ranges define করে (^4.18.2)
package-lock.json: exact versions lock করে (4.18.2 exactly)

→ package-lock.json commit করুন (consistent installs)
→ node_modules কখনো commit করবেন না (.gitignore-এ রাখুন)
```

**npx:**
```bash
# Package install না করেই run করুন
npx create-react-app my-app
npx ts-node script.ts
npx jest

# Specific version দিয়ে run
npx node@18 --version

# Local bin run করুন
npx eslint src/
# = ./node_modules/.bin/eslint src/
```

**.npmrc — npm configuration:**
```bash
# project root-এ .npmrc
registry=https://registry.npmjs.org/
save-exact=true          # ^ ছাড়া exact version save করুন
```

---

<a id="p1-firstapp"></a>
**Topic 8: প্রথম Node.js Application**

**Simple HTTP Server:**
```javascript
// server.js
const http = require('http');

const PORT = process.env.PORT || 3000;

const server = http.createServer((req, res) => {
    console.log(`${req.method} ${req.url}`);

    // Response headers
    res.setHeader('Content-Type', 'application/json');
    res.setHeader('X-Powered-By', 'Node.js');

    // Routing
    if (req.method === 'GET' && req.url === '/') {
        res.statusCode = 200;
        res.end(JSON.stringify({ message: 'Hello from Node.js!' }));

    } else if (req.method === 'GET' && req.url === '/health') {
        res.statusCode = 200;
        res.end(JSON.stringify({ status: 'healthy', uptime: process.uptime() }));

    } else {
        res.statusCode = 404;
        res.end(JSON.stringify({ error: 'Not Found' }));
    }
});

server.listen(PORT, () => {
    console.log(`Server running at http://localhost:${PORT}/`);
});

// Graceful shutdown
process.on('SIGTERM', () => {
    console.log('SIGTERM received, shutting down...');
    server.close(() => {
        console.log('Server closed');
        process.exit(0);
    });
});
```

**Project structure (best practice):**
```
my-node-app/
├── src/
│   ├── index.js          ← entry point
│   ├── app.js            ← Express app
│   ├── routes/
│   │   ├── auth.js
│   │   └── users.js
│   ├── controllers/
│   │   ├── authController.js
│   │   └── userController.js
│   ├── models/
│   │   └── User.js
│   ├── middleware/
│   │   ├── auth.js
│   │   └── errorHandler.js
│   ├── config/
│   │   └── database.js
│   └── utils/
│       └── helpers.js
├── tests/
│   └── auth.test.js
├── .env                  ← secrets (gitignore!)
├── .env.example          ← template (commit করুন)
├── .gitignore
├── package.json
└── README.md
```

**nodemon — Development auto-restart:**
```bash
npm install -D nodemon

# package.json scripts:
# "dev": "nodemon src/index.js"

npm run dev
# [nodemon] watching: *.*
# [nodemon] starting `node src/index.js`
# Server running at http://localhost:3000/
# (file save হলে auto-restart)
```

---

<a id="p1-qa"></a>
**Topic 9: PART 1 Interview Q&A**

```
প্রশ্ন: Node.js কী? Browser JavaScript-এর সাথে পার্থক্য কী?
উত্তর: Node.js হলো server-side JavaScript runtime।
Browser JS: DOM manipulation, window, fetch
Node.js: File system, Network, OS — কোনো DOM নেই।
দুটোতেই V8 engine কিন্তু environment আলাদা।

প্রশ্ন: Node.js single-threaded হলেও কীভাবে concurrent requests handle করে?
উত্তর: Event Loop-এর মাধ্যমে। I/O operations (file read, DB query)
OS/libuv-কে delegate করে। Callback queue-তে result আসলে process করে।
CPU block না হওয়ায় অন্য requests process করতে পারে।

প্রশ্ন: Event Loop কী? Phases কী কী?
উত্তর: Node.js-এর async mechanism। Phases:
timers → pending callbacks → idle/prepare → poll → check → close callbacks
process.nextTick সবার আগে, তারপর Promises (microtasks), তারপর macro tasks।

প্রশ্ন: CommonJS ও ES Modules-এর পার্থক্য?
উত্তর:
CJS: require/module.exports, synchronous, default
ESM: import/export, async, "type":"module" দরকার
ESM-এ top-level await পাওয়া যায়, CJS-এ নয়।

প্রশ্ন: package-lock.json কেন important?
উত্তর: Exact dependency versions lock করে।
package.json-এ ^4.18.2 মানে 4.19.0-ও install হতে পারে।
package-lock.json নিশ্চিত করে যে সব developer এবং CI/CD একই version পাবে।
Always commit করুন।

প্রশ্ন: CPU-intensive task Node.js-এ কীভাবে করবেন?
উত্তর: Worker Threads ব্যবহার করব (worker_threads module)।
অথবা: Child process spawn করব।
অথবা: সেই কাজটি Python/Go microservice-এ করব।
Main thread block করা যাবে না।
```

---

**PART 1 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| Node.js | Server-side JS runtime, V8 + libuv |
| V8 | Google-এর JS engine, JIT compilation |
| libuv | Async I/O library, Event Loop, Thread Pool |
| Event Loop | Async mechanism — phases: timers→poll→check |
| process.nextTick | Highest priority microtask |
| Non-blocking I/O | I/O OS-কে delegate, main thread free |
| CommonJS | require/exports, synchronous |
| ES Modules | import/export, async, modern |
| npm | Package manager, 2M+ packages |
| package-lock.json | Exact versions lock — always commit |
| npx | Install ছাড়া package run |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part2"></a>
## PART 2: Core Modules ও Asynchronous Programming

> Node.js-এর built-in modules ও async programming patterns। fs, path, events, stream, এবং Callback → Promise → async/await evolution।

| # | বিষয় |
|---|-------|
| 1 | [Core Modules Overview](#p2-overview) |
| 2 | [fs — File System Module](#p2-fs) |
| 3 | [path Module](#p2-path) |
| 4 | [os Module](#p2-os) |
| 5 | [events — EventEmitter](#p2-events) |
| 6 | [stream Module](#p2-stream) |
| 7 | [Callback Pattern](#p2-callback) |
| 8 | [Promise](#p2-promise) |
| 9 | [async/await](#p2-async-await) |
| 10 | [Error Handling in Async Code](#p2-error) |
| 11 | [PART 2 Interview Q&A](#p2-qa) |

---

<a id="p2-overview"></a>
**Topic 1: Core Modules Overview**

```javascript
// Node.js-এর built-in modules — install ছাড়াই পাওয়া যায়
const fs       = require('fs');        // File system
const path     = require('path');      // File paths
const os       = require('os');        // Operating system info
const events   = require('events');    // Event system
const http     = require('http');      // HTTP server/client
const https    = require('https');     // HTTPS
const stream   = require('stream');    // Streams
const crypto   = require('crypto');    // Cryptography
const url      = require('url');       // URL parsing
const querystring = require('querystring'); // Query strings
const util     = require('util');      // Utilities
const buffer   = require('buffer');    // Binary data
const child_process = require('child_process'); // Spawn processes
const cluster  = require('cluster');   // Multi-process
const worker_threads = require('worker_threads'); // Threads
const readline = require('readline'); // CLI input
const zlib     = require('zlib');      // Compression
const net      = require('net');       // TCP
const dns      = require('dns');       // DNS lookup
const assert   = require('assert');    // Assertions (testing)
const timers   = require('timers');    // setTimeout etc.
```

---

<a id="p2-fs"></a>
**Topic 2: fs — File System Module**

```javascript
const fs = require('fs');
const fsPromises = require('fs').promises;
// অথবা: const { promises: fsPromises } = require('fs');

// ────────────────────────────────────────────
// Async (callback) — Non-blocking ✅
// ────────────────────────────────────────────
// Read file
fs.readFile('data.txt', 'utf8', (err, data) => {
    if (err) {
        console.error('Error reading file:', err.message);
        return;
    }
    console.log(data);
});

// Write file (overwrite)
fs.writeFile('output.txt', 'Hello World!\n', 'utf8', (err) => {
    if (err) throw err;
    console.log('File written!');
});

// Append to file
fs.appendFile('log.txt', `[${new Date().toISOString()}] Log entry\n`, (err) => {
    if (err) throw err;
});

// Copy file
fs.copyFile('source.txt', 'dest.txt', (err) => {
    if (err) throw err;
    console.log('Copied!');
});

// Delete file
fs.unlink('temp.txt', (err) => {
    if (err && err.code !== 'ENOENT') throw err;  // ENOENT = file not found
    console.log('Deleted (or didn\'t exist)');
});

// File info
fs.stat('data.txt', (err, stats) => {
    if (err) throw err;
    console.log(stats.isFile());      // true
    console.log(stats.isDirectory()); // false
    console.log(stats.size);          // bytes
    console.log(stats.mtime);         // last modified
});

// ────────────────────────────────────────────
// Directories
// ────────────────────────────────────────────
fs.mkdir('new-folder', { recursive: true }, (err) => {
    if (err) throw err;
});

fs.readdir('src/', (err, files) => {
    if (err) throw err;
    console.log(files);  // ['index.js', 'app.js', ...]
});

fs.rmdir('old-folder', { recursive: true }, (err) => {
    if (err) throw err;
});

// ────────────────────────────────────────────
// Promise-based (modern, recommended)
// ────────────────────────────────────────────
async function readConfig() {
    try {
        const data = await fsPromises.readFile('config.json', 'utf8');
        return JSON.parse(data);
    } catch (err) {
        if (err.code === 'ENOENT') {
            console.log('Config file not found, using defaults');
            return {};
        }
        throw err;
    }
}

async function writeConfig(config) {
    await fsPromises.writeFile(
        'config.json',
        JSON.stringify(config, null, 2),
        'utf8'
    );
}

// ────────────────────────────────────────────
// Sync (blocking) — শুধু startup-এ ব্যবহার করুন
// ────────────────────────────────────────────
try {
    const data = fs.readFileSync('config.json', 'utf8');
    const config = JSON.parse(data);
} catch (err) {
    console.log('No config file found');
}

// ────────────────────────────────────────────
// File watching
// ────────────────────────────────────────────
fs.watch('src/', { recursive: true }, (eventType, filename) => {
    console.log(`${eventType}: ${filename}`);
    // 'change': src/app.js
    // 'rename': src/new-file.js
});
```

**util.promisify — Callback → Promise:**
```javascript
const { promisify } = require('util');
const readFile = promisify(fs.readFile);
const writeFile = promisify(fs.writeFile);

async function copyFile(src, dest) {
    const content = await readFile(src, 'utf8');
    await writeFile(dest, content, 'utf8');
}
```

---

<a id="p2-path"></a>
**Topic 3: path Module**

```javascript
const path = require('path');

// ────────────────────────────────────────────
// Path construction
// ────────────────────────────────────────────
const filePath = path.join('/home', 'user', 'project', 'src', 'app.js');
// '/home/user/project/src/app.js'

// Relative থেকে absolute
const absolute = path.resolve('src', 'app.js');
// '/home/user/project/src/app.js' (process.cwd() থেকে)

// __dirname দিয়ে (recommended)
const configPath = path.join(__dirname, '..', 'config', 'db.json');
// '/home/user/project/config/db.json'

// ────────────────────────────────────────────
// Path parsing
// ────────────────────────────────────────────
const p = '/home/user/project/src/app.js';

path.dirname(p)   // '/home/user/project/src'
path.basename(p)  // 'app.js'
path.extname(p)   // '.js'
path.basename(p, '.js')  // 'app' (extension ছাড়া)

const parsed = path.parse(p);
// { root: '/', dir: '/home/user/project/src', base: 'app.js',
//   ext: '.js', name: 'app' }

path.format(parsed)  // '/home/user/project/src/app.js'

// ────────────────────────────────────────────
// Cross-platform
// ────────────────────────────────────────────
path.sep        // '/' on Linux/Mac, '\\' on Windows
path.delimiter  // ':' on Linux/Mac, ';' on Windows

// Windows path normalize
path.normalize('/foo/bar//baz/../../../')  // '/foo/bar/baz' → '/'

// Relative path between two paths
path.relative('/home/user', '/home/user/project/src')  // 'project/src'
```

---

<a id="p2-os"></a>
**Topic 4: os Module**

```javascript
const os = require('os');

os.platform()     // 'linux', 'darwin', 'win32'
os.arch()         // 'x64', 'arm64'
os.hostname()     // 'my-server'
os.release()      // '5.15.0-100-generic'
os.type()         // 'Linux', 'Darwin', 'Windows_NT'

os.uptime()       // seconds since boot
os.totalmem()     // total RAM in bytes
os.freemem()      // free RAM in bytes

os.cpus()         // Array of CPU info
// [{ model: 'Intel...', speed: 2400, times: { user, nice, sys, idle } }]
os.cpus().length  // CPU core count

os.networkInterfaces()  // Network adapters

os.homedir()      // '/home/username'
os.tmpdir()       // '/tmp'
os.EOL            // '\n' on Unix, '\r\n' on Windows

// Practical: Log system info
function logSystemInfo() {
    const totalMB = (os.totalmem() / 1024 / 1024).toFixed(0);
    const freeMB = (os.freemem() / 1024 / 1024).toFixed(0);
    const usedPercent = ((1 - os.freemem() / os.totalmem()) * 100).toFixed(1);
    console.log(`Platform: ${os.platform()} | CPUs: ${os.cpus().length}`);
    console.log(`RAM: ${freeMB}MB free / ${totalMB}MB total (${usedPercent}% used)`);
}
```

---

<a id="p2-events"></a>
**Topic 5: events — EventEmitter**

**EventEmitter কী:**
Node.js-এর Observer pattern implementation। কোনো event emit হলে registered listeners call হয়।

```javascript
const EventEmitter = require('events');

// ────────────────────────────────────────────
// Basic usage
// ────────────────────────────────────────────
const emitter = new EventEmitter();

// Listener register করুন
emitter.on('data', (payload) => {
    console.log('Data received:', payload);
});

emitter.on('data', (payload) => {
    console.log('Second listener:', payload.length);
});

// Event emit করুন
emitter.emit('data', { items: [1, 2, 3] });
// Data received: { items: [1, 2, 3] }
// Second listener: 3

// One-time listener
emitter.once('connect', () => {
    console.log('Connected! (fires only once)');
});

// Listener remove করুন
function handler(data) { console.log(data); }
emitter.on('message', handler);
emitter.off('message', handler);     // remove
emitter.removeListener('message', handler);  // same

// সব listeners remove
emitter.removeAllListeners('data');

// Info
emitter.listenerCount('data');  // listener count
emitter.eventNames();           // ['data', 'connect', ...]

// ────────────────────────────────────────────
// Custom class (extend EventEmitter)
// ────────────────────────────────────────────
class Database extends EventEmitter {
    constructor(config) {
        super();
        this.config = config;
        this.connected = false;
    }

    async connect() {
        try {
            // ... connection logic ...
            this.connected = true;
            this.emit('connect', { host: this.config.host });
        } catch (err) {
            this.emit('error', err);
        }
    }

    async query(sql, params) {
        if (!this.connected) {
            this.emit('error', new Error('Not connected'));
            return;
        }
        // ... query logic ...
        const result = { rows: [] };
        this.emit('query', { sql, rowCount: result.rows.length });
        return result;
    }

    disconnect() {
        this.connected = false;
        this.emit('disconnect');
    }
}

// Usage
const db = new Database({ host: 'localhost' });
db.on('connect', (info) => console.log(`Connected to ${info.host}`));
db.on('error', (err) => console.error('DB Error:', err.message));
db.on('disconnect', () => console.log('Disconnected'));
db.connect();

// ────────────────────────────────────────────
// error event — MUST handle করুন
// ────────────────────────────────────────────
emitter.on('error', (err) => {
    console.error('Error:', err.message);
    // Handle gracefully
});
// 'error' event unhandled থাকলে → uncaught exception → process crash!

// ────────────────────────────────────────────
// Max listeners warning
// ────────────────────────────────────────────
emitter.setMaxListeners(20);  // default 10 — বেশি হলে warning
// Memory leak এড়াতে cleanup করুন
```

---

<a id="p2-stream"></a>
**Topic 6: stream Module**

**Stream কী:**
বড় data চাংক করে process করার mechanism। পুরো data memory-তে না এনে piece-by-piece কাজ করা।

```
Without stream: 1GB file → 1GB RAM
With stream:    1GB file → 64KB chunk → process → next chunk → ...
```

**4 types of streams:**
```javascript
const { Readable, Writable, Duplex, Transform } = require('stream');

// ────────────────────────────────────────────
// Readable — data পড়া যায়
// ────────────────────────────────────────────
const { createReadStream } = require('fs');

const readable = createReadStream('large-file.txt', {
    encoding: 'utf8',
    highWaterMark: 64 * 1024  // 64KB chunks (default)
});

readable.on('data', (chunk) => {
    console.log('Chunk size:', chunk.length);
});
readable.on('end', () => console.log('Done reading'));
readable.on('error', (err) => console.error(err));

// ────────────────────────────────────────────
// Writable — data লেখা যায়
// ────────────────────────────────────────────
const { createWriteStream } = require('fs');
const writable = createWriteStream('output.txt');

writable.write('First chunk\n');
writable.write('Second chunk\n');
writable.end('Final chunk\n');

writable.on('finish', () => console.log('Writing complete'));

// ────────────────────────────────────────────
// Pipe — streams connect করুন
// ────────────────────────────────────────────
// File copy with pipe — simple ও memory efficient
createReadStream('large.txt')
    .pipe(createWriteStream('copy.txt'));

// HTTP request pipe
const http = require('http');
http.createServer((req, res) => {
    const fileStream = createReadStream('large-file.txt');
    fileStream.pipe(res);  // file stream → response stream
}).listen(3000);

// ────────────────────────────────────────────
// Transform stream — read + modify + write
// ────────────────────────────────────────────
const { Transform } = require('stream');
const zlib = require('zlib');

// Gzip compression (Transform stream)
createReadStream('input.txt')
    .pipe(zlib.createGzip())          // Transform: compress
    .pipe(createWriteStream('input.txt.gz'));

// Custom Transform
class UpperCaseTransform extends Transform {
    _transform(chunk, encoding, callback) {
        this.push(chunk.toString().toUpperCase());
        callback();
    }
}

createReadStream('input.txt', { encoding: 'utf8' })
    .pipe(new UpperCaseTransform())
    .pipe(createWriteStream('upper.txt'));

// ────────────────────────────────────────────
// pipeline (error handling সহ pipe)
// ────────────────────────────────────────────
const { pipeline } = require('stream');
const { promisify } = require('util');
const pipelineAsync = promisify(pipeline);

async function compressFile(input, output) {
    await pipelineAsync(
        createReadStream(input),
        zlib.createGzip(),
        createWriteStream(output)
    );
    console.log('Compressed successfully');
}
```

---

<a id="p2-callback"></a>
**Topic 7: Callback Pattern**

**Callback কী:**
Function যেটি অন্য function-এ pass করা হয়, async operation শেষে call হয়।

```javascript
// Error-first callback convention (Node.js standard)
function readUserFromDB(userId, callback) {
    // Simulated async operation
    setTimeout(() => {
        if (userId <= 0) {
            callback(new Error('Invalid user ID'), null);  // error first
        } else {
            callback(null, { id: userId, name: 'Alice' }); // null error
        }
    }, 100);
}

// Usage
readUserFromDB(1, (err, user) => {
    if (err) {
        console.error('Error:', err.message);
        return;
    }
    console.log('User:', user.name);
});
```

**Callback Hell — সমস্যা:**
```javascript
// ❌ Callback Hell (Pyramid of Doom)
getUser(userId, (err, user) => {
    if (err) return handleError(err);
    getProfile(user.id, (err, profile) => {
        if (err) return handleError(err);
        getOrders(profile.id, (err, orders) => {
            if (err) return handleError(err);
            processOrders(orders, (err, result) => {
                if (err) return handleError(err);
                sendEmail(user.email, result, (err) => {
                    if (err) return handleError(err);
                    console.log('Done!');
                });
            });
        });
    });
});
```

**Named functions দিয়ে কিছুটা ভালো:**
```javascript
function onUserFetched(err, user) {
    if (err) return handleError(err);
    getProfile(user.id, onProfileFetched.bind(null, user));
}

function onProfileFetched(user, err, profile) {
    if (err) return handleError(err);
    getOrders(profile.id, onOrdersFetched.bind(null, user));
}
// ... তবু জটিল, Promise ভালো
```

---

<a id="p2-promise"></a>
**Topic 8: Promise**

**Promise কী:**
Async operation-এর eventual completion/failure represent করে। 3 states: pending, fulfilled, rejected।

```javascript
// ────────────────────────────────────────────
// Promise তৈরি করুন
// ────────────────────────────────────────────
function readUserFromDB(userId) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            if (userId <= 0) {
                reject(new Error('Invalid user ID'));
            } else {
                resolve({ id: userId, name: 'Alice' });
            }
        }, 100);
    });
}

// ────────────────────────────────────────────
// Promise chaining — Callback Hell solve হয়!
// ────────────────────────────────────────────
readUserFromDB(1)
    .then(user => getProfile(user.id))
    .then(profile => getOrders(profile.id))
    .then(orders => processOrders(orders))
    .then(result => sendEmail('alice@example.com', result))
    .then(() => console.log('Done!'))
    .catch(err => console.error('Error:', err.message))
    .finally(() => console.log('Cleanup'));

// ────────────────────────────────────────────
// Promise.all — সব parallel-এ, সবগুলো শেষ হলে resolve
// ────────────────────────────────────────────
const [user, posts, orders] = await Promise.all([
    fetchUser(1),
    fetchPosts(1),
    fetchOrders(1)
]);
// 3টি parallel request — fastest of sequential!

// ────────────────────────────────────────────
// Promise.allSettled — সব complete হওয়ার পরে, fail হলেও
// ────────────────────────────────────────────
const results = await Promise.allSettled([
    fetchUser(1),
    fetchUser(999),    // might fail
    fetchPosts(1)
]);
results.forEach(result => {
    if (result.status === 'fulfilled') {
        console.log('Success:', result.value);
    } else {
        console.log('Failed:', result.reason.message);
    }
});

// ────────────────────────────────────────────
// Promise.race — যে আগে resolve/reject করবে
// ────────────────────────────────────────────
const timeout = new Promise((_, reject) =>
    setTimeout(() => reject(new Error('Timeout')), 5000)
);
const result = await Promise.race([fetchData(), timeout]);

// ────────────────────────────────────────────
// Promise.any — যে আগে resolve করবে (reject ignore)
// ────────────────────────────────────────────
const fastest = await Promise.any([
    fetchFromServer1(),
    fetchFromServer2(),
    fetchFromServer3()
]);
// যেটা আগে সফল হবে সেটার result পাবেন
```

---

<a id="p2-async-await"></a>
**Topic 9: async/await**

**async/await কী:**
Promise-এর উপর syntactic sugar। async code synchronous-এর মতো দেখতে হয়।

```javascript
// ────────────────────────────────────────────
// Basic syntax
// ────────────────────────────────────────────
async function fetchUserData(userId) {
    const user = await readUserFromDB(userId);     // Promise resolve পর্যন্ত wait
    const profile = await getProfile(user.id);
    const orders = await getOrders(profile.id);
    return { user, profile, orders };
}

// ────────────────────────────────────────────
// Sequential vs Parallel
// ────────────────────────────────────────────
// ❌ Sequential (slow — 3×100ms = 300ms)
async function sequential() {
    const user    = await fetchUser(1);     // wait 100ms
    const posts   = await fetchPosts(1);    // wait 100ms
    const orders  = await fetchOrders(1);   // wait 100ms
    return { user, posts, orders };
}

// ✅ Parallel (fast — ~100ms total)
async function parallel() {
    const [user, posts, orders] = await Promise.all([
        fetchUser(1),
        fetchPosts(1),
        fetchOrders(1)
    ]);
    return { user, posts, orders };
}

// ────────────────────────────────────────────
// Error handling
// ────────────────────────────────────────────
async function safeGetUser(userId) {
    try {
        const user = await readUserFromDB(userId);
        return user;
    } catch (err) {
        if (err.message === 'Invalid user ID') {
            return null;  // graceful fallback
        }
        throw err;  // unexpected errors re-throw
    }
}

// ────────────────────────────────────────────
// Loop-এ async
// ────────────────────────────────────────────
const userIds = [1, 2, 3, 4, 5];

// ❌ forEach কাজ করে না (await ignore হয়)
userIds.forEach(async (id) => {
    const user = await fetchUser(id);  // Not properly awaited!
});

// ✅ for...of (sequential)
for (const id of userIds) {
    const user = await fetchUser(id);
    console.log(user);
}

// ✅ Promise.all (parallel)
const users = await Promise.all(userIds.map(id => fetchUser(id)));

// ────────────────────────────────────────────
// Top-level await (ES Modules only)
// ────────────────────────────────────────────
// In .mjs file or "type": "module" package:
const config = await loadConfig();
const db = await connectDB(config);
```

---

<a id="p2-error"></a>
**Topic 10: Error Handling in Async Code**

```javascript
// ────────────────────────────────────────────
// Custom Error classes
// ────────────────────────────────────────────
class AppError extends Error {
    constructor(message, statusCode = 500, code = 'INTERNAL_ERROR') {
        super(message);
        this.name = this.constructor.name;
        this.statusCode = statusCode;
        this.code = code;
        Error.captureStackTrace(this, this.constructor);
    }
}

class NotFoundError extends AppError {
    constructor(resource) {
        super(`${resource} not found`, 404, 'NOT_FOUND');
    }
}

class ValidationError extends AppError {
    constructor(message) {
        super(message, 400, 'VALIDATION_ERROR');
    }
}

// Usage
async function getUser(id) {
    const user = await db.findById(id);
    if (!user) throw new NotFoundError('User');
    return user;
}

// ────────────────────────────────────────────
// Async wrapper (DRY error handling)
// ────────────────────────────────────────────
function asyncWrapper(fn) {
    return (req, res, next) => {
        Promise.resolve(fn(req, res, next)).catch(next);
    };
}

// Express route-এ:
router.get('/users/:id', asyncWrapper(async (req, res) => {
    const user = await getUser(req.params.id);
    res.json(user);
}));

// ────────────────────────────────────────────
// Unhandled Promise rejections
// ────────────────────────────────────────────
process.on('unhandledRejection', (reason, promise) => {
    console.error('Unhandled Rejection:', reason);
    // Log করুন, gracefully shutdown করুন
    process.exit(1);
});

process.on('uncaughtException', (err) => {
    console.error('Uncaught Exception:', err);
    // Cleanup করুন
    process.exit(1);
});

// ────────────────────────────────────────────
// Retry mechanism
// ────────────────────────────────────────────
async function withRetry(fn, maxRetries = 3, delay = 1000) {
    for (let attempt = 1; attempt <= maxRetries; attempt++) {
        try {
            return await fn();
        } catch (err) {
            if (attempt === maxRetries) throw err;
            console.log(`Attempt ${attempt} failed, retrying in ${delay}ms...`);
            await new Promise(resolve => setTimeout(resolve, delay * attempt));
        }
    }
}

// Usage
const data = await withRetry(() => fetchFromExternalAPI());

// ────────────────────────────────────────────
// Timeout wrapper
// ────────────────────────────────────────────
function withTimeout(promise, ms) {
    const timeout = new Promise((_, reject) =>
        setTimeout(() => reject(new Error(`Timeout after ${ms}ms`)), ms)
    );
    return Promise.race([promise, timeout]);
}

const result = await withTimeout(fetchData(), 5000);
```

---

<a id="p2-qa"></a>
**Topic 11: PART 2 Interview Q&A**

```
প্রশ্ন: Callback, Promise, async/await-এর পার্থক্য এবং কোনটা কখন?
উত্তর:
Callback: Node.js tradition, error-first convention। পুরোনো API-তে।
Nested হলে Callback Hell হয়।

Promise: .then()/.catch() chaining। Cleaner, composable।
Promise.all দিয়ে parallel execution।

async/await: Promise-এর syntactic sugar। Most readable।
আজকাল সব নতুন code-এ এটাই use করি।

Conversion: util.promisify() দিয়ে callback → Promise।

প্রশ্ন: Promise.all ও Promise.allSettled-এর পার্থক্য?
উত্তর:
Promise.all: একটি fail করলে immediately reject। সব succeed করলে resolve।
Best for: সব চাই, একটা fail হলে সব বাদ।

Promise.allSettled: সব complete হওয়ার পরে result array দেয়।
প্রতিটি: { status: 'fulfilled', value } বা { status: 'rejected', reason }
Best for: সব results চাই, failures সহ।

প্রশ্ন: Stream কেন ব্যবহার করব?
উত্তর: Large files memory-তে না এনে piece-by-piece process করতে।
1GB file পুরো RAM-এ না নিয়ে 64KB chunks-এ process করা যায়।
HTTP response stream করা যায় — faster TTFB।
pipe() দিয়ে streams chain করা যায়।

প্রশ্ন: EventEmitter-এ 'error' event handle না করলে কী হয়?
উত্তর: Uncaught exception → process crash।
সবসময় emitter.on('error', handler) দিতে হবে।

প্রশ্ন: async function ভেতরে forEach-এ await কাজ করে না কেন?
উত্তর: forEach callback-কে await করে না। Promise resolve হওয়ার আগেই
loop শেষ হয়ে যায়।
Solution: for...of loop (sequential) বা Promise.all + map (parallel)।

প্রশ্ন: process.nextTick ও setImmediate-এর পার্থক্য?
উত্তর:
process.nextTick: Current operation শেষে, event loop phase-এর আগে।
সর্বোচ্চ priority।

setImmediate: I/O poll phase-এর পরে check phase-এ।
I/O callback-এর মধ্যে setImmediate সবসময় setTimeout(0) এর আগে।
```

---

**PART 2 Quick Revision Table**

| Module/Concept | মূল কথা |
|----------------|---------|
| `fs.readFile` | Async file read — callback version |
| `fs.promises.readFile` | Async file read — Promise version |
| `path.join` | Cross-platform path build করুন |
| `path.resolve` | Absolute path তৈরি করুন |
| `os.cpus().length` | CPU core count |
| EventEmitter | Observer pattern — on/emit/off |
| `emitter.on('error')` | MUST handle — না হলে crash |
| Stream | Large data — chunks-এ process |
| pipe() | Streams connect করুন |
| Callback | Error-first convention |
| Promise.all | Parallel, সব succeed চাই |
| Promise.allSettled | Parallel, failures সহ সব চাই |
| async/await | Most readable — Promise wrapper |
| for...of + await | Sequential async loop |
| withRetry | Transient error handle |
| unhandledRejection | Process-level error catch |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 3 — Express.js Fundamentals *(Next request এ লিখব)*
