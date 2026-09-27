Hey Connor! I've had a little more time to write this one up.

I wanted to give you a more thorough guide for a couple of subjects.
Ideally you'll have one command you can run as a 'bootstrapping guide'
that gives you enough of a reference to open up other guides.

One way or another that command should point you to opening up this
file for a reference on various things.

# Topics:

- Linux basics: [linux.md](./linux.md)
- using Niri: [niri.md](./niri.md)
- using a terminal: [terminal.md](./terminal.md)
- using text editors (like Helix, Vim, and Nano): [editors.md](./editors.md)
- using dnf: [dnf.md](./dnf.md)
- some tasks to learn (feel free to edit!): [tasks.md](./tasks.md)

# Understanding Markdown

All of my little guides and references will be written as
Markdown files like this one, with the `.md` extension.
I'll give you an overview for what that is and how to view it
properly while you're in this one!

### What is Markdown

Markdown is a lightweight markup language - like a little coding
language that describes what a document should look like. It uses
mostly plaintext with syntax for simple formatting - the idea is
to mirror the things people normally do when they type text without
formatting to indicate it.

For example:
- a dash and a space at the start of a line is rendered as a bullet point
- *asterisks* surrounding some text add *emphasis*, rendered as italics
- **double asterisks** make text bold
- ### One or more hashtags marks a header - more hashtags is a smaller header
- `grave marks` render text as code
- links look like this: [go to google](https://google.com)

There is additional syntax for things like tables, images, mathematical
equations, etc, although these are a little more involved.

Good viewing software will *render* Markdown the way the formatting
describes, usually by converting it into HTML.

### Why Markdown?

HTML is the language used to describe web pages. Your web browser already
'knows' how to render it, and any apps that interally use web technologies
for rendering also 'know' how to render it.

This makes Markdown super useful:
- it is really easy to understand by looking at
- it gives you most of the formatting features you need for everyday use
- it converts to a format that is already rendered everywhere
- it uses basically plaintext files - it isn't stored as some crazy
  complex binary format like MS Word documents, wasting a ton of space on

For these reason Markdown is super popular among techy people. Nearly every
serious coding project has a README.md file in it that gives an overview
of the project. Obsidian and Notion, both popular note-taking and organization
software, use Markdown (Notion uses a proprietary format based on Markdown).
You know I'm not big on AI, but LLMs are built around taking in and spitting
out Markdown. Many software projects now have a CLAUDE.md file to give Claude
Code consistent context when working, and people write "skills" for Claude
in Markdown as well.

### Viewing Markdown

Ok, enough glazing Markdown. I assume you're viewing this in Helix since that's
what I'll tell you to do initially. If you want to look at Markdown documents
as they are properly rendered, you have a couple of options:
- use the software *Obsidian* - I'd recommend this anyway for note-taking
- use a non-terminal text editor like VS Code, with extensions
- use a terminal UI like *Glow*
- view this online at [my Github](https://)

Alternatively, you can keep using Helix! It gives some barebones formatting
that helps to hint at the rendered structure. It's not a bad viewing experience,
just incomplete.
