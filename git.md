# Git and  github



## Git:
Definition: Git is an open-source distributed version control system primarily used to track changes in source code during software development. It allows multiple developers to collaborate on a project simultaneously.

### Key Features:

Version Control: Git keeps track of changes made to the codebase, allowing you to revert to previous versions if needed.
Distributed: Every user has a local copy of the entire repository, enabling them to work offline and independently.
Branching and Merging: Git supports branching, enabling developers to work on separate features or fixes in parallel and later merge them into the main codebase.
Collaboration: Multiple developers can work on the same project and merge their changes without conflicts.
Usage: Git is used locally on a developer's machine. Developers use Git commands in their terminal to manage their local repositories, create branches, commit changes, and more.

## GitHub:
Definition: GitHub is a web-based platform that provides hosting for Git repositories. It offers collaboration features like issue tracking, pull requests, and project management tools, making it a powerful platform for collaborative software development.

 ### Key Features:

Remote Repository Hosting: GitHub hosts Git repositories in the cloud, making it easy for developers to share and collaborate on projects.
Pull Requests: Developers can propose changes to a repository and request to merge these changes into the main branch, facilitating code reviews and discussions.
Issue Tracking: GitHub provides a platform for tracking issues, bugs, enhancements, and tasks related to a project.

Collaboration Tools: It offers features for team collaboration, including wikis, project boards, and actions (CI/CD), enabling automation of development workflows.
Usage: GitHub is used through a web interface. Developers can create repositories, manage issues, review and merge pull requests, and collaborate with other team members.

### Differences:
Nature: Git is a version control system (VCS), while GitHub is a web-based platform for hosting Git repositories and facilitating collaboration.

Location: Git is installed and used locally on a developer's machine, managing version control locally. In contrast, GitHub is a cloud-based platform where Git repositories are hosted and accessed through a web browser.

Functionality: Git focuses on version control and local repository management. GitHub adds collaboration features on top of Git, enhancing project management, code review, issue tracking, and more.

In summary, Git is the version control system that runs on your machine, allowing you to manage the versioning of your code locally, while GitHub is a cloud-based platform providing a collaborative environment for developers to host, share, and collaborate on Git repositories. GitHub enhances the capabilities of Git by adding collaboration and project management features.


## there are two types of version controls right?? what are those and how they are different from each other . Could you just tell how git is DVC not CVC #
There are primarily two types of version control systems (VCS): Centralized Version Control (CVC) and Distributed Version Control (DVC). Let's delve into how Git fits into the category of Distributed Version Control (DVC) and how it differs from Centralized Version Control (CVC).

## Centralized Version Control (CVC):
In a Centralized Version Control (CVC) system, there is a central server that holds the master repository. Developers check out the code from this central repository to work on it locally. They commit changes back to the central server, which tracks versions and manages conflicts.

### Key Characteristics:
Central Repository: All developers connect to a central server where the repository is stored.
Dependency on Central Server: Operations like history viewing, branching, and merging often require communication with the central server.
Single Point of Failure: If the central server goes down, it can halt development activities.
Distributed Version Control (DVC):
Distributed Version Control (DVC) allows each user to have a complete local copy of the entire repository, including its history. This means that every user has a full-fledged repository, including all branches and history, on their local machine.

### Key Characteristics:
Local Repositories: Every user has a local repository containing the entire project history.
Decentralized Workflow: Developers can work independently, without a constant connection to a central server.
Branching and Merging Efficiency: Branching and merging are fast and efficient since all operations are local.
Git as a Distributed Version Control (DVC) System:
Git is a prime example of a Distributed Version Control (DVC) system. When you clone a Git repository, you get a complete copy of the entire repository, including all branches and history, on your local machine. This enables you to work independently and efficiently even without an internet connection or connection to a central server.

## How Git Differs (DVC):
Local Repository: When you clone a Git repository, you have the complete repository on your local machine, including all its history and branches.
Offline Work: You can work on your code, create branches, commit changes, and even merge branches entirely offline.
Efficient Branching and Merging: Branching and merging are very fast and lightweight since Git deals with local repositories.
In summary, Git is a Distributed Version Control (DVC) system, where each user has a complete copy of the entire repository on their local machine. This allows for offline work, efficient branching and merging, and provides more robustness and flexibility in collaborative software development compared to Centralized Version Control (CVC) systems.

## Basics commands on the command line

#### To change directory
`cd`
### To list all the files in the directory
`ls`
### To print working directory
`pwd`
### Make directory
`mkdir`
### Create empty file
`touch file_name`
### Copy files and directories from one location to another
`cp`
### move or rename files from one location to another
`mv`
### remove files and directories 
`rm`
### Concatenate and display the content of the file
`cat`
### Display file content page by page 
`less`
### Display first few lines of the page
`head`
### Display last few lines of the page
`tail`
### Search for specific pattern or words in the file
`grep`
### Seach for specific files and directories based on specific criteria
`find`


chmod - Change file permissions:

Modify the permissions (read, write, execute) of a file or directory.
chown - Change file ownership:

Change the owner of a file or directory.
ps - Display information about running processes:

Display information about the active processes.
kill - Terminate processes:

Terminate or send signals to running processes.
df - Display disk usage:

Show information about disk space usage.
du - Display file and directory space usage:

Show disk usage for files and directories.
tar - Archive files:

Create or extract tar archives.


### List config details
 `git config --list`
 ### Change the username of the configuration
 `git config --global user.name "Name"`
 ### Change the email id of the configuration
 `git config --global user.email "email@gmail.com"`
 









