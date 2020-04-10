# Branches

- *The `$ git cat-file -p <gitid>`command shows the informations about the file*

```bash

$ git cat-file -p f6c25d
tree 98d9171528a0acdc1ca646cf13a751a0b1c2e63e
parent 4d717abed9931848443c81e1819d6516ca2f69c1
author Ragip Gashi <ragipgashi@gmial.com> 1586427317 +0200
committer Ragip Gashi <ragipgashi@gmial.com> 1586427317 +0200

#24 Remote Repos
$ git cat-file -p 98d9171528a0acdc1ca646cf13a751a0b1c2e63e
100644 blob 4f40bcb4582f574c5fef332c1695a4894fa68ed1    .gitignore
100644 blob f288702d2fa16d3cdf0035b15a9fcbc552cd88e7    LICENSE
100644 blob d038ba0f6f56f83dede922452052e2ae0061663a    README.md
040000 tree 891c012b2616a1da1e37131f75a4e14d63ebf353    challenge-010
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

## Explanation:

        - *The tree object basically reflects the root folder*

**To trace the branches back to the root use `-root_`**


 
 

