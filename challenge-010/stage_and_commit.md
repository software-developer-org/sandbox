# **Create New File**

```
Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ touch stage_and_commit.md

Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git status
On branch feature/13-stage_and_commit
Your branch is up to date with 'origin/feature/13-stage_and_commit'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        stage_and_commit.md

nothing added to commit but untracked files present (use "git add" to track)
```

## **Stage Output**

```
Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git add stage_and_commit.md

Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git status
On branch feature/13-stage_and_commit
Your branch is up to date with 'origin/feature/13-stage_and_commit'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   stage_and_commit.md
```

## **Diff**

```
Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git diff
```

The git diff command shows nothing because it has no staged file too compare with.


# **Update Content**

**What happens after we make some changes?**


## **Check Status**

```
Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git status
On branch feature/13-stage_and_commit
Your branch is up to date with 'origin/feature/13-stage_and_commit'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   stage_and_commit.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   stage_and_commit.md
```

The status command now shows 2 versions of our file.
One is the staged version and the other one is the modified one that's not staged.


## **Git Diff**

```
Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git diff
diff --git a/challenge-010/stage_and_commit.md b/challenge-010/stage_and_commit.md
index d3785e0..6d3a108 100644
--- a/challenge-010/stage_and_commit.md
+++ b/challenge-010/stage_and_commit.md
@@ -16,7 +16,7 @@ Untracked files:
 nothing added to commit but untracked files present (use "git add" to track)


-**Stage Output**
+## **Stage Output**


 Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
@@ -32,7 +32,7 @@ Changes to be committed:
         new file:   stage_and_commit.md


-**Diff**
+## **Diff**

 
 Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
@@ -40,3 +40,34 @@ $ git diff
 

 The git diff command shows nothing because it has no staged file too compare with.
+
+
+# **Update Content**
+
+**What happens after we make some changes?**
+
+
+## **Check Status**
+
+
+
+Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
+$ git status
+On branch feature/13-stage_and_commit
+Your branch is up to date with 'origin/feature/13-stage_and_commit'.
+
+Changes to be committed:
+  (use "git restore --staged <file>..." to unstage)
+        new file:   stage_and_commit.md
+
+Changes not staged for commit:
+  (use "git add <file>..." to update what will be committed)
+  (use "git restore <file>..." to discard changes in working directory)
+        modified:   stage_and_commit.md
+
+
+The status command now shows 2 versions of our file.
+One is the staged version and the other one is the modified one that's not staged.
+
+
+## **Git Diff**
+
```

The git diff command now shows the difference between the staged file and our modified one.

## **Status after Staging**

```
Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git status
On branch feature/13-stage_and_commit
Your branch is up to date with 'origin/feature/13-stage_and_commit'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   stage_and_commit.md
```

now the staged file was updatet with the modifications so only one version of our file remains.

# **Now Another Update**

## **Git Status**

```
Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git status
On branch feature/13-stage_and_commit
Your branch is up to date with 'origin/feature/13-stage_and_commit'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   stage_and_commit.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   stage_and_commit.md
```

Again a new modified version exists.

## **Diff**

```
Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
$ git diff
diff --git a/challenge-010/stage_and_commit.md b/challenge-010/stage_and_commit.md
index caccaca..b18eb05 100644
--- a/challenge-010/stage_and_commit.md
+++ b/challenge-010/stage_and_commit.md
@@ -136,4 +136,40 @@ index d3785e0..6d3a108 100644

 The git diff command now shows the difference between the staged file and our modified one.

+## **Status after Staging**
+
+
+Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
+$ git status
+On branch feature/13-stage_and_commit
+Your branch is up to date with 'origin/feature/13-stage_and_commit'.
+
+Changes to be committed:
+  (use "git restore --staged <file>..." to unstage)
+        new file:   stage_and_commit.md
+
+
+now the staged file was updatet with the modifications so only one version of our file remains.
+
+
diff --git a/challenge-010/stage_and_commit.md b/challenge-010/stage_and_commit.
diff --git a/challenge-010/stage_and_commit.md b/challenge-010/stage_and_commit.
md
index caccaca..b18eb05 100644
--- a/challenge-010/stage_and_commit.md
+++ b/challenge-010/stage_and_commit.md
@@ -136,4 +136,40 @@ index d3785e0..6d3a108 100644

 The git diff command now shows the difference between the staged file and our m
odified one.

+## **Status after Staging**
+
+
+Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sa
ndbox/challenge-010 (feature/13-stage_and_commit)
+$ git status
+On branch feature/13-stage_and_commit
+Your branch is up to date with 'origin/feature/13-stage_and_commit'.
+
+Changes to be committed:
+  (use "git restore --staged <file>..." to unstage)
+        new file:   stage_and_commit.md
+
+
+now the staged file was updatet with the modifications so only one version of our file remains.
+
+# **Now Another Update**
+
+## **Git Status**
+
+
+Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/13-stage_and_commit)
+$ git status
+On branch feature/13-stage_and_commit
+Your branch is up to date with 'origin/feature/13-stage_and_commit'.
+
+Changes to be committed:
+  (use "git restore --staged <file>..." to unstage)
+        new file:   stage_and_commit.md
+
+Changes not staged for commit:
+  (use "git add <file>..." to update what will be committed)
+  (use "git restore <file>..." to discard changes in working directory)
+        modified:   stage_and_commit.md
+
+
+Again a new modified version exists.
```

And diff shows the difference between them.


# **Finaly**

After staging the file for the last time it is ready too commit.
Wich means we upload it too our remote repository whit the command **git push**.
The status command now shows the message 'Your branch is up to date with origin'.

