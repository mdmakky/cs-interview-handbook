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

> **📌 পরবর্তী:** PART 5 — Authentication ও Authorization

---

<a id="part5"></a>
## PART 5: Authentication ও Authorization

> JWT, bcrypt, session-based auth, OAuth2, refresh tokens, role-based access control — সব কিছু practical code সহ।

| # | বিষয় |
|---|-------|
| 1 | [Authentication vs Authorization](#p5-concepts) |
| 2 | [Password Hashing — bcrypt](#p5-bcrypt) |
| 3 | [JWT — JSON Web Token](#p5-jwt) |
| 4 | [Registration ও Login Flow](#p5-auth-flow) |
| 5 | [Refresh Token Pattern](#p5-refresh) |
| 6 | [Session-based Authentication](#p5-session) |
| 7 | [OAuth2 ও Social Login](#p5-oauth) |
| 8 | [Role-Based Access Control (RBAC)](#p5-rbac) |
| 9 | [Auth Security Best Practices](#p5-security) |
| 10 | [PART 5 Interview Q&A](#p5-qa) |

---

<a id="p5-concepts"></a>
**Topic 1: Authentication vs Authorization**

```
Authentication (AuthN) — "তুমি কে?"
→ Identity verify করা
→ Login: email + password → "হ্যাঁ, এই user আছে"
→ Examples: username/password, biometric, OTP, SSO

Authorization (AuthZ) — "তুমি কী করতে পারবে?"
→ Permission check করা
→ "এই user কি admin dashboard দেখতে পারবে?"
→ Examples: RBAC, ABAC, ACL, Policies

Flow:
Request → Authentication (valid user?) → Authorization (permission?) → Resource
```

**Common auth strategies:**
```
1. Session-based   — Server-side session store, cookie (traditional)
2. JWT             — Stateless token, client stores (modern REST API)
3. API Key         — Long-lived key (machine-to-machine)
4. OAuth2          — Third-party login (Google, GitHub)
5. mTLS            — Certificate-based (microservices)
```

---

<a id="p5-bcrypt"></a>
**Topic 2: Password Hashing — bcrypt**

```bash
npm install bcryptjs
```

```javascript
const bcrypt = require('bcryptjs');

// ────────────────────────────────────────────
// Hash password (Registration-এ)
// ────────────────────────────────────────────
async function hashPassword(plainPassword) {
    const saltRounds = 12;  // cost factor — higher = slower = more secure
    // saltRounds 10 → ~100ms, 12 → ~400ms, 14 → ~1.5s
    const hash = await bcrypt.hash(plainPassword, saltRounds);
    return hash;
    // '$2a$12$N9qo8uLOickgx2ZMRZoMyeIjZAgcfl7p92ldGxad68LJZdL17lhWy'
}

// ────────────────────────────────────────────
// Verify password (Login-এ)
// ────────────────────────────────────────────
async function verifyPassword(plainPassword, hashedPassword) {
    const isMatch = await bcrypt.compare(plainPassword, hashedPassword);
    return isMatch;  // true or false
}

// ────────────────────────────────────────────
// Mongoose pre-hook-এ (PART 4 এ দেখেছিলাম)
// ────────────────────────────────────────────
userSchema.pre('save', async function (next) {
    if (!this.isModified('password')) return next();
    this.password = await bcrypt.hash(this.password, 12);
    next();
});

// ────────────────────────────────────────────
// কেন plain MD5/SHA1 নয়?
// ────────────────────────────────────────────
// MD5/SHA1: Fast → rainbow table attack possible
// bcrypt: Intentionally slow + salt → brute force infeasible
// Salt: প্রতিটি hash-এ random value — same password, different hash

console.log(await bcrypt.hash('password123', 10));
// '$2a$10$...' (different each time due to random salt)
console.log(await bcrypt.hash('password123', 10));
// '$2a$10$...' (different again!)
// compare() salt extract করে automatically verify করে
```

---

<a id="p5-jwt"></a>
**Topic 3: JWT — JSON Web Token**

```bash
npm install jsonwebtoken
```

**JWT structure:**
```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkFsaWNlIiwicm9sZSI6InVzZXIiLCJpYXQiOjE3MTU1MDAwMDAsImV4cCI6MTcxNjEwNDgwMH0.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c

Header.Payload.Signature

Header:  { "alg": "HS256", "typ": "JWT" }
Payload: { "sub": "user_id", "name": "Alice", "role": "user", "iat": ..., "exp": ... }
Signature: HMACSHA256(base64(header) + "." + base64(payload), secret)
```

```javascript
const jwt = require('jsonwebtoken');
const config = require('./config/env');

// ────────────────────────────────────────────
// Token generate করুন
// ────────────────────────────────────────────
function generateAccessToken(user) {
    return jwt.sign(
        {
            sub: user._id.toString(),   // subject — user ID
            email: user.email,
            role: user.role
        },
        config.jwtSecret,
        {
            expiresIn: '15m',           // Access token: short-lived
            issuer: 'my-app',
            audience: 'my-app-users'
        }
    );
}

function generateRefreshToken(user) {
    return jwt.sign(
        { sub: user._id.toString() },
        config.jwtRefreshSecret,
        { expiresIn: '7d' }             // Refresh token: long-lived
    );
}

// ────────────────────────────────────────────
// Token verify করুন
// ────────────────────────────────────────────
function verifyAccessToken(token) {
    try {
        return jwt.verify(token, config.jwtSecret, {
            issuer: 'my-app',
            audience: 'my-app-users'
        });
        // Returns: { sub: '...', email: '...', role: '...', iat: ..., exp: ... }
    } catch (err) {
        if (err.name === 'TokenExpiredError') {
            throw new AppError('Token expired', 401, 'TOKEN_EXPIRED');
        }
        if (err.name === 'JsonWebTokenError') {
            throw new AppError('Invalid token', 401, 'INVALID_TOKEN');
        }
        throw err;
    }
}

// ────────────────────────────────────────────
// Auth middleware
// ────────────────────────────────────────────
async function requireAuth(req, res, next) {
    try {
        // Header থেকে token extract করুন
        const authHeader = req.headers.authorization;
        if (!authHeader || !authHeader.startsWith('Bearer ')) {
            return res.status(401).json({ error: 'No token provided' });
        }

        const token = authHeader.substring(7);  // 'Bearer ' remove
        const payload = verifyAccessToken(token);

        // User DB থেকে load করুন (optional — payload-এ enough info থাকলে skip)
        // const user = await User.findById(payload.sub);
        // if (!user || !user.isActive) return res.status(401).json({ error: 'User not found' });

        req.user = {
            id: payload.sub,
            email: payload.email,
            role: payload.role
        };

        next();
    } catch (err) {
        next(err);
    }
}

module.exports = { generateAccessToken, generateRefreshToken, verifyAccessToken, requireAuth };
```

---

<a id="p5-auth-flow"></a>
**Topic 4: Registration ও Login Flow**

```javascript
// src/services/authService.js
const User = require('../models/User');
const { generateAccessToken, generateRefreshToken } = require('../utils/jwt');
const { AppError } = require('../middleware/errorHandler');

// ────────────────────────────────────────────
// Registration
// ────────────────────────────────────────────
async function register(name, email, password) {
    // 1. Email already exists?
    const existing = await User.findOne({ email: email.toLowerCase() });
    if (existing) {
        throw new AppError('Email already registered', 409, 'DUPLICATE_EMAIL');
    }

    // 2. User create করুন (password Mongoose pre-hook-এ hash হবে)
    const user = await User.create({ name, email, password });

    // 3. Tokens generate করুন
    const accessToken = generateAccessToken(user);
    const refreshToken = generateRefreshToken(user);

    // 4. Refresh token DB-তে save করুন (revocation-এর জন্য)
    user.refreshToken = refreshToken;
    await user.save({ validateBeforeSave: false });

    return {
        user: user.toSafeObject(),
        accessToken,
        refreshToken
    };
}

// ────────────────────────────────────────────
// Login
// ────────────────────────────────────────────
async function login(email, password) {
    // 1. User খুঁজুন (password select করুন — normally hidden)
    const user = await User.findOne({ email: email.toLowerCase() })
                           .select('+password');

    if (!user) {
        // Timing attack prevent: always compare (even if user not found)
        await bcrypt.compare(password, '$2a$12$dummy.hash.to.prevent.timing');
        throw new AppError('Invalid email or password', 401, 'INVALID_CREDENTIALS');
    }

    // 2. Password verify করুন
    const isValid = await user.comparePassword(password);
    if (!isValid) {
        throw new AppError('Invalid email or password', 401, 'INVALID_CREDENTIALS');
    }

    // 3. Account active?
    if (!user.isActive) {
        throw new AppError('Account is deactivated', 403, 'ACCOUNT_INACTIVE');
    }

    // 4. Last login update করুন
    user.lastLogin = new Date();
    await user.save({ validateBeforeSave: false });

    // 5. Tokens generate করুন
    const accessToken = generateAccessToken(user);
    const refreshToken = generateRefreshToken(user);

    user.refreshToken = refreshToken;
    await user.save({ validateBeforeSave: false });

    return {
        user: user.toSafeObject(),
        accessToken,
        refreshToken
    };
}

// ────────────────────────────────────────────
// Controller
// ────────────────────────────────────────────
// src/controllers/authController.js
exports.register = async (req, res, next) => {
    try {
        const { name, email, password } = req.body;
        const result = await authService.register(name, email, password);

        // Refresh token HttpOnly cookie-তে
        res.cookie('refreshToken', result.refreshToken, {
            httpOnly: true,
            secure: config.isProd,
            sameSite: 'strict',
            maxAge: 7 * 24 * 60 * 60 * 1000  // 7 days
        });

        res.status(201).json({
            success: true,
            data: {
                user: result.user,
                accessToken: result.accessToken  // client localStorage/memory-তে রাখবে
            }
        });
    } catch (err) {
        next(err);
    }
};

exports.login = async (req, res, next) => {
    try {
        const { email, password } = req.body;
        const result = await authService.login(email, password);

        res.cookie('refreshToken', result.refreshToken, {
            httpOnly: true, secure: config.isProd, sameSite: 'strict',
            maxAge: 7 * 24 * 60 * 60 * 1000
        });

        res.json({
            success: true,
            data: { user: result.user, accessToken: result.accessToken }
        });
    } catch (err) {
        next(err);
    }
};

exports.logout = async (req, res, next) => {
    try {
        // DB থেকে refresh token remove করুন
        await User.findByIdAndUpdate(req.user.id, { $unset: { refreshToken: 1 } });

        res.clearCookie('refreshToken');
        res.json({ success: true, message: 'Logged out' });
    } catch (err) {
        next(err);
    }
};
```

---

<a id="p5-refresh"></a>
**Topic 5: Refresh Token Pattern**

```
কেন Refresh Token?
Access Token: short-lived (15min) → secure কিন্তু frequent re-login
Refresh Token: long-lived (7d) → new access token পেতে ব্যবহার করি

Flow:
1. Login → access_token (15min) + refresh_token (7d, httpOnly cookie)
2. API call → Bearer access_token
3. Access token expire → 401
4. POST /auth/refresh → cookie-তে refresh_token পাঠাও
5. Server verify refresh_token → নতুন access_token return করো
6. Retry original API call
```

```javascript
// src/controllers/authController.js
exports.refresh = async (req, res, next) => {
    try {
        // HttpOnly cookie থেকে refresh token
        const refreshToken = req.cookies.refreshToken;
        if (!refreshToken) {
            return res.status(401).json({ error: 'No refresh token' });
        }

        // Verify refresh token
        let payload;
        try {
            payload = jwt.verify(refreshToken, config.jwtRefreshSecret);
        } catch {
            return res.status(401).json({ error: 'Invalid refresh token' });
        }

        // User exists এবং token matches?
        const user = await User.findById(payload.sub).select('+refreshToken');
        if (!user || user.refreshToken !== refreshToken) {
            return res.status(401).json({ error: 'Refresh token revoked' });
        }

        // নতুন access token generate করুন
        const newAccessToken = generateAccessToken(user);

        // Token rotation (optional, more secure)
        const newRefreshToken = generateRefreshToken(user);
        user.refreshToken = newRefreshToken;
        await user.save({ validateBeforeSave: false });

        res.cookie('refreshToken', newRefreshToken, {
            httpOnly: true, secure: config.isProd, sameSite: 'strict',
            maxAge: 7 * 24 * 60 * 60 * 1000
        });

        res.json({
            success: true,
            data: { accessToken: newAccessToken }
        });
    } catch (err) {
        next(err);
    }
};
```

**Token storage best practice:**
```
Access Token:
✅ Memory (JS variable) — most secure, lost on page refresh
✅ sessionStorage — tab closes-এ lost
❌ localStorage — XSS-এ vulnerable (avoid for sensitive apps)

Refresh Token:
✅ HttpOnly Cookie — JS access নেই, XSS safe
   CSRF protection: sameSite: 'strict' বা CSRF token
❌ localStorage — XSS-এ vulnerable
```

---

<a id="p5-session"></a>
**Topic 6: Session-based Authentication**

```bash
npm install express-session connect-mongo
```

```javascript
const session = require('express-session');
const MongoStore = require('connect-mongo');

app.use(session({
    secret: config.sessionSecret,
    resave: false,
    saveUninitialized: false,
    store: MongoStore.create({
        mongoUrl: config.mongoUri,
        ttl: 7 * 24 * 60 * 60,  // 7 days
        touchAfter: 24 * 3600    // 24h-এ একবার update (performance)
    }),
    cookie: {
        httpOnly: true,
        secure: config.isProd,
        sameSite: 'strict',
        maxAge: 7 * 24 * 60 * 60 * 1000  // 7 days
    },
    name: 'sessionId'  // default 'connect.sid' চেঞ্জ করুন
}));

// Login — session create করুন
app.post('/login', async (req, res) => {
    const { email, password } = req.body;
    const user = await User.findOne({ email }).select('+password');
    if (!user || !await user.comparePassword(password)) {
        return res.status(401).json({ error: 'Invalid credentials' });
    }

    req.session.userId = user._id.toString();
    req.session.role = user.role;

    res.json({ success: true, user: user.toSafeObject() });
});

// Auth middleware
async function requireAuth(req, res, next) {
    if (!req.session.userId) {
        return res.status(401).json({ error: 'Not authenticated' });
    }
    req.user = { id: req.session.userId, role: req.session.role };
    next();
}

// Logout — session destroy করুন
app.post('/logout', (req, res) => {
    req.session.destroy((err) => {
        if (err) return res.status(500).json({ error: 'Logout failed' });
        res.clearCookie('sessionId');
        res.json({ success: true });
    });
});
```

**JWT vs Session:**

| | JWT | Session |
|---|---|---|
| Storage | Client (token) | Server (session store) |
| Scalability | ✅ Stateless — horizontal scale সহজ | ❌ Shared store দরকার (Redis) |
| Revocation | ❌ কঠিন (blacklist বা short expiry) | ✅ সহজ (session delete) |
| Size | Larger payload | Small cookie ID |
| Best for | REST API, microservices | Traditional web app, SSR |

---

<a id="p5-oauth"></a>
**Topic 7: OAuth2 ও Social Login**

```bash
npm install passport passport-google-oauth20 passport-jwt
```

**OAuth2 Flow:**
```
1. User "Login with Google" click করে
2. App → Google Authorization URL redirect করে
3. User Google-এ login করে, permission দেয়
4. Google → App-এর callback URL-এ authorization code পাঠায়
5. App → Google-এ code + client_secret দিয়ে access_token চায়
6. Google → access_token + user info দেয়
7. App নিজের user create/find করে, নিজের session/JWT দেয়
```

```javascript
const passport = require('passport');
const GoogleStrategy = require('passport-google-oauth20').Strategy;

passport.use(new GoogleStrategy(
    {
        clientID: config.googleClientId,
        clientSecret: config.googleClientSecret,
        callbackURL: `${config.apiUrl}/auth/google/callback`
    },
    async (accessToken, refreshToken, profile, done) => {
        try {
            // User DB-তে আছে?
            let user = await User.findOne({ googleId: profile.id });

            if (!user) {
                // Email দিয়ে existing user খুঁজুন
                user = await User.findOne({ email: profile.emails[0].value });

                if (user) {
                    // Existing user-এ googleId connect করুন
                    user.googleId = profile.id;
                    await user.save();
                } else {
                    // নতুন user তৈরি করুন
                    user = await User.create({
                        name: profile.displayName,
                        email: profile.emails[0].value,
                        googleId: profile.id,
                        avatar: profile.photos[0]?.value,
                        password: crypto.randomBytes(32).toString('hex')
                    });
                }
            }

            done(null, user);
        } catch (err) {
            done(err, null);
        }
    }
));

// Routes
app.get('/auth/google',
    passport.authenticate('google', { scope: ['profile', 'email'] })
);

app.get('/auth/google/callback',
    passport.authenticate('google', { session: false }),
    async (req, res) => {
        const accessToken = generateAccessToken(req.user);
        const refreshToken = generateRefreshToken(req.user);

        // Refresh token cookie-তে
        res.cookie('refreshToken', refreshToken, { httpOnly: true, secure: true });

        // Frontend-এ redirect করুন access token সহ
        res.redirect(`${config.frontendUrl}/auth/callback?token=${accessToken}`);
    }
);
```

---

<a id="p5-rbac"></a>
**Topic 8: Role-Based Access Control (RBAC)**

```javascript
// ────────────────────────────────────────────
// Simple role middleware
// ────────────────────────────────────────────
function requireRole(...roles) {
    return (req, res, next) => {
        if (!req.user) {
            return res.status(401).json({ error: 'Not authenticated' });
        }
        if (!roles.includes(req.user.role)) {
            return res.status(403).json({ error: 'Forbidden — insufficient role' });
        }
        next();
    };
}

// Usage
app.get('/admin/users', requireAuth, requireRole('admin'), handler);
app.get('/dashboard', requireAuth, requireRole('admin', 'moderator'), handler);
app.get('/profile', requireAuth, requireRole('admin', 'moderator', 'user'), handler);

// ────────────────────────────────────────────
// Permission-based RBAC (more granular)
// ────────────────────────────────────────────
const PERMISSIONS = {
    admin:     ['read:users', 'write:users', 'delete:users', 'read:reports', 'write:settings'],
    moderator: ['read:users', 'write:users', 'read:reports'],
    user:      ['read:users']
};

function requirePermission(permission) {
    return (req, res, next) => {
        const userPermissions = PERMISSIONS[req.user?.role] || [];
        if (!userPermissions.includes(permission)) {
            return res.status(403).json({
                error: 'Forbidden',
                required: permission
            });
        }
        next();
    };
}

// Usage
app.delete('/users/:id', requireAuth, requirePermission('delete:users'), handler);
app.get('/reports', requireAuth, requirePermission('read:reports'), handler);

// ────────────────────────────────────────────
// Resource ownership check
// ────────────────────────────────────────────
async function requireOwnerOrAdmin(req, res, next) {
    const resource = await User.findById(req.params.id);
    if (!resource) {
        return res.status(404).json({ error: 'Not found' });
    }

    const isOwner = resource._id.toString() === req.user.id;
    const isAdmin = req.user.role === 'admin';

    if (!isOwner && !isAdmin) {
        return res.status(403).json({ error: 'Forbidden' });
    }

    req.resource = resource;  // next handler-এ পাবে
    next();
}

app.put('/users/:id', requireAuth, requireOwnerOrAdmin, updateHandler);
```

---

<a id="p5-security"></a>
**Topic 9: Auth Security Best Practices**

```javascript
// ────────────────────────────────────────────
// 1. Input validation (express-validator)
// ────────────────────────────────────────────
const { body, validationResult } = require('express-validator');

const registerValidation = [
    body('name').trim().isLength({ min: 2, max: 50 }).withMessage('Name: 2-50 chars'),
    body('email').isEmail().normalizeEmail().withMessage('Invalid email'),
    body('password')
        .isLength({ min: 8 })
        .matches(/^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)/)
        .withMessage('Password: 8+ chars, uppercase, lowercase, number')
];

const validate = (req, res, next) => {
    const errors = validationResult(req);
    if (!errors.isEmpty()) {
        return res.status(400).json({ errors: errors.array() });
    }
    next();
};

app.post('/register', registerValidation, validate, registerHandler);

// ────────────────────────────────────────────
// 2. Rate limiting for auth routes (brute force prevent)
// ────────────────────────────────────────────
const loginLimiter = rateLimit({
    windowMs: 15 * 60 * 1000,  // 15 minutes
    max: 5,                      // 5 attempts
    skipSuccessfulRequests: true,
    message: { error: 'Too many login attempts, try again in 15 minutes' }
});

app.post('/auth/login', loginLimiter, loginHandler);

// ────────────────────────────────────────────
// 3. Timing attack prevention
// ────────────────────────────────────────────
// ❌ User not found → fast response; wrong password → slow bcrypt compare
// → attacker can tell if email exists
// ✅ Always run bcrypt compare (same time regardless)
const dummyHash = '$2a$12$LRezBexLNmMobHj3GYFiLuNfFhOmgNiDJFE.WL0.cJW5v9OAFhnuO';
if (!user) {
    await bcrypt.compare(password, dummyHash);  // prevent timing attack
    throw new AppError('Invalid credentials', 401);
}

// ────────────────────────────────────────────
// 4. Account lockout
// ────────────────────────────────────────────
userSchema.add({
    loginAttempts: { type: Number, default: 0 },
    lockUntil: { type: Date }
});

userSchema.methods.incLoginAttempts = async function () {
    if (this.lockUntil && this.lockUntil > Date.now()) return; // already locked
    this.loginAttempts += 1;
    if (this.loginAttempts >= 5) {
        this.lockUntil = new Date(Date.now() + 30 * 60 * 1000); // 30 min lock
    }
    await this.save();
};

// ────────────────────────────────────────────
// 5. Password reset (secure)
// ────────────────────────────────────────────
const crypto = require('crypto');

async function requestPasswordReset(email) {
    const user = await User.findOne({ email });
    if (!user) return;  // Don't reveal if email exists

    // Cryptographically secure random token
    const resetToken = crypto.randomBytes(32).toString('hex');
    const hashedToken = crypto.createHash('sha256').update(resetToken).digest('hex');

    user.passwordResetToken = hashedToken;   // DB-তে hash store করুন
    user.passwordResetExpiry = new Date(Date.now() + 10 * 60 * 1000);  // 10 min
    await user.save({ validateBeforeSave: false });

    // Email-এ plain token পাঠান (URL-এ)
    const resetUrl = `${config.frontendUrl}/reset-password?token=${resetToken}`;
    await sendEmail({ to: email, subject: 'Password Reset', text: resetUrl });
}

async function resetPassword(plainToken, newPassword) {
    const hashedToken = crypto.createHash('sha256').update(plainToken).digest('hex');
    const user = await User.findOne({
        passwordResetToken: hashedToken,
        passwordResetExpiry: { $gt: Date.now() }
    });
    if (!user) throw new AppError('Invalid or expired reset token', 400);

    user.password = newPassword;
    user.passwordResetToken = undefined;
    user.passwordResetExpiry = undefined;
    await user.save();
}

// ────────────────────────────────────────────
// 6. HTTPS only in production
// ────────────────────────────────────────────
if (config.isProd) {
    app.use((req, res, next) => {
        if (req.header('x-forwarded-proto') !== 'https') {
            return res.redirect(`https://${req.header('host')}${req.url}`);
        }
        next();
    });
}
```

---

<a id="p5-qa"></a>
**Topic 10: PART 5 Interview Q&A**

```
প্রশ্ন: JWT কীভাবে কাজ করে? এর সুবিধা ও অসুবিধা?
উত্তর: JWT = Header.Payload.Signature।
Server secret দিয়ে sign করে। Verify করতে secret লাগে।
Payload publicly readable (base64) — sensitive data রাখবেন না।

সুবিধা: Stateless — DB check ছাড়া verify, horizontal scaling।
অসুবিধা: Revocation কঠিন — logout করলেও token valid থাকে expiry পর্যন্ত।
Solution: Short expiry (15min) + refresh token + blacklist (Redis)।

প্রশ্ন: bcrypt-এ salt rounds কেন?
উত্তর: Salt rounds মানে hashing কতবার repeat হবে। 12 মানে 2^12 = 4096 বার।
বেশি rounds → slower → brute force expensive।
Salt: প্রতিটি hash-এ random — same password, different hash → rainbow table useless।

প্রশ্ন: Refresh token কেন HttpOnly cookie-তে রাখি?
উত্তর: HttpOnly cookie JS থেকে access করা যায় না।
XSS attack হলেও document.cookie দিয়ে refresh token চুরি করা যাবে না।
Access token memory/sessionStorage-এ রাখলে XSS-এ চুরি হতে পারে,
কিন্তু short-lived হওয়ায় damage কম।

প্রশ্ন: Token revocation কীভাবে করবেন?
উত্তর: Options:
1. Short expiry (15min) — tolerable risk
2. Redis blacklist — logout-এ token blacklist করুন
3. Version number — user-এ tokenVersion field, token-এ include।
   Logout-এ version increment → old tokens invalid
4. Refresh token rotation — প্রতিবার refresh-এ নতুন token

প্রশ্ন: OAuth2 ও JWT কি same?
উত্তর: না। OAuth2 হলো authorization framework (third-party access delegation)।
JWT হলো token format।
OAuth2 access token হিসেবে JWT ব্যবহার করা যায়।
"Login with Google" OAuth2 + OpenID Connect (authentication layer) ব্যবহার করে।

প্রশ্ন: RBAC ও ABAC পার্থক্য?
উত্তর:
RBAC (Role-Based): User-এর role দেখে permission দেয়।
Simple — admin, user, moderator।

ABAC (Attribute-Based): User, resource, environment attributes দেখে।
Complex — "user.department === resource.department && time.isBusinessHours"
Fine-grained control দরকার হলে ABAC।
```

---

**PART 5 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| Authentication | "তুমি কে?" — identity verify |
| Authorization | "কী করতে পারবে?" — permission check |
| bcrypt | Slow hash + salt — brute force prevent |
| salt rounds | 12 recommended — higher = slower |
| JWT | Header.Payload.Signature — stateless |
| `jwt.sign()` | Token generate |
| `jwt.verify()` | Token validate |
| Access token | Short-lived (15min) — Bearer header |
| Refresh token | Long-lived (7d) — HttpOnly cookie |
| Token rotation | Refresh করলে নতুন refresh token |
| Session-based | Server-side store — revocation সহজ |
| RBAC | Role দেখে permission |
| requirePermission | Granular permission check |
| Timing attack | Always bcrypt.compare, same response time |
| Password reset | Crypto random token + hash in DB |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part6"></a>
## PART 6: REST API Design ও Validation

> Professional REST API design principles, input validation, file upload, API versioning, documentation এবং testing-ready architecture।

| # | বিষয় |
|---|-------|
| 1 | [REST Principles ও Constraints](#p6-rest) |
| 2 | [HTTP Status Codes](#p6-status-codes) |
| 3 | [API Response Format Standards](#p6-response-format) |
| 4 | [Input Validation — express-validator](#p6-validation) |
| 5 | [Pagination, Filtering ও Sorting](#p6-pagination) |
| 6 | [File Upload — Multer](#p6-upload) |
| 7 | [API Versioning](#p6-versioning) |
| 8 | [API Documentation — Swagger/OpenAPI](#p6-docs) |
| 9 | [CORS Configuration](#p6-cors) |
| 10 | [Complete CRUD API Example](#p6-complete) |
| 11 | [PART 6 Interview Q&A](#p6-qa) |

---

<a id="p6-rest"></a>
**Topic 1: REST Principles ও Constraints**

**REST কী:**
Representational State Transfer — web service design architectural style।

**6 REST Constraints:**
```
1. Client-Server    — Frontend ও Backend আলাদা
2. Stateless        — প্রতিটি request self-contained, server state রাখে না
3. Cacheable        — Response cache করা যাবে
4. Uniform Interface— Consistent URL, HTTP methods, status codes
5. Layered System   — Load balancer, CDN, proxy — client জানে না
6. Code on Demand   — Optional: server JS send করতে পারে (rare)
```

**RESTful URL design:**
```
Resource: users

GET    /api/users              → সব users (list)
POST   /api/users              → নতুন user তৈরি
GET    /api/users/:id          → specific user
PUT    /api/users/:id          → user পুরোটা update
PATCH  /api/users/:id          → user partial update
DELETE /api/users/:id          → user delete

Nested resources:
GET    /api/users/:id/posts    → user-এর সব posts
POST   /api/users/:id/posts    → user-এর নতুন post
GET    /api/users/:id/posts/:postId → specific post

Actions (verb URL — শুধু যদি REST-এ fit না হয়):
POST   /api/users/:id/activate
POST   /api/users/:id/deactivate
POST   /api/auth/login
POST   /api/auth/logout
POST   /api/payments/:id/refund
```

**URL best practices:**
```
✅ Lowercase: /api/users, /api/blog-posts
✅ Plural nouns: /users (not /user)
✅ Hyphens for multi-word: /blog-posts (not /blogPosts)
✅ Versioning: /api/v1/users
❌ Verbs in URL: /api/getUsers, /api/createPost
❌ Mixed case: /api/BlogPosts
❌ Underscores: /api/blog_posts
```

---

<a id="p6-status-codes"></a>
**Topic 2: HTTP Status Codes**

```
2xx — Success
200 OK             — GET, PUT, PATCH success
201 Created        — POST success (new resource created)
204 No Content     — DELETE success (no body)

3xx — Redirection
301 Moved Permanently   — permanent redirect (SEO-এ)
302 Found               — temporary redirect
304 Not Modified        — cache valid

4xx — Client Error
400 Bad Request         — Invalid input, validation error
401 Unauthorized        — Not authenticated (no/invalid token)
403 Forbidden           — Authenticated but no permission
404 Not Found           — Resource doesn't exist
405 Method Not Allowed  — GET /users-এ POST নেই
409 Conflict            — Duplicate (email already exists)
410 Gone                — Resource permanently deleted
422 Unprocessable Entity — Validation failed (alternative to 400)
429 Too Many Requests   — Rate limit exceeded

5xx — Server Error
500 Internal Server Error — Unexpected error
502 Bad Gateway         — Upstream server error
503 Service Unavailable — Server down/overloaded
504 Gateway Timeout     — Upstream timeout
```

**Common mistakes:**
```
❌ 200 OK + { error: "User not found" }  — always use correct status code!
❌ 500 for validation errors             — 400/422 ব্যবহার করুন
❌ 403 when 401 is correct               — 401: not logged in, 403: logged in but no permission
❌ 404 for wrong method                  — 405 Method Not Allowed
```

---

<a id="p6-response-format"></a>
**Topic 3: API Response Format Standards**

```javascript
// ────────────────────────────────────────────
// Success response
// ────────────────────────────────────────────
// Single resource
{
    "success": true,
    "data": {
        "id": "507f1f77bcf86cd799439011",
        "name": "Alice",
        "email": "alice@example.com",
        "role": "user",
        "createdAt": "2026-05-13T10:00:00.000Z"
    }
}

// List with pagination
{
    "success": true,
    "data": [
        { "id": "...", "name": "Alice" },
        { "id": "...", "name": "Bob" }
    ],
    "pagination": {
        "page": 1,
        "limit": 10,
        "total": 150,
        "pages": 15,
        "hasNext": true,
        "hasPrev": false
    }
}

// ────────────────────────────────────────────
// Error response
// ────────────────────────────────────────────
// Single error
{
    "success": false,
    "error": {
        "message": "User not found",
        "code": "NOT_FOUND"
    }
}

// Validation errors
{
    "success": false,
    "error": {
        "message": "Validation failed",
        "code": "VALIDATION_ERROR",
        "details": [
            { "field": "email", "message": "Invalid email format" },
            { "field": "password", "message": "Must be at least 8 characters" }
        ]
    }
}

// ────────────────────────────────────────────
// Response helpers
// ────────────────────────────────────────────
// src/utils/response.js
const sendSuccess = (res, data, statusCode = 200, meta = null) => {
    const response = { success: true, data };
    if (meta) response.pagination = meta;
    res.status(statusCode).json(response);
};

const sendError = (res, message, statusCode = 500, code = null, details = null) => {
    const error = { message };
    if (code) error.code = code;
    if (details) error.details = details;
    res.status(statusCode).json({ success: false, error });
};

const sendPaginated = (res, data, page, limit, total) => {
    sendSuccess(res, data, 200, {
        page: Number(page),
        limit: Number(limit),
        total,
        pages: Math.ceil(total / limit),
        hasNext: page * limit < total,
        hasPrev: page > 1
    });
};

module.exports = { sendSuccess, sendError, sendPaginated };
```

---

<a id="p6-validation"></a>
**Topic 4: Input Validation — express-validator**

```bash
npm install express-validator
```

```javascript
const { body, param, query, validationResult } = require('express-validator');

// ────────────────────────────────────────────
// Validation chains
// ────────────────────────────────────────────
const createUserValidation = [
    body('name')
        .trim()
        .notEmpty().withMessage('Name is required')
        .isLength({ min: 2, max: 50 }).withMessage('Name: 2-50 characters')
        .matches(/^[a-zA-Z\s]+$/).withMessage('Name: letters and spaces only'),

    body('email')
        .isEmail().withMessage('Invalid email format')
        .normalizeEmail()
        .toLowerCase(),

    body('password')
        .isLength({ min: 8 }).withMessage('Password: minimum 8 characters')
        .matches(/[A-Z]/).withMessage('Password: at least one uppercase letter')
        .matches(/[a-z]/).withMessage('Password: at least one lowercase letter')
        .matches(/\d/).withMessage('Password: at least one number'),

    body('age')
        .optional()
        .isInt({ min: 18, max: 120 }).withMessage('Age: 18-120')
        .toInt(),

    body('role')
        .optional()
        .isIn(['user', 'admin', 'moderator']).withMessage('Invalid role')
];

const updateUserValidation = [
    param('id').isMongoId().withMessage('Invalid user ID'),
    body('name').optional().trim().isLength({ min: 2, max: 50 }),
    body('email').optional().isEmail().normalizeEmail()
];

const paginationValidation = [
    query('page').optional().isInt({ min: 1 }).toInt().default(1),
    query('limit').optional().isInt({ min: 1, max: 100 }).toInt().default(10),
    query('sort').optional().isIn(['name', 'email', 'createdAt', '-createdAt'])
];

// ────────────────────────────────────────────
// Validation middleware
// ────────────────────────────────────────────
const validate = (req, res, next) => {
    const errors = validationResult(req);
    if (errors.isEmpty()) return next();

    const details = errors.array().map(err => ({
        field: err.path,
        message: err.msg,
        value: err.value
    }));

    return res.status(400).json({
        success: false,
        error: {
            message: 'Validation failed',
            code: 'VALIDATION_ERROR',
            details
        }
    });
};

// ────────────────────────────────────────────
// Routes-এ apply করুন
// ────────────────────────────────────────────
router.post('/', createUserValidation, validate, userController.create);
router.put('/:id', updateUserValidation, validate, userController.update);
router.get('/', paginationValidation, validate, userController.getAll);

// ────────────────────────────────────────────
// Custom validator
// ────────────────────────────────────────────
body('email').custom(async (email) => {
    const user = await User.findOne({ email });
    if (user) throw new Error('Email already in use');
    return true;
});

body('confirmPassword').custom((confirmPassword, { req }) => {
    if (confirmPassword !== req.body.password) {
        throw new Error('Passwords do not match');
    }
    return true;
});
```

---

<a id="p6-pagination"></a>
**Topic 5: Pagination, Filtering ও Sorting**

```javascript
// src/utils/queryBuilder.js
// MongoDB query helper

function buildQuery(reqQuery) {
    const {
        page = 1, limit = 10, sort = '-createdAt',
        fields, search,
        ...filters
    } = reqQuery;

    // ────────────────────────────────────────────
    // Filter — comparison operators
    // GET /users?age[gte]=18&age[lte]=30&role=user
    // ────────────────────────────────────────────
    let filterStr = JSON.stringify(filters);
    filterStr = filterStr.replace(/\b(gte|gt|lte|lt|in|nin|ne)\b/g, '$$$1');
    const parsedFilters = JSON.parse(filterStr);

    // ────────────────────────────────────────────
    // Search — text search
    // GET /users?search=alice
    // ────────────────────────────────────────────
    if (search) {
        parsedFilters.$or = [
            { name: { $regex: search, $options: 'i' } },
            { email: { $regex: search, $options: 'i' } }
        ];
    }

    // ────────────────────────────────────────────
    // Pagination
    // ────────────────────────────────────────────
    const pageNum = Math.max(1, parseInt(page));
    const limitNum = Math.min(100, Math.max(1, parseInt(limit)));
    const skip = (pageNum - 1) * limitNum;

    // ────────────────────────────────────────────
    // Sort — GET /users?sort=-createdAt,name
    // ────────────────────────────────────────────
    const sortStr = sort.split(',').join(' ');

    // ────────────────────────────────────────────
    // Field selection — GET /users?fields=name,email
    // ────────────────────────────────────────────
    const selectStr = fields ? fields.split(',').join(' ') : '-__v -password';

    return {
        filter: parsedFilters,
        sort: sortStr,
        select: selectStr,
        skip,
        limit: limitNum,
        page: pageNum
    };
}

// Controller-এ:
exports.getAll = async (req, res, next) => {
    try {
        const { filter, sort, select, skip, limit, page } = buildQuery(req.query);

        const [data, total] = await Promise.all([
            User.find(filter).sort(sort).select(select).skip(skip).limit(limit).lean(),
            User.countDocuments(filter)
        ]);

        sendPaginated(res, data, page, limit, total);
    } catch (err) {
        next(err);
    }
};

// Usage examples:
// GET /api/users                        → page 1, limit 10
// GET /api/users?page=2&limit=20        → page 2, 20 per page
// GET /api/users?sort=-createdAt        → newest first
// GET /api/users?sort=name              → alphabetical
// GET /api/users?fields=name,email      → only name+email
// GET /api/users?search=alice           → search by name/email
// GET /api/users?role=admin             → filter by role
// GET /api/users?age[gte]=18&age[lte]=30 → age range
```

---

<a id="p6-upload"></a>
**Topic 6: File Upload — Multer**

```bash
npm install multer sharp
```

```javascript
// src/middleware/upload.js
const multer = require('multer');
const sharp = require('sharp');
const path = require('path');
const crypto = require('crypto');
const { AppError } = require('./errorHandler');

// ────────────────────────────────────────────
// Memory storage (process before saving)
// ────────────────────────────────────────────
const multerStorage = multer.memoryStorage();

const multerFilter = (req, file, cb) => {
    const allowedTypes = ['image/jpeg', 'image/jpg', 'image/png', 'image/webp'];
    if (allowedTypes.includes(file.mimetype)) {
        cb(null, true);
    } else {
        cb(new AppError('Only JPEG, PNG, WebP images allowed', 400), false);
    }
};

const upload = multer({
    storage: multerStorage,
    fileFilter: multerFilter,
    limits: {
        fileSize: 5 * 1024 * 1024,   // 5MB
        files: 5                      // max 5 files
    }
});

// ────────────────────────────────────────────
// Image processing middleware
// ────────────────────────────────────────────
async function processAvatar(req, res, next) {
    if (!req.file) return next();

    // Unique filename
    const filename = `user-${req.user.id}-${crypto.randomBytes(8).toString('hex')}.webp`;

    // Process with sharp — resize, format, optimize
    await sharp(req.file.buffer)
        .resize(300, 300, { fit: 'cover' })
        .toFormat('webp', { quality: 80 })
        .toFile(path.join(__dirname, '../../uploads/avatars', filename));

    req.file.filename = filename;
    req.file.path = `/uploads/avatars/${filename}`;
    next();
}

// ────────────────────────────────────────────
// Routes
// ────────────────────────────────────────────
// Single file
router.post('/avatar',
    requireAuth,
    upload.single('avatar'),   // form field name: 'avatar'
    processAvatar,
    async (req, res) => {
        await User.findByIdAndUpdate(req.user.id, { avatar: req.file.path });
        res.json({ success: true, avatar: req.file.path });
    }
);

// Multiple files
router.post('/gallery',
    requireAuth,
    upload.array('photos', 10),  // max 10 files
    async (req, res) => {
        const filePaths = req.files.map(f => f.path);
        res.json({ success: true, files: filePaths });
    }
);

// Mixed fields
router.post('/post',
    requireAuth,
    upload.fields([
        { name: 'cover', maxCount: 1 },
        { name: 'attachments', maxCount: 5 }
    ]),
    async (req, res) => {
        const cover = req.files.cover?.[0];
        const attachments = req.files.attachments || [];
        // ...
    }
);

// ────────────────────────────────────────────
// Disk storage (direct save)
// ────────────────────────────────────────────
const diskStorage = multer.diskStorage({
    destination: (req, file, cb) => {
        cb(null, 'uploads/documents');
    },
    filename: (req, file, cb) => {
        const ext = path.extname(file.originalname);
        const name = `${Date.now()}-${crypto.randomBytes(8).toString('hex')}${ext}`;
        cb(null, name);
    }
});

module.exports = { upload, processAvatar };
```

---

<a id="p6-versioning"></a>
**Topic 7: API Versioning**

```javascript
// ────────────────────────────────────────────
// URL-based versioning (most common)
// ────────────────────────────────────────────
app.use('/api/v1', v1Routes);
app.use('/api/v2', v2Routes);

// v1/routes/users.js → old format
// v2/routes/users.js → new format (breaking changes)

// ────────────────────────────────────────────
// Header-based versioning
// ────────────────────────────────────────────
app.use((req, res, next) => {
    const version = req.headers['api-version'] || 'v1';
    req.apiVersion = version;
    next();
});

// ────────────────────────────────────────────
// Query param versioning
// ────────────────────────────────────────────
// GET /api/users?version=2

// ────────────────────────────────────────────
// Version deprecation
// ────────────────────────────────────────────
app.use('/api/v1', (req, res, next) => {
    res.setHeader('Deprecation', 'true');
    res.setHeader('Sunset', 'Sat, 31 Dec 2026 23:59:59 GMT');
    res.setHeader('Link', '<https://api.example.com/api/v2>; rel="successor-version"');
    next();
}, v1Routes);
```

---

<a id="p6-docs"></a>
**Topic 8: API Documentation — Swagger/OpenAPI**

```bash
npm install swagger-jsdoc swagger-ui-express
```

```javascript
// src/config/swagger.js
const swaggerJsdoc = require('swagger-jsdoc');
const swaggerUi = require('swagger-ui-express');

const options = {
    definition: {
        openapi: '3.0.0',
        info: {
            title: 'My API',
            version: '1.0.0',
            description: 'Node.js REST API documentation'
        },
        servers: [
            { url: 'http://localhost:3000/api/v1', description: 'Development' },
            { url: 'https://api.example.com/api/v1', description: 'Production' }
        ],
        components: {
            securitySchemes: {
                BearerAuth: {
                    type: 'http',
                    scheme: 'bearer',
                    bearerFormat: 'JWT'
                }
            }
        }
    },
    apis: ['./src/routes/*.js']  // JSDoc comments scan করবে
};

const specs = swaggerJsdoc(options);

// app.js-এ:
app.use('/api-docs', swaggerUi.serve, swaggerUi.setup(specs));
// http://localhost:3000/api-docs — interactive docs

// Route file-এ JSDoc:
/**
 * @swagger
 * /users:
 *   get:
 *     summary: Get all users
 *     tags: [Users]
 *     security:
 *       - BearerAuth: []
 *     parameters:
 *       - in: query
 *         name: page
 *         schema:
 *           type: integer
 *           default: 1
 *       - in: query
 *         name: limit
 *         schema:
 *           type: integer
 *           default: 10
 *     responses:
 *       200:
 *         description: Users list
 *         content:
 *           application/json:
 *             schema:
 *               type: object
 *               properties:
 *                 success:
 *                   type: boolean
 *                 data:
 *                   type: array
 *                   items:
 *                     $ref: '#/components/schemas/User'
 *       401:
 *         description: Unauthorized
 */
router.get('/', requireAuth, userController.getAll);
```

---

<a id="p6-cors"></a>
**Topic 9: CORS Configuration**

```javascript
const cors = require('cors');

// ────────────────────────────────────────────
// Simple CORS
// ────────────────────────────────────────────
app.use(cors());  // সব origins allow — development only!

// ────────────────────────────────────────────
// Specific origins
// ────────────────────────────────────────────
const allowedOrigins = [
    'http://localhost:3000',
    'http://localhost:5173',
    'https://myapp.com',
    'https://www.myapp.com'
];

app.use(cors({
    origin: (origin, callback) => {
        // Postman (no origin) বা allowed origins
        if (!origin || allowedOrigins.includes(origin)) {
            callback(null, true);
        } else {
            callback(new Error('Not allowed by CORS'));
        }
    },
    methods: ['GET', 'POST', 'PUT', 'PATCH', 'DELETE', 'OPTIONS'],
    allowedHeaders: ['Content-Type', 'Authorization', 'X-Request-Id'],
    exposedHeaders: ['X-Total-Count', 'X-Request-Id'],
    credentials: true,    // Cookie পাঠাতে হলে
    maxAge: 86400         // Preflight cache: 1 day
}));

// ────────────────────────────────────────────
// CORS কী?
// ────────────────────────────────────────────
// Browser security: origin A → origin B-এর API call block করে।
// CORS headers দিয়ে server বলে "এই origins থেকে allow করি"।
// Preflight: Browser OPTIONS request পাঠায় → server CORS headers দেয় → actual request

// Origin = protocol + domain + port
// http://localhost:3000 ≠ http://localhost:5000 (different port = different origin)
// http://example.com ≠ https://example.com (different protocol)
```

---

<a id="p6-complete"></a>
**Topic 10: Complete CRUD API Example**

```javascript
// src/routes/posts.js
const express = require('express');
const router = express.Router();
const { body, param, query } = require('express-validator');
const { requireAuth } = require('../middleware/auth');
const { validate } = require('../middleware/validate');
const postController = require('../controllers/postController');

const postValidation = [
    body('title').trim().notEmpty().isLength({ max: 200 }),
    body('content').trim().notEmpty().isLength({ max: 10000 }),
    body('tags').optional().isArray().withMessage('Tags must be an array'),
    body('tags.*').optional().isString().trim(),
    body('published').optional().isBoolean().toBoolean()
];

// GET /api/posts
router.get('/',
    [
        query('page').optional().isInt({ min: 1 }).toInt(),
        query('limit').optional().isInt({ min: 1, max: 50 }).toInt(),
        query('search').optional().trim().isLength({ max: 100 }),
        query('published').optional().isBoolean().toBoolean()
    ],
    validate,
    postController.getAll
);

// GET /api/posts/:id
router.get('/:id',
    [param('id').isMongoId()],
    validate,
    postController.getById
);

// POST /api/posts
router.post('/',
    requireAuth,
    postValidation,
    validate,
    postController.create
);

// PUT /api/posts/:id
router.put('/:id',
    requireAuth,
    [param('id').isMongoId(), ...postValidation],
    validate,
    postController.update
);

// DELETE /api/posts/:id
router.delete('/:id',
    requireAuth,
    [param('id').isMongoId()],
    validate,
    postController.remove
);

module.exports = router;
```

---

<a id="p6-qa"></a>
**Topic 11: PART 6 Interview Q&A**

```
প্রশ্ন: REST API design-এ কোন best practices follow করেন?
উত্তর:
- Plural nouns: /users, /posts (verbs না)
- HTTP methods সঠিকভাবে: GET=read, POST=create, PUT=full update,
  PATCH=partial, DELETE=remove
- Correct status codes: 201 for create, 204 for delete, 401/403 distinction
- Consistent response format: { success, data, pagination/error }
- Versioning: /api/v1/... (breaking changes-এ v2)
- Pagination সব list endpoints-এ
- Input validation সব mutating endpoints-এ

প্রশ্ন: 401 ও 403-এর পার্থক্য?
উত্তর:
401 Unauthorized: Not authenticated — token নেই বা invalid।
"আপনি কে সেটা জানি না।"

403 Forbidden: Authenticated কিন্তু permission নেই।
"আপনি কে জানি, কিন্তু এটা করার permission নেই।"

প্রশ্ন: CORS কী? কেন দরকার?
উত্তর: Browser-এর same-origin policy। Origin A থেকে Origin B-তে
API call করলে browser block করে।
Server CORS headers দিয়ে কোন origins allow — browser সেটা দেখে allow করে।
credentials: true থাকলে cookie পাঠানো যায়।
Server-to-server (Node → DB) CORS নেই — only browser।

প্রশ্ন: File upload-এ কী security check করবেন?
উত্তর:
1. MIME type check (file.mimetype) — শুধু allowed types
2. File size limit (multer limits)
3. Filename sanitize — original filename use করবেন না
4. Random filename generate করুন (crypto)
5. Scan for malware (optional, production)
6. Uploads directory outside public web root
7. CDN/S3-এ store করুন (not server disk)

প্রশ্ন: API versioning কেন দরকার?
উত্তর: Existing clients break না করে API change করতে।
v1 client চলতে থাকে, নতুন clients v2 use করে।
Deprecation header দিয়ে v1 ব্যবহারকারীদের v2-তে migrate করতে জানান।
URL versioning (/v1/) সবচেয়ে visible ও popular।

প্রশ্ন: express-validator vs Joi vs Zod?
উত্তর:
express-validator: Express middleware — req directly validate।
Joi: Object schema validation — any JS object।
Zod: TypeScript-first — type inference সহ।

Simple Express app: express-validator ভালো।
TypeScript project: Zod excellent।
Complex schemas: Joi flexible।
```

---

**PART 6 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| REST constraints | Stateless, Uniform Interface, Client-Server |
| URL design | Plural nouns, lowercase, no verbs |
| 200/201/204 | OK / Created / No Content |
| 400/401/403/404 | Bad Request / Unauth / Forbidden / Not Found |
| 409/429/500 | Conflict / Rate Limit / Server Error |
| Response format | `{ success, data, pagination/error }` |
| express-validator | `body().isEmail()`, `validationResult()` |
| Pagination | page, limit, skip, total, pages |
| Multer | File upload middleware |
| `memoryStorage` | Buffer-এ রাখো, process করো (sharp) |
| `diskStorage` | Disk-এ সরাসরি save |
| API versioning | `/api/v1/` URL path |
| Swagger | JSDoc → interactive docs at /api-docs |
| CORS | Browser security — allowed origins |
| `credentials: true` | Cookie cross-origin পাঠাতে |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 7 — Error Handling ও Logging

---

<a id="part7"></a>
## PART 7: Error Handling ও Logging

> Production-ready error handling, custom error classes, centralized error middleware, Winston logging, Morgan HTTP logger এবং unhandled rejection management।

| # | বিষয় |
|---|-------|
| 1 | [Error Types in Node.js](#p7-error-types) |
| 2 | [Custom AppError Class](#p7-custom-error) |
| 3 | [Async Error Handling](#p7-async-errors) |
| 4 | [Centralized Error Middleware](#p7-error-middleware) |
| 5 | [Operational vs Programmer Errors](#p7-op-vs-prog) |
| 6 | [Unhandled Rejections ও Uncaught Exceptions](#p7-unhandled) |
| 7 | [Winston Logger](#p7-winston) |
| 8 | [Morgan HTTP Logger](#p7-morgan) |
| 9 | [Structured Logging ও Log Levels](#p7-structured) |
| 10 | [PART 7 Interview Q&A](#p7-qa) |

---

<a id="p7-error-types"></a>
**Topic 1: Error Types in Node.js**

```
Node.js-এ 4 ধরনের error:

1. Standard JS Errors
   TypeError      — wrong type: null.property
   ReferenceError — undefined variable
   SyntaxError    — invalid syntax (parse time)
   RangeError     — out of range: new Array(-1)

2. System Errors (libuv)
   ENOENT  — file not found
   EACCES  — permission denied
   EADDRINUSE — port already in use
   ECONNREFUSED — connection refused

3. Operational Errors
   DB connection lost, API timeout, invalid user input
   → Expected, handle gracefully

4. Programmer Errors
   null.foo, wrong argument type, logic bugs
   → Unexpected, should be fixed in code
```

```javascript
// Error class hierarchy
Error
├── TypeError
├── ReferenceError
├── SyntaxError
├── RangeError
└── AppError (custom — আমরা তৈরি করব)

// System error চেনার উপায়
fs.readFile('/nonexistent', (err) => {
    if (err) {
        console.log(err.code);    // 'ENOENT'
        console.log(err.message); // "ENOENT: no such file or directory, open '/nonexistent'"
        console.log(err.syscall); // 'open'
        console.log(err.path);    // '/nonexistent'
    }
});
```

---

<a id="p7-custom-error"></a>
**Topic 2: Custom AppError Class**

```javascript
// src/utils/AppError.js

class AppError extends Error {
    constructor(message, statusCode, code = null) {
        super(message);

        this.statusCode = statusCode;
        this.code = code;                          // Machine-readable code: 'NOT_FOUND'
        this.status = String(statusCode).startsWith('4') ? 'fail' : 'error';
        this.isOperational = true;                 // Known, expected error

        Error.captureStackTrace(this, this.constructor);
    }
}

// ────────────────────────────────────────────
// Common error factory functions
// ────────────────────────────────────────────
const notFound = (resource = 'Resource') =>
    new AppError(`${resource} not found`, 404, 'NOT_FOUND');

const badRequest = (message) =>
    new AppError(message, 400, 'BAD_REQUEST');

const unauthorized = (message = 'Authentication required') =>
    new AppError(message, 401, 'UNAUTHORIZED');

const forbidden = (message = 'Insufficient permissions') =>
    new AppError(message, 403, 'FORBIDDEN');

const conflict = (message) =>
    new AppError(message, 409, 'CONFLICT');

const tooManyRequests = (message = 'Too many requests') =>
    new AppError(message, 429, 'RATE_LIMIT_EXCEEDED');

module.exports = { AppError, notFound, badRequest, unauthorized, forbidden, conflict };

// ────────────────────────────────────────────
// Usage
// ────────────────────────────────────────────
const user = await User.findById(id);
if (!user) throw notFound('User');

if (!hasPermission) throw forbidden();

if (existingUser) throw conflict('Email already registered');
```

---

<a id="p7-async-errors"></a>
**Topic 3: Async Error Handling**

```javascript
// ────────────────────────────────────────────
// Problem: async errors Express-এ catch হয় না
// ────────────────────────────────────────────
// ❌ এটা Express-এর error handler-এ যাবে না
app.get('/user/:id', async (req, res) => {
    const user = await User.findById(req.params.id); // throws → unhandled!
    res.json(user);
});

// ────────────────────────────────────────────
// Solution 1: try-catch with next
// ────────────────────────────────────────────
app.get('/user/:id', async (req, res, next) => {
    try {
        const user = await User.findById(req.params.id);
        res.json(user);
    } catch (err) {
        next(err);  // Error middleware-এ পাঠাও
    }
});

// ────────────────────────────────────────────
// Solution 2: catchAsync wrapper (DRY)
// ────────────────────────────────────────────
// src/utils/catchAsync.js
const catchAsync = (fn) => (req, res, next) => {
    Promise.resolve(fn(req, res, next)).catch(next);
};

module.exports = catchAsync;

// Usage — much cleaner!
const catchAsync = require('../utils/catchAsync');

exports.getUser = catchAsync(async (req, res) => {
    const user = await User.findById(req.params.id);
    if (!user) throw notFound('User');
    res.json({ success: true, data: user });
});

exports.createUser = catchAsync(async (req, res) => {
    const user = await User.create(req.body);
    res.status(201).json({ success: true, data: user });
});

// ────────────────────────────────────────────
// Solution 3: Express 5 (automatic async handling)
// ────────────────────────────────────────────
// Express 5-এ async errors automatically catch হয়
// npm install express@5
// catchAsync wrapper আর দরকার নেই
```

---

<a id="p7-error-middleware"></a>
**Topic 4: Centralized Error Middleware**

```javascript
// src/middleware/errorHandler.js
const { AppError } = require('../utils/AppError');
const logger = require('../utils/logger');
const config = require('../config/env');

// ────────────────────────────────────────────
// Mongoose errors → AppError convert
// ────────────────────────────────────────────
function handleCastError(err) {
    return new AppError(`Invalid ${err.path}: ${err.value}`, 400, 'INVALID_ID');
}

function handleDuplicateKey(err) {
    const field = Object.keys(err.keyValue)[0];
    return new AppError(`${field} already exists`, 409, 'DUPLICATE_KEY');
}

function handleValidationError(err) {
    const messages = Object.values(err.errors).map(e => e.message);
    return new AppError(`Validation failed: ${messages.join('. ')}`, 400, 'VALIDATION_ERROR');
}

// JWT errors
function handleJWTError() {
    return new AppError('Invalid token', 401, 'INVALID_TOKEN');
}

function handleJWTExpired() {
    return new AppError('Token expired', 401, 'TOKEN_EXPIRED');
}

// ────────────────────────────────────────────
// Development error response — full details
// ────────────────────────────────────────────
function sendDevelopmentError(err, res) {
    res.status(err.statusCode).json({
        success: false,
        error: {
            message: err.message,
            code: err.code,
            stack: err.stack
        }
    });
}

// ────────────────────────────────────────────
// Production error response — minimal info
// ────────────────────────────────────────────
function sendProductionError(err, res) {
    if (err.isOperational) {
        // Known error — client-এ বলা safe
        res.status(err.statusCode).json({
            success: false,
            error: {
                message: err.message,
                code: err.code
            }
        });
    } else {
        // Unknown/programmer error — details leak করবেন না
        logger.error('UNHANDLED ERROR', err);
        res.status(500).json({
            success: false,
            error: {
                message: 'Something went wrong. Please try again later.',
                code: 'INTERNAL_ERROR'
            }
        });
    }
}

// ────────────────────────────────────────────
// Global error handling middleware
// Express: 4 arguments = error middleware
// ────────────────────────────────────────────
module.exports = function globalErrorHandler(err, req, res, next) {
    err.statusCode = err.statusCode || 500;
    err.status = err.status || 'error';

    // Log all errors
    if (err.statusCode >= 500) {
        logger.error({
            message: err.message,
            stack: err.stack,
            url: req.url,
            method: req.method,
            userId: req.user?.id
        });
    } else {
        logger.warn({ message: err.message, code: err.code, url: req.url });
    }

    // Mongoose/JWT errors → AppError
    let error = err;
    if (err.name === 'CastError') error = handleCastError(err);
    if (err.code === 11000) error = handleDuplicateKey(err);
    if (err.name === 'ValidationError') error = handleValidationError(err);
    if (err.name === 'JsonWebTokenError') error = handleJWTError();
    if (err.name === 'TokenExpiredError') error = handleJWTExpired();

    if (config.isDev) {
        sendDevelopmentError(error, res);
    } else {
        sendProductionError(error, res);
    }
};

// ────────────────────────────────────────────
// 404 handler (route not found)
// ────────────────────────────────────────────
module.exports.notFoundHandler = (req, res, next) => {
    next(new AppError(`Route ${req.method} ${req.url} not found`, 404, 'ROUTE_NOT_FOUND'));
};

// app.js-এ:
app.use(require('./middleware/errorHandler').notFoundHandler);  // সব routes-এর পরে
app.use(require('./middleware/errorHandler'));                   // শেষে
```

---

<a id="p7-op-vs-prog"></a>
**Topic 5: Operational vs Programmer Errors**

```
Operational Errors — Runtime-এ expected:
✅ File not found
✅ DB connection failed
✅ Invalid user input
✅ Network timeout
✅ 3rd party API error
→ Handle gracefully, return meaningful error response

Programmer Errors — Bugs in code:
❌ undefined.property (TypeError)
❌ Wrong function arguments
❌ Logic errors
❌ Off-by-one errors
→ Fix the bug, don't "handle" it
→ Production-এ crash + restart → process manager (PM2) restart করুক

কীভাবে distinguish করবেন?
- AppError (isOperational: true) → operational
- Native JS errors (TypeError, ReferenceError) → programmer error
- Third-party library errors → check docs, wrap in AppError if operational
```

```javascript
// Programmer error example — fix the code, don't catch
function getUser(users, id) {
    // ❌ Bug: users could be undefined
    return users.find(u => u.id === id);
    // TypeError: Cannot read properties of undefined (reading 'find')
}

// ✅ Fix: validate inputs
function getUser(users, id) {
    if (!Array.isArray(users)) throw new TypeError('users must be an array');
    return users.find(u => u.id === id);
}
```

---

<a id="p7-unhandled"></a>
**Topic 6: Unhandled Rejections ও Uncaught Exceptions**

```javascript
// src/index.js (entry point)

const server = app.listen(config.port, () => {
    logger.info(`Server running on port ${config.port}`);
});

// ────────────────────────────────────────────
// Unhandled Promise Rejections
// async code-এ catch না করলে এখানে আসে
// ────────────────────────────────────────────
process.on('unhandledRejection', (err) => {
    logger.error('UNHANDLED REJECTION! Shutting down...', {
        name: err.name,
        message: err.message,
        stack: err.stack
    });

    // Graceful shutdown: চলমান requests finish হতে দাও
    server.close(() => {
        process.exit(1);  // PM2/Docker restart করবে
    });

    // Timeout: 10s-এ force exit
    setTimeout(() => process.exit(1), 10000).unref();
});

// ────────────────────────────────────────────
// Uncaught Exceptions
// Synchronous code-এ uncaught error
// ────────────────────────────────────────────
process.on('uncaughtException', (err) => {
    logger.error('UNCAUGHT EXCEPTION! Shutting down...', {
        name: err.name,
        message: err.message,
        stack: err.stack
    });
    // Immediate exit — state corrupted হতে পারে
    process.exit(1);
});

// ────────────────────────────────────────────
// SIGTERM — Graceful shutdown (Docker/Kubernetes)
// ────────────────────────────────────────────
process.on('SIGTERM', () => {
    logger.info('SIGTERM received. Graceful shutdown...');
    server.close(() => {
        logger.info('HTTP server closed');
        // DB connections close করুন
        mongoose.connection.close(false, () => {
            logger.info('MongoDB disconnected');
            process.exit(0);
        });
    });
});

// ────────────────────────────────────────────
// SIGINT — Ctrl+C (development)
// ────────────────────────────────────────────
process.on('SIGINT', () => {
    logger.info('SIGINT received. Shutting down...');
    server.close(() => process.exit(0));
});
```

---

<a id="p7-winston"></a>
**Topic 7: Winston Logger**

```bash
npm install winston winston-daily-rotate-file
```

```javascript
// src/utils/logger.js
const winston = require('winston');
const DailyRotateFile = require('winston-daily-rotate-file');
const path = require('path');
const config = require('../config/env');

// ────────────────────────────────────────────
// Custom format
// ────────────────────────────────────────────
const { combine, timestamp, printf, colorize, json, errors } = winston.format;

// Development: human-readable
const devFormat = combine(
    colorize({ all: true }),
    timestamp({ format: 'HH:mm:ss' }),
    errors({ stack: true }),
    printf(({ level, message, timestamp, stack, ...meta }) => {
        let log = `${timestamp} [${level}]: ${message}`;
        if (Object.keys(meta).length) log += ` ${JSON.stringify(meta)}`;
        if (stack) log += `\n${stack}`;
        return log;
    })
);

// Production: JSON (easily parseable by log aggregators)
const prodFormat = combine(
    timestamp(),
    errors({ stack: true }),
    json()
);

// ────────────────────────────────────────────
// Transports — where logs go
// ────────────────────────────────────────────
const transports = [
    // Console (always)
    new winston.transports.Console({
        format: config.isDev ? devFormat : prodFormat
    })
];

if (!config.isDev) {
    // Combined logs (info+)
    transports.push(new DailyRotateFile({
        filename: path.join('logs', 'combined-%DATE%.log'),
        datePattern: 'YYYY-MM-DD',
        maxSize: '20m',
        maxFiles: '14d',
        format: prodFormat
    }));

    // Error logs only
    transports.push(new DailyRotateFile({
        filename: path.join('logs', 'error-%DATE%.log'),
        datePattern: 'YYYY-MM-DD',
        level: 'error',
        maxSize: '20m',
        maxFiles: '30d',
        format: prodFormat
    }));
}

// ────────────────────────────────────────────
// Logger instance
// ────────────────────────────────────────────
const logger = winston.createLogger({
    level: config.isDev ? 'debug' : 'info',
    transports
});

module.exports = logger;

// ────────────────────────────────────────────
// Usage
// ────────────────────────────────────────────
logger.error('DB connection failed', { host: 'localhost', port: 5432 });
logger.warn('Rate limit approaching', { userId: '123', requests: 95 });
logger.info('Server started', { port: 3000, env: 'production' });
logger.http('Incoming request', { method: 'GET', url: '/api/users' });
logger.debug('Query executed', { sql: 'SELECT * FROM users', duration: '15ms' });
```

---

<a id="p7-morgan"></a>
**Topic 8: Morgan HTTP Logger**

```bash
npm install morgan
```

```javascript
const morgan = require('morgan');

// ────────────────────────────────────────────
// Development — colorful, detailed
// ────────────────────────────────────────────
app.use(morgan('dev'));
// GET /api/users 200 45.123 ms - 1234

// ────────────────────────────────────────────
// Production — JSON with Winston
// ────────────────────────────────────────────
const morganStream = {
    write: (message) => logger.http(message.trim())
};

// Custom format — JSON
morgan.token('userId', (req) => req.user?.id || 'anonymous');
morgan.token('body', (req) => {
    // Sensitive fields mask করুন
    const body = { ...req.body };
    if (body.password) body.password = '[REDACTED]';
    if (body.token) body.token = '[REDACTED]';
    return JSON.stringify(body);
});

app.use(morgan(
    ':method :url :status :response-time ms - :res[content-length] :userId',
    { stream: morganStream }
));

// ────────────────────────────────────────────
// Health check এবং static files skip করুন
// ────────────────────────────────────────────
app.use(morgan('combined', {
    stream: morganStream,
    skip: (req) => req.url === '/health' || req.url.startsWith('/api-docs')
}));
```

---

<a id="p7-structured"></a>
**Topic 9: Structured Logging ও Log Levels**

```
Log Levels (Winston default — RFC 5424):
error   (0) — System errors, crashes, unhandled exceptions
warn    (1) — Recoverable issues, deprecated usage, rate limits
info    (2) — Server start, user login, important events
http    (3) — HTTP requests (morgan)
verbose (4) — Detailed flow info
debug   (5) — Debug info, variable values (dev only)
silly   (6) — Extreme detail

Production: info+ (error, warn, info)
Development: debug+ (all levels)
```

```javascript
// ────────────────────────────────────────────
// Structured logging — always add context
// ────────────────────────────────────────────

// ❌ Bad — unstructured, hard to search
logger.error('User login failed for alice@example.com from 192.168.1.1');

// ✅ Good — structured, searchable, filterable
logger.warn('Login failed', {
    event: 'AUTH_FAILURE',
    email: 'alice@example.com',
    ip: req.ip,
    userAgent: req.headers['user-agent'],
    timestamp: new Date().toISOString()
});

// ────────────────────────────────────────────
// Request correlation ID
// ────────────────────────────────────────────
const { v4: uuidv4 } = require('uuid');

app.use((req, res, next) => {
    req.requestId = req.headers['x-request-id'] || uuidv4();
    res.setHeader('X-Request-Id', req.requestId);
    next();
});

// সব logs-এ requestId add করুন
logger.info('User created', {
    requestId: req.requestId,
    userId: user._id,
    email: user.email
});

// ────────────────────────────────────────────
// Sensitive data — কখনো log করবেন না
// ────────────────────────────────────────────
// ❌ Never log:
logger.info('User logged in', { password: req.body.password });
logger.info('Payment processed', { cardNumber: '4111111111111111' });
logger.info('Token generated', { accessToken: token });

// ✅ Log:
logger.info('User logged in', { userId: user._id, ip: req.ip });
logger.info('Payment processed', { orderId: order._id, amount: order.total });
logger.info('Token generated', { userId: user._id, tokenType: 'access' });
```

---

<a id="p7-qa"></a>
**Topic 10: PART 7 Interview Q&A**

```
প্রশ্ন: Operational error vs Programmer error পার্থক্য?
উত্তর:
Operational: Expected runtime errors — file not found, DB timeout, invalid input।
Handle gracefully → meaningful response return।

Programmer: Code bugs — TypeError, ReferenceError, logic errors।
Fix the code — "handle" করলে bug hidden হয়।

Production-এ programmer error → process crash → PM2 restart।
State corrupted হতে পারে বলে restart safe।

প্রশ্ন: catchAsync কেন ব্যবহার করি?
উত্তর: Express 4 async function-এর uncaught error নিজে handle করে না।
try-catch + next(err) প্রতিটি handler-এ লিখতে হবে — repetitive।
catchAsync wrapper fn-কে wrap করে, rejection catch করে next()-এ পাঠায়।
DRY principle + clean controller code।

প্রশ্ন: Express error middleware-এ 4 arguments কেন?
উত্তর: Express 4-argument function-কে error middleware হিসেবে চেনে।
(err, req, res, next) — err হলো error object।
3-argument হলে regular middleware — error catch করবে না।

প্রশ্ন: Unhandled rejection-এ process exit করি কেন?
উত্তর: Unhandled rejection মানে application unknown state-এ আছে।
Memory leak, inconsistent data, corrupted state সম্ভব।
Clean exit + process restart (PM2/Docker) safe state থেকে শুরু করে।
Node.js 15+ এ unhandled rejection-এ automatically crash হয়।

প্রশ্ন: Log-এ কী data রাখবেন না?
উত্তর:
- Passwords, tokens, secret keys
- Credit card numbers, CVV
- Social security numbers
- Personal health information (PHI)
- Full request body (mask sensitive fields)
GDPR/compliance violation হতে পারে।
Morgan-এ token redaction: body() custom token দিয়ে mask করুন।

প্রশ্ন: Winston ও Morgan-এর পার্থক্য?
উত্তর:
Morgan: HTTP request logger — method, URL, status, response time।
Express-specific middleware। মূলত HTTP traffic log করে।

Winston: General-purpose logger — যেকোনো log (error, info, debug)।
Transport: console, file, external services।
Morgan → Winston: stream দিয়ে Morgan-এর output Winston-এ পাঠানো যায়।
```

---

**PART 7 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| AppError | Custom error: statusCode + code + isOperational |
| isOperational | true = known error, false = bug |
| catchAsync | async handler wrapper — next(err) auto |
| Error middleware | 4 args: (err, req, res, next) |
| CastError | Invalid MongoDB ObjectId |
| Duplicate key (11000) | MongoDB unique constraint |
| ValidationError | Mongoose schema validation |
| unhandledRejection | Uncaught Promise rejection |
| uncaughtException | Synchronous uncaught error |
| SIGTERM | Graceful shutdown (Docker/K8s) |
| Winston | General logger — levels, transports |
| DailyRotateFile | Log rotation — date-based files |
| Morgan | HTTP request logger |
| Structured logging | JSON key-value — searchable |
| Request ID | Correlate logs across services |
| Never log | Password, token, card number, PII |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part8"></a>
## PART 8: Testing in Node.js

> Jest unit tests, Supertest integration tests, test-driven development, mocking, coverage reports এবং CI-ready test setup।

| # | বিষয় |
|---|-------|
| 1 | [Testing কেন? Test Pyramid](#p8-why-test) |
| 2 | [Jest Setup ও Configuration](#p8-jest-setup) |
| 3 | [Unit Testing — Functions](#p8-unit) |
| 4 | [Mocking — jest.mock ও jest.fn](#p8-mocking) |
| 5 | [Integration Testing — Supertest](#p8-supertest) |
| 6 | [Database Testing — In-memory MongoDB](#p8-db-testing) |
| 7 | [Test Utilities ও Factories](#p8-utilities) |
| 8 | [Code Coverage](#p8-coverage) |
| 9 | [Testing Best Practices](#p8-best-practices) |
| 10 | [PART 8 Interview Q&A](#p8-qa) |

---

<a id="p8-why-test"></a>
**Topic 1: Testing কেন? Test Pyramid**

```
Testing কেন?
1. Bugs early catch করা → production-এ cost কম
2. Refactoring নিরাপদ → regression detect
3. Living documentation → code কী করে বোঝায়
4. Confidence → deploy করতে ভয় নেই
5. Design improvement → testable code = better design

Test Pyramid:
          /\
         /  \
        / E2E \          ← কম (slow, expensive, brittle)
       /--------\
      /Integration\      ← মাঝারি (HTTP layer test)
     /------------\
    /  Unit Tests  \     ← বেশি (fast, isolated, cheap)
   /______________  \

Unit:        ~70% — functions, services, utilities
Integration: ~20% — API endpoints, DB queries
E2E:         ~10% — full user flows (Cypress/Playwright)
```

**Jest কেন?**
```
- Zero configuration
- Built-in mocking, coverage, assertions
- Snapshot testing
- Watch mode
- Parallel test execution
- Node.js ও Browser দুটোতে
```

---

<a id="p8-jest-setup"></a>
**Topic 2: Jest Setup ও Configuration**

```bash
npm install --save-dev jest supertest @types/jest
```

```json
// package.json
{
  "scripts": {
    "test": "jest",
    "test:watch": "jest --watch",
    "test:coverage": "jest --coverage",
    "test:ci": "jest --ci --coverage --forceExit"
  },
  "jest": {
    "testEnvironment": "node",
    "testMatch": ["**/__tests__/**/*.js", "**/*.test.js", "**/*.spec.js"],
    "collectCoverageFrom": [
      "src/**/*.js",
      "!src/index.js",
      "!src/config/**"
    ],
    "coverageThresholds": {
      "global": {
        "branches": 70,
        "functions": 80,
        "lines": 80,
        "statements": 80
      }
    },
    "setupFilesAfterFramework": ["./src/tests/setup.js"],
    "testTimeout": 10000
  }
}
```

```javascript
// src/tests/setup.js
const mongoose = require('mongoose');
const { MongoMemoryServer } = require('mongodb-memory-server');

let mongoServer;

// সব tests-এর আগে
beforeAll(async () => {
    mongoServer = await MongoMemoryServer.create();
    await mongoose.connect(mongoServer.getUri());
});

// সব tests-এর পরে
afterAll(async () => {
    await mongoose.disconnect();
    await mongoServer.stop();
});

// প্রতিটি test-এর পরে DB clean করো
afterEach(async () => {
    const collections = mongoose.connection.collections;
    for (const key in collections) {
        await collections[key].deleteMany({});
    }
});
```

---

<a id="p8-unit"></a>
**Topic 3: Unit Testing — Functions**

```javascript
// src/utils/queryBuilder.js থেকে (PART 6)
// function buildQuery(reqQuery) { ... }

// src/utils/__tests__/queryBuilder.test.js
const { buildQuery } = require('../queryBuilder');

describe('buildQuery', () => {

    // ────────────────────────────────────────────
    // Happy path
    // ────────────────────────────────────────────
    it('should return default pagination values', () => {
        const result = buildQuery({});
        expect(result.page).toBe(1);
        expect(result.limit).toBe(10);
        expect(result.skip).toBe(0);
        expect(result.sort).toBe('-createdAt');
    });

    it('should calculate skip correctly', () => {
        const result = buildQuery({ page: '3', limit: '20' });
        expect(result.skip).toBe(40);  // (3-1) * 20
        expect(result.page).toBe(3);
        expect(result.limit).toBe(20);
    });

    it('should apply search filter', () => {
        const result = buildQuery({ search: 'alice' });
        expect(result.filter.$or).toBeDefined();
        expect(result.filter.$or[0].name.$regex).toBe('alice');
    });

    it('should convert comparison operators', () => {
        const result = buildQuery({ age: { gte: '18', lte: '30' } });
        expect(result.filter.age.$gte).toBe('18');
        expect(result.filter.age.$lte).toBe('30');
    });

    // ────────────────────────────────────────────
    // Edge cases
    // ────────────────────────────────────────────
    it('should cap limit at 100', () => {
        const result = buildQuery({ limit: '999' });
        expect(result.limit).toBe(100);
    });

    it('should use minimum page 1', () => {
        const result = buildQuery({ page: '-5' });
        expect(result.page).toBe(1);
    });

    it('should select specified fields', () => {
        const result = buildQuery({ fields: 'name,email,role' });
        expect(result.select).toBe('name email role');
    });
});

// ────────────────────────────────────────────
// Service unit test
// ────────────────────────────────────────────
// src/services/__tests__/authService.test.js
const { hashPassword, verifyPassword } = require('../authService');

describe('Auth Utilities', () => {
    const plainPassword = 'TestPass123!';

    it('should hash a password', async () => {
        const hash = await hashPassword(plainPassword);
        expect(hash).toBeDefined();
        expect(hash).not.toBe(plainPassword);
        expect(hash.startsWith('$2')).toBe(true);  // bcrypt prefix
    });

    it('should produce different hashes for same password', async () => {
        const hash1 = await hashPassword(plainPassword);
        const hash2 = await hashPassword(plainPassword);
        expect(hash1).not.toBe(hash2);  // different salt each time
    });

    it('should verify correct password', async () => {
        const hash = await hashPassword(plainPassword);
        const isValid = await verifyPassword(plainPassword, hash);
        expect(isValid).toBe(true);
    });

    it('should reject wrong password', async () => {
        const hash = await hashPassword(plainPassword);
        const isValid = await verifyPassword('WrongPass', hash);
        expect(isValid).toBe(false);
    });
});
```

---

<a id="p8-mocking"></a>
**Topic 4: Mocking — jest.mock ও jest.fn**

```javascript
// ────────────────────────────────────────────
// Manual mock — jest.fn()
// ────────────────────────────────────────────
const mockSave = jest.fn().mockResolvedValue({ _id: '123', name: 'Alice' });

// ────────────────────────────────────────────
// Module mock — jest.mock()
// ────────────────────────────────────────────
// src/services/__tests__/userService.test.js
jest.mock('../../models/User');           // Mongoose model mock
jest.mock('../../utils/email');           // Email service mock

const User = require('../../models/User');
const emailService = require('../../utils/email');
const userService = require('../userService');

describe('UserService', () => {

    beforeEach(() => {
        jest.clearAllMocks();  // প্রতিটি test-এর আগে mocks reset
    });

    describe('createUser', () => {
        it('should create user successfully', async () => {
            const mockUser = { _id: '507f1f77bcf86cd799439011', name: 'Alice', email: 'alice@test.com' };
            User.findOne.mockResolvedValue(null);          // no existing user
            User.create.mockResolvedValue(mockUser);       // user created
            emailService.sendWelcome.mockResolvedValue();  // email sent

            const result = await userService.createUser({
                name: 'Alice',
                email: 'alice@test.com',
                password: 'Pass123!'
            });

            expect(User.findOne).toHaveBeenCalledWith({ email: 'alice@test.com' });
            expect(User.create).toHaveBeenCalledTimes(1);
            expect(emailService.sendWelcome).toHaveBeenCalledWith('alice@test.com', 'Alice');
            expect(result).toEqual(mockUser);
        });

        it('should throw conflict if email exists', async () => {
            User.findOne.mockResolvedValue({ email: 'alice@test.com' });

            await expect(
                userService.createUser({ email: 'alice@test.com', password: 'Pass123!' })
            ).rejects.toThrow('Email already registered');

            expect(User.create).not.toHaveBeenCalled();
        });
    });
});

// ────────────────────────────────────────────
// Spy — real function + track calls
// ────────────────────────────────────────────
const logger = require('../../utils/logger');
const loggerSpy = jest.spyOn(logger, 'error').mockImplementation(() => {});

// test code...

expect(loggerSpy).toHaveBeenCalledWith(expect.objectContaining({
    message: 'User not found'
}));

loggerSpy.mockRestore();  // original restore

// ────────────────────────────────────────────
// Timer mocks
// ────────────────────────────────────────────
jest.useFakeTimers();

const callback = jest.fn();
setTimeout(callback, 1000);

jest.advanceTimersByTime(1000);
expect(callback).toHaveBeenCalled();

jest.useRealTimers();
```

---

<a id="p8-supertest"></a>
**Topic 5: Integration Testing — Supertest**

```javascript
// src/tests/integration/users.test.js
const request = require('supertest');
const app = require('../../app');  // Express app (server.listen ছাড়া)
const User = require('../../models/User');

describe('Users API', () => {

    let authToken;
    let testUser;

    // Test user তৈরি ও login করো
    beforeEach(async () => {
        testUser = await User.create({
            name: 'Alice',
            email: 'alice@test.com',
            password: 'TestPass123!',
            role: 'user'
        });

        const loginRes = await request(app)
            .post('/api/auth/login')
            .send({ email: 'alice@test.com', password: 'TestPass123!' });

        authToken = loginRes.body.data.accessToken;
    });

    // ────────────────────────────────────────────
    // GET /api/users
    // ────────────────────────────────────────────
    describe('GET /api/users', () => {
        it('should return users list for authenticated user', async () => {
            const res = await request(app)
                .get('/api/users')
                .set('Authorization', `Bearer ${authToken}`);

            expect(res.status).toBe(200);
            expect(res.body.success).toBe(true);
            expect(Array.isArray(res.body.data)).toBe(true);
            expect(res.body.pagination).toBeDefined();
        });

        it('should return 401 for unauthenticated request', async () => {
            const res = await request(app).get('/api/users');
            expect(res.status).toBe(401);
            expect(res.body.success).toBe(false);
        });

        it('should paginate correctly', async () => {
            // 5 জন user তৈরি করো
            await User.insertMany(
                Array.from({ length: 5 }, (_, i) => ({
                    name: `User ${i}`, email: `user${i}@test.com`,
                    password: 'Pass123!'
                }))
            );

            const res = await request(app)
                .get('/api/users?page=1&limit=3')
                .set('Authorization', `Bearer ${authToken}`);

            expect(res.body.data.length).toBe(3);
            expect(res.body.pagination.total).toBeGreaterThan(3);
            expect(res.body.pagination.hasNext).toBe(true);
        });
    });

    // ────────────────────────────────────────────
    // POST /api/users (admin only)
    // ────────────────────────────────────────────
    describe('POST /api/users', () => {
        it('should create user with valid data', async () => {
            const adminToken = await getAdminToken();  // helper

            const res = await request(app)
                .post('/api/users')
                .set('Authorization', `Bearer ${adminToken}`)
                .send({
                    name: 'Bob',
                    email: 'bob@test.com',
                    password: 'BobPass123!'
                });

            expect(res.status).toBe(201);
            expect(res.body.data.email).toBe('bob@test.com');
            expect(res.body.data.password).toBeUndefined();  // sensitive field hidden
        });

        it('should return 400 for invalid email', async () => {
            const adminToken = await getAdminToken();

            const res = await request(app)
                .post('/api/users')
                .set('Authorization', `Bearer ${adminToken}`)
                .send({ name: 'Bob', email: 'not-an-email', password: 'Pass123!' });

            expect(res.status).toBe(400);
            expect(res.body.error.code).toBe('VALIDATION_ERROR');
        });

        it('should return 409 for duplicate email', async () => {
            const adminToken = await getAdminToken();

            const res = await request(app)
                .post('/api/users')
                .set('Authorization', `Bearer ${adminToken}`)
                .send({ name: 'Alice 2', email: 'alice@test.com', password: 'Pass123!' });

            expect(res.status).toBe(409);
        });
    });
});
```

---

<a id="p8-db-testing"></a>
**Topic 6: Database Testing — In-memory MongoDB**

```bash
npm install --save-dev mongodb-memory-server
```

```javascript
// src/tests/setup.js — global setup (PART 8 Topic 2-এ দেখেছি)

// ────────────────────────────────────────────
// Model-level testing
// ────────────────────────────────────────────
// src/models/__tests__/User.test.js
const mongoose = require('mongoose');
const User = require('../User');

describe('User Model', () => {

    describe('Schema Validation', () => {
        it('should create valid user', async () => {
            const user = await User.create({
                name: 'Alice',
                email: 'alice@test.com',
                password: 'hashed_password'
            });

            expect(user._id).toBeDefined();
            expect(user.name).toBe('Alice');
            expect(user.email).toBe('alice@test.com');
            expect(user.role).toBe('user');  // default
            expect(user.isActive).toBe(true);  // default
            expect(user.createdAt).toBeDefined();
        });

        it('should require email', async () => {
            await expect(
                User.create({ name: 'Alice', password: 'pass' })
            ).rejects.toThrow(/email.*required/i);
        });

        it('should enforce unique email', async () => {
            await User.create({ name: 'A', email: 'same@test.com', password: 'pass' });
            await expect(
                User.create({ name: 'B', email: 'same@test.com', password: 'pass' })
            ).rejects.toThrow(/duplicate|unique/i);
        });
    });

    describe('Instance Methods', () => {
        it('should hash password before save', async () => {
            const user = await User.create({
                name: 'Alice', email: 'alice2@test.com', password: 'PlainPass123'
            });
            expect(user.password).not.toBe('PlainPass123');
            expect(user.password.startsWith('$2')).toBe(true);
        });

        it('comparePassword should return true for correct password', async () => {
            const user = await User.create({
                name: 'Alice', email: 'alice3@test.com', password: 'PlainPass123'
            });
            const isValid = await user.comparePassword('PlainPass123');
            expect(isValid).toBe(true);
        });

        it('toSafeObject should not include password', async () => {
            const user = await User.create({
                name: 'Alice', email: 'alice4@test.com', password: 'PlainPass123'
            });
            const safe = user.toSafeObject();
            expect(safe.password).toBeUndefined();
            expect(safe.name).toBe('Alice');
        });
    });
});
```

---

<a id="p8-utilities"></a>
**Topic 7: Test Utilities ও Factories**

```javascript
// src/tests/utils/factories.js

const User = require('../../models/User');
const { generateAccessToken } = require('../../utils/jwt');

// ────────────────────────────────────────────
// User factory
// ────────────────────────────────────────────
let userCounter = 0;

async function createUser(overrides = {}) {
    userCounter++;
    const defaults = {
        name: `Test User ${userCounter}`,
        email: `testuser${userCounter}@test.com`,
        password: 'TestPass123!',
        role: 'user',
        isActive: true
    };
    return User.create({ ...defaults, ...overrides });
}

async function createAdmin(overrides = {}) {
    return createUser({ ...overrides, role: 'admin' });
}

// ────────────────────────────────────────────
// Auth token helpers
// ────────────────────────────────────────────
async function getAuthToken(overrides = {}) {
    const user = await createUser(overrides);
    const token = generateAccessToken(user);
    return { user, token };
}

async function getAdminToken() {
    const admin = await createAdmin();
    const token = generateAccessToken(admin);
    return { admin, token };
}

// Helper: auth header
function authHeader(token) {
    return { Authorization: `Bearer ${token}` };
}

module.exports = { createUser, createAdmin, getAuthToken, getAdminToken, authHeader };

// ────────────────────────────────────────────
// Usage in tests
// ────────────────────────────────────────────
const { getAuthToken, getAdminToken, authHeader } = require('../utils/factories');

it('should update own profile', async () => {
    const { user, token } = await getAuthToken();

    const res = await request(app)
        .patch(`/api/users/${user._id}`)
        .set(authHeader(token))
        .send({ name: 'New Name' });

    expect(res.status).toBe(200);
    expect(res.body.data.name).toBe('New Name');
});
```

---

<a id="p8-coverage"></a>
**Topic 8: Code Coverage**

```bash
# Coverage report generate করুন
npm run test:coverage

# Output:
# ------------------|---------|----------|---------|---------|
# File              | % Stmts | % Branch | % Funcs | % Lines |
# ------------------|---------|----------|---------|---------|
# All files         |   85.23 |    72.45 |   88.12 |   85.01 |
#  src/             |         |          |         |         |
#   app.js          |   100   |   100    |   100   |   100   |
#  src/services/    |         |          |         |         |
#   authService.js  |   92.30 |    78.57 |   90.00 |   92.30 |
#   userService.js  |   78.94 |    65.00 |   83.33 |   78.94 |
# ------------------|---------|----------|---------|---------|
```

```json
// jest.config.js — coverage thresholds enforce করুন
{
  "coverageThresholds": {
    "global": {
      "branches": 70,
      "functions": 80,
      "lines": 80
    },
    "./src/services/": {
      "lines": 90
    }
  }
}
```

```
Coverage Metrics:
Statements: প্রতিটি statement execute হয়েছে?
Branches:   if/else/ternary সব branches hit?
Functions:  সব functions call হয়েছে?
Lines:      সব lines execute হয়েছে?

100% coverage = bug-free নয়!
Coverage দেখায় কোড executed হয়েছে — সঠিক কিনা নয়।
Meaningful assertions > high coverage।
```

---

<a id="p8-best-practices"></a>
**Topic 9: Testing Best Practices**

```javascript
// ────────────────────────────────────────────
// 1. AAA Pattern: Arrange, Act, Assert
// ────────────────────────────────────────────
it('should return user by id', async () => {
    // Arrange — test data prepare
    const user = await createUser({ name: 'Alice' });

    // Act — function/endpoint call
    const res = await request(app)
        .get(`/api/users/${user._id}`)
        .set(authHeader(token));

    // Assert — result verify
    expect(res.status).toBe(200);
    expect(res.body.data.name).toBe('Alice');
});

// ────────────────────────────────────────────
// 2. Test naming: "should [behavior] when [condition]"
// ────────────────────────────────────────────
it('should return 404 when user does not exist', ...)
it('should hash password before saving to database', ...)
it('should return 401 when token is expired', ...)

// ────────────────────────────────────────────
// 3. One assertion per test (ideally)
// ────────────────────────────────────────────
// ❌ Too many assertions — hard to know which failed
it('should create user', async () => {
    const res = await createUser();
    expect(res.status).toBe(201);
    expect(res.body.data.name).toBeDefined();
    expect(res.body.data.password).toBeUndefined();
    expect(res.body.data.role).toBe('user');
    expect(res.body.data.createdAt).toBeDefined();
});

// ✅ Focused tests
it('should return 201 on user creation', async () => { ... });
it('should not expose password in response', async () => { ... });

// ────────────────────────────────────────────
// 4. Test isolation
// ────────────────────────────────────────────
// প্রতিটি test নিজের data তৈরি করুক
// beforeEach-এ DB clean করুন (setup.js-এ আছে)
// Shared state avoid করুন

// ────────────────────────────────────────────
// 5. Test what users care about
// ────────────────────────────────────────────
// ❌ Implementation details test করবেন না
expect(User.findOne).toHaveBeenCalledWith({ _id: id });  // internal detail

// ✅ Behavior test করুন
expect(res.body.data.name).toBe('Alice');
expect(res.status).toBe(200);

// ────────────────────────────────────────────
// 6. Error cases test করুন
// ────────────────────────────────────────────
// Happy path + sad path + edge cases
// "3 tests minimum per endpoint: success, not found, unauthorized"
```

---

<a id="p8-qa"></a>
**Topic 10: PART 8 Interview Q&A**

```
প্রশ্ন: Unit test vs Integration test পার্থক্য?
উত্তর:
Unit test: একটি function/module isolated test।
External dependencies mock করা হয়।
Fast, specific, many।

Integration test: Multiple components একসাথে।
Real DB (in-memory), HTTP requests।
Slower, broader coverage।

প্রশ্ন: Test pyramid কী?
উত্তর: Testing strategy:
Base: Unit tests (70%) — fast, cheap, isolated।
Middle: Integration tests (20%) — API + DB।
Top: E2E tests (10%) — full browser flow, slow, brittle।
বেশি unit test, কম E2E — fast feedback।

প্রশ্ন: Mocking কেন করি?
উত্তর: External dependencies isolate করতে।
DB call mock → tests faster, no actual DB দরকার।
Email service mock → test-এ actual email না যাক।
3rd party API mock → network ছাড়া test।
Deterministic results: mock return value control করা যায়।

প্রশ্ন: 100% test coverage মানে কি bug নেই?
উত্তর: না। Coverage মানে lines execute হয়েছে।
Assertion ভুল হলে coverage আছে কিন্তু bug আছে।
Missing edge cases cover করে না।
Integration between components test করে না।
Meaningful assertions দরকার, শুধু coverage না।

প্রশ্ন: catchAsync কে কি unit test করা সম্ভব?
উত্তর: হ্যাঁ। Handler function directly call করুন,
বা mock req/res/next দিয়ে।
Express app-এ supertest দিয়ে integration test বেশি practical।

প্রশ্ন: MongoMemoryServer কী? কেন ব্যবহার করি?
উত্তর: In-memory MongoDB — real MongoDB engine, disk নেই।
Tests real DB-তে dependency নেই।
CI/CD-এ MongoDB setup ছাড়াই চলে।
প্রতিটি test suite clean state — isolation guaranteed।
```

---

**PART 8 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| Test Pyramid | Unit 70% / Integration 20% / E2E 10% |
| Jest | Zero-config test framework |
| `describe` | Test grouping |
| `it` / `test` | Single test case |
| `beforeAll/afterAll` | Suite setup/teardown |
| `beforeEach/afterEach` | Per-test setup/teardown |
| `expect().toBe()` | Strict equality |
| `expect().toEqual()` | Deep equality |
| `expect().rejects.toThrow()` | Async error test |
| `jest.fn()` | Mock function |
| `jest.mock()` | Module mock |
| `jest.spyOn()` | Spy on real function |
| `jest.clearAllMocks()` | Reset mock state |
| Supertest | HTTP integration testing |
| `request(app).get()` | Make HTTP test request |
| MongoMemoryServer | In-memory MongoDB for tests |
| AAA Pattern | Arrange, Act, Assert |
| Coverage | Statement / Branch / Function / Line |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 9 — Performance ও Security

---

<a id="part9"></a>
## PART 9: Performance ও Security

> Rate limiting, helmet, Redis caching, compression, clustering, SQL/NoSQL injection prevention, XSS, CSRF — production-ready security ও performance।

| # | বিষয় |
|---|-------|
| 1 | [Security Headers — Helmet](#p9-helmet) |
| 2 | [Rate Limiting](#p9-rate-limit) |
| 3 | [Input Sanitization — XSS ও Injection](#p9-sanitize) |
| 4 | [Redis Caching](#p9-redis) |
| 5 | [Response Compression](#p9-compression) |
| 6 | [Clustering ও Worker Threads](#p9-clustering) |
| 7 | [Database Query Optimization](#p9-db-perf) |
| 8 | [Memory Leak Prevention](#p9-memory) |
| 9 | [Security Checklist](#p9-security-checklist) |
| 10 | [PART 9 Interview Q&A](#p9-qa) |

---

<a id="p9-helmet"></a>
**Topic 1: Security Headers — Helmet**

```bash
npm install helmet
```

```javascript
const helmet = require('helmet');

// ────────────────────────────────────────────
// Default helmet — সব headers একসাথে
// ────────────────────────────────────────────
app.use(helmet());

// ────────────────────────────────────────────
// Helmet কী করে?
// ────────────────────────────────────────────
// Content-Security-Policy    — XSS prevent: কোন scripts load হবে
// X-Content-Type-Options     — MIME sniffing prevent: nosniff
// X-Frame-Options            — Clickjacking prevent: DENY
// Strict-Transport-Security  — HTTPS force (HSTS)
// X-XSS-Protection           — Old browsers XSS filter
// Referrer-Policy            — Referrer info control
// Permissions-Policy         — Browser features restrict

// ────────────────────────────────────────────
// Custom configuration
// ────────────────────────────────────────────
app.use(helmet({
    contentSecurityPolicy: {
        directives: {
            defaultSrc: ["'self'"],
            styleSrc: ["'self'", 'https://fonts.googleapis.com'],
            fontSrc: ["'self'", 'https://fonts.gstatic.com'],
            imgSrc: ["'self'", 'data:', 'https:'],
            scriptSrc: ["'self'"]
        }
    },
    hsts: {
        maxAge: 31536000,       // 1 year
        includeSubDomains: true,
        preload: true
    },
    frameguard: { action: 'deny' }
}));

// ────────────────────────────────────────────
// Response headers চেক করুন
// ────────────────────────────────────────────
// Before helmet:
// (no security headers)

// After helmet:
// X-Content-Type-Options: nosniff
// X-Frame-Options: DENY
// Strict-Transport-Security: max-age=31536000; includeSubDomains; preload
// Content-Security-Policy: default-src 'self'; ...
```

---

<a id="p9-rate-limit"></a>
**Topic 2: Rate Limiting**

```bash
npm install express-rate-limit rate-limit-redis
```

```javascript
const rateLimit = require('express-rate-limit');
const RedisStore = require('rate-limit-redis');
const redisClient = require('./utils/redis');

// ────────────────────────────────────────────
// Basic rate limiter
// ────────────────────────────────────────────
const globalLimiter = rateLimit({
    windowMs: 15 * 60 * 1000,  // 15 minutes
    max: 100,                   // 100 requests per window
    standardHeaders: true,      // RateLimit-* headers return
    legacyHeaders: false,
    message: {
        success: false,
        error: { message: 'Too many requests. Try again in 15 minutes.', code: 'RATE_LIMIT' }
    }
});

app.use('/api/', globalLimiter);

// ────────────────────────────────────────────
// Specific limiters
// ────────────────────────────────────────────
// Auth routes — strict
const authLimiter = rateLimit({
    windowMs: 15 * 60 * 1000,
    max: 5,                     // 5 attempts per 15 min
    skipSuccessfulRequests: true
});
app.use('/api/auth/login', authLimiter);
app.use('/api/auth/register', authLimiter);

// Password reset — very strict
const resetLimiter = rateLimit({
    windowMs: 60 * 60 * 1000,  // 1 hour
    max: 3                      // 3 attempts per hour
});
app.use('/api/auth/forgot-password', resetLimiter);

// Upload — bandwidth protect
const uploadLimiter = rateLimit({
    windowMs: 60 * 1000,
    max: 10                     // 10 uploads per minute
});
app.use('/api/upload', uploadLimiter);

// ────────────────────────────────────────────
// Redis store (distributed — multiple servers)
// ────────────────────────────────────────────
const distributedLimiter = rateLimit({
    windowMs: 15 * 60 * 1000,
    max: 100,
    store: new RedisStore({
        sendCommand: (...args) => redisClient.sendCommand(args)
    })
});

// ────────────────────────────────────────────
// Custom key — IP + user (authenticated)
// ────────────────────────────────────────────
const userLimiter = rateLimit({
    windowMs: 60 * 1000,
    max: 60,
    keyGenerator: (req) => {
        return req.user ? `user:${req.user.id}` : `ip:${req.ip}`;
    }
});
```

---

<a id="p9-sanitize"></a>
**Topic 3: Input Sanitization — XSS ও Injection**

```bash
npm install express-mongo-sanitize xss-clean hpp
```

```javascript
const mongoSanitize = require('express-mongo-sanitize');
const xssClean = require('xss-clean');
const hpp = require('hpp');

// ────────────────────────────────────────────
// NoSQL Injection prevent
// ────────────────────────────────────────────
// Attack: { "email": { "$gt": "" } } → all users access
app.use(mongoSanitize());
// $ ও . remove করে request body/query/params থেকে

// Manual check
function sanitizeMongoQuery(obj) {
    if (typeof obj === 'object' && obj !== null) {
        for (const key of Object.keys(obj)) {
            if (key.startsWith('$') || key.includes('.')) {
                delete obj[key];
            } else {
                sanitizeMongoQuery(obj[key]);
            }
        }
    }
    return obj;
}

// ────────────────────────────────────────────
// XSS prevent
// ────────────────────────────────────────────
// Attack: name = "<script>document.cookie</script>"
app.use(xssClean());
// HTML entities encode করে: < → &lt;, > → &gt;

// Manual sanitize
const escapeHtml = (str) => {
    if (typeof str !== 'string') return str;
    return str
        .replace(/&/g, '&amp;')
        .replace(/</g, '&lt;')
        .replace(/>/g, '&gt;')
        .replace(/"/g, '&quot;')
        .replace(/'/g, '&#x27;');
};

// ────────────────────────────────────────────
// SQL Injection (PostgreSQL/pg-এ)
// ────────────────────────────────────────────
// ❌ Vulnerable — string concatenation
const query = `SELECT * FROM users WHERE email = '${email}'`;
// Attack: email = "' OR '1'='1" → all users

// ✅ Safe — parameterized queries
const { rows } = await pool.query(
    'SELECT * FROM users WHERE email = $1',
    [email]  // driver handles escaping
);

// Knex also safe
const user = await db('users').where({ email }).first();

// ────────────────────────────────────────────
// HTTP Parameter Pollution (HPP)
// ────────────────────────────────────────────
// Attack: GET /api?sort=name&sort=password → array-এ confusion
app.use(hpp({
    whitelist: ['tags', 'categories']  // these can be arrays
}));

// ────────────────────────────────────────────
// Body size limit
// ────────────────────────────────────────────
app.use(express.json({ limit: '10kb' }));     // 10KB max
app.use(express.urlencoded({ extended: true, limit: '10kb' }));
```

---

<a id="p9-redis"></a>
**Topic 4: Redis Caching**

```bash
npm install ioredis
```

```javascript
// src/utils/redis.js
const Redis = require('ioredis');
const config = require('../config/env');

const redis = new Redis({
    host: config.redisHost,
    port: config.redisPort,
    password: config.redisPassword,
    retryStrategy: (times) => Math.min(times * 50, 2000),
    maxRetriesPerRequest: 3
});

redis.on('connect', () => console.log('Redis connected'));
redis.on('error', (err) => console.error('Redis error:', err));

module.exports = redis;

// ────────────────────────────────────────────
// Cache middleware — GET requests
// ────────────────────────────────────────────
const redis = require('../utils/redis');

function cacheMiddleware(ttl = 300) {  // 5 minutes default
    return async (req, res, next) => {
        if (req.method !== 'GET') return next();

        const key = `cache:${req.url}`;
        const cached = await redis.get(key);

        if (cached) {
            res.setHeader('X-Cache', 'HIT');
            return res.json(JSON.parse(cached));
        }

        // Original json() override করুন
        const originalJson = res.json.bind(res);
        res.json = async (data) => {
            await redis.setex(key, ttl, JSON.stringify(data));
            res.setHeader('X-Cache', 'MISS');
            return originalJson(data);
        };

        next();
    };
}

// Route-এ apply
router.get('/products', cacheMiddleware(600), productController.getAll);
router.get('/categories', cacheMiddleware(3600), categoryController.getAll);

// ────────────────────────────────────────────
// Cache invalidation
// ────────────────────────────────────────────
async function invalidateCache(pattern) {
    const keys = await redis.keys(`cache:${pattern}`);
    if (keys.length > 0) {
        await redis.del(...keys);
    }
}

// Product update হলে cache clear
exports.updateProduct = catchAsync(async (req, res) => {
    const product = await Product.findByIdAndUpdate(req.params.id, req.body, { new: true });
    await invalidateCache('/api/products*');  // product list cache clear
    res.json({ success: true, data: product });
});

// ────────────────────────────────────────────
// Specific data caching
// ────────────────────────────────────────────
async function getUserById(id) {
    const cacheKey = `user:${id}`;
    
    // Cache hit?
    const cached = await redis.get(cacheKey);
    if (cached) return JSON.parse(cached);

    // DB থেকে fetch
    const user = await User.findById(id).lean();
    if (!user) return null;

    // Cache করুন — 1 hour
    await redis.setex(cacheKey, 3600, JSON.stringify(user));
    return user;
}

// Cache invalidation on update
async function updateUser(id, data) {
    const user = await User.findByIdAndUpdate(id, data, { new: true });
    await redis.del(`user:${id}`);  // cache clear
    return user;
}

// ────────────────────────────────────────────
// Redis কখন ব্যবহার করবেন?
// ────────────────────────────────────────────
// ✅ Frequently read, rarely changed: categories, configs, product lists
// ✅ Session store
// ✅ Rate limiting counters
// ✅ Job queues (Bull/BullMQ)
// ✅ Pub/Sub (realtime features)
// ❌ User-specific data (cache invalidation জটিল)
// ❌ Frequently updated data
```

---

<a id="p9-compression"></a>
**Topic 5: Response Compression**

```bash
npm install compression
```

```javascript
const compression = require('compression');

// ────────────────────────────────────────────
// Basic compression
// ────────────────────────────────────────────
app.use(compression({
    level: 6,         // 1 (fast) to 9 (best) — 6 is balanced
    threshold: 1024,  // 1KB-এর কম compress করবেন না
    filter: (req, res) => {
        // Already compressed content skip করুন
        if (req.headers['x-no-compression']) return false;
        return compression.filter(req, res);
    }
}));

// ────────────────────────────────────────────
// কতটা benefit?
// ────────────────────────────────────────────
// JSON response: 100KB → ~15KB (85% reduction)
// HTML: 200KB → ~30KB
// Images: আগে থেকে compressed — skip

// Client-এ Accept-Encoding: gzip, deflate, br পাঠায়
// Server: Content-Encoding: gzip দিয়ে respond করে
// Browser automatically decompress করে
```

---

<a id="p9-clustering"></a>
**Topic 6: Clustering ও Worker Threads**

```javascript
// ────────────────────────────────────────────
// Cluster module — multi-core CPU ব্যবহার
// ────────────────────────────────────────────
// Node.js single-threaded → single core ব্যবহার
// Cluster: multiple processes, each on a core

const cluster = require('cluster');
const os = require('os');
const numCPUs = os.cpus().length;

if (cluster.isPrimary) {
    console.log(`Primary ${process.pid} running`);
    console.log(`Forking ${numCPUs} workers...`);

    // Worker তৈরি করুন
    for (let i = 0; i < numCPUs; i++) {
        cluster.fork();
    }

    // Worker crash হলে নতুন তৈরি করুন
    cluster.on('exit', (worker, code, signal) => {
        console.log(`Worker ${worker.process.pid} died. Restarting...`);
        cluster.fork();
    });

} else {
    // প্রতিটি worker নিজের Express server চালায়
    const app = require('./app');
    app.listen(process.env.PORT, () => {
        console.log(`Worker ${process.pid} started`);
    });
}

// ────────────────────────────────────────────
// PM2 cluster (recommended — easier)
// ────────────────────────────────────────────
// ecosystem.config.js-এ (PART 10-এ দেখব):
// instances: 'max'  → সব cores

// ────────────────────────────────────────────
// Worker Threads — CPU-intensive tasks
// ────────────────────────────────────────────
// Image processing, cryptography, data parsing
// Event loop block করবেন না!

const { Worker, isMainThread, parentPort, workerData } = require('worker_threads');

// Main thread
if (isMainThread) {
    function runWorker(data) {
        return new Promise((resolve, reject) => {
            const worker = new Worker(__filename, { workerData: data });
            worker.on('message', resolve);
            worker.on('error', reject);
            worker.on('exit', (code) => {
                if (code !== 0) reject(new Error(`Worker exited with code ${code}`));
            });
        });
    }

    // CPU-intensive work offload করুন
    app.post('/process', async (req, res) => {
        const result = await runWorker(req.body);
        res.json({ result });
    });

} else {
    // Worker thread — heavy computation
    const result = heavyComputation(workerData);
    parentPort.postMessage(result);
}

function heavyComputation(data) {
    // CSV parse, image resize, etc.
    return data;
}
```

---

<a id="p9-db-perf"></a>
**Topic 7: Database Query Optimization**

```javascript
// ────────────────────────────────────────────
// MongoDB Indexes
// ────────────────────────────────────────────
// Indexes ছাড়া: full collection scan → O(n)
// Index সহ: B-tree lookup → O(log n)

// Schema-তে index
const userSchema = new Schema({
    email: { type: String, unique: true, index: true },
    createdAt: { type: Date, index: true }
});

// Compound index — frequently queried together
userSchema.index({ role: 1, isActive: 1 });
userSchema.index({ createdAt: -1 });  // sorting-এর জন্য
userSchema.index({ name: 'text', bio: 'text' });  // text search

// explain() দিয়ে query analyze
const plan = await User.find({ email: 'alice@test.com' }).explain('executionStats');
console.log(plan.executionStats.totalDocsExamined);  // 1 = index used
console.log(plan.executionStats.executionTimeMillis);

// ────────────────────────────────────────────
// .lean() — Mongoose overhead কমান
// ────────────────────────────────────────────
// Normal: Mongoose Document object (methods, getters, setters)
// lean(): Plain JS object — 3-4x faster for read-only

const users = await User.find().lean();        // ✅ Read-only queries-এ
const user = await User.findById(id);          // ✅ Update/save দরকার হলে

// ────────────────────────────────────────────
// Projection — শুধু দরকারি fields
// ────────────────────────────────────────────
// ❌ সব fields fetch
const users = await User.find();

// ✅ শুধু দরকারি fields
const users = await User.find().select('name email role').lean();

// ────────────────────────────────────────────
// Aggregation pipeline — DB-তে processing
// ────────────────────────────────────────────
// ❌ JS-এ process — সব data fetch করে
const users = await User.find({ isActive: true });
const adminCount = users.filter(u => u.role === 'admin').length;

// ✅ DB-তে aggregate — শুধু result আসে
const stats = await User.aggregate([
    { $match: { isActive: true } },
    { $group: { _id: '$role', count: { $sum: 1 } } },
    { $sort: { count: -1 } }
]);

// ────────────────────────────────────────────
// Connection pooling
// ────────────────────────────────────────────
await mongoose.connect(config.mongoUri, {
    maxPoolSize: 10,       // max concurrent connections
    minPoolSize: 2,        // min connections kept alive
    serverSelectionTimeoutMS: 5000,
    socketTimeoutMS: 45000
});

// ────────────────────────────────────────────
// N+1 Problem — populate vs aggregate
// ────────────────────────────────────────────
// ❌ N+1: 1 query posts + N query users
const posts = await Post.find();
for (const post of posts) {
    post.author = await User.findById(post.authorId);  // N queries!
}

// ✅ populate — 2 queries
const posts = await Post.find().populate('authorId', 'name email');

// ✅ Aggregate — 1 query
const posts = await Post.aggregate([
    { $lookup: {
        from: 'users',
        localField: 'authorId',
        foreignField: '_id',
        as: 'author'
    }},
    { $unwind: '$author' }
]);
```

---

<a id="p9-memory"></a>
**Topic 8: Memory Leak Prevention**

```javascript
// ────────────────────────────────────────────
// Common memory leaks
// ────────────────────────────────────────────

// 1. Event listener leak
// ❌ প্রতি request-এ নতুন listener
app.use((req, res, next) => {
    emitter.on('data', (data) => {
        res.write(data);  // listener never removed!
    });
    next();
});

// ✅ Cleanup listener
app.use((req, res, next) => {
    const handler = (data) => res.write(data);
    emitter.on('data', handler);
    res.on('close', () => emitter.off('data', handler));  // cleanup
    next();
});

// 2. Unbounded cache (Map/object that grows forever)
// ❌
const cache = {};
app.get('/data/:id', (req, res) => {
    cache[req.params.id] = expensiveData;  // grows forever!
});

// ✅ LRU cache with limit
const LRU = require('lru-cache');
const cache = new LRU({ max: 500, ttl: 1000 * 60 * 5 });

// 3. Unclosed DB connections/streams
// Always close:
const stream = fs.createReadStream(file);
stream.on('end', () => stream.destroy());
stream.on('error', () => stream.destroy());

// ────────────────────────────────────────────
// Memory monitoring
// ────────────────────────────────────────────
function logMemoryUsage() {
    const { heapUsed, heapTotal, external, rss } = process.memoryUsage();
    logger.info('Memory usage', {
        heapUsed: `${Math.round(heapUsed / 1024 / 1024)}MB`,
        heapTotal: `${Math.round(heapTotal / 1024 / 1024)}MB`,
        rss: `${Math.round(rss / 1024 / 1024)}MB`
    });
}

setInterval(logMemoryUsage, 60 * 1000);  // every minute

// Health endpoint-এ
app.get('/health', (req, res) => {
    const { heapUsed, heapTotal } = process.memoryUsage();
    res.json({
        status: 'ok',
        uptime: process.uptime(),
        memory: {
            used: Math.round(heapUsed / 1024 / 1024),
            total: Math.round(heapTotal / 1024 / 1024)
        }
    });
});
```

---

<a id="p9-security-checklist"></a>
**Topic 9: Security Checklist**

```
Production Security Checklist:

Authentication & Authorization
✅ JWT: short expiry (15min) + refresh token
✅ bcrypt salt rounds >= 12
✅ Rate limiting on auth endpoints (5 attempts/15min)
✅ Account lockout after failed attempts
✅ Password strength validation
✅ RBAC: role ও permission check
✅ Sensitive routes: requireAuth middleware

Data Security
✅ helmet() — security headers
✅ mongoSanitize() — NoSQL injection prevent
✅ xssClean() — XSS prevent
✅ Parameterized queries — SQL injection prevent
✅ Input validation (express-validator)
✅ Body size limit (10kb)
✅ hpp() — HTTP parameter pollution

Transport Security
✅ HTTPS only in production
✅ HSTS header
✅ Secure cookies (httpOnly, secure, sameSite)
✅ CORS: specific origins only
✅ credentials: true সাবধানে

Secrets Management
✅ .env file — never commit to git
✅ .gitignore-এ .env
✅ Strong random secrets (crypto.randomBytes)
✅ Different secrets per environment
✅ Secrets rotation plan

Infrastructure
✅ Dependencies update: npm audit
✅ Node.js LTS version
✅ Error messages: no stack traces in production
✅ Logging: no sensitive data
✅ Rate limiting: global + specific
✅ PM2 / Docker: non-root user
```

---

<a id="p9-qa"></a>
**Topic 10: PART 9 Interview Q&A**

```
প্রশ্ন: Node.js-এ XSS prevent কীভাবে করবেন?
উত্তর:
Input side: xss-clean middleware — HTML entities encode।
Output side: template engine auto-escape (EJS, Pug)।
React/Vue: JSX/templates automatically escape।
CSP header (helmet): inline scripts block করে।
Never: innerHTML = userInput, eval(userInput)।

প্রশ্ন: NoSQL injection কী? MongoDB-তে কীভাবে হয়?
উত্তর:
MongoDB operator inject: { "password": { "$gt": "" } }
যদি direct req.body MongoDB query-তে যায়।
Express: req.body.password = { $gt: "" } → all passwords match করে।
Solution: express-mongo-sanitize — $ ও . remove।
Manual: object keys validate করুন।

প্রশ্ন: Redis কেন cache হিসেবে ব্যবহার করি?
উত্তর: RAM-based — microsecond read/write (DB: milliseconds)।
Frequently read, rarely changed data cache করি।
Categories, configs, product lists।
Horizontal scaling-এ shared cache — সব servers একই data।
TTL support — automatic expiry।

প্রশ্ন: Node.js clustering কী?
উত্তর: Node.js single-threaded — একটি CPU core ব্যবহার।
Cluster: N worker processes, প্রতিটি একটি core।
Master process: incoming connections distribute।
CPU-bound: clustering improve করে।
I/O-bound (most web apps): less benefit — async already efficient।
Production: PM2 -i max (all cores)।

প্রশ্ন: N+1 problem কী?
উত্তর: 1 query দিয়ে N items fetch, তারপর প্রতিটির জন্য আলাদা query।
1 + N = N+1 total queries।
10 posts → 1 (posts) + 10 (authors) = 11 queries।
Solution: Mongoose populate (2 queries) বা aggregate $lookup (1 query)।

প্রশ্ন: .lean() কখন ব্যবহার করবেন?
উত্তর: Read-only queries-এ — list page, API responses।
Plain JS object — Mongoose Document overhead নেই।
3-4x faster, less memory।
save(), instance methods দরকার হলে lean() না।
```

---

**PART 9 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| helmet() | Security headers — XSS, clickjacking, HSTS |
| CSP | Content-Security-Policy — script sources control |
| rateLimit() | windowMs + max — brute force prevent |
| mongoSanitize() | NoSQL injection — $ ও . remove |
| xssClean() | XSS — HTML entities encode |
| Parameterized query | SQL injection prevent — `$1` placeholder |
| hpp() | HTTP parameter pollution prevent |
| Redis cache | RAM-based — fast read/write |
| cacheMiddleware | GET request cache — TTL সহ |
| Cache invalidation | Update-এ cache clear |
| compression() | gzip — response size 80% কমে |
| cluster | Multi-core — N worker processes |
| Worker Threads | CPU-intensive tasks — event loop block না |
| .lean() | Plain JS object — 3-4x faster read |
| index() | MongoDB query speedup |
| N+1 | Loop-এ query → populate দিয়ে solve |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part10"></a>
## PART 10: Deployment ও DevOps

> Docker, PM2, Nginx, GitHub Actions CI/CD, environment config, health checks এবং production deployment checklist।

| # | বিষয় |
|---|-------|
| 1 | [Environment Configuration](#p10-env) |
| 2 | [PM2 Process Manager](#p10-pm2) |
| 3 | [Docker — Dockerfile ও docker-compose](#p10-docker) |
| 4 | [Nginx Reverse Proxy](#p10-nginx) |
| 5 | [GitHub Actions CI/CD](#p10-cicd) |
| 6 | [Health Check Endpoint](#p10-health) |
| 7 | [Complete Project Structure](#p10-structure) |
| 8 | [Production Checklist](#p10-checklist) |
| 9 | [Interview Quick Revision](#p10-revision) |
| 10 | [PART 10 Interview Q&A](#p10-qa) |

---

<a id="p10-env"></a>
**Topic 1: Environment Configuration**

```bash
npm install dotenv envalid
```

```javascript
// .env (never commit!)
NODE_ENV=production
PORT=3000

MONGO_URI=mongodb+srv://user:pass@cluster.mongodb.net/mydb
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=your_redis_password

JWT_SECRET=super-long-random-secret-min-32-chars
JWT_REFRESH_SECRET=another-super-long-random-secret
JWT_EXPIRES_IN=15m
JWT_REFRESH_EXPIRES_IN=7d

BCRYPT_ROUNDS=12
SESSION_SECRET=session-secret-here

GOOGLE_CLIENT_ID=...
GOOGLE_CLIENT_SECRET=...

FRONTEND_URL=https://myapp.com
API_URL=https://api.myapp.com
CORS_ORIGINS=https://myapp.com,https://www.myapp.com

EMAIL_HOST=smtp.sendgrid.net
EMAIL_PORT=587
EMAIL_USER=apikey
EMAIL_PASS=SG.xxx

AWS_ACCESS_KEY_ID=...
AWS_SECRET_ACCESS_KEY=...
AWS_S3_BUCKET=my-bucket
AWS_REGION=ap-southeast-1
```

```javascript
// src/config/env.js — validated config
const { cleanEnv, str, port, num, bool, url } = require('envalid');

const env = cleanEnv(process.env, {
    NODE_ENV:              str({ choices: ['development', 'test', 'production'] }),
    PORT:                  port({ default: 3000 }),

    MONGO_URI:             str(),
    REDIS_HOST:            str({ default: 'localhost' }),
    REDIS_PORT:            port({ default: 6379 }),

    JWT_SECRET:            str({ minLength: 32 }),
    JWT_REFRESH_SECRET:    str({ minLength: 32 }),
    JWT_EXPIRES_IN:        str({ default: '15m' }),
    JWT_REFRESH_EXPIRES_IN: str({ default: '7d' }),

    BCRYPT_ROUNDS:         num({ default: 12 }),
    FRONTEND_URL:          url(),
    CORS_ORIGINS:          str()
});

module.exports = {
    ...env,
    isDev:  env.NODE_ENV === 'development',
    isProd: env.NODE_ENV === 'production',
    isTest: env.NODE_ENV === 'test',
    corsOrigins: env.CORS_ORIGINS.split(',').map(s => s.trim())
};

// index.js-এ সবার আগে:
require('dotenv').config();
const config = require('./config/env');  // validation এখানে হয়
```

```
.gitignore-এ:
.env
.env.*
!.env.example

.env.example (commit করুন — template):
NODE_ENV=development
PORT=3000
MONGO_URI=mongodb://localhost:27017/myapp
JWT_SECRET=change-this-to-random-32-char-string
...
```

---

<a id="p10-pm2"></a>
**Topic 2: PM2 Process Manager**

```bash
npm install -g pm2
```

```javascript
// ecosystem.config.js
module.exports = {
    apps: [
        {
            name: 'my-api',
            script: 'src/index.js',

            // Cluster mode — all CPU cores
            instances: 'max',
            exec_mode: 'cluster',

            // Environment variables
            env: {
                NODE_ENV: 'development',
                PORT: 3000
            },
            env_production: {
                NODE_ENV: 'production',
                PORT: 3000
            },

            // Auto-restart on crash
            autorestart: true,
            watch: false,           // production-এ false (dev-এ true)

            // Memory limit — leak prevent
            max_memory_restart: '500M',

            // Restart delay
            restart_delay: 4000,
            max_restarts: 10,

            // Logs
            error_file: 'logs/pm2-error.log',
            out_file: 'logs/pm2-out.log',
            log_date_format: 'YYYY-MM-DD HH:mm:ss Z',

            // Graceful shutdown
            kill_timeout: 10000,    // 10s graceful shutdown window
            wait_ready: true,
            listen_timeout: 10000
        }
    ]
};
```

```bash
# Start
pm2 start ecosystem.config.js --env production

# Status
pm2 status
pm2 list

# Logs
pm2 logs my-api
pm2 logs my-api --lines 100

# Restart (zero-downtime)
pm2 reload my-api

# Stop
pm2 stop my-api

# Delete
pm2 delete my-api

# Monitoring dashboard
pm2 monit

# Auto-start on server reboot
pm2 startup
pm2 save
```

```javascript
// Graceful shutdown — app.js
process.on('SIGINT', gracefulShutdown);
process.on('SIGTERM', gracefulShutdown);

async function gracefulShutdown() {
    logger.info('Shutting down gracefully...');
    server.close(async () => {
        await mongoose.connection.close();
        await redis.quit();
        logger.info('Shutdown complete');
        process.exit(0);
    });
    // PM2-কে ready signal
    if (process.send) process.send('ready');
}
```

---

<a id="p10-docker"></a>
**Topic 3: Docker — Dockerfile ও docker-compose**

```dockerfile
# Dockerfile
# ────────────────────────────────────────────
# Stage 1: Dependencies
# ────────────────────────────────────────────
FROM node:20-alpine AS deps
WORKDIR /app

COPY package*.json ./
RUN npm ci --only=production && npm cache clean --force

# ────────────────────────────────────────────
# Stage 2: Production image
# ────────────────────────────────────────────
FROM node:20-alpine AS production

# Security: non-root user
RUN addgroup -g 1001 -S nodejs && adduser -S nodeuser -u 1001

WORKDIR /app

# Dependencies copy করুন
COPY --from=deps --chown=nodeuser:nodejs /app/node_modules ./node_modules
COPY --chown=nodeuser:nodejs . .

# Non-root user use করুন
USER nodeuser

EXPOSE 3000

# Health check
HEALTHCHECK --interval=30s --timeout=10s --start-period=30s --retries=3 \
  CMD node -e "require('http').get('http://localhost:3000/health', r => process.exit(r.statusCode === 200 ? 0 : 1))"

CMD ["node", "src/index.js"]
```

```yaml
# docker-compose.yml
version: '3.8'

services:
  api:
    build:
      context: .
      dockerfile: Dockerfile
      target: production
    ports:
      - "3000:3000"
    environment:
      - NODE_ENV=production
    env_file:
      - .env
    depends_on:
      mongo:
        condition: service_healthy
      redis:
        condition: service_healthy
    restart: unless-stopped
    networks:
      - app-network

  mongo:
    image: mongo:7
    volumes:
      - mongo_data:/data/db
    environment:
      MONGO_INITDB_ROOT_USERNAME: admin
      MONGO_INITDB_ROOT_PASSWORD: ${MONGO_PASSWORD}
    healthcheck:
      test: ["CMD", "mongosh", "--eval", "db.adminCommand('ping')"]
      interval: 10s
      timeout: 5s
      retries: 5
    restart: unless-stopped
    networks:
      - app-network

  redis:
    image: redis:7-alpine
    command: redis-server --requirepass ${REDIS_PASSWORD}
    volumes:
      - redis_data:/data
    healthcheck:
      test: ["CMD", "redis-cli", "ping"]
      interval: 10s
      timeout: 3s
      retries: 5
    restart: unless-stopped
    networks:
      - app-network

  nginx:
    image: nginx:alpine
    ports:
      - "80:80"
      - "443:443"
    volumes:
      - ./nginx/nginx.conf:/etc/nginx/nginx.conf
      - ./nginx/ssl:/etc/nginx/ssl
    depends_on:
      - api
    restart: unless-stopped
    networks:
      - app-network

networks:
  app-network:
    driver: bridge

volumes:
  mongo_data:
  redis_data:
```

```bash
# Start all services
docker-compose up -d

# Logs
docker-compose logs -f api

# Rebuild
docker-compose up -d --build api

# Stop
docker-compose down

# Stop + volumes remove
docker-compose down -v
```

---

<a id="p10-nginx"></a>
**Topic 4: Nginx Reverse Proxy**

```nginx
# nginx/nginx.conf

upstream api {
    server api:3000;
    # Multiple instances:
    # server api_1:3000;
    # server api_2:3000;
    keepalive 32;
}

server {
    listen 80;
    server_name api.myapp.com;

    # HTTP → HTTPS redirect
    return 301 https://$server_name$request_uri;
}

server {
    listen 443 ssl http2;
    server_name api.myapp.com;

    # SSL certificates (Let's Encrypt)
    ssl_certificate     /etc/nginx/ssl/fullchain.pem;
    ssl_certificate_key /etc/nginx/ssl/privkey.pem;
    ssl_protocols       TLSv1.2 TLSv1.3;
    ssl_ciphers         HIGH:!aNULL:!MD5;

    # Security headers
    add_header Strict-Transport-Security "max-age=31536000; includeSubDomains" always;
    add_header X-Frame-Options "DENY" always;
    add_header X-Content-Type-Options "nosniff" always;

    # Proxy settings
    location /api/ {
        proxy_pass http://api;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_cache_bypass $http_upgrade;
        proxy_read_timeout 60s;
        client_max_body_size 10M;
    }

    # Static files
    location /uploads/ {
        alias /var/www/uploads/;
        expires 1d;
        add_header Cache-Control "public, immutable";
    }

    # Rate limiting (Nginx level)
    limit_req_zone $binary_remote_addr zone=api:10m rate=10r/s;
    location / {
        limit_req zone=api burst=20 nodelay;
        proxy_pass http://api;
    }
}
```

---

<a id="p10-cicd"></a>
**Topic 5: GitHub Actions CI/CD**

```yaml
# .github/workflows/ci.yml
name: CI/CD Pipeline

on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

jobs:
  # ────────────────────────────────────────────
  # Test job
  # ────────────────────────────────────────────
  test:
    runs-on: ubuntu-latest

    services:
      mongodb:
        image: mongo:7
        ports:
          - 27017:27017

      redis:
        image: redis:7-alpine
        ports:
          - 6379:6379

    steps:
      - uses: actions/checkout@v4

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '20'
          cache: 'npm'

      - name: Install dependencies
        run: npm ci

      - name: Lint
        run: npm run lint

      - name: Run tests
        run: npm run test:ci
        env:
          NODE_ENV: test
          MONGO_URI: mongodb://localhost:27017/testdb
          REDIS_HOST: localhost
          JWT_SECRET: test-secret-at-least-32-characters-long
          JWT_REFRESH_SECRET: test-refresh-secret-32-characters-long

      - name: Upload coverage
        uses: codecov/codecov-action@v4
        with:
          token: ${{ secrets.CODECOV_TOKEN }}

  # ────────────────────────────────────────────
  # Build ও Deploy job (main branch only)
  # ────────────────────────────────────────────
  deploy:
    needs: test
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'

    steps:
      - uses: actions/checkout@v4

      - name: Login to Docker Hub
        uses: docker/login-action@v3
        with:
          username: ${{ secrets.DOCKER_USERNAME }}
          password: ${{ secrets.DOCKER_TOKEN }}

      - name: Build ও Push Docker image
        uses: docker/build-push-action@v5
        with:
          context: .
          push: true
          tags: |
            myusername/my-api:latest
            myusername/my-api:${{ github.sha }}

      - name: Deploy to server
        uses: appleboy/ssh-action@v1
        with:
          host: ${{ secrets.SERVER_HOST }}
          username: ${{ secrets.SERVER_USER }}
          key: ${{ secrets.SSH_PRIVATE_KEY }}
          script: |
            cd /app
            docker-compose pull api
            docker-compose up -d api
            docker system prune -f
```

---

<a id="p10-health"></a>
**Topic 6: Health Check Endpoint**

```javascript
// src/routes/health.js
const router = require('express').Router();
const mongoose = require('mongoose');
const redis = require('../utils/redis');
const config = require('../config/env');

router.get('/health', async (req, res) => {
    const health = {
        status: 'ok',
        timestamp: new Date().toISOString(),
        uptime: Math.floor(process.uptime()),
        version: process.env.npm_package_version || '1.0.0',
        environment: config.NODE_ENV,
        checks: {}
    };

    // MongoDB check
    try {
        if (mongoose.connection.readyState === 1) {
            await mongoose.connection.db.admin().ping();
            health.checks.mongodb = { status: 'ok' };
        } else {
            health.checks.mongodb = { status: 'disconnected' };
            health.status = 'degraded';
        }
    } catch {
        health.checks.mongodb = { status: 'error' };
        health.status = 'degraded';
    }

    // Redis check
    try {
        await redis.ping();
        health.checks.redis = { status: 'ok' };
    } catch {
        health.checks.redis = { status: 'error' };
        health.status = 'degraded';
    }

    // Memory check
    const { heapUsed, heapTotal } = process.memoryUsage();
    const memUsagePct = (heapUsed / heapTotal) * 100;
    health.checks.memory = {
        status: memUsagePct < 90 ? 'ok' : 'warning',
        used: `${Math.round(heapUsed / 1024 / 1024)}MB`,
        total: `${Math.round(heapTotal / 1024 / 1024)}MB`,
        percent: `${Math.round(memUsagePct)}%`
    };

    const statusCode = health.status === 'ok' ? 200 : 503;
    res.status(statusCode).json(health);
});

// Liveness probe (Kubernetes — process alive?)
router.get('/health/live', (req, res) => {
    res.json({ status: 'ok' });
});

// Readiness probe (Kubernetes — ready to serve traffic?)
router.get('/health/ready', async (req, res) => {
    const isReady = mongoose.connection.readyState === 1;
    res.status(isReady ? 200 : 503).json({
        status: isReady ? 'ready' : 'not ready'
    });
});

module.exports = router;
```

---

<a id="p10-structure"></a>
**Topic 7: Complete Project Structure**

```
my-node-api/
├── src/
│   ├── index.js              ← Entry point (listen + process events)
│   ├── app.js                ← Express app (middleware + routes)
│   ├── config/
│   │   └── env.js            ← Validated environment config
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── userController.js
│   │   └── postController.js
│   ├── services/
│   │   ├── authService.js    ← Business logic
│   │   └── userService.js
│   ├── models/
│   │   ├── User.js
│   │   └── Post.js
│   ├── routes/
│   │   ├── index.js          ← Route aggregator
│   │   ├── auth.js
│   │   ├── users.js
│   │   └── health.js
│   ├── middleware/
│   │   ├── auth.js           ← requireAuth, requireRole
│   │   ├── errorHandler.js   ← Global error handler
│   │   ├── validate.js       ← express-validator result check
│   │   ├── upload.js         ← Multer config
│   │   └── cache.js          ← Redis cache middleware
│   ├── utils/
│   │   ├── AppError.js       ← Custom error class
│   │   ├── catchAsync.js     ← Async wrapper
│   │   ├── logger.js         ← Winston
│   │   ├── redis.js          ← Redis client
│   │   ├── jwt.js            ← Token utils
│   │   ├── email.js          ← Email service
│   │   └── response.js       ← sendSuccess, sendError
│   └── tests/
│       ├── setup.js          ← Jest global setup
│       ├── integration/
│       │   ├── auth.test.js
│       │   └── users.test.js
│       └── utils/
│           └── factories.js  ← Test data factories
├── logs/                     ← Winston log files
├── uploads/                  ← File uploads
├── nginx/
│   └── nginx.conf
├── .github/
│   └── workflows/
│       └── ci.yml
├── .env                      ← Never commit
├── .env.example              ← Template — commit করুন
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── ecosystem.config.js       ← PM2 config
├── package.json
└── README.md
```

---

<a id="p10-checklist"></a>
**Topic 8: Production Checklist**

```
Pre-deployment Checklist:

Code Quality
✅ All tests pass (npm test)
✅ No console.log in production code (logger use)
✅ No hardcoded secrets
✅ npm audit — no critical vulnerabilities
✅ Code reviewed (PR)

Security
✅ helmet() middleware
✅ Rate limiting (global + auth routes)
✅ Input validation (all POST/PUT/PATCH)
✅ mongoSanitize() + xssClean()
✅ HTTPS only
✅ Secure cookies
✅ CORS: specific origins

Performance
✅ compression() middleware
✅ MongoDB indexes
✅ .lean() for read queries
✅ Redis cache (hot data)
✅ PM2 cluster mode (max instances)

Operations
✅ Health check endpoint (/health)
✅ Structured logging (Winston)
✅ Error tracking (Sentry optional)
✅ Graceful shutdown (SIGTERM handler)
✅ PM2 startup (auto-restart on reboot)
✅ Log rotation (DailyRotateFile)

Environment
✅ NODE_ENV=production
✅ All required env vars set
✅ .env not committed
✅ Different secrets per environment
✅ Backup strategy for DB
```

---

<a id="p10-revision"></a>
**Topic 9: Interview Quick Revision**

```
Node.js Handbook — সম্পূর্ণ Summary

PART 1 — Fundamentals
V8 engine, libuv, Event Loop (6 phases), single-threaded,
CommonJS vs ESM, npm, first HTTP server

PART 2 — Core Modules & Async
fs, path, os, EventEmitter, Streams, Callbacks → Promises → async/await,
Error-first callback, Promise.all/race/allSettled

PART 3 — Express.js
app.use, Router, middleware chain, req/res/next,
helmet/cors/morgan, global error handler, project structure

PART 4 — Database Integration
Mongoose (Schema/Model/CRUD), MongoDB aggregation,
pg raw queries, Knex query builder, transactions, connection pool

PART 5 — Authentication & Authorization
bcrypt hash/compare, JWT sign/verify, access+refresh tokens,
HttpOnly cookie, OAuth2, RBAC, timing attack prevention

PART 6 — REST API Design
RESTful URLs, HTTP status codes, response format,
express-validator, pagination+filtering, Multer upload,
versioning, Swagger, CORS

PART 7 — Error Handling & Logging
AppError class, catchAsync wrapper, centralized error middleware,
Mongoose/JWT error handling, unhandledRejection, SIGTERM,
Winston + DailyRotateFile, Morgan, structured logging

PART 8 — Testing
Jest setup, unit tests, mocking (jest.fn/mock/spyOn),
Supertest integration tests, MongoMemoryServer, factories, coverage

PART 9 — Performance & Security
helmet, rate limiting, mongoSanitize, xssClean, Redis caching,
compression, clustering, Worker Threads, N+1 problem, indexes

PART 10 — Deployment & DevOps
dotenv + envalid config, PM2 cluster, Docker multi-stage build,
docker-compose, Nginx reverse proxy, GitHub Actions CI/CD,
health checks, graceful shutdown, production checklist
```

---

<a id="p10-qa"></a>
**Topic 10: PART 10 Interview Q&A**

```
প্রশ্ন: Docker multi-stage build কেন ব্যবহার করি?
উত্তর: Image size কমানো।
Stage 1 (deps): devDependencies সহ — শুধু production deps install।
Stage 2 (production): শুধু node_modules + source copy।
devDependencies, build tools image-এ নেই।
Result: 100MB+ → 50MB image।
Security: কম dependencies = কম attack surface।

প্রশ্ন: PM2 cluster mode vs Node.js cluster module?
উত্তর: দুটোই same concept — multiple worker processes।
Node.js cluster: manual code লিখতে হয়।
PM2 cluster: ecosystem.config.js-এ instances: 'max' — zero code।
PM2 extra: log management, monitoring, auto-restart, startup scripts।
Production-এ PM2 preferred।

প্রশ্ন: Nginx reverse proxy কেন?
উত্তর:
SSL termination — HTTPS Nginx handle করে, Node HTTP চলে।
Load balancing — multiple Node instances।
Static files — Nginx fast, Node-এর load কমে।
Rate limiting — Nginx level (before app)।
Gzip compression।
Security — Node-এর port direct expose হয় না।

প্রশ্ন: .env file কি Docker image-এ রাখবেন?
উত্তর: না। Security risk।
Docker: env_file: .env (docker-compose) বা --env-file।
Production: Secret management service — AWS Secrets Manager,
HashiCorp Vault, Kubernetes Secrets।
GitHub Actions: Repository secrets → environment variables।

প্রশ্ন: Graceful shutdown কী? কেন দরকার?
উত্তর: Sudden exit → in-flight requests incomplete।
Graceful: SIGTERM receive → নতুন connections বন্ধ → চলমান requests finish →
DB disconnect → exit।
Docker/K8s deployment: pod stop → SIGTERM → 30s grace period → SIGKILL।
PM2 reload: zero-downtime restart — graceful shutdown + new workers।

প্রশ্ন: CI/CD pipeline-এ কী steps থাকে?
উত্তর:
1. Code push (git push)
2. Lint (code quality)
3. Tests (unit + integration)
4. Coverage check (threshold)
5. Docker image build
6. Image push to registry
7. Deploy to server (SSH / kubectl)
8. Health check verify
Fail হলে deploy বন্ধ — code safe।
```

---

**PART 10 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| dotenv | .env file load |
| envalid | Env vars validate — startup-এ crash |
| PM2 | Process manager — cluster, restart, logs |
| `instances: 'max'` | All CPU cores |
| `pm2 reload` | Zero-downtime restart |
| Dockerfile | Multi-stage — small, secure image |
| `FROM node:20-alpine` | Minimal base image |
| Non-root user | Security — never run as root |
| docker-compose | Multi-service orchestration |
| `depends_on` | Service startup order |
| Nginx | SSL, load balancing, static files |
| `proxy_pass` | Requests forward to Node |
| GitHub Actions | CI/CD workflow |
| `needs: test` | Sequential jobs |
| `/health` | DB + Redis + memory check |
| Liveness probe | Process alive? |
| Readiness probe | Ready to serve traffic? |
| SIGTERM | Graceful shutdown signal |
| `server.close()` | Stop accepting new connections |

---

**Node.js Junior Engineer Handbook — সম্পূর্ণ!**

| PART | বিষয় | Topics |
|------|-------|--------|
| 1 | Fundamentals | V8, Event Loop, CommonJS/ESM, npm |
| 2 | Core Modules & Async | fs, streams, Promises, async/await |
| 3 | Express.js | Middleware, routing, error handling |
| 4 | Database Integration | Mongoose, PostgreSQL, Knex, Prisma |
| 5 | Authentication | JWT, bcrypt, refresh tokens, OAuth2, RBAC |
| 6 | REST API Design | Validation, pagination, upload, Swagger |
| 7 | Error Handling & Logging | AppError, catchAsync, Winston, Morgan |
| 8 | Testing | Jest, Supertest, mocking, coverage |
| 9 | Performance & Security | helmet, rate limiting, Redis, clustering |
| 10 | Deployment & DevOps | PM2, Docker, Nginx, CI/CD, checklist |

---

[⬆ শীর্ষে ফিরুন](#top)
