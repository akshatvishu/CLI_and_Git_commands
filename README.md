Refs: [Git_sheet](https://bitbucket.org/BitPusher16/dotfiles/raw/49a01d929dcaebcca68bbb1859b4ac1aea93b073/refs/git/git_examples.sh)
- In case of pytest discovery error:
```py
pytest --collect-only
```
refs: [stackoverflow](https://stackoverflow.com/questions/55837922/vscode-pytest-test-discovery-fails)

# CLI_and_Git_commands
- Repo for uselfull command in git and CLI for me! 

### Check a pull request quickly without polluting local branch
```py
git fetch upstream pull/ID/head && git checkout FETCH_HEAD
```
refs: [stackoverflow](https://stackoverflow.com/questions/27567846/how-can-i-check-out-a-github-pull-request-with-git)

### Check for modified file in branch:
```py
git diff --name-only <name_of_branch_to_compare>
```
### Watch stash creation date:
```py
git stash list --date=short
```
### Fancy Git log:
```
git log --all --oneline --graph --decorate

```
