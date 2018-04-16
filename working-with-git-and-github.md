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



