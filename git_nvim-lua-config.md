
### No_ 01: Cloning "kickstart.nvim" Repository

https://github.com/nvim-lua/kickstart.nvim

`cd C:\PROJECTS\` <br>
`git clone https://github.com/nvim-lua/kickstart.nvim.git`

NOTE: I changed the name of the repository from "kickstart.nvim" to "nvim-lua-config". <br>
C:\PROJECTS\nvim-lua-config\

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


### No_ 04: Configure the Remotes - "origin"

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

Info: <br>
git pull (https://github.com/nvim-lua/kickstart.nvim) <br>
git push (https://github.com/mlabrkic/nvim-lua-config)


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

git push origin my-new-branch <br>

==>
(git push origin master) <br>
`git push`


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
`C:\Users\userName\.gitconfig`

TODO: <br>
Creating and Switching Branches <br>
https://devguide.python.org/getting-started/git-boot-camp/index.html#creating-and-switching-branches

