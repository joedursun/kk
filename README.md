KK is a convenience script to quickly kill any stubborn processes.

Disclaimer:
----------
There is plenty of room for improvement. This script will kill off any process that match the given argument. For a test run provide a signal of 0: ```kk skype 0```. This will list all processes that match 'skype' but will not perform any actions.

Requirements:
------------
* Ruby
* sys-proctable gem (```gem install sys-proctable```)

Supported platforms:
--------------------
The sys-proctable gem supports Linux, BSD, OS X, Windows, Solaris, and HP-UX; however, at the moment, this script requires the ```kill``` command and therefore may not work across all platforms. Future versions will likely move to a pure ruby implementation.

Setup:
------
Add kk to your path. On POSIX-compliant systems:
```ln -s /path/to/kk /usr/local/bin```

Usage:
------
kk accepts two arguments: the first is the program you wish to terminate, and the second is the signal number (defaults to 9).

```kk firefox 0``` Trial run to see what processes get terminated

```kk firefox``` Send SIGKILL to Firefox (kill -9)

```kk textmate 3``` Send SIGQUIT to Textmate (kill -3)

```kk subl``` Partial names work well

```kk 'sublime text 2' 2``` When the application's name has numbers in it

