# **Logs and Commits

## **Last 3 Logs**

RagipGashisMBP:challenge-010 ragipgashi$ git log -3
commit 57cb5d79afc5971c297b25a7c1b76cd427db6996
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Mon Apr 6 00:56:38 2020 +0200

    #17 Stage and Commit Completed

commit 9434d88897cc35af9c81f2fd2a1edf162d50c4db
Merge: a8ebe5e 0e283e1
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 14:18:10 2020 +0200

    Merge branch 'develop' of https://github.com/software-developer-org/sandbox into develop

commit a8ebe5efe2a6761bc366300e867359d5a7c01af6
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 12:05:49 2020 +0200

    Ignoring Files with DS_Store
RagipGashisMBP:challenge-010 ragipgashi$ 


## **Log 3 Explanation:**

commit a8ebe5efe2a6761bc366300e867359d5a7c01af6

* **Shows the Author and the Date 

Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 12:05:49 2020 +0200

* **Commit message**

Ignoring Files with DS_Store


## **Log 3 Changes**

RagipGashisMBP:challenge-010 ragipgashi$ git show a8ebe
commit a8ebe5efe2a6761bc366300e867359d5a7c01af6
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 12:05:49 2020 +0200

    Ignoring Files with DS_Store


diff --git a/challenge-010/.gitignore b/challenge-010/.gitignore
new file mode 100644
index 0000000..4f40bcb
--- /dev/null
+++ b/challenge-010/.gitignore
@@ -0,0 +1,2 @@
+# Ignore DS_Store files
+**/*.DS_Store
RagipGashisMBP:challenge-010 ragipgashi$ 

* **Explanation:**

*Shows the commit I have done in Sandbox for adding a .gitignore file*


## **Log 2 Changes**

RagipGashisMBP:challenge-010 ragipgashi$ git show 9434d
commit 9434d88897cc35af9c81f2fd2a1edf162d50c4db
Merge: a8ebe5e 0e283e1
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Fri Apr 3 14:18:10 2020 +0200

    Merge branch 'develop' of https://github.com/software-developer-org/sandbox into develop

RagipGashisMBP:challenge-010 ragipgashi$ 

* **Explanation:**

*Shows the merge I've done*


## **Log 1 Changes**

RagipGashisMBP:challenge-010 ragipgashi$ git show 57cb5d
commit 57cb5d79afc5971c297b25a7c1b76cd427db6996
Author: Ragip Gashi <ragipgashi@gmial.com>
Date:   Mon Apr 6 00:56:38 2020 +0200

    #17 Stage and Commit Completed

diff --git a/challenge-010/00017-stage_and_commit.md b/challenge-010/00017-stage_and_commit.md
new file mode 100644
index 0000000..83ee320
--- /dev/null
+++ b/challenge-010/00017-stage_and_commit.md
@@ -0,0 +1,166 @@
+# **Create New File**
+
+RagipGashisMBP:challenge-010 ragipgashi$ git checkout develop
+Switched to branch 'develop'
+Your branch is up-to-date with 'origin/develop'.
+
+RagipGashisMBP:challenge-010 ragipgashi$ touch 00017-stage_and_commit.md
+RagipGashisMBP:challenge-010 ragipgashi$ git status
+On branch feature/17-stage_and_commit
+Untracked files:




