Title: Project Hamster Reboot

Today marks a new beginning for 'Project Hamster'. After several months of
resting in a dormant state 'Project Hamster' is happy and proud to announce that
its hibernation has ended.

Over this past weekend the original creator (Tom Baugis)[https://github.com/tbaugis)
took me [elbenfreund](https://github.com/elbenfreund/) up by my offer to take over
this project. For the last couple of months I have been working on a private rewrite
of hamsters underlying codebase in an effort to make it more pythonic, standards compliant
and easier to maintain.


## Status Quo
It is no secret to anyone following this project that at this point 'Project Hamster'
has multiple serious areas that need improvement. Not all of them are code.
For far to long we have neglected to engage with your community and failed to provide fast
and constructive feedback to motivated contributors. As a consequence our
[main repository](https://github.com/projecthamster/hamster) has currently over a hundred open issues and 
16 open pull requests.


'Project Hamster' is in rather peculiar state right now. From a user perspective it is working
rather OK. Yes people run into issues and miss some functionality earlier versions provided but
all in all 'Hamster' seems to do its job. I guess it is for exactly this reason that we got away
with not making progress on the code for so long.
On the other hand, if one actually looks at the code, one can not help but to notice a significant
amount of fundamental issues that have not been addressed in a long time.

* Little separation of concerns
* Multi class inheritance
* No documentation
* No tests
* No proper python 3 support
* No proper unicode handling
* Not adhering to any python coding convention (pep8, pep257)
* Legacy code
* Custom hand written solutions instead of using established libraries

In light of those issues its rather surprising we got away so easily.
Disclaimer, Before anyone gets the wrong idea: I am honestly eternally grateful for all
the work Tom and all contributors did! I am. But I think it is important to acknowledge
the amount of 'technical debt' we have accumulated in the process. Originally I wanted to write a
accompanying article providing a more detailed analysis of those technical points but unless there is
actual interest I will spend my time on hacking.


## So where do we go from here?
As a direct consequence I personally feel that investing the (huge amount) of time needed
to clean up the existing codebase to be even be able to address those open issues is not the best
use of my time. Instead I did opt to rewrite hamsters core functionality in a way that tries to
address and avoid most of those issues. The result is a set of packages that each for themself
deal with a specific aspect formerly handled by hamster. At the core of this rewrite is a new
'hamster-lib' package that provides a clean and transparent library to handle all time tracking
related work. Additional packages are provided to build on top of that and provide a CLI client, a
DBUS service and the GUI interface. It is worth reiterating that the goal of this rewrite is to be
as close as possible to how 'hamster v2 (hamster-time-tracker)' does things, most of the changes are fundamental but internal.
Whilst not covering all of hamsters current features just yet those packages are already somewhat
'useable' and should provide a good idea about the direction I envision.


Starting over instead of improving existing code is of cause an all to common paradigm in FLOSS
software project and I am well aware of its fallacies. But in this particular case I am confident it
is the right choice and it will pay of very soon by making live easier for every one and hence making
'Project Hamster' more attractive to work on. Especially for new contributors.

## Consequences
As it looks right now, the current [hamster repository](https://github.com/projecthamster/hamster)
will stay as it is. That is unmaintained and deprecated. If you have the time and resources to
invest into cleaning it up and going through its issues and pull request I would love to hear from
you, but if not no additional resources will be directed to this codebase.
This is particularly sad and disappointing to all those people who have created issues and pull requests,
but lets face it - after month without feedback you are not expecting progress on them anymore anyway.
At some point we will go trough all existing 'feature requests' and transfer them to our new solution
if still relevant. All open bug reports will however remain unsettled unless someone steps forward
offering to deal with them.

On the positive side: we have a clear direction to go to and me and hopefully others will invest
significant amounts of time into bringing you a revamped, updated and cleaned up hamster in foreseeable
future. My personal, unofficial, non-binding timeline is to be able to have a proper end user release by
the end of the year. I know this sound like ages away, but I think clear and realistic perspectives
are already a major improvement over the previous lack of communication.
If you are interested 'what takes you so long' and how you can help be sure to check our the article
about our short and midterm roadmap!

## Help us out
So, if you want to contribute to project hamster, but so far have felt disheartened by the lack of feedback
please feel encouraged to get i touch. No mapper if you feel at home in the world of user interfaces,
want to write documentation or want to get your hand dirty reviewing my backend code. All help is welcome.

This being said, all thats left is a big *thank you* towards Tom Baugis and Markus Koller for
taking 'Project Hamster' that far, and my wish to make the best of it.


