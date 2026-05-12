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

> **📌 পরবর্তী:** PART 3 — Advanced Git

---

<a id="part3"></a>
## PART 3: Advanced Git

> Git-এর deep internals এবং power features। এই PART-এ Detached HEAD, Reset vs Revert, Reflog, Interactive Rebase, Hooks, Submodules এবং Git-এর object model বিস্তারিত আলোচনা করা হয়েছে।

| # | বিষয় |
|---|-------|
| 1 | [Detached HEAD State](#p3-detached-head) |
| 2 | [git reset — Soft, Mixed, Hard](#p3-reset) |
| 3 | [git revert](#p3-revert) |
| 4 | [Reset vs Revert — কখন কোনটা](#p3-reset-vs-revert) |
| 5 | [git reflog — Time Machine](#p3-reflog) |
| 6 | [Squash Commits ও Interactive Rebase](#p3-squash) |
| 7 | [Git Hooks](#p3-hooks) |
| 8 | [Git Submodules](#p3-submodules) |
| 9 | [Git Internals — Object Model](#p3-internals) |
| 10 | [SHA Hashing Basics](#p3-sha) |
| 11 | [Recovery Strategies](#p3-recovery) |

---

<a id="p3-detached-head"></a>
**Topic 1: Detached HEAD State**

**সংজ্ঞা:**
Normally HEAD একটি branch-এর দিকে point করে, সেই branch latest commit-এর দিকে। **Detached HEAD** মানে HEAD সরাসরি একটি commit-এর দিকে point করছে — কোনো branch-এ নয়।

```
Normal (Attached HEAD):
A ─── B ─── C ─── D
                   ↑
                  main ← HEAD

Detached HEAD (after: git checkout B):
A ─── B ─── C ─── D
      ↑              ↑
    HEAD            main
```

**কীভাবে Detached HEAD হয়:**
```bash
# Specific commit checkout করলে
git checkout 3a7f8b2

# Tag checkout করলে
git checkout v1.0.0

# Remote branch directly checkout করলে
git checkout origin/main

# HEAD~N syntax
git checkout HEAD~3
```

**Warning message:**
```
$ git checkout 3a7f8b2
Note: switching to '3a7f8b2'.

You are in 'detached HEAD' state. You can look around, make
experimental changes and commit them, and you can discard any
commits you make in this state without impacting any branches
by switching back to a branch.

If you want to create a new branch to retain commits you make,
you may do so (now or later) by using -c with the switch command.
HEAD is now at 3a7f8b2 feat: add login
```

**Detached HEAD-এ করা commits হারিয়ে যাওয়ার বিপদ:**
```bash
# Detached HEAD-এ commit করলেন
git checkout 3a7f8b2
# code edit করলেন...
git commit -m "experiment: test something"
# নতুন commit hash: abc1234

# Branch-এ ফিরে গেলেন
git checkout main
# এখন abc1234 কোনো branch-এ নেই — unreachable!
# Git garbage collection-এ মুছে যাবে
```

**Detached HEAD থেকে বের হওয়া:**
```bash
# Option 1: কোনো branch-এ ফিরে যান (changes হারিয়ে যাবে)
git checkout main
git switch main

# Option 2: Detached HEAD-এর commits save করুন (নতুন branch)
git switch -c my-experiment    # নতুন branch তৈরি
git checkout -b my-experiment  # same, old syntax

# Option 3: Detached state-এ থেকে commit করুন, তারপর branch
git add .
git commit -m "save my work"
git switch -c saved-experiment
```

**কখন intentionally Detached HEAD ব্যবহার করবেন:**
```bash
# পুরোনো code দেখতে (read-only)
git checkout v1.0.0
# ... code পড়লেন ...
git checkout main  # ফিরে এলেন

# Bug reproduction করতে (পুরোনো version test)
git checkout 3a7f8b2
# ... test করলেন ...
git checkout main

# Bisect-এ (automatically হয়)
git bisect start
```

**Interview Q&A:**
```
প্রশ্ন: "Detached HEAD state কী? কীভাবে হয় এবং কীভাবে বের হবেন?"

উত্তর: "Detached HEAD মানে HEAD কোনো branch-এ নয়, সরাসরি
একটি commit-এ আছে। git checkout [hash] বা git checkout [tag] করলে হয়।

এই state-এ commit করলে সেগুলো কোনো branch-এ নেই — branch-এ ফিরে
গেলে হারিয়ে যায়। তাই Detached HEAD-এ কাজ করতে হলে আগে
'git switch -c new-branch-name' দিয়ে branch তৈরি করুন।

দ্রুত বের হতে: git checkout main।"
```

---

<a id="p3-reset"></a>
**Topic 2: git reset — Soft, Mixed, Hard**

**সংজ্ঞা:**
`git reset` HEAD-কে নির্দিষ্ট commit-এ নিয়ে যায় এবং তার পরের commits "undo" করে। তিনটি mode আছে যা বিভিন্ন level-এ কাজ করে।

**তিনটি area আবার মনে করুন:**
```
Working Directory  ←→  Staging Area  ←→  Repository (commits)
```

**তিন mode-এর পার্থক্য:**

| Mode | Repository | Staging Area | Working Directory |
|------|-----------|--------------|------------------|
| `--soft` | পরিবর্তিত (HEAD সরে) | অপরিবর্তিত | অপরিবর্তিত |
| `--mixed` (default) | পরিবর্তিত | Reset (unstaged) | অপরিবর্তিত |
| `--hard` | পরিবর্তিত | Reset | Reset (changes মুছে যায়) |

**Visual explanation:**
```
Commits: A ─── B ─── C ─── D  ← HEAD (main)

git reset --soft HEAD~2  (HEAD → B)
  → Repository: HEAD = B
  → Staging: C ও D-এর changes staged আছে
  → Working Dir: C ও D-এর changes আছে
  (commits undo, কিন্তু changes staged রয়েছে)

git reset --mixed HEAD~2  (HEAD → B)  [DEFAULT]
  → Repository: HEAD = B
  → Staging: empty (C, D-এর changes unstaged)
  → Working Dir: C ও D-এর changes আছে
  (commits undo, staging cleared, working dir অক্ষত)

git reset --hard HEAD~2  (HEAD → B)
  → Repository: HEAD = B
  → Staging: empty
  → Working Dir: C ও D-এর changes পুরোপুরি মুছে গেছে ⚠️
  (সব undo — DESTRUCTIVE!)
```

**Practical examples:**
```bash
# ──────────────────────────────────────────────
# --soft: Commit undo কিন্তু changes staged রাখুন
# Use case: Commit message ভুল, বা কয়েকটি commit একসাথে করতে
# ──────────────────────────────────────────────
git reset --soft HEAD~1
# শেষ commit undo হলো, কিন্তু changes staging-এ আছে
git commit -m "feat: better commit message"  # re-commit

# ──────────────────────────────────────────────
# --mixed (default): Commit undo, changes working dir-এ
# Use case: কিছু changes বাদ দিয়ে re-commit করতে
# ──────────────────────────────────────────────
git reset HEAD~1       # default = --mixed
git reset --mixed HEAD~1
# Changes এখন working directory-তে, unstaged
# আপনি বেছে git add করতে পারবেন

# ──────────────────────────────────────────────
# --hard: সব undo — DANGEROUS! ⚠️
# Use case: পুরোপুরি কোনো feature বাদ দিতে
# ──────────────────────────────────────────────
git reset --hard HEAD~1
# শেষ commit এবং তার সব changes মুছে গেছে!
# Reflog দিয়ে recover করা যেতে পারে (কিছু সময়ের জন্য)

# Specific commit-এ reset
git reset --hard 3a7f8b2

# Staging area clear করুন (file মুছে না)
git reset HEAD              # HEAD = --mixed (সব unstage)
git reset HEAD filename.py  # specific file unstage
git restore --staged .      # modern equivalent
```

**Common use cases:**
```bash
# Last commit-এর message fix করতে (push না করলে)
git reset --soft HEAD~1
git commit -m "correct message"

# Accidental commit undo (3টি undo, changes রাখুন)
git reset --mixed HEAD~3

# Feature branch পুরো reset করতে (দরকার নেই আর)
git reset --hard origin/main
# অথবা:
git checkout main
git branch -D bad-feature

# Staged changes unstage করুন
git reset HEAD .
```

**⚠️ Warning:**
```
git reset --hard দেওয়ার আগে নিশ্চিত হন —
এটি working directory-র changes মুছে দেয়।
Push করা commits-এ reset করা অন্যদের problem করে।
```

---

<a id="p3-revert"></a>
**Topic 3: git revert**

**সংজ্ঞা:**
`git revert` একটি commit-এর changes undo করে একটি **নতুন commit** তৈরি করে। History মুছে না — বরং reverse করে। এটি **safe** কারণ public history পরিবর্তন করে না।

```bash
# Specific commit revert করুন
git revert 3a7f8b2

# Last commit revert
git revert HEAD

# Editor ছাড়াই (default message ব্যবহার করে)
git revert HEAD --no-edit

# Multiple commits revert
git revert HEAD~2..HEAD   # last 3 commits revert

# Revert করুন কিন্তু commit করবেন না (staging-এ রাখুন)
git revert --no-commit HEAD
git revert -n HEAD        # short form
# তারপর: git revert --continue
# বা abort: git revert --abort

# Merge commit revert (parent specify করতে হয়)
git revert -m 1 HEAD  # -m 1 = main parent
```

**Revert কী করে:**
```
Before:
A ─── B ─── C ─── D  ← HEAD
              ↑
         (bad commit — add wrong feature)

After git revert C:
A ─── B ─── C ─── D ─── C'  ← HEAD
                        ↑
               (new commit that undoes C)
```

**Output:**
```
$ git revert HEAD
[main abc1234] Revert "feat: add wrong feature"
 1 file changed, 50 deletions(-)
```

---

<a id="p3-reset-vs-revert"></a>
**Topic 4: Reset vs Revert — কখন কোনটা**

এটি interview-এর সবচেয়ে common question।

| | git reset | git revert |
|--|-----------|-----------|
| History | পরিবর্তিত করে | Preserve করে |
| New commit? | না | হ্যাঁ |
| Public commits-এ safe? | ❌ না | ✅ হ্যাঁ |
| Destructive? | হতে পারে (`--hard`) | না |
| Collaboration-এ | সমস্যা করে | Safe |

**Decision tree:**
```
Commit undo করতে হবে?
│
├── শুধু local branch? (push করা হয়নি)
│   └── git reset --soft/mixed/hard
│       └── ─ message fix → --soft
│           ─ re-stage → --mixed
│           ─ পুরো delete → --hard
│
└── Already pushed? / Shared branch?
    └── git revert [commit-hash]
        └── নতুন "undo" commit তৈরি হবে, history safe
```

**Real-world scenarios:**
```bash
# Scenario 1: Local commit-এ typo fix
git reset --soft HEAD~1
git commit -m "correct message"

# Scenario 2: Production-এ bad commit undo
git revert abc1234    # safe, নতুন commit
git push origin main

# Scenario 3: Feature branch-এর last 3 commits বাদ দিন (local only)
git reset --hard HEAD~3

# Scenario 4: Staging area clear করুন
git reset HEAD .      # --mixed = unstage all
```

**Interview answer:**
```
প্রশ্ন: "git reset এবং git revert-এর পার্থক্য কী?"

উত্তর: "মূল পার্থক্য হলো history।

git reset HEAD-কে পুরোনো commit-এ নিয়ে যায় — পরের commits
যেন হয়নি এমন। History পরিবর্তন হয়। এটি local, unpushed commits-এ
safe — কিন্তু pushed commits-এ করলে team-এর সবার repo-তে conflict হয়।

git revert একটি নতুন commit তৈরি করে যা target commit-এর changes
reverse করে। History অক্ষত থাকে। Production বা shared branch-এ
এটাই safe option।

Rule: Already pushed = git revert, only local = git reset।"
```

---

<a id="p3-reflog"></a>
**Topic 5: git reflog — Time Machine**

**সংজ্ঞা:**
`git reflog` (reference log) হলো HEAD এবং branch-এর সব movements-এর log — একটি local time machine। এমনকি deleted commits, hard reset-এর পরেও reflog দিয়ে recover করা যায়।

```bash
git reflog
# অথবা:
git reflog show HEAD
```

**Output:**
```
$ git reflog
3a7f8b2 HEAD@{0}: commit: feat: add payment
b2c4d5e HEAD@{1}: reset: moving to HEAD~1
abc1234 HEAD@{2}: commit: feat: add broken feature
def5678 HEAD@{3}: checkout: moving from feature to main
111aaaa HEAD@{4}: commit: fix: resolve bug
```

**Reflog দিয়ে recovery:**

```bash
# ──────────────────────────────────────────────
# Scenario 1: git reset --hard করে commit হারিয়েছেন
# ──────────────────────────────────────────────
git reset --hard HEAD~3   # oops! 3 commits মুছে গেছে

# Reflog দেখুন
git reflog
# abc1234 HEAD@{1}: commit: feat: important feature  ← এটাই দরকার

# Recover করুন
git reset --hard abc1234
# অথবা: নতুন branch-এ
git checkout -b recovered-branch abc1234

# ──────────────────────────────────────────────
# Scenario 2: Branch delete করে ফেলেছেন
# ──────────────────────────────────────────────
git branch -D important-feature   # oops!

# Branch-এর last commit খুঁজুন
git reflog | grep important-feature
# abc1234 HEAD@{5}: checkout: moving from important-feature to main

# Branch recreate করুন
git checkout -b important-feature abc1234

# ──────────────────────────────────────────────
# Scenario 3: Wrong merge করেছেন
# ──────────────────────────────────────────────
git merge wrong-branch   # oops!

git reflog
# abc1234 HEAD@{1}: merge wrong-branch: ...
# def5678 HEAD@{2}: commit: last good commit  ← এটাতে ফিরুন

git reset --hard def5678
```

**Reflog-এর limitations:**
```
⚠️ Reflog শুধু LOCAL — remote repository-তে নেই
⚠️ Default 90 দিন পরে expire হয়
   (git config gc.reflogExpire)
⚠️ git gc (garbage collection) পরে হারিয়ে যেতে পারে
```

**Interview Q&A:**
```
প্রশ্ন: "git reset --hard করে important commits মুছে ফেলেছেন। কীভাবে recover করবেন?"

উত্তর: "git reflog দিয়ে! Reflog সব HEAD movements track করে —
এমনকি hard reset-এর পরেও। git reflog দিয়ে হারানো commit-এর hash
খুঁজে git reset --hard [hash] অথবা git checkout -b recovery [hash]
দিয়ে recover করা যায়।

তবে এটি local — remote-এ নেই, এবং ৯০ দিন পরে expire হয়।"
```

---

<a id="p3-squash"></a>
**Topic 6: Squash Commits ও Interactive Rebase**

**Squash কেন দরকার:**
Feature development-এ অনেক ছোট ছোট commits হয় — "fix typo", "wip", "try again"। Main branch-এ merge করার আগে এগুলো একটি meaningful commit-এ পরিণত করা ভালো practice।

```
Before squash (messy history):
feat: add login form
fix: typo in login
wip: working on validation
fix: validation almost done
fix: actually fixed now

After squash (clean history):
feat: add login with form validation
```

**Interactive Rebase দিয়ে squash:**
```bash
# শেষ 5টি commit interactive rebase
git rebase -i HEAD~5

# Editor খুলবে:
pick a1b2c3d feat: add login form
pick b2c4d5e fix: typo in login
pick c3d4e5f wip: working on validation
pick d4e5f6a fix: validation almost done
pick e5f6a7b fix: actually fixed now

# পরিবর্তন করুন (প্রথমটি pick, বাকিগুলো squash):
pick a1b2c3d feat: add login form
squash b2c4d5e fix: typo in login
squash c3d4e5f wip: working on validation
squash d4e5f6a fix: validation almost done
squash e5f6a7b fix: actually fixed now

# Save করুন (Vim: :wq, VS Code: close tab)
# তারপর combined message editor আসবে:
# সব message দেখাবে, সুন্দর একটি message রাখুন:
feat: add login form with input validation
```

**Interactive Rebase সব commands:**
```bash
# শেষ 4টি commit
git rebase -i HEAD~4

# Available commands:
# p, pick   = use commit (unchanged)
# r, reword = use commit, but edit the commit message
# e, edit   = use commit, but stop for amending
# s, squash = use commit, meld into previous commit
# f, fixup  = like squash, but discard this commit's log message
# x, exec   = run command (e.g., run tests)
# b, break  = stop here (continue with 'git rebase --continue')
# d, drop   = remove commit
# l, label  = label current HEAD with a name
# t, reset  = reset HEAD to a label
# m, merge  = create a merge commit
```

**Practical example — reword:**
```bash
git rebase -i HEAD~3

# Change "pick" to "reword" for first commit:
reword a1b2c3d feat: add lgin form  ← typo!
pick b2c4d5e fix: validation
pick c3d4e5f feat: add logout

# Save → Editor opens with the commit message to fix:
feat: add login form   ← corrected
# Save → done
```

**Practical example — drop:**
```bash
git rebase -i HEAD~4

# Remove a commit entirely:
pick a1b2c3d feat: add login
drop b2c4d5e debug: console.log passwords  ← security! remove this
pick c3d4e5f fix: validation
pick d4e5f6a feat: add logout
```

**Conflict during interactive rebase:**
```bash
# Conflict হলে:
git status          # conflict দেখুন
# ... resolve করুন ...
git add resolved-file.py
git rebase --continue

# বাদ দিতে:
git rebase --abort
```

---

<a id="p3-hooks"></a>
**Topic 7: Git Hooks**

**সংজ্ঞা:**
Git Hooks হলো scripts যা নির্দিষ্ট Git events-এ automatically run হয় — commit করার আগে, push করার আগে, merge-এর পরে ইত্যাদি।

**Hook location:**
```bash
ls .git/hooks/
# applypatch-msg.sample    pre-push.sample
# commit-msg.sample        pre-rebase.sample
# post-commit.sample       pre-receive.sample
# pre-applypatch.sample    prepare-commit-msg.sample
# pre-commit.sample        update.sample
```

`.sample` extension সরালে active হয়।

**সবচেয়ে বেশি ব্যবহৃত hooks:**

| Hook | কখন চলে | Use case |
|------|---------|---------|
| `pre-commit` | commit-এর আগে | Lint, tests, secrets check |
| `commit-msg` | commit message check | Message format validation |
| `pre-push` | push-এর আগে | Full test suite run |
| `post-commit` | commit-এর পরে | Notification |
| `pre-rebase` | rebase-এর আগে | Safety check |

**pre-commit hook example:**
```bash
#!/bin/sh
# .git/hooks/pre-commit

echo "Running pre-commit checks..."

# Python lint check
if command -v flake8 &>/dev/null; then
    flake8 src/
    if [ $? -ne 0 ]; then
        echo "❌ Flake8 errors found. Commit aborted."
        exit 1
    fi
fi

# Check for debug statements
if git diff --cached | grep -E "(console\.log|debugger|pdb\.set_trace|breakpoint\(\))" > /dev/null; then
    echo "❌ Debug statements found! Remove them before committing."
    exit 1
fi

# Check for TODO/FIXME (warning only)
if git diff --cached | grep -E "(TODO|FIXME)" > /dev/null; then
    echo "⚠️  Warning: TODO/FIXME found in staged changes"
fi

echo "✅ Pre-commit checks passed!"
exit 0
```

**commit-msg hook — Conventional Commits enforce:**
```bash
#!/bin/sh
# .git/hooks/commit-msg

commit_msg=$(cat "$1")
pattern="^(feat|fix|docs|style|refactor|test|chore|perf|ci)(\(.+\))?: .{1,72}"

if ! echo "$commit_msg" | grep -qE "$pattern"; then
    echo "❌ Invalid commit message format!"
    echo "   Required: type(scope): description"
    echo "   Example:  feat(auth): add login functionality"
    echo "   Types: feat|fix|docs|style|refactor|test|chore|perf|ci"
    exit 1
fi

echo "✅ Commit message valid!"
exit 0
```

**Hook activate করুন:**
```bash
# .git/hooks/pre-commit তৈরি করুন
nano .git/hooks/pre-commit
# উপরের script paste করুন

# Executable করুন
chmod +x .git/hooks/pre-commit
```

**Husky — team-wide hooks (Node.js projects):**
```bash
npm install -D husky
npx husky init

# .husky/pre-commit:
npm test
npm run lint

# .husky/commit-msg:
npx commitlint --edit $1
```

**Hook skip করা (জরুরি অবস্থায়):**
```bash
git commit --no-verify -m "emergency: hotfix"
git push --no-verify
# ⚠️ সাবধানে ব্যবহার করুন
```

**Interview Q&A:**
```
প্রশ্ন: "Git Hooks কী? একটি practical example দিন।"

উত্তর: "Git Hooks হলো scripts যা নির্দিষ্ট Git events-এ automatically
execute হয়। যেমন pre-commit hook commit করার আগে চলে।

আমি pre-commit hook-এ lint check রাখি — code standard maintain করতে।
commit-msg hook-এ Conventional Commits format validate করি।
pre-push hook-এ test suite run করি — broken code push না হওয়ার জন্য।

Husky npm package দিয়ে team-এর সবার জন্য same hooks share করা যায়।"
```

---

<a id="p3-submodules"></a>
**Topic 8: Git Submodules**

**সংজ্ঞা:**
Git Submodule দিয়ে একটি Git repository-র ভেতরে আরেকটি Git repository embed করা যায়। External library বা shared component include করতে ব্যবহার হয়।

```bash
# Submodule add করুন
git submodule add https://github.com/org/shared-lib.git libs/shared

# .gitmodules file তৈরি হয়:
[submodule "libs/shared"]
    path = libs/shared
    url = https://github.com/org/shared-lib.git

# Submodule সহ clone করুন
git clone --recursive https://github.com/user/project.git

# বা clone-এর পরে initialize:
git submodule update --init --recursive

# Submodule update করুন
git submodule update --remote
git submodule update --remote --merge  # merge with local

# সব submodule-এ command run করুন
git submodule foreach 'git pull origin main'

# Submodule status দেখুন
git submodule status
```

**Interview tip:**
```
প্রশ্ন: "Git Submodule কী? কখন ব্যবহার করবেন?"

উত্তর: "Submodule দিয়ে parent repository-র ভেতরে child repository
include করা যায়। Monorepo setup বা external shared library pin করতে।

তবে submodule বেশ complex — developer-দের সবসময় --recursive
flag মনে রাখতে হয়। Modern alternative হলো Git Subtree বা npm/pip
dependency management। ছোট team-এ submodule avoid করাই ভালো।"
```

---

<a id="p3-internals"></a>
**Topic 9: Git Internals — Object Model**

**Git-এর 4টি object type:**

**1. Blob — File content:**
```bash
# Blob তৈরি দেখুন
echo "Hello, Git!" | git hash-object --stdin
# d8e8fca2dc0f896fd7cb4cb0031ba249  (SHA-1 hash)

# File-এর blob hash
git hash-object src/app.py

# Blob content দেখুন
git cat-file -p d8e8fca2dc0f896fd7cb4cb0031ba249
# Hello, Git!
```

**2. Tree — Directory structure:**
```bash
# Current commit-এর tree
git cat-file -p HEAD^{tree}
# 100644 blob a8c3... README.md
# 040000 tree b2d4... src
# 100644 blob c5e6... requirements.txt

# src/ directory-এর tree
git cat-file -p b2d4...
# 100644 blob d7f8... app.py
# 100644 blob e9a0... models.py
```

**3. Commit — Snapshot + metadata:**
```bash
git cat-file -p HEAD
# tree 7b8c...          ← root tree hash
# parent 3a7f...        ← previous commit
# author Alice <a@b.com> 1715500000 +0600
# committer Alice <a@b.com> 1715500000 +0600
#
# feat: add login functionality
```

**4. Tag — Named commit reference:**
```bash
git cat-file -p v1.0.0
# object 3a7f8b2...
# type commit
# tag v1.0.0
# tagger Alice <a@b.com>
# Initial stable release
```

**Object storage:**
```bash
# Objects কোথায় থাকে:
.git/objects/
├── 3a/
│   └── 7f8b2c...  (first 2 chars = folder, rest = filename)
├── b2/
│   └── c4d5e6...
└── pack/          (compressed objects)
```

**Interview tip:**
```
প্রশ্ন: "Git-এর ভেতরে files কীভাবে store হয়?"

উত্তর: "Git content-addressable storage ব্যবহার করে। প্রতিটি file-এর
content SHA-1 hash করা হয়, সেই hash-ই key। একই content-এর file
একাধিক commit-এ থাকলে Git duplicate store করে না — same blob।

4 ধরনের object: Blob (file content), Tree (directory), Commit
(snapshot + metadata), Tag (named pointer)। এই কারণে Git অনেক
efficient এবং fast।"
```

---

<a id="p3-sha"></a>
**Topic 10: SHA Hashing Basics**

**SHA-1 কী:**
Git প্রতিটি object-এর জন্য SHA-1 (Secure Hash Algorithm 1) ব্যবহার করে — একটি 40-character hexadecimal string।

```bash
# SHA-1 demo
echo "Hello" | sha1sum
# f7ff9e8b7bb2e09b70935a5d785e0cc5d9d0abf0  -

# Git object-এর hash দেখুন
git rev-parse HEAD
# 3a7f8b2c1d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a

git rev-parse HEAD~1
# b2c4d5e6f7a8b9c0d1e2f3a4b5c6d7e8f9a0b1c2

# Short hash (first 7 chars, usually unique enough)
git rev-parse --short HEAD
# 3a7f8b2
```

**SHA-1 → SHA-256 transition:**
```
Git 2.29+ এ SHA-256 support আসছে (SHA-1 এর collision vulnerability)।
তবে এখনো বেশিরভাগ project SHA-1 ব্যবহার করে।
```

**Why SHA:**
```
1. Content-addressing: same content → same hash (always)
2. Integrity: hash mismatch → corruption detected
3. Deduplication: duplicate files → shared object
4. Distributed: দুই developer-এর same commit → same hash
```

---

<a id="p3-recovery"></a>
**Topic 11: Recovery Strategies**

**সাধারণ disaster scenarios এবং recovery:**

**Scenario 1: Accidental `git reset --hard`**
```bash
git reset --hard HEAD~5   # oops! 5 commits মুছে গেছে

# Recovery:
git reflog
# abc1234 HEAD@{1}: commit: the commit I need

git reset --hard abc1234  # ফিরে এলাম!
```

**Scenario 2: Branch accidentally deleted**
```bash
git branch -D feature/important  # oops!

# Recovery:
git reflog | grep "feature/important"
# def5678 HEAD@{3}: checkout: moving from feature/important to main

git checkout -b feature/important def5678
```

**Scenario 3: Wrong file committed (sensitive data)**
```bash
# .env file commit হয়ে গেছে
git log --oneline
# abc1234 add .env accidentally

# Option 1: Revert (push করা হলে)
git revert abc1234
git push

# Option 2: Reset (push না হলে)
git reset --mixed HEAD~1
echo ".env" >> .gitignore
git add .gitignore
git commit -m "chore: add .env to gitignore"

# Option 3: Completely remove from history (nuclear option)
git filter-branch --index-filter \
  'git rm --cached --ignore-unmatch .env' HEAD
# অথবা modern: git filter-repo --path .env --invert-paths
```

**Scenario 4: Merge করে ফেলেছেন, undo করতে হবে**
```bash
# Merge commit hash খুঁজুন
git log --oneline
# abc1234 Merge branch 'wrong-feature'  ← এটা undo করতে হবে

# Revert merge commit (-m 1 = main parent)
git revert -m 1 abc1234
git push

# অথবা reset (shared branch নয় যদি)
git reset --hard HEAD~1
```

**Scenario 5: Push করা হয়নি এমন স্থানে সব কিছু undo করতে**
```bash
git reset --hard origin/main
# Local changes এবং local commits সব বাদ, remote-এর সাথে sync
```

**Emergency checklist:**
```
কিছু ভুল হলে:
1. panic করবেন না
2. git status দিন
3. git log --oneline দিন
4. git reflog দিন
5. Force push করবেন না (--force) — team-এ সবার আগে জানান
6. Stack Overflow / colleague-কে জিজ্ঞেস করুন
```

---

**PART 3 Quick Revision Table**

| Concept/Command | মূল কথা |
|----------------|---------|
| Detached HEAD | HEAD সরাসরি commit-এ, কোনো branch-এ নয় |
| Detached HEAD fix | `git switch -c new-branch` |
| `reset --soft` | Commit undo, changes staged রাখে |
| `reset --mixed` | Commit undo, changes unstaged রাখে (default) |
| `reset --hard` | Commit undo + সব changes মুছে দেয় ⚠️ |
| `git revert` | নতুন commit দিয়ে undo — history safe |
| Reset vs Revert | Local unpushed → reset, Pushed/shared → revert |
| `git reflog` | সব HEAD movements-এর local log — time machine |
| Squash commits | Interactive rebase + `squash` command |
| `git rebase -i` | Commit history rewrite: squash/reword/drop |
| Git Hooks | Event-based scripts: pre-commit, commit-msg |
| Submodule | Repo-এর ভেতরে অন্য repo |
| Blob | File content object |
| Tree | Directory structure object |
| Commit object | Snapshot + author + parent reference |
| SHA-1 | 40-char content-based unique identifier |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part4"></a>
## PART 4: GitHub Fundamentals

> GitHub হলো Git repository hosting-এর সবচেয়ে popular platform। এই PART-এ GitHub-এর মূল concepts — repository, fork, pull request, code review, issues থেকে শুরু করে professional profile optimization পর্যন্ত সব কিছু বিস্তারিত আলোচনা করা হয়েছে।

| # | বিষয় |
|---|-------|
| 1 | [GitHub কী? Git vs GitHub](#p4-github-intro) |
| 2 | [Repository তৈরি ও Setup](#p4-create-repo) |
| 3 | [Public vs Private Repository](#p4-public-private) |
| 4 | [Fork — কী এবং কেন](#p4-fork) |
| 5 | [Pull Request (PR) — সম্পূর্ণ গাইড](#p4-pr) |
| 6 | [Code Review Process](#p4-code-review) |
| 7 | [Issues ও Project Management](#p4-issues) |
| 8 | [GitHub Discussions](#p4-discussions) |
| 9 | [README.md ও Markdown](#p4-readme) |
| 10 | [Releases ও Tags](#p4-releases) |
| 11 | [GitHub Profile Optimization](#p4-profile) |

---

<a id="p4-github-intro"></a>
**Topic 1: GitHub কী? Git vs GitHub**

**GitHub কী:**
GitHub হলো Microsoft-এর মালিকানাধীন একটি **web-based platform** যা Git repository hosting, collaboration tools, CI/CD, project management এবং social coding features প্রদান করে।

**Git vs GitHub — এই প্রশ্ন প্রায় সব interview-এ আসে:**

| | Git | GitHub |
|--|-----|--------|
| কী? | Version control software | Web hosting platform |
| কোথায় চলে? | Local computer-এ | Cloud (github.com) |
| Internet দরকার? | না (local কাজে) | হ্যাঁ |
| তৈরি করেছে | Linus Torvalds (2005) | Tom Preston-Werner (2008) |
| মালিকানা | Open-source | Microsoft (2018 থেকে) |
| বিকল্প | Mercurial, SVN | GitLab, Bitbucket, Gitea |
| মূল কাজ | Version control | Collaboration + hosting |

**GitHub ছাড়া কি Git ব্যবহার করা যায়?**
হ্যাঁ! GitHub শুধু একটি hosting platform। Git একেবারে locally ব্যবহার করা যায়, বা self-hosted GitLab-এও।

**GitHub-এর প্রধান features:**
```
✅ Repository hosting (public + private)
✅ Pull Request + Code Review
✅ Issues (bug tracking, feature requests)
✅ GitHub Actions (CI/CD)
✅ GitHub Pages (static site hosting)
✅ GitHub Packages (package registry)
✅ GitHub Copilot (AI coding assistant)
✅ GitHub Projects (kanban board)
✅ GitHub Discussions (forum-style Q&A)
✅ Dependency graph + Dependabot
✅ GitHub Security Advisories
```

**Interview answer:**
```
প্রশ্ন: "Git এবং GitHub-এর পার্থক্য কী?"

উত্তর: "Git হলো একটি software tool — locally install করে
version control করা যায়। Internet ছাড়াও কাজ করে।

GitHub হলো একটি web platform যেখানে Git repositories
host করা হয়। Collaboration-এর জন্য: Pull Request, Code Review,
Issues, Actions সব এখানে আছে।

Analogy: Git হলো camera, GitHub হলো Instagram — camera দিয়ে
ছবি তোলা যায় Instagram ছাড়াও, কিন্তু share করতে platform দরকার।"
```

---

<a id="p4-create-repo"></a>
**Topic 2: Repository তৈরি ও Setup**

**GitHub-এ নতুন repository:**
```
github.com → "+" → "New repository"
→ Repository name: my-project
→ Description: Brief description
→ Public / Private
→ Initialize with README ✅
→ Add .gitignore: Python / Node / etc.
→ License: MIT / Apache / etc.
→ "Create repository"
```

**Existing local project → GitHub:**
```bash
# Local project আছে, GitHub-এ push করতে হবে

# Step 1: GitHub-এ new repo তৈরি করুন (README ছাড়া)

# Step 2: Local project-এ remote add করুন
cd my-project
git init   # আগে init না করলে
git add .
git commit -m "feat: initial project setup"

# Step 3: Remote connect করুন
git remote add origin https://github.com/username/my-project.git
# অথবা SSH:
git remote add origin git@github.com:username/my-project.git

# Step 4: Push করুন
git push -u origin main
# -u = --set-upstream, পরে শুধু 'git push' কাজ করবে
```

**GitHub থেকে existing project:**
```bash
# HTTPS clone
git clone https://github.com/username/project.git

# SSH clone (key setup থাকলে)
git clone git@github.com:username/project.git

# Specific branch
git clone -b develop https://github.com/username/project.git

# Specific folder নামে
git clone https://github.com/username/project.git my-folder
```

**SSH Key Setup (once per machine):**
```bash
# SSH key তৈরি করুন
ssh-keygen -t ed25519 -C "your@email.com"
# Enter file: ~/.ssh/id_ed25519
# Passphrase: (optional)

# Public key copy করুন
cat ~/.ssh/id_ed25519.pub

# GitHub → Settings → SSH and GPG keys → New SSH key
# Paste করুন

# Test করুন
ssh -T git@github.com
# Hi username! You've successfully authenticated.
```

**Remote management:**
```bash
# Remote দেখুন
git remote -v
# origin  git@github.com:username/project.git (fetch)
# origin  git@github.com:username/project.git (push)

# Remote add করুন
git remote add upstream https://github.com/original/project.git

# Remote rename করুন
git remote rename origin github

# Remote URL পরিবর্তন করুন (HTTPS → SSH)
git remote set-url origin git@github.com:username/project.git

# Remote সরান
git remote remove upstream
```

---

<a id="p4-public-private"></a>
**Topic 3: Public vs Private Repository**

| | Public | Private |
|--|--------|---------|
| কে দেখতে পারে | সবাই (internet-এ) | শুধু আপনি + collaborators |
| কে clone করতে পারে | সবাই | শুধু authorized users |
| GitHub Pages | ✅ Free | ✅ (paid plan-এ) |
| Open-source | ✅ | ❌ |
| Free? | ✅ Unlimited | ✅ Unlimited (GitHub Free) |
| Code search | GitHub-এ সবাই | শুধু authorized |

**কখন কোনটা:**
```
Public:
✅ Open-source project
✅ Portfolio projects (recruiters দেখবে)
✅ Study notes, documentation
✅ GitHub Pages websites

Private:
✅ Client project (NDA)
✅ Company/startup product
✅ WIP project (ready না হলে)
✅ Sensitive configuration
```

**Interview tip:**
```
প্রশ্ন: "আপনার GitHub-এ কী আছে? Public না Private?"

উত্তর: "আমার portfolio projects public রাখি — recruiters এবং
interviewer-রা দেখতে পারেন। Client বা company project private।
Public project-গুলোতে README সুন্দর করে লিখেছি — live demo link,
tech stack, setup guide সহ।"
```

---

<a id="p4-fork"></a>
**Topic 4: Fork — কী এবং কেন**

**সংজ্ঞা:**
Fork মানে অন্য কারো repository-র একটি complete copy নিজের GitHub account-এ তৈরি করা। Open-source contribution-এর মূল প্রক্রিয়া।

**Fork vs Clone:**

| | Fork | Clone |
|--|------|-------|
| কোথায় হয় | GitHub server-এ | Local machine-এ |
| কার account? | আপনার GitHub-এ copy | শুধু local |
| Original repo-তে push? | না (PR দিয়ে) | Permission থাকলে |
| Use case | Open-source contribution | Local development |

**Fork workflow — Open-source contribution:**
```
Original Repo (org/project)
         ↓
        Fork
         ↓
Your Repo (you/project) ← GitHub-এ আপনার copy
         ↓
        Clone
         ↓
Local Machine → feature branch → commit
         ↓
        Push to your fork
         ↓
   Pull Request: you/project → org/project
         ↓
    Code Review by maintainers
         ↓
        Merge ✅
```

**Fork করার পরে:**
```bash
# Step 1: GitHub-এ "Fork" button click

# Step 2: আপনার fork clone করুন
git clone https://github.com/YOUR-USERNAME/project.git
cd project

# Step 3: Original repo-কে "upstream" হিসেবে add করুন
git remote add upstream https://github.com/ORIGINAL/project.git

# Verify:
git remote -v
# origin    https://github.com/YOUR-USERNAME/project.git (fetch/push)
# upstream  https://github.com/ORIGINAL/project.git (fetch)

# Step 4: Feature branch-এ কাজ করুন
git checkout -b fix/typo-in-readme

# Step 5: Changes করুন, commit করুন
git add README.md
git commit -m "docs: fix typo in installation guide"

# Step 6: আপনার fork-এ push করুন
git push origin fix/typo-in-readme

# Step 7: GitHub-এ Pull Request তৈরি করুন
# base: ORIGINAL/project:main ← head: YOUR/project:fix/typo-in-readme
```

**Fork sync (upstream থেকে latest নিন):**
```bash
# Upstream-এর latest changes নিন
git fetch upstream

# main branch sync করুন
git checkout main
git merge upstream/main
# অথবা: git rebase upstream/main

# আপনার fork update করুন
git push origin main
```

**Interview Q&A:**
```
প্রশ্ন: "Fork এবং Clone-এর পার্থক্য কী?"

উত্তর: "Clone হলো repository-র একটি local copy — আপনার machine-এ।
Fork হলো GitHub server-এ repository-র copy — আপনার account-এ।

Fork ব্যবহার হয় open-source contribution-এ: original repo-তে
direct push access নেই, তাই fork করে নিজের copy-তে কাজ করি,
তারপর Pull Request দিয়ে original-এ merge request করি।"
```

---

<a id="p4-pr"></a>
**Topic 5: Pull Request (PR) — সম্পূর্ণ গাইড**

**সংজ্ঞা:**
Pull Request (PR) হলো GitHub-এর একটি feature যা দিয়ে আপনি অন্যদের জানান "আমি এই changes merge করতে চাই"। এটি code review, discussion এবং automated checks-এর একটি সম্পূর্ণ platform।

**PR তৈরির ধাপ:**
```
1. Feature branch-এ কাজ সম্পন্ন
2. GitHub-এ push: git push origin feature/login
3. GitHub.com-এ repository খুলুন
4. "Compare & pull request" notification দেখবেন
5. অথবা: "Pull requests" tab → "New pull request"
6. Base: main ← Compare: feature/login
7. Title, description লিখুন
8. Reviewers, labels, milestone assign করুন
9. "Create pull request"
```

**PR description template (professional):**
```markdown
## 📝 কী পরিবর্তন করেছি
- User authentication system implement করেছি
- JWT-based login/logout endpoint তৈরি করেছি  
- Password bcrypt দিয়ে hash করা হচ্ছে
- Refresh token mechanism add করেছি

## 🎯 কেন এই পরিবর্তন (Motivation)
Issue #45-এর অংশ হিসেবে — v2.0 release-এর জন্য user auth দরকার।
আগে session-based ছিল, stateless JWT-তে migrate করছি।

## 🧪 Testing
- Unit tests: `pytest tests/auth/`
- Manual testing:
  1. `POST /api/auth/login` — body: `{"email": "test@test.com", "password": "pass123"}`
  2. Response-এ JWT token পাবেন
  3. `Authorization: Bearer <token>` header দিয়ে protected routes access করুন

## 📸 Screenshots (UI change হলে)
[Before] [After]

## ✅ Checklist
- [x] Unit tests written and passing
- [x] No hardcoded secrets or credentials
- [x] API documentation updated
- [x] Migration files included
- [x] No console.log / debug statements
- [ ] Performance tested (large dataset)

## 🔗 Related
Closes #45
Depends on #42 (merged)
```

**PR labels:**
```
Type labels: feature, bug, documentation, refactor
Status labels: ready-for-review, work-in-progress, blocked
Priority: critical, high, medium, low
```

**Draft PR — কাজ চলাকালীন:**
```bash
# Push করুন
git push origin feature/wip-feature

# GitHub-এ: "Create pull request" → "Create draft pull request"
# Draft PR-এ: code দেখানো যায়, early feedback নেওয়া যায়
# কিন্তু reviewers merge করতে পারবে না
# Ready হলে: "Ready for review" button
```

**PR merge strategies:**

| Strategy | কী করে | কখন |
|----------|--------|------|
| Merge commit | Merge commit তৈরি করে (--no-ff) | Full history দেখতে |
| Squash and merge | সব commits → একটি | Clean history চাইলে |
| Rebase and merge | Linear history, no merge commit | Linear preference |

**Interview Q&A:**
```
প্রশ্ন: "Pull Request কী? Code review-এ কীভাবে অংশগ্রহণ করেন?"

উত্তর: "Pull Request হলো team-এর কাছে 'এই changes main-এ নিন'
এর formal request। শুধু code change নয় — discussion, review,
automated CI checks সব এক জায়গায়।

আমি PR-এ বিস্তারিত description লিখি: কী করেছি, কেন করেছি,
কীভাবে test করবেন। Review comment-এ constructive feedback দিই
— personal না করে code নিয়ে কথা বলি। Change request-এ
promptly respond করি।"
```

---

<a id="p4-code-review"></a>
**Topic 6: Code Review Process**

**Code review কেন গুরুত্বপূর্ণ:**
```
✅ Bug detection — reviewer নতুন চোখে দেখে
✅ Knowledge sharing — team সবাই code জানে
✅ Code quality — standards maintain হয়
✅ Mentoring — junior developer শেখে
✅ Collective ownership — "আমার code" না, "আমাদের code"
```

**Review করার সময় কী দেখবেন:**
```
Functionality:
✅ Requested changes সঠিকভাবে implement হয়েছে?
✅ Edge cases handle হয়েছে?
✅ Error handling আছে?

Code Quality:
✅ Code readable ও maintainable?
✅ DRY principle (Don't Repeat Yourself)?
✅ Functions/methods ছোট ও focused?
✅ Naming convention followed?

Security:
✅ SQL injection, XSS vulnerability নেই?
✅ Sensitive data hardcoded নেই?
✅ Authentication/authorization সঠিক?

Performance:
✅ N+1 query problem নেই?
✅ Unnecessary loops নেই?

Testing:
✅ Tests আছে? Sufficient coverage?
✅ Tests meaningful?
```

**GitHub review features:**
```bash
# Review types:
# ✅ Approve — merge করা যাবে
# 💬 Comment — general feedback, merge block করে না
# ❌ Request changes — এগুলো fix না করে merge করা যাবে না

# Line comment:
# File-এর specific line-এ click → comment add

# Suggestion (inline fix):
# ```suggestion
# corrected code here
# ```
# Author "Accept suggestion" click করলে automatically apply হয়
```

**Code review etiquette:**
```
Reviewer হিসেবে:
✅ "This function is too long" → "Could we break this into smaller functions?"
✅ Explain WHY, not just WHAT to change
✅ Distinguish blocking vs non-blocking comments
✅ Praise good work too: "Nice approach here! 👍"
✅ Response করুন 24 hours-এর মধ্যে
✅ "Nit:" prefix minor suggestions-এ

Author হিসেবে:
✅ প্রতিটি comment-এ response দিন (agree/disagree/question)
✅ Defensive হবেন না — code improve হচ্ছে
✅ Change করলে "Done" বা "Fixed in abc1234" লিখুন
✅ Complex changes-এ PR-এ explanation add করুন
```

**Branch protection rules (Team settings):**
```
GitHub → Repository → Settings → Branches → Branch protection rules

✅ Require pull request before merging
✅ Require approvals: 1 (minimum)
✅ Dismiss stale pull request approvals
✅ Require status checks to pass (CI)
✅ Require branches to be up to date
✅ Do not allow force pushes
✅ Do not allow deletions
```

---

<a id="p4-issues"></a>
**Topic 7: Issues ও Project Management**

**GitHub Issues:**
Issues হলো bug reports, feature requests, এবং tasks track করার জায়গা।

```markdown
# Issue title: [BUG] Login page crashes on mobile Chrome

## Bug Description
Login page-এ "Submit" button click করলে mobile Chrome-এ crash হয়।

## Steps to Reproduce
1. Mobile Chrome-এ example.com/login খুলুন
2. Email ও password দিন
3. "Login" button click করুন
4. Page crash হয় / blank screen

## Expected Behavior
Dashboard-এ redirect হওয়া উচিত।

## Actual Behavior
Page crash হয়, console-এ "TypeError: Cannot read property 'token' of undefined"

## Environment
- OS: Android 13
- Browser: Chrome 124
- App version: 2.1.0

## Screenshots
[screenshot attached]

## Possible Fix
auth.js line 145-এ null check নেই।
```

**Issue labels:**
```
bug           → red      — কিছু কাজ করছে না
enhancement   → blue     — নতুন feature
documentation → green    — docs দরকার
help wanted   → teal     — community contribution চাই
good first issue → purple — beginner-friendly
question      → pink     — প্রশ্ন
wontfix       → white    — এটা fix করা হবে না
duplicate     → grey     — আগে থেকেই আছে
```

**Issue linking:**
```bash
# PR description বা commit message-এ issue reference:
"Closes #45"     → PR merge হলে issue automatically close
"Fixes #45"      → same
"Resolves #45"   → same

"Related to #45" → close করে না, শুধু link
"See #45"        → same

# Commit message-এ:
git commit -m "fix(auth): resolve null token on mobile (closes #45)"
```

**GitHub Projects (Kanban):**
```
GitHub → Projects → New project → Board

Columns:
📋 Backlog → 🏃 In Progress → 👀 In Review → ✅ Done

Cards = Issues or Pull Requests
Automation: PR merged → Issue → Done column
```

**Milestones:**
```
GitHub → Issues → Milestones → New milestone
Name: v2.0.0 Release
Due date: June 30, 2026
Description: All features for major release

Issues assign to milestone → progress tracking
```

---

<a id="p4-discussions"></a>
**Topic 8: GitHub Discussions**

**Discussions কী:**
Issues-এর মতো কিন্তু open-ended conversation-এর জন্য। Q&A, announcements, ideas, polls — formal issue নয় এমন topics-এর জন্য।

```
Categories:
📣 Announcements — maintainer announcements
💬 General — general discussion
💡 Ideas — feature suggestions
🙏 Q&A — help questions
🙌 Show and tell — community showcase
```

**Issues vs Discussions:**

| | Issues | Discussions |
|--|--------|------------|
| উদ্দেশ্য | Bug, task, feature | Open conversation |
| Close হয়? | হ্যাঁ | না (usually) |
| Assignee | হ্যাঁ | না |
| Linked to PR? | হ্যাঁ | সীমিত |
| Best for | Actionable items | Ideas, Q&A |

---

<a id="p4-readme"></a>
**Topic 9: README.md ও Markdown**

**README কেন গুরুত্বপূর্ণ:**
README হলো project-এর "মুখ" — GitHub-এ repository খুললে প্রথমে দেখা যায়। Recruiter ও contributor উভয়ের জন্য গুরুত্বপূর্ণ।

**Professional README structure:**
```markdown
# Project Name

Short description (1-2 lines)

![Build Status](badge-url)
![License](badge-url)
![Version](badge-url)

## 🎯 Overview
কী করে এই project, কেন তৈরি করলেন।

## ✨ Features
- Feature 1
- Feature 2
- Feature 3

## 🛠️ Tech Stack
- React 18, TypeScript
- FastAPI, PostgreSQL
- Docker, GitHub Actions

## 🚀 Quick Start

### Prerequisites
- Python 3.11+
- Node.js 20+
- Docker

### Installation
```bash
# Clone করুন
git clone https://github.com/username/project.git
cd project

# Dependencies install করুন
pip install -r requirements.txt

# Environment variables
cp .env.example .env
# .env file edit করুন

# Run করুন
python manage.py runserver
```

## 📸 Screenshots
[Add screenshots or GIFs]

## 📚 API Documentation
API docs: [https://api.example.com/docs](link)

## 🤝 Contributing
1. Fork করুন
2. Feature branch তৈরি করুন (`git checkout -b feature/amazing`)
3. Commit করুন (`git commit -m 'feat: add amazing feature'`)
4. Push করুন (`git push origin feature/amazing`)
5. Pull Request দিন

## 📄 License
MIT License — [LICENSE](LICENSE) দেখুন।

## 📧 Contact
Your Name — your@email.com
GitHub: [@username](https://github.com/username)
```

**Markdown essentials:**
```markdown
# H1 Heading
## H2 Heading
### H3 Heading

**bold text**
*italic text*
~~strikethrough~~
`inline code`

```python
# code block
def hello():
    print("Hello!")
```

- unordered list
- item 2
  - nested item

1. ordered list
2. item 2

[Link text](https://url.com)
![Image alt](image.png)

| Column 1 | Column 2 |
|----------|----------|
| Cell 1   | Cell 2   |

> Blockquote

---  (horizontal rule)

- [x] checked task
- [ ] unchecked task
```

**Shields.io badges:**
```markdown
![GitHub Stars](https://img.shields.io/github/stars/user/repo?style=flat)
![License](https://img.shields.io/badge/license-MIT-blue)
![Python Version](https://img.shields.io/badge/python-3.11+-green)
![Build](https://github.com/user/repo/actions/workflows/test.yml/badge.svg)
```

---

<a id="p4-releases"></a>
**Topic 10: Releases ও Tags**

**GitHub Release তৈরি:**
```
GitHub → Repository → Releases → "Draft a new release"
→ Tag: v1.0.0 (নতুন তৈরি করুন বা existing)
→ Target: main
→ Release title: v1.0.0 — First Stable Release
→ Description (auto-generate from commits)
→ Attach binaries (optional)
→ Pre-release checkbox (beta versions)
→ "Publish release"
```

**Release notes format:**
```markdown
## 🎉 What's New in v2.0.0

### ✨ New Features
- User authentication with JWT (#45)
- Payment gateway integration (#67)
- Dark mode support (#89)

### 🐛 Bug Fixes
- Fixed login crash on mobile Chrome (#52)
- Resolved cart quantity bug (#61)

### 💥 Breaking Changes
- API endpoint `/api/user` renamed to `/api/users`
- Response format changed: `userId` → `user_id`

### 📦 Dependencies Updated
- React 17 → 18
- FastAPI 0.95 → 0.110

### 🙏 Contributors
Thanks to @alice, @bob, @charlie for contributions!

**Full Changelog**: https://github.com/user/repo/compare/v1.0.0...v2.0.0
```

**GitHub CLI দিয়ে release:**
```bash
# GitHub CLI install
sudo apt install gh    # Linux
brew install gh        # macOS

# Login
gh auth login

# Release তৈরি
gh release create v1.0.0 \
  --title "v1.0.0 — First Release" \
  --notes "Initial stable release" \
  --target main

# Pre-release
gh release create v2.0.0-beta.1 --prerelease

# Assets attach করুন
gh release create v1.0.0 ./dist/app-linux.tar.gz ./dist/app-windows.zip
```

---

<a id="p4-profile"></a>
**Topic 11: GitHub Profile Optimization**

**Profile README তৈরি:**
```bash
# username/username নামে special repository তৈরি করুন
# (username = আপনার GitHub username)
# README.md automatically profile-এ দেখাবে
```

**Professional profile README:**
```markdown
<div align="center">

# Hi, I'm Alice 👋

**Full-Stack Developer | Open Source Enthusiast | Bangladesh 🇧🇩**

[![LinkedIn](badge)](linkedin-url)
[![Portfolio](badge)](portfolio-url)
[![Email](badge)](mailto:alice@email.com)

</div>

---

### 🔧 Tech Stack

**Frontend:** React · TypeScript · Next.js · Tailwind CSS  
**Backend:** Python · FastAPI · Node.js · Express  
**Database:** PostgreSQL · MongoDB · Redis  
**DevOps:** Docker · GitHub Actions · Nginx · Vercel  

---

### 📊 GitHub Stats

<div align="center">
  
![Stats](https://github-readme-stats.vercel.app/api?username=alice&show_icons=true&theme=dark)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=alice&layout=compact&theme=dark)

</div>

---

### 🚀 Featured Projects

| Project | Description | Tech |
|---------|-------------|------|
| [E-Commerce App](link) | Full-stack shopping platform | React, FastAPI, PostgreSQL |
| [Chat Application](link) | Real-time chat with WebSocket | Node.js, Socket.io, Redis |
| [CS Handbook](link) | Interview prep in Bangla | Markdown |

---

### 📈 Contribution Graph

![Snake animation](https://github.com/alice/alice/blob/output/github-contribution-grid-snake.svg)

---

*📫 Reach me: alice@email.com | Open to remote opportunities*
```

**Profile optimization checklist:**
```
Profile basics:
✅ Professional photo (না হলে avatar)
✅ Full name (real name, professional)
✅ Bio: role, tech, location
✅ Location: Dhaka, Bangladesh
✅ Company/University
✅ Website/Portfolio link
✅ Email (public করুন)
✅ Twitter/LinkedIn link

Repositories:
✅ 6 repositories pin করুন (best projects)
✅ প্রতিটি repository-তে description add করুন
✅ Topics/tags add করুন (react, python, etc.)
✅ README সুন্দর করুন (screenshot, demo link)
✅ License add করুন

Activity:
✅ Green contribution graph (daily habit)
✅ Open source contributions (even small)
✅ Stars দিন interesting repos-এ
✅ Follow relevant developers

What recruiters see:
✅ Contribution frequency
✅ Code quality (repo + commits)
✅ Project variety
✅ Collaboration (PRs to other repos)
✅ README quality
```

**Contribution graph tips:**
```bash
# Daily small contribution habits:
- Everyday কিছু না কিছু commit করুন
- Documentation improve করুন
- Issue comment করুন
- Open source project-এ small PR দিন

# Private repos-ও count করে settings-এ enable করলে:
# Settings → Contributions → Private contributions
```

---

**PART 4 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| GitHub কী? | Git repository hosting + collaboration platform |
| Git vs GitHub | Software vs Platform (camera vs Instagram) |
| Fork | GitHub-এ অন্যের repo-র আপনার account-এ copy |
| Fork vs Clone | GitHub server copy vs local machine copy |
| Pull Request | "আমার changes merge করুন" — review + discussion |
| `git remote add` | Remote repository connect করা |
| `git push -u origin main` | First push + upstream set |
| Upstream remote | Fork-এ original repo-র reference |
| Code review: Approve | Merge করা যাবে |
| Code review: Request changes | Fix না করে merge করা যাবে না |
| Issue close via PR | "Closes #45" PR description-এ |
| Branch protection | Force push, direct push block করা |
| SSH key কেন? | Password ছাড়া secure authentication |
| Profile README | username/username special repo |
| SemVer | v{MAJOR}.{MINOR}.{PATCH} |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 5 — GitHub Collaboration & Team Workflow

---

<a id="part5"></a>
## PART 5: GitHub Collaboration & Team Workflow

> Solo project-এ Git ব্যবহার এক রকম, কিন্তু team-এ কাজ করতে হলে সঠিক workflow জানা আবশ্যক। এই PART-এ branching strategies, team collaboration tools, CODEOWNERS, PR templates এবং organization management বিস্তারিত আলোচনা করা হয়েছে।

| # | বিষয় |
|---|-------|
| 1 | [Branching Strategies — GitHub Flow, Git Flow, Trunk-Based](#p5-branch-strategy) |
| 2 | [GitHub Flow — Step by Step](#p5-github-flow) |
| 3 | [Git Flow — Complete Guide](#p5-git-flow) |
| 4 | [Trunk-Based Development](#p5-trunk-based) |
| 5 | [Branch Naming Conventions](#p5-branch-naming) |
| 6 | [CODEOWNERS — Automatic Review Assignment](#p5-codeowners) |
| 7 | [PR Templates ও Issue Templates](#p5-templates) |
| 8 | [.github Folder Structure](#p5-github-folder) |
| 9 | [Collaborators vs Teams vs Organizations](#p5-org) |
| 10 | [Forking vs Branching for Contribution](#p5-fork-vs-branch) |
| 11 | [Conflict Prevention Strategies](#p5-conflict-prevention) |
| 12 | [GitHub Notifications ও Watching](#p5-notifications) |

---

<a id="p5-branch-strategy"></a>
**Topic 1: Branching Strategies — GitHub Flow, Git Flow, Trunk-Based**

Team-এ কোন branching strategy ব্যবহার করবেন সেটা project-এর size, release cycle এবং team size-এর উপর নির্ভর করে।

**তিনটি প্রধান strategy:**

| | GitHub Flow | Git Flow | Trunk-Based |
|--|------------|---------|------------|
| Branch count | কম (main + feature) | অনেক (main, develop, release, hotfix) | সর্বনিম্ন (শুধু main) |
| Release cycle | Continuous | Scheduled | Continuous |
| Complexity | Simple | Complex | Simple |
| Best for | Web apps, SaaS | Versioned software | Large teams, CI/CD |
| Teams | Small-medium | Medium-large | Large (Google, Facebook) |

---

<a id="p5-github-flow"></a>
**Topic 2: GitHub Flow — Step by Step**

**GitHub Flow কী:**
GitHub নিজেই যে workflow ব্যবহার করে — সহজ এবং continuous deployment-এর জন্য ideal।

**Core rule:** `main` branch সবসময় deployable থাকবে।

```
GitHub Flow:
                    ┌─ feature/login ──────────────┐
main ──────────────────────────────── merge ─────── main (deploy)
                    └─ fix/payment-bug ────────────┘

Steps:
1. main থেকে feature branch তৈরি
2. Feature branch-এ commits
3. PR open করুন (যত তাড়াতাড়ি সম্ভব, draft হলেও)
4. Review ও automated tests
5. Deploy to staging (preview environment)
6. Approve হলে merge to main
7. Main থেকে production deploy
```

**Practical commands:**
```bash
# Step 1: Always start from updated main
git checkout main
git pull origin main

# Step 2: New feature branch
git checkout -b feature/user-profile

# Step 3: কাজ করুন, commit করুন
git add .
git commit -m "feat(profile): add user avatar upload"
git commit -m "feat(profile): add bio field"

# Step 4: Push and create PR
git push origin feature/user-profile
# GitHub-এ PR তৈরি করুন

# Step 5: Review comments address করুন
git add .
git commit -m "fix: address review comments"
git push origin feature/user-profile

# Step 6: After merge, cleanup
git checkout main
git pull origin main
git branch -d feature/user-profile  # local cleanup
```

**GitHub Flow-এর সুবিধা:**
```
✅ Simple — নতুন developer সহজে বোঝে
✅ Always deployable main
✅ Fast feedback loop
✅ Less merge conflicts (branches ছোট রাখলে)
✅ Continuous delivery-এর জন্য perfect
```

---

<a id="p5-git-flow"></a>
**Topic 3: Git Flow — Complete Guide**

**Git Flow কী:**
Vincent Driessen-এর branching model — scheduled release (যেমন software package, mobile app) project-এর জন্য।

**Branches:**
```
main       — production code, tagged releases
develop    — integration branch, next release
feature/*  — নতুন features
release/*  — release preparation (version bump, docs)
hotfix/*   — production bug fix
```

**Git Flow diagram:**
```
main     ────────────────── v1.0 ──────────────────── v1.1
              ↑ merge                      ↑ merge
develop  ──── ──────────────────────────── ─────────────
              ↑            ↑ merge
feature  ─────             │
              └── feat/login ──┘
                                    ┌─ release/1.1 ─┐
develop                ────────────── ──────────────── ─────
                                    ↑ merge             ↑
main                                                  v1.1

hotfix   ─── hotfix/payment ──── merge to main + develop
```

**Git Flow commands:**
```bash
# git-flow tool install করুন (optional, কিন্তু helpful)
sudo apt install git-flow      # Linux
brew install git-flow          # macOS

# Initialize
git flow init
# Default branch names accept করুন (Enter key)

# Feature শুরু
git flow feature start user-auth
# = git checkout -b feature/user-auth develop

# Feature শেষ (develop-এ merge হয়)
git flow feature finish user-auth
# = git checkout develop && git merge feature/user-auth && git branch -d feature/user-auth

# Release শুরু
git flow release start 1.2.0
# = git checkout -b release/1.2.0 develop

# Release শেষ
git flow release finish 1.2.0
# = develop + main-এ merge, tag v1.2.0, branch delete

# Hotfix শুরু (main থেকে)
git flow hotfix start payment-crash
# = git checkout -b hotfix/payment-crash main

# Hotfix শেষ
git flow hotfix finish payment-crash
# = main + develop-এ merge, tag, branch delete
```

**Manual Git Flow (tool ছাড়া):**
```bash
# Feature branch
git checkout develop
git pull origin develop
git checkout -b feature/payment-gateway

# ... কাজ করুন ...

git checkout develop
git merge --no-ff feature/payment-gateway  # --no-ff = merge commit রাখুন
git push origin develop
git branch -d feature/payment-gateway

# Release
git checkout develop
git checkout -b release/2.0.0
# version bump করুন (package.json, setup.py, etc.)
git commit -m "chore: bump version to 2.0.0"

# Testing done, release করুন
git checkout main
git merge --no-ff release/2.0.0
git tag -a v2.0.0 -m "Release version 2.0.0"
git push origin main --tags

git checkout develop
git merge --no-ff release/2.0.0
git push origin develop
git branch -d release/2.0.0
```

---

<a id="p5-trunk-based"></a>
**Topic 4: Trunk-Based Development**

**Trunk-Based Development কী:**
সবাই `main` (trunk) branch-এ সরাসরি কাজ করে বা খুব short-lived branches (1-2 দিন) ব্যবহার করে। Google, Facebook এই model ব্যবহার করে।

```
Trunk-Based:
main ─── commit ─── commit ─── commit ─── commit ─── (always green)
              ↑           ↑
        Small, frequent commits   No long-lived feature branches
```

**Key practices:**
```bash
# Feature Flags দিয়ে incomplete features hide করুন
# code push হয়, কিন্তু UI/API disabled থাকে

# config.py
FEATURES = {
    "new_payment": False,   # disable in production
    "dark_mode": True,
}

# code-এ:
if FEATURES["new_payment"]:
    # new code
else:
    # old code

# CI/CD mandatory — প্রতি commit-এ automated test
# যদি test fail করে → immediately fix করতে হবে
```

**কখন কোন strategy:**
```
GitHub Flow → Web app, SaaS, small-medium team
Git Flow    → Mobile app, npm package, scheduled release
Trunk-Based → Large team, microservices, very mature CI/CD
```

**Interview Q&A:**
```
প্রশ্ন: "আপনার previous project-এ কোন Git workflow ব্যবহার হতো?"

উত্তর: "আমরা GitHub Flow ব্যবহার করতাম। main branch সবসময়
deployable রাখতাম। Feature branch তৈরি করতাম, PR দিতাম, review
হলে merge করতাম। Simple এবং continuous deployment-এর জন্য
এটাই best ছিল আমাদের ছোট team-এর জন্য।

Git Flow জানি — versioned software বা mobile app-এ যেখানে
scheduled release cycle আছে, সেখানে Git Flow ভালো।"
```

---

<a id="p5-branch-naming"></a>
**Topic 5: Branch Naming Conventions**

**Standard convention:**
```bash
# Format: type/short-description
# type: feature, fix, hotfix, release, chore, docs, refactor, test

feature/user-authentication
feature/payment-gateway-integration
fix/login-crash-mobile
fix/cart-quantity-overflow
hotfix/production-data-loss
release/2.0.0
chore/update-dependencies
docs/api-documentation
refactor/auth-module
test/payment-unit-tests

# Issue number include করলে traceability ভালো হয়
feature/45-user-authentication
fix/52-login-crash-mobile
```

**Branch naming rules:**
```bash
# ✅ Good
feature/user-profile-upload
fix/42-payment-timeout
docs/setup-guide

# ❌ Bad
mywork              # no type, vague
Feature/Login Page  # spaces not allowed
john/test-stuff     # person name (not meaningful)
temp                # too vague
```

**Git-এ branch pattern enforce (pre-receive hook):**
```bash
#!/bin/sh
# Server-side hook: pre-receive
while read oldrev newrev refname; do
    branch=$(echo "$refname" | sed 's/refs\/heads\///')
    if ! echo "$branch" | grep -qE "^(main|develop|feature|fix|hotfix|release|chore|docs|refactor|test)\/.+"; then
        echo "❌ Branch name '$branch' doesn't follow convention!"
        echo "   Use: type/description (e.g., feature/user-auth)"
        exit 1
    fi
done
exit 0
```

---

<a id="p5-codeowners"></a>
**Topic 6: CODEOWNERS — Automatic Review Assignment**

**CODEOWNERS কী:**
একটি special file যা define করে কোন file বা directory-র জন্য কোন team member-কে automatically review request পাঠানো হবে।

**File location:**
```
.github/CODEOWNERS    ← recommended
CODEOWNERS            ← root-এও কাজ করে
docs/CODEOWNERS       ← docs folder-এর জন্য
```

**CODEOWNERS syntax:**
```bash
# .github/CODEOWNERS

# Default owners (সব file)
*                           @lead-developer

# Backend code
src/api/**                  @backend-team
src/api/auth/**             @security-team @backend-team

# Frontend code
src/frontend/**             @frontend-team
src/frontend/components/**  @alice @bob

# Database migrations
migrations/**               @dba-team @backend-team

# CI/CD configuration
.github/**                  @devops-team
Dockerfile                  @devops-team
docker-compose.yml          @devops-team

# Documentation
docs/**                     @tech-writer
*.md                        @tech-writer

# Package files (dependency changes require approval)
package.json                @lead-developer
requirements.txt            @lead-developer
Pipfile                     @lead-developer

# Security-sensitive files
src/auth/**                 @security-team
src/payment/**              @security-team @payment-team
```

**CODEOWNERS-এর সুবিধা:**
```
✅ Automatic reviewer assignment — manually tag করতে হয় না
✅ Domain experts সবসময় review করেন
✅ Security-sensitive code extra review পায়
✅ PR merge-এর আগে CODEOWNER approval required করা যায়
```

**Branch protection + CODEOWNERS:**
```
GitHub → Settings → Branches → Branch protection rules
→ ✅ Require review from Code Owners
```

---

<a id="p5-templates"></a>
**Topic 7: PR Templates ও Issue Templates**

**Pull Request Template:**
```markdown
<!-- .github/pull_request_template.md -->
## কী পরিবর্তন করেছি
<!-- সংক্ষেপে describe করুন -->

## কেন এই পরিবর্তন
<!-- Motivation, context -->

## Related Issue
Closes #<!-- issue number -->

## Testing করেছেন?
- [ ] Unit tests pass করছে
- [ ] Manual testing করেছি
- [ ] Edge cases check করেছি

## Screenshots (UI change হলে)
<!-- Before/After screenshots -->

## Checklist
- [ ] Code review guidelines follow করেছি
- [ ] No hardcoded secrets
- [ ] Documentation update করেছি (যদি দরকার)
- [ ] No console.log / debug statements
```

**Multiple PR templates (type-based):**
```bash
# .github/PULL_REQUEST_TEMPLATE/ folder
.github/
  PULL_REQUEST_TEMPLATE/
    feature.md      # ?template=feature
    bugfix.md       # ?template=bugfix
    hotfix.md       # ?template=hotfix
    documentation.md
```

**Issue Templates:**
```markdown
<!-- .github/ISSUE_TEMPLATE/bug_report.md -->
---
name: Bug Report
about: Report a bug to help us improve
title: '[BUG] '
labels: bug
assignees: ''
---

## Bug Description
<!-- কী সমস্যা হচ্ছে -->

## Steps to Reproduce
1. 
2. 
3. 

## Expected Behavior
<!-- কী হওয়া উচিত -->

## Actual Behavior
<!-- কী হচ্ছে -->

## Environment
- OS: 
- Browser/Version: 
- App Version: 

## Screenshots
<!-- যদি থাকে -->
```

```markdown
<!-- .github/ISSUE_TEMPLATE/feature_request.md -->
---
name: Feature Request
about: Suggest a new feature
title: '[FEAT] '
labels: enhancement
assignees: ''
---

## Feature Description
<!-- কী feature চান -->

## Problem it Solves
<!-- কোন problem solve করবে -->

## Proposed Solution
<!-- কীভাবে implement করা যেতে পারে -->

## Alternatives Considered
<!-- অন্য কোন approach ভেবেছেন? -->
```

---

<a id="p5-github-folder"></a>
**Topic 8: .github Folder Structure**

`.github` folder-এ GitHub-specific configuration files রাখা হয়।

```
.github/
├── CODEOWNERS                          # Auto reviewer assignment
├── FUNDING.yml                         # Sponsor button
├── SECURITY.md                         # Security policy
├── SUPPORT.md                          # Support info
│
├── ISSUE_TEMPLATE/                     # Issue templates
│   ├── bug_report.md
│   ├── feature_request.md
│   └── config.yml                      # Template chooser config
│
├── PULL_REQUEST_TEMPLATE/              # PR templates
│   ├── feature.md
│   └── bugfix.md
│   (or single file:)
├── pull_request_template.md
│
└── workflows/                          # GitHub Actions
    ├── ci.yml                          # Run tests on PR
    ├── deploy.yml                      # Deploy on merge to main
    ├── release.yml                     # Create release
    └── codeql.yml                      # Security scanning
```

**ISSUE_TEMPLATE/config.yml:**
```yaml
# .github/ISSUE_TEMPLATE/config.yml
blank_issues_enabled: false
contact_links:
  - name: 💬 GitHub Discussions
    url: https://github.com/user/repo/discussions
    about: General questions এখানে করুন
  - name: 📖 Documentation
    url: https://docs.example.com
    about: Docs দেখুন আগে
```

---

<a id="p5-org"></a>
**Topic 9: Collaborators vs Teams vs Organizations**

**তিনটির পার্থক্য:**

**Collaborators (Personal Repository):**
```
Personal repo → Settings → Collaborators
→ GitHub username add করুন
→ Permission: Read / Write / Admin

ব্যবহার: ছোট project, 1-5 জন
```

**Teams (Organization):**
```
Organization → Teams → New Team
→ Team name: backend-team
→ Members add করুন
→ Repository access: org/project → Maintain / Write

ব্যবহার: department বা squad-based access
```

**Organizations:**
```
github.com/organizations/new
→ Organization name: my-company
→ Billing plan
→ Members invite করুন

Organization benefits:
✅ Shared repository ownership
✅ Team-based permissions
✅ Audit logs
✅ SSO (Single Sign-On) support
✅ Centralized billing
```

**Permission levels:**

| Level | Read | Write | Triage | Maintain | Admin |
|-------|------|-------|--------|----------|-------|
| Code read | ✅ | ✅ | ✅ | ✅ | ✅ |
| Issues manage | | | ✅ | ✅ | ✅ |
| Push code | | ✅ | | ✅ | ✅ |
| Manage branches | | | | ✅ | ✅ |
| Settings change | | | | | ✅ |

**Interview tip:**
```
প্রশ্ন: "Team-এ GitHub access কীভাবে manage করবেন?"

উত্তর: "Company project-এ Organization তৈরি করব। Team structure
অনুযায়ী Teams তৈরি করব — backend-team, frontend-team, devops-team।
Least privilege principle follow করব — developer-দের Write,
lead-দের Maintain, শুধু 1-2 জনকে Admin।

CODEOWNERS দিয়ে ensure করব sensitive code-এ (auth, payment)
সঠিক team auto-assign হচ্ছে।"
```

---

<a id="p5-fork-vs-branch"></a>
**Topic 10: Forking vs Branching for Contribution**

**কখন Fork, কখন Branch:**

| | Branch | Fork |
|--|--------|------|
| Repository access আছে? | হ্যাঁ | না |
| Open-source project? | না | হ্যাঁ |
| Team member? | হ্যাঁ | না |
| External contributor? | না | হ্যাঁ |

**Internal team workflow (Branch):**
```bash
# Team member → সরাসরি repository-তে access আছে
git clone https://github.com/company/project.git
git checkout -b feature/new-feature
# কাজ করুন, push করুন
git push origin feature/new-feature
# PR দিন company/project-এ
```

**Open-source contribution (Fork):**
```bash
# External contributor → সরাসরি access নেই
# GitHub-এ Fork করুন
git clone https://github.com/YOUR-USER/project.git  # fork
git remote add upstream https://github.com/original/project.git
git checkout -b fix/typo
# কাজ করুন
git push origin fix/typo
# PR দিন: YOUR-USER/project → original/project
```

---

<a id="p5-conflict-prevention"></a>
**Topic 11: Conflict Prevention Strategies**

**Merge conflict কেন হয়:**
দুইজন developer একই file-এর একই line পরিবর্তন করলে Git বুঝতে পারে না কোনটা রাখবে।

**Prevention strategies:**

```bash
# ──────────────────────────────────────────────
# Strategy 1: Branch ছোট রাখুন
# ──────────────────────────────────────────────
# ❌ Bad: 2 সপ্তাহ ধরে বড় feature branch
# ✅ Good: 1-3 দিনের ছোট focused changes

# ──────────────────────────────────────────────
# Strategy 2: main থেকে নিয়মিত sync করুন
# ──────────────────────────────────────────────
git fetch origin
git rebase origin/main   # অথবা:
git merge origin/main

# Daily habit:
git checkout main && git pull && git checkout feature/my-feature && git rebase main

# ──────────────────────────────────────────────
# Strategy 3: Team communication
# ──────────────────────────────────────────────
# Same file-এ কে কাজ করছে জানুন
# GitHub Projects বা Slack-এ coordinate করুন

# ──────────────────────────────────────────────
# Strategy 4: Modular code structure
# ──────────────────────────────────────────────
# একটি file-এ সব না রেখে ছোট modules-এ ভাগ করুন
# src/auth/login.py, src/auth/logout.py
# → different developers different files-এ কাজ করতে পারবেন

# ──────────────────────────────────────────────
# Strategy 5: PR-এ up-to-date requirement
# ──────────────────────────────────────────────
# Branch protection-এ "Require branches to be up to date"
# merge করার আগে latest main-এ rebase করতে হবে
```

**Conflict হলে কী করবেন:**
```bash
git merge origin/main
# Auto-merging failed; fix conflicts and then commit

git status
# both modified: src/auth/user.py

# user.py-তে দেখুন:
<<<<<<< HEAD (আপনার changes)
def get_user(user_id: int):
    return db.query(User).filter(User.id == user_id).first()
=======
def get_user(user_id: int) -> Optional[User]:
    return db.session.get(User, user_id)
>>>>>>> origin/main (incoming)

# Resolve: সঠিকটা রাখুন, markers সরান
def get_user(user_id: int) -> Optional[User]:
    return db.query(User).filter(User.id == user_id).first()

git add src/auth/user.py
git commit -m "merge: resolve conflict in get_user"
```

**Visual merge tool:**
```bash
# VS Code-এ merge editor
git config --global merge.tool vscode
git config --global mergetool.vscode.cmd 'code --wait $MERGED'
git mergetool

# IntelliJ/PyCharm-এ build-in merge editor আছে
```

---

<a id="p5-notifications"></a>
**Topic 12: GitHub Notifications ও Watching**

```bash
# Repository Watching:
# GitHub → Repository → Watch → Options:
#   Participating and @mentions (recommended)
#   All Activity (noisy)
#   Ignore
#   Custom (Issues/PRs/Releases)

# Notification settings:
# github.com/settings/notifications
# Email/Web/Mobile (GitHub app)

# @mention করা:
# PR comment-এ: "@alice এটা দেখুন"
# Issue-এ: "@backend-team এই bug আপনাদের area"

# Team mention:
# @org/backend-team → পুরো team notification পাবে
```

---

**PART 5 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| GitHub Flow | main সবসময় deployable, feature branch → PR → merge |
| Git Flow | main + develop + feature + release + hotfix |
| Trunk-Based | সবাই main-এ, feature flags ব্যবহার |
| Branch naming | `type/description` (feature/fix/hotfix/chore) |
| CODEOWNERS | Auto reviewer assignment by file/directory |
| PR Template | `.github/pull_request_template.md` |
| Issue Template | `.github/ISSUE_TEMPLATE/*.md` |
| .github folder | CODEOWNERS, templates, workflows |
| Organization | Company-level GitHub account |
| Teams | Group-based repository permissions |
| Least privilege | যতটুকু দরকার ততটুকু permission |
| Conflict prevention | ছোট branch, নিয়মিত rebase, modular code |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part6"></a>
## PART 6: GitHub Actions — CI/CD Automation

> GitHub Actions হলো GitHub-এর built-in automation platform। Code push থেকে শুরু করে production deploy পর্যন্ত সব automated করা যায়। এই PART-এ CI/CD concepts, workflow syntax, practical examples এবং real-world automation বিস্তারিত আলোচনা করা হয়েছে।

| # | বিষয় |
|---|-------|
| 1 | [CI/CD কী এবং কেন দরকার](#p6-cicd) |
| 2 | [GitHub Actions — মূল Concepts](#p6-concepts) |
| 3 | [Workflow YAML Syntax](#p6-yaml) |
| 4 | [Triggers — কখন Workflow চলবে](#p6-triggers) |
| 5 | [Runners](#p6-runners) |
| 6 | [Environment Variables ও Secrets](#p6-secrets) |
| 7 | [Practical Example — Python CI](#p6-python-ci) |
| 8 | [Practical Example — Node.js CI](#p6-node-ci) |
| 9 | [Matrix Builds](#p6-matrix) |
| 10 | [Caching Dependencies](#p6-cache) |
| 11 | [Deploy to GitHub Pages](#p6-pages) |
| 12 | [Reusable Workflows ও Composite Actions](#p6-reusable) |

---

<a id="p6-cicd"></a>
**Topic 1: CI/CD কী এবং কেন দরকার**

**CI — Continuous Integration:**
প্রতিটি code change-এ automatically:
- Build করা
- Tests run করা
- Code quality check করা
- Security scan করা

**CD — Continuous Delivery / Deployment:**
- **Continuous Delivery:** Staging-এ automatically deploy, production-এ manual approval
- **Continuous Deployment:** Production-এ automatically deploy (approval ছাড়া)

**CI/CD ছাড়া সমস্যা:**
```
❌ "Works on my machine" — local-এ চলে, server-এ চলে না
❌ Integration-এ late bug discovery — days/weeks পরে
❌ Manual deployment — slow, error-prone
❌ Inconsistent environments
❌ Fear of deploying on Fridays
```

**CI/CD থাকলে:**
```
✅ প্রতি PR-এ automatic test — bug early catch
✅ Consistent build environment
✅ Fast feedback (5-10 min)
✅ Automated deployment — human error কম
✅ Deploy anytime, confidently
✅ Code quality gate — linting, security scan
```

**Interview Q&A:**
```
প্রশ্ন: "CI/CD কী? কেন important?"

উত্তর: "CI হলো প্রতিটি code change-এ automatically build ও test
চালানো — integration bug early catch করতে। CD হলো verified code
automatically staging বা production-এ deploy করা।

GitHub Actions দিয়ে করেছি: PR open হলে pytest run হয়, main-এ
merge হলে automatic deploy হয় Railway-তে। Manual step নেই,
human error নেই, সবসময় tested code deploy হয়।"
```

---

<a id="p6-concepts"></a>
**Topic 2: GitHub Actions — মূল Concepts**

**পাঁচটি core concepts:**

```
Workflow
  └── Event (trigger: push, PR, schedule)
        └── Job (parallel বা sequential)
              └── Step (sequential)
                    └── Action (reusable unit) / Run (shell command)
```

**Visual:**
```
Workflow: ci.yml
│
├── Event: push to main
│
└── Job: test
      ├── Step 1: Checkout code       (uses: actions/checkout@v4)
      ├── Step 2: Setup Python        (uses: actions/setup-python@v5)
      ├── Step 3: Install deps        (run: pip install -r requirements.txt)
      ├── Step 4: Run lint            (run: flake8 src/)
      └── Step 5: Run tests           (run: pytest tests/ -v)
```

**Terms:**

| Term | কী | Example |
|------|----|---------|
| Workflow | Automation pipeline | `.github/workflows/ci.yml` |
| Event | Trigger condition | `push`, `pull_request`, `schedule` |
| Job | Group of steps (একটি runner-এ চলে) | `test`, `build`, `deploy` |
| Step | Individual task | Run command বা use action |
| Action | Reusable step | `actions/checkout@v4` |
| Runner | Virtual machine যেখানে job চলে | `ubuntu-latest` |
| Artifact | Build output | compiled binary, test report |
| Secret | Encrypted variable | API key, password |

---

<a id="p6-yaml"></a>
**Topic 3: Workflow YAML Syntax**

**Complete workflow structure:**
```yaml
# .github/workflows/ci.yml

name: CI Pipeline                  # Workflow নাম (GitHub UI-তে দেখা যায়)

on:                                # Trigger(s)
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

env:                               # Global environment variables
  PYTHON_VERSION: "3.11"
  NODE_VERSION: "20"

jobs:                              # একটি বা একাধিক job
  
  test:                            # Job ID (unique within workflow)
    name: Run Tests                # Job display name
    runs-on: ubuntu-latest         # Runner
    
    steps:                         # Sequential steps
      
      - name: Checkout code        # Step display name
        uses: actions/checkout@v4  # Pre-built action ব্যবহার
      
      - name: Setup Python
        uses: actions/setup-python@v5
        with:                      # Action-এর inputs
          python-version: ${{ env.PYTHON_VERSION }}
      
      - name: Install dependencies
        run: |                     # Multi-line shell command
          python -m pip install --upgrade pip
          pip install -r requirements.txt
          pip install -r requirements-dev.txt
      
      - name: Run lint
        run: flake8 src/ tests/
      
      - name: Run tests
        run: pytest tests/ -v --tb=short
        env:                       # Step-level env vars
          DATABASE_URL: ${{ secrets.TEST_DATABASE_URL }}
      
      - name: Upload test results  # Artifact upload
        uses: actions/upload-artifact@v4
        if: always()               # Always run (even on failure)
        with:
          name: test-results
          path: reports/

  deploy:
    name: Deploy to Staging
    runs-on: ubuntu-latest
    needs: test                    # test job সফল হলেই চলবে
    if: github.ref == 'refs/heads/main'  # Only on main branch
    
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      
      - name: Deploy
        run: ./scripts/deploy.sh
        env:
          DEPLOY_KEY: ${{ secrets.DEPLOY_KEY }}
```

**Common YAML patterns:**
```yaml
# Conditional step
- name: Only on failure
  if: failure()
  run: echo "Something went wrong!"

- name: Only on main
  if: github.ref == 'refs/heads/main'
  run: ./deploy.sh

# Working directory
- name: Run in subdirectory
  working-directory: ./backend
  run: pytest tests/

# Timeout
- name: Long test
  timeout-minutes: 30
  run: pytest tests/integration/

# Continue on error
- name: Optional lint
  continue-on-error: true
  run: flake8 src/

# Multi-line run
- name: Setup and install
  run: |
    echo "Installing dependencies..."
    pip install -r requirements.txt
    echo "Done!"
```

---

<a id="p6-triggers"></a>
**Topic 4: Triggers — কখন Workflow চলবে**

```yaml
on:
  # ──────────────────────────────────────────
  # Code events
  # ──────────────────────────────────────────
  push:
    branches:
      - main
      - develop
      - 'release/**'       # wildcard
    tags:
      - 'v*'               # v1.0.0 এর মতো tag
    paths:
      - 'src/**'           # শুধু src/ পরিবর্তনে
      - '!docs/**'         # docs/ বাদে

  pull_request:
    branches: [main]
    types: [opened, synchronize, reopened]  # PR events
    paths-ignore:
      - '**.md'            # markdown changes ignore

  # ──────────────────────────────────────────
  # Scheduled (cron)
  # ──────────────────────────────────────────
  schedule:
    - cron: '0 2 * * *'   # প্রতিদিন রাত ২টায় (UTC)
    - cron: '0 9 * * 1'   # প্রতি সোমবার সকাল ৯টায়

  # ──────────────────────────────────────────
  # Manual trigger
  # ──────────────────────────────────────────
  workflow_dispatch:
    inputs:
      environment:
        description: 'Deploy to which environment?'
        required: true
        default: 'staging'
        type: choice
        options: [staging, production]
      debug:
        description: 'Enable debug mode'
        type: boolean
        default: false

  # ──────────────────────────────────────────
  # Other workflow calls this one
  # ──────────────────────────────────────────
  workflow_call:
    inputs:
      version:
        required: true
        type: string

  # ──────────────────────────────────────────
  # Release published
  # ──────────────────────────────────────────
  release:
    types: [published, created]
```

---

<a id="p6-runners"></a>
**Topic 5: Runners**

**GitHub-hosted runners:**
```yaml
runs-on: ubuntu-latest     # Ubuntu 24.04 (most common)
runs-on: ubuntu-22.04      # Specific version
runs-on: windows-latest    # Windows Server 2022
runs-on: macos-latest      # macOS 14 (Sonoma)
runs-on: macos-13          # Specific macOS version
```

**Self-hosted runners:**
```yaml
# Company server-এ নিজের runner চালানো
runs-on: self-hosted
runs-on: [self-hosted, linux, x64]
runs-on: [self-hosted, linux, gpu]  # GPU machine

# কেন self-hosted?
# ✅ Private network access (database, internal services)
# ✅ Faster (powerful hardware)
# ✅ Cost saving (large projects)
# ✅ Custom software pre-installed
```

**GitHub-hosted runner specs:**
```
ubuntu-latest:
  CPU: 4 cores
  RAM: 16 GB
  Storage: 14 GB
  Cost: Free (2000 min/month for free plan)
```

---

<a id="p6-secrets"></a>
**Topic 6: Environment Variables ও Secrets**

**Secrets (encrypted):**
```
GitHub → Repository → Settings → Secrets and variables → Actions
→ New repository secret
→ Name: DATABASE_URL
→ Value: postgresql://user:pass@host:5432/db
```

**Environment variables (plaintext):**
```
Settings → Secrets and variables → Variables tab
→ New repository variable
→ Name: APP_ENV
→ Value: staging
```

**Workflow-এ ব্যবহার:**
```yaml
env:
  # Plain variable (not secret)
  APP_ENV: production
  LOG_LEVEL: info

jobs:
  deploy:
    runs-on: ubuntu-latest
    
    env:
      # Job-level env
      DEPLOY_ENV: staging
    
    steps:
      - name: Use secrets
        run: |
          echo "Deploying to $APP_ENV"
          # Secrets print হয় না — *** দেখায়
          curl -H "Authorization: Bearer $API_KEY" https://api.example.com/deploy
        env:
          API_KEY: ${{ secrets.API_KEY }}              # Secret
          DATABASE_URL: ${{ secrets.DATABASE_URL }}    # Secret
          APP_VERSION: ${{ vars.APP_VERSION }}         # Variable (non-secret)
```

**Context variables:**
```yaml
# GitHub context
${{ github.sha }}          # Commit hash
${{ github.ref }}          # Branch/tag ref
${{ github.event_name }}   # Trigger event name
${{ github.actor }}        # Who triggered
${{ github.repository }}   # owner/repo
${{ github.run_number }}   # Workflow run number

# Runner context
${{ runner.os }}           # Linux/Windows/macOS
${{ runner.temp }}         # Temp directory

# Job context
${{ job.status }}          # success/failure/cancelled
```

**⚠️ Secrets security:**
```yaml
# ✅ Good
- name: Deploy
  env:
    API_KEY: ${{ secrets.API_KEY }}  # env দিয়ে pass করুন

# ❌ Bad — log-এ expose হতে পারে
- name: Deploy
  run: ./deploy.sh ${{ secrets.API_KEY }}  # command args-এ না দিন

# Secret কখনো echo করবেন না:
# run: echo ${{ secrets.API_KEY }}  # GitHub mask করে, তবু bad practice
```

---

<a id="p6-python-ci"></a>
**Topic 7: Practical Example — Python CI**

```yaml
# .github/workflows/python-ci.yml
name: Python CI

on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main]

jobs:
  test:
    name: Test (Python ${{ matrix.python-version }})
    runs-on: ubuntu-latest
    
    strategy:
      matrix:
        python-version: ["3.10", "3.11", "3.12"]
    
    services:
      postgres:
        image: postgres:16
        env:
          POSTGRES_USER: testuser
          POSTGRES_PASSWORD: testpass
          POSTGRES_DB: testdb
        ports:
          - 5432:5432
        options: >-
          --health-cmd pg_isready
          --health-interval 10s
          --health-timeout 5s
          --health-retries 5
    
    steps:
      - name: Checkout code
        uses: actions/checkout@v4
      
      - name: Set up Python ${{ matrix.python-version }}
        uses: actions/setup-python@v5
        with:
          python-version: ${{ matrix.python-version }}
          cache: pip                        # pip cache
      
      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt
          pip install -r requirements-dev.txt
      
      - name: Run linting (flake8)
        run: |
          flake8 src/ tests/ --max-line-length=120 \
            --exclude=migrations/
      
      - name: Run type check (mypy)
        run: mypy src/ --ignore-missing-imports
        continue-on-error: true
      
      - name: Run tests with coverage
        run: |
          pytest tests/ -v \
            --cov=src \
            --cov-report=xml \
            --cov-report=term-missing \
            --tb=short
        env:
          DATABASE_URL: postgresql://testuser:testpass@localhost:5432/testdb
          SECRET_KEY: test-secret-key-for-ci
          DEBUG: "False"
      
      - name: Upload coverage to Codecov
        uses: codecov/codecov-action@v4
        with:
          file: ./coverage.xml
          fail_ci_if_error: false
      
      - name: Upload test results
        uses: actions/upload-artifact@v4
        if: always()
        with:
          name: test-results-${{ matrix.python-version }}
          path: |
            reports/
            coverage.xml
```

---

<a id="p6-node-ci"></a>
**Topic 8: Practical Example — Node.js CI**

```yaml
# .github/workflows/node-ci.yml
name: Node.js CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  lint-and-test:
    name: Lint & Test
    runs-on: ubuntu-latest
    
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      
      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: "20"
          cache: npm                  # npm cache
      
      - name: Install dependencies
        run: npm ci                   # npm install-এর চেয়ে stricter
      
      - name: Run ESLint
        run: npm run lint
      
      - name: Type check (TypeScript)
        run: npm run type-check
      
      - name: Run tests
        run: npm test -- --coverage --watchAll=false
      
      - name: Build
        run: npm run build
      
      - name: Upload build artifacts
        uses: actions/upload-artifact@v4
        with:
          name: build
          path: dist/
          retention-days: 7

  deploy:
    name: Deploy to Vercel
    runs-on: ubuntu-latest
    needs: lint-and-test
    if: github.ref == 'refs/heads/main' && github.event_name == 'push'
    
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      
      - name: Deploy to Vercel
        uses: amondnet/vercel-action@v25
        with:
          vercel-token: ${{ secrets.VERCEL_TOKEN }}
          vercel-org-id: ${{ secrets.VERCEL_ORG_ID }}
          vercel-project-id: ${{ secrets.VERCEL_PROJECT_ID }}
          vercel-args: '--prod'
```

---

<a id="p6-matrix"></a>
**Topic 9: Matrix Builds**

**Matrix strategy কী:**
একটি job বিভিন্ন combinations-এ parallel-এ run করা।

```yaml
jobs:
  test:
    runs-on: ${{ matrix.os }}
    
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest, macos-latest]
        python-version: ["3.10", "3.11", "3.12"]
        # 3 × 3 = 9 parallel jobs!
      
      fail-fast: false    # একটি fail করলে বাকিগুলো বন্ধ না করতে
      max-parallel: 4     # একসাথে সর্বোচ্চ 4টি job
    
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: ${{ matrix.python-version }}
      - run: pytest tests/

  # ──────────────────────────────────────────────
  # Matrix include/exclude
  # ──────────────────────────────────────────────
  test-advanced:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        python-version: ["3.10", "3.11", "3.12"]
        experimental: [false]
        include:
          - python-version: "3.13"   # Extra combination add
            experimental: true
        exclude:
          - python-version: "3.10"   # Specific combination remove
            os: macos-latest
    
    continue-on-error: ${{ matrix.experimental }}
    steps:
      - run: pytest tests/
```

---

<a id="p6-cache"></a>
**Topic 10: Caching Dependencies**

**Cache কেন দরকার:**
প্রতি run-এ `pip install` বা `npm install` করা সময়সাপেক্ষ। Cache দিয়ে 60-80% time বাঁচানো যায়।

```yaml
# ──────────────────────────────────────────────
# Python pip cache
# ──────────────────────────────────────────────
- uses: actions/setup-python@v5
  with:
    python-version: "3.11"
    cache: pip                    # Built-in cache

# Manual cache (more control):
- name: Cache pip
  uses: actions/cache@v4
  with:
    path: ~/.cache/pip
    key: ${{ runner.os }}-pip-${{ hashFiles('**/requirements*.txt') }}
    restore-keys: |
      ${{ runner.os }}-pip-

# ──────────────────────────────────────────────
# Node.js npm cache
# ──────────────────────────────────────────────
- uses: actions/setup-node@v4
  with:
    node-version: "20"
    cache: npm                    # Built-in npm cache

# pnpm:
- uses: pnpm/action-setup@v3
  with:
    version: 9
- uses: actions/setup-node@v4
  with:
    node-version: "20"
    cache: pnpm

# ──────────────────────────────────────────────
# Docker layer cache
# ──────────────────────────────────────────────
- name: Set up Docker Buildx
  uses: docker/setup-buildx-action@v3

- name: Build and push
  uses: docker/build-push-action@v6
  with:
    cache-from: type=gha       # GitHub Actions cache
    cache-to: type=gha,mode=max
```

---

<a id="p6-pages"></a>
**Topic 11: Deploy to GitHub Pages**

```yaml
# .github/workflows/deploy-pages.yml
name: Deploy to GitHub Pages

on:
  push:
    branches: [main]
  workflow_dispatch:

# GitHub Pages permissions
permissions:
  contents: read
  pages: write
  id-token: write

# Prevent multiple concurrent deployments
concurrency:
  group: pages
  cancel-in-progress: false

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      
      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: "20"
          cache: npm
      
      - name: Install and build
        run: |
          npm ci
          npm run build           # dist/ বা build/ folder তৈরি হবে
      
      - name: Setup Pages
        uses: actions/configure-pages@v5
      
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: dist/             # build output folder
  
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

**GitHub Pages enable করুন:**
```
Repository → Settings → Pages
→ Source: GitHub Actions
→ Save
```

---

<a id="p6-reusable"></a>
**Topic 12: Reusable Workflows ও Composite Actions**

**Reusable Workflow — একটি workflow অন্য workflow-এ call করুন:**
```yaml
# .github/workflows/reusable-test.yml (reusable)
name: Reusable Test Workflow

on:
  workflow_call:                  # Called by other workflows
    inputs:
      python-version:
        required: true
        type: string
    secrets:
      DATABASE_URL:
        required: true

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: ${{ inputs.python-version }}
      - run: pytest tests/
        env:
          DATABASE_URL: ${{ secrets.DATABASE_URL }}
```

```yaml
# .github/workflows/ci.yml (caller)
name: CI

on:
  push:
    branches: [main]

jobs:
  call-test:
    uses: ./.github/workflows/reusable-test.yml    # Same repo
    with:
      python-version: "3.11"
    secrets:
      DATABASE_URL: ${{ secrets.DATABASE_URL }}
```

**Workflow status badge — README-এ:**
```markdown
![CI Status](https://github.com/username/repo/actions/workflows/ci.yml/badge.svg)

![Deploy](https://github.com/username/repo/actions/workflows/deploy.yml/badge.svg?branch=main)
```

**Popular marketplace actions:**
```yaml
# Code checkout
uses: actions/checkout@v4

# Language setup
uses: actions/setup-python@v5
uses: actions/setup-node@v4
uses: actions/setup-java@v4

# Cache
uses: actions/cache@v4

# Artifacts
uses: actions/upload-artifact@v4
uses: actions/download-artifact@v4

# Docker
uses: docker/login-action@v3
uses: docker/build-push-action@v6

# Security
uses: github/codeql-action/analyze@v3
uses: snyk/actions/python@master

# Deployment
uses: amondnet/vercel-action@v25
uses: appleboy/ssh-action@v1      # SSH deploy
uses: aws-actions/configure-aws-credentials@v4

# Notifications
uses: 8398a7/action-slack@v3
```

---

**PART 6 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| CI | প্রতি code change-এ auto build + test |
| CD | Auto deploy to staging/production |
| Workflow | `.github/workflows/*.yml` file |
| Event/Trigger | `push`, `pull_request`, `schedule`, `workflow_dispatch` |
| Job | Steps-এর group, একটি runner-এ চলে |
| Step | Individual task: `run` বা `uses` |
| Action | Reusable step (Marketplace থেকে বা custom) |
| Runner | `ubuntu-latest`, `windows-latest`, `macos-latest` |
| Secret | Encrypted variable — `${{ secrets.NAME }}` |
| Matrix | Same job multiple combinations-এ parallel run |
| Cache | Dependencies cache — speed up workflows |
| `needs` | Job dependency — A সফল হলে B চলবে |
| `if` | Conditional step/job execution |
| `workflow_call` | Reusable workflow trigger |
| GitHub Pages | Static site auto-deploy |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 7 — Advanced GitHub Features

---

<a id="part7"></a>
## PART 7: Advanced GitHub Features

> GitHub-এর power features যা professional developer-রা ব্যবহার করেন — Security scanning, Dependabot, GitHub Packages, GitHub CLI, Codespaces, Copilot এবং আরো। এই PART জানলে interview-এ আপনি একটু আলাদা হয়ে উঠবেন।

| # | বিষয় |
|---|-------|
| 1 | [GitHub Security Features](#p7-security) |
| 2 | [Dependabot — Automated Dependency Updates](#p7-dependabot) |
| 3 | [GitHub Packages — Package Registry](#p7-packages) |
| 4 | [GitHub CLI (gh)](#p7-cli) |
| 5 | [GitHub Codespaces](#p7-codespaces) |
| 6 | [GitHub Copilot](#p7-copilot) |
| 7 | [GitHub Pages — Advanced](#p7-pages-advanced) |
| 8 | [GitHub Webhooks](#p7-webhooks) |
| 9 | [GitHub API (REST ও GraphQL)](#p7-api) |
| 10 | [Repository Insights ও Analytics](#p7-insights) |

---

<a id="p7-security"></a>
**Topic 1: GitHub Security Features**

**GitHub-এর security layers:**

```
Code Scanning (CodeQL)
  → Code-এ vulnerability automatically detect করে

Secret Scanning
  → API key, password accidentally commit হলে alert

Dependabot Alerts
  → Known vulnerability থাকা dependency detect করে

Security Policy (SECURITY.md)
  → কীভাবে vulnerability report করবেন

Private Vulnerability Reporting
  → Public issue ছাড়া private security report
```

**Code Scanning — CodeQL:**
```yaml
# .github/workflows/codeql.yml
name: CodeQL Security Scan

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
  schedule:
    - cron: '0 6 * * 1'   # সাপ্তাহিক

jobs:
  analyze:
    name: Analyze
    runs-on: ubuntu-latest
    permissions:
      actions: read
      contents: read
      security-events: write
    
    strategy:
      matrix:
        language: [python, javascript]   # বা: java, csharp, go, ruby
    
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      
      - name: Initialize CodeQL
        uses: github/codeql-action/init@v3
        with:
          languages: ${{ matrix.language }}
      
      - name: Autobuild
        uses: github/codeql-action/autobuild@v3
      
      - name: Perform CodeQL Analysis
        uses: github/codeql-action/analyze@v3
        with:
          category: "/language:${{ matrix.language }}"
```

**Secret Scanning:**
```
GitHub → Repository → Settings → Security → Secret scanning
→ Enable secret scanning ✅
→ Push protection ✅ (push block করে যদি secret detect করে)

Supported: AWS keys, GitHub tokens, Stripe keys, Google API keys, 200+ patterns

Accidental commit হলে:
1. GitHub alert পাঠাবে
2. সেই key/token immediately revoke করুন
3. git filter-repo দিয়ে history থেকে সরান
4. Force push করুন (team-কে জানান)
```

**SECURITY.md:**
```markdown
# Security Policy

## Supported Versions

| Version | Supported |
| ------- | --------- |
| 2.x     | ✅ |
| 1.x     | ❌ |

## Reporting a Vulnerability

**Please do NOT create public issues for security vulnerabilities.**

Email: security@example.com
Response time: 48 hours

আমরা সমস্যা confirm করে 90 দিনের মধ্যে fix করব।
Fix হওয়ার পরে CVE publish করা হবে।
```

---

<a id="p7-dependabot"></a>
**Topic 2: Dependabot — Automated Dependency Updates**

**Dependabot কী:**
GitHub-এর bot যা automatically dependency updates এবং security patches-এর PR তৈরি করে।

**দুই ধরনের Dependabot:**
```
1. Dependabot Alerts — Known vulnerability থাকা packages-এ alert
2. Dependabot Version Updates — Regular dependency version updates PR
```

**dependabot.yml configuration:**
```yaml
# .github/dependabot.yml
version: 2

updates:
  # Python (pip)
  - package-ecosystem: pip
    directory: /                    # requirements.txt কোথায়
    schedule:
      interval: weekly              # daily / weekly / monthly
      day: monday
      time: "09:00"
      timezone: Asia/Dhaka
    open-pull-requests-limit: 5
    reviewers:
      - lead-developer
    labels:
      - dependencies
      - automated
    ignore:
      - dependency-name: django
        versions: ["4.x"]           # Major update ignore
    groups:
      django-ecosystem:
        patterns:
          - "django*"
          - "djangorestframework*"

  # Node.js (npm)
  - package-ecosystem: npm
    directory: /frontend
    schedule:
      interval: weekly
    open-pull-requests-limit: 10
    versioning-strategy: increase

  # Docker
  - package-ecosystem: docker
    directory: /
    schedule:
      interval: monthly

  # GitHub Actions
  - package-ecosystem: github-actions
    directory: /
    schedule:
      interval: monthly
```

**Dependabot PR দেখতে পাবেন:**
```
PR title: "chore(deps): bump requests from 2.28.0 to 2.31.0"
Label: dependencies
Auto-assigned reviewer

Merge করার আগে check করুন:
✅ CHANGELOG দেখুন — breaking change আছে?
✅ CI tests pass করছে?
✅ Major version bump-এ সাবধান
```

**Security alert response:**
```
GitHub → Security → Dependabot alerts
→ Critical/High alerts সবার আগে fix করুন

Alert-এ থাকবে:
- CVE number
- Affected version range
- Fixed version
- CVSS score
- Description
- Suggested fix (PR)
```

---

<a id="p7-packages"></a>
**Topic 3: GitHub Packages — Package Registry**

**GitHub Packages কী:**
GitHub-এ নিজের packages (npm, pip, Docker images, Maven, etc.) publish ও host করা যায়।

**Docker image publish:**
```yaml
# .github/workflows/docker-publish.yml
name: Publish Docker Image

on:
  push:
    tags: ['v*']

jobs:
  push:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      packages: write

    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Log in to GitHub Container Registry
        uses: docker/login-action@v3
        with:
          registry: ghcr.io
          username: ${{ github.actor }}
          password: ${{ secrets.GITHUB_TOKEN }}   # Auto-provided!

      - name: Extract metadata
        id: meta
        uses: docker/metadata-action@v5
        with:
          images: ghcr.io/${{ github.repository }}
          tags: |
            type=semver,pattern={{version}}
            type=semver,pattern={{major}}.{{minor}}
            type=sha

      - name: Build and push
        uses: docker/build-push-action@v6
        with:
          context: .
          push: true
          tags: ${{ steps.meta.outputs.tags }}
          labels: ${{ steps.meta.outputs.labels }}
```

**Docker image pull করুন:**
```bash
# Public image
docker pull ghcr.io/username/my-app:latest

# Private image (auth দরকার)
echo $GITHUB_TOKEN | docker login ghcr.io -u USERNAME --password-stdin
docker pull ghcr.io/username/private-app:v1.0.0
```

**npm package publish:**
```bash
# package.json-এ:
{
  "name": "@username/my-package",
  "publishConfig": {
    "registry": "https://npm.pkg.github.com"
  }
}

# .npmrc:
//npm.pkg.github.com/:_authToken=${GITHUB_TOKEN}
@username:registry=https://npm.pkg.github.com
```

---

<a id="p7-cli"></a>
**Topic 4: GitHub CLI (gh)**

**GitHub CLI কী:**
Terminal থেকে GitHub-এর সব কাজ করা যায় — PR তৈরি, issue manage, workflow run, release create।

**Install:**
```bash
# Linux
sudo apt install gh             # Ubuntu/Debian
sudo dnf install gh             # Fedora

# macOS
brew install gh

# Login
gh auth login
# → GitHub.com
# → HTTPS / SSH
# → Authenticate via browser
```

**সবচেয়ে useful commands:**
```bash
# ──────────────────────────────────────────────
# Repository
# ──────────────────────────────────────────────
gh repo create my-project --public --clone
gh repo clone username/project
gh repo view                    # Current repo info
gh repo view --web              # Browser-এ খুলুন
gh repo fork username/project --clone

# ──────────────────────────────────────────────
# Pull Requests
# ──────────────────────────────────────────────
gh pr create --title "feat: add login" --body "Adds JWT auth"
gh pr create --fill                    # Branch name + commits থেকে auto-fill
gh pr list
gh pr list --state open --assignee @me
gh pr view 42
gh pr view --web                       # Browser-এ খুলুন
gh pr checkout 42                      # PR branch checkout
gh pr review 42 --approve
gh pr review 42 --request-changes --body "Please fix the tests"
gh pr merge 42 --squash --delete-branch

# ──────────────────────────────────────────────
# Issues
# ──────────────────────────────────────────────
gh issue create --title "Bug: login crash" --label "bug"
gh issue list --label "bug" --state open
gh issue view 15
gh issue close 15 --comment "Fixed in PR #42"

# ──────────────────────────────────────────────
# GitHub Actions
# ──────────────────────────────────────────────
gh workflow list
gh workflow run ci.yml                 # Manual trigger
gh workflow run deploy.yml -f env=staging
gh run list --workflow=ci.yml
gh run view 1234567890
gh run watch                           # Live watch running workflow

# ──────────────────────────────────────────────
# Releases
# ──────────────────────────────────────────────
gh release create v1.0.0 --title "First Release" --notes "Initial release"
gh release list
gh release download v1.0.0

# ──────────────────────────────────────────────
# Secrets
# ──────────────────────────────────────────────
gh secret set DATABASE_URL
gh secret set API_KEY --body "actual-key-value"
gh secret list

# ──────────────────────────────────────────────
# GitHub Codespaces
# ──────────────────────────────────────────────
gh cs create --repo username/project
gh cs list
gh cs ssh                              # SSH into codespace
```

**Productivity aliases:**
```bash
# ~/.bashrc বা ~/.zshrc
alias ghpr='gh pr create --fill'
alias ghpl='gh pr list'
alias ghil='gh issue list'
alias ghwv='gh run watch'
```

**Interview Q&A:**
```
প্রশ্ন: "GitHub CLI কীভাবে আপনার workflow improve করেছে?"

উত্তর: "gh pr create --fill দিয়ে seconds-এ PR তৈরি করি — browser
খুলতে হয় না। gh run watch দিয়ে terminal-এই CI status দেখি।
gh pr checkout দিয়ে colleague-এর PR locally test করি।
Scripts-এ GitHub API call-এর বদলে gh CLI ব্যবহার করি — simpler।"
```

---

<a id="p7-codespaces"></a>
**Topic 5: GitHub Codespaces**

**GitHub Codespaces কী:**
Browser বা VS Code-এ cloud-based development environment। Local setup ছাড়াই project-এ কাজ করা যায়।

```
GitHub → Repository → Code → Codespaces → Create codespace on main
→ VS Code in browser (অথবা desktop VS Code)
→ সব extensions, settings, terminal ready
→ Commit ও push করা যায় directly
```

**devcontainer.json — Custom environment:**
```json
// .devcontainer/devcontainer.json
{
  "name": "Python Development",
  "image": "mcr.microsoft.com/devcontainers/python:3.11",
  
  "features": {
    "ghcr.io/devcontainers/features/docker-in-docker:2": {},
    "ghcr.io/devcontainers/features/github-cli:1": {}
  },
  
  "customizations": {
    "vscode": {
      "extensions": [
        "ms-python.python",
        "ms-python.black-formatter",
        "charliermarsh.ruff",
        "ms-azuretools.vscode-docker"
      ],
      "settings": {
        "python.defaultInterpreterPath": "/usr/local/bin/python",
        "editor.formatOnSave": true
      }
    }
  },
  
  "postCreateCommand": "pip install -r requirements.txt",
  "forwardPorts": [8000, 5432],
  
  "remoteEnv": {
    "DATABASE_URL": "${localEnv:DATABASE_URL}"
  }
}
```

**কেন Codespaces useful:**
```
✅ "Works on my machine" সমস্যা নেই — সবার same environment
✅ New developer onboarding: minutes, not days
✅ Contribute to open-source: browser-এই কাজ করুন
✅ Low-spec machine-এও powerful development
✅ Secrets safe — local-এ সংরক্ষণ নেই
```

---

<a id="p7-copilot"></a>
**Topic 6: GitHub Copilot**

**GitHub Copilot কী:**
OpenAI Codex (GPT-4 based) দিয়ে তৈরি AI pair programmer যা code suggest করে।

```
Features:
→ Inline code completion
→ Copilot Chat (conversation-based)
→ Copilot in CLI: gh copilot suggest "command to do X"
→ Copilot for PRs: PR description auto-generate
→ Copilot Workspace: Task-based development
```

**Effective Copilot usage:**
```python
# ভালো comment লিখলে ভালো suggestion পায়
# Function to validate Bengali phone number (01XXXXXXXXX format)
def validate_bd_phone(phone: str) -> bool:
    # Copilot এখানে regex সহ implementation suggest করবে

# Type hints দিলে better suggestions
def calculate_discount(price: float, discount_percent: float) -> float:
    # ...

# Test লেখার সময় বিশেষ useful
# Test that login returns 401 for invalid credentials
def test_login_invalid_credentials():
    # Copilot complete test লিখে দেবে
```

**Interview Q&A:**
```
প্রশ্ন: "GitHub Copilot ব্যবহার করেন? কীভাবে?"

উত্তর: "হ্যাঁ, boilerplate code, unit tests এবং documentation লেখায়
খুব helpful। তবে সব suggestion blindly accept করি না — code review
করি, security implications বুঝি।

বিশেষত repetitive patterns যেমন CRUD endpoints, test cases,
regex validation-এ productivity অনেক বাড়ে। Core business logic
নিজেই লিখি।"
```

---

<a id="p7-pages-advanced"></a>
**Topic 7: GitHub Pages — Advanced**

```bash
# Custom domain setup:
# 1. Repository → Settings → Pages → Custom domain
# 2. DNS provider-এ CNAME record add করুন:
#    CNAME www.example.com username.github.io

# HTTPS enforce:
# Settings → Pages → Enforce HTTPS ✅

# Jekyll theme (built-in static site generator):
# _config.yml
theme: minima
title: My Portfolio
description: Software Engineer Portfolio

# GitHub Pages কোন folder-এ build করবে:
# Settings → Pages → Source
# → Deploy from branch: /root বা /docs
# → Deploy from GitHub Actions (recommended)

# SPA (React/Vue) routing fix:
# 404.html = index.html copy করুন
# বা: HashRouter ব্যবহার করুন React-এ
```

---

<a id="p7-webhooks"></a>
**Topic 8: GitHub Webhooks**

**Webhooks কী:**
GitHub events হলে আপনার server-এ HTTP POST request পাঠানো হয়।

```
GitHub Events → Webhook → Your Server (HTTP POST)
                              ↓
                    Custom automation
                    (Slack notification, deployment, etc.)
```

**Webhook setup:**
```
Repository → Settings → Webhooks → Add webhook
→ Payload URL: https://your-server.com/webhook
→ Content type: application/json
→ Secret: (HMAC signature verify করতে)
→ Events: push, pull_request, issues, etc.
→ Active: ✅
```

**Webhook payload handle করুন (Python FastAPI):**
```python
import hashlib
import hmac
from fastapi import FastAPI, Request, HTTPException

app = FastAPI()
WEBHOOK_SECRET = "your-webhook-secret"

def verify_signature(payload_body: bytes, signature: str) -> bool:
    """GitHub webhook signature verify করুন"""
    expected = hmac.new(
        WEBHOOK_SECRET.encode(),
        payload_body,
        hashlib.sha256
    ).hexdigest()
    return hmac.compare_digest(f"sha256={expected}", signature)

@app.post("/webhook")
async def github_webhook(request: Request):
    signature = request.headers.get("X-Hub-Signature-256", "")
    body = await request.body()
    
    if not verify_signature(body, signature):
        raise HTTPException(status_code=401, detail="Invalid signature")
    
    event = request.headers.get("X-GitHub-Event")
    payload = await request.json()
    
    if event == "push" and payload["ref"] == "refs/heads/main":
        # main-এ push হলে deploy trigger করুন
        await trigger_deployment(payload)
    
    elif event == "pull_request" and payload["action"] == "opened":
        # PR open হলে Slack notification
        await notify_slack(f"New PR: {payload['pull_request']['title']}")
    
    return {"status": "ok"}
```

---

<a id="p7-api"></a>
**Topic 9: GitHub API (REST ও GraphQL)**

**REST API:**
```bash
# Base URL: https://api.github.com

# Authentication
curl -H "Authorization: Bearer $GITHUB_TOKEN" https://api.github.com/user

# Repository info
curl https://api.github.com/repos/username/project

# Create issue
curl -X POST \
  -H "Authorization: Bearer $GITHUB_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"title": "Bug found", "body": "Description here", "labels": ["bug"]}' \
  https://api.github.com/repos/username/project/issues

# List PRs
curl -H "Authorization: Bearer $GITHUB_TOKEN" \
  "https://api.github.com/repos/username/project/pulls?state=open"
```

**Python-এ PyGithub:**
```python
from github import Github

g = Github("your-token")
repo = g.get_repo("username/project")

# Issues
for issue in repo.get_issues(state="open", labels=["bug"]):
    print(f"#{issue.number}: {issue.title}")

# Create PR
pr = repo.create_pull(
    title="feat: add feature",
    body="Description",
    head="feature/my-feature",
    base="main"
)

# Workflow trigger
workflow = repo.get_workflow("deploy.yml")
workflow.create_dispatch(ref="main", inputs={"env": "staging"})
```

---

<a id="p7-insights"></a>
**Topic 10: Repository Insights ও Analytics**

```
Repository → Insights

Tabs:
→ Pulse        — recent activity (PRs, issues, commits)
→ Contributors — কে কতটুকু contribute করেছেন (commits, additions, deletions)
→ Community    — README, CONTRIBUTING, LICENSE checklist
→ Traffic      — Views, clones, popular content
→ Commits      — Commit frequency graph
→ Code frequency — Lines added/removed over time
→ Dependency graph — Dependencies ও dependents
→ Network      — Fork network visual
→ Forks        — Who forked, their branches
```

**Traffic data (API দিয়ে):**
```bash
# Repository views
curl -H "Authorization: Bearer $TOKEN" \
  https://api.github.com/repos/user/repo/traffic/views

# Clones
curl -H "Authorization: Bearer $TOKEN" \
  https://api.github.com/repos/user/repo/traffic/clones

# Popular paths
curl -H "Authorization: Bearer $TOKEN" \
  https://api.github.com/repos/user/repo/traffic/popular/paths
```

---

**PART 7 Quick Revision Table**

| Feature | কী | কোথায় |
|---------|----|----|
| CodeQL | Automated security vulnerability scan | Security tab |
| Secret Scanning | Accidentally committed secrets detect | Security tab |
| Dependabot Alerts | Vulnerable dependency detect | Security tab |
| dependabot.yml | Auto dependency update PR | `.github/dependabot.yml` |
| GitHub Packages | Docker/npm/pip package registry | `ghcr.io` |
| GitHub CLI | Terminal থেকে GitHub operations | `gh` command |
| Codespaces | Cloud-based dev environment | Code → Codespaces |
| devcontainer.json | Codespace environment config | `.devcontainer/` |
| Webhooks | GitHub events → HTTP POST to server | Settings → Webhooks |
| GITHUB_TOKEN | Auto-provided secret in Actions | `${{ secrets.GITHUB_TOKEN }}` |
| Insights | Repo analytics | Repository → Insights |
| gh pr create --fill | Auto-fill PR from branch/commits | gh CLI |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part8"></a>
## PART 8: Git Best Practices & Professional Workflow

> এই PART-এ সেইসব practices আলোচনা করা হয়েছে যা junior ও senior developer-দের আলাদা করে। Commit message standards, code review culture, GitOps, mono-repo, এবং real-world team workflow।

| # | বিষয় |
|---|-------|
| 1 | [Conventional Commits Standard](#p8-conventional-commits) |
| 2 | [Commit Message Best Practices](#p8-commit-msg) |
| 3 | [Semantic Versioning (SemVer)](#p8-semver) |
| 4 | [CHANGELOG Automation](#p8-changelog) |
| 5 | [Git Aliases — Productivity Boost](#p8-aliases) |
| 6 | [.gitignore Best Practices](#p8-gitignore) |
| 7 | [Monorepo vs Polyrepo](#p8-monorepo) |
| 8 | [GitOps](#p8-gitops) |
| 9 | [Git for Data Science Projects](#p8-data-science) |
| 10 | [Common Git Mistakes ও Prevention](#p8-mistakes) |
| 11 | [Git Interview Cheat Sheet](#p8-cheatsheet) |

---

<a id="p8-conventional-commits"></a>
**Topic 1: Conventional Commits Standard**

**Conventional Commits কী:**
একটি commit message format specification যা human-readable এবং machine-parseable উভয়ই।

**Format:**
```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Types:**
```
feat     → নতুন feature
fix      → Bug fix
docs     → Documentation পরিবর্তন
style    → Code style (formatting, semicolons) — logic change নয়
refactor → Code restructure — feature বা bug fix নয়
perf     → Performance improvement
test     → Test add বা fix
build    → Build system বা dependency পরিবর্তন (webpack, pip)
ci       → CI configuration পরিবর্তন
chore    → Maintenance (version bump, gitignore update)
revert   → Previous commit revert
```

**Real examples:**
```bash
# Simple
git commit -m "feat: add user registration endpoint"
git commit -m "fix: resolve null pointer in payment service"
git commit -m "docs: update API documentation for v2"
git commit -m "style: apply black formatting to all files"
git commit -m "refactor: extract auth logic to separate module"
git commit -m "test: add unit tests for CartService"
git commit -m "chore: upgrade Django from 4.2 to 5.0"
git commit -m "ci: add Python 3.12 to test matrix"

# With scope
git commit -m "feat(auth): implement OAuth2 Google login"
git commit -m "fix(cart): resolve quantity overflow on add"
git commit -m "perf(db): add index on user.email column"
git commit -m "test(api): add integration tests for order endpoints"

# Breaking change (!)
git commit -m "feat!: change API response format to JSON:API spec"
git commit -m "feat(api)!: remove deprecated v1 endpoints"

# With body
git commit -m "fix(payment): handle Stripe webhook timeout

Stripe webhooks can take up to 30 seconds to process.
Increased timeout from 10s to 35s and added retry logic.

Fixes #142"

# With footer (issue reference, breaking change)
git commit -m "feat(auth): add multi-factor authentication

Implements TOTP-based MFA using pyotp library.
Users can enable MFA from account settings.

BREAKING CHANGE: /api/auth/login now returns 202 (MFA required)
instead of 200 when MFA is enabled.
Closes #89
Reviewed-by: Alice <alice@example.com>"
```

**Conventional Commits-এর সুবিধা:**
```
✅ CHANGELOG automatic generation
✅ Semantic version bump automatic
✅ CI/CD-এ commit type দেখে decision নেওয়া যায়
✅ git log পড়তে সহজ
✅ Code review-এ context পাওয়া যায়
```

---

<a id="p8-commit-msg"></a>
**Topic 2: Commit Message Best Practices**

**Golden rules:**

```
1. Subject line: 50 characters বা কম (imperative mood)
   ✅ "Add user authentication"
   ❌ "Added user authentication"
   ❌ "Adding user authentication"
   ❌ "I added user authentication to the codebase to allow users to..."

2. Subject line: Capitalize first letter
   ✅ "Fix payment timeout bug"
   ❌ "fix payment timeout bug"

3. Subject line-এর শেষে period নয়
   ✅ "Update README"
   ❌ "Update README."

4. Subject ও body-এর মাঝে blank line
   feat: add login

   This implements JWT-based authentication...

5. Body line: 72 characters wrap
   (WHY explain করুন, WHAT নয় — code-ই what বলে)

6. Footer-এ issue reference
   Closes #42
   Fixes #89
```

**Bad vs Good examples:**
```bash
# ❌ Bad commits (real examples!)
git commit -m "fix"
git commit -m "wip"
git commit -m "asdf"
git commit -m "changes"
git commit -m "update code"
git commit -m "fixed the bug that was causing issues with the login system when users tried to log in with incorrect passwords"

# ✅ Good commits
git commit -m "fix(auth): reject expired JWT tokens"
git commit -m "feat: add password reset via email"
git commit -m "perf: cache user permissions in Redis"
git commit -m "docs: add API usage examples to README"
git commit -m "test: add edge cases for empty cart checkout"
```

**Atomic commits:**
```bash
# ❌ Bad: একটি commit-এ সব
git commit -m "add login, fix cart, update docs, bump version"

# ✅ Good: প্রতিটি logical change আলাদা commit
git commit -m "feat(auth): add login endpoint"
git commit -m "fix(cart): resolve quantity overflow"
git commit -m "docs: update API reference for login"
git commit -m "chore: bump version to 1.2.0"
```

---

<a id="p8-semver"></a>
**Topic 3: Semantic Versioning (SemVer)**

**Format: `MAJOR.MINOR.PATCH`**

```
v2.4.1
│ │ └── PATCH: backward-compatible bug fixes
│ └──── MINOR: backward-compatible new features
└────── MAJOR: breaking changes (backward-incompatible)
```

**কখন কোনটা bump:**
```bash
# PATCH (2.4.1 → 2.4.2)
# Bug fix, security patch, internal refactor
git commit -m "fix: resolve login crash on iOS"

# MINOR (2.4.1 → 2.5.0)
# নতুন feature, backward-compatible
git commit -m "feat: add dark mode support"

# MAJOR (2.4.1 → 3.0.0)
# Breaking change
git commit -m "feat!: redesign API response format"
# অথবা footer-এ: BREAKING CHANGE: ...
```

**Pre-release versions:**
```
1.0.0-alpha.1    → Alpha (unstable)
1.0.0-beta.1     → Beta (feature complete, not stable)
1.0.0-rc.1       → Release Candidate (ready for testing)
1.0.0            → Stable release
```

**SemVer tools:**
```bash
# Python: bump2version বা bumpversion
pip install bump2version
bump2version patch   # 1.0.0 → 1.0.1
bump2version minor   # 1.0.1 → 1.1.0
bump2version major   # 1.1.0 → 2.0.0

# Conventional commits থেকে auto version:
# semantic-release, release-please
```

---

<a id="p8-changelog"></a>
**Topic 4: CHANGELOG Automation**

**Manual CHANGELOG.md format:**
```markdown
# Changelog

All notable changes documented here.
Format: [Keep a Changelog](https://keepachangelog.com)
Versioning: [SemVer](https://semver.org)

## [Unreleased]
### Added
- Dark mode support

## [2.1.0] — 2026-03-15
### Added
- Multi-factor authentication (#89)
- Export to PDF feature (#102)

### Fixed
- Login crash on iOS Safari (#95)
- Cart quantity overflow (#98)

### Changed
- Improved error messages for API validation

### Deprecated
- `/api/v1/users` endpoint (use `/api/v2/users`)

## [2.0.0] — 2026-01-10
### Breaking Changes
- API response format changed to JSON:API spec
- Minimum Python version: 3.10

### Added
- Complete API redesign
```

**Automated CHANGELOG — release-please (Google):**
```yaml
# .github/workflows/release-please.yml
name: Release Please

on:
  push:
    branches: [main]

permissions:
  contents: write
  pull-requests: write

jobs:
  release-please:
    runs-on: ubuntu-latest
    steps:
      - uses: google-github-actions/release-please-action@v4
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          release-type: python        # node / python / go / etc.
```

```
কীভাবে কাজ করে:
1. main-এ Conventional Commits push করুন
2. release-please PR তৈরি করে: "Release 2.1.0"
3. PR-এ CHANGELOG.md auto-updated থাকবে
4. PR merge করলে → git tag + GitHub Release auto-create
```

---

<a id="p8-aliases"></a>
**Topic 5: Git Aliases — Productivity Boost**

```bash
# ~/.gitconfig বা git config --global alias.NAME 'command'
git config --global alias.st 'status'
git config --global alias.co 'checkout'
git config --global alias.br 'branch'
git config --global alias.ci 'commit'
git config --global alias.unstage 'reset HEAD --'
git config --global alias.last 'log -1 HEAD'

# Useful log aliases
git config --global alias.lg "log --oneline --graph --decorate --all"
git config --global alias.hist "log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short"

# Amend last commit
git config --global alias.amend 'commit --amend --no-edit'

# Undo last commit (keep changes)
git config --global alias.undo 'reset HEAD~1 --mixed'

# Show modified files
git config --global alias.changed 'diff --name-only'

# Delete merged branches
git config --global alias.cleanup "!git branch --merged | grep -v '\\*\\|main\\|develop' | xargs -n 1 git branch -d"
```

**~/.gitconfig এর aliases section:**
```ini
[alias]
    st = status
    co = checkout
    br = branch
    ci = commit
    unstage = reset HEAD --
    last = log -1 HEAD
    lg = log --oneline --graph --decorate --all
    amend = commit --amend --no-edit
    undo = reset HEAD~1 --mixed
    cleanup = !git branch --merged | grep -v '\\*\\|main\\|develop' | xargs -n 1 git branch -d
```

**ব্যবহার:**
```bash
git st          # git status
git lg          # beautiful log
git undo        # last commit undo
git cleanup     # merged branch delete
```

---

<a id="p8-gitignore"></a>
**Topic 6: .gitignore Best Practices**

**Python project .gitignore:**
```gitignore
# .gitignore

# ──────────────────────────────────────────────
# Python
# ──────────────────────────────────────────────
__pycache__/
*.py[cod]
*$py.class
*.so
*.egg
*.egg-info/
dist/
build/
.eggs/
.Python
.venv/
venv/
ENV/
env/

# ──────────────────────────────────────────────
# Environment & Secrets ⚠️ CRITICAL
# ──────────────────────────────────────────────
.env
.env.*
!.env.example      # Example file commit করুন
*.pem
*.key
*.p12
secrets.json
config/secrets.yml

# ──────────────────────────────────────────────
# Testing
# ──────────────────────────────────────────────
.pytest_cache/
.coverage
coverage.xml
htmlcov/
.tox/

# ──────────────────────────────────────────────
# Database
# ──────────────────────────────────────────────
*.db
*.sqlite3
*.sqlite
db.sqlite3

# ──────────────────────────────────────────────
# IDE
# ──────────────────────────────────────────────
.idea/
.vscode/
*.swp
*.swo
*~
.DS_Store       # macOS

# ──────────────────────────────────────────────
# Logs
# ──────────────────────────────────────────────
*.log
logs/
```

**Global gitignore (সব project-এ apply):**
```bash
# ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global

# Content:
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
Thumbs.db
*.swp
*.swo
.idea/
.vscode/
```

**Tracked file ignore করুন:**
```bash
# Already tracked file gitignore করতে:
git rm --cached .env           # Index থেকে সরান, file রাখুন
echo ".env" >> .gitignore
git add .gitignore
git commit -m "chore: remove .env from tracking"
```

---

<a id="p8-monorepo"></a>
**Topic 7: Monorepo vs Polyrepo**

| | Monorepo | Polyrepo |
|--|----------|---------|
| সব projects | একটি repo | আলাদা আলাদা repo |
| Code sharing | সহজ | NPM/pip package দরকার |
| CI/CD | Complex (affected packages only) | Simple per-repo |
| Team autonomy | কম | বেশি |
| Tooling | Nx, Turborepo, Bazel | সহজ |
| Who uses | Google, Microsoft, Meta | Smaller teams |

**Monorepo structure:**
```
my-company/
├── apps/
│   ├── web-app/           (React)
│   ├── mobile-app/        (React Native)
│   └── admin-dashboard/   (Vue)
├── services/
│   ├── auth-service/      (FastAPI)
│   ├── payment-service/   (Node.js)
│   └── notification/      (Go)
├── packages/
│   ├── ui-components/     (shared React components)
│   ├── api-client/        (auto-generated SDK)
│   └── utils/             (shared utilities)
├── tools/
│   └── scripts/
├── package.json           (Nx/Turborepo config)
└── turbo.json
```

**Turborepo (popular monorepo tool):**
```bash
npx create-turbo@latest
# বা add to existing: npm install turbo -D

# turbo.json
{
  "pipeline": {
    "build": {
      "dependsOn": ["^build"],
      "outputs": ["dist/**"]
    },
    "test": {
      "dependsOn": ["build"]
    },
    "lint": {}
  }
}

# Affected packages only build/test:
turbo run build --filter=[HEAD^1]
turbo run test --filter=...web-app
```

---

<a id="p8-gitops"></a>
**Topic 8: GitOps**

**GitOps কী:**
Infrastructure ও application configuration-এর desired state Git repository-তে রাখা এবং Git-কে single source of truth হিসেবে ব্যবহার করা।

```
Developer → Git push → CI pipeline
                            ↓
                    GitOps operator (ArgoCD/Flux)
                            ↓
                    Kubernetes cluster update
                    (desired state = Git state)
```

**Core principles:**
```
1. Git = Single source of truth
2. Declarative: কী হওয়া উচিত (not how)
3. Versioned: সব change git history-তে
4. Automatic: Git state ≠ cluster state → auto fix
5. Auditable: কে কখন কী deploy করেছে = git log
```

**ArgoCD example:**
```yaml
# argocd application
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: my-app
spec:
  project: default
  source:
    repoURL: https://github.com/company/k8s-configs
    targetRevision: main
    path: apps/my-app
  destination:
    server: https://kubernetes.default.svc
    namespace: production
  syncPolicy:
    automated:
      prune: true       # Git-এ না থাকলে cluster থেকে সরাও
      selfHeal: true    # Manual change হলে Git-এ ফিরে যাও
```

**GitOps benefits:**
```
✅ Audit trail: কে কখন কী deploy করেছে
✅ Rollback: git revert করলে infra rollback
✅ Disaster recovery: repo থেকে পুরো infra recreate
✅ Pull-based: cluster pulls from Git (more secure)
✅ Review: infra change = PR + code review
```

---

<a id="p8-data-science"></a>
**Topic 9: Git for Data Science Projects**

**Data Science-এ বিশেষ চ্যালেঞ্জ:**
```
❌ Large data files (CSV, model files) → Git-এ রাখা যায় না
❌ Jupyter notebooks → merge conflict nightmare (JSON format)
❌ Experiments → অনেক trial runs, কোনটা ভালো?
❌ Model weights → GB size
```

**Solutions:**

**DVC (Data Version Control):**
```bash
pip install dvc dvc-s3   # বা dvc-gdrive, dvc-azure

# Initialize
dvc init

# Large data file track করুন
dvc add data/raw/dataset.csv
# .gitignore-এ add হয়, data/raw/dataset.csv.dvc file তৈরি হয়
git add data/raw/dataset.csv.dvc data/.gitignore
git commit -m "data: add raw dataset tracking"

# Remote storage (S3, GDrive, etc.)
dvc remote add -d myremote s3://my-bucket/dvc-store
dvc push    # data remote-এ push করুন
dvc pull    # data download করুন
```

**Jupyter Notebook best practices:**
```bash
# nbstripout — output সরিয়ে clean notebook commit করুন
pip install nbstripout
nbstripout --install    # git filter install

# প্রতিটি save-এ automatically output strip হবে

# Jupytext — notebook → Python script
pip install jupytext
jupytext --to py notebook.ipynb    # .py ফাইল তৈরি হবে
# .py file-ই git-এ রাখুন — merge সহজ হয়
```

**MLflow — Experiment tracking:**
```python
import mlflow

with mlflow.start_run():
    mlflow.log_param("learning_rate", 0.01)
    mlflow.log_param("epochs", 100)
    mlflow.log_metric("accuracy", 0.95)
    mlflow.sklearn.log_model(model, "model")
```

---

<a id="p8-mistakes"></a>
**Topic 10: Common Git Mistakes ও Prevention**

**Top 10 Git mistakes:**

```bash
# ──────────────────────────────────────────────
# Mistake 1: Commit to main directly
# ──────────────────────────────────────────────
# Prevention: Branch protection rules on GitHub
# Fix: git reset --soft HEAD~1, create branch, commit

# ──────────────────────────────────────────────
# Mistake 2: Commit .env / secrets
# ──────────────────────────────────────────────
# Prevention: .gitignore + pre-commit hook + secret scanning
# Fix:
git rm --cached .env
# History cleanup:
git filter-repo --path .env --invert-paths
# Immediately revoke the exposed key!

# ──────────────────────────────────────────────
# Mistake 3: Large file in repository
# ──────────────────────────────────────────────
# Prevention: .gitignore, DVC for data
# Fix:
git filter-repo --path large-file.zip --invert-paths

# ──────────────────────────────────────────────
# Mistake 4: Force push to shared branch
# ──────────────────────────────────────────────
# Prevention: Branch protection: "Do not allow force pushes"
# Never: git push --force origin main
# If needed: git push --force-with-lease (safer)

# ──────────────────────────────────────────────
# Mistake 5: Wrong branch merge
# ──────────────────────────────────────────────
# Fix: git revert -m 1 [merge-commit-hash]

# ──────────────────────────────────────────────
# Mistake 6: git reset --hard (lost work)
# ──────────────────────────────────────────────
# Fix: git reflog → git reset --hard [old-hash]

# ──────────────────────────────────────────────
# Mistake 7: Messy commit history
# ──────────────────────────────────────────────
# Prevention: Meaningful commits from start
# Fix: git rebase -i (before push)

# ──────────────────────────────────────────────
# Mistake 8: Not pulling before push
# ──────────────────────────────────────────────
git pull --rebase origin main   # always before push
# অথবা:
git config --global pull.rebase true   # default pull = rebase

# ──────────────────────────────────────────────
# Mistake 9: Ignoring merge conflicts (<<<< left in code)
# ──────────────────────────────────────────────
# Prevention: pre-commit hook
grep -r "<<<<<<" src/ && echo "Unresolved conflicts!" && exit 1

# ──────────────────────────────────────────────
# Mistake 10: git add . (staging unwanted files)
# ──────────────────────────────────────────────
# Better: git add -p (interactive, patch by patch)
git add -p          # hunk by hunk review করুন
git diff --staged   # সবসময় review করুন commit-এর আগে
```

---

<a id="p8-cheatsheet"></a>
**Topic 11: Git Interview Cheat Sheet**

**সবচেয়ে বেশি জিজ্ঞেস করা প্রশ্ন:**

```
Q: git merge vs git rebase?
A: merge — history preserve, merge commit তৈরি করে
   rebase — linear history, commits re-apply করে
   Public branch-এ rebase করবেন না (history rewrite)

Q: git reset vs git revert?
A: reset — HEAD move করে (history change)
   revert — নতুন "undo" commit তৈরি করে (history safe)
   Pushed commits = revert, local only = reset

Q: git fetch vs git pull?
A: fetch — remote-এর latest ডাউনলোড করে, merge করে না
   pull = fetch + merge (বা fetch + rebase)
   habit: fetch করুন, diff দেখুন, তারপর merge

Q: HEAD কী?
A: Current working position-এর pointer
   সাধারণত latest commit of current branch

Q: Staging area কেন দরকার?
A: Commit-এর আগে কোন changes include করবেন select করতে
   git add -p দিয়ে partial commit করা যায়

Q: git stash কখন ব্যবহার?
A: কাজ অসম্পন্ন, branch switch করতে হবে — stash করুন
   git stash / git stash pop

Q: Detached HEAD কী?
A: HEAD কোনো branch-এ নয়, সরাসরি commit-এ
   git switch -c new-branch দিয়ে বের হন

Q: Fast-forward merge vs 3-way merge?
A: FF — linear history, divergence নেই
   3-way — দুই branch diverged, merge commit তৈরি হয়

Q: Interactive rebase কী?
A: git rebase -i HEAD~N — commit history rewrite
   squash, reword, drop, fixup, reorder

Q: Cherry-pick কখন?
A: নির্দিষ্ট commit অন্য branch-এ নিতে
   git cherry-pick [hash]

Q: Fork vs Clone?
A: Fork — GitHub server-এ আপনার account-এ copy
   Clone — local machine-এ copy

Q: PR merge strategies?
A: Merge commit — full history
   Squash and merge — clean, single commit
   Rebase and merge — linear history

Q: CI/CD কী?
A: CI — প্রতি push-এ auto test
   CD — verified code auto deploy

Q: Branch protection কী?
A: Direct push block, PR required, review required, CI must pass

Q: CODEOWNERS কী?
A: File/folder-এর owner define করে — PR-এ auto review request

Q: git reflog কী?
A: Local HEAD movements log — time machine, হারানো commit recover
```

---

**PART 8 Quick Revision Table**

| Concept | মূল কথা |
|---------|---------|
| Conventional Commits | `type(scope): description` format |
| feat/fix/docs/chore | Commit type — changelog auto-generate হয় |
| Breaking change | `feat!:` বা footer-এ `BREAKING CHANGE:` |
| Atomic commit | এক commit = এক logical change |
| SemVer | MAJOR.MINOR.PATCH — breaking/feature/bugfix |
| CHANGELOG | Conventional commits থেকে auto-generate |
| release-please | Google-এর automated release workflow |
| Git aliases | `~/.gitconfig` → `git lg`, `git undo` |
| .gitignore | `.env`, `__pycache__`, `.venv` সবসময় ignore |
| `git rm --cached` | Tracked file untrack করুন |
| Monorepo | সব projects একটি repo — Turborepo, Nx |
| GitOps | Git = infrastructure source of truth |
| DVC | Large data files version control |
| nbstripout | Jupyter output strip before commit |
| `git add -p` | Selective staging (patch mode) |
| `git push --force-with-lease` | Force push-এর safer alternative |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **📌 পরবর্তী:** PART 9 — Git Internals Deep Dive ও Troubleshooting

---

<a id="part9"></a>
## PART 9: Git Internals Deep Dive ও Troubleshooting

> Git-এর ভেতরের কাজকর্ম বোঝা এবং সমস্যা সমাধান করার advanced skills। `git bisect`, `git blame`, `git log` advanced filters, pack files, garbage collection এবং performance tuning।

| # | বিষয় |
|---|-------|
| 1 | [git bisect — Binary Search for Bugs](#p9-bisect) |
| 2 | [git blame — কে কী লিখেছে](#p9-blame) |
| 3 | [git log Advanced Filtering](#p9-log-advanced) |
| 4 | [git diff Advanced](#p9-diff-advanced) |
| 5 | [git grep — Repository-wide Search](#p9-grep) |
| 6 | [git show ও git cat-file](#p9-show) |
| 7 | [Pack Files ও Object Storage](#p9-packfiles) |
| 8 | [Garbage Collection (git gc)](#p9-gc) |
| 9 | [git fsck — Repository Integrity](#p9-fsck) |
| 10 | [Performance Tuning](#p9-performance) |
| 11 | [Common Error Messages ও Fix](#p9-errors) |
| 12 | [git worktree — Multiple Working Directories](#p9-worktree) |

---

<a id="p9-bisect"></a>
**Topic 1: git bisect — Binary Search for Bugs**

**সংজ্ঞা:**
"কোন commit-এ bug টি introduce হয়েছিল?" — এই প্রশ্নের উত্তর binary search দিয়ে খুঁজে বের করে `git bisect`।

**কীভাবে কাজ করে:**
```
Commits: A ─── B ─── C ─── D ─── E ─── F ─── G
                                             ↑
                                           HEAD (bug আছে)

git bisect: D test করো → bad
            B test করো → good
            C test করো → bad → C-তেই bug introduce হয়েছে!
```

**Manual bisect:**
```bash
# Start
git bisect start

# Current state (HEAD) — bad
git bisect bad

# Known good state (যে version-এ bug ছিল না)
git bisect good v1.0.0
# অথবা commit hash:
git bisect good 3a7f8b2

# Git এখন middle commit checkout করবে
# Test করুন...
# Bug আছে:
git bisect bad
# Bug নেই:
git bisect good

# Git আবার middle-এ যাবে → test → bad/good
# কয়েক step পরে:
# "3a7f8b2 is the first bad commit"

# End
git bisect reset    # original HEAD-এ ফিরে যান
```

**Automated bisect — test script দিয়ে:**
```bash
# test.sh
#!/bin/bash
python -m pytest tests/test_login.py::test_user_login -q
# exit 0 = good, exit 1 = bad

# Automated run
git bisect start
git bisect bad HEAD
git bisect good v2.0.0
git bisect run ./test.sh   # automatically সব steps!

# Output:
# Running: ./test.sh
# ...
# b2c4d5e is the first bad commit
# commit b2c4d5e
# Author: Bob <bob@example.com>
# Date:   Mon Mar 10 14:30:00 2026
#     feat: refactor auth middleware
```

**Interview Q&A:**
```
প্রশ্ন: "Production-এ bug আছে কিন্তু কোন commit থেকে এলো জানেন না।
কীভাবে খুঁজবেন?"

উত্তর: "git bisect ব্যবহার করব। একটি known-good commit
(যেমন last stable tag) এবং current bad state দিয়ে bisect শুরু করব।
Git binary search করে মাঝের commit checkout করবে।
Test করব — bad বা good mark করব।
কয়েক step পরে Git নির্দিষ্ট commit বলে দেবে।

Test script থাকলে git bisect run দিয়ে fully automated করা যায়।"
```

---

<a id="p9-blame"></a>
**Topic 2: git blame — কে কী লিখেছে**

**সংজ্ঞা:**
`git blame` প্রতিটি line-এর জন্য দেখায় কে, কখন, কোন commit-এ লিখেছে।

```bash
git blame src/auth/login.py

# Output:
# a1b2c3d4 (Alice     2026-03-10 14:30 +0600  1) def login(email: str, password: str):
# b2c4d5e6 (Bob       2026-02-15 09:00 +0600  2)     user = get_user_by_email(email)
# a1b2c3d4 (Alice     2026-03-10 14:30 +0600  3)     if not user:
# c3d4e5f6 (Charlie   2026-01-20 11:00 +0600  4)         raise AuthError("User not found")
# b2c4d5e6 (Bob       2026-02-15 09:00 +0600  5)     if not verify_password(password, user.password_hash):
# d4e5f6a7 (Alice     2026-03-15 16:00 +0600  6)         raise AuthError("Invalid credentials")
# a1b2c3d4 (Alice     2026-03-10 14:30 +0600  7)     return generate_token(user)
```

**Useful options:**
```bash
# Specific lines (5 থেকে 20)
git blame -L 5,20 src/auth/login.py

# Function/method blame
git blame -L '/def login/,/^def/' src/auth/login.py

# Whitespace ignore করুন
git blame -w src/auth/login.py

# Copy/move detect করুন (refactoring)
git blame -C src/auth/login.py   # same file-এর copy
git blame -CC src/auth/login.py  # অন্য file-এর copy

# Specific commit-এর সময়ের blame
git blame v1.0.0 -- src/auth/login.py

# Email দেখুন (name-এর বদলে)
git blame -e src/auth/login.py

# Date format
git blame --date=short src/auth/login.py
```

**VS Code-এ GitLens:**
```
Extension: GitLens (eamodio.gitlens)
→ প্রতিটি line-এ inline blame দেখা যায়
→ Author, date, commit message
→ Commit history navigation
```

**Real use case:**
```bash
# একটি mysterious bug খুঁজে পেলেন line 145-এ
git blame src/payment.py -L 145,145
# b2c4d5e6 (Bob 2026-02-15) 145) return amount * 1.15  # VAT

# Bob-এর সেই commit দেখুন
git show b2c4d5e6
# Context বুঝলেন — সমস্যা fix করলেন
```

---

<a id="p9-log-advanced"></a>
**Topic 3: git log Advanced Filtering**

```bash
# ──────────────────────────────────────────────
# Author/Committer filter
# ──────────────────────────────────────────────
git log --author="Alice"
git log --author="alice@example.com"
git log --committer="Bob"

# ──────────────────────────────────────────────
# Date filter
# ──────────────────────────────────────────────
git log --since="2026-01-01"
git log --until="2026-03-31"
git log --since="2 weeks ago"
git log --after="yesterday"
git log --since="2026-01-01" --until="2026-03-31"

# ──────────────────────────────────────────────
# Message search
# ──────────────────────────────────────────────
git log --grep="fix"              # message-এ "fix" আছে
git log --grep="feat" --grep="auth" --all-match   # দুটোই থাকতে হবে
git log --grep="fix" -i           # case-insensitive

# ──────────────────────────────────────────────
# Code change search (Pickaxe)
# ──────────────────────────────────────────────
git log -S "verify_password"      # এই string add/remove করা commits
git log -G "def login"            # regex match

# ──────────────────────────────────────────────
# File/path filter
# ──────────────────────────────────────────────
git log -- src/auth/login.py      # specific file-এর history
git log -- src/auth/             # directory
git log -- "*.py"                 # pattern

# ──────────────────────────────────────────────
# Limit
# ──────────────────────────────────────────────
git log -5                        # শেষ 5টি
git log -n 10                     # শেষ 10টি

# ──────────────────────────────────────────────
# Format
# ──────────────────────────────────────────────
git log --oneline
git log --oneline --graph --all --decorate
git log --stat                    # changed files count
git log -p                        # full diff (patch)
git log --name-only               # শুধু file names
git log --name-status             # A/M/D status সহ

# Custom format
git log --pretty=format:"%h | %an | %ad | %s" --date=short
# a1b2c3d | Alice | 2026-03-10 | feat: add login

# ──────────────────────────────────────────────
# Range
# ──────────────────────────────────────────────
git log main..feature/login       # feature-এ আছে, main-এ নেই
git log main...feature/login      # দুই দিক থেকে আলাদা commits
git log v1.0.0..v2.0.0           # release-এর মধ্যে

# ──────────────────────────────────────────────
# Merge commits
# ──────────────────────────────────────────────
git log --merges                  # শুধু merge commits
git log --no-merges               # merge commits বাদে
git log --first-parent            # merge branch history বাদে, main line শুধু
```

---

<a id="p9-diff-advanced"></a>
**Topic 4: git diff Advanced**

```bash
# ──────────────────────────────────────────────
# Basic diffs
# ──────────────────────────────────────────────
git diff                         # working dir vs staging
git diff --staged                # staging vs last commit
git diff --cached                # same as --staged
git diff HEAD                    # working dir vs last commit

# ──────────────────────────────────────────────
# Commit comparison
# ──────────────────────────────────────────────
git diff HEAD~1 HEAD             # last two commits
git diff v1.0.0 v2.0.0          # between tags
git diff main feature/login      # between branches
git diff a1b2c3d b2c4d5e         # between hashes

# ──────────────────────────────────────────────
# Specific file
# ──────────────────────────────────────────────
git diff HEAD -- src/auth.py
git diff main..feature -- src/

# ──────────────────────────────────────────────
# Stat (summary only)
# ──────────────────────────────────────────────
git diff --stat main..feature
# src/auth.py   | 25 +++++++++---------
# tests/test_auth.py | 40 ++++++++++++++++++++++

git diff --shortstat main..feature
# 2 files changed, 65 insertions(+), 9 deletions(-)

# ──────────────────────────────────────────────
# Word-level diff (ভালো readability)
# ──────────────────────────────────────────────
git diff --word-diff
git diff --word-diff=color

# ──────────────────────────────────────────────
# Whitespace ignore
# ──────────────────────────────────────────────
git diff -w                      # সব whitespace ignore
git diff -b                      # trailing whitespace ignore

# ──────────────────────────────────────────────
# Name only (changed files list)
# ──────────────────────────────────────────────
git diff --name-only HEAD~3
git diff --name-status HEAD~3    # A/M/D status

# ──────────────────────────────────────────────
# External diff tool
# ──────────────────────────────────────────────
git difftool                     # configured tool
git difftool --tool=vimdiff
git config --global diff.tool vscode
git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'
```

---

<a id="p9-grep"></a>
**Topic 5: git grep — Repository-wide Search**

```bash
# Basic search
git grep "verify_password"
git grep "TODO"

# Case-insensitive
git grep -i "todo"

# Regex
git grep -E "def (login|logout)"

# Line numbers
git grep -n "api_key"

# Count matches per file
git grep -c "import"

# Only file names
git grep -l "DATABASE_URL"

# Context lines (before/after)
git grep -B 3 -A 3 "raise AuthError"

# Specific branch বা commit
git grep "old_function" main
git grep "old_function" v1.0.0

# Multiple patterns
git grep -e "login" --and -e "password"

# All branches
git grep "deprecated" $(git rev-list --all)

# Practical: Find all TODO comments with file+line
git grep -n "TODO\|FIXME\|HACK" --include="*.py"
```

**git grep vs grep:**
```
git grep:
✅ .gitignore respect করে
✅ Faster (git index ব্যবহার করে)
✅ Branch/commit-এ search করা যায়
✅ Binary files skip করে automatically

grep/ripgrep:
✅ git repository ছাড়াও কাজ করে
✅ More advanced regex
✅ ripgrep (rg) সবচেয়ে fast
```

---

<a id="p9-show"></a>
**Topic 6: git show ও git cat-file**

**git show:**
```bash
# Commit details + diff
git show HEAD
git show a1b2c3d
git show v1.0.0

# শুধু commit info (diff ছাড়া)
git show --stat HEAD
git show --name-only HEAD

# Specific file at commit
git show HEAD:src/auth.py        # HEAD-এর auth.py দেখুন
git show v1.0.0:README.md        # v1.0.0-এর README

# Tag details
git show v1.0.0

# Stash
git show stash@{0}

# Branch tip
git show main
git show origin/main
```

**git cat-file — low-level object inspection:**
```bash
# Object type
git cat-file -t HEAD
# commit

git cat-file -t HEAD^{tree}
# tree

# Object size
git cat-file -s HEAD
# 287  (bytes)

# Object content
git cat-file -p HEAD
# tree 7b8c...
# parent 3a7f...
# author Alice <alice@example.com> 1715500000 +0600
# committer Alice <alice@example.com> 1715500000 +0600
#
# feat: add login functionality

git cat-file -p HEAD^{tree}
# 100644 blob a8c3... README.md
# 040000 tree b2d4... src
# 100644 blob c5e6... requirements.txt

# File content at specific commit
git cat-file blob HEAD:src/auth.py
```

---

<a id="p9-packfiles"></a>
**Topic 7: Pack Files ও Object Storage**

**Loose objects vs Pack files:**

```bash
# Loose objects: .git/objects/ab/cdef...
# প্রতিটি object আলাদা file
ls .git/objects/
# 3a/  b2/  c4/  pack/  info/

# Pack files: অনেক objects একটি compressed file-এ
ls .git/objects/pack/
# pack-abc123.idx   (index — fast lookup)
# pack-abc123.pack  (data)
# pack-abc123.rev   (reverse index)
```

**কীভাবে pack file তৈরি হয়:**
```bash
# Git automatically করে:
# 1. git gc চালালে
# 2. git fetch/clone-এ remote থেকে
# 3. 50+ loose objects হলে

# Manual repack:
git repack -a -d -f           # সব loose objects pack করুন, old pack delete

# Pack file inspect করুন
git verify-pack -v .git/objects/pack/pack-abc123.idx | head -20
# sha1 type size size-in-packfile offset-in-packfile
# a1b2c3d commit 287 215 12
# b2c4d5e blob   1024 456 227
```

**Delta compression:**
```
Pack files use delta compression:
- Similar objects (file versions) → base + diff store করে
- Large space savings for text files (source code)
- git log history চলার সাথে সাথে rebuild করে
```

---

<a id="p9-gc"></a>
**Topic 8: Garbage Collection (git gc)**

**git gc কী:**
Unreachable objects, old reflog entries এবং loose objects cleanup করে।

```bash
# Manual garbage collection
git gc

# Aggressive GC (more thorough, slower)
git gc --aggressive

# Prune করুন (unreachable objects delete)
git gc --prune=now        # সব unreachable এখনই delete
git gc --prune=2.weeks.ago  # 2 সপ্তাহের পুরোনো unreachable delete (default)

# Auto GC (already runs automatically)
git gc --auto

# GC stats দেখুন
git count-objects -v
# count: 5          (loose objects)
# size: 20          (KB)
# in-pack: 1523     (packed objects)
# packs: 1
# size-pack: 423    (KB)
# prune-packable: 0
# garbage: 0
# size-garbage: 0
```

**Auto GC trigger:**
```bash
# Default: 6700+ loose objects বা 50+ packs হলে auto
git config gc.auto 6700        # loose object threshold
git config gc.autopacklimit 50 # pack file threshold
git config gc.autoDetach true  # background-এ চলে
```

**reflog expiry:**
```bash
# Reflog entries কতদিন রাখবে
git config gc.reflogExpire "90 days"          # default
git config gc.reflogExpireUnreachable "30 days"

# Manual expire
git reflog expire --expire=30.days --all
```

---

<a id="p9-fsck"></a>
**Topic 9: git fsck — Repository Integrity**

**git fsck কী:**
Git repository-র integrity check করে — corrupt বা dangling objects খুঁজে বের করে।

```bash
# Full integrity check
git fsck

# Output examples:
# Checking object directory...
# Checking connectivity...
# dangling blob a1b2c3d     ← unreachable blob
# dangling commit b2c4d5e  ← unreachable commit (সম্ভবত reset --hard-এ হারিয়েছে)
# unreachable tree c3d4e5f

# Dangling commits (হারানো commits recover করতে পারেন)
git fsck --lost-found
# .git/lost-found/commit/a1b2c3d  (dangling commits)
# .git/lost-found/other/b2c4d5e   (dangling blobs/trees)

# Verbose
git fsck --verbose

# Specific object check
git fsck --full

# Strict mode
git fsck --strict
```

**হারানো commit recover করুন:**
```bash
# git fsck দিয়ে dangling commits খুঁজুন
git fsck --lost-found

# Dangling commit দেখুন
git log --oneline .git/lost-found/commit/

# অথবা সরাসরি
git show a1b2c3d   # dangling commit দেখুন

# Branch তৈরি করে recover করুন
git checkout -b recovered a1b2c3d
```

---

<a id="p9-performance"></a>
**Topic 10: Performance Tuning**

**Large repository performance:**

```bash
# ──────────────────────────────────────────────
# Shallow clone (full history দরকার নেই)
# ──────────────────────────────────────────────
git clone --depth=1 https://github.com/org/repo.git
# শুধু latest commit — CI/CD-এর জন্য ideal

# Specific branch, shallow
git clone --depth=1 --branch main https://github.com/org/repo.git

# Shallow → full (পরে full history দরকার হলে)
git fetch --unshallow

# ──────────────────────────────────────────────
# Sparse checkout (partial checkout)
# ──────────────────────────────────────────────
git clone --filter=blob:none --sparse https://github.com/org/monorepo.git
cd monorepo
git sparse-checkout set apps/web-app packages/ui-components
# শুধু নির্দিষ্ট directories checkout হবে

# ──────────────────────────────────────────────
# Partial clone (blob filter)
# ──────────────────────────────────────────────
git clone --filter=blob:none https://github.com/org/repo.git
# Blobs on-demand fetch করে — large binary files clone-এ skip

# ──────────────────────────────────────────────
# File system monitor
# ──────────────────────────────────────────────
git config core.fsmonitor true         # FS events watch করে
git config core.untrackedCache true    # Untracked file cache

# ──────────────────────────────────────────────
# Index optimization
# ──────────────────────────────────────────────
git update-index --index-version 4    # Faster index format

# ──────────────────────────────────────────────
# Maintenance (background tasks)
# ──────────────────────────────────────────────
git maintenance start                  # Background maintenance enable
git maintenance run --task=gc
git maintenance run --task=commit-graph
git maintenance run --task=prefetch
```

**Commit graph (faster log/merge-base):**
```bash
# Commit graph file তৈরি করুন (very large repos-এ helpful)
git commit-graph write --reachable
git config core.commitGraph true
git config fetch.writeCommitGraph true
```

---

<a id="p9-errors"></a>
**Topic 11: Common Error Messages ও Fix**

```bash
# ──────────────────────────────────────────────
# Error: "Your local changes would be overwritten by merge"
# ──────────────────────────────────────────────
git stash
git pull
git stash pop

# ──────────────────────────────────────────────
# Error: "fatal: refusing to merge unrelated histories"
# ──────────────────────────────────────────────
# হয়: দুটি আলাদা git init হওয়া repo connect করলে
git pull origin main --allow-unrelated-histories

# ──────────────────────────────────────────────
# Error: "error: failed to push some refs"
# "hint: Updates were rejected because the remote contains work"
# ──────────────────────────────────────────────
git pull --rebase origin main   # বা git pull origin main
git push origin main

# ──────────────────────────────────────────────
# Error: "CONFLICT (content): Merge conflict in file.py"
# ──────────────────────────────────────────────
git status             # conflict files দেখুন
# Manually resolve করুন (<<<< ==== >>>> markers সরান)
git add file.py
git commit

# ──────────────────────────────────────────────
# Error: "detached HEAD state"
# ──────────────────────────────────────────────
git switch -c new-branch    # নতুন branch তৈরি করুন
# অথবা: git checkout main   # main-এ ফিরুন

# ──────────────────────────────────────────────
# Error: "git push rejected — non-fast-forward"
# ──────────────────────────────────────────────
git pull --rebase origin main   # rebase করুন
git push origin main

# ──────────────────────────────────────────────
# Error: "cannot lock ref" বা "ref file exists"
# ──────────────────────────────────────────────
rm .git/refs/heads/branch-name   # lock file সরান
# অথবা:
rm .git/index.lock               # index lock

# ──────────────────────────────────────────────
# Error: "SSL certificate problem"
# ──────────────────────────────────────────────
# Corporate proxy-তে হয়
git config --global http.sslVerify false   # ⚠️ শুধু trusted network-এ
# Better: CA certificate configure করুন

# ──────────────────────────────────────────────
# Error: "Permission denied (publickey)"
# ──────────────────────────────────────────────
# SSH key issue
ssh-add ~/.ssh/id_ed25519        # agent-এ key add করুন
ssh -T git@github.com            # test করুন

# ──────────────────────────────────────────────
# Error: "repository not found"
# ──────────────────────────────────────────────
git remote -v                    # URL check করুন
git remote set-url origin git@github.com:user/repo.git  # fix করুন

# ──────────────────────────────────────────────
# Error: "LF will be replaced by CRLF" (Windows)
# ──────────────────────────────────────────────
git config --global core.autocrlf input   # Linux/Mac
git config --global core.autocrlf true    # Windows
# .gitattributes:
# * text=auto
# *.py text eol=lf

# ──────────────────────────────────────────────
# Error: "index file smaller than expected"
# ──────────────────────────────────────────────
# Corrupt index
rm .git/index
git reset   # index rebuild করবে
```

---

<a id="p9-worktree"></a>
**Topic 12: git worktree — Multiple Working Directories**

**git worktree কী:**
একটি repository-র একাধিক branch একসাথে আলাদা directory-তে checkout করা — clone না করেই।

```bash
# বর্তমান worktrees দেখুন
git worktree list

# নতুন worktree add করুন
git worktree add ../hotfix-branch hotfix/payment-crash
# ../hotfix-branch directory-তে hotfix/payment-crash branch checkout হবে

# নতুন branch সহ
git worktree add -b hotfix/new-fix ../my-hotfix main

# কাজ করুন hotfix-এ (আলাদা terminal)
cd ../hotfix-branch
# ... fix করুন, commit করুন ...

# Worktree remove করুন
git worktree remove ../hotfix-branch
git worktree prune    # stale worktrees cleanup

# ──────────────────────────────────────────────
# Real use case: Feature-এ কাজ করছেন, urgent hotfix দরকার
# ──────────────────────────────────────────────
# আগে: stash করতেন, branch switch করতেন
# এখন: worktree add করুন — দুটি directory, দুটি branch একসাথে!

git worktree add ../urgent-fix main
cd ../urgent-fix
git checkout -b hotfix/critical-bug
# fix করুন
git commit -m "fix: critical payment bug"
# Main project-এ ফিরে যান
cd ../original-project
# feature কাজ continue করুন — কিছুই হারায়নি!
```

---

**PART 9 Quick Revision Table**

| Command | কী করে |
|---------|--------|
| `git bisect start/bad/good` | Binary search — bug-introducing commit খুঁজুন |
| `git bisect run script.sh` | Automated bisect |
| `git blame -L 5,20 file.py` | Line-by-line author history |
| `git log -S "string"` | Code string add/remove করা commits |
| `git log -G "regex"` | Regex match করা diff-এর commits |
| `git log --author="Alice"` | Specific author-এর commits |
| `git log main..feature` | feature-এ আছে, main-এ নেই |
| `git diff --word-diff` | Word-level diff |
| `git grep -n "pattern"` | Repo-wide search with line numbers |
| `git show HEAD:file.py` | Specific commit-এ file দেখুন |
| `git cat-file -p HEAD` | Low-level object content |
| `git gc --aggressive` | Thorough garbage collection |
| `git fsck --lost-found` | Dangling objects → lost-found |
| `git clone --depth=1` | Shallow clone (CI/CD-এর জন্য) |
| `git sparse-checkout set` | Partial checkout |
| `git worktree add` | Multiple branches, multiple directories |
| `rm .git/index.lock` | Lock file error fix |

---

[⬆ শীর্ষে ফিরুন](#top)

---

<a id="part10"></a>
## PART 10: Real-World Git Scenarios ও Interview Masterclass

> এই PART হলো complete interview preparation। Real-world scenarios, system design questions, complete Q&A bank এবং quick reference card — সব এক জায়গায়।

| # | বিষয় |
|---|-------|
| 1 | [Real-World Scenarios — Simulation](#p10-scenarios) |
| 2 | [System Design: Git Workflow for Large Team](#p10-system-design) |
| 3 | [Junior Engineer Interview Q&A Bank](#p10-junior-qa) |
| 4 | [Senior Engineer Interview Questions](#p10-senior-qa) |
| 5 | [GitHub Actions Interview Questions](#p10-actions-qa) |
| 6 | [Practical Coding Test Tips](#p10-practical) |
| 7 | [Complete Git Command Quick Reference](#p10-reference) |
| 8 | [One-Page Cheat Sheet](#p10-cheatsheet) |

---

<a id="p10-scenarios"></a>
**Topic 1: Real-World Scenarios — Simulation**

এই scenarios গুলো interview-তে "কী করবেন?" ধরনের প্রশ্নে হুবহু ব্যবহার করতে পারবেন।

---

**Scenario A: Production-এ critical bug, আপনি feature কাজ করছেন**

```bash
# আপনি feature/payment-redesign branch-এ কাজ করছেন
git status
# modified: src/payment/checkout.py

# Step 1: কাজ save করুন
git stash push -m "WIP: payment redesign"
# অথবা: commit করুন draft হিসেবে
git add . && git commit -m "wip: payment redesign (in progress)"

# Step 2: main থেকে hotfix branch
git checkout main
git pull origin main
git checkout -b hotfix/login-500-error

# Step 3: Bug fix করুন
# ... fix করলেন ...
git add src/auth/login.py
git commit -m "fix(auth): resolve 500 error on concurrent login"

# Step 4: PR দিন বা direct merge করুন (emergency)
git checkout main
git merge --no-ff hotfix/login-500-error
git push origin main
git tag v2.1.1 -m "hotfix: login 500 error"
git push origin v2.1.1

# Step 5: Feature-এ ফিরুন
git checkout feature/payment-redesign
git stash pop   # অথবা: কাজ already commit-এ আছে
git rebase main  # latest main changes নিন
```

---

**Scenario B: Team member-এর PR-এ conflict, আপনার review**

```bash
# PR review করতে branch checkout করুন
gh pr checkout 45
# = git fetch origin pull/45/head:pr-45 && git checkout pr-45

# Conflict test করুন (local-এ main-এর সাথে merge করে দেখুন)
git merge main
# CONFLICT (content): Merge conflict in src/models/user.py

# Conflict resolve করুন
# ... edit করলেন ...
git add src/models/user.py
git commit -m "merge: resolve conflict with main"

# PR-এ comment দিন:
# "Conflict found with main. Please rebase: git rebase main"

# GitHub-এ review:
gh pr review 45 --request-changes \
  --body "Please rebase your branch on main to resolve the conflict in user.py"
```

---

**Scenario C: Accidental commit to main, team shared**

```bash
# main-এ ভুলে commit করেছেন
git log --oneline -3
# a1b2c3d (HEAD -> main, origin/main) feat: add broken feature
# b2c4d5e (origin/main) fix: update auth

# Wait — origin/main মানে আগেই push হয়েছে!
# git reset --hard করা যাবে না — team break হবে

# Safe fix: git revert
git revert a1b2c3d --no-edit
git push origin main

# Team-কে জানান:
# "Reverted accidental commit a1b2c3d. Please pull."
# git pull --rebase করলেই হবে তাদের
```

---

**Scenario D: পুরো feature delete করতে হবে (not merged yet)**

```bash
# feature/dark-mode branch — stakeholder বললেন বাদ দিতে
git branch -D feature/dark-mode    # local delete

# Remote delete
git push origin --delete feature/dark-mode

# প্রথমে GitHub-এ PR close করুন (don't merge)
gh pr close 67 --comment "Feature cancelled per product decision"

# যদি কোনো commits main-এ চলে গিয়ে থাকে:
git log --oneline main | grep "dark-mode"
# c3d4e5f feat: add dark mode toggle

# Revert করুন
git revert c3d4e5f --no-edit
git push origin main
```

---

**Scenario E: Release tag করুন এবং deploy করুন**

```bash
# Release branch তৈরি করুন
git checkout develop
git pull origin develop
git checkout -b release/2.0.0

# Version bump করুন
sed -i 's/version = "1.9.0"/version = "2.0.0"/' setup.py
git add setup.py
git commit -m "chore: bump version to 2.0.0"

# Final testing করুন (CI pass হলে)

# Main-এ merge
git checkout main
git pull origin main
git merge --no-ff release/2.0.0
git tag -a v2.0.0 -m "Release 2.0.0 — Major redesign"
git push origin main --tags

# Develop-এও merge
git checkout develop
git merge --no-ff release/2.0.0
git push origin develop

# Release branch delete
git branch -d release/2.0.0
git push origin --delete release/2.0.0

# GitHub Release তৈরি করুন
gh release create v2.0.0 \
  --title "v2.0.0 — Major Redesign" \
  --notes "$(cat CHANGELOG.md | head -50)" \
  --target main
```

---

<a id="p10-system-design"></a>
**Topic 2: System Design: Git Workflow for Large Team**

**Interview question:** "১০০ জন developer-এর team-এ Git workflow কীভাবে setup করবেন?"

**Answer structure:**

```
1. Repository Strategy:
   - Monorepo (shared tooling, Nx/Bazel)
   - অথবা: Service-per-repo (microservices)
   - Decision factor: code sharing, team autonomy

2. Branching Strategy:
   - GitHub Flow (continuous deployment web app)
   - Git Flow (versioned mobile/desktop app)
   - Trunk-Based (very mature CI, feature flags)

3. Branch Protection:
   - main: PR required, 2 reviewers, CI must pass
   - develop: PR required, 1 reviewer
   - No direct push, no force push
   - CODEOWNERS for domain-specific review

4. CI/CD Pipeline:
   PR opened:    lint + unit tests (fast, < 5 min)
   PR approved:  integration tests
   Merge to main: full suite + staging deploy
   Tag pushed:   production deploy

5. Code Quality Gates:
   - Linting (flake8, ESLint)
   - Type checking (mypy, TypeScript)
   - Test coverage minimum (e.g., 80%)
   - Security scan (CodeQL, Snyk)
   - Dependency scan (Dependabot)

6. Commit Standards:
   - Conventional Commits enforced via commitlint + Husky
   - PR title = squash commit message
   - Auto CHANGELOG via release-please

7. Access Control:
   - GitHub Organization + Teams
   - Least privilege principle
   - Periodic access review (quarterly)
   - SSO integration (SAML/OIDC)

8. Developer Experience:
   - devcontainer.json for consistent env
   - Pre-commit hooks (local fast checks)
   - Git aliases, good documentation
   - Onboarding checklist
```

---

<a id="p10-junior-qa"></a>
**Topic 3: Junior Engineer Interview Q&A Bank**

**প্রশ্ন ১: Git কী এবং কেন ব্যবহার করি?**
```
Git একটি distributed version control system। Code-এর সব পরিবর্তন
track করে, যেকোনো সময় আগের version-এ ফিরতে পারা যায়, team-এর
সবাই একসাথে কাজ করতে পারে conflict ছাড়াই।

Distributed মানে প্রতিজনের কাছে full history আছে — server down
হলেও কাজ চলে।
```

**প্রশ্ন ২: git add এবং git commit-এর পার্থক্য?**
```
git add: পরিবর্তনগুলো staging area-তে রাখে — "commit করার জন্য prepare"
git commit: staging area-র সব changes repository-তে save করে
           একটি permanent snapshot তৈরি করে

Staging area-র কারণ: কিছু changes commit করব, কিছু না —
selective করা যায়।
```

**প্রশ্ন ৩: git pull এবং git fetch-এর পার্থক্য?**
```
git fetch: remote-এর latest changes download করে, কিন্তু
           working directory-তে apply করে না।
           Safe — কী এলো আগে দেখা যায়।

git pull: fetch + merge (বা fetch + rebase)।
          Immediately working branch update হয়।

Best practice: git fetch করুন, git diff origin/main দেখুন, তারপর merge।
```

**প্রশ্ন ৪: Merge conflict কীভাবে resolve করবেন?**
```
1. git status দিয়ে conflict files দেখি
2. File খুলি — <<<<<<, =======, >>>>>>> markers দেখি
3. কোন version রাখব decide করি (বা দুটো মিলিয়ে)
4. Markers সরিয়ে দিই
5. git add করি
6. git commit দিই

IDE/VS Code-এর merge editor অনেক সহজ করে দেয়।
```

**প্রশ্ন ৫: Branch কী? কেন ব্যবহার করি?**
```
Branch হলো main codebase থেকে আলাদা একটি line of development।
feature/login branch-এ কাজ করলে main branch-এ কোনো impact নেই।

কেন: Isolation — experiment করা যায়, টিমের অন্যদের কাজ break হয় না।
Multiple features parallel-এ develop করা যায়।
```

**প্রশ্ন ৬: git stash কী?**
```
Uncommitted changes temporarily save করার জায়গা।
Branch switch করতে হবে কিন্তু commit করতে চাই না — git stash করি।
পরে git stash pop দিয়ে ফিরিয়ে আনি।
```

**প্রশ্ন ৭: .gitignore কী?**
```
Git কোন files track করবে না সেটা বলে দেওয়ার file।
.env (secrets), __pycache__, node_modules, build output — এগুলো
repository-তে থাকা উচিত নয়।
```

**প্রশ্ন ৮: Fork এবং Clone পার্থক্য?**
```
Clone: repository local machine-এ copy করা।
Fork: GitHub-এ নিজের account-এ repository-র copy করা।

Open-source contribute করতে Fork করি — নিজের copy-তে কাজ করি,
তারপর Pull Request দিই।
```

**প্রশ্ন ৯: Pull Request (PR) কী?**
```
GitHub-এ "এই changes main branch-এ নিন" এর formal request।
Code review, discussion, automated tests — সব এক জায়গায়।
Team-এ code quality maintain করার প্রধান mechanism।
```

**প্রশ্ন ১০: git rebase কী? Merge থেকে কীভাবে আলাদা?**
```
Merge: দুটি branch-এর history combine করে, merge commit তৈরি হয়।
Rebase: feature branch-এর commits main-এর latest-এর উপর re-apply করে
        — linear, clean history।

Main branch-এ already আছে এমন commits rebase করবেন না (history rewrite,
team-এর সমস্যা)।
```

---

<a id="p10-senior-qa"></a>
**Topic 4: Senior Engineer Interview Questions**

**প্রশ্ন ১: Large team-এ Git workflow কীভাবে design করবেন?**
```
(Topic 2-এর system design answer দিন)
Key points: Branch strategy, protection rules, CI gates, CODEOWNERS,
commit standards, access control
```

**প্রশ্ন ২: Git history rewrite করার risks কী?**
```
git rebase, git reset --hard, git commit --amend, git filter-repo —
এগুলো history rewrite করে।

Risks:
- Pushed commits rewrite করলে team-এর সবার repo diverge হয়
- Force push দরকার হয় — অন্যদের local branch corrupted হতে পারে
- CI/CD pipeline-এ cached state invalid হয়

Safe rule: Never rewrite public/shared branch history.
Local, unpushed commits — যা খুশি করুন।
```

**প্রশ্ন ৩: Monorepo vs Polyrepo — কখন কোনটা?**
```
Monorepo:
+ Code sharing সহজ, atomic cross-project changes
+ Single CI/CD, consistent tooling
- Build complexity (affected packages only)
- Requires mature tooling (Nx, Bazel, Turborepo)

Polyrepo:
+ Team autonomy, simpler CI per repo
+ Clearer ownership
- Code sharing কঠিন (versioned packages দরকার)
- Cross-repo changes অনেক PRs

Decision: shared code অনেক → monorepo; independent services → polyrepo
```

**প্রশ্ন ৪: GitOps কী? কীভাবে implement করবেন?**
```
Git = single source of truth for infrastructure.
Desired state Git-এ থাকে। ArgoCD/Flux Git-এ watch করে,
cluster state align করে।

Benefits: audit trail, rollback via git revert, disaster recovery,
PR-based infra changes।

Implementation:
1. k8s manifests বা Helm charts একটি Git repo-তে
2. ArgoCD install → repo watch করে
3. Push to Git → auto sync to cluster
4. Manual change → auto revert (self-healing)
```

**প্রশ্ন ৫: CI/CD pipeline কীভাবে setup করবেন? Security কী কী দেখবেন?**
```
Stages:
PR: lint → unit test → security scan (CodeQL, Snyk)
Merge: integration test → staging deploy → smoke test
Tag/Release: production deploy → health check → notify

Security:
- Secrets never in code, always in GitHub Secrets
- Dependency scan (Dependabot + Snyk)
- SAST (CodeQL) on every PR
- Container scan (Trivy for Docker images)
- Least privilege: GITHUB_TOKEN minimal permissions
- Pin action versions (@v4, not @latest)
- Self-hosted runner isolation
```

---

<a id="p10-actions-qa"></a>
**Topic 5: GitHub Actions Interview Questions**

```
Q: GitHub Actions-এ Secrets কীভাবে pass করবেন?
A: Repository → Settings → Secrets-এ encrypted store করি।
   Workflow-এ: ${{ secrets.MY_SECRET }} দিয়ে access করি।
   Command args-এ নয়, env দিয়ে pass করি।

Q: Matrix build কখন ব্যবহার করবেন?
A: Multiple OS বা language version-এ same test চালাতে।
   strategy.matrix দিয়ে combinations define করি — parallel jobs।

Q: Job-এর মধ্যে data কীভাবে share করবেন?
A: Artifacts দিয়ে: upload-artifact → download-artifact।
   অথবা: outputs + needs.[job].outputs.value।

Q: GitHub Actions-এর free tier limit কী?
A: Public repo: unlimited।
   Private repo (free plan): 2000 min/month। Ubuntu runner।

Q: Self-hosted runner কখন দরকার?
A: Private network access, specific hardware (GPU), cost saving,
   custom software, faster machines।

Q: workflow_dispatch কী?
A: Manual trigger — GitHub UI বা gh CLI দিয়ে।
   Inputs define করা যায় (choice, boolean, string)।

Q: Reusable workflow কী? কীভাবে কাজ করে?
A: workflow_call trigger দিয়ে অন্য workflow থেকে call করা যায়।
   DRY principle — common CI steps একবার define।

Q: GITHUB_TOKEN কী?
A: Actions-এ automatically provided secret।
   Repository-র operations (PR comment, release create) করতে।
   Scope: current repository only।
```

---

<a id="p10-practical"></a>
**Topic 6: Practical Coding Test Tips**

**সাধারণ practical Git test-এ যা দেওয়া হয়:**

```bash
# Task 1: Feature branch তৈরি করুন
git checkout -b feature/your-name-test

# Task 2: File তৈরি করুন ও commit করুন
echo "Hello World" > hello.txt
git add hello.txt
git commit -m "feat: add hello.txt"

# Task 3: Commit message Conventional Commits format-এ
git commit -m "feat(greeting): add hello world file"

# Task 4: Branch-এ conflict তৈরি করে resolve করুন
# (interviewer দুটো branch-এ same file change করে দেবে)
git merge main
# Conflict resolve করুন
git add conflicted-file.txt
git commit -m "merge: resolve conflict in greeting"

# Task 5: Interactive rebase — 3টি commit squash করুন
git rebase -i HEAD~3
# squash/fixup দিয়ে একটিতে combine করুন

# Task 6: git log দিয়ে specific author-এর commits দেখুন
git log --author="Your Name" --oneline

# Task 7: .gitignore তৈরি করুন
echo "*.pyc\n.env\n__pycache__/" > .gitignore
git add .gitignore
git commit -m "chore: add .gitignore"
```

**Interview-এ কথা বলতে বলতে করুন:**
```
"এখন main থেকে একটি feature branch নিচ্ছি — কারণ main সবসময়
deployable রাখতে চাই। Branch-এ কাজ শেষে PR দেব।

Commit message Conventional Commits format-এ দিচ্ছি — feat:, fix:,
docs: ইত্যাদি। এতে CHANGELOG auto-generate করা যায়।

Conflict resolve করার সময় — আমি আগে দুটো version-ই পড়ি,
বুঝি কোনটা রাখা উচিত, তারপর markers সরাই।"
```

---

<a id="p10-reference"></a>
**Topic 7: Complete Git Command Quick Reference**

**Setup:**
```bash
git config --global user.name "Name"
git config --global user.email "email"
git config --global core.editor "code --wait"
git config --list
```

**Repository:**
```bash
git init                          # নতুন repo
git clone <url>                   # clone
git clone --depth=1 <url>         # shallow clone
git remote -v                     # remotes দেখুন
git remote add origin <url>       # remote add
git remote set-url origin <url>   # URL change
```

**Basic workflow:**
```bash
git status                        # অবস্থা দেখুন
git add .                         # সব stage করুন
git add -p                        # interactive staging
git commit -m "message"           # commit
git commit --amend                # last commit edit
git push origin branch            # push
git push -u origin branch         # push + upstream set
git pull                          # pull
git pull --rebase                 # pull with rebase
git fetch origin                  # fetch (no merge)
```

**Branch:**
```bash
git branch                        # list branches
git branch -a                     # remote সহ
git branch new-branch             # তৈরি করুন
git checkout new-branch           # switch
git switch new-branch             # modern switch
git checkout -b new-branch        # তৈরি + switch
git switch -c new-branch          # modern
git branch -d branch              # delete (merged)
git branch -D branch              # force delete
git push origin --delete branch   # remote delete
git branch -m old new             # rename
```

**Merge ও Rebase:**
```bash
git merge branch                  # merge
git merge --no-ff branch          # merge commit সবসময়
git merge --squash branch         # squash merge
git rebase main                   # rebase on main
git rebase -i HEAD~3              # interactive rebase
git rebase --continue             # conflict resolve-এর পরে
git rebase --abort                # rebase cancel
git cherry-pick abc1234           # specific commit
```

**Undo:**
```bash
git reset HEAD~1                  # last commit undo (mixed)
git reset --soft HEAD~1           # undo, changes staged
git reset --hard HEAD~1           # undo, changes deleted ⚠️
git revert abc1234                # safe undo (new commit)
git restore file.py               # working dir restore
git restore --staged file.py      # unstage
git stash                         # stash changes
git stash pop                     # stash apply + drop
git stash list                    # all stashes
git stash apply stash@{2}         # specific stash
git reflog                        # all HEAD movements
```

**Inspection:**
```bash
git log --oneline --graph --all   # visual log
git log -p                        # log with diff
git log --author="Name"           # by author
git log -S "string"               # code search
git log -- file.py                # file history
git diff                          # unstaged diff
git diff --staged                 # staged diff
git diff main..feature            # branch diff
git blame file.py                 # line-by-line author
git show abc1234                  # commit details
git bisect start/bad/good         # bug search
git grep "pattern"                # repo search
```

**Tag:**
```bash
git tag                           # list tags
git tag v1.0.0                    # lightweight tag
git tag -a v1.0.0 -m "message"   # annotated tag
git push origin --tags            # push all tags
git push origin v1.0.0            # push specific tag
git tag -d v1.0.0                 # delete local
git push origin --delete v1.0.0   # delete remote
```

**Stash:**
```bash
git stash push -m "description"   # named stash
git stash list                    # সব stash
git stash show stash@{0}          # stash content
git stash pop                     # apply + delete
git stash apply                   # apply, keep stash
git stash drop stash@{0}          # delete stash
git stash clear                   # সব delete ⚠️
git stash branch new-branch       # branch থেকে stash
```

**Advanced:**
```bash
git worktree add ../dir branch    # multiple workdirs
git submodule add <url> path      # submodule
git gc --aggressive               # garbage collection
git fsck --lost-found             # integrity check
git count-objects -v              # object stats
git filter-repo --path f --invert-paths  # history rewrite
git maintenance start             # auto maintenance
```

---

<a id="p10-cheatsheet"></a>
**Topic 8: One-Page Cheat Sheet**

**Daily workflow:**
```
সকালে: git pull --rebase origin main
কাজ: git checkout -b feature/task-name
     ... code করুন ...
     git add -p (selective)
     git commit -m "feat(scope): description"
শেষে: git push origin feature/task-name
      → GitHub-এ PR তৈরি করুন
Merge-এর পরে: git checkout main && git pull
```

**Emergency commands:**
```
হারানো commit  → git reflog → git reset --hard [hash]
Secret commit   → git rm --cached .env + filter-repo
Wrong branch    → git stash + git checkout correct-branch + git stash pop
Last commit fix → git commit --amend (push না হলে)
Production undo → git revert HEAD → git push
Detached HEAD   → git switch -c new-branch
Conflict        → edit + git add + git commit
```

**বড় পার্থক্য মনে রাখুন:**
```
merge vs rebase     → history vs linear
reset vs revert     → local vs safe (pushed)
fetch vs pull       → download vs download+merge
fork vs clone       → GitHub copy vs local copy
HEAD vs head        → current position vs latest commit (branch tip)
origin vs upstream  → your fork's remote vs original repo
```

**সংখ্যা মনে রাখুন:**
```
SHA-1 hash: 40 characters (7 = short)
reflog expires: 90 days (default)
gc threshold: 6700 loose objects
commit subject: ≤50 characters ideal, ≤72 max
body line wrap: 72 characters
```

---

**PART 10 Quick Revision Table**

| Scenario | সমাধান |
|---------|--------|
| Feature-এ কাজ, urgent hotfix | `git stash` → hotfix branch → fix → merge → `git stash pop` |
| Accidental push to main | `git revert HEAD` → push (team safe) |
| PR-এ conflict | `git rebase main` → resolve → push |
| Bug কোন commit-এ? | `git bisect start/bad/good` |
| কে লিখেছে এই line? | `git blame -L N,M file.py` |
| হারানো commit recover | `git reflog` → `git reset --hard [hash]` |
| .env committed | `git rm --cached .env` + filter-repo + revoke key |
| Release করতে হবে | tag → push --tags → gh release create |
| Messy commits clean করুন | `git rebase -i HEAD~N` → squash |
| Multiple branches একসাথে | `git worktree add ../dir branch` |

---

[⬆ শীর্ষে ফিরুন](#top)

---

> **✅ Git & GitHub Junior Engineer Handbook সম্পূর্ণ হয়েছে! PART 1–10 cover করা হয়েছে।**
