# **Tagging**

## **Important Commands**

### **Search**

* **List All Tags**
  * **`$ git tag`**

* **Search for a Tag**
  * **`$ git tag -l <tagname>`**

### **Create**

* **Creating a Lightweight Tag**
  * **`$ git tag <tagname>`**
    * creates a tag for the currend HEAD

  * **`$ git tag <tagname> <gitid>`**
    * creates a tag for a specific commit 


* **Creating a Annotated Tag**
  * **`$ git -a <tagname> -m <tag message>`

* **Annotated Tags store meta-data you can see using**
  * **`$ git show <tagname>`**


### **Share**

* **Pushing Tags to Remote**
  * **`$ git push origin --tags`**
     
     or for an specific one

  * **`$ git push origin <tagnmae>`**


### **Delete**

* **Remove a Tag**

  * **`$ git tag -d <tagname>`**
    * remove a local tag

  * **`$ git push origin --delete <tagname>`**
    * remove a remote tag

### **Checking**

* **Use the cheockout command to see the version of  the tag you choose**
  * **`$ git checkout <tagname>`**

* **Warning: this puts your repository in _"detached HEAD"_ state**

