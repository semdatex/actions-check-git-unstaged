actions/check-git-unstaged
==========================

GitHub Action that checks if there are staged, but uncommitted changes in a CI pipeline

### How to use

Add this step to check if previous steps have made changes on versioned files: `semdatex/actions-check-git-unstaged`

Example workflow:

```yaml
name: Test
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Install modules
        run: npm ci
      - uses: semdatex/actions-check-git-unstaged@v1
```
