# Revisions and the Cloud
## Git Tutorial

- Version Control:
  **Version Control** is a system that allows you to revisit various versions of a file or set of files by recording changes. Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes.
  &nbsp;
  - Local Version Control System (**LVCS**):
    this was many years ago , this intails one database on our hard disks that store changes to files.
  - Centralized Version Control System (**CVCS**):
    The need for collaboration within a developer team on a single file or set of files led to the advent of the **Centralized Version Control System** (CVCS). This system entails a single server storing all changes and file versions, which can be accessed by various clients. This streamlined the collaboration process (by eliminating the need to involve all local databases), allowed programmers to have more knowledge of team members, activities with certain files, and gave administrators much more control over divvying up revision privileges.
  - Distributed Version Control System (**DVCS**):
    If a CVS goes down, collaborators cannot work with each other on a file or save changes and new versions. Also, in the event of corruption of a central database’s hard disk — with the absence of backups — all work will be lost, except for any portions on local machines.

    To prevent this type of catastrophic loss, a DVCS allows clients to create mirrored repositories. These data backups can be easily be placed on the server to replace any lost information.Because the DVCS allows for multiple mirrored repositories, programmers working in teams can collaborate with each other in various ways to complete a joint project, which enables the use of various simultaneous workflows.

- ***GIT*** is a DVCS that stores data in a file system made up of *snapshots*. Each time you save a changed version of your project called **commit** Git creates a *snapshot* of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it. **GIT** mostly relies on *local operations* because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.

  Beside the snapshots and local operations GIT has more commands to perform such like *tracking changes* where Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit. And in terms of *loss of data* Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

- Local Repository Structure:
  The local Git repository has three components:
  1. Working Directory: The actual files reside here.
  2. Index: The area used for staging.
  3. Head: Points to the most recent commit.

  ![Repository sections](https://blog.udemy.com/wp-content/uploads/2015/08/image036.png)


 
[Home]( https://kztahat.github.io/reading-notes/)