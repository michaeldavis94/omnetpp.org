---
layout: post
title: OMNeT++ 2.3 released
joomla_id: 3581
joomla_url: "-sp-2006953913"
date: 2003-06-16 02:04:00.000000000 +02:00
author: Andras
excerpt: It includes a major revision of the Manual. There's lots of new information
  in it, even for experienced users -- time to print a new copy!
category: Software
---
It includes a major revision of the Manual. There's lots of new information in it, even for experienced users -- time to print a new copy! <pre>
What's New
==========

OMNeT++ 2.3 release (June 2003)
-------------------------------
A major revision of the User Manual has taken place. In addition to
documenting new features, several existing sections have been revised,
updated and expanded for clarity and informativeness, based on feedback
from the community.

Even if you already have a printed copy of an earlier manual, this is
a good time to discard it and print a new one -- even experienced OMNeT++
users will find a wealth of new information in it. For the list of
changes, see the "Document History" table at the front of the manual.

Deprecations! To ensure your simulation will be compatible with future
releases, please check doc/API-Changes.txt and remove use of
deprecated functions from you simulation models. Functions deprecated
now are likely to be removed in next major release.

Improvements:
- message subclassing: generated message classes now accept message kind
  in the constructor.

Bugfixes since 2.3b2:
- fixed problem with deleting dynamically created modules
- fixed opp_msgc problem with RedHat9's broken Perl (doesn't recognize [^s]
  in regexps)
- minor improvements: opp_nmakemake now autodetects C++ file extension
  (.cc or .cpp); opp_msgc doesn't choke on -I flag
</pre>
