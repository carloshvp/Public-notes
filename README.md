# My new notes

The intention of this initiative is to get used to write MarkDown notes using VSCode shortcuts and pushing to git/Github once in a while

## Docs extensions
I have installed in VSCode 2 extensions, one for editing (docs-markdown) and a second one for preview (docs-preview), both from Microsoft.

To open shortcuts, either use F1 and write "docs:" or use ALT+M to show palette

## Git and GitHub

The info below from Git is obtained from [this video](https://youtu.be/RGOj5yH7evk)

Hints for pushing to git/github
- Start tracking either new repo (git init) or cloning (git clone)
    - If started with new repo and for each new files: Add them with git add . # Replace . by single files if you want
    - If file(s) are already added, use: git commit -am "message" 
- "git status" to see where we are
- "git checkout -b feature/new-branch-creation"
- git commit -m "here some message" -m "Here some description"
- git merge master
- git checkout master
- git push
- git push -u origin master
    - -u sets the default remote and next time "git push" is enough (no "origin master" required)
- git pull origin master
- git branch -d feature/new-branch-creation
- git reset HEAD~1
    - This comes back 1 commit (undo)
- git log
    - See last commits
- git reset 22984ea49d...
    - Come back to that commitID
- git reset --hard 22984ea49d...
    - Go back to that commitID and remove further commit IDs
- git remote add origin git@github.com:carloshvp/Public-notes.git
- git remote -v
    - List remotes
- git pull --allow-unrelated-histories
    - This is useful to be able to bring together repos in different locations which both already have some unrelated commits


### How to make a pull request

1. Go to GitHub
1. Search and click the "*Create Pull-request*" button :)

### VIM exit
I hate Vim because I always forget how to use it. If I am ever trapped there, press "Esc" and write ":wq" and "Enter" so that it is saves and exit

# ToDos
- show git branch/status in terminal?
- MD tutorial for advanced stuff
- Advanced Git tutorial
- Merge several commit IDs into one from December 2019
- Do some more trainings in GitHub