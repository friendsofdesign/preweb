# Working with Git and GitHub

> Having a distributed architecture, Git is an example of a DVCS \(hence Distributed Version Control System\). Rather than have only one single place for the full version history of the software as is common in once-popular version control systems like CVS or Subversion \(also known as SVN\), in Git, every developer's working copy of the code is also a repository that can contain the full history of all changes.

[https://www.atlassian.com/git/tutorials/what-is-git](https://www.atlassian.com/git/tutorials/what-is-git)

While the above link can give an excellent technical explanation about performance and security, as students it may not seem helpful at all. However, it will be a great read once the terminology is broken down.

Git is a Revision Control, although it can be referred to as Version Control sometimes. Like with Markdown, you may not have heard of this before, but you have probably seen it in action. Dropbox, for example, has a feature that allows you to list all the previous changes on a file, this is Revision Control.

Revision Control quite simply just takes the previous version of a file and the new version, compares them, figures out what has been changed and then saves just the changes as a revision. This is done by saving, mainly, just three things: What's been added, what's been removed and what's been modified.

To do this, Git uses a tool called Diff \(short for difference\). There are many standalone Diff tools available, but the following examples have been taken using [Diff Checker](https://www.diffchecker.com/diff), an online Diff tool.

When a new file is created in Git, it is basically just a diff of all additions:

![](/assets/Screen Shot 2018-04-16 at 11.47.29.png)

...and similarly, when a file is deleted, it is basically just a diff of all deletions:

![](/assets/Screen Shot 2018-04-16 at 11.48.02.png)

When a file is just edited, the diff will contain a list a reference to all characters that have been changed. In extreme cases, if the changes are just too destructive, the entire line or even file will just be automatically replaced with 100% additions:

![](/assets/Screen Shot 2018-04-16 at 11.49.32.png)

The major advantage of Git being a Distributed Revision Control System is that these revisions don't just exist on the editors device, but on all editors devices in the for of a repository. In addition to this "backup" also comes the security of not being able to overwrite someone else's changes. Git will determine what changes to overwrite and what to keep from a previous version. IF it cannot automatically fix these conflicts, it will prompt you to do so.

## Git is not GitHub

It is very important to know that, as the title suggests, Git and GitHub are entirely too separate things. Git is a program that runs on a devices \(your laptop or on a server\) while GitHub is a SaaS \(Software as a Service\) that uses Git to create a social code sharing web application. While the confusion may not come in by simply looking at GitHub, it does when we start to use the GitHub Desktop Client. Even though this application is named GitHub, it is actually just an interface for Git.

Git is a command line application. This means that without an interface like the GitHub Desktop application, you would need to be very comfortable using the command line. Going forward, each example will be presented in both the command line and using the GitHub Desktop application.

It is also very important to note that services like GitHub, BitBucket, GitLab etc are **not** required to use Git, but are recommended. These services are essentially the Git Servers that enable the remote \(distributed\) features of Git. If you are just using Git for revisions, then servers are not required.

## Working with Git

To start using Git, it needs a folder to create a repository in. A repository is where all your files and information regarding the repository will be kept. The all this information is stored in a hidden `.git` folder. This folder should never be removed unless you really want to delete the revision history.

The process of creating a repository is called initialising. This can be done in an empty folder or a folder with existing files. No pre-existing files will be removed or modified.

In GitHub Desktop we can initialise a new repository by using the "Create a New Repository" button and filling in the repository's name. This will automatically create the folder, with the same name as the repository, and initialise a new Git repository.

![](/assets/Screen Shot 2018-04-16 at 14.26.25.png)

Using the CLI \(Command Line Interface\), we will have to create the folder first, go into it and then initialise the repository using the `git init` command:

![](/assets/Screen Shot 2018-04-16 at 14.25.11.png)

In GitHub Desktop you will be presented with a repository "status" screen. This screen will update automatically with any changes you make to any file within the repository:

![](/assets/Screen Shot 2018-04-16 at 14.24.28.png) 



