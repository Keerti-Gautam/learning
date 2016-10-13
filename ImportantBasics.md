**How other VCS store their data**
onceptually, most other systems store information as a list of file-based changes.
CVS, Subversion etc systems think of the information they keep as a set of files and the changes made to each file over time.

**How Git stores its data**
Git thinks of its data more like a set of snapshots of a miniature filesystem. Every time you commit, or save the state of your project in Git, it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. 
To be efficient, if files have not changed, Git doesn’t store the file again, just a link to the previous identical file it has already stored. 
Git thinks about its data more like a stream of snapshots.

In fact, Git stores everything in its database not by file name but by the hash value of its contents.
Everything in Git is "check-summed" before it is stored and is then referred to by that checksum. 
So, you can’t lose information in transit or get file corruption without Git being able to detect it.

**Key pointers**

* When you do actions in Git, nearly all of them only add data to the Git database. Hence, we can experiment without the danger of severely screwing things up. 
* Most operations in Git only need local files and resources to operate – generally no information is needed from another computer on your network.
* The mechanism that Git uses for this checksumming is called a SHA-1 hash. This is a 40-character string composed of hexadecimal characters (0–9 and a–f) and calculated based on the data itself (contents of a file or directory structure in Git.) 

*Source* [Here](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)
