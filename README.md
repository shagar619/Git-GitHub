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


### 🚀 Git Commands

**🔧 Setup & config**
`git config` — configure Git behavior (global or repo-level).
```bash
# set name/email (global)
git config --global user.name "Your Name"
git config --global user.email "you@company.com"

# set editor, default branch name
git config --global core.editor "code --wait"
git config --global init.defaultBranch main

# show configuration
git config --list
```

**📁 Create & clone repositories**
```bash
# initialize a new repo (local)
git init               # creates .git folder

# clone remote repository (creates local copy)
git clone https://github.com/org/repo.git
# clone into specific directory
git clone <url> my-repo
```

> `git clone` over SSH use `git@github.com:org/repo.git`.

**📊 Status / inspection**
```bash
git status             # what changed / staged / untracked
git diff               # unstaged changes (working -> index)
git diff --staged      # staged changes (index -> HEAD)
git diff HEAD          # difference between working tree and HEAD
git ls-files           # list tracked files
git show <commit>      # show a commit details (message + diff)
git --no-pager log --oneline --graph --all  # compact commit graph
git log                # detailed history
git log --stat         # files changed summary
git blame path/file    # who last changed each line
git shortlog -sne      # contributor summary
```

Example:
```bash
git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short -n 15
```

**➕ Staging & committing**
```bash
git branch                    # list branches (local)
git branch -a                 # list all (including remotes)
git branch feature/awesome    # create branch (no checkout)
git checkout feature/awesome  # old: switch to branch
# modern commands:
git switch -c feature/awesome # create and switch
git switch feature/awesome    # switch to existing branch
```

Example workflow:
```bash
git switch -c feature/login   # create a feature branch
# do work...
git add .
git commit -m "feat(login): implement API integration"
```

**🔗 Merging, rebasing & integrating**

Merge (preserve history):
```bash
git switch main
git pull origin main
git merge feature/login       # merges feature into main (creates merge commit)
```

Fast-forward only:
```bash
git merge --ff-only feature/login
```

Rebase (linearize history):
```bash
git switch feature/login
git fetch origin
git rebase origin/main        # reapply commits onto latest main
# resolve conflicts if any, then:
git rebase --continue
# push (force-with-lease recommended after rebase)
git push --force-with-lease origin feature/login
```

When to use:

- Use merge for public branches (preserves merge structure).
- Use rebase for local cleanup or to keep a feature branch up-to-date before PR — but do not rebase published commits unless everyone agrees.

Interactive rebase (squash/modify history):
```bash
git rebase -i HEAD~5  # edit last 5 commits (squash, fixup, reorder)
```

**🔁 Pull & fetch**
```bash
git fetch origin               # download objects and refs (does not change working tree)
git pull                       # fetch + merge (default)
git pull --rebase              # fetch + rebase (common in feature workflows)
```

> `git fetch` + inspect (`git log origin/main..HEAD`) before merging/pulling in critical workflows.


**📤 Push & remotes**
```bash
git remote -v         # list remotes
git remote add origin git@github.com:org/repo.git
git push -u origin main     # first push: set upstream
git push origin feature/branch
git push --delete origin old-branch   # delete remote branch
git push --force-with-lease origin feature/branch # safer force push
```

> `--force-with-lease` is preferred over `--force` as it's safer (fails if remote changed).

**🔄 Undoing changes (safety first)**

Unstage, restore, remove:
```bash
git restore file.txt                 # restore file from HEAD to working tree (newer command)
git restore --staged file.txt        # unstage file (remove from index)
# older equivalents:
git reset HEAD file.txt              # unstage
git checkout -- file.txt             # restore (older legacy)
```

Undo commits (local only):
```bash
git reset --soft HEAD^    # move HEAD back, keep changes in index (undo commit, keep staged)
git reset --mixed HEAD^   # default: undo commit, unstages changes (keeps working tree)
git reset --hard HEAD^    # WARNING: remove commit and working changes (destructive)
```

Revert (safe for public history):
```bash
git revert <commit>   # create a new commit that undoes <commit>
```

> Use `revert` when you need to undo a commit that has already been pushed/shared.


