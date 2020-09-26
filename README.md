# diff-size-limit
A pre-commit hook that enforces a maximum number of lines changed in a branch. It warns you when you have 300 lines changed compared to the master branch, and fails at 600 lines changed.

The limits were chosen based on [this research from IBM](https://www.ibm.com/developerworks/rational/library/11-proven-practices-for-peer-review/index.html) about effective code review practices and the knowledge that developers are likely to complain if the limits were actually that low. 

If you need some help figuring out how to make your code review smaller, [try some of these ideas](https://alexgaynor.net/2015/dec/29/shrinking-code-review/).

## Installation
Add this to your .pre-commit-config.yaml file:

```
- repo: https://github.com/tsaylor/diff-size-limit
  rev: master
  hooks:
  - id: diff-size-limit
```
