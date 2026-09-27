# Linux History

This is both cool to learn about and very helpful for understanding
*why* things are the way they are in Linux.

Linux was born out of three things:
- Unix
- Free Software
- The Linux Kernel

### Unix

Unix was a major operating system from the 1970s onward, though it mostly
died out in the 90s with some modern descendents, among which is Linux.
(The others include BSD, or Berkeley Software Distribution; a version of
Unix created and distributed by Berkeley University in California, for
which they got in a lot of legal trouble; also, Mac OS is actually
basically a more locked-down BSD at its core).

Like a lot of cool things in computing it originated at Bell Labs. It
was created at a time of business mainframe computers, when loads of
people would log in to one really big computer from their own terminals
and do work on it at the same time. It has a file system that reflects
this need, and a model of user permissions designed to allow many people
to work on the same system without interfering with each other.

Also, it *invented* (or at least solidified) a lot of conventions for
how programs work, and how people interact with the computer. At the time
the main interface to the mainframe was a teletype terminal, a keyboard
attached to a screen that could only display lines of text. People
interacted with the computer via a *command-line interface* (cli); they
typed out textual commands for the computer to run, and it responded with
textual output. The abbreviation `tty` is still in use to refer to
*terminal emulators*, programs like Alacritty that follow the same
interaction model. Until Apple, *graphical user interfaces* (GUIs)
and mice weren't really in wide use.

Because you had to do everything by typing, command names got really terse
(short). Most commands are one to three letters long as an acronym or
abbreviation. Take `cd` (change directory) and `ls` (list contents), or
modern package manager commands like `apt` (advanced package tool) and
`dnf` (dandified yum - yum standing for yellowdog updater module). A lot
of commands also ended up being associated with behavior that wasn't really
their intended use. For example:

`cat`:
- stands for "concatenate"
- concatenates (adds) the contents of the first file you list to the second one
- however, with only a single file, it 'adds' the contents to the standard
  output file, effectively printing the contents onto the terminal
- this is now all it is really used for

`touch`:
- updates the 'last modified' timestamp of a file
- but when the file you list doesn't exist, it creates it instead!
- the second behavior ended up being pretty common used

### FSF

The Free Software Foundation is a group of people whose views are responsible
for the creation of Linux at all. It started with a guy named Richard Stallman,
who became very concerned with the legal boundaries around software and source
code. He felt strongly that proprietary software infringed on the rights of its
own users by limiting how they were allowed to interact with it, preventing
people from being able to understand source code to learn from it or even fix
bugs!

He started the FSF to promote free software; 'free' as in 'free speech', not
'free beer' (although usually you don't have to pay to use it too!). Software
started to be developed as open-source: anyone could read the code, create
changes, and ask that they be incorporated into the main version. 

He also started a project called GNU, for "GNU's Not Unix", which was an
attempt to create completely free and open source operating system that was
similar to but independent of Unix. With it he created the GNU General Public
License (GPL), a sort of inverse-copyright software license. Software licensed
under the GPL is required to be free and open source, including any variations
of it or direct forks/modifications. It *also* requires *any other software
that uses it* to be and do the same. Its little brother, the Lesser GPL, relaxes
that second restriction but maintains strictly free and open source status for
the software and its variants. 

The GPL and LGPL have been major boons for the proliferation of free and open
source software. To this day major companies have avoided infringing on it,
simply because they can't risk going to court and setting the precedent that
the GPL is truly enforcable - they might lose proprietary control of a lot of
their own software. Big companies like Microsoft and Google have officially
supported large open-source projects, and even made (some of) their own software
open-source to take advantage of the benefits of this development model (at
least, the parts of the software they consider safe to put in public - the
software still usually relies on something external that is proprietary). GNU
and the GPL have at least forced companies to stay more in line with what
developers want and expect, and as a byproduct software developers can freely
download and modify the source code for nearly all of the major tools they use,
making software development a pretty uniquely accessible field. 

Back to the GNU OS - by the mid 90s they were actually almost all the way there.
The GNU project had its own open-source versions of all of the Unix 'coreutils',
the main set of utility programs on all Unix systems. To have a complete operating
system they only needed to implement a *kernel*, which is the core part of an
operating system that interacts directly with hardware and manages the concept
of computing resources like programs, memory, and files on top of this.

The GNU kernel, called Hurd, was in progress but going slowly and with a lot of
issues. Then Linus showed up.

### Linus

Linus Torvalds gets a lot of the credit for Linux as a whole. He was a computer
science student at the university of Helsinki in Finland who loved writing low-level
code that interacted directly with hardware. He got frustrated with his Operating
Systems class which used a teaching OS called Minix. He could not get Minix to run
on his new intel 386 processor, and he also could not get access to the source to
try and tweak it without paying. 

He ended up deciding he knew enough to at least try it himself anyway, and created
the Linux Kernel. He decided to put it on the internet and make it open source,
understanding that he could only solve so many problems on his own and there were
many other smart people out there who might be able to improve the kernel in ways
he could not.

The kernel's development totally exploded, and people decided to attach the Linux
Kernel to the GNU utilities, since it was the only thing GNU still needed to be a
complete operating system - the result was the first set of Linux distributions.

There is a bit of a historical accident in the name: Linus wanted to call the kernel
Freax, as in "freak" + "unix". However, the person hosting the project decided Linux
was a better name and released it under that name anyway, and it stuck - and it stuck
beyond just the kernel. Despite all of the work GNU put into it, Linus ended up with
the publicity and the catchy name, and most people commonly refer to the family of
OSs as Linux. There are some people who get very bent over this, and insist that we
all call it GNU/Linux. To be completely fair, they are right: Linus only really made
the kernel, and is only part of the overall management and collaboration that maintains
Linux to this day. However, Linux is the name that stuck - everyone recognizes it, it
is easier to say, and most people understand the context anyway and respect the work
that GNU put into it as well. 

# The modern day

This is a good background on the history that led to Linux and explains why a lot of
things are the way they are; but what way are they? To get a sense of the modern
Linux ecosystem you have to understand [distributions](./distros.md).
