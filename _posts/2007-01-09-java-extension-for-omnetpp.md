---
layout: post
title: Java extension for OMNeT++
joomla_id: 3486
joomla_url: "-sp-582764270"
date: 2007-01-09 15:02:00.000000000 +01:00
author: Andras
excerpt: '<P>I am happy to announce an OMNeT++ extension that makes it possible to
  write OMNeT++ simple modules in Java. With <STRONG><A href="pmwiki/index.php?n=Main.JSimpleModule">JSimpleModule</A></STRONG>,
  simulation programmers can work with almost the same API as in C++ (thanks to wrapper
  objects generated using <A href="http://www.swig.org/">SWIG</A>). Java and C++-based
  simple modules can be freely mixed in simulations. You can dowload it a source and
  a Windows binary package, the latter being an Eclipse project as well: [<A href="index.php?option=com_docman&task=doc_details&gid=2081">Source</A>]
  [<A href="index.php?option=com_docman&task=doc_details&gid=2080">Windows binary+Eclipse
  project</A>].</P>'
category: Software
---
<P>I am happy to announce an OMNeT++ extension that makes it possible to write OMNeT++ simple modules in Java. With <STRONG><A href="pmwiki/index.php?n=Main.JSimpleModule">JSimpleModule</A></STRONG>, simulation programmers can work with almost the same API as in C++ (thanks to wrapper objects generated using <A href="http://www.swig.org/">SWIG</A>). Java and C++-based simple modules can be freely mixed in simulations. You can dowload it a source and a Windows binary package, the latter being an Eclipse project as well: [<A href="index.php?option=com_docman&task=doc_details&gid=2081">Source</A>] [<A href="index.php?option=com_docman&task=doc_details&gid=2080">Windows binary+Eclipse project</A>].</P><P>Operation is based on the JSimpleModule class. This is an ordinary C++ simple module, which receives the name of a Java class in a module parameter. During initialize, it loads the Java Virtual Machine (if not already loaded), instantiates the given Java class, then simply delegates initialize(), handleMessage() and finish() calls to it. The Java class should be subclassed from org.omnetpp.simkernel.JSimpleModule, which provides the usual methods: send(), scheduleAt(), cancelEvent(), etc. Messages are instances of org.omnetpp.simkernel.cMessage, and the org.omnetpp.simkernel package contains Java versions of most simulation kernel classes. The org.omnetpp.simkernel.* Java classes are just JNI-based wrappers around the corresponding C++ classes: every Java object holds a pointer to a corresponding C++ object, and delegates all method calls to it. This has a few consequences about the programming model. The wrapper classes have been generated using SWIG.</P>
<P><EM>So, should I program all my simulations in Java now?</EM> No, probably not all your simulations, but it can be useful for smaller models with relaxed performance requirements, or if you want to reuse an existing body of Java code as part of an OMNeT++ simulation.</P>
<P>You can read more on the <A href="pmwiki/index.php?n=Main.JSimpleModule">JSimpleModule wiki page</A>.</P>
