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

<a id="part3"></a>

## 📋 PART 3 সূচিপত্র — React Component Architecture

| # | Topic | Key Concept |
|---|---|---|
| 1 | [Component Communication](#p3-communication) | Data flow patterns overview |
| 2 | [Parent to Child](#p3-parent-child) | Props, one-way flow |
| 3 | [Child to Parent](#p3-child-parent) | Callback functions |
| 4 | [Lifting State Up](#p3-lifting-state) | Shared state in common ancestor |
| 5 | [Controlled vs Uncontrolled](#p3-controlled) | Form input patterns |
| 6 | [Reusable Components](#p3-reusable) | Design principles |
| 7 | [Compound Components](#p3-compound) | Implicit state sharing pattern |
| 8 | [Higher Order Components (HOC)](#p3-hoc) | Component wrapper pattern |
| 9 | [Render Props](#p3-render-props) | Function as children |
| 10 | [Composition vs Inheritance](#p3-composition) | React's preferred pattern |

---

<a id="p3-communication"></a>

## 1. Component Communication — Overview

**Definition:**
React-এ components নিজেদের মধ্যে বিভিন্নভাবে communicate করে। Data flow unidirectional হওয়ায় নির্দিষ্ট patterns follow করতে হয়।

**Communication Patterns:**

```
Direct Relationship:
  Parent → Child         : Props দিয়ে
  Child → Parent         : Callback function দিয়ে
  Sibling ↔ Sibling      : Lifting state up

Distant Relationship:
  Any → Any (global)     : Context API / Redux / Zustand
  Deep nested            : Context API (prop drilling avoid)
```

**Communication Pattern চার্ট:**

| Relationship | Pattern | Tool |
|---|---|---|
| Parent → Child | Props | `<Child data={value} />` |
| Child → Parent | Callback | `<Child onEvent={handler} />` |
| Sibling → Sibling | Lifting State | Common parent-এ state রাখা |
| Deeply Nested | Context | `useContext` / Redux |
| Unrelated | Global State | Redux, Zustand, Context |

**Interview-style Explanation:**
> "React-এ data সবসময় top-down — parent থেকে child। কিন্তু child যদি parent-কে কিছু জানাতে চায়, parent একটি callback function prop হিসেবে দেয়, child সেই function call করে। দূরের component-এর মধ্যে communicate করতে Context বা Redux use করি।"

---

<a id="p3-parent-child"></a>

## 2. Parent to Child Communication

**Definition:**
Parent component child-এ data পাঠায় **props** এর মাধ্যমে। এটি React-এর সবচেয়ে মৌলিক data flow — unidirectional, predictable।

**Basic Pattern:**
```jsx
// Parent — data রাখে, child-এ পাঠায়
function ParentComponent() {
  const [products, setProducts] = useState([
    { id: 1, name: 'Laptop', price: 75000, stock: 10 },
    { id: 2, name: 'Phone', price: 25000, stock: 5 },
    { id: 3, name: 'Tablet', price: 35000, stock: 0 },
  ]);

  return (
    <div className="product-grid">
      {products.map(product => (
        <ProductCard
          key={product.id}
          name={product.name}
          price={product.price}
          inStock={product.stock > 0}
          stockCount={product.stock}
        />
      ))}
    </div>
  );
}

// Child — props receive করে display করে
function ProductCard({ name, price, inStock, stockCount }) {
  return (
    <div className={`card ${inStock ? 'available' : 'out-of-stock'}`}>
      <h3>{name}</h3>
      <p>৳{price.toLocaleString('bn-BD')}</p>
      {inStock
        ? <span className="badge green">In Stock ({stockCount})</span>
        : <span className="badge red">Out of Stock</span>
      }
    </div>
  );
}
```

**Complex Props — Objects, Arrays, Functions:**
```jsx
function DashboardPage() {
  const user = { name: 'Rahim', role: 'admin', avatar: '/rahim.jpg' };
  const permissions = ['read', 'write', 'delete'];
  const stats = { orders: 142, revenue: 285000, users: 1204 };

  const handleLogout = () => {
    console.log('logout');
  };

  return (
    <>
      <Header
        user={user}
        permissions={permissions}
        onLogout={handleLogout}
      />
      <StatsPanel stats={stats} />
    </>
  );
}

function Header({ user, permissions, onLogout }) {
  const canDelete = permissions.includes('delete');

  return (
    <nav>
      <img src={user.avatar} alt={user.name} />
      <span>{user.name} ({user.role})</span>
      {canDelete && <span className="admin-badge">Admin</span>}
      <button onClick={onLogout}>Logout</button>
    </nav>
  );
}
```

**Props Forwarding / Spreading:**
```jsx
// Button wrapper — সব HTML button props forward করে
function Button({ children, variant = 'primary', loading, ...rest }) {
  return (
    <button
      className={`btn btn-${variant} ${loading ? 'loading' : ''}`}
      disabled={loading}
      {...rest}   // onClick, type, aria-label, etc. automatically forward
    >
      {loading ? <Spinner /> : children}
    </button>
  );
}

// Usage — extra props automatically forwarded
<Button
  variant="danger"
  loading={isSubmitting}
  onClick={handleDelete}
  type="button"
  aria-label="Delete item"
>
  Delete
</Button>
```

**Follow-up Interview Questions:**
1. Props immutable কেন? React কি enforce করে?
2. Component-এ অনেক props দিতে হলে কী করবেন?
3. TypeScript-এ props কীভাবে type করবেন?

---

<a id="p3-child-parent"></a>

## 3. Child to Parent Communication

**Definition:**
Child component সরাসরি parent-এর state change করতে পারে না। Parent একটি **callback function** prop হিসেবে দেয়, child সেটি call করে data উপরে পাঠায়।

**Basic Callback Pattern:**
```jsx
// Parent — callback define করে, child-এ দেয়
function ShoppingApp() {
  const [cart, setCart] = useState([]);
  const [searchQuery, setSearchQuery] = useState('');

  // ✅ Callback — child এটি call করবে
  const handleAddToCart = (product) => {
    setCart(prev => [...prev, product]);
  };

  const handleSearch = (query) => {
    setSearchQuery(query);
  };

  return (
    <div>
      <SearchBar onSearch={handleSearch} />
      <ProductList
        query={searchQuery}
        onAddToCart={handleAddToCart}
      />
      <CartSummary itemCount={cart.length} />
    </div>
  );
}

// Child — callback prop call করে parent-কে notify করে
function SearchBar({ onSearch }) {
  const [value, setValue] = useState('');

  const handleChange = (e) => {
    setValue(e.target.value);
    onSearch(e.target.value);  // Parent-কে জানায়
  };

  return (
    <input
      value={value}
      onChange={handleChange}
      placeholder="Search products..."
    />
  );
}

function ProductList({ query, onAddToCart }) {
  const products = useProducts(query);  // custom hook

  return (
    <ul>
      {products.map(product => (
        <li key={product.id}>
          {product.name}
          <button onClick={() => onAddToCart(product)}>
            Add to Cart
          </button>
        </li>
      ))}
    </ul>
  );
}
```

**Form Submit Pattern (Child → Parent):**
```jsx
// Reusable form component — submit করলে parent পায়
function LoginForm({ onSubmit, onForgotPassword }) {
  const [credentials, setCredentials] = useState({
    email: '',
    password: '',
  });
  const [error, setError] = useState('');

  const handleChange = (field) => (e) => {
    setCredentials(prev => ({ ...prev, [field]: e.target.value }));
    setError('');
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    if (!credentials.email || !credentials.password) {
      setError('All fields required');
      return;
    }
    onSubmit(credentials);  // ✅ Parent-এ data পাঠানো
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="email"
        value={credentials.email}
        onChange={handleChange('email')}
        placeholder="Email"
      />
      <input
        type="password"
        value={credentials.password}
        onChange={handleChange('password')}
        placeholder="Password"
      />
      {error && <p className="error">{error}</p>}
      <button type="submit">Login</button>
      <button type="button" onClick={onForgotPassword}>
        Forgot Password?
      </button>
    </form>
  );
}

// Parent uses form
function LoginPage() {
  const navigate = useNavigate();

  const handleLogin = async (credentials) => {
    try {
      await loginAPI(credentials);
      navigate('/dashboard');
    } catch (err) {
      console.error(err);
    }
  };

  return (
    <div className="login-page">
      <h1>Welcome Back</h1>
      <LoginForm
        onSubmit={handleLogin}
        onForgotPassword={() => navigate('/forgot-password')}
      />
    </div>
  );
}
```

**Common Mistakes:**
```jsx
// ❌ Prop name inconsistency
<Button onClick={handleClick} />  // HTML-like
<Modal onClose={handleClose} />   // React-like

// ✅ Convention: "on" prefix for event callbacks
onSubmit, onClose, onDelete, onSelect, onChange, onSearch

// ❌ Directly mutating parent state
function Child({ items, setItems }) {
  items.push(newItem);  // Direct mutation — BAD
  setItems(items);      // Same reference, no re-render
}

// ✅ Use callback
function Child({ onAddItem }) {
  onAddItem(newItem);  // Parent handles immutable update
}
```

---

<a id="p3-lifting-state"></a>

## 4. Lifting State Up

**Definition:**
দুটি sibling component-এ same data দরকার হলে সেই state তাদের **common ancestor** (parent)-এ রাখা হয়। Parent উভয়কে props দেয়। এটি "lifting state up" pattern।

**Real-life Analogy:**
দুটি সন্তান (sibling components) একই তথ্য শেয়ার করতে চায় — তারা parent-কে জানায়, parent উভয়কে update করে। Central source of truth।

**Problem Without Lifting:**
```jsx
// ❌ Each has own state — out of sync
function TemperatureConverter() {
  return (
    <>
      <CelsiusInput />   {/* নিজের state */}
      <FahrenheitInput /> {/* নিজের state — sync হয় না! */}
    </>
  );
}
```

**Lifting State Up — Solution:**
```jsx
// ✅ State parent-এ — both in sync
function TemperatureConverter() {
  const [celsius, setCelsius] = useState('');

  const fahrenheit = celsius !== '' ? (celsius * 9/5 + 32).toFixed(1) : '';

  return (
    <div>
      <h2>Temperature Converter</h2>
      <TemperatureInput
        unit="Celsius"
        value={celsius}
        onChange={setCelsius}
      />
      <TemperatureInput
        unit="Fahrenheit"
        value={fahrenheit}
        onChange={(f) => setCelsius(((f - 32) * 5/9).toFixed(1))}
      />
      {celsius && (
        <p>
          {celsius}°C = {fahrenheit}°F
          {celsius >= 100 ? ' 🔥 Boiling!' : celsius <= 0 ? ' 🧊 Freezing!' : ''}
        </p>
      )}
    </div>
  );
}

function TemperatureInput({ unit, value, onChange }) {
  return (
    <label>
      {unit}:
      <input
        type="number"
        value={value}
        onChange={e => onChange(e.target.value)}
        placeholder={`Enter ${unit}`}
      />
    </label>
  );
}
```

**Real-world Example — Filter + List:**
```jsx
// State lifted to parent — Filter আর List synchronized
function ProductPage() {
  // Lifted state
  const [category, setCategory] = useState('all');
  const [priceRange, setPriceRange] = useState([0, 100000]);
  const [sortBy, setSortBy] = useState('name');

  return (
    <div className="product-page">
      <FilterPanel
        category={category}
        priceRange={priceRange}
        sortBy={sortBy}
        onCategoryChange={setCategory}
        onPriceChange={setPriceRange}
        onSortChange={setSortBy}
      />
      <ProductGrid
        category={category}
        priceRange={priceRange}
        sortBy={sortBy}
      />
    </div>
  );
}

function FilterPanel({ category, onCategoryChange, sortBy, onSortChange }) {
  return (
    <aside>
      <select value={category} onChange={e => onCategoryChange(e.target.value)}>
        <option value="all">All</option>
        <option value="electronics">Electronics</option>
        <option value="clothing">Clothing</option>
      </select>
      <select value={sortBy} onChange={e => onSortChange(e.target.value)}>
        <option value="name">Name</option>
        <option value="price">Price</option>
      </select>
    </aside>
  );
}

function ProductGrid({ category, priceRange, sortBy }) {
  const products = useFilteredProducts(category, priceRange, sortBy);
  return (
    <main>
      {products.map(p => <ProductCard key={p.id} {...p} />)}
    </main>
  );
}
```

**When to Lift State:**
```
✅ Lift state when:
- Two siblings need same data
- A component needs to control another
- Data needs to be shared across subtree

❌ Don't over-lift:
- Every state to root — performance issue
- State only one component needs — keep it local
```

**Follow-up Interview Questions:**
1. State কতটা উপরে নেওয়া উচিত?
2. Lifting state vs Context — কখন কোনটি?
3. Performance-এ lifting state-এর impact কী?

---

<a id="p3-controlled"></a>

## 5. Controlled vs Uncontrolled Components

**Definition:**
**Controlled component** এ form input-এর value React state দ্বারা নিয়ন্ত্রিত। **Uncontrolled component** এ DOM নিজেই value রাখে, `useRef` দিয়ে access করা হয়।

**Controlled Component:**
```jsx
// ✅ Controlled — React state = single source of truth
function RegistrationForm() {
  const [formData, setFormData] = useState({
    name: '',
    email: '',
    phone: '',
    password: '',
  });
  const [errors, setErrors] = useState({});

  const handleChange = (field) => (e) => {
    setFormData(prev => ({ ...prev, [field]: e.target.value }));
    // Validate on change
    if (errors[field]) {
      setErrors(prev => ({ ...prev, [field]: '' }));
    }
  };

  const validate = () => {
    const newErrors = {};
    if (!formData.name.trim()) newErrors.name = 'Name required';
    if (!formData.email.includes('@')) newErrors.email = 'Invalid email';
    if (formData.phone.length < 11) newErrors.phone = 'Invalid phone';
    if (formData.password.length < 6) newErrors.password = 'Min 6 characters';
    return newErrors;
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    const validationErrors = validate();
    if (Object.keys(validationErrors).length > 0) {
      setErrors(validationErrors);
      return;
    }
    console.log('Submitting:', formData);
  };

  return (
    <form onSubmit={handleSubmit}>
      <div>
        <input
          value={formData.name}
          onChange={handleChange('name')}
          placeholder="Full Name"
        />
        {errors.name && <span className="error">{errors.name}</span>}
      </div>
      <div>
        <input
          type="email"
          value={formData.email}
          onChange={handleChange('email')}
          placeholder="Email"
        />
        {errors.email && <span className="error">{errors.email}</span>}
      </div>
      <button type="submit">Register</button>
    </form>
  );
}
```

**Uncontrolled Component:**
```jsx
// Uncontrolled — DOM keeps value, ref দিয়ে access
function FileUploadForm() {
  const nameRef = useRef(null);
  const fileRef = useRef(null);

  const handleSubmit = (e) => {
    e.preventDefault();
    const name = nameRef.current.value;
    const file = fileRef.current.files[0];
    console.log('Name:', name, 'File:', file?.name);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input ref={nameRef} defaultValue="Default Name" />
      <input ref={fileRef} type="file" accept=".pdf,.doc" />
      <button type="submit">Upload</button>
    </form>
  );
}
```

**Controlled vs Uncontrolled Comparison:**

| Feature | Controlled | Uncontrolled |
|---|---|---|
| Value stored in | React state | DOM |
| Access via | `value` prop | `ref.current.value` |
| Validation | Real-time, easy | On submit only |
| Instant feedback | ✅ | ❌ |
| Complex forms | ✅ | ❌ |
| File input | ❌ (uncontrollable) | ✅ |
| Performance | More re-renders | Fewer re-renders |
| Code | More | Less |
| Recommended | ✅ (most cases) | ⚠️ (file/legacy) |

**When to Use Uncontrolled:**
```
- File input (<input type="file">) — always uncontrolled
- Integrating with non-React library
- Very simple form (just submit, no validation)
- Performance critical large forms
```

**Interview-style Explanation:**
> "Controlled component-এ input-এর value সবসময় React state থেকে আসে — `value={state}` আর `onChange` দিয়ে state update করি। এতে form-এর full control React-এর হাতে থাকে, validation সহজ। Uncontrolled-এ DOM value রাখে, ref দিয়ে পড়ি — simpler কিন্তু real-time validation কঠিন। File input সবসময় uncontrolled।"

---

<a id="p3-reusable"></a>

## 6. Reusable Components

**Definition:**
Reusable component এমনভাবে design করা হয় যাতে different contexts-এ আলাদা আলাদা data দিয়ে use করা যায়। Good reusable component: **single responsibility**, **configurable via props**, এবং **independent**।

**Principles:**
```
1. Single Responsibility — একটি component একটি কাজ
2. Props-driven — behavior props দিয়ে configure
3. No hardcoded data — data প্রপ থেকে
4. Composable — ছোট components দিয়ে বড় বানানো
5. Documented — PropTypes / TypeScript types
```

**Bad → Good Refactor:**
```jsx
// ❌ Not reusable — hardcoded, specific
function SubmitOrderButton() {
  return (
    <button
      style={{ background: 'blue', color: 'white', padding: '10px 20px' }}
      onClick={() => submitOrder()}
    >
      Submit Order
    </button>
  );
}

// ✅ Reusable — configurable
function Button({
  children,
  onClick,
  variant = 'primary',       // primary | secondary | danger | ghost
  size = 'medium',           // small | medium | large
  loading = false,
  disabled = false,
  fullWidth = false,
  leftIcon,
  rightIcon,
  type = 'button',
}) {
  const classes = [
    'btn',
    `btn-${variant}`,
    `btn-${size}`,
    fullWidth && 'btn-full',
    loading && 'btn-loading',
  ].filter(Boolean).join(' ');

  return (
    <button
      type={type}
      className={classes}
      onClick={onClick}
      disabled={disabled || loading}
    >
      {leftIcon && <span className="btn-icon-left">{leftIcon}</span>}
      {loading ? <Spinner size="small" /> : children}
      {rightIcon && <span className="btn-icon-right">{rightIcon}</span>}
    </button>
  );
}

// Use anywhere with different config
<Button variant="primary" size="large" onClick={handleSubmit}>Submit Order</Button>
<Button variant="danger" size="small" onClick={handleDelete}>Delete</Button>
<Button variant="ghost" loading={isLoading}>Save Draft</Button>
<Button variant="primary" fullWidth type="submit">Login</Button>
```

**Reusable Card Component:**
```jsx
function Card({
  children,
  title,
  subtitle,
  footer,
  headerAction,
  padding = 'normal',
  shadow = true,
  bordered = true,
  className = '',
}) {
  return (
    <div className={[
      'card',
      shadow && 'card-shadow',
      bordered && 'card-bordered',
      `card-padding-${padding}`,
      className,
    ].filter(Boolean).join(' ')}>
      {(title || headerAction) && (
        <div className="card-header">
          <div>
            {title && <h3 className="card-title">{title}</h3>}
            {subtitle && <p className="card-subtitle">{subtitle}</p>}
          </div>
          {headerAction && <div className="card-action">{headerAction}</div>}
        </div>
      )}
      <div className="card-body">{children}</div>
      {footer && <div className="card-footer">{footer}</div>}
    </div>
  );
}

// Multiple uses
<Card title="Monthly Revenue" subtitle="May 2026">
  <RevenueChart />
</Card>

<Card
  title="Recent Orders"
  headerAction={<Button size="small">View All</Button>}
  footer={<Pagination />}
>
  <OrderTable orders={orders} />
</Card>
```

---

<a id="p3-compound"></a>

## 7. Compound Components

**Definition:**
Compound Components pattern হলো একটি group of components যারা একসাথে কাজ করে, implicit state share করে। HTML-এর `<select>` + `<option>` এর মতো — এরা together কাজ করে।

**Real-life Analogy:**
`<select>` আর `<option>` এর সম্পর্কের মতো — `<option>` alone কাজ করে না, `<select>` এর context দরকার।

**Example — Tabs Component:**
```jsx
import { createContext, useContext, useState } from 'react';

// ──── Context for implicit state sharing ────
const TabsContext = createContext(null);

// ──── Parent — state owns করে ────
function Tabs({ children, defaultTab }) {
  const [activeTab, setActiveTab] = useState(defaultTab);

  return (
    <TabsContext.Provider value={{ activeTab, setActiveTab }}>
      <div className="tabs">{children}</div>
    </TabsContext.Provider>
  );
}

// ──── TabList — tab buttons container ────
function TabList({ children }) {
  return <div className="tab-list" role="tablist">{children}</div>;
}

// ──── Tab — individual tab button ────
function Tab({ id, children }) {
  const { activeTab, setActiveTab } = useContext(TabsContext);
  const isActive = activeTab === id;

  return (
    <button
      role="tab"
      aria-selected={isActive}
      className={`tab ${isActive ? 'tab-active' : ''}`}
      onClick={() => setActiveTab(id)}
    >
      {children}
    </button>
  );
}

// ──── TabPanels — panels container ────
function TabPanels({ children }) {
  return <div className="tab-panels">{children}</div>;
}

// ──── TabPanel — individual panel ────
function TabPanel({ id, children }) {
  const { activeTab } = useContext(TabsContext);
  if (activeTab !== id) return null;

  return (
    <div role="tabpanel" className="tab-panel">
      {children}
    </div>
  );
}

// ──── Attach sub-components ────
Tabs.List = TabList;
Tabs.Tab = Tab;
Tabs.Panels = TabPanels;
Tabs.Panel = TabPanel;

// ──── Usage — clean, declarative ────
function ProfilePage() {
  return (
    <Tabs defaultTab="overview">
      <Tabs.List>
        <Tabs.Tab id="overview">Overview</Tabs.Tab>
        <Tabs.Tab id="orders">Orders</Tabs.Tab>
        <Tabs.Tab id="settings">Settings</Tabs.Tab>
      </Tabs.List>

      <Tabs.Panels>
        <Tabs.Panel id="overview">
          <UserOverview />
        </Tabs.Panel>
        <Tabs.Panel id="orders">
          <OrderHistory />
        </Tabs.Panel>
        <Tabs.Panel id="settings">
          <AccountSettings />
        </Tabs.Panel>
      </Tabs.Panels>
    </Tabs>
  );
}
```

**Compound Components — Accordion:**
```jsx
const AccordionContext = createContext(null);

function Accordion({ children, allowMultiple = false }) {
  const [openItems, setOpenItems] = useState(new Set());

  const toggle = (id) => {
    setOpenItems(prev => {
      const next = new Set(prev);
      if (next.has(id)) {
        next.delete(id);
      } else {
        if (!allowMultiple) next.clear();
        next.add(id);
      }
      return next;
    });
  };

  return (
    <AccordionContext.Provider value={{ openItems, toggle }}>
      <div className="accordion">{children}</div>
    </AccordionContext.Provider>
  );
}

function AccordionItem({ id, title, children }) {
  const { openItems, toggle } = useContext(AccordionContext);
  const isOpen = openItems.has(id);

  return (
    <div className="accordion-item">
      <button
        className="accordion-header"
        onClick={() => toggle(id)}
        aria-expanded={isOpen}
      >
        {title}
        <span>{isOpen ? '▲' : '▼'}</span>
      </button>
      {isOpen && (
        <div className="accordion-body">{children}</div>
      )}
    </div>
  );
}

Accordion.Item = AccordionItem;

// Usage
<Accordion allowMultiple>
  <Accordion.Item id="faq1" title="React কী?">
    React হলো Facebook-এর JavaScript UI library।
  </Accordion.Item>
  <Accordion.Item id="faq2" title="Hooks কী?">
    Hooks হলো functional component-এ state ব্যবহারের mechanism।
  </Accordion.Item>
</Accordion>
```

**Follow-up Interview Questions:**
1. Compound components-এর benefit কী regular props-এর চেয়ে?
2. Context ছাড়া compound components বানানো যায়?
3. `React.Children` API কী?

---

<a id="p3-hoc"></a>

## 8. Higher Order Components (HOC)

**Definition:**
Higher Order Component (HOC) হলো একটি function যা একটি component নেয় এবং enhanced version return করে। এটি **cross-cutting concerns** (logging, auth check, loading, error handling) reuse করার pattern।

**Structure:**
```jsx
function withEnhancement(WrappedComponent) {
  function EnhancedComponent(props) {
    // Extra logic
    return <WrappedComponent {...props} />;
  }
  EnhancedComponent.displayName = `withEnhancement(${WrappedComponent.displayName || WrappedComponent.name})`;
  return EnhancedComponent;
}
```

**HOC Examples:**
```jsx
// ──── 1. withAuth — Protected component ────
function withAuth(WrappedComponent) {
  return function AuthenticatedComponent(props) {
    const { isLoggedIn, user } = useAuth();

    if (!isLoggedIn) {
      return <Navigate to="/login" replace />;
    }

    return <WrappedComponent {...props} user={user} />;
  };
}

// Usage
const ProtectedDashboard = withAuth(Dashboard);
const ProtectedProfile = withAuth(Profile);
```

```jsx
// ──── 2. withLoading — Loading state ────
function withLoading(WrappedComponent) {
  return function LoadingComponent({ isLoading, loadingText = 'Loading...', ...props }) {
    if (isLoading) {
      return (
        <div className="loading-container">
          <Spinner />
          <p>{loadingText}</p>
        </div>
      );
    }
    return <WrappedComponent {...props} />;
  };
}

const ProductListWithLoading = withLoading(ProductList);

// Usage
<ProductListWithLoading
  isLoading={loading}
  loadingText="Fetching products..."
  products={products}
/>
```

```jsx
// ──── 3. withErrorBoundary ────
function withErrorBoundary(WrappedComponent, FallbackComponent) {
  return class extends React.Component {
    state = { hasError: false, error: null };

    static getDerivedStateFromError(error) {
      return { hasError: true, error };
    }

    componentDidCatch(error, info) {
      console.error('Error caught by HOC:', error, info);
    }

    render() {
      if (this.state.hasError) {
        return FallbackComponent
          ? <FallbackComponent error={this.state.error} />
          : <div>Something went wrong!</div>;
      }
      return <WrappedComponent {...this.props} />;
    }
  };
}

const SafeChart = withErrorBoundary(Chart, ErrorFallback);
```

```jsx
// ──── 4. withLogger ────
function withLogger(WrappedComponent) {
  return function LoggedComponent(props) {
    useEffect(() => {
      console.log(`[${WrappedComponent.name}] mounted`, props);
      return () => {
        console.log(`[${WrappedComponent.name}] unmounted`);
      };
    }, []);

    return <WrappedComponent {...props} />;
  };
}
```

**HOC Compose করা:**
```jsx
// Multiple HOCs chain করা
const EnhancedComponent = withLogger(withAuth(withLoading(Dashboard)));

// বা compose utility দিয়ে (Redux-style)
const compose = (...fns) => (x) => fns.reduceRight((acc, fn) => fn(acc), x);
const EnhancedDashboard = compose(
  withLogger,
  withAuth,
  withLoading
)(Dashboard);
```

**HOC vs Custom Hooks:**

| | HOC | Custom Hook |
|---|---|---|
| Returns | Component | Value/function |
| Logic sharing | ✅ | ✅ |
| Props interference | ⚠️ Possible | ❌ None |
| JSX involvement | ✅ Can wrap JSX | ❌ Logic only |
| Modern React | ⚠️ Less preferred | ✅ Preferred |
| Debugging | Complex (wrapper hell) | Clear |

**Interview-style Explanation:**
> "HOC হলো component factory — একটি component নেয়, extra behavior যোগ করে, নতুন component return করে। `withAuth`, `withLoading`, `connect()` (Redux) — সব HOC। এখন Custom Hooks HOC-এর অনেক use case cover করে, তাই modern code-এ HOC কম দেখা যায়।"

---

<a id="p3-render-props"></a>

## 9. Render Props

**Definition:**
Render Props হলো একটি pattern যেখানে component একটি **function prop** নেয় এবং সেই function-এ তার internal state/data pass করে call করে। এটি code sharing-এর আরেকটি pattern।

**Basic Pattern:**
```jsx
// Component with render prop
function MouseTracker({ render }) {
  const [position, setPosition] = useState({ x: 0, y: 0 });

  const handleMouseMove = (e) => {
    setPosition({ x: e.clientX, y: e.clientY });
  };

  return (
    <div onMouseMove={handleMouseMove} style={{ height: '200px' }}>
      {render(position)}   {/* internal state pass করে function call */}
    </div>
  );
}

// Usage — render prop-এ যা চাই তা render করি
<MouseTracker
  render={({ x, y }) => (
    <p>Mouse at: ({x}, {y})</p>
  )}
/>

<MouseTracker
  render={({ x, y }) => (
    <div
      className="cursor-follower"
      style={{ left: x, top: y }}
    />
  )}
/>
```

**Children as Function (common variant):**
```jsx
// "children as a function" — render prop-এর elegant version
function DataFetcher({ url, children }) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    fetch(url)
      .then(r => r.json())
      .then(d => { setData(d); setLoading(false); })
      .catch(e => { setError(e.message); setLoading(false); });
  }, [url]);

  return children({ data, loading, error });
}

// Usage — children হলো function
<DataFetcher url="/api/products">
  {({ data, loading, error }) => {
    if (loading) return <Spinner />;
    if (error) return <ErrorMessage message={error} />;
    return <ProductList products={data} />;
  }}
</DataFetcher>

<DataFetcher url="/api/users">
  {({ data: users, loading }) =>
    loading ? <Spinner /> : <UserTable users={users} />
  }
</DataFetcher>
```

**Render Props vs Custom Hooks:**
```jsx
// Same logic — Render Props version
<Toggle>
  {({ isOn, toggle }) => (
    <button onClick={toggle}>{isOn ? 'ON' : 'OFF'}</button>
  )}
</Toggle>

// Same logic — Custom Hook version (cleaner)
function MyButton() {
  const [isOn, toggle] = useToggle(false);
  return <button onClick={toggle}>{isOn ? 'ON' : 'OFF'}</button>;
}
```

> **Note:** Render Props এখন Custom Hooks দিয়ে replace করা হয় বেশিরভাগ ক্ষেত্রে। Legacy codebase-এ দেখা যায়, interview-এ জানা দরকার।

---

<a id="p3-composition"></a>

## 10. Composition vs Inheritance

**Definition:**
React **composition over inheritance** recommend করে। Component-এ behavior add করার জন্য class inheritance-এর বদলে components compose করা হয়।

**React-এ কেন Inheritance নয়:**
```jsx
// ❌ Inheritance — React-এ এভাবে করা হয় না
class SpecialButton extends Button {
  render() {
    return super.render();  // Fragile, tightly coupled
  }
}

// ✅ Composition — React way
function SpecialButton({ children, ...props }) {
  return (
    <Button {...props} className="special">
      <StarIcon />
      {children}
    </Button>
  );
}
```

**Composition Patterns:**
```jsx
// ──── 1. Containment — children prop ────
function Modal({ title, children, footer, onClose }) {
  return (
    <div className="modal-overlay" onClick={onClose}>
      <div className="modal" onClick={e => e.stopPropagation()}>
        <div className="modal-header">
          <h2>{title}</h2>
          <button onClick={onClose}>×</button>
        </div>
        <div className="modal-body">{children}</div>
        {footer && <div className="modal-footer">{footer}</div>}
      </div>
    </div>
  );
}

// Modal reused with different content
<Modal title="Delete Confirm" onClose={close} footer={<ConfirmButtons />}>
  <p>Are you sure you want to delete this item?</p>
</Modal>

<Modal title="Add Product" onClose={close}>
  <ProductForm onSubmit={handleAdd} />
</Modal>
```

```jsx
// ──── 2. Specialization — specific version of general ────
function Dialog({ title, message, actions }) {
  return (
    <div className="dialog">
      <h3>{title}</h3>
      <p>{message}</p>
      <div className="dialog-actions">{actions}</div>
    </div>
  );
}

// Specialized versions
function ConfirmDialog({ onConfirm, onCancel, message }) {
  return (
    <Dialog
      title="Confirm Action"
      message={message}
      actions={
        <>
          <Button variant="ghost" onClick={onCancel}>Cancel</Button>
          <Button variant="danger" onClick={onConfirm}>Confirm</Button>
        </>
      }
    />
  );
}

function AlertDialog({ onOk, message, type = 'info' }) {
  return (
    <Dialog
      title={type === 'error' ? '⛔ Error' : 'ℹ️ Info'}
      message={message}
      actions={<Button onClick={onOk}>OK</Button>}
    />
  );
}
```

**Composition — Layout Pattern:**
```jsx
// Flexible layout composition
function PageLayout({ sidebar, header, children, footer }) {
  return (
    <div className="page-layout">
      {header && <header className="page-header">{header}</header>}
      <div className="page-content">
        {sidebar && <aside className="sidebar">{sidebar}</aside>}
        <main className="main-content">{children}</main>
      </div>
      {footer && <footer className="page-footer">{footer}</footer>}
    </div>
  );
}

// Compose with different content
<PageLayout
  header={<DashboardHeader />}
  sidebar={<NavigationMenu />}
  footer={<AppFooter />}
>
  <Dashboard />
</PageLayout>

<PageLayout header={<MinimalHeader />}>
  <LoginPage />
</PageLayout>
```

**Follow-up Interview Questions:**
1. React কেন inheritance recommend করে না?
2. `children` prop আর `render` prop-এর পার্থক্য?
3. HOC vs Render Props vs Custom Hooks — কোনটি prefer করবেন?

---

## PART 3 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Say |
|---|---|---|
| Communication | Parent→Child: props, Child→Parent: callback | Data unidirectional |
| Parent→Child | Props, spread, children | Props immutable |
| Child→Parent | Callback function props | `on` prefix convention |
| Lifting State | Shared state in common ancestor | Single source of truth |
| Controlled | React state = form value | `value` + `onChange` |
| Uncontrolled | DOM holds value, ref reads | File input always uncontrolled |
| Reusable | Single responsibility, configurable | Props-driven, no hardcode |
| Compound | Context-based implicit sharing | `<Tabs.Tab>`, `<Select.Option>` |
| HOC | Component → Enhanced Component | `withAuth`, `withLoading` |
| Render Props | Function prop gets internal state | Children as function |
| Composition | compose, not inherit | `children` prop, specialization |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part4"></a>

## 📋 PART 4 সূচিপত্র — React Routing & Navigation

| # | Topic | Key Concept |
|---|---|---|
| 1 | [React Router Overview](#p4-overview) | Client-side routing |
| 2 | [BrowserRouter Setup](#p4-browserrouter) | Installation, basic setup |
| 3 | [Routes & Route](#p4-routes) | Defining routes |
| 4 | [Route Parameters](#p4-params) | Dynamic segments, useParams |
| 5 | [Nested Routing](#p4-nested) | Layout routes, outlet |
| 6 | [Navigation](#p4-navigation) | Link, NavLink, useNavigate |
| 7 | [Protected Routes](#p4-protected) | Auth-based routing |
| 8 | [Lazy Loading Routes](#p4-lazy) | Code splitting |
| 9 | [Dynamic Routing](#p4-dynamic) | Data-driven routes |
| 10 | [SPA Navigation Flow](#p4-flow) | Complete flow diagram |

---

<a id="p4-overview"></a>

## 1. React Router Overview

**Definition:**
React Router হলো React-এর সবচেয়ে popular routing library। SPA-তে URL change করলে different components render করার mechanism। Browser-এর URL আর React component-এর মধ্যে mapping করে।

**কেন React Router:**
```
Traditional website: URL change → Server নতুন HTML পাঠায়
SPA with React Router: URL change → Client-side JS different component render করে
                                   → Server-এ কোনো request যায় না!
```

**React Router v6 — Key Concepts:**

| Concept | কী করে |
|---|---|
| `BrowserRouter` | HTML5 History API use করে routing |
| `Routes` | Route definitions container |
| `Route` | URL pattern → component mapping |
| `Link` | SPA-friendly `<a>` tag |
| `NavLink` | Active state সহ Link |
| `Outlet` | Nested route render point |
| `useNavigate` | Programmatic navigation |
| `useParams` | URL parameters পড়া |
| `useLocation` | Current URL info |
| `useSearchParams` | Query string manage |

**Installation:**
```bash
npm install react-router-dom
```

---

<a id="p4-browserrouter"></a>

## 2. BrowserRouter Setup

**Basic Setup:**
```jsx
// main.jsx — root level-এ BrowserRouter
import { StrictMode } from 'react';
import { createRoot } from 'react-dom/client';
import { BrowserRouter } from 'react-router-dom';
import App from './App';

createRoot(document.getElementById('root')).render(
  <StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </StrictMode>
);
```

**Router Types:**

| Router | Use Case | URL |
|---|---|---|
| `BrowserRouter` | Modern apps (recommended) | `/about`, `/users/1` |
| `HashRouter` | Static hosting, no server config | `/#/about`, `/#/users/1` |
| `MemoryRouter` | Testing, non-browser (React Native) | No URL change |
| `createBrowserRouter` | New v6.4+ data API | Same as Browser |

```jsx
// Alternative — createBrowserRouter (v6.4+, recommended for new projects)
import { createBrowserRouter, RouterProvider } from 'react-router-dom';

const router = createBrowserRouter([
  {
    path: '/',
    element: <RootLayout />,
    errorElement: <ErrorPage />,
    children: [
      { index: true, element: <HomePage /> },
      { path: 'about', element: <AboutPage /> },
      {
        path: 'products',
        element: <ProductsPage />,
        children: [
          { path: ':id', element: <ProductDetail /> },
        ],
      },
    ],
  },
]);

// main.jsx
<RouterProvider router={router} />
```

---

<a id="p4-routes"></a>

## 3. Routes & Route

**Basic Route Setup:**
```jsx
// App.jsx
import { Routes, Route } from 'react-router-dom';
import HomePage from './pages/HomePage';
import AboutPage from './pages/AboutPage';
import ProductsPage from './pages/ProductsPage';
import ProductDetail from './pages/ProductDetail';
import NotFoundPage from './pages/NotFoundPage';
import DashboardPage from './pages/DashboardPage';

function App() {
  return (
    <div>
      <Navbar />
      <Routes>
        {/* Exact match — "/" */}
        <Route path="/" element={<HomePage />} />

        {/* Static routes */}
        <Route path="/about" element={<AboutPage />} />
        <Route path="/contact" element={<ContactPage />} />

        {/* Dynamic route */}
        <Route path="/products" element={<ProductsPage />} />
        <Route path="/products/:id" element={<ProductDetail />} />

        {/* Index route */}
        <Route path="/dashboard" element={<DashboardLayout />}>
          <Route index element={<DashboardHome />} />
          <Route path="profile" element={<ProfilePage />} />
          <Route path="settings" element={<SettingsPage />} />
        </Route>

        {/* 404 — catch all */}
        <Route path="*" element={<NotFoundPage />} />
      </Routes>
      <Footer />
    </div>
  );
}
```

**Route Matching Rules (v6):**
```
"/" → only exact "/"
"/products" → exact "/products"
"/products/:id" → "/products/123", "/products/abc"
"/products/*" → "/products/any/path/here"
"*" → matches everything (404 page)
```

---

<a id="p4-params"></a>

## 4. Route Parameters

**URL Parameters — `useParams`:**
```jsx
// Route definition
<Route path="/products/:productId" element={<ProductDetail />} />
<Route path="/users/:userId/orders/:orderId" element={<OrderDetail />} />

// ProductDetail component
import { useParams } from 'react-router-dom';

function ProductDetail() {
  const { productId } = useParams();
  const [product, setProduct] = useState(null);
  const [loading, setLoading] = useState(true);

  useEffect(() => {
    fetch(`/api/products/${productId}`)
      .then(r => r.json())
      .then(data => {
        setProduct(data);
        setLoading(false);
      });
  }, [productId]);  // productId change হলে re-fetch

  if (loading) return <ProductSkeleton />;
  if (!product) return <NotFound />;

  return (
    <div className="product-detail">
      <h1>{product.name}</h1>
      <p>৳{product.price}</p>
      <ProductImages images={product.images} />
      <AddToCartButton productId={productId} />
    </div>
  );
}
```

**Query String Parameters — `useSearchParams`:**
```jsx
import { useSearchParams } from 'react-router-dom';

// URL: /products?category=electronics&sort=price&page=2

function ProductsPage() {
  const [searchParams, setSearchParams] = useSearchParams();

  const category = searchParams.get('category') || 'all';
  const sort = searchParams.get('sort') || 'name';
  const page = parseInt(searchParams.get('page') || '1');

  const updateFilter = (key, value) => {
    setSearchParams(prev => {
      const params = new URLSearchParams(prev);
      params.set(key, value);
      params.set('page', '1');  // reset page on filter change
      return params;
    });
  };

  return (
    <div>
      <select
        value={category}
        onChange={e => updateFilter('category', e.target.value)}
      >
        <option value="all">All</option>
        <option value="electronics">Electronics</option>
        <option value="clothing">Clothing</option>
      </select>

      <select
        value={sort}
        onChange={e => updateFilter('sort', e.target.value)}
      >
        <option value="name">Name</option>
        <option value="price">Price ↑</option>
        <option value="-price">Price ↓</option>
      </select>

      <ProductGrid category={category} sort={sort} page={page} />
      <Pagination
        current={page}
        onPageChange={p => updateFilter('page', p)}
      />
    </div>
  );
}
```

**`useLocation` — Current URL Info:**
```jsx
import { useLocation } from 'react-router-dom';

function BreadCrumb() {
  const location = useLocation();
  // location.pathname = "/products/123"
  // location.search = "?color=red"
  // location.hash = "#reviews"
  // location.state = { from: '/cart' }  (navigate-এ দেওয়া)

  const paths = location.pathname.split('/').filter(Boolean);

  return (
    <nav aria-label="breadcrumb">
      <Link to="/">Home</Link>
      {paths.map((path, i) => (
        <span key={i}>
          {' / '}
          <Link to={`/${paths.slice(0, i + 1).join('/')}`}>
            {path}
          </Link>
        </span>
      ))}
    </nav>
  );
}
```

---

<a id="p4-nested"></a>

## 5. Nested Routing

**Definition:**
Nested routing মানে parent route-এর ভেতরে child routes। Parent layout (navbar, sidebar) same থাকে, শুধু content area change হয়। `<Outlet />` দিয়ে child route render হয়।

**Layout with Nested Routes:**
```jsx
// App.jsx — route structure
function App() {
  return (
    <Routes>
      {/* Public routes */}
      <Route path="/" element={<PublicLayout />}>
        <Route index element={<HomePage />} />
        <Route path="about" element={<AboutPage />} />
        <Route path="products" element={<ProductsPage />} />
        <Route path="products/:id" element={<ProductDetail />} />
      </Route>

      {/* Dashboard routes — different layout */}
      <Route path="/dashboard" element={<DashboardLayout />}>
        <Route index element={<DashboardHome />} />
        <Route path="analytics" element={<AnalyticsPage />} />
        <Route path="products" element={<ManageProducts />} />
        <Route path="products/new" element={<AddProduct />} />
        <Route path="products/:id/edit" element={<EditProduct />} />
        <Route path="orders" element={<OrdersPage />} />
        <Route path="settings" element={<SettingsLayout />}>
          <Route index element={<GeneralSettings />} />
          <Route path="profile" element={<ProfileSettings />} />
          <Route path="security" element={<SecuritySettings />} />
        </Route>
      </Route>

      {/* Auth routes */}
      <Route path="/auth" element={<AuthLayout />}>
        <Route path="login" element={<LoginPage />} />
        <Route path="register" element={<RegisterPage />} />
        <Route path="forgot-password" element={<ForgotPassword />} />
      </Route>

      <Route path="*" element={<NotFoundPage />} />
    </Routes>
  );
}
```

```jsx
// DashboardLayout.jsx — Outlet দিয়ে child render
import { Outlet, NavLink } from 'react-router-dom';

function DashboardLayout() {
  return (
    <div className="dashboard-layout">
      <aside className="sidebar">
        <NavLink to="/dashboard" end className={({ isActive }) =>
          isActive ? 'nav-link active' : 'nav-link'
        }>
          🏠 Overview
        </NavLink>
        <NavLink to="/dashboard/analytics" className={({ isActive }) =>
          isActive ? 'nav-link active' : 'nav-link'
        }>
          📊 Analytics
        </NavLink>
        <NavLink to="/dashboard/products">
          🛍 Products
        </NavLink>
        <NavLink to="/dashboard/orders">
          📦 Orders
        </NavLink>
        <NavLink to="/dashboard/settings">
          ⚙️ Settings
        </NavLink>
      </aside>

      <main className="dashboard-content">
        <Outlet />   {/* Child route এখানে render হবে */}
      </main>
    </div>
  );
}
```

```jsx
// Outlet with context (data pass করা)
function DashboardLayout() {
  const { user } = useAuth();

  return (
    <div>
      <Sidebar />
      <main>
        <Outlet context={{ user, role: user.role }} />
      </main>
    </div>
  );
}

// Child component-এ outlet context পড়া
import { useOutletContext } from 'react-router-dom';

function AnalyticsPage() {
  const { user, role } = useOutletContext();
  return <div>Analytics for {user.name} ({role})</div>;
}
```

**Follow-up Interview Questions:**
1. `<Outlet />` না থাকলে কী হবে?
2. Nested route-এ URL কীভাবে build হয়?
3. `index` route কী?

---

<a id="p4-navigation"></a>

## 6. Navigation

**Link vs NavLink vs useNavigate:**

```jsx
import { Link, NavLink, useNavigate } from 'react-router-dom';

// ──── Link — basic SPA navigation ────
function Navbar() {
  return (
    <nav>
      <Link to="/">Home</Link>
      <Link to="/products">Products</Link>
      <Link to="/about">About</Link>

      {/* Dynamic link */}
      <Link to={`/products/${product.id}`}>{product.name}</Link>

      {/* With state */}
      <Link to="/checkout" state={{ from: '/cart', items: cartItems }}>
        Checkout
      </Link>
    </nav>
  );
}

// ──── NavLink — active styling ────
function Sidebar() {
  return (
    <nav>
      {/* isActive prop দিয়ে styling */}
      <NavLink
        to="/dashboard"
        end  // exact match (এটা না দিলে /dashboard/* সব active হবে)
        className={({ isActive }) =>
          `nav-item ${isActive ? 'nav-item-active' : ''}`
        }
        style={({ isActive }) => ({
          color: isActive ? '#0066cc' : '#333',
          fontWeight: isActive ? 'bold' : 'normal',
        })}
      >
        Dashboard
      </NavLink>

      <NavLink to="/dashboard/analytics" className={({ isActive }) =>
        isActive ? 'active' : ''
      }>
        Analytics
      </NavLink>
    </nav>
  );
}

// ──── useNavigate — programmatic navigation ────
function LoginForm() {
  const navigate = useNavigate();
  const location = useLocation();

  const handleLogin = async (credentials) => {
    await loginAPI(credentials);

    // Navigate after action
    const from = location.state?.from || '/dashboard';
    navigate(from, { replace: true });  // replace: back button-এ login page আসবে না

    // Other navigate examples:
    // navigate('/dashboard');            // push
    // navigate(-1);                      // go back
    // navigate(1);                       // go forward
    // navigate('/login', { replace: true });  // replace history
    // navigate('/order/1', { state: { order } }); // with state
  };

  return <form onSubmit={handleLogin}>...</form>;
}
```

**Link vs `<a>` tag:**

| | `<a href>` | `<Link to>` |
|---|---|---|
| Page reload | ✅ Full reload | ❌ No reload |
| SPA friendly | ❌ | ✅ |
| History API | ❌ | ✅ |
| State pass | ❌ | ✅ |
| Active class | ❌ | ✅ (NavLink) |

**Redirect:**
```jsx
import { Navigate } from 'react-router-dom';

function OldPage() {
  return <Navigate to="/new-page" replace />;
}

// Conditional redirect
function Dashboard() {
  const { isLoggedIn } = useAuth();
  if (!isLoggedIn) {
    return <Navigate to="/login" state={{ from: '/dashboard' }} replace />;
  }
  return <DashboardContent />;
}
```

---

<a id="p4-protected"></a>

## 7. Protected Routes

**Definition:**
Protected (Private) Route হলো এমন route যেখানে শুধু authenticated user প্রবেশ করতে পারে। Unauthorized user-কে login page-এ redirect করা হয়।

**Protected Route Component:**
```jsx
// components/ProtectedRoute.jsx
import { Navigate, useLocation } from 'react-router-dom';
import { useAuth } from '../context/AuthContext';

function ProtectedRoute({ children, requiredRole }) {
  const { isLoggedIn, user } = useAuth();
  const location = useLocation();

  // না logged in → login page-এ পাঠাও, current location মনে রাখো
  if (!isLoggedIn) {
    return (
      <Navigate
        to="/auth/login"
        state={{ from: location.pathname }}  // লগইনের পরে এখানে ফিরতে
        replace
      />
    );
  }

  // Role check
  if (requiredRole && user.role !== requiredRole) {
    return <Navigate to="/unauthorized" replace />;
  }

  return children;
}
```

```jsx
// App.jsx — protected routes use
function App() {
  return (
    <Routes>
      {/* Public routes */}
      <Route path="/" element={<HomePage />} />
      <Route path="/auth/login" element={<LoginPage />} />
      <Route path="/auth/register" element={<RegisterPage />} />
      <Route path="/products" element={<ProductsPage />} />

      {/* Protected — any authenticated user */}
      <Route path="/dashboard" element={
        <ProtectedRoute>
          <DashboardLayout />
        </ProtectedRoute>
      }>
        <Route index element={<DashboardHome />} />
        <Route path="profile" element={<ProfilePage />} />
        <Route path="orders" element={<MyOrders />} />
      </Route>

      {/* Admin only */}
      <Route path="/admin" element={
        <ProtectedRoute requiredRole="admin">
          <AdminLayout />
        </ProtectedRoute>
      }>
        <Route index element={<AdminDashboard />} />
        <Route path="users" element={<UserManagement />} />
        <Route path="settings" element={<AdminSettings />} />
      </Route>
    </Routes>
  );
}
```

**Return to Original Page After Login:**
```jsx
// Login page — state থেকে "from" পড়ে
function LoginPage() {
  const navigate = useNavigate();
  const location = useLocation();
  const { login } = useAuth();

  const from = location.state?.from || '/dashboard';

  const handleSubmit = async (credentials) => {
    await login(credentials);
    navigate(from, { replace: true });
    // User যেখান থেকে এসেছিল, সেখানে ফিরে যাবে
  };

  return <LoginForm onSubmit={handleSubmit} />;
}
```

**Role-based Protected Route:**
```jsx
// Multiple role support
function ProtectedRoute({ children, roles = [] }) {
  const { user, isLoggedIn } = useAuth();
  const location = useLocation();

  if (!isLoggedIn) {
    return <Navigate to="/auth/login" state={{ from: location.pathname }} replace />;
  }

  if (roles.length > 0 && !roles.includes(user.role)) {
    return <Navigate to="/403" replace />;
  }

  return children;
}

// Usage
<Route path="/reports" element={
  <ProtectedRoute roles={['admin', 'manager']}>
    <ReportsPage />
  </ProtectedRoute>
} />

<Route path="/admin/users" element={
  <ProtectedRoute roles={['admin']}>
    <UserManagementPage />
  </ProtectedRoute>
} />
```

**Interview-style Explanation:**
> "Protected route একটি wrapper component যা check করে user logged in কিনা। না থাকলে `<Navigate>` দিয়ে login page-এ redirect করি — `state={{ from: location.pathname }}` দিয়ে current URL মনে রাখি। Login সফল হলে user সেই original page-এ ফিরে যায়।"

---

<a id="p4-lazy"></a>

## 8. Lazy Loading Routes

**Definition:**
Lazy loading মানে route-এর component initial bundle-এ না রেখে, যখন সেই route-এ যাওয়া হয় তখন load করা। `React.lazy()` আর `Suspense` ব্যবহার করা হয়। Initial bundle size কমে, app faster হয়।

**কেন Lazy Load:**
```
Without lazy loading:
App.js bundle = Home + Dashboard + Admin + Settings + Chart + ...
= 2MB initial download 😱

With lazy loading:
Initial bundle = Home only = 200KB ✅
Dashboard load করলে → Dashboard chunk download (300KB)
Admin load করলে → Admin chunk download (400KB)
```

**Implementation:**
```jsx
import { Suspense, lazy } from 'react';
import { Routes, Route } from 'react-router-dom';

// ✅ Lazy imports — function must return dynamic import
const HomePage = lazy(() => import('./pages/HomePage'));
const AboutPage = lazy(() => import('./pages/AboutPage'));
const DashboardPage = lazy(() => import('./pages/Dashboard'));
const ProductsPage = lazy(() => import('./pages/Products'));
const AdminPage = lazy(() => import('./pages/Admin'));

// Loading fallback component
function PageLoader() {
  return (
    <div className="page-loader">
      <div className="spinner-large" />
      <p>Loading...</p>
    </div>
  );
}

function App() {
  return (
    // Suspense — lazy component load হওয়া পর্যন্ত fallback দেখায়
    <Suspense fallback={<PageLoader />}>
      <Routes>
        <Route path="/" element={<HomePage />} />
        <Route path="/about" element={<AboutPage />} />
        <Route path="/dashboard/*" element={
          <ProtectedRoute>
            <DashboardPage />
          </ProtectedRoute>
        } />
        <Route path="/products/*" element={<ProductsPage />} />
        <Route path="/admin/*" element={
          <ProtectedRoute requiredRole="admin">
            <AdminPage />
          </ProtectedRoute>
        } />
      </Routes>
    </Suspense>
  );
}
```

**Multiple Suspense Boundaries:**
```jsx
// Per-section fallback — granular control
function App() {
  return (
    <Routes>
      <Route path="/" element={
        <Suspense fallback={<HomePageSkeleton />}>
          <HomePage />
        </Suspense>
      } />

      <Route path="/dashboard" element={
        <ProtectedRoute>
          <Suspense fallback={<DashboardSkeleton />}>
            <Dashboard />
          </Suspense>
        </ProtectedRoute>
      } />
    </Routes>
  );
}
```

**Preloading (Performance optimization):**
```jsx
// Hover করলেই preload শুরু — navigation-এ faster
const DashboardPage = lazy(() => import('./pages/Dashboard'));

function Navbar() {
  const handleMouseEnter = () => {
    // Prefetch — hover করলেই background-এ load শুরু
    import('./pages/Dashboard');
  };

  return (
    <Link
      to="/dashboard"
      onMouseEnter={handleMouseEnter}
    >
      Dashboard
    </Link>
  );
}
```

---

<a id="p4-dynamic"></a>

## 9. Dynamic Routing

**Definition:**
Dynamic routing মানে route structure runtime-এ data দিয়ে তৈরি হয়। Hardcoded routes-এর বদলে config বা API data থেকে routes generate করা।

**Data-driven Routes:**
```jsx
// Config-based routing
const routes = [
  { path: '/', component: HomePage, exact: true },
  { path: '/about', component: AboutPage },
  { path: '/products', component: ProductsPage },
  { path: '/products/:id', component: ProductDetail },
  { path: '/dashboard', component: DashboardPage, protected: true },
  { path: '/admin', component: AdminPage, protected: true, role: 'admin' },
];

function AppRouter() {
  return (
    <Routes>
      {routes.map(({ path, component: Component, protected: isProtected, role }) => (
        <Route
          key={path}
          path={path}
          element={
            isProtected
              ? <ProtectedRoute requiredRole={role}><Component /></ProtectedRoute>
              : <Component />
          }
        />
      ))}
      <Route path="*" element={<NotFound />} />
    </Routes>
  );
}
```

**Role-based Dynamic Menu + Routes:**
```jsx
const menuConfig = {
  admin: [
    { label: 'Dashboard', path: '/admin/dashboard', icon: '🏠', component: AdminDashboard },
    { label: 'Users', path: '/admin/users', icon: '👥', component: UserManagement },
    { label: 'Products', path: '/admin/products', icon: '🛍', component: ProductManagement },
    { label: 'Reports', path: '/admin/reports', icon: '📊', component: Reports },
    { label: 'Settings', path: '/admin/settings', icon: '⚙️', component: Settings },
  ],
  manager: [
    { label: 'Dashboard', path: '/dashboard', icon: '🏠', component: ManagerDashboard },
    { label: 'Products', path: '/dashboard/products', icon: '🛍', component: ProductManagement },
    { label: 'Reports', path: '/dashboard/reports', icon: '📊', component: Reports },
  ],
  user: [
    { label: 'Home', path: '/home', icon: '🏠', component: UserHome },
    { label: 'Orders', path: '/orders', icon: '📦', component: MyOrders },
    { label: 'Profile', path: '/profile', icon: '👤', component: Profile },
  ],
};

function DynamicSidebar() {
  const { user } = useAuth();
  const items = menuConfig[user.role] || menuConfig.user;

  return (
    <aside>
      {items.map(item => (
        <NavLink key={item.path} to={item.path} className={({ isActive }) =>
          `menu-item ${isActive ? 'active' : ''}`
        }>
          {item.icon} {item.label}
        </NavLink>
      ))}
    </aside>
  );
}

function DynamicRoutes() {
  const { user } = useAuth();
  const items = menuConfig[user.role] || menuConfig.user;

  return (
    <Routes>
      {items.map(({ path, component: Component }) => (
        <Route key={path} path={path} element={<Component />} />
      ))}
    </Routes>
  );
}
```

---

<a id="p4-flow"></a>

## 10. SPA Navigation Flow — Complete Picture

**Full Authentication Flow:**
```
User visits /dashboard (not logged in)
    ↓
ProtectedRoute checks: isLoggedIn = false
    ↓
<Navigate to="/auth/login" state={{ from: '/dashboard' }} />
    ↓
LoginPage renders — shows login form
    ↓
User submits credentials
    ↓
API call — success → token stored
    ↓
AuthContext: setUser(), setToken()
    ↓
navigate(from) → navigate('/dashboard')
    ↓
ProtectedRoute checks: isLoggedIn = true ✅
    ↓
DashboardLayout renders with <Outlet />
    ↓
DashboardHome renders inside Outlet
```

**Complete App Routing Example:**
```jsx
// Full production-like routing setup
function App() {
  return (
    <AuthProvider>
      <BrowserRouter>
        <Suspense fallback={<FullPageLoader />}>
          <Routes>
            {/* Public layout */}
            <Route element={<PublicLayout />}>
              <Route path="/" element={<HomePage />} />
              <Route path="/products" element={<ProductsPage />} />
              <Route path="/products/:id" element={<ProductDetail />} />
              <Route path="/about" element={<AboutPage />} />
            </Route>

            {/* Auth pages — no layout */}
            <Route path="/auth/login" element={<LoginPage />} />
            <Route path="/auth/register" element={<RegisterPage />} />
            <Route path="/auth/forgot-password" element={<ForgotPassword />} />

            {/* Protected user dashboard */}
            <Route path="/dashboard" element={
              <ProtectedRoute>
                <DashboardLayout />
              </ProtectedRoute>
            }>
              <Route index element={<DashboardHome />} />
              <Route path="orders" element={<OrdersPage />} />
              <Route path="orders/:id" element={<OrderDetail />} />
              <Route path="profile" element={<ProfilePage />} />
              <Route path="settings" element={<SettingsPage />} />
            </Route>

            {/* Admin panel */}
            <Route path="/admin" element={
              <ProtectedRoute roles={['admin']}>
                <AdminLayout />
              </ProtectedRoute>
            }>
              <Route index element={<AdminDashboard />} />
              <Route path="users" element={<UsersManagement />} />
              <Route path="users/:id" element={<UserDetail />} />
              <Route path="products" element={<ProductsManagement />} />
              <Route path="analytics" element={<Analytics />} />
            </Route>

            {/* Error pages */}
            <Route path="/403" element={<UnauthorizedPage />} />
            <Route path="*" element={<NotFoundPage />} />
          </Routes>
        </Suspense>
      </BrowserRouter>
    </AuthProvider>
  );
}
```

**Routing Hooks Summary:**
```jsx
// useNavigate — programmatic navigation
const navigate = useNavigate();
navigate('/home');
navigate(-1);
navigate('/login', { replace: true, state: { from: '/dashboard' } });

// useParams — URL params
const { id, category } = useParams();

// useLocation — current URL info
const { pathname, search, hash, state } = useLocation();

// useSearchParams — query string
const [params, setParams] = useSearchParams();
const page = params.get('page');

// useOutletContext — data from parent Outlet
const { user } = useOutletContext();
```

---

## PART 4 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Say |
|---|---|---|
| React Router | Client-side routing, URL↔Component mapping | No server request on navigation |
| BrowserRouter | HTML5 History API | Wrap app at root level |
| Routes/Route | URL pattern matching | `path="*"` for 404 |
| useParams | Dynamic URL segments | `const { id } = useParams()` |
| useSearchParams | Query string management | `params.get('key')` |
| Nested Routes | `<Outlet />` for child render | Layout + child pattern |
| Link/NavLink | SPA link, no reload | NavLink has `isActive` |
| useNavigate | Programmatic navigation | `navigate(-1)` for back |
| Protected Route | Auth check wrapper | Redirect + `state={{ from }}` |
| Lazy Loading | `React.lazy` + `Suspense` | Smaller initial bundle |
| Dynamic Routing | Config/data-driven routes | Role-based menu |

---

## PART 3 & 4 Common Interview Questions

**PART 3 — Architecture:**
1. Component composition কী? উদাহরণ দিন।
2. HOC কী? Custom Hooks-এর সাথে পার্থক্য?
3. Controlled vs Uncontrolled component — কখন কোনটি?
4. Lifting state up কেন দরকার?
5. Compound components pattern কী?

**PART 4 — Routing:**
1. React Router-এ `BrowserRouter` কী করে?
2. `<Link>` আর `<a>` পার্থক্য?
3. Protected route কীভাবে implement করবেন?
4. Nested routing-এ `<Outlet>` কী করে?
5. Lazy loading routes কেন দরকার?
6. `useNavigate` আর `<Navigate>` পার্থক্য?
7. URL parameter আর query string পার্থক্য?

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 5 — State Management *(Next request এ লিখব)*
