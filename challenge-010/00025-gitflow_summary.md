# Gitflow


**The following branching model is based on the Gitflow workflow.**


The Gitflow worlflow has three type of branches:


- **Develop branch**

        - contains complete history with all commits
        - serves as integration branch for other branches (feature, release, hot fix branches)
        - tracking branch for developers


- **Master Master**

        - reflects production environment
        - stores release history
        - fixes from hotfixes branch


- **Feature Branches**

        - parent: develop branch
        - short-living fork/branch
        - created on the latest develop branch and may be updated from all the time until completion
        - may be owned by specific developer
        - every story has its own feature branch
        - merged/rebased into develop branch (never to master)
        - merge/rebase may be done via pull request for code review
        - may be deleted after completion


- **Release Branch(es)**

        - parent: develop branch
        - short-living fork/branch
        - fork of develop branch based on defined release (based on features or date)
        - no (feature) further update from develop (unlike feature branches)
        - only commits for bug fixes and non-functional tasks (e.g. documentation)
        - every shipment/release will be tagged (e.g. 1.2.0-M1, 1.2.0-M2).
	- further shipments leads to further tags (e.g.1.2.0-RELEASE)
        - every shipment merges release branch into master


- **Hotfix Branches)**

        - parent: master
        - hofixes are the only branches directly forking of our master branch
        - merged into master and develop
        - may be deleted


### *GitHub* flow is a lightweight, branch-based workflow that supports teams and projects where deployments are made regularly.


-- INSERT --