**🧰 Stash — temporary shelve work**
```bash
git stash                 # stash staged + unstaged changes
git stash push -m "WIP login feature"   # better: name stash
git stash list
git stash apply stash@{0} # reapply stash but keep it
git stash pop             # reapply and drop stash
git stash drop stash@{0}
git stash branch wip/stash stash@{0}  # create branch from stash
```

> Use case: quick context switch when you need a clean working tree.

**🕵️ Viewing & searching history**
```bash
git log --oneline --graph --decorate --all
git log -p -S "functionName"      # search patch for text
git log --author="Alice"          # commits by author
git grep "TODO"                   # search working tree
git bisect start
git bisect bad HEAD
git bisect good v1.2.0            # find commit that introduced a bug (binary search)
```

> `git bisect` is invaluable in large repos to find the commit that broke behavior.

**🧩 Tags & releases**
```bash
git tag                     # list tags
git tag -a v1.2.0 -m "Release 1.2.0"   # annotated tag
git push origin v1.2.0
git push --tags             # push all tags
git describe --tags          # show nearest tag for current commit
```

**🧾 Patches & emailing**
```bash
git format-patch -n <base>   # generate patch files between base..HEAD
git am <patchfile>           # apply mailbox patches
git apply <patch.diff>       # apply patch file
```

**🔍 Recovery & rewriting history**

Reflog — recover lost commits:
```bash
git reflog                 # show HEAD history (even after reset)
git checkout -b rescue HEAD@{3}   # create branch from an older HEAD
```

Reset vs Revert (summary):

- `git reset` rewrites local history (moves HEAD). Use locally, be cautious if pushed.
- `git revert` creates a new commit that undoes a past commit — safe for shared history.

Filter-branch / filter-repo (history rewrite):

- `git filter-repo` (preferred current tool) or older `git filter-branch` can rewrite history to remove sensitive data (e.g., accidental secrets). This requires force-pushing and coordinating with team.


**🧩 Cherry-pick**
```bash
git cherry-pick <commit>         # apply changes from a commit onto current branch
git cherry-pick -x <commit>      # record original commit reference (-x)
```

**🧪 Debugging tools**
```bash
git bisect                     # find commit introducing bug using binary search
git blame file                  # see who changed each line
git diff --name-only HEAD~1..HEAD  # list files changed between revisions
```

**📦 Submodules, subtrees & worktrees**

Submodule (link to another Git repo inside your repo):
```bash
git submodule add git@github.com:org/lib.git libs/lib
git submodule update --init --recursive
git submodule status
```

Worktree (multiple working directories from same repo):
```bash
git worktree add ../feature-2 feature/branch
# now you can work on two branches simultaneously in separate folders
```

> Subtree is alternative to submodule — consider depending on needs.

**🧰 Maintenance & housekeeping**
```bash
git gc --aggressive --prune=now   # garbage collect (cleanup)
git fsck                          # check repository integrity
git prune                         # remove unreachable objects
```

**🛡 Security: signing commits & tags**
```bash
# enable signing
git config --global user.signingkey <GPG-key-id>
git config --global commit.gpgSign true

# sign a tag
git tag -s v1.2.0 -m "Signed release"
```

**🧩 Misc useful commands**
```bash
git archive --format=tar --output=../repo.tar HEAD   # export snapshot
git bundle create repo.bundle --all                  # portable pack of a repo
git restore --source=HEAD~1 -- path/file              # restore a file from earlier commit
git credential-cache                                 # credential helper usage
git help <command>                                   # open built-in help
```



#### 🧭 Collaboration workflows (practical examples)

**Feature branch + PR workflow**
```bash
# local
git switch -c feature/awesome
# work, commit...
git push -u origin feature/awesome
# open Pull Request on GitHub, request review

# after merge to main via PR:
git switch main
git pull origin main
git branch -d feature/awesome        # delete local branch (if merged)
git push origin --delete feature/awesome # delete remote branch
```

**Hotfix to production (safe)**
```bash
git switch main
git pull origin main
git switch -c hotfix/typo
# fix and commit
git push origin hotfix/typo
# open PR, merge to main, then cherry-pick or merge to develop if needed
```


