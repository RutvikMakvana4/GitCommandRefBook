## **Git Commands Reference :-**

## <span style="color: orange">Configuring Git</span>

To set up your Git configuration globally, use the following commands:

```bash
# Set the global Git username
$ git config --global user.name "Your Name"

# Set the global Git email
$ git config --global user.email "you@example.com"

# Enable colorization of Git output
$ git config --global color.ui auto

```

## <span style="color: orange">Git Commands for Project Management</span>

### Initializing a New Repository

- To create a new local repository:

```bash
git init [project name]
```

### Cloning a Repository

- To download a project with its entire history from a remote repository:

```bash
git clone [project url]
```

### Removing a File

- To remove a file from the working directory and staging area:

```bash
git rm [file]
```

### Stashing Changes

- To temporarily stash current changes for later use:

```bash
git stash
```

### Applying Stashed Changes

- To apply stored stash content into the working directory and clear the stash:

```bash
git stash pop
```

### Dropping a Stash

- To delete a specific stash from all your previous stashes:

```bash
git stash drop
```

## <span style="color: orange">Day-to-Day Git Commands</span>

### Checking Repository Status

- To display the status of your working directory:

```bash
git status
```

### Adding Files to Staging Area

- Adding Files to Staging Area

```bash
git add [file]
```

### Viewing Changes

- To show changes between the working directory and the staging area:

```bash
git diff [file]
```

- To show changes between the staging area and the repository:

```bash
git diff --staged [file]
```

### Discarding Changes

- To discard changes in the working directory irreversibly:

```bash
git checkout -- [file]
```

### Reverting Changes

- To revert your repository to a previous known working state:

```bash
git reset [file]
```

### Committing Changes

- To create a new commit from changes added to the staging area:

```bash
git commit
```

## <span style="color: orange">Git Branching Commands</span>

### Listing Branches

- To list all local branches in the repository:
- With -a, it shows all branches including remote branches.

```bash
git branch [-a]
```

### Creating a New Branch

- To create a new branch referencing the current HEAD:
- Creates a new branch named [branch_name].

```bash
git branch [branch_name]
```

### Switching Branches

- To switch the working directory to the specified branch:
- Switches to [branch_name]. Use -b to create the branch if it doesn't exist.

```bash
git checkout [-b] [branch_name]
```

### Merging Branches

- To merge a specified branch into your current branch:
- Merges [from_name] into your current branch.

```bash
git merge [from_name]
```

### Deleting Branches

- To remove a selected branch if it is already merged:
- Use -D instead of -d to force deletion even if not merged.

```bash
git branch -d [name]
```

## <span style="color: orange">Reviewing Your Work</span>

### Viewing Commit History

- To list commit history of the current branch:

```bash
git log [-n count]
```

### Compact Commit History View

- To view an overview with reference labels and history graph, showing one commit per line:

```bash
git log --oneline --graph --decorate
```

### Comparing Commit History

- To list commits that are present on the current branch and not merged into [ref]:
- Replace [ref] with a branch name or tag name.

- To list commits that are present on [ref] and not merged into the current branch:

```bash
git log ..[ref]


git log [ref]..

```

### Viewing Local Repository Operations

- To list operations (e.g., checkouts or commits) made on the local repository:

```bash
git reflog
```

## <span style="color: orange">Tagging Commits</span>

### Listing Tags

- To list all tags in the repository:

```bash
git tag
```

### Creating Lightweight Tags

- To create a tag reference named [name] for the current commit:
- Use [commit sha] to tag a specific commit instead of the current one.

```bash
git tag [name] [commit sha]
```

### Creating Annotated Tags

- To create an annotated tag object named [name] for the current commit:
- Annotated tags include a message and other metadata.

```bash
git tag -a [name] [commit sha]
```

### Deleting Tags

- To remove a tag from the local repository:

```bash
git tag -d [name]
```

## <span style="color: orange">Reverting Changes</span>

### Resetting Changes

- To switch the current branch to `[target reference]`, leaving differences as uncommitted changes:
- Use --hard to discard all changes.

```bash
git reset [--hard] [target reference]
```

### Reverting Commits

- To create a new commit that reverts changes from a specified commit:
- Creates a new commit that inverses changes from [commit sha].

```bash
git revert [commit sha]
```

## <span style="color: orange">Synchronizing Repositories</span>

### Fetching Changes

- To fetch changes from the remote repository `[remote]` without updating tracking branches:

```bash
git fetch [remote]
```

### Deleting Remote References

- To fetch changes from [remote] and delete remote references that were removed from the remote repository:

```bash
git fetch --prune [remote]
```

### Pulling Changes

- To fetch changes from [remote] and merge the current branch with its upstream:

```bash
git pull [remote]
```

### Pushing Changes

- To push local changes to the remote repository [remote]:
- Use --tags to push tags along with the commits.

```bash
git push [--tags] [remote]
```

### Setting Upstream Branch

- To push a local branch to [remote] and set it as the upstream branch:

```bash
git push -u [remote] [branch]
```
