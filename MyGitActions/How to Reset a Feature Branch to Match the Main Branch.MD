# Resetting a Feature Branch to Match the Main Branch

When working on a feature branch, you may want to discard all changes and reset it back to match the main branch. Follow the steps below:

## Steps to Reset a Feature Branch

### 1. Navigate to the Git Repository
Change your working directory to the location where the Git repository resides:
```sh
cd /path/to/your/git/repository
```

### 2. Switch to the Feature Branch
Ensure you are on the correct feature branch:
```sh
git checkout feature
```

### 3. Reset the Feature Branch to Match the Main Branch
Perform a hard reset to discard all local changes and set the branch to match `main`:
```sh
git reset --hard origin/main
```
This will:
- Remove all local commits that are not in `origin/main`.
- Discard all uncommitted changes.

### 4. Force Push to Remote (If Needed)
If the feature branch is already pushed to the remote repository and you want to overwrite it:
```sh
git push --force
```
**Warning:** Force pushing can overwrite changes made by others on the remote branch. Use with caution, especially when collaborating with a team.
