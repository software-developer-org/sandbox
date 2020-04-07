# **Branches**


* **The `$ git cat-fíle -p <gitid>` command sows more information**


```bash 

Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/23-branches)
$ git cat-file -p 9fba6b
tree 8e85e2f73f673fda99876c792f1bc1652fbd98b5
parent 9434d88897cc35af9c81f2fd2a1edf162d50c4db
author RouvenGonzalez <rouvengonzalez@gmail.com> 1586249751 +0200
committer RouvenGonzalez <rouvengonzalez@gmail.com> 1586249751 +0200

#23 initial commit

Medion AKOYA@DESKTOP-76ECOJG MINGW64 ~/Desktop/Rouven/Programmieren/Gitspace/sandbox/challenge-010 (feature/23-branches)
$ git cat-file -p  8e85e2f73f673fda99876c792f1bc1652fbd98b5
100644 blob 4f40bcb4582f574c5fef332c1695a4894fa68ed1    .gitignore
100644 blob f288702d2fa16d3cdf0035b15a9fcbc552cd88e7    LICENSE
100644 blob d038ba0f6f56f83dede922452052e2ae0061663a    README.md
040000 tree 9bdb3f3786435e208e2ef0ba8a81f06e57c4aef2    challenge-010
040000 tree ebe0326d9241016f3133fdf9672970ca178c640c    challenge-020
040000 tree ebe0326d9241016f3133fdf9672970ca178c640c    challenge-030
040000 tree ebe0326d9241016f3133fdf9672970ca178c640c    challenge-040
040000 tree ebe0326d9241016f3133fdf9672970ca178c640c    challenge-050
040000 tree ebe0326d9241016f3133fdf9672970ca178c640c    challenge-060
040000 tree ebe0326d9241016f3133fdf9672970ca178c640c    challenge-070
040000 tree ebe0326d9241016f3133fdf9672970ca178c640c    challenge-080
040000 tree ebe0326d9241016f3133fdf9672970ca178c640c    challenge-090
100644 blob 270c611ee72c567bc1b2abec4cbc345bab9f15ba    myfile.md

```

* **Our tree object basically reflects our root folder**

* **You can trace your branches back to the -root_ like this**

