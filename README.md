# workshops
Workshop Files, Documents and Projects organised at 42 Warsaw

Each workshop lives in its own repository and is included here as a [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules), so it can be cloned, versioned and shared on its own.

## Workshops

| Workshop | What it covers | Folder |
|---|---|---|
| **Guided Coding Workshop** | AI-assisted development at three levels (web chat → editor + memory → CLI agents), building one weather dashboard three times. | [`guided-coding-workshop/`](https://github.com/Delta-43/guided-coding-workshop) |

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
