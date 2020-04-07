# **Creating a Tag**


1. `git tag v1.4`.
	- **Annotated Tag**, stores Meta Data like, Name, Email and Date. Best practice, use  as **public**.
2. `git tag <tagname>`.
	- **Lightweight Tag**, are bookmarks to a commit. Just a Name and a Pointer to a commit. Best practice, use it like **private**.


## **Creating and Saving Message in a Tag**
-  `git tag -a v1.4 -m 'my version 1.4', 
	- *Created a new Tag and opened the text editor in favor of saving the message*


## **Listing Tags**

- `git tag`
	- *This command list the stored tags in a repo*


## **Tagging Later**

- `git tag -a v1.2 <SHA>`
	- *With this command we can tag a project at v1.2*


## **Sharing Tags**

- `git push origin v1.2`
	- *This command shares tags to the remote**
- `git push origin --tags`
	- *This command pushes all of the tags to the remote server*


## **Deleting Tags**

- `git tag -d <tagname>`
	- *Using this command we delete a tag on our local repo, but **not remove** it from remote server*

### **There are two ways for deleting a tag from a remote server**
1. `git push origin :refs/tags/v1.2-lw`
	- *This reads it as a null value, effectively deleting it.*
2. `git push origin --delete <tagname>
	- *This is more intuitive way to delete a remote tag.*


## **Checking out Tags**

- `git checkout v2.0.0`
	- *This command used to view a version of file a tag pointing to.

**Warning: This puts your repository in _"detached HEAD"_ state**



