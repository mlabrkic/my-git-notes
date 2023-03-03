## My git notes

### TRACKING PATH CHANGES

Versioning file removes and path changes

git rm [file]<br>
delete the file from project and stage the removal for commit

**git mv [existing-path] [new-path]<br>**
change an existing file path and stage the move

git log --stat -M<br>
show all commit logs with indication of any paths that moved

<br>

#### Example:

I have this:

```
nvim
│
├── lua
│   ├── plugins\bufferline.lua, todocomments.lua, ...
│   └── plugins.lua
```

<br>

I want this:

```
nvim
│
├── lua
│   ├── CUSTOM
│   │  ├── CONFIG\bufferline.lua, todocomments.lua, ...
│   │  └── plugins.lua
```

1. Move "plugins.lua" to "custom" folder

git mv plugins.lua **custom**\plugins.lua<br>
git commit -m "Moved to "custom" folder"

2. Rename "plugins" folder to "config" and move to "custom" folder

git mv plugins\ **custom**\config\ <br>
git commit -m "Renamed "plugins" folder to "config", and moved to "custom" folder"








<br>

## RESOURCES

* GitHub Education:  git-cheat-sheet-education.pdf
* [GitHub Docs -Get started](https://docs.github.com/en/get-started#all-docs)
* [GitHub Docs -Quickstart](https://docs.github.com/en/get-started/quickstart)


