<a id="top"></a>

# 🐍 Python Interview Preparation Handbook
### বাংলাদেশের Junior SWE, Python Developer, Backend Developer, এবং Automation Engineer-দের জন্য Part-by-Part Handbook

> **💡 ব্যবহার নির্দেশিকা:**
> এই handbook Bangla-তে লেখা, কিন্তু interview-এ যেসব English technical term শোনা যাবে সেগুলো রাখা হয়েছে। প্রতিটি topic এ Definition, Real-life Analogy, Practical Use Case, Interview-style Explanation, Common Mistakes, Follow-up Questions, এবং Code Example আছে।

---

<a id="toc"></a>

## 📋 PART 1 সূচিপত্র — Python Fundamentals

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [What is Python](#what-is-python) | Python কী, কেন use করা হয় |
| 2 | [History of Python](#history-of-python) | Python এর origin ও evolution |
| 3 | [Features of Python](#features-of-python) | Python এর major strengths |
| 4 | [Python Installation](#python-installation) | Install, version check, environment setup |
| 5 | [Python Execution Flow](#python-execution-flow) | Code কীভাবে run হয় |
| 6 | [Variables](#variables) | Variable, naming, assignment |
| 7 | [Data Types](#data-types) | Numeric, string, boolean, collection types |
| 8 | [Type Casting](#type-casting) | Explicit vs implicit conversion |
| 9 | [Input/Output](#inputoutput) | input(), print(), formatting |
| 10 | [Operators](#operators) | Arithmetic, comparison, logical, bitwise |
| 11 | [Conditional Statements](#conditional-statements) | if, elif, else, nested condition |
| 12 | [Loops](#loops) | for, while, break, continue, else |
| 13 | [Functions](#functions) | Reusable logic, return, default values |
| 14 | [Arguments & Parameters](#arguments--parameters) | Positional, keyword, *args, **kwargs |
| 15 | [Lambda Functions](#lambda-functions) | Anonymous function, use cases |
| 16 | [Scope](#scope) | local, global, nonlocal |
| 17 | [Modules & Packages](#modules--packages) | import system, package structure |
| 18 | [Virtual Environment](#virtual-environment) | venv, dependency isolation |

---

## 1. What is Python

**Definition:**
Python হলো একটি high-level, interpreted, general-purpose programming language. এটি পড়তে সহজ, লিখতে সহজ, এবং beginner-friendly। Python দিয়ে web backend, automation, data analysis, scripting, AI/ML, testing, DevOps tool, এমনকি desktop app-ও বানানো যায়।

**Real-life Analogy:**
Python কে আপনি একটি **smart assistant** হিসেবে ভাবতে পারেন। আপনি assistant-কে খুব পরিষ্কারভাবে বলেন কী করতে হবে, আর সে অনেক technical complexity নিজের ভিতরে manage করে ফেলে।

**Practical Use Case:**
বাংলাদেশের অনেক software company Python use করে:
- API backend তৈরিতে
- automation script লেখায়
- log analysis ও reporting এ
- test automation এ
- internal tools তৈরিতে

**Interview-style Explanation:**
> "Python হলো একটি simple, readable, interpreted language. আমি Python পছন্দ করি কারণ এর syntax clean, development speed fast, এবং backend, automation, data-related কাজ এক language দিয়েই করা যায়। Junior developer হিসেবে Python দ্রুত problem solve করতে সাহায্য করে।"

**Common Mistakes:**
- Python কে শুধু scripting language ভাবা
- Interpreted মানে slow, তাই production এ use করা যাবে না মনে করা
- Python শুধুই beginnerদের জন্য মনে করা

**Follow-up Interview Questions:**
1. Python কে interpreted বলা হয় কেন?
2. Python কি compiled language না interpreted language?
3. Python কোথায় best use হয়?

**Code Example:**
```python
name = "Rahim"
age = 24
print(f"Name: {name}, Age: {age}")
```

---

## 2. History of Python

**Definition:**
Python তৈরি করেন Guido van Rossum। তিনি 1989 সালে Python develop করা শুরু করেন, এবং 1991 সালে প্রথম public version release হয়। Python এর নাম এসেছে "Monty Python" comedy group থেকে।

**Real-life Analogy:**
Python এর evolution কে একটি **school syllabus** পরিবর্তনের মতো ভাবতে পারেন। শুরুতে syllabus ছোট ছিল, পরে বাস্তব প্রয়োজন অনুযায়ী new chapter যোগ হয়েছে।

**Practical Use Case:**
History জানা interview-এ help করে, কারণ interviewer often asks:
- কেন Python তৈরি করা হয়েছিল?
- Python 2 এবং Python 3 এর পার্থক্য কী?
- Python 3 কেন preferred?

**Interview-style Explanation:**
> "Python Guido van Rossum তৈরি করেন readability, simplicity, এবং productivity focus করে। Python 2 থেকে Python 3 এ major changes আসে, especially Unicode, print function, and better language design এর জন্য। আজ Python 3 modern development এর standard।"

**Common Mistakes:**
- Python 2 আর Python 3 কে same ধরে নেওয়া
- Python 2 এখনও production standard মনে করা
- Python এর creator ভুলে যাওয়া

**Follow-up Interview Questions:**
1. Python 2 কেন deprecated?
2. Python 3 এর major improvements কী?
3. Why was Python named after Monty Python?

**Code Example:**
```python
print("Python 3 is the modern standard version")
```

---

## 3. Features of Python

**Definition:**
Python-এর কিছু key feature হলো readability, simple syntax, large standard library, cross-platform support, dynamic typing, object-oriented support, and huge ecosystem।

**Real-life Analogy:**
Python কে একটি **multi-tool knife** এর মতো ভাবতে পারেন। একই tool দিয়ে multiple কাজ করা যায়, তাই developer productivity বেড়ে যায়।

**Practical Use Case:**
- দ্রুত prototype বানানো
- REST API development
- automation script
- data parsing
- test writing

**Interview-style Explanation:**
> "Python জনপ্রিয় কারণ এটি readable, fast to develop, and versatile. Small team দিয়েও production-grade system build করা যায়। Standard library এবং third-party packages ecosystem খুব strong।"

**Common Mistakes:**
- শুধু syntax দেখে feature explain করা
- readability, library ecosystem, portability mention না করা
- features কে shallow ভাবে বলা

**Quick Comparison Table:**

| Feature | Why it matters |
|---|---|
| Readable syntax | Code সহজে বুঝতে পারে team member |
| Interpreted | দ্রুত test ও run করা যায় |
| Cross-platform | Windows, Linux, macOS-এ চলে |
| Large ecosystem | অনেক ready-made package পাওয়া যায় |
| Dynamic typing | Rapid development possible |
| Standard library | Extra package ছাড়াও অনেক কাজ হয় |

**Follow-up Interview Questions:**
1. Python dynamic typed হলেও type hints কেন লাগে?
2. Why is Python considered productive?
3. What is the role of standard library?

**Code Example:**
```python
numbers = [1, 2, 3, 4]
print(sum(numbers))
```

---

## 4. Python Installation

**Definition:**
Python install মানে interpreter, pip, এবং basic tooling setup করা। বাংলাদেশে interview-এর আগে candidate-কে command line থেকে version check, venv create, and package install জানতেই হয়।

**Real-life Analogy:**
Python installation কে **kitchen setup** হিসেবে ভাবতে পারেন। রান্না শুরু করার আগে stove, gas, pan, knife সব ready থাকতে হবে।

**Practical Use Case:**
- নতুন project start করা
- version mismatch সমস্যা সমাধান করা
- dependency install করা

**Interview-style Explanation:**
> "আমি Python install করার পর প্রথমে version check করি, তারপর virtual environment create করি, তারপর pip দিয়ে required packages install করি। এতে global system Python নষ্ট না করে project-wise dependency manage করা যায়।"

**Common Mistakes:**
- system Python-এর ওপর সরাসরি package install করা
- `python` এবং `python3` command confusion
- pip version check না করা
- PATH ঠিকমতো set না করা

**Installation Commands:**
```bash
python --version
pip --version
python -m venv venv
source venv/bin/activate
pip install requests
```

**Follow-up Interview Questions:**
1. pip কী?
2. কেন virtual environment ব্যবহার করা উচিত?
3. `python -m venv` কেন preferred?

**Code Example:**
```bash
python -m venv venv
source venv/bin/activate
python --version
```

---

## 5. Python Execution Flow

**Definition:**
Python code সাধারণত source code থেকে interpreter দ্বারা line by line execute হয়। Internally CPython source code কে bytecode এ convert করে, তারপর Python Virtual Machine (PVM) সেই bytecode execute করে।

**Real-life Analogy:**
Execution flow কে **translator + worker** এর মতো ভাবতে পারেন। Translator কথা বুঝে নেয়, তারপর worker সেই instruction execute করে।

**Practical Use Case:**
- error কোথায় হচ্ছে তা বুঝতে
- import কেন slow হতে পারে তা জানার জন্য
- script run হওয়ার sequence বুঝতে

**Interview-style Explanation:**
> "Python সাধারণত interpreted language, কিন্তু internally source code প্রথমে bytecode এ compile হয়। তারপর Python Virtual Machine সেই bytecode execute করে। তাই Python সম্পূর্ণ line-by-line পড়ে মনে হলেও internal process একটু বেশি structured।"

**Common Mistakes:**
- Python মানে একেবারে compile হয় না বলা
- bytecode concept ignore করা
- interpreter এবং runtime কে mix করা

**Execution Flow Diagram:**

```text
.py source code
   ↓
Parser
   ↓
Bytecode (.pyc)
   ↓
Python Virtual Machine
   ↓
Output / Error
```

**Follow-up Interview Questions:**
1. Bytecode কী?
2. `.pyc` file কেন তৈরি হয়?
3. Interpreter এবং compiler এর পার্থক্য কী?

**Code Example:**
```python
print("Step 1")
print("Step 2")
```

---

## 6. Variables

**Definition:**
Variable হলো একটি named memory reference, যা data store করার জন্য use হয়। Python-এ variable declare করার জন্য আলাদা keyword লাগে না।

**Real-life Analogy:**
Variable কে **label লাগানো box** হিসেবে ভাবুন। Box-এর ভিতরে value থাকে, আর label দিয়ে আপনি box চেনেন।

**Practical Use Case:**
- user name, age, salary store করা
- API response temporary রাখা
- loop counter রাখা

**Interview-style Explanation:**
> "Python-এ variable dynamically assign হয়। আমরা একই variable name-এ different type-এর value later assign করতে পারি, কারণ Python dynamically typed language।"

**Common Mistakes:**
- meaningful variable name না দেওয়া
- reserved keyword ব্যবহার করা
- uppercase/lowercase mismatch ভুলে যাওয়া
- type change unexpectedly হয় বলে confused হওয়া

**Variable Naming Rules:**
- শুরুতে letter বা underscore ব্যবহার করুন
- number দিয়ে শুরু করবেন না
- space ব্যবহার করবেন না
- meaningful নাম দিন: `user_age`, `total_price`

**Follow-up Interview Questions:**
1. Variable এবং constant-এর পার্থক্য কী?
2. Python-এ variable declaration কীভাবে হয়?
3. Dynamic typing কীভাবে কাজ করে?

**Code Example:**
```python
user_name = "Karim"
user_age = 26
is_active = True
print(user_name, user_age, is_active)
```

---

## 7. Data Types

**Definition:**
Data type হলো value-এর category। Python-এ common data types হলো `int`, `float`, `str`, `bool`, `list`, `tuple`, `set`, `dict`, এবং `None`।

**Real-life Analogy:**
Data type কে **different storage container** হিসেবে ভাবুন। দুধ রাখার container আর চাল রাখার container এক না — তেমনি text, number, and collection আলাদা type এ রাখি।

**Practical Use Case:**
- price, quantity → `int` / `float`
- name, address → `str`
- yes/no flag → `bool`
- multiple items → `list`
- unique items → `set`
- structured data → `dict`

**Interview-style Explanation:**
> "Python এ built-in data types অনেক, এবং এগুলো data model simplify করে। Interview-এ শুধু নাম বলা যথেষ্ট নয়; কখন কোন type use করবেন সেটাও বলা দরকার।"

**Common Mistakes:**
- `list` এবং `tuple` confuse করা
- `set` কে unordered unique collection না জানা
- `None` কে `0` বা empty string মনে করা

**Comparison Table:**

| Type | Mutable? | Ordered? | Duplicate allowed? |
|---|---|---|---|
| `int` | No | No | No |
| `str` | No | Yes | Yes |
| `list` | Yes | Yes | Yes |
| `tuple` | No | Yes | Yes |
| `set` | Yes | No | No |
| `dict` | Yes | Yes (3.7+) | Keys no, values yes |

**Follow-up Interview Questions:**
1. Mutable আর immutable কী?
2. `list` vs `tuple`?
3. `set` কেন unique?

**Code Example:**
```python
name = "Amina"
age = 23
marks = [80, 90, 95]
profile = {"name": name, "age": age}
print(type(name), type(marks), type(profile))
```

---

## 8. Type Casting

**Definition:**
Type casting হলো এক data type থেকে অন্য type এ conversion করা। এটি explicit বা implicit হতে পারে।

**Real-life Analogy:**
Type casting কে **currency exchange** এর মতো ভাবুন। একই value, কিন্তু different format-এ convert করা হচ্ছে।

**Practical Use Case:**
- form input string থেকে number বানানো
- JSON parse করার পর type conversion
- calculation করার আগে string to int conversion

**Interview-style Explanation:**
> "Python-এ user input সবসময় string আসে, তাই calculation করতে হলে type casting লাগে। Explicit casting আমরা `int()`, `float()`, `str()` দিয়ে করি।"

**Common Mistakes:**
- string number মনে করা
- `int("10.5")` করে error হওয়া
- implicit conversion সবসময় expected মনে করা

**Follow-up Interview Questions:**
1. Explicit এবং implicit casting-এর পার্থক্য কী?
2. `int('10.5')` কেন error দেয়?
3. Python কি সব type automatically convert করে?

**Code Example:**
```python
price = "120"
quantity = "3"

total = int(price) * int(quantity)
print(total)
```

---

## 9. Input/Output

**Definition:**
Input মানে user বা external source থেকে data নেওয়া। Output মানে result display বা return করা। Python-এ `input()` এবং `print()` খুব common।

**Real-life Analogy:**
Input/output কে **conversation** ভাবুন। User প্রশ্ন করে, system উত্তর দেয়।

**Practical Use Case:**
- CLI tool
- student management script
- automation script
- beginner-level calculation program

**Interview-style Explanation:**
> "Python-এ `input()` দিয়ে user থেকে data নেওয়া হয়, কিন্তু সেটা string হিসেবে আসে। `print()` output দেখাতে use হয়। Production backend এ direct input কম use হলেও scripts এবং automation এ খুব দরকারি।"

**Common Mistakes:**
- `input()` string return করে এটা ভুলে যাওয়া
- formatting না জানা
- multiple values output করার সময় separator ভুল দেওয়া

**Follow-up Interview Questions:**
1. `input()` কী return করে?
2. f-string কেন useful?
3. `print()` এ `end` parameter কী?

**Code Example:**
```python
name = input("Your name: ")
age = int(input("Your age: "))
print(f"Hello {name}, next year your age will be {age + 1}")
```

---

## 10. Operators

**Definition:**
Operators data-এর উপর operation করে। Python-এ arithmetic, comparison, logical, assignment, membership, এবং bitwise operators আছে।

**Real-life Analogy:**
Operators হলো **calculator + decision maker** এর মতো। হিসাব করে, compare করে, এবং সিদ্ধান্ত নিতে সাহায্য করে।

**Practical Use Case:**
- salary calculation
- login validation
- filter condition
- bit-level system flag handling

**Interview-style Explanation:**
> "Operators Python-এর basic building block. Interview-এ শুধু symbols মুখস্থ না করে use case explain করতে হবে, যেমন `==` comparison করে, `=` assignment করে, `in` membership check করে।"

**Comparison Table:**

| Category | Example | Use |
|---|---|---|
| Arithmetic | `+ - * / // % **` | math calculation |
| Comparison | `== != > < >= <=` | compare values |
| Logical | `and or not` | combine conditions |
| Assignment | `= += -=` | value assign/update |
| Membership | `in`, `not in` | collection check |
| Identity | `is`, `is not` | same object check |

**Common Mistakes:**
- `=` এবং `==` confuse করা
- `is` কে `==` ভাবা
- `//` and `/` output mismatch না জানা

**Follow-up Interview Questions:**
1. `is` এবং `==` এর পার্থক্য কী?
2. `//` কেন ব্যবহার করি?
3. `and` এবং `&` কি একই?

**Code Example:**
```python
x = 10
y = 3

print(x + y)
print(x // y)
print(x > y and y > 0)
print("a" in "bangladesh")
```

---

## 11. Conditional Statements

**Definition:**
Conditional statement দিয়ে program সিদ্ধান্ত নেয় কোন block run হবে। Python-এ `if`, `elif`, `else` use করা হয়।

**Real-life Analogy:**
Conditional statements কে **traffic signal** এর মতো ভাবুন। condition অনুযায়ী stop, go, or wait।

**Practical Use Case:**
- login success/failure
- discount calculation
- age-based validation
- access control

**Interview-style Explanation:**
> "Conditional statements programকে decision-making capability দেয়। Interview-এ nested condition এড়িয়ে clear logic লিখতে পারা গুরুত্বপূর্ণ।"

**Common Mistakes:**
- indentation ভুল করা
- unnecessary nested `if` লেখা
- multiple conditions cleanভাবে না লেখা

**Follow-up Interview Questions:**
1. `if` এবং `elif` পার্থক্য কী?
2. Nested `if` কখন দরকার?
3. Truthy এবং falsy value কী?

**Code Example:**
```python
score = 72

if score >= 80:
    print("A+")
elif score >= 70:
    print("A")
else:
    print("Need improvement")
```

---

## 12. Loops

**Definition:**
Loop হলো repeat করার mechanism। Python-এ `for` এবং `while` loop আছে।

**Real-life Analogy:**
Loop কে **assembly line** ভাবুন। একই কাজ বারবার করতে হয়, তাই machine step repeat করে।

**Practical Use Case:**
- list এর প্রতিটি item process করা
- search operation
- retry logic
- batch processing

**Interview-style Explanation:**
> "`for` loop নির্দিষ্ট collection বা range-এর উপর চলে, আর `while` loop condition true থাকা পর্যন্ত চলে। Interview-এ break, continue, এবং loop-else জানা দরকার।"

**Common Mistakes:**
- infinite loop বানিয়ে ফেলা
- `range()` ভুল use করা
- `break` এবং `continue` confusion

**Follow-up Interview Questions:**
1. `for` এবং `while` পার্থক্য কী?
2. `break` কী করে?
3. `continue` কী করে?

**Code Example:**
```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)

count = 1
while count <= 3:
    print("Count:", count)
    count += 1
```

---

## 13. Functions

**Definition:**
Function হলো reusable code block, যা নির্দিষ্ট কাজ করে। এতে code organized হয় এবং duplication কমে।

**Real-life Analogy:**
Function কে **machine button** হিসেবে ভাবুন। একটি button চাপলে নির্দিষ্ট কাজ হয়।

**Practical Use Case:**
- calculation reuse
- validation logic
- formatting
- API helper logic

**Interview-style Explanation:**
> "Function reusable, testable, এবং maintainable code লেখার ভিত্তি। আমি একই logic বারবার না লিখে function বানাই, কারণ এতে bug কমে এবং readability বাড়ে।"

**Common Mistakes:**
- too many responsibilities এক function এ রাখা
- return vs print confusion
- default value না বোঝা

**Follow-up Interview Questions:**
1. Function এবং method-এর পার্থক্য কী?
2. `return` না দিলে কী হয়?
3. Pure function কী?

**Code Example:**
```python
def add_numbers(a, b):
    return a + b

result = add_numbers(10, 20)
print(result)
```

---

## 14. Arguments & Parameters

**Definition:**
Parameters হলো function definition-এর variable। Arguments হলো function call করার সময় দেয়া actual value।

**Real-life Analogy:**
Parameters কে **empty slots** এবং arguments কে **actual items** হিসেবে ভাবুন।

**Practical Use Case:**
- reusable functions design
- flexible APIs
- multiple data handle করা

**Interview-style Explanation:**
> "Parameter function-এর signature-এ থাকে, argument call-time এ pass হয়। Python-এ positional, keyword, default, variable-length arguments—সবই common interview topic।"

**Types Table:**

| Type | Example | Use |
|---|---|---|
| Positional | `add(2, 3)` | order matters |
| Keyword | `add(a=2, b=3)` | readable call |
| Default | `greet(name="Rahim")` | fallback value |
| `*args` | multiple positional args | tuple হিসাবে collect |
| `**kwargs` | multiple keyword args | dict হিসাবে collect |

**Common Mistakes:**
- positional order ভুল করা
- mutable default argument bug
- `*args` আর `**kwargs` order ভুল রাখা

**Follow-up Interview Questions:**
1. `*args` কী return করে?
2. `**kwargs` কী return করে?
3. Mutable default argument problem কী?

**Code Example:**
```python
def introduce(name, age=25, *skills, **info):
    print(name, age)
    print(skills)
    print(info)

introduce("Amina", 24, "Python", "FastAPI", city="Dhaka")
```

---

## 15. Lambda Functions

**Definition:**
Lambda function হলো ছোট anonymous function। এক line এ simple logic লিখতে use করা হয়।

**Real-life Analogy:**
Lambda কে **one-time shortcut** হিসেবে ভাবুন। বড় machine না বানিয়ে quick task handle করা।

**Practical Use Case:**
- sorting key
- quick map/filter operation
- ছোট callback function

**Interview-style Explanation:**
> "Lambda function তখনই use করি যখন function খুব ছোট এবং একবারের জন্য দরকার। Complex logic-এর জন্য named function better।"

**Common Mistakes:**
- lambda দিয়ে long logic লেখা
- readability sacrifice করা
- nested lambda misuse করা

**Follow-up Interview Questions:**
1. Lambda function কেন use করি?
2. Lambda এবং def-এর পার্থক্য কী?
3. কোথায় lambda avoid করা উচিত?

**Code Example:**
```python
square = lambda x: x * x
print(square(5))

numbers = [(1, 3), (2, 1), (5, 2)]
numbers.sort(key=lambda item: item[1])
print(numbers)
```

---

## 16. Scope

**Definition:**
Scope হলো variable কোথায় accessible হবে তার boundary। Common scopes: local, global, এবং nonlocal।

**Real-life Analogy:**
Scope কে **office access level** হিসেবে ভাবুন। কিছু data শুধু নিজের room-এ, কিছু পুরো office-এ accessible।

**Practical Use Case:**
- function এর ভিতরের temporary variable
- global configuration
- nested function state sharing

**Interview-style Explanation:**
> "Local variable function-এর ভিতরে থাকে, global variable পুরো file জুড়ে accessible, আর nonlocal nested function-এ outer function variable modify করতে help করে।"

**Common Mistakes:**
- global variable অতিরিক্ত use করা
- scope shadowing না বোঝা
- `nonlocal` এবং `global` confuse করা

**Follow-up Interview Questions:**
1. Local variable কী?
2. `global` keyword কেন লাগে?
3. `nonlocal` কী করে?

**Code Example:**
```python
x = 10

def outer():
    y = 20
    def inner():
        nonlocal y
        y += 5
        print(y)
    inner()
    print(y)

outer()
print(x)
```

---

## 17. Modules & Packages

**Definition:**
Module হলো একটি `.py` file, আর package হলো multiple module-এর collection। Python import system use করে reusability support করে।

**Real-life Analogy:**
Module কে **single book chapter** আর package কে **পুরো বই** হিসেবে ভাবুন। Chapter আলাদা, কিন্তু same subject cover করে।

**Practical Use Case:**
- code organization
- team collaboration
- reuse in multiple projects
- large project structure maintain করা

**Interview-style Explanation:**
> "Module এবং package বড় codebase manage করার মূল tool। Small scripts এ এক file enough, কিন্তু real projects এ logic আলাদা module/package-এ ভাগ করি।"

**Common Mistakes:**
- circular import problem
- same file এ সব code রেখে দেওয়া
- package structure clean না রাখা

**Typical Structure:**
```text
project/
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── services.py
│   └── utils.py
└── tests/
```

**Follow-up Interview Questions:**
1. Module এবং package পার্থক্য কী?
2. `__init__.py` কেন use করা হয়?
3. Circular import কী?

**Code Example:**
```python
# utils.py
def greet(name):
    return f"Hello, {name}"

# main.py
from utils import greet
print(greet("Rahim"))
```

---

## 18. Virtual Environment

**Definition:**
Virtual environment হলো isolated Python environment, যেখানে project-specific dependency install করা হয়। এতে one project-এর package অন্য project-এর সাথে conflict করে না।

**Real-life Analogy:**
Virtual environment কে **separate room** হিসেবে ভাবুন। প্রতিটি room-এ আলাদা বই, আলাদা tools রাখা যায়।

**Practical Use Case:**
- multiple project manage করা
- dependency conflict avoid করা
- reproducible setup তৈরি করা

**Interview-style Explanation:**
> "আমি সব Python project-এ virtual environment use করি। এতে global Python polluted হয় না, dependency version conflict কমে, এবং project share করা সহজ হয়।"

**Common Mistakes:**
- venv activate না করে package install করা
- requirements.txt update না করা
- একই environment এ সব project চালানো

**Steps:**
```bash
python -m venv venv
source venv/bin/activate
pip install fastapi uvicorn
pip freeze > requirements.txt
```

**Follow-up Interview Questions:**
1. Virtual environment কেন দরকার?
2. `venv` এবং `virtualenv` পার্থক্য কী?
3. `requirements.txt` কেন use করি?

**Code Example:**
```bash
python -m venv venv
source venv/bin/activate
pip install requests
pip freeze
```

---

## PART 1 Quick Revision Table

| Topic | Must Remember |
|---|---|
| Python | High-level, interpreted, general-purpose language |
| History | Guido van Rossum, 1991 release |
| Features | Readability, ecosystem, cross-platform |
| Installation | Use `python -m venv` and `pip` properly |
| Execution Flow | Source code → bytecode → PVM |
| Variables | No explicit declaration keyword |
| Data Types | `int`, `str`, `list`, `dict`, `set`, `tuple` |
| Casting | Use `int()`, `float()`, `str()` |
| Input/Output | `input()` returns string, `print()` displays |
| Operators | Know `==`, `=`, `is`, `in`, `//` |
| Conditions | `if / elif / else` with clean indentation |
| Loops | `for`, `while`, `break`, `continue` |
| Functions | Reusable, testable, maintainable |
| Arguments | Positional, keyword, default, `*args`, `**kwargs` |
| Lambda | Use for small one-line logic |
| Scope | local, global, nonlocal |
| Modules | Reuse and organize code |
| Virtual Env | Isolate dependencies per project |

---

## PART 1 Interview Strategy

বাংলাদেশের junior interview-এ সাধারণত এইভাবে প্রশ্ন আসে:
- definition-level question
- difference-based question
- small code writing question
- debugging / mistake identification

**Best answer pattern:**
1. First, simple definition দিন
2. Then, practical use case বলুন
3. তারপর ছোট code example দিন
4. শেষে common mistake mention করুন

এই pattern follow করলে interviewer বুঝবে যে আপনি শুধু theory মুখস্থ করেননি, concept বুঝেছেনও।

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part2"></a>

## 📋 PART 2 সূচিপত্র — Python Data Structures

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [List](#p2-list) | Mutable ordered collection, operations, complexity |
| 2 | [Tuple](#p2-tuple) | Immutable sequence, use cases, named tuple |
| 3 | [Set](#p2-set) | Unique unordered collection, set operations |
| 4 | [Dictionary](#p2-dictionary) | Key-value store, internal hashing |
| 5 | [List Comprehension](#p2-list-comprehension) | Concise list creation, filter, map patterns |
| 6 | [Dictionary Comprehension](#p2-dictionary-comprehension) | Dynamic dict building |
| 7 | [Nested Data Structures](#p2-nested-data-structures) | Nested list/dict patterns, real-world JSON |
| 8 | [String Manipulation](#p2-string-manipulation) | Common string methods, slicing, formatting |
| 9 | [Iterators](#p2-iterators) | `__iter__`, `__next__`, custom iterator |
| 10 | [Generators](#p2-generators) | `yield`, lazy evaluation, memory efficiency |

---

<a id="p2-list"></a>

## 1. List

**Definition:**
List হলো Python-এর একটি ordered, mutable collection। একটি list-এ যেকোনো data type-এর element রাখা যায়, এবং index দিয়ে access করা যায়।

**Real-life Analogy:**
List কে **বাজারের থলে** হিসেবে ভাবুন। থলেতে যেকোনো জিনিস রাখা যায়, order মনে রাখা যায়, এবং নতুন জিনিস যোগ বা বাদও দেওয়া যায়।

**Internal Working:**
Python list internally একটি **dynamic array**। List এর size বাড়ার সাথে সাথে Python automatically নতুন memory allocate করে। যখন capacity পূর্ণ হয়, list প্রায় দ্বিগুণ আকারে নতুন memory নেয় — এটাকে **amortized O(1) append** বলে।

```text
List memory layout:
[ pointer_to_obj_0 | pointer_to_obj_1 | pointer_to_obj_2 | ... ]
```

**Time Complexity:**

| Operation | Complexity |
|---|---|
| `append()` | O(1) amortized |
| `insert(i, x)` | O(n) |
| `pop()` (last) | O(1) |
| `pop(i)` | O(n) |
| `remove(x)` | O(n) |
| `index` access `lst[i]` | O(1) |
| `in` check | O(n) |
| `sort()` | O(n log n) |

**Practical Use Case:**
- student marks রাখা
- API response items
- to-do items
- search results

**Interview-style Explanation:**
> "List হলো Python-এর most versatile data structure। এটি ordered এবং mutable, তাই dynamic collection এর জন্য best। কিন্তু lookup O(n) হওয়ার কারণে যদি key-based access দরকার হয়, তাহলে dictionary use করা উচিত।"

**Common Mistakes:**
- `list.copy()` না করে list assign করলে shallow reference তৈরি হওয়া
- `remove()` duplicate element-এ শুধু first occurrence মুছে দেওয়া
- `sort()` vs `sorted()` confusion — `sort()` in-place, `sorted()` নতুন list return করে

**Follow-up Interview Questions:**
1. `list.append()` এবং `list.extend()` পার্থক্য কী?
2. `list.sort()` এবং `sorted()` পার্থক্য কী?
3. List slicing কীভাবে কাজ করে?
4. Negative index মানে কী?

**Code Example:**
```python
students = ["Rahim", "Karim", "Amina"]
students.append("Sohel")
students.insert(1, "Nadia")
print(students)

# Slicing
print(students[1:3])   # index 1 থেকে 2
print(students[::-1])  # reverse

# Sort
marks = [85, 72, 90, 68]
marks.sort(reverse=True)
print(marks)

# Common trap — shallow copy
a = [1, 2, 3]
b = a          # same object
b.append(4)
print(a)       # [1, 2, 3, 4] — a-ও বদলে গেছে!

c = a.copy()   # independent copy
c.append(5)
print(a)       # [1, 2, 3, 4] — a অপরিবর্তিত
```

---

<a id="p2-tuple"></a>

## 2. Tuple

**Definition:**
Tuple হলো ordered কিন্তু **immutable** collection। একবার তৈরি হলে এর element পরিবর্তন করা যায় না।

**Real-life Analogy:**
Tuple কে **printed certificate** হিসেবে ভাবুন। Certificate-এ যা লেখা আছে তা পরিবর্তন করা যাবে না।

**Internal Working:**
Tuple list-এর চেয়ে **memory efficient** কারণ এটি fixed-size। CPython-এ small tuple cache করে রাখে, তাই frequently same tuple create করলে memory reuse হয়।

**List vs Tuple Comparison:**

| Feature | List | Tuple |
|---|---|---|
| Mutable | Yes | No |
| Memory | More | Less |
| Speed | Slower | Faster |
| Use case | Dynamic collection | Fixed data |
| Hashable | No | Yes (if elements hashable) |

**Practical Use Case:**
- coordinate pair: `(23.7, 90.4)` — unchangeable
- function multiple return values
- dictionary key হিসেবে use করা
- named tuple — readable structured data

**Interview-style Explanation:**
> "Tuple immutable হওয়ার সুবিধা হলো এটি hashable, তাই dictionary key হিসেবে use করা যায়। Multiple return values return করার সময় tuple automatic তৈরি হয়। যদি data constant থাকবে জানি, তাহলে list-এর বদলে tuple use করি।"

**Common Mistakes:**
- single element tuple-এ comma ভুলে যাওয়া: `(5,)` নয় `(5)`
- tuple immutable মানে element-এর object নিজেও immutable ভাবা — list inside tuple modify হতে পারে

**Follow-up Interview Questions:**
1. Tuple কি সবসময় hashable?
2. Tuple-এ mutable object রাখলে কী হয়?
3. `namedtuple` কী এবং কেন useful?

**Code Example:**
```python
# Basic tuple
point = (10, 20)
print(point[0])

# Single element
single = (42,)   # comma দরকার
print(type(single))

# Multiple return
def min_max(numbers):
    return min(numbers), max(numbers)

low, high = min_max([3, 9, 1, 7])
print(low, high)

# Named tuple
from collections import namedtuple
Student = namedtuple("Student", ["name", "age", "grade"])
s = Student("Amina", 22, "A+")
print(s.name, s.grade)

# Tuple inside — mutable element can still change
t = ([1, 2], [3, 4])
t[0].append(99)   # OK — list inside is mutable
print(t)
```

---

<a id="p2-set"></a>

## 3. Set

**Definition:**
Set হলো **unordered, unique** element-এর collection। Duplicate আপনাআপনি বাদ যায়।

**Real-life Analogy:**
Set কে **উপস্থিতি খাতা** হিসেবে ভাবুন। প্রতিটি student-এর নাম একবারই থাকবে, দুইবার থাকবে না।

**Internal Working:**
Set internally **hash table** use করে। এজন্যই lookup O(1) এবং element-গুলো hashable হতে হয়। Internally dict-এর মতো memory layout, কিন্তু শুধু key, কোনো value নেই।

**Time Complexity:**

| Operation | Complexity |
|---|---|
| `add()` | O(1) |
| `remove()` | O(1) |
| `in` check | O(1) |
| Union / Intersection | O(n) |

**Practical Use Case:**
- duplicate remove করা
- membership test (fast)
- intersection/union — common emails, IDs

**Interview-style Explanation:**
> "যখন unique elements দরকার এবং order matter করে না, তখন set use করি। `in` check set-এ O(1), list-এ O(n) — তাই large collection-এ membership test করতে set অনেক fast।"

**Set Operations:**

| Operation | Symbol | Method |
|---|---|---|
| Union | `a \| b` | `a.union(b)` |
| Intersection | `a & b` | `a.intersection(b)` |
| Difference | `a - b` | `a.difference(b)` |
| Symmetric Diff | `a ^ b` | `a.symmetric_difference(b)` |

**Common Mistakes:**
- set এর order expect করা
- mutable object (list) রাখার চেষ্টা করা
- `{}` empty set মনে করা — `{}` আসলে empty dict, `set()` লিখতে হবে

**Follow-up Interview Questions:**
1. `set` আর `frozenset` পার্থক্য কী?
2. Set কেন unordered?
3. Empty set কীভাবে তৈরি করবেন?

**Code Example:**
```python
nums = [1, 2, 2, 3, 3, 4]
unique = set(nums)
print(unique)   # {1, 2, 3, 4}

a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

print(a | b)   # union
print(a & b)   # intersection
print(a - b)   # difference

# Fast membership test
emails = {"rahim@example.com", "karim@example.com"}
print("rahim@example.com" in emails)   # O(1)

# Frozenset — immutable set, can be dict key
fs = frozenset([1, 2, 3])
```

---

<a id="p2-dictionary"></a>

## 4. Dictionary

**Definition:**
Dictionary হলো **key-value** pair-এর collection। Python 3.7+ থেকে dict insertion order মনে রাখে।

**Real-life Analogy:**
Dictionary কে **contact book** হিসেবে ভাবুন। নাম (key) দিয়ে নম্বর (value) খোঁজা যায়।

**Internal Working:**
Dictionary internally **hash table** use করে। Key-কে hash করে একটি slot খোঁজা হয়, তারপর সেখানে value রাখা হয়। এজন্যই key lookup O(1)। **Hash collision** হলে Python open addressing বা linked chaining use করে।

```text
dict["name"] → hash("name") → slot → value
```

**Time Complexity:**

| Operation | Complexity |
|---|---|
| Get by key | O(1) |
| Set by key | O(1) |
| Delete key | O(1) |
| `in` check | O(1) |
| Iteration | O(n) |

**Practical Use Case:**
- user profile store করা
- API response parse করা
- counting frequency
- grouping related data

**Interview-style Explanation:**
> "Dictionary fast key-based lookup এর জন্য best choice। JSON data সরাসরি dict এ map হয়। Interview-এ `.get()`, `.items()`, `.setdefault()`, এবং nested dict access জানা দরকার।"

**Common Mistakes:**
- missing key-এ direct access করলে `KeyError` হওয়া
- `.get()` এর default value না দেওয়া
- dict iterate করার সময় dict modify করা

**Follow-up Interview Questions:**
1. `dict.get()` এবং `dict[key]` পার্থক্য কী?
2. `defaultdict` কখন use করবেন?
3. Dict comprehension কীভাবে কাজ করে?
4. Python dict কি thread-safe?

**Code Example:**
```python
student = {"name": "Rahim", "age": 23, "grade": "A"}

# Safe access
print(student.get("phone", "N/A"))   # KeyError এড়ানো

# Update
student["city"] = "Dhaka"
student.update({"grade": "A+", "gpa": 3.9})

# Iterate
for key, value in student.items():
    print(f"{key}: {value}")

# Frequency counting
sentence = "banana"
freq = {}
for ch in sentence:
    freq[ch] = freq.get(ch, 0) + 1
print(freq)

# defaultdict
from collections import defaultdict
groups = defaultdict(list)
data = [("A", 10), ("B", 20), ("A", 30)]
for k, v in data:
    groups[k].append(v)
print(dict(groups))
```

---

<a id="p2-list-comprehension"></a>

## 5. List Comprehension

**Definition:**
List comprehension হলো Python-এর concise syntax যা দিয়ে এক line-এ নতুন list তৈরি করা যায়। `for` loop এবং optional `if` filter একসাথে use করা যায়।

**Real-life Analogy:**
List comprehension কে **assembly line filter** হিসেবে ভাবুন। একটি conveyor belt থেকে নির্দিষ্ট শর্তের জিনিস বেছে নতুন pile বানাচ্ছেন।

**Syntax:**
```text
[expression for item in iterable if condition]
```

**Practical Use Case:**
- transform করা: marks list থেকে grades list
- filter করা: active users থেকে শুধু admin list
- flatten করা: nested list একটি list এ নামানো

**Interview-style Explanation:**
> "List comprehension readable এবং `map()` + `filter()` এর চেয়ে বেশি Pythonic। কিন্তু complex logic থাকলে regular loop বেশি readable হয়।"

**Common Mistakes:**
- comprehension-এ complex logic ঢোকানো
- deeply nested comprehension — পড়তে অনেক কঠিন হয়
- generator-এর বদলে list comprehension use করা যখন iteration একবারই হবে

**Follow-up Interview Questions:**
1. List comprehension vs `map()` কোনটি faster?
2. `[x for x in range(10) if x % 2 == 0]` — এটি কী করে?
3. Nested list comprehension কীভাবে কাজ করে?

**Code Example:**
```python
# Basic
squares = [x**2 for x in range(1, 6)]
print(squares)

# With condition
evens = [x for x in range(20) if x % 2 == 0]
print(evens)

# Transform strings
names = ["  rahim  ", "  karim  ", "  amina  "]
clean = [n.strip().title() for n in names]
print(clean)

# Nested — flatten 2D list
matrix = [[1, 2], [3, 4], [5, 6]]
flat = [num for row in matrix for num in row]
print(flat)

# Conditional expression inside comprehension
labels = ["pass" if m >= 40 else "fail" for m in [80, 35, 60, 25]]
print(labels)
```

---

<a id="p2-dictionary-comprehension"></a>

## 6. Dictionary Comprehension

**Definition:**
Dictionary comprehension দিয়ে এক line-এ নতুন dictionary তৈরি করা যায়। Syntax list comprehension-এর মতো, কিন্তু `{key: value ...}` format।

**Real-life Analogy:**
Dict comprehension কে **spreadsheet formula** হিসেবে ভাবুন। একটি column থেকে নতুন column বানাচ্ছেন।

**Practical Use Case:**
- list থেকে indexed dict তৈরি
- value transform করা
- filter করে new dict বানানো

**Interview-style Explanation:**
> "Dict comprehension তখন use করি যখন existing data থেকে structured dict বানাতে হয়। zip(), enumerate() এর সাথে মিলিয়ে অনেক powerful।"

**Common Mistakes:**
- key collision — same key twice থাকলে শেষেরটি জেতে
- complex expression দিয়ে readability নষ্ট করা

**Follow-up Interview Questions:**
1. Dict comprehension এবং `dict()` constructor পার্থক্য কী?
2. Duplicate key থাকলে কী হয়?
3. `zip()` দিয়ে dict বানানোর সবচেয়ে clean way কী?

**Code Example:**
```python
# Basic
squares = {x: x**2 for x in range(1, 6)}
print(squares)

# Filter
scores = {"Rahim": 80, "Karim": 35, "Amina": 70}
passed = {name: score for name, score in scores.items() if score >= 40}
print(passed)

# Invert a dict
original = {"a": 1, "b": 2, "c": 3}
inverted = {v: k for k, v in original.items()}
print(inverted)

# Zip two lists
keys = ["name", "age", "city"]
values = ["Rahim", 24, "Dhaka"]
profile = {k: v for k, v in zip(keys, values)}
print(profile)
```

---

<a id="p2-nested-data-structures"></a>

## 7. Nested Data Structures

**Definition:**
Nested data structure মানে একটি data structure-এর ভিতরে আরেকটি। যেমন list of dicts, dict of lists, list of lists।

**Real-life Analogy:**
Nested data কে **office hierarchy** হিসেবে ভাবুন। Company-এর ভিতরে department, department-এর ভিতরে employees।

**Practical Use Case:**
- JSON API response parse করা
- database rows-এর collection
- tree/graph data represent করা
- config file structure

**Interview-style Explanation:**
> "Real-world data প্রায়ই nested। API response আসলে সাধারণত list of dicts আসে। Deep access করতে careful থাকা দরকার — key missing হলে KeyError, index missing হলে IndexError।"

**Common Mistakes:**
- deeply nested access করতে error handling না রাখা
- nested structure modify করার সময় reference vs copy সমস্যা

**Follow-up Interview Questions:**
1. List of dicts কীভাবে sort করবেন?
2. Nested dict-এ safe access কীভাবে করবেন?
3. Deep copy কখন দরকার?

**Code Example:**
```python
# List of dicts — typical API response
students = [
    {"name": "Rahim", "marks": [80, 75, 90]},
    {"name": "Karim", "marks": [60, 55, 70]},
    {"name": "Amina", "marks": [95, 92, 88]},
]

# Access
print(students[0]["name"])
print(students[0]["marks"][1])

# Sort list of dicts by a key
sorted_students = sorted(students, key=lambda s: sum(s["marks"]), reverse=True)
for s in sorted_students:
    print(s["name"], sum(s["marks"]))

# Safe nested access
data = {"user": {"address": {"city": "Dhaka"}}}
city = data.get("user", {}).get("address", {}).get("city", "Unknown")
print(city)

# Deep copy
import copy
original = {"tags": [1, 2, 3]}
deep = copy.deepcopy(original)
deep["tags"].append(99)
print(original["tags"])   # [1, 2, 3] — unchanged
```

---

<a id="p2-string-manipulation"></a>

## 8. String Manipulation

**Definition:**
String হলো immutable character sequence। Python-এ string manipulation অনেক built-in method দিয়ে করা যায়।

**Real-life Analogy:**
String manipulation কে **text editing** হিসেবে ভাবুন। Copy, cut, find, replace, format — সব করা যায়।

**Internal Working:**
Python string immutable হওয়ায় প্রতিবার string modify করলে নতুন object তৈরি হয়। Loop-এ string concatenation করলে O(n²) হয় — সমাধান: `"".join(list)`।

**Practical Use Case:**
- user input clean করা
- email validation
- log parsing
- name formatting

**Key Methods Table:**

| Method | করে কী |
|---|---|
| `strip()` | শুরু ও শেষের whitespace বাদ দেয় |
| `split(sep)` | separator দিয়ে ভাগ করে list বানায় |
| `join(list)` | list join করে string বানায় |
| `replace(old, new)` | সব occurrence replace করে |
| `find(sub)` | index return করে, না পেলে -1 |
| `startswith()` / `endswith()` | prefix/suffix check করে |
| `upper()` / `lower()` | case change করে |
| `title()` | প্রতিটি word capitalize করে |
| `count(sub)` | substring count করে |
| `format()` / f-string | string interpolation |

**Common Mistakes:**
- string concatenation loop-এ করা (O(n²))
- `split()` default whitespace এবং specific separator-এর পার্থক্য না বোঝা
- `find()` আর `index()` পার্থক্য — `find()` না পেলে -1, `index()` exception দেয়

**Follow-up Interview Questions:**
1. String কেন immutable?
2. f-string, `%` formatting, `.format()` কোনটি best?
3. String reverse করার fastest way কী?
4. Palindrome check করতে কোড লিখুন।

**Code Example:**
```python
text = "  Hello Bangladesh  "
print(text.strip())
print(text.strip().lower())

# Split and join
csv = "Rahim,Karim,Amina"
names = csv.split(",")
print(names)
print(" | ".join(names))

# Replace
raw = "Hello World Hello"
print(raw.replace("Hello", "Hi"))

# String formatting
name, age = "Rahim", 24
print(f"My name is {name} and I am {age} years old.")

# Reverse string — slicing
s = "Python"
print(s[::-1])

# Palindrome check
def is_palindrome(s):
    s = s.lower().replace(" ", "")
    return s == s[::-1]

print(is_palindrome("racecar"))   # True
print(is_palindrome("hello"))     # False

# Efficient concatenation
words = ["Python", "is", "great"]
result = " ".join(words)   # O(n), not O(n²)
```

---

<a id="p2-iterators"></a>

## 9. Iterators

**Definition:**
Iterator হলো এমন একটি object যা `__iter__()` এবং `__next__()` method implement করে। এটি একবারে একটি element return করে।

**Real-life Analogy:**
Iterator কে **book এর page turner** হিসেবে ভাবুন। প্রতিবার চাইলে একটি page পাবেন, সব page একসাথে নয়।

**Internal Working:**
```text
Iterable → __iter__() → Iterator object
Iterator → __next__() → next element
                      → StopIteration (শেষ হলে)
```

`for` loop internally `iter()` call করে iterator নেয়, তারপর `next()` call করতে থাকে।

**Practical Use Case:**
- large file line by line read করা
- custom data source থেকে step-by-step data নেওয়া
- lazy evaluation

**Interview-style Explanation:**
> "`for` loop এর নিচে iterator protocol আছে। Custom class-এ `__iter__` এবং `__next__` implement করলে সেটি iterable হয়। Iterator হলো one-time use — exhausted হলে reset করতে হয়।"

**Common Mistakes:**
- iterator-কে iterable মনে করা — iterator এর element শেষ হলে আর পাওয়া যায় না
- large data মেমরিতে রেখে iterate করা — iterator-ই এক্ষেত্রে সঠিক সমাধান

**Follow-up Interview Questions:**
1. Iterable এবং Iterator পার্থক্য কী?
2. `iter()` এবং `next()` কী করে?
3. Custom iterator class কীভাবে বানাবেন?

**Code Example:**
```python
# Built-in iterator
numbers = [10, 20, 30]
it = iter(numbers)
print(next(it))   # 10
print(next(it))   # 20
print(next(it))   # 30
# print(next(it)) → StopIteration

# Custom iterator
class CountDown:
    def __init__(self, start):
        self.current = start

    def __iter__(self):
        return self

    def __next__(self):
        if self.current <= 0:
            raise StopIteration
        val = self.current
        self.current -= 1
        return val

for num in CountDown(5):
    print(num, end=" ")
```

---

<a id="p2-generators"></a>

## 10. Generators

**Definition:**
Generator হলো special function যা `yield` keyword use করে। প্রতিবার `next()` call করলে পরের value return করে — কিন্তু সব value একসাথে memory-তে রাখে না।

**Real-life Analogy:**
Generator কে **ATM machine** হিসেবে ভাবুন। সব টাকা একসাথে বের করে দেয় না, প্রতিবার request করলে পরিমাণমতো দেয়।

**Internal Working:**
Generator function call করলে generator object তৈরি হয়। Function body execute হয় না। `next()` call করলে `yield` পর্যন্ত চলে, value দেয়, এবং state **suspend** করে রাখে। পরের `next()` call সেখান থেকে resume করে।

```text
generator() → generator object (no execution yet)
next(gen)   → run until yield → yield value → suspend
next(gen)   → resume → run until next yield
next(gen)   → StopIteration (function ends)
```

**Memory Comparison:**

| Approach | Memory Use | Use Case |
|---|---|---|
| List `[x for x in range(1_000_000)]` | High (all in RAM) | need random access |
| Generator `(x for x in range(1_000_000))` | Low (one at a time) | sequential iteration |

**Practical Use Case:**
- large file line-by-line read করা
- infinite sequence তৈরি করা
- data pipeline
- paginated API data

**Interview-style Explanation:**
> "Generator দিয়ে memory-efficient lazy iteration করা যায়। যেমন ১০ লাখ rows এর CSV পড়তে হলে, সব row একসাথে memory-তে না রেখে generator দিয়ে one-by-one process করা better।"

**Common Mistakes:**
- generator-কে multiple times iterate করার চেষ্টা করা — generator exhausted হলে আর value দেয় না
- generator expression আর list comprehension syntax confuse করা

**Follow-up Interview Questions:**
1. Generator এবং iterator পার্থক্য কী?
2. `yield` এবং `return` পার্থক্য কী?
3. `yield from` কী করে?
4. Generator expression syntax কী?

**Code Example:**
```python
# Generator function
def count_up(limit):
    n = 1
    while n <= limit:
        yield n
        n += 1

gen = count_up(5)
print(next(gen))   # 1
print(next(gen))   # 2

for val in count_up(5):
    print(val, end=" ")
print()

# Generator expression
gen_expr = (x**2 for x in range(10))
print(sum(gen_expr))   # no big list created

# Real-world: read large file line by line
def read_large_file(path):
    with open(path) as f:
        for line in f:
            yield line.strip()

# Infinite sequence
def infinite_counter(start=0):
    while True:
        yield start
        start += 1

counter = infinite_counter(100)
for _ in range(3):
    print(next(counter))

# yield from
def chain(*iterables):
    for it in iterables:
        yield from it

print(list(chain([1, 2], [3, 4], [5])))
```

---

## PART 2 Quick Revision Table

| Topic | Key Point | Interview Tip |
|---|---|---|
| **List** | Ordered, mutable, dynamic array | `sort()` vs `sorted()`, copy trap |
| **Tuple** | Ordered, immutable, hashable | Single element needs comma: `(x,)` |
| **Set** | Unordered, unique, hash table | `in` check O(1), empty set is `set()` |
| **Dictionary** | Key-value, hash table, O(1) lookup | `.get()` safe access, `defaultdict` |
| **List Comprehension** | Concise loop+filter in one line | Avoid complex nested comprehension |
| **Dict Comprehension** | Dynamic dict building | Duplicate key → last one wins |
| **Nested Structures** | List of dicts, JSON pattern | Use `.get()` for safe deep access |
| **String** | Immutable, rich methods | Loop concat bad → use `join()` |
| **Iterator** | `__iter__` + `__next__` protocol | One-time use, `for` uses internally |
| **Generator** | `yield` based lazy evaluation | Memory efficient, exhaust once |

---

## PART 2 Interview Coding Patterns

**Pattern 1 — Counting frequency:**
```python
from collections import Counter
words = ["apple", "banana", "apple", "cherry", "banana", "apple"]
freq = Counter(words)
print(freq.most_common(2))
```

**Pattern 2 — Group items by key:**
```python
from collections import defaultdict
students = [("Math", "Rahim"), ("Science", "Karim"), ("Math", "Amina")]
groups = defaultdict(list)
for subject, name in students:
    groups[subject].append(name)
print(dict(groups))
```

**Pattern 3 — Remove duplicates preserving order:**
```python
items = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3]
seen = set()
result = [x for x in items if not (x in seen or seen.add(x))]
print(result)
```

**Pattern 4 — Flatten nested list:**
```python
nested = [[1, 2], [3, 4], [5, 6]]
flat = [x for sublist in nested for x in sublist]
print(flat)
```

**Pattern 5 — Find top-N from dict:**
```python
scores = {"Rahim": 85, "Karim": 72, "Amina": 91, "Sohel": 68}
top2 = sorted(scores, key=scores.get, reverse=True)[:2]
print(top2)
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part3"></a>

## 📋 PART 3 সূচিপত্র — Object-Oriented Programming in Python

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [Class & Object](#p3-class-object) | Blueprint ও instance |
| 2 | [Constructor](#p3-constructor) | `__init__`, object initialization |
| 3 | [Destructor](#p3-destructor) | `__del__`, cleanup |
| 4 | [Encapsulation](#p3-encapsulation) | Private, protected, public |
| 5 | [Abstraction](#p3-abstraction) | Hide complexity, ABC module |
| 6 | [Inheritance](#p3-inheritance) | Single, multiple, MRO |
| 7 | [Polymorphism](#p3-polymorphism) | Same interface, different behavior |
| 8 | [Method Overloading](#p3-overloading) | Python approach with default args |
| 9 | [Method Overriding](#p3-overriding) | Child class re-defines parent method |
| 10 | [Abstract Class](#p3-abstract-class) | ABC, `@abstractmethod` |
| 11 | [Magic / Dunder Methods](#p3-dunder) | `__str__`, `__len__`, `__eq__` etc. |
| 12 | [SOLID Principles](#p3-solid) | 5 principles, Python examples |

---

<a id="p3-class-object"></a>

## 1. Class & Object

**Definition:**
**Class** হলো object-এর blueprint বা template। **Object** হলো সেই class-এর একটি instance — actual data সহ।

**Real-life Analogy:**
Class হলো **building plan** (নকশা), Object হলো সেই নকশা অনুযায়ী **তৈরি বাড়ি**। একই plan থেকে অনেক বাড়ি বানানো যায়।

**Practical Use Case:**
- User, Product, Order, Transaction — এসব real-world entity কে class দিয়ে model করা হয়

**Interview-style Explanation:**
> "Class হলো একটি custom data type যা attributes (data) এবং methods (behavior) define করে। Object হলো সেই class-এর একটি specific instance। Python-এ সবকিছুই object — numbers, strings, functions সব।"

**Common Mistakes:**
- class আর object কে একই মনে করা
- `self` কেন দরকার না বোঝা
- class variable আর instance variable confuse করা

**Class Variable vs Instance Variable:**

| | Class Variable | Instance Variable |
|---|---|---|
| Define করা হয় | class body-তে directly | `__init__` এর ভিতরে `self.` দিয়ে |
| Shared? | সব instance share করে | প্রতিটি instance এর নিজস্ব |
| Access | `ClassName.var` বা `self.var` | `self.var` |

**Follow-up Interview Questions:**
1. `self` কী? কেন প্রথম parameter?
2. Class variable আর instance variable পার্থক্য?
3. Python-এ সবকিছু object — মানে কী?

**Code Example:**
```python
class Student:
    school = "BUET"  # class variable — shared

    def __init__(self, name, age):
        self.name = name    # instance variable
        self.age = age

    def introduce(self):
        return f"I am {self.name}, age {self.age}, from {self.school}"

s1 = Student("Rahim", 22)
s2 = Student("Amina", 23)

print(s1.introduce())
print(s2.introduce())

# Class variable change affects all
Student.school = "CUET"
print(s1.school)   # CUET
print(s2.school)   # CUET
```

---

<a id="p3-constructor"></a>

## 2. Constructor

**Definition:**
Constructor হলো `__init__` method যা object তৈরির সময় automatically call হয়। এটি object-এর initial state set করে।

**Real-life Analogy:**
Constructor কে **নতুন employee-এর joining kit** হিসেবে ভাবুন। যোগ দেওয়ার সময়ই ID card, laptop, email — সব দেওয়া হয়।

**Practical Use Case:**
- object initialization
- required attribute validation
- dependency injection

**Interview-style Explanation:**
> "`__init__` Python-এ constructor হিসেবে কাজ করে। এটি automatically execute হয় যখন object তৈরি হয়। Python-এ constructor overloading সরাসরি নেই — default arguments বা `*args` দিয়ে flexible constructor বানানো হয়।"

**Common Mistakes:**
- `__init__` return করার চেষ্টা করা — `None` return করতে হবে, অন্যথায় error
- constructor-এ too much logic রাখা

**Follow-up Interview Questions:**
1. `__init__` এবং `__new__` পার্থক্য কী?
2. Constructor overloading Python-এ কীভাবে করবেন?
3. `__new__` কখন দরকার হয়?

**Code Example:**
```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance
        self.transactions = []

    def deposit(self, amount):
        self.balance += amount
        self.transactions.append(f"+{amount}")

    def __repr__(self):
        return f"BankAccount(owner={self.owner}, balance={self.balance})"

acc = BankAccount("Rahim", 5000)
acc.deposit(1000)
print(acc)
print(acc.transactions)
```

---

<a id="p3-destructor"></a>

## 3. Destructor

**Definition:**
Destructor হলো `__del__` method যা object garbage collected হওয়ার আগে call হয়। Resource cleanup এর জন্য use করা হয়।

**Real-life Analogy:**
Destructor কে **অফিস থেকে বিদায়** হিসেবে ভাবুন। চলে যাওয়ার আগে laptop ফেরত দেওয়া, access card জমা দেওয়া।

**Interview-style Explanation:**
> "Python-এ `__del__` আছে কিন্তু এর উপর নির্ভর করা উচিত নয় কারণ কখন call হবে তা guaranteed না। Resource cleanup এর জন্য `with` statement এবং context manager best practice।"

**Common Mistakes:**
- destructor-এ critical cleanup রাখা — call হওয়ার guarantee নেই
- `del obj` মানে destructor call নয়, reference কমানো

**Follow-up Interview Questions:**
1. `__del__` কি সবসময় call হয়?
2. `del obj` কী করে?
3. Context manager কেন destructor-এর চেয়ে better?

**Code Example:**
```python
class FileHandler:
    def __init__(self, filename):
        self.filename = filename
        print(f"Opening {filename}")

    def __del__(self):
        print(f"Closing {self.filename}")

fh = FileHandler("data.txt")
del fh   # triggers __del__ (usually)
```

---

<a id="p3-encapsulation"></a>

## 4. Encapsulation

**Definition:**
Encapsulation মানে object-এর data এবং method একসাথে bundle করা এবং direct access restrict করা। Python-এ naming convention দিয়ে এটি করা হয়।

**Real-life Analogy:**
Encapsulation কে **ATM machine** হিসেবে ভাবুন। আপনি শুধু card insert করেন, PIN দেন। ভিতরের mechanism দেখেন না বা সরাসরি cash কাউন্ট করতে পারেন না।

**Access Level Conventions:**

| Prefix | Type | Access |
|---|---|---|
| `name` | Public | সবখান থেকে accessible |
| `_name` | Protected | Convention — class ও subclass |
| `__name` | Private | Name mangling — class-এর বাইরে directly accessible নয় |

**Practical Use Case:**
- sensitive data hide করা (password, balance)
- validation enforce করা
- internal implementation change করা externally-visible interface ঠিক রেখে

**Interview-style Explanation:**
> "Python-এ strict private নেই Java-এর মতো। `__` prefix দিলে name mangling হয় — `_ClassName__attr` হিসেবে store হয়। তবে convention হিসেবে `_` protected এবং `__` private ব্যবহার করি।"

**Common Mistakes:**
- `__` prefix মানে সম্পূর্ণ private ভাবা — technically access করা যায় name mangling দিয়ে
- getter/setter না বানিয়ে সরাসরি `__attr` access করার চেষ্টা করা

**Follow-up Interview Questions:**
1. Python-এ private attribute কীভাবে করেন?
2. Name mangling কী?
3. `@property` কেন use করি?

**Code Example:**
```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.__salary = salary   # private

    @property
    def salary(self):
        return self.__salary

    @salary.setter
    def salary(self, amount):
        if amount < 0:
            raise ValueError("Salary cannot be negative")
        self.__salary = amount

    def __repr__(self):
        return f"Employee({self.name}, {self.__salary})"

emp = Employee("Karim", 50000)
print(emp.salary)           # 50000 — via getter
emp.salary = 60000          # via setter
print(emp.salary)

# Name mangling — technically accessible but discouraged
print(emp._Employee__salary)
```

---

<a id="p3-abstraction"></a>

## 5. Abstraction

**Definition:**
Abstraction মানে complex implementation hide করে শুধু necessary interface expose করা। Python-এ `abc` module দিয়ে abstract class তৈরি করা হয়।

**Real-life Analogy:**
Abstraction কে **car driving** এর মতো ভাবুন। আপনি gear shift করেন, accelerator চাপেন — engine-এর ভিতরে কী হচ্ছে জানতে হয় না।

**Practical Use Case:**
- common interface define করা multiple class-এর জন্য
- plugin / strategy pattern
- code contract enforce করা

**Interview-style Explanation:**
> "Abstraction implementation details hide করে। Abstract class define করি যেখানে subclass-গুলো specific method implement করতে বাধ্য থাকে। এটি team-এ coding contract হিসেবে কাজ করে।"

**Common Mistakes:**
- abstract class directly instantiate করার চেষ্টা করা
- abstract method implement না করে subclass বানানো

**Follow-up Interview Questions:**
1. Abstract class আর Interface-এর পার্থক্য?
2. Python-এ interface কীভাবে করবেন?
3. `ABCMeta` কী?

**Code Example:**
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self) -> float:
        pass

    @abstractmethod
    def perimeter(self) -> float:
        pass

    def describe(self):
        return f"Area={self.area():.2f}, Perimeter={self.perimeter():.2f}"

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14159 * self.radius ** 2

    def perimeter(self):
        return 2 * 3.14159 * self.radius

class Rectangle(Shape):
    def __init__(self, w, h):
        self.w, self.h = w, h

    def area(self):
        return self.w * self.h

    def perimeter(self):
        return 2 * (self.w + self.h)

shapes = [Circle(5), Rectangle(4, 6)]
for s in shapes:
    print(s.describe())

# shape = Shape()  → TypeError: Can't instantiate abstract class
```

---

<a id="p3-inheritance"></a>

## 6. Inheritance

**Definition:**
Inheritance মানে একটি class অন্য class-এর attributes ও methods inherit করে। Parent (base) class-এর সব feature child (derived) class পায়।

**Real-life Analogy:**
Inheritance কে **পারিবারিক বৈশিষ্ট্য** হিসেবে ভাবুন। সন্তান বাবার কিছু বৈশিষ্ট্য পায়, প্রয়োজনে নিজস্ব বৈশিষ্ট্যও যোগ করে।

**Types:**

| Type | Example | Python Support |
|---|---|---|
| Single | `class B(A)` | ✅ |
| Multiple | `class C(A, B)` | ✅ |
| Multilevel | `class C(B)` where `B(A)` | ✅ |
| Hierarchical | Multiple child from one parent | ✅ |
| Hybrid | Mix of above | ✅ (MRO handles) |

**MRO (Method Resolution Order):**
Multiple inheritance এ Python **C3 linearization** algorithm use করে। `ClassName.__mro__` দিয়ে দেখা যায়।

**Practical Use Case:**
- User → AdminUser, RegularUser
- Vehicle → Car, Truck, Motorcycle
- BaseModel → UserModel, ProductModel

**Interview-style Explanation:**
> "Inheritance code reuse এর tool। Parent class-এ common logic রাখি, child class-এ specific behavior add করি। Multiple inheritance-এ Python C3 MRO algorithm use করে conflict resolve করে।"

**Common Mistakes:**
- `super()` ভুল জায়গায় call করা
- MRO না বুঝে multiple inheritance করা
- deep inheritance chain তৈরি করা — composition often better

**Follow-up Interview Questions:**
1. `super()` কী করে?
2. MRO কী এবং কীভাবে কাজ করে?
3. Diamond problem কী? Python কীভাবে solve করে?

**Code Example:**
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return f"{self.name} makes a sound"

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

# Multilevel
class GuideDog(Dog):
    def guide(self):
        return f"{self.name} is guiding"

# Multiple inheritance
class Pet:
    def pet_info(self):
        return "I am a pet"

class PetDog(Dog, Pet):
    pass

animals = [Dog("Rex"), Cat("Whiskers"), GuideDog("Buddy")]
for a in animals:
    print(a.speak())

pd = PetDog("Max")
print(pd.speak())
print(pd.pet_info())
print(PetDog.__mro__)

# super()
class Manager(Animal):
    def __init__(self, name, department):
        super().__init__(name)   # parent __init__
        self.department = department
```

---

<a id="p3-polymorphism"></a>

## 7. Polymorphism

**Definition:**
Polymorphism মানে same interface বা method name দিয়ে different behavior। "Many forms" — একই নামের method different class-এ different কাজ করে।

**Real-life Analogy:**
Polymorphism কে **"speak" button** এর মতো ভাবুন। Dog-এ চাপলে "woof", Cat-এ চাপলে "meow", Human-এ চাপলে কথা বলে।

**Types:**

| Type | Description |
|---|---|
| Duck Typing | Object-এর type না দেখে method আছে কিনা দেখা |
| Method Overriding | Child class parent method replace করে |
| Operator Overloading | `+`, `==` etc. custom behavior |

**Interview-style Explanation:**
> "Python-এ polymorphism duck typing দিয়ে আসে। কোনো object-এর type check না করে শুধু দেখি সে নির্দিষ্ট method সাপোর্ট করে কিনা। `if it walks like a duck and quacks like a duck, it's a duck.`"

**Common Mistakes:**
- polymorphism শুধু inheritance মনে করা
- duck typing এর concept না বোঝা

**Follow-up Interview Questions:**
1. Duck typing কী?
2. Compile-time এবং runtime polymorphism পার্থক্য?
3. Python-এ operator overloading কীভাবে করবেন?

**Code Example:**
```python
# Method overriding (runtime polymorphism)
class Shape:
    def area(self):
        return 0

class Circle(Shape):
    def __init__(self, r): self.r = r
    def area(self): return 3.14 * self.r ** 2

class Rectangle(Shape):
    def __init__(self, w, h): self.w, self.h = w, h
    def area(self): return self.w * self.h

shapes = [Circle(5), Rectangle(4, 6)]
for s in shapes:
    print(s.area())   # polymorphic call

# Duck typing
class Dog:
    def sound(self): return "Woof"

class Cat:
    def sound(self): return "Meow"

class Robot:
    def sound(self): return "Beep"

def make_sound(thing):
    print(thing.sound())   # type না জেনেই call

for obj in [Dog(), Cat(), Robot()]:
    make_sound(obj)
```

---

<a id="p3-overloading"></a>

## 8. Method Overloading

**Definition:**
Method overloading মানে same name কিন্তু different parameters দিয়ে multiple method define করা। Python directly support করে না — `default arguments` বা `*args` দিয়ে simulate করা হয়।

**Real-life Analogy:**
একই restaurant-এ "coffee দিন" বললে — আপনি specify করলে black coffee, না করলে default milk coffee দেবে।

**Interview-style Explanation:**
> "Python-এ same name দিয়ে দুটো function লিখলে দ্বিতীয়টি প্রথমটি overwrite করে। Overloading simulate করতে `default arguments`, `*args`, বা `isinstance()` check use করি।"

**Common Mistakes:**
- Java-এর মতো Python-এ দুটো same-name function ভাবা — দ্বিতীয়টি প্রথমটি replace করে
- `functools.singledispatch` না জানা

**Follow-up Interview Questions:**
1. Python কি method overloading support করে?
2. `@singledispatch` কী?
3. Overloading simulate করার best way কী?

**Code Example:**
```python
# Default arguments দিয়ে simulate
class Calculator:
    def add(self, a, b=0, c=0):
        return a + b + c

calc = Calculator()
print(calc.add(5))         # 5
print(calc.add(5, 3))      # 8
print(calc.add(5, 3, 2))   # 10

# functools.singledispatch
from functools import singledispatch

@singledispatch
def process(value):
    raise NotImplementedError(f"Unsupported type: {type(value)}")

@process.register(int)
def _(value):
    return f"Integer: {value * 2}"

@process.register(str)
def _(value):
    return f"String: {value.upper()}"

print(process(10))
print(process("hello"))
```

---

<a id="p3-overriding"></a>

## 9. Method Overriding

**Definition:**
Method overriding হলো child class-এ parent class-এর same-name method নতুনভাবে define করা। Runtime-এ child-এর version call হয়।

**Real-life Analogy:**
Parent বলেন "greeting হলো নমস্কার"। Child বলেন "আমার কাছে greeting হলো সালাম"। একই concept, নিজস্ব implementation।

**Practical Use Case:**
- animal hierarchy-তে `speak()` method
- payment system-এ `process()` method
- serializer-এ `to_json()` method

**Interview-style Explanation:**
> "Method overriding runtime polymorphism-এর মূল mechanism। `super()` call করে parent-এর version চালানো যায়, তারপর extra behavior add করা যায়।"

**Common Mistakes:**
- `super()` call ভুলে যাওয়া — parent initialization skip হওয়া
- overriding করতে গিয়ে parent interface ভাঙা

**Follow-up Interview Questions:**
1. Overloading আর overriding পার্থক্য কী?
2. `super()` কীভাবে কাজ করে?
3. Python-এ runtime method dispatch কীভাবে হয়?

**Code Example:**
```python
class Notification:
    def send(self, message):
        print(f"[Base] Sending: {message}")

class EmailNotification(Notification):
    def send(self, message):
        super().send(message)   # parent call
        print(f"[Email] Emailing: {message}")

class SMSNotification(Notification):
    def send(self, message):
        print(f"[SMS] Texting: {message}")

notifications = [EmailNotification(), SMSNotification()]
for n in notifications:
    n.send("Your OTP is 1234")
    print()
```

---

<a id="p3-abstract-class"></a>

## 10. Abstract Class

**Definition:**
Abstract class হলো এমন class যেটি directly instantiate করা যায় না। এতে abstract method থাকে যেগুলো subclass-কে implement করতে হবে।

**Real-life Analogy:**
Abstract class কে **job description template** হিসেবে ভাবুন। Template বলে কী কী skills দরকার, কিন্তু template নিজে কাজ করে না।

**Practical Use Case:**
- plugin interface define করা
- team-এর common API contract
- framework base class

**Interview-style Explanation:**
> "Abstract class define করলে subclass-গুলো নির্দিষ্ট method implement করতে বাধ্য হয়। এটি compile-time contract-এর Python equivalent। `ABCMeta` বা `ABC` use করি।"

**Common Mistakes:**
- abstract method implement না করলে object তৈরিতে `TypeError` হবে — এটা intended
- concrete method-ও abstract class-এ রাখা যায়, সব method abstract হতে হয় না

**Follow-up Interview Questions:**
1. Abstract class কি instantiate করা যায়?
2. Abstract class এবং interface-এর পার্থক্য?
3. Python-এ interface simulate কীভাবে করবেন?

**Code Example:**
```python
from abc import ABC, abstractmethod

class PaymentGateway(ABC):
    @abstractmethod
    def charge(self, amount: float) -> bool:
        pass

    @abstractmethod
    def refund(self, amount: float) -> bool:
        pass

    def receipt(self, amount):   # concrete method — subclass পাবে
        return f"Receipt for BDT {amount}"

class BkashGateway(PaymentGateway):
    def charge(self, amount):
        print(f"Charging BDT {amount} via bKash")
        return True

    def refund(self, amount):
        print(f"Refunding BDT {amount} via bKash")
        return True

class NagadGateway(PaymentGateway):
    def charge(self, amount):
        print(f"Charging BDT {amount} via Nagad")
        return True

    def refund(self, amount):
        print(f"Refunding BDT {amount} via Nagad")
        return True

gateways = [BkashGateway(), NagadGateway()]
for gw in gateways:
    gw.charge(500)
    print(gw.receipt(500))
```

---

<a id="p3-dunder"></a>

## 11. Magic / Dunder Methods

**Definition:**
Dunder (double underscore) methods হলো Python-এর special methods যা built-in operations override করে। `__init__`, `__str__`, `__len__`, `__eq__`, `__add__` — এগুলো magic methods।

**Real-life Analogy:**
Magic methods কে **universal remote control button** হিসেবে ভাবুন। `+` button চাপলে custom behavior — number হলে যোগ, string হলে concatenation।

**Key Dunder Methods:**

| Method | কখন call হয় |
|---|---|
| `__init__` | Object তৈরির সময় |
| `__str__` | `str(obj)` বা `print(obj)` |
| `__repr__` | `repr(obj)`, debugging |
| `__len__` | `len(obj)` |
| `__eq__` | `obj1 == obj2` |
| `__lt__` | `obj1 < obj2` |
| `__add__` | `obj1 + obj2` |
| `__getitem__` | `obj[key]` |
| `__contains__` | `item in obj` |
| `__iter__` | `for item in obj` |
| `__enter__`/`__exit__` | `with` statement |

**Interview-style Explanation:**
> "Dunder methods Python-এর operator overloading mechanism। Class-এ `__add__` implement করলে `+` operator কাজ করে। `__str__` implement করলে `print()` readable output দেয়।"

**Common Mistakes:**
- `__str__` আর `__repr__` confuse করা — `__repr__` debugging, `__str__` user-facing
- Dunder method directly call করার চেষ্টা — `obj.__str__()` নয়, `str(obj)` ব্যবহার করুন

**Follow-up Interview Questions:**
1. `__str__` এবং `__repr__` পার্থক্য কী?
2. Operator overloading কীভাবে করবেন?
3. `__eq__` implement করলে `__hash__` কেন affect হয়?

**Code Example:**
```python
class Vector:
    def __init__(self, x, y):
        self.x, self.y = x, y

    def __str__(self):
        return f"Vector({self.x}, {self.y})"

    def __repr__(self):
        return f"Vector(x={self.x}, y={self.y})"

    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    def __eq__(self, other):
        return self.x == other.x and self.y == other.y

    def __len__(self):
        return int((self.x**2 + self.y**2) ** 0.5)

v1 = Vector(1, 2)
v2 = Vector(3, 4)

print(v1)           # __str__
print(v1 + v2)      # __add__
print(v1 == v2)     # __eq__
print(len(v2))      # __len__

# Context manager with __enter__/__exit__
class ManagedFile:
    def __init__(self, name):
        self.name = name

    def __enter__(self):
        self.file = open(self.name, "w")
        return self.file

    def __exit__(self, exc_type, exc_val, exc_tb):
        self.file.close()
        return False

with ManagedFile("test.txt") as f:
    f.write("Hello")
```

---

<a id="p3-solid"></a>

## 12. SOLID Principles

**Definition:**
SOLID হলো 5টি OOP design principle যা maintainable, scalable code লেখার guideline দেয়।

| Letter | Principle | মানে |
|---|---|---|
| **S** | Single Responsibility | একটি class-এর একটিই কাজ থাকবে |
| **O** | Open/Closed | Extension-এর জন্য open, modification-এর জন্য closed |
| **L** | Liskov Substitution | Subclass parent-এর জায়গায় use করা যাবে |
| **I** | Interface Segregation | ছোট specific interface বানানো |
| **D** | Dependency Inversion | Abstraction-এর উপর depend করা, concrete-এর নয় |

**Real-life Analogy:**
SOLID হলো **engineering best practices** — যেমন building এ load-bearing wall আলাদা রাখা, electrical wiring আলাদা রাখা।

**Interview-style Explanation:**
> "SOLID principles follow করলে code সহজে test করা যায়, extend করা যায়, এবং team-এ work করা সহজ হয়। Junior developer হিসেবে অন্তত S এবং O ভালোভাবে explain করতে পারা দরকার।"

**S — Single Responsibility:**
```python
# ❌ Bad — একটি class দুটো কাজ করছে
class UserService:
    def get_user(self, uid): ...
    def send_email(self, email): ...   # email পাঠানো এর কাজ না

# ✅ Good
class UserService:
    def get_user(self, uid): ...

class EmailService:
    def send_email(self, email): ...
```

**O — Open/Closed:**
```python
# ✅ Good — new gateway add করতে UserService বদলাতে হবে না
class PaymentGateway(ABC):
    @abstractmethod
    def pay(self, amount): pass

class BkashGateway(PaymentGateway):
    def pay(self, amount): print(f"bKash: {amount}")

class NagadGateway(PaymentGateway):
    def pay(self, amount): print(f"Nagad: {amount}")

def process_payment(gateway: PaymentGateway, amount):
    gateway.pay(amount)
```

**L — Liskov Substitution:**
```python
class Bird:
    def fly(self): return "Flying"

class Sparrow(Bird):
    def fly(self): return "Sparrow flying"

# ✅ Sparrow can replace Bird anywhere
def make_fly(bird: Bird):
    print(bird.fly())

make_fly(Sparrow())
```

**D — Dependency Inversion:**
```python
# ✅ Good — depend on abstraction, not concrete
class Database(ABC):
    @abstractmethod
    def save(self, data): pass

class PostgreSQL(Database):
    def save(self, data): print(f"Saved in PostgreSQL: {data}")

class UserRepo:
    def __init__(self, db: Database):   # injected abstraction
        self.db = db

    def create_user(self, user):
        self.db.save(user)

repo = UserRepo(PostgreSQL())
repo.create_user({"name": "Rahim"})
```

**Common Mistakes:**
- SOLID শুধু theory মুখস্থ করা, code example না দেখানো
- L (Liskov) কে সবচেয়ে কম explain করা
- একটি project-এ সব SOLID apply করার চেষ্টা করা — pragmatic হতে হবে

**Follow-up Interview Questions:**
1. SOLID-এর S কী? Code দিয়ে বোঝান।
2. Open/Closed principle কেন দরকার?
3. Dependency Injection আর Dependency Inversion পার্থক্য কী?

---

## PART 3 Quick Revision Table

| Concept | Key Takeaway | Interview Must-Know |
|---|---|---|
| Class & Object | Blueprint vs instance | class variable vs instance variable |
| Constructor | `__init__` auto-called | `__init__` vs `__new__` |
| Destructor | `__del__` — unreliable | Use context manager instead |
| Encapsulation | `_` protected, `__` private | `@property` for getter/setter |
| Abstraction | ABC + `@abstractmethod` | Can't instantiate abstract class |
| Inheritance | Reuse + extend, MRO | `super()`, Diamond problem |
| Polymorphism | Same interface, different behavior | Duck typing |
| Overloading | Simulate with defaults/`*args` | No native overloading in Python |
| Overriding | Child replaces parent method | `super()` to keep parent logic |
| Abstract Class | Contract for subclasses | `ABC` from `abc` module |
| Dunder Methods | Operator overloading | `__str__` vs `__repr__` |
| SOLID | S, O, L, I, D | S and O most commonly asked |

---

## PART 3 Interview Common Traps

**Trap 1:** "Python-এ method overloading আছে?"
> নেই। Same name দুটো function লিখলে দ্বিতীয়টি প্রথমটি replace করে।

**Trap 2:** "`__del__` দিয়ে file close করা safe?"
> না। `with` statement / context manager use করুন।

**Trap 3:** "Abstract class instantiate করা যায়?"
> না, `TypeError` দেবে।

**Trap 4:** "Encapsulation আর Abstraction একই?"
> না। Encapsulation = data hide করা। Abstraction = complexity hide করা।

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part4"></a>

## 📋 PART 4 সূচিপত্র — Advanced Python

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [Decorators](#p4-decorators) | Function wrapping, `@` syntax, use cases |
| 2 | [Closures](#p4-closures) | Inner function + outer scope, factory pattern |
| 3 | [Generators](#p4-generators-adv) | Advanced generator patterns, `send()`, `yield from` |
| 4 | [Iterators (Custom)](#p4-iterators-adv) | Iterator protocol deep dive |
| 5 | [Context Managers](#p4-context-managers) | `with`, `__enter__`/`__exit__`, `contextlib` |
| 6 | [*args & **kwargs](#p4-args-kwargs) | Flexible function signatures, unpacking |
| 7 | [Deep vs Shallow Copy](#p4-copy) | `copy.copy()` vs `copy.deepcopy()` |
| 8 | [Mutable vs Immutable](#p4-mutable-immutable) | Memory model, gotchas |
| 9 | [Memory Management](#p4-memory) | Reference counting, garbage collection |
| 10 | [GIL](#p4-gil) | Global Interpreter Lock, threading impact |
| 11 | [Multithreading](#p4-threading) | `threading` module, I/O-bound tasks |
| 12 | [Multiprocessing](#p4-multiprocessing) | `multiprocessing` module, CPU-bound tasks |
| 13 | [Asyncio](#p4-asyncio) | async/await, event loop, concurrent I/O |
| 14 | [Type Hinting](#p4-type-hinting) | `typing` module, annotations, `mypy` |

---

<a id="p4-decorators"></a>

## 1. Decorators

**Definition:**
Decorator হলো এমন function যা অন্য function-কে wrap করে extra behavior যোগ করে, original function modify না করে।

**Real-life Analogy:**
Decorator কে **coffee-তে extra toppings** হিসেবে ভাবুন। Plain coffee-তে whipped cream, chocolate add করছেন — coffee-র core recipe বদলাচ্ছেন না।

**Internal Working:**
```text
@my_decorator
def func(): ...

এটি equivalent to:
func = my_decorator(func)
```

**Practical Use Case:**
- logging
- authentication check
- caching / memoization
- execution time measurement
- retry logic

**Interview-style Explanation:**
> "Decorator Python-এর metaprogramming feature। একটি function-কে argument হিসেবে নিয়ে modified version return করে। `@` syntax syntactic sugar। FastAPI, Flask-এর route decorator এই concept-এর উপর built।"

**Common Mistakes:**
- `functools.wraps` না দেওয়া — decorated function-এর `__name__`, `__doc__` হারিয়ে যায়
- decorator vs decorator factory confuse করা

**Follow-up Interview Questions:**
1. Decorator কীভাবে internally কাজ করে?
2. `functools.wraps` কেন দরকার?
3. Decorator stack করলে কী হয়?
4. Class-based decorator কীভাবে বানাবেন?

**Code Example:**
```python
import functools
import time

# Basic decorator
def timer(func):
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        start = time.perf_counter()
        result = func(*args, **kwargs)
        end = time.perf_counter()
        print(f"{func.__name__} took {end-start:.4f}s")
        return result
    return wrapper

@timer
def heavy_task(n):
    return sum(range(n))

print(heavy_task(1_000_000))

# Decorator with arguments (decorator factory)
def repeat(times):
    def decorator(func):
        @functools.wraps(func)
        def wrapper(*args, **kwargs):
            for _ in range(times):
                result = func(*args, **kwargs)
            return result
        return wrapper
    return decorator

@repeat(times=3)
def greet(name):
    print(f"Hello {name}")

greet("Rahim")

# Stacking decorators
def bold(func):
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        return f"**{func(*args, **kwargs)}**"
    return wrapper

def exclaim(func):
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        return f"{func(*args, **kwargs)}!"
    return wrapper

@bold
@exclaim
def say(msg):
    return msg

print(say("Hello"))   # **Hello!**
```

---

<a id="p4-closures"></a>

## 2. Closures

**Definition:**
Closure হলো inner function যা outer function-এর variable মনে রাখে — outer function শেষ হয়ে যাওয়ার পরেও।

**Real-life Analogy:**
Closure কে **backpack** হিসেবে ভাবুন। School শেষ হয়ে গেলেও backpack-এর বইগুলো থেকে যায়।

**Internal Working:**
Python closure `__closure__` attribute এ outer scope variable store করে। এই mechanism-টিকে বলে **free variable capture**।

**Practical Use Case:**
- factory function
- configuration-based function generator
- state সহ lightweight object

**Interview-style Explanation:**
> "Closure তখন তৈরি হয় যখন inner function outer function-এর variable use করে। Decorator-এর foundation এই closure। Class না বানিয়ে state maintain করতে closure elegant solution।"

**Common Mistakes:**
- loop-এ closure তৈরির classic bug — সব closure শেষ value দেখে
- `nonlocal` ছাড়া outer variable modify করার চেষ্টা

**Follow-up Interview Questions:**
1. Closure কীভাবে outer variable মনে রাখে?
2. `nonlocal` কী?
3. Loop-এ closure bug কেন হয়?

**Code Example:**
```python
# Basic closure
def make_multiplier(factor):
    def multiply(x):
        return x * factor   # factor remembered from outer scope
    return multiply

double = make_multiplier(2)
triple = make_multiplier(3)
print(double(5))   # 10
print(triple(5))   # 15

# Inspect closure
print(double.__closure__[0].cell_contents)   # 2

# Loop closure bug and fix
# Bug:
funcs_bug = [lambda: i for i in range(3)]
print([f() for f in funcs_bug])   # [2, 2, 2] — all see last i

# Fix with default argument:
funcs_ok = [lambda i=i: i for i in range(3)]
print([f() for f in funcs_ok])    # [0, 1, 2]

# Counter with nonlocal
def make_counter():
    count = 0
    def increment():
        nonlocal count
        count += 1
        return count
    return increment

counter = make_counter()
print(counter())   # 1
print(counter())   # 2
print(counter())   # 3
```

---

<a id="p4-generators-adv"></a>

## 3. Advanced Generators

**Definition:**
Generator-এর advanced features: `send()`, `throw()`, `close()`, `yield from` এবং generator pipeline।

**Practical Use Case:**
- data pipeline
- coroutine (asyncio-এর predecessor)
- infinite stream processing

**Interview-style Explanation:**
> "`send()` দিয়ে generator-এ value পাঠানো যায়, যা generator কে bidirectional করে। `yield from` দিয়ে sub-generator delegate করা যায়।"

**Code Example:**
```python
# send() — bidirectional generator
def accumulator():
    total = 0
    while True:
        value = yield total
        if value is None:
            break
        total += value

gen = accumulator()
next(gen)          # prime the generator
print(gen.send(10))   # 10
print(gen.send(20))   # 30
print(gen.send(5))    # 35

# Generator pipeline
def integers(start=1):
    while True:
        yield start
        start += 1

def take(n, iterable):
    for i, val in enumerate(iterable):
        if i >= n: break
        yield val

def square(iterable):
    for val in iterable:
        yield val ** 2

pipeline = square(take(5, integers()))
print(list(pipeline))   # [1, 4, 9, 16, 25]
```

---

<a id="p4-context-managers"></a>

## 4. Context Managers

**Definition:**
Context manager `with` statement-এর সাথে কাজ করে। `__enter__` শুরুতে এবং `__exit__` শেষে (error হলেও) call হয়।

**Real-life Analogy:**
Context manager কে **hotel check-in/check-out** হিসেবে ভাবুন। ঢুকলেই room পান, বেরোলে auto-checkout হয়।

**Practical Use Case:**
- file handling
- database transaction
- lock acquire/release
- test setup/teardown

**Interview-style Explanation:**
> "Context manager resource management guarantee করে। File open করলে close করতে ভুলে গেলেও `with` block automatically close করে। Error হলেও `__exit__` call হয়।"

**Code Example:**
```python
# Class-based context manager
class DatabaseConnection:
    def __init__(self, db_name):
        self.db_name = db_name

    def __enter__(self):
        print(f"Connecting to {self.db_name}")
        return self   # 'as' variable পাবে

    def __exit__(self, exc_type, exc_val, exc_tb):
        print(f"Closing connection to {self.db_name}")
        if exc_type:
            print(f"Error occurred: {exc_val}")
        return False   # exception suppress না করা

with DatabaseConnection("users_db") as db:
    print(f"Using {db.db_name}")

# contextlib decorator
from contextlib import contextmanager

@contextmanager
def timer_ctx(label):
    import time
    start = time.perf_counter()
    try:
        yield
    finally:
        elapsed = time.perf_counter() - start
        print(f"{label}: {elapsed:.4f}s")

with timer_ctx("My task"):
    result = sum(range(1_000_000))
    print(result)
```

---

<a id="p4-args-kwargs"></a>

## 5. *args & **kwargs

**Definition:**
`*args` function-এ variable number of positional arguments নেয় (tuple)। `**kwargs` variable number of keyword arguments নেয় (dict)।

**Interview-style Explanation:**
> "`*args` আর `**kwargs` flexible function signature-এর জন্য। Decorator wrapper-এ `*args, **kwargs` use করি যাতে যেকোনো function wrap করা যায়। Unpacking-এ `*list` এবং `**dict` use করি।"

**Common Mistakes:**
- parameter order ভুল: `def f(a, *args, **kwargs)` — এই order mandatory
- `*args` কে list মনে করা — tuple

**Code Example:**
```python
def log(level, *messages, **meta):
    print(f"[{level}]", " ".join(messages))
    for k, v in meta.items():
        print(f"  {k}={v}")

log("INFO", "User", "logged in", user_id=42, ip="192.168.1.1")

# Unpacking
def add(a, b, c):
    return a + b + c

nums = [1, 2, 3]
print(add(*nums))   # unpacking list

config = {"a": 10, "b": 20, "c": 30}
print(add(**config))   # unpacking dict

# Merge dicts
d1 = {"x": 1, "y": 2}
d2 = {"y": 99, "z": 3}
merged = {**d1, **d2}
print(merged)   # {"x": 1, "y": 99, "z": 3}
```

---

<a id="p4-copy"></a>

## 6. Deep Copy vs Shallow Copy

**Definition:**
**Shallow copy** — নতুন object কিন্তু nested objects-এর reference share করে। **Deep copy** — সম্পূর্ণ independent copy, nested objects সহ।

**Real-life Analogy:**
Shallow copy কে **folder shortcut** হিসেবে ভাবুন — folder নতুন, কিন্তু ফাইলগুলো same। Deep copy কে **সম্পূর্ণ নতুন folder** — সব ফাইলও copied।

**Visualization:**
```text
Original:  [ [1,2], [3,4] ]
             ↓       ↓
Shallow:   [ ref1,  ref2  ]   ← নতুন outer list, same inner lists

Deep:      [ [1,2], [3,4] ]   ← সব নতুন
```

**Interview-style Explanation:**
> "Nested mutable objects নিয়ে কাজ করার সময় shallow copy trap-এ পড়া সহজ। Inner list modify করলে original-ও বদলে যায়। Deep copy দরকার হলে `copy.deepcopy()` use করি।"

**Code Example:**
```python
import copy

original = {"name": "Rahim", "scores": [80, 90, 95]}

shallow = copy.copy(original)
deep = copy.deepcopy(original)

# Shallow: nested list shared
shallow["scores"].append(100)
print(original["scores"])   # [80, 90, 95, 100] — affected!

# Deep: completely independent
deep["scores"].append(200)
print(original["scores"])   # [80, 90, 95, 100] — NOT affected
```

---

<a id="p4-mutable-immutable"></a>

## 7. Mutable vs Immutable

**Definition:**
**Mutable** object তৈরির পর বদলানো যায়। **Immutable** object তৈরির পর বদলানো যায় না — নতুন object তৈরি হয়।

**Quick Reference:**

| Immutable | Mutable |
|---|---|
| `int`, `float`, `str` | `list`, `dict`, `set` |
| `tuple`, `bool` | Custom class (usually) |
| `frozenset` | `bytearray` |

**Interview-style Explanation:**
> "Immutability Python-এর memory optimization-এ help করে। Python ছোট integer (-5 থেকে 256) এবং string interning cache করে। Mutable default argument Python-এর classic bug।"

**Common Mistakes:**
- Mutable default argument bug — সব call-এ same object share হয়
- String immutable মানে variable কে নতুন value দেওয়া যাবে না ভাবা

**Code Example:**
```python
# Mutable default argument bug
def add_item(item, lst=[]):   # ❌ খুব common bug
    lst.append(item)
    return lst

print(add_item(1))   # [1]
print(add_item(2))   # [1, 2] — পুরনো list-এ যোগ হয়েছে!

# Fix
def add_item_fixed(item, lst=None):   # ✅
    if lst is None:
        lst = []
    lst.append(item)
    return lst

# Integer caching
a = 100; b = 100
print(a is b)   # True — cached

a = 300; b = 300
print(a is b)   # False (usually) — not cached
```

---

<a id="p4-memory"></a>

## 8. Memory Management

**Definition:**
Python automatic memory management করে **reference counting** এবং **garbage collector** দিয়ে।

**Internal Working:**
- প্রতিটি object-এর একটি **reference count** আছে
- count 0 হলে memory deallocate হয়
- **Cyclic reference** (A → B → A) reference counting দিয়ে clean হয় না — GC (generational garbage collector) এটা handle করে

**Interview-style Explanation:**
> "Python reference counting দিয়ে memory manage করে। `gc` module cyclic reference deal করে। Memory leak সাধারণত circular reference বা global variable accumulation থেকে হয়।"

**Code Example:**
```python
import sys

x = [1, 2, 3]
print(sys.getrefcount(x))   # reference count

# Manual check
import gc
gc.collect()   # force garbage collection

# id() — memory address
a = 10
b = 10
print(id(a) == id(b))   # True — same cached object
```

---

<a id="p4-gil"></a>

## 9. GIL (Global Interpreter Lock)

**Definition:**
GIL হলো CPython-এর একটি mutex lock যা একসাথে মাত্র একটি thread Python bytecode execute করতে দেয়।

**Real-life Analogy:**
GIL কে **একটি office building-এ একটিই chabi** এর মতো ভাবুন। যে chabi ধরবে সে-ই কাজ করতে পারবে।

**Impact:**

| Task Type | GIL Impact |
|---|---|
| I/O-bound (network, file) | Threading কাজ করে — thread wait করার সময় GIL ছাড়ে |
| CPU-bound (computation) | Threading help করে না — multiprocessing ব্যবহার করুন |

**Interview-style Explanation:**
> "GIL থাকার কারণে Python multi-threaded হলেও CPU-bound কাজে true parallelism নেই। তবে I/O-bound task এ threading ভালো কাজ করে কারণ I/O wait করার সময় GIL release হয়।"

**Common Mistakes:**
- সব কাজে threading মনে করা — CPU-bound কাজে multiprocessing দরকার
- GIL মানে threading একদম useless ভাবা

**Follow-up Interview Questions:**
1. GIL কেন আছে?
2. GIL remove করলে কী হবে?
3. CPU-bound কাজে কোনটি ব্যবহার করবেন?

---

<a id="p4-threading"></a>

## 10. Multithreading

**Definition:**
Multithreading দিয়ে একসাথে multiple thread চালানো যায়। Python-এ `threading` module use হয়। GIL-এর কারণে I/O-bound task-এ বেশি useful।

**Practical Use Case:**
- multiple API call একসাথে করা
- file download
- concurrent user request handle করা

**Code Example:**
```python
import threading
import time

def fetch_data(url, results, index):
    time.sleep(1)   # Simulate I/O
    results[index] = f"Data from {url}"

urls = ["url1", "url2", "url3"]
results = [None] * len(urls)
threads = []

for i, url in enumerate(urls):
    t = threading.Thread(target=fetch_data, args=(url, results, i))
    threads.append(t)
    t.start()

for t in threads:
    t.join()

print(results)

# Thread lock for shared resource
counter = 0
lock = threading.Lock()

def increment():
    global counter
    with lock:
        counter += 1

threads = [threading.Thread(target=increment) for _ in range(1000)]
for t in threads: t.start()
for t in threads: t.join()
print(counter)   # 1000
```

---

<a id="p4-multiprocessing"></a>

## 11. Multiprocessing

**Definition:**
Multiprocessing দিয়ে আলাদা OS process চালানো যায় — প্রতিটির নিজস্ব Python interpreter ও memory। CPU-bound কাজে GIL bypass করা যায়।

**Threading vs Multiprocessing:**

| | Threading | Multiprocessing |
|---|---|---|
| Memory | Shared | Separate |
| GIL | Bound | Free |
| Best for | I/O-bound | CPU-bound |
| Overhead | Low | Higher |

**Code Example:**
```python
from multiprocessing import Pool
import time

def cpu_task(n):
    return sum(i * i for i in range(n))

if __name__ == "__main__":
    numbers = [1_000_000] * 4

    # Sequential
    start = time.time()
    results = [cpu_task(n) for n in numbers]
    print(f"Sequential: {time.time()-start:.2f}s")

    # Parallel
    start = time.time()
    with Pool(4) as pool:
        results = pool.map(cpu_task, numbers)
    print(f"Parallel: {time.time()-start:.2f}s")
```

---

<a id="p4-asyncio"></a>

## 12. Asyncio

**Definition:**
`asyncio` Python-এর standard async library। Single thread-এ concurrent I/O করা যায় **event loop** দিয়ে।

**Real-life Analogy:**
Asyncio কে **একজন efficient waiter** হিসেবে ভাবুন। একসাথে ১০ টেবিলের order নেয়, kitchen wait করার সময় অন্য টেবিলে যায়।

**Async vs Threading vs Multiprocessing:**

| | Asyncio | Threading | Multiprocessing |
|---|---|---|---|
| Model | Cooperative | Preemptive | Parallel |
| Best for | I/O-bound | I/O-bound | CPU-bound |
| Overhead | Minimal | Medium | High |
| Python GIL | One thread | GIL-bound | GIL-free |

**Interview-style Explanation:**
> "Asyncio single thread-এ concurrent I/O করতে পারে। `await` দিয়ে coroutine suspend করি, event loop অন্য coroutine চালায়। FastAPI internally asyncio use করে।"

**Code Example:**
```python
import asyncio
import time

async def fetch(url):
    print(f"Fetching {url}...")
    await asyncio.sleep(1)   # Simulate I/O
    return f"Data from {url}"

async def main():
    urls = ["api/users", "api/products", "api/orders"]

    # Sequential
    start = time.time()
    for url in urls:
        await fetch(url)
    print(f"Sequential: {time.time()-start:.2f}s")

    # Concurrent with gather
    start = time.time()
    results = await asyncio.gather(*[fetch(url) for url in urls])
    print(f"Concurrent: {time.time()-start:.2f}s")
    print(results)

asyncio.run(main())
```

---

<a id="p4-type-hinting"></a>

## 13. Type Hinting

**Definition:**
Type hint হলো Python-এর optional annotation যা variable ও function-এর expected type describe করে। Runtime এ enforce হয় না, কিন্তু IDE এবং `mypy` tool check করতে পারে।

**Practical Use Case:**
- codebase readability বাড়ানো
- IDE autocomplete improve করা
- `mypy` static analysis
- FastAPI/Pydantic type validation

**Interview-style Explanation:**
> "Type hints Python কোডকে self-documenting করে। আমি সব function-এ parameter ও return type annotate করি — এতে team-এর অন্য developer দ্রুত বোঝে এবং bug early catch হয়।"

**Common Mistakes:**
- type hint মানে runtime enforcement ভাবা
- `Optional[str]` এবং `str | None` পার্থক্য না জানা

**Code Example:**
```python
from typing import Optional, Union, List, Dict, Tuple

def greet(name: str, age: int = 18) -> str:
    return f"Hello {name}, age {age}"

def get_user(uid: int) -> Optional[Dict[str, str]]:
    if uid == 1:
        return {"name": "Rahim"}
    return None

def process_scores(scores: List[int]) -> Tuple[float, int, int]:
    return sum(scores)/len(scores), min(scores), max(scores)

# Python 3.10+ union syntax
def format_value(value: int | float | str) -> str:
    return str(value)

# TypedDict for structured dicts
from typing import TypedDict

class UserProfile(TypedDict):
    name: str
    age: int
    email: str

def display(user: UserProfile) -> None:
    print(user["name"])
```

---

## PART 4 Quick Revision Table

| Topic | Key Concept | Interview Tip |
|---|---|---|
| **Decorators** | `func = wrapper(func)`, `@` sugar | `functools.wraps` — must use |
| **Closures** | Inner function captures outer vars | Loop closure bug |
| **Generators (adv)** | `send()`, `yield from`, pipeline | Bidirectional with `send()` |
| **Context Managers** | `__enter__`/`__exit__`, cleanup guarantee | `@contextmanager` shortcut |
| **`*args`/`**kwargs`** | tuple / dict collection | Order: positional, `*args`, keyword, `**kwargs` |
| **Copy** | Shallow shares nested refs, deep independent | `copy.deepcopy()` for nested mutable |
| **Mutable/Immutable** | Immutable: int, str, tuple | Mutable default argument bug |
| **Memory** | Reference counting + GC | `sys.getrefcount()`, cyclic refs |
| **GIL** | One thread runs at a time | I/O-bound → threading, CPU-bound → multiprocessing |
| **Threading** | I/O concurrent, shared memory | Use `Lock` for shared resource |
| **Multiprocessing** | CPU parallel, separate memory | `Pool.map()` for batch |
| **Asyncio** | Event loop, cooperative concurrency | `await`, `asyncio.gather()` |
| **Type Hinting** | Optional annotation, IDE/mypy | `Optional`, `List`, `Dict`, `|` syntax |

---

## PART 4 Interview Comparison

**কোন concurrency tool কখন:**
```text
I/O-bound (API calls, DB, file): asyncio > threading
CPU-bound (math, processing):    multiprocessing
Mixed simple cases:               threading (simpler to implement)
```

**Decorator mental model:**
```text
@decorator
def func(): ...

≡ func = decorator(func)
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part5"></a>

## 📋 PART 5 সূচিপত্র — File Handling & Exception Handling

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [File Operations](#p5-file-ops) | open(), modes, pathlib |
| 2 | [Read & Write Files](#p5-read-write) | text, binary, line-by-line |
| 3 | [CSV Handling](#p5-csv) | csv module, DictReader, DictWriter |
| 4 | [JSON Handling](#p5-json) | json module, loads/dumps, file I/O |
| 5 | [Exception Handling](#p5-exceptions) | try/except/else/finally, hierarchy |
| 6 | [Custom Exceptions](#p5-custom-exceptions) | Exception subclass, best practices |
| 7 | [Logging](#p5-logging) | logging module, levels, handlers |
| 8 | [Debugging](#p5-debugging) | pdb, print debug, VS Code tips |

---

<a id="p5-file-ops"></a>

## 1. File Operations

**Definition:**
Python-এ `open()` function দিয়ে file open করা হয়। `with` statement ব্যবহার করলে file automatically close হয় — error হলেও।

**File Open Modes:**

| Mode | মানে |
|---|---|
| `'r'` | Read (default) |
| `'w'` | Write — file না থাকলে তৈরি, থাকলে overwrite |
| `'a'` | Append — শেষে যোগ করা |
| `'x'` | Exclusive create — file থাকলে error |
| `'b'` | Binary mode (combine: `'rb'`, `'wb'`) |
| `'+'` | Read + Write (combine: `'r+'`, `'w+'`) |

**Real-life Analogy:**
File open করা কে **খাতা বের করা** হিসেবে ভাবুন। `'r'` = শুধু পড়া, `'w'` = নতুন পাতায় লেখা, `'a'` = পুরনো লেখার পর যোগ করা।

**Practical Use Case:**
- configuration file read করা
- log file-এ write করা
- report CSV/JSON export করা

**Interview-style Explanation:**
> "File handling-এ সবসময় `with` statement use করি — এটি context manager, নিশ্চিত করে file সঠিকভাবে close হবে। `pathlib.Path` modern Python-এ OS-independent path handling-এর জন্য preferred।"

**Common Mistakes:**
- `with` ছাড়া file open করলে close ভুলে যাওয়া
- binary mode (`'rb'`) ছাড়া binary file read করা
- relative path hardcode করা — `pathlib` use করা উচিত

**Follow-up Interview Questions:**
1. `with` statement ছাড়া file handle করলে কী সমস্যা?
2. `pathlib` কেন `os.path`-এর চেয়ে better?
3. `'w'` আর `'a'` mode পার্থক্য কী?

**Code Example:**
```python
from pathlib import Path

# pathlib — modern approach
base = Path(__file__).parent
data_file = base / "data" / "users.txt"

# Directory তৈরি (exist করলে error নয়)
data_file.parent.mkdir(parents=True, exist_ok=True)

# Write
with open(data_file, "w", encoding="utf-8") as f:
    f.write("Rahim\nAmina\nKarim\n")

# Check existence
print(data_file.exists())
print(data_file.stat().st_size)   # file size bytes

# Append
with open(data_file, "a", encoding="utf-8") as f:
    f.write("Sohel\n")
```

---

<a id="p5-read-write"></a>

## 2. Read & Write Files

**Definition:**
File-এর content তিনভাবে read করা যায়: `read()` (সম্পূর্ণ), `readline()` (এক লাইন), `readlines()` (list of lines)। বড় file-এর জন্য iteration best।

**Practical Use Case:**
- log file parse করা
- large dataset line-by-line process করা
- binary image/audio read করা

**Interview-style Explanation:**
> "বড় file এর জন্য `read()` দিয়ে সব memory-তে load না করে `for line in file` loop দিয়ে lazy read করি। এটি generator-এর মতো কাজ করে — memory efficient।"

**Common Mistakes:**
- encoding না দেওয়া — Windows-এ `cp1252`, Linux-এ `utf-8` default, cross-platform issue
- `readlines()` দিয়ে বড় file পড়া — সব memory-তে load হয়

**Code Example:**
```python
# Write
with open("sample.txt", "w", encoding="utf-8") as f:
    lines = ["Brain Station 23\n", "BJIT Group\n", "Pathao\n", "bKash\n"]
    f.writelines(lines)

# Read all
with open("sample.txt", "r", encoding="utf-8") as f:
    content = f.read()
    print(content)

# Line by line (memory efficient)
with open("sample.txt", "r", encoding="utf-8") as f:
    for line in f:
        print(line.strip())

# Binary read
with open("sample.txt", "rb") as f:
    data = f.read()
    print(data[:10])   # first 10 bytes
```

---

<a id="p5-csv"></a>

## 3. CSV Handling

**Definition:**
Python-এর `csv` module দিয়ে CSV (Comma Separated Values) file read ও write করা যায়। `DictReader`/`DictWriter` column name দিয়ে access করতে দেয়।

**Real-life Analogy:**
CSV কে **Excel spreadsheet** হিসেবে ভাবুন — rows ও columns, কিন্তু plain text format।

**Practical Use Case:**
- employee/student data import-export
- bank transaction report
- e-commerce order list

**Interview-style Explanation:**
> "Data processing project-এ CSV handle করতে `DictReader` use করি — column name দিয়ে access করা যায়, column order নিয়ে চিন্তা নেই। বড় file-এর জন্য `csv.reader` with iteration ভালো।"

**Common Mistakes:**
- encoding issue — UTF-8 BOM থাকলে `encoding='utf-8-sig'` দিতে হবে
- `newline=''` না দেওয়া Windows-এ — extra blank line আসে

**Follow-up Interview Questions:**
1. `csv.reader` আর `DictReader` পার্থক্য কী?
2. CSV-তে comma থাকলে কীভাবে handle করবেন?
3. pandas CSV read করার চেয়ে `csv` module কখন better?

**Code Example:**
```python
import csv

# Write CSV
employees = [
    {"name": "Rahim", "dept": "Engineering", "salary": 80000},
    {"name": "Amina", "dept": "Design", "salary": 75000},
    {"name": "Karim", "dept": "QA", "salary": 70000},
]

with open("employees.csv", "w", newline="", encoding="utf-8") as f:
    writer = csv.DictWriter(f, fieldnames=["name", "dept", "salary"])
    writer.writeheader()
    writer.writerows(employees)

# Read CSV with DictReader
with open("employees.csv", "r", encoding="utf-8") as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(f"{row['name']} — {row['dept']} — BDT {row['salary']}")

# Filter engineering team
with open("employees.csv", "r", encoding="utf-8") as f:
    eng_team = [r for r in csv.DictReader(f) if r["dept"] == "Engineering"]
    print(eng_team)
```

---

<a id="p5-json"></a>

## 4. JSON Handling

**Definition:**
`json` module দিয়ে Python object থেকে JSON string এবং JSON string থেকে Python object convert করা যায়।

**Key Functions:**

| Function | কাজ |
|---|---|
| `json.dumps(obj)` | Python → JSON string |
| `json.loads(string)` | JSON string → Python |
| `json.dump(obj, f)` | Python → JSON file |
| `json.load(f)` | JSON file → Python |

**Real-life Analogy:**
JSON কে **universal language** হিসেবে ভাবুন। Python, JavaScript, Java — সবাই বোঝে। API response সবসময় JSON।

**Practical Use Case:**
- REST API response parse করা
- config file read/write করা
- data সংরক্ষণ করা

**Interview-style Explanation:**
> "`json.dumps()` Python dict কে JSON string-এ convert করে। `indent` parameter দিলে pretty print হয়। `default` parameter দিয়ে non-serializable object handle করা যায় — যেমন `datetime`।"

**Common Mistakes:**
- `datetime` object directly JSON serialize করা — TypeError
- `json.loads()` আর `json.load()` confuse করা — string vs file

**Follow-up Interview Questions:**
1. `json.dumps()` আর `json.dump()` পার্থক্য কী?
2. Non-serializable object (datetime) কীভাবে handle করবেন?
3. JSON-এ circular reference থাকলে কী হয়?

**Code Example:**
```python
import json
from datetime import datetime

# Dict → JSON string
user = {
    "name": "Rahim",
    "age": 25,
    "skills": ["Python", "Django", "PostgreSQL"],
    "active": True,
}

json_str = json.dumps(user, indent=2, ensure_ascii=False)
print(json_str)

# JSON string → Dict
parsed = json.loads(json_str)
print(parsed["skills"])

# File I/O
with open("user.json", "w", encoding="utf-8") as f:
    json.dump(user, f, indent=2, ensure_ascii=False)

with open("user.json", "r", encoding="utf-8") as f:
    data = json.load(f)
    print(data["name"])

# Custom serializer for datetime
def json_serializer(obj):
    if isinstance(obj, datetime):
        return obj.isoformat()
    raise TypeError(f"Not serializable: {type(obj)}")

event = {"title": "Interview", "date": datetime(2026, 5, 12)}
print(json.dumps(event, default=json_serializer))
```

---

<a id="p5-exceptions"></a>

## 5. Exception Handling

**Definition:**
Exception handling হলো runtime error gracefully handle করার mechanism। `try`, `except`, `else`, `finally` block দিয়ে করা হয়।

**Real-life Analogy:**
Exception handling কে **সড়ক দুর্ঘটনার plan** হিসেবে ভাবুন। স্বাভাবিক পথে গেলে ঠিকঠাক পৌঁছাবেন (`else`), দুর্ঘটনা হলে ambulance ডাকবেন (`except`), যাই হোক insurance-এ কল করবেন (`finally`)।

**Exception Hierarchy:**

```text
BaseException
├── SystemExit
├── KeyboardInterrupt
└── Exception
    ├── ValueError
    ├── TypeError
    ├── KeyError
    ├── IndexError
    ├── AttributeError
    ├── FileNotFoundError
    ├── ZeroDivisionError
    ├── OverflowError
    └── ...
```

**try/except/else/finally:**

| Block | কখন চলে |
|---|---|
| `try` | সবসময় |
| `except` | Exception হলে |
| `else` | Exception না হলে |
| `finally` | সবসময় — error হোক বা না হোক |

**Practical Use Case:**
- API call failure handle করা
- file not found gracefully handle করা
- user input validation

**Interview-style Explanation:**
> "`else` block তখন চলে যখন `try` block-এ কোনো exception হয় না — এটি অনেকে জানেন না। `finally` always চলে, এমনকি `return` statement থাকলেও — resource cleanup-এর জন্য perfect।"

**Common Mistakes:**
- bare `except:` use করা — সব exception ধরে ফেলে, debug কঠিন হয়
- exception ignore করা (`except: pass`) — silent failure
- too broad exception ধরা (`except Exception`) — specific type ধরুন

**Follow-up Interview Questions:**
1. `else` block কখন execute হয়?
2. `finally` কি `return` statement-এর পরেও চলে?
3. `raise` আর `raise e` পার্থক্য কী?

**Code Example:**
```python
# Basic exception handling
def divide(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        print("Error: Cannot divide by zero")
        return None
    except TypeError as e:
        print(f"Type error: {e}")
        return None
    else:
        print("Division successful")
        return result
    finally:
        print("divide() called")   # always runs

print(divide(10, 2))
print(divide(10, 0))

# Multiple exceptions
def parse_config(filename):
    try:
        with open(filename, "r") as f:
            import json
            return json.load(f)
    except FileNotFoundError:
        print(f"Config file not found: {filename}")
    except json.JSONDecodeError as e:
        print(f"Invalid JSON: {e}")
    except PermissionError:
        print("No permission to read file")
    return {}

# Re-raise
def process(data):
    try:
        return int(data)
    except ValueError:
        print("Logging the error...")
        raise   # re-raise same exception with traceback preserved
```

---

<a id="p5-custom-exceptions"></a>

## 6. Custom Exceptions

**Definition:**
Custom exception হলো `Exception` (বা subclass) থেকে inherit করা নিজস্ব exception class। Domain-specific error communicate করতে use করা হয়।

**Real-life Analogy:**
Custom exception কে **hospital-এর specific error code** হিসেবে ভাবুন। General "patient problem" না বলে "BloodPressureHighError" বলা — specific ও actionable।

**Best Practices:**
- `Error` suffix দেওয়া: `InsufficientFundsError`, `InvalidUserError`
- error message এবং context data সহ রাখা
- exception hierarchy বানানো বড় project-এর জন্য

**Interview-style Explanation:**
> "Custom exception তৈরি করলে code readable হয়, caller জানতে পারে exactly কী error হয়েছে এবং কীভাবে handle করবে। বড় project-এ base exception hierarchy রাখি — যেমন `AppError` → `ValidationError`, `DatabaseError`।"

**Common Mistakes:**
- `Exception` directly catch করা custom exception-এর জায়গায়
- exception-এ enough context না দেওয়া

**Follow-up Interview Questions:**
1. Custom exception কেন বানাবেন?
2. Exception hierarchy কীভাবে design করবেন?
3. Exception-এ additional data কীভাবে পাঠাবেন?

**Code Example:**
```python
# Domain-specific exception hierarchy
class AppError(Exception):
    """Base exception for this application"""
    pass

class ValidationError(AppError):
    def __init__(self, field, message):
        self.field = field
        super().__init__(f"Validation failed on '{field}': {message}")

class InsufficientFundsError(AppError):
    def __init__(self, balance, amount):
        self.balance = balance
        self.amount = amount
        super().__init__(
            f"Insufficient funds: balance={balance}, requested={amount}"
        )

class UserNotFoundError(AppError):
    def __init__(self, user_id):
        self.user_id = user_id
        super().__init__(f"User not found: id={user_id}")

# Usage
class BankAccount:
    def __init__(self, owner, balance):
        if balance < 0:
            raise ValidationError("balance", "Must be non-negative")
        self.owner = owner
        self.balance = balance

    def withdraw(self, amount):
        if amount > self.balance:
            raise InsufficientFundsError(self.balance, amount)
        self.balance -= amount
        return self.balance

def process_transaction(account, amount):
    try:
        new_balance = account.withdraw(amount)
        print(f"Withdrawn BDT {amount}. New balance: {new_balance}")
    except InsufficientFundsError as e:
        print(f"Transaction failed: {e}")
        print(f"  Balance: {e.balance}, Requested: {e.amount}")
    except ValidationError as e:
        print(f"Validation: {e}")

acc = BankAccount("Rahim", 5000)
process_transaction(acc, 2000)
process_transaction(acc, 10000)
```

---

<a id="p5-logging"></a>

## 7. Logging

**Definition:**
`logging` module দিয়ে application-এর runtime information record করা হয়। `print()` এর professional alternative।

**Log Levels:**

| Level | Value | কখন ব্যবহার |
|---|---|---|
| `DEBUG` | 10 | Detailed debug info |
| `INFO` | 20 | Normal operation info |
| `WARNING` | 30 | Something unexpected (default min level) |
| `ERROR` | 40 | Error occurred, but app continues |
| `CRITICAL` | 50 | Serious error, app may stop |

**Real-life Analogy:**
Logging কে **factory-র CCTV** হিসেবে ভাবুন। সব ঘটনা record হয়, পরে দরকারে দেখা যায়।

**Practical Use Case:**
- production server debugging
- audit trail
- error tracking

**Interview-style Explanation:**
> "`print()` production-এ use করি না। `logging` module দিয়ে level অনুযায়ী filter করা যায়, file-এ লেখা যায়, timestamp আসে। Production-এ `ERROR` level-এর উপর log রাখি, development-এ `DEBUG`।"

**Common Mistakes:**
- `print()` দিয়ে debug করা production code-এ
- root logger configure না করে `logging.basicConfig()` call না করা
- log file-এ sensitive information (password, token) লেখা

**Follow-up Interview Questions:**
1. `print()` আর `logging` পার্থক্য কী?
2. Log level কীভাবে কাজ করে?
3. Multiple module-এ logging কীভাবে করবেন?

**Code Example:**
```python
import logging
from pathlib import Path

# Basic setup
logging.basicConfig(
    level=logging.DEBUG,
    format="%(asctime)s [%(levelname)s] %(name)s: %(message)s",
    datefmt="%Y-%m-%d %H:%M:%S",
)

# Named logger (best practice — module-specific)
logger = logging.getLogger(__name__)

logger.debug("Starting process")
logger.info("User logged in: rahim@example.com")
logger.warning("Disk usage above 80%")
logger.error("Failed to connect to database")
logger.critical("System out of memory")

# File handler
def setup_file_logger(name: str, log_file: str) -> logging.Logger:
    file_logger = logging.getLogger(name)
    file_logger.setLevel(logging.DEBUG)

    fh = logging.FileHandler(log_file, encoding="utf-8")
    fh.setLevel(logging.INFO)

    formatter = logging.Formatter(
        "%(asctime)s [%(levelname)s] %(message)s"
    )
    fh.setFormatter(formatter)
    file_logger.addHandler(fh)
    return file_logger

app_logger = setup_file_logger("app", "app.log")
app_logger.info("Application started")
app_logger.error("Something went wrong")

# Exception logging
def risky():
    try:
        1 / 0
    except ZeroDivisionError:
        logger.exception("Division error occurred")   # includes traceback

risky()
```

---

<a id="p5-debugging"></a>

## 8. Debugging

**Definition:**
Debugging হলো code-এর bug খুঁজে বের করার process। Python-এ `pdb` (Python Debugger), `print()`, logging, এবং IDE debugger use করা হয়।

**Real-life Analogy:**
Debugging কে **গোয়েন্দার তদন্ত** হিসেবে ভাবুন। Clue সংগ্রহ করো, suspect narrow করো, সত্য বের করো।

**Key pdb Commands:**

| Command | কাজ |
|---|---|
| `n` | Next line |
| `s` | Step into function |
| `c` | Continue to next breakpoint |
| `p var` | Print variable value |
| `l` | List code around current line |
| `q` | Quit debugger |
| `b 25` | Set breakpoint at line 25 |
| `h` | Help |

**Practical Use Case:**
- complex logic trace করা
- unexpected value কোথায় থেকে আসছে বের করা
- third-party code debug করা

**Interview-style Explanation:**
> "Production-এ `pdb` নয়, `logging` use করি। Development-এ VS Code debugger সবচেয়ে সুবিধাজনক। `breakpoint()` Python 3.7+ এ built-in — IDE-তে debugger attached থাকলে সেটাই use করে।"

**Common Mistakes:**
- `print()` debug statement production code-এ রেখে দেওয়া
- `pdb.set_trace()` production-এ রেখে দেওয়া — app hang হয়ে যাবে
- debugger use না শিখে শুধু print-এ depend করা

**Follow-up Interview Questions:**
1. `breakpoint()` কী Python 3.7+-এ?
2. `pdb` কীভাবে use করবেন?
3. Production debugging কীভাবে করবেন?

**Code Example:**
```python
# Python 3.7+ built-in breakpoint()
def calculate_discount(price, discount_pct):
    if discount_pct < 0 or discount_pct > 100:
        raise ValueError(f"Invalid discount: {discount_pct}")
    discount = price * discount_pct / 100
    # breakpoint()   # Uncomment to drop into debugger here
    final = price - discount
    return final

# Manual pdb
import pdb

def buggy_function(items):
    total = 0
    for item in items:
        # pdb.set_trace()   # Drop into debugger
        total += item["price"] * item["qty"]
    return total

# Python's built-in assertion
def process_payment(amount):
    assert amount > 0, f"Amount must be positive, got {amount}"
    print(f"Processing BDT {amount}")

# Useful debug helper
import traceback

def safe_execute(func, *args):
    try:
        return func(*args)
    except Exception as e:
        traceback.print_exc()   # full traceback
        return None
```

---

## PART 5 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Know |
|---|---|---|
| File Operations | `with open()` — always | File modes: r, w, a, x, b |
| Read/Write | Line iteration for large files | `encoding='utf-8'` always |
| CSV | `DictReader`/`DictWriter` | `newline=''` on Windows |
| JSON | `dumps`/`loads` (str), `dump`/`load` (file) | Custom serializer for datetime |
| Exception Handling | `try/except/else/finally` | `else` = no exception, `finally` = always |
| Custom Exceptions | Inherit `Exception`, add context | Hierarchy: `AppError` → specific |
| Logging | `logging.getLogger(__name__)` | Levels: DEBUG→INFO→WARNING→ERROR→CRITICAL |
| Debugging | `breakpoint()`, pdb, IDE | Never leave `pdb.set_trace()` in production |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part6"></a>

## 📋 PART 6 সূচিপত্র — Database & Backend Python

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [SQLite with sqlite3](#p6-sqlite) | Built-in DB, CRUD operations |
| 2 | [PostgreSQL with psycopg2](#p6-postgres) | Real DB connection, parameterized queries |
| 3 | [SQLAlchemy ORM](#p6-sqlalchemy) | ORM concept, models, session |
| 4 | [CRUD Operations](#p6-crud) | Create, Read, Update, Delete patterns |
| 5 | [REST API Concepts](#p6-rest) | HTTP methods, status codes, JSON API |
| 6 | [FastAPI Overview](#p6-fastapi) | Async, Pydantic, routing (full handbook link) |
| 7 | [Flask Overview](#p6-flask) | Minimal framework, routing, templates |
| 8 | [Environment Variables](#p6-env) | `.env`, `python-dotenv`, secrets management |

---

<a id="p6-sqlite"></a>

## 1. SQLite with sqlite3

**Definition:**
`sqlite3` Python-এর built-in module। কোনো server লাগে না — single file database। Development ও small project-এর জন্য ideal।

**Real-life Analogy:**
SQLite কে **portable notebook** হিসেবে ভাবুন। সাথে নিয়ে যাওয়া যায়, কোনো server লাগে না।

**Practical Use Case:**
- local app data store করা
- testing এবং prototyping
- mobile app embedded database
- small tool এবং script

**Interview-style Explanation:**
> "SQLite production-এ high concurrency-তে ভালো না, কিন্তু development এবং testing-এ perfect। Parameterized query সবসময় use করি SQL injection prevent করতে।"

**Common Mistakes:**
- SQL string concatenation দিয়ে query বানানো — SQL injection vulnerability
- `commit()` ভুলে যাওয়া — data save হবে না
- connection close না করা

**Follow-up Interview Questions:**
1. Parameterized query কেন ব্যবহার করবেন?
2. SQLite কখন use করবেন, কখন PostgreSQL?
3. `with` statement দিয়ে SQLite transaction কীভাবে করবেন?

**Code Example:**
```python
import sqlite3
from contextlib import contextmanager

DATABASE = "company.db"

@contextmanager
def get_db():
    conn = sqlite3.connect(DATABASE)
    conn.row_factory = sqlite3.Row   # dict-like access
    try:
        yield conn
        conn.commit()
    except Exception:
        conn.rollback()
        raise
    finally:
        conn.close()

# Create table
def create_tables():
    with get_db() as conn:
        conn.execute("""
            CREATE TABLE IF NOT EXISTS employees (
                id INTEGER PRIMARY KEY AUTOINCREMENT,
                name TEXT NOT NULL,
                department TEXT NOT NULL,
                salary REAL NOT NULL,
                created_at DATETIME DEFAULT CURRENT_TIMESTAMP
            )
        """)

# Insert
def add_employee(name: str, dept: str, salary: float):
    with get_db() as conn:
        cursor = conn.execute(
            "INSERT INTO employees (name, department, salary) VALUES (?, ?, ?)",
            (name, dept, salary)   # parameterized — SQL injection safe
        )
        return cursor.lastrowid

# Read
def get_employees(dept: str = None):
    with get_db() as conn:
        if dept:
            rows = conn.execute(
                "SELECT * FROM employees WHERE department = ?", (dept,)
            ).fetchall()
        else:
            rows = conn.execute("SELECT * FROM employees").fetchall()
        return [dict(row) for row in rows]

# Update
def update_salary(emp_id: int, new_salary: float):
    with get_db() as conn:
        conn.execute(
            "UPDATE employees SET salary = ? WHERE id = ?",
            (new_salary, emp_id)
        )

# Delete
def delete_employee(emp_id: int):
    with get_db() as conn:
        conn.execute("DELETE FROM employees WHERE id = ?", (emp_id,))

# Demo
create_tables()
add_employee("Rahim", "Engineering", 80000)
add_employee("Amina", "Design", 75000)
add_employee("Karim", "Engineering", 70000)

print(get_employees())
print(get_employees("Engineering"))
update_salary(1, 90000)
```

---

<a id="p6-postgres"></a>

## 2. PostgreSQL with psycopg2

**Definition:**
`psycopg2` সবচেয়ে popular PostgreSQL adapter for Python। Production-grade application-এ SQLite-এর পরিবর্তে PostgreSQL use করা হয়।

**Real-life Analogy:**
PostgreSQL হলো **professional office building** — security, concurrency, scalability সব আছে। SQLite হলো home office।

**Practical Use Case:**
- production web application database
- concurrent user support
- complex query ও transaction
- bKash, Nagad, Pathao — সব production app-এ PostgreSQL বা MySQL

**Interview-style Explanation:**
> "psycopg2 দিয়ে PostgreSQL connect করি। Real project-এ connection pool (psycopg2.pool বা SQLAlchemy) use করি — প্রতি request-এ নতুন connection তৈরি expensive। Parameterized query SQL injection থেকে রক্ষা করে।"

**Common Mistakes:**
- credentials hardcode করা — environment variable use করুন
- connection pool না করা — প্রতি request-এ new connection expensive
- `%s` placeholder ব্যবহার (psycopg2 style) vs `?` (sqlite3 style) confuse করা

**Follow-up Interview Questions:**
1. Connection pooling কেন দরকার?
2. psycopg2-এ `%s` কেন SQL injection safe?
3. SQLite আর PostgreSQL কখন কোনটি choose করবেন?

**Code Example:**
```python
import os
import psycopg2
from psycopg2.extras import RealDictCursor
from contextlib import contextmanager

# Credentials from environment (never hardcode)
DB_CONFIG = {
    "host": os.environ.get("DB_HOST", "localhost"),
    "port": int(os.environ.get("DB_PORT", 5432)),
    "dbname": os.environ.get("DB_NAME", "myapp"),
    "user": os.environ.get("DB_USER", "postgres"),
    "password": os.environ.get("DB_PASSWORD", ""),
}

@contextmanager
def get_connection():
    conn = psycopg2.connect(**DB_CONFIG)
    try:
        yield conn
        conn.commit()
    except Exception:
        conn.rollback()
        raise
    finally:
        conn.close()

def get_all_users():
    with get_connection() as conn:
        with conn.cursor(cursor_factory=RealDictCursor) as cur:
            cur.execute("SELECT id, name, email FROM users ORDER BY id")
            return cur.fetchall()

def get_user_by_id(user_id: int):
    with get_connection() as conn:
        with conn.cursor(cursor_factory=RealDictCursor) as cur:
            # %s — psycopg2 parameterized placeholder (SQL injection safe)
            cur.execute(
                "SELECT * FROM users WHERE id = %s", (user_id,)
            )
            return cur.fetchone()

def create_user(name: str, email: str) -> int:
    with get_connection() as conn:
        with conn.cursor() as cur:
            cur.execute(
                "INSERT INTO users (name, email) VALUES (%s, %s) RETURNING id",
                (name, email)
            )
            return cur.fetchone()[0]
```

---

<a id="p6-sqlalchemy"></a>

## 3. SQLAlchemy ORM

**Definition:**
SQLAlchemy ORM (Object Relational Mapper) database table-কে Python class হিসেবে represent করে। Raw SQL না লিখে Python object দিয়ে DB operation করা যায়।

**ORM Concept:**

```text
Python Class   ←→   Database Table
Object         ←→   Row
Attribute      ←→   Column
```

**Real-life Analogy:**
ORM কে **translation service** হিসেবে ভাবুন। আপনি Bangla-তে কথা বলেন, translator SQL-এ convert করে database-কে বলে।

**Practical Use Case:**
- FastAPI + SQLAlchemy — standard production stack
- database migration (with Alembic)
- multiple DB backend support (SQLite dev, PostgreSQL prod)

**Interview-style Explanation:**
> "SQLAlchemy দুটো mode-এ কাজ করে: Core (SQL expression) এবং ORM (model class)। FastAPI-তে ORM use করি কারণ Pydantic model এর সাথে easily integrate হয়। Session দিয়ে transaction manage করি।"

**Common Mistakes:**
- N+1 query problem — lazy loading relationship-এ অনেক query হয়
- session management ভুল করা — session close না করা
- `Base.metadata.create_all()` production-এ use করা — Alembic migration use করুন

**Follow-up Interview Questions:**
1. ORM কী? Raw SQL-এর চেয়ে কোনটি ভালো?
2. N+1 query problem কী?
3. SQLAlchemy session কী করে?

**Code Example:**
```python
from sqlalchemy import create_engine, Column, Integer, String, Float, DateTime
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker
from datetime import datetime

# Setup
DATABASE_URL = "sqlite:///./company.db"   # or postgresql://user:pass@host/db
engine = create_engine(DATABASE_URL, echo=False)
SessionLocal = sessionmaker(autocommit=False, autoflush=False, bind=engine)
Base = declarative_base()

# Model
class Employee(Base):
    __tablename__ = "employees"

    id = Column(Integer, primary_key=True, index=True)
    name = Column(String, nullable=False)
    department = Column(String, nullable=False)
    salary = Column(Float, nullable=False)
    created_at = Column(DateTime, default=datetime.utcnow)

    def __repr__(self):
        return f"<Employee {self.name} ({self.department})>"

# Create tables
Base.metadata.create_all(bind=engine)

# Context manager for session
from contextlib import contextmanager

@contextmanager
def get_session():
    session = SessionLocal()
    try:
        yield session
        session.commit()
    except Exception:
        session.rollback()
        raise
    finally:
        session.close()

# CRUD operations
def create_employee(name: str, dept: str, salary: float) -> Employee:
    with get_session() as session:
        emp = Employee(name=name, department=dept, salary=salary)
        session.add(emp)
        session.flush()   # get ID before commit
        session.refresh(emp)
        return emp

def get_employees(dept: str = None):
    with get_session() as session:
        query = session.query(Employee)
        if dept:
            query = query.filter(Employee.department == dept)
        return query.all()

def update_salary(emp_id: int, new_salary: float):
    with get_session() as session:
        emp = session.query(Employee).filter(Employee.id == emp_id).first()
        if emp:
            emp.salary = new_salary

# Demo
create_employee("Rahim", "Engineering", 80000)
create_employee("Amina", "Design", 75000)

employees = get_employees()
for emp in employees:
    print(emp)
```

---

<a id="p6-crud"></a>

## 4. CRUD Operations

**Definition:**
CRUD = **Create**, **Read**, **Update**, **Delete** — database-এর ৪টি মৌলিক operation। প্রতিটি web application-এর core।

**CRUD → HTTP Mapping:**

| Operation | HTTP Method | SQL | URL Pattern |
|---|---|---|---|
| Create | POST | INSERT | `/users` |
| Read (all) | GET | SELECT | `/users` |
| Read (one) | GET | SELECT WHERE | `/users/{id}` |
| Update | PUT/PATCH | UPDATE | `/users/{id}` |
| Delete | DELETE | DELETE | `/users/{id}` |

**Interview-style Explanation:**
> "CRUD pattern সব backend application-এর foundation। REST API design-এ HTTP method এবং URL pattern CRUD-এর সাথে align করা standard practice।"

**Code Example (FastAPI-style CRUD):**
```python
from fastapi import FastAPI, HTTPException
from pydantic import BaseModel
from typing import Optional, List

app = FastAPI()

# In-memory store (real app-এ DB use করবেন)
users_db = {}
next_id = 1

class UserCreate(BaseModel):
    name: str
    email: str

class UserUpdate(BaseModel):
    name: Optional[str] = None
    email: Optional[str] = None

class UserResponse(BaseModel):
    id: int
    name: str
    email: str

# Create
@app.post("/users", response_model=UserResponse, status_code=201)
def create_user(user: UserCreate):
    global next_id
    new_user = {"id": next_id, "name": user.name, "email": user.email}
    users_db[next_id] = new_user
    next_id += 1
    return new_user

# Read all
@app.get("/users", response_model=List[UserResponse])
def get_users():
    return list(users_db.values())

# Read one
@app.get("/users/{user_id}", response_model=UserResponse)
def get_user(user_id: int):
    if user_id not in users_db:
        raise HTTPException(status_code=404, detail="User not found")
    return users_db[user_id]

# Update (PATCH — partial update)
@app.patch("/users/{user_id}", response_model=UserResponse)
def update_user(user_id: int, user: UserUpdate):
    if user_id not in users_db:
        raise HTTPException(status_code=404, detail="User not found")
    stored = users_db[user_id]
    update_data = user.model_dump(exclude_unset=True)
    stored.update(update_data)
    return stored

# Delete
@app.delete("/users/{user_id}", status_code=204)
def delete_user(user_id: int):
    if user_id not in users_db:
        raise HTTPException(status_code=404, detail="User not found")
    del users_db[user_id]
```

---

<a id="p6-rest"></a>

## 5. REST API Concepts

**Definition:**
REST (Representational State Transfer) হলো web API design-এর architectural style। HTTP protocol-এর উপর resource-based communication।

**REST Principles:**

| Principle | মানে |
|---|---|
| Stateless | প্রতিটি request independent — server client state রাখে না |
| Resource-based | URL = noun (resource), Method = verb |
| Uniform Interface | Standard HTTP methods |
| JSON/XML | Standard data format |

**HTTP Methods:**

| Method | কাজ | Idempotent? |
|---|---|---|
| GET | Data read | ✅ |
| POST | Create | ❌ |
| PUT | Full replace | ✅ |
| PATCH | Partial update | ✅ |
| DELETE | Delete | ✅ |

**HTTP Status Codes:**

| Code | মানে |
|---|---|
| 200 OK | Success |
| 201 Created | Resource created |
| 204 No Content | Success, no response body |
| 400 Bad Request | Client-side error |
| 401 Unauthorized | Authentication required |
| 403 Forbidden | Permission denied |
| 404 Not Found | Resource not found |
| 422 Unprocessable | Validation error |
| 500 Internal Error | Server-side error |

**Interview-style Explanation:**
> "REST API design-এ URL কে resource হিসেবে ভাবি — `/users` (collection), `/users/1` (specific user)। HTTP method দিয়ে action বোঝাই। Status code দিয়ে result communicate করি। Idempotent মানে same request বারবার same result দেয়।"

**Common Mistakes:**
- URL-এ verb ব্যবহার: `/getUsers` — ❌, `/users` GET — ✅
- 200 সব response-এ return করা — proper status code দিন
- `POST` এবং `PUT` পার্থক্য না বোঝা

**Follow-up Interview Questions:**
1. REST কী? RESTful API কীভাবে design করবেন?
2. Idempotent মানে কী? কোন methods idempotent?
3. 401 আর 403 পার্থক্য কী?

---

<a id="p6-fastapi"></a>

## 6. FastAPI Overview

**Definition:**
FastAPI হলো modern, fast Python web framework। Async support, automatic OpenAPI docs, Pydantic validation — সব built-in।

**Key Features:**

| Feature | বিবরণ |
|---|---|
| Performance | Uvicorn ASGI — Node.js comparable |
| Validation | Pydantic automatic request/response validation |
| Docs | `/docs` (Swagger) এবং `/redoc` auto-generated |
| Async | `async def` — high concurrency |
| Type Hints | Python type hints থেকে API schema generate |

**Real-life Analogy:**
FastAPI কে **modern office building** হিসেবে ভাবুন — elevator, security, AC সব automatic। Flask হলো basic room — নিজে সব setup করতে হবে।

**Interview-style Explanation:**
> "FastAPI async-first, type hint-driven framework। Request আসলে Pydantic automatically validate করে — invalid data হলে 422 return করে। Background task, dependency injection, OAuth2 — সব built-in।"

> 📚 **বিস্তারিত:** [FastAPI Complete Handbook →](./FastAPI_Junior_Engineer_BD_QA.md) — 12 PART সম্পূর্ণ গাইড

**Quick Code Example:**
```python
from fastapi import FastAPI, Depends, HTTPException, status
from pydantic import BaseModel, EmailStr
from typing import Optional

app = FastAPI(title="Company API", version="1.0.0")

class EmployeeCreate(BaseModel):
    name: str
    email: str
    department: str
    salary: float

class EmployeeResponse(EmployeeCreate):
    id: int

    class Config:
        from_attributes = True

# Dependency injection
def get_current_user(token: str = ""):
    if not token:
        raise HTTPException(
            status_code=status.HTTP_401_UNAUTHORIZED,
            detail="Token required"
        )
    return {"user_id": 1, "role": "admin"}

@app.get("/")
async def root():
    return {"message": "Company API", "status": "healthy"}

@app.post("/employees", response_model=EmployeeResponse, status_code=201)
async def create_employee(
    employee: EmployeeCreate,
    current_user: dict = Depends(get_current_user)
):
    # Save to DB...
    return {**employee.model_dump(), "id": 1}

@app.get("/employees/{emp_id}", response_model=EmployeeResponse)
async def get_employee(emp_id: int):
    # Fetch from DB...
    if emp_id != 1:
        raise HTTPException(status_code=404, detail="Employee not found")
    return {"id": 1, "name": "Rahim", "email": "rahim@company.com",
            "department": "Engineering", "salary": 80000}
```

---

<a id="p6-flask"></a>

## 7. Flask Overview

**Definition:**
Flask হলো lightweight, micro web framework। Core শুধু routing এবং request handling — বাকি সব extension দিয়ে add করতে হয়।

**Flask vs FastAPI:**

| | Flask | FastAPI |
|---|---|---|
| Type | Sync (default) | Async-first |
| Validation | Manual / Flask-Marshmallow | Pydantic (built-in) |
| Docs | Manual setup | Auto-generated |
| Learning curve | Lower | Medium |
| Performance | Good | Excellent |
| Use case | Simple APIs, quick prototyping | Production APIs |

**Interview-style Explanation:**
> "Flask simple project এবং quick prototype-এর জন্য ভালো। FastAPI production-grade API-এর জন্য better — type safety, async, auto-docs। Bangladesh-এ অনেক legacy project Flask-এ আছে, তাই দুটোই জানা দরকার।"

**Code Example:**
```python
from flask import Flask, request, jsonify, abort

app = Flask(__name__)

# In-memory store
employees = {}
next_id = 1

@app.route("/")
def index():
    return jsonify({"message": "Flask API", "status": "running"})

@app.route("/employees", methods=["GET"])
def get_all():
    return jsonify(list(employees.values()))

@app.route("/employees/<int:emp_id>", methods=["GET"])
def get_one(emp_id):
    emp = employees.get(emp_id)
    if not emp:
        abort(404)
    return jsonify(emp)

@app.route("/employees", methods=["POST"])
def create():
    global next_id
    data = request.get_json()
    if not data or "name" not in data:
        abort(400)
    emp = {"id": next_id, **data}
    employees[next_id] = emp
    next_id += 1
    return jsonify(emp), 201

@app.route("/employees/<int:emp_id>", methods=["DELETE"])
def delete(emp_id):
    if emp_id not in employees:
        abort(404)
    del employees[emp_id]
    return "", 204

@app.errorhandler(404)
def not_found(e):
    return jsonify({"error": "Not found"}), 404

if __name__ == "__main__":
    app.run(debug=True, port=8000)
```

---

<a id="p6-env"></a>

## 8. Environment Variables

**Definition:**
Environment variable হলো OS-level variable যেখানে sensitive configuration (API key, DB password, secret key) store করা হয়। Code-এ hardcode করা unsafe।

**Real-life Analogy:**
Environment variable কে **personal diary** এর মতো ভাবুন। Public বইয়ে (code) sensitive তথ্য লেখেন না — diary-তে লেখেন।

**Practical Use Case:**
- Database credentials
- API keys (OpenAI, Stripe, bKash)
- Secret keys
- Feature flags

**Interview-style Explanation:**
> "Production-এ secrets কখনো code-এ hardcode করি না। `.env` file-এ রাখি, `.gitignore`-এ add করি। `python-dotenv` দিয়ে load করি। Environment-based config (dev/staging/prod) আলাদা রাখি।"

**Common Mistakes:**
- `.env` file git-এ commit করা — সবচেয়ে dangerous mistake
- production-এ `DEBUG=True` রাখা
- default insecure value রাখা

**Follow-up Interview Questions:**
1. `.env` file git-এ commit করা উচিত কি?
2. `os.environ.get()` আর `os.environ[]` পার্থক্য?
3. Different environment (dev/prod) config কীভাবে manage করবেন?

**Code Example:**
```python
# .env file (কখনো git-এ push করবেন না)
# DB_HOST=localhost
# DB_PORT=5432
# DB_NAME=myapp
# DB_USER=postgres
# DB_PASSWORD=secret123
# SECRET_KEY=super-secret-key
# DEBUG=False

from dotenv import load_dotenv
import os

load_dotenv()   # .env file থেকে load করে

# Access
DB_HOST = os.environ.get("DB_HOST", "localhost")
DB_PORT = int(os.environ.get("DB_PORT", 5432))
SECRET_KEY = os.environ.get("SECRET_KEY")
DEBUG = os.environ.get("DEBUG", "False").lower() == "true"

if not SECRET_KEY:
    raise RuntimeError("SECRET_KEY environment variable not set!")

# Config class pattern (best practice)
class Settings:
    DB_HOST: str = os.environ.get("DB_HOST", "localhost")
    DB_PORT: int = int(os.environ.get("DB_PORT", 5432))
    DB_NAME: str = os.environ.get("DB_NAME", "myapp")
    DB_USER: str = os.environ.get("DB_USER", "postgres")
    DB_PASSWORD: str = os.environ.get("DB_PASSWORD", "")
    SECRET_KEY: str = os.environ.get("SECRET_KEY", "")
    DEBUG: bool = os.environ.get("DEBUG", "False").lower() == "true"

    @property
    def DATABASE_URL(self) -> str:
        return (
            f"postgresql://{self.DB_USER}:{self.DB_PASSWORD}"
            f"@{self.DB_HOST}:{self.DB_PORT}/{self.DB_NAME}"
        )

settings = Settings()
print(settings.DATABASE_URL)
```

---

## PART 6 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Know |
|---|---|---|
| SQLite | Built-in, no server, dev/test | Parameterized query (`?`) |
| PostgreSQL | Production DB, concurrent | psycopg2, connection pool |
| SQLAlchemy | ORM — class → table mapping | Session management, N+1 problem |
| CRUD | Create/Read/Update/Delete | CRUD → HTTP method mapping |
| REST API | Stateless, resource-based | HTTP methods, status codes |
| FastAPI | Async, Pydantic, auto-docs | `async def`, Depends() |
| Flask | Micro, sync, minimal | `request`, `jsonify`, `abort()` |
| Env Variables | Never hardcode secrets | `.env` + `.gitignore` |

---

## PART 6 Interview Must-Know Comparisons

**SQLite vs PostgreSQL:**
```text
SQLite:      Single file, no server, development/testing/embedded
PostgreSQL:  Server, concurrent, production, complex queries
```

**Flask vs FastAPI:**
```text
Flask:    Synchronous, simple, flexible, mature ecosystem
FastAPI:  Async, type-safe, auto-docs, faster, modern
```

**ORM vs Raw SQL:**
```text
ORM:      Readable, type-safe, DB agnostic, slower complex queries
Raw SQL:  Faster, full control, harder to maintain, DB-specific
```

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part7"></a>

## 📋 PART 7 সূচিপত্র — Python for Automation & Scripting

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [os & sys Module](#p7-os-sys) | File system, environment, path operations |
| 2 | [subprocess Module](#p7-subprocess) | Run shell commands from Python |
| 3 | [shutil Module](#p7-shutil) | File copy, move, delete, archive |
| 4 | [File & Directory Automation](#p7-file-auto) | Auto-organize files, batch rename |
| 5 | [requests Module](#p7-requests) | HTTP GET/POST, API calls, headers |
| 6 | [Web Scraping — BeautifulSoup](#p7-bs4) | Parse HTML, extract data |
| 7 | [Selenium Basics](#p7-selenium) | Browser automation, dynamic content |
| 8 | [Schedule & Cron Jobs](#p7-schedule) | Automate recurring tasks |

---

<a id="p7-os-sys"></a>

## 1. os & sys Module

**Definition:**
`os` module OS-level operations করে — file system, environment variables, path manipulation। `sys` module Python interpreter-এর সাথে interact করে — arguments, path, exit।

**Real-life Analogy:**
`os` হলো **file manager** — folder তৈরি, file সরানো, path জানা। `sys` হলো **Python runtime control panel** — version দেখা, arguments পড়া, program exit করা।

**Key Functions:**

| Module | Function | কাজ |
|---|---|---|
| `os` | `os.getcwd()` | Current working directory |
| `os` | `os.listdir(path)` | Directory contents list |
| `os` | `os.makedirs(path, exist_ok=True)` | Nested directory তৈরি |
| `os` | `os.rename(src, dst)` | Rename/move file |
| `os` | `os.remove(path)` | File delete |
| `os` | `os.environ.get(key)` | Environment variable read |
| `os.path` | `os.path.join(a, b)` | OS-safe path join |
| `os.path` | `os.path.exists(path)` | Path exists check |
| `os.path` | `os.path.splitext(file)` | Extension separate |
| `sys` | `sys.argv` | Command-line arguments list |
| `sys` | `sys.exit(code)` | Program exit |
| `sys` | `sys.path` | Module search paths |
| `sys` | `sys.version` | Python version string |

**Interview-style Explanation:**
> "Automation script-এ `os` এবং `pathlib` দুটোই ব্যবহার করি। `pathlib` modern এবং object-oriented — cross-platform সহজ। `sys.argv` দিয়ে command-line tool বানাই যেখানে user argument pass করতে পারে।"

**Common Mistakes:**
- Windows-এ `\\` backslash hardcode করা — `os.path.join()` বা `pathlib` ব্যবহার করুন
- `os.remove()` দিয়ে directory delete করার চেষ্টা — `shutil.rmtree()` দরকার

**Follow-up Interview Questions:**
1. `os.path` আর `pathlib` পার্থক্য কী?
2. `sys.argv` কী? Script-এ কীভাবে use করবেন?
3. Environment variable কীভাবে read করবেন?

**Code Example:**
```python
import os
import sys
from pathlib import Path

# Current working directory
print(os.getcwd())
print(Path.cwd())   # pathlib equivalent

# Directory listing
for item in Path(".").iterdir():
    print(f"{'DIR' if item.is_dir() else 'FILE'}: {item.name}")

# Create nested directories
Path("output/reports/2026").mkdir(parents=True, exist_ok=True)

# Path operations
file_path = Path("data/users.csv")
print(file_path.stem)        # users
print(file_path.suffix)      # .csv
print(file_path.parent)      # data
print(file_path.absolute())  # absolute path

# Walk directory tree
for root, dirs, files in os.walk("output"):
    for f in files:
        full_path = os.path.join(root, f)
        print(full_path)

# sys.argv — command-line script
# Run: python script.py Rahim 25
if len(sys.argv) >= 3:
    name = sys.argv[1]
    age = sys.argv[2]
    print(f"Hello {name}, age {age}")
else:
    print("Usage: script.py <name> <age>")
    sys.exit(1)   # non-zero exit = error
```

---

<a id="p7-subprocess"></a>

## 2. subprocess Module

**Definition:**
`subprocess` module দিয়ে Python script থেকে shell command, external program চালানো যায়। Output capture করা এবং return code check করা যায়।

**Real-life Analogy:**
Subprocess হলো **Python-এর terminal access** — যেন Python থেকে directly terminal-এ command টাইপ করছেন।

**Practical Use Case:**
- git operations automate করা
- shell script চালানো
- ffmpeg/imagemagick এর মতো tool invoke করা
- system info collect করা

**Interview-style Explanation:**
> "`subprocess.run()` modern এবং recommended। `capture_output=True` দিলে stdout/stderr capture হয়। `check=True` দিলে non-zero exit code-এ exception raise হয়। Security-র জন্য `shell=True` avoid করি — এতে shell injection vulnerable।"

**Common Mistakes:**
- `shell=True` ব্যবহার করা user input দিয়ে — shell injection risk
- old `os.system()` use করা — subprocess prefer করুন
- encoding না দেওয়া — bytes পাওয়া যায়, `text=True` দিন

**Follow-up Interview Questions:**
1. `subprocess.run()` আর `os.system()` পার্থক্য?
2. `shell=True` কেন risky?
3. Command output কীভাবে capture করবেন?

**Code Example:**
```python
import subprocess

# Run command and capture output
result = subprocess.run(
    ["ls", "-la"],
    capture_output=True,
    text=True,           # string output (not bytes)
    check=True           # raise CalledProcessError on failure
)
print(result.stdout)
print("Return code:", result.returncode)

# Git automation
def git_log(n=5):
    result = subprocess.run(
        ["git", "log", f"--oneline", f"-n{n}"],
        capture_output=True,
        text=True,
        cwd="/home/musematrix/Desktop/cs-interview-handbook"
    )
    return result.stdout.strip()

print(git_log())

# Handle errors
try:
    subprocess.run(
        ["nonexistent-command"],
        capture_output=True,
        text=True,
        check=True
    )
except subprocess.CalledProcessError as e:
    print(f"Command failed: {e.returncode}")
    print(e.stderr)
except FileNotFoundError:
    print("Command not found")

# Pipe — like shell pipe
ps = subprocess.run(["ps", "aux"], capture_output=True, text=True)
grep = subprocess.run(
    ["grep", "python"],
    input=ps.stdout,
    capture_output=True,
    text=True
)
print(grep.stdout)
```

---

<a id="p7-shutil"></a>

## 3. shutil Module

**Definition:**
`shutil` (shell utilities) module high-level file operations করে — copy, move, delete, archive। `os` এর চেয়ে বেশি feature।

**Key Functions:**

| Function | কাজ |
|---|---|
| `shutil.copy(src, dst)` | File copy (permissions ছাড়া) |
| `shutil.copy2(src, dst)` | File copy (metadata সহ) |
| `shutil.copytree(src, dst)` | Entire directory copy |
| `shutil.move(src, dst)` | File/directory move/rename |
| `shutil.rmtree(path)` | Directory + contents delete |
| `shutil.make_archive(name, fmt, root)` | zip/tar archive তৈরি |
| `shutil.unpack_archive(file, dest)` | Archive extract |
| `shutil.disk_usage(path)` | Disk usage info |

**Interview-style Explanation:**
> "`shutil.rmtree()` non-empty directory delete করতে পারে। Production-এ delete করার আগে confirm বা backup নেওয়া best practice। `shutil.make_archive()` দিয়ে backup automation করা যায়।"

**Common Mistakes:**
- `shutil.rmtree()` accidentally wrong path-এ call করা — irreversible!
- `shutil.copy()` vs `shutil.copy2()` পার্থক্য না জানা (metadata)

**Code Example:**
```python
import shutil
from pathlib import Path

# Copy file
shutil.copy2("report.csv", "backup/report_backup.csv")

# Copy entire directory
shutil.copytree("src_project", "src_project_backup")

# Move file
shutil.move("old_location/file.txt", "new_location/file.txt")

# Delete directory (careful!)
if Path("temp_dir").exists():
    shutil.rmtree("temp_dir")

# Create zip backup
shutil.make_archive(
    "backup_2026_05_12",   # archive name (no extension)
    "zip",                  # format: zip, tar, gztar
    "output"               # directory to archive
)
# → creates backup_2026_05_12.zip

# Extract
shutil.unpack_archive("backup_2026_05_12.zip", "extracted/")

# Disk usage
usage = shutil.disk_usage("/")
print(f"Total: {usage.total // (1024**3)} GB")
print(f"Used:  {usage.used  // (1024**3)} GB")
print(f"Free:  {usage.free  // (1024**3)} GB")
```

---

<a id="p7-file-auto"></a>

## 4. File & Directory Automation

**Definition:**
File automation হলো repetitive file operation Python দিয়ে automate করা — file organize করা, batch rename, cleanup, report generate করা।

**Real-life Analogy:**
File automation কে **office peon** হিসেবে ভাবুন — প্রতিদিন একই কাজ (file sort, backup) করে, কিন্তু এখন Python সেটা automatically করে।

**Practical Use Case:**
- Download folder organize করা (extension অনুযায়ী)
- পুরনো log file archive করা
- batch image rename করা
- report folder-এ daily backup নেওয়া

**Code Example:**
```python
import shutil
from pathlib import Path
from datetime import datetime

def organize_downloads(download_dir: str):
    """
    File extension অনুযায়ী Downloads folder organize করা।
    .pdf → PDFs/, .jpg/.png → Images/, .csv/.xlsx → Data/ etc.
    """
    folder_map = {
        "Images":    [".jpg", ".jpeg", ".png", ".gif", ".webp", ".svg"],
        "Documents": [".pdf", ".docx", ".doc", ".txt", ".pptx"],
        "Data":      [".csv", ".xlsx", ".xls", ".json", ".xml"],
        "Code":      [".py", ".js", ".html", ".css", ".java", ".cpp"],
        "Archives":  [".zip", ".tar", ".gz", ".rar", ".7z"],
        "Videos":    [".mp4", ".mkv", ".avi", ".mov"],
    }

    # Extension → folder lookup
    ext_to_folder = {}
    for folder, exts in folder_map.items():
        for ext in exts:
            ext_to_folder[ext] = folder

    base = Path(download_dir)
    moved = 0

    for file in base.iterdir():
        if not file.is_file():
            continue
        ext = file.suffix.lower()
        dest_folder = ext_to_folder.get(ext, "Others")
        dest_dir = base / dest_folder
        dest_dir.mkdir(exist_ok=True)

        dest_path = dest_dir / file.name
        # Handle duplicate names
        counter = 1
        while dest_path.exists():
            dest_path = dest_dir / f"{file.stem}_{counter}{file.suffix}"
            counter += 1

        shutil.move(str(file), str(dest_path))
        moved += 1
        print(f"Moved: {file.name} → {dest_folder}/")

    print(f"\nTotal moved: {moved} files")

def daily_backup(source: str, backup_root: str):
    """Daily timestamped backup"""
    today = datetime.now().strftime("%Y-%m-%d")
    archive_name = f"backup_{today}"
    dest = Path(backup_root) / archive_name

    if dest.with_suffix(".zip").exists():
        print(f"Backup already exists: {archive_name}.zip")
        return

    Path(backup_root).mkdir(parents=True, exist_ok=True)
    shutil.make_archive(str(dest), "zip", source)
    print(f"Backup created: {archive_name}.zip")

def clean_old_logs(log_dir: str, days_old: int = 30):
    """30 দিনের পুরনো log file delete করা"""
    import time
    cutoff = time.time() - (days_old * 86400)
    deleted = 0
    for log_file in Path(log_dir).glob("*.log"):
        if log_file.stat().st_mtime < cutoff:
            log_file.unlink()
            deleted += 1
    print(f"Deleted {deleted} old log files")
```

---

<a id="p7-requests"></a>

## 5. requests Module

**Definition:**
`requests` হলো HTTP library for Python। API call, web page download, form submit — সব সহজে করা যায়।

**Real-life Analogy:**
`requests` হলো **Python-এর browser** — URL দিলে response নিয়ে আসে।

**Practical Use Case:**
- REST API consume করা
- external service integration (bKash API, Google Maps API)
- data scraping (static page)
- webhook call করা

**HTTP Methods:**

| Method | Code |
|---|---|
| GET | `requests.get(url)` |
| POST | `requests.post(url, json=data)` |
| PUT | `requests.put(url, json=data)` |
| PATCH | `requests.patch(url, json=data)` |
| DELETE | `requests.delete(url)` |

**Interview-style Explanation:**
> "`requests` synchronous — FastAPI/asyncio project-এ `httpx` (async) better। Error handling করতে `response.raise_for_status()` call করি — 4xx/5xx-এ exception raise হয়। Session object দিয়ে connection reuse এবং persistent headers set করা যায়।"

**Common Mistakes:**
- `response.status_code` check না করে data use করা
- timeout না দেওয়া — network hang হতে পারে
- sensitive data (API key) URL-এ রাখা — headers-এ রাখুন

**Follow-up Interview Questions:**
1. `requests.Session()` কেন use করবেন?
2. `raise_for_status()` কী করে?
3. API key কীভাবে securely pass করবেন?

**Code Example:**
```python
import requests
from requests.exceptions import RequestException, Timeout, HTTPError

BASE_URL = "https://jsonplaceholder.typicode.com"

# GET request
def get_users():
    try:
        response = requests.get(
            f"{BASE_URL}/users",
            timeout=10   # seconds — always set timeout
        )
        response.raise_for_status()   # raises HTTPError on 4xx/5xx
        return response.json()
    except Timeout:
        print("Request timed out")
    except HTTPError as e:
        print(f"HTTP error: {e.response.status_code}")
    except RequestException as e:
        print(f"Request failed: {e}")
    return []

# POST request
def create_post(title: str, body: str, user_id: int):
    payload = {"title": title, "body": body, "userId": user_id}
    response = requests.post(
        f"{BASE_URL}/posts",
        json=payload,          # auto-serializes dict + sets Content-Type
        timeout=10
    )
    response.raise_for_status()
    return response.json()

# Session — persistent headers, connection reuse
def fetch_with_auth(api_key: str, endpoint: str):
    with requests.Session() as session:
        session.headers.update({
            "Authorization": f"Bearer {api_key}",
            "Accept": "application/json",
        })
        session.timeout = 10   # default timeout for all requests

        response = session.get(endpoint)
        response.raise_for_status()
        return response.json()

# Example usage
users = get_users()
for u in users[:3]:
    print(f"{u['id']}: {u['name']} — {u['email']}")

new_post = create_post("Python Tutorial", "Learn Python in Bangla", 1)
print(new_post)
```

---

<a id="p7-bs4"></a>

## 6. Web Scraping — BeautifulSoup

**Definition:**
`BeautifulSoup` HTML/XML parse করে data extract করতে দেয়। `requests` দিয়ে page download করি, `bs4` দিয়ে parse করি।

**Real-life Analogy:**
BeautifulSoup হলো **HTML-এর চিরুনি তল্লাশি** — একটি বড় HTML page থেকে দরকারি তথ্য খুঁজে বের করা।

**Practical Use Case:**
- news headline collect করা
- product price monitor করা
- job listing aggregate করা
- research data collection

**Important:**
> Scraping করার আগে website-এর `robots.txt` এবং Terms of Service দেখুন। Rate limit দিন — server overload করবেন না।

**Interview-style Explanation:**
> "Static page scraping-এ `requests + BeautifulSoup`। Dynamic content (JavaScript render) হলে `Selenium` বা `Playwright` দরকার। `find()` first match, `find_all()` সব match return করে। CSS selector-এ `select()` use করি।"

**Common Mistakes:**
- JavaScript-rendered content BeautifulSoup দিয়ে scrape করার চেষ্টা
- no delay — server IP ban করে দিতে পারে
- HTML structure change হলে scraper break হয়

**Follow-up Interview Questions:**
1. Static এবং dynamic page scraping-এর পার্থক্য?
2. `find()` আর `find_all()` পার্থক্য?
3. `robots.txt` কেন check করবেন?

**Code Example:**
```python
import requests
from bs4 import BeautifulSoup
import time

def scrape_quotes():
    """http://quotes.toscrape.com থেকে quotes scrape"""
    url = "http://quotes.toscrape.com"
    quotes = []

    while url:
        response = requests.get(url, timeout=10)
        response.raise_for_status()
        soup = BeautifulSoup(response.text, "html.parser")

        # Extract quotes
        for quote_div in soup.find_all("div", class_="quote"):
            text = quote_div.find("span", class_="text").get_text(strip=True)
            author = quote_div.find("small", class_="author").get_text(strip=True)
            tags = [t.get_text() for t in quote_div.find_all("a", class_="tag")]
            quotes.append({"text": text, "author": author, "tags": tags})

        # Pagination
        next_btn = soup.find("li", class_="next")
        url = "http://quotes.toscrape.com" + next_btn.find("a")["href"] if next_btn else None

        time.sleep(1)   # polite delay — server-কে চাপ দেবেন না

    return quotes

def extract_table(html_content: str) -> list[dict]:
    """HTML table → list of dicts"""
    soup = BeautifulSoup(html_content, "html.parser")
    table = soup.find("table")
    if not table:
        return []

    headers = [th.get_text(strip=True) for th in table.find_all("th")]
    rows = []
    for tr in table.find("tbody").find_all("tr"):
        cells = [td.get_text(strip=True) for td in tr.find_all("td")]
        if cells:
            rows.append(dict(zip(headers, cells)))
    return rows

# CSS selector approach
def get_all_links(url: str) -> list[str]:
    response = requests.get(url, timeout=10)
    soup = BeautifulSoup(response.text, "html.parser")
    return [
        a["href"] for a in soup.select("a[href]")
        if a["href"].startswith("http")
    ]
```

---

<a id="p7-selenium"></a>

## 7. Selenium Basics

**Definition:**
Selenium browser automate করে — real browser (Chrome/Firefox) control করা যায়। JavaScript-rendered dynamic content scrape করা এবং web UI testing-এ use হয়।

**Real-life Analogy:**
Selenium হলো **robot user** — browser open করে, click করে, form fill করে, result পড়ে।

**Practical Use Case:**
- login-protected site scraping
- JavaScript-rendered content
- automated UI testing (browser-based)
- form submission automation
- screenshot capture

**selenium vs playwright:**

| | Selenium | Playwright |
|---|---|---|
| Speed | Moderate | Faster |
| Async | Limited | Native async |
| Browser | Chrome, Firefox, Edge | Chromium, Firefox, WebKit |
| API | Verbose | Cleaner |
| Use case | Legacy, widespread | Modern projects |

**Interview-style Explanation:**
> "Selenium দিয়ে real browser control করি — dynamic page, JavaScript-rendered content scrape করার সময় দরকার হয়। Modern project-এ `playwright` prefer করি — faster এবং async-friendly। QA automation-এ Selenium widely used।"

**Common Mistakes:**
- hardcoded `time.sleep()` — `WebDriverWait` use করুন
- `driver.quit()` ভুলে যাওয়া — zombie browser process থেকে যায়
- headless mode না দেওয়া production/server-এ

**Follow-up Interview Questions:**
1. Selenium আর BeautifulSoup-এর পার্থক্য কী?
2. `implicitly_wait()` আর `WebDriverWait` পার্থক্য?
3. Headless mode কী? কখন use করবেন?

**Code Example:**
```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.common.exceptions import TimeoutException

def setup_driver(headless: bool = True) -> webdriver.Chrome:
    options = Options()
    if headless:
        options.add_argument("--headless")
    options.add_argument("--no-sandbox")
    options.add_argument("--disable-dev-shm-usage")
    return webdriver.Chrome(options=options)

def scrape_dynamic_page(url: str) -> list[dict]:
    driver = setup_driver(headless=True)
    results = []

    try:
        driver.get(url)

        # Wait for element to appear (up to 10s)
        wait = WebDriverWait(driver, timeout=10)
        wait.until(
            EC.presence_of_element_located((By.CSS_SELECTOR, ".results"))
        )

        # Extract data
        items = driver.find_elements(By.CSS_SELECTOR, ".item")
        for item in items:
            title = item.find_element(By.CSS_SELECTOR, ".title").text
            price = item.find_element(By.CSS_SELECTOR, ".price").text
            results.append({"title": title, "price": price})

    except TimeoutException:
        print("Element not found within timeout")
    finally:
        driver.quit()   # always quit — release browser process

    return results

def fill_form(url: str, name: str, email: str):
    driver = setup_driver(headless=False)
    try:
        driver.get(url)
        wait = WebDriverWait(driver, 10)

        # Fill form
        name_field = wait.until(EC.presence_of_element_located((By.ID, "name")))
        name_field.clear()
        name_field.send_keys(name)

        email_field = driver.find_element(By.ID, "email")
        email_field.send_keys(email)

        submit_btn = driver.find_element(By.CSS_SELECTOR, "button[type='submit']")
        submit_btn.click()

        # Wait for success message
        wait.until(EC.presence_of_element_located((By.CLASS_NAME, "success")))
        print("Form submitted successfully")
    finally:
        driver.quit()
```

---

<a id="p7-schedule"></a>

## 8. Schedule & Cron Jobs

**Definition:**
Recurring task automate করার দুটো approach: Python-এ `schedule` library অথবা OS-level `cron` (Linux/macOS) বা Task Scheduler (Windows)।

**Real-life Analogy:**
Schedule হলো **alarm clock** — নির্দিষ্ট সময়ে নির্দিষ্ট কাজ automatically করে।

**Practical Use Case:**
- daily report generate করা
- hourly data sync করা
- weekly backup নেওয়া
- periodic health check করা

**cron expression:**
```text
* * * * *  command
│ │ │ │ └─ Day of week (0–7, 0=Sun)
│ │ │ └─── Month (1–12)
│ │ └───── Day of month (1–31)
│ └─────── Hour (0–23)
└───────── Minute (0–59)

Examples:
0 9 * * 1-5   → Every weekday at 9:00 AM
*/30 * * * *   → Every 30 minutes
0 0 * * 0      → Every Sunday at midnight
```

**Interview-style Explanation:**
> "Production-এ cron job বা Celery beat use করি। Development/simple automation-এ Python `schedule` library সহজ। Long-running background task-এর জন্য Celery + Redis production standard।"

**Common Mistakes:**
- script-এ `schedule` run না করে block হওয়া — `while True` loop দরকার
- timezone handle না করা — UTC vs BDT (UTC+6)
- cron job-এ absolute path না দেওয়া — relative path error হয়

**Follow-up Interview Questions:**
1. `schedule` library আর cron-এর পার্থক্য?
2. Production-এ periodic task কীভাবে করবেন?
3. Celery কী? কখন দরকার?

**Code Example:**
```python
import schedule
import time
import logging
from datetime import datetime

logging.basicConfig(level=logging.INFO, format="%(asctime)s %(message)s")
logger = logging.getLogger(__name__)

# Tasks
def generate_daily_report():
    logger.info("Generating daily sales report...")
    # DB query, CSV export, email send...
    with open(f"reports/report_{datetime.now().date()}.csv", "w") as f:
        f.write("date,sales,orders\n")
        f.write(f"{datetime.now().date()},150000,45\n")
    logger.info("Report generated")

def sync_data():
    logger.info("Syncing data from external API...")
    # requests.get(), save to DB...

def cleanup_temp_files():
    import shutil
    from pathlib import Path
    for f in Path("temp").glob("*.tmp"):
        f.unlink()
    logger.info("Temp files cleaned")

def health_check():
    logger.info(f"Health check: {datetime.now()} — OK")

# Schedule
schedule.every().day.at("09:00").do(generate_daily_report)
schedule.every(30).minutes.do(sync_data)
schedule.every().monday.at("00:00").do(cleanup_temp_files)
schedule.every(5).minutes.do(health_check)

# Run loop
logger.info("Scheduler started...")
while True:
    schedule.run_pending()
    time.sleep(30)   # check every 30 seconds
```

---

## PART 7 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Know |
|---|---|---|
| os & sys | `os.path`, `pathlib`, `sys.argv` | pathlib over os.path |
| subprocess | `subprocess.run()`, capture output | `shell=True` security risk |
| shutil | Copy/move/delete/archive | `rmtree()` irreversible |
| File Automation | Pattern: walk → categorize → move | Duplicate name handling |
| requests | GET/POST, timeout, raise_for_status | `Session()` for reuse |
| BeautifulSoup | `find()`, `find_all()`, `select()` | Dynamic page → Selenium |
| Selenium | Browser automation, `WebDriverWait` | Always `driver.quit()` |
| Schedule | `schedule` library + `while True` | Production → Celery/cron |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part8"></a>

## 📋 PART 8 সূচিপত্র — Python DSA & Problem Solving

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [Big O Notation](#p8-bigo) | Time & space complexity analysis |
| 2 | [Arrays & Lists](#p8-arrays) | Operations, complexity, patterns |
| 3 | [Stack](#p8-stack) | LIFO, implementation, use cases |
| 4 | [Queue](#p8-queue) | FIFO, deque, priority queue |
| 5 | [Linked List](#p8-linked-list) | Singly/doubly, traversal, reversal |
| 6 | [Trees](#p8-trees) | BST, traversal (inorder/preorder/postorder) |
| 7 | [Graphs](#p8-graphs) | BFS, DFS, adjacency list |
| 8 | [Recursion](#p8-recursion) | Base case, call stack, memoization |
| 9 | [Sorting Algorithms](#p8-sorting) | Bubble, merge, quick sort |
| 10 | [Searching Algorithms](#p8-searching) | Linear, binary search |
| 11 | [Dynamic Programming](#p8-dp) | Memoization, tabulation, common patterns |
| 12 | [Common Patterns](#p8-patterns) | Two pointers, sliding window, hash map |

---

<a id="p8-bigo"></a>

## 1. Big O Notation

**Definition:**
Big O Notation হলো algorithm-এর time/space complexity describe করার standard। Input size বাড়লে runtime কতটা বাড়ে তা measure করে।

**Common Complexities (Best → Worst):**

| Notation | নাম | Example |
|---|---|---|
| O(1) | Constant | Array index access, hash map get |
| O(log n) | Logarithmic | Binary search, BST operations |
| O(n) | Linear | List traversal, linear search |
| O(n log n) | Linearithmic | Merge sort, heap sort |
| O(n²) | Quadratic | Bubble sort, nested loops |
| O(2ⁿ) | Exponential | Recursive fibonacci (naive) |
| O(n!) | Factorial | Permutations |

**Interview-style Explanation:**
> "Big O worst-case scenario describe করে। n=1000-এ O(n²) = 1,000,000 operations, O(log n) = ~10 operations। Interview-এ যেকোনো solution-এর time complexity বলতে পারা mandatory।"

**Common Mistakes:**
- Best case আর worst case confuse করা — Big O is worst case
- Constants drop করতে ভুলে যাওয়া: O(2n) = O(n)
- Space complexity ভুলে যাওয়া

**Follow-up Interview Questions:**
1. O(n) আর O(n²) solution-এর পার্থক্য কি practically গুরুত্বপূর্ণ?
2. Space complexity কীভাবে calculate করবেন?
3. `in` operator list-এ O(n), set-এ O(1) — কেন?

---

<a id="p8-arrays"></a>

## 2. Arrays & Lists

**Definition:**
Python `list` dynamic array — random access O(1), append amortized O(1), insert/delete middle O(n)।

**List Complexity:**

| Operation | Complexity |
|---|---|
| `lst[i]` (access) | O(1) |
| `lst.append()` | O(1) amortized |
| `lst.insert(i, x)` | O(n) |
| `lst.remove(x)` | O(n) |
| `x in lst` | O(n) |
| `len(lst)` | O(1) |
| `lst.sort()` | O(n log n) |

**Common Interview Patterns:**
- Two pointers
- Sliding window
- Prefix sum
- Kadane's algorithm (max subarray)

**Code Example:**
```python
from typing import List

# Two Sum — O(n) with hash map
def two_sum(nums: List[int], target: int) -> List[int]:
    seen = {}   # value → index
    for i, num in enumerate(nums):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
    return []

print(two_sum([2, 7, 11, 15], 9))   # [0, 1]

# Maximum subarray sum — Kadane's O(n)
def max_subarray(nums: List[int]) -> int:
    max_sum = current = nums[0]
    for num in nums[1:]:
        current = max(num, current + num)
        max_sum = max(max_sum, current)
    return max_sum

print(max_subarray([-2, 1, -3, 4, -1, 2, 1, -5, 4]))   # 6

# Rotate array k steps — O(n), O(1) space
def rotate(nums: List[int], k: int) -> None:
    n = len(nums)
    k %= n
    nums[:] = nums[-k:] + nums[:-k]

nums = [1, 2, 3, 4, 5, 6, 7]
rotate(nums, 3)
print(nums)   # [5, 6, 7, 1, 2, 3, 4]

# Prefix sum — range sum query O(1)
def range_sum(nums: List[int], l: int, r: int) -> int:
    prefix = [0] * (len(nums) + 1)
    for i, n in enumerate(nums):
        prefix[i+1] = prefix[i] + n
    return prefix[r+1] - prefix[l]

print(range_sum([1, 2, 3, 4, 5], 1, 3))   # 2+3+4 = 9
```

---

<a id="p8-stack"></a>

## 3. Stack

**Definition:**
Stack হলো **LIFO** (Last In First Out) data structure। Python-এ `list` অথবা `collections.deque` দিয়ে implement করা হয়।

**Real-life Analogy:**
Stack হলো **থালা-বাসনের stack** — উপরে রাখা, উপর থেকে নেওয়া।

**Operations:**

| Operation | List (Python) | Complexity |
|---|---|---|
| Push | `lst.append(x)` | O(1) |
| Pop | `lst.pop()` | O(1) |
| Peek | `lst[-1]` | O(1) |
| Empty check | `not lst` | O(1) |

**Use Cases:**
- undo/redo functionality
- function call stack
- balanced parentheses check
- expression evaluation
- browser back button

**Code Example:**
```python
from collections import deque
from typing import Optional

# Stack using deque (thread-safe, efficient)
class Stack:
    def __init__(self):
        self._data = deque()

    def push(self, item): self._data.append(item)
    def pop(self) -> Optional[any]: return self._data.pop() if self._data else None
    def peek(self) -> Optional[any]: return self._data[-1] if self._data else None
    def is_empty(self) -> bool: return not self._data
    def size(self) -> int: return len(self._data)

# Classic interview problem: Balanced Parentheses — O(n)
def is_balanced(s: str) -> bool:
    stack = []
    pairs = {")": "(", "]": "[", "}": "{"}
    for ch in s:
        if ch in "([{":
            stack.append(ch)
        elif ch in ")]}":
            if not stack or stack[-1] != pairs[ch]:
                return False
            stack.pop()
    return not stack

print(is_balanced("({[]})"))     # True
print(is_balanced("({[})"))      # False
print(is_balanced("((()))"))     # True

# Next Greater Element — O(n) with stack
def next_greater(nums: list[int]) -> list[int]:
    result = [-1] * len(nums)
    stack = []   # indices
    for i, num in enumerate(nums):
        while stack and nums[stack[-1]] < num:
            result[stack.pop()] = num
        stack.append(i)
    return result

print(next_greater([4, 5, 2, 10, 8]))   # [5, 10, 10, -1, -1]
```

---

<a id="p8-queue"></a>

## 4. Queue

**Definition:**
Queue হলো **FIFO** (First In First Out) data structure। Python-এ `collections.deque` অথবা `queue.Queue` use করা হয়।

**Real-life Analogy:**
Queue হলো **bank counter-এর লাইন** — যে আগে আসে, আগে সেবা পায়।

**Types:**

| Type | Python | Use Case |
|---|---|---|
| Simple Queue | `deque` | FIFO processing |
| Priority Queue | `heapq` / `queue.PriorityQueue` | Task priority |
| Double-ended | `deque` | Sliding window |

**Code Example:**
```python
from collections import deque
import heapq

# Queue with deque
queue = deque()
queue.append("task1")      # enqueue
queue.append("task2")
queue.append("task3")
print(queue.popleft())     # dequeue → "task1"

# BFS uses queue
def bfs_level_order(root):
    if not root: return []
    result, queue = [], deque([root])
    while queue:
        level = []
        for _ in range(len(queue)):
            node = queue.popleft()
            level.append(node.val)
            if node.left:  queue.append(node.left)
            if node.right: queue.append(node.right)
        result.append(level)
    return result

# Priority Queue with heapq (min-heap)
tasks = []
heapq.heappush(tasks, (3, "low priority task"))
heapq.heappush(tasks, (1, "high priority task"))
heapq.heappush(tasks, (2, "medium priority task"))

while tasks:
    priority, task = heapq.heappop(tasks)
    print(f"[{priority}] {task}")

# Sliding Window Maximum — deque O(n)
def max_sliding_window(nums: list[int], k: int) -> list[int]:
    dq = deque()   # stores indices
    result = []
    for i, num in enumerate(nums):
        # remove indices outside window
        while dq and dq[0] < i - k + 1:
            dq.popleft()
        # remove smaller elements
        while dq and nums[dq[-1]] < num:
            dq.pop()
        dq.append(i)
        if i >= k - 1:
            result.append(nums[dq[0]])
    return result

print(max_sliding_window([1,3,-1,-3,5,3,6,7], 3))   # [3,3,5,5,6,7]
```

---

<a id="p8-linked-list"></a>

## 5. Linked List

**Definition:**
Linked List হলো nodes-এর chain, প্রতিটি node data ও next pointer ধরে। Array-এর alternative — insert/delete O(1) কিন্তু random access নেই।

**Array vs Linked List:**

| | Array (List) | Linked List |
|---|---|---|
| Access | O(1) | O(n) |
| Insert/Delete (middle) | O(n) | O(1) (node known) |
| Memory | Contiguous | Non-contiguous |
| Cache friendly | ✅ | ❌ |

**Singly Linked List Operations:**

```python
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

# Build: 1 → 2 → 3 → 4 → 5
def build_list(values: list) -> ListNode:
    dummy = ListNode(0)
    curr = dummy
    for v in values:
        curr.next = ListNode(v)
        curr = curr.next
    return dummy.next

def to_list(head: ListNode) -> list:
    result = []
    while head:
        result.append(head.val)
        head = head.next
    return result

# Reverse Linked List — O(n), O(1)
def reverse_list(head: ListNode) -> ListNode:
    prev, curr = None, head
    while curr:
        next_node = curr.next
        curr.next = prev
        prev = curr
        curr = next_node
    return prev

# Detect cycle — Floyd's algorithm O(n), O(1)
def has_cycle(head: ListNode) -> bool:
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
        if slow is fast:
            return True
    return False

# Find middle — slow/fast pointer O(n)
def find_middle(head: ListNode) -> ListNode:
    slow = fast = head
    while fast and fast.next:
        slow = slow.next
        fast = fast.next.next
    return slow

# Merge two sorted lists — O(n+m)
def merge_sorted(l1: ListNode, l2: ListNode) -> ListNode:
    dummy = ListNode(0)
    curr = dummy
    while l1 and l2:
        if l1.val <= l2.val:
            curr.next, l1 = l1, l1.next
        else:
            curr.next, l2 = l2, l2.next
        curr = curr.next
    curr.next = l1 or l2
    return dummy.next

# Test
head = build_list([1, 2, 3, 4, 5])
print(to_list(reverse_list(head)))    # [5, 4, 3, 2, 1]
head2 = build_list([1, 2, 3, 4, 5])
print(find_middle(head2).val)         # 3
```

---

<a id="p8-trees"></a>

## 6. Trees

**Definition:**
Tree হলো hierarchical data structure। **Binary Search Tree (BST)** — left < root < right। Balanced BST-এ search O(log n)।

**Traversal Types:**

| Traversal | Order | Use Case |
|---|---|---|
| Inorder (LNR) | Left → Node → Right | BST → sorted output |
| Preorder (NLR) | Node → Left → Right | Tree copy, serialize |
| Postorder (LRN) | Left → Right → Node | Delete tree, evaluate |
| Level Order | Level by level (BFS) | Shortest path, level info |

**Code Example:**
```python
from collections import deque
from typing import Optional

class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

# Build BST
def insert_bst(root: Optional[TreeNode], val: int) -> TreeNode:
    if not root: return TreeNode(val)
    if val < root.val:
        root.left = insert_bst(root.left, val)
    else:
        root.right = insert_bst(root.right, val)
    return root

# Traversals
def inorder(root: Optional[TreeNode]) -> list:
    if not root: return []
    return inorder(root.left) + [root.val] + inorder(root.right)

def preorder(root: Optional[TreeNode]) -> list:
    if not root: return []
    return [root.val] + preorder(root.left) + preorder(root.right)

def level_order(root: Optional[TreeNode]) -> list[list]:
    if not root: return []
    result, queue = [], deque([root])
    while queue:
        level = []
        for _ in range(len(queue)):
            node = queue.popleft()
            level.append(node.val)
            if node.left: queue.append(node.left)
            if node.right: queue.append(node.right)
        result.append(level)
    return result

# Max depth — O(n)
def max_depth(root: Optional[TreeNode]) -> int:
    if not root: return 0
    return 1 + max(max_depth(root.left), max_depth(root.right))

# Validate BST — O(n)
def is_valid_bst(root, min_val=float('-inf'), max_val=float('inf')) -> bool:
    if not root: return True
    if not (min_val < root.val < max_val): return False
    return (is_valid_bst(root.left, min_val, root.val) and
            is_valid_bst(root.right, root.val, max_val))

# Test
root = None
for val in [5, 3, 7, 2, 4, 6, 8]:
    root = insert_bst(root, val)

print("Inorder (sorted):", inorder(root))    # [2,3,4,5,6,7,8]
print("Level order:", level_order(root))
print("Max depth:", max_depth(root))
print("Valid BST:", is_valid_bst(root))
```

---

<a id="p8-graphs"></a>

## 7. Graphs

**Definition:**
Graph হলো nodes (vertices) এবং edges-এর collection। Directed/undirected, weighted/unweighted হতে পারে।

**Representation:**

| Type | কখন use |
|---|---|
| Adjacency List | Sparse graph (most common) |
| Adjacency Matrix | Dense graph, edge existence O(1) |

**BFS vs DFS:**

| | BFS | DFS |
|---|---|---|
| Data structure | Queue | Stack/Recursion |
| Use case | Shortest path (unweighted) | Cycle detection, path finding |
| Complexity | O(V + E) | O(V + E) |

**Code Example:**
```python
from collections import defaultdict, deque
from typing import Optional

class Graph:
    def __init__(self):
        self.adj = defaultdict(list)   # adjacency list

    def add_edge(self, u, v, directed=False):
        self.adj[u].append(v)
        if not directed:
            self.adj[v].append(u)

    # BFS — shortest path (unweighted)
    def bfs(self, start) -> list:
        visited = set([start])
        queue = deque([start])
        order = []
        while queue:
            node = queue.popleft()
            order.append(node)
            for neighbor in self.adj[node]:
                if neighbor not in visited:
                    visited.add(neighbor)
                    queue.append(neighbor)
        return order

    # DFS — iterative
    def dfs(self, start) -> list:
        visited = set()
        stack = [start]
        order = []
        while stack:
            node = stack.pop()
            if node not in visited:
                visited.add(node)
                order.append(node)
                stack.extend(self.adj[node])
        return order

    # Shortest path with BFS
    def shortest_path(self, start, end) -> Optional[list]:
        if start == end: return [start]
        visited = {start: None}   # node → parent
        queue = deque([start])
        while queue:
            node = queue.popleft()
            for neighbor in self.adj[node]:
                if neighbor not in visited:
                    visited[neighbor] = node
                    if neighbor == end:
                        # Reconstruct path
                        path = []
                        curr = end
                        while curr is not None:
                            path.append(curr)
                            curr = visited[curr]
                        return path[::-1]
                    queue.append(neighbor)
        return None   # no path

# Test
g = Graph()
for u, v in [("A","B"),("A","C"),("B","D"),("C","D"),("D","E")]:
    g.add_edge(u, v)

print("BFS:", g.bfs("A"))
print("DFS:", g.dfs("A"))
print("Path A→E:", g.shortest_path("A", "E"))
```

---

<a id="p8-recursion"></a>

## 8. Recursion

**Definition:**
Recursion হলো function নিজেকে নিজে call করা। প্রতিটি recursive function-এ **base case** (termination) এবং **recursive case** থাকতে হবে।

**Real-life Analogy:**
Recursion কে **Russian nesting doll** এর মতো ভাবুন — খুললে আরেকটি, সবশেষে সবচেয়ে ছোটটি (base case)।

**Call Stack visualization:**
```text
factorial(4)
  └── 4 * factorial(3)
          └── 3 * factorial(2)
                  └── 2 * factorial(1)
                              └── 1  (base case)
```

**Code Example:**
```python
import sys
from functools import lru_cache

# Factorial
def factorial(n: int) -> int:
    if n <= 1: return 1          # base case
    return n * factorial(n - 1)  # recursive case

# Fibonacci — naive O(2ⁿ)
def fib_naive(n: int) -> int:
    if n <= 1: return n
    return fib_naive(n-1) + fib_naive(n-2)

# Fibonacci — memoized O(n) with lru_cache
@lru_cache(maxsize=None)
def fib(n: int) -> int:
    if n <= 1: return n
    return fib(n-1) + fib(n-2)

print(fib(50))   # instant

# Power — O(log n) divide and conquer
def power(base: float, exp: int) -> float:
    if exp == 0: return 1
    if exp % 2 == 0:
        half = power(base, exp // 2)
        return half * half
    return base * power(base, exp - 1)

# Flatten nested list (recursive)
def flatten(nested: list) -> list:
    result = []
    for item in nested:
        if isinstance(item, list):
            result.extend(flatten(item))
        else:
            result.append(item)
    return result

print(flatten([1, [2, [3, 4], 5], [6, 7]]))   # [1,2,3,4,5,6,7]
```

---

<a id="p8-sorting"></a>

## 9. Sorting Algorithms

**Comparison:**

| Algorithm | Best | Average | Worst | Space | Stable? |
|---|---|---|---|---|---|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | ✅ |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) | ❌ |
| Python `sort()` | O(n) | O(n log n) | O(n log n) | O(n) | ✅ |

**Interview-style Explanation:**
> "Python-এ `sorted()` এবং `.sort()` Timsort algorithm use করে — merge sort + insertion sort-এর hybrid। Interview-এ merge sort বা quick sort implement করতে বলা হয়।"

**Code Example:**
```python
# Merge Sort — O(n log n), stable
def merge_sort(arr: list) -> list:
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    return merge(left, right)

def merge(left: list, right: list) -> list:
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i]); i += 1
        else:
            result.append(right[j]); j += 1
    result.extend(left[i:])
    result.extend(right[j:])
    return result

# Quick Sort — O(n log n) average
def quick_sort(arr: list) -> list:
    if len(arr) <= 1: return arr
    pivot = arr[len(arr) // 2]
    left   = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right  = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)

arr = [64, 34, 25, 12, 22, 11, 90]
print(merge_sort(arr))
print(quick_sort(arr))
print(sorted(arr))   # Python built-in Timsort
```

---

<a id="p8-searching"></a>

## 10. Searching Algorithms

**Binary Search — O(log n):**
```python
def binary_search(arr: list, target: int) -> int:
    left, right = 0, len(arr) - 1
    while left <= right:
        mid = left + (right - left) // 2   # overflow safe
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1   # not found

# Binary search variants
def search_insert_position(arr: list, target: int) -> int:
    """Find index to insert target (leftmost position)"""
    left, right = 0, len(arr)
    while left < right:
        mid = (left + right) // 2
        if arr[mid] < target:
            left = mid + 1
        else:
            right = mid
    return left

# Python bisect module
import bisect

arr = [1, 3, 5, 7, 9, 11]
print(binary_search(arr, 7))                   # 3
print(bisect.bisect_left(arr, 6))              # 3 (insert position)
print(bisect.bisect_right(arr, 7))             # 4
```

---

<a id="p8-dp"></a>

## 11. Dynamic Programming

**Definition:**
Dynamic Programming (DP) complex problem-কে overlapping subproblem-এ ভেঙে solve করে এবং result cache করে।

**Two Approaches:**

| Approach | মানে | Implementation |
|---|---|---|
| Memoization | Top-down, cache recursion | `@lru_cache` বা dict |
| Tabulation | Bottom-up, iterative table | Array/2D array |

**Common DP Patterns:**
- Fibonacci sequence
- 0/1 Knapsack
- Coin change
- Longest Common Subsequence
- Climbing stairs

**Code Example:**
```python
from functools import lru_cache

# Climbing Stairs — O(n)
# n stairs, 1 or 2 steps at a time — how many ways?
def climb_stairs(n: int) -> int:
    if n <= 2: return n
    dp = [0] * (n + 1)
    dp[1], dp[2] = 1, 2
    for i in range(3, n + 1):
        dp[i] = dp[i-1] + dp[i-2]
    return dp[n]

print(climb_stairs(10))   # 89

# Coin Change — minimum coins — O(amount * len(coins))
def coin_change(coins: list[int], amount: int) -> int:
    dp = [float("inf")] * (amount + 1)
    dp[0] = 0
    for coin in coins:
        for x in range(coin, amount + 1):
            dp[x] = min(dp[x], dp[x - coin] + 1)
    return dp[amount] if dp[amount] != float("inf") else -1

print(coin_change([1, 5, 10, 25], 36))   # 3 (25+10+1)

# Longest Common Subsequence — O(m*n)
def lcs(s1: str, s2: str) -> int:
    m, n = len(s1), len(s2)
    dp = [[0] * (n + 1) for _ in range(m + 1)]
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if s1[i-1] == s2[j-1]:
                dp[i][j] = dp[i-1][j-1] + 1
            else:
                dp[i][j] = max(dp[i-1][j], dp[i][j-1])
    return dp[m][n]

print(lcs("ABCBDAB", "BDCABA"))   # 4

# 0/1 Knapsack — O(n * capacity)
def knapsack(weights: list, values: list, capacity: int) -> int:
    n = len(weights)
    dp = [[0] * (capacity + 1) for _ in range(n + 1)]
    for i in range(1, n + 1):
        for w in range(capacity + 1):
            dp[i][w] = dp[i-1][w]
            if weights[i-1] <= w:
                dp[i][w] = max(dp[i][w], dp[i-1][w-weights[i-1]] + values[i-1])
    return dp[n][capacity]

print(knapsack([2, 3, 4, 5], [3, 4, 5, 6], 8))   # 10
```

---

<a id="p8-patterns"></a>

## 12. Common Patterns

**Definition:**
Interview-এ বারবার দেখা যায় এমন problem-solving patterns — এগুলো চেনা থাকলে নতুন problem-ও দ্রুত solve করা যায়।

**Pattern 1 — Two Pointers:**
```python
# Pair with given sum in sorted array — O(n)
def two_sum_sorted(arr: list[int], target: int) -> tuple:
    l, r = 0, len(arr) - 1
    while l < r:
        s = arr[l] + arr[r]
        if s == target: return (l, r)
        elif s < target: l += 1
        else: r -= 1
    return (-1, -1)

# Remove duplicates in-place — O(n)
def remove_duplicates(nums: list[int]) -> int:
    if not nums: return 0
    slow = 0
    for fast in range(1, len(nums)):
        if nums[fast] != nums[slow]:
            slow += 1
            nums[slow] = nums[fast]
    return slow + 1
```

**Pattern 2 — Sliding Window:**
```python
# Max sum subarray of size k — O(n)
def max_sum_subarray(nums: list[int], k: int) -> int:
    window_sum = sum(nums[:k])
    max_sum = window_sum
    for i in range(k, len(nums)):
        window_sum += nums[i] - nums[i - k]
        max_sum = max(max_sum, window_sum)
    return max_sum

# Longest substring without repeating — O(n)
def length_of_longest_substring(s: str) -> int:
    char_index = {}
    max_len = start = 0
    for i, ch in enumerate(s):
        if ch in char_index and char_index[ch] >= start:
            start = char_index[ch] + 1
        char_index[ch] = i
        max_len = max(max_len, i - start + 1)
    return max_len

print(length_of_longest_substring("abcabcbb"))   # 3 (abc)
```

**Pattern 3 — Hash Map for O(1) lookup:**
```python
# Frequency counter — anagram check O(n)
def is_anagram(s: str, t: str) -> bool:
    from collections import Counter
    return Counter(s) == Counter(t)

# Group anagrams — O(n * k log k)
def group_anagrams(words: list[str]) -> list[list[str]]:
    from collections import defaultdict
    groups = defaultdict(list)
    for word in words:
        key = tuple(sorted(word))
        groups[key].append(word)
    return list(groups.values())

print(group_anagrams(["eat","tea","tan","ate","nat","bat"]))
```

---

## PART 8 Quick Revision Table

| Topic | Key Concept | Interview Must-Know |
|---|---|---|
| Big O | Worst-case time/space | O(1) < O(log n) < O(n) < O(n log n) < O(n²) |
| Arrays | Dynamic array, index O(1) | `in` list = O(n), `in` set = O(1) |
| Stack | LIFO, `deque` | Balanced parentheses, monotonic stack |
| Queue | FIFO, `deque` | BFS uses queue |
| Linked List | Node chain, no random access | Reverse, cycle detection, two pointer |
| Trees | BST, traversals | Inorder BST = sorted, BFS = level order |
| Graphs | BFS (shortest), DFS (explore) | Adjacency list, visited set |
| Recursion | Base case + recursive case | Stack overflow, memoize |
| Sorting | Merge O(n log n) stable | Quick sort avg O(n log n), worst O(n²) |
| Binary Search | Sorted array, O(log n) | `left + (right-left)//2` overflow safe |
| DP | Cache overlapping subproblems | Memoization vs tabulation |
| Patterns | Two pointer, sliding window, hash map | Recognize pattern → apply template |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 9 — Testing & Best Practices *(Next request এ লিখব)*
