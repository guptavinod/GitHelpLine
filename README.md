## GIT Commands and branching concepts

**GIT COMMANDS**
```
git config --global user.name "guptavinod"
git config --global user.email "gupta.vinodkumar@gmail.com"
git config --list (in home dir) 
git status
git add <file> [to staging]
git reset <file> [staging to local area]
git commit -m "jmd"<file>
git push -u origin master 
git pull origin master
git log
git log --all --graph --decorate --oneline (logging history)

touch .gitignore (file created and thhis file in working directory and contains files to be ignored)	

git remote -v (information of remote repository)

git branch -a (information about branches in our repository - locally an remotely)


git branch newbranch
git checkout newbranch 
git push -u origin newbranch |  make changes and push back using push command 

--> Now we have 2 branches - master and newbranch and now lets merge them
git checkout master 
git pull origin master (incase there are changes in master - keep in synch with local)
git branch --merged (see what is merged currently - will show only master)
git merge newbranch (merges changes to master where you are sitting right now)
Check again: 
git branch --merged (will show master and new branch)
git push origin master (after merging the changes to the master push it up again to the repository)
	
Now to delete the branch: 
git branch -d newbranch
git branch --merged (check now only master remains again)
git branch -a (check whther gone - local shows only master while remote still has newbranch - hence the next step) 
git push origin --delete newbranch (delets it from remote repository GIthub as well)
```
[https://www.youtube.com/watch?v=HVsySz-h9r4](https://www.youtube.com/watch?v=HVsySz-h9r4)  
[https://www.javacodegeeks.com/2016/07/git-tutorial.html#section_4_1](https://www.javacodegeeks.com/2016/07/git-tutorial.html#section_4_1)  


**GIT FLOW**

![Git branching model](images/git-model.png)	

**The overall flow of Gitflow is:** 
- A develop branch is created from master
- A release branch is created from develop
- Feature branches are created from develop
- When a feature is complete it is merged into the develop branch
- When the release branch is done it is merged into develop and master
- If an issue in master is detected a hotfix branch is created from master
- Once the hotfix is complete it is merged to both develop and master

For complete understadning on above model visit following [link: https://nvie.com/posts/a-successful-git-branching-model/](https://nvie.com/posts/a-successful-git-branching-model/).


**Other reference GIT commands for quick reference**
```
> git checkout -b f1 develop
> git checkout -b f2 develop

> git push --set-upstream origin f1

> git checkout develop
> git merge --no-ff f1
> git push origin develop

> git checkout -b release-1.0
> git commit -am "bug fixing done"
> git push --set-upstream origin release-1.0

> git checkout master
> git merge --no-ff release-1.0
> git tag -a 1.0
> git push origin tag 1.0
> git push origin master

> git checkout develop
> git merge --no-ff release-1.0
> git push
> git branch -d release-1.0

```

**SmartGit Tool for using GIT-Hub**
URL of video on Version Controlling with SmartGit and Github:  
[https://www.youtube.com/watch?v=Aj-sZ2JWnj4](https://www.youtube.com/watch?v=Aj-sZ2JWnj4)

**Blogs:**   
Understand GIT Flow using GIT native commands:   
[https://nvie.com/posts/a-successful-git-branching-model/](https://nvie.com/posts/a-successful-git-branching-model/)  
[https://jeffkreeftmeijer.com/git-flow/](https://jeffkreeftmeijer.com/git-flow/)  

**Repo:**  
[https://github.com/nvie/gitflow](https://github.com/nvie/gitflow)

**Videos:**  
[https://buildamodule.com/video/change-management-and-version-control-deploying-releases-features-and-fixes-with-git-how-to-use-a-scalable-git-branching-model-called-gitflow#viewing](https://buildamodule.com/video/change-management-and-version-control-deploying-releases-features-and-fixes-with-git-how-to-use-a-scalable-git-branching-model-called-gitflow#viewing)  
[https://vimeo.com/16018419](https://vimeo.com/16018419)  

**FOR SSH KEY RELATED ISSUES:**
[https://devmarketer.io/learn/set-ssh-key-github/](https://devmarketer.io/learn/set-ssh-key-github/)  
[https://www.youtube.com/watch?v=H5qNpRGB7Qw&list=PLwAKR305CRO-fenwcN2-IC0rgaB6vaJgD&index=8&t=0s](https://www.youtube.com/watch?v=H5qNpRGB7Qw&list=PLwAKR305CRO-fenwcN2-IC0rgaB6vaJgD&index=8&t=0s)  

**How GIT Commands map to GITFlow commands:**   
[https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

**FOR GIT REBASE & INTERACTIVE REBASE COMMANDS:**  
[https://www.themoderncoder.com/a-better-git-workflow-with-rebase/](https://www.themoderncoder.com/a-better-git-workflow-with-rebase/)

**GOOD SPRING BLOG & REPOSITORY**  
[https://www.baeldung.com/](https://www.baeldung.com/)



