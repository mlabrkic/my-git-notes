### No_ 01: Forking "kickstart.nvim" GitHub Repository

You will only need to do this once.

Go to <br>
https://github.com/nvim-lua/kickstart.nvim

Press "Fork" on the top right. <br>
When asked where to fork the repository, choose to fork it to your username.

Your forked "kickstart.nvim" repository will be created at <br>
https://github.com\/<username\>/kickstart.nvim <br>
https://github.com/mlabrkic/kickstart.nvim

NOTE: <br>
I changed the name of the repository from "kickstart.nvim" to "nvim-lua-config". <br>
https://github.com/mlabrkic/nvim-lua-config


### No_ 02: Cloning a Forked "kickstart.nvim" Repository

NOTE: <br>
`git clone https://github.com/mlabrkic/nvim-lua-config.git`

C:\GITHUB\nvim-lua-config\\.git\

```
HEAD

ref: refs/heads/master
```

```
config

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
	remote = origin
	merge = refs/heads/master
```

https://github.com/nvim-lua/kickstart.nvim

https://github.com/mlabrkic/nvim-lua-config


### No_ 03: It is also recommended to configure an "upstream" remote repository

NOTE: <br>
`cd nvim-lua-config`

NOTE: <br>
`git remote add upstream https://github.com/nvim-lua/kickstart.nvim`

You can also use SSH-based or HTTPS-based URLs.

```
config

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
	remote = origin
	merge = refs/heads/master
[remote "upstream"]
	url = https://github.com/nvim-lua/kickstart.nvim
	fetch = +refs/heads/*:refs/remotes/upstream/*
```


### No_ 04: Configure the Remotes

Configure git to "pull" master from the "upstream" remote: <br>
(branch "master") <br>
NOTE: <br>
`git config --local branch.master.remote upstream`

Since one should never attempt to push to "upstream", <br>
configure git to "push" always to "origin": <br>
NOTE: <br>
`git remote set-url --push upstream https://github.com/mlabrkic/nvim-lua-config.git`


```
config

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
	url = https://github.com/nvim-lua/kickstart.nvim
	fetch = +refs/heads/*:refs/remotes/upstream/*
	pushurl = https://github.com/mlabrkic/nvim-lua-config.git
```


### No_ 05: Listing the Remote Repositories

To list the remote repositories that are configured, along with their URLs: <br>
`git remote -v`

You should have two remote repositories: <br>
"origin" pointing to your forked "kickstart.nvim" repository, and <br>
"upstream" pointing to the official "kickstart.nvim" repository:

```
origin	https://github.com/mlabrkic/nvim-lua-config.git (fetch)
origin	https://github.com/mlabrkic/nvim-lua-config.git (push)

upstream	https://github.com/nvim-lua/kickstart.nvim (fetch)
upstream	https://github.com/mlabrkic/nvim-lua-config.git (push)
```

To verify the upstream for master: <br>
`git config branch.master.remote`

It should emit "upstream", <br>
indicating to track/pull changes for main from the upstream remote.


### No_ 06:


To find the branch you are currently on: <br>
`git branch` <br>
==> * master

NOTE: <br>
`git pull` <br>
(or git pull upstream master)

`git checkout master`


Info, pull from <br>
https://github.com/mlabrkic/nvim-lua-config <br>
`git pull origin master`


---

### REFERENCES

[Python: Git Bootcamp and Cheat Sheet](https://devguide.python.org/getting-started/git-boot-camp/index.html)


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
.gitconfig


TODO: <br>
Creating and Switching Branches <br>
https://devguide.python.org/getting-started/git-boot-camp/index.html#creating-and-switching-branches



