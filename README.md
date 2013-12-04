KK a convenience script to quickly kill any stubborn processes.

Disclaimer:
There is plenty of room for improvement. This script will kill off any process that match the given argument. By default, KK will only

Requirements:
* Ruby
* sys-proctable gem (```gem install sys-proctable```)

Supported platforms:
The sys-proctable gem supports Linux, BSD, OS X, Windows, Solaris, and HP-UX; however, at the moment, this script requires the ```kill``` command. Future versions will likely move to a pure ruby implementation.

Setup:
Add kk to your path. On POSIX-compliant systems:
```ln -s /path/to/kk /usr/local/bin```

Usage:
kk accepts two arguments: the first is the program you wish to terminate, and the second is the signal number (defaults to 9).

```kk firefox```
```kk firefox 2```
```kk 'sublime text 2' 2```
