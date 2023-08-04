---
layout: post
title: OMNeT++ 6.0 Preview 8 Available
category: Software
details-url: https://github.com/omnetpp/omnetpp/releases/tag/omnetpp-6.0pre8
---
We are happy to announce the eighth preview version of OMNeT++ 6. The main focus
of improvements since pre7 was to improve the scalability of the new Analysis
Tool. Indeed, the UI is now easily capable of dealing with at least several tens
of thousands of result files, and a million result items (this was the input
routinely used during the development). If you are unfamiliar with how and why
the Analysis Tool was rewritten almost from scratch from the 4.x and 5.x
version, read the preview 7 highlights below.

In the Sequence Chart Tool, support for horizontally finite sized events was
added. This allows message sends and method calls in the same event to be
separated along the y axis.

<!--more-->

Additional, relatively minor improvements in the core:

- Added the "resultdir-subdivision" config option that causes result files to be
  distributed into a hierarchical subdirectory tree inside results/, using
  iteration variables as directory names. This is useful for simulation
  campaigns, because most file managers tend to struggle with directories
  containing more than a few thousand files.
- opp_scavetool now accepts directory names as well ("load all result files
  recursively from there"), and also the "**" wildcard that can match several
  directory levels.
- Added the "config-recording" config option, to control the of amount of config
  options to save in result files.
- Added the "${datetimef}" config variable that is a better choice to be used as
  part of result file names than "${datetime}"
