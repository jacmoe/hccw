+++
title = "Tracking progress"
author = ["Jacob Moena"]
draft = false
weight = 5
+++

## Track-table {#tracking-progress-track-table}

{{< figure src="images/tracktable.png" alt="Track-table keeps track of words written per day" title="Track-table keeps track of words written per day" >}}


## Clocking time {#tracking-progress-clocking-time}

`c x i` to clock in. `c x o` to clock out. `c x q` to cancel a clock.
There is also the option of starting a 20 minute Pomodoro session, by pressing `B`.

<div title="Pomodoro session">

<img src="images/pomodoro.png" alt="Pomodoro session" title="Pomodoro session" />
Clocking is tied to the heading you are working under, and will add a `:LOGBOOK:` section to it, like this:

</div>

```nil
:LOGBOOK:
CLOCK: [2017-04-10 Mon 15:16]--[2017-04-10 Mon 15:17] =>  0:01
CLOCK: [2017-04-07 Fri 16:05]--[2017-04-07 Fri 16:35] =>  0:30
CLOCK: [2017-04-05 Wed 16:42]--[2017-04-05 Wed 16:52] =>  0:10
:END:
```

We can generate clock report table by executing `C-c l c R` or `M-x org-clock-report`.
The following will be inserted at point, depending on the logbooks in the current document:

```nil
#+BEGIN: clocktable :scope subtree :maxlevel 2
#+CAPTION: Clock summary at [2022-10-23 søn 09:56]
| Headline   | Time |
|------------+------|
| *Total time* | *0:41* |
|------------+------|
#+END:
```

A clocktable can be configured, for example, to show time clocked until now, like this:

```nil
#+BEGIN: clocktable :maxlevel 3 :scope file :block untilnow
```

<div title="Time clocked in total">

<img src="images/clocktable-master.png" alt="Time clocked in total" title="Time clocked in total" />
Time clocked today:

</div>

```nil
#+BEGIN: clocktable :maxlevel 3 :scope file :block today
```

Time clocked yesterday:

```nil
#+BEGIN: clocktable :maxlevel 3 :scope file :block yesterday
```

To update a clocktable, simply place the point somewhere in the `BEGIN` line, and press `c c`.

For more on clocking time, see [Clocking time with Org-mode](https://writequit.org/denver-emacs/presentations/2017-04-11-time-clocking-with-org.html).

Often when writing, our progress can’t always be measured in words, so time spent is a good alternative.


## Org-analyzer {#tracking-progress-org-analyzer}


## Org-habit streak count {#tracking-progress-org-habit-streak-count}


## Words per heading {#tracking-progress-words-per-heading}

Using `org-wc`.

{{< figure src="images/org-wc.png" alt="Running M-x org-wc-display shows word count per heading" title="Running M-x org-wc-display shows word count per heading" >}}


## Column view {#tracking-progress-column-view}

Column view is a good way to view properties of headers. While we can view todo status, categories, tags, time logged, and other standard properties, we can add our own, custom properties, and this is where it gets real interesting for creative writers.
We can easily add properties to a heading by running `C-c C-x p`:

{{< figure src="images/properties-actions.png" alt="Adding properties to a heading" title="Adding properties to a heading" >}}

Now we can configure the `COLUMNS` special property, which will be inherited by child headings:

{{< figure src="images/columns-source.png" alt="Setting up columns with properties" title="Setting up columns with properties" >}}

See [Org column view tutorial](https://orgmode.org/worg/org-tutorials/org-column-view-tutorial.html) for details.

Having set it all up, we can now run `org-columns` by pressing `c x c`:

{{< figure src="images/columns.png" alt="Column view" title="Column view" >}}

Pres `q` to exit.
