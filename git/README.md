# Git

## What I am learning

Git as an engineering tool, not just a way to upload code: how history is built, how branches diverge and merge, how to undo mistakes, and how teams collaborate through remotes and pull requests.

## Why it matters

Every change I make to the main project, and every CI/CD pipeline later on, starts from a Git commit. Knowing Git well means I can change shared code safely and recover when something goes wrong.

> **Goal:** be able to work safely in a team Git repository.

---

## Learning objectives

By the end of this topic I can:

- Explain the working tree, staging area, and commit history in my own words
- Write clear, atomic commits and read history
- Create, switch, and merge branches
- Resolve merge conflicts calmly
- Explain merge versus rebase and use rebase safely
- Choose correctly between `restore`, `revert`, and `reset`
- Recover lost work with `reflog`
- Use remotes (`fetch`, `pull`, `push`)
- Work through a pull request workflow
- Keep secrets out of the repository

---

## Weekly progression

Git runs alongside Linux, starting in week 3.

| Week | Focus | Key commands |
|---|---|---|
| 3 | Core model: working tree, staging, commits, history | `init` `status` `add` `commit` `log` `diff` `show` |
| 4 | Branches, merging, conflicts, rebasing, undoing, remotes, pull requests | `branch` `switch` `merge` `rebase` `restore` `revert` `reset` `reflog` `fetch` `pull` `push` |

---

## Checklist

- [ ] Explain working tree, staging area, and commits
- [ ] Write atomic commits with clear messages
- [ ] Read history (`log`, `diff`, `show`)
- [ ] Create and switch branches
- [ ] Merge branches
- [ ] Resolve a merge conflict
- [ ] Explain merge versus rebase
- [ ] Rebase a feature branch safely
- [ ] Undo changes with `restore`, `revert`, and `reset`
- [ ] Recover a lost commit with `reflog`
- [ ] Use `fetch`, `pull`, and `push` and explain how they differ
- [ ] Complete a pull request workflow
- [ ] Use `.gitignore` and know what to do if a secret is committed

A box is ticked only when I can do or explain the task without relying entirely on a tutorial.

---

## Exercises

- [ ] Make five small commits, then rewrite their messages
- [ ] Create a conflict between two branches and resolve it
- [ ] Undo a pushed commit with `revert`
- [ ] Undo a local commit with `reset`, then recover it with `reflog`
- [ ] Rebase a branch onto an updated `main`
- [ ] Add a `.gitignore` and remove an already-tracked file from the index

## Labs

- [ ] **Broken history:** given a repository with a bad merge, a wrong reset, and a lost commit, repair it and document each step
- [ ] **Two clones, one remote:** simulate two collaborators, create diverging work, and resolve the push rejection
- [ ] **Leaked secret:** commit a fake secret, then remove it from history and explain why rotating it still matters

## Mini-project

Use Git on the Linux Server Health Monitor:

- Feature branches for each addition
- At least one pull request reviewed against its description
- A clean, readable commit history
- A short note on the branching workflow used

---

## Resources

- *Pro Git*: Scott Chacon and Ben Straub
- Official Git documentation
- *The Missing Semester of Your CS Education* (version control lecture)

## Completion criteria

- [ ] I can explain every checklist item in my own words
- [ ] I can resolve a conflict and recover from a mistake without a tutorial
- [ ] The mini-project has a clean history and a pull request workflow
- [ ] I reviewed the key concepts without AI
- [ ] Weekly reviews are written