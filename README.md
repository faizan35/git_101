# Git Mastery

## [Module 0 — Orientation & Setup](./00_Orientation_and_Setup.md)

**0.1** What is Git? Install Git; verify with `git --version`
**0.2** Global config: `user.name`, `user.email`, `init.defaultBranch`, pager, aliases
**0.3** Mental model: Working tree vs Index (staging) vs HEAD
**0.4** First repo: `git init`, `git clone`, `remote add`, `fetch` vs `pull`, `push`
**0.5** Editor/merge tool: `core.editor`, `merge.tool`, `difftool`
**0.6** Credential management: credential helpers (manager/libsecret), SSH vs HTTPS
**0.7** Repo layout basics: `.git/` overview (high level)

## Module 1 — Everyday Git

**1.1** Status, add, commit: `status`, `add -p`, `commit -m/-v`
**1.2** Viewing changes: `diff` (WT↔Index, Index↔HEAD), `show`
**1.3** Ignore rules: `.gitignore` vs `.git/info/exclude`
**1.4** History quick view: `log --oneline --graph --decorate --all`
**1.5** Remotes & tracking: `remote -v`, `push -u`, upstream branches
**1.6** Safe pulls: `pull --ff-only` and when FF fails
**1.7** File rename/move awareness: `mv`, detection in diffs/logs

## Module 2 — Branching & Merging

**2.1** Branch lifecycle: `branch`, `switch`/`checkout -b`, set upstream
**2.2** Merge types: fast-forward vs 3-way; `--no-ff` semantics
**2.3** Conflict resolution flow: conflict markers → stage → `merge --continue`
**2.4** `rerere` basics (reuse recorded conflict resolutions)
**2.5** Feature branch hygiene and deletion (`-d`/`-D`)
**2.6** Strategies for small, reviewable PRs

## Module 3 — Rebase & History Crafting

**3.1** Rebase fundamentals: `rebase main` to linearize feature work
**3.2** Interactive rebase: `rebase -i` with `reword/edit/squash/fixup/exec`
**3.3** Autosquash: `fixup!`/`squash!` messages and `--autosquash`
**3.4** Rebase vs merge: trade-offs, policy guidance
**3.5** Public vs private history: when **not** to rebase
**3.6** Handling rebase conflicts & continuing/aborting

## Module 4 — Undo, Restore & Recovery

**4.1** Working tree fixes: `restore` (and legacy `checkout --`)
**4.2** Staging fixes: `restore --staged`, `reset HEAD <path>`
**4.3** Amend last commit: `commit --amend` (message vs content)
**4.4** Safe undo: `revert` (including reverting merges)
**4.5** `reset` modes: `--soft`, `--mixed` (default), `--hard`
**4.6** Reflog rescue: `reflog`, `rev-parse` to recover lost commits
**4.7** Deleted branch recovery & `fsck --lost-found`

## Module 5 — Search, Inspect & Debug

**5.1** Blame/annotate: `blame`, `-L`, ignore-rev lists for refactors
**5.2** Powerful log queries: `--grep`, `-S` (pickaxe), `-G`, `--since/--until`
**5.3** Diff mastery: `--word-diff`, `--color-moved`, rename `-M`, copy `-C`
**5.4** Bisect workflow: `bisect start/good/bad/reset`
**5.5** Inspect a commit: `show`, `cat-file -p` (peek objects)
**5.6** Tracing specific file history across renames

## Module 6 — Collaboration & Code Review

**6.1** Fork vs single-repo models; upstream remotes
**6.2** Syncing & pruning: `fetch --prune`, branch cleanup
**6.3** PR/MR etiquette: small diffs, rebasing before open, drafts
**6.4** Merge strategies in platforms: merge commit, squash, rebase-merge
**6.5** Branch protection rules: reviews, checks, linear history
**6.6** Project scaffolding: PR/Issue templates, `CODEOWNERS`

## Module 7 — Commit Messages & Release Tags

**7.1** Crafting good messages (subject/body, imperative mood)
**7.2** Conventional Commits: types, scopes, BREAKING CHANGE
**7.3** Tags: lightweight vs annotated (`-a`), signed tags
**7.4** SemVer alignment; `git describe` for build metadata
**7.5** Generating release notes from commit conventions

## Module 8 — Config, Attributes & Line Endings

**8.1** Config scopes: system/global/local; conditional includes
**8.2** `.gitattributes`: EOL (`* text=auto`), binary hints, diff/merge drivers
**8.3** Cross-OS line endings: `core.autocrlf`, `.editorconfig` interplay
**8.4** Clean/smudge filters (formatters, normalizers)
**8.5** Linguist overrides (language stats) awareness

## Module 9 — Advanced Object Model (Plumbing)

**9.1** Objects: blob, tree, commit, tag; content-addressing (SHA-1/SHA-256)
**9.2** Walking objects: `ls-tree`, `cat-file -p`, parents, trees
**9.3** Creating objects: `hash-object`, writing trees/commits (concept)
**9.4** Refs: `for-each-ref`, `update-ref`, `show-ref`
**9.5** Revision syntax: `^`, `~`, ranges `A..B` vs `A...B`, pathspecs
**9.6** Packs & maintenance: loose vs packfiles, `gc`, `repack`, `prune`

