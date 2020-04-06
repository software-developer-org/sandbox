# **Remote Commands**


* **`$ git fetch `**

  * **Checks for updates on the origin without making any changes**


* **`$ git remote add -f --tags -t master -t develop <remotename> <remoteurl>`**

  * **`-f` stands for fetch `--tags` add tags `-t` fetch this branch**


* **`$ git show <remote>`**

  * **shows metadata of your remote**

  * **the command shows more specifics on a cloned remote**


* **`$ git branch --set-upstream-to origin/master`**

  * **Doesn't work on empty branches without commits**
  
  * **Altenative Commands are `--track` or `-u`**


* **`$ git merge origin/master --allow-unrelated-histories`**

  * **Allows merges mady by the 'recursive' strategy**

 
## **Use `git fetch` followed by `git merge` to first check changes and than pulling them to your lokal**

