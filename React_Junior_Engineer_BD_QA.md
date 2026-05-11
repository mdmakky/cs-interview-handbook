<a id="top"></a>

# 🚀 React Interview Preparation Handbook — Junior Frontend Developer (Bangladesh)

> **Target:** Junior Software Engineer, Frontend Developer, React Developer — Bangladeshi IT Company interviews
>
> **Language:** বাংলা (English technical terms সহ)
>
> **Author:** CS Interview Handbook Series
>
> **Companies:** Brain Station 23, BJIT, Pathao, Shajgoj, Chaldal, Shohoz, 10 Minute School, Augmedix, SSL Wireless

---

## 📋 সম্পূর্ণ সূচিপত্র

| PART | বিষয় | Status |
|---|---|---|
| PART 1 | React Fundamentals | ✅ |
| PART 2 | React Hooks | ✅ |
| PART 3 | Component Architecture | 🔄 |
| PART 4 | Routing & Navigation | 🔄 |
| PART 5 | State Management | 🔄 |
| PART 6 | API Integration & Async | 🔄 |
| PART 7 | Performance Optimization | 🔄 |
| PART 8 | Advanced React | 🔄 |
| PART 9 | Backend & Authentication | 🔄 |
| PART 10 | React Projects | 🔄 |
| PART 11 | Interview Questions Bank | 🔄 |
| PART 12 | Next.js Basics | 🔄 |
| PART 13 | Testing & Best Practices | 🔄 |
| PART 14 | BD Interview Preparation | 🔄 |

---

<a id="part1"></a>

## 📋 PART 1 সূচিপত্র — React Fundamentals

