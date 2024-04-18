---
download: true
layout: download-details
title: ProcessBusIec61850 - IEC61850 process bus communication (GOOSE and SV) for INET
years-active: 2015-
category: models
tags: model inet3 omnetpp5
keywords: electrical, grid, process, bus
github-url: https://github.com/hectordelahoz/ProcessBusIec61850/
opp-env-command: opp_env install processbus_allinone-latest
---

This project contains an OMNeT++/INET extension to support IEC61850 process bus
communication (GOOSE and SV). The followings simulation models were developed:

- Merging Unit simulation model that permits to configure the sample rate
  (protection profile and measurement profile).
- Protection and Control (P&C) IED simulation model that process SV and GOOSE
  messages but only generates GOOSE messages.
- Networking Switch simulation model that suports IEEE 802.1q VLAN and Priority
  Tagging using fixed priorities Queues. This project is intended for
  educational purpose.

IEC 61850 is an international standard defining communication protocols for
intelligent electronic devices at electrical substations.