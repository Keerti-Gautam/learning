## Doubt Encountered No. 1
I had made a folder called Branches in the root folder of my repository, and had manually transferred (cut and pasted) some files from the root inside the folder. I, then staged the repository Branches, committed the changes and pushed them to the remote.

### Observation:

The files in the root which were moved to Branches were still there in the remote but not in my local repository. Unexpected behaviour for a newbie like me.

Meanwhile, the transferred files were there in the folder Branches.

What followed was that I saw the status of the files in the root by using `git status` and saw that git had recorded those transferred files as deleted but those files were unstaged. I staged them, and then committed my changes and pushed to remote and voila! there were deleted from the remote too!

### Inference: 

The deleted files is also an activity which is recorded, and just like every activity (every change), even deleted files are *required* to be staged and committed for any changes to show in the remote. 

## Doubt Encountered No. 2
I had made another folder named VersionControlOfFolders, staged it and created a single file inside it, say XYZ.md and put some nonsense content in there, and staged it too. Since the content was not making sense at all, I had to remove it from git history so I `git -rm --cached XYZ.md`. I thought that this would only remove my file from the history and eventually from the remote when I `git push` it but what happened was unexpected behaviour. 

### Observation: 
Committing the above changes to remote, first the addition of file to the repository and then removing the file from the git history, I saw the folder VersionControlOfFolders being created upon first commit and getting deleted from the git history and eventually from the remote. Why? I had no answer. 

### Help from Community: 

Since I got no answer from the web, I had called my friend [Saksham Saxena](https://github.com/sakshamsaxena) and told him this behaviour. He explained that the folders which are empty remain untracked by git, which is why in the next commit, the directory was removed from the git tracking and eventually from the remote. 
