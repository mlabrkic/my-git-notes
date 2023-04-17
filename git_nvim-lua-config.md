
### No_ 01: Cloning "kickstart.nvim" Repository

https://github.com/nvim-lua/kickstart.nvim

`cd C:\PROJECTS\` <br>
`git clone https://github.com/nvim-lua/kickstart.nvim.git`

NOTE: I changed the name of the repository from "kickstart.nvim" to "nvim-lua-config". <br>

```
C:\PROJECTS\nvim-lua-config\.git\config

[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[remote "origin"]
	url = https://github.com/nvim-lua/kickstart.nvim.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
```


### No_ 02: Add an "upstream" Remote Repository

`cd nvim-lua-config` <br>
`git remote add upstream https://github.com/nvim-lua/kickstart.nvim.git`

You can also use SSH-based or HTTPS-based URLs.

```
nvim-lua-config\.git\config

[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[remote "origin"]
	url = https://github.com/nvim-lua/kickstart.nvim.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
[remote "upstream"]
	url = https://github.com/nvim-lua/kickstart.nvim.git
	fetch = +refs/heads/*:refs/remotes/upstream/*
```


### No_ 03: Configure the Remotes - "upstream"

Configure git to "pull" master from the "upstream" remote: <br>
(branch "master") <br>
`git config --local branch.master.remote upstream`

Since one should never attempt to push to "upstream", <br>
configure git to "push" always to "origin": <br>
`git remote set-url --push upstream https://github.com/mlabrkic/nvim-lua-config.git`

```
nvim-lua-config\.git\config

[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[remote "origin"]
	url = https://github.com/nvim-lua/kickstart.nvim.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = upstream
	merge = refs/heads/master
[remote "upstream"]
	url = https://github.com/nvim-lua/kickstart.nvim.git
	fetch = +refs/heads/*:refs/remotes/upstream/*
	pushurl = https://github.com/mlabrkic/nvim-lua-config.git
```


### No_ 04: Configure the Remotes - "origin" (url)

`git remote set-url origin https://github.com/mlabrkic/nvim-lua-config.git`

```
nvim-lua-config\.git\config

[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[remote "origin"]
	url = https://github.com/mlabrkic/nvim-lua-config.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = upstream
	merge = refs/heads/master
[remote "upstream"]
	url = https://github.com/nvim-lua/kickstart.nvim.git
	fetch = +refs/heads/*:refs/remotes/upstream/*
	pushurl = https://github.com/mlabrkic/nvim-lua-config.git
```


### No_ 05: Listing the Remote Repositories

To list the remote repositories that are configured, along with their URLs: <br>
`git remote -v`

You should have two remote repositories: <br>
"origin" pointing to your forked "kickstart.nvim" (new name "nvim-lua-config") repository, and <br>
"upstream" pointing to the official "kickstart.nvim" repository:

```
origin	https://github.com/mlabrkic/nvim-lua-config.git (fetch)
origin	https://github.com/mlabrkic/nvim-lua-config.git (push)

upstream	https://github.com/nvim-lua/kickstart.nvim.git (fetch)
upstream	https://github.com/mlabrkic/nvim-lua-config.git (push)
```

To verify the upstream for master: <br>
`git config branch.master.remote`

It should emit "upstream", indicating to track/pull changes for main from the upstream remote.


### No_ 06: Create a New Repository on GitHub

To create a new repo on GitHub, log in and go to the GitHub home page.

You can find the "New repository" option under the "+" sign next to your profile picture,
in the top right corner of the navbar. <br>
Leave the initial settings (Do not mark: license, readme,...)!!!


### No_ 07: Push a Branch to GitHub

Instead of branch "master", I want branch "main".

To find the branch you are currently on: <br>
`git branch` <br>
==> master

To list all the branches, including the remote branches: <br>
`git branch -a` <br>
==> master

Create a new branch from "master" and switch to it: <br>
`git switch -c <branch-name> master` <br>
`git switch -c main master`

```
Or
Create a new branch from "master":
git branch main master

Switch to the new branch:
git switch main
```

Push a Branch to GitHub: <br>
`git push origin main`

Info: <br>
git pull  (https://github.com/nvim-lua/kickstart.nvim) <br>
git push  (https://github.com/mlabrkic/nvim-lua-config)


### No_ 08: Create a new "lazyconfig" branch from "main"

Create a new branch from "main" and switch to it: <br>
`git switch -c lazyconfig main`

```
Or

Create a new branch from "main":
git branch lazyconfig main

Switch to the new branch:
git switch lazyconfig

git push origin lazyconfig
```

Optionally verify the commit using the log command: <br>
`git log`


### No_ 09: Delete a branch "master"

Optionally delete a **local** branch "master": <br>
```
git switch main
git branch -d master
```

`git push origin -f`

To delete a **remote** branch:
`git push origin -d <branch-name>`


### REFERENCES

[Python: Git Bootcamp and Cheat Sheet](https://devguide.python.org/getting-started/git-boot-camp/index.html)

[github.com: renaming-a-branch](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-branches-in-your-repository/renaming-a-branch)

```
git config -l --global
git config -l --local

git config -l
git config -l --system
git config -l --show-origin
```

The --global flag sets these parameters globally <br>
while the --local flag sets them only for the current project.

```
git config --global user.name "Your Name"
git config --global user.email your.email@example.com

git config --global init.defaultBranch main
```

==> <br>
`C:\Users\userName\.gitconfig`

TODO: <br>
Creating and Switching Branches <br>
https://devguide.python.org/getting-started/git-boot-camp/index.html#creating-and-switching-branches

