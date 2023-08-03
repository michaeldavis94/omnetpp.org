---
layout: post
title: New INET Framework release
joomla_id: 3520
joomla_url: "-sp-311419858"
date: 2005-07-07 09:59:17.000000000 +02:00
author: Andras
excerpt: "<FONT size=2>\r\n<P>This release, marked 20050706, is a significant update
  -- it is well worth reading the change summary below! Future INET releases are planned
  to have support for <STRONG>wireless protocols and mobility</STRONG>, and these
  parts will be based on Mobility Framework code. I've integrated&nbsp;(a modified
  version of) MF lower layers into INET, and added&nbsp;several new mobility models
  (including ones contributed by Emin Ilker Cetinbas and Georg Lutz). Small wireless/ah-hoc
  demos have also been included. We have also started to implement IPv6 support, partly
  based on IPv6SuiteWithINET. There's more -- read on. [<A href=\"index.php?option=com_docman&task=doc_details&gid=2113\">download</A>]
  [<A href=\"doc/INET\">on-line docu</A>]</P></FONT>"
category: Software
---
<FONT size=2>
<P>This release, marked 20050706, is a significant update -- it is well worth reading the change summary below! Future INET releases are planned to have support for <STRONG>wireless protocols and mobility</STRONG>, and these parts will be based on Mobility Framework code. I've integrated&nbsp;(a modified version of) MF lower layers into INET, and added&nbsp;several new mobility models (including ones contributed by Emin Ilker Cetinbas and Georg Lutz). Small wireless/ah-hoc demos have also been included. We have also started to implement IPv6 support, partly based on IPv6SuiteWithINET. There's more -- read on. [<A href="index.php?option=com_docman&task=doc_details&gid=2113">download</A>] [<A href="doc/INET">on-line docu</A>]</P></FONT><P>Summary of changes:
<P>
<UL>
<LI>TCP improvements: separate congestion control behaviour classes TCPTahoe, TCPReno and TCPNoCongestionControl provided, for teaching purposes (their code is very short, to the point, and extensively commented).
<LI>TCP: fixed bogus RTT calculation and other other bugs; also, sequence numbers are now recorded into omnetpp.vec, so with Plove one can create sequence number plots like Sally Floyd's [thanks to Ahmet Sekercioglu for help!]
<LI>still TCP: fixed the bug which caused closing of a connection to be reported 2MSL (240s) later to the user.
<LI>Added support for drop-tail router queues, and queues with QoS support based on DS Code Point; RED in preparation (see Network/Queue)
<LI>Added wireless and mobility support (based on Mobility Framework code), including 802.11b ad-hoc mode MAC, and several new mobility models (also new to MF). Supports mobility traces from BonnMotion and ANSim.
<LI>Contract directories introduced: Transport/Contract, Network/Contract and NetworkInterfaces/Contract. These directories contain a minimal set of classes necessary for using one layer's functionality from higher layers.
<LI>Added notification mechanism: modules can now notify each other about "events" such as routing table changes, interface status changes (up/down), interface configuration changes, wireless handovers, changes in the state of the wireless channel, mobile node position changes, etc. Notification works via the NotificationBoard which replaces the Blackboard.
<LI>InterfaceTable introduced: it stores all interface configuration that was previously stored in RoutingTable. Per-interface data structure was also split into protocol independent (InterfaceEntry) and protocol dependent (IPv4InterfaceData, IPv6InterfaceData) parts.
<LI>ScenarioManager introduced (experimental, in World/ subdirectory): it addresses the need for simulating scenarios like "what if this cable breaks at t=20s", or "what if traffic intensity grows at t=100s". Scenario is described in an XML file.
<LI>Ping and VideoStream applications added (from IPv6SuiteWithINET)
<LI>ARP got moved up from L2 to L3; this is to prepare for IPv6 support (IPv6 doesn't need ARP, so we can no longer have it as part of the network interfaces)
<LI>prepared for IPv6: application layer, transport layer and IPv6 contract taken over from IPv6SuiteWithINET-20050502
<LI>work in progress: from-scratch IPv6 implementation by Wei Yang Ng (Monash University) and Andras Varga
<LI>added INET_API definitions to classes, so that one can build a DLL that can be loaded dynamically into INET.exe (hint: compile DLL code *without* /DBUILDING_INET, and link them with INET.lib! then add [General]/load-libs= to omnetpp.ini.)
<LI>Network/IPv4d subdirectory removed.
<LI>added files called !WORK_IN_PROGRESS! with some explanations to directories which contain unfinished simulation models.</LI></UL>
<P></P>
