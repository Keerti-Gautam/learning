**Version Control**

Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later. 
It allows you to revert files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. Using a VCS also generally means that if you screw things up or lose files, you can easily recover. 

*Local VCS*

==Need== Copying files into another directory is error prone. 
  
A  local VCSs has a simple database that keeps all the changes to files under revision control.
One of the more popular VCS tools was a system called RCS, which is still distributed with many computers today.
RCS works by keeping patch sets (that is, the differences between files) in a special format on disk; it can then re-create what any file looked like at any point in time by adding up all the patches.

Example: RCS

*Centralised VCS*

==Need== Can't collaborate with other fellow developers with Local VCS.

Centralised VCS have a single server that contains all the versioned files, and a number of clients that check out files from that central place. For many years, this has been the standard for version control. 

Example: Subversion, Perforce etc 

==Advantages==
* Everyone knows to a certain degree what everyone else on the project is doing. 
* Administrators have fine-grained control over who can do what; and it’s far easier to administer a CVCS than it is to deal with local databases on every client.

==Disadvantages==
* If that server goes down for an hour, then during that hour nobody can collaborate at all or save versioned changes to anything they’re working on.
* You have the entire history of a project/software in a single piece so you have risk of losing everything altogether in case the server loses data by mistake, or a hard disk gets corrupted.

*Distributed VCS*

==Need== Shortcomings of CVS

In a DVCS, clients don’t just check out the latest snapshot of the files: they fully mirror the repository. Thus if any server dies, and these systems were collaborating via it, any of the client repositories can be copied back up to the server to restore it. 
Every clone is really a full backup of all the data.

Example: Git, Mercurial

==Advantages== 
* These systems deal pretty well with having several remote repositories they can work with, so you can collaborate with different groups of people in different ways simultaneously within the same project.
* Allows you to set up several types of workflows that aren’t possible in centralized systems, such as hierarchical models.
