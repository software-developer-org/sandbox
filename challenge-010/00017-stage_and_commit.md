# **Create New File**

RagipGashisMBP:challenge-010 ragipgashi$ git checkout develop
Switched to branch 'develop'
Your branch is up-to-date with 'origin/develop'.

RagipGashisMBP:challenge-010 ragipgashi$ touch 00017-stage_and_commit.md
RagipGashisMBP:challenge-010 ragipgashi$ git status
On branch feature/17-stage_and_commit
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	00017-stage_and_commit.md

nothing added to commit but untracked files present (use "git add" to track)


## **Stage Output**

RagipGashisMBP:challenge-010 ragipgashi$ git add 00017-stage_and_commit.md 
RagipGashisMBP:challenge-010 ragipgashi$ git status

On branch feature/17-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   00017-stage_and_commit.md

RagipGashisMBP:challenge-010 ragipgashi$ 


## **Diff**

*The git diff command cannot show anything as long as there has no staged file to compare with*



# **Update Content**

*This is a **history** of bash commands*


## **Checkout Status**

RagipGashisMBP:challenge-010 ragipgashi$ git status
On branch feature/17-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   00017-stage_and_commit.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   00017-stage_and_commit.md

RagipGashisMBP:challenge-010 ragipgashi$

### Explanation:
 
*This happends because we have modified the file with some contents and it needs to be staged and than commited.*


## **Git Diff**

RagipGashisMBP:challenge-010 ragipgashi$ git diff
diff --git a/challenge-010/00017-stage_and_commit.md b/challenge-010/00017-stage_and_commit.md
index ee3b157..791aadd 100644
--- a/challenge-010/00017-stage_and_commit.md
+++ b/challenge-010/00017-stage_and_commit.md
@@ -3,6 +3,7 @@
 RagipGashisMBP:challenge-010 ragipgashi$ git checkout develop
 Switched to branch 'develop'
 Your branch is up-to-date with 'origin/develop'.
+
 RagipGashisMBP:challenge-010 ragipgashi$ touch 00017-stage_and_commit.md
 RagipGashisMBP:challenge-010 ragipgashi$ git status
 On branch feature/17-stage_and_commit
@@ -12,3 +13,52 @@ Untracked files:
        00017-stage_and_commit.md
 
 nothing added to commit but untracked files present (use "git add" to track)

### Expnanation:

*Git diff command shows nothing just like in the previous case, there is no file to compare with*


## **Stage Output**

RagipGashisMBP:challenge-010 ragipgashi$ git add 00017-stage_and_commit.md 
RagipGashisMBP:challenge-010 ragipgashi$ git status

On branch feature/17-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

       new file:   00017-stage_and_commit.md

RagipGashisMBP:challenge-010 ragipgashi$ 

### Explanation: 

*The command **git status** shows only one version of the file, that means that this file is up to date and staged, so ready to be commited.*


# **Update Contend Again**

*This is some other content to see the difference*


## **Check Status**

RagipGashisMBP:challenge-010 ragipgashi$ git status
On branch feature/17-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   00017-stage_and_commit.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   00017-stage_and_commit.md

RagipGashisMBP:challenge-010 ragipgashi$ 

### Explanation:

*This shows two versions of the file, means: we have updated the file but it is not staged*


## **Git Diff**

*The diff command now shows the difference between the staged file and modified file.*


## **Status after Staging**

RagipGashisMBP:challenge-010 ragipgashi$ git add 00017-stage_and_commit.md 
RagipGashisMBP:challenge-010 ragipgashi$ git status
On branch feature/17-stage_and_commit
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   00017-stage_and_commit.md

RagipGashisMBP:challenge-010 ragipgashi$ 

## Explanation:

*Now the file is updated and everything is staged, ready to be commited. That's why ony one file remains*


## **Check Status After Commit**

RagipGashisMBP:challenge-010 ragipgashi$ git status
On branch feature/17-stage_and_commit
nothing to commit, working tree clean
RagipGashisMBP:challenge-010 ragipgashi$ 

*Now the file is ready to be uploaded to our remote repository with the command **git push**. The **git status** command now shows the message 'Your branch is up to date with origin'.


