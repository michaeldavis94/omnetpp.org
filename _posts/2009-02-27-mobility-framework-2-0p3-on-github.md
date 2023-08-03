---
layout: post
title: Mobility Framework 2.0p3 for OMNeT++ 4.x on GitHub
joomla_id: 3451
joomla_url: "-sp-316970269"
date: 2009-02-27 18:02:00.000000000 +01:00
author: Andras
excerpt: In the last days we have uploaded the OMNeT++ 4 port of the Mobility Framework
  to github.com, with the project name <b>mf-opp4</b>. You can access the repository
  at <a href="http://github.com/mobility-fw/mf-opp4">http://github.com/mobility-fw/mf-opp4</a>.
category: Software
---
In the last days we have uploaded the OMNeT++ 4 port of the Mobility Framework to github.com, with the project name <b>mf-opp4</b>. You can access the repository at <a href="http://github.com/mobility-fw/mf-opp4">http://github.com/mobility-fw/mf-opp4</a>.

<p>Jérôme Rousselot has ported the original framework to OMNeT++ 4.

<p>The current repository contains two branches of the code:

<ul>
<li>The <b>master</b> branch contains only the original code ported to OMNeT++ 4
<li>The <b>ext</b> branch adds several other extensions to the framework:
  <ul>
    <li>BatteryModule -- by Anna Förster
    <li>BMAC -- by Anna Förster
    <li>LMAC -- by Anna Förster
    <li>RadioAccNoise3 phy model -- Jérôme Rousselot
    <li>IEEE 802.15.4 CSMA -- Jérôme Rousselot
  </ul>
</ul>

<p>Please check the wiki pages for further info how to use and download the code.

<p>Wiki: http://wiki.github.com/mobility-fw/mf-opp4

<p>Direct tarball downloads: http://github.com/mobility-fw/mf-opp4/downloads

<p>If you want to hack on the code, feel free to fork the project on github. If you make something interesting, you can contribute it back to the original project so other people can use it too.

<p>NOTE: Mobility FW is no longer supported. If you start a new project we strongly recommend to use the MiXiM framework instead.

<p>PS: OMNeT++ 4.0 rc2 will contain support for the GIT version control system, so you will be able to check out the project from the IDE.