## Module 10 — Performance, Scale & Large Repos

**10.1** Shallow clones: `--depth`, pitfalls and updates
**10.2** Partial clone: `--filter=blob:none`, promisor remotes (overview)
**10.3** Sparse-checkout: cone mode, focus folders
**10.4** Monorepo onboarding speed-ups (combine 10.2 + 10.3)
**10.5** Server/protocol v2 awareness; negotiation basics
**10.6** Hygiene: removing big binaries; path/depth limits

## Module 11 — Submodules, Subtrees & LFS

**11.1** Submodules: `submodule add/init/update`, pinning SHAs
**11.2** Submodule pitfalls: nested updates, CI cloning, `--recursive`
**11.3** Subtree merges: vendor code without submodule UX
**11.4** Choosing submodule vs subtree vs package managers
**11.5** Git LFS: when to use, quotas, CI caching
**11.6** Migrating existing binaries to LFS

## Module 12 — Hooks, Signing & Compliance

**12.1** Client hooks: `pre-commit`, `commit-msg`, `pre-push`
**12.2** Centralizing hooks with frameworks (e.g., pre-commit)
**12.3** Commit signing: GPG vs SSH signatures; verifying in platforms
**12.4** Policies: branch names, message linting, size limits
**12.5** DCO vs CLA; provenance/audit trail basics

## Module 13 — GitHub/GitLab/Bitbucket Ecosystem

**13.1** Branch protection & required checks; auto-merge options
**13.2** CI basics: gating PRs, caching dependency layers
**13.3** Security: Dependabot/Renovate, secret scanning
**13.4** Repo hygiene: default branch, templates, labels, Discussions
**13.5** Environments & deployment gates (high level)

## Module 14 — Release & Deployment Workflows

**14.1** Branching models: Trunk-based, GitFlow, Release branches (pros/cons)
**14.2** Cutting releases: cut branch, tag, build metadata
**14.3** Hotfix flow: cherry-pick to release, backports to main
**14.4** Changelogs: auto-generate from Conventional Commits
**14.5** Deploying by tag vs by SHA; rollback strategy

## Module 15 — Monorepo Strategy (Advanced)

**15.1** Repo structure: ownership boundaries, shared libs
**15.2** Selective builds: `git diff --name-only` for CI scoping
**15.3** Worktrees + sparse-checkout for focused development
**15.4** Versioning models: single vs independent; release orchestration
**15.5** Preventing cross-team contention (policies & tooling)

## Module 16 — Worktrees, Stash & Power Workflows

**16.1** Multiple worktrees: `worktree add/list/prune`, parallel PRs
**16.2** Stash patterns: `stash push -p`, named stashes, apply vs pop
**16.3** Advanced difftool/mergetool setup; custom drivers
**16.4** Useful aliases: `lg`, `wip`, `undo`, scripted helpers

## Module 17 — History Rewriting & Repo Surgery

**17.1** `git filter-repo` (preferred): remove paths/secrets, rewrite emails
**17.2** BFG Repo-Cleaner (contrast & limitations)
**17.3** Root squashes; `subtree split` to extract components
**17.4** Coordination & safety when rewriting shared history
**17.5** Post-rewrite validation & remote force-push etiquette

## Module 18 — Troubleshooting & Disaster Recovery

**18.1** Detached HEAD: identification & safe exits
**18.2** Remote divergence: `pull --rebase`, reconciling rewrites
**18.3** Safe force push: `push --force-with-lease` vs `--force`
**18.4** Repo health: `fsck`, `gc` problems, corrupt refs
**18.5** Backups & mirrors: `bundle`, `clone --mirror`
**18.6** Playbooks for “oops” moments (checklist mindset)

## Module 19 — Tooling & Ecosystem Add-Ons

**19.1** Terminal UIs & pagers: `tig`, delta
**19.2** GitHub CLI/`gh`, GitLab CLI/`glab` basics
**19.3** Commit linting & policy: commitlint, pre-commit config
**19.4** Semantic release/versioning bots
**19.5** Visualizers & analytics (contrib graphs, hotspots)

## Module 20 — Curated Interview Drills

**20.1** WT/Index/HEAD; HEAD/ORIG_HEAD/FETCH_HEAD/MERGE_HEAD roles
**20.2** Undo matrix: staged edits, last commit, a merge, a pushed commit
**20.3** Rebase vs merge narratives: pros/cons & failure modes
**20.4** Conflict-resolution clinic: minimal, correct merges
**20.5** Bisect storytelling: end-to-end example
**20.6** Scaling: shallow/partial/sparse, monorepo onboarding
**20.7** Security: scrub a secret from history; prevent re-intro (hooks/CI)
**20.8** Submodule pitfalls in CI and how to fix
**20.9** Hotfix & backport scenario on release branch
**20.10** Branch-protection design for regulated teams

If you want, I can turn this into a printable one-pager checklist or add sample interview Q\&A under each sub-module.
