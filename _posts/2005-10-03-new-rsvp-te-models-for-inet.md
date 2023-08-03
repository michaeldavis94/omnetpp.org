---
layout: post
title: New RSVP-TE models for INET
joomla_id: 3513
joomla_url: "-sp-108343245"
date: 2005-10-03 10:11:31.000000000 +02:00
author: Andras
excerpt: "<P>Vojta Janota has completed the implementation of the <STRONG>MPLS/RSVP-TE</STRONG>
  model for OMNeT++. This&nbsp;model will replace the current MPLS/RSVP-TE code in
  the INET Framework.</P>\r<P>For further info, <U>read on</U>&nbsp;or&nbsp;visit
  the web site: <A href=\"http://vojta.pohoda.cz/omnetpp/\">http://vojta.pohoda.cz/omnetpp/</A></P>"
category: Software
---
<P>Vojta Janota has completed the implementation of the <STRONG>MPLS/RSVP-TE</STRONG> model for OMNeT++. This&nbsp;model will replace the current MPLS/RSVP-TE code in the INET Framework.</P>
<P>For further info, <U>read on</U>&nbsp;or&nbsp;visit the web site: <A href="http://vojta.pohoda.cz/omnetpp/">http://vojta.pohoda.cz/omnetpp/</A></P><P>A partial list of&nbsp;highlights&nbsp;in Vojta's implementation: more realistic TED (it is now a per-router database which gets&nbsp;built&nbsp;using a simple link state routing protocol, instead of being approximated by&nbsp;a global object holding "the" topology); ability to write&nbsp;<A href="http://www.isi.edu/nsnam/nam/">nam</A>&nbsp;traces; scriptability&nbsp;via <A href="doc/INET/neddoc/ScenarioManager-id2265134.html">ScenarioManager</A>; consistent use of XML input files. On the other hand, this is not yet a finished product and further development is expected. The source code is based on <A href="index.php?option=com_docman&task=doc_details&gid=2108">INET-20059022</A>.&nbsp;</P>
