---
title: On Picking Code Editor
date: 2016-07-04 16:18:35
tags: tools
---

{% img /images/on-picking-code-editor.png %}

### Motivation
Happy July 4th! During the holiday I've decided to take another look at the new shiny Atom/Nuclide code editor. Although I've spend a couple of years on Sublime test, and a year or so on Emacs, exploring great tools it still great fun.

After poking around for three hours, it turns out to be a NO. And I would like to reason about it.

### Modal editing is a blessing

As discussed in a previous post, the majority of the time spent in text editors is actually browsing around. Atom really shines at displaying code in a beautiful GUI, and it offers fuzzy search of file names that are on par with all of other editors. However when it comes to defining clear modal contexts, it falls short.

Vim/emacs are defined with clear context in mind, which allows maximum knowledge transfer after one learns about the basic of one context. If you are in a grep-mode, you can expect all the shortcuts (most important ones are 'n' and 'p') to work in that context. In Atom it's a chaos of interfaces. Each plugin tries to define some unique UI that does not follow the convention of the others. And the shared context is nowhere defined.

### Command line efficiency

I spend a great amount of my day working in terminal window, which is a great time-saver. For almost all known tools, command-line versions have less bugs and run much faster. The performance for Emacs to open a file is noticeably faster than atom. Same for syntax highlighting and automatic styling code.

For finding hidden features in the editor, all editors evolved into some search solution. On Atom this is achieved with command palette fuzzy search, on Emacs this is done via ido.el/helm.el. In a GUI setting Atom wins for much easier access to commands and descriptions for each selection.

### After all, coding speed is limited in thoughts, not tools

For over 50 years, engineers are stuck on keyboards and they have yet to discover/input a better input device. If this does not change, the efficiency for human-code interaction is not likely to see a dramatic change simply from improving current tools.

In a nutshell, software is purely thought stuff. And for most engineers, the real bottleneck for productivity is actually the speed of organizing thoughts. It would certainly be easier with better tools. But as far as thoughts are organized into texts, mainstream editors are almost equal at efficiency.