| # | Topic | Key Concept |
|---|---|---|
| 1 | [What is React](#p1-what-is-react) | Library, UI, component-based |
| 2 | [Why React is Popular](#p1-why-react) | Ecosystem, performance, community |
| 3 | [SPA — Single Page Application](#p1-spa) | No page reload, dynamic UI |
| 4 | [Virtual DOM](#p1-vdom) | In-memory DOM, diffing |
| 5 | [Real DOM vs Virtual DOM](#p1-dom-compare) | Comparison table |
| 6 | [React Architecture](#p1-architecture) | Component tree, unidirectional flow |
| 7 | [JSX](#p1-jsx) | JavaScript + XML syntax |
| 8 | [Components](#p1-components) | Building blocks of React |
| 9 | [Functional Components](#p1-functional) | Modern, hooks-based |
| 10 | [Class Components](#p1-class) | Legacy, lifecycle methods |
| 11 | [Props](#p1-props) | Parent → Child data flow |
| 12 | [State](#p1-state) | Dynamic, internal data |
| 13 | [Event Handling](#p1-events) | onClick, onChange, synthetic events |
| 14 | [Conditional Rendering](#p1-conditional) | if, ternary, && operator |
| 15 | [List Rendering](#p1-list) | map(), rendering arrays |
| 16 | [Keys in React](#p1-keys) | Reconciliation identity |
| 17 | [Component Lifecycle Overview](#p1-lifecycle) | Mount → Update → Unmount |

---

<a id="p1-what-is-react"></a>

## 1. What is React?

**Definition:**
React হলো Facebook (Meta) কর্তৃক তৈরি একটি open-source **JavaScript Library** যা User Interface (UI) তৈরি করার জন্য ব্যবহার হয়। এটি component-based architecture follow করে — মানে UI-কে ছোট ছোট reusable pieces-এ ভাগ করে তৈরি করা হয়।

> **Note:** React একটি library, framework নয়। এটি শুধু UI layer handle করে। Routing, state management ইত্যাদির জন্য আলাদা library দরকার।

**Real-life Analogy:**
React হলো **LEGO block** সিস্টেমের মতো। প্রতিটি LEGO piece (component) আলাদাভাবে তৈরি করা যায়, পরীক্ষা করা যায়, এবং একসাথে জোড়া লাগিয়ে বড় কিছু বানানো যায়। একটি piece পরিবর্তন করলে অন্যগুলো affect হয় না।

**Practical Use Case:**
- Facebook, Instagram, WhatsApp Web — React দিয়ে তৈরি
- Pathao, Shohoz, 10 Minute School-এর frontend
- E-commerce dashboard, admin panel, single page apps

**Interview-style Explanation:**
> "React একটি JavaScript UI library যা Meta তৈরি করেছে। এটি component-based — মানে আমরা UI-কে ছোট ছোট reusable component-এ ভাঙি। React-এর সবচেয়ে বড় সুবিধা হলো Virtual DOM — এটি actual DOM-এ শুধু পরিবর্তিত অংশটুকু update করে, ফলে performance অনেক ভালো হয়।"

**Common Mistakes:**
- React-কে framework বলা — এটি library
- Angular বা Vue-এর সাথে confuse করা
- "React is a programming language" বলা — JavaScript library

**Follow-up Interview Questions:**
1. React framework না library — পার্থক্য কী?
2. React কে তৈরি করেছে? কোন সালে?
3. React-এর latest stable version কত?
4. Angular vs React vs Vue — কোনটি কখন?

**Quick Facts:**
```
Release: 2013 (by Jordan Walke, Facebook)
Current: React 18+
License: MIT
Package: npm install react react-dom
```

---

<a id="p1-why-react"></a>

## 2. Why React is Popular?

**Definition:**
React-এর popularity-র পেছনে বেশ কিছু কারণ আছে যা developer experience, performance, এবং ecosystem-কে exceptional করে তোলে।

**কারণসমূহ:**

| কারণ | বিবরণ |
|---|---|
| Component-based | Reusable, maintainable code |
| Virtual DOM | Fast UI updates |
| Unidirectional Data Flow | Predictable, debuggable |
| JSX | HTML + JS একসাথে |
| Large Ecosystem | Thousands of libraries |
| Strong Community | Huge support, documentation |
| Meta Backing | Long-term support guaranteed |
| React Native | Mobile app same codebase |
| Developer Tools | React DevTools, excellent debugging |
| Flexible | Library — choose your own stack |

**Real-life Analogy:**
React-এর popularity হলো **smartphone OS**-এর মতো। Android যেমন সব manufacturer use করে কারণ ecosystem, support, আর flexibility আছে — React-ও তেমনি frontend world-এ dominant।

**Interview-style Explanation:**
> "React popular কারণ: প্রথমত, component reusability — একবার বানালে সব জায়গায় use করা যায়। দ্বিতীয়ত, Virtual DOM performance optimization। তৃতীয়ত, React Native দিয়ে mobile app বানানো যায় same JavaScript codebase দিয়ে। চতুর্থত, Meta-র মতো বড় company maintain করে — community আর ecosystem বিশাল।"

**Angular vs React vs Vue Comparison:**

| Feature | React | Angular | Vue |
|---|---|---|---|
| Type | Library | Full Framework | Progressive Framework |
| Language | JSX | TypeScript | Template/JSX |
| Learning Curve | Medium | Steep | Easy |
| Data Flow | Unidirectional | Two-way (NgModel) | Two-way |
| Performance | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Company | Meta | Google | Community |
| Mobile | React Native | Ionic/NativeScript | Weex/NativeScript |
| BD Market Demand | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ |

**Follow-up Interview Questions:**
1. React-এর সবচেয়ে বড় advantage কী বলে মনে করেন?
2. কোন project-এ React use করবেন না?
3. React vs Next.js — পার্থক্য?

---

<a id="p1-spa"></a>

## 3. SPA — Single Page Application

**Definition:**
Single Page Application (SPA) হলো একটি web application যেখানে **একটিমাত্র HTML page** load হয় এবং user navigate করলে পুরো page reload না হয়ে শুধু প্রয়োজনীয় content dynamically update হয়।

**Real-life Analogy:**
SPA হলো **mobile app**-এর মতো। Gmail-এ email click করলে পুরো app restart হয় না — শুধু email content show হয়। Traditional website হলো বইয়ের পাতা উল্টানোর মতো (full reload), SPA হলো ebook app-এর মতো (smooth transition)।

**Traditional MPA vs SPA:**

| Feature | Traditional MPA | SPA (React) |
|---|---|---|
| Page Load | প্রতিটি navigate-এ full reload | একবার load, তারপর dynamic update |
| Server Requests | প্রতিটি page-এ HTML request | Initial load, তারপর API (JSON) |
| User Experience | Slow, flicker visible | Fast, smooth |
| SEO | ভালো (সহজ) | Extra work দরকার (SSR/SSG) |
| Initial Load | Fast | Slow (bundle download) |
| Examples | Traditional PHP site | Gmail, Facebook, Pathao web |

**কীভাবে কাজ করে:**
```
1. Browser → server: index.html চাই
2. Server → browser: একটাই index.html + JS bundle পাঠায়
3. React JavaScript load হয়, পুরো app render করে
4. User navigate করলে → React Router URL change করে
5. Server-এ নতুন page request যায় না
6. Component swap হয়, API call হয় (শুধু data)
```

**Interview-style Explanation:**
> "SPA-তে initial page load-এ পুরো React app download হয়। এরপর navigation-এ server-এ HTML request যায় না — React Router client-side route handle করে, শুধু API থেকে data fetch হয়। এতে user experience smooth হয় কিন্তু initial load time বেশি হতে পারে এবং SEO challenge থাকে — যেটা Next.js SSR দিয়ে solve করা যায়।"

**Code Example:**
```jsx
// React SPA — index.html শুধু একটি <div id="root">
// React এই root-এ পুরো app inject করে

// index.html
// <div id="root"></div>

// main.jsx
import React from 'react';
import { createRoot } from 'react-dom/client';
import App from './App';

const root = createRoot(document.getElementById('root'));
root.render(<App />);
// পুরো app এখান থেকে শুরু — কোনো page reload নেই!
```

**Common Mistakes:**
- SEO-র কথা না ভেবে SPA বানানো — public-facing site-এ SSR দরকার
- Large bundle size — code splitting করতে হবে
- Back button handle না করা — React Router ব্যবহার করতে হবে

**Follow-up Interview Questions:**
1. SPA-এর SEO problem কীভাবে solve করবেন?
2. SPA-এ Back button কীভাবে কাজ করে?
3. SPA কোথায় use করবেন না?

---

<a id="p1-vdom"></a>

## 4. Virtual DOM

**Definition:**
Virtual DOM (VDOM) হলো actual (Real) DOM-এর একটি **lightweight JavaScript object copy** যা React memory-তে রাখে। React কোনো change হলে প্রথমে VDOM-এ update করে, তারপর পুরানো VDOM আর নতুন VDOM compare (diff) করে, এবং শুধু পরিবর্তিত অংশটুকু Real DOM-এ update করে।

**Real-life Analogy:**
ধরুন আপনি একটি বড় document edit করছেন। পুরো document reprint না করে আপনি একটি draft copy-তে change করেন, তারপর original-এর সাথে compare করে শুধু different parts print করেন। Virtual DOM হলো সেই **draft copy**।

**Virtual DOM Process — Step by Step:**
```
Step 1: State/Props change হলো
         ↓
Step 2: React নতুন Virtual DOM tree বানায়
         ↓
Step 3: নতুন VDOM vs পুরানো VDOM compare (Diffing algorithm)
         ↓
Step 4: পার্থক্য (diff) বের করে
         ↓
Step 5: শুধু সেই অংশটুকু Real DOM-এ update (Reconciliation)
         ↓
Step 6: Browser screen update করে
```

**Visual Representation:**
```
State change হলো: count: 0 → count: 1

Old VDOM:              New VDOM:
<div>                  <div>
  <h1>Hello</h1>         <h1>Hello</h1>   ← same, skip
  <p>Count: 0</p>        <p>Count: 1</p>  ← DIFFERENT!
  <button>+</button>     <button>+</button> ← same, skip
</div>                 </div>

React শুধু <p> element-এর text update করবে Real DOM-এ।
```

**Interview-style Explanation:**
> "Virtual DOM হলো React-এর performance secret। Real DOM manipulation slow কারণ প্রতিটি change browser-এর reflow আর repaint trigger করে। React VDOM-এ change করে, diff করে, এবং batch করে minimal Real DOM operations চালায়। এতে performance dramatically improve হয়।"

**Follow-up Interview Questions:**
1. Virtual DOM কি সবসময় Real DOM-এর চেয়ে fast?
2. React Fiber কী? Virtual DOM-এর সাথে সম্পর্ক?
3. Vue-তেও Virtual DOM আছে — React-এর সাথে পার্থক্য?

---

<a id="p1-dom-compare"></a>

## 5. Real DOM vs Virtual DOM

**Detailed Comparison:**

| Feature | Real DOM | Virtual DOM |
|---|---|---|
| কী | Browser-এর actual HTML tree | JS object representation |
| কোথায় থাকে | Browser memory | JavaScript memory |
| Update speed | Slow (reflow/repaint trigger) | Fast (in-memory operation) |
| Direct manipulation | `document.getElementById()` | React handle করে |
| Re-render | পুরো subtree re-render | শুধু changed part |
| Memory | Less (actual browser objects) | More (JS objects + Real DOM) |
| Developer control | Manual | React automate করে |
| Batch updates | না | হ্যাঁ (multiple changes batched) |

**কেন Real DOM Slow?**
```
document.getElementById('count').textContent = '1';

Browser-এ কী হয়:
1. DOM tree parse
2. CSSOM recalculate (styles)
3. Render tree rebuild
4. Layout (reflow) — element positions recalculate
5. Paint (repaint) — pixels draw
6. Composite — layers merge

→ এই পুরো process expensive!
```

**React কীভাবে এটা Optimize করে:**
```jsx
// React এই updates batch করে
setState({ count: 1 });
setState({ name: 'Rahim' });
setState({ active: true });

// React 18: তিনটি change একসাথে process করে
// শুধু একটি Real DOM update → একটি reflow/repaint
```

**Interview-style Explanation:**
> "Real DOM manipulation browser-এ reflow আর repaint trigger করে যা expensive। Virtual DOM হলো JavaScript object — in-memory operation much faster। React multiple state changes batch করে একটি Real DOM update করে। তবে Virtual DOM itself extra memory নেয় — trade-off আছে।"

---

<a id="p1-architecture"></a>

## 6. React Architecture

**Definition:**
React unidirectional (one-way) data flow follow করে — data সবসময় parent থেকে child-এ নামে। এটি component tree হিসেবে structure করা হয়।

**React Application Architecture:**
```
App (Root)
├── Header
│   ├── Logo
│   ├── NavBar
│   └── UserMenu
├── Main
│   ├── Sidebar
│   └── ContentArea
│       ├── ProductList
│       │   ├── ProductCard
│       │   └── ProductCard
│       └── Pagination
└── Footer
```

**Unidirectional Data Flow:**
```
Parent Component
    │
    │ Props (data নামে)
    ↓
Child Component
    │
    │ Callback (event উঠে)
    ↑
Parent Component (state update)
```

**React App-এর তিনটি Layer:**

| Layer | কী | Example |
|---|---|---|
| UI Layer | Components, JSX | `<Button>`, `<Card>` |
| State Layer | useState, Redux, Context | User data, cart items |
| Data Layer | API calls, services | `fetchProducts()`, axios |

**Interview-style Explanation:**
> "React-এর architecture component tree-based। সবকিছু component — ছোট থেকে বড়। Data flow unidirectional — parent থেকে child props দিয়ে, child থেকে parent callback দিয়ে। এই predictable flow debugging সহজ করে।"

**Follow-up Interview Questions:**
1. Unidirectional data flow কেন bidirectional-এর চেয়ে better?
2. Large app-এ component tree কীভাবে organize করবেন?

---

<a id="p1-jsx"></a>

## 7. JSX — JavaScript XML

**Definition:**
JSX (JavaScript XML) হলো JavaScript-এর একটি syntax extension যা HTML-এর মতো দেখতে। Browser directly JSX বোঝে না — Babel এটাকে `React.createElement()` call-এ compile করে।

**Real-life Analogy:**
JSX হলো **shorthand notation**-এর মতো। Mathematical shorthand `x²` লেখা সহজ কিন্তু computer `x*x` বোঝে। JSX হলো developer-friendly shorthand, Babel করে machine-readable JavaScript।

**JSX কীভাবে Compile হয়:**
```jsx
// আপনি লেখেন (JSX):
const element = <h1 className="title">Hello, {name}!</h1>;

// Babel compile করে (JavaScript):
const element = React.createElement(
  'h1',
  { className: 'title' },
  `Hello, ${name}!`
);
```

**JSX Rules — মনে রাখুন:**

| Rule | উদাহরণ |
|---|---|
| Single root element | `<>...</>` বা `<div>...</div>` |
| className (not class) | `className="container"` |
| camelCase attributes | `onClick`, `onChange`, `onSubmit` |
| Self-closing tags | `<img />`, `<input />`, `<br />` |
| JS expression in `{}` | `{name}`, `{2 + 2}`, `{isLoggedIn ? 'Hi' : 'Login'}` |
| Style as object | `style={{ color: 'red', fontSize: '16px' }}` |
| Comments | `{/* This is a comment */}` |

**Code Example:**
```jsx
// JSX practical example
function UserCard({ name, age, isOnline }) {
  return (
    <div className="card" style={{ border: '1px solid #ccc' }}>
      {/* User info */}
      <h2>{name}</h2>
      <p>Age: {age}</p>
      <span className={isOnline ? 'online' : 'offline'}>
        {isOnline ? '🟢 Online' : '🔴 Offline'}
      </span>
      <img src={`/avatars/${name}.jpg`} alt={`${name}'s avatar`} />
    </div>
  );
}
```

**Common Mistakes:**
- `class` লেখা `className`-এর বদলে
- Multiple root elements return করা — Fragment use করুন `<></>`
- `for` attribute — React-এ `htmlFor` ব্যবহার করতে হয়
- Inline style string — `style="color: red"` JSX-এ কাজ করে না, object দিতে হবে

**Follow-up Interview Questions:**
1. JSX কি mandatory React-এ?
2. `React.createElement()` সরাসরি ব্যবহার করলে কী হয়?
3. JSX-এ `if` statement কেন directly লেখা যায় না?

```jsx
// ❌ Bad — if statement directly in JSX
return (
  <div>
    if (isLoggedIn) { <p>Welcome!</p> }  // syntax error
  </div>
);

// ✅ Good — ternary operator
return (
  <div>
    {isLoggedIn ? <p>Welcome!</p> : <p>Please login</p>}
  </div>
);

// ✅ Good — outside JSX
function render() {
  let content;
  if (isLoggedIn) {
    content = <p>Welcome!</p>;
  } else {
    content = <p>Please login</p>;
  }
  return <div>{content}</div>;
}
```

---

<a id="p1-components"></a>

## 8. Components

**Definition:**
Component হলো React-এর সবচেয়ে মৌলিক building block। এটি একটি reusable UI piece যা নিজস্ব logic আর markup contain করে। Component একটি JavaScript function বা class যা JSX return করে।

**Real-life Analogy:**
Component হলো **stamp** বা **mold** (ছাঁচ)-এর মতো। একটি button mold বানিয়ে রাখুন, তারপর ১০০ বার ব্যবহার করুন — রং আর text আলাদা হলেও মূল shape একই।

**Component-এর বৈশিষ্ট্য:**

| বৈশিষ্ট্য | বিবরণ |
|---|---|
| Reusable | একবার বানাও, বারবার use করো |
| Independent | নিজস্ব state আর logic |
| Composable | ছোট component দিয়ে বড় component |
| Testable | Isolated testing সহজ |
| Maintainable | একজায়গায় change = সব জায়গায় update |

**Types of Components:**
```
React Components
├── Functional Component (Modern — recommended)
│   ├── Stateless (only UI)
│   └── Stateful (with Hooks)
└── Class Component (Legacy — older codebases)
```

**Component Naming Rules:**
```jsx
// ✅ PascalCase — React component
function UserProfile() { ... }
function NavBar() { ... }
const ProductCard = () => { ... };

// ❌ lowercase — React treats as HTML tag!
function userprofile() { ... }  // JSX-এ <userprofile /> HTML tag মনে করবে
```

**Code Example:**
```jsx
// Simple component composition
function Avatar({ src, alt }) {
  return <img className="avatar" src={src} alt={alt} />;
}

function UserInfo({ name, role }) {
  return (
    <div>
      <h3>{name}</h3>
      <p>{role}</p>
    </div>
  );
}

function UserCard({ user }) {
  return (
    <div className="user-card">
      <Avatar src={user.avatar} alt={user.name} />
      <UserInfo name={user.name} role={user.role} />
    </div>
  );
}

// Usage
function App() {
  const user = { name: 'Rahim', role: 'Developer', avatar: '/rahim.jpg' };
  return <UserCard user={user} />;
}
```

---

<a id="p1-functional"></a>

## 9. Functional Components

**Definition:**
Functional Component হলো একটি JavaScript function যা props নেয় এবং JSX return করে। React 16.8-এর পর Hooks দিয়ে functional component-এ state আর lifecycle পাওয়া যায় — এটাই এখন **recommended approach**।

**Structure:**
```jsx
// Arrow function syntax (most common)
const ComponentName = (props) => {
  return <JSX />;
};

// Function declaration syntax
function ComponentName(props) {
  return <JSX />;
}

// Destructured props
const ComponentName = ({ prop1, prop2 }) => {
  return <JSX />;
};
```

**Complete Example:**
```jsx
import { useState } from 'react';

function Counter({ initialCount = 0, step = 1 }) {
  const [count, setCount] = useState(initialCount);

  const increment = () => setCount(prev => prev + step);
  const decrement = () => setCount(prev => prev - step);
  const reset = () => setCount(initialCount);

  return (
    <div className="counter">
      <h2>Count: {count}</h2>
      <button onClick={decrement}>-</button>
      <button onClick={reset}>Reset</button>
      <button onClick={increment}>+</button>
    </div>
  );
}

export default Counter;

// Usage
// <Counter initialCount={10} step={5} />
```

**Functional Component-এর Advantages:**

| Advantage | বিবরণ |
|---|---|
| Simple syntax | কম code, বেশি readable |
| No `this` confusion | Arrow function-এ `this` binding নেই |
| Hooks support | useState, useEffect, custom hooks |
| Better testing | Pure function — easier to test |
| Performance | React-এর future optimizations functional-first |
| Tree shaking | Unused code eliminate সহজ |

**Follow-up Interview Questions:**
1. Functional component কি Class component-এর চেয়ে fast?
2. Functional component-এ `this` keyword কী?
3. Hooks ছাড়া functional component-এ state রাখা যায়?

---

<a id="p1-class"></a>

## 10. Class Components

**Definition:**
Class Component হলো ES6 class যা `React.Component` extend করে। `render()` method JSX return করে। React 16.8-এর আগে state আর lifecycle-এর জন্য class component ছিল একমাত্র option। এখন legacy code-এ দেখা যায়।

**Structure:**
```jsx
import React, { Component } from 'react';

class ComponentName extends Component {
  constructor(props) {
    super(props);
    this.state = {
      // initial state
    };
  }

  render() {
    return <JSX />;
  }
}
```

**Complete Example:**
```jsx
import React, { Component } from 'react';

class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
    // ⚠️ class component-এ bind করতে হয়
    this.increment = this.increment.bind(this);
  }

  increment() {
    this.setState(prevState => ({ count: prevState.count + 1 }));
  }

  decrement = () => {  // arrow function — auto bind
    this.setState(prevState => ({ count: prevState.count - 1 }));
  };

  componentDidMount() {
    console.log('Component mounted!');
  }

  componentDidUpdate(prevProps, prevState) {
    if (prevState.count !== this.state.count) {
      console.log('Count changed:', this.state.count);
    }
  }

  componentWillUnmount() {
    console.log('Component will unmount!');
  }

  render() {
    return (
      <div>
        <h2>Count: {this.state.count}</h2>
        <button onClick={this.decrement}>-</button>
        <button onClick={this.increment}>+</button>
      </div>
    );
  }
}
```

**Functional vs Class Component:**

| Feature | Functional | Class |
|---|---|---|
| Syntax | Simple function | ES6 class |
| State | `useState` hook | `this.state` |
| Lifecycle | `useEffect` hook | Lifecycle methods |
| `this` keyword | নেই | আছে (binding দরকার) |
| Code length | কম | বেশি |
| Performance | Same (React internally) | Same |
| Modern React | ✅ Recommended | ⚠️ Legacy |

**Interview-style Explanation:**
> "Class component-এ `this.state`, `this.setState()`, আর lifecycle methods যেমন `componentDidMount`, `componentDidUpdate` ব্যবহার করতে হয়। কিন্তু `this` binding confusing এবং code verbose। Hooks দিয়ে functional component-এ same কাজ অনেক কম code-এ করা যায়। নতুন project-এ functional component use করা best practice।"

---

<a id="p1-props"></a>

## 11. Props

**Definition:**
Props (Properties) হলো parent component থেকে child component-এ data pass করার mechanism। Props **read-only** — child কখনো props সরাসরি modify করে না।

**Real-life Analogy:**
Props হলো **function arguments**-এর মতো। আপনি যখন কাউকে চিঠি পাঠান, চিঠির ভেতরের content (props) recipient পরিবর্তন করে না — শুধু পড়ে।

**Props Basics:**
```jsx
// Parent — data পাঠায়
function App() {
  return (
    <UserCard
      name="Rahim"
      age={25}
      isActive={true}
      hobbies={['coding', 'reading']}
      address={{ city: 'Dhaka', district: 'Dhaka' }}
      onDelete={() => console.log('delete clicked')}
    />
  );
}

// Child — props receives
function UserCard({ name, age, isActive, hobbies, address, onDelete }) {
  return (
    <div>
      <h2>{name}, {age}</h2>
      <p>City: {address.city}</p>
      <p>Hobbies: {hobbies.join(', ')}</p>
      <span>{isActive ? '✅ Active' : '❌ Inactive'}</span>
      <button onClick={onDelete}>Delete</button>
    </div>
  );
}
```

**Default Props:**
```jsx
// Method 1: Default parameter (modern)
function Button({ text = 'Click Me', color = 'blue', size = 'medium' }) {
  return <button className={`btn btn-${color} btn-${size}`}>{text}</button>;
}

// Method 2: defaultProps (older)
Button.defaultProps = {
  text: 'Click Me',
  color: 'blue',
};
```

**Props Types (PropTypes validation):**
```jsx
import PropTypes from 'prop-types';

function UserCard({ name, age, email }) {
  return <div>{name} — {age}</div>;
}

UserCard.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number.isRequired,
  email: PropTypes.string,
};
```

**Children Props:**
```jsx
// children — special prop
function Card({ title, children }) {
  return (
    <div className="card">
      <h3>{title}</h3>
      <div className="card-body">
        {children}    {/* যা card-এর ভেতরে দেবেন */}
      </div>
    </div>
  );
}

// Usage
<Card title="User Info">
  <p>Name: Rahim</p>
  <p>Age: 25</p>
  <button>Edit</button>
</Card>
```

**Props Spreading:**
```jsx
const buttonProps = {
  className: 'btn-primary',
  disabled: false,
  type: 'submit',
};

// ✅ Spread operator
<button {...buttonProps}>Submit</button>

// Same as:
<button className="btn-primary" disabled={false} type="submit">Submit</button>
```

**Common Mistakes:**
- Props modify করার চেষ্টা করা — `props.name = 'new'` ❌ (immutable!)
- Props drilling (5+ levels নামানো) — Context API use করুন
- Function props-এ () দেওয়া — `onClick={handleClick}` ✅ না `onClick={handleClick()}` ❌

**Follow-up Interview Questions:**
1. Props immutable কেন?
2. Props drilling কী? কীভাবে avoid করবেন?
3. `children` prop কী?
4. TypeScript-এ props কীভাবে type করবেন?

---

<a id="p1-state"></a>

## 12. State

**Definition:**
State হলো component-এর internal, dynamic data যা time-এর সাথে পরিবর্তন হতে পারে। State change হলে React automatically component re-render করে। `useState` hook দিয়ে functional component-এ state manage করা হয়।

**Real-life Analogy:**
State হলো **whiteboard**-এর মতো। আপনি যা লেখেন তা পরিবর্তন করা যায় (mutable)। Props হলো **printed book** — unchangeable।

**Props vs State:**

| Feature | Props | State |
|---|---|---|
| কোথা থেকে আসে | Parent থেকে | Component নিজেই manage করে |
| Mutable | ❌ না | ✅ হ্যাঁ |
| Re-render trigger | Parent re-render করলে | setState call হলে |
| Ownership | Parent-এর | Component-এর নিজের |
| Access | `props.name` | `state` (class), `useState` value |

**useState Basics:**
```jsx
import { useState } from 'react';

function LoginForm() {
  // [current value, setter function]
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');
  const [isLoggedIn, setIsLoggedIn] = useState(false);
  const [error, setError] = useState(null);

  const handleSubmit = (e) => {
    e.preventDefault();
    if (username === 'rahim' && password === '1234') {
      setIsLoggedIn(true);
      setError(null);
    } else {
      setError('Invalid credentials');
    }
  };

  if (isLoggedIn) {
    return <h2>Welcome, {username}! 🎉</h2>;
  }

  return (
    <form onSubmit={handleSubmit}>
      <input
        value={username}
        onChange={e => setUsername(e.target.value)}
        placeholder="Username"
      />
      <input
        type="password"
        value={password}
        onChange={e => setPassword(e.target.value)}
        placeholder="Password"
      />
      {error && <p className="error">{error}</p>}
      <button type="submit">Login</button>
    </form>
  );
}
```

**State Update Rules:**
```jsx
// ✅ Functional update — previous state এর উপর depend করলে
setCount(prev => prev + 1);  // Safe for async batching

// ❌ Direct use — async issue হতে পারে
setCount(count + 1);  // Stale closure risk

// ✅ Object state update — spread করতে হবে
const [user, setUser] = useState({ name: '', age: 0 });
setUser(prev => ({ ...prev, name: 'Rahim' }));  // age preserve হবে

// ❌ Direct mutation — React re-render করবে না!
user.name = 'Rahim';  // NO! State directly mutate করবেন না
setUser(user);         // Reference same, React diff detect করবে না
```

**Common Mistakes:**
- State directly mutate করা — সবসময় new object/array দিন
- Async state-এ stale closure — functional update use করুন
- Unnecessary state — derive করা যায় এমন data state-এ রাখা

**Follow-up Interview Questions:**
1. State আর Props-এর পার্থক্য কী?
2. `setState` asynchronous কেন?
3. Object state update করার সময় কেন spread করতে হয়?
4. Derived state কী? কখন avoid করবেন?

---

<a id="p1-events"></a>

## 13. Event Handling

**Definition:**
React-এ event handling HTML-এর মতোই কিন্তু camelCase syntax, JSX-এ function reference, আর SyntheticEvent wrapper ব্যবহার করে। React সব events নিজে manage করে browser inconsistency handle করার জন্য।

**SyntheticEvent কী:**
React নিজে `SyntheticEvent` wrapper তৈরি করে যা সব browser-এ consistent behavior দেয়। এটি native event-এর একটি cross-browser wrapper।

**Common Events:**
```jsx
function EventExamples() {
  // Click event
  const handleClick = (e) => {
    e.preventDefault();
    console.log('Clicked!', e.target);
  };

  // Input change
  const handleChange = (e) => {
    console.log('Value:', e.target.value);
  };

  // Form submit
  const handleSubmit = (e) => {
    e.preventDefault();   // page reload prevent
    console.log('Form submitted');
  };

  // Keyboard event
  const handleKeyDown = (e) => {
    if (e.key === 'Enter') {
      console.log('Enter pressed');
    }
    if (e.ctrlKey && e.key === 's') {
      console.log('Ctrl+S pressed');
    }
  };

  // Mouse events
  const handleMouseEnter = () => console.log('Mouse entered');
  const handleMouseLeave = () => console.log('Mouse left');

  return (
    <div>
      <button onClick={handleClick}>Click Me</button>
      <input
        onChange={handleChange}
        onKeyDown={handleKeyDown}
      />
      <form onSubmit={handleSubmit}>
        <button type="submit">Submit</button>
      </form>
      <div
        onMouseEnter={handleMouseEnter}
        onMouseLeave={handleMouseLeave}
      >
        Hover me
      </div>
    </div>
  );
}
```

**Passing Arguments to Event Handlers:**
```jsx
function TodoList({ items, onDelete }) {
  return (
    <ul>
      {items.map(item => (
        <li key={item.id}>
          {item.text}
          {/* ✅ Arrow function দিয়ে argument pass */}
          <button onClick={() => onDelete(item.id)}>Delete</button>

          {/* ❌ এভাবে না — immediately call হবে! */}
          {/* <button onClick={onDelete(item.id)}>Delete</button> */}
        </li>
      ))}
    </ul>
  );
}
```

**Event Delegation — React-এর Optimization:**
```
React সব events document root-এ attach করে।
এটি event delegation pattern।
Individual element-এ event listener দেয় না।
Memory efficient + better performance।
```

**Common Mistakes:**
- `onClick={handleClick()}` — immediately invoke হবে, render-এ call হবে!
- `e.preventDefault()` ভুলে যাওয়া form submit-এ
- Event object async-এ use করা — `e.persist()` বা value আগে store করুন

**Follow-up Interview Questions:**
1. Synthetic Event কী? কেন দরকার?
2. Event bubbling React-এ কীভাবে stop করবেন?
3. `e.preventDefault()` আর `e.stopPropagation()` পার্থক্য?

```jsx
// Event bubbling stop
const handleInnerClick = (e) => {
  e.stopPropagation();  // parent-এ bubble হবে না
  console.log('Inner clicked');
};

const handleOuterClick = () => {
  console.log('Outer clicked');
};

<div onClick={handleOuterClick}>
  <button onClick={handleInnerClick}>Inner</button>
</div>
```

---

<a id="p1-conditional"></a>

## 14. Conditional Rendering

**Definition:**
Conditional rendering মানে condition-এর উপর ভিত্তি করে different UI দেখানো। JavaScript-এর `if/else`, ternary operator (`? :`), আর logical AND (`&&`) ব্যবহার করা হয়।

**Methods:**
```jsx
function ConditionalExamples({ isLoggedIn, role, notifications, data }) {

  // Method 1: if/else (return এর বাইরে)
  if (!data) {
    return <p>Loading...</p>;
  }

  // Method 2: ternary operator (JSX-এর ভেতরে)
  // condition ? <TrueComponent /> : <FalseComponent />

  // Method 3: Logical AND (condition true হলেই দেখাবে)
  // condition && <Component />

  // Method 4: Switch/object map (multiple conditions)

  return (
    <div>
      {/* Ternary — দুটি option */}
      {isLoggedIn
        ? <p>Welcome back! 👋</p>
        : <button>Login</button>
      }

      {/* Logical AND — একটি option (show/hide) */}
      {notifications > 0 && (
        <span className="badge">{notifications}</span>
      )}

      {/* Nested ternary — avoid করুন, readable না */}
      {/* role === 'admin' ? <AdminPanel /> : role === 'user' ? <UserPanel /> : null */}

      {/* Better — object map */}
      {{
        admin: <AdminPanel />,
        user: <UserPanel />,
        guest: <GuestPanel />,
      }[role] || <UnknownRole />}
    </div>
  );
}
```

**Loading/Error/Data Pattern (Common in interviews):**
```jsx
function ProductList() {
  const [products, setProducts] = useState([]);
  const [isLoading, setIsLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    fetch('/api/products')
      .then(res => res.json())
      .then(data => {
        setProducts(data);
        setIsLoading(false);
      })
      .catch(err => {
        setError(err.message);
        setIsLoading(false);
      });
  }, []);

  // Guard clauses — early return pattern
  if (isLoading) return <Spinner />;
  if (error) return <ErrorMessage message={error} />;
  if (products.length === 0) return <EmptyState />;

  return (
    <ul>
      {products.map(p => <ProductCard key={p.id} product={p} />)}
    </ul>
  );
}
```

**Common Mistakes:**
- `0 && <Component />` — `0` render হবে! `!!count && <Component />` বা `count > 0 && <Component />` use করুন
- Nested ternary — readable না, extract করুন

```jsx
// ❌ 0 renders as text!
{notifications && <Badge count={notifications} />}
// notifications=0 হলে "0" screen-এ দেখাবে!

// ✅ Fix:
{notifications > 0 && <Badge count={notifications} />}
```

---

<a id="p1-list"></a>

## 15. List Rendering

**Definition:**
React-এ array data render করতে JavaScript-এর `map()` method ব্যবহার করা হয়। প্রতিটি list item-এ unique `key` prop দিতে হয়।

**Basic List Rendering:**
```jsx
function ProductList({ products }) {
  return (
    <ul>
      {products.map(product => (
        <li key={product.id}>
          <h3>{product.name}</h3>
          <p>৳{product.price}</p>
        </li>
      ))}
    </ul>
  );
}
```

**List with Components:**
```jsx
function StudentList({ students }) {
  // Empty state
  if (students.length === 0) {
    return <p>No students found.</p>;
  }

  return (
    <div className="student-list">
      {students
        .filter(s => s.isActive)          // filter
        .sort((a, b) => a.name.localeCompare(b.name))  // sort
        .map(student => (
          <StudentCard
            key={student.id}
            name={student.name}
            grade={student.grade}
            gpa={student.gpa}
          />
        ))
      }
    </div>
  );
}

function StudentCard({ name, grade, gpa }) {
  return (
    <div className="card">
      <h3>{name}</h3>
      <p>Grade: {grade} | GPA: {gpa}</p>
    </div>
  );
}
```

**Nested List:**
```jsx
function Menu({ categories }) {
  return (
    <nav>
      {categories.map(category => (
        <div key={category.id}>
          <h3>{category.name}</h3>
          <ul>
            {category.items.map(item => (
              <li key={item.id}>{item.label}</li>
            ))}
          </ul>
        </div>
      ))}
    </nav>
  );
}
```

**Common Mistakes:**
- `key` না দেওয়া — React warning দেবে
- `key={index}` ব্যবহার করা reorder/delete হলে — unique ID use করুন
- map-এর return ভুলে যাওয়া

---

<a id="p1-keys"></a>

## 16. Keys in React

**Definition:**
Key হলো list-এর প্রতিটি element-এ দেওয়া একটি unique identifier যা React-কে help করে কোন item changed, added, বা removed হয়েছে তা efficiently identify করতে (reconciliation-এ)।

**কেন Key দরকার:**
```
List without key:
[A, B, C] → [A, X, B, C]  (X inserted at index 1)

Key ছাড়া React ভাবে:
- Index 1: B → X (changed)
- Index 2: C → B (changed)
- Index 3: (new) C
→ 3টি DOM operation!

Key দিয়ে React জানে:
- A: same position
- X: new item (insert)
- B: moved
- C: moved
→ 1টি DOM operation (insert X)!
```

**Key Best Practices:**
```jsx
// ✅ Unique, stable ID — best
{products.map(p => <ProductCard key={p.id} {...p} />)}

// ✅ String combination (যদি id না থাকে)
{items.map(item => <Item key={`${item.type}-${item.name}`} />)}

// ⚠️ Index — stable list-এ acceptable
{staticMenuItems.map((item, index) => <MenuItem key={index} {...item} />)}

// ❌ Index — reorderable/deletable list-এ
{todos.map((todo, index) => (
  <TodoItem key={index} todo={todo} />  // Bug: delete করলে wrong item re-render
))}

// ❌ Random key — প্রতি render-এ নতুন key → performance kill
{items.map(item => <Item key={Math.random()} />)}
```

**Index Key Bug Demo:**
```jsx
// কেন index key bug করে:
// todos = ['Buy milk', 'Go to gym', 'Code review']
// keys:     0           1            2

// 'Go to gym' delete করলে:
// todos = ['Buy milk', 'Code review']
// keys:     0           1

// React ভাবে: key=1 is now 'Code review'
// কিন্তু 'Code review' আগে key=2 ছিল
// React সঠিক DOM state maintain করতে পারে না!
// Bug: input fields মিশে যায়!
```

**Follow-up Interview Questions:**
1. Key হিসেবে array index কখন acceptable?
2. Key কি child component-এ prop হিসেবে পাওয়া যায়?
3. Key unique কোথায় হতে হবে — globally নাকি sibling-এর মধ্যে?

---

<a id="p1-lifecycle"></a>

## 17. Component Lifecycle Overview

**Definition:**
React component-এর তিনটি lifecycle phase আছে: Mount (DOM-এ add), Update (state/props change), এবং Unmount (DOM থেকে remove)।

**Lifecycle Phases:**

```
┌─────────────────────────────────────────────┐
│           COMPONENT LIFECYCLE               │
│                                             │
│  MOUNT          UPDATE          UNMOUNT     │
│  ─────          ──────          ───────     │
│  constructor    new props       cleanup     │
│  render()       new state       remove      │
│  DOM update     re-render       from DOM    │
│  useEffect(,[]) useEffect([x])  useEffect   │
│                                 return fn   │
└─────────────────────────────────────────────┘
```

**Functional Component Lifecycle (with Hooks):**
```jsx
import { useState, useEffect } from 'react';

function LifecycleDemo({ userId }) {
  const [user, setUser] = useState(null);

  // componentDidMount + componentDidUpdate combined
  useEffect(() => {
    console.log('Effect runs after render');

    // API call
    fetch(`/api/users/${userId}`)
      .then(res => res.json())
      .then(data => setUser(data));

    // componentWillUnmount — cleanup
    return () => {
      console.log('Cleanup! Component unmounting or userId changing');
    };
  }, [userId]);  // dependency: userId change হলে re-run

  // componentDidMount only (empty dependency array)
  useEffect(() => {
    console.log('Only runs once — on mount');
    document.title = 'User Profile';

    return () => {
      document.title = 'App';  // cleanup on unmount
    };
  }, []);

  if (!user) return <p>Loading...</p>;
  return <div>{user.name}</div>;
}
```

**Class Component vs Functional Lifecycle:**

| Lifecycle Event | Class Component | Functional (Hooks) |
|---|---|---|
| After mount | `componentDidMount()` | `useEffect(() => {}, [])` |
| After update | `componentDidUpdate()` | `useEffect(() => {}, [dep])` |
| Before unmount | `componentWillUnmount()` | `useEffect(() => { return () => {} }, [])` |
| Every render | `render()` | Function body |
| Initial state | `constructor` / `state = {}` | `useState()` |

---

## PART 1 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Say |
|---|---|---|
| React | JS Library for UI, component-based | Library, না framework |
| Virtual DOM | In-memory DOM, diffing algorithm | Batch updates, minimal Real DOM ops |
| SPA | Single HTML page, dynamic routing | SEO challenge, smooth UX |
| JSX | JS+HTML syntax, Babel compiles | `className`, camelCase, `{}` expressions |
| Functional Component | Modern, hooks-based | Recommended over class |
| Props | Parent→Child, read-only | Immutable, children prop |
| State | Internal dynamic data | useState, functional update |
| Events | SyntheticEvent, camelCase | `onClick={fn}` না `onClick={fn()}` |
| Conditional | ternary, &&, if/else | `0 &&` trap |
| List Rendering | `map()` + unique key | Index key bug |
| Keys | Reconciliation helper | Stable unique ID |
| Lifecycle | Mount/Update/Unmount | `useEffect` replaces all |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part2"></a>

## 📋 PART 2 সূচিপত্র — React Hooks

| # | Hook | Key Concept |
|---|---|---|
| 1 | [What are Hooks](#p2-what-hooks) | Rules, motivation |
| 2 | [useState](#p2-usestate) | Local state, re-render |
| 3 | [useEffect](#p2-useeffect) | Side effects, lifecycle |
| 4 | [useRef](#p2-useref) | DOM access, mutable ref |
| 5 | [useMemo](#p2-usememo) | Expensive computation cache |
| 6 | [useCallback](#p2-usecallback) | Function reference cache |
| 7 | [useContext](#p2-usecontext) | Global state, prop drilling solution |
| 8 | [useReducer](#p2-usereducer) | Complex state, Redux-like |
| 9 | [Custom Hooks](#p2-custom-hooks) | Reusable logic extraction |
| 10 | [Hook Rules](#p2-hook-rules) | Must follow, linting |
| 11 | [Dependency Array](#p2-dependency) | When effects run |
| 12 | [Cleanup Functions](#p2-cleanup) | Memory leak prevention |

---

<a id="p2-what-hooks"></a>

## 1. What are Hooks?

**Definition:**
Hooks হলো React 16.8-এ introduce হওয়া special functions যা functional component-এ React features (state, lifecycle, context) ব্যবহার করতে দেয়। নামের শুরু সবসময় `use` দিয়ে।

**কেন Hooks আসলো — Problems Solved:**

| Problem (Before Hooks) | Solution (With Hooks) |
|---|---|
| Stateful logic reuse কঠিন | Custom Hooks দিয়ে share করা যায় |
| Complex class lifecycle | `useEffect` একটিতে সব |
| `this` keyword confusion | নেই — plain functions |
| Code splitting কঠিন | Hook দিয়ে logic extract |
| Test করা কঠিন | Hooks easily testable |

**Available Built-in Hooks:**
```
Basic Hooks:
├── useState       — local state
├── useEffect      — side effects
└── useContext     — context value

Additional Hooks:
├── useRef         — mutable ref, DOM access
├── useMemo        — memoize value
├── useCallback    — memoize function
├── useReducer     — complex state
├── useLayoutEffect — sync DOM measurement
└── useId          — unique IDs

React 18+ Hooks:
├── useTransition  — non-urgent updates
├── useDeferredValue — defer value update
└── useSyncExternalStore — external stores
```

**Interview-style Explanation:**
> "Hooks React-এর game changer ছিল। আগে class component ছাড়া state রাখা যেত না। Hooks দিয়ে functional component-এ state, lifecycle, context সব পাওয়া যায়। আর Custom Hooks দিয়ে stateful logic extract করে যেকোনো component-এ reuse করা যায়।"

---

<a id="p2-usestate"></a>

## 2. useState

**Definition:**
`useState` হলো সবচেয়ে basic hook। এটি functional component-এ local state declare করে। State change হলে component re-render হয়।

**Syntax:**
```jsx
const [state, setState] = useState(initialValue);
//     ↑        ↑                   ↑
//  current   setter fn         initial value
//   value
```

**Internal Workflow:**
```
1. Initial render: useState(0) → state = 0
2. setState(1) call হলো
3. React schedules re-render
4. Component function আবার call হয়
5. useState(0) → এখন 0 নয়, saved state 1 return করে
6. New JSX render হয়
7. Virtual DOM diff → Real DOM update
```

**useState Deep Dive:**
```jsx
import { useState } from 'react';

function ShoppingCart() {
  // Primitive state
  const [count, setCount] = useState(0);
  const [message, setMessage] = useState('');

  // Object state
  const [user, setUser] = useState({
    name: '',
    email: '',
    age: 0,
  });

  // Array state
  const [items, setItems] = useState([]);

  // Lazy initialization (expensive computation)
  const [expensiveData, setExpensiveData] = useState(() => {
    // এই function শুধু initial render-এ call হবে
    return computeExpensiveValue();
  });

  // ──── State update patterns ────

  // Counter increment (functional update)
  const increment = () => setCount(prev => prev + 1);

  // Multiple rapid updates — functional update safe
  const addThree = () => {
    setCount(prev => prev + 1);
    setCount(prev => prev + 1);
    setCount(prev => prev + 1);
    // ✅ count 3 বাড়বে

    // ❌ Non-functional — সবগুলো same stale value use করবে
    // setCount(count + 1);  // শুধু 1 বাড়বে!
    // setCount(count + 1);
    // setCount(count + 1);
  };

  // Object state — always spread!
  const updateName = (newName) => {
    setUser(prev => ({ ...prev, name: newName }));
    // age আর email preserve হবে
  };

  // Array state
  const addItem = (item) => {
    setItems(prev => [...prev, item]);
  };

  const removeItem = (id) => {
    setItems(prev => prev.filter(item => item.id !== id));
  };

  const updateItem = (id, updates) => {
    setItems(prev =>
      prev.map(item =>
        item.id === id ? { ...item, ...updates } : item
      )
    );
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>+</button>
      <input
        value={user.name}
        onChange={e => updateName(e.target.value)}
      />
    </div>
  );
}
```

**Re-render Deep Dive:**
```jsx
// React কখন re-render করে?
// Object.is() দিয়ে compare করে

const [count, setCount] = useState(0);

// ❌ Same value — NO re-render
setCount(0);  // count already 0

// ✅ Different value — re-render
setCount(1);

// ❌ Same object reference — NO re-render
const [obj, setObj] = useState({ a: 1 });
setObj(obj);  // same reference

// ✅ New object — re-render
setObj({ ...obj, b: 2 });  // new object
```

**Common Mistakes:**
```jsx
// ❌ State directly mutate করা
const [items, setItems] = useState([1, 2, 3]);
items.push(4);          // BAD — React এটা detect করবে না
setItems(items);         // same reference!

// ✅ New array create করুন
setItems([...items, 4]);

// ❌ Object directly mutate
const [user, setUser] = useState({ name: 'Rahim' });
user.name = 'Karim';  // BAD
setUser(user);          // same reference!

// ✅ New object
setUser({ ...user, name: 'Karim' });
```

**Follow-up Interview Questions:**
1. useState-এর initial value কয়বার use হয়?
2. Batching কী? React 18-এ কী পরিবর্তন হয়েছে?
3. useState vs useReducer — কখন কোনটি?

---

<a id="p2-useeffect"></a>

## 3. useEffect

**Definition:**
`useEffect` hook দিয়ে functional component-এ **side effects** handle করা হয়। Side effect মানে: API call, DOM manipulation, subscription, timer, logging — যা React-এর render process-এর বাইরে।

**Syntax:**
```jsx
useEffect(() => {
  // effect code (side effect)
  return () => {
    // cleanup function (optional)
  };
}, [dependencies]);  // dependency array
```

**Three Modes:**
```jsx
// Mode 1: প্রতিটি render-এর পরে run
useEffect(() => {
  console.log('Every render');
});
// dependency array নেই → সব render-এ চলে

// Mode 2: শুধু mount-এ (once)
useEffect(() => {
  console.log('Only on mount');
}, []);
// empty array → শুধু first render-এ

// Mode 3: নির্দিষ্ট dependency change-এ
useEffect(() => {
  console.log('userId changed:', userId);
}, [userId]);
// userId change হলে re-run
```

**useEffect Execution Order:**
```
Render Phase:          Commit Phase:
1. Component renders   3. DOM updated
2. JSX returned        4. useEffect runs
                       5. (cleanup from previous effect)
```

**Real-world Examples:**
```jsx
function UserProfile({ userId }) {
  const [user, setUser] = useState(null);
  const [loading, setLoading] = useState(true);

  // API call — dependency: userId
  useEffect(() => {
    setLoading(true);

    const controller = new AbortController();  // cleanup-এর জন্য

    fetch(`/api/users/${userId}`, { signal: controller.signal })
      .then(res => res.json())
      .then(data => {
        setUser(data);
        setLoading(false);
      })
      .catch(err => {
        if (err.name !== 'AbortError') {
          console.error(err);
          setLoading(false);
        }
      });

    // Cleanup: component unmount বা userId change হলে request cancel
    return () => controller.abort();

  }, [userId]);  // userId change হলে re-run

  if (loading) return <Spinner />;
  return <div>{user?.name}</div>;
}
```

```jsx
function Timer() {
  const [seconds, setSeconds] = useState(0);

  // Timer setup — mount-এ start, unmount-এ clear
  useEffect(() => {
    const interval = setInterval(() => {
      setSeconds(prev => prev + 1);
    }, 1000);

    // Cleanup — memory leak prevent
    return () => clearInterval(interval);
  }, []);  // empty — once on mount

  return <p>Time: {seconds}s</p>;
}
```

```jsx
function SearchComponent({ query }) {
  const [results, setResults] = useState([]);

  // Debounced search
  useEffect(() => {
    if (!query) {
      setResults([]);
      return;
    }

    const timer = setTimeout(() => {
      fetch(`/api/search?q=${query}`)
        .then(res => res.json())
        .then(setResults);
    }, 300);  // 300ms debounce

    return () => clearTimeout(timer);  // Previous timer cancel
  }, [query]);

  return <SearchResults results={results} />;
}
```

```jsx
// Document title update
function ProductPage({ product }) {
  useEffect(() => {
    document.title = `${product.name} — My Shop`;
    return () => {
      document.title = 'My Shop';  // restore on unmount
    };
  }, [product.name]);

  return <div>{product.name}</div>;
}
```

**useEffect Internal Flow:**
```
Component renders (first time)
    ↓
DOM updated
    ↓
useEffect callback runs
    ↓
[later] userId changes
    ↓
Component re-renders
    ↓
DOM updated
    ↓
Previous effect cleanup runs
    ↓
New effect callback runs
```

**Common Mistakes:**
```jsx
// ❌ Infinite loop — state update dependency-তে
const [data, setData] = useState(null);
useEffect(() => {
  setData(fetchSomething());  // setData triggers re-render
}, [data]);  // data change → effect runs → setData → re-render → loop!

// ✅ Fix: empty dependency বা conditional
useEffect(() => {
  if (!data) {
    setData(fetchSomething());
  }
}, []);

// ❌ Async function directly in useEffect
useEffect(async () => {  // BAD — async function returns Promise
  const data = await fetch('/api');
}, []);

// ✅ Fix: inner async function
useEffect(() => {
  const fetchData = async () => {
    const res = await fetch('/api');
    const data = await res.json();
    setData(data);
  };
  fetchData();
}, []);
```

**Follow-up Interview Questions:**
1. useEffect কি synchronous নাকি asynchronous?
2. Cleanup function কখন run হয়?
3. Infinite loop কীভাবে হয় useEffect-এ?
4. `useLayoutEffect` vs `useEffect` পার্থক্য?

---

<a id="p2-useref"></a>

## 4. useRef

**Definition:**
`useRef` দুটি কাজ করে: DOM element directly access করা, এবং re-render না করে mutable value persist করা। `ref.current` property-তে value থাকে।

**Syntax:**
```jsx
const ref = useRef(initialValue);
// ref.current = initialValue (মুতুব্য, re-render করে না)
```

**Use Case 1: DOM Access**
```jsx
import { useRef, useEffect } from 'react';

function AutoFocusInput() {
  const inputRef = useRef(null);

  useEffect(() => {
    // Component mount-এ input-এ focus
    inputRef.current.focus();
  }, []);

  const handleClear = () => {
    inputRef.current.value = '';
    inputRef.current.focus();
  };

  return (
    <div>
      <input ref={inputRef} placeholder="Auto-focused input" />
      <button onClick={handleClear}>Clear</button>
    </div>
  );
}
```

```jsx
// Video player control
function VideoPlayer() {
  const videoRef = useRef(null);

  const play = () => videoRef.current.play();
  const pause = () => videoRef.current.pause();

  return (
    <div>
      <video ref={videoRef} src="/movie.mp4" />
      <button onClick={play}>▶ Play</button>
      <button onClick={pause}>⏸ Pause</button>
    </div>
  );
}
```

**Use Case 2: Persist Value Without Re-render**
```jsx
function ClickTracker() {
  const [displayCount, setDisplayCount] = useState(0);
  const clickCountRef = useRef(0);  // re-render করে না

  const handleClick = () => {
    clickCountRef.current += 1;  // silently increment
    console.log('Total clicks:', clickCountRef.current);
  };

  const showCount = () => {
    setDisplayCount(clickCountRef.current);  // এখন re-render
  };

  return (
    <div>
      <button onClick={handleClick}>Click (no re-render)</button>
      <button onClick={showCount}>Show Count</button>
      <p>Displayed count: {displayCount}</p>
    </div>
  );
}
```

**Use Case 3: Previous Value Store**
```jsx
function PreviousValueTracker({ value }) {
  const prevValueRef = useRef();

  useEffect(() => {
    prevValueRef.current = value;
  });

  const prevValue = prevValueRef.current;

  return (
    <div>
      <p>Current: {value}</p>
      <p>Previous: {prevValue}</p>
    </div>
  );
}
```

**useState vs useRef:**

| Feature | useState | useRef |
|---|---|---|
| Re-render on change | ✅ হ্যাঁ | ❌ না |
| Persistent across renders | ✅ | ✅ |
| DOM access | ❌ | ✅ |
| Trigger UI update | ✅ | ❌ |
| Use case | Dynamic UI data | DOM refs, timers, previous values |

**Common Mistakes:**
```jsx
// ❌ ref value UI-তে directly render করা
// ref change হলে UI update হবে না!
const countRef = useRef(0);
return <p>{countRef.current}</p>;  // won't update on change!

// ✅ useState for UI-visible data
const [count, setCount] = useState(0);

// ❌ useRef দিয়ে DOM-এ না থাকা element access
// component unmount হলে ref.current = null
```

**Follow-up Interview Questions:**
1. useRef আর useState-এর পার্থক্য?
2. `forwardRef` কী? কখন দরকার?
3. `useRef` দিয়ে কি closure problem solve হয়?

---

<a id="p2-usememo"></a>

## 5. useMemo

**Definition:**
`useMemo` একটি expensive calculation-এর result **memoize** করে — মানে cache করে রাখে। Dependency change না হলে cached result return করে, নতুন calculation করে না।

**Syntax:**
```jsx
const memoizedValue = useMemo(() => {
  return expensiveCalculation(a, b);
}, [a, b]);  // a বা b change হলে recalculate
```

**কখন useMemo দরকার:**
```
✅ Use useMemo when:
- Heavy computation (sorting, filtering large arrays)
- Referential equality (object/array passing to child)
- Expensive derived data

❌ Don't use useMemo when:
- Simple calculation (a + b)
- Rarely re-renders
- Premature optimization
```

**Real Example:**
```jsx
import { useState, useMemo } from 'react';

function ProductSearch({ products }) {
  const [searchTerm, setSearchTerm] = useState('');
  const [sortBy, setSortBy] = useState('name');
  const [counter, setCounter] = useState(0);  // unrelated state

  // ✅ useMemo — products বা sortBy বা searchTerm না বদলালে recalculate হবে না
  // counter change হলেও এই calculation হবে না
  const processedProducts = useMemo(() => {
    console.log('Processing products...');  // কতবার run হয় দেখুন

    const filtered = products.filter(p =>
      p.name.toLowerCase().includes(searchTerm.toLowerCase())
    );

    return [...filtered].sort((a, b) => {
      if (sortBy === 'name') return a.name.localeCompare(b.name);
      if (sortBy === 'price') return a.price - b.price;
      return 0;
    });

  }, [products, searchTerm, sortBy]);
  // counter dependency-তে নেই → counter change-এ recalculate হবে না

  return (
    <div>
      <input
        value={searchTerm}
        onChange={e => setSearchTerm(e.target.value)}
        placeholder="Search..."
      />
      <select value={sortBy} onChange={e => setSortBy(e.target.value)}>
        <option value="name">Sort by Name</option>
        <option value="price">Sort by Price</option>
      </select>
      <button onClick={() => setCounter(c => c + 1)}>
        Counter: {counter}
      </button>

      <ul>
        {processedProducts.map(p => (
          <li key={p.id}>{p.name} — ৳{p.price}</li>
        ))}
      </ul>
    </div>
  );
}
```

**Object Reference Problem (useMemo solves):**
```jsx
// Without useMemo — child re-renders unnecessarily
function Parent() {
  const [count, setCount] = useState(0);

  // ❌ প্রতি render-এ new object → child always re-renders
  const config = { theme: 'dark', lang: 'bn' };

  // ✅ useMemo — same reference যদি না বদলায়
  const config = useMemo(() => ({
    theme: 'dark',
    lang: 'bn'
  }), []);

  return (
    <>
      <button onClick={() => setCount(c => c + 1)}>{count}</button>
      <ChildComponent config={config} />  {/* config change না হলে re-render নেই */}
    </>
  );
}
```

**Follow-up Interview Questions:**
1. useMemo কি always performance improve করে?
2. useMemo vs useCallback পার্থক্য?
3. Memoization-এর cost কী?

---

<a id="p2-usecallback"></a>

## 6. useCallback

**Definition:**
`useCallback` একটি **function-কে memoize** করে। Dependency না বদলালে same function reference return করে। `useMemo`-এর মতোই কিন্তু function-এর জন্য।

**Syntax:**
```jsx
const memoizedFn = useCallback(() => {
  doSomething(a, b);
}, [a, b]);
```

**কেন দরকার — Reference Equality Problem:**
```jsx
// ❌ Problem — প্রতি render-এ নতুন function তৈরি হয়
function Parent() {
  const [count, setCount] = useState(0);

  const handleDelete = (id) => {
    // ...delete logic
  };
  // প্রতি render-এ handleDelete নতুন reference
  // Child-এ React.memo থাকলেও re-render হবে কারণ prop changed!

  return <ChildList onDelete={handleDelete} />;
}

// ✅ Fix — useCallback দিয়ে same reference
function Parent() {
  const [count, setCount] = useState(0);

  const handleDelete = useCallback((id) => {
    setItems(prev => prev.filter(item => item.id !== id));
  }, []);  // no dependencies — never changes

  return <ChildList onDelete={handleDelete} />;
}
```

**Complete Example:**
```jsx
import { useState, useCallback, memo } from 'react';

// React.memo — props change না হলে re-render হবে না
const TodoItem = memo(function TodoItem({ todo, onToggle, onDelete }) {
  console.log(`TodoItem render: ${todo.text}`);
  return (
    <li>
      <input
        type="checkbox"
        checked={todo.done}
        onChange={() => onToggle(todo.id)}
      />
      {todo.text}
      <button onClick={() => onDelete(todo.id)}>×</button>
    </li>
  );
});

function TodoApp() {
  const [todos, setTodos] = useState([
    { id: 1, text: 'Buy groceries', done: false },
    { id: 2, text: 'Read book', done: true },
  ]);
  const [count, setCount] = useState(0);  // unrelated state

  // ✅ useCallback — function reference stable
  const handleToggle = useCallback((id) => {
    setTodos(prev =>
      prev.map(t => t.id === id ? { ...t, done: !t.done } : t)
    );
  }, []);

  const handleDelete = useCallback((id) => {
    setTodos(prev => prev.filter(t => t.id !== id));
  }, []);

  return (
    <div>
      {/* count change হলে TodoItem re-render হবে না — useCallback + memo */}
      <button onClick={() => setCount(c => c + 1)}>Counter: {count}</button>
      <ul>
        {todos.map(todo => (
          <TodoItem
            key={todo.id}
            todo={todo}
            onToggle={handleToggle}
            onDelete={handleDelete}
          />
        ))}
      </ul>
    </div>
  );
}
```

**useMemo vs useCallback:**

| | useMemo | useCallback |
|---|---|---|
| Returns | Memoized **value** | Memoized **function** |
| Use for | Expensive calculations | Stable function reference |
| Equivalent | `useMemo(() => fn, deps)` | `useCallback(fn, deps)` |

**Common Mistakes:**
```jsx
// ❌ Over-optimization — simple case-এ overhead বেশি
const handleClick = useCallback(() => {
  console.log('clicked');
}, []);
// এতটুকু simple function-এ useCallback unnecessary

// ✅ Use when:
// 1. Function child component-এ prop হিসেবে যাচ্ছে (React.memo সহ)
// 2. Function useEffect dependency
```

---

<a id="p2-usecontext"></a>

## 7. useContext

**Definition:**
`useContext` hook দিয়ে React Context-এর value পড়া যায়। Context হলো **global state** mechanism — props drilling ছাড়াই deeply nested component-এ data pass করা যায়।

**Props Drilling Problem:**
```
App (has user data)
  └── Layout
        └── Sidebar
              └── UserMenu  ← needs user data
                    └── Avatar ← needs user data

Without Context: App→Layout→Sidebar→UserMenu→Avatar সব props দিয়ে পাস করতে হতো!
```

**Context Setup — 3 Steps:**
```jsx
// Step 1: Context তৈরি (separate file)
// context/ThemeContext.js
import { createContext, useState, useContext } from 'react';

const ThemeContext = createContext(null);

// Step 2: Provider দিয়ে wrap
export function ThemeProvider({ children }) {
  const [theme, setTheme] = useState('light');

  const toggleTheme = () => {
    setTheme(prev => prev === 'light' ? 'dark' : 'light');
  };

  return (
    <ThemeContext.Provider value={{ theme, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
}

// Step 3: Custom hook (best practice)
export function useTheme() {
  const context = useContext(ThemeContext);
  if (!context) {
    throw new Error('useTheme must be used within ThemeProvider');
  }
  return context;
}
```

```jsx
// App.jsx — Provider দিয়ে wrap
import { ThemeProvider } from './context/ThemeContext';

function App() {
  return (
    <ThemeProvider>
      <Layout />
    </ThemeProvider>
  );
}
```

```jsx
// যেকোনো nested component-এ — props drill ছাড়া!
import { useTheme } from './context/ThemeContext';

function ThemeToggleButton() {
  const { theme, toggleTheme } = useTheme();
  return (
    <button
      onClick={toggleTheme}
      style={{ background: theme === 'dark' ? '#333' : '#fff' }}
    >
      {theme === 'dark' ? '☀️ Light' : '🌙 Dark'}
    </button>
  );
}

function Avatar({ src }) {
  const { theme } = useTheme();
  return (
    <img
      src={src}
      className={`avatar avatar-${theme}`}
    />
  );
}
```

**Real-world Auth Context:**
```jsx
// context/AuthContext.jsx
import { createContext, useContext, useState } from 'react';

const AuthContext = createContext(null);

export function AuthProvider({ children }) {
  const [user, setUser] = useState(null);
  const [token, setToken] = useState(localStorage.getItem('token'));

  const login = async (credentials) => {
    const res = await fetch('/api/login', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(credentials),
    });
    const data = await res.json();
    setUser(data.user);
    setToken(data.token);
    localStorage.setItem('token', data.token);
  };

  const logout = () => {
    setUser(null);
    setToken(null);
    localStorage.removeItem('token');
  };

  return (
    <AuthContext.Provider value={{ user, token, login, logout, isLoggedIn: !!token }}>
      {children}
    </AuthContext.Provider>
  );
}

export const useAuth = () => {
  const ctx = useContext(AuthContext);
  if (!ctx) throw new Error('useAuth must be used within AuthProvider');
  return ctx;
};
```

**Context vs Redux:**

| | Context | Redux |
|---|---|---|
| Setup | Simple | Complex (boilerplate) |
| Performance | Re-renders all consumers | Selective re-renders |
| DevTools | Limited | Excellent |
| Best for | Theme, Auth, Language | Large complex state |
| Async | Manual | Redux Thunk/Saga |

**Common Mistakes:**
```jsx
// ❌ Unnecessary re-renders — object value প্রতি render-এ নতুন
<ThemeContext.Provider value={{ theme, toggleTheme }}>
// প্রতি render-এ new object → সব consumers re-render!

// ✅ Fix — useMemo দিয়ে value memoize
const contextValue = useMemo(() => ({
  theme, toggleTheme
}), [theme]);

<ThemeContext.Provider value={contextValue}>
```

---

<a id="p2-usereducer"></a>

## 8. useReducer

**Definition:**
`useReducer` hook complex state logic handle করার জন্য। Redux-এর মতো pattern — action dispatch করলে reducer function state update করে। Multiple related state values বা complex state transitions-এ useful।

**Syntax:**
```jsx
const [state, dispatch] = useReducer(reducer, initialState);

// Reducer function
function reducer(state, action) {
  switch (action.type) {
    case 'ACTION_TYPE':
      return { ...state, /* updated */ };
    default:
      return state;
  }
}
```

**useState vs useReducer:**

| | useState | useReducer |
|---|---|---|
| Best for | Simple, independent state | Complex, related state |
| Update logic | In component | In reducer (outside) |
| Action pattern | Direct setter | Dispatch action object |
| Testing | Medium | Easy (pure function) |
| Multiple state | Multiple useState | One reducer |

**Complete Example — Shopping Cart:**
```jsx
import { useReducer } from 'react';

// Initial state
const initialState = {
  items: [],
  total: 0,
  itemCount: 0,
};

// Reducer — pure function
function cartReducer(state, action) {
  switch (action.type) {
    case 'ADD_ITEM': {
      const existing = state.items.find(i => i.id === action.payload.id);
      if (existing) {
        const updatedItems = state.items.map(i =>
          i.id === action.payload.id
            ? { ...i, quantity: i.quantity + 1 }
            : i
        );
        return {
          ...state,
          items: updatedItems,
          total: state.total + action.payload.price,
          itemCount: state.itemCount + 1,
        };
      }
      return {
        ...state,
        items: [...state.items, { ...action.payload, quantity: 1 }],
        total: state.total + action.payload.price,
        itemCount: state.itemCount + 1,
      };
    }

    case 'REMOVE_ITEM': {
      const item = state.items.find(i => i.id === action.payload.id);
      if (!item) return state;
      return {
        ...state,
        items: state.items.filter(i => i.id !== action.payload.id),
        total: state.total - (item.price * item.quantity),
        itemCount: state.itemCount - item.quantity,
      };
    }

    case 'CLEAR_CART':
      return initialState;

    default:
      throw new Error(`Unknown action: ${action.type}`);
  }
}

// Component
function ShoppingCart() {
  const [cart, dispatch] = useReducer(cartReducer, initialState);

  const addToCart = (product) => {
    dispatch({ type: 'ADD_ITEM', payload: product });
  };

  const removeFromCart = (id) => {
    dispatch({ type: 'REMOVE_ITEM', payload: { id } });
  };

  const clearCart = () => {
    dispatch({ type: 'CLEAR_CART' });
  };

  return (
    <div>
      <h2>Cart ({cart.itemCount} items)</h2>
      <p>Total: ৳{cart.total}</p>
      {cart.items.map(item => (
        <div key={item.id}>
          <span>{item.name} × {item.quantity}</span>
          <button onClick={() => removeFromCart(item.id)}>Remove</button>
        </div>
      ))}
      <button onClick={clearCart}>Clear Cart</button>
    </div>
  );
}
```

**Follow-up Interview Questions:**
1. useReducer কখন useState-এর চেয়ে better?
2. Redux আর useReducer পার্থক্য?
3. Reducer function pure হওয়া কেন important?

---

<a id="p2-custom-hooks"></a>

## 9. Custom Hooks

**Definition:**
Custom Hook হলো একটি JavaScript function যার নাম `use` দিয়ে শুরু হয় এবং যেকোনো built-in hook call করতে পারে। এটি **stateful logic reuse** করার pattern।

**কেন Custom Hook:**
```
একই logic বারবার different component-এ লেখা → DRY violation
Custom Hook → extract করুন → যেকোনো component-এ reuse
```

**Common Custom Hooks:**
```jsx
// ──── 1. useFetch — API data fetching ────
function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    const controller = new AbortController();

    setLoading(true);
    setError(null);

    fetch(url, { signal: controller.signal })
      .then(res => {
        if (!res.ok) throw new Error(`HTTP ${res.status}`);
        return res.json();
      })
      .then(data => {
        setData(data);
        setLoading(false);
      })
      .catch(err => {
        if (err.name !== 'AbortError') {
          setError(err.message);
          setLoading(false);
        }
      });

    return () => controller.abort();
  }, [url]);

  return { data, loading, error };
}

// Usage — যেকোনো component-এ
function UserList() {
  const { data: users, loading, error } = useFetch('/api/users');
  if (loading) return <Spinner />;
  if (error) return <Error message={error} />;
  return <ul>{users.map(u => <li key={u.id}>{u.name}</li>)}</ul>;
}

function ProductList() {
  const { data: products, loading } = useFetch('/api/products');
  // same hook, different data!
}
```

```jsx
// ──── 2. useLocalStorage — localStorage sync ────
function useLocalStorage(key, initialValue) {
  const [value, setValue] = useState(() => {
    try {
      const stored = localStorage.getItem(key);
      return stored ? JSON.parse(stored) : initialValue;
    } catch {
      return initialValue;
    }
  });

  const setStoredValue = (newValue) => {
    const valueToStore = typeof newValue === 'function'
      ? newValue(value)
      : newValue;
    setValue(valueToStore);
    localStorage.setItem(key, JSON.stringify(valueToStore));
  };

  return [value, setStoredValue];
}

// Usage
function Settings() {
  const [theme, setTheme] = useLocalStorage('theme', 'light');
  const [language, setLanguage] = useLocalStorage('language', 'bn');
  // Automatically synced to localStorage!
}
```

```jsx
// ──── 3. useDebounce — debounced value ────
function useDebounce(value, delay = 300) {
  const [debouncedValue, setDebouncedValue] = useState(value);

  useEffect(() => {
    const timer = setTimeout(() => {
      setDebouncedValue(value);
    }, delay);
    return () => clearTimeout(timer);
  }, [value, delay]);

  return debouncedValue;
}

// Usage
function SearchBox() {
  const [query, setQuery] = useState('');
  const debouncedQuery = useDebounce(query, 500);

  useEffect(() => {
    if (debouncedQuery) {
      searchAPI(debouncedQuery);
    }
  }, [debouncedQuery]);
  // API call শুধু 500ms পরে, typing-এ না
}
```

```jsx
// ──── 4. useToggle ────
function useToggle(initial = false) {
  const [value, setValue] = useState(initial);
  const toggle = useCallback(() => setValue(v => !v), []);
  const setTrue = useCallback(() => setValue(true), []);
  const setFalse = useCallback(() => setValue(false), []);
  return [value, toggle, setTrue, setFalse];
}

// Usage
function Modal() {
  const [isOpen, toggleModal, openModal, closeModal] = useToggle(false);
  return (
    <>
      <button onClick={openModal}>Open</button>
      {isOpen && <div className="modal">
        <button onClick={closeModal}>Close</button>
      </div>}
    </>
  );
}
```

**Follow-up Interview Questions:**
1. Custom hook কি component?
2. Same custom hook দুটি component-এ use করলে state share হয়?
3. Custom hook-এ hook rules apply হয়?

> **Important:** Same custom hook দুটি component-এ use করলে state **share হয় না** — প্রতিটি component-এ independent state।

---

<a id="p2-hook-rules"></a>

## 10. Hook Rules

**Definition:**
React Hooks-এর দুটি mandatory rules আছে যা ভাঙলে bugs হয়। `eslint-plugin-react-hooks` এই rules enforce করে।

**Rule 1: Only Call Hooks at the Top Level**
```jsx
// ✅ Correct — top level-এ
function Component() {
  const [count, setCount] = useState(0);  // ✅
  const [name, setName] = useState('');   // ✅
  useEffect(() => { }, []);               // ✅

  return <div>{count}</div>;
}

// ❌ Wrong — conditional-এ
function Component({ isAdmin }) {
  if (isAdmin) {
    const [data, setData] = useState(null);  // ❌ conditional hook!
  }

  // ❌ loop-এ
  for (let i = 0; i < 5; i++) {
    const [item, setItem] = useState(null);  // ❌
  }
}
```

**কেন এই Rule:**
```
React hook call order track করে linked list-এ।
First render:  useState → useEffect → useRef (order: 1,2,3)
Second render: useState → useEffect → useRef (order: 1,2,3 — same!)

Conditional-এ hook থাকলে:
First render:  isAdmin=true  → useState → useEffect → useRef (1,2,3)
Second render: isAdmin=false → useEffect → useRef (1,2 — order mismatch!)
→ React state wrong করে দেবে!
```

**Rule 2: Only Call Hooks from React Functions**
```jsx
// ✅ Functional Component-এ
function MyComponent() {
  const [state, setState] = useState(0);  // ✅
}

// ✅ Custom Hook-এ
function useMyHook() {
  const [state, setState] = useState(0);  // ✅
}

// ❌ Regular function-এ
function regularFunction() {
  const [state, setState] = useState(0);  // ❌
}

// ❌ Class component-এ
class MyClass extends Component {
  render() {
    const [state, setState] = useState(0);  // ❌
  }
}
```

**ESLint Setup:**
```bash
npm install eslint-plugin-react-hooks --save-dev
```
```json
// .eslintrc
{
  "plugins": ["react-hooks"],
  "rules": {
    "react-hooks/rules-of-hooks": "error",
    "react-hooks/exhaustive-deps": "warn"
  }
}
```

---

<a id="p2-dependency"></a>

## 11. Dependency Array

**Definition:**
`useEffect`, `useMemo`, `useCallback`-এর দ্বিতীয় argument হলো dependency array। এই array-এর values change হলে effect/memo/callback re-run হয়।

**Three Cases:**
```jsx
// Case 1: No dependency array → every render
useEffect(() => {
  console.log('Every render');
});

// Case 2: Empty array → only on mount
useEffect(() => {
  console.log('Mount only');
}, []);

// Case 3: With dependencies → when deps change
useEffect(() => {
  console.log('userId or role changed');
}, [userId, role]);
```

**Common Dependency Issues:**
```jsx
// ❌ Missing dependency — ESLint warning
function Component({ userId }) {
  const [user, setUser] = useState(null);

  useEffect(() => {
    fetchUser(userId).then(setUser);
  }, []);  // ⚠️ userId missing! stale closure bug
  // userId prop change হলেও re-fetch হবে না!

  // ✅ Fix
  useEffect(() => {
    fetchUser(userId).then(setUser);
  }, [userId]);
}
```

```jsx
// ❌ Object/array dependency — infinite loop
const config = { timeout: 5000 };  // প্রতি render-এ new object

useEffect(() => {
  fetchWithConfig(config);
}, [config]);  // config প্রতিবার new reference → infinite loop!

// ✅ Fix — useMemo বা primitive values
const timeout = 5000;
useEffect(() => {
  fetchWithConfig({ timeout });
}, [timeout]);  // primitive — safe
```

```jsx
// ❌ Function dependency — possible infinite loop
function Component() {
  const fetchData = () => fetch('/api/data');  // প্রতি render-এ new fn

  useEffect(() => {
    fetchData();
  }, [fetchData]);  // infinite loop!

  // ✅ Fix — useCallback
  const fetchData = useCallback(() => fetch('/api/data'), []);

  useEffect(() => {
    fetchData();
  }, [fetchData]);
}
```

**Dependency Array Cheatsheet:**

| Array | কখন runs |
|---|---|
| না দেওয়া | Every render |
| `[]` | Mount only |
| `[a]` | Mount + when a changes |
| `[a, b]` | Mount + when a or b changes |

---

<a id="p2-cleanup"></a>

## 12. Cleanup Functions

**Definition:**
`useEffect`-এর return function হলো cleanup। Component unmount হওয়ার আগে বা next effect run-এর আগে চলে। Memory leak আর stale data prevent করে।

**কেন Cleanup দরকার:**
```
Memory Leaks:
- Timer চলছে, component নেই
- Event listener attached, component গেছে
- API response আসছে, component unmounted
- WebSocket connection open, component gone
```

**Cleanup Examples:**
```jsx
// ──── Timer cleanup ────
function Countdown({ from }) {
  const [count, setCount] = useState(from);

  useEffect(() => {
    if (count <= 0) return;

    const timer = setTimeout(() => {
      setCount(c => c - 1);
    }, 1000);

    return () => clearTimeout(timer);  // cleanup!
  }, [count]);

  return <p>{count > 0 ? count : '🎉 Done!'}</p>;
}
```

```jsx
// ──── Event listener cleanup ────
function WindowSizeTracker() {
  const [size, setSize] = useState({
    width: window.innerWidth,
    height: window.innerHeight,
  });

  useEffect(() => {
    const handleResize = () => {
      setSize({ width: window.innerWidth, height: window.innerHeight });
    };

    window.addEventListener('resize', handleResize);

    // Cleanup — prevent memory leak
    return () => window.removeEventListener('resize', handleResize);
  }, []);

  return <p>{size.width} × {size.height}</p>;
}
```

```jsx
// ──── API request cleanup ────
function UserProfile({ userId }) {
  const [user, setUser] = useState(null);

  useEffect(() => {
    let isMounted = true;  // flag approach
    const controller = new AbortController();

    fetch(`/api/users/${userId}`, { signal: controller.signal })
      .then(res => res.json())
      .then(data => {
        if (isMounted) {  // component এখনো mounted?
          setUser(data);
        }
      });

    return () => {
      isMounted = false;
      controller.abort();  // fetch cancel
    };
  }, [userId]);

  return user ? <div>{user.name}</div> : <Spinner />;
}
```

```jsx
// ──── WebSocket cleanup ────
function LiveChat({ roomId }) {
  const [messages, setMessages] = useState([]);

  useEffect(() => {
    const ws = new WebSocket(`wss://chat.example.com/room/${roomId}`);

    ws.onmessage = (event) => {
      setMessages(prev => [...prev, JSON.parse(event.data)]);
    };

    ws.onerror = (error) => {
      console.error('WebSocket error:', error);
    };

    // Cleanup — connection close করুন
    return () => {
      ws.close();
    };
  }, [roomId]);

  return (
    <div>
      {messages.map((msg, i) => (
        <p key={i}>{msg.user}: {msg.text}</p>
      ))}
    </div>
  );
}
```

**Cleanup Flow:**
```
Component mounts → Effect runs
userId changes:
    1. Cleanup previous effect (abort old fetch)
    2. Re-render
    3. New effect runs (new fetch)
Component unmounts:
    1. Final cleanup (abort any pending fetch)
```

---

## PART 2 Quick Revision Table

| Hook | Purpose | Key Point |
|---|---|---|
| `useState` | Local state | Functional update for prev-dependent updates |
| `useEffect` | Side effects | Cleanup function, dependency array |
| `useRef` | DOM access + mutable value | No re-render on change |
| `useMemo` | Cache expensive value | Returns memoized value |
| `useCallback` | Cache function reference | Prevents child re-renders with memo |
| `useContext` | Consume context | Custom hook wrapper best practice |
| `useReducer` | Complex state | Action dispatch, pure reducer |
| Custom Hooks | Reuse stateful logic | `use` prefix, independent state per component |
| Hook Rules | Call at top level only | No conditionals/loops |
| Dependency Array | Control effect timing | Missing dep = stale closure |
| Cleanup | Prevent memory leaks | Timer, listeners, fetch cancel |

---

## PART 1 & 2 Common Interview Questions (Quick List)

**PART 1 — Fundamentals:**
1. React কী? Framework না Library?
2. Virtual DOM কীভাবে কাজ করে?
3. JSX-এ `class` লিখলে কী হবে?
4. Props আর State পার্থক্য?
5. `key` হিসেবে index কখন ব্যবহার করা যাবে না?
6. Functional vs Class component — কোনটি prefer করবেন কেন?
7. Controlled vs Uncontrolled component কী?

**PART 2 — Hooks:**
1. Hooks-এর দুটি rules কী কী?
2. `useEffect` dependency array-এ empty `[]` দিলে কী হয়?
3. `useState`-এ object update করতে spread কেন দরকার?
4. `useMemo` আর `useCallback` পার্থক্য?
5. Custom Hook কি component?
6. Cleanup function কখন call হয়?
7. `useRef` দিয়ে কী করা যায় যা `useState` দিয়ে পারা যায় না?

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 3 — React Component Architecture *(Next request এ লিখব)*
