## Branching

Branching means you diverge from the main line of development and continue to do work without messing with that main line.
The way Git branches is incredibly lightweight, making branching operations nearly instantaneous, and switching back and forth between branches generally just as fast. 

*How does git store the data?*

Git doesn’t store data as a series of changesets or differences, but instead as a series of snapshots.

When you make a commit, Git stores a commit object that contains a pointer to the snapshot of the content you staged. This object also contains the author’s name and email, the message that you typed, and pointers to the commit or commits that directly came before this commit (its parent or parents): zero parents for the initial commit, one parent for a normal commit, and multiple parents for a commit that results from a merge of two or more branches.


Need to really visit [this](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell) page to see and learn the whole thing.

***PLease read through it all***

