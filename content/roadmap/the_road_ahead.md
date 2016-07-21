Title: The Road Ahead

As mentioned in the [Hamster Reboot]({filename}/news/reboot.md) article
'Project Hamster's future lies in a rewrite of its underlying codebase.

The main idea here is to have multiple packages each focusing on a specific task
and potentially depending on each other instead of the current on big blob of code.

This approach allows us and our users to just install the functionality and its
dependencies that they have an interest in. No more mandatory ``dbbus`` if all you
want is using the CLI or start hacking on a flask app.

## Where we are now
As of now, our functional core ``hamster-lib`` covers a significant part of the old 
hamsters functionality. So does our CLI client ``hamster-cli``. As far as the
dbus service ``hamster-dbus`` is concerned, we can say that the bulk of the work has
been done, but we stopped working on this for now as it seemed there were lots of
legacy interfaces involved that are not actually being used by hamster at all.
So investing in replicating them in a backwards compatible manner seemed like a waste.
We will however have to get back to the shell-extension and tray-icon developers
to see what dbus-interfaces they may require to work.
This leave us with ``hamster-gtk``. Whilst being the last part of the old hamster
that I worked on it is clearly the one with the most public visibility.
As of now it is possible to start and stop a *current fact* as well as to display
the overview of already stored facts. This is however far from being production
ready as there is no configuration handling or fact editing capability present
right now. My guess is that we can see some significant progress here within the next
two weeks. Depending on how much extra time will have to be invested in general
project management after the owner change.
One cool feature you may find intriguing is a consequence of us using ``SQLAlchemy``
as default database backend. Whilst the configuration process is not very posished so far
it should be fairly straight forward for interested hackers to get òur clients
to store their data in a remote database. A feature many current hamster users hope
for quite a while now.

## Short term goals
Our immediate goal with this new suite of hamster packages will be to provide the
the same functionality and user experience as ``hamster-time-tracker`` did.
This is our general baseline. That means addressing two remaining major issues:

* Facts need to support tags
* Autocomplete at least for ``Fact.activity`` and ``Fact.category``.


## Mid term goals
One of the common patterns we have seen in multiple issues was that people are missing
certain functionality from the ``hamster-applet`` in the ``hamster-time-tracker``
that succeeded it and that is the baseline for our own development.
Once this first major milestone has been achieved we can start going through those
features and see what can be reimplemented within our new setup without too much work.

## After that
Then, and only then we will have a solid and reliable base for new features and it may
very well not be before the start of the new year that we can work on any of them.
But once we have reached this point we will have a codebase that is

* documented
* tested
* clearly structured

and as a consequence will make it very easy to work with it.
Things that we can already see as useful ideas to contemplate:

* A REST API (using flask?) to expose hamster-lib over a network?
* A Web interface to hamster-lib?
* Maybe even mobile clients that talk to aforementioned API?
* Extended plugin infrastructure.

## What does that mean for you as a contributor
If you want to contribute to 'Project Hamster' and maybe even got a fork going I fear 
this may be bad news. As the current codebase your commits most likely will not be
suitable to our new codebase. However, there is a good likelihood that your work does not need
to be in vain and you are very much encouraged to check out the new code in order to
determine if your changes are still needed and how to incorporate them.
If you have not yet started working on your contributions I strongly advise you to 
check out the future codebase and work from there.

