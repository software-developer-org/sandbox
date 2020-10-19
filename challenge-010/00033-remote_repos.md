**for this challenge you need to know about**
   - [working with remotes](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes)
   - [remote branches](https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches)


# remote commands 

**`$ git remote`**
- list set of repositories (= remotes) whose branches are tracked

**`$ git remote -v`**
- shows URL after remote name

**`$ git remote add <remotename> <url>`**
- create a new remote track with the name <remotename> and the repository is in <url>
  - just using _git remote add <url>_, the remotename will be _origin_ by default

**`$ git remote rm <remotename>`**
- does not delete the remote repository from the server. It simply removes the remote and its references from your local repository

**`$ git remote rename`**
- renames your remote i.e. from origin to upstream

**`$ git remote add -f --tags -t <branch-one> -t <branch-two> <remotename> <url>`**
- '-f' fetching immediately after remote information is set up
- '--tags' imports every tag from the remote repository
- '-t <branch> is used to track a specific branch instead of all branches on the remote repository
  - this option can be used multiple times
- <remotename> the name you choose for the remote tracking
- <url> where the repository you want to track is located

**`$ git branch --set-uptsream <remotename>/<branch>`**
- configure which branch on the remote repo is the 'upstream branch' (= <remotename>/<branch>), which is going to be tracked from the local branch (= master, ...)
  - there will be a fatel error, as long as this is an empty branch without commits
  - one solution: just commit something
  - after commiting the local branch and the remote branch will be divergent (showed by _git status_)
  - first we have to merge the <remotename>/<branch> with the local branch using
  - `$ git merge <remotename>/<branch> --allow-unrelated-histories`
  - then we can use _git push_ to push to the configured remote branch

**`$ git checkout --track <remotename>/<branch>`**
- creating a new local branch, based on the the remote branch
  - by default, Git uses the same name for the local branch as given in the remote
  - the new local branch will start, pointing to the latest commit, like in the based remote branch
