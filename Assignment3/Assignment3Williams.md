# Assignment #3 – Nigel Williams

## Configuration

### Set Git global configuration

```bash
git config --global user.name "nigelwilli"
git config --global user.email "nigelwilliams180@gmail.com"
git config --global core.editor "code --wait"
```
View current Git configuration

```bash
git config --global --list
git config --local --list
```

Result (Global):
```bash
user.name=nigelwilli
user.email=nigelwilliams180@gmail.com
core.editor=code --wait
```
Result (Local):

```bash
remote.origin.url=https://github.com/nigelwilli/msse642-2025summer.git

Working with a Local Repo
```
Create a new repo

```bash
mkdir local-repo
cd local-repo
git init
```
Clone a repo

```bash
git clone https://github.com/nigelwilli/msse642-2025summer.git
cd msse642-2025summer
```
Check repo status

```bash
git status
```
Result:

```bash
On branch main
nothing to commit, working tree clean
```
Stage and commit changes

```bash
echo "msse git file" > msse.txt
git add msse.txt
git commit -m "Add msse.txt for assignment"
```
Delete a versioned file

```bash
git rm msse.txt
git commit -m "Remove msse.txt from repo"
```
Example .gitignore
Create a .gitignore file:

```bash
echo "*.log" > .gitignore
echo "node_modules/" >> .gitignore
git add .gitignore
git commit -m "Add .gitignore to exclude logs and dependencies"
```
Working with a Remote
View remote

```bash
git remote -v
```
Result:

```bash
origin  https://github.com/nigelwilli/msse642-2025summer.git (fetch)
origin  https://github.com/nigelwilli/msse642-2025summer.git (push)
```
Fetch changes

```bash
git fetch
```
Pull changes

```bash
git pull
```
Result:

```bash
Already up to date.
```
Push local commits

```bash
git push
```
Result:

```bash
Everything up-to-date
```
Branches
View local branches

```bash
git branch
```
Result:

```bash
* main
```
Create and switch branches

```bash
git branch msse-feature
git branch
git checkout msse-feature
```
Result:

```bash
* msse-feature
  main
```
View all branches

```bash
git branch -a
```
Result:


```bash
  main
* msse-feature
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
```
Delete local branch

```bash
git checkout main
git branch -d msse-feature
git branch
```
Result:

```bash
Switched to branch 'main'
Deleted branch msse-feature.
* main