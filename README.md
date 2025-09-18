<!-- markdownlint-disable MD012 MD026 MD001 MD022 MD032 MD029 MD019 MD034 MD031 MD047 MD040 MD009 MD058 MD024 MD033 MD041 MD045 MD007 MD036 MD028  -->

<div>

 <img src="https://i.ibb.co.com/Z68g59hL/1-mtsk3f-Q-BRem-Fidhkel3d-A.png" style="width:100%; height:auto;">

</div>

## Git & GitHub

#### 🧩 Git

**Git** is a distributed **version control system (VCS)** created by Linus Torvalds (the creator of Linux) in 2005.

It allows developers to:

- Track changes in source code.
- Collaborate with others without overwriting work.
- Roll back to previous versions if needed.
- Work offline (local repository).

**🔑 Key Features of Git**

- **Distributed System** → Every developer has a full copy of the repository, including history.
- **Branching and Merging** → Work on features independently, then merge them back.
- **Staging Area** → Control what goes into the next commit.
- **Snapshots, not diffs** → Git saves a snapshot of the project at each commit.
- **Speed & Performance** → Lightweight and fast, even for large projects.

#### 🌐 GitHub

**GitHub** is a cloud-based hosting platform for Git repositories.

It provides:

- Remote storage for Git repositories.
- Collaboration tools (issues, pull requests, discussions).
- CI/CD integration (GitHub Actions).
- Project management features (kanban boards, milestones).
- Social coding (followers, stars, forks).

#### 📊 Difference Between Git and GitHub

| Feature              | **Git** (Tool) | **GitHub** (Platform) |
|----------------------|----------------|------------------------|
| **Definition**       | A distributed version control system (software). | A cloud-based hosting service for Git repositories. |
| **Type**             | Command-line tool (runs locally on your computer). | Web-based platform (runs online, requires internet). |
| **Usage**            | Tracks changes, manages versions, and branches locally. | Stores repositories remotely, enables collaboration and sharing. |
| **Offline/Online**   | Works offline. | Requires internet to access repos. |
| **Ownership**        | Open-source, developed by Linus Torvalds. | Owned by Microsoft (since 2018). |
| **Authentication**   | No account needed (local use). | Requires account to host/share repos. |
| **Collaboration**    | Limited to your local machine unless you push to a shared repo. | Rich collaboration: pull requests, code reviews, issues, discussions. |
| **Alternatives**     | None (Git is the underlying system). | GitLab, Bitbucket, Azure Repos (all Git hosting platforms). |


### Version Control System (VCS)

A Version Control System (VCS) is a tool/software that helps developers track, manage, and control changes to source code (or any files) over time.

It allows you to:

- Keep a history of changes.
- Work on projects with multiple people simultaneously.
- Roll back to previous versions if something breaks.
- Experiment with new features safely using branches.

👉 In simple words: VCS is like a time machine + collaboration tool for code.

**🔑 Key Features of VCS**

1. **Track Changes** → Every modification (who, when, what) is recorded.
2. **Collaboration** → Multiple developers can work together without overwriting each other’s work.
3. **Branching and Merging** → Create isolated versions of code (branches) and later merge them.
4. **Backup & Recovery** → Since changes are stored, you can recover previous versions.
5. **Audit Trail** → Helps see who made specific changes (important in professional teams).


#### 🛠️ Types of Version Control Systems

**1. Local VCS**

- All versions stored on a developer’s local machine.
- Example: RCS (Revision Control System).
- ❌ Limitation: No collaboration support.

**2. Centralized VCS (CVCS)**

- A single central server stores all files.
- Developers check in/out files from the server.
- Examples: Subversion (SVN), CVS.
- ✅ Easier collaboration.
- ❌ If server crashes, you lose everything.

**3. Distributed VCS (DVCS)**

