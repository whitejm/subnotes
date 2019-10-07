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

Stage a modified file, `LICENSE.txt`

>     git add LICENSE.txt

---

Get a compact status of your rep

>     git status -s

---

### Ignoring Files

---

How do you get git to ignore files?

> add the to a `.gitignore` file

---

How are `.gitignore` files applied by git?

> They are applied to the directory they are in recursively 

---

