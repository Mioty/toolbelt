# Git Aliases

- `git bl`
- `git blr`
- `git co`
- `git fe`
- `git fi`
- `git mi`
- `git up`
- `git cm`
- `git sync`
- `git bdone`

<br>

## Branch Operations

- List local branches
```
git bl
```
- List remote branches
```
git blr
```
- Checkout remote branch
```
git co <remote-branch>
```
- Create a feature branch
```
git fe <branch-name>
```
- Create a fix branch
```
git fi <branch-name>
```
- Create a misc branch
```
git mi <branch-name>
```
- Update currrent branch
```
git up
```

<br>

## Commiting

- Launches commit tool. Creates commit and returns after **one** commit.
```
git cm
```

<br>

## Pull Request

- Updates current branch by pull-ing in any updates on origin/master into the branch*
```
git sync
```
- Once pull request has been merged, this will checkout/update *master* and delete the branch
```
git bdone
```

<br>

## *Notes
If `git sync` results in a conflict then:

1. Correct conflict
2. `git add <conflicting-file>`
3. `git rebase --continue`