**Fork + PR workflow (open source)**
```bash
# fork repo on GitHub
git clone
git remote add upstream
git fetch upstream
git switch main
git merge upstream/main
git switch -c feature/awesome
# work, commit...
git push -u origin feature/awesome
# open Pull Request from your fork to original repo
```

**Rebase feature branch onto updated main**
```bash
git switch feature/awesome
git fetch origin
git rebase origin/main
# resolve conflicts if any
git rebase --continue
git push --force-with-lease origin feature/awesome
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
git init
git remote add origin https://github.com/user/project.git
git push -u origin main
```

Now `origin` = shortcut for that URL.

When push code:
```bash
git push origin main
```

> This means → Push the `main` branch to the repo located at `origin`.


**📊 Difference Between origin and upstream**
| Feature              | **origin** (Your Remote) | **upstream** (Original Repo) |
|----------------------|--------------------------|------------------------------|
| **Definition**       | Your forked copy of the repository. | The original repository you forked from. |
| **Usage**            | Push your changes here. | Fetch updates from here. |
| **Common Commands**  | `git push origin main`   | `git fetch upstream`         |
| **Purpose**          | Share your work.         | Stay updated with original project. |


### `git status` command

The `git status` command is one of the most frequently used commands in Git. It provides a summary of the current state of the working directory and the staging area.

When you run `git status`, it shows:
1. **Current Branch** → Which branch you are on.
2. **Changes to be committed** → Files that are staged and ready to be committed.
3. **Changes not staged for commit** → Files that have been modified but not yet staged.
4. **Untracked files** → New files that are not being tracked by Git.
5. **Instructions** → Suggestions on what commands to run next.

**📌 Example Output of `git status`**
```perl
On branch main
Your branch is up to date with 'origin/main'.
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   file1.txt
        new file:   file2.txt
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
            modified:   file3.txt
Untracked files:
(use "git add <file>..." to include in what will be committed)
        file4.txt
nothing added to commit but untracked files present (use "git add" to track)
```

### `git clean` command

The `git clean` command is used to remove untracked files and directories from your working directory. It helps keep your workspace clean by getting rid of files that are not being tracked by Git.
**⚠️ Warning:** `git clean` is a destructive operation. Once files are deleted, they cannot be easily recovered. Always use the `-n` (dry run) option first to see what will be deleted.

**📌 Common Options for `git clean`**

- `-n` or `--dry-run` → Show what would be deleted without actually deleting anything.
- `-f` or `--force` → Force the deletion of untracked files.
- `-d` → Remove untracked directories in addition to untracked files.
- `-x` → Remove all untracked files, including those ignored by `.gitignore`.
- `-X` → Remove only files ignored by `.gitignore`.

**📌 Example Usage of `git clean`**
```bash
# Show what would be deleted (dry run)
git clean -n
# Remove untracked files (force)
git clean -f
# Remove untracked files and directories (force)
git clean -fd
# Remove all untracked files, including ignored ones (force)
git clean -fx
# Remove only ignored files (force)
git clean -fX
```

### `git reset` command

The `git reset` command is used to undo changes in your Git repository. It can modify the state of the staging area (index) and the working directory, depending on the options you use.

**📌 Common Options for `git reset`**

```bash
# Soft reset (keep changes in working directory)
git reset --soft HEAD~1

# Mixed reset (keep changes in working directory, unstage them)
git reset --mixed HEAD~1

# Hard reset (discard all changes)
git reset --hard HEAD~1
```
- `--soft` → Moves the HEAD pointer to a specified commit but leaves the staging area and working directory unchanged. This is useful for undoing a commit while keeping your changes staged.
- `--mixed` (default) → Moves the HEAD pointer and updates the staging area to match the specified commit, but leaves the working directory unchanged. This unstages any changes that were previously staged.
- `--hard` → Moves the HEAD pointer, updates the staging area, and resets the working directory to match the specified commit. This discards all changes in the working directory and staging area.


### 'Index' in git

In Git, the "index" (also known as the "staging area") is an intermediate area where changes are gathered before they are committed to the repository. It acts as a buffer between the working directory (where you make changes) and the repository (where commits are stored).

