### 1. Trying the same commit again

If you commit too early, forget to add some files or mess up your commit message. If you want to try that commit again, you can run commit `git commit --amend` 


### 2. Unstaging an Accidentally Staged file

If you accidentally stage two files using `git add *` or `git add xyz.d abc.md`, you can unstage one file by simply using the command 'git reset HEAD filename.ext`.


### 3. Unmodifying an Accidentally Modified File

After modifying a file with some changes you don't want anymore, you can easily unmodify it – revert it back to what it looked like when you last committed (or initially cloned) by the command `git checkout -- NameOfModifiedFile.ext`. 
Note that, this command wouldn't work for changes which weren't committed (not even for changes which were staged). 
So you change a file X, commit the changes, add hey to the contents of the file again, and then `git checkout --` it, the added hey would be removed.  
