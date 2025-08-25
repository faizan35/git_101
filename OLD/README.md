# Git and GitHub for DevOps Engineer

To prepare for a DevOps Engineer role with a focus on Git and GitHub, you should be proficient in the following topics:

### 1. **Basic Git Concepts**

#### [1.1. **Version Control Systems (VCS)**](./01-Basic-Git-Concepts/1.1-VCS.md)

- Understanding VCS and the benefits of using Git
- Difference between centralized and distributed VCS

#### [1.2. **Git Installation and Configuration**](./01-Basic-Git-Concepts/1.2-Git-Installation-Configuration.md)

- Installing Git on different operating systems
- Configuring Git (username, email, etc.)

#### [1.3. **Git Basics**](./01-Basic-Git-Concepts/1.3-Git-Basics.md)

- Initializing a repository (`git init`)
- Cloning a repository (`git clone`)
- Checking the status of files (`git status`)
- Adding files to staging (`git add`)
- Committing changes (`git commit`)
- Viewing commit history (`git log`)

### 2. **Branching and Merging**

#### [2.1. **Branching**](./02-Branching-and-Merging/2.1-Branching.md)

- Creating branches (`git branch`)
- Switching branches (`git checkout`)
- Creating and switching in one command (`git checkout -b`)

#### [2.2. **Merging**](./02-Branching-and-Merging/2.2-Merging.md)

- Merging branches (`git merge`)
- Fast-forward vs. three-way merges
- Resolving merge conflicts

#### [2.3. **Branch Management**](./02-Branching-and-Merging/2.3-Branch-Management.md)

- Deleting branches (`git branch -d`)
- Renaming branches (`git branch -m`)

### 3. **Remote Repositories**

#### [3.1. **Working with Remotes**](./03-Remote-Repositories/3.1-Working-with-Remotes.md)

- Adding remote repositories (`git remote add`)
- Removing and renaming remotes (`git remote remove`, `git remote rename`)

#### [3.2. **Fetching and Pulling**](./03-Remote-Repositories/3.2-Fetching-Pulling.md)

- Fetching changes from remote (`git fetch`)
- Pulling changes from remote (`git pull`)

#### [3.3. **Pushing**](./03-Remote-Repositories/3.3-Pushing.md)

- Pushing changes to remote (`git push`)
- Force pushing (`git push --force`)

### 4. **Collaboration and Workflow**

#### [4.1. **Pull Requests (PR)**](./04-Collaboration-Workflow/4.1-Pull-Requests.md)

- Creating pull requests on GitHub
- Reviewing and merging pull requests
- Resolving conflicts in PRs

#### [4.2. **Code Reviews**](./04-Collaboration-Workflow/4.2-Code-Reviews.md)

- Performing code reviews on GitHub
- Using GitHub review tools and comments

#### [4.3. **Collaboration Workflow / Straregy**](./04-Collaboration-Workflow/4.3-Collaboration-Workflow-Straregy.md)

- Gitflow workflow
- Forking workflow
- Feature branching workflow

### 5. **Advanced Git Concepts**

#### [5.1. **Rebasing**](./05-Advanced-Git-Concepts/5.1-Rebasing.md)

- Interactive rebasing (`git rebase -i`)
- Squashing commits
- Resolving rebase conflicts

#### [5.2. **Cherry-picking**](./05-Advanced-Git-Concepts/5.2-Cherry-picking.md)

- Cherry-picking commits (`git cherry-pick`)

#### [5.3. **Stashing**](./05-Advanced-Git-Concepts/5.3-Stashing.md)

- Stashing changes (`git stash`)
- Applying stashed changes (`git stash apply`)

#### [5.4. **Reflog**](./05-Advanced-Git-Concepts/5.4-Reflog.md)

- Understanding and using Git reflog (`git reflog`)

### 6. **Security and Best Practices**

#### [6.1. **SSH and GPG**](./06-Security-and-Best-Practices/6.1-SSH-GPG.md)

- Configuring SSH keys for GitHub
- Signing commits with GPG

#### [6.2. **Best Practices**](./06-Security-and-Best-Practices/6.2-Best-Practices.md)

- Writing good commit messages
- Keeping a clean commit history
- Avoiding common pitfalls (e.g., committing sensitive information)

### 7. **Backup and Recovery**

#### [7.1. **Backup Strategies**](./07-Backup-and-Recovery/7.1-Backup-Strategies.md)

- Strategies for backing up Git repositories

#### [7.2. **Recovery**](./07-Backup-and-Recovery/7.2-Recovery.md)

- Recovering lost commits and branches
- Using reflog and stash for recovery

### 8. **Git and GitHub for DevOps**

#### [8.1. **Infrastructure as Code (IaC)**](./08-Git-and-GitHub-for-DevOps/8.1-Infrastructure-as-Code.md)

- Versioning infrastructure code with Git
- Using GitHub for IaC repositories

#### [8.2. **Monitoring and Logging**](./08-Git-and-GitHub-for-DevOps/8.2-Monitoring-Logging.md)

- Setting up webhooks for monitoring repository events
- Integrating GitHub with monitoring tools
