Refs: [Git_sheet](https://bitbucket.org/BitPusher16/dotfiles/raw/49a01d929dcaebcca68bbb1859b4ac1aea93b073/refs/git/git_examples.sh)
### Clean your Docker (check it weekly/everytime I build ivy container ):
```py
# check how much space is getting used:
docker system df

# check how much space is getting used by `dangling images`:
docker images -f dangling=true # -f = filter

# run the command below to remove `dangling` as well as `unused` images
docker image prune -a # removing the -a flag will just prune `dangling`
```
refs:
- <https://stackoverflow.com/questions/53221412/why-the-none-image-appears-in-docker-and-how-can-we-avoid-it/53224187#53224187>
- <https://stackoverflow.com/questions/45142528/what-is-a-dangling-image-and-what-is-an-unused-image>
### How to run pdb:
can set a breakpoint by adding the line `import pdb`; `pdb.set_trace()` at the point in your code where you want the debugger to pause.

Run your code: Run your code as you normally would. When the code reaches the breakpoint, it will pause execution and enter the debugger.

Step through the code: Once you are in the debugger, you can use various commands to step through your code. Some common commands include:
```text
n: Execute the next line of code.
c: Continue execution until the next breakpoint.
q: Quit the debugger.
p: Print the value of an expression.
ll: List the source code for the current function or frame.
```
### In case of pytest discovery error:
```py
pytest --collect-only
```
refs: [stackoverflow](https://stackoverflow.com/questions/55837922/vscode-pytest-test-discovery-fails)

### Update Array_API:

You can go inside the `ivy_tests/array_api_testing/test_array_api`
```py
 git submodule update --remote
```
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
### git stash with name:
```py
git stash push -m "describe_the_stash"
```
### Fancy Git log:
```
git log --all --oneline --graph --decorate

```
### View a file content:
```py
git show <branch_name>:<file_name>
```
### Run pre-commit for a file:
```py
pre-commit run --files <path-to-file>
```

### Running VPN(mullvad) via openvpn CLI :
```py

cd /etc/openvpn/
sudo openvpn --config /etc/openvpn/mullvad_gb_all.conf # Change "_gb_all" with whatever region you like
curl https://am.i.mullvad.net/connected # check for connection! 


```

