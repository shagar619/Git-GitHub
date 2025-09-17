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