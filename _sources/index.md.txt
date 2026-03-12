# Introduction to version control with Git - Why we want to track versions and how to go back in time to a working version

This is the introductory lesson to version control using
[Git](https://git-scm.com/).
It is based on the Git introduction from the
[CodeRefinery workshop from September/October 2025](https://coderefinery.github.io/2025-09-09-workshop/).

We start with an **existing repository on the web** to visually explain the basic
concepts of version control. We later move to a local
repository. Our goal there is not only to be able to apply changes to an
existing repository but to also be able to turn own projects into Git
repositories and to share them with others.

In the separate, we focus more on
the collaboration and the use of remote repositories. We try to stick to simple
workflows, just enough for researchers who are not obsessed with Git to be able
to work well.

The goals of the module as a whole are that the learner will feel comfortable
about committing changes, branching, and merging.

:::{prereq}
We offer several options to go through the material: **in an editor,
or in the terminal**.
CodeRefinery has summarized the [installation instructions](https://coderefinery.github.io/installation/).
However, please be noted that they do not fully apply to our lesson.
What you will need is the following:

- [GitHub Account](https://coderefinery.github.io/installation/github/#github)
- [SSH connection to GitHub](https://coderefinery.github.io/installation/ssh/#ssh). We do not recommend HTTPS.
- Either [Visual Studio Code](https://code.visualstudio.com/download) or
  [any editor of your choice](https://coderefinery.github.io/installation/editors/#editors).
- If you choose to use Windows without Visual Studio Code, we suggest to use
  the [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install)
  as an improved command line environment.

Basic knowledge of the command line is a prerequisite to this course. You
usually won't need it for Visual Studio Code, but having basic knowledge will
still be helpful.

If you wish to follow in the terminal and are new to the command line, a
[short shell crash course](https://youtu.be/xbTTDLA3txI) is available.
Another introduction suited for beginners is the Linux class from the
[FSI Informatik](https://video.cs.fau.de/by-lecture/Linux/2024s/) (German only,
2h long!).

We recommend to have a [GitHub](https://github.com) account.
**Why GitHub?**
Also [GitLab](https://gitlab.com) and [Bitbucket](https://bitbucket.org) would
allow similar workflows and basically everything that we will discuss is
transferable. E.g. GitLab is quite common as a private instance for research
insitutes. With this material and these exercises we do not implicitly
endorse the company [GitHub](https://github.com). We have chosen to demonstrate
a number of concepts using examples with [GitHub](https://github.com) because
it is currently the most popular web platform for hosting Git repositories and
the chance is high that you will interact with
[GitHub](https://github.com)-based repositories even if you choose to host your
Git repository on another service.
:::

```{toctree}
:maxdepth: 1
:caption: (Day 1) Getting started

motivation
configuration
```

```{toctree}
:maxdepth: 1
:caption: (Day 1) Modifying an existing project

browsing
commits
merging
```

```{toctree}
:maxdepth: 1
:caption: (Day 1) Studying an existing project

archaeology
```

```{toctree}
:maxdepth: 1
:caption: (Day 1) Optional episodes

staging-area
recovering
interrupted
aliases
under-the-hood
```

```{toctree}
:maxdepth: 1
:caption: (Day 2) Sharing your work

sharing
```

```{toctree}
:maxdepth: 1
:caption: (Day 2) Finding the balance

level
what-to-avoid
```

```{toctree}
:maxdepth: 1
:caption: (Day 2) Core lesson

concepts.md
same-repository.md
code-review.md
forking-workflow.md
```

```{toctree}
:maxdepth: 1
:caption: (Day 2) Optional episodes

hooks.md
bare-repos.md
```

```{toctree}
:maxdepth: 1
:caption: Reference

Shell crash course <https://youtu.be/xbTTDLA3txI>
reference
customizing
resources
exercises
guide-1
guide-2
PDF version <https://ipatix.github.io/git-intro/lesson.pdf>
```

```{toctree}
:maxdepth: 1
:caption: About

All CodeRefinery lessons <https://coderefinery.org/lessons/core/>
CodeRefinery <https://coderefinery.org/>
Reusing <https://coderefinery.org/lessons/reusing/>
```
