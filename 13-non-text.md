---
layout: page
title: Version Control with Mercurial
subtitle: Working with Non-Text Files
---
> ## Learning Objectives {.objectives}
>
> * Explain how Mercurial handles non-text files.
> * Explain some strategies for enabling Mercurial to show diffs of non-text files.
> * Explain what issues are associated with large binary files and how they can be mitigated.

There are no theoretical limits on the kinds of files that Mercurial can handle --- it's all just data,
and data can be version controlled by Mercurial.
There are,
however,
some practical limitations:

* `hg diff` doesn't have much meaning for files that aren't intended to be read by humans
* merging makes no sense to binary data,
so Mercurial stores a full copy of binary files each time they are committed

For more details,
see the discussion of [binary files](https://mercurial.selenic.com/wiki/BinaryFiles) in the Mercurial wiki.

One strategy for working with non-text files like those stored by word processor and spreadsheet programs is to export the files contents to a human readable form
(e.g. Rich Text Format (RTF) for word processor files,
Comma Separated Values (CSV) for spreadsheets)
before each commit and track the human readable version of the file in parallel with the machine readable version.
Doing so allows `hg diff` to be used on the human readable files.

Mercurial's built-in [`extdiff` extension](https://mercurial.selenic.com/wiki/ExtdiffExtension) provides a mechanism that can be used to integrate custom external diff tools.

Binary files are often large,
and storing large files requires a lot of memory in order to avoid degrading Mercurial's performance.
Mercurial will warn you when you try to track a file that is likely to cause memory issues.
Practical file size limits vary with operating system and the amount of RAM in your machine,
but files larger than several hundred Mb will often cause the warning to appear.
There is presently a hard upper limit of 2 Gb.
However,
the built-in [`largefiles` extension](https://mercurial.selenic.com/wiki/LargefilesExtension) provides one mechanism to work around large file issues,
The downside of using `largefiles` is that there is a cost of extra setup and storage infrastructure and reduced portability.


> ## Learning Objectives {.objectives}
>
> * Explain how Mercurial handles non-text files.
> * Explain some strategies for enabling Mercurial to show diffs of non-text files.
> * Explain what issues are associated with large binary files and how they can be mitigated.
