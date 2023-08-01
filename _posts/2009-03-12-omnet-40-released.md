---
layout: post
title: OMNeT++ 4.0 released
joomla_id: 3448
joomla_url: omnet-40-released
date: 2009-03-12 08:44:00.000000000 +01:00
author: Andras
excerpt: After more than 3 years of intense work of the team, 8 beta releases and
  two release candidates, OMNeT++ 4.0 has been finally released. (We'd like to take
  the opportunity to congratulate ourselves for this great achievement! :) With the
  new Eclipse-based IDE, greatly enhanced NED language and simulation kernel, and
  tons of other improvements, 4.0 is guaranteed to redefine the way you do simulations
  with OMNeT++, and it will open up new horizons. <p>Downloads are available <a href="/download/old">in
  the download area</a>. Report bugs in our <a href="http://dev.omnetpp.org/bugs">bugtracker</a>.  </p><p>Read on for a brief summary of what's new in 4.0!   </p>
category: Software
---

<p>After more than 3 years of intense work of the team, 8 beta releases and two release candidates, OMNeT++ 4.0 has been finally released. (We'd like to take the opportunity to congratulate ourselves for this great achievement! :) With the new Eclipse-based IDE, greatly enhanced NED language and simulation kernel, and tons of other improvements, 4.0 is guaranteed to redefine the way you do simulations with OMNeT++, and it will open up new horizons.</p>
<p>Downloads are available <a href="/download/old">in the download area</a>. Report bugs in our <a href="http://dev.omnetpp.org/bugs">bugtracker</a>.  </p>
<p>Read on for a brief summary of what's new in 4.0!   </p>
<h3>GUI</h3>
<p>  An Eclipse-based comprehensive simulation IDE has been introduced to replace   the previous standalone GUI programs gned, scalars and plove. The IDE supports   all stages of a simulation project: developing, building, configuring and   running simulation models, and analysing results. It also supports   visualizing simulation execution traces as sequence charts, and generating   documentation. We are also bundling version control (cvs, svn, git) Eclipse   plug-ins with the IDE. The IDE is supported on the three major platforms,   Linux, Mac OS X and Windows. Since Eclipse is extremely extensible, we expect   that OMNeT++-based simulation frameworks will contribute their own custom   wizards into the IDE.</p>
<h3>Tooling</h3>
<p>   On the Windows platform, we have standardized on using the MinGW compiler.   We are bundling a version of MSys and MinGW with the distribution, along   with MinGW versions of several open-source programs and libraries needed   or found useful with OMNeT++, such as gdb, perl, libxml, gmp, graphviz,   Tcl/Tk, svn and git. MinGW was chosen over Cygwin because MinGW builds and   uses libraries in the native Windows (MSVC-compatible) binary format, and   builds programs that execute without a Unix emulation layer. The MSVC   compiler is only supported in the commercial version of OMNeT++.  </p>
<h3>Build system</h3>
<p>   In order to facilitate working with large simulation models like the INET   Framework, the makefile generator opp_makemake has been extended with the   --deep option. With --deep, opp_makemake generates a makefile that takes   care of building a whole source directory tree.    </p>
<p>   Another big change is out-of-directory builds for both the OMNeT++ libraries   and simulation models: object files and other by-products of the build   process go in a separate directory tree (out/).    </p>
<p>   Simulation models can now easily be compiled with debug/release compiler   options, simply with the commands "make MODE=debug" and "make MODE=release";   there is no need to modify configure.user.  </p>
<h3>Simulation kernel</h3>
<p>   Simulation kernel internals have been redesigned with memory efficiency in   mind, to support large-scale simulations better. Techniques include string   pooling (storing freqeuently occurring strings such as module, gate and   parameter names only in one copy), shared parameter value instances,   gate vector descriptors (gate name, type and size are only stored once   for the whole gate vector), and optimal packing of object fields (e.g.   packing several boolean variables into an unsigned int).    </p>
<p>   The simulation kernel as a library has been made significantly easier to   embed in other (non-OMNeT++) programs. The way of using the OMNeT++   simulation kernel as a plain C++ library has been documented in the Manual,   and two corresponding code examples have been added to the distribution.    </p>
<p>   There have been several complaints about precision loss due to simtime_t   being represented with the C type "double". In 4.0, double has been replaced   with an int64-based fixed-point representation; the precision can be   configured in omnetpp.ini as a power of ten, with the default being   picosecond resolution (1e-12).    </p>
<p>   Regarding the API, several functions have been given better or more   consistent names, with the most visible change being that getter methods   have been prefixed with the word "get". Migration of simulation models   to 4.0 is assisted by scripts that perform this renaming (and several other   adjustments) in the source code.    </p>
<p>   cMessage has been split into a base cMessage plus a cPacket class.   The bit length, encapsulated message and error flag fields have been   moved to cPacket.    </p>
<p>   Modules have now the possibility to receive nonzero-duration messages   at the beginning of the reception; this is done by reconfiguring the   gate object.    </p>
<p>   sendDirect() calls now expect the propagation delay and transmission   duration values in separate arguments; this was done to facilitate   the animation of wireless transmissions later.  </p>
<h3>NED</h3>
<p>   The NED language has been revised and significantly extended. An overview   of changes:    </p>
<p>   The language syntax has been changed to make it more consistent. A migration   tool is provided to convert old NED files to the new syntax.    </p>
<p>   A Java-like package system has been introduced to make the language scale   to large model frameworks and to prevent name clashes; NED files files are   now read from directory trees listed on the NEDPATH.    </p>
<p>   Channels have been made first-class citizens. They can have arbitrary   parameters like modules do, and may have custom C++ implementation classes.   Three predefined channel types have been created, ned.IdealChannel,   ned.DelayChannel and ned.DatarateChannel.    </p>
<p>   Inheritance is now supported for module and channel types. Derived modules   and channels may add new parameters and gates, may set or modify parameter   values and gate vector size, and (in the case of compound modules) may add   new submodules and connections.    </p>
<p>   Inner types are now supported. This is most useful for making channel   definitions local to the network definition that uses them.    </p>
<p>   Module and channel interfaces have been introduced, to make "like"   relationships more explicit. Module and channel interfaces can be used as   a placeholder where normally a module or channel type would be used, and the   concrete module or channel type is determined at network setup time by a   parameter. Concrete module types have to "implement" the interface they can   substitute.    </p>
<p>   Inout gates and bidirectional gates are now supported. In the C++ code,   inout gates appear as (input,output) gate pairs.    </p>
<p>   Parameters can now have default values. The default value can be overridden   in the ini file. If the ini file does not assign any value to the parameter,   the default values get used automatically.    </p>
<p>   Support for arithmetic expressions has become more complete, e.g. string   manipulation is also possible.    </p>
<p>   It is possible to annotate module or channel types, parameters, gates and   submodules with properties. Metadata can carry extra information for   various tools, the runtime environment, or even for other modules in the   model. Examples include display strings, parameter prompt string and unit   of measurement.    </p>
<p>   Default icons (in general, default display strings) are now supported.   Display strings are represented as metadata annotation (@display property),   which can be modified via inhertance.  </p>
<h3>Ini files</h3>
<p>   Instead of runs, named configuration sections were introduced in the ini   file.    </p>
<p>   The concept of "runs" have been refined to provide parameter study support;   Ini files now can specify parameter ranges and the runtime is able to explore   them. The notion of experiment, measurement and replication was introduced to   help the general workflow of result analysis.    </p>
<p>   Configuration options are now checked; mistyped configuration options are   reported. Configuration options can be given on the command-line as well,   overriding the values specified in the ini file.    </p>
<p>   The new "fingerprint" ini file option allows for quick-and-simple regression   tests. The fingerprint is basically a hash of event times and module IDs   during the simulation, and it can detect if the simulation follows a   different trajectory after a supposedly "harmless" code change.  </p>
<h3>Result analysis</h3>
<p>   The new result analysis tool in the IDE (which replaces plove and scave)   supports the notion of experiments, measurements and replication. The IDE   now stores all operations required to create a diagram or chart in a "recipe"   file. It can recreate the charts and diagrams automatically after re-running   the simulation or the whole experiment.    </p>
<p>   The vector and scalar file format has changed to support the new features   of the IDE. Vector files are now indexed for efficiency. </p>
