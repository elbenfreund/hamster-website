Title: End of Hibernation / State of Affairs

After more than two months of stagnation on my end due to a breakup and
personal challenges I am finally in a position again to muster enough mental
energy to work on project hamster.  First of all I want to take the opportunity
to apologise for my recent absence and express my gratitude for your patience.
I know from personal experience how fast a lack of feedback can discourage even
the most interested contributor to a project and it is my sincere hope that we
will continue to work on hamsters bright future together.

Because this question has been raised in one of the github issues I wish to
also take this as an opportunity to give a brief overview over where we are and
what lies ahead. This seems to be even more important because a simple
glance over the projects individual repositories may lead you believe that
after all this time we failed to provide a viable alternative. In fact, the
opposite is true and here is why:

1. ``hamster-lib`` has become a quite mature backbone for several clients and
	whilst not finished yet I dare say that it surpasses the old codebase in
	several aspects already. Beside several functional and design advantages one of
	its biggest selling points is it's test coverage and documentation.

2. It is certainly true that ``hamster-gtk`` is nowhere ready to function as a
	drop in replacement for our wider userbase, but despite it's looks this is
	mostly due to cosmetics and GUI work. In fact, I personally do use it
	productively (which I still discourage anyone but the most masochistic
	followers :)).  Jan's work has brought this client forward by a long way and I
	hope that he will stay with us to make it even better.

3. The client that suffered the most is very likely ``hamster-cli``. Since its
	 inception ``hamster-lib`` has moved forward by quite a bit and our CLI has
	not really recieved the love it should have. To make matters worse, I
	personally will not have the time to invest much here before the first major
	release. Once the dust has settled with ``hamster-lib`` and ``hamster-gtk`` I
	suspect a concerted effort will be needed to bring ``hamster-cli`` up to speed.

4. Most of my new found energy will go into wrapping up ``hamster-dbus``. It is
	 almost done and the biggest time eater by far is still writing tests in the
	hell's pit that is dbus ... The last big remaining issues here for now will be
	to implement the signals and a basic way of error reporting, something the old
	service never did.

5. ``hamster-shell-extension`` is in a horrible place right now. Whist we
	invested some time restructuring its codebase we currently do not have a
	new dbus-service ready that we can develop against. One such a service
  can be provided we should be in a far better position to clean things up and
	come up with an updated and improved extension rather fast.

The big picture and main reason why there may seem to be a lack of progress
here is that whilst all the individual repositories are actually moving along
and have reached a somewhat decent stage already we are currently not in a
position to 'string it all together' just yet. Which brings up straight to the
road ahead: 
1. Once ``hamster-dbus`` is ready we will be able to integrate it into
	 ``hamster-gtk``.
2. This should provide a major boost, not the least to
	 ``hamster-shell-extension`` that will finally have a proper dbus-service to
	query against.
3. Once there, all that's left to do to have a somewhat usable initial client is
	 to fix some GUI details and we should be good to go.

I hope those few paragraphs provided some insight into the current state of affairs
and reassured you of the project still being alive and kicking. As always: if you
are interested in helping out do not hesitate to drop us a line!
For now, I will come to an end and focus on working on some actual issues. :)

