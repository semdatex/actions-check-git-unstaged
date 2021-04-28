check-git-integrity-action
==========================

Github Action that checks if there are staged, but uncommitted changes in a CI pipeline

### How to use

Add this step to check if previous steps have made changes on versioned files: `Qualifyze/check-integrity-git-integrity-action`

Example workflow:

```yaml 
name: Test
on: push
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Install modules
        run: npm ci
      - uses: Qualifyze/check-git-integrity-action
```
