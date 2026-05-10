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
| 📙 | **PART 3** — Linked List | *(শীঘ্রই আসছে)* |
| 📕 | **PART 4** — Stack & Queue | *(শীঘ্রই আসছে)* |
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

*হ্যান্ডবুক তৈরিতে: Senior Software Engineer, Competitive Programmer & DSA Instructor*
*Version: 1.0 | তারিখ: মে ২০২৬*
*মোট PART: 12 | চলমান — PART 1 ও 2 সম্পন্ন*
