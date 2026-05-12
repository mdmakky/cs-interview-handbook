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

> **📌 পরবর্তী:** PART 3 — Express.js Fundamentals

---

<a id="part3"></a>
## PART 3: Express.js Fundamentals

> Node.js-এর সবচেয়ে popular web framework। Routing, Middleware, Request/Response handling, Template Engines এবং static files — সব কিছু এক জায়গায়।

| # | বিষয় |
|---|-------|
| 1 | [Express.js কী? কেন ব্যবহার করি](#p3-intro) |
| 2 | [Installation ও Hello World](#p3-setup) |
| 3 | [Routing — Basic ও Advanced](#p3-routing) |
| 4 | [Middleware — Concept ও Types](#p3-middleware) |
| 5 | [Request Object (req)](#p3-request) |
| 6 | [Response Object (res)](#p3-response) |
| 7 | [Error Handling Middleware](#p3-error) |
| 8 | [Static Files ও Template Engines](#p3-static) |
| 9 | [Router — Modular Routing](#p3-router) |
| 10 | [Environment Variables ও dotenv](#p3-env) |
| 11 | [Complete Express App Structure](#p3-structure) |
| 12 | [PART 3 Interview Q&A](#p3-qa) |

---

<a id="p3-intro"></a>
**Topic 1: Express.js কী? কেন ব্যবহার করি**

**Express.js কী:**
Express.js হলো Node.js-এর জন্য একটি **minimal, unopinionated web framework**। HTTP server তৈরি করা, routing, middleware — সব সহজ করে দেয়।

```
Raw Node.js HTTP server:
- Manual routing (if/else)
- Manual request body parsing
- Manual headers set করা
- কোনো middleware system নেই

Express.js:
✅ Declarative routing
✅ Middleware pipeline
✅ Request body auto-parsing
✅ Error handling built-in
✅ Huge ecosystem (passport, multer, cors…)
```

**Express vs Alternatives:**

| Framework | Style | Use Case |
|-----------|-------|----------|
| Express | Minimal, flexible | General purpose, REST API |
| Fastify | High performance | High-throughput APIs |
| Koa | Modern, async-first | Successor to Express (same team) |
| NestJS | Opinionated, TypeScript | Enterprise, structured |
| Hapi | Configuration-driven | Secure APIs |

---

<a id="p3-setup"></a>
**Topic 2: Installation ও Hello World**

```bash
mkdir my-express-app && cd my-express-app
npm init -y
npm install express
npm install -D nodemon
```

**Minimal app:**
```javascript
// src/app.js
const express = require('express');
const app = express();

// Middleware — JSON body parse করুন
app.use(express.json());
app.use(express.urlencoded({ extended: true }));

// Route
app.get('/', (req, res) => {
    res.json({ message: 'Hello from Express!' });
});

module.exports = app;

// src/index.js
const app = require('./app');
const PORT = process.env.PORT || 3000;

const server = app.listen(PORT, () => {
    console.log(`Server running on http://localhost:${PORT}`);
});

// Graceful shutdown
process.on('SIGTERM', () => {
    server.close(() => {
        console.log('Server shut down');
        process.exit(0);
    });
});
```

**package.json scripts:**
```json
{
  "scripts": {
    "start": "node src/index.js",
    "dev": "nodemon src/index.js",
    "test": "jest"
  }
}
```

---

<a id="p3-routing"></a>
**Topic 3: Routing — Basic ও Advanced**

**Basic routing:**
```javascript
// HTTP Methods
app.get('/users', (req, res) => { ... });       // GET
app.post('/users', (req, res) => { ... });      // POST
app.put('/users/:id', (req, res) => { ... });   // PUT (full update)
app.patch('/users/:id', (req, res) => { ... }); // PATCH (partial)
app.delete('/users/:id', (req, res) => { ... }); // DELETE
app.all('/users', (req, res) => { ... });       // সব methods

// Route parameters
app.get('/users/:id', (req, res) => {
    const { id } = req.params;
    res.json({ userId: id });
});

// Multiple parameters
app.get('/users/:userId/posts/:postId', (req, res) => {
    const { userId, postId } = req.params;
    res.json({ userId, postId });
});

// Optional parameter
app.get('/users/:id?', (req, res) => {
    if (req.params.id) {
        res.json({ user: req.params.id });
    } else {
        res.json({ message: 'All users' });
    }
});

// Query strings
// GET /search?q=nodejs&page=2&limit=10
app.get('/search', (req, res) => {
    const { q, page = 1, limit = 10 } = req.query;
    res.json({ query: q, page: Number(page), limit: Number(limit) });
});

// Wildcard
app.get('/files/*', (req, res) => {
    const filePath = req.params[0];  // 'images/photo.jpg'
    res.json({ file: filePath });
});
```

**Route handlers — Multiple callbacks:**
```javascript
// Middleware + handler chain
function authenticate(req, res, next) {
    const token = req.headers.authorization;
    if (!token) return res.status(401).json({ error: 'Unauthorized' });
    next();  // পরের handler-এ যান
}

function validate(req, res, next) {
    if (!req.body.name) return res.status(400).json({ error: 'Name required' });
    next();
}

app.post('/users', authenticate, validate, async (req, res) => {
    // token check ✅, validation ✅ — এখানে main logic
    const user = await createUser(req.body);
    res.status(201).json(user);
});

// Array-এ pass করা যায়
const middlewares = [authenticate, validate];
app.post('/users', middlewares, handler);
```

---

<a id="p3-middleware"></a>
**Topic 4: Middleware — Concept ও Types**

**Middleware কী:**
Request → [middleware 1] → [middleware 2] → [middleware 3] → Response

প্রতিটি middleware: `(req, res, next)` — request modify করতে পারে, response পাঠাতে পারে, অথবা `next()` call করে পরেরটিতে যেতে পারে।

```javascript
// ────────────────────────────────────────────
// Application-level middleware
// ────────────────────────────────────────────
// সব requests-এ apply হয়
app.use((req, res, next) => {
    console.log(`[${new Date().toISOString()}] ${req.method} ${req.url}`);
    next();  // পরের middleware/route-এ যান
});

// Specific path-এ apply
app.use('/api', (req, res, next) => {
    console.log('API request');
    next();
});

// ────────────────────────────────────────────
// Built-in middleware
// ────────────────────────────────────────────
app.use(express.json());                       // JSON body parse
app.use(express.urlencoded({ extended: true })); // Form data parse
app.use(express.static('public'));             // Static files

// ────────────────────────────────────────────
// Third-party middleware
// ────────────────────────────────────────────
const cors = require('cors');
const morgan = require('morgan');
const helmet = require('helmet');
const compression = require('compression');
const rateLimit = require('express-rate-limit');

app.use(cors({
    origin: process.env.FRONTEND_URL || 'http://localhost:3000',
    credentials: true
}));
app.use(morgan('dev'));        // HTTP request logging
app.use(helmet());             // Security headers
app.use(compression());        // Response compression

const limiter = rateLimit({
    windowMs: 15 * 60 * 1000, // 15 minutes
    max: 100,                  // 100 requests per window
    message: { error: 'Too many requests' }
});
app.use('/api', limiter);

// ────────────────────────────────────────────
// Custom middleware examples
// ────────────────────────────────────────────

// Request ID (tracing)
const { v4: uuidv4 } = require('uuid');
app.use((req, res, next) => {
    req.id = uuidv4();
    res.setHeader('X-Request-Id', req.id);
    next();
});

// Request timing
app.use((req, res, next) => {
    req.startTime = Date.now();
    res.on('finish', () => {
        const duration = Date.now() - req.startTime;
        console.log(`${req.method} ${req.url} — ${res.statusCode} (${duration}ms)`);
    });
    next();
});

// Auth middleware
async function requireAuth(req, res, next) {
    try {
        const authHeader = req.headers.authorization;
        if (!authHeader || !authHeader.startsWith('Bearer ')) {
            return res.status(401).json({ error: 'No token provided' });
        }
        const token = authHeader.split(' ')[1];
        const payload = verifyToken(token);
        req.user = payload;
        next();
    } catch (err) {
        res.status(401).json({ error: 'Invalid token' });
    }
}

// Role check middleware (factory)
function requireRole(...roles) {
    return (req, res, next) => {
        if (!roles.includes(req.user?.role)) {
            return res.status(403).json({ error: 'Forbidden' });
        }
        next();
    };
}

// Usage
app.get('/admin', requireAuth, requireRole('admin'), handler);
app.get('/profile', requireAuth, requireRole('admin', 'user'), handler);
```

---

<a id="p3-request"></a>
**Topic 5: Request Object (req)**

```javascript
app.post('/users/:id/profile', (req, res) => {
    // ────────────────────────────────────────────
    // Route parameters — URL-এ :name
    // ────────────────────────────────────────────
    req.params.id          // '123'
    req.params             // { id: '123' }

    // ────────────────────────────────────────────
    // Query string — ?key=value
    // ────────────────────────────────────────────
    req.query.page         // '2'
    req.query              // { page: '2', limit: '10' }

    // ────────────────────────────────────────────
    // Request body — POST/PUT/PATCH body
    // ────────────────────────────────────────────
    req.body.name          // 'Alice'
    req.body               // { name: 'Alice', email: '...' }
    // দরকার: app.use(express.json())

    // ────────────────────────────────────────────
    // Headers
    // ────────────────────────────────────────────
    req.headers
    req.headers.authorization      // 'Bearer token...'
    req.get('Content-Type')        // 'application/json'
    req.get('User-Agent')

    // ────────────────────────────────────────────
    // URL Info
    // ────────────────────────────────────────────
    req.method             // 'POST'
    req.url                // '/users/123/profile?page=2'
    req.path               // '/users/123/profile'
    req.originalUrl        // full URL including mount path
    req.protocol           // 'http' or 'https'
    req.hostname           // 'localhost'
    req.ip                 // '127.0.0.1'
    req.secure             // true if HTTPS

    // ────────────────────────────────────────────
    // Content negotiation
    // ────────────────────────────────────────────
    req.accepts('json')    // 'json' if client accepts JSON
    req.is('application/json')  // content-type check

    // ────────────────────────────────────────────
    // Cookies (cookie-parser middleware দরকার)
    // ────────────────────────────────────────────
    req.cookies.sessionId

    // ────────────────────────────────────────────
    // Custom properties (middleware থেকে)
    // ────────────────────────────────────────────
    req.user               // auth middleware থেকে
    req.id                 // request ID middleware থেকে
});
```

---

<a id="p3-response"></a>
**Topic 6: Response Object (res)**

```javascript
app.get('/demo', (req, res) => {
    // ────────────────────────────────────────────
    // Status code set করুন
    // ────────────────────────────────────────────
    res.status(200)        // chainable
    res.statusCode = 200   // directly

    // ────────────────────────────────────────────
    // JSON response (API-এর জন্য সবচেয়ে common)
    // ────────────────────────────────────────────
    res.json({ message: 'OK', data: [] });
    res.status(201).json({ id: 1, name: 'Alice' });
    res.status(404).json({ error: 'Not Found' });

    // ────────────────────────────────────────────
    // Text / HTML
    // ────────────────────────────────────────────
    res.send('Hello World');                // text
    res.send('<h1>Hello</h1>');             // HTML (Content-Type auto-set)

    // ────────────────────────────────────────────
    // Redirect
    // ────────────────────────────────────────────
    res.redirect('/new-path');              // 302
    res.redirect(301, '/permanent-path');  // 301 permanent
    res.redirect('back');                  // referrer-এ ফিরুন

    // ────────────────────────────────────────────
    // Headers
    // ────────────────────────────────────────────
    res.set('X-Custom-Header', 'value');
    res.set({ 'Cache-Control': 'no-cache', 'X-Version': '1.0' });
    res.setHeader('Content-Type', 'application/json');
    res.append('Link', '<http://localhost/>; rel="index"');

    // ────────────────────────────────────────────
    // File download/send
    // ────────────────────────────────────────────
    res.sendFile('/absolute/path/to/file.pdf');
    res.download('/path/to/report.pdf', 'monthly-report.pdf');

    // ────────────────────────────────────────────
    // Cookies
    // ────────────────────────────────────────────
    res.cookie('sessionId', 'abc123', {
        httpOnly: true,     // JS থেকে access নেই
        secure: true,       // HTTPS only
        sameSite: 'strict', // CSRF protection
        maxAge: 7 * 24 * 60 * 60 * 1000  // 7 days ms
    });
    res.clearCookie('sessionId');

    // ────────────────────────────────────────────
    // End without body
    // ────────────────────────────────────────────
    res.status(204).end();  // No Content

    // ────────────────────────────────────────────
    // Streaming response
    // ────────────────────────────────────────────
    const fileStream = require('fs').createReadStream('large.txt');
    fileStream.pipe(res);
});
```

**Standard API response format:**
```javascript
// Success responses
const sendSuccess = (res, data, statusCode = 200) => {
    res.status(statusCode).json({
        success: true,
        data,
        timestamp: new Date().toISOString()
    });
};

// Error responses
const sendError = (res, message, statusCode = 500, code = null) => {
    res.status(statusCode).json({
        success: false,
        error: { message, code },
        timestamp: new Date().toISOString()
    });
};

// Usage
app.get('/users/:id', async (req, res) => {
    const user = await getUser(req.params.id);
    if (!user) return sendError(res, 'User not found', 404, 'USER_NOT_FOUND');
    sendSuccess(res, user);
});
```

---

<a id="p3-error"></a>
**Topic 7: Error Handling Middleware**

**Express error middleware — 4 parameters:**
```javascript
// src/middleware/errorHandler.js

// Custom error class
class AppError extends Error {
    constructor(message, statusCode = 500, code = 'INTERNAL_ERROR') {
        super(message);
        this.name = 'AppError';
        this.statusCode = statusCode;
        this.code = code;
        this.isOperational = true;  // expected errors
    }
}

// Error handling middleware — MUST be last
function errorHandler(err, req, res, next) {
    // Log করুন
    console.error(`[Error] ${req.method} ${req.url}:`, err.message);
    if (process.env.NODE_ENV === 'development') {
        console.error(err.stack);
    }

    // Operational errors (known errors — client-friendly message)
    if (err.isOperational) {
        return res.status(err.statusCode).json({
            success: false,
            error: { message: err.message, code: err.code }
        });
    }

    // MongoDB validation errors
    if (err.name === 'ValidationError') {
        const messages = Object.values(err.errors).map(e => e.message);
        return res.status(400).json({
            success: false,
            error: { message: 'Validation failed', details: messages }
        });
    }

    // Mongoose CastError (invalid ObjectId)
    if (err.name === 'CastError') {
        return res.status(400).json({
            success: false,
            error: { message: 'Invalid ID format' }
        });
    }

    // JWT errors
    if (err.name === 'JsonWebTokenError') {
        return res.status(401).json({
            success: false,
            error: { message: 'Invalid token' }
        });
    }
    if (err.name === 'TokenExpiredError') {
        return res.status(401).json({
            success: false,
            error: { message: 'Token expired' }
        });
    }

    // Duplicate key (MongoDB)
    if (err.code === 11000) {
        const field = Object.keys(err.keyValue)[0];
        return res.status(409).json({
            success: false,
            error: { message: `${field} already exists`, code: 'DUPLICATE_KEY' }
        });
    }

    // Unknown errors — generic message (security: don't expose internals)
    res.status(500).json({
        success: false,
        error: {
            message: process.env.NODE_ENV === 'development'
                ? err.message
                : 'Internal server error'
        }
    });
}

// 404 handler (routes-এর শেষে, errorHandler-এর আগে)
function notFoundHandler(req, res, next) {
    next(new AppError(`Route ${req.method} ${req.url} not found`, 404, 'NOT_FOUND'));
}

module.exports = { AppError, errorHandler, notFoundHandler };

// src/app.js-এ use করুন:
const { errorHandler, notFoundHandler } = require('./middleware/errorHandler');

// ... সব routes define করুন ...
app.use(notFoundHandler);    // 404 — routes-এর পরে
app.use(errorHandler);       // Error handler — সবার শেষে

// Async route-এ error throw করলে:
// asyncWrapper দরকার অথবা try/catch with next(err)
app.get('/users/:id', async (req, res, next) => {
    try {
        const user = await getUser(req.params.id);
        if (!user) throw new AppError('User not found', 404, 'NOT_FOUND');
        res.json(user);
    } catch (err) {
        next(err);  // errorHandler-এ পাঠান
    }
});

// asyncWrapper দিয়ে cleaner:
const asyncWrapper = fn => (req, res, next) =>
    Promise.resolve(fn(req, res, next)).catch(next);

app.get('/users/:id', asyncWrapper(async (req, res) => {
    const user = await getUser(req.params.id);
    if (!user) throw new AppError('User not found', 404, 'NOT_FOUND');
    res.json(user);
}));
```

---

<a id="p3-static"></a>
**Topic 8: Static Files ও Template Engines**

**Static Files:**
```javascript
// public/ folder থেকে static files serve করুন
app.use(express.static('public'));
// GET /images/logo.png → public/images/logo.png
// GET /css/style.css → public/css/style.css

// Virtual path prefix
app.use('/static', express.static('public'));
// GET /static/images/logo.png → public/images/logo.png

// Absolute path (recommended)
app.use(express.static(require('path').join(__dirname, 'public')));

// Multiple directories
app.use(express.static('public'));
app.use(express.static('uploads'));
// প্রথমে public, না পেলে uploads-এ খোঁজে

// Options
app.use(express.static('public', {
    maxAge: '1d',          // Browser cache 1 day
    etag: false,           // ETag disable
    index: 'index.html',   // default file
    dotfiles: 'deny'       // .env files block করুন
}));
```

**EJS Template Engine (REST API-তে কম দরকার, SSR-এ লাগে):**
```bash
npm install ejs
```

```javascript
app.set('view engine', 'ejs');
app.set('views', path.join(__dirname, 'views'));

// views/users.ejs
// <ul>
//   <% users.forEach(user => { %>
//     <li><%= user.name %></li>
//   <% }) %>
// </ul>

app.get('/users', async (req, res) => {
    const users = await getUsers();
    res.render('users', { users, title: 'User List' });
});
```

---

<a id="p3-router"></a>
**Topic 9: Router — Modular Routing**

```javascript
// src/routes/users.js
const express = require('express');
const router = express.Router();
const userController = require('../controllers/userController');
const { requireAuth } = require('../middleware/auth');

// GET /api/users
router.get('/', userController.getAll);

// GET /api/users/:id
router.get('/:id', userController.getById);

// POST /api/users
router.post('/', requireAuth, userController.create);

// PUT /api/users/:id
router.put('/:id', requireAuth, userController.update);

// DELETE /api/users/:id
router.delete('/:id', requireAuth, userController.remove);

module.exports = router;

// src/routes/auth.js
const express = require('express');
const router = express.Router();
const authController = require('../controllers/authController');

router.post('/register', authController.register);
router.post('/login', authController.login);
router.post('/logout', authController.logout);
router.post('/refresh', authController.refresh);

module.exports = router;

// src/app.js — mount করুন
const userRoutes = require('./routes/users');
const authRoutes = require('./routes/auth');

app.use('/api/users', userRoutes);   // /api/users/... → userRoutes
app.use('/api/auth', authRoutes);    // /api/auth/... → authRoutes

// Router-level middleware (শুধু এই router-এ apply)
router.use(requireAuth);  // সব routes-এ auth দরকার

// Route param middleware
router.param('id', async (req, res, next, id) => {
    // :id থাকা সব routes-এ automatically run হবে
    if (!id.match(/^[0-9a-fA-F]{24}$/)) {
        return res.status(400).json({ error: 'Invalid ID' });
    }
    next();
});
```

**Controller pattern:**
```javascript
// src/controllers/userController.js
const User = require('../models/User');
const { AppError } = require('../middleware/errorHandler');

exports.getAll = async (req, res, next) => {
    try {
        const { page = 1, limit = 10, sort = '-createdAt' } = req.query;
        const skip = (page - 1) * limit;

        const [users, total] = await Promise.all([
            User.find().sort(sort).skip(skip).limit(Number(limit)),
            User.countDocuments()
        ]);

        res.json({
            success: true,
            data: users,
            pagination: {
                page: Number(page),
                limit: Number(limit),
                total,
                pages: Math.ceil(total / limit)
            }
        });
    } catch (err) {
        next(err);
    }
};

exports.getById = async (req, res, next) => {
    try {
        const user = await User.findById(req.params.id);
        if (!user) throw new AppError('User not found', 404, 'NOT_FOUND');
        res.json({ success: true, data: user });
    } catch (err) {
        next(err);
    }
};

exports.create = async (req, res, next) => {
    try {
        const user = await User.create(req.body);
        res.status(201).json({ success: true, data: user });
    } catch (err) {
        next(err);
    }
};

exports.update = async (req, res, next) => {
    try {
        const user = await User.findByIdAndUpdate(
            req.params.id,
            req.body,
            { new: true, runValidators: true }
        );
        if (!user) throw new AppError('User not found', 404, 'NOT_FOUND');
        res.json({ success: true, data: user });
    } catch (err) {
        next(err);
    }
};

exports.remove = async (req, res, next) => {
    try {
        const user = await User.findByIdAndDelete(req.params.id);
        if (!user) throw new AppError('User not found', 404, 'NOT_FOUND');
        res.status(204).end();
    } catch (err) {
        next(err);
    }
};
```

---

<a id="p3-env"></a>
**Topic 10: Environment Variables ও dotenv**

```bash
npm install dotenv
```

```bash
# .env (gitignore-এ রাখুন!)
NODE_ENV=development
PORT=3000
MONGODB_URI=mongodb://localhost:27017/myapp
JWT_SECRET=your-super-secret-key-here
JWT_EXPIRES_IN=7d
FRONTEND_URL=http://localhost:3000
SMTP_HOST=smtp.gmail.com
SMTP_USER=your@gmail.com
SMTP_PASS=your-app-password

# .env.example (commit করুন — template)
NODE_ENV=development
PORT=3000
MONGODB_URI=mongodb://localhost:27017/your-app-name
JWT_SECRET=change-this-to-random-secret
JWT_EXPIRES_IN=7d
FRONTEND_URL=http://localhost:3000
```

```javascript
// src/config/env.js — validate ও export করুন
require('dotenv').config();

const required = ['MONGODB_URI', 'JWT_SECRET'];
const missing = required.filter(key => !process.env[key]);
if (missing.length) {
    throw new Error(`Missing required env vars: ${missing.join(', ')}`);
}

module.exports = {
    nodeEnv:     process.env.NODE_ENV || 'development',
    port:        parseInt(process.env.PORT) || 3000,
    mongoUri:    process.env.MONGODB_URI,
    jwtSecret:   process.env.JWT_SECRET,
    jwtExpiresIn: process.env.JWT_EXPIRES_IN || '7d',
    frontendUrl: process.env.FRONTEND_URL || 'http://localhost:3000',
    isDev:       process.env.NODE_ENV === 'development',
    isProd:      process.env.NODE_ENV === 'production',
};

// Usage
const config = require('./config/env');
app.listen(config.port, () => console.log(`Port: ${config.port}`));
```

---

<a id="p3-structure"></a>
**Topic 11: Complete Express App Structure**

```javascript
// src/app.js — সম্পূর্ণ setup
const express = require('express');
const cors = require('cors');
const morgan = require('morgan');
const helmet = require('helmet');
const compression = require('compression');
const rateLimit = require('express-rate-limit');
const path = require('path');

const config = require('./config/env');
const userRoutes = require('./routes/users');
const authRoutes = require('./routes/auth');
const { errorHandler, notFoundHandler } = require('./middleware/errorHandler');

const app = express();

// ────────────────────────────────────────────
// Security & utility middleware
// ────────────────────────────────────────────
app.use(helmet());
app.use(cors({ origin: config.frontendUrl, credentials: true }));
app.use(compression());

if (config.isDev) {
    app.use(morgan('dev'));
}

// ────────────────────────────────────────────
// Rate limiting
// ────────────────────────────────────────────
app.use('/api', rateLimit({
    windowMs: 15 * 60 * 1000,
    max: 100,
    standardHeaders: true,
    legacyHeaders: false,
}));

// ────────────────────────────────────────────
// Body parsing
// ────────────────────────────────────────────
app.use(express.json({ limit: '10kb' }));   // JSON body size limit
app.use(express.urlencoded({ extended: true }));

// ────────────────────────────────────────────
// Static files
// ────────────────────────────────────────────
app.use('/uploads', express.static(path.join(__dirname, '../uploads')));

// ────────────────────────────────────────────
// Health check
// ────────────────────────────────────────────
app.get('/health', (req, res) => {
    res.json({
        status: 'healthy',
        uptime: process.uptime(),
        timestamp: new Date().toISOString()
    });
});

// ────────────────────────────────────────────
// API routes
// ────────────────────────────────────────────
app.use('/api/auth', authRoutes);
app.use('/api/users', userRoutes);

// ────────────────────────────────────────────
// Error handlers (routes-এর পরে)
// ────────────────────────────────────────────
app.use(notFoundHandler);
app.use(errorHandler);

module.exports = app;
```

**Final project structure:**
```
my-express-app/
├── src/
│   ├── index.js              ← server start
│   ├── app.js                ← Express app, middleware
│   ├── config/
│   │   ├── env.js            ← env validation + export
│   │   └── database.js       ← DB connection
│   ├── routes/
│   │   ├── auth.js
│   │   └── users.js
│   ├── controllers/
│   │   ├── authController.js
│   │   └── userController.js
│   ├── models/
│   │   └── User.js
│   ├── middleware/
│   │   ├── auth.js           ← JWT verify
│   │   └── errorHandler.js   ← error middleware
│   ├── services/
│   │   ├── authService.js    ← business logic
│   │   └── userService.js
│   └── utils/
│       ├── asyncWrapper.js
│       └── sendEmail.js
├── tests/
│   ├── auth.test.js
│   └── users.test.js
├── uploads/                  ← user uploads (gitignore)
├── .env                      ← (gitignore!)
├── .env.example
├── .gitignore
├── package.json
└── README.md
```

---

<a id="p3-qa"></a>
**Topic 12: PART 3 Interview Q&A**

```
প্রশ্ন: Middleware কী? Express-এ middleware pipeline কীভাবে কাজ করে?
উত্তর: Middleware হলো (req, res, next) function। Request → Response-এর
মাঝে run হয়। next() call করলে পরের middleware-এ যায়, না করলে
pipeline থামে।

Use cases: Logging, auth check, body parsing, CORS, rate limiting।
Order গুরুত্বপূর্ণ — app.use() এর ক্রম অনুযায়ী run হয়।

প্রশ্ন: Error handling middleware কীভাবে কাজ করে?
উত্তর: (err, req, res, next) — 4 parameters। Express automatically
error middleware চিনে। সবার শেষে define করতে হয়।
next(err) call করলে normal middleware skip করে error handler-এ যায়।

প্রশ্ন: app.use() ও app.get() পার্থক্য?
উত্তর:
app.use(): সব HTTP methods, path prefix match।
/api → /api/users, /api/posts সব match করে।
app.get(): শুধু GET method, exact path।

প্রশ্ন: Express Router কেন ব্যবহার করি?
উত্তর: Code modularize করতে। প্রতিটি resource (users, posts, auth)
আলাদা router file-এ রাখি। app.js clean থাকে।
Team-এ কাজ সহজ হয় — আলাদা file, কম conflict।

প্রশ্ন: .env file কখনো commit করব না কেন?
উত্তর: Secrets (DB password, JWT secret, API keys) থাকে।
GitHub-এ গেলে publicly exposed হবে।
.gitignore-এ রাখুন, .env.example commit করুন।
CI/CD-এ secrets manager বা GitHub Secrets ব্যবহার করুন।

প্রশ্ন: Rate limiting কেন দরকার?
উত্তর: DDoS/brute force attack থেকে protect করতে।
একজন user নির্দিষ্ট সময়ে limited requests করতে পারবে।
express-rate-limit package সহজে setup করা যায়।
```

---

**PART 3 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| Middleware | `(req, res, next)` — pipeline |
| `app.use()` | All methods, prefix match |
| `app.get/post/put/delete` | Specific method + exact path |
| `express.json()` | JSON body parse করুন |
| `helmet()` | Security headers |
| `cors()` | Cross-Origin Resource Sharing |
| `rateLimit()` | DDoS/brute force protection |
| `req.params` | URL :parameters |
| `req.query` | ?key=value |
| `req.body` | POST body (json middleware দরকার) |
| `res.json()` | JSON response |
| `res.status(404).json()` | Status + JSON |
| Error middleware | 4 params — সবার শেষে |
| Router | Modular routing — separate files |
| `asyncWrapper` | try/catch + next(err) avoid করুন |
| `.env` | Secrets — never commit! |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part4"></a>
## PART 4: Database Integration (MongoDB ও PostgreSQL)

> Node.js-এ database connect করা, Mongoose ORM, raw PostgreSQL (pg), query patterns, connection pooling, transactions এবং best practices।

| # | বিষয় |
|---|-------|
| 1 | [MongoDB ও Mongoose Setup](#p4-mongo-setup) |
| 2 | [Mongoose Schema ও Model](#p4-schema) |
| 3 | [Mongoose CRUD Operations](#p4-mongoose-crud) |
| 4 | [Mongoose Advanced — Population, Aggregation](#p4-mongoose-advanced) |
| 5 | [PostgreSQL ও pg Library](#p4-postgres-setup) |
| 6 | [PostgreSQL CRUD ও Query Patterns](#p4-postgres-crud) |
| 7 | [Transactions](#p4-transactions) |
| 8 | [Connection Pooling](#p4-pooling) |
| 9 | [Query Builder — Knex.js](#p4-knex) |
| 10 | [ORM — Sequelize vs Prisma](#p4-orm) |
| 11 | [Database Best Practices](#p4-best-practices) |
| 12 | [PART 4 Interview Q&A](#p4-qa) |

---

<a id="p4-mongo-setup"></a>
**Topic 1: MongoDB ও Mongoose Setup**

```bash
npm install mongoose
```

```javascript
// src/config/database.js
const mongoose = require('mongoose');
const config = require('./env');

let isConnected = false;

async function connectDB() {
    if (isConnected) return;

    try {
        const conn = await mongoose.connect(config.mongoUri, {
            // Connection options (Mongoose 7+ এ কম দরকার)
            serverSelectionTimeoutMS: 5000,  // 5 seconds
            socketTimeoutMS: 45000,
        });

        isConnected = true;
        console.log(`MongoDB connected: ${conn.connection.host}`);

        // Connection events
        mongoose.connection.on('error', (err) => {
            console.error('MongoDB error:', err);
        });

        mongoose.connection.on('disconnected', () => {
            console.warn('MongoDB disconnected — reconnecting...');
            isConnected = false;
        });

    } catch (err) {
        console.error('MongoDB connection failed:', err.message);
        process.exit(1);
    }
}

async function disconnectDB() {
    await mongoose.connection.close();
    isConnected = false;
    console.log('MongoDB disconnected');
}

module.exports = { connectDB, disconnectDB };

// src/index.js-এ:
const { connectDB } = require('./config/database');
connectDB().then(() => {
    app.listen(config.port, () => console.log(`Server on port ${config.port}`));
});
```

---

<a id="p4-schema"></a>
**Topic 2: Mongoose Schema ও Model**

```javascript
// src/models/User.js
const mongoose = require('mongoose');
const bcrypt = require('bcryptjs');

const userSchema = new mongoose.Schema(
    {
        name: {
            type: String,
            required: [true, 'Name is required'],
            trim: true,
            minlength: [2, 'Name must be at least 2 characters'],
            maxlength: [50, 'Name cannot exceed 50 characters']
        },
        email: {
            type: String,
            required: [true, 'Email is required'],
            unique: true,
            lowercase: true,
            trim: true,
            match: [/^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/, 'Invalid email']
        },
        password: {
            type: String,
            required: [true, 'Password is required'],
            minlength: [8, 'Password must be at least 8 characters'],
            select: false  // find()-এ default-এ include হবে না
        },
        role: {
            type: String,
            enum: {
                values: ['user', 'admin', 'moderator'],
                message: 'Role must be user, admin, or moderator'
            },
            default: 'user'
        },
        age: {
            type: Number,
            min: [18, 'Must be at least 18'],
            max: [120, 'Age cannot exceed 120']
        },
        avatar: {
            type: String,
            default: null
        },
        isActive: {
            type: Boolean,
            default: true
        },
        lastLogin: Date,
        tags: [String],               // Array of strings
        address: {                    // Embedded document
            street: String,
            city: String,
            country: { type: String, default: 'Bangladesh' }
        },
        posts: [{                     // Reference to Post model
            type: mongoose.Schema.Types.ObjectId,
            ref: 'Post'
        }]
    },
    {
        timestamps: true,             // createdAt, updatedAt auto-add
        toJSON: {
            transform: (doc, ret) => {
                delete ret.password;  // JSON-এ password exclude
                delete ret.__v;
                return ret;
            }
        }
    }
);

// ────────────────────────────────────────────
// Indexes
// ────────────────────────────────────────────
userSchema.index({ email: 1 });               // Single field
userSchema.index({ name: 1, createdAt: -1 }); // Compound
userSchema.index({ email: 1 }, { unique: true }); // Unique (already via field)

// ────────────────────────────────────────────
// Pre hooks (middleware)
// ────────────────────────────────────────────
userSchema.pre('save', async function (next) {
    // Password change হলেই hash করুন
    if (!this.isModified('password')) return next();
    this.password = await bcrypt.hash(this.password, 12);
    next();
});

userSchema.pre(/^find/, function (next) {
    // সব find queries-এ inactive users filter করুন
    this.where({ isActive: true });
    next();
});

// ────────────────────────────────────────────
// Instance methods
// ────────────────────────────────────────────
userSchema.methods.comparePassword = async function (candidatePassword) {
    return bcrypt.compare(candidatePassword, this.password);
};

userSchema.methods.toSafeObject = function () {
    const obj = this.toObject();
    delete obj.password;
    return obj;
};

// ────────────────────────────────────────────
// Static methods
// ────────────────────────────────────────────
userSchema.statics.findByEmail = function (email) {
    return this.findOne({ email: email.toLowerCase() });
};

userSchema.statics.findActiveAdmins = function () {
    return this.find({ role: 'admin', isActive: true });
};

// ────────────────────────────────────────────
// Virtual fields (not stored in DB)
// ────────────────────────────────────────────
userSchema.virtual('fullProfile').get(function () {
    return `${this.name} (${this.role}) — ${this.email}`;
});

const User = mongoose.model('User', userSchema);
module.exports = User;
```

---

<a id="p4-mongoose-crud"></a>
**Topic 3: Mongoose CRUD Operations**

```javascript
const User = require('./models/User');

// ────────────────────────────────────────────
// CREATE
// ────────────────────────────────────────────
// Method 1: create()
const user = await User.create({
    name: 'Alice',
    email: 'alice@example.com',
    password: 'password123'
});

// Method 2: new + save()
const user2 = new User({ name: 'Bob', email: 'bob@example.com', password: 'pass' });
await user2.save();

// Bulk insert
await User.insertMany([
    { name: 'Charlie', email: 'charlie@example.com', password: 'pass' },
    { name: 'Diana', email: 'diana@example.com', password: 'pass' }
]);

// ────────────────────────────────────────────
// READ
// ────────────────────────────────────────────
// সব users
const users = await User.find();

// Filter
const admins = await User.find({ role: 'admin' });
const activeUsers = await User.find({ isActive: true, role: 'user' });

// Comparison operators
const seniors = await User.find({ age: { $gte: 30, $lte: 60 } });
const topRoles = await User.find({ role: { $in: ['admin', 'moderator'] } });

// One document
const user = await User.findOne({ email: 'alice@example.com' });
const userById = await User.findById('507f1f77bcf86cd799439011');

// Select specific fields (projection)
const users = await User.find().select('name email role -_id');
// name, email, role include; _id exclude

// Sort
const recent = await User.find().sort({ createdAt: -1 });
const alphabetical = await User.find().sort({ name: 1 });

// Pagination
const page = 2, limit = 10;
const users = await User.find()
    .sort({ createdAt: -1 })
    .skip((page - 1) * limit)
    .limit(limit);

const total = await User.countDocuments({ isActive: true });

// ────────────────────────────────────────────
// UPDATE
// ────────────────────────────────────────────
// findByIdAndUpdate — default: old document, { new: true } → new document
const updated = await User.findByIdAndUpdate(
    userId,
    { name: 'Alice Updated', lastLogin: new Date() },
    { new: true, runValidators: true }
);

// updateOne / updateMany
await User.updateOne({ email: 'alice@example.com' }, { $set: { isActive: false } });
await User.updateMany({ role: 'user' }, { $set: { tags: [] } });

// Update operators
await User.findByIdAndUpdate(userId, {
    $set:  { name: 'New Name' },     // field set করুন
    $push: { tags: 'nodejs' },       // array-এ add করুন
    $pull: { tags: 'old-tag' },      // array থেকে remove করুন
    $inc:  { loginCount: 1 },        // increment
    $unset: { avatar: '' }           // field delete করুন
});

// ────────────────────────────────────────────
// DELETE
// ────────────────────────────────────────────
await User.findByIdAndDelete(userId);
await User.deleteOne({ email: 'alice@example.com' });
await User.deleteMany({ isActive: false });

// Soft delete (best practice — actual delete করবেন না)
await User.findByIdAndUpdate(userId, {
    isActive: false,
    deletedAt: new Date()
});
```

---

<a id="p4-mongoose-advanced"></a>
**Topic 4: Mongoose Advanced — Population ও Aggregation**

**Population (JOIN equivalent):**
```javascript
// src/models/Post.js
const postSchema = new mongoose.Schema({
    title: { type: String, required: true },
    content: String,
    author: { type: mongoose.Schema.Types.ObjectId, ref: 'User', required: true },
    comments: [{
        user: { type: mongoose.Schema.Types.ObjectId, ref: 'User' },
        text: String,
        createdAt: { type: Date, default: Date.now }
    }],
    tags: [String],
    published: { type: Boolean, default: false }
}, { timestamps: true });

const Post = mongoose.model('Post', postSchema);

// Population — reference ID → actual document
const post = await Post.findById(postId).populate('author', 'name email avatar');
// post.author এখন User object, _id নয়

// Multiple populate
const post = await Post.findById(postId)
    .populate('author', 'name email')
    .populate('comments.user', 'name avatar');

// Nested populate
const posts = await Post.find({ published: true })
    .populate({
        path: 'author',
        select: 'name email',
        populate: {
            path: 'address',  // author-এর address-ও populate
            select: 'city country'
        }
    });
```

**Aggregation Pipeline:**
```javascript
// MongoDB aggregation — powerful data transformation
const stats = await User.aggregate([
    // Stage 1: Filter
    { $match: { isActive: true } },

    // Stage 2: Group by role, count করুন
    { $group: {
        _id: '$role',
        count: { $sum: 1 },
        avgAge: { $avg: '$age' }
    }},

    // Stage 3: Sort
    { $sort: { count: -1 } },

    // Stage 4: Rename fields
    { $project: {
        role: '$_id',
        count: 1,
        avgAge: { $round: ['$avgAge', 1] },
        _id: 0
    }}
]);
// [{ role: 'user', count: 150, avgAge: 28.5 }, { role: 'admin', count: 5, avgAge: 32.0 }]

// Lookup (JOIN)
const postsWithAuthors = await Post.aggregate([
    { $match: { published: true } },
    { $lookup: {
        from: 'users',
        localField: 'author',
        foreignField: '_id',
        as: 'authorInfo'
    }},
    { $unwind: '$authorInfo' },
    { $project: {
        title: 1,
        'authorInfo.name': 1,
        'authorInfo.email': 1,
        createdAt: 1
    }}
]);

// Pagination with total count
const result = await Post.aggregate([
    { $match: { published: true } },
    { $facet: {
        data: [
            { $sort: { createdAt: -1 } },
            { $skip: (page - 1) * limit },
            { $limit: limit }
        ],
        total: [{ $count: 'count' }]
    }}
]);
const posts = result[0].data;
const total = result[0].total[0]?.count || 0;
```

---

<a id="p4-postgres-setup"></a>
**Topic 5: PostgreSQL ও pg Library**

```bash
npm install pg
```

```javascript
// src/config/postgres.js
const { Pool } = require('pg');
const config = require('./env');

const pool = new Pool({
    connectionString: config.postgresUri,
    // অথবা individual fields:
    // host: 'localhost',
    // port: 5432,
    // database: 'myapp',
    // user: 'postgres',
    // password: 'password',

    max: 20,                    // pool size
    idleTimeoutMillis: 30000,   // idle connection timeout
    connectionTimeoutMillis: 2000,  // connection timeout

    // SSL (production)
    ssl: config.isProd ? { rejectUnauthorized: false } : false
});

// Connection test
pool.on('connect', () => {
    console.log('PostgreSQL connected');
});

pool.on('error', (err) => {
    console.error('PostgreSQL pool error:', err);
});

async function testConnection() {
    try {
        const client = await pool.connect();
        const result = await client.query('SELECT NOW() as now');
        console.log('DB time:', result.rows[0].now);
        client.release();
    } catch (err) {
        console.error('PostgreSQL connection failed:', err.message);
        process.exit(1);
    }
}

module.exports = { pool, testConnection };
```

---

<a id="p4-postgres-crud"></a>
**Topic 6: PostgreSQL CRUD ও Query Patterns**

```javascript
const { pool } = require('./config/postgres');

// ────────────────────────────────────────────
// CREATE TABLE (migration)
// ────────────────────────────────────────────
await pool.query(`
    CREATE TABLE IF NOT EXISTS users (
        id SERIAL PRIMARY KEY,
        name VARCHAR(50) NOT NULL,
        email VARCHAR(255) UNIQUE NOT NULL,
        password_hash VARCHAR(255) NOT NULL,
        role VARCHAR(20) DEFAULT 'user' CHECK (role IN ('user', 'admin', 'moderator')),
        is_active BOOLEAN DEFAULT TRUE,
        created_at TIMESTAMPTZ DEFAULT NOW(),
        updated_at TIMESTAMPTZ DEFAULT NOW()
    )
`);

// Index
await pool.query('CREATE INDEX IF NOT EXISTS idx_users_email ON users(email)');

// ────────────────────────────────────────────
// INSERT (Parameterized — SQL injection safe!)
// ────────────────────────────────────────────
const insertResult = await pool.query(
    'INSERT INTO users (name, email, password_hash, role) VALUES ($1, $2, $3, $4) RETURNING *',
    ['Alice', 'alice@example.com', hashedPassword, 'user']
);
const newUser = insertResult.rows[0];

// ────────────────────────────────────────────
// SELECT
// ────────────────────────────────────────────
// সব users
const allUsers = await pool.query('SELECT id, name, email, role FROM users');
const users = allUsers.rows;

// By ID
const userResult = await pool.query(
    'SELECT id, name, email, role FROM users WHERE id = $1',
    [userId]
);
const user = userResult.rows[0];  // undefined if not found

// Filtering + Pagination
const { rows: users, rowCount } = await pool.query(
    `SELECT id, name, email, role, created_at
     FROM users
     WHERE is_active = true AND role = $1
     ORDER BY created_at DESC
     LIMIT $2 OFFSET $3`,
    [role, limit, (page - 1) * limit]
);

const countResult = await pool.query(
    'SELECT COUNT(*) as total FROM users WHERE is_active = true AND role = $1',
    [role]
);
const total = parseInt(countResult.rows[0].total);

// ────────────────────────────────────────────
// UPDATE
// ────────────────────────────────────────────
const updateResult = await pool.query(
    `UPDATE users SET name = $1, updated_at = NOW() WHERE id = $2 RETURNING *`,
    ['Alice Updated', userId]
);
if (updateResult.rowCount === 0) throw new AppError('User not found', 404);
const updatedUser = updateResult.rows[0];

// ────────────────────────────────────────────
// DELETE
// ────────────────────────────────────────────
const deleteResult = await pool.query(
    'DELETE FROM users WHERE id = $1 RETURNING id',
    [userId]
);
if (deleteResult.rowCount === 0) throw new AppError('User not found', 404);

// Soft delete
await pool.query(
    'UPDATE users SET is_active = false, updated_at = NOW() WHERE id = $1',
    [userId]
);

// ────────────────────────────────────────────
// JOIN
// ────────────────────────────────────────────
const postsWithAuthors = await pool.query(`
    SELECT
        p.id, p.title, p.created_at,
        u.name as author_name, u.email as author_email
    FROM posts p
    INNER JOIN users u ON p.author_id = u.id
    WHERE p.published = true
    ORDER BY p.created_at DESC
    LIMIT $1
`, [limit]);
```

---

<a id="p4-transactions"></a>
**Topic 7: Transactions**

**MongoDB transactions:**
```javascript
const session = await mongoose.startSession();
session.startTransaction();

try {
    // Debit sender
    await Account.findByIdAndUpdate(
        senderId,
        { $inc: { balance: -amount } },
        { session, new: true }
    );

    // Credit receiver
    await Account.findByIdAndUpdate(
        receiverId,
        { $inc: { balance: amount } },
        { session, new: true }
    );

    // Transaction log
    await Transaction.create([{
        from: senderId, to: receiverId, amount, type: 'transfer'
    }], { session });

    await session.commitTransaction();
    console.log('Transfer successful');

} catch (err) {
    await session.abortTransaction();
    console.error('Transfer failed, rolled back:', err.message);
    throw err;
} finally {
    session.endSession();
}
```

**PostgreSQL transactions:**
```javascript
async function transfer(senderId, receiverId, amount) {
    const client = await pool.connect();

    try {
        await client.query('BEGIN');

        // Debit with lock
        const senderResult = await client.query(
            'SELECT balance FROM accounts WHERE id = $1 FOR UPDATE',
            [senderId]
        );

        if (senderResult.rows[0].balance < amount) {
            throw new AppError('Insufficient balance', 400);
        }

        await client.query(
            'UPDATE accounts SET balance = balance - $1 WHERE id = $2',
            [amount, senderId]
        );

        await client.query(
            'UPDATE accounts SET balance = balance + $1 WHERE id = $2',
            [amount, receiverId]
        );

        await client.query(
            'INSERT INTO transactions (from_id, to_id, amount) VALUES ($1, $2, $3)',
            [senderId, receiverId, amount]
        );

        await client.query('COMMIT');
        return { success: true };

    } catch (err) {
        await client.query('ROLLBACK');
        throw err;
    } finally {
        client.release();  // pool-এ ফিরিয়ে দিন
    }
}
```

---

<a id="p4-pooling"></a>
**Topic 8: Connection Pooling**

```
Connection pooling ছাড়া:
- প্রতিটি request → নতুন DB connection open → query → close
- Overhead: connection establishment time (~50-100ms)
- DB-এ too many connections error

Connection Pool:
- App start → N connections create → pool-এ রাখো
- Request → pool থেকে connection নাও → query → pool-এ ফেরাও
- Fast (0ms connection overhead), controlled concurrency
```

```javascript
// MongoDB — Mongoose automatically pools (default 5)
mongoose.connect(uri, {
    maxPoolSize: 10,     // max connections
    minPoolSize: 2,      // min connections
    serverSelectionTimeoutMS: 5000,
    socketTimeoutMS: 45000,
});

// PostgreSQL — pg Pool
const pool = new Pool({
    max: 20,                    // max pool size
    min: 2,                     // min pool size
    idleTimeoutMillis: 10000,   // idle connection close
    connectionTimeoutMillis: 3000,
});

// Pool events monitoring
pool.on('acquire', (client) => {
    // client pool থেকে নেওয়া হয়েছে
});
pool.on('remove', (client) => {
    // client pool থেকে সরানো হয়েছে
});

// Pool stats
console.log(`Total: ${pool.totalCount}`);
console.log(`Idle: ${pool.idleCount}`);
console.log(`Waiting: ${pool.waitingCount}`);
```

---

<a id="p4-knex"></a>
**Topic 9: Query Builder — Knex.js**

```bash
npm install knex pg
npx knex init  # knexfile.js তৈরি হবে
```

```javascript
// knexfile.js
module.exports = {
    development: {
        client: 'postgresql',
        connection: process.env.DATABASE_URL,
        pool: { min: 2, max: 10 },
        migrations: { tableName: 'knex_migrations', directory: './migrations' },
        seeds: { directory: './seeds' }
    }
};

// src/config/knex.js
const knex = require('knex')(require('../../knexfile')[process.env.NODE_ENV || 'development']);
module.exports = knex;

// Usage — type-safe, chainable queries
const db = require('./config/knex');

// SELECT
const users = await db('users')
    .select('id', 'name', 'email')
    .where({ is_active: true, role: 'user' })
    .orderBy('created_at', 'desc')
    .limit(10)
    .offset(0);

// INSERT
const [user] = await db('users').insert({
    name: 'Alice',
    email: 'alice@example.com',
    password_hash: hashedPassword
}).returning('*');

// UPDATE
const [updated] = await db('users')
    .where({ id: userId })
    .update({ name: 'Updated', updated_at: db.fn.now() })
    .returning('*');

// DELETE
await db('users').where({ id: userId }).delete();

// JOIN
const posts = await db('posts as p')
    .join('users as u', 'p.author_id', 'u.id')
    .select('p.id', 'p.title', 'u.name as author_name')
    .where('p.published', true);

// Raw query
const result = await db.raw(
    'SELECT * FROM users WHERE email = ? AND is_active = ?',
    ['alice@example.com', true]
);

// Migration তৈরি করুন
// npx knex migrate:make create_users_table
// migrations/20260513_create_users_table.js
exports.up = (knex) => knex.schema.createTable('users', (table) => {
    table.increments('id').primary();
    table.string('name', 50).notNullable();
    table.string('email', 255).notNullable().unique();
    table.string('password_hash', 255).notNullable();
    table.enum('role', ['user', 'admin']).defaultTo('user');
    table.boolean('is_active').defaultTo(true);
    table.timestamps(true, true);  // created_at, updated_at
});

exports.down = (knex) => knex.schema.dropTable('users');

// Run migrations
// npx knex migrate:latest
// npx knex migrate:rollback
```

---

<a id="p4-orm"></a>
**Topic 10: ORM — Sequelize vs Prisma**

**Sequelize (traditional ORM):**
```javascript
// npm install sequelize pg pg-hstore
const { Sequelize, DataTypes, Model } = require('sequelize');

const sequelize = new Sequelize(process.env.DATABASE_URL, {
    dialect: 'postgres',
    logging: false,
    pool: { max: 10, min: 2 }
});

class User extends Model {}
User.init({
    name: { type: DataTypes.STRING(50), allowNull: false },
    email: { type: DataTypes.STRING, allowNull: false, unique: true },
    role: { type: DataTypes.ENUM('user', 'admin'), defaultValue: 'user' }
}, { sequelize, modelName: 'User' });

// CRUD
const user = await User.create({ name: 'Alice', email: 'alice@example.com' });
const users = await User.findAll({ where: { role: 'user' }, limit: 10 });
const found = await User.findByPk(1);
await User.update({ name: 'Bob' }, { where: { id: 1 } });
await User.destroy({ where: { id: 1 } });
```

**Prisma (modern ORM — type-safe):**
```bash
npm install @prisma/client
npm install -D prisma
npx prisma init
```

```prisma
// prisma/schema.prisma
model User {
  id        Int      @id @default(autoincrement())
  name      String   @db.VarChar(50)
  email     String   @unique
  role      Role     @default(USER)
  posts     Post[]
  createdAt DateTime @default(now())
  updatedAt DateTime @updatedAt
}

enum Role {
  USER
  ADMIN
}
```

```javascript
const { PrismaClient } = require('@prisma/client');
const prisma = new PrismaClient();

// TypeScript-friendly, auto-completion সহ
const user = await prisma.user.create({
    data: { name: 'Alice', email: 'alice@example.com' }
});

const users = await prisma.user.findMany({
    where: { role: 'USER' },
    select: { id: true, name: true, email: true },
    orderBy: { createdAt: 'desc' },
    take: 10, skip: 0
});

const updated = await prisma.user.update({
    where: { id: userId },
    data: { name: 'Updated' }
});

await prisma.user.delete({ where: { id: userId } });

// Relations
const usersWithPosts = await prisma.user.findMany({
    include: { posts: { where: { published: true } } }
});
```

**Comparison:**

| | Mongoose | pg (raw) | Knex | Sequelize | Prisma |
|---|---|---|---|---|---|
| DB | MongoDB only | PostgreSQL | Multi-DB | Multi-DB | Multi-DB |
| Type safety | Moderate | Manual | Moderate | Moderate | ✅ Excellent |
| Learning curve | Easy | Easy | Easy | Medium | Easy |
| Migrations | Manual | Manual | ✅ Built-in | ✅ Built-in | ✅ Built-in |
| Performance | Good | Best | Good | Good | Good |

---

<a id="p4-best-practices"></a>
**Topic 11: Database Best Practices**

```javascript
// ────────────────────────────────────────────
// 1. Parameterized queries — SQL injection prevent
// ────────────────────────────────────────────
// ❌ NEVER — SQL injection vulnerable!
const userId = req.params.id;
await pool.query(`SELECT * FROM users WHERE id = ${userId}`);
// userId = "1 OR 1=1" → সব user data leak!

// ✅ Always parameterized
await pool.query('SELECT * FROM users WHERE id = $1', [userId]);

// ────────────────────────────────────────────
// 2. Sensitive fields exclude করুন
// ────────────────────────────────────────────
// Mongoose
const user = await User.findById(id).select('-password -__v');

// PostgreSQL
await pool.query('SELECT id, name, email, role FROM users WHERE id = $1', [id]);
// ❌ SELECT * — password সহ সব আসবে

// ────────────────────────────────────────────
// 3. Indexes — performance critical
// ────────────────────────────────────────────
// Frequently queried fields-এ index দিন
userSchema.index({ email: 1 });
userSchema.index({ createdAt: -1 });
userSchema.index({ role: 1, isActive: 1 });  // compound

// ────────────────────────────────────────────
// 4. Connection error gracefully handle করুন
// ────────────────────────────────────────────
mongoose.connection.on('error', (err) => {
    console.error('DB Error:', err);
    // Alert send করুন (Sentry, PagerDuty)
});

// ────────────────────────────────────────────
// 5. Lean queries (MongoDB performance)
// ────────────────────────────────────────────
// .lean() — plain JS object return করে, Mongoose document নয়
// toJSON(), save() methods নেই — but faster, less memory
const users = await User.find().lean();

// Read-only queries-এ lean() ব্যবহার করুন
const user = await User.findById(id).lean();

// ────────────────────────────────────────────
// 6. Limit query results
// ────────────────────────────────────────────
// ❌ Return all records
const allUsers = await User.find();

// ✅ Always paginate
const users = await User.find().limit(50).skip(page * 50);
// Max limit enforce করুন
const safeLimit = Math.min(Number(req.query.limit) || 10, 100);

// ────────────────────────────────────────────
// 7. Database secrets secure রাখুন
// ────────────────────────────────────────────
// .env-এ রাখুন, never hardcode
// Production-এ secrets manager ব্যবহার করুন

// ────────────────────────────────────────────
// 8. Graceful shutdown — connections close করুন
// ────────────────────────────────────────────
process.on('SIGTERM', async () => {
    await mongoose.connection.close();
    await pool.end();
    process.exit(0);
});
```

---

<a id="p4-qa"></a>
**Topic 12: PART 4 Interview Q&A**

```
প্রশ্ন: MongoDB ও PostgreSQL কখন কোনটা?
উত্তর:
MongoDB (NoSQL):
→ Flexible schema — data structure পরিবর্তন হয়
→ Hierarchical/nested data (blog posts with comments)
→ Horizontal scaling দরকার
→ Real-time apps, catalogs, content management

PostgreSQL (SQL):
→ Structured data, strict schema
→ Complex relations, JOINs দরকার
→ ACID transactions critical (banking, e-commerce)
→ Reporting, analytics

প্রশ্ন: Mongoose-এ populate কীভাবে কাজ করে? JOIN-এর সাথে পার্থক্য?
উত্তর: populate() reference ObjectId → actual document করে।
এটি আসলে 2টি separate query — প্রথমে main document, তারপর
referenced documents।

SQL JOIN server-side single query-এ data combine করে।
MongoDB Atlas আসল $lookup aggregation করে, populate() করে না।

প্রশ্ন: SQL injection কীভাবে prevent করবেন?
উত্তর: Parameterized queries সবসময়।
pg: query('SELECT ... WHERE id = $1', [id])
Knex/Sequelize/Prisma automatically handle করে।
Never string concatenation করবেন না।

প্রশ্ন: Connection pooling কেন দরকার?
উত্তর: প্রতিটি request-এ নতুন connection খুলতে 50-100ms লাগে।
Pool: N connections আগে থেকে তৈরি রাখে।
Request → pool থেকে connection নাও → use করো → ফেরাও।
Fast, controlled concurrency, DB overload prevent।

প্রশ্ন: Transaction কখন দরকার?
উত্তর: Multiple operations atomically run করতে — সব succeed বা সব fail।
Bank transfer: debit + credit — একটি fail হলে দুটোই rollback।
Order placement: inventory decrease + order create + payment।
Data consistency critical যেখানে।

প্রশ্ন: MongoDB-তে index না থাকলে কী হয়?
উত্তর: Collection scan (COLLSCAN) — সব documents check করে।
Millions of documents → very slow।
Frequently queried fields-এ index দিলে index scan (IXSCAN) → fast।
explain() দিয়ে query plan দেখা যায়।
Tradeoff: Index → faster read, slower write (index update), বেশি storage।
```

---

**PART 4 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| Mongoose connect | `mongoose.connect(uri, options)` |
| Schema | Type, validation, hooks, indexes define |
| `pre('save')` | Save হওয়ার আগে hook — password hash |
| `select: false` | Field normally exclude (password) |
| `.populate()` | ObjectId → actual document (2 queries) |
| `.lean()` | Plain JS object — faster read-only |
| Aggregation | Pipeline — match, group, sort, project |
| pg Pool | `new Pool({max: 20})` — connection pool |
| Parameterized | `$1, $2` — SQL injection prevent |
| Transaction (Mongo) | `session.startTransaction()` |
| Transaction (pg) | `BEGIN / COMMIT / ROLLBACK` |
| `FOR UPDATE` | Row-level lock in PostgreSQL |
| Knex | Query builder — chainable, multi-DB |
| Prisma | Modern ORM — type-safe, migrations |
| Soft delete | `is_active = false` — data preserve |
| Connection pool | Pre-created connections — fast reuse |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 5 — Authentication ও Authorization *(Next request এ লিখব)*
