# Welcome to Linux!

I've really enjoyed switching to Linux from Windows systems, but
there's definitely some things that were a rough transition for
me and I'd love to make that smoother for you.

A lot of these are really about mindset shifts. This is a little
more difficult for me than it probably will be for you, for a
few reasons:
- I'm older
- I primarily used the Windows 10/11 desktop for close to 7 years
Whereas:
- You are younger
- You haven't really used a desktop computer much outside of school
- at school you mainly just need to get to Google
- You have used a variety of other devices: iphones, ipads, ChromeBooks,
  the Switch

Still, I'll document a couple of things here to get you started on
the right direction with this system.

# Historical Context

I strongly believe that having any understanding of where something
comes from is helpful in trying to use and understand it.
(of course, you can skip this if you find it really boring)

Linux is born out of three things:
- Unix
- the Free Software Foundation
- Linus Torvalds

I have a more in-depth examination of this all in another file:
- [history.md](./history.md)

The TLDR of it is that Linux inherits a lot old software conventions
from Unix, and has a loose and decentralized development model because
of its roots as free and open-source software.

# Mindset

Because of the history of Linux, you have to have a certain mindset
to use it.

### Software Is Interchangable

One of the biggest things about Linux is that most software is
interchangable, and you don't need most software to actually be
able to use the computer.

Unlike Windows and Mac, this is baked into Linux deeply: even the OS
itself isn't really one single system, but rather a family of related
systems that share a common core, called distributions or "distros".

Each distribution bundles a couple main things with it, but these
core parts are still interchangable - just at the installation
time rather than once you have it running.

To understand more about distributions, see [distros.md](./distros.md).

### You Have Control

You have complete control over your computer. You decide what goes on
it, how its configured, and what its allowed to do with the rest of
the system. This is powerful: if you don't like something, no one is forcing you
to use it (unless it is built into your distro). You can always swap it
out (or swap to a different distro). 

This philosophy is largely tied to Linux's roots as free and open source
software (FOSS). FOSS users really value software that respects them
and places their control first, and this operating system is no different. 

However, giving control to users and providing users with an easy and
comfortable experience are two distinct goals, and they don't often
overlap in Linux. You have to do some work to have the proper
understanding to exercise your control effectively.

### You Have Responsibility

You have the responsibility to learn, tinker, and try to solve problems
yourself. Linux inherits a lot of old stuff, and not all of it is user-friendly.
It has gotten a lot better in recent years, but you have to accept a certain
amount of responsibility in problem-solving on your own.

You can always look for help online or through me, but people on forums (and me,
too) will expect you to have at least tried the basics of figuring things out
yourself. You have resources:
- Google is good
- AI is actually pretty decent at understanding complex and subtle configuration
  issues in Linux, but you have to be detailed and think between the lines - don't
  just blindly copy and past commands if you don't understand what they are doing
- nearly every command has an associated *manual page*, or "man page", accessed
  with the `man` command.

Most commands also give you a very brief guide to using them if you run them with
just the `--help` flag.

If you encounter issues, and your responsibility to solve them gets frustrating,
take a breath. You don't have to know everything or solve things immediately -
you just have to make an honest effort to use the resources that are available
to you already. You can always reach out to me for help if that isn't enough!

### The Terminal is King

If you *really* want to be a power user of your computer you must understand
the terminal. At its heart, *everything* in Linux and Unix comes from a terminal.

I like this setup, without the graphical start, because it serves as a reminder
of this fact. Even your window manager is just another user program started
with some command.

While desktop environments for Linux have come a long way, the terminal still rules
because it is one of the few things consistent across all distros. Since you can
have any of a large number of desktop environments and window managers, you may or
may not be able to solve system problems graphically the way someone else does.
However, every Linux system has some way to get to a command line interface and
run commands in Bash (the *shell language* that the command-line uses).

I have a more in-depth guide to terminals, shells, and commands:
[terminal.md](./terminal.md)

### Software Management with Packages

Installing software on Linux can be done with various graphical interfaces, but
these are all wrappers around the package manager that each distro ships with.

Package managers are pretty easy to use on a command line, and they are pretty
nifty. You simply type the package manager's name as the main command and follow
it with a sub-command, and it will automatically pull information from software
*repositories* online to do what you want. Most package managers support the
following basic operations:
- update: update one or all of your software packages
- install: install a new software package
- search: search for packages, both installed on your system and available online
- info: provide detailed info on a specific package
- downgrade: revert a package version to an older one
- remove: uninstall a package (may or may not fully delete it and its files, since
  you might want to reinstall it - normally just marks it as unusable)

### Your System

Your system has the following:
- Fedora Linux as the base
- Niri as a window manager
- Noctalia as a desktop 'shell' (think of it as a lightweight desktop environment built
  on niri)

I settled on this setup because it is super minimal and I really like the experience
of using a tiling window manager like Niri - you really don't need a mouse much. I
like Fedora mainly because it uses the `dnf` package manager:
- it has a good command-line interface
- it is pretty fast, with clear output
- it hits the sweet spot of software versions: up-to-date, but not so bleeding-edge that
  you encounter bugs

See here for a guide to [dnf](./dnf.md).

You do not have one of the main desktop environment or their usual suites of software;
I have kept this installation basically as minimal as possible. You can add another
desktop environment or apps from it and try them out if you want!

You can even distro-hop if you want and try out different Linux distributions to see
what you do and don't like. This is a great experience, and I have done a little bit of
this myself. I would encourage you to stick with this for at least a little while and
give it a solid try.

