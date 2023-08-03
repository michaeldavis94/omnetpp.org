---
layout: post
title: FACTS - Future Aeronautical Communications Traffic Simulator
joomla_id: 3469
joomla_url: "-sp-1132886828"
date: 2007-09-26 16:35:00.000000000 +02:00
author: Andras
excerpt: "<P>From&nbsp; Felix Hoffmann: </P>\r<P>The <A href=\"http://www.dlr.de/kn\">Institute
  of Communications and Navigations</A> at the <A href=\"http://www.dlr.de\">German
  Aerospace Center (DLR)</A> is currently developing a simulation platform for aeronautical
  communications within the project <EM>FACTS - Future Aeronautical Communications
  Traffic Simulator</EM>. The project investigates the possibilities of shifting from
  voice communications to digital data traffic in Air Traffic Control, and creating
  an IP-based aeronautical telecommunications network. The simulator is based on OMNeT++
  and the INET Framework, and will feature a <A href=\"http://worldwind.arc.nasa.gov\">NASA
  WorldWind</A>-based GUI.</P>"
category: News
---
<P>From&nbsp; Felix Hoffmann: </P>
<P>The <A href="http://www.dlr.de/kn">Institute of Communications and Navigations</A> at the <A href="http://www.dlr.de">German Aerospace Center (DLR)</A> is currently developing a simulation platform for aeronautical communications within the project <EM>FACTS - Future Aeronautical Communications Traffic Simulator</EM>. The project investigates the possibilities of shifting from voice communications to digital data traffic in Air Traffic Control, and creating an IP-based aeronautical telecommunications network. The simulator is based on OMNeT++ and the INET Framework, and will feature a <A href="http://worldwind.arc.nasa.gov">NASA WorldWind</A>-based GUI.</P><P>The field of aeronautical communications is currently undergoing significant changes. Up to now, Air Traffic Control (ATC) has been carried out mainly by means of analog voice communication between the controller and the pilot. In the future, ATC will make increasing use of data traffic in order to be able to cope with the increasing number of flights. This has led to a demand for new aeronautical data links that provide a high data rate and sufficient quality of service for such a safety critical environment. </P>
<P>A second trend is the use of IP in aeronautical communications. In the future, an IP-based aeronautical telecommunications network will integrate different types of link technologies (e.g. satellite links, aviation-specific air/ground data links, Wimax or WiFi links at the airport, etc.) into one single heterogeneous network. Among the features that it will need to support are global mobility, QoS provisioning for safety critical data, and seamless handovers between different link technologies. </P>
<P>To support research being conducted in these areas, our group at the Institute of Communications and Navigations at the German Aerospace Center is currently developing a simulation platform specifically for aeronautical communications within the project FACTS - Future Aeronautical Communications Traffic Simulator. This simulator is based on OMNeT++ and the INET framework. </P>
<P>Although we are still in the implementation phase, the final version of our simulator will support:</P>
<UL type=DISC>
<LI>Realistic representation of air traffic: A sequence of waypoints for each airplane is generated from a database of all scheduled flights worldwide. An OMNeT++ mobility module within the aircraft node interpolates between these waypoints.
<LI>Integration of ATC sectors in Europe, as well as the ground stations used for data communication
<LI>Modelling of data applications used for ATC. Such applications may be triggered e.g. when an airplane enters a new ATC sector and must register with the controller responsible for that sector. </LI></UL>
<P>To accomplish this, several modifications to OMNeT++/INET are required:</P>
<UL type=DISC>
<LI>support for three dimensional movement of nodes, representation of coordinates in form of latitude, longitude, elevation
<LI>support for multiple technologies/network interfaces onboard an aircraft (requiring changes to the ChannelControl module)
<LI>additional GUI based on NASA World Wind. WorldWind is a virtual globe that is available as open source and is programmed in Java. This allows us to display air traffic worldwide, in three dimensions, draw ATC sectors, etc. </LI></UL>
<P>Upon completion, possible applications for our simulator may include</P>
<UL type=DISC>
<LI>capacity analysis of new data links in the aeronautical context
<LI>network-layer simulations, e.g. handover between different technologies; this could occur when an airplane is no longer within range of a terrestrial base station and must switch to a satellite link </LI></UL>
<P>The first figure below shows a simulation scenario containing all scheduled flights in Europe within a certain thirty minute time slot on May 21, 2007. This amounts to roughly 2,700 aircraft. Base stations are depicted as red cones, and connections between airplanes and base stations are shown as white lines. The transmission range is typically limited by the radio horizon, and is about 200 nautical miles.</P>
<P><img width="300" height="225" src="/images/omnetpp/20070926144402513_1.jpg" alt=""></P>
<P>The next figure shows the WorldWind window in front of the OMNeT++ Tkenv window. The messages that are scheduled on OMNeT++ are all “move” messages of the aircrafts’ mobility modules.</P>
<P><img width="300" height="225" src="/images/omnetpp/20070926144402513_2.jpg" alt=""></P>
<P>The last figure shows a less dense traffic scenario, from a perspective closer to the Earth’s surface. These figures simply show an alternate visualization of the OMNeT++ simulation. All aircraft and base stations are represented as compound modules within OMNeT++, the distances are calculated by a modified version of ChannelControl. </P>
<P><img width="300" height="225" src="/images/omnetpp/20070926144402513_3.jpg" alt=""><BR></P>
