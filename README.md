Table of Contents
=================

  * [What You Get From This control\-repo](#what-you-get-from-this-control-repo)
    * [Copy This Repo Into Your Own Git Server](#copy-this-repo-into-your-own-git-server)
      * [Gitlab](#gitlab)
      * [Stash](#stash)
      * [Github](#github)

Created by [gh-md-toc](https://github.com/ekalinin/github-markdown-toc.go)

# What You Get From This control-repo

This control-repo displays an example of a best-practices structure for a control-repo.  

The major points are:
 - An environment.conf that correctly implements:
   - A site directory for roles, profiles, and any custom modules for your organization
   - A config_version script 
 - Provided config_version scripts to output the commit of code that your agent just applied
 - Basic example of roles/profiles code
 - Example hieradata directory with pre-created common.yaml and nodes directory 
   - These match the default hierarchy that ships with PE

##Copy This Repo Into Your Own Git Server

###Gitlab

1. Install Gitlab
 - https://about.gitlab.com/downloads/

2. After Gitlab is installed you may sign if with the `root` user and password `5iveL!fe`

3. Make a user for yourself

4. Make an ssh key to link with your user.  You’ll want to do this on the machine you intend to edit code from ( most likely not your puppet master but your local workstation / laptop )
 - http://doc.gitlab.com/ce/ssh/README.html
 - https://help.github.com/articles/generating-ssh-keys/

5. Create a group called `puppet` ( this is case sensitive )
 - http://doc.gitlab.com/ce/workflow/groups.html

6. Add your user to the `puppet` group as well

7. Create a project called `control-repo` and set the Namespace to be the `puppet` group

8. Clone this control repository to your laptop/workstation
 - `git clone <repository url>`
 - `cd control-repo`

9. Remove this repository as the origin remote 
 - `git remote remove origin`

10. Add your internal repository as the origin remote
 - `git remote add origin <url of your gitlab repository>`

11. Push the production branch of the repository from your machine up to your git server
 - `git push origin production`

###Stash

Coming soon!

###Github

Coming soon!
