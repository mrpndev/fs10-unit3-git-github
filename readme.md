# Git Lesson

- version control system created by Linus Torvalds in 2005
- allows multiple developers to contribute to the same codebase
- that codebase or project is called a repository (repo for short)

## First Time Git Setup

- to see your git config, use the command `git config --global --list`
- to set your username, use `git conifg user.name --global "first last"`
- to set your email, use `git config user.email --global "email@here.com"`

## How to use Git

- **in the folder in which you intend to create a project** initialize a new git repository
- initialize a new repository using `git init` command
- to check the status of the repository, use `git status` command
- in order to track files, use `git add <name of file>` to track a file
	- if you want to add all of the files at once, use `git add .`
- if you would like to unstage a file, you can use `git rm --cached <name of file>` to do so
- if you are ready to commit, use the `git commit -m "your commit message here"` command
> [!TIP]
> commit messages should succintly explain your changes
- `git log` will show you a history of your commits

## Git Lingo

- branch - a timeline of your code at any given point
- the default branch is called the `main` branch or `master`
- commit - a snapshot of your code at a specific point in time
- commit message - a message describing changes in your commit

## Git Stages
- [ ] tracking
	- a way for us to decide which files git will track in its repository
- [ ] staging
	- a way for us to decide what will become a commit
- [ ] committing

## Git Log Explained
- commit hash - unique value describing our commit
- main/master (or other) - name of the branch on which the commit resides
- HEAD - think of it as eyes. It points to what our eyes are looking at
- author of the commit
- date the commit occurred
- commit message
- to get out of it, you may need to hit `q`

## Connecting Git Repo to GitHub Repo
- create a repository on GitHub
	- sign in to GitHub with your credentials
	- find the green `new` button to create a new repository
	- give it a repository name
	- choose visibility (usuallly public)
	- click `create repository`
- copy the HTTPS (or SSH if your setup requires it) link to your repo
- run the following command `git remote add origin <paste your link here>`
	- `remote` is responsible for remote repos
	- `add` adds something
	- `origin` this is the name we will give our remote repo to reference later. Commonly use origin or upstream.
	- `<your link>` is the HTTPS or SSH endpoint from the GitHub repo
- return back to syntax is a good thing!
- to verify it's successfully linked, run `git remote -v` to see the endpoint
- you should see the following:
	- name of the endpoint
	- the endpoint itself
	- fetch (bring down) and push (send up)
- in order to push your code, run `git push origin <name of branch>` (ex: `git push origin main`)