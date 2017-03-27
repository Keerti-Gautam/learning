## Important Concept

Yep. Important Concept *that I might forget*

X was my master and I was updating it and had one commit to it. The tip is X.1 now, say. After the commit, I thought I would *try* to optimise my code and thus created a new branch called Z and started working on it.  

I do this by `git branch Z` (please note that this creates a branch but our HEAD is still on X).
To move to Z, I do a `git checkout Z` and do the changes that I wish to do. It becomes Z.1 after changes.  

Now I see that I need to update my event page with the details and hence want to move to the master and do the changes. 
I commit my changes in the branch (Now at Z.2) and `checkout` to master and change some dates etc.  
I commit my changes in master and switch back to Z to keep doing ninja stuff with it. Meanwhile, my friend makes a new branch from master viz, Y.1 to do her ninja stuff and I was not aware of that. She does her revisions and now she *merges* her files to master.
(Merging necessarily revises your work and includes changes to master, as well as moves ahead the HEAD, which is the tip)  

Now I might be 
*  Unaware that she had made these xyz changes to the same files that I was working on, and that might create some conflicts in future. 
*  I might know what she did and want to update my branch. 

*How do I do the latter?*
We have two ways for it. We can, git merge or we can git rebase. 
* If I `git merge master` to feature branch, then my uncommitted changes wouldn't be merged, and my HEAD would *move* to a new merge point (new commit). So I'll have her changes then too. This merge may or may not conflict, can't say. This is good except the fact that my uncommitted files would be lost in case of conflict and that this might be tedious and tiring. 
* I can `git rebase master` my Z.2 with the latest changes, which would update it and my HEAD would remain in Z.2 and I can freely work without having to worry about the files that I didn't commit. Now when I have tested the new file and it is working fine, then I can checkout to master and can then *merge* Z.3

I can then change, revise, update my new X and then commit.
In either cases, I need to delete my branches so that they don't take up space unneccesarily. I do that by `git branch -d Z` and `git branch -d Y`

**When you are not authorised to Change the Master or Make a Branch**

When you fork the remote repo to your local repo, you commit your changes and do ninja stuff without changing anything in master, just like you do in branches. But when your remote is upstream, then you can update your repo by 
* You can first  fetch the master see if there are any changes to the file that you were working in, if there are changes then you can do your changes and commit them after which you git merge. 
* You can even git pull (essentially git fetch and then git merge) if you haven't changed anything in your local repo. 

Now you've implemented features and pushed everything to GitHub repo, and now want to get these merged to master. So you create a pull request, and then the authors review it and then merge. Yes. 
