XS Computer One - Apple 1 Replica Project
=========================================

About
-----

This project is an attempt to build a working replica of the [Apple-1] computer, made in 1976 by Steve Wozniak and released by Apple Computer Company, now Apple, Inc.

Only about 200 units of this computer were made. Today, only about 60 units still exists, and less than 10 are known working.  
They are sometimes sold at auctions, for record prices. In 2012, one was sold for $671,000.

To my knowledge, three replica projects exists:  
[Replica-1] by Vince Briel, [Mimeo-1] by Mike Willegal, and Obtronix by Steve Gabaly.

The last two are exact replicas, while the first one uses actual components with a different motherboard layout.

So this project will be (hopefully) a fourth one.

I decided to build my own replica from scratch, including the PCB design, as it's a very nice occasion to learn about electronics.  
As a programmer, I sometimes feel frustrated not to know more about this... ; )

[Apple-1]:   http://en.wikipedia.org/wiki/Apple_I
[Replica-1]: http://www.brielcomputers.com/wordpress/?cat=17
[Mimeo-1]:   http://www.willegal.net/appleii/apple1.htm

### Roadmap

There's of course no real roadmap yet, as I'm currently learning as I go. The project will surely takes a huge amount of time, so don't expect results too soon.

Here are the actual project parts:

| # | Part                     | Status      | Description                                                                              |
|---|--------------------------|-------------|------------------------------------------------------------------------------------------|
| 1 | Learn                    | In progress | Learn as much as possible on electronics, as I'm completely new to this.                 |
| 2 | Test                     |             | Experiment with a few basic PCB and components.                                          |
| 3 | Component Identification | Done        | Get the original component specification from the original schematics and documentation. |
| 4 | Component Purchase       | In progress | Purchase components or find alternatives if they are not available anymore.              |
| 5 | ROM                      |             | Find a way to get the original ROM and have it built somehow.                            |
| 6 | Prototype                |             | Get a prototype working on a breadboard.                                                 |
| 7 | PCB Design               |             | Design the final PCB, as close as possible to the original Apple-1, and have it printed. |
| 8 | Mounting                 |             | Mount all components on the motherboard.                                                 |

Tools & Equipment
-----------------

Here are the tools I'll use for this project:

| Manufacturer       | Part No.       | Details                           | Alternative | Quantity | Found | Status |
|--------------------|----------------|-----------------------------------|-------------|----------|-------|--------|
| B&K Precision      | [DP 21]        | Logic Probe / 20 MHz - 30 Ns      | N/A         | 1        | Yes   | -      |
| Fluke              | [87-V]         | True RMS Digital Multimeter       | N/A         | 1        | Yes   | -      |
| Global Specialties | [PB-105T]      | Breadboard                        | N/A         | 1        | Yes   | -      |
| Power Bright       | VC500W         | 120 V / 220 V Voltage Transformer | N/A         | 1        | No    | -      |
| Weller             | WECP-20        | Soldering Station                 | N/A         | 1        | No    | -      |
| Weller             | [7881]         | Desolder Pump                     | N/A         | 1        | Yes   | -      |
| Kester             | [24-6040-0027] | Solder / 60/40 - 0.79 mm          | N/A         | 1        | Yes   | -      |
| ArcOne             | G-FLY-A1101    | Safety Goggles                    | N/A         | 1        | Yes   | -      |
| CadSoft            | [EAGLE]        | PCB Design Software               | N/A         | 1        | Yes   | -      |

***Note:*** *Any equivalent tool may be used.*

[DP 21]:        https://ch.mouser.com/Search/ProductDetail.aspx?R=DP_21virtualkey61500000virtualkey615-DP-21
[87-V]:         http://ch.mouser.com/ProductDetail/Fluke/FLUKE-87-V/?qs=sGAEpiMZZMuBVu7Wy0UTy5lFkCyOv5Wu
[PB-105T]:      https://ch.mouser.com/Search/ProductDetail.aspx?R=PB-105Tvirtualkey51000000virtualkey510-PB-105T
[7881]:         https://ch.mouser.com/Search/ProductDetail.aspx?R=7881virtualkey57800000virtualkey578-7881
[24-6040-0027]: https://ch.mouser.com/Search/ProductDetail.aspx?R=24-6040-0027virtualkey53300000virtualkey533-24-6040-27
[EAGLE]:        http://www.cadsoftusa.com/eagle-pcb-design-software/?language=en

Documentation
-------------

I'm using the original schematics and original Apple-1 photos in order to identify the components and build the PCB.  
The original [**Apple-1 Operation Manual**](https://github.com/macmade/XS-Computer-One/blob/master/Documentation/Apple-1%20Operation%20Manual.pdf?raw=true) is included in the repository.

Bill Of Materials
-----------------

The complete list of the Apple-1 components can be found in the [BOM.md](https://github.com/macmade/XS-Computer-One/blob/master/BOM.md) file.

When the components are still available for purchase, links are provided ([Mouser Electronics](http://www.mouser.com/)).  
For vintage components, valid alternatives may be provided. In such a case, I try to find components that look the same as the original.

Unfortunately, I haven't been able to find alternative for all components, so your best option to find those parts is on sites like [eBay](http://www.ebay.com/). Note that rare/vintage components can be expensive.

Schematics
----------

Here's a schematic of motherboard layout, with all components.  
Note that the components' size is not respected, and their position is not always totally correct, but it's still better than looking at original pictures for quick component identification:

![](https://github.com/macmade/XS-Computer-One/raw/master/Schematics/Apple-1 Board.png)

Repository Infos
----------------

    Owner:			Jean-David Gadina - XS-Labs
    Web:			www.xs-labs.com
    Blog:			www.noxeos.com
    Twitter:		@macmade
    GitHub:			github.com/macmade
    LinkedIn:		ch.linkedin.com/in/macmade/
    StackOverflow:	stackoverflow.com/users/182676/macmade
