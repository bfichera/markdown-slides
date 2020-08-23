**Using markdown, write simple but beautiful presentations with math,
animations and media, which can be visualized in a web browser even without
an internet connection.**

See the official [repo](https://gitlab.com/da_doomer/markdown-slides) on Gitlab.

This program appropriately inserts markdown files into Reveal.js files,
completely avoiding the need to edit HTML files directly.

# Quick start

For example, to compile the example presentation:

```
git clone https://gitlab.com/da_doomer/markdown-slides.git
cd markdown-slides
python make.py presentation.md --include media
```

# Usage

```
python make.py [-h] [--include RESOURCE] [--pdf] FILE
```

Notes:

 - PDF exporting requires chromium (see [PDF exporting on
	 reveal-js](https://revealjs.com/pdf-export/)).

# Features

Some of Reveal.js's features are:

- LaTeX syntax.
- Automatic animations.
- Background videos and images.

MathJax is bundled in this repository, so web browsers do not need internet
connection to display the presentations.

# Why:

 - Markdown is simple and portable. You can write markdown in a cellphone or
 in a remote server.
 - You want to write equations in LaTeX.
 - PDFs have no support for videos, but HTML does.
 - PowerPoint and LibreOffice are not available in all computers, but virtually
 every computer has a web browser.

# Syntax:

For a quick start see the example [`presentation.md`](./presentation.md).
If you need a quick refresher on markdown see e.g.
[this cheatsheet](https://www.markdownguide.org/cheat-sheet/), the
[CommonMark reference page](https://commonmark.org/help/), or this
[Gfm tutorial](https://guides.github.com/features/mastering-markdown/).

You will not have to break your markdown files to use this program. Control
Reveal.js' theme and options using CommonMark-compliant comments:

```md
[comment]: # (Set the theme:)
[comment]: # (THEME = white)
[comment]: # (CODE_THEME = white)

[comment]: # (Pass optional settings to reveal.js:)
[comment]: # (controls: false)
[comment]: # (keyboard: true)
[comment]: # (markdown: { smartypants: true })
[comment]: # (hash: true)
```

Everything but slide-break comments and option comments is passed to Reveal.js verbatim. Check out their documentation, especially the [markdown section](https://revealjs.com/markdown/).
