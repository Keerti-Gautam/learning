# Commands

### To create a new branch: 

` git branch xyz ` 

_Note:_ This only creates a new branch, and doesn't switch to it.


### To switch to an existing branch:

` git checkout xyz `

Now all the changes and commits are made on the `xyz` branch (as head is now pointing to `xyz`)
Kindly note that `xyz` is now ahead of `master` (if no changes were made to it in the meantime)


### Switch back to `master` branch:

` git checkout master `

You work has now been reverted to what was done till you created new branch `xyz`
If you commit changes to this branch, then the changes in `master` and `xyz` are isolated from each other. 


### Create a new branch and switch to it at the same time:

` git checkout -b abc `

Do some changes to `abc` and commit using

` git commit -m "Changes made" `


### To merge your changes to master: 

``
git checkout master
git merge xyz
``


### To delete a merged branch: 

` git branch -d xyz `


*Note* that the branch `abc` doesn't contain the changes you did in master after merging `xyz` so you need to merge master into `abc`


## *_Merge Conflicts_*

If you were trying to merge `abc` and `master` (after the merging of `xyz`) and there are some changes which you did to the same part of the file in both the branches, then merging conflict arises.
Merge conflicts, if unresolved, is listed as unmerged after checking the status though `git status`


*In case of no conflicts* 

Git does a three way merging and creates a new snapshot that results from this three way merge and automatically creates a new commit that points to it. This commit now has more than one parent. 


[_Source_](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)

