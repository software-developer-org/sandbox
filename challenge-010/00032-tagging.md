# tagging

**what is tagging**
- basicly marking points in a repository's history as important
 - e.g. release points
 - [Git Basics - Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
 - [tutorial for tagging](https://dev.to/neshaz/a-tutorial-for-tagging-releases-in-git-147e)

## basics commands

**`$ git tag`**
- lists all existing tags in alphabetical order

**`$ git tag -n`**
- lists all existing tags with message

**`$ git tag -l '<tagname>'`**
- searching a tag that matches the pattern
  - `$ git tag -l '<tagname.*>'` uses a wildcard  

## create tags

**annotated tags**
do store metadata
1. **`$ git tag -a <tagname> -m '<message>'`**
- creates tag for _latest_ commit
- contains tagger name
- email
- date and time
- tagging messsage
- running _git show <tagname>_:
  - diplays 1st the metadata above,
  - then the tagged commit

2. **`$ git tag -a <tagname> <GitID>`**
- creates tag for _specific_ commit, e.g. an older commit
  - after executing, editor opens for optional tag message
  - running _git show <tagname>_:
  - displays the metadata

**lightweight tags**
do not store metadata
1. **`$ git tag <tagname>`**
- basicly the commit checksum stored in a file
- creates a tag for the _current_ HEAD (latest commit)
- running _git show <tagname>_:
  - just shows the tagged commit
2. **`$ git tag <tagname> <GitID>`**
- creates a tag for a _specific_ commit without metadata

**deleting tags**
only local tags
1. **`$ git tag -d <tagname>`**
- already pushed tags
2. **`$ git push <location> :<tagname>`**

**sharing tags**
tags are _not_ automatically pushed to remotes
1. **`$ git push origin --tags`**
- pushes all tags to remote
2. **`$ git push origin <tagname>`**
- pushes a specified tag 


## testing tags

showing last 3 logs :
```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git log -3
commit 55f8e191f90658dfbdcb4871c07ad3679c3f07e7 (HEAD -> feature/32-tagging, origin/feature/32-tagging)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Fri Oct 16 09:54:22 2020 +0200

    #32 commit for tagging test 02

commit 2eb4513540870aec372f7ad17a5cca31fc54a10c
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Fri Oct 16 09:53:42 2020 +0200

    #32 commit for tagging test 01

commit bb19e62f961d51a4b7ff6dd9e47fbce6c38bd132
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Fri Oct 16 09:52:58 2020 +0200

    #32 initial commit
```

### using annotated tag with tag message for latest commit (#32 commit for tagging test 02)

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git tag tag.test.02 -m 'tagged latest commit'

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git tag
tag.test.02

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git show tag.test.02
tag tag.test.02
Tagger: Christian Kluge <christian.kluge@software-developer.org>
Date:   Fri Oct 16 11:47:00 2020 +0200

tagged latest commit

commit 55f8e191f90658dfbdcb4871c07ad3679c3f07e7 (HEAD -> feature/32-tagging, tag: tag.test.02, origin/feature/32-tagging)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Fri Oct 16 09:54:22 2020 +0200

    #32 commit for tagging test 02

diff --git a/challenge-010/02-tagging_test.md b/challenge-010/02-tagging_test.md
new file mode 100644
index 0000000..500a3b1
--- /dev/null
+++ b/challenge-010/02-tagging_test.md
@@ -0,0 +1 @@
+**that's all folks**

```

### using annotated tag for specific commit (#32 initial commit)

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git tag -a tag.initial bb19e62f961d51a4b7ff6dd9e47fbce6c38bd132

```
- entered tag message in editor

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git show tag.initial
tag tag.initial
Tagger: Christian Kluge <christian.kluge@software-developer.org>
Date:   Fri Oct 16 11:54:15 2020 +0200

tagged initial commit

commit bb19e62f961d51a4b7ff6dd9e47fbce6c38bd132 (tag: tag.initial)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Fri Oct 16 09:52:58 2020 +0200

    #32 initial commit

diff --git a/challenge-010/00032-tagging.md b/challenge-010/00032-tagging.md
new file mode 100644
index 0000000..7cce668
--- /dev/null
+++ b/challenge-010/00032-tagging.md
@@ -0,0 +1,41 @@
+# tagging
+
+**what is tagging**
+- basicly marking points in a repository's history as important
+ - e.g. release points
+ - [Git Basics Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
+ - [tutorial for tagging](https://dev.to/neshaz/a-tutorial-for-tagging-releases-in-git-147e)
+
+## basics commands
+
+**`$ git tag`**
+- lists all existing tags in alphabetical order
+
+**`$ git tag -l <tagname>`**
+- searching a tag that matches the pattern
+
+## create tags
+
+1. **annotated tags**
+**`$ git tag <tagname> -m '<message>'`**
+- contains tagger name
+- email
+- date and time
+- tagging messsage
+- running _git show <tagname>_:
+ - diplays 1st the informations above,
+ - than the tagged commit
+
+
+2. **lightweight tags**
+**`$ git tag <tagname>`**
+- basicly the commit checksum stored in a file
+- creates a tag for the current HEAD
+- running _git show< tagname>_:
+ - just shows the tagged commit
+
+3. **tagging later**
+**`$ git tag -a <tagname> <GitID>`**
+- its possible to pick a commit from history and tag it
+- running _git show <tagname>_:
+ - displays same informations like an annotated tag

```

### using lightweight tag for specific commit (#32 commit for tagging test 01)

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git tag tag.test.01 2eb4513540870aec372f7ad17a5cca31fc54a10c

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git show tag.test.01
commit 2eb4513540870aec372f7ad17a5cca31fc54a10c (tag: tag.test.01)
Author: Christian Kluge <christian.kluge@software-developer.org>
Date:   Fri Oct 16 09:53:42 2020 +0200

    #32 commit for tagging test 01

diff --git a/challenge-010/01-tagging_test.md b/challenge-010/01-tagging_test.md
new file mode 100644
index 0000000..b5c4e54
--- /dev/null
+++ b/challenge-010/01-tagging_test.md
@@ -0,0 +1 @@
+**hello world**

```

### using the basic commands 

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git tag
tag.initial
tag.test.01
tag.test.02
taggin-is-easy

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git tag -n
tag.initial     tagged initial commit
tag.test.01     #32 commit for tagging test 01
tag.test.02     tagged latest commit
taggin-is-easy  #19 all about tagging completed

Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git tag -l 'tag.*'
tag.initial
tag.test.01
tag.test.02

```

### pushing to remote

```
Christian Kluge@Laptop-CK MINGW64 ~/sandbox/challenge-010 (feature/32-tagging)
$ git push origin --tags
Enumerating objects: 2, done.
Counting objects: 100% (2/2), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 333 bytes | 333.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0)
To https://github.com/software-developer-org/sandbox
 * [new tag]         tag.initial -> tag.initial
 * [new tag]         tag.test.01 -> tag.test.01
 * [new tag]         tag.test.02 -> tag.test.02

```