When you modify files in your working directory, those changes are not automatically included in the next commit. Instead, you need to explicitly add them to the index using the `git add` command. Once changes are staged in the index, they are ready to be committed with `git commit`.

**📌 Key Points about the Index**

1. **Staging Area** → The index holds a snapshot of the changes you want to include in the next commit.
2. **Selective Staging** → You can choose which changes to stage, allowing for more granular commits.
3. **Temporary Storage** → The index is a temporary area; changes in the index are not permanent until committed.
4. **File States** → Files can be in one of three states: untracked, modified (unstaged), or staged (in the index).
5. **Commands** → Common commands that interact with the index include:
   - `git add <file>` → Stage changes to the index.
   - `git reset <file>` → Unstage changes from the index.
   - `git commit` → Commit staged changes from the index to the repository.

**📌 Example Workflow with the Index**

1. Make changes to a file in your working directory.
2. Stage the changes using `git add <file>`.
3. Check the status with `git status` to see the staged changes.
4. Commit the changes with `git commit -m "Your commit message"`.
5. The changes are now permanently recorded in the repository.


### `git checkout` command

The `git checkout` command is used to switch between branches or restore files in your working directory. It allows you to navigate through different branches of your repository and manage the state of your files.

**📌 Common Uses of `git checkout`**

1. **Switching Branches** → Change the current branch to another branch.
```bash
git checkout feature-branch
```

2. **Creating and Switching to a New Branch** → Create a new branch and switch to it in one command.
```bash
git checkout -b new-feature
```

3. **Restoring Files** → Restore a file in your working directory to match the version in the index or a specific commit.
```bash
git checkout -- file.txt          # restore from index
git checkout <commit> -- file.txt  # restore from specific commit
```

4. **Checkout a Specific Commit** → Switch to a specific commit by its hash.
```bash
git checkout <commit-hash>
```

**📌 Important Notes**

- When switching branches, any uncommitted changes in your working directory may be lost if they conflict with the target branch. Use `git stash` to save changes temporarily if needed.
- The `git checkout` command has been partially replaced by `git switch` (for switching branches) and `git restore` (for restoring files) in newer versions of Git for better clarity.

### `git switch` command

The `git switch` command is a more user-friendly way to switch between branches in Git. It was introduced in Git 2.23 as part of an effort to simplify the user experience by separating branch switching from file restoration, which was previously handled by the `git checkout` command.

**📌 Common Uses of `git switch`**

1. **Switching to an Existing Branch** → Change the current branch to another existing branch.
```bash
git switch feature-branch
```

2. **Creating and Switching to a New Branch** → Create a new branch and switch to it in one command.
```bash
git switch -c new-feature
```

3. **Switching to a Specific Commit** → Switch to a specific commit by its hash (detached HEAD state).
```bash
git switch --detach <commit-hash>
```

**📌 Important Notes**

- `git switch` is focused solely on branch management, making it clearer and easier to use than `git checkout` for this purpose.
- For restoring files, use the `git restore` command instead.

### `git restore` command

The `git restore` command is used to restore files in your working directory to a previous state. It was introduced in Git 2.23 to provide a clearer and more focused way to handle file restoration, separating this functionality from the `git checkout` command.

**📌 Common Uses of `git restore`**

1. **Restoring a File from the Index** → Restore a file in your working directory to match the version in the index (staging area).
```bash
git restore file.txt
```

2. **Restoring a File from a Specific Commit** → Restore a file to the state it was in at a specific commit.
```bash
git restore --source=<commit-hash> -- file.txt
```

3. **Unstaging a File** → Remove a file from the staging area (index) without changing the working directory.
```bash
git restore --staged file.txt
```

4. **Restoring All Files** → Restore all files in the working directory to match the index.
```bash
git restore .
```

**📌 Important Notes**

- `git restore` is focused solely on file restoration, making it clearer and easier to use than `git checkout` for this purpose.
- Always be cautious when using `git restore`, as it can overwrite changes in your working directory. Use `git status` to check the state of your files before restoring.


