# Distributions

Because of the nature of its open-source decentralized development, Linux isn't really
a single operating system, but rather an ecosystem of related operating systems with
the same core. These are called 'distributions', and the way they differ from each other
is subtle in a way that is not always easy for new users to understand. These differences
are more about the philosophy of how they operate under the hood, rather than what how
they *look*.

### What Comes with a Distro

Each distribution bundles a couple of things with it:
- a package manager: a command-line tool for downloading and installing software
- an init system: usually `systemd`
- core libraries: code needed for other code to properly run on the system
- a desktop environment: a graphical user interface for the whole OS
- some default set of user programs, both graphical and command-line based

### Desktop Environments

New users tend to see the *desktop environment* as the OS, because it defines
the look and feel of the OS visually. It is important to remember that the
desktop environment is just another set of programs which are interchangable.

Desktop environments include:
- GNOME: The main GNU desktop, which looks and behaves similarly to Apple
- KDE: A super-customizable desktop that looks and behaves similarly to Windows
- Cinnamon: A derivative of GNOME that is used mostly by Linux Mint, which is
  recommended to new users a lot these days
- Mate: an older, minimal desktop that is simple and effective

GNOME and KDE are also associated with a large number of applications designed
to work best with their respective environments. These are of course usable
on other systems, but they will match the look and feel of their own native
desktop best.

Most distributions let you select which desktop you want from a list of many
options, including the above list and more. Each distro will have slight differences
in their default configurations for each one - for example Ubuntu is famous for
its custom GNOME default environment.

### Major Distros

As for distros, here is a list of a couple of the major distros along with the
things they are known for. Most other distros are just variations on these ones
with additional software pre-installed/configurated. Only the first 6 or so are
ones you are likely to try, as the others are more niche or complicated. Still,
each one is interestingP

1. *Debian*:
  - uses the `apt` package manager and DEB package format
  - uses the GNOME desktop by default
  - focuses on *stability*
  - tends to have older versions of software that are mature and well-established
  - a LOT of other Linux distros are based off of Debian and apt

2. *Ubuntu*:
  - Debian-based
  - famously user-friendly
  - maintained by a company called Canonical
  - ships with a unique variant of GNOME by default
  - recently became controversial for changing apt packages to its own snap software
    system secretly and collecting user data

3. *Mint*:
  - newer Deban-based distro
  - ships with the Cinnamon desktop
  - has overtaken Ubuntu as the gold standard for new-user-friendliness
  - a lot of people have put their grandparents on computers running Mint with no issue

5. *RHEL*:
  - Red Hat Enterprise Linux
  - maintained by the Red Hat Corporation
  - Red Hat doesn't 'sell' RHEL; anyone with the right skills could download and set it up
    themselve, since it is open source
  - rather, they sell large-scale support for RHEL to other big businesses as a service
  - uses the rpm package manager and format
  - focused on security and modern features, especially for servers and containers
  - used to be the main example of corporations trying to take over Linux; Canonical
    has largely taken its place as the main 'big bad' of the Linux community right now 

6. *Fedora*:
  - a community-driven version of Red Hat
  - newer Red Hat features are often introduced to Fedora first for testing
  - uses the `dnf` package manager with RPM packages

7. *Arch*:
  - famously minimal distribution
  - you have to set up most things on your own, and this is not super easy
  - users have a bit of a reputation as egotistical super-nerds - "I use arch btw"
    has become a meme satirizing their bragging
  - uses the `pacman` package manager
  - the Arch Wiki is an excellent source of knowledge for just about anything
    Linux-related, not just for Arch specifically
  - the community-maintained Arch User Repository (AUR) has a TON of unofficial packages
    for Arch (some of which were recently found to have malware)

8. *Alpine*:
  - a super-lightweight Linux distro
  - uses a lighter init system than the standard `systemd`
  - uses `musl`, a minimal version of the standard C library, instead of GNU's `glibc`
  - uses the `apk` package manager
  - primarily geared towards *containers* - virtual Linux environments used to make
    deploying apps to servers much easier, since you can start the app in a consistent
    environment regardless of the machine it is actually running on

9. *Void*:
  - an independent distribution made from scratch
  - uses the `xbps` package manager, which allows installation of packages as binaries
    or compiled from the source code
  - uses `runit` instead of `systemd`
  - can support both `musl` and `glibc`

10. *Gentoo*:
  - an infamous distro based around building *everything* from source code
  - packages are *all* first downloaded as source code, and then compiled on
    your machine
  - known for being difficult to work with, mostly because simple things can
    take a very long time to 1. compile and 2. sort out errors when compilation fails

11. *NixOS*:
  - A newer distro based around the concept of a *declarative system*
  - Uses the Nix language to define the system environment; NixOS then automatically
    rebuilds the system with the required versions of all software
  - really cool idea that lets you do some very interesting things
  - not very new-user friendly, huge learning curve
