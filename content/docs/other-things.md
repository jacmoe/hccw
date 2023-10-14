+++
title = "Other things"
author = ["Jacob Moena"]
draft = false
weight = 12
+++

## Journaling {#other-things-journaling}


## Blogging {#other-things-blogging}


## Bibliography {#other-things-bibliography}


### Zotero {#other-things-bibliography-zotero}

Zotero is used to gather and store and export the citations/references, by the use of the `Better-Bibtex` plugin.

<div title="Zotero">

<img src="/images/zotero.png" alt="Zotero" title="Zotero" />
After installing Zotero itself, the plugin can be installed by following this guide: <https://retorque.re/zotero-better-bibtex/installation/>. When downloading using Firefox, I had to right-click and “save as” because otherwise Firefox thought I was trying to install a Firefox add-on due to the file-extension being the same.

</div>

<div title="BetterBibtex installed">

<img src="/images/zotero-plugins.png" alt="BetterBibtex installed" title="BetterBibtex installed" />
When the plugin has been successfully installed, it can be set up to automatically export and keep updated the LaTeX formatted Bibtex file that we need in order to use it from Emacs.

</div>

<div title="Zotero export settings">

<img src="/images/zotero-export-settings.png" alt="Zotero export settings" title="Zotero export settings" />
Choose “file - Export Library”, and choose the `Better BibLaTeX` as the format, and make sure to check the “keep updated” box. When you click “OK” you will be asked where to save the export. For my configuration, I have it as `~/Dropbox/skriv/jacmoe.bib`.

</div>

To actually populate the bibliography library, I am using the Zotero Firefox connector plugin. I can press a button in Firefox whenever I am visiting a resource.


### Emacs {#other-things-bibliography-emacs}

After all the work with Zotero, we are now ready to use the bibliography from within Emacs.
In the file where we want to insert citations, we configure the bibliography file to be used, and configure the export of the citations to use the CSL format:

```nil
#+bibliography: ~/Dropbox/skriv/jacmoe.bib
#+cite_export: csl
```

Then, we set a placeholder for where the generated bibliography list will be rendered in the document:

```nil
#+print_bibliography:
```

Now that we’re all set up, we can now insert citations into our document by running `org-cite-insert` (bound to `C-c l @`)

{{< figure src="/images/citation-insert.png" alt="Inserting a citation in Emacs" title="Inserting a citation in Emacs" >}}

{{< figure src="/images/bibliography-source.png" alt="Bibliography source code" title="Bibliography source code" >}}

{{< figure src="/images/bibliography-test.png" alt="Bibliography test rendering" title="Bibliography test rendering" >}}


## Snippets {#other-things-snippets}


## Miscellaneous {#other-things-miscellaneous}


### Grabbing links from the web browser {#other-things-miscellaneous-grabbing-links-from-the-web-browser}

By running `M-x grab-x-link` we can insert a link from an active web browser window.
It will ask you to choose your browser—Chromium, Chrome, Firefox, or Brave—and what format to use (plain, markdown or Org format). Much quicker than manually copying, pasting, and write the title manually. The links can be edited by `c l` , and opened by `c o`.


### Reading ebooks {#other-things-reading-ebooks}

Use nov.el to read ebooks.
