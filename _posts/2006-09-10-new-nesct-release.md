---
layout: post
title: New NesCT release
joomla_id: 3493
joomla_url: "-sp-1335513629"
date: 2006-09-10 09:52:05.000000000 +02:00
author: Andras
excerpt: Omer Sinan Kaya released a new version of <STRONG>NesCT</STRONG>, a NesC-to-OMNeT++
  translator. NesCT makes it possible to simulate <EM>TinyOS</EM> sensor networks
  with OMNeT++, by translating the NesC programs into C++ code. As part of the new
  release, <EM>Deluge</EM>, the famous code distribution protocol of TinyOS is now
  working with OMNeT++, and is included in the Examples package. [<A href="http://nesct.sourceforge.net/">NesCT
  home page</A>]
category: Software
---
Omer Sinan Kaya released a new version of <STRONG>NesCT</STRONG>, a NesC-to-OMNeT++ translator. NesCT makes it possible to simulate <EM>TinyOS</EM> sensor networks with OMNeT++, by translating the NesC programs into C++ code. As part of the new release, <EM>Deluge</EM>, the famous code distribution protocol of TinyOS is now working with OMNeT++, and is included in the Examples package. [<A href="http://nesct.sourceforge.net/">NesCT home page</A>] <P>Newest changes include: </P>
<UL>
<LI>Added Deluge, the&nbsp;famous code distribution protocol of TinyOS
<LI>There used to be a problem with single shot timers, fixed.
<LI>Added packet loss due to biterror.
<LI>Fixed a bug with EEPROM , would not read or write at the same moment to EEPROM.
<LI>EEPROM files are located in logger directory and from now on, the contents of these files are saved across simulations.
<LI>Fixed a permission problem with creating directories, NesCt does not require you to be a root user anymore. </LI></UL>
