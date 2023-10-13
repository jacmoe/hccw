+++
title = "Org-mode"
author = ["Jacob Moena"]
draft = false
weight = 2
+++

## Introduction {#introduction}

{{< himg image="org-mode-unicorn" ext="svg" title="Org-mode">}}

> A GNU Emacs major mode for keeping notes, authoring documents, computational notebooks, literate programming, maintaining to-do lists, planning projects, and more — in a fast and effective plain text system.

<br/>

[Org-mode](https://orgmode.org/) is based on outline-mode which is again based on text-mode, and is both a markup language, an organizer (GTD), and an out-liner, and there are some people who live their entire lives in Org-mode.

<br/>

Here’s a small demo of Org-mode in action (_may I suggest that you turn off the sound for this one_):
[Emacs Org Mode Demo 2021](hnMntOQjs7Q)
Here is a nerdy blog post about why Org-mode is a great markup language: [Org Mode Syntax Is One of the Most Reasonable Markup Languages to Use for Text](https://karl-voit.at/2017/09/23/orgmode-as-markup-only/)

-   Official format
-   Out-liner
-   Organizer
-   Extendable
-   One hundred percent pure text


## Standard markup {#org-mode-standard-markup}

-   `*bold*` **bold**
-   `/italic/` _italic_
-   `_underline_` <span class="underline">underline</span>
-   `~code~`  `code`
-   `=monospaced=` `monospaced`
-   `# comment` anything after a hash sign and a space will not be exported


## Headings (structure) {#org-mode-headings}

A heading is one or more asterisks followed by a space and some text.

-   `* heading` level 1 heading
-   `** heading` level 2 heading
-   `*** heading` level 3 heading, and so on
-   `* todo heading` a heading with a todo
-   `* heading :tag:` heading with a tag
-   `* heading :tag1:tag2:` heading with two tags
-   `* heading :@category:` heading with a category

Press `C-<Enter>` to insert a new heading at the same level as the heading you’re in.

`M-<up>` and `M-<down>` will move a heading up and down.

`M-<left>` and `M-<right>` will promote/demote a heading.

`c n` and `c p` will navigate to next and previous heading, respectively.

`c u` navigates up to the parent heading, if any.

`S-<right>` and `S-<left>` cycles through todo states for a heading, ie from _draft_ to _revise_ to _done_.

`c q` can be used to set tags/categories for a heading. (`c c` also works, when standing on the actual heading)


## Lists {#org-mode-lists}

A list item is a dash (-) followed by a space and some text.

-   `- list item` unnumbered list item
-   `1 list item` numbered list item ()
-   `- [ ] list item` list item with unchecked check box
-   `- [X] list item` list item with checked check box

Press `C-<Enter>` to insert a new list item at the same level as the heading you’re in.

`M-<up>` and `M-<down>` will move a list item up and down.

`M-<left>` and `M-<right>` will demote/promote a list item.

`S-<left>` and `S-<right>` will cycle through different list styles, provided that the point is placed on the list item symbol (by default a `-`))


## Document options {#org-mode-document-options}


### TOC {#org-mode-document-options-toc}

`#+OPTIONS: toc:nil` turns off the insertion of an auto-generated Table Of Contents (TOC) upon export.
You can then use `#+toc: headlines 2` to manually insert a table of contents into the document.


## Links {#org-mode-links}

-   `[[link][description]]` link with description (use `c l` to insert)
-   `[[file:link_to_file]]` inline image is a file link **without** description

Use `c l` to insert a link, or to edit a link. Use `c o` to open a link.

If the link is a file link to an image, and without a description, it is an inline image. To toggle the rendering of inline images, you can press `c <TAB>`.


## Footnote-links {#org-mode-footnote-links}

-   `[fn:1: this is an inline, numbered footnote]`
-   `[fn:name: named, inline footnote]`
-   `[fn:: anonymous, inline footnote]`

For more information about footnotes, see&nbsp;[^fn:1]


## Special blocks {#org-mode-special-blocks}

In addition to the standard markup, Org-mode has special blocks. Use `C-c C-,` to insert a block.

<div title="Special blocks">

<img src="images/orgmode-blocks.png" alt="Special blocks" title="Special blocks" />
For example, choosing “comment” as a block type will result in the following being inserted in the document:

</div>

```nil
#+begin_comment
#+end_comment
```

The “verse” block is useful for when you want to have a piece of poetry and not have Emacs mess with the formatting.

Special blocks is a good way to extend the markup, and—of course—you can define your own special blocks.


## Noexport tags {#org-mode-noexport-tags}

The `:noexport:` tag tells Org-mode that the contents—including any children—of a section is not to be exported. Useful for when you keep your work in one single file, including sections for things like research, notes, and character studies.


## Ignore tags {#org-mode-ignore-tags}

The `:ignore:` tag instructs Org-mode to export the contents of a heading section, but not the heading itself. That’s useful when we organize your outline/document in chapters and scenes, but don’t want the exported text to be partitioned with scene headings. Having the text partitioned using headings allows us to rearrange those sections of the document—promoting, demoting, moving up and down—and we wouldn’t be able to do that if the text was not organized in an outline. Or, put another way: the `:ignore:` tag allows us to keep the outline to ourselves.


## Tables {#org-mode-tables}

In Org-mode tables are made of ASCII characters, but it feels like magic in action.

[Using Emacs episode 54 - Org Tables](5vGGgfs0q3k)

See [Tables (The Org Manual)](https://orgmode.org/manual/Tables.html) for more details.

We’ll see more of what Org-mode tables can do later on in this article, when discussing clock-tables and when discussing Org-tracktable.

[^fn:1]: [Creating Footnotes (The Org Manual)](https://orgmode.org/manual/Creating-Footnotes.html)