---
layout: post
title: Debian GNU/Linux packages for OMNeT++ 2.0
joomla_id: 3615
joomla_url: "-sp-1108111293"
date: 2001-04-23 22:01:08.000000000 +02:00
author: Andras
excerpt: Debian GNU/Linux packages for OMNeT++ 2.0, by Enrik Berkhan (<A href="mailto:Enrik.Berkhan@planb.de">Enrik.Berkhan@planb.de</A>).
  The packages are not perfect right now, but are available for testing.
category: Software
---
Debian GNU/Linux packages for OMNeT++ 2.0, by Enrik Berkhan (<A href="mailto:Enrik.Berkhan@planb.de">Enrik.Berkhan@planb.de</A>). The packages are not perfect right now, but are available for testing.<FONT face="courier new, courier, mono">Hi,<BR>I've prepared some Debian GNU/Linux packages from the OMNeT++ sources.<BR>These packages will be far from perfect right now, but are available<BR>for testing. Just add the following lines to your /etc/apt/sources.list:<BR>deb </FONT><A href="ftp://ftp.ka.nu/pub/people/enrik/debian"><FONT face="courier new, courier, mono">ftp://ftp.ka.nu/pub/people/enrik/debian</FONT></A><FONT face="courier new, courier, mono"> potato non-free<BR>deb-src </FONT><A href="ftp://ftp.ka.nu/pub/people/enrik/debian"><FONT face="courier new, courier, mono">ftp://ftp.ka.nu/pub/people/enrik/debian</FONT></A><FONT face="courier new, courier, mono"> potato non-free<BR>Or download the packages manually and install them using dpkg.<BR>The main package is called "omnetpp". The shared libraries were moved<BR>to their own packages "libomnetpp0", "libomnetpp0-tk", "libomnetpp0-pvm".<BR>"omnetpp" depends on all the libraries right now. Precompiled samples<BR>are in the package, too, including both Cmdenv and Tkenv user interfaces<BR>in the binaries, Tkenv being the default. Use "-u Cmdenv" to use Cmdenv.<BR>You'll find the samples in /usr/lib/omnetpp/samples and the HTML docu-<BR>mentation in /usr/share/doc/omnetpp as usual.<BR>Feedback welcome.<BR>Enrik</FONT>
