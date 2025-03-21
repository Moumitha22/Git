# Task 3 - Undoing Changes and Reverting Commits
    
## Objectives:
- Experiment with undoing changes in your working directory and commits.
    
## Commands Used:

### 1. `git restore file-name`
- **Purpose:** Discards uncommitted changes in a file, restoring it to the last committed state.
- **Use Case:** When you modify a file and want to undo changes before staging.
- It is the newer alternative to `git checkout -- <file>`
- **Effect:** Changes in the working directory are discarded, but the commit history is not affected.

```sh
git restore file.txt  # Newer version
# OR
git checkout -- file.txt  # Older Git versions
```
![Restore](restore.png)



### 2. `git reset`
- **Purpose:** Moves the branch pointer (HEAD) to an earlier commit, removing commits from history.

#### Use Cases:
- Soft Reset (--soft): Undo commit but keep changes staged.
- Mixed Reset (--mixed): Undo commit and unstage changes.
- Hard Reset (--hard): Undo commit and discard changes permanently.
- Reset a particular file: Unstages a file,but keeps it modified.

```sh
git reset --soft HEAD~1  # Undo last commit, keep changes staged
git reset --mixed HEAD~1  # Undo last commit, unstage changes
git reset --hard HEAD~1  # Undo last commit and discard changes
git reset file_name   # Unstages the file only, keeping its changes
```
![Reset](reset.png)

- **Note :** The commit history is rewritten, so it's not safe for shared repositories.



### `git revert <commit>`

#### `git revert <commit_hash>`:
- Purpose: Creates a new commit that undoes the changes from a specific commit.
- Use Case: When you want to undo changes safely without rewriting history.
- Effect: A new commit is created, preserving history. This is the preferred method for shared repositories.

```sh
git revert abc1234  # Undo commit with hash abc1234
```

#### `git revert HEAD`:
- Reverts the most recent commit (HEAD).
- Equivalent to git revert <latest commit hash>.

```sh
git revert HEAD
```

![Revert](revert.png)