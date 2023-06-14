# Git Cheat Sheet

**Git Configuration**

- Git config: Get and set configuration variables that control all facets of how Git looks and operates.
  - Set the name: `$ git config --global user.name "User name"`
  - Set the email: `$ git config --global user.email "himanshudubey481@gmail.com"`
  - Set the default editor: `$ git config --global core.editor Vim`
  - Check the settings: `$ git config --list`

Git Alias: Set up an alias for each command.
  - `$ git config --global alias.co checkout`
  - `$ git config --global alias.br branch`
  - `$ git config --global alias.ci commit`
  - `$ git config --global alias.st status`

**Starting a Project**

- Git init: Create a local repository
  - `$ git init <Repo Name>`
- Git clone: Make a local copy of the server repository
  - `$ git clone <remote Url>`

**Local Changes**

- Git add: Add a file to the staging (Index) area
  - `$ git add <Filename>`
- Git commit: Record or snapshots the file permanently in the version history with a message
  - `$ git commit -m "Commit Message"`

**Track Changes**

- Git diff: Track the changes that have not been staged
  - `$ git diff`
- Git status: Display the state of the working directory and the staging area
  - `$ git status`
- Git show: Shows objects
  - `$ git show <options> <objects>`

**Commit History**

- Git log: Display the most recent commits and the status of the head
  - `$ git log`
- Git blame: Display the modification on each line of a file
  - `$ git blame <file name>`

**Ignoring Files**

- .gitignore: Specify intentionally untracked files that Git should ignore
  - Create .gitignore: `$ touch .gitignore`
  - List the ignored files: `$ git ls-files -i --exclude-standard`

**Branching**

- Git branch: Create, list, delete, and rename branches
  - Create branch: `$ git branch <branch name>`
  - List branches: `$ git branch --list`
  - Delete branch: `$ git branch -d <branch name>`
  - Delete a remote branch: `$ git push origin --delete <branch name>`
  - Rename branch: `$ git branch -m <old branch name> <new branch name>`
- Git checkout: Switch between branches in a repository
  - Switch to a particular branch: `$ git checkout <branch name>`
  - Create a new branch and switch to it: `$ git checkout -b <branch name>`
  - Checkout a remote branch: `$ git checkout <remote branch>`
- Git stash: Switch branches without committing the current branch
  - Stash current work: `$ git stash`
  - Saving stashes with a message: `$ git stash save "<Stashing Message>"`
  - Check stored stashes: `$ git stash list`
  - Re-apply the changes that you just stashed: `$ git stash apply`
  - Track the stashes and their changes: `$ git stash show`
  - Re-apply the previous commits: `$ git stash pop`
  - Delete the most recent stash from the queue: `$ git stash drop`
  - Delete all available stashes at once: `$ git stash clear`
  - Stash work on a separate branch: `$ git stash branch <branch name>`
- Git cherry-pick: Apply the changes introduced by some existing commit
  - `$ git cherry-pick <commit id>`

**Merging**

- Git merge: Merge branches and commits
  - Merge branches: `$ git merge <branch name>`
  - Merge a specified commit to the currently active branch: `$ git merge <commit>`
- Git rebase: Apply a sequence of commits from distinct branches into a final commit
  - `$ git rebase <branch name>`
  - Continue the rebasing process: `$ git rebase --continue`
  - Abort the rebasing process: `$ git rebase --skip`
- Git interactive rebase: Allow various operations on existing commits
  - `$ git rebase -i`

**Remote**

- Git remote: Check the configuration of the remote server
  - Check the configuration: `$ git remote -v`
  - Add a remote for the repository: `$ git remote add <short name> <remote URL>`
  - Fetch data from the remote server: `$ git fetch <Remote>`
  - Remove a remote connection from the repository: `$ git remote rm <destination>`
  - Rename remote server: `$ git remote rename <old name> <new name>`
  - Show additional information about a particular remote: `$ git remote show <remote>`
  - Change remote: `$ git remote set-url <remote name> <new URL>`
- Git origin master: Push and pull data to/from a remote server
  - Push data to the remote server: `$ git push origin master`
  - Pull data from the remote server: `$ git pull origin master`

**Pushing Updates**

- Git push: Transfer commits from your local repository to a remote server
  - Push data to the remote server: `$ git push origin master`
  - Force push data: `$ git push <remote> <branch> -f`
  - Delete a remote branch using push command: `$ git push origin --delete <branch>`

**Pulling Updates**

- Git pull: Pull data from the server
  - Pull data from the server: `$ git pull origin master`
  - Pull a remote branch: `$ git pull <remote branch URL>`
- Git fetch: Download branches and tags from one or more repositories
  - Fetch the remote repository: `$ git fetch <repository URL>`
  - Fetch a specific branch: `$ git fetch <branch URL> <branch name>`
  - Fetch all branches simultaneously: `$ git fetch --all`
  - Synchronize the local repository: `$ git fetch origin`

**Undo Changes**

- Git revert: Undo changes
  - Undo changes: `$ git revert`
  - Revert a particular commit: `$ git revert <commit-ish>`
- Git reset: Reset changes
  - Reset changes hard: `$ git reset --hard`
  - Reset changes soft: `$ git reset --soft`
  - Reset changes mixed: `$ git reset --mixed`

**Removing Files**

- Git rm: Remove files from the working tree and the index
  - Remove files: `$ git rm <file Name>`
  - Remove files from Git but keep them in your local repository: `$ git rm --cached`
