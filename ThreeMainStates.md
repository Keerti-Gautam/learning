Git has three main states that your files can reside in: committed, modified, and staged. 

*Committed means that the data is safely stored in your local database. 
*Modified means that you have changed the file but have not committed it to your database yet. 
*Staged means that you have marked a modified file in its current version to go into your next commit snapshot.

This leads us to the three main sections of a Git project: the Git directory, the working directory, and the staging area.

**Git Directory**
The Git directory is where Git stores the metadata and object database for your project. This is the most important part of Git, and it is what is copied when you clone a repository from another computer.
If a particular version of a file is in the Git directory, it’s considered committed. 

**Working Directory**
The working directory is a single checkout of one version of the project. These files are pulled out of the compressed database in the Git directory and placed on disk for you to use or modify.

**Staging Area**

The staging area is a file, generally contained in your Git directory, that stores information about what will go into your next commit. It is also sometimes referred to as "index".


*The main workflow is like the following:*
* You modify files in your working directory.
* You stage the files, adding snapshots of them to your staging area.
* You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory.
