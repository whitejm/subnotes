# Git Basics

## Getting a Git Repository

---

Initialize a new repo for a working dir called `myproject`

>     cd myproject/ 
>     git init

---

Clone `https://github.com/libgit2/libgit2` renaming it `mylibgit2`

>     git clone https://github.com/libgit2/libgit2 mylibgit2

---

Clone `https://github.com/libgit2/libgit2` without renaming it

>     git clone https://github.com/libgit2/libgit2

---

## Recording Changes to the Repository

---

The two "top" states a file can be in

> - Untracked
> - Tracked

---

The three states a Tracked file can be in

> - Unmodified
> - Modified 
> - Staged 

---

How do you check the status ("state") of your files?

>     git status

---

What kind of files will go into your next commit?

> Staged files

---

Start tracking a new file, `README.md`

>     git add README.md

---

**TODO** add level 3 headings for above questions

### Staging Modified Files

---

Stage a modified file, `LICENSE.txt`

>     git add LICENSE.txt

---

### Short Status

---

Get a compact status of your rep

>     git status -s

---

### Ignoring Files

---

How do you get git to ignore files?

> add them to a `.gitignore` file

---

What files are rules in `.gitignore` applied to by git?

> They are applied to the directory they are in recursively 

---

Can you have multiple `.gitignore` files in a repo?

> Yes, they are applied to the directory they are in recursively 

---

What kind of pattern matching to `.gitignore` files use?

> Glob patterns

---

Write rules in a `.gitignore` file that ignore all `.a` files except
`lib.a`

>     *.a
>     !lib.a

---

**TODO:** more gitignore questions... 

### Viewing Your Staged and Unstaged Changes

---

Command to see what you've changed, but not yet staged

>     git diff

---

Command to compare working files and staged files

>     git diff

---

Command to view changes in staged files

>     git diff --staged

---

Does `git diff` show all changes since last commit?

> No, only unstaged changes, you would need to also use `git diff --staged` to 
> any see staged changes

---

### Committing Your Changes

---

Command to commit staged files

>     git commit

---

Command to commit staged files with message included

>     git commit -m my commit message

---

### Skipping the Staging Area

---

Command to stage and commit files at the same time

>     git commit -a

---

### Removing Files

---

Command for remove a file (`README.md`) (untrack/unstage/delete)

>     git rm README.md

---

Command to unstage/untrack file (`README.md`), but not delete it from working directory

>     git rm --cached README.md

---

### Moving Files

---

Does git explicitly track file movement?

> No

---

rename or move file `README` to `README.md`

>     git mv README README.md

---

What 3 commands is `git mv README README.md` equivalent to?

>     mv README README.md
>     git rm README
>     git add README.md

---

## Viewing the Commit History


## Undoing Things

## Working with Remotes

## Tagging

### Listing Your Tags

---

List all tags

> `git tag`

---

List all tags that start with `v1.8`

> `git tag -l "v1.8*"`

---

### Creating Tags

---

What are the two types of tags in git?

> lightweight & annotated

---

Which type of tag is recommended?

> annotated tags

---

describe lightweight tag

> just a pointer to a specific commit

---

### Annotated Tags

---

What command and option is used to create an annotated tag?

> `git tag -a v1.5 -m "v1.5 message"`

---

Command to display info about tag `v1.2`

> `git show v1.2`

---

### Lightweight Tags

---

create a lightweight tag, `v2.4`

> `git tag v2.4`

---

### Tagging Later

---

Tag a previous commit (checksum is `8a5cbc4`) with `v3.4`

> `git tag -a v3.4 8a5cbc4`

---

### Sharing Tags

---

Does a normal git push transfer tags to a remote server?

> No

---

Push all tags to remote `origin` server

> `git push origin --tags`

---

Push tag `v2.1` to remote `origin` server

> `git push origin v2.1`

---

Does `git push` distinguish between lightweight and annotated tags?

> No

---

### Deleting Tags

---

Delete local tag `5.1.3`

> `git tag -d 5.1.3 

---

Delete tag `3.2` on the remote (`origin`) server

> `git push origin --delete 3.2`

---

### Checking out Tags


## Git Aliases

## Summary

Some personal additions..

---

What does `git add somefile` do?

> - If `somefile` is untracked it will now be tracked and staged
> - If `somefile` is tracked and modified it will now be staged

---

What will `git commit -a somefile` do if `somefile` is untracked?

> Nothing

---