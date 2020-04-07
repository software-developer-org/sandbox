# **Gitflow**

* **_Gitflow_ is a workflow that uses multiple types of branches to split development.**

## **Branch-Types**

* **Develop branch**

  * contains complete history with all commits
  * serves as integration branch for other branches
  * tracking branch for developers


* **Master Master**

  * reflects production environment
  * stores release history
  * fixes from hotfixes branch


* **Feature Branches**

  * parent: develop branch
  * short-living fork/branch
  * created on the latest develop branch and may be updated from develop all the time until completion
  * may be owned by specific developer
  * every story has its own feature branch
  * merged/rebased into develop branch (never to master)
  * merge/rebase may be done via pull request for code review
  * may be deleted after completion


* **Release Branch(es)**

  * parent: develop branch
  * short-living fork/branch
  * fork of develop branch based on defined release (based on features or date)
  * no (feature) further update from develop (unlike feature branches)
  * only commits for bug fixes and non-functional tasks (e.g. dokumentation)
  * every shipment/release will be tagged (e.g. 1.2.0-M1, 1.2.0-M2).
  * further shipments leads to further tags (e.g. 1.2.0-RELEASE)
  * every shipment merges release branch into master


* **Hotfix Branches**

  * parent: master
  * hotfixes are the only branches directly forking off of our master branch
  * merged into master and develop
  * may be deleted
