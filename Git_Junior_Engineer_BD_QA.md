<div align="center">

# 🔀 Git & GitHub Interview Handbook
### বাংলাদেশের Junior Software Engineer-দের জন্য সম্পূর্ণ Git & GitHub প্রস্তুতি গাইড

![Language](https://img.shields.io/badge/Language-বাংলা-green?style=for-the-badge)
![Target](https://img.shields.io/badge/Target-Junior%20SWE-blue?style=for-the-badge)
![Parts](https://img.shields.io/badge/Parts-11%20Total-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=for-the-badge)

</div>

---

<a id="top"></a>

## 📋 সম্পূর্ণ সূচিপত্র

| PART | বিষয় | অবস্থা |
|------|------|--------|
| [PART 1](#part1) | Git Fundamentals | ✅ |
| [PART 2](#part2) | Git Branching & Workflow | ✅ |
| PART 3 | Advanced Git | 🔜 |
| PART 4 | GitHub Fundamentals | 🔜 |
| PART 5 | GitHub Collaboration & Team Workflow | 🔜 |
| PART 6 | GitHub Actions & CI/CD Basics | 🔜 |
| PART 7 | Git & GitHub for Real Projects | 🔜 |
| PART 8 | Git Command Mastery | 🔜 |
| PART 9 | Git & GitHub Interview Questions | 🔜 |
| PART 10 | Professional Developer Workflow | 🔜 |
| PART 11 | Bangladeshi Interview Preparation | 🔜 |

---

<a id="part1"></a>
## PART 1: Git Fundamentals

> Git হলো প্রতিটি Software Engineer-এর সবচেয়ে প্রয়োজনীয় tool। এই PART-এ Git-এর একেবারে মূল ভিত্তি থেকে শুরু করে দৈনন্দিন commands পর্যন্ত সব কিছু বিস্তারিত আলোচনা করা হয়েছে।

| # | বিষয় |
|---|-------|
| 1 | [Git কী?](#p1-what-is-git) |
| 2 | [Version Control System (VCS)](#p1-vcs) |
| 3 | [Centralized vs Distributed VCS](#p1-cvs-dvcs) |
| 4 | [Git Architecture](#p1-architecture) |
| 5 | [Repository](#p1-repository) |
| 6 | [Working Directory, Staging Area, Commit](#p1-three-areas) |
| 7 | [HEAD](#p1-head) |
| 8 | [Git Installation ও Configuration](#p1-install-config) |
| 9 | [git init ও git clone](#p1-init-clone) |
| 10 | [git status](#p1-status) |
| 11 | [git add](#p1-add) |
| 12 | [git commit](#p1-commit) |
| 13 | [git log](#p1-log) |

---

<a id="p1-what-is-git"></a>
**Topic 1: Git কী?**

**সংজ্ঞা:**
Git হলো একটি **Distributed Version Control System (DVCS)** — অর্থাৎ এমন একটি software যা আপনার code-এর পরিবর্তনের ইতিহাস track করে এবং একাধিক developer-কে একই project-এ একসাথে কাজ করতে দেয়।

Git তৈরি করেন **Linus Torvalds** ২০০৫ সালে — Linux kernel-এর development-এর জন্য। এটি **open-source** এবং এখন পর্যন্ত সবচেয়ে বেশি ব্যবহৃত version control system।

**বাস্তব জীবনের উপমা:**
ধরুন আপনি একটি বই লিখছেন। প্রতিদিন লেখার পরে আপনি সেটির একটি photocopy রাখছেন। কোনো দিন ভুল করলে আপনি পুরোনো photocopy থেকে ফিরে আসতে পারবেন। Git ঠিক এটাই করে — কিন্তু code-এর জন্য, এবং এটি অনেক বেশি intelligent।

**Interview-style explanation:**
```
প্রশ্ন: "Git কী এবং এটা কেন ব্যবহার করা হয়?"

উত্তর: "Git হলো একটি Distributed Version Control System যা:
1. Code-এর প্রতিটি পরিবর্তনের record রাখে
2. Multiple developer-দের একসাথে কাজ করতে দেয় conflict ছাড়া
3. যেকোনো পুরোনো version-এ ফিরে যাওয়ার সুযোগ দেয়
4. Experimentation-এর জন্য আলাদা branch তৈরি করতে দেয়
5. Local-এ সম্পূর্ণ project history রাখে — internet ছাড়াও কাজ করা যায়"
```

**Git কেন গুরুত্বপূর্ণ:**
```
✅ Code history — "কে কখন কী পরিবর্তন করেছে" জানা যায়
✅ Collaboration — team-এর সবাই একই codebase-এ কাজ করতে পারে
✅ Backup — remote repository-তে code safe থাকে
✅ Experimentation — নতুন feature branch-এ test করে main-এ merge করা যায়
✅ Rollback — bug আসলে পুরোনো version-এ ফেরা যায়
✅ Code review — pull request-এ change review করা যায়
```

**Common mistakes:**
```
❌ Git-কে শুধু backup tool মনে করা
❌ Commit না করে সব কাজ local-এ রাখা
❌ Git শুধু team project-এর জন্য মনে করা (personal project-এও দরকার)
```

**Follow-up interview questions:**
- "Git এবং GitHub-এর পার্থক্য কী?"
- "Git কে তৈরি করেছেন এবং কেন?"
- "Distributed বলতে কী বোঝায়?"

---

<a id="p1-vcs"></a>
**Topic 2: Version Control System (VCS)**

**সংজ্ঞা:**
Version Control System (VCS) হলো এমন software যা সময়ের সাথে file-এর পরিবর্তন track করে। এটি দলের সদস্যদের coordinate করতে, পুরোনো version পুনরুদ্ধার করতে এবং পরিবর্তন compare করতে সাহায্য করে।

**VCS ছাড়া কী হয়:**
```
project/
├── app_v1.py
├── app_v2.py
├── app_v2_final.py
├── app_v2_final_REALLY_FINAL.py
├── app_backup_before_boss_change.py
└── app_DONT_DELETE.py
```

এই nightmare আপনার পরিচিত? VCS এই সমস্যার সমাধান করে।

**VCS-এর তিন ধরন:**

| ধরন | উদাহরণ | বৈশিষ্ট্য |
|-----|--------|-----------|
| Local VCS | RCS | শুধু নিজের machine-এ, team collaboration নেই |
| Centralized VCS | SVN, CVS | একটি central server, সবাই সেখান থেকে কাজ করে |
| Distributed VCS | Git, Mercurial | সবার কাছে পূর্ণ copy, offline কাজ করা যায় |

**VCS-এর সুবিধা:**
```
1. History — প্রতিটি পরিবর্তনের record
2. Collaboration — একাধিক developer একসাথে কাজ করতে পারে
3. Branching — parallel development সম্ভব
4. Backup — code হারানোর ভয় নেই
5. Accountability — কে কী পরিবর্তন করেছে জানা যায়
6. Rollback — যেকোনো সময় পুরোনো state-এ ফেরা যায়
```

**Interview tip:**
```
প্রশ্ন: "আপনি কি VCS ব্যবহার করেন? কেন?"

উত্তর: "হ্যাঁ, আমি Git ব্যবহার করি। VCS ছাড়া team project-এ কাজ করা
প্রায় অসম্ভব — কে কোন file পরিবর্তন করেছে, কখন bug introduce হয়েছে,
এই সব track করা যায় না। আমার সব personal project-ও Git-এ রাখি।"
```

---

<a id="p1-cvs-dvcs"></a>
**Topic 3: Centralized vs Distributed VCS**

এটি interview-এ প্রায়ই জিজ্ঞেস করা হয়।

**Centralized VCS (CVCS):**
```
        ┌─────────────────────┐
        │   Central Server    │
        │   (SVN/CVS repo)    │
        └────────┬────────────┘
                 │
    ┌────────────┼────────────┐
    │            │            │
┌───▼───┐   ┌───▼───┐   ┌───▼───┐
│Dev A  │   │Dev B  │   │Dev C  │
│Working│   │Working│   │Working│
│ Copy  │   │ Copy  │   │ Copy  │
└───────┘   └───────┘   └───────┘
```
- সবার কাছে শুধু **working copy** থাকে
- পুরো history শুধু **central server-এ**
- Server down হলে কেউ কাজ করতে পারে না
- উদাহরণ: **SVN (Subversion)**, CVS

**Distributed VCS (DVCS):**
```
     ┌──────────────────────┐
     │   Remote Repository  │
     │    (GitHub/GitLab)   │
     └──────────────────────┘
          ↑            ↑
    push/pull      push/pull
          │            │
┌─────────▼──┐   ┌─────▼──────────┐
│   Dev A    │   │     Dev B      │
│ Full Clone │   │  Full Clone    │
│ (History+  │   │  (History+     │
│  Working)  │   │   Working)     │
└────────────┘   └────────────────┘
```
- সবার কাছে **পূর্ণ repository** (সম্পূর্ণ history সহ)
- **Offline কাজ** করা যায়
- Server down হলেও local-এ সব কাজ চলে
- উদাহরণ: **Git**, Mercurial

**তুলনামূলক সারণী:**

| বিষয় | Centralized (SVN) | Distributed (Git) |
|------|------------------|------------------|
| History কোথায় | শুধু server-এ | সবার local-এও |
| Offline কাজ | না | হ্যাঁ |
| Speed | ধীর (network দরকার) | দ্রুত (local operation) |
| Branching | কঠিন, ধীর | সহজ, দ্রুত |
| Backup | Single point of failure | প্রতিটি clone = backup |
| Learning curve | সহজ | একটু জটিল |
| Popular use | Legacy enterprise | Modern software |

**Interview answer template:**
```
"Centralized VCS-এ যেমন SVN-এ, একটি central server থাকে এবং
সবাই সেখান থেকে checkout করে কাজ করে। Server down হলে কেউ কাজ
করতে পারে না।

Git-এর মতো Distributed VCS-এ, প্রতিটি developer-এর কাছে
পূর্ণ repository-র clone থাকে। তাই internet ছাড়াও commit, branch,
merge সব করা যায়। এটি faster, more flexible, এবং no single point
of failure — এই কারণেই আজকাল Git সবাই ব্যবহার করে।"
```

---

<a id="p1-architecture"></a>
**Topic 4: Git Architecture**

Git-এর ভেতরে কীভাবে কাজ করে — এটি বুঝলে বাকি সব সহজ হয়ে যায়।

**Git-এর তিনটি প্রধান area:**
```
┌─────────────────────────────────────────────────────────────┐
│                        Git Project                          │
│                                                             │
│  ┌──────────────┐  git add  ┌──────────────┐  git commit  │
│  │   Working    │ ────────► │   Staging    │ ────────────► │
│  │  Directory   │           │    Area      │               │
│  │              │ ◄──────── │  (Index)     │               │
│  │  (আপনার      │ git restore│              │               │
│  │   files)     │           │              │               │
│  └──────────────┘           └──────────────┘               │
│                                                      ┌──────┤
│                                                      │ .git │
│  ◄──────────────────────────── git checkout ─────── │ Repo │
│                                                      └──────┘
└─────────────────────────────────────────────────────────────┘
```

**Git Objects (ভেতরের structure):**

Git চারটি object type ব্যবহার করে:

| Object | কী করে | উদাহরণ |
|--------|--------|---------|
| **Blob** | File-এর content store করে | `hello.py`-এর content |
| **Tree** | Directory structure store করে | কোন blob কোন নামে |
| **Commit** | Snapshot + metadata | Author, message, parent |
| **Tag** | Specific commit mark করে | `v1.0.0` |

**SHA-1 হ্যাশিং:**
প্রতিটি Git object-এর একটি unique 40-character SHA-1 hash আছে:
```bash
commit 3a7f8b2c1d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a
Author: Alice <alice@example.com>
Date:   Mon May 12 10:00:00 2026
Message: feat: add login functionality
```

**Interview tip:**
```
প্রশ্ন: "Git কীভাবে changes track করে?"

উত্তর: "Git প্রতিটি commit-এ একটি complete snapshot নেয় (difference নয়)।
প্রতিটি file-এর content SHA-1 hash দিয়ে identify করা হয়। কোনো file না
পরিবর্তিত হলে Git সেই পুরোনো hash-এর reference রাখে — নতুন copy বানায় না।
এই কারণে Git খুব efficient।"
```

---

<a id="p1-repository"></a>
**Topic 5: Repository**

**সংজ্ঞা:**
Repository (সংক্ষেপে "repo") হলো সেই জায়গা যেখানে Git আপনার project-এর সম্পূর্ণ ইতিহাস এবং metadata store করে। এটি আপনার project folder-এর ভেতরে `.git` নামক hidden folder হিসেবে থাকে।

**Local vs Remote Repository:**

```
Local Repository          Remote Repository
(আপনার computer)          (GitHub/GitLab/Bitbucket)

┌──────────────────┐      ┌──────────────────────┐
│  my-project/     │      │  github.com/user/     │
│  ├── src/        │      │  my-project           │
│  ├── tests/      │ push │                       │
│  ├── README.md   │ ───► │  - সবার code share   │
│  └── .git/       │ pull │  - Backup             │
│      ├── objects │ ◄─── │  - Collaboration      │
│      ├── refs    │      │                       │
│      └── HEAD    │      └──────────────────────┘
└──────────────────┘
```

**`.git` folder-এর ভেতরে:**
```bash
.git/
├── HEAD          # current branch কোনটি
├── config        # local git config
├── index         # staging area
├── objects/      # সব blobs, trees, commits
│   ├── 3a/
│   │   └── 7f8b2c...  # SHA hash
│   └── pack/
├── refs/
│   ├── heads/    # local branches
│   └── remotes/  # remote branches
└── logs/         # reflog data
```

**Repository types:**
- **Bare repository:** শুধু `.git`-এর content, working directory নেই। Server-এ থাকে।
- **Non-bare repository:** Normal project folder + `.git`। আমরা সাধারণত এটাই ব্যবহার করি।

**Interview Q:**
```
প্রশ্ন: "`.git` folder delete করলে কী হবে?"

উত্তর: "`.git` folder delete করলে সেই project-এর পুরো Git history
চলে যাবে — সব commits, branches, configuration সব। তবে working
directory-র files থাকবে। এই কারণে `.git` folder কখনো manually
delete করা উচিত না।"
```

---

<a id="p1-three-areas"></a>
**Topic 6: Working Directory, Staging Area ও Commit History**

এই তিনটি area বোঝাই Git-এর সবচেয়ে গুরুত্বপূর্ণ concept।

**তিনটি area:**

```
Working Directory    Staging Area (Index)    Repository (.git)
─────────────────    ────────────────────    ─────────────────
আপনি যেখানে         git add করলে            git commit করলে
files edit করেন     files এখানে আসে         permanent snapshot
                                              তৈরি হয়
[Modified files]  →  [Staged files]       →  [Committed]
                  git add               git commit
```

**বাস্তব উপমা:**
```
Staging Area = রেস্টুরেন্টে order slip

আপনি menu থেকে items বেছে নিলেন (modified files)
→ Waiter-কে order দিলেন (git add) → order slip-এ লেখা হলো (staging area)
→ Kitchen-এ order গেল (git commit) → permanent record হলো (repository)

যেকোনো সময় order থেকে কোনো item বাদ দিতে পারেন
(git restore --staged) কিন্তু kitchen-এ গেলে (commit) সেটা history-তে থাকে।
```

**File states:**

| State | মানে | কীভাবে হয় |
|-------|------|----------|
| **Untracked** | Git এই file সম্পর্কে জানে না | নতুন file তৈরি করলে |
| **Modified** | Tracked file পরিবর্তিত হয়েছে | File edit করলে |
| **Staged** | Staging area-তে আছে | `git add` করলে |
| **Committed** | Repository-তে safe | `git commit` করলে |
| **Unmodified** | Track হচ্ছে, কোনো change নেই | After commit |

```bash
# File state flow:
# Untracked → Staged → Committed → Unmodified → Modified → Staged...

touch new-file.py          # Untracked
git add new-file.py        # Staged
git commit -m "add file"   # Committed / Unmodified
vim new-file.py            # Modified
git add new-file.py        # Staged again
git commit -m "update"     # Committed again
```

**Common interview question:**
```
প্রশ্ন: "Staging area কেন দরকার? সরাসরি commit করা যায় না?"

উত্তর: "Staging area একটি powerful feature। ধরুন আপনি ১০টি file
পরিবর্তন করেছেন — কিছু login feature-এর জন্য, কিছু bug fix-এর জন্য।
Staging area দিয়ে আপনি সিলেক্ট করে শুধু login feature-এর files
একসাথে commit করতে পারবেন, bug fix-এর files আলাদা commit-এ।
এতে Git history পরিষ্কার ও meaningful থাকে।"
```

---

<a id="p1-head"></a>
**Topic 7: HEAD**

**সংজ্ঞা:**
HEAD হলো একটি special pointer যা বর্তমানে আপনি কোন commit-এ আছেন সেটি নির্দেশ করে। সাধারণত HEAD কোনো branch-এর দিকে point করে, আর সেই branch সর্বশেষ commit-এর দিকে।

```
main branch:
A ── B ── C ── D
               ↑
             HEAD (বর্তমানে এখানে আছেন)
               ↑
              main
```

**HEAD কীভাবে কাজ করে:**
```bash
# .git/HEAD ফাইলের content:
ref: refs/heads/main

# .git/refs/heads/main এর content:
3a7f8b2c1d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a  # latest commit hash
```

**HEAD-এর বিভিন্ন অবস্থা:**

```
Normal (attached HEAD):
HEAD → main → commit D

After git checkout [commit-hash] (detached HEAD):
HEAD → commit B  (branch-এ নয়, directly commit-এ)

After git checkout feature:
HEAD → feature → commit F
```

**Detached HEAD (পরে বিস্তারিত আসবে):**
```bash
# Detached HEAD-এ যাওয়া
git checkout 3a7f8b2

# Warning দেখাবে:
# You are in 'detached HEAD' state.
# HEAD is now at 3a7f8b2 some old commit
```

**Interview tip:**
```
প্রশ্ন: "HEAD মানে কী?"

উত্তর: "HEAD হলো একটি pointer যা আমাদের current position নির্দেশ
করে — আমরা বর্তমানে কোন commit-এ বা কোন branch-এ কাজ করছি।
Normally HEAD একটি branch-এর দিকে point করে, সেই branch latest
commit-এর দিকে। 'Detached HEAD' মানে আমরা directly কোনো
commit-এ আছি, কোনো branch-এ নই।"
```

---

<a id="p1-install-config"></a>
**Topic 8: Git Installation ও Configuration**

**Installation:**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install git -y

# Linux (Fedora/RHEL)
sudo dnf install git -y

# macOS
brew install git
# অথবা: xcode-select --install (Xcode Command Line Tools)

# Windows
# git-scm.com থেকে installer download করুন

# Version check
git --version
# Output: git version 2.43.0
```

**First-time Setup (অবশ্যই করতে হবে):**
```bash
# আপনার নাম এবং email set করুন
git config --global user.name "আপনার নাম"
git config --global user.email "your@email.com"

# Default branch name (main ব্যবহার করুন — industry standard)
git config --global init.defaultBranch main

# Default editor
git config --global core.editor "code --wait"  # VS Code
git config --global core.editor "vim"           # Vim
git config --global core.editor "nano"          # Nano

# Line ending (OS compatibility)
git config --global core.autocrlf input   # Linux/macOS
git config --global core.autocrlf true    # Windows

# Color output
git config --global color.ui auto

# Useful alias (shortcut)
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.lg "log --oneline --graph --decorate --all"
```

**Config levels:**

| Level | File | Scope |
|-------|------|-------|
| `--system` | `/etc/gitconfig` | সব users, সব repos |
| `--global` | `~/.gitconfig` | এই user-এর সব repos |
| `--local` | `.git/config` | শুধু এই repo |

Local > Global > System (priority order)

**Config দেখুন:**
```bash
git config --list                    # সব config দেখুন
git config --global --list           # global config দেখুন
git config user.name                 # specific key দেখুন
cat ~/.gitconfig                     # config file সরাসরি দেখুন
```

**Interview common mistake:**
```
প্রশ্ন: "Git install করার পরে প্রথমে কী করবেন?"

ভুল উত্তর: "git init করব"

সঠিক উত্তর: "প্রথমে user.name এবং user.email configure করব।
এটি না করলে commit-এ author information সঠিক থাকবে না।
তারপর init.defaultBranch main সেট করব।"
```

---

<a id="p1-init-clone"></a>
**Topic 9: git init ও git clone**

**`git init` — নতুন repository তৈরি:**

```bash
# নতুন folder তৈরি করে git init
mkdir my-project
cd my-project
git init

# Output:
# Initialized empty Git repository in /home/user/my-project/.git/

# অথবা একসাথে:
git init my-project
cd my-project
```

`git init` করলে `.git` folder তৈরি হয় — এখান থেকেই Git tracking শুরু হয়।

```bash
# কী তৈরি হলো দেখুন
ls -la
# .git/  ← এই hidden folder-ই সব

ls .git/
# HEAD  config  description  hooks/  info/  objects/  refs/
```

**`git clone` — existing repository copy করা:**

```bash
# GitHub থেকে clone
git clone https://github.com/username/repo-name.git

# Custom folder name দিয়ে clone
git clone https://github.com/username/repo-name.git my-folder

# Specific branch clone
git clone -b develop https://github.com/username/repo-name.git

# Shallow clone (শুধু latest history, পুরো history নয়)
git clone --depth 1 https://github.com/username/repo-name.git

# SSH দিয়ে clone (SSH key setup থাকলে)
git clone git@github.com:username/repo-name.git
```

**init vs clone:**

| | git init | git clone |
|--|----------|-----------|
| ব্যবহার | নতুন project শুরু | existing repo copy |
| Remote | নিজে add করতে হয় | automatically set হয় |
| Files | শুধু `.git` | পুরো project + `.git` |
| History | শুরুতে নেই | পুরো history আসে |

**Clone-এর পরে কী কী হয়:**
```bash
git clone https://github.com/user/project.git
cd project

# Remote automatically "origin" নামে set হয়
git remote -v
# origin  https://github.com/user/project.git (fetch)
# origin  https://github.com/user/project.git (push)

# Default branch (সাধারণত main) automatically checkout হয়
git branch
# * main
```

**Interview question:**
```
প্রশ্ন: "git init এবং git clone-এর পার্থক্য কী?"

উত্তর: "git init দিয়ে একটি নতুন empty Git repository তৈরি করা হয়।
git clone দিয়ে একটি existing remote repository-এর সম্পূর্ণ copy
(সব history সহ) local machine-এ নামানো হয়। Clone-এ remote
automatically 'origin' নামে configure হয়ে যায়।"
```

---

<a id="p1-status"></a>
**Topic 10: git status**

**সংজ্ঞা:**
`git status` হলো Git-এর সবচেয়ে বেশি ব্যবহৃত command। এটি আপনার working directory এবং staging area-র বর্তমান অবস্থা দেখায়।

```bash
git status
```

**বিভিন্ন output বোঝা:**

**Clean state (কোনো change নেই):**
```bash
$ git status
On branch main
nothing to commit, working tree clean
```

**Untracked file:**
```bash
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        new-feature.py

nothing added to commit but untracked files present
```

**Modified file (tracked কিন্তু staged নয়):**
```bash
$ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   app.py

no changes added to commit
```

**Staged file (commit করার জন্য ready):**
```bash
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   new-feature.py
        modified:   app.py
```

**Mixed state:**
```bash
$ git status
On branch main
Changes to be committed:
        modified:   app.py          ← staged

Changes not staged for commit:
        modified:   utils.py        ← modified but not staged

Untracked files:
        test.py                     ← brand new file
```

**Short status:**
```bash
git status -s   # অথবা git status --short

# Output:
M  app.py       # M = Modified and staged
 M utils.py     # M = Modified but not staged (space = not staged)
?? test.py      # ?? = Untracked
A  new.py       # A = Added (new file staged)
D  old.py       # D = Deleted
```

**Interview tip:**
```
প্রশ্ন: "কাজ শুরুর আগে প্রথমে কী command দেন?"

উত্তর: "প্রথমে git status দিই — দেখি কোন branch-এ আছি,
কোনো uncommitted changes আছে কিনা। তারপর git pull দিই
latest changes নিতে। এই দুটো habit হয়ে গেছে।"
```

---

<a id="p1-add"></a>
**Topic 11: git add**

**সংজ্ঞা:**
`git add` command files-কে working directory থেকে staging area-তে নিয়ে যায় — অর্থাৎ commit-এর জন্য তৈরি করে।

**Syntax ও বিভিন্ন ব্যবহার:**

```bash
# Specific file add করুন
git add filename.py

# Multiple files
git add file1.py file2.py

# Current directory-র সব files (. = current directory)
git add .

# সব modified ও deleted files (new files বাদে)
git add -u
git add --update

# সব files (new + modified + deleted)
git add -A
git add --all

# Directory add করুন
git add src/

# Wildcard
git add *.py          # সব .py files
git add src/*.js      # src/ folder-এর সব .js files

# Interactive add (কোন parts add করবেন বেছে নিন)
git add -p            # অথবা --patch
git add -i            # অথবা --interactive
```

**Patch mode (`git add -p`) — interview-এ আলাদা marks:**
```bash
git add -p app.py

# প্রতিটি hunk (পরিবর্তিত section) দেখাবে:
# Stage this hunk [y,n,q,a,d,/,e,?]?
# y = yes, stage this hunk
# n = no, skip
# s = split into smaller hunks
# e = manually edit
# q = quit
```

এটি দিয়ে একটি file-এর কিছু অংশ stage করা যায়, বাকি অংশ রাখা যায়।

**Common mistakes:**

```bash
# ❌ সব সময় git add . করা — unnecessary files চলে যায়
git add .

# ✅ Specific files add করুন
git add src/feature.py tests/test_feature.py

# ❌ .gitignore ছাড়া git add .
# ✅ আগে .gitignore তৈরি করুন, তারপর git add .
```

**`.gitignore` — important:**
```bash
# .gitignore file (project root-এ)
node_modules/
__pycache__/
*.pyc
.env
.DS_Store
dist/
build/
*.log
.venv/
venv/
```

**Unstage করা:**
```bash
# Staging area থেকে file সরান (file পরিবর্তন হয় না)
git restore --staged filename.py

# আগের syntax (এখনো কাজ করে)
git reset HEAD filename.py
```

**Interview question:**
```
প্রশ্ন: "git add . এবং git add -A এর পার্থক্য কী?"

উত্তর: "git add . current directory এবং subdirectory-র
সব changes add করে — কিন্তু parent directory-তে কাজ করে না।
git add -A পুরো repository-র সব changes add করে, যেখানেই থাকুন।
Modern Git-এ (2.0+) দুটোর behavior প্রায় same হয়ে গেছে।"
```

---

<a id="p1-commit"></a>
**Topic 12: git commit**

**সংজ্ঞা:**
`git commit` staging area-র contents-কে repository-তে permanent snapshot হিসেবে save করে। প্রতিটি commit একটি unique SHA hash পায় এবং author, timestamp, message সহ store হয়।

**Basic commit:**
```bash
git commit -m "feat: add user login functionality"
```

**বিভিন্ন commit syntax:**
```bash
# Message সহ commit
git commit -m "fix: resolve null pointer exception in user service"

# Multi-line message
git commit -m "feat: add payment gateway

- Integrate Stripe API
- Add payment validation
- Handle refund scenarios"

# Stage করা ছাড়াই tracked files commit (git add -u + commit একসাথে)
git commit -am "fix: update config values"
# ⚠️ শুধু tracked (already committed) files-এর জন্য, new files নয়

# Editor খুলে message লিখুন
git commit

# শেষ commit fix করুন (push না করলে)
git commit --amend -m "feat: add user login functionality (fixed typo)"

# Empty commit (CI/CD trigger-এর জন্য)
git commit --allow-empty -m "chore: trigger CI pipeline"
```

**Commit anatomy:**
```
commit 3a7f8b2c1d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a
Author: Alice <alice@example.com>
Date:   Mon May 12 10:00:00 2026 +0600
    feat: add user authentication
    
    - Implement JWT token generation
    - Add password hashing with bcrypt
    - Create login/logout endpoints
```

**Conventional Commits format (Bangladesh companies-এ বেশি ব্যবহৃত):**

```
<type>(<scope>): <short description>

[optional body]

[optional footer]
```

| Type | ব্যবহার |
|------|---------|
| `feat` | নতুন feature |
| `fix` | Bug fix |
| `docs` | Documentation |
| `style` | Code formatting |
| `refactor` | Code restructure |
| `test` | Test add/fix |
| `chore` | Build, dependencies |
| `perf` | Performance |

```bash
# ভালো commit message examples:
git commit -m "feat(auth): add JWT refresh token"
git commit -m "fix(cart): prevent negative quantity"
git commit -m "docs: update API documentation"
git commit -m "refactor(user): extract validation logic to service"

# খারাপ commit message examples:
git commit -m "fix"              # ❌ অস্পষ্ট
git commit -m "wip"              # ❌ work in progress — share করবেন না
git commit -m "asdf"             # ❌ meaningless
git commit -m "updated stuff"    # ❌ কী update করলেন?
```

**Commit best practices:**
```
✅ Atomic commits — একটি commit = একটি logical change
✅ Present tense — "add feature" না "added feature"
✅ 50 chars limit subject line
✅ Body-তে "what" এবং "why" explain করুন
✅ Reference issue: "fix: resolve login bug (closes #42)"
❌ "final", "really final", "fixed" — meaningless
❌ একটি commit-এ অনেক unrelated changes
```

**Interview question:**
```
প্রশ্ন: "একটি ভালো commit message কেমন হওয়া উচিত?"

উত্তর: "আমি Conventional Commits format follow করি।
Subject line 50 characters-এর মধ্যে, present tense-এ।
যেমন: 'feat(auth): add password reset via email'।
Body-তে কেন এই change দরকার ছিল সেটা explain করি।
এতে code review সহজ হয় এবং changelog automatically
generate করা যায়।"
```

---

<a id="p1-log"></a>
**Topic 13: git log**

**সংজ্ঞা:**
`git log` commit history দেখায় — সব commits, তাদের hash, author, date, message।

**বিভিন্ন log format:**

```bash
# Default log
git log
# সব details দেখায়, q দিয়ে quit করুন

# One line per commit
git log --oneline
# 3a7f8b2 feat: add login
# b2c4d5e fix: resolve bug
# a1b2c3d initial commit

# Graph দেখান (branch visualization)
git log --oneline --graph --decorate --all
# * 3a7f8b2 (HEAD -> main, origin/main) feat: add login
# * b2c4d5e fix: resolve bug
# * a1b2c3d initial commit

# Last N commits
git log -5              # শেষ 5টি commit
git log -n 10           # শেষ 10টি commit

# Specific author
git log --author="Alice"
git log --author="alice@example.com"

# Date range
git log --since="2026-01-01"
git log --after="2 weeks ago"
git log --before="2026-05-01"
git log --since="2026-01-01" --until="2026-05-01"

# Specific file-এর history
git log -- filename.py
git log --follow filename.py   # rename track করে

# Commit message search
git log --grep="login"         # message-এ "login" আছে এমন commits
git log --grep="fix" -i        # case-insensitive

# Code search (কোন commit-এ এই code ছিল)
git log -S "function login"    # string খোঁজে
git log -G "def.*login"        # regex খোঁজে

# Stat দেখুন
git log --stat          # কোন files পরিবর্তিত হয়েছে
git log --shortstat     # সংক্ষিপ্ত stats

# Patch (actual diff)
git log -p              # full diff সহ
git log -p -1           # শেষ commit-এর diff
```

**Custom format:**
```bash
git log --pretty=format:"%h - %an, %ar : %s"
# 3a7f8b2 - Alice, 2 hours ago : feat: add login

# Format specifiers:
# %H = full hash, %h = short hash
# %an = author name, %ae = author email
# %ar = relative date, %ad = absolute date
# %s = subject (first line of message)
# %b = body
```

**Useful aliases:**
```bash
# ~/.gitconfig-এ add করুন
[alias]
    lg = log --oneline --graph --decorate --all
    lp = log -p --follow -S
    la = log --all --oneline --graph --decorate

# ব্যবহার:
git lg
git lp -- filename.py
```

**Interview question:**
```
প্রশ্ন: "নির্দিষ্ট কোনো function কখন কে পরিবর্তন করেছে কীভাবে বের করবেন?"

উত্তর: "দুটো উপায়:
1. git log -S 'function_name' -- filename.py
   — এই string কখন add/remove হয়েছে দেখাবে
2. git blame filename.py
   — প্রতিটি line কে কখন লিখেছে দেখাবে

দুটো command একসাথে ব্যবহার করলে সহজেই খুঁজে পাওয়া যায়।"
```

---

**PART 1 Quick Revision Table**

| Command/Concept | মূল কথা |
|----------------|---------|
| Git কী? | Distributed Version Control System |
| VCS কেন? | History track, collaboration, rollback |
| DVCS-এর সুবিধা | Offline কাজ, প্রতিটি clone = backup |
| Working Directory | যেখানে files edit করা হয় |
| Staging Area | Commit-এর আগের holding area |
| Commit | Permanent snapshot + metadata |
| HEAD | Current position (branch/commit) pointer |
| `git init` | নতুন repository তৈরি |
| `git clone` | Existing repo copy করা |
| `git status` | Current state দেখা |
| `git add .` | সব changes stage করা |
| `git add -p` | Selective staging (hunk by hunk) |
| `git commit -m` | Message সহ commit |
| `git commit --amend` | শেষ commit fix করা |
| `git log --oneline` | সংক্ষিপ্ত history |
| `git log --graph` | Branch visualization |
| Conventional Commits | `type(scope): description` format |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part2"></a>
## PART 2: Git Branching & Workflow

> Branch হলো Git-এর সবচেয়ে শক্তিশালী feature। এই PART-এ branching strategy, merge, rebase, conflict resolution থেকে শুরু করে real team workflow পর্যন্ত সব কিছু বিস্তারিত আলোচনা করা হয়েছে।

| # | বিষয় |
|---|-------|
| 1 | [Branch কী এবং কেন?](#p2-branch) |
| 2 | [git branch](#p2-git-branch) |
| 3 | [git checkout ও git switch](#p2-checkout-switch) |
| 4 | [git merge ও Fast-forward Merge](#p2-merge) |
| 5 | [Merge Conflict ও Resolution](#p2-conflict) |
| 6 | [git rebase](#p2-rebase) |
| 7 | [Cherry-pick](#p2-cherry-pick) |
| 8 | [Stash](#p2-stash) |
| 9 | [Tagging](#p2-tagging) |
| 10 | [Feature Branch Workflow](#p2-workflow) |
| 11 | [Git Flow Basics](#p2-gitflow) |

---

<a id="p2-branch"></a>
**Topic 1: Branch কী এবং কেন?**

**সংজ্ঞা:**
Branch হলো একটি independent line of development — মূল code থেকে আলাদা হয়ে নতুন feature বা bug fix তৈরির জায়গা। Branch আসলে একটি pointer যা একটি commit-কে নির্দেশ করে।

**বাস্তব উপমা:**
```
ধরুন আপনি একটি book লিখছেন (main branch)।
নতুন chapter পরীক্ষামূলকভাবে লিখতে চান?
Photocopy নিন এবং সেখানে লিখুন (feature branch)।
ভালো হলে original-এ যোগ করুন (merge)।
খারাপ হলে photocopy ফেলে দিন (branch delete)।
মূল book-এ কোনো প্রভাব নেই।
```

**Branch কেন দরকার:**
```
Team A:  ─── main ───────────────────────────────► production
                 \                       /
Team B:           ── feature/login ─────           নতুন feature
                 \               /
Team C:           ── fix/bug-123 ─                 bug fix (urgent)
```

**Branch-এর সুবিধা:**
```
✅ Isolated development — main code নিরাপদ থাকে
✅ Parallel work — একাধিক team একসাথে আলাদা feature
✅ Experimentation — পরীক্ষা করে দেখুন, ভুল হলে delete
✅ Code review — merge করার আগে review করা যায়
✅ Rollback — bad feature branch delete করলেই শেষ
```

**Branch = Lightweight pointer:**
```bash
# Branch create হওয়া মানে শুধু একটি pointer file তৈরি:
cat .git/refs/heads/main
# 3a7f8b2c1d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a

# নতুন branch = আরেকটি pointer file
cat .git/refs/heads/feature/login
# 3a7f8b2c1d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a  (same commit!)
```

Git-এ branch create করা প্রায় instantaneous — কারণ এটি শুধু একটি 41-byte file তৈরি করে।

---

<a id="p2-git-branch"></a>
**Topic 2: git branch**

```bash
# সব local branches দেখুন (* = current branch)
git branch
# * main
#   feature/login
#   fix/bug-123

# সব remote branches দেখুন
git branch -r
# origin/main
# origin/develop
# origin/feature/login

# সব branches (local + remote)
git branch -a

# নতুন branch তৈরি করুন (switch হয় না)
git branch feature/user-profile

# Branch তৈরি করে সেখানে switch করুন
git branch feature/user-profile
git checkout feature/user-profile
# অথবা একসাথে:
git checkout -b feature/user-profile
git switch -c feature/user-profile   # modern syntax

# Branch rename করুন
git branch -m old-name new-name           # current branch
git branch -m feature/old feature/new    # specific branch

# Branch delete করুন (merged হয়ে থাকলে)
git branch -d feature/login

# Force delete (merged না হলেও)
git branch -D feature/experimental

# Remote branch delete করুন
git push origin --delete feature/login
git push origin :feature/login   # old syntax

# Branch-এর last commit দেখুন
git branch -v
# * main          3a7f8b2 feat: add login
#   feature/login b2c4d5e fix: resolve bug

# Merged branches দেখুন
git branch --merged main     # main-এ already merged
git branch --no-merged main  # merge হয়নি এমন
```

**Branch naming convention (BD companies-এ popular):**
```
feature/user-authentication
feature/product-search-filter
fix/cart-quantity-bug
fix/login-redirect-issue
hotfix/security-xss-patch
release/v2.1.0
chore/upgrade-dependencies
refactor/payment-service
docs/api-documentation
test/integration-tests
```

**Interview question:**
```
প্রশ্ন: "Branch delete করলে সেই branch-এর commits কি চলে যায়?"

উত্তর: "না, commits চলে যায় না — শুধু pointer (branch name) delete হয়।
তবে যদি সেই commits অন্য branch বা tag দিয়ে reachable না হয়, তাহলে
eventually Git garbage collection-এ সেগুলো মুছে যেতে পারে (কিছু সময়
পরে)। Merge করার পরে branch delete করলে commits main-এ থাকে।"
```

---

<a id="p2-checkout-switch"></a>
**Topic 3: git checkout ও git switch**

**`git checkout` — traditional (এখনো widely used):**
```bash
# Branch-এ switch করুন
git checkout main
git checkout feature/login

# নতুন branch তৈরি করে switch
git checkout -b feature/payment

# Remote branch থেকে local branch তৈরি
git checkout -b feature/login origin/feature/login
git checkout --track origin/feature/login  # same as above

# Specific file restore করুন (staging থেকে working directory-তে)
git checkout -- filename.py

# Specific commit checkout (detached HEAD)
git checkout 3a7f8b2

# Tag checkout
git checkout v1.0.0
```

**`git switch` — modern (Git 2.23+, recommended):**
```bash
# Branch switch
git switch main
git switch feature/login

# নতুন branch তৈরি করে switch
git switch -c feature/payment    # -c = --create

# Remote branch track করুন
git switch --track origin/feature/login

# আগের branch-এ ফিরে যান
git switch -
```

**checkout vs switch:**

| Feature | git checkout | git switch |
|---------|-------------|-----------|
| Branch switch | ✅ | ✅ (preferred) |
| New branch | `checkout -b` | `switch -c` |
| File restore | ✅ (confusing) | ❌ (use `git restore`) |
| Detached HEAD | ✅ | `switch --detach` |
| Modern? | No (legacy) | Yes (2.23+) |

**`git restore` — file restoration (Git 2.23+):**
```bash
# Working directory changes discard (undo modification)
git restore filename.py
git restore .           # সব files

# Unstage করুন (staging area → working directory)
git restore --staged filename.py
git restore --staged .

# Specific commit থেকে restore
git restore --source=HEAD~2 filename.py
```

**Common interview trap:**
```
প্রশ্ন: "git checkout main এবং git switch main-এর পার্থক্য কী?"

উত্তর: "Functionally একই — দুটোই branch switch করে। তবে git switch
শুধু branch switching-এর জন্য তৈরি, আর git checkout অনেক কাজ করে
(branch switch, file restore, detached HEAD) — এই কারণে confusing।
Git 2.23 থেকে git switch এবং git restore এনেছে responsibilities
আলাদা করতে। Modern project-এ git switch prefer করি।"
```

---

<a id="p2-merge"></a>
**Topic 4: git merge ও Fast-forward Merge**

**সংজ্ঞা:**
`git merge` একটি branch-এর changes অন্য branch-এ যোগ করে।

**দুই ধরনের merge:**

**1. Fast-forward Merge:**
```
Before merge:
main:    A ─── B
                \
feature:         C ─── D

main branch থেকে feature branch তৈরির পর
main-এ নতুন commit নেই — তাই fast-forward সম্ভব।

After git merge feature (fast-forward):
main:    A ─── B ─── C ─── D
                              ↑
                            HEAD (main)
```

```bash
git checkout main
git merge feature/login

# Output:
# Updating b2c4d5e..3a7f8b2
# Fast-forward
#  login.py | 50 ++++++++++++++
```

Fast-forward merge-এ কোনো merge commit তৈরি হয় না — শুধু pointer এগিয়ে যায়।

**2. Three-way Merge (Merge Commit):**
```
Before:
main:    A ─── B ─── E ─── F
                \
feature:         C ─── D

main-এ নতুন commits (E, F) আছে — fast-forward সম্ভব নয়।

After git merge feature:
main:    A ─── B ─── E ─── F ─── M (merge commit)
                \                /
feature:         C ─────── D ───
```

```bash
git checkout main
git merge feature/login

# Output:
# Merge made by the 'ort' strategy.
#  login.py | 50 ++++++++++++++
# 1 file changed, 50 insertions(+)
```

**Merge options:**

```bash
# Default merge
git merge feature/login

# No fast-forward — সবসময় merge commit তৈরি করে
git merge --no-ff feature/login

# Squash merge — feature-এর সব commits একটিতে মিশিয়ে দেয়
git merge --squash feature/login
# তারপর আলাদা commit করতে হবে:
git commit -m "feat: add login functionality"

# Merge abort করুন (conflict-এ)
git merge --abort

# Merge-এর message দিন
git merge -m "Merge feature/login into main" feature/login
```

**Fast-forward vs No-fast-forward:**

| | Fast-forward | No-fast-forward (--no-ff) |
|--|-------------|--------------------------|
| Merge commit | নেই | আছে |
| History | Linear | Branch visible |
| Revert সহজ? | কঠিন | সহজ (single commit revert) |
| Recommended | Simple fixes | Feature branches |

**Interview question:**
```
প্রশ্ন: "Fast-forward merge কখন হয়? কখন three-way merge হয়?"

উত্তর: "Fast-forward merge হয় যখন merge করার target branch
(যেমন main) source branch তৈরির পরে কোনো নতুন commit পায়নি।
তখন Git শুধু pointer এগিয়ে দেয় — কোনো merge commit লাগে না।

Three-way merge হয় যখন উভয় branch-এই নতুন commits আছে।
Git তখন common ancestor খুঁজে, দুই branch-এর changes combine করে,
একটি new merge commit তৈরি করে।"
```

---

<a id="p2-conflict"></a>
**Topic 5: Merge Conflict ও Resolution**

**Conflict কখন হয়:**
দুটো branch-এ একই file-এর একই জায়গায় ভিন্ন পরিবর্তন হলে Git নিজে সিদ্ধান্ত নিতে পারে না — conflict হয়।

```
main branch-এ:
def greet():
    return "Hello, World!"

feature branch-এ:
def greet():
    return "Namaste, World!"

Merge করলে Git কোনটা রাখবে জানে না → Conflict!
```

**Conflict কেমন দেখায়:**
```python
def greet():
<<<<<<< HEAD
    return "Hello, World!"    # main branch-এর version
=======
    return "Namaste, World!"  # feature branch-এর version
>>>>>>> feature/greeting
```

**Conflict markers:**
```
<<<<<<< HEAD          → current branch (HEAD)-এর content
=======               → separator
>>>>>>> branch-name   → merging branch-এর content
```

**Step-by-step conflict resolution:**

```bash
# Step 1: Merge শুরু করুন
git checkout main
git merge feature/greeting

# Output:
# Auto-merging greet.py
# CONFLICT (content): Merge conflict in greet.py
# Automatic merge failed; fix conflicts and then commit the result.

# Step 2: Conflict দেখুন
git status
# Unmerged paths:
#   both modified: greet.py

# Step 3: File খুলুন এবং manually resolve করুন
# conflict markers সরিয়ে সঠিক code রাখুন:

def greet(language="en"):
    if language == "bn":
        return "Namaste, World!"
    return "Hello, World!"

# Step 4: Resolved file stage করুন
git add greet.py

# Step 5: Commit করুন
git commit
# Git automatically merge commit message দেবে
# অথবা: git commit -m "merge: resolve greeting conflict"

# অথবা abort করুন যদি resolve করতে না চান
git merge --abort
```

**Visual merge tools:**
```bash
# Built-in mergetool
git mergetool

# VS Code (recommended)
git config --global merge.tool vscode
git config --global mergetool.vscode.cmd 'code --wait $MERGED'

# IntelliJ IDEA
git config --global merge.tool intellij

# vimdiff
git mergetool --tool=vimdiff
```

**Conflict prevention strategies:**
```
✅ Feature branch-গুলো ছোট রাখুন
✅ Regularly main থেকে update নিন (git merge main / git rebase main)
✅ একটি file-এ অনেক unrelated কাজ করবেন না
✅ Team-এ communicate করুন — কে কোন file কাজ করছে
✅ Pull করার আগে commit করুন
```

**Interview question:**
```
প্রশ্ন: "Merge conflict হলে কীভাবে solve করেন?"

উত্তর: "প্রথমে git status দিয়ে কোন files conflict-এ আছে দেখি।
তারপর সেই files-গুলো VS Code বা mergetool-এ খুলি।
<<<<<<< HEAD, =======, >>>>>>> markers দেখি।
দুটো change বুঝে manually সঠিক code রাখি।
Conflict markers সব মুছি।
git add দিয়ে resolved files stage করি।
git commit দিয়ে merge complete করি।

Complex conflict-এ team member-কে জিজ্ঞেস করি
কারণ একা ভুল সিদ্ধান্ত নেওয়ার চেয়ে জিজ্ঞেস করা ভালো।"
```

---

<a id="p2-rebase"></a>
**Topic 6: git rebase**

**সংজ্ঞা:**
Rebase মানে একটি branch-এর commits-কে অন্য base commit-এর উপরে নতুন করে apply করা — history পরিষ্কার ও linear রাখার জন্য।

**Merge vs Rebase:**

```
Initial state:
main:    A ─── B ─── E
                \
feature:         C ─── D

After git merge (three-way):
main:    A ─── B ─── E ─── M
                \          /
feature:         C ─── D ─

History: non-linear কিন্তু truthful

After git rebase main (on feature branch):
main:    A ─── B ─── E
                      \
feature:               C' ─── D'

History: linear, C এবং D নতুন commits হিসেবে E-এর উপরে বসেছে
```

**Rebase করার ধাপ:**
```bash
# feature branch-এ আছেন
git checkout feature/login

# main-এর latest-এর উপরে rebase করুন
git rebase main

# Conflict হলে:
# 1. Conflict resolve করুন
# 2. git add resolved-file.py
# 3. git rebase --continue
# অথবা abort করতে: git rebase --abort

# Rebase সম্পূর্ণ হওয়ার পরে main-এ merge (fast-forward হবে)
git checkout main
git merge feature/login  # Fast-forward merge
```

**Interactive Rebase (`git rebase -i`) — powerful:**
```bash
# শেষ 3টি commit-কে interactive-ভাবে edit করুন
git rebase -i HEAD~3

# Editor খুলবে:
pick 3a7f8b2 feat: add login form
pick b2c4d5e fix: fix typo in login
pick a1b2c3d feat: add logout

# Commands:
# pick = keep as is
# reword = commit রাখো, message change করো
# edit = commit রাখো, content amend করো
# squash = আগের commit-এর সাথে merge করো
# fixup = squash কিন্তু message বাদ দাও
# drop = এই commit delete করো
# s = squash (shorthand)
# f = fixup (shorthand)
```

**Squash example:**
```bash
git rebase -i HEAD~3

# Change to:
pick 3a7f8b2 feat: add login form
squash b2c4d5e fix: fix typo in login     # এই commit আগেরটায় merge হবে
squash a1b2c3d feat: add logout           # এটাও

# Save করুন → নতুন combined commit message দিন
# Result: একটি clean commit তৈরি হবে
```

**Rebase rules (CRITICAL):**
```
⚠️  GOLDEN RULE: Never rebase shared/public commits!

✅ Local branch rebase করা safe
✅ Push করার আগে rebase করা safe
✅ feature branch-কে main-এর উপরে rebase করা safe

❌ main branch rebase করবেন না
❌ Already pushed commits rebase করবেন না
   (অন্যরা যে commits use করছে সেগুলো rebase করলে
   তাদের repository corrupt হয়ে যেতে পারে)
```

**Merge vs Rebase কখন কোনটা:**

| | Merge | Rebase |
|--|-------|--------|
| History | Real (non-linear) | Clean (linear) |
| Merge commit | আছে | নেই |
| Public commits? | ✅ Safe | ❌ Avoid |
| Feature work? | ✅ OK | ✅ Preferred |
| Controversy | কম | বেশি |

**Interview question:**
```
প্রশ্ন: "Merge এবং Rebase-এর পার্থক্য কী? কখন কোনটা ব্যবহার করবেন?"

উত্তর: "Merge দুটো branch-এর history preserve করে একটি merge commit
তৈরি করে। History non-linear কিন্তু truthful।

Rebase feature branch-এর commits-কে target branch-এর latest-এর
উপরে reapply করে — history linear ও clean থাকে।

আমি সাধারণত: local feature branch update রাখতে git rebase main ব্যবহার করি।
Final merge-এ --no-ff দিয়ে merge করি যাতে branch history বোঝা যায়।

GOLDEN RULE: Already pushed/shared commits কখনো rebase করব না —
এটি team-এর সবার repo-তে problem তৈরি করে।"
```

---

<a id="p2-cherry-pick"></a>
**Topic 7: Cherry-pick**

**সংজ্ঞা:**
Cherry-pick মানে অন্য কোনো branch থেকে specific commit(s) বর্তমান branch-এ apply করা — পুরো branch merge না করে।

**কখন দরকার:**
```
Scenario: develop branch-এ একটি critical bug fix আছে (commit X)।
সেই fix আজকেই main/production-এ দরকার,
কিন্তু develop-এর বাকি half-done features main-এ নেওয়া যাবে না।
Solution: Cherry-pick করুন শুধু সেই fix commit।
```

```
develop: A ─── B ─── X (fix) ─── C ─── D (WIP features)
main:    A ─── B

Cherry-pick X:
main:    A ─── B ─── X' (same fix, new hash)
```

**Cherry-pick commands:**
```bash
# Single commit cherry-pick
git cherry-pick 3a7f8b2

# Multiple commits
git cherry-pick 3a7f8b2 b2c4d5e

# Range (A থেকে B পর্যন্ত, A বাদে)
git cherry-pick A..B

# Range (A সহ)
git cherry-pick A^..B

# Commit না করে শুধু changes apply করুন
git cherry-pick --no-commit 3a7f8b2
git cherry-pick -n 3a7f8b2

# Conflict হলে:
# 1. Resolve conflict
# 2. git add .
# 3. git cherry-pick --continue
# অথবা: git cherry-pick --abort
```

**Cherry-pick workflow:**
```bash
# 1. Fix commit hash খুঁজুন
git log develop --oneline
# abc1234 fix: critical security vulnerability
# def5678 feat: half-done new dashboard

# 2. main-এ যান
git checkout main

# 3. Only the fix cherry-pick করুন
git cherry-pick abc1234

# 4. Push করুন
git push origin main
```

**Common mistake:**
```
❌ Cherry-pick abuse — বারবার একই fix multiple branches-এ করা
✅ Better: একটি shared fix branch, সব branches সেখান থেকে merge করুক
```

**Interview question:**
```
প্রশ্ন: "Cherry-pick কী? কোন situation-এ ব্যবহার করবেন?"

উত্তর: "Cherry-pick দিয়ে অন্য branch-এর নির্দিষ্ট commit(s)
বর্তমান branch-এ apply করা যায়।

Hotfix scenario-তে বেশি ব্যবহার হয়: develop branch-এ critical fix
আছে, production (main) branch-এ শুধু সেই fix দরকার — বাকি
in-progress features নয়। তখন git cherry-pick [fix-commit-hash]।"
```

---

<a id="p2-stash"></a>
**Topic 8: git stash**

**সংজ্ঞা:**
Stash হলো temporary storage — uncommitted changes সরিয়ে রাখার জায়গা। কাজ করার মাঝে জরুরি অন্য কাজ করতে হলে বর্তমান অসম্পূর্ণ কাজ stash করে রাখা যায়।

**বাস্তব উপমা:**
```
আপনি রান্না করছেন (feature কাজ করছেন)।
হঠাৎ ফোন এলো — গুরুত্বপূর্ণ message reply করতে হবে (urgent bug fix)।
রান্না থামিয়ে ফোন ধরলেন (stash করলেন)।
Message reply করলেন (bug fix commit করলেন)।
আবার রান্নায় ফিরলেন (stash pop করলেন)।
```

**Stash commands:**
```bash
# Current changes stash করুন
git stash
git stash push          # same as git stash

# Message সহ stash (recommended)
git stash push -m "WIP: half-done login form"

# Untracked files-ও stash করুন
git stash push -u
git stash push --include-untracked

# Ignored files-ও stash করুন
git stash push -a
git stash push --all

# Specific files stash করুন
git stash push -m "WIP" -- src/login.py src/utils.py

# Stash list দেখুন
git stash list
# stash@{0}: WIP on feature/login: abc1234 feat: add form
# stash@{1}: WIP on main: def5678 fix: resolve bug

# Latest stash apply করুন (stash থেকে সরায় না)
git stash apply
git stash apply stash@{1}   # specific stash

# Latest stash apply করুন এবং stash থেকে সরান
git stash pop
git stash pop stash@{1}     # specific stash

# Stash-এর content দেখুন
git stash show
git stash show -p           # full diff

# Stash থেকে new branch তৈরি করুন
git stash branch feature/new-branch stash@{1}

# Specific stash delete করুন
git stash drop stash@{0}

# সব stash clear করুন
git stash clear
```

**Common workflow:**
```bash
# feature branch-এ কাজ করছেন
git checkout feature/login
# ... কিছু code লিখলেন ...

# Urgent: main-এ bug fix দরকার
git stash push -m "WIP: login form validation"

# main-এ যান
git checkout main
git pull origin main

# Hotfix branch তৈরি করুন
git checkout -b hotfix/null-pointer
# ... fix করলেন ...
git commit -m "fix: resolve null pointer in user service"
git checkout main
git merge hotfix/null-pointer
git push origin main

# Feature branch-এ ফিরুন
git checkout feature/login
git stash pop  # কাজ ফিরে পান
```

**Interview question:**
```
প্রশ্ন: "git stash এবং git commit-এর পার্থক্য কী? কখন stash ব্যবহার করবেন?"

উত্তর: "git commit permanent snapshot তৈরি করে repository-তে।
git stash temporary storage — uncommitted changes সরিয়ে রাখে
কিন্তু history-তে যায় না।

Stash ব্যবহার করি যখন: কাজের মাঝে হঠাৎ অন্য branch-এ যেতে হয়
কিন্তু current কাজ commit করার মতো ready নয়। অর্থাৎ WIP (Work in
Progress) অবস্থায় branch switch করতে হলে।"
```

---

<a id="p2-tagging"></a>
**Topic 9: Tagging**

**সংজ্ঞা:**
Tag হলো specific commit-এর একটি named reference — সাধারণত software release-এ ব্যবহার হয়। Branch-এর মতো move করে না, একটি fixed point।

**Tag types:**

| Type | বৈশিষ্ট্য | ব্যবহার |
|------|-----------|---------|
| **Lightweight** | শুধু commit hash | Quick temporary mark |
| **Annotated** | Message, author, date, sign করা যায় | Release versions |

```bash
# Lightweight tag
git tag v1.0

# Annotated tag (recommended for releases)
git tag -a v1.0.0 -m "Release version 1.0.0 — first stable release"

# Specific commit-এ tag
git tag -a v0.9.0 -m "Beta release" 3a7f8b2

# সব tags দেখুন
git tag
git tag -l "v1.*"    # pattern match

# Tag details দেখুন
git show v1.0.0

# Remote-এ push করুন (push by default tags পাঠায় না)
git push origin v1.0.0       # specific tag
git push origin --tags       # সব tags

# Tag delete করুন
git tag -d v0.9.0            # local delete
git push origin --delete v0.9.0  # remote delete

# Tag checkout (detached HEAD)
git checkout v1.0.0

# Tag থেকে branch তৈরি
git checkout -b hotfix/v1.0.1 v1.0.0
```

**Semantic Versioning (SemVer) — industry standard:**
```
v{MAJOR}.{MINOR}.{PATCH}

v1.0.0 → Initial release
v1.1.0 → New feature (backward compatible)
v1.1.1 → Bug fix
v2.0.0 → Breaking change

Pre-release:
v2.0.0-alpha.1
v2.0.0-beta.3
v2.0.0-rc.1  (Release Candidate)
```

**Interview question:**
```
প্রশ্ন: "Git tag কী? Branch-এর সাথে পার্থক্য কী?"

উত্তর: "Tag হলো specific commit-এর একটি fixed label, সাধারণত
release version mark করতে। v1.0.0, v2.1.3 এই format-এ।

Branch-এর সাথে পার্থক্য: Branch নতুন commit-এর সাথে move করে।
Tag static — সবসময় একই commit-এ থাকে।
Tag release point mark করার জন্য, branch development-এর জন্য।"
```

---

<a id="p2-workflow"></a>
**Topic 10: Feature Branch Workflow**

Feature Branch Workflow হলো সবচেয়ে common এবং Bangladeshi companies-এ সবচেয়ে বেশি ব্যবহৃত workflow।

**Core concept:**
```
✅ প্রতিটি feature / bug fix / task-এর জন্য আলাদা branch
✅ main (বা develop) branch সবসময় deployable
✅ Feature complete হলে Pull Request → code review → merge
```

**Complete workflow:**

```bash
# ──────────────────────────────────────────────────
# STEP 1: Latest code নিন
# ──────────────────────────────────────────────────
git checkout main
git pull origin main

# ──────────────────────────────────────────────────
# STEP 2: Feature branch তৈরি করুন
# ──────────────────────────────────────────────────
git checkout -b feature/user-authentication

# ──────────────────────────────────────────────────
# STEP 3: কাজ করুন, atomic commits করুন
# ──────────────────────────────────────────────────
# ... code লিখুন ...
git add src/auth/
git commit -m "feat(auth): add user model with password hashing"

# ... আরো code ...
git add src/auth/ tests/
git commit -m "feat(auth): implement JWT token generation"

# ... আরো code ...
git add src/auth/ src/routes/
git commit -m "feat(auth): add login and logout endpoints"

# ──────────────────────────────────────────────────
# STEP 4: Regularly main থেকে update নিন
# ──────────────────────────────────────────────────
git fetch origin
git rebase origin/main
# অথবা: git merge origin/main

# ──────────────────────────────────────────────────
# STEP 5: Remote-এ push করুন
# ──────────────────────────────────────────────────
git push origin feature/user-authentication

# ──────────────────────────────────────────────────
# STEP 6: Pull Request তৈরি করুন GitHub-এ
# ──────────────────────────────────────────────────
# GitHub UI-তে:
# - Base: main, Compare: feature/user-authentication
# - Description লিখুন (কী করেছেন, কেন, how to test)
# - Reviewers assign করুন
# - Labels: feature, ready-for-review

# ──────────────────────────────────────────────────
# STEP 7: Code review ও requested changes
# ──────────────────────────────────────────────────
# Review comment এলে:
git add .
git commit -m "refactor(auth): address code review feedback"
git push origin feature/user-authentication

# ──────────────────────────────────────────────────
# STEP 8: Merge (after approval)
# ──────────────────────────────────────────────────
# GitHub-এ "Merge pull request" button
# অথবা locally:
git checkout main
git merge --no-ff feature/user-authentication
git push origin main

# ──────────────────────────────────────────────────
# STEP 9: Branch cleanup
# ──────────────────────────────────────────────────
git branch -d feature/user-authentication
git push origin --delete feature/user-authentication
```

**Diagram:**
```
main:    ─────────────────────────────────────► production
              \                         /
feature:       ──C──D──E──F──G─────────
               ↑                       ↑
            git checkout -b         PR merge
```

**Pull Request description template:**
```markdown
## কী পরিবর্তন করেছি
- User authentication system add করেছি
- JWT token-based login/logout implement করেছি
- Password bcrypt দিয়ে hash করা হচ্ছে

## কেন এই পরিবর্তন
Issue #45 — User authentication এখনো নেই, এটি v2.0 milestone-এর জন্য দরকার

## কীভাবে test করবেন
1. `python manage.py runserver`
2. POST /api/auth/login — body: {"email": "test@example.com", "password": "test123"}
3. 200 response-এ JWT token পাবেন

## Checklist
- [x] Unit tests added
- [x] API documentation updated
- [x] No hardcoded secrets
- [x] Migration files included
```

---

<a id="p2-gitflow"></a>
**Topic 11: Git Flow Basics**

**Git Flow** হলো Vincent Driessen-এর তৈরি একটি branch management model — বড় project-এ structured release management-এর জন্য।

**Git Flow-এর branches:**

```
main ──────────────────────────────────────► (production releases)
  │                              ↑
  │                          release/1.0
  │                         /            \
develop ────────────────────────────────────► (integration)
  │       \                  ↑          ↑
  │        feature/login     │          │
  │         \      /         │          │
  │          ──────     hotfix/fix  feature/payment
  │                         /
  └── (hotfix merged to both main and develop)
```

**Branches-এর role:**

| Branch | Role | Lifetime |
|--------|------|---------|
| `main` | Production code, tagged releases | Permanent |
| `develop` | Integration branch, next release | Permanent |
| `feature/*` | নতুন feature development | Temporary |
| `release/*` | Release preparation, final testing | Temporary |
| `hotfix/*` | Production bug fix (urgent) | Temporary |

**Git Flow কমান্ড (git-flow extension):**
```bash
# Install
sudo apt install git-flow   # Linux

# Initialize
git flow init

# Feature শুরু
git flow feature start user-login
# → develop থেকে feature/user-login তৈরি হয়

# Feature শেষ
git flow feature finish user-login
# → develop-এ merge হয়, branch delete হয়

# Release শুরু
git flow release start 1.0.0
# → develop থেকে release/1.0.0 তৈরি হয়

# Release শেষ
git flow release finish 1.0.0
# → main-এ merge, develop-এ merge, tag v1.0.0

# Hotfix শুরু (main থেকে)
git flow hotfix start fix-null-pointer
# → main থেকে hotfix/fix-null-pointer তৈরি হয়

# Hotfix শেষ
git flow hotfix finish fix-null-pointer
# → main ও develop উভয়ে merge, tag তৈরি
```

**Simple GitHub Flow (আধুনিক, ছোট team-এর জন্য):**
```
1. main থেকে branch তৈরি
2. Commit করুন
3. Pull Request খুলুন
4. Review ও discuss
5. Deploy করুন (staging-এ test)
6. main-এ merge করুন
```

**কোন workflow কখন:**

| Workflow | কখন ব্যবহার করবেন |
|----------|-----------------|
| Feature Branch | Small-medium team, continuous deployment |
| Git Flow | Large team, scheduled releases, multiple versions |
| GitHub Flow | CI/CD heavy, frequent deployments, startups |
| Trunk-based | Advanced teams, feature flags ব্যবহার করে |

**Interview question:**
```
প্রশ্ন: "আপনার team-এ কোন Git workflow follow করেন?"

উত্তর: "আমরা Feature Branch Workflow follow করি। প্রতিটি feature বা
bug fix-এর জন্য main/develop থেকে আলাদা branch তৈরি করি।
কাজ শেষে Pull Request দিয়ে code review হয়, approve হলে merge করা হয়।

বড় release-ভিত্তিক project-এ Git Flow use হয় — সেখানে develop,
release, hotfix branches থাকে। আমাদের project-এ continuous deployment
তাই GitHub Flow-এর মতো simpler approach।"
```

---

**PART 2 Quick Revision Table**

| Command/Concept | মূল কথা |
|----------------|---------|
| Branch কী? | Commit-এর lightweight pointer, independent development line |
| `git branch -b name` | Branch তৈরি করুন (`-b` = create) |
| `git switch -c name` | Modern branch create + switch |
| `git merge --no-ff` | Merge commit সহ merge |
| Fast-forward merge | Main-এ নতুন commit নেই, pointer এগিয়ে যায় |
| Three-way merge | উভয়েই নতুন commit, merge commit তৈরি হয় |
| Conflict কখন? | একই file-এর একই জায়গায় different changes |
| Conflict markers | `<<<<< HEAD`, `=====`, `>>>>> branch` |
| `git rebase main` | Feature commits-কে main-এর উপরে reapply |
| Rebase golden rule | Public commits কখনো rebase করবেন না |
| Cherry-pick | Specific commit(s) অন্য branch-এ apply |
| `git stash push -m` | Named temporary storage |
| `git stash pop` | Latest stash apply + remove |
| Annotated tag | `git tag -a v1.0.0 -m "message"` |
| Feature Branch Workflow | Branch → commit → PR → review → merge |
| Git Flow | main + develop + feature + release + hotfix |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 3 — Advanced Git *(Next request এ লিখব)*
