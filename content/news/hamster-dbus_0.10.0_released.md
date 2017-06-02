Title: hamster-dbus 0.10.0 Released
Date: 2017-06-02

As of today [``hammster-dbus``](https://pypi.python.org/pypi/hamster-dbus) has
been released in it's initial version ``0.10.0``.

While this early release is far from finished it should give interested parties
an idea where we are going with this as well as provide an initial foundation
for integrating hamster with dbus (hence getting closer to hamsters original
feature set).

``hamster-dbus`` contains the means to provide a hamster service that allows
clients just dump their information without caring for any backend logic or be
informed if underlying data changes - something projects like
[``hamster-bridge``](https://github.com/kraiz/hamster-bridge) may find
interesting. In addition to this, ``hamster-dbus`` also provides a new 'dbus
storage backend' that can be used by clients to communicate with a running
'hamster-dbus' service so they do not have to implement the client side logic
themself at all.

Disclaimer: Whilst I invested a significant amount of time into providing a
sane and maintainable unittest setup the reality seems to be that unittesting
dbus is something not really done nor supported, especially when it comes down
to services and their exported objects. In order to get on with things I had
to cut my looses at some point and so the test coverage is not as high as I
would like (but still significantly better that what seems to be the baseline
for dbus services). if anyone has any experience with testing python dbus
code I would very interested in hearing from you :)

I hope you find this useful and wish you all a sunny afternoon
Eric


