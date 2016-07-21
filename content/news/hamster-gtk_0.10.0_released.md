Title: Hamster-GTK 0.10.0 Released

Just a few seconds ago the initial release of ``Hamster-GTK``, version 0.10.0,
has been uploaded to the
 [cheese shop](https://pypi.python.org/pypi/hamster-gtk/0.10.0). That means
 that after the rewritten backend codebase ``hamster-lib`` has been out in the
wild for a few days by now you can now have a first look at a reimplementation
of the original hamster 2.0 GUI.
It will come as no surprise that this current early version is rather
unpolished and leaves a lot to be desired. However, if you are familiar with
``legacy hamster 2.0`` aka ``hamster-time-tracker`` you will surely see some
major resemblance.

I personally think that one of the most striking improvements with this release
is actually the ease with which you can give it a try.
No buildchain, no arcane dependencies, simply get some GTK bindings, setup a
virtual env and pip install and you are good to go. This is something I
personally find highly attractive. For details please refer to the readme.

This first version already allows for realtime tracking of activities
as well as editing and listing of existing entries. Furthermore a basic
dialog to adjust config settings as well as export data as ``tsv`` is present
 as well.

Once caveat is that any changes to the preferences will only take effect after
the application is restarted, which is due to some limitations of
``hamster-lib``. While developing this first prototype some additional lessons
could be learned with regards to ``hamster-lib`` and whilst I am eager to
continue working on ``hamster-gtk`` I feel that it would be best to apply
those lessons to our backend code first.

In the meantime I hope you read this release more as a vivid sign of Project
Hamsters revived activity rather than the definitive final product it is not.
Please be sure to file bug reports and feature requests as you see fit
with the [issue tracker](https://github.com/projecthamster/hamster-gtk/issues).


