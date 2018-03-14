# Config > Git Aliases

The following commands will be shown using the following template:

```sh
$ git full-command-name
$ git shorthand
```

When there is no shorthand form of the command, only one command will be shown. Arguments are listed in each description using shell notation (`$1`, `$2`, etc).

**NOTE**: these commands assume the developer is using [nvie's branching model](http://nvie.com/posts/a-successful-git-branching-model/).

### Meta

- list all aliases

```sh
$ git list-aliases
$ git la
```

### Branches

- which branch is develop? ("dev" by default; good practice to override in ~/.gitaliases_local)

```sh
$ git dev-branch
```

- what is the current branch?

```sh
$ git current-branch
$ git cb
```

### Checking out branches (assumes they exist on remote)

- checkout bugfix branch for a given ticket (`$1`)

```sh
$ git checkout-bugfix
$ git cobf
```

- checkout feature branch for a given ticket (`$1`)

```sh
$ git checkout-feature
$ git cof
```

- checkout hotfix branch for a given version (`$1`)

```sh
$ git checkout-hotfix
$ git cohf
```

- checkout release branch for a given version (`$1`)

```sh
$ git checkout-release
$ git cor
```

- checkout tag (`$1`) as branch

```sh
$ git checkout-tag
$ git ct
```

### Committing files

- commit all files

```sh
$ git commit-all
$ git ca
```

### Comparing branches

- non-merged commits in current branch not in a given branch (`$1`)

```sh
$ git current-commits-not-in
$ git ccni
```

- non-merged commits in current branch that are not in dev

```sh
$ git current-commits-not-in-dev
$ git ccnid
```

- non-merged commits in current branch that are not in master

```sh
$ git current-commits-not-in-master
$ git ccnim
```

- non-merged commits in branch (`$1`) but not in dev

```sh
$ git commits-not-in-dev
$ git cnid
```

- non-merged commits in branch (`$1`) but not in master

```sh
$ git commits-not-in-master
$ git cnim
```

- non-merged commits between current branch and target branch (`$1`); both directions

```sh
$ git commit-diff-against
$ git cda
```

### Comparing commits

- diff between last commit and its parent

```sh
$ git diff-last-commit
$ git dlc
```

### Creating branches

- create bugfix branch from local dev branch as bugfix/{ticketId} (`$1`)

```sh
$ git bugfix-from-dev
$ git bfd
```

- create feature branch from current branch as feature/{ticketId} (`$1`)

```sh
$ git feature-from-current
$ git ffc
```

- create feature branch from local dev branch as feature/{ticketId} (`$1`)

```sh
$ git feature-from-dev
$ git ffd
```

- create hotfix branch from local dev branch as hotfix/{version} (`$1`)

```sh
$ git hotfix-from-master
$ git hfm
```

- create release branch from local dev branch as release/{version} (`$1`)

```sh
$ git release-from-dev
$ git rfd
```

### Deleting branches

- delete all branches without "dev" (or whatever `git dev-branch` returns) or "master" in the name

```sh
$ git cleanup-branches
$ git cub
```

- dry run of the above command:

```sh
$ git dry-run-cleanup-branches
$ git drcub
```

- prune all remotes

```sh
$ git prune-all
```

### Finding files

- find files (`$1`) in codebase

```sh
$ git find
```

### Git shortcuts

- branch

```sh
$ git br
```

- commit

```sh
$ git ci
```

- checkout

```sh
$ git co
```

- status

```sh
$ git st
```

### Logs

- list one-line commits showing dates

```sh
$ git lds
```

- list one-line commits showing dates & changed files

```sh
$ git llds
```

- list commits in short form

```sh
$ git ls
```

- list commits showing changed files

```sh
$ git ll
```

### Reloading branches

- Reload a given branch (`$1`) (local branch will be lost)

```sh
$ git reload-branch
$ git rb
```

### Tags

- latest tag name

```sh
$ git latest-tag-name
$ git ltn
```

- list tags by create date

```sh
$ git tag-create-dates
$ git tcd
```

### Workflow

- set the current branch's upstream to origin

```sh
$ git fixup-branch
$ git fb
```

- oldest ancestor from a given branch (`$1`)

```sh
$ git oldest-ancestor
$ git oa
```

- rebuild branch against a given branch (`$1`) (destructive)

**NOTE**: this assumes that both branches are local and up-to-date. Consider pushing a copy of the branch to the remote before executing.

```sh
$ git rebuild-branch-against
$ git rba
```

- undo rebuild branch with a given remote (`$1`)

```sh
$ git undo-rebuild-branch-with-remote
$ git urba
```

- reset all branch commits starting from oldest-ancestor from a given branch (`$1`)

```sh
$ git reset-all-commits
$ git rac
```

- squash all branch commits starting from oldest-ancestor of a given branch (`$1`)

```sh
$ git squash-all-commits
$ git sac
```

- push everything to the current branch at origin (more explicit that git push)

```sh
$ git push-origin
$ git po
```

- force-push everything to the current branch at origin

```sh
$ git force-push-origin
$ git fpo
```

- add everything to a new "Work in Progress" commit

```sh
$ git work-in-progress-local
$ git wipl
```

- commit everything and push up a "Work in Progress" commit to the current branch

```sh
$ git work-in-progress
$ git wip
```

- commit everything and force-push a "Work in Progress" commit to the current branch (use with caution)

```sh
$ git work-in-progress-forced
$ git wipf
```

- switch to dev, clean up local and remote branches

```sh
$ git sync
```

- pull the "canonical" ignore for the given language (`$1`) (view available ignores with `git ignore list`)

```sh
$ git ignore
```