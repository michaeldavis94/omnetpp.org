---
download: true
layout: download-details
title: OppBSD
years-active: 2005-2012
category: models
tags: model omnetpp4 omnetpp3
keywords: ipv6, tcp, ipv4, udp, icmpv6, arp, nd, ethernet
download-page-url: https://svn.tm.kit.edu/trac/OppBSD/downloads
website-url: https://svn.tm.kit.edu/trac/OppBSD
opp-env-command: opp_env install oppbsd-latest
---

OppBSD integrates essential parts of the real FreeBSD networking stack into
OMNeT++ as a simulation model. Every simulated host (or router) runs its own
copy of the FreeBSD kernel's networking stack. Consequently, the simulation
model is very accurate, i.e., almost behaving like a real implementation.
Release 4.0 works with OMNeT++ v4.3 (alternatively v4.1, v4.2) and provides IPv6
support. Presently, the package covers the full TCP/IP stack including IPv4,
IPv6, UDP, TCP, ICMP, ICMPv6, ARP, ND, sockets and Ethernet frames.
