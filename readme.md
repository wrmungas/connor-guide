# Welcome

Hey Connor!

This page serves as a "bootstrapping guide". What follows are some basic
instructions for setting up the laptop, and links to a bunch of other pages 
I've written with info that will hopefully be relevant and/or cool.

You should be able to view this online at the Github link I send you.
You can access the other pages of this guide from the [main](./main.md)
page; part of the instructions will be getting the files from this
guide onto your computer so you can view them without an internet
connection.

### Expectations

You'll have to forgive my writing style: I like to explain things a
little bit at each step so making progress feels like:
1. motivation for doing something
2. the thing to do
3. understanding what just happened

I think it is helpful to pause to understand not just *how* to do
something, but *why* you're doing it and *what* it really accomplishes.
If that gets tedious you can skim the paragraphs to look for the commands
(formatted like `code`) - but I would of course recommend you pay attention
to really get the most out of this!

With that out of the way, here's what I expect from you:
- keep an open mind
- take this as a learning experience
- be able to roll with problems
- know how to use your resources to at least *try* to solve them

I don't expect for you to know everything from the start, or that everything
will just work right off the bat. Your laptop might have some quirks to it that
are different from my desktop or my laptop, as an older HP. 

Most importantly, I want you to try and have fun! Computers aren't supposed to be
boring - humans have been using them to do silly and fun things ever since they
were invented, just as much as we've been using them to do "real" work. You will
absolutely learn the most if you take a playful attitude towards this one.

Computer science is a world of weird acronyms and quirky nerd culture. Its a lot
of fun to get immersed in, and you'll also have to forgive me if I indulge myself
a little bit by dumping some of that knowledge on you. I'll try to keep lore and
trivia that isn't really relevant in separate files so it isn't too distracting
from the task at hand.

# Getting Started

Boot up your laptop; once it's done you should see a mostly blank screen
with a text login prompt:
```
login:
```

Welcome to the `tty`. The letters stand for 'teletype', a bit of historical
computer science terminology related to command-prompt programs. In Linux,
the `tty` is the basic user interface to the operating system; everything
else, including graphics, is just another user program running on top of the
`tty`. My computer starts the same way; I like it as a little reminder of how
things really work here.

From here on out, the terms `tty`, terminal, shell, and command prompt will
be mostly interchangable. They do have subtle differences in meaning, but
that's not super important and it will be covered in my [terminal guide](./terminal.md).

## 1. Log In

To do anything useful by running commands you first have to log in.

Use the username and password I've texted you. Type them in and hit
'Enter': first the username, then the password. Make sure caps lock
is off!

If the login fails, you will get a message informing you and the login
prompt will repeat. Be careful with your typing and try again!

If the login succeeds, you should see a text prompt like the following:
```
cjm@hp-fedora ~:
```

I'll break this down a little bit more in my terminal guide, but this
is a good sign that you're in. From here you can type in a command, and
once that command is done running and printing its output you will keep
seeing this same prompt.

From here on out, a block of code starting with a `$` indicates a command
to run. The `$` stands for your command prompt, since I can't predict
what exactly that will look like. You can run commands by typing them
and hitting enter. Anything enclosed in angle brackets `<like this>`
is a value you should substitute in rather than copying character-for-character.

## 2. Start a GUI

I don't expect you to master the command line right now; the [terminal
guide](./terminal.md) is for that. Let's start off by getting you into
the graphical user interface I've installed. Run the command:
```
$ niri
```

This starts `niri`, a *window manager* program. I'll explain more about
the environment of this computer in the main guide. For now, you should
see a top bar and an owl-themed background, with a pop-up in the middle
of the screen noting shortcut keys. Press ESC to get out of the pop-up.

## 3. Set Your Password

You can change your password with the `passwd` command. Now that you're
in the GUI, you have start a program called a *terminal emulator* to
give you that same command-line interface to the OS. Open a terminal
window by holding down the super (windows) key and tapping the 'T' key.

You should see a new window pop up on half of the screen, with the same
kind of text prompt you saw at the login `tty`. This is an application
called 'alacritty' (see the `tty` in the name?). It is a much fancier
program with nicer colors and faster performance than the built-in login
`tty`, but ultimately you run the same commands with the same text.

To set your password:
```
$ passwd
```

You will be asked to type your current password, and then your new
password *twice* for confirmation. If the two don't match, the new
password will be rejected. Be careful!

## 4. Clone the Guide

With Alacritty still open, your next step is to clone the files of this
guide onto your computer so you can continue to read them offline. This
is a good way to 'learn by doing' since I'll show you how to access the
files from your terminal as well.

This step will involve a couple of commands.

### 1. Find or Create a Suitable Location

First, you'll want to have a suitable place for these files to live. In
computer science, we tend to refer to folders as 'directories'; I'll use
both terms interchangably.

I believe I made a 'docs' or 'documents' directory for you, and that
would be a sensible place for this new folder to go - but you can put it
anywhere you want.

Terminals maintain a sense of your location in the hierarchy of files on
your computer. You start out in your 'home' directory, which is where
files and folders owned by you live. To accomplish this task you will need
the following three commands:
- `$ ls`: *lists* the files at your current location
- `$ cd <path>`: *change directory*, changes your current location to `<path>`
- `$ mkdir <dir>`: *make directory*, creates a new directory named `<dir>`

**To make a folder within `docs`**:
1. Check that `docs` (or `documents`) exists using `$ ls`
2. Go to `docs` using `$ cd docs`
3. Create a folder, say `guide`, within `docs`: `$ mkdir guide`
4. Go to this new folder, using `$ cd guide`

You can verify the success with another command called `pwd` (*print working directory*):
```
$ pwd
```

This should print something like `/home/cjm/docs/guide`

### 2. Clone the files

Now that you're in a folder you are happy with, run the following command to
fetch the files for this guide from where they are hosted online:
```
$ git clone https://github.com:wrmungas/connor-guide.git .
```

Note the `.` at the end!
This command will print out some output about copying files into `.`, which
is your current location. After it finishes, it should say `Done!`.

You can verify the results with `$ ls`. You should see a couple of files listed
now, all ending with the `.md` extension. `.md` specifies a Markdown file, a type
of file that supports basic text formatting. I use Markdown for all of my guides
as it is super popular for this kind of thing, and it is very readable even
when you view the 'source code' for the file.

## 5. Next Steps

Now that you've got the files on your computer, I recommend you stop viewing
them on Github. Instead we will view the files as they are on your computer,
and learn to use something called a 'text editor' along the way. From here on
out we will move into the main guide.

You should still have a terminal open, and you should still be at the folder
you made for the guide files. Run the command `$ clear` to clear your screen
of any old command output.

Then, open the [main guide](./main.md) using a text editor I particularly like
called Helix using the following command:
```
$ hx main.md
```
