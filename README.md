forkbomb
========

Simpliest one liner fork bomb for Linux/Unix written in C++.

For clearer code the source was rewritten in ANSI C++ style. But I think the
one liner version is pretty understandable.

This code has one drawback - you can press ctrl-c and end the program, and then
the OS gets back to its normal cpu load.
If you have got an idea to improve the forkbomb app - please send me a pull
request.

Example test scenario:

1. Create a VM (eg. virtualbox one)
2. Copy one of the source files to the VM
3. Compile the code
   g++ onelinerforkmbomb.cpp -o onelinerforkbomb
   sudo cp onelinerforkbomb /usr/local/sbin
4. Add the fork bomb execution to system startup script
   vim /etc/rc.local
   put the following code (before exit 0 statement):
   /usr/local/sbin/onelinerforkbomb
5. Reboot the OS

REMEMBER!

   Don't do it on production systems or you laptop/box!!!

best regards,

bartgee
