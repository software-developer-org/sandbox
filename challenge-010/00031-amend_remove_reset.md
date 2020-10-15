# **add**


**using _git add <filename>_**
- [add file contents to the index](https://git-scm.com/docs/git-add)

```
$ git add 00031-amend_remove_reset.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git commit -m 'created file for writing steps and results'
[feature/31-amend_remove_reset f45edc5] created file for writing steps and results
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 challenge-010/00031-amend_remove_reset.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git push -u origin feature/31-amend_remove_reset
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 360 bytes | 360.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'feature/31-amend_remove_reset' on GitHub by visiting:
remote:      https://github.com/software-developer-org/sandbox/pull/new/feature/31-amend_remove_reset
remote:
To https://github.com/software-developer-org/sandbox
 * [new branch]      feature/31-amend_remove_reset -> feature/31-amend_remove_reset
Branch 'feature/31-amend_remove_reset' set up to track remote branch 'feature/31-amend_remove_reset' from 'origin'.

``` 

**using _git add ._**
- stage all untracked files in folder

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git add .

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is up to date with 'origin/feature/31-amend_remove_reset'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   01-testfile.md
        new file:   02-testfile.md
        new file:   03-testfile.md


Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git commit -m 'created dummy-files for exercises'
[feature/31-amend_remove_reset e6ff111] created dummy-files for exercises
 3 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 challenge-010/01-testfile.md
 create mode 100644 challenge-010/02-testfile.md
 create mode 100644 challenge-010/03-testfile.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git push -u origin feature/31-amend_remove_reset
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 377 bytes | 377.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/software-developer-org/sandbox
   f45edc5..e6ff111  feature/31-amend_remove_reset -> feature/31-amend_remove_reset
Branch 'feature/31-amend_remove_reset' set up to track remote branch 'feature/31-amend_remove_reset' from 'origin'.
```
# **remove**

**using _git rm_**
- [removing files from working tree and index](https://git-scm.com/docs/git-rm#_description) 
- means: removing files from repository and filesystem 

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git rm 01-testfile.md
rm 'challenge-010/01-testfile.md'

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is up to date with 'origin/feature/31-amend_remove_reset'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        deleted:    01-testfile.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   00031-amend_remove_reset.md

```
**using _git rm --cached <filename>_**
- removing a file from staging area _without_ deleting it

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ touch 04-testfile.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git add 04-testfile.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git rm --cached 04-testfile.md
rm 'challenge-010/04-testfile.md'

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is up to date with 'origin/feature/31-amend_remove_reset'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        04-testfile.md

nothing added to commit but untracked files present (use "git add" to track)

```
- the file is back in _untracked_ state

**using _git rm -f_ <filename>** (-f = forced)
- removing _and_ deleting a staged file

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git add 04-testfile.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is up to date with 'origin/feature/31-amend_remove_reset'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   04-testfile.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git rm -f 04-testfile.md
rm 'challenge-010/04-testfile.md'

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is up to date with 'origin/feature/31-amend_remove_reset'.

```
> Remove files matching pathspec from the index, or from the working tree and the index.
> Git rm will not remove a file from just your > working directory. Remove files matching
> pathspec from the index, or from the working tree and the index. git rm will not remove
> a file from just your working directory.
> [more details](https://git-scm.com/docs/git-rm#_description)



**using _git clean_**
- [remove untracked file](https://git-scm.com/docs/git-clean)

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ touch 04-testfile.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is up to date with 'origin/feature/31-amend_remove_reset'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        04-testfile.md


Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git rm -f 04-testfile.md
fatal: pathspec '04-testfile.md' did not match any files

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git rm 04-testfile.md
fatal: pathspec '04-testfile.md' did not match any files

```

- both _git rm_ commands don't work!
- we have to use _git clean_


```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git clean -d -n
Would remove 04-testfile.md

```

- _git clean_ [-d= delete] [-n= dryrun] shows which file would be removed

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git clean -d -f 04-testfile.md
Removing 04-testfile.md

```
- _git clean -d -f <file>_ removes selectively the chosen file
 

# **amend**

**using commit --amend** 
- [undoing things](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)

1. stage this file: 00031-amend_remove_reset.md
2. commit this file: 00031-amend_remove_reset.md
3. assume i forgot to make and stage changes
4. update my last commit and replacing its result with new commit

```
$ git status
On branch feature/31-amend_remove_reset
Your branch is up to date with 'origin/feature/31-amend_remove_reset'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   00031-amend_remove_reset.md

no changes added to commit (use "git add" and/or "git commit -a")

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git add 00031-amend_remove_reset.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git commit -m 'testing --amend'
[feature/31-amend_remove_reset 95641ee] testing --amend
 1 file changed, 11 insertions(+), 1 deletion(-)

```
- using _git log -2_ for viewing the SHA1 of the commit i've just done

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git log -2
commit 95641eed00d703d13e3d0adcb138167e5289e63b (HEAD -> feature/31-amend_remove_reset)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Thu Oct 15 15:39:48 2020 +0200

    testing --amend

commit ce99e3bd64b2365817689281f364423e5acebf33 (origin/feature/31-amend_remove_reset)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Thu Oct 15 15:09:52 2020 +0200

    added description for remove and clean to 00031-amend_remove_reset.md

```

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ vi 00031-amend_remove_reset.md

```

- added the content above

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is ahead of 'origin/feature/31-amend_remove_reset' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   00031-amend_remove_reset.md

no changes added to commit (use "git add" and/or "git commit -a")

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git add 00031-amend_remove_reset.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git commit --amend -m 'corrected the --amend exercise'
[feature/31-amend_remove_reset 1630924] corrected the --amend exercise
 Date: Thu Oct 15 15:39:48 2020 +0200
 1 file changed, 54 insertions(+), 1 deletion(-)

```
- updated my last commit #95641eed00d703d13e3d0adcb138167e5289e63b and replaced it including 
- new commmit message with the one below

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git log -2
commit 1630924fc56a7cc46b54b825c9759e5cc7288c32 (HEAD -> feature/31-amend_remove_reset)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Thu Oct 15 15:39:48 2020 +0200

    corrected the --amend exercise

commit ce99e3bd64b2365817689281f364423e5acebf33 (origin/feature/31-amend_remove_reset)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Thu Oct 15 15:09:52 2020 +0200

    added description for remove and clean to 00031-amend_remove_reset.md

```
- again using _git log -2_ to review my work

# **reset**

**using git reset**
- [reset current HEAD to the specified state](https://git-scm.com/docs/git-reset)

- until now there are a lot of commits - most of them unnecessary:

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git log -8
commit 5d1ffd83db3e2fdae815e0d1c93b66958ce42e47 (HEAD -> feature/31-amend_remove_reset)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Thu Oct 15 15:51:42 2020 +0200

    added exercise --amend to 0031-amend_remove_reset.md

commit 1630924fc56a7cc46b54b825c9759e5cc7288c32
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Thu Oct 15 15:39:48 2020 +0200

    corrected the --amend exercise

commit ce99e3bd64b2365817689281f364423e5acebf33 (origin/feature/31-amend_remove_reset)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Thu Oct 15 15:09:52 2020 +0200

    added description for remove and clean to 00031-amend_remove_reset.md

commit 7a5b80a17ae835aa4b305835f333d96e7f9fd989
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Thu Oct 15 09:15:33 2020 +0200

    added content to 00031-amend_remove_reset.md for removing files

commit adde0be0ba81a288156a6954466855443c5dd599
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Wed Oct 14 19:50:19 2020 +0200

    deleted 01-testfile.md, updated 00031-amend_remove_reset.md

commit e6ff111917966d9d38c28ab1d728b8a5417601ab
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Wed Oct 14 19:33:15 2020 +0200

    created dummy-files for exercises

commit f45edc5440a40159bda8b4d04c76b8cb8e6a7380
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Wed Oct 14 19:31:14 2020 +0200

    created file for writing steps and results

commit d136b4bf0ae7bf4d82e527fab9d9d08ae083e85b (origin/develop, origin/HEAD, develop)
Author: Ragip Gashi <44840806+RagipGashi@users.noreply.github.com>
Date:   Wed Apr 8 15:30:56 2020 +0200

    Deleting .gitignore

```
- we want to reset the commit history in a 'clean' state.
- through _git log_ i know, that i want to go back 6 commits to #f45edc5440a40159bda8b4d04c76b8cb8e6a7380


```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git reset HEAD~6
Unstaged changes after reset:
M       challenge-010/00031-amend_remove_reset.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is behind 'origin/feature/31-amend_remove_reset' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   00031-amend_remove_reset.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        02-testfile.md
        03-testfile.md

no changes added to commit (use "git add" and/or "git commit -a")

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git log -3
commit f45edc5440a40159bda8b4d04c76b8cb8e6a7380 (HEAD -> feature/31-amend_remove_reset)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Wed Oct 14 19:31:14 2020 +0200

    created file for writing steps and results

commit d136b4bf0ae7bf4d82e527fab9d9d08ae083e85b (origin/develop, origin/HEAD, develop)
Author: Ragip Gashi <44840806+RagipGashi@users.noreply.github.com>
Date:   Wed Apr 8 15:30:56 2020 +0200

    Deleting .gitignore

commit 9434d88897cc35af9c81f2fd2a1edf162d50c4db
Merge: a8ebe5e 0e283e1
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 14:18:10 2020 +0200

    Merge branch 'develop' of https://github.com/software-developer-org/sandbox into develop

```
- now, commit f45edc5440a40159bda8b4d04c76b8cb8e6a7380 (HEAD -> feature/31-amend_remove_reset) is the **current** commit!

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git add 00031-amend_remove_reset.md

```
- adding my changes to satging area **but not commiting** it

```

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git push -f
Total 0 (delta 0), reused 0 (delta 0)
To https://github.com/software-developer-org/sandbox
 + ce99e3b...f45edc5 feature/31-amend_remove_reset -> feature/31-amend_remove_reset (forced update)

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ vi 00031-amend_remove_reset.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/31-amend_remove_reset)
$ git status
On branch feature/31-amend_remove_reset
Your branch is up to date with 'origin/feature/31-amend_remove_reset'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   00031-amend_remove_reset.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        02-testfile.md
        03-testfile.md

```
- after the _forced_ push my local and my remote branch are reseted to my first commit
- 0031-amend_remove_reset.md in the remote repository has no content
- the testfiles arent't commited or stage - like at beginning
- 0031-amend_remove_reset.md in my _local_ repository has still all the changes i made since starting this challenge

# last step

- staging this file
- commiting
- pushing to branch
- review work


