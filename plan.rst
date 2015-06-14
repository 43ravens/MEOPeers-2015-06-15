*********************************************
MEOPeers Version Control Workshop 15-Jun-2015
*********************************************

ToDo
====

* Add TortoiseHg workflow to 01-configuration
* Add TortoiseHg workflow to 02-create-repo
* Add TortoiseHg workflow to 03-tracking
* Add TortoiseHg workflow to 04-changes
* Add TortoiseHg workflow to 05-history
* Add TortoiseHg workflow to 06-revert
* Add TortoiseHg workflow to 07-ignore

* Add learning objectives to all sections
* Update reference.md to reflect sections structure and content
* Add commands.md

* Add Previous and Next links to section pages

Schedule
========

09:00 to 10:30 (1h30h)

* Intro Slides

  * Pull from seminar deck
  * Separate use of hg for self and for collaboration
  * http://hgbook.red-bean.com/

* Installation

* Configuration

  * hg config --edit

* Create a Repo

  * hg init

* Tracking Files

  * hg status
  * hg add
  * hg commit
  * hg log

10:30 to 10:45 Break

10:45 to 12:30 (1h45m)

* Making Changes

  * hg diff

* Exploring History

  * hg diff -r
  * hg diff -c
  * hg log -r

* Recovering Old Versions

  * hg revert
  * hg revert -r

* Ignoring Things

  * repo .hgignore file
  * glob and regexp syntax
  * user-level .hgignore file

* Working with Remote Repositories

  * Bitbucket.org
  * hg config --local
  * hg push
  * hg clone
  * hg pull
  * hg update
  * hg pull --update

12:30 to 13:10 Lunch

13:10 to 15:45 (2h35m)

* Collaborating

  * Bitbucket public and private repos
  * Bitbucket repo access management

* Merges and Conflicts

  * hg heads
  * hg log --graph
  * hg summary
  * hg merge --tool

* Working with Non-Text Files

  * diff and merge make no sense, so full copies are stored
  * large binary files make large repos and can require lots of memory to manage;
    hg warns you; largefiles extension can help
  * export to text; csv for spreadsheets, rtf for word processing; automation may be possible
  * extdiff extension allows use of custom external diff tools

* Advanced Topics

  * hg commit --amend
  * hg forget
  * hg rm
  * hg cp
  * hg mv
  * hg tag
  * hg tags
  * hg update -r
  * hg pull --rebase
  * ssh keys
  * Bitbucket forks and pull requests
  * other ways to share repos; filesystem, ssh, http, hg serve
