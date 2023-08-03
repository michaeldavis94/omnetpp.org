---
layout: post
title: AntNet model update
joomla_id: 3547
joomla_url: "-sp-2039097126"
date: 2004-05-18 11:56:00.000000000 +02:00
author: Andras
excerpt: "<P><A href=\"index.php?option=com_docman&task=doc_details&gid=2139\">AntNet
  version 3.0</A> has been released by Mudassar Farooq. This version works with OMNeT++
  3.0a3 or later.</P><FONT size=2>\r<P>AntNet was proposed by Gianni Di Caro &amp;
  Marco Dorigo in [1] . In AntNet the network state is monitored through two ant agents:
  Forward_Ant and Backward_Ant. A Forward_Ant agent is launched at regular intervals
  from a source to a certain destination. It uses the same queues as data packets
  to monitor the real traffic situation. ...</FONT></P>"
category: Software
---
<P><A href="index.php?option=com_docman&task=doc_details&gid=2139">AntNet version 3.0</A> has been released by Mudassar Farooq. This version works with OMNeT++ 3.0a3 or later.</P><FONT size=2>
<P>AntNet was proposed by Gianni Di Caro &amp; Marco Dorigo in [1] . In AntNet the network state is monitored through two ant agents: Forward_Ant and Backward_Ant. A Forward_Ant agent is launched at regular intervals from a source to a certain destination. It uses the same queues as data packets to monitor the real traffic situation. ...</FONT></P>Forward_Ant agent is equipped with a stack memory on which the address and entrance time of each node on its path are pushed. Once the Forward_Ant agent reaches its destination it creates a Backward_Ant agent and transfers all information to it. Backward_Ant visits the same nodes as Forward_Ant in reverse order and modifies the entries in the routing tables based on the trip time from the nodes to the destination. At each node the average trip time, the best trip time and the variance of the trip times for each destination are maintained. The trip time values are calculated by taking the difference of entrance times of two subsequent nodes pushed onto the stack. Backward_Ant agent uses the system priority queues so that it disseminates the information to the nodes as soon as possible.
<P>[1] G. Di Caro and M. Dorigo. AntNet: Distributed Stigmergetic Control for Communications Networks.Journal of Artificial Intelligence Research, 9:317--365, 1998</P>
