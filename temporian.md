## Update Your Local Repository:

First, ensure you're on the main branch and pull the latest changes:

```bash
git checkout main
git pull origin main
```

Then, switch to your trig branch. If it's a new branch, create it based on the updated main branch:

```bash
git checkout -b trig  # Creates and switches to the new branch if it doesn't exist
# or, if the branch already exists:
git checkout trig
```

## Activate the Python Environment:

This step remains the same. Activate the Poetry environment:

```bash
poetry shell
```

## Update Dependencies:

Inside the Poetry environment, update your dependencies:

```bash
poetry update
```

## Install and Sync Bazel Dependencies:

Ensure Bazel dependencies are in sync. This is the same regardless of the branch you're on:

```bash
bazel sync
```

## Run Tests Regularly:

Continue to run tests regularly while working on the trig branch:

```bash
bazel test --config=linux //...:all
```
