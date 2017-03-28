### 1. Clone your fork:

    git clone git@github.com:USERNAME/FORKED-REPO.git

### 2. Add remote from original repository in your forked repository: 

    cd into/cloned/fork-repo
    git remote add upstream git://github.com/ORIGINAL-USERNAME/ORIGINAL-REPO.git

Using this command we are adding the source of the original repository from which we want to update our local repository for new changes.

    git fetch upstream

Using this command, we are fetching the contents of the original repo. This command also tells us the status of our forked repo which may be up to date already or some commits ahead or behind the source.

### 3. Updating your fork from original repo to keep up with their changes:

    git pull upstream master

Using this command, we are pulling the contents and merging them with our forked copy of the same repository. 
