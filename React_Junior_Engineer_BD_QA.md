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
| PART 3 | Component Architecture | ✅ |
| PART 4 | Routing & Navigation | ✅ |
| PART 5 | State Management | ✅ |
| PART 6 | API Integration & Async | ✅ |
| PART 7 | Performance Optimization | ✅ |
| PART 8 | Advanced React | ✅ |
| PART 9 | Backend & Authentication | ✅ |
| PART 10 | React Projects | ✅ |
| PART 11 | Interview Questions Bank | ✅ |
| PART 12 | Next.js Basics | ✅ |
| PART 13 | Testing & Best Practices | ✅ |
| PART 14 | BD Interview Preparation | ✅ |

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

<a id="part5"></a>

## 📋 PART 5 সূচিপত্র — State Management

| # | Topic | Key Concept |
|---|---|---|
| 1 | [State Management Overview](#p5-overview) | কেন দরকার, options |
| 2 | [Local vs Global State](#p5-local-global) | কোনটা কোথায় |
| 3 | [Context API — Advanced](#p5-context-adv) | Multiple context, performance |
| 4 | [Redux Toolkit — Basics](#p5-redux-basics) | Store, Slice, Dispatch |
| 5 | [Redux Toolkit — Async (Thunk)](#p5-redux-thunk) | createAsyncThunk, loading states |
| 6 | [Redux Toolkit — Full Example](#p5-redux-example) | E-commerce cart complete |
| 7 | [Zustand](#p5-zustand) | Lightweight, simple |
| 8 | [Redux vs Context vs Zustand](#p5-comparison) | Decision guide |
| 9 | [Immer & Immutability](#p5-immer) | Why immutable, Immer under hood |
| 10 | [State Management Patterns](#p5-patterns) | Normalized state, selectors |

---

<a id="p5-overview"></a>

## 1. State Management Overview

**Definition:**
State management মানে application-এর data কোথায় রাখবো, কীভাবে update করবো, এবং কোন component access করতে পারবে — তা নির্ধারণ করা। Complex app-এ multiple components same data use করলে centralized state management দরকার।

**কেন State Management Library দরকার:**
```
ছোট App:
  useState + Context → যথেষ্ট

Medium App:
  Context বা Zustand → ভালো choice

Large App (e-commerce, dashboard):
  Redux Toolkit → predictable, scalable, DevTools
```

**State-এর ধরন:**

| ধরন | উদাহরণ | কোথায় রাখবো |
|---|---|---|
| Local UI state | Modal open/close, form input | `useState` |
| Shared UI state | Selected tab, active filter | Lifted state / Context |
| Server/remote state | API data, products list | React Query / SWR |
| Global app state | Auth user, cart, theme | Context / Redux / Zustand |
| URL state | Filters, pagination, active tab | React Router / `useSearchParams` |

**State Management Options:**

| Library | Bundle size | Learning curve | Best for |
|---|---|---|---|
| useState + useReducer | 0 (built-in) | Easy | Component-level |
| Context API | 0 (built-in) | Easy | Theme, Auth |
| Zustand | ~1KB | Very easy | Small-medium apps |
| Jotai | ~3KB | Easy | Atomic state |
| Redux Toolkit | ~11KB | Medium | Large enterprise apps |
| Recoil | ~21KB | Medium | Atomic, Facebook-style |

**Interview-style Explanation:**
> "State management-এর choice app-এর size আর complexity-র উপর নির্ভর করে। Simple app-এ `useState` আর Context যথেষ্ট। Large app-এ — অনেক async action, DevTools দরকার, team বড় — Redux Toolkit best। Performance-critical আর simple API চাই — Zustand। Server state separately React Query দিয়ে manage করি।"

---

<a id="p5-local-global"></a>

## 2. Local vs Global State

**Definition:**
**Local state** শুধু একটি component-এর নিজের — অন্য কেউ দরকার নেই। **Global state** multiple unrelated components share করে।

**কোনটি কোথায় রাখবো:**
```jsx
// ✅ LOCAL STATE — শুধু এই component-এর দরকার
function SearchInput() {
  const [query, setQuery] = useState('');  // Only this component needs it
  return <input value={query} onChange={e => setQuery(e.target.value)} />;
}

// ✅ LOCAL STATE — form state, modal open/close
function ProductCard({ product }) {
  const [isWishlisted, setIsWishlisted] = useState(false);
  const [showDetails, setShowDetails] = useState(false);
  // ...
}

// ✅ GLOBAL STATE — multiple far-apart components need it
// Cart count: Navbar badge + Cart page + Checkout page
// Auth user: Header + Profile + Protected Routes + API calls
// Theme: Every component's styling
```

**Rule of Thumb:**
```
Ask: "কতজন component এই data দরকার?"

  শুধু ১টি → useState (local)
  Parent + Child → Lifted state (props)
  ৩-৪টি nearby → Context
  অনেকগুলো, app-wide → Redux / Zustand
```

**State Colocation Principle:**
```jsx
// ✅ GOOD — state যেখানে দরকার সেখানেই রাখো
// Counter শুধু CounterWidget-এর দরকার → locally রাখো
function CounterWidget() {
  const [count, setCount] = useState(0);  // not global!
  return (
    <div>
      <button onClick={() => setCount(c => c - 1)}>-</button>
      <span>{count}</span>
      <button onClick={() => setCount(c => c + 1)}>+</button>
    </div>
  );
}

// ❌ BAD — not everything should be global
// Redux-এ modal open/close state রাখা over-engineering
const modalSlice = createSlice({
  name: 'modal',
  initialState: { isProductDetailOpen: false },  // ❌ Unnecessary global
  // ...
});
```

---

<a id="p5-context-adv"></a>

## 3. Context API — Advanced

**Multiple Contexts:**
```jsx
// ✅ Separate contexts for separate concerns
// ThemeContext, AuthContext, CartContext — আলাদা করুন

// context/CartContext.jsx
import { createContext, useContext, useReducer, useMemo } from 'react';

const CartContext = createContext(null);

function cartReducer(state, action) {
  switch (action.type) {
    case 'ADD': {
      const exists = state.items.find(i => i.id === action.payload.id);
      if (exists) {
        return {
          ...state,
          items: state.items.map(i =>
            i.id === action.payload.id
              ? { ...i, qty: i.qty + 1 }
              : i
          ),
        };
      }
      return { ...state, items: [...state.items, { ...action.payload, qty: 1 }] };
    }
    case 'REMOVE':
      return { ...state, items: state.items.filter(i => i.id !== action.payload) };
    case 'UPDATE_QTY':
      return {
        ...state,
        items: state.items.map(i =>
          i.id === action.payload.id
            ? { ...i, qty: Math.max(1, action.payload.qty) }
            : i
        ),
      };
    case 'CLEAR':
      return { items: [] };
    default:
      return state;
  }
}

export function CartProvider({ children }) {
  const [cart, dispatch] = useReducer(cartReducer, { items: [] });

  // ✅ Memoize derived values
  const cartTotal = useMemo(
    () => cart.items.reduce((sum, item) => sum + item.price * item.qty, 0),
    [cart.items]
  );
  const cartCount = useMemo(
    () => cart.items.reduce((sum, item) => sum + item.qty, 0),
    [cart.items]
  );

  // ✅ Memoize actions — stable references
  const actions = useMemo(() => ({
    addToCart: (product) => dispatch({ type: 'ADD', payload: product }),
    removeFromCart: (id) => dispatch({ type: 'REMOVE', payload: id }),
    updateQty: (id, qty) => dispatch({ type: 'UPDATE_QTY', payload: { id, qty } }),
    clearCart: () => dispatch({ type: 'CLEAR' }),
  }), []);

  // ✅ Split state + actions to avoid unnecessary re-renders
  const value = useMemo(() => ({
    items: cart.items,
    total: cartTotal,
    count: cartCount,
    ...actions,
  }), [cart.items, cartTotal, cartCount, actions]);

  return <CartContext.Provider value={value}>{children}</CartContext.Provider>;
}

export const useCart = () => {
  const ctx = useContext(CartContext);
  if (!ctx) throw new Error('useCart must be used within CartProvider');
  return ctx;
};
```

**Context Performance — Split Pattern:**
```jsx
// ❌ One big context — any state change re-renders ALL consumers
const AppContext = createContext(null);

function AppProvider({ children }) {
  const [user, setUser] = useState(null);
  const [cart, setCart] = useState([]);
  const [theme, setTheme] = useState('light');
  const [notifications, setNotifications] = useState([]);

  // cart change হলে user, theme, notifications সব consumer re-render হবে!
  return (
    <AppContext.Provider value={{ user, cart, theme, notifications, ... }}>
      {children}
    </AppContext.Provider>
  );
}

// ✅ Split into separate contexts
function AppProvider({ children }) {
  return (
    <AuthProvider>
      <ThemeProvider>
        <CartProvider>
          <NotificationProvider>
            {children}
          </NotificationProvider>
        </CartProvider>
      </ThemeProvider>
    </AuthProvider>
  );
}

// Avatar only uses AuthContext → cart change-এ re-render হবে না
function Avatar() {
  const { user } = useAuth();  // Only AuthContext consumer
  return <img src={user.avatar} />;
}

// CartBadge only uses CartContext → auth change-এ re-render হবে না
function CartBadge() {
  const { count } = useCart();  // Only CartContext consumer
  return <span className="badge">{count}</span>;
}
```

**Follow-up Interview Questions:**
1. Context re-render সমস্যা কীভাবে solve করবেন?
2. `useMemo` context value-এ কেন দরকার?
3. Context-এ selector pattern কীভাবে করবেন?

---

<a id="p5-redux-basics"></a>

## 4. Redux Toolkit — Basics

**Definition:**
Redux Toolkit (RTK) হলো Redux-এর official, opinionated toolset যা boilerplate কমায়। `createSlice`, `configureStore`, `createAsyncThunk` দিয়ে Redux much simpler হয়।

**Core Concepts:**

| Concept | কী | Analogy |
|---|---|---|
| Store | Global state container | Central database |
| Slice | একটি feature-এর state + reducers | Database table |
| Action | State change request object | Database query |
| Reducer | Action → new state (pure fn) | Query handler |
| Dispatch | Action পাঠানোর mechanism | Query execute |
| Selector | State থেকে data read করা | SELECT query |

**Installation:**
```bash
npm install @reduxjs/toolkit react-redux
```

**Basic Setup:**
```jsx
// store/authSlice.js
import { createSlice } from '@reduxjs/toolkit';

const authSlice = createSlice({
  name: 'auth',
  initialState: {
    user: null,
    token: localStorage.getItem('token') || null,
    isLoggedIn: !!localStorage.getItem('token'),
  },
  reducers: {
    // RTK Immer দিয়ে direct mutation allow করে (internally immutable)
    setUser: (state, action) => {
      state.user = action.payload;
      state.isLoggedIn = true;
    },
    setToken: (state, action) => {
      state.token = action.payload;
      localStorage.setItem('token', action.payload);
    },
    logout: (state) => {
      state.user = null;
      state.token = null;
      state.isLoggedIn = false;
      localStorage.removeItem('token');
    },
  },
});

export const { setUser, setToken, logout } = authSlice.actions;

// Selectors
export const selectUser = (state) => state.auth.user;
export const selectIsLoggedIn = (state) => state.auth.isLoggedIn;
export const selectToken = (state) => state.auth.token;

export default authSlice.reducer;
```

```jsx
// store/index.js
import { configureStore } from '@reduxjs/toolkit';
import authReducer from './authSlice';
import cartReducer from './cartSlice';
import productsReducer from './productsSlice';

export const store = configureStore({
  reducer: {
    auth: authReducer,
    cart: cartReducer,
    products: productsReducer,
  },
  // DevTools automatically enabled in development
  // Middleware: thunk automatically added
});

export type RootState = ReturnType<typeof store.getState>;
export type AppDispatch = typeof store.dispatch;
```

```jsx
// main.jsx — Provider wrap
import { Provider } from 'react-redux';
import { store } from './store';

createRoot(document.getElementById('root')).render(
  <Provider store={store}>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </Provider>
);
```

**Using Redux in Components:**
```jsx
import { useSelector, useDispatch } from 'react-redux';
import { logout, selectUser, selectIsLoggedIn } from '../store/authSlice';

function Header() {
  const user = useSelector(selectUser);          // state read
  const isLoggedIn = useSelector(selectIsLoggedIn);
  const dispatch = useDispatch();                // action dispatch

  const handleLogout = () => {
    dispatch(logout());  // action dispatch করো
  };

  return (
    <header>
      {isLoggedIn ? (
        <>
          <span>Hello, {user.name}!</span>
          <button onClick={handleLogout}>Logout</button>
        </>
      ) : (
        <Link to="/login">Login</Link>
      )}
    </header>
  );
}
```

---

<a id="p5-redux-thunk"></a>

## 5. Redux Toolkit — Async (createAsyncThunk)

**Definition:**
`createAsyncThunk` দিয়ে async operations (API calls) Redux-এ handle করা হয়। Automatically `pending`, `fulfilled`, `rejected` states তৈরি করে।

**createAsyncThunk — Pattern:**
```jsx
// store/productsSlice.js
import { createSlice, createAsyncThunk } from '@reduxjs/toolkit';

// Async thunk — API call
export const fetchProducts = createAsyncThunk(
  'products/fetchAll',         // action type prefix
  async (params = {}, { rejectWithValue }) => {
    try {
      const query = new URLSearchParams(params).toString();
      const res = await fetch(`/api/products?${query}`);
      if (!res.ok) throw new Error(`HTTP ${res.status}`);
      return await res.json();                   // returned value → action.payload
    } catch (err) {
      return rejectWithValue(err.message);       // error → rejected payload
    }
  }
);

export const fetchProductById = createAsyncThunk(
  'products/fetchById',
  async (id, { rejectWithValue }) => {
    try {
      const res = await fetch(`/api/products/${id}`);
      if (!res.ok) throw new Error('Product not found');
      return await res.json();
    } catch (err) {
      return rejectWithValue(err.message);
    }
  }
);

export const createProduct = createAsyncThunk(
  'products/create',
  async (productData, { rejectWithValue, getState }) => {
    try {
      const { auth } = getState();         // other slice state পড়া
      const res = await fetch('/api/products', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          'Authorization': `Bearer ${auth.token}`,
        },
        body: JSON.stringify(productData),
      });
      if (!res.ok) throw new Error('Failed to create');
      return await res.json();
    } catch (err) {
      return rejectWithValue(err.message);
    }
  }
);

// Slice with extraReducers for async actions
const productsSlice = createSlice({
  name: 'products',
  initialState: {
    items: [],
    selectedProduct: null,
    loading: false,
    error: null,
    total: 0,
    page: 1,
  },
  reducers: {
    clearError: (state) => { state.error = null; },
    setPage: (state, action) => { state.page = action.payload; },
    clearSelected: (state) => { state.selectedProduct = null; },
  },
  extraReducers: (builder) => {
    // fetchProducts
    builder
      .addCase(fetchProducts.pending, (state) => {
        state.loading = true;
        state.error = null;
      })
      .addCase(fetchProducts.fulfilled, (state, action) => {
        state.loading = false;
        state.items = action.payload.data;
        state.total = action.payload.total;
      })
      .addCase(fetchProducts.rejected, (state, action) => {
        state.loading = false;
        state.error = action.payload;
      });

    // fetchProductById
    builder
      .addCase(fetchProductById.pending, (state) => {
        state.loading = true;
      })
      .addCase(fetchProductById.fulfilled, (state, action) => {
        state.loading = false;
        state.selectedProduct = action.payload;
      })
      .addCase(fetchProductById.rejected, (state, action) => {
        state.loading = false;
        state.error = action.payload;
      });

    // createProduct
    builder
      .addCase(createProduct.fulfilled, (state, action) => {
        state.items.unshift(action.payload);  // list-এর শুরুতে যোগ
      });
  },
});

export const { clearError, setPage, clearSelected } = productsSlice.actions;

// Selectors
export const selectProducts = (state) => state.products.items;
export const selectProductsLoading = (state) => state.products.loading;
export const selectProductsError = (state) => state.products.error;
export const selectSelectedProduct = (state) => state.products.selectedProduct;

export default productsSlice.reducer;
```

**Using Async Thunk in Component:**
```jsx
import { useEffect } from 'react';
import { useSelector, useDispatch } from 'react-redux';
import {
  fetchProducts,
  selectProducts,
  selectProductsLoading,
  selectProductsError,
} from '../store/productsSlice';

function ProductsPage() {
  const dispatch = useDispatch();
  const products = useSelector(selectProducts);
  const loading = useSelector(selectProductsLoading);
  const error = useSelector(selectProductsError);

  useEffect(() => {
    dispatch(fetchProducts({ category: 'electronics', page: 1 }));
  }, [dispatch]);

  if (loading) return <ProductGridSkeleton />;
  if (error) return <ErrorBanner message={error} />;

  return (
    <div className="product-grid">
      {products.map(p => <ProductCard key={p.id} product={p} />)}
    </div>
  );
}
```

---

<a id="p5-redux-example"></a>

## 6. Redux Toolkit — Full Cart Example

**Complete Cart Slice:**
```jsx
// store/cartSlice.js
import { createSlice } from '@reduxjs/toolkit';

const cartSlice = createSlice({
  name: 'cart',
  initialState: {
    items: [],
    isOpen: false,
    couponCode: null,
    discount: 0,
  },
  reducers: {
    addItem: (state, action) => {
      const existing = state.items.find(i => i.id === action.payload.id);
      if (existing) {
        existing.qty += 1;  // Immer: direct mutation OK inside RTK
      } else {
        state.items.push({ ...action.payload, qty: 1 });
      }
    },
    removeItem: (state, action) => {
      state.items = state.items.filter(i => i.id !== action.payload);
    },
    updateQty: (state, action) => {
      const item = state.items.find(i => i.id === action.payload.id);
      if (item) {
        item.qty = Math.max(1, action.payload.qty);
      }
    },
    clearCart: (state) => {
      state.items = [];
      state.couponCode = null;
      state.discount = 0;
    },
    toggleCart: (state) => {
      state.isOpen = !state.isOpen;
    },
    applyCoupon: (state, action) => {
      state.couponCode = action.payload.code;
      state.discount = action.payload.discount;
    },
  },
});

export const {
  addItem, removeItem, updateQty,
  clearCart, toggleCart, applyCoupon,
} = cartSlice.actions;

// Memoized selectors (reselect-style)
export const selectCartItems = (state) => state.cart.items;
export const selectCartIsOpen = (state) => state.cart.isOpen;
export const selectCartCount = (state) =>
  state.cart.items.reduce((sum, i) => sum + i.qty, 0);
export const selectCartSubtotal = (state) =>
  state.cart.items.reduce((sum, i) => sum + i.price * i.qty, 0);
export const selectCartTotal = (state) => {
  const subtotal = selectCartSubtotal(state);
  return subtotal - (subtotal * state.cart.discount / 100);
};

export default cartSlice.reducer;
```

**Cart Components:**
```jsx
// CartIcon — Navbar-এ
function CartIcon() {
  const dispatch = useDispatch();
  const count = useSelector(selectCartCount);

  return (
    <button onClick={() => dispatch(toggleCart())} className="cart-icon">
      🛒
      {count > 0 && <span className="badge">{count}</span>}
    </button>
  );
}

// Add to Cart button
function AddToCartButton({ product }) {
  const dispatch = useDispatch();
  const items = useSelector(selectCartItems);
  const isInCart = items.some(i => i.id === product.id);

  return (
    <button
      onClick={() => dispatch(addItem(product))}
      className={`btn ${isInCart ? 'btn-secondary' : 'btn-primary'}`}
    >
      {isInCart ? '✓ Added' : 'Add to Cart'}
    </button>
  );
}

// Cart Drawer
function CartDrawer() {
  const dispatch = useDispatch();
  const isOpen = useSelector(selectCartIsOpen);
  const items = useSelector(selectCartItems);
  const subtotal = useSelector(selectCartSubtotal);
  const total = useSelector(selectCartTotal);

  if (!isOpen) return null;

  return (
    <div className="cart-overlay" onClick={() => dispatch(toggleCart())}>
      <div className="cart-drawer" onClick={e => e.stopPropagation()}>
        <div className="cart-header">
          <h2>Shopping Cart ({items.length})</h2>
          <button onClick={() => dispatch(toggleCart())}>×</button>
        </div>

        <div className="cart-items">
          {items.length === 0
            ? <p className="empty-cart">Your cart is empty</p>
            : items.map(item => (
              <CartItem key={item.id} item={item} />
            ))
          }
        </div>

        {items.length > 0 && (
          <div className="cart-footer">
            <div className="subtotal">
              <span>Subtotal:</span>
              <span>৳{subtotal.toLocaleString()}</span>
            </div>
            <div className="total">
              <strong>Total: ৳{total.toLocaleString()}</strong>
            </div>
            <button
              onClick={() => dispatch(clearCart())}
              className="btn btn-ghost btn-sm"
            >
              Clear Cart
            </button>
            <Link to="/checkout" className="btn btn-primary btn-full">
              Checkout
            </Link>
          </div>
        )}
      </div>
    </div>
  );
}

function CartItem({ item }) {
  const dispatch = useDispatch();

  return (
    <div className="cart-item">
      <img src={item.image} alt={item.name} />
      <div className="item-info">
        <p>{item.name}</p>
        <p>৳{item.price.toLocaleString()}</p>
      </div>
      <div className="item-controls">
        <button onClick={() => dispatch(updateQty({ id: item.id, qty: item.qty - 1 }))}>-</button>
        <span>{item.qty}</span>
        <button onClick={() => dispatch(updateQty({ id: item.id, qty: item.qty + 1 }))}>+</button>
        <button onClick={() => dispatch(removeItem(item.id))}>🗑</button>
      </div>
    </div>
  );
}
```

---

<a id="p5-zustand"></a>

## 7. Zustand

**Definition:**
Zustand হলো lightweight (~1KB) state management library যা React-এর বাইরেও কাজ করে। Minimal boilerplate, no Provider wrap দরকার (optional), simple API।

**Installation:**
```bash
npm install zustand
```

**Basic Store:**
```jsx
// store/useCartStore.js
import { create } from 'zustand';
import { persist, devtools } from 'zustand/middleware';

const useCartStore = create(
  devtools(  // Redux DevTools support
    persist(  // localStorage persist
      (set, get) => ({
        // State
        items: [],
        isOpen: false,

        // Actions (no slice, no dispatch — direct!)
        addItem: (product) => set((state) => {
          const existing = state.items.find(i => i.id === product.id);
          if (existing) {
            return {
              items: state.items.map(i =>
                i.id === product.id ? { ...i, qty: i.qty + 1 } : i
              ),
            };
          }
          return { items: [...state.items, { ...product, qty: 1 }] };
        }),

        removeItem: (id) => set((state) => ({
          items: state.items.filter(i => i.id !== id),
        })),

        updateQty: (id, qty) => set((state) => ({
          items: state.items.map(i =>
            i.id === id ? { ...i, qty: Math.max(1, qty) } : i
          ),
        })),

        clearCart: () => set({ items: [] }),
        toggleCart: () => set((state) => ({ isOpen: !state.isOpen })),

        // Derived (computed via get())
        getTotal: () => get().items.reduce((sum, i) => sum + i.price * i.qty, 0),
        getCount: () => get().items.reduce((sum, i) => sum + i.qty, 0),
      }),
      { name: 'cart-storage' }  // localStorage key
    )
  )
);

export default useCartStore;
```

**Using Zustand Store:**
```jsx
// Selector দিয়ে — শুধু প্রয়োজনীয় part subscribe করো
function CartIcon() {
  // Only re-renders when count changes
  const count = useCartStore(state => state.getCount());
  const toggleCart = useCartStore(state => state.toggleCart);

  return (
    <button onClick={toggleCart}>
      🛒 {count > 0 && <span>{count}</span>}
    </button>
  );
}

function AddToCartButton({ product }) {
  const addItem = useCartStore(state => state.addItem);
  const items = useCartStore(state => state.items);
  const isInCart = items.some(i => i.id === product.id);

  return (
    <button onClick={() => addItem(product)}>
      {isInCart ? '✓ Added' : 'Add to Cart'}
    </button>
  );
}

// Outside React component (no hooks needed!)
const { addItem, getTotal } = useCartStore.getState();
```

**Zustand with Immer (for complex nested updates):**
```jsx
import { create } from 'zustand';
import { immer } from 'zustand/middleware/immer';

const useStore = create(
  immer((set) => ({
    user: { profile: { name: '', address: { city: '' } } },

    updateCity: (city) => set((state) => {
      // Direct mutation thanks to immer!
      state.user.profile.address.city = city;
    }),
  }))
);
```

---

<a id="p5-comparison"></a>

## 8. Redux vs Context vs Zustand

**Detailed Comparison:**

| Feature | Context API | Zustand | Redux Toolkit |
|---|---|---|---|
| Setup | Built-in, no install | `npm install zustand` | `npm install @reduxjs/toolkit react-redux` |
| Boilerplate | Low | Very Low | Medium |
| Bundle size | 0 | ~1KB | ~11KB |
| DevTools | Limited | ✅ (plugin) | ✅ Excellent |
| Time-travel debug | ❌ | ❌ | ✅ |
| Async handling | Manual | Manual | `createAsyncThunk` |
| Performance | Re-renders all consumers | Selective subscription | Selective (`useSelector`) |
| Learning curve | Easy | Very Easy | Medium |
| Outside React | ❌ | ✅ | ✅ |
| Best for | Theme, Auth, small global state | Small-medium apps | Large, complex apps |

**Decision Guide:**
```
Is it just Theme/Auth/Language?
  → Context API ✅

Small-medium app, want simplicity?
  → Zustand ✅

Large team, complex async, need DevTools & time-travel?
  → Redux Toolkit ✅

Server state (API data)?
  → React Query / SWR (separate tool)
```

**Interview-style Explanation:**
> "Context API simple কিন্তু performance issue আছে — সব consumer re-render হয়। Redux Toolkit powerful কিন্তু boilerplate আছে। Zustand middle ground — Redux-এর power, Context-এর simplicity। আমি project size দেখে choose করি। Production large app-এ RTK prefer করি কারণ DevTools আর team collaboration."

---

<a id="p5-immer"></a>

## 9. Immer & Immutability

**Definition:**
Immer হলো library যা direct mutation-এর মতো code লিখতে দেয় কিন্তু internally immutable update করে। Redux Toolkit Immer built-in use করে।

**কেন Immutability দরকার:**
```jsx
// ❌ Mutable update — React detect করে না!
const state = { user: { name: 'Rahim', score: 10 } };
state.user.score = 20;           // same reference!
setState(state);                  // React: "nothing changed"

// ✅ Immutable update — new reference
setState({
  ...state,
  user: { ...state.user, score: 20 }
});
// React: "new object! re-render!"
```

**Immer under Redux Toolkit:**
```jsx
// RTK-এ Immer built-in — আপনি mutate করুন, Immer new object বানাবে
const slice = createSlice({
  name: 'example',
  initialState: { items: [], user: { name: '', preferences: {} } },
  reducers: {
    // ✅ RTK/Immer — মনে হচ্ছে mutate কিন্তু internally new state
    addItem: (state, action) => {
      state.items.push(action.payload);           // OK in RTK!
    },
    updatePreference: (state, action) => {
      state.user.preferences[action.payload.key] = action.payload.value;
    },

    // ✅ Return new state explicitly (also valid)
    clearItems: (state) => {
      return { ...state, items: [] };
    },

    // ❌ CANNOT both mutate and return
    // bad: (state) => {
    //   state.items = [];     // mutate
    //   return state;         // return — will throw!
    // }
  },
});
```

**Immutability without Immer:**
```jsx
// Nested object update — manual spread
const updateNestedState = (state, userId, newCity) => ({
  ...state,
  users: {
    ...state.users,
    [userId]: {
      ...state.users[userId],
      address: {
        ...state.users[userId].address,
        city: newCity,
      },
    },
  },
});
// 😫 Very verbose! Immer এটা simple করে
```

---

<a id="p5-patterns"></a>

## 10. State Management Patterns

**Normalized State:**
```jsx
// ❌ Nested/Denormalized — update কঠিন
const state = {
  posts: [
    {
      id: 1,
      title: 'React Tips',
      author: { id: 10, name: 'Rahim', avatar: '...' },
      comments: [
        { id: 101, text: 'Great!', author: { id: 20, name: 'Karim' } },
      ],
    },
  ],
};

// ✅ Normalized — flat, update সহজ
const normalizedState = {
  posts: {
    byId: {
      1: { id: 1, title: 'React Tips', authorId: 10, commentIds: [101] },
    },
    allIds: [1],
  },
  users: {
    byId: {
      10: { id: 10, name: 'Rahim', avatar: '...' },
      20: { id: 20, name: 'Karim' },
    },
  },
  comments: {
    byId: {
      101: { id: 101, text: 'Great!', authorId: 20 },
    },
  },
};

// Update author name — একটি জায়গায়, সব reference update
normalizedState.users.byId[10].name = 'Rahim Ahmed';
```

**RTK `createEntityAdapter` (Auto-normalizer):**
```jsx
import { createEntityAdapter, createSlice } from '@reduxjs/toolkit';

const productsAdapter = createEntityAdapter({
  selectId: (product) => product.id,
  sortComparer: (a, b) => a.name.localeCompare(b.name),
});

const productsSlice = createSlice({
  name: 'products',
  initialState: productsAdapter.getInitialState({ loading: false }),
  reducers: {
    addProduct: productsAdapter.addOne,
    addProducts: productsAdapter.addMany,
    updateProduct: productsAdapter.updateOne,
    removeProduct: productsAdapter.removeOne,
    upsertProducts: productsAdapter.upsertMany,
  },
});

// Auto-generated selectors
export const {
  selectAll: selectAllProducts,
  selectById: selectProductById,
  selectIds: selectProductIds,
} = productsAdapter.getSelectors(state => state.products);
```

---

## PART 5 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Say |
|---|---|---|
| State types | Local/Global/Server/URL | Colocate state near usage |
| Context Advanced | Split contexts, memoize value | One big context = all re-render |
| Redux Toolkit | Store → Slice → Action → Dispatch | Immer built-in |
| createAsyncThunk | pending/fulfilled/rejected | `rejectWithValue` for errors |
| Cart Slice | `addOne`, RTK mutation pattern | `extraReducers` for async |
| Zustand | No Provider, selector subscribe | ~1KB, outside React too |
| Comparison | Context:simple, RTK:large, Zustand:medium | Server state → React Query |
| Immer | Apparent mutation → actual immutability | RTK uses it built-in |
| Normalization | Flat state, IDs as keys | `createEntityAdapter` |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part6"></a>

## 📋 PART 6 সূচিপত্র — API Integration & Async React

| # | Topic | Key Concept |
|---|---|---|
| 1 | [Fetch API Basics](#p6-fetch) | fetch, async/await, error handling |
| 2 | [Axios](#p6-axios) | Interceptors, instance, defaults |
| 3 | [API Service Layer](#p6-service) | Separation of concerns |
| 4 | [Loading & Error States](#p6-states) | UI feedback patterns |
| 5 | [React Query (TanStack Query)](#p6-react-query) | Server state management |
| 6 | [Debouncing API Calls](#p6-debounce) | Search optimization |
| 7 | [Infinite Scroll / Pagination](#p6-pagination) | Large data sets |
| 8 | [Optimistic UI Updates](#p6-optimistic) | Instant feedback |
| 9 | [File Upload](#p6-file-upload) | FormData, progress |
| 10 | [Race Conditions & Cleanup](#p6-race) | Stale request handling |

---

<a id="p6-fetch"></a>

## 1. Fetch API Basics

**Definition:**
`fetch` হলো browser-এর built-in HTTP client। React-এ `useEffect`-এর ভেতরে async data fetching করা হয়।

**Fetch Patterns:**
```jsx
// Basic fetch with error handling
async function fetchData(url) {
  const res = await fetch(url);

  // ⚠️ fetch শুধু network error-এ reject করে
  // 404, 500 — reject করে না! manually check করতে হবে
  if (!res.ok) {
    throw new Error(`HTTP error! Status: ${res.status}`);
  }

  return res.json();
}
```

```jsx
// Fetch with full options
async function apiRequest(url, options = {}) {
  const token = localStorage.getItem('token');

  const defaultOptions = {
    headers: {
      'Content-Type': 'application/json',
      ...(token && { 'Authorization': `Bearer ${token}` }),
    },
  };

  const config = {
    ...defaultOptions,
    ...options,
    headers: {
      ...defaultOptions.headers,
      ...options.headers,
    },
  };

  const res = await fetch(url, config);

  if (res.status === 401) {
    // Token expired
    localStorage.removeItem('token');
    window.location.href = '/auth/login';
    throw new Error('Unauthorized');
  }

  if (!res.ok) {
    const error = await res.json().catch(() => ({ message: 'Unknown error' }));
    throw new Error(error.message || `HTTP ${res.status}`);
  }

  // 204 No Content
  if (res.status === 204) return null;

  return res.json();
}

// Usage
const products = await apiRequest('/api/products');
const created = await apiRequest('/api/products', {
  method: 'POST',
  body: JSON.stringify(newProduct),
});
```

**All HTTP Methods:**
```jsx
// GET
const getProducts = () => apiRequest('/api/products');

// POST
const createProduct = (data) => apiRequest('/api/products', {
  method: 'POST',
  body: JSON.stringify(data),
});

// PUT — full update
const updateProduct = (id, data) => apiRequest(`/api/products/${id}`, {
  method: 'PUT',
  body: JSON.stringify(data),
});

// PATCH — partial update
const patchProduct = (id, changes) => apiRequest(`/api/products/${id}`, {
  method: 'PATCH',
  body: JSON.stringify(changes),
});

// DELETE
const deleteProduct = (id) => apiRequest(`/api/products/${id}`, {
  method: 'DELETE',
});
```

---

<a id="p6-axios"></a>

## 2. Axios

**Definition:**
Axios হলো popular HTTP client library। Automatic JSON parsing, request/response interceptors, timeout support, আর better error handling দেয়।

**Installation:**
```bash
npm install axios
```

**Axios vs Fetch:**

| Feature | Fetch | Axios |
|---|---|---|
| Auto JSON parse | ❌ Manual | ✅ |
| Error on 4xx/5xx | ❌ | ✅ |
| Request cancel | AbortController | CancelToken / AbortController |
| Interceptors | ❌ | ✅ |
| Progress | Limited | ✅ |
| Node.js | ❌ Native | ✅ |
| Bundle size | 0 (built-in) | ~14KB |
| Timeout | Manual | Built-in |

**Axios Instance Setup:**
```jsx
// services/api.js
import axios from 'axios';

const api = axios.create({
  baseURL: import.meta.env.VITE_API_BASE_URL || 'http://localhost:8000/api',
  timeout: 15000,
  headers: {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
  },
});

// ──── Request Interceptor ────
api.interceptors.request.use(
  (config) => {
    const token = localStorage.getItem('token');
    if (token) {
      config.headers.Authorization = `Bearer ${token}`;
    }
    // Request logging (dev)
    if (import.meta.env.DEV) {
      console.log(`→ ${config.method?.toUpperCase()} ${config.url}`);
    }
    return config;
  },
  (error) => Promise.reject(error)
);

// ──── Response Interceptor ────
api.interceptors.response.use(
  (response) => {
    // Success — data unwrap
    return response.data;
  },
  async (error) => {
    const original = error.config;

    // 401 — Token refresh attempt
    if (error.response?.status === 401 && !original._retry) {
      original._retry = true;
      try {
        const refreshToken = localStorage.getItem('refreshToken');
        const { data } = await axios.post('/api/auth/refresh', { refreshToken });
        localStorage.setItem('token', data.token);
        original.headers.Authorization = `Bearer ${data.token}`;
        return api(original);  // Retry original request
      } catch {
        localStorage.clear();
        window.location.href = '/auth/login';
      }
    }

    // Error format normalize
    const message = error.response?.data?.message
      || error.message
      || 'Something went wrong';

    return Promise.reject(new Error(message));
  }
);

export default api;
```

**Using Axios Instance:**
```jsx
// services/productService.js
import api from './api';

export const productService = {
  getAll: (params) => api.get('/products', { params }),
  getById: (id) => api.get(`/products/${id}`),
  create: (data) => api.post('/products', data),
  update: (id, data) => api.put(`/products/${id}`, data),
  patch: (id, data) => api.patch(`/products/${id}`, data),
  delete: (id) => api.delete(`/products/${id}`),
  uploadImage: (id, file) => {
    const formData = new FormData();
    formData.append('image', file);
    return api.post(`/products/${id}/image`, formData, {
      headers: { 'Content-Type': 'multipart/form-data' },
    });
  },
};
```

---

<a id="p6-service"></a>

## 3. API Service Layer

**Definition:**
Service layer হলো API call গুলো একটি আলাদা module-এ রাখার pattern। Component-এ সরাসরি fetch না করে service function call করা হয়।

**Folder Structure:**
```
src/
  services/
    api.js              ← axios instance
    authService.js      ← auth API calls
    productService.js   ← product API calls
    orderService.js     ← order API calls
    userService.js      ← user API calls
  hooks/
    useProducts.js      ← data fetching hook
    useAuth.js
  store/
    productsSlice.js
```

**Service Implementation:**
```jsx
// services/authService.js
import api from './api';

export const authService = {
  login: (credentials) =>
    api.post('/auth/login', credentials),

  register: (userData) =>
    api.post('/auth/register', userData),

  logout: () =>
    api.post('/auth/logout'),

  getProfile: () =>
    api.get('/auth/me'),

  updateProfile: (data) =>
    api.patch('/auth/me', data),

  changePassword: (data) =>
    api.patch('/auth/me/password', data),

  forgotPassword: (email) =>
    api.post('/auth/forgot-password', { email }),

  resetPassword: (token, password) =>
    api.post('/auth/reset-password', { token, password }),
};
```

```jsx
// hooks/useProducts.js — service + state combined
import { useState, useEffect, useCallback } from 'react';
import { productService } from '../services/productService';

export function useProducts(initialParams = {}) {
  const [products, setProducts] = useState([]);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);
  const [params, setParams] = useState(initialParams);

  const fetchProducts = useCallback(async () => {
    setLoading(true);
    setError(null);
    try {
      const data = await productService.getAll(params);
      setProducts(data.items || data);
    } catch (err) {
      setError(err.message);
    } finally {
      setLoading(false);
    }
  }, [params]);

  useEffect(() => {
    fetchProducts();
  }, [fetchProducts]);

  return {
    products,
    loading,
    error,
    refetch: fetchProducts,
    updateParams: setParams,
  };
}

// Usage in component
function ProductsPage() {
  const { products, loading, error, updateParams } = useProducts({ page: 1 });
  // ...
}
```

---

<a id="p6-states"></a>

## 4. Loading & Error States

**Definition:**
API call-এর সময় user-কে proper feedback দেওয়া — loading indicator, error message, empty state, skeleton loading।

**Loading State Patterns:**
```jsx
// ──── Pattern 1: Simple boolean ────
function SimpleList() {
  const [data, setData] = useState([]);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    productService.getAll()
      .then(setData)
      .catch(e => setError(e.message))
      .finally(() => setLoading(false));
  }, []);

  if (loading) return <div className="spinner-container"><Spinner /></div>;
  if (error) return <ErrorMessage message={error} onRetry={() => window.location.reload()} />;
  if (data.length === 0) return <EmptyState message="No products found" />;
  return <ProductGrid products={data} />;
}
```

```jsx
// ──── Pattern 2: Status enum (better) ────
const STATUS = { IDLE: 'idle', LOADING: 'loading', SUCCESS: 'success', ERROR: 'error' };

function ProductPage({ productId }) {
  const [status, setStatus] = useState(STATUS.IDLE);
  const [product, setProduct] = useState(null);
  const [error, setError] = useState(null);

  useEffect(() => {
    setStatus(STATUS.LOADING);
    productService.getById(productId)
      .then(data => {
        setProduct(data);
        setStatus(STATUS.SUCCESS);
      })
      .catch(err => {
        setError(err.message);
        setStatus(STATUS.ERROR);
      });
  }, [productId]);

  const renders = {
    [STATUS.IDLE]: null,
    [STATUS.LOADING]: <ProductDetailSkeleton />,
    [STATUS.ERROR]: <ErrorBanner message={error} />,
    [STATUS.SUCCESS]: <ProductDetail product={product} />,
  };

  return renders[status];
}
```

**Skeleton Loading:**
```jsx
// Better UX than spinner — shape ধরে রাখে
function ProductCardSkeleton() {
  return (
    <div className="product-card skeleton">
      <div className="skeleton-image" />
      <div className="skeleton-text skeleton-title" />
      <div className="skeleton-text skeleton-price" />
      <div className="skeleton-button" />
    </div>
  );
}

function ProductGridSkeleton({ count = 6 }) {
  return (
    <div className="product-grid">
      {Array.from({ length: count }, (_, i) => (
        <ProductCardSkeleton key={i} />
      ))}
    </div>
  );
}

// CSS
// .skeleton { animation: shimmer 1.5s infinite; }
// @keyframes shimmer { 0% { opacity: 0.6 } 50% { opacity: 1 } 100% { opacity: 0.6 } }
```

**Global Error Boundary + Toast:**
```jsx
function useToast() {
  const [toasts, setToasts] = useState([]);

  const addToast = useCallback((message, type = 'info', duration = 3000) => {
    const id = Date.now();
    setToasts(prev => [...prev, { id, message, type }]);
    setTimeout(() => {
      setToasts(prev => prev.filter(t => t.id !== id));
    }, duration);
  }, []);

  return {
    toasts,
    success: (msg) => addToast(msg, 'success'),
    error: (msg) => addToast(msg, 'error'),
    info: (msg) => addToast(msg, 'info'),
    warning: (msg) => addToast(msg, 'warning'),
  };
}
```

---

<a id="p6-react-query"></a>

## 5. React Query (TanStack Query)

**Definition:**
React Query হলো server state management library। Caching, background refetching, pagination, mutations — সব automatic। API data-র জন্য Redux-এর বিকল্প।

**Installation:**
```bash
npm install @tanstack/react-query
```

**Setup:**
```jsx
// main.jsx
import { QueryClient, QueryClientProvider } from '@tanstack/react-query';
import { ReactQueryDevtools } from '@tanstack/react-query-devtools';

const queryClient = new QueryClient({
  defaultOptions: {
    queries: {
      staleTime: 5 * 60 * 1000,    // 5 min — data fresh থাকে
      gcTime: 10 * 60 * 1000,      // 10 min — cache থাকে
      retry: 2,                     // fail হলে 2 বার retry
      refetchOnWindowFocus: true,   // tab focus-এ refetch
    },
  },
});

createRoot(document.getElementById('root')).render(
  <QueryClientProvider client={queryClient}>
    <App />
    <ReactQueryDevtools initialIsOpen={false} />
  </QueryClientProvider>
);
```

**useQuery — Data Fetching:**
```jsx
import { useQuery } from '@tanstack/react-query';
import { productService } from '../services/productService';

function ProductsPage() {
  const {
    data,
    isLoading,
    isError,
    error,
    refetch,
    isFetching,   // background refetch indicator
  } = useQuery({
    queryKey: ['products'],              // cache key
    queryFn: () => productService.getAll(),
    staleTime: 5 * 60 * 1000,
  });

  if (isLoading) return <ProductGridSkeleton />;
  if (isError) return <ErrorMessage message={error.message} onRetry={refetch} />;

  return (
    <div>
      {isFetching && <div className="refetch-indicator">Updating...</div>}
      <ProductGrid products={data.items} />
    </div>
  );
}
```

**useQuery with Params:**
```jsx
function ProductDetail({ productId }) {
  const { data: product, isLoading } = useQuery({
    queryKey: ['products', productId],       // productId-dependent key
    queryFn: () => productService.getById(productId),
    enabled: !!productId,                    // productId থাকলেই fetch করো
  });

  if (isLoading) return <Skeleton />;
  return <ProductView product={product} />;
}
```

**useMutation — Create/Update/Delete:**
```jsx
import { useMutation, useQueryClient } from '@tanstack/react-query';

function AddProductForm() {
  const queryClient = useQueryClient();

  const { mutate: createProduct, isPending } = useMutation({
    mutationFn: (data) => productService.create(data),
    onSuccess: (newProduct) => {
      // Cache invalidate — products list refetch হবে
      queryClient.invalidateQueries({ queryKey: ['products'] });
      // অথবা optimistic update
      queryClient.setQueryData(['products'], (old) => ({
        ...old,
        items: [newProduct, ...(old?.items || [])],
      }));
      toast.success('Product created!');
    },
    onError: (error) => {
      toast.error(error.message);
    },
  });

  const handleSubmit = (formData) => {
    createProduct(formData);
  };

  return (
    <form onSubmit={handleSubmit}>
      {/* form fields */}
      <button type="submit" disabled={isPending}>
        {isPending ? 'Creating...' : 'Create Product'}
      </button>
    </form>
  );
}
```

**React Query vs Redux:**

| | React Query | Redux Toolkit |
|---|---|---|
| Purpose | Server state | Client state + server |
| Caching | ✅ Auto | ❌ Manual |
| Background refetch | ✅ | ❌ |
| Loading/error states | ✅ Auto | Manual |
| Devtools | ✅ | ✅ |
| When to use | API data | App state, cart, auth |

---

<a id="p6-debounce"></a>

## 6. Debouncing API Calls

**Definition:**
Debouncing মানে user typing শেষ হওয়ার নির্দিষ্ট সময় পরে API call করা — প্রতিটি keystroke-এ নয়। Network request কমায়।

**Without Debounce — Problem:**
```
User types: "R" "e" "a" "c" "t"
API calls:   5টি request! অপচয়
```

**With Debounce — Solution:**
```
User types: "R" "e" "a" "c" "t" (থামে ৩০০ms)
API calls:   শুধু ১টি request: "React"
```

**useDebounce Hook:**
```jsx
function useDebounce(value, delay = 300) {
  const [debouncedValue, setDebouncedValue] = useState(value);

  useEffect(() => {
    const timer = setTimeout(() => setDebouncedValue(value), delay);
    return () => clearTimeout(timer);
  }, [value, delay]);

  return debouncedValue;
}
```

**Search Component — Complete:**
```jsx
function ProductSearch() {
  const [query, setQuery] = useState('');
  const [results, setResults] = useState([]);
  const [loading, setLoading] = useState(false);

  const debouncedQuery = useDebounce(query, 400);

  useEffect(() => {
    if (!debouncedQuery.trim()) {
      setResults([]);
      return;
    }

    const controller = new AbortController();
    setLoading(true);

    productService.getAll({ search: debouncedQuery, signal: controller.signal })
      .then(data => {
        setResults(data.items);
        setLoading(false);
      })
      .catch(err => {
        if (err.name !== 'AbortError') {
          setLoading(false);
        }
      });

    return () => controller.abort();
  }, [debouncedQuery]);

  return (
    <div className="search-container">
      <input
        value={query}
        onChange={e => setQuery(e.target.value)}
        placeholder="Search products..."
        className="search-input"
      />
      {loading && <SearchSpinner />}

      {results.length > 0 && (
        <ul className="search-results">
          {results.map(product => (
            <li key={product.id}>
              <Link to={`/products/${product.id}`}>
                <img src={product.thumbnail} alt={product.name} />
                <div>
                  <p>{product.name}</p>
                  <p>৳{product.price.toLocaleString()}</p>
                </div>
              </Link>
            </li>
          ))}
        </ul>
      )}

      {!loading && query && results.length === 0 && (
        <p className="no-results">"{query}" — কোনো পণ্য পাওয়া যায়নি</p>
      )}
    </div>
  );
}
```

**Throttle vs Debounce:**

| | Debounce | Throttle |
|---|---|---|
| কখন call | Activity শেষে (idle after X ms) | প্রতি X ms-এ once |
| Use case | Search input, form validation | Scroll handler, resize, button |
| Example | Wait 300ms after last keystroke | Max once per 200ms on scroll |

---

<a id="p6-pagination"></a>

## 7. Infinite Scroll / Pagination

**Traditional Pagination:**
```jsx
function PaginatedProducts() {
  const [page, setPage] = useState(1);
  const [totalPages, setTotalPages] = useState(1);
  const { data, isLoading } = useQuery({
    queryKey: ['products', page],
    queryFn: () => productService.getAll({ page, limit: 12 }),
    onSuccess: (data) => setTotalPages(data.totalPages),
    keepPreviousData: true,    // previous page data দেখা থাকে next fetch-এ
  });

  return (
    <div>
      <ProductGrid products={data?.items || []} loading={isLoading} />
      <Pagination
        current={page}
        total={totalPages}
        onChange={setPage}
      />
    </div>
  );
}

function Pagination({ current, total, onChange }) {
  return (
    <div className="pagination">
      <button
        onClick={() => onChange(current - 1)}
        disabled={current === 1}
      >
        ← Prev
      </button>

      {Array.from({ length: Math.min(total, 7) }, (_, i) => {
        const pageNum = i + 1;
        return (
          <button
            key={pageNum}
            onClick={() => onChange(pageNum)}
            className={current === pageNum ? 'active' : ''}
          >
            {pageNum}
          </button>
        );
      })}

      <button
        onClick={() => onChange(current + 1)}
        disabled={current === total}
      >
        Next →
      </button>
    </div>
  );
}
```

**Infinite Scroll:**
```jsx
import { useInfiniteQuery } from '@tanstack/react-query';
import { useEffect, useRef, useCallback } from 'react';

function InfiniteProductList() {
  const loadMoreRef = useRef(null);

  const {
    data,
    fetchNextPage,
    hasNextPage,
    isFetchingNextPage,
    isLoading,
  } = useInfiniteQuery({
    queryKey: ['products', 'infinite'],
    queryFn: ({ pageParam = 1 }) =>
      productService.getAll({ page: pageParam, limit: 12 }),
    getNextPageParam: (lastPage, allPages) => {
      return lastPage.hasMore ? allPages.length + 1 : undefined;
    },
  });

  // Intersection Observer — "load more" element দৃষ্টিতে এলে next page
  useEffect(() => {
    const observer = new IntersectionObserver(
      ([entry]) => {
        if (entry.isIntersecting && hasNextPage && !isFetchingNextPage) {
          fetchNextPage();
        }
      },
      { threshold: 0.1 }
    );

    if (loadMoreRef.current) observer.observe(loadMoreRef.current);
    return () => observer.disconnect();
  }, [fetchNextPage, hasNextPage, isFetchingNextPage]);

  const allProducts = data?.pages.flatMap(page => page.items) || [];

  if (isLoading) return <ProductGridSkeleton />;

  return (
    <div>
      <div className="product-grid">
        {allProducts.map(product => (
          <ProductCard key={product.id} product={product} />
        ))}
      </div>

      {/* Sentinel element — scroll করে এখানে এলে next page load হয় */}
      <div ref={loadMoreRef} className="load-more-sentinel">
        {isFetchingNextPage && <Spinner />}
        {!hasNextPage && allProducts.length > 0 && (
          <p className="end-of-list">সব পণ্য দেখা হয়েছে</p>
        )}
      </div>
    </div>
  );
}
```

---

<a id="p6-optimistic"></a>

## 8. Optimistic UI Updates

**Definition:**
Optimistic UI মানে API response-এর আগেই UI update করা — ধরে নেওয়া যে success হবে। Request fail হলে rollback। Instant, responsive feel।

**Real-life Analogy:**
WhatsApp message send করলে immediately tick দেখায় — server confirm হওয়ার আগেই। Fail হলে error দেখায়। এটা optimistic UI।

**Optimistic Like Button:**
```jsx
function LikeButton({ postId, initialLikes, initialLiked }) {
  const [liked, setLiked] = useState(initialLiked);
  const [likes, setLikes] = useState(initialLikes);
  const [error, setError] = useState(null);

  const handleLike = async () => {
    // ✅ Optimistic update — সাথে সাথে UI change
    const wasLiked = liked;
    const prevLikes = likes;

    setLiked(!liked);
    setLikes(prev => liked ? prev - 1 : prev + 1);
    setError(null);

    try {
      await postService.toggleLike(postId);
    } catch (err) {
      // ❌ Rollback on failure
      setLiked(wasLiked);
      setLikes(prevLikes);
      setError('Failed to update. Try again.');
    }
  };

  return (
    <div>
      <button
        onClick={handleLike}
        className={`like-btn ${liked ? 'liked' : ''}`}
      >
        {liked ? '❤️' : '🤍'} {likes}
      </button>
      {error && <span className="error-tooltip">{error}</span>}
    </div>
  );
}
```

**Optimistic with React Query:**
```jsx
function TodoList() {
  const queryClient = useQueryClient();

  const { mutate: toggleTodo } = useMutation({
    mutationFn: ({ id, done }) => todoService.update(id, { done }),

    // Optimistic update
    onMutate: async ({ id, done }) => {
      // Pending queries cancel করো
      await queryClient.cancelQueries({ queryKey: ['todos'] });

      // Current state snapshot
      const previousTodos = queryClient.getQueryData(['todos']);

      // Optimistically update
      queryClient.setQueryData(['todos'], (old) =>
        old.map(todo => todo.id === id ? { ...todo, done } : todo)
      );

      // Context return করো rollback-এর জন্য
      return { previousTodos };
    },

    onError: (err, variables, context) => {
      // Rollback
      queryClient.setQueryData(['todos'], context.previousTodos);
      toast.error('Update failed');
    },

    onSettled: () => {
      // Server-এর fresh data দিয়ে sync করো
      queryClient.invalidateQueries({ queryKey: ['todos'] });
    },
  });

  const todos = useQuery({ queryKey: ['todos'], queryFn: todoService.getAll });

  return (
    <ul>
      {todos.data?.map(todo => (
        <li key={todo.id}>
          <input
            type="checkbox"
            checked={todo.done}
            onChange={() => toggleTodo({ id: todo.id, done: !todo.done })}
          />
          <span className={todo.done ? 'done' : ''}>{todo.text}</span>
        </li>
      ))}
    </ul>
  );
}
```

---

<a id="p6-file-upload"></a>

## 9. File Upload

**Definition:**
File upload React-এ `FormData` + `uncontrolled input` (file input সবসময় uncontrolled) দিয়ে করা হয়। Progress tracking-এ `axios` onUploadProgress use করা হয়।

**File Upload Component:**
```jsx
import { useState, useRef } from 'react';
import api from '../services/api';

function FileUpload({ onSuccess }) {
  const fileRef = useRef(null);
  const [preview, setPreview] = useState(null);
  const [progress, setProgress] = useState(0);
  const [uploading, setUploading] = useState(false);
  const [error, setError] = useState(null);

  const handleFileSelect = (e) => {
    const file = e.target.files[0];
    if (!file) return;

    // Validate
    const allowedTypes = ['image/jpeg', 'image/png', 'image/webp'];
    if (!allowedTypes.includes(file.type)) {
      setError('Only JPG, PNG, WebP allowed');
      return;
    }
    if (file.size > 5 * 1024 * 1024) {  // 5MB
      setError('File must be under 5MB');
      return;
    }

    setError(null);
    // Preview
    const reader = new FileReader();
    reader.onloadend = () => setPreview(reader.result);
    reader.readAsDataURL(file);
  };

  const handleUpload = async () => {
    const file = fileRef.current?.files[0];
    if (!file) return;

    const formData = new FormData();
    formData.append('image', file);
    formData.append('folder', 'products');

    setUploading(true);
    setProgress(0);

    try {
      const data = await api.post('/upload', formData, {
        headers: { 'Content-Type': 'multipart/form-data' },
        onUploadProgress: (progressEvent) => {
          const pct = Math.round(
            (progressEvent.loaded * 100) / progressEvent.total
          );
          setProgress(pct);
        },
      });
      onSuccess(data.url);
      setPreview(null);
      setProgress(0);
      if (fileRef.current) fileRef.current.value = '';
    } catch (err) {
      setError(err.message);
    } finally {
      setUploading(false);
    }
  };

  return (
    <div className="file-upload">
      <input
        ref={fileRef}
        type="file"
        accept="image/*"
        onChange={handleFileSelect}
        disabled={uploading}
      />

      {preview && (
        <div className="preview">
          <img src={preview} alt="Preview" />
        </div>
      )}

      {uploading && (
        <div className="progress-bar">
          <div
            className="progress-fill"
            style={{ width: `${progress}%` }}
          />
          <span>{progress}%</span>
        </div>
      )}

      {error && <p className="error">{error}</p>}

      <button
        onClick={handleUpload}
        disabled={!preview || uploading}
        className="btn btn-primary"
      >
        {uploading ? `Uploading ${progress}%...` : 'Upload Image'}
      </button>
    </div>
  );
}
```

---

<a id="p6-race"></a>

## 10. Race Conditions & Cleanup

**Definition:**
Race condition হলো একাধিক async request-এর response যখন ভুল order-এ আসে। Fast typing-এ প্রতিটি keystroke request করলে — পুরানো request-এর response নতুন response-এর পরে আসতে পারে।

**Race Condition Problem:**
```
User types: "R" → Request 1: GET /search?q=R
User types: "Re" → Request 2: GET /search?q=Re
User types: "Rea" → Request 3: GET /search?q=Rea

Response order (network varies):
  Request 3 arrives: results = ["React", "Reason"]  ← correct
  Request 1 arrives: results = ["Rahim", "Rice"]    ← WRONG! old results shown!
```

**Fix 1: AbortController (Recommended):**
```jsx
function SearchResults({ query }) {
  const [results, setResults] = useState([]);

  useEffect(() => {
    if (!query) {
      setResults([]);
      return;
    }

    const controller = new AbortController();

    fetch(`/api/search?q=${query}`, { signal: controller.signal })
      .then(r => r.json())
      .then(setResults)
      .catch(err => {
        if (err.name !== 'AbortError') {
          console.error(err);
        }
        // AbortError ignore — expected
      });

    // Cleanup: query change হলে previous request cancel
    return () => controller.abort();
  }, [query]);  // query change → cleanup previous → new request

  return <ResultsList results={results} />;
}
```

**Fix 2: Ignore Stale Results:**
```jsx
function SearchWithIgnore({ query }) {
  const [results, setResults] = useState([]);

  useEffect(() => {
    let isCurrentRequest = true;  // flag

    fetch(`/api/search?q=${query}`)
      .then(r => r.json())
      .then(data => {
        if (isCurrentRequest) {     // still the latest request?
          setResults(data);
        }
        // else: ignore — outdated response
      });

    return () => {
      isCurrentRequest = false;    // mark as stale
    };
  }, [query]);

  return <ResultsList results={results} />;
}
```

**Fix 3: React Query (Handles automatically):**
```jsx
// React Query automatically handles race conditions!
function SearchResults({ query }) {
  const { data } = useQuery({
    queryKey: ['search', query],
    queryFn: () => searchService.search(query),
    enabled: !!query,
    // React Query automatically cancels in-flight queries
    // when the key changes
  });

  return <ResultsList results={data || []} />;
}
```

---

## PART 6 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Say |
|---|---|---|
| Fetch | `res.ok` check করতে হয় | Network error ≠ HTTP error |
| Axios | Auto JSON, interceptors | Instance create করো |
| Service Layer | Component থেকে API logic আলাদা | Separation of concerns |
| Loading States | Status enum বা boolean | Skeleton > Spinner |
| React Query | Server state management | `queryKey`, `staleTime` |
| Debounce | API call delay | `setTimeout` + cleanup |
| Pagination | `keepPreviousData`, page state | URL-এ page রাখো |
| Infinite Scroll | `IntersectionObserver` | `useInfiniteQuery` |
| Optimistic UI | Immediate update, rollback on error | Snapshot → update → rollback |
| File Upload | `FormData`, `uncontrolled` | Progress with `onUploadProgress` |
| Race Condition | `AbortController` cleanup | useEffect return abort |

---

## PART 5 & 6 Common Interview Questions

**PART 5 — State Management:**
1. Context API-তে re-render সমস্যা কীভাবে solve করবেন?
2. Redux-এ `createAsyncThunk`-এর তিনটি state কী কী?
3. Zustand আর Redux Toolkit-এর পার্থক্য?
4. RTK-এ কেন directly state mutate করা যায়?
5. Normalized state কী? কেন দরকার?
6. Redux Toolkit-এ `createEntityAdapter` কী করে?

**PART 6 — API Integration:**
1. Fetch আর Axios-এর পার্থক্য কী?
2. Axios interceptor কোন কাজে লাগে?
3. Debounce আর Throttle পার্থক্য?
4. Race condition কীভাবে fix করবেন?
5. Optimistic UI update কী? Rollback কীভাবে করবেন?
6. Infinite scroll কীভাবে implement করবেন?
7. React Query আর Redux-এর পার্থক্য কী?

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part7"></a>

## 📋 PART 7 সূচিপত্র — Performance Optimization

| # | Topic | Key Concept |
|---|---|---|
| 1 | [Rendering & Reconciliation](#p7-rendering) | Virtual DOM, diffing |
| 2 | [React.memo](#p7-memo) | Unnecessary re-render prevent |
| 3 | [useMemo](#p7-usememo) | Expensive calculation cache |
| 4 | [useCallback](#p7-usecallback) | Stable function reference |
| 5 | [Code Splitting](#p7-codesplit) | lazy + Suspense |
| 6 | [List Virtualization](#p7-virtual) | react-window, large lists |
| 7 | [Bundle Optimization](#p7-bundle) | Tree shaking, analysis |
| 8 | [Image & Asset Optimization](#p7-images) | Lazy loading, WebP |
| 9 | [Web Vitals](#p7-vitals) | LCP, CLS, INP |
| 10 | [React DevTools Profiler](#p7-profiler) | Finding bottlenecks |

---

<a id="p7-rendering"></a>

## 1. Rendering & Reconciliation

**Definition:**
React render মানে component function call করে JSX থেকে Virtual DOM তৈরি করা। Reconciliation মানে previous Virtual DOM-এর সাথে তুলনা করে শুধু changed parts real DOM-এ update করা।

**Render Triggers:**
```
Component re-render হয় যখন:
  1. State change (useState, useReducer)
  2. Props change (parent re-render → child re-render by default)
  3. Context value change (useContext)
  4. forceUpdate (class components)
```

**React Render Pipeline:**
```
State/Props Change
       ↓
  Component fn() called → New Virtual DOM (JSX)
       ↓
  Diffing: Old Virtual DOM vs New Virtual DOM
       ↓
  Commit: Only changed nodes → Real DOM update
       ↓
  Browser Paint
```

**Re-render Cascade Problem:**
```jsx
// ❌ Every parent re-render triggers ALL children
function ParentComponent() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <button onClick={() => setCount(c => c + 1)}>Count: {count}</button>
      <ExpensiveChild />          {/* Re-renders on every count change! */}
      <AnotherChild />            {/* Re-renders on every count change! */}
      <DeepNestedTree />          {/* Entire tree re-renders! */}
    </div>
  );
}
```

**Key Insight:**
> "React-এ render হওয়া মানেই DOM update না। Virtual DOM diffing cheap। কিন্তু expensive calculation বা large component tree-তে unnecessary renders performance hit করে।"

**Re-render vs Remount:**

| | Re-render | Remount |
|---|---|---|
| কী হয় | fn() আবার call | unmount → mount |
| State | Preserved | Reset |
| Triggered by | State/Props change | `key` prop change, conditional |
| Speed | Fast | Slow |

---

<a id="p7-memo"></a>

## 2. React.memo

**Definition:**
`React.memo` একটি HOC যা props না বদলালে component re-render skip করে। Parent re-render হলেও memoized child শুধু props same থাকলে re-render করে না।

**Basic Usage:**
```jsx
// ✅ React.memo — props same → no re-render
const ProductCard = React.memo(function ProductCard({ product, onAddToCart }) {
  console.log('ProductCard rendered:', product.id);
  return (
    <div className="card">
      <img src={product.image} alt={product.name} />
      <h3>{product.name}</h3>
      <p>৳{product.price.toLocaleString()}</p>
      <button onClick={() => onAddToCart(product)}>Add to Cart</button>
    </div>
  );
});

// Without memo: 100 products × every parent update = 100 re-renders
// With memo: only changed product cards re-render
function ProductGrid({ products }) {
  const [sortBy, setSortBy] = useState('name');
  const { addToCart } = useCart();

  // ⚠️ Problem: new function reference on every render
  // React.memo sees new onAddToCart → re-renders all cards anyway!
  const handleAdd = (product) => addToCart(product);  // ❌

  // ✅ Fix: useCallback for stable reference
  const handleAdd = useCallback((product) => addToCart(product), [addToCart]);

  return (
    <div>
      <SortBar sortBy={sortBy} onChange={setSortBy} />
      <div className="grid">
        {products.map(p => (
          <ProductCard key={p.id} product={p} onAddToCart={handleAdd} />
        ))}
      </div>
    </div>
  );
}
```

**Custom Comparison:**
```jsx
// React.memo default: shallow comparison (Object.is)
// Custom comparator for complex props
const UserRow = React.memo(
  function UserRow({ user, onEdit }) {
    return (
      <tr>
        <td>{user.name}</td>
        <td>{user.email}</td>
        <td><button onClick={() => onEdit(user.id)}>Edit</button></td>
      </tr>
    );
  },
  // Custom: only re-render if these fields change
  (prevProps, nextProps) => {
    return (
      prevProps.user.id === nextProps.user.id &&
      prevProps.user.name === nextProps.user.name &&
      prevProps.user.email === nextProps.user.email &&
      prevProps.onEdit === nextProps.onEdit
    );
  }
);
```

**When to use React.memo:**
```
✅ Use React.memo when:
  - Component renders often with same props
  - Component is expensive to render (heavy DOM, complex logic)
  - Pure presentational component in large list

❌ Skip React.memo when:
  - Component always receives new props anyway
  - Component is cheap/simple
  - Props comparison itself is expensive (deep objects)
```

---

<a id="p7-usememo"></a>

## 3. useMemo

**Definition:**
`useMemo` expensive computation-এর result cache করে। Dependencies না বদলালে cached value return করে — function re-run হয় না।

**Syntax:**
```jsx
const cachedValue = useMemo(() => expensiveCalculation(a, b), [a, b]);
```

**Real Examples:**
```jsx
function ProductAnalytics({ products, filters }) {
  // ❌ Every render-এ recalculate — 10,000 products × every keystroke!
  const stats = calculateComplexStats(products, filters);

  // ✅ Only recalculate when products or filters change
  const stats = useMemo(() => calculateComplexStats(products, filters), [products, filters]);

  // ✅ Expensive sorting
  const sortedProducts = useMemo(() =>
    [...products].sort((a, b) => b.rating - a.rating),
    [products]
  );

  // ✅ Derived data — filtered + grouped
  const grouped = useMemo(() => {
    const filtered = products.filter(p =>
      filters.categories.length === 0 ||
      filters.categories.includes(p.categoryId)
    );
    return filtered.reduce((acc, product) => {
      const cat = product.categoryName;
      if (!acc[cat]) acc[cat] = [];
      acc[cat].push(product);
      return acc;
    }, {});
  }, [products, filters.categories]);

  return <AnalyticsDashboard stats={stats} grouped={grouped} />;
}
```

**Referential Equality — Object/Array:**
```jsx
function UserList({ userId }) {
  // ❌ New array every render → child re-renders even if data same
  const options = { userId, role: 'admin' };  // new object ref every time!

  // ✅ Stable reference — only changes when userId changes
  const options = useMemo(() => ({ userId, role: 'admin' }), [userId]);

  return <UserTable options={options} />;
}
```

**useMemo vs useCallback:**

| | `useMemo` | `useCallback` |
|---|---|---|
| Returns | Computed **value** | **Function** |
| Use for | Expensive calculations, stable objects | Stable function references |
| Equivalent | `useMemo(() => fn, deps)` | `useMemo(() => () => {}, deps)` |

---

<a id="p7-usecallback"></a>

## 4. useCallback

**Definition:**
`useCallback` function-এর stable reference cache করে। Dependencies না বদলালে same function reference return করে — React.memo children unnecessary re-render হয় না।

**Problem without useCallback:**
```jsx
function Parent() {
  const [count, setCount] = useState(0);

  // ❌ New function reference every render
  const handleDelete = (id) => {
    setItems(prev => prev.filter(i => i.id !== id));
  };

  // React.memo on Child is useless — new handleDelete = new prop = re-render!
  return <MemoizedChild onDelete={handleDelete} />;
}
```

**Fix with useCallback:**
```jsx
function Parent() {
  const [count, setCount] = useState(0);
  const [items, setItems] = useState([]);

  // ✅ Stable reference — only changes when setItems changes (never)
  const handleDelete = useCallback((id) => {
    setItems(prev => prev.filter(i => i.id !== id));
  }, []);  // empty deps → setItems from useState is stable

  // ✅ With dependency
  const handleSearch = useCallback((query) => {
    fetchResults(query, filters);   // filters in deps
  }, [filters]);

  return <MemoizedChild onDelete={handleDelete} />;
}
```

**useCallback + useEffect:**
```jsx
function DataFetcher({ userId }) {
  const [data, setData] = useState(null);

  // ✅ Stable fetch function — can be in useEffect deps safely
  const fetchUser = useCallback(async () => {
    const user = await userService.getById(userId);
    setData(user);
  }, [userId]);  // only re-create when userId changes

  useEffect(() => {
    fetchUser();
  }, [fetchUser]);  // safe to include fetchUser in deps

  // ✅ Expose refetch
  return <UserProfile data={data} onRefresh={fetchUser} />;
}
```

**Over-optimization Warning:**
```jsx
// ❌ useCallback on every function — unnecessary overhead
function SimpleComponent() {
  // This component doesn't pass functions to memoized children
  // useCallback here is pointless overhead
  const handleClick = useCallback(() => {
    console.log('clicked');
  }, []);

  return <button onClick={handleClick}>Click</button>;
}

// ✅ useCallback শুধু যেখানে দরকার
// Rule: React.memo child-এ prop হিসেবে pass করলে
//       useEffect deps-এ থাকলে
//       অন্যত্র usually not needed
```

---

<a id="p7-codesplit"></a>

## 5. Code Splitting

**Definition:**
Code splitting মানে app-এর JavaScript bundle কে ছোট ছোট chunk-এ ভাগ করা — প্রয়োজনে lazy load করা। Initial load time কমে।

**Without Code Splitting:**
```
User loads "/" (Home page)
Browser downloads: home.js + products.js + admin.js + dashboard.js + ...
= 2MB download, even though user only needs Home!
```

**With Code Splitting:**
```
User loads "/"
Browser downloads: home.js (~200KB) — fast!

User navigates to /products
Browser downloads: products.js (~400KB) — on demand
```

**React.lazy + Suspense:**
```jsx
import { lazy, Suspense } from 'react';

// ✅ Lazy imports — each route is a separate chunk
const Home = lazy(() => import('./pages/Home'));
const Products = lazy(() => import('./pages/Products'));
const ProductDetail = lazy(() => import('./pages/ProductDetail'));
const Cart = lazy(() => import('./pages/Cart'));
const Checkout = lazy(() => import('./pages/Checkout'));
const AdminDashboard = lazy(() => import('./pages/admin/Dashboard'));
const Profile = lazy(() => import('./pages/Profile'));

// Loading fallback component
function PageLoader() {
  return (
    <div className="page-loader">
      <div className="spinner" />
      <p>Loading...</p>
    </div>
  );
}

function App() {
  return (
    <BrowserRouter>
      <Navbar />
      {/* Suspense: lazy component load হওয়ার আগ পর্যন্ত fallback দেখায় */}
      <Suspense fallback={<PageLoader />}>
        <Routes>
          <Route path="/" element={<Home />} />
          <Route path="/products" element={<Products />} />
          <Route path="/products/:id" element={<ProductDetail />} />
          <Route path="/cart" element={<Cart />} />
          <Route path="/checkout" element={<Checkout />} />
          <Route path="/admin/*" element={
            <ProtectedRoute role="admin">
              <AdminDashboard />
            </ProtectedRoute>
          } />
          <Route path="/profile" element={<Profile />} />
        </Routes>
      </Suspense>
      <Footer />
    </BrowserRouter>
  );
}
```

**Component-level Code Splitting:**
```jsx
// Heavy component (chart library, map, editor) — conditionally load
const RichTextEditor = lazy(() => import('./components/RichTextEditor'));
const SalesChart = lazy(() => import('./components/SalesChart'));

function ProductForm({ mode }) {
  return (
    <form>
      <input name="name" />
      {/* Editor শুধু edit mode-এ দরকার */}
      {mode === 'edit' && (
        <Suspense fallback={<div>Loading editor...</div>}>
          <RichTextEditor />
        </Suspense>
      )}
    </form>
  );
}
```

**Named Exports with lazy:**
```jsx
// ⚠️ React.lazy শুধু default export support করে
// Named export হলে wrapper লাগবে

// components/Charts/index.js
export { BarChart, LineChart, PieChart };

// Wrapper approach
const BarChart = lazy(() =>
  import('./components/Charts').then(module => ({ default: module.BarChart }))
);
```

**Preloading Critical Routes:**
```jsx
// User "/products" link-এ hover করলেই preload শুরু
const Products = lazy(() => import('./pages/Products'));

function Navbar() {
  // Hover করলে preload — click এর আগেই ready
  const preloadProducts = () => import('./pages/Products');

  return (
    <nav>
      <Link to="/products" onMouseEnter={preloadProducts}>
        Products
      </Link>
    </nav>
  );
}
```

---

<a id="p7-virtual"></a>

## 6. List Virtualization

**Definition:**
Virtualization মানে large list-এ শুধু visible items-ই render করা — বাকিগুলো virtual। 10,000 items list থেকে শুধু screen-এ দেখা যাচ্ছে এমন ~20টি render হয়।

**Problem with Large Lists:**
```jsx
// ❌ 10,000 product cards render — browser choke করবে!
function AllProducts({ products }) {
  return (
    <div>
      {products.map(p => <ProductCard key={p.id} product={p} />)}
      {/* 10,000 DOM nodes = slow scroll, high memory */}
    </div>
  );
}
```

**Installation:**
```bash
npm install react-window
# Or: npm install react-virtual (lighter alternative)
```

**react-window — Fixed Size List:**
```jsx
import { FixedSizeList } from 'react-window';

const ITEM_HEIGHT = 80;  // প্রতিটি row-এর height

function VirtualProductList({ products }) {
  const Row = ({ index, style }) => (
    // ⚠️ style prop MUST be applied — virtualization এটা দিয়ে position করে
    <div style={style} className="product-row">
      <img src={products[index].thumbnail} alt={products[index].name} />
      <span>{products[index].name}</span>
      <span>৳{products[index].price.toLocaleString()}</span>
    </div>
  );

  return (
    <FixedSizeList
      height={600}              // visible container height
      width="100%"
      itemCount={products.length}
      itemSize={ITEM_HEIGHT}    // each row height
      overscanCount={5}         // extra rows above/below visible area
    >
      {Row}
    </FixedSizeList>
  );
}
```

**react-window — Variable Size List:**
```jsx
import { VariableSizeList } from 'react-window';

function VariableList({ items }) {
  const getItemSize = (index) => {
    // Different heights based on content
    return items[index].hasDescription ? 120 : 60;
  };

  const Row = ({ index, style }) => (
    <div style={style}>
      <h4>{items[index].title}</h4>
      {items[index].hasDescription && <p>{items[index].description}</p>}
    </div>
  );

  return (
    <VariableSizeList
      height={500}
      width="100%"
      itemCount={items.length}
      itemSize={getItemSize}
    >
      {Row}
    </VariableSizeList>
  );
}
```

**Grid Virtualization:**
```jsx
import { FixedSizeGrid } from 'react-window';

function VirtualProductGrid({ products, columnCount = 4 }) {
  const rowCount = Math.ceil(products.length / columnCount);

  const Cell = ({ columnIndex, rowIndex, style }) => {
    const index = rowIndex * columnCount + columnIndex;
    if (index >= products.length) return <div style={style} />;

    return (
      <div style={{ ...style, padding: '8px' }}>
        <ProductCard product={products[index]} />
      </div>
    );
  };

  return (
    <FixedSizeGrid
      columnCount={columnCount}
      columnWidth={280}
      height={600}
      rowCount={rowCount}
      rowHeight={350}
      width={1200}
    >
      {Cell}
    </FixedSizeGrid>
  );
}
```

---

<a id="p7-bundle"></a>

## 7. Bundle Optimization

**Definition:**
Bundle optimization মানে final JavaScript bundle-এর size কমানো। Tree shaking, dynamic imports, আর unnecessary dependencies remove করা।

**Bundle Analysis — Vite:**
```bash
npm install --save-dev rollup-plugin-visualizer

# vite.config.js
import { visualizer } from 'rollup-plugin-visualizer';

export default {
  plugins: [
    react(),
    visualizer({
      open: true,           // build-এ auto browser open
      filename: 'stats.html',
      gzipSize: true,
      brotliSize: true,
    }),
  ],
};

npm run build
# stats.html খুলবে — কোন library কতটুকু size নিচ্ছে দেখা যাবে
```

**Tree Shaking — Import Correctly:**
```jsx
// ❌ Entire lodash bundle import (~70KB gzipped)
import _ from 'lodash';
const result = _.sortBy(items, 'name');

// ✅ Only the function needed (~1KB)
import sortBy from 'lodash/sortBy';
const result = sortBy(items, 'name');

// ✅ Or use modern alternatives
const result = [...items].sort((a, b) => a.name.localeCompare(b.name));
```

```jsx
// ❌ Entire date-fns import
import * as dateFns from 'date-fns';

// ✅ Named imports — tree-shakeable
import { format, parseISO, differenceInDays } from 'date-fns';
```

**Vite Build Config Optimization:**
```jsx
// vite.config.js
export default defineConfig({
  build: {
    rollupOptions: {
      output: {
        // Manual chunk splitting
        manualChunks: {
          // vendor chunk — rarely changes, long cache
          'react-vendor': ['react', 'react-dom', 'react-router-dom'],
          'redux-vendor': ['@reduxjs/toolkit', 'react-redux'],
          'ui-vendor': ['framer-motion', '@headlessui/react'],
          'chart-vendor': ['recharts'],
        },
      },
    },
    // Chunk size warning threshold
    chunkSizeWarningLimit: 500,  // KB
  },
});
```

**Performance Budget:**
```
Target metrics (Bangladeshi 4G network):
  Initial JS: < 200KB gzipped
  Total bundle: < 1MB gzipped
  First chunk: < 100KB
  TTI (Time to Interactive): < 3s
```

---

<a id="p7-images"></a>

## 8. Image & Asset Optimization

**Definition:**
Images often app-এর largest assets। Lazy loading, correct format, responsive sizes দিয়ে load time উল্লেখযোগ্য কমানো যায়।

**Native Lazy Loading:**
```jsx
// ✅ Browser built-in lazy loading
function ProductCard({ product }) {
  return (
    <div className="card">
      <img
        src={product.image}
        alt={product.name}
        loading="lazy"          // viewport-এ আসার আগে load হবে না
        decoding="async"        // non-blocking image decode
        width={300}             // ✅ Set dimensions — CLS prevent
        height={300}
      />
      <h3>{product.name}</h3>
    </div>
  );
}
```

**Responsive Images:**
```jsx
function HeroBanner({ banner }) {
  return (
    <picture>
      {/* WebP format — ~30% smaller than JPG */}
      <source
        srcSet={`${banner.url}?w=400&fmt=webp 400w,
                 ${banner.url}?w=800&fmt=webp 800w,
                 ${banner.url}?w=1200&fmt=webp 1200w`}
        type="image/webp"
        sizes="(max-width: 600px) 400px, (max-width: 1200px) 800px, 1200px"
      />
      {/* Fallback JPG */}
      <img
        src={`${banner.url}?w=800`}
        alt={banner.alt}
        loading="eager"         // hero image — eager load (above fold)
        fetchpriority="high"    // LCP image — high priority
        width={1200}
        height={400}
      />
    </picture>
  );
}
```

**Intersection Observer — Custom Lazy Load:**
```jsx
function LazyImage({ src, alt, className }) {
  const [loaded, setLoaded] = useState(false);
  const [inView, setInView] = useState(false);
  const imgRef = useRef(null);

  useEffect(() => {
    const observer = new IntersectionObserver(
      ([entry]) => {
        if (entry.isIntersecting) {
          setInView(true);
          observer.disconnect();
        }
      },
      { rootMargin: '200px' }   // 200px আগে থেকে load শুরু
    );

    if (imgRef.current) observer.observe(imgRef.current);
    return () => observer.disconnect();
  }, []);

  return (
    <div ref={imgRef} className={`img-wrapper ${loaded ? 'loaded' : 'loading'}`}>
      {inView && (
        <img
          src={src}
          alt={alt}
          className={className}
          onLoad={() => setLoaded(true)}
        />
      )}
      {!loaded && <div className="img-placeholder shimmer" />}
    </div>
  );
}
```

---

<a id="p7-vitals"></a>

## 9. Web Vitals

**Definition:**
Web Vitals হলো Google-এর user experience metrics। Real-world performance measure করে। SEO ranking-এও impact করে।

**Core Web Vitals:**

| Metric | Full Name | কী মাপে | Good | Needs Improvement | Poor |
|---|---|---|---|---|---|
| LCP | Largest Contentful Paint | Loading — বড় content কতক্ষণে দেখা যায় | ≤2.5s | 2.5–4s | >4s |
| INP | Interaction to Next Paint | Interactivity — click/tap response | ≤200ms | 200–500ms | >500ms |
| CLS | Cumulative Layout Shift | Visual stability — layout shift | ≤0.1 | 0.1–0.25 | >0.25 |

**Measuring Web Vitals:**
```jsx
// npm install web-vitals
import { onCLS, onINP, onLCP, onFCP, onTTFB } from 'web-vitals';

function reportToAnalytics({ name, value, rating }) {
  console.log(`${name}: ${value} (${rating})`);
  // Google Analytics, Datadog, etc.
  gtag('event', name, { value: Math.round(value), metric_rating: rating });
}

onCLS(reportToAnalytics);
onINP(reportToAnalytics);
onLCP(reportToAnalytics);
onFCP(reportToAnalytics);
onTTFB(reportToAnalytics);
```

**Common CLS Causes & Fixes:**
```jsx
// ❌ Image without dimensions — layout shift!
<img src={product.image} alt={product.name} />

// ✅ Always set width/height or aspect-ratio
<img src={product.image} alt={product.name} width={300} height={300} />

// Or CSS aspect ratio
// .product-image { aspect-ratio: 1/1; width: 100%; }

// ❌ Dynamic content insertion above existing content
// (ads, banners loading in) → reserve space
// ✅ CSS min-height for dynamic areas
// .ad-slot { min-height: 90px; }
```

**LCP Optimization:**
```jsx
// ✅ Preload LCP image
// <link rel="preload" as="image" href="/hero-banner.webp">

// ✅ fetchpriority on hero image
<img src="/hero-banner.webp" fetchpriority="high" loading="eager" alt="..." />

// ✅ Avoid lazy loading above-the-fold images
// loading="lazy" শুধু below the fold images-এ
```

---

<a id="p7-profiler"></a>

## 10. React DevTools Profiler

**Definition:**
React DevTools Profiler দিয়ে কোন component কতবার, কতক্ষণ render হচ্ছে — তা visually দেখা যায়। Performance bottleneck identify করার tool।

**Using Profiler Component:**
```jsx
import { Profiler } from 'react';

function onRenderCallback(
  id,           // component tree name
  phase,        // "mount" or "update"
  actualDuration,   // render time ms
  baseDuration,     // without memoization (estimate)
  startTime,
  commitTime
) {
  if (actualDuration > 16) {  // 16ms = 60fps budget
    console.warn(`Slow render: ${id} took ${actualDuration.toFixed(2)}ms`);
  }
}

function App() {
  return (
    <Profiler id="ProductGrid" onRender={onRenderCallback}>
      <ProductGrid />
    </Profiler>
  );
}
```

**DevTools Workflow:**
```
1. Chrome/Firefox → React DevTools extension install
2. DevTools → Profiler tab
3. "Record" click → User action করো → "Stop"
4. Flame graph দেখো:
   - Wide bars = slow renders
   - Grey = not rendered (memoized ✅)
   - Yellow/Orange = re-rendered
5. "Ranked" view → slowest components top-এ
6. Click component → why rendered (props/state/context changed)
```

**Common Optimization Findings:**
```
Problem: Context value প্রতিটি render-এ নতুন object
Fix: useMemo(() => value, [deps])

Problem: Callback fn প্রতিটি render-এ নতুন reference
Fix: useCallback(() => fn, [deps])

Problem: Large list সব render
Fix: react-window virtualization

Problem: Expensive filter/sort প্রতিটি render
Fix: useMemo

Problem: Child re-renders যদিও props same
Fix: React.memo
```

---

## PART 7 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Say |
|---|---|---|
| Rendering | Virtual DOM diff → only changed DOM update | Render ≠ DOM update |
| React.memo | Shallow props compare → skip re-render | Pair with useCallback |
| useMemo | Cache computed value | Dependencies same → cached |
| useCallback | Cache function reference | Needed for React.memo children |
| Code Splitting | lazy + Suspense → route-based chunks | Initial bundle কমায় |
| Virtualization | Only visible items render | react-window, 10k items |
| Bundle | Tree shaking, named imports | Lodash/fp not full import |
| Images | lazy loading, dimensions, WebP | CLS fix: always set dimensions |
| Web Vitals | LCP, CLS, INP | LCP≤2.5s, CLS≤0.1, INP≤200ms |
| Profiler | Flame graph, why-rendered | actualDuration > 16ms = problem |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part8"></a>

## 📋 PART 8 সূচিপত্র — Advanced React

| # | Topic | Key Concept |
|---|---|---|
| 1 | [Error Boundaries](#p8-error-boundary) | Crash isolation |
| 2 | [Portals](#p8-portals) | Outside root DOM |
| 3 | [Refs & forwardRef](#p8-refs) | DOM access, parent ref |
| 4 | [useImperativeHandle](#p8-imperative) | Custom ref API |
| 5 | [useTransition & startTransition](#p8-transition) | Non-urgent updates |
| 6 | [useDeferredValue](#p8-deferred) | Input responsiveness |
| 7 | [Suspense for Data](#p8-suspense) | Declarative loading |
| 8 | [React Fiber Architecture](#p8-fiber) | How React works inside |
| 9 | [Custom Hooks — Advanced](#p8-custom-hooks) | Reusable logic patterns |
| 10 | [React 19 New Features](#p8-react19) | use(), Actions, Compiler |

---

<a id="p8-error-boundary"></a>

## 1. Error Boundaries

**Definition:**
Error Boundary হলো class component যা child component tree-তে JavaScript error catch করে — পুরো app crash না করে fallback UI দেখায়। `componentDidCatch` + `getDerivedStateFromError` দিয়ে তৈরি।

**Why Class Component:**
> Hooks দিয়ে Error Boundary বানানো যায় না — `componentDidCatch` lifecycle-এর equivalent hook নেই (এখনো)।

**Error Boundary Implementation:**
```jsx
import { Component } from 'react';

class ErrorBoundary extends Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false, error: null, errorInfo: null };
  }

  // Error হলে state update করো (render phase)
  static getDerivedStateFromError(error) {
    return { hasError: true, error };
  }

  // Error log করো (commit phase)
  componentDidCatch(error, errorInfo) {
    this.setState({ errorInfo });
    // Error reporting service
    console.error('ErrorBoundary caught:', error, errorInfo);
    // logErrorToService(error, errorInfo.componentStack);
  }

  handleReset = () => {
    this.setState({ hasError: false, error: null, errorInfo: null });
  };

  render() {
    if (this.state.hasError) {
      // Custom fallback
      if (this.props.fallback) {
        return this.props.fallback({
          error: this.state.error,
          reset: this.handleReset,
        });
      }

      return (
        <div className="error-boundary">
          <h2>কিছু একটা ভুল হয়েছে</h2>
          <p>{this.state.error?.message}</p>
          <button onClick={this.handleReset}>আবার চেষ্টা করুন</button>
        </div>
      );
    }

    return this.props.children;
  }
}
```

**Usage — Granular Error Isolation:**
```jsx
function App() {
  return (
    <ErrorBoundary fallback={({ error, reset }) => (
      <div className="app-error">
        <h1>App crashed: {error.message}</h1>
        <button onClick={reset}>Reload</button>
      </div>
    )}>
      <Navbar />

      {/* Independent sections — one crash doesn't kill others */}
      <ErrorBoundary fallback={({ reset }) => (
        <div className="section-error">
          <p>Products section failed to load</p>
          <button onClick={reset}>Retry</button>
        </div>
      )}>
        <ProductSection />
      </ErrorBoundary>

      <ErrorBoundary fallback={() => <p>Recommendations unavailable</p>}>
        <RecommendationEngine />   {/* 3rd party widget */}
      </ErrorBoundary>
    </ErrorBoundary>
  );
}
```

**react-error-boundary (library):**
```jsx
// npm install react-error-boundary
import { ErrorBoundary, useErrorBoundary } from 'react-error-boundary';

function ProductPage() {
  const { showBoundary } = useErrorBoundary();

  const loadProducts = async () => {
    try {
      const data = await productService.getAll();
      setProducts(data);
    } catch (err) {
      showBoundary(err);  // Trigger nearest ErrorBoundary
    }
  };

  return (
    <ErrorBoundary
      FallbackComponent={({ error, resetErrorBoundary }) => (
        <div>
          <p>Error: {error.message}</p>
          <button onClick={resetErrorBoundary}>Try again</button>
        </div>
      )}
      onReset={() => {
        // reset state when retry
        setProducts([]);
      }}
    >
      <ProductGrid />
    </ErrorBoundary>
  );
}
```

---

<a id="p8-portals"></a>

## 2. Portals

**Definition:**
Portal দিয়ে component-কে DOM-এর অন্য জায়গায় render করা যায় — parent-এর বাইরে। Modal, tooltip, dropdown-এ z-index আর overflow: hidden সমস্যা solve করে।

**Problem Portals Solve:**
```html
<!-- ❌ Without portal — Modal parent-এর overflow: hidden-এ আটকে যায় -->
<div class="product-card" style="overflow: hidden">
  <button>View Details</button>
  <!-- Modal এখানে render হলে কেটে যাবে! -->
  <div class="modal">...</div>
</div>

<!-- ✅ With portal — Modal সরাসরি body-তে render -->
<div class="product-card" style="overflow: hidden">
  <button>View Details</button>
</div>
<!-- Portal: body-তে render, z-index সমস্যা নেই -->
<div id="modal-root">
  <div class="modal">...</div>
</div>
```

**Portal Implementation:**
```jsx
import { createPortal } from 'react-dom';
import { useEffect, useRef } from 'react';

function Modal({ isOpen, onClose, title, children }) {
  const modalRoot = document.getElementById('modal-root');

  // ESC key to close
  useEffect(() => {
    const handleKeyDown = (e) => {
      if (e.key === 'Escape') onClose();
    };
    if (isOpen) {
      document.addEventListener('keydown', handleKeyDown);
      document.body.style.overflow = 'hidden';  // Scroll lock
    }
    return () => {
      document.removeEventListener('keydown', handleKeyDown);
      document.body.style.overflow = '';
    };
  }, [isOpen, onClose]);

  if (!isOpen) return null;

  // Portal: React tree-তে ProductCard-এর child কিন্তু DOM-এ #modal-root-এ
  return createPortal(
    <div
      className="modal-overlay"
      onClick={onClose}
      role="dialog"
      aria-modal="true"
      aria-labelledby="modal-title"
    >
      <div
        className="modal-content"
        onClick={e => e.stopPropagation()}
      >
        <div className="modal-header">
          <h2 id="modal-title">{title}</h2>
          <button onClick={onClose} aria-label="Close">&times;</button>
        </div>
        <div className="modal-body">
          {children}
        </div>
      </div>
    </div>,
    modalRoot
  );
}

// index.html
// <div id="root"></div>
// <div id="modal-root"></div>  ← Portal target
```

**Tooltip with Portal:**
```jsx
function Tooltip({ text, children }) {
  const [show, setShow] = useState(false);
  const [position, setPosition] = useState({ top: 0, left: 0 });
  const triggerRef = useRef(null);

  const handleMouseEnter = () => {
    const rect = triggerRef.current.getBoundingClientRect();
    setPosition({
      top: rect.top - 40 + window.scrollY,
      left: rect.left + rect.width / 2 + window.scrollX,
    });
    setShow(true);
  };

  return (
    <>
      <span
        ref={triggerRef}
        onMouseEnter={handleMouseEnter}
        onMouseLeave={() => setShow(false)}
      >
        {children}
      </span>

      {show && createPortal(
        <div
          className="tooltip"
          style={{ top: position.top, left: position.left }}
        >
          {text}
        </div>,
        document.body
      )}
    </>
  );
}
```

---

<a id="p8-refs"></a>

## 3. Refs & forwardRef

**Definition:**
`useRef` দুটি কাজ করে: (1) DOM element-এ direct access, (2) render trigger না করে mutable value store। `forwardRef` parent component-কে child-এর DOM-এ access দেয়।

**useRef — DOM Access:**
```jsx
function AutoFocusInput() {
  const inputRef = useRef(null);

  // Component mount হলে auto focus
  useEffect(() => {
    inputRef.current?.focus();
  }, []);

  const handleClear = () => {
    if (inputRef.current) {
      inputRef.current.value = '';
      inputRef.current.focus();
    }
  };

  return (
    <div>
      <input ref={inputRef} type="text" placeholder="Search..." />
      <button onClick={handleClear}>Clear</button>
    </div>
  );
}
```

**useRef — Mutable Value (no re-render):**
```jsx
function Timer() {
  const [count, setCount] = useState(0);
  const intervalRef = useRef(null);    // interval ID store — no re-render

  const start = () => {
    if (!intervalRef.current) {
      intervalRef.current = setInterval(() => {
        setCount(c => c + 1);
      }, 1000);
    }
  };

  const stop = () => {
    clearInterval(intervalRef.current);
    intervalRef.current = null;
  };

  useEffect(() => {
    return () => clearInterval(intervalRef.current);   // cleanup on unmount
  }, []);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={start}>Start</button>
      <button onClick={stop}>Stop</button>
    </div>
  );
}
```

**forwardRef — Parent Access to Child DOM:**
```jsx
// Custom Input — parent wants to focus/blur it
const CustomInput = forwardRef(function CustomInput(
  { label, error, ...props },
  ref       // forwarded ref from parent
) {
  return (
    <div className="input-group">
      <label>{label}</label>
      <input ref={ref} {...props} className={error ? 'error' : ''} />
      {error && <span className="error-msg">{error}</span>}
    </div>
  );
});

// Parent component
function LoginForm() {
  const emailRef = useRef(null);
  const passwordRef = useRef(null);

  const handleSubmit = (e) => {
    e.preventDefault();
    if (!emailRef.current.value) {
      emailRef.current.focus();     // Parent controls child input focus!
      return;
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <CustomInput ref={emailRef} label="Email" type="email" />
      <CustomInput ref={passwordRef} label="Password" type="password" />
      <button type="submit">Login</button>
    </form>
  );
}
```

---

<a id="p8-imperative"></a>

## 4. useImperativeHandle

**Definition:**
`useImperativeHandle` parent-কে child-এর custom methods expose করে — পুরো DOM না দিয়ে specific API। `forwardRef`-এর সাথে use করা হয়।

```jsx
// Custom Video Player — parent controls play/pause/seek
const VideoPlayer = forwardRef(function VideoPlayer({ src, poster }, ref) {
  const videoRef = useRef(null);

  // Parent শুধু এই methods পাবে — পুরো <video> DOM না
  useImperativeHandle(ref, () => ({
    play: () => videoRef.current?.play(),
    pause: () => videoRef.current?.pause(),
    seek: (time) => { if (videoRef.current) videoRef.current.currentTime = time; },
    getCurrentTime: () => videoRef.current?.currentTime ?? 0,
    getDuration: () => videoRef.current?.duration ?? 0,
    setVolume: (vol) => { if (videoRef.current) videoRef.current.volume = Math.max(0, Math.min(1, vol)); },
  }), []);

  return (
    <video ref={videoRef} src={src} poster={poster} className="video-player" />
  );
});

// Parent usage
function CoursePage({ lesson }) {
  const playerRef = useRef(null);

  return (
    <div>
      <VideoPlayer ref={playerRef} src={lesson.videoUrl} poster={lesson.thumbnail} />

      {/* Custom controls — parent calls child methods */}
      <div className="custom-controls">
        <button onClick={() => playerRef.current?.play()}>▶ Play</button>
        <button onClick={() => playerRef.current?.pause()}>⏸ Pause</button>
        <button onClick={() => playerRef.current?.seek(0)}>⏮ Restart</button>
        <button onClick={() => playerRef.current?.seek(
          (playerRef.current?.getCurrentTime() ?? 0) + 10
        )}>+10s</button>
      </div>
    </div>
  );
}
```

---

<a id="p8-transition"></a>

## 5. useTransition & startTransition

**Definition:**
`useTransition` non-urgent state updates mark করে — urgent updates (typing, clicking) priority পায়। Heavy re-render-এ UI freeze হয় না।

**Problem without Transition:**
```jsx
// ❌ Typing করলে search আর input — দুটোই block হয়
function SearchPage() {
  const [query, setQuery] = useState('');
  const [results, setResults] = useState(allProducts);

  const handleChange = (e) => {
    setQuery(e.target.value);
    // ⚠️ 10,000 items filter — UI freeze করে! input lag!
    setResults(allProducts.filter(p =>
      p.name.toLowerCase().includes(e.target.value.toLowerCase())
    ));
  };

  return (
    <>
      <input value={query} onChange={handleChange} />
      <ResultList results={results} />   {/* 10,000 items */}
    </>
  );
}
```

**Fix with useTransition:**
```jsx
import { useState, useTransition } from 'react';

function SearchPage() {
  const [query, setQuery] = useState('');
  const [results, setResults] = useState(allProducts);
  const [isPending, startTransition] = useTransition();

  const handleChange = (e) => {
    const value = e.target.value;

    // Urgent: input update immediately
    setQuery(value);

    // Non-urgent: heavy filter can be deferred
    startTransition(() => {
      setResults(allProducts.filter(p =>
        p.name.toLowerCase().includes(value.toLowerCase())
      ));
    });
  };

  return (
    <>
      <input value={query} onChange={handleChange} />
      {/* isPending: show loading state while transitioning */}
      {isPending
        ? <div className="searching">Searching...</div>
        : <ResultList results={results} />
      }
    </>
  );
}
```

**Tab Switching with Transition:**
```jsx
function TabPanel() {
  const [activeTab, setActiveTab] = useState('feed');
  const [isPending, startTransition] = useTransition();

  const switchTab = (tab) => {
    startTransition(() => {
      setActiveTab(tab);   // Heavy tab content — non-urgent
    });
  };

  return (
    <div>
      <div className="tabs">
        {['feed', 'trending', 'following'].map(tab => (
          <button
            key={tab}
            onClick={() => switchTab(tab)}
            className={`tab ${activeTab === tab ? 'active' : ''} ${isPending ? 'loading' : ''}`}
          >
            {tab}
          </button>
        ))}
      </div>
      <Suspense fallback={<TabSkeleton />}>
        <TabContent tab={activeTab} />
      </Suspense>
    </div>
  );
}
```

---

<a id="p8-deferred"></a>

## 6. useDeferredValue

**Definition:**
`useDeferredValue` একটি value-এর "deferred copy" রাখে। Input responsive থাকে, heavy render defer হয়। `useTransition`-এর alternative — third-party component control না থাকলে।

```jsx
import { useState, useDeferredValue, memo } from 'react';

// ✅ Heavy list — memoized
const ProductResults = memo(function ProductResults({ query }) {
  // Expensive filter
  const filtered = allProducts.filter(p =>
    p.name.toLowerCase().includes(query.toLowerCase())
  );
  return (
    <ul>
      {filtered.map(p => <ProductRow key={p.id} product={p} />)}
    </ul>
  );
});

function SearchInput() {
  const [query, setQuery] = useState('');
  // Deferred: React urgent update (input) আগে করে, list update defer করে
  const deferredQuery = useDeferredValue(query);

  // query !== deferredQuery → still processing
  const isStale = query !== deferredQuery;

  return (
    <div>
      <input
        value={query}
        onChange={e => setQuery(e.target.value)}
        placeholder="Search products..."
      />
      {/* Stale state visual hint */}
      <div style={{ opacity: isStale ? 0.5 : 1, transition: 'opacity 0.2s' }}>
        <ProductResults query={deferredQuery} />
      </div>
    </div>
  );
}
```

**useTransition vs useDeferredValue:**

| | `useTransition` | `useDeferredValue` |
|---|---|---|
| কী defer করে | setState call | Value |
| কখন | নিজের state control আছে | Third-party/prop value |
| isPending | ✅ | ❌ (stale comparison করতে হয়) |
| Use case | Tab switch, search filter | List rendering, third-party |

---

<a id="p8-suspense"></a>

## 7. Suspense for Data

**Definition:**
Suspense data fetching-এর সময় fallback দেখায় — `isLoading` manually manage না করে। React Query, Relay, বা React 19 `use()` hook-এর সাথে কাজ করে।

**Suspense with React Query:**
```jsx
// QueryClient — suspense enable
const queryClient = new QueryClient({
  defaultOptions: {
    queries: {
      suspense: true,   // Enable suspense mode
    },
  },
});

// Suspense-enabled query
function ProductDetail({ id }) {
  // No isLoading check needed — Suspense handles it
  const { data: product } = useQuery({
    queryKey: ['product', id],
    queryFn: () => productService.getById(id),
    suspense: true,
  });

  return (
    <div>
      <h1>{product.name}</h1>
      <p>৳{product.price.toLocaleString()}</p>
    </div>
  );
}

// Parent — declarative loading
function ProductPage({ id }) {
  return (
    <ErrorBoundary fallback={<ErrorMessage />}>
      <Suspense fallback={<ProductDetailSkeleton />}>
        <ProductDetail id={id} />      {/* No loading state inside */}
      </Suspense>
    </ErrorBoundary>
  );
}
```

**Nested Suspense:**
```jsx
function Dashboard() {
  return (
    <div className="dashboard">
      {/* Critical content loads first */}
      <Suspense fallback={<HeaderSkeleton />}>
        <DashboardHeader />
      </Suspense>

      <div className="dashboard-body">
        {/* Independent sections — parallel loading */}
        <Suspense fallback={<ChartSkeleton />}>
          <SalesChart />
        </Suspense>

        <Suspense fallback={<TableSkeleton />}>
          <RecentOrders />
        </Suspense>

        <Suspense fallback={<StatsSkeleton />}>
          <TopProducts />
        </Suspense>
      </div>
    </div>
  );
}
```

---

<a id="p8-fiber"></a>

## 8. React Fiber Architecture

**Definition:**
React Fiber হলো React 16+ এর reconciliation engine। Work unit-কে ছোট chunks-এ ভাগ করে — pause, resume, prioritize করা যায়। Concurrent features এটার উপর ভিত্তি করে।

**Before Fiber (React 15 Stack Reconciler):**
```
Problem: বড় component tree update একবারে করতে হতো
         — 100ms লাগলে browser input block হতো (frame drop)

Stack: synchronous, non-interruptible
     → 60fps impossible for heavy updates
```

**Fiber — Incremental Rendering:**
```
Fiber: Virtual DOM-এর প্রতিটি component = একটি Fiber node (linked list)

Work loop:
  1. Render phase (interruptible):
     - Component render করো, Virtual DOM তৈরি করো
     - Higher priority work আসলে pause করো
     - Browser idle time-এ resume করো

  2. Commit phase (non-interruptible):
     - Real DOM update করো
     - Side effects চালাও
```

**Priority Levels (Lanes):**
```
SyncLane:         User input (click, type) — immediate
InputContinuous:  Mouse move, scroll
DefaultLane:      useEffect, data fetch
TransitionLane:   startTransition — deferrable
IdleLane:         Background work — lowest priority
```

**Practical Implications:**
```jsx
// Fiber enables:
// 1. Concurrent rendering (useTransition, useDeferredValue)
// 2. Suspense
// 3. Error Boundaries (per-tree)
// 4. Priority-based rendering

// Example: two setState calls batch হয় (React 18+ automatic batching)
function handleClick() {
  setCount(c => c + 1);    // These are batched —
  setTitle('Updated');      // ONE re-render, not two
  setLoading(false);        // ← React 18: batched even in async!
}

// React 17: async function-এ batching ছিল না
// React 18: automatic batching everywhere
```

---

<a id="p8-custom-hooks"></a>

## 9. Custom Hooks — Advanced Patterns

**Definition:**
Advanced custom hooks complex logic encapsulate করে। Multiple hooks combine করে reusable, testable patterns তৈরি করে।

**useLocalStorage:**
```jsx
function useLocalStorage(key, initialValue) {
  const [storedValue, setStoredValue] = useState(() => {
    try {
      const item = localStorage.getItem(key);
      return item ? JSON.parse(item) : initialValue;
    } catch {
      return initialValue;
    }
  });

  const setValue = useCallback((value) => {
    try {
      const valueToStore = value instanceof Function
        ? value(storedValue)
        : value;
      setStoredValue(valueToStore);
      localStorage.setItem(key, JSON.stringify(valueToStore));
    } catch (error) {
      console.error(error);
    }
  }, [key, storedValue]);

  const removeValue = useCallback(() => {
    localStorage.removeItem(key);
    setStoredValue(initialValue);
  }, [key, initialValue]);

  return [storedValue, setValue, removeValue];
}

// Usage
const [theme, setTheme] = useLocalStorage('theme', 'light');
const [recentSearches, setRecentSearches] = useLocalStorage('searches', []);
```

**useAsync — Generic Async Handler:**
```jsx
function useAsync(asyncFn, immediate = true) {
  const [status, setStatus] = useState('idle');
  const [data, setData] = useState(null);
  const [error, setError] = useState(null);

  const execute = useCallback(async (...args) => {
    setStatus('loading');
    setData(null);
    setError(null);
    try {
      const result = await asyncFn(...args);
      setData(result);
      setStatus('success');
      return result;
    } catch (err) {
      setError(err.message);
      setStatus('error');
      throw err;
    }
  }, [asyncFn]);

  useEffect(() => {
    if (immediate) execute();
  }, [execute, immediate]);

  return {
    execute,
    status,
    data,
    error,
    isLoading: status === 'loading',
    isSuccess: status === 'success',
    isError: status === 'error',
  };
}

// Usage
function UserProfile({ userId }) {
  const { data: user, isLoading, error, execute: refetch } = useAsync(
    () => userService.getById(userId)
  );

  if (isLoading) return <Skeleton />;
  if (error) return <ErrorState onRetry={refetch} />;
  return <Profile user={user} />;
}
```

**useEventListener:**
```jsx
function useEventListener(eventName, handler, element = window) {
  const savedHandler = useRef(handler);

  useEffect(() => {
    savedHandler.current = handler;
  }, [handler]);

  useEffect(() => {
    if (!element?.addEventListener) return;
    const listener = (e) => savedHandler.current(e);
    element.addEventListener(eventName, listener);
    return () => element.removeEventListener(eventName, listener);
  }, [eventName, element]);
}

// Usage
function App() {
  useEventListener('keydown', (e) => {
    if (e.key === 'Escape') closeModal();
    if ((e.ctrlKey || e.metaKey) && e.key === 'k') openSearch();
  });
}
```

**usePrevious:**
```jsx
function usePrevious(value) {
  const ref = useRef(undefined);
  useEffect(() => {
    ref.current = value;
  }, [value]);
  return ref.current;   // Returns value from previous render
}

// Usage
function Counter() {
  const [count, setCount] = useState(0);
  const prevCount = usePrevious(count);

  return (
    <div>
      <p>Now: {count} | Before: {prevCount ?? 'none'}</p>
      <button onClick={() => setCount(c => c + 1)}>Increment</button>
    </div>
  );
}
```

---

<a id="p8-react19"></a>

## 10. React 19 New Features

**Definition:**
React 19 (2024) major new features নিয়ে এসেছে: `use()` hook, Server Actions, React Compiler (auto-memoization), আর form Actions।

**`use()` Hook:**
```jsx
import { use, Suspense } from 'react';

// use() — Promise বা Context read করে
// Suspense আর Error Boundary automatically handle করে

// Create a promise (outside component)
function fetchProductData(id) {
  return fetch(`/api/products/${id}`).then(r => r.json());
}

function ProductDetail({ id }) {
  // use() suspends component until promise resolves
  const product = use(fetchProductData(id));    // No await, no useEffect!

  return (
    <div>
      <h1>{product.name}</h1>
      <p>৳{product.price.toLocaleString()}</p>
    </div>
  );
}

function ProductPage({ id }) {
  const productPromise = fetchProductData(id);  // Start fetching early!

  return (
    <ErrorBoundary fallback={<ErrorUI />}>
      <Suspense fallback={<ProductSkeleton />}>
        <ProductDetail id={id} />
      </Suspense>
    </ErrorBoundary>
  );
}

// use() with Context (conditionally!)
// unlike useContext, use() can be called conditionally
function ThemedButton({ variant, children }) {
  if (variant === 'plain') {
    return <button>{children}</button>;  // No theme needed
  }
  const theme = use(ThemeContext);       // ✅ Conditional context read
  return <button style={{ background: theme.primary }}>{children}</button>;
}
```

**Form Actions (React 19):**
```jsx
import { useActionState, useFormStatus } from 'react';

// useActionState — form submission state
function LoginForm() {
  async function loginAction(prevState, formData) {
    const email = formData.get('email');
    const password = formData.get('password');

    try {
      const user = await authService.login({ email, password });
      return { success: true, user };
    } catch (err) {
      return { success: false, error: err.message };
    }
  }

  const [state, dispatch, isPending] = useActionState(loginAction, null);

  return (
    <form action={dispatch}>
      {state?.error && <p className="error">{state.error}</p>}
      {state?.success && <p className="success">Logged in!</p>}

      <input name="email" type="email" required />
      <input name="password" type="password" required />

      <SubmitButton />
    </form>
  );
}

// useFormStatus — inside form component
function SubmitButton() {
  const { pending } = useFormStatus();    // parent form-এর status
  return (
    <button type="submit" disabled={pending}>
      {pending ? 'Logging in...' : 'Login'}
    </button>
  );
}
```

**React Compiler (React 19+):**
```jsx
// React Compiler — automatic memoization
// useMemo, useCallback, React.memo manually লেখা লাগবে না
// Compiler analyze করে automatically optimize করে

// Before Compiler: manually optimize
const ExpensiveList = React.memo(({ items, onDelete }) => {
  const sorted = useMemo(() => [...items].sort(), [items]);
  const handleDelete = useCallback((id) => onDelete(id), [onDelete]);
  // ...
});

// After React Compiler: write natural code, compiler handles it
function ExpensiveList({ items, onDelete }) {
  const sorted = [...items].sort();       // Compiler auto-memoizes
  const handleDelete = (id) => onDelete(id);  // Compiler makes stable ref
  // ...
}

// Enable: babel plugin or next.js built-in
// next.config.js: experimental: { reactCompiler: true }
```

**React 19 Summary:**

| Feature | Description | Old way |
|---|---|---|
| `use()` hook | Promise/Context read anywhere | `useEffect` + `useState` |
| `useActionState` | Form action state | Manual form state |
| `useFormStatus` | Form pending in child | Prop drilling |
| `useOptimistic` | Optimistic UI built-in | Manual rollback |
| React Compiler | Auto memoization | Manual `useMemo`/`useCallback` |
| Server Components | Zero JS on client | N/A (Next.js feature) |

---

## PART 8 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Say |
|---|---|---|
| Error Boundary | Class component, `componentDidCatch` | Hook দিয়ে হয় না |
| Portals | `createPortal(children, domNode)` | Modal/tooltip overflow fix |
| forwardRef | Parent → child DOM access | `React.forwardRef(fn)` |
| useImperativeHandle | Custom ref API expose | forwardRef এর সাথে |
| useTransition | Non-urgent setState | `isPending` loading state |
| useDeferredValue | Deferred value copy | Stale opacity pattern |
| Suspense data | Declarative loading | ErrorBoundary wrap করো |
| Fiber | Incremental, prioritized rendering | Pause/resume/prioritize |
| Custom Hooks | Logic encapsulation | `use` prefix, return values |
| React 19 | `use()`, Actions, Compiler | Auto memoization |

---

## PART 7 & 8 Common Interview Questions

**PART 7 — Performance:**
1. `useMemo` আর `useCallback`-এর পার্থক্য কী?
2. `React.memo` কখন কাজ করে না?
3. Code splitting কীভাবে করবেন?
4. List virtualization কেন দরকার?
5. CLS কী? কীভাবে fix করবেন?
6. `useCallback` ছাড়া `React.memo` কেন কাজ করে না?

**PART 8 — Advanced:**
1. Error Boundary class component কেন হতে হয়?
2. Portal কোন সমস্যা solve করে?
3. `forwardRef` vs `useImperativeHandle` পার্থক্য?
4. `useTransition` vs `useDeferredValue` কখন কোনটা?
5. React Fiber কী? কেন দরকার?
6. React 19-এর `use()` hook কীভাবে কাজ করে?

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part9"></a>

## 📋 PART 9 সূচিপত্র — Backend Integration & Authentication

| # | Topic | Key Concept |
|---|---|---|
| 1 | [JWT Authentication Flow](#p9-jwt) | Token lifecycle, storage |
| 2 | [Login System Implementation](#p9-login) | Full auth flow in React |
| 3 | [AuthContext — Global Auth State](#p9-authcontext) | Provider, hooks, persistence |
| 4 | [Protected Routes](#p9-protected) | Role-based access control |
| 5 | [Token Refresh Strategy](#p9-refresh) | Silent refresh, interceptor |
| 6 | [RBAC — Role Based Access](#p9-rbac) | Permissions, guards |
| 7 | [OAuth / Social Login](#p9-oauth) | Google, GitHub login flow |
| 8 | [Form Validation](#p9-validation) | React Hook Form + Zod |
| 9 | [Environment Variables & Config](#p9-env) | Vite env, API base URL |
| 10 | [Security Best Practices](#p9-security) | XSS, CSRF, HTTPS |

---

<a id="p9-jwt"></a>

## 1. JWT Authentication Flow

**Definition:**
JWT (JSON Web Token) হলো self-contained token যাতে user info encode থাকে। Server session রাখে না — token-ই proof of identity।

**JWT Structure:**
```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9   ← Header (base64)
.eyJzdWIiOiIxMjM0IiwibmFtZSI6IlJhaGltIn0   ← Payload (base64)
.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c   ← Signature (HMAC)

Payload contains: userId, email, role, exp (expiry), iat (issued at)
```

**Complete Auth Flow:**
```
1. User: email + password → POST /api/auth/login
2. Server: verify credentials → create JWT (accessToken) + refreshToken
3. Server: response → { accessToken, refreshToken, user }
4. Client: store tokens
5. Client: every API request → Authorization: Bearer <accessToken>
6. Server: verify token signature → allow/deny
7. accessToken expire (15min) → use refreshToken → new accessToken
8. refreshToken expire (7d) → logout
```

**Token Storage — Where to keep:**

| Storage | XSS Risk | CSRF Risk | Notes |
|---|---|---|---|
| `localStorage` | ❌ HIGH | ✅ Safe | JS readable — XSS সহজ |
| `sessionStorage` | ❌ HIGH | ✅ Safe | Tab বন্ধে clear |
| `httpOnly Cookie` | ✅ Safe | ❌ CSRF risk | Best for refresh token |
| Memory (useState) | ✅ Safe | ✅ Safe | Page refresh-এ হারায় |

**Recommended Strategy:**
```
accessToken → Memory (React state) — short-lived (15min), XSS safe
refreshToken → httpOnly Cookie — long-lived (7d), JS cannot read

Why: accessToken memory-তে → page refresh-এ হারায়
     → silent refresh endpoint hit করো → new accessToken পাও
     → seamless UX
```

**JWT Decode (without verification):**
```jsx
function decodeJWT(token) {
  try {
    const payload = token.split('.')[1];
    const decoded = JSON.parse(atob(payload));
    return decoded;
  } catch {
    return null;
  }
}

function isTokenExpired(token) {
  const decoded = decodeJWT(token);
  if (!decoded?.exp) return true;
  return Date.now() / 1000 > decoded.exp;
}

// Usage
const payload = decodeJWT(token);
// { sub: "123", name: "Rahim", role: "admin", exp: 1716000000 }
```

---

<a id="p9-login"></a>

## 2. Login System Implementation

**Complete Login Flow:**
```jsx
// services/authService.js
import api from './api';

export const authService = {
  login: async ({ email, password }) => {
    const data = await api.post('/auth/login', { email, password });
    // data: { accessToken, refreshToken (set in cookie by server), user }
    return data;
  },

  register: async (userData) => {
    return api.post('/auth/register', userData);
  },

  logout: async () => {
    await api.post('/auth/logout');  // server-side cookie clear
  },

  refreshToken: async () => {
    // httpOnly cookie automatic-এ পাঠায়
    return api.post('/auth/refresh');
  },

  getProfile: async () => {
    return api.get('/auth/me');
  },
};
```

```jsx
// pages/Login.jsx
import { useState } from 'react';
import { useNavigate, useLocation, Link } from 'react-router-dom';
import { useAuth } from '../context/AuthContext';

function LoginPage() {
  const [form, setForm] = useState({ email: '', password: '' });
  const [loading, setLoading] = useState(false);
  const [error, setError] = useState('');
  const [showPassword, setShowPassword] = useState(false);

  const { login } = useAuth();
  const navigate = useNavigate();
  const location = useLocation();

  // Redirect to previous page after login
  const from = location.state?.from?.pathname || '/dashboard';

  const handleChange = (e) => {
    setForm(prev => ({ ...prev, [e.target.name]: e.target.value }));
    if (error) setError('');
  };

  const handleSubmit = async (e) => {
    e.preventDefault();

    // Client-side validation
    if (!form.email || !form.password) {
      setError('সব field পূরণ করুন');
      return;
    }

    setLoading(true);
    setError('');

    try {
      await login(form.email, form.password);
      navigate(from, { replace: true });
    } catch (err) {
      setError(err.message || 'Login failed. Check your credentials.');
    } finally {
      setLoading(false);
    }
  };

  return (
    <div className="auth-page">
      <div className="auth-card">
        <div className="auth-header">
          <img src="/logo.svg" alt="Logo" />
          <h1>স্বাগতম</h1>
          <p>আপনার account-এ login করুন</p>
        </div>

        {error && (
          <div className="alert alert-error" role="alert">
            {error}
          </div>
        )}

        <form onSubmit={handleSubmit} noValidate>
          <div className="form-group">
            <label htmlFor="email">Email</label>
            <input
              id="email"
              name="email"
              type="email"
              value={form.email}
              onChange={handleChange}
              placeholder="example@email.com"
              autoComplete="email"
              disabled={loading}
              required
            />
          </div>

          <div className="form-group">
            <label htmlFor="password">Password</label>
            <div className="input-with-icon">
              <input
                id="password"
                name="password"
                type={showPassword ? 'text' : 'password'}
                value={form.password}
                onChange={handleChange}
                placeholder="••••••••"
                autoComplete="current-password"
                disabled={loading}
                required
              />
              <button
                type="button"
                onClick={() => setShowPassword(s => !s)}
                className="toggle-password"
                aria-label={showPassword ? 'Hide password' : 'Show password'}
              >
                {showPassword ? '🙈' : '👁'}
              </button>
            </div>
          </div>

          <div className="form-options">
            <label className="checkbox-label">
              <input type="checkbox" name="rememberMe" /> Remember me
            </label>
            <Link to="/forgot-password">Password ভুলে গেছেন?</Link>
          </div>

          <button
            type="submit"
            className="btn btn-primary btn-full"
            disabled={loading}
          >
            {loading ? (
              <><span className="spinner-sm" /> Logging in...</>
            ) : 'Login'}
          </button>
        </form>

        <p className="auth-footer">
          Account নেই? <Link to="/register">Register করুন</Link>
        </p>
      </div>
    </div>
  );
}

export default LoginPage;
```

---

<a id="p9-authcontext"></a>

## 3. AuthContext — Global Auth State

**Complete AuthContext:**
```jsx
// context/AuthContext.jsx
import {
  createContext, useContext, useState,
  useEffect, useCallback, useMemo
} from 'react';
import { authService } from '../services/authService';

const AuthContext = createContext(null);

export function AuthProvider({ children }) {
  const [user, setUser] = useState(null);
  const [token, setToken] = useState(null);    // memory only (XSS safe)
  const [loading, setLoading] = useState(true); // initial auth check

  // App start-এ silent refresh — cookie থেকে নতুন accessToken
  useEffect(() => {
    const initAuth = async () => {
      try {
        const data = await authService.refreshToken();
        setToken(data.accessToken);
        setUser(data.user);
      } catch {
        // No valid session — user is logged out
        setUser(null);
        setToken(null);
      } finally {
        setLoading(false);
      }
    };
    initAuth();
  }, []);

  const login = useCallback(async (email, password) => {
    const data = await authService.login({ email, password });
    setToken(data.accessToken);
    setUser(data.user);
    return data;
  }, []);

  const logout = useCallback(async () => {
    try {
      await authService.logout();
    } catch {
      // logout silently even if API fails
    } finally {
      setToken(null);
      setUser(null);
    }
  }, []);

  const updateUser = useCallback((updates) => {
    setUser(prev => prev ? { ...prev, ...updates } : prev);
  }, []);

  // Expose token to api.js interceptor
  useEffect(() => {
    // Store token in a module-level variable for interceptor access
    window.__authToken = token;
  }, [token]);

  const value = useMemo(() => ({
    user,
    token,
    isLoggedIn: !!user,
    isLoading: loading,
    login,
    logout,
    updateUser,
  }), [user, token, loading, login, logout, updateUser]);

  if (loading) {
    return (
      <div className="app-loading">
        <div className="spinner-lg" />
        <p>Loading...</p>
      </div>
    );
  }

  return (
    <AuthContext.Provider value={value}>
      {children}
    </AuthContext.Provider>
  );
}

export const useAuth = () => {
  const ctx = useContext(AuthContext);
  if (!ctx) throw new Error('useAuth must be used within AuthProvider');
  return ctx;
};

// Convenience hooks
export const useUser = () => useAuth().user;
export const useIsLoggedIn = () => useAuth().isLoggedIn;
```

**Axios Interceptor — Token from Context:**
```jsx
// services/api.js — use window.__authToken set by AuthContext
api.interceptors.request.use((config) => {
  const token = window.__authToken;
  if (token) config.headers.Authorization = `Bearer ${token}`;
  return config;
});
```

---

<a id="p9-protected"></a>

## 4. Protected Routes

**Complete Protected Route System:**
```jsx
// components/ProtectedRoute.jsx
import { Navigate, Outlet, useLocation } from 'react-router-dom';
import { useAuth } from '../context/AuthContext';

// Basic auth guard
export function ProtectedRoute({ children }) {
  const { isLoggedIn, isLoading } = useAuth();
  const location = useLocation();

  if (isLoading) return <PageLoader />;

  if (!isLoggedIn) {
    // Save attempted URL for post-login redirect
    return <Navigate to="/login" state={{ from: location }} replace />;
  }

  return children || <Outlet />;
}

// Role-based guard
export function RoleGuard({ allowedRoles, children, fallback }) {
  const { user, isLoggedIn, isLoading } = useAuth();
  const location = useLocation();

  if (isLoading) return <PageLoader />;

  if (!isLoggedIn) {
    return <Navigate to="/login" state={{ from: location }} replace />;
  }

  if (!allowedRoles.includes(user?.role)) {
    return fallback || <Navigate to="/unauthorized" replace />;
  }

  return children || <Outlet />;
}

// Public-only route (login/register) — redirect if logged in
export function PublicOnlyRoute({ children }) {
  const { isLoggedIn, isLoading } = useAuth();

  if (isLoading) return <PageLoader />;
  if (isLoggedIn) return <Navigate to="/dashboard" replace />;

  return children || <Outlet />;
}
```

**App Routes Setup:**
```jsx
// App.jsx
import { lazy, Suspense } from 'react';
import { Routes, Route } from 'react-router-dom';
import { ProtectedRoute, RoleGuard, PublicOnlyRoute } from './components/ProtectedRoute';

const Home = lazy(() => import('./pages/Home'));
const Login = lazy(() => import('./pages/Login'));
const Register = lazy(() => import('./pages/Register'));
const Dashboard = lazy(() => import('./pages/Dashboard'));
const Profile = lazy(() => import('./pages/Profile'));
const AdminPanel = lazy(() => import('./pages/admin/AdminPanel'));
const AdminUsers = lazy(() => import('./pages/admin/Users'));
const Unauthorized = lazy(() => import('./pages/Unauthorized'));

function App() {
  return (
    <Suspense fallback={<PageLoader />}>
      <Routes>
        {/* Public routes */}
        <Route path="/" element={<Home />} />
        <Route path="/unauthorized" element={<Unauthorized />} />

        {/* Public-only (redirect if logged in) */}
        <Route element={<PublicOnlyRoute />}>
          <Route path="/login" element={<Login />} />
          <Route path="/register" element={<Register />} />
        </Route>

        {/* Protected — any logged-in user */}
        <Route element={<ProtectedRoute />}>
          <Route path="/dashboard" element={<Dashboard />} />
          <Route path="/profile" element={<Profile />} />
          <Route path="/settings" element={<Settings />} />
        </Route>

        {/* Admin only */}
        <Route element={<RoleGuard allowedRoles={['admin', 'super_admin']} />}>
          <Route path="/admin" element={<AdminPanel />} />
          <Route path="/admin/users" element={<AdminUsers />} />
          <Route path="/admin/products" element={<AdminProducts />} />
        </Route>

        <Route path="*" element={<NotFound />} />
      </Routes>
    </Suspense>
  );
}
```

---

<a id="p9-refresh"></a>

## 5. Token Refresh Strategy

**Silent Refresh Pattern:**
```jsx
// Axios interceptor — automatic token refresh on 401
let isRefreshing = false;
let failedQueue = [];   // 401 হলে pending requests queue

const processQueue = (error, token = null) => {
  failedQueue.forEach(({ resolve, reject }) => {
    if (error) reject(error);
    else resolve(token);
  });
  failedQueue = [];
};

api.interceptors.response.use(
  (response) => response,
  async (error) => {
    const original = error.config;

    if (error.response?.status !== 401 || original._retry) {
      return Promise.reject(error);
    }

    if (isRefreshing) {
      // Already refreshing — queue this request
      return new Promise((resolve, reject) => {
        failedQueue.push({ resolve, reject });
      }).then(token => {
        original.headers.Authorization = `Bearer ${token}`;
        return api(original);
      });
    }

    original._retry = true;
    isRefreshing = true;

    try {
      const data = await authService.refreshToken();
      const newToken = data.accessToken;

      // Update global token
      window.__authToken = newToken;

      // Retry queued requests
      processQueue(null, newToken);

      original.headers.Authorization = `Bearer ${newToken}`;
      return api(original);
    } catch (refreshError) {
      processQueue(refreshError, null);
      // Refresh failed — force logout
      window.__authToken = null;
      window.dispatchEvent(new Event('auth:logout'));
      return Promise.reject(refreshError);
    } finally {
      isRefreshing = false;
    }
  }
);

// Listen in AuthContext
useEffect(() => {
  const handleAuthLogout = () => logout();
  window.addEventListener('auth:logout', handleAuthLogout);
  return () => window.removeEventListener('auth:logout', handleAuthLogout);
}, [logout]);
```

**Token Expiry Check — Proactive Refresh:**
```jsx
// Refresh before expiry (e.g., 1 min before)
function useTokenRefresh(token) {
  useEffect(() => {
    if (!token) return;

    const decoded = decodeJWT(token);
    if (!decoded?.exp) return;

    // Calculate time until 1 min before expiry
    const expiresIn = decoded.exp * 1000 - Date.now() - 60000;

    if (expiresIn <= 0) return;   // Already near expiry

    const timer = setTimeout(async () => {
      try {
        const data = await authService.refreshToken();
        setToken(data.accessToken);
      } catch {
        logout();
      }
    }, expiresIn);

    return () => clearTimeout(timer);
  }, [token]);
}
```

---

<a id="p9-rbac"></a>

## 6. RBAC — Role Based Access Control

**Definition:**
RBAC মানে user-এর role অনুযায়ী কী দেখতে পাবে, কী করতে পারবে তা নির্ধারণ। Admin সব দেখে, editor content manage করে, user শুধু নিজেরটা দেখে।

**Permission System:**
```jsx
// config/permissions.js
export const ROLES = {
  SUPER_ADMIN: 'super_admin',
  ADMIN: 'admin',
  EDITOR: 'editor',
  USER: 'user',
};

export const PERMISSIONS = {
  // Products
  'products:read': ['super_admin', 'admin', 'editor', 'user'],
  'products:create': ['super_admin', 'admin', 'editor'],
  'products:update': ['super_admin', 'admin', 'editor'],
  'products:delete': ['super_admin', 'admin'],

  // Users
  'users:read': ['super_admin', 'admin'],
  'users:create': ['super_admin', 'admin'],
  'users:update': ['super_admin', 'admin'],
  'users:delete': ['super_admin'],

  // Orders
  'orders:read_own': ['super_admin', 'admin', 'user'],
  'orders:read_all': ['super_admin', 'admin'],
  'orders:update_status': ['super_admin', 'admin'],

  // Analytics
  'analytics:view': ['super_admin', 'admin'],
  'analytics:export': ['super_admin'],
};

export function hasPermission(userRole, permission) {
  return PERMISSIONS[permission]?.includes(userRole) ?? false;
}

export function hasAnyPermission(userRole, permissions) {
  return permissions.some(p => hasPermission(userRole, p));
}
```

**usePermission Hook:**
```jsx
// hooks/usePermission.js
import { useUser } from '../context/AuthContext';
import { hasPermission, hasAnyPermission } from '../config/permissions';

export function usePermission() {
  const user = useUser();

  return {
    can: (permission) => hasPermission(user?.role, permission),
    canAny: (permissions) => hasAnyPermission(user?.role, permissions),
    role: user?.role,
    isAdmin: ['admin', 'super_admin'].includes(user?.role),
    isSuperAdmin: user?.role === 'super_admin',
  };
}
```

**Permission Guard Component:**
```jsx
// components/Can.jsx
import { usePermission } from '../hooks/usePermission';

export function Can({ permission, fallback = null, children }) {
  const { can } = usePermission();
  return can(permission) ? children : fallback;
}

export function CanAny({ permissions, fallback = null, children }) {
  const { canAny } = usePermission();
  return canAny(permissions) ? children : fallback;
}

// Usage in components
function ProductActions({ product }) {
  const { can } = usePermission();

  return (
    <div className="actions">
      {/* Everyone sees view */}
      <Link to={`/products/${product.id}`}>View</Link>

      {/* Only editor+ can edit */}
      <Can permission="products:update">
        <Link to={`/products/${product.id}/edit`}>Edit</Link>
      </Can>

      {/* Only admin can delete */}
      <Can
        permission="products:delete"
        fallback={<span className="tooltip" title="Admin only">Delete</span>}
      >
        <button onClick={() => handleDelete(product.id)}>Delete</button>
      </Can>
    </div>
  );
}

// Navbar — conditional menu items
function AdminNav() {
  const { isAdmin } = usePermission();

  return (
    <nav>
      <Link to="/dashboard">Dashboard</Link>
      <Can permission="products:create">
        <Link to="/products/new">Add Product</Link>
      </Can>
      <Can permission="users:read">
        <Link to="/admin/users">Users</Link>
      </Can>
      <Can permission="analytics:view">
        <Link to="/admin/analytics">Analytics</Link>
      </Can>
    </nav>
  );
}
```

---

<a id="p9-oauth"></a>

## 7. OAuth / Social Login

**Definition:**
OAuth 2.0 দিয়ে Google, Facebook, GitHub-এর account দিয়ে login করা যায়। Password manage করতে হয় না। Authorization Code Flow সবচেয়ে secure।

**OAuth Flow:**
```
1. User: "Login with Google" click করে
2. Frontend: Google OAuth URL-এ redirect করে
   https://accounts.google.com/o/oauth2/auth?
     client_id=YOUR_CLIENT_ID&
     redirect_uri=https://yourapp.com/auth/callback&
     response_type=code&
     scope=email profile

3. Google: User login করে → permission দেয়
4. Google: redirect_uri-তে ?code=AUTH_CODE পাঠায়

5. Frontend: code → backend-এ পাঠায়
6. Backend: code দিয়ে Google-এর token endpoint hit করে
7. Backend: Google থেকে user info পায়
8. Backend: নিজের JWT তৈরি করে → frontend-কে দেয়
9. Frontend: normal JWT auth flow
```

**Frontend — Google OAuth Button:**
```jsx
// Option 1: Redirect-based (simple, secure)
function GoogleLoginButton() {
  const handleGoogleLogin = () => {
    const params = new URLSearchParams({
      client_id: import.meta.env.VITE_GOOGLE_CLIENT_ID,
      redirect_uri: `${window.location.origin}/auth/callback/google`,
      response_type: 'code',
      scope: 'email profile',
      access_type: 'offline',
      prompt: 'select_account',
    });

    window.location.href = `https://accounts.google.com/o/oauth2/auth?${params}`;
  };

  return (
    <button onClick={handleGoogleLogin} className="btn-social btn-google">
      <GoogleIcon />
      Google দিয়ে login করুন
    </button>
  );
}
```

```jsx
// Option 2: Google One Tap (npm install @react-oauth/google)
import { GoogleOAuthProvider, GoogleLogin } from '@react-oauth/google';
import { useAuth } from '../context/AuthContext';

function App() {
  return (
    <GoogleOAuthProvider clientId={import.meta.env.VITE_GOOGLE_CLIENT_ID}>
      <AuthProvider>
        <BrowserRouter>
          <Routes>...</Routes>
        </BrowserRouter>
      </AuthProvider>
    </GoogleOAuthProvider>
  );
}

function SocialLoginButtons() {
  const { login } = useAuth();

  const handleGoogleSuccess = async (credentialResponse) => {
    try {
      // Send Google token to your backend
      const data = await authService.googleLogin(credentialResponse.credential);
      // data: { accessToken, user }
      login(data);
    } catch (err) {
      toast.error('Google login failed');
    }
  };

  return (
    <div className="social-login">
      <GoogleLogin
        onSuccess={handleGoogleSuccess}
        onError={() => toast.error('Google login failed')}
        useOneTap
      />
    </div>
  );
}
```

**OAuth Callback Handler:**
```jsx
// pages/OAuthCallback.jsx
import { useEffect } from 'react';
import { useNavigate, useSearchParams } from 'react-router-dom';
import { useAuth } from '../context/AuthContext';

function OAuthCallback() {
  const [searchParams] = useSearchParams();
  const navigate = useNavigate();
  const { login } = useAuth();

  useEffect(() => {
    const code = searchParams.get('code');
    const error = searchParams.get('error');

    if (error) {
      navigate('/login?error=oauth_denied');
      return;
    }

    if (code) {
      authService.exchangeCode(code)
        .then(data => {
          login(data);
          navigate('/dashboard');
        })
        .catch(() => navigate('/login?error=oauth_failed'));
    }
  }, []);

  return (
    <div className="oauth-loading">
      <Spinner />
      <p>Logging you in...</p>
    </div>
  );
}
```

---

<a id="p9-validation"></a>

## 8. Form Validation — React Hook Form + Zod

**Definition:**
React Hook Form (RHF) performance-optimized form library। Zod TypeScript-first schema validation। দুটো একসাথে powerful form + validation system তৈরি করে।

**Installation:**
```bash
npm install react-hook-form zod @hookform/resolvers
```

**Registration Form — Full Example:**
```jsx
import { useForm } from 'react-hook-form';
import { zodResolver } from '@hookform/resolvers/zod';
import { z } from 'zod';

// Zod schema — validation rules
const registerSchema = z.object({
  name: z
    .string()
    .min(3, 'নাম কমপক্ষে ৩ অক্ষরের হতে হবে')
    .max(50, 'নাম ৫০ অক্ষরের বেশি হবে না'),

  email: z
    .string()
    .email('সঠিক email address দিন'),

  phone: z
    .string()
    .regex(/^01[3-9]\d{8}$/, 'সঠিক বাংলাদেশি মোবাইল নম্বর দিন')
    .optional()
    .or(z.literal('')),

  password: z
    .string()
    .min(8, 'Password কমপক্ষে ৮ অক্ষরের হতে হবে')
    .regex(/[A-Z]/, 'কমপক্ষে একটি uppercase letter লাগবে')
    .regex(/[0-9]/, 'কমপক্ষে একটি number লাগবে'),

  confirmPassword: z.string(),

  agreeToTerms: z
    .boolean()
    .refine(val => val === true, 'Terms and conditions agree করতে হবে'),
})
.refine(
  (data) => data.password === data.confirmPassword,
  {
    message: 'Password মিলছে না',
    path: ['confirmPassword'],
  }
);

function RegisterForm() {
  const {
    register,
    handleSubmit,
    formState: { errors, isSubmitting, isValid },
    watch,
    setError,
    reset,
  } = useForm({
    resolver: zodResolver(registerSchema),
    mode: 'onChange',    // validate on change
    defaultValues: {
      name: '', email: '', phone: '',
      password: '', confirmPassword: '',
      agreeToTerms: false,
    },
  });

  const password = watch('password');

  const onSubmit = async (data) => {
    try {
      await authService.register(data);
      reset();
      navigate('/login?registered=true');
    } catch (err) {
      // Server validation errors
      if (err.field) {
        setError(err.field, { message: err.message });
      } else {
        setError('root', { message: err.message });
      }
    }
  };

  return (
    <form onSubmit={handleSubmit(onSubmit)} noValidate>
      {errors.root && (
        <div className="alert alert-error">{errors.root.message}</div>
      )}

      <div className="form-group">
        <label htmlFor="name">পূর্ণ নাম *</label>
        <input
          id="name"
          {...register('name')}
          className={errors.name ? 'input-error' : ''}
          placeholder="আপনার নাম লিখুন"
        />
        {errors.name && (
          <span className="field-error">{errors.name.message}</span>
        )}
      </div>

      <div className="form-group">
        <label htmlFor="email">Email *</label>
        <input
          id="email"
          type="email"
          {...register('email')}
          className={errors.email ? 'input-error' : ''}
          placeholder="example@email.com"
        />
        {errors.email && (
          <span className="field-error">{errors.email.message}</span>
        )}
      </div>

      <div className="form-group">
        <label htmlFor="password">Password *</label>
        <input
          id="password"
          type="password"
          {...register('password')}
          className={errors.password ? 'input-error' : ''}
        />
        {errors.password && (
          <span className="field-error">{errors.password.message}</span>
        )}
        {/* Password strength indicator */}
        <PasswordStrength password={password} />
      </div>

      <div className="form-group">
        <label htmlFor="confirmPassword">Password নিশ্চিত করুন *</label>
        <input
          id="confirmPassword"
          type="password"
          {...register('confirmPassword')}
          className={errors.confirmPassword ? 'input-error' : ''}
        />
        {errors.confirmPassword && (
          <span className="field-error">{errors.confirmPassword.message}</span>
        )}
      </div>

      <div className="form-group">
        <label className="checkbox-label">
          <input type="checkbox" {...register('agreeToTerms')} />
          <Link to="/terms">Terms & Conditions</Link> এ রাজি
        </label>
        {errors.agreeToTerms && (
          <span className="field-error">{errors.agreeToTerms.message}</span>
        )}
      </div>

      <button
        type="submit"
        disabled={isSubmitting || !isValid}
        className="btn btn-primary btn-full"
      >
        {isSubmitting ? 'Creating account...' : 'Register'}
      </button>
    </form>
  );
}
```

---

<a id="p9-env"></a>

## 9. Environment Variables & Config

**Vite Environment Variables:**
```bash
# .env (committed — public defaults)
VITE_APP_NAME=MyShop
VITE_APP_VERSION=1.0.0

# .env.development (local dev)
VITE_API_BASE_URL=http://localhost:8000/api
VITE_GOOGLE_CLIENT_ID=dev_client_id

# .env.production (production build)
VITE_API_BASE_URL=https://api.myshop.com/api
VITE_GOOGLE_CLIENT_ID=prod_client_id

# .env.local (never commit — secrets)
VITE_STRIPE_PUBLIC_KEY=pk_test_...
```

```jsx
// ⚠️ VITE_ prefix REQUIRED — otherwise not exposed to client
// ⚠️ Never put SECRET keys here — client-side is public!

// Usage in code
const apiUrl = import.meta.env.VITE_API_BASE_URL;
const appName = import.meta.env.VITE_APP_NAME;
const isDev = import.meta.env.DEV;         // built-in
const isProd = import.meta.env.PROD;       // built-in
const mode = import.meta.env.MODE;         // 'development' | 'production'
```

**Config Object Pattern:**
```jsx
// config/app.js — centralized config
const config = {
  api: {
    baseUrl: import.meta.env.VITE_API_BASE_URL,
    timeout: 15000,
    version: 'v1',
  },
  auth: {
    googleClientId: import.meta.env.VITE_GOOGLE_CLIENT_ID,
    tokenKey: 'access_token',
  },
  app: {
    name: import.meta.env.VITE_APP_NAME || 'App',
    version: import.meta.env.VITE_APP_VERSION || '1.0.0',
    isDev: import.meta.env.DEV,
  },
  features: {
    googleLogin: !!import.meta.env.VITE_GOOGLE_CLIENT_ID,
    analytics: import.meta.env.PROD,
  },
};

export default config;
```

**.gitignore:**
```
# Always ignore these!
.env.local
.env.*.local
.env.production   # Production secrets
```

---

<a id="p9-security"></a>

## 10. Security Best Practices

**XSS (Cross-Site Scripting) Prevention:**
```jsx
// ❌ Dangerous — never do this
function Comment({ comment }) {
  return (
    <div dangerouslySetInnerHTML={{ __html: comment.content }} />
    // Attacker can inject: <script>steal(document.cookie)</script>
  );
}

// ✅ React auto-escapes — use text content
function Comment({ comment }) {
  return <div>{comment.content}</div>;  // Safe — JSX escapes HTML
}

// ✅ If you MUST render HTML — sanitize first
import DOMPurify from 'dompurify';

function RichContent({ html }) {
  const clean = DOMPurify.sanitize(html, {
    ALLOWED_TAGS: ['p', 'b', 'i', 'em', 'strong', 'a', 'ul', 'ol', 'li'],
    ALLOWED_ATTR: ['href', 'target'],
  });
  return <div dangerouslySetInnerHTML={{ __html: clean }} />;
}
```

**CSRF Prevention:**
```jsx
// httpOnly cookie-তে token থাকলে CSRF risk আছে
// Solution: CSRF token (double submit cookie pattern)

api.interceptors.request.use((config) => {
  // CSRF token header
  const csrfToken = document.cookie
    .split('; ')
    .find(r => r.startsWith('csrf_token='))
    ?.split('=')[1];

  if (csrfToken) {
    config.headers['X-CSRF-Token'] = csrfToken;
  }
  return config;
});
```

**Input Sanitization:**
```jsx
// URL-এ user input — never trust!
function SearchPage() {
  const [searchParams] = useSearchParams();
  const query = searchParams.get('q') || '';

  // ✅ Use as text only — not in dangerouslySetInnerHTML
  // ✅ Encode when sending to API
  const encoded = encodeURIComponent(query);

  // ❌ Never use in eval, Function(), or innerHTML
}
```

**Security Checklist:**
```
✅ Tokens: accessToken in memory, refreshToken in httpOnly cookie
✅ HTTPS: Always in production (API + frontend)
✅ Input: Sanitize with DOMPurify before dangerouslySetInnerHTML
✅ CSP: Content Security Policy header (server-side)
✅ Dependencies: npm audit regularly, update packages
✅ Env vars: Secrets never in VITE_ (client-side) variables
✅ Error messages: Don't expose stack traces to client
✅ Auth endpoints: Rate limiting (server-side)
✅ Sensitive routes: Server-side permission check too (never trust client)
✅ Logout: Clear tokens + invalidate server session
```

---

## PART 9 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Say |
|---|---|---|
| JWT | Header.Payload.Signature | `exp` check করো |
| Token storage | accessToken memory, refreshToken httpOnly | localStorage = XSS risk |
| AuthContext | `isLoading` initial check | Silent refresh on mount |
| Protected Route | `<Navigate state={{from}}` | Redirect back after login |
| Token refresh | Queue pending requests | `isRefreshing` flag |
| RBAC | Permission map, `Can` component | Server-side check too |
| OAuth | Code → backend → JWT | Never exchange code client-side |
| RHF + Zod | `zodResolver`, `setError` | `mode: 'onChange'` |
| Env vars | `VITE_` prefix, never secrets | `.env.local` gitignore |
| Security | XSS: DOMPurify, CSRF: X-CSRF-Token | Server validates too |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part10"></a>

## 📋 PART 10 সূচিপত্র — React Projects

| # | Project | Stack | Key Concepts |
|---|---|---|---|
| 1 | [E-Commerce App](#p10-ecommerce) | RTK, React Router, Axios | Cart, Auth, Orders |
| 2 | [Task Management (Kanban)](#p10-kanban) | Context, DnD, localStorage | Drag & Drop, CRUD |
| 3 | [Real-time Chat App](#p10-chat) | Socket.io, React Query | WebSocket, rooms |
| 4 | [Blog Platform](#p10-blog) | RHF, Zod, Rich Editor | CMS, comments, tags |
| 5 | [Dashboard & Analytics](#p10-dashboard) | Recharts, React Query | Charts, data viz |
| 6 | [Job Portal](#p10-jobs) | Search, Filters, Pagination | Multi-filter, saved jobs |
| 7 | [Multi-step Form Wizard](#p10-wizard) | RHF, Zod, Progress | Stepper, validation |

---

<a id="p10-ecommerce"></a>

## 1. E-Commerce App — Full Stack

**Project Structure:**
```
src/
  components/
    layout/     Navbar, Footer, Sidebar
    ui/         Button, Input, Modal, Badge
    product/    ProductCard, ProductGrid, ProductDetail
    cart/       CartDrawer, CartItem, CartSummary
    checkout/   CheckoutForm, OrderSummary, PaymentForm
  pages/
    Home, Products, ProductDetail, Cart,
    Checkout, OrderSuccess, Orders, Profile
    auth/       Login, Register, ForgotPassword
    admin/      Dashboard, Products, Orders, Users
  store/        authSlice, cartSlice, productsSlice
  services/     api, authService, productService, orderService
  hooks/        useProducts, useOrder, usePermission
  context/      AuthContext, ThemeContext
```

**Core Features List:**
```
✅ Auth: Login, Register, JWT, Protected Routes, RBAC
✅ Products: List, Filter, Search, Sort, Detail, Related
✅ Cart: Add/Remove/Update, Persist (Redux Persist)
✅ Checkout: Address, Payment (Stripe/SSLCommerz), Order
✅ Orders: History, Detail, Track status
✅ Admin: Product CRUD, Order management, User list
✅ UI: Dark mode, Responsive, Skeleton loading, Toast
```

**Key Implementation — Product Filter System:**
```jsx
// hooks/useProductFilters.js
function useProductFilters() {
  const [searchParams, setSearchParams] = useSearchParams();

  // URL-based filters — shareable, bookmarkable
  const filters = {
    search: searchParams.get('q') || '',
    category: searchParams.get('category') || '',
    minPrice: Number(searchParams.get('minPrice')) || 0,
    maxPrice: Number(searchParams.get('maxPrice')) || Infinity,
    rating: Number(searchParams.get('rating')) || 0,
    inStock: searchParams.get('inStock') === 'true',
    sortBy: searchParams.get('sort') || 'newest',
    page: Number(searchParams.get('page')) || 1,
  };

  const updateFilter = useCallback((key, value) => {
    setSearchParams(prev => {
      const next = new URLSearchParams(prev);
      if (value === '' || value === null || value === undefined) {
        next.delete(key);
      } else {
        next.set(key, String(value));
      }
      next.set('page', '1');  // Reset pagination on filter change
      return next;
    });
  }, [setSearchParams]);

  const clearFilters = useCallback(() => {
    setSearchParams({});
  }, [setSearchParams]);

  return { filters, updateFilter, clearFilters };
}
```

```jsx
// components/product/FilterSidebar.jsx
function FilterSidebar({ categories }) {
  const { filters, updateFilter, clearFilters } = useProductFilters();
  const hasActiveFilters = filters.category || filters.minPrice || filters.rating;

  return (
    <aside className="filter-sidebar">
      <div className="filter-header">
        <h3>ফিল্টার</h3>
        {hasActiveFilters && (
          <button onClick={clearFilters} className="btn-ghost btn-sm">
            সব মুছুন
          </button>
        )}
      </div>

      {/* Category */}
      <div className="filter-group">
        <h4>ক্যাটাগরি</h4>
        {categories.map(cat => (
          <label key={cat.id} className="filter-option">
            <input
              type="radio"
              name="category"
              value={cat.slug}
              checked={filters.category === cat.slug}
              onChange={e => updateFilter('category', e.target.value)}
            />
            {cat.name} ({cat.count})
          </label>
        ))}
      </div>

      {/* Price Range */}
      <div className="filter-group">
        <h4>মূল্য পরিসর</h4>
        <div className="price-inputs">
          <input
            type="number"
            placeholder="Min ৳"
            value={filters.minPrice || ''}
            onChange={e => updateFilter('minPrice', e.target.value)}
          />
          <span>–</span>
          <input
            type="number"
            placeholder="Max ৳"
            value={filters.maxPrice === Infinity ? '' : filters.maxPrice}
            onChange={e => updateFilter('maxPrice', e.target.value)}
          />
        </div>
      </div>

      {/* Rating */}
      <div className="filter-group">
        <h4>রেটিং</h4>
        {[4, 3, 2, 1].map(star => (
          <label key={star} className="filter-option">
            <input
              type="radio"
              name="rating"
              value={star}
              checked={filters.rating === star}
              onChange={() => updateFilter('rating', star)}
            />
            {'★'.repeat(star)} ও তার বেশি
          </label>
        ))}
      </div>

      {/* In Stock */}
      <div className="filter-group">
        <label className="filter-option">
          <input
            type="checkbox"
            checked={filters.inStock}
            onChange={e => updateFilter('inStock', e.target.checked)}
          />
          Stock-এ আছে শুধু
        </label>
      </div>
    </aside>
  );
}
```

**Checkout Flow:**
```jsx
// pages/Checkout.jsx
function CheckoutPage() {
  const [step, setStep] = useState(1);  // 1:Address, 2:Payment, 3:Review
  const [address, setAddress] = useState(null);
  const cartItems = useSelector(selectCartItems);
  const total = useSelector(selectCartTotal);
  const dispatch = useDispatch();
  const navigate = useNavigate();

  const { mutate: placeOrder, isPending } = useMutation({
    mutationFn: (orderData) => orderService.create(orderData),
    onSuccess: (order) => {
      dispatch(clearCart());
      navigate(`/order-success/${order.id}`);
    },
  });

  const handlePlaceOrder = (paymentData) => {
    placeOrder({
      items: cartItems.map(({ id, qty, price }) => ({ productId: id, qty, price })),
      address,
      payment: paymentData,
      total,
    });
  };

  if (cartItems.length === 0) {
    return <Navigate to="/cart" replace />;
  }

  return (
    <div className="checkout-page">
      <CheckoutStepper current={step} steps={['ঠিকানা', 'পেমেন্ট', 'নিশ্চিত করুন']} />

      <div className="checkout-layout">
        <div className="checkout-main">
          {step === 1 && (
            <AddressForm
              onNext={(addr) => { setAddress(addr); setStep(2); }}
            />
          )}
          {step === 2 && (
            <PaymentForm
              onBack={() => setStep(1)}
              onNext={(payment) => { setStep(3); }}
            />
          )}
          {step === 3 && (
            <OrderReview
              address={address}
              onBack={() => setStep(2)}
              onConfirm={handlePlaceOrder}
              isLoading={isPending}
            />
          )}
        </div>

        <OrderSummary items={cartItems} total={total} />
      </div>
    </div>
  );
}
```

---

<a id="p10-kanban"></a>

## 2. Task Management — Kanban Board

**Core Features:**
```
✅ Columns: Todo, In Progress, Review, Done
✅ Cards: Title, Description, Priority, Assignee, Due date
✅ Drag & Drop: Card reorder, column transfer
✅ CRUD: Add/Edit/Delete cards and columns
✅ Persist: localStorage
✅ Filter: By assignee, priority, due date
```

**Kanban State:**
```jsx
// useKanbanStore.js (Zustand)
import { create } from 'zustand';
import { persist } from 'zustand/middleware';
import { nanoid } from 'nanoid';

const useKanbanStore = create(
  persist(
    (set, get) => ({
      columns: {
        'todo': { id: 'todo', title: '📋 Todo', taskIds: [] },
        'in-progress': { id: 'in-progress', title: '🔄 In Progress', taskIds: [] },
        'review': { id: 'review', title: '👀 Review', taskIds: [] },
        'done': { id: 'done', title: '✅ Done', taskIds: [] },
      },
      columnOrder: ['todo', 'in-progress', 'review', 'done'],
      tasks: {},

      addTask: (columnId, taskData) => set((state) => {
        const id = nanoid();
        return {
          tasks: {
            ...state.tasks,
            [id]: {
              id, ...taskData,
              priority: taskData.priority || 'medium',
              createdAt: new Date().toISOString(),
            },
          },
          columns: {
            ...state.columns,
            [columnId]: {
              ...state.columns[columnId],
              taskIds: [...state.columns[columnId].taskIds, id],
            },
          },
        };
      }),

      moveTask: (taskId, fromColumn, toColumn, toIndex) => set((state) => {
        const from = state.columns[fromColumn];
        const to = state.columns[toColumn];

        const fromIds = from.taskIds.filter(id => id !== taskId);
        const toIds = [...to.taskIds];
        toIds.splice(toIndex, 0, taskId);

        return {
          columns: {
            ...state.columns,
            [fromColumn]: { ...from, taskIds: fromIds },
            [toColumn]: { ...to, taskIds: toIds },
          },
        };
      }),

      deleteTask: (taskId, columnId) => set((state) => {
        const { [taskId]: removed, ...remainingTasks } = state.tasks;
        return {
          tasks: remainingTasks,
          columns: {
            ...state.columns,
            [columnId]: {
              ...state.columns[columnId],
              taskIds: state.columns[columnId].taskIds.filter(id => id !== taskId),
            },
          },
        };
      }),
    }),
    { name: 'kanban-board' }
  )
);
```

**Drag & Drop (react-beautiful-dnd / @dnd-kit):**
```jsx
// npm install @dnd-kit/core @dnd-kit/sortable
import {
  DndContext, DragOverlay,
  PointerSensor, useSensor, useSensors,
  closestCorners,
} from '@dnd-kit/core';

function KanbanBoard() {
  const { columns, columnOrder, tasks, moveTask } = useKanbanStore();
  const [activeTask, setActiveTask] = useState(null);

  const sensors = useSensors(
    useSensor(PointerSensor, {
      activationConstraint: { distance: 5 },  // 5px drag to start
    })
  );

  const handleDragStart = ({ active }) => {
    setActiveTask(tasks[active.id]);
  };

  const handleDragEnd = ({ active, over }) => {
    setActiveTask(null);
    if (!over) return;

    const taskId = active.id;
    const targetColumnId = over.id;

    // Find source column
    const sourceColumnId = columnOrder.find(colId =>
      columns[colId].taskIds.includes(taskId)
    );

    if (sourceColumnId && targetColumnId !== sourceColumnId) {
      const toIndex = columns[targetColumnId].taskIds.length;
      moveTask(taskId, sourceColumnId, targetColumnId, toIndex);
    }
  };

  return (
    <DndContext
      sensors={sensors}
      collisionDetection={closestCorners}
      onDragStart={handleDragStart}
      onDragEnd={handleDragEnd}
    >
      <div className="kanban-board">
        {columnOrder.map(colId => (
          <KanbanColumn
            key={colId}
            column={columns[colId]}
            tasks={columns[colId].taskIds.map(id => tasks[id]).filter(Boolean)}
          />
        ))}
      </div>

      {/* Drag preview */}
      <DragOverlay>
        {activeTask && <TaskCard task={activeTask} isDragging />}
      </DragOverlay>
    </DndContext>
  );
}
```

---

<a id="p10-chat"></a>

## 3. Real-time Chat App

**Core Features:**
```
✅ Rooms: Public channels, Private DMs
✅ Real-time: Socket.io messages
✅ History: React Query for past messages
✅ Typing indicators
✅ Online presence
✅ Message reactions, read receipts
```

**Socket.io Integration:**
```jsx
// hooks/useSocket.js
import { useEffect, useRef } from 'react';
import { io } from 'socket.io-client';
import { useAuth } from '../context/AuthContext';

let socket = null;

export function useSocket() {
  const { token } = useAuth();

  useEffect(() => {
    if (!token) return;

    socket = io(import.meta.env.VITE_WS_URL, {
      auth: { token },
      transports: ['websocket'],
      reconnection: true,
      reconnectionDelay: 1000,
      reconnectionAttempts: 5,
    });

    socket.on('connect', () => console.log('Socket connected'));
    socket.on('connect_error', (err) => console.error('Socket error:', err.message));

    return () => {
      socket?.disconnect();
      socket = null;
    };
  }, [token]);

  return socket;
}
```

```jsx
// pages/ChatRoom.jsx
function ChatRoom({ roomId }) {
  const socket = useSocket();
  const { user } = useAuth();
  const [messages, setMessages] = useState([]);
  const [typingUsers, setTypingUsers] = useState([]);
  const [newMessage, setNewMessage] = useState('');
  const bottomRef = useRef(null);
  const typingTimeoutRef = useRef(null);

  // Load history with React Query
  const { data: history } = useQuery({
    queryKey: ['messages', roomId],
    queryFn: () => chatService.getMessages(roomId, { limit: 50 }),
  });

  useEffect(() => {
    if (history) setMessages(history.messages);
  }, [history]);

  // Socket listeners
  useEffect(() => {
    if (!socket) return;

    socket.emit('room:join', roomId);

    socket.on('message:new', (msg) => {
      setMessages(prev => [...prev, msg]);
    });

    socket.on('typing:start', ({ userId, name }) => {
      if (userId !== user.id) {
        setTypingUsers(prev => [...new Set([...prev, name])]);
      }
    });

    socket.on('typing:stop', ({ userId, name }) => {
      setTypingUsers(prev => prev.filter(n => n !== name));
    });

    return () => {
      socket.emit('room:leave', roomId);
      socket.off('message:new');
      socket.off('typing:start');
      socket.off('typing:stop');
    };
  }, [socket, roomId, user.id]);

  // Auto scroll
  useEffect(() => {
    bottomRef.current?.scrollIntoView({ behavior: 'smooth' });
  }, [messages]);

  const handleTyping = () => {
    socket?.emit('typing:start', { roomId });
    clearTimeout(typingTimeoutRef.current);
    typingTimeoutRef.current = setTimeout(() => {
      socket?.emit('typing:stop', { roomId });
    }, 1500);
  };

  const sendMessage = (e) => {
    e.preventDefault();
    if (!newMessage.trim() || !socket) return;

    socket.emit('message:send', {
      roomId,
      content: newMessage.trim(),
    });

    setNewMessage('');
    socket.emit('typing:stop', { roomId });
  };

  return (
    <div className="chat-room">
      <div className="messages-container">
        {messages.map(msg => (
          <MessageBubble
            key={msg.id}
            message={msg}
            isOwn={msg.senderId === user.id}
          />
        ))}
        {typingUsers.length > 0 && (
          <div className="typing-indicator">
            {typingUsers.join(', ')} typing...
          </div>
        )}
        <div ref={bottomRef} />
      </div>

      <form onSubmit={sendMessage} className="message-input-bar">
        <input
          value={newMessage}
          onChange={e => { setNewMessage(e.target.value); handleTyping(); }}
          placeholder="Message লিখুন..."
          autoComplete="off"
        />
        <button type="submit" disabled={!newMessage.trim()}>Send ➤</button>
      </form>
    </div>
  );
}
```

---

<a id="p10-dashboard"></a>

## 4. Dashboard & Analytics

**Core Features:**
```
✅ KPI Cards: Revenue, Orders, Users, Conversion
✅ Charts: Line (sales trend), Bar (category), Pie (traffic)
✅ Date range picker: Last 7d, 30d, 90d, Custom
✅ Data table: Sortable, filterable, exportable
✅ Real-time: WebSocket or polling
```

**Dashboard Layout:**
```jsx
// npm install recharts
import {
  LineChart, Line, BarChart, Bar,
  PieChart, Pie, Cell,
  XAxis, YAxis, CartesianGrid, Tooltip, Legend,
  ResponsiveContainer,
} from 'recharts';

function SalesTrendChart({ data }) {
  return (
    <div className="chart-card">
      <h3>Sales Trend</h3>
      <ResponsiveContainer width="100%" height={300}>
        <LineChart data={data}>
          <CartesianGrid strokeDasharray="3 3" />
          <XAxis dataKey="date" tickFormatter={d => format(new Date(d), 'MMM d')} />
          <YAxis tickFormatter={v => `৳${(v/1000).toFixed(0)}k`} />
          <Tooltip formatter={(v) => [`৳${v.toLocaleString()}`, 'Revenue']} />
          <Legend />
          <Line
            type="monotone"
            dataKey="revenue"
            stroke="#6366f1"
            strokeWidth={2}
            dot={false}
            name="Revenue"
          />
          <Line
            type="monotone"
            dataKey="orders"
            stroke="#22c55e"
            strokeWidth={2}
            dot={false}
            name="Orders"
            yAxisId="right"
          />
        </LineChart>
      </ResponsiveContainer>
    </div>
  );
}

function KPICard({ title, value, change, icon, color }) {
  const isPositive = change >= 0;
  return (
    <div className={`kpi-card kpi-${color}`}>
      <div className="kpi-icon">{icon}</div>
      <div className="kpi-content">
        <p className="kpi-title">{title}</p>
        <p className="kpi-value">{value}</p>
        <p className={`kpi-change ${isPositive ? 'positive' : 'negative'}`}>
          {isPositive ? '↑' : '↓'} {Math.abs(change)}% vs last period
        </p>
      </div>
    </div>
  );
}

function AdminDashboard() {
  const [dateRange, setDateRange] = useState('30d');

  const { data: stats } = useQuery({
    queryKey: ['dashboard', dateRange],
    queryFn: () => analyticsService.getStats(dateRange),
    refetchInterval: 60000,   // Auto-refresh every minute
  });

  return (
    <div className="dashboard">
      <DashboardHeader dateRange={dateRange} onRangeChange={setDateRange} />

      <div className="kpi-grid">
        <KPICard title="মোট আয়" value={`৳${stats?.revenue?.toLocaleString()}`} change={stats?.revenueChange} icon="💰" color="purple" />
        <KPICard title="Orders" value={stats?.orders} change={stats?.ordersChange} icon="📦" color="blue" />
        <KPICard title="নতুন Users" value={stats?.newUsers} change={stats?.usersChange} icon="👥" color="green" />
        <KPICard title="Conversion" value={`${stats?.conversion}%`} change={stats?.conversionChange} icon="📈" color="orange" />
      </div>

      <div className="charts-grid">
        <SalesTrendChart data={stats?.trend || []} />
        <CategoryPieChart data={stats?.categories || []} />
      </div>

      <RecentOrdersTable />
    </div>
  );
}
```

---

<a id="p10-jobs"></a>

## 5. Job Portal

**Core Features:**
```
✅ Job listings: Filter by type, location, salary, tech stack
✅ Job detail: Description, requirements, company info
✅ Apply: Resume upload, cover letter
✅ Saved jobs: Bookmark, track applications
✅ Company profiles
✅ Search: Full-text, debounced
```

**Job Search with Multi-Filter:**
```jsx
function JobListingPage() {
  const { filters, updateFilter, clearFilters } = useJobFilters();
  const debouncedSearch = useDebounce(filters.search, 400);

  const { data, isLoading, fetchNextPage, hasNextPage } = useInfiniteQuery({
    queryKey: ['jobs', { ...filters, search: debouncedSearch }],
    queryFn: ({ pageParam = 1 }) =>
      jobService.getAll({ ...filters, search: debouncedSearch, page: pageParam }),
    getNextPageParam: (last) => last.hasMore ? last.nextPage : undefined,
  });

  const jobs = data?.pages.flatMap(p => p.jobs) || [];

  return (
    <div className="job-portal">
      {/* Search bar */}
      <div className="search-hero">
        <input
          value={filters.search}
          onChange={e => updateFilter('search', e.target.value)}
          placeholder="Job title, skill, company..."
          className="search-input-lg"
        />
        <input
          value={filters.location}
          onChange={e => updateFilter('location', e.target.value)}
          placeholder="Location (Dhaka, Remote...)"
        />
      </div>

      <div className="job-layout">
        {/* Filters */}
        <aside className="job-filters">
          <MultiSelect
            label="Job Type"
            options={['Full-time', 'Part-time', 'Remote', 'Contract', 'Internship']}
            selected={filters.types}
            onChange={v => updateFilter('types', v)}
          />
          <MultiSelect
            label="Tech Stack"
            options={['React', 'Node.js', 'Python', 'Laravel', 'Django', 'Vue']}
            selected={filters.skills}
            onChange={v => updateFilter('skills', v)}
          />
          <RangeSlider
            label="Salary (৳/month)"
            min={0} max={200000}
            value={[filters.minSalary, filters.maxSalary]}
            onChange={([min, max]) => {
              updateFilter('minSalary', min);
              updateFilter('maxSalary', max);
            }}
          />
        </aside>

        {/* Job list */}
        <main className="job-list">
          {isLoading
            ? Array.from({ length: 5 }, (_, i) => <JobCardSkeleton key={i} />)
            : jobs.map(job => <JobCard key={job.id} job={job} />)
          }
          {hasNextPage && (
            <button onClick={() => fetchNextPage()} className="load-more">
              আরও দেখুন
            </button>
          )}
        </main>
      </div>
    </div>
  );
}
```

---

<a id="p10-blog"></a>

## 6. Blog Platform

**Core Features:**
```
✅ Posts: List, Detail, Categories, Tags
✅ Editor: Rich text (Tiptap/Quill)
✅ Comments: Nested, pagination
✅ Author: Profile, post history
✅ SEO: Meta tags, OG tags
✅ Auth: Login to comment/write
```

**Blog Post Detail:**
```jsx
function BlogPostPage() {
  const { slug } = useParams();

  const { data: post } = useQuery({
    queryKey: ['post', slug],
    queryFn: () => blogService.getBySlug(slug),
  });

  const { data: comments } = useQuery({
    queryKey: ['comments', post?.id],
    queryFn: () => blogService.getComments(post.id),
    enabled: !!post?.id,
  });

  // SEO meta tags
  useEffect(() => {
    if (post) {
      document.title = `${post.title} | MyBlog`;
      document.querySelector('meta[name="description"]')
        ?.setAttribute('content', post.excerpt);
    }
  }, [post]);

  if (!post) return <PostSkeleton />;

  return (
    <article className="blog-post">
      <header className="post-header">
        <div className="post-meta">
          <CategoryBadge category={post.category} />
          <time>{format(new Date(post.publishedAt), 'MMMM d, yyyy')}</time>
          <span>{post.readTime} min read</span>
        </div>
        <h1>{post.title}</h1>
        <p className="post-excerpt">{post.excerpt}</p>
        <AuthorCard author={post.author} />
        <img src={post.coverImage} alt={post.title} className="post-cover" />
      </header>

      <div
        className="post-content prose"
        dangerouslySetInnerHTML={{ __html: DOMPurify.sanitize(post.content) }}
      />

      <footer className="post-footer">
        <TagList tags={post.tags} />
        <SocialShare post={post} />
      </footer>

      <CommentSection postId={post.id} comments={comments} />
      <RelatedPosts currentPost={post} />
    </article>
  );
}
```

---

<a id="p10-wizard"></a>

## 7. Multi-step Form Wizard

**Core Features:**
```
✅ Steps: Progress bar, step validation before next
✅ Navigation: Back/Next, direct step click
✅ Persist: Step data survives component unmount
✅ Review: Final confirmation step
✅ Submit: With loading, success, error states
```

**Form Wizard Implementation:**
```jsx
// Multi-step — each step has its own Zod schema
const step1Schema = z.object({
  firstName: z.string().min(2, 'নাম কমপক্ষে ২ অক্ষর'),
  lastName: z.string().min(2),
  email: z.string().email('সঠিক email দিন'),
  phone: z.string().regex(/^01[3-9]\d{8}$/, 'সঠিক মোবাইল নম্বর'),
});

const step2Schema = z.object({
  division: z.string().min(1, 'বিভাগ নির্বাচন করুন'),
  district: z.string().min(1, 'জেলা নির্বাচন করুন'),
  address: z.string().min(10, 'সম্পূর্ণ ঠিকানা লিখুন'),
  postalCode: z.string().regex(/^\d{4}$/, '৪ সংখ্যার postal code'),
});

const step3Schema = z.object({
  occupation: z.string().min(1),
  experience: z.string().min(1),
  skills: z.array(z.string()).min(1, 'কমপক্ষে একটি skill'),
  bio: z.string().max(500),
});

const schemas = [null, step1Schema, step2Schema, step3Schema];

function useFormWizard(totalSteps) {
  const [currentStep, setCurrentStep] = useState(1);
  const [formData, setFormData] = useState({});
  const [completedSteps, setCompletedSteps] = useState(new Set());

  const goNext = (stepData) => {
    setFormData(prev => ({ ...prev, ...stepData }));
    setCompletedSteps(prev => new Set([...prev, currentStep]));
    if (currentStep < totalSteps) setCurrentStep(s => s + 1);
  };

  const goBack = () => {
    if (currentStep > 1) setCurrentStep(s => s - 1);
  };

  const goToStep = (step) => {
    if (completedSteps.has(step - 1) || step <= currentStep) {
      setCurrentStep(step);
    }
  };

  return {
    currentStep, formData, completedSteps,
    goNext, goBack, goToStep,
    isFirstStep: currentStep === 1,
    isLastStep: currentStep === totalSteps,
  };
}

function MultiStepForm() {
  const wizard = useFormWizard(4);  // 4 steps including review
  const { mutate: submitForm, isPending } = useMutation({
    mutationFn: (data) => userService.createProfile(data),
    onSuccess: () => navigate('/dashboard?welcome=true'),
  });

  const STEPS = [
    { label: 'ব্যক্তিগত তথ্য', icon: '👤' },
    { label: 'ঠিকানা', icon: '📍' },
    { label: 'পেশাদার তথ্য', icon: '💼' },
    { label: 'নিশ্চিত করুন', icon: '✅' },
  ];

  return (
    <div className="wizard-container">
      {/* Progress stepper */}
      <div className="stepper">
        {STEPS.map((step, i) => {
          const stepNum = i + 1;
          const isDone = wizard.completedSteps.has(stepNum);
          const isCurrent = wizard.currentStep === stepNum;

          return (
            <button
              key={stepNum}
              onClick={() => wizard.goToStep(stepNum)}
              className={`step ${isDone ? 'done' : ''} ${isCurrent ? 'current' : ''}`}
              disabled={!isDone && stepNum > wizard.currentStep}
            >
              <span className="step-icon">{isDone ? '✓' : step.icon}</span>
              <span className="step-label">{step.label}</span>
              {stepNum < STEPS.length && <div className="step-connector" />}
            </button>
          );
        })}
      </div>

      {/* Step content */}
      <div className="step-content">
        {wizard.currentStep === 1 && (
          <PersonalInfoStep
            defaultValues={wizard.formData}
            onNext={wizard.goNext}
          />
        )}
        {wizard.currentStep === 2 && (
          <AddressStep
            defaultValues={wizard.formData}
            onNext={wizard.goNext}
            onBack={wizard.goBack}
          />
        )}
        {wizard.currentStep === 3 && (
          <ProfessionalStep
            defaultValues={wizard.formData}
            onNext={wizard.goNext}
            onBack={wizard.goBack}
          />
        )}
        {wizard.currentStep === 4 && (
          <ReviewStep
            data={wizard.formData}
            onBack={wizard.goBack}
            onSubmit={() => submitForm(wizard.formData)}
            isLoading={isPending}
          />
        )}
      </div>
    </div>
  );
}
```

---

## PART 10 Quick Revision Table

| Project | Key Tech | Must-Mention Feature |
|---|---|---|
| E-Commerce | RTK, Axios, React Router | URL-based filters, Checkout flow |
| Kanban | Zustand, @dnd-kit, localStorage | Drag-drop between columns |
| Chat | Socket.io, React Query | Typing indicator, room join/leave |
| Dashboard | Recharts, React Query | Auto-refresh, KPI cards |
| Job Portal | Infinite scroll, Multi-filter | URL-synced filters, debounce |
| Blog | DOMPurify, SEO meta | Sanitize HTML, nested comments |
| Form Wizard | RHF + Zod per-step, useReducer | Persist data between steps |

---

## Projects Common Interview Points

**1. Interview-এ Project জিজ্ঞেস করলে যা বলবেন:**
```
Project: E-Commerce App

"এটা একটা full-featured e-commerce app যেখানে আমি:
- Redux Toolkit দিয়ে cart + auth state manage করেছি
- Axios instance + interceptor দিয়ে API layer তৈরি করেছি
- JWT + httpOnly cookie দিয়ে secure auth implement করেছি
- React.memo + useCallback দিয়ে product grid optimize করেছি
- URL-based filter system বানিয়েছি যাতে filter share করা যায়
- Code splitting দিয়ে initial bundle 60% কমিয়েছি"
```

**2. Technical Challenge জিজ্ঞেস করলে:**
```
"Cart state persist করতে গিয়ে challenge হয়েছিল —
Page refresh-এ cart হারিয়ে যাচ্ছিল।
Redux Persist দিয়ে localStorage-এ cart serialize করে solve করেছি।
আবার sensitive auth data persist করিনি — শুধু cart।"
```

**3. কোনটা কেন chose করলেন:**
```
"Zustand না নিয়ে Redux Toolkit নিলাম কারণ:
- Team project — DevTools + time-travel debugging দরকার
- Complex async (API) operations আছে — createAsyncThunk helpful
- Large codebase — predictable patterns important"
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 11 — Interview Questions Bank

---

<a id="part11"></a>
## PART 11: Interview Questions Bank

> 150+ curated questions — Theoretical, Coding, Tricky, এবং Bangladeshi company patterns। Junior থেকে Mid-level সব level cover করা হয়েছে।

| # | বিষয় |
|---|-------|
| 1 | [Fundamentals Q&A](#p11-fundamentals) |
| 2 | [React Hooks Q&A](#p11-hooks) |
| 3 | [State Management Q&A](#p11-state) |
| 4 | [Performance Q&A](#p11-perf) |
| 5 | [Advanced Topics Q&A](#p11-advanced) |
| 6 | [Coding Challenges](#p11-coding) |
| 7 | [Tricky Questions](#p11-tricky) |
| 8 | [BD Company Interview Patterns](#p11-bd) |

---

<a id="p11-fundamentals"></a>
**Section A: React Fundamentals — Theoretical Q&A**

---

**Q1: React কী এবং এটা কীভাবে কাজ করে?**

React হলো Facebook-এর তৈরি একটি JavaScript UI library। এটি component-based architecture ব্যবহার করে — UI-কে ছোট ছোট reusable pieces-এ ভাগ করে। React একটি Virtual DOM maintain করে, state/props পরিবর্তন হলে নতুন Virtual DOM তৈরি করে পুরোনোটির সাথে diff করে (reconciliation), এবং শুধু changed parts-ই real DOM-এ update করে।

**Q2: JSX কী? Browser কি JSX বোঝে?**

JSX (JavaScript XML) হলো JavaScript-এর একটি syntax extension যা HTML-এর মতো দেখতে। Browser সরাসরি JSX বোঝে না — Babel এটিকে `React.createElement()` calls-এ transpile করে। যেমন:
```jsx
// JSX
const el = <h1 className="title">Hello</h1>;

// Transpiled
const el = React.createElement("h1", { className: "title" }, "Hello");
```

**Q3: Virtual DOM কী এবং Real DOM থেকে কীভাবে আলাদা?**

| বিষয় | Real DOM | Virtual DOM |
|------|----------|-------------|
| কোথায় থাকে | Browser memory | JS memory (object) |
| Update speed | ধীর (reflow/repaint) | দ্রুত (in-memory diff) |
| Direct manipulation | হ্যাঁ | না (React করে) |
| Re-render | পুরো tree | শুধু changed nodes |

Virtual DOM React-এর একটি in-memory JavaScript object representation। State change হলে React নতুন Virtual DOM তৈরি করে, আগেরটির সাথে compare (diffing) করে, এবং minimal changes-ই real DOM-এ apply করে।

**Q4: Reconciliation কী?**

Reconciliation হলো React-এর প্রক্রিয়া যেখানে সে নির্ধারণ করে কোন DOM changes দরকার। React দুটি Virtual DOM tree compare করে:
- Same type element → props update করে
- Different type element → পুরো subtree unmount+remount করে
- Lists → `key` prop দিয়ে identify করে

**Q5: Props vs State পার্থক্য কী?**

| | Props | State |
|--|-------|-------|
| কে নিয়ন্ত্রণ করে | Parent component | Component নিজে |
| Mutable? | না (read-only) | হ্যাঁ (setter দিয়ে) |
| Re-render trigger | Parent re-render করলে | setState call-এ |
| কোথায় defined | Parent-এ | Component-এ |

**Q6: Component কত ধরনের?**

**Functional Component:**
```jsx
function Greeting({ name }) {
  return <h1>Hello, {name}</h1>;
}
```
**Class Component (legacy):**
```jsx
class Greeting extends React.Component {
  render() { return <h1>Hello, {this.props.name}</h1>; }
}
```
আধুনিক React-এ সবসময় Functional Component ব্যবহার করুন।

**Q7: key prop কেন দরকার?**

React list render করার সময় প্রতিটি item-কে uniquely identify করতে `key` ব্যবহার করে। Key ছাড়া React ভুলভাবে elements reuse করতে পারে:
```jsx
// ✅ সঠিক — stable unique id
items.map(item => <Item key={item.id} data={item} />)

// ❌ ভুল — index as key (sort/delete-এ bug হয়)
items.map((item, i) => <Item key={i} data={item} />)
```

**Q8: Controlled vs Uncontrolled Component কী?**

**Controlled:** Form value React state-এ থাকে, React সব কিছু control করে।
```jsx
const [val, setVal] = useState('');
<input value={val} onChange={e => setVal(e.target.value)} />
```
**Uncontrolled:** DOM নিজে value রাখে, React ref দিয়ে পড়ে।
```jsx
const ref = useRef();
<input ref={ref} defaultValue="hello" />
```
Controlled preferred — validation, formatting সহজ।

**Q9: React.Fragment কেন ব্যবহার করি?**

JSX-এ একটি root element থাকতে হয়। Extra `<div>` avoid করতে Fragment ব্যবহার করি:
```jsx
// Extra div add করে
return <div><h1>Title</h1><p>Body</p></div>;

// Fragment — no extra DOM node
return <><h1>Title</h1><p>Body</p></>;
// বা: <React.Fragment key={id}>...</React.Fragment>
```

**Q10: Lifting State Up কী?**

দুটি sibling component-এর মধ্যে shared state থাকলে সেই state-কে তাদের common parent-এ নিয়ে যাওয়াকে lifting state up বলে:
```jsx
// Parent holds shared state
function Parent() {
  const [count, setCount] = useState(0);
  return (
    <>
      <Display count={count} />
      <Counter onIncrement={() => setCount(c => c + 1)} />
    </>
  );
}
```

**Q11: React-এ event handling কীভাবে কাজ করে?**

React synthetic events ব্যবহার করে — cross-browser consistent। Event names camelCase:
```jsx
// HTML: onclick="handleClick()"
// React: onClick={handleClick}
function Button() {
  const handleClick = (e) => {
    e.preventDefault(); // default behavior বন্ধ
    e.stopPropagation(); // bubbling বন্ধ
    console.log('clicked');
  };
  return <button onClick={handleClick}>Click</button>;
}
```

**Q12: Conditional Rendering কতভাবে করা যায়?**

```jsx
// 1. if-else
if (isLoggedIn) return <Dashboard />;
return <Login />;

// 2. Ternary
return isLoggedIn ? <Dashboard /> : <Login />;

// 3. && (short-circuit) — false হলে কিছু render হয় না
return isLoggedIn && <Dashboard />;

// 4. Switch case (multiple conditions)
switch(role) {
  case 'admin': return <AdminPanel />;
  case 'user': return <UserPanel />;
  default: return <GuestPanel />;
}
```

**Q13: React.StrictMode কী করে?**

Development-এ double-invoke করে lifecycle methods এবং state initializers — side effects detect করতে। Production-এ কোনো effect নেই। `useEffect` দুইবার run হওয়া StrictMode-এর কারণ।

**Q14: Component কখন re-render হয়?**

1. `setState` বা `useState` setter call হলে
2. Parent component re-render হলে
3. `useContext` এর value পরিবর্তন হলে
4. `forceUpdate()` call হলে (class component)

**Q15: Pure Component কী?**

Same props/state দিলে same output দেয় এবং side effects নেই। `React.memo` দিয়ে functional component-কে memoize করা যায়:
```jsx
const Pure = React.memo(({ value }) => <div>{value}</div>);
```

---

<a id="p11-hooks"></a>
**Section B: React Hooks Q&A**

---

**Q16: Hooks কী এবং কেন আনা হয়েছে?**

Hooks হলো React 16.8-এ আসা functions যা functional component-এ state ও lifecycle features ব্যবহার করতে দেয়। Class component-এর `this` binding, HOC hell, এবং logic reuse সমস্যা সমাধানের জন্য।

**Q17: useState-এর lazy initialization কী?**

Initial state হিসেবে function দিলে শুধু প্রথম render-এ call হয়:
```jsx
// ❌ প্রতি render-এ expensiveCalc() call হয়
const [state, setState] = useState(expensiveCalc());

// ✅ শুধু প্রথম render-এ
const [state, setState] = useState(() => expensiveCalc());
```

**Q18: useEffect-এর dependency array না দিলে কী হয়?**

```jsx
useEffect(() => { ... });          // প্রতি render-এ চলে
useEffect(() => { ... }, []);      // শুধু mount-এ চলে
useEffect(() => { ... }, [id]);    // id পরিবর্তনে চলে
```
Cleanup function return করলে unmount বা next run-এর আগে call হয়।

**Q19: useRef vs useState পার্থক্য কী?**

| | useRef | useState |
|--|--------|----------|
| Re-render trigger | না | হ্যাঁ |
| Value persist | হ্যাঁ | হ্যাঁ |
| Use case | DOM access, timer | UI state |

```jsx
const count = useRef(0); // render না করে count track
count.current++;         // directly mutate
```

**Q20: Custom Hook কী? Rules কী?**

Custom Hook হলো `use` দিয়ে শুরু হওয়া function যা অন্য hooks ব্যবহার করে। Rules:
1. শুধু top level-এ call করুন (loop/condition-এ না)
2. শুধু React function-এ call করুন
3. নাম `use` দিয়ে শুরু করতে হবে

```jsx
function useWindowSize() {
  const [size, setSize] = useState({ w: window.innerWidth, h: window.innerHeight });
  useEffect(() => {
    const handler = () => setSize({ w: window.innerWidth, h: window.innerHeight });
    window.addEventListener('resize', handler);
    return () => window.removeEventListener('resize', handler);
  }, []);
  return size;
}
```

**Q21: useMemo vs useCallback পার্থক্য কী?**

```jsx
// useMemo — value memoize করে
const sorted = useMemo(() => items.sort(), [items]);

// useCallback — function memoize করে
const handleClick = useCallback(() => doSomething(id), [id]);
```
`useCallback(fn, deps)` === `useMemo(() => fn, deps)`

**Q22: useReducer কখন useState-এর চেয়ে ভালো?**

- Complex state logic (multiple sub-values)
- Next state depends on previous state
- Testing সহজ — pure reducer function

```jsx
const initialState = { count: 0, error: null, loading: false };
function reducer(state, action) {
  switch (action.type) {
    case 'increment': return { ...state, count: state.count + 1 };
    case 'reset': return initialState;
    default: return state;
  }
}
const [state, dispatch] = useReducer(reducer, initialState);
dispatch({ type: 'increment' });
```

**Q23: useContext কীভাবে কাজ করে? Performance issue কী?**

Context value change হলে সব `useContext` consumer re-render হয়। Solution:
```jsx
// ✅ Context split করুন
const ThemeContext = createContext(null);
const UserContext = createContext(null);

// Context-এ value memo করুন
const value = useMemo(() => ({ theme, setTheme }), [theme]);
<ThemeContext.Provider value={value}>
```

**Q24: useLayoutEffect vs useEffect পার্থক্য?**

| | useEffect | useLayoutEffect |
|--|-----------|-----------------|
| কখন চলে | Paint-এর পরে (async) | Paint-এর আগে (sync) |
| Use case | API calls, subscriptions | DOM measurement, tooltip position |
| Performance | ভালো | Block করে (সতর্কে ব্যবহার) |

**Q25: Hooks rules কেন enforce করতে হয়?**

React hooks call order-এর উপর নির্ভর করে internal state track করে। Conditional বা loop-এ hook call করলে order change হয় এবং wrong state এর সাথে map হয়:
```jsx
// ❌ Bug — render-এ হয়তো skip হবে
if (condition) {
  const [val, setVal] = useState(0); // hooks rules violation
}
```

---

<a id="p11-state"></a>
**Section C: State Management Q&A**

---

**Q26: Context API vs Redux কখন কোনটা ব্যবহার করব?**

| | Context API | Redux Toolkit |
|--|------------|---------------|
| Complexity | Simple | Medium-High |
| DevTools | না | হ্যাঁ (time-travel) |
| Middleware | না | হ্যাঁ (thunk, saga) |
| Performance | Context split করতে হয় | Selector-based |
| Team size | Small | Large |

Rule of thumb: Theme, Auth-এর মতো infrequently changing data → Context। Complex async, large app → Redux।

**Q27: Redux-এর 3টি মূল নীতি কী?**

1. **Single source of truth:** পুরো app state একটি store-এ
2. **State is read-only:** শুধু action dispatch করে change করা যায়
3. **Changes via pure reducers:** Reducer = `(state, action) => newState`

**Q28: Redux Toolkit-এ createSlice কী করে?**

`createSlice` একসাথে reducer, actions, এবং action creators তৈরি করে। Immer internally ব্যবহার করে তাই mutable syntax লেখা যায়:
```jsx
const counterSlice = createSlice({
  name: 'counter',
  initialState: { value: 0 },
  reducers: {
    increment: state => { state.value += 1; }, // Immer handle করে
    addBy: (state, action) => { state.value += action.payload; }
  }
});
export const { increment, addBy } = counterSlice.actions;
```

**Q29: Zustand vs Redux পার্থক্য কী?**

Zustand অনেক হালকা এবং boilerplate-free:
```jsx
// Zustand — মাত্র কয়েক লাইন
const useStore = create(set => ({
  count: 0,
  increment: () => set(state => ({ count: state.count + 1 }))
}));
```
Small-medium app-এ Zustand, large enterprise-এ Redux Toolkit prefer করুন।

**Q30: Prop Drilling কী এবং কীভাবে এড়াবেন?**

Prop drilling হলো intermediate components-এর মধ্য দিয়ে props pass করা যারা সেই data actually ব্যবহার করে না। Solutions:
1. Context API
2. Redux / Zustand
3. Component composition (children prop)
4. Render props pattern

---

<a id="p11-perf"></a>
**Section D: Performance Q&A**

---

**Q31: React.memo কীভাবে কাজ করে?**

Parent re-render হলে child-ও re-render হয় — React.memo এটি prevent করে props same থাকলে। Shallow comparison করে by default:
```jsx
const Child = React.memo(({ name, onClick }) => {
  return <button onClick={onClick}>{name}</button>;
}, (prevProps, nextProps) => {
  // true return করলে re-render হবে না
  return prevProps.name === nextProps.name;
});
```

**Q32: Code Splitting কীভাবে করবেন?**

```jsx
import { lazy, Suspense } from 'react';

// Route-based splitting — most effective
const Dashboard = lazy(() => import('./pages/Dashboard'));
const Profile = lazy(() => import('./pages/Profile'));

function App() {
  return (
    <Suspense fallback={<PageSkeleton />}>
      <Routes>
        <Route path="/dashboard" element={<Dashboard />} />
        <Route path="/profile" element={<Profile />} />
      </Routes>
    </Suspense>
  );
}
```

**Q33: List virtualization কী এবং কখন দরকার?**

10,000+ items render করলে DOM-এ একসাথে সব থাকলে browser ধীর হয়। Virtualization শুধু visible items render করে:
```jsx
import { FixedSizeList } from 'react-window';

<FixedSizeList height={600} itemCount={10000} itemSize={50} width="100%">
  {({ index, style }) => <div style={style}>Item {index}</div>}
</FixedSizeList>
```

**Q34: Web Vitals কী? React-এ কীভাবে improve করবেন?**

| Metric | মানে | Target |
|--------|------|--------|
| LCP | Largest Contentful Paint | ≤ 2.5s |
| CLS | Cumulative Layout Shift | ≤ 0.1 |
| INP | Interaction to Next Paint | ≤ 200ms |

React-এ: Code split করুন, Image optimize করুন (width/height দিন), `useTransition` দিয়ে non-urgent updates defer করুন।

**Q35: Bundle size কমাবেন কীভাবে?**

1. Tree shaking — named exports ব্যবহার করুন
2. Dynamic import — `import()` 
3. External CDN for large libs (moment → day.js)
4. Compression (gzip/brotli) Nginx-এ
5. `vite-bundle-visualizer` দিয়ে analyze করুন

---

<a id="p11-advanced"></a>
**Section E: Advanced Topics Q&A**

---

**Q36: Error Boundary কী? Hooks-এ কেন করা যায় না?**

Error Boundary হলো class component যা child-এর render error catch করে fallback দেখায়। `getDerivedStateFromError` এবং `componentDidCatch` lifecycle methods দরকার — এখনো functional equivalent নেই। `react-error-boundary` package সহজ API দেয়:
```jsx
import { ErrorBoundary } from 'react-error-boundary';
<ErrorBoundary fallback={<div>Something went wrong</div>}>
  <RiskyComponent />
</ErrorBoundary>
```

**Q37: Portal কী এবং কোথায় ব্যবহার করবেন?**

Portal দিয়ে child component-কে parent-এর বাইরে অন্য DOM node-এ render করা যায়:
```jsx
import { createPortal } from 'react-dom';

function Modal({ children }) {
  return createPortal(
    <div className="modal">{children}</div>,
    document.getElementById('modal-root')
  );
}
```
Use case: Modal, Tooltip, Dropdown (z-index/overflow issues এড়াতে)।

**Q38: Higher-Order Component (HOC) কী?**

HOC হলো function যা component নেয় এবং enhanced component return করে:
```jsx
function withAuth(Component) {
  return function AuthenticatedComponent(props) {
    const { isLoggedIn } = useAuth();
    if (!isLoggedIn) return <Navigate to="/login" />;
    return <Component {...props} />;
  };
}
const ProtectedDashboard = withAuth(Dashboard);
```

**Q39: Render Props pattern কী?**

Component-এর `render` prop হিসেবে function দিয়ে logic share করা:
```jsx
function MouseTracker({ render }) {
  const [pos, setPos] = useState({ x: 0, y: 0 });
  return (
    <div onMouseMove={e => setPos({ x: e.clientX, y: e.clientY })}>
      {render(pos)}
    </div>
  );
}
// Usage:
<MouseTracker render={({ x, y }) => <p>Mouse at {x}, {y}</p>} />
```
Modern React-এ custom hooks এই pattern replace করেছে।

**Q40: Compound Component pattern কী?**

Related components একসাথে group করার pattern:
```jsx
// Select, Select.Option, Select.Group একসাথে কাজ করে
<Select value={val} onChange={setVal}>
  <Select.Option value="a">Option A</Select.Option>
  <Select.Option value="b">Option B</Select.Option>
</Select>
```
`Context` দিয়ে parent-child এর মধ্যে state share করা হয়।

**Q41: React Fiber কী?**

React 16-তে আসা নতুন reconciliation engine। Fiber-এর মূল বৈশিষ্ট্য:
- **Incremental rendering:** কাজ ছোট units-এ ভাগ করে pause/resume করতে পারে
- **Priority lanes:** High priority updates (user input) আগে process করে
- **Concurrent Mode সম্ভব হয়:** `useTransition`, `useDeferredValue` কাজ করে

**Q42: Strict Mode-এ useEffect দুইবার চলে কেন?**

React 18-এ StrictMode development-এ component mount → unmount → remount করে। এটি intentional — side effects-এর cleanup সঠিক কিনা test করতে। Production-এ হয় না।

---

<a id="p11-coding"></a>
**Section F: Coding Challenges**

---

**Challenge 1: Custom useLocalStorage Hook**
```jsx
function useLocalStorage(key, initialValue) {
  const [value, setValue] = useState(() => {
    try {
      const item = localStorage.getItem(key);
      return item ? JSON.parse(item) : initialValue;
    } catch {
      return initialValue;
    }
  });

  const setStoredValue = useCallback((val) => {
    try {
      const newValue = val instanceof Function ? val(value) : val;
      setValue(newValue);
      localStorage.setItem(key, JSON.stringify(newValue));
    } catch (error) {
      console.error(error);
    }
  }, [key, value]);

  return [value, setStoredValue];
}
```

**Challenge 2: Infinite Scroll with Intersection Observer**
```jsx
function useInfiniteScroll(callback) {
  const observerRef = useRef(null);
  const lastItemRef = useCallback(node => {
    if (observerRef.current) observerRef.current.disconnect();
    observerRef.current = new IntersectionObserver(entries => {
      if (entries[0].isIntersecting) callback();
    });
    if (node) observerRef.current.observe(node);
  }, [callback]);
  return lastItemRef;
}

// Usage:
function PostList() {
  const [posts, setPosts] = useState([]);
  const [page, setPage] = useState(1);
  const loadMore = useCallback(() => setPage(p => p + 1), []);
  const lastRef = useInfiniteScroll(loadMore);
  
  return posts.map((post, i) => (
    <div key={post.id} ref={i === posts.length - 1 ? lastRef : null}>
      {post.title}
    </div>
  ));
}
```

**Challenge 3: Debounce Hook**
```jsx
function useDebounce(value, delay = 300) {
  const [debounced, setDebounced] = useState(value);
  useEffect(() => {
    const timer = setTimeout(() => setDebounced(value), delay);
    return () => clearTimeout(timer);
  }, [value, delay]);
  return debounced;
}
```

**Challenge 4: Shopping Cart Reducer**
```jsx
function cartReducer(state, action) {
  switch (action.type) {
    case 'ADD': {
      const existing = state.find(item => item.id === action.payload.id);
      if (existing) {
        return state.map(item =>
          item.id === action.payload.id
            ? { ...item, qty: item.qty + 1 }
            : item
        );
      }
      return [...state, { ...action.payload, qty: 1 }];
    }
    case 'REMOVE':
      return state.filter(item => item.id !== action.payload);
    case 'UPDATE_QTY':
      return state.map(item =>
        item.id === action.payload.id
          ? { ...item, qty: action.payload.qty }
          : item
      );
    case 'CLEAR':
      return [];
    default:
      return state;
  }
}
```

**Challenge 5: Form Validation without Library**
```jsx
function useForm(initialValues, validate) {
  const [values, setValues] = useState(initialValues);
  const [errors, setErrors] = useState({});
  const [touched, setTouched] = useState({});

  const handleChange = (e) => {
    const { name, value } = e.target;
    setValues(prev => ({ ...prev, [name]: value }));
    if (touched[name]) {
      const err = validate({ ...values, [name]: value });
      setErrors(err);
    }
  };

  const handleBlur = (e) => {
    const { name } = e.target;
    setTouched(prev => ({ ...prev, [name]: true }));
    const err = validate(values);
    setErrors(err);
  };

  const handleSubmit = (onSubmit) => (e) => {
    e.preventDefault();
    const err = validate(values);
    setErrors(err);
    setTouched(Object.keys(initialValues).reduce((acc, k) => ({ ...acc, [k]: true }), {}));
    if (Object.keys(err).length === 0) onSubmit(values);
  };

  return { values, errors, touched, handleChange, handleBlur, handleSubmit };
}
```

**Challenge 6: useAsync Hook**
```jsx
function useAsync(asyncFn, deps = []) {
  const [state, setState] = useState({ data: null, loading: false, error: null });

  useEffect(() => {
    let cancelled = false;
    setState({ data: null, loading: true, error: null });
    asyncFn()
      .then(data => { if (!cancelled) setState({ data, loading: false, error: null }); })
      .catch(error => { if (!cancelled) setState({ data: null, loading: false, error }); });
    return () => { cancelled = true; };
    // eslint-disable-next-line react-hooks/exhaustive-deps
  }, deps);

  return state;
}
```

**Challenge 7: Throttle Hook**
```jsx
function useThrottle(value, limit = 300) {
  const [throttled, setThrottled] = useState(value);
  const lastRan = useRef(Date.now());

  useEffect(() => {
    const handler = setTimeout(() => {
      if (Date.now() - lastRan.current >= limit) {
        setThrottled(value);
        lastRan.current = Date.now();
      }
    }, limit - (Date.now() - lastRan.current));
    return () => clearTimeout(handler);
  }, [value, limit]);

  return throttled;
}
```

---

<a id="p11-tricky"></a>
**Section G: Tricky / Gotcha Questions**

---

**Tricky Q1: এই code-এ কী সমস্যা?**
```jsx
function Counter() {
  const [count, setCount] = useState(0);
  useEffect(() => {
    const id = setInterval(() => {
      setCount(count + 1); // ❌ stale closure!
    }, 1000);
    return () => clearInterval(id);
  }, []); // count নেই dependency-তে
}
```
**সমস্যা:** `count` stale — সবসময় 0 থাকবে।
**Fix:** `setCount(c => c + 1)` (functional update) বা `count` dependency-তে add করুন।

---

**Tricky Q2: কতবার render হবে?**
```jsx
function App() {
  const [a, setA] = useState(0);
  const [b, setB] = useState(0);

  const handleClick = () => {
    setA(1);
    setB(2);
  };
  // handleClick call-এ কতবার re-render?
}
```
**উত্তর:** একবার। React 18-এ automatic batching — event handler-এর সব setState একসাথে process হয়।

---

**Tricky Q3: এই component কি re-render হবে?**
```jsx
const obj = { name: 'Alice' }; // component-এর বাইরে

function App() {
  const [count, setCount] = useState(0);
  return <Child data={obj} />;
}

const Child = React.memo(({ data }) => {
  console.log('Child rendered');
  return <div>{data.name}</div>;
});
```
**উত্তর:** না। `obj` component-এর বাইরে — reference same থাকে। React.memo shallow comparison-এ same reference পাবে।

---

**Tricky Q4: এই code কী print করবে?**
```jsx
function App() {
  const [count, setCount] = useState(0);
  
  const handleClick = () => {
    setCount(count + 1);
    setCount(count + 1);
    setCount(count + 1);
    // count এখন কত হবে?
  };
}
```
**উত্তর:** 1, কারণ তিনটিই `count + 1` = `0 + 1`। Fix: `setCount(c => c + 1)` তিনবার → 3 হবে।

---

**Tricky Q5: useEffect infinite loop কেন হচ্ছে?**
```jsx
function App() {
  const [data, setData] = useState([]);
  
  useEffect(() => {
    fetchData().then(res => setData(res));
  }, [data]); // ❌ data dependency
}
```
**সমস্যা:** setData → data change → useEffect → setData... অনন্ত loop।
**Fix:** `[]` dependency বা `data` remove করুন।

---

**Tricky Q6: key change করলে কী হয়?**
```jsx
<UserForm key={userId} userId={userId} />
```
`key` change হলে React পুরো component unmount করে নতুন instance mount করে — সব state reset হয়। এটি intentional reset করার কৌশল।

---

**Tricky Q7: Event handler-এ `this` কেন undefined হয় (class component)?**
```jsx
class Button extends React.Component {
  handleClick() {
    console.log(this); // undefined!
  }
  render() {
    return <button onClick={this.handleClick}>Click</button>; // ❌
  }
}
```
**Fix:** Arrow function বা constructor-এ bind: `this.handleClick = this.handleClick.bind(this)` বা `handleClick = () => {...}`

---

**Tricky Q8: Suspense boundary-এর বাইরে lazy component throw করলে?**

Error হবে। প্রতিটি lazy component-কে nearest Suspense boundary-র ভেতরে রাখতে হবে। Nested Suspense দিয়ে granular loading states তৈরি করা যায়।

---

**Tricky Q9: useState initial value callback কখন কাজে লাগে?**
```jsx
// ব্যবহার হবে না — প্রতি render-এ JSON.parse() call হয়
const [user, setUser] = useState(JSON.parse(localStorage.getItem('user')));

// ✅ শুধু প্রথম render-এ parse হয়
const [user, setUser] = useState(() => JSON.parse(localStorage.getItem('user')));
```

---

**Tricky Q10: Props drilling vs Context — কোনটা better?**

Context সবসময় better না। Context value change হলে সব consumers re-render হয়। Small component trees-এ prop drilling সহজ এবং explicit। Context ব্যবহার করুন যখন: deep nesting, cross-cutting concerns (theme, auth, i18n)।

---

<a id="p11-bd"></a>
**Section H: Bangladeshi Company Interview Patterns**

---

**Brain Station 23 — Interview Style:**

Focus areas: Problem solving, OOP concepts, React fundamentals, team collaboration।

সাধারণ প্রশ্ন:
- "React-এর কোনো project বানিয়েছেন? সেখানে কী কী challenge face করেছিলেন?"
- "REST API কীভাবে consume করেন React-এ?"
- "Git workflow কী follow করেন?"
- "Agile/Scrum কী? Daily standup কী?"
- Live coding: Simple counter, todo list, API fetch with loading state

**Therap BD — Interview Style:**

Focus: Core CS fundamentals, Java/React hybrid, problem solving capacity।

সাধারণ প্রশ্ন:
- "JavaScript closures explain করুন। React-এ কোথায় দেখেছেন?"
- "Async/await vs Promise chain — কী পার্থক্য?"
- "Component design — কীভাবে reusable component বানাবেন?"
- "Database query optimization জানেন?"
- Algorithm: Array manipulation, string processing

**BJIT Group — Interview Style:**

Focus: Technical depth, React + TypeScript, system thinking।

সাধারণ প্রশ্ন:
- "TypeScript কী? React-এ Props কীভাবে type করবেন?"
- "State management কোনটা prefer করেন এবং কেন?"
- "CORS কী? React-এ এই error কীভাবে handle করেন?"
- "Testing জানেন? Jest/React Testing Library?"
- Project walkthrough: নিজের project explain করতে হবে

**Enosis Solutions — Interview Style:**

Focus: Clean code, best practices, scalable architecture।

সাধারণ প্রশ্ন:
- "SOLID principles explain করুন। React-এ কোথায় apply করেন?"
- "Code review করার সময় কী কী দেখেন?"
- "Performance optimization কীভাবে করেছেন কোনো project-এ?"
- "Micro-frontend কী শুনেছেন?"
- Pair programming session হতে পারে

**Kaz Software / Leads Tech / Sourcecod — Interview Style:**

Focus: Product thinking, quick delivery, communication।

সাধারণ প্রশ্ন:
- "React Router-এ protected route কীভাবে implement করবেন?"
- "JWT authentication flow explain করুন।"
- "Responsive design কীভাবে করেন? Tailwind ব্যবহার করেছেন?"
- "Deadline pressure-এ কীভাবে কাজ করেন?"
- Portfolio project-এর live demo দেখাতে হতে পারে

**Chaldal / Shajgoj / Pathao (Product Companies):**

Focus: Impact, scalability, user experience।

সাধারণ প্রশ্ন:
- "আমাদের app-এর কোন feature improve করবেন? কীভাবে?"
- "1 million user-এর জন্য React app scale করবেন কীভাবে?"
- "A/B testing কী? Feature flag কীভাবে implement করবেন?"
- "Web accessibility (a11y) জানেন?"
- Data-driven decisions, metrics সম্পর্কে জিজ্ঞেস করতে পারে

**Common BD Interview Tips:**

```
✅ বাংলায় explain করতে comfortable থাকুন
✅ নিজের project-এর প্রতিটি line explain করতে পারুন
✅ "আমি জানি না কিন্তু শিখতে পারব" — honest থাকুন
✅ GitHub profile সুন্দর রাখুন (README, contributions)
✅ LeetCode Easy/Medium করুন (Arrays, String, HashMap)
✅ সময়মতো যান, professional থাকুন
✅ Salary expectation জানুন (Junior: 25-45k BDT, market research করুন)
```

---

**PART 11 Quick Revision Table**

| প্রশ্ন | উত্তর (এক লাইনে) |
|--------|-----------------|
| Virtual DOM কী? | JS-এ DOM-এর memory representation |
| Reconciliation কী? | Old/new Virtual DOM diff করে minimal update |
| Props vs State | Props = parent থেকে, State = component-এর নিজের |
| key prop কেন? | List-এ items uniquely identify করতে |
| useState lazy init | `useState(() => fn())` — শুধু প্রথম render-এ |
| stale closure fix | Functional update: `setState(prev => ...)` |
| React.memo কী? | Props same থাকলে re-render prevent করে |
| useMemo vs useCallback | value vs function memoize |
| Error Boundary কী? | Render error catch করে fallback দেখায় |
| Portal কী? | Parent-এর বাইরে DOM-এ render করা |
| Batching কী? | Multiple setState একসাথে process করা |
| Code splitting কীভাবে? | `lazy()` + `Suspense` + dynamic import |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part12"></a>
## PART 12: Next.js Basics

> React developer-দের জন্য Next.js শেখা আজ প্রায় mandatory। App Router, Server Components, SSR/SSG/ISR — সব কিছু এখানে covered।

| # | বিষয় |
|---|-------|
| 1 | Next.js পরিচিতি ও কেন ব্যবহার করব |
| 2 | Pages Router vs App Router |
| 3 | File-based Routing (layouts, loading, error) |
| 4 | Server Components vs Client Components |
| 5 | Data Fetching (SSG, SSR, ISR) |
| 6 | Route Handlers (API Routes) |
| 7 | next/image — Image Optimization |
| 8 | Metadata API ও SEO |
| 9 | Middleware |
| 10 | Deployment ও Vercel |

---

**Topic 1: Next.js পরিচিতি ও কেন ব্যবহার করব**

Next.js হলো Vercel-এর তৈরি React-এর উপর built full-stack framework। Pure React-এ যা নেই:

| Feature | Pure React | Next.js |
|---------|-----------|---------|
| Server-side rendering | ❌ | ✅ |
| File-based routing | ❌ | ✅ |
| API routes | ❌ | ✅ |
| Image optimization | ❌ | ✅ |
| SEO (SSR/SSG) | কঠিন | সহজ |
| Code splitting | manual | automatic |

**কখন Next.js ব্যবহার করবেন:**
- SEO important (blog, e-commerce, landing page)
- Initial load performance critical
- Full-stack app (frontend + backend একসাথে)
- Server-side data fetching দরকার

```bash
# নতুন project তৈরি
npx create-next-app@latest my-app
# TypeScript, Tailwind, App Router — সব yes দিন
```

---

**Topic 2: Pages Router vs App Router**

**Pages Router (Next.js 12 এবং আগে):**
```
pages/
├── index.js          → /
├── about.js          → /about
├── blog/
│   ├── index.js      → /blog
│   └── [id].js       → /blog/123
├── api/
│   └── users.js      → /api/users
└── _app.js           → root layout
```

**App Router (Next.js 13+ — recommended):**
```
app/
├── page.js           → /
├── layout.js         → root layout
├── about/
│   └── page.js       → /about
├── blog/
│   ├── page.js       → /blog
│   └── [id]/
│       └── page.js   → /blog/123
└── api/
    └── users/
        └── route.js  → /api/users
```

App Router-এর সুবিধা:
- Server Components by default
- Nested layouts
- Streaming (Suspense-based)
- `loading.js`, `error.js` per-segment

---

**Topic 3: File-based Routing**

**Special files:**
```
app/
├── layout.js         → Shared UI (persists across navigation)
├── page.js           → Route UI
├── loading.js        → Suspense fallback
├── error.js          → Error boundary
├── not-found.js      → 404 page
└── template.js       → Re-renders on every navigation
```

**Root Layout (required):**
```jsx
// app/layout.js
export default function RootLayout({ children }) {
  return (
    <html lang="bn">
      <body>
        <Header />
        <main>{children}</main>
        <Footer />
      </body>
    </html>
  );
}
```

**Dynamic Routes:**
```
app/blog/[slug]/page.js     → /blog/my-post
app/shop/[...slug]/page.js  → /shop/a/b/c (catch-all)
app/shop/[[...slug]]/page.js → /shop + /shop/a/b (optional)
```

```jsx
// app/blog/[slug]/page.js
export default function BlogPost({ params }) {
  return <h1>Post: {params.slug}</h1>;
}

// Static params generate করা (SSG-এর জন্য)
export async function generateStaticParams() {
  const posts = await fetchAllPosts();
  return posts.map(post => ({ slug: post.slug }));
}
```

**Loading UI:**
```jsx
// app/blog/loading.js — automatically shown during page load
export default function Loading() {
  return <BlogSkeleton />;
}
```

**Error Handling:**
```jsx
// app/blog/error.js
'use client'; // Error components must be client components
export default function Error({ error, reset }) {
  return (
    <div>
      <h2>কিছু একটা ভুল হয়েছে!</h2>
      <p>{error.message}</p>
      <button onClick={() => reset()}>আবার চেষ্টা করুন</button>
    </div>
  );
}
```

**Route Groups (URL affect করে না):**
```
app/
├── (auth)/
│   ├── login/page.js    → /login
│   └── register/page.js → /register
└── (dashboard)/
    ├── layout.js        → dashboard-specific layout
    └── home/page.js     → /home
```

---

**Topic 4: Server Components vs Client Components**

Next.js App Router-এ সব components default Server Component।

| | Server Component | Client Component |
|--|-----------------|-----------------|
| Rendering | Server-এ | Browser-এ |
| `useState`, `useEffect` | ❌ | ✅ |
| Event handlers | ❌ | ✅ |
| Browser APIs | ❌ | ✅ |
| Direct DB access | ✅ | ❌ |
| `async/await` | ✅ | ❌ (top level) |
| Bundle size | 0 JS sent | JS bundle-এ যায় |

**Client Component:**
```jsx
'use client'; // এই directive শুরুতে দিতে হবে

import { useState } from 'react';

export default function Counter() {
  const [count, setCount] = useState(0);
  return <button onClick={() => setCount(c => c + 1)}>{count}</button>;
}
```

**Server Component (async data fetch):**
```jsx
// app/posts/page.js — NO 'use client' needed
async function getPosts() {
  const res = await fetch('https://api.example.com/posts', {
    next: { revalidate: 3600 } // ISR — 1 hour
  });
  return res.json();
}

export default async function PostsPage() {
  const posts = await getPosts(); // সরাসরি await!
  return (
    <ul>
      {posts.map(post => <li key={post.id}>{post.title}</li>)}
    </ul>
  );
}
```

**Pattern: Server wraps Client**
```jsx
// ✅ Server Component-এ Client Component use করা যায়
export default async function Page() {
  const data = await fetchData(); // server-side
  return (
    <div>
      <h1>Server rendered heading</h1>
      <ClientInteractiveWidget data={data} /> {/* client component */}
    </div>
  );
}
```

**`use server` directive:**
```jsx
// Server Actions — form submit বা button click-এ server function call
async function createPost(formData) {
  'use server';
  const title = formData.get('title');
  await db.post.create({ data: { title } });
  revalidatePath('/posts');
}

export default function NewPostForm() {
  return (
    <form action={createPost}>
      <input name="title" required />
      <button type="submit">Post তৈরি করুন</button>
    </form>
  );
}
```

---

**Topic 5: Data Fetching Strategies**

**1. SSG — Static Site Generation (Build time):**
```jsx
// app/blog/[slug]/page.js
export default async function BlogPost({ params }) {
  const post = await fetch(`/api/posts/${params.slug}`).then(r => r.json());
  return <article>{post.content}</article>;
}

// Build time-এ কোন pages generate করব
export async function generateStaticParams() {
  const posts = await fetch('/api/posts').then(r => r.json());
  return posts.map(p => ({ slug: p.slug }));
}
```
**Best for:** Blog, docs, marketing pages (rarely changes)

**2. SSR — Server-side Rendering (Request time):**
```jsx
// cache: 'no-store' → প্রতি request-এ fresh data
async function getUser(id) {
  const res = await fetch(`/api/users/${id}`, { cache: 'no-store' });
  return res.json();
}

export default async function UserProfile({ params }) {
  const user = await getUser(params.id);
  return <div>Welcome, {user.name}</div>;
}
```
**Best for:** User dashboard, personalized content, real-time data

**3. ISR — Incremental Static Regeneration:**
```jsx
// revalidate: 60 → ৬০ সেকেন্ড পরে background-এ rebuild
async function getProducts() {
  const res = await fetch('/api/products', {
    next: { revalidate: 60 }
  });
  return res.json();
}
```
**Best for:** Product catalog, news, data that changes occasionally

**4. On-demand Revalidation:**
```jsx
// app/api/revalidate/route.js
import { revalidatePath, revalidateTag } from 'next/cache';

export async function POST(req) {
  const { path } = await req.json();
  revalidatePath(path); // specific path clear
  // অথবা: revalidateTag('products') — tagged cache clear
  return Response.json({ revalidated: true });
}
```

**fetch() cache options summary:**
```jsx
fetch(url)                          // default: force-cache (SSG)
fetch(url, { cache: 'no-store' })   // SSR — no cache
fetch(url, { next: { revalidate: 60 } }) // ISR
fetch(url, { next: { tags: ['products'] } }) // tag-based revalidation
```

---

**Topic 6: Route Handlers (API Routes)**

App Router-এ `route.js` ফাইল API endpoint তৈরি করে:

```jsx
// app/api/posts/route.js
import { NextResponse } from 'next/server';

// GET /api/posts
export async function GET(request) {
  const { searchParams } = new URL(request.url);
  const page = searchParams.get('page') || '1';
  
  const posts = await db.post.findMany({
    skip: (parseInt(page) - 1) * 10,
    take: 10
  });
  
  return NextResponse.json({ posts, page });
}

// POST /api/posts
export async function POST(request) {
  const body = await request.json();
  const post = await db.post.create({ data: body });
  return NextResponse.json(post, { status: 201 });
}
```

**Dynamic Route Handler:**
```jsx
// app/api/posts/[id]/route.js
export async function GET(request, { params }) {
  const post = await db.post.findUnique({ where: { id: params.id } });
  if (!post) return NextResponse.json({ error: 'Not found' }, { status: 404 });
  return NextResponse.json(post);
}

export async function DELETE(request, { params }) {
  await db.post.delete({ where: { id: params.id } });
  return new Response(null, { status: 204 });
}
```

**Authentication in Route Handler:**
```jsx
import { getServerSession } from 'next-auth';

export async function GET(request) {
  const session = await getServerSession();
  if (!session) {
    return NextResponse.json({ error: 'Unauthorized' }, { status: 401 });
  }
  // authenticated request handle করুন
}
```

---

**Topic 7: next/image — Image Optimization**

`next/image` automatically: resize, WebP conversion, lazy loading, CLS prevention করে।

```jsx
import Image from 'next/image';

// Local image
import avatar from '@/public/avatar.jpg';
<Image src={avatar} alt="User avatar" />

// Remote image — width/height required
<Image
  src="https://example.com/photo.jpg"
  alt="Photo"
  width={800}
  height={600}
  priority  // LCP image-এ দিন (above-the-fold)
/>

// Fill — parent container fill করে
<div style={{ position: 'relative', height: '400px' }}>
  <Image
    src="/hero.jpg"
    alt="Hero"
    fill
    style={{ objectFit: 'cover' }}
  />
</div>
```

**Remote images allow করতে (next.config.js):**
```js
/** @type {import('next').NextConfig} */
const nextConfig = {
  images: {
    remotePatterns: [
      {
        protocol: 'https',
        hostname: 'res.cloudinary.com',
      },
      {
        protocol: 'https',
        hostname: '**.githubusercontent.com',
      }
    ],
  },
};
export default nextConfig;
```

**Responsive images:**
```jsx
<Image
  src="/banner.jpg"
  alt="Banner"
  sizes="(max-width: 768px) 100vw, (max-width: 1200px) 50vw, 33vw"
  fill
  style={{ objectFit: 'cover' }}
/>
```

---

**Topic 8: Metadata API ও SEO**

**Static Metadata:**
```jsx
// app/about/page.js
export const metadata = {
  title: 'আমাদের সম্পর্কে | MyApp',
  description: 'আমাদের team ও mission সম্পর্কে জানুন।',
  openGraph: {
    title: 'আমাদের সম্পর্কে',
    description: 'আমাদের team ও mission সম্পর্কে জানুন।',
    images: ['/og-about.jpg'],
    type: 'website',
  },
  twitter: {
    card: 'summary_large_image',
    title: 'আমাদের সম্পর্কে',
  },
};
```

**Dynamic Metadata (data-based):**
```jsx
// app/blog/[slug]/page.js
export async function generateMetadata({ params }) {
  const post = await getPost(params.slug);
  
  return {
    title: `${post.title} | Blog`,
    description: post.excerpt,
    openGraph: {
      title: post.title,
      images: [post.coverImage],
      publishedTime: post.publishedAt,
      type: 'article',
    },
    alternates: {
      canonical: `https://myapp.com/blog/${params.slug}`,
    },
  };
}
```

**Metadata Template (root layout):**
```jsx
// app/layout.js
export const metadata = {
  title: {
    default: 'MyApp',
    template: '%s | MyApp', // child page title এখানে %s হবে
  },
  description: 'Best app ever',
  metadataBase: new URL('https://myapp.com'), // absolute URLs-এর জন্য
};
```

**robots.txt ও sitemap:**
```jsx
// app/robots.js
export default function robots() {
  return {
    rules: { userAgent: '*', allow: '/' },
    sitemap: 'https://myapp.com/sitemap.xml',
  };
}

// app/sitemap.js
export default async function sitemap() {
  const posts = await getAllPosts();
  return [
    { url: 'https://myapp.com', lastModified: new Date() },
    ...posts.map(post => ({
      url: `https://myapp.com/blog/${post.slug}`,
      lastModified: post.updatedAt,
    })),
  ];
}
```

---

**Topic 9: Middleware**

Middleware request পৌঁছানোর আগে intercept করে — auth check, redirect, header modification।

```jsx
// middleware.js (root-এ, app/ বাইরে)
import { NextResponse } from 'next/server';
import { getToken } from 'next-auth/jwt';

export async function middleware(request) {
  const token = await getToken({ req: request });
  const { pathname } = request.nextUrl;

  // Auth check
  const protectedPaths = ['/dashboard', '/profile', '/settings'];
  const isProtected = protectedPaths.some(p => pathname.startsWith(p));

  if (isProtected && !token) {
    const loginUrl = new URL('/login', request.url);
    loginUrl.searchParams.set('callbackUrl', pathname);
    return NextResponse.redirect(loginUrl);
  }

  // Role-based check
  if (pathname.startsWith('/admin') && token?.role !== 'admin') {
    return NextResponse.redirect(new URL('/403', request.url));
  }

  // Custom header add
  const response = NextResponse.next();
  response.headers.set('x-pathname', pathname);
  return response;
}

// কোন paths-এ middleware চলবে
export const config = {
  matcher: [
    '/((?!_next/static|_next/image|favicon.ico|public/).*)',
  ],
};
```

**Internationalization (i18n) redirect:**
```jsx
export function middleware(request) {
  const { pathname } = request.nextUrl;
  const locale = getLocale(request); // Accept-Language header পড়ুন
  
  if (!pathname.startsWith(`/${locale}`)) {
    return NextResponse.redirect(new URL(`/${locale}${pathname}`, request.url));
  }
}
```

---

**Topic 10: Deployment ও Vercel**

**Vercel Deploy (সহজতম):**
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Production deploy
vercel --prod
```

**Environment Variables:**
```bash
# .env.local (local development)
DATABASE_URL="postgresql://..."
NEXTAUTH_SECRET="your-secret"
NEXTAUTH_URL="http://localhost:3000"

# Public variables (browser-এ accessible)
NEXT_PUBLIC_API_URL="https://api.example.com"
```

**Vercel dashboard-এ:** Settings → Environment Variables-এ add করুন।

**next.config.js — Common configurations:**
```js
/** @type {import('next').NextConfig} */
const nextConfig = {
  // Standalone output (Docker deploy-এর জন্য)
  output: 'standalone',
  
  // Redirect
  async redirects() {
    return [
      { source: '/old-path', destination: '/new-path', permanent: true },
    ];
  },
  
  // Rewrite (proxy)
  async rewrites() {
    return [
      { source: '/api/v1/:path*', destination: 'https://backend.example.com/:path*' },
    ];
  },
  
  // Turbopack (Next.js 15+ default)
  experimental: {
    turbo: {},
  },
};
export default nextConfig;
```

**Docker deploy:**
```dockerfile
FROM node:20-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build

FROM node:20-alpine AS runner
WORKDIR /app
ENV NODE_ENV production
COPY --from=builder /app/.next/standalone ./
COPY --from=builder /app/.next/static ./.next/static
COPY --from=builder /app/public ./public
EXPOSE 3000
CMD ["node", "server.js"]
```

**Performance checklist:**
```
✅ Image: next/image ব্যবহার করুন, priority LCP image-এ
✅ Font: next/font দিয়ে Google Fonts load করুন (zero layout shift)
✅ Bundle: dynamic imports দিয়ে code split করুন
✅ Cache: fetch() revalidate সঠিকভাবে set করুন
✅ Metadata: প্রতিটি page-এ title + description
✅ CSP headers: next.config.js-এ security headers add করুন
✅ Rate limiting: API routes-এ implement করুন
```

**next/font example:**
```jsx
// app/layout.js
import { Inter, Hind_Siliguri } from 'next/font/google';

const inter = Inter({ subsets: ['latin'], variable: '--font-inter' });
const hind = Hind_Siliguri({
  subsets: ['bengali'],
  weight: ['400', '500', '600'],
  variable: '--font-hind'
});

export default function RootLayout({ children }) {
  return (
    <html className={`${inter.variable} ${hind.variable}`}>
      <body>{children}</body>
    </html>
  );
}
```

---

**PART 12 Quick Revision Table**

| বিষয় | মূল কথা |
|------|---------|
| Next.js কী? | React-এর উপর full-stack framework (SSR, routing, API) |
| App Router কী? | Next.js 13+-এর নতুন routing system, `app/` directory |
| Server Component | Server-এ render, no useState/useEffect, async/await সরাসরি |
| `'use client'` | Browser APIs, state, event handlers দরকার হলে |
| SSG | Build time-এ generate, `generateStaticParams` |
| SSR | প্রতি request-এ `cache: 'no-store'` |
| ISR | `next: { revalidate: N }` — background rebuild |
| Route Handler | `route.js` ফাইল — API endpoint |
| next/image | Auto optimize, lazy load, CLS prevent |
| Metadata API | `export const metadata` বা `generateMetadata()` |
| Middleware | `middleware.js` — auth check, redirect, headers |
| Server Actions | `'use server'` — form/button থেকে server function call |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 13 — Testing & Best Practices

---

<a id="part13"></a>
## PART 13: Testing & Best Practices

> Production-ready React code লেখার জন্য testing ও best practices জানা অপরিহার্য। এই PART-এ Jest, React Testing Library, accessibility testing, ESLint/Prettier, folder structure এবং Git workflow cover করা হয়েছে।

| # | বিষয় |
|---|-------|
| 1 | Testing কেন দরকার — Testing Pyramid |
| 2 | Jest Setup ও Basics |
| 3 | React Testing Library (RTL) |
| 4 | Component Testing Patterns |
| 5 | Hook Testing (renderHook) |
| 6 | API Mocking (MSW) |
| 7 | Accessibility Testing |
| 8 | ESLint ও Prettier Setup |
| 9 | Folder Structure Best Practices |
| 10 | Git Workflow ও Conventional Commits |

---

**Topic 1: Testing কেন দরকার — Testing Pyramid**

Testing ছাড়া code refactor করা ভয়ের — কোথায় কী ভাঙবে জানা যায় না।

**Testing Pyramid:**
```
         /\
        /  \  E2E Tests (Playwright, Cypress)
       /----\  — সবচেয়ে কম, সবচেয়ে ধীর, most realistic
      /      \
     /--------\  Integration Tests
    /          \  — components + hooks + API একসাথে
   /------------\
  /              \  Unit Tests (সবচেয়ে বেশি)
 /________________\  — pure functions, utils, hooks
```

| Type | Tool | Speed | Confidence |
|------|------|-------|-----------|
| Unit | Jest | ⚡⚡⚡ | কম |
| Integration | RTL | ⚡⚡ | মাঝারি |
| E2E | Playwright | ⚡ | সবচেয়ে বেশি |

**React project-এ কী test করব:**
```
✅ Pure utility functions
✅ Custom hooks
✅ Component rendering (snapshot/behavior)
✅ User interactions (click, type, submit)
✅ Async operations (API calls)
✅ Error states
❌ Implementation details (state variable names)
❌ Third-party library internals
```

---

**Topic 2: Jest Setup ও Basics**

Vite project-এ Jest setup:
```bash
npm install -D jest @types/jest jest-environment-jsdom
npm install -D @testing-library/react @testing-library/jest-dom
npm install -D @testing-library/user-event
npm install -D babel-jest @babel/preset-env @babel/preset-react
```

**jest.config.js:**
```js
export default {
  testEnvironment: 'jsdom',
  setupFilesAfterFramework: ['<rootDir>/src/setupTests.js'],
  moduleNameMapper: {
    '^@/(.*)$': '<rootDir>/src/$1',       // path alias
    '\\.(css|less|scss)$': 'identity-obj-proxy', // CSS modules mock
    '\\.(jpg|png|svg)$': '<rootDir>/src/__mocks__/fileMock.js',
  },
  transform: {
    '^.+\\.[jt]sx?$': 'babel-jest',
  },
  coverageThreshold: {
    global: { branches: 70, functions: 70, lines: 70 },
  },
};
```

**src/setupTests.js:**
```js
import '@testing-library/jest-dom';
// extends expect() with: toBeInTheDocument, toHaveClass, toHaveValue, etc.
```

**Jest basics — matchers:**
```js
// Equality
expect(2 + 2).toBe(4);
expect({ a: 1 }).toEqual({ a: 1 }); // deep equal

// Truthiness
expect(null).toBeNull();
expect(undefined).toBeUndefined();
expect(true).toBeTruthy();
expect(0).toBeFalsy();

// Numbers
expect(5).toBeGreaterThan(3);
expect(5).toBeLessThanOrEqual(5);

// Strings
expect('Hello World').toContain('World');
expect('Hello').toMatch(/hell/i);

// Arrays
expect([1, 2, 3]).toContain(2);
expect([1, 2, 3]).toHaveLength(3);

// Async
await expect(fetchUser(1)).resolves.toEqual({ id: 1, name: 'Alice' });
await expect(fetchUser(-1)).rejects.toThrow('User not found');
```

**describe ও test structure:**
```js
describe('Calculator', () => {
  describe('add()', () => {
    test('দুটি positive number যোগ করে', () => {
      expect(add(2, 3)).toBe(5);
    });

    test('negative number handle করে', () => {
      expect(add(-1, 1)).toBe(0);
    });
  });

  describe('divide()', () => {
    test('zero দিয়ে ভাগ করলে error throw করে', () => {
      expect(() => divide(5, 0)).toThrow('Cannot divide by zero');
    });
  });
});
```

**Mocking:**
```js
// Function mock
const mockFn = jest.fn();
mockFn('hello');
expect(mockFn).toHaveBeenCalledWith('hello');
expect(mockFn).toHaveBeenCalledTimes(1);

// Module mock
jest.mock('./api/userService', () => ({
  getUser: jest.fn().mockResolvedValue({ id: 1, name: 'Alice' }),
  createUser: jest.fn().mockResolvedValue({ id: 2, name: 'Bob' }),
}));

// Implementation mock
import { getUser } from './api/userService';
getUser.mockResolvedValueOnce({ id: 1, name: 'Alice' }); // একবার
getUser.mockRejectedValueOnce(new Error('Network error')); // error case
```

---

**Topic 3: React Testing Library (RTL)**

RTL-এর philosophy: **Test behavior, not implementation.** User কীভাবে interact করে সেটা test করুন।

**Core queries — priority order:**
```js
// 1. getByRole — সবচেয়ে preferred (accessibility-friendly)
screen.getByRole('button', { name: /submit/i })
screen.getByRole('textbox', { name: /email/i })
screen.getByRole('heading', { level: 1 })
screen.getByRole('link', { name: /home/i })

// 2. getByLabelText — form elements-এর জন্য
screen.getByLabelText(/email address/i)

// 3. getByPlaceholderText
screen.getByPlaceholderText(/your name/i)

// 4. getByText — visible text
screen.getByText(/hello world/i)

// 5. getByTestId — শেষ উপায়
screen.getByTestId('submit-btn')
```

**get vs query vs find:**
```js
// getBy* — পাওয়া না গেলে error throw করে
screen.getByText('Submit')

// queryBy* — পাওয়া না গেলে null return করে (absence check)
expect(screen.queryByText('Error')).not.toBeInTheDocument()

// findBy* — async, returns Promise (appear করার জন্য অপেক্ষা করে)
await screen.findByText('Loading complete')
```

**render ও cleanup:**
```js
import { render, screen } from '@testing-library/react';

test('renders greeting', () => {
  render(<Greeting name="Alice" />);
  expect(screen.getByText('Hello, Alice!')).toBeInTheDocument();
});
// cleanup automatically happens after each test
```

**Wrapping with providers:**
```js
// Custom render function — project-এ একবার তৈরি করুন
function renderWithProviders(ui, options = {}) {
  const { initialState = {}, ...renderOptions } = options;
  const store = setupStore(initialState);
  
  function Wrapper({ children }) {
    return (
      <Provider store={store}>
        <BrowserRouter>
          <ThemeProvider>
            {children}
          </ThemeProvider>
        </BrowserRouter>
      </Provider>
    );
  }
  
  return { store, ...render(ui, { wrapper: Wrapper, ...renderOptions }) };
}

// Usage:
const { store } = renderWithProviders(<Dashboard />, {
  initialState: { user: { name: 'Alice', role: 'admin' } }
});
```

---

**Topic 4: Component Testing Patterns**

**Pattern 1: Simple render test**
```js
// components/Badge.test.jsx
import { render, screen } from '@testing-library/react';
import Badge from './Badge';

describe('Badge component', () => {
  test('text সঠিকভাবে render হয়', () => {
    render(<Badge>New</Badge>);
    expect(screen.getByText('New')).toBeInTheDocument();
  });

  test('variant class apply হয়', () => {
    const { container } = render(<Badge variant="success">OK</Badge>);
    expect(container.firstChild).toHaveClass('badge-success');
  });

  test('custom className accept করে', () => {
    render(<Badge className="extra">Test</Badge>);
    expect(screen.getByText('Test')).toHaveClass('extra');
  });
});
```

**Pattern 2: User interaction test**
```js
// components/Counter.test.jsx
import { render, screen } from '@testing-library/react';
import userEvent from '@testing-library/user-event';
import Counter from './Counter';

describe('Counter', () => {
  test('initial count 0 দেখায়', () => {
    render(<Counter />);
    expect(screen.getByText('Count: 0')).toBeInTheDocument();
  });

  test('increment button click-এ count বাড়ে', async () => {
    const user = userEvent.setup();
    render(<Counter />);
    
    await user.click(screen.getByRole('button', { name: /increment/i }));
    expect(screen.getByText('Count: 1')).toBeInTheDocument();
    
    await user.click(screen.getByRole('button', { name: /increment/i }));
    expect(screen.getByText('Count: 2')).toBeInTheDocument();
  });

  test('reset button-এ 0-এ ফেরে', async () => {
    const user = userEvent.setup();
    render(<Counter initialCount={5} />);
    
    await user.click(screen.getByRole('button', { name: /reset/i }));
    expect(screen.getByText('Count: 0')).toBeInTheDocument();
  });
});
```

**Pattern 3: Form test**
```js
// components/LoginForm.test.jsx
import { render, screen, waitFor } from '@testing-library/react';
import userEvent from '@testing-library/user-event';
import LoginForm from './LoginForm';

describe('LoginForm', () => {
  const mockOnSubmit = jest.fn();

  beforeEach(() => {
    mockOnSubmit.mockClear();
  });

  test('valid credentials দিয়ে submit করা যায়', async () => {
    const user = userEvent.setup();
    render(<LoginForm onSubmit={mockOnSubmit} />);

    await user.type(screen.getByLabelText(/email/i), 'alice@example.com');
    await user.type(screen.getByLabelText(/password/i), 'password123');
    await user.click(screen.getByRole('button', { name: /login/i }));

    await waitFor(() => {
      expect(mockOnSubmit).toHaveBeenCalledWith({
        email: 'alice@example.com',
        password: 'password123',
      });
    });
  });

  test('empty email-এ validation error দেখায়', async () => {
    const user = userEvent.setup();
    render(<LoginForm onSubmit={mockOnSubmit} />);

    await user.click(screen.getByRole('button', { name: /login/i }));

    expect(await screen.findByText(/email is required/i)).toBeInTheDocument();
    expect(mockOnSubmit).not.toHaveBeenCalled();
  });

  test('invalid email format-এ error দেখায়', async () => {
    const user = userEvent.setup();
    render(<LoginForm onSubmit={mockOnSubmit} />);

    await user.type(screen.getByLabelText(/email/i), 'not-an-email');
    await user.tab(); // blur trigger

    expect(await screen.findByText(/invalid email/i)).toBeInTheDocument();
  });
});
```

**Pattern 4: Async / Loading state test**
```js
// components/UserProfile.test.jsx
import { render, screen } from '@testing-library/react';
import { rest } from 'msw';
import { server } from '../mocks/server';
import UserProfile from './UserProfile';

test('loading spinner দেখায়', () => {
  render(<UserProfile userId="1" />);
  expect(screen.getByRole('progressbar')).toBeInTheDocument();
});

test('user data load হওয়ার পরে দেখায়', async () => {
  render(<UserProfile userId="1" />);
  
  expect(await screen.findByText('Alice Smith')).toBeInTheDocument();
  expect(screen.getByText('alice@example.com')).toBeInTheDocument();
});

test('error state সঠিকভাবে দেখায়', async () => {
  // Override server response for this test
  server.use(
    rest.get('/api/users/1', (req, res, ctx) =>
      res(ctx.status(500), ctx.json({ message: 'Server error' }))
    )
  );
  
  render(<UserProfile userId="1" />);
  expect(await screen.findByText(/something went wrong/i)).toBeInTheDocument();
});
```

---

**Topic 5: Hook Testing (renderHook)**

```js
// hooks/useCounter.test.js
import { renderHook, act } from '@testing-library/react';
import useCounter from './useCounter';

describe('useCounter', () => {
  test('initial value দিয়ে শুরু হয়', () => {
    const { result } = renderHook(() => useCounter(10));
    expect(result.current.count).toBe(10);
  });

  test('increment কাজ করে', () => {
    const { result } = renderHook(() => useCounter(0));
    
    act(() => {
      result.current.increment();
    });
    
    expect(result.current.count).toBe(1);
  });

  test('decrement minimum 0-এ আটকে', () => {
    const { result } = renderHook(() => useCounter(0));
    
    act(() => {
      result.current.decrement();
    });
    
    expect(result.current.count).toBe(0); // 0-এর নিচে যায় না
  });
});
```

**Async hook test:**
```js
// hooks/useFetch.test.js
import { renderHook, waitFor } from '@testing-library/react';
import useFetch from './useFetch';

test('data fetch করে এবং loading state পরিচালনা করে', async () => {
  const { result } = renderHook(() => useFetch('/api/users'));

  // Initially loading
  expect(result.current.loading).toBe(true);
  expect(result.current.data).toBeNull();

  // Wait for data
  await waitFor(() => {
    expect(result.current.loading).toBe(false);
  });

  expect(result.current.data).toEqual([{ id: 1, name: 'Alice' }]);
  expect(result.current.error).toBeNull();
});
```

**Context-dependent hook:**
```js
// hooks/useAuth.test.js
import { renderHook } from '@testing-library/react';
import { AuthProvider } from '../context/AuthContext';
import useAuth from './useAuth';

const wrapper = ({ children }) => <AuthProvider>{children}</AuthProvider>;

test('authenticated user-এর info return করে', () => {
  const { result } = renderHook(() => useAuth(), { wrapper });
  expect(result.current.isLoggedIn).toBe(false);
  expect(result.current.user).toBeNull();
});
```

---

**Topic 6: API Mocking (MSW)**

MSW (Mock Service Worker) — network level-এ intercept করে, implementation details থেকে independent:

```bash
npm install -D msw
npx msw init public/ --save
```

**src/mocks/handlers.js:**
```js
import { http, HttpResponse } from 'msw';

export const handlers = [
  // GET users list
  http.get('/api/users', () => {
    return HttpResponse.json([
      { id: 1, name: 'Alice', email: 'alice@example.com' },
      { id: 2, name: 'Bob', email: 'bob@example.com' },
    ]);
  }),

  // GET single user
  http.get('/api/users/:id', ({ params }) => {
    const users = { '1': { id: 1, name: 'Alice' }, '2': { id: 2, name: 'Bob' } };
    const user = users[params.id];
    if (!user) return new HttpResponse(null, { status: 404 });
    return HttpResponse.json(user);
  }),

  // POST create user
  http.post('/api/users', async ({ request }) => {
    const body = await request.json();
    return HttpResponse.json({ id: 3, ...body }, { status: 201 });
  }),

  // DELETE user
  http.delete('/api/users/:id', () => {
    return new HttpResponse(null, { status: 204 });
  }),
];
```

**src/mocks/server.js (Node/Jest-এর জন্য):**
```js
import { setupServer } from 'msw/node';
import { handlers } from './handlers';

export const server = setupServer(...handlers);
```

**src/setupTests.js-এ add করুন:**
```js
import '@testing-library/jest-dom';
import { server } from './mocks/server';

beforeAll(() => server.listen({ onUnhandledRequest: 'error' }));
afterEach(() => server.resetHandlers()); // test-specific overrides reset
afterAll(() => server.close());
```

**Error scenario test:**
```js
import { http, HttpResponse } from 'msw';
import { server } from '../mocks/server';

test('network error gracefully handle করে', async () => {
  server.use(
    http.get('/api/users', () => {
      return HttpResponse.error(); // network failure simulate
    })
  );
  
  render(<UserList />);
  expect(await screen.findByText(/network error/i)).toBeInTheDocument();
});
```

---

**Topic 7: Accessibility Testing**

```bash
npm install -D jest-axe
```

```js
// components/Modal.test.jsx
import { render } from '@testing-library/react';
import { axe, toHaveNoViolations } from 'jest-axe';
import Modal from './Modal';

expect.extend(toHaveNoViolations);

test('Modal has no accessibility violations', async () => {
  const { container } = render(
    <Modal isOpen={true} onClose={() => {}} title="Test Modal">
      <p>Modal content</p>
    </Modal>
  );
  
  const results = await axe(container);
  expect(results).toHaveNoViolations();
});
```

**ARIA attributes test:**
```js
test('button has accessible name', () => {
  render(<IconButton icon="close" ariaLabel="Close dialog" />);
  
  const button = screen.getByRole('button', { name: /close dialog/i });
  expect(button).toHaveAttribute('aria-label', 'Close dialog');
});

test('form field has associated label', () => {
  render(<EmailInput />);
  
  // getByLabelText verifies label-input association
  expect(screen.getByLabelText(/email/i)).toBeInTheDocument();
});

test('error message linked to input', async () => {
  const user = userEvent.setup();
  render(<LoginForm />);
  
  await user.click(screen.getByRole('button', { name: /submit/i }));
  
  const errorMsg = await screen.findByRole('alert');
  expect(errorMsg).toBeInTheDocument();
  // aria-describedby check
  expect(screen.getByLabelText(/email/i)).toHaveAttribute('aria-invalid', 'true');
});
```

---

**Topic 8: ESLint ও Prettier Setup**

**Installation:**
```bash
# ESLint
npm install -D eslint @eslint/js eslint-plugin-react eslint-plugin-react-hooks
npm install -D eslint-plugin-jsx-a11y eslint-plugin-import

# Prettier
npm install -D prettier eslint-config-prettier eslint-plugin-prettier
```

**eslint.config.js (Flat config — ESLint 9+):**
```js
import js from '@eslint/js';
import reactPlugin from 'eslint-plugin-react';
import reactHooks from 'eslint-plugin-react-hooks';
import jsxA11y from 'eslint-plugin-jsx-a11y';
import prettier from 'eslint-config-prettier';

export default [
  js.configs.recommended,
  {
    plugins: {
      react: reactPlugin,
      'react-hooks': reactHooks,
      'jsx-a11y': jsxA11y,
    },
    rules: {
      // React
      'react/prop-types': 'off',        // TypeScript থাকলে off
      'react/react-in-jsx-scope': 'off', // React 17+ import লাগে না
      'react/jsx-no-target-blank': 'error', // Security: noopener noreferrer
      
      // Hooks
      'react-hooks/rules-of-hooks': 'error',
      'react-hooks/exhaustive-deps': 'warn',
      
      // Accessibility
      'jsx-a11y/alt-text': 'error',
      'jsx-a11y/anchor-has-content': 'error',
      'jsx-a11y/click-events-have-key-events': 'warn',
      
      // General
      'no-console': 'warn',
      'no-unused-vars': ['error', { argsIgnorePattern: '^_' }],
      'prefer-const': 'error',
      'no-var': 'error',
    },
    settings: {
      react: { version: 'detect' },
    },
  },
  prettier, // prettier-এর conflicting rules off করে
];
```

**.prettierrc:**
```json
{
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "es5",
  "printWidth": 100,
  "bracketSpacing": true,
  "arrowParens": "avoid",
  "endOfLine": "lf"
}
```

**package.json scripts:**
```json
{
  "scripts": {
    "lint": "eslint src/",
    "lint:fix": "eslint src/ --fix",
    "format": "prettier --write src/",
    "format:check": "prettier --check src/",
    "test": "jest",
    "test:watch": "jest --watch",
    "test:coverage": "jest --coverage"
  }
}
```

**VSCode settings (.vscode/settings.json):**
```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit"
  },
  "eslint.validate": ["javascript", "javascriptreact", "typescript", "typescriptreact"]
}
```

**Husky + lint-staged (commit-এ auto lint):**
```bash
npm install -D husky lint-staged
npx husky init
```

**.husky/pre-commit:**
```bash
npx lint-staged
```

**package.json:**
```json
{
  "lint-staged": {
    "src/**/*.{js,jsx,ts,tsx}": ["eslint --fix", "prettier --write"],
    "src/**/*.{css,json,md}": "prettier --write"
  }
}
```

---

**Topic 9: Folder Structure Best Practices**

**Feature-based structure (recommended for medium-large apps):**
```
src/
├── app/                    # App-wide setup
│   ├── store.js            # Redux store
│   ├── routes.jsx          # Route definitions
│   └── App.jsx
├── features/               # Feature modules
│   ├── auth/
│   │   ├── components/     # Feature-specific components
│   │   │   ├── LoginForm.jsx
│   │   │   └── RegisterForm.jsx
│   │   ├── hooks/          # Feature-specific hooks
│   │   │   └── useAuth.js
│   │   ├── api/            # API calls
│   │   │   └── authApi.js
│   │   ├── store/          # Redux slice
│   │   │   └── authSlice.js
│   │   └── index.js        # Public API (barrel export)
│   ├── products/
│   │   ├── components/
│   │   ├── hooks/
│   │   ├── api/
│   │   └── index.js
│   └── cart/
│       ├── components/
│       ├── hooks/
│       ├── store/
│       └── index.js
├── shared/                 # Cross-feature shared code
│   ├── components/         # Reusable UI components
│   │   ├── Button/
│   │   │   ├── Button.jsx
│   │   │   ├── Button.test.jsx
│   │   │   └── index.js
│   │   ├── Modal/
│   │   └── Table/
│   ├── hooks/              # Generic custom hooks
│   │   ├── useDebounce.js
│   │   ├── useLocalStorage.js
│   │   └── useWindowSize.js
│   ├── utils/              # Pure utility functions
│   │   ├── formatDate.js
│   │   ├── formatCurrency.js
│   │   └── validators.js
│   └── types/              # TypeScript types (shared)
├── pages/                  # Route components (thin wrappers)
│   ├── HomePage.jsx
│   ├── ProductsPage.jsx
│   └── CheckoutPage.jsx
├── assets/                 # Static files
│   ├── images/
│   └── fonts/
├── styles/                 # Global styles
│   ├── globals.css
│   └── variables.css
├── mocks/                  # MSW handlers (testing)
│   ├── handlers.js
│   └── server.js
└── config/                 # App configuration
    ├── constants.js
    └── env.js
```

**Component folder pattern:**
```
Button/
├── Button.jsx          # Component
├── Button.test.jsx     # Tests (co-located)
├── Button.module.css   # Styles
└── index.js            # Re-export: export { default } from './Button'
```

**Barrel exports (index.js):**
```js
// features/auth/index.js
export { default as LoginForm } from './components/LoginForm';
export { default as RegisterForm } from './components/RegisterForm';
export { useAuth } from './hooks/useAuth';
export { authApi } from './api/authApi';
// authSlice internal only — not exported
```

**Import rules:**
```js
// ✅ features একে অপরের internals import করে না
import { LoginForm } from '@/features/auth'; // barrel থেকে

// ❌ cross-feature direct import
import LoginForm from '@/features/auth/components/LoginForm'; // avoid

// ✅ shared-এ যা কেউ ব্যবহার করতে পারে
import { Button } from '@/shared/components/Button';
import { useDebounce } from '@/shared/hooks/useDebounce';
```

---

**Topic 10: Git Workflow ও Conventional Commits**

**Feature Branch Workflow:**
```bash
# 1. main থেকে feature branch তৈরি
git checkout main && git pull origin main
git checkout -b feature/user-authentication

# 2. কাজ করুন, ছোট commits করুন
git add src/features/auth/
git commit -m "feat(auth): add login form with validation"

# 3. Push করুন
git push origin feature/user-authentication

# 4. Pull Request তৈরি করুন GitHub-এ
# 5. Code review → merge → branch delete
```

**Conventional Commits format:**
```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

**Types:**
```
feat:     নতুন feature
fix:      bug fix
docs:     documentation change
style:    formatting (no logic change)
refactor: code restructure (no feature/fix)
test:     test add/fix
chore:    build, dependency update
perf:     performance improvement
ci:       CI/CD config change
```

**Examples:**
```bash
git commit -m "feat(auth): add JWT refresh token rotation"
git commit -m "fix(cart): prevent negative quantity on decrement"
git commit -m "docs(readme): add setup instructions for Windows"
git commit -m "refactor(products): extract product card to shared component"
git commit -m "test(auth): add login form validation tests"
git commit -m "chore: upgrade React to 18.3.1"
git commit -m "perf(images): lazy load product images below fold"

# Breaking change
git commit -m "feat(api)!: rename userId to user_id in responses

BREAKING CHANGE: API response shape changed.
Old: { userId: 1 }
New: { user_id: 1 }"
```

**Useful Git commands:**
```bash
# Interactive rebase — commits clean করুন
git rebase -i HEAD~3

# Stash — অসম্পূর্ণ কাজ সরিয়ে রাখুন
git stash push -m "WIP: cart feature"
git stash pop

# Cherry-pick — specific commit নিন
git cherry-pick abc1234

# Bisect — কোন commit bug আনল খুঁজুন
git bisect start
git bisect bad HEAD
git bisect good v1.0.0

# Log — সুন্দর format
git log --oneline --graph --decorate --all
```

**Branch naming convention:**
```
feature/user-authentication
feature/product-search-filter
fix/cart-quantity-bug
fix/login-redirect-issue
hotfix/security-xss-fix
chore/upgrade-dependencies
release/v2.1.0
```

**Pull Request best practices:**
```
✅ PR ছোট রাখুন (300 lines এর নিচে)
✅ Screenshot/GIF add করুন (UI change হলে)
✅ Description-এ "what" এবং "why" লিখুন
✅ Reviewers assign করুন
✅ Draft PR — কাজ চলার সময়
✅ Squash merge — clean history রাখতে
✅ Delete branch after merge
```

---

**PART 13 Quick Revision Table**

| বিষয় | মূল কথা |
|------|---------|
| Testing Pyramid | Unit (বেশি) → Integration → E2E (কম) |
| RTL philosophy | Behavior test করুন, implementation না |
| getBy vs queryBy vs findBy | error/null/Promise |
| MSW কী? | Network level mock — realistic testing |
| jest-axe কী? | Automated accessibility violation detect |
| ESLint কী করে? | Code quality rules enforce করে |
| Prettier কী করে? | Code formatting auto-fix করে |
| Feature-based structure | Feature folder-এ related সব কিছু |
| Barrel export কী? | index.js দিয়ে public API define করা |
| Conventional Commits | `type(scope): description` format |
| Husky কী? | Git hooks — commit-এ auto lint/test |
| Feature branch workflow | main → branch → PR → review → merge |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part14"></a>
## PART 14: Bangladeshi Interview Preparation

> এই PART শুধুমাত্র বাংলাদেশি job market-এর জন্য। Company profiles, salary expectations, CV tips, behavioral questions — সব কিছু বাস্তব অভিজ্ঞতার ভিত্তিতে।

| # | বিষয় |
|---|-------|
| 1 | BD Tech Job Market Overview |
| 2 | Top IT Companies — Profiles ও Culture |
| 3 | Salary Guide (2025) |
| 4 | CV ও GitHub Portfolio Tips |
| 5 | Interview Process — Step by Step |
| 6 | Behavioral Questions in Bangla |
| 7 | Technical Phone/Video Interview Tips |
| 8 | Live Coding ও Whiteboard Tactics |
| 9 | Remote ও Freelance Opportunities |
| 10 | Career Growth Roadmap |

---

**Topic 1: BD Tech Job Market Overview**

**Bangladesh-এর IT sector (2025 snapshot):**
```
Software export: $1.4 billion+ (rapidly growing)
IT professionals: 700,000+
Major hubs: Dhaka (Gulshan, Banani, Uttara), Chittagong, Sylhet
Growth areas: Fintech, e-commerce, health tech, edtech
Remote work: বাড়ছে (post-COVID permanent shift)
```

**Job types:**
| Type | Company | Salary Range | Work Style |
|------|---------|--------------|-----------|
| Software Development | IT firms, product co. | 25k–120k BDT | Office/Hybrid |
| Frontend Engineer | Startups, agencies | 30k–100k BDT | Often remote-friendly |
| Full-stack | All types | 35k–130k BDT | Mixed |
| Remote (foreign client) | Freelance/remote first | $1,000–5,000/month | Home |
| Freelancing | Upwork, Fiverr | Variable | Home |

**Job portals:**
```
🇧🇩 Local: bdjobs.com, prothomalo jobs, chakri.com
🌐 International: LinkedIn, Indeed, RemoteOK, We Work Remotely
💻 Tech-specific: GitHub Jobs, Stack Overflow Jobs
📱 Network: LinkedIn, local Facebook groups (BD Developer Community)
```

---

**Topic 2: Top IT Companies — Profiles ও Culture**

**Brain Station 23**
```
Type: Service company (outsourcing + product)
Size: 1,000+ employees
Tech stack: Java, .NET, React, Angular, Python
Location: Dhaka (Banani), remote options
Interview: 3 rounds — HR, Technical, Final
Culture: Professional, structured, good L&D
Perks: Health insurance, training budget, annual increment
Junior SWE: 30,000 – 45,000 BDT
```

**Therap (BD) Ltd.**
```
Type: US-based product company (healthcare)
Size: 500+ (BD office)
Tech stack: Java, React, PostgreSQL
Location: Dhaka (Gulshan)
Interview: Online test + 2 technical rounds
Culture: Quality-focused, process-driven, stable
Perks: Best salary in BD for junior, USA standard product
Junior SWE: 40,000 – 60,000 BDT
```

**BJIT Group**
```
Type: Japanese outsourcing
Size: 1,000+ employees
Tech stack: Java, React, TypeScript, embedded
Location: Dhaka (Gulshan)
Interview: Written test + technical + HR
Culture: Disciplined, Japanese work culture influence
Perks: Japan training opportunity, stable employment
Junior SWE: 35,000 – 55,000 BDT
```

**Enosis Solutions**
```
Type: US/UK outsourcing
Size: 300+
Tech stack: .NET, React, Vue, TypeScript
Location: Dhaka (Uttara)
Interview: Coding test + 2 technical rounds
Culture: Collaborative, clean code focus, code review culture
Perks: Good tech exposure, growth opportunities
Junior SWE: 30,000 – 50,000 BDT
```

**Kaz Software**
```
Type: US outsourcing
Size: 200+
Tech stack: React, Node.js, .NET, Python
Location: Dhaka (Dhanmondi)
Interview: Phone screening + technical + HR
Culture: Flexible, work-life balance good
Junior SWE: 25,000 – 40,000 BDT
```

**Product Companies (BD-based):**

| Company | Product | Tech | Junior Range |
|---------|---------|------|-------------|
| Chaldal | Grocery delivery | React, Django | 35k–55k |
| Shajgoj | Beauty e-commerce | React, Laravel | 30k–50k |
| 10 Minute School | EdTech | React, Node | 30k–50k |
| ShopUp | B2B commerce | React, Go | 35k–60k |
| bKash (FinTech) | Mobile banking | React, Java | 45k–70k |
| Pathao | Ride/Delivery | React Native | 40k–65k |

**Startups ও Agencies:**
```
Advantage: Fast learning, ownership, flexible
Disadvantage: Unstable, salary inconsistent, less process
Tip: Good for 1-2 years experience building, then move
```

---

**Topic 3: Salary Guide (2025)**

**Frontend/React Developer Salary (Dhaka, BDT/month):**

| Level | Experience | Range | Notes |
|-------|-----------|-------|-------|
| Junior | 0–1 year | 20,000–40,000 | Fresh graduate |
| Junior-Mid | 1–2 years | 35,000–60,000 | After 1st job |
| Mid-level | 2–4 years | 55,000–100,000 | Strong portfolio |
| Senior | 4–7 years | 90,000–160,000 | Lead/architect |
| Principal/Lead | 7+ years | 150,000–250,000+ | Rare, negotiable |

**Salary factors:**
```
✅ Company type: Product > Outsourcing > Agency
✅ Tech stack: React+TypeScript > React alone
✅ English skill: Fluent = +20-30% premium
✅ Portfolio: Strong projects = skip 1 level
✅ Referral: Network hire pays more
✅ Negotiation: Always negotiate (80% room)
```

**Remote (foreign company) earnings:**
```
Entry remote: $500–1,200/month
Mid remote: $1,500–3,000/month
Senior remote: $3,000–7,000/month

Companies hiring BD developers remotely:
- Toptal (top 3%, but premium rates)
- Arc.dev
- X-Team
- Remote-first startups (LinkedIn "remote" filter)
- Upwork (freelance platform)
```

**Increment pattern:**
```
Year 1: 15–25% increment (if performing well)
Year 2: 20–30% (or job change for 40-60% jump)
Tip: Job change every 2-3 years = fastest salary growth
```

---

**Topic 4: CV ও GitHub Portfolio Tips**

**CV essentials (1 page, PDF format):**
```
✅ Header: নাম, email, phone, GitHub URL, LinkedIn URL, portfolio URL
✅ Summary: 2-3 lines — কী করেন, কী জানেন, কী খুঁজছেন
✅ Skills: React, JavaScript, TypeScript, Next.js, Redux, REST API, Git
✅ Projects: 2-3 best project (GitHub link + live demo)
✅ Experience: Role, company, duration, 2-3 bullet achievements
✅ Education: University, degree, CGPA (3.0+ হলে দিন)
✅ Certifications: Meta React, Udemy certificates (relevant হলে)
```

**CV mistakes এড়িয়ে চলুন:**
```
❌ "Responsible for..." → ✅ "Built...", "Reduced...", "Increased..."
❌ Objective section (outdated)
❌ References available upon request
❌ Photo (বেশিরভাগ modern companies prefer না)
❌ Buzzwords without evidence: "passionate", "team player"
❌ Typos ও grammar errors
❌ 2+ pages (junior-এর জন্য)
```

**GitHub Profile:**
```
✅ Profile README — নিজের intro, skills, stats
✅ Pinned repositories — 6টি best project pin করুন
✅ Green contribution graph — daily commit habit
✅ Project README — screenshot, live demo link, tech stack, setup guide
✅ Commit messages: conventional commits follow করুন
✅ Issues + PRs — open source contribute করুন (যেকোনো ছোট repo)
```

**Profile README template:**
```markdown
# Hi, I'm [Name] 👋

React/Frontend Developer from Bangladesh 🇧🇩

**Currently:** Junior SWE @ [Company] | Open to remote opportunities

**Tech Stack:**
React · TypeScript · Next.js · Redux Toolkit · Tailwind CSS · Node.js

**Projects:**
- [E-Commerce App](link) — React, Redux, Stripe integration
- [Kanban Board](link) — Drag & Drop, Zustand, TypeScript
- [Blog Platform](link) — Next.js, MDX, SEO optimized

📫 [your@email.com](mailto:your@email.com) | [LinkedIn](link)
```

**Portfolio website:**
```
✅ Domain: yourname.dev বা yourname.com (yearly ~$15)
✅ Tech: Next.js + Vercel (free hosting, fast)
✅ Content: Projects with screenshots + tech badges
✅ About: Brief story + contact form
✅ Blog: Technical articles (bonus — shows expertise)
✅ Mobile responsive + fast loading
```

---

**Topic 5: Interview Process — Step by Step**

**Typical BD IT Company Process:**

```
1️⃣  CV Screening (HR)
    └── ATS system → human review
    └── LinkedIn/Referral → faster

2️⃣  HR Phone Screening (15-30 min)
    └── Background, salary expectation, availability
    └── Basic English check

3️⃣  Online Assessment / Home Assignment (1-3 days)
    └── Coding test (HackerRank / custom)
    └── Or: Small project assignment
    
4️⃣  Technical Interview Round 1 (1 hour)
    └── JavaScript fundamentals
    └── React concepts
    └── Problem solving (1-2 problems)

5️⃣  Technical Interview Round 2 / System Design (30-60 min)
    └── Project walkthrough
    └── Architecture discussion
    └── Senior/Lead interviewer

6️⃣  Final / Culture Fit (30 min)
    └── Behavioral questions
    └── Team intro
    └── Q&A session

7️⃣  Offer → Negotiation → Acceptance
```

**Product company process (Chaldal, Therap, etc.) — stricter:**
```
→ Online test (DSA + system thinking)
→ Technical round 1: Live coding
→ Technical round 2: System design + past projects
→ Bar raiser / culture interview
→ Offer
```

**Preparation timeline:**
```
2 weeks before: DSA basics (Arrays, String, HashMap, Sorting)
1 week before: React deep dive, project walkthrough practice
3 days before: Behavioral answers, company research
1 day before: Light review, good sleep, outfit ready
```

---

**Topic 6: Behavioral Questions in Bangla**

Interview-এ Bangla বা English দুটোতেই answer দেওয়া যায়। **STAR format** follow করুন: **S**ituation → **T**ask → **A**ction → **R**esult।

---

**"নিজের সম্পর্কে বলুন" (Tell me about yourself):**
```
"আমার নাম [নাম]। আমি [বিশ্ববিদ্যালয়] থেকে CSE/SE graduation করেছি [সাল]-এ।
গত [X মাস/বছর] ধরে React এবং JavaScript নিয়ে কাজ করছি।
আমার সবচেয়ে notable project হলো [project name] — যেখানে আমি [feature/achievement]।
এখন আমি এমন একটি position খুঁজছি যেখানে [growth/impact/technology]।"
```

**"আপনার সবচেয়ে বড় weakness কী?"**
```
"আমি মাঝে মাঝে perfectionism-এ পড়ে যাই — একটা feature ঠিকমতো না হওয়া পর্যন্ত
submit করতে চাই না। তবে এখন আমি শিখেছি 'good enough to ship' mindset রাখতে।
Time-box করি — এতটুকু সময় দেব, তারপর submit করব।"
```

**"Deadline miss হয়েছে কখনো? কী করেছিলেন?"**
```
"হ্যাঁ, একবার [project]-এ আমার estimate ভুল ছিল। API integration-এ expected-এর
double সময় লেগেছে। আমি immediately team lead-কে জানিয়েছি, scope কমিয়ে MVP
deliver করেছি, এবং পরে missing features আনা হয়েছে। শিখেছি: estimate-এ buffer রাখতে
এবং আগে blocker জানাতে।"
```

**"Team conflict কীভাবে handle করেছেন?"**
```
"একবার code review-তে colleague আমার approach নিয়ে disagreement ছিল।
আমি first সুনেছি তার point of view, তারপর আমার reasoning explain করেছি।
শেষে আমরা একটি third approach-এ agree করেছি যেটা দুজনেরই better মনে হয়েছে।
Technical disagreement-এ data আর evidence দিয়ে কথা বলি — personal করি না।"
```

**"কেন এই company-তে join করতে চান?"**
```
"[Company] এর product আমি actually use করি — [product name]। আমি দেখেছি
[specific feature/problem] যেটা interesting। আপনাদের tech stack (React + TypeScript)
আমি use করছি, এবং আমার [specific skill] এখানে contribute করতে পারব।
এছাড়া আপনাদের engineering culture সম্পর্কে [source]-এ পড়েছি — learning culture
আমার কাছে important।"
```

**"৫ বছর পরে নিজেকে কোথায় দেখছেন?"**
```
"৫ বছর পরে আমি একজন senior-level engineer হতে চাই যে technical decisions নিতে
পারে এবং junior developers-দের mentor করতে পারে। আমি open source-এ contribute
করতে এবং হয়তো একটি product build করতে চাই। Short-term goal হলো এখানে
strong foundation গড়া এবং real-world large codebase-এর experience নেওয়া।"
```

**"Salary expectation কত?"**
```
Strategy: Research করুন → Range দিন → Anchor high

"আমি research করে দেখেছি এই role-এর জন্য Dhaka-তে [range] typical।
আমার skills ও experience বিবেচনায় আমি [X] থেকে [Y] expect করছি।
তবে total package (benefits, growth, learning) এর উপরও নির্ভর করে।"
```

---

**Topic 7: Technical Phone/Video Interview Tips**

**আগে:**
```
✅ Company research: product, tech blog, recent news
✅ নিজের project ২-৩টি ভালো করে practice করুন (30 sec pitch)
✅ Quiet environment নিশ্চিত করুন
✅ Camera, mic, internet test করুন
✅ Code editor ready রাখুন (VS Code বা CodeSandbox)
✅ Water glass রাখুন
✅ Resume প্রিন্ট বা screen-এ খোলা রাখুন
```

**Interview-এ:**
```
✅ প্রশ্ন না বুঝলে clarify করুন — guess করবেন না
✅ Think aloud করুন — "আমি ভাবছি X approach নেব কারণ..."
✅ জানেন না → "এই specific syntax মনে নেই তবে এভাবে approach করব..."
✅ Body language: সোজা বসুন, camera-তে তাকান (screen নয়)
✅ Specific উদাহরণ দিন — abstract answer এড়িয়ে চলুন
✅ প্রশ্ন করুন শেষে (genuine curiosity দেখান)
```

**শেষে জিজ্ঞেস করুন:**
```
"এই role-এ প্রথম ৩০ দিনে কী করা expect করা হয়?"
"Team-এর biggest technical challenge এখন কী?"
"Engineering culture সম্পর্কে বলবেন — code review কীভাবে হয়?"
"এই position কি recently তৈরি হয়েছে নাকি কেউ leave করেছেন?"
```

---

**Topic 8: Live Coding ও Whiteboard Tactics**

**Live coding-এ common patterns:**

**React component build:**
```jsx
// Interviewer: "একটি todo app বানান"
// আপনি প্রথমে structure জিজ্ঞেস করুন:
// - State কোথায় থাকবে?
// - Persist করতে হবে?
// - Delete/edit feature দরকার?

function TodoApp() {
  const [todos, setTodos] = useState([]);
  const [input, setInput] = useState('');

  const addTodo = () => {
    if (!input.trim()) return;
    setTodos(prev => [...prev, { id: Date.now(), text: input, done: false }]);
    setInput('');
  };

  const toggleTodo = (id) => {
    setTodos(prev => prev.map(t => t.id === id ? { ...t, done: !t.done } : t));
  };

  const deleteTodo = (id) => {
    setTodos(prev => prev.filter(t => t.id !== id));
  };

  return (
    <div>
      <input value={input} onChange={e => setInput(e.target.value)}
        onKeyDown={e => e.key === 'Enter' && addTodo()} />
      <button onClick={addTodo}>Add</button>
      <ul>
        {todos.map(todo => (
          <li key={todo.id} style={{ textDecoration: todo.done ? 'line-through' : 'none' }}>
            <span onClick={() => toggleTodo(todo.id)}>{todo.text}</span>
            <button onClick={() => deleteTodo(todo.id)}>×</button>
          </li>
        ))}
      </ul>
    </div>
  );
}
```

**Algorithm question strategy:**
```
1. প্রশ্ন সম্পূর্ণ বুঝুন — edge cases জিজ্ঞেস করুন
2. Example দিয়ে নিজে verify করুন
3. Brute force approach প্রথমে বলুন
4. Optimize করুন — "O(n²) থেকে O(n) করা যায় HashMap দিয়ে"
5. Code লিখুন — clean, readable
6. Test করুন — edge cases: empty, single element, duplicates
```

**Common patterns Bangladeshi interviews-এ:**
```js
// Two Sum (HashMap)
function twoSum(nums, target) {
  const map = new Map();
  for (let i = 0; i < nums.length; i++) {
    const complement = target - nums[i];
    if (map.has(complement)) return [map.get(complement), i];
    map.set(nums[i], i);
  }
  return [];
}

// Reverse String
const reverseStr = str => str.split('').reverse().join('');

// Palindrome Check
const isPalindrome = str => {
  const clean = str.toLowerCase().replace(/[^a-z0-9]/g, '');
  return clean === clean.split('').reverse().join('');
};

// FizzBuzz (এখনো জিজ্ঞেস হয়!)
for (let i = 1; i <= 100; i++) {
  if (i % 15 === 0) console.log('FizzBuzz');
  else if (i % 3 === 0) console.log('Fizz');
  else if (i % 5 === 0) console.log('Buzz');
  else console.log(i);
}

// Array flatten
const flatten = arr => arr.reduce((acc, val) =>
  Array.isArray(val) ? acc.concat(flatten(val)) : acc.concat(val), []);

// Debounce (বহুবার জিজ্ঞেস হয়)
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}
```

---

**Topic 9: Remote ও Freelance Opportunities**

**Remote job পাওয়ার strategy:**

**Step 1 — English communication strong করুন:**
```
✅ Daily English writing practice (dev.to, Medium-এ article)
✅ GitHub commit messages ও PR descriptions English-এ
✅ LinkedIn-এ English-এ post করুন
✅ Mock interview English-এ practice করুন
```

**Step 2 — Platform-based approach:**
```
Upwork (সবচেয়ে accessible):
- Profile 100% complete করুন
- First 3 months: low-rate bids করুন reviews পেতে
- Niche specialize করুন (React + TypeScript + Next.js)
- Portfolio দিন, proposal personalize করুন

Fiverr:
- Gig: "I will build React web app with TypeScript"
- Fast delivery option রাখুন (+fee)
- Package tiers: Basic/Standard/Premium

Toptal/Arc.dev (premium):
- Screening process কঠিন কিন্তু rates high
- 1-2 বছর experience পরে apply করুন
```

**Step 3 — LinkedIn remote job hunting:**
```
Profile: "Open to Work" → Remote positions
Search: "React developer remote" → Filter: Remote
Keywords: "Remote-first", "Fully remote", "Work from anywhere"
Timezone overlap: EU startups often accept BD timezone
```

**Remote work setup:**
```
Hardware:
- Laptop: 16GB RAM minimum (development heavy)
- Backup internet (mobile hotspot)
- Good headphones (noise-cancelling preferred)
- Webcam (if built-in is bad)

Software:
- Slack/Teams: communication
- Zoom/Google Meet: video calls
- Notion/Linear: project management
- GitHub/GitLab: code collaboration

Productivity:
- Fixed working hours রাখুন
- Daily standup attend করুন
- Proactive communication — no radio silence
- Time zone: "I'm UTC+6" — calendar shared রাখুন
```

**Freelance rates (BD developer, 2025):**
```
Beginner (0-1yr): $5-15/hour
Junior (1-2yr): $15-30/hour
Mid (2-4yr): $30-60/hour
Senior (4+yr): $60-120/hour

Project-based:
- Landing page: $200-500
- React app (medium): $1,000-3,000
- Full-stack app: $3,000-10,000+
```

---

**Topic 10: Career Growth Roadmap**

**Junior React Developer → Senior Engineer (5-year path):**

```
Year 0-1: Foundation
├── Strong JS fundamentals (closures, async, prototypes)
├── React basics + hooks mastery
├── 2-3 personal projects on GitHub
├── First job (any good company)
└── Goal: Learn team workflow, code review culture

Year 1-2: Mid-junior
├── TypeScript add করুন
├── State management (Redux Toolkit / Zustand)
├── Testing (RTL + Jest)
├── Next.js basics
└── Goal: Own features end-to-end, first promotion

Year 2-3: Mid-level
├── System design basics
├── Performance optimization expertise
├── CI/CD, Docker basics
├── Tech blog / open source contributions শুরু
└── Goal: Lead small features, mentor juniors, job switch for 40%+ raise

Year 3-4: Mid-Senior
├── Full-stack capability (Node.js / backend basics)
├── Architecture decisions contribute
├── Team leadership experience
├── Speaking at meetups / writing articles
└── Goal: Senior title, significant salary jump

Year 4-5: Senior
├── System design complex apps
├── Engineering roadmap decisions
├── Cross-team collaboration
├── Remote senior role (international market)
└── Goal: $3,000+/month remote or 150k+ BDT local
```

**Skills priority order (2025 BD market):**
```
Tier 1 (Must have):
  React, JavaScript ES6+, Git, REST API, responsive CSS

Tier 2 (Strong advantage):
  TypeScript, Next.js, Testing (RTL/Jest), Redux Toolkit

Tier 3 (Senior level):
  System Design, Docker/K8s basics, CI/CD, Performance

Tier 4 (Specialist):
  React Native, GraphQL, Web3, AI integration
```

**Learning resources (free/affordable):**
```
Documentation:
  react.dev (official, best), nextjs.org/docs, javascript.info

YouTube:
  Traversy Media, Codevolution, Jack Herrington, Theo (t3)
  বাংলা: Stack Learner, Learn with Sumit, Programming Hero

Courses:
  Epic React (Kent C. Dodds) — best React course
  Total TypeScript (Matt Pocock)
  Josh W Comeau CSS courses
  Udemy (sale-এ $10-15)

Practice:
  LeetCode (Easy/Medium), Frontend Mentor (UI challenges)
  GreatFrontEnd (frontend-specific)

Community:
  BD Developer Community (Facebook Group)
  React Bangladesh (local meetup)
  dev.to (English articles লিখুন)
  Twitter/X: follow Kent C. Dodds, Dan Abramov, Theo
```

**Networking in BD:**
```
✅ LinkedIn active থাকুন — Bengali IT people connect করুন
✅ Bangladesh Developer Conference attend করুন
✅ Local React meetup যোগ দিন
✅ Open source: বাংলাদেশি founders-দের project-এ PR দিন
✅ Ex-colleagues network maintain করুন — referral সবচেয়ে effective
✅ Alumni network use করুন — BUET/SUST/KUET groups
```

**Offer receive করলে:**
```
1. লিখিত offer চান — verbal accept করবেন না
2. সব terms review করুন: salary, benefits, notice period, probation
3. Counter offer দিন (10-15% more ask করুন)
4. Current employer-এর counter offer — সতর্ক থাকুন
5. Joining date negotiation — notice period clear করুন
6. Background check / bond — read carefully
```

---

**PART 14 Quick Revision Table**

| বিষয় | মূল কথা |
|------|---------|
| Top paying company | Therap BD > BJIT > Brain Station 23 > Enosis |
| Junior salary range | 20,000–45,000 BDT (Dhaka, 2025) |
| Remote entry level | $500–1,200/month |
| CV length | 1 page, PDF, no photo |
| GitHub must-have | Profile README + 6 pinned repos + green graph |
| Interview rounds | HR → Test → Tech 1 → Tech 2 → Offer |
| STAR format | Situation → Task → Action → Result |
| Salary negotiation | Always counter, anchor high, range দিন |
| Top freelance platform | Upwork (most accessible for BD) |
| Career switch | Job change every 2-3yr = fastest growth |
| Must-learn skills | React + TypeScript + Next.js + Testing |
| BD community | BD Developer Community Facebook Group |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **🎉 সম্পূর্ণ হয়েছে!** React Junior Engineer Handbook — সকল 14টি PART লেখা শেষ।
>
> **Handbook Summary:**
> - PART 1–2: React Fundamentals + Hooks
> - PART 3–4: Architecture + Routing
> - PART 5–6: State Management + API Integration
> - PART 7–8: Performance + Advanced React
> - PART 9–10: Auth + Projects
> - PART 11–12: Interview Q&A + Next.js
> - PART 13–14: Testing + BD Career Guide
