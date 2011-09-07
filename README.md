# What is it? ##
TUT is a telnet replacement that has some nice extra features:

* BASH-like command history, which lets the user use ↑/↓ and `C-r`
  to go back to and search for previous commands.
* Custom defined command completion, editable through the source code
* Sane quitting - just `C-c`, not `C-] exit`

# Compilation #

### Dependencies ###

* GNU Readline (on ubuntu: `sudo apt-get install libreadline-dev`)

### How to ###

    gcc -lreadline -o tut tut.c

or

    make tut

# Usage #

    tut ${server} ${port}

e.g.,

    tut localhost 2020

# More Background ##
This is something I wrote over the summer of 2010 while working for
the [SNO+](http://en.wikipedia.org/wiki/SNO%2B) team at the
[High Energy Physics](http://www.hep.upenn.edu/HEP_website_09/SNO/SNO.html) department
of the University of Pennsylvania. My role in the project was focused on rewriting and
improving the existing DAQ (digital acquisition code) which allows for data to be collected.
One of the biggest gripes the team had at the time was the fact that Telnet doesn't have
the capability for a BASH-like command line history retrieval through the ↑ and ↓ arrows.
Using the GNU readline library and the socket programming I learned improving the DAQ, I
quickly threw this together.
