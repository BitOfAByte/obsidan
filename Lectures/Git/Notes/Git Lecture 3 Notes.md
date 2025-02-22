---
tags:
  - Notes
links: "[[Git Lecture 3 Repository]]"
creation date: 2024-11-10 21:05
modification date: Sunday 10th November 2024 21:05:17
semester: 3
year: 2024
---


---
# [[Git Lecture 3 Notes]]

---



### Repo
A Git repository (repo) is a storage space where your project's history is stored. It <mark style="background: #FFB8EBA6;">contains all the revisions and edits of your files, along with the commit history, branches, tags, and more</mark>. Here's how it works and what you need to know about managing a Git repository.

### Understanding a Git Repo

- **Local Repository**: A local repo is on your computer, containing all the files and their history, allowing you to track changes, revert to previous states, and manage branches. 
- **Remote Repository**: A remote repo, often hosted on services like GitHub, GitLab, or Bitbucket, allows multiple developers to collaborate on the same project. Changes are pushed from local repos to remote repos and fetched or pulled from remote to local.

### Key Concepts and Operations

1. **Initializing a Repository**: To start a new Git repository in your project directory, use the `git init` command. This creates a `.git` directory in your project, which houses all the necessary repository files and history.

2. **Cloning a Repository**: To copy an existing Git repository, use the `git clone <repository-url>` command. This creates a local copy of the repo, including all its files, history, and branches.

3. **Staging Changes**: Before committing changes, they must be staged (indexed) using the `git add <file>` or `git add .` command, which adds the current changes in the specified files to the staging area.

4. **Committing Changes**: To save changes in the repository’s history, use the `git commit -m "commit message"` command. Each commit is a snapshot of your repository’s files at a specific point in time.

5. **Pushing Changes**: To upload your local branch commits to a remote repository, use the `git push <remote> <branch>` command. This updates the remote repository with your local changes.

6. **Fetching and Pulling Changes**: To update your local repository with changes from the remote, use `git fetch <remote>` to fetch changes without merging them, and `git pull <remote> <branch>` to fetch and directly merge the changes.

7. **Viewing the Commit History**: The `git log` command shows the commit history of the current branch, listing the commits in reverse chronological order.

8. **Branching in Repositories**: Branches are used to develop features or fix bugs in parallel. The `git branch` command lists, creates, or deletes branches.

9. **Merging Branches**: To integrate changes from one branch into another, use the `git merge <branch>` command. Conflicts may arise if the changes in the branches are incompatible.

### Best Practices
- Commit Often: Regular commits help to track changes more effectively and isolate issues.
- Meaningful Commit Messages: Use descriptive and meaningful commit messages to explain why a change was made.
- Branch Strategically: Use branches for separate features or fixes to keep the main codebase stable.

### Example: Simulating Two Coders Working on the Same Repo

#### Step 1: Initializing and Cloning the Repository

1. Alice initializes a new repository:

   ```sh
   git init my_project
   cd my_project
   ```

2. Alice creates a remote repository on GitHub and adds it as a remote:

   ```sh
   git remote add origin https://github.com/alice/my_project.git
   ```

3. Bob clones the repository:

   ```sh
   git clone https://github.com/alice/my_project.git
   cd my_project
   ```

#### Step 2: Creating Branches and Making Changes

1. Alice creates a new branch for her feature:

   ```sh
   git checkout -b feature-alice
   ```

2. Bob creates a new branch for his feature:

   ```sh
   git checkout -b feature-bob
   ```

3. Alice and Bob make changes in their respective branches and commit them:

   Alice:

   ```sh
   echo "Alice's code" > alice.txt
   git add alice.txt
   git commit -m "Add Alice's code"
   ```

   Bob:

   ```sh
   echo "Bob's code" > bob.txt
   git add bob.txt
   git commit -m "Add Bob's code"
   ```

#### Step 3: Pushing Changes to the Remote Repository

1. Alice pushes her changes:

   ```sh
   git push origin feature-alice
   ```

2. Bob pushes his changes:

   ```sh
   git push origin feature-bob
   ```

#### Step 4: Merging Changes

1. Alice merges her feature branch into the main branch:

   ```sh
   git checkout main
   git merge feature-alice
   git push origin main
   ```

2. Bob fetches the latest changes from the remote and merges his feature branch:

   ```sh
   git fetch origin
   git checkout main
   git merge origin/main
   git merge feature-bob
   git push origin main
   ```

#### Step 5: Resolving Conflicts (if any)

If there are any conflicts, Bob resolves them, stages the resolved files, commits, and pushes the changes:

   ```sh
   git add resolved_file.txt
   git commit -m "Resolve merge conflict"
   git push origin main
   ```

