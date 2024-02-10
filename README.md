# Git Aliases

## Common Aliases

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.last 'log -1 HEAD'
```

- **git co**: Short for git checkout.
- **git br**: Short for git branch.
- **git ci**: Short for git commit.
- **git st**: Short for git status.
- **git last**: Show the last commit.

## Shortcuts for Log

```sh
git config --global alias.lg "log --graph --oneline --all --decorate"
git config --global alias.ll "log --pretty=format:'%C(auto)%h %ad | %s%d [%an]' --graph --date=short"

```

- **git lg**: Compact log with a graph.
- **git ll**: Detailed log with a formatted output.

## Diff Aliases

```sh
git config --global alias.dif "diff"
git config --global alias.difc "diff --cached"
git config --global alias.difs "diff --stat"
```

- **git dif**: Show file changes.
- **git difc**: Show staged changes.
- **git difs**: Show a summary of changes.

## Alias for Pull with Rebase

```sh
git config --global alias.pullr "pull --rebase"
```

- **git pullr**: Pull with rebase.

## Alias for Amend

```sh
git config --global alias.amend "commit --amend"
```

- **git amend**: Amend the last commit.

## Alias for Tagging

```sh
git config --global alias.tagm "tag -a -m"
git config --global alias.tagl "tag -l -n1"
git config --global alias.tagd "!f() { git tag -d $1; git push origin --delete $1; }; f"
git config --global alias.tagp "push --tags"
git config --global alias.tagv "tag -v"

```

- **git tagm**:"Version 1.0.0": Create an annotated tag with a message.
- **git tagl**: List tags with details.
- **git tagd**: tagName: Delete local and remote tag.
- **git tagp**: Push all tags to remote.
- **git tagv**: tagName: Verify tag signature.

## Remote and Upstream Operations

```sh
git config --global alias.upstream "branch --set-upstream-to"
git config --global alias.fetchall "fetch --all --prune"
git config --global alias.remotes "remote -v"
git config --global alias.addremote "remote add"
git config --global alias.upinfo "rev-parse --abbrev-ref --symbolic-full-name @{u}"
git config --global alias.pruneremote "remote prune origin"
```

- **git upstream**: origin/main: Set upstream branch.
- **git fetchall**: Fetch all branches from all remotes and prune.
- **git remotes**: Show remote URLs.
- **git addremote**: upstream <upstream_repo_url>: Add a remote.
- **git upinfo**: Show upstream information.
- **git pruneremote**: Prune stale remote tracking branches.

## Creating README and .gitignore

```sh
git config --global alias.addreadme "add README.md"
git config --global alias.newreadme "!touch README.md && git add README.md"
git config --global alias.gitignore "!echo 'node_modules\n.vscode\n.env' > .gitignore && git add .gitignore"

```

- **git addreadme**: Add README.md to staging area.
- **git newreadme**: Create an empty README.md and add it to staging.
- **git gitignore**: Create .gitignore with specified content and add to staging.

## Git Clone

```sh
git config --global alias.cloneit "clone"
```

- **git cl** "https://github.com/example/repository.git": Clone a repository.
