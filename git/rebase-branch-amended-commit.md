#Rebase a branch from a commit that has been amended
Given the following situation where a branch has been created from a specific commit and that
commit has been amended (such that the hash has been changed).

```
git checkout master
git checkout -b foo
git commit //commit to foo
git checkout master
git add ...
git commit --amend
git checkout foo
git rebase master
```
The follwing command can be run:

```git rebase --onto master ORIGINAL_FORK_SHA food```

Where `ORIGINAL_FORK_SHA` is the old SHA hash from the point at which `foo` was forked.

Example:

Your tree currently looks like this, and you need to rebase `foo` with the updated commit `aaaaaa` made to `master`

```
* aaaaaa - (master)
| * bbbbbb - (foo)
| * cccccc - (old master)
|/  
* ffffff
```

You can run:

```git rebase --onto master cccccc foo```

And the resulting tree will be:

```
* dddddd - (foo)
|
* aaaaaa - (master)
|
* ffffff
```