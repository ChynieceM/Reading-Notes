## Git Tutorial 

* *Version Control* allows you to revisit various versionls pf a file or set by recording changes -- similar to a history.
We can track changes with version control

* Local version contrl (local VCS) has one database on the hard disk that stores changes to the files 

* Centralized VCS - this has 1 server that stores all the changes and the file versions that can be accessed by different people - eliminated the need for Local VCS and gave admins control over revision priveldges 

* Distributed VCS - if something happens to the CVCS ^ the DVCS allows people to make mirrored repositories. If a CVS goes down all is lost or if the central dtabase is corrupted all is not lost with DVCS

**Git** is a DCVS and it stores data in a file system made of **Snapshots**. After each change or commit Git creates a snapshot and stors a reference to it. 

**Local Operations** Git mostly relies on operation bc a project's history is on the local disk whiich emilinates the need to be online to work on a project.

All changes are tracked by git and it will always detect corruption/ loss 
So you wont lose anything

Files in Git will be 
1. Committed - securely stored 
2. Modified - changed but not committed
3. Staged - flagged a files changed version to be commited in next snapshot


#### Commands in Git
To check settings
Getting help
Setting up a repository
-Importing
-Cloning - creating a copy
Check File Status
Tracking and Staging a new file
Committing a file
Committing all changes
Pushing changes
Stashing changes - not ready to trash or committ

##### Remote Repos
These are versions of a project residing online or on a network
-seeing your remotes use a command

Local Repo structure 
Working directory (where the files reside) - Index (area used for staging) - Head (points to the most recent commit)






Questions - do we need to do any of the intial customizations or we did that yesterday? 
