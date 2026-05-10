<a id="top"></a>

<div align="center">

# 📊 DSA Interview Preparation Handbook
## বাংলাদেশের Junior Software Engineer ইন্টারভিউয়ের জন্য সম্পূর্ণ DSA গাইড

**লেখক:** Senior Software Engineer, Competitive Programmer & DSA Instructor  
**লক্ষ্য:** বাংলাদেশের শীর্ষ সফটওয়্যার কোম্পানিতে Junior SWE পদে চাকরি পাওয়া  
**ভাষা:** বাংলা (Technical terms ইংরেজিতে)

</div>

---

<a id="toc"></a>

## 📋 সূচিপত্র (Table of Contents)

| # | PART | বিষয়বস্তু |
|---|------|-----------|
| 📘 | [**PART 1** — DSA Fundamentals](#part1) | Data Structure, Algorithm, Time/Space Complexity, Big O, Recursion, Memory |
| 📗 | [**PART 2** — Arrays & Strings](#part2) | Array, Prefix Sum, Sliding Window, Two Pointer, Kadane, Binary Search, Matrix |
| 📙 | [**PART 3** — Linked List](#part3) | Singly/Doubly/Circular LL, Insert/Delete, Reverse, Cycle Detection, Floyd, Merge |
| 📕 | [**PART 4** — Stack & Queue](#part4) | Stack, Queue, Circular Queue, Deque, Priority Queue, Monotonic Stack, Expression Eval |
| 📓 | **PART 5** — Trees & Binary Trees | *(শীঘ্রই আসছে)* |
| 📔 | **PART 6** — Graphs | *(শীঘ্রই আসছে)* |
| 📒 | **PART 7** — Sorting & Searching | *(শীঘ্রই আসছে)* |
| 📃 | **PART 8** — Dynamic Programming & Greedy | *(শীঘ্রই আসছে)* |
| 📄 | **PART 9** — Advanced DSA | *(শীঘ্রই আসছে)* |
| 🗒️ | **PART 10** — Coding Interview Q&A | *(শীঘ্রই আসছে)* |
| 🗓️ | **PART 11** — Problem Solving Strategy | *(শীঘ্রই আসছে)* |
| 🗃️ | **PART 12** — Bangladeshi Interview Prep | *(শীঘ্রই আসছে)* |

---

<details>
<summary><strong>📘 PART 1 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [১.১ Data Structure কী?](#১১-data-structure-কী)
- [১.২ Algorithm কী?](#১২-algorithm-কী)
- [১.৩ DSA কেন গুরুত্বপূর্ণ?](#১৩-dsa-কেন-গুরুত্বপূর্ণ)
- [১.৪ Time Complexity](#১৪-time-complexity)
- [১.৫ Space Complexity](#১৫-space-complexity)
- [১.৬ Big O Notation](#১৬-big-o-notation)
- [১.৭ Big Omega ও Big Theta](#১৭-big-omega-ও-big-theta)
- [১.৮ Best, Average, Worst Case](#১৮-best-average-worst-case)
- [১.৯ Recursion](#১৯-recursion)
- [১.১০ Iteration](#১১০-iteration)
- [১.১১ Memory Concepts](#১১১-memory-concepts)
- [১.১২ Stack vs Heap Memory](#১১২-stack-vs-heap-memory)
- [১.১৩ PART 1 — Interview Q&A](#১১৩-part-1--interview-qa)

</details>

<details>
<summary><strong>📗 PART 2 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [২.১ Array Basics](#২১-array-basics)
- [২.২ Static vs Dynamic Array](#২২-static-vs-dynamic-array)
- [২.৩ String Operations](#২৩-string-operations)
- [২.৪ Prefix Sum](#২৪-prefix-sum)
- [২.৫ Sliding Window](#২৫-sliding-window)
- [২.৬ Two Pointer](#২৬-two-pointer)
- [২.৭ Kadane's Algorithm](#২৭-kadanes-algorithm)
- [২.৮ Binary Search](#২৮-binary-search)
- [২.৯ Matrix Operations](#২৯-matrix-operations)
- [২.১০ PART 2 — Interview Q&A](#২১০-part-2--interview-qa)

</details>

---

<a id="part1"></a>

# PART 1: DSA Fundamentals (মূল ধারণাসমূহ)

> **পড়ার নির্দেশনা:** এই PART টি DSA এর একদম গোড়ার ধারণাগুলো নিয়ে। Interview তে এগুলো সরাসরি জিজ্ঞেস করা হয়। প্রতিটি topic এর definition, analogy, এবং interview-style উত্তর মুখস্থ না করে বুঝে পড়ুন।

---

## ১.১ Data Structure কী?

### সংজ্ঞা (Definition)

**Data Structure** হলো data organize, store এবং manage করার একটি নির্দিষ্ট পদ্ধতি যেন সেই data কে efficiently access ও modify করা যায়।

সহজ ভাষায়: **"Data কে সাজিয়ে রাখার নিয়ম।"**

### বাস্তব জীবনের উদাহরণ (Real-life Analogy)

```
📚 বইয়ের তাক (Array):
   → বই গুলো একটার পর একটা সাজানো থাকে
   → Index দিয়ে যেকোনো বই সরাসরি পাওয়া যায়

📋 Queue (লাইন):
   → ব্যাংকে লাইনে যে আগে আসে সে আগে সেবা পায়
   → FIFO (First In First Out)

📚 Stack (বই এর স্তুপ):
   → উপর থেকে বই রাখা হয়, উপর থেকেই তোলা হয়
   → LIFO (Last In First Out)

🗂️ Dictionary (Hash Map):
   → নাম দিলে তার নম্বর বের হয় — key-value pair
```

### Data Structure এর প্রকারভেদ

```
Data Structures
├── Linear (একমাত্রিক)
│   ├── Array
│   ├── Linked List
│   ├── Stack
│   └── Queue
└── Non-Linear (বহুমাত্রিক)
    ├── Tree
    │   ├── Binary Tree
    │   ├── BST
    │   ├── Heap
    │   └── Trie
    └── Graph
```

### Interview-style উত্তর

**প্রশ্ন: "Data Structure কী?"**

> "Data Structure হলো data কে একটি নির্দিষ্ট pattern এ organize করার পদ্ধতি যাতে নির্দিষ্ট operation গুলো efficiently করা যায়। যেমন — Array তে random access O(1) এ হয়, কিন্তু Linked List এ O(n) লাগে। Problem এর nature অনুযায়ী সঠিক Data Structure বেছে নেওয়াই ভালো programmer এর কাজ।"

### সাধারণ ভুল (Common Mistakes)

```
❌ "Data Structure মানে শুধু Array আর Linked List"
✅ Tree, Graph, Hash Table, Heap সবই Data Structure

❌ "সব সমস্যায় Array ব্যবহার করব"
✅ Problem দেখে কোন DS সবচেয়ে উপযুক্ত তা বুঝতে হবে

❌ "Data Structure শুধু theory"
✅ প্রতিটি real application এ specific DS ব্যবহার হয়
```

### Follow-up Interview Questions

1. Linear ও Non-linear data structure এর পার্থক্য কী?
2. কোন data structure কখন ব্যবহার করবেন?
3. Abstract Data Type (ADT) কী?

---

## ১.২ Algorithm কী?

### সংজ্ঞা

**Algorithm** হলো একটি নির্দিষ্ট সমস্যা সমাধানের জন্য step-by-step নির্দেশনার সমষ্টি। প্রতিটি step সুনির্দিষ্ট, limited, এবং terminate হয়।

একটি ভালো Algorithm এর ৫টি বৈশিষ্ট্য:

| বৈশিষ্ট্য | ব্যাখ্যা |
|----------|---------|
| **Input** | ০ বা তার বেশি input নিতে পারে |
| **Output** | কমপক্ষে ১টি output দিতে হবে |
| **Definiteness** | প্রতিটি step স্পষ্ট ও অস্পষ্টতামুক্ত |
| **Finiteness** | নির্দিষ্ট সংখ্যক step এ শেষ হতে হবে |
| **Effectiveness** | প্রতিটি step বাস্তবে কার্যকর হওয়া সম্ভব |

### বাস্তব উদাহরণ

```
রান্নার Recipe = Algorithm:
  Step 1: চুলায় তেল দিন
  Step 2: পেঁয়াজ কুঁচি দিয়ে ভাজুন
  Step 3: মসলা দিন
  Step 4: মাংস দিন
  Step 5: পানি দিয়ে ঢাকুন
  → সুনির্দিষ্ট steps, নির্দিষ্ট output (রান্না)
```

### Algorithm vs Program

| Algorithm | Program |
|-----------|---------|
| Language independent | Specific language এ লেখা |
| Design level | Implementation level |
| Pseudocode বা flowchart | Actual code |
| Finite steps | Infinite loop থাকতে পারে (OS) |

### Interview-style উত্তর

**প্রশ্ন: "Algorithm কী? একটি উদাহরণ দিন।"**

> "Algorithm হলো একটি সমস্যার step-by-step সমাধান পদ্ধতি যা finite সংখ্যক step এ শেষ হয়। উদাহরণ: দুটি সংখ্যার মধ্যে বড়টি বের করা — Step 1: a এবং b নিন, Step 2: যদি a > b হয় তাহলে a return করুন, Step 3: নাহলে b return করুন। এটি একটি simple algorithm।"

---

## ১.৩ DSA কেন গুরুত্বপূর্ণ?

### ক্যারিয়ারে গুরুত্ব

```
Top Companies Interview Process:
  Google, Facebook, Amazon → DSA problem solving = primary filter
  Brain Station 23, Kaz Software → DSA + Framework
  Pathao, Shohoz, Chaldal → DSA basics + System Design

কেন জানতে হবে?
  ✅ Efficient code লেখা যায় (fast + less memory)
  ✅ Complex problems ছোট ছোট ভাগে ভেঙে সমাধান করা যায়
  ✅ Interview এ confidence আসে
  ✅ Senior engineer হওয়ার ভিত্তি
```

### Real Project Impact

| ছাড়া DSA | সাথে DSA |
|----------|---------|
| N² loops সব জায়গায় | Optimal O(n log n) |
| Memory overflow | Efficient memory use |
| Slow API response | Fast query processing |
| Scale করা যায় না | Millions of users handle করা যায় |

---

## ১.৪ Time Complexity

### সংজ্ঞা

**Time Complexity** হলো input size (n) বাড়ার সাথে সাথে algorithm এর execution time কীভাবে বাড়ে তার পরিমাপ। এটি actual time নয় — operations এর সংখ্যার বৃদ্ধির হার।

> **মনে রাখুন:** Time complexity মাপা হয় **operations এর সংখ্যায়**, seconds এ নয়।

### উদাহরণ দিয়ে বোঝা

```python
# উদাহরণ ১: O(1) — Constant
def get_first(arr):
    return arr[0]   # সবসময় ১টি operation

# উদাহরণ ২: O(n) — Linear
def find_element(arr, target):
    for item in arr:    # n টি element হলে n বার চলে
        if item == target:
            return True
    return False

# উদাহরণ ৩: O(n²) — Quadratic
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):         # n বার
        for j in range(n-1):   # n বার → মোট n × n = n² operations
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

# উদাহরণ ৪: O(log n) — Logarithmic
def binary_search(arr, target):
    lo, hi = 0, len(arr) - 1
    while lo <= hi:
        mid = (lo + hi) // 2   # প্রতি step এ অর্ধেক বাদ
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            lo = mid + 1
        else:
            hi = mid - 1
    return -1
```

### কীভাবে Count করবেন

```
Rule 1: Constant operations → O(1)
  x = 5          → O(1)
  return arr[0]  → O(1)

Rule 2: Single loop 0 to n → O(n)
  for i in range(n): ...

Rule 3: Nested loop → O(n²)
  for i in range(n):
    for j in range(n): ...

Rule 4: Halving each step → O(log n)
  while n > 1: n = n // 2

Rule 5: Loop + halving → O(n log n)
  Merge Sort, Heap Sort

Rule 6: Constants বাদ দিন
  O(3n + 5) → O(n)
  O(2n² + 10n) → O(n²)

Rule 7: যে term সবচেয়ে দ্রুত বাড়ে সেটি রাখুন
  O(n² + n + log n) → O(n²)
```

---

## ১.৫ Space Complexity

### সংজ্ঞা

**Space Complexity** হলো input size (n) বাড়ার সাথে সাথে algorithm কতটুকু extra memory ব্যবহার করে তার পরিমাপ।

```
Total Space = Auxiliary Space + Input Space

Auxiliary Space = Algorithm এর নিজের জন্য extra memory
  (Input বাদ দিয়ে)
```

### উদাহরণ

```python
# O(1) Space — In-place
def reverse_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left += 1
        right -= 1
    # Extra variable মাত্র ২টি (left, right) → O(1)

# O(n) Space — Extra array
def reverse_copy(arr):
    n = len(arr)
    result = [0] * n    # n size এর নতুন array → O(n)
    for i in range(n):
        result[i] = arr[n-1-i]
    return result

# O(n) Space — Recursion stack
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n-1)
    # n টি recursive call → call stack এ n frame → O(n) space
```

### Time vs Space Trade-off

```
সাধারণত:
  → বেশি memory ব্যবহার করলে time কমে
  → কম memory ব্যবহার করলে time বাড়তে পারে

Example: Memoization
  → Extra O(n) space রেখে O(2ⁿ) → O(n) time এ আনা হয়
```

---

## ১.৬ Big O Notation

### সংজ্ঞা

**Big O Notation** হলো algorithm এর **worst case** time/space complexity express করার mathematical notation।

> O(f(n)) মানে: n বড় হলে algorithm এর running time f(n) এর সমানুপাতিক বা কম।

### Common Complexities (ছোট থেকে বড়)

| Notation | নাম | উদাহরণ | n=100 তে operations |
|----------|-----|---------|---------------------|
| O(1) | Constant | Array index access | 1 |
| O(log n) | Logarithmic | Binary Search | ~7 |
| O(n) | Linear | Linear Search | 100 |
| O(n log n) | Linearithmic | Merge Sort | ~664 |
| O(n²) | Quadratic | Bubble Sort | 10,000 |
| O(n³) | Cubic | Matrix multiplication (naive) | 1,000,000 |
| O(2ⁿ) | Exponential | Recursive Fibonacci | 2¹⁰⁰ (অকল্পনীয়!) |
| O(n!) | Factorial | Traveling Salesman (brute) | 100! (∞) |

### Growth Rate Visualization

```
O(1)      ████ (flat)
O(log n)  ████▌ (very slow growth)
O(n)      ████████████ (linear)
O(n log n)████████████████ (slightly above linear)
O(n²)     ████████████████████████████████ (steep)
O(2ⁿ)     ∞∞∞∞∞∞∞∞∞∞ (explosive)
```

### Rules মনে রাখার সহজ উপায়

```
🔑 Drop Constants:
   O(5n) → O(n)
   O(100) → O(1)

🔑 Drop Lower Order Terms:
   O(n² + n) → O(n²)
   O(n + log n) → O(n)

🔑 Different inputs, different variables:
   for a in arr_a:      → O(a)
     for b in arr_b:    → O(b)
   → O(a × b), না O(n²)

🔑 Nested loop দিয়ে multiply:
   for i in range(n):
     for j in range(n):  → O(n²)

🔑 Sequential loop দিয়ে add:
   for i in range(n): ...   → O(n)
   for j in range(n): ...   → O(n)
   Total → O(n + n) = O(2n) = O(n)
```

### Real Code Examples

```python
def analyze_complexities(n, arr):
    # O(1) — constant
    x = arr[0]

    # O(n) — single loop
    total = 0
    for i in range(n):
        total += arr[i]

    # O(log n) — binary search
    lo, hi = 0, n - 1
    while lo <= hi:
        mid = (lo + hi) // 2
        lo = mid + 1  # simplified

    # O(n²) — nested loop
    for i in range(n):
        for j in range(n):
            pass

    # O(n log n) — sorting
    arr.sort()  # TimSort

    # এই function এর overall: O(n log n) (dominant term)
```

---

## ১.৭ Big Omega ও Big Theta

### Big Omega — Ω(f(n))

**Best case** lower bound। Algorithm কমপক্ষে এতটুকু সময় নেবে।

```
Ω(f(n)): সবচেয়ে কম সময়ে যা লাগে

Example: Linear Search এ target প্রথম element হলে
→ Ω(1) — শুধু একবার check করতে হয়
```

### Big Theta — Θ(f(n))

Algorithm exactly f(n) অনুযায়ী চলে — upper bound ও lower bound একই।

```
Θ(f(n)): Average case যখন worst ও best case একই

Example: Single loop সবসময় n বার চলে
→ Θ(n) — সবসময়ই n operations
```

### তিনটির তুলনা

| Notation | মানে | কখন ব্যবহার |
|----------|------|------------|
| O(f(n)) | Upper bound (worst case) | সাধারণত এটাই বলা হয় |
| Ω(f(n)) | Lower bound (best case) | Algorithm analysis এ |
| Θ(f(n)) | Tight bound (exact) | যখন worst = best |

### Interview এ কী বলবেন

> "Interview তে সাধারণত Big O (worst case) বলা হয়। কারণ real system এ আমরা worst case এর জন্য prepare করি। তবে average case analysis এ Θ notation ব্যবহার হয়।"

---

## ১.৮ Best, Average, Worst Case

### তিনটি Case কী?

```
Worst Case:  সবচেয়ে বেশি সময় লাগার situation
Average Case: গড়ে কতটুকু সময় লাগে
Best Case:   সবচেয়ে কম সময় লাগার situation
```

### Linear Search দিয়ে উদাহরণ

```python
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i
    return -1

# arr = [3, 1, 7, 9, 2, 5], target = ?

# Best Case: target = 3 (প্রথম element)
#   → ১ বার check → O(1)

# Average Case: target যেকোনো জায়গায় থাকে
#   → গড়ে n/2 বার check → O(n/2) = O(n)

# Worst Case: target নেই অথবা শেষ element
#   → n বার check → O(n)
```

### Quick Sort এর Cases

| Case | কখন হয় | Complexity |
|------|---------|-----------|
| Best | Pivot সবসময় মাঝখানে | O(n log n) |
| Average | Random data | O(n log n) |
| Worst | Already sorted / All same | O(n²) |

### Interview Tip

```
প্রশ্ন: "Algorithm টির complexity কত?"
সঠিক উত্তর: "Worst case O(...), Best case O(...), Average case O(...)"

কখনো শুধু "O(n)" বলে থামবেন না — case specify করুন।
```

---

## ১.৯ Recursion

### সংজ্ঞা

**Recursion** হলো এমন একটি technique যেখানে একটি function নিজেকে নিজে call করে, যতক্ষণ না একটি base case এ পৌঁছায়।

### Recursion এর অবশ্যই দরকার

```
১. Base Case:  যখন recursion থামে (সবচেয়ে জরুরি!)
২. Recursive Case: নিজেকে call করে smaller problem এ
৩. Progress:  প্রতিটি call এ problem ছোট হয়
```

### Factorial — Step by Step

```python
def factorial(n):
    # Base Case
    if n <= 1:
        return 1
    # Recursive Case
    return n * factorial(n - 1)

# factorial(4) এর execution trace:
# factorial(4)
#   → 4 * factorial(3)
#         → 3 * factorial(2)
#               → 2 * factorial(1)
#                     → return 1  ← Base Case
#               → 2 * 1 = 2
#         → 3 * 2 = 6
#   → 4 * 6 = 24
# return 24
```

### Call Stack Visualization

```
factorial(4) কল করলে Stack:
┌─────────────────────────┐
│ factorial(1) → returns 1│  ← TOP (সবশেষে resolve)
├─────────────────────────┤
│ factorial(2) → 2 × 1    │
├─────────────────────────┤
│ factorial(3) → 3 × 2    │
├─────────────────────────┤
│ factorial(4) → 4 × 6    │  ← BOTTOM (সবার আগে call)
└─────────────────────────┘
```

### Fibonacci — Recursion এর সমস্যা

```python
# ❌ Naive Recursion — O(2ⁿ) time!
def fib_naive(n):
    if n <= 1:
        return n
    return fib_naive(n-1) + fib_naive(n-2)

# fib(5) এর call tree:
#           fib(5)
#          /       \
#       fib(4)    fib(3)
#       /    \    /    \
#    fib(3) fib(2) fib(2) fib(1)
#    ...
# একই calculation বারবার হচ্ছে! (Overlapping Subproblems)

# ✅ Memoization দিয়ে — O(n) time
def fib_memo(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fib_memo(n-1, memo) + fib_memo(n-2, memo)
    return memo[n]
```

### Recursion vs Iteration

| বিষয় | Recursion | Iteration |
|------|-----------|-----------|
| কোড | সহজ, readable | কিছুটা verbose |
| Memory | O(n) stack space | O(1) |
| Speed | Overhead আছে | দ্রুত |
| Stack Overflow | হতে পারে | না |
| কখন | Tree, Graph, Divide & Conquer | Simple loops |

### Tail Recursion

```python
# Regular recursion (NOT tail recursive)
def factorial(n):
    if n <= 1: return 1
    return n * factorial(n-1)  # return এর পর আরও কাজ আছে

# Tail Recursive — return এর পরে কোনো কাজ নেই
def factorial_tail(n, acc=1):
    if n <= 1: return acc
    return factorial_tail(n-1, n * acc)  # শেষ operation = recursive call
# Compiler optimize করতে পারে → O(1) space
```

### সাধারণ ভুল

```
❌ Base Case না দেওয়া → Infinite recursion → Stack Overflow
❌ Progress না থাকা → Same input এ নিজেকে call → Infinite loop
❌ সব সমস্যায় recursion → Simple loop এ সমাধান হলে iteration better
```

---

## ১.১০ Iteration

### সংজ্ঞা

**Iteration** হলো একটি block of code বারবার execute করা যতক্ষণ একটি condition সত্য থাকে — loop ব্যবহার করে।

### Types of Loops

```python
# For loop — নির্দিষ্ট সংখ্যকবার
for i in range(5):
    print(i)      # 0, 1, 2, 3, 4

# While loop — condition ভিত্তিক
n = 10
while n > 0:
    print(n)
    n -= 1        # 10, 9, 8, ..., 1

# Do-while equivalent (Python তে নেই, simulate করতে হয়)
while True:
    action()
    if condition:
        break
```

### Recursion কে Iteration এ রূপান্তর

```python
# Recursive fibonacci → Iterative
def fib_iterative(n):
    if n <= 1:
        return n
    prev, curr = 0, 1
    for _ in range(2, n+1):
        prev, curr = curr, prev + curr
    return curr
# O(n) time, O(1) space — recursion এর চেয়ে efficient!
```

---

## ১.১১ Memory Concepts

### Computer Memory Layout

```
┌─────────────────────────────────┐
│          Text/Code Segment      │  Program instructions
├─────────────────────────────────┤
│          Data Segment           │  Global & Static variables
├─────────────────────────────────┤
│          Heap                   │  Dynamic allocation (malloc, new)
│          ↓ grows downward       │
│                                 │
│          ↑ grows upward         │
│          Stack                  │  Function calls, local variables
└─────────────────────────────────┘
```

### Memory এর প্রকারভেদ

| Memory | কোথায় | কী থাকে | Lifetime |
|--------|--------|---------|---------|
| **Register** | CPU | Temp calculations | নানোসেকেন্ড |
| **Cache** | CPU কাছে | Recently used data | মাইক্রোসেকেন্ড |
| **RAM (Stack)** | Main memory | Local vars, function calls | Function শেষ পর্যন্ত |
| **RAM (Heap)** | Main memory | Dynamic objects | Manually free করা পর্যন্ত |
| **Disk** | Storage | Files, DB | Permanent |

### Pointer Basics (C/C++ context)

```c
int x = 10;       // x নামে variable, value 10
int *p = &x;      // p হলো pointer, x এর address store করে

printf("%d", x);  // 10 — value
printf("%p", p);  // 0x7ffd... — address
printf("%d", *p); // 10 — dereferencing (address থেকে value)

*p = 20;          // p এর মাধ্যমে x এর value পরিবর্তন
printf("%d", x);  // 20
```

---

## ১.১২ Stack vs Heap Memory

### Stack Memory

```
বৈশিষ্ট্য:
  ✅ Fast access (LIFO structure)
  ✅ Automatically managed (function শেষে auto-free)
  ✅ Thread safe (প্রতিটি thread এর আলাদা stack)
  ❌ Limited size (~1-8 MB typical)
  ❌ Stack Overflow হতে পারে (deep recursion)

কী থাকে:
  → Local variables
  → Function parameters
  → Return addresses
  → Recursion frames
```

### Heap Memory

```
বৈশিষ্ট্য:
  ✅ Large size (RAM এর সমান)
  ✅ Runtime এ size নির্ধারণ করা যায়
  ❌ Slower (allocation/deallocation overhead)
  ❌ Manually manage করতে হয় (C/C++ এ)
  ❌ Memory leak হতে পারে
  ❌ Fragmentation

কী থাকে:
  → new/malloc দিয়ে তৈরি objects
  → Dynamic arrays
  → Linked list nodes
```

### উদাহরণ

```python
# Python এ memory management automatic

# Stack এ যায়: local variables
def my_function():
    x = 10          # Stack
    y = [1, 2, 3]   # y হলো Stack এ, কিন্তু list object Heap এ
    return x

# Heap এ যায়: objects, lists, dicts
my_list = [1, 2, 3, 4, 5]    # List object Heap এ
my_dict = {"key": "value"}    # Dict object Heap এ
```

```cpp
// C++ এ স্পষ্টভাবে দেখা যায়
void example() {
    int x = 10;         // Stack — function শেষে auto-free
    int* p = new int(5); // Heap — manually delete করতে হবে!
    delete p;           // Heap free করা
}
// x automatically freed, p manually freed
```

### Stack Overflow কখন হয়?

```python
# অসীম recursion → Stack Overflow
def infinite():
    return infinite()  # Base case নেই!

infinite()
# RecursionError: maximum recursion depth exceeded
# Python এর default recursion limit: 1000
```

---

## ১.১৩ PART 1 — Interview Q&A

### সেকশন ১: বিস্তারিত প্রশ্নোত্তর

**Q1: O(log n) মানে কী? কীভাবে চিনবেন?**

> **উত্তর:** O(log n) মানে প্রতিটি step এ problem এর size অর্ধেক (বা কোনো constant ভাগে) কমে যায়। চেনার উপায়: যদি দেখেন input প্রতিটি iteration এ half হচ্ছে — সেটি O(log n)। Binary Search এর উদাহরণ: n=1000 হলে log₂(1000) ≈ 10 বার — মাত্র ১০টি step এ উত্তর পাওয়া যায়।

**Q2: Recursion ব্যবহার করা কখন উচিত আর কখন উচিত নয়?**

> **উত্তর:** উচিত — Tree traversal, Graph DFS, Divide & Conquer (Merge Sort, Quick Sort), Backtracking। উচিত নয় — Simple iteration দিয়ে হলে (Fibonacci sum), deep recursion যেখানে stack overflow হতে পারে, performance critical code। Rule: যদি problem naturally recursive structure এ থাকে (Tree, Graph) তাহলে recursion, নাহলে iteration prefer করুন।

**Q3: Time Complexity O(n log n) কোন algorithms এ দেখা যায়?**

> **উত্তর:** Merge Sort, Heap Sort, Quick Sort (average case), এবং বেশিরভাগ efficient sorting algorithms এ। এছাড়া Segment Tree construction O(n log n), Binary Indexed Tree operations O(n log n)।

**Q4: Space Complexity O(1) মানে কী? উদাহরণ দিন।**

> **উত্তর:** O(1) space মানে algorithm extra memory ব্যবহার করে না — শুধু constant কিছু variables। Input size যাই হোক, extra memory same থাকে। উদাহরণ: Two-pointer approach, in-place swap, binary search (iterative version)।

**Q5: Worst case এবং Average case এর পার্থক্য practical example দিয়ে বলুন।**

> **উত্তর:** Quick Sort এর Worst case O(n²) — যখন array already sorted এবং pivot সবসময় largest/smallest হয়। Average case O(n log n) — random data তে। তাই real applications এ Quick Sort random pivot বা median-of-three strategy ব্যবহার করে worst case avoid করে।

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| O(1) এর উদাহরণ | Array index access, HashMap get |
| O(n²) এর উদাহরণ | Bubble Sort, Nested loop |
| Stack memory কে manage করে? | OS automatically |
| Recursion এর memory complexity | O(n) — call stack |
| Big O কোন case measure করে? | Worst case (upper bound) |
| Stack Overflow কেন হয়? | Infinite/deep recursion |
| Θ(n) মানে কী? | Exactly n operations (tight bound) |
| log₂(1024) = ? | 10 |
| O(n!) কোন algorithm? | Brute force permutation |
| Tail recursion সুবিধা কী? | Stack frame reuse (O(1) space) |

---

> **⚠️ PART 1 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part2"></a>

# PART 2: Arrays & Strings (অ্যারে ও স্ট্রিং)

> **পড়ার নির্দেশনা:** Array এবং String হলো সবচেয়ে fundamental data structures। Interview তে প্রায় সব coding problem এর ভিত্তি এখানেই। Sliding Window, Two Pointer, Prefix Sum — এই patterns শিখলে ৪০-৫০% interview problems সমাধান করা যায়।

---

## ২.১ Array Basics

### সংজ্ঞা

**Array** হলো একই ধরনের (homogeneous) data elements এর একটি contiguous (পাশাপাশি) collection যেখানে প্রতিটি element কে index দিয়ে access করা যায়।

```
Index:  [0]  [1]  [2]  [3]  [4]
Array:  [10] [20] [30] [40] [50]
         ↑                   ↑
      প্রথম element        শেষ element (index = n-1)
```

### মূল বৈশিষ্ট্য

| বৈশিষ্ট্য | মান | কারণ |
|----------|-----|------|
| **Access** | O(1) | Base address + offset গণনা |
| **Search** | O(n) unsorted, O(log n) sorted | Linear/Binary scan |
| **Insert (end)** | O(1) amortized | Array তে জায়গা থাকলে |
| **Insert (middle)** | O(n) | Shift করতে হয় |
| **Delete (middle)** | O(n) | Shift করতে হয় |
| **Delete (end)** | O(1) | শুধু size কমে |

### Random Access কেন O(1)?

```
Array address = Base Address + (Index × Element Size)

Example: int arr[] — Base = 1000, int = 4 bytes
  arr[0] → 1000 + (0 × 4) = 1000
  arr[3] → 1000 + (3 × 4) = 1012
  arr[9] → 1000 + (9 × 4) = 1036
  → যেকোনো index এ direct calculation → O(1)
```

### Array Operations — Code

```python
# Array তৈরি
arr = [10, 20, 30, 40, 50]

# Access — O(1)
print(arr[2])       # 30
print(arr[-1])      # 50 (Python: negative indexing)

# Traverse — O(n)
for i in range(len(arr)):
    print(arr[i])

# Insert at end — O(1) amortized
arr.append(60)       # [10, 20, 30, 40, 50, 60]

# Insert at position — O(n)
arr.insert(2, 25)    # [10, 20, 25, 30, 40, 50, 60]
# index 2 এর পর সব element shift হয়

# Delete — O(n)
arr.remove(25)       # value দিয়ে remove (first occurrence)
arr.pop(2)           # index দিয়ে remove
arr.pop()            # শেষ element remove — O(1)

# Search — O(n) unsorted
print(30 in arr)     # True/False
print(arr.index(30)) # index return

# Slice — O(k), k = slice size
sub = arr[1:4]       # [20, 30, 40]

# Length
n = len(arr)         # O(1)
```

### Array তৈরির সহজ উপায়

```python
# Zeros
zeros = [0] * 5         # [0, 0, 0, 0, 0]

# Range
nums = list(range(1, 6)) # [1, 2, 3, 4, 5]

# 2D Array (Matrix)
matrix = [[0] * 3 for _ in range(3)]
# [[0, 0, 0],
#  [0, 0, 0],
#  [0, 0, 0]]

# ⚠️ এই ভুল করবেন না:
wrong = [[0] * 3] * 3  # 3টি row একই reference share করে!
wrong[0][0] = 1
print(wrong)  # [[1, 0, 0], [1, 0, 0], [1, 0, 0]] — সব row change!
```

---

## ২.২ Static vs Dynamic Array

### Static Array

```
Size fixed at declaration — পরে পরিবর্তন করা যায় না।

int arr[5] = {1, 2, 3, 4, 5};  // C এ
// ৫টির বেশি element রাখা যাবে না

Advantages:
  ✅ Memory efficient — exact size allocate
  ✅ Cache friendly — contiguous memory
  ✅ Faster — no reallocation overhead

Disadvantages:
  ❌ Size আগে থেকে জানতে হয়
  ❌ Overflow হতে পারে
  ❌ Underflow — memory waste
```

### Dynamic Array

```
Runtime এ size বাড়ানো যায়।

Python: list, Java: ArrayList, C++: vector

Mechanism:
  1. Initial capacity = 1 (বা কিছু small number)
  2. Full হলে: নতুন array তৈরি (2× size)
  3. সব element copy করো নতুন array তে
  4. পুরনো array delete

Visualization:
  [10] → full!
  [10, _, _, _] → doubled (capacity 4)
  add 20: [10, 20, _, _]
  add 30: [10, 20, 30, _]
  add 40: [10, 20, 30, 40] → full!
  [10, 20, 30, 40, _, _, _, _] → doubled (capacity 8)
```

### Amortized O(1) — কেন?

```
Suppose n elements insert করব:

n insertions এর মধ্যে কতবার copy হয়?
  capacity 1→2: 1 element copy
  capacity 2→4: 2 elements copy
  capacity 4→8: 4 elements copy
  ...
  Total copies = 1 + 2 + 4 + ... + n = 2n

Total work = n insertions + 2n copies = 3n = O(n)
Per insertion = O(n)/n = O(1) amortized
```

| বিষয় | Static Array | Dynamic Array |
|------|-------------|---------------|
| Size | Fixed | Flexible |
| Memory | Exact | Extra (unused capacity) |
| Insert (end) | O(1) | O(1) amortized |
| Insert (middle) | O(n) | O(n) |
| Languages | C arrays | Python list, C++ vector |

---

## ২.৩ String Operations

### String কী?

**String** হলো character এর sequence (array of characters)।

```python
s = "Hello, Bangladesh!"

# Basic Operations
print(len(s))          # 18 — O(n) Python, O(1) C++
print(s[0])            # 'H' — O(1)
print(s[7:17])         # 'Bangladesh' — O(k)
print(s.upper())       # 'HELLO, BANGLADESH!'
print(s.lower())       # 'hello, bangladesh!'
print(s.strip())       # leading/trailing whitespace সরায়
print(s.split(', '))   # ['Hello', 'Bangladesh!']
print(s.replace('Bangladesh', 'BD'))
print(s.count('l'))    # 3 — 'l' কতবার আছে
print(s.find('Bang'))  # 7 — index
print(s.startswith('Hello'))  # True
print(s.endswith('!'))        # True
```

### String Immutability

```python
# Python এ string immutable — পরিবর্তন করা যায় না
s = "hello"
# s[0] = 'H'  ← TypeError!

# পরিবর্তন করতে হলে নতুন string তৈরি করতে হয়
s = 'H' + s[1:]    # 'Hello'

# String Concatenation সমস্যা:
result = ""
for i in range(n):
    result += str(i)   # ❌ O(n²) — প্রতিবার নতুন string তৈরি!

# সঠিক পদ্ধতি:
parts = []
for i in range(n):
    parts.append(str(i))
result = ''.join(parts)  # ✅ O(n)
```

### String Hashing

```python
# Anagram check — O(n)
from collections import Counter

def is_anagram(s, t):
    return Counter(s) == Counter(t)

# অথবা:
def is_anagram_v2(s, t):
    if len(s) != len(t):
        return False
    freq = [0] * 26
    for c in s:
        freq[ord(c) - ord('a')] += 1
    for c in t:
        freq[ord(c) - ord('a')] -= 1
    return all(f == 0 for f in freq)
```

### Palindrome Check

```python
def is_palindrome(s):
    # Two Pointer approach — O(n) time, O(1) space
    left, right = 0, len(s) - 1
    while left < right:
        if s[left] != s[right]:
            return False
        left += 1
        right -= 1
    return True

# One-liner (সহজ কিন্তু O(n) space):
def is_palindrome_v2(s):
    return s == s[::-1]
```

---

## ২.৪ Prefix Sum

### ধারণা

**Prefix Sum** হলো array এর প্রতিটি index পর্যন্ত সব elements এর যোগফল। এটি precompute করে রাখলে পরে যেকোনো range এর sum O(1) এ বের করা যায়।

```
Array:       [3, 1, 4, 1, 5, 9, 2, 6]
Index:        0  1  2  3  4  5  6  7

Prefix Sum:  [3, 4, 8, 9, 14, 23, 25, 31]
  prefix[0] = 3
  prefix[1] = 3 + 1 = 4
  prefix[2] = 3 + 1 + 4 = 8
  ...
  prefix[i] = prefix[i-1] + arr[i]
```

### Range Sum Query

```
Range [l, r] এর sum = prefix[r] - prefix[l-1]

Example: sum from index 2 to 5
  = prefix[5] - prefix[1]
  = 23 - 4
  = 19

Verify: 4 + 1 + 5 + 9 = 19 ✓
```

### Implementation

```python
def build_prefix(arr):
    n = len(arr)
    prefix = [0] * n
    prefix[0] = arr[0]
    for i in range(1, n):
        prefix[i] = prefix[i-1] + arr[i]
    return prefix

def range_sum(prefix, l, r):
    if l == 0:
        return prefix[r]
    return prefix[r] - prefix[l-1]

# Usage
arr = [3, 1, 4, 1, 5, 9, 2, 6]
prefix = build_prefix(arr)
print(range_sum(prefix, 2, 5))  # 19 — O(1)!

# Without prefix: O(n) per query
# With prefix: O(n) build, O(1) per query
# Q queries হলে: O(n + Q) vs O(nQ) — massive difference!
```

### 2D Prefix Sum (Matrix)

```python
def build_2d_prefix(matrix):
    rows, cols = len(matrix), len(matrix[0])
    prefix = [[0] * (cols + 1) for _ in range(rows + 1)]

    for r in range(1, rows + 1):
        for c in range(1, cols + 1):
            prefix[r][c] = (matrix[r-1][c-1]
                          + prefix[r-1][c]
                          + prefix[r][c-1]
                          - prefix[r-1][c-1])
    return prefix

def query_2d(prefix, r1, c1, r2, c2):
    # (r1,c1) থেকে (r2,c2) পর্যন্ত rectangle এর sum
    return (prefix[r2+1][c2+1]
           - prefix[r1][c2+1]
           - prefix[r2+1][c1]
           + prefix[r1][c1])
```

### Prefix Sum দিয়ে Subarray Count

```python
# Subarray যাদের sum = k → O(n) solution
def count_subarrays_with_sum_k(arr, k):
    count = 0
    prefix_sum = 0
    freq = {0: 1}  # empty subarray

    for num in arr:
        prefix_sum += num
        # prefix_sum - k আগে দেখা গেলে, সেই point থেকে এখন পর্যন্ত sum = k
        if prefix_sum - k in freq:
            count += freq[prefix_sum - k]
        freq[prefix_sum] = freq.get(prefix_sum, 0) + 1

    return count

# Example: arr = [1, 2, 3], k = 3
# Subarrays: [3], [1,2] → count = 2
```

---

## ২.৫ Sliding Window

### ধারণা

**Sliding Window** হলো একটি technique যেখানে একটি fixed বা variable size এর "window" array বরাবর slide করে। Brute force O(n²) কে O(n) এ আনে।

```
Array: [2, 3, 1, 5, 4, 2, 3]
Window size k = 3

Step 1: [2, 3, 1] 5  4  2  3   → sum = 6
Step 2:  2 [3, 1, 5] 4  2  3   → sum = 9 (window সরল)
Step 3:  2  3 [1, 5, 4] 2  3   → sum = 10
Step 4:  2  3  1 [5, 4, 2] 3   → sum = 11
Step 5:  2  3  1  5 [4, 2, 3]  → sum = 9

Maximum sum = 11
```

### Fixed Window — Maximum Sum Subarray of Size K

```python
def max_sum_subarray(arr, k):
    n = len(arr)
    if n < k:
        return -1

    # প্রথম window এর sum
    window_sum = sum(arr[:k])
    max_sum = window_sum

    # Window slide করো
    for i in range(k, n):
        # নতুন element যোগ করো, পুরনো element বাদ দাও
        window_sum += arr[i] - arr[i - k]
        max_sum = max(max_sum, window_sum)

    return max_sum

# Dry Run: arr = [2, 3, 1, 5, 4, 2, 3], k = 3
# Initial: window_sum = 2+3+1 = 6, max = 6
# i=3: sum = 6 + 5 - 2 = 9,  max = 9
# i=4: sum = 9 + 4 - 3 = 10, max = 10
# i=5: sum = 10+ 2 - 1 = 11, max = 11
# i=6: sum = 11+ 3 - 5 = 9,  max = 11
# Result: 11 ✓
```

### Variable Window — Longest Substring Without Repeating

```python
def length_of_longest_substring(s):
    char_index = {}    # char → last seen index
    max_len = 0
    left = 0           # window এর বাম সীমা

    for right in range(len(s)):
        char = s[right]

        # char আগে দেখা গেছে এবং window এর ভেতরে আছে
        if char in char_index and char_index[char] >= left:
            left = char_index[char] + 1  # window সংকুচিত করো

        char_index[char] = right  # position update
        max_len = max(max_len, right - left + 1)

    return max_len

# Dry Run: s = "abcabcbb"
# r=0 'a': left=0, window="a",    len=1
# r=1 'b': left=0, window="ab",   len=2
# r=2 'c': left=0, window="abc",  len=3
# r=3 'a': 'a' at 0, left=1, window="bca", len=3
# r=4 'b': 'b' at 1, left=2, window="cab", len=3
# r=5 'c': 'c' at 2, left=3, window="abc", len=3
# r=6 'b': 'b' at 4, left=5, window="cb",  len=2
# r=7 'b': 'b' at 6, left=7, window="b",   len=1
# Result: 3 ✓
```

### Minimum Window Substring

```python
def min_window(s, t):
    from collections import Counter

    need = Counter(t)
    missing = len(t)
    best = (float('inf'), 0, 0)
    left = 0

    for right, char in enumerate(s):
        if need[char] > 0:
            missing -= 1
        need[char] -= 1

        if missing == 0:  # সব character পাওয়া গেছে
            # বাম থেকে অপ্রয়োজনীয় characters সরাও
            while need[s[left]] < 0:
                need[s[left]] += 1
                left += 1
            if right - left + 1 < best[0]:
                best = (right - left + 1, left, right)
            need[s[left]] += 1
            missing += 1
            left += 1

    return s[best[1]:best[2]+1] if best[0] != float('inf') else ""
```

### Sliding Window Pattern চেনার উপায়

```
এই keywords দেখলে Sliding Window ভাবুন:
  → "contiguous subarray/substring"
  → "maximum/minimum of fixed size k"
  → "longest/shortest substring with condition"
  → "all subarrays of size k"
```

---

## ২.৬ Two Pointer

### ধারণা

**Two Pointer** technique তে দুটি pointer ব্যবহার করে array তে iterate করা হয়। একটি শুরু থেকে (left), একটি শেষ থেকে (right)। O(n²) কে O(n) এ আনে।

### Two Sum — Sorted Array

```python
def two_sum_sorted(arr, target):
    """
    Sorted array তে দুটি number খোঁজো যাদের sum = target
    """
    left, right = 0, len(arr) - 1

    while left < right:
        current_sum = arr[left] + arr[right]

        if current_sum == target:
            return [left, right]
        elif current_sum < target:
            left += 1   # sum বাড়াতে left এগিয়ে আসে
        else:
            right -= 1  # sum কমাতে right পিছিয়ে যায়

    return []

# Dry Run: arr = [1, 3, 5, 7, 9, 11], target = 12
# left=0(1), right=5(11): sum=12 → Found! [0,5] ✓

# Dry Run: target = 10
# left=0(1), right=5(11): sum=12 > 10, right--
# left=0(1), right=4(9):  sum=10 → Found! [0,4] ✓
```

### Remove Duplicates from Sorted Array

```python
def remove_duplicates(arr):
    """In-place, O(1) extra space"""
    if not arr:
        return 0

    slow = 0  # unique elements এর pointer

    for fast in range(1, len(arr)):
        if arr[fast] != arr[slow]:  # নতুন unique element
            slow += 1
            arr[slow] = arr[fast]

    return slow + 1  # unique count

# Dry Run: [1, 1, 2, 2, 3, 4, 4]
# slow=0(1), fast=1: arr[1]=1 == arr[0]=1, skip
# slow=0(1), fast=2: arr[2]=2 != arr[0]=1 → slow=1, arr[1]=2
# slow=1(2), fast=3: arr[3]=2 == arr[1]=2, skip
# slow=1(2), fast=4: arr[4]=3 != arr[1]=2 → slow=2, arr[2]=3
# ...
# Result: [1, 2, 3, 4, ...], return 4
```

### Container With Most Water

```python
def max_area(height):
    """
    Array এর প্রতিটি element একটি vertical line এর height।
    সর্বোচ্চ water ধরার container খুঁজুন।
    """
    left, right = 0, len(height) - 1
    max_water = 0

    while left < right:
        # water = min height × width
        water = min(height[left], height[right]) * (right - left)
        max_water = max(max_water, water)

        # ছোট height টার pointer সরাও (বড় করার চেষ্টা)
        if height[left] < height[right]:
            left += 1
        else:
            right -= 1

    return max_water
```

### 3Sum Problem

```python
def three_sum(nums):
    """তিনটি number খোঁজো যাদের sum = 0"""
    nums.sort()
    result = []
    n = len(nums)

    for i in range(n - 2):
        # Duplicate skip
        if i > 0 and nums[i] == nums[i-1]:
            continue

        left, right = i + 1, n - 1

        while left < right:
            total = nums[i] + nums[left] + nums[right]

            if total == 0:
                result.append([nums[i], nums[left], nums[right]])
                while left < right and nums[left] == nums[left+1]:
                    left += 1
                while left < right and nums[right] == nums[right-1]:
                    right -= 1
                left += 1
                right -= 1
            elif total < 0:
                left += 1
            else:
                right -= 1

    return result
```

### Two Pointer Pattern চেনার উপায়

```
এই keywords দেখলে Two Pointer ভাবুন:
  → "Sorted array তে pair/triplet"
  → "In-place modification"
  → "Palindrome check"
  → "Merge two sorted arrays"
  → "Remove duplicates"
  → "Squeeze from both ends"
```

---

## ২.৭ Kadane's Algorithm

### সমস্যা: Maximum Subarray Sum

Array তে এমন contiguous subarray খুঁজুন যার sum সবচেয়ে বেশি।

```
Input:  [-2, 1, -3, 4, -1, 2, 1, -5, 4]
Output: 6
Explanation: [4, -1, 2, 1] = 6
```

### Brute Force — O(n³)

```python
def max_subarray_brute(arr):
    n = len(arr)
    max_sum = float('-inf')
    for i in range(n):
        for j in range(i, n):
            current = sum(arr[i:j+1])  # O(n) per pair
            max_sum = max(max_sum, current)
    return max_sum
# O(n³) — সব subarray try করা
```

### Kadane's Algorithm — O(n)

```python
def max_subarray_kadane(arr):
    max_sum = arr[0]      # global maximum
    current_sum = arr[0]  # current window এর sum

    for i in range(1, len(arr)):
        # নতুন element যোগ করা উচিত নাকি নতুন subarray শুরু?
        current_sum = max(arr[i], current_sum + arr[i])
        max_sum = max(max_sum, current_sum)

    return max_sum
```

### Dry Run — Step by Step

```
arr = [-2, 1, -3, 4, -1, 2, 1, -5, 4]

i=0: current=-2, max=-2
i=1: current=max(1, -2+1)=max(1,-1)=1,  max=1
i=2: current=max(-3,1-3)=max(-3,-2)=-2, max=1
i=3: current=max(4,-2+4)=max(4,2)=4,    max=4
i=4: current=max(-1,4-1)=max(-1,3)=3,   max=4
i=5: current=max(2,3+2)=max(2,5)=5,     max=5
i=6: current=max(1,5+1)=max(1,6)=6,     max=6
i=7: current=max(-5,6-5)=max(-5,1)=1,   max=6
i=8: current=max(4,1+4)=max(4,5)=5,     max=6

Answer: 6 ✓ (subarray = [4,-1,2,1])
```

### Intuition

```
মূল idea:
  যদি current_sum negative হয়ে যায়, তাহলে এটি বাদ দিয়ে
  নতুন subarray শুরু করা লাভজনক।

  কারণ: negative sum যোগ করলে future sum কমে।
```

### Subarray Start & End Position সহ

```python
def max_subarray_with_indices(arr):
    max_sum = arr[0]
    current_sum = arr[0]
    start = end = temp_start = 0

    for i in range(1, len(arr)):
        if arr[i] > current_sum + arr[i]:
            current_sum = arr[i]
            temp_start = i          # নতুন subarray শুরু
        else:
            current_sum += arr[i]

        if current_sum > max_sum:
            max_sum = current_sum
            start = temp_start
            end = i

    return max_sum, arr[start:end+1]

# Output: (6, [4, -1, 2, 1])
```

### Variants

```python
# Maximum circular subarray sum
def max_circular_subarray(arr):
    # Case 1: Maximum subarray (না circular) — Kadane's
    max_normal = max_subarray_kadane(arr)

    # Case 2: Circular subarray
    # Total sum - minimum subarray sum
    total = sum(arr)
    # Array invert করে minimum খুঁজি = maximum of negated
    negated = [-x for x in arr]
    min_subarray = -max_subarray_kadane(negated)
    max_circular = total - min_subarray

    # সব negative হলে circular sum invalid
    return max(max_normal, max_circular) if max_circular != 0 else max_normal
```

---

## ২.৮ Binary Search

### সংজ্ঞা

**Binary Search** হলো sorted array তে target খোঁজার O(log n) algorithm। প্রতিটি step এ search space অর্ধেক হয়।

### Condition

```
Binary Search শুধু কাজ করে যখন:
  ✅ Array sorted (ascending বা descending)
  ✅ Random access possible (array, না linked list)
```

### Standard Implementation

```python
# Iterative — O(log n) time, O(1) space (preferred)
def binary_search(arr, target):
    lo, hi = 0, len(arr) - 1

    while lo <= hi:
        mid = lo + (hi - lo) // 2  # Overflow prevent (না (lo+hi)//2)

        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            lo = mid + 1   # target ডান দিকে
        else:
            hi = mid - 1   # target বাম দিকে

    return -1  # না পাওয়া গেলে

# Recursive — O(log n) time, O(log n) space
def binary_search_recursive(arr, target, lo, hi):
    if lo > hi:
        return -1
    mid = lo + (hi - lo) // 2
    if arr[mid] == target:
        return mid
    elif arr[mid] < target:
        return binary_search_recursive(arr, target, mid+1, hi)
    else:
        return binary_search_recursive(arr, target, lo, mid-1)
```

### Dry Run

```
arr = [1, 3, 5, 7, 9, 11, 13], target = 7

lo=0, hi=6, mid=3 → arr[3]=7 == target → return 3 ✓

arr = [1, 3, 5, 7, 9, 11, 13], target = 6

lo=0, hi=6, mid=3 → arr[3]=7 > 6  → hi=2
lo=0, hi=2, mid=1 → arr[1]=3 < 6  → lo=2
lo=2, hi=2, mid=2 → arr[2]=5 < 6  → lo=3
lo=3 > hi=2 → return -1 ✓
```

### First & Last Occurrence

```python
def first_occurrence(arr, target):
    lo, hi = 0, len(arr) - 1
    result = -1

    while lo <= hi:
        mid = lo + (hi - lo) // 2
        if arr[mid] == target:
            result = mid
            hi = mid - 1   # বামে আরো আছে কিনা দেখো
        elif arr[mid] < target:
            lo = mid + 1
        else:
            hi = mid - 1

    return result

def last_occurrence(arr, target):
    lo, hi = 0, len(arr) - 1
    result = -1

    while lo <= hi:
        mid = lo + (hi - lo) // 2
        if arr[mid] == target:
            result = mid
            lo = mid + 1   # ডানে আরো আছে কিনা দেখো
        elif arr[mid] < target:
            lo = mid + 1
        else:
            hi = mid - 1

    return result
```

### Binary Search on Answer

```python
# সমস্যা: n টি chocolates, k জন students এ ভাগ কর।
# max(minimum chocolates per student) maximize কর।
# Constraints: প্রতিটি student consecutive chocolates পাবে।

def is_feasible(arr, k, mid):
    """mid minimum হলে k students এ ভাগ করা যায়?"""
    students = 1
    current = 0
    for chocolates in arr:
        if chocolates > mid:
            return False     # single package এ বেশি
        if current + chocolates > mid:
            students += 1
            current = chocolates
        else:
            current += chocolates
    return students <= k

def allocate_chocolates(arr, k):
    lo, hi = max(arr), sum(arr)
    result = hi

    while lo <= hi:
        mid = lo + (hi - lo) // 2
        if is_feasible(arr, k, mid):
            result = mid
            hi = mid - 1   # smaller value সম্ভব?
        else:
            lo = mid + 1

    return result
```

### Binary Search Template

```python
# Template: "condition সত্য হওয়ার প্রথম/শেষ position খোঁজো"

def binary_search_template(lo, hi):
    result = -1
    while lo <= hi:
        mid = lo + (hi - lo) // 2
        if condition(mid):      # আপনার condition এখানে
            result = mid
            hi = mid - 1       # বামে search (first occurrence)
            # অথবা lo = mid+1  # ডানে search (last occurrence)
        else:
            lo = mid + 1       # অথবা hi = mid-1
    return result
```

---

## ২.৯ Matrix Operations

### Matrix Basics

```python
# 3×4 matrix
matrix = [
    [1,  2,  3,  4],
    [5,  6,  7,  8],
    [9, 10, 11, 12]
]

rows = len(matrix)       # 3
cols = len(matrix[0])    # 4

# Element access — O(1)
print(matrix[1][2])      # 7 (row 1, col 2)

# Row traverse
for col in range(cols):
    print(matrix[0][col])   # First row: 1 2 3 4

# Column traverse
for row in range(rows):
    print(matrix[row][1])   # Second column: 2 6 10
```

### Matrix Traversal Patterns

```python
# ── Spiral Order Traversal ─────────────────────────
def spiral_order(matrix):
    result = []
    if not matrix:
        return result

    top, bottom = 0, len(matrix) - 1
    left, right = 0, len(matrix[0]) - 1

    while top <= bottom and left <= right:
        # Left to Right (top row)
        for col in range(left, right + 1):
            result.append(matrix[top][col])
        top += 1

        # Top to Bottom (right column)
        for row in range(top, bottom + 1):
            result.append(matrix[row][right])
        right -= 1

        # Right to Left (bottom row)
        if top <= bottom:
            for col in range(right, left - 1, -1):
                result.append(matrix[bottom][col])
            bottom -= 1

        # Bottom to Top (left column)
        if left <= right:
            for row in range(bottom, top - 1, -1):
                result.append(matrix[row][left])
            left += 1

    return result

# ── Diagonal Traversal ──────────────────────────────
def diagonal_traverse(matrix):
    rows, cols = len(matrix), len(matrix[0])
    result = []
    going_up = True

    r, c = 0, 0
    for _ in range(rows * cols):
        result.append(matrix[r][c])
        if going_up:
            if c == cols - 1:
                r += 1; going_up = False
            elif r == 0:
                c += 1; going_up = False
            else:
                r -= 1; c += 1
        else:
            if r == rows - 1:
                c += 1; going_up = True
            elif c == 0:
                r += 1; going_up = True
            else:
                r += 1; c -= 1

    return result
```

### Matrix Rotation (90° Clockwise)

```python
def rotate_90_clockwise(matrix):
    """
    In-place rotation — O(n²) time, O(1) space
    Step 1: Transpose (rows → columns)
    Step 2: Reverse each row
    """
    n = len(matrix)

    # Step 1: Transpose
    for i in range(n):
        for j in range(i + 1, n):
            matrix[i][j], matrix[j][i] = matrix[j][i], matrix[i][j]

    # Step 2: Reverse each row
    for i in range(n):
        matrix[i].reverse()

# Example:
# Original:     After Transpose:  After Row Reverse:
# 1 2 3         1 4 7             7 4 1
# 4 5 6    →    2 5 8      →      8 5 2
# 7 8 9         3 6 9             9 6 3
```

### Set Matrix Zeroes

```python
def set_zeroes(matrix):
    """
    কোনো cell 0 হলে সেই পুরো row ও column 0 করো।
    O(mn) time, O(1) extra space (in-place)
    """
    rows, cols = len(matrix), len(matrix[0])
    first_row_zero = any(matrix[0][c] == 0 for c in range(cols))
    first_col_zero = any(matrix[r][0] == 0 for r in range(rows))

    # প্রথম row ও col কে marker হিসেবে ব্যবহার
    for r in range(1, rows):
        for c in range(1, cols):
            if matrix[r][c] == 0:
                matrix[r][0] = 0   # row marker
                matrix[0][c] = 0   # col marker

    # Markers দেখে zero করো
    for r in range(1, rows):
        for c in range(1, cols):
            if matrix[r][0] == 0 or matrix[0][c] == 0:
                matrix[r][c] = 0

    if first_row_zero:
        for c in range(cols):
            matrix[0][c] = 0

    if first_col_zero:
        for r in range(rows):
            matrix[r][0] = 0
```

### BFS on Matrix (Shortest Path)

```python
from collections import deque

def shortest_path(grid, start, end):
    """
    Grid এ shortest path — BFS (unweighted)
    0 = open, 1 = blocked
    """
    rows, cols = len(grid), len(grid[0])
    directions = [(0,1), (0,-1), (1,0), (-1,0)]
    queue = deque([(start[0], start[1], 0)])  # (row, col, distance)
    visited = {start}

    while queue:
        r, c, dist = queue.popleft()

        if (r, c) == tuple(end):
            return dist

        for dr, dc in directions:
            nr, nc = r + dr, c + dc
            if (0 <= nr < rows and 0 <= nc < cols
                    and grid[nr][nc] == 0
                    and (nr, nc) not in visited):
                visited.add((nr, nc))
                queue.append((nr, nc, dist + 1))

    return -1  # path নেই
```

---

## ২.১০ PART 2 — Interview Q&A

### সেকশন ১: বিস্তারিত প্রশ্নোত্তর

**Q1: Sliding Window এবং Two Pointer এর মধ্যে পার্থক্য কী?**

> **উত্তর:** Sliding Window এ একটি "window" (range) maintain করা হয় যেটি এক দিকে এগোয় — window এর size fixed বা variable হতে পারে। Two Pointer এ দুটি pointer সাধারণত দুই দিক থেকে মাঝে আসে (বা একই দিকে slow/fast)। Overlap আছে — variable sliding window আসলে two pointer এরই একটি form। তবে Two Pointer বেশি general — merge, partition, palindrome check এও কাজ করে।

**Q2: Binary Search এ mid = (lo + hi) / 2 না লিখে lo + (hi - lo) / 2 কেন লিখব?**

> **উত্তর:** Integer overflow এর জন্য। যদি lo এবং hi উভয় INT_MAX এর কাছাকাছি হয়, তাহলে lo + hi overflow করতে পারে (C/Java/C++ এ)। lo + (hi - lo) / 2 সবসময় safe। Python এ arbitrary precision integer আছে তাই সমস্যা নেই, কিন্তু habit হিসেবে এটি লেখাই ভালো।

**Q3: Kadane's Algorithm কীভাবে কাজ করে? Explain করুন।**

> **উত্তর:** Kadane's Algorithm দুটি variable রাখে — current_sum (এখন পর্যন্ত subarray sum) এবং max_sum। প্রতিটি element এ সিদ্ধান্ত নিতে হয়: এই element কে current subarray তে যোগ করব নাকি নতুন subarray শুরু করব? `current_sum = max(arr[i], current_sum + arr[i])` — যদি current_sum negative হয়, নতুন subarray শুরু করা লাভজনক। এটি Dynamic Programming এর একটি form — local optimal থেকে global optimal।

**Q4: Prefix Sum কোন ধরনের problem এ কাজ করে না?**

> **উত্তর:** Prefix Sum কাজ করে না যখন: (১) array frequently update হয় (সব prefix rebuild করতে হবে — এখানে Segment Tree বা BIT better), (২) 2D তে complex query (সরল নয়), (৩) multiplication বা অন্য operations যেখানে sum এর মতো simple নয়।

**Q5: Dynamic Array এর amortized O(1) insertion কীভাবে বুঝবেন?**

> **উত্তর:** n insertions করলে কতটি copy operation হয়? Capacity doubling এ: 1 + 2 + 4 + ... + n = 2n total copies। Total work = n insertions + 2n copies = 3n = O(n)। Per insertion average = O(n)/n = O(1)। Amortized মানে — মাঝে মাঝে একটি insertion O(n) লাগে (copy time), কিন্তু n insertions এর গড় O(1)।

**Q6: Sorted Array তে duplicate সহ binary search কীভাবে করবেন?**

> **উত্তর:** Standard binary search target পেলেই return করে — duplicate এ যেকোনো একটি পাবে। First occurrence এর জন্য: target পেলে result = mid রাখো এবং hi = mid - 1 করে বাম দিকে continue করো। Last occurrence এর জন্য: target পেলে result = mid রাখো এবং lo = mid + 1 করে ডান দিকে continue করো।

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| Array এ random access এর complexity | O(1) |
| Unsorted array এ search | O(n) linear search |
| Sliding Window এর use case | Contiguous subarray/substring |
| Two Pointer এর condition | সাধারণত sorted array |
| Kadane's এর complexity | O(n) time, O(1) space |
| Binary Search এর condition | Sorted array |
| Binary Search এর complexity | O(log n) |
| Prefix Sum build করতে | O(n) |
| Prefix Sum query | O(1) |
| Matrix 90° rotation in-place | Transpose + Reverse rows |
| Dynamic array কখন resize হয়? | Full হলে 2× করে |
| String concatenation ভুল পদ্ধতি | += loop এ (O(n²)) |
| String concatenation সঠিক | join() — O(n) |
| Sliding Window maximum window | Variable — left/right দুই pointer |

### সেকশন ৩: Coding Practice Problems

```
Easy:
  □ Two Sum (unsorted — HashMap, sorted — Two Pointer)
  □ Maximum subarray (Kadane's)
  □ Binary search (standard)
  □ Reverse string in-place
  □ Check palindrome
  □ Remove duplicates from sorted array

Medium:
  □ Longest substring without repeating characters
  □ Container with most water
  □ 3Sum
  □ Minimum window substring
  □ Rotate matrix 90°
  □ Set matrix zeroes
  □ Subarray sum equals K
  □ Search in rotated sorted array

Hard:
  □ Minimum window substring (optimization)
  □ Sliding window maximum (Monotonic deque)
  □ Trapping rain water
  □ Median of two sorted arrays
```

---

> **⚠️ PART 2 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---


<details>
<summary><strong>📙 PART 3 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৩.১ Linked List কী?](#৩১-linked-list-কী)
- [৩.২ Singly Linked List](#৩২-singly-linked-list)
- [৩.৩ Doubly Linked List](#৩৩-doubly-linked-list)
- [৩.৪ Circular Linked List](#৩৪-circular-linked-list)
- [৩.৫ Insert ও Delete Operations](#৩৫-insert-ও-delete-operations)
- [৩.৬ Reverse Linked List](#৩৬-reverse-linked-list)
- [৩.৭ Cycle Detection — Floyd's Algorithm](#৩৭-cycle-detection--floyds-algorithm)
- [৩.৮ Merge Linked Lists](#৩৮-merge-linked-lists)
- [৩.৯ PART 3 — Interview Q&A](#৩৯-part-3--interview-qa)

</details>

<details>
<summary><strong>📕 PART 4 — বিস্তারিত সূচি দেখুন</strong></summary>
<br>

- [৪.১ Stack](#৪১-stack)
- [৪.২ Queue](#৪২-queue)
- [৪.৩ Circular Queue](#৪৩-circular-queue)
- [৪.৪ Deque (Double-Ended Queue)](#৪৪-deque-double-ended-queue)
- [৪.৫ Priority Queue ও Heap](#৪৫-priority-queue-ও-heap)
- [৪.৬ Monotonic Stack](#৪৬-monotonic-stack)
- [৪.৭ Expression Evaluation](#৪৭-expression-evaluation)
- [৪.৮ Infix to Postfix](#৪৮-infix-to-postfix)
- [৪.৯ PART 4 — Interview Q&A](#৪৯-part-4--interview-qa)

</details>



<a id="part3"></a>

# PART 3: Linked List (লিংকড লিস্ট)

> **পড়ার নির্দেশনা:** Linked List হলো pointer/reference ভিত্তিক data structure। Interview তে Reverse, Cycle Detection, Merge — এই তিনটি প্রায় সবসময় জিজ্ঞেস করা হয়। Pointer visualization দিয়ে পড়ুন।

---

## ৩.১ Linked List কী?

### সংজ্ঞা

**Linked List** হলো linear data structure যেখানে elements (node) memory তে contiguous নয় — প্রতিটি node তার data এবং পরবর্তী node এর **reference (pointer)** ধারণ করে।

```
Array (Contiguous):
  [10][20][30][40][50]
   ↑   ↑   ↑   ↑   ↑
  1000 1004 1008 1012 1016  ← memory addresses পাশাপাশি

Linked List (Non-contiguous):
  [10|→] ── [20|→] ── [30|→] ── [40|→] ── [50|None]
  1000        3048       2016       5102       4560
              ↑           ↑           ↑
           যেকোনো       যেকোনো     যেকোনো
           address       address    address
```

### Array vs Linked List

| বিষয় | Array | Linked List |
|------|-------|-------------|
| **Memory** | Contiguous | Scattered |
| **Access** | O(1) random | O(n) sequential |
| **Insert (front)** | O(n) shift | O(1) |
| **Insert (middle)** | O(n) | O(n) traverse + O(1) insert |
| **Insert (end)** | O(1) amortized | O(n) বা O(1) with tail |
| **Delete** | O(n) | O(n) traverse + O(1) delete |
| **Search** | O(n) / O(log n) sorted | O(n) |
| **Extra memory** | No | O(n) for pointers |
| **Cache friendly** | ✅ Yes | ❌ No |

### Node Structure

```python
class Node:
    def __init__(self, data):
        self.data = data    # data field
        self.next = None    # pointer to next node

# Node তৈরি
n1 = Node(10)
n2 = Node(20)
n3 = Node(30)

# Link করা
n1.next = n2
n2.next = n3
# n3.next = None (already)

# Structure:
# n1(10) → n2(20) → n3(30) → None
```

---

## ৩.২ Singly Linked List

### সম্পূর্ণ Implementation

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class SinglyLinkedList:
    def __init__(self):
        self.head = None
        self.size = 0

    # ── Traversal — O(n) ────────────────────────────
    def display(self):
        current = self.head
        nodes = []
        while current:
            nodes.append(str(current.data))
            current = current.next
        print(" → ".join(nodes) + " → None")

    def __len__(self):
        return self.size

    # ── Insert at Beginning — O(1) ──────────────────
    def insert_at_head(self, data):
        new_node = Node(data)
        new_node.next = self.head  # নতুন node head কে point করে
        self.head = new_node       # head সরে যায়
        self.size += 1

    # Visualization:
    # Before: head → [20] → [30] → None
    # After:  head → [10] → [20] → [30] → None

    # ── Insert at End — O(n) ────────────────────────
    def insert_at_tail(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            self.size += 1
            return

        current = self.head
        while current.next:     # শেষ node খুঁজি
            current = current.next
        current.next = new_node # শেষে যোগ
        self.size += 1

    # ── Insert at Position — O(n) ───────────────────
    def insert_at_position(self, pos, data):
        if pos < 0 or pos > self.size:
            raise IndexError("Invalid position")

        if pos == 0:
            self.insert_at_head(data)
            return

        new_node = Node(data)
        current = self.head
        for _ in range(pos - 1):  # pos-1 এ পৌঁছাও
            current = current.next

        new_node.next = current.next
        current.next = new_node
        self.size += 1

    # ── Delete by Value — O(n) ──────────────────────
    def delete_by_value(self, data):
        if not self.head:
            return False

        # Head delete
        if self.head.data == data:
            self.head = self.head.next
            self.size -= 1
            return True

        current = self.head
        while current.next:
            if current.next.data == data:
                current.next = current.next.next  # skip করো
                self.size -= 1
                return True
            current = current.next
        return False

    # Visualization (delete 20):
    # Before: [10] → [20] → [30] → None
    #          ↑
    #        current
    # current.next (20) এর data == 20 → current.next = current.next.next
    # After:  [10] → [30] → None

    # ── Search — O(n) ───────────────────────────────
    def search(self, data):
        current = self.head
        pos = 0
        while current:
            if current.data == data:
                return pos
            current = current.next
            pos += 1
        return -1

    # ── Get by Index — O(n) ─────────────────────────
    def get(self, index):
        if index < 0 or index >= self.size:
            raise IndexError("Index out of range")
        current = self.head
        for _ in range(index):
            current = current.next
        return current.data

# Usage
ll = SinglyLinkedList()
ll.insert_at_tail(10)
ll.insert_at_tail(20)
ll.insert_at_tail(30)
ll.insert_at_head(5)
ll.display()   # 5 → 10 → 20 → 30 → None

ll.delete_by_value(20)
ll.display()   # 5 → 10 → 30 → None
print(ll.search(30))  # 2
```

### Middle Element খোঁজা — Slow/Fast Pointer

```python
def find_middle(head):
    """
    Fast pointer 2 step এগোয়, Slow 1 step।
    Fast শেষে পৌঁছালে Slow মাঝে থাকে।
    """
    slow = head
    fast = head

    while fast and fast.next:
        slow = slow.next       # 1 step
        fast = fast.next.next  # 2 step

    return slow

# Dry Run: 1 → 2 → 3 → 4 → 5 → None
# Initial: slow=1, fast=1
# Step 1:  slow=2, fast=3
# Step 2:  slow=3, fast=5
# fast.next = None → stop
# Middle = 3 ✓ (odd: exact middle; even: second of two middles)
```

---

## ৩.৩ Doubly Linked List

### সংজ্ঞা ও Structure

প্রতিটি node এ **দুটি pointer** — পরবর্তী node (next) এবং পূর্ববর্তী node (prev)।

```
None ← [10] ↔ [20] ↔ [30] ↔ [40] → None
        ↑                           ↑
       head                        tail

Node structure:
  ┌──────┬──────┬──────┐
  │ prev │ data │ next │
  └──────┴──────┴──────┘
```

```python
class DNode:
    def __init__(self, data):
        self.data = data
        self.prev = None
        self.next = None

class DoublyLinkedList:
    def __init__(self):
        self.head = None
        self.tail = None
        self.size = 0

    def insert_at_head(self, data):
        new_node = DNode(data)
        if not self.head:
            self.head = self.tail = new_node
        else:
            new_node.next = self.head
            self.head.prev = new_node
            self.head = new_node
        self.size += 1

    def insert_at_tail(self, data):
        new_node = DNode(data)
        if not self.tail:
            self.head = self.tail = new_node
        else:
            new_node.prev = self.tail
            self.tail.next = new_node
            self.tail = new_node
        self.size += 1

    def delete_node(self, node):
        """O(1) — node reference জানলে directly delete"""
        if node.prev:
            node.prev.next = node.next
        else:
            self.head = node.next  # head ছিল

        if node.next:
            node.next.prev = node.prev
        else:
            self.tail = node.prev  # tail ছিল

        self.size -= 1

    def display_forward(self):
        curr, parts = self.head, []
        while curr:
            parts.append(str(curr.data))
            curr = curr.next
        print("None ↔ " + " ↔ ".join(parts) + " ↔ None")

    def display_backward(self):
        curr, parts = self.tail, []
        while curr:
            parts.append(str(curr.data))
            curr = curr.prev
        print("None ↔ " + " ↔ ".join(parts) + " ↔ None")
```

### Singly vs Doubly

| বিষয় | Singly | Doubly |
|------|--------|--------|
| Pointers per node | 1 (next) | 2 (prev + next) |
| Memory | কম | বেশি |
| Backward traversal | ❌ | ✅ |
| Delete (given node) | O(n) — previous খুঁজতে হয় | O(1) |
| Insert before node | O(n) | O(1) |
| Use case | Stack, simple list | LRU Cache, Browser history |

---

## ৩.৪ Circular Linked List

### সংজ্ঞা

শেষ node এর next pointer প্রথম node (head) কে point করে — কোনো None নেই।

```
Singly Circular:
  head → [10] → [20] → [30] → [40] ─┐
           ↑________________________________┘

Doubly Circular:
  ┌─────────────────────────────┐
  └→ [10] ↔ [20] ↔ [30] ↔ [40] ←┘
```

```python
class CircularLinkedList:
    def __init__(self):
        self.head = None

    def insert_at_end(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            new_node.next = self.head  # নিজেকে point
            return

        # শেষ node খুঁজি (যার next = head)
        current = self.head
        while current.next != self.head:
            current = current.next
        current.next = new_node
        new_node.next = self.head

    def display(self):
        if not self.head:
            return
        current = self.head
        parts = []
        while True:
            parts.append(str(current.data))
            current = current.next
            if current == self.head:
                break
        print(" → ".join(parts) + " → (head)")

    def detect_length(self):
        if not self.head:
            return 0
        count = 1
        current = self.head.next
        while current != self.head:
            count += 1
            current = current.next
        return count
```

### Circular LL এর Use Case

```
✅ Round-robin scheduling (CPU scheduling)
✅ Circular buffer / Ring buffer
✅ Multiplayer game — turn management
✅ Media player — playlist loop
```

---

## ৩.৫ Insert ও Delete Operations

### Insert Positions এর Pointer Visualization

```
Insert 25 between 20 and 30:

Before:
  [10] → [20] → [30] → [40] → None
          ↑
        current (pos-1 তে)

Step 1: new_node = Node(25)
Step 2: new_node.next = current.next  → new_node → [30]
Step 3: current.next = new_node       → [20] → [25]

After:
  [10] → [20] → [25] → [30] → [40] → None
```

```
Delete node 30 (জানা আছে previous node 20):

Before:
  [10] → [20] → [30] → [40] → None
          ↑       ↑
        prev    to_delete

Step: prev.next = to_delete.next  → [20] → [40]

After:
  [10] → [20] → [40] → None
  [30] is now unreferenced → garbage collected
```

### "Delete Given Node" — Tricky Interview Pattern

```python
def delete_given_node(node):
    """
    Head এ access নেই, শুধু delete করার node আছে।
    Last node হবে না এই guarantee আছে।
    """
    # পরের node এর data copy করো
    node.data = node.next.data
    # পরের node skip করো
    node.next = node.next.next

# Visualization: delete node containing 20
# Before: [10] → [20] → [30] → [40] → None
#                  ↑ node
# Step 1: node.data = 30  → [10] → [30] → [30] → [40] → None
# Step 2: node.next = [40] → [10] → [30] → [40] → None ✓
```

---

## ৩.৬ Reverse Linked List

### Iterative Approach — O(n) time, O(1) space

```python
def reverse_iterative(head):
    prev = None
    current = head

    while current:
        next_node = current.next  # ধরে রাখো
        current.next = prev       # উল্টে দাও
        prev = current            # এগিয়ে যাও
        current = next_node

    return prev  # নতুন head

# Dry Run: 1 → 2 → 3 → 4 → None

# Initial: prev=None, current=1
#
# Step 1: next=2, 1.next=None, prev=1, current=2
#   None ← [1]   [2] → [3] → [4] → None
#
# Step 2: next=3, 2.next=1,   prev=2, current=3
#   None ← [1] ← [2]   [3] → [4] → None
#
# Step 3: next=4, 3.next=2,   prev=3, current=4
#   None ← [1] ← [2] ← [3]   [4] → None
#
# Step 4: next=None, 4.next=3, prev=4, current=None
#   None ← [1] ← [2] ← [3] ← [4]
#
# return prev = 4 (নতুন head)
# Final: 4 → 3 → 2 → 1 → None ✓
```

### Recursive Approach — O(n) time, O(n) space (call stack)

```python
def reverse_recursive(head):
    # Base case
    if not head or not head.next:
        return head

    # বাকি list reverse করো
    new_head = reverse_recursive(head.next)

    # head.next কে (এখন শেষে) head কে point করাও
    head.next.next = head
    head.next = None

    return new_head

# Trace: reverse(1 → 2 → 3 → None)
# reverse(1):
#   new_head = reverse(2 → 3 → None)
#     new_head = reverse(3 → None)
#       return 3 (base case)
#     3.next = 2, 2.next = None → 3 → 2 → None
#     return 3
#   3.next = 2, 2.next = 1, 1.next = None → 3 → 2 → 1 → None
#   return 3
```

### Reverse in Groups of K

```python
def reverse_k_group(head, k):
    """প্রতি k টি node কে reverse করো"""
    # k টি node আছে কিনা check
    count = 0
    current = head
    while current and count < k:
        current = current.next
        count += 1

    if count < k:
        return head  # k এর কম বাকি, unchanged

    # প্রথম k টি reverse করো
    prev, curr = None, head
    for _ in range(k):
        nxt = curr.next
        curr.next = prev
        prev = curr
        curr = nxt

    # head এখন শেষে — বাকি অংশকে connect করো
    head.next = reverse_k_group(curr, k)
    return prev
```

---

## ৩.৭ Cycle Detection — Floyd's Algorithm

### সমস্যা

Linked List এ cycle আছে কিনা detect করতে হবে। Cycle মানে — কোনো node এর next তার আগের কোনো node কে point করে।

```
Cycle সহ:
  1 → 2 → 3 → 4 → 5
              ↑       ↓
              8 ← 7 ← 6
```

### Floyd's Tortoise and Hare

```python
def has_cycle(head):
    """O(n) time, O(1) space"""
    slow = head
    fast = head

    while fast and fast.next:
        slow = slow.next        # 1 step (tortoise)
        fast = fast.next.next   # 2 step (hare)

        if slow == fast:        # মিলে গেলে cycle আছে
            return True

    return False  # fast None এ পৌঁছালে cycle নেই

# Intuition:
# Cycle না থাকলে fast ahead চলে শেষে None এ যাবে।
# Cycle থাকলে fast loop এর ভেতরে ঘুরবে,
# slow ও cycle এ ঢুকবে, ধীরে ধীরে fast তাকে ধরবে।
# (যেমন circular track এ দ্রুত runner slower কে lap করে)
```

### Cycle এর Starting Point খোঁজা

```python
def detect_cycle_start(head):
    """
    Floyd's extended: cycle শুরু কোথায়?
    """
    slow = fast = head

    # Phase 1: Meeting point খোঁজো
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow == fast:
            break
    else:
        return None  # cycle নেই

    # Phase 2: Head থেকে ও meeting point থেকে
    # same speed এ চলো — cycle start এ মিলবে
    slow = head
    while slow != fast:
        slow = slow.next
        fast = fast.next

    return slow  # cycle এর শুরু

# Mathematical Proof:
# distance(head → cycle_start) = distance(meeting_point → cycle_start)
# তাই দুই pointer একসাথে চললে cycle start এ মিলবে।
```

### Cycle Length বের করা

```python
def cycle_length(head):
    slow = fast = head

    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow == fast:
            # Meeting point থেকে আবার ঘুরে length বের করো
            length = 1
            current = slow.next
            while current != slow:
                length += 1
                current = current.next
            return length

    return 0  # cycle নেই
```

---

## ৩.৮ Merge Linked Lists

### Merge Two Sorted Linked Lists

```python
def merge_sorted(l1, l2):
    """O(m+n) time, O(1) space (iterative)"""
    # Dummy head — edge cases সহজ করে
    dummy = Node(0)
    current = dummy

    while l1 and l2:
        if l1.data <= l2.data:
            current.next = l1
            l1 = l1.next
        else:
            current.next = l2
            l2 = l2.next
        current = current.next

    # বাকি অংশ attach করো
    current.next = l1 if l1 else l2

    return dummy.next

# Dry Run:
# l1: 1 → 3 → 5
# l2: 2 → 4 → 6

# dummy → 1(l1<l2) → 2(l2<l1) → 3 → 4 → 5 → 6 → None ✓
```

### Merge K Sorted Linked Lists — Heap দিয়ে

```python
import heapq

def merge_k_sorted(lists):
    """O(N log k) — N = total nodes, k = list count"""
    dummy = Node(0)
    current = dummy
    heap = []

    # Initial: প্রতিটি list এর head heap এ
    for i, node in enumerate(lists):
        if node:
            heapq.heappush(heap, (node.data, i, node))

    while heap:
        val, i, node = heapq.heappop(heap)
        current.next = node
        current = current.next
        if node.next:
            heapq.heappush(heap, (node.next.data, i, node.next))

    return dummy.next
```

### Add Two Numbers (Linked List হিসেবে)

```python
def add_two_numbers(l1, l2):
    """
    দুটি number reversed linked list হিসেবে দেওয়া।
    তাদের sum ও reversed linked list এ return করো।
    Input: 2→4→3 (342) + 5→6→4 (465) = 807 → 7→0→8
    """
    dummy = Node(0)
    current = dummy
    carry = 0

    while l1 or l2 or carry:
        val1 = l1.data if l1 else 0
        val2 = l2.data if l2 else 0

        total = val1 + val2 + carry
        carry = total // 10
        digit = total % 10

        current.next = Node(digit)
        current = current.next

        if l1: l1 = l1.next
        if l2: l2 = l2.next

    return dummy.next
```

---

## ৩.৯ PART 3 — Interview Q&A

### সেকশন ১: বিস্তারিত প্রশ্নোত্তর

**Q1: Linked List এবং Array এর মধ্যে কোনটি কখন ব্যবহার করবেন?**

> **উত্তর:** Array: random access দরকার হলে (O(1)), size আগে থেকে জানা থাকলে, cache performance গুরুত্বপূর্ণ হলে। Linked List: frequent insert/delete at beginning দরকার হলে (O(1)), size dynamic এবং unpredictable হলে, memory fragmentation এর সমস্যা থাকলে। Real example: Browser history (doubly LL — forward/back), Undo/Redo (stack-based LL)।

**Q2: Floyd's Cycle Detection Algorithm কীভাবে কাজ করে?**

> **উত্তর:** দুটি pointer — slow (১ step) ও fast (২ step) একসাথে চলে। Cycle না থাকলে fast None এ পৌঁছাবে। Cycle থাকলে fast slow কে eventually overtake করবে এবং একই node এ মিলবে। কারণ: relative speed এর পার্থক্য ১ — তাই cycle এর ভেতরে fast প্রতিটি iteration এ slow থেকে ১ step এগিয়ে যায়, তাই eventually মিলবে। O(n) time, O(1) space।

**Q3: Dummy head node কখন ব্যবহার করবেন?**

> **উত্তর:** Linked List এর head পরিবর্তন হওয়ার সম্ভাবনা থাকলে dummy head ব্যবহার করলে edge cases সহজ হয়। যেমন: merge sorted lists, delete at head, remove nth from end। Dummy node এর data irrelevant — এটি একটি stable entry point। Return করতে হয় dummy.next।

**Q4: Reverse Linked List Recursively এর space complexity কত এবং কেন?**

> **উত্তর:** O(n) — কারণ n টি recursive call stack এ জমা হয়। Iterative reverse এ O(1) space কারণ শুধু ৩টি pointer (prev, current, next) লাগে। Interview তে বলুন: "Space critical হলে iterative prefer করব।"

**Q5: "Delete given node without head" — কীভাবে করবেন?**

> **উত্তর:** পরের node এর data কে current node এ copy করো, তারপর পরের node কে skip করো। `node.data = node.next.data; node.next = node.next.next`। Limitation: Last node এ কাজ করে না (কারণ next নেই)।

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| LL এ random access | O(n) |
| Head তে insert | O(1) |
| Tail এ insert (without tail pointer) | O(n) |
| Middle element খোঁজা | Slow/Fast pointer |
| Cycle detect করতে | Floyd's algorithm |
| Reverse LL iterative space | O(1) |
| Reverse LL recursive space | O(n) call stack |
| Merge 2 sorted LL | O(m+n), dummy head |
| Doubly LL এ node delete (given node) | O(1) |
| Circular LL traversal থামানো | current == head |
| LRU Cache তে কোন LL? | Doubly LL + HashMap |
| k-group reverse | Recursive + count |

---

> **⚠️ PART 3 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

<a id="part4"></a>

# PART 4: Stack & Queue (স্ট্যাক ও কিউ)

> **পড়ার নির্দেশনা:** Stack ও Queue হলো দুটি fundamental abstract data types। Interview তে Monotonic Stack ও Expression Evaluation প্রায়ই জিজ্ঞেস করা হয়। Real-life analogies দিয়ে concepts বুঝুন।

---

## ৪.১ Stack

### সংজ্ঞা

**Stack** হলো LIFO (Last In, First Out) data structure। সবশেষে যা ঢুকেছে সেটি সবার আগে বের হয়।

```
Real-life Analogy — বই এর স্তুপ:
  Push(C): [A][B][C]  ← TOP
  Push(D): [A][B][C][D]  ← TOP
  Pop():   [A][B][C]  ← C বের হলো না, D বের হলো!
  Peek():  C দেখা যাচ্ছে কিন্তু তোলা হচ্ছে না

Operations:
  push(x)  → TOP এ element যোগ   — O(1)
  pop()    → TOP থেকে remove     — O(1)
  peek()   → TOP element দেখা    — O(1)
  isEmpty  → খালি কিনা           — O(1)
  size()   → element সংখ্যা      — O(1)
```

### Implementation — Array দিয়ে

```python
class ArrayStack:
    def __init__(self, capacity=1000):
        self._data = [None] * capacity
        self._top = -1
        self._capacity = capacity

    def push(self, x):
        if self._top == self._capacity - 1:
            raise OverflowError("Stack is full")
        self._top += 1
        self._data[self._top] = x

    def pop(self):
        if self.is_empty():
            raise IndexError("Stack is empty")
        val = self._data[self._top]
        self._data[self._top] = None
        self._top -= 1
        return val

    def peek(self):
        if self.is_empty():
            raise IndexError("Stack is empty")
        return self._data[self._top]

    def is_empty(self):
        return self._top == -1

    def size(self):
        return self._top + 1
```

### Implementation — Python List দিয়ে (সহজ)

```python
class Stack:
    def __init__(self):
        self._stack = []

    def push(self, x):
        self._stack.append(x)      # O(1) amortized

    def pop(self):
        if self.is_empty():
            raise IndexError("Stack underflow")
        return self._stack.pop()   # O(1)

    def peek(self):
        return self._stack[-1] if self._stack else None

    def is_empty(self):
        return len(self._stack) == 0

    def size(self):
        return len(self._stack)

# Python built-in: list as stack
stack = []
stack.append(10)   # push
stack.append(20)
stack.append(30)
print(stack[-1])   # peek → 30
stack.pop()        # pop → 30
```

### Valid Parentheses — Classic Stack Problem

```python
def is_valid_parentheses(s):
    """
    '(', '{', '[' — opening
    ')', '}', ']' — closing
    সব pair সঠিকভাবে বন্ধ আছে কিনা?
    """
    stack = []
    mapping = {')': '(', '}': '{', ']': '['}

    for char in s:
        if char in '({[':
            stack.append(char)
        elif char in ')}]':
            if not stack or stack[-1] != mapping[char]:
                return False
            stack.pop()

    return len(stack) == 0

# Dry Run: s = "({[]})"
# '(' → push: ['(']
# '{' → push: ['(', '{']
# '[' → push: ['(', '{', '[']
# ']' → mapping[']']='[', top='[' ✓ pop: ['(', '{']
# '}' → mapping['}']='{', top='{' ✓ pop: ['(']
# ')' → mapping[')']=\'(\', top='(' ✓ pop: []
# stack empty → True ✓
```

### Stack এর Real-World Use Cases

```
✅ Function call management (Call Stack)
✅ Undo/Redo operations (text editors)
✅ Browser back/forward navigation
✅ Expression evaluation (infix/postfix)
✅ DFS (Depth First Search)
✅ Balanced parentheses check
✅ Syntax parsing (compilers)
✅ Backtracking algorithms
```

### Min Stack — O(1) minimum

```python
class MinStack:
    """সব operation O(1) — minimum সবসময় track রাখে"""
    def __init__(self):
        self.stack = []     # (value, current_min) tuple
    
    def push(self, val):
        current_min = min(val, self.stack[-1][1]) if self.stack else val
        self.stack.append((val, current_min))
    
    def pop(self):
        return self.stack.pop()[0]
    
    def top(self):
        return self.stack[-1][0]
    
    def get_min(self):
        return self.stack[-1][1]

# Usage:
ms = MinStack()
ms.push(5)   # stack: [(5,5)]
ms.push(3)   # stack: [(5,5),(3,3)]
ms.push(7)   # stack: [(5,5),(3,3),(7,3)]
ms.get_min() # 3 ✓
ms.pop()     # 7 removed
ms.get_min() # 3 ✓
ms.pop()     # 3 removed
ms.get_min() # 5 ✓
```

---

## ৪.২ Queue

### সংজ্ঞা

**Queue** হলো FIFO (First In, First Out) data structure। প্রথমে যা ঢুকেছে সেটি প্রথমে বের হয়।

```
Real-life Analogy — ব্যাংকের লাইন:
  Enqueue(A): [A]         ← REAR
  Enqueue(B): [A][B]      ← REAR
  Enqueue(C): [A][B][C]   ← REAR
  Dequeue():  [B][C]      ← A বের হলো (FRONT থেকে)

  FRONT ──────────────── REAR
  [B]   →   [C]   →   (next will be here)
  dequeue                 enqueue
```

### Implementation — collections.deque দিয়ে (Optimal)

```python
from collections import deque

class Queue:
    def __init__(self):
        self._queue = deque()

    def enqueue(self, x):
        self._queue.append(x)       # O(1) — rear এ

    def dequeue(self):
        if self.is_empty():
            raise IndexError("Queue is empty")
        return self._queue.popleft()  # O(1) — front থেকে

    def front(self):
        return self._queue[0] if self._queue else None

    def rear(self):
        return self._queue[-1] if self._queue else None

    def is_empty(self):
        return len(self._queue) == 0

    def size(self):
        return len(self._queue)

# ⚠️ List দিয়ে Queue বানালে popleft() O(n) — এড়িয়ে চলুন
# deque তে append ও popleft উভয়ই O(1)
```

### Queue এর Real-World Use Cases

```
✅ BFS (Breadth First Search)
✅ CPU Process Scheduling
✅ Printer Queue
✅ Message Queue (RabbitMQ, Kafka)
✅ Web Server Request Handling
✅ Level-order Tree Traversal
✅ Cache Replacement (FIFO policy)
```

### BFS with Queue

```python
from collections import deque

def bfs(graph, start):
    """Graph BFS — O(V + E)"""
    visited = set([start])
    queue = deque([start])
    order = []

    while queue:
        node = queue.popleft()
        order.append(node)

        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)

    return order
```

---

## ৪.৩ Circular Queue

### সমস্যা

Regular array-based queue তে dequeue করার পরে front এর আগের জায়গা waste হয়।

```
Regular Queue সমস্যা:
  Initial:  [_][_][_][_][_]  front=0, rear=-1
  Enqueue A: [A][_][_][_][_]  front=0, rear=0
  Enqueue B: [A][B][_][_][_]  front=0, rear=1
  Dequeue:   [_][B][_][_][_]  front=1, rear=1
  Dequeue:   [_][_][_][_][_]  front=2, rear=1
  Enqueue C: [_][_][C][_][_]  front=2, rear=2
  ...
  Enqueue তে rear শেষে যাবে, কিন্তু front এর আগে জায়গা খালি!
```

### Circular Queue — Modular Arithmetic

```python
class CircularQueue:
    def __init__(self, capacity):
        self.capacity = capacity
        self.queue = [None] * capacity
        self.front = 0
        self.rear = -1
        self.size = 0

    def enqueue(self, x):
        if self.is_full():
            raise OverflowError("Circular Queue is full")
        self.rear = (self.rear + 1) % self.capacity  # circular!
        self.queue[self.rear] = x
        self.size += 1

    def dequeue(self):
        if self.is_empty():
            raise IndexError("Circular Queue is empty")
        val = self.queue[self.front]
        self.queue[self.front] = None
        self.front = (self.front + 1) % self.capacity  # circular!
        self.size -= 1
        return val

    def is_empty(self):
        return self.size == 0

    def is_full(self):
        return self.size == self.capacity

    def peek_front(self):
        return self.queue[self.front] if not self.is_empty() else None

# Visualization: capacity=5, wraparound
# [D][E][_][A][B][C] → front=3(A), rear=1(E)
#  0  1  2  3  4
# Enqueue F: rear = (1+1)%5 = 2 → [D][E][F][A][B][C]
```

---

## ৪.৪ Deque (Double-Ended Queue)

### সংজ্ঞা

**Deque** (Double-Ended Queue) — দুই দিক থেকেই insert ও delete করা যায়।

```
         addFirst  addLast
            ↓         ↓
  FRONT → [A][B][C][D] ← REAR
            ↑         ↑
        removeFirst  removeLast
```

```python
from collections import deque

dq = deque()

# Add
dq.append(10)        # right end: [10]
dq.append(20)        # right: [10, 20]
dq.appendleft(5)     # left: [5, 10, 20]
dq.appendleft(1)     # left: [1, 5, 10, 20]

# Remove
dq.pop()             # right: [1, 5, 10] (20 removed)
dq.popleft()         # left:  [5, 10]    (1 removed)

# Peek
print(dq[0])         # 5 (front)
print(dq[-1])        # 10 (rear)

# All O(1)!
```

### Sliding Window Maximum — Deque দিয়ে O(n)

```python
def sliding_window_max(arr, k):
    """
    প্রতিটি k-size window এর maximum খোঁজো।
    Brute: O(nk), Deque: O(n)
    """
    from collections import deque
    dq = deque()  # indices store করে, decreasing order এ values
    result = []

    for i in range(len(arr)):
        # Window এর বাইরে চলে গেছে এমন index বাদ দাও
        while dq and dq[0] < i - k + 1:
            dq.popleft()

        # Smaller element বাদ দাও (তারা কখনো maximum হবে না)
        while dq and arr[dq[-1]] < arr[i]:
            dq.pop()

        dq.append(i)

        # Window complete হলে result যোগ করো
        if i >= k - 1:
            result.append(arr[dq[0]])

    return result

# Dry Run: arr=[3,1,2,5,4,2,3], k=3
# i=0: dq=[0], no result
# i=1: arr[1]=1 < arr[0]=3, dq=[0,1], no result
# i=2: arr[2]=2 > arr[1]=1 → pop 1, dq=[0,2], result=[arr[0]]=3
# i=3: arr[3]=5>arr[2]=2→pop, 5>arr[0]=3→pop, dq=[3], result=[3,5]
# i=4: arr[4]=4<5, dq=[3,4], result=[3,5,5]
# i=5: arr[5]=2<4, dq=[3,4,5], dq[0]=3 < 5-3+1=3? No, result=[3,5,5,5]
# i=6: arr[6]=3>arr[5]=2→pop5, 3<arr[4]=4, dq=[3,4,6]
#       dq[0]=3 < 6-3+1=4 → popleft, dq=[4,6], result=[3,5,5,5,4]
# Final: [3, 5, 5, 5, 4]
```

---

## ৪.৫ Priority Queue ও Heap

### সংজ্ঞা

**Priority Queue** হলো এমন queue যেখানে highest priority element সবার আগে dequeue হয়। সাধারণত **Binary Heap** দিয়ে implement করা হয়।

```
Min-Heap: সবচেয়ে ছোট element সবার আগে বের হয়
Max-Heap: সবচেয়ে বড় element সবার আগে বের হয়

Binary Heap properties:
  1. Complete Binary Tree (বামদিক থেকে fill হয়)
  2. Min-Heap: parent ≤ children সবসময়

Min-Heap উদাহরণ:
          1
        /          3     5
      / \   /      7   8  9  10
```

### Python heapq (Min-Heap)

```python
import heapq

# Min-Heap
heap = []
heapq.heappush(heap, 5)
heapq.heappush(heap, 1)
heapq.heappush(heap, 3)
heapq.heappush(heap, 2)

print(heap[0])              # 1 — minimum, O(1) peek
print(heapq.heappop(heap))  # 1 — O(log n)
print(heapq.heappop(heap))  # 2

# Heapify existing list — O(n)
arr = [5, 3, 8, 1, 9, 2]
heapq.heapify(arr)
print(arr[0])  # 1 — minimum

# Max-Heap: negate করুন
max_heap = []
heapq.heappush(max_heap, -5)
heapq.heappush(max_heap, -1)
heapq.heappush(max_heap, -3)
print(-heapq.heappop(max_heap))  # 5 (maximum)

# K largest elements
nums = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3]
k = 3
print(heapq.nlargest(k, nums))   # [9, 6, 5]
print(heapq.nsmallest(k, nums))  # [1, 1, 2]
```

### Heap Sort — O(n log n)

```python
def heap_sort(arr):
    n = len(arr)

    # Max-Heap তৈরি করো (bottom-up heapify)
    for i in range(n // 2 - 1, -1, -1):
        heapify(arr, n, i)

    # Root (max) সরিয়ে শেষে রাখো
    for i in range(n - 1, 0, -1):
        arr[0], arr[i] = arr[i], arr[0]  # root ↔ শেষ
        heapify(arr, i, 0)               # remaining heap restore

def heapify(arr, n, i):
    largest = i
    left = 2 * i + 1
    right = 2 * i + 2

    if left < n and arr[left] > arr[largest]:
        largest = left
    if right < n and arr[right] > arr[largest]:
        largest = right

    if largest != i:
        arr[i], arr[largest] = arr[largest], arr[i]
        heapify(arr, n, largest)
```

### K-th Largest Element

```python
def find_kth_largest(nums, k):
    """Min-Heap of size k — O(n log k)"""
    heap = []
    for num in nums:
        heapq.heappush(heap, num)
        if len(heap) > k:
            heapq.heappop(heap)   # ছোটটা বাদ
    return heap[0]   # k-th largest = heap এর minimum

# Intuition: k টি largest রাখি heap এ।
# নতুন element বড় হলে → ছোটটা বের করি, নতুনটা রাখি।
# শেষে heap তে k largest → minimum = k-th largest।
```

---

## ৪.৬ Monotonic Stack

### সংজ্ঞা

**Monotonic Stack** হলো এমন stack যেখানে elements সবসময় increasing বা decreasing order এ থাকে।

```
Monotonic Increasing Stack:
  [1, 3, 5, 7] — bottom থেকে top পর্যন্ত বাড়তে থাকে
  নতুন element যোগ করার সময় ছোট elements পপ করা হয়

Monotonic Decreasing Stack:
  [7, 5, 3, 1] — top থেকে bottom পর্যন্ত বাড়তে থাকে
```

### Next Greater Element

```python
def next_greater_element(arr):
    """
    প্রতিটি element এর ডানে প্রথম বড় element কোনটি?
    O(n) — প্রতিটি element একবার push, একবার pop।
    """
    n = len(arr)
    result = [-1] * n
    stack = []  # indices (monotonic decreasing values)

    for i in range(n):
        # Stack এর top যদি arr[i] এর চেয়ে ছোট হয়
        while stack and arr[stack[-1]] < arr[i]:
            idx = stack.pop()
            result[idx] = arr[i]  # arr[i] হলো next greater
        stack.append(i)

    return result

# Dry Run: arr = [4, 5, 2, 10, 8]
#
# i=0: stack=[], push 0,   stack=[0]
# i=1: arr[0]=4 < arr[1]=5 → result[0]=5, pop; push 1, stack=[1]
# i=2: arr[1]=5 > arr[2]=2 → push 2, stack=[1,2]
# i=3: arr[2]=2 < 10 → result[2]=10, pop
#       arr[1]=5 < 10 → result[1]=10, pop
#       push 3, stack=[3]
# i=4: arr[3]=10 > arr[4]=8 → push 4, stack=[3,4]
# End: stack=[3,4] → result[3]=-1, result[4]=-1
#
# result = [5, 10, 10, -1, -1] ✓
```

### Previous Smaller Element

```python
def previous_smaller(arr):
    """প্রতিটি element এর বামে প্রথম ছোট element"""
    n = len(arr)
    result = [-1] * n
    stack = []  # monotonic increasing

    for i in range(n):
        while stack and stack[-1] >= arr[i]:
            stack.pop()
        result[i] = stack[-1] if stack else -1
        stack.append(arr[i])

    return result
```

### Largest Rectangle in Histogram

```python
def largest_rectangle(heights):
    """
    Histogram এ সবচেয়ে বড় rectangle এর area।
    Monotonic Stack দিয়ে O(n)।
    """
    stack = []  # indices, increasing heights
    max_area = 0
    n = len(heights)

    for i in range(n + 1):
        h = heights[i] if i < n else 0  # sentinel 0

        while stack and heights[stack[-1]] > h:
            height = heights[stack.pop()]
            width = i if not stack else i - stack[-1] - 1
            max_area = max(max_area, height * width)

        stack.append(i)

    return max_area

# heights = [2, 1, 5, 6, 2, 3]
# Maximum rectangle = 10 (heights 5,6 × width 2)
```

### Monotonic Stack Pattern চেনার উপায়

```
এই keywords দেখলে Monotonic Stack ভাবুন:
  → "Next Greater/Smaller Element"
  → "Previous Greater/Smaller Element"
  → "Largest Rectangle in Histogram"
  → "Trapping Rain Water"
  → "Daily Temperatures"
  → "Stock Span Problem"
```

### Daily Temperatures

```python
def daily_temperatures(temperatures):
    """কতদিন পরে temperature বাড়বে?"""
    n = len(temperatures)
    result = [0] * n
    stack = []  # indices

    for i in range(n):
        while stack and temperatures[stack[-1]] < temperatures[i]:
            idx = stack.pop()
            result[idx] = i - idx   # দিনের পার্থক্য
        stack.append(i)

    return result

# temperatures = [73,74,75,71,69,72,76,73]
# result =       [1, 1, 4, 2, 1, 1, 0, 0]
```

---

## ৪.৭ Expression Evaluation

### Expression এর প্রকারভেদ

```
Infix:   A + B   (operator মাঝে — মানুষ পড়ে)
Prefix:  + A B   (operator আগে — Polish notation)
Postfix: A B +   (operator পরে — Reverse Polish / machine friendly)

কেন Postfix ভালো?
  → কোনো parentheses দরকার নেই
  → Priority সমস্যা নেই
  → Stack দিয়ে সহজে evaluate করা যায়
```

### Postfix Evaluation

```python
def evaluate_postfix(expression):
    """
    Postfix expression evaluate করো।
    Input: "3 4 + 2 * 7 /"
    Output: (3+4)*2/7 = 2
    """
    stack = []
    tokens = expression.split()

    for token in tokens:
        if token.lstrip('-').isdigit():   # number
            stack.append(int(token))
        else:                             # operator
            b = stack.pop()   # দ্বিতীয় operand
            a = stack.pop()   # প্রথম operand
            if token == '+':
                stack.append(a + b)
            elif token == '-':
                stack.append(a - b)
            elif token == '*':
                stack.append(a * b)
            elif token == '/':
                stack.append(int(a / b))  # truncate toward zero

    return stack[0]

# Dry Run: "3 4 + 2 *"
# token=3: stack=[3]
# token=4: stack=[3,4]
# token=+: b=4, a=3, push 7; stack=[7]
# token=2: stack=[7,2]
# token=*: b=2, a=7, push 14; stack=[14]
# return 14 ✓ (3+4)*2 = 14
```

---

## ৪.৮ Infix to Postfix

### Shunting-Yard Algorithm

```python
def infix_to_postfix(expression):
    """
    Dijkstra's Shunting-Yard Algorithm
    Rules:
      1. Operand → directly output
      2. '(' → push to stack
      3. ')' → pop until '('
      4. Operator → pop higher/equal priority operators, then push
    """
    precedence = {'+': 1, '-': 1, '*': 2, '/': 2, '^': 3}
    right_assoc = {'^'}  # right-associative operators

    output = []
    stack = []

    for token in expression.split():
        if token.lstrip('-').replace('.','').isdigit():
            output.append(token)               # Operand

        elif token == '(':
            stack.append(token)

        elif token == ')':
            while stack and stack[-1] != '(':
                output.append(stack.pop())
            stack.pop()  # '(' remove

        else:  # Operator
            while (stack and stack[-1] != '('
                   and stack[-1] in precedence
                   and (precedence[stack[-1]] > precedence[token]
                        or (precedence[stack[-1]] == precedence[token]
                            and token not in right_assoc))):
                output.append(stack.pop())
            stack.append(token)

    while stack:
        output.append(stack.pop())

    return ' '.join(output)

# infix_to_postfix("3 + 4 * 2")       → "3 4 2 * +"
# infix_to_postfix("( 3 + 4 ) * 2")   → "3 4 + 2 *"
# infix_to_postfix("A + B * C - D")   → "A B C * + D -"
```

### Dry Run — "A + B * C"

```
Operator precedence: * > +

Token  Action              Output       Stack
A      → output            [A]          []
+      push                [A]          [+]
B      → output            [A,B]        [+]
*      * > + → push        [A,B]        [+,*]
C      → output            [A,B,C]      [+,*]
end    pop all             [A,B,C,*,+]  []

Postfix: A B C * +
Verify: A + B*C = A + (B*C) ✓
```

### Evaluate Infix Directly (Two Stacks)

```python
def evaluate_infix(expression):
    """Values stack + Operators stack"""
    precedence = {'+': 1, '-': 1, '*': 2, '/': 2}
    values = []
    ops = []

    def apply_op():
        op = ops.pop()
        b, a = values.pop(), values.pop()
        if op == '+': values.append(a + b)
        elif op == '-': values.append(a - b)
        elif op == '*': values.append(a * b)
        elif op == '/': values.append(int(a / b))

    for token in expression.split():
        if token.lstrip('-').isdigit():
            values.append(int(token))
        elif token == '(':
            ops.append(token)
        elif token == ')':
            while ops[-1] != '(':
                apply_op()
            ops.pop()
        else:
            while (ops and ops[-1] in precedence
                   and precedence[ops[-1]] >= precedence[token]):
                apply_op()
            ops.append(token)

    while ops:
        apply_op()

    return values[0]
```

---

## ৪.৯ PART 4 — Interview Q&A

### সেকশন ১: বিস্তারিত প্রশ্নোত্তর

**Q1: Stack এবং Queue এর মধ্যে মূল পার্থক্য কী? কোনটি কোথায় ব্যবহার হয়?**

> **উত্তর:** Stack = LIFO। সবশেষে ঢুকেছে সেটি সবার আগে বের হয়। Use case: DFS, Function call, Undo/Redo, Expression eval। Queue = FIFO। সবার আগে ঢুকেছে সেটি সবার আগে বের হয়। Use case: BFS, Process scheduling, Print queue, Message broker। Interview tip: "DFS → Stack, BFS → Queue" এই rule মনে রাখুন।

**Q2: Circular Queue কেন দরকার? Regular Queue এ সমস্যা কী?**

> **উত্তর:** Array-based regular Queue তে dequeue করলে front এর আগের indices waste হয়। rear index array এর শেষে পৌঁছালে নতুন element রাখা যায় না — even though শুরুতে জায়গা আছে। Circular Queue তে modular arithmetic (`(rear + 1) % capacity`) ব্যবহার করে এই waste এড়ানো হয়। Ring Buffer, Audio streaming, Network packet buffering এ ব্যবহার হয়।

**Q3: Monotonic Stack কী? কোন ধরনের problem এ কাজ করে?**

> **উত্তর:** Monotonic Stack এ elements সবসময় monotonic (increasing বা decreasing) order এ থাকে। নতুন element push করার সময় monotonicity ভাঙলে উপযুক্ত elements pop করা হয়। কাজ করে: Next/Previous Greater/Smaller Element, Largest Rectangle in Histogram, Trapping Rain Water, Daily Temperatures। Brute O(n²) কে O(n) এ আনে — প্রতিটি element একবার push ও একবার pop।

**Q4: Priority Queue সাধারণত কীভাবে implement করা হয়?**

> **উত্তর:** Binary Heap দিয়ে। Min-Heap: parent সবসময় children এর চেয়ে ছোট বা সমান। Operations: insert O(log n), extract-min O(log n), peek-min O(1)। Python এ `heapq` module হলো min-heap। Max-heap এর জন্য values negate করুন। Use case: Dijkstra's algorithm, Task scheduling, K-th largest/smallest।

**Q5: Postfix evaluation এ কেন parentheses লাগে না?**

> **উত্তর:** Postfix (Reverse Polish Notation) এ operator এর position নিজেই operands এর বন্ধন নির্ধারণ করে। Stack ব্যবহার করে left-to-right scan করলে প্রতিটি operator তার ঠিক আগের দুটি operand এর উপর apply হয়। কোনো ambiguity নেই — priority বা associativity আলাদাভাবে বলতে হয় না।

### সেকশন ২: Rapid-Fire

| প্রশ্ন | উত্তর |
|-------|-------|
| Stack এর order | LIFO |
| Queue এর order | FIFO |
| Stack এর push/pop | O(1) |
| Queue enqueue/dequeue | O(1) (deque) |
| Min Stack এর getMin | O(1) |
| Heap peek | O(1) |
| Heap push/pop | O(log n) |
| Heapify n elements | O(n) |
| Monotonic Stack problem | Next Greater Element |
| Valid parentheses | Stack দিয়ে |
| Sliding Window Max | Deque, O(n) |
| Postfix eval | Single stack |
| Infix to Postfix | Shunting-yard, operator stack |
| DFS কোন DS | Stack |
| BFS কোন DS | Queue |
| K-th largest | Min-Heap size k |

---

> **⚠️ PART 4 সম্পন্ন হয়েছে।**

<div align="right"><a href="#top">⬆ শীর্ষে ফিরুন</a> &nbsp;|&nbsp; <a href="#toc">📋 সূচিপত্র</a></div>

---

*হ্যান্ডবুক তৈরিতে: Senior Software Engineer, Competitive Programmer & DSA Instructor*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 12 | চলমান — PART 1–4 সম্পন্ন*
