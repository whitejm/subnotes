# Git Branching

## 3.1 Branches in a Nutshell

--- 

What are branches in git?

> Basically a named pointer to a specific commit

---

### Creating a New Branch

---

Create a new branch call `testing`

> `git branch testing`

---

How does git keep track of what branch you are on?

> It uses a special pointer called `HEAD` to point to the current branch pointer

---

If you create a new branch `testing` using the command `git branch testing`
will you automatically change to that new branch?

> No, you will remain on the current branch, you would still need to run
> `git checkout testing` to switch to the new `testing` branch

---

### Switching Branches

---

Command to change to branch `dev`

> `git checkout dev`

---

Create a new branch called `mydev` and switch to it with one command

> `git checkout -b mydev`

---

## 3.2 Basic Branching and Merging

---

You've just commmited to branch `dev1` and want to merger it into `master` (2 commands)

> `git checkout master`  
> `git merger dev1`

---

After you've merged in a branch and no longer need it, is it a good idea to delete it?

> Yes

---

Delete branch `dev234`

> `git branch -d dev234`

---

### Basic Merging

---

Under what conditions does git merger create a new snapshot/commit?

> When the two branches being merged have diverged history

---

Does a git merger always create a new commit?

> No, only when the branches being merged have a "diverged" history.
> In other words, when the they both have commits that the other does not.

---

### Basic Merge Conflicts

---

When do merge conflicts happen?

> When you've changed the same part of the same file differently in two 
> different branches and then try to merge them... 
> Or when you've added two different versions of the same new file in both branches

---

Your merger fails with conflicts. What is the command to get more information 
about the files involved with the conflict?

> `git status`

---

There is a merge conflict involving `somefile`. After you've edited `somefile`
to address the conflict what git command do you use to resolve it?

> `git add somefile`  
> `git commit -m "merge conflict resolved"`  
> OR...  
> `git commit -a -m "merge conflict resolved"`

---

