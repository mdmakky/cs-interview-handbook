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

<a id="part9"></a>

## 📋 PART 9 সূচিপত্র — Testing & Best Practices

| # | Topic | What You Will Learn |
|---|---|---|
| 1 | [Unit Testing — unittest](#p9-unittest) | TestCase, assertions, setUp/tearDown |
| 2 | [pytest](#p9-pytest) | Fixtures, parametrize, markers, coverage |
| 3 | [Mocking](#p9-mocking) | `unittest.mock`, patch, MagicMock |
| 4 | [PEP 8 — Style Guide](#p9-pep8) | Naming, indentation, line length rules |
| 5 | [Clean Code Principles](#p9-clean-code) | Readable, maintainable Python |
| 6 | [Virtual Environment](#p9-venv) | venv, pip, requirements.txt |
| 7 | [Project Structure](#p9-structure) | Standard layout, packaging |
| 8 | [Git Workflow](#p9-git) | Branching, commit messages, .gitignore |

---

<a id="p9-unittest"></a>

## 1. Unit Testing — unittest

**Definition:**
Unit testing মানে code-এর সবচেয়ে ছোট unit (function, method) আলাদাভাবে test করা। Python-এর built-in `unittest` module এর জন্য।

**Real-life Analogy:**
Unit testing হলো **factory QA** — প্রতিটি part আলাদাভাবে check করা, final product assemble করার আগে।

**Key Assertion Methods:**

| Method | চেক করে |
|---|---|
| `assertEqual(a, b)` | a == b |
| `assertNotEqual(a, b)` | a != b |
| `assertTrue(x)` | bool(x) is True |
| `assertFalse(x)` | bool(x) is False |
| `assertIsNone(x)` | x is None |
| `assertIn(a, b)` | a in b |
| `assertRaises(exc)` | exception raised |
| `assertAlmostEqual(a, b)` | float equality |

**Interview-style Explanation:**
> "`setUp()` প্রতিটি test-এর আগে এবং `tearDown()` প্রতিটি test-এর পরে চলে। `setUpClass()` পুরো class-এ একবার চলে — expensive resource (DB connection) এর জন্য। Test method-এর নাম `test_` দিয়ে শুরু হতে হয়।"

**Common Mistakes:**
- test method `test_` prefix না দেওয়া — run হবে না
- test-এ external dependency (DB, API) সরাসরি call করা — mock করুন
- test isolation না করা — একটি test আরেকটির উপর depend করা

**Follow-up Interview Questions:**
1. `setUp()` আর `setUpClass()` পার্থক্য?
2. Test isolation কেন দরকার?
3. `assertRaises()` কীভাবে use করবেন?

**Code Example:**
```python
import unittest
from unittest import TestCase

# Code under test
class BankAccount:
    def __init__(self, owner: str, balance: float = 0):
        if balance < 0:
            raise ValueError("Balance cannot be negative")
        self.owner = owner
        self.balance = balance
        self._transactions = []

    def deposit(self, amount: float) -> float:
        if amount <= 0:
            raise ValueError("Deposit amount must be positive")
        self.balance += amount
        self._transactions.append(("deposit", amount))
        return self.balance

    def withdraw(self, amount: float) -> float:
        if amount <= 0:
            raise ValueError("Withdraw amount must be positive")
        if amount > self.balance:
            raise ValueError(f"Insufficient funds: balance={self.balance}")
        self.balance -= amount
        self._transactions.append(("withdraw", amount))
        return self.balance

    def get_history(self) -> list:
        return self._transactions.copy()


# Test class
class TestBankAccount(TestCase):

    def setUp(self):
        """Runs before each test"""
        self.account = BankAccount("Rahim", 10000)

    def tearDown(self):
        """Runs after each test (cleanup)"""
        pass

    def test_initial_balance(self):
        self.assertEqual(self.account.balance, 10000)
        self.assertEqual(self.account.owner, "Rahim")

    def test_deposit_valid(self):
        new_balance = self.account.deposit(5000)
        self.assertEqual(new_balance, 15000)
        self.assertEqual(self.account.balance, 15000)

    def test_deposit_invalid(self):
        with self.assertRaises(ValueError):
            self.account.deposit(-100)
        with self.assertRaises(ValueError):
            self.account.deposit(0)

    def test_withdraw_valid(self):
        new_balance = self.account.withdraw(3000)
        self.assertEqual(new_balance, 7000)

    def test_withdraw_insufficient_funds(self):
        with self.assertRaises(ValueError) as ctx:
            self.account.withdraw(50000)
        self.assertIn("Insufficient funds", str(ctx.exception))

    def test_negative_initial_balance_raises(self):
        with self.assertRaises(ValueError):
            BankAccount("Karim", -100)

    def test_transaction_history(self):
        self.account.deposit(2000)
        self.account.withdraw(1000)
        history = self.account.get_history()
        self.assertEqual(len(history), 2)
        self.assertIn(("deposit", 2000), history)
        self.assertIn(("withdraw", 1000), history)


if __name__ == "__main__":
    unittest.main(verbosity=2)
```

---

<a id="p9-pytest"></a>

## 2. pytest

**Definition:**
`pytest` Python-এর most popular testing framework। `unittest`-এর চেয়ে concise syntax, powerful fixtures, parametrize, এবং rich plugin ecosystem।

**unittest vs pytest:**

| | unittest | pytest |
|---|---|---|
| Setup | `class TestCase` | Function-based (class optional) |
| Assertions | `self.assertEqual()` | Plain `assert` |
| Fixtures | `setUp`/`tearDown` | `@pytest.fixture` (reusable) |
| Parametrize | Manual | `@pytest.mark.parametrize` |
| Output | Basic | Rich, colored |

**Practical Use Case:**
- FastAPI endpoint testing
- database layer testing
- utility function testing

**Interview-style Explanation:**
> "pytest-এ plain `assert` ব্যবহার করি — pytest automatically introspects assertion failure। `@pytest.fixture` reusable test setup বানায়, `scope` দিয়ে lifetime control করা যায় (function/class/module/session)।"

**Common Mistakes:**
- fixture scope না বোঝা — `session` scope fixture একবার তৈরি হয় সব test-এ
- `conftest.py` এর role না জানা — shared fixtures এখানে রাখা হয়
- test file `test_` prefix না দেওয়া — pytest discover করবে না

**Follow-up Interview Questions:**
1. pytest fixture কী? `setUp()` থেকে কীভাবে আলাদা?
2. `conftest.py` কী?
3. pytest দিয়ে coverage কীভাবে check করবেন?

**Code Example:**
```python
# test_bank.py
import pytest
from bank import BankAccount   # previous example

# ──── Fixtures ────
@pytest.fixture
def account():
    """Function-scoped — প্রতি test-এ নতুন"""
    return BankAccount("Rahim", 10000)

@pytest.fixture(scope="module")
def read_only_account():
    """Module-scoped — এই file-এ একবার"""
    return BankAccount("ReadOnly", 100000)

# ──── Basic tests ────
def test_deposit(account):
    result = account.deposit(5000)
    assert result == 15000
    assert account.balance == 15000

def test_withdraw(account):
    account.withdraw(3000)
    assert account.balance == 7000

def test_negative_balance_raises():
    with pytest.raises(ValueError, match="cannot be negative"):
        BankAccount("X", -1)

# ──── Parametrize ────
@pytest.mark.parametrize("amount,expected", [
    (1000, 11000),
    (5000, 15000),
    (9999, 19999),
])
def test_deposit_parametrized(account, amount, expected):
    assert account.deposit(amount) == expected

@pytest.mark.parametrize("invalid_amount", [-100, 0, -0.01])
def test_deposit_invalid_amounts(account, invalid_amount):
    with pytest.raises(ValueError):
        account.deposit(invalid_amount)

# ──── Markers ────
@pytest.mark.slow
def test_large_operations(account):
    for _ in range(10000):
        account.deposit(1)
    assert account.balance == 20000

# Run: pytest test_bank.py -v
# Run with coverage: pytest --cov=bank --cov-report=term-missing
# Skip slow: pytest -m "not slow"
```

```ini
# pytest.ini
[pytest]
testpaths = tests
addopts = -v --tb=short
markers =
    slow: marks tests as slow
    integration: marks integration tests
```

---

<a id="p9-mocking"></a>

## 3. Mocking

**Definition:**
Mock হলো real object-এর fake version যা test-এ external dependency (DB, API, email) replace করে। `unittest.mock` module use হয়।

**Real-life Analogy:**
Mock হলো **film set** — আসল বাড়ি নয়, কিন্তু দেখতে বাড়ির মতো। Actor-রা real জায়গায় না গিয়েই scene করে।

**Key Mock Tools:**

| Tool | কাজ |
|---|---|
| `MagicMock()` | All-purpose mock object |
| `patch()` | Temporarily replace an object |
| `patch.object()` | Replace specific method |
| `Mock(return_value=x)` | Set return value |
| `mock.assert_called_once_with(args)` | Verify call |
| `mock.call_count` | How many times called |

**Interview-style Explanation:**
> "Mock দিয়ে external API, database, email, payment gateway — সব fake করা যায়। Test fast থাকে, external service-এর উপর depend করে না। `patch()` context manager বা decorator হিসেবে use করি।"

**Common Mistakes:**
- patch করার path ভুল দেওয়া — যেখানে import হয়েছে সেখানে patch করতে হবে
- `assert_called_with()` আর `assert_called_once_with()` confuse করা
- mock করার প্রয়োজন নেই এমন কিছু mock করা

**Follow-up Interview Questions:**
1. Mock কেন দরকার?
2. `patch` decorator কীভাবে কাজ করে?
3. `MagicMock` আর `Mock` পার্থক্য?

**Code Example:**
```python
import pytest
from unittest.mock import MagicMock, patch, call

# ──── Code to test ────
import requests

class WeatherService:
    BASE_URL = "https://api.weather.com/v1"

    def get_temperature(self, city: str) -> float:
        response = requests.get(f"{self.BASE_URL}/temp?city={city}", timeout=5)
        response.raise_for_status()
        return response.json()["temperature"]

class NotificationService:
    def send_email(self, to: str, subject: str, body: str) -> bool:
        # external email API call
        pass

class UserService:
    def __init__(self, notifier: NotificationService):
        self.notifier = notifier

    def register_user(self, email: str, name: str) -> dict:
        user = {"id": 1, "email": email, "name": name}
        self.notifier.send_email(
            to=email,
            subject="Welcome!",
            body=f"Hello {name}, welcome to our platform!"
        )
        return user


# ──── Tests with mock ────
class TestWeatherService:

    @patch("requests.get")   # patch where it's used
    def test_get_temperature_success(self, mock_get):
        # Setup mock response
        mock_response = MagicMock()
        mock_response.json.return_value = {"temperature": 32.5}
        mock_response.raise_for_status.return_value = None
        mock_get.return_value = mock_response

        service = WeatherService()
        temp = service.get_temperature("Dhaka")

        assert temp == 32.5
        mock_get.assert_called_once_with(
            "https://api.weather.com/v1/temp?city=Dhaka",
            timeout=5
        )

    @patch("requests.get")
    def test_get_temperature_api_error(self, mock_get):
        mock_get.side_effect = requests.exceptions.ConnectionError("Network error")

        service = WeatherService()
        with pytest.raises(requests.exceptions.ConnectionError):
            service.get_temperature("Dhaka")


class TestUserService:

    def test_register_sends_welcome_email(self):
        mock_notifier = MagicMock(spec=NotificationService)
        mock_notifier.send_email.return_value = True

        service = UserService(mock_notifier)
        user = service.register_user("rahim@example.com", "Rahim")

        assert user["email"] == "rahim@example.com"
        mock_notifier.send_email.assert_called_once_with(
            to="rahim@example.com",
            subject="Welcome!",
            body="Hello Rahim, welcome to our platform!"
        )

    def test_register_calls_notifier_exactly_once(self):
        mock_notifier = MagicMock(spec=NotificationService)
        service = UserService(mock_notifier)

        service.register_user("a@b.com", "Alice")
        service.register_user("c@d.com", "Bob")

        assert mock_notifier.send_email.call_count == 2
```

---

<a id="p9-pep8"></a>

## 4. PEP 8 — Style Guide

**Definition:**
PEP 8 হলো Python-এর official coding style guide। Readable, consistent Python code-এর standard।

**Key Rules:**

| Category | Rule | Example |
|---|---|---|
| Indentation | 4 spaces (no tabs) | `def func():` → 4 space indent |
| Line length | Max 79 chars (99 acceptable) | Long line → backslash বা parentheses |
| Blank lines | 2 lines between top-level, 1 inside class | `def f():` — 2 blank lines before |
| Imports | One per line, grouped | stdlib → third-party → local |
| Naming | `snake_case` for variables/functions | `user_name`, `get_user()` |
| Naming | `PascalCase` for classes | `UserService`, `BankAccount` |
| Naming | `UPPER_CASE` for constants | `MAX_RETRY`, `BASE_URL` |
| Naming | `_single_leading` for protected | `_internal_method` |
| Naming | `__double_leading` for private | `__private_attr` |
| Whitespace | Around operators | `x = 1 + 2` not `x=1+2` |
| Whitespace | No space before `(` in call | `func()` not `func ()` |
| Comments | Full sentence, `# ` space after `#` | `# This calculates total` |
| Docstrings | `"""Triple quotes"""` | Public function-এ always |

**Tools:**
- `flake8` — style checker
- `black` — auto-formatter
- `isort` — import sorter
- `pylint` — full linter

**Interview-style Explanation:**
> "PEP 8 follow করলে team-এ code review সহজ হয়, code readable থাকে। Production project-এ `black` দিয়ে auto-format করি, CI/CD-এ `flake8` check রাখি।"

**Code Example:**
```python
# ❌ Bad PEP 8
import os,sys
from pathlib import Path
x=1+2
def getUserById( id,db ):
    user=db.query(User).filter(User.id==id).first()
    return(user)
class userService:
    def __init__(self,db):
        self.db=db

# ✅ Good PEP 8
import os
import sys
from pathlib import Path

# Third-party
from sqlalchemy.orm import Session

# Local
from models import User

MAX_RETRY = 3
BASE_URL = "https://api.example.com"


def get_user_by_id(user_id: int, db: Session):
    """Retrieve a user by their primary key.

    Args:
        user_id: The user's database ID.
        db: SQLAlchemy database session.

    Returns:
        User object or None if not found.
    """
    return db.query(User).filter(User.id == user_id).first()


class UserService:
    def __init__(self, db: Session):
        self.db = db

    def get_user(self, user_id: int):
        return get_user_by_id(user_id, self.db)
```

---

<a id="p9-clean-code"></a>

## 5. Clean Code Principles

**Definition:**
Clean code মানে code যা পড়া সহজ, বোঝা সহজ, এবং maintain করা সহজ। Robert C. Martin-এর "Clean Code" বইয়ের principles।

**Key Principles:**

| Principle | মানে |
|---|---|
| Meaningful names | Variable/function নাম দেখেই বোঝা যায় কী করে |
| Small functions | একটি function একটি কাজ করে (SRP) |
| No magic numbers | `86400` নয়, `SECONDS_PER_DAY = 86400` |
| DRY | Don't Repeat Yourself — duplication avoid |
| Early return | Nested `if` কমানো, early guard clause |
| Avoid deep nesting | Max 2-3 level nesting |

**Interview-style Explanation:**
> "Clean code-এর সবচেয়ে important rule: code একবার লেখা হয়, বারবার পড়া হয়। Function নাম দেখলেই বোঝা যাওয়া উচিত কী করে — comment-এর দরকার নেই। Magic number কখনো না।"

**Code Example:**
```python
# ❌ Bad — Magic numbers, unclear names, deep nesting
def calc(x, lst):
    r = []
    for i in lst:
        if i["type"] == 1:
            if i["active"] == True:
                if i["val"] > 0:
                    r.append(i["val"] * x * 0.18)
    return r

# ✅ Clean
TAX_RATE = 0.18
PRODUCT_TYPE_PHYSICAL = 1

def calculate_tax_for_active_physical_products(
    multiplier: float,
    products: list[dict]
) -> list[float]:
    return [
        product["val"] * multiplier * TAX_RATE
        for product in products
        if _is_taxable_product(product)
    ]

def _is_taxable_product(product: dict) -> bool:
    return (
        product["type"] == PRODUCT_TYPE_PHYSICAL
        and product["active"]
        and product["val"] > 0
    )

# ❌ Bad — no early return, deep nesting
def process_order(order):
    if order is not None:
        if order["status"] == "pending":
            if order["items"]:
                if order["total"] > 0:
                    # actual logic here
                    return True
    return False

# ✅ Clean — early return / guard clause
def process_order(order: dict) -> bool:
    if order is None:
        return False
    if order["status"] != "pending":
        return False
    if not order["items"]:
        return False
    if order["total"] <= 0:
        return False

    # actual logic — no nesting
    return True
```

---

<a id="p9-venv"></a>

## 6. Virtual Environment

**Definition:**
Virtual environment হলো isolated Python environment — প্রতিটি project-এর আলাদা dependencies, system Python-এ conflict নেই।

**Real-life Analogy:**
Virtual environment কে **আলাদা apartment** হিসেবে ভাবুন। প্রতিটি apartment-এর নিজস্ব furniture — একটির পরিবর্তন অন্যটিতে effect করে না।

**Essential Commands:**

```bash
# Create
python3 -m venv venv

# Activate
source venv/bin/activate        # Linux/macOS
venv\Scripts\activate           # Windows

# Deactivate
deactivate

# Install packages
pip install fastapi uvicorn sqlalchemy

# Save dependencies
pip freeze > requirements.txt

# Install from requirements
pip install -r requirements.txt

# Check installed
pip list
pip show fastapi
```

**requirements.txt best practices:**
```text
# requirements.txt — pinned versions
fastapi==0.115.0
uvicorn[standard]==0.32.0
sqlalchemy==2.0.36
pydantic==2.10.0
python-dotenv==1.0.0

# requirements-dev.txt — dev only
pytest==8.3.0
pytest-cov==6.0.0
black==24.10.0
flake8==7.1.1
```

**Interview-style Explanation:**
> "প্রতিটি project-এ `venv` তৈরি করি — system Python dirty করা উচিত নয়। `requirements.txt`-এ exact version pin করি production-এ। `.venv` folder সবসময় `.gitignore`-এ রাখি।"

**Common Mistakes:**
- `venv` folder git-এ commit করা — `.gitignore`-এ add করুন
- `requirements.txt` update না রাখা — নতুন package install করলে freeze করুন
- exact version pin না করা — `fastapi` নয়, `fastapi==0.115.0`

---

<a id="p9-structure"></a>

## 7. Project Structure

**Definition:**
Standard project structure Python project-কে maintainable, scalable করে। Packaging, testing, configuration আলাদা রাখা হয়।

**Standard Layout:**
```text
my_project/
├── src/
│   └── my_app/
│       ├── __init__.py
│       ├── main.py
│       ├── models/
│       │   ├── __init__.py
│       │   └── user.py
│       ├── services/
│       │   ├── __init__.py
│       │   └── user_service.py
│       ├── routers/
│       │   ├── __init__.py
│       │   └── users.py
│       └── utils/
│           └── helpers.py
├── tests/
│   ├── conftest.py
│   ├── test_models.py
│   └── test_services.py
├── .env
├── .env.example          ← commit এটি, .env নয়
├── .gitignore
├── requirements.txt
├── requirements-dev.txt
├── README.md
└── pyproject.toml        ← modern project config
```

**`.gitignore` essentials:**
```text
# Python
__pycache__/
*.py[cod]
*.egg-info/
dist/
build/

# Virtual env
venv/
.venv/
env/

# Environment
.env
*.env

# IDE
.vscode/
.idea/

# Testing
.pytest_cache/
.coverage
htmlcov/
```

---

<a id="p9-git"></a>

## 8. Git Workflow

**Definition:**
Git workflow হলো team-এ code collaborate করার systematic approach। Branching strategy, commit messages, code review।

**Conventional Commit Format:**
```text
<type>(<scope>): <short description>

feat(auth): add JWT token refresh endpoint
fix(payment): handle bKash timeout gracefully
docs(readme): update installation instructions
test(user): add unit tests for user service
refactor(db): extract connection pool setup
chore(deps): upgrade fastapi to 0.115.0
```

**Common Branch Strategy:**
```text
main          ← production-ready
develop       ← integration branch
feature/xxx   ← new feature
bugfix/xxx    ← bug fix
hotfix/xxx    ← urgent production fix
```

**Interview-style Explanation:**
> "Conventional commits দিয়ে changelog auto-generate করা যায়। `git rebase` করি feature branch-কে main-এর উপরে রাখতে। `git stash` দিয়ে incomplete work সাময়িক সরিয়ে রাখি। Squash commit করি PR merge-এর আগে।"

**Essential Git Commands:**
```bash
# Branch
git checkout -b feature/user-auth
git branch -d feature/user-auth

# Stash
git stash push -m "WIP: user auth"
git stash pop

# Rebase (keep history clean)
git fetch origin
git rebase origin/main

# Interactive rebase — squash commits
git rebase -i HEAD~3

# Undo last commit (keep changes)
git reset HEAD~1 --soft

# Check what changed
git diff HEAD
git log --oneline --graph -10
```

---

## PART 9 Quick Revision Table

| Topic | Key Takeaway | Interview Must-Know |
|---|---|---|
| unittest | `TestCase`, `setUp`/`tearDown` | `assertRaises()`, `assert*` methods |
| pytest | Fixtures, parametrize, plain assert | `conftest.py`, `--cov` flag |
| Mocking | Replace external deps in tests | `patch()` path = where imported |
| PEP 8 | Naming, spacing, import order | `black` auto-formatter |
| Clean Code | Readable names, small functions, no magic numbers | Guard clause / early return |
| venv | Isolated environment per project | `.gitignore` venv, pin versions |
| Project Structure | src/, tests/, conftest.py | `.env.example` commit, `.env` no |
| Git | Conventional commits, branching | `rebase` vs `merge`, `stash` |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part10"></a>

## 📋 PART 10 সূচিপত্র — Python Projects

| # | Project | Skills Practiced |
|---|---|---|
| 1 | [Student Management CLI](#p10-student-mgmt) | OOP, file I/O, JSON, CRUD |
| 2 | [CLI Todo App](#p10-todo) | argparse, JSON persistence, clean code |
| 3 | [File Organizer Script](#p10-organizer) | os, shutil, pathlib, automation |
| 4 | [Weather CLI App](#p10-weather) | requests, API integration, error handling |
| 5 | [REST API with FastAPI](#p10-rest-api) | FastAPI, Pydantic, SQLAlchemy, CRUD |
| 6 | [JWT Auth System](#p10-auth) | FastAPI, JWT, hashing, middleware |
| 7 | [Web Scraper](#p10-scraper) | requests, BeautifulSoup, CSV export |
| 8 | [Task Automation Script](#p10-automation) | subprocess, schedule, logging |

---

<a id="p10-student-mgmt"></a>

## 1. Student Management CLI

**Skills:** OOP, JSON persistence, CRUD, input validation

**Project Overview:**
Terminal-based student management system — add, list, search, update, delete student records। JSON file-এ data persist করা।

```python
# student_manager.py
import json
import os
from dataclasses import dataclass, asdict
from typing import Optional
from pathlib import Path

DATA_FILE = Path("students.json")


@dataclass
class Student:
    student_id: str
    name: str
    age: int
    department: str
    gpa: float

    def __post_init__(self):
        if not (0.0 <= self.gpa <= 4.0):
            raise ValueError(f"GPA must be 0.0–4.0, got {self.gpa}")
        if self.age < 16 or self.age > 60:
            raise ValueError(f"Invalid age: {self.age}")


class StudentManager:
    def __init__(self):
        self._students: dict[str, Student] = {}
        self._load()

    def _load(self):
        if DATA_FILE.exists():
            with open(DATA_FILE, encoding="utf-8") as f:
                data = json.load(f)
                self._students = {
                    sid: Student(**info) for sid, info in data.items()
                }

    def _save(self):
        with open(DATA_FILE, "w", encoding="utf-8") as f:
            json.dump(
                {sid: asdict(s) for sid, s in self._students.items()},
                f, indent=2, ensure_ascii=False
            )

    def add(self, student: Student) -> bool:
        if student.student_id in self._students:
            print(f"Student {student.student_id} already exists")
            return False
        self._students[student.student_id] = student
        self._save()
        return True

    def get(self, student_id: str) -> Optional[Student]:
        return self._students.get(student_id)

    def list_all(self, dept: str = None) -> list[Student]:
        students = list(self._students.values())
        if dept:
            students = [s for s in students if s.department == dept]
        return sorted(students, key=lambda s: s.name)

    def update_gpa(self, student_id: str, new_gpa: float) -> bool:
        student = self._students.get(student_id)
        if not student:
            return False
        if not (0.0 <= new_gpa <= 4.0):
            raise ValueError("Invalid GPA")
        student.gpa = new_gpa
        self._save()
        return True

    def delete(self, student_id: str) -> bool:
        if student_id not in self._students:
            return False
        del self._students[student_id]
        self._save()
        return True

    def search(self, query: str) -> list[Student]:
        q = query.lower()
        return [
            s for s in self._students.values()
            if q in s.name.lower() or q in s.department.lower()
        ]

    def top_students(self, n: int = 5) -> list[Student]:
        return sorted(
            self._students.values(), key=lambda s: s.gpa, reverse=True
        )[:n]


def print_student(s: Student):
    print(f"  [{s.student_id}] {s.name} | {s.department} | Age: {s.age} | GPA: {s.gpa:.2f}")


def main():
    mgr = StudentManager()
    while True:
        print("\n=== Student Management System ===")
        print("1. Add Student  2. List All  3. Search")
        print("4. Update GPA   5. Delete    6. Top Students  0. Exit")
        choice = input("Choice: ").strip()

        if choice == "1":
            try:
                s = Student(
                    student_id=input("ID: ").strip(),
                    name=input("Name: ").strip(),
                    age=int(input("Age: ")),
                    department=input("Dept: ").strip(),
                    gpa=float(input("GPA (0.0–4.0): "))
                )
                if mgr.add(s):
                    print(f"Added: {s.name}")
            except ValueError as e:
                print(f"Error: {e}")

        elif choice == "2":
            dept = input("Filter by dept (Enter to skip): ").strip() or None
            students = mgr.list_all(dept)
            for s in students:
                print_student(s)
            print(f"Total: {len(students)}")

        elif choice == "3":
            query = input("Search name/dept: ").strip()
            for s in mgr.search(query):
                print_student(s)

        elif choice == "4":
            sid = input("Student ID: ").strip()
            try:
                gpa = float(input("New GPA: "))
                print("Updated" if mgr.update_gpa(sid, gpa) else "Not found")
            except ValueError as e:
                print(f"Error: {e}")

        elif choice == "5":
            sid = input("Student ID to delete: ").strip()
            print("Deleted" if mgr.delete(sid) else "Not found")

        elif choice == "6":
            for s in mgr.top_students(5):
                print_student(s)

        elif choice == "0":
            print("Goodbye!")
            break


if __name__ == "__main__":
    main()
```

---

<a id="p10-todo"></a>

## 2. CLI Todo App

**Skills:** `argparse`, JSON persistence, dataclasses, clean code

```python
# todo.py — run: python todo.py add "Buy groceries" --priority high
import json
import argparse
from dataclasses import dataclass, asdict, field
from pathlib import Path
from datetime import datetime
from enum import Enum

DATA_FILE = Path.home() / ".todo_data.json"


class Priority(str, Enum):
    LOW = "low"
    MEDIUM = "medium"
    HIGH = "high"


@dataclass
class Todo:
    id: int
    title: str
    priority: str = Priority.MEDIUM
    done: bool = False
    created_at: str = field(default_factory=lambda: datetime.now().isoformat())


class TodoStore:
    def __init__(self):
        self.todos: list[Todo] = []
        self._next_id = 1
        self._load()

    def _load(self):
        if DATA_FILE.exists():
            data = json.loads(DATA_FILE.read_text(encoding="utf-8"))
            self.todos = [Todo(**t) for t in data]
            self._next_id = max((t.id for t in self.todos), default=0) + 1

    def _save(self):
        DATA_FILE.write_text(
            json.dumps([asdict(t) for t in self.todos], indent=2),
            encoding="utf-8"
        )

    def add(self, title: str, priority: str = "medium") -> Todo:
        todo = Todo(id=self._next_id, title=title, priority=priority)
        self.todos.append(todo)
        self._next_id += 1
        self._save()
        return todo

    def complete(self, todo_id: int) -> bool:
        for t in self.todos:
            if t.id == todo_id:
                t.done = True
                self._save()
                return True
        return False

    def delete(self, todo_id: int) -> bool:
        original = len(self.todos)
        self.todos = [t for t in self.todos if t.id != todo_id]
        if len(self.todos) < original:
            self._save()
            return True
        return False

    def list_todos(self, show_done: bool = False) -> list[Todo]:
        items = self.todos if show_done else [t for t in self.todos if not t.done]
        priority_order = {"high": 0, "medium": 1, "low": 2}
        return sorted(items, key=lambda t: priority_order.get(t.priority, 1))


def format_todo(t: Todo) -> str:
    status = "✅" if t.done else "⬜"
    priority_icons = {"high": "🔴", "medium": "🟡", "low": "🟢"}
    icon = priority_icons.get(t.priority, "⬜")
    return f"  [{t.id}] {status} {icon} {t.title}"


def build_parser() -> argparse.ArgumentParser:
    parser = argparse.ArgumentParser(description="CLI Todo App")
    sub = parser.add_subparsers(dest="command")

    add_p = sub.add_parser("add", help="Add a new todo")
    add_p.add_argument("title", help="Todo title")
    add_p.add_argument("--priority", choices=["low","medium","high"],
                       default="medium")

    done_p = sub.add_parser("done", help="Mark todo as complete")
    done_p.add_argument("id", type=int)

    del_p = sub.add_parser("delete", help="Delete a todo")
    del_p.add_argument("id", type=int)

    list_p = sub.add_parser("list", help="List todos")
    list_p.add_argument("--all", action="store_true", help="Include done items")

    return parser


def main():
    parser = build_parser()
    args = parser.parse_args()
    store = TodoStore()

    if args.command == "add":
        todo = store.add(args.title, args.priority)
        print(f"Added: {format_todo(todo)}")

    elif args.command == "done":
        print("Marked done!" if store.complete(args.id) else "Not found")

    elif args.command == "delete":
        print("Deleted!" if store.delete(args.id) else "Not found")

    elif args.command == "list":
        todos = store.list_todos(show_done=args.all)
        if not todos:
            print("No todos!")
        for t in todos:
            print(format_todo(t))
        print(f"\n{len(todos)} item(s)")

    else:
        parser.print_help()


if __name__ == "__main__":
    main()
```

---

<a id="p10-organizer"></a>

## 3. File Organizer Script

**Skills:** `pathlib`, `shutil`, automation, logging

```python
# organizer.py — python organizer.py ~/Downloads
import argparse
import logging
import shutil
from pathlib import Path
from datetime import datetime

logging.basicConfig(
    level=logging.INFO,
    format="%(asctime)s %(levelname)s %(message)s",
    datefmt="%H:%M:%S"
)
logger = logging.getLogger(__name__)

FOLDER_MAP = {
    "Images":    {".jpg",".jpeg",".png",".gif",".webp",".svg",".bmp"},
    "Documents": {".pdf",".docx",".doc",".txt",".pptx",".xlsx",".odt"},
    "Data":      {".csv",".json",".xml",".yaml",".yml",".sql"},
    "Code":      {".py",".js",".ts",".html",".css",".java",".cpp",".go"},
    "Archives":  {".zip",".tar",".gz",".rar",".7z"},
    "Videos":    {".mp4",".mkv",".avi",".mov",".wmv"},
    "Audio":     {".mp3",".wav",".flac",".aac",".ogg"},
}

def build_ext_map() -> dict[str, str]:
    return {ext: folder for folder, exts in FOLDER_MAP.items() for ext in exts}

def unique_path(dest_dir: Path, filename: str) -> Path:
    stem = Path(filename).stem
    suffix = Path(filename).suffix
    dest = dest_dir / filename
    counter = 1
    while dest.exists():
        dest = dest_dir / f"{stem}_{counter}{suffix}"
        counter += 1
    return dest

def organize(source_dir: str, dry_run: bool = False) -> dict:
    source = Path(source_dir).expanduser().resolve()
    if not source.is_dir():
        raise ValueError(f"Not a directory: {source}")

    ext_map = build_ext_map()
    stats = {"moved": 0, "skipped": 0, "errors": 0}

    for file in source.iterdir():
        if not file.is_file():
            continue
        if file.name.startswith("."):
            continue

        folder = ext_map.get(file.suffix.lower(), "Others")
        dest_dir = source / folder
        dest = unique_path(dest_dir, file.name)

        if dry_run:
            logger.info(f"[DRY RUN] {file.name} → {folder}/")
            stats["moved"] += 1
            continue

        try:
            dest_dir.mkdir(exist_ok=True)
            shutil.move(str(file), str(dest))
            logger.info(f"Moved: {file.name} → {folder}/")
            stats["moved"] += 1
        except Exception as e:
            logger.error(f"Failed to move {file.name}: {e}")
            stats["errors"] += 1

    return stats


if __name__ == "__main__":
    parser = argparse.ArgumentParser(description="Organize files by type")
    parser.add_argument("directory", help="Directory to organize")
    parser.add_argument("--dry-run", action="store_true",
                        help="Preview without moving")
    args = parser.parse_args()

    stats = organize(args.directory, dry_run=args.dry_run)
    print(f"\nDone: moved={stats['moved']}, errors={stats['errors']}")
```

---

<a id="p10-weather"></a>

## 4. Weather CLI App

**Skills:** `requests`, API integration, error handling, argparse

```python
# weather.py — python weather.py Dhaka
# Uses OpenWeatherMap free API (api.openweathermap.org)
import os
import sys
import argparse
import requests
from dotenv import load_dotenv

load_dotenv()

API_KEY = os.environ.get("OPENWEATHER_API_KEY", "")
BASE_URL = "https://api.openweathermap.org/data/2.5"

def get_weather(city: str, units: str = "metric") -> dict:
    if not API_KEY:
        raise RuntimeError("OPENWEATHER_API_KEY not set in .env")
    response = requests.get(
        f"{BASE_URL}/weather",
        params={"q": city, "appid": API_KEY, "units": units},
        timeout=10
    )
    if response.status_code == 404:
        raise ValueError(f"City not found: {city}")
    response.raise_for_status()
    return response.json()

def display_weather(data: dict, units: str):
    unit_sym = "°C" if units == "metric" else "°F"
    city = data["name"]
    country = data["sys"]["country"]
    temp = data["main"]["temp"]
    feels_like = data["main"]["feels_like"]
    humidity = data["main"]["humidity"]
    description = data["weather"][0]["description"].title()
    wind = data["wind"]["speed"]

    print(f"\n{'='*35}")
    print(f"  📍 {city}, {country}")
    print(f"  🌡  Temperature : {temp}{unit_sym} (feels like {feels_like}{unit_sym})")
    print(f"  💧 Humidity    : {humidity}%")
    print(f"  🌬  Wind        : {wind} m/s")
    print(f"  ☁  Condition   : {description}")
    print(f"{'='*35}\n")

def main():
    parser = argparse.ArgumentParser(description="Weather CLI")
    parser.add_argument("city", help="City name (e.g., Dhaka)")
    parser.add_argument("--units", choices=["metric","imperial"],
                        default="metric")
    args = parser.parse_args()

    try:
        data = get_weather(args.city, args.units)
        display_weather(data, args.units)
    except ValueError as e:
        print(f"Error: {e}")
        sys.exit(1)
    except requests.exceptions.ConnectionError:
        print("Error: No internet connection")
        sys.exit(1)
    except RuntimeError as e:
        print(f"Config error: {e}")
        sys.exit(1)

if __name__ == "__main__":
    main()
```

---

<a id="p10-rest-api"></a>

## 5. REST API with FastAPI

**Skills:** FastAPI, Pydantic, SQLAlchemy, CRUD, error handling

```python
# main.py — uvicorn main:app --reload
from fastapi import FastAPI, Depends, HTTPException, status
from sqlalchemy import create_engine, Column, Integer, String, Float, Boolean
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker, Session
from pydantic import BaseModel, field_validator
from typing import Optional
import os

DATABASE_URL = os.environ.get("DATABASE_URL", "sqlite:///./products.db")
engine = create_engine(DATABASE_URL, connect_args={"check_same_thread": False})
SessionLocal = sessionmaker(autocommit=False, autoflush=False, bind=engine)
Base = declarative_base()

# ──── Model ────
class ProductDB(Base):
    __tablename__ = "products"
    id = Column(Integer, primary_key=True, index=True)
    name = Column(String, nullable=False, index=True)
    price = Column(Float, nullable=False)
    stock = Column(Integer, default=0)
    active = Column(Boolean, default=True)

Base.metadata.create_all(bind=engine)

# ──── Schemas ────
class ProductCreate(BaseModel):
    name: str
    price: float
    stock: int = 0

    @field_validator("price")
    @classmethod
    def price_positive(cls, v):
        if v <= 0:
            raise ValueError("Price must be positive")
        return round(v, 2)

class ProductUpdate(BaseModel):
    name: Optional[str] = None
    price: Optional[float] = None
    stock: Optional[int] = None

class ProductResponse(BaseModel):
    id: int
    name: str
    price: float
    stock: int
    active: bool

    class Config:
        from_attributes = True

# ──── Dependency ────
def get_db():
    db = SessionLocal()
    try:
        yield db
    finally:
        db.close()

# ──── App ────
app = FastAPI(title="Products API", version="1.0.0")

@app.get("/products", response_model=list[ProductResponse])
def list_products(
    skip: int = 0,
    limit: int = 20,
    db: Session = Depends(get_db)
):
    return db.query(ProductDB).filter(
        ProductDB.active == True
    ).offset(skip).limit(limit).all()

@app.post("/products", response_model=ProductResponse,
          status_code=status.HTTP_201_CREATED)
def create_product(product: ProductCreate, db: Session = Depends(get_db)):
    db_product = ProductDB(**product.model_dump())
    db.add(db_product)
    db.commit()
    db.refresh(db_product)
    return db_product

@app.get("/products/{product_id}", response_model=ProductResponse)
def get_product(product_id: int, db: Session = Depends(get_db)):
    product = db.query(ProductDB).filter(ProductDB.id == product_id).first()
    if not product:
        raise HTTPException(status_code=404, detail="Product not found")
    return product

@app.patch("/products/{product_id}", response_model=ProductResponse)
def update_product(
    product_id: int,
    updates: ProductUpdate,
    db: Session = Depends(get_db)
):
    product = db.query(ProductDB).filter(ProductDB.id == product_id).first()
    if not product:
        raise HTTPException(status_code=404, detail="Product not found")
    for key, value in updates.model_dump(exclude_unset=True).items():
        setattr(product, key, value)
    db.commit()
    db.refresh(product)
    return product

@app.delete("/products/{product_id}", status_code=status.HTTP_204_NO_CONTENT)
def delete_product(product_id: int, db: Session = Depends(get_db)):
    product = db.query(ProductDB).filter(ProductDB.id == product_id).first()
    if not product:
        raise HTTPException(status_code=404, detail="Product not found")
    product.active = False   # soft delete
    db.commit()
```

---

<a id="p10-auth"></a>

## 6. JWT Auth System

**Skills:** FastAPI, JWT, bcrypt password hashing, OAuth2

```python
# auth.py — JWT authentication with FastAPI
from fastapi import FastAPI, Depends, HTTPException, status
from fastapi.security import OAuth2PasswordBearer, OAuth2PasswordRequestForm
from jose import JWTError, jwt
from passlib.context import CryptContext
from pydantic import BaseModel
from datetime import datetime, timedelta
from typing import Optional
import os

# ──── Config ────
SECRET_KEY = os.environ.get("SECRET_KEY", "change-this-in-production")
ALGORITHM = "HS256"
ACCESS_TOKEN_EXPIRE_MINUTES = 30

# ──── Security ────
pwd_context = CryptContext(schemes=["bcrypt"], deprecated="auto")
oauth2_scheme = OAuth2PasswordBearer(tokenUrl="/auth/login")

def hash_password(password: str) -> str:
    return pwd_context.hash(password)

def verify_password(plain: str, hashed: str) -> bool:
    return pwd_context.verify(plain, hashed)

def create_access_token(data: dict, expires_delta: Optional[timedelta] = None):
    to_encode = data.copy()
    expire = datetime.utcnow() + (expires_delta or timedelta(minutes=15))
    to_encode["exp"] = expire
    return jwt.encode(to_encode, SECRET_KEY, algorithm=ALGORITHM)

# ──── Fake DB ────
USERS_DB = {
    "rahim": {
        "username": "rahim",
        "hashed_password": hash_password("secret123"),
        "email": "rahim@example.com",
        "role": "user",
    }
}

# ──── Schemas ────
class Token(BaseModel):
    access_token: str
    token_type: str

class UserResponse(BaseModel):
    username: str
    email: str
    role: str

# ──── Auth dependency ────
async def get_current_user(token: str = Depends(oauth2_scheme)) -> dict:
    credentials_exception = HTTPException(
        status_code=status.HTTP_401_UNAUTHORIZED,
        detail="Could not validate credentials",
        headers={"WWW-Authenticate": "Bearer"},
    )
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=[ALGORITHM])
        username: str = payload.get("sub")
        if username is None:
            raise credentials_exception
    except JWTError:
        raise credentials_exception

    user = USERS_DB.get(username)
    if not user:
        raise credentials_exception
    return user

# ──── App ────
app = FastAPI(title="Auth API")

@app.post("/auth/login", response_model=Token)
async def login(form_data: OAuth2PasswordRequestForm = Depends()):
    user = USERS_DB.get(form_data.username)
    if not user or not verify_password(form_data.password, user["hashed_password"]):
        raise HTTPException(
            status_code=status.HTTP_401_UNAUTHORIZED,
            detail="Incorrect username or password",
            headers={"WWW-Authenticate": "Bearer"},
        )
    token = create_access_token(
        data={"sub": user["username"]},
        expires_delta=timedelta(minutes=ACCESS_TOKEN_EXPIRE_MINUTES)
    )
    return {"access_token": token, "token_type": "bearer"}

@app.get("/me", response_model=UserResponse)
async def get_me(current_user: dict = Depends(get_current_user)):
    return current_user

@app.get("/protected")
async def protected_route(current_user: dict = Depends(get_current_user)):
    return {"message": f"Hello {current_user['username']}! This is protected."}
```

---

<a id="p10-scraper"></a>

## 7. Web Scraper

**Skills:** `requests`, `BeautifulSoup`, CSV export, rate limiting

```python
# scraper.py — Scrape quotes.toscrape.com and export to CSV
import csv
import time
import logging
import requests
from bs4 import BeautifulSoup
from dataclasses import dataclass, fields, astuple
from pathlib import Path

logging.basicConfig(level=logging.INFO, format="%(asctime)s %(message)s")
logger = logging.getLogger(__name__)

BASE_URL = "http://quotes.toscrape.com"
OUTPUT_FILE = Path("quotes.csv")
DELAY_SECONDS = 1.0


@dataclass
class Quote:
    text: str
    author: str
    tags: str   # comma-joined


def scrape_page(url: str, session: requests.Session) -> tuple[list[Quote], str | None]:
    response = session.get(url, timeout=10)
    response.raise_for_status()
    soup = BeautifulSoup(response.text, "html.parser")

    quotes = []
    for div in soup.find_all("div", class_="quote"):
        text = div.find("span", class_="text").get_text(strip=True)
        author = div.find("small", class_="author").get_text(strip=True)
        tags = ",".join(t.get_text() for t in div.find_all("a", class_="tag"))
        quotes.append(Quote(text=text, author=author, tags=tags))

    next_li = soup.find("li", class_="next")
    next_url = BASE_URL + next_li.find("a")["href"] if next_li else None
    return quotes, next_url


def save_to_csv(quotes: list[Quote], path: Path):
    with open(path, "w", newline="", encoding="utf-8") as f:
        writer = csv.writer(f)
        writer.writerow([field.name for field in fields(Quote)])
        for q in quotes:
            writer.writerow(astuple(q))
    logger.info(f"Saved {len(quotes)} quotes to {path}")


def scrape_all() -> list[Quote]:
    all_quotes = []
    url = BASE_URL
    page = 1

    with requests.Session() as session:
        session.headers.update({"User-Agent": "QuoteScraper/1.0"})

        while url:
            logger.info(f"Scraping page {page}: {url}")
            try:
                quotes, url = scrape_page(url, session)
                all_quotes.extend(quotes)
                logger.info(f"  Found {len(quotes)} quotes")
            except requests.RequestException as e:
                logger.error(f"Request failed: {e}")
                break

            page += 1
            if url:
                time.sleep(DELAY_SECONDS)   # polite delay

    return all_quotes


if __name__ == "__main__":
    quotes = scrape_all()
    save_to_csv(quotes, OUTPUT_FILE)
    print(f"\nTotal quotes scraped: {len(quotes)}")
    print(f"Saved to: {OUTPUT_FILE}")
```

---

<a id="p10-automation"></a>

## 8. Task Automation Script

**Skills:** `subprocess`, `schedule`, `logging`, `pathlib`, system automation

```python
# automation.py — Daily automation: backup, health check, log cleanup
import schedule
import time
import shutil
import logging
import subprocess
from datetime import datetime
from pathlib import Path

# ──── Logging ────
LOG_DIR = Path("logs")
LOG_DIR.mkdir(exist_ok=True)

logging.basicConfig(
    level=logging.INFO,
    format="%(asctime)s [%(levelname)s] %(message)s",
    handlers=[
        logging.FileHandler(LOG_DIR / "automation.log", encoding="utf-8"),
        logging.StreamHandler()
    ]
)
logger = logging.getLogger(__name__)

# ──── Config ────
BACKUP_SOURCE = Path("data")
BACKUP_DEST = Path("backups")
LOG_RETENTION_DAYS = 7
API_ENDPOINT = "http://localhost:8000/health"


# ──── Tasks ────
def daily_backup():
    """Daily zip backup of data directory"""
    if not BACKUP_SOURCE.exists():
        logger.warning(f"Source not found: {BACKUP_SOURCE}")
        return

    BACKUP_DEST.mkdir(exist_ok=True)
    timestamp = datetime.now().strftime("%Y-%m-%d_%H-%M")
    archive = BACKUP_DEST / f"backup_{timestamp}"

    try:
        shutil.make_archive(str(archive), "zip", str(BACKUP_SOURCE))
        size = archive.with_suffix(".zip").stat().st_size
        logger.info(f"Backup created: {archive}.zip ({size:,} bytes)")
    except Exception as e:
        logger.error(f"Backup failed: {e}")


def clean_old_logs():
    """Delete logs older than retention period"""
    cutoff = time.time() - (LOG_RETENTION_DAYS * 86400)
    deleted = 0
    for log_file in LOG_DIR.glob("*.log.*"):   # rotated logs
        if log_file.stat().st_mtime < cutoff:
            log_file.unlink()
            deleted += 1
    logger.info(f"Log cleanup: {deleted} old files removed")


def api_health_check():
    """Ping local API and log status"""
    try:
        import requests
        resp = requests.get(API_ENDPOINT, timeout=5)
        if resp.status_code == 200:
            logger.info(f"Health check OK: {API_ENDPOINT}")
        else:
            logger.warning(f"Health check returned {resp.status_code}")
    except Exception as e:
        logger.error(f"Health check FAILED: {e}")


def git_auto_commit():
    """Auto-commit any changes in current repo"""
    try:
        status = subprocess.run(
            ["git", "status", "--porcelain"],
            capture_output=True, text=True, check=True
        )
        if not status.stdout.strip():
            logger.info("No git changes to commit")
            return
        subprocess.run(["git", "add", "-A"], check=True)
        msg = f"auto: scheduled backup {datetime.now().strftime('%Y-%m-%d %H:%M')}"
        subprocess.run(["git", "commit", "-m", msg], check=True)
        logger.info(f"Auto-committed: {msg}")
    except subprocess.CalledProcessError as e:
        logger.error(f"Git commit failed: {e}")


def system_report():
    """Log basic system info"""
    try:
        disk = shutil.disk_usage("/")
        used_pct = disk.used / disk.total * 100
        if used_pct > 90:
            logger.warning(f"Disk usage high: {used_pct:.1f}%")
        else:
            logger.info(f"Disk usage: {used_pct:.1f}%")
    except Exception as e:
        logger.error(f"System report failed: {e}")


# ──── Schedule ────
schedule.every().day.at("02:00").do(daily_backup)
schedule.every().day.at("03:00").do(clean_old_logs)
schedule.every(5).minutes.do(api_health_check)
schedule.every().hour.do(system_report)
# schedule.every().day.at("23:55").do(git_auto_commit)

logger.info("Automation scheduler started")
logger.info(f"Next backup at 02:00 | Health check every 5 min")

if __name__ == "__main__":
    # Run once immediately on start
    system_report()
    api_health_check()

    while True:
        schedule.run_pending()
        time.sleep(30)
```

---

## PART 10 Quick Revision Table

| Project | Core Skills | Key Takeaway |
|---|---|---|
| Student Management | OOP, dataclass, JSON CRUD | `dataclass` + `asdict()` for JSON |
| CLI Todo | argparse, Enum, persistence | `argparse` subcommands |
| File Organizer | pathlib, shutil, automation | `shutil.move()`, duplicate handling |
| Weather App | requests, .env, error handling | API key from env, `raise_for_status()` |
| REST API | FastAPI, Pydantic, SQLAlchemy | Soft delete, `Depends()`, validators |
| JWT Auth | bcrypt, JWT, OAuth2 | `passlib`, `python-jose`, `OAuth2PasswordBearer` |
| Web Scraper | bs4, CSV, polite scraping | `time.sleep()`, `User-Agent` header |
| Task Automation | schedule, subprocess, logging | `schedule.run_pending()` loop |

---

## PART 10 Interview Tips

**Project-based questions:** Bangladesh-এর interview-এ প্রায়ই জিজ্ঞেস করা হয়:

1. **"আপনার কোনো personal project আছে?"** → এই projects GitHub-এ upload করুন, README ভালো করে লিখুন।

2. **"Biggest challenge কী ছিল project-এ?"** → Authentication-এ JWT refresh token handle করা, database relation setup করা।

3. **"কীভাবে deploy করেছেন?"** → FastAPI project → Render/Railway/DigitalOcean, Docker container।

4. **"Testing করেছেন?"** → pytest দিয়ে unit test, coverage ৮০%+ রাখার চেষ্টা।

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part11"></a>

## 📋 PART 11 সূচিপত্র — Python Interview Questions Bank

| # | Section | Questions |
|---|---|---|
| 1 | [Theoretical Questions](#p11-theory) | 60 প্রশ্ন — সব topic cover |
| 2 | [Coding Questions](#p11-coding) | 30 প্রশ্ন — easy/medium/hard with solutions |
| 3 | [Tricky Python Questions](#p11-tricky) | 20 gotcha questions |
| 4 | [Rapid-fire Q&A](#p11-rapid) | 20 one-liner answers |
| 5 | [Scenario-based Questions](#p11-scenario) | 20 real project situations |

---

<a id="p11-theory"></a>

## 1. Theoretical Questions (60টি)

**Python Basics (১–১০)**

**1. Python-এ `is` আর `==` পার্থক্য কী?**
> `==` value comparison করে, `is` identity comparison করে (same object কিনা memory-তে)। `a = [1,2]; b = [1,2]` → `a == b` True কিন্তু `a is b` False।

**2. Mutable আর Immutable type-এর পার্থক্য বলুন। উদাহরণ দিন।**
> Mutable: list, dict, set — পরিবর্তন করা যায়। Immutable: int, str, tuple, frozenset — পরিবর্তন করলে নতুন object তৈরি হয়। String immutable বলেই string concatenation loop-এ slow।

**3. `*args` আর `**kwargs` কী?**
> `*args` variable positional arguments tuple হিসেবে নেয়। `**kwargs` variable keyword arguments dict হিসেবে নেয়। Function signature: `def func(*args, **kwargs)`।

**4. Python-এ `None` কী? কখন use করবেন?**
> `None` হলো Python-এর null value। Type: `NoneType`। Function কিছু return না করলে implicitly `None` return করে। Optional value indicate করতে use করি। Check: `if x is None` (not `if x == None`)।

**5. List comprehension আর `map()` কখন use করবেন?**
> Readable, simple transformation-এ list comprehension। Complex function বা existing function apply করতে `map()`। Performance প্রায় same। Comprehension generally more Pythonic।

**6. `__init__` আর `__new__` পার্থক্য?**
> `__new__` object তৈরি করে (allocate memory), `__init__` সেই object initialize করে। সাধারণত শুধু `__init__` override করি। Singleton pattern বা immutable type subclass করতে `__new__` দরকার।

**7. Python-এ `global` আর `nonlocal` keyword কী?**
> `global` function-এর ভেতর থেকে module-level variable modify করতে। `nonlocal` nested function-এর ভেতর থেকে enclosing scope-এর variable modify করতে।

**8. `del` keyword কী করে?**
> Object-এর reference delete করে। `del x` মানে `x` নামের reference সরে যায়। যদি কোনো reference না থাকে, garbage collector memory free করে। List-এ `del lst[2]` element delete করে।

**9. Python-এ truthiness rules কী কী?**
> Falsy: `None`, `False`, `0`, `0.0`, `""`, `[]`, `{}`, `set()`, `()`. বাকি সব Truthy। `bool([])` → False, `bool([0])` → True।

**10. `__slots__` কী এবং কখন use করবেন?**
> Class-এ `__slots__ = ['x','y']` দিলে per-instance `__dict__` তৈরি হয় না — memory বাঁচে। Millions of instances তৈরি হলে use করুন। Downside: dynamic attribute add করা যায় না।

---

**OOP (১১–২০)**

**11. Python-এ MRO (Method Resolution Order) কী?**
> Multiple inheritance-এ Python C3 Linearization algorithm দিয়ে কোন class-এর method আগে check করবে তা ঠিক করে। `ClassName.__mro__` বা `mro()` দিয়ে দেখা যায়।

**12. `@classmethod` আর `@staticmethod` পার্থক্য?**
> `@classmethod` first argument `cls` নেয় — class access করতে পারে, subclass-এ override হয়। `@staticmethod` কোনো implicit argument নেয় না — utility function। `@classmethod` alternative constructor pattern-এ use হয়।

**13. Abstract class কী? কীভাবে বানাবেন?**
> Abstract class directly instantiate করা যায় না — subclass-এ implement বাধ্যতামূলক। `from abc import ABC, abstractmethod`। `@abstractmethod` decorator দিয়ে abstract method define করি।

**14. Python-এ `super()` কী করে?**
> Parent class-এর method call করে। Multiple inheritance-এ MRO অনুযায়ী সঠিক parent call করে। `super().__init__()` child class-এর `__init__`-এ parent initialization করে।

**15. Dunder/magic method কী? কয়েকটি উদাহরণ দিন।**
> `__str__`, `__repr__`, `__len__`, `__eq__`, `__lt__`, `__add__`, `__iter__`, `__next__`, `__enter__`, `__exit__`, `__getitem__`. Operator overloading এবং protocol implementation-এ use হয়।

**16. Composition আর Inheritance পার্থক্য? কখন কোনটি?**
> Inheritance: "is-a" relationship। Composition: "has-a" relationship। Composition more flexible — runtime-এ behavior swap করা যায়। Rule: "Favor composition over inheritance"।

**17. Encapsulation Python-এ কীভাবে implement করবেন?**
> `_single` = convention-based protected। `__double` = name mangling (actual private-ish)। `@property` দিয়ে getter/setter। Python-এ true private নেই — সব accessible।

**18. Duck typing কী?**
> "If it walks like a duck and quacks like a duck, it's a duck." Python-এ object-এর type check না করে behavior check করা। `hasattr()` বা try/except দিয়ে check করা। Protocol-based programming।

**19. Mixin কী?**
> Multiple inheritance-এর একটি pattern — small reusable class যা single specific behavior add করে। Mixin class সাধারণত standalone instantiate হয় না। Example: `LogMixin`, `JSONMixin`, `TimestampMixin`।

**20. `__repr__` আর `__str__` পার্থক্য?**
> `__repr__` developer-friendly (eval করলে object recreate হওয়া উচিত)। `__str__` user-friendly readable string। `print()` `__str__` call করে। Console-এ `repr()` call হয়। Always `__repr__` define করুন।

---

**Functional Python (২১–৩০)**

**21. Closure কী? Example দিন।**
> Inner function outer function-এর variable remember করে enclosing scope। Variable সেই function return হওয়ার পরেও বেঁচে থাকে।
```python
def counter(start=0):
    count = [start]
    def increment():
        count[0] += 1
        return count[0]
    return increment
c = counter(10)
print(c())  # 11
```

**22. Decorator কীভাবে কাজ করে?**
> Function take করে, নতুন wrapped function return করে। `@decorator` syntax sugar for `func = decorator(func)`। `functools.wraps` দিয়ে metadata preserve করি।

**23. Generator আর Iterator পার্থক্য?**
> Iterator: `__iter__` + `__next__` implement করা যেকোনো object। Generator: `yield` ব্যবহার করে lazy evaluation করে — automatically iterator। `yield from` দিয়ে sub-generator delegate করা যায়।

**24. `map()`, `filter()`, `reduce()` কীভাবে কাজ করে?**
> `map(func, iter)` — প্রতিটি element-এ function apply। `filter(func, iter)` — True return করা elements রাখে। `reduce(func, iter)` — cumulative result (from `functools`)।

**25. Lambda function কী? সীমাবদ্ধতা?**
> Anonymous single-expression function। `lambda x: x*2`। Limitation: শুধু single expression, no statements (no `if/else` as statement, no loops), no docstring। Complex logic-এ regular function use করুন।

**26. `any()` আর `all()` কীভাবে কাজ করে?**
> `any(iter)` — কোনো একটি Truthy হলে True। `all(iter)` — সব Truthy হলে True। Empty iterable-এ: `any([])` → False, `all([])` → True। Generator expression-এ efficiently use করা যায়।

**27. `zip()` কী করে? `zip_longest` কখন?**
> Multiple iterables একসাথে iterate করে tuple pair বানায়। Shortest iterable-এ stop করে। `itertools.zip_longest(fill_value=None)` different length handle করে।

**28. Partial function কী?**
> `functools.partial(func, arg)` — function-এর কিছু argument pre-fill করে নতুন callable তৈরি করে।
```python
from functools import partial
power_of_2 = partial(pow, 2)
print(power_of_2(10))  # 1024
```

**29. `enumerate()` কখন use করবেন?**
> Index আর value দুটোই দরকার হলে। `for i, val in enumerate(lst):` — range(len()) এর চেয়ে Pythonic। `start` parameter দিয়ে index শুরু customize করা যায়।

**30. Comprehension কি সবসময় list-এর জন্য? Set, Dict comprehension কীভাবে?**
> List: `[x for x in iter]`, Dict: `{k: v for k, v in pairs}`, Set: `{x for x in iter}`, Generator: `(x for x in iter)` — parentheses, no square brackets।

---

**Data Structures & Algorithms (৩১–৪০)**

**31. Python-এ `list` vs `tuple` কখন কোনটি?**
> List: mutable collection, data যখন change হবে। Tuple: immutable, dict key হিসেবে use, function থেকে multiple return, record-like data। Tuple slightly faster।

**32. `dict` এর time complexity কী?**
> Average case: get/set/delete O(1)। Worst case: O(n) (hash collision)। Python 3.7+ dict insertion order maintain করে। `collections.OrderedDict` explicitly ordered।

**33. `set` কীভাবে কাজ করে? কখন use করবেন?**
> Hash table — O(1) lookup। Duplicate remove, membership test (`in`), set operations (union/intersection/difference)। Unhashable type (list) element হিসেবে রাখা যায় না।

**34. `defaultdict` আর `Counter` কীভাবে কাজ করে?**
> `defaultdict(list)` — missing key-এ default value। `Counter(seq)` — frequency counting। `counter.most_common(n)` top-n elements। Both from `collections`।

**35. Heap/Priority Queue Python-এ কীভাবে use করবেন?**
> `import heapq` — min-heap by default। `heapq.heappush(h, item)`, `heapq.heappop(h)`। Max-heap: negate values। `heapq.nlargest(n, iter)`, `heapq.nsmallest(n, iter)`।

**36. Python-এ stack আর queue কীভাবে implement করবেন?**
> Stack: `list` — `append()` push, `pop()` pop। Queue: `collections.deque` — `append()` enqueue, `popleft()` dequeue। List-এ `pop(0)` O(n) — deque O(1)।

**37. Binary search Python-এ?**
> `bisect` module — `bisect.bisect_left(sorted_list, x)` index returns। Manual: classic while loop with `mid = (lo+hi)//2`।

**38. Sorting Python-এ — `sort()` vs `sorted()`?**
> `list.sort()` in-place, returns None। `sorted(iter)` নতুন list return করে, কোনো iterable নিতে পারে। `key=` parameter দিয়ে custom sort। Stable sort (equal elements relative order maintain করে)।

**39. String-এর `join()` কেন concatenation `+` চেয়ে better?**
> `+` string immutable বলে প্রতিবার নতুন string তৈরি করে — O(n²)। `"".join(list)` একবারে করে — O(n)। `"sep".join(["a","b","c"])` → `"a,b,c"` (sep কোনো string)।

**40. Python-এ recursion limit কত? কীভাবে change করবেন?**
> Default 1000। `sys.getrecursionlimit()`। `sys.setrecursionlimit(10000)` বাড়ানো যায়। Deep recursion-এ stack overflow। Iterative বা tail recursion optimization prefer করুন।

---

**Advanced Python (৪১–৫০)**

**41. GIL (Global Interpreter Lock) কী? CPython-এ কী effect?**
> GIL একটি mutex যা CPython-এ একসময় শুধু একটি thread Python bytecode execute করতে দেয়। CPU-bound task-এ multithreading সাহায্য করে না — `multiprocessing` use করুন। I/O-bound task-এ threading effective।

**42. `threading` vs `multiprocessing` vs `asyncio` কখন কোনটি?**
> Threading: I/O-bound concurrent tasks (GIL issue নেই I/O-তে)। Multiprocessing: CPU-bound parallel tasks (separate Python interpreter)। Asyncio: high-concurrency I/O, single-threaded event loop — best for web servers, API calls।

**43. Context manager কীভাবে কাজ করে?**
> `with` statement — `__enter__` resource acquire, `__exit__` cleanup (error হলেও)। File `close()`, DB commit/rollback, lock release guarantee করে। `contextlib.contextmanager` দিয়ও বানানো যায়।

**44. `async/await` কীভাবে কাজ করে?**
> `async def` coroutine define করে। `await` expression coroutine suspend করে event loop-এ control ফিরিয়ে দেয়। `asyncio.run()` entry point। `asyncio.gather()` multiple coroutine parallel চালায়।

**45. Python memory management কীভাবে কাজ করে?**
> Reference counting — object-এর ref count 0 হলে free। Cyclic garbage collector — circular reference handle করে। `gc` module। Small integer (-5 to 256) আর common string interned হয়।

**46. Descriptor protocol কী?**
> Object যদি `__get__`, `__set__`, `__delete__` implement করে — descriptor। `@property` internally descriptor। Django ORM field, SQLAlchemy column — সব descriptor।

**47. `__call__` কী?**
> Class-এ `__call__` define করলে instance-কে function-এর মতো call করা যায়। `obj()` → `obj.__call__()` invoke হয়। Decorator class, callable object বানাতে use হয়।

**48. Metaclass কী?**
> Class-এর class। সাধারণত `type` metaclass। Custom metaclass দিয়ে class creation control করা যায়। ORM (Django), API framework-এ use হয়। `class Meta:` আর metaclass আলাদা জিনিস।

**49. `__getattr__` vs `__getattribute__` পার্থক্য?**
> `__getattribute__` প্রতিটি attribute access-এ call হয়। `__getattr__` শুধু তখন call হয় যখন normal mechanism attribute খুঁজে পায় না। `__getattr__` overriding safer।

**50. `dataclass` vs `NamedTuple` কখন কোনটি?**
> `dataclass`: mutable, methods add করা যায়, inheritance support, default values, `__post_init__`। `NamedTuple`: immutable, tuple-compatible (unpack, index), slightly faster। Immutable record-এ `NamedTuple`, mutable data model-এ `dataclass`।

---

**Testing, Tools & Web (৫১–৬০)**

**51. Unit test vs Integration test vs E2E test পার্থক্য?**
> Unit: একটি function/method isolated। Integration: multiple component একসাথে (DB + service)। E2E: পুরো system (browser থেকে DB)। Fast unit → slower integration → slowest E2E।

**52. pytest fixture `scope` কী কী আছে?**
> `function` (default), `class`, `module`, `package`, `session`। Scope বড় হলে fixture কম বার create হয় — expensive setup (DB) session scope ব্যবহার করি।

**53. `pip` আর `pip3` পার্থক্য?**
> System-এ Python 2/3 দুটো থাকলে `pip3` explicitly Python 3-এর। Virtual environment activate করার পর `pip` সেই env-এর Python-এর। Best practice: always use venv।

**54. `requirements.txt` আর `pyproject.toml` পার্থক্য?**
> `requirements.txt` simple package list with pins — deployment। `pyproject.toml` modern PEP 517/518 standard — project metadata, build system, tool config (black, pytest, mypy) সব এক জায়গায়।

**55. Type hints Python-এ কীভাবে কাজ করে?**
> Runtime-এ enforce হয় না — documentation এবং static analysis (`mypy`, `pyright`) এর জন্য। `def greet(name: str) -> str:`. `Optional[str]` বা `str | None` (3.10+)।

**56. FastAPI-তে dependency injection কীভাবে কাজ করে?**
> `Depends(func)` — FastAPI automatically `func` call করে result inject করে। DB session, auth, config — সব dependency হিসেবে define করা যায়। Testable, reusable।

**57. SQLAlchemy-তে lazy loading vs eager loading?**
> Lazy: relationship first access-এ additional query। Eager: `joinedload()` বা `selectinload()` — main query-তেই relationship load করে N+1 problem সমাধান করে।

**58. REST API-তে idempotency কী?**
> Same request multiple times করলে same result। GET, PUT, DELETE idempotent। POST generally not idempotent। Idempotent design retry-safe করে।

**59. JWT (JSON Web Token) কীভাবে কাজ করে?**
> Header + Payload + Signature (base64url encoded, `.` separated)। Signature secret key দিয়ে verify করা হয়। Stateless — server session রাখে না। Expiry (`exp` claim) দিয়ে security।

**60. Pydantic validation কীভাবে কাজ করে?**
> Class define করলে `__init__` runtime-এ type coerce + validate করে। Invalid data → `ValidationError`। `@field_validator` custom validation। `model_dump()` dict-এ convert।

---

<a id="p11-coding"></a>

## 2. Coding Questions with Solutions (30টি)

**Easy (১–১০)**

**1. List-এর duplicate remove করুন, order maintain করে।**
```python
def remove_duplicates(lst: list) -> list:
    seen = set()
    return [x for x in lst if not (x in seen or seen.add(x))]

# Test
print(remove_duplicates([3, 1, 4, 1, 5, 9, 2, 6, 5, 3]))
# [3, 1, 4, 5, 9, 2, 6]
```

**2. String-এ প্রতিটি word-এর প্রথম letter capital করুন।**
```python
def title_case(sentence: str) -> str:
    return " ".join(word.capitalize() for word in sentence.split())

print(title_case("hello world from bangladesh"))
# Hello World From Bangladesh
```

**3. Number factorial বের করুন (iterative)।**
```python
def factorial(n: int) -> int:
    if n < 0:
        raise ValueError("Negative input")
    result = 1
    for i in range(2, n + 1):
        result *= i
    return result
```

**4. List-এ দুটো number যোগ করলে target হয় কিনা চেক করুন (Two Sum)।**
```python
def two_sum(nums: list[int], target: int) -> list[int]:
    seen = {}
    for i, num in enumerate(nums):
        complement = target - num
        if complement in seen:
            return [seen[complement], i]
        seen[num] = i
    return []

print(two_sum([2, 7, 11, 15], 9))  # [0, 1]
```

**5. String palindrome কিনা check করুন।**
```python
def is_palindrome(s: str) -> bool:
    cleaned = "".join(c.lower() for c in s if c.isalnum())
    return cleaned == cleaned[::-1]

print(is_palindrome("A man a plan a canal Panama"))  # True
```

**6. List-এর second largest element বের করুন।**
```python
def second_largest(nums: list[int]) -> int | None:
    unique = list(set(nums))
    if len(unique) < 2:
        return None
    unique.sort(reverse=True)
    return unique[1]
```

**7. Dict-এর value দিয়ে sort করুন।**
```python
scores = {"Rahim": 85, "Karim": 92, "Salam": 78}
sorted_scores = dict(sorted(scores.items(), key=lambda x: x[1], reverse=True))
# {'Karim': 92, 'Rahim': 85, 'Salam': 78}
```

**8. FizzBuzz।**
```python
def fizzbuzz(n: int) -> list[str]:
    return [
        "FizzBuzz" if i % 15 == 0
        else "Fizz" if i % 3 == 0
        else "Buzz" if i % 5 == 0
        else str(i)
        for i in range(1, n + 1)
    ]
```

**9. String-এর anagram কিনা check করুন।**
```python
from collections import Counter

def is_anagram(s1: str, s2: str) -> bool:
    return Counter(s1.lower()) == Counter(s2.lower())

print(is_anagram("listen", "silent"))  # True
```

**10. List-এর running sum বের করুন।**
```python
from itertools import accumulate

def running_sum(nums: list[int]) -> list[int]:
    return list(accumulate(nums))

print(running_sum([1, 2, 3, 4]))  # [1, 3, 6, 10]
```

---

**Medium (১১–২০)**

**11. Linked list reverse করুন।**
```python
class Node:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def reverse_linked_list(head: Node) -> Node:
    prev = None
    curr = head
    while curr:
        next_node = curr.next
        curr.next = prev
        prev = curr
        curr = next_node
    return prev
```

**12. Binary search implement করুন।**
```python
def binary_search(arr: list[int], target: int) -> int:
    lo, hi = 0, len(arr) - 1
    while lo <= hi:
        mid = (lo + hi) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            lo = mid + 1
        else:
            hi = mid - 1
    return -1
```

**13. Stack দিয়ে balanced parentheses check করুন।**
```python
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
    return len(stack) == 0

print(is_balanced("({[]})"))   # True
print(is_balanced("({[})"))    # False
```

**14. LRU Cache implement করুন।**
```python
from collections import OrderedDict

class LRUCache:
    def __init__(self, capacity: int):
        self.cache = OrderedDict()
        self.capacity = capacity

    def get(self, key: int) -> int:
        if key not in self.cache:
            return -1
        self.cache.move_to_end(key)
        return self.cache[key]

    def put(self, key: int, value: int) -> None:
        if key in self.cache:
            self.cache.move_to_end(key)
        self.cache[key] = value
        if len(self.cache) > self.capacity:
            self.cache.popitem(last=False)
```

**15. Flatten nested list করুন (recursive)।**
```python
def flatten(nested: list) -> list:
    result = []
    for item in nested:
        if isinstance(item, list):
            result.extend(flatten(item))
        else:
            result.append(item)
    return result

print(flatten([1, [2, [3, 4]], [5, 6]]))  # [1, 2, 3, 4, 5, 6]
```

**16. Group anagrams একসাথে করুন।**
```python
from collections import defaultdict

def group_anagrams(words: list[str]) -> list[list[str]]:
    groups = defaultdict(list)
    for word in words:
        key = tuple(sorted(word))
        groups[key].append(word)
    return list(groups.values())

print(group_anagrams(["eat","tea","tan","ate","nat","bat"]))
# [['eat', 'tea', 'ate'], ['tan', 'nat'], ['bat']]
```

**17. Merge two sorted arrays।**
```python
def merge_sorted(a: list[int], b: list[int]) -> list[int]:
    result, i, j = [], 0, 0
    while i < len(a) and j < len(b):
        if a[i] <= b[j]:
            result.append(a[i]); i += 1
        else:
            result.append(b[j]); j += 1
    result.extend(a[i:])
    result.extend(b[j:])
    return result
```

**18. Word frequency counter বানান।**
```python
from collections import Counter
import re

def word_frequency(text: str) -> Counter:
    words = re.findall(r'\b[a-z]+\b', text.lower())
    return Counter(words)

freq = word_frequency("the quick brown fox jumps over the lazy dog the fox")
print(freq.most_common(3))  # [('the', 3), ('fox', 2), ...]
```

**19. Fibonacci generator বানান (infinite)।**
```python
from typing import Generator

def fibonacci() -> Generator[int, None, None]:
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b

gen = fibonacci()
first_10 = [next(gen) for _ in range(10)]
# [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
```

**20. Decorator implement করুন যা function execution time measure করে।**
```python
import time
import functools

def timer(func):
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        start = time.perf_counter()
        result = func(*args, **kwargs)
        elapsed = time.perf_counter() - start
        print(f"{func.__name__} took {elapsed:.4f}s")
        return result
    return wrapper

@timer
def slow_function():
    time.sleep(0.1)
    return "done"
```

---

**Hard (২১–৩০)**

**21. Longest substring without repeating characters।**
```python
def length_of_longest_substring(s: str) -> int:
    char_index = {}
    max_len = left = 0
    for right, char in enumerate(s):
        if char in char_index and char_index[char] >= left:
            left = char_index[char] + 1
        char_index[char] = right
        max_len = max(max_len, right - left + 1)
    return max_len

print(length_of_longest_substring("abcabcbb"))  # 3 ("abc")
```

**22. Implement `@retry` decorator with exponential backoff।**
```python
import time
import functools
import random

def retry(max_attempts: int = 3, base_delay: float = 1.0, exceptions=(Exception,)):
    def decorator(func):
        @functools.wraps(func)
        def wrapper(*args, **kwargs):
            for attempt in range(1, max_attempts + 1):
                try:
                    return func(*args, **kwargs)
                except exceptions as e:
                    if attempt == max_attempts:
                        raise
                    delay = base_delay * (2 ** (attempt - 1)) + random.uniform(0, 0.1)
                    print(f"Attempt {attempt} failed: {e}. Retrying in {delay:.2f}s")
                    time.sleep(delay)
        return wrapper
    return decorator

@retry(max_attempts=3, base_delay=0.5, exceptions=(ConnectionError,))
def fetch_data(url: str):
    # simulated unstable network
    if random.random() < 0.7:
        raise ConnectionError("Network error")
    return {"data": "success"}
```

**23. Thread-safe counter implement করুন।**
```python
import threading

class ThreadSafeCounter:
    def __init__(self):
        self._count = 0
        self._lock = threading.Lock()

    def increment(self, amount: int = 1):
        with self._lock:
            self._count += amount

    def decrement(self, amount: int = 1):
        with self._lock:
            self._count -= amount

    @property
    def value(self) -> int:
        with self._lock:
            return self._count
```

**24. Observer pattern implement করুন।**
```python
from typing import Callable, Any

class EventEmitter:
    def __init__(self):
        self._listeners: dict[str, list[Callable]] = {}

    def on(self, event: str, handler: Callable):
        self._listeners.setdefault(event, []).append(handler)
        return self  # fluent interface

    def off(self, event: str, handler: Callable):
        if event in self._listeners:
            self._listeners[event].remove(handler)

    def emit(self, event: str, *args, **kwargs):
        for handler in self._listeners.get(event, []):
            handler(*args, **kwargs)

# Usage
emitter = EventEmitter()
emitter.on("user_registered", lambda user: print(f"Welcome, {user}!"))
emitter.on("user_registered", lambda user: print(f"Sending email to {user}"))
emitter.emit("user_registered", "Rahim")
```

**25. Async concurrent API calls।**
```python
import asyncio
import aiohttp
from typing import Any

async def fetch(session: aiohttp.ClientSession, url: str) -> dict:
    async with session.get(url, timeout=aiohttp.ClientTimeout(total=10)) as resp:
        resp.raise_for_status()
        return await resp.json()

async def fetch_all(urls: list[str]) -> list[Any]:
    async with aiohttp.ClientSession() as session:
        tasks = [fetch(session, url) for url in urls]
        results = await asyncio.gather(*tasks, return_exceptions=True)
    return results

# urls = ["https://api.example.com/1", "https://api.example.com/2"]
# results = asyncio.run(fetch_all(urls))
```

**26. Rate limiter decorator বানান।**
```python
import time
import functools
from collections import deque

def rate_limit(calls: int, period: float):
    """Allow `calls` calls per `period` seconds."""
    def decorator(func):
        timestamps = deque()

        @functools.wraps(func)
        def wrapper(*args, **kwargs):
            now = time.monotonic()
            # remove old timestamps
            while timestamps and timestamps[0] <= now - period:
                timestamps.popleft()
            if len(timestamps) >= calls:
                sleep_for = period - (now - timestamps[0])
                time.sleep(sleep_for)
            timestamps.append(time.monotonic())
            return func(*args, **kwargs)
        return wrapper
    return decorator

@rate_limit(calls=5, period=1.0)
def api_call():
    return "OK"
```

**27. JSON-like deep merge করুন।**
```python
def deep_merge(base: dict, override: dict) -> dict:
    result = base.copy()
    for key, value in override.items():
        if (key in result and isinstance(result[key], dict)
                and isinstance(value, dict)):
            result[key] = deep_merge(result[key], value)
        else:
            result[key] = value
    return result

print(deep_merge(
    {"db": {"host": "localhost", "port": 5432}, "debug": True},
    {"db": {"port": 5433, "name": "prod"}, "env": "prod"}
))
# {'db': {'host': 'localhost', 'port': 5433, 'name': 'prod'}, 'debug': True, 'env': 'prod'}
```

**28. Trie data structure implement করুন।**
```python
class TrieNode:
    def __init__(self):
        self.children: dict[str, TrieNode] = {}
        self.is_end = False

class Trie:
    def __init__(self):
        self.root = TrieNode()

    def insert(self, word: str):
        node = self.root
        for char in word:
            node = node.children.setdefault(char, TrieNode())
        node.is_end = True

    def search(self, word: str) -> bool:
        node = self.root
        for char in word:
            if char not in node.children:
                return False
            node = node.children[char]
        return node.is_end

    def starts_with(self, prefix: str) -> bool:
        node = self.root
        for char in prefix:
            if char not in node.children:
                return False
            node = node.children[char]
        return True
```

**29. Producer-Consumer pattern asyncio দিয়ে।**
```python
import asyncio
import random

async def producer(queue: asyncio.Queue, n: int):
    for i in range(n):
        await asyncio.sleep(random.uniform(0.01, 0.05))
        item = f"task-{i}"
        await queue.put(item)
        print(f"Produced: {item}")
    await queue.put(None)  # sentinel

async def consumer(queue: asyncio.Queue):
    while True:
        item = await queue.get()
        if item is None:
            break
        await asyncio.sleep(random.uniform(0.02, 0.08))
        print(f"Consumed: {item}")
        queue.task_done()

async def main():
    queue = asyncio.Queue(maxsize=10)
    await asyncio.gather(producer(queue, 10), consumer(queue))

asyncio.run(main())
```

**30. Dependency injection container বানান।**
```python
from typing import Type, TypeVar, Callable, Any

T = TypeVar("T")

class Container:
    def __init__(self):
        self._factories: dict[type, Callable] = {}
        self._singletons: dict[type, Any] = {}

    def register(self, interface: type, factory: Callable, singleton=False):
        self._factories[interface] = (factory, singleton)

    def resolve(self, interface: Type[T]) -> T:
        if interface in self._singletons:
            return self._singletons[interface]
        factory, singleton = self._factories[interface]
        instance = factory(self)
        if singleton:
            self._singletons[interface] = instance
        return instance

# Usage
container = Container()
container.register(str, lambda c: "Hello, DI!", singleton=True)
print(container.resolve(str))  # Hello, DI!
```

---

<a id="p11-tricky"></a>

## 3. Tricky Python Questions (20টি)

**1. এই code-এর output কী?**
```python
x = [1, 2, 3]
y = x
y.append(4)
print(x)  # [1, 2, 3, 4] — x আর y একই object!
```
> List assignment reference copy করে — deep copy না। `y = x.copy()` বা `y = x[:]` দিয়ে shallow copy করুন।

**2. Default mutable argument trap।**
```python
def add_item(item, lst=[]):  # ❌ BAD
    lst.append(item)
    return lst

print(add_item(1))  # [1]
print(add_item(2))  # [1, 2] — same list!

# ✅ Fix:
def add_item(item, lst=None):
    if lst is None:
        lst = []
    lst.append(item)
    return lst
```

**3. Late binding closure trap।**
```python
funcs = [lambda: i for i in range(5)]
print([f() for f in funcs])  # [4, 4, 4, 4, 4] — সব 4!

# Fix — capture current value:
funcs = [lambda i=i: i for i in range(5)]
print([f() for f in funcs])  # [0, 1, 2, 3, 4]
```

**4. `is` operator integer trap।**
```python
a = 256
b = 256
print(a is b)  # True — integer caching (-5 to 256)

a = 257
b = 257
print(a is b)  # False (বা True — implementation dependent!)
# Always use == for value comparison!
```

**5. String multiplication trap।**
```python
matrix = [[0] * 3] * 3
matrix[0][0] = 1
print(matrix)  # [[1, 0, 0], [1, 0, 0], [1, 0, 0]] — সব row একই object!

# Fix:
matrix = [[0] * 3 for _ in range(3)]
matrix[0][0] = 1
print(matrix)  # [[1, 0, 0], [0, 0, 0], [0, 0, 0]] ✅
```

**6. `==` vs `is` None comparison।**
```python
x = None
print(x == None)   # True (works but not Pythonic)
print(x is None)   # True (Pythonic — PEP 8 recommend করে)
# None singleton তাই 'is' safe
```

**7. Augmented assignment আর immutable।**
```python
t = (1, [2, 3])
try:
    t[1] += [4, 5]   # Exception raise করে...
except TypeError:
    pass
print(t)  # (1, [2, 3, 4, 5]) — tuple unchanged, কিন্তু list modified!
# tuple immutable কিন্তু element মুতুব্য
```

**8. `for-else` আর `while-else`।**
```python
for i in range(5):
    if i == 10:
        break
else:
    print("No break!")  # এটি print হবে — break হয়নি

# else block: loop normally শেষ হলে run হয়, break-এ run হয় না
```

**9. Chained comparison।**
```python
print(1 < 2 < 3)     # True (mathematical: 1<2 AND 2<3)
print(1 < 2 > 0)     # True
print(1 == 1.0 == True)  # True (True == 1 == 1.0)
```

**10. Dictionary key-এ float trap।**
```python
d = {}
d[1] = "one"
d[1.0] = "one-float"
print(len(d))  # 1! — 1 == 1.0 == True, hash same
print(d)       # {1: 'one-float'}
```

**11. `sort()` vs `sorted()` return value।**
```python
lst = [3, 1, 2]
result = lst.sort()
print(result)   # None — sort() in-place, returns None
print(lst)      # [1, 2, 3]
# Mistake: sorted_lst = lst.sort() → sorted_lst is None!
```

**12. Generator exhaustion।**
```python
gen = (x for x in range(5))
print(list(gen))  # [0, 1, 2, 3, 4]
print(list(gen))  # [] — generator exhausted!
# Generator একবারই iterate করা যায়
```

**13. String `+` vs `join()` performance।**
```python
import timeit
# Bad O(n²)
t1 = timeit.timeit('result = ""; [result.__add__(str(i)) for i in range(1000)]', number=1000)
# Good O(n)
t2 = timeit.timeit('"".join(str(i) for i in range(1000))', number=1000)
# join significantly faster for large lists
```

**14. `__del__` reliable না।**
```python
class Resource:
    def __del__(self):
        print("Cleaning up!")  # কখন call হবে guarantee নেই

# Context manager use করুন:
class Resource:
    def __enter__(self): return self
    def __exit__(self, *args): print("Cleaning up!")  # guaranteed!
```

**15. Walrus operator `:=` (Python 3.8+)।**
```python
import re
text = "User: Rahim, Age: 25"
if m := re.search(r"User: (\w+)", text):
    print(m.group(1))  # Rahim
# := assigns and evaluates in one step
```

**16. `dict.get()` vs `dict[]`।**
```python
d = {"a": 1}
print(d["b"])        # KeyError!
print(d.get("b"))    # None (no error)
print(d.get("b", 0)) # 0 (default value)
```

**17. `any()` short-circuit।**
```python
def side_effect(x):
    print(f"Checking {x}")
    return x > 3

print(any(side_effect(x) for x in [1, 2, 5, 6, 7]))
# Checking 1, Checking 2, Checking 5 — stops at 5! Short-circuit.
```

**18. Shallow copy trap।**
```python
import copy
original = [[1, 2], [3, 4]]
shallow = copy.copy(original)     # or original[:]
deep = copy.deepcopy(original)

shallow[0][0] = 99
print(original)   # [[99, 2], [3, 4]] — affected!
print(deep)       # [[1, 2], [3, 4]] — safe!
```

**19. `*` unpacking।**
```python
first, *rest = [1, 2, 3, 4, 5]
print(first)  # 1
print(rest)   # [2, 3, 4, 5]

*init, last = [1, 2, 3, 4, 5]
print(last)   # 5

a, *_, b = [1, 2, 3, 4, 5]
print(a, b)   # 1 5
```

**20. `exec()` আর `eval()` — security risk।**
```python
# NEVER do this with user input:
user_code = input("Enter code: ")
exec(user_code)    # Arbitrary code execution!
eval(user_code)    # Same risk!

# Safe alternative: use ast.literal_eval for data only
import ast
safe_data = ast.literal_eval("[1, 2, 3]")  # Only literals
```

---

<a id="p11-rapid"></a>

## 4. Rapid-fire Q&A (20টি)

| # | প্রশ্ন | উত্তর |
|---|---|---|
| 1 | Python-এ `pass` কী করে? | Placeholder — empty block syntax-এর জন্য |
| 2 | `break` vs `continue` vs `pass`? | break: loop exit, continue: next iteration, pass: nothing |
| 3 | `list` vs `array` (numpy)? | list heterogeneous, array homogeneous + fast math |
| 4 | Python 2 vs 3 প্রধান পার্থক্য? | print function, unicode default, integer division, range |
| 5 | `int`, `float` precision issue? | `0.1 + 0.2 != 0.3` — floating point binary representation |
| 6 | `str.format()` vs f-string? | f-string (3.6+) faster, readable; format backward-compatible |
| 7 | `os.path` vs `pathlib`? | pathlib OOP, cross-platform, preferred (3.4+) |
| 8 | `json.dumps()` vs `json.dump()`? | dumps → string, dump → file write |
| 9 | `pickle` কী? | Python object serialization (binary) — security risk with untrusted data |
| 10 | `__name__ == "__main__"` কেন? | Import হলে run না করতে, direct execute হলে run করতে |
| 11 | List vs Deque prepend speed? | list.insert(0,x) O(n), deque.appendleft() O(1) |
| 12 | `setdefault()` কী করে? | Key না থাকলে default set করে এবং value return করে |
| 13 | `vars()` কী? | Object-এর `__dict__` return করে |
| 14 | `dir()` কী? | Object-এর all attributes/methods list করে |
| 15 | `isinstance()` vs `type()`? | isinstance inheritance check করে, type exact type only |
| 16 | Python-এ `//` operator? | Floor division — integer result |
| 17 | `@property` কী করে? | Method-কে attribute-এর মতো access করতে দেয় |
| 18 | Walrus operator কখন? | Loop/condition-এ assign + check একসাথে (Python 3.8+) |
| 19 | `NotImplemented` vs `NotImplementedError`? | NotImplemented: operator method return value, Error: abstract method |
| 20 | `__all__` কী? | Module-এ `from module import *` কী export হবে তা define করে |

---

<a id="p11-scenario"></a>

## 5. Scenario-based Questions (20টি)

**1. আপনার FastAPI app-এ production-এ N+1 query problem দেখছেন। কীভাবে diagnose আর fix করবেন?**
> Diagnose: `sqlalchemy-utils` বা `flask-sqlalchemy` query logging enable করুন — কতটি query হচ্ছে দেখুন। Fix: `joinedload()` বা `selectinload()` দিয়ে eager loading। একটি query-তেই related data আনুন।

**2. API-তে memory leak দেখছেন — RAM ক্রমাগত বাড়ছে। কীভাবে debug করবেন?**
> `tracemalloc` module দিয়ে memory snapshot নিন। `objgraph` library দিয়ে object count দেখুন। Common cause: circular reference, unbounded cache, event listener যা detach হয়নি। `gc.collect()` force করুন।

**3. একটি Python script 10 মিনিট ধরে চলছে। কীভাবে optimize করবেন?**
> Step 1: Profile — `cProfile` বা `line_profiler` দিয়ে hotspot find করুন। Step 2: Algorithm improve করুন। Step 3: `numpy`/`pandas` vectorization। Step 4: Caching (`lru_cache`)। Step 5: Multiprocessing CPU-bound task-এ।

**4. 1 million records CSV process করতে হবে। কীভাবে করবেন memory-efficiently?**
> Generator + chunked processing। `pandas` chunking: `pd.read_csv(file, chunksize=10000)`। বা pure Python: CSV reader line by line, never load all in memory। Database bulk insert।

**5. Third-party API 30% time timeout করে। কীভাবে handle করবেন?**
> Retry with exponential backoff + jitter। Circuit breaker pattern। Timeout set করুন (`requests timeout=5`)। Fallback value বা cached response return করুন। Alert/log প্রতিটি failure।

**6. Team-এর নতুন developer বারবার mutable default argument bug করছেন। কীভাবে prevent করবেন?**
> `flake8` + `flake8-bugbear` plugin — B006 rule এই bug detect করে। Pre-commit hook-এ add করুন। Code review checklist-এ রাখুন।

**7. Production-এ অচানক 500 error। Log দেখছেন `RecursionError: maximum recursion depth exceeded`। কী করবেন?**
> Immediate: `sys.setrecursionlimit()` বাড়ানো temporary fix। Root cause: infinite recursion — base case missing বা circular reference। Refactor করুন iterative approach-এ অথবা memoization দিয়ে।

**8. JWT token expire হওয়ার পরে user-এর session lost হচ্ছে। UX improve করবেন কীভাবে?**
> Refresh token pattern implement করুন। Short-lived access token (15 min) + long-lived refresh token (7 days)। Frontend silent refresh করবে। Refresh token rotation security-র জন্য।

**9. Concurrent user-রা একই database row update করছে। Race condition prevent করবেন কীভাবে?**
> Optimistic locking: version column — update-এর আগে version check করুন। Pessimistic locking: `SELECT FOR UPDATE`। SQLAlchemy-তে `with_for_update()`।

**10. Python script-এ credentials hardcode হয়ে গেছে production-এ। কী করবেন?**
> Immediate: git history rewrite করুন (`git filter-branch` বা BFG Repo Cleaner), credentials rotate করুন। Prevention: `.env` file + `python-dotenv`, `.gitignore`-এ `.env`, `git-secrets` pre-commit hook।

**11. pytest suite আগে 2 মিনিটে চলত, এখন 15 মিনিট লাগছে। কীভাবে debug করবেন?**
> `pytest --durations=10` — slowest 10 test দেখান। DB call করছে এমন test mock করুন। `pytest-xdist` দিয়ে parallel run (`pytest -n auto`)।

**12. Deployed app-এ একটি bug শুধু production-এ হচ্ছে, local-এ হচ্ছে না। কী হতে পারে?**
> Environment variables different। Database data different (edge case)। Python/library version different। Race condition — local single process, prod multiple workers। Log level different।

**13. API endpoint-এ same data বারবার DB থেকে fetch হচ্ছে। কীভাবে optimize করবেন?**
> In-memory cache: `functools.lru_cache` বা `cachetools`। Redis cache: `redis-py` + TTL set। HTTP cache headers: `Cache-Control`, `ETag`। CDN-এ cache।

**14. 100+ microservices-এর Python project-এ shared code manage করবেন কীভাবে?**
> Internal Python package তৈরি করুন — private PyPI (Nexus/Artifactory) বা Git package। Shared models, utilities, clients। Version properly।

**15. বড় Python project-এ circular import এর কীভাবে সমাধান করবেন?**
> Import function-এর ভেতরে move করুন (local import)। Module restructure করুন — circular dependency সাধারণত design problem। Shared code আলাদা module-এ move করুন।

**16. Python-এ একটি function 500ms নেয় কিন্তু সেটা 1000 concurrent request handle করতে হবে। কী করবেন?**
> `asyncio` + `async def` যদি I/O-bound হয়। CPU-bound হলে `multiprocessing.Pool` বা Celery task queue। Redis queue + worker pool। Horizontal scaling।

**17. Pydantic model validation-এ custom error message দিতে চান। কীভাবে?**
```python
from pydantic import field_validator

class User(BaseModel):
    age: int

    @field_validator("age")
    @classmethod
    def age_must_be_positive(cls, v):
        if v < 0:
            raise ValueError("বয়স negaitive হতে পারে না")
        return v
```

**18. একটি Python web scraper IP block হচ্ছে। কীভাবে handle করবেন?**
> Polite delay (`time.sleep`), `User-Agent` rotate, proxy rotation। `Scrapy` middleware। Respect `robots.txt`। Rate limiting।

**19. DB migration করতে গিয়ে production-এ data loss হওয়ার ঝুঁকি আছে। কীভাবে safe করবেন?**
> Backup নিন আগে। Alembic migration script review করুন। Staging-এ আগে test করুন। Rollback migration তৈরি করুন। Zero-downtime migration: additive changes (add column) → deploy → remove old।

**20. Interview-এ "আপনার সবচেয়ে কঠিন bug" জিজ্ঞেস করলে কীভাবে উত্তর দেবেন?**
> STAR method: Situation (project context), Task (কী করতে হয়েছিল), Action (কীভাবে debug করলেন — tools, steps), Result (কীভাবে solve হলো, কী শিখলেন)। Honest, specific, learning-focused উত্তর দিন।

---

## PART 11 Quick Revision Table

| Section | Key Points |
|---|---|
| Theoretical (60) | Basics → OOP → Functional → DS → Advanced → Web stack |
| Coding (30) | Easy: fundamentals, Medium: data structures, Hard: patterns |
| Tricky (20) | Mutable default, late binding, `is` vs `==`, generator exhaustion |
| Rapid-fire (20) | One-liner concept checks |
| Scenario (20) | Real project problems: N+1, memory leak, race condition |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part12"></a>

## 📋 PART 12 সূচিপত্র — Bangladeshi Interview Preparation

| # | Topic | What's Inside |
|---|---|---|
| 1 | [BD Company Interview Patterns](#p12-companies) | Brain Station 23, BJIT, Pathao, bKash, Nagad |
| 2 | [Mock Interview Script](#p12-mock) | Bangla conversation format — full simulation |
| 3 | [Common Rejection Reasons](#p12-rejection) | কেন fail করেন, কীভাবে avoid করবেন |
| 4 | [Salary Negotiation](#p12-salary) | BDT context, Junior SWE salary range |
| 5 | [Resume Tips](#p12-resume) | Python developer CV — do's and don'ts |
| 6 | [Practice Resources](#p12-resources) | LeetCode, HackerRank, BD job sites |
| 7 | [Final Checklist](#p12-checklist) | Interview-এর আগের দিন সব check |

---

<a id="p12-companies"></a>

## 1. Bangladesh Company Interview Patterns

### Brain Station 23

**প্রোফাইল:** Large software firm, outsourcing + product। ~2000+ engineers।

**Interview Process (Python/Backend):**
1. CV Screening (ATS — keyword: Python, Django/FastAPI, REST, SQL)
2. Online Assessment — HackerRank (2 coding problems, 45 min)
3. Technical Phone Screen (30 min — basics, OOP, SQL)
4. Technical Interview Round 1 (1 hr — coding + design)
5. Technical Interview Round 2 (1 hr — system design light, project discussion)
6. HR Round (salary, notice period)

**প্রায়ই আসা topics:**
- OOP — `__init__`, inheritance, polymorphism
- Python basics — list/dict operations, generators
- SQL — JOIN, GROUP BY, subquery
- REST API concepts — HTTP methods, status codes
- Git — basic workflow
- একটি project নিয়ে বিস্তারিত আলোচনা

**Tips:** GitHub profile clean করুন। Project-এ README ভালো লিখুন। HackerRank practice করুন।

---

### BJIT Limited

**প্রোফাইল:** Japanese partnership, formal process, quality-focused।

**Interview Process:**
1. Written Test (aptitude + programming fundamentals)
2. Technical Interview (2-3 rounds)
3. HR + Management Interview

**প্রায়ই আসা topics:**
- Strong OOP — Design patterns (Factory, Singleton, Observer)
- Testing — unit testing, TDD concept
- Code quality — clean code, SOLID principles
- Database — normalization, indexing, query optimization
- Japanese work culture fit (communication, punctuality)

**Tips:** Problem-solving approach explain করুন clearly। Communication skill important।

---

### Pathao

**প্রোফাইল:** Ride-sharing/delivery startup, fast-paced, tech-first।

**Interview Process:**
1. Take-home assignment (real feature implementation, 48-72 hrs)
2. Technical deep-dive (code review of assignment, 1 hr)
3. System Design Interview (scale: millions of rides)
4. Culture fit + behavioral

**প্রায়ই আসা topics:**
- System design — location tracking, real-time matching
- Scalability — caching, message queue (Kafka/RabbitMQ)
- Python async — asyncio, Celery
- Database — PostgreSQL, Redis, optimization
- API design — versioning, rate limiting
- Microservices — service communication

**Tips:** Take-home assignment-এ production-quality code দিন — tests, error handling, README। System design-এ tradeoffs বলুন।

---

### bKash

**প্রোফাইল:** FinTech leader, security-critical, compliance-heavy।

**Interview Process:**
1. HR Pre-screening
2. Technical Written Test
3. Technical Interview (multiple rounds)
4. Security/Compliance awareness check
5. Senior Management Interview

**প্রায়ই আসা topics:**
- Security — OWASP Top 10, SQL injection, XSS prevention
- Financial transactions — ACID properties, idempotency
- API security — JWT, OAuth2, rate limiting
- Encryption — at rest, in transit
- Audit logging, compliance
- Python — strong fundamentals + security

**Tips:** Security consciousness দেখান সব answer-এ। "এটি কি secure?" নিজেই জিজ্ঞেস করুন।

---

### Nagad

**প্রোফাইল:** Digital financial service, growing fast, competitive।

**Interview Process:**
1. Online Coding Test
2. Technical Interview (2 rounds)
3. HR Interview

**প্রায়ই আসা topics:**
- Python backend — Django/FastAPI
- Database — PostgreSQL, query optimization
- API design — REST, documentation
- Security basics — authentication, authorization
- Problem-solving coding

**Tips:** MFS (Mobile Financial Service) domain knowledge থাকলে plus point।

---

### General Tips for BD Market

**Preparation Timeline:**
- **3 months before:** DSA foundation, Python deep dive
- **2 months before:** Projects build করুন, system design শুরু
- **1 month before:** Mock interviews, company-specific research
- **1 week before:** Revision, portfolio clean করুন

**Salary Benchmark (2025-2026, Dhaka):**
| Level | Range (BDT/month) |
|---|---|
| Junior Python Developer (0–1 yr) | 25,000 – 50,000 |
| Mid-level (2–4 yr) | 50,000 – 1,20,000 |
| Senior (5+ yr) | 1,00,000 – 2,50,000+ |
| Tech Lead / Architect | 2,00,000+ |

---

<a id="p12-mock"></a>

## 2. Mock Interview Script (Python Junior Developer)

**Scenario:** Brain Station 23-এর Technical Round 1। Interviewer: Senior Engineer। Candidate: Rahim (1 year experience)।

---

**Interviewer:** আপনার সম্পর্কে বলুন।

**Rahim:** আমি Rahim। Computer Science-এ graduate করেছি 2023 সালে। Last 1 year একটি software company-তে Python developer হিসেবে কাজ করেছি। Django আর FastAPI দিয়ে REST API তৈরি করেছি। PostgreSQL, Redis আর Git নিয়মিত use করি। আমার GitHub-এ কয়েকটি personal project আছে — একটি FastAPI-based e-commerce API যেটিতে JWT auth, Celery task queue, আর Redis caching implement করেছি।

---

**Interviewer:** Python-এ `list` আর `tuple`-এর পার্থক্য বলুন।

**Rahim:** দুটো ordered sequence। পার্থক্য হলো mutability। List mutable — পরে add, remove, change করা যায়। Tuple immutable — একবার তৈরি হলে change করা যায় না।

আমি tuple use করি যখন data fixed থাকে — যেমন database record return করার সময়, বা function থেকে multiple value return করতে। Tuple slightly faster এবং dictionary key হিসেবে use করা যায়, list যায় না কারণ list unhashable।

---

**Interviewer:** OOP-এ polymorphism কী? Python-এ কীভাবে implement করবেন?

**Rahim:** Polymorphism মানে "many forms" — একই interface দিয়ে different types handle করা।

Python-এ দুভাবে: Method overriding — child class parent-এর method নিজের মতো করে implement করে। আর duck typing — Python type check করে না, শুধু দেখে object-এর সেই method আছে কিনা।

উদাহরণ: একটি `Payment` base class, তার from `bKashPayment` আর `NagadPayment` child। দুটোই `process()` method implement করে কিন্তু আলাদাভাবে। আমি একই `payment.process()` call করি — কোন provider সেটা caller জানে না।

---

**Interviewer:** একটি coding problem দিচ্ছি। একটি list-এ সব duplicate element remove করুন কিন্তু insertion order maintain করতে হবে।

**Rahim:** *(চিন্তা করুন জোরে)* Okay, সবচেয়ে simple approach হলো `list(set())` কিন্তু এটি order maintain করে না।

Order maintain করতে আমি `seen` set use করব — O(1) lookup। যা already দেখেছি সেটা skip, বাকিগুলো রাখব।

```python
def remove_duplicates(lst):
    seen = set()
    result = []
    for item in lst:
        if item not in seen:
            result.append(item)
            seen.add(item)
    return result
```

Alternatively, list comprehension দিয়ে:
```python
def remove_duplicates(lst):
    seen = set()
    return [x for x in lst if not (x in seen or seen.add(x))]
```

Time complexity O(n), space O(n)।

---

**Interviewer:** আপনার project-এ সবচেয়ে challenging কী ছিল?

**Rahim:** আমার e-commerce project-এ payment processing-এ একটি race condition ছিল। দুটি concurrent request একই order-এ double charge করছিল।

আমি diagnose করলাম logs দিয়ে — দেখলাম দুটো request microsecond-এর পার্থক্যে একই payment ID create করছে।

Solution: Database-এ optimistic locking implement করলাম। Order table-এ `version` column add করলাম। Payment process করার আগে version check করি — যদি changed হয়ে যায়, transaction rollback করে error return করি। Frontend retry করে।

এটি থেকে শিখলাম: concurrent system-এ race condition assume করতে হবে, test করতে হবে।

---

**Interviewer:** REST API-তে HTTP status code 400 আর 422 পার্থক্য?

**Rahim:** দুটোই client error কিন্তু context আলাদা।

400 Bad Request — general client error, request malformed বা invalid।

422 Unprocessable Entity — request structure correct কিন্তু semantic validation fail — যেমন email format wrong, age negative। FastAPI automatically 422 return করে Pydantic validation fail হলে। এটি আরো specific, client-এর জন্য better error message।

---

**Interviewer:** আর কোনো প্রশ্ন আছে আমার জন্য?

**Rahim:** হ্যাঁ, কয়েকটি জিজ্ঞেস করতে চাই। Team-এ কতজন Python developer আছেন? আমি কোন project-এ কাজ করব? Code review process কেমন? আর আপনারা কোন Python version আর কোন framework use করছেন production-এ?

---

<a id="p12-rejection"></a>

## 3. Common Rejection Reasons — এবং কীভাবে Avoid করবেন

**Technical Reasons:**

**1. Fundamentals দুর্বল**
- ❌ Basic OOP, Python data structures জিজ্ঞেস করলে uncertain
- ✅ Fix: PART 1–6 পুরোটা পড়ুন, flashcard বানান

**2. Coding problem solve করতে পারছেন না under pressure**
- ❌ চুপ করে আছেন, approach বলছেন না
- ✅ Fix: Think aloud করুন। "আমি প্রথমে brute force দিয়ে শুরু করব, তারপর optimize করব।"

**3. Project নিজে তৈরি করেননি**
- ❌ Tutorial project copy করেছেন, কিছু জিজ্ঞেস করলে জানেন না
- ✅ Fix: একটি হলেও নিজে build করুন — feature add করুন, bug fix করুন

**4. SQL দুর্বল**
- ❌ JOIN, GROUP BY জিজ্ঞেস করলে struggle
- ✅ Fix: SQLZoo, LeetCode SQL section practice করুন

**5. No testing knowledge**
- ❌ "Testing করিনি" — automatic red flag
- ✅ Fix: যেকোনো project-এ কমপক্ষে basic pytest লিখুন

---

**Communication Reasons:**

**6. উত্তর অনেক ছোট বা অনেক বড়**
- ❌ "হ্যাঁ, জানি" বা 10 মিনিট বলতে থাকা
- ✅ Fix: 2–3 sentence answer। Interviewer যদি detail চায়, তখন বিস্তারিত বলুন

**7. "জানি না" বলে থেমে যাওয়া**
- ❌ আটকে গেলে complete silence
- ✅ Fix: "এই exact term জানি না, কিন্তু এই concept টা আমার মনে হয় এভাবে কাজ করে..."

**8. Question না করা**
- ❌ "আর কোনো প্রশ্ন নেই।" — disengaged মনে হয়
- ✅ Fix: Team, tech stack, learning opportunities — genuine question করুন

---

**Attitude Reasons:**

**9. Overconfidence বা underconfidence**
- ❌ "এটা সহজ" বা extremely nervous
- ✅ Fix: Honest আর curious হন। "আমি এটা exactly জানি না, কিন্তু শিখতে আগ্রহী।"

**10. Previous job/employer সম্পর্কে negative**
- ❌ "আগের company horrible ছিল"
- ✅ Fix: Neutral বা positive frame করুন — "আমি নতুন challenge খুঁজছিলাম"

---

<a id="p12-salary"></a>

## 4. Salary Negotiation Tips (BDT Context)

**Research আগে:**
- glassdoor.com, linkedin.com salary insights
- BD tech community (Facebook groups: "Software Engineers of Bangladesh")
- বন্ধু/senior যারা target company-তে আছেন

**Negotiation Script:**

**যখন HR জিজ্ঞেস করে "আপনার expected salary কত?"**

> "আমি এই role-এর জন্য market rate-এ interested। আমার research অনুযায়ী এই position-এ [range] offer হয়। আমার skills আর experience বিবেচনায় [specific amount] expect করছি। এটা কি আপনাদের budget-এর মধ্যে?"

**Offer পেয়ে negotiate করতে হলে:**

> "আপনার offer-এর জন্য ধন্যবাদ। এই role নিয়ে আমি genuinely excited। আমার current compensation আর market research-এর ভিত্তিতে [higher amount]-এ কি বিবেচনা করা সম্ভব?"

**Tips:**
- সবসময় range দিন, single number নয়
- Benefits negotiate করুন — work from home, learning budget, flexible hours
- "Is this negotiable?" জিজ্ঞেস করুন সরাসরি
- Written offer আসার আগে কিছু accept করবেন না verbally-এর বাইরে
- Counter-offer দিলে 24-48 hrs time নিন — impulsive হবেন না

**Counter-offer trap:**
বর্তমান employer counter-offer দিলে সাবধান — raise দিলেও underlying reason (growth, culture) change হয় না। Statistics: 80% who accept counter-offer within 6 months চলে যায়।

---

<a id="p12-resume"></a>

## 5. Resume Tips — Python Developer

**Resume Structure:**

```
[Name] | [Phone] | [Email] | [LinkedIn] | [GitHub]

SUMMARY (2–3 lines)
Python developer with X years of experience building scalable
REST APIs using FastAPI/Django. Strong in PostgreSQL, Redis, Docker.

SKILLS
Languages: Python, SQL, JavaScript (basic)
Frameworks: FastAPI, Django REST Framework, SQLAlchemy
Databases: PostgreSQL, MySQL, Redis, MongoDB
Tools: Git, Docker, Linux, Celery, pytest

EXPERIENCE
Company Name | Python Developer | Jan 2024 – Present
• Built REST API for X feature using FastAPI, serving 50K+ daily requests
• Reduced API response time by 40% using Redis caching
• Wrote pytest test suite with 80% coverage
• Collaborated in Agile team of 8 engineers

PROJECTS
Project Name | GitHub Link
• FastAPI e-commerce API with JWT auth, Celery background tasks, PostgreSQL
• Web scraper using BeautifulSoup that collected 100K+ records

EDUCATION
B.Sc. in CSE | University Name | 2023
```

**DO:**
- Quantify achievements — "50K requests/day", "40% faster", "80% coverage"
- GitHub link দিন — recruiter check করবে
- Tech stack clearly list করুন — ATS (Automated Tracking System) keyword match করে
- Active verb use করুন — "built", "reduced", "implemented"
- 1 page (0–2 years experience)

**DON'T:**
- "Proficient in all programming languages" — credibility হারাবেন
- Objective statement পুরানো format — summary ব্যবহার করুন
- Photo দেওয়া নিয়ে: international job avoid করুন, BD local companies-এ optional
- `hello123@gmail.com` type email — professional email রাখুন
- Tutorial project copy করে রাখবেন না — interview-এ ধরা পড়বেন

**ATS Keywords (Python Backend):**
`Python`, `FastAPI`, `Django`, `REST API`, `PostgreSQL`, `Redis`, `Docker`, `Git`, `pytest`, `SQLAlchemy`, `JWT`, `Celery`, `microservices`, `agile`, `CI/CD`

---

<a id="p12-resources"></a>

## 6. Practice Resources

**Coding Practice:**

| Platform | Focus | Link |
|---|---|---|
| LeetCode | DSA — FAANG style | leetcode.com |
| HackerRank | Python domain, certifications | hackerrank.com |
| Codeforces | Competitive — logic | codeforces.com |
| Project Euler | Math + Python | projecteuler.net |
| Exercism | Python idiomatic code | exercism.org/tracks/python |

**Target for Junior BD Job:**
- LeetCode: 50+ Easy, 20+ Medium (Arrays, Strings, HashMap, Stack)
- HackerRank Python: Silver badge minimum

---

**System Design:**

| Resource | What |
|---|---|
| "Designing Data-Intensive Applications" — Martin Kleppmann | Best book on distributed systems |
| System Design Primer (GitHub) | Free, comprehensive |
| ByteByteGo (YouTube) | Visual explanations |

---

**BD Job Boards:**

| Site | সেরা জন্য |
|---|---|
| bdjobs.com | Large companies, corporate |
| linkedin.com | Startups + multinational |
| chakri.com | BD tech focus |
| jobsbd.com | General + tech |
| Facebook: "Job Circular BD IT" | Community, startup |

**Community:**
- Facebook: "Software Engineers of Bangladesh" — 70K+ members
- Discord: BD Tech Community
- LinkedIn: BD Python developers follow করুন

---

**Learning Resources:**

| Resource | কী শিখবেন |
|---|---|
| Real Python (realpython.com) | Practical Python articles |
| FastAPI docs | Best framework documentation |
| SQLAlchemy docs | ORM deep dive |
| TestDriven.io | TDD with Python/FastAPI |
| Arjan Codes (YouTube) | Clean code, design patterns |
| Corey Schafer (YouTube) | Python fundamentals |

---

<a id="p12-checklist"></a>

## 7. Final Checklist — Interview-এর আগে

**১ সপ্তাহ আগে:**
- [ ] GitHub profile clean করুন — pinned projects readable README সহ
- [ ] Interview company research করুন — product, tech stack, recent news
- [ ] PART 1–11 quick revision করুন
- [ ] 2–3 mock interview practice করুন (friend বা mirror-এ)
- [ ] Target questions prepare করুন interviewer-এর জন্য

**১ দিন আগে:**
- [ ] Interview time, location/video link confirm করুন
- [ ] Outfit prepare করুন (smart casual — jeans + formal shirt okay)
- [ ] পথের route জানুন — 30 min আগে পৌঁছানোর plan করুন
- [ ] Resume/CV print করুন 2-3 copies (in-person হলে)
- [ ] Portfolio/GitHub খুলে রাখুন browser-এ
- [ ] রাত 11টার আগে ঘুমাতে যান

**Interview-এর দিন:**
- [ ] সময় মেনে যান — 10–15 min আগে
- [ ] Phone silent করুন
- [ ] Water bottle সাথে রাখুন
- [ ] Deep breath — nervous হলেও okay

**Interview-এর সময়:**
- [ ] Interviewer-এর নাম জানুন আগে, সম্বোধন করুন
- [ ] Think aloud করুন coding-এ
- [ ] "জানি না" বললে approach বলুন
- [ ] প্রশ্ন করুন শেষে
- [ ] Thank you বলুন শেষে

**Interview-এর পরে:**
- [ ] 24 ঘণ্টার মধ্যে thank-you email পাঠান (LinkedIn বা email)
- [ ] কী ভালো হলো, কী improve করা দরকার — note করুন
- [ ] পরের সুযোগের জন্য ready থাকুন

---

## PART 12 Quick Revision Table

| Topic | Key Takeaway | Action |
|---|---|---|
| BD Company Patterns | Brain Station 23 online test, BJIT formal, Pathao take-home, bKash security-focus | Research target company |
| Mock Interview | Think aloud, honest, question করুন | 3+ mock practices |
| Rejection Reasons | Fundamentals, communication, project ownership | Identify weak area |
| Salary Negotiation | Research → range → counter → written | Never accept verbally first |
| Resume | Quantify, ATS keywords, GitHub | 1 page, active verbs |
| Resources | LeetCode 50+ Easy, HackerRank Python | 30 min/day consistent |
| Checklist | 1 week → 1 day → day-of → after | Follow systematically |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **🎉 সম্পূর্ণ হয়েছে!**
> এই Python Junior Engineer Interview Handbook-এর সব **12টি PART** সম্পূর্ণ।
>
> **PART 1** — Python Basics | **PART 2** — Data Structures | **PART 3** — OOP | **PART 4** — Functional Python | **PART 5** — File & Exception Handling | **PART 6** — Modules & Standard Library | **PART 7** — Database & ORM | **PART 8** — Web Development & API | **PART 9** — Testing & Best Practices | **PART 10** — Python Projects | **PART 11** — Interview Questions Bank | **PART 12** — Bangladeshi Interview Preparation
>
> **শুভকামনা তোমার interview-এ!** 🐍
