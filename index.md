---
layout: page
title: Version Control with Mercurial
---
Version control is the lab notebook of the digital world:
it's what software developers use to keep track of what they've done and to collaborate with other people.
Every large software development project relies on it,
and most programmers use it for their small jobs as well.
And it isn't just for software:
instructional materials (like this),
papers,
theses,
small data sets,
and anything that changes over time or needs to be shared can and should be stored in a version control system.

Version control is better than emailing files back and forth because:

*   Nothing that is committed to version control is ever lost.
    This means it can be used like the "undo" feature in an editor,
    and since all old versions of files are saved it's always possible to go back in time to see exactly who wrote what on a particular day,
    or what version of a program was used to generate a particular set of results.
*   It keeps a record of who made what changes when,
    so that if people have questions later on they know who to ask.
*   With version control it is hard (but not impossible) to accidentally overlook or overwrite someone's changes:
    the version control system automatically notifies users whenever there's a conflict between one person's work and another's.

This workshop shows how to use a popular open source version control system called [Mercurial][mercurial] (also known as `hg`).
It is widely used,
both because it's easy to set up,
and because of a hosting site called [Bitbucket](http://bitbucket.org).
No matter which version control system you use,
the most important thing to learn is not the details of their more obscure commands,
but the workflow that they encourage.

[mercurial]: https://mercurial.selenic.com/


> ## Getting Ready {.getready}
>
> Follow the [setup instructions](setup.html) to install [Mercurial][mercurial] or [TortoiseHg](http://tortoisehg.bitbucket.org/),
> and [KDiff3](http://kdiff3.sourceforge.net/) on your laptop.
> If you are working on Windows,
> TortoiseHg is the easiest way to get everything (including KDiff3) installed.


## Topics

### The Basics
0. [Setup Instructions](00-setup.html)
1. [Configuring Mercurial](01-configuration.html)
2. [Creating a Repository](02-create-repo.html)
3. [Tracking Files](03-tracking.html)

### Day-to-Day Mercurial
4. [Making Changes](04-changes.html)
5. [Exploring History](05-history.html)
6. [Recovering Old Versions](06-revert.html)
7. [Ignoring Things](07-ignore.html)

### Reaching Out
8. [Remote Repositories](08-remote-repos.html)
9. [Working with Clone Repositories](09-repo-clones.html)
10. [Collaboration](10-collaboration.html)
11. [Merging Changes from Different Clones](11-merges.html)
12. [Merge Conflicts](12-conflicts.html)

### Digging Deeper
13. [Working with Non-Text Files](13-non-text.html)
14. [Other Topics](14-other-topic.html)


## Other Resources

* [An Intro to Version Control Slidedeck](intro-slides.pdf)
* [Mercurial Web Site](https://mercurial.selenic.com/)
* [Mercurial: The Definitive Guide](http://hgbook.red-bean.com/) (also known as "The Red-bean Book")
* [Mercurial Command Reminders](commands.html)


Some of the instructional material in this workshop is based on the [Software Carpentry Foundation][swc] lesson that introduces [Version Control with Mercurial](http://swcarpentry.github.io/hg-novice/).
The design of the web pages is also adapted from the [Software Carpentry][swc] lessons pages.

[swc]: http://software-carpentry.org/
