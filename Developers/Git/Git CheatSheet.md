> [!info]- Setup
>
> > [!Tip]- Set the name that will be attached to your commits  
> > **git config --global user.name "Your Name"**
>
> > [!Tip]- Set the email that will be attached to your commits  
> > **git config --global user.email "Your email"**

> [!info]- Basics
>
> > [!Tip]- Create new local Git repository  
> > **git init**
>
> > [!Tip]- Download a remote repository  
> > **git clone**
>
> > [!Tip]- Show the working directory status (staged, unstaged, untracked files)  
> > **git status**
>
> > [!Tip]- Add new or changed files to the next commits (Stage for next commit)  
> > **git add**
>
> > [!Tip]- Commit the staged snapshot using "Message" as the commit message  
> > **git commit -m "Message**
>
> > [!Tip]- Push local branch commits to the remote repository branch  
> > **git push `<remote> <branch>`**

> [!info]- Branch, Merge and Update
>
> > [!Tip]- List all local branches
> > **git branch**
>
> > [!Tip]- List all local and remote branches
> > **git branch -a**
>
> > [!Tip]- Create a new branch at the current commit
> > **git branch `<branch-name>`**
>
> > [!Tip]- Switch to an existing branch and check it out
> > **git checkout `<branch-name>`**
>
> > [!Tip]- Create and check out a new branch
> > **git checkout -b `<branch-name>`**
>
> > [!Tip]- Fetch changes from the remote
> > **git fetch `<remote>`**
>
> > [!Tip]- Merge a remote branch into your current branch
> > **git merge `<remote>/<branch>`**
>
> > [!Tip]- Fetch and Merge the remote branch into the current branch (pull = fetch + merge)
> > **git pull `<remote><branch>`**
>
> > [!Tip]- Push local branch commits to the remote repository branch
> > **git push `<remote><branch>`**
>
> > [!Tip]- Push local branch to remote repository and set its copy as an upstream (-u or --set-upstream)
> > **git push -u `<remote><branch>`**

> [!info]- Inspect and Comparare
>
> > [!Tip]- Show commit history of current branch
> > **git log**
>
> > [!Tip]- Show commit history of remote branch
> > **git log `<remote>/<branch>`**
>
> > [!Tip]- Show commit history on branch2 that are not on branch1
> > **git log branch1..branch2**
>
> > [!Tip]- Show unstaged changes between working directory and the index
> > **git diff `<file>`**
>
> > [!Tip]- Show the diff of what on branch2 that on branch1
> > **git diff branch1..branch2**

> [!info]- Tagging
>
> > [!Tip]- List all tags
> > **git tag**
>
> > [!Tip]- Create a new tag v1.2
> > **git tag -a v1.2**
>
> > [!Tip]- Create a new annotated tag v1.3 with a tagging message
> > **git tag -a v1.3 -m "message"**
>
> > [!Tip]- Show tag data
> > **git show v1.3**
>
> > [!Tip]- Push v1.3 tag to remote server
> > **git push remote v1.3**
