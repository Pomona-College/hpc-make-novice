---
permalink: index.html
site: sandpaper::sandpaper_site
---

::::::::::::::::::::::::::::::::::::: callout

## Pomona College HPC Workshop Series

This workshop is part of the **Pomona College Research Computing Workshop
Series**, adapted from [Automation and Make](https://swcarpentry.github.io/make-novice/)
by [Software Carpentry](https://software-carpentry.org/).

**Cluster:** sagehen.hpc.pomona.edu
**Web Portal:** [OnDemand](https://ondemand.hpc.pomona.edu/)
**Support:** its-hpc@pomona.edu

Make is available on the Sagehen HPC cluster by default. Automating your
analysis pipelines with Make is especially valuable for reproducible
HPC workflows.

*Adapted for Pomona College by Andrew Wilson, ITS Research Computing.
Licensed under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).*

::::::::::::::::::::::::::::::::::::::::::::::::

Make is a tool which can run commands to read files, process these
files in some way, and write out the processed files. For example,
in software development, Make is used to compile source code
into executable programs or libraries, but Make can also be used
to:

- run analysis scripts on raw data files to get data files that
  summarize the raw data;
- run visualization scripts on data files to produce plots; and to
- parse and combine text files and plots to create papers.

Make is called a build tool - it builds data files, plots, papers,
programs or libraries. It can also update existing files if
desired.

Make tracks the dependencies between the files it creates and the
files used to create these. If one of the original files (e.g. a data
file) is changed, then Make knows to recreate, or update, the files
that depend upon this file (e.g. a plot).

There are now many build tools available, all of which are based on
the same concepts as Make.

::::::::::::::::::::::::::::::::::::::::::  prereq

## Prerequisites

In this lesson we use `make` from the Unix Shell. Some previous
experience with using the shell to list directories, create, copy,
remove and list files and directories, and run simple scripts is
necessary.

::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::  prereq

## Setup

In order to follow this lesson, you will need to download some files.
Please follow instructions on the [setup](learners/setup.md) page.

::::::::::::::::::::::::::::::::::::::::::::::::::

## Acknowledgments

Developed by **Andrew Wilson**, Director of Research Computing and Digital
Scholarship at Pomona College, with **Andrei Motchenko**, who tested, edited
and produced screenshots for the workshop series.
