---
layout: post
title: Mobility Framework prerelease
joomla_id: 3555
joomla_url: "-sp-460849234"
date: 2004-02-09 15:13:00.000000000 +01:00
author: Andras
excerpt: <P>Finally we are ready to publish a pre-release of our Mobility Framework
  implementation:&nbsp;<A href="http://www.tkn.tu-berlin.de/research/research_texte/framework.html">http://www.tkn.tu-berlin.de/research/research_texte/framework.html</A></A>.
  The Mobility Framework is the successor of the FraSiMo and FraSiMo II developed
  at our university. It has been totally remodeled and only contains the basic ideas
  from FraSiMo II presented on the OMNeT++ workshop in 2003. The pre-release only
  contains very basic functionality and is primarily intended to get an impression
  of its abilities and for us to get (hopefully a lot ;) feedback for the first release.
  </P>
category: Software
---
<P>Finally we are ready to publish a pre-release of our Mobility Framework implementation:&nbsp;<A href="http://www.tkn.tu-berlin.de/research/research_texte/framework.html">http://www.tkn.tu-berlin.de/research/research_texte/framework.html</A></A>. The Mobility Framework is the successor of the FraSiMo and FraSiMo II developed at our university. It has been totally remodeled and only contains the basic ideas from FraSiMo II presented on the OMNeT++ workshop in 2003. The pre-release only contains very basic functionality and is primarily intended to get an impression of its abilities and for us to get (hopefully a lot ;) feedback for the first release. </P><P>So please play around a little bit and tell us your experiences (conceptual and documentational comments are as welcome as bug reports). Unfortunately none of us has experiences with OMNeT++ running under windows, so we only provide a gnu-make system until now. Maybe someone can develop a windows make system to be integrated in the first release... For the first real release additional modules are planned such as: </P>
<UL>
<LI>a very simple CSMA MAC layer
<LI>an implementation of a flooding network layer
<LI>a SNR evaluation model being able to calculate a list of SNR values over time for a message </LI></UL>
