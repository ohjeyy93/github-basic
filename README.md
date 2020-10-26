# [](#header-1)github-basic and syncing for collaboation of developers with SVN (distributed version control)

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
