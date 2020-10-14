# create new file

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ touch 00029-new_file.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git status
On branch feature/29-stage_and_commit
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        00029-new_file.md

nothing added to commit but untracked files present (use "git add" to track)
```


* created new file, _git status_ shows the the untracked file


```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git add 00029-new_file.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git status
On branch feature/29-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   00029-new_file.md


Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git diff

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$
```

* the file is now staged and tracked
* because its a new file and it wasn't staged before, _git diff_ can't compare it to a former version

# update content


``` 
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git status
On branch feature/29-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   00029-new_file.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   00029-new_file.md
```


* after staging the file we added content, so we **modified** it, and _git status_ shows two versions
 * `new file:   00029-new_file.md staged` - excluding the new modifcation
 * `modified:   00029-new_file.md unstaged` - including the new modification


```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git diff
diff --git a/challenge-010/00029-new_file.md b/challenge-010/00029-new_file.md
index d883735..5fc8a29 100644
--- a/challenge-010/00029-new_file.md
+++ b/challenge-010/00029-new_file.md
@@ -17,5 +17,28 @@ nothing added to commit but untracked files present (use "git add" to track)

 * created new file, _git status_ shows the the untracked file

+```
+Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
+$ git add 00029-new_file.md
+
+Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
+$ git status
+On branch feature/29-stage_and_commit
+Changes to be committed:
+  (use "git reset HEAD <file>..." to unstage)
+
+        new file:   00029-new_file.md
+
+
+Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
+$ git diff
+
+Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
+$
+```
+
+* the file is now staged and tracked
+* because its a new file and it wasn't staged before, _git diff_ can't compare it to a former version

+# update content
```

* now _git diff_ can compare the staged and the unstaged file and shows the insertions/deletions bewtween the two versions


```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git add 00029-new_file.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git status
On branch feature/29-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   00029-new_file.md
```

* after using _git add_ the status shows the latest version, including the latest modifications

# update content again


```
$ git status
On branch feature/29-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   00029-new_file.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   00029-new_file.md


Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git diff
diff --git a/challenge-010/00029-new_file.md b/challenge-010/00029-new_file.md
index 6b36cbf..b188187 100644
--- a/challenge-010/00029-new_file.md
+++ b/challenge-010/00029-new_file.md
@@ -122,4 +122,7 @@ Changes to be committed:

  after using _git add_ the status shows the latest version, including the latest modifications

+# update content again
+
+


Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git add 00029-new_file.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git status
On branch feature/29-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   00029-new_file.md
```


* again, the same cycle like above

<<<<<<< HEAD
=======
<<<<<<< HEAD
>>>>>>> e221c4ed806cc8d0b273d43584930f88c624f2bd
# output after staging, commiting and pushing

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git add 00029-new_file.md

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git commit -m '#29-stage_and_commit'
[feature/29-stage_and_commit bc7d545] #29-stage_and_commit
 1 file changed, 172 insertions(+)
 create mode 100644 challenge-010/00029-new_file.md
``` 
* we staged the file
* we commited it, and added a message


```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git status
On branch feature/29-stage_and_commit
nothing to commit, working tree clean

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git push -u origin feature/29-stage_and_commit
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 1.22 KiB | 1.22 MiB/s, done.
Total 4 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'feature/29-stage_and_commit' on GitHub by visiting:
remote:      https://github.com/software-developer-org/sandbox/pull/new/feature/29-stage_and_commit
remote:
To https://github.com/software-developer-org/sandbox
  [new branch]      feature/29-stage_and_commit -> feature/29-stage_and_commit
Branch 'feature/29-stage_and_commit' set up to track remote branch 'feature/29-stage_and_commit' from 'origin'.

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git status
On branch feature/29-stage_and_commit
Your branch is up to date with 'origin/feature/29-stage_and_commit'.

nothing to commit, working tree clean
```


```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git status
On branch feature/29-stage_and_commit
Your branch is up to date with 'origin/feature/29-stage_and_commit'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   00029-new_file.md

no changes added to commit (use "git add" and/or "git commit -a")

```

* to show the output of _git commit_, _git push_ and _git status_ **after** using these commands, the file had to be modified again

