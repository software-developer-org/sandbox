# Git_Started_Exercies


- **`git remote`**

	- *List the remote connections you have to other repositories.*


- **`git remote -v`**

	- *List the remote connections, include the URL for fetch connection.*


- **`git remote add <name> <url>`**

	- *Create a new connection to a remote repository.*


- **´git remote rm <name>`**

	- *Remove the connection to the remote repository called <name>*


- **´git remote rename <old-name> <new-name>**

	- *Rename a remote connection from <old-name> to <new-name>*


- **`git remote add -f --tags -t master -t develop <remotename> <remoteurl>`**

 	- **`-f` stands for fetch `--tags` add tags `-t` fetch this branch**


- **`git show <remote>`**

	- *Outputs high-level information about the remote.*

- **`git branch --set-upstream-to origin/master.**

  	- * Doesn't work on empty branches without commits*
  
 	- *Altenative are **`--track` or `-u`** Commands*

- **`git merge origin/master --allow-unrelated-histories`**

	- *Allows merges made by the `recursive` strategy*

## Use `git fetch` followed by `git merge`


### Now pull to the local repository.

