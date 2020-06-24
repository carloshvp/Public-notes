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
- git commit --amend --no-edit
  - This rewrites the last commit to include in it the changes you have just made (like a squash of the last 2 commits)
- git merge master
- git checkout master
- git push
- git push -u origin master
  - -u sets the default remote and next time "git push" is enough (no "origin master" required)
- git pull origin master
  - Conflicts possible
- git fetch
  - Same as pull, it gets from origin the changes, but it does NOT merge them with the local repo, so no conflicts are possible
- git branch -d feature/new-branch-creation
- git reset HEAD~1
  - This comes back 1 commit (undo)
- git log
  - See last commits in all branches
- git log --oneline --decorate --graph --all
  - Last commits in all branches and beautified
- git reset 22984ea49d...
  - Come back to that commitID
- git reset --hard 22984ea49d...
  - Go back to that commitID and remove further commit IDs
- git remote add origin git@github.com:carloshvp/Public-notes.git
- git remote -v
  - List remotes
- git pull --allow-unrelated-histories
  - This is useful to be able to bring together repos in different locations which both already have some unrelated commits
- git rebase
  - Same as git merge, but copies all commits in the feature branch to master (not only 1 commit)
  - To use this, 2 need to execute to rebases, one from feature branch against master (to sync feature branch with master) and one with the feature branch from master (to sync master with the feature branch). Opposite order destroys latest changes in master
- git rebase -i HEAD~3
  - This open vim with the last 3 commits, so that we can squash them or do anything else. To squash commits, change "pick" to "squash", those with squash will be combined with the immediate "pick" above them and create a new commit (with new commit ID). We will need to edit the commit messages too. If we want to drop editing the commit messages, simply use "fixup" instead of "squash"
  - We can also use "reword" insetead of pick or squash, which allows me to change the commit message
  - When pushing to origin, we will get an error "non-fast-forward" because git believes the tip of the branch is behind to the one in origin. To solve this, repeat the git push with -f for "force"

### How to make a pull request

1. Go to GitHub
2. Search and click the "*Create Pull-request*" button :)
   1. Or use the GitHub extension for Pull-requests

### VIM exit

I hate Vim because I always forget how to use it. If I am ever trapped there, press "Esc" and write ":wq" and "Enter" so that it is saves and exit.

To edit a file opened in VIM, press i

## VSCode tricks

Mainly from [Visual Studio Code tips and tricks](https://mybuild.microsoft.com/sessions/6e0072d1-7326-47b6-a7c7-b3ed06c509f8?source=sessions) and [Supercharge your data science workflow with Python and Visual Studio Code](https://mybuild.microsoft.com/sessions/357f159b-945e-4012-9695-8262aabf8f50?source=sessions)

- CMD + D to create multicursor (first select a word, then CMD + D will autoselect the next same word)
  - ESC to exit multicursor
- CMD + SHIFT + L to select all same words (= find and replace)
- CMD + P go to file view
- CMD + SHIFT + P to open control palette

## Python tricks in VSCode

From: [Python development with Visual Studio Code](https://mybuild.microsoft.com/sessions/359a2d3c-56da-4869-9b04-672ffb64c9dd?source=sessions)

### Autogeneration of dependencies

- pip install pip-tools
  - REquirement for next steps
- pip-compile
  - Requires a requirements.in with dependencies without version number and creates the requirements.txt
- pip install -r requirements.txt

### Data science tricks in VSCode

To attach a compute target (kernel) to a Jupyter Notebook:

- CMD + SHIFT + P
- "Specify local or remote Jupyter server for connections"

### Others

- Use Black for auto-formatting
- While debugging in VSCode a piece of Python, we can set conditional breakpoints by right clicking on a breakpoint and "Edit"
  - Expression: can halt execution only if a certain condition is met (e.g. "X > 10" )
  - Hit count
  - Log message: debugger will not stop, but the desired message is printed in the debug console
- Support for PyTest, UnitTest and nose (which one is better? I know only PyTest)

## ToDos

- Learn how to attach a Kaggle kernel to a Jupyter notebook in VSCode (it seems not possible?)
- Show git branch/status in terminal (on the left of my command)
- MD tutorial for advanced stuff
- Advanced Git tutorial
- Merge several commit IDs into one from December 2019
- Do some more trainings in GitHub
- Do some more trainings in Kaggle
  - Pandas training ongoing
- Create [VSCode Extension](https://code.visualstudio.com/api/get-started/your-first-extension) (written in JS) with OSS vulnerability search for non-OSS projects
- Try to understand why Microsoft can include a Linux Kernel (GPLv2) into Windows OS and Marketplace without the need to open source the whole Windows OS
