---
layout: post
title: New OverSim release
joomla_id: 3482
joomla_url: "-sp-2068580905"
date: 2007-04-14 11:19:07.000000000 +02:00
author: Andras
excerpt: <P><EM>From Ingmar Baumgart</EM>:&nbsp;<FONT size=2>I am happy to announce
  the new OverSim snapshot release 20070404. You can download <STRONG>OverSim-20070404</STRONG>
  and the patched INET framework from </FONT><A href="http://www.oversim.org"><U><FONT
  color=#0000ff size=2>www.oversim.org</U></FONT></A>. Read on to see what's new in
  this release.</P>
category: Software
---
<P><EM>From Ingmar Baumgart</EM>:&nbsp;<FONT size=2>I am happy to announce the new OverSim snapshot release 20070404. You can download <STRONG>OverSim-20070404</STRONG> and the patched INET framework from </FONT><A href="http://www.oversim.org"><U><FONT color=#0000ff size=2>www.oversim.org</U></FONT></A>. Read on to see what's new in this release.</P><FONT size=2>
<P><FONT size=2>Changes from the 20061215 release:</FONT></P>
<UL>
<LI>Connect IPv4Underlay to real networks via TunOut (see HOWTO.Realworld) </LI>
<LI>New SingleHost Underlay: Emulate a single host. This host can be connected to a real network and an external Application (RealApp) (see HOWTO.Realworld)
<LI>up to 3 tiers with compound modules on application layer instead of one single application module, new TierDummy module for unused tiers.
<LI>Support for compiled-in NED files and disabled dynamic library loading
<LI>Added maximum hop count parameter for iterative routing
<LI>Several bug fixes for the BaseLookup class
<LI>new global module: GlobalStatistics
<LI>Correct statistics for forwarded Chord messages
<LI>Bug fixes and support for multiple runs in bin/overStat.pl
<LI>API: new gate names at each tier: to_upperTier, from_upperTier, to_lowerTier, from_lowerTier, from_udp, to_udp;
<LI>API: BaseOverlay::isResponsible() now queries, if a node is in the k neighborhood for a given key.</LI></UL></FONT>
