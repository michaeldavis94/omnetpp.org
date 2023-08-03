---
layout: post
title: 'Mobility Framework:  first official release (v1.0a1)'
joomla_id: 3543
joomla_url: "-sp-1748508302"
date: 2004-07-27 08:24:50.000000000 +02:00
author: Andras
excerpt: "<FONT size=2>\r<P>The MF team at <A href=\"http://www-tkn.ee.tu-berlin.de/\">TKN</A>,
  TU Berlin are proud to announce the first official release of the Mobility Framework
  (MF), a <STRONG>model framework&nbsp;intended to support wireless and / or mobile
  applications</STRONG> within OMNeT++. We moved the MF to SourceForge so you can
  find the source code to download, the manual, API &amp; neddoc reference etc. at
  <A href=\"http://mobility-fw.sourceforge.net/\"><STRONG>http://mobility-fw.sourceforge.net</STRONG></A>.&nbsp;Enjoy,
  and please don't hesitate to send us any kind of feedback. Especially in this early
  stage it is very important for us.</P></FONT>"
category: Software
---
<FONT size=2>
<P>The MF team at <A href="http://www-tkn.ee.tu-berlin.de/">TKN</A>, TU Berlin are proud to announce the first official release of the Mobility Framework (MF), a <STRONG>model framework&nbsp;intended to support wireless and / or mobile applications</STRONG> within OMNeT++. We moved the MF to SourceForge so you can find the source code to download, the manual, API &amp; neddoc reference etc. at <A href="http://mobility-fw.sourceforge.net/"><STRONG>http://mobility-fw.sourceforge.net</STRONG></A>.&nbsp;Enjoy, and please don't hesitate to send us any kind of feedback. Especially in this early stage it is very important for us.</P></FONT><P>What the hell is this Mobility Framework?</P>
<P>The MF is intended to support wireless and / or mobile applications within OMNeT++. The core part is a set of basic modules for the lower layers (1-4) of the ISO/OSI stack in conjunction with modules to support connection management and mobility handling. The idea is that a programmer (that's you ;-) can easily develop its own communication protocols by subclassing our basic modules. With this you do not have to take care about the nasty connection management and mobility stuff plus you can easily use protocols developed by other people. If you are interested in different ad-hoc routing protocols for example you might not want to implement your own MAC and PHY modules so you can just use some modules already implemented for the MF.</P>
<P>And that is already the second part of the MF: Apart from the core modules we plan to provide a rich library of "standard" protocols for the MF. There is already a flooding algorithm as well as a simple CSMA MAC and we even provide an implementation of the 802.11 protocol. However ALL of these protocols should be considered EXPERIMENTAL and have not been extensively tested so far. And that's where you come into play. Currently our resources here at the Telecommunication Networks Group (Technical University of Berlin) are very limited. So we will have to focus on the maintenance of the core framework. It is up to you to test the existing protocols and implement new ones. </P>
<P>Please let us know about any bugs you find as well as about new protocols you implemented. There is a "development" area where we are happy to include all kinds of implementations to share it with the rest of the community. Once an implementation has reached a "decent" state it will be moved to the "protocols" area where we plan to put all protocol implementations that can be used with some certainity that they really do what they are supposed to do (to assure the correctness of an implementation is something that we all know is impossible).</P>
<P>Another thing is that we only work with OMNeT++ under linux and the MF relies on GNU-make. If you make any experience with the MF under windows please let us know so that we can update the documentation and probably add a windows installation howto or even provide a make system thats works for windows.</P>
<P>We hope that the MF will help many people building simulation with OMNeT++. Please let us know if there is anything how you think we can improve the MF.</P>
<P>For the MF team,</P>
<P>Daniel Willkomm</P>
