# [Distributed Git workflows](https://git-scm.com/book/en/v2/Distributed-Git-Distributed-Workflows)
1. Delimination to a [centralized version control](https://www.atlassian.com/blog/software-teams/version-control-centralized-dvcs) (VCS) 
- When you’re working with a centralized verison control system, your workflow for adding a new feature or fixing a bug in your project will usually look something like this:

   - Pull down any changes other people have made from the central server.
   - Make your changes, and make sure they work properly.
   - Commit your changes to the central server, so other programmers can see them.

2. Git is a distributed version control system (DVCS) 

- These systems do not necessarily rely on a central server to store all the versions of a project’s files. Instead, every developer “clones” a copy of a repository and has the full history of the project on their **own** hard drive. This copy (or “clone”) has **all** of the metadata of the original(= most users known it as `origin`).

   - Performing actions other than pushing and pulling changesets is extremely fast because the tool only needs to access the hard drive, not a remote server.
   - Committing new changesets can be done locally without anyone else seeing them. Once you have a group of changesets ready, you can push all of them at once.
   - Everything but pushing and pulling can be done without an internet connection. So you can work on a plane, and you won’t be forced to commit several bugfixes as one big changeset.
   - Since each programmer has a full copy of the project repository, they can share changes with one or two other people at a time if they want to get some feedback (i.e. in subteams) before showing the changes to everyone.


## conclusion of [A successfull Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)

**Main Branches**
- **have an infinite lifetime**

**1. _master_**
  
- stores the official release history (= an abridged project history)
- all commits in this branch should be [tagged](https://git-scm.com/book/en/v2/Git-Basics-Tagging) with a version number
- gets fixes from the hotfix branch (see below)
- the source code of `HEAD` (= your 'pointer' in this branch) always reflects the current production state (= the version you delivered to your client)
- shown as `origin/master` (= the remote tracking branch)

**2. _develop_**
  
- containes the complete project history 
- should be based on, and track, the master branch
  - `$ git branch develop` creates local branch based on master
  - `$ git push -u origin develop` pushed to server
- the source code of `HEAD` reflects the latest development changes for the next release
- shown as `origin/develop` (= the remote tracking branch)
- can be seen as an 'integration branch' for supporting branches (see below)
- when considered as stable it is [merged](https://git-scm.com/docs/git-merge) back into master branch
  - _this is a production release! and has to be tagged with a release number_

**Supporting Branches**
- **have a limited lifetime**

**1. _feature_**

- parent branch: `develop`
- naming convention - anything except: master, develop, release-... or hotfix-...
  - each feature should have its own branch
    ```
    $ git checkout develop
    Switched to branch 'develop'
    Your branch is up to date with 'origin/develop'.

    $ git checkout -b feature/feature_xyz
    Switched to branch 'feature/feature_xyz'

    ```
 - created on the latest develop branch
 - can be merged from develop (i.e. hotfixes) until feature is finished 
 - **must** merge back to develop (**never** to master !!)
   - merge maybe done by [pull request](https://guides.github.com/introduction/flow/) (=reviewing/commentating/rejecting/approving your work by other teammates/developers)
 - maybe deleted after feature is finished

**2. _release_**

- parent branch: `develop`
- naming convention: release-...
- branched off from develop, _after all features that are targeted for the release are merged into develop_
  - merging large features directly into `release` is strongly forbidden! 
  - _exactly_ at the start, the release branch gets assigned a version number!
    ```
    $ git checkout -b release-v1.0
    Switched to branch 'release-v1.0'  
  
    ```
  - i.e. v1.0.1, v1.0.2, v1.2, ....
  - naming is carried out by the project's rules of [version number](https://en.wikipedia.org/wiki/Software_versioning) bumping, (i.e. major.minor.patch)
- **must** merge back to develop **and** master
- maybe removed after release

**3. _hotfix_**

- parent branch: `master`
- naming convention: hotfix-...
- needed to react immediately to an undesired state of a live production version (current used version in master branch)
  - when a critical bug has to be solved a team can do a quick production fix without using the develop branch
- **must** merge back into master **and** develop (it has to be included in the next release)
- maybe removed after merging 


### souces used:
- [Git Pro Book](https://git-scm.com/book/en/v2/Distributed-Git-Distributed-Workflows)
- [atlassian](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [nvie.com](https://nvie.com/posts/a-successful-git-branching-model/)
- [wikipedia](https://en.wikipedia.org/wiki/Software_versioning)
