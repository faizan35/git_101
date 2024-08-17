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

#### 3.1. **Working with Remotes**

- Adding remote repositories (`git remote add`)
- Removing and renaming remotes (`git remote remove`, `git remote rename`)

#### 3.2. **Fetching and Pulling**

- Fetching changes from remote (`git fetch`)
- Pulling changes from remote (`git pull`)

#### 3.3. **Pushing**

- Pushing changes to remote (`git push`)
- Force pushing (`git push --force`)

### 4. **Collaboration and Workflow**

- **Pull Requests (PR)**

  - Creating pull requests on GitHub
  - Reviewing and merging pull requests
  - Resolving conflicts in PRs

- **Code Reviews**

  - Performing code reviews on GitHub
  - Using GitHub review tools and comments

- **Collaboration Workflow**
  - Gitflow workflow
  - Forking workflow
  - Feature branching workflow

### 5. **Advanced Git Concepts**

- **Rebasing**

  - Interactive rebasing (`git rebase -i`)
  - Squashing commits
  - Resolving rebase conflicts

- **Cherry-picking**

  - Cherry-picking commits (`git cherry-pick`)

- **Stashing**

  - Stashing changes (`git stash`)
  - Applying stashed changes (`git stash apply`)

- **Reflog**
  - Understanding and using Git reflog (`git reflog`)

### 6. **GitHub Specific Features**

- **GitHub Actions**

  - Understanding GitHub Actions and workflows
  - Creating and managing workflows

- **GitHub Issues**

  - Creating and managing issues
  - Using labels, milestones, and projects

- **GitHub Projects**

  - Managing projects using GitHub Projects

- **GitHub Wiki**
  - Creating and managing a GitHub Wiki

### 7. **Security and Best Practices**

- **SSH and GPG**

  - Configuring SSH keys for GitHub
  - Signing commits with GPG

- **Best Practices**
  - Writing good commit messages
  - Keeping a clean commit history
  - Avoiding common pitfalls (e.g., committing sensitive information)

### 8. **Tools and Integrations**

- **Git Tools**

  - GUI tools for Git (e.g., GitKraken, Sourcetree)
  - Using Git in IDEs (e.g., VSCode, IntelliJ)

- **CI/CD Integrations**
  - Integrating GitHub with CI/CD tools (e.g., Jenkins, Travis CI)
  - Automating deployments with GitHub Actions

### 9. **Backup and Recovery**

- **Backup Strategies**

  - Strategies for backing up Git repositories

- **Recovery**
  - Recovering lost commits and branches
  - Using reflog and stash for recovery

### 10. **Git and GitHub for DevOps**

- **Infrastructure as Code (IaC)**

  - Versioning infrastructure code with Git
  - Using GitHub for IaC repositories

- **Monitoring and Logging**
  - Setting up webhooks for monitoring repository events
  - Integrating GitHub with monitoring tools
