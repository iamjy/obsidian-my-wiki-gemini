---
title: "[Comprehensive Explanation] MIPI is not difficult! Newbies learn the MIPI standard from scratch ~ Basics Part 1 What is D-PHY? ~ - Semiconductor Business"
source: "https://www.macnica.co.jp/en/business/semiconductor/articles/lattice/141510/"
author:
published:
created: 2026-05-09
description: "What is the MIPI standard? This is a Lattice Terakoya that teaches everything from the basics of the MIPI interface standard (MIPI DSI/CSI-2) to the design method."
tags:
  - "clippings"
---
Hello! I'm Hiromin from Lattice team rookie FAE!

This blog is my study process about MIPI standards.

What is MIPI? What are the differences between the DSI/CSI-2 standards? How to design with Lattice FPGA?

From the basics to applications, I would like to tell you everything I have learned!

Now, I would like to learn the basics of the MIPI interface according to the table of contents.

You can also go directly to the part you want to learn by the links below, please check it out!

\[What you can learn from this article\]  
Learn about the basics of the MIPI standard, the differences and examples of DSI/CSI-2!

・ [What is the MIPI standard? Physical layer (D-PHY) and protocol layer (DSI/CSI-2)](#link1)

・ [What is D-PHY? Does the configuration change with DSI/CSI-2? ~](#link2)

・ [What is D-PHY? Electrical characteristics and transfer modes](#link3)

・ [What is D-PHY ~Comparison with LVDS~](#link4)

You can all read the study blogs related to MIPI from the summary link below.

I am happy if you are interested!

[\[Thorough explanation\] MIPI is not difficult! Summary of MIPI standards for newcomers to learn from scratch](https://www.macnica.co.jp/en/business/semiconductor/articles/lattice/141503/)

## What is the MIPI standard? Physical layer (D-PHY) and protocol layer (DSI/CSI-2)

First, let's learn what kind of standard MIPI is!

MIPI is an abbreviation for Mobile Industry Processor Interface, and is a standard established in 2005 by the standardization body MIPI Alliance.

This interface is mainly used for camera-related products such as smartphones, industrial equipment, and automotive applications.

MIPI can be divided into physical layer and protocol layer. The physical layer includes D-PHY, M-PHY, C-PHY, and A-PHY.

Each is as shown in the figure below.

![](https://www.macnica.co.jp/business/semiconductor/articles/3c8df2dd4d225a95c7df7f4042dd63d5.png)

I want to finally verify with the actual machine with Lattice FPGA

because I would like to learn more about MIPI D-PHY that Lattice supports.

There are two types of protocols in MIPI D-PHY, each with different uses.

CSI-2 is a protocol that is often used around cameras, and DSI is a protocol that is often used around displays.

## What is D-PHY? Does the configuration change with DSI/CSI-2? ~

Let's study D-PHY first!

Is there any differences in DSI/CSI-2? I would like to deepen my understanding of D-PHY by comparing it with LVDS.

D-PHY is the physical layer, and each configuration of DSI/CSI-2 is as follows.

![](https://www.macnica.co.jp/business/semiconductor/articles/e98bbcc389696f45f9bb630b95ba56e4.png)

First, the DSI configuration. Basically 1 lane for clock and 1, 2, 4 data lanes for data.

Both will be differential signals and the clock will be DDR operation.

Next is the configuration of CSI-2. The configuration of D-PHY is the same as that of DSI.

So what is the difference?  
  
The DSI/CSI-2 difference has a difference in Data Lene0. DSI seems to be able to bi-directionally communicate with DataLane0!

DSI can communicate with Slave devices using this Data Lane0.

The configuration of D-PHY is DSI/CSI-2 Basically the configuration is the same, the only difference is that Data Lane 0 becomes bi-directional communication in DSI!

## What is D-PHY? Electrical Characteristics and Transfer Modes

Next, I would like to learn about the electrical characteristics of D-PHY.

D-PHY seems to have two transmission modes, ow Power (LP) Mode / High Speed (HS) Mode .

Data is output as a single-ended output with 1.2V amplitude in LP Mode and as a differential output with ±200mV amplitude in HS Mode.

So why are there two modes? Let's look at the waveform during the transfer below.

![](https://www.macnica.co.jp/business/semiconductor/articles/LPHS.png)

I would like to learn more about the above waveforms in the next installment.

As far as this waveform is concerned, it seems that data transfer is performed by switching between LP Mode and HS Mode.

The transmission distance is 30 cm, and the data transmission speed is HS: Max 2.5 Gbps, LP: Max 10 Mbps.

Data is output as a single-ended output with 1.2V amplitude in LP Mode and as a differential output with ±200mV amplitude in HS Mode.

It turns out that communication is performed by switching LP/HS!

D-PYH seems to be a point that this LP-HS can be switched in the chip.

Compared to other standards, it may give you a better image.

Compare the difference between LVDS and MIPI communication!

## What is D-PHY ~Comparison with LVDS~

I have heard about LVDS several times since I joined the company, and I am more familiar with communication than MIPI.

However, I don't know the details, so I thought it would be useful to study more about it, so I made a comparison table!

<table><tbody><tr><td></td><td><p>MIPI D-PHY</p></td><td><p>LVDS</p></td></tr><tr><td><p>Transmission distance</p></td><td><p>Short distance (Max 30cm)</p></td><td><p>　Max 10m</p></td></tr><tr><td rowspan="2"><p>Per lane<br>transfer speed</p></td><td><p>HS: Max 2.5Gbps</p></td><td rowspan="2"><p>Max 655Mbps</p></td></tr><tr><td><p>LP: Max 10Mbps</p></td></tr><tr><td rowspan="2"><p>Electrical signal (amplitude)</p></td><td><p>HS: Differential p-p200 mV</p></td><td rowspan="2"><p>Differential pp 350 mV</p></td></tr><tr><td><p>LP: Single-ended 1.2V</p></td></tr><tr><td><p>Common voltage</p></td><td><p>HS: 330mV, LP: 0.6V</p></td><td><p>0.2 to 2.2V</p></td></tr><tr><td><p>Constant current source</p></td><td><p>2.0mA</p></td><td><p>3.5mA</p></td></tr><tr><td><p>Clock method</p></td><td><p>DDR source sync</p></td><td><p>DDR source sync</p></td></tr><tr><td><p>Others</p></td><td><p>Transfer clock signals separately from data lines<br>HS (High Speed) Mode,<br>LP (Low Power) Mode transition available</p></td><td><p>Clock signal to the data line<br>transferred separately</p></td></tr></tbody></table>

From the table above, we can see that MIPI can communicate faster than LVDS even though the transmission distance is shorter!

I didn't know that LVDS can communicate with Max10m, so I learned a lot by comparing them.

This is the end of our study for today. From next time, we will take a closer look at each of the MIPI DSI/CSI-2 protocol layers!

At the last:

My impression is that the physical layer (D-PHY) is not much different from DSI/CSI-2, and I got a better image by comparing it with LVDS!

If the physical layer doesn't change that much, will there be a big difference in the protocol layer? Hiromin is wondering.

Well, see you next time in Part 2, MIPI DSI Part 1! Bye!

[![](https://www.macnica.co.jp/business/semiconductor/articles/9ea7c12e8731b3cd516323ec5d3386e2_20.png)](https://www.macnica.co.jp/en/business/semiconductor/articles/lattice/141662/)

[Previous](https://www.macnica.co.jp/en/business/semiconductor/articles/lattice/141503/) articleThe hard work of a [of articlesNext article](https://www.macnica.co.jp/en/business/semiconductor/articles/lattice/141662/)

[Struggle story of a new engineer ~MIPI standard version~ List of articles](https://www.macnica.co.jp/en/business/semiconductor/articles/lattice/141503/)

### New Engineer's Struggle Journal -MIPI standard version-

The MIPI standard is a communication standard often used in recent years for display interfaces and image sensor output interfaces.  
  
I know the name of the standard, but what is the communication band? What protocol are you using?  
  
Among MIPI, this article focuses on DSI/CSI for newcomers to study from scratch.  
  
We are creating articles about the MIPI standard with the motto of making it easier to understand and more fun than other articles.  
  
Would you like to study with a newcomer?