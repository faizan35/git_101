# Module 0 — Orientation & Setup

## 0.1 What is Git? Install & verify

**What to know (interview):**

- Git is a **distributed** VCS: every clone is a full repo (history + refs).
- Git stores **snapshots** of files as **content-addressed objects** (not line deltas conceptually).
- “Commit = snapshot + metadata + parent pointers.”

**Commands:**

```bash
git --version                         # verify
# Windows: install “Git for Windows” (includes Git Bash, GCM)
# macOS: brew install git
# Linux: apt-get install git  |  dnf install git
```

**Gotchas:** corporate proxies can break install/update; ensure PATH points to the Git you expect (`where git` / `which git`).

## 0.2 Global config (identity, defaults, pager, aliases)

**What to know (interview):**

- Config has **scopes**: system → global → local; local overrides global.
- Set identity once per machine; set a sensible default branch name; choose an editor that **waits**.

**Commands:**

```bash
# Identity
git config --global user.name  "Faizan Ansari"
git config --global user.email "faizanansari4862@gmail.com"

# Default initial branch (new repos)
git config --global init.defaultBranch main

# Editor (VS Code waits until you close)
git config --global core.editor "code --wait"

# Pager (plain 'less' is fine; upgrade later to 'delta' if you like)
git config --global core.pager "less -+F -+X"

# Useful aliases
git config --global alias.st "status -sb"
git config --global alias.lg "log --graph --decorate --oneline --all"
git config --global alias.co "checkout"
git config --global alias.br "branch"
git config --global alias.ci "commit"
```

**Gotchas:** if `code --wait` doesn’t work, VS Code isn’t on PATH; use `notepad` (Win) or `nano -w` (Unix) temporarily.

## 0.3 Mental model: Working tree vs Index vs HEAD

**What to know (interview):**

- **Working tree (WT):** your files on disk.
- **Index/staging area:** the _next_ commit’s contents.
- **HEAD:** the current commit (usually “the tip of your branch”).
- Flow: **edit → stage (`git add`) → commit (`git commit`)**.
- Detached HEAD = HEAD points directly to a commit, not a branch ref.

**Commands (to see states):**

```bash
git status                   # WT ↔ Index differences
git diff                     # WT vs Index
git diff --staged            # Index vs HEAD (what you’ll commit)
git show HEAD                # inspect current commit
```

**Gotchas:** editing after staging means the staged version and WT can differ—commit won’t include post-stage edits unless you re-add.

## 0.4 First repo: init/clone, remotes, fetch vs pull, push

**What to know (interview):**

- `git init` creates `.git/` and your default branch.
- `git clone` sets `origin` remote and a tracking branch.
- **fetch** = download refs/objects; **pull** = fetch + merge (or rebase, if configured).
- First push: `-u` sets upstream so later `git push` knows where.

**Commands:**

```bash
# Start from scratch
mkdir demo && cd demo
git init
echo "hello" > README.md
git add README.md
git commit -m "feat: initial commit"

# Attach a remote (replace URL)
git remote add origin https://github.com/you/demo.git
git push -u origin main

# From existing repo on server
git clone https://github.com/you/demo.git
cd demo
git fetch --all --prune
git pull --ff-only
```

**Optional defaults for cleaner pulls (pick one policy):**

```bash
# Prefer fast-forward or fail
git config --global pull.ff only

# OR prefer rebasing your local commits on top of remote
git config --global pull.rebase true
```

**Gotchas:** `pull --ff-only` fails if you have local commits diverged from remote; resolve via `git pull --rebase` or a manual rebase.

## 0.5 Editor / diff & merge tools

**What to know (interview):**

- Git can launch your editor for commit messages and tools for diffs/merges.
- You can standardize team UX with a common tool (VS Code, vimdiff, etc.).

**Commands (VS Code examples):**

```bash
# Editor already set in 0.2
git config --global diff.tool vscode
git config --global difftool.vscode.cmd "code --wait --diff \"$LOCAL\" \"$REMOTE\""

git config --global merge.tool vscode
git config --global mergetool.vscode.cmd \
"code --wait \"$MERGED\""

# Use them
git difftool
git mergetool
```

**Gotchas:** mergetool integrates with conflict markers; always stage resolved hunks then `git merge --continue` (or `rebase --continue`).

## 0.6 Credential management: helpers, SSH vs HTTPS

**What to know (interview):**

- HTTPS pushes use a **credential helper** (stores PAT/tokens securely).
- SSH uses **key pairs**; no password per push; good for 2FA environments.
- Windows: **Git Credential Manager** (GCM) is bundled; macOS: `osxkeychain`; Linux: `libsecret`.

**Setup (HTTPS helper):**

```bash
# Windows (GCM installed by default)
git config --global credential.helper manager

# macOS
git config --global credential.helper osxkeychain

# Linux (libsecret; ensure package installed)
git config --global credential.helper libsecret
```

**Setup (SSH keys):**

```bash
ssh-keygen -t ed25519 -C "faizanansari4862@gmail.com"
# Press enter to accept default path; add a passphrase if allowed.
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# Copy public key and add to Git hosting (GitHub/GitLab/Bitbucket)
cat ~/.ssh/id_ed25519.pub
```

**Gotchas:** old RSA keys may be rejected on strict hosts; prefer **ed25519**. On Windows, ensure the **OpenSSH Authentication Agent** service is running if keys don’t load.

## 0.7 Repo layout basics: `.git/` at a glance

**What to know (interview):**

- `.git/HEAD` → points to your current ref (e.g., `refs/heads/main`).
- `.git/refs/` → branch/tag pointers (sometimes packed in `packed-refs`).
- `.git/objects/` → all blobs/trees/commits/tags.
- `.git/index` → the staging area (binary file).
- `.git/config` → repo-local config; overrides global.
- `.git/hooks/` → sample hook scripts (disabled by default).
- `.git/logs/` → reflogs (how `git reflog` knows history of refs).

**Commands (peek safely):**

```bash
cat .git/HEAD
git rev-parse --abbrev-ref HEAD
git show-ref --heads --tags
git cat-file -p HEAD            # pretty-print the HEAD commit object
```

**Gotchas:** don’t hand-edit files under `.git/` unless you know exactly what you’re doing; use porcelain/plumbing commands instead.
