---
layout: page
title: Version Control with Mercurial
subtitle: Recovering Old Versions
---
All right:
we can save changes to files and see what we've changed --- how can we restore older versions of things?
Let's suppose we accidentally overwrite Salish Sea NEMO forecast planning file with our grocery list:

~~~ {.bash}
$ nano plan.txt
$ cat plan.txt
~~~
~~~ {.output}
Ricotta
Mushroom Tortellini
Bacon
~~~

`hg status` now tells us that the file has been changed,
but those changes haven't been committed:

~~~ {.bash}
$ hg status
~~~
~~~ {.output}
M plan.txt
~~~

We can put things back the way they were by using `hg revert`:

~~~ {.bash}
$ hg revert plan.txt
$ cat plan.txt
~~~
~~~ {.output}
Goal: Run NEMO everyday to forecast storm surge water levels

Need daily high resolution weather forcing from EC.
Also need daily average Fraser River flow from EC.
~~~

As you might guess from its name,
`hg revert` reverts to (i.e. restores) an old version of a file.
In this case,
we're telling Mercurial that we want to recover the last committed version of the file.
If we want to go back even further,
we can use the `--rev` or `-r` flag and a revision number instead:

~~~ {.bash}
$ hg revert --rev 0 plan.txt
~~~

Mercurial really doesn't want to cause us to lose our work,
so it defaults to making a backup when we use `hg revert`:

~~~ {.bash}
$ hg status
~~~
~~~ {.output}
? plan.txt.orig
~~~

The `plan.txt.orig` file is a copy of `plan.txt` as it stood before the `hg revert` command.
It's not tracked by Mercurial.
It's just there in case we made a mistake and really didn't want to revert,
or in case there's some content from before the revert that we decide that we really do want to copy into `plan.txt`.
When we're sure that we don't need `*.orig` files we can just go ahead and delete them.
If we really don't want Mercurial to create `*.orig` files when we use `hg revert`,
we can use the `--no-backup` option,
its short version `-C` or use `hg config --edit` to add

~~~
[alias]
revert = revert --no-backup
~~~
to our Mercurial configuration settings.
That changes the meaning of the `hg revert` command to always be `hg revert --no-backup`.
A better practice than redefining the meaning of an existing command is to give it a slightly difference alias name,
perhaps `nbrevert` (for "no backup revert").

The fact that files can be reverted one by one tends to change the way people organize their work.
If everything is in one large document,
it's hard (but not impossible) to undo changes to the introduction without also undoing changes made later to the conclusion.
If the introduction and conclusion are stored in separate files,
on the other hand,
moving backward and forward in time becomes much easier.
