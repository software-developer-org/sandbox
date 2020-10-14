# show last 3 logs
```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git log -3
commit b11489b1795e3124bc36bee7d74a8e5bc2246542 (HEAD -> feature/29-stage_and_commit, origin/feature/29-stage_and_commit)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Wed Oct 14 11:26:07 2020 +0200

    #29-stage_and_commit completed!

commit d136b4bf0ae7bf4d82e527fab9d9d08ae083e85b (origin/develop, origin/HEAD, feature/30-logs_and_commits, develop)
Author: Ragip Gashi <44840806+RagipGashi@users.noreply.github.com>
Date:   Wed Apr 8 15:30:56 2020 +0200

    Deleting .gitignore

commit 9434d88897cc35af9c81f2fd2a1edf162d50c4db
Merge: a8ebe5e 0e283e1
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 14:18:10 2020 +0200

    Merge branch 'develop' of https://github.com/software-developer-org/sandbox into develop

```

# explain log 3
```
commit 9434d88897cc35af9c81f2fd2a1edf162d50c4db
```
* shows Git ID

```
Merge: a8ebe5e 0e283e1

```
* user merged two commits

```
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 14:18:10 2020 +0200

```

*  name and email author

```
    Merge branch 'develop' of https://github.com/software-developer-org/sandbox into develop


```
* commit message


# show log 3 changes

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git show 9434d88897cc35af9c81f2fd2a1edf162d50c4db
commit 9434d88897cc35af9c81f2fd2a1edf162d50c4db
Merge: a8ebe5e 0e283e1
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 14:18:10 2020 +0200

    Merge branch 'develop' of https://github.com/software-developer-org/sandbox into develop

```

# explain log 2

```
commit d136b4bf0ae7bf4d82e527fab9d9d08ae083e85b (origin/develop, origin/HEAD, feature/30-logs_and_commits, develop)

```
* beside the SHA1 it shows the origin/HEAD branch

# show changes log 2
```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git show d136b4bf0ae7bf4d82e527fab9d9d08ae083e85b
commit d136b4bf0ae7bf4d82e527fab9d9d08ae083e85b (origin/develop, origin/HEAD, feature/30-logs_and_commits, develop)
Author: Ragip Gashi <44840806+RagipGashi@users.noreply.github.com>
Date:   Wed Apr 8 15:30:56 2020 +0200

    Deleting .gitignore

diff --git a/challenge-010/.gitignore b/challenge-010/.gitignore
deleted file mode 100644
index 4f40bcb..0000000
--- a/challenge-010/.gitignore
+++ /dev/null
@@ -1,2 +0,0 @@
-# Ignore DS_Store files
-**/*.DS_Store

```

# explain log 1
```
commit b11489b1795e3124bc36bee7d74a8e5bc2246542 (HEAD -> feature/29-stage_and_commit, origin/feature/29-stage_and_commit)

```
* at the moment, user is on local branch:
`feature/29-stage_and_commit`
* remote:
`origin/feature/29-stage_and_commit`



# show changes log 1
```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
$ git show b11489b1795e3124bc36bee7d74a8e5bc2246542
commit b11489b1795e3124bc36bee7d74a8e5bc2246542 (HEAD -> feature/29-stage_and_commit, origin/feature/29-stage_and_commit)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Wed Oct 14 11:26:07 2020 +0200

    #29-stage_and_commit completed!

diff --git a/challenge-010/00029-new_file.md b/challenge-010/00029-new_file.md
new file mode 100644
index 0000000..e22846a
--- /dev/null
+++ b/challenge-010/00029-new_file.md
@@ -0,0 +1,242 @@
+# create new file
+
+```
+Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
+$ touch 00029-new_file.md
+
+Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
+$ git status
+On branch feature/29-stage_and_commit
+Untracked files:
+  (use "git add <file>..." to include in what will be committed)
+
+        00029-new_file.md
+
+nothing added to commit but untracked files present (use "git add" to track)
+```
+
+
+* created new file, _git status_ shows the the untracked file
+
+
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
+
+# update content
+
+
+```
+Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/29-stage_and_commit)
+$ git status
+On branch feature/29-stage_and_commit
+Changes to be committed:
+  (use "git reset HEAD <file>..." to unstage)
+
+        new file:   00029-new_file.md
+
+Changes not staged for commit:
+  (use "git add <file>..." to update what will be committed)
:

```

