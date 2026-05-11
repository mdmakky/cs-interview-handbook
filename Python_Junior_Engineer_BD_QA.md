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

> **📌 পরবর্তী:** PART 3 — Object-Oriented Programming in Python *(Next request এ লিখব)*
