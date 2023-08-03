---
layout: post
title: oppbsd 1.0 - a full FreeBSD TCP/IP stack in OMNeT++
joomla_id: 3521
joomla_url: "-sp-1253590453"
date: 2005-07-02 07:18:48.000000000 +02:00
author: Andras
excerpt: "<STRONG>OppBSD 1.0 released!</STRONG> The project aim was to get (part of)
  the FreeBSD kernel networking code working in OMNeT++ as a simulation model. Though
  the original aim was to use FreeBSD's validated TCP implementation in OMNeT++ as
  a TCP model, but along the way it turned out that porting the full networking stack
  was in fact an easier task. Therefore, we now present OppBSD as full TCP/IP stack
  including ICMP, ARP, sockets and Ethernet frames."
category: Software
---
<STRONG>OppBSD 1.0 released!</STRONG> The project aim was to get (part of) the FreeBSD kernel networking code working in OMNeT++ as a simulation model. Though the original aim was to use FreeBSD's validated TCP implementation in OMNeT++ as a TCP model, but along the way it turned out that porting the full networking stack was in fact an easier task. Therefore, we now present OppBSD as full TCP/IP stack including ICMP, ARP, sockets and Ethernet frames. <STRONG>INTRODUCTION </STRONG>
<P>TCP is currently still the dominating transport protocol in the Internet. If you must simulate applications that use TCP as a reliable transport protocol, you need a good TCP stack. But implementing TCP correctly is not easy. Besides a lot extensions to the base specification which must be also covered in order to get an up-to-date implementation, several implementation mistakes have to be avoided. Finally, you must validate your implementation that it behaves exactly like the specifications prescribe. Simulators should, however, show a realistic TCP behavior. </P>
<P>Our approach was to avoid re-implementing TCP including all the usual bugs as well as to avoid a thorough validation. Therefore, we integrated an existing (and validated) TCP stack from a real operating system into OMNeT++. The project aim was to get (part of) the FreeBSD kernel networking code working in OMNeT++ as a simulation model. Though the original aim was to use FreeBSD's validated TCP implementation in OMNeT++ as a TCP model, but along the way it turned out that porting the full networking stack was in fact an easier task. Therefore, we now present OppBSD as full TCP/IP stack including ICMP, ARP, sockets and Ethernet frames.</P>
<P>This model was developed at the Institute of Telematics, University of Karlsruhe by Roland Bless, Mark Doll and Jerome Freilinger, who did the first implementation.</P>
<P><STRONG>Overview</STRONG></P>The oppbsd code should run on<BR>&nbsp;&nbsp; OMNeT++: v3.0/v3.1<BR>&nbsp;&nbsp; OS: Linux<BR>
<P>In the simulation models provided, every simulated host (or router) runs its own copy of the FreeBSD kernel's networking stack. </P>Features:
<UL>
<LI>precise emulation of the FreeBSD network stack behaviour
<LI>test your model's interoperability with "real" implementations.
<LI>provides a controlled environment to try BSD "kernel hacks"
<LI>FreeBSD kernel patches (e.g. KAME patch for mobile IPv6) can be easily incorporated (currently ongoing work)
<LI>higher scalability than using emulators: 1000 hosts with two simultaneous connections per host use approx. 411 MiB
<LI>automatic IP address assignment and routing! </LI></UL><A href="http://www.tm.uka.de/~bless/oppbsd-1.0-136.tar.gz">Download</A>
