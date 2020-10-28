# [](#header-1)github-basic and syncing for collaboation of developers with SVN (distributed version control)
This repository will help build up git proficiency.

## [](#header-2)git remote
  * This function allows you to manipulate, view, and create connections to the other repositories. 
  * Real time access is possible with the git remote for repositories. Its like creating link to the repository. 
  * Different repositories can be connected simulataneously
  * command line is "git remote" to connect (add url allows specific repository)
  * git remote requires manual pull or push of local repository/commits to central repositories. This is basically sharing command.
  * other common commands include, -f for fetch, -rm for remove, and show <NAME> for viewing the high level information. 
  * git remote add jehoon http://dev.example.com/ohjeyy93.git
  * Allows individual developers to collbatorate outside of the central repositories

## [](#header-2)git fetch
  * This command is used for downlaoding commits, files, and references from the remote repositories connected. 
  * git fetch allows you to track the history of central repository. 
  * Fetching is safe way to review commits before combining with local repository. 
  * git fetch doesn't affect the local current work state so it is safer than git pull
  * git merge can be later used to create a merge commit for the new remote content. 
  * remote branches can be checked as well
  * command example : get fetch <remote> + [optinal] <branch>
  * example git ohjeyy93 jehoon Bayesian
  * git checkout allows to check the remote branch that has been just downloaded
  * git fetch origin command allows to synchronize with the origin
  ![Test Image 1](https://github.com/ohjeyy93/github-basic/blob/main/github%20fetch%20image.png)
  (git fetch concept picture from :https://www.atlassian.com/git/tutorials/syncing/git-fetch)
  * git fetch is basically primary command to download from a remote repository. It is very important for collaborative work. 

## [](#header-2)git push
 * git push is useed to upload files from local repository to the remote repository. 
 * It is quiet the opposite of gitfetch 
 * Remote branches get configured when gitremote command works. 
 * git push command: git push <remote> <branch>
 * git push is common way to upload files to the central repositroy and the modification is shared among collaborators. 
 ![Test Image 1](https://github.com/ohjeyy93/github-basic/blob/main/gitpush.png)
  (git fetch concept picture from :https://www.atlassian.com/git/tutorials/syncing/git-push)
 * example usage of git syncing: 
 * git checkout <branch>
 * git fetch origin <branch>
 * git rebase -i origin/<branch>
 * git push origin <branch>
 * force push also works. This will overwrite the history. 

## [](#header-2)git pull
 * git pull is used to download content from remote repository which instantly updates the local repositroy. 
 * This is similar to git fetch plus git merge but in one step. 
(git fetch concept picture from :https://www.atlassian.com/git/tutorials/syncing/git-pull)
 ![Test Image 1](https://github.com/ohjeyy93/github-basic/blob/main/gitpull1.png)
 * This image explains downloading changes in the content from A,B,C and creating E. 
 ![Test Image 1](https://github.com/ohjeyy93/github-basic/blob/main/gitpull2.png)
 * This example is similar as above but with repository H. 
 ![Test Image 1](https://github.com/ohjeyy93/github-basic/blob/main/gitpull3.png)
 * git Rebase allows to fetch from other modificiations which would be E and F for G. 
 ![Test Image 1](https://github.com/ohjeyy93/github-basic/blob/main/gitpull4.png)
 * git pull is basically a svn update. Basically you git fetch first and then merge with new master. 
 * git pull <remote repo>

# [](#header-1)github-basic and making pull request

## [](#header-2)git pull request
 * It is basically a forum to allow feedbacks and give notification. This activities can be tracked. 
 * Follow up commits can be tracked and discussed. 
 * There is source repostiory and dstination repository. 
 * First developer creates a new feature to a targeted branch from their local repo.
 * The developer send pull request and the other collaborators can reveiw the changes. 
 * The projector manager could accept or close the pull request. 
 * This allows gitflow workflow for collaboration where many developers can work together and add features to the project.
 
 # [](#header-1)github-basic git branching
 
 ## [](#header-2)branching
 
  * A branch is an independent line of the developement for a project. It is abstract stage where the project can be edited and commited. 
  * git branch command can manipulate the branch with deletion, creation, and renaming.
  * new remote branches can be created as git remote add <new remote repo> <url of the repository>
  * git merge combines seuqences of commits into one overall history of commits. 
  * Merge will work unless confilct in the changes. 
  * git checkout allows you to navigate the git repository and branches. 
  * git merge conflict requires navigating and resolving the conflicts to collaborate. When two seperate branches make same edits on the same location of the file we need to identify the conflict using gitlog, gitreset, gitstatus, gitcheckout, and gitreset. 
  * git log will produce log list of conflicts and commits. 
  * git check out can be checked for undoing the changes. 
  * git reset undos the changes to the working directory. 
  * Types of merges are: implicting merge by rebase, fast-forward merge, squash or merge, without explicit merge, and recursvie git merge.
  * explicit merge is default where creating new merge commit is done. 
  * Implicting merge via rebase takes a sequence of commits and applies them on top of the branch. 
  * Rebase events are usually triggered by rebase-events. 
  * Squash on merge is done usually without explicit merge. This is interactive rebase where commits from target branch are combined into one commit. In the end the final commit is a singular squashed branch commit. 
 
  # [](#header-1)github-basic comparing work flows 
  
  ## [](#header-2)comparing
  
   * scale with the team size
   * undo mistakes and errors with the workflow
   * Workflow should make things simple to work together. 
   * The general workflow includes initialize cnetral repository, host the central repository, clone the repositroy, modify, push new commits, manage conflicts, 
  
  

