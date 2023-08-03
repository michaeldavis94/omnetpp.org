---
layout: post
title: Routing tables made visible
joomla_id: 3553
joomla_url: "-sp-1534730906"
date: 2004-03-11 01:04:00.000000000 +01:00
author: Andras
excerpt: "<P>Any large network model has routing tables and other internal data structures
  which had been hard to monitor during simulation -- most of the time you had to
  print their contents periodically to be able to see what was going on. OMNeT++3.0
  will help this. It will make it easy to get std::vectors, structs, vectors of structs
  and other data displayed in Tkenv.</P>"
category: News
---
<P>Any large network model has routing tables and other internal data structures which had been hard to monitor during simulation -- most of the time you had to print their contents periodically to be able to see what was going on. OMNeT++3.0 will help this. It will make it easy to get std::vectors, structs, vectors of structs and other data displayed in Tkenv.</P><P>The following screenshot was made with the development versions of IPSuite and OMNeT++.</P>
<P><A href="http://whale.hit.bme.hu/misc/screenshots/tables.gif"><img width="155" height="114" src="/images/omnetpp/20040311010419874_1.gif" alt=""></A> </P>
<P>Three of the four tables used std::vectors. LIBTable and TED were structs stored in std::vectors:</P><PRE>struct lib_type {..};
std::vector&lt;lib_type&gt; lib;</PRE>And all code necessary to get them displayed&nbsp;into Tkenv was writing an operator&lt;&lt; function which can write the struct on an std::ostream and adding the WATCH_vector(lib) line into initialize(). <PRE>std::ostream&amp; operator&lt;&lt;(std::ostream&amp; os, const lib_type&amp; lib) {
    os &lt;&lt; "InL:" &lt;&lt; lib.inLabel;
&nbsp;&nbsp;&nbsp; os &lt;&lt; "&nbsp; InIf:" &lt;&lt; lib.inInterface.c_str();
&nbsp;&nbsp;&nbsp; os &lt;&lt; "&nbsp; OutL:" &lt;&lt; lib.outLabel;
&nbsp;&nbsp;&nbsp; os &lt;&lt; "&nbsp; OutIf:" &lt;&lt; lib.outInterface.c_str();
&nbsp;&nbsp;&nbsp; os &lt;&lt; "&nbsp; Optcode:" &lt;&lt; lib.optcode;<BR>&nbsp;&nbsp;&nbsp; return os;
}
</PRE><PRE>WATCH_vector(lib);</PRE>
<P>The syntax may change, but the idea remains: your tables will be easy to get watched.</P>
