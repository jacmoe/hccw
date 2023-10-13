+++
title = "Emacs"
author = ["Jacob Moena"]
draft = false
weight = 1
+++

## Introduction {#emacs-introduction}

> “I use emacs, which might be thought of as a thermonuclear word processor... the engineer-hours that, in the case of Microsoft Word, were devoted to features like mail merge, and the ability to embed feature-length motion pictures in corporate memoranda, were, in the case of emacs, focused with maniacal intensity on the deceptively simple-seeming problem of editing text. If you are a professional writer... emacs outshines all other editing software in approximately the same way that the noonday sun does the stars. It is not just bigger and brighter; it simply makes everything else vanish.”

<div style="font-size:0.7em;font-style:italic;padding-left:30px;padding-bottom:40px;">

-Neal Stephenson, 1998 ([In the Beginning... Was the Command Line - Wikipedia](https://en.wikipedia.org/wiki/In_the_Beginning..._Was_the_Command_Line))

</div>

I can make Emacs fit my workflow rather than the other way around.

{{< figure src="images/hackerman1.jpg" alt="Hackerman" title="Hackerman" width="40%" >}}

Emacs is a LISP machine.


## Emacs basics {#emacs-basics}

[Emacs Basic Movement and Editing](RuiBsWQeeTs)
It’s highly recommended to run Emacs without any customization a couple of times to learn how the basic Emacs commands work. We can do that by running Emacs with the `Q` command-line argument, like this: `emacs -Q`. If you want—again, highly recommended—you can run the Emacs Tutorial by running `C-h t`. Do the tutorial until you feel confident. Also, experiment in the Scratch buffer, like in the video tutorial above.

<br/>

Common Emacs commands:

-   `C-x C-f` : `find-file`, allows you to open an existing file. If the file doesn’t exist, create a new file.
-   `C-x C-s` : `save-buffer`, saves buffer to disk.
-   `C-x b` : `ibuffer`, show a list of buffers in the minibuffer, and allows you to switch to a different buffer.
-   `C-x C-b` : `ibuffer`, runs ibuffer in a new window (use `q` to quit).
-   `C-x k` : kill (close) buffer.
-   `C-x C-c` : quit Emacs.
-   `C-o` : `org-open-line` : inserts new line below point.
-   `C-x 2` : split window in two, one below another.
-   `C-x 3` : split window in two, side-by-side windows.
-   `C-x o` : switch to other window.
-   `C-x 0` : close window.
-   `C-x 1` : close other windows.
-   `C-<space>` : toggle the mark.
-   `C-w` : kill (cut) text between point and mark. _(‘w’ is for “wipe”)_.
-   `M-w` : (copy) save region, but don’t kill it. _(‘w’ is for “wipe”)_
-   `C-y` : yank (paste) first item from the kill-ring.
-   `M-y` : display items in the kill-ring to yank (paste) into the buffer.

<br/>

To get out of trouble, use `C-g` (keyboard quit) to cancel whatever it is that Emacs is doing at the moment. Use `C-x C-c` to rage-quit if you need to (I admit that I have when I first started out). `C-x u` will undo, and `C-?` will redo. Use `C-x C-s` to save current buffer. If the current buffer is a horrible mess, you can run `M-x revert-buffer` to get back to whatever it was when you loaded it from disk (by doing a `C-x C-f`). Also, sometimes you will want to toggle a file read-only. You can do that by pressing `x C-q`.

<br/>

Press `C-h` to view a list of options to get help. Especially useful is `C-h k` when you want to know what a keyboard command does without running it first. For example, pressing `C-h k <F4>` will tell you that it runs the command `kmacro-end-or-call-macro`. Press `q` to close the help window.

<br/>

If you want to read a comprehensive—very much so—guide to Emacs, the history, and the details of how it works, read my massive [Creative writing with Emacs](https://jacmoes.wordpress.com/2019/09/24/creative-writing-with-emacs/) blog post from 2019. It delves into the mechanics of Emacs in much more depth, leaving us free to explore Emacs as a writer’s toolbox. So, if you are completely blank with regard to Emacs, I highly recommend that you read at least the first part of it before continuing.

<br/>

And, before you ask, let me tell you my favorite Emacs command: `C-o` (_insert new line below_); I use it all the time!

<br/>

Now that you know a thing or two about Emacs, here’s another introductory video about Emacs as a text editor:
[The Basics of Emacs as a Text Editor](jPkIaqSh3cA)
NB: He uses the `<Esc>` key as an alternative to `<Control>` like in `<Esc> y`. May I suggest that you use `C-y` instead. Using the Escape key that way will conflict with the modal editing package Boon mentioned below./

<br/>


## Doom-Emacs {#emacs-doom-emacs}

[Doom-Emacs](https://github.com/hlissner/doom-emacs) is a minimalist modern Emacs distribution that is light and fast. It provides a rock-solid and highly configurable infrastructure to base an Emacs configuration on.

<br/>

I switched to Doom-Emacs after declaring Emacs Bankruptcy&nbsp;[^fn:1], and I haven’t regretted it. It uses every trick in the book to optimize, and the install/upgrade/maintenance scripts are excellent. It provides infrastructure and a well thought out framework for creating your own, speedy Emacs configuration.


## Notes about the Hotel California configuration {#emacs-notes-hotel-california}

If you feel that you need to have at least a menu-bar, then you can turn it on/off by running this command: `M-x menu-bar-mode`. It can be useful sometimes, especially when learning the Emacs ropes.

[^fn:1]: When your InitFile gets so large that you really need to start over, then you have declared “.emacs bankruptcy”. [EmacsWiki: Dot Emacs Bankruptcy](https://www.emacswiki.org/emacs/DotEmacsBankruptcy)