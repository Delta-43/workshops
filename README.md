# workshops
Workshop Files, Documents and Projects organised at 42 Warsaw

[![Guided Coding](https://img.shields.io/badge/guided%20coding-showcase-1f6feb)](https://delta-43.github.io/guided-coding-workshop/)
[![Co-operative Coding](https://img.shields.io/badge/co--operative%20coding-play%20the%20demo-1f6feb)](https://delta-43.github.io/cooperative-coding-workshop/)

Each workshop lives in its own repository and is included here as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules), so it can be cloned, versioned and shared on its own.

## Workshops

| Workshop | What it covers | Try it | Folder |
|---|---|---|---|
| **Guided Coding Workshop** | AI-assisted development at three levels (web chat → editor + memory → CLI agents), building one weather dashboard three times. | [Weather Dashboard](https://delta-43.github.io/guided-coding-workshop/) | [`guided-coding-workshop/`](https://github.com/Delta-43/guided-coding-workshop) |
| **Co-operative Coding Workshop** | Working as a team with AI agents: roles, a shared contract, issues, branches, pull requests, CI and sign-off. Two people and two agents build a live quiz game on stage. | [Guess Closer!](https://delta-43.github.io/cooperative-coding-workshop/) | [`cooperative-coding-workshop/`](https://github.com/Delta-43/cooperative-coding-workshop) |

## Get everything

```bash
git clone --recurse-submodules https://github.com/Delta-43/workshops.git
```

Already cloned without submodules? Run `git submodule update --init`.

To get just one workshop, clone its own repository, e.g. `git clone https://github.com/Delta-43/guided-coding-workshop.git`.

## For maintainers

A submodule is pinned to one commit of its workshop repo. After pushing new work to a workshop, update the pin here:

```bash
git submodule update --remote guided-coding-workshop
git add guided-coding-workshop
git commit -m "Update guided-coding-workshop"
git push
```

Adding a new workshop (create the empty repo on GitHub first):

```bash
git submodule add -b main ../<new-workshop>.git <new-workshop>
git commit -m "Add <new-workshop>"
git push
```

The relative URL (`../<name>.git`) means the submodule clones over SSH for anyone who cloned this repo over SSH, and over HTTPS otherwise.
