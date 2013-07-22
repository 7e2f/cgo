cgo - a terminal gopher client
==============================

Summary
-------

cgo is a UNIX/Linux terminal based gopher client. It has no other
dependencies than libc and some syscalls. It should run on every
VT100 compatible terminal. To show media like images, music or
webpages it relies on external programs you can specify.


What does cgo mean?
-------------------

cgo means more or less, the "c go"pher client. And c could
stand for C (the programming language), colorful or console.
You may choose one of the meanings or propose other :)
(but please not crappy!)


How to install
--------------

Grab the source code, open cgo.c and adjust the external programs
to your needs. You can also change the default gopherhole where
cgo connects on startup without any parameters (e.g. you can
tell cgo to connect directly to some Veronica search engine).
And if you don't like the default colors, you're able to change
them also here.
If you're done with changing the defaults, just "make" the
final binary.


Parameters
----------

In case you omit all parameters cgo will show you the default
gopherhole specified in the source file.

 * -h [host]        use this host to connect
 * -p [port]        use this port to connect
 * -s [selector]    use this selector on startup
 * -H               show usage
 * -v               print version


Usage
-----

 When "surfing" in the gopherspace cgo only present you
 directory listings. Every selector is preceeded with two
 ascii chars. By typing in both chars cgo will jump to
 the given selector. Every time you jump to another
 directory listing cgo generates a history entry (like every
 browser). To show other media cgo uses external programs
 to present it (e.g. less, display, mplayer, firefox).
 Following commands are understood by cgo:

  * ?       help
  * <       jump back in history
  * *       reload directory
  * [xx]    show / jump to selector
  * .[xx]   download selector
  * h       show history
  * h[xx]   jump to specifiy history item

[xx] stands for the two colored letters in front of selectors.


Todo
----

 * write a man page or something like that
 * configuration files (editing code is not that easy for everyone)


Bugs
----

 * none I'm aware of :)


Feel free to use this small gopher client. I hope you'll
find it as useful as I do. Send me comments or patches it you
like. I would appreciate it.

