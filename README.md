  Git has three core areas namely Working directory,Staging area and the Local Repository.The Working directory is the area where currently we are working which contains the untracked files.The Staging area is where git start tracking the files and saving them and the local repository is our .git directory where we can see all ours commits.
  The following are the steps done for demonstrating concepts of Git      
  
* **Signup for the GitHub and create a repository**

* **Create a local git repository using the following commands**

   ```
  mkdir first_local_repo
  cd first_local_repo
  git init
  ```
  `git init` is used to convert an existing, unversioned project to a Git repository or initialize a new, empty repository
  
* **Create a text file named hello_world and copy the text provided.**

  `vi hello_world.txt` 
  
   Save it using Esc :wq
   
* **Commit to local repository and push it to Git Repository**
   ```
  git add hello_world
  git commit -m "First Commit"
  git remote add origin url (https://github.com/Likhitha016/test)
  git pull origin master
  git push origin master
  ```
  `git commit` command is used to save the changes to the local repository.
  
  `git remote` command is used to add our remote repository location as origin(branch) which is used to refer our remote repository.
  
  `git pull` command is used to keep our master branch up to date.
  
  `git push` command is used to push the committted contents from our local repository to remote repository.
  
* **Replace all "to" words by your name. Check git diff to make sure all to words have been replaced and make another commit and push it to Github.**

  By using the following command replace all "to" words with name.
  
  `sed -i 's/ to / name /g' hello_world`
  
  Check whether the words are replaced by using:
  
   `git diff`
   
  Commit the changes and push it to git using:
    ```
    git commit -m "Second Commit" 
    git push origin master
    ```
    
* **Revert back to previous step and check in again.**

   Revert command will create a new commit that inverses the changes specified which revert the last commit.We alse specify the hashcode of the commit we want to revert.
   
   `git revert HEAD` or `git revert hashcode`
   
* **Create a new_branch with name new_branch.**

  A new branch can be created using checkout command as follows
  
    `git checkout -b new_branch`
    
* **Replace all "Torvalds" words with your name in this new_branch and commit + push it to Github**

  By using the following command replace all "Torvalds" words with name
  
  `sed -i 's/Torvlds/name/g' hello_world`
  
  Commit the changes and push it to git using:
  
    ```
    git commit -m "First Commit in new_branch" 
    git push origin new_branch
    ```
* **Merge new_branch to the previous branch.**

  By using checkout command we can switch to the master branch and merge both the branches by using following commands
    ```
     git checkout
     git merge new_branch
    ```
    
* **Clone the repository from the Git to local repository in some folder**

  By creating a new directory git_clone_repo and initializing git in this folder,clone the git repository
    ```
     mkdir git_clone_repo
     cd git_clone_repo
     git init
     git clone url
     ```
  
   
   

  
  


 
  
