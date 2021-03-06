## d._.b Codices - Common Terminal Commands
### Last Update: 3/31/2019
Using Unix/Mac terminal is simple, don't be afraid to use it. Here are some common commands when using NPM, Yarn, Brew, Git, Heroku, and more. This single README.MD file Repo was created to help new developers with common commands that are used throughout the development process of building Angular apps and other related package managers and Command Line Interfaces (CLI). I will continue to update this file and hope this will help others through their development journey!

[Comman Commands Repo](https://github.com/CodicesTechnology/Common-Commands)

## Versions
* Angular v5.2.9
* Angular Cli v1.7.3 
* Angular Cli v7.2.11
* Homebrew v2.0.6
* Yarn v1.15.2
* Node v11.10.0
* NPM v6.7.0
* MongoDB v4.0.3 
* Mongoose v5.0.11
* Express v4.16.3
* Heroku Cli v7.22.7

## Terminal/NPM
### Making folders and files
* Navigate to a specific directory
    * $ `cd /FOLDER/FOLDER`
    
* Making a folder aka "**directory**"
    * $ `mkdir folderA`
    
* Making a file
    * $ `touch fileOne.html`
    
### USing Nodemon four auto-recompiling the server
You can install nodemon as a project dependency or globaly to your machine

* **If you want to install it the project...**
   * $ `npm install --save-dev nodemon`

* **If you want to install it globally...**
   * $ `npm install -g nodemon`
   
* Then replace your "**node server.js**" start script with "**nodemon server.js**" in the **package.json** file.

* Once you run $ `npm start` or your projet's start command it will begin recompiling automatically anytime you make changes to server files.

## Angular Cli 
### Angular Universal
* Run command to add universal module and files
    * `ng g universal universal`

## Git 
### Git Clone
* Clone a specific GitHub Repo by copying the HTTPS  
    * $ `git clone https://github.com/USERNAME/REPO-NAME.git`

### New GitHub Repo and Remote
* 1st make a new GitHub Repo from your GitHub account. I usually never include a README file or anything else with my new repo. [GitHub](https://github.com/)

* Initialize your root project directory
    * $ `git init`
    
* Copy the origin remote command
    * $ `git remote add origin https://github.com/USERNAME/REPO-NAME.git`
    
* Verify added remote origin
    * $ `git remote -v`
    
* Stage all your files
    * $ `git add .`
    
* Commit staged files
    * $ `git commit -m "MY FIRST COMMIT d._.b Codices"`
    
* Push to remote Repo
    * $ `git push -u origin master`

### REMOVE REMOTE
* First verfiy that yor local directory has a remote. If nothing appears after the following command, it means you dont have one attached.
    * $ `git remote -v`

* It may look something like this...
    * heroku  https://git.heroku.com/HEROKU-REPO-URL.git (fetch)
    * heroku  https://git.heroku.com/HEROKU-REPO-URL.git (push)
    * origin  https://github.com/USERNAME/REPO-NAME.git (fetch)
    * origin  https://github.com/USERNAME/REPO-NAME.git (push)

* Remove the selected remote by passing the remote's label. If I wanted to remove the "heroku" remote, I would use the following...
    * $ `git remote rm heroku`

* If I wanted to remove the "origin" remote, I would use the following...
    * $ `git remote rm origin`

* Finally, make sure you removed the GitHub remotes by running the first command. The remiaing remotes or nothing will show.
    * $ `git remote -v`

## BRANCHES 

### Create New GitHub Branch
* Make sure you are up to date on the repo.
    * $ `git pull`
    
* Make your new repo branch locally.
    * $ `git checkout -b BRANCH-NAME`
    
* Now push your newly made branch.
    * $ `git push -u origin BRANCH-NAME`
    
### Remove Branches 
* To get a list of all branches use the following command.
    * $ `git branch -r`
* To get a list of the branches connected to your local repository only, use...
   * $ `git ls-remote --heads REMOTE-NAME`

* For a detailed list of branches you can use...
   * $ `git remote show REMOTE-NAME`
   
* Use the following command to delete the branch you want.
   * $ `git push REMOTE-NAME --delete BRANCH-NAME`

* Another common command would be.
   * $ `git remote prune REMOTE-NAME :BRANCH-NAME`
        
### Push Updates to a GitHub Branch

Before merging your local repository to your remote repository it is important to understand what these commands will do.
* $ `git pull --rebase` invokes a shortcut combo script of $ `git fetch` followed by $ `git rebase`.
* $ `git pull` invokes $`git fetch` followed by $ `git merge`.

* If you want to push to an existing **non-master** remote branch,  first make sure you are up-to-date using the pull command.
   * $`git pull origin`
   or
   * $`git pull origin BRANCH-NAME`
   
* then specify which existing **non-master** remote branch you'd like to push to.
   * $ `git push origin BRANCH-NAME`
   
## Yarn
* Install dependencies, first make sure you are in the project's root directory, then run...
    * $ `yarn install`
* Upgrade Yarn
    * $ `yarn upgrade`

## Homebrew
* Coming Soon...

## MongoDB
* Coming Soon...

## Heroku Cli
### Heroku Deployment
* First, make sure you are logged in to your Heroku account. To login to your Heroku account run...
   * $ `heroku login`
   * You'll be asked to enter your email and password.
   
* Once you are ready to deploy your application, you need to create a Heroku repo. From your Project's root directory run the following command...
   * $ `heroku create REPO-NAME`
   * if you don't pass a repo-name, it generate a random Heroku repo name for you.
   
* If you've already made a Heroku repo or to make sure you initialized git in your local repository, from your root directory run the following command...
   * $ `git init`
   
* Next, make sure you've connected your local repo to your Heroku repo by running...
   * $ `heroku git:remote -a REPO-NAME`
   
* Once the setup is complete you can begin deployment by running...
   * $ `git add .`
   
* Make a commit with a comment by running...
   * $ `git commit -am "CODICES COMMENT, MADE EDITS TO REPO"`
   
* Finally, push your project to your Heroku repo by running...
   * $ `git push heroku master`
   
### Continued deployments to your Heroku repo
* If you're making changes to your previously deployed project and set up has been complete you simply run the following commands for each deployment version. In this order 
   * $ `git add .`
   * $ `git commit -am "ANOTHER COMMENT"`
   * $ `git push heroku master`

### Connecting to an existing Heroku repository
* From your root directory run this command and then follow the deployment steps above.
   * $ `heroku git:remote -a REPO-NAME`

* You may need to initiate git in your directory. If so run...
   * $ `git init`


# Author
d._.b [Codices](https://github.com/CodicesTechnology)
