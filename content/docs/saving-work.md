+++
title = "Saving the work"
author = ["Jacob Moena"]
draft = false
weight = 8
+++

## Magit {#saving-the-work-magit}

{{< figure src="/images/magit.png" alt="Prose linting with Vale" title="Prose linting with Vale" >}}


## Unsaved changes {#saving-the-work-unsaved-changes}

Sometimes you want to know what changes you have made to a buffer since your last save. Since you haven’t saved the file yet, Magit can’t help you, so you need something else. Fortunately, we can use Emacs’ `diff-buffer-with-file`, mapped to `C-d`.

{{< figure src="/images/diff.png" alt="Using diff to see the difference between buffer and file" title="Using diff to see the difference between buffer and file" >}}

Emacs will ask you for the file on disk, and then open a diff buffer where you can examine the differences. Use `x o` (o for ‘other’) to go to the diff buffer, if you’re not already in it. Using movement commands, like `i o k l`, etc. And then, when done, close the buffer by pressing `x 0` (zero), or `x 1` if you’re not in the diff buffer.