- Every developer has a full copy of the repository (including history).
- Collaboration happens by pushing/pulling changes between repos.
- Examples: Git, Mercurial.
- ✅ Faster, offline work possible, safer backups.
- ❌ Slightly more complex for beginners.


### 📂 Repository in Git

A Git repository (repo) is a storage space where Git tracks your project files and their history.

It contains:

- Project files (source code, documentation, etc.).
- The entire version history (commits, branches, tags).
- Git configuration (remote URLs, settings).

👉 Think of a repository as a project folder + history of everything that ever happened in it.

#### 📂 Types of Git Repositories

**1. Local Repository**

- Exists on your computer.
- Created using:
```bash
git init
```
- Stores files + Git history inside the hidden `.git` folder.
- Can work offline.
- Use commands like `git add`, `git commit`, `git log` to manage it.

**2. Remote Repository**

- Hosted on a server (e.g., GitHub, GitLab, Bitbucket).
- Allows collaboration with others.
- Created by pushing a local repo to a remote server or cloning an existing remote repo.
- Use commands like `git push`, `git pull`, `git clone` to interact with it.
- Requires internet access.
- Example:
```bash
git clone
git push origin main
git pull origin main
```

### `origin` in Git

In Git, `origin` is the default name given to the remote repository when clone a project or add a new remote.

- It’s basically an alias (shortcut) for the remote repo URL (e.g., GitHub, GitLab, Bitbucket).
- Instead of typing the long repo URL every time, just use `origin`.

**📌 Example 1: Cloning a Repository**

When clone a repo from GitHub:
```bash
git clone https://github.com/user/project.git
```

Git automatically creates a remote named `origin` that points to:
```arduino
https://github.com/user/project.git
```

Check it with:
```bash
git remote -v
```

**✅ Output:**
```perl
origin  https://github.com/user/project.git (fetch)
origin  https://github.com/user/project.git (push)
```

**📌 Example 2: Adding origin Manually**

If create a local repo with git init, later connect it to a remote:
```bash
git remote add origin https://github.com/user/project.git
```

Now `origin` = shortcut for that URL.

When push code:
```bash
git push origin main
```

> This means → Push the `main` branch to the repo located at `origin`.

### 📂 `.gitignore` file in Git

The `.gitignore` file tells Git which files or folders it should ignore (not track) in a repository.

- It prevents unnecessary, sensitive, or temporary files from being committed.
- Each line in `.gitignore` specifies a pattern of files/folders to exclude.

👉 Think of it as a filter that says:
“Hey Git, don’t bother tracking these files.”

**📌 Why Do Need `.gitignore`**

- Avoid cluttering your repo with files that are auto-generated or not useful to others.
- Protect sensitive info like API keys or passwords.
- Prevent OS or editor-specific junk files from being shared.

**📌 Common Files/Folders to Ignore**

- `node_modules/` → For Node.js projects (dependencies).
- `*.log` → Log files.
- `*.env` → Environment variable files (sensitive info).
- `dist/` or `build/` → Compiled output folders.
- `.DS_Store` → macOS system files.
- `Thumbs.db` → Windows system files.
- `.vscode/` → VSCode settings folder.
- `*.class` → Compiled Java files.
- `*.pyc` → Compiled Python files.
- `*.swp` → Vim swap files.
- `*.exe` → Executable files.
- `*.zip` or `*.tar.gz` → Compressed files.
- `*.iml` → IntelliJ IDEA project files.
- `*.out` → Compiled output files.
- `*.o` or `*.obj` → Compiled object files.
- `*.bak` → Backup files.
- `*.tmp` → Temporary files.
- `*.cache` → Cache files.
- `*.dll` or `*.so` → Dynamic libraries.

**📌 Important Notes**

- `.gitignore` only works on untracked files.
If a file is already tracked, Git will continue tracking it unless you remove it first:
```bash
git rm --cached filename
```

- can have global .gitignore (for all repos on your system):
```bash
git config --global core.excludesfile ~/.gitignore_global
```

